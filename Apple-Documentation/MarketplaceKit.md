# MarketplaceKit Documentation

Source: https://sosumi.ai/documentation/marketplacekit

---
title: MarketplaceKit
source: https://developer.apple.com/documentation/marketplacekit
timestamp: 2026-02-13T18:59:12.888Z
---

## Essentials

- [Creating an alternative app marketplace](/documentation/marketplacekit/creating-an-alternative-app-marketplace)
- [Distributing your app from your website](/documentation/marketplacekit/distributing-your-app-from-your-website)
- [Distributing your app on an alternative app marketplace](/documentation/marketplacekit/distributing-your-app-on-an-alternative-marketplace)

## Web services

- [Processing alternative app marketplace notifications](/documentation/marketplacekit/processing-alternative-marketplace-notifications)
- [Ingesting an alternative distribution package](/documentation/marketplacekit/ingesting-an-alternative-distribution-package)
- [Installing your app from your website](/documentation/marketplacekit/installing-your-app-from-your-website)
- [Installing apps from an alternative marketplace](/documentation/marketplacekit/installing-apps-from-an-alternative-marketplace)
- [Supplying an install verification token](/documentation/marketplacekit/supplying-an-install-verification-token)

## Authorization

- [Reauthenticating a person to manage apps](/documentation/marketplacekit/reauthenticating-a-person-to-manage-apps)
- [Providing age-rating appropriate content](/documentation/marketplacekit/providing-age-rating-appropriate-content)
- [com.apple.developer.marketplace.app-installation](/documentation/bundleresources/entitlements/com.apple.developer.marketplace.app-installation)
- [com.apple.developer.browser.app-installation](/documentation/bundleresources/entitlements/com.apple.developer.browser.app-installation)
- [App License Delivery SDK](/documentation/applicensedeliverysdk)

## Browser support

- [Enabling alternative distribution app installation in a browser](/documentation/marketplacekit/enabling-alternative-distribution-app-installation-in-a-browser)

## App management

- [AppLibrary](/documentation/marketplacekit/applibrary)

### Accessing app library and account authorization information

- [static let current: AppLibrary](/documentation/marketplacekit/applibrary/current)
- [func didAuthenticate(account: String) async](/documentation/marketplacekit/applibrary/didauthenticate(account:))

### Managing app installation

- [AppLibrary.App](/documentation/marketplacekit/applibrary/app)

#### Inspecting an app’s version and account

- [var installedMetadata: AppLibrary.App.Metadata?](/documentation/marketplacekit/applibrary/app/installedmetadata)
- [AppLibrary.App.Metadata](/documentation/marketplacekit/applibrary/app/metadata)

##### Inspecting app metadata

- [let account: String?](/documentation/marketplacekit/applibrary/app/metadata/account)
- [let appleVersionID: AppleVersionID](/documentation/marketplacekit/applibrary/app/metadata/appleversionid)
- [let shortVersion: String](/documentation/marketplacekit/applibrary/app/metadata/shortversion)
- [let version: String](/documentation/marketplacekit/applibrary/app/metadata/version)

#### Inspecting app installation and update status

- [var installation: AppLibrary.App.Installation?](/documentation/marketplacekit/applibrary/app/installation-swift.property)
- [AppLibrary.App.Installation](/documentation/marketplacekit/applibrary/app/installation-swift.struct)

##### Inspecting installation progress

- [var progress: Progress](/documentation/marketplacekit/applibrary/app/installation-swift.struct/progress)
- [var isInstalled: Bool](/documentation/marketplacekit/applibrary/app/isinstalled)
- [var isInstalling: Bool](/documentation/marketplacekit/applibrary/app/isinstalling)
- [var isUpdating: Bool](/documentation/marketplacekit/applibrary/app/isupdating)
- [var installationError: MarketplaceKitError?](/documentation/marketplacekit/applibrary/app/installationerror)

#### Requesting installation approval

- [func presentAgeExceptionApproveInPersonSheet() async throws](/documentation/marketplacekit/applibrary/app/presentageexceptionapproveinpersonsheet())
- [AppLibrary.InstallationRequest](/documentation/marketplacekit/applibrary/installationrequest)

#### Initializing an app installation request

- [init(alternativeDistributionPackageURL: URL, account: String, installVerificationToken: String)](/documentation/marketplacekit/applibrary/installationrequest/init(alternativedistributionpackageurl:account:installverificationtoken:))

#### Inspecting app installation information

- [var account: String](/documentation/marketplacekit/applibrary/installationrequest/account)
- [var alternativeDistributionPackageURL: URL](/documentation/marketplacekit/applibrary/installationrequest/alternativedistributionpackageurl)
- [var appShareURL: URL?](/documentation/marketplacekit/applibrary/installationrequest/appshareurl)
- [var installVerificationToken: String](/documentation/marketplacekit/applibrary/installationrequest/installverificationtoken)
- [var installingApps: Set<AppLibrary.App>](/documentation/marketplacekit/applibrary/installingapps)
- [var isLoading: Bool](/documentation/marketplacekit/applibrary/isloading)
- [func requestAppInstallation(AppLibrary.InstallationRequest) async throws](/documentation/marketplacekit/applibrary/requestappinstallation(_:))
- [func requestAppInstallationFromBrowser(for: URL, referrer: URL) async throws](/documentation/marketplacekit/applibrary/requestappinstallationfrombrowser(for:referrer:))

### Accessing installed apps

- [func app(forAppleItemID: AppleItemID) -> AppLibrary.App](/documentation/marketplacekit/applibrary/app(forappleitemid:))
- [var installedApps: Set<AppLibrary.App>](/documentation/marketplacekit/applibrary/installedapps)

### Checking for age-rating based content restrictions

- [var maximumAllowedAgeRating: Int](/documentation/marketplacekit/applibrary/maximumallowedagerating)
- [AppLibrary.ExceptionRequest](/documentation/marketplacekit/applibrary/exceptionrequest)

#### Identifying the requested app

- [let appleItemID: AppleItemID](/documentation/marketplacekit/applibrary/exceptionrequest/appleitemid)

#### Inspecting the request status

- [let status: AppLibrary.ExceptionRequest.Status](/documentation/marketplacekit/applibrary/exceptionrequest/status-swift.property)
- [AppLibrary.ExceptionRequest.Status](/documentation/marketplacekit/applibrary/exceptionrequest/status-swift.enum)

##### Determining the status

- [case approved](/documentation/marketplacekit/applibrary/exceptionrequest/status-swift.enum/approved)
- [case declined](/documentation/marketplacekit/applibrary/exceptionrequest/status-swift.enum/declined)
- [case pending](/documentation/marketplacekit/applibrary/exceptionrequest/status-swift.enum/pending)
- [func currentAgeExceptionRequests() async throws -> [AppLibrary.ExceptionRequest]](/documentation/marketplacekit/applibrary/currentageexceptionrequests())

### Filtering app searches

- [var searchTerritory: String?](/documentation/marketplacekit/applibrary/searchterritory)
- [func setSearchTerritory(String?) async](/documentation/marketplacekit/applibrary/setsearchterritory(_:))

### Updating apps

- [func requestAppUpdate(AppLibrary.InstallationRequest) async throws](/documentation/marketplacekit/applibrary/requestappupdate(_:))
- [func requestLicenseRenewal(appleItemIDs: [UInt64]) async throws](/documentation/marketplacekit/applibrary/requestlicenserenewal(appleitemids:))

### Determining device region

- [var catalogRegion: String?](/documentation/marketplacekit/applibrary/catalogregion)

### Deprecated

- [func requestAppInstallation(for: URL, account: String, installVerificationToken: String) async throws](/documentation/marketplacekit/applibrary/requestappinstallation(for:account:installverificationtoken:))
- [func requestAppUpdate(for: URL, account: String, installVerificationToken: String) async throws](/documentation/marketplacekit/applibrary/requestappupdate(for:account:installverificationtoken:))
- [AppVersion](/documentation/marketplacekit/appversion)

### Initializers

- [init(appleItemID: AppleItemID, appleVersionID: UInt64)](/documentation/marketplacekit/appversion/init(appleitemid:appleversionid:))

### Instance Properties

- [let appleItemID: AppleItemID](/documentation/marketplacekit/appversion/appleitemid)
- [let appleVersionID: UInt64](/documentation/marketplacekit/appversion/appleversionid)
- [AutomaticUpdate](/documentation/marketplacekit/automaticupdate)

### Initializers

- [init(appleItemID: AppleItemID, alternativeDistributionPackage: URL, account: String, installVerificationToken: String)](/documentation/marketplacekit/automaticupdate/init(appleitemid:alternativedistributionpackage:account:installverificationtoken:))

### Instance Properties

- [let account: String](/documentation/marketplacekit/automaticupdate/account)
- [let alternativeDistributionPackage: URL](/documentation/marketplacekit/automaticupdate/alternativedistributionpackage)
- [var appShareURL: URL?](/documentation/marketplacekit/automaticupdate/appshareurl)
- [let appleItemID: AppleItemID](/documentation/marketplacekit/automaticupdate/appleitemid)
- [let installVerificationToken: String](/documentation/marketplacekit/automaticupdate/installverificationtoken)
- [InstallRequirements](/documentation/marketplacekit/installrequirements)

### Initializers

- [init()](/documentation/marketplacekit/installrequirements/init())

### Instance Properties

- [var ageRatingRank: Int?](/documentation/marketplacekit/installrequirements/ageratingrank)
- [var expectedInstallSize: UInt64?](/documentation/marketplacekit/installrequirements/expectedinstallsize)
- [var minimumSystemVersion: String?](/documentation/marketplacekit/installrequirements/minimumsystemversion)
- [var requiredDeviceCapabilities: Set<String>?](/documentation/marketplacekit/installrequirements/requireddevicecapabilities)

### Instance Methods

- [func satisfiedByDevice() -> Bool](/documentation/marketplacekit/installrequirements/satisfiedbydevice())
- [AppleItemID](/documentation/marketplacekit/appleitemid)
- [AppleVersionID](/documentation/marketplacekit/appleversionid)
- [let MarketplaceKitURIScheme: String](/documentation/marketplacekit/marketplacekiturischeme)

## Background services

- [MarketplaceAppExtension](/documentation/marketplacekit/marketplaceappextension)

### Instance Methods

- [func additionalHeaders(for: URLRequest, account: String) async -> [String : String]](/documentation/marketplacekit/marketplaceappextension/additionalheaders(for:account:))
- [func automaticUpdates(for: [AppVersion]) async throws -> [AutomaticUpdate]](/documentation/marketplacekit/marketplaceappextension/automaticupdates(for:))
- [func availableAppVersions(forAppleItemIDs: [AppleItemID]) async -> [AppVersion]](/documentation/marketplacekit/marketplaceappextension/availableappversions(forappleitemids:))
- [func requestFailed(response: HTTPURLResponse) async -> Bool](/documentation/marketplacekit/marketplaceappextension/requestfailed(response:))

## App distribution UI

- [ActionButton](/documentation/marketplacekit/actionbutton)

### Initializers

- [init(action: ActionButton.Action)](/documentation/marketplacekit/actionbutton/init(action:))

### Instance Properties

- [let action: ActionButton.Action](/documentation/marketplacekit/actionbutton/action-swift.property)
- [var backgroundColor: UIColor?](/documentation/marketplacekit/actionbutton/backgroundcolor)
- [var borderColor: UIColor](/documentation/marketplacekit/actionbutton/bordercolor)
- [var borderWidth: CGFloat](/documentation/marketplacekit/actionbutton/borderwidth)
- [var cornerRadius: CGFloat](/documentation/marketplacekit/actionbutton/cornerradius)
- [var fontSize: CGFloat](/documentation/marketplacekit/actionbutton/fontsize)
- [var imageName: String?](/documentation/marketplacekit/actionbutton/imagename)
- [var imagePlacement: ActionButton.ButtonImagePlacement](/documentation/marketplacekit/actionbutton/imageplacement)
- [var isEnabled: Bool](/documentation/marketplacekit/actionbutton/isenabled)
- [var isHighlighted: Bool](/documentation/marketplacekit/actionbutton/ishighlighted)
- [var label: String](/documentation/marketplacekit/actionbutton/label)
- [var size: CGSize](/documentation/marketplacekit/actionbutton/size)
- [var tintColor: UIColor!](/documentation/marketplacekit/actionbutton/tintcolor)

### Enumerations

- [ActionButton.Action](/documentation/marketplacekit/actionbutton/action-swift.enum)

#### Enumeration Cases

- [case batchInstall(BatchInstallConfiguration)](/documentation/marketplacekit/actionbutton/action-swift.enum/batchinstall(_:))
- [case delete(AppleItemID)](/documentation/marketplacekit/actionbutton/action-swift.enum/delete(_:))
- [case install(InstallConfiguration)](/documentation/marketplacekit/actionbutton/action-swift.enum/install(_:))
- [case launch(AppleItemID)](/documentation/marketplacekit/actionbutton/action-swift.enum/launch(_:))
- [ActionButton.ButtonImagePlacement](/documentation/marketplacekit/actionbutton/buttonimageplacement)

#### Enumeration Cases

- [case bottom](/documentation/marketplacekit/actionbutton/buttonimageplacement/bottom)
- [case leading](/documentation/marketplacekit/actionbutton/buttonimageplacement/leading)
- [case top](/documentation/marketplacekit/actionbutton/buttonimageplacement/top)
- [case trailing](/documentation/marketplacekit/actionbutton/buttonimageplacement/trailing)
- [InstallMetadata](/documentation/marketplacekit/installmetadata)

### Initializing an install metadata instance

- [init(account: String, appleItemID: AppleItemID, alternativeDistributionPackage: URL, isUpdate: Bool)](/documentation/marketplacekit/installmetadata/init(account:appleitemid:alternativedistributionpackage:isupdate:))
- [init(account: String, appleItemID: AppleItemID, alternativeDistributionPackage: URL, isUpdate: Bool, appShareURL: URL?, requestAgeException: Bool)](/documentation/marketplacekit/installmetadata/init(account:appleitemid:alternativedistributionpackage:isupdate:appshareurl:requestageexception:))

### Inspecting app and account information

- [let appleItemID: AppleItemID](/documentation/marketplacekit/installmetadata/appleitemid)
- [let alternativeDistributionPackage: URL](/documentation/marketplacekit/installmetadata/alternativedistributionpackage)
- [var appShareURL: URL?](/documentation/marketplacekit/installmetadata/appshareurl)
- [let isUpdate: Bool](/documentation/marketplacekit/installmetadata/isupdate)
- [let account: String](/documentation/marketplacekit/installmetadata/account)

### Requesting an exception

- [var requestAgeException: Bool](/documentation/marketplacekit/installmetadata/requestageexception)
- [InstallConfiguration](/documentation/marketplacekit/installconfiguration)

### Initializers

- [init(install: InstallMetadata, confirmInstall: () async -> InstallConfirmationResult)](/documentation/marketplacekit/installconfiguration/init(install:confirminstall:))

### Instance Properties

- [let confirmInstall: () async -> InstallConfirmationResult](/documentation/marketplacekit/installconfiguration/confirminstall)
- [let install: InstallMetadata](/documentation/marketplacekit/installconfiguration/install)
- [InstallConfirmationResult](/documentation/marketplacekit/installconfirmationresult)

### Enumeration Cases

- [case cancel](/documentation/marketplacekit/installconfirmationresult/cancel)
- [case confirmed(installVerificationToken: String, authenticationContext: LAContext?)](/documentation/marketplacekit/installconfirmationresult/confirmed(installverificationtoken:authenticationcontext:))
- [BatchInstallConfiguration](/documentation/marketplacekit/batchinstallconfiguration)

### Initializers

- [init(installs: [InstallMetadata], confirmInstall: () async -> BatchInstallConfirmationResult)](/documentation/marketplacekit/batchinstallconfiguration/init(installs:confirminstall:))

### Instance Properties

- [let confirmInstall: () async -> BatchInstallConfirmationResult](/documentation/marketplacekit/batchinstallconfiguration/confirminstall)
- [let installs: [InstallMetadata]](/documentation/marketplacekit/batchinstallconfiguration/installs)
- [BatchInstallConfirmationResult](/documentation/marketplacekit/batchinstallconfirmationresult)

### Enumeration Cases

- [case cancel](/documentation/marketplacekit/batchinstallconfirmationresult/cancel)
- [case confirmed(installVerificationTokens: [AppleItemID : String], authenticationContext: LAContext?)](/documentation/marketplacekit/batchinstallconfirmationresult/confirmed(installverificationtokens:authenticationcontext:))
- [MarketplaceDisplayOption](/documentation/marketplacekit/marketplacedisplayoption)

### Enumeration Cases

- [case authentication(account: String)](/documentation/marketplacekit/marketplacedisplayoption/authentication(account:))
- [case productPage(appleItemID: AppleItemID, appleVersionID: AppleVersionID?)](/documentation/marketplacekit/marketplacedisplayoption/productpage(appleitemid:appleversionid:))
- [case searchResults(query: String)](/documentation/marketplacekit/marketplacedisplayoption/searchresults(query:))
- [MarketplaceSceneDelegate](/documentation/marketplacekit/marketplacescenedelegate)

### Instance Methods

- [func scene(UIWindowScene, askedToDisplay: MarketplaceDisplayOption)](/documentation/marketplacekit/marketplacescenedelegate/scene(_:askedtodisplay:))

## Installation sources

- [AppDistributor](/documentation/marketplacekit/appdistributor)

### Enumeration Cases

- [case appStore](/documentation/marketplacekit/appdistributor/appstore)
- [case marketplace(String)](/documentation/marketplacekit/appdistributor/marketplace(_:))
- [case other](/documentation/marketplacekit/appdistributor/other)
- [case testFlight](/documentation/marketplacekit/appdistributor/testflight)
- [case web](/documentation/marketplacekit/appdistributor/web)

### Type Properties

- [static var current: AppDistributor](/documentation/marketplacekit/appdistributor/current)

## Token and transaction reporting

- [Reporting transactions for the Core Technology Commission](/documentation/marketplacekit/reporting-transactions-for-core-technology-commission)
- [TransactionReporting](/documentation/marketplacekit/transactionreporting)

### Retrieving a token

- [static func token(for: TransactionReporting.TokenType) async throws -> String](/documentation/marketplacekit/transactionreporting/token(for:))

### Specifying the token type

- [TransactionReporting.TokenType](/documentation/marketplacekit/transactionreporting/tokentype)

#### Reporting transactions

- [static let coreTechnology: TransactionReporting.TokenType](/documentation/marketplacekit/transactionreporting/tokentype/coretechnology)

## Errors

- [MarketplaceKitError](/documentation/marketplacekit/marketplacekiterror)

### Device and platform compatibility errors

- [case minimumPlatformVersionNotSatisfied(String)](/documentation/marketplacekit/marketplacekiterror/minimumplatformversionnotsatisfied(_:))
- [case missingCapabilities([String])](/documentation/marketplacekit/marketplacekiterror/missingcapabilities(_:))
- [case noSupportedVariant](/documentation/marketplacekit/marketplacekiterror/nosupportedvariant)
- [case unsupportedPlatform](/documentation/marketplacekit/marketplacekiterror/unsupportedplatform)
- [case insufficientStorageSpace(Measurement<UnitInformationStorage>)](/documentation/marketplacekit/marketplacekiterror/insufficientstoragespace(_:))

### Installation and permission errors

- [case appNotInstalled](/documentation/marketplacekit/marketplacekiterror/appnotinstalled)
- [case installationOfMarketplaceDenied](/documentation/marketplacekit/marketplacekiterror/installationofmarketplacedenied)
- [case installationRestricted](/documentation/marketplacekit/marketplacekiterror/installationrestricted)
- [case mismatchedInstallType](/documentation/marketplacekit/marketplacekiterror/mismatchedinstalltype)
- [case missingInstallVerificationToken](/documentation/marketplacekit/marketplacekiterror/missinginstallverificationtoken)

### Content validation and security errors

- [case invalidAlternativeDistributionPackageSignature](/documentation/marketplacekit/marketplacekiterror/invalidalternativedistributionpackagesignature)
- [case invalidAlternativeDistributionPackageURL](/documentation/marketplacekit/marketplacekiterror/invalidalternativedistributionpackageurl)
- [case invalidLicense](/documentation/marketplacekit/marketplacekiterror/invalidlicense)
- [case invalidManifest](/documentation/marketplacekit/marketplacekiterror/invalidmanifest)
- [case invalidURL](/documentation/marketplacekit/marketplacekiterror/invalidurl)

### Age-rating errors

- [case ageRatingExceptionNotNeeded](/documentation/marketplacekit/marketplacekiterror/ageratingexceptionnotneeded)
- [case missingAgeRatingExceptionRequest](/documentation/marketplacekit/marketplacekiterror/missingageratingexceptionrequest)
- [case ratingRestricted](/documentation/marketplacekit/marketplacekiterror/ratingrestricted)

### System and network errors

- [case cancelled](/documentation/marketplacekit/marketplacekiterror/cancelled)
- [case featureUnavailable](/documentation/marketplacekit/marketplacekiterror/featureunavailable)
- [case networkError](/documentation/marketplacekit/marketplacekiterror/networkerror)
- [case oauthTokenError](/documentation/marketplacekit/marketplacekiterror/oauthtokenerror)
- [case unknown](/documentation/marketplacekit/marketplacekiterror/unknown)

## Region support

- [Participating in alternative distribution for specific regions](/documentation/marketplacekit/participating-in-alternative-distribution-for-specific-regions)

## Deprecations

- [MarketplaceExtension](/documentation/marketplacekit/marketplaceextension)

### Instance Methods

- [func additionalHeaders(for: URLRequest, account: String) -> [String : String]?](/documentation/marketplacekit/marketplaceextension/additionalheaders(for:account:))
- [func automaticUpdates(for: [AppVersion]) async throws -> [AutomaticUpdate]](/documentation/marketplacekit/marketplaceextension/automaticupdates(for:))
- [func availableAppVersions(forAppleItemIDs: [AppleItemID]) -> [AppVersion]?](/documentation/marketplacekit/marketplaceextension/availableappversions(forappleitemids:))
- [func requestFailed(with: HTTPURLResponse) -> Bool](/documentation/marketplacekit/marketplaceextension/requestfailed(with:))
- [MarketplaceExtensionConfiguration](/documentation/marketplacekit/marketplaceextensionconfiguration)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
