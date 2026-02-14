# Video Subscriber Account Documentation

Source: https://sosumi.ai/documentation/videosubscriberaccount

---
title: Video Subscriber Account
source: https://developer.apple.com/documentation/videosubscriberaccount
timestamp: 2026-02-13T19:03:36.964Z
---

## Essentials

- [Video Subscriber Account updates](/documentation/updates/videosubscriberaccount)

## TV provider authentication

- [VSAccountManager](/documentation/videosubscriberaccount/vsaccountmanager)

### Responding to account manager requests

- [var delegate: (any VSAccountManagerDelegate)?](/documentation/videosubscriberaccount/vsaccountmanager/delegate)
- [VSAccountManagerDelegate](/documentation/videosubscriberaccount/vsaccountmanagerdelegate)

#### Displaying Authentication Views

- [func accountManager(VSAccountManager, present: UIViewController)](/documentation/videosubscriberaccount/vsaccountmanagerdelegate/accountmanager(_:present:))

#### Dismissing Authentication Views

- [func accountManager(VSAccountManager, dismiss: UIViewController)](/documentation/videosubscriberaccount/vsaccountmanagerdelegate/accountmanager(_:dismiss:))

#### Supporting Degradation Scenarios

- [func accountManager(VSAccountManager, shouldAuthenticateAccountProviderWithIdentifier: String) -> Bool](/documentation/videosubscriberaccount/vsaccountmanagerdelegate/accountmanager(_:shouldauthenticateaccountproviderwithidentifier:))

### Checking access status

- [func checkAccessStatus(options: [VSCheckAccessOption : Any], completionHandler: (VSAccountAccessStatus, (any Error)?) -> Void)](/documentation/videosubscriberaccount/vsaccountmanager/checkaccessstatus(options:completionhandler:))
- [VSCheckAccessOption](/documentation/videosubscriberaccount/vscheckaccessoption)

#### Options

- [static let prompt: VSCheckAccessOption](/documentation/videosubscriberaccount/vscheckaccessoption/prompt)

#### Creating check access options

- [init(rawValue: String)](/documentation/videosubscriberaccount/vscheckaccessoption/init(rawvalue:))
- [VSAccountAccessStatus](/documentation/videosubscriberaccount/vsaccountaccessstatus)

#### Statuses

- [case denied](/documentation/videosubscriberaccount/vsaccountaccessstatus/denied)
- [case granted](/documentation/videosubscriberaccount/vsaccountaccessstatus/granted)
- [case notDetermined](/documentation/videosubscriberaccount/vsaccountaccessstatus/notdetermined)
- [case restricted](/documentation/videosubscriberaccount/vsaccountaccessstatus/restricted)

#### Initializers

- [init?(rawValue: Int)](/documentation/videosubscriberaccount/vsaccountaccessstatus/init(rawvalue:))

### Enqueuing requests

- [func enqueue(VSAccountMetadataRequest, completionHandler: (VSAccountMetadata?, (any Error)?) -> Void) -> VSAccountManagerResult](/documentation/videosubscriberaccount/vsaccountmanager/enqueue(_:completionhandler:))
- [VSAccountMetadataRequest](/documentation/videosubscriberaccount/vsaccountmetadatarequest)

#### Requesting TV Provider Info

- [var includeAccountProviderIdentifier: Bool](/documentation/videosubscriberaccount/vsaccountmetadatarequest/includeaccountprovideridentifier)
- [var includeAuthenticationExpirationDate: Bool](/documentation/videosubscriberaccount/vsaccountmetadatarequest/includeauthenticationexpirationdate)

#### Requesting App-Level Authentication

- [var attributeNames: [String]](/documentation/videosubscriberaccount/vsaccountmetadatarequest/attributenames)
- [var channelIdentifier: String?](/documentation/videosubscriberaccount/vsaccountmetadatarequest/channelidentifier)
- [var supportedAccountProviderIdentifiers: [String]](/documentation/videosubscriberaccount/vsaccountmetadatarequest/supportedaccountprovideridentifiers)
- [var supportedAuthenticationSchemes: [VSAccountProviderAuthenticationScheme]](/documentation/videosubscriberaccount/vsaccountmetadatarequest/supportedauthenticationschemes)
- [var verificationToken: String?](/documentation/videosubscriberaccount/vsaccountmetadatarequest/verificationtoken)

#### Specifying Additional Options

- [var isInterruptionAllowed: Bool](/documentation/videosubscriberaccount/vsaccountmetadatarequest/isinterruptionallowed)
- [var featuredAccountProviderIdentifiers: [String]](/documentation/videosubscriberaccount/vsaccountmetadatarequest/featuredaccountprovideridentifiers)
- [var forceAuthentication: Bool](/documentation/videosubscriberaccount/vsaccountmetadatarequest/forceauthentication)
- [var localizedVideoTitle: String?](/documentation/videosubscriberaccount/vsaccountmetadatarequest/localizedvideotitle)
- [var applicationAccountProviders: [VSAccountApplicationProvider]?](/documentation/videosubscriberaccount/vsaccountmetadatarequest/applicationaccountproviders)

#### Supporting Authentication Share

- [var accountProviderAuthenticationToken: String?](/documentation/videosubscriberaccount/vsaccountmetadatarequest/accountproviderauthenticationtoken)
- [VSAccountMetadata](/documentation/videosubscriberaccount/vsaccountmetadata)

#### Getting TV Provider Info

- [var accountProviderIdentifier: String?](/documentation/videosubscriberaccount/vsaccountmetadata/accountprovideridentifier)
- [var authenticationExpirationDate: Date?](/documentation/videosubscriberaccount/vsaccountmetadata/authenticationexpirationdate)

#### Getting App Authentication Info

- [var accountProviderResponse: VSAccountProviderResponse?](/documentation/videosubscriberaccount/vsaccountmetadata/accountproviderresponse)
- [var samlAttributeQueryResponse: String?](/documentation/videosubscriberaccount/vsaccountmetadata/samlattributequeryresponse)
- [var verificationData: Data?](/documentation/videosubscriberaccount/vsaccountmetadata/verificationdata)
- [VSAccountManagerResult](/documentation/videosubscriberaccount/vsaccountmanagerresult)

#### Cancelling a Request

- [func cancel()](/documentation/videosubscriberaccount/vsaccountmanagerresult/cancel())
- [VSAccountProviderResponse](/documentation/videosubscriberaccount/vsaccountproviderresponse)

#### Getting Response Info

- [var authenticationScheme: VSAccountProviderAuthenticationScheme](/documentation/videosubscriberaccount/vsaccountproviderresponse/authenticationscheme)
- [var body: String?](/documentation/videosubscriberaccount/vsaccountproviderresponse/body)
- [var status: String?](/documentation/videosubscriberaccount/vsaccountproviderresponse/status)
- [VSAccountProviderAuthenticationScheme](/documentation/videosubscriberaccount/vsaccountproviderauthenticationscheme)

#### Creating an Authentication Scheme

- [init(String)](/documentation/videosubscriberaccount/vsaccountproviderauthenticationscheme/init(_:))
- [init(rawValue: String)](/documentation/videosubscriberaccount/vsaccountproviderauthenticationscheme/init(rawvalue:))

#### Authentication Scheme Types

- [static let saml: VSAccountProviderAuthenticationScheme](/documentation/videosubscriberaccount/vsaccountproviderauthenticationscheme/saml)
- [static let api: VSAccountProviderAuthenticationScheme](/documentation/videosubscriberaccount/vsaccountproviderauthenticationscheme/api)

### Deep linking to TV provider settings

- [let VSOpenTVProviderSettingsURLString: String](/documentation/videosubscriberaccount/vsopentvprovidersettingsurlstring)

## TV app integration

- [VSAppleSubscription](/documentation/videosubscriberaccount/vsapplesubscription-swift.struct)

### Creating an Apple subscription

- [init(customerID: String, productCodes: [String])](/documentation/videosubscriberaccount/vsapplesubscription-swift.struct/init(customerid:productcodes:))

### Identifying a subscription

- [var customerID: String](/documentation/videosubscriberaccount/vsapplesubscription-swift.struct/customerid)
- [var productCodes: [String]](/documentation/videosubscriberaccount/vsapplesubscription-swift.struct/productcodes)
- [VSSubscriptionRegistrationCenter](/documentation/videosubscriberaccount/vssubscriptionregistrationcenter)

### Setting the Current Subscription

- [func setCurrentSubscription(VSSubscription?)](/documentation/videosubscriberaccount/vssubscriptionregistrationcenter/setcurrentsubscription(_:))

### Getting the Default Registration Center

- [class func `default`() -> VSSubscriptionRegistrationCenter](/documentation/videosubscriberaccount/vssubscriptionregistrationcenter/default())
- [VSAccountApplicationProvider](/documentation/videosubscriberaccount/vsaccountapplicationprovider)

### Creating an application provider

- [init(localizedDisplayName: String, identifier: String)](/documentation/videosubscriberaccount/vsaccountapplicationprovider/init(localizeddisplayname:identifier:))

### Application provider details

- [var identifier: String](/documentation/videosubscriberaccount/vsaccountapplicationprovider/identifier)
- [var localizedDisplayName: String](/documentation/videosubscriberaccount/vsaccountapplicationprovider/localizeddisplayname)

## User account management

- [Signing people in to their media accounts automatically](/documentation/videosubscriberaccount/signing-people-in-to-media-apps-automatically)
- [VSUserAccountManager](/documentation/videosubscriberaccount/vsuseraccountmanager)

### Getting the account manager

- [class var shared: VSUserAccountManager](/documentation/videosubscriberaccount/vsuseraccountmanager/shared)

### Getting user accounts

- [func userAccounts(options: VSUserAccountManager.QueryOptions) async throws -> [VSUserAccount]](/documentation/videosubscriberaccount/vsuseraccountmanager/useraccounts(options:))
- [VSUserAccountManager.QueryOptions](/documentation/videosubscriberaccount/vsuseraccountmanager/queryoptions)

#### Query options

- [static var allDevices: VSUserAccountManager.QueryOptions](/documentation/videosubscriberaccount/vsuseraccountmanager/queryoptions/alldevices)

#### Initializing query options

- [init(rawValue: Int)](/documentation/videosubscriberaccount/vsuseraccountmanager/queryoptions/init(rawvalue:))

### Updating a user account

- [func update(VSUserAccount) async throws](/documentation/videosubscriberaccount/vsuseraccountmanager/update(_:))

### Signing people in automatically

- [VSUserAccountManager.AutoSignInToken](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintoken-swift.struct)

#### Defining the token value

- [var value: String?](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintoken-swift.struct/value)

#### Determining status

- [var authorization: VSUserAccountManager.AutoSignInAuthorization](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintoken-swift.struct/authorization)
- [VSUserAccountManager.AutoSignInTokenUpdateContext](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintokenupdatecontext)

#### Determining status

- [var authorization: VSUserAccountManager.AutoSignInAuthorization](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintokenupdatecontext/authorization)
- [VSUserAccountManager.AutoSignInAuthorization](/documentation/videosubscriberaccount/vsuseraccountmanager/autosigninauthorization)

#### Possible states

- [case notDetermined](/documentation/videosubscriberaccount/vsuseraccountmanager/autosigninauthorization/notdetermined)
- [case granted](/documentation/videosubscriberaccount/vsuseraccountmanager/autosigninauthorization/granted)
- [case denied](/documentation/videosubscriberaccount/vsuseraccountmanager/autosigninauthorization/denied)
- [var autoSignInToken: VSUserAccountManager.AutoSignInToken](/documentation/videosubscriberaccount/vsuseraccountmanager/autosignintoken-swift.property)
- [func deleteAutoSignInToken() async throws](/documentation/videosubscriberaccount/vsuseraccountmanager/deleteautosignintoken())
- [func requestAutoSignInAuthorization() async throws -> VSUserAccountManager.AutoSignInTokenUpdateContext](/documentation/videosubscriberaccount/vsuseraccountmanager/requestautosigninauthorization())
- [func updateAutoSignInToken(String, updateContext: VSUserAccountManager.AutoSignInTokenUpdateContext) async throws](/documentation/videosubscriberaccount/vsuseraccountmanager/updateautosignintoken(_:updatecontext:))
- [VSUserAccount](/documentation/videosubscriberaccount/vsuseraccount-swift.struct)

### Creating user accounts

- [init(accountType: VSUserAccount.AccountType, updateURL: URL?)](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/init(accounttype:updateurl:))
- [VSUserAccount.AccountType](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/accounttype-swift.enum)

#### Account types

- [case free](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/accounttype-swift.enum/free)
- [case paid](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/accounttype-swift.enum/paid)

### User account information

- [var accountProviderIdentifier: String?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/accountprovideridentifier)
- [var accountType: VSUserAccount.AccountType](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/accounttype-swift.property)
- [var authenticationData: String?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/authenticationdata)
- [var billingIdentifier: String?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/billingidentifier)
- [var deviceCategory: VSUserAccount.OriginatingDeviceCategory](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/devicecategory)
- [VSUserAccount.OriginatingDeviceCategory](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/originatingdevicecategory)

#### Originating device categories

- [case mobile](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/originatingdevicecategory/mobile)
- [case other](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/originatingdevicecategory/other)
- [var identifier: String?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/identifier)
- [var isFromCurrentDevice: Bool](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/isfromcurrentdevice)
- [var isSignedOut: Bool](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/issignedout)
- [var requiresSystemTrust: Bool](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/requiressystemtrust)
- [var subscriptionBillingCycleEndDate: Date?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/subscriptionbillingcycleenddate)
- [var tierIdentifiers: [String]?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/tieridentifiers)
- [var updateURL: URL?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/updateurl)

### Instance Properties

- [var appleSubscription: VSAppleSubscription?](/documentation/videosubscriberaccount/vsuseraccount-swift.struct/applesubscription)

## Errors

- [let VSErrorDomain: String](/documentation/videosubscriberaccount/vserrordomain)
- [let VSErrorInfoKeySAMLResponse: String](/documentation/videosubscriberaccount/vserrorinfokeysamlresponse)
- [let VSErrorInfoKeySAMLResponseStatus: String](/documentation/videosubscriberaccount/vserrorinfokeysamlresponsestatus)
- [let VSErrorInfoKeyAccountProviderResponse: String](/documentation/videosubscriberaccount/vserrorinfokeyaccountproviderresponse)
- [let VSErrorInfoKeyUnsupportedProviderIdentifier: String](/documentation/videosubscriberaccount/vserrorinfokeyunsupportedprovideridentifier)
- [VSError](/documentation/videosubscriberaccount/vserror)

### Error information

- [static var errorDomain: String](/documentation/videosubscriberaccount/vserror/errordomain)

### Error codes

- [static var accessNotGranted: VSError.Code](/documentation/videosubscriberaccount/vserror/accessnotgranted)
- [static var invalidVerificationToken: VSError.Code](/documentation/videosubscriberaccount/vserror/invalidverificationtoken)
- [static var providerRejected: VSError.Code](/documentation/videosubscriberaccount/vserror/providerrejected)
- [static var rejected: VSError.Code](/documentation/videosubscriberaccount/vserror/rejected)
- [static var serviceTemporarilyUnavailable: VSError.Code](/documentation/videosubscriberaccount/vserror/servicetemporarilyunavailable)
- [static var unsupported: VSError.Code](/documentation/videosubscriberaccount/vserror/unsupported)
- [static var unsupportedProvider: VSError.Code](/documentation/videosubscriberaccount/vserror/unsupportedprovider)
- [static var userCancelled: VSError.Code](/documentation/videosubscriberaccount/vserror/usercancelled)
- [VSError.Code](/documentation/videosubscriberaccount/vserror/code)

#### Error Codes

- [case accessNotGranted](/documentation/videosubscriberaccount/vserror/code/accessnotgranted)
- [case invalidVerificationToken](/documentation/videosubscriberaccount/vserror/code/invalidverificationtoken)
- [case providerRejected](/documentation/videosubscriberaccount/vserror/code/providerrejected)
- [case rejected](/documentation/videosubscriberaccount/vserror/code/rejected)
- [case serviceTemporarilyUnavailable](/documentation/videosubscriberaccount/vserror/code/servicetemporarilyunavailable)
- [case unsupported](/documentation/videosubscriberaccount/vserror/code/unsupported)
- [case unsupportedProvider](/documentation/videosubscriberaccount/vserror/code/unsupportedprovider)
- [case userCancelled](/documentation/videosubscriberaccount/vserror/code/usercancelled)

#### Initializers

- [init?(rawValue: Int)](/documentation/videosubscriberaccount/vserror/code/init(rawvalue:))
- [VSError.Code](/documentation/videosubscriberaccount/vserror/code)

### Error Codes

- [case accessNotGranted](/documentation/videosubscriberaccount/vserror/code/accessnotgranted)
- [case invalidVerificationToken](/documentation/videosubscriberaccount/vserror/code/invalidverificationtoken)
- [case providerRejected](/documentation/videosubscriberaccount/vserror/code/providerrejected)
- [case rejected](/documentation/videosubscriberaccount/vserror/code/rejected)
- [case serviceTemporarilyUnavailable](/documentation/videosubscriberaccount/vserror/code/servicetemporarilyunavailable)
- [case unsupported](/documentation/videosubscriberaccount/vserror/code/unsupported)
- [case unsupportedProvider](/documentation/videosubscriberaccount/vserror/code/unsupportedprovider)
- [case userCancelled](/documentation/videosubscriberaccount/vserror/code/usercancelled)

### Initializers

- [init?(rawValue: Int)](/documentation/videosubscriberaccount/vserror/code/init(rawvalue:))

## Deprecated

- [VSSubscription](/documentation/videosubscriberaccount/vssubscription)

### Setting Subscription Details

- [var accessLevel: VSSubscriptionAccessLevel](/documentation/videosubscriberaccount/vssubscription/accesslevel)
- [VSSubscriptionAccessLevel](/documentation/videosubscriberaccount/vssubscriptionaccesslevel)

#### Subscription Tiers

- [case freeWithAccount](/documentation/videosubscriberaccount/vssubscriptionaccesslevel/freewithaccount)
- [case paid](/documentation/videosubscriberaccount/vssubscriptionaccesslevel/paid)
- [case unknown](/documentation/videosubscriberaccount/vssubscriptionaccesslevel/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/videosubscriberaccount/vssubscriptionaccesslevel/init(rawvalue:))
- [var billingIdentifier: String?](/documentation/videosubscriberaccount/vssubscription/billingidentifier)
- [var expirationDate: Date!](/documentation/videosubscriberaccount/vssubscription/expirationdate)
- [var tierIdentifiers: [String]!](/documentation/videosubscriberaccount/vssubscription/tieridentifiers)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
