# DeviceDiscoveryUI Documentation

Source: https://sosumi.ai/documentation/devicediscoveryui

---
title: DeviceDiscoveryUI
source: https://developer.apple.com/documentation/devicediscoveryui
timestamp: 2026-02-13T18:56:18.737Z
---

## Selecting nearby devices

- [Connecting a tvOS app to other devices over the local network](/documentation/devicediscoveryui/connecting-a-tvos-app-to-other-devices-over-the-local-network)
- [DevicePicker](/documentation/devicediscoveryui/devicepicker)

### Creating a device picker

- [init(NWBrowser.Descriptor, onSelect: (NWEndpoint) -> Void, label: () -> Label, fallback: () -> Fallback, parameters: (() -> NWParameters)?)](/documentation/devicediscoveryui/devicepicker/init(_:onselect:label:fallback:parameters:))

### Initializers

- [init<Provider>(Provider, access: DDDevicePairingAccess, onSelect: (Provider.Endpoint) -> Void, label: () -> Label, fallback: () -> Fallback, parameters: (() -> NWParameters)?)](/documentation/devicediscoveryui/devicepicker/init(_:access:onselect:label:fallback:parameters:))
- [DDDevicePickerViewController](/documentation/devicediscoveryui/dddevicepickerviewcontroller)

### Creating device picker view controllers

- [static func isSupported(NWBrowser.Descriptor, using: NWParameters?) -> Bool](/documentation/devicediscoveryui/dddevicepickerviewcontroller/issupported(_:using:))
- [convenience init?(browseDescriptor: NWBrowser.Descriptor, parameters: NWParameters?)](/documentation/devicediscoveryui/dddevicepickerviewcontroller/init(browsedescriptor:parameters:))

### Accessing the selected endpoint

- [var endpoint: NWEndpoint](/documentation/devicediscoveryui/dddevicepickerviewcontroller/endpoint)

### Initializers

- [convenience init?(browseDescriptor: NWBrowser.Descriptor, parameters: NWParameters?, access: DDDevicePairingAccess)](/documentation/devicediscoveryui/dddevicepickerviewcontroller/init(browsedescriptor:parameters:access:))
- [DevicePickerSupportedAction](/documentation/devicediscoveryui/devicepickersupportedaction)

### Checking for support

- [func callAsFunction(NWBrowser.Descriptor, parameters: (() -> NWParameters)?) -> Bool](/documentation/devicediscoveryui/devicepickersupportedaction/callasfunction(_:parameters:))
- [NSApplicationServices](/documentation/bundleresources/information-property-list/nsapplicationservices)

## Classes

- [DDDevicePairingViewController](/documentation/devicediscoveryui/dddevicepairingviewcontroller)

### Initializers

- [init(listenerProvider: any ListenerProvider, access: DDDevicePairingAccess)](/documentation/devicediscoveryui/dddevicepairingviewcontroller/init(listenerprovider:access:))

### Instance Methods

- [func viewDidLoad()](/documentation/devicediscoveryui/dddevicepairingviewcontroller/viewdidload())

### Type Methods

- [static func isSupported(any ListenerProvider) -> Bool](/documentation/devicediscoveryui/dddevicepairingviewcontroller/issupported(_:))

## Structures

- [DDDevicePairingAccess](/documentation/devicediscoveryui/dddevicepairingaccess)

### Type Properties

- [static var `default`: DDDevicePairingAccess](/documentation/devicediscoveryui/dddevicepairingaccess/default)
- [static var permanent: DDDevicePairingAccess](/documentation/devicediscoveryui/dddevicepairingaccess/permanent)
- [DevicePairingView](/documentation/devicediscoveryui/devicepairingview)

### Initializers

- [init(any ListenerProvider, access: DDDevicePairingAccess, label: () -> Label, fallback: () -> Fallback)](/documentation/devicediscoveryui/devicepairingview/init(_:access:label:fallback:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
