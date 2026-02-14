# Accounts Documentation

Source: https://sosumi.ai/documentation/accounts

---
title: Accounts
source: https://developer.apple.com/documentation/accounts
timestamp: 2026-02-13T19:06:35.032Z
---

## Account Management

- [ACAccountStore](/documentation/accounts/acaccountstore)

### Requesting Access

- [func requestAccessToAccounts(with: ACAccountType!, options: [AnyHashable : Any]!, completion: ((Bool, (any Error)?) -> Void)!)](/documentation/accounts/acaccountstore/requestaccesstoaccounts(with:options:completion:))
- [ACAccountStoreRequestAccessCompletionHandler](/documentation/accounts/acaccountstorerequestaccesscompletionhandler)

### Getting Accounts

- [var accounts: NSArray!](/documentation/accounts/acaccountstore/accounts)
- [func account(withIdentifier: String!) -> ACAccount!](/documentation/accounts/acaccountstore/account(withidentifier:))
- [func accounts(with: ACAccountType!) -> [Any]!](/documentation/accounts/acaccountstore/accounts(with:))

### Getting Account Types

- [func accountType(withAccountTypeIdentifier: String!) -> ACAccountType!](/documentation/accounts/acaccountstore/accounttype(withaccounttypeidentifier:))

### Saving Accounts

- [func saveAccount(ACAccount!, withCompletionHandler: ((Bool, (any Error)?) -> Void)!)](/documentation/accounts/acaccountstore/saveaccount(_:withcompletionhandler:))
- [ACAccountStoreSaveCompletionHandler](/documentation/accounts/acaccountstoresavecompletionhandler)

### Renewing Account Credentials

- [func renewCredentials(for: ACAccount!, completion: ((ACAccountCredentialRenewResult, (any Error)?) -> Void)!)](/documentation/accounts/acaccountstore/renewcredentials(for:completion:))
- [ACAccountStoreCredentialRenewalHandler](/documentation/accounts/acaccountstorecredentialrenewalhandler)
- [ACAccountCredentialRenewResult](/documentation/accounts/acaccountcredentialrenewresult)

#### Constants

- [case renewed](/documentation/accounts/acaccountcredentialrenewresult/renewed)
- [case rejected](/documentation/accounts/acaccountcredentialrenewresult/rejected)
- [case failed](/documentation/accounts/acaccountcredentialrenewresult/failed)

#### Initializers

- [init?(rawValue: Int)](/documentation/accounts/acaccountcredentialrenewresult/init(rawvalue:))

### Removing Accounts

- [func removeAccount(ACAccount!, withCompletionHandler: ((Bool, (any Error)?) -> Void)!)](/documentation/accounts/acaccountstore/removeaccount(_:withcompletionhandler:))
- [ACAccountStoreRemoveCompletionHandler](/documentation/accounts/acaccountstoreremovecompletionhandler)
- [ACAccount](/documentation/accounts/acaccount)

### Creating an Account Object

- [init!(accountType: ACAccountType!)](/documentation/accounts/acaccount/init(accounttype:))

### Accessing Properties

- [var accountDescription: String!](/documentation/accounts/acaccount/accountdescription)
- [var accountType: ACAccountType!](/documentation/accounts/acaccount/accounttype)
- [var credential: ACAccountCredential!](/documentation/accounts/acaccount/credential)
- [var identifier: NSString!](/documentation/accounts/acaccount/identifier)
- [var username: String!](/documentation/accounts/acaccount/username)
- [var userFullName: String!](/documentation/accounts/acaccount/userfullname)
- [ACAccountCredential](/documentation/accounts/acaccountcredential)

### Initializing Credentials

- [init!(oAuthToken: String!, tokenSecret: String!)](/documentation/accounts/acaccountcredential/init(oauthtoken:tokensecret:))
- [init!(oAuth2Token: String!, refreshToken: String!, expiryDate: Date!)](/documentation/accounts/acaccountcredential/init(oauth2token:refreshtoken:expirydate:))

### Accessing Credential Properties

- [var oauthToken: String!](/documentation/accounts/acaccountcredential/oauthtoken)

## Account Types

- [ACAccountType](/documentation/accounts/acaccounttype)

### Accessing Properties

- [var accessGranted: Bool](/documentation/accounts/acaccounttype/accessgranted)
- [var accountTypeDescription: String!](/documentation/accounts/acaccounttype/accounttypedescription)
- [var identifier: String!](/documentation/accounts/acaccounttype/identifier)

## Errors

- [ACErrorCode](/documentation/accounts/acerrorcode)

### Errors

- [var ACErrorUnknown: ACErrorCode](/documentation/accounts/acerrorunknown)
- [var ACErrorAccountMissingRequiredProperty: ACErrorCode](/documentation/accounts/acerroraccountmissingrequiredproperty)
- [var ACErrorAccountAuthenticationFailed: ACErrorCode](/documentation/accounts/acerroraccountauthenticationfailed)
- [var ACErrorAccountTypeInvalid: ACErrorCode](/documentation/accounts/acerroraccounttypeinvalid)
- [var ACErrorAccountAlreadyExists: ACErrorCode](/documentation/accounts/acerroraccountalreadyexists)
- [var ACErrorAccountNotFound: ACErrorCode](/documentation/accounts/acerroraccountnotfound)
- [var ACErrorPermissionDenied: ACErrorCode](/documentation/accounts/acerrorpermissiondenied)
- [var ACErrorAccessInfoInvalid: ACErrorCode](/documentation/accounts/acerroraccessinfoinvalid)
- [var ACErrorClientPermissionDenied: ACErrorCode](/documentation/accounts/acerrorclientpermissiondenied)
- [var ACErrorAccessDeniedByProtectionPolicy: ACErrorCode](/documentation/accounts/acerroraccessdeniedbyprotectionpolicy)
- [var ACErrorCredentialNotFound: ACErrorCode](/documentation/accounts/acerrorcredentialnotfound)
- [var ACErrorFetchCredentialFailed: ACErrorCode](/documentation/accounts/acerrorfetchcredentialfailed)
- [var ACErrorStoreCredentialFailed: ACErrorCode](/documentation/accounts/acerrorstorecredentialfailed)
- [var ACErrorRemoveCredentialFailed: ACErrorCode](/documentation/accounts/acerrorremovecredentialfailed)
- [var ACErrorUpdatingNonexistentAccount: ACErrorCode](/documentation/accounts/acerrorupdatingnonexistentaccount)
- [var ACErrorInvalidClientBundleID: ACErrorCode](/documentation/accounts/acerrorinvalidclientbundleid)
- [var ACErrorDeniedByPlugin: ACErrorCode](/documentation/accounts/acerrordeniedbyplugin)
- [var ACErrorCoreDataSaveFailed: ACErrorCode](/documentation/accounts/acerrorcoredatasavefailed)
- [var ACErrorFailedSerializingAccountInfo: ACErrorCode](/documentation/accounts/acerrorfailedserializingaccountinfo)
- [var ACErrorInvalidCommand: ACErrorCode](/documentation/accounts/acerrorinvalidcommand)
- [var ACErrorMissingTransportMessageID: ACErrorCode](/documentation/accounts/acerrormissingtransportmessageid)
- [var ACErrorCredentialItemNotFound: ACErrorCode](/documentation/accounts/acerrorcredentialitemnotfound)
- [var ACErrorCredentialItemNotExpired: ACErrorCode](/documentation/accounts/acerrorcredentialitemnotexpired)

### Initializers

- [init(UInt32)](/documentation/accounts/acerrorcode/init(_:))
- [init(rawValue: UInt32)](/documentation/accounts/acerrorcode/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/accounts/acerrorcode/rawvalue)
- [let ACErrorDomain: String](/documentation/accounts/acerrordomain)

## Deprecated

- [Deprecated Symbols](/documentation/accounts/deprecated-symbols)

### Account Type Strings

- [let ACAccountTypeIdentifierFacebook: String](/documentation/accounts/acaccounttypeidentifierfacebook)
- [let ACAccountTypeIdentifierLinkedIn: String](/documentation/accounts/acaccounttypeidentifierlinkedin)
- [let ACAccountTypeIdentifierSinaWeibo: String](/documentation/accounts/acaccounttypeidentifiersinaweibo)
- [let ACAccountTypeIdentifierTencentWeibo: String](/documentation/accounts/acaccounttypeidentifiertencentweibo)
- [let ACAccountTypeIdentifierTwitter: String](/documentation/accounts/acaccounttypeidentifiertwitter)

### Account Keys

- [let ACFacebookAppIdKey: String](/documentation/accounts/acfacebookappidkey)
- [let ACFacebookAudienceEveryone: String](/documentation/accounts/acfacebookaudienceeveryone)
- [let ACFacebookAudienceFriends: String](/documentation/accounts/acfacebookaudiencefriends)
- [let ACFacebookAudienceKey: String](/documentation/accounts/acfacebookaudiencekey)
- [let ACFacebookAudienceOnlyMe: String](/documentation/accounts/acfacebookaudienceonlyme)
- [let ACFacebookPermissionsKey: String](/documentation/accounts/acfacebookpermissionskey)
- [let ACLinkedInAppIdKey: String](/documentation/accounts/aclinkedinappidkey)
- [let ACLinkedInPermissionsKey: String](/documentation/accounts/aclinkedinpermissionskey)
- [let ACTencentWeiboAppIdKey: String](/documentation/accounts/actencentweiboappidkey)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
