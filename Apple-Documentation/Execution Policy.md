# Execution Policy Documentation

Source: https://sosumi.ai/documentation/executionpolicy

---
title: Execution Policy
source: https://developer.apple.com/documentation/executionpolicy
timestamp: 2026-02-13T18:56:44.194Z
---

## Structures

- [EPError](/documentation/executionpolicy/eperror-swift.struct)

### Type Properties

- [static var generic: EPError.Code](/documentation/executionpolicy/eperror-swift.struct/generic)
- [static var notADeveloperTool: EPError.Code](/documentation/executionpolicy/eperror-swift.struct/notadevelopertool)
- [static var errorDomain: String](/documentation/executionpolicy/eperror-swift.struct/errordomain)

### Enumerations

- [EPError.Code](/documentation/executionpolicy/eperror-swift.struct/code)

#### Enumeration Cases

- [case generic](/documentation/executionpolicy/eperror-swift.struct/code/generic)
- [case notADeveloperTool](/documentation/executionpolicy/eperror-swift.struct/code/notadevelopertool)

#### Initializers

- [init?(rawValue: Int)](/documentation/executionpolicy/eperror-swift.struct/code/init(rawvalue:))

## Classes

- [EPDeveloperTool](/documentation/executionpolicy/epdevelopertool)

### Initializers

- [init()](/documentation/executionpolicy/epdevelopertool/init())

### Instance Properties

- [var authorizationStatus: EPDeveloperToolStatus](/documentation/executionpolicy/epdevelopertool/authorizationstatus)

### Instance Methods

- [func requestAccess(completionHandler: (Bool) -> Void)](/documentation/executionpolicy/epdevelopertool/requestaccess(completionhandler:))
- [EPExecutionPolicy](/documentation/executionpolicy/epexecutionpolicy)

### Initializers

- [init()](/documentation/executionpolicy/epexecutionpolicy/init())

### Instance Methods

- [func addException(for: URL) throws](/documentation/executionpolicy/epexecutionpolicy/addexception(for:))

## Reference

- [ExecutionPolicy Constants](/documentation/executionpolicy/executionpolicy-constants)

### Constants

- [let EPErrorDomain: String](/documentation/executionpolicy/eperrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
