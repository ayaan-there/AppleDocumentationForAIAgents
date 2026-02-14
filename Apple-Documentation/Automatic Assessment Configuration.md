# Automatic Assessment Configuration Documentation

Source: https://sosumi.ai/documentation/automaticassessmentconfiguration

---
title: Automatic Assessment Configuration
source: https://developer.apple.com/documentation/automaticassessmentconfiguration
timestamp: 2026-02-13T18:54:09.901Z
---

## Essentials

- [com.apple.developer.automatic-assessment-configuration](/documentation/bundleresources/entitlements/com.apple.developer.automatic-assessment-configuration)

## Sessions

- [Preparing an educational assessment app for distribution](/documentation/automaticassessmentconfiguration/preparing-an-educational-assessment-app-for-distribution)
- [Build an Educational Assessment App](/documentation/automaticassessmentconfiguration/build-an-educational-assessment-app)
- [AEAssessmentConfiguration](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration)

### Allowing access to other apps

- [func setConfiguration(AEAssessmentParticipantConfiguration, for: AEAssessmentApplication)](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/setconfiguration(_:for:))
- [var configurationsByApplication: [AEAssessmentApplication : AEAssessmentParticipantConfiguration]](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/configurationsbyapplication)
- [func remove(AEAssessmentApplication)](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/remove(_:))
- [var mainParticipantConfiguration: AEAssessmentParticipantConfiguration](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/mainparticipantconfiguration)
- [AEAssessmentApplication](/documentation/automaticassessmentconfiguration/aeassessmentapplication)

#### Creating an assessment application

- [init(bundleIdentifier: String, teamIdentifier: String?)](/documentation/automaticassessmentconfiguration/aeassessmentapplication/init(bundleidentifier:teamidentifier:))
- [init(bundleIdentifier: String)](/documentation/automaticassessmentconfiguration/aeassessmentapplication/init(bundleidentifier:))
- [var bundleIdentifier: String](/documentation/automaticassessmentconfiguration/aeassessmentapplication/bundleidentifier)
- [var teamIdentifier: String?](/documentation/automaticassessmentconfiguration/aeassessmentapplication/teamidentifier)

#### Requiring code-signed apps

- [var requiresSignatureValidation: Bool](/documentation/automaticassessmentconfiguration/aeassessmentapplication/requiressignaturevalidation)
- [AEAssessmentParticipantConfiguration](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration)

#### Creating participant configuration instances

- [init()](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration/init())
- [class func new() -> Self](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration/new())

#### Allowing network access

- [var allowsNetworkAccess: Bool](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration/allowsnetworkaccess)

#### Instance Properties

- [var configurationInfo: [String : Any]](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration/configurationinfo)
- [var isRequired: Bool](/documentation/automaticassessmentconfiguration/aeassessmentparticipantconfiguration/isrequired)

### Allowing accessibility

- [var allowsAccessibilitySpeech: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsaccessibilityspeech)
- [var allowsDictation: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsdictation)

### Allowing typing assistance

- [var allowsContinuousPathKeyboard: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowscontinuouspathkeyboard)
- [var allowsKeyboardShortcuts: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowskeyboardshortcuts)
- [var allowsPredictiveKeyboard: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowspredictivekeyboard)
- [var allowsPasswordAutoFill: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowspasswordautofill)

### Allowing corrections

- [var allowsSpellCheck: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsspellcheck)
- [var autocorrectMode: AEAssessmentConfiguration.AutocorrectMode](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/autocorrectmode-swift.property)
- [AEAssessmentConfiguration.AutocorrectMode](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/autocorrectmode-swift.struct)

#### Creating a mode

- [init(rawValue: UInt)](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/autocorrectmode-swift.struct/init(rawvalue:))

#### Modes

- [static var punctuation: AEAssessmentConfiguration.AutocorrectMode](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/autocorrectmode-swift.struct/punctuation)
- [static var spelling: AEAssessmentConfiguration.AutocorrectMode](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/autocorrectmode-swift.struct/spelling)

### Allowing handoff

- [var allowsActivityContinuation: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsactivitycontinuation)

### Instance Properties

- [var allowsAccessibilityKeyboard: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsaccessibilitykeyboard)
- [var allowsAccessibilityLiveCaptions: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsaccessibilitylivecaptions)
- [var allowsAccessibilityReader: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsaccessibilityreader)
- [var allowsAccessibilityTypingFeedback: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsaccessibilitytypingfeedback)
- [var allowsScreenshots: Bool](/documentation/automaticassessmentconfiguration/aeassessmentconfiguration/allowsscreenshots)
- [AEAssessmentSession](/documentation/automaticassessmentconfiguration/aeassessmentsession)

### Creating a session

- [init(configuration: AEAssessmentConfiguration)](/documentation/automaticassessmentconfiguration/aeassessmentsession/init(configuration:))

### Managing session configuration

- [func update(to: AEAssessmentConfiguration)](/documentation/automaticassessmentconfiguration/aeassessmentsession/update(to:))
- [var configuration: AEAssessmentConfiguration](/documentation/automaticassessmentconfiguration/aeassessmentsession/configuration)
- [class var supportsMultipleParticipants: Bool](/documentation/automaticassessmentconfiguration/aeassessmentsession/supportsmultipleparticipants)
- [class var supportsConfigurationUpdates: Bool](/documentation/automaticassessmentconfiguration/aeassessmentsession/supportsconfigurationupdates)

### Responding to session updates

- [var delegate: (any AEAssessmentSessionDelegate)?](/documentation/automaticassessmentconfiguration/aeassessmentsession/delegate)
- [AEAssessmentSessionDelegate](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate)

#### Responding to session start and stop

- [func assessmentSessionDidBegin(AEAssessmentSession)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsessiondidbegin(_:))
- [func assessmentSession(AEAssessmentSession, failedToBeginWithError: any Error)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsession(_:failedtobeginwitherror:))
- [func assessmentSession(AEAssessmentSession, wasInterruptedWithError: any Error)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsession(_:wasinterruptedwitherror:))
- [func assessmentSessionDidEnd(AEAssessmentSession)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsessiondidend(_:))

#### Responding to configuration changes

- [func assessmentSessionDidUpdate(AEAssessmentSession)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsessiondidupdate(_:))
- [func assessmentSession(AEAssessmentSession, failedToUpdateTo: AEAssessmentConfiguration, error: any Error)](/documentation/automaticassessmentconfiguration/aeassessmentsessiondelegate/assessmentsession(_:failedtoupdateto:error:))

### Starting and stopping a session

- [func begin()](/documentation/automaticassessmentconfiguration/aeassessmentsession/begin())
- [func end()](/documentation/automaticassessmentconfiguration/aeassessmentsession/end())
- [var isActive: Bool](/documentation/automaticassessmentconfiguration/aeassessmentsession/isactive)

## Errors

- [AEAssessmentError](/documentation/automaticassessmentconfiguration/aeassessmenterror)

### Error codes

- [static var unknown: AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/unknown)
- [static var unsupportedPlatform: AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/unsupportedplatform)
- [AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/code)

#### Possible errors

- [case configurationUpdatesNotSupported](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/configurationupdatesnotsupported)
- [case multipleParticipantsNotSupported](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/multipleparticipantsnotsupported)
- [case unknown](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/unknown)
- [case unsupportedPlatform](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/unsupportedplatform)

#### Enumeration Cases

- [case requiredParticipantsNotAvailable](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/requiredparticipantsnotavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/init(rawvalue:))

### Error characteristics

- [let AEAssessmentErrorDomain: String](/documentation/automaticassessmentconfiguration/aeassessmenterrordomain)

### Instance Properties

- [var notInstalledParticipants: [String]?](/documentation/automaticassessmentconfiguration/aeassessmenterror/notinstalledparticipants)
- [var restrictedSystemParticipants: [String]?](/documentation/automaticassessmentconfiguration/aeassessmenterror/restrictedsystemparticipants)

### Type Properties

- [static var configurationUpdatesNotSupported: AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/configurationupdatesnotsupported)
- [static var errorDomain: String](/documentation/automaticassessmentconfiguration/aeassessmenterror/errordomain)
- [static var multipleParticipantsNotSupported: AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/multipleparticipantsnotsupported)
- [static var requiredParticipantsNotAvailable: AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/requiredparticipantsnotavailable)
- [AEAssessmentError.Code](/documentation/automaticassessmentconfiguration/aeassessmenterror/code)

### Possible errors

- [case configurationUpdatesNotSupported](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/configurationupdatesnotsupported)
- [case multipleParticipantsNotSupported](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/multipleparticipantsnotsupported)
- [case unknown](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/unknown)
- [case unsupportedPlatform](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/unsupportedplatform)

### Enumeration Cases

- [case requiredParticipantsNotAvailable](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/requiredparticipantsnotavailable)

### Initializers

- [init?(rawValue: Int)](/documentation/automaticassessmentconfiguration/aeassessmenterror/code/init(rawvalue:))
- [let AEAssessmentErrorDomain: String](/documentation/automaticassessmentconfiguration/aeassessmenterrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
