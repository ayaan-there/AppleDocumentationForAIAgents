# Managed App Distribution Documentation

Source: https://sosumi.ai/documentation/managedappdistribution

---
title: ManagedAppDistribution
source: https://developer.apple.com/documentation/managedappdistribution
timestamp: 2026-02-13T18:59:01.297Z
---

## Essentials

- [Fetching and displaying managed apps](/documentation/managedappdistribution/fetching-and-displaying-managed-apps)
- [ManagedApp](/documentation/managedappdistribution/managedapp)

### Obtaining general information

- [let name: String](/documentation/managedappdistribution/managedapp/name)
- [let subtitle: String?](/documentation/managedappdistribution/managedapp/subtitle)
- [let description: String?](/documentation/managedappdistribution/managedapp/description)
- [let fileSize: Measurement<UnitInformationStorage>?](/documentation/managedappdistribution/managedapp/filesize)
- [func iconURL(fitting: CGSize) -> URL?](/documentation/managedappdistribution/managedapp/iconurl(fitting:))
- [func screenshotURLs(fitting: CGSize) -> [URL]](/documentation/managedappdistribution/managedapp/screenshoturls(fitting:))

### Obtaining platform and requirement information

- [let platform: Platform](/documentation/managedappdistribution/managedapp/platform-swift.property)
- [let requirements: String?](/documentation/managedappdistribution/managedapp/requirements)
- [ManagedApp.Platform](/documentation/managedappdistribution/managedapp/platform-swift.struct)

#### Type Properties

- [static var iOS: ManagedApp.Platform](/documentation/managedappdistribution/managedapp/platform-swift.struct/ios)
- [static var macOS: ManagedApp.Platform](/documentation/managedappdistribution/managedapp/platform-swift.struct/macos)
- [static var visionOS: ManagedApp.Platform](/documentation/managedappdistribution/managedapp/platform-swift.struct/visionos)

### Obtaining supported languages

- [let languages: [Locale.Language]](/documentation/managedappdistribution/managedapp/languages)
- [let metadataLanguage: Locale.Language?](/documentation/managedappdistribution/managedapp/metadatalanguage)

### Obtaining seller information

- [let seller: String?](/documentation/managedappdistribution/managedapp/seller)
- [let developerWebsite: URL?](/documentation/managedappdistribution/managedapp/developerwebsite)

### Obtaining rating information

- [let genres: [String]](/documentation/managedappdistribution/managedapp/genres)
- [let contentRating: String?](/documentation/managedappdistribution/managedapp/contentrating)

### Obtaining privacy and copyright information

- [let privacyPolicy: URL?](/documentation/managedappdistribution/managedapp/privacypolicy)
- [let copyright: String?](/documentation/managedappdistribution/managedapp/copyright)
- [var licenseAgreement: URL?](/documentation/managedappdistribution/managedapp/licenseagreement)

### Obtaining version information

- [let version: String?](/documentation/managedappdistribution/managedapp/version)
- [let releaseNotes: String?](/documentation/managedappdistribution/managedapp/releasenotes)
- [let releaseDate: Date?](/documentation/managedappdistribution/managedapp/releasedate)
- [ManagedAppLibrary](/documentation/managedappdistribution/managedapplibrary)

### Obtaining library information

- [var availableApps: ManagedAppLibrary.ManagedApps](/documentation/managedappdistribution/managedapplibrary/availableapps)
- [ManagedAppLibrary.ManagedApps](/documentation/managedappdistribution/managedapplibrary/managedapps)

#### Obtaining managed apps

- [ManagedAppLibrary.ManagedApps.AsyncIterator](/documentation/managedappdistribution/managedapplibrary/managedapps/asynciterator)

##### Iterating

- [ManagedAppLibrary.ManagedApps.AsyncIterator.Element](/documentation/managedappdistribution/managedapplibrary/managedapps/asynciterator/element)
- [func next() async throws -> ManagedAppLibrary.ManagedApps.AsyncIterator.Element?](/documentation/managedappdistribution/managedapplibrary/managedapps/asynciterator/next())

##### Instance Methods

- [func next(isolation: isolated (any Actor)?) async throws(ManagedAppLibrary.ManagedApps.AsyncIterator.Failure) -> ManagedAppLibrary.ManagedApps.AsyncIterator.Element?](/documentation/managedappdistribution/managedapplibrary/managedapps/asynciterator/next(isolation:))
- [ManagedAppLibrary.ManagedApps.Element](/documentation/managedappdistribution/managedapplibrary/managedapps/element)
- [func makeAsyncIterator() -> ManagedAppLibrary.ManagedApps.AsyncIterator](/documentation/managedappdistribution/managedapplibrary/managedapps/makeasynciterator())
- [static let currentDistributor: ManagedAppLibrary](/documentation/managedappdistribution/managedapplibrary/currentdistributor)

## App information

- [Platform](/documentation/managedappdistribution/platform)

### Obtaining supported platforms

- [static var iOS: Platform](/documentation/managedappdistribution/platform/ios)
- [static var macOS: Platform](/documentation/managedappdistribution/platform/macos)

### Type Properties

- [static var visionOS: Platform](/documentation/managedappdistribution/platform/visionos)

## View creation

- [ManagedAppView](/documentation/managedappdistribution/managedappview)

### Creating a view

- [init(app: ManagedApp)](/documentation/managedappdistribution/managedappview/init(app:))
- [ManagedContentView](/documentation/managedappdistribution/managedcontentview)

### Creating views

- [init(primaryLabel: LocalizedStringKey, secondaryLabel: LocalizedStringKey, tertiaryLabel: LocalizedStringKey, quaternaryLabel: LocalizedStringKey, offerState: ManagedContentOfferState, offerAction: (ManagedContentOfferState) -> Void, icon: () -> Icon)](/documentation/managedappdistribution/managedcontentview/init(primarylabel:secondarylabel:tertiarylabel:quaternarylabel:offerstate:offeraction:icon:)-4blv1)
- [init(primaryLabel: any StringProtocol, secondaryLabel: any StringProtocol, tertiaryLabel: any StringProtocol, quaternaryLabel: any StringProtocol, offerState: ManagedContentOfferState, offerAction: (ManagedContentOfferState) -> Void, icon: () -> Icon)](/documentation/managedappdistribution/managedcontentview/init(primarylabel:secondarylabel:tertiarylabel:quaternarylabel:offerstate:offeraction:icon:)-8l3xw)
- [ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate)

### Creating states

- [static func custom(title: String) -> ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/custom(title:))
- [static func installing(progress: Double?) -> ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/installing(progress:))

### Determining installation status

- [static var installed: ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/installed)
- [static var notInstalled: ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/notinstalled)
- [static var neverInstalled: ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/neverinstalled)
- [static var noninteractive: ManagedContentOfferState](/documentation/managedappdistribution/managedcontentofferstate/noninteractive)
- [ManagedContentStyle](/documentation/managedappdistribution/managedcontentstyle)

### Determining styles

- [static var automatic: ManagedContentStyle](/documentation/managedappdistribution/managedcontentstyle/automatic)
- [static var compact: ManagedContentStyle](/documentation/managedappdistribution/managedcontentstyle/compact)
- [static var header: ManagedContentStyle](/documentation/managedappdistribution/managedcontentstyle/header)
- [static var vertical: ManagedContentStyle](/documentation/managedappdistribution/managedcontentstyle/vertical)

## Errors

- [ManagedAppDistributionError](/documentation/managedappdistribution/managedappdistributionerror)

### Inspecting errors

- [case deviceNotManaged](/documentation/managedappdistribution/managedappdistributionerror/devicenotmanaged)
- [case networkError](/documentation/managedappdistribution/managedappdistributionerror/networkerror)
- [case unrecoverableError](/documentation/managedappdistribution/managedappdistributionerror/unrecoverableerror)
- [case unsupportedPlatform](/documentation/managedappdistribution/managedappdistributionerror/unsupportedplatform)

### Providing error information

- [var description: String](/documentation/managedappdistribution/managedappdistributionerror/description)
- [var errorDescription: String?](/documentation/managedappdistribution/managedappdistributionerror/errordescription)
- [var failureReason: String?](/documentation/managedappdistribution/managedappdistributionerror/failurereason)
- [var recoveryOptions: [String]](/documentation/managedappdistribution/managedappdistributionerror/recoveryoptions)
- [var recoverySuggestion: String?](/documentation/managedappdistribution/managedappdistributionerror/recoverysuggestion)
- [var localizedStringResource: LocalizedStringResource](/documentation/managedappdistribution/managedappdistributionerror/localizedstringresource)

### Providing help information

- [var helpAnchor: String?](/documentation/managedappdistribution/managedappdistributionerror/helpanchor)

### Recovering from errors

- [func attemptRecovery(optionIndex: Int) -> Bool](/documentation/managedappdistribution/managedappdistributionerror/attemptrecovery(optionindex:))
- [func attemptRecovery(optionIndex: Int, resultHandler: (Bool) -> Void)](/documentation/managedappdistribution/managedappdistributionerror/attemptrecovery(optionindex:resulthandler:))

### Enumeration Cases

- [case appNotManaged](/documentation/managedappdistribution/managedappdistributionerror/appnotmanaged)
- [case licenseNotFound](/documentation/managedappdistribution/managedappdistributionerror/licensenotfound)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
