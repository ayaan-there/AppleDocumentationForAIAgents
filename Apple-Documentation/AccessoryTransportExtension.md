# AccessoryTransportExtension Documentation

Source: https://sosumi.ai/documentation/accessorytransportextension

---
title: AccessoryTransportExtension
source: https://developer.apple.com/documentation/accessorytransportextension
timestamp: 2026-02-13T19:06:29.558Z
---

## Essentials

- [com.apple.developer.accessory-transport-extension](/documentation/bundleresources/entitlements/com.apple.developer.accessory-transport-extension)

## App extensions

- [AccessoryTransportAppExtension](/documentation/accessorytransportextension/accessorytransportappextension)

### Interacting with a session

- [func accept(sessionRequest: AccessoryTransportSession.Request) -> AccessoryTransportSession.Request.Decision](/documentation/accessorytransportextension/accessorytransportappextension/accept(sessionrequest:))
- [AccessoryTransportSession.Request.Decision](/documentation/accessorytransportextension/accessorytransportsession/request/decision)
- [AccessoryTransportExtensionConfiguration](/documentation/accessorytransportextension/accessorytransportextensionconfiguration)

## Transport sessions

- [AccessoryTransportSession](/documentation/accessorytransportextension/accessorytransportsession)

### Handling a session request

- [AccessoryTransportSession.Request](/documentation/accessorytransportextension/accessorytransportsession/request)

#### Accepting and rejecting session requests

- [func accept<Handler>(() -> Handler) -> AccessoryTransportSession.Request.Decision](/documentation/accessorytransportextension/accessorytransportsession/request/accept(_:))
- [func reject(error: AccessoryTransportSession.Error?) -> AccessoryTransportSession.Request.Decision](/documentation/accessorytransportextension/accessorytransportsession/request/reject(error:))
- [AccessoryTransportSession.Request.Decision](/documentation/accessorytransportextension/accessorytransportsession/request/decision)

#### Inspecting request properties

- [let session: AccessoryTransportSession](/documentation/accessorytransportextension/accessorytransportsession/request/session)

### Handling events

- [AccessoryTransportSession.EventHandler](/documentation/accessorytransportextension/accessorytransportsession/eventhandler)

#### Handling session cancellation

- [func invalidationHandler(error: AccessoryTransportSession.Error?)](/documentation/accessorytransportextension/accessorytransportsession/eventhandler/invalidationhandler(error:))
- [AccessoryTransportSession.Error](/documentation/accessorytransportextension/accessorytransportsession/error)

##### Handling session errors

- [case invalidated](/documentation/accessorytransportextension/accessorytransportsession/error/invalidated)

##### Handling accessory errors

- [case unsupported](/documentation/accessorytransportextension/accessorytransportsession/error/unsupported)

##### Handling unknown errors

- [case unknown](/documentation/accessorytransportextension/accessorytransportsession/error/unknown)

##### Describing an error

- [var description: String](/documentation/accessorytransportextension/accessorytransportsession/error/description)

### Canceling a session

- [func cancel(error: AccessoryTransportSession.Error?)](/documentation/accessorytransportextension/accessorytransportsession/cancel(error:))
- [AccessoryTransportSession.Error](/documentation/accessorytransportextension/accessorytransportsession/error)

#### Handling session errors

- [case invalidated](/documentation/accessorytransportextension/accessorytransportsession/error/invalidated)

#### Handling accessory errors

- [case unsupported](/documentation/accessorytransportextension/accessorytransportsession/error/unsupported)

#### Handling unknown errors

- [case unknown](/documentation/accessorytransportextension/accessorytransportsession/error/unknown)

#### Describing an error

- [var description: String](/documentation/accessorytransportextension/accessorytransportsession/error/description)

### Describing a session

- [var description: String](/documentation/accessorytransportextension/accessorytransportsession/description)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
