# Group Activities Documentation

Source: https://sosumi.ai/documentation/groupactivities

---
title: Group Activities
source: https://developer.apple.com/documentation/groupactivities
timestamp: 2026-02-13T18:57:42.455Z
---

## Essentials

- [com.apple.developer.group-session](/documentation/bundleresources/entitlements/com.apple.developer.group-session)

## Activity definition

- [Defining your app’s SharePlay activities](/documentation/groupactivities/defining-your-apps-shareplay-activities)
- [Supporting coordinated media playback](/documentation/avfoundation/supporting-coordinated-media-playback)
- [GroupActivity](/documentation/groupactivities/groupactivity)

### Specifying the activity details

- [static var activityIdentifier: String](/documentation/groupactivities/groupactivity/activityidentifier)
- [var metadata: GroupActivityMetadata](/documentation/groupactivities/groupactivity/metadata)

### Starting an activity immediately

- [func prepareForActivation() async -> GroupActivityActivationResult](/documentation/groupactivities/groupactivity/prepareforactivation())
- [GroupActivityActivationResult](/documentation/groupactivities/groupactivityactivationresult)

#### Getting the activation results

- [case activationPreferred](/documentation/groupactivities/groupactivityactivationresult/activationpreferred)
- [case activationDisabled](/documentation/groupactivities/groupactivityactivationresult/activationdisabled)
- [case cancelled](/documentation/groupactivities/groupactivityactivationresult/cancelled)
- [func activate() async throws -> Bool](/documentation/groupactivities/groupactivity/activate())

### Receiving an activity-related session

- [static func sessions() -> Self.Sessions](/documentation/groupactivities/groupactivity/sessions())
- [GroupActivity.Sessions](/documentation/groupactivities/groupactivity/sessions)

### Transferring data types

- [static var transferRepresentation: some TransferRepresentation](/documentation/groupactivities/groupactivity/transferrepresentation)
- [GroupActivityMetadata](/documentation/groupactivities/groupactivitymetadata)

### Creating group activity metadata

- [init()](/documentation/groupactivities/groupactivitymetadata/init())

### Presenting the activity

- [var title: String?](/documentation/groupactivities/groupactivitymetadata/title)
- [var subtitle: String?](/documentation/groupactivities/groupactivitymetadata/subtitle)
- [var previewImage: CGImage?](/documentation/groupactivities/groupactivitymetadata/previewimage)
- [var fallbackURL: URL?](/documentation/groupactivities/groupactivitymetadata/fallbackurl)

### Indicating the activity’s type

- [var type: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/type)
- [GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype)

#### Getting the Activity Types

- [static let generic: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/generic)
- [static let listenTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/listentogether)
- [static let watchTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/watchtogether)

#### Type Properties

- [static let createTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/createtogether)
- [static let exploreTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/exploretogether)
- [static let learnTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/learntogether)
- [static let readTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/readtogether)
- [static let shopTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/shoptogether)
- [static let workoutTogether: GroupActivityMetadata.ActivityType](/documentation/groupactivities/groupactivitymetadata/activitytype/workouttogether)

### Assigning an app-specific scene

- [var sceneAssociationBehavior: SceneAssociationBehavior](/documentation/groupactivities/groupactivitymetadata/sceneassociationbehavior)
- [SceneAssociationBehavior](/documentation/groupactivities/sceneassociationbehavior)

#### Getting the scene-association options

- [static let `default`: SceneAssociationBehavior](/documentation/groupactivities/sceneassociationbehavior/default)
- [static func content(String) -> SceneAssociationBehavior](/documentation/groupactivities/sceneassociationbehavior/content(_:))
- [static let none: SceneAssociationBehavior](/documentation/groupactivities/sceneassociationbehavior/none)

### Specifying media-related behavior

- [var supportsContinuationOnTV: Bool](/documentation/groupactivities/groupactivitymetadata/supportscontinuationontv)
- [var preferredBroadcastOptions: BroadcastOptions](/documentation/groupactivities/groupactivitymetadata/preferredbroadcastoptions)
- [BroadcastOptions](/documentation/groupactivities/broadcastoptions)

#### Getting the broadcast options

- [static let mirroredVideo: BroadcastOptions](/documentation/groupactivities/broadcastoptions/mirroredvideo)

#### Creating options from a raw value

- [init(rawValue: Int)](/documentation/groupactivities/broadcastoptions/init(rawvalue:))
- [let rawValue: Int](/documentation/groupactivities/broadcastoptions/rawvalue)

### Structures

- [GroupActivityMetadata.LifetimePolicy](/documentation/groupactivities/groupactivitymetadata/lifetimepolicy-swift.struct)

#### Type Properties

- [static let automatic: GroupActivityMetadata.LifetimePolicy](/documentation/groupactivities/groupactivitymetadata/lifetimepolicy-swift.struct/automatic)
- [static let endsWhenInitiatorLeaves: GroupActivityMetadata.LifetimePolicy](/documentation/groupactivities/groupactivitymetadata/lifetimepolicy-swift.struct/endswheninitiatorleaves)

### Instance Properties

- [var experience: GroupActivityMetadata.Experience?](/documentation/groupactivities/groupactivitymetadata/experience-swift.property)
- [var lifetimePolicy: GroupActivityMetadata.LifetimePolicy](/documentation/groupactivities/groupactivitymetadata/lifetimepolicy-swift.property)
- [var localizedSubtitle: String?](/documentation/groupactivities/groupactivitymetadata/localizedsubtitle)
- [var localizedTitle: String?](/documentation/groupactivities/groupactivitymetadata/localizedtitle)

### Enumerations

- [GroupActivityMetadata.Experience](/documentation/groupactivities/groupactivitymetadata/experience-swift.enum)

#### Enumeration Cases

- [case listenTogether](/documentation/groupactivities/groupactivitymetadata/experience-swift.enum/listentogether)
- [case watchTogether](/documentation/groupactivities/groupactivitymetadata/experience-swift.enum/watchtogether)
- [GroupActivityActivationResult](/documentation/groupactivities/groupactivityactivationresult)

### Getting the activation results

- [case activationPreferred](/documentation/groupactivities/groupactivityactivationresult/activationpreferred)
- [case activationDisabled](/documentation/groupactivities/groupactivityactivationresult/activationdisabled)
- [case cancelled](/documentation/groupactivities/groupactivityactivationresult/cancelled)
- [GroupActivityTransferRepresentation](/documentation/groupactivities/groupactivitytransferrepresentation)

### Initializers

- [init<ActivityType>(exporting: (Item) async throws -> ActivityType)](/documentation/groupactivities/groupactivitytransferrepresentation/init(exporting:))

## Interface presentation

- [Presenting SharePlay activities from your app’s UI](/documentation/groupactivities/promoting-shareplay-activities-from-your-apps-ui)
- [GroupActivitySharingController](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk)

### Creating the group activity sharing controller

- [init<ActivityType>(ActivityType) throws](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/init(_:))
- [init<ActivityType>(preparationHandler: () async throws -> ActivityType)](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/init(preparationhandler:))

### Getting the result

- [var result: GroupActivitySharingResult](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/result)
- [GroupActivitySharingResult](/documentation/groupactivities/groupactivitysharingresult-1gln2)

#### Enumeration Cases

- [case cancelled](/documentation/groupactivities/groupactivitysharingresult-1gln2/cancelled)
- [case success](/documentation/groupactivities/groupactivitysharingresult-1gln2/success)

### Responding to view-related events

- [func viewDidLoad()](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/viewdidload())

### Instance Methods

- [func loadView()](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/loadview())
- [func viewWillAppear()](/documentation/groupactivities/groupactivitysharingcontroller-4gtfk/viewwillappear())
- [GroupActivitySharingController](/documentation/groupactivities/groupactivitysharingcontroller-ybcy)

### Creating the group activity sharing controller

- [init<ActivityType>(ActivityType) throws](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/init(_:))
- [init<ActivityType>(preparationHandler: () async throws -> ActivityType)](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/init(preparationhandler:))

### Getting the result

- [var result: GroupActivitySharingResult](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/result)
- [GroupActivitySharingResult](/documentation/groupactivities/groupactivitysharingresult-2ijfu)

#### Getting the result

- [case success](/documentation/groupactivities/groupactivitysharingresult-2ijfu/success)
- [case cancelled](/documentation/groupactivities/groupactivitysharingresult-2ijfu/cancelled)

### Responding to view-related events

- [func viewDidLoad()](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/viewdidload())
- [func viewWillAppear(Bool)](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/viewwillappear(_:))

### Instance Properties

- [var modalPresentationStyle: UIModalPresentationStyle](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/modalpresentationstyle)
- [var preferredContainerBackgroundStyle: UIContainerBackgroundStyle](/documentation/groupactivities/groupactivitysharingcontroller-ybcy/preferredcontainerbackgroundstyle)

## Session management

- [Joining and managing a shared activity](/documentation/groupactivities/joining-and-managing-a-shared-activity)
- [Drawing content in a group session](/documentation/groupactivities/drawing_content_in_a_group_session)
- [GroupSession](/documentation/groupactivities/groupsession)

### Getting the current session

- [GroupSession.Sessions](/documentation/groupactivities/groupsession/sessions)

#### Creating an iterator

- [GroupSession.Sessions.Iterator](/documentation/groupactivities/groupsession/sessions/iterator)

### Joining and leaving the session

- [func join()](/documentation/groupactivities/groupsession/join())
- [func leave()](/documentation/groupactivities/groupsession/leave())
- [func end()](/documentation/groupactivities/groupsession/end())

### Accessing the shared activity

- [var activity: ActivityType](/documentation/groupactivities/groupsession/activity)

### Getting the session details

- [var state: GroupSession<ActivityType>.State](/documentation/groupactivities/groupsession/state-swift.property)
- [GroupSession.State](/documentation/groupactivities/groupsession/state-swift.enum)

#### Session states

- [case waiting](/documentation/groupactivities/groupsession/state-swift.enum/waiting)
- [case joined](/documentation/groupactivities/groupsession/state-swift.enum/joined)
- [case invalidated(reason: any Error)](/documentation/groupactivities/groupsession/state-swift.enum/invalidated(reason:))
- [let id: UUID](/documentation/groupactivities/groupsession/id)

### Getting the participants

- [var localParticipant: Participant](/documentation/groupactivities/groupsession/localparticipant)
- [var activeParticipants: Set<Participant>](/documentation/groupactivities/groupsession/activeparticipants)

### Getting the scene-association identifier

- [var sceneSessionIdentifier: String?](/documentation/groupactivities/groupsession/scenesessionidentifier)

### Getting the participant’s attention

- [func requestForegroundPresentation()](/documentation/groupactivities/groupsession/requestforegroundpresentation())

### Notifying participants of playback changes

- [func showNotice(GroupSessionEvent)](/documentation/groupactivities/groupsession/shownotice(_:))
- [GroupSessionEvent](/documentation/groupactivities/groupsessionevent)

#### Creating a group session event

- [init(originator: Participant, action: GroupSessionEvent.Action, url: URL?)](/documentation/groupactivities/groupsessionevent/init(originator:action:url:))

#### Getting the event details

- [let originator: Participant](/documentation/groupactivities/groupsessionevent/originator)
- [let url: URL?](/documentation/groupactivities/groupsessionevent/url)
- [let action: GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.property)
- [GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct)

##### Getting playback-related actions

- [static let play: GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/play)
- [static let pause: GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/pause)
- [static let seek: GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/seek)
- [static func skip(item: String) -> GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/skip(item:))

##### Getting change-related actions

- [static func updatedQueue(GroupSessionEvent.Action.QueueChange) -> GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/updatedqueue(_:))
- [static let updatedQueue: GroupSessionEvent.Action](/documentation/groupactivities/groupsessionevent/action-swift.struct/updatedqueue)
- [GroupSessionEvent.Action.QueueChange](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange)

###### Specifying the type of change

- [static func added(GroupSessionEvent.Action.QueueChange.Item) -> GroupSessionEvent.Action.QueueChange](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange/added(_:))
- [static func setUpNext(GroupSessionEvent.Action.QueueChange.Item) -> GroupSessionEvent.Action.QueueChange](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange/setupnext(_:))

###### Getting the changed item

- [GroupSessionEvent.Action.QueueChange.Item](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange/item)

###### Creating the item

- [static func song(String) -> GroupSessionEvent.Action.QueueChange.Item](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange/item/song(_:))
- [static func container(String) -> GroupSessionEvent.Action.QueueChange.Item](/documentation/groupactivities/groupsessionevent/action-swift.struct/queuechange/item/container(_:))

### Structures

- [GroupSession.Event](/documentation/groupactivities/groupsession/event)

#### Getting the event details

- [let originator: Participant](/documentation/groupactivities/groupsession/event/originator)

#### Initializers

- [init(originator: Participant, localizedDescription: String)](/documentation/groupactivities/groupsession/event/init(originator:localizeddescription:))

#### Instance Properties

- [var localizedDescription: String](/documentation/groupactivities/groupsession/event/localizeddescription)

### Instance Properties

- [var $activeParticipants: Published<Set<Participant>>.Publisher](/documentation/groupactivities/groupsession/$activeparticipants)
- [var $activity: Published<ActivityType>.Publisher](/documentation/groupactivities/groupsession/$activity)
- [var $state: Published<GroupSession<ActivityType>.State>.Publisher](/documentation/groupactivities/groupsession/$state)
- [let isLocallyInitiated: Bool](/documentation/groupactivities/groupsession/islocallyinitiated)
- [var systemCoordinator: SystemCoordinator?](/documentation/groupactivities/groupsession/systemcoordinator)

### Instance Methods

- [func postEvent(GroupSession<ActivityType>.Event)](/documentation/groupactivities/groupsession/postevent(_:))
- [CustomMessageIdentifiable](/documentation/groupactivities/custommessageidentifiable)

### Type Properties

- [static var messageIdentifier: String](/documentation/groupactivities/custommessageidentifiable/messageidentifier)
- [Participant](/documentation/groupactivities/participant)

### Getting the unique identifier

- [let id: UUID](/documentation/groupactivities/participant/id)

### Instance Properties

- [var isNearbyWithLocalParticipant: Bool](/documentation/groupactivities/participant/isnearbywithlocalparticipant)

## Spatial activities

- [Configure your visionOS app for sharing with people nearby](/documentation/groupactivities/configure-your-app-for-sharing-with-people-nearby)
- [Adding spatial Persona support to an activity](/documentation/groupactivities/adding-spatial-persona-support-to-an-activity)
- [SystemCoordinator](/documentation/groupactivities/systemcoordinator)

### Configuring the system coordinator

- [var configuration: SystemCoordinator.Configuration](/documentation/groupactivities/systemcoordinator/configuration-swift.property)
- [SystemCoordinator.Configuration](/documentation/groupactivities/systemcoordinator/configuration-swift.struct)

#### Creating a configuration structure

- [init()](/documentation/groupactivities/systemcoordinator/configuration-swift.struct/init())

#### Specifying spatial position preferences

- [var spatialTemplatePreference: SpatialTemplatePreference](/documentation/groupactivities/systemcoordinator/configuration-swift.struct/spatialtemplatepreference)
- [SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference)

##### Getting the spatial position preferences

- [static let none: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/none)
- [static let sideBySide: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/sidebyside)
- [static let conversational: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/conversational)
- [static func custom(any SpatialTemplate) -> SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/custom(_:))

##### Specifying the distance between content and participants

- [func contentExtent(CGFloat) -> SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/contentextent(_:))

##### Type Properties

- [static let surround: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/surround)

#### Supporting activities in immersive spaces

- [var supportsGroupImmersiveSpace: Bool](/documentation/groupactivities/systemcoordinator/configuration-swift.struct/supportsgroupimmersivespace)

### Getting the participant state

- [var remoteParticipantStates: [Participant : SystemCoordinator.ParticipantState]](/documentation/groupactivities/systemcoordinator/remoteparticipantstates)
- [var localParticipantState: SystemCoordinator.ParticipantState](/documentation/groupactivities/systemcoordinator/localparticipantstate)
- [var localParticipantStates: SystemCoordinator.ParticipantStates](/documentation/groupactivities/systemcoordinator/localparticipantstates)
- [SystemCoordinator.ParticipantStates](/documentation/groupactivities/systemcoordinator/participantstates)

#### Creating an iterator

- [func makeAsyncIterator() -> SystemCoordinator.ParticipantStates.Iterator](/documentation/groupactivities/systemcoordinator/participantstates/makeasynciterator())
- [SystemCoordinator.ParticipantStates.Iterator](/documentation/groupactivities/systemcoordinator/participantstates/iterator)

##### Instance Methods

- [func next() async -> SystemCoordinator.ParticipantStates.Element?](/documentation/groupactivities/systemcoordinator/participantstates/iterator/next())
- [SystemCoordinator.ParticipantStates.Element](/documentation/groupactivities/systemcoordinator/participantstates/element)

### Getting the current immersion level

- [var groupImmersionStyle: SystemCoordinator.GroupImmersionStyles](/documentation/groupactivities/systemcoordinator/groupimmersionstyle)
- [SystemCoordinator.GroupImmersionStyles](/documentation/groupactivities/systemcoordinator/groupimmersionstyles)

#### Classes

- [SystemCoordinator.GroupImmersionStyles.Iterator](/documentation/groupactivities/systemcoordinator/groupimmersionstyles/iterator)

##### Instance Methods

- [func next() async -> SystemCoordinator.GroupImmersionStyles.Element?](/documentation/groupactivities/systemcoordinator/groupimmersionstyles/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> SystemCoordinator.GroupImmersionStyles.Iterator](/documentation/groupactivities/systemcoordinator/groupimmersionstyles/makeasynciterator())

#### Type Aliases

- [SystemCoordinator.GroupImmersionStyles.Element](/documentation/groupactivities/systemcoordinator/groupimmersionstyles/element)

### Assigning the local participant role

- [func assignRole(some SpatialTemplateRole)](/documentation/groupactivities/systemcoordinator/assignrole(_:))
- [func resignRole()](/documentation/groupactivities/systemcoordinator/resignrole())

### Structures

- [SystemCoordinator.ParticipantState](/documentation/groupactivities/systemcoordinator/participantstate)

#### Getting the participant details

- [let isSpatial: Bool](/documentation/groupactivities/systemcoordinator/participantstate/isspatial)

#### Structures

- [SystemCoordinator.ParticipantState.Seat](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct)

##### Instance Properties

- [let pose: Pose3D](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct/pose)
- [let role: (any SpatialTemplateRole)?](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct/role)

#### Instance Properties

- [let pose: Pose3D?](/documentation/groupactivities/systemcoordinator/participantstate/pose)
- [let role: (any SpatialTemplateRole)?](/documentation/groupactivities/systemcoordinator/participantstate/role)
- [let seat: SystemCoordinator.ParticipantState.Seat?](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.property)
- [SystemCoordinator.ParticipantState](/documentation/groupactivities/systemcoordinator/participantstate)

### Getting the participant details

- [let isSpatial: Bool](/documentation/groupactivities/systemcoordinator/participantstate/isspatial)

### Structures

- [SystemCoordinator.ParticipantState.Seat](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct)

#### Instance Properties

- [let pose: Pose3D](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct/pose)
- [let role: (any SpatialTemplateRole)?](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.struct/role)

### Instance Properties

- [let pose: Pose3D?](/documentation/groupactivities/systemcoordinator/participantstate/pose)
- [let role: (any SpatialTemplateRole)?](/documentation/groupactivities/systemcoordinator/participantstate/role)
- [let seat: SystemCoordinator.ParticipantState.Seat?](/documentation/groupactivities/systemcoordinator/participantstate/seat-swift.property)
- [func groupActivityAssociation(GroupActivityAssociationKind?) -> some View](/documentation/swiftui/view/groupactivityassociation(_:))
- [GroupActivityAssociationInteraction](/documentation/groupactivities/groupactivityassociationinteraction)

### Initializers

- [init(associationKind: GroupActivityAssociationKind?)](/documentation/groupactivities/groupactivityassociationinteraction/init(associationkind:))

### Instance Properties

- [var associationKind: GroupActivityAssociationKind?](/documentation/groupactivities/groupactivityassociationinteraction/associationkind)
- [GroupActivityAssociationKind](/documentation/groupactivities/groupactivityassociationkind)

### Type Methods

- [static func primary(String) -> GroupActivityAssociationKind](/documentation/groupactivities/groupactivityassociationkind/primary(_:))

## Custom spatial templates

- [Building a guessing game for visionOS](/documentation/groupactivities/building-a-guessing-game-for-visionos)
- [SpatialTemplate](/documentation/groupactivities/spatialtemplate)

### Configuring the spatial template

- [var configuration: SpatialTemplateConfiguration](/documentation/groupactivities/spatialtemplate/configuration)
- [SpatialTemplateConfiguration](/documentation/groupactivities/spatialtemplateconfiguration)

#### Operators

- [static func == (SpatialTemplateConfiguration, SpatialTemplateConfiguration) -> Bool](/documentation/groupactivities/spatialtemplateconfiguration/==(_:_:))

#### Initializers

- [init(defaultInitiatorRole: (any SpatialTemplateRole)?)](/documentation/groupactivities/spatialtemplateconfiguration/init(defaultinitiatorrole:))

#### Instance Properties

- [let defaultInitiatorRole: (any SpatialTemplateRole)?](/documentation/groupactivities/spatialtemplateconfiguration/defaultinitiatorrole)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/groupactivities/spatialtemplateconfiguration/hash(into:))

### Placing the template seats

- [var elements: [any SpatialTemplateElement]](/documentation/groupactivities/spatialtemplate/elements)
- [SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference)

### Getting the spatial position preferences

- [static let none: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/none)
- [static let sideBySide: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/sidebyside)
- [static let conversational: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/conversational)
- [static func custom(any SpatialTemplate) -> SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/custom(_:))

### Specifying the distance between content and participants

- [func contentExtent(CGFloat) -> SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/contentextent(_:))

### Type Properties

- [static let surround: SpatialTemplatePreference](/documentation/groupactivities/spatialtemplatepreference/surround)
- [SpatialTemplateSeatElement](/documentation/groupactivities/spatialtemplateseatelement)

### Getting the element details

- [let position: SpatialTemplateElementPosition](/documentation/groupactivities/spatialtemplateseatelement/position)
- [let direction: SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateseatelement/direction)
- [let role: (any SpatialTemplateRole)?](/documentation/groupactivities/spatialtemplateseatelement/role)

### Operators

- [static func == (SpatialTemplateSeatElement, SpatialTemplateSeatElement) -> Bool](/documentation/groupactivities/spatialtemplateseatelement/==(_:_:))

### Initializers

- [init(position: SpatialTemplateElementPosition, direction: SpatialTemplateElementDirection, role: (any SpatialTemplateRole)?)](/documentation/groupactivities/spatialtemplateseatelement/init(position:direction:role:))

### Instance Methods

- [func hash(into: inout Hasher)](/documentation/groupactivities/spatialtemplateseatelement/hash(into:))
- [SpatialTemplateElement](/documentation/groupactivities/spatialtemplateelement)

### Creating a seat position

- [static func seat(position: SpatialTemplateElementPosition, direction: SpatialTemplateElementDirection, role: (any SpatialTemplateRole)?) -> Self](/documentation/groupactivities/spatialtemplateelement/seat(position:direction:role:))

### Getting the element details

- [var position: SpatialTemplateElementPosition](/documentation/groupactivities/spatialtemplateelement/position)
- [var direction: SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelement/direction)
- [var role: (any SpatialTemplateRole)?](/documentation/groupactivities/spatialtemplateelement/role)
- [SpatialTemplateElementPosition](/documentation/groupactivities/spatialtemplateelementposition)

### Getting the app’s position

- [static var app: SpatialTemplateElementPosition](/documentation/groupactivities/spatialtemplateelementposition/app)

### Modifying a position

- [func offsetBy(x: Double, z: Double) -> SpatialTemplateElementPosition](/documentation/groupactivities/spatialtemplateelementposition/offsetby(x:z:))
- [SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection)

### Looking at a specific location

- [static func lookingAt(any SpatialTemplateElement) -> SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection/lookingat(_:)-70j0i)
- [static func lookingAt(SpatialTemplateElementPosition) -> SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection/lookingat(_:)-1d7ak)

### Looking along an axis

- [static func alignedWith(appAxis: SpatialTemplateElementAxis) -> SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection/alignedwith(appaxis:))
- [SpatialTemplateElementAxis](/documentation/groupactivities/spatialtemplateelementaxis)

#### Type Properties

- [static let x: SpatialTemplateElementAxis](/documentation/groupactivities/spatialtemplateelementaxis/x)
- [static let z: SpatialTemplateElementAxis](/documentation/groupactivities/spatialtemplateelementaxis/z)

### Rotating the element

- [func rotatedBy(Angle2D) -> SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection/rotatedby(_:))

### Operators

- [static func + (SpatialTemplateElementDirection, Angle2D) -> SpatialTemplateElementDirection](/documentation/groupactivities/spatialtemplateelementdirection/+(_:_:))
- [SpatialTemplateRole](/documentation/groupactivities/spatialtemplaterole)

### Getting the role identifier

- [var roleIdentifier: String](/documentation/groupactivities/spatialtemplaterole/roleidentifier)

## File and data transfer

- [Synchronizing data during a SharePlay activity](/documentation/groupactivities/synchronizing-data-during-a-shareplay-activity)
- [GroupSessionMessenger](/documentation/groupactivities/groupsessionmessenger)

### Creating a group session messenger

- [init<Activity>(session: GroupSession<Activity>)](/documentation/groupactivities/groupsessionmessenger/init(session:))

### Sending data to the group

- [func send(Data, to: Participants) async throws](/documentation/groupactivities/groupsessionmessenger/send(_:to:)-4o52m)
- [func send<Message>(Message, to: Participants) async throws](/documentation/groupactivities/groupsessionmessenger/send(_:to:)-2a4ku)
- [func send(Data, to: Participants, completion: ((any Error)?) -> Void)](/documentation/groupactivities/groupsessionmessenger/send(_:to:completion:)-zufl)
- [func send<Message>(Message, to: Participants, completion: ((any Error)?) -> Void)](/documentation/groupactivities/groupsessionmessenger/send(_:to:completion:)-9e0sn)
- [Participants](/documentation/groupactivities/participants)

#### Getting the set of participants

- [case all](/documentation/groupactivities/participants/all)
- [case only(Set<Participant>)](/documentation/groupactivities/participants/only(_:)-swift.enum.case)
- [static func only(Participant) -> Participants](/documentation/groupactivities/participants/only(_:)-swift.type.method)

### Receiving data from other participants

- [func messages(of: Data.Type) -> GroupSessionMessenger.Messages<Data>](/documentation/groupactivities/groupsessionmessenger/messages(of:)-626qo)
- [func messages<Message>(of: Message.Type) -> GroupSessionMessenger.Messages<Message>](/documentation/groupactivities/groupsessionmessenger/messages(of:)-jvoz)
- [GroupSessionMessenger.Messages](/documentation/groupactivities/groupsessionmessenger/messages)

#### Creating an iterator

- [GroupSessionMessenger.Messages.Iterator](/documentation/groupactivities/groupsessionmessenger/messages/iterator)
- [GroupSessionMessenger.MessageContext](/documentation/groupactivities/groupsessionmessenger/messagecontext)

#### Getting the initiating participant

- [var source: Participant](/documentation/groupactivities/groupsessionmessenger/messagecontext/source)

### Initializers

- [init<Activity>(session: GroupSession<Activity>, deliveryMode: GroupSessionMessenger.DeliveryMode)](/documentation/groupactivities/groupsessionmessenger/init(session:deliverymode:))

### Instance Properties

- [let deliveryMode: GroupSessionMessenger.DeliveryMode](/documentation/groupactivities/groupsessionmessenger/deliverymode-swift.property)

### Enumerations

- [GroupSessionMessenger.DeliveryMode](/documentation/groupactivities/groupsessionmessenger/deliverymode-swift.enum)

#### Getting the delivery mode options

- [case reliable](/documentation/groupactivities/groupsessionmessenger/deliverymode-swift.enum/reliable)
- [case unreliable](/documentation/groupactivities/groupsessionmessenger/deliverymode-swift.enum/unreliable)
- [GroupSessionJournal](/documentation/groupactivities/groupsessionjournal)

### Creating an attachment manager

- [convenience init<Activity>(session: GroupSession<Activity>)](/documentation/groupactivities/groupsessionjournal/init(session:))

### Uploading content to the session

- [func add<ItemType>(ItemType) async throws -> GroupSessionJournal.Attachment](/documentation/groupactivities/groupsessionjournal/add(_:))
- [func add<ItemType, MetadataType>(ItemType, metadata: MetadataType) async throws -> GroupSessionJournal.Attachment](/documentation/groupactivities/groupsessionjournal/add(_:metadata:))

### Downloading content from the session

- [var attachments: GroupSessionJournal.Attachments](/documentation/groupactivities/groupsessionjournal/attachments-swift.property)
- [GroupSessionJournal.Attachments](/documentation/groupactivities/groupsessionjournal/attachments-swift.struct)

#### Creating an iterator

- [func makeAsyncIterator() -> GroupSessionJournal.Attachments.Iterator](/documentation/groupactivities/groupsessionjournal/attachments-swift.struct/makeasynciterator())
- [GroupSessionJournal.Attachments.Iterator](/documentation/groupactivities/groupsessionjournal/attachments-swift.struct/iterator)
- [GroupSessionJournal.Attachments.Element](/documentation/groupactivities/groupsessionjournal/attachments-swift.struct/element)
- [GroupSessionJournal.Attachment](/documentation/groupactivities/groupsessionjournal/attachment)

#### Downloading the attachment data

- [func load<AttachmentType>(AttachmentType.Type) async throws -> AttachmentType](/documentation/groupactivities/groupsessionjournal/attachment/load(_:))
- [func loadMetadata<MetadataType>(of: MetadataType.Type) async throws -> MetadataType](/documentation/groupactivities/groupsessionjournal/attachment/loadmetadata(of:))

#### Identifying the attachment

- [var id: UUID](/documentation/groupactivities/groupsessionjournal/attachment/id)

### Removing content from the session

- [func remove(attachment: GroupSessionJournal.Attachment) async throws](/documentation/groupactivities/groupsessionjournal/remove(attachment:))

## System status

- [GroupStateObserver](/documentation/groupactivities/groupstateobserver)

### Creating a group state observer

- [convenience init()](/documentation/groupactivities/groupstateobserver/init())

### Determining the eligibility for shared activities

- [var isEligibleForGroupSession: Bool](/documentation/groupactivities/groupstateobserver/iseligibleforgroupsession)

### Instance Properties

- [var $isEligibleForGroupSession: Published<Bool>.Publisher](/documentation/groupactivities/groupstateobserver/$iseligibleforgroupsession)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
