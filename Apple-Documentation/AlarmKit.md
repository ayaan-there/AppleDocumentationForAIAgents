# AlarmKit Documentation

Source: https://sosumi.ai/documentation/alarmkit

---
title: AlarmKit
source: https://developer.apple.com/documentation/alarmkit
timestamp: 2026-02-13T19:06:50.197Z
---

## Alarm management

- [Scheduling an alarm with AlarmKit](/documentation/alarmkit/scheduling-an-alarm-with-alarmkit)
- [AlarmManager](/documentation/alarmkit/alarmmanager)

### Creating a shared instance

- [static let shared: AlarmManager](/documentation/alarmkit/alarmmanager/shared)

### Updating an alarm

- [AlarmManager.AlarmUpdates](/documentation/alarmkit/alarmmanager/alarmupdates-swift.struct)

#### Creating an iterator

- [AlarmManager.AlarmUpdates.Iterator](/documentation/alarmkit/alarmmanager/alarmupdates-swift.struct/iterator)

##### Interating a function

- [func next() async -> AlarmManager.AlarmUpdates.Element?](/documentation/alarmkit/alarmmanager/alarmupdates-swift.struct/iterator/next())
- [func makeAsyncIterator() -> AlarmManager.AlarmUpdates.Iterator](/documentation/alarmkit/alarmmanager/alarmupdates-swift.struct/makeasynciterator())
- [AlarmManager.AlarmUpdates.Element](/documentation/alarmkit/alarmmanager/alarmupdates-swift.struct/element)
- [var alarmUpdates: some AsyncSequence<Array<Alarm>, Never>](/documentation/alarmkit/alarmmanager/alarmupdates-swift.property)
- [var alarms: [Alarm]](/documentation/alarmkit/alarmmanager/alarms)

### Scheduling an alarm

- [func schedule<Metadata>(id: Alarm.ID, configuration: AlarmManager.AlarmConfiguration<Metadata>) async throws -> Alarm](/documentation/alarmkit/alarmmanager/schedule(id:configuration:))
- [AlarmManager.AlarmConfiguration](/documentation/alarmkit/alarmmanager/alarmconfiguration)

#### Configuring a scheduled alarm

- [static func alarm(schedule: Alarm.Schedule?, attributes: AlarmAttributes<Metadata>, stopIntent: (any LiveActivityIntent)?, secondaryIntent: (any LiveActivityIntent)?, sound: AlertConfiguration.AlertSound) -> AlarmManager.AlarmConfiguration<Metadata>](/documentation/alarmkit/alarmmanager/alarmconfiguration/alarm(schedule:attributes:stopintent:secondaryintent:sound:))

#### Configuring a countdown

- [init(countdownDuration: Alarm.CountdownDuration?, schedule: Alarm.Schedule?, attributes: AlarmAttributes<Metadata>, stopIntent: (any LiveActivityIntent)?, secondaryIntent: (any LiveActivityIntent)?, sound: AlertConfiguration.AlertSound)](/documentation/alarmkit/alarmmanager/alarmconfiguration/init(countdownduration:schedule:attributes:stopintent:secondaryintent:sound:))
- [static func timer(duration: TimeInterval, attributes: AlarmAttributes<Metadata>, stopIntent: (any LiveActivityIntent)?, secondaryIntent: (any LiveActivityIntent)?, sound: AlertConfiguration.AlertSound) -> AlarmManager.AlarmConfiguration<Metadata>](/documentation/alarmkit/alarmmanager/alarmconfiguration/timer(duration:attributes:stopintent:secondaryintent:sound:))

### Requesting authorization

- [func requestAuthorization() async throws -> AlarmManager.AuthorizationState](/documentation/alarmkit/alarmmanager/requestauthorization())

### Checking authorization status

- [AlarmManager.AlarmAuthorizationStateUpdates](/documentation/alarmkit/alarmmanager/alarmauthorizationstateupdates)

#### Iterating an update

- [AlarmManager.AlarmAuthorizationStateUpdates.Iterator](/documentation/alarmkit/alarmmanager/alarmauthorizationstateupdates/iterator)

##### Instance Methods

- [func next() async -> AlarmManager.AuthorizationState?](/documentation/alarmkit/alarmmanager/alarmauthorizationstateupdates/iterator/next())
- [func makeAsyncIterator() -> AlarmManager.AlarmAuthorizationStateUpdates.Iterator](/documentation/alarmkit/alarmmanager/alarmauthorizationstateupdates/makeasynciterator())
- [AlarmManager.AlarmAuthorizationStateUpdates.Element](/documentation/alarmkit/alarmmanager/alarmauthorizationstateupdates/element)
- [var authorizationUpdates: some AsyncSequence<AlarmManager.AuthorizationState, Never>](/documentation/alarmkit/alarmmanager/authorizationupdates)
- [AlarmManager.AuthorizationState](/documentation/alarmkit/alarmmanager/authorizationstate-swift.enum)

#### Describing an authorization state

- [case authorized](/documentation/alarmkit/alarmmanager/authorizationstate-swift.enum/authorized)
- [case denied](/documentation/alarmkit/alarmmanager/authorizationstate-swift.enum/denied)
- [case notDetermined](/documentation/alarmkit/alarmmanager/authorizationstate-swift.enum/notdetermined)
- [var authorizationState: AlarmManager.AuthorizationState](/documentation/alarmkit/alarmmanager/authorizationstate-swift.property)

### Changing an alarm state

- [func cancel(id: Alarm.ID) throws](/documentation/alarmkit/alarmmanager/cancel(id:))
- [func countdown(id: Alarm.ID) throws](/documentation/alarmkit/alarmmanager/countdown(id:))
- [func pause(id: Alarm.ID) throws](/documentation/alarmkit/alarmmanager/pause(id:))
- [func resume(id: Alarm.ID) throws](/documentation/alarmkit/alarmmanager/resume(id:))
- [func stop(id: Alarm.ID) throws](/documentation/alarmkit/alarmmanager/stop(id:))

### Throwing an error

- [AlarmManager.AlarmError](/documentation/alarmkit/alarmmanager/alarmerror)

#### Checking for alarm limit

- [case maximumLimitReached](/documentation/alarmkit/alarmmanager/alarmerror/maximumlimitreached)
- [Alarm](/documentation/alarmkit/alarm)

### Defining a countdown duration

- [Alarm.CountdownDuration](/documentation/alarmkit/alarm/countdownduration-swift.struct)

#### Creating a countdown duration

- [init(preAlert: TimeInterval?, postAlert: TimeInterval?)](/documentation/alarmkit/alarm/countdownduration-swift.struct/init(prealert:postalert:))
- [var postAlert: TimeInterval?](/documentation/alarmkit/alarm/countdownduration-swift.struct/postalert)
- [var preAlert: TimeInterval?](/documentation/alarmkit/alarm/countdownduration-swift.struct/prealert)
- [var countdownDuration: Alarm.CountdownDuration?](/documentation/alarmkit/alarm/countdownduration-swift.property)
- [var id: UUID](/documentation/alarmkit/alarm/id)
- [Alarm.State](/documentation/alarmkit/alarm/state-swift.enum)

#### Setting alarm states

- [case alerting](/documentation/alarmkit/alarm/state-swift.enum/alerting)
- [case countdown](/documentation/alarmkit/alarm/state-swift.enum/countdown)
- [case paused](/documentation/alarmkit/alarm/state-swift.enum/paused)
- [case scheduled](/documentation/alarmkit/alarm/state-swift.enum/scheduled)
- [var state: Alarm.State](/documentation/alarmkit/alarm/state-swift.property)

### Setting an alarm schedule

- [Alarm.Schedule](/documentation/alarmkit/alarm/schedule-swift.enum)

#### Setting an alarm schedule

- [Alarm.Schedule.Relative](/documentation/alarmkit/alarm/schedule-swift.enum/relative)

##### Creating a scheduled alarm

- [init(time: Alarm.Schedule.Relative.Time, repeats: Alarm.Schedule.Relative.Recurrence)](/documentation/alarmkit/alarm/schedule-swift.enum/relative/init(time:repeats:))
- [Alarm.Schedule.Relative.Time](/documentation/alarmkit/alarm/schedule-swift.enum/relative/time-swift.struct)

###### Creating a scheduled time

- [init(hour: Int, minute: Int)](/documentation/alarmkit/alarm/schedule-swift.enum/relative/time-swift.struct/init(hour:minute:))
- [var hour: Int](/documentation/alarmkit/alarm/schedule-swift.enum/relative/time-swift.struct/hour)
- [var minute: Int](/documentation/alarmkit/alarm/schedule-swift.enum/relative/time-swift.struct/minute)

##### Describing an alarm

- [var repeats: Alarm.Schedule.Relative.Recurrence](/documentation/alarmkit/alarm/schedule-swift.enum/relative/repeats)
- [var time: Alarm.Schedule.Relative.Time](/documentation/alarmkit/alarm/schedule-swift.enum/relative/time-swift.property)
- [Alarm.Schedule.Relative.Recurrence](/documentation/alarmkit/alarm/schedule-swift.enum/relative/recurrence)

###### Recurring alarms

- [case never](/documentation/alarmkit/alarm/schedule-swift.enum/relative/recurrence/never)
- [case weekly([Locale.Weekday])](/documentation/alarmkit/alarm/schedule-swift.enum/relative/recurrence/weekly(_:))
- [case fixed(Date)](/documentation/alarmkit/alarm/schedule-swift.enum/fixed(_:))
- [case relative(Alarm.Schedule.Relative)](/documentation/alarmkit/alarm/schedule-swift.enum/relative(_:))
- [var schedule: Alarm.Schedule?](/documentation/alarmkit/alarm/schedule-swift.property)

## Buttons

- [AlarmButton](/documentation/alarmkit/alarmbutton)

### Creating a button

- [init(text: LocalizedStringResource, textColor: Color, systemImageName: String)](/documentation/alarmkit/alarmbutton/init(text:textcolor:systemimagename:))
- [var systemImageName: String](/documentation/alarmkit/alarmbutton/systemimagename)
- [var textColor: Color](/documentation/alarmkit/alarmbutton/textcolor)
- [var text: LocalizedStringResource](/documentation/alarmkit/alarmbutton/text)

### Encoding and decoding

- [func encode(to: any Encoder) throws](/documentation/alarmkit/alarmbutton/encode(to:))
- [init(from: any Decoder) throws](/documentation/alarmkit/alarmbutton/init(from:))

## Views

- [AlarmPresentation](/documentation/alarmkit/alarmpresentation)

### Defining the alarm UI

- [init(alert: AlarmPresentation.Alert, countdown: AlarmPresentation.Countdown?, paused: AlarmPresentation.Paused?)](/documentation/alarmkit/alarmpresentation/init(alert:countdown:paused:))
- [var alert: AlarmPresentation.Alert](/documentation/alarmkit/alarmpresentation/alert-swift.property)
- [var countdown: AlarmPresentation.Countdown?](/documentation/alarmkit/alarmpresentation/countdown-swift.property)
- [var paused: AlarmPresentation.Paused?](/documentation/alarmkit/alarmpresentation/paused-swift.property)

### Describing an alarm state

- [AlarmPresentation.Alert](/documentation/alarmkit/alarmpresentation/alert-swift.struct)

#### Creating a button

- [init(title: LocalizedStringResource, stopButton: AlarmButton, secondaryButton: AlarmButton?, secondaryButtonBehavior: AlarmPresentation.Alert.SecondaryButtonBehavior?)](/documentation/alarmkit/alarmpresentation/alert-swift.struct/init(title:stopbutton:secondarybutton:secondarybuttonbehavior:))
- [var stopButton: AlarmButton](/documentation/alarmkit/alarmpresentation/alert-swift.struct/stopbutton)
- [var title: LocalizedStringResource](/documentation/alarmkit/alarmpresentation/alert-swift.struct/title)

#### Creating a second button

- [var secondaryButton: AlarmButton?](/documentation/alarmkit/alarmpresentation/alert-swift.struct/secondarybutton)
- [var secondaryButtonBehavior: AlarmPresentation.Alert.SecondaryButtonBehavior?](/documentation/alarmkit/alarmpresentation/alert-swift.struct/secondarybuttonbehavior-swift.property)
- [AlarmPresentation.Alert.SecondaryButtonBehavior](/documentation/alarmkit/alarmpresentation/alert-swift.struct/secondarybuttonbehavior-swift.enum)

##### Enumeration Cases

- [case countdown](/documentation/alarmkit/alarmpresentation/alert-swift.struct/secondarybuttonbehavior-swift.enum/countdown)
- [case custom](/documentation/alarmkit/alarmpresentation/alert-swift.struct/secondarybuttonbehavior-swift.enum/custom)

#### Initializers

- [init(title: LocalizedStringResource, secondaryButton: AlarmButton?, secondaryButtonBehavior: AlarmPresentation.Alert.SecondaryButtonBehavior?)](/documentation/alarmkit/alarmpresentation/alert-swift.struct/init(title:secondarybutton:secondarybuttonbehavior:))
- [AlarmPresentation.Countdown](/documentation/alarmkit/alarmpresentation/countdown-swift.struct)

#### Creates a pause button

- [init(title: LocalizedStringResource, pauseButton: AlarmButton?)](/documentation/alarmkit/alarmpresentation/countdown-swift.struct/init(title:pausebutton:))
- [var pauseButton: AlarmButton?](/documentation/alarmkit/alarmpresentation/countdown-swift.struct/pausebutton)
- [var title: LocalizedStringResource](/documentation/alarmkit/alarmpresentation/countdown-swift.struct/title)
- [AlarmPresentation.Paused](/documentation/alarmkit/alarmpresentation/paused-swift.struct)

#### Creating a resume button

- [init(title: LocalizedStringResource, resumeButton: AlarmButton)](/documentation/alarmkit/alarmpresentation/paused-swift.struct/init(title:resumebutton:))
- [var resumeButton: AlarmButton](/documentation/alarmkit/alarmpresentation/paused-swift.struct/resumebutton)
- [var title: LocalizedStringResource](/documentation/alarmkit/alarmpresentation/paused-swift.struct/title)
- [AlarmPresentationState](/documentation/alarmkit/alarmpresentationstate)

### Creating an alarm state

- [init(alarmID: Alarm.ID, mode: AlarmPresentationState.Mode)](/documentation/alarmkit/alarmpresentationstate/init(alarmid:mode:))
- [var alarmID: Alarm.ID](/documentation/alarmkit/alarmpresentationstate/alarmid)
- [var mode: AlarmPresentationState.Mode](/documentation/alarmkit/alarmpresentationstate/mode-swift.property)
- [AlarmPresentationState.Mode](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum)

#### Creating a countdown

- [AlarmPresentationState.Mode.Countdown](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown)

##### Creating a countdown

- [init(totalCountdownDuration: TimeInterval, previouslyElapsedDuration: TimeInterval, startDate: Date, fireDate: Date)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown/init(totalcountdownduration:previouslyelapsedduration:startdate:firedate:))
- [var fireDate: Date](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown/firedate)
- [var previouslyElapsedDuration: TimeInterval](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown/previouslyelapsedduration)
- [var startDate: Date](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown/startdate)
- [var totalCountdownDuration: TimeInterval](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown/totalcountdownduration)
- [case countdown(AlarmPresentationState.Mode.Countdown)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/countdown(_:))

#### Creating an alert

- [AlarmPresentationState.Mode.Alert](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/alert)

##### Creating an alert

- [init(time: Alarm.Schedule.Relative.Time)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/alert/init(time:))
- [var time: Alarm.Schedule.Relative.Time](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/alert/time)
- [case alert(AlarmPresentationState.Mode.Alert)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/alert(_:))

#### Pausing an alarm

- [AlarmPresentationState.Mode.Paused](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/paused)

##### Pausing an alarm

- [init(totalCountdownDuration: TimeInterval, previouslyElapsedDuration: TimeInterval)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/paused/init(totalcountdownduration:previouslyelapsedduration:))
- [var previouslyElapsedDuration: TimeInterval](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/paused/previouslyelapsedduration)
- [var totalCountdownDuration: TimeInterval](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/paused/totalcountdownduration)
- [case paused(AlarmPresentationState.Mode.Paused)](/documentation/alarmkit/alarmpresentationstate/mode-swift.enum/paused(_:))
- [AlarmAttributes](/documentation/alarmkit/alarmattributes)

### Creating an alarm attribute

- [init(presentation: AlarmPresentation, metadata: Metadata?, tintColor: Color)](/documentation/alarmkit/alarmattributes/init(presentation:metadata:tintcolor:))
- [var tintColor: Color](/documentation/alarmkit/alarmattributes/tintcolor)
- [var presentation: AlarmPresentation](/documentation/alarmkit/alarmattributes/presentation)
- [var metadata: Metadata?](/documentation/alarmkit/alarmattributes/metadata)
- [AlarmAttributes.ContentState](/documentation/alarmkit/alarmattributes/contentstate)

### Decoding and encoding

- [init(from: any Decoder) throws](/documentation/alarmkit/alarmattributes/init(from:))
- [func encode(to: any Encoder) throws](/documentation/alarmkit/alarmattributes/encode(to:))
- [AlarmMetadata](/documentation/alarmkit/alarmmetadata)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
