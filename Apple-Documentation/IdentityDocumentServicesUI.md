# IdentityDocumentServicesUI Documentation

Source: https://sosumi.ai/documentation/identitydocumentservicesui

---
title: IdentityDocumentServicesUI
source: https://developer.apple.com/documentation/identitydocumentservicesui
timestamp: 2026-02-13T18:58:02.858Z
---

## Building identity document provider authorization UI

- [IdentityDocumentProvider](/documentation/identitydocumentservicesui/identitydocumentprovider)

### Associated Types

- [Body](/documentation/identitydocumentservicesui/identitydocumentprovider/body-swift.associatedtype)

### Instance Properties

- [var body: Self.Body](/documentation/identitydocumentservicesui/identitydocumentprovider/body-swift.property)

### Instance Methods

- [func performRegistrationUpdates() async](/documentation/identitydocumentservicesui/identitydocumentprovider/performregistrationupdates())
- [IdentityDocumentRequestScene](/documentation/identitydocumentservicesui/identitydocumentrequestscene)
- [ISO18013MobileDocumentRequestScene](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestscene)

### Initializers

- [init(content: (ISO18013MobileDocumentRequestContext) -> Content)](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestscene/init(content:))
- [ISO18013MobileDocumentRequestContext](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestcontext)

### Instance Properties

- [let request: ISO18013MobileDocumentRequest](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestcontext/request)
- [let requestingWebsiteOrigin: URL?](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestcontext/requestingwebsiteorigin)

### Instance Methods

- [func cancel()](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestcontext/cancel())
- [func sendResponse((IdentityDocumentWebPresentmentRawRequest) async throws -> ISO18013MobileDocumentResponse) async throws](/documentation/identitydocumentservicesui/iso18013mobiledocumentrequestcontext/sendresponse(_:))
- [IdentityDocumentRequestSceneBuilder](/documentation/identitydocumentservicesui/identitydocumentrequestscenebuilder)

### Type Methods

- [static func buildBlock(some IdentityDocumentRequestScene) -> some IdentityDocumentRequestScene](/documentation/identitydocumentservicesui/identitydocumentrequestscenebuilder/buildblock(_:))
- [static func buildBlock(some IdentityDocumentRequestScene, some IdentityDocumentRequestScene) -> some IdentityDocumentRequestScene](/documentation/identitydocumentservicesui/identitydocumentrequestscenebuilder/buildblock(_:_:))
- [static func buildLimitedAvailability(some IdentityDocumentRequestScene) -> some IdentityDocumentRequestScene](/documentation/identitydocumentservicesui/identitydocumentrequestscenebuilder/buildlimitedavailability(_:))
- [static func buildOptional((some IdentityDocumentRequestScene)?) -> some IdentityDocumentRequestScene](/documentation/identitydocumentservicesui/identitydocumentrequestscenebuilder/buildoptional(_:))

## Implementing the web presentment flow into your browser

- [Implementing as an identity document provider](/documentation/identitydocumentservices/implenting-as-an-identity-document-provider)
- [IdentityDocumentWebPresentmentController](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontroller)

### Initializers

- [init()](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontroller/init())

### Instance Properties

- [var delegate: (any IdentityDocumentWebPresentmentControllerDelegate)?](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontroller/delegate)
- [var presentationContextProvider: (any IdentityDocumentPresentmentControllerPresentationContextProviding)?](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontroller/presentationcontextprovider)

### Instance Methods

- [func performRequests([any IdentityDocumentWebPresentmentRequest], origin: URL) async throws -> any IdentityDocumentWebPresentmentResponse](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontroller/performrequests(_:origin:))
- [IdentityDocumentWebPresentmentControllerDelegate](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontrollerdelegate)

### Instance Methods

- [func rawRequestsForWebPresentmentController(IdentityDocumentWebPresentmentController) async -> [IdentityDocumentWebPresentmentRawRequest]](/documentation/identitydocumentservicesui/identitydocumentwebpresentmentcontrollerdelegate/rawrequestsforwebpresentmentcontroller(_:))
- [IdentityDocumentPresentmentControllerPresentationContextProviding](/documentation/identitydocumentservicesui/identitydocumentpresentmentcontrollerpresentationcontextproviding)

### Instance Methods

- [func presentationAnchorForPresentmentController(any IdentityDocumentPresentmentControlling) -> IdentityDocumentPresentationAnchor?](/documentation/identitydocumentservicesui/identitydocumentpresentmentcontrollerpresentationcontextproviding/presentationanchorforpresentmentcontroller(_:)-26ohw)
- [func presentationAnchorForPresentmentController(any IdentityDocumentPresentmentControlling) -> IdentityDocumentPresentationAnchor?](/documentation/identitydocumentservicesui/identitydocumentpresentmentcontrollerpresentationcontextproviding/presentationanchorforpresentmentcontroller(_:)-58gth)
- [IdentityDocumentPresentationAnchor](/documentation/identitydocumentservicesui/identitydocumentpresentationanchor)
- [IdentityDocumentPresentmentControlling](/documentation/identitydocumentservicesui/identitydocumentpresentmentcontrolling)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
