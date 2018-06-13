# OneMobile SDK Renderer release notes
======================================

2.12 (2018-05-22 17:07:16 +0300)
--------------------------------
- Updated slack token
- Update build script to use androidCi plugin

2.11 (2018-04-30 15:50:09 +0300)
--------------------------------
- Bump gradle version to 4.4
- Fixed crash when chromecast module is not present
- Renderer gradle fix

2.10 (2018-03-26 16:34:39 +0300)
--------------------------------
- Updated chromecast version
- Fix API changes generation bug
- Refactored Chromecast module usage
- Subtitle rendering using ExoPlayer ui module
- Update ExoVideoRenderer.java
- ExoPlayer update to 2.7.1
- Ignore proguard-classes.pro
- Copyright update
- MIT license

2.9 (2018-02-27 13:34:50 +0200)
-------------------------------
- Public API tracking integration
- Slack integration update
- Travis CD fix

2.8 (2018-01-18 16:21:05 +0200)
-------------------------------
- ExoPlayer version bump to 2.6.1
- Delete empty video listener
- Stop casting
- Add empty video listener
- Stop casting logic
- Chromecast update
- Update player UI for that state, when video is being streamed to the chromecast
- Subtitles telemetry
- License and copyright update, reformat and imports optimization of sources
- castVM fix
- Naming update
- support-annotations fix
- Update exoplayer to 2.6.0
- Travis update
- Update assertj-core to 3.3.0
- Ads on chromecast
- Chromecast module structure update
- Update to 27th platform API

2.7 (2017-11-10 18:11:12 +0200)
-------------------------------
- Proguard support
- Prevent warning in RenderersRegistry
- Application is crashed when I try to play restricted video
- Android gradle plugin 3.0.0 support
- Android gradle plugin update to 3.0.0
- Move cast renderer to flat renderer
- OMSDK-302 Chromecast implementation
- Support for snapshots build
- Tools update
- Dynamic renderers detection support
- Kotlin support added

2.6.4 (Wed Sep 20 19:21:10 2017 +0300)
--------------------------------------
- ProtocolException: unexpected end of stream
- Update exoplayer to version 2.5.2

2.6.3 (2017-09-13 16:23:10 +0300)
---------------------------------
- Group audio tracks by language considering id

2.6.2 (2017-09-13 14:48:37 +0300)
---------------------------------
- Added automatic seeking to live edge for live videos
- Group audio tracks by language

2.6.1 (Tue Sep 12 18:00:17 2017 +0300)
--------------------------------------
- NullPointerException Attempt to invoke virtual method 'long java.lang.Long.longValue()'
- Pipeline for track changing

2.5 (Mon Aug 21 19:33:28 2017 +0300)
------------------------------------
- Extra renderer check
