# Security Documentation

Source: https://sosumi.ai/documentation/security

---
title: Security
source: https://developer.apple.com/documentation/security
timestamp: 2026-02-13T19:01:51.344Z
---

## Essentials

- [Security updates](/documentation/updates/security)

## Authorization and authentication

- [Password AutoFill](/documentation/security/password-autofill)

### Essentials

- [About the Password AutoFill workflow](/documentation/security/about-the-password-autofill-workflow)
- [Supporting associated domains](/documentation/xcode/supporting-associated-domains)
- [object applinks](/documentation/bundleresources/applinks)

### Text input views

- [Enabling Password AutoFill on a text input view](/documentation/security/enabling-password-autofill-on-a-text-input-view)
- [var textContentType: UITextContentType!](/documentation/uikit/uitextinputtraits/textcontenttype)
- [static let username: UITextContentType](/documentation/uikit/uitextcontenttype/username)
- [static let password: UITextContentType](/documentation/uikit/uitextcontenttype/password)
- [static let newPassword: UITextContentType](/documentation/uikit/uitextcontenttype/newpassword)
- [static let oneTimeCode: UITextContentType](/documentation/uikit/uitextcontenttype/onetimecode)

### Text input elements

- [Enabling Password AutoFill on an HTML input element](/documentation/security/enabling-password-autofill-on-an-html-input-element)

### Password rules

- [Customizing Password AutoFill rules](/documentation/security/customizing-password-autofill-rules)
- [var passwordRules: UITextInputPasswordRules?](/documentation/uikit/uitextinputtraits/passwordrules)
- [UITextInputPasswordRules](/documentation/uikit/uitextinputpasswordrules)
- [Shared Web Credentials](/documentation/security/shared-web-credentials)

### First Steps

- [Supporting associated domains](/documentation/xcode/supporting-associated-domains)
- [Managing Shared Credentials](/documentation/security/managing-shared-credentials)

### Password Sharing

- [func SecAddSharedWebCredential(CFString, CFString, CFString?, (CFError?) -> Void)](/documentation/security/secaddsharedwebcredential(_:_:_:_:))
- [func SecRequestSharedWebCredential(CFString?, CFString?, (CFArray?, CFError?) -> Void)](/documentation/security/secrequestsharedwebcredential(_:_:_:))
- [func SecCreateSharedWebCredentialPassword() -> CFString?](/documentation/security/seccreatesharedwebcredentialpassword())
- [let kSecSharedPassword: CFString](/documentation/security/ksecsharedpassword)
- [Authorization Services](/documentation/security/authorization-services)

### Authorization References

- [func AuthorizationCreate(UnsafePointer<AuthorizationRights>?, UnsafePointer<AuthorizationEnvironment>?, AuthorizationFlags, UnsafeMutablePointer<AuthorizationRef?>?) -> OSStatus](/documentation/security/authorizationcreate(_:_:_:_:))
- [func AuthorizationFree(AuthorizationRef, AuthorizationFlags) -> OSStatus](/documentation/security/authorizationfree(_:_:))
- [AuthorizationFlags](/documentation/security/authorizationflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/authorizationflags/init(rawvalue:))

#### Type Properties

- [static var interactionAllowed: AuthorizationFlags](/documentation/security/authorizationflags/interactionallowed)
- [static var extendRights: AuthorizationFlags](/documentation/security/authorizationflags/extendrights)
- [static var partialRights: AuthorizationFlags](/documentation/security/authorizationflags/partialrights)
- [static var destroyRights: AuthorizationFlags](/documentation/security/authorizationflags/destroyrights)
- [static var preAuthorize: AuthorizationFlags](/documentation/security/authorizationflags/preauthorize)
- [static var noData: AuthorizationFlags](/documentation/security/authorizationflags/nodata)
- [static var skipInternalAuth: AuthorizationFlags](/documentation/security/authorizationflags/skipinternalauth)
- [AuthorizationRef](/documentation/security/authorizationref)

### Authorization Items

- [AuthorizationItem](/documentation/security/authorizationitem)

#### Initializers

- [init(name: AuthorizationString, valueLength: Int, value: UnsafeMutableRawPointer?, flags: UInt32)](/documentation/security/authorizationitem/init(name:valuelength:value:flags:))

#### Instance Properties

- [var flags: UInt32](/documentation/security/authorizationitem/flags)
- [var name: AuthorizationString](/documentation/security/authorizationitem/name)
- [var value: UnsafeMutableRawPointer?](/documentation/security/authorizationitem/value)
- [var valueLength: Int](/documentation/security/authorizationitem/valuelength)
- [AuthorizationItemSet](/documentation/security/authorizationitemset)

#### Initializers

- [init()](/documentation/security/authorizationitemset/init())
- [init(count: UInt32, items: UnsafeMutablePointer<AuthorizationItem>?)](/documentation/security/authorizationitemset/init(count:items:))

#### Instance Properties

- [var count: UInt32](/documentation/security/authorizationitemset/count)
- [var items: UnsafeMutablePointer<AuthorizationItem>?](/documentation/security/authorizationitemset/items)
- [AuthorizationRights](/documentation/security/authorizationrights)
- [AuthorizationEnvironment](/documentation/security/authorizationenvironment)
- [Authorization Name Tags](/documentation/security/authorization-name-tags)

#### Constants

- [var kAuthorizationEnvironmentUsername: String](/documentation/security/kauthorizationenvironmentusername)
- [var kAuthorizationEnvironmentPassword: String](/documentation/security/kauthorizationenvironmentpassword)
- [var kAuthorizationEnvironmentShared: String](/documentation/security/kauthorizationenvironmentshared)
- [var kAuthorizationRightExecute: String](/documentation/security/kauthorizationrightexecute)
- [var kAuthorizationEnvironmentPrompt: String](/documentation/security/kauthorizationenvironmentprompt)
- [var kAuthorizationEnvironmentIcon: String](/documentation/security/kauthorizationenvironmenticon)
- [var kAuthorizationPamResult: String](/documentation/security/kauthorizationpamresult)
- [func AuthorizationFreeItemSet(UnsafeMutablePointer<AuthorizationItemSet>) -> OSStatus](/documentation/security/authorizationfreeitemset(_:))

### Rights and Credentials

- [func AuthorizationCopyInfo(AuthorizationRef, AuthorizationString?, UnsafeMutablePointer<UnsafeMutablePointer<AuthorizationItemSet>?>) -> OSStatus](/documentation/security/authorizationcopyinfo(_:_:_:))
- [func AuthorizationCopyRights(AuthorizationRef, UnsafePointer<AuthorizationRights>, UnsafePointer<AuthorizationEnvironment>?, AuthorizationFlags, UnsafeMutablePointer<UnsafeMutablePointer<AuthorizationRights>?>?) -> OSStatus](/documentation/security/authorizationcopyrights(_:_:_:_:_:))
- [func AuthorizationCopyRightsAsync(AuthorizationRef, UnsafePointer<AuthorizationRights>, UnsafePointer<AuthorizationEnvironment>?, AuthorizationFlags, AuthorizationAsyncCallback)](/documentation/security/authorizationcopyrightsasync(_:_:_:_:_:))
- [AuthorizationAsyncCallback](/documentation/security/authorizationasynccallback)
- [AuthorizationString](/documentation/security/authorizationstring)
- [Authorization Rights Flags](/documentation/security/authorization-rights-flags)

#### Constants

- [var kAuthorizationFlagCanNotPreAuthorize: Int](/documentation/security/kauthorizationflagcannotpreauthorize)

### Import and Export

- [func AuthorizationMakeExternalForm(AuthorizationRef, UnsafeMutablePointer<AuthorizationExternalForm>) -> OSStatus](/documentation/security/authorizationmakeexternalform(_:_:))
- [func AuthorizationCreateFromExternalForm(UnsafePointer<AuthorizationExternalForm>, UnsafeMutablePointer<AuthorizationRef?>) -> OSStatus](/documentation/security/authorizationcreatefromexternalform(_:_:))
- [AuthorizationExternalForm](/documentation/security/authorizationexternalform)

#### Initializers

- [init()](/documentation/security/authorizationexternalform/init())
- [init(bytes: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar))](/documentation/security/authorizationexternalform/init(bytes:))

#### Instance Properties

- [var bytes: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/security/authorizationexternalform/bytes)
- [var kAuthorizationExternalFormLength: Int32](/documentation/security/kauthorizationexternalformlength)

### The Policy Database

- [func AuthorizationRightGet(UnsafePointer<CChar>, UnsafeMutablePointer<CFDictionary?>?) -> OSStatus](/documentation/security/authorizationrightget(_:_:))
- [func AuthorizationRightSet(AuthorizationRef, UnsafePointer<CChar>, CFTypeRef, CFString?, CFBundle?, CFString?) -> OSStatus](/documentation/security/authorizationrightset(_:_:_:_:_:_:))
- [func AuthorizationRightRemove(AuthorizationRef, UnsafePointer<CChar>) -> OSStatus](/documentation/security/authorizationrightremove(_:_:))
- [Policy Database Constants](/documentation/security/policy-database-constants)

#### Constants

- [var kAuthorizationRightRule: String](/documentation/security/kauthorizationrightrule)
- [var kAuthorizationRuleIsAdmin: String](/documentation/security/kauthorizationruleisadmin)
- [var kAuthorizationRuleAuthenticateAsAdmin: String](/documentation/security/kauthorizationruleauthenticateasadmin)
- [var kAuthorizationRuleAuthenticateAsSessionUser: String](/documentation/security/kauthorizationruleauthenticateassessionuser)
- [var kAuthorizationRuleClassAllow: String](/documentation/security/kauthorizationruleclassallow)
- [var kAuthorizationRuleClassDeny: String](/documentation/security/kauthorizationruleclassdeny)
- [var kAuthorizationComment: String](/documentation/security/kauthorizationcomment)

### Result Codes

- [Authorization Services Result Codes](/documentation/security/authorization-services-result-codes)

#### Codes

- [var errAuthorizationSuccess: OSStatus](/documentation/security/errauthorizationsuccess)
- [var errAuthorizationInvalidSet: OSStatus](/documentation/security/errauthorizationinvalidset)
- [var errAuthorizationInvalidRef: OSStatus](/documentation/security/errauthorizationinvalidref)
- [var errAuthorizationInvalidTag: OSStatus](/documentation/security/errauthorizationinvalidtag)
- [var errAuthorizationInvalidPointer: OSStatus](/documentation/security/errauthorizationinvalidpointer)
- [var errAuthorizationDenied: OSStatus](/documentation/security/errauthorizationdenied)
- [var errAuthorizationCanceled: OSStatus](/documentation/security/errauthorizationcanceled)
- [var errAuthorizationInteractionNotAllowed: OSStatus](/documentation/security/errauthorizationinteractionnotallowed)
- [var errAuthorizationInternal: OSStatus](/documentation/security/errauthorizationinternal)
- [var errAuthorizationExternalizeNotAllowed: OSStatus](/documentation/security/errauthorizationexternalizenotallowed)
- [var errAuthorizationInternalizeNotAllowed: OSStatus](/documentation/security/errauthorizationinternalizenotallowed)
- [var errAuthorizationInvalidFlags: OSStatus](/documentation/security/errauthorizationinvalidflags)
- [var errAuthorizationToolExecuteFailure: OSStatus](/documentation/security/errauthorizationtoolexecutefailure)
- [var errAuthorizationToolEnvironmentError: OSStatus](/documentation/security/errauthorizationtoolenvironmenterror)
- [var errAuthorizationBadAddress: OSStatus](/documentation/security/errauthorizationbadaddress)
- [Authorization Plug-ins](/documentation/security/authorization-plug-ins)

### First Steps

- [Extending authorization services with plug-ins](/documentation/security/extending-authorization-services-with-plug-ins)

### Creating a Plug-in

- [AuthorizationCallbacks Version](/documentation/security/authorizationcallbacks-version)
- [AuthorizationPluginInterface Version](/documentation/security/authorizationplugininterface-version)
- [Sessions](/documentation/security/sessions)

### Creating a Session

- [func SessionCreate(SessionCreationFlags, SessionAttributeBits) -> OSStatus](/documentation/security/sessioncreate(_:_:))
- [SessionCreationFlags](/documentation/security/sessioncreationflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/sessioncreationflags/init(rawvalue:))

#### Flags

- [static var sessionKeepCurrentBootstrap: SessionCreationFlags](/documentation/security/sessioncreationflags/sessionkeepcurrentbootstrap)
- [SessionAttributeBits](/documentation/security/sessionattributebits)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/sessionattributebits/init(rawvalue:))

#### Bits

- [static var sessionIsRoot: SessionAttributeBits](/documentation/security/sessionattributebits/sessionisroot)
- [static var sessionHasGraphicAccess: SessionAttributeBits](/documentation/security/sessionattributebits/sessionhasgraphicaccess)
- [static var sessionHasTTY: SessionAttributeBits](/documentation/security/sessionattributebits/sessionhastty)
- [static var sessionIsRemote: SessionAttributeBits](/documentation/security/sessionattributebits/sessionisremote)

### Session Information

- [func SessionGetInfo(SecuritySessionId, UnsafeMutablePointer<SecuritySessionId>?, UnsafeMutablePointer<SessionAttributeBits>?) -> OSStatus](/documentation/security/sessiongetinfo(_:_:_:))
- [Session ID Values](/documentation/security/session-id-values)

#### Constants

- [var callerSecuritySession: SecuritySessionId](/documentation/security/callersecuritysession)
- [var noSecuritySession: SecuritySessionId](/documentation/security/nosecuritysession)
- [SecuritySessionId](/documentation/security/securitysessionid)

### Result Codes

- [Sessions API Result Codes](/documentation/security/sessions-api-result-codes)

#### Codes

- [var errSessionSuccess: OSStatus](/documentation/security/errsessionsuccess)
- [var errSessionInvalidId: OSStatus](/documentation/security/errsessioninvalidid)
- [var errSessionInvalidAttributes: OSStatus](/documentation/security/errsessioninvalidattributes)
- [var errSessionAuthorizationDenied: OSStatus](/documentation/security/errsessionauthorizationdenied)
- [var errSessionValueNotSet: OSStatus](/documentation/security/errsessionvaluenotset)
- [var errSessionInternal: OSStatus](/documentation/security/errsessioninternal)
- [var errSessionInvalidFlags: OSStatus](/documentation/security/errsessioninvalidflags)
- [One-time codes](/documentation/security/one-time-codes)

### Essentials

- [Enabling AutoFill for domain-bound SMS codes](/documentation/security/enabling-autofill-for-domain-bound-sms-codes)

## Secure data

- [Keychain services](/documentation/security/keychain-services)

### API components

- [Keychain items](/documentation/security/keychain-items)

#### Essentials

- [Using the keychain to manage user secrets](/documentation/security/using-the-keychain-to-manage-user-secrets)

##### Item Creation and Modification

- [Adding a password to the keychain](/documentation/security/adding-a-password-to-the-keychain)
- [Searching for keychain items](/documentation/security/searching-for-keychain-items)
- [Updating and deleting keychain items](/documentation/security/updating-and-deleting-keychain-items)

##### Item Access

- [Sharing access to keychain items among a collection of apps](/documentation/security/sharing-access-to-keychain-items-among-a-collection-of-apps)
- [Restricting keychain item accessibility](/documentation/security/restricting-keychain-item-accessibility)
- [TN3137: On Mac keychain APIs and implementations](/documentation/technotes/tn3137-on-mac-keychains)
- [SecKeychainItem](/documentation/security/seckeychainitem)
- [func SecKeychainItemGetTypeID() -> CFTypeID](/documentation/security/seckeychainitemgettypeid())

#### Adding keychain items

- [Adding a password to the keychain](/documentation/security/adding-a-password-to-the-keychain)
- [func SecItemAdd(CFDictionary, UnsafeMutablePointer<CFTypeRef?>?) -> OSStatus](/documentation/security/secitemadd(_:_:))
- [Item class keys and values](/documentation/security/item-class-keys-and-values)

##### Item class keys

- [let kSecClass: CFString](/documentation/security/ksecclass)

##### Item class values

- [let kSecClassGenericPassword: CFString](/documentation/security/ksecclassgenericpassword)
- [let kSecClassInternetPassword: CFString](/documentation/security/ksecclassinternetpassword)
- [let kSecClassCertificate: CFString](/documentation/security/ksecclasscertificate)
- [let kSecClassKey: CFString](/documentation/security/ksecclasskey)
- [let kSecClassIdentity: CFString](/documentation/security/ksecclassidentity)
- [Item attribute keys and values](/documentation/security/item-attribute-keys-and-values)

##### General Item Attribute Keys

- [let kSecAttrAccess: CFString](/documentation/security/ksecattraccess)
- [let kSecAttrAccessControl: CFString](/documentation/security/ksecattraccesscontrol)
- [let kSecAttrAccessible: CFString](/documentation/security/ksecattraccessible)
- [let kSecAttrAccessGroup: CFString](/documentation/security/ksecattraccessgroup)
- [let kSecAttrSynchronizable: CFString](/documentation/security/ksecattrsynchronizable)
- [let kSecAttrCreationDate: CFString](/documentation/security/ksecattrcreationdate)
- [let kSecAttrModificationDate: CFString](/documentation/security/ksecattrmodificationdate)
- [let kSecAttrDescription: CFString](/documentation/security/ksecattrdescription)
- [let kSecAttrComment: CFString](/documentation/security/ksecattrcomment)
- [let kSecAttrCreator: CFString](/documentation/security/ksecattrcreator)
- [let kSecAttrType: CFString](/documentation/security/ksecattrtype)
- [let kSecAttrLabel: CFString](/documentation/security/ksecattrlabel)
- [let kSecAttrIsInvisible: CFString](/documentation/security/ksecattrisinvisible)
- [let kSecAttrIsNegative: CFString](/documentation/security/ksecattrisnegative)
- [let kSecAttrSyncViewHint: CFString](/documentation/security/ksecattrsyncviewhint)
- [let kSecAttrPersistantReference: CFString](/documentation/security/ksecattrpersistantreference)
- [let kSecAttrPersistentReference: CFString](/documentation/security/ksecattrpersistentreference)
- [let kSecUseUserIndependentKeychain: CFString](/documentation/security/ksecuseuserindependentkeychain)

##### Password Attribute Keys

- [let kSecAttrAccount: CFString](/documentation/security/ksecattraccount)
- [let kSecAttrService: CFString](/documentation/security/ksecattrservice)
- [let kSecAttrGeneric: CFString](/documentation/security/ksecattrgeneric)
- [let kSecAttrSecurityDomain: CFString](/documentation/security/ksecattrsecuritydomain)
- [let kSecAttrServer: CFString](/documentation/security/ksecattrserver)
- [let kSecAttrProtocol: CFString](/documentation/security/ksecattrprotocol)
- [let kSecAttrAuthenticationType: CFString](/documentation/security/ksecattrauthenticationtype)
- [let kSecAttrPort: CFString](/documentation/security/ksecattrport)
- [let kSecAttrPath: CFString](/documentation/security/ksecattrpath)

##### Certificate Attribute Keys

- [let kSecAttrSubject: CFString](/documentation/security/ksecattrsubject)
- [let kSecAttrIssuer: CFString](/documentation/security/ksecattrissuer)
- [let kSecAttrSerialNumber: CFString](/documentation/security/ksecattrserialnumber)
- [let kSecAttrSubjectKeyID: CFString](/documentation/security/ksecattrsubjectkeyid)
- [let kSecAttrPublicKeyHash: CFString](/documentation/security/ksecattrpublickeyhash)
- [let kSecAttrCertificateType: CFString](/documentation/security/ksecattrcertificatetype)
- [let kSecAttrCertificateEncoding: CFString](/documentation/security/ksecattrcertificateencoding)

##### Cryptographic Key Attribute Keys

- [let kSecAttrKeyClass: CFString](/documentation/security/ksecattrkeyclass)
- [let kSecAttrApplicationLabel: CFString](/documentation/security/ksecattrapplicationlabel)
- [let kSecAttrApplicationTag: CFString](/documentation/security/ksecattrapplicationtag)
- [let kSecAttrKeyType: CFString](/documentation/security/ksecattrkeytype)
- [let kSecAttrPRF: CFString](/documentation/security/ksecattrprf)
- [let kSecAttrSalt: CFString](/documentation/security/ksecattrsalt)
- [let kSecAttrRounds: CFString](/documentation/security/ksecattrrounds)
- [let kSecAttrKeySizeInBits: CFString](/documentation/security/ksecattrkeysizeinbits)
- [let kSecAttrEffectiveKeySize: CFString](/documentation/security/ksecattreffectivekeysize)
- [let kSecAttrTokenID: CFString](/documentation/security/ksecattrtokenid)

##### Cryptographic Key Usage Attribute Keys

- [let kSecAttrIsPermanent: CFString](/documentation/security/ksecattrispermanent)
- [let kSecAttrIsSensitive: CFString](/documentation/security/ksecattrissensitive)
- [let kSecAttrIsExtractable: CFString](/documentation/security/ksecattrisextractable)
- [let kSecAttrCanEncrypt: CFString](/documentation/security/ksecattrcanencrypt)
- [let kSecAttrCanDecrypt: CFString](/documentation/security/ksecattrcandecrypt)
- [let kSecAttrCanDerive: CFString](/documentation/security/ksecattrcanderive)
- [let kSecAttrCanSign: CFString](/documentation/security/ksecattrcansign)
- [let kSecAttrCanVerify: CFString](/documentation/security/ksecattrcanverify)
- [let kSecAttrCanWrap: CFString](/documentation/security/ksecattrcanwrap)
- [let kSecAttrCanUnwrap: CFString](/documentation/security/ksecattrcanunwrap)

##### Protocol Values

- [let kSecAttrProtocolFTP: CFString](/documentation/security/ksecattrprotocolftp)
- [let kSecAttrProtocolFTPAccount: CFString](/documentation/security/ksecattrprotocolftpaccount)
- [let kSecAttrProtocolHTTP: CFString](/documentation/security/ksecattrprotocolhttp)
- [let kSecAttrProtocolIRC: CFString](/documentation/security/ksecattrprotocolirc)
- [let kSecAttrProtocolNNTP: CFString](/documentation/security/ksecattrprotocolnntp)
- [let kSecAttrProtocolPOP3: CFString](/documentation/security/ksecattrprotocolpop3)
- [let kSecAttrProtocolSMTP: CFString](/documentation/security/ksecattrprotocolsmtp)
- [let kSecAttrProtocolSOCKS: CFString](/documentation/security/ksecattrprotocolsocks)
- [let kSecAttrProtocolIMAP: CFString](/documentation/security/ksecattrprotocolimap)
- [let kSecAttrProtocolLDAP: CFString](/documentation/security/ksecattrprotocolldap)
- [let kSecAttrProtocolAppleTalk: CFString](/documentation/security/ksecattrprotocolappletalk)
- [let kSecAttrProtocolAFP: CFString](/documentation/security/ksecattrprotocolafp)
- [let kSecAttrProtocolTelnet: CFString](/documentation/security/ksecattrprotocoltelnet)
- [let kSecAttrProtocolSSH: CFString](/documentation/security/ksecattrprotocolssh)
- [let kSecAttrProtocolFTPS: CFString](/documentation/security/ksecattrprotocolftps)
- [let kSecAttrProtocolHTTPS: CFString](/documentation/security/ksecattrprotocolhttps)
- [let kSecAttrProtocolHTTPProxy: CFString](/documentation/security/ksecattrprotocolhttpproxy)
- [let kSecAttrProtocolHTTPSProxy: CFString](/documentation/security/ksecattrprotocolhttpsproxy)
- [let kSecAttrProtocolFTPProxy: CFString](/documentation/security/ksecattrprotocolftpproxy)
- [let kSecAttrProtocolSMB: CFString](/documentation/security/ksecattrprotocolsmb)
- [let kSecAttrProtocolRTSP: CFString](/documentation/security/ksecattrprotocolrtsp)
- [let kSecAttrProtocolRTSPProxy: CFString](/documentation/security/ksecattrprotocolrtspproxy)
- [let kSecAttrProtocolDAAP: CFString](/documentation/security/ksecattrprotocoldaap)
- [let kSecAttrProtocolEPPC: CFString](/documentation/security/ksecattrprotocoleppc)
- [let kSecAttrProtocolIPP: CFString](/documentation/security/ksecattrprotocolipp)
- [let kSecAttrProtocolNNTPS: CFString](/documentation/security/ksecattrprotocolnntps)
- [let kSecAttrProtocolLDAPS: CFString](/documentation/security/ksecattrprotocolldaps)
- [let kSecAttrProtocolTelnetS: CFString](/documentation/security/ksecattrprotocoltelnets)
- [let kSecAttrProtocolIMAPS: CFString](/documentation/security/ksecattrprotocolimaps)
- [let kSecAttrProtocolIRCS: CFString](/documentation/security/ksecattrprotocolircs)
- [let kSecAttrProtocolPOP3S: CFString](/documentation/security/ksecattrprotocolpop3s)

##### Authentication Type Values

- [let kSecAttrAuthenticationTypeNTLM: CFString](/documentation/security/ksecattrauthenticationtypentlm)
- [let kSecAttrAuthenticationTypeMSN: CFString](/documentation/security/ksecattrauthenticationtypemsn)
- [let kSecAttrAuthenticationTypeDPA: CFString](/documentation/security/ksecattrauthenticationtypedpa)
- [let kSecAttrAuthenticationTypeRPA: CFString](/documentation/security/ksecattrauthenticationtyperpa)
- [let kSecAttrAuthenticationTypeHTTPBasic: CFString](/documentation/security/ksecattrauthenticationtypehttpbasic)
- [let kSecAttrAuthenticationTypeHTTPDigest: CFString](/documentation/security/ksecattrauthenticationtypehttpdigest)
- [let kSecAttrAuthenticationTypeHTMLForm: CFString](/documentation/security/ksecattrauthenticationtypehtmlform)
- [let kSecAttrAuthenticationTypeDefault: CFString](/documentation/security/ksecattrauthenticationtypedefault)

##### Key Class Values

- [let kSecAttrKeyClassPublic: CFString](/documentation/security/ksecattrkeyclasspublic)
- [let kSecAttrKeyClassPrivate: CFString](/documentation/security/ksecattrkeyclassprivate)
- [let kSecAttrKeyClassSymmetric: CFString](/documentation/security/ksecattrkeyclasssymmetric)

##### Key Type Values

- [let kSecAttrKeyTypeRSA: CFString](/documentation/security/ksecattrkeytypersa)
- [let kSecAttrKeyTypeDSA: CFString](/documentation/security/ksecattrkeytypedsa)
- [let kSecAttrKeyTypeAES: CFString](/documentation/security/ksecattrkeytypeaes)
- [let kSecAttrKeyTypeDES: CFString](/documentation/security/ksecattrkeytypedes)
- [let kSecAttrKeyType3DES: CFString](/documentation/security/ksecattrkeytype3des)
- [let kSecAttrKeyTypeRC4: CFString](/documentation/security/ksecattrkeytyperc4)
- [let kSecAttrKeyTypeRC2: CFString](/documentation/security/ksecattrkeytyperc2)
- [let kSecAttrKeyTypeCAST: CFString](/documentation/security/ksecattrkeytypecast)
- [let kSecAttrKeyTypeECDSA: CFString](/documentation/security/ksecattrkeytypeecdsa)
- [let kSecAttrKeyTypeEC: CFString](/documentation/security/ksecattrkeytypeec)
- [let kSecAttrKeyTypeECSECPrimeRandom: CFString](/documentation/security/ksecattrkeytypeecsecprimerandom)

##### Synchronizability Values

- [let kSecAttrSynchronizableAny: CFString](/documentation/security/ksecattrsynchronizableany)

##### Token ID Values

- [let kSecAttrTokenIDSecureEnclave: CFString](/documentation/security/ksecattrtokenidsecureenclave)

##### Accessibility Values

- [let kSecAttrAccessibleWhenPasscodeSetThisDeviceOnly: CFString](/documentation/security/ksecattraccessiblewhenpasscodesetthisdeviceonly)
- [let kSecAttrAccessibleWhenUnlockedThisDeviceOnly: CFString](/documentation/security/ksecattraccessiblewhenunlockedthisdeviceonly)
- [let kSecAttrAccessibleWhenUnlocked: CFString](/documentation/security/ksecattraccessiblewhenunlocked)
- [let kSecAttrAccessibleAfterFirstUnlockThisDeviceOnly: CFString](/documentation/security/ksecattraccessibleafterfirstunlockthisdeviceonly)
- [let kSecAttrAccessibleAfterFirstUnlock: CFString](/documentation/security/ksecattraccessibleafterfirstunlock)
- [let kSecAttrAccessibleAlwaysThisDeviceOnly: CFString](/documentation/security/ksecattraccessiblealwaysthisdeviceonly)
- [let kSecAttrAccessibleAlways: CFString](/documentation/security/ksecattraccessiblealways)

##### Pseudorandom Function Values

- [let kSecAttrPRFHmacAlgSHA1: CFString](/documentation/security/ksecattrprfhmacalgsha1)
- [let kSecAttrPRFHmacAlgSHA224: CFString](/documentation/security/ksecattrprfhmacalgsha224)
- [let kSecAttrPRFHmacAlgSHA256: CFString](/documentation/security/ksecattrprfhmacalgsha256)
- [let kSecAttrPRFHmacAlgSHA384: CFString](/documentation/security/ksecattrprfhmacalgsha384)
- [let kSecAttrPRFHmacAlgSHA512: CFString](/documentation/security/ksecattrprfhmacalgsha512)

##### Access Group Values

- [let kSecAttrAccessGroupToken: CFString](/documentation/security/ksecattraccessgrouptoken)

#### Keychain item search

- [Searching for keychain items](/documentation/security/searching-for-keychain-items)
- [func SecItemCopyMatching(CFDictionary, UnsafeMutablePointer<CFTypeRef?>?) -> OSStatus](/documentation/security/secitemcopymatching(_:_:))
- [Search attribute keys and values](/documentation/security/search-attribute-keys-and-values)

##### Item search matching keys

- [let kSecMatchPolicy: CFString](/documentation/security/ksecmatchpolicy)
- [let kSecMatchItemList: CFString](/documentation/security/ksecmatchitemlist)
- [let kSecMatchSearchList: CFString](/documentation/security/ksecmatchsearchlist)
- [let kSecMatchIssuers: CFString](/documentation/security/ksecmatchissuers)
- [let kSecMatchEmailAddressIfPresent: CFString](/documentation/security/ksecmatchemailaddressifpresent)
- [let kSecMatchSubjectContains: CFString](/documentation/security/ksecmatchsubjectcontains)
- [let kSecMatchSubjectStartsWith: CFString](/documentation/security/ksecmatchsubjectstartswith)
- [let kSecMatchSubjectEndsWith: CFString](/documentation/security/ksecmatchsubjectendswith)
- [let kSecMatchSubjectWholeString: CFString](/documentation/security/ksecmatchsubjectwholestring)
- [let kSecMatchCaseInsensitive: CFString](/documentation/security/ksecmatchcaseinsensitive)
- [let kSecMatchDiacriticInsensitive: CFString](/documentation/security/ksecmatchdiacriticinsensitive)
- [let kSecMatchWidthInsensitive: CFString](/documentation/security/ksecmatchwidthinsensitive)
- [let kSecMatchTrustedOnly: CFString](/documentation/security/ksecmatchtrustedonly)
- [let kSecMatchValidOnDate: CFString](/documentation/security/ksecmatchvalidondate)
- [let kSecMatchLimit: CFString](/documentation/security/ksecmatchlimit)

##### Match limit values

- [let kSecMatchLimitOne: CFString](/documentation/security/ksecmatchlimitone)
- [let kSecMatchLimitAll: CFString](/documentation/security/ksecmatchlimitall)

##### Additional item search keys

- [let kSecUseItemList: CFString](/documentation/security/ksecuseitemlist)
- [let kSecUseKeychain: CFString](/documentation/security/ksecusekeychain)
- [let kSecUseOperationPrompt: CFString](/documentation/security/ksecuseoperationprompt)
- [let kSecUseNoAuthenticationUI: CFString](/documentation/security/ksecusenoauthenticationui)
- [let kSecUseAuthenticationUI: CFString](/documentation/security/ksecuseauthenticationui)
- [let kSecUseAuthenticationContext: CFString](/documentation/security/ksecuseauthenticationcontext)
- [let kSecUseDataProtectionKeychain: CFString](/documentation/security/ksecusedataprotectionkeychain)

##### UI authentication values

- [let kSecUseAuthenticationUIAllow: CFString](/documentation/security/ksecuseauthenticationuiallow)
- [let kSecUseAuthenticationUIFail: CFString](/documentation/security/ksecuseauthenticationuifail)
- [let kSecUseAuthenticationUISkip: CFString](/documentation/security/ksecuseauthenticationuiskip)
- [Item return result keys](/documentation/security/item-return-result-keys)

##### Item result keys

- [let kSecReturnData: CFString](/documentation/security/ksecreturndata)
- [let kSecReturnAttributes: CFString](/documentation/security/ksecreturnattributes)
- [let kSecReturnRef: CFString](/documentation/security/ksecreturnref)
- [let kSecReturnPersistentRef: CFString](/documentation/security/ksecreturnpersistentref)

##### Item value type keys

- [let kSecValueData: CFString](/documentation/security/ksecvaluedata)
- [let kSecValueRef: CFString](/documentation/security/ksecvalueref)
- [let kSecValuePersistentRef: CFString](/documentation/security/ksecvaluepersistentref)

#### Keychain item modification

- [Updating and deleting keychain items](/documentation/security/updating-and-deleting-keychain-items)
- [func SecItemUpdate(CFDictionary, CFDictionary) -> OSStatus](/documentation/security/secitemupdate(_:_:))
- [func SecItemDelete(CFDictionary) -> OSStatus](/documentation/security/secitemdelete(_:))

#### Keychain item access

- [Sharing access to keychain items among a collection of apps](/documentation/security/sharing-access-to-keychain-items-among-a-collection-of-apps)
- [Keychain Access Groups Entitlement](/documentation/bundleresources/entitlements/keychain-access-groups)
- [Restricting keychain item accessibility](/documentation/security/restricting-keychain-item-accessibility)
- [func SecAccessControlCreateWithFlags(CFAllocator?, CFTypeRef, SecAccessControlCreateFlags, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecAccessControl?](/documentation/security/secaccesscontrolcreatewithflags(_:_:_:_:))
- [SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags)

##### Constraints

- [static var devicePasscode: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/devicepasscode)
- [static var biometryAny: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/biometryany)
- [static var biometryCurrentSet: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/biometrycurrentset)
- [static var userPresence: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/userpresence)
- [static var watch: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/watch)

##### Conjunctions

- [static var and: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/and)
- [static var or: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/or)

##### Additional Options

- [static var applicationPassword: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/applicationpassword)
- [static var privateKeyUsage: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/privatekeyusage)

##### Initializers

- [init(rawValue: CFOptionFlags)](/documentation/security/secaccesscontrolcreateflags/init(rawvalue:))

##### Legacy Constraints

- [static var touchIDAny: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/touchidany)
- [static var touchIDCurrentSet: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/touchidcurrentset)

##### Type Properties

- [static var companion: SecAccessControlCreateFlags](/documentation/security/secaccesscontrolcreateflags/companion)
- [SecAccessControl](/documentation/security/secaccesscontrol)
- [func SecAccessControlGetTypeID() -> CFTypeID](/documentation/security/secaccesscontrolgettypeid())

#### Import and export

- [func SecItemImport(CFData, CFString?, UnsafeMutablePointer<SecExternalFormat>?, UnsafeMutablePointer<SecExternalItemType>?, SecItemImportExportFlags, UnsafePointer<SecItemImportExportKeyParameters>?, SecKeychain?, UnsafeMutablePointer<CFArray?>?) -> OSStatus](/documentation/security/secitemimport(_:_:_:_:_:_:_:_:))
- [func SecItemExport(CFTypeRef, SecExternalFormat, SecItemImportExportFlags, UnsafePointer<SecItemImportExportKeyParameters>?, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/secitemexport(_:_:_:_:_:))
- [SecExternalFormat](/documentation/security/secexternalformat)

##### Constants

- [case formatUnknown](/documentation/security/secexternalformat/formatunknown)
- [case formatOpenSSL](/documentation/security/secexternalformat/formatopenssl)
- [case formatSSH](/documentation/security/secexternalformat/formatssh)
- [case formatBSAFE](/documentation/security/secexternalformat/formatbsafe)
- [case formatSSHv2](/documentation/security/secexternalformat/formatsshv2)
- [case formatRawKey](/documentation/security/secexternalformat/formatrawkey)
- [case formatWrappedPKCS8](/documentation/security/secexternalformat/formatwrappedpkcs8)
- [case formatWrappedOpenSSL](/documentation/security/secexternalformat/formatwrappedopenssl)
- [case formatWrappedSSH](/documentation/security/secexternalformat/formatwrappedssh)
- [case formatWrappedLSH](/documentation/security/secexternalformat/formatwrappedlsh)
- [case formatX509Cert](/documentation/security/secexternalformat/formatx509cert)
- [case formatPEMSequence](/documentation/security/secexternalformat/formatpemsequence)
- [case formatPKCS7](/documentation/security/secexternalformat/formatpkcs7)
- [case formatPKCS12](/documentation/security/secexternalformat/formatpkcs12)
- [case formatNetscapeCertSequence](/documentation/security/secexternalformat/formatnetscapecertsequence)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/secexternalformat/init(rawvalue:))
- [SecExternalItemType](/documentation/security/secexternalitemtype)

##### Constants

- [case itemTypeUnknown](/documentation/security/secexternalitemtype/itemtypeunknown)
- [case itemTypePrivateKey](/documentation/security/secexternalitemtype/itemtypeprivatekey)
- [case itemTypePublicKey](/documentation/security/secexternalitemtype/itemtypepublickey)
- [case itemTypeSessionKey](/documentation/security/secexternalitemtype/itemtypesessionkey)
- [case itemTypeCertificate](/documentation/security/secexternalitemtype/itemtypecertificate)
- [case itemTypeAggregate](/documentation/security/secexternalitemtype/itemtypeaggregate)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/secexternalitemtype/init(rawvalue:))
- [SecItemImportExportFlags](/documentation/security/secitemimportexportflags)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/secitemimportexportflags/init(rawvalue:))

##### Constants

- [static var pemArmour: SecItemImportExportFlags](/documentation/security/secitemimportexportflags/pemarmour)
- [SecItemImportExportKeyParameters](/documentation/security/secitemimportexportkeyparameters)

##### Instance Properties

- [var accessRef: Unmanaged<SecAccess>?](/documentation/security/secitemimportexportkeyparameters/accessref)
- [var alertPrompt: Unmanaged<CFString>?](/documentation/security/secitemimportexportkeyparameters/alertprompt)
- [var alertTitle: Unmanaged<CFString>?](/documentation/security/secitemimportexportkeyparameters/alerttitle)
- [var flags: SecKeyImportExportFlags](/documentation/security/secitemimportexportkeyparameters/flags)
- [var keyAttributes: Unmanaged<CFArray>?](/documentation/security/secitemimportexportkeyparameters/keyattributes)
- [var keyUsage: Unmanaged<CFArray>?](/documentation/security/secitemimportexportkeyparameters/keyusage)
- [var passphrase: Unmanaged<CFTypeRef>?](/documentation/security/secitemimportexportkeyparameters/passphrase)
- [var version: UInt32](/documentation/security/secitemimportexportkeyparameters/version)

##### Initializers

- [init()](/documentation/security/secitemimportexportkeyparameters/init())
- [init(version: UInt32, flags: SecKeyImportExportFlags, passphrase: Unmanaged<CFTypeRef>?, alertTitle: Unmanaged<CFString>?, alertPrompt: Unmanaged<CFString>?, accessRef: Unmanaged<SecAccess>?, keyUsage: Unmanaged<CFArray>?, keyAttributes: Unmanaged<CFArray>?)](/documentation/security/secitemimportexportkeyparameters/init(version:flags:passphrase:alerttitle:alertprompt:accessref:keyusage:keyattributes:))
- [SecKeyImportExportFlags](/documentation/security/seckeyimportexportflags)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/seckeyimportexportflags/init(rawvalue:))

##### Constants

- [static var importOnlyOne: SecKeyImportExportFlags](/documentation/security/seckeyimportexportflags/importonlyone)
- [static var securePassphrase: SecKeyImportExportFlags](/documentation/security/seckeyimportexportflags/securepassphrase)
- [static var noAccessControl: SecKeyImportExportFlags](/documentation/security/seckeyimportexportflags/noaccesscontrol)
- [var SEC_KEY_IMPORT_EXPORT_PARAMS_VERSION: Int32](/documentation/security/sec_key_import_export_params_version)
- [SecKeyImportExportParameters](/documentation/security/seckeyimportexportparameters)

##### Instance Properties

- [var accessRef: Unmanaged<SecAccess>?](/documentation/security/seckeyimportexportparameters/accessref)
- [var alertPrompt: Unmanaged<CFString>](/documentation/security/seckeyimportexportparameters/alertprompt)
- [var alertTitle: Unmanaged<CFString>](/documentation/security/seckeyimportexportparameters/alerttitle)
- [var flags: SecKeyImportExportFlags](/documentation/security/seckeyimportexportparameters/flags)
- [var keyAttributes: CSSM_KEYATTR_FLAGS](/documentation/security/seckeyimportexportparameters/keyattributes)
- [var keyUsage: CSSM_KEYUSE](/documentation/security/seckeyimportexportparameters/keyusage)
- [var passphrase: Unmanaged<CFTypeRef>?](/documentation/security/seckeyimportexportparameters/passphrase)
- [var version: UInt32](/documentation/security/seckeyimportexportparameters/version)

##### Initializers

- [init(version: UInt32, flags: SecKeyImportExportFlags, passphrase: Unmanaged<CFTypeRef>?, alertTitle: Unmanaged<CFString>, alertPrompt: Unmanaged<CFString>, accessRef: Unmanaged<SecAccess>?, keyUsage: CSSM_KEYUSE, keyAttributes: CSSM_KEYATTR_FLAGS)](/documentation/security/seckeyimportexportparameters/init(version:flags:passphrase:alerttitle:alertprompt:accessref:keyusage:keyattributes:))

#### Legacy keychain item creation

- [func SecKeychainItemCreateFromContent(SecItemClass, UnsafeMutablePointer<SecKeychainAttributeList>, UInt32, UnsafeRawPointer?, SecKeychain?, SecAccess?, UnsafeMutablePointer<SecKeychainItem?>?) -> OSStatus](/documentation/security/seckeychainitemcreatefromcontent(_:_:_:_:_:_:_:))
- [func SecKeychainItemCreateCopy(SecKeychainItem, SecKeychain?, SecAccess?, UnsafeMutablePointer<SecKeychainItem?>) -> OSStatus](/documentation/security/seckeychainitemcreatecopy(_:_:_:_:))
- [func SecKeychainItemCreatePersistentReference(SecKeychainItem, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/seckeychainitemcreatepersistentreference(_:_:))
- [func SecKeychainItemCopyFromPersistentReference(CFData, UnsafeMutablePointer<SecKeychainItem?>) -> OSStatus](/documentation/security/seckeychainitemcopyfrompersistentreference(_:_:))
- [SecItemClass](/documentation/security/secitemclass)

##### Constants

- [case internetPasswordItemClass](/documentation/security/secitemclass/internetpassworditemclass)
- [case genericPasswordItemClass](/documentation/security/secitemclass/genericpassworditemclass)
- [case certificateItemClass](/documentation/security/secitemclass/certificateitemclass)
- [case publicKeyItemClass](/documentation/security/secitemclass/publickeyitemclass)
- [case privateKeyItemClass](/documentation/security/secitemclass/privatekeyitemclass)
- [case symmetricKeyItemClass](/documentation/security/secitemclass/symmetrickeyitemclass)

##### Initializers

- [init?(rawValue: FourCharCode)](/documentation/security/secitemclass/init(rawvalue:))

#### Legacy keychain item management

- [func SecKeychainItemCopyAttributesAndData(SecKeychainItem, UnsafeMutablePointer<SecKeychainAttributeInfo>?, UnsafeMutablePointer<SecItemClass>?, UnsafeMutablePointer<UnsafeMutablePointer<SecKeychainAttributeList>?>?, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UnsafeMutableRawPointer?>?) -> OSStatus](/documentation/security/seckeychainitemcopyattributesanddata(_:_:_:_:_:_:))
- [func SecKeychainItemModifyAttributesAndData(SecKeychainItem, UnsafePointer<SecKeychainAttributeList>?, UInt32, UnsafeRawPointer?) -> OSStatus](/documentation/security/seckeychainitemmodifyattributesanddata(_:_:_:_:))
- [func SecKeychainItemFreeAttributesAndData(UnsafeMutablePointer<SecKeychainAttributeList>?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/security/seckeychainitemfreeattributesanddata(_:_:))
- [func SecKeychainItemCopyContent(SecKeychainItem, UnsafeMutablePointer<SecItemClass>?, UnsafeMutablePointer<SecKeychainAttributeList>?, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UnsafeMutableRawPointer?>?) -> OSStatus](/documentation/security/seckeychainitemcopycontent(_:_:_:_:_:))
- [func SecKeychainItemModifyContent(SecKeychainItem, UnsafePointer<SecKeychainAttributeList>?, UInt32, UnsafeRawPointer?) -> OSStatus](/documentation/security/seckeychainitemmodifycontent(_:_:_:_:))
- [func SecKeychainItemFreeContent(UnsafeMutablePointer<SecKeychainAttributeList>?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/security/seckeychainitemfreecontent(_:_:))
- [func SecKeychainItemCopyKeychain(SecKeychainItem, UnsafeMutablePointer<SecKeychain?>) -> OSStatus](/documentation/security/seckeychainitemcopykeychain(_:_:))
- [func SecKeychainItemDelete(SecKeychainItem) -> OSStatus](/documentation/security/seckeychainitemdelete(_:))
- [SecKeychainAttrType](/documentation/security/seckeychainattrtype)
- [SecKeychainAttribute](/documentation/security/seckeychainattribute)

##### Instance Properties

- [var data: UnsafeMutableRawPointer?](/documentation/security/seckeychainattribute/data)
- [var length: UInt32](/documentation/security/seckeychainattribute/length)
- [var tag: SecKeychainAttrType](/documentation/security/seckeychainattribute/tag)

##### Initializers

- [init()](/documentation/security/seckeychainattribute/init())
- [init(tag: SecKeychainAttrType, length: UInt32, data: UnsafeMutableRawPointer?)](/documentation/security/seckeychainattribute/init(tag:length:data:))
- [SecKeychainAttributePtr](/documentation/security/seckeychainattributeptr)
- [SecKeychainAttributeList](/documentation/security/seckeychainattributelist)

##### Instance Properties

- [var attr: UnsafeMutablePointer<SecKeychainAttribute>?](/documentation/security/seckeychainattributelist/attr)
- [var count: UInt32](/documentation/security/seckeychainattributelist/count)

##### Initializers

- [init()](/documentation/security/seckeychainattributelist/init())
- [init(count: UInt32, attr: UnsafeMutablePointer<SecKeychainAttribute>?)](/documentation/security/seckeychainattributelist/init(count:attr:))

#### Legacy attribute info

- [func SecKeychainAttributeInfoForItemID(SecKeychain?, UInt32, UnsafeMutablePointer<UnsafeMutablePointer<SecKeychainAttributeInfo>?>) -> OSStatus](/documentation/security/seckeychainattributeinfoforitemid(_:_:_:))
- [func SecKeychainFreeAttributeInfo(UnsafeMutablePointer<SecKeychainAttributeInfo>) -> OSStatus](/documentation/security/seckeychainfreeattributeinfo(_:))
- [SecKeychainAttributeInfo](/documentation/security/seckeychainattributeinfo)

##### Instance Properties

- [var count: UInt32](/documentation/security/seckeychainattributeinfo/count)
- [var format: UnsafeMutablePointer<UInt32>?](/documentation/security/seckeychainattributeinfo/format)
- [var tag: UnsafeMutablePointer<UInt32>](/documentation/security/seckeychainattributeinfo/tag)

##### Initializers

- [init(count: UInt32, tag: UnsafeMutablePointer<UInt32>, format: UnsafeMutablePointer<UInt32>?)](/documentation/security/seckeychainattributeinfo/init(count:tag:format:))
- [SecItemAttr](/documentation/security/secitemattr)

##### Constants

- [case creationDateItemAttr](/documentation/security/secitemattr/creationdateitemattr)
- [case modDateItemAttr](/documentation/security/secitemattr/moddateitemattr)
- [case descriptionItemAttr](/documentation/security/secitemattr/descriptionitemattr)
- [case commentItemAttr](/documentation/security/secitemattr/commentitemattr)
- [case creatorItemAttr](/documentation/security/secitemattr/creatoritemattr)
- [case typeItemAttr](/documentation/security/secitemattr/typeitemattr)
- [case scriptCodeItemAttr](/documentation/security/secitemattr/scriptcodeitemattr)
- [case labelItemAttr](/documentation/security/secitemattr/labelitemattr)
- [case invisibleItemAttr](/documentation/security/secitemattr/invisibleitemattr)
- [case negativeItemAttr](/documentation/security/secitemattr/negativeitemattr)
- [case customIconItemAttr](/documentation/security/secitemattr/customiconitemattr)
- [case accountItemAttr](/documentation/security/secitemattr/accountitemattr)
- [case serviceItemAttr](/documentation/security/secitemattr/serviceitemattr)
- [case genericItemAttr](/documentation/security/secitemattr/genericitemattr)
- [case securityDomainItemAttr](/documentation/security/secitemattr/securitydomainitemattr)
- [case serverItemAttr](/documentation/security/secitemattr/serveritemattr)
- [case authenticationTypeItemAttr](/documentation/security/secitemattr/authenticationtypeitemattr)
- [case portItemAttr](/documentation/security/secitemattr/portitemattr)
- [case pathItemAttr](/documentation/security/secitemattr/pathitemattr)
- [case volumeItemAttr](/documentation/security/secitemattr/volumeitemattr)
- [case addressItemAttr](/documentation/security/secitemattr/addressitemattr)
- [case signatureItemAttr](/documentation/security/secitemattr/signatureitemattr)
- [case protocolItemAttr](/documentation/security/secitemattr/protocolitemattr)
- [case certificateType](/documentation/security/secitemattr/certificatetype)
- [case certificateEncoding](/documentation/security/secitemattr/certificateencoding)
- [case crlType](/documentation/security/secitemattr/crltype)
- [case crlEncoding](/documentation/security/secitemattr/crlencoding)
- [case alias](/documentation/security/secitemattr/alias)

##### Initializers

- [init?(rawValue: FourCharCode)](/documentation/security/secitemattr/init(rawvalue:))
- [Keychain Item Attribute Constants For Keys](/documentation/security/keychain-item-attribute-constants-for-keys)

##### Constants

- [var kSecKeyKeyClass: Int32](/documentation/security/kseckeykeyclass)
- [var kSecKeyPrintName: Int32](/documentation/security/kseckeyprintname)
- [var kSecKeyAlias: Int32](/documentation/security/kseckeyalias)
- [var kSecKeyPermanent: Int32](/documentation/security/kseckeypermanent)
- [var kSecKeyPrivate: Int32](/documentation/security/kseckeyprivate)
- [var kSecKeyModifiable: Int32](/documentation/security/kseckeymodifiable)
- [var kSecKeyLabel: Int32](/documentation/security/kseckeylabel)
- [var kSecKeyApplicationTag: Int32](/documentation/security/kseckeyapplicationtag)
- [var kSecKeyKeyCreator: Int32](/documentation/security/kseckeykeycreator)
- [var kSecKeyKeyType: Int32](/documentation/security/kseckeykeytype)
- [var kSecKeyKeySizeInBits: Int32](/documentation/security/kseckeykeysizeinbits)
- [var kSecKeyEffectiveKeySize: Int32](/documentation/security/kseckeyeffectivekeysize)
- [var kSecKeyStartDate: Int32](/documentation/security/kseckeystartdate)
- [var kSecKeyEndDate: Int32](/documentation/security/kseckeyenddate)
- [var kSecKeySensitive: Int32](/documentation/security/kseckeysensitive)
- [var kSecKeyAlwaysSensitive: Int32](/documentation/security/kseckeyalwayssensitive)
- [var kSecKeyExtractable: Int32](/documentation/security/kseckeyextractable)
- [var kSecKeyNeverExtractable: Int32](/documentation/security/kseckeyneverextractable)
- [var kSecKeyEncrypt: Int32](/documentation/security/kseckeyencrypt)
- [var kSecKeyDecrypt: Int32](/documentation/security/kseckeydecrypt)
- [var kSecKeyDerive: Int32](/documentation/security/kseckeyderive)
- [var kSecKeySign: Int32](/documentation/security/kseckeysign)
- [var kSecKeyVerify: Int32](/documentation/security/kseckeyverify)
- [var kSecKeySignRecover: Int32](/documentation/security/kseckeysignrecover)
- [var kSecKeyVerifyRecover: Int32](/documentation/security/kseckeyverifyrecover)
- [var kSecKeyWrap: Int32](/documentation/security/kseckeywrap)
- [var kSecKeyUnwrap: Int32](/documentation/security/kseckeyunwrap)
- [SecAFPServerSignature](/documentation/security/secafpserversignature)

#### Legacy password storage

- [func SecKeychainAddInternetPassword(SecKeychain?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt16, SecProtocolType, SecAuthenticationType, UInt32, UnsafeRawPointer, UnsafeMutablePointer<SecKeychainItem?>?) -> OSStatus](/documentation/security/seckeychainaddinternetpassword(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func SecKeychainFindInternetPassword(CFTypeRef?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt16, SecProtocolType, SecAuthenticationType, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UnsafeMutableRawPointer?>?, UnsafeMutablePointer<SecKeychainItem?>?) -> OSStatus](/documentation/security/seckeychainfindinternetpassword(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func SecKeychainAddGenericPassword(SecKeychain?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafeRawPointer, UnsafeMutablePointer<SecKeychainItem?>?) -> OSStatus](/documentation/security/seckeychainaddgenericpassword(_:_:_:_:_:_:_:_:))
- [func SecKeychainFindGenericPassword(CFTypeRef?, UInt32, UnsafePointer<CChar>?, UInt32, UnsafePointer<CChar>?, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UnsafeMutableRawPointer?>?, UnsafeMutablePointer<SecKeychainItem?>?) -> OSStatus](/documentation/security/seckeychainfindgenericpassword(_:_:_:_:_:_:_:_:))
- [SecProtocolType](/documentation/security/secprotocoltype)

##### Constants

- [case FTP](/documentation/security/secprotocoltype/ftp)
- [case ftpAccount](/documentation/security/secprotocoltype/ftpaccount)
- [case HTTP](/documentation/security/secprotocoltype/http)
- [case IRC](/documentation/security/secprotocoltype/irc)
- [case NNTP](/documentation/security/secprotocoltype/nntp)
- [case POP3](/documentation/security/secprotocoltype/pop3)
- [case SMTP](/documentation/security/secprotocoltype/smtp)
- [case SOCKS](/documentation/security/secprotocoltype/socks)
- [case IMAP](/documentation/security/secprotocoltype/imap)
- [case LDAP](/documentation/security/secprotocoltype/ldap)
- [case appleTalk](/documentation/security/secprotocoltype/appletalk)
- [case AFP](/documentation/security/secprotocoltype/afp)
- [case telnet](/documentation/security/secprotocoltype/telnet)
- [case SSH](/documentation/security/secprotocoltype/ssh)
- [case FTPS](/documentation/security/secprotocoltype/ftps)
- [case HTTPS](/documentation/security/secprotocoltype/https)
- [case httpProxy](/documentation/security/secprotocoltype/httpproxy)
- [case httpsProxy](/documentation/security/secprotocoltype/httpsproxy)
- [case ftpProxy](/documentation/security/secprotocoltype/ftpproxy)
- [case CIFS](/documentation/security/secprotocoltype/cifs)
- [case SMB](/documentation/security/secprotocoltype/smb)
- [case RTSP](/documentation/security/secprotocoltype/rtsp)
- [case rtspProxy](/documentation/security/secprotocoltype/rtspproxy)
- [case DAAP](/documentation/security/secprotocoltype/daap)
- [case EPPC](/documentation/security/secprotocoltype/eppc)
- [case IPP](/documentation/security/secprotocoltype/ipp)
- [case NNTPS](/documentation/security/secprotocoltype/nntps)
- [case LDAPS](/documentation/security/secprotocoltype/ldaps)
- [case telnetS](/documentation/security/secprotocoltype/telnets)
- [case IMAPS](/documentation/security/secprotocoltype/imaps)
- [case IRCS](/documentation/security/secprotocoltype/ircs)
- [case POP3S](/documentation/security/secprotocoltype/pop3s)
- [case cvSpserver](/documentation/security/secprotocoltype/cvspserver)
- [case SVN](/documentation/security/secprotocoltype/svn)
- [case any](/documentation/security/secprotocoltype/any)

##### Initializers

- [init?(rawValue: FourCharCode)](/documentation/security/secprotocoltype/init(rawvalue:))
- [SecAuthenticationType](/documentation/security/secauthenticationtype)

##### Constants

- [case NTLM](/documentation/security/secauthenticationtype/ntlm)
- [case MSN](/documentation/security/secauthenticationtype/msn)
- [case DPA](/documentation/security/secauthenticationtype/dpa)
- [case RPA](/documentation/security/secauthenticationtype/rpa)
- [case httpBasic](/documentation/security/secauthenticationtype/httpbasic)
- [case httpDigest](/documentation/security/secauthenticationtype/httpdigest)
- [case htmlForm](/documentation/security/secauthenticationtype/htmlform)
- [case `default`](/documentation/security/secauthenticationtype/default)
- [case any](/documentation/security/secauthenticationtype/any)

##### Initializers

- [init?(rawValue: FourCharCode)](/documentation/security/secauthenticationtype/init(rawvalue:))
- [SecPassword](/documentation/security/secpassword)
- [Keychains](/documentation/security/keychains)

#### Creation and Deletion

- [func SecKeychainCreate(UnsafePointer<CChar>, UInt32, UnsafeRawPointer?, Bool, SecAccess?, UnsafeMutablePointer<SecKeychain?>) -> OSStatus](/documentation/security/seckeychaincreate(_:_:_:_:_:_:))
- [func SecKeychainDelete(SecKeychain?) -> OSStatus](/documentation/security/seckeychaindelete(_:))
- [SecKeychain](/documentation/security/seckeychain)
- [func SecKeychainGetTypeID() -> CFTypeID](/documentation/security/seckeychaingettypeid())

#### Locking and Unlocking

- [func SecKeychainLock(SecKeychain?) -> OSStatus](/documentation/security/seckeychainlock(_:))
- [func SecKeychainLockAll() -> OSStatus](/documentation/security/seckeychainlockall())
- [func SecKeychainUnlock(SecKeychain?, UInt32, UnsafeRawPointer?, Bool) -> OSStatus](/documentation/security/seckeychainunlock(_:_:_:_:))

#### Settings

- [func SecKeychainSetSettings(SecKeychain?, UnsafePointer<SecKeychainSettings>) -> OSStatus](/documentation/security/seckeychainsetsettings(_:_:))
- [func SecKeychainCopySettings(SecKeychain?, UnsafeMutablePointer<SecKeychainSettings>) -> OSStatus](/documentation/security/seckeychaincopysettings(_:_:))
- [SecKeychainSettings](/documentation/security/seckeychainsettings)

##### Initializers

- [init()](/documentation/security/seckeychainsettings/init())
- [init(version: UInt32, lockOnSleep: DarwinBoolean, useLockInterval: DarwinBoolean, lockInterval: UInt32)](/documentation/security/seckeychainsettings/init(version:lockonsleep:uselockinterval:lockinterval:))

##### Instance Properties

- [var lockInterval: UInt32](/documentation/security/seckeychainsettings/lockinterval)
- [var lockOnSleep: DarwinBoolean](/documentation/security/seckeychainsettings/lockonsleep)
- [var useLockInterval: DarwinBoolean](/documentation/security/seckeychainsettings/uselockinterval)
- [var version: UInt32](/documentation/security/seckeychainsettings/version)
- [var SEC_KEYCHAIN_SETTINGS_VERS1: Int32](/documentation/security/sec_keychain_settings_vers1)

#### Keychain Management

- [func SecKeychainGetVersion(UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/security/seckeychaingetversion(_:))
- [func SecKeychainOpen(UnsafePointer<CChar>, UnsafeMutablePointer<SecKeychain?>) -> OSStatus](/documentation/security/seckeychainopen(_:_:))
- [func SecKeychainSetDefault(SecKeychain?) -> OSStatus](/documentation/security/seckeychainsetdefault(_:))
- [func SecKeychainCopyDefault(UnsafeMutablePointer<SecKeychain?>) -> OSStatus](/documentation/security/seckeychaincopydefault(_:))
- [func SecKeychainGetPath(SecKeychain?, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<CChar>) -> OSStatus](/documentation/security/seckeychaingetpath(_:_:_:))
- [func SecKeychainGetStatus(SecKeychain?, UnsafeMutablePointer<SecKeychainStatus>) -> OSStatus](/documentation/security/seckeychaingetstatus(_:_:))
- [SecKeychainStatus](/documentation/security/seckeychainstatus)
- [SecKeychainStatus Values](/documentation/security/seckeychainstatus-values)

##### Constants

- [var kSecUnlockStateStatus: UInt32](/documentation/security/ksecunlockstatestatus)
- [var kSecReadPermStatus: UInt32](/documentation/security/ksecreadpermstatus)
- [var kSecWritePermStatus: UInt32](/documentation/security/ksecwritepermstatus)

#### Search

- [func SecKeychainSetSearchList(CFArray) -> OSStatus](/documentation/security/seckeychainsetsearchlist(_:))
- [func SecKeychainCopySearchList(UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/seckeychaincopysearchlist(_:))
- [SecKeychainSearch](/documentation/security/seckeychainsearch)

#### User Interaction

- [func SecKeychainSetUserInteractionAllowed(Bool) -> OSStatus](/documentation/security/seckeychainsetuserinteractionallowed(_:))
- [func SecKeychainGetUserInteractionAllowed(UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/security/seckeychaingetuserinteractionallowed(_:))

#### Callbacks

- [func SecKeychainAddCallback(SecKeychainCallback, SecKeychainEventMask, UnsafeMutableRawPointer?) -> OSStatus](/documentation/security/seckeychainaddcallback(_:_:_:))
- [func SecKeychainRemoveCallback(SecKeychainCallback) -> OSStatus](/documentation/security/seckeychainremovecallback(_:))
- [SecKeychainCallback](/documentation/security/seckeychaincallback)
- [SecKeychainCallbackInfo](/documentation/security/seckeychaincallbackinfo)

##### Instance Properties

- [var item: Unmanaged<SecKeychainItem>](/documentation/security/seckeychaincallbackinfo/item)
- [var keychain: Unmanaged<SecKeychain>](/documentation/security/seckeychaincallbackinfo/keychain)
- [var pid: pid_t](/documentation/security/seckeychaincallbackinfo/pid)
- [var version: UInt32](/documentation/security/seckeychaincallbackinfo/version)

##### Initializers

- [init(version: UInt32, item: Unmanaged<SecKeychainItem>, keychain: Unmanaged<SecKeychain>, pid: pid_t)](/documentation/security/seckeychaincallbackinfo/init(version:item:keychain:pid:))
- [SecKeychainEvent](/documentation/security/seckeychainevent)

##### Constants

- [case lockEvent](/documentation/security/seckeychainevent/lockevent)
- [case unlockEvent](/documentation/security/seckeychainevent/unlockevent)
- [case addEvent](/documentation/security/seckeychainevent/addevent)
- [case deleteEvent](/documentation/security/seckeychainevent/deleteevent)
- [case updateEvent](/documentation/security/seckeychainevent/updateevent)
- [case passwordChangedEvent](/documentation/security/seckeychainevent/passwordchangedevent)
- [case defaultChangedEvent](/documentation/security/seckeychainevent/defaultchangedevent)
- [case dataAccessEvent](/documentation/security/seckeychainevent/dataaccessevent)
- [case keychainListChangedEvent](/documentation/security/seckeychainevent/keychainlistchangedevent)
- [case trustSettingsChangedEvent](/documentation/security/seckeychainevent/trustsettingschangedevent)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/seckeychainevent/init(rawvalue:))
- [SecKeychainEventMask](/documentation/security/seckeychaineventmask)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/seckeychaineventmask/init(rawvalue:))

##### Constants

- [static var lockEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/lockeventmask)
- [static var unlockEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/unlockeventmask)
- [static var addEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/addeventmask)
- [static var deleteEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/deleteeventmask)
- [static var updateEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/updateeventmask)
- [static var passwordChangedEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/passwordchangedeventmask)
- [static var defaultChangedEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/defaultchangedeventmask)
- [static var dataAccessEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/dataaccesseventmask)
- [static var keychainListChangedMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/keychainlistchangedmask)
- [static var trustSettingsChangedEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/trustsettingschangedeventmask)
- [static var everyEventMask: SecKeychainEventMask](/documentation/security/seckeychaineventmask/everyeventmask)

#### Preference Domains

- [func SecKeychainGetPreferenceDomain(UnsafeMutablePointer<SecPreferencesDomain>) -> OSStatus](/documentation/security/seckeychaingetpreferencedomain(_:))
- [func SecKeychainSetPreferenceDomain(SecPreferencesDomain) -> OSStatus](/documentation/security/seckeychainsetpreferencedomain(_:))
- [func SecKeychainCopyDomainDefault(SecPreferencesDomain, UnsafeMutablePointer<SecKeychain?>) -> OSStatus](/documentation/security/seckeychaincopydomaindefault(_:_:))
- [func SecKeychainSetDomainDefault(SecPreferencesDomain, SecKeychain?) -> OSStatus](/documentation/security/seckeychainsetdomaindefault(_:_:))
- [func SecKeychainCopyDomainSearchList(SecPreferencesDomain, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/seckeychaincopydomainsearchlist(_:_:))
- [func SecKeychainSetDomainSearchList(SecPreferencesDomain, CFArray) -> OSStatus](/documentation/security/seckeychainsetdomainsearchlist(_:_:))
- [SecPreferencesDomain](/documentation/security/secpreferencesdomain)

##### Constants

- [case user](/documentation/security/secpreferencesdomain/user)
- [case system](/documentation/security/secpreferencesdomain/system)
- [case common](/documentation/security/secpreferencesdomain/common)
- [case dynamic](/documentation/security/secpreferencesdomain/dynamic)

##### Initializers

- [init?(rawValue: Int32)](/documentation/security/secpreferencesdomain/init(rawvalue:))

#### Access

- [func SecKeychainSetAccess(SecKeychain?, SecAccess) -> OSStatus](/documentation/security/seckeychainsetaccess(_:_:))
- [func SecKeychainCopyAccess(SecKeychain?, UnsafeMutablePointer<SecAccess?>) -> OSStatus](/documentation/security/seckeychaincopyaccess(_:_:))
- [Access Control Lists](/documentation/security/access-control-lists)

#### Access Creation

- [func SecAccessCreate(CFString, CFArray?, UnsafeMutablePointer<SecAccess?>) -> OSStatus](/documentation/security/secaccesscreate(_:_:_:))
- [func SecAccessCreateWithOwnerAndACL(uid_t, gid_t, SecAccessOwnerType, CFArray?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecAccess?](/documentation/security/secaccesscreatewithownerandacl(_:_:_:_:_:))
- [SecAccessOwnerType](/documentation/security/secaccessownertype)
- [SecAccessOwnerType Values](/documentation/security/secaccessownertype-values)

##### Constants

- [var kSecUseOnlyUID: Int](/documentation/security/ksecuseonlyuid)
- [var kSecUseOnlyGID: Int](/documentation/security/ksecuseonlygid)
- [var kSecHonorRoot: Int](/documentation/security/ksechonorroot)
- [var kSecMatchBits: Int](/documentation/security/ksecmatchbits)
- [SecAccess](/documentation/security/secaccess)
- [func SecAccessGetTypeID() -> CFTypeID](/documentation/security/secaccessgettypeid())

#### Access Query

- [func SecAccessCopyACLList(SecAccess, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/secaccesscopyacllist(_:_:))
- [func SecAccessCopyMatchingACLList(SecAccess, CFTypeRef) -> CFArray?](/documentation/security/secaccesscopymatchingacllist(_:_:))
- [func SecAccessCopyOwnerAndACL(SecAccess, UnsafeMutablePointer<uid_t>?, UnsafeMutablePointer<gid_t>?, UnsafeMutablePointer<SecAccessOwnerType>?, UnsafeMutablePointer<CFArray?>?) -> OSStatus](/documentation/security/secaccesscopyownerandacl(_:_:_:_:_:))

#### Access Control List Entries

- [func SecACLCreateWithSimpleContents(SecAccess, CFArray?, CFString, SecKeychainPromptSelector, UnsafeMutablePointer<SecACL?>) -> OSStatus](/documentation/security/secaclcreatewithsimplecontents(_:_:_:_:_:))
- [func SecACLRemove(SecACL) -> OSStatus](/documentation/security/secaclremove(_:))
- [ACL Authorization Keys](/documentation/security/acl-authorization-keys)

##### Constants

- [let kSecACLAuthorizationAny: CFString](/documentation/security/ksecaclauthorizationany)
- [let kSecACLAuthorizationLogin: CFString](/documentation/security/ksecaclauthorizationlogin)
- [let kSecACLAuthorizationGenKey: CFString](/documentation/security/ksecaclauthorizationgenkey)
- [let kSecACLAuthorizationDelete: CFString](/documentation/security/ksecaclauthorizationdelete)
- [let kSecACLAuthorizationExportWrapped: CFString](/documentation/security/ksecaclauthorizationexportwrapped)
- [let kSecACLAuthorizationExportClear: CFString](/documentation/security/ksecaclauthorizationexportclear)
- [let kSecACLAuthorizationImportWrapped: CFString](/documentation/security/ksecaclauthorizationimportwrapped)
- [let kSecACLAuthorizationImportClear: CFString](/documentation/security/ksecaclauthorizationimportclear)
- [let kSecACLAuthorizationSign: CFString](/documentation/security/ksecaclauthorizationsign)
- [let kSecACLAuthorizationEncrypt: CFString](/documentation/security/ksecaclauthorizationencrypt)
- [let kSecACLAuthorizationDecrypt: CFString](/documentation/security/ksecaclauthorizationdecrypt)
- [let kSecACLAuthorizationMAC: CFString](/documentation/security/ksecaclauthorizationmac)
- [let kSecACLAuthorizationDerive: CFString](/documentation/security/ksecaclauthorizationderive)
- [let kSecACLAuthorizationKeychainCreate: CFString](/documentation/security/ksecaclauthorizationkeychaincreate)
- [let kSecACLAuthorizationKeychainDelete: CFString](/documentation/security/ksecaclauthorizationkeychaindelete)
- [let kSecACLAuthorizationKeychainItemRead: CFString](/documentation/security/ksecaclauthorizationkeychainitemread)
- [let kSecACLAuthorizationKeychainItemInsert: CFString](/documentation/security/ksecaclauthorizationkeychainiteminsert)
- [let kSecACLAuthorizationKeychainItemModify: CFString](/documentation/security/ksecaclauthorizationkeychainitemmodify)
- [let kSecACLAuthorizationKeychainItemDelete: CFString](/documentation/security/ksecaclauthorizationkeychainitemdelete)
- [let kSecACLAuthorizationChangeACL: CFString](/documentation/security/ksecaclauthorizationchangeacl)
- [let kSecACLAuthorizationChangeOwner: CFString](/documentation/security/ksecaclauthorizationchangeowner)
- [let kSecACLAuthorizationIntegrity: CFString](/documentation/security/ksecaclauthorizationintegrity)
- [let kSecACLAuthorizationPartitionID: CFString](/documentation/security/ksecaclauthorizationpartitionid)
- [SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector)

##### Constants

- [static var requirePassphase: SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector/requirepassphase)
- [static var unsigned: SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector/unsigned)
- [static var unsignedAct: SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector/unsignedact)
- [static var invalid: SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector/invalid)
- [static var invalidAct: SecKeychainPromptSelector](/documentation/security/seckeychainpromptselector/invalidact)

##### Initializers

- [init(rawValue: uint16)](/documentation/security/seckeychainpromptselector/init(rawvalue:))
- [SecACL](/documentation/security/secacl)
- [func SecACLGetTypeID() -> CFTypeID](/documentation/security/secaclgettypeid())

#### Access Control List Configuration

- [func SecACLCopyContents(SecACL, UnsafeMutablePointer<CFArray?>, UnsafeMutablePointer<CFString?>, UnsafeMutablePointer<SecKeychainPromptSelector>) -> OSStatus](/documentation/security/secaclcopycontents(_:_:_:_:))
- [func SecACLSetContents(SecACL, CFArray?, CFString, SecKeychainPromptSelector) -> OSStatus](/documentation/security/secaclsetcontents(_:_:_:_:))
- [func SecACLCopyAuthorizations(SecACL) -> CFArray](/documentation/security/secaclcopyauthorizations(_:))
- [func SecACLUpdateAuthorizations(SecACL, CFArray) -> OSStatus](/documentation/security/secaclupdateauthorizations(_:_:))

#### Trusted Applications

- [func SecTrustedApplicationCreateFromPath(UnsafePointer<CChar>?, UnsafeMutablePointer<SecTrustedApplication?>) -> OSStatus](/documentation/security/sectrustedapplicationcreatefrompath(_:_:))
- [func SecTrustedApplicationCopyData(SecTrustedApplication, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/sectrustedapplicationcopydata(_:_:))
- [func SecTrustedApplicationSetData(SecTrustedApplication, CFData) -> OSStatus](/documentation/security/sectrustedapplicationsetdata(_:_:))
- [SecTrustedApplication](/documentation/security/sectrustedapplication)
- [func SecTrustedApplicationGetTypeID() -> CFTypeID](/documentation/security/sectrustedapplicationgettypeid())

#### Keychain Item Access

- [func SecKeychainItemSetAccess(SecKeychainItem, SecAccess) -> OSStatus](/documentation/security/seckeychainitemsetaccess(_:_:))
- [func SecKeychainItemCopyAccess(SecKeychainItem, UnsafeMutablePointer<SecAccess?>) -> OSStatus](/documentation/security/seckeychainitemcopyaccess(_:_:))
- [Preventing Insecure Network Connections](/documentation/security/preventing-insecure-network-connections)

### Evaluation

- [Identifying the Source of Blocked Connections](/documentation/security/identifying-the-source-of-blocked-connections)

### Exceptions

- [NSAppTransportSecurity](/documentation/bundleresources/information-property-list/nsapptransportsecurity)

## Secure code

- [Code Signing Services](/documentation/security/code-signing-services)

### Code Objects

- [SecCode](/documentation/security/seccode)
- [func SecCodeCopySelf(SecCSFlags, UnsafeMutablePointer<SecCode?>) -> OSStatus](/documentation/security/seccodecopyself(_:_:))
- [SecCSFlags](/documentation/security/seccsflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/seccsflags/init(rawvalue:))

#### Constants

- [static var considerExpiration: SecCSFlags](/documentation/security/seccsflags/considerexpiration)
- [static var enforceRevocationChecks: SecCSFlags](/documentation/security/seccsflags/enforcerevocationchecks)
- [static var checkTrustedAnchors: SecCSFlags](/documentation/security/seccsflags/checktrustedanchors)
- [static var noNetworkAccess: SecCSFlags](/documentation/security/seccsflags/nonetworkaccess)
- [static var reportProgress: SecCSFlags](/documentation/security/seccsflags/reportprogress)
- [static var quickCheck: SecCSFlags](/documentation/security/seccsflags/quickcheck)

#### Type Properties

- [static var applyEmbeddedPolicy: SecCSFlags](/documentation/security/seccsflags/applyembeddedpolicy)
- [static var matchGuestRequirementInKernel: SecCSFlags](/documentation/security/seccsflags/matchguestrequirementinkernel)
- [static var stripDisallowedXattrs: SecCSFlags](/documentation/security/seccsflags/stripdisallowedxattrs)
- [func SecCodeGetTypeID() -> CFTypeID](/documentation/security/seccodegettypeid())

### Static Code

- [SecStaticCode](/documentation/security/secstaticcode)
- [func SecStaticCodeCreateWithPath(CFURL, SecCSFlags, UnsafeMutablePointer<SecStaticCode?>) -> OSStatus](/documentation/security/secstaticcodecreatewithpath(_:_:_:))
- [func SecStaticCodeCreateWithPathAndAttributes(CFURL, SecCSFlags, CFDictionary, UnsafeMutablePointer<SecStaticCode?>) -> OSStatus](/documentation/security/secstaticcodecreatewithpathandattributes(_:_:_:_:))
- [Code Attributes](/documentation/security/code-attributes)

#### Constants

- [let kSecCodeAttributeArchitecture: CFString](/documentation/security/kseccodeattributearchitecture)
- [let kSecCodeAttributeSubarchitecture: CFString](/documentation/security/kseccodeattributesubarchitecture)
- [let kSecCodeAttributeBundleVersion: CFString](/documentation/security/kseccodeattributebundleversion)
- [let kSecCodeAttributeUniversalFileOffset: CFString](/documentation/security/kseccodeattributeuniversalfileoffset)
- [func SecStaticCodeGetTypeID() -> CFTypeID](/documentation/security/secstaticcodegettypeid())

### Working with Code Objects

- [func SecCodeCopyPath(SecStaticCode, SecCSFlags, UnsafeMutablePointer<CFURL?>) -> OSStatus](/documentation/security/seccodecopypath(_:_:_:))
- [func SecCodeCopyStaticCode(SecCode, SecCSFlags, UnsafeMutablePointer<SecStaticCode?>) -> OSStatus](/documentation/security/seccodecopystaticcode(_:_:_:))
- [Code Signing Architecture Flags](/documentation/security/code-signing-architecture-flags)

#### Constants

- [var kSecCSUseAllArchitectures: UInt32](/documentation/security/kseccsuseallarchitectures)

### Code Signatures

- [func SecCodeCopySigningInformation(SecStaticCode, SecCSFlags, UnsafeMutablePointer<CFDictionary?>) -> OSStatus](/documentation/security/seccodecopysigninginformation(_:_:_:))
- [Code Signing Information Flags](/documentation/security/code-signing-information-flags)

#### Constants

- [var kSecCSInternalInformation: UInt32](/documentation/security/kseccsinternalinformation)
- [var kSecCSSigningInformation: UInt32](/documentation/security/kseccssigninginformation)
- [var kSecCSRequirementInformation: UInt32](/documentation/security/kseccsrequirementinformation)
- [var kSecCSDynamicInformation: UInt32](/documentation/security/kseccsdynamicinformation)
- [var kSecCSContentInformation: UInt32](/documentation/security/kseccscontentinformation)
- [var kSecCSSkipResourceDirectory: UInt32](/documentation/security/kseccsskipresourcedirectory)
- [var kSecCSCalculateCMSDigest: UInt32](/documentation/security/kseccscalculatecmsdigest)
- [Signing Information Dictionary Keys](/documentation/security/signing-information-dictionary-keys)

#### Constants

- [let kSecCodeInfoCdHashes: CFString](/documentation/security/kseccodeinfocdhashes)
- [let kSecCodeInfoCertificates: CFString](/documentation/security/kseccodeinfocertificates)
- [let kSecCodeInfoChangedFiles: CFString](/documentation/security/kseccodeinfochangedfiles)
- [let kSecCodeInfoCMS: CFString](/documentation/security/kseccodeinfocms)
- [let kSecCodeInfoDesignatedRequirement: CFString](/documentation/security/kseccodeinfodesignatedrequirement)
- [let kSecCodeInfoDigestAlgorithm: CFString](/documentation/security/kseccodeinfodigestalgorithm)
- [let kSecCodeInfoDigestAlgorithms: CFString](/documentation/security/kseccodeinfodigestalgorithms)
- [let kSecCodeInfoEntitlements: CFString](/documentation/security/kseccodeinfoentitlements)
- [let kSecCodeInfoEntitlementsDict: CFString](/documentation/security/kseccodeinfoentitlementsdict)
- [let kSecCodeInfoFormat: CFString](/documentation/security/kseccodeinfoformat)
- [let kSecCodeInfoFlags: CFString](/documentation/security/kseccodeinfoflags)
- [let kSecCodeInfoIdentifier: CFString](/documentation/security/kseccodeinfoidentifier)
- [let kSecCodeInfoImplicitDesignatedRequirement: CFString](/documentation/security/kseccodeinfoimplicitdesignatedrequirement)
- [let kSecCodeInfoMainExecutable: CFString](/documentation/security/kseccodeinfomainexecutable)
- [let kSecCodeInfoPList: CFString](/documentation/security/kseccodeinfoplist)
- [let kSecCodeInfoPlatformIdentifier: CFString](/documentation/security/kseccodeinfoplatformidentifier)
- [let kSecCodeInfoRequirements: CFString](/documentation/security/kseccodeinforequirements)
- [let kSecCodeInfoRequirementData: CFString](/documentation/security/kseccodeinforequirementdata)
- [let kSecCodeInfoRuntimeVersion: CFString](/documentation/security/kseccodeinforuntimeversion)
- [let kSecCodeInfoSource: CFString](/documentation/security/kseccodeinfosource)
- [let kSecCodeInfoStatus: CFString](/documentation/security/kseccodeinfostatus)
- [let kSecCodeInfoTeamIdentifier: CFString](/documentation/security/kseccodeinfoteamidentifier)
- [let kSecCodeInfoTime: CFString](/documentation/security/kseccodeinfotime)
- [let kSecCodeInfoTimestamp: CFString](/documentation/security/kseccodeinfotimestamp)
- [let kSecCodeInfoTrust: CFString](/documentation/security/kseccodeinfotrust)
- [let kSecCodeInfoUnique: CFString](/documentation/security/kseccodeinfounique)
- [SecCodeSignatureFlags](/documentation/security/seccodesignatureflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/seccodesignatureflags/init(rawvalue:))

#### Constants

- [static var host: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/host)
- [static var adhoc: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/adhoc)
- [static var forceHard: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/forcehard)
- [static var forceKill: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/forcekill)
- [static var forceExpiration: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/forceexpiration)
- [static var enforcement: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/enforcement)
- [static var libraryValidation: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/libraryvalidation)
- [static var restrict: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/restrict)
- [static var runtime: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/runtime)

#### Type Properties

- [static var linkerSigned: SecCodeSignatureFlags](/documentation/security/seccodesignatureflags/linkersigned)
- [SecCSDigestAlgorithm](/documentation/security/seccsdigestalgorithm)

#### Enumeration Cases

- [case codeSignatureHashSHA1](/documentation/security/seccsdigestalgorithm/codesignaturehashsha1)
- [case codeSignatureHashSHA256](/documentation/security/seccsdigestalgorithm/codesignaturehashsha256)
- [case codeSignatureHashSHA256Truncated](/documentation/security/seccsdigestalgorithm/codesignaturehashsha256truncated)
- [case codeSignatureHashSHA384](/documentation/security/seccsdigestalgorithm/codesignaturehashsha384)
- [case codeSignatureHashSHA512](/documentation/security/seccsdigestalgorithm/codesignaturehashsha512)
- [case codeSignatureNoHash](/documentation/security/seccsdigestalgorithm/codesignaturenohash)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/security/seccsdigestalgorithm/init(rawvalue:))

### Code Requirements

- [Applying Code Requirements](/documentation/security/applying-code-requirements)
- [func SecCodeCopyDesignatedRequirement(SecStaticCode, SecCSFlags, UnsafeMutablePointer<SecRequirement?>) -> OSStatus](/documentation/security/seccodecopydesignatedrequirement(_:_:_:))
- [SecRequirement](/documentation/security/secrequirement)
- [func SecRequirementGetTypeID() -> CFTypeID](/documentation/security/secrequirementgettypeid())
- [SecRequirementType](/documentation/security/secrequirementtype)

#### Constants

- [case hostRequirementType](/documentation/security/secrequirementtype/hostrequirementtype)
- [case guestRequirementType](/documentation/security/secrequirementtype/guestrequirementtype)
- [case designatedRequirementType](/documentation/security/secrequirementtype/designatedrequirementtype)
- [case libraryRequirementType](/documentation/security/secrequirementtype/libraryrequirementtype)
- [case pluginRequirementType](/documentation/security/secrequirementtype/pluginrequirementtype)
- [case invalidRequirementType](/documentation/security/secrequirementtype/invalidrequirementtype)
- [static var requirementTypeCount: SecRequirementType](/documentation/security/secrequirementtype/requirementtypecount)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/security/secrequirementtype/init(rawvalue:))

### Code Requirements as Data

- [func SecRequirementCopyData(SecRequirement, SecCSFlags, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/secrequirementcopydata(_:_:_:))
- [func SecRequirementCreateWithData(CFData, SecCSFlags, UnsafeMutablePointer<SecRequirement?>) -> OSStatus](/documentation/security/secrequirementcreatewithdata(_:_:_:))

### Code Requirements as Text

- [func SecRequirementCopyString(SecRequirement, SecCSFlags, UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/security/secrequirementcopystring(_:_:_:))
- [func SecRequirementCreateWithString(CFString, SecCSFlags, UnsafeMutablePointer<SecRequirement?>) -> OSStatus](/documentation/security/secrequirementcreatewithstring(_:_:_:))
- [func SecRequirementCreateWithStringAndErrors(CFString, SecCSFlags, UnsafeMutablePointer<Unmanaged<CFError>?>?, UnsafeMutablePointer<SecRequirement?>) -> OSStatus](/documentation/security/secrequirementcreatewithstringanderrors(_:_:_:_:))

### Guest Code

- [Hosting Guest Code](/documentation/security/hosting-guest-code)
- [func SecCodeCopyGuestWithAttributes(SecCode?, CFDictionary?, SecCSFlags, UnsafeMutablePointer<SecCode?>) -> OSStatus](/documentation/security/seccodecopyguestwithattributes(_:_:_:_:))
- [Null Guest Handle](/documentation/security/null-guest-handle)

#### Constants

- [var kSecNoGuest: SecGuestRef](/documentation/security/ksecnoguest)
- [SecCodeStatus](/documentation/security/seccodestatus)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/seccodestatus/init(rawvalue:))

#### Constants

- [static var valid: SecCodeStatus](/documentation/security/seccodestatus/valid)
- [static var hard: SecCodeStatus](/documentation/security/seccodestatus/hard)
- [static var kill: SecCodeStatus](/documentation/security/seccodestatus/kill)
- [static var debugged: SecCodeStatus](/documentation/security/seccodestatus/debugged)
- [static var platform: SecCodeStatus](/documentation/security/seccodestatus/platform)
- [Guest Creation Flags](/documentation/security/guest-creation-flags)

#### Constants

- [var kSecCSDedicatedHost: UInt32](/documentation/security/kseccsdedicatedhost)
- [var kSecCSGenerateGuestHash: UInt32](/documentation/security/kseccsgenerateguesthash)
- [Guest Attribute Dictionary Keys](/documentation/security/guest-attribute-dictionary-keys)

#### Constants

- [let kSecGuestAttributeArchitecture: CFString](/documentation/security/ksecguestattributearchitecture)
- [let kSecGuestAttributeAudit: CFString](/documentation/security/ksecguestattributeaudit)
- [let kSecGuestAttributeCanonical: CFString](/documentation/security/ksecguestattributecanonical)
- [let kSecGuestAttributeDynamicCode: CFString](/documentation/security/ksecguestattributedynamiccode)
- [let kSecGuestAttributeDynamicCodeInfoPlist: CFString](/documentation/security/ksecguestattributedynamiccodeinfoplist)
- [let kSecGuestAttributeHash: CFString](/documentation/security/ksecguestattributehash)
- [let kSecGuestAttributeMachPort: CFString](/documentation/security/ksecguestattributemachport)
- [let kSecGuestAttributePid: CFString](/documentation/security/ksecguestattributepid)
- [let kSecGuestAttributeSubarchitecture: CFString](/documentation/security/ksecguestattributesubarchitecture)
- [SecGuestRef](/documentation/security/secguestref)

### Guest Management

- [func SecCodeCopyHost(SecCode, SecCSFlags, UnsafeMutablePointer<SecCode?>) -> OSStatus](/documentation/security/seccodecopyhost(_:_:_:))
- [func SecCodeMapMemory(SecStaticCode, SecCSFlags) -> OSStatus](/documentation/security/seccodemapmemory(_:_:))

### Tasks

- [func SecTaskCreateFromSelf(CFAllocator?) -> SecTask?](/documentation/security/sectaskcreatefromself(_:))
- [func SecTaskCreateWithAuditToken(CFAllocator?, audit_token_t) -> SecTask?](/documentation/security/sectaskcreatewithaudittoken(_:_:))
- [SecTask](/documentation/security/sectask)
- [func SecTaskGetTypeID() -> CFTypeID](/documentation/security/sectaskgettypeid())
- [func SecTaskCopySigningIdentifier(SecTask, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFString?](/documentation/security/sectaskcopysigningidentifier(_:_:))
- [func SecTaskCopyValueForEntitlement(SecTask, CFString, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFTypeRef?](/documentation/security/sectaskcopyvalueforentitlement(_:_:_:))
- [func SecTaskCopyValuesForEntitlements(SecTask, CFArray, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFDictionary?](/documentation/security/sectaskcopyvaluesforentitlements(_:_:_:))

### Code Signature Validity

- [func SecCodeCheckValidity(SecCode, SecCSFlags, SecRequirement?) -> OSStatus](/documentation/security/seccodecheckvalidity(_:_:_:))
- [func SecCodeCheckValidityWithErrors(SecCode, SecCSFlags, SecRequirement?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> OSStatus](/documentation/security/seccodecheckvaliditywitherrors(_:_:_:_:))
- [func SecStaticCodeCheckValidity(SecStaticCode, SecCSFlags, SecRequirement?) -> OSStatus](/documentation/security/secstaticcodecheckvalidity(_:_:_:))
- [func SecStaticCodeCheckValidityWithErrors(SecStaticCode, SecCSFlags, SecRequirement?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> OSStatus](/documentation/security/secstaticcodecheckvaliditywitherrors(_:_:_:_:))
- [Static Code Validation Flags](/documentation/security/static-code-validation-flags)

#### Constants

- [var kSecCSCheckAllArchitectures: UInt32](/documentation/security/kseccscheckallarchitectures)
- [var kSecCSDoNotValidateExecutable: UInt32](/documentation/security/kseccsdonotvalidateexecutable)
- [var kSecCSDoNotValidateResources: UInt32](/documentation/security/kseccsdonotvalidateresources)
- [var kSecCSBasicValidateOnly: UInt32](/documentation/security/kseccsbasicvalidateonly)
- [var kSecCSCheckNestedCode: UInt32](/documentation/security/kseccschecknestedcode)
- [var kSecCSStrictValidate: UInt32](/documentation/security/kseccsstrictvalidate)
- [var kSecCSFullReport: UInt32](/documentation/security/kseccsfullreport)
- [var kSecCSCheckGatekeeperArchitectures: UInt32](/documentation/security/kseccscheckgatekeeperarchitectures)
- [var kSecCSRestrictSymlinks: UInt32](/documentation/security/kseccsrestrictsymlinks)
- [var kSecCSRestrictToAppLike: UInt32](/documentation/security/kseccsrestricttoapplike)
- [var kSecCSRestrictSidebandData: UInt32](/documentation/security/kseccsrestrictsidebanddata)
- [var kSecCSUseSoftwareSigningCert: UInt32](/documentation/security/kseccsusesoftwaresigningcert)
- [var kSecCSValidatePEH: UInt32](/documentation/security/kseccsvalidatepeh)
- [var kSecCSSingleThreaded: UInt32](/documentation/security/kseccssinglethreaded)

### Result Codes

- [Code Signing Services Result Codes](/documentation/security/code-signing-services-result-codes)

#### Code-signing format result codes

- [var errSecCSAmbiguousBundleFormat: OSStatus](/documentation/security/errseccsambiguousbundleformat)
- [var errSecCSBadBundleFormat: OSStatus](/documentation/security/errseccsbadbundleformat)
- [var errSecCSBadDictionaryFormat: OSStatus](/documentation/security/errseccsbaddictionaryformat)
- [var errSecCSBadDiskImageFormat: OSStatus](/documentation/security/errseccsbaddiskimageformat)
- [var errSecCSBadObjectFormat: OSStatus](/documentation/security/errseccsbadobjectformat)

#### Code-signing database issue result codes

- [var errSecCSDBAccess: OSStatus](/documentation/security/errseccsdbaccess)
- [var errSecCSDBDenied: OSStatus](/documentation/security/errseccsdbdenied)
- [var errSecCSDbCorrupt: OSStatus](/documentation/security/errseccsdbcorrupt)
- [var errSecCSSigDBAccess: OSStatus](/documentation/security/errseccssigdbaccess)
- [var errSecCSSigDBDenied: OSStatus](/documentation/security/errseccssigdbdenied)

#### Code-signing host protocol issue result codes

- [var errSecCSHostProtocolContradiction: OSStatus](/documentation/security/errseccshostprotocolcontradiction)
- [var errSecCSHostProtocolDedicationError: OSStatus](/documentation/security/errseccshostprotocoldedicationerror)
- [var errSecCSHostProtocolInvalidAttribute: OSStatus](/documentation/security/errseccshostprotocolinvalidattribute)
- [var errSecCSHostProtocolInvalidHash: OSStatus](/documentation/security/errseccshostprotocolinvalidhash)
- [var errSecCSHostProtocolNotProxy: OSStatus](/documentation/security/errseccshostprotocolnotproxy)
- [var errSecCSHostProtocolRelativePath: OSStatus](/documentation/security/errseccshostprotocolrelativepath)
- [var errSecCSHostProtocolStateError: OSStatus](/documentation/security/errseccshostprotocolstateerror)
- [var errSecCSHostProtocolUnrelated: OSStatus](/documentation/security/errseccshostprotocolunrelated)

#### Code-signing signature issue result codes

- [var errSecCSSignatureFailed: OSStatus](/documentation/security/errseccssignaturefailed)
- [var errSecCSSignatureInvalid: OSStatus](/documentation/security/errseccssignatureinvalid)
- [var errSecCSSignatureNotVerifiable: OSStatus](/documentation/security/errseccssignaturenotverifiable)
- [var errSecCSSignatureUnsupported: OSStatus](/documentation/security/errseccssignatureunsupported)
- [var errSecCSUnsigned: OSStatus](/documentation/security/errseccsunsigned)
- [var errSecCSUnsignedNestedCode: OSStatus](/documentation/security/errseccsunsignednestedcode)
- [var errSecCSUnsupportedDigestAlgorithm: OSStatus](/documentation/security/errseccsunsupporteddigestalgorithm)
- [var errSecCSSignatureUntrusted: OSStatus](/documentation/security/errseccssignatureuntrusted)

#### Code-signing file format issue result codes

- [var errSecCSDSStoreSymlink: OSStatus](/documentation/security/errseccsdsstoresymlink)
- [var errSecCSFileHardQuarantined: OSStatus](/documentation/security/errseccsfilehardquarantined)
- [var errSecCSInvalidSymlink: OSStatus](/documentation/security/errseccsinvalidsymlink)
- [var errSecCSNoMainExecutable: OSStatus](/documentation/security/errseccsnomainexecutable)
- [var errSecCSRegularFile: OSStatus](/documentation/security/errseccsregularfile)
- [var errSecCSUnsealedAppRoot: OSStatus](/documentation/security/errseccsunsealedapproot)
- [var errSecCSUnsealedFrameworkRoot: OSStatus](/documentation/security/errseccsunsealedframeworkroot)

#### Code-signing resource issue result codes

- [var errSecCSResourceDirectoryFailed: OSStatus](/documentation/security/errseccsresourcedirectoryfailed)
- [var errSecCSResourceNotSupported: OSStatus](/documentation/security/errseccsresourcenotsupported)
- [var errSecCSResourceRulesInvalid: OSStatus](/documentation/security/errseccsresourcerulesinvalid)
- [var errSecCSResourcesInvalid: OSStatus](/documentation/security/errseccsresourcesinvalid)
- [var errSecCSResourcesNotFound: OSStatus](/documentation/security/errseccsresourcesnotfound)
- [var errSecCSResourcesNotSealed: OSStatus](/documentation/security/errseccsresourcesnotsealed)

#### Other result codes

- [var errSecCSBadCallbackValue: OSStatus](/documentation/security/errseccsbadcallbackvalue)
- [var errSecCSBadFrameworkVersion: OSStatus](/documentation/security/errseccsbadframeworkversion)
- [var errSecCSBadLVArch: OSStatus](/documentation/security/errseccsbadlvarch)
- [var errSecCSBadMainExecutable: OSStatus](/documentation/security/errseccsbadmainexecutable)
- [var errSecCSBadNestedCode: OSStatus](/documentation/security/errseccsbadnestedcode)
- [var errSecCSBadResource: OSStatus](/documentation/security/errseccsbadresource)
- [var errSecCSCMSTooLarge: OSStatus](/documentation/security/errseccscmstoolarge)
- [var errSecCSCancelled: OSStatus](/documentation/security/errseccscancelled)
- [var errSecCSGuestInvalid: OSStatus](/documentation/security/errseccsguestinvalid)
- [var errSecCSHelperFailed: OSStatus](/documentation/security/errseccshelperfailed)
- [var errSecCSHostReject: OSStatus](/documentation/security/errseccshostreject)
- [var errSecCSInfoPlistFailed: OSStatus](/documentation/security/errseccsinfoplistfailed)
- [var errSecCSInternalError: OSStatus](/documentation/security/errseccsinternalerror)
- [var errSecCSInvalidAttributeValues: OSStatus](/documentation/security/errseccsinvalidattributevalues)
- [var errSecCSInvalidFlags: OSStatus](/documentation/security/errseccsinvalidflags)
- [var errSecCSInvalidObjectRef: OSStatus](/documentation/security/errseccsinvalidobjectref)
- [var errSecCSInvalidPlatform: OSStatus](/documentation/security/errseccsinvalidplatform)
- [var errSecCSMultipleGuests: OSStatus](/documentation/security/errseccsmultipleguests)
- [var errSecCSNoMatches: OSStatus](/documentation/security/errseccsnomatches)
- [var errSecCSNoSuchCode: OSStatus](/documentation/security/errseccsnosuchcode)
- [var errSecCSNotAHost: OSStatus](/documentation/security/errseccsnotahost)
- [var errSecCSNotAppLike: OSStatus](/documentation/security/errseccsnotapplike)
- [var errSecCSNotSupported: OSStatus](/documentation/security/errseccsnotsupported)
- [var errSecCSObjectRequired: OSStatus](/documentation/security/errseccsobjectrequired)
- [var errSecCSOutdated: OSStatus](/documentation/security/errseccsoutdated)
- [var errSecCSReqFailed: OSStatus](/documentation/security/errseccsreqfailed)
- [var errSecCSReqInvalid: OSStatus](/documentation/security/errseccsreqinvalid)
- [var errSecCSReqUnsupported: OSStatus](/documentation/security/errseccsrequnsupported)
- [var errSecCSStaticCodeChanged: OSStatus](/documentation/security/errseccsstaticcodechanged)
- [var errSecCSStaticCodeNotFound: OSStatus](/documentation/security/errseccsstaticcodenotfound)
- [var errSecCSTooBig: OSStatus](/documentation/security/errseccstoobig)
- [var errSecCSUnimplemented: OSStatus](/documentation/security/errseccsunimplemented)
- [var errSecCSUnsupportedGuestAttributes: OSStatus](/documentation/security/errseccsunsupportedguestattributes)
- [var errSecCSVetoed: OSStatus](/documentation/security/errseccsvetoed)
- [var errSecCSWeakResourceEnvelope: OSStatus](/documentation/security/errseccsweakresourceenvelope)
- [var errSecCSWeakResourceRules: OSStatus](/documentation/security/errseccsweakresourcerules)
- [var errSecCSBadTeamIdentifier: OSStatus](/documentation/security/errseccsbadteamidentifier)
- [var errSecCSInvalidAssociatedFileData: OSStatus](/documentation/security/errseccsinvalidassociatedfiledata)
- [var errSecCSInvalidTeamIdentifier: OSStatus](/documentation/security/errseccsinvalidteamidentifier)
- [var errSecMultipleExecSegments: OSStatus](/documentation/security/errsecmultipleexecsegments)
- [var errSecCSInvalidEntitlements: OSStatus](/documentation/security/errseccsinvalidentitlements)
- [var errSecCSInvalidRuntimeVersion: OSStatus](/documentation/security/errseccsinvalidruntimeversion)
- [var errSecCSRevokedNotarization: OSStatus](/documentation/security/errseccsrevokednotarization)
- [User Info Dictionary Error Keys](/documentation/security/user-info-dictionary-error-keys)

#### Constants

- [let kSecCFErrorArchitecture: CFString](/documentation/security/kseccferrorarchitecture)
- [let kSecCFErrorPattern: CFString](/documentation/security/kseccferrorpattern)
- [let kSecCFErrorResourceSeal: CFString](/documentation/security/kseccferrorresourceseal)
- [let kSecCFErrorResourceAdded: CFString](/documentation/security/kseccferrorresourceadded)
- [let kSecCFErrorResourceAltered: CFString](/documentation/security/kseccferrorresourcealtered)
- [let kSecCFErrorResourceMissing: CFString](/documentation/security/kseccferrorresourcemissing)
- [let kSecCFErrorResourceSideband: CFString](/documentation/security/kseccferrorresourcesideband)
- [let kSecCFErrorInfoPlist: CFString](/documentation/security/kseccferrorinfoplist)
- [let kSecCFErrorGuestAttributes: CFString](/documentation/security/kseccferrorguestattributes)
- [let kSecCFErrorRequirementSyntax: CFString](/documentation/security/kseccferrorrequirementsyntax)
- [let kSecCFErrorPath: CFString](/documentation/security/kseccferrorpath)
- [Notarizing macOS software before distribution](/documentation/security/notarizing-macos-software-before-distribution)

### Notarization

- [Customizing the notarization workflow](/documentation/security/customizing-the-notarization-workflow)

#### Automation

- [Customizing the Xcode archive process](/documentation/security/customizing-the-xcode-archive-process)
- [Resolving common notarization issues](/documentation/security/resolving-common-notarization-issues)
- [Preparing your app to work with pointer authentication](/documentation/security/preparing-your-app-to-work-with-pointer-authentication)
- [App Sandbox](/documentation/security/app-sandbox)

### Essentials

- [App Sandbox Entitlement](/documentation/bundleresources/entitlements/com.apple.security.app-sandbox)
- [Protecting user data with App Sandbox](/documentation/security/protecting-user-data-with-app-sandbox)
- [Embedding a command-line tool in a sandboxed app](/documentation/xcode/embedding-a-helper-tool-in-a-sandboxed-app)
- [Discovering and diagnosing App Sandbox violations](/documentation/security/discovering-and-diagnosing-app-sandbox-violations)

### Network

- [com.apple.security.network.server](/documentation/bundleresources/entitlements/com.apple.security.network.server)
- [com.apple.security.network.client](/documentation/bundleresources/entitlements/com.apple.security.network.client)

### Hardware

- [Camera entitlement](/documentation/bundleresources/entitlements/com.apple.security.device.camera)
- [com.apple.security.device.microphone](/documentation/bundleresources/entitlements/com.apple.security.device.microphone)
- [com.apple.security.device.usb](/documentation/bundleresources/entitlements/com.apple.security.device.usb)
- [com.apple.security.print](/documentation/bundleresources/entitlements/com.apple.security.print)
- [com.apple.security.device.bluetooth](/documentation/bundleresources/entitlements/com.apple.security.device.bluetooth)

### App Data

- [Address book entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.addressbook)
- [Location entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.location)
- [Calendars entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.calendars)

### File Access

- [Accessing files from the macOS App Sandbox](/documentation/security/accessing-files-from-the-macos-app-sandbox)
- [Migrating your app’s files to its App Sandbox container](/documentation/security/migrating-your-app-s-files-to-its-app-sandbox-container)
- [com.apple.security.files.user-selected.read-only](/documentation/bundleresources/entitlements/com.apple.security.files.user-selected.read-only)
- [com.apple.security.files.user-selected.read-write](/documentation/bundleresources/entitlements/com.apple.security.files.user-selected.read-write)
- [com.apple.security.files.downloads.read-only](/documentation/bundleresources/entitlements/com.apple.security.files.downloads.read-only)
- [com.apple.security.files.downloads.read-write](/documentation/bundleresources/entitlements/com.apple.security.files.downloads.read-write)
- [com.apple.security.assets.pictures.read-only](/documentation/bundleresources/entitlements/com.apple.security.assets.pictures.read-only)
- [com.apple.security.assets.pictures.read-write](/documentation/bundleresources/entitlements/com.apple.security.assets.pictures.read-write)
- [com.apple.security.assets.music.read-only](/documentation/bundleresources/entitlements/com.apple.security.assets.music.read-only)
- [com.apple.security.assets.music.read-write](/documentation/bundleresources/entitlements/com.apple.security.assets.music.read-write)
- [com.apple.security.assets.movies.read-only](/documentation/bundleresources/entitlements/com.apple.security.assets.movies.read-only)
- [com.apple.security.assets.movies.read-write](/documentation/bundleresources/entitlements/com.apple.security.assets.movies.read-write)
- [All files entitlement](/documentation/bundleresources/entitlements/com.apple.security.files.all)
- [NSAppDataUsageDescription](/documentation/bundleresources/information-property-list/nsappdatausagedescription)
- [Hardened Runtime](/documentation/security/hardened-runtime)

### Runtime Exceptions

- [Allow execution of JIT-compiled code entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.allow-jit)
- [Allow Unsigned Executable Memory Entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.allow-unsigned-executable-memory)
- [Allow DYLD environment variables entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.allow-dyld-environment-variables)
- [Disable Library Validation Entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.disable-library-validation)
- [Disable Executable Memory Protection Entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.disable-executable-page-protection)
- [Debugging tool entitlement](/documentation/bundleresources/entitlements/com.apple.security.cs.debugger)

### Resource Access

- [Audio Input Entitlement](/documentation/bundleresources/entitlements/com.apple.security.device.audio-input)
- [Camera entitlement](/documentation/bundleresources/entitlements/com.apple.security.device.camera)
- [Location entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.location)
- [Address book entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.addressbook)
- [Calendars entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.calendars)
- [Photos Library Entitlement](/documentation/bundleresources/entitlements/com.apple.security.personal-information.photos-library)
- [Apple Events Entitlement](/documentation/bundleresources/entitlements/com.apple.security.automation.apple-events)
- [Disabling and Enabling System Integrity Protection](/documentation/security/disabling-and-enabling-system-integrity-protection)
- [Using the latest code signature format](/documentation/xcode/using-the-latest-code-signature-format)
- [Updating Mac Software](/documentation/security/updating-mac-software)
- [TN3125: Inside Code Signing: Provisioning Profiles](/documentation/technotes/tn3125-inside-code-signing-provisioning-profiles)

## Launch environment constraints

- [Applying launch environment and library constraints](/documentation/security/applying-launch-environment-and-library-constraints)
- [Defining launch environment and library constraints](/documentation/security/defining-launch-environment-and-library-constraints)
- [Constraining a tool’s launch environment](/documentation/security/constraining-a-tool's-launch-environment)

## Cryptography

- [Complying with Encryption Export Regulations](/documentation/security/complying-with-encryption-export-regulations)

### Encryption Export Compliance Keys

- [ITSAppUsesNonExemptEncryption](/documentation/bundleresources/information-property-list/itsappusesnonexemptencryption)
- [ITSEncryptionExportComplianceCode](/documentation/bundleresources/information-property-list/itsencryptionexportcompliancecode)
- [Certificate, Key, and Trust Services](/documentation/security/certificate-key-and-trust-services)

### API Components

- [Certificates](/documentation/security/certificates)

#### Essentials

- [Getting a Certificate](/documentation/security/getting-a-certificate)
- [Storing a Certificate in the Keychain](/documentation/security/storing-a-certificate-in-the-keychain)
- [SecCertificate](/documentation/security/seccertificate)
- [func SecCertificateGetTypeID() -> CFTypeID](/documentation/security/seccertificategettypeid())

#### Import and Export

- [Storing a DER-Encoded X.509 Certificate](/documentation/security/storing-a-der-encoded-x-509-certificate)
- [func SecCertificateCreateWithData(CFAllocator?, CFData) -> SecCertificate?](/documentation/security/seccertificatecreatewithdata(_:_:))
- [func SecCertificateCopyData(SecCertificate) -> CFData](/documentation/security/seccertificatecopydata(_:))

#### Certificate Components

- [Examining a Certificate](/documentation/security/examining-a-certificate)
- [func SecCertificateCopySubjectSummary(SecCertificate) -> CFString?](/documentation/security/seccertificatecopysubjectsummary(_:))
- [func SecCertificateCopyCommonName(SecCertificate, UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/security/seccertificatecopycommonname(_:_:))
- [func SecCertificateCopyEmailAddresses(SecCertificate, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/seccertificatecopyemailaddresses(_:_:))
- [func SecCertificateCopyNormalizedIssuerSequence(SecCertificate) -> CFData?](/documentation/security/seccertificatecopynormalizedissuersequence(_:))
- [func SecCertificateCopyNormalizedSubjectSequence(SecCertificate) -> CFData?](/documentation/security/seccertificatecopynormalizedsubjectsequence(_:))
- [func SecCertificateCopySerialNumberData(SecCertificate, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seccertificatecopyserialnumberdata(_:_:))
- [func SecCertificateCopyKey(SecCertificate) -> SecKey?](/documentation/security/seccertificatecopykey(_:))
- [func SecCertificateCopyShortDescription(CFAllocator?, SecCertificate, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFString?](/documentation/security/seccertificatecopyshortdescription(_:_:_:))
- [func SecCertificateCopyLongDescription(CFAllocator?, SecCertificate, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFString?](/documentation/security/seccertificatecopylongdescription(_:_:_:))

#### Detailed Certificate Information

- [Getting Certificate Values](/documentation/security/getting-certificate-values)
- [func SecCertificateCopyValues(SecCertificate, CFArray?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFDictionary?](/documentation/security/seccertificatecopyvalues(_:_:_:))
- [Certificate OIDs](/documentation/security/certificate-oids)

##### Constants

- [let kSecOIDADC_CERT_POLICY: CFString](/documentation/security/ksecoidadc_cert_policy)
- [let kSecOIDAPPLE_CERT_POLICY: CFString](/documentation/security/ksecoidapple_cert_policy)
- [let kSecOIDAPPLE_EKU_CODE_SIGNING: CFString](/documentation/security/ksecoidapple_eku_code_signing)
- [let kSecOIDAPPLE_EKU_CODE_SIGNING_DEV: CFString](/documentation/security/ksecoidapple_eku_code_signing_dev)
- [let kSecOIDAPPLE_EKU_ICHAT_ENCRYPTION: CFString](/documentation/security/ksecoidapple_eku_ichat_encryption)
- [let kSecOIDAPPLE_EKU_ICHAT_SIGNING: CFString](/documentation/security/ksecoidapple_eku_ichat_signing)
- [let kSecOIDAPPLE_EKU_RESOURCE_SIGNING: CFString](/documentation/security/ksecoidapple_eku_resource_signing)
- [let kSecOIDAPPLE_EKU_SYSTEM_IDENTITY: CFString](/documentation/security/ksecoidapple_eku_system_identity)
- [let kSecOIDAPPLE_EXTENSION: CFString](/documentation/security/ksecoidapple_extension)
- [let kSecOIDAPPLE_EXTENSION_AAI_INTERMEDIATE: CFString](/documentation/security/ksecoidapple_extension_aai_intermediate)
- [let kSecOIDAPPLE_EXTENSION_ADC_APPLE_SIGNING: CFString](/documentation/security/ksecoidapple_extension_adc_apple_signing)
- [let kSecOIDAPPLE_EXTENSION_ADC_DEV_SIGNING: CFString](/documentation/security/ksecoidapple_extension_adc_dev_signing)
- [let kSecOIDAPPLE_EXTENSION_APPLEID_INTERMEDIATE: CFString](/documentation/security/ksecoidapple_extension_appleid_intermediate)
- [let kSecOIDAPPLE_EXTENSION_APPLE_SIGNING: CFString](/documentation/security/ksecoidapple_extension_apple_signing)
- [let kSecOIDAPPLE_EXTENSION_CODE_SIGNING: CFString](/documentation/security/ksecoidapple_extension_code_signing)
- [let kSecOIDAPPLE_EXTENSION_INTERMEDIATE_MARKER: CFString](/documentation/security/ksecoidapple_extension_intermediate_marker)
- [let kSecOIDAPPLE_EXTENSION_ITMS_INTERMEDIATE: CFString](/documentation/security/ksecoidapple_extension_itms_intermediate)
- [let kSecOIDAPPLE_EXTENSION_WWDR_INTERMEDIATE: CFString](/documentation/security/ksecoidapple_extension_wwdr_intermediate)
- [let kSecOIDAuthorityInfoAccess: CFString](/documentation/security/ksecoidauthorityinfoaccess)
- [let kSecOIDAuthorityKeyIdentifier: CFString](/documentation/security/ksecoidauthoritykeyidentifier)
- [let kSecOIDBasicConstraints: CFString](/documentation/security/ksecoidbasicconstraints)
- [let kSecOIDBiometricInfo: CFString](/documentation/security/ksecoidbiometricinfo)
- [let kSecOIDCSSMKeyStruct: CFString](/documentation/security/ksecoidcssmkeystruct)
- [let kSecOIDCertIssuer: CFString](/documentation/security/ksecoidcertissuer)
- [let kSecOIDCertificatePolicies: CFString](/documentation/security/ksecoidcertificatepolicies)
- [let kSecOIDClientAuth: CFString](/documentation/security/ksecoidclientauth)
- [let kSecOIDCollectiveStateProvinceName: CFString](/documentation/security/ksecoidcollectivestateprovincename)
- [let kSecOIDCollectiveStreetAddress: CFString](/documentation/security/ksecoidcollectivestreetaddress)
- [let kSecOIDCommonName: CFString](/documentation/security/ksecoidcommonname)
- [let kSecOIDCountryName: CFString](/documentation/security/ksecoidcountryname)
- [let kSecOIDCrlDistributionPoints: CFString](/documentation/security/ksecoidcrldistributionpoints)
- [let kSecOIDCrlNumber: CFString](/documentation/security/ksecoidcrlnumber)
- [let kSecOIDCrlReason: CFString](/documentation/security/ksecoidcrlreason)
- [let kSecOIDDOTMAC_CERT_EMAIL_ENCRYPT: CFString](/documentation/security/ksecoiddotmac_cert_email_encrypt)
- [let kSecOIDDOTMAC_CERT_EMAIL_SIGN: CFString](/documentation/security/ksecoiddotmac_cert_email_sign)
- [let kSecOIDDOTMAC_CERT_EXTENSION: CFString](/documentation/security/ksecoiddotmac_cert_extension)
- [let kSecOIDDOTMAC_CERT_IDENTITY: CFString](/documentation/security/ksecoiddotmac_cert_identity)
- [let kSecOIDDOTMAC_CERT_POLICY: CFString](/documentation/security/ksecoiddotmac_cert_policy)
- [let kSecOIDDeltaCrlIndicator: CFString](/documentation/security/ksecoiddeltacrlindicator)
- [let kSecOIDDescription: CFString](/documentation/security/ksecoiddescription)
- [let kSecOIDEKU_IPSec: CFString](/documentation/security/ksecoideku_ipsec)
- [let kSecOIDEmailAddress: CFString](/documentation/security/ksecoidemailaddress)
- [let kSecOIDEmailProtection: CFString](/documentation/security/ksecoidemailprotection)
- [let kSecOIDExtendedKeyUsage: CFString](/documentation/security/ksecoidextendedkeyusage)
- [let kSecOIDExtendedKeyUsageAny: CFString](/documentation/security/ksecoidextendedkeyusageany)
- [let kSecOIDExtendedUseCodeSigning: CFString](/documentation/security/ksecoidextendedusecodesigning)
- [let kSecOIDGivenName: CFString](/documentation/security/ksecoidgivenname)
- [let kSecOIDHoldInstructionCode: CFString](/documentation/security/ksecoidholdinstructioncode)
- [let kSecOIDInvalidityDate: CFString](/documentation/security/ksecoidinvaliditydate)
- [let kSecOIDIssuerAltName: CFString](/documentation/security/ksecoidissueraltname)
- [let kSecOIDIssuingDistributionPoint: CFString](/documentation/security/ksecoidissuingdistributionpoint)
- [let kSecOIDIssuingDistributionPoints: CFString](/documentation/security/ksecoidissuingdistributionpoints)
- [let kSecOIDKERBv5_PKINIT_KP_CLIENT_AUTH: CFString](/documentation/security/ksecoidkerbv5_pkinit_kp_client_auth)
- [let kSecOIDKERBv5_PKINIT_KP_KDC: CFString](/documentation/security/ksecoidkerbv5_pkinit_kp_kdc)
- [let kSecOIDKeyUsage: CFString](/documentation/security/ksecoidkeyusage)
- [let kSecOIDLocalityName: CFString](/documentation/security/ksecoidlocalityname)
- [let kSecOIDMS_NTPrincipalName: CFString](/documentation/security/ksecoidms_ntprincipalname)
- [let kSecOIDMicrosoftSGC: CFString](/documentation/security/ksecoidmicrosoftsgc)
- [let kSecOIDNameConstraints: CFString](/documentation/security/ksecoidnameconstraints)
- [let kSecOIDNetscapeCertSequence: CFString](/documentation/security/ksecoidnetscapecertsequence)
- [let kSecOIDNetscapeCertType: CFString](/documentation/security/ksecoidnetscapecerttype)
- [let kSecOIDNetscapeSGC: CFString](/documentation/security/ksecoidnetscapesgc)
- [let kSecOIDOCSPSigning: CFString](/documentation/security/ksecoidocspsigning)
- [let kSecOIDOrganizationName: CFString](/documentation/security/ksecoidorganizationname)
- [let kSecOIDOrganizationalUnitName: CFString](/documentation/security/ksecoidorganizationalunitname)
- [let kSecOIDPolicyConstraints: CFString](/documentation/security/ksecoidpolicyconstraints)
- [let kSecOIDPolicyMappings: CFString](/documentation/security/ksecoidpolicymappings)
- [let kSecOIDPrivateKeyUsagePeriod: CFString](/documentation/security/ksecoidprivatekeyusageperiod)
- [let kSecOIDQC_Statements: CFString](/documentation/security/ksecoidqc_statements)
- [let kSecOIDSRVName: CFString](/documentation/security/ksecoidsrvname)
- [let kSecOIDSerialNumber: CFString](/documentation/security/ksecoidserialnumber)
- [let kSecOIDServerAuth: CFString](/documentation/security/ksecoidserverauth)
- [let kSecOIDStateProvinceName: CFString](/documentation/security/ksecoidstateprovincename)
- [let kSecOIDStreetAddress: CFString](/documentation/security/ksecoidstreetaddress)
- [let kSecOIDSubjectAltName: CFString](/documentation/security/ksecoidsubjectaltname)
- [let kSecOIDSubjectDirectoryAttributes: CFString](/documentation/security/ksecoidsubjectdirectoryattributes)
- [let kSecOIDSubjectEmailAddress: CFString](/documentation/security/ksecoidsubjectemailaddress)
- [let kSecOIDSubjectInfoAccess: CFString](/documentation/security/ksecoidsubjectinfoaccess)
- [let kSecOIDSubjectKeyIdentifier: CFString](/documentation/security/ksecoidsubjectkeyidentifier)
- [let kSecOIDSubjectPicture: CFString](/documentation/security/ksecoidsubjectpicture)
- [let kSecOIDSubjectSignatureBitmap: CFString](/documentation/security/ksecoidsubjectsignaturebitmap)
- [let kSecOIDSurname: CFString](/documentation/security/ksecoidsurname)
- [let kSecOIDTimeStamping: CFString](/documentation/security/ksecoidtimestamping)
- [let kSecOIDTitle: CFString](/documentation/security/ksecoidtitle)
- [let kSecOIDUseExemptions: CFString](/documentation/security/ksecoiduseexemptions)
- [let kSecOIDX509V1CertificateIssuerUniqueId: CFString](/documentation/security/ksecoidx509v1certificateissueruniqueid)
- [let kSecOIDX509V1CertificateSubjectUniqueId: CFString](/documentation/security/ksecoidx509v1certificatesubjectuniqueid)
- [let kSecOIDX509V1IssuerName: CFString](/documentation/security/ksecoidx509v1issuername)
- [let kSecOIDX509V1IssuerNameCStruct: CFString](/documentation/security/ksecoidx509v1issuernamecstruct)
- [let kSecOIDX509V1IssuerNameLDAP: CFString](/documentation/security/ksecoidx509v1issuernameldap)
- [let kSecOIDX509V1IssuerNameStd: CFString](/documentation/security/ksecoidx509v1issuernamestd)
- [let kSecOIDX509V1SerialNumber: CFString](/documentation/security/ksecoidx509v1serialnumber)
- [let kSecOIDX509V1Signature: CFString](/documentation/security/ksecoidx509v1signature)
- [let kSecOIDX509V1SignatureAlgorithm: CFString](/documentation/security/ksecoidx509v1signaturealgorithm)
- [let kSecOIDX509V1SignatureAlgorithmParameters: CFString](/documentation/security/ksecoidx509v1signaturealgorithmparameters)
- [let kSecOIDX509V1SignatureAlgorithmTBS: CFString](/documentation/security/ksecoidx509v1signaturealgorithmtbs)
- [let kSecOIDX509V1SignatureCStruct: CFString](/documentation/security/ksecoidx509v1signaturecstruct)
- [let kSecOIDX509V1SignatureStruct: CFString](/documentation/security/ksecoidx509v1signaturestruct)
- [let kSecOIDX509V1SubjectName: CFString](/documentation/security/ksecoidx509v1subjectname)
- [let kSecOIDX509V1SubjectNameCStruct: CFString](/documentation/security/ksecoidx509v1subjectnamecstruct)
- [let kSecOIDX509V1SubjectNameLDAP: CFString](/documentation/security/ksecoidx509v1subjectnameldap)
- [let kSecOIDX509V1SubjectNameStd: CFString](/documentation/security/ksecoidx509v1subjectnamestd)
- [let kSecOIDX509V1SubjectPublicKey: CFString](/documentation/security/ksecoidx509v1subjectpublickey)
- [let kSecOIDX509V1SubjectPublicKeyAlgorithm: CFString](/documentation/security/ksecoidx509v1subjectpublickeyalgorithm)
- [let kSecOIDX509V1SubjectPublicKeyAlgorithmParameters: CFString](/documentation/security/ksecoidx509v1subjectpublickeyalgorithmparameters)
- [let kSecOIDX509V1SubjectPublicKeyCStruct: CFString](/documentation/security/ksecoidx509v1subjectpublickeycstruct)
- [let kSecOIDX509V1ValidityNotAfter: CFString](/documentation/security/ksecoidx509v1validitynotafter)
- [let kSecOIDX509V1ValidityNotBefore: CFString](/documentation/security/ksecoidx509v1validitynotbefore)
- [let kSecOIDX509V1Version: CFString](/documentation/security/ksecoidx509v1version)
- [let kSecOIDX509V3Certificate: CFString](/documentation/security/ksecoidx509v3certificate)
- [let kSecOIDX509V3CertificateCStruct: CFString](/documentation/security/ksecoidx509v3certificatecstruct)
- [let kSecOIDX509V3CertificateExtensionCStruct: CFString](/documentation/security/ksecoidx509v3certificateextensioncstruct)
- [let kSecOIDX509V3CertificateExtensionCritical: CFString](/documentation/security/ksecoidx509v3certificateextensioncritical)
- [let kSecOIDX509V3CertificateExtensionId: CFString](/documentation/security/ksecoidx509v3certificateextensionid)
- [let kSecOIDX509V3CertificateExtensionStruct: CFString](/documentation/security/ksecoidx509v3certificateextensionstruct)
- [let kSecOIDX509V3CertificateExtensionType: CFString](/documentation/security/ksecoidx509v3certificateextensiontype)
- [let kSecOIDX509V3CertificateExtensionValue: CFString](/documentation/security/ksecoidx509v3certificateextensionvalue)
- [let kSecOIDX509V3CertificateExtensionsCStruct: CFString](/documentation/security/ksecoidx509v3certificateextensionscstruct)
- [let kSecOIDX509V3CertificateExtensionsStruct: CFString](/documentation/security/ksecoidx509v3certificateextensionsstruct)
- [let kSecOIDX509V3CertificateNumberOfExtensions: CFString](/documentation/security/ksecoidx509v3certificatenumberofextensions)
- [let kSecOIDX509V3SignedCertificate: CFString](/documentation/security/ksecoidx509v3signedcertificate)
- [let kSecOIDX509V3SignedCertificateCStruct: CFString](/documentation/security/ksecoidx509v3signedcertificatecstruct)
- [Certificate Property Keys](/documentation/security/certificate-property-keys)

##### Constants

- [let kSecPropertyKeyType: CFString](/documentation/security/ksecpropertykeytype)
- [let kSecPropertyKeyLabel: CFString](/documentation/security/ksecpropertykeylabel)
- [let kSecPropertyKeyLocalizedLabel: CFString](/documentation/security/ksecpropertykeylocalizedlabel)
- [let kSecPropertyKeyValue: CFString](/documentation/security/ksecpropertykeyvalue)
- [Certificate Property Type Values](/documentation/security/certificate-property-type-values)

##### Constants

- [let kSecPropertyTypeWarning: CFString](/documentation/security/ksecpropertytypewarning)
- [let kSecPropertyTypeSuccess: CFString](/documentation/security/ksecpropertytypesuccess)
- [let kSecPropertyTypeSection: CFString](/documentation/security/ksecpropertytypesection)
- [let kSecPropertyTypeData: CFString](/documentation/security/ksecpropertytypedata)
- [let kSecPropertyTypeString: CFString](/documentation/security/ksecpropertytypestring)
- [let kSecPropertyTypeURL: CFString](/documentation/security/ksecpropertytypeurl)
- [let kSecPropertyTypeDate: CFString](/documentation/security/ksecpropertytypedate)
- [let kSecPropertyTypeArray: CFString](/documentation/security/ksecpropertytypearray)
- [let kSecPropertyTypeNumber: CFString](/documentation/security/ksecpropertytypenumber)
- [let kSecPropertyTypeTitle: CFString](/documentation/security/ksecpropertytypetitle)
- [let kSecPropertyTypeError: CFString](/documentation/security/ksecpropertytypeerror)
- [Certificate Item Attribute Constants](/documentation/security/certificate-item-attribute-constants)

##### Constants

- [var kSecSubjectItemAttr: Int](/documentation/security/ksecsubjectitemattr)
- [var kSecIssuerItemAttr: Int](/documentation/security/ksecissueritemattr)
- [var kSecSerialNumberItemAttr: Int](/documentation/security/ksecserialnumberitemattr)
- [var kSecPublicKeyHashItemAttr: Int](/documentation/security/ksecpublickeyhashitemattr)
- [var kSecSubjectKeyIdentifierItemAttr: Int](/documentation/security/ksecsubjectkeyidentifieritemattr)
- [var kSecCertTypeItemAttr: Int](/documentation/security/kseccerttypeitemattr)
- [var kSecCertEncodingItemAttr: Int](/documentation/security/kseccertencodingitemattr)

#### Certificate Names

- [func SecCertificateSetPreferred(SecCertificate?, CFString, CFArray?) -> OSStatus](/documentation/security/seccertificatesetpreferred(_:_:_:))
- [func SecCertificateCopyPreferred(CFString, CFArray?) -> SecCertificate?](/documentation/security/seccertificatecopypreferred(_:_:))

#### Legacy Symbols

- [func SecCertificateAddToKeychain(SecCertificate, SecKeychain?) -> OSStatus](/documentation/security/seccertificateaddtokeychain(_:_:))
- [func SecCertificateCopyNormalizedIssuerContent(SecCertificate, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seccertificatecopynormalizedissuercontent(_:_:))
- [func SecCertificateCopyNormalizedSubjectContent(SecCertificate, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seccertificatecopynormalizedsubjectcontent(_:_:))
- [func SecCertificateCopySerialNumber(SecCertificate) -> CFData?](/documentation/security/seccertificatecopyserialnumber(_:_:))
- [func SecCertificateCopyPublicKey(SecCertificate) -> SecKey?](/documentation/security/seccertificatecopypublickey(_:_:))
- [Keys](/documentation/security/keys)

#### Essentials

- [Getting an Existing Key](/documentation/security/getting-an-existing-key)
- [Storing Keys in the Keychain](/documentation/security/storing-keys-in-the-keychain)
- [SecKey](/documentation/security/seckey)
- [func SecKeyGetTypeID() -> CFTypeID](/documentation/security/seckeygettypeid())

#### Key Generation

- [Generating New Cryptographic Keys](/documentation/security/generating-new-cryptographic-keys)
- [Protecting keys with the Secure Enclave](/documentation/security/protecting-keys-with-the-secure-enclave)
- [func SecKeyCreateRandomKey(CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeycreaterandomkey(_:_:))
- [func SecKeyCopyPublicKey(SecKey) -> SecKey?](/documentation/security/seckeycopypublickey(_:))
- [Key Generation Attributes](/documentation/security/key-generation-attributes)

##### Required

- [let kSecAttrKeyType: CFString](/documentation/security/ksecattrkeytype)
- [let kSecAttrKeySizeInBits: CFString](/documentation/security/ksecattrkeysizeinbits)

##### Key Specific

- [let kSecPrivateKeyAttrs: CFString](/documentation/security/ksecprivatekeyattrs)
- [let kSecPublicKeyAttrs: CFString](/documentation/security/ksecpublickeyattrs)

##### Optional

- [let kSecAttrLabel: CFString](/documentation/security/ksecattrlabel)
- [let kSecAttrTokenID: CFString](/documentation/security/ksecattrtokenid)
- [let kSecAttrIsPermanent: CFString](/documentation/security/ksecattrispermanent)
- [let kSecAttrApplicationTag: CFString](/documentation/security/ksecattrapplicationtag)
- [let kSecAttrEffectiveKeySize: CFString](/documentation/security/ksecattreffectivekeysize)
- [let kSecAttrCanEncrypt: CFString](/documentation/security/ksecattrcanencrypt)
- [let kSecAttrCanDecrypt: CFString](/documentation/security/ksecattrcandecrypt)
- [let kSecAttrCanDerive: CFString](/documentation/security/ksecattrcanderive)
- [let kSecAttrCanSign: CFString](/documentation/security/ksecattrcansign)
- [let kSecAttrCanVerify: CFString](/documentation/security/ksecattrcanverify)
- [let kSecAttrCanWrap: CFString](/documentation/security/ksecattrcanwrap)
- [let kSecAttrCanUnwrap: CFString](/documentation/security/ksecattrcanunwrap)

#### Examining Keys

- [func SecKeyIsAlgorithmSupported(SecKey, SecKeyOperationType, SecKeyAlgorithm) -> Bool](/documentation/security/seckeyisalgorithmsupported(_:_:_:))
- [func SecKeyGetBlockSize(SecKey) -> Int](/documentation/security/seckeygetblocksize(_:))
- [func SecKeyCopyAttributes(SecKey) -> CFDictionary?](/documentation/security/seckeycopyattributes(_:))
- [SecKeyAlgorithm](/documentation/security/seckeyalgorithm)

##### Elliptic curve encryption standard X963

- [static let eciesEncryptionStandardX963SHA1AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardx963sha1aesgcm)
- [static let eciesEncryptionStandardX963SHA224AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardx963sha224aesgcm)
- [static let eciesEncryptionStandardX963SHA256AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardx963sha256aesgcm)
- [static let eciesEncryptionStandardX963SHA384AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardx963sha384aesgcm)
- [static let eciesEncryptionStandardX963SHA512AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardx963sha512aesgcm)

##### Elliptic curve encryption standard variable IVX963

- [static let eciesEncryptionStandardVariableIVX963SHA224AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardvariableivx963sha224aesgcm)
- [static let eciesEncryptionStandardVariableIVX963SHA256AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardvariableivx963sha256aesgcm)
- [static let eciesEncryptionStandardVariableIVX963SHA384AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardvariableivx963sha384aesgcm)
- [static let eciesEncryptionStandardVariableIVX963SHA512AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptionstandardvariableivx963sha512aesgcm)

##### Elliptic curve encryption cofactor variable IVX963

- [static let eciesEncryptionCofactorVariableIVX963SHA224AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorvariableivx963sha224aesgcm)
- [static let eciesEncryptionCofactorVariableIVX963SHA256AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorvariableivx963sha256aesgcm)
- [static let eciesEncryptionCofactorVariableIVX963SHA384AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorvariableivx963sha384aesgcm)
- [static let eciesEncryptionCofactorVariableIVX963SHA512AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorvariableivx963sha512aesgcm)

##### Elliptic curve encryption cofactor X963

- [static let eciesEncryptionCofactorX963SHA1AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorx963sha1aesgcm)
- [static let eciesEncryptionCofactorX963SHA224AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorx963sha224aesgcm)
- [static let eciesEncryptionCofactorX963SHA256AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorx963sha256aesgcm)
- [static let eciesEncryptionCofactorX963SHA384AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorx963sha384aesgcm)
- [static let eciesEncryptionCofactorX963SHA512AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/eciesencryptioncofactorx963sha512aesgcm)

##### Elliptic curve signature RFC4754

- [static let ecdsaSignatureRFC4754: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturerfc4754)

##### Elliptic curve signature digest RFC4754

- [static let ecdsaSignatureDigestRFC4754: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754)
- [static let ecdsaSignatureDigestRFC4754SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754sha1)
- [static let ecdsaSignatureDigestRFC4754SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754sha224)
- [static let ecdsaSignatureDigestRFC4754SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754sha256)
- [static let ecdsaSignatureDigestRFC4754SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754sha384)
- [static let ecdsaSignatureDigestRFC4754SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestrfc4754sha512)

##### Elliptic curve signature message RFC4754

- [static let ecdsaSignatureMessageRFC4754SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagerfc4754sha1)
- [static let ecdsaSignatureMessageRFC4754SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagerfc4754sha224)
- [static let ecdsaSignatureMessageRFC4754SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagerfc4754sha256)
- [static let ecdsaSignatureMessageRFC4754SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagerfc4754sha384)
- [static let ecdsaSignatureMessageRFC4754SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagerfc4754sha512)

##### Elliptic curve signature digest X962

- [static let ecdsaSignatureDigestX962: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962)
- [static let ecdsaSignatureDigestX962SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962sha1)
- [static let ecdsaSignatureDigestX962SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962sha224)
- [static let ecdsaSignatureDigestX962SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962sha256)
- [static let ecdsaSignatureDigestX962SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962sha384)
- [static let ecdsaSignatureDigestX962SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturedigestx962sha512)

##### Elliptic curve signature message X962

- [static let ecdsaSignatureMessageX962SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagex962sha1)
- [static let ecdsaSignatureMessageX962SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagex962sha224)
- [static let ecdsaSignatureMessageX962SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagex962sha256)
- [static let ecdsaSignatureMessageX962SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagex962sha384)
- [static let ecdsaSignatureMessageX962SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdsasignaturemessagex962sha512)

##### Elliptic curve key exchange

- [static let ecdhKeyExchangeCofactor: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactor)
- [static let ecdhKeyExchangeStandard: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandard)
- [static let ecdhKeyExchangeCofactorX963SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactorx963sha1)
- [static let ecdhKeyExchangeStandardX963SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandardx963sha1)
- [static let ecdhKeyExchangeCofactorX963SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactorx963sha224)
- [static let ecdhKeyExchangeCofactorX963SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactorx963sha256)
- [static let ecdhKeyExchangeCofactorX963SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactorx963sha384)
- [static let ecdhKeyExchangeCofactorX963SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangecofactorx963sha512)
- [static let ecdhKeyExchangeStandardX963SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandardx963sha224)
- [static let ecdhKeyExchangeStandardX963SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandardx963sha256)
- [static let ecdhKeyExchangeStandardX963SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandardx963sha384)
- [static let ecdhKeyExchangeStandardX963SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/ecdhkeyexchangestandardx963sha512)

##### RSA encryption

- [static let rsaEncryptionRaw: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionraw)
- [static let rsaEncryptionPKCS1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionpkcs1)

##### RSA encryption OAEP

- [static let rsaEncryptionOAEPSHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha1)
- [static let rsaEncryptionOAEPSHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha224)
- [static let rsaEncryptionOAEPSHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha256)
- [static let rsaEncryptionOAEPSHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha384)
- [static let rsaEncryptionOAEPSHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha512)

##### RSA encryption OAEP AESGCM

- [static let rsaEncryptionOAEPSHA1AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha1aesgcm)
- [static let rsaEncryptionOAEPSHA224AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha224aesgcm)
- [static let rsaEncryptionOAEPSHA256AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha256aesgcm)
- [static let rsaEncryptionOAEPSHA384AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha384aesgcm)
- [static let rsaEncryptionOAEPSHA512AESGCM: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsaencryptionoaepsha512aesgcm)

##### RSA signature raw

- [static let rsaSignatureRaw: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignatureraw)

##### RSA signature digest PKCS1v15

- [static let rsaSignatureDigestPKCS1v15Raw: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15raw)
- [static let rsaSignatureDigestPKCS1v15SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15sha1)
- [static let rsaSignatureDigestPKCS1v15SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15sha224)
- [static let rsaSignatureDigestPKCS1v15SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15sha256)
- [static let rsaSignatureDigestPKCS1v15SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15sha384)
- [static let rsaSignatureDigestPKCS1v15SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpkcs1v15sha512)

##### RSA signature message PKCS1v15

- [static let rsaSignatureMessagePKCS1v15SHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepkcs1v15sha1)
- [static let rsaSignatureMessagePKCS1v15SHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepkcs1v15sha224)
- [static let rsaSignatureMessagePKCS1v15SHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepkcs1v15sha256)
- [static let rsaSignatureMessagePKCS1v15SHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepkcs1v15sha384)
- [static let rsaSignatureMessagePKCS1v15SHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepkcs1v15sha512)

##### RSA signature digest PSS

- [static let rsaSignatureDigestPSSSHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpsssha1)
- [static let rsaSignatureDigestPSSSHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpsssha224)
- [static let rsaSignatureDigestPSSSHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpsssha256)
- [static let rsaSignatureDigestPSSSHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpsssha384)
- [static let rsaSignatureDigestPSSSHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturedigestpsssha512)

##### RSA signature message PSS

- [static let rsaSignatureMessagePSSSHA1: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepsssha1)
- [static let rsaSignatureMessagePSSSHA224: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepsssha224)
- [static let rsaSignatureMessagePSSSHA256: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepsssha256)
- [static let rsaSignatureMessagePSSSHA384: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepsssha384)
- [static let rsaSignatureMessagePSSSHA512: SecKeyAlgorithm](/documentation/security/seckeyalgorithm/rsasignaturemessagepsssha512)

##### Initializers

- [init(rawValue: CFString)](/documentation/security/seckeyalgorithm/init(rawvalue:))
- [SecKeyOperationType](/documentation/security/seckeyoperationtype)

##### Enumeration Cases

- [case decrypt](/documentation/security/seckeyoperationtype/decrypt)
- [case encrypt](/documentation/security/seckeyoperationtype/encrypt)
- [case keyExchange](/documentation/security/seckeyoperationtype/keyexchange)
- [case sign](/documentation/security/seckeyoperationtype/sign)
- [case verify](/documentation/security/seckeyoperationtype/verify)

##### Initializers

- [init?(rawValue: CFIndex)](/documentation/security/seckeyoperationtype/init(rawvalue:))

#### Import and Export

- [Storing Keys as Data](/documentation/security/storing-keys-as-data)
- [func SecKeyCopyExternalRepresentation(SecKey, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeycopyexternalrepresentation(_:_:))
- [func SecKeyCreateWithData(CFData, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeycreatewithdata(_:_:_:))

#### Key Exchange

- [func SecKeyCopyKeyExchangeResult(SecKey, SecKeyAlgorithm, SecKey, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeycopykeyexchangeresult(_:_:_:_:_:))
- [SecKeyKeyExchangeParameter](/documentation/security/seckeykeyexchangeparameter)

##### Type Properties

- [static let requestedSize: SecKeyKeyExchangeParameter](/documentation/security/seckeykeyexchangeparameter/requestedsize)
- [static let sharedInfo: SecKeyKeyExchangeParameter](/documentation/security/seckeykeyexchangeparameter/sharedinfo)

##### Initializers

- [init(rawValue: CFString)](/documentation/security/seckeykeyexchangeparameter/init(rawvalue:))

#### Encryption

- [Using Keys for Encryption](/documentation/security/using-keys-for-encryption)
- [func SecKeyCreateEncryptedData(SecKey, SecKeyAlgorithm, CFData, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeycreateencrypteddata(_:_:_:_:))
- [func SecKeyCreateDecryptedData(SecKey, SecKeyAlgorithm, CFData, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeycreatedecrypteddata(_:_:_:_:))

#### Digital Signatures

- [Signing and Verifying](/documentation/security/signing-and-verifying)
- [func SecKeyCreateSignature(SecKey, SecKeyAlgorithm, CFData, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeycreatesignature(_:_:_:_:))
- [func SecKeyVerifySignature(SecKey, SecKeyAlgorithm, CFData, CFData, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/security/seckeyverifysignature(_:_:_:_:_:))

#### Legacy iOS Key Operations

- [func SecKeyGeneratePair(CFDictionary, UnsafeMutablePointer<SecKey?>?, UnsafeMutablePointer<SecKey?>?) -> OSStatus](/documentation/security/seckeygeneratepair(_:_:_:))
- [func SecKeyEncrypt(SecKey, SecPadding, UnsafePointer<UInt8>, Int, UnsafeMutablePointer<UInt8>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/seckeyencrypt(_:_:_:_:_:_:))
- [func SecKeyDecrypt(SecKey, SecPadding, UnsafePointer<UInt8>, Int, UnsafeMutablePointer<UInt8>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/seckeydecrypt(_:_:_:_:_:_:))
- [func SecKeyRawSign(SecKey, SecPadding, UnsafePointer<UInt8>, Int, UnsafeMutablePointer<UInt8>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/seckeyrawsign(_:_:_:_:_:_:))
- [func SecKeyRawVerify(SecKey, SecPadding, UnsafePointer<UInt8>, Int, UnsafePointer<UInt8>, Int) -> OSStatus](/documentation/security/seckeyrawverify(_:_:_:_:_:_:))
- [SecPadding](/documentation/security/secpadding)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/secpadding/init(rawvalue:))

##### Constants

- [static var sigRaw: SecPadding](/documentation/security/secpadding/sigraw)
- [static var PKCS1: SecPadding](/documentation/security/secpadding/pkcs1)
- [static var OAEP: SecPadding](/documentation/security/secpadding/oaep)
- [static var PKCS1MD2: SecPadding](/documentation/security/secpadding/pkcs1md2)
- [static var PKCS1MD5: SecPadding](/documentation/security/secpadding/pkcs1md5)
- [static var PKCS1SHA1: SecPadding](/documentation/security/secpadding/pkcs1sha1)
- [static var PKCS1SHA224: SecPadding](/documentation/security/secpadding/pkcs1sha224)
- [static var PKCS1SHA256: SecPadding](/documentation/security/secpadding/pkcs1sha256)
- [static var PKCS1SHA384: SecPadding](/documentation/security/secpadding/pkcs1sha384)
- [static var PKCS1SHA512: SecPadding](/documentation/security/secpadding/pkcs1sha512)

#### Legacy macOS Key Operations

- [func SecKeyGeneratePairAsync(CFDictionary, dispatch_queue_t, SecKeyGeneratePairBlock)](/documentation/security/seckeygeneratepairasync(_:_:_:))
- [func SecKeyGenerateSymmetric(CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeygeneratesymmetric(_:_:))
- [func SecKeyCreateFromData(CFDictionary, CFData, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeycreatefromdata(_:_:_:))
- [func SecKeyDeriveFromPassword(CFString, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeyderivefrompassword(_:_:_:))
- [func SecKeyWrapSymmetric(SecKey, SecKey, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFData?](/documentation/security/seckeywrapsymmetric(_:_:_:_:))
- [func SecKeyUnwrapSymmetric(UnsafeMutablePointer<Unmanaged<CFData>?>, SecKey, CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecKey?](/documentation/security/seckeyunwrapsymmetric(_:_:_:_:))
- [SecKeySizes](/documentation/security/seckeysizes)

##### Constants

- [case secDefaultKeySize](/documentation/security/seckeysizes/secdefaultkeysize)
- [case sec3DES192](/documentation/security/seckeysizes/sec3des192)
- [case secAES128](/documentation/security/seckeysizes/secaes128)
- [static var secAES192: SecKeySizes](/documentation/security/seckeysizes/secaes192)
- [case secAES256](/documentation/security/seckeysizes/secaes256)
- [static var secp192r1: SecKeySizes](/documentation/security/seckeysizes/secp192r1)
- [static var secp256r1: SecKeySizes](/documentation/security/seckeysizes/secp256r1)
- [case secp384r1](/documentation/security/seckeysizes/secp384r1)
- [case secp521r1](/documentation/security/seckeysizes/secp521r1)
- [case secRSAMin](/documentation/security/seckeysizes/secrsamin)
- [case secRSAMax](/documentation/security/seckeysizes/secrsamax)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/seckeysizes/init(rawvalue:))
- [SecKeyUsage](/documentation/security/seckeyusage)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/seckeyusage/init(rawvalue:))

##### Flags

- [static var crlSign: SecKeyUsage](/documentation/security/seckeyusage/crlsign)
- [static var contentCommitment: SecKeyUsage](/documentation/security/seckeyusage/contentcommitment)
- [static var critical: SecKeyUsage](/documentation/security/seckeyusage/critical)
- [static var dataEncipherment: SecKeyUsage](/documentation/security/seckeyusage/dataencipherment)
- [static var decipherOnly: SecKeyUsage](/documentation/security/seckeyusage/decipheronly)
- [static var digitalSignature: SecKeyUsage](/documentation/security/seckeyusage/digitalsignature)
- [static var encipherOnly: SecKeyUsage](/documentation/security/seckeyusage/encipheronly)
- [static var keyAgreement: SecKeyUsage](/documentation/security/seckeyusage/keyagreement)
- [static var keyCertSign: SecKeyUsage](/documentation/security/seckeyusage/keycertsign)
- [static var keyEncipherment: SecKeyUsage](/documentation/security/seckeyusage/keyencipherment)
- [static var nonRepudiation: SecKeyUsage](/documentation/security/seckeyusage/nonrepudiation)
- [static var all: SecKeyUsage](/documentation/security/seckeyusage/all)
- [SecPublicKeyHash](/documentation/security/secpublickeyhash)
- [SecKeyGeneratePairBlock](/documentation/security/seckeygeneratepairblock)
- [SecCredentialType](/documentation/security/seccredentialtype)

##### Constants

- [case `default`](/documentation/security/seccredentialtype/default)
- [case withUI](/documentation/security/seccredentialtype/withui)
- [case noUI](/documentation/security/seccredentialtype/noui)

##### Initializers

- [init?(rawValue: uint32)](/documentation/security/seccredentialtype/init(rawvalue:))
- [Identities](/documentation/security/identities)

#### Essentials

- [Creating an Identity](/documentation/security/creating-an-identity)
- [Storing an Identity in the Keychain](/documentation/security/storing-an-identity-in-the-keychain)
- [func SecIdentityCreateWithCertificate(CFTypeRef?, SecCertificate, UnsafeMutablePointer<SecIdentity?>) -> OSStatus](/documentation/security/secidentitycreatewithcertificate(_:_:_:))
- [SecIdentity](/documentation/security/secidentity)
- [func SecIdentityGetTypeID() -> CFTypeID](/documentation/security/secidentitygettypeid())

#### Identity Import

- [Importing an Identity](/documentation/security/importing-an-identity)
- [func SecPKCS12Import(CFData, CFDictionary, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/secpkcs12import(_:_:_:))
- [Keychain Import and Export Options](/documentation/security/keychain-import-and-export-options)

##### Constants

- [let kSecImportExportPassphrase: CFString](/documentation/security/ksecimportexportpassphrase)
- [let kSecImportExportKeychain: CFString](/documentation/security/ksecimportexportkeychain)
- [let kSecImportExportAccess: CFString](/documentation/security/ksecimportexportaccess)
- [PKCS #12 Import Item Keys](/documentation/security/pkcs-12-import-item-keys)

##### Constants

- [let kSecImportItemLabel: CFString](/documentation/security/ksecimportitemlabel)
- [let kSecImportItemKeyID: CFString](/documentation/security/ksecimportitemkeyid)
- [let kSecImportItemTrust: CFString](/documentation/security/ksecimportitemtrust)
- [let kSecImportItemCertChain: CFString](/documentation/security/ksecimportitemcertchain)
- [let kSecImportItemIdentity: CFString](/documentation/security/ksecimportitemidentity)

#### Identity Components

- [Parsing an Identity](/documentation/security/parsing-an-identity)
- [func SecIdentityCopyCertificate(SecIdentity, UnsafeMutablePointer<SecCertificate?>) -> OSStatus](/documentation/security/secidentitycopycertificate(_:_:))
- [func SecIdentityCopyPrivateKey(SecIdentity, UnsafeMutablePointer<SecKey?>) -> OSStatus](/documentation/security/secidentitycopyprivatekey(_:_:))

#### System Identities

- [func SecIdentityCopySystemIdentity(CFString, UnsafeMutablePointer<SecIdentity?>, UnsafeMutablePointer<CFString?>?) -> OSStatus](/documentation/security/secidentitycopysystemidentity(_:_:_:))
- [func SecIdentitySetSystemIdentity(CFString, SecIdentity?) -> OSStatus](/documentation/security/secidentitysetsystemidentity(_:_:))
- [System Identity Domains](/documentation/security/system-identity-domains)

##### Constants

- [let kSecIdentityDomainDefault: CFString](/documentation/security/ksecidentitydomaindefault)
- [let kSecIdentityDomainKerberosKDC: CFString](/documentation/security/ksecidentitydomainkerberoskdc)

#### Identity Naming

- [func SecIdentitySetPreferred(SecIdentity?, CFString, CFArray?) -> OSStatus](/documentation/security/secidentitysetpreferred(_:_:_:))
- [func SecIdentityCopyPreferred(CFString, CFArray?, CFArray?) -> SecIdentity?](/documentation/security/secidentitycopypreferred(_:_:_:))

#### Identity Search

- [SecIdentitySearch](/documentation/security/secidentitysearch)

#### Creating an Identity for Local Network TLS

- [Creating an Identity for Local Network TLS](/documentation/network/creating-an-identity-for-local-network-tls)
- [Policies](/documentation/security/policies)

#### Standard Policies

- [func SecPolicyCreateBasicX509() -> SecPolicy](/documentation/security/secpolicycreatebasicx509())
- [func SecPolicyCreateSSL(Bool, CFString?) -> SecPolicy](/documentation/security/secpolicycreatessl(_:_:))
- [func SecPolicyCreateRevocation(CFOptionFlags) -> SecPolicy?](/documentation/security/secpolicycreaterevocation(_:))
- [Revocation Policy Constants](/documentation/security/revocation-policy-constants)

##### Constants

- [var kSecRevocationCRLMethod: CFOptionFlags](/documentation/security/ksecrevocationcrlmethod)
- [var kSecRevocationNetworkAccessDisabled: CFOptionFlags](/documentation/security/ksecrevocationnetworkaccessdisabled)
- [var kSecRevocationOCSPMethod: CFOptionFlags](/documentation/security/ksecrevocationocspmethod)
- [var kSecRevocationPreferCRL: CFOptionFlags](/documentation/security/ksecrevocationprefercrl)
- [var kSecRevocationRequirePositiveResponse: CFOptionFlags](/documentation/security/ksecrevocationrequirepositiveresponse)
- [var kSecRevocationUseAnyAvailableMethod: CFOptionFlags](/documentation/security/ksecrevocationuseanyavailablemethod)
- [SecPolicy](/documentation/security/secpolicy)
- [func SecPolicyGetTypeID() -> CFTypeID](/documentation/security/secpolicygettypeid())

#### Advanced Policy Management

- [func SecPolicyCreateWithProperties(CFTypeRef, CFDictionary?) -> SecPolicy?](/documentation/security/secpolicycreatewithproperties(_:_:))
- [func SecPolicyCopyProperties(SecPolicy) -> CFDictionary?](/documentation/security/secpolicycopyproperties(_:))
- [Security Policy Keys](/documentation/security/security-policy-keys)

##### Constants

- [let kSecPolicyOid: CFString](/documentation/security/ksecpolicyoid)
- [let kSecPolicyName: CFString](/documentation/security/ksecpolicyname)
- [let kSecPolicyClient: CFString](/documentation/security/ksecpolicyclient)
- [let kSecPolicyRevocationFlags: CFString](/documentation/security/ksecpolicyrevocationflags)
- [let kSecPolicyTeamIdentifier: CFString](/documentation/security/ksecpolicyteamidentifier)
- [let kSecPolicyKU_DigitalSignature: CFString](/documentation/security/ksecpolicyku_digitalsignature)
- [let kSecPolicyKU_NonRepudiation: CFString](/documentation/security/ksecpolicyku_nonrepudiation)
- [let kSecPolicyKU_KeyEncipherment: CFString](/documentation/security/ksecpolicyku_keyencipherment)
- [let kSecPolicyKU_DataEncipherment: CFString](/documentation/security/ksecpolicyku_dataencipherment)
- [let kSecPolicyKU_KeyAgreement: CFString](/documentation/security/ksecpolicyku_keyagreement)
- [let kSecPolicyKU_KeyCertSign: CFString](/documentation/security/ksecpolicyku_keycertsign)
- [let kSecPolicyKU_CRLSign: CFString](/documentation/security/ksecpolicyku_crlsign)
- [let kSecPolicyKU_EncipherOnly: CFString](/documentation/security/ksecpolicyku_encipheronly)
- [let kSecPolicyKU_DecipherOnly: CFString](/documentation/security/ksecpolicyku_decipheronly)
- [Standard Policies for Specific Certificate Types](/documentation/security/standard-policies-for-specific-certificate-types)

##### Constants

- [let kSecPolicyAppleX509Basic: CFString](/documentation/security/ksecpolicyapplex509basic)
- [let kSecPolicyAppleSSL: CFString](/documentation/security/ksecpolicyapplessl)
- [let kSecPolicyAppleSMIME: CFString](/documentation/security/ksecpolicyapplesmime)
- [let kSecPolicyAppleEAP: CFString](/documentation/security/ksecpolicyappleeap)
- [let kSecPolicyAppleIPsec: CFString](/documentation/security/ksecpolicyappleipsec)
- [let kSecPolicyApplePKINITClient: CFString](/documentation/security/ksecpolicyapplepkinitclient)
- [let kSecPolicyApplePKINITServer: CFString](/documentation/security/ksecpolicyapplepkinitserver)
- [let kSecPolicyAppleCodeSigning: CFString](/documentation/security/ksecpolicyapplecodesigning)
- [let kSecPolicyMacAppStoreReceipt: CFString](/documentation/security/ksecpolicymacappstorereceipt)
- [let kSecPolicyAppleIDValidation: CFString](/documentation/security/ksecpolicyappleidvalidation)
- [let kSecPolicyAppleTimeStamping: CFString](/documentation/security/ksecpolicyappletimestamping)
- [let kSecPolicyApplePassbookSigning: CFString](/documentation/security/ksecpolicyapplepassbooksigning)
- [let kSecPolicyApplePayIssuerEncryption: CFString](/documentation/security/ksecpolicyapplepayissuerencryption)
- [let kSecPolicyAppleRevocation: CFString](/documentation/security/ksecpolicyapplerevocation)

#### Legacy Symbols

- [SecPolicySearch](/documentation/security/secpolicysearch)
- [Trust](/documentation/security/trust)

#### Essentials

- [Creating a Trust Object](/documentation/security/creating-a-trust-object)
- [func SecTrustCreateWithCertificates(CFTypeRef, CFTypeRef?, UnsafeMutablePointer<SecTrust?>) -> OSStatus](/documentation/security/sectrustcreatewithcertificates(_:_:_:))
- [SecTrust](/documentation/security/sectrust)
- [func SecTrustGetTypeID() -> CFTypeID](/documentation/security/sectrustgettypeid())

#### Trust Evaluation

- [Evaluating a Trust and Parsing the Result](/documentation/security/evaluating-a-trust-and-parsing-the-result)
- [func SecTrustEvaluateWithError(SecTrust, UnsafeMutablePointer<CFError?>?) -> Bool](/documentation/security/sectrustevaluatewitherror(_:_:))
- [func SecTrustEvaluateAsyncWithError(SecTrust, dispatch_queue_t, SecTrustWithErrorCallback) -> OSStatus](/documentation/security/sectrustevaluateasyncwitherror(_:_:_:))
- [SecTrustWithErrorCallback](/documentation/security/sectrustwitherrorcallback)

#### Trust Evaluation Result

- [Discovering Why a Trust Evaluation Failed](/documentation/security/discovering-why-a-trust-evaluation-failed)
- [func SecTrustGetTrustResult(SecTrust, UnsafeMutablePointer<SecTrustResultType>) -> OSStatus](/documentation/security/sectrustgettrustresult(_:_:))
- [SecTrustResultType](/documentation/security/sectrustresulttype)

##### Result Codes

- [case unspecified](/documentation/security/sectrustresulttype/unspecified)
- [case proceed](/documentation/security/sectrustresulttype/proceed)
- [case deny](/documentation/security/sectrustresulttype/deny)
- [case recoverableTrustFailure](/documentation/security/sectrustresulttype/recoverabletrustfailure)
- [case fatalTrustFailure](/documentation/security/sectrustresulttype/fataltrustfailure)
- [case otherError](/documentation/security/sectrustresulttype/othererror)
- [case invalid](/documentation/security/sectrustresulttype/invalid)
- [case confirm](/documentation/security/sectrustresulttype/confirm)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/sectrustresulttype/init(rawvalue:))
- [func SecTrustCopyResult(SecTrust) -> CFDictionary?](/documentation/security/sectrustcopyresult(_:))
- [Trust Result Dictionary Keys](/documentation/security/trust-result-dictionary-keys)

##### Constants

- [let kSecTrustCertificateTransparency: CFString](/documentation/security/ksectrustcertificatetransparency)
- [let kSecTrustCertificateTransparencyWhiteList: CFString](/documentation/security/ksectrustcertificatetransparencywhitelist)
- [let kSecTrustEvaluationDate: CFString](/documentation/security/ksectrustevaluationdate)
- [let kSecTrustExtendedValidation: CFString](/documentation/security/ksectrustextendedvalidation)
- [let kSecTrustOrganizationName: CFString](/documentation/security/ksectrustorganizationname)
- [let kSecTrustResultValue: CFString](/documentation/security/ksectrustresultvalue)
- [let kSecTrustRevocationChecked: CFString](/documentation/security/ksectrustrevocationchecked)
- [let kSecTrustRevocationValidUntilDate: CFString](/documentation/security/ksectrustrevocationvaliduntildate)

#### Trust Components

- [func SecTrustCopyPublicKey(SecTrust) -> SecKey?](/documentation/security/sectrustcopypublickey(_:))
- [func SecTrustGetCertificateCount(SecTrust) -> CFIndex](/documentation/security/sectrustgetcertificatecount(_:))
- [func SecTrustGetCertificateAtIndex(SecTrust, CFIndex) -> SecCertificate?](/documentation/security/sectrustgetcertificateatindex(_:_:))
- [func SecTrustGetVerifyTime(SecTrust) -> CFAbsoluteTime](/documentation/security/sectrustgetverifytime(_:))
- [func SecTrustCopyAnchorCertificates(UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sectrustcopyanchorcertificates(_:))
- [func SecTrustCopyCustomAnchorCertificates(SecTrust, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sectrustcopycustomanchorcertificates(_:_:))
- [func SecTrustCopyExceptions(SecTrust) -> CFData?](/documentation/security/sectrustcopyexceptions(_:))
- [func SecTrustCopyPolicies(SecTrust, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sectrustcopypolicies(_:_:))
- [func SecTrustCopyProperties(SecTrust) -> CFArray?](/documentation/security/sectrustcopyproperties(_:))

#### Advanced Trust Configuation

- [Configuring a Trust](/documentation/security/configuring-a-trust)
- [func SecTrustSetVerifyDate(SecTrust, CFDate) -> OSStatus](/documentation/security/sectrustsetverifydate(_:_:))
- [func SecTrustSetAnchorCertificates(SecTrust, CFArray?) -> OSStatus](/documentation/security/sectrustsetanchorcertificates(_:_:))
- [func SecTrustSetAnchorCertificatesOnly(SecTrust, Bool) -> OSStatus](/documentation/security/sectrustsetanchorcertificatesonly(_:_:))
- [func SecTrustSetExceptions(SecTrust, CFData?) -> Bool](/documentation/security/sectrustsetexceptions(_:_:))
- [func SecTrustSetPolicies(SecTrust, CFTypeRef) -> OSStatus](/documentation/security/sectrustsetpolicies(_:_:))
- [func SecTrustSetOptions(SecTrust, SecTrustOptionFlags) -> OSStatus](/documentation/security/sectrustsetoptions(_:_:))
- [SecTrustOptionFlags](/documentation/security/sectrustoptionflags)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/sectrustoptionflags/init(rawvalue:))

##### Flags

- [static var allowExpired: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/allowexpired)
- [static var leafIsCA: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/leafisca)
- [static var fetchIssuerFromNet: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/fetchissuerfromnet)
- [static var allowExpiredRoot: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/allowexpiredroot)
- [static var requireRevPerCert: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/requirerevpercert)
- [static var useTrustSettings: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/usetrustsettings)
- [static var implicitAnchors: SecTrustOptionFlags](/documentation/security/sectrustoptionflags/implicitanchors)
- [func SecTrustGetNetworkFetchAllowed(SecTrust, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/security/sectrustgetnetworkfetchallowed(_:_:))
- [func SecTrustSetNetworkFetchAllowed(SecTrust, Bool) -> OSStatus](/documentation/security/sectrustsetnetworkfetchallowed(_:_:))
- [func SecTrustSetOCSPResponse(SecTrust, CFTypeRef?) -> OSStatus](/documentation/security/sectrustsetocspresponse(_:_:))
- [func SecTrustSetSignedCertificateTimestamps(SecTrust, CFArray?) -> OSStatus](/documentation/security/sectrustsetsignedcertificatetimestamps(_:_:))

#### Trust Settings

- [func SecTrustSettingsCopyCertificates(SecTrustSettingsDomain, UnsafeMutablePointer<CFArray?>?) -> OSStatus](/documentation/security/sectrustsettingscopycertificates(_:_:))
- [func SecTrustSettingsCopyModificationDate(SecCertificate, SecTrustSettingsDomain, UnsafeMutablePointer<CFDate?>) -> OSStatus](/documentation/security/sectrustsettingscopymodificationdate(_:_:_:))
- [Usage Constraints Dictionary Keys](/documentation/security/usage-constraints-dictionary-keys)

##### Constants

- [var kSecTrustSettingsPolicy: String](/documentation/security/ksectrustsettingspolicy)
- [var kSecTrustSettingsApplication: String](/documentation/security/ksectrustsettingsapplication)
- [var kSecTrustSettingsPolicyString: String](/documentation/security/ksectrustsettingspolicystring)
- [var kSecTrustSettingsKeyUsage: String](/documentation/security/ksectrustsettingskeyusage)
- [var kSecTrustSettingsAllowedError: String](/documentation/security/ksectrustsettingsallowederror)
- [var kSecTrustSettingsResult: String](/documentation/security/ksectrustsettingsresult)
- [func SecTrustSettingsCopyTrustSettings(SecCertificate, SecTrustSettingsDomain, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sectrustsettingscopytrustsettings(_:_:_:))
- [func SecTrustSettingsCreateExternalRepresentation(SecTrustSettingsDomain, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/sectrustsettingscreateexternalrepresentation(_:_:))
- [func SecTrustSettingsImportExternalRepresentation(SecTrustSettingsDomain, CFData) -> OSStatus](/documentation/security/sectrustsettingsimportexternalrepresentation(_:_:))
- [func SecTrustSettingsRemoveTrustSettings(SecCertificate, SecTrustSettingsDomain) -> OSStatus](/documentation/security/sectrustsettingsremovetrustsettings(_:_:))
- [func SecTrustSettingsSetTrustSettings(SecCertificate, SecTrustSettingsDomain, CFTypeRef?) -> OSStatus](/documentation/security/sectrustsettingssettrustsettings(_:_:_:))
- [SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage)

##### Initializers

- [init(rawValue: UInt32)](/documentation/security/sectrustsettingskeyusage/init(rawvalue:))

##### Constants

- [static var useSignature: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/usesignature)
- [static var useEnDecryptData: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/useendecryptdata)
- [static var useEnDecryptKey: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/useendecryptkey)
- [static var useSignCert: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/usesigncert)
- [static var useSignRevocation: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/usesignrevocation)
- [static var useKeyExchange: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/usekeyexchange)
- [static var useAny: SecTrustSettingsKeyUsage](/documentation/security/sectrustsettingskeyusage/useany)
- [SecTrustSettingsResult](/documentation/security/sectrustsettingsresult)

##### Constants

- [case invalid](/documentation/security/sectrustsettingsresult/invalid)
- [case trustRoot](/documentation/security/sectrustsettingsresult/trustroot)
- [case trustAsRoot](/documentation/security/sectrustsettingsresult/trustasroot)
- [case deny](/documentation/security/sectrustsettingsresult/deny)
- [case unspecified](/documentation/security/sectrustsettingsresult/unspecified)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/sectrustsettingsresult/init(rawvalue:))
- [SecTrustSettingsDomain](/documentation/security/sectrustsettingsdomain)

##### Constants

- [case user](/documentation/security/sectrustsettingsdomain/user)
- [case admin](/documentation/security/sectrustsettingsdomain/admin)
- [case system](/documentation/security/sectrustsettingsdomain/system)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/security/sectrustsettingsdomain/init(rawvalue:))

#### Legacy Symbols

- [func SecTrustEvaluate(SecTrust, UnsafeMutablePointer<SecTrustResultType>) -> OSStatus](/documentation/security/sectrustevaluate(_:_:))
- [func SecTrustEvaluateAsync(SecTrust, dispatch_queue_t?, SecTrustCallback) -> OSStatus](/documentation/security/sectrustevaluateasync(_:_:_:))
- [SecTrustCallback](/documentation/security/sectrustcallback)
- [func SecTrustSetKeychains(SecTrust, CFTypeRef?) -> OSStatus](/documentation/security/sectrustsetkeychains(_:_:))

### Thread Safety

- [Working with Concurrency](/documentation/security/working-with-concurrency)
- [Cryptographic Message Syntax Services](/documentation/security/cryptographic-message-syntax-services)

### The Encoder

- [func CMSEncoderCreate(UnsafeMutablePointer<CMSEncoder?>) -> OSStatus](/documentation/security/cmsencodercreate(_:))
- [CMSEncoder](/documentation/security/cmsencoder)
- [func CMSEncoderGetTypeID() -> CFTypeID](/documentation/security/cmsencodergettypeid())

### Message Creation

- [func CMSEncoderAddSigners(CMSEncoder, CFTypeRef) -> OSStatus](/documentation/security/cmsencoderaddsigners(_:_:))
- [func CMSEncoderAddRecipients(CMSEncoder, CFTypeRef) -> OSStatus](/documentation/security/cmsencoderaddrecipients(_:_:))
- [func CMSEncoderSetHasDetachedContent(CMSEncoder, Bool) -> OSStatus](/documentation/security/cmsencodersethasdetachedcontent(_:_:))
- [func CMSEncoderSetEncapsulatedContentTypeOID(CMSEncoder, CFTypeRef) -> OSStatus](/documentation/security/cmsencodersetencapsulatedcontenttypeoid(_:_:))
- [func CMSEncoderAddSupportingCerts(CMSEncoder, CFTypeRef) -> OSStatus](/documentation/security/cmsencoderaddsupportingcerts(_:_:))
- [func CMSEncoderAddSignedAttributes(CMSEncoder, CMSSignedAttributes) -> OSStatus](/documentation/security/cmsencoderaddsignedattributes(_:_:))
- [CMSSignedAttributes](/documentation/security/cmssignedattributes)

#### Attributes

- [static var attrSmimeCapabilities: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrsmimecapabilities)
- [static var attrSmimeEncryptionKeyPrefs: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrsmimeencryptionkeyprefs)
- [static var attrSmimeMSEncryptionKeyPrefs: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrsmimemsencryptionkeyprefs)
- [static var attrSigningTime: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrsigningtime)
- [static var attrAppleCodesigningHashAgility: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrapplecodesigninghashagility)
- [static var attrAppleCodesigningHashAgilityV2: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrapplecodesigninghashagilityv2)
- [static var attrAppleExpirationTime: CMSSignedAttributes](/documentation/security/cmssignedattributes/attrappleexpirationtime)

#### Initializers

- [init(rawValue: UInt32)](/documentation/security/cmssignedattributes/init(rawvalue:))
- [func CMSEncoderSetCertificateChainMode(CMSEncoder, CMSCertificateChainMode) -> OSStatus](/documentation/security/cmsencodersetcertificatechainmode(_:_:))
- [CMSCertificateChainMode](/documentation/security/cmscertificatechainmode)

#### Constants

- [case none](/documentation/security/cmscertificatechainmode/none)
- [case signerOnly](/documentation/security/cmscertificatechainmode/signeronly)
- [case chain](/documentation/security/cmscertificatechainmode/chain)
- [case chainWithRoot](/documentation/security/cmscertificatechainmode/chainwithroot)

#### Enumeration Cases

- [case chainWithRootOrFail](/documentation/security/cmscertificatechainmode/chainwithrootorfail)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/security/cmscertificatechainmode/init(rawvalue:))
- [func CMSEncoderSetSignerAlgorithm(CMSEncoder, CFString) -> OSStatus](/documentation/security/cmsencodersetsigneralgorithm(_:_:))

### Message Characteristics

- [func CMSEncoderCopySigners(CMSEncoder, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/cmsencodercopysigners(_:_:))
- [func CMSEncoderCopyRecipients(CMSEncoder, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/cmsencodercopyrecipients(_:_:))
- [func CMSEncoderGetHasDetachedContent(CMSEncoder, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/security/cmsencodergethasdetachedcontent(_:_:))
- [func CMSEncoderCopyEncapsulatedContentType(CMSEncoder, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/cmsencodercopyencapsulatedcontenttype(_:_:))
- [func CMSEncoderCopySupportingCerts(CMSEncoder, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/cmsencodercopysupportingcerts(_:_:))
- [func CMSEncoderGetCertificateChainMode(CMSEncoder, UnsafeMutablePointer<CMSCertificateChainMode>) -> OSStatus](/documentation/security/cmsencodergetcertificatechainmode(_:_:))

### Encoding

- [func CMSEncoderUpdateContent(CMSEncoder, UnsafeRawPointer, Int) -> OSStatus](/documentation/security/cmsencoderupdatecontent(_:_:_:))
- [func CMSEncoderCopyEncodedContent(CMSEncoder, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/cmsencodercopyencodedcontent(_:_:))
- [func CMSEncodeContent(CFTypeRef?, CFTypeRef?, CFTypeRef?, Bool, CMSSignedAttributes, UnsafeRawPointer, Int, UnsafeMutablePointer<CFData?>?) -> OSStatus](/documentation/security/cmsencodecontent(_:_:_:_:_:_:_:_:))

### The Decoder

- [func CMSDecoderCreate(UnsafeMutablePointer<CMSDecoder?>) -> OSStatus](/documentation/security/cmsdecodercreate(_:))
- [CMSDecoder](/documentation/security/cmsdecoder)
- [func CMSDecoderGetTypeID() -> CFTypeID](/documentation/security/cmsdecodergettypeid())

### Decoding

- [func CMSDecoderUpdateMessage(CMSDecoder, UnsafeRawPointer, Int) -> OSStatus](/documentation/security/cmsdecoderupdatemessage(_:_:_:))
- [func CMSDecoderFinalizeMessage(CMSDecoder) -> OSStatus](/documentation/security/cmsdecoderfinalizemessage(_:))
- [func CMSDecoderSetDetachedContent(CMSDecoder, CFData) -> OSStatus](/documentation/security/cmsdecodersetdetachedcontent(_:_:))
- [func CMSDecoderCopyDetachedContent(CMSDecoder, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/cmsdecodercopydetachedcontent(_:_:))

### Signature Verification

- [func CMSDecoderSetSearchKeychain(CMSDecoder, CFTypeRef) -> OSStatus](/documentation/security/cmsdecodersetsearchkeychain(_:_:))
- [func CMSDecoderGetNumSigners(CMSDecoder, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/cmsdecodergetnumsigners(_:_:))
- [func CMSDecoderCopySignerEmailAddress(CMSDecoder, Int, UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/security/cmsdecodercopysigneremailaddress(_:_:_:))
- [func CMSDecoderCopySignerCert(CMSDecoder, Int, UnsafeMutablePointer<SecCertificate?>) -> OSStatus](/documentation/security/cmsdecodercopysignercert(_:_:_:))
- [func CMSDecoderCopySignerStatus(CMSDecoder, Int, CFTypeRef, Bool, UnsafeMutablePointer<CMSSignerStatus>?, UnsafeMutablePointer<SecTrust?>?, UnsafeMutablePointer<OSStatus>?) -> OSStatus](/documentation/security/cmsdecodercopysignerstatus(_:_:_:_:_:_:_:))
- [CMSSignerStatus](/documentation/security/cmssignerstatus)

#### Constants

- [case unsigned](/documentation/security/cmssignerstatus/unsigned)
- [case valid](/documentation/security/cmssignerstatus/valid)
- [case needsDetachedContent](/documentation/security/cmssignerstatus/needsdetachedcontent)
- [case invalidSignature](/documentation/security/cmssignerstatus/invalidsignature)
- [case invalidCert](/documentation/security/cmssignerstatus/invalidcert)
- [case invalidIndex](/documentation/security/cmssignerstatus/invalidindex)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/security/cmssignerstatus/init(rawvalue:))

### Message Content

- [func CMSDecoderIsContentEncrypted(CMSDecoder, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/security/cmsdecoderiscontentencrypted(_:_:))
- [func CMSDecoderCopyEncapsulatedContentType(CMSDecoder, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/cmsdecodercopyencapsulatedcontenttype(_:_:))
- [func CMSDecoderCopyAllCerts(CMSDecoder, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/cmsdecodercopyallcerts(_:_:))
- [func CMSDecoderCopyContent(CMSDecoder, UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/security/cmsdecodercopycontent(_:_:))

### Timestamps

- [func CMSDecoderCopySignerSigningTime(CMSDecoder, Int, UnsafeMutablePointer<CFAbsoluteTime>) -> OSStatus](/documentation/security/cmsdecodercopysignersigningtime(_:_:_:))
- [func CMSDecoderCopySignerTimestamp(CMSDecoder, Int, UnsafeMutablePointer<CFAbsoluteTime>) -> OSStatus](/documentation/security/cmsdecodercopysignertimestamp(_:_:_:))
- [func CMSDecoderCopySignerTimestampCertificates(CMSDecoder, Int, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/cmsdecodercopysignertimestampcertificates(_:_:_:))
- [func CMSDecoderCopySignerTimestampWithPolicy(CMSDecoder, CFTypeRef?, Int, UnsafeMutablePointer<CFAbsoluteTime>) -> OSStatus](/documentation/security/cmsdecodercopysignertimestampwithpolicy(_:_:_:_:))
- [func CMSEncoderCopySignerTimestamp(CMSEncoder, Int, UnsafeMutablePointer<CFAbsoluteTime>) -> OSStatus](/documentation/security/cmsencodercopysignertimestamp(_:_:_:))
- [func CMSEncoderCopySignerTimestampWithPolicy(CMSEncoder, CFTypeRef?, Int, UnsafeMutablePointer<CFAbsoluteTime>) -> OSStatus](/documentation/security/cmsencodercopysignertimestampwithpolicy(_:_:_:_:))
- [Randomization Services](/documentation/security/randomization-services)

### Random Numbers

- [func SecRandomCopyBytes(SecRandomRef?, Int, UnsafeMutableRawPointer) -> Int32](/documentation/security/secrandomcopybytes(_:_:_:))
- [SecRandomRef](/documentation/security/secrandomref)
- [let kSecRandomDefault: SecRandomRef](/documentation/security/ksecrandomdefault)
- [Security Transforms](/documentation/security/security-transforms)

### Transforms

- [func SecTransformCreateReadTransformWithReadStream(CFReadStream) -> SecTransform](/documentation/security/sectransformcreatereadtransformwithreadstream(_:))
- [SecTransform](/documentation/security/sectransform)
- [func SecTransformGetTypeID() -> CFTypeID](/documentation/security/sectransformgettypeid())

### Encoding

- [func SecEncodeTransformCreate(CFTypeRef, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/secencodetransformcreate(_:_:))
- [func SecDecodeTransformCreate(CFTypeRef, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/secdecodetransformcreate(_:_:))

### Encrypting

- [func SecEncryptTransformCreate(SecKey, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform](/documentation/security/secencrypttransformcreate(_:_:))
- [func SecDecryptTransformCreate(SecKey, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform](/documentation/security/secdecrypttransformcreate(_:_:))
- [func SecEncryptTransformGetTypeID() -> CFTypeID](/documentation/security/secencrypttransformgettypeid())
- [func SecDecryptTransformGetTypeID() -> CFTypeID](/documentation/security/secdecrypttransformgettypeid())

### Signing

- [func SecSignTransformCreate(SecKey, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/secsigntransformcreate(_:_:))
- [func SecVerifyTransformCreate(SecKey, CFData?, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/secverifytransformcreate(_:_:_:))
- [func SecDigestTransformCreate(CFTypeRef?, CFIndex, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform](/documentation/security/secdigesttransformcreate(_:_:_:))
- [func SecDigestTransformGetTypeID() -> CFTypeID](/documentation/security/secdigesttransformgettypeid())

### Custom Transforms

- [func SecTransformCreate(CFString, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/sectransformcreate(_:_:))
- [func SecTransformRegister(CFString, SecTransformCreateFP, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/security/sectransformregister(_:_:_:))
- [SecTransformCreateFP](/documentation/security/sectransformcreatefp)
- [SecTransformInstanceBlock](/documentation/security/sectransforminstanceblock)
- [SecTransformImplementationRef](/documentation/security/sectransformimplementationref)

### Transform Groups

- [func SecTransformCreateGroupTransform() -> SecGroupTransform](/documentation/security/sectransformcreategrouptransform())
- [func SecTransformFindByName(SecGroupTransform, CFString) -> SecTransform?](/documentation/security/sectransformfindbyname(_:_:))
- [SecGroupTransform](/documentation/security/secgrouptransform)
- [func SecGroupTransformGetTypeID() -> CFTypeID](/documentation/security/secgrouptransformgettypeid())

### Transform Characteristics

- [func SecTransformSetAttribute(SecTransform, CFString, CFTypeRef, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> Bool](/documentation/security/sectransformsetattribute(_:_:_:_:))
- [func SecTransformGetAttribute(SecTransform, CFString) -> CFTypeRef?](/documentation/security/sectransformgetattribute(_:_:))
- [func SecTransformCustomSetAttribute(SecTransformImplementationRef, SecTransformStringOrAttribute, SecTransformMetaAttributeType, CFTypeRef?) -> CFTypeRef?](/documentation/security/sectransformcustomsetattribute(_:_:_:_:))
- [func SecTransformCustomGetAttribute(SecTransformImplementationRef, SecTransformStringOrAttribute, SecTransformMetaAttributeType) -> CFTypeRef?](/documentation/security/sectransformcustomgetattribute(_:_:_:))
- [func SecTransformPushbackAttribute(SecTransformImplementationRef, SecTransformStringOrAttribute, CFTypeRef) -> CFTypeRef?](/documentation/security/sectransformpushbackattribute(_:_:_:))
- [Transform Attributes](/documentation/security/transform-attributes)

#### Encode and Decode Keys

- [let kSecEncodeLineLengthAttribute: CFString](/documentation/security/ksecencodelinelengthattribute)
- [let kSecEncodeTypeAttribute: CFString](/documentation/security/ksecencodetypeattribute)
- [let kSecDecodeTypeAttribute: CFString](/documentation/security/ksecdecodetypeattribute)
- [let kSecCompressionRatio: CFString](/documentation/security/kseccompressionratio)

#### Digest and Encryption Keys

- [let kSecDigestTypeAttribute: CFString](/documentation/security/ksecdigesttypeattribute)
- [let kSecDigestLengthAttribute: CFString](/documentation/security/ksecdigestlengthattribute)
- [let kSecDigestHMACKeyAttribute: CFString](/documentation/security/ksecdigesthmackeyattribute)
- [let kSecInputIsAttributeName: CFString](/documentation/security/ksecinputisattributename)
- [let kSecEncryptionMode: CFString](/documentation/security/ksecencryptionmode)
- [let kSecEncryptKey: CFString](/documentation/security/ksecencryptkey)
- [let kSecIVKey: CFString](/documentation/security/ksecivkey)
- [let kSecPaddingKey: CFString](/documentation/security/ksecpaddingkey)
- [let kSecOAEPEncodingParametersAttributeName: CFString](/documentation/security/ksecoaepencodingparametersattributename)
- [let kSecOAEPMGF1DigestAlgorithmAttributeName: CFString](/documentation/security/ksecoaepmgf1digestalgorithmattributename)
- [let kSecOAEPMessageLengthAttributeName: CFString](/documentation/security/ksecoaepmessagelengthattributename)

#### Transform Keys

- [let kSecTransformInputAttributeName: CFString](/documentation/security/ksectransforminputattributename)
- [let kSecTransformOutputAttributeName: CFString](/documentation/security/ksectransformoutputattributename)
- [let kSecTransformDebugAttributeName: CFString](/documentation/security/ksectransformdebugattributename)
- [let kSecKeyAttributeName: CFString](/documentation/security/kseckeyattributename)
- [let kSecSignatureAttributeName: CFString](/documentation/security/ksecsignatureattributename)
- [let kSecTransformAbortAttributeName: CFString](/documentation/security/ksectransformabortattributename)
- [let kSecTransformTransformName: CFString](/documentation/security/ksectransformtransformname)

#### Encode Types

- [let kSecBase32Encoding: CFString](/documentation/security/ksecbase32encoding)
- [let kSecBase64Encoding: CFString](/documentation/security/ksecbase64encoding)
- [let kSecZLibEncoding: CFString](/documentation/security/kseczlibencoding)

#### Digest Types

- [let kSecDigestMD2: CFString](/documentation/security/ksecdigestmd2)
- [let kSecDigestMD4: CFString](/documentation/security/ksecdigestmd4)
- [let kSecDigestMD5: CFString](/documentation/security/ksecdigestmd5)
- [let kSecDigestSHA1: CFString](/documentation/security/ksecdigestsha1)
- [let kSecDigestSHA2: CFString](/documentation/security/ksecdigestsha2)
- [let kSecDigestHMACMD5: CFString](/documentation/security/ksecdigesthmacmd5)
- [let kSecDigestHMACSHA1: CFString](/documentation/security/ksecdigesthmacsha1)
- [let kSecDigestHMACSHA2: CFString](/documentation/security/ksecdigesthmacsha2)

#### Line Lengths

- [let kSecLineLength64: CFString](/documentation/security/kseclinelength64)
- [let kSecLineLength76: CFString](/documentation/security/kseclinelength76)

#### Input Types

- [let kSecInputIsDigest: CFString](/documentation/security/ksecinputisdigest)
- [let kSecInputIsPlainText: CFString](/documentation/security/ksecinputisplaintext)
- [let kSecInputIsRaw: CFString](/documentation/security/ksecinputisraw)

#### Padding Types

- [let kSecPaddingNoneKey: CFString](/documentation/security/ksecpaddingnonekey)
- [let kSecPaddingOAEPKey: CFString](/documentation/security/ksecpaddingoaepkey)
- [let kSecPaddingPKCS1Key: CFString](/documentation/security/ksecpaddingpkcs1key)
- [let kSecPaddingPKCS5Key: CFString](/documentation/security/ksecpaddingpkcs5key)
- [let kSecPaddingPKCS7Key: CFString](/documentation/security/ksecpaddingpkcs7key)

#### Encryption Modes

- [let kSecModeNoneKey: CFString](/documentation/security/ksecmodenonekey)
- [let kSecModeCBCKey: CFString](/documentation/security/ksecmodecbckey)
- [let kSecModeCFBKey: CFString](/documentation/security/ksecmodecfbkey)
- [let kSecModeECBKey: CFString](/documentation/security/ksecmodeecbkey)
- [let kSecModeOFBKey: CFString](/documentation/security/ksecmodeofbkey)
- [SecTransformAttribute](/documentation/security/sectransformattribute)
- [SecTransformStringOrAttribute](/documentation/security/sectransformstringorattribute)
- [SecTransformMetaAttributeType](/documentation/security/sectransformmetaattributetype)

#### Constants

- [case canCycle](/documentation/security/sectransformmetaattributetype/cancycle)
- [case deferred](/documentation/security/sectransformmetaattributetype/deferred)
- [case externalize](/documentation/security/sectransformmetaattributetype/externalize)
- [case hasInboundConnection](/documentation/security/sectransformmetaattributetype/hasinboundconnection)
- [case hasOutboundConnections](/documentation/security/sectransformmetaattributetype/hasoutboundconnections)
- [case name](/documentation/security/sectransformmetaattributetype/name)
- [case ref](/documentation/security/sectransformmetaattributetype/ref)
- [case required](/documentation/security/sectransformmetaattributetype/required)
- [case requiresOutboundConnection](/documentation/security/sectransformmetaattributetype/requiresoutboundconnection)
- [case stream](/documentation/security/sectransformmetaattributetype/stream)
- [case value](/documentation/security/sectransformmetaattributetype/value)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/security/sectransformmetaattributetype/init(rawvalue:))

### Actions

- [func SecTransformSetDataAction(SecTransformImplementationRef, CFString, SecTransformDataBlock) -> CFError?](/documentation/security/sectransformsetdataaction(_:_:_:))
- [func SecTransformSetAttributeAction(SecTransformImplementationRef, CFString, SecTransformStringOrAttribute?, SecTransformAttributeActionBlock) -> CFError?](/documentation/security/sectransformsetattributeaction(_:_:_:_:))
- [func SecTransformSetTransformAction(SecTransformImplementationRef, CFString, SecTransformActionBlock) -> CFError?](/documentation/security/sectransformsettransformaction(_:_:_:))
- [SecTransformActionBlock](/documentation/security/sectransformactionblock)
- [SecTransformAttributeActionBlock](/documentation/security/sectransformattributeactionblock)
- [SecTransformDataBlock](/documentation/security/sectransformdatablock)
- [Actions](/documentation/security/actions)

#### Constants

- [let kSecTransformActionAttributeNotification: CFString](/documentation/security/ksectransformactionattributenotification)
- [let kSecTransformActionAttributeValidation: CFString](/documentation/security/ksectransformactionattributevalidation)
- [let kSecTransformActionCanExecute: CFString](/documentation/security/ksectransformactioncanexecute)
- [let kSecTransformActionExternalizeExtraData: CFString](/documentation/security/ksectransformactionexternalizeextradata)
- [let kSecTransformActionFinalize: CFString](/documentation/security/ksectransformactionfinalize)
- [let kSecTransformActionInternalizeExtraData: CFString](/documentation/security/ksectransformactioninternalizeextradata)
- [let kSecTransformActionProcessData: CFString](/documentation/security/ksectransformactionprocessdata)
- [let kSecTransformActionStartingExecution: CFString](/documentation/security/ksectransformactionstartingexecution)

### Piping

- [func SecTransformConnectTransforms(SecTransform, CFString, SecTransform, CFString, SecGroupTransform, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecGroupTransform?](/documentation/security/sectransformconnecttransforms(_:_:_:_:_:_:))

### Execution

- [func SecTransformExecute(SecTransform, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> CFTypeRef](/documentation/security/sectransformexecute(_:_:))
- [func SecTransformExecuteAsync(SecTransform, dispatch_queue_t, SecMessageBlock)](/documentation/security/sectransformexecuteasync(_:_:_:))
- [func SecTransformNoData() -> CFTypeRef](/documentation/security/sectransformnodata())
- [SecMessageBlock](/documentation/security/secmessageblock)

### Import and Export

- [func SecTransformCopyExternalRepresentation(SecTransform) -> CFDictionary](/documentation/security/sectransformcopyexternalrepresentation(_:))
- [func SecTransformCreateFromExternalRepresentation(CFDictionary, UnsafeMutablePointer<Unmanaged<CFError>?>?) -> SecTransform?](/documentation/security/sectransformcreatefromexternalrepresentation(_:_:))

### Reporting Errors

- [let kSecTransformErrorDomain: CFString](/documentation/security/ksectransformerrordomain)
- [Security Transform Error Codes](/documentation/security/security-transform-error-codes)

#### Constants

- [var kSecTransformErrorAttributeNotFound: CFIndex](/documentation/security/ksectransformerrorattributenotfound)
- [var kSecTransformErrorInvalidOperation: CFIndex](/documentation/security/ksectransformerrorinvalidoperation)
- [var kSecTransformErrorNotInitializedCorrectly: CFIndex](/documentation/security/ksectransformerrornotinitializedcorrectly)
- [var kSecTransformErrorMoreThanOneOutput: CFIndex](/documentation/security/ksectransformerrormorethanoneoutput)
- [var kSecTransformErrorInvalidInputDictionary: CFIndex](/documentation/security/ksectransformerrorinvalidinputdictionary)
- [var kSecTransformErrorInvalidAlgorithm: CFIndex](/documentation/security/ksectransformerrorinvalidalgorithm)
- [var kSecTransformErrorInvalidLength: CFIndex](/documentation/security/ksectransformerrorinvalidlength)
- [var kSecTransformErrorInvalidType: CFIndex](/documentation/security/ksectransformerrorinvalidtype)
- [var kSecTransformErrorInvalidInput: CFIndex](/documentation/security/ksectransformerrorinvalidinput)
- [var kSecTransformErrorNameAlreadyRegistered: CFIndex](/documentation/security/ksectransformerrornamealreadyregistered)
- [var kSecTransformErrorUnsupportedAttribute: CFIndex](/documentation/security/ksectransformerrorunsupportedattribute)
- [var kSecTransformOperationNotSupportedOnGroup: CFIndex](/documentation/security/ksectransformoperationnotsupportedongroup)
- [var kSecTransformErrorMissingParameter: CFIndex](/documentation/security/ksectransformerrormissingparameter)
- [var kSecTransformErrorInvalidConnection: CFIndex](/documentation/security/ksectransformerrorinvalidconnection)
- [var kSecTransformTransformIsExecuting: CFIndex](/documentation/security/ksectransformtransformisexecuting)
- [var kSecTransformInvalidOverride: CFIndex](/documentation/security/ksectransforminvalidoverride)
- [var kSecTransformTransformIsNotRegistered: CFIndex](/documentation/security/ksectransformtransformisnotregistered)
- [var kSecTransformErrorAbortInProgress: CFIndex](/documentation/security/ksectransformerrorabortinprogress)
- [var kSecTransformErrorAborted: CFIndex](/documentation/security/ksectransformerroraborted)
- [var kSecTransformInvalidArgument: CFIndex](/documentation/security/ksectransforminvalidargument)
- [let kSecTransformPreviousErrorKey: CFString](/documentation/security/ksectransformpreviouserrorkey)
- [let kSecTransformAbortOriginatorKey: CFString](/documentation/security/ksectransformabortoriginatorkey)
- [ASN.1](/documentation/security/asn-1)

### Encoding

- [SecAsn1Item](/documentation/security/secasn1item)
- [SecAsn1Template_struct](/documentation/security/secasn1template_struct)

#### Initializers

- [init(kind: UInt32, offset: UInt32, sub: UnsafeRawPointer, size: UInt32)](/documentation/security/secasn1template_struct/init(kind:offset:sub:size:))

#### Instance Properties

- [var kind: UInt32](/documentation/security/secasn1template_struct/kind)
- [var offset: UInt32](/documentation/security/secasn1template_struct/offset)
- [var size: UInt32](/documentation/security/secasn1template_struct/size)
- [var sub: UnsafeRawPointer](/documentation/security/secasn1template_struct/sub)
- [SecAsn1Template_struct](/documentation/security/secasn1template_struct)

#### Initializers

- [init(kind: UInt32, offset: UInt32, sub: UnsafeRawPointer, size: UInt32)](/documentation/security/secasn1template_struct/init(kind:offset:sub:size:))

#### Instance Properties

- [var kind: UInt32](/documentation/security/secasn1template_struct/kind)
- [var offset: UInt32](/documentation/security/secasn1template_struct/offset)
- [var size: UInt32](/documentation/security/secasn1template_struct/size)
- [var sub: UnsafeRawPointer](/documentation/security/secasn1template_struct/sub)
- [SecAsn1TemplateChooser](/documentation/security/secasn1templatechooser)
- [SecAsn1TemplateChooserPtr](/documentation/security/secasn1templatechooserptr)
- [Type Tags](/documentation/security/type-tags)

#### The Tag Mask

- [var SEC_ASN1_TAG_MASK: Int32](/documentation/security/sec_asn1_tag_mask)

#### Universal Type Tags

- [var SEC_ASN1_TAGNUM_MASK: Int32](/documentation/security/sec_asn1_tagnum_mask)
- [var SEC_ASN1_BOOLEAN: Int32](/documentation/security/sec_asn1_boolean)
- [var SEC_ASN1_INTEGER: Int32](/documentation/security/sec_asn1_integer)
- [var SEC_ASN1_BIT_STRING: Int32](/documentation/security/sec_asn1_bit_string)
- [var SEC_ASN1_OCTET_STRING: Int32](/documentation/security/sec_asn1_octet_string)
- [var SEC_ASN1_NULL: Int32](/documentation/security/sec_asn1_null)
- [var SEC_ASN1_OBJECT_ID: Int32](/documentation/security/sec_asn1_object_id)
- [var SEC_ASN1_OBJECT_DESCRIPTOR: Int32](/documentation/security/sec_asn1_object_descriptor)
- [var SEC_ASN1_REAL: Int32](/documentation/security/sec_asn1_real)
- [var SEC_ASN1_ENUMERATED: Int32](/documentation/security/sec_asn1_enumerated)
- [var SEC_ASN1_EMBEDDED_PDV: Int32](/documentation/security/sec_asn1_embedded_pdv)
- [var SEC_ASN1_UTF8_STRING: Int32](/documentation/security/sec_asn1_utf8_string)
- [var SEC_ASN1_SEQUENCE: Int32](/documentation/security/sec_asn1_sequence)
- [var SEC_ASN1_SET: Int32](/documentation/security/sec_asn1_set)
- [var SEC_ASN1_NUMERIC_STRING: Int32](/documentation/security/sec_asn1_numeric_string)
- [var SEC_ASN1_PRINTABLE_STRING: Int32](/documentation/security/sec_asn1_printable_string)
- [var SEC_ASN1_T61_STRING: Int32](/documentation/security/sec_asn1_t61_string)
- [var SEC_ASN1_VIDEOTEX_STRING: Int32](/documentation/security/sec_asn1_videotex_string)
- [var SEC_ASN1_IA5_STRING: Int32](/documentation/security/sec_asn1_ia5_string)
- [var SEC_ASN1_UTC_TIME: Int32](/documentation/security/sec_asn1_utc_time)
- [var SEC_ASN1_GENERALIZED_TIME: Int32](/documentation/security/sec_asn1_generalized_time)
- [var SEC_ASN1_GRAPHIC_STRING: Int32](/documentation/security/sec_asn1_graphic_string)
- [var SEC_ASN1_VISIBLE_STRING: Int32](/documentation/security/sec_asn1_visible_string)
- [var SEC_ASN1_GENERAL_STRING: Int32](/documentation/security/sec_asn1_general_string)
- [var SEC_ASN1_UNIVERSAL_STRING: Int32](/documentation/security/sec_asn1_universal_string)
- [var SEC_ASN1_BMP_STRING: Int32](/documentation/security/sec_asn1_bmp_string)
- [var SEC_ASN1_HIGH_TAG_NUMBER: Int32](/documentation/security/sec_asn1_high_tag_number)
- [var SEC_ASN1_TELETEX_STRING: Int32](/documentation/security/sec_asn1_teletex_string)

#### Type Tag Modifiers

- [var SEC_ASN1_METHOD_MASK: Int32](/documentation/security/sec_asn1_method_mask)
- [var SEC_ASN1_PRIMITIVE: Int32](/documentation/security/sec_asn1_primitive)
- [var SEC_ASN1_CONSTRUCTED: Int32](/documentation/security/sec_asn1_constructed)
- [var SEC_ASN1_CLASS_MASK: Int32](/documentation/security/sec_asn1_class_mask)
- [var SEC_ASN1_UNIVERSAL: Int32](/documentation/security/sec_asn1_universal)
- [var SEC_ASN1_APPLICATION: Int32](/documentation/security/sec_asn1_application)
- [var SEC_ASN1_CONTEXT_SPECIFIC: Int32](/documentation/security/sec_asn1_context_specific)
- [var SEC_ASN1_PRIVATE: Int32](/documentation/security/sec_asn1_private)

#### Apple Specific Additions

- [var SEC_ASN1_OPTIONAL: Int32](/documentation/security/sec_asn1_optional)
- [var SEC_ASN1_EXPLICIT: Int32](/documentation/security/sec_asn1_explicit)
- [var SEC_ASN1_ANY: Int32](/documentation/security/sec_asn1_any)
- [var SEC_ASN1_INLINE: Int32](/documentation/security/sec_asn1_inline)
- [var SEC_ASN1_POINTER: Int32](/documentation/security/sec_asn1_pointer)
- [var SEC_ASN1_GROUP: Int32](/documentation/security/sec_asn1_group)
- [var SEC_ASN1_DYNAMIC: Int32](/documentation/security/sec_asn1_dynamic)
- [var SEC_ASN1_SKIP: Int32](/documentation/security/sec_asn1_skip)
- [var SEC_ASN1_INNER: Int32](/documentation/security/sec_asn1_inner)
- [var SEC_ASN1_SAVE: Int32](/documentation/security/sec_asn1_save)
- [var SEC_ASN1_SKIP_REST: Int32](/documentation/security/sec_asn1_skip_rest)
- [var SEC_ASN1_CHOICE: Int32](/documentation/security/sec_asn1_choice)
- [var SEC_ASN1_SIGNED_INT: Int32](/documentation/security/sec_asn1_signed_int)
- [var SEC_ASN1_ANY_CONTENTS: Int32](/documentation/security/sec_asn1_any_contents)
- [var SEC_ASN1_SEQUENCE_OF: Int32](/documentation/security/sec_asn1_sequence_of)
- [var SEC_ASN1_SET_OF: Int32](/documentation/security/sec_asn1_set_of)

### OID Comparison

- [SecAsn1Oid](/documentation/security/secasn1oid)

### Public Key Info

- [SecAsn1AlgId](/documentation/security/secasn1algid)

#### Algorithm Characteristics

- [var algorithm: SecAsn1Oid](/documentation/security/secasn1algid/algorithm)
- [var parameters: SecAsn1Item](/documentation/security/secasn1algid/parameters)

#### Creating a Structure

- [init()](/documentation/security/secasn1algid/init())
- [init(algorithm: SecAsn1Oid, parameters: SecAsn1Item)](/documentation/security/secasn1algid/init(algorithm:parameters:))
- [SecAsn1PubKeyInfo](/documentation/security/secasn1pubkeyinfo)

#### Public Key Characteristics

- [var subjectPublicKey: SecAsn1Item](/documentation/security/secasn1pubkeyinfo/subjectpublickey)
- [var algorithm: SecAsn1AlgId](/documentation/security/secasn1pubkeyinfo/algorithm)

#### Creating a Public Key

- [init()](/documentation/security/secasn1pubkeyinfo/init())
- [init(algorithm: SecAsn1AlgId, subjectPublicKey: SecAsn1Item)](/documentation/security/secasn1pubkeyinfo/init(algorithm:subjectpublickey:))

## Result codes

- [Security Framework Result Codes](/documentation/security/security-framework-result-codes)

### Result Strings

- [func SecCopyErrorMessageString(OSStatus, UnsafeMutableRawPointer?) -> CFString?](/documentation/security/seccopyerrormessagestring(_:_:))

### System Result Codes

- [var errSecSuccess: OSStatus](/documentation/security/errsecsuccess)
- [var errSecUnimplemented: OSStatus](/documentation/security/errsecunimplemented)
- [var errSecDskFull: OSStatus](/documentation/security/errsecdskfull)
- [var errSecDiskFull: OSStatus](/documentation/security/errsecdiskfull)
- [var errSecIO: OSStatus](/documentation/security/errsecio)
- [var errSecOpWr: OSStatus](/documentation/security/errsecopwr)
- [var errSecParam: OSStatus](/documentation/security/errsecparam)
- [var errSecWrPerm: OSStatus](/documentation/security/errsecwrperm)
- [var errSecAllocate: OSStatus](/documentation/security/errsecallocate)
- [var errSecUserCanceled: OSStatus](/documentation/security/errsecusercanceled)
- [var errSecBadReq: OSStatus](/documentation/security/errsecbadreq)

### Internal Error Result Codes

- [var errSecInternalComponent: OSStatus](/documentation/security/errsecinternalcomponent)
- [var errSecCoreFoundationUnknown: OSStatus](/documentation/security/errseccorefoundationunknown)
- [var errSecInternalError: OSStatus](/documentation/security/errsecinternalerror)

### Keychain Result Codes

- [var errSecNotAvailable: OSStatus](/documentation/security/errsecnotavailable)
- [var errSecReadOnly: OSStatus](/documentation/security/errsecreadonly)
- [var errSecAuthFailed: OSStatus](/documentation/security/errsecauthfailed)
- [var errSecNoSuchKeychain: OSStatus](/documentation/security/errsecnosuchkeychain)
- [var errSecInvalidKeychain: OSStatus](/documentation/security/errsecinvalidkeychain)
- [var errSecDuplicateKeychain: OSStatus](/documentation/security/errsecduplicatekeychain)
- [var errSecDuplicateCallback: OSStatus](/documentation/security/errsecduplicatecallback)
- [var errSecInvalidCallback: OSStatus](/documentation/security/errsecinvalidcallback)
- [var errSecDuplicateItem: OSStatus](/documentation/security/errsecduplicateitem)
- [var errSecItemNotFound: OSStatus](/documentation/security/errsecitemnotfound)
- [var errSecBufferTooSmall: OSStatus](/documentation/security/errsecbuffertoosmall)
- [var errSecDataTooLarge: OSStatus](/documentation/security/errsecdatatoolarge)
- [var errSecNoSuchAttr: OSStatus](/documentation/security/errsecnosuchattr)
- [var errSecInvalidItemRef: OSStatus](/documentation/security/errsecinvaliditemref)
- [var errSecInvalidSearchRef: OSStatus](/documentation/security/errsecinvalidsearchref)
- [var errSecNoSuchClass: OSStatus](/documentation/security/errsecnosuchclass)
- [var errSecNoDefaultKeychain: OSStatus](/documentation/security/errsecnodefaultkeychain)
- [var errSecInteractionNotAllowed: OSStatus](/documentation/security/errsecinteractionnotallowed)
- [var errSecReadOnlyAttr: OSStatus](/documentation/security/errsecreadonlyattr)
- [var errSecWrongSecVersion: OSStatus](/documentation/security/errsecwrongsecversion)
- [var errSecKeySizeNotAllowed: OSStatus](/documentation/security/errseckeysizenotallowed)
- [var errSecNoStorageModule: OSStatus](/documentation/security/errsecnostoragemodule)
- [var errSecNoCertificateModule: OSStatus](/documentation/security/errsecnocertificatemodule)
- [var errSecNoPolicyModule: OSStatus](/documentation/security/errsecnopolicymodule)
- [var errSecInteractionRequired: OSStatus](/documentation/security/errsecinteractionrequired)
- [var errSecDataNotAvailable: OSStatus](/documentation/security/errsecdatanotavailable)
- [var errSecDataNotModifiable: OSStatus](/documentation/security/errsecdatanotmodifiable)
- [var errSecCreateChainFailed: OSStatus](/documentation/security/errseccreatechainfailed)
- [var errSecInvalidPrefsDomain: OSStatus](/documentation/security/errsecinvalidprefsdomain)
- [var errSecInDarkWake: OSStatus](/documentation/security/errsecindarkwake)

### Certificate Result Codes

- [var errSecUnknownCriticalExtensionFlag: OSStatus](/documentation/security/errsecunknowncriticalextensionflag)
- [var errSecCertificateCannotOperate: OSStatus](/documentation/security/errseccertificatecannotoperate)
- [var errSecCertificateExpired: OSStatus](/documentation/security/errseccertificateexpired)
- [var errSecCertificateNotValidYet: OSStatus](/documentation/security/errseccertificatenotvalidyet)
- [var errSecCertificateRevoked: OSStatus](/documentation/security/errseccertificaterevoked)
- [var errSecCertificateSuspended: OSStatus](/documentation/security/errseccertificatesuspended)
- [var errSecInvalidCertAuthority: OSStatus](/documentation/security/errsecinvalidcertauthority)
- [var errSecInvalidCertificateGroup: OSStatus](/documentation/security/errsecinvalidcertificategroup)
- [var errSecInvalidCertificateRef: OSStatus](/documentation/security/errsecinvalidcertificateref)
- [var errSecCertificateNameNotAllowed: OSStatus](/documentation/security/errseccertificatenamenotallowed)
- [var errSecCertificatePolicyNotAllowed: OSStatus](/documentation/security/errseccertificatepolicynotallowed)
- [var errSecCertificateValidityPeriodTooLong: OSStatus](/documentation/security/errseccertificatevalidityperiodtoolong)

### ACL Result Codes

- [var errSecACLAddFailed: OSStatus](/documentation/security/errsecacladdfailed)
- [var errSecACLChangeFailed: OSStatus](/documentation/security/errsecaclchangefailed)
- [var errSecACLDeleteFailed: OSStatus](/documentation/security/errsecacldeletefailed)
- [var errSecACLNotSimple: OSStatus](/documentation/security/errsecaclnotsimple)
- [var errSecACLReplaceFailed: OSStatus](/documentation/security/errsecaclreplacefailed)
- [var errSecAppleAddAppACLSubject: OSStatus](/documentation/security/errsecappleaddappaclsubject)
- [var errSecInvalidBaseACLs: OSStatus](/documentation/security/errsecinvalidbaseacls)
- [var errSecInvalidACL: OSStatus](/documentation/security/errsecinvalidacl)

### CRL Result Codes

- [var errSecCRLExpired: OSStatus](/documentation/security/errseccrlexpired)
- [var errSecCRLNotValidYet: OSStatus](/documentation/security/errseccrlnotvalidyet)
- [var errSecCRLNotFound: OSStatus](/documentation/security/errseccrlnotfound)
- [var errSecCRLServerDown: OSStatus](/documentation/security/errseccrlserverdown)
- [var errSecCRLBadURI: OSStatus](/documentation/security/errseccrlbaduri)
- [var errSecCRLNotTrusted: OSStatus](/documentation/security/errseccrlnottrusted)
- [var errSecUnknownCertExtension: OSStatus](/documentation/security/errsecunknowncertextension)
- [var errSecUnknownCRLExtension: OSStatus](/documentation/security/errsecunknowncrlextension)
- [var errSecCRLPolicyFailed: OSStatus](/documentation/security/errseccrlpolicyfailed)
- [var errSecCRLAlreadySigned: OSStatus](/documentation/security/errseccrlalreadysigned)
- [var errSecIDPFailure: OSStatus](/documentation/security/errsecidpfailure)
- [var errSecInvalidCRLEncoding: OSStatus](/documentation/security/errsecinvalidcrlencoding)
- [var errSecInvalidCRLType: OSStatus](/documentation/security/errsecinvalidcrltype)
- [var errSecInvalidCRL: OSStatus](/documentation/security/errsecinvalidcrl)
- [var errSecInvalidCRLGroup: OSStatus](/documentation/security/errsecinvalidcrlgroup)
- [var errSecInvalidCRLIndex: OSStatus](/documentation/security/errsecinvalidcrlindex)
- [var errSecInvaldCRLAuthority: OSStatus](/documentation/security/errsecinvaldcrlauthority)

### SMIME Result Codes

- [var errSecSMIMEEmailAddressesNotFound: OSStatus](/documentation/security/errsecsmimeemailaddressesnotfound)
- [var errSecSMIMEBadExtendedKeyUsage: OSStatus](/documentation/security/errsecsmimebadextendedkeyusage)
- [var errSecSMIMEBadKeyUsage: OSStatus](/documentation/security/errsecsmimebadkeyusage)
- [var errSecSMIMEKeyUsageNotCritical: OSStatus](/documentation/security/errsecsmimekeyusagenotcritical)
- [var errSecSMIMENoEmailAddress: OSStatus](/documentation/security/errsecsmimenoemailaddress)
- [var errSecSMIMESubjAltNameNotCritical: OSStatus](/documentation/security/errsecsmimesubjaltnamenotcritical)
- [var errSecSSLBadExtendedKeyUsage: OSStatus](/documentation/security/errsecsslbadextendedkeyusage)

### OCSP Result Codes

- [var errSecOCSPBadResponse: OSStatus](/documentation/security/errsecocspbadresponse)
- [var errSecOCSPBadRequest: OSStatus](/documentation/security/errsecocspbadrequest)
- [var errSecOCSPUnavailable: OSStatus](/documentation/security/errsecocspunavailable)
- [var errSecOCSPStatusUnrecognized: OSStatus](/documentation/security/errsecocspstatusunrecognized)
- [var errSecEndOfData: OSStatus](/documentation/security/errsecendofdata)
- [var errSecIncompleteCertRevocationCheck: OSStatus](/documentation/security/errsecincompletecertrevocationcheck)
- [var errSecNetworkFailure: OSStatus](/documentation/security/errsecnetworkfailure)
- [var errSecOCSPNotTrustedToAnchor: OSStatus](/documentation/security/errsecocspnottrustedtoanchor)
- [var errSecRecordModified: OSStatus](/documentation/security/errsecrecordmodified)
- [var errSecOCSPSignatureError: OSStatus](/documentation/security/errsecocspsignatureerror)
- [var errSecOCSPNoSigner: OSStatus](/documentation/security/errsecocspnosigner)
- [var errSecOCSPResponderMalformedReq: OSStatus](/documentation/security/errsecocsprespondermalformedreq)
- [var errSecOCSPResponderInternalError: OSStatus](/documentation/security/errsecocspresponderinternalerror)
- [var errSecOCSPResponderTryLater: OSStatus](/documentation/security/errsecocsprespondertrylater)
- [var errSecOCSPResponderSignatureRequired: OSStatus](/documentation/security/errsecocsprespondersignaturerequired)
- [var errSecOCSPResponderUnauthorized: OSStatus](/documentation/security/errsecocspresponderunauthorized)
- [var errSecOCSPResponseNonceMismatch: OSStatus](/documentation/security/errsecocspresponsenoncemismatch)

### Code Signing Result Codes

- [var errSecCodeSigningBadCertChainLength: OSStatus](/documentation/security/errseccodesigningbadcertchainlength)
- [var errSecCodeSigningNoBasicConstraints: OSStatus](/documentation/security/errseccodesigningnobasicconstraints)
- [var errSecCodeSigningBadPathLengthConstraint: OSStatus](/documentation/security/errseccodesigningbadpathlengthconstraint)
- [var errSecCodeSigningNoExtendedKeyUsage: OSStatus](/documentation/security/errseccodesigningnoextendedkeyusage)
- [var errSecCodeSigningDevelopment: OSStatus](/documentation/security/errseccodesigningdevelopment)
- [var errSecResourceSignBadCertChainLength: OSStatus](/documentation/security/errsecresourcesignbadcertchainlength)
- [var errSecResourceSignBadExtKeyUsage: OSStatus](/documentation/security/errsecresourcesignbadextkeyusage)
- [var errSecTrustSettingDeny: OSStatus](/documentation/security/errsectrustsettingdeny)
- [var errSecInvalidSubjectName: OSStatus](/documentation/security/errsecinvalidsubjectname)
- [var errSecUnknownQualifiedCertStatement: OSStatus](/documentation/security/errsecunknownqualifiedcertstatement)

### Mobile Me Result Codes

- [var errSecMobileMeRequestQueued: OSStatus](/documentation/security/errsecmobilemerequestqueued)
- [var errSecMobileMeRequestRedirected: OSStatus](/documentation/security/errsecmobilemerequestredirected)
- [var errSecMobileMeServerError: OSStatus](/documentation/security/errsecmobilemeservererror)
- [var errSecMobileMeServerNotAvailable: OSStatus](/documentation/security/errsecmobilemeservernotavailable)
- [var errSecMobileMeServerAlreadyExists: OSStatus](/documentation/security/errsecmobilemeserveralreadyexists)
- [var errSecMobileMeServerServiceErr: OSStatus](/documentation/security/errsecmobilemeserverserviceerr)
- [var errSecMobileMeRequestAlreadyPending: OSStatus](/documentation/security/errsecmobilemerequestalreadypending)
- [var errSecMobileMeNoRequestPending: OSStatus](/documentation/security/errsecmobilemenorequestpending)
- [var errSecMobileMeCSRVerifyFailure: OSStatus](/documentation/security/errsecmobilemecsrverifyfailure)
- [var errSecMobileMeFailedConsistencyCheck: OSStatus](/documentation/security/errsecmobilemefailedconsistencycheck)

### Cryptographic Key Result Codes

- [var errSecKeyUsageIncorrect: OSStatus](/documentation/security/errseckeyusageincorrect)
- [var errSecKeyBlobTypeIncorrect: OSStatus](/documentation/security/errseckeyblobtypeincorrect)
- [var errSecKeyHeaderInconsistent: OSStatus](/documentation/security/errseckeyheaderinconsistent)
- [var errSecKeyIsSensitive: OSStatus](/documentation/security/errseckeyissensitive)
- [var errSecUnsupportedKeyFormat: OSStatus](/documentation/security/errsecunsupportedkeyformat)
- [var errSecUnsupportedKeySize: OSStatus](/documentation/security/errsecunsupportedkeysize)
- [var errSecInvalidKeyUsageMask: OSStatus](/documentation/security/errsecinvalidkeyusagemask)
- [var errSecUnsupportedKeyUsageMask: OSStatus](/documentation/security/errsecunsupportedkeyusagemask)
- [var errSecInvalidKeyAttributeMask: OSStatus](/documentation/security/errsecinvalidkeyattributemask)
- [var errSecUnsupportedKeyAttributeMask: OSStatus](/documentation/security/errsecunsupportedkeyattributemask)
- [var errSecInvalidKeyLabel: OSStatus](/documentation/security/errsecinvalidkeylabel)
- [var errSecUnsupportedKeyLabel: OSStatus](/documentation/security/errsecunsupportedkeylabel)
- [var errSecInvalidKeyFormat: OSStatus](/documentation/security/errsecinvalidkeyformat)
- [var errSecInvalidKeyBlob: OSStatus](/documentation/security/errsecinvalidkeyblob)
- [var errSecInvalidKeyHierarchy: OSStatus](/documentation/security/errsecinvalidkeyhierarchy)
- [var errSecInvalidKeyRef: OSStatus](/documentation/security/errsecinvalidkeyref)
- [var errSecInvalidKeyUsageForPolicy: OSStatus](/documentation/security/errsecinvalidkeyusageforpolicy)

### Invalid Attribute Result Codes

- [var errSecInvalidAttributeKey: OSStatus](/documentation/security/errsecinvalidattributekey)
- [var errSecInvalidAttributeInitVector: OSStatus](/documentation/security/errsecinvalidattributeinitvector)
- [var errSecInvalidAttributeSalt: OSStatus](/documentation/security/errsecinvalidattributesalt)
- [var errSecInvalidAttributePadding: OSStatus](/documentation/security/errsecinvalidattributepadding)
- [var errSecInvalidAttributeRandom: OSStatus](/documentation/security/errsecinvalidattributerandom)
- [var errSecInvalidAttributeSeed: OSStatus](/documentation/security/errsecinvalidattributeseed)
- [var errSecInvalidAttributePassphrase: OSStatus](/documentation/security/errsecinvalidattributepassphrase)
- [var errSecInvalidAttributeKeyLength: OSStatus](/documentation/security/errsecinvalidattributekeylength)
- [var errSecInvalidAttributeBlockSize: OSStatus](/documentation/security/errsecinvalidattributeblocksize)
- [var errSecInvalidAttributeOutputSize: OSStatus](/documentation/security/errsecinvalidattributeoutputsize)
- [var errSecInvalidAttributeRounds: OSStatus](/documentation/security/errsecinvalidattributerounds)
- [var errSecInvalidAlgorithmParms: OSStatus](/documentation/security/errsecinvalidalgorithmparms)
- [var errSecInvalidAttributeLabel: OSStatus](/documentation/security/errsecinvalidattributelabel)
- [var errSecInvalidAttributeKeyType: OSStatus](/documentation/security/errsecinvalidattributekeytype)
- [var errSecInvalidAttributeMode: OSStatus](/documentation/security/errsecinvalidattributemode)
- [var errSecInvalidAttributeEffectiveBits: OSStatus](/documentation/security/errsecinvalidattributeeffectivebits)
- [var errSecInvalidAttributeStartDate: OSStatus](/documentation/security/errsecinvalidattributestartdate)
- [var errSecInvalidAttributeEndDate: OSStatus](/documentation/security/errsecinvalidattributeenddate)
- [var errSecInvalidAttributeVersion: OSStatus](/documentation/security/errsecinvalidattributeversion)
- [var errSecInvalidAttributePrime: OSStatus](/documentation/security/errsecinvalidattributeprime)
- [var errSecInvalidAttributeBase: OSStatus](/documentation/security/errsecinvalidattributebase)
- [var errSecInvalidAttributeSubprime: OSStatus](/documentation/security/errsecinvalidattributesubprime)
- [var errSecInvalidAttributeIterationCount: OSStatus](/documentation/security/errsecinvalidattributeiterationcount)
- [var errSecInvalidAttributeDLDBHandle: OSStatus](/documentation/security/errsecinvalidattributedldbhandle)
- [var errSecInvalidAttributeAccessCredentials: OSStatus](/documentation/security/errsecinvalidattributeaccesscredentials)
- [var errSecInvalidAttributePublicKeyFormat: OSStatus](/documentation/security/errsecinvalidattributepublickeyformat)
- [var errSecInvalidAttributePrivateKeyFormat: OSStatus](/documentation/security/errsecinvalidattributeprivatekeyformat)
- [var errSecInvalidAttributeSymmetricKeyFormat: OSStatus](/documentation/security/errsecinvalidattributesymmetrickeyformat)
- [var errSecInvalidAttributeWrappedKeyFormat: OSStatus](/documentation/security/errsecinvalidattributewrappedkeyformat)

### Missing Attribute Result Codes

- [var errSecMissingAttributeKey: OSStatus](/documentation/security/errsecmissingattributekey)
- [var errSecMissingAttributeInitVector: OSStatus](/documentation/security/errsecmissingattributeinitvector)
- [var errSecMissingAttributeSalt: OSStatus](/documentation/security/errsecmissingattributesalt)
- [var errSecMissingAttributePadding: OSStatus](/documentation/security/errsecmissingattributepadding)
- [var errSecMissingAttributeRandom: OSStatus](/documentation/security/errsecmissingattributerandom)
- [var errSecMissingAttributeSeed: OSStatus](/documentation/security/errsecmissingattributeseed)
- [var errSecMissingAttributePassphrase: OSStatus](/documentation/security/errsecmissingattributepassphrase)
- [var errSecMissingAttributeKeyLength: OSStatus](/documentation/security/errsecmissingattributekeylength)
- [var errSecMissingAttributeBlockSize: OSStatus](/documentation/security/errsecmissingattributeblocksize)
- [var errSecMissingAttributeOutputSize: OSStatus](/documentation/security/errsecmissingattributeoutputsize)
- [var errSecMissingAttributeRounds: OSStatus](/documentation/security/errsecmissingattributerounds)
- [var errSecMissingAlgorithmParms: OSStatus](/documentation/security/errsecmissingalgorithmparms)
- [var errSecMissingAttributeLabel: OSStatus](/documentation/security/errsecmissingattributelabel)
- [var errSecMissingAttributeKeyType: OSStatus](/documentation/security/errsecmissingattributekeytype)
- [var errSecMissingAttributeMode: OSStatus](/documentation/security/errsecmissingattributemode)
- [var errSecMissingAttributeEffectiveBits: OSStatus](/documentation/security/errsecmissingattributeeffectivebits)
- [var errSecMissingAttributeStartDate: OSStatus](/documentation/security/errsecmissingattributestartdate)
- [var errSecMissingAttributeEndDate: OSStatus](/documentation/security/errsecmissingattributeenddate)
- [var errSecMissingAttributeVersion: OSStatus](/documentation/security/errsecmissingattributeversion)
- [var errSecMissingAttributePrime: OSStatus](/documentation/security/errsecmissingattributeprime)
- [var errSecMissingAttributeBase: OSStatus](/documentation/security/errsecmissingattributebase)
- [var errSecMissingAttributeSubprime: OSStatus](/documentation/security/errsecmissingattributesubprime)
- [var errSecMissingAttributeIterationCount: OSStatus](/documentation/security/errsecmissingattributeiterationcount)
- [var errSecMissingAttributeDLDBHandle: OSStatus](/documentation/security/errsecmissingattributedldbhandle)
- [var errSecMissingAttributeAccessCredentials: OSStatus](/documentation/security/errsecmissingattributeaccesscredentials)
- [var errSecMissingAttributePublicKeyFormat: OSStatus](/documentation/security/errsecmissingattributepublickeyformat)
- [var errSecMissingAttributePrivateKeyFormat: OSStatus](/documentation/security/errsecmissingattributeprivatekeyformat)
- [var errSecMissingAttributeSymmetricKeyFormat: OSStatus](/documentation/security/errsecmissingattributesymmetrickeyformat)
- [var errSecMissingAttributeWrappedKeyFormat: OSStatus](/documentation/security/errsecmissingattributewrappedkeyformat)

### Timestamp Result Codes

- [var errSecTimestampMissing: OSStatus](/documentation/security/errsectimestampmissing)
- [var errSecTimestampInvalid: OSStatus](/documentation/security/errsectimestampinvalid)
- [var errSecTimestampNotTrusted: OSStatus](/documentation/security/errsectimestampnottrusted)
- [var errSecTimestampServiceNotAvailable: OSStatus](/documentation/security/errsectimestampservicenotavailable)
- [var errSecTimestampBadAlg: OSStatus](/documentation/security/errsectimestampbadalg)
- [var errSecTimestampBadRequest: OSStatus](/documentation/security/errsectimestampbadrequest)
- [var errSecTimestampBadDataFormat: OSStatus](/documentation/security/errsectimestampbaddataformat)
- [var errSecTimestampTimeNotAvailable: OSStatus](/documentation/security/errsectimestamptimenotavailable)
- [var errSecTimestampUnacceptedPolicy: OSStatus](/documentation/security/errsectimestampunacceptedpolicy)
- [var errSecTimestampUnacceptedExtension: OSStatus](/documentation/security/errsectimestampunacceptedextension)
- [var errSecTimestampAddInfoNotAvailable: OSStatus](/documentation/security/errsectimestampaddinfonotavailable)
- [var errSecTimestampSystemFailure: OSStatus](/documentation/security/errsectimestampsystemfailure)
- [var errSecSigningTimeMissing: OSStatus](/documentation/security/errsecsigningtimemissing)
- [var errSecTimestampRejection: OSStatus](/documentation/security/errsectimestamprejection)
- [var errSecTimestampWaiting: OSStatus](/documentation/security/errsectimestampwaiting)
- [var errSecTimestampRevocationWarning: OSStatus](/documentation/security/errsectimestamprevocationwarning)
- [var errSecTimestampRevocationNotification: OSStatus](/documentation/security/errsectimestamprevocationnotification)

### Invalid parameter result codes

- [var errSecInvalidAction: OSStatus](/documentation/security/errsecinvalidaction)
- [var errSecInvalidAddinFunctionTable: OSStatus](/documentation/security/errsecinvalidaddinfunctiontable)
- [var errSecInvalidAlgorithm: OSStatus](/documentation/security/errsecinvalidalgorithm)
- [var errSecInvalidAuthority: OSStatus](/documentation/security/errsecinvalidauthority)
- [var errSecInvalidAuthorityKeyID: OSStatus](/documentation/security/errsecinvalidauthoritykeyid)
- [var errSecInvalidBundleInfo: OSStatus](/documentation/security/errsecinvalidbundleinfo)
- [var errSecInvalidContext: OSStatus](/documentation/security/errsecinvalidcontext)
- [var errSecInvalidDBList: OSStatus](/documentation/security/errsecinvaliddblist)
- [var errSecInvalidDBLocation: OSStatus](/documentation/security/errsecinvaliddblocation)
- [var errSecInvalidData: OSStatus](/documentation/security/errsecinvaliddata)
- [var errSecInvalidDatabaseBlob: OSStatus](/documentation/security/errsecinvaliddatabaseblob)
- [var errSecInvalidDigestAlgorithm: OSStatus](/documentation/security/errsecinvaliddigestalgorithm)
- [var errSecInvalidEncoding: OSStatus](/documentation/security/errsecinvalidencoding)
- [var errSecInvalidExtendedKeyUsage: OSStatus](/documentation/security/errsecinvalidextendedkeyusage)
- [var errSecInvalidFormType: OSStatus](/documentation/security/errsecinvalidformtype)
- [var errSecInvalidGUID: OSStatus](/documentation/security/errsecinvalidguid)
- [var errSecInvalidHandle: OSStatus](/documentation/security/errsecinvalidhandle)
- [var errSecInvalidHandleUsage: OSStatus](/documentation/security/errsecinvalidhandleusage)
- [var errSecInvalidID: OSStatus](/documentation/security/errsecinvalidid)
- [var errSecInvalidIDLinkage: OSStatus](/documentation/security/errsecinvalididlinkage)
- [var errSecInvalidIdentifier: OSStatus](/documentation/security/errsecinvalididentifier)
- [var errSecInvalidIndex: OSStatus](/documentation/security/errsecinvalidindex)
- [var errSecInvalidIndexInfo: OSStatus](/documentation/security/errsecinvalidindexinfo)
- [var errSecInvalidInputVector: OSStatus](/documentation/security/errsecinvalidinputvector)
- [var errSecInvalidLoginName: OSStatus](/documentation/security/errsecinvalidloginname)
- [var errSecInvalidModifyMode: OSStatus](/documentation/security/errsecinvalidmodifymode)
- [var errSecInvalidName: OSStatus](/documentation/security/errsecinvalidname)
- [var errSecInvalidNetworkAddress: OSStatus](/documentation/security/errsecinvalidnetworkaddress)
- [var errSecInvalidNewOwner: OSStatus](/documentation/security/errsecinvalidnewowner)
- [var errSecInvalidNumberOfFields: OSStatus](/documentation/security/errsecinvalidnumberoffields)
- [var errSecInvalidOutputVector: OSStatus](/documentation/security/errsecinvalidoutputvector)
- [var errSecInvalidOwnerEdit: OSStatus](/documentation/security/errsecinvalidowneredit)
- [var errSecInvalidPVC: OSStatus](/documentation/security/errsecinvalidpvc)
- [var errSecInvalidParsingModule: OSStatus](/documentation/security/errsecinvalidparsingmodule)
- [var errSecInvalidPassthroughID: OSStatus](/documentation/security/errsecinvalidpassthroughid)
- [var errSecInvalidPasswordRef: OSStatus](/documentation/security/errsecinvalidpasswordref)
- [var errSecInvalidPointer: OSStatus](/documentation/security/errsecinvalidpointer)
- [var errSecInvalidPolicyIdentifiers: OSStatus](/documentation/security/errsecinvalidpolicyidentifiers)
- [var errSecInvalidQuery: OSStatus](/documentation/security/errsecinvalidquery)
- [var errSecInvalidReason: OSStatus](/documentation/security/errsecinvalidreason)
- [var errSecInvalidRecord: OSStatus](/documentation/security/errsecinvalidrecord)
- [var errSecInvalidRequestInputs: OSStatus](/documentation/security/errsecinvalidrequestinputs)
- [var errSecInvalidRequestor: OSStatus](/documentation/security/errsecinvalidrequestor)
- [var errSecInvalidResponseVector: OSStatus](/documentation/security/errsecinvalidresponsevector)
- [var errSecInvalidRoot: OSStatus](/documentation/security/errsecinvalidroot)
- [var errSecInvalidSampleValue: OSStatus](/documentation/security/errsecinvalidsamplevalue)
- [var errSecInvalidScope: OSStatus](/documentation/security/errsecinvalidscope)
- [var errSecInvalidServiceMask: OSStatus](/documentation/security/errsecinvalidservicemask)
- [var errSecInvalidSignature: OSStatus](/documentation/security/errsecinvalidsignature)
- [var errSecInvalidStopOnPolicy: OSStatus](/documentation/security/errsecinvalidstoponpolicy)
- [var errSecInvalidSubServiceID: OSStatus](/documentation/security/errsecinvalidsubserviceid)
- [var errSecInvalidSubjectKeyID: OSStatus](/documentation/security/errsecinvalidsubjectkeyid)
- [var errSecInvalidTimeString: OSStatus](/documentation/security/errsecinvalidtimestring)
- [var errSecInvalidTrustSetting: OSStatus](/documentation/security/errsecinvalidtrustsetting)
- [var errSecInvalidTrustSettings: OSStatus](/documentation/security/errsecinvalidtrustsettings)
- [var errSecInvalidTuple: OSStatus](/documentation/security/errsecinvalidtuple)
- [var errSecInvalidTupleCredendtials: OSStatus](/documentation/security/errsecinvalidtuplecredendtials)
- [var errSecInvalidTupleGroup: OSStatus](/documentation/security/errsecinvalidtuplegroup)
- [var errSecInvalidValidityPeriod: OSStatus](/documentation/security/errsecinvalidvalidityperiod)
- [var errSecInvalidValue: OSStatus](/documentation/security/errsecinvalidvalue)

### Unsupported input result codes

- [var errSecUnsupportedAddressType: OSStatus](/documentation/security/errsecunsupportedaddresstype)
- [var errSecUnsupportedFieldFormat: OSStatus](/documentation/security/errsecunsupportedfieldformat)
- [var errSecUnsupportedFormat: OSStatus](/documentation/security/errsecunsupportedformat)
- [var errSecUnsupportedIndexInfo: OSStatus](/documentation/security/errsecunsupportedindexinfo)
- [var errSecUnsupportedLocality: OSStatus](/documentation/security/errsecunsupportedlocality)
- [var errSecUnsupportedNumAttributes: OSStatus](/documentation/security/errsecunsupportednumattributes)
- [var errSecUnsupportedNumIndexes: OSStatus](/documentation/security/errsecunsupportednumindexes)
- [var errSecUnsupportedNumRecordTypes: OSStatus](/documentation/security/errsecunsupportednumrecordtypes)
- [var errSecUnsupportedNumSelectionPreds: OSStatus](/documentation/security/errsecunsupportednumselectionpreds)
- [var errSecUnsupportedOperator: OSStatus](/documentation/security/errsecunsupportedoperator)
- [var errSecUnsupportedQueryLimits: OSStatus](/documentation/security/errsecunsupportedquerylimits)
- [var errSecUnsupportedService: OSStatus](/documentation/security/errsecunsupportedservice)
- [var errSecUnsupportedVectorOfBuffers: OSStatus](/documentation/security/errsecunsupportedvectorofbuffers)

### Apple specific result codes

- [var errSecAppleInvalidKeyEndDate: OSStatus](/documentation/security/errsecappleinvalidkeyenddate)
- [var errSecAppleInvalidKeyStartDate: OSStatus](/documentation/security/errsecappleinvalidkeystartdate)
- [var errSecApplePublicKeyIncomplete: OSStatus](/documentation/security/errsecapplepublickeyincomplete)
- [var errSecAppleSSLv2Rollback: OSStatus](/documentation/security/errsecapplesslv2rollback)
- [var errSecAppleSignatureMismatch: OSStatus](/documentation/security/errsecapplesignaturemismatch)

### Module manager result codes

- [var errSecEMMLoadFailed: OSStatus](/documentation/security/errsecemmloadfailed)
- [var errSecEMMUnloadFailed: OSStatus](/documentation/security/errsecemmunloadfailed)
- [var errSecModuleManagerInitializeFailed: OSStatus](/documentation/security/errsecmodulemanagerinitializefailed)
- [var errSecModuleManagerNotFound: OSStatus](/documentation/security/errsecmodulemanagernotfound)
- [var errSecModuleManifestVerifyFailed: OSStatus](/documentation/security/errsecmodulemanifestverifyfailed)
- [var errSecModuleNotLoaded: OSStatus](/documentation/security/errsecmodulenotloaded)

### Other Result Codes

- [var errSecAddinLoadFailed: OSStatus](/documentation/security/errsecaddinloadfailed)
- [var errSecAddinUnloadFailed: OSStatus](/documentation/security/errsecaddinunloadfailed)
- [var errSecAlgorithmMismatch: OSStatus](/documentation/security/errsecalgorithmmismatch)
- [var errSecAlreadyLoggedIn: OSStatus](/documentation/security/errsecalreadyloggedin)
- [var errSecAttachHandleBusy: OSStatus](/documentation/security/errsecattachhandlebusy)
- [var errSecAttributeNotInContext: OSStatus](/documentation/security/errsecattributenotincontext)
- [var errSecBlockSizeMismatch: OSStatus](/documentation/security/errsecblocksizemismatch)
- [var errSecCallbackFailed: OSStatus](/documentation/security/errseccallbackfailed)
- [var errSecConversionError: OSStatus](/documentation/security/errsecconversionerror)
- [var errSecDatabaseLocked: OSStatus](/documentation/security/errsecdatabaselocked)
- [var errSecDatastoreIsOpen: OSStatus](/documentation/security/errsecdatastoreisopen)
- [var errSecDecode: OSStatus](/documentation/security/errsecdecode)
- [var errSecDeviceError: OSStatus](/documentation/security/errsecdeviceerror)
- [var errSecDeviceFailed: OSStatus](/documentation/security/errsecdevicefailed)
- [var errSecDeviceReset: OSStatus](/documentation/security/errsecdevicereset)
- [var errSecDeviceVerifyFailed: OSStatus](/documentation/security/errsecdeviceverifyfailed)
- [var errSecEventNotificationCallbackNotFound: OSStatus](/documentation/security/errseceventnotificationcallbacknotfound)
- [var errSecExtendedKeyUsageNotCritical: OSStatus](/documentation/security/errsecextendedkeyusagenotcritical)
- [var errSecFieldSpecifiedMultiple: OSStatus](/documentation/security/errsecfieldspecifiedmultiple)
- [var errSecFileTooBig: OSStatus](/documentation/security/errsecfiletoobig)
- [var errSecFunctionFailed: OSStatus](/documentation/security/errsecfunctionfailed)
- [var errSecFunctionIntegrityFail: OSStatus](/documentation/security/errsecfunctionintegrityfail)
- [var errSecHostNameMismatch: OSStatus](/documentation/security/errsechostnamemismatch)
- [var errSecIncompatibleDatabaseBlob: OSStatus](/documentation/security/errsecincompatibledatabaseblob)
- [var errSecIncompatibleFieldFormat: OSStatus](/documentation/security/errsecincompatiblefieldformat)
- [var errSecIncompatibleKeyBlob: OSStatus](/documentation/security/errsecincompatiblekeyblob)
- [var errSecIncompatibleVersion: OSStatus](/documentation/security/errsecincompatibleversion)
- [var errSecInputLengthError: OSStatus](/documentation/security/errsecinputlengtherror)
- [var errSecInsufficientClientID: OSStatus](/documentation/security/errsecinsufficientclientid)
- [var errSecInsufficientCredentials: OSStatus](/documentation/security/errsecinsufficientcredentials)
- [var errSecInvalidAccessCredentials: OSStatus](/documentation/security/errsecinvalidaccesscredentials)
- [var errSecInvalidAccessRequest: OSStatus](/documentation/security/errsecinvalidaccessrequest)
- [var errSecLibraryReferenceNotFound: OSStatus](/documentation/security/errseclibraryreferencenotfound)
- [var errSecMDSError: OSStatus](/documentation/security/errsecmdserror)
- [var errSecMemoryError: OSStatus](/documentation/security/errsecmemoryerror)
- [var errSecMissingEntitlement: OSStatus](/documentation/security/errsecmissingentitlement)
- [var errSecMissingRequiredExtension: OSStatus](/documentation/security/errsecmissingrequiredextension)
- [var errSecMissingValue: OSStatus](/documentation/security/errsecmissingvalue)
- [var errSecMultiplePrivKeys: OSStatus](/documentation/security/errsecmultipleprivkeys)
- [var errSecMultipleValuesUnsupported: OSStatus](/documentation/security/errsecmultiplevaluesunsupported)
- [var errSecNoAccessForItem: OSStatus](/documentation/security/errsecnoaccessforitem)
- [var errSecNoBasicConstraints: OSStatus](/documentation/security/errsecnobasicconstraints)
- [var errSecNoBasicConstraintsCA: OSStatus](/documentation/security/errsecnobasicconstraintsca)
- [var errSecNoDefaultAuthority: OSStatus](/documentation/security/errsecnodefaultauthority)
- [var errSecNoFieldValues: OSStatus](/documentation/security/errsecnofieldvalues)
- [var errSecNoTrustSettings: OSStatus](/documentation/security/errsecnotrustsettings)
- [var errSecNotInitialized: OSStatus](/documentation/security/errsecnotinitialized)
- [var errSecNotLoggedIn: OSStatus](/documentation/security/errsecnotloggedin)
- [var errSecNotSigner: OSStatus](/documentation/security/errsecnotsigner)
- [var errSecNotTrusted: OSStatus](/documentation/security/errsecnottrusted)
- [var errSecOutputLengthError: OSStatus](/documentation/security/errsecoutputlengtherror)
- [var errSecPVCAlreadyConfigured: OSStatus](/documentation/security/errsecpvcalreadyconfigured)
- [var errSecPVCReferentNotFound: OSStatus](/documentation/security/errsecpvcreferentnotfound)
- [var errSecPassphraseRequired: OSStatus](/documentation/security/errsecpassphraserequired)
- [var errSecPathLengthConstraintExceeded: OSStatus](/documentation/security/errsecpathlengthconstraintexceeded)
- [var errSecPkcs12VerifyFailure: OSStatus](/documentation/security/errsecpkcs12verifyfailure)
- [var errSecPolicyNotFound: OSStatus](/documentation/security/errsecpolicynotfound)
- [var errSecPrivilegeNotGranted: OSStatus](/documentation/security/errsecprivilegenotgranted)
- [var errSecPrivilegeNotSupported: OSStatus](/documentation/security/errsecprivilegenotsupported)
- [var errSecPublicKeyInconsistent: OSStatus](/documentation/security/errsecpublickeyinconsistent)
- [var errSecQuerySizeUnknown: OSStatus](/documentation/security/errsecquerysizeunknown)
- [var errSecQuotaExceeded: OSStatus](/documentation/security/errsecquotaexceeded)
- [var errSecRejectedForm: OSStatus](/documentation/security/errsecrejectedform)
- [var errSecRequestDescriptor: OSStatus](/documentation/security/errsecrequestdescriptor)
- [var errSecRequestLost: OSStatus](/documentation/security/errsecrequestlost)
- [var errSecRequestRejected: OSStatus](/documentation/security/errsecrequestrejected)
- [var errSecSelfCheckFailed: OSStatus](/documentation/security/errsecselfcheckfailed)
- [var errSecServiceNotAvailable: OSStatus](/documentation/security/errsecservicenotavailable)
- [var errSecStagedOperationInProgress: OSStatus](/documentation/security/errsecstagedoperationinprogress)
- [var errSecStagedOperationNotStarted: OSStatus](/documentation/security/errsecstagedoperationnotstarted)
- [var errSecTagNotFound: OSStatus](/documentation/security/errsectagnotfound)
- [var errSecTrustNotAvailable: OSStatus](/documentation/security/errsectrustnotavailable)
- [var errSecUnknownFormat: OSStatus](/documentation/security/errsecunknownformat)
- [var errSecUnknownTag: OSStatus](/documentation/security/errsecunknowntag)
- [var errSecVerificationFailure: OSStatus](/documentation/security/errsecverificationfailure)
- [var errSecVerifyActionFailed: OSStatus](/documentation/security/errsecverifyactionfailed)
- [var errSecVerifyFailed: OSStatus](/documentation/security/errsecverifyfailed)

## Legacy interfaces

- [Common Security Services Manager](/documentation/security/common-security-services-manager)

### Data Types

- [cssm_applecspdl_db_change_password_parameters](/documentation/security/cssm_applecspdl_db_change_password_parameters-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_applecspdl_db_change_password_parameters-swift.struct/init())
- [init(accessCredentials: UnsafeMutablePointer<cssm_access_credentials>!)](/documentation/security/cssm_applecspdl_db_change_password_parameters-swift.struct/init(accesscredentials:))

#### Instance Properties

- [var accessCredentials: UnsafeMutablePointer<cssm_access_credentials>!](/documentation/security/cssm_applecspdl_db_change_password_parameters-swift.struct/accesscredentials)
- [cssm_applecspdl_db_is_locked_parameters](/documentation/security/cssm_applecspdl_db_is_locked_parameters-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_applecspdl_db_is_locked_parameters-swift.struct/init())
- [init(isLocked: uint8)](/documentation/security/cssm_applecspdl_db_is_locked_parameters-swift.struct/init(islocked:))

#### Instance Properties

- [var isLocked: uint8](/documentation/security/cssm_applecspdl_db_is_locked_parameters-swift.struct/islocked)
- [cssm_applecspdl_db_settings_parameters](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.struct/init())
- [init(idleTimeout: uint32, lockOnSleep: uint8)](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.struct/init(idletimeout:lockonsleep:))

#### Instance Properties

- [var idleTimeout: uint32](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.struct/idletimeout)
- [var lockOnSleep: uint8](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.struct/lockonsleep)
- [cssm_appledl_open_parameters](/documentation/security/cssm_appledl_open_parameters-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_appledl_open_parameters-swift.struct/init())
- [init(length: uint32, version: uint32, autoCommit: CSSM_BOOL, mask: uint32, mode: mode_t)](/documentation/security/cssm_appledl_open_parameters-swift.struct/init(length:version:autocommit:mask:mode:))

#### Instance Properties

- [var autoCommit: CSSM_BOOL](/documentation/security/cssm_appledl_open_parameters-swift.struct/autocommit)
- [var length: uint32](/documentation/security/cssm_appledl_open_parameters-swift.struct/length)
- [var mask: uint32](/documentation/security/cssm_appledl_open_parameters-swift.struct/mask)
- [var mode: mode_t](/documentation/security/cssm_appledl_open_parameters-swift.struct/mode)
- [var version: uint32](/documentation/security/cssm_appledl_open_parameters-swift.struct/version)
- [cssm_authorizationgroup](/documentation/security/cssm_authorizationgroup-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_authorizationgroup-swift.struct/init())
- [init(NumberOfAuthTags: uint32, AuthTags: UnsafeMutablePointer<CSSM_ACL_AUTHORIZATION_TAG>!)](/documentation/security/cssm_authorizationgroup-swift.struct/init(numberofauthtags:authtags:))

#### Instance Properties

- [var AuthTags: UnsafeMutablePointer<CSSM_ACL_AUTHORIZATION_TAG>!](/documentation/security/cssm_authorizationgroup-swift.struct/authtags)
- [var NumberOfAuthTags: uint32](/documentation/security/cssm_authorizationgroup-swift.struct/numberofauthtags)
- [cssm_csp_operational_statistics](/documentation/security/cssm_csp_operational_statistics-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_csp_operational_statistics-swift.struct/init())
- [init(UserAuthenticated: CSSM_BOOL, DeviceFlags: CSSM_CSP_FLAGS, TokenMaxSessionCount: uint32, TokenOpenedSessionCount: uint32, TokenMaxRWSessionCount: uint32, TokenOpenedRWSessionCount: uint32, TokenTotalPublicMem: uint32, TokenFreePublicMem: uint32, TokenTotalPrivateMem: uint32, TokenFreePrivateMem: uint32)](/documentation/security/cssm_csp_operational_statistics-swift.struct/init(userauthenticated:deviceflags:tokenmaxsessioncount:tokenopenedsessioncount:tokenmaxrwsessioncount:tokenopenedrwsessioncount:tokentotalpublicmem:tokenfreepublicmem:tokentotalprivatemem:tokenfreeprivatemem:))

#### Instance Properties

- [var DeviceFlags: CSSM_CSP_FLAGS](/documentation/security/cssm_csp_operational_statistics-swift.struct/deviceflags)
- [var TokenFreePrivateMem: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenfreeprivatemem)
- [var TokenFreePublicMem: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenfreepublicmem)
- [var TokenMaxRWSessionCount: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenmaxrwsessioncount)
- [var TokenMaxSessionCount: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenmaxsessioncount)
- [var TokenOpenedRWSessionCount: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenopenedrwsessioncount)
- [var TokenOpenedSessionCount: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokenopenedsessioncount)
- [var TokenTotalPrivateMem: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokentotalprivatemem)
- [var TokenTotalPublicMem: uint32](/documentation/security/cssm_csp_operational_statistics-swift.struct/tokentotalpublicmem)
- [var UserAuthenticated: CSSM_BOOL](/documentation/security/cssm_csp_operational_statistics-swift.struct/userauthenticated)
- [cssm_data](/documentation/security/cssm_data-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_data-swift.struct/init())
- [init(Length: Int, Data: UnsafeMutablePointer<UInt8>?)](/documentation/security/cssm_data-swift.struct/init(length:data:))

#### Instance Properties

- [var Data: UnsafeMutablePointer<UInt8>?](/documentation/security/cssm_data-swift.struct/data)
- [var Length: Int](/documentation/security/cssm_data-swift.struct/length)
- [cssm_date](/documentation/security/cssm_date-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_date-swift.struct/init())
- [init(Year: (uint8, uint8, uint8, uint8), Month: (uint8, uint8), Day: (uint8, uint8))](/documentation/security/cssm_date-swift.struct/init(year:month:day:))

#### Instance Properties

- [var Day: (uint8, uint8)](/documentation/security/cssm_date-swift.struct/day)
- [var Month: (uint8, uint8)](/documentation/security/cssm_date-swift.struct/month)
- [var Year: (uint8, uint8, uint8, uint8)](/documentation/security/cssm_date-swift.struct/year)
- [cssm_db_schema_index_info](/documentation/security/cssm_db_schema_index_info-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_db_schema_index_info-swift.struct/init())
- [init(AttributeId: uint32, IndexId: uint32, IndexType: CSSM_DB_INDEX_TYPE, IndexedDataLocation: CSSM_DB_INDEXED_DATA_LOCATION)](/documentation/security/cssm_db_schema_index_info-swift.struct/init(attributeid:indexid:indextype:indexeddatalocation:))

#### Instance Properties

- [var AttributeId: uint32](/documentation/security/cssm_db_schema_index_info-swift.struct/attributeid)
- [var IndexId: uint32](/documentation/security/cssm_db_schema_index_info-swift.struct/indexid)
- [var IndexType: CSSM_DB_INDEX_TYPE](/documentation/security/cssm_db_schema_index_info-swift.struct/indextype)
- [var IndexedDataLocation: CSSM_DB_INDEXED_DATA_LOCATION](/documentation/security/cssm_db_schema_index_info-swift.struct/indexeddatalocation)
- [cssm_dl_db_handle](/documentation/security/cssm_dl_db_handle-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_dl_db_handle-swift.struct/init())
- [init(DLHandle: CSSM_DL_HANDLE, DBHandle: CSSM_DB_HANDLE)](/documentation/security/cssm_dl_db_handle-swift.struct/init(dlhandle:dbhandle:))

#### Instance Properties

- [var DBHandle: CSSM_DB_HANDLE](/documentation/security/cssm_dl_db_handle-swift.struct/dbhandle)
- [var DLHandle: CSSM_DL_HANDLE](/documentation/security/cssm_dl_db_handle-swift.struct/dlhandle)
- [cssm_dl_pkcs11_attributes](/documentation/security/cssm_dl_pkcs11_attributes)

#### Initializers

- [init()](/documentation/security/cssm_dl_pkcs11_attributes/init())
- [init(DeviceAccessFlags: uint32)](/documentation/security/cssm_dl_pkcs11_attributes/init(deviceaccessflags:))

#### Instance Properties

- [var DeviceAccessFlags: uint32](/documentation/security/cssm_dl_pkcs11_attributes/deviceaccessflags)
- [cssm_func_name_addr](/documentation/security/cssm_func_name_addr-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_func_name_addr-swift.struct/init())
- [init(Name: CSSM_STRING, Address: CSSM_PROC_ADDR!)](/documentation/security/cssm_func_name_addr-swift.struct/init(name:address:))

#### Instance Properties

- [var Address: CSSM_PROC_ADDR!](/documentation/security/cssm_func_name_addr-swift.struct/address)
- [var Name: CSSM_STRING](/documentation/security/cssm_func_name_addr-swift.struct/name)
- [cssm_guid](/documentation/security/cssm_guid-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_guid-swift.struct/init())
- [init(Data1: uint32, Data2: uint16, Data3: uint16, Data4: (uint8, uint8, uint8, uint8, uint8, uint8, uint8, uint8))](/documentation/security/cssm_guid-swift.struct/init(data1:data2:data3:data4:))

#### Instance Properties

- [var Data1: uint32](/documentation/security/cssm_guid-swift.struct/data1)
- [var Data2: uint16](/documentation/security/cssm_guid-swift.struct/data2)
- [var Data3: uint16](/documentation/security/cssm_guid-swift.struct/data3)
- [var Data4: (uint8, uint8, uint8, uint8, uint8, uint8, uint8, uint8)](/documentation/security/cssm_guid-swift.struct/data4)
- [cssm_key_size](/documentation/security/cssm_key_size-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_key_size-swift.struct/init())
- [init(LogicalKeySizeInBits: uint32, EffectiveKeySizeInBits: uint32)](/documentation/security/cssm_key_size-swift.struct/init(logicalkeysizeinbits:effectivekeysizeinbits:))

#### Instance Properties

- [var EffectiveKeySizeInBits: uint32](/documentation/security/cssm_key_size-swift.struct/effectivekeysizeinbits)
- [var LogicalKeySizeInBits: uint32](/documentation/security/cssm_key_size-swift.struct/logicalkeysizeinbits)
- [cssm_kr_name](/documentation/security/cssm_kr_name-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_kr_name-swift.struct/init())
- [init(Type: uint8, Length: uint8, Name: UnsafeMutablePointer<CChar>!)](/documentation/security/cssm_kr_name-swift.struct/init(type:length:name:))

#### Instance Properties

- [var Length: uint8](/documentation/security/cssm_kr_name-swift.struct/length)
- [var Name: UnsafeMutablePointer<CChar>!](/documentation/security/cssm_kr_name-swift.struct/name)
- [var `Type`: uint8](/documentation/security/cssm_kr_name-swift.struct/type)
- [cssm_list](/documentation/security/cssm_list-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_list-swift.struct/init())
- [init(ListType: CSSM_LIST_TYPE, Head: CSSM_LIST_ELEMENT_PTR!, Tail: CSSM_LIST_ELEMENT_PTR!)](/documentation/security/cssm_list-swift.struct/init(listtype:head:tail:))

#### Instance Properties

- [var Head: CSSM_LIST_ELEMENT_PTR!](/documentation/security/cssm_list-swift.struct/head)
- [var ListType: CSSM_LIST_TYPE](/documentation/security/cssm_list-swift.struct/listtype)
- [var Tail: CSSM_LIST_ELEMENT_PTR!](/documentation/security/cssm_list-swift.struct/tail)
- [cssm_memory_funcs](/documentation/security/cssm_memory_funcs-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_memory_funcs-swift.struct/init())
- [init(malloc_func: CSSM_MALLOC!, free_func: CSSM_FREE!, realloc_func: CSSM_REALLOC!, calloc_func: CSSM_CALLOC!, AllocRef: UnsafeMutableRawPointer!)](/documentation/security/cssm_memory_funcs-swift.struct/init(malloc_func:free_func:realloc_func:calloc_func:allocref:))

#### Instance Properties

- [var AllocRef: UnsafeMutableRawPointer!](/documentation/security/cssm_memory_funcs-swift.struct/allocref)
- [var calloc_func: CSSM_CALLOC!](/documentation/security/cssm_memory_funcs-swift.struct/calloc_func)
- [var free_func: CSSM_FREE!](/documentation/security/cssm_memory_funcs-swift.struct/free_func)
- [var malloc_func: CSSM_MALLOC!](/documentation/security/cssm_memory_funcs-swift.struct/malloc_func)
- [var realloc_func: CSSM_REALLOC!](/documentation/security/cssm_memory_funcs-swift.struct/realloc_func)
- [cssm_name_list](/documentation/security/cssm_name_list-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_name_list-swift.struct/init())
- [init(NumStrings: uint32, String: UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>!)](/documentation/security/cssm_name_list-swift.struct/init(numstrings:string:))

#### Instance Properties

- [var NumStrings: uint32](/documentation/security/cssm_name_list-swift.struct/numstrings)
- [var String: UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>!](/documentation/security/cssm_name_list-swift.struct/string)
- [cssm_parsed_cert](/documentation/security/cssm_parsed_cert-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_parsed_cert-swift.struct/init())
- [init(CertType: CSSM_CERT_TYPE, ParsedCertFormat: CSSM_CERT_PARSE_FORMAT, ParsedCert: UnsafeMutableRawPointer!)](/documentation/security/cssm_parsed_cert-swift.struct/init(certtype:parsedcertformat:parsedcert:))

#### Instance Properties

- [var CertType: CSSM_CERT_TYPE](/documentation/security/cssm_parsed_cert-swift.struct/certtype)
- [var ParsedCert: UnsafeMutableRawPointer!](/documentation/security/cssm_parsed_cert-swift.struct/parsedcert)
- [var ParsedCertFormat: CSSM_CERT_PARSE_FORMAT](/documentation/security/cssm_parsed_cert-swift.struct/parsedcertformat)
- [cssm_parsed_crl](/documentation/security/cssm_parsed_crl-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_parsed_crl-swift.struct/init())
- [init(CrlType: CSSM_CRL_TYPE, ParsedCrlFormat: CSSM_CRL_PARSE_FORMAT, ParsedCrl: UnsafeMutableRawPointer!)](/documentation/security/cssm_parsed_crl-swift.struct/init(crltype:parsedcrlformat:parsedcrl:))

#### Instance Properties

- [var CrlType: CSSM_CRL_TYPE](/documentation/security/cssm_parsed_crl-swift.struct/crltype)
- [var ParsedCrl: UnsafeMutableRawPointer!](/documentation/security/cssm_parsed_crl-swift.struct/parsedcrl)
- [var ParsedCrlFormat: CSSM_CRL_PARSE_FORMAT](/documentation/security/cssm_parsed_crl-swift.struct/parsedcrlformat)
- [cssm_query_size_data](/documentation/security/cssm_query_size_data-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_query_size_data-swift.struct/init())
- [init(SizeInputBlock: uint32, SizeOutputBlock: uint32)](/documentation/security/cssm_query_size_data-swift.struct/init(sizeinputblock:sizeoutputblock:))

#### Instance Properties

- [var SizeInputBlock: uint32](/documentation/security/cssm_query_size_data-swift.struct/sizeinputblock)
- [var SizeOutputBlock: uint32](/documentation/security/cssm_query_size_data-swift.struct/sizeoutputblock)
- [cssm_range](/documentation/security/cssm_range-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_range-swift.struct/init())
- [init(Min: uint32, Max: uint32)](/documentation/security/cssm_range-swift.struct/init(min:max:))

#### Instance Properties

- [var Max: uint32](/documentation/security/cssm_range-swift.struct/max)
- [var Min: uint32](/documentation/security/cssm_range-swift.struct/min)
- [cssm_tp_result_set](/documentation/security/cssm_tp_result_set-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_tp_result_set-swift.struct/init())
- [init(NumberOfResults: uint32, Results: UnsafeMutableRawPointer!)](/documentation/security/cssm_tp_result_set-swift.struct/init(numberofresults:results:))

#### Instance Properties

- [var NumberOfResults: uint32](/documentation/security/cssm_tp_result_set-swift.struct/numberofresults)
- [var Results: UnsafeMutableRawPointer!](/documentation/security/cssm_tp_result_set-swift.struct/results)
- [cssm_version](/documentation/security/cssm_version-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_version-swift.struct/init())
- [init(Major: uint32, Minor: uint32)](/documentation/security/cssm_version-swift.struct/init(major:minor:))

#### Instance Properties

- [var Major: uint32](/documentation/security/cssm_version-swift.struct/major)
- [var Minor: uint32](/documentation/security/cssm_version-swift.struct/minor)

### Constants

- [var SEC_OS_IPHONE: Int32](/documentation/security/sec_os_iphone)
- [var SEC_OS_OSX: Int32](/documentation/security/sec_os_osx)
- [var SEC_OS_OSX_INCLUDES: Bool](/documentation/security/sec_os_osx_includes)
- [var SECURITY_TYPE_UNIFICATION: Int32](/documentation/security/security_type_unification)
- [var CSSM_APPLE_ACL_TAG_INTEGRITY: String](/documentation/security/cssm_apple_acl_tag_integrity)
- [var CSSM_APPLE_ACL_TAG_PARTITION_ID: String](/documentation/security/cssm_apple_acl_tag_partition_id)
- [let kCMSEncoderDigestAlgorithmSHA1: CFString](/documentation/security/kcmsencoderdigestalgorithmsha1)
- [let kCMSEncoderDigestAlgorithmSHA256: CFString](/documentation/security/kcmsencoderdigestalgorithmsha256)
- [var BER_TAG_BOOLEAN: Int32](/documentation/security/ber_tag_boolean)
- [var BER_TAG_EXTERNAL: Int32](/documentation/security/ber_tag_external)
- [var CSSMERR_AC_DEVICE_FAILED: Int](/documentation/security/cssmerr_ac_device_failed)
- [var CSSMERR_AC_DEVICE_RESET: Int](/documentation/security/cssmerr_ac_device_reset)
- [var CSSMERR_AC_FUNCTION_FAILED: Int](/documentation/security/cssmerr_ac_function_failed)
- [var CSSMERR_AC_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_ac_function_not_implemented)
- [var CSSMERR_AC_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_ac_insufficient_client_identification)
- [var CSSMERR_AC_INTERNAL_ERROR: Int](/documentation/security/cssmerr_ac_internal_error)
- [var CSSMERR_AC_INVALID_BASE_ACLS: Int](/documentation/security/cssmerr_ac_invalid_base_acls)
- [var CSSMERR_AC_INVALID_CL_HANDLE: Int](/documentation/security/cssmerr_ac_invalid_cl_handle)
- [var CSSMERR_AC_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssmerr_ac_invalid_context_handle)
- [var CSSMERR_AC_INVALID_DATA: Int](/documentation/security/cssmerr_ac_invalid_data)
- [var CSSMERR_AC_INVALID_DB_HANDLE: Int](/documentation/security/cssmerr_ac_invalid_db_handle)
- [var CSSMERR_AC_INVALID_DB_LIST: Int](/documentation/security/cssmerr_ac_invalid_db_list)
- [var CSSMERR_AC_INVALID_DB_LIST_POINTER: Int](/documentation/security/cssmerr_ac_invalid_db_list_pointer)
- [var CSSMERR_AC_INVALID_DL_HANDLE: Int](/documentation/security/cssmerr_ac_invalid_dl_handle)
- [var CSSMERR_AC_INVALID_ENCODING: Int](/documentation/security/cssmerr_ac_invalid_encoding)
- [var CSSMERR_AC_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_ac_invalid_input_pointer)
- [var CSSMERR_AC_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_ac_invalid_output_pointer)
- [var CSSMERR_AC_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssmerr_ac_invalid_passthrough_id)
- [var CSSMERR_AC_INVALID_POINTER: Int](/documentation/security/cssmerr_ac_invalid_pointer)
- [var CSSMERR_AC_INVALID_REQUESTOR: Int](/documentation/security/cssmerr_ac_invalid_requestor)
- [var CSSMERR_AC_INVALID_REQUEST_DESCRIPTOR: Int](/documentation/security/cssmerr_ac_invalid_request_descriptor)
- [var CSSMERR_AC_INVALID_TP_HANDLE: Int](/documentation/security/cssmerr_ac_invalid_tp_handle)
- [var CSSMERR_AC_INVALID_TUPLE_CREDENTIALS: Int](/documentation/security/cssmerr_ac_invalid_tuple_credentials)
- [var CSSMERR_AC_INVALID_VALIDITY_PERIOD: Int](/documentation/security/cssmerr_ac_invalid_validity_period)
- [var CSSMERR_AC_IN_DARK_WAKE: Int](/documentation/security/cssmerr_ac_in_dark_wake)
- [var CSSMERR_AC_MDS_ERROR: Int](/documentation/security/cssmerr_ac_mds_error)
- [var CSSMERR_AC_MEMORY_ERROR: Int](/documentation/security/cssmerr_ac_memory_error)
- [var CSSMERR_AC_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_ac_no_user_interaction)
- [var CSSMERR_AC_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_ac_os_access_denied)
- [var CSSMERR_AC_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_ac_self_check_failed)
- [var CSSMERR_AC_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_ac_service_not_available)
- [var CSSMERR_AC_USER_CANCELED: Int](/documentation/security/cssmerr_ac_user_canceled)
- [var CSSMERR_APPLEDL_DISK_FULL: Int](/documentation/security/cssmerr_appledl_disk_full)
- [var CSSMERR_APPLEDL_FILE_TOO_BIG: Int](/documentation/security/cssmerr_appledl_file_too_big)
- [var CSSMERR_APPLEDL_INCOMPATIBLE_DATABASE_BLOB: Int](/documentation/security/cssmerr_appledl_incompatible_database_blob)
- [var CSSMERR_APPLEDL_INCOMPATIBLE_KEY_BLOB: Int](/documentation/security/cssmerr_appledl_incompatible_key_blob)
- [var CSSMERR_APPLEDL_INVALID_DATABASE_BLOB: Int](/documentation/security/cssmerr_appledl_invalid_database_blob)
- [var CSSMERR_APPLEDL_INVALID_KEY_BLOB: Int](/documentation/security/cssmerr_appledl_invalid_key_blob)
- [var CSSMERR_APPLEDL_INVALID_OPEN_PARAMETERS: Int](/documentation/security/cssmerr_appledl_invalid_open_parameters)
- [var CSSMERR_APPLEDL_QUOTA_EXCEEDED: Int](/documentation/security/cssmerr_appledl_quota_exceeded)
- [var CSSMERR_APPLETP_BAD_CERT_FROM_ISSUER: Int](/documentation/security/cssmerr_appletp_bad_cert_from_issuer)
- [var CSSMERR_APPLETP_CA_PIN_MISMATCH: Int](/documentation/security/cssmerr_appletp_ca_pin_mismatch)
- [var CSSMERR_APPLETP_CERT_NOT_FOUND_FROM_ISSUER: Int](/documentation/security/cssmerr_appletp_cert_not_found_from_issuer)
- [var CSSMERR_APPLETP_CODE_SIGN_DEVELOPMENT: Int](/documentation/security/cssmerr_appletp_code_sign_development)
- [var CSSMERR_APPLETP_CRL_BAD_URI: Int](/documentation/security/cssmerr_appletp_crl_bad_uri)
- [var CSSMERR_APPLETP_CRL_EXPIRED: Int](/documentation/security/cssmerr_appletp_crl_expired)
- [var CSSMERR_APPLETP_CRL_INVALID_ANCHOR_CERT: Int](/documentation/security/cssmerr_appletp_crl_invalid_anchor_cert)
- [var CSSMERR_APPLETP_CRL_NOT_FOUND: Int](/documentation/security/cssmerr_appletp_crl_not_found)
- [var CSSMERR_APPLETP_CRL_NOT_TRUSTED: Int](/documentation/security/cssmerr_appletp_crl_not_trusted)
- [var CSSMERR_APPLETP_CRL_NOT_VALID_YET: Int](/documentation/security/cssmerr_appletp_crl_not_valid_yet)
- [var CSSMERR_APPLETP_CRL_POLICY_FAIL: Int](/documentation/security/cssmerr_appletp_crl_policy_fail)
- [var CSSMERR_APPLETP_CRL_SERVER_DOWN: Int](/documentation/security/cssmerr_appletp_crl_server_down)
- [var CSSMERR_APPLETP_CS_BAD_CERT_CHAIN_LENGTH: Int](/documentation/security/cssmerr_appletp_cs_bad_cert_chain_length)
- [var CSSMERR_APPLETP_CS_BAD_PATH_LENGTH: Int](/documentation/security/cssmerr_appletp_cs_bad_path_length)
- [var CSSMERR_APPLETP_CS_NO_BASIC_CONSTRAINTS: Int](/documentation/security/cssmerr_appletp_cs_no_basic_constraints)
- [var CSSMERR_APPLETP_CS_NO_EXTENDED_KEY_USAGE: Int](/documentation/security/cssmerr_appletp_cs_no_extended_key_usage)
- [var CSSMERR_APPLETP_EXT_KEYUSAGE_NOT_CRITICAL: Int](/documentation/security/cssmerr_appletp_ext_keyusage_not_critical)
- [var CSSMERR_APPLETP_HOSTNAME_MISMATCH: Int](/documentation/security/cssmerr_appletp_hostname_mismatch)
- [var CSSMERR_APPLETP_IDENTIFIER_MISSING: Int](/documentation/security/cssmerr_appletp_identifier_missing)
- [var CSSMERR_APPLETP_IDP_FAIL: Int](/documentation/security/cssmerr_appletp_idp_fail)
- [var CSSMERR_APPLETP_INCOMPLETE_REVOCATION_CHECK: Int](/documentation/security/cssmerr_appletp_incomplete_revocation_check)
- [var CSSMERR_APPLETP_INVALID_AUTHORITY_ID: Int](/documentation/security/cssmerr_appletp_invalid_authority_id)
- [var CSSMERR_APPLETP_INVALID_CA: Int](/documentation/security/cssmerr_appletp_invalid_ca)
- [var CSSMERR_APPLETP_INVALID_EMPTY_SUBJECT: Int](/documentation/security/cssmerr_appletp_invalid_empty_subject)
- [var CSSMERR_APPLETP_INVALID_EXTENDED_KEY_USAGE: Int](/documentation/security/cssmerr_appletp_invalid_extended_key_usage)
- [var CSSMERR_APPLETP_INVALID_ID_LINKAGE: Int](/documentation/security/cssmerr_appletp_invalid_id_linkage)
- [var CSSMERR_APPLETP_INVALID_KEY_USAGE: Int](/documentation/security/cssmerr_appletp_invalid_key_usage)
- [var CSSMERR_APPLETP_INVALID_ROOT: Int](/documentation/security/cssmerr_appletp_invalid_root)
- [var CSSMERR_APPLETP_INVALID_SUBJECT_ID: Int](/documentation/security/cssmerr_appletp_invalid_subject_id)
- [var CSSMERR_APPLETP_LEAF_PIN_MISMATCH: Int](/documentation/security/cssmerr_appletp_leaf_pin_mismatch)
- [var CSSMERR_APPLETP_MISSING_REQUIRED_EXTENSION: Int](/documentation/security/cssmerr_appletp_missing_required_extension)
- [var CSSMERR_APPLETP_NETWORK_FAILURE: Int](/documentation/security/cssmerr_appletp_network_failure)
- [var CSSMERR_APPLETP_NO_BASIC_CONSTRAINTS: Int](/documentation/security/cssmerr_appletp_no_basic_constraints)
- [var CSSMERR_APPLETP_OCSP_BAD_REQUEST: Int](/documentation/security/cssmerr_appletp_ocsp_bad_request)
- [var CSSMERR_APPLETP_OCSP_BAD_RESPONSE: Int](/documentation/security/cssmerr_appletp_ocsp_bad_response)
- [var CSSMERR_APPLETP_OCSP_INVALID_ANCHOR_CERT: Int](/documentation/security/cssmerr_appletp_ocsp_invalid_anchor_cert)
- [var CSSMERR_APPLETP_OCSP_NONCE_MISMATCH: Int](/documentation/security/cssmerr_appletp_ocsp_nonce_mismatch)
- [var CSSMERR_APPLETP_OCSP_NOT_TRUSTED: Int](/documentation/security/cssmerr_appletp_ocsp_not_trusted)
- [var CSSMERR_APPLETP_OCSP_NO_SIGNER: Int](/documentation/security/cssmerr_appletp_ocsp_no_signer)
- [var CSSMERR_APPLETP_OCSP_RESP_INTERNAL_ERR: Int](/documentation/security/cssmerr_appletp_ocsp_resp_internal_err)
- [var CSSMERR_APPLETP_OCSP_RESP_MALFORMED_REQ: Int](/documentation/security/cssmerr_appletp_ocsp_resp_malformed_req)
- [var CSSMERR_APPLETP_OCSP_RESP_SIG_REQUIRED: Int](/documentation/security/cssmerr_appletp_ocsp_resp_sig_required)
- [var CSSMERR_APPLETP_OCSP_RESP_TRY_LATER: Int](/documentation/security/cssmerr_appletp_ocsp_resp_try_later)
- [var CSSMERR_APPLETP_OCSP_RESP_UNAUTHORIZED: Int](/documentation/security/cssmerr_appletp_ocsp_resp_unauthorized)
- [var CSSMERR_APPLETP_OCSP_SIG_ERROR: Int](/documentation/security/cssmerr_appletp_ocsp_sig_error)
- [var CSSMERR_APPLETP_OCSP_STATUS_UNRECOGNIZED: Int](/documentation/security/cssmerr_appletp_ocsp_status_unrecognized)
- [var CSSMERR_APPLETP_OCSP_UNAVAILABLE: Int](/documentation/security/cssmerr_appletp_ocsp_unavailable)
- [var CSSMERR_APPLETP_PATH_LEN_CONSTRAINT: Int](/documentation/security/cssmerr_appletp_path_len_constraint)
- [var CSSMERR_APPLETP_RS_BAD_CERT_CHAIN_LENGTH: Int](/documentation/security/cssmerr_appletp_rs_bad_cert_chain_length)
- [var CSSMERR_APPLETP_RS_BAD_EXTENDED_KEY_USAGE: Int](/documentation/security/cssmerr_appletp_rs_bad_extended_key_usage)
- [var CSSMERR_APPLETP_SMIME_BAD_EXT_KEY_USE: Int](/documentation/security/cssmerr_appletp_smime_bad_ext_key_use)
- [var CSSMERR_APPLETP_SMIME_BAD_KEY_USE: Int](/documentation/security/cssmerr_appletp_smime_bad_key_use)
- [var CSSMERR_APPLETP_SMIME_EMAIL_ADDRS_NOT_FOUND: Int](/documentation/security/cssmerr_appletp_smime_email_addrs_not_found)
- [var CSSMERR_APPLETP_SMIME_KEYUSAGE_NOT_CRITICAL: Int](/documentation/security/cssmerr_appletp_smime_keyusage_not_critical)
- [var CSSMERR_APPLETP_SMIME_NO_EMAIL_ADDRS: Int](/documentation/security/cssmerr_appletp_smime_no_email_addrs)
- [var CSSMERR_APPLETP_SMIME_SUBJ_ALT_NAME_NOT_CRIT: Int](/documentation/security/cssmerr_appletp_smime_subj_alt_name_not_crit)
- [var CSSMERR_APPLETP_SSL_BAD_EXT_KEY_USE: Int](/documentation/security/cssmerr_appletp_ssl_bad_ext_key_use)
- [var CSSMERR_APPLETP_TRUST_SETTING_DENY: Int](/documentation/security/cssmerr_appletp_trust_setting_deny)
- [var CSSMERR_APPLETP_UNKNOWN_CERT_EXTEN: Int](/documentation/security/cssmerr_appletp_unknown_cert_exten)
- [var CSSMERR_APPLETP_UNKNOWN_CRITICAL_EXTEN: Int](/documentation/security/cssmerr_appletp_unknown_critical_exten)
- [var CSSMERR_APPLETP_UNKNOWN_CRL_EXTEN: Int](/documentation/security/cssmerr_appletp_unknown_crl_exten)
- [var CSSMERR_APPLETP_UNKNOWN_QUAL_CERT_STATEMENT: Int](/documentation/security/cssmerr_appletp_unknown_qual_cert_statement)
- [var CSSMERR_APPLE_DOTMAC_CSR_VERIFY_FAIL: Int](/documentation/security/cssmerr_apple_dotmac_csr_verify_fail)
- [var CSSMERR_APPLE_DOTMAC_FAILED_CONSISTENCY_CHECK: Int](/documentation/security/cssmerr_apple_dotmac_failed_consistency_check)
- [var CSSMERR_APPLE_DOTMAC_NO_REQ_PENDING: Int](/documentation/security/cssmerr_apple_dotmac_no_req_pending)
- [var CSSMERR_APPLE_DOTMAC_REQ_IS_PENDING: Int](/documentation/security/cssmerr_apple_dotmac_req_is_pending)
- [var CSSMERR_APPLE_DOTMAC_REQ_QUEUED: Int](/documentation/security/cssmerr_apple_dotmac_req_queued)
- [var CSSMERR_APPLE_DOTMAC_REQ_REDIRECT: Int](/documentation/security/cssmerr_apple_dotmac_req_redirect)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_ALREADY_EXIST: Int](/documentation/security/cssmerr_apple_dotmac_req_server_already_exist)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_AUTH: Int](/documentation/security/cssmerr_apple_dotmac_req_server_auth)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_ERR: Int](/documentation/security/cssmerr_apple_dotmac_req_server_err)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_NOT_AVAIL: Int](/documentation/security/cssmerr_apple_dotmac_req_server_not_avail)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_PARAM: Int](/documentation/security/cssmerr_apple_dotmac_req_server_param)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_SERVICE_ERROR: Int](/documentation/security/cssmerr_apple_dotmac_req_server_service_error)
- [var CSSMERR_APPLE_DOTMAC_REQ_SERVER_UNIMPL: Int](/documentation/security/cssmerr_apple_dotmac_req_server_unimpl)
- [var CSSMERR_CL_CRL_ALREADY_SIGNED: Int](/documentation/security/cssmerr_cl_crl_already_signed)
- [var CSSMERR_CL_DEVICE_FAILED: Int](/documentation/security/cssmerr_cl_device_failed)
- [var CSSMERR_CL_DEVICE_RESET: Int](/documentation/security/cssmerr_cl_device_reset)
- [var CSSMERR_CL_FUNCTION_FAILED: Int](/documentation/security/cssmerr_cl_function_failed)
- [var CSSMERR_CL_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_cl_function_not_implemented)
- [var CSSMERR_CL_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_cl_insufficient_client_identification)
- [var CSSMERR_CL_INTERNAL_ERROR: Int](/documentation/security/cssmerr_cl_internal_error)
- [var CSSMERR_CL_INVALID_BUNDLE_INFO: Int](/documentation/security/cssmerr_cl_invalid_bundle_info)
- [var CSSMERR_CL_INVALID_BUNDLE_POINTER: Int](/documentation/security/cssmerr_cl_invalid_bundle_pointer)
- [var CSSMERR_CL_INVALID_CACHE_HANDLE: Int](/documentation/security/cssmerr_cl_invalid_cache_handle)
- [var CSSMERR_CL_INVALID_CERTGROUP_POINTER: Int](/documentation/security/cssmerr_cl_invalid_certgroup_pointer)
- [var CSSMERR_CL_INVALID_CERT_POINTER: Int](/documentation/security/cssmerr_cl_invalid_cert_pointer)
- [var CSSMERR_CL_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssmerr_cl_invalid_context_handle)
- [var CSSMERR_CL_INVALID_CRL_INDEX: Int](/documentation/security/cssmerr_cl_invalid_crl_index)
- [var CSSMERR_CL_INVALID_CRL_POINTER: Int](/documentation/security/cssmerr_cl_invalid_crl_pointer)
- [var CSSMERR_CL_INVALID_DATA: Int](/documentation/security/cssmerr_cl_invalid_data)
- [var CSSMERR_CL_INVALID_FIELD_POINTER: Int](/documentation/security/cssmerr_cl_invalid_field_pointer)
- [var CSSMERR_CL_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_cl_invalid_input_pointer)
- [var CSSMERR_CL_INVALID_NUMBER_OF_FIELDS: Int](/documentation/security/cssmerr_cl_invalid_number_of_fields)
- [var CSSMERR_CL_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_cl_invalid_output_pointer)
- [var CSSMERR_CL_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssmerr_cl_invalid_passthrough_id)
- [var CSSMERR_CL_INVALID_POINTER: Int](/documentation/security/cssmerr_cl_invalid_pointer)
- [var CSSMERR_CL_INVALID_RESULTS_HANDLE: Int](/documentation/security/cssmerr_cl_invalid_results_handle)
- [var CSSMERR_CL_INVALID_SCOPE: Int](/documentation/security/cssmerr_cl_invalid_scope)
- [var CSSMERR_CL_IN_DARK_WAKE: Int](/documentation/security/cssmerr_cl_in_dark_wake)
- [var CSSMERR_CL_MDS_ERROR: Int](/documentation/security/cssmerr_cl_mds_error)
- [var CSSMERR_CL_MEMORY_ERROR: Int](/documentation/security/cssmerr_cl_memory_error)
- [var CSSMERR_CL_NO_FIELD_VALUES: Int](/documentation/security/cssmerr_cl_no_field_values)
- [var CSSMERR_CL_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_cl_no_user_interaction)
- [var CSSMERR_CL_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_cl_os_access_denied)
- [var CSSMERR_CL_SCOPE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_cl_scope_not_supported)
- [var CSSMERR_CL_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_cl_self_check_failed)
- [var CSSMERR_CL_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_cl_service_not_available)
- [var CSSMERR_CL_UNKNOWN_FORMAT: Int](/documentation/security/cssmerr_cl_unknown_format)
- [var CSSMERR_CL_UNKNOWN_TAG: Int](/documentation/security/cssmerr_cl_unknown_tag)
- [var CSSMERR_CL_USER_CANCELED: Int](/documentation/security/cssmerr_cl_user_canceled)
- [var CSSMERR_CL_VERIFICATION_FAILURE: Int](/documentation/security/cssmerr_cl_verification_failure)
- [var CSSMERR_CSPDL_APPLE_DL_CONVERSION_ERROR: Int](/documentation/security/cssmerr_cspdl_apple_dl_conversion_error)
- [var CSSMERR_CSP_ACL_ADD_FAILED: Int](/documentation/security/cssmerr_csp_acl_add_failed)
- [var CSSMERR_CSP_ACL_BASE_CERTS_NOT_SUPPORTED: Int](/documentation/security/cssmerr_csp_acl_base_certs_not_supported)
- [var CSSMERR_CSP_ACL_CHALLENGE_CALLBACK_FAILED: Int](/documentation/security/cssmerr_csp_acl_challenge_callback_failed)
- [var CSSMERR_CSP_ACL_CHANGE_FAILED: Int](/documentation/security/cssmerr_csp_acl_change_failed)
- [var CSSMERR_CSP_ACL_DELETE_FAILED: Int](/documentation/security/cssmerr_csp_acl_delete_failed)
- [var CSSMERR_CSP_ACL_ENTRY_TAG_NOT_FOUND: Int](/documentation/security/cssmerr_csp_acl_entry_tag_not_found)
- [var CSSMERR_CSP_ACL_REPLACE_FAILED: Int](/documentation/security/cssmerr_csp_acl_replace_failed)
- [var CSSMERR_CSP_ACL_SUBJECT_TYPE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_csp_acl_subject_type_not_supported)
- [var CSSMERR_CSP_ALGID_MISMATCH: Int](/documentation/security/cssmerr_csp_algid_mismatch)
- [var CSSMERR_CSP_ALREADY_LOGGED_IN: Int](/documentation/security/cssmerr_csp_already_logged_in)
- [var CSSMERR_CSP_APPLE_ADD_APPLICATION_ACL_SUBJECT: Int](/documentation/security/cssmerr_csp_apple_add_application_acl_subject)
- [var CSSMERR_CSP_APPLE_INVALID_KEY_END_DATE: Int](/documentation/security/cssmerr_csp_apple_invalid_key_end_date)
- [var CSSMERR_CSP_APPLE_INVALID_KEY_START_DATE: Int](/documentation/security/cssmerr_csp_apple_invalid_key_start_date)
- [var CSSMERR_CSP_APPLE_PUBLIC_KEY_INCOMPLETE: Int](/documentation/security/cssmerr_csp_apple_public_key_incomplete)
- [var CSSMERR_CSP_APPLE_SIGNATURE_MISMATCH: Int](/documentation/security/cssmerr_csp_apple_signature_mismatch)
- [var CSSMERR_CSP_APPLE_SSLv2_ROLLBACK: Int](/documentation/security/cssmerr_csp_apple_sslv2_rollback)
- [var CSSMERR_CSP_ATTACH_HANDLE_BUSY: Int](/documentation/security/cssmerr_csp_attach_handle_busy)
- [var CSSMERR_CSP_BLOCK_SIZE_MISMATCH: Int](/documentation/security/cssmerr_csp_block_size_mismatch)
- [var CSSMERR_CSP_CRYPTO_DATA_CALLBACK_FAILED: Int](/documentation/security/cssmerr_csp_crypto_data_callback_failed)
- [var CSSMERR_CSP_DEVICE_ERROR: Int](/documentation/security/cssmerr_csp_device_error)
- [var CSSMERR_CSP_DEVICE_FAILED: Int](/documentation/security/cssmerr_csp_device_failed)
- [var CSSMERR_CSP_DEVICE_MEMORY_ERROR: Int](/documentation/security/cssmerr_csp_device_memory_error)
- [var CSSMERR_CSP_DEVICE_RESET: Int](/documentation/security/cssmerr_csp_device_reset)
- [var CSSMERR_CSP_DEVICE_VERIFY_FAILED: Int](/documentation/security/cssmerr_csp_device_verify_failed)
- [var CSSMERR_CSP_FUNCTION_FAILED: Int](/documentation/security/cssmerr_csp_function_failed)
- [var CSSMERR_CSP_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_csp_function_not_implemented)
- [var CSSMERR_CSP_INPUT_LENGTH_ERROR: Int](/documentation/security/cssmerr_csp_input_length_error)
- [var CSSMERR_CSP_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_csp_insufficient_client_identification)
- [var CSSMERR_CSP_INTERNAL_ERROR: Int](/documentation/security/cssmerr_csp_internal_error)
- [var CSSMERR_CSP_INVALID_ACCESS_CREDENTIALS: Int](/documentation/security/cssmerr_csp_invalid_access_credentials)
- [var CSSMERR_CSP_INVALID_ACL_BASE_CERTS: Int](/documentation/security/cssmerr_csp_invalid_acl_base_certs)
- [var CSSMERR_CSP_INVALID_ACL_CHALLENGE_CALLBACK: Int](/documentation/security/cssmerr_csp_invalid_acl_challenge_callback)
- [var CSSMERR_CSP_INVALID_ACL_EDIT_MODE: Int](/documentation/security/cssmerr_csp_invalid_acl_edit_mode)
- [var CSSMERR_CSP_INVALID_ACL_ENTRY_TAG: Int](/documentation/security/cssmerr_csp_invalid_acl_entry_tag)
- [var CSSMERR_CSP_INVALID_ACL_SUBJECT_VALUE: Int](/documentation/security/cssmerr_csp_invalid_acl_subject_value)
- [var CSSMERR_CSP_INVALID_ALGORITHM: Int](/documentation/security/cssmerr_csp_invalid_algorithm)
- [var CSSMERR_CSP_INVALID_ATTR_ACCESS_CREDENTIALS: Int](/documentation/security/cssmerr_csp_invalid_attr_access_credentials)
- [var CSSMERR_CSP_INVALID_ATTR_ALG_PARAMS: Int](/documentation/security/cssmerr_csp_invalid_attr_alg_params)
- [var CSSMERR_CSP_INVALID_ATTR_BASE: Int](/documentation/security/cssmerr_csp_invalid_attr_base)
- [var CSSMERR_CSP_INVALID_ATTR_BLOCK_SIZE: Int](/documentation/security/cssmerr_csp_invalid_attr_block_size)
- [var CSSMERR_CSP_INVALID_ATTR_DL_DB_HANDLE: Int](/documentation/security/cssmerr_csp_invalid_attr_dl_db_handle)
- [var CSSMERR_CSP_INVALID_ATTR_EFFECTIVE_BITS: Int](/documentation/security/cssmerr_csp_invalid_attr_effective_bits)
- [var CSSMERR_CSP_INVALID_ATTR_END_DATE: Int](/documentation/security/cssmerr_csp_invalid_attr_end_date)
- [var CSSMERR_CSP_INVALID_ATTR_INIT_VECTOR: Int](/documentation/security/cssmerr_csp_invalid_attr_init_vector)
- [var CSSMERR_CSP_INVALID_ATTR_ITERATION_COUNT: Int](/documentation/security/cssmerr_csp_invalid_attr_iteration_count)
- [var CSSMERR_CSP_INVALID_ATTR_KEY: Int](/documentation/security/cssmerr_csp_invalid_attr_key)
- [var CSSMERR_CSP_INVALID_ATTR_KEY_LENGTH: Int](/documentation/security/cssmerr_csp_invalid_attr_key_length)
- [var CSSMERR_CSP_INVALID_ATTR_KEY_TYPE: Int](/documentation/security/cssmerr_csp_invalid_attr_key_type)
- [var CSSMERR_CSP_INVALID_ATTR_LABEL: Int](/documentation/security/cssmerr_csp_invalid_attr_label)
- [var CSSMERR_CSP_INVALID_ATTR_MODE: Int](/documentation/security/cssmerr_csp_invalid_attr_mode)
- [var CSSMERR_CSP_INVALID_ATTR_OUTPUT_SIZE: Int](/documentation/security/cssmerr_csp_invalid_attr_output_size)
- [var CSSMERR_CSP_INVALID_ATTR_PADDING: Int](/documentation/security/cssmerr_csp_invalid_attr_padding)
- [var CSSMERR_CSP_INVALID_ATTR_PASSPHRASE: Int](/documentation/security/cssmerr_csp_invalid_attr_passphrase)
- [var CSSMERR_CSP_INVALID_ATTR_PRIME: Int](/documentation/security/cssmerr_csp_invalid_attr_prime)
- [var CSSMERR_CSP_INVALID_ATTR_PRIVATE_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_invalid_attr_private_key_format)
- [var CSSMERR_CSP_INVALID_ATTR_PUBLIC_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_invalid_attr_public_key_format)
- [var CSSMERR_CSP_INVALID_ATTR_RANDOM: Int](/documentation/security/cssmerr_csp_invalid_attr_random)
- [var CSSMERR_CSP_INVALID_ATTR_ROUNDS: Int](/documentation/security/cssmerr_csp_invalid_attr_rounds)
- [var CSSMERR_CSP_INVALID_ATTR_SALT: Int](/documentation/security/cssmerr_csp_invalid_attr_salt)
- [var CSSMERR_CSP_INVALID_ATTR_SEED: Int](/documentation/security/cssmerr_csp_invalid_attr_seed)
- [var CSSMERR_CSP_INVALID_ATTR_START_DATE: Int](/documentation/security/cssmerr_csp_invalid_attr_start_date)
- [var CSSMERR_CSP_INVALID_ATTR_SUBPRIME: Int](/documentation/security/cssmerr_csp_invalid_attr_subprime)
- [var CSSMERR_CSP_INVALID_ATTR_SYMMETRIC_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_invalid_attr_symmetric_key_format)
- [var CSSMERR_CSP_INVALID_ATTR_VERSION: Int](/documentation/security/cssmerr_csp_invalid_attr_version)
- [var CSSMERR_CSP_INVALID_ATTR_WRAPPED_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_invalid_attr_wrapped_key_format)
- [var CSSMERR_CSP_INVALID_CONTEXT: Int](/documentation/security/cssmerr_csp_invalid_context)
- [var CSSMERR_CSP_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssmerr_csp_invalid_context_handle)
- [var CSSMERR_CSP_INVALID_CRYPTO_DATA: Int](/documentation/security/cssmerr_csp_invalid_crypto_data)
- [var CSSMERR_CSP_INVALID_DATA: Int](/documentation/security/cssmerr_csp_invalid_data)
- [var CSSMERR_CSP_INVALID_DATA_COUNT: Int](/documentation/security/cssmerr_csp_invalid_data_count)
- [var CSSMERR_CSP_INVALID_DIGEST_ALGORITHM: Int](/documentation/security/cssmerr_csp_invalid_digest_algorithm)
- [var CSSMERR_CSP_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_csp_invalid_input_pointer)
- [var CSSMERR_CSP_INVALID_INPUT_VECTOR: Int](/documentation/security/cssmerr_csp_invalid_input_vector)
- [var CSSMERR_CSP_INVALID_KEY: Int](/documentation/security/cssmerr_csp_invalid_key)
- [var CSSMERR_CSP_INVALID_KEYATTR_MASK: Int](/documentation/security/cssmerr_csp_invalid_keyattr_mask)
- [var CSSMERR_CSP_INVALID_KEYUSAGE_MASK: Int](/documentation/security/cssmerr_csp_invalid_keyusage_mask)
- [var CSSMERR_CSP_INVALID_KEY_CLASS: Int](/documentation/security/cssmerr_csp_invalid_key_class)
- [var CSSMERR_CSP_INVALID_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_invalid_key_format)
- [var CSSMERR_CSP_INVALID_KEY_LABEL: Int](/documentation/security/cssmerr_csp_invalid_key_label)
- [var CSSMERR_CSP_INVALID_KEY_POINTER: Int](/documentation/security/cssmerr_csp_invalid_key_pointer)
- [var CSSMERR_CSP_INVALID_KEY_REFERENCE: Int](/documentation/security/cssmerr_csp_invalid_key_reference)
- [var CSSMERR_CSP_INVALID_LOGIN_NAME: Int](/documentation/security/cssmerr_csp_invalid_login_name)
- [var CSSMERR_CSP_INVALID_NEW_ACL_ENTRY: Int](/documentation/security/cssmerr_csp_invalid_new_acl_entry)
- [var CSSMERR_CSP_INVALID_NEW_ACL_OWNER: Int](/documentation/security/cssmerr_csp_invalid_new_acl_owner)
- [var CSSMERR_CSP_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_csp_invalid_output_pointer)
- [var CSSMERR_CSP_INVALID_OUTPUT_VECTOR: Int](/documentation/security/cssmerr_csp_invalid_output_vector)
- [var CSSMERR_CSP_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssmerr_csp_invalid_passthrough_id)
- [var CSSMERR_CSP_INVALID_POINTER: Int](/documentation/security/cssmerr_csp_invalid_pointer)
- [var CSSMERR_CSP_INVALID_SAMPLE_VALUE: Int](/documentation/security/cssmerr_csp_invalid_sample_value)
- [var CSSMERR_CSP_INVALID_SIGNATURE: Int](/documentation/security/cssmerr_csp_invalid_signature)
- [var CSSMERR_CSP_IN_DARK_WAKE: Int](/documentation/security/cssmerr_csp_in_dark_wake)
- [var CSSMERR_CSP_KEY_BLOB_TYPE_INCORRECT: Int](/documentation/security/cssmerr_csp_key_blob_type_incorrect)
- [var CSSMERR_CSP_KEY_HEADER_INCONSISTENT: Int](/documentation/security/cssmerr_csp_key_header_inconsistent)
- [var CSSMERR_CSP_KEY_LABEL_ALREADY_EXISTS: Int](/documentation/security/cssmerr_csp_key_label_already_exists)
- [var CSSMERR_CSP_KEY_USAGE_INCORRECT: Int](/documentation/security/cssmerr_csp_key_usage_incorrect)
- [var CSSMERR_CSP_MDS_ERROR: Int](/documentation/security/cssmerr_csp_mds_error)
- [var CSSMERR_CSP_MEMORY_ERROR: Int](/documentation/security/cssmerr_csp_memory_error)
- [var CSSMERR_CSP_MISSING_ATTR_ACCESS_CREDENTIALS: Int](/documentation/security/cssmerr_csp_missing_attr_access_credentials)
- [var CSSMERR_CSP_MISSING_ATTR_ALG_PARAMS: Int](/documentation/security/cssmerr_csp_missing_attr_alg_params)
- [var CSSMERR_CSP_MISSING_ATTR_BASE: Int](/documentation/security/cssmerr_csp_missing_attr_base)
- [var CSSMERR_CSP_MISSING_ATTR_BLOCK_SIZE: Int](/documentation/security/cssmerr_csp_missing_attr_block_size)
- [var CSSMERR_CSP_MISSING_ATTR_DL_DB_HANDLE: Int](/documentation/security/cssmerr_csp_missing_attr_dl_db_handle)
- [var CSSMERR_CSP_MISSING_ATTR_EFFECTIVE_BITS: Int](/documentation/security/cssmerr_csp_missing_attr_effective_bits)
- [var CSSMERR_CSP_MISSING_ATTR_END_DATE: Int](/documentation/security/cssmerr_csp_missing_attr_end_date)
- [var CSSMERR_CSP_MISSING_ATTR_INIT_VECTOR: Int](/documentation/security/cssmerr_csp_missing_attr_init_vector)
- [var CSSMERR_CSP_MISSING_ATTR_ITERATION_COUNT: Int](/documentation/security/cssmerr_csp_missing_attr_iteration_count)
- [var CSSMERR_CSP_MISSING_ATTR_KEY: Int](/documentation/security/cssmerr_csp_missing_attr_key)
- [var CSSMERR_CSP_MISSING_ATTR_KEY_LENGTH: Int](/documentation/security/cssmerr_csp_missing_attr_key_length)
- [var CSSMERR_CSP_MISSING_ATTR_KEY_TYPE: Int](/documentation/security/cssmerr_csp_missing_attr_key_type)
- [var CSSMERR_CSP_MISSING_ATTR_LABEL: Int](/documentation/security/cssmerr_csp_missing_attr_label)
- [var CSSMERR_CSP_MISSING_ATTR_MODE: Int](/documentation/security/cssmerr_csp_missing_attr_mode)
- [var CSSMERR_CSP_MISSING_ATTR_OUTPUT_SIZE: Int](/documentation/security/cssmerr_csp_missing_attr_output_size)
- [var CSSMERR_CSP_MISSING_ATTR_PADDING: Int](/documentation/security/cssmerr_csp_missing_attr_padding)
- [var CSSMERR_CSP_MISSING_ATTR_PASSPHRASE: Int](/documentation/security/cssmerr_csp_missing_attr_passphrase)
- [var CSSMERR_CSP_MISSING_ATTR_PRIME: Int](/documentation/security/cssmerr_csp_missing_attr_prime)
- [var CSSMERR_CSP_MISSING_ATTR_PRIVATE_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_missing_attr_private_key_format)
- [var CSSMERR_CSP_MISSING_ATTR_PUBLIC_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_missing_attr_public_key_format)
- [var CSSMERR_CSP_MISSING_ATTR_RANDOM: Int](/documentation/security/cssmerr_csp_missing_attr_random)
- [var CSSMERR_CSP_MISSING_ATTR_ROUNDS: Int](/documentation/security/cssmerr_csp_missing_attr_rounds)
- [var CSSMERR_CSP_MISSING_ATTR_SALT: Int](/documentation/security/cssmerr_csp_missing_attr_salt)
- [var CSSMERR_CSP_MISSING_ATTR_SEED: Int](/documentation/security/cssmerr_csp_missing_attr_seed)
- [var CSSMERR_CSP_MISSING_ATTR_START_DATE: Int](/documentation/security/cssmerr_csp_missing_attr_start_date)
- [var CSSMERR_CSP_MISSING_ATTR_SUBPRIME: Int](/documentation/security/cssmerr_csp_missing_attr_subprime)
- [var CSSMERR_CSP_MISSING_ATTR_SYMMETRIC_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_missing_attr_symmetric_key_format)
- [var CSSMERR_CSP_MISSING_ATTR_VERSION: Int](/documentation/security/cssmerr_csp_missing_attr_version)
- [var CSSMERR_CSP_MISSING_ATTR_WRAPPED_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_missing_attr_wrapped_key_format)
- [var CSSMERR_CSP_NOT_LOGGED_IN: Int](/documentation/security/cssmerr_csp_not_logged_in)
- [var CSSMERR_CSP_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_csp_no_user_interaction)
- [var CSSMERR_CSP_OBJECT_ACL_NOT_SUPPORTED: Int](/documentation/security/cssmerr_csp_object_acl_not_supported)
- [var CSSMERR_CSP_OBJECT_ACL_REQUIRED: Int](/documentation/security/cssmerr_csp_object_acl_required)
- [var CSSMERR_CSP_OBJECT_MANIP_AUTH_DENIED: Int](/documentation/security/cssmerr_csp_object_manip_auth_denied)
- [var CSSMERR_CSP_OBJECT_USE_AUTH_DENIED: Int](/documentation/security/cssmerr_csp_object_use_auth_denied)
- [var CSSMERR_CSP_OPERATION_AUTH_DENIED: Int](/documentation/security/cssmerr_csp_operation_auth_denied)
- [var CSSMERR_CSP_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_csp_os_access_denied)
- [var CSSMERR_CSP_OUTPUT_LENGTH_ERROR: Int](/documentation/security/cssmerr_csp_output_length_error)
- [var CSSMERR_CSP_PRIVATE_KEY_ALREADY_EXISTS: Int](/documentation/security/cssmerr_csp_private_key_already_exists)
- [var CSSMERR_CSP_PRIVATE_KEY_NOT_FOUND: Int](/documentation/security/cssmerr_csp_private_key_not_found)
- [var CSSMERR_CSP_PRIVILEGE_NOT_GRANTED: Int](/documentation/security/cssmerr_csp_privilege_not_granted)
- [var CSSMERR_CSP_PRIVILEGE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_csp_privilege_not_supported)
- [var CSSMERR_CSP_PUBLIC_KEY_INCONSISTENT: Int](/documentation/security/cssmerr_csp_public_key_inconsistent)
- [var CSSMERR_CSP_QUERY_SIZE_UNKNOWN: Int](/documentation/security/cssmerr_csp_query_size_unknown)
- [var CSSMERR_CSP_SAMPLE_VALUE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_csp_sample_value_not_supported)
- [var CSSMERR_CSP_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_csp_self_check_failed)
- [var CSSMERR_CSP_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_csp_service_not_available)
- [var CSSMERR_CSP_STAGED_OPERATION_IN_PROGRESS: Int](/documentation/security/cssmerr_csp_staged_operation_in_progress)
- [var CSSMERR_CSP_STAGED_OPERATION_NOT_STARTED: Int](/documentation/security/cssmerr_csp_staged_operation_not_started)
- [var CSSMERR_CSP_UNSUPPORTED_KEYATTR_MASK: Int](/documentation/security/cssmerr_csp_unsupported_keyattr_mask)
- [var CSSMERR_CSP_UNSUPPORTED_KEYUSAGE_MASK: Int](/documentation/security/cssmerr_csp_unsupported_keyusage_mask)
- [var CSSMERR_CSP_UNSUPPORTED_KEY_FORMAT: Int](/documentation/security/cssmerr_csp_unsupported_key_format)
- [var CSSMERR_CSP_UNSUPPORTED_KEY_LABEL: Int](/documentation/security/cssmerr_csp_unsupported_key_label)
- [var CSSMERR_CSP_UNSUPPORTED_KEY_SIZE: Int](/documentation/security/cssmerr_csp_unsupported_key_size)
- [var CSSMERR_CSP_USER_CANCELED: Int](/documentation/security/cssmerr_csp_user_canceled)
- [var CSSMERR_CSP_VECTOR_OF_BUFS_UNSUPPORTED: Int](/documentation/security/cssmerr_csp_vector_of_bufs_unsupported)
- [var CSSMERR_CSP_VERIFY_FAILED: Int](/documentation/security/cssmerr_csp_verify_failed)
- [var CSSMERR_CSSM_ADDIN_AUTHENTICATE_FAILED: Int](/documentation/security/cssmerr_cssm_addin_authenticate_failed)
- [var CSSMERR_CSSM_ADDIN_LOAD_FAILED: Int](/documentation/security/cssmerr_cssm_addin_load_failed)
- [var CSSMERR_CSSM_ADDIN_UNLOAD_FAILED: Int](/documentation/security/cssmerr_cssm_addin_unload_failed)
- [var CSSMERR_CSSM_ATTRIBUTE_NOT_IN_CONTEXT: Int](/documentation/security/cssmerr_cssm_attribute_not_in_context)
- [var CSSMERR_CSSM_BUFFER_TOO_SMALL: Int](/documentation/security/cssmerr_cssm_buffer_too_small)
- [var CSSMERR_CSSM_DEVICE_FAILED: Int](/documentation/security/cssmerr_cssm_device_failed)
- [var CSSMERR_CSSM_DEVICE_RESET: Int](/documentation/security/cssmerr_cssm_device_reset)
- [var CSSMERR_CSSM_EMM_AUTHENTICATE_FAILED: Int](/documentation/security/cssmerr_cssm_emm_authenticate_failed)
- [var CSSMERR_CSSM_EMM_LOAD_FAILED: Int](/documentation/security/cssmerr_cssm_emm_load_failed)
- [var CSSMERR_CSSM_EMM_UNLOAD_FAILED: Int](/documentation/security/cssmerr_cssm_emm_unload_failed)
- [var CSSMERR_CSSM_EVENT_NOTIFICATION_CALLBACK_NOT_FOUND: Int](/documentation/security/cssmerr_cssm_event_notification_callback_not_found)
- [var CSSMERR_CSSM_FUNCTION_FAILED: Int](/documentation/security/cssmerr_cssm_function_failed)
- [var CSSMERR_CSSM_FUNCTION_INTEGRITY_FAIL: Int](/documentation/security/cssmerr_cssm_function_integrity_fail)
- [var CSSMERR_CSSM_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_cssm_function_not_implemented)
- [var CSSMERR_CSSM_INCOMPATIBLE_VERSION: Int](/documentation/security/cssmerr_cssm_incompatible_version)
- [var CSSMERR_CSSM_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_cssm_insufficient_client_identification)
- [var CSSMERR_CSSM_INTERNAL_ERROR: Int](/documentation/security/cssmerr_cssm_internal_error)
- [var CSSMERR_CSSM_INVALID_ADDIN_FUNCTION_TABLE: Int](/documentation/security/cssmerr_cssm_invalid_addin_function_table)
- [var CSSMERR_CSSM_INVALID_ADDIN_HANDLE: Int](/documentation/security/cssmerr_cssm_invalid_addin_handle)
- [var CSSMERR_CSSM_INVALID_ATTRIBUTE: Int](/documentation/security/cssmerr_cssm_invalid_attribute)
- [var CSSMERR_CSSM_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssmerr_cssm_invalid_context_handle)
- [var CSSMERR_CSSM_INVALID_GUID: Int](/documentation/security/cssmerr_cssm_invalid_guid)
- [var CSSMERR_CSSM_INVALID_HANDLE_USAGE: Int](/documentation/security/cssmerr_cssm_invalid_handle_usage)
- [var CSSMERR_CSSM_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_cssm_invalid_input_pointer)
- [var CSSMERR_CSSM_INVALID_KEY_HIERARCHY: Int](/documentation/security/cssmerr_cssm_invalid_key_hierarchy)
- [var CSSMERR_CSSM_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_cssm_invalid_output_pointer)
- [var CSSMERR_CSSM_INVALID_POINTER: Int](/documentation/security/cssmerr_cssm_invalid_pointer)
- [var CSSMERR_CSSM_INVALID_PVC: Int](/documentation/security/cssmerr_cssm_invalid_pvc)
- [var CSSMERR_CSSM_INVALID_SERVICE_MASK: Int](/documentation/security/cssmerr_cssm_invalid_service_mask)
- [var CSSMERR_CSSM_INVALID_SUBSERVICEID: Int](/documentation/security/cssmerr_cssm_invalid_subserviceid)
- [var CSSMERR_CSSM_IN_DARK_WAKE: Int](/documentation/security/cssmerr_cssm_in_dark_wake)
- [var CSSMERR_CSSM_LIB_REF_NOT_FOUND: Int](/documentation/security/cssmerr_cssm_lib_ref_not_found)
- [var CSSMERR_CSSM_MDS_ERROR: Int](/documentation/security/cssmerr_cssm_mds_error)
- [var CSSMERR_CSSM_MEMORY_ERROR: Int](/documentation/security/cssmerr_cssm_memory_error)
- [var CSSMERR_CSSM_MODULE_MANAGER_INITIALIZE_FAIL: Int](/documentation/security/cssmerr_cssm_module_manager_initialize_fail)
- [var CSSMERR_CSSM_MODULE_MANAGER_NOT_FOUND: Int](/documentation/security/cssmerr_cssm_module_manager_not_found)
- [var CSSMERR_CSSM_MODULE_MANIFEST_VERIFY_FAILED: Int](/documentation/security/cssmerr_cssm_module_manifest_verify_failed)
- [var CSSMERR_CSSM_MODULE_NOT_LOADED: Int](/documentation/security/cssmerr_cssm_module_not_loaded)
- [var CSSMERR_CSSM_NOT_INITIALIZED: Int](/documentation/security/cssmerr_cssm_not_initialized)
- [var CSSMERR_CSSM_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_cssm_no_user_interaction)
- [var CSSMERR_CSSM_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_cssm_os_access_denied)
- [var CSSMERR_CSSM_PRIVILEGE_NOT_GRANTED: Int](/documentation/security/cssmerr_cssm_privilege_not_granted)
- [var CSSMERR_CSSM_PVC_ALREADY_CONFIGURED: Int](/documentation/security/cssmerr_cssm_pvc_already_configured)
- [var CSSMERR_CSSM_PVC_REFERENT_NOT_FOUND: Int](/documentation/security/cssmerr_cssm_pvc_referent_not_found)
- [var CSSMERR_CSSM_SCOPE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_cssm_scope_not_supported)
- [var CSSMERR_CSSM_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_cssm_self_check_failed)
- [var CSSMERR_CSSM_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_cssm_service_not_available)
- [var CSSMERR_CSSM_USER_CANCELED: Int](/documentation/security/cssmerr_cssm_user_canceled)
- [var CSSMERR_DL_ACL_ADD_FAILED: Int](/documentation/security/cssmerr_dl_acl_add_failed)
- [var CSSMERR_DL_ACL_BASE_CERTS_NOT_SUPPORTED: Int](/documentation/security/cssmerr_dl_acl_base_certs_not_supported)
- [var CSSMERR_DL_ACL_CHALLENGE_CALLBACK_FAILED: Int](/documentation/security/cssmerr_dl_acl_challenge_callback_failed)
- [var CSSMERR_DL_ACL_CHANGE_FAILED: Int](/documentation/security/cssmerr_dl_acl_change_failed)
- [var CSSMERR_DL_ACL_DELETE_FAILED: Int](/documentation/security/cssmerr_dl_acl_delete_failed)
- [var CSSMERR_DL_ACL_ENTRY_TAG_NOT_FOUND: Int](/documentation/security/cssmerr_dl_acl_entry_tag_not_found)
- [var CSSMERR_DL_ACL_REPLACE_FAILED: Int](/documentation/security/cssmerr_dl_acl_replace_failed)
- [var CSSMERR_DL_ACL_SUBJECT_TYPE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_dl_acl_subject_type_not_supported)
- [var CSSMERR_DL_DATABASE_CORRUPT: Int](/documentation/security/cssmerr_dl_database_corrupt)
- [var CSSMERR_DL_DATASTORE_ALREADY_EXISTS: Int](/documentation/security/cssmerr_dl_datastore_already_exists)
- [var CSSMERR_DL_DATASTORE_DOESNOT_EXIST: Int](/documentation/security/cssmerr_dl_datastore_doesnot_exist)
- [var CSSMERR_DL_DATASTORE_IS_OPEN: Int](/documentation/security/cssmerr_dl_datastore_is_open)
- [var CSSMERR_DL_DB_LOCKED: Int](/documentation/security/cssmerr_dl_db_locked)
- [var CSSMERR_DL_DEVICE_FAILED: Int](/documentation/security/cssmerr_dl_device_failed)
- [var CSSMERR_DL_DEVICE_RESET: Int](/documentation/security/cssmerr_dl_device_reset)
- [var CSSMERR_DL_ENDOFDATA: Int](/documentation/security/cssmerr_dl_endofdata)
- [var CSSMERR_DL_FIELD_SPECIFIED_MULTIPLE: Int](/documentation/security/cssmerr_dl_field_specified_multiple)
- [var CSSMERR_DL_FUNCTION_FAILED: Int](/documentation/security/cssmerr_dl_function_failed)
- [var CSSMERR_DL_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_dl_function_not_implemented)
- [var CSSMERR_DL_INCOMPATIBLE_FIELD_FORMAT: Int](/documentation/security/cssmerr_dl_incompatible_field_format)
- [var CSSMERR_DL_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_dl_insufficient_client_identification)
- [var CSSMERR_DL_INTERNAL_ERROR: Int](/documentation/security/cssmerr_dl_internal_error)
- [var CSSMERR_DL_INVALID_ACCESS_CREDENTIALS: Int](/documentation/security/cssmerr_dl_invalid_access_credentials)
- [var CSSMERR_DL_INVALID_ACCESS_REQUEST: Int](/documentation/security/cssmerr_dl_invalid_access_request)
- [var CSSMERR_DL_INVALID_ACL_BASE_CERTS: Int](/documentation/security/cssmerr_dl_invalid_acl_base_certs)
- [var CSSMERR_DL_INVALID_ACL_CHALLENGE_CALLBACK: Int](/documentation/security/cssmerr_dl_invalid_acl_challenge_callback)
- [var CSSMERR_DL_INVALID_ACL_EDIT_MODE: Int](/documentation/security/cssmerr_dl_invalid_acl_edit_mode)
- [var CSSMERR_DL_INVALID_ACL_ENTRY_TAG: Int](/documentation/security/cssmerr_dl_invalid_acl_entry_tag)
- [var CSSMERR_DL_INVALID_ACL_SUBJECT_VALUE: Int](/documentation/security/cssmerr_dl_invalid_acl_subject_value)
- [var CSSMERR_DL_INVALID_CL_HANDLE: Int](/documentation/security/cssmerr_dl_invalid_cl_handle)
- [var CSSMERR_DL_INVALID_CSP_HANDLE: Int](/documentation/security/cssmerr_dl_invalid_csp_handle)
- [var CSSMERR_DL_INVALID_DB_HANDLE: Int](/documentation/security/cssmerr_dl_invalid_db_handle)
- [var CSSMERR_DL_INVALID_DB_LIST_POINTER: Int](/documentation/security/cssmerr_dl_invalid_db_list_pointer)
- [var CSSMERR_DL_INVALID_DB_LOCATION: Int](/documentation/security/cssmerr_dl_invalid_db_location)
- [var CSSMERR_DL_INVALID_DB_NAME: Int](/documentation/security/cssmerr_dl_invalid_db_name)
- [var CSSMERR_DL_INVALID_DL_HANDLE: Int](/documentation/security/cssmerr_dl_invalid_dl_handle)
- [var CSSMERR_DL_INVALID_FIELD_NAME: Int](/documentation/security/cssmerr_dl_invalid_field_name)
- [var CSSMERR_DL_INVALID_INDEX_INFO: Int](/documentation/security/cssmerr_dl_invalid_index_info)
- [var CSSMERR_DL_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_dl_invalid_input_pointer)
- [var CSSMERR_DL_INVALID_MODIFY_MODE: Int](/documentation/security/cssmerr_dl_invalid_modify_mode)
- [var CSSMERR_DL_INVALID_NETWORK_ADDR: Int](/documentation/security/cssmerr_dl_invalid_network_addr)
- [var CSSMERR_DL_INVALID_NEW_ACL_ENTRY: Int](/documentation/security/cssmerr_dl_invalid_new_acl_entry)
- [var CSSMERR_DL_INVALID_NEW_ACL_OWNER: Int](/documentation/security/cssmerr_dl_invalid_new_acl_owner)
- [var CSSMERR_DL_INVALID_NEW_OWNER: Int](/documentation/security/cssmerr_dl_invalid_new_owner)
- [var CSSMERR_DL_INVALID_OPEN_PARAMETERS: Int](/documentation/security/cssmerr_dl_invalid_open_parameters)
- [var CSSMERR_DL_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_dl_invalid_output_pointer)
- [var CSSMERR_DL_INVALID_PARSING_MODULE: Int](/documentation/security/cssmerr_dl_invalid_parsing_module)
- [var CSSMERR_DL_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssmerr_dl_invalid_passthrough_id)
- [var CSSMERR_DL_INVALID_POINTER: Int](/documentation/security/cssmerr_dl_invalid_pointer)
- [var CSSMERR_DL_INVALID_QUERY: Int](/documentation/security/cssmerr_dl_invalid_query)
- [var CSSMERR_DL_INVALID_RECORDTYPE: Int](/documentation/security/cssmerr_dl_invalid_recordtype)
- [var CSSMERR_DL_INVALID_RECORD_INDEX: Int](/documentation/security/cssmerr_dl_invalid_record_index)
- [var CSSMERR_DL_INVALID_RECORD_UID: Int](/documentation/security/cssmerr_dl_invalid_record_uid)
- [var CSSMERR_DL_INVALID_RESULTS_HANDLE: Int](/documentation/security/cssmerr_dl_invalid_results_handle)
- [var CSSMERR_DL_INVALID_SAMPLE_VALUE: Int](/documentation/security/cssmerr_dl_invalid_sample_value)
- [var CSSMERR_DL_INVALID_SELECTION_TAG: Int](/documentation/security/cssmerr_dl_invalid_selection_tag)
- [var CSSMERR_DL_INVALID_UNIQUE_INDEX_DATA: Int](/documentation/security/cssmerr_dl_invalid_unique_index_data)
- [var CSSMERR_DL_INVALID_VALUE: Int](/documentation/security/cssmerr_dl_invalid_value)
- [var CSSMERR_DL_IN_DARK_WAKE: Int](/documentation/security/cssmerr_dl_in_dark_wake)
- [var CSSMERR_DL_MDS_ERROR: Int](/documentation/security/cssmerr_dl_mds_error)
- [var CSSMERR_DL_MEMORY_ERROR: Int](/documentation/security/cssmerr_dl_memory_error)
- [var CSSMERR_DL_MISSING_VALUE: Int](/documentation/security/cssmerr_dl_missing_value)
- [var CSSMERR_DL_MULTIPLE_VALUES_UNSUPPORTED: Int](/documentation/security/cssmerr_dl_multiple_values_unsupported)
- [var CSSMERR_DL_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_dl_no_user_interaction)
- [var CSSMERR_DL_OBJECT_ACL_NOT_SUPPORTED: Int](/documentation/security/cssmerr_dl_object_acl_not_supported)
- [var CSSMERR_DL_OBJECT_ACL_REQUIRED: Int](/documentation/security/cssmerr_dl_object_acl_required)
- [var CSSMERR_DL_OBJECT_MANIP_AUTH_DENIED: Int](/documentation/security/cssmerr_dl_object_manip_auth_denied)
- [var CSSMERR_DL_OBJECT_USE_AUTH_DENIED: Int](/documentation/security/cssmerr_dl_object_use_auth_denied)
- [var CSSMERR_DL_OPERATION_AUTH_DENIED: Int](/documentation/security/cssmerr_dl_operation_auth_denied)
- [var CSSMERR_DL_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_dl_os_access_denied)
- [var CSSMERR_DL_RECORD_MODIFIED: Int](/documentation/security/cssmerr_dl_record_modified)
- [var CSSMERR_DL_RECORD_NOT_FOUND: Int](/documentation/security/cssmerr_dl_record_not_found)
- [var CSSMERR_DL_SAMPLE_VALUE_NOT_SUPPORTED: Int](/documentation/security/cssmerr_dl_sample_value_not_supported)
- [var CSSMERR_DL_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_dl_self_check_failed)
- [var CSSMERR_DL_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_dl_service_not_available)
- [var CSSMERR_DL_STALE_UNIQUE_RECORD: Int](/documentation/security/cssmerr_dl_stale_unique_record)
- [var CSSMERR_DL_UNSUPPORTED_FIELD_FORMAT: Int](/documentation/security/cssmerr_dl_unsupported_field_format)
- [var CSSMERR_DL_UNSUPPORTED_INDEX_INFO: Int](/documentation/security/cssmerr_dl_unsupported_index_info)
- [var CSSMERR_DL_UNSUPPORTED_LOCALITY: Int](/documentation/security/cssmerr_dl_unsupported_locality)
- [var CSSMERR_DL_UNSUPPORTED_NUM_ATTRIBUTES: Int](/documentation/security/cssmerr_dl_unsupported_num_attributes)
- [var CSSMERR_DL_UNSUPPORTED_NUM_INDEXES: Int](/documentation/security/cssmerr_dl_unsupported_num_indexes)
- [var CSSMERR_DL_UNSUPPORTED_NUM_RECORDTYPES: Int](/documentation/security/cssmerr_dl_unsupported_num_recordtypes)
- [var CSSMERR_DL_UNSUPPORTED_NUM_SELECTION_PREDS: Int](/documentation/security/cssmerr_dl_unsupported_num_selection_preds)
- [var CSSMERR_DL_UNSUPPORTED_OPERATOR: Int](/documentation/security/cssmerr_dl_unsupported_operator)
- [var CSSMERR_DL_UNSUPPORTED_QUERY: Int](/documentation/security/cssmerr_dl_unsupported_query)
- [var CSSMERR_DL_UNSUPPORTED_QUERY_LIMITS: Int](/documentation/security/cssmerr_dl_unsupported_query_limits)
- [var CSSMERR_DL_UNSUPPORTED_RECORDTYPE: Int](/documentation/security/cssmerr_dl_unsupported_recordtype)
- [var CSSMERR_DL_USER_CANCELED: Int](/documentation/security/cssmerr_dl_user_canceled)
- [var CSSMERR_TP_AUTHENTICATION_FAILED: Int](/documentation/security/cssmerr_tp_authentication_failed)
- [var CSSMERR_TP_CERTGROUP_INCOMPLETE: Int](/documentation/security/cssmerr_tp_certgroup_incomplete)
- [var CSSMERR_TP_CERTIFICATE_CANT_OPERATE: Int](/documentation/security/cssmerr_tp_certificate_cant_operate)
- [var CSSMERR_TP_CERT_EXPIRED: Int](/documentation/security/cssmerr_tp_cert_expired)
- [var CSSMERR_TP_CERT_NOT_VALID_YET: Int](/documentation/security/cssmerr_tp_cert_not_valid_yet)
- [var CSSMERR_TP_CERT_REVOKED: Int](/documentation/security/cssmerr_tp_cert_revoked)
- [var CSSMERR_TP_CERT_SUSPENDED: Int](/documentation/security/cssmerr_tp_cert_suspended)
- [var CSSMERR_TP_CRL_ALREADY_SIGNED: Int](/documentation/security/cssmerr_tp_crl_already_signed)
- [var CSSMERR_TP_DEVICE_FAILED: Int](/documentation/security/cssmerr_tp_device_failed)
- [var CSSMERR_TP_DEVICE_RESET: Int](/documentation/security/cssmerr_tp_device_reset)
- [var CSSMERR_TP_FUNCTION_FAILED: Int](/documentation/security/cssmerr_tp_function_failed)
- [var CSSMERR_TP_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssmerr_tp_function_not_implemented)
- [var CSSMERR_TP_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssmerr_tp_insufficient_client_identification)
- [var CSSMERR_TP_INSUFFICIENT_CREDENTIALS: Int](/documentation/security/cssmerr_tp_insufficient_credentials)
- [var CSSMERR_TP_INTERNAL_ERROR: Int](/documentation/security/cssmerr_tp_internal_error)
- [var CSSMERR_TP_INVALID_ACTION: Int](/documentation/security/cssmerr_tp_invalid_action)
- [var CSSMERR_TP_INVALID_ACTION_DATA: Int](/documentation/security/cssmerr_tp_invalid_action_data)
- [var CSSMERR_TP_INVALID_ANCHOR_CERT: Int](/documentation/security/cssmerr_tp_invalid_anchor_cert)
- [var CSSMERR_TP_INVALID_AUTHORITY: Int](/documentation/security/cssmerr_tp_invalid_authority)
- [var CSSMERR_TP_INVALID_CALLBACK: Int](/documentation/security/cssmerr_tp_invalid_callback)
- [var CSSMERR_TP_INVALID_CALLERAUTH_CONTEXT_POINTER: Int](/documentation/security/cssmerr_tp_invalid_callerauth_context_pointer)
- [var CSSMERR_TP_INVALID_CERTGROUP: Int](/documentation/security/cssmerr_tp_invalid_certgroup)
- [var CSSMERR_TP_INVALID_CERTGROUP_POINTER: Int](/documentation/security/cssmerr_tp_invalid_certgroup_pointer)
- [var CSSMERR_TP_INVALID_CERTIFICATE: Int](/documentation/security/cssmerr_tp_invalid_certificate)
- [var CSSMERR_TP_INVALID_CERT_AUTHORITY: Int](/documentation/security/cssmerr_tp_invalid_cert_authority)
- [var CSSMERR_TP_INVALID_CERT_POINTER: Int](/documentation/security/cssmerr_tp_invalid_cert_pointer)
- [var CSSMERR_TP_INVALID_CL_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_cl_handle)
- [var CSSMERR_TP_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_context_handle)
- [var CSSMERR_TP_INVALID_CRL: Int](/documentation/security/cssmerr_tp_invalid_crl)
- [var CSSMERR_TP_INVALID_CRLGROUP: Int](/documentation/security/cssmerr_tp_invalid_crlgroup)
- [var CSSMERR_TP_INVALID_CRLGROUP_POINTER: Int](/documentation/security/cssmerr_tp_invalid_crlgroup_pointer)
- [var CSSMERR_TP_INVALID_CRL_AUTHORITY: Int](/documentation/security/cssmerr_tp_invalid_crl_authority)
- [var CSSMERR_TP_INVALID_CRL_ENCODING: Int](/documentation/security/cssmerr_tp_invalid_crl_encoding)
- [var CSSMERR_TP_INVALID_CRL_POINTER: Int](/documentation/security/cssmerr_tp_invalid_crl_pointer)
- [var CSSMERR_TP_INVALID_CRL_TYPE: Int](/documentation/security/cssmerr_tp_invalid_crl_type)
- [var CSSMERR_TP_INVALID_CSP_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_csp_handle)
- [var CSSMERR_TP_INVALID_DATA: Int](/documentation/security/cssmerr_tp_invalid_data)
- [var CSSMERR_TP_INVALID_DB_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_db_handle)
- [var CSSMERR_TP_INVALID_DB_LIST: Int](/documentation/security/cssmerr_tp_invalid_db_list)
- [var CSSMERR_TP_INVALID_DB_LIST_POINTER: Int](/documentation/security/cssmerr_tp_invalid_db_list_pointer)
- [var CSSMERR_TP_INVALID_DL_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_dl_handle)
- [var CSSMERR_TP_INVALID_FIELD_POINTER: Int](/documentation/security/cssmerr_tp_invalid_field_pointer)
- [var CSSMERR_TP_INVALID_FORM_TYPE: Int](/documentation/security/cssmerr_tp_invalid_form_type)
- [var CSSMERR_TP_INVALID_ID: Int](/documentation/security/cssmerr_tp_invalid_id)
- [var CSSMERR_TP_INVALID_IDENTIFIER: Int](/documentation/security/cssmerr_tp_invalid_identifier)
- [var CSSMERR_TP_INVALID_IDENTIFIER_POINTER: Int](/documentation/security/cssmerr_tp_invalid_identifier_pointer)
- [var CSSMERR_TP_INVALID_INDEX: Int](/documentation/security/cssmerr_tp_invalid_index)
- [var CSSMERR_TP_INVALID_INPUT_POINTER: Int](/documentation/security/cssmerr_tp_invalid_input_pointer)
- [var CSSMERR_TP_INVALID_KEYCACHE_HANDLE: Int](/documentation/security/cssmerr_tp_invalid_keycache_handle)
- [var CSSMERR_TP_INVALID_NAME: Int](/documentation/security/cssmerr_tp_invalid_name)
- [var CSSMERR_TP_INVALID_NETWORK_ADDR: Int](/documentation/security/cssmerr_tp_invalid_network_addr)
- [var CSSMERR_TP_INVALID_NUMBER_OF_FIELDS: Int](/documentation/security/cssmerr_tp_invalid_number_of_fields)
- [var CSSMERR_TP_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssmerr_tp_invalid_output_pointer)
- [var CSSMERR_TP_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssmerr_tp_invalid_passthrough_id)
- [var CSSMERR_TP_INVALID_POINTER: Int](/documentation/security/cssmerr_tp_invalid_pointer)
- [var CSSMERR_TP_INVALID_POLICY_IDENTIFIERS: Int](/documentation/security/cssmerr_tp_invalid_policy_identifiers)
- [var CSSMERR_TP_INVALID_REASON: Int](/documentation/security/cssmerr_tp_invalid_reason)
- [var CSSMERR_TP_INVALID_REQUEST_INPUTS: Int](/documentation/security/cssmerr_tp_invalid_request_inputs)
- [var CSSMERR_TP_INVALID_RESPONSE_VECTOR: Int](/documentation/security/cssmerr_tp_invalid_response_vector)
- [var CSSMERR_TP_INVALID_SIGNATURE: Int](/documentation/security/cssmerr_tp_invalid_signature)
- [var CSSMERR_TP_INVALID_STOP_ON_POLICY: Int](/documentation/security/cssmerr_tp_invalid_stop_on_policy)
- [var CSSMERR_TP_INVALID_TIMESTRING: Int](/documentation/security/cssmerr_tp_invalid_timestring)
- [var CSSMERR_TP_INVALID_TUPLE: Int](/documentation/security/cssmerr_tp_invalid_tuple)
- [var CSSMERR_TP_INVALID_TUPLEGROUP: Int](/documentation/security/cssmerr_tp_invalid_tuplegroup)
- [var CSSMERR_TP_INVALID_TUPLEGROUP_POINTER: Int](/documentation/security/cssmerr_tp_invalid_tuplegroup_pointer)
- [var CSSMERR_TP_IN_DARK_WAKE: Int](/documentation/security/cssmerr_tp_in_dark_wake)
- [var CSSMERR_TP_MDS_ERROR: Int](/documentation/security/cssmerr_tp_mds_error)
- [var CSSMERR_TP_MEMORY_ERROR: Int](/documentation/security/cssmerr_tp_memory_error)
- [var CSSMERR_TP_NOT_SIGNER: Int](/documentation/security/cssmerr_tp_not_signer)
- [var CSSMERR_TP_NOT_TRUSTED: Int](/documentation/security/cssmerr_tp_not_trusted)
- [var CSSMERR_TP_NO_DEFAULT_AUTHORITY: Int](/documentation/security/cssmerr_tp_no_default_authority)
- [var CSSMERR_TP_NO_USER_INTERACTION: Int](/documentation/security/cssmerr_tp_no_user_interaction)
- [var CSSMERR_TP_OS_ACCESS_DENIED: Int](/documentation/security/cssmerr_tp_os_access_denied)
- [var CSSMERR_TP_REJECTED_FORM: Int](/documentation/security/cssmerr_tp_rejected_form)
- [var CSSMERR_TP_REQUEST_LOST: Int](/documentation/security/cssmerr_tp_request_lost)
- [var CSSMERR_TP_REQUEST_REJECTED: Int](/documentation/security/cssmerr_tp_request_rejected)
- [var CSSMERR_TP_SELF_CHECK_FAILED: Int](/documentation/security/cssmerr_tp_self_check_failed)
- [var CSSMERR_TP_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssmerr_tp_service_not_available)
- [var CSSMERR_TP_UNKNOWN_FORMAT: Int](/documentation/security/cssmerr_tp_unknown_format)
- [var CSSMERR_TP_UNKNOWN_TAG: Int](/documentation/security/cssmerr_tp_unknown_tag)
- [var CSSMERR_TP_UNSUPPORTED_ADDR_TYPE: Int](/documentation/security/cssmerr_tp_unsupported_addr_type)
- [var CSSMERR_TP_UNSUPPORTED_SERVICE: Int](/documentation/security/cssmerr_tp_unsupported_service)
- [var CSSMERR_TP_USER_CANCELED: Int](/documentation/security/cssmerr_tp_user_canceled)
- [var CSSMERR_TP_VERIFICATION_FAILURE: Int](/documentation/security/cssmerr_tp_verification_failure)
- [var CSSMERR_TP_VERIFY_ACTION_FAILED: Int](/documentation/security/cssmerr_tp_verify_action_failed)
- [var CSSM_ACL_AUTHORIZATION_ANY: Int](/documentation/security/cssm_acl_authorization_any)
- [var CSSM_ACL_AUTHORIZATION_CHANGE_ACL: Int](/documentation/security/cssm_acl_authorization_change_acl)
- [var CSSM_ACL_AUTHORIZATION_CHANGE_OWNER: Int](/documentation/security/cssm_acl_authorization_change_owner)
- [var CSSM_ACL_AUTHORIZATION_DBS_CREATE: Int](/documentation/security/cssm_acl_authorization_dbs_create)
- [var CSSM_ACL_AUTHORIZATION_DBS_DELETE: Int](/documentation/security/cssm_acl_authorization_dbs_delete)
- [var CSSM_ACL_AUTHORIZATION_DB_DELETE: Int](/documentation/security/cssm_acl_authorization_db_delete)
- [var CSSM_ACL_AUTHORIZATION_DB_INSERT: Int](/documentation/security/cssm_acl_authorization_db_insert)
- [var CSSM_ACL_AUTHORIZATION_DB_MODIFY: Int](/documentation/security/cssm_acl_authorization_db_modify)
- [var CSSM_ACL_AUTHORIZATION_DB_READ: Int](/documentation/security/cssm_acl_authorization_db_read)
- [var CSSM_ACL_AUTHORIZATION_DECRYPT: Int](/documentation/security/cssm_acl_authorization_decrypt)
- [var CSSM_ACL_AUTHORIZATION_DELETE: Int](/documentation/security/cssm_acl_authorization_delete)
- [var CSSM_ACL_AUTHORIZATION_DERIVE: Int](/documentation/security/cssm_acl_authorization_derive)
- [var CSSM_ACL_AUTHORIZATION_ENCRYPT: Int](/documentation/security/cssm_acl_authorization_encrypt)
- [var CSSM_ACL_AUTHORIZATION_EXPORT_CLEAR: Int](/documentation/security/cssm_acl_authorization_export_clear)
- [var CSSM_ACL_AUTHORIZATION_EXPORT_WRAPPED: Int](/documentation/security/cssm_acl_authorization_export_wrapped)
- [var CSSM_ACL_AUTHORIZATION_GENKEY: Int](/documentation/security/cssm_acl_authorization_genkey)
- [var CSSM_ACL_AUTHORIZATION_IMPORT_CLEAR: Int](/documentation/security/cssm_acl_authorization_import_clear)
- [var CSSM_ACL_AUTHORIZATION_IMPORT_WRAPPED: Int](/documentation/security/cssm_acl_authorization_import_wrapped)
- [var CSSM_ACL_AUTHORIZATION_INTEGRITY: Int](/documentation/security/cssm_acl_authorization_integrity)
- [var CSSM_ACL_AUTHORIZATION_LOGIN: Int](/documentation/security/cssm_acl_authorization_login)
- [var CSSM_ACL_AUTHORIZATION_MAC: Int](/documentation/security/cssm_acl_authorization_mac)
- [var CSSM_ACL_AUTHORIZATION_PARTITION_ID: Int](/documentation/security/cssm_acl_authorization_partition_id)
- [var CSSM_ACL_AUTHORIZATION_PREAUTH_BASE: Int](/documentation/security/cssm_acl_authorization_preauth_base)
- [var CSSM_ACL_AUTHORIZATION_PREAUTH_END: Int](/documentation/security/cssm_acl_authorization_preauth_end)
- [var CSSM_ACL_AUTHORIZATION_SIGN: Int](/documentation/security/cssm_acl_authorization_sign)
- [var CSSM_ACL_AUTHORIZATION_TAG_VENDOR_DEFINED_START: Int](/documentation/security/cssm_acl_authorization_tag_vendor_defined_start)
- [var CSSM_ACL_CODE_SIGNATURE_INVALID: Int](/documentation/security/cssm_acl_code_signature_invalid)
- [var CSSM_ACL_CODE_SIGNATURE_OSX: Int](/documentation/security/cssm_acl_code_signature_osx)
- [var CSSM_ACL_EDIT_MODE_ADD: Int](/documentation/security/cssm_acl_edit_mode_add)
- [var CSSM_ACL_EDIT_MODE_DELETE: Int](/documentation/security/cssm_acl_edit_mode_delete)
- [var CSSM_ACL_EDIT_MODE_REPLACE: Int](/documentation/security/cssm_acl_edit_mode_replace)
- [var CSSM_ACL_KEYCHAIN_PROMPT_CURRENT_VERSION: Int](/documentation/security/cssm_acl_keychain_prompt_current_version)
- [var CSSM_ACL_KEYCHAIN_PROMPT_INVALID: Int](/documentation/security/cssm_acl_keychain_prompt_invalid)
- [var CSSM_ACL_KEYCHAIN_PROMPT_INVALID_ACT: Int](/documentation/security/cssm_acl_keychain_prompt_invalid_act)
- [var CSSM_ACL_KEYCHAIN_PROMPT_REQUIRE_PASSPHRASE: Int](/documentation/security/cssm_acl_keychain_prompt_require_passphrase)
- [var CSSM_ACL_KEYCHAIN_PROMPT_UNSIGNED: Int](/documentation/security/cssm_acl_keychain_prompt_unsigned)
- [var CSSM_ACL_KEYCHAIN_PROMPT_UNSIGNED_ACT: Int](/documentation/security/cssm_acl_keychain_prompt_unsigned_act)
- [var CSSM_ACL_MATCH_BITS: Int](/documentation/security/cssm_acl_match_bits)
- [var CSSM_ACL_MATCH_GID: Int](/documentation/security/cssm_acl_match_gid)
- [var CSSM_ACL_MATCH_HONOR_ROOT: Int](/documentation/security/cssm_acl_match_honor_root)
- [var CSSM_ACL_MATCH_UID: Int](/documentation/security/cssm_acl_match_uid)
- [var CSSM_ACL_PREAUTH_TRACKING_AUTHORIZED: UInt32](/documentation/security/cssm_acl_preauth_tracking_authorized)
- [var CSSM_ACL_PREAUTH_TRACKING_BLOCKED: UInt32](/documentation/security/cssm_acl_preauth_tracking_blocked)
- [var CSSM_ACL_PREAUTH_TRACKING_COUNT_MASK: UInt32](/documentation/security/cssm_acl_preauth_tracking_count_mask)
- [var CSSM_ACL_PREAUTH_TRACKING_UNKNOWN: UInt32](/documentation/security/cssm_acl_preauth_tracking_unknown)
- [var CSSM_ACL_PROCESS_SELECTOR_CURRENT_VERSION: Int](/documentation/security/cssm_acl_process_selector_current_version)
- [var CSSM_ACL_SUBJECT_TYPE_ANY: Int](/documentation/security/cssm_acl_subject_type_any)
- [var CSSM_ACL_SUBJECT_TYPE_ASYMMETRIC_KEY: Int](/documentation/security/cssm_acl_subject_type_asymmetric_key)
- [var CSSM_ACL_SUBJECT_TYPE_BIOMETRIC: Int](/documentation/security/cssm_acl_subject_type_biometric)
- [var CSSM_ACL_SUBJECT_TYPE_CODE_SIGNATURE: Int](/documentation/security/cssm_acl_subject_type_code_signature)
- [var CSSM_ACL_SUBJECT_TYPE_COMMENT: Int](/documentation/security/cssm_acl_subject_type_comment)
- [var CSSM_ACL_SUBJECT_TYPE_EXT_PAM_NAME: Int](/documentation/security/cssm_acl_subject_type_ext_pam_name)
- [var CSSM_ACL_SUBJECT_TYPE_HASHED_SUBJECT: Int](/documentation/security/cssm_acl_subject_type_hashed_subject)
- [var CSSM_ACL_SUBJECT_TYPE_KEYCHAIN_PROMPT: Int](/documentation/security/cssm_acl_subject_type_keychain_prompt)
- [var CSSM_ACL_SUBJECT_TYPE_LOGIN_NAME: Int](/documentation/security/cssm_acl_subject_type_login_name)
- [var CSSM_ACL_SUBJECT_TYPE_PARTITION: Int](/documentation/security/cssm_acl_subject_type_partition)
- [var CSSM_ACL_SUBJECT_TYPE_PASSWORD: Int](/documentation/security/cssm_acl_subject_type_password)
- [var CSSM_ACL_SUBJECT_TYPE_PREAUTH: Int](/documentation/security/cssm_acl_subject_type_preauth)
- [var CSSM_ACL_SUBJECT_TYPE_PREAUTH_SOURCE: Int](/documentation/security/cssm_acl_subject_type_preauth_source)
- [var CSSM_ACL_SUBJECT_TYPE_PROCESS: Int](/documentation/security/cssm_acl_subject_type_process)
- [var CSSM_ACL_SUBJECT_TYPE_PROMPTED_BIOMETRIC: Int](/documentation/security/cssm_acl_subject_type_prompted_biometric)
- [var CSSM_ACL_SUBJECT_TYPE_PROMPTED_PASSWORD: Int](/documentation/security/cssm_acl_subject_type_prompted_password)
- [var CSSM_ACL_SUBJECT_TYPE_PROTECTED_BIOMETRIC: Int](/documentation/security/cssm_acl_subject_type_protected_biometric)
- [var CSSM_ACL_SUBJECT_TYPE_PROTECTED_PASSWORD: Int](/documentation/security/cssm_acl_subject_type_protected_password)
- [var CSSM_ACL_SUBJECT_TYPE_PUBLIC_KEY: Int](/documentation/security/cssm_acl_subject_type_public_key)
- [var CSSM_ACL_SUBJECT_TYPE_SYMMETRIC_KEY: Int](/documentation/security/cssm_acl_subject_type_symmetric_key)
- [var CSSM_ACL_SUBJECT_TYPE_THRESHOLD: Int](/documentation/security/cssm_acl_subject_type_threshold)
- [var CSSM_AC_BASE_AC_ERROR: Int](/documentation/security/cssm_ac_base_ac_error)
- [var CSSM_AC_BASE_ERROR: Int](/documentation/security/cssm_ac_base_error)
- [var CSSM_AC_PRIVATE_ERROR: Int](/documentation/security/cssm_ac_private_error)
- [var CSSM_ADDR_CUSTOM: Int](/documentation/security/cssm_addr_custom)
- [var CSSM_ADDR_NAME: Int](/documentation/security/cssm_addr_name)
- [var CSSM_ADDR_NONE: Int](/documentation/security/cssm_addr_none)
- [var CSSM_ADDR_SOCKADDR: Int](/documentation/security/cssm_addr_sockaddr)
- [var CSSM_ADDR_URL: Int](/documentation/security/cssm_addr_url)
- [var CSSM_ALGCLASS_ASYMMETRIC: Int](/documentation/security/cssm_algclass_asymmetric)
- [var CSSM_ALGCLASS_CUSTOM: Int](/documentation/security/cssm_algclass_custom)
- [var CSSM_ALGCLASS_DERIVEKEY: Int](/documentation/security/cssm_algclass_derivekey)
- [var CSSM_ALGCLASS_DIGEST: Int](/documentation/security/cssm_algclass_digest)
- [var CSSM_ALGCLASS_KEYGEN: Int](/documentation/security/cssm_algclass_keygen)
- [var CSSM_ALGCLASS_MAC: Int](/documentation/security/cssm_algclass_mac)
- [var CSSM_ALGCLASS_NONE: Int](/documentation/security/cssm_algclass_none)
- [var CSSM_ALGCLASS_RANDOMGEN: Int](/documentation/security/cssm_algclass_randomgen)
- [var CSSM_ALGCLASS_SIGNATURE: Int](/documentation/security/cssm_algclass_signature)
- [var CSSM_ALGCLASS_SYMMETRIC: Int](/documentation/security/cssm_algclass_symmetric)
- [var CSSM_ALGCLASS_UNIQUEGEN: Int](/documentation/security/cssm_algclass_uniquegen)
- [var CSSM_ALGID_3DES: UInt32](/documentation/security/cssm_algid_3des)
- [var CSSM_ALGID_3DES_1KEY: UInt32](/documentation/security/cssm_algid_3des_1key)
- [var CSSM_ALGID_3DES_1KEY_EEE: UInt32](/documentation/security/cssm_algid_3des_1key_eee)
- [var CSSM_ALGID_3DES_2KEY: UInt32](/documentation/security/cssm_algid_3des_2key)
- [var CSSM_ALGID_3DES_2KEY_EDE: UInt32](/documentation/security/cssm_algid_3des_2key_ede)
- [var CSSM_ALGID_3DES_2KEY_EEE: UInt32](/documentation/security/cssm_algid_3des_2key_eee)
- [var CSSM_ALGID_3DES_3KEY: UInt32](/documentation/security/cssm_algid_3des_3key)
- [var CSSM_ALGID_3DES_3KEY_EDE: UInt32](/documentation/security/cssm_algid_3des_3key_ede)
- [var CSSM_ALGID_3DES_3KEY_EEE: UInt32](/documentation/security/cssm_algid_3des_3key_eee)
- [var CSSM_ALGID_AES: UInt32](/documentation/security/cssm_algid_aes)
- [var CSSM_ALGID_APPLE_YARROW: UInt32](/documentation/security/cssm_algid_apple_yarrow)
- [var CSSM_ALGID_ASC: UInt32](/documentation/security/cssm_algid_asc)
- [var CSSM_ALGID_BATON: UInt32](/documentation/security/cssm_algid_baton)
- [var CSSM_ALGID_BLOWFISH: UInt32](/documentation/security/cssm_algid_blowfish)
- [var CSSM_ALGID_CAST: UInt32](/documentation/security/cssm_algid_cast)
- [var CSSM_ALGID_CAST3: UInt32](/documentation/security/cssm_algid_cast3)
- [var CSSM_ALGID_CAST5: UInt32](/documentation/security/cssm_algid_cast5)
- [var CSSM_ALGID_CDMF: UInt32](/documentation/security/cssm_algid_cdmf)
- [var CSSM_ALGID_CRAB: UInt32](/documentation/security/cssm_algid_crab)
- [var CSSM_ALGID_CUSTOM: UInt32](/documentation/security/cssm_algid_custom)
- [var CSSM_ALGID_ConcatBaseAndData: UInt32](/documentation/security/cssm_algid_concatbaseanddata)
- [var CSSM_ALGID_ConcatBaseAndKey: UInt32](/documentation/security/cssm_algid_concatbaseandkey)
- [var CSSM_ALGID_ConcatDataAndBase: UInt32](/documentation/security/cssm_algid_concatdataandbase)
- [var CSSM_ALGID_ConcatKeyAndBase: UInt32](/documentation/security/cssm_algid_concatkeyandbase)
- [var CSSM_ALGID_DES: UInt32](/documentation/security/cssm_algid_des)
- [var CSSM_ALGID_DESRandom: UInt32](/documentation/security/cssm_algid_desrandom)
- [var CSSM_ALGID_DESX: UInt32](/documentation/security/cssm_algid_desx)
- [var CSSM_ALGID_DH: UInt32](/documentation/security/cssm_algid_dh)
- [var CSSM_ALGID_DSA: UInt32](/documentation/security/cssm_algid_dsa)
- [var CSSM_ALGID_DSA_BSAFE: UInt32](/documentation/security/cssm_algid_dsa_bsafe)
- [var CSSM_ALGID_ECAES: UInt32](/documentation/security/cssm_algid_ecaes)
- [var CSSM_ALGID_ECC: UInt32](/documentation/security/cssm_algid_ecc)
- [var CSSM_ALGID_ECDH: UInt32](/documentation/security/cssm_algid_ecdh)
- [var CSSM_ALGID_ECDH_X963_KDF: UInt32](/documentation/security/cssm_algid_ecdh_x963_kdf)
- [var CSSM_ALGID_ECDSA: UInt32](/documentation/security/cssm_algid_ecdsa)
- [var CSSM_ALGID_ECDSA_SPECIFIED: UInt32](/documentation/security/cssm_algid_ecdsa_specified)
- [var CSSM_ALGID_ECES: UInt32](/documentation/security/cssm_algid_eces)
- [var CSSM_ALGID_ECMQV: UInt32](/documentation/security/cssm_algid_ecmqv)
- [var CSSM_ALGID_ECNRA: UInt32](/documentation/security/cssm_algid_ecnra)
- [var CSSM_ALGID_ENTROPY_DEFAULT: UInt32](/documentation/security/cssm_algid_entropy_default)
- [var CSSM_ALGID_ElGamal: UInt32](/documentation/security/cssm_algid_elgamal)
- [var CSSM_ALGID_ExtractFromKey: UInt32](/documentation/security/cssm_algid_extractfromkey)
- [var CSSM_ALGID_FASTHASH: UInt32](/documentation/security/cssm_algid_fasthash)
- [var CSSM_ALGID_FEAL: UInt32](/documentation/security/cssm_algid_feal)
- [var CSSM_ALGID_FEE: UInt32](/documentation/security/cssm_algid_fee)
- [var CSSM_ALGID_FEED: UInt32](/documentation/security/cssm_algid_feed)
- [var CSSM_ALGID_FEEDEXP: UInt32](/documentation/security/cssm_algid_feedexp)
- [var CSSM_ALGID_FEE_MD5: UInt32](/documentation/security/cssm_algid_fee_md5)
- [var CSSM_ALGID_FEE_SHA1: UInt32](/documentation/security/cssm_algid_fee_sha1)
- [var CSSM_ALGID_FIPS186Random: UInt32](/documentation/security/cssm_algid_fips186random)
- [var CSSM_ALGID_FortezzaTimestamp: UInt32](/documentation/security/cssm_algid_fortezzatimestamp)
- [var CSSM_ALGID_GOST: UInt32](/documentation/security/cssm_algid_gost)
- [var CSSM_ALGID_GenericSecret: UInt32](/documentation/security/cssm_algid_genericsecret)
- [var CSSM_ALGID_HAVAL: UInt32](/documentation/security/cssm_algid_haval)
- [var CSSM_ALGID_HAVAL3: UInt32](/documentation/security/cssm_algid_haval3)
- [var CSSM_ALGID_HAVAL4: UInt32](/documentation/security/cssm_algid_haval4)
- [var CSSM_ALGID_HAVAL5: UInt32](/documentation/security/cssm_algid_haval5)
- [var CSSM_ALGID_IBCHASH: UInt32](/documentation/security/cssm_algid_ibchash)
- [var CSSM_ALGID_IDEA: UInt32](/documentation/security/cssm_algid_idea)
- [var CSSM_ALGID_IntelPlatformRandom: UInt32](/documentation/security/cssm_algid_intelplatformrandom)
- [var CSSM_ALGID_JUNIPER: UInt32](/documentation/security/cssm_algid_juniper)
- [var CSSM_ALGID_KEA: UInt32](/documentation/security/cssm_algid_kea)
- [var CSSM_ALGID_KEYCHAIN_KEY: UInt32](/documentation/security/cssm_algid_keychain_key)
- [var CSSM_ALGID_KHAFRE: UInt32](/documentation/security/cssm_algid_khafre)
- [var CSSM_ALGID_KHUFU: UInt32](/documentation/security/cssm_algid_khufu)
- [var CSSM_ALGID_LAST: UInt32](/documentation/security/cssm_algid_last)
- [var CSSM_ALGID_LOKI: UInt32](/documentation/security/cssm_algid_loki)
- [var CSSM_ALGID_LUCIFER: UInt32](/documentation/security/cssm_algid_lucifer)
- [var CSSM_ALGID_MADRYGA: UInt32](/documentation/security/cssm_algid_madryga)
- [var CSSM_ALGID_MAYFLY: UInt32](/documentation/security/cssm_algid_mayfly)
- [var CSSM_ALGID_MD2: UInt32](/documentation/security/cssm_algid_md2)
- [var CSSM_ALGID_MD2Random: UInt32](/documentation/security/cssm_algid_md2random)
- [var CSSM_ALGID_MD2WithRSA: UInt32](/documentation/security/cssm_algid_md2withrsa)
- [var CSSM_ALGID_MD4: UInt32](/documentation/security/cssm_algid_md4)
- [var CSSM_ALGID_MD5: UInt32](/documentation/security/cssm_algid_md5)
- [var CSSM_ALGID_MD5HMAC: UInt32](/documentation/security/cssm_algid_md5hmac)
- [var CSSM_ALGID_MD5Random: UInt32](/documentation/security/cssm_algid_md5random)
- [var CSSM_ALGID_MD5WithRSA: UInt32](/documentation/security/cssm_algid_md5withrsa)
- [var CSSM_ALGID_MMB: UInt32](/documentation/security/cssm_algid_mmb)
- [var CSSM_ALGID_MQV: UInt32](/documentation/security/cssm_algid_mqv)
- [var CSSM_ALGID_NHASH: UInt32](/documentation/security/cssm_algid_nhash)
- [var CSSM_ALGID_NONE: UInt32](/documentation/security/cssm_algid_none)
- [var CSSM_ALGID_NRA: UInt32](/documentation/security/cssm_algid_nra)
- [var CSSM_ALGID_OPENSSH1: UInt32](/documentation/security/cssm_algid_openssh1)
- [var CSSM_ALGID_PBE_OPENSSL_MD5: UInt32](/documentation/security/cssm_algid_pbe_openssl_md5)
- [var CSSM_ALGID_PH: UInt32](/documentation/security/cssm_algid_ph)
- [var CSSM_ALGID_PKCS12_PBE_ENCR: UInt32](/documentation/security/cssm_algid_pkcs12_pbe_encr)
- [var CSSM_ALGID_PKCS12_PBE_MAC: UInt32](/documentation/security/cssm_algid_pkcs12_pbe_mac)
- [var CSSM_ALGID_PKCS12_SHA1_PBE: UInt32](/documentation/security/cssm_algid_pkcs12_sha1_pbe)
- [var CSSM_ALGID_PKCS5_PBKDF1_MD2: UInt32](/documentation/security/cssm_algid_pkcs5_pbkdf1_md2)
- [var CSSM_ALGID_PKCS5_PBKDF1_MD5: UInt32](/documentation/security/cssm_algid_pkcs5_pbkdf1_md5)
- [var CSSM_ALGID_PKCS5_PBKDF1_SHA1: UInt32](/documentation/security/cssm_algid_pkcs5_pbkdf1_sha1)
- [var CSSM_ALGID_PKCS5_PBKDF2: UInt32](/documentation/security/cssm_algid_pkcs5_pbkdf2)
- [var CSSM_ALGID_RC2: UInt32](/documentation/security/cssm_algid_rc2)
- [var CSSM_ALGID_RC4: UInt32](/documentation/security/cssm_algid_rc4)
- [var CSSM_ALGID_RC5: UInt32](/documentation/security/cssm_algid_rc5)
- [var CSSM_ALGID_RDES: UInt32](/documentation/security/cssm_algid_rdes)
- [var CSSM_ALGID_REDOC: UInt32](/documentation/security/cssm_algid_redoc)
- [var CSSM_ALGID_REDOC3: UInt32](/documentation/security/cssm_algid_redoc3)
- [var CSSM_ALGID_RIPEMAC: UInt32](/documentation/security/cssm_algid_ripemac)
- [var CSSM_ALGID_RIPEMD: UInt32](/documentation/security/cssm_algid_ripemd)
- [var CSSM_ALGID_RSA: UInt32](/documentation/security/cssm_algid_rsa)
- [var CSSM_ALGID_RUNNING_COUNTER: UInt32](/documentation/security/cssm_algid_running_counter)
- [var CSSM_ALGID_SAFER: UInt32](/documentation/security/cssm_algid_safer)
- [var CSSM_ALGID_SEAL: UInt32](/documentation/security/cssm_algid_seal)
- [var CSSM_ALGID_SECURE_PASSPHRASE: UInt32](/documentation/security/cssm_algid_secure_passphrase)
- [var CSSM_ALGID_SHA1: UInt32](/documentation/security/cssm_algid_sha1)
- [var CSSM_ALGID_SHA1HMAC: UInt32](/documentation/security/cssm_algid_sha1hmac)
- [var CSSM_ALGID_SHA1HMAC_LEGACY: UInt32](/documentation/security/cssm_algid_sha1hmac_legacy)
- [var CSSM_ALGID_SHA1WithDSA: UInt32](/documentation/security/cssm_algid_sha1withdsa)
- [var CSSM_ALGID_SHA1WithECDSA: UInt32](/documentation/security/cssm_algid_sha1withecdsa)
- [var CSSM_ALGID_SHA1WithECNRA: UInt32](/documentation/security/cssm_algid_sha1withecnra)
- [var CSSM_ALGID_SHA1WithRSA: UInt32](/documentation/security/cssm_algid_sha1withrsa)
- [var CSSM_ALGID_SHA224: UInt32](/documentation/security/cssm_algid_sha224)
- [var CSSM_ALGID_SHA224WithECDSA: UInt32](/documentation/security/cssm_algid_sha224withecdsa)
- [var CSSM_ALGID_SHA224WithRSA: UInt32](/documentation/security/cssm_algid_sha224withrsa)
- [var CSSM_ALGID_SHA256: UInt32](/documentation/security/cssm_algid_sha256)
- [var CSSM_ALGID_SHA256WithECDSA: UInt32](/documentation/security/cssm_algid_sha256withecdsa)
- [var CSSM_ALGID_SHA256WithRSA: UInt32](/documentation/security/cssm_algid_sha256withrsa)
- [var CSSM_ALGID_SHA384: UInt32](/documentation/security/cssm_algid_sha384)
- [var CSSM_ALGID_SHA384WithECDSA: UInt32](/documentation/security/cssm_algid_sha384withecdsa)
- [var CSSM_ALGID_SHA384WithRSA: UInt32](/documentation/security/cssm_algid_sha384withrsa)
- [var CSSM_ALGID_SHA512: UInt32](/documentation/security/cssm_algid_sha512)
- [var CSSM_ALGID_SHA512WithECDSA: UInt32](/documentation/security/cssm_algid_sha512withecdsa)
- [var CSSM_ALGID_SHA512WithRSA: UInt32](/documentation/security/cssm_algid_sha512withrsa)
- [var CSSM_ALGID_SHARandom: UInt32](/documentation/security/cssm_algid_sharandom)
- [var CSSM_ALGID_SKIPJACK: UInt32](/documentation/security/cssm_algid_skipjack)
- [var CSSM_ALGID_SSL3KeyAndMacDerive: UInt32](/documentation/security/cssm_algid_ssl3keyandmacderive)
- [var CSSM_ALGID_SSL3MD5: UInt32](/documentation/security/cssm_algid_ssl3md5)
- [var CSSM_ALGID_SSL3MD5_MAC: UInt32](/documentation/security/cssm_algid_ssl3md5_mac)
- [var CSSM_ALGID_SSL3MasterDerive: UInt32](/documentation/security/cssm_algid_ssl3masterderive)
- [var CSSM_ALGID_SSL3PreMasterGen: UInt32](/documentation/security/cssm_algid_ssl3premastergen)
- [var CSSM_ALGID_SSL3PrePrimaryGen: UInt32](/documentation/security/cssm_algid_ssl3preprimarygen)
- [var CSSM_ALGID_SSL3PrimaryDerive: UInt32](/documentation/security/cssm_algid_ssl3primaryderive)
- [var CSSM_ALGID_SSL3SHA1: UInt32](/documentation/security/cssm_algid_ssl3sha1)
- [var CSSM_ALGID_SSL3SHA1_MAC: UInt32](/documentation/security/cssm_algid_ssl3sha1_mac)
- [var CSSM_ALGID_TIGER: UInt32](/documentation/security/cssm_algid_tiger)
- [var CSSM_ALGID_UTC: UInt32](/documentation/security/cssm_algid_utc)
- [var CSSM_ALGID_VENDOR_DEFINED: UInt32](/documentation/security/cssm_algid_vendor_defined)
- [var CSSM_ALGID_WrapLynks: UInt32](/documentation/security/cssm_algid_wraplynks)
- [var CSSM_ALGID_WrapSET_OAEP: UInt32](/documentation/security/cssm_algid_wrapset_oaep)
- [var CSSM_ALGID_XORBaseAndData: UInt32](/documentation/security/cssm_algid_xorbaseanddata)
- [var CSSM_ALGID__FIRST_UNUSED: UInt32](/documentation/security/cssm_algid__first_unused)
- [var CSSM_ALGMODE_BC: UInt32](/documentation/security/cssm_algmode_bc)
- [var CSSM_ALGMODE_CBC: UInt32](/documentation/security/cssm_algmode_cbc)
- [var CSSM_ALGMODE_CBC128: UInt32](/documentation/security/cssm_algmode_cbc128)
- [var CSSM_ALGMODE_CBC64: UInt32](/documentation/security/cssm_algmode_cbc64)
- [var CSSM_ALGMODE_CBCC: UInt32](/documentation/security/cssm_algmode_cbcc)
- [var CSSM_ALGMODE_CBCPD: UInt32](/documentation/security/cssm_algmode_cbcpd)
- [var CSSM_ALGMODE_CBCPadIV8: UInt32](/documentation/security/cssm_algmode_cbcpadiv8)
- [var CSSM_ALGMODE_CBC_IV8: UInt32](/documentation/security/cssm_algmode_cbc_iv8)
- [var CSSM_ALGMODE_CFB: UInt32](/documentation/security/cssm_algmode_cfb)
- [var CSSM_ALGMODE_CFB16: UInt32](/documentation/security/cssm_algmode_cfb16)
- [var CSSM_ALGMODE_CFB32: UInt32](/documentation/security/cssm_algmode_cfb32)
- [var CSSM_ALGMODE_CFB8: UInt32](/documentation/security/cssm_algmode_cfb8)
- [var CSSM_ALGMODE_CFBPadIV8: UInt32](/documentation/security/cssm_algmode_cfbpadiv8)
- [var CSSM_ALGMODE_CFB_IV8: UInt32](/documentation/security/cssm_algmode_cfb_iv8)
- [var CSSM_ALGMODE_COUNTER: UInt32](/documentation/security/cssm_algmode_counter)
- [var CSSM_ALGMODE_CUSTOM: UInt32](/documentation/security/cssm_algmode_custom)
- [var CSSM_ALGMODE_ECB: UInt32](/documentation/security/cssm_algmode_ecb)
- [var CSSM_ALGMODE_ECB128: UInt32](/documentation/security/cssm_algmode_ecb128)
- [var CSSM_ALGMODE_ECB64: UInt32](/documentation/security/cssm_algmode_ecb64)
- [var CSSM_ALGMODE_ECB96: UInt32](/documentation/security/cssm_algmode_ecb96)
- [var CSSM_ALGMODE_ECBPad: UInt32](/documentation/security/cssm_algmode_ecbpad)
- [var CSSM_ALGMODE_ISO_9796: UInt32](/documentation/security/cssm_algmode_iso_9796)
- [var CSSM_ALGMODE_LAST: UInt32](/documentation/security/cssm_algmode_last)
- [var CSSM_ALGMODE_NONE: UInt32](/documentation/security/cssm_algmode_none)
- [var CSSM_ALGMODE_OAEP_HASH: UInt32](/documentation/security/cssm_algmode_oaep_hash)
- [var CSSM_ALGMODE_OFB: UInt32](/documentation/security/cssm_algmode_ofb)
- [var CSSM_ALGMODE_OFB64: UInt32](/documentation/security/cssm_algmode_ofb64)
- [var CSSM_ALGMODE_OFBNLF: UInt32](/documentation/security/cssm_algmode_ofbnlf)
- [var CSSM_ALGMODE_OFBPadIV8: UInt32](/documentation/security/cssm_algmode_ofbpadiv8)
- [var CSSM_ALGMODE_OFB_IV8: UInt32](/documentation/security/cssm_algmode_ofb_iv8)
- [var CSSM_ALGMODE_PBC: UInt32](/documentation/security/cssm_algmode_pbc)
- [var CSSM_ALGMODE_PCBC: UInt32](/documentation/security/cssm_algmode_pcbc)
- [var CSSM_ALGMODE_PFB: UInt32](/documentation/security/cssm_algmode_pfb)
- [var CSSM_ALGMODE_PKCS1_EME_OAEP: UInt32](/documentation/security/cssm_algmode_pkcs1_eme_oaep)
- [var CSSM_ALGMODE_PKCS1_EME_V15: UInt32](/documentation/security/cssm_algmode_pkcs1_eme_v15)
- [var CSSM_ALGMODE_PKCS1_EMSA_V15: UInt32](/documentation/security/cssm_algmode_pkcs1_emsa_v15)
- [var CSSM_ALGMODE_PRIVATE_KEY: UInt32](/documentation/security/cssm_algmode_private_key)
- [var CSSM_ALGMODE_PRIVATE_WRAP: UInt32](/documentation/security/cssm_algmode_private_wrap)
- [var CSSM_ALGMODE_PUBLIC_KEY: UInt32](/documentation/security/cssm_algmode_public_key)
- [var CSSM_ALGMODE_RELAYX: UInt32](/documentation/security/cssm_algmode_relayx)
- [var CSSM_ALGMODE_SHUFFLE: UInt32](/documentation/security/cssm_algmode_shuffle)
- [var CSSM_ALGMODE_VENDOR_DEFINED: UInt32](/documentation/security/cssm_algmode_vendor_defined)
- [var CSSM_ALGMODE_WRAP: UInt32](/documentation/security/cssm_algmode_wrap)
- [var CSSM_ALGMODE_X9_31: UInt32](/documentation/security/cssm_algmode_x9_31)
- [var CSSM_APPLECSPDL_DB_CHANGE_PASSWORD: Int](/documentation/security/cssm_applecspdl_db_change_password)
- [var CSSM_APPLECSPDL_DB_GET_HANDLE: Int](/documentation/security/cssm_applecspdl_db_get_handle)
- [var CSSM_APPLECSPDL_DB_GET_SETTINGS: Int](/documentation/security/cssm_applecspdl_db_get_settings)
- [var CSSM_APPLECSPDL_DB_IS_LOCKED: Int](/documentation/security/cssm_applecspdl_db_is_locked)
- [var CSSM_APPLECSPDL_DB_LOCK: Int](/documentation/security/cssm_applecspdl_db_lock)
- [var CSSM_APPLECSPDL_DB_SET_SETTINGS: Int](/documentation/security/cssm_applecspdl_db_set_settings)
- [var CSSM_APPLECSPDL_DB_UNLOCK: Int](/documentation/security/cssm_applecspdl_db_unlock)
- [var CSSM_APPLECSP_KEYDIGEST: Int](/documentation/security/cssm_applecsp_keydigest)
- [var CSSM_APPLECSP_PUBKEY: Int](/documentation/security/cssm_applecsp_pubkey)
- [var CSSM_APPLEDL_OPEN_PARAMETERS_VERSION: Int](/documentation/security/cssm_appledl_open_parameters_version)
- [var CSSM_APPLEFILEDL_COMMIT: Int](/documentation/security/cssm_applefiledl_commit)
- [var CSSM_APPLEFILEDL_DELETE_FILE: Int](/documentation/security/cssm_applefiledl_delete_file)
- [var CSSM_APPLEFILEDL_MAKE_BACKUP: Int](/documentation/security/cssm_applefiledl_make_backup)
- [var CSSM_APPLEFILEDL_MAKE_COPY: Int](/documentation/security/cssm_applefiledl_make_copy)
- [var CSSM_APPLEFILEDL_ROLLBACK: Int](/documentation/security/cssm_applefiledl_rollback)
- [var CSSM_APPLEFILEDL_TAKE_FILE_LOCK: Int](/documentation/security/cssm_applefiledl_take_file_lock)
- [var CSSM_APPLEFILEDL_TOGGLE_AUTOCOMMIT: Int](/documentation/security/cssm_applefiledl_toggle_autocommit)
- [var CSSM_APPLESCPDL_CSP_GET_KEYHANDLE: Int](/documentation/security/cssm_applescpdl_csp_get_keyhandle)
- [var CSSM_APPLEX509CL_OBTAIN_CSR: Int](/documentation/security/cssm_applex509cl_obtain_csr)
- [var CSSM_APPLEX509CL_VERIFY_CSR: Int](/documentation/security/cssm_applex509cl_verify_csr)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_10: Int](/documentation/security/cssm_apple_private_cspdl_code_10)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_11: Int](/documentation/security/cssm_apple_private_cspdl_code_11)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_12: Int](/documentation/security/cssm_apple_private_cspdl_code_12)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_13: Int](/documentation/security/cssm_apple_private_cspdl_code_13)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_14: Int](/documentation/security/cssm_apple_private_cspdl_code_14)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_15: Int](/documentation/security/cssm_apple_private_cspdl_code_15)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_16: Int](/documentation/security/cssm_apple_private_cspdl_code_16)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_17: Int](/documentation/security/cssm_apple_private_cspdl_code_17)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_18: Int](/documentation/security/cssm_apple_private_cspdl_code_18)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_19: Int](/documentation/security/cssm_apple_private_cspdl_code_19)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_20: Int](/documentation/security/cssm_apple_private_cspdl_code_20)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_21: Int](/documentation/security/cssm_apple_private_cspdl_code_21)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_22: Int](/documentation/security/cssm_apple_private_cspdl_code_22)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_23: Int](/documentation/security/cssm_apple_private_cspdl_code_23)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_24: Int](/documentation/security/cssm_apple_private_cspdl_code_24)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_25: Int](/documentation/security/cssm_apple_private_cspdl_code_25)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_26: Int](/documentation/security/cssm_apple_private_cspdl_code_26)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_27: Int](/documentation/security/cssm_apple_private_cspdl_code_27)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_8: Int](/documentation/security/cssm_apple_private_cspdl_code_8)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_9: Int](/documentation/security/cssm_apple_private_cspdl_code_9)
- [var CSSM_APPLE_UNLOCK_TYPE_KEYBAG: Int](/documentation/security/cssm_apple_unlock_type_keybag)
- [var CSSM_APPLE_UNLOCK_TYPE_KEY_DIRECT: Int](/documentation/security/cssm_apple_unlock_type_key_direct)
- [var CSSM_APPLE_UNLOCK_TYPE_WRAPPED_PRIVATE: Int](/documentation/security/cssm_apple_unlock_type_wrapped_private)
- [var CSSM_ASC_OPTIMIZE_ASCII: Int](/documentation/security/cssm_asc_optimize_ascii)
- [var CSSM_ASC_OPTIMIZE_DEFAULT: Int](/documentation/security/cssm_asc_optimize_default)
- [var CSSM_ASC_OPTIMIZE_SECURITY: Int](/documentation/security/cssm_asc_optimize_security)
- [var CSSM_ASC_OPTIMIZE_SIZE: Int](/documentation/security/cssm_asc_optimize_size)
- [var CSSM_ASC_OPTIMIZE_TIME: Int](/documentation/security/cssm_asc_optimize_time)
- [var CSSM_ASC_OPTIMIZE_TIME_SIZE: Int](/documentation/security/cssm_asc_optimize_time_size)
- [var CSSM_ATTACH_READ_ONLY: Int](/documentation/security/cssm_attach_read_only)
- [var CSSM_ATTRIBUTE_ACCESS_CREDENTIALS: UInt32](/documentation/security/cssm_attribute_access_credentials)
- [var CSSM_ATTRIBUTE_ALERT_TITLE: Int](/documentation/security/cssm_attribute_alert_title)
- [var CSSM_ATTRIBUTE_ALG_ID: UInt32](/documentation/security/cssm_attribute_alg_id)
- [var CSSM_ATTRIBUTE_ALG_PARAMS: UInt32](/documentation/security/cssm_attribute_alg_params)
- [var CSSM_ATTRIBUTE_ASC_OPTIMIZATION: Int](/documentation/security/cssm_attribute_asc_optimization)
- [var CSSM_ATTRIBUTE_BASE: UInt32](/documentation/security/cssm_attribute_base)
- [var CSSM_ATTRIBUTE_BLOCK_SIZE: UInt32](/documentation/security/cssm_attribute_block_size)
- [var CSSM_ATTRIBUTE_CSP_HANDLE: UInt32](/documentation/security/cssm_attribute_csp_handle)
- [var CSSM_ATTRIBUTE_CUSTOM: UInt32](/documentation/security/cssm_attribute_custom)
- [var CSSM_ATTRIBUTE_DATA_ACCESS_CREDENTIALS: UInt32](/documentation/security/cssm_attribute_data_access_credentials)
- [var CSSM_ATTRIBUTE_DATA_CRYPTO_DATA: UInt32](/documentation/security/cssm_attribute_data_crypto_data)
- [var CSSM_ATTRIBUTE_DATA_CSSM_DATA: UInt32](/documentation/security/cssm_attribute_data_cssm_data)
- [var CSSM_ATTRIBUTE_DATA_DATE: UInt32](/documentation/security/cssm_attribute_data_date)
- [var CSSM_ATTRIBUTE_DATA_DL_DB_HANDLE: UInt32](/documentation/security/cssm_attribute_data_dl_db_handle)
- [var CSSM_ATTRIBUTE_DATA_KEY: UInt32](/documentation/security/cssm_attribute_data_key)
- [var CSSM_ATTRIBUTE_DATA_KR_PROFILE: UInt32](/documentation/security/cssm_attribute_data_kr_profile)
- [var CSSM_ATTRIBUTE_DATA_NONE: UInt32](/documentation/security/cssm_attribute_data_none)
- [var CSSM_ATTRIBUTE_DATA_RANGE: UInt32](/documentation/security/cssm_attribute_data_range)
- [var CSSM_ATTRIBUTE_DATA_STRING: UInt32](/documentation/security/cssm_attribute_data_string)
- [var CSSM_ATTRIBUTE_DATA_UINT32: UInt32](/documentation/security/cssm_attribute_data_uint32)
- [var CSSM_ATTRIBUTE_DATA_VERSION: UInt32](/documentation/security/cssm_attribute_data_version)
- [var CSSM_ATTRIBUTE_DESCRIPTION: UInt32](/documentation/security/cssm_attribute_description)
- [var CSSM_ATTRIBUTE_DL_DB_HANDLE: UInt32](/documentation/security/cssm_attribute_dl_db_handle)
- [var CSSM_ATTRIBUTE_EFFECTIVE_BITS: UInt32](/documentation/security/cssm_attribute_effective_bits)
- [var CSSM_ATTRIBUTE_END_DATE: UInt32](/documentation/security/cssm_attribute_end_date)
- [var CSSM_ATTRIBUTE_FEE_CURVE_TYPE: Int](/documentation/security/cssm_attribute_fee_curve_type)
- [var CSSM_ATTRIBUTE_FEE_PRIME_TYPE: Int](/documentation/security/cssm_attribute_fee_prime_type)
- [var CSSM_ATTRIBUTE_INIT_VECTOR: UInt32](/documentation/security/cssm_attribute_init_vector)
- [var CSSM_ATTRIBUTE_ITERATION_COUNT: UInt32](/documentation/security/cssm_attribute_iteration_count)
- [var CSSM_ATTRIBUTE_IV_SIZE: UInt32](/documentation/security/cssm_attribute_iv_size)
- [var CSSM_ATTRIBUTE_KEY: UInt32](/documentation/security/cssm_attribute_key)
- [var CSSM_ATTRIBUTE_KEYATTR: UInt32](/documentation/security/cssm_attribute_keyattr)
- [var CSSM_ATTRIBUTE_KEYUSAGE: UInt32](/documentation/security/cssm_attribute_keyusage)
- [var CSSM_ATTRIBUTE_KEY_LENGTH: UInt32](/documentation/security/cssm_attribute_key_length)
- [var CSSM_ATTRIBUTE_KEY_LENGTH_RANGE: UInt32](/documentation/security/cssm_attribute_key_length_range)
- [var CSSM_ATTRIBUTE_KEY_TYPE: UInt32](/documentation/security/cssm_attribute_key_type)
- [var CSSM_ATTRIBUTE_KRPROFILE_LOCAL: UInt32](/documentation/security/cssm_attribute_krprofile_local)
- [var CSSM_ATTRIBUTE_KRPROFILE_REMOTE: UInt32](/documentation/security/cssm_attribute_krprofile_remote)
- [var CSSM_ATTRIBUTE_LABEL: UInt32](/documentation/security/cssm_attribute_label)
- [var CSSM_ATTRIBUTE_MODE: UInt32](/documentation/security/cssm_attribute_mode)
- [var CSSM_ATTRIBUTE_NONE: UInt32](/documentation/security/cssm_attribute_none)
- [var CSSM_ATTRIBUTE_OUTPUT_SIZE: UInt32](/documentation/security/cssm_attribute_output_size)
- [var CSSM_ATTRIBUTE_PADDING: UInt32](/documentation/security/cssm_attribute_padding)
- [var CSSM_ATTRIBUTE_PARAM_KEY: Int](/documentation/security/cssm_attribute_param_key)
- [var CSSM_ATTRIBUTE_PASSPHRASE: UInt32](/documentation/security/cssm_attribute_passphrase)
- [var CSSM_ATTRIBUTE_PRIME: UInt32](/documentation/security/cssm_attribute_prime)
- [var CSSM_ATTRIBUTE_PRIVATE_KEY_FORMAT: UInt32](/documentation/security/cssm_attribute_private_key_format)
- [var CSSM_ATTRIBUTE_PROMPT: Int](/documentation/security/cssm_attribute_prompt)
- [var CSSM_ATTRIBUTE_PUBLIC_KEY: Int](/documentation/security/cssm_attribute_public_key)
- [var CSSM_ATTRIBUTE_PUBLIC_KEY_FORMAT: UInt32](/documentation/security/cssm_attribute_public_key_format)
- [var CSSM_ATTRIBUTE_RANDOM: UInt32](/documentation/security/cssm_attribute_random)
- [var CSSM_ATTRIBUTE_ROUNDS: UInt32](/documentation/security/cssm_attribute_rounds)
- [var CSSM_ATTRIBUTE_ROUNDS_RANGE: UInt32](/documentation/security/cssm_attribute_rounds_range)
- [var CSSM_ATTRIBUTE_RSA_BLINDING: Int](/documentation/security/cssm_attribute_rsa_blinding)
- [var CSSM_ATTRIBUTE_SALT: UInt32](/documentation/security/cssm_attribute_salt)
- [var CSSM_ATTRIBUTE_SEED: UInt32](/documentation/security/cssm_attribute_seed)
- [var CSSM_ATTRIBUTE_START_DATE: UInt32](/documentation/security/cssm_attribute_start_date)
- [var CSSM_ATTRIBUTE_SUBPRIME: UInt32](/documentation/security/cssm_attribute_subprime)
- [var CSSM_ATTRIBUTE_SYMMETRIC_KEY_FORMAT: UInt32](/documentation/security/cssm_attribute_symmetric_key_format)
- [var CSSM_ATTRIBUTE_TYPE_MASK: UInt32](/documentation/security/cssm_attribute_type_mask)
- [var CSSM_ATTRIBUTE_VENDOR_DEFINED: Int](/documentation/security/cssm_attribute_vendor_defined)
- [var CSSM_ATTRIBUTE_VERIFY_PASSPHRASE: Int](/documentation/security/cssm_attribute_verify_passphrase)
- [var CSSM_ATTRIBUTE_VERSION: UInt32](/documentation/security/cssm_attribute_version)
- [var CSSM_ATTRIBUTE_WRAPPED_KEY_FORMAT: UInt32](/documentation/security/cssm_attribute_wrapped_key_format)
- [var CSSM_BASE_ERROR: Int](/documentation/security/cssm_base_error)
- [var CSSM_CERTGROUP_CERT_PAIR: Int](/documentation/security/cssm_certgroup_cert_pair)
- [var CSSM_CERTGROUP_DATA: Int](/documentation/security/cssm_certgroup_data)
- [var CSSM_CERTGROUP_ENCODED_CERT: Int](/documentation/security/cssm_certgroup_encoded_cert)
- [var CSSM_CERTGROUP_PARSED_CERT: Int](/documentation/security/cssm_certgroup_parsed_cert)
- [var CSSM_CERT_ACL_ENTRY: Int](/documentation/security/cssm_cert_acl_entry)
- [var CSSM_CERT_BUNDLE_CUSTOM: Int](/documentation/security/cssm_cert_bundle_custom)
- [var CSSM_CERT_BUNDLE_ENCODING_BER: Int](/documentation/security/cssm_cert_bundle_encoding_ber)
- [var CSSM_CERT_BUNDLE_ENCODING_CUSTOM: Int](/documentation/security/cssm_cert_bundle_encoding_custom)
- [var CSSM_CERT_BUNDLE_ENCODING_DER: Int](/documentation/security/cssm_cert_bundle_encoding_der)
- [var CSSM_CERT_BUNDLE_ENCODING_PGP: Int](/documentation/security/cssm_cert_bundle_encoding_pgp)
- [var CSSM_CERT_BUNDLE_ENCODING_SEXPR: Int](/documentation/security/cssm_cert_bundle_encoding_sexpr)
- [var CSSM_CERT_BUNDLE_ENCODING_UNKNOWN: Int](/documentation/security/cssm_cert_bundle_encoding_unknown)
- [var CSSM_CERT_BUNDLE_LAST: Int](/documentation/security/cssm_cert_bundle_last)
- [var CSSM_CERT_BUNDLE_PFX: Int](/documentation/security/cssm_cert_bundle_pfx)
- [var CSSM_CERT_BUNDLE_PGP_KEYRING: Int](/documentation/security/cssm_cert_bundle_pgp_keyring)
- [var CSSM_CERT_BUNDLE_PKCS12: Int](/documentation/security/cssm_cert_bundle_pkcs12)
- [var CSSM_CERT_BUNDLE_PKCS7_SIGNED_DATA: Int](/documentation/security/cssm_cert_bundle_pkcs7_signed_data)
- [var CSSM_CERT_BUNDLE_PKCS7_SIGNED_ENVELOPED_DATA: Int](/documentation/security/cssm_cert_bundle_pkcs7_signed_enveloped_data)
- [var CSSM_CERT_BUNDLE_SPKI_SEQUENCE: Int](/documentation/security/cssm_cert_bundle_spki_sequence)
- [var CSSM_CERT_BUNDLE_UNKNOWN: Int](/documentation/security/cssm_cert_bundle_unknown)
- [var CSSM_CERT_ENCODING_BER: Int](/documentation/security/cssm_cert_encoding_ber)
- [var CSSM_CERT_ENCODING_CUSTOM: Int](/documentation/security/cssm_cert_encoding_custom)
- [var CSSM_CERT_ENCODING_DER: Int](/documentation/security/cssm_cert_encoding_der)
- [var CSSM_CERT_ENCODING_LAST: Int](/documentation/security/cssm_cert_encoding_last)
- [var CSSM_CERT_ENCODING_MULTIPLE: Int](/documentation/security/cssm_cert_encoding_multiple)
- [var CSSM_CERT_ENCODING_NDR: Int](/documentation/security/cssm_cert_encoding_ndr)
- [var CSSM_CERT_ENCODING_PGP: Int](/documentation/security/cssm_cert_encoding_pgp)
- [var CSSM_CERT_ENCODING_SEXPR: Int](/documentation/security/cssm_cert_encoding_sexpr)
- [var CSSM_CERT_ENCODING_UNKNOWN: Int](/documentation/security/cssm_cert_encoding_unknown)
- [var CSSM_CERT_Intel: Int](/documentation/security/cssm_cert_intel)
- [var CSSM_CERT_LAST: Int](/documentation/security/cssm_cert_last)
- [var CSSM_CERT_MULTIPLE: Int](/documentation/security/cssm_cert_multiple)
- [var CSSM_CERT_PARSE_FORMAT_COMPLEX: Int](/documentation/security/cssm_cert_parse_format_complex)
- [var CSSM_CERT_PARSE_FORMAT_CUSTOM: Int](/documentation/security/cssm_cert_parse_format_custom)
- [var CSSM_CERT_PARSE_FORMAT_LAST: Int](/documentation/security/cssm_cert_parse_format_last)
- [var CSSM_CERT_PARSE_FORMAT_MULTIPLE: Int](/documentation/security/cssm_cert_parse_format_multiple)
- [var CSSM_CERT_PARSE_FORMAT_NONE: Int](/documentation/security/cssm_cert_parse_format_none)
- [var CSSM_CERT_PARSE_FORMAT_OID_NAMED: Int](/documentation/security/cssm_cert_parse_format_oid_named)
- [var CSSM_CERT_PARSE_FORMAT_SEXPR: Int](/documentation/security/cssm_cert_parse_format_sexpr)
- [var CSSM_CERT_PARSE_FORMAT_TUPLE: Int](/documentation/security/cssm_cert_parse_format_tuple)
- [var CSSM_CERT_PGP: Int](/documentation/security/cssm_cert_pgp)
- [var CSSM_CERT_SDSIv1: Int](/documentation/security/cssm_cert_sdsiv1)
- [var CSSM_CERT_SPKI: Int](/documentation/security/cssm_cert_spki)
- [var CSSM_CERT_STATUS_EXPIRED: Int](/documentation/security/cssm_cert_status_expired)
- [var CSSM_CERT_STATUS_IS_FROM_NET: Int](/documentation/security/cssm_cert_status_is_from_net)
- [var CSSM_CERT_STATUS_IS_IN_ANCHORS: Int](/documentation/security/cssm_cert_status_is_in_anchors)
- [var CSSM_CERT_STATUS_IS_IN_INPUT_CERTS: Int](/documentation/security/cssm_cert_status_is_in_input_certs)
- [var CSSM_CERT_STATUS_IS_ROOT: Int](/documentation/security/cssm_cert_status_is_root)
- [var CSSM_CERT_STATUS_NOT_VALID_YET: Int](/documentation/security/cssm_cert_status_not_valid_yet)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_DENY: Int](/documentation/security/cssm_cert_status_trust_settings_deny)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_FOUND_ADMIN: Int](/documentation/security/cssm_cert_status_trust_settings_found_admin)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_FOUND_SYSTEM: Int](/documentation/security/cssm_cert_status_trust_settings_found_system)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_FOUND_USER: Int](/documentation/security/cssm_cert_status_trust_settings_found_user)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_IGNORED_ERROR: Int](/documentation/security/cssm_cert_status_trust_settings_ignored_error)
- [var CSSM_CERT_STATUS_TRUST_SETTINGS_TRUST: Int](/documentation/security/cssm_cert_status_trust_settings_trust)
- [var CSSM_CERT_TUPLE: Int](/documentation/security/cssm_cert_tuple)
- [var CSSM_CERT_UNKNOWN: Int](/documentation/security/cssm_cert_unknown)
- [var CSSM_CERT_X9_ATTRIBUTE: Int](/documentation/security/cssm_cert_x9_attribute)
- [var CSSM_CERT_X_509_ATTRIBUTE: Int](/documentation/security/cssm_cert_x_509_attribute)
- [var CSSM_CERT_X_509v1: Int](/documentation/security/cssm_cert_x_509v1)
- [var CSSM_CERT_X_509v2: Int](/documentation/security/cssm_cert_x_509v2)
- [var CSSM_CERT_X_509v3: Int](/documentation/security/cssm_cert_x_509v3)
- [var CSSM_CL_BASE_CL_ERROR: Int](/documentation/security/cssm_cl_base_cl_error)
- [var CSSM_CL_BASE_ERROR: Int](/documentation/security/cssm_cl_base_error)
- [var CSSM_CL_CUSTOM_CERT_BUNDLE_TYPE: Int](/documentation/security/cssm_cl_custom_cert_bundle_type)
- [var CSSM_CL_CUSTOM_CERT_ENCODING: Int](/documentation/security/cssm_cl_custom_cert_encoding)
- [var CSSM_CL_CUSTOM_CERT_PARSE_FORMAT: Int](/documentation/security/cssm_cl_custom_cert_parse_format)
- [var CSSM_CL_CUSTOM_CERT_TYPE: Int](/documentation/security/cssm_cl_custom_cert_type)
- [var CSSM_CL_CUSTOM_CRL_PARSE_FORMAT: Int](/documentation/security/cssm_cl_custom_crl_parse_format)
- [var CSSM_CL_PRIVATE_ERROR: Int](/documentation/security/cssm_cl_private_error)
- [var CSSM_CL_TEMPLATE_INTERMEDIATE_CERT: Int](/documentation/security/cssm_cl_template_intermediate_cert)
- [var CSSM_CL_TEMPLATE_PKIX_CERTTEMPLATE: Int](/documentation/security/cssm_cl_template_pkix_certtemplate)
- [var CSSM_CONTEXT_EVENT_CREATE: Int](/documentation/security/cssm_context_event_create)
- [var CSSM_CONTEXT_EVENT_DELETE: Int](/documentation/security/cssm_context_event_delete)
- [var CSSM_CONTEXT_EVENT_UPDATE: Int](/documentation/security/cssm_context_event_update)
- [var CSSM_CRLGROUP_CRL_PAIR: Int](/documentation/security/cssm_crlgroup_crl_pair)
- [var CSSM_CRLGROUP_DATA: Int](/documentation/security/cssm_crlgroup_data)
- [var CSSM_CRLGROUP_ENCODED_CRL: Int](/documentation/security/cssm_crlgroup_encoded_crl)
- [var CSSM_CRLGROUP_PARSED_CRL: Int](/documentation/security/cssm_crlgroup_parsed_crl)
- [var CSSM_CRL_ENCODING_BER: Int](/documentation/security/cssm_crl_encoding_ber)
- [var CSSM_CRL_ENCODING_BLOOM: Int](/documentation/security/cssm_crl_encoding_bloom)
- [var CSSM_CRL_ENCODING_CUSTOM: Int](/documentation/security/cssm_crl_encoding_custom)
- [var CSSM_CRL_ENCODING_DER: Int](/documentation/security/cssm_crl_encoding_der)
- [var CSSM_CRL_ENCODING_MULTIPLE: Int](/documentation/security/cssm_crl_encoding_multiple)
- [var CSSM_CRL_ENCODING_SEXPR: Int](/documentation/security/cssm_crl_encoding_sexpr)
- [var CSSM_CRL_ENCODING_UNKNOWN: Int](/documentation/security/cssm_crl_encoding_unknown)
- [var CSSM_CRL_PARSE_FORMAT_COMPLEX: Int](/documentation/security/cssm_crl_parse_format_complex)
- [var CSSM_CRL_PARSE_FORMAT_CUSTOM: Int](/documentation/security/cssm_crl_parse_format_custom)
- [var CSSM_CRL_PARSE_FORMAT_LAST: Int](/documentation/security/cssm_crl_parse_format_last)
- [var CSSM_CRL_PARSE_FORMAT_MULTIPLE: Int](/documentation/security/cssm_crl_parse_format_multiple)
- [var CSSM_CRL_PARSE_FORMAT_NONE: Int](/documentation/security/cssm_crl_parse_format_none)
- [var CSSM_CRL_PARSE_FORMAT_OID_NAMED: Int](/documentation/security/cssm_crl_parse_format_oid_named)
- [var CSSM_CRL_PARSE_FORMAT_SEXPR: Int](/documentation/security/cssm_crl_parse_format_sexpr)
- [var CSSM_CRL_PARSE_FORMAT_TUPLE: Int](/documentation/security/cssm_crl_parse_format_tuple)
- [var CSSM_CRL_TYPE_MULTIPLE: Int](/documentation/security/cssm_crl_type_multiple)
- [var CSSM_CRL_TYPE_SPKI: Int](/documentation/security/cssm_crl_type_spki)
- [var CSSM_CRL_TYPE_UNKNOWN: Int](/documentation/security/cssm_crl_type_unknown)
- [var CSSM_CRL_TYPE_X_509v1: Int](/documentation/security/cssm_crl_type_x_509v1)
- [var CSSM_CRL_TYPE_X_509v2: Int](/documentation/security/cssm_crl_type_x_509v2)
- [var CSSM_CSP_BASE_CSP_ERROR: Int](/documentation/security/cssm_csp_base_csp_error)
- [var CSSM_CSP_BASE_ERROR: Int](/documentation/security/cssm_csp_base_error)
- [var CSSM_CSP_HARDWARE: Int](/documentation/security/cssm_csp_hardware)
- [var CSSM_CSP_HYBRID: Int](/documentation/security/cssm_csp_hybrid)
- [var CSSM_CSP_PRIVATE_ERROR: Int](/documentation/security/cssm_csp_private_error)
- [var CSSM_CSP_RDR_EXISTS: Int](/documentation/security/cssm_csp_rdr_exists)
- [var CSSM_CSP_RDR_HW: Int](/documentation/security/cssm_csp_rdr_hw)
- [var CSSM_CSP_RDR_TOKENPRESENT: Int](/documentation/security/cssm_csp_rdr_tokenpresent)
- [var CSSM_CSP_SOFTWARE: Int](/documentation/security/cssm_csp_software)
- [var CSSM_CSP_STORES_CERTIFICATES: Int](/documentation/security/cssm_csp_stores_certificates)
- [var CSSM_CSP_STORES_GENERIC: Int](/documentation/security/cssm_csp_stores_generic)
- [var CSSM_CSP_STORES_PRIVATE_KEYS: Int](/documentation/security/cssm_csp_stores_private_keys)
- [var CSSM_CSP_STORES_PUBLIC_KEYS: Int](/documentation/security/cssm_csp_stores_public_keys)
- [var CSSM_CSP_STORES_SESSION_KEYS: Int](/documentation/security/cssm_csp_stores_session_keys)
- [var CSSM_CSP_TOK_CLOCK_EXISTS: Int](/documentation/security/cssm_csp_tok_clock_exists)
- [var CSSM_CSP_TOK_LOGIN_REQUIRED: Int](/documentation/security/cssm_csp_tok_login_required)
- [var CSSM_CSP_TOK_PRIVATE_KEY_PASSWORD: Int](/documentation/security/cssm_csp_tok_private_key_password)
- [var CSSM_CSP_TOK_PROT_AUTHENTICATION: Int](/documentation/security/cssm_csp_tok_prot_authentication)
- [var CSSM_CSP_TOK_RNG: Int](/documentation/security/cssm_csp_tok_rng)
- [var CSSM_CSP_TOK_SESSION_KEY_PASSWORD: Int](/documentation/security/cssm_csp_tok_session_key_password)
- [var CSSM_CSP_TOK_USER_PIN_EXPIRED: Int](/documentation/security/cssm_csp_tok_user_pin_expired)
- [var CSSM_CSP_TOK_USER_PIN_INITIALIZED: Int](/documentation/security/cssm_csp_tok_user_pin_initialized)
- [var CSSM_CSP_TOK_WRITE_PROTECTED: Int](/documentation/security/cssm_csp_tok_write_protected)
- [var CSSM_CSSM_BASE_CSSM_ERROR: Int](/documentation/security/cssm_cssm_base_cssm_error)
- [var CSSM_CSSM_BASE_ERROR: Int](/documentation/security/cssm_cssm_base_error)
- [var CSSM_CSSM_PRIVATE_ERROR: Int](/documentation/security/cssm_cssm_private_error)
- [var CSSM_CUSTOM_COMMON_ERROR_EXTENT: Int](/documentation/security/cssm_custom_common_error_extent)
- [var CSSM_DB_ACCESS_PRIVILEGED: Int](/documentation/security/cssm_db_access_privileged)
- [var CSSM_DB_ACCESS_READ: Int](/documentation/security/cssm_db_access_read)
- [var CSSM_DB_ACCESS_RESET: Int](/documentation/security/cssm_db_access_reset)
- [var CSSM_DB_ACCESS_WRITE: Int](/documentation/security/cssm_db_access_write)
- [var CSSM_DB_AND: Int](/documentation/security/cssm_db_and)
- [var CSSM_DB_ATTRIBUTE_FORMAT_BIG_NUM: Int](/documentation/security/cssm_db_attribute_format_big_num)
- [var CSSM_DB_ATTRIBUTE_FORMAT_BLOB: Int](/documentation/security/cssm_db_attribute_format_blob)
- [var CSSM_DB_ATTRIBUTE_FORMAT_COMPLEX: Int](/documentation/security/cssm_db_attribute_format_complex)
- [var CSSM_DB_ATTRIBUTE_FORMAT_MULTI_UINT32: Int](/documentation/security/cssm_db_attribute_format_multi_uint32)
- [var CSSM_DB_ATTRIBUTE_FORMAT_REAL: Int](/documentation/security/cssm_db_attribute_format_real)
- [var CSSM_DB_ATTRIBUTE_FORMAT_SINT32: Int](/documentation/security/cssm_db_attribute_format_sint32)
- [var CSSM_DB_ATTRIBUTE_FORMAT_STRING: Int](/documentation/security/cssm_db_attribute_format_string)
- [var CSSM_DB_ATTRIBUTE_FORMAT_TIME_DATE: Int](/documentation/security/cssm_db_attribute_format_time_date)
- [var CSSM_DB_ATTRIBUTE_FORMAT_UINT32: Int](/documentation/security/cssm_db_attribute_format_uint32)
- [var CSSM_DB_ATTRIBUTE_NAME_AS_INTEGER: Int](/documentation/security/cssm_db_attribute_name_as_integer)
- [var CSSM_DB_ATTRIBUTE_NAME_AS_OID: Int](/documentation/security/cssm_db_attribute_name_as_oid)
- [var CSSM_DB_ATTRIBUTE_NAME_AS_STRING: Int](/documentation/security/cssm_db_attribute_name_as_string)
- [var CSSM_DB_CERT_USE_OWNER: Int](/documentation/security/cssm_db_cert_use_owner)
- [var CSSM_DB_CERT_USE_PRIVACY: Int](/documentation/security/cssm_db_cert_use_privacy)
- [var CSSM_DB_CERT_USE_REVOKED: Int](/documentation/security/cssm_db_cert_use_revoked)
- [var CSSM_DB_CERT_USE_SIGNING: Int](/documentation/security/cssm_db_cert_use_signing)
- [var CSSM_DB_CERT_USE_SYSTEM: Int](/documentation/security/cssm_db_cert_use_system)
- [var CSSM_DB_CERT_USE_TRUSTED: Int](/documentation/security/cssm_db_cert_use_trusted)
- [var CSSM_DB_CONTAINS: Int](/documentation/security/cssm_db_contains)
- [var CSSM_DB_CONTAINS_FINAL_SUBSTRING: Int](/documentation/security/cssm_db_contains_final_substring)
- [var CSSM_DB_CONTAINS_INITIAL_SUBSTRING: Int](/documentation/security/cssm_db_contains_initial_substring)
- [var CSSM_DB_DATASTORES_UNKNOWN: UInt32](/documentation/security/cssm_db_datastores_unknown)
- [var CSSM_DB_EQUAL: Int](/documentation/security/cssm_db_equal)
- [var CSSM_DB_FILESYSTEMSCAN_MODE: Int](/documentation/security/cssm_db_filesystemscan_mode)
- [var CSSM_DB_GREATER_THAN: Int](/documentation/security/cssm_db_greater_than)
- [var CSSM_DB_INDEX_NONUNIQUE: Int](/documentation/security/cssm_db_index_nonunique)
- [var CSSM_DB_INDEX_ON_ATTRIBUTE: Int](/documentation/security/cssm_db_index_on_attribute)
- [var CSSM_DB_INDEX_ON_RECORD: Int](/documentation/security/cssm_db_index_on_record)
- [var CSSM_DB_INDEX_ON_UNKNOWN: Int](/documentation/security/cssm_db_index_on_unknown)
- [var CSSM_DB_INDEX_UNIQUE: Int](/documentation/security/cssm_db_index_unique)
- [var CSSM_DB_LESS_THAN: Int](/documentation/security/cssm_db_less_than)
- [var CSSM_DB_MODIFY_ATTRIBUTE_ADD: Int](/documentation/security/cssm_db_modify_attribute_add)
- [var CSSM_DB_MODIFY_ATTRIBUTE_DELETE: Int](/documentation/security/cssm_db_modify_attribute_delete)
- [var CSSM_DB_MODIFY_ATTRIBUTE_NONE: Int](/documentation/security/cssm_db_modify_attribute_none)
- [var CSSM_DB_MODIFY_ATTRIBUTE_REPLACE: Int](/documentation/security/cssm_db_modify_attribute_replace)
- [var CSSM_DB_NONE: Int](/documentation/security/cssm_db_none)
- [var CSSM_DB_NOT_EQUAL: Int](/documentation/security/cssm_db_not_equal)
- [var CSSM_DB_OR: Int](/documentation/security/cssm_db_or)
- [var CSSM_DB_RECORDTYPE_APP_DEFINED_END: UInt32](/documentation/security/cssm_db_recordtype_app_defined_end)
- [var CSSM_DB_RECORDTYPE_APP_DEFINED_START: UInt32](/documentation/security/cssm_db_recordtype_app_defined_start)
- [var CSSM_DB_RECORDTYPE_OPEN_GROUP_END: UInt32](/documentation/security/cssm_db_recordtype_open_group_end)
- [var CSSM_DB_RECORDTYPE_OPEN_GROUP_START: UInt32](/documentation/security/cssm_db_recordtype_open_group_start)
- [var CSSM_DB_RECORDTYPE_SCHEMA_END: UInt32](/documentation/security/cssm_db_recordtype_schema_end)
- [var CSSM_DB_RECORDTYPE_SCHEMA_START: UInt32](/documentation/security/cssm_db_recordtype_schema_start)
- [var CSSM_DB_TRANSACTIONAL_MODE: Int](/documentation/security/cssm_db_transactional_mode)
- [var CSSM_DL_BASE_DL_ERROR: Int](/documentation/security/cssm_dl_base_dl_error)
- [var CSSM_DL_BASE_ERROR: Int](/documentation/security/cssm_dl_base_error)
- [var CSSM_DL_CUSTOM: Int](/documentation/security/cssm_dl_custom)
- [var CSSM_DL_DB_RECORD_ALL_KEYS: UInt32](/documentation/security/cssm_dl_db_record_all_keys)
- [var CSSM_DL_DB_RECORD_ANY: UInt32](/documentation/security/cssm_dl_db_record_any)
- [var CSSM_DL_DB_RECORD_APPLESHARE_PASSWORD: UInt32](/documentation/security/cssm_dl_db_record_appleshare_password)
- [var CSSM_DL_DB_RECORD_CERT: UInt32](/documentation/security/cssm_dl_db_record_cert)
- [var CSSM_DL_DB_RECORD_CRL: UInt32](/documentation/security/cssm_dl_db_record_crl)
- [var CSSM_DL_DB_RECORD_EXTENDED_ATTRIBUTE: UInt32](/documentation/security/cssm_dl_db_record_extended_attribute)
- [var CSSM_DL_DB_RECORD_GENERIC: UInt32](/documentation/security/cssm_dl_db_record_generic)
- [var CSSM_DL_DB_RECORD_GENERIC_PASSWORD: UInt32](/documentation/security/cssm_dl_db_record_generic_password)
- [var CSSM_DL_DB_RECORD_INTERNET_PASSWORD: UInt32](/documentation/security/cssm_dl_db_record_internet_password)
- [var CSSM_DL_DB_RECORD_METADATA: UInt32](/documentation/security/cssm_dl_db_record_metadata)
- [var CSSM_DL_DB_RECORD_POLICY: UInt32](/documentation/security/cssm_dl_db_record_policy)
- [var CSSM_DL_DB_RECORD_PRIVATE_KEY: UInt32](/documentation/security/cssm_dl_db_record_private_key)
- [var CSSM_DL_DB_RECORD_PUBLIC_KEY: UInt32](/documentation/security/cssm_dl_db_record_public_key)
- [var CSSM_DL_DB_RECORD_SYMMETRIC_KEY: UInt32](/documentation/security/cssm_dl_db_record_symmetric_key)
- [var CSSM_DL_DB_RECORD_UNLOCK_REFERRAL: UInt32](/documentation/security/cssm_dl_db_record_unlock_referral)
- [var CSSM_DL_DB_RECORD_USER_TRUST: UInt32](/documentation/security/cssm_dl_db_record_user_trust)
- [var CSSM_DL_DB_RECORD_X509_CERTIFICATE: UInt32](/documentation/security/cssm_dl_db_record_x509_certificate)
- [var CSSM_DL_DB_RECORD_X509_CRL: UInt32](/documentation/security/cssm_dl_db_record_x509_crl)
- [var CSSM_DL_DB_SCHEMA_ATTRIBUTES: UInt32](/documentation/security/cssm_dl_db_schema_attributes)
- [var CSSM_DL_DB_SCHEMA_INDEXES: UInt32](/documentation/security/cssm_dl_db_schema_indexes)
- [var CSSM_DL_DB_SCHEMA_INFO: UInt32](/documentation/security/cssm_dl_db_schema_info)
- [var CSSM_DL_DB_SCHEMA_PARSING_MODULE: UInt32](/documentation/security/cssm_dl_db_schema_parsing_module)
- [var CSSM_DL_FFS: Int](/documentation/security/cssm_dl_ffs)
- [var CSSM_DL_LDAP: Int](/documentation/security/cssm_dl_ldap)
- [var CSSM_DL_MEMORY: Int](/documentation/security/cssm_dl_memory)
- [var CSSM_DL_ODBC: Int](/documentation/security/cssm_dl_odbc)
- [var CSSM_DL_PKCS11: Int](/documentation/security/cssm_dl_pkcs11)
- [var CSSM_DL_PRIVATE_ERROR: Int](/documentation/security/cssm_dl_private_error)
- [var CSSM_DL_REMOTEDIR: Int](/documentation/security/cssm_dl_remotedir)
- [var CSSM_DL_UNKNOWN: Int](/documentation/security/cssm_dl_unknown)
- [var CSSM_ELAPSED_TIME_COMPLETE: Int](/documentation/security/cssm_elapsed_time_complete)
- [var CSSM_ELAPSED_TIME_UNKNOWN: Int](/documentation/security/cssm_elapsed_time_unknown)
- [var CSSM_ERRCODE_ACL_ADD_FAILED: Int](/documentation/security/cssm_errcode_acl_add_failed)
- [var CSSM_ERRCODE_ACL_BASE_CERTS_NOT_SUPPORTED: Int](/documentation/security/cssm_errcode_acl_base_certs_not_supported)
- [var CSSM_ERRCODE_ACL_CHALLENGE_CALLBACK_FAILED: Int](/documentation/security/cssm_errcode_acl_challenge_callback_failed)
- [var CSSM_ERRCODE_ACL_CHANGE_FAILED: Int](/documentation/security/cssm_errcode_acl_change_failed)
- [var CSSM_ERRCODE_ACL_DELETE_FAILED: Int](/documentation/security/cssm_errcode_acl_delete_failed)
- [var CSSM_ERRCODE_ACL_ENTRY_TAG_NOT_FOUND: Int](/documentation/security/cssm_errcode_acl_entry_tag_not_found)
- [var CSSM_ERRCODE_ACL_REPLACE_FAILED: Int](/documentation/security/cssm_errcode_acl_replace_failed)
- [var CSSM_ERRCODE_ACL_SUBJECT_TYPE_NOT_SUPPORTED: Int](/documentation/security/cssm_errcode_acl_subject_type_not_supported)
- [var CSSM_ERRCODE_CRL_ALREADY_SIGNED: Int](/documentation/security/cssm_errcode_crl_already_signed)
- [var CSSM_ERRCODE_DEVICE_FAILED: Int](/documentation/security/cssm_errcode_device_failed)
- [var CSSM_ERRCODE_DEVICE_RESET: Int](/documentation/security/cssm_errcode_device_reset)
- [var CSSM_ERRCODE_FUNCTION_FAILED: Int](/documentation/security/cssm_errcode_function_failed)
- [var CSSM_ERRCODE_FUNCTION_NOT_IMPLEMENTED: Int](/documentation/security/cssm_errcode_function_not_implemented)
- [var CSSM_ERRCODE_INCOMPATIBLE_VERSION: Int](/documentation/security/cssm_errcode_incompatible_version)
- [var CSSM_ERRCODE_INSUFFICIENT_CLIENT_IDENTIFICATION: Int](/documentation/security/cssm_errcode_insufficient_client_identification)
- [var CSSM_ERRCODE_INTERNAL_ERROR: Int](/documentation/security/cssm_errcode_internal_error)
- [var CSSM_ERRCODE_INVALID_ACCESS_CREDENTIALS: Int](/documentation/security/cssm_errcode_invalid_access_credentials)
- [var CSSM_ERRCODE_INVALID_ACL_BASE_CERTS: Int](/documentation/security/cssm_errcode_invalid_acl_base_certs)
- [var CSSM_ERRCODE_INVALID_ACL_CHALLENGE_CALLBACK: Int](/documentation/security/cssm_errcode_invalid_acl_challenge_callback)
- [var CSSM_ERRCODE_INVALID_ACL_EDIT_MODE: Int](/documentation/security/cssm_errcode_invalid_acl_edit_mode)
- [var CSSM_ERRCODE_INVALID_ACL_ENTRY_TAG: Int](/documentation/security/cssm_errcode_invalid_acl_entry_tag)
- [var CSSM_ERRCODE_INVALID_ACL_SUBJECT_VALUE: Int](/documentation/security/cssm_errcode_invalid_acl_subject_value)
- [var CSSM_ERRCODE_INVALID_AC_HANDLE: Int](/documentation/security/cssm_errcode_invalid_ac_handle)
- [var CSSM_ERRCODE_INVALID_CERTGROUP_POINTER: Int](/documentation/security/cssm_errcode_invalid_certgroup_pointer)
- [var CSSM_ERRCODE_INVALID_CERT_POINTER: Int](/documentation/security/cssm_errcode_invalid_cert_pointer)
- [var CSSM_ERRCODE_INVALID_CL_HANDLE: Int](/documentation/security/cssm_errcode_invalid_cl_handle)
- [var CSSM_ERRCODE_INVALID_CONTEXT_HANDLE: Int](/documentation/security/cssm_errcode_invalid_context_handle)
- [var CSSM_ERRCODE_INVALID_CRL_POINTER: Int](/documentation/security/cssm_errcode_invalid_crl_pointer)
- [var CSSM_ERRCODE_INVALID_CRYPTO_DATA: Int](/documentation/security/cssm_errcode_invalid_crypto_data)
- [var CSSM_ERRCODE_INVALID_CSP_HANDLE: Int](/documentation/security/cssm_errcode_invalid_csp_handle)
- [var CSSM_ERRCODE_INVALID_DATA: Int](/documentation/security/cssm_errcode_invalid_data)
- [var CSSM_ERRCODE_INVALID_DB_HANDLE: Int](/documentation/security/cssm_errcode_invalid_db_handle)
- [var CSSM_ERRCODE_INVALID_DB_LIST: Int](/documentation/security/cssm_errcode_invalid_db_list)
- [var CSSM_ERRCODE_INVALID_DB_LIST_POINTER: Int](/documentation/security/cssm_errcode_invalid_db_list_pointer)
- [var CSSM_ERRCODE_INVALID_DL_HANDLE: Int](/documentation/security/cssm_errcode_invalid_dl_handle)
- [var CSSM_ERRCODE_INVALID_FIELD_POINTER: Int](/documentation/security/cssm_errcode_invalid_field_pointer)
- [var CSSM_ERRCODE_INVALID_GUID: Int](/documentation/security/cssm_errcode_invalid_guid)
- [var CSSM_ERRCODE_INVALID_INPUT_POINTER: Int](/documentation/security/cssm_errcode_invalid_input_pointer)
- [var CSSM_ERRCODE_INVALID_KR_HANDLE: Int](/documentation/security/cssm_errcode_invalid_kr_handle)
- [var CSSM_ERRCODE_INVALID_NETWORK_ADDR: Int](/documentation/security/cssm_errcode_invalid_network_addr)
- [var CSSM_ERRCODE_INVALID_NEW_ACL_ENTRY: Int](/documentation/security/cssm_errcode_invalid_new_acl_entry)
- [var CSSM_ERRCODE_INVALID_NEW_ACL_OWNER: Int](/documentation/security/cssm_errcode_invalid_new_acl_owner)
- [var CSSM_ERRCODE_INVALID_NUMBER_OF_FIELDS: Int](/documentation/security/cssm_errcode_invalid_number_of_fields)
- [var CSSM_ERRCODE_INVALID_OUTPUT_POINTER: Int](/documentation/security/cssm_errcode_invalid_output_pointer)
- [var CSSM_ERRCODE_INVALID_PASSTHROUGH_ID: Int](/documentation/security/cssm_errcode_invalid_passthrough_id)
- [var CSSM_ERRCODE_INVALID_POINTER: Int](/documentation/security/cssm_errcode_invalid_pointer)
- [var CSSM_ERRCODE_INVALID_SAMPLE_VALUE: Int](/documentation/security/cssm_errcode_invalid_sample_value)
- [var CSSM_ERRCODE_INVALID_TP_HANDLE: Int](/documentation/security/cssm_errcode_invalid_tp_handle)
- [var CSSM_ERRCODE_IN_DARK_WAKE: Int](/documentation/security/cssm_errcode_in_dark_wake)
- [var CSSM_ERRCODE_MDS_ERROR: Int](/documentation/security/cssm_errcode_mds_error)
- [var CSSM_ERRCODE_MEMORY_ERROR: Int](/documentation/security/cssm_errcode_memory_error)
- [var CSSM_ERRCODE_MODULE_MANIFEST_VERIFY_FAILED: Int](/documentation/security/cssm_errcode_module_manifest_verify_failed)
- [var CSSM_ERRCODE_NO_USER_INTERACTION: Int](/documentation/security/cssm_errcode_no_user_interaction)
- [var CSSM_ERRCODE_OBJECT_ACL_NOT_SUPPORTED: Int](/documentation/security/cssm_errcode_object_acl_not_supported)
- [var CSSM_ERRCODE_OBJECT_ACL_REQUIRED: Int](/documentation/security/cssm_errcode_object_acl_required)
- [var CSSM_ERRCODE_OBJECT_MANIP_AUTH_DENIED: Int](/documentation/security/cssm_errcode_object_manip_auth_denied)
- [var CSSM_ERRCODE_OBJECT_USE_AUTH_DENIED: Int](/documentation/security/cssm_errcode_object_use_auth_denied)
- [var CSSM_ERRCODE_OPERATION_AUTH_DENIED: Int](/documentation/security/cssm_errcode_operation_auth_denied)
- [var CSSM_ERRCODE_OS_ACCESS_DENIED: Int](/documentation/security/cssm_errcode_os_access_denied)
- [var CSSM_ERRCODE_PRIVILEGE_NOT_GRANTED: Int](/documentation/security/cssm_errcode_privilege_not_granted)
- [var CSSM_ERRCODE_SAMPLE_VALUE_NOT_SUPPORTED: Int](/documentation/security/cssm_errcode_sample_value_not_supported)
- [var CSSM_ERRCODE_SELF_CHECK_FAILED: Int](/documentation/security/cssm_errcode_self_check_failed)
- [var CSSM_ERRCODE_SERVICE_NOT_AVAILABLE: Int](/documentation/security/cssm_errcode_service_not_available)
- [var CSSM_ERRCODE_UNKNOWN_FORMAT: Int](/documentation/security/cssm_errcode_unknown_format)
- [var CSSM_ERRCODE_UNKNOWN_TAG: Int](/documentation/security/cssm_errcode_unknown_tag)
- [var CSSM_ERRCODE_USER_CANCELED: Int](/documentation/security/cssm_errcode_user_canceled)
- [var CSSM_ERRCODE_VERIFICATION_FAILURE: Int](/documentation/security/cssm_errcode_verification_failure)
- [var CSSM_ERRORCODE_COMMON_EXTENT: Int](/documentation/security/cssm_errorcode_common_extent)
- [var CSSM_ERRORCODE_CUSTOM_OFFSET: Int](/documentation/security/cssm_errorcode_custom_offset)
- [var CSSM_ERRORCODE_MODULE_EXTENT: Int](/documentation/security/cssm_errorcode_module_extent)
- [var CSSM_ESTIMATED_TIME_UNKNOWN: Int](/documentation/security/cssm_estimated_time_unknown)
- [var CSSM_EVIDENCE_FORM_APPLE_CERTGROUP: UInt32](/documentation/security/cssm_evidence_form_apple_certgroup)
- [var CSSM_EVIDENCE_FORM_APPLE_CERT_INFO: UInt32](/documentation/security/cssm_evidence_form_apple_cert_info)
- [var CSSM_EVIDENCE_FORM_APPLE_HEADER: UInt32](/documentation/security/cssm_evidence_form_apple_header)
- [var CSSM_EVIDENCE_FORM_CERT: Int](/documentation/security/cssm_evidence_form_cert)
- [var CSSM_EVIDENCE_FORM_CERT_ID: Int](/documentation/security/cssm_evidence_form_cert_id)
- [var CSSM_EVIDENCE_FORM_CRL: Int](/documentation/security/cssm_evidence_form_crl)
- [var CSSM_EVIDENCE_FORM_CRL_ID: Int](/documentation/security/cssm_evidence_form_crl_id)
- [var CSSM_EVIDENCE_FORM_CRL_NEXTTIME: Int](/documentation/security/cssm_evidence_form_crl_nexttime)
- [var CSSM_EVIDENCE_FORM_CRL_THISTIME: Int](/documentation/security/cssm_evidence_form_crl_thistime)
- [var CSSM_EVIDENCE_FORM_POLICYINFO: Int](/documentation/security/cssm_evidence_form_policyinfo)
- [var CSSM_EVIDENCE_FORM_TUPLEGROUP: Int](/documentation/security/cssm_evidence_form_tuplegroup)
- [var CSSM_EVIDENCE_FORM_UNSPECIFIC: Int](/documentation/security/cssm_evidence_form_unspecific)
- [var CSSM_EVIDENCE_FORM_VERIFIER_TIME: Int](/documentation/security/cssm_evidence_form_verifier_time)
- [var CSSM_FALSE: Int](/documentation/security/cssm_false)
- [var CSSM_FEE_CURVE_TYPE_ANSI_X9_62: Int](/documentation/security/cssm_fee_curve_type_ansi_x9_62)
- [var CSSM_FEE_CURVE_TYPE_DEFAULT: Int](/documentation/security/cssm_fee_curve_type_default)
- [var CSSM_FEE_CURVE_TYPE_MONTGOMERY: Int](/documentation/security/cssm_fee_curve_type_montgomery)
- [var CSSM_FEE_CURVE_TYPE_WEIERSTRASS: Int](/documentation/security/cssm_fee_curve_type_weierstrass)
- [var CSSM_FEE_PRIME_TYPE_DEFAULT: Int](/documentation/security/cssm_fee_prime_type_default)
- [var CSSM_FEE_PRIME_TYPE_FEE: Int](/documentation/security/cssm_fee_prime_type_fee)
- [var CSSM_FEE_PRIME_TYPE_GENERAL: Int](/documentation/security/cssm_fee_prime_type_general)
- [var CSSM_FEE_PRIME_TYPE_MERSENNE: Int](/documentation/security/cssm_fee_prime_type_mersenne)
- [var CSSM_FIELDVALUE_COMPLEX_DATA_TYPE: UInt32](/documentation/security/cssm_fieldvalue_complex_data_type)
- [var CSSM_HINT_ADDRESS_APP: Int](/documentation/security/cssm_hint_address_app)
- [var CSSM_HINT_ADDRESS_SP: Int](/documentation/security/cssm_hint_address_sp)
- [var CSSM_HINT_NONE: Int](/documentation/security/cssm_hint_none)
- [var CSSM_INVALID_HANDLE: Int](/documentation/security/cssm_invalid_handle)
- [var CSSM_KEYATTR_ALWAYS_SENSITIVE: Int](/documentation/security/cssm_keyattr_always_sensitive)
- [var CSSM_KEYATTR_EXTRACTABLE: Int](/documentation/security/cssm_keyattr_extractable)
- [var CSSM_KEYATTR_MODIFIABLE: Int](/documentation/security/cssm_keyattr_modifiable)
- [var CSSM_KEYATTR_NEVER_EXTRACTABLE: Int](/documentation/security/cssm_keyattr_never_extractable)
- [var CSSM_KEYATTR_PARTIAL: Int](/documentation/security/cssm_keyattr_partial)
- [var CSSM_KEYATTR_PERMANENT: Int](/documentation/security/cssm_keyattr_permanent)
- [var CSSM_KEYATTR_PRIVATE: Int](/documentation/security/cssm_keyattr_private)
- [var CSSM_KEYATTR_PUBLIC_KEY_ENCRYPT: Int](/documentation/security/cssm_keyattr_public_key_encrypt)
- [var CSSM_KEYATTR_RETURN_DATA: Int](/documentation/security/cssm_keyattr_return_data)
- [var CSSM_KEYATTR_RETURN_DEFAULT: Int](/documentation/security/cssm_keyattr_return_default)
- [var CSSM_KEYATTR_RETURN_NONE: Int](/documentation/security/cssm_keyattr_return_none)
- [var CSSM_KEYATTR_RETURN_REF: Int](/documentation/security/cssm_keyattr_return_ref)
- [var CSSM_KEYATTR_SENSITIVE: Int](/documentation/security/cssm_keyattr_sensitive)
- [var CSSM_KEYBLOB_OTHER: UInt32](/documentation/security/cssm_keyblob_other)
- [var CSSM_KEYBLOB_RAW: UInt32](/documentation/security/cssm_keyblob_raw)
- [var CSSM_KEYBLOB_RAW_FORMAT_BSAFE: UInt32](/documentation/security/cssm_keyblob_raw_format_bsafe)
- [var CSSM_KEYBLOB_RAW_FORMAT_CCA: UInt32](/documentation/security/cssm_keyblob_raw_format_cca)
- [var CSSM_KEYBLOB_RAW_FORMAT_FIPS186: UInt32](/documentation/security/cssm_keyblob_raw_format_fips186)
- [var CSSM_KEYBLOB_RAW_FORMAT_MSCAPI: UInt32](/documentation/security/cssm_keyblob_raw_format_mscapi)
- [var CSSM_KEYBLOB_RAW_FORMAT_NONE: UInt32](/documentation/security/cssm_keyblob_raw_format_none)
- [var CSSM_KEYBLOB_RAW_FORMAT_OCTET_STRING: UInt32](/documentation/security/cssm_keyblob_raw_format_octet_string)
- [var CSSM_KEYBLOB_RAW_FORMAT_OPENSSH: UInt32](/documentation/security/cssm_keyblob_raw_format_openssh)
- [var CSSM_KEYBLOB_RAW_FORMAT_OPENSSH2: UInt32](/documentation/security/cssm_keyblob_raw_format_openssh2)
- [var CSSM_KEYBLOB_RAW_FORMAT_OPENSSL: UInt32](/documentation/security/cssm_keyblob_raw_format_openssl)
- [var CSSM_KEYBLOB_RAW_FORMAT_OTHER: UInt32](/documentation/security/cssm_keyblob_raw_format_other)
- [var CSSM_KEYBLOB_RAW_FORMAT_PGP: UInt32](/documentation/security/cssm_keyblob_raw_format_pgp)
- [var CSSM_KEYBLOB_RAW_FORMAT_PKCS1: UInt32](/documentation/security/cssm_keyblob_raw_format_pkcs1)
- [var CSSM_KEYBLOB_RAW_FORMAT_PKCS3: UInt32](/documentation/security/cssm_keyblob_raw_format_pkcs3)
- [var CSSM_KEYBLOB_RAW_FORMAT_PKCS8: UInt32](/documentation/security/cssm_keyblob_raw_format_pkcs8)
- [var CSSM_KEYBLOB_RAW_FORMAT_SPKI: UInt32](/documentation/security/cssm_keyblob_raw_format_spki)
- [var CSSM_KEYBLOB_RAW_FORMAT_VENDOR_DEFINED: UInt32](/documentation/security/cssm_keyblob_raw_format_vendor_defined)
- [var CSSM_KEYBLOB_RAW_FORMAT_X509: UInt32](/documentation/security/cssm_keyblob_raw_format_x509)
- [var CSSM_KEYBLOB_REFERENCE: UInt32](/documentation/security/cssm_keyblob_reference)
- [var CSSM_KEYBLOB_REF_FORMAT_INTEGER: UInt32](/documentation/security/cssm_keyblob_ref_format_integer)
- [var CSSM_KEYBLOB_REF_FORMAT_OTHER: UInt32](/documentation/security/cssm_keyblob_ref_format_other)
- [var CSSM_KEYBLOB_REF_FORMAT_SPKI: UInt32](/documentation/security/cssm_keyblob_ref_format_spki)
- [var CSSM_KEYBLOB_REF_FORMAT_STRING: UInt32](/documentation/security/cssm_keyblob_ref_format_string)
- [var CSSM_KEYBLOB_WRAPPED: UInt32](/documentation/security/cssm_keyblob_wrapped)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_APPLE_CUSTOM: Int](/documentation/security/cssm_keyblob_wrapped_format_apple_custom)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_MSCAPI: UInt32](/documentation/security/cssm_keyblob_wrapped_format_mscapi)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_NONE: UInt32](/documentation/security/cssm_keyblob_wrapped_format_none)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_OPENSSH1: Int](/documentation/security/cssm_keyblob_wrapped_format_openssh1)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_OPENSSL: Int](/documentation/security/cssm_keyblob_wrapped_format_openssl)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_OTHER: UInt32](/documentation/security/cssm_keyblob_wrapped_format_other)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_PKCS7: UInt32](/documentation/security/cssm_keyblob_wrapped_format_pkcs7)
- [var CSSM_KEYBLOB_WRAPPED_FORMAT_PKCS8: UInt32](/documentation/security/cssm_keyblob_wrapped_format_pkcs8)
- [var CSSM_KEYCLASS_OTHER: UInt32](/documentation/security/cssm_keyclass_other)
- [var CSSM_KEYCLASS_PRIVATE_KEY: UInt32](/documentation/security/cssm_keyclass_private_key)
- [var CSSM_KEYCLASS_PUBLIC_KEY: UInt32](/documentation/security/cssm_keyclass_public_key)
- [var CSSM_KEYCLASS_SECRET_PART: UInt32](/documentation/security/cssm_keyclass_secret_part)
- [var CSSM_KEYCLASS_SESSION_KEY: UInt32](/documentation/security/cssm_keyclass_session_key)
- [var CSSM_KEYHEADER_VERSION: Int](/documentation/security/cssm_keyheader_version)
- [var CSSM_KEYUSE_ANY: UInt32](/documentation/security/cssm_keyuse_any)
- [var CSSM_KEYUSE_DECRYPT: UInt32](/documentation/security/cssm_keyuse_decrypt)
- [var CSSM_KEYUSE_DERIVE: UInt32](/documentation/security/cssm_keyuse_derive)
- [var CSSM_KEYUSE_ENCRYPT: UInt32](/documentation/security/cssm_keyuse_encrypt)
- [var CSSM_KEYUSE_SIGN: UInt32](/documentation/security/cssm_keyuse_sign)
- [var CSSM_KEYUSE_SIGN_RECOVER: UInt32](/documentation/security/cssm_keyuse_sign_recover)
- [var CSSM_KEYUSE_UNWRAP: UInt32](/documentation/security/cssm_keyuse_unwrap)
- [var CSSM_KEYUSE_VERIFY: UInt32](/documentation/security/cssm_keyuse_verify)
- [var CSSM_KEYUSE_VERIFY_RECOVER: UInt32](/documentation/security/cssm_keyuse_verify_recover)
- [var CSSM_KEYUSE_WRAP: UInt32](/documentation/security/cssm_keyuse_wrap)
- [var CSSM_KEY_HIERARCHY_EXPORT: Int](/documentation/security/cssm_key_hierarchy_export)
- [var CSSM_KEY_HIERARCHY_INTEG: Int](/documentation/security/cssm_key_hierarchy_integ)
- [var CSSM_KEY_HIERARCHY_NONE: Int](/documentation/security/cssm_key_hierarchy_none)
- [var CSSM_KR_BASE_ERROR: Int](/documentation/security/cssm_kr_base_error)
- [var CSSM_KR_PRIVATE_ERROR: Int](/documentation/security/cssm_kr_private_error)
- [var CSSM_LIST_ELEMENT_DATUM: Int](/documentation/security/cssm_list_element_datum)
- [var CSSM_LIST_ELEMENT_SUBLIST: Int](/documentation/security/cssm_list_element_sublist)
- [var CSSM_LIST_ELEMENT_WORDID: Int](/documentation/security/cssm_list_element_wordid)
- [var CSSM_LIST_TYPE_CUSTOM: Int](/documentation/security/cssm_list_type_custom)
- [var CSSM_LIST_TYPE_SEXPR: Int](/documentation/security/cssm_list_type_sexpr)
- [var CSSM_LIST_TYPE_UNKNOWN: Int](/documentation/security/cssm_list_type_unknown)
- [var CSSM_MDS_BASE_ERROR: Int](/documentation/security/cssm_mds_base_error)
- [var CSSM_MDS_PRIVATE_ERROR: Int](/documentation/security/cssm_mds_private_error)
- [var CSSM_MODULE_STRING_SIZE: Int](/documentation/security/cssm_module_string_size)
- [var CSSM_NET_PROTO_CMP: Int](/documentation/security/cssm_net_proto_cmp)
- [var CSSM_NET_PROTO_CMPS: Int](/documentation/security/cssm_net_proto_cmps)
- [var CSSM_NET_PROTO_CUSTOM: Int](/documentation/security/cssm_net_proto_custom)
- [var CSSM_NET_PROTO_FTP: Int](/documentation/security/cssm_net_proto_ftp)
- [var CSSM_NET_PROTO_FTPS: Int](/documentation/security/cssm_net_proto_ftps)
- [var CSSM_NET_PROTO_LDAP: Int](/documentation/security/cssm_net_proto_ldap)
- [var CSSM_NET_PROTO_LDAPNS: Int](/documentation/security/cssm_net_proto_ldapns)
- [var CSSM_NET_PROTO_LDAPS: Int](/documentation/security/cssm_net_proto_ldaps)
- [var CSSM_NET_PROTO_NONE: Int](/documentation/security/cssm_net_proto_none)
- [var CSSM_NET_PROTO_OCSP: Int](/documentation/security/cssm_net_proto_ocsp)
- [var CSSM_NET_PROTO_UNSPECIFIED: Int](/documentation/security/cssm_net_proto_unspecified)
- [var CSSM_NET_PROTO_X500DAP: Int](/documentation/security/cssm_net_proto_x500dap)
- [var CSSM_NOTIFY_FAULT: Int](/documentation/security/cssm_notify_fault)
- [var CSSM_NOTIFY_INSERT: Int](/documentation/security/cssm_notify_insert)
- [var CSSM_NOTIFY_REMOVE: Int](/documentation/security/cssm_notify_remove)
- [var CSSM_OK: Int](/documentation/security/cssm_ok)
- [var CSSM_PADDING_ALTERNATE: UInt32](/documentation/security/cssm_padding_alternate)
- [var CSSM_PADDING_APPLE_SSLv2: UInt32](/documentation/security/cssm_padding_apple_sslv2)
- [var CSSM_PADDING_CIPHERSTEALING: UInt32](/documentation/security/cssm_padding_cipherstealing)
- [var CSSM_PADDING_CUSTOM: UInt32](/documentation/security/cssm_padding_custom)
- [var CSSM_PADDING_FF: UInt32](/documentation/security/cssm_padding_ff)
- [var CSSM_PADDING_NONE: UInt32](/documentation/security/cssm_padding_none)
- [var CSSM_PADDING_ONE: UInt32](/documentation/security/cssm_padding_one)
- [var CSSM_PADDING_PKCS1: UInt32](/documentation/security/cssm_padding_pkcs1)
- [var CSSM_PADDING_PKCS5: UInt32](/documentation/security/cssm_padding_pkcs5)
- [var CSSM_PADDING_PKCS7: UInt32](/documentation/security/cssm_padding_pkcs7)
- [var CSSM_PADDING_RANDOM: UInt32](/documentation/security/cssm_padding_random)
- [var CSSM_PADDING_SIGRAW: UInt32](/documentation/security/cssm_padding_sigraw)
- [var CSSM_PADDING_VENDOR_DEFINED: UInt32](/documentation/security/cssm_padding_vendor_defined)
- [var CSSM_PADDING_ZERO: UInt32](/documentation/security/cssm_padding_zero)
- [var CSSM_PKCS5_PBKDF2_PRF_HMAC_SHA1: Int](/documentation/security/cssm_pkcs5_pbkdf2_prf_hmac_sha1)
- [var CSSM_PKCS_OAEP_MGF1_MD5: Int](/documentation/security/cssm_pkcs_oaep_mgf1_md5)
- [var CSSM_PKCS_OAEP_MGF1_SHA1: Int](/documentation/security/cssm_pkcs_oaep_mgf1_sha1)
- [var CSSM_PKCS_OAEP_MGF_NONE: Int](/documentation/security/cssm_pkcs_oaep_mgf_none)
- [var CSSM_PKCS_OAEP_PSOURCE_NONE: Int](/documentation/security/cssm_pkcs_oaep_psource_none)
- [var CSSM_PKCS_OAEP_PSOURCE_Pspecified: Int](/documentation/security/cssm_pkcs_oaep_psource_pspecified)
- [var CSSM_PRIVILEGE_SCOPE_NONE: Int](/documentation/security/cssm_privilege_scope_none)
- [var CSSM_PRIVILEGE_SCOPE_PROCESS: Int](/documentation/security/cssm_privilege_scope_process)
- [var CSSM_PRIVILEGE_SCOPE_THREAD: Int](/documentation/security/cssm_privilege_scope_thread)
- [var CSSM_PVC_APP: Int](/documentation/security/cssm_pvc_app)
- [var CSSM_PVC_NONE: Int](/documentation/security/cssm_pvc_none)
- [var CSSM_PVC_SP: Int](/documentation/security/cssm_pvc_sp)
- [var CSSM_QUERY_RETURN_DATA: Int](/documentation/security/cssm_query_return_data)
- [var CSSM_QUERY_SIZELIMIT_NONE: Int](/documentation/security/cssm_query_sizelimit_none)
- [var CSSM_QUERY_TIMELIMIT_NONE: Int](/documentation/security/cssm_query_timelimit_none)
- [var CSSM_SAMPLE_TYPE_ASYMMETRIC_KEY: Int](/documentation/security/cssm_sample_type_asymmetric_key)
- [var CSSM_SAMPLE_TYPE_BIOMETRIC: Int](/documentation/security/cssm_sample_type_biometric)
- [var CSSM_SAMPLE_TYPE_COMMENT: Int](/documentation/security/cssm_sample_type_comment)
- [var CSSM_SAMPLE_TYPE_HASHED_PASSWORD: Int](/documentation/security/cssm_sample_type_hashed_password)
- [var CSSM_SAMPLE_TYPE_KEYBAG_KEY: Int](/documentation/security/cssm_sample_type_keybag_key)
- [var CSSM_SAMPLE_TYPE_KEYCHAIN_CHANGE_LOCK: Int](/documentation/security/cssm_sample_type_keychain_change_lock)
- [var CSSM_SAMPLE_TYPE_KEYCHAIN_LOCK: Int](/documentation/security/cssm_sample_type_keychain_lock)
- [var CSSM_SAMPLE_TYPE_KEYCHAIN_PROMPT: Int](/documentation/security/cssm_sample_type_keychain_prompt)
- [var CSSM_SAMPLE_TYPE_PASSWORD: Int](/documentation/security/cssm_sample_type_password)
- [var CSSM_SAMPLE_TYPE_PREAUTH: Int](/documentation/security/cssm_sample_type_preauth)
- [var CSSM_SAMPLE_TYPE_PROCESS: Int](/documentation/security/cssm_sample_type_process)
- [var CSSM_SAMPLE_TYPE_PROMPTED_BIOMETRIC: Int](/documentation/security/cssm_sample_type_prompted_biometric)
- [var CSSM_SAMPLE_TYPE_PROMPTED_PASSWORD: Int](/documentation/security/cssm_sample_type_prompted_password)
- [var CSSM_SAMPLE_TYPE_PROTECTED_BIOMETRIC: Int](/documentation/security/cssm_sample_type_protected_biometric)
- [var CSSM_SAMPLE_TYPE_PROTECTED_PASSWORD: Int](/documentation/security/cssm_sample_type_protected_password)
- [var CSSM_SAMPLE_TYPE_RETRY_ID: Int](/documentation/security/cssm_sample_type_retry_id)
- [var CSSM_SAMPLE_TYPE_SIGNED_NONCE: Int](/documentation/security/cssm_sample_type_signed_nonce)
- [var CSSM_SAMPLE_TYPE_SIGNED_SECRET: Int](/documentation/security/cssm_sample_type_signed_secret)
- [var CSSM_SAMPLE_TYPE_SYMMETRIC_KEY: Int](/documentation/security/cssm_sample_type_symmetric_key)
- [var CSSM_SAMPLE_TYPE_THRESHOLD: Int](/documentation/security/cssm_sample_type_threshold)
- [var CSSM_SERVICE_AC: Int](/documentation/security/cssm_service_ac)
- [var CSSM_SERVICE_CL: Int](/documentation/security/cssm_service_cl)
- [var CSSM_SERVICE_CSP: Int](/documentation/security/cssm_service_csp)
- [var CSSM_SERVICE_CSSM: Int](/documentation/security/cssm_service_cssm)
- [var CSSM_SERVICE_DL: Int](/documentation/security/cssm_service_dl)
- [var CSSM_SERVICE_KR: Int](/documentation/security/cssm_service_kr)
- [var CSSM_SERVICE_TP: Int](/documentation/security/cssm_service_tp)
- [var CSSM_TP_ACTION_ALLOW_EXPIRED: Int](/documentation/security/cssm_tp_action_allow_expired)
- [var CSSM_TP_ACTION_ALLOW_EXPIRED_ROOT: Int](/documentation/security/cssm_tp_action_allow_expired_root)
- [var CSSM_TP_ACTION_CRL_SUFFICIENT: Int](/documentation/security/cssm_tp_action_crl_sufficient)
- [var CSSM_TP_ACTION_DEFAULT: Int](/documentation/security/cssm_tp_action_default)
- [var CSSM_TP_ACTION_FETCH_CERT_FROM_NET: Int](/documentation/security/cssm_tp_action_fetch_cert_from_net)
- [var CSSM_TP_ACTION_FETCH_CRL_FROM_NET: Int](/documentation/security/cssm_tp_action_fetch_crl_from_net)
- [var CSSM_TP_ACTION_IMPLICIT_ANCHORS: Int](/documentation/security/cssm_tp_action_implicit_anchors)
- [var CSSM_TP_ACTION_LEAF_IS_CA: Int](/documentation/security/cssm_tp_action_leaf_is_ca)
- [var CSSM_TP_ACTION_REQUIRE_CRL_IF_PRESENT: Int](/documentation/security/cssm_tp_action_require_crl_if_present)
- [var CSSM_TP_ACTION_REQUIRE_CRL_PER_CERT: Int](/documentation/security/cssm_tp_action_require_crl_per_cert)
- [var CSSM_TP_ACTION_REQUIRE_REV_PER_CERT: Int](/documentation/security/cssm_tp_action_require_rev_per_cert)
- [var CSSM_TP_ACTION_TRUST_SETTINGS: Int](/documentation/security/cssm_tp_action_trust_settings)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTISSUE: Int](/documentation/security/cssm_tp_authority_request_certissue)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTNOTARIZE: Int](/documentation/security/cssm_tp_authority_request_certnotarize)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTRESUME: Int](/documentation/security/cssm_tp_authority_request_certresume)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTREVOKE: Int](/documentation/security/cssm_tp_authority_request_certrevoke)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTSUSPEND: Int](/documentation/security/cssm_tp_authority_request_certsuspend)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTUSERECOVER: Int](/documentation/security/cssm_tp_authority_request_certuserecover)
- [var CSSM_TP_AUTHORITY_REQUEST_CERTVERIFY: Int](/documentation/security/cssm_tp_authority_request_certverify)
- [var CSSM_TP_AUTHORITY_REQUEST_CRLISSUE: Int](/documentation/security/cssm_tp_authority_request_crlissue)
- [var CSSM_TP_BASE_ERROR: Int](/documentation/security/cssm_tp_base_error)
- [var CSSM_TP_BASE_TP_ERROR: Int](/documentation/security/cssm_tp_base_tp_error)
- [var CSSM_TP_CERTCHANGE_HOLD: Int](/documentation/security/cssm_tp_certchange_hold)
- [var CSSM_TP_CERTCHANGE_NONE: Int](/documentation/security/cssm_tp_certchange_none)
- [var CSSM_TP_CERTCHANGE_NOT_AUTHORIZED: Int](/documentation/security/cssm_tp_certchange_not_authorized)
- [var CSSM_TP_CERTCHANGE_OK: Int](/documentation/security/cssm_tp_certchange_ok)
- [var CSSM_TP_CERTCHANGE_OKWITHNEWTIME: Int](/documentation/security/cssm_tp_certchange_okwithnewtime)
- [var CSSM_TP_CERTCHANGE_REASON_AFFILIATIONCHANGE: Int](/documentation/security/cssm_tp_certchange_reason_affiliationchange)
- [var CSSM_TP_CERTCHANGE_REASON_CACOMPROMISE: Int](/documentation/security/cssm_tp_certchange_reason_cacompromise)
- [var CSSM_TP_CERTCHANGE_REASON_CEASEOPERATION: Int](/documentation/security/cssm_tp_certchange_reason_ceaseoperation)
- [var CSSM_TP_CERTCHANGE_REASON_HOLDRELEASE: Int](/documentation/security/cssm_tp_certchange_reason_holdrelease)
- [var CSSM_TP_CERTCHANGE_REASON_KEYCOMPROMISE: Int](/documentation/security/cssm_tp_certchange_reason_keycompromise)
- [var CSSM_TP_CERTCHANGE_REASON_SUPERCEDED: Int](/documentation/security/cssm_tp_certchange_reason_superceded)
- [var CSSM_TP_CERTCHANGE_REASON_SUSPECTEDCOMPROMISE: Int](/documentation/security/cssm_tp_certchange_reason_suspectedcompromise)
- [var CSSM_TP_CERTCHANGE_REASON_UNKNOWN: Int](/documentation/security/cssm_tp_certchange_reason_unknown)
- [var CSSM_TP_CERTCHANGE_REJECTED: Int](/documentation/security/cssm_tp_certchange_rejected)
- [var CSSM_TP_CERTCHANGE_RELEASE: Int](/documentation/security/cssm_tp_certchange_release)
- [var CSSM_TP_CERTCHANGE_REVOKE: Int](/documentation/security/cssm_tp_certchange_revoke)
- [var CSSM_TP_CERTCHANGE_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_certchange_status_unknown)
- [var CSSM_TP_CERTCHANGE_WRONGCA: Int](/documentation/security/cssm_tp_certchange_wrongca)
- [var CSSM_TP_CERTISSUE_NOT_AUTHORIZED: Int](/documentation/security/cssm_tp_certissue_not_authorized)
- [var CSSM_TP_CERTISSUE_OK: Int](/documentation/security/cssm_tp_certissue_ok)
- [var CSSM_TP_CERTISSUE_OKWITHCERTMODS: Int](/documentation/security/cssm_tp_certissue_okwithcertmods)
- [var CSSM_TP_CERTISSUE_OKWITHSERVICEMODS: Int](/documentation/security/cssm_tp_certissue_okwithservicemods)
- [var CSSM_TP_CERTISSUE_REJECTED: Int](/documentation/security/cssm_tp_certissue_rejected)
- [var CSSM_TP_CERTISSUE_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_certissue_status_unknown)
- [var CSSM_TP_CERTISSUE_WILL_BE_REVOKED: Int](/documentation/security/cssm_tp_certissue_will_be_revoked)
- [var CSSM_TP_CERTNOTARIZE_NOT_AUTHORIZED: Int](/documentation/security/cssm_tp_certnotarize_not_authorized)
- [var CSSM_TP_CERTNOTARIZE_OK: Int](/documentation/security/cssm_tp_certnotarize_ok)
- [var CSSM_TP_CERTNOTARIZE_OKWITHOUTFIELDS: Int](/documentation/security/cssm_tp_certnotarize_okwithoutfields)
- [var CSSM_TP_CERTNOTARIZE_OKWITHSERVICEMODS: Int](/documentation/security/cssm_tp_certnotarize_okwithservicemods)
- [var CSSM_TP_CERTNOTARIZE_REJECTED: Int](/documentation/security/cssm_tp_certnotarize_rejected)
- [var CSSM_TP_CERTNOTARIZE_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_certnotarize_status_unknown)
- [var CSSM_TP_CERTRECLAIM_NOMATCH: Int](/documentation/security/cssm_tp_certreclaim_nomatch)
- [var CSSM_TP_CERTRECLAIM_NOT_AUTHORIZED: Int](/documentation/security/cssm_tp_certreclaim_not_authorized)
- [var CSSM_TP_CERTRECLAIM_OK: Int](/documentation/security/cssm_tp_certreclaim_ok)
- [var CSSM_TP_CERTRECLAIM_REJECTED: Int](/documentation/security/cssm_tp_certreclaim_rejected)
- [var CSSM_TP_CERTRECLAIM_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_certreclaim_status_unknown)
- [var CSSM_TP_CERTVERIFY_EXPIRED: Int](/documentation/security/cssm_tp_certverify_expired)
- [var CSSM_TP_CERTVERIFY_INVALID: Int](/documentation/security/cssm_tp_certverify_invalid)
- [var CSSM_TP_CERTVERIFY_INVALID_AUTHORITY: Int](/documentation/security/cssm_tp_certverify_invalid_authority)
- [var CSSM_TP_CERTVERIFY_INVALID_BASIC_CONSTRAINTS: Int](/documentation/security/cssm_tp_certverify_invalid_basic_constraints)
- [var CSSM_TP_CERTVERIFY_INVALID_CERTGROUP: Int](/documentation/security/cssm_tp_certverify_invalid_certgroup)
- [var CSSM_TP_CERTVERIFY_INVALID_CERT_VALUE: Int](/documentation/security/cssm_tp_certverify_invalid_cert_value)
- [var CSSM_TP_CERTVERIFY_INVALID_CRL_DIST_PT: Int](/documentation/security/cssm_tp_certverify_invalid_crl_dist_pt)
- [var CSSM_TP_CERTVERIFY_INVALID_NAME_TREE: Int](/documentation/security/cssm_tp_certverify_invalid_name_tree)
- [var CSSM_TP_CERTVERIFY_INVALID_POLICY: Int](/documentation/security/cssm_tp_certverify_invalid_policy)
- [var CSSM_TP_CERTVERIFY_INVALID_POLICY_IDS: Int](/documentation/security/cssm_tp_certverify_invalid_policy_ids)
- [var CSSM_TP_CERTVERIFY_INVALID_SIGNATURE: Int](/documentation/security/cssm_tp_certverify_invalid_signature)
- [var CSSM_TP_CERTVERIFY_NOT_VALID_YET: Int](/documentation/security/cssm_tp_certverify_not_valid_yet)
- [var CSSM_TP_CERTVERIFY_REVOKED: Int](/documentation/security/cssm_tp_certverify_revoked)
- [var CSSM_TP_CERTVERIFY_SUSPENDED: Int](/documentation/security/cssm_tp_certverify_suspended)
- [var CSSM_TP_CERTVERIFY_UNKNOWN: Int](/documentation/security/cssm_tp_certverify_unknown)
- [var CSSM_TP_CERTVERIFY_UNKNOWN_CRITICAL_EXT: Int](/documentation/security/cssm_tp_certverify_unknown_critical_ext)
- [var CSSM_TP_CERTVERIFY_VALID: Int](/documentation/security/cssm_tp_certverify_valid)
- [var CSSM_TP_CERT_DIR_UPDATE: Int](/documentation/security/cssm_tp_cert_dir_update)
- [var CSSM_TP_CERT_NOTIFY_RENEW: Int](/documentation/security/cssm_tp_cert_notify_renew)
- [var CSSM_TP_CERT_PUBLISH: Int](/documentation/security/cssm_tp_cert_publish)
- [var CSSM_TP_CONFIRM_ACCEPT: Int](/documentation/security/cssm_tp_confirm_accept)
- [var CSSM_TP_CONFIRM_REJECT: Int](/documentation/security/cssm_tp_confirm_reject)
- [var CSSM_TP_CONFIRM_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_confirm_status_unknown)
- [var CSSM_TP_CRLISSUE_INVALID_DOMAIN: Int](/documentation/security/cssm_tp_crlissue_invalid_domain)
- [var CSSM_TP_CRLISSUE_NOT_AUTHORIZED: Int](/documentation/security/cssm_tp_crlissue_not_authorized)
- [var CSSM_TP_CRLISSUE_NOT_CURRENT: Int](/documentation/security/cssm_tp_crlissue_not_current)
- [var CSSM_TP_CRLISSUE_OK: Int](/documentation/security/cssm_tp_crlissue_ok)
- [var CSSM_TP_CRLISSUE_REJECTED: Int](/documentation/security/cssm_tp_crlissue_rejected)
- [var CSSM_TP_CRLISSUE_STATUS_UNKNOWN: Int](/documentation/security/cssm_tp_crlissue_status_unknown)
- [var CSSM_TP_CRLISSUE_UNKNOWN_IDENTIFIER: Int](/documentation/security/cssm_tp_crlissue_unknown_identifier)
- [var CSSM_TP_CRL_DISTRIBUTE: Int](/documentation/security/cssm_tp_crl_distribute)
- [var CSSM_TP_FORM_TYPE_GENERIC: Int](/documentation/security/cssm_tp_form_type_generic)
- [var CSSM_TP_FORM_TYPE_REGISTRATION: Int](/documentation/security/cssm_tp_form_type_registration)
- [var CSSM_TP_KEY_ARCHIVE: Int](/documentation/security/cssm_tp_key_archive)
- [var CSSM_TP_PRIVATE_ERROR: Int](/documentation/security/cssm_tp_private_error)
- [var CSSM_TP_STOP_ON_FIRST_FAIL: Int](/documentation/security/cssm_tp_stop_on_first_fail)
- [var CSSM_TP_STOP_ON_FIRST_PASS: Int](/documentation/security/cssm_tp_stop_on_first_pass)
- [var CSSM_TP_STOP_ON_NONE: Int](/documentation/security/cssm_tp_stop_on_none)
- [var CSSM_TP_STOP_ON_POLICY: Int](/documentation/security/cssm_tp_stop_on_policy)
- [var CSSM_TRUE: Int](/documentation/security/cssm_true)
- [var CSSM_USEE_AUTHENTICATION: Int](/documentation/security/cssm_usee_authentication)
- [var CSSM_USEE_DOMESTIC: Int](/documentation/security/cssm_usee_domestic)
- [var CSSM_USEE_FINANCIAL: Int](/documentation/security/cssm_usee_financial)
- [var CSSM_USEE_INSURANCE: Int](/documentation/security/cssm_usee_insurance)
- [var CSSM_USEE_KEYEXCH: Int](/documentation/security/cssm_usee_keyexch)
- [var CSSM_USEE_KRENT: Int](/documentation/security/cssm_usee_krent)
- [var CSSM_USEE_KRLE: Int](/documentation/security/cssm_usee_krle)
- [var CSSM_USEE_LAST: Int](/documentation/security/cssm_usee_last)
- [var CSSM_USEE_MEDICAL: Int](/documentation/security/cssm_usee_medical)
- [var CSSM_USEE_NONE: Int](/documentation/security/cssm_usee_none)
- [var CSSM_USEE_SSL: Int](/documentation/security/cssm_usee_ssl)
- [var CSSM_USEE_WEAK: Int](/documentation/security/cssm_usee_weak)
- [var CSSM_VALUE_NOT_AVAILABLE: Int](/documentation/security/cssm_value_not_available)
- [var CSSM_WORDID_A: Int](/documentation/security/cssm_wordid_a)
- [var CSSM_WORDID_ACL: Int](/documentation/security/cssm_wordid_acl)
- [var CSSM_WORDID_ALPHA: Int](/documentation/security/cssm_wordid_alpha)
- [var CSSM_WORDID_ASYMMETRIC_KEY: Int](/documentation/security/cssm_wordid_asymmetric_key)
- [var CSSM_WORDID_B: Int](/documentation/security/cssm_wordid_b)
- [var CSSM_WORDID_BER: Int](/documentation/security/cssm_wordid_ber)
- [var CSSM_WORDID_BINARY: Int](/documentation/security/cssm_wordid_binary)
- [var CSSM_WORDID_BIOMETRIC: Int](/documentation/security/cssm_wordid_biometric)
- [var CSSM_WORDID_C: Int](/documentation/security/cssm_wordid_c)
- [var CSSM_WORDID_CANCELED: Int](/documentation/security/cssm_wordid_canceled)
- [var CSSM_WORDID_CERT: Int](/documentation/security/cssm_wordid_cert)
- [var CSSM_WORDID_COMMENT: Int](/documentation/security/cssm_wordid_comment)
- [var CSSM_WORDID_CRL: Int](/documentation/security/cssm_wordid_crl)
- [var CSSM_WORDID_CUSTOM: Int](/documentation/security/cssm_wordid_custom)
- [var CSSM_WORDID_D: Int](/documentation/security/cssm_wordid_d)
- [var CSSM_WORDID_DATE: Int](/documentation/security/cssm_wordid_date)
- [var CSSM_WORDID_DBS_CREATE: Int](/documentation/security/cssm_wordid_dbs_create)
- [var CSSM_WORDID_DBS_DELETE: Int](/documentation/security/cssm_wordid_dbs_delete)
- [var CSSM_WORDID_DB_DELETE: Int](/documentation/security/cssm_wordid_db_delete)
- [var CSSM_WORDID_DB_EXEC_STORED_QUERY: Int](/documentation/security/cssm_wordid_db_exec_stored_query)
- [var CSSM_WORDID_DB_INSERT: Int](/documentation/security/cssm_wordid_db_insert)
- [var CSSM_WORDID_DB_MODIFY: Int](/documentation/security/cssm_wordid_db_modify)
- [var CSSM_WORDID_DB_READ: Int](/documentation/security/cssm_wordid_db_read)
- [var CSSM_WORDID_DECRYPT: Int](/documentation/security/cssm_wordid_decrypt)
- [var CSSM_WORDID_DELETE: Int](/documentation/security/cssm_wordid_delete)
- [var CSSM_WORDID_DELTA_CRL: Int](/documentation/security/cssm_wordid_delta_crl)
- [var CSSM_WORDID_DER: Int](/documentation/security/cssm_wordid_der)
- [var CSSM_WORDID_DERIVE: Int](/documentation/security/cssm_wordid_derive)
- [var CSSM_WORDID_DISPLAY: Int](/documentation/security/cssm_wordid_display)
- [var CSSM_WORDID_DO: Int](/documentation/security/cssm_wordid_do)
- [var CSSM_WORDID_DSA: Int](/documentation/security/cssm_wordid_dsa)
- [var CSSM_WORDID_DSA_SHA1: Int](/documentation/security/cssm_wordid_dsa_sha1)
- [var CSSM_WORDID_E: Int](/documentation/security/cssm_wordid_e)
- [var CSSM_WORDID_ELGAMAL: Int](/documentation/security/cssm_wordid_elgamal)
- [var CSSM_WORDID_ENCRYPT: Int](/documentation/security/cssm_wordid_encrypt)
- [var CSSM_WORDID_ENTRY: Int](/documentation/security/cssm_wordid_entry)
- [var CSSM_WORDID_EXPORT_CLEAR: Int](/documentation/security/cssm_wordid_export_clear)
- [var CSSM_WORDID_EXPORT_WRAPPED: Int](/documentation/security/cssm_wordid_export_wrapped)
- [var CSSM_WORDID_G: Int](/documentation/security/cssm_wordid_g)
- [var CSSM_WORDID_GE: Int](/documentation/security/cssm_wordid_ge)
- [var CSSM_WORDID_GENKEY: Int](/documentation/security/cssm_wordid_genkey)
- [var CSSM_WORDID_HASH: Int](/documentation/security/cssm_wordid_hash)
- [var CSSM_WORDID_HASHED_PASSWORD: Int](/documentation/security/cssm_wordid_hashed_password)
- [var CSSM_WORDID_HASHED_SUBJECT: Int](/documentation/security/cssm_wordid_hashed_subject)
- [var CSSM_WORDID_HAVAL: Int](/documentation/security/cssm_wordid_haval)
- [var CSSM_WORDID_IBCHASH: Int](/documentation/security/cssm_wordid_ibchash)
- [var CSSM_WORDID_IMPORT_CLEAR: Int](/documentation/security/cssm_wordid_import_clear)
- [var CSSM_WORDID_IMPORT_WRAPPED: Int](/documentation/security/cssm_wordid_import_wrapped)
- [var CSSM_WORDID_INTEL: Int](/documentation/security/cssm_wordid_intel)
- [var CSSM_WORDID_ISSUER: Int](/documentation/security/cssm_wordid_issuer)
- [var CSSM_WORDID_ISSUER_INFO: Int](/documentation/security/cssm_wordid_issuer_info)
- [var CSSM_WORDID_KEA: Int](/documentation/security/cssm_wordid_kea)
- [var CSSM_WORDID_KEY: Int](/documentation/security/cssm_wordid_key)
- [var CSSM_WORDID_KEYBAG_KEY: Int](/documentation/security/cssm_wordid_keybag_key)
- [var CSSM_WORDID_KEYCHAIN_CHANGE_LOCK: Int](/documentation/security/cssm_wordid_keychain_change_lock)
- [var CSSM_WORDID_KEYCHAIN_LOCK: Int](/documentation/security/cssm_wordid_keychain_lock)
- [var CSSM_WORDID_KEYCHAIN_PROMPT: Int](/documentation/security/cssm_wordid_keychain_prompt)
- [var CSSM_WORDID_KEYHOLDER: Int](/documentation/security/cssm_wordid_keyholder)
- [var CSSM_WORDID_K_OF_N: Int](/documentation/security/cssm_wordid_k_of_n)
- [var CSSM_WORDID_L: Int](/documentation/security/cssm_wordid_l)
- [var CSSM_WORDID_LE: Int](/documentation/security/cssm_wordid_le)
- [var CSSM_WORDID_LOGIN: Int](/documentation/security/cssm_wordid_login)
- [var CSSM_WORDID_LOGIN_NAME: Int](/documentation/security/cssm_wordid_login_name)
- [var CSSM_WORDID_MAC: Int](/documentation/security/cssm_wordid_mac)
- [var CSSM_WORDID_MD2: Int](/documentation/security/cssm_wordid_md2)
- [var CSSM_WORDID_MD2WITHRSA: Int](/documentation/security/cssm_wordid_md2withrsa)
- [var CSSM_WORDID_MD4: Int](/documentation/security/cssm_wordid_md4)
- [var CSSM_WORDID_MD5: Int](/documentation/security/cssm_wordid_md5)
- [var CSSM_WORDID_MD5WITHRSA: Int](/documentation/security/cssm_wordid_md5withrsa)
- [var CSSM_WORDID_N: Int](/documentation/security/cssm_wordid_n)
- [var CSSM_WORDID_NAME: Int](/documentation/security/cssm_wordid_name)
- [var CSSM_WORDID_NDR: Int](/documentation/security/cssm_wordid_ndr)
- [var CSSM_WORDID_NHASH: Int](/documentation/security/cssm_wordid_nhash)
- [var CSSM_WORDID_NOT_AFTER: Int](/documentation/security/cssm_wordid_not_after)
- [var CSSM_WORDID_NOT_BEFORE: Int](/documentation/security/cssm_wordid_not_before)
- [var CSSM_WORDID_NULL: Int](/documentation/security/cssm_wordid_null)
- [var CSSM_WORDID_NUMERIC: Int](/documentation/security/cssm_wordid_numeric)
- [var CSSM_WORDID_OBJECT_HASH: Int](/documentation/security/cssm_wordid_object_hash)
- [var CSSM_WORDID_ONE_TIME: Int](/documentation/security/cssm_wordid_one_time)
- [var CSSM_WORDID_ONLINE: Int](/documentation/security/cssm_wordid_online)
- [var CSSM_WORDID_OWNER: Int](/documentation/security/cssm_wordid_owner)
- [var CSSM_WORDID_P: Int](/documentation/security/cssm_wordid_p)
- [var CSSM_WORDID_PAM_NAME: Int](/documentation/security/cssm_wordid_pam_name)
- [var CSSM_WORDID_PARTITION: Int](/documentation/security/cssm_wordid_partition)
- [var CSSM_WORDID_PASSWORD: Int](/documentation/security/cssm_wordid_password)
- [var CSSM_WORDID_PGP: Int](/documentation/security/cssm_wordid_pgp)
- [var CSSM_WORDID_PIN: Int](/documentation/security/cssm_wordid_pin)
- [var CSSM_WORDID_PREAUTH: Int](/documentation/security/cssm_wordid_preauth)
- [var CSSM_WORDID_PREAUTH_SOURCE: Int](/documentation/security/cssm_wordid_preauth_source)
- [var CSSM_WORDID_PREFIX: Int](/documentation/security/cssm_wordid_prefix)
- [var CSSM_WORDID_PRIVATE_KEY: Int](/documentation/security/cssm_wordid_private_key)
- [var CSSM_WORDID_PROCESS: Int](/documentation/security/cssm_wordid_process)
- [var CSSM_WORDID_PROMPTED_BIOMETRIC: Int](/documentation/security/cssm_wordid_prompted_biometric)
- [var CSSM_WORDID_PROMPTED_PASSWORD: Int](/documentation/security/cssm_wordid_prompted_password)
- [var CSSM_WORDID_PROPAGATE: Int](/documentation/security/cssm_wordid_propagate)
- [var CSSM_WORDID_PROTECTED_BIOMETRIC: Int](/documentation/security/cssm_wordid_protected_biometric)
- [var CSSM_WORDID_PROTECTED_PASSWORD: Int](/documentation/security/cssm_wordid_protected_password)
- [var CSSM_WORDID_PROTECTED_PIN: Int](/documentation/security/cssm_wordid_protected_pin)
- [var CSSM_WORDID_PUBLIC_KEY: Int](/documentation/security/cssm_wordid_public_key)
- [var CSSM_WORDID_PUBLIC_KEY_FROM_CERT: Int](/documentation/security/cssm_wordid_public_key_from_cert)
- [var CSSM_WORDID_Q: Int](/documentation/security/cssm_wordid_q)
- [var CSSM_WORDID_RANGE: Int](/documentation/security/cssm_wordid_range)
- [var CSSM_WORDID_REVAL: Int](/documentation/security/cssm_wordid_reval)
- [var CSSM_WORDID_RIPEMAC: Int](/documentation/security/cssm_wordid_ripemac)
- [var CSSM_WORDID_RIPEMD: Int](/documentation/security/cssm_wordid_ripemd)
- [var CSSM_WORDID_RIPEMD160: Int](/documentation/security/cssm_wordid_ripemd160)
- [var CSSM_WORDID_RSA: Int](/documentation/security/cssm_wordid_rsa)
- [var CSSM_WORDID_RSA_ISO9796: Int](/documentation/security/cssm_wordid_rsa_iso9796)
- [var CSSM_WORDID_RSA_PKCS: Int](/documentation/security/cssm_wordid_rsa_pkcs)
- [var CSSM_WORDID_RSA_PKCS1: Int](/documentation/security/cssm_wordid_rsa_pkcs1)
- [var CSSM_WORDID_RSA_PKCS1_MD5: Int](/documentation/security/cssm_wordid_rsa_pkcs1_md5)
- [var CSSM_WORDID_RSA_PKCS1_SHA1: Int](/documentation/security/cssm_wordid_rsa_pkcs1_sha1)
- [var CSSM_WORDID_RSA_PKCS1_SIG: Int](/documentation/security/cssm_wordid_rsa_pkcs1_sig)
- [var CSSM_WORDID_RSA_PKCS_MD5: Int](/documentation/security/cssm_wordid_rsa_pkcs_md5)
- [var CSSM_WORDID_RSA_PKCS_SHA1: Int](/documentation/security/cssm_wordid_rsa_pkcs_sha1)
- [var CSSM_WORDID_RSA_RAW: Int](/documentation/security/cssm_wordid_rsa_raw)
- [var CSSM_WORDID_SDSIV1: Int](/documentation/security/cssm_wordid_sdsiv1)
- [var CSSM_WORDID_SEQUENCE: Int](/documentation/security/cssm_wordid_sequence)
- [var CSSM_WORDID_SET: Int](/documentation/security/cssm_wordid_set)
- [var CSSM_WORDID_SEXPR: Int](/documentation/security/cssm_wordid_sexpr)
- [var CSSM_WORDID_SHA1: Int](/documentation/security/cssm_wordid_sha1)
- [var CSSM_WORDID_SHA1WITHDSA: Int](/documentation/security/cssm_wordid_sha1withdsa)
- [var CSSM_WORDID_SHA1WITHECDSA: Int](/documentation/security/cssm_wordid_sha1withecdsa)
- [var CSSM_WORDID_SHA1WITHRSA: Int](/documentation/security/cssm_wordid_sha1withrsa)
- [var CSSM_WORDID_SIGN: Int](/documentation/security/cssm_wordid_sign)
- [var CSSM_WORDID_SIGNATURE: Int](/documentation/security/cssm_wordid_signature)
- [var CSSM_WORDID_SIGNED_NONCE: Int](/documentation/security/cssm_wordid_signed_nonce)
- [var CSSM_WORDID_SIGNED_SECRET: Int](/documentation/security/cssm_wordid_signed_secret)
- [var CSSM_WORDID_SPKI: Int](/documentation/security/cssm_wordid_spki)
- [var CSSM_WORDID_SUBJECT: Int](/documentation/security/cssm_wordid_subject)
- [var CSSM_WORDID_SUBJECT_INFO: Int](/documentation/security/cssm_wordid_subject_info)
- [var CSSM_WORDID_SYMMETRIC_KEY: Int](/documentation/security/cssm_wordid_symmetric_key)
- [var CSSM_WORDID_SYSTEM: Int](/documentation/security/cssm_wordid_system)
- [var CSSM_WORDID_TAG: Int](/documentation/security/cssm_wordid_tag)
- [var CSSM_WORDID_THRESHOLD: Int](/documentation/security/cssm_wordid_threshold)
- [var CSSM_WORDID_TIME: Int](/documentation/security/cssm_wordid_time)
- [var CSSM_WORDID_URI: Int](/documentation/security/cssm_wordid_uri)
- [var CSSM_WORDID_VENDOR_END: Int](/documentation/security/cssm_wordid_vendor_end)
- [var CSSM_WORDID_VENDOR_START: Int](/documentation/security/cssm_wordid_vendor_start)
- [var CSSM_WORDID_VERSION: Int](/documentation/security/cssm_wordid_version)
- [var CSSM_WORDID_X509V1: Int](/documentation/security/cssm_wordid_x509v1)
- [var CSSM_WORDID_X509V2: Int](/documentation/security/cssm_wordid_x509v2)
- [var CSSM_WORDID_X509V3: Int](/documentation/security/cssm_wordid_x509v3)
- [var CSSM_WORDID_X509_ATTRIBUTE: Int](/documentation/security/cssm_wordid_x509_attribute)
- [var CSSM_WORDID_X9_ATTRIBUTE: Int](/documentation/security/cssm_wordid_x9_attribute)
- [var CSSM_WORDID__FIRST_UNUSED: Int](/documentation/security/cssm_wordid__first_unused)
- [var CSSM_WORDID__NLU_: Int](/documentation/security/cssm_wordid__nlu_)
- [var CSSM_WORDID__RESERVED_1: Int](/documentation/security/cssm_wordid__reserved_1)
- [var CSSM_WORDID__STAR_: Int](/documentation/security/cssm_wordid__star_)
- [var CSSM_WORDID__UNK_: Int](/documentation/security/cssm_wordid__unk_)
- [var CSSM_X509_DATAFORMAT_ENCODED: extension_data_format](/documentation/security/cssm_x509_dataformat_encoded)
- [var CSSM_X509_DATAFORMAT_PAIR: extension_data_format](/documentation/security/cssm_x509_dataformat_pair)
- [var CSSM_X509_DATAFORMAT_PARSED: extension_data_format](/documentation/security/cssm_x509_dataformat_parsed)
- [var errSSLEarlyDataRejected: OSStatus](/documentation/security/errsslearlydatarejected)
- [var errSecCSCMSConstructionFailed: OSStatus](/documentation/security/errseccscmsconstructionfailed)
- [var errSecCSRemoteSignerFailed: OSStatus](/documentation/security/errseccsremotesignerfailed)
- [var errSecCertificateDuplicateExtension: OSStatus](/documentation/security/errseccertificateduplicateextension)
- [var errSecCertificateIsCA: OSStatus](/documentation/security/errseccertificateisca)
- [var errSecInvalidCRLAuthority: OSStatus](/documentation/security/errsecinvalidcrlauthority)
- [var errSecInvalidTupleCredentials: OSStatus](/documentation/security/errsecinvalidtuplecredentials)
- [var errSecRestrictedAPI: OSStatus](/documentation/security/errsecrestrictedapi)
- [var kCSSM_APPLEDL_MASK_MODE: cssm_appledl_open_parameters_mask](/documentation/security/kcssm_appledl_mask_mode)
- [var kSecCSAllowNetworkAccess: UInt32](/documentation/security/kseccsallownetworkaccess)
- [var kSecCSFastExecutableValidation: UInt32](/documentation/security/kseccsfastexecutablevalidation)

### Certificate Extensions

- [CE_CrlNumber](/documentation/security/ce_crlnumber)
- [CE_DeltaCrl](/documentation/security/ce_deltacrl)
- [var CE_CD_AffiliationChanged: Int32](/documentation/security/ce_cd_affiliationchanged)
- [var CE_CD_CACompromise: Int32](/documentation/security/ce_cd_cacompromise)
- [var CE_CD_CertificateHold: Int32](/documentation/security/ce_cd_certificatehold)
- [var CE_CD_CessationOfOperation: Int32](/documentation/security/ce_cd_cessationofoperation)
- [var CE_CD_KeyCompromise: Int32](/documentation/security/ce_cd_keycompromise)
- [var CE_CD_Superseded: Int32](/documentation/security/ce_cd_superseded)
- [var CE_CD_Unspecified: Int32](/documentation/security/ce_cd_unspecified)
- [var CE_CR_AffiliationChanged: Int32](/documentation/security/ce_cr_affiliationchanged)
- [var SecCECR_AffiliationChanged: Int32](/documentation/security/seccecr_affiliationchanged)
- [var CE_CR_CACompromise: Int32](/documentation/security/ce_cr_cacompromise)
- [var SecCECR_CACompromise: Int32](/documentation/security/seccecr_cacompromise)
- [var CE_CR_CertificateHold: Int32](/documentation/security/ce_cr_certificatehold)
- [var SecCECR_CertificateHold: Int32](/documentation/security/seccecr_certificatehold)
- [var CE_CR_CessationOfOperation: Int32](/documentation/security/ce_cr_cessationofoperation)
- [var SecCECR_CessationOfOperation: Int32](/documentation/security/seccecr_cessationofoperation)
- [var CE_CR_KeyCompromise: Int32](/documentation/security/ce_cr_keycompromise)
- [var SecCECR_KeyCompromise: Int32](/documentation/security/seccecr_keycompromise)
- [var CE_CR_RemoveFromCRL: Int32](/documentation/security/ce_cr_removefromcrl)
- [var SecCECR_RemoveFromCRL: Int32](/documentation/security/seccecr_removefromcrl)
- [var CE_CR_Superseded: Int32](/documentation/security/ce_cr_superseded)
- [var SecCECR_Superseded: Int32](/documentation/security/seccecr_superseded)
- [var CE_CR_Unspecified: Int32](/documentation/security/ce_cr_unspecified)
- [var SecCECR_Unspecified: Int32](/documentation/security/seccecr_unspecified)
- [var CE_KU_CRLSign: Int32](/documentation/security/ce_ku_crlsign)
- [var SecCEKU_CRLSign: Int32](/documentation/security/secceku_crlsign)
- [var CE_KU_DataEncipherment: Int32](/documentation/security/ce_ku_dataencipherment)
- [var SecCEKU_DataEncipherment: Int32](/documentation/security/secceku_dataencipherment)
- [var CE_KU_DecipherOnly: Int32](/documentation/security/ce_ku_decipheronly)
- [var SecCEKU_DecipherOnly: Int32](/documentation/security/secceku_decipheronly)
- [var CE_KU_DigitalSignature: Int32](/documentation/security/ce_ku_digitalsignature)
- [var SecCEKU_DigitalSignature: Int32](/documentation/security/secceku_digitalsignature)
- [var CE_KU_EncipherOnly: Int32](/documentation/security/ce_ku_encipheronly)
- [var SecCEKU_EncipherOnly: Int32](/documentation/security/secceku_encipheronly)
- [var CE_KU_KeyAgreement: Int32](/documentation/security/ce_ku_keyagreement)
- [var SecCEKU_KeyAgreement: Int32](/documentation/security/secceku_keyagreement)
- [var CE_KU_KeyCertSign: Int32](/documentation/security/ce_ku_keycertsign)
- [var SecCEKU_KeyCertSign: Int32](/documentation/security/secceku_keycertsign)
- [var CE_KU_KeyEncipherment: Int32](/documentation/security/ce_ku_keyencipherment)
- [var SecCEKU_KeyEncipherment: Int32](/documentation/security/secceku_keyencipherment)
- [var CE_KU_NonRepudiation: Int32](/documentation/security/ce_ku_nonrepudiation)
- [var SecCEKU_NonRepudiation: Int32](/documentation/security/secceku_nonrepudiation)
- [var CE_CDNT_FullName: __CE_CrlDistributionPointNameType](/documentation/security/ce_cdnt_fullname)
- [var CE_CDNT_NameRelativeToCrlIssuer: __CE_CrlDistributionPointNameType](/documentation/security/ce_cdnt_namerelativetocrlissuer)
- [var DT_AuthorityInfoAccess: __CE_DataType](/documentation/security/dt_authorityinfoaccess)
- [var DT_AuthorityKeyID: __CE_DataType](/documentation/security/dt_authoritykeyid)
- [var DT_BasicConstraints: __CE_DataType](/documentation/security/dt_basicconstraints)
- [var DT_CertPolicies: __CE_DataType](/documentation/security/dt_certpolicies)
- [var DT_CrlDistributionPoints: __CE_DataType](/documentation/security/dt_crldistributionpoints)
- [var DT_CrlNumber: __CE_DataType](/documentation/security/dt_crlnumber)
- [var DT_CrlReason: __CE_DataType](/documentation/security/dt_crlreason)
- [var DT_DeltaCrl: __CE_DataType](/documentation/security/dt_deltacrl)
- [var DT_ExtendedKeyUsage: __CE_DataType](/documentation/security/dt_extendedkeyusage)
- [var DT_InhibitAnyPolicy: __CE_DataType](/documentation/security/dt_inhibitanypolicy)
- [var DT_IssuerAltName: __CE_DataType](/documentation/security/dt_issueraltname)
- [var DT_IssuingDistributionPoint: __CE_DataType](/documentation/security/dt_issuingdistributionpoint)
- [var DT_KeyUsage: __CE_DataType](/documentation/security/dt_keyusage)
- [var DT_NameConstraints: __CE_DataType](/documentation/security/dt_nameconstraints)
- [var DT_NetscapeCertType: __CE_DataType](/documentation/security/dt_netscapecerttype)
- [var DT_Other: __CE_DataType](/documentation/security/dt_other)
- [var DT_PolicyConstraints: __CE_DataType](/documentation/security/dt_policyconstraints)
- [var DT_PolicyMappings: __CE_DataType](/documentation/security/dt_policymappings)
- [var DT_QC_Statements: __CE_DataType](/documentation/security/dt_qc_statements)
- [var DT_SubjectAltName: __CE_DataType](/documentation/security/dt_subjectaltname)
- [var DT_SubjectKeyID: __CE_DataType](/documentation/security/dt_subjectkeyid)
- [var GNT_DNSName: __CE_GeneralNameType](/documentation/security/gnt_dnsname)
- [var GNT_DirectoryName: __CE_GeneralNameType](/documentation/security/gnt_directoryname)
- [var GNT_EdiPartyName: __CE_GeneralNameType](/documentation/security/gnt_edipartyname)
- [var GNT_IPAddress: __CE_GeneralNameType](/documentation/security/gnt_ipaddress)
- [var GNT_OtherName: __CE_GeneralNameType](/documentation/security/gnt_othername)
- [var GNT_RFC822Name: __CE_GeneralNameType](/documentation/security/gnt_rfc822name)
- [var GNT_RegisteredID: __CE_GeneralNameType](/documentation/security/gnt_registeredid)
- [var GNT_URI: __CE_GeneralNameType](/documentation/security/gnt_uri)
- [var GNT_X400Address: __CE_GeneralNameType](/documentation/security/gnt_x400address)

### OIDs

- [var APPLE_ADS_OID_LENGTH: Int32](/documentation/security/apple_ads_oid_length)
- [var APPLE_ALG_OID_LENGTH: Int32](/documentation/security/apple_alg_oid_length)
- [var APPLE_CERT_POLICIES_APPLEID_LENGTH: Int32](/documentation/security/apple_cert_policies_appleid_length)
- [var APPLE_CERT_POLICIES_APPLEID_SHARING_LENGTH: Int32](/documentation/security/apple_cert_policies_appleid_sharing_length)
- [var APPLE_CERT_POLICIES_LENGTH: Int32](/documentation/security/apple_cert_policies_length)
- [var APPLE_CERT_POLICIES_MACAPPSTORE_LENGTH: Int32](/documentation/security/apple_cert_policies_macappstore_length)
- [var APPLE_CERT_POLICIES_MACAPPSTORE_RECEIPT_LENGTH: Int32](/documentation/security/apple_cert_policies_macappstore_receipt_length)
- [var APPLE_CERT_POLICIES_MOBILE_STORE_SIGNING_LENGTH: Int32](/documentation/security/apple_cert_policies_mobile_store_signing_length)
- [var APPLE_CERT_POLICIES_TEST_MOBILE_STORE_SIGNING_LENGTH: Int32](/documentation/security/apple_cert_policies_test_mobile_store_signing_length)
- [var APPLE_DOTMAC_CERT_EXTEN_OID_LENGTH: Int32](/documentation/security/apple_dotmac_cert_exten_oid_length)
- [var APPLE_DOTMAC_CERT_OID_LENGTH: Int32](/documentation/security/apple_dotmac_cert_oid_length)
- [var APPLE_DOTMAC_CERT_REQ_OID_LENGTH: Int32](/documentation/security/apple_dotmac_cert_req_oid_length)
- [var APPLE_DOTMAC_CERT_REQ_VALUE_OID_LENGTH: Int32](/documentation/security/apple_dotmac_cert_req_value_oid_length)
- [var APPLE_EKU_CODE_SIGNING_LENGTH: Int32](/documentation/security/apple_eku_code_signing_length)
- [var APPLE_EKU_OID_LENGTH: Int32](/documentation/security/apple_eku_oid_length)
- [var APPLE_EXTENSION_AAI_INTERMEDIATE_LENGTH: Int32](/documentation/security/apple_extension_aai_intermediate_length)
- [var APPLE_EXTENSION_APPLEID_INTERMEDIATE_LENGTH: Int32](/documentation/security/apple_extension_appleid_intermediate_length)
- [var APPLE_EXTENSION_APPLEID_SHARING_LENGTH: Int32](/documentation/security/apple_extension_appleid_sharing_length)
- [var APPLE_EXTENSION_CODE_SIGNING_LENGTH: Int32](/documentation/security/apple_extension_code_signing_length)
- [var APPLE_EXTENSION_ESCROW_SERVICE_LENGTH: Int32](/documentation/security/apple_extension_escrow_service_length)
- [var APPLE_EXTENSION_INTERMEDIATE_MARKER_LENGTH: Int32](/documentation/security/apple_extension_intermediate_marker_length)
- [var APPLE_EXTENSION_ITMS_INTERMEDIATE_LENGTH: Int32](/documentation/security/apple_extension_itms_intermediate_length)
- [var APPLE_EXTENSION_MACAPPSTORE_RECEIPT_LENGTH: Int32](/documentation/security/apple_extension_macappstore_receipt_length)
- [var APPLE_EXTENSION_OID_LENGTH: Int32](/documentation/security/apple_extension_oid_length)
- [var APPLE_EXTENSION_SYSINT2_INTERMEDIATE_LENGTH: Int32](/documentation/security/apple_extension_sysint2_intermediate_length)
- [var APPLE_EXTENSION_WWDR_INTERMEDIATE_LENGTH: Int32](/documentation/security/apple_extension_wwdr_intermediate_length)
- [var APPLE_OID_LENGTH: Int32](/documentation/security/apple_oid_length)
- [var APPLE_TP_OID_LENGTH: Int32](/documentation/security/apple_tp_oid_length)
- [var INTEL_CDSASECURITY_LENGTH: Int32](/documentation/security/intel_cdsasecurity_length)
- [var INTEL_CERT_AND_PRIVATE_KEY_2_0_LENGTH: Int32](/documentation/security/intel_cert_and_private_key_2_0_length)
- [var INTEL_LENGTH: Int32](/documentation/security/intel_length)
- [var INTEL_SEC_ALGS_LENGTH: Int32](/documentation/security/intel_sec_algs_length)
- [var INTEL_SEC_FORMATS_LENGTH: Int32](/documentation/security/intel_sec_formats_length)
- [var INTEL_SEC_OBJECT_BUNDLE_LENGTH: Int32](/documentation/security/intel_sec_object_bundle_length)
- [var INTEL_X509V2_CRL_R08_LENGTH: Int32](/documentation/security/intel_x509v2_crl_r08_length)
- [var INTEL_X509V3_CERT_PRIVATE_EXTENSIONS_LENGTH: Int32](/documentation/security/intel_x509v3_cert_private_extensions_length)
- [var INTEL_X509V3_CERT_R08_LENGTH: Int32](/documentation/security/intel_x509v3_cert_r08_length)
- [var INTEL_X509V3_SIGN_R08_LENGTH: Int32](/documentation/security/intel_x509v3_sign_r08_length)
- [var INTEL_X509_C_DATATYPE: Int32](/documentation/security/intel_x509_c_datatype)
- [var INTEL_X509_LDAPSTRING_DATATYPE: Int32](/documentation/security/intel_x509_ldapstring_datatype)
- [var NETSCAPE_BASE_OID_LEN: Int32](/documentation/security/netscape_base_oid_len)
- [var NETSCAPE_CERT_EXTEN_LENGTH: Int32](/documentation/security/netscape_cert_exten_length)
- [var NETSCAPE_CERT_POLICY_LENGTH: Int32](/documentation/security/netscape_cert_policy_length)
- [var OID_AD_LENGTH: Int32](/documentation/security/oid_ad_length)
- [var OID_AD_OCSP_LENGTH: Int32](/documentation/security/oid_ad_ocsp_length)
- [var OID_ANSI_X9_42_LEN: Int32](/documentation/security/oid_ansi_x9_42_len)
- [var OID_ANSI_X9_42_NAMED_SCHEME_LEN: Int32](/documentation/security/oid_ansi_x9_42_named_scheme_len)
- [var OID_ANSI_X9_42_SCHEME_LEN: Int32](/documentation/security/oid_ansi_x9_42_scheme_len)
- [var OID_ANSI_X9_62_ELL_CURVE_LEN: Int32](/documentation/security/oid_ansi_x9_62_ell_curve_len)
- [var OID_ANSI_X9_62_LEN: Int32](/documentation/security/oid_ansi_x9_62_len)
- [var OID_ANSI_X9_62_SIG_TYPE_LEN: Int32](/documentation/security/oid_ansi_x9_62_sig_type_len)
- [var OID_ATTR_TYPE_LENGTH: Int32](/documentation/security/oid_attr_type_length)
- [var OID_CERTICOM_ELL_CURVE_LEN: Int32](/documentation/security/oid_certicom_ell_curve_len)
- [var OID_CERTICOM_LEN: Int32](/documentation/security/oid_certicom_len)
- [var OID_DS: Int32](/documentation/security/oid_ds)
- [var OID_DS_LENGTH: Int32](/documentation/security/oid_ds_length)
- [var OID_ETSI_LENGTH: Int32](/documentation/security/oid_etsi_length)
- [var OID_ETSI_QCS_LENGTH: Int32](/documentation/security/oid_etsi_qcs_length)
- [var OID_EXTENSION_LENGTH: Int32](/documentation/security/oid_extension_length)
- [var OID_ISO_CCITT_DIR_SERVICE: Int32](/documentation/security/oid_iso_ccitt_dir_service)
- [var OID_ISO_IDENTIFIED_ORG: Int32](/documentation/security/oid_iso_identified_org)
- [var OID_ISO_MEMBER: Int32](/documentation/security/oid_iso_member)
- [var OID_ISO_MEMBER_LENGTH: Int32](/documentation/security/oid_iso_member_length)
- [var OID_ISO_STANDARD: Int32](/documentation/security/oid_iso_standard)
- [var OID_ITU_RFCDATA: Int32](/documentation/security/oid_itu_rfcdata)
- [var OID_ITU_RFCDATA_2342_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_length)
- [var OID_ITU_RFCDATA_2342_UCL_DIRECTORYPILOT_ATTRIBUTES_DOMAINCOMPONENT_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_ucl_directorypilot_attributes_domaincomponent_length)
- [var OID_ITU_RFCDATA_2342_UCL_DIRECTORYPILOT_ATTRIBUTES_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_ucl_directorypilot_attributes_length)
- [var OID_ITU_RFCDATA_2342_UCL_DIRECTORYPILOT_ATTRIBUTES_USERID_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_ucl_directorypilot_attributes_userid_length)
- [var OID_ITU_RFCDATA_2342_UCL_DIRECTORYPILOT_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_ucl_directorypilot_length)
- [var OID_ITU_RFCDATA_2342_UCL_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_2342_ucl_length)
- [var OID_ITU_RFCDATA_MEMBER_LENGTH: Int32](/documentation/security/oid_itu_rfcdata_member_length)
- [var OID_KERBv5_LEN: Int32](/documentation/security/oid_kerbv5_len)
- [var OID_KERBv5_PKINIT_LEN: Int32](/documentation/security/oid_kerbv5_pkinit_len)
- [var OID_KP_LENGTH: Int32](/documentation/security/oid_kp_length)
- [var OID_NIST_HASHALG_LENGTH: Int32](/documentation/security/oid_nist_hashalg_length)
- [var OID_OIW_ALGORITHM_LENGTH: Int32](/documentation/security/oid_oiw_algorithm_length)
- [var OID_OIW_LENGTH: Int32](/documentation/security/oid_oiw_length)
- [var OID_OIW_SECSIG_LENGTH: Int32](/documentation/security/oid_oiw_secsig_length)
- [var OID_OTHER_NAME_LENGTH: Int32](/documentation/security/oid_other_name_length)
- [var OID_PDA_LENGTH: Int32](/documentation/security/oid_pda_length)
- [var OID_PE_LENGTH: Int32](/documentation/security/oid_pe_length)
- [var OID_PKCS_11_LENGTH: Int32](/documentation/security/oid_pkcs_11_length)
- [var OID_PKCS_12_LENGTH: Int32](/documentation/security/oid_pkcs_12_length)
- [var OID_PKCS_1_LENGTH: Int32](/documentation/security/oid_pkcs_1_length)
- [var OID_PKCS_3_LENGTH: Int32](/documentation/security/oid_pkcs_3_length)
- [var OID_PKCS_5_LENGTH: Int32](/documentation/security/oid_pkcs_5_length)
- [var OID_PKCS_7_LENGTH: Int32](/documentation/security/oid_pkcs_7_length)
- [var OID_PKCS_9_LENGTH: Int32](/documentation/security/oid_pkcs_9_length)
- [var OID_PKCS_LENGTH: Int32](/documentation/security/oid_pkcs_length)
- [var OID_PKIX_LENGTH: Int32](/documentation/security/oid_pkix_length)
- [var OID_QCS_LENGTH: Int32](/documentation/security/oid_qcs_length)
- [var OID_QT_LENGTH: Int32](/documentation/security/oid_qt_length)
- [var OID_RSA_ENCRYPT_LENGTH: Int32](/documentation/security/oid_rsa_encrypt_length)
- [var OID_RSA_HASH_LENGTH: Int32](/documentation/security/oid_rsa_hash_length)
- [var OID_RSA_LENGTH: Int32](/documentation/security/oid_rsa_length)
- [var OID_US_LENGTH: Int32](/documentation/security/oid_us_length)
- [let oidAdCAIssuer: DERItem](/documentation/security/oidadcaissuer)
- [let oidAdOCSP: DERItem](/documentation/security/oidadocsp)
- [let oidAnsip384r1: DERItem](/documentation/security/oidansip384r1)
- [let oidAnsip521r1: DERItem](/documentation/security/oidansip521r1)
- [let oidAnyExtendedKeyUsage: DERItem](/documentation/security/oidanyextendedkeyusage)
- [let oidAnyPolicy: DERItem](/documentation/security/oidanypolicy)
- [let oidAuthorityInfoAccess: DERItem](/documentation/security/oidauthorityinfoaccess)
- [let oidAuthorityKeyIdentifier: DERItem](/documentation/security/oidauthoritykeyidentifier)
- [let oidBasicConstraints: DERItem](/documentation/security/oidbasicconstraints)
- [let oidCertificatePolicies: DERItem](/documentation/security/oidcertificatepolicies)
- [let oidCommonName: DERItem](/documentation/security/oidcommonname)
- [let oidCountryName: DERItem](/documentation/security/oidcountryname)
- [let oidCrlDistributionPoints: DERItem](/documentation/security/oidcrldistributionpoints)
- [let oidDescription: DERItem](/documentation/security/oiddescription)
- [let oidEcPrime192v1: DERItem](/documentation/security/oidecprime192v1)
- [let oidEcPrime256v1: DERItem](/documentation/security/oidecprime256v1)
- [let oidEcPubKey: DERItem](/documentation/security/oidecpubkey)
- [let oidEmailAddress: DERItem](/documentation/security/oidemailaddress)
- [let oidEntrustVersInfo: DERItem](/documentation/security/oidentrustversinfo)
- [let oidExtendedKeyUsage: DERItem](/documentation/security/oidextendedkeyusage)
- [let oidExtendedKeyUsageClientAuth: DERItem](/documentation/security/oidextendedkeyusageclientauth)
- [let oidExtendedKeyUsageCodeSigning: DERItem](/documentation/security/oidextendedkeyusagecodesigning)
- [let oidExtendedKeyUsageEmailProtection: DERItem](/documentation/security/oidextendedkeyusageemailprotection)
- [let oidExtendedKeyUsageIPSec: DERItem](/documentation/security/oidextendedkeyusageipsec)
- [let oidExtendedKeyUsageMicrosoftSGC: DERItem](/documentation/security/oidextendedkeyusagemicrosoftsgc)
- [let oidExtendedKeyUsageNetscapeSGC: DERItem](/documentation/security/oidextendedkeyusagenetscapesgc)
- [let oidExtendedKeyUsageOCSPSigning: DERItem](/documentation/security/oidextendedkeyusageocspsigning)
- [let oidExtendedKeyUsageServerAuth: DERItem](/documentation/security/oidextendedkeyusageserverauth)
- [let oidExtendedKeyUsageTimeStamping: DERItem](/documentation/security/oidextendedkeyusagetimestamping)
- [let oidFee: DERItem](/documentation/security/oidfee)
- [let oidFriendlyName: DERItem](/documentation/security/oidfriendlyname)
- [let oidGoogleEmbeddedSignedCertificateTimestamp: DERItem](/documentation/security/oidgoogleembeddedsignedcertificatetimestamp)
- [let oidGoogleOCSPSignedCertificateTimestamp: DERItem](/documentation/security/oidgoogleocspsignedcertificatetimestamp)
- [let oidInhibitAnyPolicy: DERItem](/documentation/security/oidinhibitanypolicy)
- [let oidIssuerAltName: DERItem](/documentation/security/oidissueraltname)
- [let oidKeyUsage: DERItem](/documentation/security/oidkeyusage)
- [let oidLocalKeyId: DERItem](/documentation/security/oidlocalkeyid)
- [let oidLocalityName: DERItem](/documentation/security/oidlocalityname)
- [let oidMSNTPrincipalName: DERItem](/documentation/security/oidmsntprincipalname)
- [let oidMd2: DERItem](/documentation/security/oidmd2)
- [let oidMd2Rsa: DERItem](/documentation/security/oidmd2rsa)
- [let oidMd4: DERItem](/documentation/security/oidmd4)
- [let oidMd4Rsa: DERItem](/documentation/security/oidmd4rsa)
- [let oidMd5: DERItem](/documentation/security/oidmd5)
- [let oidMd5Fee: DERItem](/documentation/security/oidmd5fee)
- [let oidMd5Rsa: DERItem](/documentation/security/oidmd5rsa)
- [let oidNameConstraints: DERItem](/documentation/security/oidnameconstraints)
- [let oidNetscapeCertType: DERItem](/documentation/security/oidnetscapecerttype)
- [let oidOrganizationName: DERItem](/documentation/security/oidorganizationname)
- [let oidOrganizationalUnitName: DERItem](/documentation/security/oidorganizationalunitname)
- [let oidPolicyConstraints: DERItem](/documentation/security/oidpolicyconstraints)
- [let oidPolicyMappings: DERItem](/documentation/security/oidpolicymappings)
- [let oidPrivateKeyUsagePeriod: DERItem](/documentation/security/oidprivatekeyusageperiod)
- [let oidQtCps: DERItem](/documentation/security/oidqtcps)
- [let oidQtUNotice: DERItem](/documentation/security/oidqtunotice)
- [let oidRsa: DERItem](/documentation/security/oidrsa)
- [let oidSha1: DERItem](/documentation/security/oidsha1)
- [let oidSha1Dsa: DERItem](/documentation/security/oidsha1dsa)
- [let oidSha1DsaCommonOIW: DERItem](/documentation/security/oidsha1dsacommonoiw)
- [let oidSha1DsaOIW: DERItem](/documentation/security/oidsha1dsaoiw)
- [let oidSha1Ecdsa: DERItem](/documentation/security/oidsha1ecdsa)
- [let oidSha1Fee: DERItem](/documentation/security/oidsha1fee)
- [let oidSha1Rsa: DERItem](/documentation/security/oidsha1rsa)
- [let oidSha1RsaOIW: DERItem](/documentation/security/oidsha1rsaoiw)
- [let oidSha224: DERItem](/documentation/security/oidsha224)
- [let oidSha224Ecdsa: DERItem](/documentation/security/oidsha224ecdsa)
- [let oidSha224Rsa: DERItem](/documentation/security/oidsha224rsa)
- [let oidSha256: DERItem](/documentation/security/oidsha256)
- [let oidSha256Ecdsa: DERItem](/documentation/security/oidsha256ecdsa)
- [let oidSha256Rsa: DERItem](/documentation/security/oidsha256rsa)
- [let oidSha384: DERItem](/documentation/security/oidsha384)
- [let oidSha384Ecdsa: DERItem](/documentation/security/oidsha384ecdsa)
- [let oidSha384Rsa: DERItem](/documentation/security/oidsha384rsa)
- [let oidSha512: DERItem](/documentation/security/oidsha512)
- [let oidSha512Ecdsa: DERItem](/documentation/security/oidsha512ecdsa)
- [let oidSha512Rsa: DERItem](/documentation/security/oidsha512rsa)
- [let oidStateOrProvinceName: DERItem](/documentation/security/oidstateorprovincename)
- [let oidSubjectAltName: DERItem](/documentation/security/oidsubjectaltname)
- [let oidSubjectInfoAccess: DERItem](/documentation/security/oidsubjectinfoaccess)
- [let oidSubjectKeyIdentifier: DERItem](/documentation/security/oidsubjectkeyidentifier)
- [var APPLE_EXTENSION_DEVELOPER_AUTHENTICATION_LENGTH: Int32](/documentation/security/apple_extension_developer_authentication_length)
- [var APPLE_EXTENSION_PROVISIONING_PROFILE_SIGNING_LENGTH: Int32](/documentation/security/apple_extension_provisioning_profile_signing_length)
- [var APPLE_EXTENSION_SERVER_AUTHENTICATION_LENGTH: Int32](/documentation/security/apple_extension_server_authentication_length)

### Data structures

- [CSSM_APPLE_CL_CSR_REQUEST](/documentation/security/cssm_apple_cl_csr_request)

#### Initializers

- [init()](/documentation/security/cssm_apple_cl_csr_request/init())
- [init(subjectNameX509: UnsafeMutablePointer<cssm_x509_name>!, signatureAlg: CSSM_ALGORITHMS, signatureOid: SecAsn1Oid, cspHand: CSSM_CSP_HANDLE, subjectPublicKey: UnsafePointer<cssm_key>!, subjectPrivateKey: UnsafePointer<cssm_key>!, challengeString: UnsafePointer<CChar>!)](/documentation/security/cssm_apple_cl_csr_request/init(subjectnamex509:signaturealg:signatureoid:csphand:subjectpublickey:subjectprivatekey:challengestring:))

#### Instance Properties

- [var challengeString: UnsafePointer<CChar>!](/documentation/security/cssm_apple_cl_csr_request/challengestring)
- [var cspHand: CSSM_CSP_HANDLE](/documentation/security/cssm_apple_cl_csr_request/csphand)
- [var signatureAlg: CSSM_ALGORITHMS](/documentation/security/cssm_apple_cl_csr_request/signaturealg)
- [var signatureOid: SecAsn1Oid](/documentation/security/cssm_apple_cl_csr_request/signatureoid)
- [var subjectNameX509: UnsafeMutablePointer<cssm_x509_name>!](/documentation/security/cssm_apple_cl_csr_request/subjectnamex509)
- [var subjectPrivateKey: UnsafePointer<cssm_key>!](/documentation/security/cssm_apple_cl_csr_request/subjectprivatekey)
- [var subjectPublicKey: UnsafePointer<cssm_key>!](/documentation/security/cssm_apple_cl_csr_request/subjectpublickey)
- [CSSM_APPLE_TP_ACTION_DATA](/documentation/security/cssm_apple_tp_action_data)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_action_data/init())
- [init(Version: uint32, ActionFlags: CSSM_APPLE_TP_ACTION_FLAGS)](/documentation/security/cssm_apple_tp_action_data/init(version:actionflags:))

#### Instance Properties

- [var ActionFlags: CSSM_APPLE_TP_ACTION_FLAGS](/documentation/security/cssm_apple_tp_action_data/actionflags)
- [var Version: uint32](/documentation/security/cssm_apple_tp_action_data/version)
- [CSSM_APPLE_TP_CERT_REQUEST](/documentation/security/cssm_apple_tp_cert_request)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_cert_request/init())
- [init(cspHand: CSSM_CSP_HANDLE, clHand: CSSM_CL_HANDLE, serialNumber: uint32, numSubjectNames: uint32, subjectNames: UnsafeMutablePointer<CSSM_APPLE_TP_NAME_OID>!, numIssuerNames: uint32, issuerNames: UnsafeMutablePointer<CSSM_APPLE_TP_NAME_OID>!, issuerNameX509: UnsafeMutablePointer<cssm_x509_name>!, certPublicKey: UnsafePointer<cssm_key>!, issuerPrivateKey: UnsafePointer<cssm_key>!, signatureAlg: CSSM_ALGORITHMS, signatureOid: SecAsn1Oid, notBefore: uint32, notAfter: uint32, numExtensions: uint32, extensions: UnsafeMutablePointer<__CE_DataAndType>!, challengeString: UnsafePointer<CChar>!)](/documentation/security/cssm_apple_tp_cert_request/init(csphand:clhand:serialnumber:numsubjectnames:subjectnames:numissuernames:issuernames:issuernamex509:certpublickey:issuerprivatekey:signaturealg:signatureoid:notbefore:notafter:numextensions:extensions:challengestring:))

#### Instance Properties

- [var certPublicKey: UnsafePointer<cssm_key>!](/documentation/security/cssm_apple_tp_cert_request/certpublickey)
- [var challengeString: UnsafePointer<CChar>!](/documentation/security/cssm_apple_tp_cert_request/challengestring)
- [var clHand: CSSM_CL_HANDLE](/documentation/security/cssm_apple_tp_cert_request/clhand)
- [var cspHand: CSSM_CSP_HANDLE](/documentation/security/cssm_apple_tp_cert_request/csphand)
- [var extensions: UnsafeMutablePointer<__CE_DataAndType>!](/documentation/security/cssm_apple_tp_cert_request/extensions)
- [var issuerNameX509: UnsafeMutablePointer<cssm_x509_name>!](/documentation/security/cssm_apple_tp_cert_request/issuernamex509)
- [var issuerNames: UnsafeMutablePointer<CSSM_APPLE_TP_NAME_OID>!](/documentation/security/cssm_apple_tp_cert_request/issuernames)
- [var issuerPrivateKey: UnsafePointer<cssm_key>!](/documentation/security/cssm_apple_tp_cert_request/issuerprivatekey)
- [var notAfter: uint32](/documentation/security/cssm_apple_tp_cert_request/notafter)
- [var notBefore: uint32](/documentation/security/cssm_apple_tp_cert_request/notbefore)
- [var numExtensions: uint32](/documentation/security/cssm_apple_tp_cert_request/numextensions)
- [var numIssuerNames: uint32](/documentation/security/cssm_apple_tp_cert_request/numissuernames)
- [var numSubjectNames: uint32](/documentation/security/cssm_apple_tp_cert_request/numsubjectnames)
- [var serialNumber: uint32](/documentation/security/cssm_apple_tp_cert_request/serialnumber)
- [var signatureAlg: CSSM_ALGORITHMS](/documentation/security/cssm_apple_tp_cert_request/signaturealg)
- [var signatureOid: SecAsn1Oid](/documentation/security/cssm_apple_tp_cert_request/signatureoid)
- [var subjectNames: UnsafeMutablePointer<CSSM_APPLE_TP_NAME_OID>!](/documentation/security/cssm_apple_tp_cert_request/subjectnames)
- [CSSM_APPLE_TP_CRL_OPTIONS](/documentation/security/cssm_apple_tp_crl_options)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_crl_options/init())
- [init(Version: uint32, CrlFlags: CSSM_APPLE_TP_CRL_OPT_FLAGS, crlStore: UnsafeMutablePointer<cssm_dl_db_handle>!)](/documentation/security/cssm_apple_tp_crl_options/init(version:crlflags:crlstore:))

#### Instance Properties

- [var CrlFlags: CSSM_APPLE_TP_CRL_OPT_FLAGS](/documentation/security/cssm_apple_tp_crl_options/crlflags)
- [var Version: uint32](/documentation/security/cssm_apple_tp_crl_options/version)
- [var crlStore: UnsafeMutablePointer<cssm_dl_db_handle>!](/documentation/security/cssm_apple_tp_crl_options/crlstore)
- [CSSM_APPLE_TP_NAME_OID](/documentation/security/cssm_apple_tp_name_oid)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_name_oid/init())
- [init(string: UnsafePointer<CChar>!, oid: UnsafePointer<SecAsn1Oid>!)](/documentation/security/cssm_apple_tp_name_oid/init(string:oid:))

#### Instance Properties

- [var oid: UnsafePointer<SecAsn1Oid>!](/documentation/security/cssm_apple_tp_name_oid/oid)
- [var string: UnsafePointer<CChar>!](/documentation/security/cssm_apple_tp_name_oid/string)
- [CSSM_APPLE_TP_SMIME_OPTIONS](/documentation/security/cssm_apple_tp_smime_options)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_smime_options/init())
- [init(Version: uint32, IntendedUsage: uint16, SenderEmailLen: uint32, SenderEmail: UnsafePointer<CChar>!)](/documentation/security/cssm_apple_tp_smime_options/init(version:intendedusage:senderemaillen:senderemail:))

#### Instance Properties

- [var IntendedUsage: uint16](/documentation/security/cssm_apple_tp_smime_options/intendedusage)
- [var SenderEmail: UnsafePointer<CChar>!](/documentation/security/cssm_apple_tp_smime_options/senderemail)
- [var SenderEmailLen: uint32](/documentation/security/cssm_apple_tp_smime_options/senderemaillen)
- [var Version: uint32](/documentation/security/cssm_apple_tp_smime_options/version)
- [CSSM_APPLE_TP_SSL_OPTIONS](/documentation/security/cssm_apple_tp_ssl_options)

#### Initializers

- [init()](/documentation/security/cssm_apple_tp_ssl_options/init())
- [init(Version: uint32, ServerNameLen: uint32, ServerName: UnsafePointer<CChar>!, Flags: uint32)](/documentation/security/cssm_apple_tp_ssl_options/init(version:servernamelen:servername:flags:))

#### Instance Properties

- [var Flags: uint32](/documentation/security/cssm_apple_tp_ssl_options/flags)
- [var ServerName: UnsafePointer<CChar>!](/documentation/security/cssm_apple_tp_ssl_options/servername)
- [var ServerNameLen: uint32](/documentation/security/cssm_apple_tp_ssl_options/servernamelen)
- [var Version: uint32](/documentation/security/cssm_apple_tp_ssl_options/version)
- [CSSM_TP_APPLE_EVIDENCE_HEADER](/documentation/security/cssm_tp_apple_evidence_header)

#### Initializers

- [init()](/documentation/security/cssm_tp_apple_evidence_header/init())
- [init(Version: uint32)](/documentation/security/cssm_tp_apple_evidence_header/init(version:))

#### Instance Properties

- [var Version: uint32](/documentation/security/cssm_tp_apple_evidence_header/version)
- [cssm_acl_keychain_prompt_selector](/documentation/security/cssm_acl_keychain_prompt_selector-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_acl_keychain_prompt_selector-swift.struct/init())
- [init(version: uint16, flags: uint16)](/documentation/security/cssm_acl_keychain_prompt_selector-swift.struct/init(version:flags:))

#### Instance Properties

- [var flags: uint16](/documentation/security/cssm_acl_keychain_prompt_selector-swift.struct/flags)
- [var version: uint16](/documentation/security/cssm_acl_keychain_prompt_selector-swift.struct/version)
- [cssm_acl_process_subject_selector](/documentation/security/cssm_acl_process_subject_selector-swift.struct)

#### Initializers

- [init()](/documentation/security/cssm_acl_process_subject_selector-swift.struct/init())
- [init(version: uint16, mask: uint16, uid: uint32, gid: uint32)](/documentation/security/cssm_acl_process_subject_selector-swift.struct/init(version:mask:uid:gid:))

#### Instance Properties

- [var gid: uint32](/documentation/security/cssm_acl_process_subject_selector-swift.struct/gid)
- [var mask: uint16](/documentation/security/cssm_acl_process_subject_selector-swift.struct/mask)
- [var uid: uint32](/documentation/security/cssm_acl_process_subject_selector-swift.struct/uid)
- [var version: uint16](/documentation/security/cssm_acl_process_subject_selector-swift.struct/version)
- [cssm_appledl_open_parameters_mask](/documentation/security/cssm_appledl_open_parameters_mask)

#### Initializers

- [init(UInt32)](/documentation/security/cssm_appledl_open_parameters_mask/init(_:))
- [init(rawValue: UInt32)](/documentation/security/cssm_appledl_open_parameters_mask/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/security/cssm_appledl_open_parameters_mask/rawvalue)

### Functions

- [func cssmAlgToOid(CSSM_ALGORITHMS) -> UnsafePointer<SecAsn1Oid>!](/documentation/security/cssmalgtooid(_:))
- [func cssmOidToAlg(UnsafePointer<SecAsn1Oid>!, UnsafeMutablePointer<CSSM_ALGORITHMS>!) -> Bool](/documentation/security/cssmoidtoalg(_:_:))
- [func cssmPerror(UnsafePointer<CChar>!, CSSM_RETURN)](/documentation/security/cssmperror(_:_:))

### Macros

- [var BER_TAG_BIT_STRING: Int32](/documentation/security/ber_tag_bit_string)
- [var BER_TAG_ENUMERATED: Int32](/documentation/security/ber_tag_enumerated)
- [var BER_TAG_GENERALIZED_TIME: Int32](/documentation/security/ber_tag_generalized_time)
- [var BER_TAG_GENERAL_STRING: Int32](/documentation/security/ber_tag_general_string)
- [var BER_TAG_GRAPHIC_STRING: Int32](/documentation/security/ber_tag_graphic_string)
- [var BER_TAG_IA5_STRING: Int32](/documentation/security/ber_tag_ia5_string)
- [var BER_TAG_INTEGER: Int32](/documentation/security/ber_tag_integer)
- [var BER_TAG_ISO646_STRING: Int32](/documentation/security/ber_tag_iso646_string)
- [var BER_TAG_NULL: Int32](/documentation/security/ber_tag_null)
- [var BER_TAG_NUMERIC_STRING: Int32](/documentation/security/ber_tag_numeric_string)
- [var BER_TAG_OBJECT_DESCRIPTOR: Int32](/documentation/security/ber_tag_object_descriptor)
- [var BER_TAG_OCTET_STRING: Int32](/documentation/security/ber_tag_octet_string)
- [var BER_TAG_OID: Int32](/documentation/security/ber_tag_oid)
- [var BER_TAG_PKIX_BMP_STRING: Int32](/documentation/security/ber_tag_pkix_bmp_string)
- [var BER_TAG_PKIX_UNIVERSAL_STRING: Int32](/documentation/security/ber_tag_pkix_universal_string)
- [var BER_TAG_PKIX_UTF8_STRING: Int32](/documentation/security/ber_tag_pkix_utf8_string)
- [var BER_TAG_PRINTABLE_STRING: Int32](/documentation/security/ber_tag_printable_string)
- [var BER_TAG_REAL: Int32](/documentation/security/ber_tag_real)
- [var BER_TAG_SEQUENCE: Int32](/documentation/security/ber_tag_sequence)
- [var BER_TAG_SET: Int32](/documentation/security/ber_tag_set)
- [var BER_TAG_T61_STRING: Int32](/documentation/security/ber_tag_t61_string)
- [var BER_TAG_TELETEX_STRING: Int32](/documentation/security/ber_tag_teletex_string)
- [var BER_TAG_UNKNOWN: Int32](/documentation/security/ber_tag_unknown)
- [var BER_TAG_UTC_TIME: Int32](/documentation/security/ber_tag_utc_time)
- [var BER_TAG_VIDEOTEX_STRING: Int32](/documentation/security/ber_tag_videotex_string)
- [var BER_TAG_VISIBLE_STRING: Int32](/documentation/security/ber_tag_visible_string)
- [var CE_NCT_ObjSign: Int32](/documentation/security/ce_nct_objsign)
- [var CE_NCT_ObjSignCA: Int32](/documentation/security/ce_nct_objsignca)
- [var CE_NCT_Reserved: Int32](/documentation/security/ce_nct_reserved)
- [var CE_NCT_SMIME: Int32](/documentation/security/ce_nct_smime)
- [var CE_NCT_SMIME_CA: Int32](/documentation/security/ce_nct_smime_ca)
- [var CE_NCT_SSL_CA: Int32](/documentation/security/ce_nct_ssl_ca)
- [var CE_NCT_SSL_Client: Int32](/documentation/security/ce_nct_ssl_client)
- [var CE_NCT_SSL_Server: Int32](/documentation/security/ce_nct_ssl_server)
- [var CSSM_APPLE_CRL_END_OF_TIME: String](/documentation/security/cssm_apple_crl_end_of_time)
- [var CSSM_APPLE_TP_ACTION_VERSION: Int32](/documentation/security/cssm_apple_tp_action_version)
- [var CSSM_APPLE_TP_CRL_OPTS_VERSION: Int32](/documentation/security/cssm_apple_tp_crl_opts_version)
- [var CSSM_APPLE_TP_SMIME_OPTS_VERSION: Int32](/documentation/security/cssm_apple_tp_smime_opts_version)
- [var CSSM_APPLE_TP_SSL_CLIENT: Int32](/documentation/security/cssm_apple_tp_ssl_client)
- [var CSSM_APPLE_TP_SSL_OPTS_VERSION: Int32](/documentation/security/cssm_apple_tp_ssl_opts_version)
- [var CSSM_DB_ATTRIBUTE_MDS_END: Int32](/documentation/security/cssm_db_attribute_mds_end)
- [var CSSM_DB_ATTRIBUTE_MDS_START: Int32](/documentation/security/cssm_db_attribute_mds_start)
- [var CSSM_DB_RELATIONID_MDS_END: Int32](/documentation/security/cssm_db_relationid_mds_end)
- [var CSSM_DB_RELATIONID_MDS_START: Int32](/documentation/security/cssm_db_relationid_mds_start)
- [var CSSM_EVIDENCE_FORM_APPLE_CUSTOM: UInt32](/documentation/security/cssm_evidence_form_apple_custom)
- [var CSSM_HINT_CALLBACK: Int32](/documentation/security/cssm_hint_callback)
- [var CSSM_KR_DROP_WORKFACTOR: Int32](/documentation/security/cssm_kr_drop_workfactor)
- [var CSSM_KR_ENT: Int32](/documentation/security/cssm_kr_ent)
- [var CSSM_KR_ENT_POLICY: Int32](/documentation/security/cssm_kr_ent_policy)
- [var CSSM_KR_INDIV: Int32](/documentation/security/cssm_kr_indiv)
- [var CSSM_KR_INDIV_POLICY: Int32](/documentation/security/cssm_kr_indiv_policy)
- [var CSSM_KR_LE: Int32](/documentation/security/cssm_kr_le)
- [var CSSM_KR_LE_MAN: Int32](/documentation/security/cssm_kr_le_man)
- [var CSSM_KR_LE_MAN_POLICY: Int32](/documentation/security/cssm_kr_le_man_policy)
- [var CSSM_KR_LE_USE: Int32](/documentation/security/cssm_kr_le_use)
- [var CSSM_KR_LE_USE_POLICY: Int32](/documentation/security/cssm_kr_le_use_policy)
- [var CSSM_KR_OPTIMIZE: Int32](/documentation/security/cssm_kr_optimize)
- [var CSSM_MANAGER_REPLY: Int32](/documentation/security/cssm_manager_reply)
- [var CSSM_MANAGER_SERVICE_REQUEST: Int32](/documentation/security/cssm_manager_service_request)
- [var CSSM_TP_APPLE_EVIDENCE_VERSION: Int32](/documentation/security/cssm_tp_apple_evidence_version)

### Enumerations

- [Anonymous](/documentation/security/1434707-anonymous)

#### Constants

- [var CSSM_APPLEFILEDL_MAKE_BACKUP: Int](/documentation/security/cssm_applefiledl_make_backup)
- [var CSSM_APPLEFILEDL_TAKE_FILE_LOCK: Int](/documentation/security/cssm_applefiledl_take_file_lock)
- [var CSSM_APPLEFILEDL_DELETE_FILE: Int](/documentation/security/cssm_applefiledl_delete_file)
- [var CSSM_APPLEFILEDL_MAKE_COPY: Int](/documentation/security/cssm_applefiledl_make_copy)
- [Anonymous](/documentation/security/1434766-anonymous)

#### Constants

- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_19: Int](/documentation/security/cssm_apple_private_cspdl_code_19)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_20: Int](/documentation/security/cssm_apple_private_cspdl_code_20)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_21: Int](/documentation/security/cssm_apple_private_cspdl_code_21)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_22: Int](/documentation/security/cssm_apple_private_cspdl_code_22)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_23: Int](/documentation/security/cssm_apple_private_cspdl_code_23)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_24: Int](/documentation/security/cssm_apple_private_cspdl_code_24)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_25: Int](/documentation/security/cssm_apple_private_cspdl_code_25)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_26: Int](/documentation/security/cssm_apple_private_cspdl_code_26)
- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_27: Int](/documentation/security/cssm_apple_private_cspdl_code_27)
- [Anonymous](/documentation/security/1434818-anonymous)

#### Constants

- [var CSSM_WORDID_PARTITION: Int](/documentation/security/cssm_wordid_partition)
- [var CSSM_WORDID_KEYBAG_KEY: Int](/documentation/security/cssm_wordid_keybag_key)
- [Anonymous](/documentation/security/1434848-anonymous)

#### Constants

- [var CSSM_ACL_AUTHORIZATION_INTEGRITY: Int](/documentation/security/cssm_acl_authorization_integrity)
- [var CSSM_ACL_AUTHORIZATION_PARTITION_ID: Int](/documentation/security/cssm_acl_authorization_partition_id)
- [Anonymous](/documentation/security/1434858-anonymous)

#### Constants

- [var CSSM_ACL_SUBJECT_TYPE_PARTITION: Int](/documentation/security/cssm_acl_subject_type_partition)
- [Anonymous](/documentation/security/1434897-anonymous)

#### Constants

- [var CSSMERR_APPLETP_CA_PIN_MISMATCH: Int](/documentation/security/cssmerr_appletp_ca_pin_mismatch)

### Type aliases

- [CSSM_ACL_AUTHORIZATION_TAG](/documentation/security/cssm_acl_authorization_tag)
- [CSSM_ACL_EDIT_MODE](/documentation/security/cssm_acl_edit_mode)
- [CSSM_ACL_HANDLE](/documentation/security/cssm_acl_handle)
- [CSSM_ACL_KEYCHAIN_PROMPT_SELECTOR](/documentation/security/cssm_acl_keychain_prompt_selector-swift.typealias)
- [CSSM_ACL_PREAUTH_TRACKING_STATE](/documentation/security/cssm_acl_preauth_tracking_state)
- [CSSM_ACL_PROCESS_SUBJECT_SELECTOR](/documentation/security/cssm_acl_process_subject_selector-swift.typealias)
- [CSSM_ACL_SUBJECT_TYPE](/documentation/security/cssm_acl_subject_type)
- [CSSM_AC_HANDLE](/documentation/security/cssm_ac_handle)
- [CSSM_ALGORITHMS](/documentation/security/cssm_algorithms)
- [CSSM_APPLECSPDL_DB_CHANGE_PASSWORD_PARAMETERS](/documentation/security/cssm_applecspdl_db_change_password_parameters-swift.typealias)
- [CSSM_APPLECSPDL_DB_CHANGE_PASSWORD_PARAMETERS_PTR](/documentation/security/cssm_applecspdl_db_change_password_parameters_ptr)
- [CSSM_APPLECSPDL_DB_IS_LOCKED_PARAMETERS](/documentation/security/cssm_applecspdl_db_is_locked_parameters-swift.typealias)
- [CSSM_APPLECSPDL_DB_IS_LOCKED_PARAMETERS_PTR](/documentation/security/cssm_applecspdl_db_is_locked_parameters_ptr)
- [CSSM_APPLECSPDL_DB_SETTINGS_PARAMETERS](/documentation/security/cssm_applecspdl_db_settings_parameters-swift.typealias)
- [CSSM_APPLECSPDL_DB_SETTINGS_PARAMETERS_PTR](/documentation/security/cssm_applecspdl_db_settings_parameters_ptr)
- [CSSM_APPLEDL_OPEN_PARAMETERS](/documentation/security/cssm_appledl_open_parameters-swift.typealias)
- [CSSM_APPLEDL_OPEN_PARAMETERS_PTR](/documentation/security/cssm_appledl_open_parameters_ptr)
- [CSSM_APPLE_TP_ACTION_FLAGS](/documentation/security/cssm_apple_tp_action_flags)
- [CSSM_APPLE_TP_CRL_OPT_FLAGS](/documentation/security/cssm_apple_tp_crl_opt_flags)
- [CSSM_ATTACH_FLAGS](/documentation/security/cssm_attach_flags)
- [CSSM_ATTRIBUTE_TYPE](/documentation/security/cssm_attribute_type)
- [CSSM_BER_TAG](/documentation/security/cssm_ber_tag)
- [CSSM_BITMASK](/documentation/security/cssm_bitmask)
- [CSSM_BOOL](/documentation/security/cssm_bool)
- [CSSM_CALLOC](/documentation/security/cssm_calloc)
- [CSSM_CC_HANDLE](/documentation/security/cssm_cc_handle)
- [CSSM_CERTGROUP_TYPE](/documentation/security/cssm_certgroup_type)
- [CSSM_CERTGROUP_TYPE_PTR](/documentation/security/cssm_certgroup_type_ptr)
- [CSSM_CERT_BUNDLE_ENCODING](/documentation/security/cssm_cert_bundle_encoding)
- [CSSM_CERT_BUNDLE_TYPE](/documentation/security/cssm_cert_bundle_type)
- [CSSM_CERT_ENCODING](/documentation/security/cssm_cert_encoding)
- [CSSM_CERT_ENCODING_PTR](/documentation/security/cssm_cert_encoding_ptr)
- [CSSM_CERT_PARSE_FORMAT](/documentation/security/cssm_cert_parse_format)
- [CSSM_CERT_PARSE_FORMAT_PTR](/documentation/security/cssm_cert_parse_format_ptr)
- [CSSM_CERT_TYPE](/documentation/security/cssm_cert_type)
- [CSSM_CERT_TYPE_PTR](/documentation/security/cssm_cert_type_ptr)
- [CSSM_CL_HANDLE](/documentation/security/cssm_cl_handle)
- [CSSM_CL_TEMPLATE_TYPE](/documentation/security/cssm_cl_template_type)
- [CSSM_CONTEXT_EVENT](/documentation/security/cssm_context_event)
- [CSSM_CONTEXT_TYPE](/documentation/security/cssm_context_type)
- [CSSM_CRLGROUP_TYPE](/documentation/security/cssm_crlgroup_type)
- [CSSM_CRLGROUP_TYPE_PTR](/documentation/security/cssm_crlgroup_type_ptr)
- [CSSM_CRL_ENCODING](/documentation/security/cssm_crl_encoding)
- [CSSM_CRL_ENCODING_PTR](/documentation/security/cssm_crl_encoding_ptr)
- [CSSM_CRL_PARSE_FORMAT](/documentation/security/cssm_crl_parse_format)
- [CSSM_CRL_PARSE_FORMAT_PTR](/documentation/security/cssm_crl_parse_format_ptr)
- [CSSM_CRL_TYPE](/documentation/security/cssm_crl_type)
- [CSSM_CRL_TYPE_PTR](/documentation/security/cssm_crl_type_ptr)
- [CSSM_CSPTYPE](/documentation/security/cssm_csptype)
- [CSSM_CSP_FLAGS](/documentation/security/cssm_csp_flags)
- [CSSM_CSP_HANDLE](/documentation/security/cssm_csp_handle)
- [CSSM_CSP_READER_FLAGS](/documentation/security/cssm_csp_reader_flags)
- [CSSM_DB_ACCESS_TYPE](/documentation/security/cssm_db_access_type)
- [CSSM_DB_ACCESS_TYPE_PTR](/documentation/security/cssm_db_access_type_ptr)
- [CSSM_DB_ATTRIBUTE_FORMAT](/documentation/security/cssm_db_attribute_format)
- [CSSM_DB_ATTRIBUTE_FORMAT_PTR](/documentation/security/cssm_db_attribute_format_ptr)
- [CSSM_DB_ATTRIBUTE_NAME_FORMAT](/documentation/security/cssm_db_attribute_name_format)
- [CSSM_DB_ATTRIBUTE_NAME_FORMAT_PTR](/documentation/security/cssm_db_attribute_name_format_ptr)
- [CSSM_DB_CONJUNCTIVE](/documentation/security/cssm_db_conjunctive)
- [CSSM_DB_CONJUNCTIVE_PTR](/documentation/security/cssm_db_conjunctive_ptr)
- [CSSM_DB_HANDLE](/documentation/security/cssm_db_handle)
- [CSSM_DB_INDEXED_DATA_LOCATION](/documentation/security/cssm_db_indexed_data_location)
- [CSSM_DB_INDEX_TYPE](/documentation/security/cssm_db_index_type)
- [CSSM_DB_MODIFY_MODE](/documentation/security/cssm_db_modify_mode)
- [CSSM_DB_OPERATOR](/documentation/security/cssm_db_operator)
- [CSSM_DB_OPERATOR_PTR](/documentation/security/cssm_db_operator_ptr)
- [CSSM_DB_RECORDTYPE](/documentation/security/cssm_db_recordtype)
- [CSSM_DB_RETRIEVAL_MODES](/documentation/security/cssm_db_retrieval_modes)
- [CSSM_DLTYPE](/documentation/security/cssm_dltype)
- [CSSM_DLTYPE_PTR](/documentation/security/cssm_dltype_ptr)
- [CSSM_DL_CUSTOM_ATTRIBUTES](/documentation/security/cssm_dl_custom_attributes)
- [CSSM_DL_FFS_ATTRIBUTES](/documentation/security/cssm_dl_ffs_attributes)
- [CSSM_DL_HANDLE](/documentation/security/cssm_dl_handle)
- [CSSM_DL_LDAP_ATTRIBUTES](/documentation/security/cssm_dl_ldap_attributes)
- [CSSM_DL_ODBC_ATTRIBUTES](/documentation/security/cssm_dl_odbc_attributes)
- [CSSM_DL_PKCS11_ATTRIBUTE](/documentation/security/cssm_dl_pkcs11_attribute)
- [CSSM_DL_PKCS11_ATTRIBUTE_PTR](/documentation/security/cssm_dl_pkcs11_attribute_ptr)
- [CSSM_ENCRYPT_MODE](/documentation/security/cssm_encrypt_mode)
- [CSSM_EVIDENCE_FORM](/documentation/security/cssm_evidence_form)
- [CSSM_FREE](/documentation/security/cssm_free)
- [CSSM_HANDLE](/documentation/security/cssm_handle)
- [CSSM_HANDLE_PTR](/documentation/security/cssm_handle_ptr)
- [CSSM_HEADERVERSION](/documentation/security/cssm_headerversion)
- [CSSM_INTPTR](/documentation/security/cssm_intptr)
- [CSSM_KEYATTR_FLAGS](/documentation/security/cssm_keyattr_flags)
- [CSSM_KEYBLOB_FORMAT](/documentation/security/cssm_keyblob_format)
- [CSSM_KEYBLOB_TYPE](/documentation/security/cssm_keyblob_type)
- [CSSM_KEYCLASS](/documentation/security/cssm_keyclass)
- [CSSM_KEYUSE](/documentation/security/cssm_keyuse)
- [CSSM_KEY_HIERARCHY](/documentation/security/cssm_key_hierarchy)
- [CSSM_KEY_TYPE](/documentation/security/cssm_key_type)
- [CSSM_KRSP_HANDLE](/documentation/security/cssm_krsp_handle)
- [CSSM_KR_POLICY_FLAGS](/documentation/security/cssm_kr_policy_flags)
- [CSSM_KR_POLICY_TYPE](/documentation/security/cssm_kr_policy_type)
- [CSSM_LIST_ELEMENT_PTR](/documentation/security/cssm_list_element_ptr)
- [CSSM_LIST_ELEMENT_TYPE](/documentation/security/cssm_list_element_type)
- [CSSM_LIST_ELEMENT_TYPE_PTR](/documentation/security/cssm_list_element_type_ptr)
- [CSSM_LIST_TYPE](/documentation/security/cssm_list_type)
- [CSSM_LIST_TYPE_PTR](/documentation/security/cssm_list_type_ptr)
- [CSSM_LONG_HANDLE](/documentation/security/cssm_long_handle)
- [CSSM_LONG_HANDLE_PTR](/documentation/security/cssm_long_handle_ptr)
- [CSSM_MALLOC](/documentation/security/cssm_malloc)
- [CSSM_MANAGER_EVENT_TYPES](/documentation/security/cssm_manager_event_types)
- [CSSM_MODULE_EVENT](/documentation/security/cssm_module_event)
- [CSSM_MODULE_EVENT_PTR](/documentation/security/cssm_module_event_ptr)
- [CSSM_MODULE_HANDLE](/documentation/security/cssm_module_handle)
- [CSSM_MODULE_HANDLE_PTR](/documentation/security/cssm_module_handle_ptr)
- [CSSM_NET_ADDRESS_TYPE](/documentation/security/cssm_net_address_type)
- [CSSM_NET_PROTOCOL](/documentation/security/cssm_net_protocol)
- [CSSM_PADDING](/documentation/security/cssm_padding)
- [CSSM_PKCS5_PBKDF2_PRF](/documentation/security/cssm_pkcs5_pbkdf2_prf)
- [CSSM_PKCS_OAEP_MGF](/documentation/security/cssm_pkcs_oaep_mgf)
- [CSSM_PKCS_OAEP_PSOURCE](/documentation/security/cssm_pkcs_oaep_psource)
- [CSSM_PRIVILEGE](/documentation/security/cssm_privilege)
- [CSSM_PRIVILEGE_SCOPE](/documentation/security/cssm_privilege_scope)
- [CSSM_PROC_ADDR](/documentation/security/cssm_proc_addr)
- [CSSM_PROC_ADDR_PTR](/documentation/security/cssm_proc_addr_ptr)
- [CSSM_PVC_MODE](/documentation/security/cssm_pvc_mode)
- [CSSM_QUERY_FLAGS](/documentation/security/cssm_query_flags)
- [CSSM_REALLOC](/documentation/security/cssm_realloc)
- [CSSM_RETURN](/documentation/security/cssm_return)
- [CSSM_SAMPLE_TYPE](/documentation/security/cssm_sample_type)
- [CSSM_SC_FLAGS](/documentation/security/cssm_sc_flags)
- [CSSM_SERVICE_MASK](/documentation/security/cssm_service_mask)
- [CSSM_SERVICE_TYPE](/documentation/security/cssm_service_type)
- [CSSM_SIZE](/documentation/security/cssm_size)
- [CSSM_STRING](/documentation/security/cssm_string)
- [CSSM_TIMESTRING](/documentation/security/cssm_timestring)
- [CSSM_TP_ACTION](/documentation/security/cssm_tp_action)
- [CSSM_TP_APPLE_CERT_STATUS](/documentation/security/cssm_tp_apple_cert_status)
- [CSSM_TP_AUTHORITY_REQUEST_TYPE](/documentation/security/cssm_tp_authority_request_type)
- [CSSM_TP_AUTHORITY_REQUEST_TYPE_PTR](/documentation/security/cssm_tp_authority_request_type_ptr)
- [CSSM_TP_CERTCHANGE_ACTION](/documentation/security/cssm_tp_certchange_action)
- [CSSM_TP_CERTCHANGE_REASON](/documentation/security/cssm_tp_certchange_reason)
- [CSSM_TP_CERTCHANGE_STATUS](/documentation/security/cssm_tp_certchange_status)
- [CSSM_TP_CERTISSUE_STATUS](/documentation/security/cssm_tp_certissue_status)
- [CSSM_TP_CERTNOTARIZE_STATUS](/documentation/security/cssm_tp_certnotarize_status)
- [CSSM_TP_CERTRECLAIM_STATUS](/documentation/security/cssm_tp_certreclaim_status)
- [CSSM_TP_CERTVERIFY_STATUS](/documentation/security/cssm_tp_certverify_status)
- [CSSM_TP_CONFIRM_STATUS](/documentation/security/cssm_tp_confirm_status)
- [CSSM_TP_CONFIRM_STATUS_PTR](/documentation/security/cssm_tp_confirm_status_ptr)
- [CSSM_TP_CRLISSUE_STATUS](/documentation/security/cssm_tp_crlissue_status)
- [CSSM_TP_FORM_TYPE](/documentation/security/cssm_tp_form_type)
- [CSSM_TP_HANDLE](/documentation/security/cssm_tp_handle)
- [CSSM_TP_SERVICES](/documentation/security/cssm_tp_services)
- [CSSM_TP_STOP_ON](/documentation/security/cssm_tp_stop_on)
- [CSSM_USEE_TAG](/documentation/security/cssm_usee_tag)
- [CSSM_WORDID_TYPE](/documentation/security/cssm_wordid_type)
- [CSSM_X509EXT_DATA_FORMAT](/documentation/security/cssm_x509ext_data_format)
- [CSSM_X509_OPTION](/documentation/security/cssm_x509_option)

### Apple Specific

- [var kKeychainDbSuffix: String](/documentation/security/kkeychaindbsuffix)
- [Secure Transport](/documentation/security/secure-transport)

### First Steps

- [Using the Secure Socket Layer for Network Communication](/documentation/security/using-the-secure-socket-layer-for-network-communication)

### Session Context

- [func SSLCreateContext(CFAllocator?, SSLProtocolSide, SSLConnectionType) -> SSLContext?](/documentation/security/sslcreatecontext(_:_:_:))
- [SSLProtocolSide](/documentation/security/sslprotocolside)

#### Constants

- [case serverSide](/documentation/security/sslprotocolside/serverside)
- [case clientSide](/documentation/security/sslprotocolside/clientside)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslprotocolside/init(rawvalue:))
- [SSLConnectionType](/documentation/security/sslconnectiontype)

#### Constants

- [case streamType](/documentation/security/sslconnectiontype/streamtype)
- [case datagramType](/documentation/security/sslconnectiontype/datagramtype)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslconnectiontype/init(rawvalue:))
- [SSLContext](/documentation/security/sslcontext)
- [func SSLContextGetTypeID() -> CFTypeID](/documentation/security/sslcontextgettypeid())

### Context Options

- [func SSLSetSessionOption(SSLContext, SSLSessionOption, Bool) -> OSStatus](/documentation/security/sslsetsessionoption(_:_:_:))
- [func SSLGetSessionOption(SSLContext, SSLSessionOption, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/security/sslgetsessionoption(_:_:_:))
- [SSLSessionOption](/documentation/security/sslsessionoption)

#### Constants

- [case breakOnServerAuth](/documentation/security/sslsessionoption/breakonserverauth)
- [case breakOnCertRequested](/documentation/security/sslsessionoption/breakoncertrequested)
- [case breakOnClientAuth](/documentation/security/sslsessionoption/breakonclientauth)
- [case falseStart](/documentation/security/sslsessionoption/falsestart)
- [case sendOneByteRecord](/documentation/security/sslsessionoption/sendonebyterecord)
- [case allowServerIdentityChange](/documentation/security/sslsessionoption/allowserveridentitychange)
- [case fallback](/documentation/security/sslsessionoption/fallback)
- [case breakOnClientHello](/documentation/security/sslsessionoption/breakonclienthello)
- [case allowRenegotiation](/documentation/security/sslsessionoption/allowrenegotiation)
- [case enableSessionTickets](/documentation/security/sslsessionoption/enablesessiontickets)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslsessionoption/init(rawvalue:))

### Context Callbacks

- [func SSLSetIOFuncs(SSLContext, SSLReadFunc, SSLWriteFunc) -> OSStatus](/documentation/security/sslsetiofuncs(_:_:_:))
- [SSLReadFunc](/documentation/security/sslreadfunc)
- [SSLWriteFunc](/documentation/security/sslwritefunc)

### Session Configuration

- [func SSLSetSessionConfig(SSLContext, CFString) -> OSStatus](/documentation/security/sslsetsessionconfig(_:_:))
- [func SSLSetClientSideAuthenticate(SSLContext, SSLAuthenticate) -> OSStatus](/documentation/security/sslsetclientsideauthenticate(_:_:))
- [SSLConfig](/documentation/security/sslconfig)

#### Constants

- [let kSSLSessionConfig_3DES_fallback: CFString](/documentation/security/ksslsessionconfig_3des_fallback)
- [let kSSLSessionConfig_ATSv1: CFString](/documentation/security/ksslsessionconfig_atsv1)
- [let kSSLSessionConfig_ATSv1_noPFS: CFString](/documentation/security/ksslsessionconfig_atsv1_nopfs)
- [let kSSLSessionConfig_RC4_fallback: CFString](/documentation/security/ksslsessionconfig_rc4_fallback)
- [let kSSLSessionConfig_TLSv1_3DES_fallback: CFString](/documentation/security/ksslsessionconfig_tlsv1_3des_fallback)
- [let kSSLSessionConfig_TLSv1_RC4_fallback: CFString](/documentation/security/ksslsessionconfig_tlsv1_rc4_fallback)
- [let kSSLSessionConfig_TLSv1_fallback: CFString](/documentation/security/ksslsessionconfig_tlsv1_fallback)
- [let kSSLSessionConfig_anonymous: CFString](/documentation/security/ksslsessionconfig_anonymous)
- [let kSSLSessionConfig_default: CFString](/documentation/security/ksslsessionconfig_default)
- [let kSSLSessionConfig_legacy: CFString](/documentation/security/ksslsessionconfig_legacy)
- [let kSSLSessionConfig_legacy_DHE: CFString](/documentation/security/ksslsessionconfig_legacy_dhe)
- [let kSSLSessionConfig_standard: CFString](/documentation/security/ksslsessionconfig_standard)
- [SSLAuthenticate](/documentation/security/sslauthenticate)

#### Constants

- [case neverAuthenticate](/documentation/security/sslauthenticate/neverauthenticate)
- [case alwaysAuthenticate](/documentation/security/sslauthenticate/alwaysauthenticate)
- [case tryAuthenticate](/documentation/security/sslauthenticate/tryauthenticate)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslauthenticate/init(rawvalue:))

### I/O Connections

- [func SSLSetConnection(SSLContext, SSLConnectionRef?) -> OSStatus](/documentation/security/sslsetconnection(_:_:))
- [func SSLGetConnection(SSLContext, UnsafeMutablePointer<SSLConnectionRef?>) -> OSStatus](/documentation/security/sslgetconnection(_:_:))
- [SSLConnectionRef](/documentation/security/sslconnectionref)

### Session State

- [func SSLHandshake(SSLContext) -> OSStatus](/documentation/security/sslhandshake(_:))
- [func SSLReHandshake(SSLContext) -> OSStatus](/documentation/security/sslrehandshake(_:))
- [func SSLClose(SSLContext) -> OSStatus](/documentation/security/sslclose(_:))
- [func SSLSetPeerID(SSLContext, UnsafeRawPointer?, Int) -> OSStatus](/documentation/security/sslsetpeerid(_:_:_:))
- [func SSLGetPeerID(SSLContext, UnsafeMutablePointer<UnsafeRawPointer?>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetpeerid(_:_:_:))
- [func SSLGetSessionState(SSLContext, UnsafeMutablePointer<SSLSessionState>) -> OSStatus](/documentation/security/sslgetsessionstate(_:_:))
- [SSLSessionState](/documentation/security/sslsessionstate)

#### Constants

- [case idle](/documentation/security/sslsessionstate/idle)
- [case handshake](/documentation/security/sslsessionstate/handshake)
- [case connected](/documentation/security/sslsessionstate/connected)
- [case closed](/documentation/security/sslsessionstate/closed)
- [case aborted](/documentation/security/sslsessionstate/aborted)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslsessionstate/init(rawvalue:))
- [func SSLSetError(SSLContext, OSStatus) -> OSStatus](/documentation/security/sslseterror(_:_:))

### Read Operations

- [func SSLRead(SSLContext, UnsafeMutableRawPointer, Int, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslread(_:_:_:_:))
- [func SSLGetBufferedReadSize(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetbufferedreadsize(_:_:))

### Write Operations

- [func SSLWrite(SSLContext, UnsafeRawPointer?, Int, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslwrite(_:_:_:_:))
- [func SSLGetDatagramWriteSize(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetdatagramwritesize(_:_:))
- [func SSLGetMaxDatagramRecordSize(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetmaxdatagramrecordsize(_:_:))
- [func SSLSetMaxDatagramRecordSize(SSLContext, Int) -> OSStatus](/documentation/security/sslsetmaxdatagramrecordsize(_:_:))
- [func SSLSetDatagramHelloCookie(SSLContext, UnsafeRawPointer?, Int) -> OSStatus](/documentation/security/sslsetdatagramhellocookie(_:_:_:))

### The Peer Domain Name

- [func SSLSetPeerDomainName(SSLContext, UnsafePointer<CChar>?, Int) -> OSStatus](/documentation/security/sslsetpeerdomainname(_:_:_:))
- [func SSLGetPeerDomainNameLength(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetpeerdomainnamelength(_:_:))
- [func SSLGetPeerDomainName(SSLContext, UnsafeMutablePointer<CChar>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetpeerdomainname(_:_:_:))
- [func SSLCopyRequestedPeerName(SSLContext, UnsafeMutablePointer<CChar>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslcopyrequestedpeername(_:_:_:))
- [func SSLCopyRequestedPeerNameLength(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslcopyrequestedpeernamelength(_:_:))

### Versions

- [func SSLSetProtocolVersionMax(SSLContext, SSLProtocol) -> OSStatus](/documentation/security/sslsetprotocolversionmax(_:_:))
- [func SSLSetProtocolVersionMin(SSLContext, SSLProtocol) -> OSStatus](/documentation/security/sslsetprotocolversionmin(_:_:))
- [func SSLGetProtocolVersionMax(SSLContext, UnsafeMutablePointer<SSLProtocol>) -> OSStatus](/documentation/security/sslgetprotocolversionmax(_:_:))
- [func SSLGetProtocolVersionMin(SSLContext, UnsafeMutablePointer<SSLProtocol>) -> OSStatus](/documentation/security/sslgetprotocolversionmin(_:_:))
- [func SSLGetNegotiatedProtocolVersion(SSLContext, UnsafeMutablePointer<SSLProtocol>) -> OSStatus](/documentation/security/sslgetnegotiatedprotocolversion(_:_:))
- [tls_protocol_version_t](/documentation/security/tls_protocol_version_t)

#### Protocol Versions

- [case TLSv10](/documentation/security/tls_protocol_version_t/tlsv10)
- [case TLSv11](/documentation/security/tls_protocol_version_t/tlsv11)
- [case TLSv12](/documentation/security/tls_protocol_version_t/tlsv12)
- [case TLSv13](/documentation/security/tls_protocol_version_t/tlsv13)
- [case DTLSv10](/documentation/security/tls_protocol_version_t/dtlsv10)
- [case DTLSv12](/documentation/security/tls_protocol_version_t/dtlsv12)

#### Initializers

- [init?(rawValue: UInt16)](/documentation/security/tls_protocol_version_t/init(rawvalue:))
- [SSLProtocol](/documentation/security/sslprotocol)

#### SSL Protocols

- [case sslProtocolUnknown](/documentation/security/sslprotocol/sslprotocolunknown)
- [case sslProtocol2](/documentation/security/sslprotocol/sslprotocol2)
- [case sslProtocol3](/documentation/security/sslprotocol/sslprotocol3)
- [case sslProtocol3Only](/documentation/security/sslprotocol/sslprotocol3only)
- [case sslProtocolAll](/documentation/security/sslprotocol/sslprotocolall)

#### TLS Protocols

- [case tlsProtocol1](/documentation/security/sslprotocol/tlsprotocol1)
- [case tlsProtocol1Only](/documentation/security/sslprotocol/tlsprotocol1only)
- [case tlsProtocol11](/documentation/security/sslprotocol/tlsprotocol11)
- [case tlsProtocol12](/documentation/security/sslprotocol/tlsprotocol12)
- [case tlsProtocol13](/documentation/security/sslprotocol/tlsprotocol13)
- [case tlsProtocolMaxSupported](/documentation/security/sslprotocol/tlsprotocolmaxsupported)

#### DTLS Protocols

- [case dtlsProtocol1](/documentation/security/sslprotocol/dtlsprotocol1)
- [case dtlsProtocol12](/documentation/security/sslprotocol/dtlsprotocol12)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslprotocol/init(rawvalue:))

### Application Layer Protocols

- [func SSLCopyALPNProtocols(SSLContext, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/security/sslcopyalpnprotocols(_:_:))
- [func SSLSetALPNProtocols(SSLContext, CFArray) -> OSStatus](/documentation/security/sslsetalpnprotocols(_:_:))

### Ciphers

- [func SSLGetNumberSupportedCiphers(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetnumbersupportedciphers(_:_:))
- [func SSLGetSupportedCiphers(SSLContext, UnsafeMutablePointer<SSLCipherSuite>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetsupportedciphers(_:_:_:))
- [func SSLSetEnabledCiphers(SSLContext, UnsafePointer<SSLCipherSuite>, Int) -> OSStatus](/documentation/security/sslsetenabledciphers(_:_:_:))
- [func SSLGetNumberEnabledCiphers(SSLContext, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetnumberenabledciphers(_:_:))
- [func SSLGetEnabledCiphers(SSLContext, UnsafeMutablePointer<SSLCipherSuite>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetenabledciphers(_:_:_:))
- [func SSLGetNegotiatedCipher(SSLContext, UnsafeMutablePointer<SSLCipherSuite>) -> OSStatus](/documentation/security/sslgetnegotiatedcipher(_:_:))
- [func SSLSetDiffieHellmanParams(SSLContext, UnsafeRawPointer?, Int) -> OSStatus](/documentation/security/sslsetdiffiehellmanparams(_:_:_:))
- [func SSLGetDiffieHellmanParams(SSLContext, UnsafeMutablePointer<UnsafeRawPointer?>, UnsafeMutablePointer<Int>) -> OSStatus](/documentation/security/sslgetdiffiehellmanparams(_:_:_:))
- [tls_ciphersuite_group_t](/documentation/security/tls_ciphersuite_group_t)

#### Ciphersuite Groups

- [case ats](/documentation/security/tls_ciphersuite_group_t/ats)
- [case ats_compatibility](/documentation/security/tls_ciphersuite_group_t/ats_compatibility)
- [case compatibility](/documentation/security/tls_ciphersuite_group_t/compatibility)
- [case `default`](/documentation/security/tls_ciphersuite_group_t/default)
- [case legacy](/documentation/security/tls_ciphersuite_group_t/legacy)

#### Initializers

- [init?(rawValue: UInt16)](/documentation/security/tls_ciphersuite_group_t/init(rawvalue:))
- [tls_ciphersuite_t](/documentation/security/tls_ciphersuite_t)

#### AES

- [case AES_128_GCM_SHA256](/documentation/security/tls_ciphersuite_t/aes_128_gcm_sha256)
- [case AES_256_GCM_SHA384](/documentation/security/tls_ciphersuite_t/aes_256_gcm_sha384)

#### Cha Cha Poly

- [case CHACHA20_POLY1305_SHA256](/documentation/security/tls_ciphersuite_t/chacha20_poly1305_sha256)

#### Elliptic Curve

- [case ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_3des_ede_cbc_sha)
- [case ECDHE_ECDSA_WITH_AES_128_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_128_cbc_sha)
- [case ECDHE_ECDSA_WITH_AES_128_CBC_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_128_cbc_sha256)
- [case ECDHE_ECDSA_WITH_AES_128_GCM_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_128_gcm_sha256)
- [case ECDHE_ECDSA_WITH_AES_256_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_256_cbc_sha)
- [case ECDHE_ECDSA_WITH_AES_256_CBC_SHA384](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_256_cbc_sha384)
- [case ECDHE_ECDSA_WITH_AES_256_GCM_SHA384](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_aes_256_gcm_sha384)
- [case ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_ecdsa_with_chacha20_poly1305_sha256)
- [case ECDHE_RSA_WITH_3DES_EDE_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_3des_ede_cbc_sha)
- [case ECDHE_RSA_WITH_AES_128_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_128_cbc_sha)
- [case ECDHE_RSA_WITH_AES_128_CBC_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_128_cbc_sha256)
- [case ECDHE_RSA_WITH_AES_128_GCM_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_128_gcm_sha256)
- [case ECDHE_RSA_WITH_AES_256_CBC_SHA](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_256_cbc_sha)
- [case ECDHE_RSA_WITH_AES_256_CBC_SHA384](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_256_cbc_sha384)
- [case ECDHE_RSA_WITH_AES_256_GCM_SHA384](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_aes_256_gcm_sha384)
- [case ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256](/documentation/security/tls_ciphersuite_t/ecdhe_rsa_with_chacha20_poly1305_sha256)

#### RSA

- [case RSA_WITH_3DES_EDE_CBC_SHA](/documentation/security/tls_ciphersuite_t/rsa_with_3des_ede_cbc_sha)
- [case RSA_WITH_AES_128_CBC_SHA](/documentation/security/tls_ciphersuite_t/rsa_with_aes_128_cbc_sha)
- [case RSA_WITH_AES_128_CBC_SHA256](/documentation/security/tls_ciphersuite_t/rsa_with_aes_128_cbc_sha256)
- [case RSA_WITH_AES_128_GCM_SHA256](/documentation/security/tls_ciphersuite_t/rsa_with_aes_128_gcm_sha256)
- [case RSA_WITH_AES_256_CBC_SHA](/documentation/security/tls_ciphersuite_t/rsa_with_aes_256_cbc_sha)
- [case RSA_WITH_AES_256_CBC_SHA256](/documentation/security/tls_ciphersuite_t/rsa_with_aes_256_cbc_sha256)
- [case RSA_WITH_AES_256_GCM_SHA384](/documentation/security/tls_ciphersuite_t/rsa_with_aes_256_gcm_sha384)

#### Initializers

- [init?(rawValue: UInt16)](/documentation/security/tls_ciphersuite_t/init(rawvalue:))
- [SSLCipherSuite](/documentation/security/sslciphersuite)
- [SSLCiphersuiteGroup](/documentation/security/sslciphersuitegroup)

#### Enumeration Cases

- [case `default`](/documentation/security/sslciphersuitegroup/default)
- [case compatibility](/documentation/security/sslciphersuitegroup/compatibility)
- [case legacy](/documentation/security/sslciphersuitegroup/legacy)
- [case ATS](/documentation/security/sslciphersuitegroup/ats)
- [case atsCompatibility](/documentation/security/sslciphersuitegroup/atscompatibility)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslciphersuitegroup/init(rawvalue:))
- [SSL Cipher Suite Values](/documentation/security/ssl-cipher-suite-values)

#### Constants

- [var SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_dss_export_with_des40_cbc_sha)
- [var SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_dss_with_3des_ede_cbc_sha)
- [var SSL_DHE_DSS_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_dss_with_des_cbc_sha)
- [var SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_rsa_export_with_des40_cbc_sha)
- [var SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_rsa_with_3des_ede_cbc_sha)
- [var SSL_DHE_RSA_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dhe_rsa_with_des_cbc_sha)
- [var SSL_DH_DSS_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_dss_export_with_des40_cbc_sha)
- [var SSL_DH_DSS_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_dss_with_3des_ede_cbc_sha)
- [var SSL_DH_DSS_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_dss_with_des_cbc_sha)
- [var SSL_DH_RSA_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_rsa_export_with_des40_cbc_sha)
- [var SSL_DH_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_rsa_with_3des_ede_cbc_sha)
- [var SSL_DH_RSA_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_rsa_with_des_cbc_sha)
- [var SSL_DH_anon_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_anon_export_with_des40_cbc_sha)
- [var SSL_DH_anon_EXPORT_WITH_RC4_40_MD5: SSLCipherSuite](/documentation/security/ssl_dh_anon_export_with_rc4_40_md5)
- [var SSL_DH_anon_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_anon_with_3des_ede_cbc_sha)
- [var SSL_DH_anon_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_dh_anon_with_des_cbc_sha)
- [var SSL_DH_anon_WITH_RC4_128_MD5: SSLCipherSuite](/documentation/security/ssl_dh_anon_with_rc4_128_md5)
- [var SSL_FORTEZZA_DMS_WITH_FORTEZZA_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_fortezza_dms_with_fortezza_cbc_sha)
- [var SSL_FORTEZZA_DMS_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/ssl_fortezza_dms_with_null_sha)
- [var SSL_NO_SUCH_CIPHERSUITE: SSLCipherSuite](/documentation/security/ssl_no_such_ciphersuite)
- [var SSL_NULL_WITH_NULL_NULL: SSLCipherSuite](/documentation/security/ssl_null_with_null_null)
- [var SSL_RSA_EXPORT_WITH_DES40_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_export_with_des40_cbc_sha)
- [var SSL_RSA_EXPORT_WITH_RC2_CBC_40_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_export_with_rc2_cbc_40_md5)
- [var SSL_RSA_EXPORT_WITH_RC4_40_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_export_with_rc4_40_md5)
- [var SSL_RSA_WITH_3DES_EDE_CBC_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_3des_ede_cbc_md5)
- [var SSL_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_with_3des_ede_cbc_sha)
- [var SSL_RSA_WITH_DES_CBC_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_des_cbc_md5)
- [var SSL_RSA_WITH_DES_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_with_des_cbc_sha)
- [var SSL_RSA_WITH_IDEA_CBC_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_idea_cbc_md5)
- [var SSL_RSA_WITH_IDEA_CBC_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_with_idea_cbc_sha)
- [var SSL_RSA_WITH_NULL_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_null_md5)
- [var SSL_RSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_with_null_sha)
- [var SSL_RSA_WITH_RC2_CBC_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_rc2_cbc_md5)
- [var SSL_RSA_WITH_RC4_128_MD5: SSLCipherSuite](/documentation/security/ssl_rsa_with_rc4_128_md5)
- [var SSL_RSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/ssl_rsa_with_rc4_128_sha)
- [var TLS_AES_128_CCM_8_SHA256: SSLCipherSuite](/documentation/security/tls_aes_128_ccm_8_sha256)
- [var TLS_AES_128_CCM_SHA256: SSLCipherSuite](/documentation/security/tls_aes_128_ccm_sha256)
- [var TLS_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_aes_128_gcm_sha256)
- [var TLS_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_aes_256_gcm_sha384)
- [var TLS_CHACHA20_POLY1305_SHA256: SSLCipherSuite](/documentation/security/tls_chacha20_poly1305_sha256)
- [var TLS_DHE_DSS_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_3des_ede_cbc_sha)
- [var TLS_DHE_DSS_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_128_cbc_sha)
- [var TLS_DHE_DSS_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_128_cbc_sha256)
- [var TLS_DHE_DSS_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_128_gcm_sha256)
- [var TLS_DHE_DSS_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_256_cbc_sha)
- [var TLS_DHE_DSS_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_256_cbc_sha256)
- [var TLS_DHE_DSS_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dhe_dss_with_aes_256_gcm_sha384)
- [var TLS_DHE_PSK_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_3des_ede_cbc_sha)
- [var TLS_DHE_PSK_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_128_cbc_sha)
- [var TLS_DHE_PSK_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_128_cbc_sha256)
- [var TLS_DHE_PSK_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_128_gcm_sha256)
- [var TLS_DHE_PSK_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_256_cbc_sha)
- [var TLS_DHE_PSK_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_256_cbc_sha384)
- [var TLS_DHE_PSK_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_aes_256_gcm_sha384)
- [var TLS_DHE_PSK_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_null_sha)
- [var TLS_DHE_PSK_WITH_NULL_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_null_sha256)
- [var TLS_DHE_PSK_WITH_NULL_SHA384: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_null_sha384)
- [var TLS_DHE_PSK_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_dhe_psk_with_rc4_128_sha)
- [var TLS_DHE_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_3des_ede_cbc_sha)
- [var TLS_DHE_RSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_128_cbc_sha)
- [var TLS_DHE_RSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_128_cbc_sha256)
- [var TLS_DHE_RSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_128_gcm_sha256)
- [var TLS_DHE_RSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_256_cbc_sha)
- [var TLS_DHE_RSA_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_256_cbc_sha256)
- [var TLS_DHE_RSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dhe_rsa_with_aes_256_gcm_sha384)
- [var TLS_DH_DSS_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_dss_with_3des_ede_cbc_sha)
- [var TLS_DH_DSS_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_128_cbc_sha)
- [var TLS_DH_DSS_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_128_cbc_sha256)
- [var TLS_DH_DSS_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_128_gcm_sha256)
- [var TLS_DH_DSS_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_256_cbc_sha)
- [var TLS_DH_DSS_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_256_cbc_sha256)
- [var TLS_DH_DSS_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dh_dss_with_aes_256_gcm_sha384)
- [var TLS_DH_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_3des_ede_cbc_sha)
- [var TLS_DH_RSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_128_cbc_sha)
- [var TLS_DH_RSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_128_cbc_sha256)
- [var TLS_DH_RSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_128_gcm_sha256)
- [var TLS_DH_RSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_256_cbc_sha)
- [var TLS_DH_RSA_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_256_cbc_sha256)
- [var TLS_DH_RSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dh_rsa_with_aes_256_gcm_sha384)
- [var TLS_DH_anon_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_anon_with_3des_ede_cbc_sha)
- [var TLS_DH_anon_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_128_cbc_sha)
- [var TLS_DH_anon_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_128_cbc_sha256)
- [var TLS_DH_anon_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_128_gcm_sha256)
- [var TLS_DH_anon_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_256_cbc_sha)
- [var TLS_DH_anon_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_256_cbc_sha256)
- [var TLS_DH_anon_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_dh_anon_with_aes_256_gcm_sha384)
- [var TLS_DH_anon_WITH_RC4_128_MD5: SSLCipherSuite](/documentation/security/tls_dh_anon_with_rc4_128_md5)
- [var TLS_ECDHE_ECDSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_3des_ede_cbc_sha)
- [var TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_128_cbc_sha)
- [var TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_128_cbc_sha256)
- [var TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_128_gcm_sha256)
- [var TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_256_cbc_sha)
- [var TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_256_cbc_sha384)
- [var TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_aes_256_gcm_sha384)
- [var TLS_ECDHE_ECDSA_WITH_CHACHA20_POLY1305_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_chacha20_poly1305_sha256)
- [var TLS_ECDHE_ECDSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_null_sha)
- [var TLS_ECDHE_ECDSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_ecdsa_with_rc4_128_sha)
- [var TLS_ECDHE_PSK_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_psk_with_aes_128_cbc_sha)
- [var TLS_ECDHE_PSK_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_psk_with_aes_256_cbc_sha)
- [var TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_3des_ede_cbc_sha)
- [var TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_128_cbc_sha)
- [var TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_128_cbc_sha256)
- [var TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_128_gcm_sha256)
- [var TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_256_cbc_sha)
- [var TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_256_cbc_sha384)
- [var TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_aes_256_gcm_sha384)
- [var TLS_ECDHE_RSA_WITH_CHACHA20_POLY1305_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_chacha20_poly1305_sha256)
- [var TLS_ECDHE_RSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_null_sha)
- [var TLS_ECDHE_RSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_ecdhe_rsa_with_rc4_128_sha)
- [var TLS_ECDH_ECDSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_3des_ede_cbc_sha)
- [var TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_128_cbc_sha)
- [var TLS_ECDH_ECDSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_128_cbc_sha256)
- [var TLS_ECDH_ECDSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_128_gcm_sha256)
- [var TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_256_cbc_sha)
- [var TLS_ECDH_ECDSA_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_256_cbc_sha384)
- [var TLS_ECDH_ECDSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_aes_256_gcm_sha384)
- [var TLS_ECDH_ECDSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_null_sha)
- [var TLS_ECDH_ECDSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_ecdsa_with_rc4_128_sha)
- [var TLS_ECDH_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_3des_ede_cbc_sha)
- [var TLS_ECDH_RSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_128_cbc_sha)
- [var TLS_ECDH_RSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_128_cbc_sha256)
- [var TLS_ECDH_RSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_128_gcm_sha256)
- [var TLS_ECDH_RSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_256_cbc_sha)
- [var TLS_ECDH_RSA_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_256_cbc_sha384)
- [var TLS_ECDH_RSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_aes_256_gcm_sha384)
- [var TLS_ECDH_RSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_null_sha)
- [var TLS_ECDH_RSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_rsa_with_rc4_128_sha)
- [var TLS_ECDH_anon_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_anon_with_3des_ede_cbc_sha)
- [var TLS_ECDH_anon_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_anon_with_aes_128_cbc_sha)
- [var TLS_ECDH_anon_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_anon_with_aes_256_cbc_sha)
- [var TLS_ECDH_anon_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_anon_with_null_sha)
- [var TLS_ECDH_anon_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_ecdh_anon_with_rc4_128_sha)
- [var TLS_EMPTY_RENEGOTIATION_INFO_SCSV: SSLCipherSuite](/documentation/security/tls_empty_renegotiation_info_scsv)
- [var TLS_NULL_WITH_NULL_NULL: SSLCipherSuite](/documentation/security/tls_null_with_null_null)
- [var TLS_PSK_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_psk_with_3des_ede_cbc_sha)
- [var TLS_PSK_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_psk_with_aes_128_cbc_sha)
- [var TLS_PSK_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_psk_with_aes_128_cbc_sha256)
- [var TLS_PSK_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_psk_with_aes_128_gcm_sha256)
- [var TLS_PSK_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_psk_with_aes_256_cbc_sha)
- [var TLS_PSK_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_psk_with_aes_256_cbc_sha384)
- [var TLS_PSK_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_psk_with_aes_256_gcm_sha384)
- [var TLS_PSK_WITH_CHACHA20_POLY1305_SHA256: SSLCipherSuite](/documentation/security/tls_psk_with_chacha20_poly1305_sha256)
- [var TLS_PSK_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_psk_with_null_sha)
- [var TLS_PSK_WITH_NULL_SHA256: SSLCipherSuite](/documentation/security/tls_psk_with_null_sha256)
- [var TLS_PSK_WITH_NULL_SHA384: SSLCipherSuite](/documentation/security/tls_psk_with_null_sha384)
- [var TLS_PSK_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_psk_with_rc4_128_sha)
- [var TLS_RSA_PSK_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_3des_ede_cbc_sha)
- [var TLS_RSA_PSK_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_128_cbc_sha)
- [var TLS_RSA_PSK_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_128_cbc_sha256)
- [var TLS_RSA_PSK_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_128_gcm_sha256)
- [var TLS_RSA_PSK_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_256_cbc_sha)
- [var TLS_RSA_PSK_WITH_AES_256_CBC_SHA384: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_256_cbc_sha384)
- [var TLS_RSA_PSK_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_aes_256_gcm_sha384)
- [var TLS_RSA_PSK_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_null_sha)
- [var TLS_RSA_PSK_WITH_NULL_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_null_sha256)
- [var TLS_RSA_PSK_WITH_NULL_SHA384: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_null_sha384)
- [var TLS_RSA_PSK_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_rsa_psk_with_rc4_128_sha)
- [var TLS_RSA_WITH_3DES_EDE_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_with_3des_ede_cbc_sha)
- [var TLS_RSA_WITH_AES_128_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_128_cbc_sha)
- [var TLS_RSA_WITH_AES_128_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_128_cbc_sha256)
- [var TLS_RSA_WITH_AES_128_GCM_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_128_gcm_sha256)
- [var TLS_RSA_WITH_AES_256_CBC_SHA: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_256_cbc_sha)
- [var TLS_RSA_WITH_AES_256_CBC_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_256_cbc_sha256)
- [var TLS_RSA_WITH_AES_256_GCM_SHA384: SSLCipherSuite](/documentation/security/tls_rsa_with_aes_256_gcm_sha384)
- [var TLS_RSA_WITH_NULL_MD5: SSLCipherSuite](/documentation/security/tls_rsa_with_null_md5)
- [var TLS_RSA_WITH_NULL_SHA: SSLCipherSuite](/documentation/security/tls_rsa_with_null_sha)
- [var TLS_RSA_WITH_NULL_SHA256: SSLCipherSuite](/documentation/security/tls_rsa_with_null_sha256)
- [var TLS_RSA_WITH_RC4_128_MD5: SSLCipherSuite](/documentation/security/tls_rsa_with_rc4_128_md5)
- [var TLS_RSA_WITH_RC4_128_SHA: SSLCipherSuite](/documentation/security/tls_rsa_with_rc4_128_sha)

### Root Certificates

- [func SSLSetCertificateAuthorities(SSLContext, CFTypeRef, Bool) -> OSStatus](/documentation/security/sslsetcertificateauthorities(_:_:_:))
- [func SSLCopyCertificateAuthorities(SSLContext, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sslcopycertificateauthorities(_:_:))

### Authentication

- [func SSLAddDistinguishedName(SSLContext, UnsafeRawPointer?, Int) -> OSStatus](/documentation/security/ssladddistinguishedname(_:_:_:))
- [func SSLCopyDistinguishedNames(SSLContext, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/security/sslcopydistinguishednames(_:_:))
- [func SSLSetCertificate(SSLContext, CFArray?) -> OSStatus](/documentation/security/sslsetcertificate(_:_:))
- [func SSLGetClientCertificateState(SSLContext, UnsafeMutablePointer<SSLClientCertificateState>) -> OSStatus](/documentation/security/sslgetclientcertificatestate(_:_:))
- [func SSLCopyPeerTrust(SSLContext, UnsafeMutablePointer<SecTrust?>) -> OSStatus](/documentation/security/sslcopypeertrust(_:_:))
- [SSLClientCertificateState](/documentation/security/sslclientcertificatestate)

#### Constants

- [case certNone](/documentation/security/sslclientcertificatestate/certnone)
- [case certRequested](/documentation/security/sslclientcertificatestate/certrequested)
- [case certSent](/documentation/security/sslclientcertificatestate/certsent)
- [case certRejected](/documentation/security/sslclientcertificatestate/certrejected)

#### Initializers

- [init?(rawValue: Int32)](/documentation/security/sslclientcertificatestate/init(rawvalue:))
- [func SSLSetOCSPResponse(SSLContext, CFData) -> OSStatus](/documentation/security/sslsetocspresponse(_:_:))
- [func SSLSetSessionTicketsEnabled(SSLContext, Bool) -> OSStatus](/documentation/security/sslsetsessionticketsenabled(_:_:))

### Result Codes

- [Secure Transport Result Codes](/documentation/security/secure-transport-result-codes)

#### App Transport Security result codes

- [var errSSLATSViolation: OSStatus](/documentation/security/errsslatsviolation)
- [var errSSLATSMinimumVersionViolation: OSStatus](/documentation/security/errsslatsminimumversionviolation)
- [var errSSLATSCiphersuiteViolation: OSStatus](/documentation/security/errsslatsciphersuiteviolation)
- [var errSSLATSMinimumKeySizeViolation: OSStatus](/documentation/security/errsslatsminimumkeysizeviolation)
- [var errSSLATSLeafCertificateHashAlgorithmViolation: OSStatus](/documentation/security/errsslatsleafcertificatehashalgorithmviolation)
- [var errSSLATSCertificateHashAlgorithmViolation: OSStatus](/documentation/security/errsslatscertificatehashalgorithmviolation)
- [var errSSLATSCertificateTrustViolation: OSStatus](/documentation/security/errsslatscertificatetrustviolation)

#### Certificate issue result codes

- [var errSSLBadCert: OSStatus](/documentation/security/errsslbadcert)
- [var errSSLBadCertificateStatusResponse: OSStatus](/documentation/security/errsslbadcertificatestatusresponse)
- [var errSSLCertExpired: OSStatus](/documentation/security/errsslcertexpired)
- [var errSSLCertNotYetValid: OSStatus](/documentation/security/errsslcertnotyetvalid)
- [var errSSLCertificateRequired: OSStatus](/documentation/security/errsslcertificaterequired)
- [var errSSLClientCertRequested: OSStatus](/documentation/security/errsslclientcertrequested)
- [var errSSLHostNameMismatch: OSStatus](/documentation/security/errsslhostnamemismatch)
- [var errSSLNoRootCert: OSStatus](/documentation/security/errsslnorootcert)
- [var errSSLPeerBadCert: OSStatus](/documentation/security/errsslpeerbadcert)
- [var errSSLPeerCertExpired: OSStatus](/documentation/security/errsslpeercertexpired)
- [var errSSLPeerCertRevoked: OSStatus](/documentation/security/errsslpeercertrevoked)
- [var errSSLPeerCertUnknown: OSStatus](/documentation/security/errsslpeercertunknown)
- [var errSSLPeerUnsupportedCert: OSStatus](/documentation/security/errsslpeerunsupportedcert)
- [var errSSLUnknownRootCert: OSStatus](/documentation/security/errsslunknownrootcert)
- [var errSSLXCertChainInvalid: OSStatus](/documentation/security/errsslxcertchaininvalid)
- [var errSSLPeerUnknownCA: OSStatus](/documentation/security/errsslpeerunknownca)

#### Connection status result codes

- [var errSSLClientHelloReceived: OSStatus](/documentation/security/errsslclienthelloreceived)
- [var errSSLClosedAbort: OSStatus](/documentation/security/errsslclosedabort)
- [var errSSLClosedGraceful: OSStatus](/documentation/security/errsslclosedgraceful)
- [var errSSLClosedNoNotify: OSStatus](/documentation/security/errsslclosednonotify)
- [var errSSLConnectionRefused: OSStatus](/documentation/security/errsslconnectionrefused)
- [var errSSLPeerAuthCompleted: OSStatus](/documentation/security/errsslpeerauthcompleted)
- [var errSSLWouldBlock: OSStatus](/documentation/security/errsslwouldblock)

#### Cryptography result codes

- [var errSSLCrypto: OSStatus](/documentation/security/errsslcrypto)
- [var errSSLDecryptionFail: OSStatus](/documentation/security/errssldecryptionfail)
- [var errSSLPeerDecryptError: OSStatus](/documentation/security/errsslpeerdecrypterror)
- [var errSSLPeerDecryptionFail: OSStatus](/documentation/security/errsslpeerdecryptionfail)
- [var errSSLWeakPeerEphemeralDHKey: OSStatus](/documentation/security/errsslweakpeerephemeraldhkey)

#### Other result codes

- [var errSSLBadCipherSuite: OSStatus](/documentation/security/errsslbadciphersuite)
- [var errSSLBadConfiguration: OSStatus](/documentation/security/errsslbadconfiguration)
- [var errSSLBadRecordMac: OSStatus](/documentation/security/errsslbadrecordmac)
- [var errSSLBufferOverflow: OSStatus](/documentation/security/errsslbufferoverflow)
- [var errSSLConfigurationFailed: OSStatus](/documentation/security/errsslconfigurationfailed)
- [var errSSLDecodeError: OSStatus](/documentation/security/errssldecodeerror)
- [var errSSLDecompressFail: OSStatus](/documentation/security/errssldecompressfail)
- [var errSSLFatalAlert: OSStatus](/documentation/security/errsslfatalalert)
- [var errSSLHandshakeFail: OSStatus](/documentation/security/errsslhandshakefail)
- [var errSSLIllegalParam: OSStatus](/documentation/security/errsslillegalparam)
- [var errSSLInappropriateFallback: OSStatus](/documentation/security/errsslinappropriatefallback)
- [var errSSLInternal: OSStatus](/documentation/security/errsslinternal)
- [var errSSLMissingExtension: OSStatus](/documentation/security/errsslmissingextension)
- [var errSSLModuleAttach: OSStatus](/documentation/security/errsslmoduleattach)
- [var errSSLNegotiation: OSStatus](/documentation/security/errsslnegotiation)
- [var errSSLNetworkTimeout: OSStatus](/documentation/security/errsslnetworktimeout)
- [var errSSLPeerAccessDenied: OSStatus](/documentation/security/errsslpeeraccessdenied)
- [var errSSLPeerBadRecordMac: OSStatus](/documentation/security/errsslpeerbadrecordmac)
- [var errSSLPeerDecodeError: OSStatus](/documentation/security/errsslpeerdecodeerror)
- [var errSSLPeerDecompressFail: OSStatus](/documentation/security/errsslpeerdecompressfail)
- [var errSSLPeerExportRestriction: OSStatus](/documentation/security/errsslpeerexportrestriction)
- [var errSSLPeerHandshakeFail: OSStatus](/documentation/security/errsslpeerhandshakefail)
- [var errSSLPeerInsufficientSecurity: OSStatus](/documentation/security/errsslpeerinsufficientsecurity)
- [var errSSLPeerInternalError: OSStatus](/documentation/security/errsslpeerinternalerror)
- [var errSSLPeerNoRenegotiation: OSStatus](/documentation/security/errsslpeernorenegotiation)
- [var errSSLPeerProtocolVersion: OSStatus](/documentation/security/errsslpeerprotocolversion)
- [var errSSLPeerRecordOverflow: OSStatus](/documentation/security/errsslpeerrecordoverflow)
- [var errSSLPeerUnexpectedMsg: OSStatus](/documentation/security/errsslpeerunexpectedmsg)
- [var errSSLPeerUserCancelled: OSStatus](/documentation/security/errsslpeerusercancelled)
- [var errSSLProtocol: OSStatus](/documentation/security/errsslprotocol)
- [var errSSLRecordOverflow: OSStatus](/documentation/security/errsslrecordoverflow)
- [var errSSLSessionNotFound: OSStatus](/documentation/security/errsslsessionnotfound)
- [var errSSLTransportReset: OSStatus](/documentation/security/errssltransportreset)
- [var errSSLUnexpectedMessage: OSStatus](/documentation/security/errsslunexpectedmessage)
- [var errSSLUnexpectedRecord: OSStatus](/documentation/security/errsslunexpectedrecord)
- [var errSSLUnknownPSKIdentity: OSStatus](/documentation/security/errsslunknownpskidentity)
- [var errSSLUnrecognizedName: OSStatus](/documentation/security/errsslunrecognizedname)
- [var errSSLUnsupportedExtension: OSStatus](/documentation/security/errsslunsupportedextension)

### Legacy Operations

- [func SSLSetEncryptionCertificate(SSLContext, CFArray) -> OSStatus](/documentation/security/sslsetencryptioncertificate(_:_:))
- [Secure Download](/documentation/security/secure-download)

### Result Codes

- [Secure Download Result Codes](/documentation/security/secure-download-result-codes)
- [Security legacy reference](/documentation/security/security-legacy-reference)

### Module directory service

- [var MDS_CDSAATTR_ACLSUBJECTTYPES: Int32](/documentation/security/mds_cdsaattr_aclsubjecttypes)
- [var MDS_CDSAATTR_ALG_TYPE: Int32](/documentation/security/mds_cdsaattr_alg_type)
- [var MDS_CDSAATTR_ATTRIBUTE_TYPE: Int32](/documentation/security/mds_cdsaattr_attribute_type)
- [var MDS_CDSAATTR_ATTRIBUTE_VALUE: Int32](/documentation/security/mds_cdsaattr_attribute_value)
- [var MDS_CDSAATTR_AUTHORITY_REQUEST_TYPE: Int32](/documentation/security/mds_cdsaattr_authority_request_type)
- [var MDS_CDSAATTR_AUTHTAGS: Int32](/documentation/security/mds_cdsaattr_authtags)
- [var MDS_CDSAATTR_BUNDLE_TYPEFORMAT: Int32](/documentation/security/mds_cdsaattr_bundle_typeformat)
- [var MDS_CDSAATTR_CDSAVERSION: Int32](/documentation/security/mds_cdsaattr_cdsaversion)
- [var MDS_CDSAATTR_CERT_CLASSNAME: Int32](/documentation/security/mds_cdsaattr_cert_classname)
- [var MDS_CDSAATTR_CERT_FIELDNAMES: Int32](/documentation/security/mds_cdsaattr_cert_fieldnames)
- [var MDS_CDSAATTR_CERT_TYPEFORMAT: Int32](/documentation/security/mds_cdsaattr_cert_typeformat)
- [var MDS_CDSAATTR_CONJUNCTIVE_OPS: Int32](/documentation/security/mds_cdsaattr_conjunctive_ops)
- [var MDS_CDSAATTR_CONTEXT_TYPE: Int32](/documentation/security/mds_cdsaattr_context_type)
- [var MDS_CDSAATTR_CRL_TYPEFORMAT: Int32](/documentation/security/mds_cdsaattr_crl_typeformat)
- [var MDS_CDSAATTR_CSP_CUSTOMFLAGS: Int32](/documentation/security/mds_cdsaattr_csp_customflags)
- [var MDS_CDSAATTR_CSP_FLAGS: Int32](/documentation/security/mds_cdsaattr_csp_flags)
- [var MDS_CDSAATTR_CSP_TYPE: Int32](/documentation/security/mds_cdsaattr_csp_type)
- [var MDS_CDSAATTR_DEFAULT_TEMPLATE_TYPE: Int32](/documentation/security/mds_cdsaattr_default_template_type)
- [var MDS_CDSAATTR_DESC: Int32](/documentation/security/mds_cdsaattr_desc)
- [var MDS_CDSAATTR_DL_TYPE: Int32](/documentation/security/mds_cdsaattr_dl_type)
- [var MDS_CDSAATTR_DYNAMIC_FLAG: Int32](/documentation/security/mds_cdsaattr_dynamic_flag)
- [var MDS_CDSAATTR_EMMSPECVERSION: Int32](/documentation/security/mds_cdsaattr_emmspecversion)
- [var MDS_CDSAATTR_EMM_TYPE: Int32](/documentation/security/mds_cdsaattr_emm_type)
- [var MDS_CDSAATTR_EMM_VENDOR: Int32](/documentation/security/mds_cdsaattr_emm_vendor)
- [var MDS_CDSAATTR_EMM_VERSION: Int32](/documentation/security/mds_cdsaattr_emm_version)
- [var MDS_CDSAATTR_GROUP_ID: Int32](/documentation/security/mds_cdsaattr_group_id)
- [var MDS_CDSAATTR_INTERFACE_GUID: Int32](/documentation/security/mds_cdsaattr_interface_guid)
- [var MDS_CDSAATTR_MANIFEST: Int32](/documentation/security/mds_cdsaattr_manifest)
- [var MDS_CDSAATTR_MODULE_ID: Int32](/documentation/security/mds_cdsaattr_module_id)
- [var MDS_CDSAATTR_MODULE_NAME: Int32](/documentation/security/mds_cdsaattr_module_name)
- [var MDS_CDSAATTR_MULTITHREAD_FLAG: Int32](/documentation/security/mds_cdsaattr_multithread_flag)
- [var MDS_CDSAATTR_NATIVE_SERVICES: Int32](/documentation/security/mds_cdsaattr_native_services)
- [var MDS_CDSAATTR_OID: Int32](/documentation/security/mds_cdsaattr_oid)
- [var MDS_CDSAATTR_PATH: Int32](/documentation/security/mds_cdsaattr_path)
- [var MDS_CDSAATTR_POLICY_STMT: Int32](/documentation/security/mds_cdsaattr_policy_stmt)
- [var MDS_CDSAATTR_PRODUCT_CUSTOMFLAGS: Int32](/documentation/security/mds_cdsaattr_product_customflags)
- [var MDS_CDSAATTR_PRODUCT_DESC: Int32](/documentation/security/mds_cdsaattr_product_desc)
- [var MDS_CDSAATTR_PRODUCT_FLAGS: Int32](/documentation/security/mds_cdsaattr_product_flags)
- [var MDS_CDSAATTR_PRODUCT_VENDOR: Int32](/documentation/security/mds_cdsaattr_product_vendor)
- [var MDS_CDSAATTR_PRODUCT_VERSION: Int32](/documentation/security/mds_cdsaattr_product_version)
- [var MDS_CDSAATTR_PROTOCOL: Int32](/documentation/security/mds_cdsaattr_protocol)
- [var MDS_CDSAATTR_QUERY_LIMITS: Int32](/documentation/security/mds_cdsaattr_query_limits)
- [var MDS_CDSAATTR_READER_CUSTOMFLAGS: Int32](/documentation/security/mds_cdsaattr_reader_customflags)
- [var MDS_CDSAATTR_READER_DESC: Int32](/documentation/security/mds_cdsaattr_reader_desc)
- [var MDS_CDSAATTR_READER_FLAGS: Int32](/documentation/security/mds_cdsaattr_reader_flags)
- [var MDS_CDSAATTR_READER_FWVERSION: Int32](/documentation/security/mds_cdsaattr_reader_fwversion)
- [var MDS_CDSAATTR_READER_SERIALNUMBER: Int32](/documentation/security/mds_cdsaattr_reader_serialnumber)
- [var MDS_CDSAATTR_READER_VENDOR: Int32](/documentation/security/mds_cdsaattr_reader_vendor)
- [var MDS_CDSAATTR_READER_VERSION: Int32](/documentation/security/mds_cdsaattr_reader_version)
- [var MDS_CDSAATTR_RELATIONAL_OPS: Int32](/documentation/security/mds_cdsaattr_relational_ops)
- [var MDS_CDSAATTR_REQCREDENTIALS: Int32](/documentation/security/mds_cdsaattr_reqcredentials)
- [var MDS_CDSAATTR_RETRIEVALMODE: Int32](/documentation/security/mds_cdsaattr_retrievalmode)
- [var MDS_CDSAATTR_ROOTCERT: Int32](/documentation/security/mds_cdsaattr_rootcert)
- [var MDS_CDSAATTR_ROOTCERT_TYPEFORMAT: Int32](/documentation/security/mds_cdsaattr_rootcert_typeformat)
- [var MDS_CDSAATTR_SAMPLETYPES: Int32](/documentation/security/mds_cdsaattr_sampletypes)
- [var MDS_CDSAATTR_SC_CUSTOMFLAGS: Int32](/documentation/security/mds_cdsaattr_sc_customflags)
- [var MDS_CDSAATTR_SC_DESC: Int32](/documentation/security/mds_cdsaattr_sc_desc)
- [var MDS_CDSAATTR_SC_FLAGS: Int32](/documentation/security/mds_cdsaattr_sc_flags)
- [var MDS_CDSAATTR_SC_FWVERSION: Int32](/documentation/security/mds_cdsaattr_sc_fwversion)
- [var MDS_CDSAATTR_SC_SERIALNUMBER: Int32](/documentation/security/mds_cdsaattr_sc_serialnumber)
- [var MDS_CDSAATTR_SC_VENDOR: Int32](/documentation/security/mds_cdsaattr_sc_vendor)
- [var MDS_CDSAATTR_SC_VERSION: Int32](/documentation/security/mds_cdsaattr_sc_version)
- [var MDS_CDSAATTR_SERVICE_MASK: Int32](/documentation/security/mds_cdsaattr_service_mask)
- [var MDS_CDSAATTR_SERVICE_TYPE: Int32](/documentation/security/mds_cdsaattr_service_type)
- [var MDS_CDSAATTR_SSID: Int32](/documentation/security/mds_cdsaattr_ssid)
- [var MDS_CDSAATTR_STANDARD_DESC: Int32](/documentation/security/mds_cdsaattr_standard_desc)
- [var MDS_CDSAATTR_STANDARD_VERSION: Int32](/documentation/security/mds_cdsaattr_standard_version)
- [var MDS_CDSAATTR_TEMPLATE_FIELD_NAMES: Int32](/documentation/security/mds_cdsaattr_template_field_names)
- [var MDS_CDSAATTR_USEETAG: Int32](/documentation/security/mds_cdsaattr_useetag)
- [var MDS_CDSAATTR_USEE_TAGS: Int32](/documentation/security/mds_cdsaattr_usee_tags)
- [var MDS_CDSAATTR_VALUE: Int32](/documentation/security/mds_cdsaattr_value)
- [var MDS_CDSAATTR_VENDOR: Int32](/documentation/security/mds_cdsaattr_vendor)
- [var MDS_CDSAATTR_XLATIONTYPEFORMAT: Int32](/documentation/security/mds_cdsaattr_xlationtypeformat)
- [var MDS_CDSADIR_AC_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_ac_primary_num_attributes)
- [var MDS_CDSADIR_CL_ENCAPSULATED_PRODUCT_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_cl_encapsulated_product_num_attributes)
- [var MDS_CDSADIR_CL_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_cl_primary_num_attributes)
- [var MDS_CDSADIR_COMMON_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_common_num_attributes)
- [var MDS_CDSADIR_CSP_CAPABILITY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_csp_capability_num_attributes)
- [var MDS_CDSADIR_CSP_ENCAPSULATED_PRODUCT_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_csp_encapsulated_product_num_attributes)
- [var MDS_CDSADIR_CSP_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_csp_primary_num_attributes)
- [var MDS_CDSADIR_CSP_SC_INFO_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_csp_sc_info_num_attributes)
- [var MDS_CDSADIR_CSSM_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_cssm_num_attributes)
- [var MDS_CDSADIR_DL_ENCAPSULATED_PRODUCT_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_dl_encapsulated_product_num_attributes)
- [var MDS_CDSADIR_DL_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_dl_primary_num_attributes)
- [var MDS_CDSADIR_EMM_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_emm_num_attributes)
- [var MDS_CDSADIR_EMM_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_emm_primary_num_attributes)
- [var MDS_CDSADIR_NUM_RELATIONS: Int32](/documentation/security/mds_cdsadir_num_relations)
- [var MDS_CDSADIR_SCHEMA_ATTRIBUTES_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_schema_attributes_num_attributes)
- [var MDS_CDSADIR_SCHEMA_INDEXES_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_schema_indexes_num_attributes)
- [var MDS_CDSADIR_SCHEMA_RELATONS_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_schema_relatons_num_attributes)
- [var MDS_CDSADIR_TP_ENCAPSULATED_PRODUCT_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_tp_encapsulated_product_num_attributes)
- [var MDS_CDSADIR_TP_OIDS_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_tp_oids_num_attributes)
- [var MDS_CDSADIR_TP_PRIMARY_NUM_ATTRIBUTES: Int32](/documentation/security/mds_cdsadir_tp_primary_num_attributes)
- [var MDS_CDSA_DIRECTORY_NAME: String](/documentation/security/mds_cdsa_directory_name)
- [var MDS_CDSA_SCHEMA_START: Int32](/documentation/security/mds_cdsa_schema_start)
- [var MDS_OBJECT_DIRECTORY_NAME: String](/documentation/security/mds_object_directory_name)
- [var MDS_OBJECT_NUM_ATTRIBUTES: Int32](/documentation/security/mds_object_num_attributes)
- [var MDS_OBJECT_NUM_RELATIONS: Int32](/documentation/security/mds_object_num_relations)
- [var MDS_OBJECT_RECORDTYPE: Int32](/documentation/security/mds_object_recordtype)
- [MDS_HANDLE](/documentation/security/mds_handle)

### Protocols

- [OS_sec_certificate](/documentation/security/os_sec_certificate)
- [OS_sec_identity](/documentation/security/os_sec_identity)
- [OS_sec_object](/documentation/security/os_sec_object)
- [OS_sec_protocol_metadata](/documentation/security/os_sec_protocol_metadata)
- [OS_sec_protocol_options](/documentation/security/os_sec_protocol_options)
- [OS_sec_trust](/documentation/security/os_sec_trust)

### Variables

- [let gGuidAppleCSP: cssm_guid](/documentation/security/gguidapplecsp)
- [let gGuidAppleCSPDL: cssm_guid](/documentation/security/gguidapplecspdl)
- [let gGuidAppleDotMacDL: cssm_guid](/documentation/security/gguidappledotmacdl)
- [let gGuidAppleDotMacTP: cssm_guid](/documentation/security/gguidappledotmactp)
- [let gGuidAppleFileDL: cssm_guid](/documentation/security/gguidapplefiledl)
- [let gGuidAppleLDAPDL: cssm_guid](/documentation/security/gguidappleldapdl)
- [let gGuidAppleSdCSPDL: cssm_guid](/documentation/security/gguidapplesdcspdl)
- [let gGuidAppleX509CL: cssm_guid](/documentation/security/gguidapplex509cl)
- [let gGuidAppleX509TP: cssm_guid](/documentation/security/gguidapplex509tp)
- [let gGuidCssm: cssm_guid](/documentation/security/gguidcssm)

### Functions

- [func sec_certificate_copy_ref(sec_certificate_t) -> Unmanaged<SecCertificate>](/documentation/security/sec_certificate_copy_ref(_:))
- [func sec_certificate_create(SecCertificate) -> sec_certificate_t?](/documentation/security/sec_certificate_create(_:))
- [func sec_identity_access_certificates(sec_identity_t, (sec_certificate_t) -> Void) -> Bool](/documentation/security/sec_identity_access_certificates(_:_:))
- [func sec_identity_copy_certificates_ref(sec_identity_t) -> Unmanaged<CFArray>?](/documentation/security/sec_identity_copy_certificates_ref(_:))
- [func sec_identity_copy_ref(sec_identity_t) -> Unmanaged<SecIdentity>?](/documentation/security/sec_identity_copy_ref(_:))
- [func sec_identity_create(SecIdentity) -> sec_identity_t?](/documentation/security/sec_identity_create(_:))
- [func sec_identity_create_with_certificates(SecIdentity, CFArray) -> sec_identity_t?](/documentation/security/sec_identity_create_with_certificates(_:_:))
- [func sec_protocol_metadata_access_distinguished_names(sec_protocol_metadata_t, (dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_distinguished_names(_:_:))
- [func sec_protocol_metadata_access_ocsp_response(sec_protocol_metadata_t, (dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_ocsp_response(_:_:))
- [func sec_protocol_metadata_access_peer_certificate_chain(sec_protocol_metadata_t, (sec_certificate_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_peer_certificate_chain(_:_:))
- [func sec_protocol_metadata_access_pre_shared_keys(sec_protocol_metadata_t, (dispatch_data_t, dispatch_data_t) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_pre_shared_keys(_:_:))
- [func sec_protocol_metadata_access_supported_signature_algorithms(sec_protocol_metadata_t, (UInt16) -> Void) -> Bool](/documentation/security/sec_protocol_metadata_access_supported_signature_algorithms(_:_:))
- [func sec_protocol_metadata_challenge_parameters_are_equal(sec_protocol_metadata_t, sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_challenge_parameters_are_equal(_:_:))
- [func sec_protocol_metadata_copy_peer_public_key(sec_protocol_metadata_t) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_copy_peer_public_key(_:))
- [func sec_protocol_metadata_create_secret(sec_protocol_metadata_t, Int, UnsafePointer<CChar>, Int) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_create_secret(_:_:_:_:))
- [func sec_protocol_metadata_create_secret_with_context(sec_protocol_metadata_t, Int, UnsafePointer<CChar>, Int, UnsafePointer<UInt8>, Int) -> dispatch_data_t?](/documentation/security/sec_protocol_metadata_create_secret_with_context(_:_:_:_:_:_:))
- [func sec_protocol_metadata_get_early_data_accepted(sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_get_early_data_accepted(_:))
- [func sec_protocol_metadata_get_negotiated_ciphersuite(sec_protocol_metadata_t) -> SSLCipherSuite](/documentation/security/sec_protocol_metadata_get_negotiated_ciphersuite(_:))
- [func sec_protocol_metadata_get_negotiated_protocol(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_get_negotiated_protocol(_:))
- [func sec_protocol_metadata_get_negotiated_protocol_version(sec_protocol_metadata_t) -> SSLProtocol](/documentation/security/sec_protocol_metadata_get_negotiated_protocol_version(_:))
- [func sec_protocol_metadata_get_negotiated_tls_ciphersuite(sec_protocol_metadata_t) -> tls_ciphersuite_t](/documentation/security/sec_protocol_metadata_get_negotiated_tls_ciphersuite(_:))
- [func sec_protocol_metadata_get_negotiated_tls_protocol_version(sec_protocol_metadata_t) -> tls_protocol_version_t](/documentation/security/sec_protocol_metadata_get_negotiated_tls_protocol_version(_:))
- [func sec_protocol_metadata_get_server_name(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_get_server_name(_:))
- [func sec_protocol_metadata_peers_are_equal(sec_protocol_metadata_t, sec_protocol_metadata_t) -> Bool](/documentation/security/sec_protocol_metadata_peers_are_equal(_:_:))
- [func sec_protocol_options_add_pre_shared_key(sec_protocol_options_t, dispatch_data_t, dispatch_data_t)](/documentation/security/sec_protocol_options_add_pre_shared_key(_:_:_:))
- [func sec_protocol_options_add_tls_application_protocol(sec_protocol_options_t, UnsafePointer<CChar>)](/documentation/security/sec_protocol_options_add_tls_application_protocol(_:_:))
- [func sec_protocol_options_add_tls_ciphersuite(sec_protocol_options_t, SSLCipherSuite)](/documentation/security/sec_protocol_options_add_tls_ciphersuite(_:_:))
- [func sec_protocol_options_add_tls_ciphersuite_group(sec_protocol_options_t, SSLCiphersuiteGroup)](/documentation/security/sec_protocol_options_add_tls_ciphersuite_group(_:_:))
- [func sec_protocol_options_append_tls_ciphersuite(sec_protocol_options_t, tls_ciphersuite_t)](/documentation/security/sec_protocol_options_append_tls_ciphersuite(_:_:))
- [func sec_protocol_options_append_tls_ciphersuite_group(sec_protocol_options_t, tls_ciphersuite_group_t)](/documentation/security/sec_protocol_options_append_tls_ciphersuite_group(_:_:))
- [func sec_protocol_options_are_equal(sec_protocol_options_t, sec_protocol_options_t) -> Bool](/documentation/security/sec_protocol_options_are_equal(_:_:))
- [func sec_protocol_options_get_default_max_dtls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_max_dtls_protocol_version())
- [func sec_protocol_options_get_default_max_tls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_max_tls_protocol_version())
- [func sec_protocol_options_get_default_min_dtls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_min_dtls_protocol_version())
- [func sec_protocol_options_get_default_min_tls_protocol_version() -> tls_protocol_version_t](/documentation/security/sec_protocol_options_get_default_min_tls_protocol_version())
- [func sec_protocol_options_set_challenge_block(sec_protocol_options_t, sec_protocol_challenge_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_challenge_block(_:_:_:))
- [func sec_protocol_options_set_key_update_block(sec_protocol_options_t, sec_protocol_key_update_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_key_update_block(_:_:_:))
- [func sec_protocol_options_set_local_identity(sec_protocol_options_t, sec_identity_t)](/documentation/security/sec_protocol_options_set_local_identity(_:_:))
- [func sec_protocol_options_set_max_tls_protocol_version(sec_protocol_options_t, tls_protocol_version_t)](/documentation/security/sec_protocol_options_set_max_tls_protocol_version(_:_:))
- [func sec_protocol_options_set_min_tls_protocol_version(sec_protocol_options_t, tls_protocol_version_t)](/documentation/security/sec_protocol_options_set_min_tls_protocol_version(_:_:))
- [func sec_protocol_options_set_peer_authentication_required(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_peer_authentication_required(_:_:))
- [func sec_protocol_options_set_pre_shared_key_selection_block(sec_protocol_options_t, sec_protocol_pre_shared_key_selection_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_pre_shared_key_selection_block(_:_:_:))
- [func sec_protocol_options_set_tls_diffie_hellman_parameters(sec_protocol_options_t, dispatch_data_t)](/documentation/security/sec_protocol_options_set_tls_diffie_hellman_parameters(_:_:))
- [func sec_protocol_options_set_tls_false_start_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_false_start_enabled(_:_:))
- [func sec_protocol_options_set_tls_is_fallback_attempt(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_is_fallback_attempt(_:_:))
- [func sec_protocol_options_set_tls_max_version(sec_protocol_options_t, SSLProtocol)](/documentation/security/sec_protocol_options_set_tls_max_version(_:_:))
- [func sec_protocol_options_set_tls_min_version(sec_protocol_options_t, SSLProtocol)](/documentation/security/sec_protocol_options_set_tls_min_version(_:_:))
- [func sec_protocol_options_set_tls_ocsp_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_ocsp_enabled(_:_:))
- [func sec_protocol_options_set_tls_pre_shared_key_identity_hint(sec_protocol_options_t, dispatch_data_t)](/documentation/security/sec_protocol_options_set_tls_pre_shared_key_identity_hint(_:_:))
- [func sec_protocol_options_set_tls_renegotiation_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_renegotiation_enabled(_:_:))
- [func sec_protocol_options_set_tls_resumption_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_resumption_enabled(_:_:))
- [func sec_protocol_options_set_tls_sct_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_sct_enabled(_:_:))
- [func sec_protocol_options_set_tls_server_name(sec_protocol_options_t, UnsafePointer<CChar>)](/documentation/security/sec_protocol_options_set_tls_server_name(_:_:))
- [func sec_protocol_options_set_tls_tickets_enabled(sec_protocol_options_t, Bool)](/documentation/security/sec_protocol_options_set_tls_tickets_enabled(_:_:))
- [func sec_protocol_options_set_verify_block(sec_protocol_options_t, sec_protocol_verify_t, dispatch_queue_t)](/documentation/security/sec_protocol_options_set_verify_block(_:_:_:))
- [func sec_release(UnsafeMutableRawPointer!)](/documentation/security/sec_release(_:))
- [func sec_retain(UnsafeMutableRawPointer!) -> UnsafeMutableRawPointer!](/documentation/security/sec_retain(_:))
- [func sec_trust_copy_ref(sec_trust_t) -> Unmanaged<SecTrust>](/documentation/security/sec_trust_copy_ref(_:))
- [func sec_trust_create(SecTrust) -> sec_trust_t?](/documentation/security/sec_trust_create(_:))

### Macros

- [var errSecErrnoBase: Int32](/documentation/security/errsecerrnobase)
- [var errSecErrnoLimit: Int32](/documentation/security/errsecerrnolimit)
- [var kKeychainSuffix: String](/documentation/security/kkeychainsuffix)
- [var kSystemKeychainDir: String](/documentation/security/ksystemkeychaindir)
- [var kSystemKeychainName: String](/documentation/security/ksystemkeychainname)
- [var kSystemUnlockFile: String](/documentation/security/ksystemunlockfile)

### Type aliases

- [SecAsn1Template](/documentation/security/secasn1template)
- [sec_certificate_t](/documentation/security/sec_certificate_t)
- [sec_identity_t](/documentation/security/sec_identity_t)
- [sec_object_t](/documentation/security/sec_object_t)
- [sec_protocol_challenge_complete_t](/documentation/security/sec_protocol_challenge_complete_t)
- [sec_protocol_challenge_t](/documentation/security/sec_protocol_challenge_t)
- [sec_protocol_key_update_complete_t](/documentation/security/sec_protocol_key_update_complete_t)
- [sec_protocol_key_update_t](/documentation/security/sec_protocol_key_update_t)
- [sec_protocol_metadata_t](/documentation/security/sec_protocol_metadata_t)
- [sec_protocol_options_t](/documentation/security/sec_protocol_options_t)
- [sec_protocol_pre_shared_key_selection_complete_t](/documentation/security/sec_protocol_pre_shared_key_selection_complete_t)
- [sec_protocol_pre_shared_key_selection_t](/documentation/security/sec_protocol_pre_shared_key_selection_t)
- [sec_protocol_verify_complete_t](/documentation/security/sec_protocol_verify_complete_t)
- [sec_protocol_verify_t](/documentation/security/sec_protocol_verify_t)
- [sec_trust_t](/documentation/security/sec_trust_t)
- [sint16](/documentation/security/sint16)
- [sint32](/documentation/security/sint32)
- [sint64](/documentation/security/sint64)
- [sint8](/documentation/security/sint8)
- [uint16](/documentation/security/uint16)
- [uint32](/documentation/security/uint32)
- [uint64](/documentation/security/uint64)
- [uint8](/documentation/security/uint8)

### Enumerations

- [extension_data_format](/documentation/security/extension_data_format)

#### Initializers

- [init(UInt32)](/documentation/security/extension_data_format/init(_:))
- [init(rawValue: UInt32)](/documentation/security/extension_data_format/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/security/extension_data_format/rawvalue)

## Reference

- [Security Structures](/documentation/security/security-structures)

### Structures

- [SecCEBasicConstraints](/documentation/security/seccebasicconstraints)

#### Initializers

- [init()](/documentation/security/seccebasicconstraints/init())
- [init(present: Bool, critical: Bool, isCA: Bool, pathLenConstraintPresent: Bool, pathLenConstraint: UInt32)](/documentation/security/seccebasicconstraints/init(present:critical:isca:pathlenconstraintpresent:pathlenconstraint:))

#### Instance Properties

- [var critical: Bool](/documentation/security/seccebasicconstraints/critical)
- [var isCA: Bool](/documentation/security/seccebasicconstraints/isca)
- [var pathLenConstraint: UInt32](/documentation/security/seccebasicconstraints/pathlenconstraint)
- [var pathLenConstraintPresent: Bool](/documentation/security/seccebasicconstraints/pathlenconstraintpresent)
- [var present: Bool](/documentation/security/seccebasicconstraints/present)
- [SecCEPolicyConstraints](/documentation/security/seccepolicyconstraints)

#### Initializers

- [init()](/documentation/security/seccepolicyconstraints/init())
- [init(present: Bool, critical: Bool, requireExplicitPolicyPresent: Bool, requireExplicitPolicy: UInt32, inhibitPolicyMappingPresent: Bool, inhibitPolicyMapping: UInt32)](/documentation/security/seccepolicyconstraints/init(present:critical:requireexplicitpolicypresent:requireexplicitpolicy:inhibitpolicymappingpresent:inhibitpolicymapping:))

#### Instance Properties

- [var critical: Bool](/documentation/security/seccepolicyconstraints/critical)
- [var inhibitPolicyMapping: UInt32](/documentation/security/seccepolicyconstraints/inhibitpolicymapping)
- [var inhibitPolicyMappingPresent: Bool](/documentation/security/seccepolicyconstraints/inhibitpolicymappingpresent)
- [var present: Bool](/documentation/security/seccepolicyconstraints/present)
- [var requireExplicitPolicy: UInt32](/documentation/security/seccepolicyconstraints/requireexplicitpolicy)
- [var requireExplicitPolicyPresent: Bool](/documentation/security/seccepolicyconstraints/requireexplicitpolicypresent)
- [Security Constants](/documentation/security/security-constants)

### Constants

- [var kAuthorizationExternalFormLength: Int32](/documentation/security/kauthorizationexternalformlength)
- [var kAuthorizationFlags: String](/documentation/security/kauthorizationflags)
- [let kSecCFErrorResourceRecursive: CFString](/documentation/security/kseccferrorresourcerecursive)
- [let kSecCodeInfoDefaultDesignatedLightweightCodeRequirement: CFString](/documentation/security/kseccodeinfodefaultdesignatedlightweightcoderequirement)
- [let kSecCodeInfoStapledNotarizationTicket: CFString](/documentation/security/kseccodeinfostaplednotarizationticket)
- [let kSecImportToMemoryOnly: CFString](/documentation/security/ksecimporttomemoryonly)
- [let kSecMatchHostOrSubdomainOfHost: CFString](/documentation/security/ksecmatchhostorsubdomainofhost)
- [Security Functions](/documentation/security/security-functions)

### Functions

- [func SecCertificateCopyNotValidAfterDate(SecCertificate) -> CFDate?](/documentation/security/seccertificatecopynotvalidafterdate(_:))
- [func SecCertificateCopyNotValidBeforeDate(SecCertificate) -> CFDate?](/documentation/security/seccertificatecopynotvalidbeforedate(_:))
- [func SecCodeCreateWithXPCMessage(xpc_object_t, SecCSFlags, UnsafeMutablePointer<SecCode?>) -> OSStatus](/documentation/security/seccodecreatewithxpcmessage(_:_:_:))
- [func SecCodeValidateFileResource(SecStaticCode, CFString, CFData, SecCSFlags) -> OSStatus](/documentation/security/seccodevalidatefileresource(_:_:_:_:))
- [func SecTaskGetCodeSignStatus(SecTask) -> UInt32](/documentation/security/sectaskgetcodesignstatus(_:))
- [func SecTrustCopyCertificateChain(SecTrust) -> CFArray?](/documentation/security/sectrustcopycertificatechain(_:))
- [func SecTrustCopyKey(SecTrust) -> SecKey?](/documentation/security/sectrustcopykey(_:))
- [Security Data Types](/documentation/security/security-data-types)

### Data Types

- [SecCECrlReason](/documentation/security/seccecrlreason)
- [SecCEKeyUsage](/documentation/security/seccekeyusage)

## Variables

- [var CSSM_APPLE_PRIVATE_CSPDL_CODE_28: Int](/documentation/security/cssm_apple_private_cspdl_code_28)
- [var TLS_ECDHE_PSK_WITH_CHACHA20_POLY1305_SHA256: SSLCipherSuite](/documentation/security/tls_ecdhe_psk_with_chacha20_poly1305_sha256)
- [var errSecMissingQualifiedCertStatement: OSStatus](/documentation/security/errsecmissingqualifiedcertstatement)
- [let kSecPolicyAppleEAPClient: CFString](/documentation/security/ksecpolicyappleeapclient)
- [let kSecPolicyAppleEAPServer: CFString](/documentation/security/ksecpolicyappleeapserver)
- [let kSecPolicyAppleIPSecClient: CFString](/documentation/security/ksecpolicyappleipsecclient)
- [let kSecPolicyAppleIPSecServer: CFString](/documentation/security/ksecpolicyappleipsecserver)
- [let kSecPolicyAppleSSLClient: CFString](/documentation/security/ksecpolicyapplesslclient)
- [let kSecPolicyAppleSSLServer: CFString](/documentation/security/ksecpolicyapplesslserver)
- [let kSecTrustQCStatements: CFString](/documentation/security/ksectrustqcstatements)
- [let kSecTrustQWACValidation: CFString](/documentation/security/ksectrustqwacvalidation)

## Functions

- [func SecIdentityCreate(CFAllocator?, SecCertificate, SecKey) -> SecIdentity?](/documentation/security/secidentitycreate(_:_:_:))
- [func sec_protocol_metadata_copy_negotiated_protocol(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_copy_negotiated_protocol(_:))
- [func sec_protocol_metadata_copy_server_name(sec_protocol_metadata_t) -> UnsafePointer<CChar>?](/documentation/security/sec_protocol_metadata_copy_server_name(_:))

## Type Aliases

- [CE_DataType](/documentation/security/ce_datatype-swift.typealias)
- [CE_ExtendedKeyUsage](/documentation/security/ce_extendedkeyusage-swift.typealias)
- [CE_GeneralNameType](/documentation/security/ce_generalnametype-swift.typealias)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
