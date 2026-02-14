# Managed Settings Documentation

Source: https://sosumi.ai/documentation/managedsettings

---
title: ManagedSettings
source: https://developer.apple.com/documentation/managedsettings
timestamp: 2026-02-13T18:59:03.351Z
---

## Essentials

- [Manage Settings on Devices in a Family Sharing Group](/documentation/managedsettings/connectionwithframeworks)
- [Confirming the Effective TV and Movie Ratings](/documentation/managedsettings/readingmedia)

## Settings

- [ManagedSettingsStore](/documentation/managedsettings/managedsettingsstore)

### Creating the Store

- [init()](/documentation/managedsettings/managedsettingsstore/init())

### Managing a Settings Group

- [ManagedSettingsGroup](/documentation/managedsettings/managedsettingsgroup)

### Restricting Device Settings

- [var account: AccountSettings](/documentation/managedsettings/managedsettingsstore/account)
- [AccountSettings](/documentation/managedsettings/accountsettings)

#### Constraining Accounts

- [var lockAccounts: Bool?](/documentation/managedsettings/accountsettings/lockaccounts-swift.property)
- [static let lockAccounts: SettingMetadata<Bool>](/documentation/managedsettings/accountsettings/lockaccounts-swift.type.property)
- [var cellular: CellularSettings](/documentation/managedsettings/managedsettingsstore/cellular)
- [CellularSettings](/documentation/managedsettings/cellularsettings)

#### Locking App Access to Cell Data

- [var lockAppCellularData: Bool?](/documentation/managedsettings/cellularsettings/lockappcellulardata-swift.property)
- [static let lockAppCellularData: SettingMetadata<Bool>](/documentation/managedsettings/cellularsettings/lockappcellulardata-swift.type.property)

#### Locking the Device’s Cell Plan

- [var lockCellularPlan: Bool?](/documentation/managedsettings/cellularsettings/lockcellularplan-swift.property)
- [static let lockCellularPlan: SettingMetadata<Bool>](/documentation/managedsettings/cellularsettings/lockcellularplan-swift.type.property)

#### Locking the Device’s eSIM Settings

- [var lockESIM: Bool?](/documentation/managedsettings/cellularsettings/lockesim-swift.property)
- [static let lockESIM: SettingMetadata<Bool>](/documentation/managedsettings/cellularsettings/lockesim-swift.type.property)
- [var dateAndTime: DateAndTimeSettings](/documentation/managedsettings/managedsettingsstore/dateandtime)
- [DateAndTimeSettings](/documentation/managedsettings/dateandtimesettings)

#### Requiring Automatic Date and Time

- [var requireAutomaticDateAndTime: Bool?](/documentation/managedsettings/dateandtimesettings/requireautomaticdateandtime-swift.property)
- [static let requireAutomaticDateAndTime: SettingMetadata<Bool>](/documentation/managedsettings/dateandtimesettings/requireautomaticdateandtime-swift.type.property)
- [var passcode: PasscodeSettings](/documentation/managedsettings/managedsettingsstore/passcode)
- [PasscodeSettings](/documentation/managedsettings/passcodesettings)

#### Blocking Passcode Changes

- [var lockPasscode: Bool?](/documentation/managedsettings/passcodesettings/lockpasscode-swift.property)
- [static let lockPasscode: SettingMetadata<Bool>](/documentation/managedsettings/passcodesettings/lockpasscode-swift.type.property)
- [var shield: ShieldSettings](/documentation/managedsettings/managedsettingsstore/shield)
- [ShieldSettings](/documentation/managedsettings/shieldsettings)

#### Blocking Apps and Websites

- [var applications: Set<ApplicationToken>?](/documentation/managedsettings/shieldsettings/applications-swift.property)
- [static let applications: SettingMetadata<Set<ApplicationToken>>](/documentation/managedsettings/shieldsettings/applications-swift.type.property)
- [var webDomains: Set<WebDomainToken>?](/documentation/managedsettings/shieldsettings/webdomains-swift.property)
- [static let webDomains: SettingMetadata<Set<WebDomainToken>>](/documentation/managedsettings/shieldsettings/webdomains-swift.type.property)

#### Blocking Categories of Apps and Websites

- [ShieldSettings.ActivityCategoryPolicy](/documentation/managedsettings/shieldsettings/activitycategorypolicy)

##### Shielding Categories

- [case none](/documentation/managedsettings/shieldsettings/activitycategorypolicy/none)
- [case all(except: Set<Token<Activity>>)](/documentation/managedsettings/shieldsettings/activitycategorypolicy/all(except:))
- [case specific(Set<ActivityCategoryToken>, except: Set<Token<Activity>>)](/documentation/managedsettings/shieldsettings/activitycategorypolicy/specific(_:except:))

##### Getting the Range

- [static func == (ShieldSettings.ActivityCategoryPolicy<Activity>, ShieldSettings.ActivityCategoryPolicy<Activity>) -> Bool](/documentation/managedsettings/shieldsettings/activitycategorypolicy/==(_:_:))
- [var applicationCategories: ShieldSettings.ActivityCategoryPolicy<Application>?](/documentation/managedsettings/shieldsettings/applicationcategories-swift.property)
- [static let applicationCategories: SettingMetadata<ShieldSettings.ActivityCategoryPolicy<Application>>](/documentation/managedsettings/shieldsettings/applicationcategories-swift.type.property)
- [var webDomainCategories: ShieldSettings.ActivityCategoryPolicy<WebDomain>?](/documentation/managedsettings/shieldsettings/webdomaincategories-swift.property)
- [static let webDomainCategories: SettingMetadata<ShieldSettings.ActivityCategoryPolicy<WebDomain>>](/documentation/managedsettings/shieldsettings/webdomaincategories-swift.type.property)
- [var siri: SiriSettings](/documentation/managedsettings/managedsettingsstore/siri)
- [SiriSettings](/documentation/managedsettings/sirisettings)

#### Restricting Siri Usage

- [var denySiri: Bool?](/documentation/managedsettings/sirisettings/denysiri-swift.property)
- [static let denySiri: SettingMetadata<Bool>](/documentation/managedsettings/sirisettings/denysiri-swift.type.property)

### Filtering Media Content

- [var appStore: AppStoreSettings](/documentation/managedsettings/managedsettingsstore/appstore)
- [AppStoreSettings](/documentation/managedsettings/appstoresettings)

#### Denying In-App Purchases

- [var denyInAppPurchases: Bool?](/documentation/managedsettings/appstoresettings/denyinapppurchases-swift.property)
- [static let denyInAppPurchases: SettingMetadata<Bool>](/documentation/managedsettings/appstoresettings/denyinapppurchases-swift.type.property)

#### Setting an App Rating Limit

- [var maximumRating: Int?](/documentation/managedsettings/appstoresettings/maximumrating-swift.property)
- [static let maximumRating: BoundedSettingMetadata<Int>](/documentation/managedsettings/appstoresettings/maximumrating-swift.type.property)

#### Requiring a Password

- [var requirePasswordForPurchases: Bool?](/documentation/managedsettings/appstoresettings/requirepasswordforpurchases-swift.property)
- [static let requirePasswordForPurchases: SettingMetadata<Bool>](/documentation/managedsettings/appstoresettings/requirepasswordforpurchases-swift.type.property)
- [var application: ApplicationSettings](/documentation/managedsettings/managedsettingsstore/application)
- [ApplicationSettings](/documentation/managedsettings/applicationsettings)

#### Blocking Applications

- [var blockedApplications: Set<Application>?](/documentation/managedsettings/applicationsettings/blockedapplications-swift.property)
- [static let blockedApplications: SettingMetadata<Set<Application>>](/documentation/managedsettings/applicationsettings/blockedapplications-swift.type.property)

#### Preventing App Installation and Removal

- [var denyAppInstallation: Bool?](/documentation/managedsettings/applicationsettings/denyappinstallation-swift.property)
- [static let denyAppInstallation: SettingMetadata<Bool>](/documentation/managedsettings/applicationsettings/denyappinstallation-swift.type.property)
- [var denyAppRemoval: Bool?](/documentation/managedsettings/applicationsettings/denyappremoval-swift.property)
- [static let denyAppRemoval: SettingMetadata<Bool>](/documentation/managedsettings/applicationsettings/denyappremoval-swift.type.property)
- [var effectiveMaximumMovieRating: Int](/documentation/managedsettings/managedsettingsstore/effectivemaximummovierating)
- [var effectiveMaximumTVShowRating: Int](/documentation/managedsettings/managedsettingsstore/effectivemaximumtvshowrating)
- [var gameCenter: GameCenterSettings](/documentation/managedsettings/managedsettingsstore/gamecenter)
- [GameCenterSettings](/documentation/managedsettings/gamecentersettings)

#### Denying the Ability to Join Multiplayer Games

- [var denyMultiplayerGaming: Bool?](/documentation/managedsettings/gamecentersettings/denymultiplayergaming-swift.property)
- [static let denyMultiplayerGaming: SettingMetadata<Bool>](/documentation/managedsettings/gamecentersettings/denymultiplayergaming-swift.type.property)

#### Denying the Ability to Add Friends

- [var denyAddingFriends: Bool?](/documentation/managedsettings/gamecentersettings/denyaddingfriends-swift.property)
- [static let denyAddingFriends: SettingMetadata<Bool>](/documentation/managedsettings/gamecentersettings/denyaddingfriends-swift.type.property)
- [var media: MediaSettings](/documentation/managedsettings/managedsettingsstore/media)
- [MediaSettings](/documentation/managedsettings/mediasettings)

#### Limiting Movie and TV Show Ratings

- [var maximumMovieRating: Int?](/documentation/managedsettings/mediasettings/maximummovierating-swift.property)
- [var maximumTVShowRating: Int?](/documentation/managedsettings/mediasettings/maximumtvshowrating-swift.property)
- [static let maximumMovieRating: BoundedSettingMetadata<Int>](/documentation/managedsettings/mediasettings/maximummovierating-swift.type.property)
- [static let maximumTVShowRating: BoundedSettingMetadata<Int>](/documentation/managedsettings/mediasettings/maximumtvshowrating-swift.type.property)

#### Denying Explicit Media

- [var denyExplicitContent: Bool?](/documentation/managedsettings/mediasettings/denyexplicitcontent-swift.property)
- [static let denyExplicitContent: SettingMetadata<Bool>](/documentation/managedsettings/mediasettings/denyexplicitcontent-swift.type.property)

#### Denying the Apple Music Service

- [var denyMusicService: Bool?](/documentation/managedsettings/mediasettings/denymusicservice-swift.property)
- [static let denyMusicService: SettingMetadata<Bool>](/documentation/managedsettings/mediasettings/denymusicservice-swift.type.property)

#### Constraining Content in the Books App

- [var denyBookstoreErotica: Bool?](/documentation/managedsettings/mediasettings/denybookstoreerotica-swift.property)
- [static let denyBookstoreErotica: SettingMetadata<Bool>](/documentation/managedsettings/mediasettings/denybookstoreerotica-swift.type.property)

### Restricting Web Content

- [var safari: SafariSettings](/documentation/managedsettings/managedsettingsstore/safari)
- [SafariSettings](/documentation/managedsettings/safarisettings)

#### Specifying a Cookie Policy

- [var cookiePolicy: SafariSettings.CookiePolicy?](/documentation/managedsettings/safarisettings/cookiepolicy-swift.property)
- [static let cookiePolicy: SettingMetadata<SafariSettings.CookiePolicy>](/documentation/managedsettings/safarisettings/cookiepolicy-swift.type.property)
- [SafariSettings.CookiePolicy](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum)

##### Accepting Cookies

- [case always](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum/always)
- [case currentWebsite](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum/currentwebsite)
- [case never](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum/never)
- [case visitedWebsites](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum/visitedwebsites)

##### Operators

- [static func < (SafariSettings.CookiePolicy, SafariSettings.CookiePolicy) -> Bool](/documentation/managedsettings/safarisettings/cookiepolicy-swift.enum/_(_:_:))

#### Denying AutoFill

- [var denyAutoFill: Bool?](/documentation/managedsettings/safarisettings/denyautofill-swift.property)
- [static let denyAutoFill: SettingMetadata<Bool>](/documentation/managedsettings/safarisettings/denyautofill-swift.type.property)
- [var webContent: WebContentSettings](/documentation/managedsettings/managedsettingsstore/webcontent)
- [WebContentSettings](/documentation/managedsettings/webcontentsettings)

#### Filtering Web Domains

- [var blockedByFilter: WebContentSettings.FilterPolicy?](/documentation/managedsettings/webcontentsettings/blockedbyfilter-swift.property)
- [static let blockedByFilter: SettingMetadata<WebContentSettings.FilterPolicy>](/documentation/managedsettings/webcontentsettings/blockedbyfilter-swift.type.property)
- [WebContentSettings.FilterPolicy](/documentation/managedsettings/webcontentsettings/filterpolicy)

##### Providing Filters and Exceptions

- [case all(except: Set<WebDomain>)](/documentation/managedsettings/webcontentsettings/filterpolicy/all(except:))
- [case auto(Set<WebDomain>, except: Set<WebDomain>)](/documentation/managedsettings/webcontentsettings/filterpolicy/auto(_:except:))
- [case none](/documentation/managedsettings/webcontentsettings/filterpolicy/none)
- [case specific(Set<WebDomain>)](/documentation/managedsettings/webcontentsettings/filterpolicy/specific(_:))

##### Comparing Policies

- [static func == (WebContentSettings.FilterPolicy, WebContentSettings.FilterPolicy) -> Bool](/documentation/managedsettings/webcontentsettings/filterpolicy/==(_:_:))

### Accessing Metadata

- [BoundedSettingMetadata](/documentation/managedsettings/boundedsettingmetadata)

#### Getting Metadata

- [let bounds: ClosedRange<Value>](/documentation/managedsettings/boundedsettingmetadata/bounds)
- [let defaultValue: Value](/documentation/managedsettings/boundedsettingmetadata/defaultvalue)
- [SettingMetadata](/documentation/managedsettings/settingmetadata)

#### Getting the Default

- [let defaultValue: Value](/documentation/managedsettings/settingmetadata/defaultvalue)

### Observing Current Settings

- [var $effectiveMaximumMovieRating: Published<Int>.Publisher](/documentation/managedsettings/managedsettingsstore/$effectivemaximummovierating)
- [var $effectiveMaximumTVShowRating: Published<Int>.Publisher](/documentation/managedsettings/managedsettingsstore/$effectivemaximumtvshowrating)

### Structures

- [ManagedSettingsStore.Name](/documentation/managedsettings/managedsettingsstore/name)

#### Initializers

- [init(String)](/documentation/managedsettings/managedsettingsstore/name/init(_:))
- [init(rawValue: String)](/documentation/managedsettings/managedsettingsstore/name/init(rawvalue:))

#### Instance Properties

- [let rawValue: String](/documentation/managedsettings/managedsettingsstore/name/rawvalue)

#### Type Properties

- [static let `default`: ManagedSettingsStore.Name](/documentation/managedsettings/managedsettingsstore/name/default)

### Initializers

- [convenience init(named: ManagedSettingsStore.Name)](/documentation/managedsettings/managedsettingsstore/init(named:))

### Instance Properties

- [var $effectiveDenyExplicitContent: Published<Bool>.Publisher](/documentation/managedsettings/managedsettingsstore/$effectivedenyexplicitcontent)
- [var effectiveDenyExplicitContent: Bool](/documentation/managedsettings/managedsettingsstore/effectivedenyexplicitcontent)

### Instance Methods

- [func clearAllSettings()](/documentation/managedsettings/managedsettingsstore/clearallsettings())

## Shield Actions

- [ShieldActionDelegate](/documentation/managedsettings/shieldactiondelegate)

### Handling Shield Actions

- [ShieldAction](/documentation/managedsettings/shieldaction)

#### Buttons

- [case primaryButtonPressed](/documentation/managedsettings/shieldaction/primarybuttonpressed)
- [case secondaryButtonPressed](/documentation/managedsettings/shieldaction/secondarybuttonpressed)
- [ShieldActionResponse](/documentation/managedsettings/shieldactionresponse)

#### Responses

- [case close](/documentation/managedsettings/shieldactionresponse/close)
- [case `defer`](/documentation/managedsettings/shieldactionresponse/defer)
- [case none](/documentation/managedsettings/shieldactionresponse/none)

### Initializers

- [init()](/documentation/managedsettings/shieldactiondelegate/init())

### Instance Methods

- [func handle(action: ShieldAction, for: ApplicationToken, completionHandler: (ShieldActionResponse) -> Void)](/documentation/managedsettings/shieldactiondelegate/handle(action:for:completionhandler:)-4jgek)
- [func handle(action: ShieldAction, for: WebDomainToken, completionHandler: (ShieldActionResponse) -> Void)](/documentation/managedsettings/shieldactiondelegate/handle(action:for:completionhandler:)-4tqna)
- [func handle(action: ShieldAction, for: ActivityCategoryToken, completionHandler: (ShieldActionResponse) -> Void)](/documentation/managedsettings/shieldactiondelegate/handle(action:for:completionhandler:)-9hcqc)

## Family Privacy

- [Token](/documentation/managedsettings/token)

## Apps

- [Application](/documentation/managedsettings/application)

### Creating an Application

- [init(bundleIdentifier: String)](/documentation/managedsettings/application/init(bundleidentifier:))
- [init(token: ApplicationToken)](/documentation/managedsettings/application/init(token:))

### Accessing Application Information

- [let bundleIdentifier: String?](/documentation/managedsettings/application/bundleidentifier)
- [let token: ApplicationToken?](/documentation/managedsettings/application/token)
- [let localizedDisplayName: String?](/documentation/managedsettings/application/localizeddisplayname)
- [ApplicationToken](/documentation/managedsettings/applicationtoken)

## Categories

- [ActivityCategory](/documentation/managedsettings/activitycategory)

### Creating a Category

- [init(token: ActivityCategoryToken)](/documentation/managedsettings/activitycategory/init(token:))

### Accessing Category Identifiers

- [let localizedDisplayName: String?](/documentation/managedsettings/activitycategory/localizeddisplayname)
- [let token: ActivityCategoryToken?](/documentation/managedsettings/activitycategory/token)
- [ActivityCategoryToken](/documentation/managedsettings/activitycategorytoken)

## Websites

- [WebDomain](/documentation/managedsettings/webdomain)

### Creating a Web Domain

- [init(domain: String)](/documentation/managedsettings/webdomain/init(domain:))
- [init(token: WebDomainToken)](/documentation/managedsettings/webdomain/init(token:))

### Identifying a Web Domain

- [let domain: String?](/documentation/managedsettings/webdomain/domain)
- [let token: WebDomainToken?](/documentation/managedsettings/webdomain/token)
- [WebDomainToken](/documentation/managedsettings/webdomaintoken)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
