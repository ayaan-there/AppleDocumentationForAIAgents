# DeviceCheck Documentation

Source: https://sosumi.ai/documentation/devicecheck

---
title: DeviceCheck
source: https://developer.apple.com/documentation/devicecheck
timestamp: 2026-02-13T18:56:14.934Z
---

## Device identification

- [Accessing and modifying per-device data](/documentation/devicecheck/accessing-and-modifying-per-device-data)
- [DCDevice](/documentation/devicecheck/dcdevice)

### Getting the current device

- [class var current: DCDevice](/documentation/devicecheck/dcdevice/current)

### Determining API support

- [var isSupported: Bool](/documentation/devicecheck/dcdevice/issupported)

### Getting a device token

- [func generateToken(completionHandler: (Data?, (any Error)?) -> Void)](/documentation/devicecheck/dcdevice/generatetoken(completionhandler:))

## App Attest

- [Establishing your app’s integrity](/documentation/devicecheck/establishing-your-app-s-integrity)
- [Validating apps that connect to your server](/documentation/devicecheck/validating-apps-that-connect-to-your-server)
- [Assessing fraud risk](/documentation/devicecheck/assessing-fraud-risk)
- [Preparing to use the app attest service](/documentation/devicecheck/preparing-to-use-the-app-attest-service)
- [Attestation Object Validation Guide](/documentation/devicecheck/attestation-object-validation-guide)
- [DCAppAttestService](/documentation/devicecheck/dcappattestservice)

### Accessing the service

- [class var shared: DCAppAttestService](/documentation/devicecheck/dcappattestservice/shared)
- [var isSupported: Bool](/documentation/devicecheck/dcappattestservice/issupported)

### Preparing a key

- [func generateKey(completionHandler: (String?, (any Error)?) -> Void)](/documentation/devicecheck/dcappattestservice/generatekey(completionhandler:))
- [func attestKey(String, clientDataHash: Data, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/devicecheck/dcappattestservice/attestkey(_:clientdatahash:completionhandler:))

### Validating the app instance

- [func generateAssertion(String, clientDataHash: Data, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/devicecheck/dcappattestservice/generateassertion(_:clientdatahash:completionhandler:))
- [App Attest Environment](/documentation/bundleresources/entitlements/com.apple.developer.devicecheck.appattest-environment)

## Errors

- [DCError](/documentation/devicecheck/dcerror-swift.struct)

### Errors

- [static var featureUnsupported: DCError.Code](/documentation/devicecheck/dcerror-swift.struct/featureunsupported)
- [static var invalidInput: DCError.Code](/documentation/devicecheck/dcerror-swift.struct/invalidinput)
- [static var invalidKey: DCError.Code](/documentation/devicecheck/dcerror-swift.struct/invalidkey)
- [static var serverUnavailable: DCError.Code](/documentation/devicecheck/dcerror-swift.struct/serverunavailable)
- [static var unknownSystemFailure: DCError.Code](/documentation/devicecheck/dcerror-swift.struct/unknownsystemfailure)
- [DCError.Code](/documentation/devicecheck/dcerror-swift.struct/code)

#### Error codes

- [case featureUnsupported](/documentation/devicecheck/dcerror-swift.struct/code/featureunsupported)
- [case invalidInput](/documentation/devicecheck/dcerror-swift.struct/code/invalidinput)
- [case invalidKey](/documentation/devicecheck/dcerror-swift.struct/code/invalidkey)
- [case serverUnavailable](/documentation/devicecheck/dcerror-swift.struct/code/serverunavailable)
- [case unknownSystemFailure](/documentation/devicecheck/dcerror-swift.struct/code/unknownsystemfailure)

#### Initializers

- [init?(rawValue: Int)](/documentation/devicecheck/dcerror-swift.struct/code/init(rawvalue:))

### Error information

- [static var errorDomain: String](/documentation/devicecheck/dcerror-swift.struct/errordomain)
- [DCError.Code](/documentation/devicecheck/dcerror-swift.struct/code)

### Error codes

- [case featureUnsupported](/documentation/devicecheck/dcerror-swift.struct/code/featureunsupported)
- [case invalidInput](/documentation/devicecheck/dcerror-swift.struct/code/invalidinput)
- [case invalidKey](/documentation/devicecheck/dcerror-swift.struct/code/invalidkey)
- [case serverUnavailable](/documentation/devicecheck/dcerror-swift.struct/code/serverunavailable)
- [case unknownSystemFailure](/documentation/devicecheck/dcerror-swift.struct/code/unknownsystemfailure)

### Initializers

- [init?(rawValue: Int)](/documentation/devicecheck/dcerror-swift.struct/code/init(rawvalue:))
- [let DCErrorDomain: String](/documentation/devicecheck/dcerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
