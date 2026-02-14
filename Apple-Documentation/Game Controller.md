# Game Controller Documentation

Source: https://sosumi.ai/documentation/gamecontroller

---
title: Game Controller
source: https://developer.apple.com/documentation/gamecontroller
timestamp: 2026-02-13T18:57:15.319Z
---

## Essentials

- [Game Controller updates](/documentation/updates/gamecontroller)
- [GCSupportsControllerUserInteraction](/documentation/bundleresources/information-property-list/gcsupportscontrolleruserinteraction)
- [GCSupportedGameControllers](/documentation/bundleresources/information-property-list/gcsupportedgamecontrollers)
- [GCSupportsMultipleMicroGamepads](/documentation/bundleresources/information-property-list/gcsupportsmultiplemicrogamepads)
- [Handling input events](/documentation/gamecontroller/handling-input-events)

## View controller

- [GCEventViewController](/documentation/gamecontroller/gceventviewcontroller)

### Delivering game controller inputs

- [var controllerUserInteractionEnabled: Bool](/documentation/gamecontroller/gceventviewcontroller/controlleruserinteractionenabled)

## Game controllers

- [Supporting Game Controllers](/documentation/gamecontroller/supporting-game-controllers)
- [Letting players use their second-generation Siri Remote as a game controller](/documentation/gamecontroller/letting-players-use-their-second-generation-siri-remote-as-a-game-controller)
- [Discovering and tracking spatial game controllers and styli](/documentation/gamecontroller/discovering-and-tracking-spatial-game-controllers-and-styli)
- [GCDevice](/documentation/gamecontroller/gcdevice)

### Getting device information

- [var vendorName: String?](/documentation/gamecontroller/gcdevice/vendorname)
- [var productCategory: String](/documentation/gamecontroller/gcdevice/productcategory)
- [Product category constants](/documentation/gamecontroller/product-category-constants)

#### Game controller categories

- [let GCProductCategoryDualSense: String](/documentation/gamecontroller/gcproductcategorydualsense)
- [let GCProductCategoryDualShock4: String](/documentation/gamecontroller/gcproductcategorydualshock4)
- [let GCProductCategoryMFi: String](/documentation/gamecontroller/gcproductcategorymfi)
- [let GCProductCategoryXboxOne: String](/documentation/gamecontroller/gcproductcategoryxboxone)
- [let GCProductCategoryArcadeStick: String](/documentation/gamecontroller/gcproductcategoryarcadestick)
- [let GCProductCategoryHID: String](/documentation/gamecontroller/gcproductcategoryhid)

#### Apple TV remote categories

- [let GCProductCategorySiriRemote1stGen: String](/documentation/gamecontroller/gcproductcategorysiriremote1stgen)
- [let GCProductCategorySiriRemote2ndGen: String](/documentation/gamecontroller/gcproductcategorysiriremote2ndgen)
- [let GCProductCategoryControlCenterRemote: String](/documentation/gamecontroller/gcproductcategorycontrolcenterremote)
- [let GCProductCategoryUniversalElectronicsRemote: String](/documentation/gamecontroller/gcproductcategoryuniversalelectronicsremote)
- [let GCProductCategoryCoalescedRemote: String](/documentation/gamecontroller/gcproductcategorycoalescedremote)

#### Mouse and keyboard categories

- [let GCProductCategoryMouse: String](/documentation/gamecontroller/gcproductcategorymouse)
- [let GCProductCategoryKeyboard: String](/documentation/gamecontroller/gcproductcategorykeyboard)

#### Spatial categoriess

- [let GCProductCategorySpatialStylus: String](/documentation/gamecontroller/gcproductcategoryspatialstylus)
- [let GCProductCategorySpatialController: String](/documentation/gamecontroller/gcproductcategoryspatialcontroller)

### Handling input

- [var handlerQueue: dispatch_queue_t](/documentation/gamecontroller/gcdevice/handlerqueue)
- [var physicalInputProfile: GCPhysicalInputProfile](/documentation/gamecontroller/gcdevice/physicalinputprofile)
- [GCController](/documentation/gamecontroller/gccontroller)

### Discovering controllers

- [class func controllers() -> [GCController]](/documentation/gamecontroller/gccontroller/controllers())
- [class func startWirelessControllerDiscovery(completionHandler: (() -> Void)?)](/documentation/gamecontroller/gccontroller/startwirelesscontrollerdiscovery(completionhandler:))
- [class func stopWirelessControllerDiscovery()](/documentation/gamecontroller/gccontroller/stopwirelesscontrollerdiscovery())
- [static let GCControllerDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gccontrollerdidconnect)
- [static let GCControllerDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gccontrollerdiddisconnect)

### Handling multiple controllers

- [class var current: GCController?](/documentation/gamecontroller/gccontroller/current)
- [static let GCControllerDidBecomeCurrent: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gccontrollerdidbecomecurrent)
- [static let GCControllerDidStopBeingCurrent: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gccontrollerdidstopbeingcurrent)

### Inspecting a controller

- [var isAttachedToDevice: Bool](/documentation/gamecontroller/gccontroller/isattachedtodevice)
- [class func supportsHIDDevice(IOHIDDevice) -> Bool](/documentation/gamecontroller/gccontroller/supportshiddevice(_:))
- [class var shouldMonitorBackgroundEvents: Bool](/documentation/gamecontroller/gccontroller/shouldmonitorbackgroundevents)

### Accessing controller input

- [var input: GCControllerLiveInput](/documentation/gamecontroller/gccontroller/input)
- [GCControllerLiveInput](/documentation/gamecontroller/gccontrollerliveinput)

#### Handling device input

- [func nextInputState() -> (any GCControllerInputState & GCDevicePhysicalInputStateDiff)?](/documentation/gamecontroller/gccontrollerliveinput/nextinputstate())
- [func capture() -> GCControllerInputState](/documentation/gamecontroller/gccontrollerliveinput/capture())

#### Remapping controls

- [var unmapped: GCControllerLiveInput?](/documentation/gamecontroller/gccontrollerliveinput/unmapped)
- [GCControllerInputState](/documentation/gamecontroller/gccontrollerinputstate)

### Accessing controller profiles

- [var extendedGamepad: GCExtendedGamepad?](/documentation/gamecontroller/gccontroller/extendedgamepad)
- [GCPhysicalInputProfile](/documentation/gamecontroller/gcphysicalinputprofile)

#### Getting the device

- [var device: (any GCDevice)?](/documentation/gamecontroller/gcphysicalinputprofile/device)

#### Getting change information

- [var lastEventTimestamp: TimeInterval](/documentation/gamecontroller/gcphysicalinputprofile/lasteventtimestamp)
- [var valueDidChangeHandler: ((GCPhysicalInputProfile, GCControllerElement) -> Void)?](/documentation/gamecontroller/gcphysicalinputprofile/valuedidchangehandler)

#### Accessing elements by name or key

- [var elements: [String : GCControllerElement]](/documentation/gamecontroller/gcphysicalinputprofile/elements)
- [var buttons: [String : GCControllerButtonInput]](/documentation/gamecontroller/gcphysicalinputprofile/buttons)
- [var axes: [String : GCControllerAxisInput]](/documentation/gamecontroller/gcphysicalinputprofile/axes)
- [var dpads: [String : GCControllerDirectionPad]](/documentation/gamecontroller/gcphysicalinputprofile/dpads)
- [var touchpads: [String : GCControllerTouchpad]](/documentation/gamecontroller/gcphysicalinputprofile/touchpads)
- [subscript(String) -> GCControllerElement?](/documentation/gamecontroller/gcphysicalinputprofile/subscript(_:))

#### Getting elements by type

- [var allElements: Set<GCControllerElement>](/documentation/gamecontroller/gcphysicalinputprofile/allelements)
- [var allButtons: Set<GCControllerButtonInput>](/documentation/gamecontroller/gcphysicalinputprofile/allbuttons)
- [var allAxes: Set<GCControllerAxisInput>](/documentation/gamecontroller/gcphysicalinputprofile/allaxes)
- [var allDpads: Set<GCControllerDirectionPad>](/documentation/gamecontroller/gcphysicalinputprofile/alldpads)
- [var allTouchpads: Set<GCControllerTouchpad>](/documentation/gamecontroller/gcphysicalinputprofile/alltouchpads)

#### Setting snapshot values

- [func capture() -> Self](/documentation/gamecontroller/gcphysicalinputprofile/capture())
- [func setStateFromPhysicalInput(GCPhysicalInputProfile)](/documentation/gamecontroller/gcphysicalinputprofile/setstatefromphysicalinput(_:))

#### Remapping input elements

- [var hasRemappedElements: Bool](/documentation/gamecontroller/gcphysicalinputprofile/hasremappedelements)
- [func mappedElementAlias(forPhysicalInputName: String) -> String](/documentation/gamecontroller/gcphysicalinputprofile/mappedelementalias(forphysicalinputname:))
- [func mappedPhysicalInputNames(forElementAlias: String) -> Set<String>](/documentation/gamecontroller/gcphysicalinputprofile/mappedphysicalinputnames(forelementalias:))
- [static let GCControllerUserCustomizationsDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gccontrollerusercustomizationsdidchange)
- [GCKeyboardInput](/documentation/gamecontroller/gckeyboardinput)

#### Getting Change Information

- [var keyChangedHandler: GCKeyboardValueChangedHandler?](/documentation/gamecontroller/gckeyboardinput/keychangedhandler)
- [GCKeyboardValueChangedHandler](/documentation/gamecontroller/gckeyboardvaluechangedhandler)

#### Accessing Buttons

- [var isAnyKeyPressed: Bool](/documentation/gamecontroller/gckeyboardinput/isanykeypressed)
- [func button(forKeyCode: GCKeyCode) -> GCControllerButtonInput?](/documentation/gamecontroller/gckeyboardinput/button(forkeycode:))
- [GCKeyCode](/documentation/gamecontroller/gckeycode)

##### Letter and Number Keys

- [static let keyA: GCKeyCode](/documentation/gamecontroller/gckeycode/keya)
- [static let keyB: GCKeyCode](/documentation/gamecontroller/gckeycode/keyb)
- [static let keyC: GCKeyCode](/documentation/gamecontroller/gckeycode/keyc)
- [static let keyD: GCKeyCode](/documentation/gamecontroller/gckeycode/keyd)
- [static let keyE: GCKeyCode](/documentation/gamecontroller/gckeycode/keye)
- [static let keyF: GCKeyCode](/documentation/gamecontroller/gckeycode/keyf)
- [static let keyG: GCKeyCode](/documentation/gamecontroller/gckeycode/keyg)
- [static let keyH: GCKeyCode](/documentation/gamecontroller/gckeycode/keyh)
- [static let keyI: GCKeyCode](/documentation/gamecontroller/gckeycode/keyi)
- [static let keyJ: GCKeyCode](/documentation/gamecontroller/gckeycode/keyj)
- [static let keyK: GCKeyCode](/documentation/gamecontroller/gckeycode/keyk)
- [static let keyL: GCKeyCode](/documentation/gamecontroller/gckeycode/keyl)
- [static let keyM: GCKeyCode](/documentation/gamecontroller/gckeycode/keym)
- [static let keyN: GCKeyCode](/documentation/gamecontroller/gckeycode/keyn)
- [static let keyO: GCKeyCode](/documentation/gamecontroller/gckeycode/keyo)
- [static let keyP: GCKeyCode](/documentation/gamecontroller/gckeycode/keyp)
- [static let keyQ: GCKeyCode](/documentation/gamecontroller/gckeycode/keyq)
- [static let keyR: GCKeyCode](/documentation/gamecontroller/gckeycode/keyr)
- [static let keyS: GCKeyCode](/documentation/gamecontroller/gckeycode/keys)
- [static let keyT: GCKeyCode](/documentation/gamecontroller/gckeycode/keyt)
- [static let keyU: GCKeyCode](/documentation/gamecontroller/gckeycode/keyu)
- [static let keyV: GCKeyCode](/documentation/gamecontroller/gckeycode/keyv)
- [static let keyW: GCKeyCode](/documentation/gamecontroller/gckeycode/keyw)
- [static let keyX: GCKeyCode](/documentation/gamecontroller/gckeycode/keyx)
- [static let keyY: GCKeyCode](/documentation/gamecontroller/gckeycode/keyy)
- [static let keyZ: GCKeyCode](/documentation/gamecontroller/gckeycode/keyz)
- [static let one: GCKeyCode](/documentation/gamecontroller/gckeycode/one)
- [static let two: GCKeyCode](/documentation/gamecontroller/gckeycode/two)
- [static let three: GCKeyCode](/documentation/gamecontroller/gckeycode/three)
- [static let four: GCKeyCode](/documentation/gamecontroller/gckeycode/four)
- [static let five: GCKeyCode](/documentation/gamecontroller/gckeycode/five)
- [static let six: GCKeyCode](/documentation/gamecontroller/gckeycode/six)
- [static let seven: GCKeyCode](/documentation/gamecontroller/gckeycode/seven)
- [static let eight: GCKeyCode](/documentation/gamecontroller/gckeycode/eight)
- [static let nine: GCKeyCode](/documentation/gamecontroller/gckeycode/nine)
- [static let zero: GCKeyCode](/documentation/gamecontroller/gckeycode/zero)

##### Punctuation and Command Keys

- [static let tab: GCKeyCode](/documentation/gamecontroller/gckeycode/tab)
- [static let spacebar: GCKeyCode](/documentation/gamecontroller/gckeycode/spacebar)
- [static let hyphen: GCKeyCode](/documentation/gamecontroller/gckeycode/hyphen)
- [static let equalSign: GCKeyCode](/documentation/gamecontroller/gckeycode/equalsign)
- [static let openBracket: GCKeyCode](/documentation/gamecontroller/gckeycode/openbracket)
- [static let closeBracket: GCKeyCode](/documentation/gamecontroller/gckeycode/closebracket)
- [static let backslash: GCKeyCode](/documentation/gamecontroller/gckeycode/backslash)
- [static let nonUSPound: GCKeyCode](/documentation/gamecontroller/gckeycode/nonuspound)
- [static let semicolon: GCKeyCode](/documentation/gamecontroller/gckeycode/semicolon)
- [static let quote: GCKeyCode](/documentation/gamecontroller/gckeycode/quote)
- [static let graveAccentAndTilde: GCKeyCode](/documentation/gamecontroller/gckeycode/graveaccentandtilde)
- [static let comma: GCKeyCode](/documentation/gamecontroller/gckeycode/comma)
- [static let period: GCKeyCode](/documentation/gamecontroller/gckeycode/period)
- [static let slash: GCKeyCode](/documentation/gamecontroller/gckeycode/slash)
- [static let capsLock: GCKeyCode](/documentation/gamecontroller/gckeycode/capslock)
- [static let deleteOrBackspace: GCKeyCode](/documentation/gamecontroller/gckeycode/deleteorbackspace)
- [static let escape: GCKeyCode](/documentation/gamecontroller/gckeycode/escape)
- [static let returnOrEnter: GCKeyCode](/documentation/gamecontroller/gckeycode/returnorenter)
- [static let nonUSBackslash: GCKeyCode](/documentation/gamecontroller/gckeycode/nonusbackslash)
- [static let application: GCKeyCode](/documentation/gamecontroller/gckeycode/application)
- [static let power: GCKeyCode](/documentation/gamecontroller/gckeycode/power)

##### Function Keys

- [static let F1: GCKeyCode](/documentation/gamecontroller/gckeycode/f1)
- [static let F2: GCKeyCode](/documentation/gamecontroller/gckeycode/f2)
- [static let F3: GCKeyCode](/documentation/gamecontroller/gckeycode/f3)
- [static let F4: GCKeyCode](/documentation/gamecontroller/gckeycode/f4)
- [static let F5: GCKeyCode](/documentation/gamecontroller/gckeycode/f5)
- [static let F6: GCKeyCode](/documentation/gamecontroller/gckeycode/f6)
- [static let F7: GCKeyCode](/documentation/gamecontroller/gckeycode/f7)
- [static let F8: GCKeyCode](/documentation/gamecontroller/gckeycode/f8)
- [static let F9: GCKeyCode](/documentation/gamecontroller/gckeycode/f9)
- [static let F10: GCKeyCode](/documentation/gamecontroller/gckeycode/f10)
- [static let F11: GCKeyCode](/documentation/gamecontroller/gckeycode/f11)
- [static let F12: GCKeyCode](/documentation/gamecontroller/gckeycode/f12)
- [static let F13: GCKeyCode](/documentation/gamecontroller/gckeycode/f13)
- [static let F14: GCKeyCode](/documentation/gamecontroller/gckeycode/f14)
- [static let F15: GCKeyCode](/documentation/gamecontroller/gckeycode/f15)
- [static let F16: GCKeyCode](/documentation/gamecontroller/gckeycode/f16)
- [static let F17: GCKeyCode](/documentation/gamecontroller/gckeycode/f17)
- [static let F18: GCKeyCode](/documentation/gamecontroller/gckeycode/f18)
- [static let F19: GCKeyCode](/documentation/gamecontroller/gckeycode/f19)
- [static let F20: GCKeyCode](/documentation/gamecontroller/gckeycode/f20)

##### Directional and Similar Keys

- [static let printScreen: GCKeyCode](/documentation/gamecontroller/gckeycode/printscreen)
- [static let scrollLock: GCKeyCode](/documentation/gamecontroller/gckeycode/scrolllock)
- [static let pause: GCKeyCode](/documentation/gamecontroller/gckeycode/pause)
- [static let insert: GCKeyCode](/documentation/gamecontroller/gckeycode/insert)
- [static let home: GCKeyCode](/documentation/gamecontroller/gckeycode/home)
- [static let pageUp: GCKeyCode](/documentation/gamecontroller/gckeycode/pageup)
- [static let deleteForward: GCKeyCode](/documentation/gamecontroller/gckeycode/deleteforward)
- [static let end: GCKeyCode](/documentation/gamecontroller/gckeycode/end)
- [static let pageDown: GCKeyCode](/documentation/gamecontroller/gckeycode/pagedown)
- [static let rightArrow: GCKeyCode](/documentation/gamecontroller/gckeycode/rightarrow)
- [static let leftArrow: GCKeyCode](/documentation/gamecontroller/gckeycode/leftarrow)
- [static let downArrow: GCKeyCode](/documentation/gamecontroller/gckeycode/downarrow)
- [static let upArrow: GCKeyCode](/documentation/gamecontroller/gckeycode/uparrow)

##### Keypad Keys

- [static let keypadNumLock: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadnumlock)
- [static let keypadSlash: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadslash)
- [static let keypadAsterisk: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadasterisk)
- [static let keypadHyphen: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadhyphen)
- [static let keypadPlus: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadplus)
- [static let keypadEnter: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadenter)
- [static let keypad1: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad1)
- [static let keypad2: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad2)
- [static let keypad3: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad3)
- [static let keypad4: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad4)
- [static let keypad5: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad5)
- [static let keypad6: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad6)
- [static let keypad7: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad7)
- [static let keypad8: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad8)
- [static let keypad9: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad9)
- [static let keypad0: GCKeyCode](/documentation/gamecontroller/gckeycode/keypad0)
- [static let keypadPeriod: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadperiod)
- [static let keypadEqualSign: GCKeyCode](/documentation/gamecontroller/gckeycode/keypadequalsign)

##### International Keys

- [static let international1: GCKeyCode](/documentation/gamecontroller/gckeycode/international1)
- [static let international2: GCKeyCode](/documentation/gamecontroller/gckeycode/international2)
- [static let international3: GCKeyCode](/documentation/gamecontroller/gckeycode/international3)
- [static let international4: GCKeyCode](/documentation/gamecontroller/gckeycode/international4)
- [static let international5: GCKeyCode](/documentation/gamecontroller/gckeycode/international5)
- [static let international6: GCKeyCode](/documentation/gamecontroller/gckeycode/international6)
- [static let international7: GCKeyCode](/documentation/gamecontroller/gckeycode/international7)
- [static let international8: GCKeyCode](/documentation/gamecontroller/gckeycode/international8)
- [static let international9: GCKeyCode](/documentation/gamecontroller/gckeycode/international9)

##### Language Keys

- [static let LANG1: GCKeyCode](/documentation/gamecontroller/gckeycode/lang1)
- [static let LANG2: GCKeyCode](/documentation/gamecontroller/gckeycode/lang2)
- [static let LANG3: GCKeyCode](/documentation/gamecontroller/gckeycode/lang3)
- [static let LANG4: GCKeyCode](/documentation/gamecontroller/gckeycode/lang4)
- [static let LANG5: GCKeyCode](/documentation/gamecontroller/gckeycode/lang5)
- [static let LANG6: GCKeyCode](/documentation/gamecontroller/gckeycode/lang6)
- [static let LANG7: GCKeyCode](/documentation/gamecontroller/gckeycode/lang7)
- [static let LANG8: GCKeyCode](/documentation/gamecontroller/gckeycode/lang8)
- [static let LANG9: GCKeyCode](/documentation/gamecontroller/gckeycode/lang9)

##### Left- and Right-Side Keys

- [static let leftControl: GCKeyCode](/documentation/gamecontroller/gckeycode/leftcontrol)
- [static let leftShift: GCKeyCode](/documentation/gamecontroller/gckeycode/leftshift)
- [static let leftAlt: GCKeyCode](/documentation/gamecontroller/gckeycode/leftalt)
- [static let leftGUI: GCKeyCode](/documentation/gamecontroller/gckeycode/leftgui)
- [static let rightControl: GCKeyCode](/documentation/gamecontroller/gckeycode/rightcontrol)
- [static let rightShift: GCKeyCode](/documentation/gamecontroller/gckeycode/rightshift)
- [static let rightAlt: GCKeyCode](/documentation/gamecontroller/gckeycode/rightalt)
- [static let rightGUI: GCKeyCode](/documentation/gamecontroller/gckeycode/rightgui)

##### Initializers

- [init(rawValue: CFIndex)](/documentation/gamecontroller/gckeycode/init(rawvalue:))
- [Keycode Constants](/documentation/gamecontroller/keycode-constants)

##### Letter and Number Keys

- [let GCKeyA: String](/documentation/gamecontroller/gckeya)
- [let GCKeyB: String](/documentation/gamecontroller/gckeyb)
- [let GCKeyC: String](/documentation/gamecontroller/gckeyc)
- [let GCKeyD: String](/documentation/gamecontroller/gckeyd)
- [let GCKeyE: String](/documentation/gamecontroller/gckeye)
- [let GCKeyF: String](/documentation/gamecontroller/gckeyf)
- [let GCKeyG: String](/documentation/gamecontroller/gckeyg)
- [let GCKeyH: String](/documentation/gamecontroller/gckeyh)
- [let GCKeyI: String](/documentation/gamecontroller/gckeyi)
- [let GCKeyJ: String](/documentation/gamecontroller/gckeyj)
- [let GCKeyK: String](/documentation/gamecontroller/gckeyk)
- [let GCKeyL: String](/documentation/gamecontroller/gckeyl)
- [let GCKeyM: String](/documentation/gamecontroller/gckeym)
- [let GCKeyN: String](/documentation/gamecontroller/gckeyn)
- [let GCKeyO: String](/documentation/gamecontroller/gckeyo)
- [let GCKeyP: String](/documentation/gamecontroller/gckeyp)
- [let GCKeyQ: String](/documentation/gamecontroller/gckeyq)
- [let GCKeyR: String](/documentation/gamecontroller/gckeyr)
- [let GCKeyS: String](/documentation/gamecontroller/gckeys)
- [let GCKeyT: String](/documentation/gamecontroller/gckeyt)
- [let GCKeyU: String](/documentation/gamecontroller/gckeyu)
- [let GCKeyV: String](/documentation/gamecontroller/gckeyv)
- [let GCKeyW: String](/documentation/gamecontroller/gckeyw)
- [let GCKeyX: String](/documentation/gamecontroller/gckeyx)
- [let GCKeyY: String](/documentation/gamecontroller/gckeyy)
- [let GCKeyZ: String](/documentation/gamecontroller/gckeyz)
- [let GCKeyOne: String](/documentation/gamecontroller/gckeyone)
- [let GCKeyTwo: String](/documentation/gamecontroller/gckeytwo)
- [let GCKeyThree: String](/documentation/gamecontroller/gckeythree)
- [let GCKeyFour: String](/documentation/gamecontroller/gckeyfour)
- [let GCKeyFive: String](/documentation/gamecontroller/gckeyfive)
- [let GCKeySix: String](/documentation/gamecontroller/gckeysix)
- [let GCKeySeven: String](/documentation/gamecontroller/gckeyseven)
- [let GCKeyEight: String](/documentation/gamecontroller/gckeyeight)
- [let GCKeyNine: String](/documentation/gamecontroller/gckeynine)
- [let GCKeyZero: String](/documentation/gamecontroller/gckeyzero)

##### Punctuation and Command Keys

- [let GCKeyTab: String](/documentation/gamecontroller/gckeytab)
- [let GCKeySpacebar: String](/documentation/gamecontroller/gckeyspacebar)
- [let GCKeyHyphen: String](/documentation/gamecontroller/gckeyhyphen)
- [let GCKeyEqualSign: String](/documentation/gamecontroller/gckeyequalsign)
- [let GCKeyOpenBracket: String](/documentation/gamecontroller/gckeyopenbracket)
- [let GCKeyCloseBracket: String](/documentation/gamecontroller/gckeyclosebracket)
- [let GCKeyBackslash: String](/documentation/gamecontroller/gckeybackslash)
- [let GCKeyNonUSPound: String](/documentation/gamecontroller/gckeynonuspound)
- [let GCKeySemicolon: String](/documentation/gamecontroller/gckeysemicolon)
- [let GCKeyQuote: String](/documentation/gamecontroller/gckeyquote)
- [let GCKeyGraveAccentAndTilde: String](/documentation/gamecontroller/gckeygraveaccentandtilde)
- [let GCKeyComma: String](/documentation/gamecontroller/gckeycomma)
- [let GCKeyPeriod: String](/documentation/gamecontroller/gckeyperiod)
- [let GCKeySlash: String](/documentation/gamecontroller/gckeyslash)
- [let GCKeyCapsLock: String](/documentation/gamecontroller/gckeycapslock)
- [let GCKeyDeleteOrBackspace: String](/documentation/gamecontroller/gckeydeleteorbackspace)
- [let GCKeyEscape: String](/documentation/gamecontroller/gckeyescape)
- [let GCKeyReturnOrEnter: String](/documentation/gamecontroller/gckeyreturnorenter)
- [let GCKeyNonUSBackslash: String](/documentation/gamecontroller/gckeynonusbackslash)
- [let GCKeyApplication: String](/documentation/gamecontroller/gckeyapplication)
- [let GCKeyPower: String](/documentation/gamecontroller/gckeypower)

##### Function Keys

- [let GCKeyF1: String](/documentation/gamecontroller/gckeyf1)
- [let GCKeyF2: String](/documentation/gamecontroller/gckeyf2)
- [let GCKeyF3: String](/documentation/gamecontroller/gckeyf3)
- [let GCKeyF4: String](/documentation/gamecontroller/gckeyf4)
- [let GCKeyF5: String](/documentation/gamecontroller/gckeyf5)
- [let GCKeyF6: String](/documentation/gamecontroller/gckeyf6)
- [let GCKeyF7: String](/documentation/gamecontroller/gckeyf7)
- [let GCKeyF8: String](/documentation/gamecontroller/gckeyf8)
- [let GCKeyF9: String](/documentation/gamecontroller/gckeyf9)
- [let GCKeyF10: String](/documentation/gamecontroller/gckeyf10)
- [let GCKeyF11: String](/documentation/gamecontroller/gckeyf11)
- [let GCKeyF12: String](/documentation/gamecontroller/gckeyf12)
- [let GCKeyF13: String](/documentation/gamecontroller/gckeyf13)
- [let GCKeyF14: String](/documentation/gamecontroller/gckeyf14)
- [let GCKeyF15: String](/documentation/gamecontroller/gckeyf15)
- [let GCKeyF16: String](/documentation/gamecontroller/gckeyf16)
- [let GCKeyF17: String](/documentation/gamecontroller/gckeyf17)
- [let GCKeyF18: String](/documentation/gamecontroller/gckeyf18)
- [let GCKeyF19: String](/documentation/gamecontroller/gckeyf19)
- [let GCKeyF20: String](/documentation/gamecontroller/gckeyf20)

##### Directional and Similar Keys

- [let GCKeyPrintScreen: String](/documentation/gamecontroller/gckeyprintscreen)
- [let GCKeyScrollLock: String](/documentation/gamecontroller/gckeyscrolllock)
- [let GCKeyPause: String](/documentation/gamecontroller/gckeypause)
- [let GCKeyInsert: String](/documentation/gamecontroller/gckeyinsert)
- [let GCKeyHome: String](/documentation/gamecontroller/gckeyhome)
- [let GCKeyPageUp: String](/documentation/gamecontroller/gckeypageup)
- [let GCKeyDeleteForward: String](/documentation/gamecontroller/gckeydeleteforward)
- [let GCKeyEnd: String](/documentation/gamecontroller/gckeyend)
- [let GCKeyPageDown: String](/documentation/gamecontroller/gckeypagedown)
- [let GCKeyRightArrow: String](/documentation/gamecontroller/gckeyrightarrow)
- [let GCKeyLeftArrow: String](/documentation/gamecontroller/gckeyleftarrow)
- [let GCKeyDownArrow: String](/documentation/gamecontroller/gckeydownarrow)
- [let GCKeyUpArrow: String](/documentation/gamecontroller/gckeyuparrow)

##### Keypad Keys

- [let GCKeyKeypadNumLock: String](/documentation/gamecontroller/gckeykeypadnumlock)
- [let GCKeyKeypadSlash: String](/documentation/gamecontroller/gckeykeypadslash)
- [let GCKeyKeypadAsterisk: String](/documentation/gamecontroller/gckeykeypadasterisk)
- [let GCKeyKeypadHyphen: String](/documentation/gamecontroller/gckeykeypadhyphen)
- [let GCKeyKeypadPlus: String](/documentation/gamecontroller/gckeykeypadplus)
- [let GCKeyKeypadEnter: String](/documentation/gamecontroller/gckeykeypadenter)
- [let GCKeyKeypad1: String](/documentation/gamecontroller/gckeykeypad1)
- [let GCKeyKeypad2: String](/documentation/gamecontroller/gckeykeypad2)
- [let GCKeyKeypad3: String](/documentation/gamecontroller/gckeykeypad3)
- [let GCKeyKeypad4: String](/documentation/gamecontroller/gckeykeypad4)
- [let GCKeyKeypad5: String](/documentation/gamecontroller/gckeykeypad5)
- [let GCKeyKeypad6: String](/documentation/gamecontroller/gckeykeypad6)
- [let GCKeyKeypad7: String](/documentation/gamecontroller/gckeykeypad7)
- [let GCKeyKeypad8: String](/documentation/gamecontroller/gckeykeypad8)
- [let GCKeyKeypad9: String](/documentation/gamecontroller/gckeykeypad9)
- [let GCKeyKeypad0: String](/documentation/gamecontroller/gckeykeypad0)
- [let GCKeyKeypadPeriod: String](/documentation/gamecontroller/gckeykeypadperiod)
- [let GCKeyKeypadEqualSign: String](/documentation/gamecontroller/gckeykeypadequalsign)

##### International Keys

- [let GCKeyInternational1: String](/documentation/gamecontroller/gckeyinternational1)
- [let GCKeyInternational2: String](/documentation/gamecontroller/gckeyinternational2)
- [let GCKeyInternational3: String](/documentation/gamecontroller/gckeyinternational3)
- [let GCKeyInternational4: String](/documentation/gamecontroller/gckeyinternational4)
- [let GCKeyInternational5: String](/documentation/gamecontroller/gckeyinternational5)
- [let GCKeyInternational6: String](/documentation/gamecontroller/gckeyinternational6)
- [let GCKeyInternational7: String](/documentation/gamecontroller/gckeyinternational7)
- [let GCKeyInternational8: String](/documentation/gamecontroller/gckeyinternational8)
- [let GCKeyInternational9: String](/documentation/gamecontroller/gckeyinternational9)

##### Language Keys

- [let GCKeyLANG1: String](/documentation/gamecontroller/gckeylang1)
- [let GCKeyLANG2: String](/documentation/gamecontroller/gckeylang2)
- [let GCKeyLANG3: String](/documentation/gamecontroller/gckeylang3)
- [let GCKeyLANG4: String](/documentation/gamecontroller/gckeylang4)
- [let GCKeyLANG5: String](/documentation/gamecontroller/gckeylang5)
- [let GCKeyLANG6: String](/documentation/gamecontroller/gckeylang6)
- [let GCKeyLANG7: String](/documentation/gamecontroller/gckeylang7)
- [let GCKeyLANG8: String](/documentation/gamecontroller/gckeylang8)
- [let GCKeyLANG9: String](/documentation/gamecontroller/gckeylang9)

##### Left- and Right-Side Keys

- [let GCKeyLeftControl: String](/documentation/gamecontroller/gckeyleftcontrol)
- [let GCKeyLeftShift: String](/documentation/gamecontroller/gckeyleftshift)
- [let GCKeyLeftAlt: String](/documentation/gamecontroller/gckeyleftalt)
- [let GCKeyLeftGUI: String](/documentation/gamecontroller/gckeyleftgui)
- [let GCKeyRightControl: String](/documentation/gamecontroller/gckeyrightcontrol)
- [let GCKeyRightShift: String](/documentation/gamecontroller/gckeyrightshift)
- [let GCKeyRightAlt: String](/documentation/gamecontroller/gckeyrightalt)
- [let GCKeyRightGUI: String](/documentation/gamecontroller/gckeyrightgui)
- [GCMouseInput](/documentation/gamecontroller/gcmouseinput)

#### Getting Change Information

- [var mouseMovedHandler: GCMouseMoved?](/documentation/gamecontroller/gcmouseinput/mousemovedhandler)
- [GCMouseMoved](/documentation/gamecontroller/gcmousemoved)

#### Accessing Buttons

- [var leftButton: GCControllerButtonInput](/documentation/gamecontroller/gcmouseinput/leftbutton)
- [var rightButton: GCControllerButtonInput?](/documentation/gamecontroller/gcmouseinput/rightbutton)
- [var middleButton: GCControllerButtonInput?](/documentation/gamecontroller/gcmouseinput/middlebutton)
- [var auxiliaryButtons: [GCControllerButtonInput]?](/documentation/gamecontroller/gcmouseinput/auxiliarybuttons)

#### Scrolling

- [var scroll: GCDeviceCursor](/documentation/gamecontroller/gcmouseinput/scroll)
- [GCExtendedGamepad](/documentation/gamecontroller/gcextendedgamepad)

#### Getting the controller

- [var controller: GCController?](/documentation/gamecontroller/gcextendedgamepad/controller)

#### Getting change information

- [var valueChangedHandler: GCExtendedGamepadValueChangedHandler?](/documentation/gamecontroller/gcextendedgamepad/valuechangedhandler)
- [GCExtendedGamepadValueChangedHandler](/documentation/gamecontroller/gcextendedgamepadvaluechangedhandler)

#### Getting shoulder button inputs

- [var leftShoulder: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/leftshoulder)
- [var rightShoulder: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/rightshoulder)

#### Getting trigger inputs

- [var leftTrigger: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/lefttrigger)
- [var rightTrigger: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/righttrigger)

#### Getting face button inputs

- [var buttonMenu: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/buttonmenu)
- [var buttonOptions: GCControllerButtonInput?](/documentation/gamecontroller/gcextendedgamepad/buttonoptions)
- [var buttonHome: GCControllerButtonInput?](/documentation/gamecontroller/gcextendedgamepad/buttonhome)
- [var buttonA: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/buttona)
- [var buttonB: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/buttonb)
- [var buttonX: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/buttonx)
- [var buttonY: GCControllerButtonInput](/documentation/gamecontroller/gcextendedgamepad/buttony)

#### Getting directional pad inputs

- [var dpad: GCControllerDirectionPad](/documentation/gamecontroller/gcextendedgamepad/dpad)

#### Getting thumbstick and thumbstick button inputs

- [var leftThumbstick: GCControllerDirectionPad](/documentation/gamecontroller/gcextendedgamepad/leftthumbstick)
- [var rightThumbstick: GCControllerDirectionPad](/documentation/gamecontroller/gcextendedgamepad/rightthumbstick)
- [var leftThumbstickButton: GCControllerButtonInput?](/documentation/gamecontroller/gcextendedgamepad/leftthumbstickbutton)
- [var rightThumbstickButton: GCControllerButtonInput?](/documentation/gamecontroller/gcextendedgamepad/rightthumbstickbutton)

#### Accessing elements by name

- [Extended gamepad input names](/documentation/gamecontroller/extended-gamepad-input-names)

##### Shoulder button names

- [var GCInputLeftShoulder: String](/documentation/gamecontroller/gcinputleftshoulder-9assr)
- [var GCInputRightShoulder: String](/documentation/gamecontroller/gcinputrightshoulder-5lcq1)

##### Trigger names

- [var GCInputLeftTrigger: String](/documentation/gamecontroller/gcinputlefttrigger-80png)
- [var GCInputRightTrigger: String](/documentation/gamecontroller/gcinputrighttrigger-96vtj)

##### Face button names

- [var GCInputButtonMenu: String](/documentation/gamecontroller/gcinputbuttonmenu-196mn)
- [var GCInputButtonHome: String](/documentation/gamecontroller/gcinputbuttonhome-7xxwm)
- [var GCInputButtonOptions: String](/documentation/gamecontroller/gcinputbuttonoptions-84kj)
- [var GCInputButtonA: String](/documentation/gamecontroller/gcinputbuttona-8z15w)
- [var GCInputButtonB: String](/documentation/gamecontroller/gcinputbuttonb-6z361)
- [var GCInputButtonX: String](/documentation/gamecontroller/gcinputbuttonx-32i2z)
- [var GCInputButtonY: String](/documentation/gamecontroller/gcinputbuttony-9x9i9)

##### Directional pad names

- [var GCInputDirectionPad: String](/documentation/gamecontroller/gcinputdirectionpad-115st)

##### Thumbstick names

- [var GCInputLeftThumbstick: String](/documentation/gamecontroller/gcinputleftthumbstick-3hlff)
- [var GCInputRightThumbstick: String](/documentation/gamecontroller/gcinputrightthumbstick-8469p)
- [var GCInputLeftThumbstickButton: String](/documentation/gamecontroller/gcinputleftthumbstickbutton-7gej3)
- [var GCInputRightThumbstickButton: String](/documentation/gamecontroller/gcinputrightthumbstickbutton-4to77)

#### Setting snapshot values

- [func setStateFrom(GCExtendedGamepad)](/documentation/gamecontroller/gcextendedgamepad/setstatefrom(_:))
- [func saveSnapshot() -> GCExtendedGamepadSnapshot](/documentation/gamecontroller/gcextendedgamepad/savesnapshot())
- [GCDualShockGamepad](/documentation/gamecontroller/gcdualshockgamepad)

#### Getting button input

- [var touchpadButton: GCControllerButtonInput!](/documentation/gamecontroller/gcdualshockgamepad/touchpadbutton)

#### Tracking finger locations

- [var touchpadPrimary: GCControllerDirectionPad!](/documentation/gamecontroller/gcdualshockgamepad/touchpadprimary)
- [var touchpadSecondary: GCControllerDirectionPad!](/documentation/gamecontroller/gcdualshockgamepad/touchpadsecondary)

#### Accessing elements by name

- [DualShock controller input names](/documentation/gamecontroller/dualshock-controller-input-names)

##### DualShock controller button names

- [var GCInputDualShockTouchpadButton: String](/documentation/gamecontroller/gcinputdualshocktouchpadbutton-74k1l)
- [var GCInputDualShockTouchpadOne: String](/documentation/gamecontroller/gcinputdualshocktouchpadone-55wgz)
- [var GCInputDualShockTouchpadTwo: String](/documentation/gamecontroller/gcinputdualshocktouchpadtwo-5f8r9)
- [GCXboxGamepad](/documentation/gamecontroller/gcxboxgamepad)

#### Getting button inputs

- [var paddleButton1: GCControllerButtonInput?](/documentation/gamecontroller/gcxboxgamepad/paddlebutton1)
- [var paddleButton2: GCControllerButtonInput?](/documentation/gamecontroller/gcxboxgamepad/paddlebutton2)
- [var paddleButton3: GCControllerButtonInput?](/documentation/gamecontroller/gcxboxgamepad/paddlebutton3)
- [var paddleButton4: GCControllerButtonInput?](/documentation/gamecontroller/gcxboxgamepad/paddlebutton4)
- [var buttonShare: GCControllerButtonInput?](/documentation/gamecontroller/gcxboxgamepad/buttonshare)

#### Accessing elements by name

- [Xbox controller input names](/documentation/gamecontroller/xbox-controller-input-names)

##### Xbox controller button names

- [var GCInputButtonShare: String](/documentation/gamecontroller/gcinputbuttonshare-87tha)
- [var GCInputXboxPaddleOne: String](/documentation/gamecontroller/gcinputxboxpaddleone-offv)
- [var GCInputXboxPaddleTwo: String](/documentation/gamecontroller/gcinputxboxpaddletwo-4ya43)
- [var GCInputXboxPaddleThree: String](/documentation/gamecontroller/gcinputxboxpaddlethree-6zcw8)
- [var GCInputXboxPaddleFour: String](/documentation/gamecontroller/gcinputxboxpaddlefour-1obrw)
- [GCDualSenseGamepad](/documentation/gamecontroller/gcdualsensegamepad)

#### Getting button input

- [var touchpadButton: GCControllerButtonInput](/documentation/gamecontroller/gcdualsensegamepad/touchpadbutton)

#### Tracking finger locations

- [var touchpadPrimary: GCControllerDirectionPad](/documentation/gamecontroller/gcdualsensegamepad/touchpadprimary)
- [var touchpadSecondary: GCControllerDirectionPad](/documentation/gamecontroller/gcdualsensegamepad/touchpadsecondary)

#### Getting adaptive triggers

- [var leftTrigger: GCDualSenseAdaptiveTrigger](/documentation/gamecontroller/gcdualsensegamepad/lefttrigger)
- [var rightTrigger: GCDualSenseAdaptiveTrigger](/documentation/gamecontroller/gcdualsensegamepad/righttrigger)
- [var microGamepad: GCMicroGamepad?](/documentation/gamecontroller/gccontroller/microgamepad)
- [GCMicroGamepad](/documentation/gamecontroller/gcmicrogamepad)

#### Getting the controller

- [var controller: GCController?](/documentation/gamecontroller/gcmicrogamepad/controller)

#### Receiving a callback when input values change

- [var valueChangedHandler: GCMicroGamepadValueChangedHandler?](/documentation/gamecontroller/gcmicrogamepad/valuechangedhandler)
- [GCMicroGamepadValueChangedHandler](/documentation/gamecontroller/gcmicrogamepadvaluechangedhandler)

#### Getting face button inputs

- [var buttonMenu: GCControllerButtonInput](/documentation/gamecontroller/gcmicrogamepad/buttonmenu)
- [var buttonA: GCControllerButtonInput](/documentation/gamecontroller/gcmicrogamepad/buttona)
- [var buttonX: GCControllerButtonInput](/documentation/gamecontroller/gcmicrogamepad/buttonx)

#### Getting directional pad inputs

- [var dpad: GCControllerDirectionPad](/documentation/gamecontroller/gcmicrogamepad/dpad)
- [var reportsAbsoluteDpadValues: Bool](/documentation/gamecontroller/gcmicrogamepad/reportsabsolutedpadvalues)
- [var allowsRotation: Bool](/documentation/gamecontroller/gcmicrogamepad/allowsrotation)

#### Accessing elements by name

- [Micro gamepad input names](/documentation/gamecontroller/micro-gamepad-input-names)

##### Micro gamepad directional pad name

- [let GCInputMicroGamepadDpad: String](/documentation/gamecontroller/gcinputmicrogamepaddpad)

##### Micro gamepad button names

- [let GCInputMicroGamepadButtonA: String](/documentation/gamecontroller/gcinputmicrogamepadbuttona)
- [let GCInputMicroGamepadButtonX: String](/documentation/gamecontroller/gcinputmicrogamepadbuttonx)
- [let GCInputMicroGamepadButtonMenu: String](/documentation/gamecontroller/gcinputmicrogamepadbuttonmenu)

#### Setting snapshot avlues

- [func setStateFrom(GCMicroGamepad)](/documentation/gamecontroller/gcmicrogamepad/setstatefrom(_:))
- [func saveSnapshot() -> GCMicroGamepadSnapshot](/documentation/gamecontroller/gcmicrogamepad/savesnapshot())
- [GCDirectionalGamepad](/documentation/gamecontroller/gcdirectionalgamepad)

#### Accessing Elements by Name

- [Directional Gamepad Input Names](/documentation/gamecontroller/directional-gamepad-input-names)

##### Directional Pad Names

- [let GCInputDirectionalDpad: String](/documentation/gamecontroller/gcinputdirectionaldpad)
- [let GCInputDirectionalCardinalDpad: String](/documentation/gamecontroller/gcinputdirectionalcardinaldpad)

##### Directional Pad Button Names

- [let GCInputDirectionalTouchSurfaceButton: String](/documentation/gamecontroller/gcinputdirectionaltouchsurfacebutton)
- [let GCInputDirectionalCenterButton: String](/documentation/gamecontroller/gcinputdirectionalcenterbutton)
- [var motion: GCMotion?](/documentation/gamecontroller/gccontroller/motion)
- [var physicalInputProfile: GCPhysicalInputProfile](/documentation/gamecontroller/gccontroller/physicalinputprofile)
- [var gamepad: GCGamepad?](/documentation/gamecontroller/gccontroller/gamepad)

### Accessing controller elements

- [GCControllerElement](/documentation/gamecontroller/gccontrollerelement)

#### Accessing input values

- [var isAnalog: Bool](/documentation/gamecontroller/gccontrollerelement/isanalog)

#### Getting a localized name

- [var localizedName: String?](/documentation/gamecontroller/gccontrollerelement/localizedname)
- [var unmappedLocalizedName: String?](/documentation/gamecontroller/gccontrollerelement/unmappedlocalizedname)

#### Displaying a symbol

- [var sfSymbolsName: String?](/documentation/gamecontroller/gccontrollerelement/sfsymbolsname)
- [var unmappedSfSymbolsName: String?](/documentation/gamecontroller/gccontrollerelement/unmappedsfsymbolsname)

#### Accessing elements by key

- [var aliases: Set<String>](/documentation/gamecontroller/gccontrollerelement/aliases)

#### Getting the containing element

- [var collection: GCControllerElement?](/documentation/gamecontroller/gccontrollerelement/collection)

#### Handling system gesture input

- [var isBoundToSystemGesture: Bool](/documentation/gamecontroller/gccontrollerelement/isboundtosystemgesture)
- [var preferredSystemGestureState: GCControllerElement.SystemGestureState](/documentation/gamecontroller/gccontrollerelement/preferredsystemgesturestate)
- [GCControllerElement.SystemGestureState](/documentation/gamecontroller/gccontrollerelement/systemgesturestate)

##### States

- [case enabled](/documentation/gamecontroller/gccontrollerelement/systemgesturestate/enabled)
- [case alwaysReceive](/documentation/gamecontroller/gccontrollerelement/systemgesturestate/alwaysreceive)
- [case disabled](/documentation/gamecontroller/gccontrollerelement/systemgesturestate/disabled)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gccontrollerelement/systemgesturestate/init(rawvalue:))
- [GCControllerAxisInput](/documentation/gamecontroller/gccontrolleraxisinput)

#### Accessing the input values

- [var value: Float](/documentation/gamecontroller/gccontrolleraxisinput/value)
- [func setValue(Float)](/documentation/gamecontroller/gccontrolleraxisinput/setvalue(_:))

#### Getting change information

- [var valueChangedHandler: GCControllerAxisValueChangedHandler?](/documentation/gamecontroller/gccontrolleraxisinput/valuechangedhandler)
- [GCControllerAxisValueChangedHandler](/documentation/gamecontroller/gccontrolleraxisvaluechangedhandler)
- [GCControllerButtonInput](/documentation/gamecontroller/gccontrollerbuttoninput)

#### Accessing input values

- [var isTouched: Bool](/documentation/gamecontroller/gccontrollerbuttoninput/istouched)
- [var isPressed: Bool](/documentation/gamecontroller/gccontrollerbuttoninput/ispressed)
- [var value: Float](/documentation/gamecontroller/gccontrollerbuttoninput/value)

#### Getting change information

- [var touchedChangedHandler: GCControllerButtonTouchedChangedHandler?](/documentation/gamecontroller/gccontrollerbuttoninput/touchedchangedhandler)
- [GCControllerButtonTouchedChangedHandler](/documentation/gamecontroller/gccontrollerbuttontouchedchangedhandler)
- [var pressedChangedHandler: GCControllerButtonValueChangedHandler?](/documentation/gamecontroller/gccontrollerbuttoninput/pressedchangedhandler)
- [var valueChangedHandler: GCControllerButtonValueChangedHandler?](/documentation/gamecontroller/gccontrollerbuttoninput/valuechangedhandler)
- [GCControllerButtonValueChangedHandler](/documentation/gamecontroller/gccontrollerbuttonvaluechangedhandler)

#### Setting snapshot values

- [func setValue(Float)](/documentation/gamecontroller/gccontrollerbuttoninput/setvalue(_:))
- [GCControllerTouchpad](/documentation/gamecontroller/gccontrollertouchpad)

#### Getting the subelements

- [var touchSurface: GCControllerDirectionPad](/documentation/gamecontroller/gccontrollertouchpad/touchsurface)
- [var button: GCControllerButtonInput](/documentation/gamecontroller/gccontrollertouchpad/button)

#### Accessing the input values

- [var touchState: GCControllerTouchpad.TouchState](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.property)
- [GCControllerTouchpad.TouchState](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.enum)

##### States

- [case up](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.enum/up)
- [case down](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.enum/down)
- [case moving](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.enum/moving)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gccontrollertouchpad/touchstate-swift.enum/init(rawvalue:))
- [var reportsAbsoluteTouchSurfaceValues: Bool](/documentation/gamecontroller/gccontrollertouchpad/reportsabsolutetouchsurfacevalues)

#### Getting change information

- [var touchDown: GCControllerTouchpadHandler?](/documentation/gamecontroller/gccontrollertouchpad/touchdown)
- [var touchMoved: GCControllerTouchpadHandler?](/documentation/gamecontroller/gccontrollertouchpad/touchmoved)
- [var touchUp: GCControllerTouchpadHandler?](/documentation/gamecontroller/gccontrollertouchpad/touchup)
- [GCControllerTouchpadHandler](/documentation/gamecontroller/gccontrollertouchpadhandler)

#### Setting snapshot values

- [func setValueForXAxis(Float, yAxis: Float, touchDown: Bool, buttonValue: Float)](/documentation/gamecontroller/gccontrollertouchpad/setvalueforxaxis(_:yaxis:touchdown:buttonvalue:))
- [GCControllerDirectionPad](/documentation/gamecontroller/gccontrollerdirectionpad)

#### Accessing values using the axes

- [var xAxis: GCControllerAxisInput](/documentation/gamecontroller/gccontrollerdirectionpad/xaxis)
- [var yAxis: GCControllerAxisInput](/documentation/gamecontroller/gccontrollerdirectionpad/yaxis)

#### Accessing values using directional buttons

- [var right: GCControllerButtonInput](/documentation/gamecontroller/gccontrollerdirectionpad/right)
- [var left: GCControllerButtonInput](/documentation/gamecontroller/gccontrollerdirectionpad/left)
- [var up: GCControllerButtonInput](/documentation/gamecontroller/gccontrollerdirectionpad/up)
- [var down: GCControllerButtonInput](/documentation/gamecontroller/gccontrollerdirectionpad/down)

#### Getting change information

- [var valueChangedHandler: GCControllerDirectionPadValueChangedHandler?](/documentation/gamecontroller/gccontrollerdirectionpad/valuechangedhandler)
- [GCControllerDirectionPadValueChangedHandler](/documentation/gamecontroller/gccontrollerdirectionpadvaluechangedhandler)

#### Setting snapshot values

- [func setValueForXAxis(Float, yAxis: Float)](/documentation/gamecontroller/gccontrollerdirectionpad/setvalueforxaxis(_:yaxis:))
- [GCDeviceCursor](/documentation/gamecontroller/gcdevicecursor)
- [GCDualSenseAdaptiveTrigger](/documentation/gamecontroller/gcdualsenseadaptivetrigger)

#### Getting the mode

- [var mode: GCDualSenseAdaptiveTrigger.Mode](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.property)
- [GCDualSenseAdaptiveTrigger.Mode](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum)

##### Modes

- [case off](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/off)
- [case feedback](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/feedback)
- [case weapon](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/weapon)
- [case vibration](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/vibration)
- [case slopeFeedback](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/slopefeedback)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/mode-swift.enum/init(rawvalue:))
- [func setModeOff()](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodeoff())

#### Configuring the trigger

- [func setModeFeedbackWithStartPosition(Float, resistiveStrength: Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodefeedbackwithstartposition(_:resistivestrength:))
- [GCDualSenseAdaptiveTrigger.PositionalResistiveStrengths](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalresistivestrengths)

##### Creating resistive strengths

- [init(values: (Float, Float, Float, Float, Float, Float, Float, Float, Float, Float))](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalresistivestrengths/init(values:))
- [init()](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalresistivestrengths/init())

##### Accessing resistive strengths

- [var values: (Float, Float, Float, Float, Float, Float, Float, Float, Float, Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalresistivestrengths/values)
- [func setModeFeedback(resistiveStrengths: GCDualSenseAdaptiveTrigger.PositionalResistiveStrengths)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodefeedback(resistivestrengths:))
- [func setModeWeaponWithStartPosition(Float, endPosition: Float, resistiveStrength: Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodeweaponwithstartposition(_:endposition:resistivestrength:))
- [func setModeVibrationWithStartPosition(Float, amplitude: Float, frequency: Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodevibrationwithstartposition(_:amplitude:frequency:))
- [func setModeVibration(amplitudes: GCDualSenseAdaptiveTrigger.PositionalAmplitudes, frequency: Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodevibration(amplitudes:frequency:))
- [GCDualSenseAdaptiveTrigger.PositionalAmplitudes](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalamplitudes)

##### Creating multiple amplitudes

- [init(values: (Float, Float, Float, Float, Float, Float, Float, Float, Float, Float))](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalamplitudes/init(values:))
- [init()](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalamplitudes/init())

##### Accessing multiple amplitudes

- [var values: (Float, Float, Float, Float, Float, Float, Float, Float, Float, Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/positionalamplitudes/values)
- [func setModeSlopeFeedback(startPosition: Float, endPosition: Float, startStrength: Float, endStrength: Float)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/setmodeslopefeedback(startposition:endposition:startstrength:endstrength:))

#### Getting the arm position

- [var armPosition: Float](/documentation/gamecontroller/gcdualsenseadaptivetrigger/armposition)
- [class var discretePositionCount: Int](/documentation/gamecontroller/gcdualsenseadaptivetrigger/discretepositioncount)

#### Checking the status

- [var status: GCDualSenseAdaptiveTrigger.Status](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.property)
- [GCDualSenseAdaptiveTrigger.Status](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum)

##### Statuses

- [case unknown](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/unknown)
- [case feedbackNoLoad](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/feedbacknoload)
- [case feedbackLoadApplied](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/feedbackloadapplied)
- [case weaponReady](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/weaponready)
- [case weaponFiring](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/weaponfiring)
- [case weaponFired](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/weaponfired)
- [case vibrationNotVibrating](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/vibrationnotvibrating)
- [case vibrationIsVibrating](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/vibrationisvibrating)
- [case slopeFeedbackReady](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/slopefeedbackready)
- [case slopeFeedbackApplyingLoad](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/slopefeedbackapplyingload)
- [case slopeFeedbackFinished](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/slopefeedbackfinished)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcdualsenseadaptivetrigger/status-swift.enum/init(rawvalue:))

### Identifying controllers and displaying a player index

- [var playerIndex: GCControllerPlayerIndex](/documentation/gamecontroller/gccontroller/playerindex)
- [GCControllerPlayerIndex](/documentation/gamecontroller/gccontrollerplayerindex)

#### Player indices

- [case indexUnset](/documentation/gamecontroller/gccontrollerplayerindex/indexunset)
- [case index1](/documentation/gamecontroller/gccontrollerplayerindex/index1)
- [case index2](/documentation/gamecontroller/gccontrollerplayerindex/index2)
- [case index3](/documentation/gamecontroller/gccontrollerplayerindex/index3)
- [case index4](/documentation/gamecontroller/gccontrollerplayerindex/index4)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gccontrollerplayerindex/init(rawvalue:))

### Accessing battery, haptics, and light objects

- [var battery: GCDeviceBattery?](/documentation/gamecontroller/gccontroller/battery)
- [var haptics: GCDeviceHaptics?](/documentation/gamecontroller/gccontroller/haptics)
- [var light: GCDeviceLight?](/documentation/gamecontroller/gccontroller/light)

### Creating snapshots

- [class func withExtendedGamepad() -> GCController](/documentation/gamecontroller/gccontroller/withextendedgamepad())
- [class func withMicroGamepad() -> GCController](/documentation/gamecontroller/gccontroller/withmicrogamepad())
- [func capture() -> GCController](/documentation/gamecontroller/gccontroller/capture())
- [var isSnapshot: Bool](/documentation/gamecontroller/gccontroller/issnapshot)

### Responding to a paused controller or controller event

- [var controllerPausedHandler: ((GCController) -> Void)?](/documentation/gamecontroller/gccontroller/controllerpausedhandler)
- [GCGameControllerSceneDelegate](/documentation/gamecontroller/gcgamecontrollerscenedelegate)

#### Instance Methods

- [func scene(UIScene, didActivateGameControllerWith: GCGameControllerActivationContext)](/documentation/gamecontroller/gcgamecontrollerscenedelegate/scene(_:didactivategamecontrollerwith:))
- [GCEventInteraction](/documentation/gamecontroller/gceventinteraction)

#### Creating an interaction

- [init()](/documentation/gamecontroller/gceventinteraction/init())

#### Receiving view events

- [var receivesEventsInView: Bool](/documentation/gamecontroller/gceventinteraction/receiveseventsinview)
- [GameControllerEventHandlingOptions](/documentation/gamecontroller/gamecontrollereventhandlingoptions)

##### Initializers

- [init()](/documentation/gamecontroller/gamecontrollereventhandlingoptions/init())

##### Type Methods

- [static func receivesEventsInView(Bool) -> GameControllerEventHandlingOptions](/documentation/gamecontroller/gamecontrollereventhandlingoptions/receiveseventsinview(_:))

#### Getting the event types

- [var handledEventTypes: GCUIEventTypes](/documentation/gamecontroller/gceventinteraction/handledeventtypes)
- [GCUIEventTypes](/documentation/gamecontroller/gcuieventtypes)

##### Initializers

- [init(rawValue: UInt)](/documentation/gamecontroller/gcuieventtypes/init(rawvalue:))

##### Type Properties

- [static var gamepad: GCUIEventTypes](/documentation/gamecontroller/gcuieventtypes/gamepad)
- [static var stylus: GCUIEventTypes](/documentation/gamecontroller/gcuieventtypes/stylus)

### Identifying the activation context

- [GCGameControllerActivationContext](/documentation/gamecontroller/gcgamecontrolleractivationcontext)

#### Instance Properties

- [var previousApplicationBundleID: String?](/documentation/gamecontroller/gcgamecontrolleractivationcontext/previousapplicationbundleid)

### Structures

- [GCController.DidBecomeCurrentMessage](/documentation/gamecontroller/gccontroller/didbecomecurrentmessage)

#### Initializers

- [init(controller: GCController)](/documentation/gamecontroller/gccontroller/didbecomecurrentmessage/init(controller:))

#### Instance Properties

- [var controller: GCController](/documentation/gamecontroller/gccontroller/didbecomecurrentmessage/controller)
- [GCController.DidConnectMessage](/documentation/gamecontroller/gccontroller/didconnectmessage)

#### Initializers

- [init(controller: GCController)](/documentation/gamecontroller/gccontroller/didconnectmessage/init(controller:))

#### Instance Properties

- [var controller: GCController](/documentation/gamecontroller/gccontroller/didconnectmessage/controller)
- [GCController.DidDisconnectMessage](/documentation/gamecontroller/gccontroller/diddisconnectmessage)

#### Initializers

- [init(controller: GCController)](/documentation/gamecontroller/gccontroller/diddisconnectmessage/init(controller:))

#### Instance Properties

- [var controller: GCController](/documentation/gamecontroller/gccontroller/diddisconnectmessage/controller)
- [GCController.DidStopBeingCurrentMessage](/documentation/gamecontroller/gccontroller/didstopbeingcurrentmessage)

#### Initializers

- [init(controller: GCController)](/documentation/gamecontroller/gccontroller/didstopbeingcurrentmessage/init(controller:))

#### Instance Properties

- [var controller: GCController](/documentation/gamecontroller/gccontroller/didstopbeingcurrentmessage/controller)
- [GCRacingWheel](/documentation/gamecontroller/gcracingwheel)

### Discovering racing wheels

- [class var connectedRacingWheels: Set<GCRacingWheel>](/documentation/gamecontroller/gcracingwheel/connectedracingwheels)
- [static let GCRacingWheelDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcracingwheeldidconnect)
- [static let GCRacingWheelDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcracingwheeldiddisconnect)

### Getting events

- [func acquireDevice() throws](/documentation/gamecontroller/gcracingwheel/acquiredevice())
- [func relinquishDevice()](/documentation/gamecontroller/gcracingwheel/relinquishdevice())
- [var isAcquired: Bool](/documentation/gamecontroller/gcracingwheel/isacquired)

### Accessing the controller profile

- [var wheelInput: GCRacingWheelInput](/documentation/gamecontroller/gcracingwheel/wheelinput)

### Creating snapshots

- [func capture() -> GCRacingWheel](/documentation/gamecontroller/gcracingwheel/capture())
- [var isSnapshot: Bool](/documentation/gamecontroller/gcracingwheel/issnapshot)

### Structures

- [GCRacingWheel.DidConnectMessage](/documentation/gamecontroller/gcracingwheel/didconnectmessage)

#### Initializers

- [init(racingWheel: GCRacingWheel)](/documentation/gamecontroller/gcracingwheel/didconnectmessage/init(racingwheel:))

#### Instance Properties

- [var racingWheel: GCRacingWheel](/documentation/gamecontroller/gcracingwheel/didconnectmessage/racingwheel)
- [GCRacingWheel.DidDisconnectMessage](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage)

#### Initializers

- [init(racingWheel: GCRacingWheel)](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage/init(racingwheel:))

#### Instance Properties

- [var racingWheel: GCRacingWheel](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage/racingwheel)
- [GCKeyboard](/documentation/gamecontroller/gckeyboard)

### Discovering keyboards

- [class var coalesced: GCKeyboard?](/documentation/gamecontroller/gckeyboard/coalesced)
- [static let GCKeyboardDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gckeyboarddidconnect)
- [static let GCKeyboardDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gckeyboarddiddisconnect)

### Getting input values

- [var keyboardInput: GCKeyboardInput?](/documentation/gamecontroller/gckeyboard/keyboardinput)

### Structures

- [GCKeyboard.DidConnectMessage](/documentation/gamecontroller/gckeyboard/didconnectmessage)

#### Initializers

- [init(keyboard: GCKeyboard)](/documentation/gamecontroller/gckeyboard/didconnectmessage/init(keyboard:))

#### Instance Properties

- [var keyboard: GCKeyboard](/documentation/gamecontroller/gckeyboard/didconnectmessage/keyboard)
- [GCKeyboard.DidDisconnectMessage](/documentation/gamecontroller/gckeyboard/diddisconnectmessage)

#### Initializers

- [init(keyboard: GCKeyboard)](/documentation/gamecontroller/gckeyboard/diddisconnectmessage/init(keyboard:))

#### Instance Properties

- [var keyboard: GCKeyboard](/documentation/gamecontroller/gckeyboard/diddisconnectmessage/keyboard)
- [GCMouse](/documentation/gamecontroller/gcmouse)

### Discovering mouse devices

- [class func mice() -> [GCMouse]](/documentation/gamecontroller/gcmouse/mice())
- [static let GCMouseDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcmousedidconnect)
- [static let GCMouseDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcmousediddisconnect)

### Handling multiple mouse devices

- [class var current: GCMouse?](/documentation/gamecontroller/gcmouse/current)
- [static let GCMouseDidBecomeCurrent: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcmousedidbecomecurrent)
- [static let GCMouseDidStopBeingCurrent: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcmousedidstopbeingcurrent)

### Getting input values

- [var mouseInput: GCMouseInput?](/documentation/gamecontroller/gcmouse/mouseinput)

### Structures

- [GCMouse.DidBecomeCurrentMessage](/documentation/gamecontroller/gcmouse/didbecomecurrentmessage)

#### Initializers

- [init(mouse: GCMouse)](/documentation/gamecontroller/gcmouse/didbecomecurrentmessage/init(mouse:))

#### Instance Properties

- [var mouse: GCMouse](/documentation/gamecontroller/gcmouse/didbecomecurrentmessage/mouse)
- [GCMouse.DidConnectMessage](/documentation/gamecontroller/gcmouse/didconnectmessage)

#### Initializers

- [init(mouse: GCMouse)](/documentation/gamecontroller/gcmouse/didconnectmessage/init(mouse:))

#### Instance Properties

- [var mouse: GCMouse](/documentation/gamecontroller/gcmouse/didconnectmessage/mouse)
- [GCMouse.DidDisconnectMessage](/documentation/gamecontroller/gcmouse/diddisconnectmessage)

#### Initializers

- [init(mouse: GCMouse)](/documentation/gamecontroller/gcmouse/diddisconnectmessage/init(mouse:))

#### Instance Properties

- [var mouse: GCMouse](/documentation/gamecontroller/gcmouse/diddisconnectmessage/mouse)
- [GCMouse.DidStopBeingCurrentMessage](/documentation/gamecontroller/gcmouse/didstopbeingcurrentmessage)

#### Initializers

- [init(mouse: GCMouse)](/documentation/gamecontroller/gcmouse/didstopbeingcurrentmessage/init(mouse:))

#### Instance Properties

- [var mouse: GCMouse](/documentation/gamecontroller/gcmouse/didstopbeingcurrentmessage/mouse)
- [GCStylus](/documentation/gamecontroller/gcstylus)

### Accessing the styli

- [class var styli: [GCStylus]](/documentation/gamecontroller/gcstylus/styli)

### Getting input values and haptics

- [var input: (any GCDevicePhysicalInput)?](/documentation/gamecontroller/gcstylus/input)
- [var haptics: GCDeviceHaptics?](/documentation/gamecontroller/gcstylus/haptics)

### Retrieving the buttons

- [var GCInputStylusPrimaryButton: String](/documentation/gamecontroller/gcinputstylusprimarybutton-18g2p)
- [var GCInputStylusSecondaryButton: String](/documentation/gamecontroller/gcinputstylussecondarybutton-6r3q)
- [var GCInputStylusTip: String](/documentation/gamecontroller/gcinputstylustip-1rhuw)

### Structures

- [GCStylus.DidConnectMessage](/documentation/gamecontroller/gcstylus/didconnectmessage)

#### Initializers

- [init(stylus: GCStylus)](/documentation/gamecontroller/gcstylus/didconnectmessage/init(stylus:))

#### Instance Properties

- [var stylus: GCStylus](/documentation/gamecontroller/gcstylus/didconnectmessage/stylus)
- [GCStylus.DidDisconnectMessage](/documentation/gamecontroller/gcstylus/diddisconnectmessage)

#### Initializers

- [init(stylus: GCStylus)](/documentation/gamecontroller/gcstylus/diddisconnectmessage/init(stylus:))

#### Instance Properties

- [var stylus: GCStylus](/documentation/gamecontroller/gcstylus/diddisconnectmessage/stylus)

## Game controller profiles

- [Input](/documentation/gamecontroller/input)

### Essentials

- [Handling input events](/documentation/gamecontroller/handling-input-events)
- [GCDevicePhysicalInput](/documentation/gamecontroller/gcdevicephysicalinput)

#### Getting the device

- [var device: (any GCDevice)?](/documentation/gamecontroller/gcdevicephysicalinput/device)

#### Handling device input

- [func nextInputState() -> (any GCDevicePhysicalInputState & GCDevicePhysicalInputStateDiff)?](/documentation/gamecontroller/gcdevicephysicalinput/nextinputstate())
- [var inputStateAvailableHandler: ((any GCDevicePhysicalInput) -> Void)?](/documentation/gamecontroller/gcdevicephysicalinput/inputstateavailablehandler)
- [var inputStateQueueDepth: Int](/documentation/gamecontroller/gcdevicephysicalinput/inputstatequeuedepth)
- [func capture() -> any GCDevicePhysicalInputState](/documentation/gamecontroller/gcdevicephysicalinput/capture())
- [var elementValueDidChangeHandler: ((any GCDevicePhysicalInput, any GCPhysicalInputElement) -> Void)?](/documentation/gamecontroller/gcdevicephysicalinput/elementvaluedidchangehandler)

#### Changing the callback dispatch queue

- [var queue: dispatch_queue_t?](/documentation/gamecontroller/gcdevicephysicalinput/queue)
- [GCDevicePhysicalInputState](/documentation/gamecontroller/gcdevicephysicalinputstate)

#### Getting the device

- [var device: (any GCDevice)?](/documentation/gamecontroller/gcdevicephysicalinputstate/device)

#### Getting change information

- [var lastEventTimestamp: TimeInterval](/documentation/gamecontroller/gcdevicephysicalinputstate/lasteventtimestamp)
- [var lastEventLatency: TimeInterval](/documentation/gamecontroller/gcdevicephysicalinputstate/lasteventlatency)

#### Accessing elements

- [var elements: GCPhysicalInputElementCollection<any GCPhysicalInputElement>](/documentation/gamecontroller/gcdevicephysicalinputstate/elements-46hgy)
- [var axes: GCPhysicalInputElementCollection<any GCAxisElement>](/documentation/gamecontroller/gcdevicephysicalinputstate/axes-5u1xr)
- [var buttons: GCPhysicalInputElementCollection<any GCButtonElement>](/documentation/gamecontroller/gcdevicephysicalinputstate/buttons-2ovae)
- [var dpads: GCPhysicalInputElementCollection<any GCDirectionPadElement>](/documentation/gamecontroller/gcdevicephysicalinputstate/dpads-7b4o3)
- [var switches: GCPhysicalInputElementCollection<any GCSwitchElement>](/documentation/gamecontroller/gcdevicephysicalinputstate/switches-6dcny)
- [subscript(String) -> (any GCPhysicalInputElement)?](/documentation/gamecontroller/gcdevicephysicalinputstate/subscript(_:))
- [GCDevicePhysicalInputStateDiff](/documentation/gamecontroller/gcdevicephysicalinputstatediff)

#### Getting changes

- [func change(for: any GCPhysicalInputElement) -> GCDevicePhysicalInputElementChange](/documentation/gamecontroller/gcdevicephysicalinputstatediff/change(for:))
- [GCDevicePhysicalInputElementChange](/documentation/gamecontroller/gcdevicephysicalinputelementchange)

##### States

- [case unknownChange](/documentation/gamecontroller/gcdevicephysicalinputelementchange/unknownchange)
- [case noChange](/documentation/gamecontroller/gcdevicephysicalinputelementchange/nochange)
- [case changed](/documentation/gamecontroller/gcdevicephysicalinputelementchange/changed)

##### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcdevicephysicalinputelementchange/init(rawvalue:))
- [func changedElements() -> NSEnumerator?](/documentation/gamecontroller/gcdevicephysicalinputstatediff/changedelements()-9cdq4)
- [func changedElements() -> (some Sequence<any GCPhysicalInputElement>)?
](/documentation/gamecontroller/gcdevicephysicalinputstatediff/changedelements()-2zzwm)

### Elements

- [GCPhysicalInputElementCollection](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct)

#### Accessing elements by name

- [subscript(GCDirectionPadElementName) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-1twjd)
- [subscript(GCAxisElementName) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-8m218)
- [subscript(GCButtonElementName) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-3l6nj)
- [subscript(GCSwitchElementName) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-4oje0)
- [subscript(GCPhysicalInputElementName) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-85c13)

#### Subscripts

- [subscript(String) -> T?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-3tv91)
- [subscript<Name>(Name) -> Name.PhysicalInputElement?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-3womp)
- [subscript<Name>(Name) -> (any GCPhysicalInputElement)?](/documentation/gamecontroller/gcphysicalinputelementcollection-swift.struct/subscript(_:)-c5v9)
- [GCPhysicalInputElement](/documentation/gamecontroller/gcphysicalinputelement)

#### Getting a localized name

- [var localizedName: String?](/documentation/gamecontroller/gcphysicalinputelement/localizedname)

#### Displaying a symbol

- [var sfSymbolsName: String?](/documentation/gamecontroller/gcphysicalinputelement/sfsymbolsname)

#### Accessing elements by key

- [var aliases: Set<String>](/documentation/gamecontroller/gcphysicalinputelement/aliases)
- [GCButtonElement](/documentation/gamecontroller/gcbuttonelement)

#### Getting input state

- [var touchedInput: (any GCTouchedStateInput)?](/documentation/gamecontroller/gcbuttonelement/touchedinput)
- [var pressedInput: any GCLinearInput & GCPressedStateInput](/documentation/gamecontroller/gcbuttonelement/pressedinput)

#### Instance Properties

- [var forceInput: (any GCLinearInput)?](/documentation/gamecontroller/gcbuttonelement/forceinput)
- [GCAxisElement](/documentation/gamecontroller/gcaxiselement)

#### Getting the inputs

- [var absoluteInput: (any GCAxisInput)?](/documentation/gamecontroller/gcaxiselement/absoluteinput)
- [var relativeInput: any GCRelativeInput](/documentation/gamecontroller/gcaxiselement/relativeinput)
- [GCSwitchElement](/documentation/gamecontroller/gcswitchelement)

#### Getting input state

- [var positionInput: any GCSwitchPositionInput](/documentation/gamecontroller/gcswitchelement/positioninput)
- [GCDirectionPadElement](/documentation/gamecontroller/gcdirectionpadelement)

#### Directional buttons

- [var left: any GCLinearInput & GCPressedStateInput](/documentation/gamecontroller/gcdirectionpadelement/left)
- [var right: any GCLinearInput & GCPressedStateInput](/documentation/gamecontroller/gcdirectionpadelement/right)
- [var up: any GCLinearInput & GCPressedStateInput](/documentation/gamecontroller/gcdirectionpadelement/up)
- [var down: any GCLinearInput & GCPressedStateInput](/documentation/gamecontroller/gcdirectionpadelement/down)

#### Axes

- [var xAxis: any GCAxisInput](/documentation/gamecontroller/gcdirectionpadelement/xaxis)
- [var yAxis: any GCAxisInput](/documentation/gamecontroller/gcdirectionpadelement/yaxis)
- [var xyAxes: any GCAxis2DInput](/documentation/gamecontroller/gcdirectionpadelement/xyaxes)
- [GCAxis2DInput](/documentation/gamecontroller/gcaxis2dinput)

##### Getting the characteristics

- [var canWrap: Bool](/documentation/gamecontroller/gcaxis2dinput/canwrap)
- [var isAnalog: Bool](/documentation/gamecontroller/gcaxis2dinput/isanalog)

##### Getting the value

- [var value: GCPoint2](/documentation/gamecontroller/gcaxis2dinput/value)
- [GCPoint2](/documentation/gamecontroller/gcpoint2)

###### Creating a point

- [init()](/documentation/gamecontroller/gcpoint2/init())
- [init(x: Float, y: Float)](/documentation/gamecontroller/gcpoint2/init(x:y:))
- [func GCPoint2Make(Float, Float) -> GCPoint2](/documentation/gamecontroller/gcpoint2make(_:_:))
- [let GCPoint2Zero: GCPoint2](/documentation/gamecontroller/gcpoint2zero)

###### Accessing coordinates

- [var x: Float](/documentation/gamecontroller/gcpoint2/x)
- [var y: Float](/documentation/gamecontroller/gcpoint2/y)

###### Comparing and converting points

- [func GCPoint2Equal(GCPoint2, GCPoint2) -> Bool](/documentation/gamecontroller/gcpoint2equal(_:_:))
- [func NSStringFromGCPoint2(GCPoint2) -> String](/documentation/gamecontroller/nsstringfromgcpoint2(_:))
- [var valueDidChangeHandler: ((any GCPhysicalInputElement, any GCAxis2DInput, GCPoint2) -> Void)?](/documentation/gamecontroller/gcaxis2dinput/valuedidchangehandler)
- [var lastValueTimestamp: TimeInterval](/documentation/gamecontroller/gcaxis2dinput/lastvaluetimestamp)
- [var lastValueLatency: TimeInterval](/documentation/gamecontroller/gcaxis2dinput/lastvaluelatency)

##### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gcaxis2dinput/sources)

### Element inputs

- [GCPhysicalInputSource](/documentation/gamecontroller/gcphysicalinputsource)

#### Getting a localized name

- [var elementLocalizedName: String?](/documentation/gamecontroller/gcphysicalinputsource/elementlocalizedname)

#### Displaying a symbol

- [var sfSymbolsName: String?](/documentation/gamecontroller/gcphysicalinputsource/sfsymbolsname)

#### Accessing elements by key

- [var elementAliases: Set<String>](/documentation/gamecontroller/gcphysicalinputsource/elementaliases)

#### Getting directions

- [var direction: GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsource/direction)
- [GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsourcedirection)

##### Directions

- [static var up: GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsourcedirection/up)
- [static var right: GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsourcedirection/right)
- [static var down: GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsourcedirection/down)
- [static var left: GCPhysicalInputSourceDirection](/documentation/gamecontroller/gcphysicalinputsourcedirection/left)

##### Creating the supported directions

- [init(rawValue: UInt)](/documentation/gamecontroller/gcphysicalinputsourcedirection/init(rawvalue:))

### Element names

- [GCPhysicalInputElementName](/documentation/gamecontroller/gcphysicalinputelementname-swift.struct)

#### Racing wheel element names

- [static let shifter: GCPhysicalInputElementName](/documentation/gamecontroller/gcphysicalinputelementname-swift.struct/shifter)
- [GCPhysicalInputElementTypedName](/documentation/gamecontroller/gcphysicalinputelementtypedname)

#### Associated type

- [PhysicalInputElement](/documentation/gamecontroller/gcphysicalinputelementtypedname/physicalinputelement)
- [GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct)

#### Getting extended gamepad shoulder button names

- [static let leftShoulder: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/leftshoulder)
- [static let rightShoulder: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/rightshoulder)
- [static let leftBumper: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/leftbumper)
- [static let rightBumper: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/rightbumper)

#### Getting extended gamepad trigger names

- [static let leftTrigger: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/lefttrigger)
- [static let rightTrigger: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/righttrigger)

#### Getting extended gamepad face button names

- [static let menu: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/menu)
- [static let options: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/options)
- [static let home: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/home)
- [static let a: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/a)
- [static let b: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/b)
- [static let x: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/x)
- [static let y: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/y)

#### Getting extended gamepad thumbstick names

- [static let leftThumbstickButton: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/leftthumbstickbutton)
- [static let rightThumbstickButton: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/rightthumbstickbutton)

#### Getting extended gamepad back button names

- [static func backLeftButton(position: Int) -> GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/backleftbutton(position:))
- [static func backRightButton(position: Int) -> GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/backrightbutton(position:))

#### Getting steering wheel controller names

- [static let pedalClutch: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/pedalclutch)
- [static let pedalBrake: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/pedalbrake)
- [static let pedalAccelerator: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/pedalaccelerator)
- [static let leftPaddle: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/leftpaddle)
- [static let rightPaddle: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/rightpaddle)

#### Getting Xbox button names

- [static let share: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/share)

#### Getting arcade stick button names

- [static func arcadeButton(row: Int, column: Int) -> GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/arcadebutton(row:column:))

#### Type Properties

- [static let grip: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/grip)
- [static let stylusPrimaryButton: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/stylusprimarybutton)
- [static let stylusSecondaryButton: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/stylussecondarybutton)
- [static let stylusTip: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/stylustip)
- [static let thumbstickButton: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/thumbstickbutton)
- [static let trigger: GCButtonElementName](/documentation/gamecontroller/gcbuttonelementname-swift.struct/trigger)
- [GCAxisElementName](/documentation/gamecontroller/gcaxiselementname-swift.struct)

#### Getting the steering wheel name

- [static let steeringWheel: GCAxisElementName](/documentation/gamecontroller/gcaxiselementname-swift.struct/steeringwheel)
- [GCSwitchElementName](/documentation/gamecontroller/gcswitchelementname-swift.struct)
- [GCDirectionPadElementName](/documentation/gamecontroller/gcdirectionpadelementname-swift.struct)

#### Getting the directional pad component names

- [static let directionPad: GCDirectionPadElementName](/documentation/gamecontroller/gcdirectionpadelementname-swift.struct/directionpad)
- [static let leftThumbstick: GCDirectionPadElementName](/documentation/gamecontroller/gcdirectionpadelementname-swift.struct/leftthumbstick)
- [static let rightThumbstick: GCDirectionPadElementName](/documentation/gamecontroller/gcdirectionpadelementname-swift.struct/rightthumbstick)

#### Type Properties

- [static let thumbstick: GCDirectionPadElementName](/documentation/gamecontroller/gcdirectionpadelementname-swift.struct/thumbstick)
- [Extended gamepad input names](/documentation/gamecontroller/extended-gamepad-input-names)

#### Shoulder button names

- [var GCInputLeftShoulder: String](/documentation/gamecontroller/gcinputleftshoulder-9assr)
- [var GCInputRightShoulder: String](/documentation/gamecontroller/gcinputrightshoulder-5lcq1)

#### Trigger names

- [var GCInputLeftTrigger: String](/documentation/gamecontroller/gcinputlefttrigger-80png)
- [var GCInputRightTrigger: String](/documentation/gamecontroller/gcinputrighttrigger-96vtj)

#### Face button names

- [var GCInputButtonMenu: String](/documentation/gamecontroller/gcinputbuttonmenu-196mn)
- [var GCInputButtonHome: String](/documentation/gamecontroller/gcinputbuttonhome-7xxwm)
- [var GCInputButtonOptions: String](/documentation/gamecontroller/gcinputbuttonoptions-84kj)
- [var GCInputButtonA: String](/documentation/gamecontroller/gcinputbuttona-8z15w)
- [var GCInputButtonB: String](/documentation/gamecontroller/gcinputbuttonb-6z361)
- [var GCInputButtonX: String](/documentation/gamecontroller/gcinputbuttonx-32i2z)
- [var GCInputButtonY: String](/documentation/gamecontroller/gcinputbuttony-9x9i9)

#### Directional pad names

- [var GCInputDirectionPad: String](/documentation/gamecontroller/gcinputdirectionpad-115st)

#### Thumbstick names

- [var GCInputLeftThumbstick: String](/documentation/gamecontroller/gcinputleftthumbstick-3hlff)
- [var GCInputRightThumbstick: String](/documentation/gamecontroller/gcinputrightthumbstick-8469p)
- [var GCInputLeftThumbstickButton: String](/documentation/gamecontroller/gcinputleftthumbstickbutton-7gej3)
- [var GCInputRightThumbstickButton: String](/documentation/gamecontroller/gcinputrightthumbstickbutton-4to77)
- [DualShock controller input names](/documentation/gamecontroller/dualshock-controller-input-names)

#### DualShock controller button names

- [var GCInputDualShockTouchpadButton: String](/documentation/gamecontroller/gcinputdualshocktouchpadbutton-74k1l)
- [var GCInputDualShockTouchpadOne: String](/documentation/gamecontroller/gcinputdualshocktouchpadone-55wgz)
- [var GCInputDualShockTouchpadTwo: String](/documentation/gamecontroller/gcinputdualshocktouchpadtwo-5f8r9)
- [Xbox controller input names](/documentation/gamecontroller/xbox-controller-input-names)

#### Xbox controller button names

- [var GCInputButtonShare: String](/documentation/gamecontroller/gcinputbuttonshare-87tha)
- [var GCInputXboxPaddleOne: String](/documentation/gamecontroller/gcinputxboxpaddleone-offv)
- [var GCInputXboxPaddleTwo: String](/documentation/gamecontroller/gcinputxboxpaddletwo-4ya43)
- [var GCInputXboxPaddleThree: String](/documentation/gamecontroller/gcinputxboxpaddlethree-6zcw8)
- [var GCInputXboxPaddleFour: String](/documentation/gamecontroller/gcinputxboxpaddlefour-1obrw)
- [Micro gamepad input names](/documentation/gamecontroller/micro-gamepad-input-names)

#### Micro gamepad directional pad name

- [let GCInputMicroGamepadDpad: String](/documentation/gamecontroller/gcinputmicrogamepaddpad)

#### Micro gamepad button names

- [let GCInputMicroGamepadButtonA: String](/documentation/gamecontroller/gcinputmicrogamepadbuttona)
- [let GCInputMicroGamepadButtonX: String](/documentation/gamecontroller/gcinputmicrogamepadbuttonx)
- [let GCInputMicroGamepadButtonMenu: String](/documentation/gamecontroller/gcinputmicrogamepadbuttonmenu)
- [Directional Gamepad Input Names](/documentation/gamecontroller/directional-gamepad-input-names)

#### Directional Pad Names

- [let GCInputDirectionalDpad: String](/documentation/gamecontroller/gcinputdirectionaldpad)
- [let GCInputDirectionalCardinalDpad: String](/documentation/gamecontroller/gcinputdirectionalcardinaldpad)

#### Directional Pad Button Names

- [let GCInputDirectionalTouchSurfaceButton: String](/documentation/gamecontroller/gcinputdirectionaltouchsurfacebutton)
- [let GCInputDirectionalCenterButton: String](/documentation/gamecontroller/gcinputdirectionalcenterbutton)
- [GCMotion](/documentation/gamecontroller/gcmotion)

### Getting the Controller

- [var controller: GCController?](/documentation/gamecontroller/gcmotion/controller)

### Receiving a Callback When Input Values Change

- [var valueChangedHandler: GCMotionValueChangedHandler?](/documentation/gamecontroller/gcmotion/valuechangedhandler)
- [GCMotionValueChangedHandler](/documentation/gamecontroller/gcmotionvaluechangedhandler)

### Verifying Capabilities

- [var hasAttitude: Bool](/documentation/gamecontroller/gcmotion/hasattitude)
- [var hasRotationRate: Bool](/documentation/gamecontroller/gcmotion/hasrotationrate)
- [var hasGravityAndUserAcceleration: Bool](/documentation/gamecontroller/gcmotion/hasgravityanduseracceleration)
- [var hasAttitudeAndRotationRate: Bool](/documentation/gamecontroller/gcmotion/hasattitudeandrotationrate)

### Accessing Attitude and Rotation Data

- [var attitude: GCQuaternion](/documentation/gamecontroller/gcmotion/attitude)
- [GCQuaternion](/documentation/gamecontroller/gcquaternion)

#### Getting Quaternion Values

- [var x: Double](/documentation/gamecontroller/gcquaternion/x)
- [var y: Double](/documentation/gamecontroller/gcquaternion/y)
- [var z: Double](/documentation/gamecontroller/gcquaternion/z)
- [var w: Double](/documentation/gamecontroller/gcquaternion/w)

#### Initializers

- [init()](/documentation/gamecontroller/gcquaternion/init())
- [init(x: Double, y: Double, z: Double, w: Double)](/documentation/gamecontroller/gcquaternion/init(x:y:z:w:))
- [var rotationRate: GCRotationRate](/documentation/gamecontroller/gcmotion/rotationrate)
- [GCRotationRate](/documentation/gamecontroller/gcrotationrate)

#### Getting Rotation Rate Values

- [var x: Double](/documentation/gamecontroller/gcrotationrate/x)
- [var y: Double](/documentation/gamecontroller/gcrotationrate/y)
- [var z: Double](/documentation/gamecontroller/gcrotationrate/z)

#### Initializers

- [init()](/documentation/gamecontroller/gcrotationrate/init())
- [init(x: Double, y: Double, z: Double)](/documentation/gamecontroller/gcrotationrate/init(x:y:z:))
- [GCEulerAngles](/documentation/gamecontroller/gceulerangles)

#### Getting Euler Angle Values

- [var pitch: Double](/documentation/gamecontroller/gceulerangles/pitch)
- [var yaw: Double](/documentation/gamecontroller/gceulerangles/yaw)
- [var roll: Double](/documentation/gamecontroller/gceulerangles/roll)

#### Initializers

- [init()](/documentation/gamecontroller/gceulerangles/init())
- [init(pitch: Double, yaw: Double, roll: Double)](/documentation/gamecontroller/gceulerangles/init(pitch:yaw:roll:))

### Accessing Gravity and Acceleration Data

- [var acceleration: GCAcceleration](/documentation/gamecontroller/gcmotion/acceleration)
- [var gravity: GCAcceleration](/documentation/gamecontroller/gcmotion/gravity)
- [var userAcceleration: GCAcceleration](/documentation/gamecontroller/gcmotion/useracceleration)
- [GCAcceleration](/documentation/gamecontroller/gcacceleration)

#### Getting Acceleration Values

- [var x: Double](/documentation/gamecontroller/gcacceleration/x)
- [var y: Double](/documentation/gamecontroller/gcacceleration/y)
- [var z: Double](/documentation/gamecontroller/gcacceleration/z)

#### Initializers

- [init()](/documentation/gamecontroller/gcacceleration/init())
- [init(x: Double, y: Double, z: Double)](/documentation/gamecontroller/gcacceleration/init(x:y:z:))

### Accessing Sensor Data

- [var sensorsRequireManualActivation: Bool](/documentation/gamecontroller/gcmotion/sensorsrequiremanualactivation)
- [var sensorsActive: Bool](/documentation/gamecontroller/gcmotion/sensorsactive)

### Setting Snapshot Values

- [func setStateFrom(GCMotion)](/documentation/gamecontroller/gcmotion/setstatefrom(_:))
- [func setAttitude(GCQuaternion)](/documentation/gamecontroller/gcmotion/setattitude(_:))
- [func setRotationRate(GCRotationRate)](/documentation/gamecontroller/gcmotion/setrotationrate(_:))
- [func setAcceleration(GCAcceleration)](/documentation/gamecontroller/gcmotion/setacceleration(_:))
- [func setGravity(GCAcceleration)](/documentation/gamecontroller/gcmotion/setgravity(_:))
- [func setUserAcceleration(GCAcceleration)](/documentation/gamecontroller/gcmotion/setuseracceleration(_:))
- [GCDeviceBattery](/documentation/gamecontroller/gcdevicebattery)

### Getting the battery level and state

- [var batteryLevel: Float](/documentation/gamecontroller/gcdevicebattery/batterylevel)
- [var batteryState: GCDeviceBattery.State](/documentation/gamecontroller/gcdevicebattery/batterystate)
- [GCDeviceBattery.State](/documentation/gamecontroller/gcdevicebattery/state)

#### States

- [case unknown](/documentation/gamecontroller/gcdevicebattery/state/unknown)
- [case discharging](/documentation/gamecontroller/gcdevicebattery/state/discharging)
- [case charging](/documentation/gamecontroller/gcdevicebattery/state/charging)
- [case full](/documentation/gamecontroller/gcdevicebattery/state/full)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcdevicebattery/state/init(rawvalue:))
- [GCDeviceHaptics](/documentation/gamecontroller/gcdevicehaptics)

### Creating a haptics engine

- [func createEngine(withLocality: GCHapticsLocality) -> CHHapticEngine?](/documentation/gamecontroller/gcdevicehaptics/createengine(withlocality:))
- [let GCHapticDurationInfinite: Float](/documentation/gamecontroller/gchapticdurationinfinite)

### Getting the localities

- [var supportedLocalities: Set<GCHapticsLocality>](/documentation/gamecontroller/gcdevicehaptics/supportedlocalities)
- [GCHapticsLocality](/documentation/gamecontroller/gchapticslocality)

#### Localities

- [static let `default`: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/default)
- [static let all: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/all)
- [static let handles: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/handles)
- [static let leftHandle: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/lefthandle)
- [static let rightHandle: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/righthandle)
- [static let triggers: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/triggers)
- [static let leftTrigger: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/lefttrigger)
- [static let rightTrigger: GCHapticsLocality](/documentation/gamecontroller/gchapticslocality/righttrigger)

#### Initializers

- [init(rawValue: String)](/documentation/gamecontroller/gchapticslocality/init(rawvalue:))
- [GCDeviceLight](/documentation/gamecontroller/gcdevicelight)

### Getting the light’s color

- [var color: GCColor](/documentation/gamecontroller/gcdevicelight/color)
- [GCColor](/documentation/gamecontroller/gccolor)

#### Creating colors

- [init(red: Float, green: Float, blue: Float)](/documentation/gamecontroller/gccolor/init(red:green:blue:))

#### Setting color values

- [var red: Float](/documentation/gamecontroller/gccolor/red)
- [var green: Float](/documentation/gamecontroller/gccolor/green)
- [var blue: Float](/documentation/gamecontroller/gccolor/blue)

## Touch controller

- [Adding touch controls to games that support game controllers in iOS](/documentation/gamecontroller/adding-touch-controls-to-games-that-support-game-controllers-in-ios)
- [GCVirtualController](/documentation/gamecontroller/gcvirtualcontroller)

### Creating virtual controllers

- [init(configuration: GCVirtualController.Configuration)](/documentation/gamecontroller/gcvirtualcontroller/init(configuration:))
- [GCVirtualController.Configuration](/documentation/gamecontroller/gcvirtualcontroller/configuration)

#### Setting the elements

- [var elements: Set<String>](/documentation/gamecontroller/gcvirtualcontroller/configuration/elements)

#### Presenting a custom interface

- [var isHidden: Bool](/documentation/gamecontroller/gcvirtualcontroller/configuration/ishidden)

### Customizing the elements

- [func updateConfiguration(forElement: String, configuration: (GCVirtualController.ElementConfiguration) -> GCVirtualController.ElementConfiguration)](/documentation/gamecontroller/gcvirtualcontroller/updateconfiguration(forelement:configuration:))
- [GCVirtualController.ElementConfiguration](/documentation/gamecontroller/gcvirtualcontroller/elementconfiguration)

#### Configuring elements

- [var path: UIBezierPath?](/documentation/gamecontroller/gcvirtualcontroller/elementconfiguration/path)
- [var isHidden: Bool](/documentation/gamecontroller/gcvirtualcontroller/elementconfiguration/ishidden)
- [var actsAsTouchpad: Bool](/documentation/gamecontroller/gcvirtualcontroller/elementconfiguration/actsastouchpad)

### Accessing the elements

- [var controller: GCController?](/documentation/gamecontroller/gcvirtualcontroller/controller)

### Connecting and displaying virtual controllers

- [func connect(replyHandler: (((any Error)?) -> Void)?)](/documentation/gamecontroller/gcvirtualcontroller/connect(replyhandler:))
- [func disconnect()](/documentation/gamecontroller/gcvirtualcontroller/disconnect())

### Presenting a custom interface

- [func setPosition(CGPoint, forDirectionPadElement: String)](/documentation/gamecontroller/gcvirtualcontroller/setposition(_:fordirectionpadelement:))
- [func setValue(CGFloat, forButtonElement: String)](/documentation/gamecontroller/gcvirtualcontroller/setvalue(_:forbuttonelement:))

## Button elements and names

- [GCTouchedStateInput](/documentation/gamecontroller/gctouchedstateinput)

### Getting change information

- [var isTouched: Bool](/documentation/gamecontroller/gctouchedstateinput/istouched)
- [var lastTouchedStateTimestamp: TimeInterval](/documentation/gamecontroller/gctouchedstateinput/lasttouchedstatetimestamp)
- [var lastTouchedStateLatency: TimeInterval](/documentation/gamecontroller/gctouchedstateinput/lasttouchedstatelatency)
- [var touchedDidChangeHandler: ((any GCPhysicalInputElement, any GCTouchedStateInput, Bool) -> Void)?](/documentation/gamecontroller/gctouchedstateinput/toucheddidchangehandler)

### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gctouchedstateinput/sources)
- [GCPressedStateInput](/documentation/gamecontroller/gcpressedstateinput)

### Getting change information

- [var isPressed: Bool](/documentation/gamecontroller/gcpressedstateinput/ispressed)
- [var lastPressedStateTimestamp: TimeInterval](/documentation/gamecontroller/gcpressedstateinput/lastpressedstatetimestamp)
- [var lastPressedStateLatency: TimeInterval](/documentation/gamecontroller/gcpressedstateinput/lastpressedstatelatency)
- [var pressedDidChangeHandler: ((any GCPhysicalInputElement, any GCPressedStateInput, Bool) -> Void)?](/documentation/gamecontroller/gcpressedstateinput/presseddidchangehandler)

### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gcpressedstateinput/sources)

## Racing wheels

- [Racing wheel device support](/documentation/gamecontroller/racing-wheel-device-support)

### Racing wheel controller

- [GCRacingWheel](/documentation/gamecontroller/gcracingwheel)

#### Discovering racing wheels

- [class var connectedRacingWheels: Set<GCRacingWheel>](/documentation/gamecontroller/gcracingwheel/connectedracingwheels)
- [static let GCRacingWheelDidConnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcracingwheeldidconnect)
- [static let GCRacingWheelDidDisconnect: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/gcracingwheeldiddisconnect)

#### Getting events

- [func acquireDevice() throws](/documentation/gamecontroller/gcracingwheel/acquiredevice())
- [func relinquishDevice()](/documentation/gamecontroller/gcracingwheel/relinquishdevice())
- [var isAcquired: Bool](/documentation/gamecontroller/gcracingwheel/isacquired)

#### Accessing the controller profile

- [var wheelInput: GCRacingWheelInput](/documentation/gamecontroller/gcracingwheel/wheelinput)

#### Creating snapshots

- [func capture() -> GCRacingWheel](/documentation/gamecontroller/gcracingwheel/capture())
- [var isSnapshot: Bool](/documentation/gamecontroller/gcracingwheel/issnapshot)

#### Structures

- [GCRacingWheel.DidConnectMessage](/documentation/gamecontroller/gcracingwheel/didconnectmessage)

##### Initializers

- [init(racingWheel: GCRacingWheel)](/documentation/gamecontroller/gcracingwheel/didconnectmessage/init(racingwheel:))

##### Instance Properties

- [var racingWheel: GCRacingWheel](/documentation/gamecontroller/gcracingwheel/didconnectmessage/racingwheel)
- [GCRacingWheel.DidDisconnectMessage](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage)

##### Initializers

- [init(racingWheel: GCRacingWheel)](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage/init(racingwheel:))

##### Instance Properties

- [var racingWheel: GCRacingWheel](/documentation/gamecontroller/gcracingwheel/diddisconnectmessage/racingwheel)

### Racing wheel input

- [GCRacingWheelInput](/documentation/gamecontroller/gcracingwheelinput)

#### Creating snapshots

- [func capture() -> GCRacingWheelInputState](/documentation/gamecontroller/gcracingwheelinput/capture())

#### Polling for input

- [func nextInputState() -> (any GCRacingWheelInputState & GCDevicePhysicalInputStateDiff)?](/documentation/gamecontroller/gcracingwheelinput/nextinputstate())
- [GCRacingWheelInputState](/documentation/gamecontroller/gcracingwheelinputstate)

#### Getting input elements

- [var wheel: GCSteeringWheelElement](/documentation/gamecontroller/gcracingwheelinputstate/wheel)
- [var acceleratorPedal: (any GCButtonElement)?](/documentation/gamecontroller/gcracingwheelinputstate/acceleratorpedal)
- [var brakePedal: (any GCButtonElement)?](/documentation/gamecontroller/gcracingwheelinputstate/brakepedal)
- [var clutchPedal: (any GCButtonElement)?](/documentation/gamecontroller/gcracingwheelinputstate/clutchpedal)
- [var shifter: GCGearShifterElement?](/documentation/gamecontroller/gcracingwheelinputstate/shifter)

#### Accessing elements by name

- [var GCInputSteeringWheel: String](/documentation/gamecontroller/gcinputsteeringwheel-26283)
- [var GCInputShifter: String](/documentation/gamecontroller/gcinputshifter-6miga)
- [var GCInputPedalClutch: String](/documentation/gamecontroller/gcinputpedalclutch-82gwe)
- [var GCInputPedalAccelerator: String](/documentation/gamecontroller/gcinputpedalaccelerator-6kg6u)
- [var GCInputPedalBrake: String](/documentation/gamecontroller/gcinputpedalbrake-6wpdc)

### Left and right paddles

- [var GCInputLeftPaddle: String](/documentation/gamecontroller/gcinputleftpaddle-77y86)
- [var GCInputRightPaddle: String](/documentation/gamecontroller/gcinputrightpaddle-5klic)

### Gear shifter elements

- [GCAxisInput](/documentation/gamecontroller/gcaxisinput)

#### Getting the characteristics

- [var canWrap: Bool](/documentation/gamecontroller/gcaxisinput/canwrap)
- [var isAnalog: Bool](/documentation/gamecontroller/gcaxisinput/isanalog)

#### Getting the value

- [var value: Float](/documentation/gamecontroller/gcaxisinput/value)
- [var valueDidChangeHandler: ((any GCPhysicalInputElement, any GCAxisInput, Float) -> Void)?](/documentation/gamecontroller/gcaxisinput/valuedidchangehandler)
- [var lastValueTimestamp: TimeInterval](/documentation/gamecontroller/gcaxisinput/lastvaluetimestamp)
- [var lastValueLatency: TimeInterval](/documentation/gamecontroller/gcaxisinput/lastvaluelatency)

#### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gcaxisinput/sources)
- [GCGearShifterElement](/documentation/gamecontroller/gcgearshifterelement)

#### Accessing input values

- [var patternInput: (any GCSwitchPositionInput)?](/documentation/gamecontroller/gcgearshifterelement/patterninput)
- [var sequentialInput: (any GCRelativeInput)?](/documentation/gamecontroller/gcgearshifterelement/sequentialinput)
- [GCRelativeInput](/documentation/gamecontroller/gcrelativeinput)

#### Getting the characteristics

- [var isAnalog: Bool](/documentation/gamecontroller/gcrelativeinput/isanalog)

#### Getting the delta value and timestamp

- [var delta: Float](/documentation/gamecontroller/gcrelativeinput/delta)
- [var deltaDidChangeHandler: ((any GCPhysicalInputElement, any GCRelativeInput, Float) -> Void)?](/documentation/gamecontroller/gcrelativeinput/deltadidchangehandler)
- [var lastDeltaTimestamp: TimeInterval](/documentation/gamecontroller/gcrelativeinput/lastdeltatimestamp)
- [var lastDeltaLatency: TimeInterval](/documentation/gamecontroller/gcrelativeinput/lastdeltalatency)

#### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gcrelativeinput/sources)

### Steering and switch elements

- [GCSteeringWheelElement](/documentation/gamecontroller/gcsteeringwheelelement)

#### Getting the characteristics

- [var maximumDegreesOfRotation: Float](/documentation/gamecontroller/gcsteeringwheelelement/maximumdegreesofrotation)
- [GCSwitchPositionInput](/documentation/gamecontroller/gcswitchpositioninput)

#### Getting the characteristics

- [var positionRange: NSRange](/documentation/gamecontroller/gcswitchpositioninput/positionrange)
- [var isSequential: Bool](/documentation/gamecontroller/gcswitchpositioninput/issequential)
- [var canWrap: Bool](/documentation/gamecontroller/gcswitchpositioninput/canwrap)

#### Getting the position

- [var position: Int](/documentation/gamecontroller/gcswitchpositioninput/position)
- [var positionDidChangeHandler: ((any GCPhysicalInputElement, any GCSwitchPositionInput, Int) -> Void)?](/documentation/gamecontroller/gcswitchpositioninput/positiondidchangehandler)
- [var lastPositionTimestamp: TimeInterval](/documentation/gamecontroller/gcswitchpositioninput/lastpositiontimestamp)
- [var lastPositionLatency: TimeInterval](/documentation/gamecontroller/gcswitchpositioninput/lastpositionlatency)

#### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gcswitchpositioninput/sources)

### Directional pad elements

- [GCLinearInput](/documentation/gamecontroller/gclinearinput)

#### Getting the characteristics

- [var canWrap: Bool](/documentation/gamecontroller/gclinearinput/canwrap)
- [var isAnalog: Bool](/documentation/gamecontroller/gclinearinput/isanalog)

#### Getting the value

- [var value: Float](/documentation/gamecontroller/gclinearinput/value)
- [var valueDidChangeHandler: ((any GCPhysicalInputElement, any GCLinearInput, Float) -> Void)?](/documentation/gamecontroller/gclinearinput/valuedidchangehandler)
- [var lastValueTimestamp: TimeInterval](/documentation/gamecontroller/gclinearinput/lastvaluetimestamp)
- [var lastValueLatency: TimeInterval](/documentation/gamecontroller/gclinearinput/lastvaluelatency)

#### Getting user actions

- [var sources: Set<AnyHashable>](/documentation/gamecontroller/gclinearinput/sources)

#### Instance Properties

- [var physicalExtents: (any GCPhysicalInputExtents)?](/documentation/gamecontroller/gclinearinput/physicalextents)

## Game Controller framework migration from IOKit

- [Understanding game controller backward compatibility](/documentation/gamecontroller/understanding-game-controller-backward-compatibility)
- [var kIOHIDGCSyntheticDeviceKey: String](/documentation/gamecontroller/kiohidgcsyntheticdevicekey)

## Aliases for backward compatibility

- [GCDeviceElement](/documentation/gamecontroller/gcdeviceelement)
- [GCDeviceAxisInput](/documentation/gamecontroller/gcdeviceaxisinput)
- [GCDeviceButtonInput](/documentation/gamecontroller/gcdevicebuttoninput)
- [GCDeviceTouchpad](/documentation/gamecontroller/gcdevicetouchpad)
- [GCDeviceDirectionPad](/documentation/gamecontroller/gcdevicedirectionpad)

## Deprecated symbols

- [Deprecated symbols](/documentation/gamecontroller/deprecated-symbols)

### Deprecated symbols

- [GCGamepad](/documentation/gamecontroller/gcgamepad)

#### Determining the Controller That Owns This Profile

- [var controller: GCController?](/documentation/gamecontroller/gcgamepad/controller)

#### Determining When Any Element in the Profile Changes

- [var valueChangedHandler: GCGamepadValueChangedHandler?](/documentation/gamecontroller/gcgamepad/valuechangedhandler)

#### Reading Shoulder Button Inputs

- [var leftShoulder: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/leftshoulder)
- [var rightShoulder: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/rightshoulder)

#### Reading Directional Pad Inputs

- [var dpad: GCControllerDirectionPad](/documentation/gamecontroller/gcgamepad/dpad)

#### Reading Face Button Inputs

- [var buttonA: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/buttona)
- [var buttonB: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/buttonb)
- [var buttonX: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/buttonx)
- [var buttonY: GCControllerButtonInput](/documentation/gamecontroller/gcgamepad/buttony)

#### Saving a Snapshot

- [func saveSnapshot() -> GCGamepadSnapshot](/documentation/gamecontroller/gcgamepad/savesnapshot())

#### Constants

- [GCGamepadValueChangedHandler](/documentation/gamecontroller/gcgamepadvaluechangedhandler)
- [GCExtendedGamepadSnapshot](/documentation/gamecontroller/gcextendedgamepadsnapshot)

#### Converting Between Extended Snapshots and Data Objects

- [init(snapshotData: Data)](/documentation/gamecontroller/gcextendedgamepadsnapshot/init(snapshotdata:))
- [init(controller: GCController, snapshotData: Data)](/documentation/gamecontroller/gcextendedgamepadsnapshot/init(controller:snapshotdata:))
- [var snapshotData: Data](/documentation/gamecontroller/gcextendedgamepadsnapshot/snapshotdata)

#### Flattening a Snapshot to Memory

- [GCExtendedGamepadSnapShotDataV100](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100)

##### Instance Properties

- [var buttonA: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/buttona)
- [var buttonB: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/buttonb)
- [var buttonX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/buttonx)
- [var buttonY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/buttony)
- [var dpadX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/dpadx)
- [var dpadY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/dpady)
- [var leftShoulder: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/leftshoulder)
- [var leftThumbstickX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/leftthumbstickx)
- [var leftThumbstickY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/leftthumbsticky)
- [var leftTrigger: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/lefttrigger)
- [var rightShoulder: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/rightshoulder)
- [var rightThumbstickX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/rightthumbstickx)
- [var rightThumbstickY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/rightthumbsticky)
- [var rightTrigger: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/righttrigger)
- [var size: UInt16](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/size)
- [var version: UInt16](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/version)

##### Initializers

- [init()](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/init())
- [init(version: UInt16, size: UInt16, dpadX: Float, dpadY: Float, buttonA: Float, buttonB: Float, buttonX: Float, buttonY: Float, leftShoulder: Float, rightShoulder: Float, leftThumbstickX: Float, leftThumbstickY: Float, rightThumbstickX: Float, rightThumbstickY: Float, leftTrigger: Float, rightTrigger: Float)](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100/init(version:size:dpadx:dpady:buttona:buttonb:buttonx:buttony:leftshoulder:rightshoulder:leftthumbstickx:leftthumbsticky:rightthumbstickx:rightthumbsticky:lefttrigger:righttrigger:))
- [func NSDataFromGCExtendedGamepadSnapShotDataV100(UnsafeMutablePointer<GCExtendedGamepadSnapShotDataV100>?) -> Data?](/documentation/gamecontroller/nsdatafromgcextendedgamepadsnapshotdatav100(_:))
- [func GCExtendedGamepadSnapShotDataV100FromNSData(UnsafeMutablePointer<GCExtendedGamepadSnapShotDataV100>?, Data?) -> Bool](/documentation/gamecontroller/gcextendedgamepadsnapshotdatav100fromnsdata(_:_:))
- [GCGamepadSnapshot](/documentation/gamecontroller/gcgamepadsnapshot)

#### Converting Between Snapshots and Data Objects

- [init(snapshotData: Data)](/documentation/gamecontroller/gcgamepadsnapshot/init(snapshotdata:))
- [init(controller: GCController, snapshotData: Data)](/documentation/gamecontroller/gcgamepadsnapshot/init(controller:snapshotdata:))
- [var snapshotData: Data](/documentation/gamecontroller/gcgamepadsnapshot/snapshotdata)

#### Flattening a Snapshot to Memory

- [GCGamepadSnapShotDataV100](/documentation/gamecontroller/gcgamepadsnapshotdatav100)

##### Instance Properties

- [var buttonA: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/buttona)
- [var buttonB: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/buttonb)
- [var buttonX: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/buttonx)
- [var buttonY: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/buttony)
- [var dpadX: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/dpadx)
- [var dpadY: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/dpady)
- [var leftShoulder: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/leftshoulder)
- [var rightShoulder: Float](/documentation/gamecontroller/gcgamepadsnapshotdatav100/rightshoulder)
- [var size: UInt16](/documentation/gamecontroller/gcgamepadsnapshotdatav100/size)
- [var version: UInt16](/documentation/gamecontroller/gcgamepadsnapshotdatav100/version)

##### Initializers

- [init()](/documentation/gamecontroller/gcgamepadsnapshotdatav100/init())
- [init(version: UInt16, size: UInt16, dpadX: Float, dpadY: Float, buttonA: Float, buttonB: Float, buttonX: Float, buttonY: Float, leftShoulder: Float, rightShoulder: Float)](/documentation/gamecontroller/gcgamepadsnapshotdatav100/init(version:size:dpadx:dpady:buttona:buttonb:buttonx:buttony:leftshoulder:rightshoulder:))
- [func NSDataFromGCGamepadSnapShotDataV100(UnsafeMutablePointer<GCGamepadSnapShotDataV100>?) -> Data?](/documentation/gamecontroller/nsdatafromgcgamepadsnapshotdatav100(_:))
- [func GCGamepadSnapShotDataV100FromNSData(UnsafeMutablePointer<GCGamepadSnapShotDataV100>?, Data?) -> Bool](/documentation/gamecontroller/gcgamepadsnapshotdatav100fromnsdata(_:_:))
- [GCMicroGamepadSnapshot](/documentation/gamecontroller/gcmicrogamepadsnapshot)

#### Converting Between Snapshots and Data Objects

- [init(snapshotData: Data)](/documentation/gamecontroller/gcmicrogamepadsnapshot/init(snapshotdata:))
- [init(controller: GCController, snapshotData: Data)](/documentation/gamecontroller/gcmicrogamepadsnapshot/init(controller:snapshotdata:))
- [var snapshotData: Data](/documentation/gamecontroller/gcmicrogamepadsnapshot/snapshotdata)

#### Flattening a Snapshot to Memory

- [GCMicroGamepadSnapShotDataV100](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100)

##### Instance Properties

- [var buttonA: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/buttona)
- [var buttonX: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/buttonx)
- [var dpadX: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/dpadx)
- [var dpadY: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/dpady)
- [var size: UInt16](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/size)
- [var version: UInt16](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/version)

##### Initializers

- [init()](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/init())
- [init(version: UInt16, size: UInt16, dpadX: Float, dpadY: Float, buttonA: Float, buttonX: Float)](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100/init(version:size:dpadx:dpady:buttona:buttonx:))
- [func NSDataFromGCMicroGamepadSnapShotDataV100(UnsafeMutablePointer<GCMicroGamepadSnapShotDataV100>?) -> Data?](/documentation/gamecontroller/nsdatafromgcmicrogamepadsnapshotdatav100(_:))
- [func GCMicroGamepadSnapShotDataV100FromNSData(UnsafeMutablePointer<GCMicroGamepadSnapShotDataV100>?, Data?) -> Bool](/documentation/gamecontroller/gcmicrogamepadsnapshotdatav100fromnsdata(_:_:))
- [GCExtendedGamepadSnapshotData](/documentation/gamecontroller/gcextendedgamepadsnapshotdata)

#### Initializers

- [init()](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/init())
- [init(version: UInt16, size: UInt16, dpadX: Float, dpadY: Float, buttonA: Float, buttonB: Float, buttonX: Float, buttonY: Float, leftShoulder: Float, rightShoulder: Float, leftThumbstickX: Float, leftThumbstickY: Float, rightThumbstickX: Float, rightThumbstickY: Float, leftTrigger: Float, rightTrigger: Float, supportsClickableThumbsticks: ObjCBool, leftThumbstickButton: ObjCBool, rightThumbstickButton: ObjCBool)](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/init(version:size:dpadx:dpady:buttona:buttonb:buttonx:buttony:leftshoulder:rightshoulder:leftthumbstickx:leftthumbsticky:rightthumbstickx:rightthumbsticky:lefttrigger:righttrigger:supportsclickablethumbsticks:leftthumbstickbutton:rightthumb-26via)

#### Instance Properties

- [var buttonA: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/buttona)
- [var buttonB: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/buttonb)
- [var buttonX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/buttonx)
- [var buttonY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/buttony)
- [var dpadX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/dpadx)
- [var dpadY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/dpady)
- [var leftShoulder: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/leftshoulder)
- [var leftThumbstickButton: ObjCBool](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/leftthumbstickbutton)
- [var leftThumbstickX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/leftthumbstickx)
- [var leftThumbstickY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/leftthumbsticky)
- [var leftTrigger: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/lefttrigger)
- [var rightShoulder: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/rightshoulder)
- [var rightThumbstickButton: ObjCBool](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/rightthumbstickbutton)
- [var rightThumbstickX: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/rightthumbstickx)
- [var rightThumbstickY: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/rightthumbsticky)
- [var rightTrigger: Float](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/righttrigger)
- [var size: UInt16](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/size)
- [var supportsClickableThumbsticks: ObjCBool](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/supportsclickablethumbsticks)
- [var version: UInt16](/documentation/gamecontroller/gcextendedgamepadsnapshotdata/version)
- [GCMicroGamepadSnapshotData](/documentation/gamecontroller/gcmicrogamepadsnapshotdata)

#### Initializers

- [init()](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/init())
- [init(version: UInt16, size: UInt16, dpadX: Float, dpadY: Float, buttonA: Float, buttonX: Float)](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/init(version:size:dpadx:dpady:buttona:buttonx:))

#### Instance Properties

- [var buttonA: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/buttona)
- [var buttonX: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/buttonx)
- [var dpadX: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/dpadx)
- [var dpadY: Float](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/dpady)
- [var size: UInt16](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/size)
- [var version: UInt16](/documentation/gamecontroller/gcmicrogamepadsnapshotdata/version)
- [GCExtendedGamepadSnapshotDataVersion](/documentation/gamecontroller/gcextendedgamepadsnapshotdataversion)

#### Enumeration Cases

- [case version1](/documentation/gamecontroller/gcextendedgamepadsnapshotdataversion/version1)
- [case version2](/documentation/gamecontroller/gcextendedgamepadsnapshotdataversion/version2)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcextendedgamepadsnapshotdataversion/init(rawvalue:))
- [GCMicroGamepadSnapshotDataVersion](/documentation/gamecontroller/gcmicrogamepadsnapshotdataversion)

#### Enumeration Cases

- [case version1](/documentation/gamecontroller/gcmicrogamepadsnapshotdataversion/version1)

#### Initializers

- [init?(rawValue: Int)](/documentation/gamecontroller/gcmicrogamepadsnapshotdataversion/init(rawvalue:))
- [let GCCurrentExtendedGamepadSnapshotDataVersion: GCExtendedGamepadSnapshotDataVersion](/documentation/gamecontroller/gccurrentextendedgamepadsnapshotdataversion)
- [let GCCurrentMicroGamepadSnapshotDataVersion: GCMicroGamepadSnapshotDataVersion](/documentation/gamecontroller/gccurrentmicrogamepadsnapshotdataversion)
- [func GCExtendedGamepadSnapshotDataFromNSData(UnsafeMutablePointer<GCExtendedGamepadSnapshotData>?, Data?) -> Bool](/documentation/gamecontroller/gcextendedgamepadsnapshotdatafromnsdata(_:_:))
- [func GCMicroGamepadSnapshotDataFromNSData(UnsafeMutablePointer<GCMicroGamepadSnapshotData>?, Data?) -> Bool](/documentation/gamecontroller/gcmicrogamepadsnapshotdatafromnsdata(_:_:))
- [func NSDataFromGCExtendedGamepadSnapshotData(UnsafeMutablePointer<GCExtendedGamepadSnapshotData>?) -> Data?](/documentation/gamecontroller/nsdatafromgcextendedgamepadsnapshotdata(_:))
- [func NSDataFromGCMicroGamepadSnapshotData(UnsafeMutablePointer<GCMicroGamepadSnapshotData>?) -> Data?](/documentation/gamecontroller/nsdatafromgcmicrogamepadsnapshotdata(_:))

## Protocols

- [GCPhysicalInputExtents](/documentation/gamecontroller/gcphysicalinputextents)

### Instance Properties

- [var maximumValue: Double](/documentation/gamecontroller/gcphysicalinputextents/maximumvalue)
- [var minimumValue: Double](/documentation/gamecontroller/gcphysicalinputextents/minimumvalue)
- [var scaledValue: Double](/documentation/gamecontroller/gcphysicalinputextents/scaledvalue)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
