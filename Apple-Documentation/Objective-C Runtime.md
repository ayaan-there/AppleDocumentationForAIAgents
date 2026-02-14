# ObjectiveC Documentation

Source: https://sosumi.ai/documentation/objectivec

---
title: Objective-C Runtime
source: https://developer.apple.com/documentation/objectivec
timestamp: 2026-02-13T19:57:56.140Z
---

## Classes

- [NSObject](/documentation/objectivec/nsobject-swift.class)

### Initializing a Class

- [class func initialize()](/documentation/objectivec/nsobject-swift.class/initialize())
- [class func load()](/documentation/objectivec/nsobject-swift.class/load())

### Creating, Copying, and Deallocating Objects

- [init()](/documentation/objectivec/nsobject-swift.class/init())
- [func copy() -> Any](/documentation/objectivec/nsobject-swift.class/copy())
- [func mutableCopy() -> Any](/documentation/objectivec/nsobject-swift.class/mutablecopy())

### Identifying Classes

- [class func superclass() -> AnyClass?](/documentation/objectivec/nsobject-swift.class/superclass())
- [class func isSubclass(of: AnyClass) -> Bool](/documentation/objectivec/nsobject-swift.class/issubclass(of:))

### Testing Class Functionality

- [class func instancesRespond(to: Selector!) -> Bool](/documentation/objectivec/nsobject-swift.class/instancesrespond(to:))

### Testing Protocol Conformance

- [class func conforms(to: Protocol) -> Bool](/documentation/objectivec/nsobject-swift.class/conforms(to:))

### Obtaining Information About Methods

- [func method(for: Selector!) -> IMP!](/documentation/objectivec/nsobject-swift.class/method(for:))
- [class func instanceMethod(for: Selector!) -> IMP!](/documentation/objectivec/nsobject-swift.class/instancemethod(for:))

### Describing Objects

- [class func description() -> String](/documentation/objectivec/nsobject-swift.class/description())

### Supporting Discardable Content

- [var autoContentAccessingProxy: Any](/documentation/objectivec/nsobject-swift.class/autocontentaccessingproxy)

### Sending Messages

- [func perform(Selector, with: Any?, afterDelay: TimeInterval)](/documentation/objectivec/nsobject-swift.class/perform(_:with:afterdelay:))
- [func perform(Selector, with: Any?, afterDelay: TimeInterval, inModes: [RunLoop.Mode])](/documentation/objectivec/nsobject-swift.class/perform(_:with:afterdelay:inmodes:))
- [func performSelector(onMainThread: Selector, with: Any?, waitUntilDone: Bool)](/documentation/objectivec/nsobject-swift.class/performselector(onmainthread:with:waituntildone:))
- [func performSelector(onMainThread: Selector, with: Any?, waitUntilDone: Bool, modes: [String]?)](/documentation/objectivec/nsobject-swift.class/performselector(onmainthread:with:waituntildone:modes:))
- [func perform(Selector, on: Thread, with: Any?, waitUntilDone: Bool)](/documentation/objectivec/nsobject-swift.class/perform(_:on:with:waituntildone:))
- [func perform(Selector, on: Thread, with: Any?, waitUntilDone: Bool, modes: [String]?)](/documentation/objectivec/nsobject-swift.class/perform(_:on:with:waituntildone:modes:))
- [func performSelector(inBackground: Selector, with: Any?)](/documentation/objectivec/nsobject-swift.class/performselector(inbackground:with:))
- [class func cancelPreviousPerformRequests(withTarget: Any)](/documentation/objectivec/nsobject-swift.class/cancelpreviousperformrequests(withtarget:))
- [class func cancelPreviousPerformRequests(withTarget: Any, selector: Selector, object: Any?)](/documentation/objectivec/nsobject-swift.class/cancelpreviousperformrequests(withtarget:selector:object:))

### Forwarding Messages

- [func forwardingTarget(for: Selector!) -> Any?](/documentation/objectivec/nsobject-swift.class/forwardingtarget(for:))

### Dynamically Resolving Methods

- [class func resolveClassMethod(Selector!) -> Bool](/documentation/objectivec/nsobject-swift.class/resolveclassmethod(_:))
- [class func resolveInstanceMethod(Selector!) -> Bool](/documentation/objectivec/nsobject-swift.class/resolveinstancemethod(_:))

### Handling Errors

- [func doesNotRecognizeSelector(Selector!)](/documentation/objectivec/nsobject-swift.class/doesnotrecognizeselector(_:))

### Archiving

- [func awakeAfter(using: NSCoder) -> Any?](/documentation/objectivec/nsobject-swift.class/awakeafter(using:))
- [var classForArchiver: AnyClass?](/documentation/objectivec/nsobject-swift.class/classforarchiver)
- [var classForCoder: AnyClass](/documentation/objectivec/nsobject-swift.class/classforcoder)
- [var classForKeyedArchiver: AnyClass?](/documentation/objectivec/nsobject-swift.class/classforkeyedarchiver)
- [class func classFallbacksForKeyedArchiver() -> [String]](/documentation/objectivec/nsobject-swift.class/classfallbacksforkeyedarchiver())
- [class func classForKeyedUnarchiver() -> AnyClass](/documentation/objectivec/nsobject-swift.class/classforkeyedunarchiver())
- [func replacementObject(for: NSArchiver) -> Any?](/documentation/objectivec/nsobject-swift.class/replacementobject(for:)-8ih2x)
- [func replacementObject(for: NSCoder) -> Any?](/documentation/objectivec/nsobject-swift.class/replacementobject(for:)-2l8ox)
- [func replacementObject(for: NSKeyedArchiver) -> Any?](/documentation/objectivec/nsobject-swift.class/replacementobject(for:)-60vwc)
- [class func setVersion(Int)](/documentation/objectivec/nsobject-swift.class/setversion(_:))
- [class func version() -> Int](/documentation/objectivec/nsobject-swift.class/version())

### Working with Class Descriptions

- [var attributeKeys: [String]](/documentation/objectivec/nsobject-swift.class/attributekeys)
- [var classDescription: NSClassDescription](/documentation/objectivec/nsobject-swift.class/classdescription)
- [func inverse(forRelationshipKey: String) -> String?](/documentation/objectivec/nsobject-swift.class/inverse(forrelationshipkey:))
- [var toManyRelationshipKeys: [String]](/documentation/objectivec/nsobject-swift.class/tomanyrelationshipkeys)
- [var toOneRelationshipKeys: [String]](/documentation/objectivec/nsobject-swift.class/toonerelationshipkeys)

### Improving Accessibility

- [UIAccessibility](/documentation/uikit/uiaccessibility-protocol)
- [UIAccessibilityContainer](/documentation/uikit/uiaccessibilitycontainer)
- [UIAccessibilityAction](/documentation/objectivec/uiaccessibilityaction)

#### Performing an action

- [func accessibilityActivate() -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityactivate())
- [func accessibilityIncrement()](/documentation/objectivec/nsobject-swift.class/accessibilityincrement())
- [func accessibilityDecrement()](/documentation/objectivec/nsobject-swift.class/accessibilitydecrement())
- [func accessibilityScroll(UIAccessibilityScrollDirection) -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityscroll(_:))
- [func accessibilityPerformEscape() -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityperformescape())
- [func accessibilityPerformMagicTap() -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityperformmagictap())

#### Accessing custom actions

- [var accessibilityCustomActions: [UIAccessibilityCustomAction]?](/documentation/objectivec/nsobject-swift.class/accessibilitycustomactions)

#### Constants

- [UIAccessibilityScrollDirection](/documentation/uikit/uiaccessibilityscrolldirection)
- [UIAccessibilityFocus](/documentation/objectivec/uiaccessibilityfocus)

#### Getting focus information

- [func accessibilityElementDidBecomeFocused()](/documentation/objectivec/nsobject-swift.class/accessibilityelementdidbecomefocused())
- [func accessibilityElementDidLoseFocus()](/documentation/objectivec/nsobject-swift.class/accessibilityelementdidlosefocus())
- [func accessibilityElementIsFocused() -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityelementisfocused())
- [func accessibilityAssistiveTechnologyFocusedIdentifiers() -> Set<UIAccessibility.AssistiveTechnologyIdentifier>?](/documentation/objectivec/nsobject-swift.class/accessibilityassistivetechnologyfocusedidentifiers())
- [UIAccessibilityDragging](/documentation/objectivec/uiaccessibilitydragging)

#### Fine-Tuning Drag and Drop

- [var accessibilityDragSourceDescriptors: [UIAccessibilityLocationDescriptor]?](/documentation/objectivec/nsobject-swift.class/accessibilitydragsourcedescriptors)
- [var accessibilityDropPointDescriptors: [UIAccessibilityLocationDescriptor]?](/documentation/objectivec/nsobject-swift.class/accessibilitydroppointdescriptors)

### Improving browser accessibility

- [func browserAccessibilityAttributedValue(in: NSRange) -> NSAttributedString](/documentation/objectivec/nsobject-swift.class/browseraccessibilityattributedvalue(in:))
- [func browserAccessibilityDeleteTextAtCursor(numberOfCharacters: Int)](/documentation/objectivec/nsobject-swift.class/browseraccessibilitydeletetextatcursor(numberofcharacters:))
- [func browserAccessibilityInsertTextAtCursor(text: String)](/documentation/objectivec/nsobject-swift.class/browseraccessibilityinserttextatcursor(text:))
- [func browserAccessibilitySelectedTextRange() -> NSRange](/documentation/objectivec/nsobject-swift.class/browseraccessibilityselectedtextrange())
- [func browserAccessibilitySetSelectedTextRange(NSRange)](/documentation/objectivec/nsobject-swift.class/browseraccessibilitysetselectedtextrange(_:))
- [func browserAccessibilityValue(in: NSRange) -> String](/documentation/objectivec/nsobject-swift.class/browseraccessibilityvalue(in:))
- [var browserAccessibilityContainerType: BEAccessibilityContainerType](/documentation/objectivec/nsobject-swift.class/browseraccessibilitycontainertype)
- [var browserAccessibilityCurrentStatus: String?](/documentation/objectivec/nsobject-swift.class/browseraccessibilitycurrentstatus)
- [var browserAccessibilityHasDOMFocus: Bool](/documentation/objectivec/nsobject-swift.class/browseraccessibilityhasdomfocus)
- [var browserAccessibilityIsRequired: Bool](/documentation/objectivec/nsobject-swift.class/browseraccessibilityisrequired)
- [var browserAccessibilityPressedState: BEAccessibilityPressedState](/documentation/objectivec/nsobject-swift.class/browseraccessibilitypressedstate)
- [var browserAccessibilityRoleDescription: String?](/documentation/objectivec/nsobject-swift.class/browseraccessibilityroledescription)
- [var browserAccessibilitySortDirection: String?](/documentation/objectivec/nsobject-swift.class/browseraccessibilitysortdirection)

### Scripting

- [var classCode: FourCharCode](/documentation/objectivec/nsobject-swift.class/classcode)
- [var className: String](/documentation/objectivec/nsobject-swift.class/classname)
- [func copyScriptingValue(Any, forKey: String, withProperties: [String : Any]) -> Any?](/documentation/objectivec/nsobject-swift.class/copyscriptingvalue(_:forkey:withproperties:))
- [func newScriptingObject(of: AnyClass, forValueForKey: String, withContentsValue: Any?, properties: [String : Any]) -> Any?](/documentation/objectivec/nsobject-swift.class/newscriptingobject(of:forvalueforkey:withcontentsvalue:properties:))
- [var scriptingProperties: [String : Any]?](/documentation/objectivec/nsobject-swift.class/scriptingproperties)
- [func scriptingValue(for: NSScriptObjectSpecifier) -> Any?](/documentation/objectivec/nsobject-swift.class/scriptingvalue(for:))

### Integrating with Combine

- [NSObject.KeyValueObservingPublisher](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher)

#### Creating a KVO Publisher

- [init(object: Subject, keyPath: KeyPath<Subject, Value>, options: NSKeyValueObservingOptions)](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher/init(object:keypath:options:))

#### Inspecting KVO Publisher Properties

- [let object: Subject](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher/object)
- [let keyPath: KeyPath<Subject, Value>](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher/keypath)
- [let options: NSKeyValueObservingOptions](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher/options)

#### Instance Methods

- [func didChange() -> Publishers.Map<NSObject.KeyValueObservingPublisher<Subject, Value>, Void>](/documentation/objectivec/nsobject-swift.class/keyvalueobservingpublisher/didchange())

### Key-Value Observing

- [NSKeyValueObserving](/documentation/objectivec/nskeyvalueobserving)

#### Change Notification

- [func observeValue(forKeyPath: String?, of: Any?, change: [NSKeyValueChangeKey : Any]?, context: UnsafeMutableRawPointer?)](/documentation/objectivec/nsobject-swift.class/observevalue(forkeypath:of:change:context:))

#### Registering for Observation

- [func addObserver(NSObject, forKeyPath: String, options: NSKeyValueObservingOptions, context: UnsafeMutableRawPointer?)](/documentation/objectivec/nsobject-swift.class/addobserver(_:forkeypath:options:context:))
- [func removeObserver(NSObject, forKeyPath: String)](/documentation/objectivec/nsobject-swift.class/removeobserver(_:forkeypath:))
- [func removeObserver(NSObject, forKeyPath: String, context: UnsafeMutableRawPointer?)](/documentation/objectivec/nsobject-swift.class/removeobserver(_:forkeypath:context:))

#### Notifying Observers of Changes

- [func willChangeValue(forKey: String)](/documentation/objectivec/nsobject-swift.class/willchangevalue(forkey:))
- [func didChangeValue(forKey: String)](/documentation/objectivec/nsobject-swift.class/didchangevalue(forkey:))
- [func willChange(NSKeyValueChange, valuesAt: IndexSet, forKey: String)](/documentation/objectivec/nsobject-swift.class/willchange(_:valuesat:forkey:))
- [func didChange(NSKeyValueChange, valuesAt: IndexSet, forKey: String)](/documentation/objectivec/nsobject-swift.class/didchange(_:valuesat:forkey:))
- [func willChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/objectivec/nsobject-swift.class/willchangevalue(forkey:withsetmutation:using:))
- [func didChangeValue(forKey: String, withSetMutation: NSKeyValueSetMutationKind, using: Set<AnyHashable>)](/documentation/objectivec/nsobject-swift.class/didchangevalue(forkey:withsetmutation:using:))

#### Observing Customization

- [class func automaticallyNotifiesObservers(forKey: String) -> Bool](/documentation/objectivec/nsobject-swift.class/automaticallynotifiesobservers(forkey:))
- [class func keyPathsForValuesAffectingValue(forKey: String) -> Set<String>](/documentation/objectivec/nsobject-swift.class/keypathsforvaluesaffectingvalue(forkey:))
- [NSKeyValueObservingCustomization](/documentation/foundation/nskeyvalueobservingcustomization)
- [var observationInfo: UnsafeMutableRawPointer?](/documentation/objectivec/nsobject-swift.class/observationinfo)

#### Constants

- [NSKeyValueObservation](/documentation/foundation/nskeyvalueobservation)
- [NSKeyValueObservedChange](/documentation/foundation/nskeyvalueobservedchange)
- [NSKeyValueChange](/documentation/foundation/nskeyvaluechange)
- [NSKeyValueObservingOptions](/documentation/foundation/nskeyvalueobservingoptions)
- [NSKeyValueChangeKey](/documentation/foundation/nskeyvaluechangekey)
- [NSKeyValueSetMutationKind](/documentation/foundation/nskeyvaluesetmutationkind)

### Key-Value Coding

- [NSKeyValueBindingCreation](/documentation/objectivec/nskeyvaluebindingcreation)

#### Exposing bindings

- [class func exposeBinding(NSBindingName)](/documentation/objectivec/nsobject-swift.class/exposebinding(_:))
- [var exposedBindings: [NSBindingName]](/documentation/objectivec/nsobject-swift.class/exposedbindings)

#### Managing bindings

- [func valueClassForBinding(NSBindingName) -> AnyClass?](/documentation/objectivec/nsobject-swift.class/valueclassforbinding(_:))
- [func bind(NSBindingName, to: Any, withKeyPath: String, options: [NSBindingOption : Any]?)](/documentation/objectivec/nsobject-swift.class/bind(_:to:withkeypath:options:))
- [func optionDescriptionsForBinding(NSBindingName) -> [NSAttributeDescription]](/documentation/objectivec/nsobject-swift.class/optiondescriptionsforbinding(_:))
- [func infoForBinding(NSBindingName) -> [NSBindingInfoKey : Any]?](/documentation/objectivec/nsobject-swift.class/infoforbinding(_:))
- [NSBindingInfoKey](/documentation/appkit/nsbindinginfokey)
- [func unbind(NSBindingName)](/documentation/objectivec/nsobject-swift.class/unbind(_:))
- [func NSIsControllerMarker(Any?) -> Bool](/documentation/appkit/nsiscontrollermarker(_:))

#### Constants

- [NSBindingName](/documentation/appkit/nsbindingname)
- [NSBindingOption](/documentation/appkit/nsbindingoption)
- [Binding Dictionary Keys](/documentation/objectivec/binding-dictionary-keys)

##### Constants

- [static let observedObject: NSBindingInfoKey](/documentation/appkit/nsbindinginfokey/observedobject)
- [static let observedKeyPath: NSBindingInfoKey](/documentation/appkit/nsbindinginfokey/observedkeypath)
- [static let options: NSBindingInfoKey](/documentation/appkit/nsbindinginfokey/options)
- [NSKeyValueCoding](/documentation/objectivec/nskeyvaluecoding)

#### Getting Values

- [func value(forKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(forkey:))
- [func value(forKeyPath: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(forkeypath:))
- [func dictionaryWithValues(forKeys: [String]) -> [String : Any]](/documentation/objectivec/nsobject-swift.class/dictionarywithvalues(forkeys:))
- [func value(forUndefinedKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(forundefinedkey:))
- [func mutableArrayValue(forKey: String) -> NSMutableArray](/documentation/objectivec/nsobject-swift.class/mutablearrayvalue(forkey:))
- [func mutableArrayValue(forKeyPath: String) -> NSMutableArray](/documentation/objectivec/nsobject-swift.class/mutablearrayvalue(forkeypath:))
- [func mutableSetValue(forKey: String) -> NSMutableSet](/documentation/objectivec/nsobject-swift.class/mutablesetvalue(forkey:))
- [func mutableSetValue(forKeyPath: String) -> NSMutableSet](/documentation/objectivec/nsobject-swift.class/mutablesetvalue(forkeypath:))
- [func mutableOrderedSetValue(forKey: String) -> NSMutableOrderedSet](/documentation/objectivec/nsobject-swift.class/mutableorderedsetvalue(forkey:))
- [func mutableOrderedSetValue(forKeyPath: String) -> NSMutableOrderedSet](/documentation/objectivec/nsobject-swift.class/mutableorderedsetvalue(forkeypath:))

#### Setting Values

- [func setValue(Any?, forKeyPath: String)](/documentation/objectivec/nsobject-swift.class/setvalue(_:forkeypath:))
- [func setValuesForKeys([String : Any])](/documentation/objectivec/nsobject-swift.class/setvaluesforkeys(_:))
- [func setNilValueForKey(String)](/documentation/objectivec/nsobject-swift.class/setnilvalueforkey(_:))
- [func setValue(Any?, forKey: String)](/documentation/objectivec/nsobject-swift.class/setvalue(_:forkey:))
- [func setValue(Any?, forUndefinedKey: String)](/documentation/objectivec/nsobject-swift.class/setvalue(_:forundefinedkey:))

#### Changing Default Behavior

- [class var accessInstanceVariablesDirectly: Bool](/documentation/objectivec/nsobject-swift.class/accessinstancevariablesdirectly)

#### Validation

- [func validateValue(AutoreleasingUnsafeMutablePointer<AnyObject?>, forKey: String) throws](/documentation/objectivec/nsobject-swift.class/validatevalue(_:forkey:))
- [func validateValue(AutoreleasingUnsafeMutablePointer<AnyObject?>, forKeyPath: String) throws](/documentation/objectivec/nsobject-swift.class/validatevalue(_:forkeypath:))

#### Deprecated Methods

- [class func useStoredAccessor() -> Bool](/documentation/objectivec/nsobject-swift.class/usestoredaccessor())
- [func handleQuery(withUnboundKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/handlequery(withunboundkey:))
- [func handleTakeValue(Any?, forUnboundKey: String)](/documentation/objectivec/nsobject-swift.class/handletakevalue(_:forunboundkey:))
- [func storedValue(forKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/storedvalue(forkey:))
- [func takeStoredValue(Any?, forKey: String)](/documentation/objectivec/nsobject-swift.class/takestoredvalue(_:forkey:))
- [func takeValues(from: [AnyHashable : Any])](/documentation/objectivec/nsobject-swift.class/takevalues(from:))
- [func takeValue(Any?, forKeyPath: String)](/documentation/objectivec/nsobject-swift.class/takevalue(_:forkeypath:))
- [func takeValue(Any?, forKey: String)](/documentation/objectivec/nsobject-swift.class/takevalue(_:forkey:))
- [func unableToSetNil(forKey: String)](/documentation/objectivec/nsobject-swift.class/unabletosetnil(forkey:))
- [func values(forKeys: [Any]) -> [AnyHashable : Any]](/documentation/objectivec/nsobject-swift.class/values(forkeys:))

#### Constants

- [Key Value Coding Exception Names](/documentation/objectivec/key-value-coding-exception-names)

##### Constants

- [static let undefinedKeyException: NSExceptionName](/documentation/foundation/nsexceptionname/undefinedkeyexception)
- [NSUndefinedKeyException userInfo Keys](/documentation/objectivec/nsundefinedkeyexception-userinfo-keys)

##### Constants

- [NSTargetObjectUserInfoKey](/documentation/objectivec/nstargetobjectuserinfokey)
- [NSUnknownUserInfoKey](/documentation/objectivec/nsunknownuserinfokey)
- [var NSKeyValueValidationError: Int](/documentation/foundation/nskeyvaluevalidationerror-swift.var)
- [NSScriptKeyValueCoding](/documentation/objectivec/nsscriptkeyvaluecoding)

#### Indexed access

- [func insertValue(Any, at: Int, inPropertyWithKey: String)](/documentation/objectivec/nsobject-swift.class/insertvalue(_:at:inpropertywithkey:))
- [func removeValue(at: Int, fromPropertyWithKey: String)](/documentation/objectivec/nsobject-swift.class/removevalue(at:frompropertywithkey:))
- [func replaceValue(at: Int, inPropertyWithKey: String, withValue: Any)](/documentation/objectivec/nsobject-swift.class/replacevalue(at:inpropertywithkey:withvalue:))
- [func value(at: Int, inPropertyWithKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(at:inpropertywithkey:))

#### Access by name, key, or ID

- [func insertValue(Any, inPropertyWithKey: String)](/documentation/objectivec/nsobject-swift.class/insertvalue(_:inpropertywithkey:))
- [func value(withName: String, inPropertyWithKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(withname:inpropertywithkey:))
- [func value(withUniqueID: Any, inPropertyWithKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/value(withuniqueid:inpropertywithkey:))

#### Coercion

- [func coerceValue(Any?, forKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/coercevalue(_:forkey:))

#### Constants

- [NSScriptKeyValueCoding Exception Names](/documentation/objectivec/nsscriptkeyvaluecoding-exception-names)

##### Constants

- [let NSOperationNotSupportedForKeyException: String](/documentation/foundation/nsoperationnotsupportedforkeyexception)
- [NSScriptKeyValueCoding Exception Names](/documentation/objectivec/nsscriptkeyvaluecoding-exception-names)

#### Constants

- [let NSOperationNotSupportedForKeyException: String](/documentation/foundation/nsoperationnotsupportedforkeyexception)

### Interacting with Web Plug-ins

- [WebPlugInContainer](/documentation/objectivec/webplugincontainer)

#### Performing actions on the enclosing container

- [func webPlugInContainerLoad(URLRequest!, inFrame: String!)](/documentation/objectivec/nsobject-swift.class/webplugincontainerload(_:inframe:))
- [func webPlugInContainerShowStatus(String!)](/documentation/objectivec/nsobject-swift.class/webplugincontainershowstatus(_:))

#### Obtaining information about the container

- [var webFrame: WebFrame!](/documentation/objectivec/nsobject-swift.class/webframe)
- [var webPlugInContainerSelectionColor: NSColor!](/documentation/objectivec/nsobject-swift.class/webplugincontainerselectioncolor)
- [WebPlugIn](/documentation/objectivec/webplugin)

#### Accessing the Scripting Environment

- [var objectForWebScript: Any!](/documentation/objectivec/nsobject-swift.class/objectforwebscript)

#### Using Plug-in State Information

- [func webPlugInSetIsSelected(Bool)](/documentation/objectivec/nsobject-swift.class/webpluginsetisselected(_:))

#### Controlling the Plug-in

- [func webPlugInDestroy()](/documentation/objectivec/nsobject-swift.class/webplugindestroy())
- [func webPlugInInitialize()](/documentation/objectivec/nsobject-swift.class/webplugininitialize())
- [func webPlugInStart()](/documentation/objectivec/nsobject-swift.class/webpluginstart())
- [func webPlugInStop()](/documentation/objectivec/nsobject-swift.class/webpluginstop())

#### Main resource messages

- [func webPlugInMainResourceDidFailWithError((any Error)!)](/documentation/objectivec/nsobject-swift.class/webpluginmainresourcedidfailwitherror(_:))
- [func webPlugInMainResourceDidFinishLoading()](/documentation/objectivec/nsobject-swift.class/webpluginmainresourcedidfinishloading())
- [func webPlugInMainResourceDidReceive(Data!)](/documentation/objectivec/nsobject-swift.class/webpluginmainresourcedidreceive(_:)-5b6f6)
- [func webPlugInMainResourceDidReceive(URLResponse!)](/documentation/objectivec/nsobject-swift.class/webpluginmainresourcedidreceive(_:)-6x7b9)

### Implementing Web Scripting

- [WebScripting](/documentation/objectivec/webscripting)

#### Getting attributes

- [class func webScriptName(forKey: UnsafePointer<CChar>!) -> String!](/documentation/objectivec/nsobject-swift.class/webscriptname(forkey:))
- [class func webScriptName(for: Selector!) -> String!](/documentation/objectivec/nsobject-swift.class/webscriptname(for:))
- [class func isSelectorExcluded(fromWebScript: Selector!) -> Bool](/documentation/objectivec/nsobject-swift.class/isselectorexcluded(fromwebscript:))
- [class func isKeyExcluded(fromWebScript: UnsafePointer<CChar>!) -> Bool](/documentation/objectivec/nsobject-swift.class/iskeyexcluded(fromwebscript:))

#### Invoking methods

- [func invokeDefaultMethod(withArguments: [Any]!) -> Any!](/documentation/objectivec/nsobject-swift.class/invokedefaultmethod(witharguments:))
- [func invokeUndefinedMethod(fromWebScript: String!, withArguments: [Any]!) -> Any!](/documentation/objectivec/nsobject-swift.class/invokeundefinedmethod(fromwebscript:witharguments:))

#### Finalizing

- [func finalizeForWebScript()](/documentation/objectivec/nsobject-swift.class/finalizeforwebscript())

### Supporting Cocoa Scripting

- [NSScriptingComparisonMethods](/documentation/objectivec/nsscriptingcomparisonmethods)

#### Performing comparisons

- [func scriptingBegins(with: Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingbegins(with:))
- [func scriptingContains(Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingcontains(_:))
- [func scriptingEnds(with: Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingends(with:))
- [func scriptingIsEqual(to: Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingisequal(to:))
- [func scriptingIsGreaterThan(Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingisgreaterthan(_:))
- [func scriptingIsGreaterThanOrEqual(to: Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingisgreaterthanorequal(to:))
- [func scriptingIsLessThan(Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingislessthan(_:))
- [func scriptingIsLessThanOrEqual(to: Any) -> Bool](/documentation/objectivec/nsobject-swift.class/scriptingislessthanorequal(to:))

### Deprecated

- [Deprecated Symbols](/documentation/objectivec/deprecated-symbols)

#### Deprecated Class Methods

- [class func defaultPlaceholder(for: Any?, with: NSBindingName) -> Any?](/documentation/objectivec/nsobject-swift.class/defaultplaceholder(for:with:))
- [class func setDefaultPlaceholder(Any?, for: Any?, with: NSBindingName)](/documentation/objectivec/nsobject-swift.class/setdefaultplaceholder(_:for:with:))
- [class func useStoredAccessor() -> Bool](/documentation/objectivec/nsobject-swift.class/usestoredaccessor())

#### Deprecated Methods

- [func accessibilityAttributeNames() -> [NSAccessibility.Attribute]](/documentation/objectivec/nsobject-swift.class/accessibilityattributenames())
- [func accessibilityAttributeValue(NSAccessibility.Attribute) -> Any?](/documentation/objectivec/nsobject-swift.class/accessibilityattributevalue(_:))
- [func accessibilityAttributeValue(NSAccessibility.ParameterizedAttribute, forParameter: Any?) -> Any?](/documentation/objectivec/nsobject-swift.class/accessibilityattributevalue(_:forparameter:))
- [func accessibilityActionDescription(NSAccessibility.Action) -> String?](/documentation/objectivec/nsobject-swift.class/accessibilityactiondescription(_:))
- [func accessibilityActionNames() -> [NSAccessibility.Action]](/documentation/objectivec/nsobject-swift.class/accessibilityactionnames())
- [func accessibilityArrayAttributeCount(NSAccessibility.Attribute) -> Int](/documentation/objectivec/nsobject-swift.class/accessibilityarrayattributecount(_:))
- [func accessibilityArrayAttributeValues(NSAccessibility.Attribute, index: Int, maxCount: Int) -> [Any]](/documentation/objectivec/nsobject-swift.class/accessibilityarrayattributevalues(_:index:maxcount:))
- [func accessibilityIndex(ofChild: Any) -> Int](/documentation/objectivec/nsobject-swift.class/accessibilityindex(ofchild:))
- [func accessibilityIsAttributeSettable(NSAccessibility.Attribute) -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityisattributesettable(_:))
- [func accessibilityIsIgnored() -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityisignored())
- [func accessibilityParameterizedAttributeNames() -> [NSAccessibility.ParameterizedAttribute]](/documentation/objectivec/nsobject-swift.class/accessibilityparameterizedattributenames())
- [func accessibilityPerformAction(NSAccessibility.Action)](/documentation/objectivec/nsobject-swift.class/accessibilityperformaction(_:))
- [func accessibilitySetOverrideValue(Any?, forAttribute: NSAccessibility.Attribute) -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilitysetoverridevalue(_:forattribute:))
- [func accessibilitySetValue(Any?, forAttribute: NSAccessibility.Attribute)](/documentation/objectivec/nsobject-swift.class/accessibilitysetvalue(_:forattribute:))
- [func fileManager(FileManager, shouldProceedAfterError: [AnyHashable : Any]) -> Bool](/documentation/objectivec/nsobject-swift.class/filemanager(_:shouldproceedaftererror:))
- [func fileManager(FileManager, willProcessPath: String)](/documentation/objectivec/nsobject-swift.class/filemanager(_:willprocesspath:))
- [func finalize()](/documentation/objectivec/nsobject-swift.class/finalize())
- [func fontManager(Any, willIncludeFont: String) -> Bool](/documentation/objectivec/nsobject-swift.class/fontmanager(_:willincludefont:))
- [func namesOfPromisedFilesDropped(atDestination: URL) -> [String]?](/documentation/objectivec/nsobject-swift.class/namesofpromisedfilesdropped(atdestination:))
- [func storedValue(forKey: String) -> Any?](/documentation/objectivec/nsobject-swift.class/storedvalue(forkey:))
- [func textStorageDidProcessEditing(Notification)](/documentation/objectivec/nsobject-swift.class/textstoragedidprocessediting(_:))
- [func textStorageWillProcessEditing(Notification)](/documentation/objectivec/nsobject-swift.class/textstoragewillprocessediting(_:))
- [func takeStoredValue(Any?, forKey: String)](/documentation/objectivec/nsobject-swift.class/takestoredvalue(_:forkey:))
- [func takeValue(Any?, forKey: String)](/documentation/objectivec/nsobject-swift.class/takevalue(_:forkey:))
- [func takeValue(Any?, forKeyPath: String)](/documentation/objectivec/nsobject-swift.class/takevalue(_:forkeypath:))
- [func takeValues(from: [AnyHashable : Any])](/documentation/objectivec/nsobject-swift.class/takevalues(from:))
- [func unableToSetNil(forKey: String)](/documentation/objectivec/nsobject-swift.class/unabletosetnil(forkey:))
- [func values(forKeys: [Any]) -> [AnyHashable : Any]](/documentation/objectivec/nsobject-swift.class/values(forkeys:))
- [func workflowController(AMWorkflowController, didError: any Error)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:diderror:))
- [func workflowController(AMWorkflowController, didRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:didrun:))
- [func workflowController(AMWorkflowController, willRun: AMAction)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontroller(_:willrun:))
- [func workflowControllerDidRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidrun(_:))
- [func workflowControllerDidStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerdidstop(_:))
- [func workflowControllerWillRun(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillrun(_:))
- [func workflowControllerWillStop(AMWorkflowController)](/documentation/automator/amworkflowcontrollerdelegate/workflowcontrollerwillstop(_:))

### Instance Properties

- [var accessibilityActivateBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityactivateblock)
- [var accessibilityActivationPoint: CGPoint](/documentation/objectivec/nsobject-swift.class/accessibilityactivationpoint)
- [var accessibilityActivationPointBlock: AXPointReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityactivationpointblock)
- [var accessibilityAttributedHint: NSAttributedString?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedhint)
- [var accessibilityAttributedHintBlock: AXAttributedStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedhintblock)
- [var accessibilityAttributedLabel: NSAttributedString?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedlabel)
- [var accessibilityAttributedLabelBlock: AXAttributedStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedlabelblock)
- [var accessibilityAttributedUserInputLabels: [NSAttributedString]!](/documentation/objectivec/nsobject-swift.class/accessibilityattributeduserinputlabels)
- [var accessibilityAttributedUserInputLabelsBlock: AXAttributedStringArrayReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityattributeduserinputlabelsblock)
- [var accessibilityAttributedValue: NSAttributedString?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedvalue)
- [var accessibilityAttributedValueBlock: AXAttributedStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityattributedvalueblock)
- [var accessibilityContainerType: UIAccessibilityContainerType](/documentation/objectivec/nsobject-swift.class/accessibilitycontainertype)
- [var accessibilityContainerTypeBlock: AXContainerTypeReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitycontainertypeblock)
- [var accessibilityCustomActionsBlock: AXCustomActionsReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitycustomactionsblock)
- [var accessibilityCustomRotors: [UIAccessibilityCustomRotor]?](/documentation/objectivec/nsobject-swift.class/accessibilitycustomrotors)
- [var accessibilityCustomRotorsBlock: AXCustomRotorsReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitycustomrotorsblock)
- [var accessibilityDecrementBlock: AXVoidReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitydecrementblock)
- [var accessibilityDirectTouchOptions: UIAccessibility.DirectTouchOptions](/documentation/objectivec/nsobject-swift.class/accessibilitydirecttouchoptions)
- [var accessibilityElements: [Any]?](/documentation/objectivec/nsobject-swift.class/accessibilityelements)
- [var accessibilityElementsBlock: AXArrayReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityelementsblock)
- [var accessibilityElementsHidden: Bool](/documentation/objectivec/nsobject-swift.class/accessibilityelementshidden)
- [var accessibilityElementsHiddenBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityelementshiddenblock)
- [var accessibilityExpandedStatus: UIAccessibility.ExpandedStatus](/documentation/objectivec/nsobject-swift.class/accessibilityexpandedstatus)
- [var accessibilityExpandedStatusBlock: (() -> UIAccessibility.ExpandedStatus)?](/documentation/objectivec/nsobject-swift.class/accessibilityexpandedstatusblock)
- [var accessibilityFocusedUIElement: Any?](/documentation/objectivec/nsobject-swift.class/accessibilityfocuseduielement)
- [var accessibilityFrame: CGRect](/documentation/objectivec/nsobject-swift.class/accessibilityframe)
- [var accessibilityFrameBlock: AXRectReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityframeblock)
- [var accessibilityHeaderElements: [Any]?](/documentation/objectivec/nsobject-swift.class/accessibilityheaderelements)
- [var accessibilityHeaderElementsBlock: AXArrayReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityheaderelementsblock)
- [var accessibilityHint: String?](/documentation/objectivec/nsobject-swift.class/accessibilityhint)
- [var accessibilityHintBlock: AXStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityhintblock)
- [var accessibilityIdentifierBlock: AXStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityidentifierblock)
- [var accessibilityIncrementBlock: AXVoidReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityincrementblock)
- [var accessibilityLabel: String?](/documentation/objectivec/nsobject-swift.class/accessibilitylabel)
- [var accessibilityLabelBlock: AXStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitylabelblock)
- [var accessibilityLanguage: String?](/documentation/objectivec/nsobject-swift.class/accessibilitylanguage)
- [var accessibilityLanguageBlock: AXStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitylanguageblock)
- [var accessibilityMagicTapBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitymagictapblock)
- [var accessibilityNavigationStyle: UIAccessibilityNavigationStyle](/documentation/objectivec/nsobject-swift.class/accessibilitynavigationstyle)
- [var accessibilityNavigationStyleBlock: AXNavigationStyleReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitynavigationstyleblock)
- [var accessibilityNextTextNavigationElement: Any?](/documentation/objectivec/nsobject-swift.class/accessibilitynexttextnavigationelement)
- [var accessibilityNextTextNavigationElementBlock: AXObjectReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitynexttextnavigationelementblock)
- [var accessibilityNotifiesWhenDestroyed: Bool](/documentation/objectivec/nsobject-swift.class/accessibilitynotifieswhendestroyed)
- [var accessibilityPath: UIBezierPath?](/documentation/objectivec/nsobject-swift.class/accessibilitypath)
- [var accessibilityPathBlock: AXPathReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitypathblock)
- [var accessibilityPerformEscapeBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityperformescapeblock)
- [var accessibilityPreviousTextNavigationElement: Any?](/documentation/objectivec/nsobject-swift.class/accessibilityprevioustextnavigationelement)
- [var accessibilityPreviousTextNavigationElementBlock: AXObjectReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityprevioustextnavigationelementblock)
- [var accessibilityRespondsToUserInteraction: Bool](/documentation/objectivec/nsobject-swift.class/accessibilityrespondstouserinteraction)
- [var accessibilityRespondsToUserInteractionBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityrespondstouserinteractionblock)
- [var accessibilityShouldGroupAccessibilityChildrenBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityshouldgroupaccessibilitychildrenblock)
- [var accessibilityTextInputResponder: (any UITextInput)?](/documentation/objectivec/nsobject-swift.class/accessibilitytextinputresponder)
- [var accessibilityTextInputResponderBlock: AXUITextInputReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitytextinputresponderblock)
- [var accessibilityTextualContext: UIAccessibilityTextualContext?](/documentation/objectivec/nsobject-swift.class/accessibilitytextualcontext)
- [var accessibilityTextualContextBlock: AXTextualContextReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitytextualcontextblock)
- [var accessibilityTraits: UIAccessibilityTraits](/documentation/objectivec/nsobject-swift.class/accessibilitytraits)
- [var accessibilityTraitsBlock: AXTraitsReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilitytraitsblock)
- [var accessibilityUserInputLabels: [String]!](/documentation/objectivec/nsobject-swift.class/accessibilityuserinputlabels)
- [var accessibilityUserInputLabelsBlock: AXStringArrayReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityuserinputlabelsblock)
- [var accessibilityValue: String?](/documentation/objectivec/nsobject-swift.class/accessibilityvalue)
- [var accessibilityValueBlock: AXStringReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityvalueblock)
- [var accessibilityViewIsModal: Bool](/documentation/objectivec/nsobject-swift.class/accessibilityviewismodal)
- [var accessibilityViewIsModalBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/accessibilityviewismodalblock)
- [var automationElements: [Any]?](/documentation/objectivec/nsobject-swift.class/automationelements)
- [var automationElementsBlock: AXArrayReturnBlock?](/documentation/objectivec/nsobject-swift.class/automationelementsblock)
- [var isAccessibilityElement: Bool](/documentation/objectivec/nsobject-swift.class/isaccessibilityelement)
- [var isAccessibilityElementBlock: AXBoolReturnBlock?](/documentation/objectivec/nsobject-swift.class/isaccessibilityelementblock)
- [var isSelectable: Bool](/documentation/objectivec/nsobject-swift.class/isselectable)
- [var objectSpecifier: NSScriptObjectSpecifier?](/documentation/objectivec/nsobject-swift.class/objectspecifier)
- [var shouldGroupAccessibilityChildren: Bool](/documentation/objectivec/nsobject-swift.class/shouldgroupaccessibilitychildren)

### Instance Methods

- [func acceptsPreviewPanelControl(QLPreviewPanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/acceptspreviewpanelcontrol(_:))
- [func accessibilityElement(at: Int) -> Any?](/documentation/objectivec/nsobject-swift.class/accessibilityelement(at:))
- [func accessibilityElementCount() -> Int](/documentation/objectivec/nsobject-swift.class/accessibilityelementcount())
- [func accessibilityHitTest(NSPoint) -> Any?](/documentation/objectivec/nsobject-swift.class/accessibilityhittest(_:))
- [func accessibilityHitTest(CGPoint, event: UIEvent?) -> Any?](/documentation/objectivec/nsobject-swift.class/accessibilityhittest(_:event:))
- [func accessibilityLineEndPositionFromCurrentSelection() -> Int](/documentation/objectivec/nsobject-swift.class/accessibilitylineendpositionfromcurrentselection())
- [func accessibilityLineRange(forPosition: Int) -> NSRange](/documentation/objectivec/nsobject-swift.class/accessibilitylinerange(forposition:))
- [func accessibilityLineStartPositionFromCurrentSelection() -> Int](/documentation/objectivec/nsobject-swift.class/accessibilitylinestartpositionfromcurrentselection())
- [func accessibilityZoomIn(at: CGPoint) -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityzoomin(at:))
- [func accessibilityZoomOut(at: CGPoint) -> Bool](/documentation/objectivec/nsobject-swift.class/accessibilityzoomout(at:))
- [func actionProperty() -> String!](/documentation/objectivec/nsobject-swift.class/actionproperty())
- [func attemptRecovery(fromError: any Error, optionIndex: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/attemptrecovery(fromerror:optionindex:))
- [func attemptRecovery(fromError: any Error, optionIndex: Int, delegate: Any?, didRecoverSelector: Selector?, contextInfo: UnsafeMutableRawPointer?)](/documentation/objectivec/nsobject-swift.class/attemptrecovery(fromerror:optionindex:delegate:didrecoverselector:contextinfo:))
- [func authorizationViewCreatedAuthorization(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewcreatedauthorization(_:))
- [func authorizationViewDidAuthorize(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdidauthorize(_:))
- [func authorizationViewDidDeauthorize(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdiddeauthorize(_:))
- [func authorizationViewDidHide(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdidhide(_:))
- [func authorizationViewReleasedAuthorization(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewreleasedauthorization(_:))
- [func authorizationViewShouldDeauthorize(SFAuthorizationView!) -> Bool](/documentation/objectivec/nsobject-swift.class/authorizationviewshoulddeauthorize(_:))
- [func awakeFromNib()](/documentation/objectivec/nsobject-swift.class/awakefromnib())
- [func beginPreviewPanelControl(QLPreviewPanel!)](/documentation/objectivec/nsobject-swift.class/beginpreviewpanelcontrol(_:))
- [func burnProgressPanel(DRBurnProgressPanel!, burnDidFinish: DRBurn!) -> Bool](/documentation/objectivec/nsobject-swift.class/burnprogresspanel(_:burndidfinish:))
- [func burnProgressPanelDidFinish(Notification!)](/documentation/objectivec/nsobject-swift.class/burnprogresspaneldidfinish(_:))
- [func burnProgressPanelWillBegin(Notification!)](/documentation/objectivec/nsobject-swift.class/burnprogresspanelwillbegin(_:))
- [func candidates(Any!) -> [Any]!](/documentation/objectivec/nsobject-swift.class/candidates(_:))
- [func certificatePanelShowHelp(SFCertificatePanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/certificatepanelshowhelp(_:))
- [func chooseIdentityPanelShowHelp(SFChooseIdentityPanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/chooseidentitypanelshowhelp(_:))
- [func commitComposition(Any!)](/documentation/objectivec/nsobject-swift.class/commitcomposition(_:))
- [func composedString(Any!) -> Any!](/documentation/objectivec/nsobject-swift.class/composedstring(_:))
- [func compositionParameterView(QCCompositionParameterView!, didChangeParameterWithKey: String!)](/documentation/objectivec/nsobject-swift.class/compositionparameterview(_:didchangeparameterwithkey:))
- [func compositionParameterView(QCCompositionParameterView!, shouldDisplayParameterWithKey: String!, attributes: [AnyHashable : Any]!) -> Bool](/documentation/objectivec/nsobject-swift.class/compositionparameterview(_:shoulddisplayparameterwithkey:attributes:))
- [func compositionPickerView(QCCompositionPickerView!, didSelect: QCComposition!)](/documentation/objectivec/nsobject-swift.class/compositionpickerview(_:didselect:))
- [func compositionPickerViewDidStartAnimating(QCCompositionPickerView!)](/documentation/objectivec/nsobject-swift.class/compositionpickerviewdidstartanimating(_:))
- [func compositionPickerViewWillStopAnimating(QCCompositionPickerView!)](/documentation/objectivec/nsobject-swift.class/compositionpickerviewwillstopanimating(_:))
- [func didCommand(by: Selector!, client: Any!) -> Bool](/documentation/objectivec/nsobject-swift.class/didcommand(by:client:))
- [func doesContain(Any) -> Bool](/documentation/objectivec/nsobject-swift.class/doescontain(_:))
- [func endPreviewPanelControl(QLPreviewPanel!)](/documentation/objectivec/nsobject-swift.class/endpreviewpanelcontrol(_:))
- [func eraseProgressPanel(DREraseProgressPanel!, eraseDidFinish: DRErase!) -> Bool](/documentation/objectivec/nsobject-swift.class/eraseprogresspanel(_:erasedidfinish:))
- [func eraseProgressPanelDidFinish(Notification!)](/documentation/objectivec/nsobject-swift.class/eraseprogresspaneldidfinish(_:))
- [func eraseProgressPanelWillBegin(Notification!)](/documentation/objectivec/nsobject-swift.class/eraseprogresspanelwillbegin(_:))
- [func exceptionHandler(NSExceptionHandler!, shouldHandle: NSException!, mask: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/exceptionhandler(_:shouldhandle:mask:))
- [func exceptionHandler(NSExceptionHandler!, shouldLogException: NSException!, mask: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/exceptionhandler(_:shouldlogexception:mask:))
- [func fileTransferServicesAbortComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicesabortcomplete(_:error:))
- [func fileTransferServicesConnectionComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicesconnectioncomplete(_:error:))
- [func fileTransferServicesCopyRemoteFileComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicescopyremotefilecomplete(_:error:))
- [func fileTransferServicesCopyRemoteFileProgress(OBEXFileTransferServices!, transferProgress: [AnyHashable : Any]!)](/documentation/objectivec/nsobject-swift.class/filetransferservicescopyremotefileprogress(_:transferprogress:))
- [func fileTransferServicesCreateFolderComplete(OBEXFileTransferServices!, error: OBEXError, folder: String!)](/documentation/objectivec/nsobject-swift.class/filetransferservicescreatefoldercomplete(_:error:folder:))
- [func fileTransferServicesDisconnectionComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicesdisconnectioncomplete(_:error:))
- [func fileTransferServicesFilePreparationComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicesfilepreparationcomplete(_:error:))
- [func fileTransferServicesPathChangeComplete(OBEXFileTransferServices!, error: OBEXError, finalPath: String!)](/documentation/objectivec/nsobject-swift.class/filetransferservicespathchangecomplete(_:error:finalpath:))
- [func fileTransferServicesRemoveItemComplete(OBEXFileTransferServices!, error: OBEXError, removedItem: String!)](/documentation/objectivec/nsobject-swift.class/filetransferservicesremoveitemcomplete(_:error:removeditem:))
- [func fileTransferServicesRetrieveFolderListingComplete(OBEXFileTransferServices!, error: OBEXError, listing: [Any]!)](/documentation/objectivec/nsobject-swift.class/filetransferservicesretrievefolderlistingcomplete(_:error:listing:))
- [func fileTransferServicesSendFileComplete(OBEXFileTransferServices!, error: OBEXError)](/documentation/objectivec/nsobject-swift.class/filetransferservicessendfilecomplete(_:error:))
- [func fileTransferServicesSendFileProgress(OBEXFileTransferServices!, transferProgress: [AnyHashable : Any]!)](/documentation/objectivec/nsobject-swift.class/filetransferservicessendfileprogress(_:transferprogress:))
- [func handle(NSEvent!, client: Any!) -> Bool](/documentation/objectivec/nsobject-swift.class/handle(_:client:))
- [func imageBrowser(IKImageBrowserView!, backgroundWasRightClickedWith: NSEvent!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:backgroundwasrightclickedwith:))
- [func imageBrowser(IKImageBrowserView!, cellWasDoubleClickedAt: Int)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:cellwasdoubleclickedat:))
- [func imageBrowser(IKImageBrowserView!, cellWasRightClickedAt: Int, with: NSEvent!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:cellwasrightclickedat:with:))
- [func imageBrowser(IKImageBrowserView!, groupAt: Int) -> [AnyHashable : Any]!](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:groupat:))
- [func imageBrowser(IKImageBrowserView!, itemAt: Int) -> Any!](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:itemat:))
- [func imageBrowser(IKImageBrowserView!, moveItemsAt: IndexSet!, to: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:moveitemsat:to:))
- [func imageBrowser(IKImageBrowserView!, removeItemsAt: IndexSet!)](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:removeitemsat:))
- [func imageBrowser(IKImageBrowserView!, writeItemsAt: IndexSet!, to: NSPasteboard!) -> Int](/documentation/objectivec/nsobject-swift.class/imagebrowser(_:writeitemsat:to:))
- [func imageBrowserSelectionDidChange(IKImageBrowserView!)](/documentation/objectivec/nsobject-swift.class/imagebrowserselectiondidchange(_:))
- [func imageRepresentation() -> Any!](/documentation/objectivec/nsobject-swift.class/imagerepresentation())
- [func imageRepresentationType() -> String!](/documentation/objectivec/nsobject-swift.class/imagerepresentationtype())
- [func imageSubtitle() -> String!](/documentation/objectivec/nsobject-swift.class/imagesubtitle())
- [func imageTitle() -> String!](/documentation/objectivec/nsobject-swift.class/imagetitle())
- [func imageUID() -> String!](/documentation/objectivec/nsobject-swift.class/imageuid())
- [func imageVersion() -> Int](/documentation/objectivec/nsobject-swift.class/imageversion())
- [func index(ofAccessibilityElement: Any) -> Int](/documentation/objectivec/nsobject-swift.class/index(ofaccessibilityelement:))
- [func indicesOfObjects(byEvaluatingObjectSpecifier: NSScriptObjectSpecifier) -> [NSNumber]?](/documentation/objectivec/nsobject-swift.class/indicesofobjects(byevaluatingobjectspecifier:))
- [func inputText(String!, client: Any!) -> Bool](/documentation/objectivec/nsobject-swift.class/inputtext(_:client:))
- [func inputText(String!, key: Int, modifiers: Int, client: Any!) -> Bool](/documentation/objectivec/nsobject-swift.class/inputtext(_:key:modifiers:client:))
- [func isCaseInsensitiveLike(String) -> Bool](/documentation/objectivec/nsobject-swift.class/iscaseinsensitivelike(_:))
- [func isEqual(to: Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/isequal(to:))
- [func isGreaterThan(Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/isgreaterthan(_:))
- [func isGreaterThanOrEqual(to: Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/isgreaterthanorequal(to:))
- [func isLessThan(Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/islessthan(_:))
- [func isLessThanOrEqual(to: Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/islessthanorequal(to:))
- [func isLike(String) -> Bool](/documentation/objectivec/nsobject-swift.class/islike(_:))
- [func isNotEqual(to: Any?) -> Bool](/documentation/objectivec/nsobject-swift.class/isnotequal(to:))
- [func numberOfGroups(inImageBrowser: IKImageBrowserView!) -> Int](/documentation/objectivec/nsobject-swift.class/numberofgroups(inimagebrowser:))
- [func numberOfItems(inImageBrowser: IKImageBrowserView!) -> Int](/documentation/objectivec/nsobject-swift.class/numberofitems(inimagebrowser:))
- [func originalString(Any!) -> NSAttributedString!](/documentation/objectivec/nsobject-swift.class/originalstring(_:))
- [func performAction(for: ABPerson!, identifier: String!)](/documentation/objectivec/nsobject-swift.class/performaction(for:identifier:))
- [func prepareForInterfaceBuilder()](/documentation/objectivec/nsobject-swift.class/prepareforinterfacebuilder())
- [func provideImage(to: any MTLTexture, commandBuffer: any MTLCommandBuffer, originx: Int, originy: Int, width: Int, height: Int, userInfo: Any?)](/documentation/objectivec/nsobject-swift.class/provideimage(to:commandbuffer:originx:originy:width:height:userinfo:))
- [func provideImageData(UnsafeMutableRawPointer, bytesPerRow: Int, origin: Int, Int, size: Int, Int, userInfo: Any?)](/documentation/objectivec/nsobject-swift.class/provideimagedata(_:bytesperrow:origin:_:size:_:userinfo:))
- [func quartzFilterManager(QuartzFilterManager!, didAdd: QuartzFilter!)](/documentation/objectivec/nsobject-swift.class/quartzfiltermanager(_:didadd:))
- [func quartzFilterManager(QuartzFilterManager!, didModifyFilter: QuartzFilter!)](/documentation/objectivec/nsobject-swift.class/quartzfiltermanager(_:didmodifyfilter:))
- [func quartzFilterManager(QuartzFilterManager!, didRemove: QuartzFilter!)](/documentation/objectivec/nsobject-swift.class/quartzfiltermanager(_:didremove:))
- [func quartzFilterManager(QuartzFilterManager!, didSelect: QuartzFilter!)](/documentation/objectivec/nsobject-swift.class/quartzfiltermanager(_:didselect:))
- [func readLinkQuality(forDeviceComplete: Any!, device: IOBluetoothDevice!, info: UnsafeMutablePointer<BluetoothHCILinkQualityInfo>!, error: IOReturn)](/documentation/objectivec/nsobject-swift.class/readlinkquality(fordevicecomplete:device:info:error:))
- [func readRSSI(forDeviceComplete: Any!, device: IOBluetoothDevice!, info: UnsafeMutablePointer<BluetoothHCIRSSIInfo>!, error: IOReturn)](/documentation/objectivec/nsobject-swift.class/readrssi(fordevicecomplete:device:info:error:))
- [func saveOptions(IKSaveOptions!, shouldShowUTType: String!) -> Bool](/documentation/objectivec/nsobject-swift.class/saveoptions(_:shouldshowuttype:))
- [func setSharedObservers(NSKeyValueSharedObserversSnapshot?)](/documentation/objectivec/nsobject-swift.class/setsharedobservers(_:))
- [func setupPanel(DRSetupPanel!, determineBestDeviceOfA: DRDevice!, orB: DRDevice!) -> DRDevice!](/documentation/objectivec/nsobject-swift.class/setuppanel(_:determinebestdeviceofa:orb:))
- [func setupPanel(DRSetupPanel!, deviceContainsSuitableMedia: DRDevice!, promptString: AutoreleasingUnsafeMutablePointer<NSString?>!) -> Bool](/documentation/objectivec/nsobject-swift.class/setuppanel(_:devicecontainssuitablemedia:promptstring:))
- [func setupPanel(DRSetupPanel!, deviceCouldBeTarget: DRDevice!) -> Bool](/documentation/objectivec/nsobject-swift.class/setuppanel(_:devicecouldbetarget:))
- [func setupPanelDeviceSelectionChanged(Notification!)](/documentation/objectivec/nsobject-swift.class/setuppaneldeviceselectionchanged(_:))
- [func setupPanelShouldHandleMediaReservations(DRSetupPanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/setuppanelshouldhandlemediareservations(_:))
- [func shouldEnableAction(for: ABPerson!, identifier: String!) -> Bool](/documentation/objectivec/nsobject-swift.class/shouldenableaction(for:identifier:))
- [func title(for: ABPerson!, identifier: String!) -> String!](/documentation/objectivec/nsobject-swift.class/title(for:identifier:))
- [func workflowController(AMWorkflowController, didError: any Error)](/documentation/objectivec/nsobject-swift.class/workflowcontroller(_:diderror:))
- [func workflowController(AMWorkflowController, didRun: AMAction)](/documentation/objectivec/nsobject-swift.class/workflowcontroller(_:didrun:))
- [func workflowController(AMWorkflowController, willRun: AMAction)](/documentation/objectivec/nsobject-swift.class/workflowcontroller(_:willrun:))
- [func workflowControllerDidRun(AMWorkflowController)](/documentation/objectivec/nsobject-swift.class/workflowcontrollerdidrun(_:))
- [func workflowControllerDidStop(AMWorkflowController)](/documentation/objectivec/nsobject-swift.class/workflowcontrollerdidstop(_:))
- [func workflowControllerWillRun(AMWorkflowController)](/documentation/objectivec/nsobject-swift.class/workflowcontrollerwillrun(_:))
- [func workflowControllerWillStop(AMWorkflowController)](/documentation/objectivec/nsobject-swift.class/workflowcontrollerwillstop(_:))

### Type Methods

- [class func debugDescription() -> String](/documentation/objectivec/nsobject-swift.class/debugdescription())
- [class func hash() -> Int](/documentation/objectivec/nsobject-swift.class/hash())

### Default Implementations

- [Equatable Implementations](/documentation/objectivec/nsobject-swift.class/equatable-implementations)

#### Operators

- [static func == (NSObject, NSObject) -> Bool](/documentation/objectivec/nsobject-swift.class/==(_:_:))
- [Hashable Implementations](/documentation/objectivec/nsobject-swift.class/hashable-implementations)

#### Instance Properties

- [var hashValue: Int](/documentation/objectivec/nsobject-swift.class/hashvalue)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/objectivec/nsobject-swift.class/hash(into:))
- [Protocol](/documentation/objectivec/protocol)

## Protocols

- [NSObjectProtocol](/documentation/objectivec/nsobjectprotocol)

### Identifying Classes

- [var superclass: AnyClass?](/documentation/objectivec/nsobjectprotocol/superclass)

### Identifying and Comparing Objects

- [func isEqual(Any?) -> Bool](/documentation/objectivec/nsobjectprotocol/isequal(_:))
- [var hash: Int](/documentation/objectivec/nsobjectprotocol/hash)
- [func `self`() -> Self](/documentation/objectivec/nsobjectprotocol/self())

### Testing Object Inheritance, Behavior, and Conformance

- [func isKind(of: AnyClass) -> Bool](/documentation/objectivec/nsobjectprotocol/iskind(of:))
- [func isMember(of: AnyClass) -> Bool](/documentation/objectivec/nsobjectprotocol/ismember(of:))
- [func responds(to: Selector!) -> Bool](/documentation/objectivec/nsobjectprotocol/responds(to:))
- [func conforms(to: Protocol) -> Bool](/documentation/objectivec/nsobjectprotocol/conforms(to:))

### Describing Objects

- [var description: String](/documentation/objectivec/nsobjectprotocol/description)
- [var debugDescription: String](/documentation/objectivec/nsobjectprotocol/debugdescription)

### Sending Messages

- [func perform(Selector!) -> Unmanaged<AnyObject>!](/documentation/objectivec/nsobjectprotocol/perform(_:))
- [func perform(Selector!, with: Any!) -> Unmanaged<AnyObject>!](/documentation/objectivec/nsobjectprotocol/perform(_:with:))
- [func perform(Selector!, with: Any!, with: Any!) -> Unmanaged<AnyObject>!](/documentation/objectivec/nsobjectprotocol/perform(_:with:with:))

### Identifying Proxies

- [func isProxy() -> Bool](/documentation/objectivec/nsobjectprotocol/isproxy())

## Reference

- [Objective-C Runtime](/documentation/objectivec/objective-c-runtime)

### Working with Classes

- [func class_getName(AnyClass?) -> UnsafePointer<CChar>](/documentation/objectivec/class_getname(_:))
- [func class_getSuperclass(AnyClass?) -> AnyClass?](/documentation/objectivec/class_getsuperclass(_:))
- [func class_setSuperclass(AnyClass, AnyClass) -> AnyClass](/documentation/objectivec/class_setsuperclass(_:_:))
- [func class_isMetaClass(AnyClass?) -> Bool](/documentation/objectivec/class_ismetaclass(_:))
- [func class_getInstanceSize(AnyClass?) -> Int](/documentation/objectivec/class_getinstancesize(_:))
- [func class_getInstanceVariable(AnyClass?, UnsafePointer<CChar>) -> Ivar?](/documentation/objectivec/class_getinstancevariable(_:_:))
- [func class_getClassVariable(AnyClass?, UnsafePointer<CChar>) -> Ivar?](/documentation/objectivec/class_getclassvariable(_:_:))
- [func class_addIvar(AnyClass?, UnsafePointer<CChar>, Int, UInt8, UnsafePointer<CChar>?) -> Bool](/documentation/objectivec/class_addivar(_:_:_:_:_:))
- [func class_copyIvarList(AnyClass?, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<Ivar>?](/documentation/objectivec/class_copyivarlist(_:_:))
- [func class_getIvarLayout(AnyClass?) -> UnsafePointer<UInt8>?](/documentation/objectivec/class_getivarlayout(_:))
- [func class_setIvarLayout(AnyClass?, UnsafePointer<UInt8>?)](/documentation/objectivec/class_setivarlayout(_:_:))
- [func class_getWeakIvarLayout(AnyClass?) -> UnsafePointer<UInt8>?](/documentation/objectivec/class_getweakivarlayout(_:))
- [func class_setWeakIvarLayout(AnyClass?, UnsafePointer<UInt8>?)](/documentation/objectivec/class_setweakivarlayout(_:_:))
- [func class_getProperty(AnyClass?, UnsafePointer<CChar>) -> objc_property_t?](/documentation/objectivec/class_getproperty(_:_:))
- [func class_copyPropertyList(AnyClass?, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<objc_property_t>?](/documentation/objectivec/class_copypropertylist(_:_:))
- [func class_addMethod(AnyClass?, Selector, IMP, UnsafePointer<CChar>?) -> Bool](/documentation/objectivec/class_addmethod(_:_:_:_:))
- [func class_getInstanceMethod(AnyClass?, Selector) -> Method?](/documentation/objectivec/class_getinstancemethod(_:_:))
- [func class_getClassMethod(AnyClass?, Selector) -> Method?](/documentation/objectivec/class_getclassmethod(_:_:))
- [func class_copyMethodList(AnyClass?, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<Method>?](/documentation/objectivec/class_copymethodlist(_:_:))
- [func class_replaceMethod(AnyClass?, Selector, IMP, UnsafePointer<CChar>?) -> IMP?](/documentation/objectivec/class_replacemethod(_:_:_:_:))
- [func class_getMethodImplementation(AnyClass?, Selector) -> IMP?](/documentation/objectivec/class_getmethodimplementation(_:_:))
- [func class_getMethodImplementation_stret(AnyClass?, Selector) -> IMP?](/documentation/objectivec/class_getmethodimplementation_stret(_:_:))
- [func class_respondsToSelector(AnyClass?, Selector) -> Bool](/documentation/objectivec/class_respondstoselector(_:_:))
- [func class_addProtocol(AnyClass?, Protocol) -> Bool](/documentation/objectivec/class_addprotocol(_:_:))
- [func class_addProperty(AnyClass?, UnsafePointer<CChar>, UnsafePointer<objc_property_attribute_t>?, UInt32) -> Bool](/documentation/objectivec/class_addproperty(_:_:_:_:))
- [func class_replaceProperty(AnyClass?, UnsafePointer<CChar>, UnsafePointer<objc_property_attribute_t>?, UInt32)](/documentation/objectivec/class_replaceproperty(_:_:_:_:))
- [func class_conformsToProtocol(AnyClass?, Protocol?) -> Bool](/documentation/objectivec/class_conformstoprotocol(_:_:))
- [func class_copyProtocolList(AnyClass?, UnsafeMutablePointer<UInt32>?) -> AutoreleasingUnsafeMutablePointer<Protocol>?](/documentation/objectivec/class_copyprotocollist(_:_:))
- [func class_getVersion(AnyClass?) -> Int32](/documentation/objectivec/class_getversion(_:))
- [func class_setVersion(AnyClass?, Int32)](/documentation/objectivec/class_setversion(_:_:))
- [objc_setFutureClass](/documentation/objectivec/1808430-objc_setfutureclass)

### Adding Classes

- [func objc_allocateClassPair(AnyClass?, UnsafePointer<CChar>, Int) -> AnyClass?](/documentation/objectivec/objc_allocateclasspair(_:_:_:))
- [func objc_disposeClassPair(AnyClass)](/documentation/objectivec/objc_disposeclasspair(_:))
- [func objc_registerClassPair(AnyClass)](/documentation/objectivec/objc_registerclasspair(_:))
- [func objc_duplicateClass(AnyClass, UnsafePointer<CChar>, Int) -> AnyClass](/documentation/objectivec/objc_duplicateclass(_:_:_:))

### Instantiating Classes

- [func class_createInstance(AnyClass?, Int) -> Any?](/documentation/objectivec/class_createinstance(_:_:))

### Working with Instances

- [func object_getIndexedIvars(Any?) -> UnsafeMutableRawPointer?](/documentation/objectivec/object_getindexedivars(_:))
- [func object_getIvar(Any?, Ivar) -> Any?](/documentation/objectivec/object_getivar(_:_:))
- [func object_setIvar(Any?, Ivar, Any?)](/documentation/objectivec/object_setivar(_:_:_:))
- [func object_getClassName(Any?) -> UnsafePointer<CChar>](/documentation/objectivec/object_getclassname(_:))
- [func object_getClass(Any?) -> AnyClass?](/documentation/objectivec/object_getclass(_:))
- [func object_setClass(Any?, AnyClass) -> AnyClass?](/documentation/objectivec/object_setclass(_:_:))

### Obtaining Class Definitions

- [func objc_getClassList(AutoreleasingUnsafeMutablePointer<AnyClass>?, Int32) -> Int32](/documentation/objectivec/objc_getclasslist(_:_:))
- [func objc_copyClassList(UnsafeMutablePointer<UInt32>?) -> AutoreleasingUnsafeMutablePointer<AnyClass>?](/documentation/objectivec/objc_copyclasslist(_:))
- [func objc_lookUpClass(UnsafePointer<CChar>) -> AnyClass?](/documentation/objectivec/objc_lookupclass(_:))
- [func objc_getClass(UnsafePointer<CChar>) -> Any!](/documentation/objectivec/objc_getclass(_:))
- [func objc_getRequiredClass(UnsafePointer<CChar>) -> AnyClass](/documentation/objectivec/objc_getrequiredclass(_:))
- [func objc_getMetaClass(UnsafePointer<CChar>) -> Any!](/documentation/objectivec/objc_getmetaclass(_:))

### Working with Instance Variables

- [func ivar_getName(Ivar) -> UnsafePointer<CChar>?](/documentation/objectivec/ivar_getname(_:))
- [func ivar_getTypeEncoding(Ivar) -> UnsafePointer<CChar>?](/documentation/objectivec/ivar_gettypeencoding(_:))
- [func ivar_getOffset(Ivar) -> Int](/documentation/objectivec/ivar_getoffset(_:))

### Associative References

- [func objc_setAssociatedObject(Any, UnsafeRawPointer, Any?, objc_AssociationPolicy)](/documentation/objectivec/objc_setassociatedobject(_:_:_:_:))
- [func objc_getAssociatedObject(Any, UnsafeRawPointer) -> Any?](/documentation/objectivec/objc_getassociatedobject(_:_:))
- [func objc_removeAssociatedObjects(Any)](/documentation/objectivec/objc_removeassociatedobjects(_:))

### Working with Methods

- [func method_getName(Method) -> Selector](/documentation/objectivec/method_getname(_:))
- [func method_getImplementation(Method) -> IMP](/documentation/objectivec/method_getimplementation(_:))
- [func method_getTypeEncoding(Method) -> UnsafePointer<CChar>?](/documentation/objectivec/method_gettypeencoding(_:))
- [func method_copyReturnType(Method) -> UnsafeMutablePointer<CChar>](/documentation/objectivec/method_copyreturntype(_:))
- [func method_copyArgumentType(Method, UInt32) -> UnsafeMutablePointer<CChar>?](/documentation/objectivec/method_copyargumenttype(_:_:))
- [func method_getReturnType(Method, UnsafeMutablePointer<CChar>, Int)](/documentation/objectivec/method_getreturntype(_:_:_:))
- [func method_getNumberOfArguments(Method) -> UInt32](/documentation/objectivec/method_getnumberofarguments(_:))
- [func method_getArgumentType(Method, UInt32, UnsafeMutablePointer<CChar>?, Int)](/documentation/objectivec/method_getargumenttype(_:_:_:_:))
- [func method_getDescription(Method) -> UnsafeMutablePointer<objc_method_description>](/documentation/objectivec/method_getdescription(_:))
- [func method_setImplementation(Method, IMP) -> IMP](/documentation/objectivec/method_setimplementation(_:_:))
- [func method_exchangeImplementations(Method, Method)](/documentation/objectivec/method_exchangeimplementations(_:_:))

### Working with Libraries

- [func objc_copyImageNames(UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<UnsafePointer<CChar>>](/documentation/objectivec/objc_copyimagenames(_:))
- [func class_getImageName(AnyClass?) -> UnsafePointer<CChar>?](/documentation/objectivec/class_getimagename(_:))
- [func objc_copyClassNamesForImage(UnsafePointer<CChar>, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<UnsafePointer<CChar>>?](/documentation/objectivec/objc_copyclassnamesforimage(_:_:))

### Working with Selectors

- [func sel_getName(Selector) -> UnsafePointer<CChar>](/documentation/objectivec/sel_getname(_:))
- [func sel_registerName(UnsafePointer<CChar>) -> Selector](/documentation/objectivec/sel_registername(_:))
- [func sel_getUid(UnsafePointer<CChar>) -> Selector](/documentation/objectivec/sel_getuid(_:))
- [func sel_isEqual(Selector, Selector) -> Bool](/documentation/objectivec/sel_isequal(_:_:))

### Working with Protocols

- [func objc_getProtocol(UnsafePointer<CChar>) -> Protocol?](/documentation/objectivec/objc_getprotocol(_:))
- [func objc_copyProtocolList(UnsafeMutablePointer<UInt32>?) -> AutoreleasingUnsafeMutablePointer<Protocol>?](/documentation/objectivec/objc_copyprotocollist(_:))
- [func objc_allocateProtocol(UnsafePointer<CChar>) -> Protocol?](/documentation/objectivec/objc_allocateprotocol(_:))
- [func objc_registerProtocol(Protocol)](/documentation/objectivec/objc_registerprotocol(_:))
- [func protocol_addMethodDescription(Protocol, Selector, UnsafePointer<CChar>?, Bool, Bool)](/documentation/objectivec/protocol_addmethoddescription(_:_:_:_:_:))
- [func protocol_addProtocol(Protocol, Protocol)](/documentation/objectivec/protocol_addprotocol(_:_:))
- [func protocol_addProperty(Protocol, UnsafePointer<CChar>, UnsafePointer<objc_property_attribute_t>?, UInt32, Bool, Bool)](/documentation/objectivec/protocol_addproperty(_:_:_:_:_:_:))
- [func protocol_getName(Protocol) -> UnsafePointer<CChar>](/documentation/objectivec/protocol_getname(_:))
- [func protocol_isEqual(Protocol?, Protocol?) -> Bool](/documentation/objectivec/protocol_isequal(_:_:))
- [func protocol_copyMethodDescriptionList(Protocol, Bool, Bool, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<objc_method_description>?](/documentation/objectivec/protocol_copymethoddescriptionlist(_:_:_:_:))
- [func protocol_getMethodDescription(Protocol, Selector, Bool, Bool) -> objc_method_description](/documentation/objectivec/protocol_getmethoddescription(_:_:_:_:))
- [func protocol_copyPropertyList(Protocol, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<objc_property_t>?](/documentation/objectivec/protocol_copypropertylist(_:_:))
- [func protocol_getProperty(Protocol, UnsafePointer<CChar>, Bool, Bool) -> objc_property_t?](/documentation/objectivec/protocol_getproperty(_:_:_:_:))
- [func protocol_copyProtocolList(Protocol, UnsafeMutablePointer<UInt32>?) -> AutoreleasingUnsafeMutablePointer<Protocol>?](/documentation/objectivec/protocol_copyprotocollist(_:_:))
- [func protocol_conformsToProtocol(Protocol?, Protocol?) -> Bool](/documentation/objectivec/protocol_conformstoprotocol(_:_:))

### Working with Properties

- [func property_getName(objc_property_t) -> UnsafePointer<CChar>](/documentation/objectivec/property_getname(_:))
- [func property_getAttributes(objc_property_t) -> UnsafePointer<CChar>?](/documentation/objectivec/property_getattributes(_:))
- [func property_copyAttributeValue(objc_property_t, UnsafePointer<CChar>) -> UnsafeMutablePointer<CChar>?](/documentation/objectivec/property_copyattributevalue(_:_:))
- [func property_copyAttributeList(objc_property_t, UnsafeMutablePointer<UInt32>?) -> UnsafeMutablePointer<objc_property_attribute_t>?](/documentation/objectivec/property_copyattributelist(_:_:))

### Using Objective-C Language Features

- [func objc_enumerationMutation(Any)](/documentation/objectivec/objc_enumerationmutation(_:))
- [func objc_setEnumerationMutationHandler(((Any) -> Void)?)](/documentation/objectivec/objc_setenumerationmutationhandler(_:))
- [func imp_implementationWithBlock(Any) -> IMP](/documentation/objectivec/imp_implementationwithblock(_:))
- [func imp_getBlock(IMP) -> Any?](/documentation/objectivec/imp_getblock(_:))
- [func imp_removeBlock(IMP) -> Bool](/documentation/objectivec/imp_removeblock(_:))
- [func objc_loadWeak(AutoreleasingUnsafeMutablePointer<AnyObject?>) -> Any?](/documentation/objectivec/objc_loadweak(_:))
- [func objc_storeWeak(AutoreleasingUnsafeMutablePointer<AnyObject?>, Any?) -> Any?](/documentation/objectivec/objc_storeweak(_:_:))

### Class-Definition Data Structures

- [Method](/documentation/objectivec/method)
- [Ivar](/documentation/objectivec/ivar)
- [Category](/documentation/objectivec/category)
- [objc_property_t](/documentation/objectivec/objc_property_t)
- [IMP](/documentation/objectivec/imp)
- [objc_method_description](/documentation/objectivec/objc_method_description)

#### Fields

- [var name: Selector?](/documentation/objectivec/objc_method_description/name)
- [var types: UnsafeMutablePointer<CChar>?](/documentation/objectivec/objc_method_description/types)

#### Initializers

- [init()](/documentation/objectivec/objc_method_description/init())
- [init(name: Selector?, types: UnsafeMutablePointer<CChar>?)](/documentation/objectivec/objc_method_description/init(name:types:))
- [objc_cache](/documentation/objectivec/objc_cache)

#### Fields

- [mask](/documentation/objectivec/1808499-mask)
- [occupied](/documentation/objectivec/1808501-occupied)
- [buckets](/documentation/objectivec/1808503-buckets)
- [objc_property_attribute_t](/documentation/objectivec/objc_property_attribute_t)

#### Initializers

- [init(name: UnsafePointer<CChar>, value: UnsafePointer<CChar>)](/documentation/objectivec/objc_property_attribute_t/init(name:value:))

#### Instance Properties

- [var name: UnsafePointer<CChar>](/documentation/objectivec/objc_property_attribute_t/name)
- [var value: UnsafePointer<CChar>](/documentation/objectivec/objc_property_attribute_t/value)

### Instance Data Types

- [objc_object](/documentation/objectivec/objc_object)

#### Initializers

- [init(isa: AnyClass)](/documentation/objectivec/objc_object/init(isa:))

#### Instance Properties

- [var isa: AnyClass](/documentation/objectivec/objc_object/isa)
- [objc_super](/documentation/objectivec/objc_super-swift.struct)

#### Fields

- [var receiver: Unmanaged<AnyObject>](/documentation/objectivec/objc_super-swift.struct/receiver)
- [var super_class: AnyClass](/documentation/objectivec/objc_super-swift.struct/super_class)

#### Instance Properties

- [var receiver: Unmanaged<AnyObject>](/documentation/objectivec/objc_super-swift.struct/receiver)
- [var super_class: AnyClass](/documentation/objectivec/objc_super-swift.struct/super_class)

#### Initializers

- [init(receiver: Unmanaged<AnyObject>, super_class: AnyClass)](/documentation/objectivec/objc_super-swift.struct/init(receiver:super_class:))

### Associative References

- [objc_AssociationPolicy](/documentation/objectivec/objc_associationpolicy)

#### Enumeration Cases

- [case OBJC_ASSOCIATION_ASSIGN](/documentation/objectivec/objc_associationpolicy/objc_association_assign)
- [case OBJC_ASSOCIATION_COPY](/documentation/objectivec/objc_associationpolicy/objc_association_copy)
- [case OBJC_ASSOCIATION_COPY_NONATOMIC](/documentation/objectivec/objc_associationpolicy/objc_association_copy_nonatomic)
- [case OBJC_ASSOCIATION_RETAIN](/documentation/objectivec/objc_associationpolicy/objc_association_retain)
- [case OBJC_ASSOCIATION_RETAIN_NONATOMIC](/documentation/objectivec/objc_associationpolicy/objc_association_retain_nonatomic)

#### Initializers

- [init?(rawValue: UInt)](/documentation/objectivec/objc_associationpolicy/init(rawvalue:))
- [Objective-C Structures](/documentation/objectivec/objective-c-structures)

### Structures

- [NSZone](/documentation/objectivec/nszone)
- [NXHashTablePrototype](/documentation/objectivec/nxhashtableprototype)

#### Initializers

- [init(hash: (UnsafeRawPointer?, UnsafeRawPointer?) -> UInt, isEqual: (UnsafeRawPointer?, UnsafeRawPointer?, UnsafeRawPointer?) -> Int32, free: (UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void, style: Int32)](/documentation/objectivec/nxhashtableprototype/init(hash:isequal:free:style:))

#### Instance Properties

- [var free: (UnsafeRawPointer?, UnsafeMutableRawPointer?) -> Void](/documentation/objectivec/nxhashtableprototype/free)
- [var hash: (UnsafeRawPointer?, UnsafeRawPointer?) -> UInt](/documentation/objectivec/nxhashtableprototype/hash)
- [var isEqual: (UnsafeRawPointer?, UnsafeRawPointer?, UnsafeRawPointer?) -> Int32](/documentation/objectivec/nxhashtableprototype/isequal)
- [var style: Int32](/documentation/objectivec/nxhashtableprototype/style)
- [ObjCBool](/documentation/objectivec/objcbool)

#### Initializers

- [init(Bool)](/documentation/objectivec/objcbool/init(_:))
- [init(booleanLiteral: Bool)](/documentation/objectivec/objcbool/init(booleanliteral:))

#### Instance Properties

- [var boolValue: Bool](/documentation/objectivec/objcbool/boolvalue)

#### Default Implementations

- [CustomReflectable Implementations](/documentation/objectivec/objcbool/customreflectable-implementations)

##### Instance Properties

- [var customMirror: Mirror](/documentation/objectivec/objcbool/custommirror)
- [CustomStringConvertible Implementations](/documentation/objectivec/objcbool/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/objectivec/objcbool/description)
- [ObjCClassList](/documentation/objectivec/objcclasslist)
- [Selector](/documentation/objectivec/selector)

#### Initializers

- [init(String)](/documentation/objectivec/selector/init(_:))
- [init(stringLiteral: String)](/documentation/objectivec/selector/init(stringliteral:))

#### Default Implementations

- [CustomReflectable Implementations](/documentation/objectivec/selector/customreflectable-implementations)

##### Instance Properties

- [var customMirror: Mirror](/documentation/objectivec/selector/custommirror)
- [CustomStringConvertible Implementations](/documentation/objectivec/selector/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/objectivec/selector/description)
- [objc_method_description](/documentation/objectivec/objc_method_description)

#### Fields

- [var name: Selector?](/documentation/objectivec/objc_method_description/name)
- [var types: UnsafeMutablePointer<CChar>?](/documentation/objectivec/objc_method_description/types)

#### Initializers

- [init()](/documentation/objectivec/objc_method_description/init())
- [init(name: Selector?, types: UnsafeMutablePointer<CChar>?)](/documentation/objectivec/objc_method_description/init(name:types:))
- [objc_object](/documentation/objectivec/objc_object)

#### Initializers

- [init(isa: AnyClass)](/documentation/objectivec/objc_object/init(isa:))

#### Instance Properties

- [var isa: AnyClass](/documentation/objectivec/objc_object/isa)
- [objc_property_attribute_t](/documentation/objectivec/objc_property_attribute_t)

#### Initializers

- [init(name: UnsafePointer<CChar>, value: UnsafePointer<CChar>)](/documentation/objectivec/objc_property_attribute_t/init(name:value:))

#### Instance Properties

- [var name: UnsafePointer<CChar>](/documentation/objectivec/objc_property_attribute_t/name)
- [var value: UnsafePointer<CChar>](/documentation/objectivec/objc_property_attribute_t/value)
- [objc_super](/documentation/objectivec/objc_super-swift.struct)

#### Fields

- [var receiver: Unmanaged<AnyObject>](/documentation/objectivec/objc_super-swift.struct/receiver)
- [var super_class: AnyClass](/documentation/objectivec/objc_super-swift.struct/super_class)

#### Instance Properties

- [var receiver: Unmanaged<AnyObject>](/documentation/objectivec/objc_super-swift.struct/receiver)
- [var super_class: AnyClass](/documentation/objectivec/objc_super-swift.struct/super_class)

#### Initializers

- [init(receiver: Unmanaged<AnyObject>, super_class: AnyClass)](/documentation/objectivec/objc_super-swift.struct/init(receiver:super_class:))
- [Objective-C Constants](/documentation/objectivec/objective-c-constants)

### Constants

- [var NSIntegerMax: Int](/documentation/objectivec/nsintegermax)
- [var NS_ENFORCE_NSOBJECT_DESIGNATED_INITIALIZER: Int32](/documentation/objectivec/ns_enforce_nsobject_designated_initializer)
- [var OBJC_BOOL_IS_BOOL: Int32](/documentation/objectivec/objc_bool_is_bool)
- [var OBJC_BOOL_IS_CHAR: Int32](/documentation/objectivec/objc_bool_is_char)
- [var OBJC_NO_GC_API: Int32](/documentation/objectivec/objc_no_gc_api)
- [var OBJC_OLD_DISPATCH_PROTOTYPES: Int32](/documentation/objectivec/objc_old_dispatch_prototypes)
- [var OBJC_ADDLOADIMAGEFUNC_DEFINED: Int32](/documentation/objectivec/objc_addloadimagefunc_defined)
- [var OBJC_GETCLASSHOOK_DEFINED: Int32](/documentation/objectivec/objc_getclasshook_defined)
- [var OBJC_REALIZECLASSFROMSWIFT_DEFINED: Int32](/documentation/objectivec/objc_realizeclassfromswift_defined)
- [var OBJC_SETHOOK_LAZYCLASSNAMER_DEFINED: Int32](/documentation/objectivec/objc_sethook_lazyclassnamer_defined)
- [Objective-C Functions](/documentation/objectivec/objective-c-functions)

### Functions

- [func autoreleasepool<E, Result>(invoking: () throws(E) -> Result) throws(E) -> Result](/documentation/objectivec/autoreleasepool(invoking:))
- [func class_lookupMethod(AnyClass?, Selector) -> IMP?](/documentation/objectivec/class_lookupmethod(_:_:))
- [func class_respondsToMethod(AnyClass?, Selector) -> Bool](/documentation/objectivec/class_respondstomethod(_:_:))
- [func objc_addExceptionHandler(objc_exception_handler, UnsafeMutableRawPointer?) -> UInt](/documentation/objectivec/objc_addexceptionhandler(_:_:))
- [func objc_addLoadImageFunc(objc_func_loadImage)](/documentation/objectivec/objc_addloadimagefunc(_:))
- [func objc_assertRegisteredThreadWithCollector()](/documentation/objectivec/objc_assertregisteredthreadwithcollector())
- [func objc_begin_catch(UnsafeMutableRawPointer) -> Any](/documentation/objectivec/objc_begin_catch(_:))
- [func objc_clear_stack(UInt)](/documentation/objectivec/objc_clear_stack(_:))
- [func objc_collect(UInt)](/documentation/objectivec/objc_collect(_:))
- [func objc_collectableZone() -> objc_zone_t!](/documentation/objectivec/objc_collectablezone())
- [func objc_collecting_enabled() -> Bool](/documentation/objectivec/objc_collecting_enabled())
- [func objc_collectingEnabled() -> Bool](/documentation/objectivec/objc_collectingenabled())
- [func objc_end_catch()](/documentation/objectivec/objc_end_catch())
- [func objc_enumerateClasses(fromImage: ObjCEnumerationImage, matchingNamePrefix: String?, conformingTo: Protocol?, subclassing: AnyClass?) -> ObjCClassList](/documentation/objectivec/objc_enumerateclasses(fromimage:matchingnameprefix:conformingto:subclassing:))
- [func objc_exception_rethrow() -> Never](/documentation/objectivec/objc_exception_rethrow())
- [func objc_exception_throw(Any) -> Never](/documentation/objectivec/objc_exception_throw(_:))
- [func objc_finalizeOnMainThread(AnyClass!)](/documentation/objectivec/objc_finalizeonmainthread(_:))
- [func objc_is_finalized(UnsafeMutableRawPointer!) -> Bool](/documentation/objectivec/objc_is_finalized(_:))
- [func objc_memmove_collectable(UnsafeMutableRawPointer!, UnsafeRawPointer!, Int) -> UnsafeMutableRawPointer!](/documentation/objectivec/objc_memmove_collectable(_:_:_:))
- [func objc_registerThreadWithCollector()](/documentation/objectivec/objc_registerthreadwithcollector())
- [func objc_removeExceptionHandler(UInt)](/documentation/objectivec/objc_removeexceptionhandler(_:))
- [func objc_set_collection_ratio(Int)](/documentation/objectivec/objc_set_collection_ratio(_:))
- [func objc_set_collection_threshold(Int)](/documentation/objectivec/objc_set_collection_threshold(_:))
- [func objc_setCollectionRatio(Int)](/documentation/objectivec/objc_setcollectionratio(_:))
- [func objc_setCollectionThreshold(Int)](/documentation/objectivec/objc_setcollectionthreshold(_:))
- [func objc_setExceptionMatcher(objc_exception_matcher) -> objc_exception_matcher](/documentation/objectivec/objc_setexceptionmatcher(_:))
- [func objc_setExceptionPreprocessor(objc_exception_preprocessor) -> objc_exception_preprocessor](/documentation/objectivec/objc_setexceptionpreprocessor(_:))
- [func objc_setForwardHandler(UnsafeMutableRawPointer, UnsafeMutableRawPointer)](/documentation/objectivec/objc_setforwardhandler(_:_:))
- [func objc_setHook_getClass(objc_hook_getClass, UnsafeMutablePointer<objc_hook_getClass?>)](/documentation/objectivec/objc_sethook_getclass(_:_:))
- [func objc_setHook_getImageName(objc_hook_getImageName, UnsafeMutablePointer<objc_hook_getImageName?>)](/documentation/objectivec/objc_sethook_getimagename(_:_:))
- [func objc_setHook_lazyClassNamer(objc_hook_lazyClassNamer, UnsafeMutablePointer<objc_hook_lazyClassNamer>)](/documentation/objectivec/objc_sethook_lazyclassnamer(_:_:))
- [func objc_setUncaughtExceptionHandler(objc_uncaught_exception_handler) -> objc_uncaught_exception_handler](/documentation/objectivec/objc_setuncaughtexceptionhandler(_:))
- [func objc_start_collector_thread()](/documentation/objectivec/objc_start_collector_thread())
- [func objc_startCollectorThread()](/documentation/objectivec/objc_startcollectorthread())
- [func objc_terminate() -> Never](/documentation/objectivec/objc_terminate())
- [func objc_unregisterThreadWithCollector()](/documentation/objectivec/objc_unregisterthreadwithcollector())
- [func object_isClass(Any?) -> Bool](/documentation/objectivec/object_isclass(_:))
- [func object_setIvarWithStrongDefault(Any?, Ivar, Any?)](/documentation/objectivec/object_setivarwithstrongdefault(_:_:_:))
- [func protocol_copyPropertyList2(Protocol, UnsafeMutablePointer<UInt32>?, Bool, Bool) -> UnsafeMutablePointer<objc_property_t>?](/documentation/objectivec/protocol_copypropertylist2(_:_:_:_:))
- [func sel_isMapped(Selector) -> Bool](/documentation/objectivec/sel_ismapped(_:))
- [Objective-C Data Types](/documentation/objectivec/objective-c-data-types)

### Data Types

- [NSInteger](/documentation/objectivec/nsinteger)

#### Constants

- [var NSIntegerMax: Int](/documentation/objectivec/nsintegermax)
- [objc_exception_handler](/documentation/objectivec/objc_exception_handler)
- [objc_exception_matcher](/documentation/objectivec/objc_exception_matcher)
- [objc_exception_preprocessor](/documentation/objectivec/objc_exception_preprocessor)
- [objc_func_loadImage](/documentation/objectivec/objc_func_loadimage)
- [objc_hook_getClass](/documentation/objectivec/objc_hook_getclass)
- [objc_hook_getImageName](/documentation/objectivec/objc_hook_getimagename)
- [objc_hook_lazyClassNamer](/documentation/objectivec/objc_hook_lazyclassnamer)
- [objc_objectptr_t](/documentation/objectivec/objc_objectptr_t)
- [objc_uncaught_exception_handler](/documentation/objectivec/objc_uncaught_exception_handler)
- [objc_zone_t](/documentation/objectivec/objc_zone_t)
- [Objective-C Macros](/documentation/objectivec/objective-c-macros)

### Macros

- [var OBJC_API_VERSION: Int32](/documentation/objectivec/objc_api_version)
- [var OBJC_NO_GC: Int32](/documentation/objectivec/objc_no_gc)
- [Objective-C Enumerations](/documentation/objectivec/objective-c-enums)

### Enumerations

- [ObjCEnumerationImage](/documentation/objectivec/objcenumerationimage)

#### Enumeration Cases

- [case dynamicClasses](/documentation/objectivec/objcenumerationimage/dynamicclasses)
- [case image(UnsafeRawPointer)](/documentation/objectivec/objcenumerationimage/image(_:))
- [case machHeader(UnsafeRawPointer)](/documentation/objectivec/objcenumerationimage/machheader(_:))
- [var OBJC_CLEAR_RESIDENT_STACK: Int](/documentation/objectivec/objc_clear_resident_stack)
- [var OBJC_COLLECT_IF_NEEDED: Int](/documentation/objectivec/objc_collect_if_needed)
- [var OBJC_EXHAUSTIVE_COLLECTION: Int](/documentation/objectivec/objc_exhaustive_collection)
- [var OBJC_FULL_COLLECTION: Int](/documentation/objectivec/objc_full_collection)
- [var OBJC_GENERATIONAL_COLLECTION: Int](/documentation/objectivec/objc_generational_collection)
- [var OBJC_RATIO_COLLECTION: Int](/documentation/objectivec/objc_ratio_collection)
- [var OBJC_SYNC_NOT_OWNING_THREAD_ERROR: Int](/documentation/objectivec/objc_sync_not_owning_thread_error)
- [var OBJC_SYNC_SUCCESS: Int](/documentation/objectivec/objc_sync_success)
- [var OBJC_WAIT_UNTIL_DONE: Int](/documentation/objectivec/objc_wait_until_done)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
