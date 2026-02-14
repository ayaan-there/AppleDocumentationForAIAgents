# Local Authentication Documentation

Source: https://sosumi.ai/documentation/localauthentication

---
title: Local Authentication
source: https://developer.apple.com/documentation/localauthentication
timestamp: 2026-02-13T18:58:49.101Z
---

## Essentials

- [Logging a User into Your App with Face ID or Touch ID](/documentation/localauthentication/logging-a-user-into-your-app-with-face-id-or-touch-id)
- [Accessing Keychain Items with Face ID or Touch ID](/documentation/localauthentication/accessing-keychain-items-with-face-id-or-touch-id)

## Authentication and access

- [LARight](/documentation/localauthentication/laright)

### Authorizing a right

- [init()](/documentation/localauthentication/laright/init())
- [init(requirement: LAAuthenticationRequirement)](/documentation/localauthentication/laright/init(requirement:))
- [var tag: Int](/documentation/localauthentication/laright/tag)
- [func authorize(localizedReason: String, completion: ((any Error)?) -> Void)](/documentation/localauthentication/laright/authorize(localizedreason:completion:))
- [func authorize(localizedReason: String, in: LAPresentationContext, completion: ((any Error)?) -> Void)](/documentation/localauthentication/laright/authorize(localizedreason:in:completion:))

### Deauthorizing a right

- [func deauthorize(completion: () -> Void)](/documentation/localauthentication/laright/deauthorize(completion:))

### Monitoring authorization status

- [func checkCanAuthorize(completion: ((any Error)?) -> Void)](/documentation/localauthentication/laright/checkcanauthorize(completion:))
- [var state: LARight.State](/documentation/localauthentication/laright/state-swift.property)
- [LARight.State](/documentation/localauthentication/laright/state-swift.enum)

#### Authorization states

- [case authorizing](/documentation/localauthentication/laright/state-swift.enum/authorizing)
- [case authorized](/documentation/localauthentication/laright/state-swift.enum/authorized)
- [case notAuthorized](/documentation/localauthentication/laright/state-swift.enum/notauthorized)
- [case unknown](/documentation/localauthentication/laright/state-swift.enum/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/laright/state-swift.enum/init(rawvalue:))
- [LARight.State](/documentation/localauthentication/laright/state-swift.enum)

### Authorization states

- [case authorizing](/documentation/localauthentication/laright/state-swift.enum/authorizing)
- [case authorized](/documentation/localauthentication/laright/state-swift.enum/authorized)
- [case notAuthorized](/documentation/localauthentication/laright/state-swift.enum/notauthorized)
- [case unknown](/documentation/localauthentication/laright/state-swift.enum/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/laright/state-swift.enum/init(rawvalue:))
- [LAContext](/documentation/localauthentication/lacontext)

### Checking availability

- [func canEvaluatePolicy(LAPolicy, error: NSErrorPointer) -> Bool](/documentation/localauthentication/lacontext/canevaluatepolicy(_:error:))
- [LAPolicy](/documentation/localauthentication/lapolicy)

#### Policies

- [case deviceOwnerAuthenticationWithBiometrics](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithbiometrics)
- [static var deviceOwnerAuthenticationWithWatch: LAPolicy](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithwatch)
- [static var deviceOwnerAuthenticationWithBiometricsOrWatch: LAPolicy](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithbiometricsorwatch)
- [case deviceOwnerAuthentication](/documentation/localauthentication/lapolicy/deviceownerauthentication)
- [case deviceOwnerAuthenticationWithWristDetection](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithwristdetection)

#### Policy Constants

- [var kLAPolicyDeviceOwnerAuthenticationWithBiometrics: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithbiometrics)
- [var kLAPolicyDeviceOwnerAuthenticationWithWatch: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithwatch)
- [var kLAPolicyDeviceOwnerAuthenticationWithBiometricsOrWatch: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithbiometricsorwatch)
- [var kLAPolicyDeviceOwnerAuthentication: Int32](/documentation/localauthentication/klapolicydeviceownerauthentication)
- [var kLAPolicyDeviceOwnerAuthenticationWithWristDetection: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithwristdetection)

#### Enumeration Cases

- [case deviceOwnerAuthenticationWithBiometricsOrCompanion](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithbiometricsorcompanion)
- [case deviceOwnerAuthenticationWithCompanion](/documentation/localauthentication/lapolicy/deviceownerauthenticationwithcompanion)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/lapolicy/init(rawvalue:))
- [var biometryType: LABiometryType](/documentation/localauthentication/lacontext/biometrytype)
- [LABiometryType](/documentation/localauthentication/labiometrytype)

#### Types

- [case none](/documentation/localauthentication/labiometrytype/none)
- [case faceID](/documentation/localauthentication/labiometrytype/faceid)
- [case touchID](/documentation/localauthentication/labiometrytype/touchid)
- [case opticID](/documentation/localauthentication/labiometrytype/opticid)

#### Legacy Types

- [static var LABiometryNone: LABiometryType](/documentation/localauthentication/labiometrytype/labiometrynone)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/labiometrytype/init(rawvalue:))

### Evaluating authentication policies

- [func evaluatePolicy(LAPolicy, localizedReason: String, reply: (Bool, (any Error)?) -> Void)](/documentation/localauthentication/lacontext/evaluatepolicy(_:localizedreason:reply:))
- [var evaluatedPolicyDomainState: Data?](/documentation/localauthentication/lacontext/evaluatedpolicydomainstate)
- [var maxBiometryFailures: NSNumber?](/documentation/localauthentication/lacontext/maxbiometryfailures)

### Evaluating access controls

- [func evaluateAccessControl(SecAccessControl, operation: LAAccessControlOperation, localizedReason: String, reply: (Bool, (any Error)?) -> Void)](/documentation/localauthentication/lacontext/evaluateaccesscontrol(_:operation:localizedreason:reply:))
- [LAAccessControlOperation](/documentation/localauthentication/laaccesscontroloperation)

#### Constants

- [case createItem](/documentation/localauthentication/laaccesscontroloperation/createitem)
- [case useItem](/documentation/localauthentication/laaccesscontroloperation/useitem)
- [case createKey](/documentation/localauthentication/laaccesscontroloperation/createkey)
- [case useKeySign](/documentation/localauthentication/laaccesscontroloperation/usekeysign)
- [case useKeyDecrypt](/documentation/localauthentication/laaccesscontroloperation/usekeydecrypt)
- [case useKeyKeyExchange](/documentation/localauthentication/laaccesscontroloperation/usekeykeyexchange)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/laaccesscontroloperation/init(rawvalue:))
- [var interactionNotAllowed: Bool](/documentation/localauthentication/lacontext/interactionnotallowed)

### Customizing authentication prompts

- [var localizedReason: String](/documentation/localauthentication/lacontext/localizedreason)
- [var localizedFallbackTitle: String?](/documentation/localauthentication/lacontext/localizedfallbacktitle)
- [var localizedCancelTitle: String?](/documentation/localauthentication/lacontext/localizedcanceltitle)

### Reusing device unlock state

- [var touchIDAuthenticationAllowableReuseDuration: TimeInterval](/documentation/localauthentication/lacontext/touchidauthenticationallowablereuseduration)
- [let LATouchIDAuthenticationMaximumAllowableReuseDuration: TimeInterval](/documentation/localauthentication/latouchidauthenticationmaximumallowablereuseduration)

### Managing credentials

- [func setCredential(Data?, type: LACredentialType) -> Bool](/documentation/localauthentication/lacontext/setcredential(_:type:))
- [func isCredentialSet(LACredentialType) -> Bool](/documentation/localauthentication/lacontext/iscredentialset(_:))
- [LACredentialType](/documentation/localauthentication/lacredentialtype)

#### Cases

- [case applicationPassword](/documentation/localauthentication/lacredentialtype/applicationpassword)
- [case smartCardPIN](/documentation/localauthentication/lacredentialtype/smartcardpin)

#### Constants

- [var kLACredentialTypeApplicationPassword: Int32](/documentation/localauthentication/klacredentialtypeapplicationpassword)
- [var kLACredentialSmartCardPIN: Int32](/documentation/localauthentication/klacredentialsmartcardpin)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/lacredentialtype/init(rawvalue:))

### Invalidating the authentication context

- [func invalidate()](/documentation/localauthentication/lacontext/invalidate())

### Instance Properties

- [var domainState: LADomainState](/documentation/localauthentication/lacontext/domainstate)

## Persistence

- [LARightStore](/documentation/localauthentication/larightstore)

### Accessing rights

- [class var shared: LARightStore](/documentation/localauthentication/larightstore/shared)
- [func right(forIdentifier: String, completion: (LAPersistedRight?, (any Error)?) -> Void)](/documentation/localauthentication/larightstore/right(foridentifier:completion:))

### Storing rights

- [func saveRight(LARight, identifier: String, completion: (LAPersistedRight?, (any Error)?) -> Void)](/documentation/localauthentication/larightstore/saveright(_:identifier:completion:))
- [func saveRight(LARight, identifier: String, secret: Data, completion: (LAPersistedRight?, (any Error)?) -> Void)](/documentation/localauthentication/larightstore/saveright(_:identifier:secret:completion:))

### Removing stored rights

- [func removeRight(LAPersistedRight, completion: ((any Error)?) -> Void)](/documentation/localauthentication/larightstore/removeright(_:completion:))
- [func removeRight(forIdentifier: String, completion: ((any Error)?) -> Void)](/documentation/localauthentication/larightstore/removeright(foridentifier:completion:))
- [func removeAllRights(completion: ((any Error)?) -> Void)](/documentation/localauthentication/larightstore/removeallrights(completion:))
- [LAPersistedRight](/documentation/localauthentication/lapersistedright)

### Accessing persistent data

- [var key: LAPrivateKey](/documentation/localauthentication/lapersistedright/key)
- [var secret: LASecret](/documentation/localauthentication/lapersistedright/secret)
- [LASecret](/documentation/localauthentication/lasecret)

### Loading secret data

- [func loadData(completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/lasecret/loaddata(completion:))

## Key pairs

- [LAPublicKey](/documentation/localauthentication/lapublickey)

### Checking algorithm support

- [func canEncrypt(using: SecKeyAlgorithm) -> Bool](/documentation/localauthentication/lapublickey/canencrypt(using:))
- [func canVerify(using: SecKeyAlgorithm) -> Bool](/documentation/localauthentication/lapublickey/canverify(using:))

### Performing cryptographic operations

- [func encrypt(Data, algorithm: SecKeyAlgorithm, completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/lapublickey/encrypt(_:algorithm:completion:))
- [func exportBytes(completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/lapublickey/exportbytes(completion:))
- [func verify(Data, signature: Data, algorithm: SecKeyAlgorithm, completion: ((any Error)?) -> Void)](/documentation/localauthentication/lapublickey/verify(_:signature:algorithm:completion:))
- [LAPrivateKey](/documentation/localauthentication/laprivatekey)

### Accessing the associated public key

- [var publicKey: LAPublicKey](/documentation/localauthentication/laprivatekey/publickey)

### Checking algorithm support

- [func canDecrypt(using: SecKeyAlgorithm) -> Bool](/documentation/localauthentication/laprivatekey/candecrypt(using:))
- [func canExchangeKeys(using: SecKeyAlgorithm) -> Bool](/documentation/localauthentication/laprivatekey/canexchangekeys(using:))
- [func canSign(using: SecKeyAlgorithm) -> Bool](/documentation/localauthentication/laprivatekey/cansign(using:))

### Performing cryptographic operations

- [func decrypt(Data, algorithm: SecKeyAlgorithm, completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/laprivatekey/decrypt(_:algorithm:completion:))
- [func exchangeKeys(publicKey: Data, algorithm: SecKeyAlgorithm, parameters: [AnyHashable : Any], completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/laprivatekey/exchangekeys(publickey:algorithm:parameters:completion:))
- [func sign(Data, algorithm: SecKeyAlgorithm, completion: (Data?, (any Error)?) -> Void)](/documentation/localauthentication/laprivatekey/sign(_:algorithm:completion:))

## Requirements

- [LAAuthenticationRequirement](/documentation/localauthentication/laauthenticationrequirement)

### Specifying authentication requirements

- [class var `default`: LAAuthenticationRequirement](/documentation/localauthentication/laauthenticationrequirement/default)
- [class var biometry: LAAuthenticationRequirement](/documentation/localauthentication/laauthenticationrequirement/biometry)
- [class var biometryCurrentSet: LAAuthenticationRequirement](/documentation/localauthentication/laauthenticationrequirement/biometrycurrentset)
- [class func biometry(fallback: LABiometryFallbackRequirement) -> Self](/documentation/localauthentication/laauthenticationrequirement/biometry(fallback:))
- [LABiometryFallbackRequirement](/documentation/localauthentication/labiometryfallbackrequirement)

### Specifying biometric fallback requirements

- [class var `default`: LABiometryFallbackRequirement](/documentation/localauthentication/labiometryfallbackrequirement/default)
- [class var devicePasscode: LABiometryFallbackRequirement](/documentation/localauthentication/labiometryfallbackrequirement/devicepasscode)

## Authentication views

- [LocalAuthenticationView](/documentation/localauthentication/localauthenticationview)

### Authenticating with an implicit context

- [init(reason: Text, context: LAContext?, result: (Result<Void, any Error>) -> Void, label: () -> Label)](/documentation/localauthentication/localauthenticationview/init(reason:context:result:label:))
- [init<S>(S, reason: Text, context: LAContext?, result: (Result<Void, any Error>) -> Void)](/documentation/localauthentication/localauthenticationview/init(_:reason:context:result:)-8ubaq)
- [init(LocalizedStringKey, reason: Text, context: LAContext?, result: (Result<Void, any Error>) -> Void)](/documentation/localauthentication/localauthenticationview/init(_:reason:context:result:)-917ds)
- [init(Text, reason: Text, context: LAContext?, result: (Result<Void, any Error>) -> Void)](/documentation/localauthentication/localauthenticationview/init(_:reason:context:result:)-4pkpi)

### Authenticating with a context you supply

- [init<S>(S, context: LAContext)](/documentation/localauthentication/localauthenticationview/init(_:context:)-9xeoo)
- [init(context: LAContext, label: () -> Label)](/documentation/localauthentication/localauthenticationview/init(context:label:))
- [init(LocalizedStringKey, context: LAContext)](/documentation/localauthentication/localauthenticationview/init(_:context:)-676qx)

### Initializers

- [init(LocalizedStringResource, context: LAContext)](/documentation/localauthentication/localauthenticationview/init(_:context:)-7ejbu)
- [init(LocalizedStringResource, reason: Text, context: LAContext?, result: (Result<Void, any Error>) -> Void)](/documentation/localauthentication/localauthenticationview/init(_:reason:context:result:)-88u6u)

## Errors

- [LAError](/documentation/localauthentication/laerror-swift.struct)

### Error Characteristics

- [let LAErrorDomain: String](/documentation/localauthentication/laerrordomain)

### Error Codes

- [static var appCancel: LAError.Code](/documentation/localauthentication/laerror-swift.struct/appcancel)
- [static var systemCancel: LAError.Code](/documentation/localauthentication/laerror-swift.struct/systemcancel)
- [static var userCancel: LAError.Code](/documentation/localauthentication/laerror-swift.struct/usercancel)
- [static var biometryDisconnected: LAError.Code](/documentation/localauthentication/laerror-swift.struct/biometrydisconnected)
- [static var biometryLockout: LAError.Code](/documentation/localauthentication/laerror-swift.struct/biometrylockout)
- [static var biometryNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/biometrynotavailable)
- [static var biometryNotEnrolled: LAError.Code](/documentation/localauthentication/laerror-swift.struct/biometrynotenrolled)
- [static var biometryNotPaired: LAError.Code](/documentation/localauthentication/laerror-swift.struct/biometrynotpaired)
- [static var touchIDLockout: LAError.Code](/documentation/localauthentication/laerror-swift.struct/touchidlockout)
- [static var touchIDNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/touchidnotavailable)
- [static var touchIDNotEnrolled: LAError.Code](/documentation/localauthentication/laerror-swift.struct/touchidnotenrolled)
- [static var authenticationFailed: LAError.Code](/documentation/localauthentication/laerror-swift.struct/authenticationfailed)
- [static var invalidContext: LAError.Code](/documentation/localauthentication/laerror-swift.struct/invalidcontext)
- [static var invalidDimensions: LAError.Code](/documentation/localauthentication/laerror-swift.struct/invaliddimensions)
- [static var notInteractive: LAError.Code](/documentation/localauthentication/laerror-swift.struct/notinteractive)
- [static var passcodeNotSet: LAError.Code](/documentation/localauthentication/laerror-swift.struct/passcodenotset)
- [static var userFallback: LAError.Code](/documentation/localauthentication/laerror-swift.struct/userfallback)
- [static var watchNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/watchnotavailable)
- [LAError.Code](/documentation/localauthentication/laerror-swift.struct/code)

#### Cancellation

- [case appCancel](/documentation/localauthentication/laerror-swift.struct/code/appcancel)
- [case systemCancel](/documentation/localauthentication/laerror-swift.struct/code/systemcancel)
- [case userCancel](/documentation/localauthentication/laerror-swift.struct/code/usercancel)

#### Biometry failure

- [case biometryDisconnected](/documentation/localauthentication/laerror-swift.struct/code/biometrydisconnected)
- [static var biometryLockout: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrylockout)
- [static var biometryNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrynotavailable)
- [static var biometryNotEnrolled: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrynotenrolled)
- [case biometryNotPaired](/documentation/localauthentication/laerror-swift.struct/code/biometrynotpaired)
- [case touchIDLockout](/documentation/localauthentication/laerror-swift.struct/code/touchidlockout)
- [case touchIDNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/touchidnotavailable)
- [case touchIDNotEnrolled](/documentation/localauthentication/laerror-swift.struct/code/touchidnotenrolled)

#### Other errors

- [case authenticationFailed](/documentation/localauthentication/laerror-swift.struct/code/authenticationfailed)
- [case invalidContext](/documentation/localauthentication/laerror-swift.struct/code/invalidcontext)
- [case invalidDimensions](/documentation/localauthentication/laerror-swift.struct/code/invaliddimensions)
- [case notInteractive](/documentation/localauthentication/laerror-swift.struct/code/notinteractive)
- [case passcodeNotSet](/documentation/localauthentication/laerror-swift.struct/code/passcodenotset)
- [case userFallback](/documentation/localauthentication/laerror-swift.struct/code/userfallback)
- [case watchNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/watchnotavailable)

#### Supporting Constants

- [var kLAErrorDomain: String](/documentation/localauthentication/klaerrordomain)
- [var kLAErrorAppCancel: Int32](/documentation/localauthentication/klaerrorappcancel)
- [var kLAErrorSystemCancel: Int32](/documentation/localauthentication/klaerrorsystemcancel)
- [var kLAErrorUserCancel: Int32](/documentation/localauthentication/klaerrorusercancel)
- [var kLAErrorBiometryDisconnected: Int32](/documentation/localauthentication/klaerrorbiometrydisconnected)
- [var kLAErrorBiometryLockout: Int32](/documentation/localauthentication/klaerrorbiometrylockout)
- [var kLAErrorBiometryNotAvailable: Int32](/documentation/localauthentication/klaerrorbiometrynotavailable)
- [var kLAErrorBiometryNotEnrolled: Int32](/documentation/localauthentication/klaerrorbiometrynotenrolled)
- [var kLAErrorBiometryNotPaired: Int32](/documentation/localauthentication/klaerrorbiometrynotpaired)
- [var kLAErrorTouchIDLockout: Int32](/documentation/localauthentication/klaerrortouchidlockout)
- [var kLAErrorTouchIDNotAvailable: Int32](/documentation/localauthentication/klaerrortouchidnotavailable)
- [var kLAErrorTouchIDNotEnrolled: Int32](/documentation/localauthentication/klaerrortouchidnotenrolled)
- [var kLAErrorAuthenticationFailed: Int32](/documentation/localauthentication/klaerrorauthenticationfailed)
- [var kLAErrorInvalidContext: Int32](/documentation/localauthentication/klaerrorinvalidcontext)
- [var kLAErrorInvalidDimensions: Int32](/documentation/localauthentication/klaerrorinvaliddimensions)
- [var kLAErrorNotInteractive: Int32](/documentation/localauthentication/klaerrornotinteractive)
- [var kLAErrorPasscodeNotSet: Int32](/documentation/localauthentication/klaerrorpasscodenotset)
- [var kLAErrorUserFallback: Int32](/documentation/localauthentication/klaerroruserfallback)
- [var kLAErrorWatchNotAvailable: Int32](/documentation/localauthentication/klaerrorwatchnotavailable)

#### Enumeration Cases

- [case companionNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/companionnotavailable-swift.enum.case)

#### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/laerror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [static var companionNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/companionnotavailable-swift.type.property)

### Type Properties

- [static var companionNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/companionnotavailable)
- [static var errorDomain: String](/documentation/localauthentication/laerror-swift.struct/errordomain)
- [LAError.Code](/documentation/localauthentication/laerror-swift.struct/code)

### Cancellation

- [case appCancel](/documentation/localauthentication/laerror-swift.struct/code/appcancel)
- [case systemCancel](/documentation/localauthentication/laerror-swift.struct/code/systemcancel)
- [case userCancel](/documentation/localauthentication/laerror-swift.struct/code/usercancel)

### Biometry failure

- [case biometryDisconnected](/documentation/localauthentication/laerror-swift.struct/code/biometrydisconnected)
- [static var biometryLockout: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrylockout)
- [static var biometryNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrynotavailable)
- [static var biometryNotEnrolled: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/biometrynotenrolled)
- [case biometryNotPaired](/documentation/localauthentication/laerror-swift.struct/code/biometrynotpaired)
- [case touchIDLockout](/documentation/localauthentication/laerror-swift.struct/code/touchidlockout)
- [case touchIDNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/touchidnotavailable)
- [case touchIDNotEnrolled](/documentation/localauthentication/laerror-swift.struct/code/touchidnotenrolled)

### Other errors

- [case authenticationFailed](/documentation/localauthentication/laerror-swift.struct/code/authenticationfailed)
- [case invalidContext](/documentation/localauthentication/laerror-swift.struct/code/invalidcontext)
- [case invalidDimensions](/documentation/localauthentication/laerror-swift.struct/code/invaliddimensions)
- [case notInteractive](/documentation/localauthentication/laerror-swift.struct/code/notinteractive)
- [case passcodeNotSet](/documentation/localauthentication/laerror-swift.struct/code/passcodenotset)
- [case userFallback](/documentation/localauthentication/laerror-swift.struct/code/userfallback)
- [case watchNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/watchnotavailable)

### Supporting Constants

- [var kLAErrorDomain: String](/documentation/localauthentication/klaerrordomain)
- [var kLAErrorAppCancel: Int32](/documentation/localauthentication/klaerrorappcancel)
- [var kLAErrorSystemCancel: Int32](/documentation/localauthentication/klaerrorsystemcancel)
- [var kLAErrorUserCancel: Int32](/documentation/localauthentication/klaerrorusercancel)
- [var kLAErrorBiometryDisconnected: Int32](/documentation/localauthentication/klaerrorbiometrydisconnected)
- [var kLAErrorBiometryLockout: Int32](/documentation/localauthentication/klaerrorbiometrylockout)
- [var kLAErrorBiometryNotAvailable: Int32](/documentation/localauthentication/klaerrorbiometrynotavailable)
- [var kLAErrorBiometryNotEnrolled: Int32](/documentation/localauthentication/klaerrorbiometrynotenrolled)
- [var kLAErrorBiometryNotPaired: Int32](/documentation/localauthentication/klaerrorbiometrynotpaired)
- [var kLAErrorTouchIDLockout: Int32](/documentation/localauthentication/klaerrortouchidlockout)
- [var kLAErrorTouchIDNotAvailable: Int32](/documentation/localauthentication/klaerrortouchidnotavailable)
- [var kLAErrorTouchIDNotEnrolled: Int32](/documentation/localauthentication/klaerrortouchidnotenrolled)
- [var kLAErrorAuthenticationFailed: Int32](/documentation/localauthentication/klaerrorauthenticationfailed)
- [var kLAErrorInvalidContext: Int32](/documentation/localauthentication/klaerrorinvalidcontext)
- [var kLAErrorInvalidDimensions: Int32](/documentation/localauthentication/klaerrorinvaliddimensions)
- [var kLAErrorNotInteractive: Int32](/documentation/localauthentication/klaerrornotinteractive)
- [var kLAErrorPasscodeNotSet: Int32](/documentation/localauthentication/klaerrorpasscodenotset)
- [var kLAErrorUserFallback: Int32](/documentation/localauthentication/klaerroruserfallback)
- [var kLAErrorWatchNotAvailable: Int32](/documentation/localauthentication/klaerrorwatchnotavailable)

### Enumeration Cases

- [case companionNotAvailable](/documentation/localauthentication/laerror-swift.struct/code/companionnotavailable-swift.enum.case)

### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/laerror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var companionNotAvailable: LAError.Code](/documentation/localauthentication/laerror-swift.struct/code/companionnotavailable-swift.type.property)
- [let LAErrorDomain: String](/documentation/localauthentication/laerrordomain)

## Reference

- [LocalAuthentication Constants](/documentation/localauthentication/localauthentication-constants)

### Constants

- [var kLABiometryTypeFaceID: Int32](/documentation/localauthentication/klabiometrytypefaceid)
- [var kLABiometryTypeNone: Int32](/documentation/localauthentication/klabiometrytypenone)
- [var kLABiometryTypeOpticID: Int32](/documentation/localauthentication/klabiometrytypeopticid)
- [var kLABiometryTypeTouchID: Int32](/documentation/localauthentication/klabiometrytypetouchid)

## Classes

- [LADomainState](/documentation/localauthentication/ladomainstate)

### Instance Properties

- [var biometry: LADomainStateBiometry](/documentation/localauthentication/ladomainstate/biometry)
- [var companion: LADomainStateCompanion](/documentation/localauthentication/ladomainstate/companion)
- [var stateHash: Data?](/documentation/localauthentication/ladomainstate/statehash)
- [LADomainStateBiometry](/documentation/localauthentication/ladomainstatebiometry)

### Instance Properties

- [var biometryType: LABiometryType](/documentation/localauthentication/ladomainstatebiometry/biometrytype)
- [var stateHash: Data?](/documentation/localauthentication/ladomainstatebiometry/statehash)
- [LADomainStateCompanion](/documentation/localauthentication/ladomainstatecompanion)

### Instance Properties

- [var availableCompanionTypes: Set<LACompanionType>](/documentation/localauthentication/ladomainstatecompanion/availablecompaniontypes-1t7ur)
- [var stateHash: Data?](/documentation/localauthentication/ladomainstatecompanion/statehash)

### Instance Methods

- [func stateHash(for: LACompanionType) -> Data?](/documentation/localauthentication/ladomainstatecompanion/statehash(for:))
- [LAEnvironment](/documentation/localauthentication/laenvironment)

### Classes

- [LAEnvironment.Mechanism](/documentation/localauthentication/laenvironment/mechanism)

#### Instance Properties

- [var iconSystemName: String](/documentation/localauthentication/laenvironment/mechanism/iconsystemname)
- [var isUsable: Bool](/documentation/localauthentication/laenvironment/mechanism/isusable)
- [var localizedName: String](/documentation/localauthentication/laenvironment/mechanism/localizedname)
- [LAEnvironment.MechanismBiometry](/documentation/localauthentication/laenvironment/mechanismbiometry)

#### Instance Properties

- [var biometryType: LABiometryType](/documentation/localauthentication/laenvironment/mechanismbiometry/biometrytype)
- [var builtInSensorInaccessible: Bool](/documentation/localauthentication/laenvironment/mechanismbiometry/builtinsensorinaccessible)
- [var isEnrolled: Bool](/documentation/localauthentication/laenvironment/mechanismbiometry/isenrolled)
- [var isLockedOut: Bool](/documentation/localauthentication/laenvironment/mechanismbiometry/islockedout)
- [var stateHash: Data](/documentation/localauthentication/laenvironment/mechanismbiometry/statehash)
- [LAEnvironment.MechanismCompanion](/documentation/localauthentication/laenvironment/mechanismcompanion)

#### Instance Properties

- [var stateHash: Data?](/documentation/localauthentication/laenvironment/mechanismcompanion/statehash)
- [var type: LACompanionType](/documentation/localauthentication/laenvironment/mechanismcompanion/type)
- [LAEnvironment.MechanismUserPassword](/documentation/localauthentication/laenvironment/mechanismuserpassword)

#### Instance Properties

- [var isSet: Bool](/documentation/localauthentication/laenvironment/mechanismuserpassword/isset)
- [LAEnvironment.State](/documentation/localauthentication/laenvironment/state-swift.class)

#### Instance Properties

- [var allMechanisms: [LAEnvironment.Mechanism]](/documentation/localauthentication/laenvironment/state-swift.class/allmechanisms)
- [var biometry: LAEnvironment.MechanismBiometry?](/documentation/localauthentication/laenvironment/state-swift.class/biometry)
- [var companions: [LAEnvironment.MechanismCompanion]](/documentation/localauthentication/laenvironment/state-swift.class/companions)
- [var userPassword: LAEnvironment.MechanismUserPassword?](/documentation/localauthentication/laenvironment/state-swift.class/userpassword)

### Protocols

- [LAEnvironment.Observer](/documentation/localauthentication/laenvironment/observer)

#### Instance Methods

- [func environment(LAEnvironment, stateDidChangeFromOldState: LAEnvironment.State)](/documentation/localauthentication/laenvironment/observer/environment(_:statedidchangefromoldstate:))

### Instance Properties

- [var state: LAEnvironment.State](/documentation/localauthentication/laenvironment/state-swift.property)

### Instance Methods

- [func addObserver(any LAEnvironment.Observer)](/documentation/localauthentication/laenvironment/addobserver(_:))
- [func removeObserver(any LAEnvironment.Observer)](/documentation/localauthentication/laenvironment/removeobserver(_:))

### Type Properties

- [class var currentUser: LAEnvironment](/documentation/localauthentication/laenvironment/currentuser)

## Variables

- [var kLAAccessControlOperationCreateItem: Int32](/documentation/localauthentication/klaaccesscontroloperationcreateitem)
- [var kLAAccessControlOperationCreateKey: Int32](/documentation/localauthentication/klaaccesscontroloperationcreatekey)
- [var kLAAccessControlOperationUseItem: Int32](/documentation/localauthentication/klaaccesscontroloperationuseitem)
- [var kLAAccessControlOperationUseKeyDecrypt: Int32](/documentation/localauthentication/klaaccesscontroloperationusekeydecrypt)
- [var kLAAccessControlOperationUseKeyKeyExchange: Int32](/documentation/localauthentication/klaaccesscontroloperationusekeykeyexchange)
- [var kLAAccessControlOperationUseKeySign: Int32](/documentation/localauthentication/klaaccesscontroloperationusekeysign)
- [var kLACompanionTypeMac: Int32](/documentation/localauthentication/klacompaniontypemac)
- [var kLACompanionTypeNone: Int32](/documentation/localauthentication/klacompaniontypenone)
- [var kLACompanionTypeVision: Int32](/documentation/localauthentication/klacompaniontypevision)
- [var kLACompanionTypeWatch: Int32](/documentation/localauthentication/klacompaniontypewatch)
- [var kLAErrorCompanionNotAvailable: Int32](/documentation/localauthentication/klaerrorcompanionnotavailable)
- [var kLAPolicyDeviceOwnerAuthenticationWithBiometricsOrCompanion: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithbiometricsorcompanion)
- [var kLAPolicyDeviceOwnerAuthenticationWithCompanion: Int32](/documentation/localauthentication/klapolicydeviceownerauthenticationwithcompanion)

## Enumerations

- [LACompanionType](/documentation/localauthentication/lacompaniontype)

### Enumeration Cases

- [case mac](/documentation/localauthentication/lacompaniontype/mac)
- [case vision](/documentation/localauthentication/lacompaniontype/vision)
- [case watch](/documentation/localauthentication/lacompaniontype/watch)

### Initializers

- [init?(rawValue: Int)](/documentation/localauthentication/lacompaniontype/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
