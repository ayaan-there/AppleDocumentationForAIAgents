# IdentityDocumentServices Documentation

Source: https://sosumi.ai/documentation/identitydocumentservices

---
title: IdentityDocumentServices
source: https://developer.apple.com/documentation/identitydocumentservices
timestamp: 2026-02-13T18:58:00.717Z
---

## Essentials

- [Requesting a mobile document on the web](/documentation/identitydocumentservices/requesting-a-mobile-document-on-the-web)
- [Implementing as an identity document provider](/documentation/identitydocumentservices/implenting-as-an-identity-document-provider)

## Registering as an identity document provider

- [IdentityDocumentProviderRegistrationStore](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore)

### Registering and removing mobile documents

- [init()](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/init())
- [func addRegistration(some IdentityDocumentRegistration) async throws](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/addregistration(_:))
- [var registrations: [any IdentityDocumentRegistration]](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrations)
- [func removeRegistration(forDocumentIdentifier: String) async throws](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/removeregistration(fordocumentidentifier:))

### Defining and getting the status of the mobile document

- [var status: IdentityDocumentProviderRegistrationStore.Status](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.property)
- [IdentityDocumentProviderRegistrationStore.Status](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.enum)

#### Enumeration Cases

- [case authorized](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.enum/authorized)
- [case notAuthorized](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.enum/notauthorized)
- [case notDetermined](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.enum/notdetermined)
- [case notSupported](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/status-swift.enum/notsupported)

### Errors

- [IdentityDocumentProviderRegistrationStore.RegistrationError](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrationerror)

#### Enumeration Cases

- [case invalidRequest](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrationerror/invalidrequest)
- [case notAuthorized](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrationerror/notauthorized)
- [case notSupported](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrationerror/notsupported)
- [case unknown](/documentation/identitydocumentservices/identitydocumentproviderregistrationstore/registrationerror/unknown)
- [IdentityDocumentRegistration](/documentation/identitydocumentservices/identitydocumentregistration)

### Instance Properties

- [var documentIdentifier: String](/documentation/identitydocumentservices/identitydocumentregistration/documentidentifier)
- [MobileDocumentRegistration](/documentation/identitydocumentservices/mobiledocumentregistration)

### Initializers

- [init(mobileDocumentType: String, supportedAuthorityKeyIdentifiers: [Data], documentIdentifier: String, invalidationDate: Date?)](/documentation/identitydocumentservices/mobiledocumentregistration/init(mobiledocumenttype:supportedauthoritykeyidentifiers:documentidentifier:invalidationdate:))

### Instance Properties

- [var invalidationDate: Date?](/documentation/identitydocumentservices/mobiledocumentregistration/invalidationdate)
- [var mobileDocumentType: String](/documentation/identitydocumentservices/mobiledocumentregistration/mobiledocumenttype)
- [var supportedAuthorityKeyIdentifiers: [Data]](/documentation/identitydocumentservices/mobiledocumentregistration/supportedauthoritykeyidentifiers)

## Implementing the web presentment flow into your browser

- [IdentityDocumentWebPresentmentRawRequestValidator](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator)

### Initializers

- [init()](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator/init())

### Instance Methods

- [func validateISO18013MobileDocumentRequest(Data, origin: URL) throws -> ISO18013MobileDocumentRequest](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator/validateiso18013mobiledocumentrequest(_:origin:))
- [IdentityDocumentWebPresentmentRequest](/documentation/identitydocumentservices/identitydocumentwebpresentmentrequest)
- [ISO18013MobileDocumentRequest](/documentation/identitydocumentservices/iso18013mobiledocumentrequest)

### Structures

- [ISO18013MobileDocumentRequest.DocumentRequest](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequest)

#### Initializers

- [init(documentType: String, namespaces: [String : [String : ISO18013MobileDocumentRequest.ElementInfo]])](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequest/init(documenttype:namespaces:))

#### Instance Properties

- [var documentType: String](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequest/documenttype)
- [var namespaces: [String : [String : ISO18013MobileDocumentRequest.ElementInfo]]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequest/namespaces)
- [ISO18013MobileDocumentRequest.DocumentRequestSet](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequestset)

#### Initializers

- [init(requests: [ISO18013MobileDocumentRequest.DocumentRequest])](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequestset/init(requests:))

#### Instance Properties

- [var requests: [ISO18013MobileDocumentRequest.DocumentRequest]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/documentrequestset/requests)
- [ISO18013MobileDocumentRequest.ElementInfo](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/elementinfo)

#### Initializers

- [init(isRetaining: Bool)](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/elementinfo/init(isretaining:))

#### Instance Properties

- [var isRetaining: Bool](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/elementinfo/isretaining)
- [ISO18013MobileDocumentRequest.PresentmentRequest](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/presentmentrequest)

#### Initializers

- [init(documentRequestSets: [ISO18013MobileDocumentRequest.DocumentRequestSet], isMandatory: Bool)](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/presentmentrequest/init(documentrequestsets:ismandatory:))

#### Instance Properties

- [var documentRequestSets: [ISO18013MobileDocumentRequest.DocumentRequestSet]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/presentmentrequest/documentrequestsets)
- [var isMandatory: Bool](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/presentmentrequest/ismandatory)
- [ISO18013MobileDocumentRequest.RequestAuthentication](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/requestauthentication)

#### Initializers

- [init(authenticationCertificateChain: [SecCertificate])](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/requestauthentication/init(authenticationcertificatechain:))

#### Instance Properties

- [var authenticationCertificateChain: [SecCertificate]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/requestauthentication/authenticationcertificatechain)

### Initializers

- [init(presentmentRequests: [ISO18013MobileDocumentRequest.PresentmentRequest], requestAuthentications: [ISO18013MobileDocumentRequest.RequestAuthentication])](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/init(presentmentrequests:requestauthentications:))

### Instance Properties

- [var presentmentRequests: [ISO18013MobileDocumentRequest.PresentmentRequest]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/presentmentrequests)
- [var requestAuthentications: [ISO18013MobileDocumentRequest.RequestAuthentication]](/documentation/identitydocumentservices/iso18013mobiledocumentrequest/requestauthentications)
- [IdentityDocumentWebPresentmentResponse](/documentation/identitydocumentservices/identitydocumentwebpresentmentresponse)
- [ISO18013MobileDocumentResponse](/documentation/identitydocumentservices/iso18013mobiledocumentresponse)

### Initializers

- [init(responseData: Data)](/documentation/identitydocumentservices/iso18013mobiledocumentresponse/init(responsedata:))

### Instance Properties

- [let responseData: Data](/documentation/identitydocumentservices/iso18013mobiledocumentresponse/responsedata)
- [IdentityDocumentWebPresentmentRawRequest](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest)

### Creating an identity document web presentment raw request

- [init(requestType: IdentityDocumentWebPresentmentRawRequest.RequestType, requestData: Data)](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest/init(requesttype:requestdata:))
- [var requestData: Data](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest/requestdata)
- [var requestType: IdentityDocumentWebPresentmentRawRequest.RequestType](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest/requesttype-swift.property)

### Validating a web presentment raw request

- [IdentityDocumentWebPresentmentRawRequestValidator](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator)

#### Initializers

- [init()](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator/init())

#### Instance Methods

- [func validateISO18013MobileDocumentRequest(Data, origin: URL) throws -> ISO18013MobileDocumentRequest](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequestvalidator/validateiso18013mobiledocumentrequest(_:origin:))

### Enumerations

- [IdentityDocumentWebPresentmentRawRequest.RequestType](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest/requesttype-swift.enum)

#### Enumeration Cases

- [case iso18013MobileDocument](/documentation/identitydocumentservices/identitydocumentwebpresentmentrawrequest/requesttype-swift.enum/iso18013mobiledocument)

## Structures

- [IdentityDocumentPresentmentError](/documentation/identitydocumentservices/identitydocumentpresentmenterror)

### Instance Properties

- [let code: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.property)
- [let debugDescription: String](/documentation/identitydocumentservices/identitydocumentpresentmenterror/debugdescription)

### Type Properties

- [static let cancelled: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/cancelled)
- [static let invalidRequest: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/invalidrequest)
- [static let notEntitled: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/notentitled)
- [static let requestInProgress: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/requestinprogress)
- [static let unknown: IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/unknown)

### Enumerations

- [IdentityDocumentPresentmentError.Code](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum)

#### Operators

- [static func ~= (IdentityDocumentPresentmentError.Code, any Error) -> Bool](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/~=(_:_:))

#### Enumeration Cases

- [case cancelled](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/cancelled)
- [case invalidRequest](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/invalidrequest)
- [case notEntitled](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/notentitled)
- [case requestInProgress](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/requestinprogress)
- [case unknown](/documentation/identitydocumentservices/identitydocumentpresentmenterror/code-swift.enum/unknown)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
