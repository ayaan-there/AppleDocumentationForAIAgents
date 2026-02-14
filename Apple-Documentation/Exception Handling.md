# Exception Handling Documentation

Source: https://sosumi.ai/documentation/exceptionhandling

---
title: Exception Handling
source: https://developer.apple.com/documentation/exceptionhandling
timestamp: 2026-02-13T18:56:42.311Z
---

## Classes

- [NSExceptionHandler](/documentation/exceptionhandling/nsexceptionhandler)

### Getting the default exception handler

- [class func `default`() -> NSExceptionHandler!](/documentation/exceptionhandling/nsexceptionhandler/default())

### Getting and setting exception masks

- [func exceptionHandlingMask() -> Int](/documentation/exceptionhandling/nsexceptionhandler/exceptionhandlingmask())
- [func exceptionHangingMask() -> Int](/documentation/exceptionhandling/nsexceptionhandler/exceptionhangingmask())
- [func setExceptionHandlingMask(Int)](/documentation/exceptionhandling/nsexceptionhandler/setexceptionhandlingmask(_:))
- [func setExceptionHangingMask(Int)](/documentation/exceptionhandling/nsexceptionhandler/setexceptionhangingmask(_:))

### Getting and setting the delegate

- [func delegate() -> Any!](/documentation/exceptionhandling/nsexceptionhandler/delegate())
- [func setDelegate(Any!)](/documentation/exceptionhandling/nsexceptionhandler/setdelegate(_:))

### Constants

- [Logging and Handling Constants](/documentation/exceptionhandling/logging-and-handling-constants)

#### Constants

- [var NSLogUncaughtExceptionMask: Int](/documentation/exceptionhandling/nsloguncaughtexceptionmask)
- [var NSHandleUncaughtExceptionMask: Int](/documentation/exceptionhandling/nshandleuncaughtexceptionmask)
- [var NSLogUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nsloguncaughtsystemexceptionmask)
- [var NSHandleUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nshandleuncaughtsystemexceptionmask)
- [var NSLogUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nsloguncaughtruntimeerrormask)
- [var NSHandleUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nshandleuncaughtruntimeerrormask)
- [var NSLogTopLevelExceptionMask: Int](/documentation/exceptionhandling/nslogtoplevelexceptionmask)
- [var NSHandleTopLevelExceptionMask: Int](/documentation/exceptionhandling/nshandletoplevelexceptionmask)
- [var NSLogOtherExceptionMask: Int](/documentation/exceptionhandling/nslogotherexceptionmask)
- [var NSHandleOtherExceptionMask: Int](/documentation/exceptionhandling/nshandleotherexceptionmask)
- [System Hang Constants](/documentation/exceptionhandling/system-hang-constants)

#### Constants

- [var NSHangOnUncaughtExceptionMask: Int](/documentation/exceptionhandling/nshangonuncaughtexceptionmask)
- [var NSHangOnUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nshangonuncaughtsystemexceptionmask)
- [var NSHangOnUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nshangonuncaughtruntimeerrormask)
- [var NSHangOnTopLevelExceptionMask: Int](/documentation/exceptionhandling/nshangontoplevelexceptionmask)
- [var NSHangOnOtherExceptionMask: Int](/documentation/exceptionhandling/nshangonotherexceptionmask)
- [Exception Global String Constants](/documentation/exceptionhandling/exception-global-string-constants)

#### Constants

- [let NSUncaughtSystemExceptionException: String](/documentation/exceptionhandling/nsuncaughtsystemexceptionexception)
- [let NSUncaughtRuntimeErrorException: String](/documentation/exceptionhandling/nsuncaughtruntimeerrorexception)
- [let NSStackTraceKey: String](/documentation/exceptionhandling/nsstacktracekey)

## Protocols

- [NSExceptionHandlerDelegate](/documentation/exceptionhandling/nsexceptionhandlerdelegate)

### Logging and handling exceptions

- [func exceptionHandler(NSExceptionHandler!, shouldHandle: NSException!, mask: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/exceptionhandler(_:shouldhandle:mask:))
- [func exceptionHandler(NSExceptionHandler!, shouldLogException: NSException!, mask: Int) -> Bool](/documentation/objectivec/nsobject-swift.class/exceptionhandler(_:shouldlogexception:mask:))

## Reference

- [ExceptionHandling Enumerations](/documentation/exceptionhandling/exceptionhandling-enumerations)

### Enumerations

- [Logging and Handling Constants](/documentation/exceptionhandling/logging-and-handling-constants)

#### Constants

- [var NSLogUncaughtExceptionMask: Int](/documentation/exceptionhandling/nsloguncaughtexceptionmask)
- [var NSHandleUncaughtExceptionMask: Int](/documentation/exceptionhandling/nshandleuncaughtexceptionmask)
- [var NSLogUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nsloguncaughtsystemexceptionmask)
- [var NSHandleUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nshandleuncaughtsystemexceptionmask)
- [var NSLogUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nsloguncaughtruntimeerrormask)
- [var NSHandleUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nshandleuncaughtruntimeerrormask)
- [var NSLogTopLevelExceptionMask: Int](/documentation/exceptionhandling/nslogtoplevelexceptionmask)
- [var NSHandleTopLevelExceptionMask: Int](/documentation/exceptionhandling/nshandletoplevelexceptionmask)
- [var NSLogOtherExceptionMask: Int](/documentation/exceptionhandling/nslogotherexceptionmask)
- [var NSHandleOtherExceptionMask: Int](/documentation/exceptionhandling/nshandleotherexceptionmask)
- [System Hang Constants](/documentation/exceptionhandling/system-hang-constants)

#### Constants

- [var NSHangOnUncaughtExceptionMask: Int](/documentation/exceptionhandling/nshangonuncaughtexceptionmask)
- [var NSHangOnUncaughtSystemExceptionMask: Int](/documentation/exceptionhandling/nshangonuncaughtsystemexceptionmask)
- [var NSHangOnUncaughtRuntimeErrorMask: Int](/documentation/exceptionhandling/nshangonuncaughtruntimeerrormask)
- [var NSHangOnTopLevelExceptionMask: Int](/documentation/exceptionhandling/nshangontoplevelexceptionmask)
- [var NSHangOnOtherExceptionMask: Int](/documentation/exceptionhandling/nshangonotherexceptionmask)
- [ExceptionHandling Constants](/documentation/exceptionhandling/exceptionhandling-constants)

### Constants

- [let NSStackTraceKey: String](/documentation/exceptionhandling/nsstacktracekey)
- [let NSUncaughtRuntimeErrorException: String](/documentation/exceptionhandling/nsuncaughtruntimeerrorexception)
- [let NSUncaughtSystemExceptionException: String](/documentation/exceptionhandling/nsuncaughtsystemexceptionexception)
- [ExceptionHandling Functions](/documentation/exceptionhandling/exceptionhandling-functions)

### Functions

- [func NSExceptionHandlerResume()](/documentation/exceptionhandling/nsexceptionhandlerresume())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
