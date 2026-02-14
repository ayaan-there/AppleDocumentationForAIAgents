# Journaling Suggestions Documentation

Source: https://sosumi.ai/documentation/journalingsuggestions

---
title: Journaling Suggestions
source: https://developer.apple.com/documentation/journalingsuggestions
timestamp: 2026-02-13T18:58:35.154Z
---

## Essentials

- [Journaling Suggestions updates](/documentation/updates/journalingsuggestions)
- [Presenting the suggestions picker and processing a selection](/documentation/journalingsuggestions/presenting-the-suggestions-picker-and-processing-a-selection)
- [com.apple.developer.journal.allow](/documentation/bundleresources/entitlements/com.apple.developer.journal.allow)

## Implementation

- [JournalingSuggestionsPicker](/documentation/journalingsuggestions/journalingsuggestionspicker)

### Creating a suggestions picker

- [init(label: () -> Label, onCompletion: (JournalingSuggestion) async -> Void)](/documentation/journalingsuggestions/journalingsuggestionspicker/init(label:oncompletion:))
- [init(LocalizedStringKey, onCompletion: (JournalingSuggestion) async -> Void)](/documentation/journalingsuggestions/journalingsuggestionspicker/init(_:oncompletion:)-7uxov)
- [init<S>(S, onCompletion: (JournalingSuggestion) async -> Void)](/documentation/journalingsuggestions/journalingsuggestionspicker/init(_:oncompletion:)-4e82p)
- [JournalingSuggestion](/documentation/journalingsuggestions/journalingsuggestion)

### Inspecting suggestion details

- [let date: DateInterval?](/documentation/journalingsuggestions/journalingsuggestion/date)
- [let title: String](/documentation/journalingsuggestions/journalingsuggestion/title)

### Accessing suggestion data by type

- [let items: [JournalingSuggestion.ItemContent]](/documentation/journalingsuggestions/journalingsuggestion/items)
- [JournalingSuggestion.ItemContent](/documentation/journalingsuggestions/journalingsuggestion/itemcontent)

#### Identifying item contents

- [var representations: [any JournalingSuggestionAsset.Type]](/documentation/journalingsuggestions/journalingsuggestion/itemcontent/representations)

#### Accessing suggestion data by type

- [func content<Content>(forType: Content.Type) async throws -> Content?](/documentation/journalingsuggestions/journalingsuggestion/itemcontent/content(fortype:))
- [func hasContent<Content>(ofType: Content.Type) -> Bool](/documentation/journalingsuggestions/journalingsuggestion/itemcontent/hascontent(oftype:))
- [func content<Content>(forType: Content.Type) async -> [Content]](/documentation/journalingsuggestions/journalingsuggestion/content(fortype:))

### Interacting with suggestion types

- [JournalingSuggestion.Contact](/documentation/journalingsuggestions/journalingsuggestion/contact)

#### Inspecting contact information

- [var name: String](/documentation/journalingsuggestions/journalingsuggestion/contact/name)
- [let photo: URL?](/documentation/journalingsuggestions/journalingsuggestion/contact/photo)
- [JournalingSuggestion.EventPoster](/documentation/journalingsuggestions/journalingsuggestion/eventposter)

#### Identifying an event

- [var title: AttributedString](/documentation/journalingsuggestions/journalingsuggestion/eventposter/title)
- [var placeName: String?](/documentation/journalingsuggestions/journalingsuggestion/eventposter/placename)
- [var image: URL?](/documentation/journalingsuggestions/journalingsuggestion/eventposter/image)

#### Reviewing event dates

- [var eventEnd: Date?](/documentation/journalingsuggestions/journalingsuggestion/eventposter/eventend)
- [var eventStart: Date?](/documentation/journalingsuggestions/journalingsuggestion/eventposter/eventstart)

#### Distinguishing the organizer

- [var isHost: Bool?](/documentation/journalingsuggestions/journalingsuggestion/eventposter/ishost)
- [JournalingSuggestion.GenericMedia](/documentation/journalingsuggestions/journalingsuggestion/genericmedia)

#### Accessing media data

- [var album: String?](/documentation/journalingsuggestions/journalingsuggestion/genericmedia/album)
- [var appIcon: URL?](/documentation/journalingsuggestions/journalingsuggestion/genericmedia/appicon)
- [var artist: String?](/documentation/journalingsuggestions/journalingsuggestion/genericmedia/artist)
- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/genericmedia/date)
- [var title: String?](/documentation/journalingsuggestions/journalingsuggestion/genericmedia/title)
- [JournalingSuggestion.LivePhoto](/documentation/journalingsuggestions/journalingsuggestion/livephoto)

#### Accessing Live Photo data

- [var image: URL](/documentation/journalingsuggestions/journalingsuggestion/livephoto/image)
- [var video: URL](/documentation/journalingsuggestions/journalingsuggestion/livephoto/video)
- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/livephoto/date)
- [JournalingSuggestion.Location](/documentation/journalingsuggestions/journalingsuggestion/location)

#### Identifying the location

- [var city: String?](/documentation/journalingsuggestions/journalingsuggestion/location/city)
- [var place: String?](/documentation/journalingsuggestions/journalingsuggestion/location/place)

#### Plotting a location geographically

- [var location: CLLocation?](/documentation/journalingsuggestions/journalingsuggestion/location/location)

#### Accessing the visitation date

- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/location/date)

#### Instance Properties

- [var isWorkLocation: Bool?](/documentation/journalingsuggestions/journalingsuggestion/location/isworklocation)
- [var mapKitItemIdentifier: MKMapItem.Identifier?](/documentation/journalingsuggestions/journalingsuggestion/location/mapkititemidentifier)
- [JournalingSuggestion.LocationGroup](/documentation/journalingsuggestions/journalingsuggestion/locationgroup)

#### Accessing individual locations

- [var locations: [JournalingSuggestion.Location]](/documentation/journalingsuggestions/journalingsuggestion/locationgroup/locations)
- [JournalingSuggestion.MotionActivity](/documentation/journalingsuggestions/journalingsuggestion/motionactivity)

#### Accessing motion summary information

- [var icon: URL?](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/icon)
- [var date: DateInterval?](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/date)

#### Inspecting motion details

- [var steps: Int](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/steps)
- [JournalingSuggestion.MotionActivity.MovementType](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/movementtype-swift.struct)

##### Recording movement type

- [static let running: JournalingSuggestion.MotionActivity.MovementType](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/movementtype-swift.struct/running)
- [static let runningWalking: JournalingSuggestion.MotionActivity.MovementType](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/movementtype-swift.struct/runningwalking)
- [static let walking: JournalingSuggestion.MotionActivity.MovementType](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/movementtype-swift.struct/walking)
- [var movementType: JournalingSuggestion.MotionActivity.MovementType?](/documentation/journalingsuggestions/journalingsuggestion/motionactivity/movementtype-swift.property)
- [JournalingSuggestion.Photo](/documentation/journalingsuggestions/journalingsuggestion/photo)

#### Accessing photo data

- [var photo: URL](/documentation/journalingsuggestions/journalingsuggestion/photo/photo)
- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/photo/date)
- [JournalingSuggestion.Podcast](/documentation/journalingsuggestions/journalingsuggestion/podcast)

#### Identifying the podcast

- [var show: String?](/documentation/journalingsuggestions/journalingsuggestion/podcast/show)
- [var episode: String?](/documentation/journalingsuggestions/journalingsuggestion/podcast/episode)
- [var artwork: URL?](/documentation/journalingsuggestions/journalingsuggestion/podcast/artwork)

#### Inspecting interaction details

- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/podcast/date)
- [JournalingSuggestion.Reflection](/documentation/journalingsuggestions/journalingsuggestion/reflection)

#### Identifying a reflection prompt

- [var color: Color?](/documentation/journalingsuggestions/journalingsuggestion/reflection/color)
- [var prompt: String](/documentation/journalingsuggestions/journalingsuggestion/reflection/prompt)
- [JournalingSuggestion.StateOfMind](/documentation/journalingsuggestions/journalingsuggestion/stateofmind)

#### Getting the state of mind data

- [var darkBackground: Gradient?](/documentation/journalingsuggestions/journalingsuggestion/stateofmind/darkbackground)
- [var lightBackground: Gradient?](/documentation/journalingsuggestions/journalingsuggestion/stateofmind/lightbackground)
- [var icon: URL?](/documentation/journalingsuggestions/journalingsuggestion/stateofmind/icon)
- [var state: HKStateOfMind](/documentation/journalingsuggestions/journalingsuggestion/stateofmind/state)
- [JournalingSuggestion.Song](/documentation/journalingsuggestions/journalingsuggestion/song)

#### Identifying the song

- [var song: String?](/documentation/journalingsuggestions/journalingsuggestion/song/song)
- [var artist: String?](/documentation/journalingsuggestions/journalingsuggestion/song/artist)
- [var album: String?](/documentation/journalingsuggestions/journalingsuggestion/song/album)
- [var artwork: URL?](/documentation/journalingsuggestions/journalingsuggestion/song/artwork)

#### Inspecting interaction details

- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/song/date)
- [JournalingSuggestion.Video](/documentation/journalingsuggestions/journalingsuggestion/video)

#### Accessing video data

- [var url: URL](/documentation/journalingsuggestions/journalingsuggestion/video/url)
- [var date: Date?](/documentation/journalingsuggestions/journalingsuggestion/video/date)
- [JournalingSuggestion.Workout](/documentation/journalingsuggestions/journalingsuggestion/workout)

#### Accessing workout summary information

- [var icon: URL?](/documentation/journalingsuggestions/journalingsuggestion/workout/icon)
- [var route: [CLLocation]?](/documentation/journalingsuggestions/journalingsuggestion/workout/route)

#### Inspecting workout details

- [var details: JournalingSuggestion.Workout.Details?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.property)
- [JournalingSuggestion.Workout.Details](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct)

##### Instance Properties

- [var activeEnergyBurned: HKQuantity?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/activeenergyburned)
- [var activityType: HKWorkoutActivityType](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/activitytype)
- [var averageHeartRate: HKQuantity?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/averageheartrate)
- [var date: DateInterval?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/date)
- [var distance: HKQuantity?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/distance)
- [var localizedName: String?](/documentation/journalingsuggestions/journalingsuggestion/workout/details-swift.struct/localizedname)
- [JournalingSuggestion.WorkoutGroup](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup)

#### Accessing workout summary information

- [var icon: URL?](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup/icon)
- [var duration: TimeInterval?](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup/duration)
- [var activeEnergyBurned: HKQuantity?](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup/activeenergyburned)
- [var averageHeartRate: HKQuantity?](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup/averageheartrate)

#### Accessing individual workouts

- [var workouts: [JournalingSuggestion.Workout]](/documentation/journalingsuggestions/journalingsuggestion/workoutgroup/workouts)
- [JournalingSuggestionAsset](/documentation/journalingsuggestions/journalingsuggestionasset)

### Associated Types

- [JournalingSuggestionContent](/documentation/journalingsuggestions/journalingsuggestionasset/journalingsuggestioncontent)

## Notifications

- [Receiving journaling suggestions system notifications](/documentation/journalingsuggestions/receiving-journaling-suggestions-from-system-notifications)
- [JournalingSuggestionPresentationToken](/documentation/journalingsuggestions/journalingsuggestionpresentationtoken)

### Initializing a presentation token

- [init(suggestionIdentifier: UUID?)](/documentation/journalingsuggestions/journalingsuggestionpresentationtoken/init(suggestionidentifier:))
- [JournalingSuggestionsConfiguration](/documentation/journalingsuggestions/journalingsuggestionsconfiguration)

### Initializing a configuration

- [init()](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/init())

### Inspecting the notification schedule

- [var notificationSchedule: JournalingSuggestionsConfiguration.NotificationSchedule?](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/notificationschedule-swift.property)
- [JournalingSuggestionsConfiguration.NotificationSchedule](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/notificationschedule-swift.enum)

#### Identifying a notification schedule

- [case smart](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/notificationschedule-swift.enum/smart)
- [case custom](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/notificationschedule-swift.enum/custom)
- [case off](/documentation/journalingsuggestions/journalingsuggestionsconfiguration/notificationschedule-swift.enum/off)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
