# Scripting Bridge Documentation

Source: https://sosumi.ai/documentation/scriptingbridge

---
title: Scripting Bridge
source: https://developer.apple.com/documentation/scriptingbridge
timestamp: 2026-02-13T19:01:43.539Z
---

## Classes

- [SBApplication](/documentation/scriptingbridge/sbapplication)

### Initializing a Scriptable Application Object

- [init?(bundleIdentifier: String)](/documentation/scriptingbridge/sbapplication/init(bundleidentifier:))
- [init?(processIdentifier: pid_t)](/documentation/scriptingbridge/sbapplication/init(processidentifier:))
- [init?(url: URL)](/documentation/scriptingbridge/sbapplication/init(url:))

### Creating a Scripting Class

- [func `class`(forScriptingClass: String) -> AnyClass?](/documentation/scriptingbridge/sbapplication/class(forscriptingclass:))

### Controlling the Application

- [func activate()](/documentation/scriptingbridge/sbapplication/activate())
- [var isRunning: Bool](/documentation/scriptingbridge/sbapplication/isrunning)
- [var launchFlags: LSLaunchFlags](/documentation/scriptingbridge/sbapplication/launchflags)
- [sendMode](/documentation/scriptingbridge/sbapplication/sendmode)
- [timeout](/documentation/scriptingbridge/sbapplication/timeout)

### Managing the Delegate

- [var delegate: (any SBApplicationDelegate)?](/documentation/scriptingbridge/sbapplication/delegate)
- [SBElementArray](/documentation/scriptingbridge/sbelementarray)

### Getting Objects in the Array

- [func object(withName: String) -> Any](/documentation/scriptingbridge/sbelementarray/object(withname:))
- [func object(withID: Any) -> Any](/documentation/scriptingbridge/sbelementarray/object(withid:))
- [func object(atLocation: Any) -> Any](/documentation/scriptingbridge/sbelementarray/object(atlocation:))

### Getting the Referenced Array

- [func get() -> [Any]?](/documentation/scriptingbridge/sbelementarray/get())

### Filtering an Element Array

- [func array(byApplying: Selector) -> [Any]](/documentation/scriptingbridge/sbelementarray/array(byapplying:))
- [func array(byApplying: Selector, with: Any) -> [Any]](/documentation/scriptingbridge/sbelementarray/array(byapplying:with:))
- [SBObject](/documentation/scriptingbridge/sbobject)

### Initializing a Scripting Bridge Object

- [init()](/documentation/scriptingbridge/sbobject/init())
- [init(data: Any)](/documentation/scriptingbridge/sbobject/init(data:))
- [init(properties: [AnyHashable : Any])](/documentation/scriptingbridge/sbobject/init(properties:))
- [init(elementCode: DescType, properties: [String : Any]?, data: Any?)](/documentation/scriptingbridge/sbobject/init(elementcode:properties:data:))

### Getting Referenced Data

- [func get() -> Any?](/documentation/scriptingbridge/sbobject/get())

### Sending Apple Events

- [func setTo(Any?)](/documentation/scriptingbridge/sbobject/setto(_:))

### Getting Properties and Elements

- [func property(with: AnyClass, code: AEKeyword) -> SBObject](/documentation/scriptingbridge/sbobject/property(with:code:))
- [func property(withCode: AEKeyword) -> SBObject](/documentation/scriptingbridge/sbobject/property(withcode:))
- [func elementArray(withCode: DescType) -> SBElementArray](/documentation/scriptingbridge/sbobject/elementarray(withcode:))

### Instance Methods

- [func lastError() -> (any Error)?](/documentation/scriptingbridge/sbobject/lasterror())

## Protocols

- [SBApplicationDelegate](/documentation/scriptingbridge/sbapplicationdelegate)

### Handling Errors

- [func eventDidFail(UnsafePointer<AppleEvent>, withError: any Error) -> Any?](/documentation/scriptingbridge/sbapplicationdelegate/eventdidfail(_:witherror:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
