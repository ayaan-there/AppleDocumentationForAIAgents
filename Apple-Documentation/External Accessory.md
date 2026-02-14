# External Accessory Documentation

Source: https://sosumi.ai/documentation/externalaccessory

---
title: External Accessory
source: https://developer.apple.com/documentation/externalaccessory
timestamp: 2026-02-13T18:56:52.001Z
---

## Essentials

- [UISupportedExternalAccessoryProtocols](/documentation/bundleresources/information-property-list/uisupportedexternalaccessoryprotocols)
- [EAAccessoryManager](/documentation/externalaccessory/eaaccessorymanager)

### Getting the Shared Accessory Manager

- [class func shared() -> EAAccessoryManager](/documentation/externalaccessory/eaaccessorymanager/shared())

### Managing Connection Status Changes

- [func registerForLocalNotifications()](/documentation/externalaccessory/eaaccessorymanager/registerforlocalnotifications())
- [func unregisterForLocalNotifications()](/documentation/externalaccessory/eaaccessorymanager/unregisterforlocalnotifications())
- [static let EAAccessoryDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/eaaccessorydidconnect)
- [static let EAAccessoryDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/eaaccessorydiddisconnect)
- [let EAAccessoryKey: String](/documentation/externalaccessory/eaaccessorykey)
- [let EAAccessorySelectedKey: String](/documentation/externalaccessory/eaaccessoryselectedkey)

### Presenting the Bluetooth Picker

- [func showBluetoothAccessoryPicker(withNameFilter: NSPredicate?, completion: (((any Error)?) -> Void)?)](/documentation/externalaccessory/eaaccessorymanager/showbluetoothaccessorypicker(withnamefilter:completion:))
- [EABluetoothAccessoryPickerCompletion](/documentation/externalaccessory/eabluetoothaccessorypickercompletion)
- [EABluetoothAccessoryPickerError](/documentation/externalaccessory/eabluetoothaccessorypickererror)

#### Error Codes

- [static var alreadyConnected: EABluetoothAccessoryPickerError.Code](/documentation/externalaccessory/eabluetoothaccessorypickererror/alreadyconnected)
- [static var resultCancelled: EABluetoothAccessoryPickerError.Code](/documentation/externalaccessory/eabluetoothaccessorypickererror/resultcancelled)
- [static var resultFailed: EABluetoothAccessoryPickerError.Code](/documentation/externalaccessory/eabluetoothaccessorypickererror/resultfailed)
- [static var resultNotFound: EABluetoothAccessoryPickerError.Code](/documentation/externalaccessory/eabluetoothaccessorypickererror/resultnotfound)

#### Type Properties

- [static var errorDomain: String](/documentation/externalaccessory/eabluetoothaccessorypickererror/errordomain)
- [EABluetoothAccessoryPickerError.Code](/documentation/externalaccessory/eabluetoothaccessorypickererror/code)

#### Error Codes

- [case alreadyConnected](/documentation/externalaccessory/eabluetoothaccessorypickererror/code/alreadyconnected)
- [case resultNotFound](/documentation/externalaccessory/eabluetoothaccessorypickererror/code/resultnotfound)
- [case resultCancelled](/documentation/externalaccessory/eabluetoothaccessorypickererror/code/resultcancelled)
- [case resultFailed](/documentation/externalaccessory/eabluetoothaccessorypickererror/code/resultfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/externalaccessory/eabluetoothaccessorypickererror/code/init(rawvalue:))
- [let EABluetoothAccessoryPickerErrorDomain: String](/documentation/externalaccessory/eabluetoothaccessorypickererrordomain)

### Getting the Available Accessories

- [var connectedAccessories: [EAAccessory]](/documentation/externalaccessory/eaaccessorymanager/connectedaccessories)

## Accessory Communication

- [EAAccessory](/documentation/externalaccessory/eaaccessory)

### Responding to Disconnection Events

- [var delegate: (any EAAccessoryDelegate)?](/documentation/externalaccessory/eaaccessory/delegate)
- [EAAccessoryDelegate](/documentation/externalaccessory/eaaccessorydelegate)

#### Responding to Disconnection Events

- [func accessoryDidDisconnect(EAAccessory)](/documentation/externalaccessory/eaaccessorydelegate/accessorydiddisconnect(_:))

### Getting Connection Information

- [var isConnected: Bool](/documentation/externalaccessory/eaaccessory/isconnected)
- [var connectionID: Int](/documentation/externalaccessory/eaaccessory/connectionid)
- [Null Connection ID](/documentation/externalaccessory/null-connection-id)

#### Constants

- [var EAConnectionIDNone: Int](/documentation/externalaccessory/eaconnectionidnone)

### Getting the Manufacturer-Supplied Attributes

- [var name: String](/documentation/externalaccessory/eaaccessory/name)
- [var manufacturer: String](/documentation/externalaccessory/eaaccessory/manufacturer)
- [var modelNumber: String](/documentation/externalaccessory/eaaccessory/modelnumber)
- [var serialNumber: String](/documentation/externalaccessory/eaaccessory/serialnumber)
- [var firmwareRevision: String](/documentation/externalaccessory/eaaccessory/firmwarerevision)
- [var hardwareRevision: String](/documentation/externalaccessory/eaaccessory/hardwarerevision)
- [var protocolStrings: [String]](/documentation/externalaccessory/eaaccessory/protocolstrings)
- [var dockType: String](/documentation/externalaccessory/eaaccessory/docktype)
- [EASession](/documentation/externalaccessory/easession)

### Creating the Session Object

- [init?(accessory: EAAccessory, forProtocol: String)](/documentation/externalaccessory/easession/init(accessory:forprotocol:))

### Getting Session Information

- [var accessory: EAAccessory?](/documentation/externalaccessory/easession/accessory)
- [var protocolString: String?](/documentation/externalaccessory/easession/protocolstring)

### Getting the Communication Streams

- [var inputStream: InputStream?](/documentation/externalaccessory/easession/inputstream)
- [var outputStream: OutputStream?](/documentation/externalaccessory/easession/outputstream)

## Wi-Fi Accessory Configuration

- [Wireless Accessory Configuration Entitlement](/documentation/bundleresources/entitlements/com.apple.external-accessory.wireless-configuration)
- [EAWiFiUnconfiguredAccessoryBrowser](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser)

### Creating the Browser Object

- [init(delegate: (any EAWiFiUnconfiguredAccessoryBrowserDelegate)?, queue: dispatch_queue_t?)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/init(delegate:queue:))

### Managing Browser Interactions

- [var delegate: (any EAWiFiUnconfiguredAccessoryBrowserDelegate)?](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/delegate)
- [EAWiFiUnconfiguredAccessoryBrowserDelegate](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserdelegate)

#### Getting Updates About Browser State

- [func accessoryBrowser(EAWiFiUnconfiguredAccessoryBrowser, didUpdate: EAWiFiUnconfiguredAccessoryBrowserState)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserdelegate/accessorybrowser(_:didupdate:))
- [EAWiFiUnconfiguredAccessoryBrowserState](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate)

##### States

- [case wiFiUnavailable](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate/wifiunavailable)
- [case stopped](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate/stopped)
- [case searching](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate/searching)
- [case configuring](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate/configuring)

##### Initializers

- [init?(rawValue: Int)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserstate/init(rawvalue:))

#### Getting Updates About the Configuration Process

- [func accessoryBrowser(EAWiFiUnconfiguredAccessoryBrowser, didFinishConfiguringAccessory: EAWiFiUnconfiguredAccessory, with: EAWiFiUnconfiguredAccessoryConfigurationStatus)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserdelegate/accessorybrowser(_:didfinishconfiguringaccessory:with:))
- [EAWiFiUnconfiguredAccessoryConfigurationStatus](/documentation/externalaccessory/eawifiunconfiguredaccessoryconfigurationstatus)

##### Status Values

- [case success](/documentation/externalaccessory/eawifiunconfiguredaccessoryconfigurationstatus/success)
- [case userCancelledConfiguration](/documentation/externalaccessory/eawifiunconfiguredaccessoryconfigurationstatus/usercancelledconfiguration)
- [case failed](/documentation/externalaccessory/eawifiunconfiguredaccessoryconfigurationstatus/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/externalaccessory/eawifiunconfiguredaccessoryconfigurationstatus/init(rawvalue:))

#### Getting Updates About the Search Process

- [func accessoryBrowser(EAWiFiUnconfiguredAccessoryBrowser, didFindUnconfiguredAccessories: Set<EAWiFiUnconfiguredAccessory>)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserdelegate/accessorybrowser(_:didfindunconfiguredaccessories:))
- [func accessoryBrowser(EAWiFiUnconfiguredAccessoryBrowser, didRemoveUnconfiguredAccessories: Set<EAWiFiUnconfiguredAccessory>)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowserdelegate/accessorybrowser(_:didremoveunconfiguredaccessories:))

### Finding and Configuring Accessories

- [func configureAccessory(EAWiFiUnconfiguredAccessory, withConfigurationUIOn: UIViewController)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/configureaccessory(_:withconfigurationuion:))
- [func startSearchingForUnconfiguredAccessories(matching: NSPredicate?)](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/startsearchingforunconfiguredaccessories(matching:))
- [func stopSearchingForUnconfiguredAccessories()](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/stopsearchingforunconfiguredaccessories())
- [var unconfiguredAccessories: Set<EAWiFiUnconfiguredAccessory>](/documentation/externalaccessory/eawifiunconfiguredaccessorybrowser/unconfiguredaccessories)
- [EAWiFiUnconfiguredAccessory](/documentation/externalaccessory/eawifiunconfiguredaccessory)

### Getting Information About the Accessory

- [var name: String](/documentation/externalaccessory/eawifiunconfiguredaccessory/name)
- [var manufacturer: String](/documentation/externalaccessory/eawifiunconfiguredaccessory/manufacturer)
- [var model: String](/documentation/externalaccessory/eawifiunconfiguredaccessory/model)
- [var ssid: String](/documentation/externalaccessory/eawifiunconfiguredaccessory/ssid)
- [var macAddress: String](/documentation/externalaccessory/eawifiunconfiguredaccessory/macaddress)
- [var properties: EAWiFiUnconfiguredAccessoryProperties](/documentation/externalaccessory/eawifiunconfiguredaccessory/properties)
- [EAWiFiUnconfiguredAccessoryProperties](/documentation/externalaccessory/eawifiunconfiguredaccessoryproperties)

#### Getting the Accessory Properties

- [static var propertySupportsAirPlay: EAWiFiUnconfiguredAccessoryProperties](/documentation/externalaccessory/eawifiunconfiguredaccessoryproperties/propertysupportsairplay)
- [static var propertySupportsAirPrint: EAWiFiUnconfiguredAccessoryProperties](/documentation/externalaccessory/eawifiunconfiguredaccessoryproperties/propertysupportsairprint)
- [static var propertySupportsHomeKit: EAWiFiUnconfiguredAccessoryProperties](/documentation/externalaccessory/eawifiunconfiguredaccessoryproperties/propertysupportshomekit)

#### Initializers

- [init(rawValue: UInt)](/documentation/externalaccessory/eawifiunconfiguredaccessoryproperties/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
