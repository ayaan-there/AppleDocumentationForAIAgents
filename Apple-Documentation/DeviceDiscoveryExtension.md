# DeviceDiscoveryExtension Documentation

Source: https://sosumi.ai/documentation/devicediscoveryextension

---
title: DeviceDiscoveryExtension
source: https://developer.apple.com/documentation/devicediscoveryextension
timestamp: 2026-02-13T18:56:16.811Z
---

## Essentials

- [Discovering a third-party media-streaming device](/documentation/devicediscoveryextension/discovering-a-third-party-media-streaming-device)
- [Media Device Discovery Extension](/documentation/bundleresources/entitlements/com.apple.developer.media-device-discovery-extension)

## Extension

- [DDDiscoveryExtension](/documentation/devicediscoveryextension/dddiscoveryextension)

### Controlling discovery

- [func startDiscovery(session: DDDiscoverySession)](/documentation/devicediscoveryextension/dddiscoveryextension/startdiscovery(session:))
- [func stopDiscovery(session: DDDiscoverySession)](/documentation/devicediscoveryextension/dddiscoveryextension/stopdiscovery(session:))

### Observing state changes

- [func didReceiveEvent(DDDeviceEvent)](/documentation/devicediscoveryextension/dddiscoveryextension/didreceiveevent(_:))
- [DDDiscoverySession](/documentation/devicediscoveryextension/dddiscoverysession)

### Providing an event to the system

- [func report(DDDeviceEvent)](/documentation/devicediscoveryextension/dddiscoverysession/report(_:))
- [DDDiscoveryExtensionConfiguration](/documentation/devicediscoveryextension/dddiscoveryextensionconfiguration)

### Creating an extension configuration

- [init(discoveryExtension: T)](/documentation/devicediscoveryextension/dddiscoveryextensionconfiguration/init(discoveryextension:))
- [DDDiscoveryExtensionConfigurationProtocol](/documentation/devicediscoveryextension/dddiscoveryextensionconfigurationprotocol)

## Life cycle

- [DDDeviceEvent](/documentation/devicediscoveryextension/dddeviceevent)

### Creating a device event

- [init(eventType: DDDeviceEvent.EventType, device: DDDevice)](/documentation/devicediscoveryextension/dddeviceevent/init(eventtype:device:))

### Configuring a device event

- [var eventType: DDDeviceEvent.EventType](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.property)
- [DDDeviceEvent.EventType](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum)

#### Distinguishing event types

- [case unknown](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/unknown)
- [case deviceFound](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicefound)
- [case deviceLost](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicelost)
- [case deviceChanged](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicechanged)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/init(rawvalue:))
- [var device: DDDevice](/documentation/devicediscoveryextension/dddeviceevent/device)
- [DDDeviceEvent.EventType](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum)

### Distinguishing event types

- [case unknown](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/unknown)
- [case deviceFound](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicefound)
- [case deviceLost](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicelost)
- [case deviceChanged](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/devicechanged)

### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddeviceevent/eventtype-swift.enum/init(rawvalue:))
- [func DDEventTypeToString(DDDeviceEvent.EventType) -> String](/documentation/devicediscoveryextension/ddeventtypetostring(_:))
- [DDEventHandler](/documentation/devicediscoveryextension/ddeventhandler)

## Device information

- [DDDevice](/documentation/devicediscoveryextension/dddevice)

### Initializing a device

- [init(displayName: String, category: DDDevice.Category, protocolType: UTType, identifier: String)](/documentation/devicediscoveryextension/dddevice/init(displayname:category:protocoltype:identifier:))

### Identifying the device

- [var displayName: String](/documentation/devicediscoveryextension/dddevice/displayname)
- [var identifier: String](/documentation/devicediscoveryextension/dddevice/identifier)
- [var category: DDDevice.Category](/documentation/devicediscoveryextension/dddevice/category-swift.property)
- [DDDevice.Category](/documentation/devicediscoveryextension/dddevice/category-swift.enum)

#### Choosing an icon for the device picker

- [case desktopComputer](/documentation/devicediscoveryextension/dddevice/category-swift.enum/desktopcomputer)
- [case hifiSpeaker](/documentation/devicediscoveryextension/dddevice/category-swift.enum/hifispeaker)
- [case hifiSpeakerMultiple](/documentation/devicediscoveryextension/dddevice/category-swift.enum/hifispeakermultiple)
- [case laptopComputer](/documentation/devicediscoveryextension/dddevice/category-swift.enum/laptopcomputer)
- [case tv](/documentation/devicediscoveryextension/dddevice/category-swift.enum/tv)
- [case tvWithMediaBox](/documentation/devicediscoveryextension/dddevice/category-swift.enum/tvwithmediabox)

#### Enumeration Cases

- [case accessorySetup](/documentation/devicediscoveryextension/dddevice/category-swift.enum/accessorysetup)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/category-swift.enum/init(rawvalue:))

### Indicating the protocol

- [var `protocol`: DDDevice.Protocol](/documentation/devicediscoveryextension/dddevice/protocol-swift.property)
- [DDDevice.Protocol](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum)

#### Indicating a device protocol

- [case dial](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/dial)
- [case invalid](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/invalid)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/init(rawvalue:))
- [var protocolType: UTType](/documentation/devicediscoveryextension/dddevice/protocoltype)
- [var bluetoothIdentifier: UUID?](/documentation/devicediscoveryextension/dddevice/bluetoothidentifier)
- [var networkEndpoint: NWEndpoint?](/documentation/devicediscoveryextension/dddevice/networkendpoint-3lah1)

### Setting the device state

- [var state: DDDeviceState](/documentation/devicediscoveryextension/dddevice/state)
- [var txtRecord: NWTXTRecord?](/documentation/devicediscoveryextension/dddevice/txtrecord)
- [var url: URL](/documentation/devicediscoveryextension/dddevice/url)
- [var supportsGrouping: Bool](/documentation/devicediscoveryextension/dddevice/supportsgrouping)

### Communicating device content and playback status

- [var mediaContentTitle: String?](/documentation/devicediscoveryextension/dddevice/mediacontenttitle)
- [var mediaContentSubtitle: String?](/documentation/devicediscoveryextension/dddevice/mediacontentsubtitle)
- [var mediaPlaybackState: DDDevice.MediaPlaybackState](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.property)
- [DDDevice.MediaPlaybackState](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.enum)

#### Distinguishing media playback states

- [case noContent](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.enum/nocontent)
- [case paused](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.enum/paused)
- [case playing](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.enum/playing)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/mediaplaybackstate-swift.enum/init(rawvalue:))

### Instance Properties

- [var deviceSupports: DDDeviceSupports](/documentation/devicediscoveryextension/dddevice/devicesupports)
- [var displayImageName: String?](/documentation/devicediscoveryextension/dddevice/displayimagename)
- [var ssid: String?](/documentation/devicediscoveryextension/dddevice/ssid)
- [var wifiAwareModelName: String?](/documentation/devicediscoveryextension/dddevice/wifiawaremodelname)
- [var wifiAwareServiceName: String?](/documentation/devicediscoveryextension/dddevice/wifiawareservicename)
- [var wifiAwareServiceRole: DDDevice.WiFiAwareServiceRole](/documentation/devicediscoveryextension/dddevice/wifiawareservicerole-swift.property)
- [var wifiAwareVendorName: String?](/documentation/devicediscoveryextension/dddevice/wifiawarevendorname)

### Enumerations

- [DDDevice.WiFiAwareServiceRole](/documentation/devicediscoveryextension/dddevice/wifiawareservicerole-swift.enum)

#### Enumeration Cases

- [case publisher](/documentation/devicediscoveryextension/dddevice/wifiawareservicerole-swift.enum/publisher)
- [case subscriber](/documentation/devicediscoveryextension/dddevice/wifiawareservicerole-swift.enum/subscriber)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/wifiawareservicerole-swift.enum/init(rawvalue:))
- [DDDevice.Category](/documentation/devicediscoveryextension/dddevice/category-swift.enum)

### Choosing an icon for the device picker

- [case desktopComputer](/documentation/devicediscoveryextension/dddevice/category-swift.enum/desktopcomputer)
- [case hifiSpeaker](/documentation/devicediscoveryextension/dddevice/category-swift.enum/hifispeaker)
- [case hifiSpeakerMultiple](/documentation/devicediscoveryextension/dddevice/category-swift.enum/hifispeakermultiple)
- [case laptopComputer](/documentation/devicediscoveryextension/dddevice/category-swift.enum/laptopcomputer)
- [case tv](/documentation/devicediscoveryextension/dddevice/category-swift.enum/tv)
- [case tvWithMediaBox](/documentation/devicediscoveryextension/dddevice/category-swift.enum/tvwithmediabox)

### Enumeration Cases

- [case accessorySetup](/documentation/devicediscoveryextension/dddevice/category-swift.enum/accessorysetup)

### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/category-swift.enum/init(rawvalue:))
- [DDDeviceState](/documentation/devicediscoveryextension/dddevicestate)

### Communicating a device’s status

- [case invalid](/documentation/devicediscoveryextension/dddevicestate/invalid)
- [case activating](/documentation/devicediscoveryextension/dddevicestate/activating)
- [case activated](/documentation/devicediscoveryextension/dddevicestate/activated)
- [case authorized](/documentation/devicediscoveryextension/dddevicestate/authorized)
- [case invalidating](/documentation/devicediscoveryextension/dddevicestate/invalidating)

### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevicestate/init(rawvalue:))
- [func DDDeviceCategoryToString(DDDevice.Category) -> String](/documentation/devicediscoveryextension/dddevicecategorytostring(_:))
- [func DDDeviceStateToString(DDDeviceState) -> String](/documentation/devicediscoveryextension/dddevicestatetostring(_:))
- [DDDevice.Protocol](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum)

### Indicating a device protocol

- [case dial](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/dial)
- [case invalid](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/invalid)

### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dddevice/protocol-swift.enum/init(rawvalue:))
- [func DDDeviceProtocolToString(DDDevice.Protocol) -> String](/documentation/devicediscoveryextension/dddeviceprotocoltostring(_:))
- [DDDeviceProtocolString](/documentation/devicediscoveryextension/dddeviceprotocolstring)

### Creating a device protocol string

- [init(rawValue: String)](/documentation/devicediscoveryextension/dddeviceprotocolstring/init(rawvalue:))

### Specifying a device protocol string

- [static let dial: DDDeviceProtocolString](/documentation/devicediscoveryextension/dddeviceprotocolstring/dial)
- [static let invalid: DDDeviceProtocolString](/documentation/devicediscoveryextension/dddeviceprotocolstring/invalid)
- [func DDDeviceMediaPlaybackStateToString(DDDevice.MediaPlaybackState) -> String](/documentation/devicediscoveryextension/dddevicemediaplaybackstatetostring(_:))

## Errors

- [DDError](/documentation/devicediscoveryextension/dderror)

### Identifying an error cause

- [DDError.Code](/documentation/devicediscoveryextension/dderror/code)

#### Errors

- [case success](/documentation/devicediscoveryextension/dderror/code/success)
- [case unknown](/documentation/devicediscoveryextension/dderror/code/unknown)
- [case badParameter](/documentation/devicediscoveryextension/dderror/code/badparameter)
- [case unsupported](/documentation/devicediscoveryextension/dderror/code/unsupported)
- [case timeout](/documentation/devicediscoveryextension/dderror/code/timeout)
- [case `internal`](/documentation/devicediscoveryextension/dderror/code/internal)
- [case missingEntitlement](/documentation/devicediscoveryextension/dderror/code/missingentitlement)
- [case permission](/documentation/devicediscoveryextension/dderror/code/permission)
- [case next](/documentation/devicediscoveryextension/dderror/code/next)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dderror/code/init(rawvalue:))
- [static var success: DDError.Code](/documentation/devicediscoveryextension/dderror/success)
- [static var unknown: DDError.Code](/documentation/devicediscoveryextension/dderror/unknown)
- [static var badParameter: DDError.Code](/documentation/devicediscoveryextension/dderror/badparameter)
- [static var unsupported: DDError.Code](/documentation/devicediscoveryextension/dderror/unsupported)
- [static var timeout: DDError.Code](/documentation/devicediscoveryextension/dderror/timeout)
- [static var `internal`: DDError.Code](/documentation/devicediscoveryextension/dderror/internal)
- [static var missingEntitlement: DDError.Code](/documentation/devicediscoveryextension/dderror/missingentitlement)
- [static var permission: DDError.Code](/documentation/devicediscoveryextension/dderror/permission)
- [static var next: DDError.Code](/documentation/devicediscoveryextension/dderror/next)

### Type Properties

- [static var errorDomain: String](/documentation/devicediscoveryextension/dderror/errordomain)
- [DDError.Code](/documentation/devicediscoveryextension/dderror/code)

### Errors

- [case success](/documentation/devicediscoveryextension/dderror/code/success)
- [case unknown](/documentation/devicediscoveryextension/dderror/code/unknown)
- [case badParameter](/documentation/devicediscoveryextension/dderror/code/badparameter)
- [case unsupported](/documentation/devicediscoveryextension/dderror/code/unsupported)
- [case timeout](/documentation/devicediscoveryextension/dderror/code/timeout)
- [case `internal`](/documentation/devicediscoveryextension/dderror/code/internal)
- [case missingEntitlement](/documentation/devicediscoveryextension/dderror/code/missingentitlement)
- [case permission](/documentation/devicediscoveryextension/dderror/code/permission)
- [case next](/documentation/devicediscoveryextension/dderror/code/next)

### Initializers

- [init?(rawValue: Int)](/documentation/devicediscoveryextension/dderror/code/init(rawvalue:))
- [DDErrorHandler](/documentation/devicediscoveryextension/dderrorhandler)
- [DDErrorOutType](/documentation/devicediscoveryextension/dderrorouttype)
- [let DDErrorDomain: String](/documentation/devicediscoveryextension/dderrordomain)

## Reference

- [DeviceDiscoveryExtension Enumerations](/documentation/devicediscoveryextension/devicediscoveryextension-enumerations)

### Enumerations

- [DDDeviceSupports](/documentation/devicediscoveryextension/dddevicesupports)

#### Initializers

- [init(rawValue: UInt)](/documentation/devicediscoveryextension/dddevicesupports/init(rawvalue:))

#### Type Properties

- [static var bluetoothHID: DDDeviceSupports](/documentation/devicediscoveryextension/dddevicesupports/bluetoothhid)
- [static var bluetoothPairingLE: DDDeviceSupports](/documentation/devicediscoveryextension/dddevicesupports/bluetoothpairingle)
- [static var bluetoothTransportBridging: DDDeviceSupports](/documentation/devicediscoveryextension/dddevicesupports/bluetoothtransportbridging)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
