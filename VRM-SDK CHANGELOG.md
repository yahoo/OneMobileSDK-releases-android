# O2 Vrm-sdk release notes
==========================

Unreleased
----------
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
- SDK internal framework
- Licencse update
- Add stubs for VRM sdk
- Public API tracking hookup
- remove MainThread annotation
- Updated package name, names of classes, license
- Update VrmAd.java
- Update README.md
- Common files update
- Initial commit
