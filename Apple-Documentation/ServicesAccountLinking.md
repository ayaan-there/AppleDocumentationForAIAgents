# ServicesAccountLinking Documentation

Source: https://sosumi.ai/documentation/servicesaccountlinking

---
title: ServicesAccountLinking
source: https://developer.apple.com/documentation/servicesaccountlinking
timestamp: 2026-02-13T19:02:05.499Z
---

## Registration

- [ResellerAccount](/documentation/servicesaccountlinking/reselleraccount)

### Registration methods

- [static func registerToken(String) async throws](/documentation/servicesaccountlinking/reselleraccount/registertoken(_:))
- [static func registerIdentifier(String) async throws](/documentation/servicesaccountlinking/reselleraccount/registeridentifier(_:))

### Initializers

- [init()](/documentation/servicesaccountlinking/reselleraccount/init())

## Error handling

- [RegistrationError](/documentation/servicesaccountlinking/registrationerror)

### Type Properties

- [static var errorDomain: String](/documentation/servicesaccountlinking/registrationerror/errordomain)
- [static var failed: RegistrationError.Code](/documentation/servicesaccountlinking/registrationerror/failed)
- [static var notEligible: RegistrationError.Code](/documentation/servicesaccountlinking/registrationerror/noteligible)

### Enumerations

- [RegistrationError.Code](/documentation/servicesaccountlinking/registrationerror/code)

#### Enumeration Cases

- [case failed](/documentation/servicesaccountlinking/registrationerror/code/failed)
- [case notEligible](/documentation/servicesaccountlinking/registrationerror/code/noteligible)

#### Initializers

- [init?(rawValue: Int)](/documentation/servicesaccountlinking/registrationerror/code/init(rawvalue:))
- [let RegistrationErrorDomain: String](/documentation/servicesaccountlinking/registrationerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
