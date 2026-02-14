# iAd Documentation

Source: https://sosumi.ai/documentation/iad

---
title: iAd
source: https://developer.apple.com/documentation/iad
timestamp: 2026-02-13T18:57:58.791Z
---

## Essentials

- [iAd Changelog](/documentation/iad/iad-changelog)
- [Setting Up Apple Search Ads Attribution](/documentation/iad/setting-up-apple-search-ads-attribution)
- [ADClient](/documentation/iad/adclient)

### Fetching a Shared Client Object

- [class func shared() -> ADClient](/documentation/iad/adclient/shared())

### Requesting Ad Attribution

- [func requestAttributionDetails(([String : NSObject]?, (any Error)?) -> Void)](/documentation/iad/adclient/requestattributiondetails(_:))

## Attribution Errors

- [let ADClientErrorDomain: String](/documentation/iad/adclienterrordomain)
- [ADClientError](/documentation/iad/adclienterror-swift.struct)

### Error Codes

- [static var corruptResponse: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/corruptresponse)
- [static var requestClientError: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/requestclienterror)
- [static var requestNetworkError: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/requestnetworkerror)
- [static var requestServerError: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/requestservererror)
- [static var trackingRestrictedOrDenied: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/trackingrestrictedordenied)
- [static var missingData: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/missingdata)
- [static var unsupportedPlatform: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/unsupportedplatform)
- [static var limitAdTracking: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/limitadtracking)
- [static var unknown: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/unknown)
- [ADClientError.Code](/documentation/iad/adclienterror-swift.struct/code)

#### Error Codes

- [case corruptResponse](/documentation/iad/adclienterror-swift.struct/code/corruptresponse)
- [case requestClientError](/documentation/iad/adclienterror-swift.struct/code/requestclienterror)
- [case requestNetworkError](/documentation/iad/adclienterror-swift.struct/code/requestnetworkerror)
- [case requestServerError](/documentation/iad/adclienterror-swift.struct/code/requestservererror)
- [case trackingRestrictedOrDenied](/documentation/iad/adclienterror-swift.struct/code/trackingrestrictedordenied)
- [case missingData](/documentation/iad/adclienterror-swift.struct/code/missingdata)
- [case unsupportedPlatform](/documentation/iad/adclienterror-swift.struct/code/unsupportedplatform)
- [case unknown](/documentation/iad/adclienterror-swift.struct/code/unknown)
- [static var limitAdTracking: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/code/limitadtracking)

#### Initializers

- [init?(rawValue: Int)](/documentation/iad/adclienterror-swift.struct/code/init(rawvalue:))

### Error Characteristics

- [let ADClientErrorDomain: String](/documentation/iad/adclienterrordomain)

### Type Properties

- [static var errorDomain: String](/documentation/iad/adclienterror-swift.struct/errordomain)
- [ADClientError.Code](/documentation/iad/adclienterror-swift.struct/code)

### Error Codes

- [case corruptResponse](/documentation/iad/adclienterror-swift.struct/code/corruptresponse)
- [case requestClientError](/documentation/iad/adclienterror-swift.struct/code/requestclienterror)
- [case requestNetworkError](/documentation/iad/adclienterror-swift.struct/code/requestnetworkerror)
- [case requestServerError](/documentation/iad/adclienterror-swift.struct/code/requestservererror)
- [case trackingRestrictedOrDenied](/documentation/iad/adclienterror-swift.struct/code/trackingrestrictedordenied)
- [case missingData](/documentation/iad/adclienterror-swift.struct/code/missingdata)
- [case unsupportedPlatform](/documentation/iad/adclienterror-swift.struct/code/unsupportedplatform)
- [case unknown](/documentation/iad/adclienterror-swift.struct/code/unknown)
- [static var limitAdTracking: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/code/limitadtracking)

### Initializers

- [init?(rawValue: Int)](/documentation/iad/adclienterror-swift.struct/code/init(rawvalue:))

## Deprecated

- [Deprecated Symbols](/documentation/iad/deprecated-symbols)

### Enumeration Cases

- [static var limitAdTracking: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/code/limitadtracking)
- [static var unknown: ADClientError.Code](/documentation/iad/adclienterror-swift.struct/unknown)
- [case unknown](/documentation/iad/adclienterror-swift.struct/code/unknown)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
