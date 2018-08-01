# O2 Controls release notes
===========================

Unreleased
----------
- Added Chromecast dependency version check
- Minimal controls flavor (#68)
- Made vpaid ad clickable
- Splitted seekbar and timeLeft visibility properties

1.16 (2018-06-08 17:44:42 +0300)
--------------------------------
- Fixed TV devices not being able to select seek bar when using remote
- Fixed crash when dimensions are less then zero
- Made beon button not clickable when url is not present
- Updated slack token
- Implement BeOn design
- Click url handling
- Overlay advertisement text on branded content video
- Hook up updated gradle plugin for CI/CD with api changes tracking and snapshots
- Public api generation for each flavor
- Rework build script to produce flavour based setup
- Bump gradle version from 4.3 to 4.4

1.15 (2018-04-12 16:02:53 +0300)
--------------------------------
- Fix issue with rescale of controls
- Updated chromecast version
- Fixed Chromecast button not being colored with custom color
- Fix API changes generation bug
- Refactored Chromecast module usage
- Subtitle view removal from controls
- Copyright update
- MIT license

1.14 (2018-03-06 16:31:20 +0200)
--------------------------------
- Close button in TargetUrlActivity
- New close button for clickthrough presenter
- Links handling by WebView
- Click through url embed support for ad controls
- Fixed spinner control not being colored with custom color

1.13 (2018-02-27 13:23:04 +0200)
--------------------------------
- Public API tracking integration
- Chromecast app id should not be accessible
- Talkback strings update
- Midroll markers for android
- Slack integration update
- Travis CD fix
- AssertJ version bump

1.12 (2018-01-18 16:15:21 +0200)
--------------------------------
- AssertJ version bump
- Remove cast logic from controls
- Update player UI for that state when video is being streamed to the chromecast
- Chromecast fix
- Chromecast fix
- Video is played on the ChromeCast event if 'isScreenCastingEnabled' is false
- Add titles to all buttons in default controls
- Update player UI for that state, when video is being streamed to the chromecast
- License and copyright update, reformat and imports optimization of sources
- cast fix
- Proguard rule fix
- Chromecast button integration
- Naming update
- Update assertj-core to 3.3.0
- Travis update
- Update to 27th platform API

1.11 (2017-11-10 18:17:21 +0200)
--------------------------------
- Proguard support
- Android gradle plugin 3.0.0 support
- Android gradle plugin update to 3.0.0
- Chromecast implementation
- Support for snapshots build
- Kotlin support added

1.10 (Wed Sep 20 19:18:43 2017 +0300)
-------------------------------------
- Live label have to be in upper left corner

1.9.1 (2017-09-13 14:11:47 +0300)
---------------------------------
- Added live label to livestream video
- Tracks list scroll issue

1.9 (2017-09-05 16:30:36 +0300)
-------------------------------
- Controls for track selection
- Resource update

1.8 (2017-07-19 18:19:46 +0300)
-------------------------------
- Fixed too small hit-area for <| and |> buttons
- Fixed wrong initial position of cc container

1.8-alpha (2017-07-03 16:11:42 +0300)
-------------------------------------
- Bintray migration

1.7 (2017-06-26 17:22:15 +0300)
-------------------------------
- Fix touch transparency for content controls

1.7-alpha (2017-06-14 18:19:51 +0300)
-------------------------------------
- Always dispatch touch to controls view

1.6 (2017-05-23 14:03:05 +0300)
-------------------------------
- AOMSDK-1169 Play button is not visible in case when autoplay is set to False
- Travis CI settings
- Template param removal
- Initial commit
