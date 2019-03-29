# O2 Renderer-g3.0.0 release notes
==================================

2.19 (Fri Mar 29 14:07:30 2019 +0200)
-------------------------------------
- SDK should ignore the subtitle format if we can’t parse it

2.18 (2019-03-15 18:19:05 +0200)
--------------------------------
- specify compileSdkVersion

2.17 (Fri Mar 15 17:51:38 2019 +0200)
-------------------------------------
- another build fix
- Fixed build
- Implement switch for embedded cc style

2.16.1 (2018-12-13 17:15:54 +0200)
----------------------------------
- Custom ttml decoder, that makes hours timing optional
- Update README.md

2.16 (2018-12-12 13:36:09 +0200)
--------------------------------
- Proper language title in CC list
- Add language to TextTrack
- Subtitle type support of renderer
- Unify way of rendering external and internal subs inside of video renderer

2.15.1 (2018-12-05 16:51:12 +0200)
----------------------------------
- Upscale fix

2.15 (Thu Nov 22 17:04:58 2018 +0200)
-------------------------------------
- Update ExoPlayer to 2.8.4
- Android min API version downgrade to 16

2.14 (2018-08-30 14:06:26 +0300)
--------------------------------
- Bump minimal Android version to 19

2.13 (2018-08-07 14:42:25 +0300)
--------------------------------
- Fixed content being shown before ad playback
- Chromecast turn off
- Build plugin version bump
- Environment bump to latest version
- Added API for tracking visibility of video frames

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

2.6 (2017-09-05 16:13:58 +0300)
-------------------------------
- Pipeline for track changing

2.5 (Mon Aug 21 19:33:28 2017 +0300)
------------------------------------
- Extra renderer check
- Added passthrough of bitrate for hls video
- OMSDK-93 Update playback duration for live video

2.4 (2017-08-03 17:39:26 +0300)
-------------------------------
- Srt subtitles are ignored for hls videos, CC is enables only when subtitles url is present for video
- OMSDK-51 Update exoplayer to version 2.4.4
- Tune travis for CD
- Tune travis for CD

2.4-alpha (2017-06-30 17:32:36 +0300)
-------------------------------------
- Tune travis for CD
- Bintray migration

2.3 (Tue Jun 27 18:28:29 2017 +0300)
------------------------------------
- AOMSDK-1207 Crash after ad
- AOMSDK-1205 Long video buffering on mobile internet

2.3-alpha (2017-06-14 18:36:18 +0300)
-------------------------------------
- Orientation sensor moved to stock renderer

2.2 (Fri Jun 9 17:54:58 2017 +0300)
-----------------------------------
- AOMSDK-1193 Update Exoplayer to 2.4.1
- AOMSDK-1191 Incorrect broken trackers are fired after playAtIndex
- AOMSDK-1174 Investigate 'Baby's First Taste Of Chocolate' video problem Cross protocol redirection fix

2.1.1 (2017-05-23 19:22:35 +0300)
---------------------------------
- Build.gradle update for CD

2.1 (2017-05-18 19:56:39 +0300)
-------------------------------
- AOMSDK-1167 App is crashed when try to play this video: 5908a649e0fa1730350c3edf
- Travis CI settings
- Update after review
- AOMSDK-1157 Update VideoRenderer with properties

1.2 (Fri May 5 12:46:28 2017 +0300)
-----------------------------------
- Update version to 1.2
- Exoplayer update to 2.4.0
- AOMSDK-1136 Renderer refactoring
- AOMSDK-1133 Exoplayer update
- Renderers code addition
- Initial commit
