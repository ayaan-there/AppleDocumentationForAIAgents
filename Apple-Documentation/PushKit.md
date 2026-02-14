# PushKit Documentation

Source: https://sosumi.ai/documentation/pushkit

---
title: PushKit
source: https://developer.apple.com/documentation/pushkit
timestamp: 2026-02-13T19:00:53.975Z
---

## Registration

- [Supporting PushKit Notifications in Your App](/documentation/pushkit/supporting-pushkit-notifications-in-your-app)
- [PKPushRegistry](/documentation/pushkit/pkpushregistry)

### Initializing a Push Registry

- [init(queue: dispatch_queue_t?)](/documentation/pushkit/pkpushregistry/init(queue:))

### Receiving the Notification Data

- [var delegate: (any PKPushRegistryDelegate)?](/documentation/pushkit/pkpushregistry/delegate)
- [PKPushRegistryDelegate](/documentation/pushkit/pkpushregistrydelegate)

#### Responding to Registration Events

- [func pushRegistry(PKPushRegistry, didUpdate: PKPushCredentials, for: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didupdate:for:))
- [func pushRegistry(PKPushRegistry, didInvalidatePushTokenFor: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didinvalidatepushtokenfor:))

#### Handling an Incoming Notification

- [func pushRegistry(PKPushRegistry, didReceiveIncomingPushWith: PKPushPayload, for: PKPushType, completion: () -> Void)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didreceiveincomingpushwith:for:completion:))

#### Deprecated Methods

- [func pushRegistry(PKPushRegistry, didReceiveIncomingPushWith: PKPushPayload, for: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didreceiveincomingpushwith:for:))

### Managing the Push Registry

- [var desiredPushTypes: Set<PKPushType>?](/documentation/pushkit/pkpushregistry/desiredpushtypes)
- [func pushToken(for: PKPushType) -> Data?](/documentation/pushkit/pkpushregistry/pushtoken(for:))
- [PKPushRegistryDelegate](/documentation/pushkit/pkpushregistrydelegate)

### Responding to Registration Events

- [func pushRegistry(PKPushRegistry, didUpdate: PKPushCredentials, for: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didupdate:for:))
- [func pushRegistry(PKPushRegistry, didInvalidatePushTokenFor: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didinvalidatepushtokenfor:))

### Handling an Incoming Notification

- [func pushRegistry(PKPushRegistry, didReceiveIncomingPushWith: PKPushPayload, for: PKPushType, completion: () -> Void)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didreceiveincomingpushwith:for:completion:))

### Deprecated Methods

- [func pushRegistry(PKPushRegistry, didReceiveIncomingPushWith: PKPushPayload, for: PKPushType)](/documentation/pushkit/pkpushregistrydelegate/pushregistry(_:didreceiveincomingpushwith:for:))
- [PKPushCredentials](/documentation/pushkit/pkpushcredentials)

### Getting the Token

- [var token: Data](/documentation/pushkit/pkpushcredentials/token)
- [var type: PKPushType](/documentation/pushkit/pkpushcredentials/type)

## Push Types

- [Responding to VoIP Notifications from PushKit](/documentation/pushkit/responding-to-voip-notifications-from-pushkit)
- [PKPushType](/documentation/pushkit/pkpushtype)

### Notification Types

- [static let complication: PKPushType](/documentation/pushkit/pkpushtype/complication)
- [static let fileProvider: PKPushType](/documentation/pushkit/pkpushtype/fileprovider)
- [static let voIP: PKPushType](/documentation/pushkit/pkpushtype/voip)

### Initializers

- [init(rawValue: String)](/documentation/pushkit/pkpushtype/init(rawvalue:))

## Payload

- [PKPushPayload](/documentation/pushkit/pkpushpayload)

### Payload Data

- [var dictionaryPayload: [AnyHashable : Any]](/documentation/pushkit/pkpushpayload/dictionarypayload)
- [var type: PKPushType](/documentation/pushkit/pkpushpayload/type)

## Data export

- [Exporting delivery metrics logs](/documentation/pushkit/exporting-delivery-metrics-logs)
- [Exporting broadcast push notification metrics](/documentation/pushkit/exporting-broadcast-push-notification-metrics)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
