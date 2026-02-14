# IOBluetooth UI Documentation

Source: https://sosumi.ai/documentation/iobluetoothui

---
title: IOBluetooth UI
source: https://developer.apple.com/documentation/iobluetoothui
timestamp: 2026-02-13T18:58:19.444Z
---

## Classes

- [IOBluetoothAccessibilityIgnoredImageCell](/documentation/iobluetoothui/iobluetoothaccessibilityignoredimagecell)
- [IOBluetoothAccessibilityIgnoredTextFieldCell](/documentation/iobluetoothui/iobluetoothaccessibilityignoredtextfieldcell)
- [IOBluetoothDeviceSelectorController](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller)

### Instance Methods

- [func addAllowedUUID(IOBluetoothSDPUUID!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/addalloweduuid(_:))
- [func addAllowedUUIDArray([Any]!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/addalloweduuidarray(_:))
- [func beginSheetModal(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/beginsheetmodal(for:modaldelegate:didend:contextinfo:))
- [func clearAllowedUUIDs()](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/clearalloweduuids())
- [func getCancel() -> String!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getcancel())
- [func getDescriptionText() -> String!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getdescriptiontext())
- [func getHeader() -> String!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getheader())
- [func getOptions() -> IOBluetoothServiceBrowserControllerOptions](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getoptions())
- [func getPrompt() -> String!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getprompt())
- [func getResults() -> [Any]!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getresults())
- [func getSearchAttributes() -> UnsafePointer<IOBluetoothDeviceSearchAttributes>!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/getsearchattributes())
- [func getTitle() -> String!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/gettitle())
- [func runModal() -> Int32](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/runmodal())
- [func setCancel(String!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setcancel(_:))
- [func setDescriptionText(String!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setdescriptiontext(_:))
- [func setHeader(String!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setheader(_:))
- [func setOptions(IOBluetoothServiceBrowserControllerOptions)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setoptions(_:))
- [func setPrompt(String!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setprompt(_:))
- [func setSearchAttributes(UnsafePointer<IOBluetoothDeviceSearchAttributes>!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/setsearchattributes(_:))
- [func setTitle(String!)](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/settitle(_:))

### Type Methods

- [class func deviceSelector() -> IOBluetoothDeviceSelectorController!](/documentation/iobluetoothui/iobluetoothdeviceselectorcontroller/deviceselector())
- [IOBluetoothDeviceSelectorControllerRef](/documentation/iobluetoothui/iobluetoothdeviceselectorcontrollerref)
- [IOBluetoothObjectPushUIController](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller)

### Initializers

- [init!(objectPushWith: IOBluetoothDevice!, withFiles: [Any]!, delegate: Any!)](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/init(objectpushwith:withfiles:delegate:))

### Instance Methods

- [func beginSheetModal(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/beginsheetmodal(for:modaldelegate:didend:contextinfo:))
- [func getDevice() -> IOBluetoothDevice!](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/getdevice())
- [func getTitle() -> String!](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/gettitle())
- [func isTransferInProgress() -> Bool](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/istransferinprogress())
- [func runModal()](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/runmodal())
- [func runPanel()](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/runpanel())
- [func setIconImage(NSImage!)](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/seticonimage(_:))
- [func setTitle(String!)](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/settitle(_:))
- [func stop()](/documentation/iobluetoothui/iobluetoothobjectpushuicontroller/stop())
- [IOBluetoothPairingController](/documentation/iobluetoothui/iobluetoothpairingcontroller)

### Instance Methods

- [func addAllowedUUID(IOBluetoothSDPUUID!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/addalloweduuid(_:))
- [func addAllowedUUIDArray([Any]!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/addalloweduuidarray(_:))
- [func clearAllowedUUIDs()](/documentation/iobluetoothui/iobluetoothpairingcontroller/clearalloweduuids())
- [func getDescriptionText() -> String!](/documentation/iobluetoothui/iobluetoothpairingcontroller/getdescriptiontext())
- [func getOptions() -> IOBluetoothServiceBrowserControllerOptions](/documentation/iobluetoothui/iobluetoothpairingcontroller/getoptions())
- [func getPrompt() -> String!](/documentation/iobluetoothui/iobluetoothpairingcontroller/getprompt())
- [func getResults() -> [Any]!](/documentation/iobluetoothui/iobluetoothpairingcontroller/getresults())
- [func getSearchAttributes() -> UnsafePointer<IOBluetoothDeviceSearchAttributes>!](/documentation/iobluetoothui/iobluetoothpairingcontroller/getsearchattributes())
- [func getTitle() -> String!](/documentation/iobluetoothui/iobluetoothpairingcontroller/gettitle())
- [func runModal() -> Int32](/documentation/iobluetoothui/iobluetoothpairingcontroller/runmodal())
- [func setDescriptionText(String!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/setdescriptiontext(_:))
- [func setOptions(IOBluetoothServiceBrowserControllerOptions)](/documentation/iobluetoothui/iobluetoothpairingcontroller/setoptions(_:))
- [func setPrompt(String!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/setprompt(_:))
- [func setSearchAttributes(UnsafePointer<IOBluetoothDeviceSearchAttributes>!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/setsearchattributes(_:))
- [func setTitle(String!)](/documentation/iobluetoothui/iobluetoothpairingcontroller/settitle(_:))
- [IOBluetoothPairingControllerRef](/documentation/iobluetoothui/iobluetoothpairingcontrollerref)
- [IOBluetoothPasskeyDisplay](/documentation/iobluetoothui/iobluetoothpasskeydisplay)

### Instance Properties

- [var backgroundImageConstraint: NSLayoutConstraint!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/backgroundimageconstraint)
- [var centeredView: NSView!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/centeredview)
- [var isIncomingRequest: Bool](/documentation/iobluetoothui/iobluetoothpasskeydisplay/isincomingrequest-swift.property)
- [var passkey: String!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/passkey-swift.property)
- [var returnHighlightImage: NSImage!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/returnhighlightimage)
- [var returnImage: NSImage!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/returnimage)
- [var usePasskeyNotificaitons: Bool](/documentation/iobluetoothui/iobluetoothpasskeydisplay/usepasskeynotificaitons)

### Instance Methods

- [func advancePasskeyIndicator()](/documentation/iobluetoothui/iobluetoothpasskeydisplay/advancepasskeyindicator())
- [func resetPasskeyIndicator()](/documentation/iobluetoothui/iobluetoothpasskeydisplay/resetpasskeyindicator())
- [func retreatPasskeyIndicator()](/documentation/iobluetoothui/iobluetoothpasskeydisplay/retreatpasskeyindicator())
- [func setPasskey(String!, for: IOBluetoothDevice!, usingSSP: Bool)](/documentation/iobluetoothui/iobluetoothpasskeydisplay/setpasskey(_:for:usingssp:))

### Type Methods

- [class func sharedDisplayView() -> IOBluetoothPasskeyDisplay!](/documentation/iobluetoothui/iobluetoothpasskeydisplay/shareddisplayview())
- [IOBluetoothServiceBrowserController](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller)

### Initializers

- [init!(IOBluetoothServiceBrowserControllerOptions)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/init(_:))

### Instance Methods

- [func addAllowedUUID(IOBluetoothSDPUUID!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/addalloweduuid(_:))
- [func addAllowedUUIDArray([Any]!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/addalloweduuidarray(_:))
- [func beginSheetModal(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!) -> IOReturn](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/beginsheetmodal(for:modaldelegate:didend:contextinfo:))
- [func clearAllowedUUIDs()](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/clearalloweduuids())
- [func getDescriptionText() -> String!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getdescriptiontext())
- [func getOptions() -> IOBluetoothServiceBrowserControllerOptions](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getoptions())
- [func getPrompt() -> String!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getprompt())
- [func getRef() -> Unmanaged<IOBluetoothServiceBrowserControllerRef>!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getref())
- [func getResults() -> [Any]!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getresults())
- [func getSearchAttributes() -> UnsafePointer<IOBluetoothDeviceSearchAttributes>!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/getsearchattributes())
- [func getTitle() -> String!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/gettitle())
- [func runModal() -> Int32](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/runmodal())
- [func setDescriptionText(String!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/setdescriptiontext(_:))
- [func setOptions(IOBluetoothServiceBrowserControllerOptions)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/setoptions(_:))
- [func setPrompt(String!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/setprompt(_:))
- [func setSearchAttributes(UnsafePointer<IOBluetoothDeviceSearchAttributes>!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/setsearchattributes(_:))
- [func setTitle(String!)](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/settitle(_:))

### Type Methods

- [class func withServiceBrowserControllerRef(IOBluetoothServiceBrowserControllerRef!) -> IOBluetoothServiceBrowserController!](/documentation/iobluetoothui/iobluetoothservicebrowsercontroller/withservicebrowsercontrollerref(_:))
- [IOBluetoothServiceBrowserControllerRef](/documentation/iobluetoothui/iobluetoothservicebrowsercontrollerref)

## Reference

- [IOBluetoothUIUserLib.h](/documentation/iobluetoothui/iobluetoothuiuserlib-h)

### Constants

- [IOBluetoothServiceBrowserControllerOptions](/documentation/iobluetoothui/iobluetoothservicebrowsercontrolleroptions)

#### Constants

- [var kIOBluetoothServiceBrowserControllerOptionsNone: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsnone)
- [var kIOBluetoothServiceBrowserControllerOptionsAutoStartInquiry: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsautostartinquiry)
- [var kIOBluetoothServiceBrowserControllerOptionsDisconnectWhenDone: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsdisconnectwhendone)
- [IOBluetoothUI Enumerations](/documentation/iobluetoothui/iobluetoothui-enumerations)

### Enumerations

- [Anonymous](/documentation/iobluetoothui/1411883-anonymous)

#### Constants

- [var kIOBluetoothServiceBrowserControllerOptionsAutoStartInquiry: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsautostartinquiry)
- [var kIOBluetoothServiceBrowserControllerOptionsDisconnectWhenDone: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsdisconnectwhendone)
- [var kIOBluetoothServiceBrowserControllerOptionsNone: Int](/documentation/iobluetoothui/kiobluetoothservicebrowsercontrolleroptionsnone)
- [Anonymous](/documentation/iobluetoothui/1411865-anonymous)

#### Constants

- [var kIOBluetoothUISuccess: Int](/documentation/iobluetoothui/kiobluetoothuisuccess)
- [var kIOBluetoothUIUserCanceledErr: Int](/documentation/iobluetoothui/kiobluetoothuiusercancelederr)
- [BluetoothKeyboardReturnType](/documentation/iobluetoothui/bluetoothkeyboardreturntype)

#### Constants

- [init(UInt32)](/documentation/iobluetoothui/bluetoothkeyboardreturntype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetoothui/bluetoothkeyboardreturntype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetoothui/bluetoothkeyboardreturntype/rawvalue)
- [var kBluetoothKeyboardANSIReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardansireturn)
- [var kBluetoothKeyboardISOReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardisoreturn)
- [var kBluetoothKeyboardJISReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardjisreturn)
- [var kBluetoothKeyboardNoReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardnoreturn)
- [IOBluetoothUI Constants](/documentation/iobluetoothui/iobluetoothui-constants)

### Constants

- [var kBluetoothKeyboardANSIReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardansireturn)
- [var kBluetoothKeyboardISOReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardisoreturn)
- [var kBluetoothKeyboardJISReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardjisreturn)
- [var kBluetoothKeyboardNoReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardnoreturn)
- [IOBluetoothUI Functions](/documentation/iobluetoothui/iobluetoothui-functions)

### Functions

- [func IOBluetoothGetDeviceSelectorController() -> Unmanaged<IOBluetoothDeviceSelectorControllerRef>!](/documentation/iobluetoothui/iobluetoothgetdeviceselectorcontroller())
- [func IOBluetoothGetPairingController() -> Unmanaged<IOBluetoothPairingControllerRef>!](/documentation/iobluetoothui/iobluetoothgetpairingcontroller())
- [func IOBluetoothValidateHardwareWithDescription(CFString!, CFString!) -> IOReturn](/documentation/iobluetoothui/iobluetoothvalidatehardwarewithdescription(_:_:))

## Structures

- [BluetoothKeyboardReturnType](/documentation/iobluetoothui/bluetoothkeyboardreturntype)

### Constants

- [init(UInt32)](/documentation/iobluetoothui/bluetoothkeyboardreturntype/init(_:))
- [init(rawValue: UInt32)](/documentation/iobluetoothui/bluetoothkeyboardreturntype/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/iobluetoothui/bluetoothkeyboardreturntype/rawvalue)
- [var kBluetoothKeyboardANSIReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardansireturn)
- [var kBluetoothKeyboardISOReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardisoreturn)
- [var kBluetoothKeyboardJISReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardjisreturn)
- [var kBluetoothKeyboardNoReturn: BluetoothKeyboardReturnType](/documentation/iobluetoothui/kbluetoothkeyboardnoreturn)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
