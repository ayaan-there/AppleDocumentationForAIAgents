# LiveCommunicationKit Documentation

Source: https://sosumi.ai/documentation/livecommunicationkit

---
title: LiveCommunicationKit
source: https://developer.apple.com/documentation/livecommunicationkit
timestamp: 2026-02-13T18:58:44.910Z
---

## Essentials

- [Initiating VoIP conversations with LiveCommunicationKit](/documentation/livecommunicationkit/initiating-voip-conversations-with-livecommunicationkit)
- [Preparing your app to be the default dialer app](/documentation/livecommunicationkit/preparing-your-app-to-be-the-default-dialer-app)
- [LiveCommunicationKit updates](/documentation/updates/livecommunicationkit)

## Cellular network conversations

- [TelephonyConversationManager](/documentation/livecommunicationkit/telephonyconversationmanager)

### Starting a conversation

- [func startCellularConversation(StartCellularConversationAction) async throws](/documentation/livecommunicationkit/telephonyconversationmanager/startcellularconversation(_:))
- [static let sharedInstance: TelephonyConversationManager](/documentation/livecommunicationkit/telephonyconversationmanager/sharedinstance)

### Cellular services

- [var cellularServices: [CellularService]](/documentation/livecommunicationkit/telephonyconversationmanager/cellularservices)
- [StartCellularConversationAction](/documentation/livecommunicationkit/startcellularconversationaction)

### Request creation

- [init(Handle, cellularService: CellularService?)](/documentation/livecommunicationkit/startcellularconversationaction/init(_:cellularservice:))
- [init(ConversationHistoryManager.RecentConversation)](/documentation/livecommunicationkit/startcellularconversationaction/init(_:))
- [CellularService](/documentation/livecommunicationkit/cellularservice)

### Attributes

- [let label: String](/documentation/livecommunicationkit/cellularservice/label)
- [let id: UUID](/documentation/livecommunicationkit/cellularservice/id)
- [Handle](/documentation/livecommunicationkit/handle)

### Creation

- [init(type: Handle.Kind, value: String, displayName: String?)](/documentation/livecommunicationkit/handle/init(type:value:displayname:))

### Type

- [var type: Handle.Kind](/documentation/livecommunicationkit/handle/type)
- [Handle.Kind](/documentation/livecommunicationkit/handle/kind)

#### Types

- [case emailAddress](/documentation/livecommunicationkit/handle/kind/emailaddress)
- [case phoneNumber](/documentation/livecommunicationkit/handle/kind/phonenumber)
- [case generic](/documentation/livecommunicationkit/handle/kind/generic)

### Attributes

- [var displayName: String](/documentation/livecommunicationkit/handle/displayname)
- [var value: String](/documentation/livecommunicationkit/handle/value)

## VoIP conversations

- [ConversationManager](/documentation/livecommunicationkit/conversationmanager)

### Creating the manager

- [convenience init(configuration: ConversationManager.Configuration)](/documentation/livecommunicationkit/conversationmanager/init(configuration:))
- [let configuration: ConversationManager.Configuration](/documentation/livecommunicationkit/conversationmanager/configuration-swift.property)
- [ConversationManager.Configuration](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct)

#### Initializers

- [init(ringtoneName: String?, iconTemplateImageData: Data?, maximumConversationGroups: Int, maximumConversationsPerConversationGroup: Int, includesConversationInRecents: Bool, supportsVideo: Bool, supportedHandleTypes: Set<Handle.Kind>)](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/init(ringtonename:icontemplateimagedata:maximumconversationgroups:maximumconversationsperconversationgroup:includesconversationinrecents:supportsvideo:supportedhandletypes:))
- [init(ringtoneName: String?, iconTemplateImageData: Data?, maximumConversationGroups: Int, maximumConversationsPerConversationGroup: Int, includesConversationInRecents: Bool, supportsVideo: Bool, supportedHandleTypes: Set<Handle.Kind>, supportsAudioTranslation: Bool)](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/init(ringtonename:icontemplateimagedata:maximumconversationgroups:maximumconversationsperconversationgroup:includesconversationinrecents:supportsvideo:supportedhandletypes:supportsaudiotranslation:))

#### Configuration options

- [var iconTemplateImageData: Data?](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/icontemplateimagedata)
- [var includesConversationInRecents: Bool](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/includesconversationinrecents)
- [var maximumConversationGroups: Int](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/maximumconversationgroups)
- [var maximumConversationsPerConversationGroup: Int](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/maximumconversationsperconversationgroup)
- [var ringtoneName: String?](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/ringtonename)
- [var supportedHandleTypes: Set<Handle.Kind>](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/supportedhandletypes)
- [var supportsAudioTranslation: Bool](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/supportsaudiotranslation)
- [var supportsVideo: Bool](/documentation/livecommunicationkit/conversationmanager/configuration-swift.struct/supportsvideo)

### Configuring the manager

- [var conversations: [Conversation]](/documentation/livecommunicationkit/conversationmanager/conversations)
- [var pendingActions: [ConversationAction]](/documentation/livecommunicationkit/conversationmanager/pendingactions)
- [var delegate: (any ConversationManagerDelegate)?](/documentation/livecommunicationkit/conversationmanager/delegate)

### Managing conversations

- [func perform([ConversationAction]) async throws](/documentation/livecommunicationkit/conversationmanager/perform(_:))
- [func invalidate()](/documentation/livecommunicationkit/conversationmanager/invalidate())

### Observing conversations

- [func pendingConversationActions(of: ConversationAction.Type, for: Conversation) -> [ConversationAction]](/documentation/livecommunicationkit/conversationmanager/pendingconversationactions(of:for:))
- [func reportConversationEvent(Conversation.Event, for: Conversation)](/documentation/livecommunicationkit/conversationmanager/reportconversationevent(_:for:))
- [func reportNewIncomingConversation(uuid: UUID, update: Conversation.Update) async throws](/documentation/livecommunicationkit/conversationmanager/reportnewincomingconversation(uuid:update:))
- [class func reportNewIncomingVoIPPushPayload([AnyHashable : Any]) async throws](/documentation/livecommunicationkit/conversationmanager/reportnewincomingvoippushpayload(_:))
- [ConversationManagerDelegate](/documentation/livecommunicationkit/conversationmanagerdelegate)

### Observing the conversation manager

- [func conversationManagerDidBegin(ConversationManager)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanagerdidbegin(_:))
- [func conversationManagerDidReset(ConversationManager)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanagerdidreset(_:))

### Receiving status updates

- [func conversationManager(ConversationManager, conversationChanged: Conversation)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanager(_:conversationchanged:))
- [func conversationManager(ConversationManager, didActivate: AVAudioSession)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanager(_:didactivate:))
- [func conversationManager(ConversationManager, didDeactivate: AVAudioSession)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanager(_:diddeactivate:))

### Performing actions

- [func conversationManager(ConversationManager, perform: ConversationAction)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanager(_:perform:))
- [func conversationManager(ConversationManager, timedOutPerforming: ConversationAction)](/documentation/livecommunicationkit/conversationmanagerdelegate/conversationmanager(_:timedoutperforming:))
- [ConversationHistoryManager](/documentation/livecommunicationkit/conversationhistorymanager)

### Accessing the conversation history

- [static let sharedInstance: ConversationHistoryManager](/documentation/livecommunicationkit/conversationhistorymanager/sharedinstance)

### Managing recent conversations

- [func recentConversations(matching: Predicate<ConversationHistoryManager.RecentConversation>) async throws -> [ConversationHistoryManager.RecentConversation]](/documentation/livecommunicationkit/conversationhistorymanager/recentconversations(matching:))
- [func markConversationAsRead(ConversationHistoryManager.RecentConversation) async throws](/documentation/livecommunicationkit/conversationhistorymanager/markconversationasread(_:))
- [func markConversationsAsRead([ConversationHistoryManager.RecentConversation]) async throws](/documentation/livecommunicationkit/conversationhistorymanager/markconversationsasread(_:))
- [ConversationHistoryManager.RecentConversation](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation)

#### Accessing conversation attributes

- [let date: Date](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/date)
- [let direction: ConversationHistoryManager.RecentConversation.Direction](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/direction-swift.property)
- [ConversationHistoryManager.RecentConversation.Direction](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/direction-swift.enum)

##### Conversation direction

- [case incoming](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/direction-swift.enum/incoming)
- [case outgoing](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/direction-swift.enum/outgoing)
- [let duration: TimeInterval](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/duration)
- [let handles: [Handle]](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/handles)
- [let isRead: Bool](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/isread)
- [let status: ConversationHistoryManager.RecentConversation.Status](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.property)
- [ConversationHistoryManager.RecentConversation.Status](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum)

##### Connection status

- [case answeredElsewhere](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum/answeredelsewhere)
- [case cancelled](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum/cancelled)
- [case connected](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum/connected)
- [case missed](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum/missed)
- [case unknown](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/status-swift.enum/unknown)

#### Identifying a recent conversation

- [let id: UUID](/documentation/livecommunicationkit/conversationhistorymanager/recentconversation/id)

### Responding to conversation history updates

- [ConversationHistoryManager.ConversationHistoryDidUpdate](/documentation/livecommunicationkit/conversationhistorymanager/conversationhistorydidupdate)

#### Creating the message

- [init()](/documentation/livecommunicationkit/conversationhistorymanager/conversationhistorydidupdate/init())
- [Conversation](/documentation/livecommunicationkit/conversation)

### Describing a conversation

- [var localMember: Handle?](/documentation/livecommunicationkit/conversation/localmember)
- [var state: Conversation.State](/documentation/livecommunicationkit/conversation/state-swift.property)
- [Conversation.State](/documentation/livecommunicationkit/conversation/state-swift.enum)

#### States

- [case idle](/documentation/livecommunicationkit/conversation/state-swift.enum/idle)
- [case joined](/documentation/livecommunicationkit/conversation/state-swift.enum/joined)
- [case joining](/documentation/livecommunicationkit/conversation/state-swift.enum/joining)
- [case leaving](/documentation/livecommunicationkit/conversation/state-swift.enum/leaving)
- [case left](/documentation/livecommunicationkit/conversation/state-swift.enum/left)
- [case paused](/documentation/livecommunicationkit/conversation/state-swift.enum/paused)
- [let uuid: UUID](/documentation/livecommunicationkit/conversation/uuid)

### Observing a conversation

- [Conversation.Event](/documentation/livecommunicationkit/conversation/event)

#### null

- [case conversationConnected(Date)](/documentation/livecommunicationkit/conversation/event/conversationconnected(_:))
- [case conversationEnded(Date, Conversation.EndedReason)](/documentation/livecommunicationkit/conversation/event/conversationended(_:_:))
- [case conversationStartedConnecting(Date)](/documentation/livecommunicationkit/conversation/event/conversationstartedconnecting(_:))
- [case conversationUpdated(Conversation.Update)](/documentation/livecommunicationkit/conversation/event/conversationupdated(_:))
- [Conversation.EndedReason](/documentation/livecommunicationkit/conversation/endedreason)

#### Reasons

- [case declinedElsewhere](/documentation/livecommunicationkit/conversation/endedreason/declinedelsewhere)
- [case failed](/documentation/livecommunicationkit/conversation/endedreason/failed)
- [case joinedElsewhere](/documentation/livecommunicationkit/conversation/endedreason/joinedelsewhere)
- [case remoteEnded](/documentation/livecommunicationkit/conversation/endedreason/remoteended)
- [case unanswered](/documentation/livecommunicationkit/conversation/endedreason/unanswered)

### Updating a conversation

- [Conversation.Update](/documentation/livecommunicationkit/conversation/update)

#### Initializers

- [init(localMember: Handle?, members: Set<Handle>?, activeRemoteMembers: Set<Handle>?, capabilities: Conversation.Capabilities?)](/documentation/livecommunicationkit/conversation/update/init(localmember:members:activeremotemembers:capabilities:))

#### Attributes

- [var activeRemoteMembers: Set<Handle>?](/documentation/livecommunicationkit/conversation/update/activeremotemembers)
- [var capabilities: Conversation.Capabilities?](/documentation/livecommunicationkit/conversation/update/capabilities)
- [var localMember: Handle?](/documentation/livecommunicationkit/conversation/update/localmember)
- [var members: Set<Handle>?](/documentation/livecommunicationkit/conversation/update/members)
- [Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities)

#### Capabilities

- [static let merging: Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities/merging)
- [static let pausing: Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities/pausing)
- [static let playingTones: Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities/playingtones)
- [static let unmerging: Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities/unmerging)
- [static let video: Conversation.Capabilities](/documentation/livecommunicationkit/conversation/capabilities/video)

## Conversation actions

- [ConversationAction](/documentation/livecommunicationkit/conversationaction)

### Creating an action

- [convenience init(conversationUUID: UUID, timeoutDate: Date)](/documentation/livecommunicationkit/conversationaction/init(conversationuuid:timeoutdate:))

### Completing actions

- [func fulfill()](/documentation/livecommunicationkit/conversationaction/fulfill())
- [func fail()](/documentation/livecommunicationkit/conversationaction/fail())

### Accessing action attributes

- [var conversationUUID: UUID](/documentation/livecommunicationkit/conversationaction/conversationuuid)
- [var uuid: UUID](/documentation/livecommunicationkit/conversationaction/uuid)
- [var timeoutDate: Date](/documentation/livecommunicationkit/conversationaction/timeoutdate)
- [var state: ConversationAction.State](/documentation/livecommunicationkit/conversationaction/state-swift.property)
- [ConversationAction.State](/documentation/livecommunicationkit/conversationaction/state-swift.enum)

#### Constants

- [case complete](/documentation/livecommunicationkit/conversationaction/state-swift.enum/complete)
- [case failed(reason: String)](/documentation/livecommunicationkit/conversationaction/state-swift.enum/failed(reason:))
- [case idle](/documentation/livecommunicationkit/conversationaction/state-swift.enum/idle)
- [case running](/documentation/livecommunicationkit/conversationaction/state-swift.enum/running)
- [EndConversationAction](/documentation/livecommunicationkit/endconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID)](/documentation/livecommunicationkit/endconversationaction/init(conversationuuid:))

### Completing actions

- [func fulfill(dateEnded: Date)](/documentation/livecommunicationkit/endconversationaction/fulfill(dateended:))
- [JoinConversationAction](/documentation/livecommunicationkit/joinconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID)](/documentation/livecommunicationkit/joinconversationaction/init(conversationuuid:))

### Completing actions

- [func fulfill(dateConnected: Date)](/documentation/livecommunicationkit/joinconversationaction/fulfill(dateconnected:))
- [MergeConversationAction](/documentation/livecommunicationkit/mergeconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID, conversationUUIDToMergeWith: UUID)](/documentation/livecommunicationkit/mergeconversationaction/init(conversationuuid:conversationuuidtomergewith:))

### Accessing action attributes

- [let conversationUUIDToMergeWith: UUID](/documentation/livecommunicationkit/mergeconversationaction/conversationuuidtomergewith)
- [MuteConversationAction](/documentation/livecommunicationkit/muteconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID, isMuted: Bool)](/documentation/livecommunicationkit/muteconversationaction/init(conversationuuid:ismuted:))

### Accessing action attributes

- [let isMuted: Bool](/documentation/livecommunicationkit/muteconversationaction/ismuted)
- [PauseConversationAction](/documentation/livecommunicationkit/pauseconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID, isPaused: Bool)](/documentation/livecommunicationkit/pauseconversationaction/init(conversationuuid:ispaused:))

### Accessing action attributes

- [let isPaused: Bool](/documentation/livecommunicationkit/pauseconversationaction/ispaused)
- [PlayToneAction](/documentation/livecommunicationkit/playtoneaction)

### Creating a conversation action

- [init(conversationUUID: UUID, digits: String, tone: PlayToneAction.Tone)](/documentation/livecommunicationkit/playtoneaction/init(conversationuuid:digits:tone:))

### Accessing action attributes

- [let digits: String](/documentation/livecommunicationkit/playtoneaction/digits)
- [let tone: PlayToneAction.Tone](/documentation/livecommunicationkit/playtoneaction/tone-swift.property)
- [PlayToneAction.Tone](/documentation/livecommunicationkit/playtoneaction/tone-swift.enum)

#### Keypad tones

- [case hardPause](/documentation/livecommunicationkit/playtoneaction/tone-swift.enum/hardpause)
- [case single](/documentation/livecommunicationkit/playtoneaction/tone-swift.enum/single)
- [case softPause](/documentation/livecommunicationkit/playtoneaction/tone-swift.enum/softpause)
- [SetTranslatingAction](/documentation/livecommunicationkit/settranslatingaction)

### Creating a conversation action

- [init(conversationID: UUID, isTranslating: Bool, localLanguage: Locale.Language, remoteLanguage: Locale.Language)](/documentation/livecommunicationkit/settranslatingaction/init(conversationid:istranslating:locallanguage:remotelanguage:))

### Accessing action attributes

- [let isTranslating: Bool](/documentation/livecommunicationkit/settranslatingaction/istranslating)
- [let localLanguage: Locale.Language](/documentation/livecommunicationkit/settranslatingaction/locallanguage)
- [let remoteLanguage: Locale.Language](/documentation/livecommunicationkit/settranslatingaction/remotelanguage)

### Completing a translation

- [func fulfill(using: SetTranslatingAction.TranslationEngine)](/documentation/livecommunicationkit/settranslatingaction/fulfill(using:))
- [SetTranslatingAction.TranslationEngine](/documentation/livecommunicationkit/settranslatingaction/translationengine)

#### Types

- [case `default`](/documentation/livecommunicationkit/settranslatingaction/translationengine/default)
- [case custom](/documentation/livecommunicationkit/settranslatingaction/translationengine/custom)
- [StartConversationAction](/documentation/livecommunicationkit/startconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID, handles: [Handle], isVideo: Bool)](/documentation/livecommunicationkit/startconversationaction/init(conversationuuid:handles:isvideo:))

### Accessing action attributes

- [let handles: [Handle]](/documentation/livecommunicationkit/startconversationaction/handles)
- [let isVideo: Bool](/documentation/livecommunicationkit/startconversationaction/isvideo)

### Completing actions

- [func fulfill(dateStarted: Date)](/documentation/livecommunicationkit/startconversationaction/fulfill(datestarted:))
- [UnmergeConversationAction](/documentation/livecommunicationkit/unmergeconversationaction)

### Creating a conversation action

- [init(conversationUUID: UUID)](/documentation/livecommunicationkit/unmergeconversationaction/init(conversationuuid:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
