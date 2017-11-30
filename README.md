# One Mobile SDK for Android

This SDK provides easy way to integrate video playback inside your application with high
customization ability, advertisement support, metrics and O2 video provider integration.

Release notes can be found [here](CHANGELOG.md).

## Introduction

SDK consists of several core classes:

- __OneSDK__ - core class, entry point that constructs __Player__ with O2
  metrics attached and O2 playlist or video[s].

- __Player__ - main class that handles all internal logic for playback,
  advertisement and metrics.

- __PlayerView__ - content video and advertisement rendering view

- __Binder__ - helper class that manages connection between __Player__ and __PlayerView__

- __PlayerFragment__ - easy to use fragment with __PlayerView__ and properly constructed __Binder__.

## Integration guide

### Gradle integration

In `dependencies` section of modules `build.gradle` add reference
to SDK library:

```gradle

// Add SDK maven repository
allprojects {
    repositories {
        maven { url 'https://raw.github.com/aol-public/OneMobileSDK-releases-android/maven/' }
    }
}

apply plugin: 'com.android.application'

android {
    // ...
}

dependencies {
    // ...

    // AOL ONE Mobile SDK
    compile 'com.aol.one.publishers.android:sdk:2.12' // Use latest version

    // ...   
}
```

Javadoc can be found [here](vidible.github.io/mobile-sdk-android). You can attach them in Android
Studio manually using this
[guide](http://stackoverflow.com/questions/20994336/android-studio-how-to-attach-javadoc#answer-34721648).

### Sources integration

To start using the ONE Mobile SDK, you will first need to construct an instance of __OneSDK__.

```java
new OneSDKBuilder(getApplicationContext())
    .setEnvironment(environment)
    .create(new OneSDKBuilder.Callback() {
            public void onSuccess(OneSDK oneSDK) {

            }

            public void onFailure(Exception error) {

            }
        });
```
(__Environment__ can be __PRODUCTION__ -or- __STAGE__)

Use ```setExtra(JSONObject extra)``` to set Extra data for __OneSDK__ request (optional parameter)

Next step will be obtaining a __Player__ instance using __PlayerBuilder__

```java
PlayerBuilder playerBuilder = sdk.createBuilder();
```

__PlayerBuilder__ has many parameters that can be modified:
- vvuidGenerator
- autoplay
- modelTransformer
- prerollPodSize
- siteSection

Then create player by __videoId__

```java
playerBuilder.buildForVideo(String videoId, Player.Callback callback);
```

-or- by an array of __videoId__

```java
playerBuilder.buildForVideoList(String[] videoIds, Player.Callback callback);
```

-or- by __playlistId__

```java
playerBuilder.buildForPlaylist(String playlistId, Player.Callback callback);
```

If you want to check some received data you can use
```java
playerBuilder.requestForVideo(String videoId, VideoProvider.Callback callback);
playerBuilder.requestForVideoList(String[] videoIds, VideoProvider.Callback callback);
playerBuilder.requestForPlaylist(String playlistId, VideoProvider.Callback callback);
```
and then call
```java
playerBuilder.buildFrom(VideoProviderResponse videoProviderResponse)
```
with __VideoProviderResponse__

Using __Binder__ instance connect __PlayerView__ to __Player__:

```java
PlayerView playerView = new PlayerView(context);
Binder binder = new Binder();

binder.getPlayerView(playerView);
binder.setPlayer(player);
```

Snap __Binder__ to Android UI lifecycle:

```java
public onPause() {
    binder.onPause();
}

public onResume() {
    binder.onResume();
}

public void onDestroy() {
    playerView.dispose();
    binder.onDestroy();
}
```

Or you can use __PlayerFragment__:

```java
PlayerFragment playerFragment = // ... Constructed PlayerFragment

playerFragment.getBinder().setPlayer(player);
```

For handling player errors, add __ErrorListener__

```java
player.addErrorListener(new ErrorListener() {
    public void onError(ErrorState errorState) {
    }
});
```

You can add custom detectors of player state
```java
player.addPlayerStateObserver(new DecileDetector(new DecileDetector.Callback() {
    //You can use any detector from package com.aol.mobile.sdk.player.listener.detector
    public void onDecileDetected(@NonNull Properties properties, int i) {
    }
}));

player.addPlayerStateObserver(new PlayerStateObserver() {
    //You can use any custom detector witch detect any state by properties
    public void onPlayerStateChanged(@NonNull Properties properties) {
    }
});
```

All done!

## Player controls

SDK provides easy and flexibly approach for video controls and behavior customization.
Key class `UiProperties` represent basic view model that will be rendered to user and
`ControlsFeedbackHandler` interface implementation is responsible for controls behavior modification.

### Theming of controls

`PlayerControlsView` introduces `setMainColor` and `setAccentColor` methods together
with `mainColor` and `accentColor` xml attributes for enhanced controls coloring support.

Usage in Java:

```java
  PlayerControlsView controls = (PlayerControlsView) playerView.getContentControls();
  controls.setMainColor(0XFFFFFF);
  controls.setAccentColor(0XB53087);
```

Usage in xml:

```xml
<com.aol.mobile.sdk.controls.view.PlayerControlsView
      android:id="@+id/controls"
      android:layout_width="match_parent"
      android:layout_height="match_parent"
      app:mainColor="@color/main_controls_color"
      app:accentColor="@color/accent_controls_color" />
```

### Hiding of buttons

To hide some particular button you will need to extend `PlayerControlsView` and override *`render`*
method:

```java
void render(UiProperties props) {
    props.isSeekForwardButtonVisible = false;
    props.isSeekBackButtonVisible = false;
    super.render(props);
}
```

Snippet above will hide +/- 10 sec seek buttons.
Each property can be modified to achieve required UI.

Next what you should do is set your implementation of controls to `PlayerView` using:

```java
PlayerView player view = ...
playerView.setVideoControlsView(yourCustomControlsView);
```

### Custom controls

In case when you need fully customized UI you will have to implement `PlayerControls` interface.
You will have to properly render `UiProperties` inside `render` method like this:
```java
public void render(UiProperties props) {
    // Render of loading indicator
    if (progressView.getVisibility() != VISIBLE && props.isLoading) {
        progressView.setVisibility(VISIBLE);
    } else {
        progressView.setVisibility(GONE);
    }
    // And all other controls
}
```
Also inside `setListener` you may be passed with listener that should be used to propagate SDK
with user interaction via controls.

### Behaviour modification

Interface `ControlsFeedbackHandler` and class `DefaultFeedbackHandler` are responsible for interaction
of SDK with ui controls. For example if you need to override play button with custom action,
you will have to extend `DefaultFeedbackHandler` and override `onButtonClickMethod`:

```java
public class DefaultFeedbackHandler extends DefaultFeedbackHandler {
    public void onButtonClick(Player player, ControlsButton button) {
        switch(button) {
            case PLAY:
                // Do some important stuff
                break;

            default:
                super.onButtonClick(player, button);
                break;
        }
    }
}
```

then set your custom `ControlsFeedbackHandler` to `Binder`
```java
binder.setFeedbackHandler(new MyDefaultFeedbackHandler());
```

### Chromecast support

```gradle
dependencies {
    // ...

    // Chromecast
    compile 'com.aol.one.publishers.android:chromecast:1.0'

    // ...   
}
```

Add meta-data with castId of application to Manifest.xml
(https://developers.google.com/cast/docs/registration)

```xml
<manifest>
    <application>
      <!-- ...-->
        <meta-data
            android:name="com.aol.mobile.sdk.chromecast.ReceiverApplicationId"
            android:value="appCastId" />
    </application>
</manifest>
```
