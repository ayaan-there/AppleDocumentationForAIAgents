# File Provider UI Documentation

Source: https://sosumi.ai/documentation/fileproviderui

---
title: File Provider UI
source: https://developer.apple.com/documentation/fileproviderui
timestamp: 2026-02-13T18:57:00.545Z
---

## Document Browser Customization

- [Adding Actions to the Context Menu](/documentation/fileproviderui/adding-actions-to-the-context-menu)
- [FPUIActionExtensionViewController](/documentation/fileproviderui/fpuiactionextensionviewcontroller)

### Working with Actions

- [func prepare(forAction: String, itemIdentifiers: [NSFileProviderItemIdentifier])](/documentation/fileproviderui/fpuiactionextensionviewcontroller/prepare(foraction:itemidentifiers:))
- [func prepare(forError: any Error)](/documentation/fileproviderui/fpuiactionextensionviewcontroller/prepare(forerror:))
- [var extensionContext: FPUIActionExtensionContext](/documentation/fileproviderui/fpuiactionextensionviewcontroller/extensioncontext)
- [FPUIActionExtensionContext](/documentation/fileproviderui/fpuiactionextensioncontext)

#### Completing the Action

- [func completeRequest()](/documentation/fileproviderui/fpuiactionextensioncontext/completerequest())
- [func cancelRequest(withError: any Error)](/documentation/fileproviderui/fpuiactionextensioncontext/cancelrequest(witherror:))

#### Identifying the Domain

- [var domainIdentifier: NSFileProviderDomainIdentifier?](/documentation/fileproviderui/fpuiactionextensioncontext/domainidentifier)
- [NSFileProviderDomainIdentifier](/documentation/fileprovider/nsfileproviderdomainidentifier)

## Errors

- [FPUIExtensionErrorCode](/documentation/fileproviderui/fpuiextensionerrorcode)

### Error Codes

- [case failed](/documentation/fileproviderui/fpuiextensionerrorcode/failed)
- [case userCancelled](/documentation/fileproviderui/fpuiextensionerrorcode/usercancelled)

### Initializers

- [init?(rawValue: UInt)](/documentation/fileproviderui/fpuiextensionerrorcode/init(rawvalue:))
- [let FPUIErrorDomain: String](/documentation/fileproviderui/fpuierrordomain)

## Reference

- [FileProviderUI Data Types](/documentation/fileproviderui/fileproviderui-data-types)

### Data Types

- [FPUIActionIdentifier](/documentation/fileproviderui/fpuiactionidentifier)

#### Initializers

- [init(String)](/documentation/fileproviderui/fpuiactionidentifier/init(_:))
- [init(rawValue: String)](/documentation/fileproviderui/fpuiactionidentifier/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
