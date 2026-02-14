# Security Foundation Documentation

Source: https://sosumi.ai/documentation/securityfoundation

---
title: Security Foundation
source: https://developer.apple.com/documentation/securityfoundation
timestamp: 2026-02-13T19:01:53.662Z
---

## Classes

- [SFAuthorization](/documentation/securityfoundation/sfauthorization)

### Allocating and initializing an authorization object

- [class func authorization() -> Any!](/documentation/securityfoundation/sfauthorization/authorization())
- [class func authorization(with: AuthorizationFlags, rights: UnsafePointer<AuthorizationRights>!, environment: UnsafePointer<AuthorizationEnvironment>!) -> Any!](/documentation/securityfoundation/sfauthorization/authorization(with:rights:environment:))
- [init!()](/documentation/securityfoundation/sfauthorization/init())
- [init!(flags: AuthorizationFlags, rights: UnsafePointer<AuthorizationRights>!, environment: UnsafePointer<AuthorizationEnvironment>!)](/documentation/securityfoundation/sfauthorization/init(flags:rights:environment:))

### Obtaining an authorization reference

- [func authorizationRef() -> AuthorizationRef!](/documentation/securityfoundation/sfauthorization/authorizationref())

### Authorizing rights

- [func obtain(withRights: UnsafePointer<AuthorizationRights>!, flags: AuthorizationFlags, environment: UnsafePointer<AuthorizationEnvironment>!, authorizedRights: UnsafeMutablePointer<UnsafeMutablePointer<AuthorizationRights>?>!) throws](/documentation/securityfoundation/sfauthorization/obtain(withrights:flags:environment:authorizedrights:))
- [func obtain(withRight: AuthorizationString!, flags: AuthorizationFlags) throws](/documentation/securityfoundation/sfauthorization/obtain(withright:flags:))

### Preventing credentials from being shared

- [func invalidateCredentials()](/documentation/securityfoundation/sfauthorization/invalidatecredentials())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
