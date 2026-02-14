# Security Interface Documentation

Source: https://sosumi.ai/documentation/securityinterface

---
title: Security Interface
source: https://developer.apple.com/documentation/securityinterface
timestamp: 2026-02-13T19:01:55.549Z
---

## Classes

- [SFAuthorizationPluginView](/documentation/securityinterface/sfauthorizationpluginview)

### Initializing an SFAuthorizationPluginView Object

- [init!(callbacks: UnsafePointer<AuthorizationCallbacks>!, andEngineRef: AuthorizationEngineRef!)](/documentation/securityinterface/sfauthorizationpluginview/init(callbacks:andengineref:))

### Getting Instance Information

- [func callbacks() -> UnsafePointer<AuthorizationCallbacks>!](/documentation/securityinterface/sfauthorizationpluginview/callbacks())
- [func engineRef() -> AuthorizationEngineRef!](/documentation/securityinterface/sfauthorizationpluginview/engineref())
- [func lastError() -> (any Error)!](/documentation/securityinterface/sfauthorizationpluginview/lasterror())

### Responding to User Actions

- [func buttonPressed(SFButtonType)](/documentation/securityinterface/sfauthorizationpluginview/buttonpressed(_:))
- [func view(for: SFViewType) -> NSView!](/documentation/securityinterface/sfauthorizationpluginview/view(for:))

### Configuring the User Interface

- [func didActivate()](/documentation/securityinterface/sfauthorizationpluginview/didactivate())
- [func didDeactivate()](/documentation/securityinterface/sfauthorizationpluginview/diddeactivate())
- [func willActivate(withUser: [AnyHashable : Any]!)](/documentation/securityinterface/sfauthorizationpluginview/willactivate(withuser:))

### Setting Up the Keyboard Loop

- [func firstKeyView() -> NSView!](/documentation/securityinterface/sfauthorizationpluginview/firstkeyview())
- [func firstResponder() -> NSResponder!](/documentation/securityinterface/sfauthorizationpluginview/firstresponder())
- [func lastKeyView() -> NSView!](/documentation/securityinterface/sfauthorizationpluginview/lastkeyview())

### Enabling and Disabling Controls

- [func setEnabled(Bool)](/documentation/securityinterface/sfauthorizationpluginview/setenabled(_:))

### Communicating with the Authorization Plug-in

- [func display()](/documentation/securityinterface/sfauthorizationpluginview/display())
- [func setButton(SFButtonType, enabled: Bool)](/documentation/securityinterface/sfauthorizationpluginview/setbutton(_:enabled:))
- [func update()](/documentation/securityinterface/sfauthorizationpluginview/update())

### Constants

- [SFButtonType](/documentation/securityinterface/sfbuttontype)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfbuttontype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfbuttontype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfbuttontype/rawvalue)

#### Constants

- [var SFButtonTypeCancel: SFButtonType](/documentation/securityinterface/sfbuttontypecancel)
- [var SFButtonTypeOK: SFButtonType](/documentation/securityinterface/sfbuttontypeok)
- [var SFButtonTypeBack: SFButtonType](/documentation/securityinterface/sfbuttontypeback)
- [var SFButtonTypeLogin: SFButtonType](/documentation/securityinterface/sfbuttontypelogin)
- [SFViewType](/documentation/securityinterface/sfviewtype)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfviewtype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfviewtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfviewtype/rawvalue)

#### Constants

- [var SFViewTypeIdentityAndCredentials: SFViewType](/documentation/securityinterface/sfviewtypeidentityandcredentials)
- [var SFViewTypeCredentials: SFViewType](/documentation/securityinterface/sfviewtypecredentials)
- [Exceptions](/documentation/securityinterface/exceptions)

#### Constants

- [let SFDisplayViewException: String](/documentation/securityinterface/sfdisplayviewexception)
- [SFAuthorizationView](/documentation/securityinterface/sfauthorizationview)

### Setting up the authorization view

- [func setString(AuthorizationString!)](/documentation/securityinterface/sfauthorizationview/setstring(_:))
- [func setAuthorizationRights(UnsafePointer<AuthorizationRights>!)](/documentation/securityinterface/sfauthorizationview/setauthorizationrights(_:))
- [func setAutoupdate(Bool)](/documentation/securityinterface/sfauthorizationview/setautoupdate(_:))
- [func setAutoupdate(Bool, interval: TimeInterval)](/documentation/securityinterface/sfauthorizationview/setautoupdate(_:interval:))
- [func setFlags(AuthorizationFlags)](/documentation/securityinterface/sfauthorizationview/setflags(_:))
- [func setEnabled(Bool)](/documentation/securityinterface/sfauthorizationview/setenabled(_:))

### Setting and getting the delegate for the view

- [func setDelegate(Any!)](/documentation/securityinterface/sfauthorizationview/setdelegate(_:))
- [func delegate() -> Any!](/documentation/securityinterface/sfauthorizationview/delegate())

### Updating the view

- [func updateStatus(Any!) -> Bool](/documentation/securityinterface/sfauthorizationview/updatestatus(_:))

### Getting information about the authorization view

- [func authorization() -> SFAuthorization!](/documentation/securityinterface/sfauthorizationview/authorization())
- [func authorizationRights() -> UnsafeMutablePointer<AuthorizationRights>!](/documentation/securityinterface/sfauthorizationview/authorizationrights())
- [func authorizationState() -> SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationview/authorizationstate())
- [func isEnabled() -> Bool](/documentation/securityinterface/sfauthorizationview/isenabled())

### Setting the authorization state

- [func authorize(Any!) -> Bool](/documentation/securityinterface/sfauthorizationview/authorize(_:))
- [func deauthorize(Any!) -> Bool](/documentation/securityinterface/sfauthorizationview/deauthorize(_:))

### Delegate methods

- [func authorizationViewShouldDeauthorize(SFAuthorizationView!) -> Bool](/documentation/objectivec/nsobject-swift.class/authorizationviewshoulddeauthorize(_:))
- [func authorizationViewCreatedAuthorization(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewcreatedauthorization(_:))
- [func authorizationViewDidAuthorize(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdidauthorize(_:))
- [func authorizationViewDidDeauthorize(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdiddeauthorize(_:))
- [func authorizationViewDidHide(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewdidhide(_:))
- [func authorizationViewReleasedAuthorization(SFAuthorizationView!)](/documentation/objectivec/nsobject-swift.class/authorizationviewreleasedauthorization(_:))

### Constants

- [SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewstate)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfauthorizationviewstate/rawvalue)

#### Constants

- [var SFAuthorizationStartupState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationstartupstate)
- [var SFAuthorizationViewInProgressState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewinprogressstate)
- [var SFAuthorizationViewLockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewlockedstate)
- [var SFAuthorizationViewUnlockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewunlockedstate)
- [SFCertificatePanel](/documentation/securityinterface/sfcertificatepanel)

### Returning a Shared Certificate Panel Object

- [class func shared() -> SFCertificatePanel!](/documentation/securityinterface/sfcertificatepanel/shared())

### Providing Help

- [func setHelpAnchor(String!)](/documentation/securityinterface/sfcertificatepanel/sethelpanchor(_:))
- [func setShowsHelp(Bool)](/documentation/securityinterface/sfcertificatepanel/setshowshelp(_:))
- [func helpAnchor() -> String!](/documentation/securityinterface/sfcertificatepanel/helpanchor())
- [func showsHelp() -> Bool](/documentation/securityinterface/sfcertificatepanel/showshelp())

### Customizing the Appearance of the Sheet or Panel

- [func setAlternateButtonTitle(String!)](/documentation/securityinterface/sfcertificatepanel/setalternatebuttontitle(_:))
- [func setDefaultButtonTitle(String!)](/documentation/securityinterface/sfcertificatepanel/setdefaultbuttontitle(_:))
- [func setPolicies(Any!)](/documentation/securityinterface/sfcertificatepanel/setpolicies(_:))
- [func policies() -> [Any]!](/documentation/securityinterface/sfcertificatepanel/policies())

### Displaying a Sheet or Panel

- [func beginSheet(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!, certificates: [Any]!, showGroup: Bool)](/documentation/securityinterface/sfcertificatepanel/beginsheet(for:modaldelegate:didend:contextinfo:certificates:showgroup:))
- [func beginSheet(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!, trust: SecTrust!, showGroup: Bool)](/documentation/securityinterface/sfcertificatepanel/beginsheet(for:modaldelegate:didend:contextinfo:trust:showgroup:))
- [func certificateView() -> SFCertificateView!](/documentation/securityinterface/sfcertificatepanel/certificateview())
- [func runModal(for: SecTrust!, showGroup: Bool) -> Int](/documentation/securityinterface/sfcertificatepanel/runmodal(for:showgroup:))
- [func runModal(forCertificates: [Any]!, showGroup: Bool) -> Int](/documentation/securityinterface/sfcertificatepanel/runmodal(forcertificates:showgroup:))

### Delegate method for providing help

- [func certificatePanelShowHelp(SFCertificatePanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/certificatepanelshowhelp(_:))
- [SFCertificateTrustPanel](/documentation/securityinterface/sfcertificatetrustpanel)

### Returning a Shared Certificate Trust Panel Object

- [class func shared() -> SFCertificateTrustPanel!](/documentation/securityinterface/sfcertificatetrustpanel/shared())

### Displaying a Sheet or Panel

- [func beginSheet(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!, trust: SecTrust!, message: String!)](/documentation/securityinterface/sfcertificatetrustpanel/beginsheet(for:modaldelegate:didend:contextinfo:trust:message:))
- [func runModal(for: SecTrust!, message: String!) -> Int](/documentation/securityinterface/sfcertificatetrustpanel/runmodal(for:message:))

### Controlling the Appearance of a Certificate Trust Panel

- [func informativeText() -> String!](/documentation/securityinterface/sfcertificatetrustpanel/informativetext())
- [func setInformativeText(String!)](/documentation/securityinterface/sfcertificatetrustpanel/setinformativetext(_:))
- [SFCertificateView](/documentation/securityinterface/sfcertificateview)

### Specifying the Certificate to Display

- [func setCertificate(SecCertificate!)](/documentation/securityinterface/sfcertificateview/setcertificate(_:))

### Customizing the Appearance and Behavior of the View

- [func setDetailsDisclosed(Bool)](/documentation/securityinterface/sfcertificateview/setdetailsdisclosed(_:))
- [func setDisplayDetails(Bool)](/documentation/securityinterface/sfcertificateview/setdisplaydetails(_:))
- [func setDisplayTrust(Bool)](/documentation/securityinterface/sfcertificateview/setdisplaytrust(_:))
- [func setEditableTrust(Bool)](/documentation/securityinterface/sfcertificateview/seteditabletrust(_:))
- [func setPolicies(Any!)](/documentation/securityinterface/sfcertificateview/setpolicies(_:))
- [func setPoliciesDisclosed(Bool)](/documentation/securityinterface/sfcertificateview/setpoliciesdisclosed(_:))

### Getting Information About the View

- [func certificate() -> Unmanaged<SecCertificate>!](/documentation/securityinterface/sfcertificateview/certificate())
- [func detailsDisplayed() -> Bool](/documentation/securityinterface/sfcertificateview/detailsdisplayed())
- [func detailsDisclosed() -> Bool](/documentation/securityinterface/sfcertificateview/detailsdisclosed())
- [func isTrustDisplayed() -> Bool](/documentation/securityinterface/sfcertificateview/istrustdisplayed())
- [func isEditable() -> Bool](/documentation/securityinterface/sfcertificateview/iseditable())
- [func policies() -> [Any]!](/documentation/securityinterface/sfcertificateview/policies())
- [func policiesDisclosed() -> Bool](/documentation/securityinterface/sfcertificateview/policiesdisclosed())

### Saving User Trust Settings

- [func saveTrustSettings()](/documentation/securityinterface/sfcertificateview/savetrustsettings())

### Constants

- [Notifications](/documentation/securityinterface/notifications)

#### Constants

- [let SFCertificateViewDisclosureStateDidChange: String](/documentation/securityinterface/sfcertificateviewdisclosurestatedidchange)
- [SFChooseIdentityPanel](/documentation/securityinterface/sfchooseidentitypanel)

### Returning a Shared Certificate Panel Object

- [class func shared() -> SFChooseIdentityPanel!](/documentation/securityinterface/sfchooseidentitypanel/shared())

### Providing Help

- [func setHelpAnchor(String!)](/documentation/securityinterface/sfchooseidentitypanel/sethelpanchor(_:))
- [func setShowsHelp(Bool)](/documentation/securityinterface/sfchooseidentitypanel/setshowshelp(_:))
- [func helpAnchor() -> String!](/documentation/securityinterface/sfchooseidentitypanel/helpanchor())
- [func showsHelp() -> Bool](/documentation/securityinterface/sfchooseidentitypanel/showshelp())

### Customizing the Appearance of the Sheet or Panel

- [func setAlternateButtonTitle(String!)](/documentation/securityinterface/sfchooseidentitypanel/setalternatebuttontitle(_:))
- [func setDefaultButtonTitle(String!)](/documentation/securityinterface/sfchooseidentitypanel/setdefaultbuttontitle(_:))
- [func setPolicies(Any!)](/documentation/securityinterface/sfchooseidentitypanel/setpolicies(_:))
- [func policies() -> [Any]!](/documentation/securityinterface/sfchooseidentitypanel/policies())
- [func informativeText() -> String!](/documentation/securityinterface/sfchooseidentitypanel/informativetext())
- [func setInformativeText(String!)](/documentation/securityinterface/sfchooseidentitypanel/setinformativetext(_:))

### Displaying a Sheet or Panel

- [func beginSheet(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!, identities: [Any]!, message: String!)](/documentation/securityinterface/sfchooseidentitypanel/beginsheet(for:modaldelegate:didend:contextinfo:identities:message:))
- [func runModal(forIdentities: [Any]!, message: String!) -> Int](/documentation/securityinterface/sfchooseidentitypanel/runmodal(foridentities:message:))

### Getting Identity Information from a Sheet or Panel

- [func identity() -> Unmanaged<SecIdentity>!](/documentation/securityinterface/sfchooseidentitypanel/identity())

### Working with Domains

- [func domain() -> String!](/documentation/securityinterface/sfchooseidentitypanel/domain())
- [func setDomain(String!)](/documentation/securityinterface/sfchooseidentitypanel/setdomain(_:))

### Delegate methods for providing help

- [func chooseIdentityPanelShowHelp(SFChooseIdentityPanel!) -> Bool](/documentation/objectivec/nsobject-swift.class/chooseidentitypanelshowhelp(_:))
- [SFChooseIdentityTableCellView](/documentation/securityinterface/sfchooseidentitytablecellview)

### Instance Properties

- [var issuerTextField: NSTextField!](/documentation/securityinterface/sfchooseidentitytablecellview/issuertextfield-swift.property)
- [SFKeychainSavePanel](/documentation/securityinterface/sfkeychainsavepanel)

### Returning a Shared Keychain Save Panel Object

- [class func shared() -> SFKeychainSavePanel!](/documentation/securityinterface/sfkeychainsavepanel/shared())

### Displaying a Sheet or Panel

- [func setPassword(String!)](/documentation/securityinterface/sfkeychainsavepanel/setpassword(_:))
- [func beginSheet(forDirectory: String!, file: String!, modalFor: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!)](/documentation/securityinterface/sfkeychainsavepanel/beginsheet(fordirectory:file:modalfor:modaldelegate:didend:contextinfo:))
- [func runModal(forDirectory: String!, file: String!) -> Int](/documentation/securityinterface/sfkeychainsavepanel/runmodal(fordirectory:file:))

### Returning Information from the Sheet or Panel

- [func error() -> (any Error)!](/documentation/securityinterface/sfkeychainsavepanel/error())
- [func keychain() -> Unmanaged<SecKeychain>!](/documentation/securityinterface/sfkeychainsavepanel/keychain())
- [SFKeychainSettingsPanel](/documentation/securityinterface/sfkeychainsettingspanel)

### Returning a shared keychain save panel object

- [class func shared() -> SFKeychainSettingsPanel!](/documentation/securityinterface/sfkeychainsettingspanel/shared())

### Displaying a sheet or panel

- [func beginSheet(for: NSWindow!, modalDelegate: Any!, didEnd: Selector!, contextInfo: UnsafeMutableRawPointer!, settings: UnsafeMutablePointer<SecKeychainSettings>!, keychain: SecKeychain!)](/documentation/securityinterface/sfkeychainsettingspanel/beginsheet(for:modaldelegate:didend:contextinfo:settings:keychain:))
- [func runModal(for: UnsafeMutablePointer<SecKeychainSettings>!, keychain: SecKeychain!) -> Int](/documentation/securityinterface/sfkeychainsettingspanel/runmodal(for:keychain:))

## Reference

- [SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewstate)

### Initializers

- [init(UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfauthorizationviewstate/rawvalue)

### Constants

- [var SFAuthorizationStartupState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationstartupstate)
- [var SFAuthorizationViewInProgressState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewinprogressstate)
- [var SFAuthorizationViewLockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewlockedstate)
- [var SFAuthorizationViewUnlockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewunlockedstate)
- [SFButtonType](/documentation/securityinterface/sfbuttontype)

### Initializers

- [init(UInt32)](/documentation/securityinterface/sfbuttontype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfbuttontype/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfbuttontype/rawvalue)

### Constants

- [var SFButtonTypeCancel: SFButtonType](/documentation/securityinterface/sfbuttontypecancel)
- [var SFButtonTypeOK: SFButtonType](/documentation/securityinterface/sfbuttontypeok)
- [var SFButtonTypeBack: SFButtonType](/documentation/securityinterface/sfbuttontypeback)
- [var SFButtonTypeLogin: SFButtonType](/documentation/securityinterface/sfbuttontypelogin)
- [SFViewType](/documentation/securityinterface/sfviewtype)

### Initializers

- [init(UInt32)](/documentation/securityinterface/sfviewtype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfviewtype/init(rawvalue:))

### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfviewtype/rawvalue)

### Constants

- [var SFViewTypeIdentityAndCredentials: SFViewType](/documentation/securityinterface/sfviewtypeidentityandcredentials)
- [var SFViewTypeCredentials: SFViewType](/documentation/securityinterface/sfviewtypecredentials)
- [SecurityInterface Constants](/documentation/securityinterface/securityinterface-constants)

### Constants

- [Plug-in View Keys](/documentation/securityinterface/plug-in-view-keys)

#### Constants

- [let SFAuthorizationPluginViewUserNameKey: String](/documentation/securityinterface/sfauthorizationpluginviewusernamekey)
- [let SFAuthorizationPluginViewUserShortNameKey: String](/documentation/securityinterface/sfauthorizationpluginviewusershortnamekey)
- [let SFCertificateViewDisclosureStateDidChange: String](/documentation/securityinterface/sfcertificateviewdisclosurestatedidchange)
- [let SFDisplayViewException: String](/documentation/securityinterface/sfdisplayviewexception)
- [SecurityInterface Data Types](/documentation/securityinterface/securityinterface-data-types)

### Data Types

- [SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewstate)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfauthorizationviewstate/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfauthorizationviewstate/rawvalue)

#### Constants

- [var SFAuthorizationStartupState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationstartupstate)
- [var SFAuthorizationViewInProgressState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewinprogressstate)
- [var SFAuthorizationViewLockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewlockedstate)
- [var SFAuthorizationViewUnlockedState: SFAuthorizationViewState](/documentation/securityinterface/sfauthorizationviewunlockedstate)
- [SecurityInterface Enumerations](/documentation/securityinterface/securityinterface-enumerations)

### Enumerations

- [SFButtonType](/documentation/securityinterface/sfbuttontype)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfbuttontype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfbuttontype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfbuttontype/rawvalue)

#### Constants

- [var SFButtonTypeCancel: SFButtonType](/documentation/securityinterface/sfbuttontypecancel)
- [var SFButtonTypeOK: SFButtonType](/documentation/securityinterface/sfbuttontypeok)
- [var SFButtonTypeBack: SFButtonType](/documentation/securityinterface/sfbuttontypeback)
- [var SFButtonTypeLogin: SFButtonType](/documentation/securityinterface/sfbuttontypelogin)
- [SFViewType](/documentation/securityinterface/sfviewtype)

#### Initializers

- [init(UInt32)](/documentation/securityinterface/sfviewtype/init(_:))
- [init(rawValue: UInt32)](/documentation/securityinterface/sfviewtype/init(rawvalue:))

#### Instance Properties

- [var rawValue: UInt32](/documentation/securityinterface/sfviewtype/rawvalue)

#### Constants

- [var SFViewTypeIdentityAndCredentials: SFViewType](/documentation/securityinterface/sfviewtypeidentityandcredentials)
- [var SFViewTypeCredentials: SFViewType](/documentation/securityinterface/sfviewtypecredentials)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
