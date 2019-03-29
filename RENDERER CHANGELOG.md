# O2 Renderer release notes
===========================

Unreleased
----------
- SDK should ignore the subtitle format if we can’t parse it

2.18 (2019-03-15 18:19:05 +0200)
--------------------------------
- specify compileSdkVersion
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
