# Service Management Documentation

Source: https://sosumi.ai/documentation/servicemanagement

---
title: Service Management
source: https://developer.apple.com/documentation/servicemanagement
timestamp: 2026-02-13T19:02:03.595Z
---

## Essentials

- [Updating helper executables from earlier versions of macOS](/documentation/servicemanagement/updating-helper-executables-from-earlier-versions-of-macos)
- [Updating your app package installer to use the new Service Management API](/documentation/servicemanagement/updating-your-app-package-installer-to-use-the-new-service-management-api)

## Management

- [SMAppService](/documentation/servicemanagement/smappservice)

### Registering services

- [func register() throws](/documentation/servicemanagement/smappservice/register())
- [func unregister() throws](/documentation/servicemanagement/smappservice/unregister())
- [func unregister(completionHandler: ((any Error)?) -> Void)](/documentation/servicemanagement/smappservice/unregister(completionhandler:))

### Managing apps

- [class var mainApp: SMAppService](/documentation/servicemanagement/smappservice/mainapp)
- [class func agent(plistName: String) -> Self](/documentation/servicemanagement/smappservice/agent(plistname:))
- [class func daemon(plistName: String) -> Self](/documentation/servicemanagement/smappservice/daemon(plistname:))
- [class func loginItem(identifier: String) -> Self](/documentation/servicemanagement/smappservice/loginitem(identifier:))

### Interacting with System Settings

- [class func openSystemSettingsLoginItems()](/documentation/servicemanagement/smappservice/opensystemsettingsloginitems())

### Getting the state of the service

- [var status: SMAppService.Status](/documentation/servicemanagement/smappservice/status-swift.property)
- [SMAppService.Status](/documentation/servicemanagement/smappservice/status-swift.enum)

#### Constants

- [case notRegistered](/documentation/servicemanagement/smappservice/status-swift.enum/notregistered)
- [case enabled](/documentation/servicemanagement/smappservice/status-swift.enum/enabled)
- [case requiresApproval](/documentation/servicemanagement/smappservice/status-swift.enum/requiresapproval)
- [case notFound](/documentation/servicemanagement/smappservice/status-swift.enum/notfound)

#### Initializers

- [init?(rawValue: Int)](/documentation/servicemanagement/smappservice/status-swift.enum/init(rawvalue:))

### Checking authorization for earlier OS version login items

- [class func statusForLegacyPlist(at: URL) -> SMAppService.Status](/documentation/servicemanagement/smappservice/statusforlegacyplist(at:))
- [func SMJobBless(CFString!, CFString, AuthorizationRef!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/servicemanagement/smjobbless(_:_:_:_:))
- [Authorization Constants](/documentation/servicemanagement/authorization-constants)

### Constants

- [var kSMRightBlessPrivilegedHelper: String](/documentation/servicemanagement/ksmrightblessprivilegedhelper)
- [var kSMRightBlessPrivilegedHelper: String](/documentation/servicemanagement/ksmrightblessprivilegedhelper)
- [var kSMRightModifySystemDaemons: String](/documentation/servicemanagement/ksmrightmodifysystemdaemons)
- [var kSMRightModifySystemDaemons: String](/documentation/servicemanagement/ksmrightmodifysystemdaemons)
- [Property List Keys](/documentation/servicemanagement/property-list-keys)

### Constants

- [let kSMDomainSystemLaunchd: CFString!](/documentation/servicemanagement/ksmdomainsystemlaunchd)
- [let kSMDomainUserLaunchd: CFString!](/documentation/servicemanagement/ksmdomainuserlaunchd)

## Enablement

- [func SMLoginItemSetEnabled(CFString, Bool) -> Bool](/documentation/servicemanagement/smloginitemsetenabled(_:_:))

## Status

- [SMAppService.Status](/documentation/servicemanagement/smappservice/status-swift.enum)

### Constants

- [case notRegistered](/documentation/servicemanagement/smappservice/status-swift.enum/notregistered)
- [case enabled](/documentation/servicemanagement/smappservice/status-swift.enum/enabled)
- [case requiresApproval](/documentation/servicemanagement/smappservice/status-swift.enum/requiresapproval)
- [case notFound](/documentation/servicemanagement/smappservice/status-swift.enum/notfound)

### Initializers

- [init?(rawValue: Int)](/documentation/servicemanagement/smappservice/status-swift.enum/init(rawvalue:))

## Errors

- [Service Management Errors](/documentation/servicemanagement/service-management-errors)

### Constants

- [var kSMErrorAlreadyRegistered: Int](/documentation/servicemanagement/ksmerroralreadyregistered)
- [var kSMErrorAuthorizationFailure: Int](/documentation/servicemanagement/ksmerrorauthorizationfailure)
- [var kSMErrorInternalFailure: Int](/documentation/servicemanagement/ksmerrorinternalfailure)
- [var kSMErrorInvalidPlist: Int](/documentation/servicemanagement/ksmerrorinvalidplist)
- [var kSMErrorInvalidSignature: Int](/documentation/servicemanagement/ksmerrorinvalidsignature)
- [var kSMErrorJobMustBeEnabled: Int](/documentation/servicemanagement/ksmerrorjobmustbeenabled)
- [var kSMErrorJobNotFound: Int](/documentation/servicemanagement/ksmerrorjobnotfound)
- [var kSMErrorJobPlistNotFound: Int](/documentation/servicemanagement/ksmerrorjobplistnotfound)
- [var kSMErrorLaunchDeniedByUser: Int](/documentation/servicemanagement/ksmerrorlaunchdeniedbyuser)
- [var kSMErrorServiceUnavailable: Int](/documentation/servicemanagement/ksmerrorserviceunavailable)
- [var kSMErrorToolNotValid: Int](/documentation/servicemanagement/ksmerrortoolnotvalid)

## Deprecated

- [Deprecated Symbols](/documentation/servicemanagement/deprecated-symbols)

### Deprecated Constants

- [let kSMErrorDomainFramework: CFString!](/documentation/servicemanagement/ksmerrordomainframework)
- [let kSMErrorDomainIPC: CFString!](/documentation/servicemanagement/ksmerrordomainipc)
- [let kSMErrorDomainLaunchd: CFString!](/documentation/servicemanagement/ksmerrordomainlaunchd)

### Deprecated Functions

- [func SMCopyAllJobDictionaries(CFString!) -> Unmanaged<CFArray>!](/documentation/servicemanagement/smcopyalljobdictionaries(_:))
- [func SMJobCopyDictionary(CFString!, CFString) -> Unmanaged<CFDictionary>!](/documentation/servicemanagement/smjobcopydictionary(_:_:))
- [func SMJobRemove(CFString!, CFString, UnsafeMutableRawPointer!, Bool, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/servicemanagement/smjobremove(_:_:_:_:_:))
- [func SMJobSubmit(CFString!, CFDictionary, UnsafeMutableRawPointer!, UnsafeMutablePointer<Unmanaged<CFError>?>!) -> Bool](/documentation/servicemanagement/smjobsubmit(_:_:_:_:))

## Variables

- [let SMAppServiceErrorDomain: String](/documentation/servicemanagement/smappserviceerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
