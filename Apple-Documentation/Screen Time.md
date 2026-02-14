# Screen Time Documentation

Source: https://sosumi.ai/documentation/screentime

---
title: Screen Time
source: https://developer.apple.com/documentation/screentime
timestamp: 2026-02-13T19:01:39.220Z
---

## Essentials

- [STWebpageController](/documentation/screentime/stwebpagecontroller)

### Instance properties

- [var suppressUsageRecording: Bool](/documentation/screentime/stwebpagecontroller/suppressusagerecording)
- [var url: URL?](/documentation/screentime/stwebpagecontroller/url)
- [var urlIsBlocked: Bool](/documentation/screentime/stwebpagecontroller/urlisblocked)
- [var urlIsPictureInPicture: Bool](/documentation/screentime/stwebpagecontroller/urlispictureinpicture)
- [var urlIsPlayingVideo: Bool](/documentation/screentime/stwebpagecontroller/urlisplayingvideo)

### Instance methods

- [func setBundleIdentifier(String) throws](/documentation/screentime/stwebpagecontroller/setbundleidentifier(_:))

### Instance Properties

- [var profileIdentifier: STWebHistory.ProfileIdentifier?](/documentation/screentime/stwebpagecontroller/profileidentifier)

## Configuration queries

- [STScreenTimeConfigurationObserver](/documentation/screentime/stscreentimeconfigurationobserver)

### Initializers

- [init(updateQueue: dispatch_queue_t)](/documentation/screentime/stscreentimeconfigurationobserver/init(updatequeue:))

### Instance properties

- [var configuration: STScreenTimeConfiguration?](/documentation/screentime/stscreentimeconfigurationobserver/configuration)

### Instance methods

- [func startObserving()](/documentation/screentime/stscreentimeconfigurationobserver/startobserving())
- [func stopObserving()](/documentation/screentime/stscreentimeconfigurationobserver/stopobserving())
- [STScreenTimeConfiguration](/documentation/screentime/stscreentimeconfiguration)

### Instance properties

- [var enforcesChildRestrictions: Bool](/documentation/screentime/stscreentimeconfiguration/enforceschildrestrictions)

## Web-Usage data deletion

- [STWebHistory](/documentation/screentime/stwebhistory)

### Initializers

- [init(bundleIdentifier: String) throws](/documentation/screentime/stwebhistory/init(bundleidentifier:))
- [init(bundleIdentifier: String, profileIdentifier: STWebHistory.ProfileIdentifier?) throws](/documentation/screentime/stwebhistory/init(bundleidentifier:profileidentifier:))
- [init(profileIdentifier: STWebHistory.ProfileIdentifier?)](/documentation/screentime/stwebhistory/init(profileidentifier:))

### Instance methods

- [func deleteAllHistory()](/documentation/screentime/stwebhistory/deleteallhistory())
- [func deleteHistory(during: DateInterval)](/documentation/screentime/stwebhistory/deletehistory(during:))
- [func deleteHistory(for: URL)](/documentation/screentime/stwebhistory/deletehistory(for:))

### Structures

- [STWebHistory.ProfileIdentifier](/documentation/screentime/stwebhistory/profileidentifier)

#### Initializers

- [init(String)](/documentation/screentime/stwebhistory/profileidentifier/init(_:))
- [init(rawValue: String)](/documentation/screentime/stwebhistory/profileidentifier/init(rawvalue:))

### Instance Methods

- [func fetchAllHistory(completionHandler: (Set<URL>?, (any Error)?) -> Void)](/documentation/screentime/stwebhistory/fetchallhistory(completionhandler:))
- [func fetchHistory(during: DateInterval, completionHandler: (Set<URL>?, (any Error)?) -> Void)](/documentation/screentime/stwebhistory/fetchhistory(during:completionhandler:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
