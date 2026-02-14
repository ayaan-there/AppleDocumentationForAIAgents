# AdServices Documentation

Source: https://sosumi.ai/documentation/adservices

---
title: AdServices
source: https://developer.apple.com/documentation/adservices
timestamp: 2026-02-13T19:06:44.370Z
---

## Essentials

- [Changelog](/documentation/adservices/changelog)

## Tokens

- [AAAttribution](/documentation/adservices/aaattribution)

### Getting a token

- [class func attributionToken() throws -> String](/documentation/adservices/aaattribution/attributiontoken())

## Errors

- [AAAttributionError](/documentation/adservices/aaattributionerror)

### Error domain

- [static var errorDomain: String](/documentation/adservices/aaattributionerror/errordomain)

### Error codes

- [static var internalError: AAAttributionError.Code](/documentation/adservices/aaattributionerror/internalerror)
- [static var networkError: AAAttributionError.Code](/documentation/adservices/aaattributionerror/networkerror)
- [static var platformNotSupported: AAAttributionError.Code](/documentation/adservices/aaattributionerror/platformnotsupported)
- [AAAttributionError.Code](/documentation/adservices/aaattributionerror/code)

#### Creating an error code

- [init?(rawValue: Int)](/documentation/adservices/aaattributionerror/code/init(rawvalue:))

#### Determining the cause of an error

- [case internalError](/documentation/adservices/aaattributionerror/code/internalerror)
- [case networkError](/documentation/adservices/aaattributionerror/code/networkerror)
- [case platformNotSupported](/documentation/adservices/aaattributionerror/code/platformnotsupported)

#### Getting information about error codes

- [var localizedDescription: String](/documentation/swift/error/localizeddescription)

#### Comparing errors

- [func != ((), ()) -> Bool](/documentation/swift/!=(_:_:)-18co7)
- [let AAAttributionErrorDomain: String](/documentation/adservices/aaattributionerrordomain)
- [AAAttributionError.Code](/documentation/adservices/aaattributionerror/code)

### Creating an error code

- [init?(rawValue: Int)](/documentation/adservices/aaattributionerror/code/init(rawvalue:))

### Determining the cause of an error

- [case internalError](/documentation/adservices/aaattributionerror/code/internalerror)
- [case networkError](/documentation/adservices/aaattributionerror/code/networkerror)
- [case platformNotSupported](/documentation/adservices/aaattributionerror/code/platformnotsupported)

### Getting information about error codes

- [var localizedDescription: String](/documentation/swift/error/localizeddescription)

### Comparing errors

- [func != ((), ()) -> Bool](/documentation/swift/!=(_:_:)-18co7)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
