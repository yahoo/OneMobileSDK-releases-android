# O2 Vrm-sdk release notes
==========================

2.0.2 (2018-11-26 14:33:04 +0200)
---------------------------------
- Fixed ad_oppty to have the same detection logic as adRequest
- Update for workflow tests
- Update public interface
- actions update
- Detectors for icon
- State to represent when icon view is shown/hidden State to represent icon clickthrough shown/hidden
- Update public interface with Icons information
- Merge icons from wrappers inside final inline
- Parse `Icons` from VAST

2.0.1 (2018-11-06 12:33:04 -0800)
---------------------------------
- Move jacoco checks to debug build type

2.0.0 (2018-10-31 22:58:21 +0200)
---------------------------------
- videoWithPrerollSlotWithNoAdsInVast fix
- Fixed SlotOpp for empty slot
- Fixed firing SlotOpp multiple times for same ad
- videoWithNoAdsInVrm fix
- Fixed SlotOpp detector
- trk/ad-request.gif fix
- fix params of trackers in the end of ads
- Several ads fix
- Fixed failed media file case
- Fixed test app
- Quartile 4 is not fired for videoWithEmptyBumperSlot
- TestApp update
- Fixed bats beacons not being reported in TestApp
- Additional params for ad_view beacon
- VRM 2.0 initial implementation
- State extension for VRM 2.0
- Ads session concept
- Jacoco and Danger integration
- Vrm 2.0 parser

1.3.4 (Tue Sep 11 18:39:40 2018 +0300)
--------------------------------------
- Update vrm sdk test app for skip
- Added ad skip beacons tracking
- Added ad skip pixel tracking
- Add ad skip collback logic and isSkipped to ad playback state
- SkipOffset parsing Fix ad duration issue

1.3.3 (Tue Aug 14 15:57:07 2018 +0300)
--------------------------------------
- Move VrmItemResultFilter out of parser
- r implementation in pixels
- VAST 3.0 support

1.3.2 (Tue Jul 17 17:35:13 2018 +0300)
--------------------------------------
- Crash after integrating with Sports app
- Networks returned as id, not name for Yahoo Sports Android
- Remove duplicate detectors

1.3.1 (Wed Jul 11 19:36:20 2018 +0300)
--------------------------------------
- Ad finish BATS detector fix
- Update Gemfile
- Add danger support

1.3.0 (2018-06-27 18:58:03 +0300)
---------------------------------
- Empty ads fix
- Lower case BATS beacons name
- Load win detector fix
- Fix of content duration update
- Ad load/win detector fix
- Slot opportunity detector fix
- vvuid param is missed in ad-engine-flow.gif tracker
- Slot opportunity pixel implementation
- Context start pixel fix
- Store wireup with logic at VRMSDK constructor
- vast/click is fired only once
- Custom environment support
- Proper hard timeout fire timing
- Make `vid` parameter not required
- vvuid param is missed in ad-engine-flow.gif tracker
- Updated test app
- Add AdRequestDetector
- Add AdViewabilityDetector
- Context start tracking pixel
- Content complete tracking pixel
- Tests update
- Add AdViewTimeDetector

1.2.0 (2018-06-22 19:42:36 +0300)
---------------------------------
- Environment as mandatory field
