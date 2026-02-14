# App Tracking Transparency Documentation

Source: https://sosumi.ai/documentation/apptrackingtransparency

---
title: App Tracking Transparency
source: https://developer.apple.com/documentation/apptrackingtransparency
timestamp: 2026-02-13T18:53:21.369Z
---

## Essentials

- [NSUserTrackingUsageDescription](/documentation/bundleresources/information-property-list/nsusertrackingusagedescription)

## Class and Components

- [ATTrackingManager](/documentation/apptrackingtransparency/attrackingmanager)

### Requesting Authorization

- [class func requestTrackingAuthorization(completionHandler: (ATTrackingManager.AuthorizationStatus) -> Void)](/documentation/apptrackingtransparency/attrackingmanager/requesttrackingauthorization(completionhandler:))

### Determining Tracking Authorization Status

- [class var trackingAuthorizationStatus: ATTrackingManager.AuthorizationStatus](/documentation/apptrackingtransparency/attrackingmanager/trackingauthorizationstatus)
- [ATTrackingManager.AuthorizationStatus](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus)

#### Cases

- [case authorized](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus/authorized)
- [case denied](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus/denied)
- [case notDetermined](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus/notdetermined)
- [case restricted](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus/restricted)

#### Initializers

- [init?(rawValue: UInt)](/documentation/apptrackingtransparency/attrackingmanager/authorizationstatus/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
