# Device Activity Documentation

Source: https://sosumi.ai/documentation/deviceactivity

---
title: Device Activity
source: https://developer.apple.com/documentation/deviceactivity
timestamp: 2026-02-13T18:56:10.673Z
---

## Manage activities

- [DeviceActivityEvent](/documentation/deviceactivity/deviceactivityevent)

### Creating an Event

- [init(applications: Set<ApplicationToken>, categories: Set<ActivityCategoryToken>, webDomains: Set<WebDomainToken>, threshold: DateComponents)](/documentation/deviceactivity/deviceactivityevent/init(applications:categories:webdomains:threshold:))
- [DeviceActivityEvent.Name](/documentation/deviceactivity/deviceactivityevent/name)

#### Creating an Instance

- [init(rawValue: String)](/documentation/deviceactivity/deviceactivityevent/name/init(rawvalue:))
- [init(String)](/documentation/deviceactivity/deviceactivityevent/name/init(_:))
- [var includesAllActivity: Bool](/documentation/deviceactivity/deviceactivityevent/includesallactivity)

### Including Objects in an Event

- [var applications: Set<ApplicationToken>](/documentation/deviceactivity/deviceactivityevent/applications)
- [var categories: Set<ActivityCategoryToken>](/documentation/deviceactivity/deviceactivityevent/categories)
- [var webDomains: Set<WebDomainToken>](/documentation/deviceactivity/deviceactivityevent/webdomains)
- [var threshold: DateComponents](/documentation/deviceactivity/deviceactivityevent/threshold)

### Initializers

- [init(applications: Set<ApplicationToken>, categories: Set<ActivityCategoryToken>, webDomains: Set<WebDomainToken>, threshold: DateComponents, includesPastActivity: Bool)](/documentation/deviceactivity/deviceactivityevent/init(applications:categories:webdomains:threshold:includespastactivity:))

### Instance Properties

- [var includesPastActivity: Bool](/documentation/deviceactivity/deviceactivityevent/includespastactivity)
- [DeviceActivityName](/documentation/deviceactivity/deviceactivityname)

### Creating an Instance

- [init(rawValue: String)](/documentation/deviceactivity/deviceactivityname/init(rawvalue:))
- [init(String)](/documentation/deviceactivity/deviceactivityname/init(_:))
- [DeviceActivitySchedule](/documentation/deviceactivity/deviceactivityschedule)

### Creating a Schedule

- [init(intervalStart: DateComponents, intervalEnd: DateComponents, repeats: Bool, warningTime: DateComponents?)](/documentation/deviceactivity/deviceactivityschedule/init(intervalstart:intervalend:repeats:warningtime:))
- [var intervalEnd: DateComponents](/documentation/deviceactivity/deviceactivityschedule/intervalend)
- [var intervalStart: DateComponents](/documentation/deviceactivity/deviceactivityschedule/intervalstart)
- [var nextInterval: DateInterval?](/documentation/deviceactivity/deviceactivityschedule/nextinterval)
- [var repeats: Bool](/documentation/deviceactivity/deviceactivityschedule/repeats)
- [var warningTime: DateComponents?](/documentation/deviceactivity/deviceactivityschedule/warningtime)
- [DeviceActivityCenter](/documentation/deviceactivity/deviceactivitycenter)

### Monitoring Device Activities

- [init()](/documentation/deviceactivity/deviceactivitycenter/init())
- [func startMonitoring(DeviceActivityName, during: DeviceActivitySchedule, events: [DeviceActivityEvent.Name : DeviceActivityEvent]) throws](/documentation/deviceactivity/deviceactivitycenter/startmonitoring(_:during:events:))
- [func stopMonitoring([DeviceActivityName])](/documentation/deviceactivity/deviceactivitycenter/stopmonitoring(_:))
- [var activities: [DeviceActivityName]](/documentation/deviceactivity/deviceactivitycenter/activities)

### Getting the Events and Schedules

- [func events(for: DeviceActivityName) -> [DeviceActivityEvent.Name : DeviceActivityEvent]](/documentation/deviceactivity/deviceactivitycenter/events(for:))
- [func schedule(for: DeviceActivityName) -> DeviceActivitySchedule?](/documentation/deviceactivity/deviceactivitycenter/schedule(for:))

### Enumerations

- [DeviceActivityCenter.MonitoringError](/documentation/deviceactivity/deviceactivitycenter/monitoringerror)

#### Checking for Errors

- [case excessiveActivities](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/excessiveactivities)
- [case intervalTooLong](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/intervaltoolong)
- [case intervalTooShort](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/intervaltooshort)
- [case invalidDateComponents](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/invaliddatecomponents)
- [case unauthorized](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/unauthorized)

#### Getting the Localized Message

- [var errorDescription: String?](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/errordescription)
- [var recoverySuggestion: String?](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/recoverysuggestion)

## Monitor activity

- [DeviceActivityMonitor](/documentation/deviceactivity/deviceactivitymonitor)

### Configuring a Monitor

- [init()](/documentation/deviceactivity/deviceactivitymonitor/init())

### Monitoring Scheduled Intervals

- [func intervalDidEnd(for: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/intervaldidend(for:))
- [func intervalDidStart(for: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/intervaldidstart(for:))
- [func intervalWillEndWarning(for: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/intervalwillendwarning(for:))
- [func intervalWillStartWarning(for: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/intervalwillstartwarning(for:))

### Monitoring Event Thresholds

- [func eventDidReachThreshold(DeviceActivityEvent.Name, activity: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/eventdidreachthreshold(_:activity:))
- [func eventWillReachThresholdWarning(DeviceActivityEvent.Name, activity: DeviceActivityName)](/documentation/deviceactivity/deviceactivitymonitor/eventwillreachthresholdwarning(_:activity:))

## Report activity

- [DeviceActivityReport](/documentation/deviceactivity/deviceactivityreport)

### Structures

- [DeviceActivityReport.Context](/documentation/deviceactivity/deviceactivityreport/context)

#### Initializers

- [init(String)](/documentation/deviceactivity/deviceactivityreport/context/init(_:))
- [init(rawValue: String)](/documentation/deviceactivity/deviceactivityreport/context/init(rawvalue:))

#### Instance Properties

- [var rawValue: String](/documentation/deviceactivity/deviceactivityreport/context/rawvalue)

### Initializers

- [init(DeviceActivityReport.Context, filter: DeviceActivityFilter)](/documentation/deviceactivity/deviceactivityreport/init(_:filter:))

### Instance Properties

- [var body: some View](/documentation/deviceactivity/deviceactivityreport/body)
- [DeviceActivityReportExtension](/documentation/deviceactivity/deviceactivityreportextension)

### Associated Types

- [Body](/documentation/deviceactivity/deviceactivityreportextension/body-swift.associatedtype)

### Instance Properties

- [var body: Self.Body](/documentation/deviceactivity/deviceactivityreportextension/body-swift.property)
- [DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportscene)

### Associated Types

- [Configuration](/documentation/deviceactivity/deviceactivityreportscene/configuration)
- [Content](/documentation/deviceactivity/deviceactivityreportscene/content-swift.associatedtype)

### Instance Properties

- [var content: (Self.Configuration) -> Self.Content](/documentation/deviceactivity/deviceactivityreportscene/content-swift.property)
- [var context: DeviceActivityReport.Context](/documentation/deviceactivity/deviceactivityreportscene/context)

### Instance Methods

- [func makeConfiguration(representing: DeviceActivityResults<DeviceActivityData>) async -> Self.Configuration](/documentation/deviceactivity/deviceactivityreportscene/makeconfiguration(representing:))
- [DeviceActivityReportBuilder](/documentation/deviceactivity/deviceactivityreportbuilder)

### Type Methods

- [static func buildBlock<Scene>(Scene) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:))
- [static func buildBlock<S0, S1>(S0, S1) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:))
- [static func buildBlock<S0, S1, S2>(S0, S1, S2) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:))
- [static func buildBlock<S0, S1, S2, S3>(S0, S1, S2, S3) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4>(S0, S1, S2, S3, S4) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5>(S0, S1, S2, S3, S4, S5) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6>(S0, S1, S2, S3, S4, S5, S6) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7>(S0, S1, S2, S3, S4, S5, S6, S7) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8>(S0, S1, S2, S3, S4, S5, S6, S7, S8) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17, S18>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17, S18) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17, S18, S19>(S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12, S13, S14, S15, S16, S17, S18, S19) -> some DeviceActivityReportScene](/documentation/deviceactivity/deviceactivityreportbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))

## Filter activity data

- [DeviceActivityFilter](/documentation/deviceactivity/deviceactivityfilter)

### Structures

- [DeviceActivityFilter.Devices](/documentation/deviceactivity/deviceactivityfilter/devices-swift.struct)

#### Initializers

- [init(Set<DeviceActivityData.Device.Model>)](/documentation/deviceactivity/deviceactivityfilter/devices-swift.struct/init(_:))

#### Type Properties

- [static let all: DeviceActivityFilter.Devices](/documentation/deviceactivity/deviceactivityfilter/devices-swift.struct/all)
- [DeviceActivityFilter.Users](/documentation/deviceactivity/deviceactivityfilter/users-swift.struct)

#### Type Properties

- [static let all: DeviceActivityFilter.Users](/documentation/deviceactivity/deviceactivityfilter/users-swift.struct/all)
- [static let children: DeviceActivityFilter.Users](/documentation/deviceactivity/deviceactivityfilter/users-swift.struct/children)

### Initializers

- [init(segment: DeviceActivityFilter.SegmentInterval, devices: DeviceActivityFilter.Devices?, applications: Set<ApplicationToken>, categories: Set<ActivityCategoryToken>, webDomains: Set<WebDomainToken>)](/documentation/deviceactivity/deviceactivityfilter/init(segment:devices:applications:categories:webdomains:))
- [init(segment: DeviceActivityFilter.SegmentInterval, users: DeviceActivityFilter.Users, devices: DeviceActivityFilter.Devices, applications: Set<ApplicationToken>, categories: Set<ActivityCategoryToken>, webDomains: Set<WebDomainToken>)](/documentation/deviceactivity/deviceactivityfilter/init(segment:users:devices:applications:categories:webdomains:))

### Instance Properties

- [var applications: Set<ApplicationToken>](/documentation/deviceactivity/deviceactivityfilter/applications)
- [var categories: Set<ActivityCategoryToken>](/documentation/deviceactivity/deviceactivityfilter/categories)
- [let devices: DeviceActivityFilter.Devices?](/documentation/deviceactivity/deviceactivityfilter/devices-swift.property)
- [var segmentInterval: DeviceActivityFilter.SegmentInterval](/documentation/deviceactivity/deviceactivityfilter/segmentinterval-swift.property)
- [let users: DeviceActivityFilter.Users?](/documentation/deviceactivity/deviceactivityfilter/users-swift.property)
- [var webDomains: Set<WebDomainToken>](/documentation/deviceactivity/deviceactivityfilter/webdomains)

### Enumerations

- [DeviceActivityFilter.SegmentInterval](/documentation/deviceactivity/deviceactivityfilter/segmentinterval-swift.enum)

#### Enumeration Cases

- [case daily(during: DateInterval)](/documentation/deviceactivity/deviceactivityfilter/segmentinterval-swift.enum/daily(during:))
- [case hourly(during: DateInterval)](/documentation/deviceactivity/deviceactivityfilter/segmentinterval-swift.enum/hourly(during:))
- [case weekly(during: DateInterval)](/documentation/deviceactivity/deviceactivityfilter/segmentinterval-swift.enum/weekly(during:))
- [DeviceActivityData](/documentation/deviceactivity/deviceactivitydata)

### Accessing device and user information

- [var user: DeviceActivityData.User](/documentation/deviceactivity/deviceactivitydata/user-swift.property)
- [var device: DeviceActivityData.Device](/documentation/deviceactivity/deviceactivitydata/device-swift.property)
- [DeviceActivityData.User](/documentation/deviceactivity/deviceactivitydata/user-swift.struct)

#### Identifying the person

- [var appleID: String?](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/appleid)
- [var nameComponents: PersonNameComponents?](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/namecomponents)

#### Defining the account role

- [var role: DeviceActivityData.User.FamilyRole](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/role)
- [DeviceActivityData.User.FamilyRole](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/familyrole)

##### Defining family roles

- [case individual](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/familyrole/individual)
- [case child](/documentation/deviceactivity/deviceactivitydata/user-swift.struct/familyrole/child)
- [DeviceActivityData.Device](/documentation/deviceactivity/deviceactivitydata/device-swift.struct)

#### Identifying the device

- [var name: String?](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/name)
- [var model: DeviceActivityData.Device.Model](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.property)

#### Defining the device model

- [DeviceActivityData.Device.Model](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.enum)

##### Representing device models

- [case iPhone](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.enum/iphone)
- [case iPad](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.enum/ipad)
- [case iPod](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.enum/ipod)
- [case mac](/documentation/deviceactivity/deviceactivitydata/device-swift.struct/model-swift.enum/mac)

### Managing activity data

- [var activitySegments: DeviceActivityResults<DeviceActivityData.ActivitySegment>](/documentation/deviceactivity/deviceactivitydata/activitysegments)
- [var segmentInterval: DeviceActivityFilter.SegmentInterval](/documentation/deviceactivity/deviceactivitydata/segmentinterval)
- [var lastUpdatedDate: Date](/documentation/deviceactivity/deviceactivitydata/lastupdateddate)
- [DeviceActivityData.ActivitySegment](/documentation/deviceactivity/deviceactivitydata/activitysegment)

#### Defining the segment

- [var dateInterval: DateInterval](/documentation/deviceactivity/deviceactivitydata/activitysegment/dateinterval)

#### Measuring activity

- [var totalActivityDuration: TimeInterval](/documentation/deviceactivity/deviceactivitydata/activitysegment/totalactivityduration)
- [var longestActivity: DateInterval?](/documentation/deviceactivity/deviceactivitydata/activitysegment/longestactivity)

#### Tracking device usage

- [var firstPickup: Date?](/documentation/deviceactivity/deviceactivitydata/activitysegment/firstpickup)
- [var totalPickupsWithoutApplicationActivity: Int](/documentation/deviceactivity/deviceactivitydata/activitysegment/totalpickupswithoutapplicationactivity)

#### Accessing categorized activity

- [var categories: DeviceActivityResults<DeviceActivityData.CategoryActivity>](/documentation/deviceactivity/deviceactivitydata/activitysegment/categories)

### Organizing activity by type

- [DeviceActivityData.ApplicationActivity](/documentation/deviceactivity/deviceactivitydata/applicationactivity)

#### Identifying the application

- [var application: Application](/documentation/deviceactivity/deviceactivitydata/applicationactivity/application)

#### Measuring activity

- [var totalActivityDuration: TimeInterval](/documentation/deviceactivity/deviceactivitydata/applicationactivity/totalactivityduration)

#### Tracking usage

- [var numberOfPickups: Int](/documentation/deviceactivity/deviceactivitydata/applicationactivity/numberofpickups)
- [var numberOfNotifications: Int](/documentation/deviceactivity/deviceactivitydata/applicationactivity/numberofnotifications)
- [DeviceActivityData.CategoryActivity](/documentation/deviceactivity/deviceactivitydata/categoryactivity)

#### Identifying the category

- [var category: ActivityCategory](/documentation/deviceactivity/deviceactivitydata/categoryactivity/category)

#### Measuring activity

- [var totalActivityDuration: TimeInterval](/documentation/deviceactivity/deviceactivitydata/categoryactivity/totalactivityduration)

#### Accessing contributing activities

- [var applications: DeviceActivityResults<DeviceActivityData.ApplicationActivity>](/documentation/deviceactivity/deviceactivitydata/categoryactivity/applications)
- [var webDomains: DeviceActivityResults<DeviceActivityData.WebDomainActivity>](/documentation/deviceactivity/deviceactivitydata/categoryactivity/webdomains)
- [DeviceActivityData.WebDomainActivity](/documentation/deviceactivity/deviceactivitydata/webdomainactivity)

#### Identifying the web domain

- [var webDomain: WebDomain](/documentation/deviceactivity/deviceactivitydata/webdomainactivity/webdomain)

#### Measuring activity

- [var totalActivityDuration: TimeInterval](/documentation/deviceactivity/deviceactivitydata/webdomainactivity/totalactivityduration)
- [DeviceActivityResults](/documentation/deviceactivity/deviceactivityresults)

### Classes

- [DeviceActivityResults.Iterator](/documentation/deviceactivity/deviceactivityresults/iterator)

#### Instance Methods

- [func next() async -> IteratorElement?](/documentation/deviceactivity/deviceactivityresults/iterator/next())

### Instance Methods

- [func makeAsyncIterator() -> DeviceActivityResults<Element>.Iterator<Element>](/documentation/deviceactivity/deviceactivityresults/makeasynciterator())

## Authorize access

- [DeviceActivityAuthorization](/documentation/deviceactivity/deviceactivityauthorization)

### Initializers

- [init()](/documentation/deviceactivity/deviceactivityauthorization/init())

### Type Properties

- [static var authorizedClientIdentifiers: [String]](/documentation/deviceactivity/deviceactivityauthorization/authorizedclientidentifiers)
- [static var isOverridden: Bool](/documentation/deviceactivity/deviceactivityauthorization/isoverridden)
- [static var sharingEnabled: Bool](/documentation/deviceactivity/deviceactivityauthorization/sharingenabled)
- [DeviceActivityAuthorizing](/documentation/deviceactivity/deviceactivityauthorizing)

### Type Properties

- [static var isAuthorized: Bool](/documentation/deviceactivity/deviceactivityauthorizing/isauthorized)

### Type Methods

- [static func isAuthorized(String) -> Bool](/documentation/deviceactivity/deviceactivityauthorizing/isauthorized(_:))

## Handle errors

- [DeviceActivityCenter.MonitoringError](/documentation/deviceactivity/deviceactivitycenter/monitoringerror)

### Checking for Errors

- [case excessiveActivities](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/excessiveactivities)
- [case intervalTooLong](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/intervaltoolong)
- [case intervalTooShort](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/intervaltooshort)
- [case invalidDateComponents](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/invaliddatecomponents)
- [case unauthorized](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/unauthorized)

### Getting the Localized Message

- [var errorDescription: String?](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/errordescription)
- [var recoverySuggestion: String?](/documentation/deviceactivity/deviceactivitycenter/monitoringerror/recoverysuggestion)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
