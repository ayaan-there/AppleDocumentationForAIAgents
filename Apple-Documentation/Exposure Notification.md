# Exposure Notification Documentation

Source: https://sosumi.ai/documentation/exposurenotification

---
title: Exposure Notification
source: https://developer.apple.com/documentation/exposurenotification
timestamp: 2026-02-13T18:56:46.244Z
---

## Essentials

- [Supporting Exposure Notifications Express](/documentation/exposurenotification/supporting-exposure-notifications-express)

### Server Configuration

- [Setting Up an Exposure Notifications Express Test Verification Server](/documentation/exposurenotification/setting-up-an-exposure-notifications-express-test-verification-server)
- [Configuring a Key Server for Exposure Notifications Express](/documentation/exposurenotification/configuring-a-key-server-for-exposure-notifications-express)
- [Building an App to Notify Users of COVID-19 Exposure](/documentation/exposurenotification/building-an-app-to-notify-users-of-covid-19-exposure)
- [Setting Up a Key Server](/documentation/exposurenotification/setting-up-a-key-server)
- [ENManager](/documentation/exposurenotification/enmanager)

### Activating the Manager

- [func activate(completionHandler: ((any Error)?) -> Void)](/documentation/exposurenotification/enmanager/activate(completionhandler:))
- [var activityHandler: ENActivityHandler?](/documentation/exposurenotification/enmanager/activityhandler)
- [ENActivityHandler](/documentation/exposurenotification/enactivityhandler)
- [ENActivityFlags](/documentation/exposurenotification/enactivityflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/exposurenotification/enactivityflags/init(rawvalue:))

#### Type Properties

- [static var periodicRun: ENActivityFlags](/documentation/exposurenotification/enactivityflags/periodicrun)
- [static var preAuthorizedKeyReleaseNotificationTapped: ENActivityFlags](/documentation/exposurenotification/enactivityflags/preauthorizedkeyreleasenotificationtapped)
- [static var reserved1: ENActivityFlags](/documentation/exposurenotification/enactivityflags/reserved1)
- [static var reserved2: ENActivityFlags](/documentation/exposurenotification/enactivityflags/reserved2)
- [func setExposureNotificationEnabled(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/exposurenotification/enmanager/setexposurenotificationenabled(_:completionhandler:))

### Obtaining Exposure Information

- [func detectExposures(configuration: ENExposureConfiguration, diagnosisKeyURLs: [URL], completionHandler: ENDetectExposuresHandler) -> Progress](/documentation/exposurenotification/enmanager/detectexposures(configuration:diagnosiskeyurls:completionhandler:))

#### Completion Handlers

- [ENDetectExposuresHandler](/documentation/exposurenotification/endetectexposureshandler)
- [func detectExposures(configuration: ENExposureConfiguration, completionHandler: ENDetectExposuresHandler) -> Progress](/documentation/exposurenotification/enmanager/detectexposures(configuration:completionhandler:))
- [func getExposureWindows(summary: ENExposureDetectionSummary, completionHandler: ENGetExposureWindowsHandler) -> Progress](/documentation/exposurenotification/enmanager/getexposurewindows(summary:completionhandler:))
- [ENGetExposureWindowsHandler](/documentation/exposurenotification/engetexposurewindowshandler)
- [func getUserTraveled(completionHandler: (Bool, (any Error)?) -> Void)](/documentation/exposurenotification/enmanager/getusertraveled(completionhandler:))
- [ENGetUserTraveledHandler](/documentation/exposurenotification/engetusertraveledhandler)
- [func getExposureInfo(summary: ENExposureDetectionSummary, userExplanation: String, completionHandler: ENGetExposureInfoHandler) -> Progress](/documentation/exposurenotification/enmanager/getexposureinfo(summary:userexplanation:completionhandler:))

#### Completion Handlers

- [ENGetExposureInfoHandler](/documentation/exposurenotification/engetexposureinfohandler)

### Obtaining Exposure Keys

- [func getDiagnosisKeys(completionHandler: ([ENTemporaryExposureKey]?, (any Error)?) -> Void)](/documentation/exposurenotification/enmanager/getdiagnosiskeys(completionhandler:))

#### Completion Handlers

- [ENGetDiagnosisKeysHandler](/documentation/exposurenotification/engetdiagnosiskeyshandler)
- [func getTestDiagnosisKeys(completionHandler: ([ENTemporaryExposureKey]?, (any Error)?) -> Void)](/documentation/exposurenotification/enmanager/gettestdiagnosiskeys(completionhandler:))
- [ENTemporaryExposureKey](/documentation/exposurenotification/entemporaryexposurekey)

#### Exposure Criteria

- [var transmissionRiskLevel: ENRiskLevel](/documentation/exposurenotification/entemporaryexposurekey/transmissionrisklevel)
- [var rollingPeriod: ENIntervalNumber](/documentation/exposurenotification/entemporaryexposurekey/rollingperiod)
- [var keyData: Data](/documentation/exposurenotification/entemporaryexposurekey/keydata)
- [var rollingStartNumber: ENIntervalNumber](/documentation/exposurenotification/entemporaryexposurekey/rollingstartnumber)
- [ENIntervalNumber](/documentation/exposurenotification/enintervalnumber)

### Configuring the Manager

- [var exposureNotificationStatus: ENStatus](/documentation/exposurenotification/enmanager/exposurenotificationstatus)
- [var exposureNotificationEnabled: Bool](/documentation/exposurenotification/enmanager/exposurenotificationenabled)
- [class var authorizationStatus: ENAuthorizationStatus](/documentation/exposurenotification/enmanager/authorizationstatus)
- [var dispatchQueue: dispatch_queue_t](/documentation/exposurenotification/enmanager/dispatchqueue)

### Preauthorizing Exposure Keys

- [func requestPreAuthorizedDiagnosisKeys(completionHandler: ((any Error)?) -> Void)](/documentation/exposurenotification/enmanager/requestpreauthorizeddiagnosiskeys(completionhandler:))
- [func preAuthorizeDiagnosisKeys(completionHandler: ((any Error)?) -> Void)](/documentation/exposurenotification/enmanager/preauthorizediagnosiskeys(completionhandler:))
- [ENDiagnosisKeysAvailableHandler](/documentation/exposurenotification/endiagnosiskeysavailablehandler)
- [var diagnosisKeysAvailableHandler: ENDiagnosisKeysAvailableHandler?](/documentation/exposurenotification/enmanager/diagnosiskeysavailablehandler)

### Invalidating the Manager

- [func invalidate()](/documentation/exposurenotification/enmanager/invalidate())

#### Completion Handlers

- [var invalidationHandler: (() -> Void)?](/documentation/exposurenotification/enmanager/invalidationhandler)

### Instance Properties

- [var invalidationHandler: (() -> Void)?](/documentation/exposurenotification/enmanager/invalidationhandler)
- [ENDeveloperRegion](/documentation/bundleresources/information-property-list/endeveloperregion)
- [ENAPIVersion](/documentation/bundleresources/information-property-list/enapiversion)
- [Changing Configuration Values Using the Server‑to‑Server API](/documentation/exposurenotification/changing-configuration-values-using-the-server-to-server-api)
- [Testing Exposure Notifications Apps in iOS 13.7 and Later](/documentation/exposurenotification/testing-exposure-notifications-apps-in-ios-13-7-and-later)
- [Supporting Exposure Notifications in iOS 12.5](/documentation/exposurenotification/supporting-exposure-notifications-in-ios-12-5)

## Exposures

- [Configuring Exposure Notifications](/documentation/exposurenotification/configuring-exposure-notifications)
- [ENExposureConfiguration](/documentation/exposurenotification/enexposureconfiguration)

### Configuring Duration

- [var attenuationDurationThresholds: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/attenuationdurationthresholds)
- [var immediateDurationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/immediatedurationweight)
- [var mediumDurationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/mediumdurationweight)
- [var nearDurationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/neardurationweight)
- [var otherDurationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/otherdurationweight)
- [var daysSinceLastExposureThreshold: Int](/documentation/exposurenotification/enexposureconfiguration/dayssincelastexposurethreshold)

### Configuring Infectiousness

- [var infectiousnessForDaysSinceOnsetOfSymptoms: [NSNumber : NSNumber]?](/documentation/exposurenotification/enexposureconfiguration/infectiousnessfordayssinceonsetofsymptoms)
- [var infectiousnessHighWeight: Double](/documentation/exposurenotification/enexposureconfiguration/infectiousnesshighweight)
- [var infectiousnessStandardWeight: Double](/documentation/exposurenotification/enexposureconfiguration/infectiousnessstandardweight)
- [let ENDaysSinceOnsetOfSymptomsUnknown: Int](/documentation/exposurenotification/endayssinceonsetofsymptomsunknown)

### Configuring Report Types

- [var reportTypeConfirmedClinicalDiagnosisWeight: Double](/documentation/exposurenotification/enexposureconfiguration/reporttypeconfirmedclinicaldiagnosisweight)
- [var reportTypeConfirmedTestWeight: Double](/documentation/exposurenotification/enexposureconfiguration/reporttypeconfirmedtestweight)
- [var reportTypeRecursiveWeight: Double](/documentation/exposurenotification/enexposureconfiguration/reporttyperecursiveweight)
- [var reportTypeSelfReportedWeight: Double](/documentation/exposurenotification/enexposureconfiguration/reporttypeselfreportedweight)
- [var reportTypeNoneMap: ENDiagnosisReportType](/documentation/exposurenotification/enexposureconfiguration/reporttypenonemap)

### Determining Exposure Risk Level in Version 1

- [Exposure Risk Value Calculation in ExposureNotification Version 1](/documentation/exposurenotification/exposure-risk-value-calculation-in-exposurenotification-version-1)

#### Exposure Information

- [ENExposureInfo](/documentation/exposurenotification/enexposureinfo)

##### Exposure Criteria

- [var attenuationDurations: [NSNumber]](/documentation/exposurenotification/enexposureinfo/attenuationdurations)
- [var attenuationValue: ENAttenuation](/documentation/exposurenotification/enexposureinfo/attenuationvalue)
- [var date: Date](/documentation/exposurenotification/enexposureinfo/date)
- [var duration: TimeInterval](/documentation/exposurenotification/enexposureinfo/duration)
- [var totalRiskScore: ENRiskScore](/documentation/exposurenotification/enexposureinfo/totalriskscore)
- [var totalRiskScoreFullRange: Double](/documentation/exposurenotification/enexposureinfo/totalriskscorefullrange)
- [var transmissionRiskLevel: ENRiskLevel](/documentation/exposurenotification/enexposureinfo/transmissionrisklevel)
- [ENAttenuation](/documentation/exposurenotification/enattenuation)
- [var metadata: [AnyHashable : Any]?](/documentation/exposurenotification/enexposureinfo/metadata)
- [var daysSinceOnsetOfSymptoms: Int](/documentation/exposurenotification/enexposureinfo/dayssinceonsetofsymptoms)
- [var diagnosisReportType: ENDiagnosisReportType](/documentation/exposurenotification/enexposureinfo/diagnosisreporttype)
- [let ENDaysSinceOnsetOfSymptomsUnknown: Int](/documentation/exposurenotification/endayssinceonsetofsymptomsunknown)
- [ENRiskScore](/documentation/exposurenotification/enriskscore)
- [ENRiskLevel](/documentation/exposurenotification/enrisklevel)
- [ENRiskLevelValue](/documentation/exposurenotification/enrisklevelvalue)

#### Level Configuration

- [var attenuationDurationThresholds: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/attenuationdurationthresholds)
- [var attenuationLevelValues: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/attenuationlevelvalues)
- [var daysSinceLastExposureLevelValues: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/dayssincelastexposurelevelvalues)
- [var durationLevelValues: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/durationlevelvalues)
- [var transmissionRiskLevelValues: [NSNumber]](/documentation/exposurenotification/enexposureconfiguration/transmissionrisklevelvalues)
- [var metadata: [AnyHashable : Any]?](/documentation/exposurenotification/enexposureconfiguration/metadata)

#### Minimum Threshold Configuration

- [var minimumRiskScore: ENRiskScore](/documentation/exposurenotification/enexposureconfiguration/minimumriskscore)
- [var minimumRiskScoreFullRange: Double](/documentation/exposurenotification/enexposureconfiguration/minimumriskscorefullrange)

#### Weight Configuration

- [var attenuationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/attenuationweight)
- [var daysSinceLastExposureWeight: Double](/documentation/exposurenotification/enexposureconfiguration/dayssincelastexposureweight)
- [var durationWeight: Double](/documentation/exposurenotification/enexposureconfiguration/durationweight)
- [var transmissionRiskWeight: Double](/documentation/exposurenotification/enexposureconfiguration/transmissionriskweight)
- [ENExposureWindow](/documentation/exposurenotification/enexposurewindow)

### Getting Window Properties

- [var calibrationConfidence: ENCalibrationConfidence](/documentation/exposurenotification/enexposurewindow/calibrationconfidence)
- [var date: Date](/documentation/exposurenotification/enexposurewindow/date)
- [var diagnosisReportType: ENDiagnosisReportType](/documentation/exposurenotification/enexposurewindow/diagnosisreporttype)
- [var infectiousness: ENInfectiousness](/documentation/exposurenotification/enexposurewindow/infectiousness)
- [var scanInstances: [ENScanInstance]](/documentation/exposurenotification/enexposurewindow/scaninstances)
- [var variantOfConcernType: ENVariantOfConcernType](/documentation/exposurenotification/enexposurewindow/variantofconcerntype)
- [ENVariantOfConcernType](/documentation/exposurenotification/envariantofconcerntype)

#### User-Defined Types

- [case type1](/documentation/exposurenotification/envariantofconcerntype/type1)
- [case type2](/documentation/exposurenotification/envariantofconcerntype/type2)
- [case type3](/documentation/exposurenotification/envariantofconcerntype/type3)
- [case type4](/documentation/exposurenotification/envariantofconcerntype/type4)
- [case typeUnknown](/documentation/exposurenotification/envariantofconcerntype/typeunknown)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/exposurenotification/envariantofconcerntype/init(rawvalue:))
- [ENScanInstance](/documentation/exposurenotification/enscaninstance)

### Getting Scan Instance Properties

- [var minimumAttenuation: ENAttenuation](/documentation/exposurenotification/enscaninstance/minimumattenuation)
- [var secondsSinceLastScan: Int](/documentation/exposurenotification/enscaninstance/secondssincelastscan)
- [var typicalAttenuation: ENAttenuation](/documentation/exposurenotification/enscaninstance/typicalattenuation)
- [Exposure Parameter Limits](/documentation/exposurenotification/exposure-parameter-limits)

### Enumerations

- [Attenuation](/documentation/exposurenotification/attenuation)

#### Constants

- [var ENAttenuationMax: Int](/documentation/exposurenotification/enattenuationmax)
- [var ENAttenuationMin: Int](/documentation/exposurenotification/enattenuationmin)
- [Risk Level](/documentation/exposurenotification/risk-level)

#### Constants

- [var ENRiskLevelMin: Int](/documentation/exposurenotification/enrisklevelmin)
- [var ENRiskLevelMax: Int](/documentation/exposurenotification/enrisklevelmax)
- [Risk Level Value](/documentation/exposurenotification/risk-level-value)

#### Constants

- [var ENRiskLevelValueMin: Int](/documentation/exposurenotification/enrisklevelvaluemin)
- [var ENRiskLevelValueMax: Int](/documentation/exposurenotification/enrisklevelvaluemax)
- [Risk Score](/documentation/exposurenotification/risk-score)

#### Constants

- [var ENRiskScoreMin: Int](/documentation/exposurenotification/enriskscoremin)
- [var ENRiskScoreMax: Int](/documentation/exposurenotification/enriskscoremax)
- [Risk Weight](/documentation/exposurenotification/risk-weight)

#### Constants

- [var ENRiskWeightMin: Int](/documentation/exposurenotification/enriskweightmin)
- [var ENRiskWeightMax: Int](/documentation/exposurenotification/enriskweightmax)
- [var ENRiskWeightDefault: Int](/documentation/exposurenotification/enriskweightdefault)
- [ENActivityFlags](/documentation/exposurenotification/enactivityflags)

#### Initializers

- [init(rawValue: UInt32)](/documentation/exposurenotification/enactivityflags/init(rawvalue:))

#### Type Properties

- [static var periodicRun: ENActivityFlags](/documentation/exposurenotification/enactivityflags/periodicrun)
- [static var preAuthorizedKeyReleaseNotificationTapped: ENActivityFlags](/documentation/exposurenotification/enactivityflags/preauthorizedkeyreleasenotificationtapped)
- [static var reserved1: ENActivityFlags](/documentation/exposurenotification/enactivityflags/reserved1)
- [static var reserved2: ENActivityFlags](/documentation/exposurenotification/enactivityflags/reserved2)
- [ENCalibrationConfidence](/documentation/exposurenotification/encalibrationconfidence)

#### Enumeration Cases

- [case high](/documentation/exposurenotification/encalibrationconfidence/high)
- [case medium](/documentation/exposurenotification/encalibrationconfidence/medium)
- [case low](/documentation/exposurenotification/encalibrationconfidence/low)
- [case lowest](/documentation/exposurenotification/encalibrationconfidence/lowest)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/exposurenotification/encalibrationconfidence/init(rawvalue:))
- [ENDiagnosisReportType](/documentation/exposurenotification/endiagnosisreporttype)

#### Enumeration Cases

- [case confirmedClinicalDiagnosis](/documentation/exposurenotification/endiagnosisreporttype/confirmedclinicaldiagnosis)
- [case confirmedTest](/documentation/exposurenotification/endiagnosisreporttype/confirmedtest)
- [case recursive](/documentation/exposurenotification/endiagnosisreporttype/recursive)
- [case revoked](/documentation/exposurenotification/endiagnosisreporttype/revoked)
- [case selfReported](/documentation/exposurenotification/endiagnosisreporttype/selfreported)
- [case unknown](/documentation/exposurenotification/endiagnosisreporttype/unknown)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/exposurenotification/endiagnosisreporttype/init(rawvalue:))
- [ENInfectiousness](/documentation/exposurenotification/eninfectiousness)

#### Enumeration Cases

- [case high](/documentation/exposurenotification/eninfectiousness/high)
- [case none](/documentation/exposurenotification/eninfectiousness/none)
- [case standard](/documentation/exposurenotification/eninfectiousness/standard)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/exposurenotification/eninfectiousness/init(rawvalue:))

## Summaries

- [ENExposureDetectionSummary](/documentation/exposurenotification/enexposuredetectionsummary)

### Exposure Criteria

- [var attenuationDurations: [NSNumber]](/documentation/exposurenotification/enexposuredetectionsummary/attenuationdurations)
- [var daysSinceLastExposure: Int](/documentation/exposurenotification/enexposuredetectionsummary/dayssincelastexposure)
- [var matchedKeyCount: UInt64](/documentation/exposurenotification/enexposuredetectionsummary/matchedkeycount)
- [var maximumRiskScore: ENRiskScore](/documentation/exposurenotification/enexposuredetectionsummary/maximumriskscore)
- [var maximumRiskScoreFullRange: Double](/documentation/exposurenotification/enexposuredetectionsummary/maximumriskscorefullrange)
- [var riskScoreSumFullRange: Double](/documentation/exposurenotification/enexposuredetectionsummary/riskscoresumfullrange)
- [var metadata: [AnyHashable : Any]?](/documentation/exposurenotification/enexposuredetectionsummary/metadata)
- [var daySummaries: [ENExposureDaySummary]](/documentation/exposurenotification/enexposuredetectionsummary/daysummaries)
- [ENExposureDaySummary](/documentation/exposurenotification/enexposuredaysummary)

### Getting Exposure Summary Information

- [var date: Date](/documentation/exposurenotification/enexposuredaysummary/date)
- [var confirmedClinicalDiagnosisSummary: ENExposureSummaryItem?](/documentation/exposurenotification/enexposuredaysummary/confirmedclinicaldiagnosissummary)
- [var confirmedTestSummary: ENExposureSummaryItem?](/documentation/exposurenotification/enexposuredaysummary/confirmedtestsummary)
- [var recursiveSummary: ENExposureSummaryItem?](/documentation/exposurenotification/enexposuredaysummary/recursivesummary)
- [var selfReportedSummary: ENExposureSummaryItem?](/documentation/exposurenotification/enexposuredaysummary/selfreportedsummary)
- [var daySummary: ENExposureSummaryItem](/documentation/exposurenotification/enexposuredaysummary/daysummary)
- [ENExposureSummaryItem](/documentation/exposurenotification/enexposuresummaryitem)

### Getting Summary Properties

- [var maximumScore: Double](/documentation/exposurenotification/enexposuresummaryitem/maximumscore)
- [var scoreSum: Double](/documentation/exposurenotification/enexposuresummaryitem/scoresum)
- [var weightedDurationSum: TimeInterval](/documentation/exposurenotification/enexposuresummaryitem/weighteddurationsum)

## Status

- [ENAuthorizationStatus](/documentation/exposurenotification/enauthorizationstatus)

### Authorization States

- [case authorized](/documentation/exposurenotification/enauthorizationstatus/authorized)
- [case notAuthorized](/documentation/exposurenotification/enauthorizationstatus/notauthorized)
- [case restricted](/documentation/exposurenotification/enauthorizationstatus/restricted)
- [case unknown](/documentation/exposurenotification/enauthorizationstatus/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/exposurenotification/enauthorizationstatus/init(rawvalue:))
- [ENStatus](/documentation/exposurenotification/enstatus)

### States

- [case active](/documentation/exposurenotification/enstatus/active)
- [case bluetoothOff](/documentation/exposurenotification/enstatus/bluetoothoff)
- [case disabled](/documentation/exposurenotification/enstatus/disabled)
- [case restricted](/documentation/exposurenotification/enstatus/restricted)
- [case unknown](/documentation/exposurenotification/enstatus/unknown)
- [case paused](/documentation/exposurenotification/enstatus/paused)
- [case unauthorized](/documentation/exposurenotification/enstatus/unauthorized)

### Initializers

- [init?(rawValue: Int)](/documentation/exposurenotification/enstatus/init(rawvalue:))

## Errors

- [ENError](/documentation/exposurenotification/enerror)

### Error Codes

- [static var apiMisuse: ENError.Code](/documentation/exposurenotification/enerror/apimisuse)
- [static var badFormat: ENError.Code](/documentation/exposurenotification/enerror/badformat)
- [static var badParameter: ENError.Code](/documentation/exposurenotification/enerror/badparameter)
- [static var bluetoothOff: ENError.Code](/documentation/exposurenotification/enerror/bluetoothoff)
- [static var insufficientMemory: ENError.Code](/documentation/exposurenotification/enerror/insufficientmemory)
- [static var insufficientStorage: ENError.Code](/documentation/exposurenotification/enerror/insufficientstorage)
- [static var `internal`: ENError.Code](/documentation/exposurenotification/enerror/internal)
- [static var invalidated: ENError.Code](/documentation/exposurenotification/enerror/invalidated)
- [static var notAuthorized: ENError.Code](/documentation/exposurenotification/enerror/notauthorized)
- [static var notEnabled: ENError.Code](/documentation/exposurenotification/enerror/notenabled)
- [static var notEntitled: ENError.Code](/documentation/exposurenotification/enerror/notentitled)
- [static var rateLimited: ENError.Code](/documentation/exposurenotification/enerror/ratelimited)
- [static var restricted: ENError.Code](/documentation/exposurenotification/enerror/restricted)
- [static var unknown: ENError.Code](/documentation/exposurenotification/enerror/unknown)
- [static var unsupported: ENError.Code](/documentation/exposurenotification/enerror/unsupported)
- [static var dataInaccessible: ENError.Code](/documentation/exposurenotification/enerror/datainaccessible)
- [static var travelStatusNotAvailable: ENError.Code](/documentation/exposurenotification/enerror/travelstatusnotavailable)
- [ENError.Code](/documentation/exposurenotification/enerror/code)

#### Error Codes

- [case apiMisuse](/documentation/exposurenotification/enerror/code/apimisuse)
- [case badFormat](/documentation/exposurenotification/enerror/code/badformat)
- [case badParameter](/documentation/exposurenotification/enerror/code/badparameter)
- [case restricted](/documentation/exposurenotification/enerror/code/restricted)
- [case bluetoothOff](/documentation/exposurenotification/enerror/code/bluetoothoff)
- [case insufficientMemory](/documentation/exposurenotification/enerror/code/insufficientmemory)
- [case insufficientStorage](/documentation/exposurenotification/enerror/code/insufficientstorage)
- [case `internal`](/documentation/exposurenotification/enerror/code/internal)
- [case invalidated](/documentation/exposurenotification/enerror/code/invalidated)
- [case notAuthorized](/documentation/exposurenotification/enerror/code/notauthorized)
- [case notEnabled](/documentation/exposurenotification/enerror/code/notenabled)
- [case notEntitled](/documentation/exposurenotification/enerror/code/notentitled)
- [case rateLimited](/documentation/exposurenotification/enerror/code/ratelimited)
- [case unknown](/documentation/exposurenotification/enerror/code/unknown)
- [case unsupported](/documentation/exposurenotification/enerror/code/unsupported)
- [case dataInaccessible](/documentation/exposurenotification/enerror/code/datainaccessible)
- [case travelStatusNotAvailable](/documentation/exposurenotification/enerror/code/travelstatusnotavailable)

#### Initializers

- [init?(rawValue: Int)](/documentation/exposurenotification/enerror/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/exposurenotification/enerror/errordomain)
- [ENError.Code](/documentation/exposurenotification/enerror/code)

### Error Codes

- [case apiMisuse](/documentation/exposurenotification/enerror/code/apimisuse)
- [case badFormat](/documentation/exposurenotification/enerror/code/badformat)
- [case badParameter](/documentation/exposurenotification/enerror/code/badparameter)
- [case restricted](/documentation/exposurenotification/enerror/code/restricted)
- [case bluetoothOff](/documentation/exposurenotification/enerror/code/bluetoothoff)
- [case insufficientMemory](/documentation/exposurenotification/enerror/code/insufficientmemory)
- [case insufficientStorage](/documentation/exposurenotification/enerror/code/insufficientstorage)
- [case `internal`](/documentation/exposurenotification/enerror/code/internal)
- [case invalidated](/documentation/exposurenotification/enerror/code/invalidated)
- [case notAuthorized](/documentation/exposurenotification/enerror/code/notauthorized)
- [case notEnabled](/documentation/exposurenotification/enerror/code/notenabled)
- [case notEntitled](/documentation/exposurenotification/enerror/code/notentitled)
- [case rateLimited](/documentation/exposurenotification/enerror/code/ratelimited)
- [case unknown](/documentation/exposurenotification/enerror/code/unknown)
- [case unsupported](/documentation/exposurenotification/enerror/code/unsupported)
- [case dataInaccessible](/documentation/exposurenotification/enerror/code/datainaccessible)
- [case travelStatusNotAvailable](/documentation/exposurenotification/enerror/code/travelstatusnotavailable)

### Initializers

- [init?(rawValue: Int)](/documentation/exposurenotification/enerror/code/init(rawvalue:))
- [let ENErrorDomain: String](/documentation/exposurenotification/enerrordomain)
- [ENErrorHandler](/documentation/exposurenotification/enerrorhandler)

## Variables

- [var ENRiskWeightDefaultV2: Int](/documentation/exposurenotification/enriskweightdefaultv2)
- [var ENRiskWeightMaxV2: Int](/documentation/exposurenotification/enriskweightmaxv2)
- [var EN_FEATURE_GENERAL: Int32](/documentation/exposurenotification/en_feature_general)

## Type Aliases

- [ENDetectExposuresHandler](/documentation/exposurenotification/endetectexposureshandler)
- [ENErrorOutType](/documentation/exposurenotification/enerrorouttype)
- [ENGetDiagnosisKeysHandler](/documentation/exposurenotification/engetdiagnosiskeyshandler)
- [ENGetExposureInfoHandler](/documentation/exposurenotification/engetexposureinfohandler)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
