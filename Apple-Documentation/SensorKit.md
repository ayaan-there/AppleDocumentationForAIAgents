# SensorKit Documentation

Source: https://sosumi.ai/documentation/sensorkit

---
title: SensorKit
source: https://developer.apple.com/documentation/sensorkit
timestamp: 2026-02-13T19:01:59.572Z
---

## Essentials

- [SensorKit updates](/documentation/updates/sensorkit)

## Setup

- [Configuring your project for sensor reading](/documentation/sensorkit/configuring-your-project-for-sensor-reading)
- [SRSensorReader](/documentation/sensorkit/srsensorreader)

### Checking user authorization

- [var authorizationStatus: SRAuthorizationStatus](/documentation/sensorkit/srsensorreader/authorizationstatus)
- [class func requestAuthorization(sensors: Set<SRSensor>, completion: ((any Error)?) -> Void)](/documentation/sensorkit/srsensorreader/requestauthorization(sensors:completion:))
- [SRAuthorizationStatus](/documentation/sensorkit/srauthorizationstatus)

#### Enumeration Cases

- [case authorized](/documentation/sensorkit/srauthorizationstatus/authorized)
- [case denied](/documentation/sensorkit/srauthorizationstatus/denied)
- [case notDetermined](/documentation/sensorkit/srauthorizationstatus/notdetermined)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srauthorizationstatus/init(rawvalue:))

### Creating a sensor reader

- [init(sensor: SRSensor)](/documentation/sensorkit/srsensorreader/init(sensor:))
- [SRSensor](/documentation/sensorkit/srsensor)

#### Reading device sensors

- [static let deviceUsageReport: SRSensor](/documentation/sensorkit/srsensor/deviceusagereport)
- [static let keyboardMetrics: SRSensor](/documentation/sensorkit/srsensor/keyboardmetrics)
- [static let onWristState: SRSensor](/documentation/sensorkit/srsensor/onwriststate)

#### Reading app activity sensors

- [static let messagesUsageReport: SRSensor](/documentation/sensorkit/srsensor/messagesusagereport)
- [static let phoneUsageReport: SRSensor](/documentation/sensorkit/srsensor/phoneusagereport)

#### Reading user activity sensors

- [static let accelerometer: SRSensor](/documentation/sensorkit/srsensor/accelerometer)
- [static let faceMetrics: SRSensor](/documentation/sensorkit/srsensor/facemetrics)
- [static let heartRate: SRSensor](/documentation/sensorkit/srsensor/heartrate)
- [static let mediaEvents: SRSensor](/documentation/sensorkit/srsensor/mediaevents)
- [static let odometer: SRSensor](/documentation/sensorkit/srsensor/odometer)
- [static let pedometerData: SRSensor](/documentation/sensorkit/srsensor/pedometerdata)
- [static let rotationRate: SRSensor](/documentation/sensorkit/srsensor/rotationrate)
- [static let siriSpeechMetrics: SRSensor](/documentation/sensorkit/srsensor/sirispeechmetrics)
- [static let telephonySpeechMetrics: SRSensor](/documentation/sensorkit/srsensor/telephonyspeechmetrics)
- [static let visits: SRSensor](/documentation/sensorkit/srsensor/visits)
- [static let wristTemperature: SRSensor](/documentation/sensorkit/srsensor/wristtemperature)
- [static let photoplethysmogram: SRSensor](/documentation/sensorkit/srsensor/photoplethysmogram)
- [static let electrocardiogram: SRSensor](/documentation/sensorkit/srsensor/electrocardiogram)

#### Reading environment sensors

- [static let ambientLightSensor: SRSensor](/documentation/sensorkit/srsensor/ambientlightsensor)
- [static let ambientPressure: SRSensor](/documentation/sensorkit/srsensor/ambientpressure)

#### Creating a sensor

- [init(rawValue: String)](/documentation/sensorkit/srsensor/init(rawvalue:))

#### Type Properties

- [static let acousticSettings: SRSensor](/documentation/sensorkit/srsensor/acousticsettings)
- [static let sleepSessions: SRSensor](/documentation/sensorkit/srsensor/sleepsessions)
- [var sensor: SRSensor](/documentation/sensorkit/srsensorreader/sensor)

### Recording sensor data

- [func startRecording()](/documentation/sensorkit/srsensorreader/startrecording())
- [func stopRecording()](/documentation/sensorkit/srsensorreader/stoprecording())

### Reading recorded data

- [func fetch(SRFetchRequest)](/documentation/sensorkit/srsensorreader/fetch(_:))
- [func fetchDevices()](/documentation/sensorkit/srsensorreader/fetchdevices())
- [SRDevice](/documentation/sensorkit/srdevice)

#### Accessing Device Information

- [var model: String](/documentation/sensorkit/srdevice/model)
- [var name: String](/documentation/sensorkit/srdevice/name)
- [var systemName: String](/documentation/sensorkit/srdevice/systemname)
- [var systemVersion: String](/documentation/sensorkit/srdevice/systemversion)
- [var productType: String](/documentation/sensorkit/srdevice/producttype)

#### Accessing the Primary Device

- [class var current: SRDevice](/documentation/sensorkit/srdevice/current)

### Responding to sensor events

- [var delegate: (any SRSensorReaderDelegate)?](/documentation/sensorkit/srsensorreader/delegate)
- [SRSensorReaderDelegate](/documentation/sensorkit/srsensorreaderdelegate)

#### Checking Authorization Status

- [func sensorReader(SRSensorReader, didChange: SRAuthorizationStatus)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:didchange:))

#### Fetching Devices

- [func sensorReader(SRSensorReader, didFetch: [SRDevice])](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:didfetch:))
- [func sensorReader(SRSensorReader, fetchDevicesDidFailWithError: any Error)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:fetchdevicesdidfailwitherror:))
- [SRDevice](/documentation/sensorkit/srdevice)

##### Accessing Device Information

- [var model: String](/documentation/sensorkit/srdevice/model)
- [var name: String](/documentation/sensorkit/srdevice/name)
- [var systemName: String](/documentation/sensorkit/srdevice/systemname)
- [var systemVersion: String](/documentation/sensorkit/srdevice/systemversion)
- [var productType: String](/documentation/sensorkit/srdevice/producttype)

##### Accessing the Primary Device

- [class var current: SRDevice](/documentation/sensorkit/srdevice/current)

#### Recording Data

- [func sensorReaderWillStartRecording(SRSensorReader)](/documentation/sensorkit/srsensorreaderdelegate/sensorreaderwillstartrecording(_:))
- [func sensorReader(SRSensorReader, startRecordingFailedWithError: any Error)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:startrecordingfailedwitherror:))
- [func sensorReaderDidStopRecording(SRSensorReader)](/documentation/sensorkit/srsensorreaderdelegate/sensorreaderdidstoprecording(_:))
- [func sensorReader(SRSensorReader, stopRecordingFailedWithError: any Error)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:stoprecordingfailedwitherror:))

#### Reading Recorded Data

- [func sensorReader(SRSensorReader, fetching: SRFetchRequest, didFetchResult: SRFetchResult<AnyObject>) -> Bool](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:fetching:didfetchresult:))
- [func sensorReader(SRSensorReader, didCompleteFetch: SRFetchRequest)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:didcompletefetch:))
- [func sensorReader(SRSensorReader, fetching: SRFetchRequest, failedWithError: any Error)](/documentation/sensorkit/srsensorreaderdelegate/sensorreader(_:fetching:failedwitherror:))

#### Interpreting Errors

- [let SRErrorDomain: String](/documentation/sensorkit/srerrordomain)
- [SRError](/documentation/sensorkit/srerror)

##### Inspecting Error Information

- [static var errorDomain: String](/documentation/sensorkit/srerror/errordomain)

##### Identifying an Error Cause

- [static var promptDeclined: SRError.Code](/documentation/sensorkit/srerror/promptdeclined)
- [static var dataInaccessible: SRError.Code](/documentation/sensorkit/srerror/datainaccessible)
- [static var fetchRequestInvalid: SRError.Code](/documentation/sensorkit/srerror/fetchrequestinvalid)
- [static var invalidEntitlement: SRError.Code](/documentation/sensorkit/srerror/invalidentitlement)
- [static var noAuthorization: SRError.Code](/documentation/sensorkit/srerror/noauthorization)
- [SRError.Code](/documentation/sensorkit/srerror/code)

##### Errors

- [case promptDeclined](/documentation/sensorkit/srerror/code/promptdeclined)
- [case dataInaccessible](/documentation/sensorkit/srerror/code/datainaccessible)
- [case fetchRequestInvalid](/documentation/sensorkit/srerror/code/fetchrequestinvalid)
- [case invalidEntitlement](/documentation/sensorkit/srerror/code/invalidentitlement)
- [case noAuthorization](/documentation/sensorkit/srerror/code/noauthorization)

##### Creating an error

- [init?(rawValue: Int)](/documentation/sensorkit/srerror/code/init(rawvalue:))

## Authorization

- [com.apple.developer.sensorkit.reader.allow](/documentation/bundleresources/entitlements/com.apple.developer.sensorkit.reader.allow)

## Querying data

- [SRFetchRequest](/documentation/sensorkit/srfetchrequest)

### Selecting the Device

- [var device: SRDevice](/documentation/sensorkit/srfetchrequest/device)
- [SRDevice](/documentation/sensorkit/srdevice)

#### Accessing Device Information

- [var model: String](/documentation/sensorkit/srdevice/model)
- [var name: String](/documentation/sensorkit/srdevice/name)
- [var systemName: String](/documentation/sensorkit/srdevice/systemname)
- [var systemVersion: String](/documentation/sensorkit/srdevice/systemversion)
- [var productType: String](/documentation/sensorkit/srdevice/producttype)

#### Accessing the Primary Device

- [class var current: SRDevice](/documentation/sensorkit/srdevice/current)

### Defining the Time Range

- [var from: SRAbsoluteTime](/documentation/sensorkit/srfetchrequest/from)
- [var to: SRAbsoluteTime](/documentation/sensorkit/srfetchrequest/to)
- [SRAbsoluteTime](/documentation/sensorkit/srabsolutetime)

#### Creating an Absolute Time

- [init(CFTimeInterval)](/documentation/sensorkit/srabsolutetime/init(_:))
- [init(rawValue: CFTimeInterval)](/documentation/sensorkit/srabsolutetime/init(rawvalue:))

#### Accessing the Current Absolute Time

- [static func current() -> SRAbsoluteTime](/documentation/sensorkit/srabsolutetime/current())

#### Converting Absolute Times

- [func toCFAbsoluteTime() -> CFAbsoluteTime](/documentation/sensorkit/srabsolutetime/tocfabsolutetime())
- [static func current() -> SRAbsoluteTime](/documentation/sensorkit/srabsolutetime/current())
- [func toCFAbsoluteTime() -> CFAbsoluteTime](/documentation/sensorkit/srabsolutetime/tocfabsolutetime())
- [SRFetchResult](/documentation/sensorkit/srfetchresult)

### Sampling Data

- [var sample: SampleType](/documentation/sensorkit/srfetchresult/sample)
- [var timestamp: SRAbsoluteTime](/documentation/sensorkit/srfetchresult/timestamp)

## Interpreting data

- [SRAmbientLightSample](/documentation/sensorkit/srambientlightsample)

### Measuring light level

- [var chromaticity: SRAmbientLightSample.Chromaticity](/documentation/sensorkit/srambientlightsample/chromaticity-swift.property)
- [SRAmbientLightSample.Chromaticity](/documentation/sensorkit/srambientlightsample/chromaticity-swift.struct)

#### Creating a Chromaticity

- [init()](/documentation/sensorkit/srambientlightsample/chromaticity-swift.struct/init())
- [init(x: Float32, y: Float32)](/documentation/sensorkit/srambientlightsample/chromaticity-swift.struct/init(x:y:))

#### Setting chromaticity

- [var x: Float32](/documentation/sensorkit/srambientlightsample/chromaticity-swift.struct/x)
- [var y: Float32](/documentation/sensorkit/srambientlightsample/chromaticity-swift.struct/y)
- [var lux: Measurement<UnitIlluminance>](/documentation/sensorkit/srambientlightsample/lux)
- [var placement: SRAmbientLightSample.SensorPlacement](/documentation/sensorkit/srambientlightsample/placement)
- [SRAmbientLightSample.SensorPlacement](/documentation/sensorkit/srambientlightsample/sensorplacement)

#### Placement configurations

- [case frontBottom](/documentation/sensorkit/srambientlightsample/sensorplacement/frontbottom)
- [case frontBottomLeft](/documentation/sensorkit/srambientlightsample/sensorplacement/frontbottomleft)
- [case frontBottomRight](/documentation/sensorkit/srambientlightsample/sensorplacement/frontbottomright)
- [case frontLeft](/documentation/sensorkit/srambientlightsample/sensorplacement/frontleft)
- [case frontRight](/documentation/sensorkit/srambientlightsample/sensorplacement/frontright)
- [case frontTop](/documentation/sensorkit/srambientlightsample/sensorplacement/fronttop)
- [case frontTopLeft](/documentation/sensorkit/srambientlightsample/sensorplacement/fronttopleft)
- [case frontTopRight](/documentation/sensorkit/srambientlightsample/sensorplacement/fronttopright)
- [case unknown](/documentation/sensorkit/srambientlightsample/sensorplacement/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srambientlightsample/sensorplacement/init(rawvalue:))
- [SRDeviceUsageReport](/documentation/sensorkit/srdeviceusagereport)

### Summarizing Device Use

- [var duration: TimeInterval](/documentation/sensorkit/srdeviceusagereport/duration)
- [var totalScreenWakes: Int](/documentation/sensorkit/srdeviceusagereport/totalscreenwakes)
- [var totalUnlocks: Int](/documentation/sensorkit/srdeviceusagereport/totalunlocks)
- [var totalUnlockDuration: TimeInterval](/documentation/sensorkit/srdeviceusagereport/totalunlockduration)

### Analyzing App Use

- [var applicationUsageByCategory: [SRDeviceUsageReport.CategoryKey : [SRDeviceUsageReport.ApplicationUsage]]](/documentation/sensorkit/srdeviceusagereport/applicationusagebycategory)
- [SRDeviceUsageReport.ApplicationUsage](/documentation/sensorkit/srdeviceusagereport/applicationusage)

#### Identifying the App

- [var bundleIdentifier: String?](/documentation/sensorkit/srdeviceusagereport/applicationusage/bundleidentifier)
- [var reportApplicationIdentifier: String](/documentation/sensorkit/srdeviceusagereport/applicationusage/reportapplicationidentifier)
- [var supplementalCategories: [SRSupplementalCategory]](/documentation/sensorkit/srdeviceusagereport/applicationusage/supplementalcategories)
- [SRSupplementalCategory](/documentation/sensorkit/srsupplementalcategory)

##### Identifying the category

- [var identifier: String](/documentation/sensorkit/srsupplementalcategory/identifier)

#### Timing App Use

- [var usageTime: TimeInterval](/documentation/sensorkit/srdeviceusagereport/applicationusage/usagetime)
- [var relativeStartTime: TimeInterval](/documentation/sensorkit/srdeviceusagereport/applicationusage/relativestarttime)

#### Inspecting Text Input

- [var textInputSessions: [SRTextInputSession]](/documentation/sensorkit/srdeviceusagereport/applicationusage/textinputsessions)
- [SRTextInputSession](/documentation/sensorkit/srtextinputsession)

##### Identifying the Session

- [var sessionIdentifier: String](/documentation/sensorkit/srtextinputsession/sessionidentifier)

##### Timing Text Input

- [var duration: TimeInterval](/documentation/sensorkit/srtextinputsession/duration)

##### Inspecting Text Source

- [var sessionType: SRTextInputSession.SessionType](/documentation/sensorkit/srtextinputsession/sessiontype-swift.property)
- [SRTextInputSession.SessionType](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum)

###### Sources

- [case dictation](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum/dictation)
- [case keyboard](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum/keyboard)
- [case pencil](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum/pencil)
- [case thirdPartyKeyboard](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum/thirdpartykeyboard)

###### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srtextinputsession/sessiontype-swift.enum/init(rawvalue:))
- [SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey)

#### Initializers

- [init(rawValue: String)](/documentation/sensorkit/srdeviceusagereport/categorykey/init(rawvalue:))

#### Categories

- [static let books: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/books)
- [static let business: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/business)
- [static let catalogs: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/catalogs)
- [static let developerTools: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/developertools)
- [static let education: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/education)
- [static let entertainment: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/entertainment)
- [static let finance: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/finance)
- [static let foodAndDrink: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/foodanddrink)
- [static let games: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/games)
- [static let graphicsAndDesign: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/graphicsanddesign)
- [static let healthAndFitness: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/healthandfitness)
- [static let kids: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/kids)
- [static let lifestyle: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/lifestyle)
- [static let medical: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/medical)
- [static let miscellaneous: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/miscellaneous)
- [static let music: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/music)
- [static let navigation: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/navigation)
- [static let news: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/news)
- [static let newsstand: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/newsstand)
- [static let photoAndVideo: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/photoandvideo)
- [static let productivity: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/productivity)
- [static let reference: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/reference)
- [static let shopping: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/shopping)
- [static let socialNetworking: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/socialnetworking)
- [static let sports: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/sports)
- [static let stickers: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/stickers)
- [static let travel: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/travel)
- [static let utilities: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/utilities)
- [static let weather: SRDeviceUsageReport.CategoryKey](/documentation/sensorkit/srdeviceusagereport/categorykey/weather)

### Analyzing Notification Use

- [var notificationUsageByCategory: [SRDeviceUsageReport.CategoryKey : [SRDeviceUsageReport.NotificationUsage]]](/documentation/sensorkit/srdeviceusagereport/notificationusagebycategory)
- [SRDeviceUsageReport.NotificationUsage](/documentation/sensorkit/srdeviceusagereport/notificationusage)

#### Analyzing Notification Use

- [var bundleIdentifier: String?](/documentation/sensorkit/srdeviceusagereport/notificationusage/bundleidentifier)
- [var event: SRDeviceUsageReport.NotificationUsage.Event](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.property)
- [SRDeviceUsageReport.NotificationUsage.Event](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum)

##### Events

- [case appLaunch](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/applaunch)
- [case bannerPulldown](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/bannerpulldown)
- [case clear](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/clear)
- [case deduped](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/deduped)
- [case defaultAction](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/defaultaction)
- [case deviceActivated](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/deviceactivated)
- [case deviceUnlocked](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/deviceunlocked)
- [case expired](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/expired)
- [case hide](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/hide)
- [case longLook](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/longlook)
- [case notificationCenterClearAll](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/notificationcenterclearall)
- [case received](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/received)
- [case removed](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/removed)
- [case silence](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/silence)
- [case supplementaryAction](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/supplementaryaction)
- [case tapCoalesce](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/tapcoalesce)
- [case unknown](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srdeviceusagereport/notificationusage/event-swift.enum/init(rawvalue:))

### Analyzing Web Use

- [var webUsageByCategory: [SRDeviceUsageReport.CategoryKey : [SRDeviceUsageReport.WebUsage]]](/documentation/sensorkit/srdeviceusagereport/webusagebycategory)
- [SRDeviceUsageReport.WebUsage](/documentation/sensorkit/srdeviceusagereport/webusage)

#### Timing Web Use

- [var totalUsageTime: TimeInterval](/documentation/sensorkit/srdeviceusagereport/webusage/totalusagetime)

### Getting algorithm information

- [var version: String](/documentation/sensorkit/srdeviceusagereport/version)
- [SRKeyboardMetrics](/documentation/sensorkit/srkeyboardmetrics)

### Inspecting Keyboard Configuration and Sessions

- [var duration: TimeInterval](/documentation/sensorkit/srkeyboardmetrics/duration)
- [var keyboardIdentifier: String](/documentation/sensorkit/srkeyboardmetrics/keyboardidentifier)
- [var version: String](/documentation/sensorkit/srkeyboardmetrics/version)
- [var width: Measurement<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/width)
- [var height: Measurement<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/height)
- [var inputModes: [String]](/documentation/sensorkit/srkeyboardmetrics/inputmodes)
- [var sessionIdentifiers: [String]](/documentation/sensorkit/srkeyboardmetrics/sessionidentifiers)

### Quantifying Key Use

- [var totalWords: Int](/documentation/sensorkit/srkeyboardmetrics/totalwords)
- [var totalAlteredWords: Int](/documentation/sensorkit/srkeyboardmetrics/totalalteredwords)
- [var totalTaps: Int](/documentation/sensorkit/srkeyboardmetrics/totaltaps)
- [var totalDrags: Int](/documentation/sensorkit/srkeyboardmetrics/totaldrags)
- [var totalDeletes: Int](/documentation/sensorkit/srkeyboardmetrics/totaldeletes)
- [var totalEmojis: Int](/documentation/sensorkit/srkeyboardmetrics/totalemojis)
- [var totalPaths: Int](/documentation/sensorkit/srkeyboardmetrics/totalpaths)
- [var totalPathTime: TimeInterval](/documentation/sensorkit/srkeyboardmetrics/totalpathtime)
- [var totalPathLength: Measurement<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/totalpathlength)
- [var totalAutoCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalautocorrections)
- [var totalSpaceCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalspacecorrections)
- [var totalRetroCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalretrocorrections)
- [var totalTranspositionCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totaltranspositioncorrections)
- [var totalInsertKeyCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalinsertkeycorrections)
- [var totalSkipTouchCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalskiptouchcorrections)
- [var totalNearKeyCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalnearkeycorrections)
- [var totalSubstitutionCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalsubstitutioncorrections)
- [var totalHitTestCorrections: Int](/documentation/sensorkit/srkeyboardmetrics/totalhittestcorrections)
- [var totalTypingDuration: TimeInterval](/documentation/sensorkit/srkeyboardmetrics/totaltypingduration)
- [var totalPathPauses: Int](/documentation/sensorkit/srkeyboardmetrics/totalpathpauses)
- [var totalPauses: Int](/documentation/sensorkit/srkeyboardmetrics/totalpauses)
- [var totalTypingEpisodes: Int](/documentation/sensorkit/srkeyboardmetrics/totaltypingepisodes)

### Timing Key Use

- [SRKeyboardMetrics.ProbabilityMetric](/documentation/sensorkit/srkeyboardmetrics/probabilitymetric)

#### Sample Values

- [var distributionSampleValues: [Measurement<UnitType>]](/documentation/sensorkit/srkeyboardmetrics/probabilitymetric/distributionsamplevalues)
- [var touchDownUp: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/touchdownup)
- [var touchUpDown: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/touchupdown)
- [var spaceTouchDownUp: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetouchdownup)
- [var deleteTouchDownUp: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetouchdownup)
- [var shortWordCharKeyTouchDownUp: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/shortwordcharkeytouchdownup)
- [var touchDownDown: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/touchdowndown)
- [var charKeyToPrediction: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/charkeytoprediction)
- [var shortWordCharKeyToCharKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/shortwordcharkeytocharkey)
- [var charKeyToAnyTapKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/charkeytoanytapkey)
- [var anyTapToCharKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/anytaptocharkey)
- [var spaceToCharKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetocharkey)
- [var charKeyToSpaceKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/charkeytospacekey)
- [var spaceToDeleteKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetodeletekey)
- [var deleteToSpaceKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetospacekey)
- [var spaceToSpaceKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetospacekey)
- [var spaceToShiftKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetoshiftkey)
- [var spaceToPlaneChangeKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetoplanechangekey)
- [var spaceToPredictionKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetopredictionkey)
- [var deleteToCharKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetocharkey)
- [var charKeyToDelete: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/charkeytodelete)
- [var deleteToDelete: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetodelete)
- [var deleteToDeletes: [SRKeyboardMetrics.ProbabilityMetric<UnitDuration>]](/documentation/sensorkit/srkeyboardmetrics/deletetodeletes)
- [var deleteToShiftKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetoshiftkey)
- [var deleteToPlaneChangeKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetoplanechangekey)
- [var anyTapToPlaneChangeKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/anytaptoplanechangekey)
- [var planeChangeToAnyTap: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/planechangetoanytap)
- [var charKeyToPlaneChangeKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/charkeytoplanechangekey)
- [var planeChangeKeyToCharKey: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/planechangekeytocharkey)
- [var deleteToPath: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/deletetopath)
- [var pathToDelete: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/pathtodelete)
- [var spaceToPath: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/spacetopath)
- [var pathToSpace: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/pathtospace)
- [var pathToPath: SRKeyboardMetrics.ProbabilityMetric<UnitDuration>](/documentation/sensorkit/srkeyboardmetrics/pathtopath)
- [var longWordTouchDownUp: [SRKeyboardMetrics.ProbabilityMetric<UnitDuration>]](/documentation/sensorkit/srkeyboardmetrics/longwordtouchdownup)
- [var longWordTouchDownDown: [SRKeyboardMetrics.ProbabilityMetric<UnitDuration>]](/documentation/sensorkit/srkeyboardmetrics/longwordtouchdowndown)
- [var longWordTouchUpDown: [SRKeyboardMetrics.ProbabilityMetric<UnitDuration>]](/documentation/sensorkit/srkeyboardmetrics/longwordtouchupdown)
- [var pathTypingSpeed: Double](/documentation/sensorkit/srkeyboardmetrics/pathtypingspeed)
- [var typingSpeed: Double](/documentation/sensorkit/srkeyboardmetrics/typingspeed)

### Measuring Key Use

- [var longWordUpErrorDistance: [SRKeyboardMetrics.ProbabilityMetric<UnitLength>]](/documentation/sensorkit/srkeyboardmetrics/longworduperrordistance)
- [var longWordDownErrorDistance: [SRKeyboardMetrics.ProbabilityMetric<UnitLength>]](/documentation/sensorkit/srkeyboardmetrics/longworddownerrordistance)
- [var upErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/uperrordistance)
- [var downErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/downerrordistance)
- [var spaceUpErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/spaceuperrordistance)
- [var spaceDownErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/spacedownerrordistance)
- [var deleteUpErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/deleteuperrordistance)
- [var deleteDownErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/deletedownerrordistance)
- [var shortWordCharKeyUpErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/shortwordcharkeyuperrordistance)
- [var shortWordCharKeyDownErrorDistance: SRKeyboardMetrics.ProbabilityMetric<UnitLength>](/documentation/sensorkit/srkeyboardmetrics/shortwordcharkeydownerrordistance)
- [var pathErrorDistanceRatio: [NSNumber]](/documentation/sensorkit/srkeyboardmetrics/patherrordistanceratio)

### Inferring Sentiment

- [func wordCount(for: SRKeyboardMetrics.SentimentCategory) -> Int](/documentation/sensorkit/srkeyboardmetrics/wordcount(for:))
- [func emojiCount(for: SRKeyboardMetrics.SentimentCategory) -> Int](/documentation/sensorkit/srkeyboardmetrics/emojicount(for:))
- [SRKeyboardMetrics.SentimentCategory](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory)

#### Sentiments

- [case absolutist](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/absolutist)
- [case anger](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/anger)
- [case anxiety](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/anxiety)
- [case confused](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/confused)
- [case death](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/death)
- [case down](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/down)
- [case health](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/health)
- [case lowEnergy](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/lowenergy)
- [case positive](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/positive)
- [case sad](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/sad)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srkeyboardmetrics/sentimentcategory/init(rawvalue:))
- [SRMediaEvent](/documentation/sensorkit/srmediaevent)

### Identifying Media Objects

- [var mediaIdentifier: String](/documentation/sensorkit/srmediaevent/mediaidentifier)

### Tracking Media Events

- [var eventType: SRMediaEventType](/documentation/sensorkit/srmediaevent/eventtype)
- [SRMediaEventType](/documentation/sensorkit/srmediaeventtype)

#### Event types

- [case onScreen](/documentation/sensorkit/srmediaeventtype/onscreen)
- [case offScreen](/documentation/sensorkit/srmediaeventtype/offscreen)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srmediaeventtype/init(rawvalue:))
- [SRMessagesUsageReport](/documentation/sensorkit/srmessagesusagereport)

### Analyzing Message Use

- [var duration: TimeInterval](/documentation/sensorkit/srmessagesusagereport/duration)
- [var totalIncomingMessages: Int](/documentation/sensorkit/srmessagesusagereport/totalincomingmessages)
- [var totalOutgoingMessages: Int](/documentation/sensorkit/srmessagesusagereport/totaloutgoingmessages)
- [var totalUniqueContacts: Int](/documentation/sensorkit/srmessagesusagereport/totaluniquecontacts)
- [SRPhoneUsageReport](/documentation/sensorkit/srphoneusagereport)

### Analyzing Phone Use

- [var duration: TimeInterval](/documentation/sensorkit/srphoneusagereport/duration)
- [var totalIncomingCalls: Int](/documentation/sensorkit/srphoneusagereport/totalincomingcalls)
- [var totalOutgoingCalls: Int](/documentation/sensorkit/srphoneusagereport/totaloutgoingcalls)
- [var totalPhoneCallDuration: TimeInterval](/documentation/sensorkit/srphoneusagereport/totalphonecallduration)
- [var totalUniqueContacts: Int](/documentation/sensorkit/srphoneusagereport/totaluniquecontacts)
- [SRVisit](/documentation/sensorkit/srvisit)

### Identifying a Visit

- [var identifier: UUID](/documentation/sensorkit/srvisit/identifier)

### Accessing Visit Information

- [var arrivalDateInterval: DateInterval](/documentation/sensorkit/srvisit/arrivaldateinterval)
- [var departureDateInterval: DateInterval](/documentation/sensorkit/srvisit/departuredateinterval)
- [var distanceFromHome: CLLocationDistance](/documentation/sensorkit/srvisit/distancefromhome)
- [var locationCategory: SRVisit.LocationCategory](/documentation/sensorkit/srvisit/locationcategory-swift.property)
- [SRVisit.LocationCategory](/documentation/sensorkit/srvisit/locationcategory-swift.enum)

#### Categories

- [case gym](/documentation/sensorkit/srvisit/locationcategory-swift.enum/gym)
- [case home](/documentation/sensorkit/srvisit/locationcategory-swift.enum/home)
- [case school](/documentation/sensorkit/srvisit/locationcategory-swift.enum/school)
- [case unknown](/documentation/sensorkit/srvisit/locationcategory-swift.enum/unknown)
- [case work](/documentation/sensorkit/srvisit/locationcategory-swift.enum/work)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srvisit/locationcategory-swift.enum/init(rawvalue:))
- [SRWristDetection](/documentation/sensorkit/srwristdetection)

### Inspecting Watch Configuration

- [var crownOrientation: SRWristDetection.CrownOrientation](/documentation/sensorkit/srwristdetection/crownorientation-swift.property)
- [SRWristDetection.CrownOrientation](/documentation/sensorkit/srwristdetection/crownorientation-swift.enum)

#### Orientations

- [case left](/documentation/sensorkit/srwristdetection/crownorientation-swift.enum/left)
- [case right](/documentation/sensorkit/srwristdetection/crownorientation-swift.enum/right)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srwristdetection/crownorientation-swift.enum/init(rawvalue:))
- [var onWrist: Bool](/documentation/sensorkit/srwristdetection/onwrist)
- [var onWristDate: Date?](/documentation/sensorkit/srwristdetection/onwristdate)
- [var offWristDate: Date?](/documentation/sensorkit/srwristdetection/offwristdate)
- [var wristLocation: SRWristDetection.WristLocation](/documentation/sensorkit/srwristdetection/wristlocation-swift.property)
- [SRWristDetection.WristLocation](/documentation/sensorkit/srwristdetection/wristlocation-swift.enum)

#### Wrist Preferences

- [case left](/documentation/sensorkit/srwristdetection/wristlocation-swift.enum/left)
- [case right](/documentation/sensorkit/srwristdetection/wristlocation-swift.enum/right)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srwristdetection/wristlocation-swift.enum/init(rawvalue:))

## Deleting samples

- [SRDeletionRecord](/documentation/sensorkit/srdeletionrecord)

### Accessing the Deletion Reason

- [var reason: SRDeletionReason](/documentation/sensorkit/srdeletionrecord/reason)
- [SRDeletionReason](/documentation/sensorkit/srdeletionreason)

#### Reasons

- [case ageLimit](/documentation/sensorkit/srdeletionreason/agelimit)
- [case lowDiskSpace](/documentation/sensorkit/srdeletionreason/lowdiskspace)
- [case noInterestedClients](/documentation/sensorkit/srdeletionreason/nointerestedclients)
- [case systemInitiated](/documentation/sensorkit/srdeletionreason/systeminitiated)
- [case userInitiated](/documentation/sensorkit/srdeletionreason/userinitiated)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srdeletionreason/init(rawvalue:))

### Accessing the Deletion Time

- [var startTime: SRAbsoluteTime](/documentation/sensorkit/srdeletionrecord/starttime)
- [var endTime: SRAbsoluteTime](/documentation/sensorkit/srdeletionrecord/endtime)

## Analyzing speech

- [SRSpeechMetrics](/documentation/sensorkit/srspeechmetrics)

### Getting session information

- [var sessionIdentifier: String](/documentation/sensorkit/srspeechmetrics/sessionidentifier)
- [var sessionFlags: SRSpeechMetrics.SessionFlags](/documentation/sensorkit/srspeechmetrics/sessionflags-swift.property)
- [SRSpeechMetrics.SessionFlags](/documentation/sensorkit/srspeechmetrics/sessionflags-swift.struct)

#### Session flags

- [static var bypassVoiceProcessing: SRSpeechMetrics.SessionFlags](/documentation/sensorkit/srspeechmetrics/sessionflags-swift.struct/bypassvoiceprocessing)

#### Creating session flags

- [init(rawValue: UInt)](/documentation/sensorkit/srspeechmetrics/sessionflags-swift.struct/init(rawvalue:))
- [var timeSinceAudioStart: TimeInterval](/documentation/sensorkit/srspeechmetrics/timesinceaudiostart)
- [var timestamp: Date](/documentation/sensorkit/srspeechmetrics/timestamp)

### Getting speech metrics and analytics

- [var audioLevel: SRAudioLevel?](/documentation/sensorkit/srspeechmetrics/audiolevel)
- [SRAudioLevel](/documentation/sensorkit/sraudiolevel)

#### Getting metrics

- [var timeRange: CMTimeRange](/documentation/sensorkit/sraudiolevel/timerange)
- [var loudness: Double](/documentation/sensorkit/sraudiolevel/loudness)
- [var speechRecognition: SFSpeechRecognitionResult?](/documentation/sensorkit/srspeechmetrics/speechrecognition)
- [var soundClassification: SNClassificationResult?](/documentation/sensorkit/srspeechmetrics/soundclassification)
- [var speechExpression: SRSpeechExpression?](/documentation/sensorkit/srspeechmetrics/speechexpression)
- [SRSpeechExpression](/documentation/sensorkit/srspeechexpression)

### Getting speech metrics

- [var timeRange: CMTimeRange](/documentation/sensorkit/srspeechexpression/timerange)
- [var version: String](/documentation/sensorkit/srspeechexpression/version)

### Getting speech analytics

- [var confidence: Double](/documentation/sensorkit/srspeechexpression/confidence)
- [var mood: Double](/documentation/sensorkit/srspeechexpression/mood)
- [var valence: Double](/documentation/sensorkit/srspeechexpression/valence)
- [var activation: Double](/documentation/sensorkit/srspeechexpression/activation)
- [var dominance: Double](/documentation/sensorkit/srspeechexpression/dominance)

## Analyzing faces

- [SRFaceMetrics](/documentation/sensorkit/srfacemetrics)

### Getting session information

- [var sessionIdentifier: String](/documentation/sensorkit/srfacemetrics/sessionidentifier)
- [var context: SRFaceMetrics.Context](/documentation/sensorkit/srfacemetrics/context-swift.property)
- [SRFaceMetrics.Context](/documentation/sensorkit/srfacemetrics/context-swift.struct)

#### Camera contexts

- [static var deviceUnlock: SRFaceMetrics.Context](/documentation/sensorkit/srfacemetrics/context-swift.struct/deviceunlock)
- [static var messagingAppUsage: SRFaceMetrics.Context](/documentation/sensorkit/srfacemetrics/context-swift.struct/messagingappusage)

#### Creating camera contexts

- [init(rawValue: UInt)](/documentation/sensorkit/srfacemetrics/context-swift.struct/init(rawvalue:))
- [var version: String](/documentation/sensorkit/srfacemetrics/version)

### Getting face analytics

- [var faceAnchor: ARFaceAnchor](/documentation/sensorkit/srfacemetrics/faceanchor)
- [var partialFaceExpressions: [SRFaceMetricsExpression]](/documentation/sensorkit/srfacemetrics/partialfaceexpressions)
- [var wholeFaceExpressions: [SRFaceMetricsExpression]](/documentation/sensorkit/srfacemetrics/wholefaceexpressions)
- [SRFaceMetricsExpression](/documentation/sensorkit/srfacemetricsexpression)

#### Getting the expression identifier and analysis

- [var value: Double](/documentation/sensorkit/srfacemetricsexpression/value)
- [var identifier: String](/documentation/sensorkit/srfacemetricsexpression/identifier)
- [var SR_ARKIT_SUPPORTED: Int32](/documentation/sensorkit/sr_arkit_supported)

## Recording wrist temperatures

- [SRWristTemperatureSession](/documentation/sensorkit/srwristtemperaturesession)

### Getting session information

- [var startDate: Date](/documentation/sensorkit/srwristtemperaturesession/startdate)
- [var duration: TimeInterval](/documentation/sensorkit/srwristtemperaturesession/duration)
- [var version: String](/documentation/sensorkit/srwristtemperaturesession/version)

### Getting recorded temperatures

- [var temperatures: some Sequence<SRWristTemperature>](/documentation/sensorkit/srwristtemperaturesession/temperatures-8bqrl)
- [SRWristTemperature](/documentation/sensorkit/srwristtemperature)

### Getting temperature information

- [var timestamp: Date](/documentation/sensorkit/srwristtemperature/timestamp)
- [var value: Measurement<UnitTemperature>](/documentation/sensorkit/srwristtemperature/value)
- [var errorEstimate: Measurement<UnitTemperature>](/documentation/sensorkit/srwristtemperature/errorestimate)

### Determining the accuracy

- [var condition: SRWristTemperature.Condition](/documentation/sensorkit/srwristtemperature/condition-swift.property)
- [SRWristTemperature.Condition](/documentation/sensorkit/srwristtemperature/condition-swift.struct)

#### Conditions

- [static var offWrist: SRWristTemperature.Condition](/documentation/sensorkit/srwristtemperature/condition-swift.struct/offwrist)
- [static var onCharger: SRWristTemperature.Condition](/documentation/sensorkit/srwristtemperature/condition-swift.struct/oncharger)
- [static var inMotion: SRWristTemperature.Condition](/documentation/sensorkit/srwristtemperature/condition-swift.struct/inmotion)

#### Creating conditions

- [init(rawValue: UInt)](/documentation/sensorkit/srwristtemperature/condition-swift.struct/init(rawvalue:))

## Recording ectrocardiogram data

- [SRElectrocardiogramSample](/documentation/sensorkit/srelectrocardiogramsample)

### Accessing ECG data

- [var date: Date](/documentation/sensorkit/srelectrocardiogramsample/date)
- [var frequency: Measurement<UnitFrequency>](/documentation/sensorkit/srelectrocardiogramsample/frequency)
- [var lead: SRElectrocardiogramSample.Lead](/documentation/sensorkit/srelectrocardiogramsample/lead-swift.property)
- [SRElectrocardiogramSample.Lead](/documentation/sensorkit/srelectrocardiogramsample/lead-swift.enum)

#### Locations

- [case leftArmMinusRightArm](/documentation/sensorkit/srelectrocardiogramsample/lead-swift.enum/leftarmminusrightarm)
- [case rightArmMinusLeftArm](/documentation/sensorkit/srelectrocardiogramsample/lead-swift.enum/rightarmminusleftarm)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srelectrocardiogramsample/lead-swift.enum/init(rawvalue:))
- [var session: SRElectrocardiogramSession](/documentation/sensorkit/srelectrocardiogramsample/session)
- [SRElectrocardiogramSession](/documentation/sensorkit/srelectrocardiogramsession)

#### Getting session information

- [var identifier: String](/documentation/sensorkit/srelectrocardiogramsession/identifier)
- [var sessionGuidance: SRElectrocardiogramSession.SessionGuidance](/documentation/sensorkit/srelectrocardiogramsession/sessionguidance-swift.property)
- [SRElectrocardiogramSession.SessionGuidance](/documentation/sensorkit/srelectrocardiogramsession/sessionguidance-swift.enum)

##### Types

- [case guided](/documentation/sensorkit/srelectrocardiogramsession/sessionguidance-swift.enum/guided)
- [case unguided](/documentation/sensorkit/srelectrocardiogramsession/sessionguidance-swift.enum/unguided)

##### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srelectrocardiogramsession/sessionguidance-swift.enum/init(rawvalue:))
- [var state: SRElectrocardiogramSession.State](/documentation/sensorkit/srelectrocardiogramsession/state-swift.property)
- [SRElectrocardiogramSession.State](/documentation/sensorkit/srelectrocardiogramsession/state-swift.enum)

##### States

- [case begin](/documentation/sensorkit/srelectrocardiogramsession/state-swift.enum/begin)
- [case active](/documentation/sensorkit/srelectrocardiogramsession/state-swift.enum/active)
- [case end](/documentation/sensorkit/srelectrocardiogramsession/state-swift.enum/end)

##### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/srelectrocardiogramsession/state-swift.enum/init(rawvalue:))
- [var data: [SRElectrocardiogramData]](/documentation/sensorkit/srelectrocardiogramsample/data)
- [SRElectrocardiogramData](/documentation/sensorkit/srelectrocardiogramdata)

#### Getting electrocardiogram details

- [var flags: SRElectrocardiogramData.Flags](/documentation/sensorkit/srelectrocardiogramdata/flags-swift.property)
- [SRElectrocardiogramData.Flags](/documentation/sensorkit/srelectrocardiogramdata/flags-swift.struct)

##### Getting context or events

- [static var crownTouched: SRElectrocardiogramData.Flags](/documentation/sensorkit/srelectrocardiogramdata/flags-swift.struct/crowntouched)
- [static var signalInvalid: SRElectrocardiogramData.Flags](/documentation/sensorkit/srelectrocardiogramdata/flags-swift.struct/signalinvalid)

##### Initializing flags

- [init(rawValue: UInt)](/documentation/sensorkit/srelectrocardiogramdata/flags-swift.struct/init(rawvalue:))
- [var value: Measurement<UnitElectricPotentialDifference>](/documentation/sensorkit/srelectrocardiogramdata/value)

## Recording photoplethysmogram data

- [SRPhotoplethysmogramSample](/documentation/sensorkit/srphotoplethysmogramsample)

### Accessing PPG data

- [var startDate: Date](/documentation/sensorkit/srphotoplethysmogramsample/startdate)
- [var nanosecondsSinceStart: Int64](/documentation/sensorkit/srphotoplethysmogramsample/nanosecondssincestart)
- [var usage: [SRPhotoplethysmogramSample.Usage]](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.property)
- [SRPhotoplethysmogramSample.Usage](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct)

#### Getting the reading method

- [static let foregroundHeartRate: SRPhotoplethysmogramSample.Usage](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct/foregroundheartrate)
- [static let deepBreathing: SRPhotoplethysmogramSample.Usage](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct/deepbreathing)
- [static let foregroundBloodOxygen: SRPhotoplethysmogramSample.Usage](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct/foregroundbloodoxygen)
- [static let backgroundSystem: SRPhotoplethysmogramSample.Usage](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct/backgroundsystem)

#### Initializing usage

- [init(rawValue: String)](/documentation/sensorkit/srphotoplethysmogramsample/usage-swift.struct/init(rawvalue:))
- [var opticalSamples: [SRPhotoplethysmogramOpticalSample]](/documentation/sensorkit/srphotoplethysmogramsample/opticalsamples)
- [SRPhotoplethysmogramOpticalSample](/documentation/sensorkit/srphotoplethysmogramopticalsample)

#### Accessing optical data

- [var emitter: Int](/documentation/sensorkit/srphotoplethysmogramopticalsample/emitter)
- [var activePhotodiodeIndexes: IndexSet](/documentation/sensorkit/srphotoplethysmogramopticalsample/activephotodiodeindexes)
- [var signalIdentifier: Int](/documentation/sensorkit/srphotoplethysmogramopticalsample/signalidentifier)
- [var nominalWavelength: Measurement<UnitLength>](/documentation/sensorkit/srphotoplethysmogramopticalsample/nominalwavelength)
- [var effectiveWavelength: Measurement<UnitLength>](/documentation/sensorkit/srphotoplethysmogramopticalsample/effectivewavelength)
- [var samplingFrequency: Measurement<UnitFrequency>](/documentation/sensorkit/srphotoplethysmogramopticalsample/samplingfrequency)
- [var nanosecondsSinceStart: Int64](/documentation/sensorkit/srphotoplethysmogramopticalsample/nanosecondssincestart)
- [var conditions: [SRPhotoplethysmogramOpticalSample.Condition]](/documentation/sensorkit/srphotoplethysmogramopticalsample/conditions)
- [SRPhotoplethysmogramOpticalSample.Condition](/documentation/sensorkit/srphotoplethysmogramopticalsample/condition)

##### Getting the condition

- [static let signalSaturation: SRPhotoplethysmogramOpticalSample.Condition](/documentation/sensorkit/srphotoplethysmogramopticalsample/condition/signalsaturation)
- [static let unreliableNoise: SRPhotoplethysmogramOpticalSample.Condition](/documentation/sensorkit/srphotoplethysmogramopticalsample/condition/unreliablenoise)

##### Initializing a condition

- [init(rawValue: String)](/documentation/sensorkit/srphotoplethysmogramopticalsample/condition/init(rawvalue:))
- [var noiseTerms: SRPhotoplethysmogramOpticalSample.NoiseTerms?](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.property)
- [SRPhotoplethysmogramOpticalSample.NoiseTerms](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.struct)

##### Accessing noise terms

- [let whiteNoise: Double](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.struct/whitenoise)
- [let pinkNoise: Double](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.struct/pinknoise)
- [let backgroundNoise: Double](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.struct/backgroundnoise)
- [let backgroundNoiseOffset: Double](/documentation/sensorkit/srphotoplethysmogramopticalsample/noiseterms-swift.struct/backgroundnoiseoffset)
- [var normalizedReflectance: Double?](/documentation/sensorkit/srphotoplethysmogramopticalsample/normalizedreflectance-15f2k)
- [var accelerometerSamples: [SRPhotoplethysmogramAccelerometerSample]](/documentation/sensorkit/srphotoplethysmogramsample/accelerometersamples)
- [SRPhotoplethysmogramAccelerometerSample](/documentation/sensorkit/srphotoplethysmogramaccelerometersample)

#### Accessing accelerometer data

- [var nanosecondsSinceStart: Int64](/documentation/sensorkit/srphotoplethysmogramaccelerometersample/nanosecondssincestart)
- [var samplingFrequency: Measurement<UnitFrequency>](/documentation/sensorkit/srphotoplethysmogramaccelerometersample/samplingfrequency)
- [var x: Measurement<UnitAcceleration>](/documentation/sensorkit/srphotoplethysmogramaccelerometersample/x)
- [var y: Measurement<UnitAcceleration>](/documentation/sensorkit/srphotoplethysmogramaccelerometersample/y)
- [var z: Measurement<UnitAcceleration>](/documentation/sensorkit/srphotoplethysmogramaccelerometersample/z)
- [var temperature: Measurement<UnitTemperature>?](/documentation/sensorkit/srphotoplethysmogramsample/temperature)

## Classes

- [SRAcousticSettings](/documentation/sensorkit/sracousticsettings)

### Classes

- [SRAcousticSettings.Accessibility](/documentation/sensorkit/sracousticsettings/accessibility)

#### Classes

- [SRAcousticSettings.Accessibility.BackgroundSounds](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class)

##### Instance Properties

- [var isEnabled: Bool](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/isenabled)
- [var isPlayWithMediaEnabled: Bool](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/isplaywithmediaenabled)
- [var isStopOnLockEnabled: Bool](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/isstoponlockenabled)
- [var relativeVolume: Double](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/relativevolume)
- [var relativeVolumeWithMedia: Double](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/relativevolumewithmedia)
- [var soundName: SRAcousticSettings.Accessibility.BackgroundSounds.Name](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/soundname)

##### Enumerations

- [SRAcousticSettings.Accessibility.BackgroundSounds.Name](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name)

###### Enumeration Cases

- [case airplane](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/airplane)
- [case babble](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/babble)
- [case balancedNoise](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/balancednoise)
- [case boat](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/boat)
- [case brightNoise](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/brightnoise)
- [case bus](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/bus)
- [case darkNoise](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/darknoise)
- [case fire](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/fire)
- [case night](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/night)
- [case ocean](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/ocean)
- [case quietNight](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/quietnight)
- [case rain](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/rain)
- [case rainOnRoof](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/rainonroof)
- [case steam](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/steam)
- [case stream](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/stream)
- [case train](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/train)

###### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.class/name/init(rawvalue:))
- [SRAcousticSettings.Accessibility.HeadphoneAccommodations](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class)

##### Instance Properties

- [var isEnabled: Bool](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/isenabled)
- [var mediaEnhanceApplication: SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceApplication](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.property)
- [var mediaEnhanceBoosting: SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceBoosting](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.property)
- [var mediaEnhanceTuning: SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceTuning](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.property)

##### Enumerations

- [SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceApplication](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum)

###### Enumeration Cases

- [case media](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum/media)
- [case none](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum/none)
- [case phone](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum/phone)
- [case phoneAndMedia](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum/phoneandmedia)

###### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceapplication-swift.enum/init(rawvalue:))
- [SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceBoosting](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.enum)

###### Enumeration Cases

- [case moderate](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.enum/moderate)
- [case slight](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.enum/slight)
- [case strong](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.enum/strong)

###### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhanceboosting-swift.enum/init(rawvalue:))
- [SRAcousticSettings.Accessibility.HeadphoneAccommodations.MediaEnhanceTuning](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.enum)

###### Enumeration Cases

- [case balancedTone](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.enum/balancedtone)
- [case brightness](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.enum/brightness)
- [case vocalRange](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.enum/vocalrange)

###### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.class/mediaenhancetuning-swift.enum/init(rawvalue:))

#### Instance Properties

- [var backgroundSounds: SRAcousticSettings.Accessibility.BackgroundSounds](/documentation/sensorkit/sracousticsettings/accessibility/backgroundsounds-swift.property)
- [var headphoneAccommodations: SRAcousticSettings.Accessibility.HeadphoneAccommodations](/documentation/sensorkit/sracousticsettings/accessibility/headphoneaccommodations-swift.property)
- [var isMonoAudioEnabled: Bool](/documentation/sensorkit/sracousticsettings/accessibility/ismonoaudioenabled)
- [var leftRightBalance: Double](/documentation/sensorkit/sracousticsettings/accessibility/leftrightbalance)
- [SRAcousticSettings.MusicEQ](/documentation/sensorkit/sracousticsettings/musiceq)

#### Instance Properties

- [var isLateNightModeEnabled: Bool](/documentation/sensorkit/sracousticsettings/musiceq/islatenightmodeenabled)
- [var isSoundCheckEnabled: Bool](/documentation/sensorkit/sracousticsettings/musiceq/issoundcheckenabled)

### Instance Properties

- [var accessibilitySettings: SRAcousticSettings.Accessibility](/documentation/sensorkit/sracousticsettings/accessibilitysettings)
- [var audioExposureSampleLifetime: SRAcousticSettings.SampleLifetime](/documentation/sensorkit/sracousticsettings/audioexposuresamplelifetime)
- [var headphoneSafetyAudioLevel: Double?](/documentation/sensorkit/sracousticsettings/headphonesafetyaudiolevel-5lc1v)
- [var isEnvironmentalSoundMeasurementsEnabled: Bool](/documentation/sensorkit/sracousticsettings/isenvironmentalsoundmeasurementsenabled)
- [var musicEQSettings: SRAcousticSettings.MusicEQ](/documentation/sensorkit/sracousticsettings/musiceqsettings)

### Enumerations

- [SRAcousticSettings.SampleLifetime](/documentation/sensorkit/sracousticsettings/samplelifetime)

#### Enumeration Cases

- [case eightDays](/documentation/sensorkit/sracousticsettings/samplelifetime/eightdays)
- [case untilUserDeletes](/documentation/sensorkit/sracousticsettings/samplelifetime/untiluserdeletes)

#### Initializers

- [init?(rawValue: Int)](/documentation/sensorkit/sracousticsettings/samplelifetime/init(rawvalue:))
- [SRSleepSession](/documentation/sensorkit/srsleepsession)

### Instance Properties

- [var duration: TimeInterval](/documentation/sensorkit/srsleepsession/duration)
- [var identifier: String](/documentation/sensorkit/srsleepsession/identifier)
- [var startDate: Date](/documentation/sensorkit/srsleepsession/startdate)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
