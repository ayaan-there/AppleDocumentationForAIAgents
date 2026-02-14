# ActivityKit Documentation

Source: https://sosumi.ai/documentation/activitykit

---
title: ActivityKit
source: https://developer.apple.com/documentation/activitykit
timestamp: 2026-02-13T19:06:36.320Z
---

## Essentials

- [Developing a WidgetKit strategy](/documentation/widgetkit/developing-a-widgetkit-strategy)
- [ActivityKit updates](/documentation/updates/activitykit)

## Starting a Live Activity

- [Displaying live data with Live Activities](/documentation/activitykit/displaying-live-data-with-live-activities)
- [Starting and updating Live Activities with ActivityKit push notifications](/documentation/activitykit/starting-and-updating-live-activities-with-activitykit-push-notifications)
- [Activity](/documentation/activitykit/activity)

### Starting a Live Activity

- [static func request(attributes: Attributes, content: ActivityContent<Activity<Attributes>.ContentState>, pushType: PushType?) throws -> Activity<Attributes>](/documentation/activitykit/activity/request(attributes:content:pushtype:))
- [static func request(attributes: Attributes, content: ActivityContent<Activity<Attributes>.ContentState>, pushType: PushType?, style: ActivityStyle) throws -> Activity<Attributes>](/documentation/activitykit/activity/request(attributes:content:pushtype:style:))
- [static func request(attributes: Attributes, content: ActivityContent<Activity<Attributes>.ContentState>, pushType: PushType?, style: ActivityStyle, alertConfiguration: AlertConfiguration, start: Date) throws -> Activity<Attributes>](/documentation/activitykit/activity/request(attributes:content:pushtype:style:alertconfiguration:start:))
- [static func request(attributes: Attributes, content: ActivityContent<Activity<Attributes>.ContentState>, pushType: PushType?, style: ActivityStyle, alertConfiguration: AlertConfiguration, startDate: Date) throws -> Activity<Attributes>](/documentation/activitykit/activity/request(attributes:content:pushtype:style:alertconfiguration:startdate:))
- [let attributes: Attributes](/documentation/activitykit/activity/attributes)
- [ActivityAttributes](/documentation/activitykit/activityattributes)

#### Dynamic content

- [ContentState](/documentation/activitykit/activityattributes/contentstate)

#### Instance Methods

- [func previewContext(Self.ContentState, isStale: Bool, viewKind: ActivityPreviewViewKind) -> some View](/documentation/activitykit/activityattributes/previewcontext(_:isstale:viewkind:))
- [ActivityStyle](/documentation/activitykit/activitystyle)

#### Style

- [case standard](/documentation/activitykit/activitystyle/standard)
- [case transient](/documentation/activitykit/activitystyle/transient)
- [var content: ActivityContent<Activity<Attributes>.ContentState>](/documentation/activitykit/activity/content)
- [ActivityContent](/documentation/activitykit/activitycontent)

#### Describing a Live Activity

- [init(state: State, staleDate: Date?, relevanceScore: Double)](/documentation/activitykit/activitycontent/init(state:staledate:relevancescore:))
- [let state: State](/documentation/activitykit/activitycontent/state)
- [let staleDate: Date?](/documentation/activitykit/activitycontent/staledate)
- [let relevanceScore: Double](/documentation/activitykit/activitycontent/relevancescore)
- [Activity.ContentState](/documentation/activitykit/activity/contentstate-swift.typealias)
- [PushType](/documentation/activitykit/pushtype)

#### Supporting ActivityKit push notifications

- [static var token: PushType](/documentation/activitykit/pushtype/token)
- [static func channel(String) -> PushType](/documentation/activitykit/pushtype/channel(_:))
- [ActivityAuthorizationError](/documentation/activitykit/activityauthorizationerror)

#### Error codes

- [case attributesTooLarge](/documentation/activitykit/activityauthorizationerror/attributestoolarge)
- [case denied](/documentation/activitykit/activityauthorizationerror/denied)
- [case globalMaximumExceeded](/documentation/activitykit/activityauthorizationerror/globalmaximumexceeded)
- [case malformedActivityIdentifier](/documentation/activitykit/activityauthorizationerror/malformedactivityidentifier)
- [case missingProcessIdentifier](/documentation/activitykit/activityauthorizationerror/missingprocessidentifier)
- [case persistenceFailure](/documentation/activitykit/activityauthorizationerror/persistencefailure)
- [case reconnectNotPermitted](/documentation/activitykit/activityauthorizationerror/reconnectnotpermitted)
- [case targetMaximumExceeded](/documentation/activitykit/activityauthorizationerror/targetmaximumexceeded)
- [case unentitled](/documentation/activitykit/activityauthorizationerror/unentitled)
- [case unsupported](/documentation/activitykit/activityauthorizationerror/unsupported)
- [case unsupportedTarget](/documentation/activitykit/activityauthorizationerror/unsupportedtarget)
- [case visibility](/documentation/activitykit/activityauthorizationerror/visibility)

#### Getting error information

- [var failureReason: String?](/documentation/activitykit/activityauthorizationerror/failurereason)
- [var recoverySuggestion: String?](/documentation/activitykit/activityauthorizationerror/recoverysuggestion)

#### Protocol confirmation

- [var errorCode: Int](/documentation/activitykit/activityauthorizationerror/errorcode)
- [static var errorDomain: String](/documentation/activitykit/activityauthorizationerror/errordomain)

### Updating a Live Activity

- [func update(ActivityContent<Activity<Attributes>.ContentState>) async](/documentation/activitykit/activity/update(_:))
- [func update(ActivityContent<Activity<Attributes>.ContentState>, alertConfiguration: AlertConfiguration?) async](/documentation/activitykit/activity/update(_:alertconfiguration:))
- [AlertConfiguration](/documentation/activitykit/alertconfiguration)

#### Configuring Live Activity alerts

- [init(title: LocalizedStringResource, body: LocalizedStringResource, sound: AlertConfiguration.AlertSound)](/documentation/activitykit/alertconfiguration/init(title:body:sound:))
- [var title: LocalizedStringResource](/documentation/activitykit/alertconfiguration/title)
- [var body: LocalizedStringResource](/documentation/activitykit/alertconfiguration/body)
- [var sound: AlertConfiguration.AlertSound](/documentation/activitykit/alertconfiguration/sound)
- [AlertConfiguration.AlertSound](/documentation/activitykit/alertconfiguration/alertsound)

##### Configuring the alert sound

- [static func named(String) -> AlertConfiguration.AlertSound](/documentation/activitykit/alertconfiguration/alertsound/named(_:))
- [static var `default`: AlertConfiguration.AlertSound](/documentation/activitykit/alertconfiguration/alertsound/default)
- [func update(ActivityContent<Activity<Attributes>.ContentState>, alertConfiguration: AlertConfiguration?, timestamp: Date) async](/documentation/activitykit/activity/update(_:alertconfiguration:timestamp:))

### Ending a Live Activity

- [func end(ActivityContent<Activity<Attributes>.ContentState>?, dismissalPolicy: ActivityUIDismissalPolicy) async](/documentation/activitykit/activity/end(_:dismissalpolicy:))
- [ActivityUIDismissalPolicy](/documentation/activitykit/activityuidismissalpolicy)

#### Dismissing a Live Activity

- [static let `default`: ActivityUIDismissalPolicy](/documentation/activitykit/activityuidismissalpolicy/default)
- [static let immediate: ActivityUIDismissalPolicy](/documentation/activitykit/activityuidismissalpolicy/immediate)
- [static func after(Date) -> ActivityUIDismissalPolicy](/documentation/activitykit/activityuidismissalpolicy/after(_:))
- [func end(ActivityContent<Activity<Attributes>.ContentState>?, dismissalPolicy: ActivityUIDismissalPolicy, timestamp: Date) async](/documentation/activitykit/activity/end(_:dismissalpolicy:timestamp:))

### Observing Live Activity content changes

- [var contentUpdates: Activity<Attributes>.ContentUpdates](/documentation/activitykit/activity/contentupdates-swift.property)
- [Activity.ContentUpdates](/documentation/activitykit/activity/contentupdates-swift.struct)

#### Structures

- [Activity.ContentUpdates.Iterator](/documentation/activitykit/activity/contentupdates-swift.struct/iterator)

#### Instance Methods

- [func makeAsyncIterator() -> Activity<Attributes>.ContentUpdates.Iterator](/documentation/activitykit/activity/contentupdates-swift.struct/makeasynciterator())

#### Type Aliases

- [Activity.ContentUpdates.Element](/documentation/activitykit/activity/contentupdates-swift.struct/element)

### Observing the Live Activity life cycle

- [var activityState: ActivityState](/documentation/activitykit/activity/activitystate)
- [ActivityState](/documentation/activitykit/activitystate)

#### Live Activity states

- [case active](/documentation/activitykit/activitystate/active)
- [case dismissed](/documentation/activitykit/activitystate/dismissed)
- [case pending](/documentation/activitykit/activitystate/pending)
- [case stale](/documentation/activitykit/activitystate/stale)
- [case ended](/documentation/activitykit/activitystate/ended)
- [var activityStateUpdates: Activity<Attributes>.ActivityStateUpdates](/documentation/activitykit/activity/activitystateupdates-swift.property)
- [Activity.ActivityStateUpdates](/documentation/activitykit/activity/activitystateupdates-swift.struct)

#### Creating an iterator

- [func makeAsyncIterator() -> Activity<Attributes>.ActivityStateUpdates.Iterator](/documentation/activitykit/activity/activitystateupdates-swift.struct/makeasynciterator())
- [Activity.ActivityStateUpdates.Iterator](/documentation/activitykit/activity/activitystateupdates-swift.struct/iterator)
- [Activity.ActivityStateUpdates.Element](/documentation/activitykit/activity/activitystateupdates-swift.struct/element)

### Using ActivityKit push notifications

- [var pushToken: Data?](/documentation/activitykit/activity/pushtoken)
- [var pushTokenUpdates: Activity<Attributes>.PushTokenUpdates](/documentation/activitykit/activity/pushtokenupdates-swift.property)
- [Activity.PushTokenUpdates](/documentation/activitykit/activity/pushtokenupdates-swift.struct)

#### Creating an iterator

- [func makeAsyncIterator() -> Activity<Attributes>.PushTokenUpdates.Iterator](/documentation/activitykit/activity/pushtokenupdates-swift.struct/makeasynciterator())
- [Activity.PushTokenUpdates.Iterator](/documentation/activitykit/activity/pushtokenupdates-swift.struct/iterator)
- [Activity.PushTokenUpdates.Element](/documentation/activitykit/activity/pushtokenupdates-swift.struct/element)
- [static var pushToStartToken: Data?](/documentation/activitykit/activity/pushtostarttoken)
- [static var pushToStartTokenUpdates: Activity<Attributes>.PushTokenUpdates](/documentation/activitykit/activity/pushtostarttokenupdates)

### Checking user authorization

- [ActivityAuthorizationInfo](/documentation/activitykit/activityauthorizationinfo)

#### Observing Live Activity permission changes

- [var areActivitiesEnabled: Bool](/documentation/activitykit/activityauthorizationinfo/areactivitiesenabled)
- [let activityEnablementUpdates: ActivityAuthorizationInfo.ActivityEnablementUpdates](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.property)
- [ActivityAuthorizationInfo.ActivityEnablementUpdates](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.struct)

##### Creating an iterator

- [func makeAsyncIterator() -> ActivityAuthorizationInfo.ActivityEnablementUpdates.Iterator](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.struct/makeasynciterator())
- [ActivityAuthorizationInfo.ActivityEnablementUpdates.Iterator](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.struct/iterator)

###### Instance Methods

- [func next() async -> Bool?](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.struct/iterator/next())
- [ActivityAuthorizationInfo.ActivityEnablementUpdates.Element](/documentation/activitykit/activityauthorizationinfo/activityenablementupdates-swift.struct/element)
- [init()](/documentation/activitykit/activityauthorizationinfo/init())

#### Observing availability of frequent ActivityKit push notifications

- [var frequentPushesEnabled: Bool](/documentation/activitykit/activityauthorizationinfo/frequentpushesenabled)
- [let frequentPushEnablementUpdates: ActivityAuthorizationInfo.FrequentPushEnablementUpdates](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.property)
- [ActivityAuthorizationInfo.FrequentPushEnablementUpdates](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.struct)

##### Creating an iterator

- [func makeAsyncIterator() -> ActivityAuthorizationInfo.FrequentPushEnablementUpdates.Iterator](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.struct/makeasynciterator())
- [ActivityAuthorizationInfo.FrequentPushEnablementUpdates.Iterator](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.struct/iterator)

###### Instance Methods

- [func next() async -> Bool?](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.struct/iterator/next())
- [ActivityAuthorizationInfo.FrequentPushEnablementUpdates.Element](/documentation/activitykit/activityauthorizationinfo/frequentpushenablementupdates-swift.struct/element)

### Accessing Live Activities

- [static var activities: [Activity<Attributes>]](/documentation/activitykit/activity/activities)
- [static var activityUpdates: Activity<Attributes>.ActivityUpdates](/documentation/activitykit/activity/activityupdates-swift.type.property)
- [Activity.ActivityUpdates](/documentation/activitykit/activity/activityupdates-swift.struct)

#### Creating an iterator

- [func makeAsyncIterator() -> Activity<Attributes>.ActivityUpdates.Iterator](/documentation/activitykit/activity/activityupdates-swift.struct/makeasynciterator())
- [Activity.ActivityUpdates.Iterator](/documentation/activitykit/activity/activityupdates-swift.struct/iterator)
- [Activity.ActivityUpdates.Element](/documentation/activitykit/activity/activityupdates-swift.struct/element)

### Identifying a Live Activity

- [let id: String](/documentation/activitykit/activity/id)
- [let id: String](/documentation/activitykit/activity/id)

### Deprecated

- [Deprecated symbols](/documentation/activitykit/deprecated-symbols)

#### Deprecated

- [static func request(attributes: Attributes, contentState: Activity<Attributes>.ContentState, pushType: PushType?) throws -> Activity<Attributes>](/documentation/activitykit/activity/request(attributes:contentstate:pushtype:))
- [func update(using: Activity<Attributes>.ContentState) async](/documentation/activitykit/activity/update(using:))
- [func update(using: Activity<Attributes>.ContentState, alertConfiguration: AlertConfiguration?) async](/documentation/activitykit/activity/update(using:alertconfiguration:))
- [func end(using: Activity<Attributes>.ContentState?, dismissalPolicy: ActivityUIDismissalPolicy) async](/documentation/activitykit/activity/end(using:dismissalpolicy:))
- [var contentState: Activity<Attributes>.ContentState](/documentation/activitykit/activity/contentstate-swift.property)
- [var contentStateUpdates: Activity<Attributes>.ContentStateUpdates](/documentation/activitykit/activity/contentstateupdates-swift.property)
- [Activity.ContentStateUpdates](/documentation/activitykit/activity/contentstateupdates-swift.struct)

##### Creating an iterator

- [func makeAsyncIterator() -> Activity<Attributes>.ContentStateUpdates.Iterator](/documentation/activitykit/activity/contentstateupdates-swift.struct/makeasynciterator())
- [Activity.ContentStateUpdates.Iterator](/documentation/activitykit/activity/contentstateupdates-swift.struct/iterator)
- [Activity.ContentStateUpdates.Element](/documentation/activitykit/activity/contentstateupdates-swift.struct/element)
- [Emoji Rangers: Supporting Live Activities, interactivity, and animations](/documentation/widgetkit/emoji-rangers-supporting-live-activities-interactivity-and-animations)
- [NSSupportsLiveActivities](/documentation/bundleresources/information-property-list/nssupportsliveactivities)
- [NSSupportsLiveActivitiesFrequentUpdates](/documentation/bundleresources/information-property-list/nssupportsliveactivitiesfrequentupdates)

## User interface

- [Creating custom views for Live Activities](/documentation/activitykit/creating-custom-views-for-live-activities)
- [Adding accessible descriptions to widgets and Live Activities](/documentation/activitykit/adding-accessible-descriptions-to-widgets-and-live-activities)
- [Launching your app from a Live Activity](/documentation/activitykit/launching-your-app-from-a-live-activity)

## Widget ecosystem

- [Creating a widget extension](/documentation/widgetkit/creating-a-widget-extension)
- [Animating data updates in widgets and Live Activities](/documentation/widgetkit/animating-data-updates-in-widgets-and-live-activities)
- [Creating views for widgets, Live Activities, and watch complications](/documentation/widgetkit/creating-views-for-widgets-live-activities-and-watch-complications)
- [Linking to specific app scenes from your widget or Live Activity](/documentation/widgetkit/linking-to-specific-app-scenes-from-your-widget-or-live-activity)
- [WidgetKit](/documentation/widgetkit)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
