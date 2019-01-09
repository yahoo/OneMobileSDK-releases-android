# O2 Vrm-sdk release notes
==========================

Unreleased
----------
- Remove unnecessary logs from vrm sdk
- Issues with proguard configuration in Android library causing logging and debugging issues in apps
- Action in one place
- Stash
- Actions
- Kotlin redux refactor

3.0.0 (2018-12-20 17:00:37 +0200)
---------------------------------
- Reducers refactoring
- No ads logic fix
- Trackers fix
- Further kotlin migration
- Slot index fix
- Fix stg param
- Tests fix
- Rewrite test app so it will proper react on new VRM SDK behavior
- Tests fix
- Rewrite of reporter code for multi ad state
- Ads session adapter rewrite
- Slots reducer
- Multiple AdPlayback
- Partial kotlin internals rewrite
- Support multiple vrm ad results in state
- Remove vrm 1.0 support
- Fix mtype, stg parameters in trackers
- Add vrmVersion to AdsSessionCallback
- Vrm version parsing
- bckt and expn params addition
- Run all vrm 2 test cases
- Fixed order of ad_oppty and ad_callf bats beacons
- Add instrumental tests for running all cases
- Fixed r_code for successful ad_call beacon

2.0.2 (Mon Nov 26 14:57:45 2018 +0200)
--------------------------------------
- Fix ar param of trk/ad-engine response Fix dt param of ad issue
- Fix ad_oppty for videoWithNoAdsInVrm and videoWithEmptyBumperSlot cases
- Fire ad_call with timeout
- Increment adSeq parameter with adEngine request
- Added vrmver to BatsBeacons
- Removed AdOpportunity pixel for VRM 2
- Linked ad_oppty to ad_call and ad_callf
- Lint fix
- r code update
- Public interface fix
- BatsBeaconsGenerator fix
- Fix medS param
- Remove ad_callf bats beacon
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
- Content start tracking pixel implementation
- Content viewport size tracking support
- Add AdViewTimeDetector
- Test application for VRM SDK
- Test application for VRM SDK (resources and cleanup)

1.2.0 (2018-06-22 19:42:36 +0300)
---------------------------------
- Environment as mandatory field
- Set of tracking pixels for vrm state tracking and ad playback
- Player id, buying company id and video id parsing from VRM response
- Opportunity beacon rework

1.1.0 (2018-06-20 16:36:10 +0300)
---------------------------------
- Content playback state
- <Duration> VAST tag parsed as seconds
- Beacon listener with event name param
- Store moved to VRMSDK
- Algebraic type refactoring
- Content playback tracking

1.0.1 (2018-06-15 19:06:56 +0300)
---------------------------------
- Action refactored to visitor pattern
- ProGuard namespace fix
- Filter mp4 ads
- Bats beacons params fill
- AdSystem VAST field parsing

1.0 (2018-06-13 18:02:51 +0300)
-------------------------------
- Playback state support
- Bats beacons initial support
- Playback actions
- Initial commit
- Common code cleanup
- Added detectort to AdDetectorsReporter
- Detectors update
- Add AdOpportunityDetector
- Add AdErrorDetector
- Add AdTagResponseSuccessDetector
- Add AdTagResponseFailureDetector
- Add AdPlaybackViewDetector
- Add StartAdDetector
- Add AdPlaybackEndDetector
- Add AdPlaybackQuartileDetector
- Added Bats tracking generator for yaml file
- Added o2-vrm-sdk-definitions submodule
- Add bats trackers reporter
- VrmCallback adapter and tests
- Services at one place, minor refactoring
- Stub implementation removal
- AdWrapper parsing
- Item fetching tests and implementation
- Tests update
- LogicUnit refactor
- Actions refactor
- Raw AsyncService and Cancellable concept
- HttpService clean up
- Fetch XML
- Ad wrapper support for easy VAST redirects handling
- Test data for parsing as raw string VrmResult update
- Parse XML
- LogicUnit refactor
- One more requirement added
- VrmResult hard timeout logic moved to reducer
- Actual logic
- Tests
- Logic unit abstraction
- Actions
- Removed userAgent and uiHandler;
- Vrm data fetcher
- State made immutable
- Middleware support added
- VrmResponse parsing business logic
- Refactor of state
- Framework application
- Logic and reducers
- Actions and observers
- Main state
- Redux core classes
- Debug flag moved to VRMContext
- Lib package change
- Parse Group
- Create vrm url
- Update public API for initial release
- Update public API for initial release
- SDK internal framework
- SDK internal framework
- Licencse update
- Licencse update
- Add stubs for VRM sdk
- Add stubs for VRM sdk
- Public API tracking hookup
- Public API tracking hookup
- remove MainThread annotation
- remove MainThread annotation
- Updated package name, names of classes, license
- Updated package name, names of classes, license
- Update VrmAd.java
- Update VrmAd.java
- SDK interface mockup v2.0
- SDK interface mockup v2.0
- SDK interface mockup
- SDK interface mockup
- Update README.md
- Update README.md
- Common files update
- Common files update
- Project files
- Project files
- Gradle core files
- Gradle core files
- Initial commit
- Initial commit

0.1 (2018-05-23 17:48:59 +0300)
-------------------------------
- Update public API for initial release
- SDK internal framework
- Licencse update
- Add stubs for VRM sdk
- Public API tracking hookup
- remove MainThread annotation
- Updated package name, names of classes, license
- Update VrmAd.java
- SDK interface mockup v2.0
- SDK interface mockup
- Update README.md
- Common files update
- Project files
- Gradle core files
- Initial commit
