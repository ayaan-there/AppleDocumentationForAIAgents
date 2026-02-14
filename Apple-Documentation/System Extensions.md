# System Extensions Documentation

Source: https://sosumi.ai/documentation/systemextensions

---
title: System Extensions
source: https://developer.apple.com/documentation/systemextensions
timestamp: 2026-02-13T19:02:54.299Z
---

## Essentials

- [Implementing drivers, system extensions, and kexts](/documentation/systemextensions/implementing-drivers-system-extensions-and-kexts)
- [Debugging and testing system extensions](/documentation/driverkit/debugging-and-testing-system-extensions)
- [System Extension Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.system-extension.install)

## Usage descriptions

- [let NSSystemExtensionUsageDescriptionKey: String](/documentation/systemextensions/nssystemextensionusagedescriptionkey)
- [let OSBundleUsageDescriptionKey: String](/documentation/systemextensions/osbundleusagedescriptionkey)

## Extension activation and deactivation

- [Installing System Extensions and Drivers](/documentation/systemextensions/installing-system-extensions-and-drivers)
- [OSSystemExtensionManager](/documentation/systemextensions/ossystemextensionmanager)

### Accessing the Shared Extension Manager

- [class var shared: OSSystemExtensionManager](/documentation/systemextensions/ossystemextensionmanager/shared)

### Submitting Requests

- [func submitRequest(OSSystemExtensionRequest)](/documentation/systemextensions/ossystemextensionmanager/submitrequest(_:))
- [OSSystemExtensionRequest](/documentation/systemextensions/ossystemextensionrequest)

#### Creating Requests

- [class func activationRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/activationrequest(forextensionwithidentifier:queue:))
- [class func deactivationRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/deactivationrequest(forextensionwithidentifier:queue:))

#### Working with a Delegate

- [var delegate: (any OSSystemExtensionRequestDelegate)?](/documentation/systemextensions/ossystemextensionrequest/delegate)
- [OSSystemExtensionRequestDelegate](/documentation/systemextensions/ossystemextensionrequestdelegate)

##### Handling Success and Failure

- [func request(OSSystemExtensionRequest, didFinishWithResult: OSSystemExtensionRequest.Result)](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:didfinishwithresult:))
- [OSSystemExtensionRequest.Result](/documentation/systemextensions/ossystemextensionrequest/result)

###### Results

- [case completed](/documentation/systemextensions/ossystemextensionrequest/result/completed)
- [case willCompleteAfterReboot](/documentation/systemextensions/ossystemextensionrequest/result/willcompleteafterreboot)

###### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionrequest/result/init(rawvalue:))
- [func request(OSSystemExtensionRequest, didFailWithError: any Error)](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:didfailwitherror:))

##### Handling Indeterminate Installs

- [func requestNeedsUserApproval(OSSystemExtensionRequest)](/documentation/systemextensions/ossystemextensionrequestdelegate/requestneedsuserapproval(_:))
- [func request(OSSystemExtensionRequest, actionForReplacingExtension: OSSystemExtensionProperties, withExtension: OSSystemExtensionProperties) -> OSSystemExtensionRequest.ReplacementAction](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:actionforreplacingextension:withextension:))
- [OSSystemExtensionProperties](/documentation/systemextensions/ossystemextensionproperties)

###### Identifying the Extension

- [var bundleIdentifier: String](/documentation/systemextensions/ossystemextensionproperties/bundleidentifier)
- [var bundleVersion: String](/documentation/systemextensions/ossystemextensionproperties/bundleversion)
- [var bundleShortVersion: String](/documentation/systemextensions/ossystemextensionproperties/bundleshortversion)

###### Locating the Extension’s Installed Location

- [var url: URL](/documentation/systemextensions/ossystemextensionproperties/url)

###### Instance Properties

- [var isAwaitingUserApproval: Bool](/documentation/systemextensions/ossystemextensionproperties/isawaitinguserapproval)
- [var isEnabled: Bool](/documentation/systemextensions/ossystemextensionproperties/isenabled)
- [var isUninstalling: Bool](/documentation/systemextensions/ossystemextensionproperties/isuninstalling)
- [OSSystemExtensionRequest.ReplacementAction](/documentation/systemextensions/ossystemextensionrequest/replacementaction)

###### Replacement Actions

- [case cancel](/documentation/systemextensions/ossystemextensionrequest/replacementaction/cancel)
- [case replace](/documentation/systemextensions/ossystemextensionrequest/replacementaction/replace)

###### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionrequest/replacementaction/init(rawvalue:))

##### Instance Methods

- [func request(OSSystemExtensionRequest, foundProperties: [OSSystemExtensionProperties])](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:foundproperties:))

#### Identifying the Target Extension

- [var identifier: String](/documentation/systemextensions/ossystemextensionrequest/identifier)

#### Type Methods

- [class func propertiesRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/propertiesrequest(forextensionwithidentifier:queue:))
- [OSSystemExtensionRequest](/documentation/systemextensions/ossystemextensionrequest)

### Creating Requests

- [class func activationRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/activationrequest(forextensionwithidentifier:queue:))
- [class func deactivationRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/deactivationrequest(forextensionwithidentifier:queue:))

### Working with a Delegate

- [var delegate: (any OSSystemExtensionRequestDelegate)?](/documentation/systemextensions/ossystemextensionrequest/delegate)
- [OSSystemExtensionRequestDelegate](/documentation/systemextensions/ossystemextensionrequestdelegate)

#### Handling Success and Failure

- [func request(OSSystemExtensionRequest, didFinishWithResult: OSSystemExtensionRequest.Result)](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:didfinishwithresult:))
- [OSSystemExtensionRequest.Result](/documentation/systemextensions/ossystemextensionrequest/result)

##### Results

- [case completed](/documentation/systemextensions/ossystemextensionrequest/result/completed)
- [case willCompleteAfterReboot](/documentation/systemextensions/ossystemextensionrequest/result/willcompleteafterreboot)

##### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionrequest/result/init(rawvalue:))
- [func request(OSSystemExtensionRequest, didFailWithError: any Error)](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:didfailwitherror:))

#### Handling Indeterminate Installs

- [func requestNeedsUserApproval(OSSystemExtensionRequest)](/documentation/systemextensions/ossystemextensionrequestdelegate/requestneedsuserapproval(_:))
- [func request(OSSystemExtensionRequest, actionForReplacingExtension: OSSystemExtensionProperties, withExtension: OSSystemExtensionProperties) -> OSSystemExtensionRequest.ReplacementAction](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:actionforreplacingextension:withextension:))
- [OSSystemExtensionProperties](/documentation/systemextensions/ossystemextensionproperties)

##### Identifying the Extension

- [var bundleIdentifier: String](/documentation/systemextensions/ossystemextensionproperties/bundleidentifier)
- [var bundleVersion: String](/documentation/systemextensions/ossystemextensionproperties/bundleversion)
- [var bundleShortVersion: String](/documentation/systemextensions/ossystemextensionproperties/bundleshortversion)

##### Locating the Extension’s Installed Location

- [var url: URL](/documentation/systemextensions/ossystemextensionproperties/url)

##### Instance Properties

- [var isAwaitingUserApproval: Bool](/documentation/systemextensions/ossystemextensionproperties/isawaitinguserapproval)
- [var isEnabled: Bool](/documentation/systemextensions/ossystemextensionproperties/isenabled)
- [var isUninstalling: Bool](/documentation/systemextensions/ossystemextensionproperties/isuninstalling)
- [OSSystemExtensionRequest.ReplacementAction](/documentation/systemextensions/ossystemextensionrequest/replacementaction)

##### Replacement Actions

- [case cancel](/documentation/systemextensions/ossystemextensionrequest/replacementaction/cancel)
- [case replace](/documentation/systemextensions/ossystemextensionrequest/replacementaction/replace)

##### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionrequest/replacementaction/init(rawvalue:))

#### Instance Methods

- [func request(OSSystemExtensionRequest, foundProperties: [OSSystemExtensionProperties])](/documentation/systemextensions/ossystemextensionrequestdelegate/request(_:foundproperties:))

### Identifying the Target Extension

- [var identifier: String](/documentation/systemextensions/ossystemextensionrequest/identifier)

### Type Methods

- [class func propertiesRequest(forExtensionWithIdentifier: String, queue: dispatch_queue_t) -> Self](/documentation/systemextensions/ossystemextensionrequest/propertiesrequest(forextensionwithidentifier:queue:))
- [System Extension Redistributable Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.system-extension.redistributable)

## Errors

- [OSSystemExtensionError](/documentation/systemextensions/ossystemextensionerror)

### Inspecting Error Properties

- [static var errorDomain: String](/documentation/systemextensions/ossystemextensionerror/errordomain)

### Error Codes

- [OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/code)

#### Error Codes

- [case unknown](/documentation/systemextensions/ossystemextensionerror/code/unknown)
- [case missingEntitlement](/documentation/systemextensions/ossystemextensionerror/code/missingentitlement)
- [case unsupportedParentBundleLocation](/documentation/systemextensions/ossystemextensionerror/code/unsupportedparentbundlelocation)
- [case extensionNotFound](/documentation/systemextensions/ossystemextensionerror/code/extensionnotfound)
- [case extensionMissingIdentifier](/documentation/systemextensions/ossystemextensionerror/code/extensionmissingidentifier)
- [case duplicateExtensionIdentifer](/documentation/systemextensions/ossystemextensionerror/code/duplicateextensionidentifer)
- [case unknownExtensionCategory](/documentation/systemextensions/ossystemextensionerror/code/unknownextensioncategory)
- [case codeSignatureInvalid](/documentation/systemextensions/ossystemextensionerror/code/codesignatureinvalid)
- [case validationFailed](/documentation/systemextensions/ossystemextensionerror/code/validationfailed)
- [case forbiddenBySystemPolicy](/documentation/systemextensions/ossystemextensionerror/code/forbiddenbysystempolicy)
- [case requestCanceled](/documentation/systemextensions/ossystemextensionerror/code/requestcanceled)
- [case requestSuperseded](/documentation/systemextensions/ossystemextensionerror/code/requestsuperseded)
- [case authorizationRequired](/documentation/systemextensions/ossystemextensionerror/code/authorizationrequired)

#### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionerror/code/init(rawvalue:))
- [static var unknown: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/unknown)
- [static var missingEntitlement: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/missingentitlement)
- [static var unsupportedParentBundleLocation: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/unsupportedparentbundlelocation)
- [static var extensionNotFound: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/extensionnotfound)
- [static var extensionMissingIdentifier: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/extensionmissingidentifier)
- [static var duplicateExtensionIdentifer: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/duplicateextensionidentifer)
- [static var unknownExtensionCategory: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/unknownextensioncategory)
- [static var codeSignatureInvalid: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/codesignatureinvalid)
- [static var validationFailed: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/validationfailed)
- [static var forbiddenBySystemPolicy: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/forbiddenbysystempolicy)
- [static var requestCanceled: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/requestcanceled)
- [static var requestSuperseded: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/requestsuperseded)
- [static var authorizationRequired: OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/authorizationrequired)
- [OSSystemExtensionError.Code](/documentation/systemextensions/ossystemextensionerror/code)

### Error Codes

- [case unknown](/documentation/systemextensions/ossystemextensionerror/code/unknown)
- [case missingEntitlement](/documentation/systemextensions/ossystemextensionerror/code/missingentitlement)
- [case unsupportedParentBundleLocation](/documentation/systemextensions/ossystemextensionerror/code/unsupportedparentbundlelocation)
- [case extensionNotFound](/documentation/systemextensions/ossystemextensionerror/code/extensionnotfound)
- [case extensionMissingIdentifier](/documentation/systemextensions/ossystemextensionerror/code/extensionmissingidentifier)
- [case duplicateExtensionIdentifer](/documentation/systemextensions/ossystemextensionerror/code/duplicateextensionidentifer)
- [case unknownExtensionCategory](/documentation/systemextensions/ossystemextensionerror/code/unknownextensioncategory)
- [case codeSignatureInvalid](/documentation/systemextensions/ossystemextensionerror/code/codesignatureinvalid)
- [case validationFailed](/documentation/systemextensions/ossystemextensionerror/code/validationfailed)
- [case forbiddenBySystemPolicy](/documentation/systemextensions/ossystemextensionerror/code/forbiddenbysystempolicy)
- [case requestCanceled](/documentation/systemextensions/ossystemextensionerror/code/requestcanceled)
- [case requestSuperseded](/documentation/systemextensions/ossystemextensionerror/code/requestsuperseded)
- [case authorizationRequired](/documentation/systemextensions/ossystemextensionerror/code/authorizationrequired)

### Initializers

- [init?(rawValue: Int)](/documentation/systemextensions/ossystemextensionerror/code/init(rawvalue:))
- [let OSSystemExtensionErrorDomain: String](/documentation/systemextensions/ossystemextensionerrordomain)

## Reference

- [SystemExtensions Constants](/documentation/systemextensions/systemextensions-constants)

### Constants

- [let OSRelatedKernelExtensionKey: String](/documentation/systemextensions/osrelatedkernelextensionkey)

## Classes

- [OSSystemExtensionInfo](/documentation/systemextensions/ossystemextensioninfo)

### Instance Properties

- [var bundleIdentifier: String](/documentation/systemextensions/ossystemextensioninfo/bundleidentifier)
- [var bundleShortVersion: String](/documentation/systemextensions/ossystemextensioninfo/bundleshortversion)
- [var bundleVersion: String](/documentation/systemextensions/ossystemextensioninfo/bundleversion)
- [OSSystemExtensionsWorkspace](/documentation/systemextensions/ossystemextensionsworkspace)

### Instance Methods

- [func addObserver(any OSSystemExtensionsWorkspaceObserver) throws](/documentation/systemextensions/ossystemextensionsworkspace/addobserver(_:))
- [func removeObserver(any OSSystemExtensionsWorkspaceObserver)](/documentation/systemextensions/ossystemextensionsworkspace/removeobserver(_:))
- [func systemExtensions(forApplicationWithBundleID: String) throws -> Set<OSSystemExtensionProperties>](/documentation/systemextensions/ossystemextensionsworkspace/systemextensions(forapplicationwithbundleid:))

### Type Properties

- [class var shared: OSSystemExtensionsWorkspace](/documentation/systemextensions/ossystemextensionsworkspace/shared)

## Protocols

- [OSSystemExtensionsWorkspaceObserver](/documentation/systemextensions/ossystemextensionsworkspaceobserver)

### Instance Methods

- [func systemExtensionWillBecomeDisabled(OSSystemExtensionInfo)](/documentation/systemextensions/ossystemextensionsworkspaceobserver/systemextensionwillbecomedisabled(_:))
- [func systemExtensionWillBecomeEnabled(OSSystemExtensionInfo)](/documentation/systemextensions/ossystemextensionsworkspaceobserver/systemextensionwillbecomeenabled(_:))
- [func systemExtensionWillBecomeInactive(OSSystemExtensionInfo)](/documentation/systemextensions/ossystemextensionsworkspaceobserver/systemextensionwillbecomeinactive(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
