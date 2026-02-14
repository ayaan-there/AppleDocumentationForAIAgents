# JavaScriptCore Documentation

Source: https://sosumi.ai/documentation/javascriptcore

---
title: JavaScriptCore
source: https://developer.apple.com/documentation/javascriptcore
timestamp: 2026-02-13T18:58:33.070Z
---

## Execution Environment

- [JSVirtualMachine](/documentation/javascriptcore/jsvirtualmachine)

### Creating a JavaScript Virtual Machine

- [init!()](/documentation/javascriptcore/jsvirtualmachine/init())

### Managing Memory for Bridged Values

- [func addManagedReference(Any!, withOwner: Any!)](/documentation/javascriptcore/jsvirtualmachine/addmanagedreference(_:withowner:))
- [func removeManagedReference(Any!, withOwner: Any!)](/documentation/javascriptcore/jsvirtualmachine/removemanagedreference(_:withowner:))
- [JSContext](/documentation/javascriptcore/jscontext)

### Creating JavaScript contexts

- [init!()](/documentation/javascriptcore/jscontext/init())
- [init!(virtualMachine: JSVirtualMachine!)](/documentation/javascriptcore/jscontext/init(virtualmachine:))

### Making JavaScript context inspectable

- [var isInspectable: Bool](/documentation/javascriptcore/jscontext/isinspectable)

#### Related Documentation

- [var name: String!](/documentation/javascriptcore/jscontext/name)

### Evaluating scripts

- [func evaluateScript(String!) -> JSValue!](/documentation/javascriptcore/jscontext/evaluatescript(_:))
- [func evaluateScript(String!, withSourceURL: URL!) -> JSValue!](/documentation/javascriptcore/jscontext/evaluatescript(_:withsourceurl:))

### Inspecting callback state in a running context

- [class func current() -> JSContext!](/documentation/javascriptcore/jscontext/current())
- [class func currentCallee() -> JSValue!](/documentation/javascriptcore/jscontext/currentcallee())
- [class func currentThis() -> JSValue!](/documentation/javascriptcore/jscontext/currentthis())
- [class func currentArguments() -> [Any]!](/documentation/javascriptcore/jscontext/currentarguments())

### Working with JavaScript global state

- [var globalObject: JSValue!](/documentation/javascriptcore/jscontext/globalobject)
- [var exception: JSValue!](/documentation/javascriptcore/jscontext/exception)
- [var exceptionHandler: ((JSContext?, JSValue?) -> Void)!](/documentation/javascriptcore/jscontext/exceptionhandler)
- [var virtualMachine: JSVirtualMachine!](/documentation/javascriptcore/jscontext/virtualmachine)
- [var name: String!](/documentation/javascriptcore/jscontext/name)

### Accessing JavaScript global state with subscripts

- [func objectForKeyedSubscript(Any!) -> JSValue!](/documentation/javascriptcore/jscontext/objectforkeyedsubscript(_:))
- [func setObject(Any!, forKeyedSubscript: (any NSCopying & NSObjectProtocol)!)](/documentation/javascriptcore/jscontext/setobject(_:forkeyedsubscript:))

### Working with the C JavaScriptCore API

- [var jsGlobalContextRef: JSGlobalContextRef!](/documentation/javascriptcore/jscontext/jsglobalcontextref)
- [init!(JSGlobalContextRef: JSGlobalContextRef!)](/documentation/javascriptcore/jscontext/init(jsglobalcontextref:))

## JavaScript Code

- [JSValue](/documentation/javascriptcore/jsvalue)

### Creating JavaScript Values

- [init!(object: Any!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(object:in:))
- [init!(bool: Bool, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(bool:in:))
- [init!(double: Double, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(double:in:))
- [init!(int32: Int32, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(int32:in:))
- [init!(uInt32: UInt32, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(uint32:in:))
- [init!(newObjectIn: JSContext!)](/documentation/javascriptcore/jsvalue/init(newobjectin:))
- [init!(newArrayIn: JSContext!)](/documentation/javascriptcore/jsvalue/init(newarrayin:))
- [init!(newRegularExpressionFromPattern: String!, flags: String!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(newregularexpressionfrompattern:flags:in:))
- [init!(newErrorFromMessage: String!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(newerrorfrommessage:in:))
- [init!(undefinedIn: JSContext!)](/documentation/javascriptcore/jsvalue/init(undefinedin:))
- [init!(nullIn: JSContext!)](/documentation/javascriptcore/jsvalue/init(nullin:))
- [init!(point: CGPoint, inContext: JSContext!)](/documentation/javascriptcore/jsvalue/init(point:incontext:))
- [init!(range: NSRange, inContext: JSContext!)](/documentation/javascriptcore/jsvalue/init(range:incontext:))
- [init!(rect: CGRect, inContext: JSContext!)](/documentation/javascriptcore/jsvalue/init(rect:incontext:))
- [init!(size: CGSize, inContext: JSContext!)](/documentation/javascriptcore/jsvalue/init(size:incontext:))
- [init!(newSymbolFromDescription: String!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(newsymbolfromdescription:in:))
- [init!(newPromiseIn: JSContext!, fromExecutor: ((JSValue?, JSValue?) -> Void)!)](/documentation/javascriptcore/jsvalue/init(newpromisein:fromexecutor:))
- [init!(newPromiseRejectedWithReason: Any!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(newpromiserejectedwithreason:in:))
- [init!(newPromiseResolvedWithResult: Any!, in: JSContext!)](/documentation/javascriptcore/jsvalue/init(newpromiseresolvedwithresult:in:))

### Reading and Converting JavaScript Values

- [func toObject() -> Any!](/documentation/javascriptcore/jsvalue/toobject())
- [func toObjectOf(AnyClass!) -> Any!](/documentation/javascriptcore/jsvalue/toobjectof(_:))
- [func toBool() -> Bool](/documentation/javascriptcore/jsvalue/tobool())
- [func toDouble() -> Double](/documentation/javascriptcore/jsvalue/todouble())
- [func toInt32() -> Int32](/documentation/javascriptcore/jsvalue/toint32())
- [func toUInt32() -> UInt32](/documentation/javascriptcore/jsvalue/touint32())
- [func toNumber() -> NSNumber!](/documentation/javascriptcore/jsvalue/tonumber())
- [func toString() -> String!](/documentation/javascriptcore/jsvalue/tostring())
- [func toDate() -> Date!](/documentation/javascriptcore/jsvalue/todate())
- [func toArray() -> [Any]!](/documentation/javascriptcore/jsvalue/toarray())
- [func toDictionary() -> [AnyHashable : Any]!](/documentation/javascriptcore/jsvalue/todictionary())
- [func toPoint() -> CGPoint](/documentation/javascriptcore/jsvalue/topoint())
- [func toRange() -> NSRange](/documentation/javascriptcore/jsvalue/torange())
- [func toRect() -> CGRect](/documentation/javascriptcore/jsvalue/torect())
- [func toSize() -> CGSize](/documentation/javascriptcore/jsvalue/tosize())

### Determining the Type of a JavaScript Value

- [var isUndefined: Bool](/documentation/javascriptcore/jsvalue/isundefined)
- [var isNull: Bool](/documentation/javascriptcore/jsvalue/isnull)
- [var isBoolean: Bool](/documentation/javascriptcore/jsvalue/isboolean)
- [var isNumber: Bool](/documentation/javascriptcore/jsvalue/isnumber)
- [var isString: Bool](/documentation/javascriptcore/jsvalue/isstring)
- [var isObject: Bool](/documentation/javascriptcore/jsvalue/isobject)
- [var isArray: Bool](/documentation/javascriptcore/jsvalue/isarray)
- [var isDate: Bool](/documentation/javascriptcore/jsvalue/isdate)
- [var isSymbol: Bool](/documentation/javascriptcore/jsvalue/issymbol)

### Comparing JavaScript Values

- [func isEqual(to: Any!) -> Bool](/documentation/javascriptcore/jsvalue/isequal(to:))
- [func isEqualWithTypeCoercion(to: Any!) -> Bool](/documentation/javascriptcore/jsvalue/isequalwithtypecoercion(to:))
- [func isInstance(of: Any!) -> Bool](/documentation/javascriptcore/jsvalue/isinstance(of:))

### Working with Function and Constructor Values

- [func call(withArguments: [Any]!) -> JSValue!](/documentation/javascriptcore/jsvalue/call(witharguments:))
- [func construct(withArguments: [Any]!) -> JSValue!](/documentation/javascriptcore/jsvalue/construct(witharguments:))
- [func invokeMethod(String!, withArguments: [Any]!) -> JSValue!](/documentation/javascriptcore/jsvalue/invokemethod(_:witharguments:))

### Working with Container Values

- [func defineProperty(Any!, descriptor: Any!)](/documentation/javascriptcore/jsvalue/defineproperty(_:descriptor:))
- [func hasProperty(Any!) -> Bool](/documentation/javascriptcore/jsvalue/hasproperty(_:))
- [func deleteProperty(Any!) -> Bool](/documentation/javascriptcore/jsvalue/deleteproperty(_:))
- [func atIndex(Int) -> JSValue!](/documentation/javascriptcore/jsvalue/atindex(_:))

#### Related Documentation

- [func objectAtIndexedSubscript(Int) -> JSValue!](/documentation/javascriptcore/jsvalue/objectatindexedsubscript(_:))
- [func setValue(Any!, at: Int)](/documentation/javascriptcore/jsvalue/setvalue(_:at:))

#### Related Documentation

- [func setObject(Any!, atIndexedSubscript: Int)](/documentation/javascriptcore/jsvalue/setobject(_:atindexedsubscript:))
- [func forProperty(Any!) -> JSValue!](/documentation/javascriptcore/jsvalue/forproperty(_:))

#### Related Documentation

- [func objectForKeyedSubscript(Any!) -> JSValue!](/documentation/javascriptcore/jsvalue/objectforkeyedsubscript(_:))
- [func setValue(Any!, forProperty: Any!)](/documentation/javascriptcore/jsvalue/setvalue(_:forproperty:))

#### Related Documentation

- [func setObject(Any!, forKeyedSubscript: Any!)](/documentation/javascriptcore/jsvalue/setobject(_:forkeyedsubscript:))
- [JSValueProperty](/documentation/javascriptcore/jsvalueproperty)

### Accessing a Value’s JavaScript Context

- [var context: JSContext!](/documentation/javascriptcore/jsvalue/context)

### Accessing Values with Subscript Syntax

- [func objectAtIndexedSubscript(Int) -> JSValue!](/documentation/javascriptcore/jsvalue/objectatindexedsubscript(_:))
- [func setObject(Any!, atIndexedSubscript: Int)](/documentation/javascriptcore/jsvalue/setobject(_:atindexedsubscript:))
- [func objectForKeyedSubscript(Any!) -> JSValue!](/documentation/javascriptcore/jsvalue/objectforkeyedsubscript(_:))
- [func setObject(Any!, forKeyedSubscript: Any!)](/documentation/javascriptcore/jsvalue/setobject(_:forkeyedsubscript:))

### Working with the C JavaScriptCore API

- [var jsValueRef: JSValueRef!](/documentation/javascriptcore/jsvalue/jsvalueref)
- [init!(JSValueRef: JSValueRef!, inContext: JSContext!)](/documentation/javascriptcore/jsvalue/init(jsvalueref:incontext:))

### Constants

- [Property Descriptor Keys](/documentation/javascriptcore/property-descriptor-keys)

#### Constants

- [let JSPropertyDescriptorWritableKey: String](/documentation/javascriptcore/jspropertydescriptorwritablekey)
- [let JSPropertyDescriptorEnumerableKey: String](/documentation/javascriptcore/jspropertydescriptorenumerablekey)
- [let JSPropertyDescriptorConfigurableKey: String](/documentation/javascriptcore/jspropertydescriptorconfigurablekey)
- [let JSPropertyDescriptorValueKey: String](/documentation/javascriptcore/jspropertydescriptorvaluekey)
- [let JSPropertyDescriptorGetKey: String](/documentation/javascriptcore/jspropertydescriptorgetkey)
- [let JSPropertyDescriptorSetKey: String](/documentation/javascriptcore/jspropertydescriptorsetkey)

### Initializers

- [init?(newBigIntFrom: String, in: JSContext)](/documentation/javascriptcore/jsvalue/init(newbigintfrom:in:)-1f0xs)
- [init?(newBigIntFrom: UInt64, in: JSContext)](/documentation/javascriptcore/jsvalue/init(newbigintfrom:in:)-7worq)
- [init?(newBigIntFrom: Int64, in: JSContext)](/documentation/javascriptcore/jsvalue/init(newbigintfrom:in:)-8l9iv)
- [init?(newBigIntFrom: Double, in: JSContext)](/documentation/javascriptcore/jsvalue/init(newbigintfrom:in:)-r38z)

### Instance Properties

- [var isBigInt: Bool](/documentation/javascriptcore/jsvalue/isbigint)

### Instance Methods

- [func compare(Double) -> JSRelationCondition](/documentation/javascriptcore/jsvalue/compare(_:)-35b2t)
- [func compare(JSValue) -> JSRelationCondition](/documentation/javascriptcore/jsvalue/compare(_:)-5w184)
- [func compare(UInt64) -> JSRelationCondition](/documentation/javascriptcore/jsvalue/compare(_:)-64n3k)
- [func compare(Int64) -> JSRelationCondition](/documentation/javascriptcore/jsvalue/compare(_:)-9d4zq)
- [func toInt64() -> Int64](/documentation/javascriptcore/jsvalue/toint64())
- [func toUInt64() -> UInt64](/documentation/javascriptcore/jsvalue/touint64())
- [JSManagedValue](/documentation/javascriptcore/jsmanagedvalue)

### Creating a Managed Value

- [init!(value: JSValue!)](/documentation/javascriptcore/jsmanagedvalue/init(value:))
- [init!(value: JSValue!, andOwner: Any!)](/documentation/javascriptcore/jsmanagedvalue/init(value:andowner:))

### Accessing the Managed Value

- [var value: JSValue!](/documentation/javascriptcore/jsmanagedvalue/value)

## Native Code

- [JSExport](/documentation/javascriptcore/jsexport)

## C API

- [C JavaScriptCore API](/documentation/javascriptcore/c-javascriptcore-api)

### JavaScriptCore Engine Interface

- [JSContextGroupRef](/documentation/javascriptcore/jscontextgroupref)

#### Accessing the Content Group

- [func JSContextGetGroup(JSContextRef!) -> JSContextGroupRef!](/documentation/javascriptcore/jscontextgetgroup(_:))
- [JSContextRef](/documentation/javascriptcore/jscontextref)

#### Creating a Context Group

- [func JSContextGroupCreate() -> JSContextGroupRef!](/documentation/javascriptcore/jscontextgroupcreate())
- [func JSContextGroupRetain(JSContextGroupRef!) -> JSContextGroupRef!](/documentation/javascriptcore/jscontextgroupretain(_:))
- [func JSContextGroupRelease(JSContextGroupRef!)](/documentation/javascriptcore/jscontextgrouprelease(_:))

#### Accessing the Global Context

- [func JSContextGetGlobalContext(JSContextRef!) -> JSGlobalContextRef!](/documentation/javascriptcore/jscontextgetglobalcontext(_:))
- [JSGlobalContextRef](/documentation/javascriptcore/jsglobalcontextref)

#### Creating a global context

- [func JSGlobalContextCreate(JSClassRef!) -> JSGlobalContextRef!](/documentation/javascriptcore/jsglobalcontextcreate(_:))
- [func JSGlobalContextCreateInGroup(JSContextGroupRef!, JSClassRef!) -> JSGlobalContextRef!](/documentation/javascriptcore/jsglobalcontextcreateingroup(_:_:))
- [func JSGlobalContextRetain(JSGlobalContextRef!) -> JSGlobalContextRef!](/documentation/javascriptcore/jsglobalcontextretain(_:))
- [func JSGlobalContextRelease(JSGlobalContextRef!)](/documentation/javascriptcore/jsglobalcontextrelease(_:))

#### Managing the context’s name

- [func JSGlobalContextCopyName(JSGlobalContextRef!) -> JSStringRef!](/documentation/javascriptcore/jsglobalcontextcopyname(_:))
- [func JSGlobalContextSetName(JSGlobalContextRef!, JSStringRef!)](/documentation/javascriptcore/jsglobalcontextsetname(_:_:))

#### Making a context inspectable

- [func JSGlobalContextIsInspectable(JSGlobalContextRef!) -> Bool](/documentation/javascriptcore/jsglobalcontextisinspectable(_:))

##### Related Documentation

- [func JSGlobalContextCopyName(JSGlobalContextRef!) -> JSStringRef!](/documentation/javascriptcore/jsglobalcontextcopyname(_:))
- [func JSGlobalContextSetName(JSGlobalContextRef!, JSStringRef!)](/documentation/javascriptcore/jsglobalcontextsetname(_:_:))
- [func JSGlobalContextSetInspectable(JSGlobalContextRef!, Bool)](/documentation/javascriptcore/jsglobalcontextsetinspectable(_:_:))

##### Related Documentation

- [func JSGlobalContextCopyName(JSGlobalContextRef!) -> JSStringRef!](/documentation/javascriptcore/jsglobalcontextcopyname(_:))
- [func JSGlobalContextSetName(JSGlobalContextRef!, JSStringRef!)](/documentation/javascriptcore/jsglobalcontextsetname(_:_:))
- [JSStringRef](/documentation/javascriptcore/jsstringref)

#### Creating a JavaScript String

- [func JSStringCreateWithCharacters(UnsafePointer<JSChar>!, Int) -> JSStringRef!](/documentation/javascriptcore/jsstringcreatewithcharacters(_:_:))
- [JSChar](/documentation/javascriptcore/jschar)
- [func JSStringCreateWithUTF8CString(UnsafePointer<CChar>!) -> JSStringRef!](/documentation/javascriptcore/jsstringcreatewithutf8cstring(_:))
- [func JSStringRetain(JSStringRef!) -> JSStringRef!](/documentation/javascriptcore/jsstringretain(_:))
- [func JSStringRelease(JSStringRef!)](/documentation/javascriptcore/jsstringrelease(_:))

#### Accessing JavaScript String Information

- [func JSStringGetLength(JSStringRef!) -> Int](/documentation/javascriptcore/jsstringgetlength(_:))
- [func JSStringGetCharactersPtr(JSStringRef!) -> UnsafePointer<JSChar>!](/documentation/javascriptcore/jsstringgetcharactersptr(_:))
- [func JSStringGetMaximumUTF8CStringSize(JSStringRef!) -> Int](/documentation/javascriptcore/jsstringgetmaximumutf8cstringsize(_:))
- [func JSStringGetUTF8CString(JSStringRef!, UnsafeMutablePointer<CChar>!, Int) -> Int](/documentation/javascriptcore/jsstringgetutf8cstring(_:_:_:))

#### Comparing JavaScript Strings

- [func JSStringIsEqual(JSStringRef!, JSStringRef!) -> Bool](/documentation/javascriptcore/jsstringisequal(_:_:))
- [func JSStringIsEqualToUTF8CString(JSStringRef!, UnsafePointer<CChar>!) -> Bool](/documentation/javascriptcore/jsstringisequaltoutf8cstring(_:_:))

#### Converting to and from Core Foundation Strings

- [func JSStringCreateWithCFString(CFString!) -> JSStringRef!](/documentation/javascriptcore/jsstringcreatewithcfstring(_:))
- [func JSStringCopyCFString(CFAllocator!, JSStringRef!) -> CFString!](/documentation/javascriptcore/jsstringcopycfstring(_:_:))
- [JSClassRef](/documentation/javascriptcore/jsclassref)

### JavaScript Data Types

- [JSValueRef](/documentation/javascriptcore/jsvalueref)

#### Testing the Value’s Type

- [func JSValueGetType(JSContextRef!, JSValueRef!) -> JSType](/documentation/javascriptcore/jsvaluegettype(_:_:))
- [func JSValueIsUndefined(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisundefined(_:_:))
- [func JSValueIsNull(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisnull(_:_:))
- [func JSValueIsBoolean(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisboolean(_:_:))
- [func JSValueIsNumber(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisnumber(_:_:))
- [func JSValueIsString(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisstring(_:_:))
- [func JSValueIsSymbol(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueissymbol(_:_:))
- [func JSValueIsObject(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisobject(_:_:))
- [func JSValueIsObjectOfClass(JSContextRef!, JSValueRef!, JSClassRef!) -> Bool](/documentation/javascriptcore/jsvalueisobjectofclass(_:_:_:))
- [func JSValueIsArray(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisarray(_:_:))
- [func JSValueIsDate(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisdate(_:_:))
- [func JSValueGetTypedArrayType(JSContextRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSTypedArrayType](/documentation/javascriptcore/jsvaluegettypedarraytype(_:_:_:))
- [JSType](/documentation/javascriptcore/jstype)

##### Constants

- [var kJSTypeUndefined: JSType](/documentation/javascriptcore/kjstypeundefined)
- [var kJSTypeNull: JSType](/documentation/javascriptcore/kjstypenull)
- [var kJSTypeBoolean: JSType](/documentation/javascriptcore/kjstypeboolean)
- [var kJSTypeNumber: JSType](/documentation/javascriptcore/kjstypenumber)
- [var kJSTypeString: JSType](/documentation/javascriptcore/kjstypestring)
- [var kJSTypeObject: JSType](/documentation/javascriptcore/kjstypeobject)
- [var kJSTypeSymbol: JSType](/documentation/javascriptcore/kjstypesymbol)

##### Initializers

- [init(UInt32)](/documentation/javascriptcore/jstype/init(_:))
- [init(rawValue: UInt32)](/documentation/javascriptcore/jstype/init(rawvalue:))
- [var rawValue: UInt32](/documentation/javascriptcore/jstype/rawvalue)

#### Creating Values

- [func JSValueMakeUndefined(JSContextRef!) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakeundefined(_:))
- [func JSValueMakeNull(JSContextRef!) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakenull(_:))
- [func JSValueMakeBoolean(JSContextRef!, Bool) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakeboolean(_:_:))
- [func JSValueMakeNumber(JSContextRef!, Double) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakenumber(_:_:))
- [func JSValueMakeString(JSContextRef!, JSStringRef!) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakestring(_:_:))
- [func JSValueMakeSymbol(JSContextRef!, JSStringRef!) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakesymbol(_:_:))

#### Converting to Primitive Values

- [func JSValueToBoolean(JSContextRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvaluetoboolean(_:_:))
- [func JSValueToNumber(JSContextRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> Double](/documentation/javascriptcore/jsvaluetonumber(_:_:_:))
- [func JSValueToStringCopy(JSContextRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSStringRef!](/documentation/javascriptcore/jsvaluetostringcopy(_:_:_:))
- [func JSValueToObject(JSContextRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsvaluetoobject(_:_:_:))

#### Converting to and from JSON-Formatted Strings

- [func JSValueMakeFromJSONString(JSContextRef!, JSStringRef!) -> JSValueRef!](/documentation/javascriptcore/jsvaluemakefromjsonstring(_:_:))
- [func JSValueCreateJSONString(JSContextRef!, JSValueRef!, UInt32, UnsafeMutablePointer<JSValueRef?>!) -> JSStringRef!](/documentation/javascriptcore/jsvaluecreatejsonstring(_:_:_:_:))

#### Comparing Values

- [func JSValueIsEqual(JSContextRef!, JSValueRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jsvalueisequal(_:_:_:_:))
- [func JSValueIsStrictEqual(JSContextRef!, JSValueRef!, JSValueRef!) -> Bool](/documentation/javascriptcore/jsvalueisstrictequal(_:_:_:))
- [func JSValueIsInstanceOfConstructor(JSContextRef!, JSValueRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jsvalueisinstanceofconstructor(_:_:_:_:))

#### Supporting Garbage Collection

- [func JSValueProtect(JSContextRef!, JSValueRef!)](/documentation/javascriptcore/jsvalueprotect(_:_:))
- [func JSValueUnprotect(JSContextRef!, JSValueRef!)](/documentation/javascriptcore/jsvalueunprotect(_:_:))
- [JSObjectRef](/documentation/javascriptcore/jsobjectref)

#### Accessing the Global Object

- [func JSContextGetGlobalObject(JSContextRef!) -> JSObjectRef!](/documentation/javascriptcore/jscontextgetglobalobject(_:))

#### Working with Objects

- [func JSObjectCallAsConstructor(JSContextRef!, JSObjectRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectcallasconstructor(_:_:_:_:_:))
- [func JSObjectCallAsFunction(JSContextRef!, JSObjectRef!, JSObjectRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSValueRef!](/documentation/javascriptcore/jsobjectcallasfunction(_:_:_:_:_:_:))
- [func JSObjectCopyPropertyNames(JSContextRef!, JSObjectRef!) -> JSPropertyNameArrayRef!](/documentation/javascriptcore/jsobjectcopypropertynames(_:_:))
- [func JSObjectDeleteProperty(JSContextRef!, JSObjectRef!, JSStringRef!, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jsobjectdeleteproperty(_:_:_:_:))
- [func JSObjectGetPrivate(JSObjectRef!) -> UnsafeMutableRawPointer!](/documentation/javascriptcore/jsobjectgetprivate(_:))
- [func JSObjectGetProperty(JSContextRef!, JSObjectRef!, JSStringRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSValueRef!](/documentation/javascriptcore/jsobjectgetproperty(_:_:_:_:))
- [func JSObjectGetPropertyAtIndex(JSContextRef!, JSObjectRef!, UInt32, UnsafeMutablePointer<JSValueRef?>!) -> JSValueRef!](/documentation/javascriptcore/jsobjectgetpropertyatindex(_:_:_:_:))
- [func JSObjectGetPrototype(JSContextRef!, JSObjectRef!) -> JSValueRef!](/documentation/javascriptcore/jsobjectgetprototype(_:_:))
- [func JSObjectHasProperty(JSContextRef!, JSObjectRef!, JSStringRef!) -> Bool](/documentation/javascriptcore/jsobjecthasproperty(_:_:_:))
- [func JSObjectIsConstructor(JSContextRef!, JSObjectRef!) -> Bool](/documentation/javascriptcore/jsobjectisconstructor(_:_:))
- [func JSObjectIsFunction(JSContextRef!, JSObjectRef!) -> Bool](/documentation/javascriptcore/jsobjectisfunction(_:_:))
- [func JSObjectMake(JSContextRef!, JSClassRef!, UnsafeMutableRawPointer!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmake(_:_:_:))
- [func JSObjectMakeArray(JSContextRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakearray(_:_:_:_:))
- [func JSObjectMakeConstructor(JSContextRef!, JSClassRef!, JSObjectCallAsConstructorCallback!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakeconstructor(_:_:_:))
- [func JSObjectMakeDate(JSContextRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakedate(_:_:_:_:))
- [func JSObjectMakeError(JSContextRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakeerror(_:_:_:_:))
- [func JSObjectMakeFunction(JSContextRef!, JSStringRef!, UInt32, UnsafePointer<JSStringRef?>!, JSStringRef!, JSStringRef!, Int32, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakefunction(_:_:_:_:_:_:_:_:))
- [func JSObjectMakeFunctionWithCallback(JSContextRef!, JSStringRef!, JSObjectCallAsFunctionCallback!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakefunctionwithcallback(_:_:_:))
- [func JSObjectMakeRegExp(JSContextRef!, Int, UnsafePointer<JSValueRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakeregexp(_:_:_:_:))
- [func JSObjectSetPrivate(JSObjectRef!, UnsafeMutableRawPointer!) -> Bool](/documentation/javascriptcore/jsobjectsetprivate(_:_:))
- [func JSObjectSetProperty(JSContextRef!, JSObjectRef!, JSStringRef!, JSValueRef!, JSPropertyAttributes, UnsafeMutablePointer<JSValueRef?>!)](/documentation/javascriptcore/jsobjectsetproperty(_:_:_:_:_:_:))
- [func JSObjectSetPropertyAtIndex(JSContextRef!, JSObjectRef!, UInt32, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!)](/documentation/javascriptcore/jsobjectsetpropertyatindex(_:_:_:_:_:))
- [func JSObjectGetPropertyForKey(JSContextRef!, JSObjectRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSValueRef!](/documentation/javascriptcore/jsobjectgetpropertyforkey(_:_:_:_:))
- [func JSObjectSetPrototype(JSContextRef!, JSObjectRef!, JSValueRef!)](/documentation/javascriptcore/jsobjectsetprototype(_:_:_:))
- [func JSObjectDeletePropertyForKey(JSContextRef!, JSObjectRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jsobjectdeletepropertyforkey(_:_:_:_:))
- [func JSObjectHasPropertyForKey(JSContextRef!, JSObjectRef!, JSValueRef!, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jsobjecthaspropertyforkey(_:_:_:_:))
- [func JSObjectSetPropertyForKey(JSContextRef!, JSObjectRef!, JSValueRef!, JSValueRef!, JSPropertyAttributes, UnsafeMutablePointer<JSValueRef?>!)](/documentation/javascriptcore/jsobjectsetpropertyforkey(_:_:_:_:_:_:))
- [func JSObjectMakeDeferredPromise(JSContextRef!, UnsafeMutablePointer<JSObjectRef?>!, UnsafeMutablePointer<JSObjectRef?>!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakedeferredpromise(_:_:_:_:))

#### Working with Classes

- [func JSClassCreate(UnsafePointer<JSClassDefinition>!) -> JSClassRef!](/documentation/javascriptcore/jsclasscreate(_:))
- [func JSClassRelease(JSClassRef!)](/documentation/javascriptcore/jsclassrelease(_:))
- [func JSClassRetain(JSClassRef!) -> JSClassRef!](/documentation/javascriptcore/jsclassretain(_:))
- [let kJSClassDefinitionEmpty: JSClassDefinition](/documentation/javascriptcore/kjsclassdefinitionempty)
- [JSClassDefinition](/documentation/javascriptcore/jsclassdefinition)

##### Creating a Class Definition

- [init()](/documentation/javascriptcore/jsclassdefinition/init())
- [init(version: Int32, attributes: JSClassAttributes, className: UnsafePointer<CChar>!, parentClass: JSClassRef!, staticValues: UnsafePointer<JSStaticValue>!, staticFunctions: UnsafePointer<JSStaticFunction>!, initialize: JSObjectInitializeCallback!, finalize: JSObjectFinalizeCallback!, hasProperty: JSObjectHasPropertyCallback!, getProperty: JSObjectGetPropertyCallback!, setProperty: JSObjectSetPropertyCallback!, deleteProperty: JSObjectDeletePropertyCallback!, getPropertyNames: JSObjectGetPropertyNamesCallback!, callAsFunction: JSObjectCallAsFunctionCallback!, callAsConstructor: JSObjectCallAsConstructorCallback!, hasInstance: JSObjectHasInstanceCallback!, convertToType: JSObjectConvertToTypeCallback!)](/documentation/javascriptcore/jsclassdefinition/init(version:attributes:classname:parentclass:staticvalues:staticfunctions:initialize:finalize:hasproperty:getproperty:setproperty:deleteproperty:getpropertynames:callasfunction:callasconstructor:hasinstance:converttotype:))
- [JSClassAttributes](/documentation/javascriptcore/jsclassattributes)

##### Managing Class Information

- [var parentClass: JSClassRef!](/documentation/javascriptcore/jsclassdefinition/parentclass)
- [var className: UnsafePointer<CChar>!](/documentation/javascriptcore/jsclassdefinition/classname)
- [var version: Int32](/documentation/javascriptcore/jsclassdefinition/version)
- [var attributes: JSClassAttributes](/documentation/javascriptcore/jsclassdefinition/attributes)
- [var staticValues: UnsafePointer<JSStaticValue>!](/documentation/javascriptcore/jsclassdefinition/staticvalues)
- [JSStaticValue](/documentation/javascriptcore/jsstaticvalue)

###### Creating a Static Value

- [init()](/documentation/javascriptcore/jsstaticvalue/init())
- [init(name: UnsafePointer<CChar>!, getProperty: JSObjectGetPropertyCallback!, setProperty: JSObjectSetPropertyCallback!, attributes: JSPropertyAttributes)](/documentation/javascriptcore/jsstaticvalue/init(name:getproperty:setproperty:attributes:))

###### Accessing Static Value Information

- [var name: UnsafePointer<CChar>!](/documentation/javascriptcore/jsstaticvalue/name)
- [var getProperty: JSObjectGetPropertyCallback!](/documentation/javascriptcore/jsstaticvalue/getproperty)
- [var setProperty: JSObjectSetPropertyCallback!](/documentation/javascriptcore/jsstaticvalue/setproperty)
- [var attributes: JSPropertyAttributes](/documentation/javascriptcore/jsstaticvalue/attributes)
- [var staticFunctions: UnsafePointer<JSStaticFunction>!](/documentation/javascriptcore/jsclassdefinition/staticfunctions)
- [JSStaticFunction](/documentation/javascriptcore/jsstaticfunction)

###### Creating a Static Function

- [init()](/documentation/javascriptcore/jsstaticfunction/init())
- [init(name: UnsafePointer<CChar>!, callAsFunction: JSObjectCallAsFunctionCallback!, attributes: JSPropertyAttributes)](/documentation/javascriptcore/jsstaticfunction/init(name:callasfunction:attributes:))

###### Accessing Static Function Information

- [var name: UnsafePointer<CChar>!](/documentation/javascriptcore/jsstaticfunction/name)
- [var callAsFunction: JSObjectCallAsFunctionCallback!](/documentation/javascriptcore/jsstaticfunction/callasfunction)
- [var attributes: JSPropertyAttributes](/documentation/javascriptcore/jsstaticfunction/attributes)

##### Managing Callbacks

- [var initialize: JSObjectInitializeCallback!](/documentation/javascriptcore/jsclassdefinition/initialize)
- [JSObjectInitializeCallback](/documentation/javascriptcore/jsobjectinitializecallback)
- [var finalize: JSObjectFinalizeCallback!](/documentation/javascriptcore/jsclassdefinition/finalize)
- [JSObjectFinalizeCallback](/documentation/javascriptcore/jsobjectfinalizecallback)
- [var hasProperty: JSObjectHasPropertyCallback!](/documentation/javascriptcore/jsclassdefinition/hasproperty)
- [JSObjectHasPropertyCallback](/documentation/javascriptcore/jsobjecthaspropertycallback)
- [var getProperty: JSObjectGetPropertyCallback!](/documentation/javascriptcore/jsclassdefinition/getproperty)
- [JSObjectGetPropertyCallback](/documentation/javascriptcore/jsobjectgetpropertycallback)
- [var setProperty: JSObjectSetPropertyCallback!](/documentation/javascriptcore/jsclassdefinition/setproperty)
- [JSObjectSetPropertyCallback](/documentation/javascriptcore/jsobjectsetpropertycallback)
- [var deleteProperty: JSObjectDeletePropertyCallback!](/documentation/javascriptcore/jsclassdefinition/deleteproperty)
- [JSObjectDeletePropertyCallback](/documentation/javascriptcore/jsobjectdeletepropertycallback)
- [var getPropertyNames: JSObjectGetPropertyNamesCallback!](/documentation/javascriptcore/jsclassdefinition/getpropertynames)
- [JSObjectGetPropertyNamesCallback](/documentation/javascriptcore/jsobjectgetpropertynamescallback)
- [var callAsFunction: JSObjectCallAsFunctionCallback!](/documentation/javascriptcore/jsclassdefinition/callasfunction)
- [JSObjectCallAsFunctionCallback](/documentation/javascriptcore/jsobjectcallasfunctioncallback)
- [var hasInstance: JSObjectHasInstanceCallback!](/documentation/javascriptcore/jsclassdefinition/hasinstance)
- [JSObjectHasInstanceCallback](/documentation/javascriptcore/jsobjecthasinstancecallback)
- [var callAsConstructor: JSObjectCallAsConstructorCallback!](/documentation/javascriptcore/jsclassdefinition/callasconstructor)
- [JSObjectCallAsConstructorCallback](/documentation/javascriptcore/jsobjectcallasconstructorcallback)
- [var convertToType: JSObjectConvertToTypeCallback!](/documentation/javascriptcore/jsclassdefinition/converttotype)
- [JSObjectConvertToTypeCallback](/documentation/javascriptcore/jsobjectconverttotypecallback)
- [JSClassAttribute](/documentation/javascriptcore/jsclassattribute)

##### Constants

- [var kJSClassAttributeNone: Int](/documentation/javascriptcore/kjsclassattributenone)
- [var kJSClassAttributeNoAutomaticPrototype: Int](/documentation/javascriptcore/kjsclassattributenoautomaticprototype)

#### Working with Properties

- [func JSPropertyNameAccumulatorAddName(JSPropertyNameAccumulatorRef!, JSStringRef!)](/documentation/javascriptcore/jspropertynameaccumulatoraddname(_:_:))
- [func JSPropertyNameArrayGetCount(JSPropertyNameArrayRef!) -> Int](/documentation/javascriptcore/jspropertynamearraygetcount(_:))
- [func JSPropertyNameArrayGetNameAtIndex(JSPropertyNameArrayRef!, Int) -> JSStringRef!](/documentation/javascriptcore/jspropertynamearraygetnameatindex(_:_:))
- [func JSPropertyNameArrayRelease(JSPropertyNameArrayRef!)](/documentation/javascriptcore/jspropertynamearrayrelease(_:))
- [func JSPropertyNameArrayRetain(JSPropertyNameArrayRef!) -> JSPropertyNameArrayRef!](/documentation/javascriptcore/jspropertynamearrayretain(_:))
- [JSPropertyAttributes](/documentation/javascriptcore/jspropertyattributes)
- [JSPropertyAttribute](/documentation/javascriptcore/jspropertyattribute)

##### Constants

- [var kJSPropertyAttributeNone: Int](/documentation/javascriptcore/kjspropertyattributenone)
- [var kJSPropertyAttributeReadOnly: Int](/documentation/javascriptcore/kjspropertyattributereadonly)
- [var kJSPropertyAttributeDontEnum: Int](/documentation/javascriptcore/kjspropertyattributedontenum)
- [var kJSPropertyAttributeDontDelete: Int](/documentation/javascriptcore/kjspropertyattributedontdelete)
- [JSPropertyNameArrayRef](/documentation/javascriptcore/jspropertynamearrayref)
- [JSPropertyNameAccumulatorRef](/documentation/javascriptcore/jspropertynameaccumulatorref)

#### Creating a Typed Array

- [func JSObjectMakeTypedArray(JSContextRef!, JSTypedArrayType, Int, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmaketypedarray(_:_:_:_:))
- [func JSObjectMakeTypedArrayWithBytesNoCopy(JSContextRef!, JSTypedArrayType, UnsafeMutableRawPointer!, Int, JSTypedArrayBytesDeallocator!, UnsafeMutableRawPointer!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmaketypedarraywithbytesnocopy(_:_:_:_:_:_:_:))
- [func JSObjectMakeTypedArrayWithArrayBuffer(JSContextRef!, JSTypedArrayType, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmaketypedarraywitharraybuffer(_:_:_:_:))
- [func JSObjectMakeTypedArrayWithArrayBufferAndOffset(JSContextRef!, JSTypedArrayType, JSObjectRef!, Int, Int, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmaketypedarraywitharraybufferandoffset(_:_:_:_:_:_:))
- [JSTypedArrayType](/documentation/javascriptcore/jstypedarraytype)

##### Constants

- [var kJSTypedArrayTypeNone: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypenone)
- [var kJSTypedArrayTypeArrayBuffer: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypearraybuffer)
- [var kJSTypedArrayTypeInt8Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeint8array)
- [var kJSTypedArrayTypeInt16Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeint16array)
- [var kJSTypedArrayTypeInt32Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeint32array)
- [var kJSTypedArrayTypeBigInt64Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypebigint64array)
- [var kJSTypedArrayTypeUint8Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeuint8array)
- [var kJSTypedArrayTypeUint8ClampedArray: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeuint8clampedarray)
- [var kJSTypedArrayTypeUint16Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeuint16array)
- [var kJSTypedArrayTypeUint32Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypeuint32array)
- [var kJSTypedArrayTypeBigUint64Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypebiguint64array)
- [var kJSTypedArrayTypeFloat32Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypefloat32array)
- [var kJSTypedArrayTypeFloat64Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypefloat64array)

##### Initializers

- [init(UInt32)](/documentation/javascriptcore/jstypedarraytype/init(_:))
- [init(rawValue: UInt32)](/documentation/javascriptcore/jstypedarraytype/init(rawvalue:))
- [var rawValue: UInt32](/documentation/javascriptcore/jstypedarraytype/rawvalue)
- [JSTypedArrayBytesDeallocator](/documentation/javascriptcore/jstypedarraybytesdeallocator)

#### Accessing Typed Array Information

- [func JSObjectGetTypedArrayBytesPtr(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> UnsafeMutableRawPointer!](/documentation/javascriptcore/jsobjectgettypedarraybytesptr(_:_:_:))
- [func JSObjectGetTypedArrayLength(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> Int](/documentation/javascriptcore/jsobjectgettypedarraylength(_:_:_:))
- [func JSObjectGetTypedArrayByteLength(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> Int](/documentation/javascriptcore/jsobjectgettypedarraybytelength(_:_:_:))
- [func JSObjectGetTypedArrayByteOffset(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> Int](/documentation/javascriptcore/jsobjectgettypedarraybyteoffset(_:_:_:))
- [func JSObjectGetTypedArrayBuffer(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectgettypedarraybuffer(_:_:_:))

#### Working with Array Buffers

- [func JSObjectMakeArrayBufferWithBytesNoCopy(JSContextRef!, UnsafeMutableRawPointer!, Int, JSTypedArrayBytesDeallocator!, UnsafeMutableRawPointer!, UnsafeMutablePointer<JSValueRef?>!) -> JSObjectRef!](/documentation/javascriptcore/jsobjectmakearraybufferwithbytesnocopy(_:_:_:_:_:_:))
- [func JSObjectGetArrayBufferByteLength(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> Int](/documentation/javascriptcore/jsobjectgetarraybufferbytelength(_:_:_:))
- [func JSObjectGetArrayBufferBytesPtr(JSContextRef!, JSObjectRef!, UnsafeMutablePointer<JSValueRef?>!) -> UnsafeMutableRawPointer!](/documentation/javascriptcore/jsobjectgetarraybufferbytesptr(_:_:_:))

### Script Evaluation

- [func JSCheckScriptSyntax(JSContextRef!, JSStringRef!, JSStringRef!, Int32, UnsafeMutablePointer<JSValueRef?>!) -> Bool](/documentation/javascriptcore/jscheckscriptsyntax(_:_:_:_:_:))
- [func JSEvaluateScript(JSContextRef!, JSStringRef!, JSObjectRef!, JSStringRef!, Int32, UnsafeMutablePointer<JSValueRef?>!) -> JSValueRef!](/documentation/javascriptcore/jsevaluatescript(_:_:_:_:_:_:))
- [func JSGarbageCollect(JSContextRef!)](/documentation/javascriptcore/jsgarbagecollect(_:))

### Constants

- [var JSC_OBJC_API_ENABLED: Int32](/documentation/javascriptcore/jsc_objc_api_enabled)

## Reference

- [JavaScriptCore Constants](/documentation/javascriptcore/javascriptcore-constants)

### Constants

- [var kJSTypedArrayTypeBigInt64Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypebigint64array)
- [var kJSTypedArrayTypeBigUint64Array: JSTypedArrayType](/documentation/javascriptcore/kjstypedarraytypebiguint64array)

## Variables

- [var kJSTypeBigInt: JSType](/documentation/javascriptcore/kjstypebigint)

## Functions

- [func JSBigIntCreateWithDouble(JSContextRef, Double, UnsafeMutablePointer<JSValueRef?>?) -> JSValueRef](/documentation/javascriptcore/jsbigintcreatewithdouble(_:_:_:))
- [func JSBigIntCreateWithInt64(JSContextRef, Int64, UnsafeMutablePointer<JSValueRef?>?) -> JSValueRef](/documentation/javascriptcore/jsbigintcreatewithint64(_:_:_:))
- [func JSBigIntCreateWithString(JSContextRef, JSStringRef, UnsafeMutablePointer<JSValueRef?>?) -> JSValueRef](/documentation/javascriptcore/jsbigintcreatewithstring(_:_:_:))
- [func JSBigIntCreateWithUInt64(JSContextRef, UInt64, UnsafeMutablePointer<JSValueRef?>?) -> JSValueRef](/documentation/javascriptcore/jsbigintcreatewithuint64(_:_:_:))
- [func JSValueCompare(JSContextRef, JSValueRef, JSValueRef, UnsafeMutablePointer<JSValueRef?>?) -> JSRelationCondition](/documentation/javascriptcore/jsvaluecompare(_:_:_:_:))
- [func JSValueCompareDouble(JSContextRef, JSValueRef, Double, UnsafeMutablePointer<JSValueRef?>?) -> JSRelationCondition](/documentation/javascriptcore/jsvaluecomparedouble(_:_:_:_:))
- [func JSValueCompareInt64(JSContextRef, JSValueRef, Int64, UnsafeMutablePointer<JSValueRef?>?) -> JSRelationCondition](/documentation/javascriptcore/jsvaluecompareint64(_:_:_:_:))
- [func JSValueCompareUInt64(JSContextRef, JSValueRef, UInt64, UnsafeMutablePointer<JSValueRef?>?) -> JSRelationCondition](/documentation/javascriptcore/jsvaluecompareuint64(_:_:_:_:))
- [func JSValueIsBigInt(JSContextRef, JSValueRef) -> Bool](/documentation/javascriptcore/jsvalueisbigint(_:_:))
- [func JSValueToInt32(JSContextRef, JSValueRef, UnsafeMutablePointer<JSValueRef?>?) -> Int32](/documentation/javascriptcore/jsvaluetoint32(_:_:_:))
- [func JSValueToInt64(JSContextRef, JSValueRef, UnsafeMutablePointer<JSValueRef?>?) -> Int64](/documentation/javascriptcore/jsvaluetoint64(_:_:_:))
- [func JSValueToUInt32(JSContextRef, JSValueRef, UnsafeMutablePointer<JSValueRef?>?) -> UInt32](/documentation/javascriptcore/jsvaluetouint32(_:_:_:))
- [func JSValueToUInt64(JSContextRef, JSValueRef, UnsafeMutablePointer<JSValueRef?>?) -> UInt64](/documentation/javascriptcore/jsvaluetouint64(_:_:_:))

## Enumerations

- [JSRelationCondition](/documentation/javascriptcore/jsrelationcondition)

### Enumeration Cases

- [case equal](/documentation/javascriptcore/jsrelationcondition/equal)
- [case greaterThan](/documentation/javascriptcore/jsrelationcondition/greaterthan)
- [case lessThan](/documentation/javascriptcore/jsrelationcondition/lessthan)
- [case undefined](/documentation/javascriptcore/jsrelationcondition/undefined)

### Initializers

- [init?(rawValue: UInt32)](/documentation/javascriptcore/jsrelationcondition/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
