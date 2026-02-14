# Authentication Services Documentation

Source: https://sosumi.ai/documentation/authenticationservices

---
title: Authentication Services
source: https://developer.apple.com/documentation/authenticationservices
timestamp: 2026-02-13T18:54:04.740Z
---

## Authorization requests

- [ASAuthorizationController](/documentation/authenticationservices/asauthorizationcontroller)

### Creating a controller

- [init(authorizationRequests: [ASAuthorizationRequest])](/documentation/authenticationservices/asauthorizationcontroller/init(authorizationrequests:))

### Inspecting requests

- [ASAuthorizationRequest](/documentation/authenticationservices/asauthorizationrequest)

#### Inspecting the Provider

- [var provider: any ASAuthorizationProvider](/documentation/authenticationservices/asauthorizationrequest/provider)
- [ASAuthorizationProvider](/documentation/authenticationservices/asauthorizationprovider)
- [var authorizationRequests: [ASAuthorizationRequest]](/documentation/authenticationservices/asauthorizationcontroller/authorizationrequests)
- [var customAuthorizationMethods: [ASAuthorizationCustomMethod]](/documentation/authenticationservices/asauthorizationcontroller/customauthorizationmethods)

### Presenting requests

- [var presentationContextProvider: (any ASAuthorizationControllerPresentationContextProviding)?](/documentation/authenticationservices/asauthorizationcontroller/presentationcontextprovider)
- [ASAuthorizationControllerPresentationContextProviding](/documentation/authenticationservices/asauthorizationcontrollerpresentationcontextproviding)

#### Specifying the Anchor

- [func presentationAnchor(for: ASAuthorizationController) -> ASPresentationAnchor](/documentation/authenticationservices/asauthorizationcontrollerpresentationcontextproviding/presentationanchor(for:))
- [ASPresentationAnchor](/documentation/authenticationservices/aspresentationanchor)

### Executing requests

- [func performRequests()](/documentation/authenticationservices/asauthorizationcontroller/performrequests())
- [func performRequests(options: ASAuthorizationController.RequestOptions)](/documentation/authenticationservices/asauthorizationcontroller/performrequests(options:))
- [func performAutoFillAssistedRequests()](/documentation/authenticationservices/asauthorizationcontroller/performautofillassistedrequests())
- [func cancel()](/documentation/authenticationservices/asauthorizationcontroller/cancel())
- [ASAuthorizationController.RequestOptions](/documentation/authenticationservices/asauthorizationcontroller/requestoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/authenticationservices/asauthorizationcontroller/requestoptions/init(rawvalue:))

#### Constants

- [static var preferImmediatelyAvailableCredentials: ASAuthorizationController.RequestOptions](/documentation/authenticationservices/asauthorizationcontroller/requestoptions/preferimmediatelyavailablecredentials)

### Responding to request completion

- [var delegate: (any ASAuthorizationControllerDelegate)?](/documentation/authenticationservices/asauthorizationcontroller/delegate)
- [func authorizationController(ASAuthorizationController, didCompleteWithCustomMethod: ASAuthorizationCustomMethod)](/documentation/authenticationservices/asauthorizationcontrollerdelegate/authorizationcontroller(_:didcompletewithcustommethod:))
- [ASAuthorizationControllerDelegate](/documentation/authenticationservices/asauthorizationcontrollerdelegate)

#### Handling Successful Authorization

- [func authorizationController(ASAuthorizationController, didCompleteWithCustomMethod: ASAuthorizationCustomMethod)](/documentation/authenticationservices/asauthorizationcontrollerdelegate/authorizationcontroller(_:didcompletewithcustommethod:))
- [func authorizationController(controller: ASAuthorizationController, didCompleteWithAuthorization: ASAuthorization)](/documentation/authenticationservices/asauthorizationcontrollerdelegate/authorizationcontroller(controller:didcompletewithauthorization:))
- [ASAuthorization](/documentation/authenticationservices/asauthorization)

##### Getting the Provider

- [var provider: any ASAuthorizationProvider](/documentation/authenticationservices/asauthorization/provider)

##### Getting the Credential

- [var credential: any ASAuthorizationCredential](/documentation/authenticationservices/asauthorization/credential)
- [ASAuthorizationCredential](/documentation/authenticationservices/asauthorizationcredential)

##### Characterizing an Authorization

- [ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope)

###### Scopes

- [static let email: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/email)
- [static let fullName: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/fullname)

###### Creating a Scope

- [init(String)](/documentation/authenticationservices/asauthorization/scope/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/scope/init(rawvalue:))
- [ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation)

###### Operation Types

- [static let operationLogin: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogin)
- [static let operationRefresh: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationrefresh)
- [static let operationLogout: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogout)
- [static let operationImplicit: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationimplicit)

###### Creating an Operation

- [init(String)](/documentation/authenticationservices/asauthorization/openidoperation/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/openidoperation/init(rawvalue:))

#### Handling Authorization Errors

- [func authorizationController(controller: ASAuthorizationController, didCompleteWithError: any Error)](/documentation/authenticationservices/asauthorizationcontrollerdelegate/authorizationcontroller(controller:didcompletewitherror:))
- [let ASAuthorizationErrorDomain: String](/documentation/authenticationservices/asauthorizationerrordomain)
- [ASAuthorizationError](/documentation/authenticationservices/asauthorizationerror-swift.struct)

##### Getting the Properties

- [static var notInteractive: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/notinteractive)

##### Error Domain

- [let ASAuthorizationErrorDomain: String](/documentation/authenticationservices/asauthorizationerrordomain)

##### Error Codes

- [static var canceled: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/canceled)
- [static var failed: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/failed)
- [static var invalidResponse: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/invalidresponse)
- [static var notHandled: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/nothandled)
- [static var unknown: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/unknown)
- [static var credentialExport: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/credentialexport)
- [static var credentialImport: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/credentialimport)
- [ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/code)

###### Codes

- [case canceled](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/canceled)
- [case failed](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/failed)
- [case invalidResponse](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/invalidresponse)
- [case notHandled](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/nothandled)
- [case unknown](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/unknown)
- [case notInteractive](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/notinteractive)
- [case credentialExport](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/credentialexport)
- [case credentialImport](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/credentialimport)

###### Enumeration Cases

- [case deviceNotConfiguredForPasskeyCreation](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/devicenotconfiguredforpasskeycreation)
- [case matchedExcludedCredential](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/matchedexcludedcredential)
- [case preferSignInWithApple](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/prefersigninwithapple)

###### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationerror-swift.struct/code/init(rawvalue:))

##### Type Properties

- [static var deviceNotConfiguredForPasskeyCreation: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/devicenotconfiguredforpasskeycreation)
- [static var errorDomain: String](/documentation/authenticationservices/asauthorizationerror-swift.struct/errordomain)
- [static var matchedExcludedCredential: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/matchedexcludedcredential)
- [static var preferSignInWithApple: ASAuthorizationError.Code](/documentation/authenticationservices/asauthorizationerror-swift.struct/prefersigninwithapple)
- [AuthorizationController](/documentation/authenticationservices/authorizationcontroller)

### Performing requests

- [func performRequest(ASAuthorizationRequest) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequest(_:))
- [func performRequests([ASAuthorizationRequest]) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequests(_:))
- [func performRequest(ASAuthorizationRequest, options: ASAuthorizationController.RequestOptions) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequest(_:options:))
- [func performRequests([ASAuthorizationRequest], options: ASAuthorizationController.RequestOptions) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequests(_:options:))
- [func performRequest(ASAuthorizationRequest, customMethods: [ASAuthorizationCustomMethod]) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequest(_:custommethods:))
- [func performRequests([ASAuthorizationRequest], customMethods: [ASAuthorizationCustomMethod]) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performrequests(_:custommethods:))

### Performing assisted requests

- [func performAutoFillAssistedRequest(ASAuthorizationRequest) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performautofillassistedrequest(_:))
- [func performAutoFillAssistedRequests([ASAuthorizationRequest]) async throws -> ASAuthorizationResult](/documentation/authenticationservices/authorizationcontroller/performautofillassistedrequests(_:))
- [ASAuthorizationResult](/documentation/authenticationservices/asauthorizationresult)

### Authorization results

- [case appleID(ASAuthorizationAppleIDCredential)](/documentation/authenticationservices/asauthorizationresult/appleid(_:))
- [case customMethod(ASAuthorizationCustomMethod)](/documentation/authenticationservices/asauthorizationresult/custommethod(_:))
- [case passkeyAssertion(ASAuthorizationPlatformPublicKeyCredentialAssertion)](/documentation/authenticationservices/asauthorizationresult/passkeyassertion(_:))
- [case passkeyRegistration(ASAuthorizationPlatformPublicKeyCredentialRegistration)](/documentation/authenticationservices/asauthorizationresult/passkeyregistration(_:))
- [case password(ASPasswordCredential)](/documentation/authenticationservices/asauthorizationresult/password(_:))
- [case securityKeyAssertion(ASAuthorizationSecurityKeyPublicKeyCredentialAssertion)](/documentation/authenticationservices/asauthorizationresult/securitykeyassertion(_:))
- [case securityKeyRegistration(ASAuthorizationSecurityKeyPublicKeyCredentialRegistration)](/documentation/authenticationservices/asauthorizationresult/securitykeyregistration(_:))

### Enumeration Cases

- [case passkeyAccountCreation(ASAuthorizationAccountCreationPlatformPublicKeyCredential)](/documentation/authenticationservices/asauthorizationresult/passkeyaccountcreation(_:))

## Sign In with Apple

- [Implementing User Authentication with Sign in with Apple](/documentation/authenticationservices/implementing-user-authentication-with-sign-in-with-apple)
- [Simplifying User Authentication in a tvOS App](/documentation/authenticationservices/simplifying-user-authentication-in-a-tvos-app)
- [SignInWithAppleButton](/documentation/authenticationservices/signinwithapplebutton)

### Creating a button

- [init(SignInWithAppleButton.Label, onRequest: (ASAuthorizationAppleIDRequest) -> Void, onCompletion: (Result<ASAuthorization, any Error>) -> Void)](/documentation/authenticationservices/signinwithapplebutton/init(_:onrequest:oncompletion:))
- [SignInWithAppleButton.Label](/documentation/authenticationservices/signinwithapplebutton/label)

#### Labels

- [static let `continue`: SignInWithAppleButton.Label](/documentation/authenticationservices/signinwithapplebutton/label/continue)
- [static let signIn: SignInWithAppleButton.Label](/documentation/authenticationservices/signinwithapplebutton/label/signin)
- [static let signUp: SignInWithAppleButton.Label](/documentation/authenticationservices/signinwithapplebutton/label/signup)
- [SignInWithAppleButton.Style](/documentation/authenticationservices/signinwithapplebutton/style)

#### Styles

- [static let black: SignInWithAppleButton.Style](/documentation/authenticationservices/signinwithapplebutton/style/black)
- [static let white: SignInWithAppleButton.Style](/documentation/authenticationservices/signinwithapplebutton/style/white)
- [static let whiteOutline: SignInWithAppleButton.Style](/documentation/authenticationservices/signinwithapplebutton/style/whiteoutline)
- [Sign in with Apple Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.applesignin)
- [ASAuthorizationAppleIDProvider](/documentation/authenticationservices/asauthorizationappleidprovider)

### Offering Sign In with Apple

- [ASAuthorizationAppleIDButton](/documentation/authenticationservices/asauthorizationappleidbutton)

#### Initializers

- [init(authorizationButtonType: ASAuthorizationAppleIDButton.ButtonType, authorizationButtonStyle: ASAuthorizationAppleIDButton.Style)](/documentation/authenticationservices/asauthorizationappleidbutton/init(authorizationbuttontype:authorizationbuttonstyle:))
- [convenience init(type: ASAuthorizationAppleIDButton.ButtonType, style: ASAuthorizationAppleIDButton.Style)](/documentation/authenticationservices/asauthorizationappleidbutton/init(type:style:))

#### Styling the Button

- [var cornerRadius: CGFloat](/documentation/authenticationservices/asauthorizationappleidbutton/cornerradius)
- [ASAuthorizationAppleIDButton.Style](/documentation/authenticationservices/asauthorizationappleidbutton/style)

##### Choosing a Button Style

- [case black](/documentation/authenticationservices/asauthorizationappleidbutton/style/black)
- [case white](/documentation/authenticationservices/asauthorizationappleidbutton/style/white)
- [case whiteOutline](/documentation/authenticationservices/asauthorizationappleidbutton/style/whiteoutline)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationappleidbutton/style/init(rawvalue:))
- [ASAuthorizationAppleIDButton.ButtonType](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype)

##### Choosing a Button Type

- [case `continue`](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype/continue)
- [static var `default`: ASAuthorizationAppleIDButton.ButtonType](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype/default)
- [case signUp](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype/signup)
- [case signIn](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype/signin)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationappleidbutton/buttontype/init(rawvalue:))
- [WKInterfaceAuthorizationAppleIDButton](/documentation/watchkit/wkinterfaceauthorizationappleidbutton)

### Creating Requests

- [func createRequest() -> ASAuthorizationAppleIDRequest](/documentation/authenticationservices/asauthorizationappleidprovider/createrequest())
- [ASAuthorizationAppleIDRequest](/documentation/authenticationservices/asauthorizationappleidrequest)

#### Setting the User

- [var user: String?](/documentation/authenticationservices/asauthorizationappleidrequest/user)
- [ASAuthorizationOpenIDRequest](/documentation/authenticationservices/asauthorizationopenidrequest)

#### Setting the Operation

- [var requestedOperation: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorizationopenidrequest/requestedoperation)
- [ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation)

##### Operation Types

- [static let operationLogin: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogin)
- [static let operationRefresh: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationrefresh)
- [static let operationLogout: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogout)
- [static let operationImplicit: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationimplicit)

##### Creating an Operation

- [init(String)](/documentation/authenticationservices/asauthorization/openidoperation/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/openidoperation/init(rawvalue:))

#### Setting the Scope

- [var requestedScopes: [ASAuthorization.Scope]?](/documentation/authenticationservices/asauthorizationopenidrequest/requestedscopes)
- [ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope)

##### Scopes

- [static let email: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/email)
- [static let fullName: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/fullname)

##### Creating a Scope

- [init(String)](/documentation/authenticationservices/asauthorization/scope/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/scope/init(rawvalue:))

#### Setting the State

- [var state: String?](/documentation/authenticationservices/asauthorizationopenidrequest/state)

#### Setting the Nonce

- [var nonce: String?](/documentation/authenticationservices/asauthorizationopenidrequest/nonce)

### Getting State

- [func getCredentialState(forUserID: String, completion: (ASAuthorizationAppleIDProvider.CredentialState, (any Error)?) -> Void)](/documentation/authenticationservices/asauthorizationappleidprovider/getcredentialstate(foruserid:completion:))
- [ASAuthorizationAppleIDProvider.CredentialState](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate)

#### User Credential States

- [case authorized](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate/authorized)
- [case notFound](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate/notfound)
- [case revoked](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate/revoked)
- [case transferred](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate/transferred)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationappleidprovider/credentialstate/init(rawvalue:))
- [class let credentialRevokedNotification: NSNotification.Name](/documentation/authenticationservices/asauthorizationappleidprovider/credentialrevokednotification)
- [ASAuthorizationAppleIDCredential](/documentation/authenticationservices/asauthorizationappleidcredential)

### Identifying a User

- [var identityToken: Data?](/documentation/authenticationservices/asauthorizationappleidcredential/identitytoken)
- [var authorizationCode: Data?](/documentation/authenticationservices/asauthorizationappleidcredential/authorizationcode)
- [var state: String?](/documentation/authenticationservices/asauthorizationappleidcredential/state)
- [var user: String](/documentation/authenticationservices/asauthorizationappleidcredential/user)

### Getting Contact Information

- [var authorizedScopes: [ASAuthorization.Scope]](/documentation/authenticationservices/asauthorizationappleidcredential/authorizedscopes)
- [var fullName: PersonNameComponents?](/documentation/authenticationservices/asauthorizationappleidcredential/fullname)
- [var email: String?](/documentation/authenticationservices/asauthorizationappleidcredential/email)

### Detecting User Characteristics

- [var realUserStatus: ASUserDetectionStatus](/documentation/authenticationservices/asauthorizationappleidcredential/realuserstatus)
- [ASUserDetectionStatus](/documentation/authenticationservices/asuserdetectionstatus)

#### User Status

- [case likelyReal](/documentation/authenticationservices/asuserdetectionstatus/likelyreal)
- [case unknown](/documentation/authenticationservices/asuserdetectionstatus/unknown)
- [case unsupported](/documentation/authenticationservices/asuserdetectionstatus/unsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asuserdetectionstatus/init(rawvalue:))

### Instance Properties

- [var userAgeRange: ASUserAgeRange](/documentation/authenticationservices/asauthorizationappleidcredential/useragerange)

## Passwords

- [Password AutoFill](/documentation/security/password-autofill)
- [ASAuthorizationPasswordProvider](/documentation/authenticationservices/asauthorizationpasswordprovider)

### Creating Requests

- [func createRequest() -> ASAuthorizationPasswordRequest](/documentation/authenticationservices/asauthorizationpasswordprovider/createrequest())
- [ASAuthorizationPasswordRequest](/documentation/authenticationservices/asauthorizationpasswordrequest)
- [ASPasswordCredential](/documentation/authenticationservices/aspasswordcredential)

### Creating a credential

- [init(user: String, password: String)](/documentation/authenticationservices/aspasswordcredential/init(user:password:))

### Accessing the username and password

- [var user: String](/documentation/authenticationservices/aspasswordcredential/user)
- [var password: String](/documentation/authenticationservices/aspasswordcredential/password)
- [Password use in web browsers](/documentation/authenticationservices/password-use-in-web-browsers)

### Website authorization

- [ASAuthorizationWebBrowserPublicKeyCredentialManager](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager)

#### Creating credential managers

- [init()](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/init())

#### Requesting access to passkeys

- [var authorizationStateForPlatformCredentials: ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstateforplatformcredentials)
- [func requestAuthorizationForPublicKeyCredentials((ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState) -> Void)](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/requestauthorizationforpublickeycredentials(_:))
- [ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate)

##### Passkey access states

- [case authorized](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/authorized)
- [case denied](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/denied)
- [case notDetermined](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/notdetermined)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/init(rawvalue:))

#### Using passkeys

- [func platformCredentials(forRelyingParty: String) async -> [ASAuthorizationWebBrowserPlatformPublicKeyCredential]](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/platformcredentials(forrelyingparty:))
- [ASAuthorizationWebBrowserPlatformPublicKeyCredential](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct)

##### Describing credentials

- [let customTitle: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/customtitle)
- [let name: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/name)
- [let providerName: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/providername)
- [let relyingParty: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/relyingparty)
- [let userHandle: Data](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/userhandle)

##### Identifying credentials

- [let credentialID: Data](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/credentialid)

#### Type Properties

- [class var isDeviceConfiguredForPasskeys: Bool](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/isdeviceconfiguredforpasskeys)

### Website authentication requests

- [ASAuthorizationWebBrowserSecurityKeyPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialassertionrequest)

#### Information about the assertion

- [var clientData: ASPublicKeyCredentialClientData?](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialassertionrequest/clientdata-1ld1w)
- [ASAuthorizationWebBrowserSecurityKeyPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialregistrationrequest)

#### Information about the registration

- [var clientData: ASPublicKeyCredentialClientData?](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialregistrationrequest/clientdata-3hz81)

### Website credential providers

- [ASAuthorizationWebBrowserSecurityKeyPublicKeyCredentialProvider](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialprovider-8xc1s)

#### Creating credential assertion requests

- [func createCredentialAssertionRequest(clientData: ASPublicKeyCredentialClientData) -> ASAuthorizationSecurityKeyPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialprovider-8xc1s/createcredentialassertionrequest(clientdata:))
- [func createCredentialRegistrationRequest(clientData: ASPublicKeyCredentialClientData, displayName: String, name: String, userID: Data) -> ASAuthorizationSecurityKeyPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationwebbrowsersecuritykeypublickeycredentialprovider-8xc1s/createcredentialregistrationrequest(clientdata:displayname:name:userid:))

## Passkeys

- [Public-Private Key Authentication](/documentation/authenticationservices/public-private-key-authentication)

### Fundamentals

- [Connecting to a service with passkeys](/documentation/authenticationservices/connecting-to-a-service-with-passkeys)
- [Supporting passkeys](/documentation/authenticationservices/supporting-passkeys)
- [Supporting Security Key Authentication Using Physical Keys](/documentation/authenticationservices/supporting-security-key-authentication-using-physical-keys)

### Account registration

- [ASAuthorizationPublicKeyCredentialRegistration](/documentation/authenticationservices/asauthorizationpublickeycredentialregistration)

#### Getting attestation information

- [var rawAttestationObject: Data?](/documentation/authenticationservices/asauthorizationpublickeycredentialregistration/rawattestationobject)
- [ASAuthorizationPlatformPublicKeyCredentialRegistration](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistration)

#### Accessing registration properties

- [var attachment: ASAuthorizationPublicKeyCredentialAttachment](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistration/attachment)
- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistration/largeblob-5nvj9)

#### Instance Properties

- [var prf: ASAuthorizationPublicKeyCredentialPRFRegistrationOutput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistration/prf-3xcqu)
- [ASAuthorizationSecurityKeyPublicKeyCredentialRegistration](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistration)

#### Instance Properties

- [var transports: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistration/transports)
- [ASAuthorizationPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest)

#### Getting the properties

- [var attestationPreference: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/attestationpreference)
- [var challenge: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/challenge)
- [var displayName: String?](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/displayname)
- [var name: String](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/name)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/relyingpartyidentifier)
- [var userID: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/userid)
- [var userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/userverificationpreference)
- [ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest)

#### Accessing request properties

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/largeblob-5ismm)

#### Instance Properties

- [var prf: ASAuthorizationPublicKeyCredentialPRFRegistrationInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/prf-3d9iw)
- [var requestStyle: ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest.RequestStyle](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/requeststyle-swift.property)

#### Enumerations

- [ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest.RequestStyle](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/requeststyle-swift.enum)

##### Enumeration Cases

- [case conditional](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/requeststyle-swift.enum/conditional)
- [case standard](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/requeststyle-swift.enum/standard)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialregistrationrequest/requeststyle-swift.enum/init(rawvalue:))
- [ASAuthorizationSecurityKeyPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistrationrequest)

#### Getting the properties

- [var credentialParameters: [ASAuthorizationPublicKeyCredentialParameters]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistrationrequest/credentialparameters)
- [var excludedCredentials: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistrationrequest/excludedcredentials)
- [var residentKeyPreference: ASAuthorizationPublicKeyCredentialResidentKeyPreference](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialregistrationrequest/residentkeypreference)

### Account authentication

- [ASAuthorizationPublicKeyCredentialAssertion](/documentation/authenticationservices/asauthorizationpublickeycredentialassertion)

#### Getting the properties

- [var signature: Data!](/documentation/authenticationservices/asauthorizationpublickeycredentialassertion/signature)
- [var userID: Data!](/documentation/authenticationservices/asauthorizationpublickeycredentialassertion/userid)
- [var rawAuthenticatorData: Data!](/documentation/authenticationservices/asauthorizationpublickeycredentialassertion/rawauthenticatordata)
- [ASAuthorizationPlatformPublicKeyCredentialAssertion](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertion)

#### Creating requests

- [ASAuthorizationPlatformPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest)

##### Accessing request properties

- [var allowedCredentials: [ASAuthorizationPlatformPublicKeyCredentialDescriptor]](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/allowedcredentials)
- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/largeblob-9kvvl)
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/prf-47uoa)

##### Instance Properties

- [var prf: __ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/prf-60tle)
- [ASAuthorizationPlatformPublicKeyCredentialDescriptor](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialdescriptor)

##### Creating the descriptor

- [init(credentialID: Data)](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialdescriptor/init(credentialid:))

#### Accessing assertion properties

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertion/largeblob-29ggs)

#### Instance Properties

- [var attachment: ASAuthorizationPublicKeyCredentialAttachment](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertion/attachment)
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionOutput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertion/prf-8o9sr)
- [ASAuthorizationSecurityKeyPublicKeyCredentialAssertion](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialassertion)

#### Instance Properties

- [var appID: Bool](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialassertion/appid)
- [ASAuthorizationPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationpublickeycredentialassertionrequest)

#### Getting the properties

- [var challenge: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialassertionrequest/challenge)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationpublickeycredentialassertionrequest/relyingpartyidentifier)
- [var allowedCredentials: [any ASAuthorizationPublicKeyCredentialDescriptor]](/documentation/authenticationservices/asauthorizationpublickeycredentialassertionrequest/allowedcredentials)
- [var userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialassertionrequest/userverificationpreference)
- [ASAuthorizationPlatformPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest)

#### Accessing request properties

- [var allowedCredentials: [ASAuthorizationPlatformPublicKeyCredentialDescriptor]](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/allowedcredentials)
- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/largeblob-9kvvl)
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/prf-47uoa)

#### Instance Properties

- [var prf: __ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialassertionrequest/prf-60tle)
- [ASAuthorizationSecurityKeyPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialassertionrequest)

#### Getting the properties

- [var allowedCredentials: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialassertionrequest/allowedcredentials)

#### Instance Properties

- [var appID: String?](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialassertionrequest/appid)

### Credential providers

- [ASAuthorizationPlatformPublicKeyCredentialProvider](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider)

#### Creating the provider

- [init(relyingPartyIdentifier: String)](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider/init(relyingpartyidentifier:))

#### Creating the request

- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider/relyingpartyidentifier)
- [func createCredentialAssertionRequest(challenge: Data) -> ASAuthorizationPlatformPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider/createcredentialassertionrequest(challenge:))
- [func createCredentialRegistrationRequest(challenge: Data, name: String, userID: Data) -> ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider/createcredentialregistrationrequest(challenge:name:userid:))
- [func createCredentialRegistrationRequest(challenge: Data, name: String, userID: Data, requestStyle: ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest.RequestStyle) -> ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialprovider/createcredentialregistrationrequest(challenge:name:userid:requeststyle:))
- [ASAuthorizationSecurityKeyPublicKeyCredentialProvider](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialprovider)

#### Creating the provider

- [init(relyingPartyIdentifier: String)](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialprovider/init(relyingpartyidentifier:))

#### Creating the request

- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialprovider/relyingpartyidentifier)
- [func createCredentialAssertionRequest(challenge: Data) -> ASAuthorizationSecurityKeyPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialprovider/createcredentialassertionrequest(challenge:))
- [func createCredentialRegistrationRequest(challenge: Data, displayName: String, name: String, userID: Data) -> ASAuthorizationSecurityKeyPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialprovider/createcredentialregistrationrequest(challenge:displayname:name:userid:))

### Request configuration

- [ASPublicKeyCredential](/documentation/authenticationservices/aspublickeycredential)

#### Getting the properties

- [var credentialID: Data](/documentation/authenticationservices/aspublickeycredential/credentialid)
- [var rawClientDataJSON: Data](/documentation/authenticationservices/aspublickeycredential/rawclientdatajson)
- [ASAuthorizationPublicKeyCredentialParameters](/documentation/authenticationservices/asauthorizationpublickeycredentialparameters)

#### Getting the parameters

- [init(algorithm: ASCOSEAlgorithmIdentifier)](/documentation/authenticationservices/asauthorizationpublickeycredentialparameters/init(algorithm:))
- [var algorithm: ASCOSEAlgorithmIdentifier](/documentation/authenticationservices/asauthorizationpublickeycredentialparameters/algorithm)
- [ASCOSEAlgorithmIdentifier](/documentation/authenticationservices/ascosealgorithmidentifier)

#### Creating the identifier

- [init(Int)](/documentation/authenticationservices/ascosealgorithmidentifier/init(_:))
- [init(rawValue: Int)](/documentation/authenticationservices/ascosealgorithmidentifier/init(rawvalue:))
- [static let ES256: ASCOSEAlgorithmIdentifier](/documentation/authenticationservices/ascosealgorithmidentifier/es256)
- [ASCOSEEllipticCurveIdentifier](/documentation/authenticationservices/ascoseellipticcurveidentifier)

#### Creating the identifier

- [init(Int)](/documentation/authenticationservices/ascoseellipticcurveidentifier/init(_:))
- [init(rawValue: Int)](/documentation/authenticationservices/ascoseellipticcurveidentifier/init(rawvalue:))

#### Getting the properties

- [static let P256: ASCOSEEllipticCurveIdentifier](/documentation/authenticationservices/ascoseellipticcurveidentifier/p256)
- [ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind)

#### Creating the attestation type

- [init(String)](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/init(rawvalue:))

#### Getting attestation types

- [static let none: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/none)
- [static let direct: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/direct)
- [static let enterprise: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/enterprise)
- [static let indirect: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialattestationkind/indirect)
- [ASAuthorizationPublicKeyCredentialResidentKeyPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference)

#### Creating the preference

- [init(String)](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference/init(rawvalue:))

#### Getting preferences

- [static let discouraged: ASAuthorizationPublicKeyCredentialResidentKeyPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference/discouraged)
- [static let preferred: ASAuthorizationPublicKeyCredentialResidentKeyPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference/preferred)
- [static let required: ASAuthorizationPublicKeyCredentialResidentKeyPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialresidentkeypreference/required)
- [ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference)

#### Creating the preference

- [init(String)](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference/init(rawvalue:))

#### Getting preferences

- [static let discouraged: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference/discouraged)
- [static let preferred: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference/preferred)
- [static let required: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialuserverificationpreference/required)
- [ASAuthorizationPublicKeyCredentialDescriptor](/documentation/authenticationservices/asauthorizationpublickeycredentialdescriptor)

#### Getting the credential

- [var credentialID: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialdescriptor/credentialid)
- [ASAuthorizationPlatformPublicKeyCredentialDescriptor](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialdescriptor)

#### Creating the descriptor

- [init(credentialID: Data)](/documentation/authenticationservices/asauthorizationplatformpublickeycredentialdescriptor/init(credentialid:))
- [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor)

#### Creating the descriptor

- [init(credentialID: Data, transports: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport])](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/init(credentialid:transports:))
- [var transports: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transports)
- [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport)

##### Creating the transport type

- [init(String)](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/init(rawvalue:))

##### Getting the properties

- [static var allSupported: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/allsupported)
- [static let bluetooth: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/bluetooth)
- [static let nfc: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/nfc)
- [static let usb: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/usb)
- [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport)

#### Creating the transport type

- [init(String)](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/init(rawvalue:))

#### Getting the properties

- [static var allSupported: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/allsupported)
- [static let bluetooth: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/bluetooth)
- [static let nfc: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/nfc)
- [static let usb: ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/usb)
- [static var allSupported: [ASAuthorizationSecurityKeyPublicKeyCredentialDescriptor.Transport]](/documentation/authenticationservices/asauthorizationsecuritykeypublickeycredentialdescriptor/transport/allsupported)
- [Passkey use in web browsers](/documentation/authenticationservices/passkey-use-in-web-browsers)

### Website authorization

- [Authenticating people by using passkeys in browser apps](/documentation/authenticationservices/authenticating-people-by-using-passkeys-in-browser-apps)
- [ASAuthorizationWebBrowserPublicKeyCredentialManager](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager)

#### Creating credential managers

- [init()](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/init())

#### Requesting access to passkeys

- [var authorizationStateForPlatformCredentials: ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstateforplatformcredentials)
- [func requestAuthorizationForPublicKeyCredentials((ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState) -> Void)](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/requestauthorizationforpublickeycredentials(_:))
- [ASAuthorizationWebBrowserPublicKeyCredentialManager.AuthorizationState](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate)

##### Passkey access states

- [case authorized](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/authorized)
- [case denied](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/denied)
- [case notDetermined](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/notdetermined)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/authorizationstate/init(rawvalue:))

#### Using passkeys

- [func platformCredentials(forRelyingParty: String) async -> [ASAuthorizationWebBrowserPlatformPublicKeyCredential]](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/platformcredentials(forrelyingparty:))
- [ASAuthorizationWebBrowserPlatformPublicKeyCredential](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct)

##### Describing credentials

- [let customTitle: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/customtitle)
- [let name: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/name)
- [let providerName: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/providername)
- [let relyingParty: String](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/relyingparty)
- [let userHandle: Data](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/userhandle)

##### Identifying credentials

- [let credentialID: Data](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredential-swift.struct/credentialid)

#### Type Properties

- [class var isDeviceConfiguredForPasskeys: Bool](/documentation/authenticationservices/asauthorizationwebbrowserpublickeycredentialmanager/isdeviceconfiguredforpasskeys)

### Website authentication requests

- [ASAuthorizationWebBrowserExternallyAuthenticatableRequest](/documentation/authenticationservices/asauthorizationwebbrowserexternallyauthenticatablerequest)

#### Local authentication

- [var authenticatedContext: LAContext?](/documentation/authenticationservices/asauthorizationwebbrowserexternallyauthenticatablerequest/authenticatedcontext)
- [ASAuthorizationWebBrowserPlatformPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialassertionrequest)

#### Information about the assertion

- [var clientData: ASPublicKeyCredentialClientData?](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialassertionrequest/clientdata-655pi)
- [var shouldShowHybridTransport: Bool](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialassertionrequest/shouldshowhybridtransport)
- [ASAuthorizationWebBrowserPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialregistrationrequest)

#### Information about the assertion

- [var clientData: ASPublicKeyCredentialClientData?](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialregistrationrequest/clientdata-5dk66)
- [var excludedCredentials: [ASAuthorizationPlatformPublicKeyCredentialDescriptor]?](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialregistrationrequest/excludedcredentials)
- [var shouldShowHybridTransport: Bool](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialregistrationrequest/shouldshowhybridtransport)

### Website credential providers

- [ASAuthorizationWebBrowserPlatformPublicKeyCredentialProvider](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialprovider-19bq)

#### Creating requests

- [func createCredentialAssertionRequest(clientData: ASPublicKeyCredentialClientData) -> ASAuthorizationPlatformPublicKeyCredentialAssertionRequest](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialprovider-19bq/createcredentialassertionrequest(clientdata:))
- [func createCredentialRegistrationRequest(clientData: ASPublicKeyCredentialClientData, name: String, userID: Data) -> ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialprovider-19bq/createcredentialregistrationrequest(clientdata:name:userid:))
- [func createCredentialRegistrationRequest(clientData: ASPublicKeyCredentialClientData, name: String, userID: Data, requestStyle: ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest.RequestStyle) -> ASAuthorizationPlatformPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationwebbrowserplatformpublickeycredentialprovider-19bq/createcredentialregistrationrequest(clientdata:name:userid:requeststyle:))
- [Performing fast account creation with passkeys](/documentation/authenticationservices/performing-fast-account-creation-with-passkeys)
- [Connecting to a service with passkeys](/documentation/authenticationservices/connecting-to-a-service-with-passkeys)

## Web authentication sessions

- [Authenticating a User Through a Web Service](/documentation/authenticationservices/authenticating-a-user-through-a-web-service)
- [Securing Logins with iCloud Keychain Verification Codes](/documentation/authenticationservices/securing-logins-with-icloud-keychain-verification-codes)
- [ASWebAuthenticationSession](/documentation/authenticationservices/aswebauthenticationsession)

### Creating a session

- [init(url: URL, callback: ASWebAuthenticationSession.Callback, completionHandler: ASWebAuthenticationSession.CompletionHandler)](/documentation/authenticationservices/aswebauthenticationsession/init(url:callback:completionhandler:))
- [ASWebAuthenticationSession.Callback](/documentation/authenticationservices/aswebauthenticationsession/callback)

#### Creating callbacks

- [class func customScheme(String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/customscheme(_:))
- [class func https(host: String, path: String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/https(host:path:))

#### Evaluating URLs

- [func matchesURL(URL) -> Bool](/documentation/authenticationservices/aswebauthenticationsession/callback/matchesurl(_:))
- [ASWebAuthenticationSession.CompletionHandler](/documentation/authenticationservices/aswebauthenticationsession/completionhandler)

### Configuring a session

- [var prefersEphemeralWebBrowserSession: Bool](/documentation/authenticationservices/aswebauthenticationsession/prefersephemeralwebbrowsersession)

### Starting and Stopping a Session

- [var canStart: Bool](/documentation/authenticationservices/aswebauthenticationsession/canstart)
- [func start() -> Bool](/documentation/authenticationservices/aswebauthenticationsession/start())
- [func cancel()](/documentation/authenticationservices/aswebauthenticationsession/cancel())

### Presenting a Session

- [var presentationContextProvider: (any ASWebAuthenticationPresentationContextProviding)?](/documentation/authenticationservices/aswebauthenticationsession/presentationcontextprovider)
- [ASWebAuthenticationPresentationContextProviding](/documentation/authenticationservices/aswebauthenticationpresentationcontextproviding)

#### Specifying the Anchor

- [func presentationAnchor(for: ASWebAuthenticationSession) -> ASPresentationAnchor](/documentation/authenticationservices/aswebauthenticationpresentationcontextproviding/presentationanchor(for:))
- [ASPresentationAnchor](/documentation/authenticationservices/aspresentationanchor)

### Recognizing Errors

- [ASWebAuthenticationSessionError](/documentation/authenticationservices/aswebauthenticationsessionerror)

#### Error Domain

- [let ASWebAuthenticationSessionErrorDomain: String](/documentation/authenticationservices/aswebauthenticationsessionerrordomain)

#### Error Codes

- [static var canceledLogin: ASWebAuthenticationSessionError.Code](/documentation/authenticationservices/aswebauthenticationsessionerror/canceledlogin)
- [static var presentationContextNotProvided: ASWebAuthenticationSessionError.Code](/documentation/authenticationservices/aswebauthenticationsessionerror/presentationcontextnotprovided)
- [static var presentationContextInvalid: ASWebAuthenticationSessionError.Code](/documentation/authenticationservices/aswebauthenticationsessionerror/presentationcontextinvalid)
- [ASWebAuthenticationSessionError.Code](/documentation/authenticationservices/aswebauthenticationsessionerror/code)

##### Codes

- [case canceledLogin](/documentation/authenticationservices/aswebauthenticationsessionerror/code/canceledlogin)
- [case presentationContextNotProvided](/documentation/authenticationservices/aswebauthenticationsessionerror/code/presentationcontextnotprovided)
- [case presentationContextInvalid](/documentation/authenticationservices/aswebauthenticationsessionerror/code/presentationcontextinvalid)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/aswebauthenticationsessionerror/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/authenticationservices/aswebauthenticationsessionerror/errordomain)
- [let ASWebAuthenticationSessionErrorDomain: String](/documentation/authenticationservices/aswebauthenticationsessionerrordomain)
- [ASWebAuthenticationSessionError.Code](/documentation/authenticationservices/aswebauthenticationsessionerror/code)

#### Codes

- [case canceledLogin](/documentation/authenticationservices/aswebauthenticationsessionerror/code/canceledlogin)
- [case presentationContextNotProvided](/documentation/authenticationservices/aswebauthenticationsessionerror/code/presentationcontextnotprovided)
- [case presentationContextInvalid](/documentation/authenticationservices/aswebauthenticationsessionerror/code/presentationcontextinvalid)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/aswebauthenticationsessionerror/code/init(rawvalue:))

### Instance properties

- [var additionalHeaderFields: [String : String]?](/documentation/authenticationservices/aswebauthenticationsession/additionalheaderfields)

### Deprecated symbols

- [init(url: URL, callbackURLScheme: String?, completionHandler: ASWebAuthenticationSession.CompletionHandler)](/documentation/authenticationservices/aswebauthenticationsession/init(url:callbackurlscheme:completionhandler:))
- [WebAuthenticationSession](/documentation/authenticationservices/webauthenticationsession)

### Authenticating a session

- [func authenticate(using: URL, callback: ASWebAuthenticationSession.Callback, preferredBrowserSession: WebAuthenticationSession.BrowserSession?, additionalHeaderFields: [String : String]) async throws -> URL](/documentation/authenticationservices/webauthenticationsession/authenticate(using:callback:preferredbrowsersession:additionalheaderfields:))
- [WebAuthenticationSession.BrowserSession](/documentation/authenticationservices/webauthenticationsession/browsersession)

#### Behaviors

- [static var ephemeral: WebAuthenticationSession.BrowserSession](/documentation/authenticationservices/webauthenticationsession/browsersession/ephemeral)
- [static var shared: WebAuthenticationSession.BrowserSession](/documentation/authenticationservices/webauthenticationsession/browsersession/shared)
- [ASWebAuthenticationSession.Callback](/documentation/authenticationservices/aswebauthenticationsession/callback)

#### Creating callbacks

- [class func customScheme(String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/customscheme(_:))
- [class func https(host: String, path: String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/https(host:path:))

#### Evaluating URLs

- [func matchesURL(URL) -> Bool](/documentation/authenticationservices/aswebauthenticationsession/callback/matchesurl(_:))

### Deprecated methods

- [func authenticate(using: URL, callbackURLScheme: String, preferredBrowserSession: WebAuthenticationSession.BrowserSession?) async throws -> URL](/documentation/authenticationservices/webauthenticationsession/authenticate(using:callbackurlscheme:preferredbrowsersession:))
- [Supporting Single Sign-On in a Web Browser App](/documentation/authenticationservices/supporting-single-sign-on-in-a-web-browser-app)
- [ASWebAuthenticationSessionWebBrowserSessionManager](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionmanager)

### Getting the Shared Manager

- [class var shared: ASWebAuthenticationSessionWebBrowserSessionManager](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionmanager/shared)

### Handling a Session Request

- [var sessionHandler: any ASWebAuthenticationSessionWebBrowserSessionHandling](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionmanager/sessionhandler)
- [ASWebAuthenticationSessionWebBrowserSessionHandling](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionhandling)

#### Starting and Stopping a Session Request

- [func begin(ASWebAuthenticationSessionRequest!)](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionhandling/begin(_:))
- [func cancel(ASWebAuthenticationSessionRequest!)](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionhandling/cancel(_:))
- [ASWebAuthenticationSessionRequest](/documentation/authenticationservices/aswebauthenticationsessionrequest)

##### Interpreting a request

- [var url: URL](/documentation/authenticationservices/aswebauthenticationsessionrequest/url)
- [var shouldUseEphemeralSession: Bool](/documentation/authenticationservices/aswebauthenticationsessionrequest/shoulduseephemeralsession)
- [var uuid: UUID](/documentation/authenticationservices/aswebauthenticationsessionrequest/uuid)
- [var additionalHeaderFields: [String : String]?](/documentation/authenticationservices/aswebauthenticationsessionrequest/additionalheaderfields)

##### Finishing a request

- [var callback: ASWebAuthenticationSession.Callback?](/documentation/authenticationservices/aswebauthenticationsessionrequest/callback)
- [ASWebAuthenticationSession.Callback](/documentation/authenticationservices/aswebauthenticationsession/callback)

###### Creating callbacks

- [class func customScheme(String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/customscheme(_:))
- [class func https(host: String, path: String) -> Self](/documentation/authenticationservices/aswebauthenticationsession/callback/https(host:path:))

###### Evaluating URLs

- [func matchesURL(URL) -> Bool](/documentation/authenticationservices/aswebauthenticationsession/callback/matchesurl(_:))
- [func complete(withCallbackURL: URL)](/documentation/authenticationservices/aswebauthenticationsessionrequest/complete(withcallbackurl:))
- [func cancelWithError(any Error)](/documentation/authenticationservices/aswebauthenticationsessionrequest/cancelwitherror(_:))

##### Indicating completion

- [var delegate: (any ASWebAuthenticationSessionRequestDelegate)?](/documentation/authenticationservices/aswebauthenticationsessionrequest/delegate)
- [ASWebAuthenticationSessionRequestDelegate](/documentation/authenticationservices/aswebauthenticationsessionrequestdelegate)

###### Responding to Completion Events

- [func authenticationSessionRequest(ASWebAuthenticationSessionRequest, didCompleteWithCallbackURL: URL)](/documentation/authenticationservices/aswebauthenticationsessionrequestdelegate/authenticationsessionrequest(_:didcompletewithcallbackurl:))
- [func authenticationSessionRequest(ASWebAuthenticationSessionRequest, didCancelWithError: any Error)](/documentation/authenticationservices/aswebauthenticationsessionrequestdelegate/authenticationsessionrequest(_:didcancelwitherror:))

##### Deprecated symbols

- [var callbackURLScheme: String?](/documentation/authenticationservices/aswebauthenticationsessionrequest/callbackurlscheme)

### Querying the Manager

- [var wasLaunchedByAuthenticationServices: Bool](/documentation/authenticationservices/aswebauthenticationsessionwebbrowsersessionmanager/waslaunchedbyauthenticationservices)
- [ASWebAuthenticationSessionWebBrowserSupportCapabilities](/documentation/bundleresources/information-property-list/aswebauthenticationsessionwebbrowsersupportcapabilities)

## AutoFill credentials

- [Providing one-time passcodes to AutoFill](/documentation/authenticationservices/providing-one-time-passcodes-to-autofill)
- [AutoFill Credential Provider Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.authentication-services.autofill-credential-provider)
- [ASCredentialProviderViewController](/documentation/authenticationservices/ascredentialproviderviewcontroller)

### Getting the extension context

- [var extensionContext: ASCredentialProviderExtensionContext](/documentation/authenticationservices/ascredentialproviderviewcontroller/extensioncontext)
- [ASCredentialProviderExtensionContext](/documentation/authenticationservices/ascredentialproviderextensioncontext)

#### Configuring the extension

- [func completeExtensionConfigurationRequest()](/documentation/authenticationservices/ascredentialproviderextensioncontext/completeextensionconfigurationrequest())

#### Providing credentials

- [func completeRequest(withSelectedCredential: ASPasswordCredential, completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completerequest(withselectedcredential:completionhandler:))
- [func completeAssertionRequest(using: ASPasskeyAssertionCredential, completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completeassertionrequest(using:completionhandler:))
- [func completeRegistrationRequest(using: ASPasskeyRegistrationCredential, completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completeregistrationrequest(using:completionhandler:))
- [func completeOneTimeCodeRequest(using: ASOneTimeCodeCredential, completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completeonetimecoderequest(using:completionhandler:))
- [ASPasswordCredential](/documentation/authenticationservices/aspasswordcredential)

##### Creating a credential

- [init(user: String, password: String)](/documentation/authenticationservices/aspasswordcredential/init(user:password:))

##### Accessing the username and password

- [var user: String](/documentation/authenticationservices/aspasswordcredential/user)
- [var password: String](/documentation/authenticationservices/aspasswordcredential/password)
- [ASPasskeyAssertionCredential](/documentation/authenticationservices/aspasskeyassertioncredential)

##### Creating a passkey assertion credential

- [init(userHandle: Data, relyingParty: String, signature: Data, clientDataHash: Data, authenticatorData: Data, credentialID: Data)](/documentation/authenticationservices/aspasskeyassertioncredential/init(userhandle:relyingparty:signature:clientdatahash:authenticatordata:credentialid:))
- [convenience init(userHandle: Data, relyingParty: String, signature: Data, clientDataHash: Data, authenticatorData: Data, credentialID: Data, extensionOutput: ASPasskeyAssertionCredentialExtensionOutput?)](/documentation/authenticationservices/aspasskeyassertioncredential/init(userhandle:relyingparty:signature:clientdatahash:authenticatordata:credentialid:extensionoutput:))

##### Accessing credential information

- [var authenticatorData: Data](/documentation/authenticationservices/aspasskeyassertioncredential/authenticatordata)
- [var clientDataHash: Data](/documentation/authenticationservices/aspasskeyassertioncredential/clientdatahash)
- [var credentialID: Data](/documentation/authenticationservices/aspasskeyassertioncredential/credentialid)
- [var relyingParty: String](/documentation/authenticationservices/aspasskeyassertioncredential/relyingparty)
- [var signature: Data](/documentation/authenticationservices/aspasskeyassertioncredential/signature)
- [var userHandle: Data](/documentation/authenticationservices/aspasskeyassertioncredential/userhandle)

##### Accessing extension output

- [var extensionOutput: ASPasskeyAssertionCredentialExtensionOutput?](/documentation/authenticationservices/aspasskeyassertioncredential/extensionoutput-7t6rn)
- [ASPasskeyAssertionCredentialExtensionOutput](/documentation/authenticationservices/aspasskeyassertioncredentialextensionoutput-swift.struct)

###### Creating an extension output instance

- [init(largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput?, prf: ASAuthorizationPublicKeyCredentialPRFAssertionOutput?)](/documentation/authenticationservices/aspasskeyassertioncredentialextensionoutput-swift.struct/init(largeblob:prf:))

###### Inspecting properties

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensionoutput-swift.struct/largeblob)
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct)

###### Inspecting the result

- [var result: ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput.OperationResult](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/result)
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput.OperationResult](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/operationresult)

###### Results

- [case read(data: Data?)](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/operationresult/read(data:))
- [case write(success: Bool)](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/operationresult/write(success:))

###### Type Methods

- [static func read(data: Data?) -> ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/read(data:))
- [static func write(success: Bool) -> ASAuthorizationPublicKeyCredentialLargeBlobAssertionOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertionoutput-swift.struct/write(success:))
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionOutput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensionoutput-swift.struct/prf)
- [ASAuthorizationPublicKeyCredentialPRFAssertionOutput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertionoutput-swift.struct)

###### Creating a PRF assertion output

- [init(first: SymmetricKey, second: SymmetricKey?)](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertionoutput-swift.struct/init(first:second:))

###### Accessing symmetric keys

- [let first: SymmetricKey](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertionoutput-swift.struct/first)
- [let second: SymmetricKey?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertionoutput-swift.struct/second)
- [ASPasskeyRegistrationCredential](/documentation/authenticationservices/aspasskeyregistrationcredential)

##### Creating a passkey registration credential

- [init(relyingParty: String, clientDataHash: Data, credentialID: Data, attestationObject: Data)](/documentation/authenticationservices/aspasskeyregistrationcredential/init(relyingparty:clientdatahash:credentialid:attestationobject:))
- [convenience init(relyingParty: String, clientDataHash: Data, credentialID: Data, attestationObject: Data, extensionOutput: ASPasskeyRegistrationCredentialExtensionOutput?)](/documentation/authenticationservices/aspasskeyregistrationcredential/init(relyingparty:clientdatahash:credentialid:attestationobject:extensionoutput:))

##### Accessing credential information

- [var attestationObject: Data](/documentation/authenticationservices/aspasskeyregistrationcredential/attestationobject)
- [var clientDataHash: Data](/documentation/authenticationservices/aspasskeyregistrationcredential/clientdatahash)
- [var credentialID: Data](/documentation/authenticationservices/aspasskeyregistrationcredential/credentialid)
- [var relyingParty: String](/documentation/authenticationservices/aspasskeyregistrationcredential/relyingparty)

##### Accessing extension output

- [var extensionOutput: ASPasskeyRegistrationCredentialExtensionOutput?](/documentation/authenticationservices/aspasskeyregistrationcredential/extensionoutput-2lf9m)
- [ASPasskeyRegistrationCredentialExtensionOutput](/documentation/authenticationservices/aspasskeyregistrationcredentialextensionoutput-swift.struct)

###### Creating an extension output instance

- [init(largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput?, prf: ASAuthorizationPublicKeyCredentialPRFRegistrationOutput?)](/documentation/authenticationservices/aspasskeyregistrationcredentialextensionoutput-swift.struct/init(largeblob:prf:))

###### Inspecting properties

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput?](/documentation/authenticationservices/aspasskeyregistrationcredentialextensionoutput-swift.struct/largeblob)
- [ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationoutput-swift.struct)

###### Accessing output properties

- [var isSupported: Bool](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationoutput-swift.struct/issupported)

###### Using defined support values

- [static var supported: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationoutput-swift.struct/supported)
- [static var unsupported: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationoutput-swift.struct/unsupported)
- [var prf: ASAuthorizationPublicKeyCredentialPRFRegistrationOutput?](/documentation/authenticationservices/aspasskeyregistrationcredentialextensionoutput-swift.struct/prf)
- [ASAuthorizationPublicKeyCredentialPRFRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct)

###### Creating an outputs instance

- [init(first: SymmetricKey, second: SymmetricKey?)](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/init(first:second:))

###### Determining PRF support

- [let isSupported: Bool](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/issupported)

###### Using defined support values

- [static var supported: ASAuthorizationPublicKeyCredentialPRFRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/supported)
- [static var unsupported: ASAuthorizationPublicKeyCredentialPRFRegistrationOutput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/unsupported)

###### Accessing symmetric keys

- [let first: SymmetricKey?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/first)
- [let second: SymmetricKey?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationoutput-swift.struct/second)
- [ASOneTimeCodeCredential](/documentation/authenticationservices/asonetimecodecredential)

##### Creating an OTP credential

- [init(code: String)](/documentation/authenticationservices/asonetimecodecredential/init(code:))

##### Accessing the OTP

- [var code: String](/documentation/authenticationservices/asonetimecodecredential/code)

#### Providing text to AutoFill

- [func completeRequest(withTextToInsert: String, completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completerequest(withtexttoinsert:completionhandler:))

#### Canceling

- [func cancelRequest(withError: any Error)](/documentation/authenticationservices/ascredentialproviderextensioncontext/cancelrequest(witherror:))

#### Instance Methods

- [func completeGeneratePasswordRequest(results: [ASGeneratedPassword], completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completegeneratepasswordrequest(results:completionhandler:))
- [func completeSavePasswordRequest(completionHandler: ((Bool) -> Void)?)](/documentation/authenticationservices/ascredentialproviderextensioncontext/completesavepasswordrequest(completionhandler:))

### Configuring the credential provider extension

- [func prepareInterfaceForExtensionConfiguration()](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterfaceforextensionconfiguration())
- [ASCredentialIdentityStore](/documentation/authenticationservices/ascredentialidentitystore)

#### Getting the shared store

- [class var shared: ASCredentialIdentityStore](/documentation/authenticationservices/ascredentialidentitystore/shared)

#### Checking the state of the store

- [func getState((ASCredentialIdentityStoreState) -> Void)](/documentation/authenticationservices/ascredentialidentitystore/getstate(_:))
- [ASCredentialIdentityStoreState](/documentation/authenticationservices/ascredentialidentitystorestate)

##### Checking the state

- [var isEnabled: Bool](/documentation/authenticationservices/ascredentialidentitystorestate/isenabled)
- [var supportsIncrementalUpdates: Bool](/documentation/authenticationservices/ascredentialidentitystorestate/supportsincrementalupdates)

#### Adding and removing credential identities

- [func saveCredentialIdentities([any ASCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/savecredentialidentities(_:completion:)-1bbx6)
- [func replaceCredentialIdentities([any ASCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/replacecredentialidentities(_:completion:))
- [func removeAllCredentialIdentities(((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/removeallcredentialidentities(_:))
- [func removeCredentialIdentities([any ASCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/removecredentialidentities(_:completion:)-67lcw)
- [ASCredentialIdentity](/documentation/authenticationservices/ascredentialidentity)

##### Ordering credential identities

- [var rank: Int](/documentation/authenticationservices/ascredentialidentity/rank)

##### Associating a user

- [var user: String](/documentation/authenticationservices/ascredentialidentity/user)

##### Distinguishing identities

- [var recordIdentifier: String?](/documentation/authenticationservices/ascredentialidentity/recordidentifier)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/ascredentialidentity/serviceidentifier)
- [ASPasskeyCredentialIdentity](/documentation/authenticationservices/aspasskeycredentialidentity)

##### Creating a credential identity

- [convenience init(relyingPartyIdentifier: String, userName: String, credentialID: Data, userHandle: Data, recordIdentifier: String?)](/documentation/authenticationservices/aspasskeycredentialidentity/init(relyingpartyidentifier:username:credentialid:userhandle:recordidentifier:)-7u7p1)
- [convenience init(relyingPartyIdentifier: String, userName: String, credentialID: Data, userHandle: Data, recordIdentifier: String?)](/documentation/authenticationservices/aspasskeycredentialidentity/init(relyingpartyidentifier:username:credentialid:userhandle:recordidentifier:)-9iuhb)

##### Ordering credential identities

- [var rank: Int](/documentation/authenticationservices/aspasskeycredentialidentity/rank)

##### Associating a user

- [var userName: String](/documentation/authenticationservices/aspasskeycredentialidentity/username)
- [var userHandle: Data](/documentation/authenticationservices/aspasskeycredentialidentity/userhandle)

##### Associating a relying party

- [var relyingPartyIdentifier: String](/documentation/authenticationservices/aspasskeycredentialidentity/relyingpartyidentifier)

##### Distinguishing identities

- [var credentialID: Data](/documentation/authenticationservices/aspasskeycredentialidentity/credentialid)
- [var recordIdentifier: String?](/documentation/authenticationservices/aspasskeycredentialidentity/recordidentifier)
- [ASPasswordCredentialIdentity](/documentation/authenticationservices/aspasswordcredentialidentity)

##### Creating a credential identity

- [init(serviceIdentifier: ASCredentialServiceIdentifier, user: String, recordIdentifier: String?)](/documentation/authenticationservices/aspasswordcredentialidentity/init(serviceidentifier:user:recordidentifier:))
- [ASCredentialServiceIdentifier](/documentation/authenticationservices/ascredentialserviceidentifier)

###### Creating a credential service identifier

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:))

###### Identifying the credential service

- [var identifier: String](/documentation/authenticationservices/ascredentialserviceidentifier/identifier)
- [var type: ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/type)
- [ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype)

###### Identifier types

- [case URL](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/url)
- [case domain](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/domain)

###### Enumeration Cases

- [case app](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/app)

###### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/init(rawvalue:))

###### Initializers

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType, displayName: String)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:displayname:))

###### Instance Properties

- [var displayName: String?](/documentation/authenticationservices/ascredentialserviceidentifier/displayname)

##### Ordering credential identities

- [var rank: Int](/documentation/authenticationservices/aspasswordcredentialidentity/rank)

##### Associating a user

- [var user: String](/documentation/authenticationservices/aspasswordcredentialidentity/user)

##### Distinguishing identities

- [var recordIdentifier: String?](/documentation/authenticationservices/aspasswordcredentialidentity/recordidentifier)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/aspasswordcredentialidentity/serviceidentifier)

#### Fetching saved credential identities

- [func credentialIdentities(forService: ASCredentialServiceIdentifier?, credentialIdentityTypes: ASCredentialIdentityStore.IdentityTypes) async -> [any ASCredentialIdentity]](/documentation/authenticationservices/ascredentialidentitystore/credentialidentities(forservice:credentialidentitytypes:))
- [ASCredentialServiceIdentifier](/documentation/authenticationservices/ascredentialserviceidentifier)

##### Creating a credential service identifier

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:))

##### Identifying the credential service

- [var identifier: String](/documentation/authenticationservices/ascredentialserviceidentifier/identifier)
- [var type: ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/type)
- [ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype)

###### Identifier types

- [case URL](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/url)
- [case domain](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/domain)

###### Enumeration Cases

- [case app](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/app)

###### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/init(rawvalue:))

##### Initializers

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType, displayName: String)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:displayname:))

##### Instance Properties

- [var displayName: String?](/documentation/authenticationservices/ascredentialserviceidentifier/displayname)
- [ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes)

##### Working with identity types

- [static var passkey: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/passkey)
- [static var password: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/password)
- [static var oneTimeCode: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/onetimecode)

##### Working with raw values

- [init(rawValue: UInt)](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/init(rawvalue:))

#### Recognizing errors

- [ASCredentialIdentityStoreError](/documentation/authenticationservices/ascredentialidentitystoreerror)

##### Error domain

- [let ASCredentialIdentityStoreErrorDomain: String](/documentation/authenticationservices/ascredentialidentitystoreerrordomain)
- [static var internalError: ASCredentialIdentityStoreError.Code](/documentation/authenticationservices/ascredentialidentitystoreerror/internalerror)
- [static var storeBusy: ASCredentialIdentityStoreError.Code](/documentation/authenticationservices/ascredentialidentitystoreerror/storebusy)
- [static var storeDisabled: ASCredentialIdentityStoreError.Code](/documentation/authenticationservices/ascredentialidentitystoreerror/storedisabled)
- [ASCredentialIdentityStoreError.Code](/documentation/authenticationservices/ascredentialidentitystoreerror/code)

###### Codes

- [case internalError](/documentation/authenticationservices/ascredentialidentitystoreerror/code/internalerror)
- [case storeBusy](/documentation/authenticationservices/ascredentialidentitystoreerror/code/storebusy)
- [case storeDisabled](/documentation/authenticationservices/ascredentialidentitystoreerror/code/storedisabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialidentitystoreerror/code/init(rawvalue:))

##### Type Properties

- [static var errorDomain: String](/documentation/authenticationservices/ascredentialidentitystoreerror/errordomain)
- [let ASCredentialIdentityStoreErrorDomain: String](/documentation/authenticationservices/ascredentialidentitystoreerrordomain)
- [ASCredentialIdentityStoreError.Code](/documentation/authenticationservices/ascredentialidentitystoreerror/code)

##### Codes

- [case internalError](/documentation/authenticationservices/ascredentialidentitystoreerror/code/internalerror)
- [case storeBusy](/documentation/authenticationservices/ascredentialidentitystoreerror/code/storebusy)
- [case storeDisabled](/documentation/authenticationservices/ascredentialidentitystoreerror/code/storedisabled)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialidentitystoreerror/code/init(rawvalue:))

#### Deprecated methods

- [func saveCredentialIdentities([ASPasswordCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/savecredentialidentities(_:completion:)-5vs4m)
- [func replaceCredentialIdentities(with: [ASPasswordCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/replacecredentialidentities(with:completion:))
- [func removeCredentialIdentities([ASPasswordCredentialIdentity], completion: ((Bool, (any Error)?) -> Void)?)](/documentation/authenticationservices/ascredentialidentitystore/removecredentialidentities(_:completion:)-2ygnf)

### Selecting a credential

- [func prepareCredentialList(for: [ASCredentialServiceIdentifier])](/documentation/authenticationservices/ascredentialproviderviewcontroller/preparecredentiallist(for:))
- [func prepareCredentialList(for: [ASCredentialServiceIdentifier], requestParameters: ASPasskeyCredentialRequestParameters)](/documentation/authenticationservices/ascredentialproviderviewcontroller/preparecredentiallist(for:requestparameters:))
- [func prepareOneTimeCodeCredentialList(for: [ASCredentialServiceIdentifier])](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareonetimecodecredentiallist(for:))
- [func prepareInterface(forPasskeyRegistration: any ASCredentialRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterface(forpasskeyregistration:))
- [func prepareInterfaceToProvideCredential(for: any ASCredentialRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterfacetoprovidecredential(for:)-68qpo)
- [func provideCredentialWithoutUserInteraction(for: any ASCredentialRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/providecredentialwithoutuserinteraction(for:)-3mo23)
- [func performWithoutUserInteractionIfPossible(passkeyRegistration: ASPasskeyCredentialRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/performwithoutuserinteractionifpossible(passkeyregistration:))
- [ASCredentialServiceIdentifier](/documentation/authenticationservices/ascredentialserviceidentifier)

#### Creating a credential service identifier

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:))

#### Identifying the credential service

- [var identifier: String](/documentation/authenticationservices/ascredentialserviceidentifier/identifier)
- [var type: ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/type)
- [ASCredentialServiceIdentifier.IdentifierType](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype)

##### Identifier types

- [case URL](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/url)
- [case domain](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/domain)

##### Enumeration Cases

- [case app](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/app)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialserviceidentifier/identifiertype/init(rawvalue:))

#### Initializers

- [init(identifier: String, type: ASCredentialServiceIdentifier.IdentifierType, displayName: String)](/documentation/authenticationservices/ascredentialserviceidentifier/init(identifier:type:displayname:))

#### Instance Properties

- [var displayName: String?](/documentation/authenticationservices/ascredentialserviceidentifier/displayname)
- [ASCredentialRequest](/documentation/authenticationservices/ascredentialrequest)

#### Identifying the requested credential type

- [var type: ASCredentialRequestType](/documentation/authenticationservices/ascredentialrequest/type)
- [ASCredentialRequestType](/documentation/authenticationservices/ascredentialrequesttype)

##### Credential types

- [case passkeyAssertion](/documentation/authenticationservices/ascredentialrequesttype/passkeyassertion)
- [case passkeyRegistration](/documentation/authenticationservices/ascredentialrequesttype/passkeyregistration)
- [case password](/documentation/authenticationservices/ascredentialrequesttype/password)
- [case oneTimeCode](/documentation/authenticationservices/ascredentialrequesttype/onetimecode)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/ascredentialrequesttype/init(rawvalue:))

#### Identifying credentials

- [var credentialIdentity: any ASCredentialIdentity](/documentation/authenticationservices/ascredentialrequest/credentialidentity)
- [ASPasswordCredentialRequest](/documentation/authenticationservices/aspasswordcredentialrequest)

#### Creating password credential requests

- [init(credentialIdentity: ASPasswordCredentialIdentity)](/documentation/authenticationservices/aspasswordcredentialrequest/init(credentialidentity:))
- [ASOneTimeCodeCredentialRequest](/documentation/authenticationservices/asonetimecodecredentialrequest)

#### Initializers

- [init(credentialIdentity: ASOneTimeCodeCredentialIdentity)](/documentation/authenticationservices/asonetimecodecredentialrequest/init(credentialidentity:))
- [ASAuthorizationPublicKeyCredentialRegistrationRequest](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest)

#### Getting the properties

- [var attestationPreference: ASAuthorizationPublicKeyCredentialAttestationKind](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/attestationpreference)
- [var challenge: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/challenge)
- [var displayName: String?](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/displayname)
- [var name: String](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/name)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/relyingpartyidentifier)
- [var userID: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/userid)
- [var userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/asauthorizationpublickeycredentialregistrationrequest/userverificationpreference)
- [ASPasskeyCredentialRequest](/documentation/authenticationservices/aspasskeycredentialrequest)

#### Creating passkey credential requests

- [convenience init(credentialIdentity: ASPasskeyCredentialIdentity, clientDataHash: Data, userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference, supportedAlgorithms: [NSNumber])](/documentation/authenticationservices/aspasskeycredentialrequest/init(credentialidentity:clientdatahash:userverificationpreference:supportedalgorithms:)-1jihy)
- [convenience init(credentialIdentity: ASPasskeyCredentialIdentity, clientDataHash: Data, userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference, supportedAlgorithms: [ASCOSEAlgorithmIdentifier])](/documentation/authenticationservices/aspasskeycredentialrequest/init(credentialidentity:clientdatahash:userverificationpreference:supportedalgorithms:)-52txr)
- [convenience init(credentialIdentity: ASPasskeyCredentialIdentity, clientDataHash: Data, userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference, supportedAlgorithms: [ASCOSEAlgorithmIdentifier], extensionInput: ASPasskeyAssertionCredentialExtensionInput?)](/documentation/authenticationservices/aspasskeycredentialrequest/init(credentialidentity:clientdatahash:userverificationpreference:supportedalgorithms:extensioninput:)-9hsyv)
- [convenience init(credentialIdentity: ASPasskeyCredentialIdentity, clientDataHash: Data, userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference, supportedAlgorithms: [ASCOSEAlgorithmIdentifier], extensionInput: ASPasskeyRegistrationCredentialExtensionInput?)](/documentation/authenticationservices/aspasskeycredentialrequest/init(credentialidentity:clientdatahash:userverificationpreference:supportedalgorithms:extensioninput:)-1258o)

#### Viewing passkey challenge information

- [var clientDataHash: Data](/documentation/authenticationservices/aspasskeycredentialrequest/clientdatahash)
- [var userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/aspasskeycredentialrequest/userverificationpreference)
- [var supportedAlgorithms: [ASCOSEAlgorithmIdentifier]](/documentation/authenticationservices/aspasskeycredentialrequest/supportedalgorithms-74mad)
- [var extensionInput: ASPasskeyCredentialExtensionInput](/documentation/authenticationservices/aspasskeycredentialrequest/extensioninput)
- [ASPasskeyCredentialExtensionInput](/documentation/authenticationservices/aspasskeycredentialextensioninput)

##### Extension input types

- [case none](/documentation/authenticationservices/aspasskeycredentialextensioninput/none)
- [case assertion(ASPasskeyAssertionCredentialExtensionInput)](/documentation/authenticationservices/aspasskeycredentialextensioninput/assertion(_:))
- [ASPasskeyAssertionCredentialExtensionInput](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct)

###### Creating an assertion input

- [init(largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?, prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?)](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/init(largeblob:prf:))
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct)

###### Using assertion inputs

- [static var read: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/read)
- [static func write(Data) -> ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/write(_:))

###### Inspecting the operation

- [var operation: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput.Operation](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.property)
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput.Operation](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum)

###### Input operations

- [case read](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum/read)
- [case write(Data)](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum/write(_:))
- [ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct)

###### Accessing input values

- [let inputValues: ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.property)
- [static func inputValues(ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues, perCredentialInputValues: [Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]?) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues(_:percredentialinputvalues:))

###### Accessing per-credential input values

- [let perCredentialInputValues: [Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/percredentialinputvalues)
- [static func perCredentialInputValues([Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/percredentialinputvalues(_:))

###### Supporting types

- [ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct)

###### Initializers

- [init(saltInput1: Data, saltInput2: Data?)](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/init(saltinput1:saltinput2:))

###### Instance Properties

- [var saltInput1: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput1)
- [var saltInput2: Data?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput2)

###### Type Methods

- [static func saltInput1(Data, saltInput2: Data?) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput1(_:saltinput2:))

###### Using inputs

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/largeblob)
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/prf)
- [case registration(ASPasskeyRegistrationCredentialExtensionInput)](/documentation/authenticationservices/aspasskeycredentialextensioninput/registration(_:))
- [ASPasskeyRegistrationCredentialExtensionInput](/documentation/authenticationservices/aspasskeyregistrationcredentialextensioninput-swift.struct)

###### Inputs

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput?](/documentation/authenticationservices/aspasskeyregistrationcredentialextensioninput-swift.struct/largeblob)
- [ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct)

###### Determining binary large object support

- [var supportRequirement: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput.SupportRequirement](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportrequirement-swift.property)
- [ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput.SupportRequirement](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportrequirement-swift.enum)

###### Supporting requirement values

- [case preferred](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportrequirement-swift.enum/preferred)
- [case required](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportrequirement-swift.enum/required)

###### Using defined support values

- [static var supportPreferred: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportpreferred)
- [static var supportRequired: ASAuthorizationPublicKeyCredentialLargeBlobRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobregistrationinput-swift.struct/supportrequired)
- [var prf: ASAuthorizationPublicKeyCredentialPRFRegistrationInput?](/documentation/authenticationservices/aspasskeyregistrationcredentialextensioninput-swift.struct/prf)
- [ASAuthorizationPublicKeyCredentialPRFRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct)

###### Working with PRF inputs

- [let inputValues: ASAuthorizationPublicKeyCredentialPRFRegistrationInput.InputValues?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct/inputvalues-swift.property)
- [ASAuthorizationPublicKeyCredentialPRFRegistrationInput.InputValues](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct/inputvalues-swift.typealias)
- [static func inputValues(ASAuthorizationPublicKeyCredentialPRFRegistrationInput.InputValues) -> ASAuthorizationPublicKeyCredentialPRFRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct/inputvalues(_:))

###### Checking for support

- [let shouldCheckForSupport: Bool](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct/shouldcheckforsupport)
- [static var checkForSupport: ASAuthorizationPublicKeyCredentialPRFRegistrationInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfregistrationinput-swift.struct/checkforsupport)

#### Instance Properties

- [var excludedCredentials: [ASAuthorizationPlatformPublicKeyCredentialDescriptor]?](/documentation/authenticationservices/aspasskeycredentialrequest/excludedcredentials)
- [ASPasskeyCredentialRequestParameters](/documentation/authenticationservices/aspasskeycredentialrequestparameters)

#### Viewing credential request parameters

- [var allowedCredentials: [Data]](/documentation/authenticationservices/aspasskeycredentialrequestparameters/allowedcredentials)
- [var clientDataHash: Data](/documentation/authenticationservices/aspasskeycredentialrequestparameters/clientdatahash)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/aspasskeycredentialrequestparameters/relyingpartyidentifier)
- [var userVerificationPreference: ASAuthorizationPublicKeyCredentialUserVerificationPreference](/documentation/authenticationservices/aspasskeycredentialrequestparameters/userverificationpreference)

#### Working with WebAuthn extensions

- [var extensionInput: ASPasskeyAssertionCredentialExtensionInput?](/documentation/authenticationservices/aspasskeycredentialrequestparameters/extensioninput-2edlv)
- [ASPasskeyAssertionCredentialExtensionInput](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct)

##### Creating an assertion input

- [init(largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?, prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?)](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/init(largeblob:prf:))
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct)

###### Using assertion inputs

- [static var read: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/read)
- [static func write(Data) -> ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/write(_:))

###### Inspecting the operation

- [var operation: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput.Operation](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.property)
- [ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput.Operation](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum)

###### Input operations

- [case read](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum/read)
- [case write(Data)](/documentation/authenticationservices/asauthorizationpublickeycredentiallargeblobassertioninput-swift.struct/operation-swift.enum/write(_:))
- [ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct)

###### Accessing input values

- [let inputValues: ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.property)
- [static func inputValues(ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues, perCredentialInputValues: [Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]?) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues(_:percredentialinputvalues:))

###### Accessing per-credential input values

- [let perCredentialInputValues: [Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/percredentialinputvalues)
- [static func perCredentialInputValues([Data : ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues]) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/percredentialinputvalues(_:))

###### Supporting types

- [ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct)

###### Initializers

- [init(saltInput1: Data, saltInput2: Data?)](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/init(saltinput1:saltinput2:))

###### Instance Properties

- [var saltInput1: Data](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput1)
- [var saltInput2: Data?](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput2)

###### Type Methods

- [static func saltInput1(Data, saltInput2: Data?) -> ASAuthorizationPublicKeyCredentialPRFAssertionInput.InputValues](/documentation/authenticationservices/asauthorizationpublickeycredentialprfassertioninput-swift.struct/inputvalues-swift.struct/saltinput1(_:saltinput2:))

##### Using inputs

- [var largeBlob: ASAuthorizationPublicKeyCredentialLargeBlobAssertionInput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/largeblob)
- [var prf: ASAuthorizationPublicKeyCredentialPRFAssertionInput?](/documentation/authenticationservices/aspasskeyassertioncredentialextensioninput-swift.struct/prf)

### Providing text to AutoFill

- [func prepareInterfaceForUserChoosingTextToInsert()](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterfaceforuserchoosingtexttoinsert())

### Recognizing errors

- [ASExtensionError](/documentation/authenticationservices/asextensionerror)

#### Identifying the error domain

- [let ASExtensionErrorDomain: String](/documentation/authenticationservices/asextensionerrordomain)

#### Error codes

- [static var credentialIdentityNotFound: ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/credentialidentitynotfound)
- [static var failed: ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/failed)
- [static var userCanceled: ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/usercanceled)
- [static var userInteractionRequired: ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/userinteractionrequired)
- [ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/code)

##### Codes

- [case credentialIdentityNotFound](/documentation/authenticationservices/asextensionerror/code/credentialidentitynotfound)
- [case failed](/documentation/authenticationservices/asextensionerror/code/failed)
- [case userCanceled](/documentation/authenticationservices/asextensionerror/code/usercanceled)
- [case userInteractionRequired](/documentation/authenticationservices/asextensionerror/code/userinteractionrequired)

##### Enumeration Cases

- [case matchedExcludedCredential](/documentation/authenticationservices/asextensionerror/code/matchedexcludedcredential)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asextensionerror/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/authenticationservices/asextensionerror/errordomain)
- [static var matchedExcludedCredential: ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/matchedexcludedcredential)
- [let ASExtensionErrorDomain: String](/documentation/authenticationservices/asextensionerrordomain)
- [ASExtensionError.Code](/documentation/authenticationservices/asextensionerror/code)

#### Codes

- [case credentialIdentityNotFound](/documentation/authenticationservices/asextensionerror/code/credentialidentitynotfound)
- [case failed](/documentation/authenticationservices/asextensionerror/code/failed)
- [case userCanceled](/documentation/authenticationservices/asextensionerror/code/usercanceled)
- [case userInteractionRequired](/documentation/authenticationservices/asextensionerror/code/userinteractionrequired)

#### Enumeration Cases

- [case matchedExcludedCredential](/documentation/authenticationservices/asextensionerror/code/matchedexcludedcredential)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asextensionerror/code/init(rawvalue:))

### Accessing settings

- [ASSettingsHelper](/documentation/authenticationservices/assettingshelper)

#### Opening the Settings app

- [class func openCredentialProviderAppSettings(completionHandler: (((any Error)?) -> Void)?)](/documentation/authenticationservices/assettingshelper/opencredentialproviderappsettings(completionhandler:))
- [class func openVerificationCodeAppSettings(completionHandler: (((any Error)?) -> Void)?)](/documentation/authenticationservices/assettingshelper/openverificationcodeappsettings(completionhandler:))

#### Type Methods

- [class func requestToTurnOnCredentialProviderExtension(completionHandler: (Bool) -> Void)](/documentation/authenticationservices/assettingshelper/requesttoturnoncredentialproviderextension(completionhandler:))

### Receiving credential updates

- [func reportAllAcceptedPublicKeyCredentials(forRelyingParty: String, userHandle: Data, acceptedCredentialIDs: [Data])](/documentation/authenticationservices/ascredentialproviderviewcontroller/reportallacceptedpublickeycredentials(forrelyingparty:userhandle:acceptedcredentialids:))
- [func reportPublicKeyCredentialUpdate(forRelyingParty: String, userHandle: Data, newName: String)](/documentation/authenticationservices/ascredentialproviderviewcontroller/reportpublickeycredentialupdate(forrelyingparty:userhandle:newname:))
- [func reportUnknownPublicKeyCredential(forRelyingParty: String, credentialID: Data)](/documentation/authenticationservices/ascredentialproviderviewcontroller/reportunknownpublickeycredential(forrelyingparty:credentialid:))
- [func reportUnusedPasswordCredential(forDomain: String, userName: String)](/documentation/authenticationservices/ascredentialproviderviewcontroller/reportunusedpasswordcredential(fordomain:username:))

### Deprecated methods

- [func provideCredentialWithoutUserInteraction(for: ASPasswordCredentialIdentity)](/documentation/authenticationservices/ascredentialproviderviewcontroller/providecredentialwithoutuserinteraction(for:)-7jlg0)
- [func prepareInterfaceToProvideCredential(for: ASPasswordCredentialIdentity)](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterfacetoprovidecredential(for:)-18ukb)

### Instance Methods

- [func performWithoutUserInteraction(generatePasswordsRequest: ASGeneratePasswordsRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/performwithoutuserinteraction(generatepasswordsrequest:))
- [func performWithoutUserInteractionIfPossible(savePasswordRequest: ASSavePasswordRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/performwithoutuserinteractionifpossible(savepasswordrequest:))
- [func prepareInterface(for: ASSavePasswordRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterface(for:)-69elg)
- [func prepareInterface(for: ASGeneratePasswordsRequest)](/documentation/authenticationservices/ascredentialproviderviewcontroller/prepareinterface(for:)-7ideq)

## Credential migration

- [ASCredentialExportManager](/documentation/authenticationservices/ascredentialexportmanager)

### Creating an export manager

- [convenience init(presentationAnchor: ASPresentationAnchor)](/documentation/authenticationservices/ascredentialexportmanager/init(presentationanchor:)-56ki6)
- [convenience init(presentationAnchor: ASPresentationAnchor)](/documentation/authenticationservices/ascredentialexportmanager/init(presentationanchor:)-904gt)
- [ASPresentationAnchor](/documentation/authenticationservices/aspresentationanchor)

### Exporting credentials

- [func requestExport(for: String?) async throws -> ASCredentialExportManager.ExportOptions](/documentation/authenticationservices/ascredentialexportmanager/requestexport(for:))
- [ASCredentialExportManager.ExportOptions](/documentation/authenticationservices/ascredentialexportmanager/exportoptions)

#### Working with export options

- [let formatVersion: ASExportedCredentialData.FormatVersion](/documentation/authenticationservices/ascredentialexportmanager/exportoptions/formatversion)
- [func exportCredentials(ASExportedCredentialData) async throws](/documentation/authenticationservices/ascredentialexportmanager/exportcredentials(_:))
- [ASExportedCredentialData](/documentation/authenticationservices/asexportedcredentialdata)

#### Accessing accounts

- [var accounts: [ASImportableAccount]](/documentation/authenticationservices/asexportedcredentialdata/accounts)
- [ASImportableAccount](/documentation/authenticationservices/asimportableaccount)

##### Creating an account

- [init(id: Data, userName: String, email: String, fullName: String?, collections: [ASImportableCollection], items: [ASImportableItem])](/documentation/authenticationservices/asimportableaccount/init(id:username:email:fullname:collections:items:))

##### Accessing account properties

- [var id: Data](/documentation/authenticationservices/asimportableaccount/id)
- [var userName: String](/documentation/authenticationservices/asimportableaccount/username)
- [var email: String](/documentation/authenticationservices/asimportableaccount/email)
- [var fullName: String?](/documentation/authenticationservices/asimportableaccount/fullname)
- [var collections: [ASImportableCollection]](/documentation/authenticationservices/asimportableaccount/collections)
- [ASImportableCollection](/documentation/authenticationservices/asimportablecollection)

###### Accessing collection properties

- [var id: Data](/documentation/authenticationservices/asimportablecollection/id)
- [var title: String](/documentation/authenticationservices/asimportablecollection/title)
- [var subtitle: String?](/documentation/authenticationservices/asimportablecollection/subtitle)
- [var items: [ASImportableLinkedItem]](/documentation/authenticationservices/asimportablecollection/items)
- [ASImportableLinkedItem](/documentation/authenticationservices/asimportablelinkeditem)

###### Creating a linked item

- [init(item: Data, account: Data?)](/documentation/authenticationservices/asimportablelinkeditem/init(item:account:))

###### Accessing linked item properties

- [var item: Data](/documentation/authenticationservices/asimportablelinkeditem/item)
- [var account: Data?](/documentation/authenticationservices/asimportablelinkeditem/account)
- [var subcollections: [ASImportableCollection]](/documentation/authenticationservices/asimportablecollection/subcollections)

###### Initializers

- [init(id: Data, created: Date?, lastModified: Date?, title: String, subtitle: String?, items: [ASImportableLinkedItem], subcollections: [ASImportableCollection])](/documentation/authenticationservices/asimportablecollection/init(id:created:lastmodified:title:subtitle:items:subcollections:))

###### Instance Properties

- [var created: Date?](/documentation/authenticationservices/asimportablecollection/created)
- [var lastModified: Date?](/documentation/authenticationservices/asimportablecollection/lastmodified)
- [var items: [ASImportableItem]](/documentation/authenticationservices/asimportableaccount/items)
- [ASImportableItem](/documentation/authenticationservices/asimportableitem)

###### Accessing item properties

- [var id: Data](/documentation/authenticationservices/asimportableitem/id)
- [var created: Date?](/documentation/authenticationservices/asimportableitem/created)
- [var lastModified: Date?](/documentation/authenticationservices/asimportableitem/lastmodified)
- [var subtitle: String?](/documentation/authenticationservices/asimportableitem/subtitle)
- [var credentials: [ASImportableCredential]](/documentation/authenticationservices/asimportableitem/credentials)
- [ASImportableCredential](/documentation/authenticationservices/asimportablecredential)

###### Login credential types

- [case basicAuthentication(ASImportableCredential.BasicAuthentication)](/documentation/authenticationservices/asimportablecredential/basicauthentication(_:))
- [ASImportableCredential.BasicAuthentication](/documentation/authenticationservices/asimportablecredential/basicauthentication)

###### Accessing authentication properties

- [var password: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/basicauthentication/password)
- [ASImportableEditableField](/documentation/authenticationservices/asimportableeditablefield)

###### Creating an editable field

- [init(id: Data?, fieldType: ASImportableEditableField.FieldType, value: String, label: String?)](/documentation/authenticationservices/asimportableeditablefield/init(id:fieldtype:value:label:))

###### Accessing field properties

- [var id: Data?](/documentation/authenticationservices/asimportableeditablefield/id)
- [var fieldType: ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.property)
- [ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum)

###### Determining field type

- [case boolean](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/boolean)
- [case concealedString](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/concealedstring)
- [case date](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/date)
- [case email](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/email)
- [case number](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/number)
- [case string](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/string)

###### Enumeration Cases

- [case countryCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/countrycode)
- [case subdivisionCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/subdivisioncode)
- [case wifiNetworkSecurityType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/wifinetworksecuritytype)
- [case yearMonth](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/yearmonth)
- [var value: String](/documentation/authenticationservices/asimportableeditablefield/value)
- [var label: String?](/documentation/authenticationservices/asimportableeditablefield/label)

###### Initializers

- [init(userName: ASImportableEditableField?, password: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/basicauthentication/init(username:password:))

###### Instance Properties

- [var userName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/basicauthentication/username)
- [case passkey(ASImportableCredential.Passkey)](/documentation/authenticationservices/asimportablecredential/passkey(_:))
- [ASImportableCredential.Passkey](/documentation/authenticationservices/asimportablecredential/passkey)

###### Creating a passkey instance

- [init(credentialID: Data, relyingPartyIdentifier: String, userName: String, userDisplayName: String, userHandle: Data, key: Data)](/documentation/authenticationservices/asimportablecredential/passkey/init(credentialid:relyingpartyidentifier:username:userdisplayname:userhandle:key:))

###### Accessing passkey properties

- [var credentialID: Data](/documentation/authenticationservices/asimportablecredential/passkey/credentialid)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asimportablecredential/passkey/relyingpartyidentifier)
- [var userName: String](/documentation/authenticationservices/asimportablecredential/passkey/username)
- [var userDisplayName: String](/documentation/authenticationservices/asimportablecredential/passkey/userdisplayname)
- [var userHandle: Data](/documentation/authenticationservices/asimportablecredential/passkey/userhandle)
- [var key: Data](/documentation/authenticationservices/asimportablecredential/passkey/key)
- [case totp(ASImportableCredential.TOTP)](/documentation/authenticationservices/asimportablecredential/totp(_:))
- [ASImportableCredential.TOTP](/documentation/authenticationservices/asimportablecredential/totp)

###### Accessing TOTP properties

- [var secret: Data](/documentation/authenticationservices/asimportablecredential/totp/secret)
- [var period: UInt16](/documentation/authenticationservices/asimportablecredential/totp/period)
- [var digits: UInt16](/documentation/authenticationservices/asimportablecredential/totp/digits)
- [var algorithm: ASImportableCredential.TOTP.Algorithm](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.property)
- [ASImportableCredential.TOTP.Algorithm](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum)

###### Algorithms

- [case sha1](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha1)
- [case sha256](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha256)
- [case sha512](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha512)
- [var issuer: String?](/documentation/authenticationservices/asimportablecredential/totp/issuer)

###### Initializers

- [init(secret: Data, period: UInt16, digits: UInt16, userName: String?, algorithm: ASImportableCredential.TOTP.Algorithm, issuer: String?)](/documentation/authenticationservices/asimportablecredential/totp/init(secret:period:digits:username:algorithm:issuer:))

###### Instance Properties

- [var userName: String?](/documentation/authenticationservices/asimportablecredential/totp/username)

###### Document credential types

- [case note(ASImportableCredential.Note)](/documentation/authenticationservices/asimportablecredential/note(_:))
- [ASImportableCredential.Note](/documentation/authenticationservices/asimportablecredential/note)

###### Creating a note

- [init(content: ASImportableEditableField)](/documentation/authenticationservices/asimportablecredential/note/init(content:))

###### Accessing note properties

- [var content: ASImportableEditableField](/documentation/authenticationservices/asimportablecredential/note/content)

###### Identity credential types

- [case creditCard(ASImportableCredential.CreditCard)](/documentation/authenticationservices/asimportablecredential/creditcard(_:))
- [ASImportableCredential.CreditCard](/documentation/authenticationservices/asimportablecredential/creditcard)

###### Accessing credit card properties

- [var number: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/number)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/fullname)
- [var cardType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/cardtype)
- [var verificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/verificationnumber)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/expirydate)
- [var validFrom: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/validfrom)

###### Initializers

- [init(number: ASImportableEditableField?, fullName: ASImportableEditableField?, cardType: ASImportableEditableField?, verificationNumber: ASImportableEditableField?, pin: ASImportableEditableField?, expiryDate: ASImportableEditableField?, validFrom: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/creditcard/init(number:fullname:cardtype:verificationnumber:pin:expirydate:validfrom:))

###### Instance Properties

- [var pin: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/pin)

###### Structures

- [ASImportableCredential.APIKey](/documentation/authenticationservices/asimportablecredential/apikey)

###### Initializers

- [init(key: ASImportableEditableField?, userName: ASImportableEditableField?, keyType: ASImportableEditableField?, url: ASImportableEditableField?, validFrom: ASImportableEditableField?, expiryDate: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/apikey/init(key:username:keytype:url:validfrom:expirydate:))

###### Instance Properties

- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/expirydate)
- [var key: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/key)
- [var keyType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/keytype)
- [var url: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/url)
- [var userName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/username)
- [var validFrom: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/validfrom)
- [ASImportableCredential.Address](/documentation/authenticationservices/asimportablecredential/address)

###### Initializers

- [init(streetAddress: ASImportableEditableField?, postalCode: ASImportableEditableField?, city: ASImportableEditableField?, territory: ASImportableEditableField?, country: ASImportableEditableField?, telephone: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/address/init(streetaddress:postalcode:city:territory:country:telephone:))

###### Instance Properties

- [var city: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/city)
- [var country: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/country)
- [var postalCode: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/postalcode)
- [var streetAddress: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/streetaddress)
- [var telephone: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/telephone)
- [var territory: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/territory)
- [ASImportableCredential.CustomFields](/documentation/authenticationservices/asimportablecredential/customfields)

###### Initializers

- [init(id: Data?, label: String?, fields: [ASImportableEditableField])](/documentation/authenticationservices/asimportablecredential/customfields/init(id:label:fields:))

###### Instance Properties

- [var fields: [ASImportableEditableField]](/documentation/authenticationservices/asimportablecredential/customfields/fields)
- [var id: Data?](/documentation/authenticationservices/asimportablecredential/customfields/id)
- [var label: String?](/documentation/authenticationservices/asimportablecredential/customfields/label)
- [ASImportableCredential.DriversLicense](/documentation/authenticationservices/asimportablecredential/driverslicense)

###### Initializers

- [init(fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?, territory: ASImportableEditableField?, country: ASImportableEditableField?, licenseNumber: ASImportableEditableField?, licenseClass: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/driverslicense/init(fullname:birthdate:issuedate:expirydate:issuingauthority:territory:country:licensenumber:licenseclass:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/birthdate)
- [var country: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/country)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/fullname)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/issuingauthority)
- [var licenseClass: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/licenseclass)
- [var licenseNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/licensenumber)
- [var territory: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/territory)
- [ASImportableCredential.GeneratedPassword](/documentation/authenticationservices/asimportablecredential/generatedpassword)

###### Initializers

- [init(password: String)](/documentation/authenticationservices/asimportablecredential/generatedpassword/init(password:))

###### Instance Properties

- [var password: String](/documentation/authenticationservices/asimportablecredential/generatedpassword/password)
- [ASImportableCredential.IdentityDocument](/documentation/authenticationservices/asimportablecredential/identitydocument)

###### Initializers

- [init(issuingCountry: ASImportableEditableField?, documentNumber: ASImportableEditableField?, identificationNumber: ASImportableEditableField?, nationality: ASImportableEditableField?, fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, birthPlace: ASImportableEditableField?, sex: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/identitydocument/init(issuingcountry:documentnumber:identificationnumber:nationality:fullname:birthdate:birthplace:sex:issuedate:expirydate:issuingauthority:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/birthdate)
- [var birthPlace: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/birthplace)
- [var documentNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/documentnumber)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/fullname)
- [var identificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/identificationnumber)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuingauthority)
- [var issuingCountry: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuingcountry)
- [var nationality: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/nationality)
- [var sex: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/sex)
- [ASImportableCredential.ItemReference](/documentation/authenticationservices/asimportablecredential/itemreference)

###### Initializers

- [init(reference: ASImportableLinkedItem)](/documentation/authenticationservices/asimportablecredential/itemreference/init(reference:))

###### Instance Properties

- [var reference: ASImportableLinkedItem](/documentation/authenticationservices/asimportablecredential/itemreference/reference)
- [ASImportableCredential.Passport](/documentation/authenticationservices/asimportablecredential/passport)

###### Initializers

- [init(issuingCountry: ASImportableEditableField?, passportType: ASImportableEditableField?, passportNumber: ASImportableEditableField?, nationalIdentificationNumber: ASImportableEditableField?, nationality: ASImportableEditableField?, fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, birthPlace: ASImportableEditableField?, sex: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/passport/init(issuingcountry:passporttype:passportnumber:nationalidentificationnumber:nationality:fullname:birthdate:birthplace:sex:issuedate:expirydate:issuingauthority:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/birthdate)
- [var birthPlace: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/birthplace)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/fullname)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuingauthority)
- [var issuingCountry: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuingcountry)
- [var nationalIdentificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/nationalidentificationnumber)
- [var nationality: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/nationality)
- [var passportNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/passportnumber)
- [var passportType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/passporttype)
- [var sex: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/sex)
- [ASImportableCredential.PersonName](/documentation/authenticationservices/asimportablecredential/personname)

###### Initializers

- [init(title: ASImportableEditableField?, given: ASImportableEditableField?, givenInformal: ASImportableEditableField?, given2: ASImportableEditableField?, surnamePrefix: ASImportableEditableField?, surname: ASImportableEditableField?, surname2: ASImportableEditableField?, credentials: ASImportableEditableField?, generation: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/personname/init(title:given:giveninformal:given2:surnameprefix:surname:surname2:credentials:generation:))

###### Instance Properties

- [var credentials: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/credentials)
- [var generation: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/generation)
- [var given: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/given)
- [var given2: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/given2)
- [var givenInformal: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/giveninformal)
- [var surname: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surname)
- [var surname2: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surname2)
- [var surnamePrefix: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surnameprefix)
- [var title: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/title)
- [ASImportableCredential.SSHKey](/documentation/authenticationservices/asimportablecredential/sshkey)

###### Initializers

- [init(keyType: String, privateKey: Data, keyComment: String?, creationDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, keyGenerationSource: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/sshkey/init(keytype:privatekey:keycomment:creationdate:expirydate:keygenerationsource:))

###### Instance Properties

- [var creationDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/creationdate)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/expirydate)
- [var keyComment: String?](/documentation/authenticationservices/asimportablecredential/sshkey/keycomment)
- [var keyGenerationSource: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/keygenerationsource)
- [var keyType: String](/documentation/authenticationservices/asimportablecredential/sshkey/keytype)
- [var privateKey: Data](/documentation/authenticationservices/asimportablecredential/sshkey/privatekey)
- [ASImportableCredential.WiFi](/documentation/authenticationservices/asimportablecredential/wifi)

###### Initializers

- [init(ssid: ASImportableEditableField?, networkSecurityType: ASImportableEditableField?, passphrase: ASImportableEditableField?, hidden: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/wifi/init(ssid:networksecuritytype:passphrase:hidden:))

###### Instance Properties

- [var hidden: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/hidden)
- [var networkSecurityType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/networksecuritytype)
- [var passphrase: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/passphrase)
- [var ssid: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/ssid)

###### Enumeration Cases

- [case address(ASImportableCredential.Address)](/documentation/authenticationservices/asimportablecredential/address(_:))
- [case apiKey(ASImportableCredential.APIKey)](/documentation/authenticationservices/asimportablecredential/apikey(_:))
- [case customFields(ASImportableCredential.CustomFields)](/documentation/authenticationservices/asimportablecredential/customfields(_:))
- [case driversLicense(ASImportableCredential.DriversLicense)](/documentation/authenticationservices/asimportablecredential/driverslicense(_:))
- [case generatedPassword(ASImportableCredential.GeneratedPassword)](/documentation/authenticationservices/asimportablecredential/generatedpassword(_:))
- [case identityDocument(ASImportableCredential.IdentityDocument)](/documentation/authenticationservices/asimportablecredential/identitydocument(_:))
- [case itemReference(ASImportableCredential.ItemReference)](/documentation/authenticationservices/asimportablecredential/itemreference(_:))
- [case passport(ASImportableCredential.Passport)](/documentation/authenticationservices/asimportablecredential/passport(_:))
- [case personName(ASImportableCredential.PersonName)](/documentation/authenticationservices/asimportablecredential/personname(_:))
- [case sshKey(ASImportableCredential.SSHKey)](/documentation/authenticationservices/asimportablecredential/sshkey(_:))
- [case wifi(ASImportableCredential.WiFi)](/documentation/authenticationservices/asimportablecredential/wifi(_:))
- [var tags: [String]](/documentation/authenticationservices/asimportableitem/tags)

###### Initializers

- [init(id: Data, created: Date, lastModified: Date, title: String, subtitle: String?, favorite: Bool, scope: ASImportableCredentialScope?, credentials: [ASImportableCredential], tags: [String])](/documentation/authenticationservices/asimportableitem/init(id:created:lastmodified:title:subtitle:favorite:scope:credentials:tags:))
- [init(id: Data, title: String, subtitle: String?, favorite: Bool, scope: ASImportableCredentialScope?, credentials: [ASImportableCredential], tags: [String])](/documentation/authenticationservices/asimportableitem/init(id:title:subtitle:favorite:scope:credentials:tags:))

###### Instance Properties

- [var favorite: Bool](/documentation/authenticationservices/asimportableitem/favorite)
- [var scope: ASImportableCredentialScope?](/documentation/authenticationservices/asimportableitem/scope)
- [var title: String](/documentation/authenticationservices/asimportableitem/title)

#### Initializers

- [init(accounts: [ASImportableAccount], formatVersion: ASExportedCredentialData.FormatVersion, exporterRelyingPartyIdentifier: String, exporterDisplayName: String, timestamp: Date)](/documentation/authenticationservices/asexportedcredentialdata/init(accounts:formatversion:exporterrelyingpartyidentifier:exporterdisplayname:timestamp:))

#### Instance Properties

- [let exporterDisplayName: String](/documentation/authenticationservices/asexportedcredentialdata/exporterdisplayname)
- [let exporterRelyingPartyIdentifier: String](/documentation/authenticationservices/asexportedcredentialdata/exporterrelyingpartyidentifier)
- [let formatVersion: ASExportedCredentialData.FormatVersion](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.property)
- [let timestamp: Date](/documentation/authenticationservices/asexportedcredentialdata/timestamp)

#### Enumerations

- [ASExportedCredentialData.FormatVersion](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.enum)

##### Enumeration Cases

- [case v1](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.enum/v1)
- [ASCredentialImportManager](/documentation/authenticationservices/ascredentialimportmanager)

### Creating an import manager

- [init()](/documentation/authenticationservices/ascredentialimportmanager/init())

### Importing credentials

- [func importCredentials(token: UUID) async throws -> ASExportedCredentialData](/documentation/authenticationservices/ascredentialimportmanager/importcredentials(token:))
- [ASExportedCredentialData](/documentation/authenticationservices/asexportedcredentialdata)

#### Accessing accounts

- [var accounts: [ASImportableAccount]](/documentation/authenticationservices/asexportedcredentialdata/accounts)
- [ASImportableAccount](/documentation/authenticationservices/asimportableaccount)

##### Creating an account

- [init(id: Data, userName: String, email: String, fullName: String?, collections: [ASImportableCollection], items: [ASImportableItem])](/documentation/authenticationservices/asimportableaccount/init(id:username:email:fullname:collections:items:))

##### Accessing account properties

- [var id: Data](/documentation/authenticationservices/asimportableaccount/id)
- [var userName: String](/documentation/authenticationservices/asimportableaccount/username)
- [var email: String](/documentation/authenticationservices/asimportableaccount/email)
- [var fullName: String?](/documentation/authenticationservices/asimportableaccount/fullname)
- [var collections: [ASImportableCollection]](/documentation/authenticationservices/asimportableaccount/collections)
- [ASImportableCollection](/documentation/authenticationservices/asimportablecollection)

###### Accessing collection properties

- [var id: Data](/documentation/authenticationservices/asimportablecollection/id)
- [var title: String](/documentation/authenticationservices/asimportablecollection/title)
- [var subtitle: String?](/documentation/authenticationservices/asimportablecollection/subtitle)
- [var items: [ASImportableLinkedItem]](/documentation/authenticationservices/asimportablecollection/items)
- [ASImportableLinkedItem](/documentation/authenticationservices/asimportablelinkeditem)

###### Creating a linked item

- [init(item: Data, account: Data?)](/documentation/authenticationservices/asimportablelinkeditem/init(item:account:))

###### Accessing linked item properties

- [var item: Data](/documentation/authenticationservices/asimportablelinkeditem/item)
- [var account: Data?](/documentation/authenticationservices/asimportablelinkeditem/account)
- [var subcollections: [ASImportableCollection]](/documentation/authenticationservices/asimportablecollection/subcollections)

###### Initializers

- [init(id: Data, created: Date?, lastModified: Date?, title: String, subtitle: String?, items: [ASImportableLinkedItem], subcollections: [ASImportableCollection])](/documentation/authenticationservices/asimportablecollection/init(id:created:lastmodified:title:subtitle:items:subcollections:))

###### Instance Properties

- [var created: Date?](/documentation/authenticationservices/asimportablecollection/created)
- [var lastModified: Date?](/documentation/authenticationservices/asimportablecollection/lastmodified)
- [var items: [ASImportableItem]](/documentation/authenticationservices/asimportableaccount/items)
- [ASImportableItem](/documentation/authenticationservices/asimportableitem)

###### Accessing item properties

- [var id: Data](/documentation/authenticationservices/asimportableitem/id)
- [var created: Date?](/documentation/authenticationservices/asimportableitem/created)
- [var lastModified: Date?](/documentation/authenticationservices/asimportableitem/lastmodified)
- [var subtitle: String?](/documentation/authenticationservices/asimportableitem/subtitle)
- [var credentials: [ASImportableCredential]](/documentation/authenticationservices/asimportableitem/credentials)
- [ASImportableCredential](/documentation/authenticationservices/asimportablecredential)

###### Login credential types

- [case basicAuthentication(ASImportableCredential.BasicAuthentication)](/documentation/authenticationservices/asimportablecredential/basicauthentication(_:))
- [ASImportableCredential.BasicAuthentication](/documentation/authenticationservices/asimportablecredential/basicauthentication)

###### Accessing authentication properties

- [var password: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/basicauthentication/password)
- [ASImportableEditableField](/documentation/authenticationservices/asimportableeditablefield)

###### Creating an editable field

- [init(id: Data?, fieldType: ASImportableEditableField.FieldType, value: String, label: String?)](/documentation/authenticationservices/asimportableeditablefield/init(id:fieldtype:value:label:))

###### Accessing field properties

- [var id: Data?](/documentation/authenticationservices/asimportableeditablefield/id)
- [var fieldType: ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.property)
- [ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum)

###### Determining field type

- [case boolean](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/boolean)
- [case concealedString](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/concealedstring)
- [case date](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/date)
- [case email](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/email)
- [case number](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/number)
- [case string](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/string)

###### Enumeration Cases

- [case countryCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/countrycode)
- [case subdivisionCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/subdivisioncode)
- [case wifiNetworkSecurityType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/wifinetworksecuritytype)
- [case yearMonth](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/yearmonth)
- [var value: String](/documentation/authenticationservices/asimportableeditablefield/value)
- [var label: String?](/documentation/authenticationservices/asimportableeditablefield/label)

###### Initializers

- [init(userName: ASImportableEditableField?, password: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/basicauthentication/init(username:password:))

###### Instance Properties

- [var userName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/basicauthentication/username)
- [case passkey(ASImportableCredential.Passkey)](/documentation/authenticationservices/asimportablecredential/passkey(_:))
- [ASImportableCredential.Passkey](/documentation/authenticationservices/asimportablecredential/passkey)

###### Creating a passkey instance

- [init(credentialID: Data, relyingPartyIdentifier: String, userName: String, userDisplayName: String, userHandle: Data, key: Data)](/documentation/authenticationservices/asimportablecredential/passkey/init(credentialid:relyingpartyidentifier:username:userdisplayname:userhandle:key:))

###### Accessing passkey properties

- [var credentialID: Data](/documentation/authenticationservices/asimportablecredential/passkey/credentialid)
- [var relyingPartyIdentifier: String](/documentation/authenticationservices/asimportablecredential/passkey/relyingpartyidentifier)
- [var userName: String](/documentation/authenticationservices/asimportablecredential/passkey/username)
- [var userDisplayName: String](/documentation/authenticationservices/asimportablecredential/passkey/userdisplayname)
- [var userHandle: Data](/documentation/authenticationservices/asimportablecredential/passkey/userhandle)
- [var key: Data](/documentation/authenticationservices/asimportablecredential/passkey/key)
- [case totp(ASImportableCredential.TOTP)](/documentation/authenticationservices/asimportablecredential/totp(_:))
- [ASImportableCredential.TOTP](/documentation/authenticationservices/asimportablecredential/totp)

###### Accessing TOTP properties

- [var secret: Data](/documentation/authenticationservices/asimportablecredential/totp/secret)
- [var period: UInt16](/documentation/authenticationservices/asimportablecredential/totp/period)
- [var digits: UInt16](/documentation/authenticationservices/asimportablecredential/totp/digits)
- [var algorithm: ASImportableCredential.TOTP.Algorithm](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.property)
- [ASImportableCredential.TOTP.Algorithm](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum)

###### Algorithms

- [case sha1](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha1)
- [case sha256](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha256)
- [case sha512](/documentation/authenticationservices/asimportablecredential/totp/algorithm-swift.enum/sha512)
- [var issuer: String?](/documentation/authenticationservices/asimportablecredential/totp/issuer)

###### Initializers

- [init(secret: Data, period: UInt16, digits: UInt16, userName: String?, algorithm: ASImportableCredential.TOTP.Algorithm, issuer: String?)](/documentation/authenticationservices/asimportablecredential/totp/init(secret:period:digits:username:algorithm:issuer:))

###### Instance Properties

- [var userName: String?](/documentation/authenticationservices/asimportablecredential/totp/username)

###### Document credential types

- [case note(ASImportableCredential.Note)](/documentation/authenticationservices/asimportablecredential/note(_:))
- [ASImportableCredential.Note](/documentation/authenticationservices/asimportablecredential/note)

###### Creating a note

- [init(content: ASImportableEditableField)](/documentation/authenticationservices/asimportablecredential/note/init(content:))

###### Accessing note properties

- [var content: ASImportableEditableField](/documentation/authenticationservices/asimportablecredential/note/content)

###### Identity credential types

- [case creditCard(ASImportableCredential.CreditCard)](/documentation/authenticationservices/asimportablecredential/creditcard(_:))
- [ASImportableCredential.CreditCard](/documentation/authenticationservices/asimportablecredential/creditcard)

###### Accessing credit card properties

- [var number: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/number)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/fullname)
- [var cardType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/cardtype)
- [var verificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/verificationnumber)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/expirydate)
- [var validFrom: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/validfrom)

###### Initializers

- [init(number: ASImportableEditableField?, fullName: ASImportableEditableField?, cardType: ASImportableEditableField?, verificationNumber: ASImportableEditableField?, pin: ASImportableEditableField?, expiryDate: ASImportableEditableField?, validFrom: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/creditcard/init(number:fullname:cardtype:verificationnumber:pin:expirydate:validfrom:))

###### Instance Properties

- [var pin: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/creditcard/pin)

###### Structures

- [ASImportableCredential.APIKey](/documentation/authenticationservices/asimportablecredential/apikey)

###### Initializers

- [init(key: ASImportableEditableField?, userName: ASImportableEditableField?, keyType: ASImportableEditableField?, url: ASImportableEditableField?, validFrom: ASImportableEditableField?, expiryDate: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/apikey/init(key:username:keytype:url:validfrom:expirydate:))

###### Instance Properties

- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/expirydate)
- [var key: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/key)
- [var keyType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/keytype)
- [var url: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/url)
- [var userName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/username)
- [var validFrom: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/apikey/validfrom)
- [ASImportableCredential.Address](/documentation/authenticationservices/asimportablecredential/address)

###### Initializers

- [init(streetAddress: ASImportableEditableField?, postalCode: ASImportableEditableField?, city: ASImportableEditableField?, territory: ASImportableEditableField?, country: ASImportableEditableField?, telephone: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/address/init(streetaddress:postalcode:city:territory:country:telephone:))

###### Instance Properties

- [var city: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/city)
- [var country: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/country)
- [var postalCode: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/postalcode)
- [var streetAddress: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/streetaddress)
- [var telephone: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/telephone)
- [var territory: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/address/territory)
- [ASImportableCredential.CustomFields](/documentation/authenticationservices/asimportablecredential/customfields)

###### Initializers

- [init(id: Data?, label: String?, fields: [ASImportableEditableField])](/documentation/authenticationservices/asimportablecredential/customfields/init(id:label:fields:))

###### Instance Properties

- [var fields: [ASImportableEditableField]](/documentation/authenticationservices/asimportablecredential/customfields/fields)
- [var id: Data?](/documentation/authenticationservices/asimportablecredential/customfields/id)
- [var label: String?](/documentation/authenticationservices/asimportablecredential/customfields/label)
- [ASImportableCredential.DriversLicense](/documentation/authenticationservices/asimportablecredential/driverslicense)

###### Initializers

- [init(fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?, territory: ASImportableEditableField?, country: ASImportableEditableField?, licenseNumber: ASImportableEditableField?, licenseClass: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/driverslicense/init(fullname:birthdate:issuedate:expirydate:issuingauthority:territory:country:licensenumber:licenseclass:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/birthdate)
- [var country: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/country)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/fullname)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/issuingauthority)
- [var licenseClass: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/licenseclass)
- [var licenseNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/licensenumber)
- [var territory: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/driverslicense/territory)
- [ASImportableCredential.GeneratedPassword](/documentation/authenticationservices/asimportablecredential/generatedpassword)

###### Initializers

- [init(password: String)](/documentation/authenticationservices/asimportablecredential/generatedpassword/init(password:))

###### Instance Properties

- [var password: String](/documentation/authenticationservices/asimportablecredential/generatedpassword/password)
- [ASImportableCredential.IdentityDocument](/documentation/authenticationservices/asimportablecredential/identitydocument)

###### Initializers

- [init(issuingCountry: ASImportableEditableField?, documentNumber: ASImportableEditableField?, identificationNumber: ASImportableEditableField?, nationality: ASImportableEditableField?, fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, birthPlace: ASImportableEditableField?, sex: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/identitydocument/init(issuingcountry:documentnumber:identificationnumber:nationality:fullname:birthdate:birthplace:sex:issuedate:expirydate:issuingauthority:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/birthdate)
- [var birthPlace: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/birthplace)
- [var documentNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/documentnumber)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/fullname)
- [var identificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/identificationnumber)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuingauthority)
- [var issuingCountry: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/issuingcountry)
- [var nationality: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/nationality)
- [var sex: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/identitydocument/sex)
- [ASImportableCredential.ItemReference](/documentation/authenticationservices/asimportablecredential/itemreference)

###### Initializers

- [init(reference: ASImportableLinkedItem)](/documentation/authenticationservices/asimportablecredential/itemreference/init(reference:))

###### Instance Properties

- [var reference: ASImportableLinkedItem](/documentation/authenticationservices/asimportablecredential/itemreference/reference)
- [ASImportableCredential.Passport](/documentation/authenticationservices/asimportablecredential/passport)

###### Initializers

- [init(issuingCountry: ASImportableEditableField?, passportType: ASImportableEditableField?, passportNumber: ASImportableEditableField?, nationalIdentificationNumber: ASImportableEditableField?, nationality: ASImportableEditableField?, fullName: ASImportableEditableField?, birthDate: ASImportableEditableField?, birthPlace: ASImportableEditableField?, sex: ASImportableEditableField?, issueDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, issuingAuthority: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/passport/init(issuingcountry:passporttype:passportnumber:nationalidentificationnumber:nationality:fullname:birthdate:birthplace:sex:issuedate:expirydate:issuingauthority:))

###### Instance Properties

- [var birthDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/birthdate)
- [var birthPlace: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/birthplace)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/expirydate)
- [var fullName: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/fullname)
- [var issueDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuedate)
- [var issuingAuthority: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuingauthority)
- [var issuingCountry: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/issuingcountry)
- [var nationalIdentificationNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/nationalidentificationnumber)
- [var nationality: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/nationality)
- [var passportNumber: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/passportnumber)
- [var passportType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/passporttype)
- [var sex: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/passport/sex)
- [ASImportableCredential.PersonName](/documentation/authenticationservices/asimportablecredential/personname)

###### Initializers

- [init(title: ASImportableEditableField?, given: ASImportableEditableField?, givenInformal: ASImportableEditableField?, given2: ASImportableEditableField?, surnamePrefix: ASImportableEditableField?, surname: ASImportableEditableField?, surname2: ASImportableEditableField?, credentials: ASImportableEditableField?, generation: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/personname/init(title:given:giveninformal:given2:surnameprefix:surname:surname2:credentials:generation:))

###### Instance Properties

- [var credentials: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/credentials)
- [var generation: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/generation)
- [var given: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/given)
- [var given2: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/given2)
- [var givenInformal: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/giveninformal)
- [var surname: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surname)
- [var surname2: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surname2)
- [var surnamePrefix: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/surnameprefix)
- [var title: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/personname/title)
- [ASImportableCredential.SSHKey](/documentation/authenticationservices/asimportablecredential/sshkey)

###### Initializers

- [init(keyType: String, privateKey: Data, keyComment: String?, creationDate: ASImportableEditableField?, expiryDate: ASImportableEditableField?, keyGenerationSource: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/sshkey/init(keytype:privatekey:keycomment:creationdate:expirydate:keygenerationsource:))

###### Instance Properties

- [var creationDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/creationdate)
- [var expiryDate: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/expirydate)
- [var keyComment: String?](/documentation/authenticationservices/asimportablecredential/sshkey/keycomment)
- [var keyGenerationSource: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/sshkey/keygenerationsource)
- [var keyType: String](/documentation/authenticationservices/asimportablecredential/sshkey/keytype)
- [var privateKey: Data](/documentation/authenticationservices/asimportablecredential/sshkey/privatekey)
- [ASImportableCredential.WiFi](/documentation/authenticationservices/asimportablecredential/wifi)

###### Initializers

- [init(ssid: ASImportableEditableField?, networkSecurityType: ASImportableEditableField?, passphrase: ASImportableEditableField?, hidden: ASImportableEditableField?)](/documentation/authenticationservices/asimportablecredential/wifi/init(ssid:networksecuritytype:passphrase:hidden:))

###### Instance Properties

- [var hidden: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/hidden)
- [var networkSecurityType: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/networksecuritytype)
- [var passphrase: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/passphrase)
- [var ssid: ASImportableEditableField?](/documentation/authenticationservices/asimportablecredential/wifi/ssid)

###### Enumeration Cases

- [case address(ASImportableCredential.Address)](/documentation/authenticationservices/asimportablecredential/address(_:))
- [case apiKey(ASImportableCredential.APIKey)](/documentation/authenticationservices/asimportablecredential/apikey(_:))
- [case customFields(ASImportableCredential.CustomFields)](/documentation/authenticationservices/asimportablecredential/customfields(_:))
- [case driversLicense(ASImportableCredential.DriversLicense)](/documentation/authenticationservices/asimportablecredential/driverslicense(_:))
- [case generatedPassword(ASImportableCredential.GeneratedPassword)](/documentation/authenticationservices/asimportablecredential/generatedpassword(_:))
- [case identityDocument(ASImportableCredential.IdentityDocument)](/documentation/authenticationservices/asimportablecredential/identitydocument(_:))
- [case itemReference(ASImportableCredential.ItemReference)](/documentation/authenticationservices/asimportablecredential/itemreference(_:))
- [case passport(ASImportableCredential.Passport)](/documentation/authenticationservices/asimportablecredential/passport(_:))
- [case personName(ASImportableCredential.PersonName)](/documentation/authenticationservices/asimportablecredential/personname(_:))
- [case sshKey(ASImportableCredential.SSHKey)](/documentation/authenticationservices/asimportablecredential/sshkey(_:))
- [case wifi(ASImportableCredential.WiFi)](/documentation/authenticationservices/asimportablecredential/wifi(_:))
- [var tags: [String]](/documentation/authenticationservices/asimportableitem/tags)

###### Initializers

- [init(id: Data, created: Date, lastModified: Date, title: String, subtitle: String?, favorite: Bool, scope: ASImportableCredentialScope?, credentials: [ASImportableCredential], tags: [String])](/documentation/authenticationservices/asimportableitem/init(id:created:lastmodified:title:subtitle:favorite:scope:credentials:tags:))
- [init(id: Data, title: String, subtitle: String?, favorite: Bool, scope: ASImportableCredentialScope?, credentials: [ASImportableCredential], tags: [String])](/documentation/authenticationservices/asimportableitem/init(id:title:subtitle:favorite:scope:credentials:tags:))

###### Instance Properties

- [var favorite: Bool](/documentation/authenticationservices/asimportableitem/favorite)
- [var scope: ASImportableCredentialScope?](/documentation/authenticationservices/asimportableitem/scope)
- [var title: String](/documentation/authenticationservices/asimportableitem/title)

#### Initializers

- [init(accounts: [ASImportableAccount], formatVersion: ASExportedCredentialData.FormatVersion, exporterRelyingPartyIdentifier: String, exporterDisplayName: String, timestamp: Date)](/documentation/authenticationservices/asexportedcredentialdata/init(accounts:formatversion:exporterrelyingpartyidentifier:exporterdisplayname:timestamp:))

#### Instance Properties

- [let exporterDisplayName: String](/documentation/authenticationservices/asexportedcredentialdata/exporterdisplayname)
- [let exporterRelyingPartyIdentifier: String](/documentation/authenticationservices/asexportedcredentialdata/exporterrelyingpartyidentifier)
- [let formatVersion: ASExportedCredentialData.FormatVersion](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.property)
- [let timestamp: Date](/documentation/authenticationservices/asexportedcredentialdata/timestamp)

#### Enumerations

- [ASExportedCredentialData.FormatVersion](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.enum)

##### Enumeration Cases

- [case v1](/documentation/authenticationservices/asexportedcredentialdata/formatversion-swift.enum/v1)

## Single sign-on (SSO)

- [Enterprise single sign-on (SSO)](/documentation/authenticationservices/enterprise-single-sign-on-sso)

### Performing enterprise single sign-on

- [ASAuthorizationSingleSignOnProvider](/documentation/authenticationservices/asauthorizationsinglesignonprovider)

#### Creating an Authorization Provider

- [convenience init(identityProvider: URL)](/documentation/authenticationservices/asauthorizationsinglesignonprovider/init(identityprovider:))

#### Creating Authorization Requests

- [var canPerformAuthorization: Bool](/documentation/authenticationservices/asauthorizationsinglesignonprovider/canperformauthorization)
- [func createRequest() -> ASAuthorizationSingleSignOnRequest](/documentation/authenticationservices/asauthorizationsinglesignonprovider/createrequest())
- [ASAuthorizationSingleSignOnRequest](/documentation/authenticationservices/asauthorizationsinglesignonrequest)

##### Setting Options

- [var isUserInterfaceEnabled: Bool](/documentation/authenticationservices/asauthorizationsinglesignonrequest/isuserinterfaceenabled)
- [var authorizationOptions: [URLQueryItem]](/documentation/authenticationservices/asauthorizationsinglesignonrequest/authorizationoptions)
- [ASAuthorizationOpenIDRequest](/documentation/authenticationservices/asauthorizationopenidrequest)

##### Setting the Operation

- [var requestedOperation: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorizationopenidrequest/requestedoperation)
- [ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation)

###### Operation Types

- [static let operationLogin: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogin)
- [static let operationRefresh: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationrefresh)
- [static let operationLogout: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationlogout)
- [static let operationImplicit: ASAuthorization.OpenIDOperation](/documentation/authenticationservices/asauthorization/openidoperation/operationimplicit)

###### Creating an Operation

- [init(String)](/documentation/authenticationservices/asauthorization/openidoperation/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/openidoperation/init(rawvalue:))

##### Setting the Scope

- [var requestedScopes: [ASAuthorization.Scope]?](/documentation/authenticationservices/asauthorizationopenidrequest/requestedscopes)
- [ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope)

###### Scopes

- [static let email: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/email)
- [static let fullName: ASAuthorization.Scope](/documentation/authenticationservices/asauthorization/scope/fullname)

###### Creating a Scope

- [init(String)](/documentation/authenticationservices/asauthorization/scope/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorization/scope/init(rawvalue:))

##### Setting the State

- [var state: String?](/documentation/authenticationservices/asauthorizationopenidrequest/state)

##### Setting the Nonce

- [var nonce: String?](/documentation/authenticationservices/asauthorizationopenidrequest/nonce)

#### Identifying the Identity Provider

- [var url: URL](/documentation/authenticationservices/asauthorizationsinglesignonprovider/url)
- [ASAuthorizationSingleSignOnCredential](/documentation/authenticationservices/asauthorizationsinglesignoncredential)

#### Identifying a User

- [var identityToken: Data?](/documentation/authenticationservices/asauthorizationsinglesignoncredential/identitytoken)
- [var accessToken: Data?](/documentation/authenticationservices/asauthorizationsinglesignoncredential/accesstoken)
- [var state: String?](/documentation/authenticationservices/asauthorizationsinglesignoncredential/state)
- [var authorizedScopes: [ASAuthorization.Scope]](/documentation/authenticationservices/asauthorizationsinglesignoncredential/authorizedscopes)

#### Parsing the Response

- [var authenticatedResponse: HTTPURLResponse?](/documentation/authenticationservices/asauthorizationsinglesignoncredential/authenticatedresponse)
- [ASAuthorizationProviderExtensionAuthorizationRequestHandler](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequesthandler)

#### Starting or Canceling a Request

- [func beginAuthorization(with: ASAuthorizationProviderExtensionAuthorizationRequest)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequesthandler/beginauthorization(with:))
- [func cancelAuthorization(with: ASAuthorizationProviderExtensionAuthorizationRequest)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequesthandler/cancelauthorization(with:))
- [ASAuthorizationProviderExtensionAuthorizationRequest](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest)

##### Parsing the Request

- [var url: URL](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/url)
- [var httpHeaders: [String : String]](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/httpheaders)
- [var httpBody: Data](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/httpbody)
- [var realm: String](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/realm)
- [var requestedOperation: ASAuthorizationProviderAuthorizationOperation](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/requestedoperation)
- [ASAuthorizationProviderAuthorizationOperation](/documentation/authenticationservices/asauthorizationproviderauthorizationoperation)

###### Handling Configuration Removal

- [static let configurationRemoved: ASAuthorizationProviderAuthorizationOperation](/documentation/authenticationservices/asauthorizationproviderauthorizationoperation/configurationremoved)

###### Creating Operations

- [init(String)](/documentation/authenticationservices/asauthorizationproviderauthorizationoperation/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationproviderauthorizationoperation/init(rawvalue:))

###### Type Properties

- [static let directRequest: ASAuthorizationProviderAuthorizationOperation](/documentation/authenticationservices/asauthorizationproviderauthorizationoperation/directrequest)
- [var authorizationOptions: [AnyHashable : Any]](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/authorizationoptions)

##### Getting Context

- [var callerBundleIdentifier: String](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/callerbundleidentifier)
- [var callerTeamIdentifier: String](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/callerteamidentifier)
- [var localizedCallerDisplayName: String](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/localizedcallerdisplayname)
- [var isCallerManaged: Bool](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/iscallermanaged)
- [var extensionData: [AnyHashable : Any]](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/extensiondata)

##### Interacting with the User

- [func presentAuthorizationViewController(completion: (Bool, (any Error)?) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/presentauthorizationviewcontroller(completion:))
- [var isUserInterfaceEnabled: Bool](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/isuserinterfaceenabled)

##### Completing a Request

- [func complete(authorizationResult: ASAuthorizationProviderExtensionAuthorizationResult)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/complete(authorizationresult:))
- [func complete()](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/complete())
- [func complete(httpAuthorizationHeaders: [String : String])](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/complete(httpauthorizationheaders:))
- [func complete(httpResponse: HTTPURLResponse, httpBody: Data?)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/complete(httpresponse:httpbody:))
- [func complete(error: any Error)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/complete(error:))

##### Canceling a Request

- [func doNotHandle()](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/donothandle())
- [func cancel()](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/cancel())

##### Supporting Platform Single Sign-On

- [var loginManager: ASAuthorizationProviderExtensionLoginManager?](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/loginmanager)

##### Instance Properties

- [var callerAuditToken: Data](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationrequest/calleraudittoken)
- [ASAuthorizationProviderExtensionAuthorizationResult](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult)

#### Initializers

- [init(httpAuthorizationHeaders: [String : String])](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult/init(httpauthorizationheaders:))
- [init(httpResponse: HTTPURLResponse, httpBody: Data?)](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult/init(httpresponse:httpbody:))

#### Instance Properties

- [var httpAuthorizationHeaders: [String : String]?](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult/httpauthorizationheaders)
- [var httpResponse: HTTPURLResponse?](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult/httpresponse)
- [var httpBody: Data?](/documentation/authenticationservices/asauthorizationproviderextensionauthorizationresult/httpbody)
- [ASAuthorizationController.RequestOptions](/documentation/authenticationservices/asauthorizationcontroller/requestoptions)

#### Initializers

- [init(rawValue: UInt)](/documentation/authenticationservices/asauthorizationcontroller/requestoptions/init(rawvalue:))

#### Constants

- [static var preferImmediatelyAvailableCredentials: ASAuthorizationController.RequestOptions](/documentation/authenticationservices/asauthorizationcontroller/requestoptions/preferimmediatelyavailablecredentials)
- [Platform single sign-on (SSO)](/documentation/authenticationservices/platform-single-sign-on-sso)

### Essentials

- [Creating extensions that support Platform SSO](/documentation/authenticationservices/creating-extensions-that-support-platform-sso)
- [Registering devices and users](/documentation/authenticationservices/registering-devices-and-users)
- [ASAuthorizationProviderExtensionRegistrationHandler](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler)

#### Registering users and devices

- [func beginDeviceRegistration(loginManager: ASAuthorizationProviderExtensionLoginManager, options: ASAuthorizationProviderExtensionRequestOptions, completion: (ASAuthorizationProviderExtensionRegistrationResult) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/begindeviceregistration(loginmanager:options:completion:))
- [func beginUserRegistration(loginManager: ASAuthorizationProviderExtensionLoginManager, userName: String?, method: ASAuthorizationProviderExtensionAuthenticationMethod, options: ASAuthorizationProviderExtensionRequestOptions, completion: (ASAuthorizationProviderExtensionRegistrationResult) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/beginuserregistration(loginmanager:username:method:options:completion:))
- [func registrationDidComplete()](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/registrationdidcomplete())

#### Instance Methods

- [func protocolVersion() -> ASAuthorizationProviderExtensionPlatformSSOProtocolVersion](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/protocolversion())
- [func registrationDidCancel()](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/registrationdidcancel())
- [func supportedGrantTypes() -> ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/supportedgranttypes())
- [func displayNames(forGroups: [String], using: ASAuthorizationProviderExtensionLoginManager, completion: ([String : String]) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/displaynames(forgroups:using:completion:))
- [func keyWillRotate(for: ASAuthorizationProviderExtensionKeyType, newKey: SecKey, loginManager: ASAuthorizationProviderExtensionLoginManager, completion: (Bool) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/keywillrotate(for:newkey:loginmanager:completion:))
- [func profilePictureForUser(using: ASAuthorizationProviderExtensionLoginManager, completion: (Data) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/profilepictureforuser(using:completion:))

#### Instance Properties

- [var supportedDeviceEncryptionAlgorithms: [ASAuthorizationProviderExtensionEncryptionAlgorithm]](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/supporteddeviceencryptionalgorithms)
- [var supportedDeviceSigningAlgorithms: [ASAuthorizationProviderExtensionSigningAlgorithm]](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/supporteddevicesigningalgorithms)
- [var supportedUserSecureEnclaveKeySigningAlgorithms: [ASAuthorizationProviderExtensionSigningAlgorithm]](/documentation/authenticationservices/asauthorizationproviderextensionregistrationhandler/supportedusersecureenclavekeysigningalgorithms)
- [ASAuthorizationProviderExtensionAuthenticationMethod](/documentation/authenticationservices/asauthorizationproviderextensionauthenticationmethod)

#### Identifying the methods

- [case password](/documentation/authenticationservices/asauthorizationproviderextensionauthenticationmethod/password)
- [case userSecureEnclaveKey](/documentation/authenticationservices/asauthorizationproviderextensionauthenticationmethod/usersecureenclavekey)

#### Enumeration Cases

- [case smartCard](/documentation/authenticationservices/asauthorizationproviderextensionauthenticationmethod/smartcard)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionauthenticationmethod/init(rawvalue:))
- [ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions)

#### Creating the options

- [init(rawValue: UInt)](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/init(rawvalue:))

#### Identifying the options

- [static var registrationRepair: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/registrationrepair)
- [static var userInteractionEnabled: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/userinteractionenabled)

#### Type Properties

- [static var registrationDeviceKeyMigration: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/registrationdevicekeymigration)
- [static var registrationSharedDeviceKeys: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/registrationshareddevicekeys)
- [static var userKeyInvalid: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/userkeyinvalid)
- [static var setupAssistant: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/setupassistant)
- [static var strongerKeyAvailable: ASAuthorizationProviderExtensionRequestOptions](/documentation/authenticationservices/asauthorizationproviderextensionrequestoptions/strongerkeyavailable)
- [ASAuthorizationProviderExtensionRegistrationResult](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult)

#### Identifying the results

- [case failed](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult/failed)
- [case failedNoRetry](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult/failednoretry)
- [case success](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult/success)
- [case userInterfaceRequired](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult/userinterfacerequired)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionregistrationresult/init(rawvalue:))

### Configuration

- [Configuring Device Management](/documentation/authenticationservices/configuring-device-management)
- [Configuring authentication with the identity provider (IdP)](/documentation/authenticationservices/configuring-authentication-with-the-identity-provider-idp)
- [ASAuthorizationProviderExtensionLoginConfiguration](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration)

#### Creating the configuration

- [init(clientID: String, issuer: String, tokenEndpointURL: URL, jwksEndpointURL: URL, audience: String?)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/init(clientid:issuer:tokenendpointurl:jwksendpointurl:audience:))
- [class func configuration(openIDConfigurationURL: URL, clientID: String, issuer: String?, completion: (ASAuthorizationProviderExtensionLoginConfiguration?, (any Error)?) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/configuration(openidconfigurationurl:clientid:issuer:completion:))

#### Obtaining the required configuration

- [var audience: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/audience)
- [var clientID: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/clientid)
- [var jwksEndpointURL: URL](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/jwksendpointurl)
- [var tokenEndpointURL: URL](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/tokenendpointurl)
- [var issuer: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/issuer)

#### Obtaining the recommended configuration

- [var accountDisplayName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/accountdisplayname)
- [var invalidCredentialPredicate: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/invalidcredentialpredicate)

#### Configuring the server nonce

- [var customNonceRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customnoncerequestvalues)
- [var nonceEndpointURL: URL](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/nonceendpointurl)
- [var nonceResponseKeypath: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/nonceresponsekeypath)
- [var serverNonceClaimName: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/servernonceclaimname)

#### Configuring the previous refresh token

- [var includePreviousRefreshTokenInLoginRequest: Bool](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/includepreviousrefreshtokeninloginrequest)
- [var previousRefreshTokenClaimName: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/previousrefreshtokenclaimname)

#### Customizing the authentication request

- [func setCustomAssertionRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomassertionrequestbodyclaims(_:))
- [func setCustomAssertionRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomassertionrequestheaderclaims(_:))
- [func setCustomLoginRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomloginrequestbodyclaims(_:))
- [func setCustomLoginRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomloginrequestheaderclaims(_:))
- [var additionalScopes: String](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/additionalscopes)
- [var customLoginRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customloginrequestvalues)
- [var kerberosTicketMappings: [ASAuthorizationProviderExtensionKerberosMapping]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/kerberosticketmappings)

#### Instance Properties

- [var additionalAuthorizationScopes: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/additionalauthorizationscopes)
- [var customFederationUserPreauthenticationRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customfederationuserpreauthenticationrequestvalues)
- [var customKeyExchangeRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customkeyexchangerequestvalues)
- [var customKeyRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customkeyrequestvalues)
- [var customRefreshRequestValues: [URLQueryItem]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customrefreshrequestvalues)
- [var customRequestJWTParameterName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/customrequestjwtparametername)
- [var deviceContext: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/devicecontext)
- [var federationMEXURL: URL?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationmexurl)
- [var federationMEXURLKeypath: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationmexurlkeypath)
- [var federationPredicate: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationpredicate)
- [var federationRequestURN: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationrequesturn)
- [var federationType: ASAuthorizationProviderExtensionLoginConfiguration.FederationType](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.property)
- [var federationUserPreauthenticationURL: URL?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationuserpreauthenticationurl)
- [var groupRequestClaimName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/grouprequestclaimname)
- [var groupResponseClaimName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/groupresponseclaimname)
- [var jwksTrustedRootCertificates: [SecCertificate]](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/jwkstrustedrootcertificates-5y2pc)
- [var keyEndpointURL: URL?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/keyendpointurl)
- [var loginRequestEncryptionAPVPrefix: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/loginrequestencryptionapvprefix)
- [var loginRequestEncryptionPublicKey: SecKey?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/loginrequestencryptionpublickey)
- [var refreshEndpointURL: URL?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/refreshendpointurl)
- [var uniqueIdentifierClaimName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/uniqueidentifierclaimname)
- [var userSecureEnclaveKeyBiometricPolicy: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.property)
- [var hpkeAuthPublicKey: SecKey?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/hpkeauthpublickey)
- [var hpkePreSharedKey: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/hpkepresharedkey)
- [var hpkePreSharedKeyID: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/hpkepresharedkeyid)
- [var loginRequestEncryptionAlgorithm: ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/loginrequestencryptionalgorithm)
- [var loginRequestHPKEPreSharedKey: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/loginrequesthpkepresharedkey)
- [var loginRequestHPKEPreSharedKeyID: Data?](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/loginrequesthpkepresharedkeyid)

#### Instance Methods

- [func setCustomKeyExchangeRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomkeyexchangerequestbodyclaims(_:))
- [func setCustomKeyExchangeRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomkeyexchangerequestheaderclaims(_:))
- [func setCustomKeyRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomkeyrequestbodyclaims(_:))
- [func setCustomKeyRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomkeyrequestheaderclaims(_:))
- [func setCustomRefreshRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomrefreshrequestbodyclaims(_:))
- [func setCustomRefreshRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/setcustomrefreshrequestheaderclaims(_:))

#### Structures

- [ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct)

##### Initializers

- [init(rawValue: UInt)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/init(rawvalue:))

##### Type Properties

- [static var passwordFallback: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/passwordfallback)
- [static var reuseDuringUnlock: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/reuseduringunlock)
- [static var touchIDOrWatchAny: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/touchidorwatchany)
- [static var touchIDOrWatchCurrentSet: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/touchidorwatchcurrentset)

#### Enumerations

- [ASAuthorizationProviderExtensionLoginConfiguration.FederationType](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum)

##### Enumeration Cases

- [case dynamicWSTrust](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/dynamicwstrust)
- [case none](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/none)
- [case wsTrust](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/wstrust)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/init(rawvalue:))
- [ASAuthorizationProviderExtensionLoginManager](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager)

#### Performing registration

- [var loginUserName: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/loginusername)
- [var registrationToken: String?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/registrationtoken)
- [func presentRegistrationViewController(completion: ((any Error)?) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/presentregistrationviewcontroller(completion:))
- [func saveCertificate(SecCertificate, keyType: ASAuthorizationProviderExtensionKeyType)](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/savecertificate(_:keytype:))
- [func saveLoginConfiguration(ASAuthorizationProviderExtensionLoginConfiguration) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/saveloginconfiguration(_:))

#### Performing authentication

- [ASAuthorizationProviderExtensionKeyType](/documentation/authenticationservices/asauthorizationproviderextensionkeytype)

##### Identifying the key types

- [case userDeviceEncryption](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/userdeviceencryption)
- [case userDeviceSigning](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/userdevicesigning)
- [case userSecureEnclaveKey](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/usersecureenclavekey)

##### Enumeration Cases

- [case currentDeviceEncryption](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/currentdeviceencryption)
- [case currentDeviceSigning](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/currentdevicesigning)
- [case sharedDeviceEncryption](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/shareddeviceencryption)
- [case sharedDeviceSigning](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/shareddevicesigning)
- [case userSmartCard](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/usersmartcard)

##### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionkeytype/init(rawvalue:))
- [var isDeviceRegistered: Bool](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/isdeviceregistered)
- [var isUserRegistered: Bool](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/isuserregistered)
- [var loginConfiguration: ASAuthorizationProviderExtensionLoginConfiguration?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/loginconfiguration)
- [var ssoTokens: [AnyHashable : Any]?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/ssotokens)
- [func identity(for: ASAuthorizationProviderExtensionKeyType) -> SecIdentity?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/identity(for:))
- [func key(for: ASAuthorizationProviderExtensionKeyType) -> SecKey?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/key(for:))
- [func userNeedsReauthentication(completion: ((any Error)?) -> Void)](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/userneedsreauthentication(completion:))

#### Repairing registrations

- [func userRegistrationsNeedsRepair()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/userregistrationsneedsrepair())
- [func deviceRegistrationsNeedsRepair()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/deviceregistrationsneedsrepair())
- [func resetKeys()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/resetkeys())

#### Instance Properties

- [var extensionData: [AnyHashable : Any]](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/extensiondata)
- [var userLoginConfiguration: ASAuthorizationProviderExtensionUserLoginConfiguration?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/userloginconfiguration)
- [var authenticationMethod: ASAuthorizationProviderExtensionAuthenticationMethod](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/authenticationmethod)

#### Instance Methods

- [func decryptionKeysNeedRepair()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/decryptionkeysneedrepair())
- [func resetDeviceKeys()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/resetdevicekeys())
- [func resetUserSecureEnclaveKey()](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/resetusersecureenclavekey())
- [func saveUserLoginConfiguration(ASAuthorizationProviderExtensionUserLoginConfiguration) throws](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/saveuserloginconfiguration(_:))
- [func attestKey(ofType: ASAuthorizationProviderExtensionKeyType, clientDataHash: Data) async throws -> [SecCertificate]](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/attestkey(oftype:clientdatahash:))
- [func attestPendingKey(ofType: ASAuthorizationProviderExtensionKeyType, clientDataHash: Data) async throws -> [SecCertificate]](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/attestpendingkey(oftype:clientdatahash:))
- [func beginKeyRotation(ASAuthorizationProviderExtensionKeyType) -> SecKey?](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/beginkeyrotation(_:))
- [func completeKeyRotation(ASAuthorizationProviderExtensionKeyType)](/documentation/authenticationservices/asauthorizationproviderextensionloginmanager/completekeyrotation(_:))

### Authentication

- [Authentication process](/documentation/authenticationservices/authentication-process)

#### Pre-login

- [Obtaining a server nonce](/documentation/authenticationservices/obtaining-a-server-nonce)
- [Performing a preauthentication request](/documentation/authenticationservices/performing-a-preauthentication-request)
- [Performing a WS-Trust metadata exchange data (MEX) request](/documentation/authenticationservices/performing-a-ws-trust-metadata-exchange-data-mex-request)

#### Login request

- [Performing a WS-Trust login request](/documentation/authenticationservices/performing-a-ws-trust-login-request)
- [Creating an embedded assertion](/documentation/authenticationservices/creating-an-embedded-assertion)
- [Creating an encrypted embedded assertion](/documentation/authenticationservices/creating-an-encrypted-embedded-assertion)
- [Creating and validating a login request](/documentation/authenticationservices/creating-and-validating-a-login-request)
- [Creating a refresh request](/documentation/authenticationservices/creating-a-refresh-request)
- [Supporting key requests and key exchange requests](/documentation/authenticationservices/supporting-key-requests-and-key-exchange-requests)

#### Login response

- [Creating a JSON Web Encryption (JWE) login response](/documentation/authenticationservices/creating-a-json-web-encryption-jwe-login-response)
- [Processing the JSON Web Encryption (JWE) login response](/documentation/authenticationservices/processing-the-json-web-encryption-jwe-login-response)
- [Performing encryption verification](/documentation/authenticationservices/performing-encryption-verification)
- [ASAuthorizationProviderExtensionKerberosMapping](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping)

#### Getting the properties

- [var clientNameKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/clientnamekeyname)
- [var encryptionKeyTypeKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/encryptionkeytypekeyname)
- [var messageBufferKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/messagebufferkeyname)
- [var realmKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/realmkeyname)
- [var serviceNameKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/servicenamekeyname)
- [var sessionKeyKeyName: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/sessionkeykeyname)
- [var ticketKeyPath: String?](/documentation/authenticationservices/asauthorizationproviderextensionkerberosmapping/ticketkeypath)

## Apple TV authentication

- [var customAuthorizationMethods: [ASAuthorizationCustomMethod]](/documentation/authenticationservices/asauthorizationcontroller/customauthorizationmethods)
- [func authorizationController(ASAuthorizationController, didCompleteWithCustomMethod: ASAuthorizationCustomMethod)](/documentation/authenticationservices/asauthorizationcontrollerdelegate/authorizationcontroller(_:didcompletewithcustommethod:))
- [ASAuthorizationCustomMethod](/documentation/authenticationservices/asauthorizationcustommethod)

### Creating the Structure

- [init(rawValue: String)](/documentation/authenticationservices/asauthorizationcustommethod/init(rawvalue:))

### Getting the Properties

- [static let videoSubscriberAccount: ASAuthorizationCustomMethod](/documentation/authenticationservices/asauthorizationcustommethod/videosubscriberaccount)
- [static let restorePurchase: ASAuthorizationCustomMethod](/documentation/authenticationservices/asauthorizationcustommethod/restorepurchase)
- [static let other: ASAuthorizationCustomMethod](/documentation/authenticationservices/asauthorizationcustommethod/other)

## Automatic security upgrades

- [Upgrading Account Security With an Account Authentication Modification Extension](/documentation/authenticationservices/upgrading-account-security-with-an-account-authentication-modification-extension)
- [ASAccountAuthenticationModificationController](/documentation/authenticationservices/asaccountauthenticationmodificationcontroller)

### Initiating Security Upgrades from Your App

- [func perform(ASAccountAuthenticationModificationRequest)](/documentation/authenticationservices/asaccountauthenticationmodificationcontroller/perform(_:))
- [ASAccountAuthenticationModificationReplacePasswordWithSignInWithAppleRequest](/documentation/authenticationservices/asaccountauthenticationmodificationreplacepasswordwithsigninwithapplerequest)

#### Creating Upgrade Requests in Your App

- [init(user: String, serviceIdentifier: ASCredentialServiceIdentifier, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationreplacepasswordwithsigninwithapplerequest/init(user:serviceidentifier:userinfo:))
- [var user: String](/documentation/authenticationservices/asaccountauthenticationmodificationreplacepasswordwithsigninwithapplerequest/user)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/asaccountauthenticationmodificationreplacepasswordwithsigninwithapplerequest/serviceidentifier)
- [var userInfo: [AnyHashable : Any]?](/documentation/authenticationservices/asaccountauthenticationmodificationreplacepasswordwithsigninwithapplerequest/userinfo)
- [ASAccountAuthenticationModificationUpgradePasswordToStrongPasswordRequest](/documentation/authenticationservices/asaccountauthenticationmodificationupgradepasswordtostrongpasswordrequest)

#### Creating Upgrade Requests in Your App

- [init(user: String, serviceIdentifier: ASCredentialServiceIdentifier, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationupgradepasswordtostrongpasswordrequest/init(user:serviceidentifier:userinfo:))
- [var user: String](/documentation/authenticationservices/asaccountauthenticationmodificationupgradepasswordtostrongpasswordrequest/user)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/asaccountauthenticationmodificationupgradepasswordtostrongpasswordrequest/serviceidentifier)
- [var userInfo: [AnyHashable : Any]?](/documentation/authenticationservices/asaccountauthenticationmodificationupgradepasswordtostrongpasswordrequest/userinfo)
- [ASAccountAuthenticationModificationRequest](/documentation/authenticationservices/asaccountauthenticationmodificationrequest)

### Configuring Requests

- [var presentationContextProvider: (any ASAccountAuthenticationModificationControllerPresentationContextProviding)?](/documentation/authenticationservices/asaccountauthenticationmodificationcontroller/presentationcontextprovider)
- [var delegate: (any ASAccountAuthenticationModificationControllerDelegate)?](/documentation/authenticationservices/asaccountauthenticationmodificationcontroller/delegate)
- [ASAccountAuthenticationModificationViewController](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller)

### Upgrading to Sign in with Apple

- [func convertAccountToSignInWithAppleWithoutUserInteraction(for: ASCredentialServiceIdentifier, existingCredential: ASPasswordCredential, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/convertaccounttosigninwithapplewithoutuserinteraction(for:existingcredential:userinfo:))
- [func prepareInterfaceToConvertAccountToSignInWithApple(for: ASCredentialServiceIdentifier, existingCredential: ASPasswordCredential, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/prepareinterfacetoconvertaccounttosigninwithapple(for:existingcredential:userinfo:))
- [ASAccountAuthenticationModificationSupportsUpgradeToSignInWithApple](/documentation/bundleresources/information-property-list/nsextension/asaccountauthenticationmodificationsupportsupgradetosigninwithapple)

### Upgrading to Strong Passwords

- [func changePasswordWithoutUserInteraction(for: ASCredentialServiceIdentifier, existingCredential: ASPasswordCredential, newPassword: String, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/changepasswordwithoutuserinteraction(for:existingcredential:newpassword:userinfo:))
- [func prepareInterfaceToChangePassword(for: ASCredentialServiceIdentifier, existingCredential: ASPasswordCredential, newPassword: String, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/prepareinterfacetochangepassword(for:existingcredential:newpassword:userinfo:))
- [ASAccountAuthenticationModificationSupportsStrongPasswordChange](/documentation/bundleresources/information-property-list/nsextension/asaccountauthenticationmodificationsupportsstrongpasswordchange)
- [ASAccountAuthenticationModificationPasswordGenerationRequirements](/documentation/bundleresources/information-property-list/nsextension/asaccountauthenticationmodificationpasswordgenerationrequirements)
- [ASAccountAuthenticationModificationOptOutOfSecurityPromptsOnSignIn](/documentation/bundleresources/information-property-list/asaccountauthenticationmodificationoptoutofsecuritypromptsonsignin)

### Handling Modification Requests

- [func cancelRequest()](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/cancelrequest())
- [ASAccountAuthenticationModificationControllerDelegate](/documentation/authenticationservices/asaccountauthenticationmodificationcontrollerdelegate)

#### Handling Requests

- [func accountAuthenticationModificationController(ASAccountAuthenticationModificationController, didSuccessfullyComplete: ASAccountAuthenticationModificationRequest, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationcontrollerdelegate/accountauthenticationmodificationcontroller(_:didsuccessfullycomplete:userinfo:))
- [func accountAuthenticationModificationController(ASAccountAuthenticationModificationController, didFail: ASAccountAuthenticationModificationRequest, error: any Error)](/documentation/authenticationservices/asaccountauthenticationmodificationcontrollerdelegate/accountauthenticationmodificationcontroller(_:didfail:error:))
- [ASAccountAuthenticationModificationControllerPresentationContextProviding](/documentation/authenticationservices/asaccountauthenticationmodificationcontrollerpresentationcontextproviding)

#### Presenting the Account Modification Interface

- [func presentationAnchor(for: ASAccountAuthenticationModificationController) -> ASPresentationAnchor](/documentation/authenticationservices/asaccountauthenticationmodificationcontrollerpresentationcontextproviding/presentationanchor(for:))

### Getting the Extension Context

- [var extensionContext: ASAccountAuthenticationModificationExtensionContext](/documentation/authenticationservices/asaccountauthenticationmodificationviewcontroller/extensioncontext)
- [ASAccountAuthenticationModificationExtensionContext](/documentation/authenticationservices/asaccountauthenticationmodificationextensioncontext)

### Handling Requests

- [func completeUpgradeToSignInWithApple(userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationextensioncontext/completeupgradetosigninwithapple(userinfo:))
- [func completeChangePasswordRequest(updatedCredential: ASPasswordCredential, userInfo: [AnyHashable : Any]?)](/documentation/authenticationservices/asaccountauthenticationmodificationextensioncontext/completechangepasswordrequest(updatedcredential:userinfo:))
- [func getSignInWithAppleUpgradeAuthorization(state: String?, nonce: String?, completionHandler: (ASAuthorizationAppleIDCredential?, (any Error)?) -> Void)](/documentation/authenticationservices/asaccountauthenticationmodificationextensioncontext/getsigninwithappleupgradeauthorization(state:nonce:completionhandler:))
- [func cancelRequest(withError: any Error)](/documentation/authenticationservices/asaccountauthenticationmodificationextensioncontext/cancelrequest(witherror:))
- [let ASExtensionLocalizedFailureReasonErrorKey: String](/documentation/authenticationservices/asextensionlocalizedfailurereasonerrorkey)

## Updating credential managers

- [ASCredentialUpdater](/documentation/authenticationservices/ascredentialupdater)

### Creating a credential updater

- [init()](/documentation/authenticationservices/ascredentialupdater/init())

### Reporting accepted credentials

- [func reportAllAcceptedPublicKeyCredentials(relyingPartyIdentifier: String, userHandle: Data, acceptedCredentialIDs: [Data]) async throws](/documentation/authenticationservices/ascredentialupdater/reportallacceptedpublickeycredentials(relyingpartyidentifier:userhandle:acceptedcredentialids:))

### Reporting updated credentials

- [func reportPublicKeyCredentialUpdate(relyingPartyIdentifier: String, userHandle: Data, newName: String) async throws](/documentation/authenticationservices/ascredentialupdater/reportpublickeycredentialupdate(relyingpartyidentifier:userhandle:newname:))

### Reporting unused and unknown credentials

- [func reportUnusedPasswordCredential(domain: String, userName: String) async throws](/documentation/authenticationservices/ascredentialupdater/reportunusedpasswordcredential(domain:username:))
- [func reportUnknownPublicKeyCredential(relyingPartyIdentifier: String, credentialID: Data) async throws](/documentation/authenticationservices/ascredentialupdater/reportunknownpublickeycredential(relyingpartyidentifier:credentialid:))

## Reference

- [AuthenticationServices Enumerations](/documentation/authenticationservices/authenticationservices-enumerations)

### Enumerations

- [ASAuthorizationProviderExtensionLoginConfiguration.FederationType](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum)

#### Enumeration Cases

- [case dynamicWSTrust](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/dynamicwstrust)
- [case none](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/none)
- [case wsTrust](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/wstrust)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/federationtype-swift.enum/init(rawvalue:))
- [ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct)

#### Initializers

- [init(rawValue: UInt)](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/init(rawvalue:))

#### Type Properties

- [static var passwordFallback: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/passwordfallback)
- [static var reuseDuringUnlock: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/reuseduringunlock)
- [static var touchIDOrWatchAny: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/touchidorwatchany)
- [static var touchIDOrWatchCurrentSet: ASAuthorizationProviderExtensionLoginConfiguration.UserSecureEnclaveKeyBiometricPolicy](/documentation/authenticationservices/asauthorizationproviderextensionloginconfiguration/usersecureenclavekeybiometricpolicy-swift.struct/touchidorwatchcurrentset)
- [ASAuthorizationProviderExtensionPlatformSSOProtocolVersion](/documentation/authenticationservices/asauthorizationproviderextensionplatformssoprotocolversion)

#### Enumeration Cases

- [case version1_0](/documentation/authenticationservices/asauthorizationproviderextensionplatformssoprotocolversion/version1_0)
- [case version2_0](/documentation/authenticationservices/asauthorizationproviderextensionplatformssoprotocolversion/version2_0)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionplatformssoprotocolversion/init(rawvalue:))
- [ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes)

#### Initializers

- [init(rawValue: Int)](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes/init(rawvalue:))

#### Type Properties

- [static var jwtBearer: ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes/jwtbearer)
- [static var password: ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes/password)
- [static var saml1_1: ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes/saml1_1)
- [static var saml2_0: ASAuthorizationProviderExtensionSupportedGrantTypes](/documentation/authenticationservices/asauthorizationproviderextensionsupportedgranttypes/saml2_0)
- [ASAuthorizationPublicKeyCredentialAttachment](/documentation/authenticationservices/asauthorizationpublickeycredentialattachment)

#### Enumeration Cases

- [case crossPlatform](/documentation/authenticationservices/asauthorizationpublickeycredentialattachment/crossplatform)
- [case platform](/documentation/authenticationservices/asauthorizationpublickeycredentialattachment/platform)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asauthorizationpublickeycredentialattachment/init(rawvalue:))
- [ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes)

#### Working with identity types

- [static var passkey: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/passkey)
- [static var password: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/password)
- [static var oneTimeCode: ASCredentialIdentityStore.IdentityTypes](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/onetimecode)

#### Working with raw values

- [init(rawValue: UInt)](/documentation/authenticationservices/ascredentialidentitystore/identitytypes/init(rawvalue:))
- [ASPublicKeyCredentialClientDataCrossOriginValue](/documentation/authenticationservices/aspublickeycredentialclientdatacrossoriginvalue)

#### Enumeration Cases

- [case crossOrigin](/documentation/authenticationservices/aspublickeycredentialclientdatacrossoriginvalue/crossorigin)
- [case notSet](/documentation/authenticationservices/aspublickeycredentialclientdatacrossoriginvalue/notset)
- [case sameOriginWithAncestors](/documentation/authenticationservices/aspublickeycredentialclientdatacrossoriginvalue/sameoriginwithancestors)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/aspublickeycredentialclientdatacrossoriginvalue/init(rawvalue:))
- [ASUserAgeRange](/documentation/authenticationservices/asuseragerange)

#### Enumeration Cases

- [case child](/documentation/authenticationservices/asuseragerange/child)
- [case notChild](/documentation/authenticationservices/asuseragerange/notchild)
- [case unknown](/documentation/authenticationservices/asuseragerange/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/asuseragerange/init(rawvalue:))
- [AuthenticationServices Data Types](/documentation/authenticationservices/authenticationservices-data-types)

## Classes

- [ASAuthorizationAccountCreationPlatformPublicKeyCredential](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredential)

### Instance Properties

- [var contactIdentifier: ASContactIdentifier](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredential/contactidentifier)
- [var credentialRegistration: ASAuthorizationPlatformPublicKeyCredentialRegistration](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredential/credentialregistration)
- [var name: PersonNameComponents?](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredential/name)
- [ASAuthorizationAccountCreationPlatformPublicKeyCredentialRequest](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest)

### Instance Properties

- [let acceptedContactIdentifiers: [ASContactIdentifierRequest]](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/acceptedcontactidentifiers)
- [let challenge: Data](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/challenge)
- [let relyingPartyIdentifier: String](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/relyingpartyidentifier)
- [let shouldRequestName: Bool](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/shouldrequestname)
- [let userID: Data](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/userid)

### Instance Methods

- [func encode(with: NSCoder)](/documentation/authenticationservices/asauthorizationaccountcreationplatformpublickeycredentialrequest/encode(with:))
- [ASAuthorizationAccountCreationProvider](/documentation/authenticationservices/asauthorizationaccountcreationprovider)

### Initializers

- [init()](/documentation/authenticationservices/asauthorizationaccountcreationprovider/init())

### Instance Methods

- [func createPlatformPublicKeyCredentialRegistrationRequest(acceptedContactIdentifiers: [ASContactIdentifierRequest], shouldRequestName: Bool, relyingPartyIdentifier: String, challenge: Data, userID: Data) -> ASAuthorizationAccountCreationPlatformPublicKeyCredentialRequest](/documentation/authenticationservices/asauthorizationaccountcreationprovider/createplatformpublickeycredentialregistrationrequest(acceptedcontactidentifiers:shouldrequestname:relyingpartyidentifier:challenge:userid:))
- [ASAuthorizationProviderExtensionUserLoginConfiguration](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration)

### Initializers

- [init(loginUserName: String)](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/init(loginusername:))

### Instance Properties

- [var loginUserName: String](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/loginusername)

### Instance Methods

- [func setCustomAssertionRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/setcustomassertionrequestbodyclaims(_:))
- [func setCustomAssertionRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/setcustomassertionrequestheaderclaims(_:))
- [func setCustomLoginRequestBodyClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/setcustomloginrequestbodyclaims(_:))
- [func setCustomLoginRequestHeaderClaims([String : Any]) throws](/documentation/authenticationservices/asauthorizationproviderextensionuserloginconfiguration/setcustomloginrequestheaderclaims(_:))
- [ASCredentialDataManager](/documentation/authenticationservices/ascredentialdatamanager)

### Initializers

- [init()](/documentation/authenticationservices/ascredentialdatamanager/init())

### Instance Methods

- [func reportAllAcceptedPublicKeyCredentials(relyingPartyIdentifier: String, userHandle: Data, acceptedCredentialIDs: [Data]) async throws](/documentation/authenticationservices/ascredentialdatamanager/reportallacceptedpublickeycredentials(relyingpartyidentifier:userhandle:acceptedcredentialids:))
- [func reportPublicKeyCredentialUpdate(relyingPartyIdentifier: String, userHandle: Data, newName: String) async throws](/documentation/authenticationservices/ascredentialdatamanager/reportpublickeycredentialupdate(relyingpartyidentifier:userhandle:newname:))
- [func reportUnknownPublicKeyCredential(relyingPartyIdentifier: String, credentialID: Data) async throws](/documentation/authenticationservices/ascredentialdatamanager/reportunknownpublickeycredential(relyingpartyidentifier:credentialid:))
- [func reportUnusedPasswordCredential(domain: String, userName: String) async throws](/documentation/authenticationservices/ascredentialdatamanager/reportunusedpasswordcredential(domain:username:))
- [func save(password: ASPasswordCredential, for: ASAutoFillURLScope, title: String?, anchor: ASPresentationAnchor) async throws](/documentation/authenticationservices/ascredentialdatamanager/save(password:for:title:anchor:))
- [ASGeneratePasswordsRequest](/documentation/authenticationservices/asgeneratepasswordsrequest)

### Initializers

- [init(serviceIdentifier: ASCredentialServiceIdentifier, passwordFieldPasswordRules: String?, confirmPasswordFieldPasswordRules: String?, passwordRulesFromQuirks: String?)](/documentation/authenticationservices/asgeneratepasswordsrequest/init(serviceidentifier:passwordfieldpasswordrules:confirmpasswordfieldpasswordrules:passwordrulesfromquirks:))

### Instance Properties

- [var confirmPasswordFieldPasswordRules: String?](/documentation/authenticationservices/asgeneratepasswordsrequest/confirmpasswordfieldpasswordrules)
- [var passwordFieldPasswordRules: String?](/documentation/authenticationservices/asgeneratepasswordsrequest/passwordfieldpasswordrules)
- [var passwordRulesFromQuirks: String?](/documentation/authenticationservices/asgeneratepasswordsrequest/passwordrulesfromquirks)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/asgeneratepasswordsrequest/serviceidentifier)
- [ASGeneratedPassword](/documentation/authenticationservices/asgeneratedpassword)

### Structures

- [ASGeneratedPassword.Kind](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct)

#### Initializers

- [init(String)](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct/init(_:))
- [init(rawValue: String)](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct/init(rawvalue:))

#### Type Properties

- [static let alphanumeric: ASGeneratedPassword.Kind](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct/alphanumeric)
- [static let passphrase: ASGeneratedPassword.Kind](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct/passphrase)
- [static let strong: ASGeneratedPassword.Kind](/documentation/authenticationservices/asgeneratedpassword/kind-swift.struct/strong)

### Initializers

- [init(kind: ASGeneratedPassword.Kind, value: String)](/documentation/authenticationservices/asgeneratedpassword/init(kind:value:))

### Instance Properties

- [var kind: ASGeneratedPassword.Kind](/documentation/authenticationservices/asgeneratedpassword/kind-swift.property)
- [var localizedName: String](/documentation/authenticationservices/asgeneratedpassword/localizedname)
- [var value: String](/documentation/authenticationservices/asgeneratedpassword/value)
- [ASOneTimeCodeCredentialIdentity](/documentation/authenticationservices/asonetimecodecredentialidentity)

### Initializers

- [init(serviceIdentifier: ASCredentialServiceIdentifier, label: String, recordIdentifier: String?)](/documentation/authenticationservices/asonetimecodecredentialidentity/init(serviceidentifier:label:recordidentifier:))

### Instance Properties

- [var label: String](/documentation/authenticationservices/asonetimecodecredentialidentity/label)
- [ASSavePasswordRequest](/documentation/authenticationservices/assavepasswordrequest)

### Initializers

- [init(serviceIdentifier: ASCredentialServiceIdentifier, credential: ASPasswordCredential, sessionID: String, event: ASSavePasswordRequest.Event)](/documentation/authenticationservices/assavepasswordrequest/init(serviceidentifier:credential:sessionid:event:))
- [init(serviceIdentifier: ASCredentialServiceIdentifier, credential: ASPasswordCredential, sessionID: String, event: ASSavePasswordRequest.Event, passwordKind: ASGeneratedPassword.Kind?)](/documentation/authenticationservices/assavepasswordrequest/init(serviceidentifier:credential:sessionid:event:passwordkind:))
- [init(serviceIdentifier: ASCredentialServiceIdentifier, credential: ASPasswordCredential, title: String?, sessionID: String, event: ASSavePasswordRequest.Event)](/documentation/authenticationservices/assavepasswordrequest/init(serviceidentifier:credential:title:sessionid:event:))
- [init(serviceIdentifier: ASCredentialServiceIdentifier, credential: ASPasswordCredential, title: String?, sessionID: String, event: ASSavePasswordRequest.Event, passwordKind: ASGeneratedPassword.Kind?)](/documentation/authenticationservices/assavepasswordrequest/init(serviceidentifier:credential:title:sessionid:event:passwordkind:))

### Instance Properties

- [var credential: ASPasswordCredential](/documentation/authenticationservices/assavepasswordrequest/credential)
- [var event: ASSavePasswordRequest.Event](/documentation/authenticationservices/assavepasswordrequest/event-swift.property)
- [var passwordKind: ASGeneratedPassword.Kind?](/documentation/authenticationservices/assavepasswordrequest/passwordkind)
- [var serviceIdentifier: ASCredentialServiceIdentifier](/documentation/authenticationservices/assavepasswordrequest/serviceidentifier)
- [var sessionID: String](/documentation/authenticationservices/assavepasswordrequest/sessionid)
- [var title: String?](/documentation/authenticationservices/assavepasswordrequest/title)

### Enumerations

- [ASSavePasswordRequest.Event](/documentation/authenticationservices/assavepasswordrequest/event-swift.enum)

#### Enumeration Cases

- [case formDidDisappear](/documentation/authenticationservices/assavepasswordrequest/event-swift.enum/formdiddisappear)
- [case generatedPasswordFilled](/documentation/authenticationservices/assavepasswordrequest/event-swift.enum/generatedpasswordfilled)
- [case userInitiated](/documentation/authenticationservices/assavepasswordrequest/event-swift.enum/userinitiated)

#### Initializers

- [init?(rawValue: Int)](/documentation/authenticationservices/assavepasswordrequest/event-swift.enum/init(rawvalue:))

## Structures

- [ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm)

### Initializers

- [init(NSNumber)](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/init(_:))
- [init(rawValue: NSNumber)](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/init(rawvalue:))

### Type Properties

- [static let ecdhe_A256GCM: ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/ecdhe_a256gcm)
- [static let hpke_Curve25519_SHA256_ChachaPoly: ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/hpke_curve25519_sha256_chachapoly)
- [static let hpke_P256_SHA256_AES_GCM_256: ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/hpke_p256_sha256_aes_gcm_256)
- [static let hpke_P384_SHA384_AES_GCM_256: ASAuthorizationProviderExtensionEncryptionAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionencryptionalgorithm/hpke_p384_sha384_aes_gcm_256)
- [ASAuthorizationProviderExtensionSigningAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm)

### Initializers

- [init(NSNumber)](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm/init(_:))
- [init(rawValue: NSNumber)](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm/init(rawvalue:))

### Type Properties

- [static let ed25519: ASAuthorizationProviderExtensionSigningAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm/ed25519)
- [static let es256: ASAuthorizationProviderExtensionSigningAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm/es256)
- [static let es384: ASAuthorizationProviderExtensionSigningAlgorithm](/documentation/authenticationservices/asauthorizationproviderextensionsigningalgorithm/es384)
- [ASAutoFillURLScope](/documentation/authenticationservices/asautofillurlscope)

### Initializers

- [init(scheme: ASAutoFillURLScope.Scheme, host: String, port: Int?, path: String)](/documentation/authenticationservices/asautofillurlscope/init(scheme:host:port:path:))
- [init?(url: URL)](/documentation/authenticationservices/asautofillurlscope/init(url:))

### Instance Properties

- [var host: String](/documentation/authenticationservices/asautofillurlscope/host)
- [var path: String](/documentation/authenticationservices/asautofillurlscope/path)
- [var port: Int?](/documentation/authenticationservices/asautofillurlscope/port)
- [var scheme: ASAutoFillURLScope.Scheme](/documentation/authenticationservices/asautofillurlscope/scheme-swift.property)
- [var url: URL?](/documentation/authenticationservices/asautofillurlscope/url)

### Enumerations

- [ASAutoFillURLScope.Scheme](/documentation/authenticationservices/asautofillurlscope/scheme-swift.enum)

#### Enumeration Cases

- [case http](/documentation/authenticationservices/asautofillurlscope/scheme-swift.enum/http)
- [case https](/documentation/authenticationservices/asautofillurlscope/scheme-swift.enum/https)
- [ASEmailIdentifier](/documentation/authenticationservices/asemailidentifier)

### Instance Properties

- [var value: String](/documentation/authenticationservices/asemailidentifier/value)
- [ASImportableCredentialScope](/documentation/authenticationservices/asimportablecredentialscope)

### Structures

- [ASImportableCredentialScope.AndroidAppCertificationFingerprint](/documentation/authenticationservices/asimportablecredentialscope/androidappcertificationfingerprint)

#### Initializers

- [init(fingerprint: Data, hashAlgorithm: String)](/documentation/authenticationservices/asimportablecredentialscope/androidappcertificationfingerprint/init(fingerprint:hashalgorithm:))

#### Instance Properties

- [var fingerprint: Data](/documentation/authenticationservices/asimportablecredentialscope/androidappcertificationfingerprint/fingerprint)
- [var hashAlgorithm: String](/documentation/authenticationservices/asimportablecredentialscope/androidappcertificationfingerprint/hashalgorithm)
- [ASImportableCredentialScope.AndroidAppID](/documentation/authenticationservices/asimportablecredentialscope/androidappid)

#### Initializers

- [init(bundleID: String, certificate: ASImportableCredentialScope.AndroidAppCertificationFingerprint?, name: String?)](/documentation/authenticationservices/asimportablecredentialscope/androidappid/init(bundleid:certificate:name:))

#### Instance Properties

- [var bundleID: String](/documentation/authenticationservices/asimportablecredentialscope/androidappid/bundleid)
- [var certificate: ASImportableCredentialScope.AndroidAppCertificationFingerprint?](/documentation/authenticationservices/asimportablecredentialscope/androidappid/certificate)
- [var name: String?](/documentation/authenticationservices/asimportablecredentialscope/androidappid/name)

### Initializers

- [init(urls: [URL], androidApps: [ASImportableCredentialScope.AndroidAppID])](/documentation/authenticationservices/asimportablecredentialscope/init(urls:androidapps:))

### Instance Properties

- [var androidApps: [ASImportableCredentialScope.AndroidAppID]](/documentation/authenticationservices/asimportablecredentialscope/androidapps)
- [var urls: [URL]](/documentation/authenticationservices/asimportablecredentialscope/urls)
- [ASImportableEditableField](/documentation/authenticationservices/asimportableeditablefield)

### Creating an editable field

- [init(id: Data?, fieldType: ASImportableEditableField.FieldType, value: String, label: String?)](/documentation/authenticationservices/asimportableeditablefield/init(id:fieldtype:value:label:))

### Accessing field properties

- [var id: Data?](/documentation/authenticationservices/asimportableeditablefield/id)
- [var fieldType: ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.property)
- [ASImportableEditableField.FieldType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum)

#### Determining field type

- [case boolean](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/boolean)
- [case concealedString](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/concealedstring)
- [case date](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/date)
- [case email](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/email)
- [case number](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/number)
- [case string](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/string)

#### Enumeration Cases

- [case countryCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/countrycode)
- [case subdivisionCode](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/subdivisioncode)
- [case wifiNetworkSecurityType](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/wifinetworksecuritytype)
- [case yearMonth](/documentation/authenticationservices/asimportableeditablefield/fieldtype-swift.enum/yearmonth)
- [var value: String](/documentation/authenticationservices/asimportableeditablefield/value)
- [var label: String?](/documentation/authenticationservices/asimportableeditablefield/label)
- [ASPhoneNumberIdentifier](/documentation/authenticationservices/asphonenumberidentifier)

### Instance Properties

- [var value: String](/documentation/authenticationservices/asphonenumberidentifier/value)
- [ASPublicKeyCredentialClientData](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct)

### Initializers

- [init(challenge: Data, origin: String, topOrigin: String?, crossOrigin: ASPublicKeyCredentialClientData.CrossOriginValue?)](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/init(challenge:origin:toporigin:crossorigin:))

### Instance Properties

- [var challenge: Data](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/challenge)
- [var crossOrigin: ASPublicKeyCredentialClientData.CrossOriginValue?](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/crossorigin)
- [var origin: String](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/origin)
- [var topOrigin: String?](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/toporigin)

### Enumerations

- [ASPublicKeyCredentialClientData.CrossOriginValue](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/crossoriginvalue)

#### Enumeration Cases

- [case crossOrigin](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/crossoriginvalue/crossorigin)
- [case sameOriginWithAncestors](/documentation/authenticationservices/aspublickeycredentialclientdata-swift.struct/crossoriginvalue/sameoriginwithancestors)
- [CredentialDataManager](/documentation/authenticationservices/credentialdatamanager)

### Instance Methods

- [func reportAllAcceptedPublicKeyCredentials(relyingPartyIdentifier: String, userHandle: Data, acceptedCredentialIDs: [Data]) async throws](/documentation/authenticationservices/credentialdatamanager/reportallacceptedpublickeycredentials(relyingpartyidentifier:userhandle:acceptedcredentialids:))
- [func reportPublicKeyCredentialUpdate(relyingPartyIdentifier: String, userHandle: Data, newName: String) async throws](/documentation/authenticationservices/credentialdatamanager/reportpublickeycredentialupdate(relyingpartyidentifier:userhandle:newname:))
- [func reportUnknownPublicKeyCredential(relyingPartyIdentifier: String, credentialID: Data) async throws](/documentation/authenticationservices/credentialdatamanager/reportunknownpublickeycredential(relyingpartyidentifier:credentialid:))
- [func reportUnusedPasswordCredential(domain: String, userName: String) async throws](/documentation/authenticationservices/credentialdatamanager/reportunusedpasswordcredential(domain:username:))
- [func save(password: ASPasswordCredential, for: ASAutoFillURLScope, title: String?) async throws](/documentation/authenticationservices/credentialdatamanager/save(password:for:title:))

## Variables

- [let ASCredentialExchangeActivity: String](/documentation/authenticationservices/ascredentialexchangeactivity)
- [let ASCredentialImportToken: String](/documentation/authenticationservices/ascredentialimporttoken)

## Enumerations

- [ASContactIdentifier](/documentation/authenticationservices/ascontactidentifier)

### Enumeration Cases

- [case email(ASEmailIdentifier)](/documentation/authenticationservices/ascontactidentifier/email(_:))
- [case phoneNumber(ASPhoneNumberIdentifier)](/documentation/authenticationservices/ascontactidentifier/phonenumber(_:))
- [ASContactIdentifierRequest](/documentation/authenticationservices/ascontactidentifierrequest)

### Enumeration Cases

- [case email](/documentation/authenticationservices/ascontactidentifierrequest/email)
- [case phoneNumber](/documentation/authenticationservices/ascontactidentifierrequest/phonenumber)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
