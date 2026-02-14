# AccessorySetupKit Documentation

Source: https://sosumi.ai/documentation/accessorysetupkit

---
title: AccessorySetupKit
source: https://developer.apple.com/documentation/accessorysetupkit
timestamp: 2026-02-13T19:06:27.680Z
---

## Essentials

- [Setting up and authorizing a Bluetooth accessory](/documentation/accessorysetupkit/setting-up-and-authorizing-a-bluetooth-accessory)
- [Discovering and configuring accessories](/documentation/accessorysetupkit/discovering-and-configuring-accessories)
- [ASAccessorySession](/documentation/accessorysetupkit/asaccessorysession)

### Managing the session life cycle

- [func activate(on: dispatch_queue_t, eventHandler: (ASAccessoryEvent) -> Void)](/documentation/accessorysetupkit/asaccessorysession/activate(on:eventhandler:))
- [func invalidate()](/documentation/accessorysetupkit/asaccessorysession/invalidate())

### Displaying an accessory picker

- [func showPicker(completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/showpicker(completionhandler:))
- [func showPicker(for: [ASPickerDisplayItem], completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/showpicker(for:completionhandler:))

### Customizing picker behavior

- [var pickerDisplaySettings: ASPickerDisplaySettings?](/documentation/accessorysetupkit/asaccessorysession/pickerdisplaysettings)
- [ASPickerDisplaySettings](/documentation/accessorysetupkit/aspickerdisplaysettings)

#### Accessing the default instance

- [class var `default`: ASPickerDisplaySettings](/documentation/accessorysetupkit/aspickerdisplaysettings/default)

#### Customizing the discovery timeout

- [var discoveryTimeout: ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.property)
- [ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct)

##### Determining discovery timeout

- [class var `default`: ASPickerDisplaySettings](/documentation/accessorysetupkit/aspickerdisplaysettings/default)
- [static let short: ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct/short)
- [static let medium: ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct/medium)
- [static let long: ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct/long)
- [static let unbounded: ASPickerDisplaySettings.DiscoveryTimeout](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct/unbounded)

##### Working with raw values

- [init(rawValue: TimeInterval)](/documentation/accessorysetupkit/aspickerdisplaysettings/discoverytimeout-swift.struct/init(rawvalue:))

#### Customizing picker options

- [var options: ASPickerDisplaySettings.Options](/documentation/accessorysetupkit/aspickerdisplaysettings/options-swift.property)
- [ASPickerDisplaySettings.Options](/documentation/accessorysetupkit/aspickerdisplaysettings/options-swift.struct)

##### Working with filter options

- [static var filterDiscoveryResults: ASPickerDisplaySettings.Options](/documentation/accessorysetupkit/aspickerdisplaysettings/options-swift.struct/filterdiscoveryresults)

##### Initializers

- [init(rawValue: UInt)](/documentation/accessorysetupkit/aspickerdisplaysettings/options-swift.struct/init(rawvalue:))

### Updating the picker

- [func updatePicker(showing: [ASDiscoveredDisplayItem], completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/updatepicker(showing:completionhandler:))

### Ending filtered discovery

- [func finishPickerDiscovery(completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/finishpickerdiscovery(completionhandler:))

### Accessing discovered accessories

- [var accessories: [ASAccessory]](/documentation/accessorysetupkit/asaccessorysession/accessories)

### Managing accessories

- [func renameAccessory(ASAccessory, options: ASAccessory.RenameOptions, completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/renameaccessory(_:options:completionhandler:))
- [ASAccessory.RenameOptions](/documentation/accessorysetupkit/asaccessory/renameoptions)

#### Creating an options instance

- [init(rawValue: UInt)](/documentation/accessorysetupkit/asaccessory/renameoptions/init(rawvalue:))

#### Options

- [static var ssid: ASAccessory.RenameOptions](/documentation/accessorysetupkit/asaccessory/renameoptions/ssid)
- [func removeAccessory(ASAccessory, completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/removeaccessory(_:completionhandler:))

### Managing authorization

- [func finishAuthorization(for: ASAccessory, settings: ASAccessorySettings, completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/finishauthorization(for:settings:completionhandler:))
- [ASAccessorySettings](/documentation/accessorysetupkit/asaccessorysettings)

#### Applying default settings

- [class var `default`: ASAccessorySettings](/documentation/accessorysetupkit/asaccessorysettings/default)

#### Inspecting accessory settings

- [var ssid: String?](/documentation/accessorysetupkit/asaccessorysettings/ssid)
- [var bluetoothTransportBridgingIdentifier: Data?](/documentation/accessorysetupkit/asaccessorysettings/bluetoothtransportbridgingidentifier)
- [func failAuthorization(for: ASAccessory, completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/failauthorization(for:completionhandler:))
- [func updateAuthorization(for: ASAccessory, descriptor: ASDiscoveryDescriptor, completionHandler: ((any Error)?) -> Void)](/documentation/accessorysetupkit/asaccessorysession/updateauthorization(for:descriptor:completionhandler:))

## Accessory discovery

- [ASAccessoryEvent](/documentation/accessorysetupkit/asaccessoryevent)

### Inspecting the event

- [var accessory: ASAccessory?](/documentation/accessorysetupkit/asaccessoryevent/accessory)
- [ASAccessory](/documentation/accessorysetupkit/asaccessory)

#### Accessing identifiers

- [var bluetoothIdentifier: UUID?](/documentation/accessorysetupkit/asaccessory/bluetoothidentifier)
- [var bluetoothTransportBridgingIdentifier: Data?](/documentation/accessorysetupkit/asaccessory/bluetoothtransportbridgingidentifier)
- [var ssid: String?](/documentation/accessorysetupkit/asaccessory/ssid)

#### Presenting a display name

- [var displayName: String](/documentation/accessorysetupkit/asaccessory/displayname)

#### Inspecting the accessory’s descriptor

- [var descriptor: ASDiscoveryDescriptor](/documentation/accessorysetupkit/asaccessory/descriptor)

#### Inspecting accessory state

- [var state: ASAccessory.AccessoryState](/documentation/accessorysetupkit/asaccessory/state)
- [ASAccessory.AccessoryState](/documentation/accessorysetupkit/asaccessory/accessorystate)

##### Creating a state instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asaccessory/accessorystate/init(rawvalue:))

##### Accessory states

- [case unauthorized](/documentation/accessorysetupkit/asaccessory/accessorystate/unauthorized)
- [case awaitingAuthorization](/documentation/accessorysetupkit/asaccessory/accessorystate/awaitingauthorization)
- [case authorized](/documentation/accessorysetupkit/asaccessory/accessorystate/authorized)

#### Working with Wi-Fi Aware

- [var wifiAwarePairedDeviceID: ASAccessory.WiFiAwarePairedDeviceID](/documentation/accessorysetupkit/asaccessory/wifiawarepaireddeviceid-swift.property)
- [ASAccessory.WiFiAwarePairedDeviceID](/documentation/accessorysetupkit/asaccessory/wifiawarepaireddeviceid-swift.typealias)
- [var eventType: ASAccessoryEventType](/documentation/accessorysetupkit/asaccessoryevent/eventtype)
- [ASAccessoryEventType](/documentation/accessorysetupkit/asaccessoryeventtype)

#### Creating an event type instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asaccessoryeventtype/init(rawvalue:))

#### Accessory events

- [case accessoryAdded](/documentation/accessorysetupkit/asaccessoryeventtype/accessoryadded)
- [case accessoryChanged](/documentation/accessorysetupkit/asaccessoryeventtype/accessorychanged)
- [case accessoryRemoved](/documentation/accessorysetupkit/asaccessoryeventtype/accessoryremoved)

#### Life cycle events

- [case activated](/documentation/accessorysetupkit/asaccessoryeventtype/activated)
- [case invalidated](/documentation/accessorysetupkit/asaccessoryeventtype/invalidated)

#### Discovery events

- [case accessoryDiscovered](/documentation/accessorysetupkit/asaccessoryeventtype/accessorydiscovered)

#### Picker events

- [case pickerDidPresent](/documentation/accessorysetupkit/asaccessoryeventtype/pickerdidpresent)
- [case pickerDidDismiss](/documentation/accessorysetupkit/asaccessoryeventtype/pickerdiddismiss)
- [case pickerSetupBridging](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetupbridging)
- [case pickerSetupPairing](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetuppairing)
- [case pickerSetupFailed](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetupfailed)
- [case pickerSetupRename](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetuprename)

#### Migration events

- [case migrationComplete](/documentation/accessorysetupkit/asaccessoryeventtype/migrationcomplete)

#### Unclassified events

- [case unknown](/documentation/accessorysetupkit/asaccessoryeventtype/unknown)

### Handling errors

- [var error: (any Error)?](/documentation/accessorysetupkit/asaccessoryevent/error)
- [ASAccessoryEventType](/documentation/accessorysetupkit/asaccessoryeventtype)

### Creating an event type instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asaccessoryeventtype/init(rawvalue:))

### Accessory events

- [case accessoryAdded](/documentation/accessorysetupkit/asaccessoryeventtype/accessoryadded)
- [case accessoryChanged](/documentation/accessorysetupkit/asaccessoryeventtype/accessorychanged)
- [case accessoryRemoved](/documentation/accessorysetupkit/asaccessoryeventtype/accessoryremoved)

### Life cycle events

- [case activated](/documentation/accessorysetupkit/asaccessoryeventtype/activated)
- [case invalidated](/documentation/accessorysetupkit/asaccessoryeventtype/invalidated)

### Discovery events

- [case accessoryDiscovered](/documentation/accessorysetupkit/asaccessoryeventtype/accessorydiscovered)

### Picker events

- [case pickerDidPresent](/documentation/accessorysetupkit/asaccessoryeventtype/pickerdidpresent)
- [case pickerDidDismiss](/documentation/accessorysetupkit/asaccessoryeventtype/pickerdiddismiss)
- [case pickerSetupBridging](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetupbridging)
- [case pickerSetupPairing](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetuppairing)
- [case pickerSetupFailed](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetupfailed)
- [case pickerSetupRename](/documentation/accessorysetupkit/asaccessoryeventtype/pickersetuprename)

### Migration events

- [case migrationComplete](/documentation/accessorysetupkit/asaccessoryeventtype/migrationcomplete)

### Unclassified events

- [case unknown](/documentation/accessorysetupkit/asaccessoryeventtype/unknown)
- [ASDiscoveryDescriptor](/documentation/accessorysetupkit/asdiscoverydescriptor)

### Specifying Bluetooth properties

- [var bluetoothCompanyIdentifier: ASBluetoothCompanyIdentifier](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothcompanyidentifier)
- [ASBluetoothCompanyIdentifier](/documentation/accessorysetupkit/asbluetoothcompanyidentifier)

#### Creating an identifier

- [init(UInt16)](/documentation/accessorysetupkit/asbluetoothcompanyidentifier/init(_:))
- [init(rawValue: UInt16)](/documentation/accessorysetupkit/asbluetoothcompanyidentifier/init(rawvalue:))
- [ASBluetoothCompanyIdentifier](/documentation/accessorysetupkit/asbluetoothcompanyidentifier)

#### Creating an identifier

- [init(UInt16)](/documentation/accessorysetupkit/asbluetoothcompanyidentifier/init(_:))
- [init(rawValue: UInt16)](/documentation/accessorysetupkit/asbluetoothcompanyidentifier/init(rawvalue:))
- [var bluetoothManufacturerDataBlob: Data?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothmanufacturerdatablob)
- [var bluetoothManufacturerDataMask: Data?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothmanufacturerdatamask)
- [var bluetoothServiceDataBlob: Data?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothservicedatablob)
- [var bluetoothServiceDataMask: Data?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothservicedatamask)
- [var bluetoothNameSubstring: String?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothnamesubstring)
- [var bluetoothNameSubstringCompareOptions: NSString.CompareOptions](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothnamesubstringcompareoptions)
- [var bluetoothServiceUUID: CBUUID?](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothserviceuuid)
- [var bluetoothRange: ASDiscoveryDescriptor.Range](/documentation/accessorysetupkit/asdiscoverydescriptor/bluetoothrange)
- [ASDiscoveryDescriptor.Range](/documentation/accessorysetupkit/asdiscoverydescriptor/range)

#### Creating an options instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asdiscoverydescriptor/range/init(rawvalue:))

#### Bluetooth options

- [case `default`](/documentation/accessorysetupkit/asdiscoverydescriptor/range/default)
- [case immediate](/documentation/accessorysetupkit/asdiscoverydescriptor/range/immediate)

### Specifying Wi-Fi properties

- [var ssid: String?](/documentation/accessorysetupkit/asdiscoverydescriptor/ssid)
- [var ssidPrefix: String?](/documentation/accessorysetupkit/asdiscoverydescriptor/ssidprefix)

### Specifying options

- [var supportedOptions: ASAccessory.SupportOptions](/documentation/accessorysetupkit/asdiscoverydescriptor/supportedoptions)
- [ASAccessory.SupportOptions](/documentation/accessorysetupkit/asaccessory/supportoptions)

#### Creating an options instance

- [init(rawValue: UInt)](/documentation/accessorysetupkit/asaccessory/supportoptions/init(rawvalue:))

#### Bluetooth options

- [static var bluetoothPairingLE: ASAccessory.SupportOptions](/documentation/accessorysetupkit/asaccessory/supportoptions/bluetoothpairingle)
- [static var bluetoothTransportBridging: ASAccessory.SupportOptions](/documentation/accessorysetupkit/asaccessory/supportoptions/bluetoothtransportbridging)
- [static var bluetoothHID: ASAccessory.SupportOptions](/documentation/accessorysetupkit/asaccessory/supportoptions/bluetoothhid)

### Specifying Wi-Fi Aware properties

- [var wifiAwareServiceName: String?](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicename)
- [var wifiAwareServiceRole: ASDiscoveryDescriptor.WiFiAwareServiceRole](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicerole-swift.property)
- [ASDiscoveryDescriptor.WiFiAwareServiceRole](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicerole-swift.enum)

#### Determining service role

- [case subscriber](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicerole-swift.enum/subscriber)
- [case publisher](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicerole-swift.enum/publisher)

#### Working with raw values

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawareservicerole-swift.enum/init(rawvalue:))
- [var wifiAwareModelNameMatch: ASPropertyCompareString?](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawaremodelnamematch)
- [var wifiAwareVendorNameMatch: ASPropertyCompareString?](/documentation/accessorysetupkit/asdiscoverydescriptor/wifiawarevendornamematch)
- [ASPropertyCompareString](/documentation/accessorysetupkit/aspropertycomparestring)

#### Creating a compare string instance

- [init(string: String, compareOptions: NSString.CompareOptions)](/documentation/accessorysetupkit/aspropertycomparestring/init(string:compareoptions:))

#### Accessing compare string properties

- [var string: String](/documentation/accessorysetupkit/aspropertycomparestring/string)
- [var compareOptions: NSString.CompareOptions](/documentation/accessorysetupkit/aspropertycomparestring/compareoptions)

## Accessory description

- [ASAccessory](/documentation/accessorysetupkit/asaccessory)

### Accessing identifiers

- [var bluetoothIdentifier: UUID?](/documentation/accessorysetupkit/asaccessory/bluetoothidentifier)
- [var bluetoothTransportBridgingIdentifier: Data?](/documentation/accessorysetupkit/asaccessory/bluetoothtransportbridgingidentifier)
- [var ssid: String?](/documentation/accessorysetupkit/asaccessory/ssid)

### Presenting a display name

- [var displayName: String](/documentation/accessorysetupkit/asaccessory/displayname)

### Inspecting the accessory’s descriptor

- [var descriptor: ASDiscoveryDescriptor](/documentation/accessorysetupkit/asaccessory/descriptor)

### Inspecting accessory state

- [var state: ASAccessory.AccessoryState](/documentation/accessorysetupkit/asaccessory/state)
- [ASAccessory.AccessoryState](/documentation/accessorysetupkit/asaccessory/accessorystate)

#### Creating a state instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asaccessory/accessorystate/init(rawvalue:))

#### Accessory states

- [case unauthorized](/documentation/accessorysetupkit/asaccessory/accessorystate/unauthorized)
- [case awaitingAuthorization](/documentation/accessorysetupkit/asaccessory/accessorystate/awaitingauthorization)
- [case authorized](/documentation/accessorysetupkit/asaccessory/accessorystate/authorized)

### Working with Wi-Fi Aware

- [var wifiAwarePairedDeviceID: ASAccessory.WiFiAwarePairedDeviceID](/documentation/accessorysetupkit/asaccessory/wifiawarepaireddeviceid-swift.property)
- [ASAccessory.WiFiAwarePairedDeviceID](/documentation/accessorysetupkit/asaccessory/wifiawarepaireddeviceid-swift.typealias)
- [ASDiscoveredAccessory](/documentation/accessorysetupkit/asdiscoveredaccessory)

### Working with accessory properties

- [var bluetoothAdvertisementData: [AnyHashable : Any]?](/documentation/accessorysetupkit/asdiscoveredaccessory/bluetoothadvertisementdata)
- [var bluetoothRSSI: Int?](/documentation/accessorysetupkit/asdiscoveredaccessory/bluetoothrssi-5a2gp)
- [ASAccessory.AccessoryState](/documentation/accessorysetupkit/asaccessory/accessorystate)

### Creating a state instance

- [init?(rawValue: Int)](/documentation/accessorysetupkit/asaccessory/accessorystate/init(rawvalue:))

### Accessory states

- [case unauthorized](/documentation/accessorysetupkit/asaccessory/accessorystate/unauthorized)
- [case awaitingAuthorization](/documentation/accessorysetupkit/asaccessory/accessorystate/awaitingauthorization)
- [case authorized](/documentation/accessorysetupkit/asaccessory/accessorystate/authorized)

## Displaying picker items

- [ASPickerDisplayItem](/documentation/accessorysetupkit/aspickerdisplayitem)

### Creating a display item

- [init(name: String, productImage: UIImage, descriptor: ASDiscoveryDescriptor)](/documentation/accessorysetupkit/aspickerdisplayitem/init(name:productimage:descriptor:))

### Specifying discovery properties

- [var descriptor: ASDiscoveryDescriptor](/documentation/accessorysetupkit/aspickerdisplayitem/descriptor)

### Customizing display properties

- [var name: String](/documentation/accessorysetupkit/aspickerdisplayitem/name)
- [var productImage: UIImage](/documentation/accessorysetupkit/aspickerdisplayitem/productimage)

### Customizing setup options

- [var setupOptions: ASPickerDisplayItem.SetupOptions](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.property)
- [ASPickerDisplayItem.SetupOptions](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.struct)

#### Creating an options instance

- [init(rawValue: UInt)](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.struct/init(rawvalue:))

#### Options

- [static var rename: ASPickerDisplayItem.SetupOptions](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.struct/rename)
- [static var confirmAuthorization: ASPickerDisplayItem.SetupOptions](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.struct/confirmauthorization)
- [static var finishInApp: ASPickerDisplayItem.SetupOptions](/documentation/accessorysetupkit/aspickerdisplayitem/setupoptions-swift.struct/finishinapp)
- [var renameOptions: ASAccessory.RenameOptions](/documentation/accessorysetupkit/aspickerdisplayitem/renameoptions)
- [ASAccessory.RenameOptions](/documentation/accessorysetupkit/asaccessory/renameoptions)

#### Creating an options instance

- [init(rawValue: UInt)](/documentation/accessorysetupkit/asaccessory/renameoptions/init(rawvalue:))

#### Options

- [static var ssid: ASAccessory.RenameOptions](/documentation/accessorysetupkit/asaccessory/renameoptions/ssid)
- [ASDiscoveredDisplayItem](/documentation/accessorysetupkit/asdiscovereddisplayitem)

### Creating an updated display item

- [init(name: String, productImage: UIImage, accessory: ASDiscoveredAccessory)](/documentation/accessorysetupkit/asdiscovereddisplayitem/init(name:productimage:accessory:))
- [ASMigrationDisplayItem](/documentation/accessorysetupkit/asmigrationdisplayitem)

### Accessory identifiers

- [var peripheralIdentifier: UUID?](/documentation/accessorysetupkit/asmigrationdisplayitem/peripheralidentifier)
- [var hotspotSSID: String?](/documentation/accessorysetupkit/asmigrationdisplayitem/hotspotssid)
- [var wifiAwarePairedDeviceID: ASAccessory.WiFiAwarePairedDeviceID](/documentation/accessorysetupkit/asmigrationdisplayitem/wifiawarepaireddeviceid)

## Information property list keys

- [NSAccessorySetupSupports](/documentation/bundleresources/information-property-list/nsaccessorysetupsupports)
- [NSAccessorySetupBluetoothCompanyIdentifiers](/documentation/bundleresources/information-property-list/nsaccessorysetupbluetoothcompanyidentifiers)
- [NSAccessorySetupBluetoothNames](/documentation/bundleresources/information-property-list/nsaccessorysetupbluetoothnames)
- [NSAccessorySetupBluetoothServices](/documentation/bundleresources/information-property-list/nsaccessorysetupbluetoothservices)

## Errors

- [ASError](/documentation/accessorysetupkit/aserror)

### Activation errors

- [static var activationFailed: ASError.Code](/documentation/accessorysetupkit/aserror/activationfailed)

### Life cycle errors

- [static var invalidated: ASError.Code](/documentation/accessorysetupkit/aserror/invalidated)

### Configuration errors

- [static var extensionNotFound: ASError.Code](/documentation/accessorysetupkit/aserror/extensionnotfound)
- [static var invalidRequest: ASError.Code](/documentation/accessorysetupkit/aserror/invalidrequest)

### Picker errors

- [static var pickerRestricted: ASError.Code](/documentation/accessorysetupkit/aserror/pickerrestricted)
- [static var pickerAlreadyActive: ASError.Code](/documentation/accessorysetupkit/aserror/pickeralreadyactive)

### Cancellation and permission errors

- [static var userCancelled: ASError.Code](/documentation/accessorysetupkit/aserror/usercancelled)
- [static var userRestricted: ASError.Code](/documentation/accessorysetupkit/aserror/userrestricted)

### Communication errors

- [static var connectionFailed: ASError.Code](/documentation/accessorysetupkit/aserror/connectionfailed)
- [static var discoveryTimeout: ASError.Code](/documentation/accessorysetupkit/aserror/discoverytimeout)

### Success cases

- [static var success: ASError.Code](/documentation/accessorysetupkit/aserror/success)

### Unclassified errors

- [static var unknown: ASError.Code](/documentation/accessorysetupkit/aserror/unknown)

### Accessing the error domain

- [static var errorDomain: String](/documentation/accessorysetupkit/aserror/errordomain)
- [let ASErrorDomain: String](/documentation/accessorysetupkit/aserrordomain)
- [let ASErrorDomain: String](/documentation/accessorysetupkit/aserrordomain)
- [ASError.Code](/documentation/accessorysetupkit/aserror/code)

### Activation errors

- [case activationFailed](/documentation/accessorysetupkit/aserror/code/activationfailed)

### Timeout and life cycle errors

- [case discoveryTimeout](/documentation/accessorysetupkit/aserror/code/discoverytimeout)
- [case invalidated](/documentation/accessorysetupkit/aserror/code/invalidated)

### Configuration errors

- [case extensionNotFound](/documentation/accessorysetupkit/aserror/code/extensionnotfound)
- [case userRestricted](/documentation/accessorysetupkit/aserror/code/userrestricted)
- [case invalidRequest](/documentation/accessorysetupkit/aserror/code/invalidrequest)

### Picker errors

- [case pickerRestricted](/documentation/accessorysetupkit/aserror/code/pickerrestricted)
- [case pickerAlreadyActive](/documentation/accessorysetupkit/aserror/code/pickeralreadyactive)

### Cancellation errors

- [case userCancelled](/documentation/accessorysetupkit/aserror/code/usercancelled)

### Communication errors

- [case connectionFailed](/documentation/accessorysetupkit/aserror/code/connectionfailed)

### Success cases

- [case success](/documentation/accessorysetupkit/aserror/code/success)

### Unclassified errors

- [case unknown](/documentation/accessorysetupkit/aserror/code/unknown)

### Accessing the error domain

- [static var errorDomain: String](/documentation/accessorysetupkit/aserror/errordomain)
- [let ASErrorDomain: String](/documentation/accessorysetupkit/aserrordomain)

### Working with raw values

- [init?(rawValue: Int)](/documentation/accessorysetupkit/aserror/code/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
