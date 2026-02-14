# XPC Documentation

Source: https://sosumi.ai/documentation/xpc

---
title: XPC
source: https://developer.apple.com/documentation/xpc
timestamp: 2026-02-13T19:04:37.083Z
---

## Essentials

- [XPC updates](/documentation/updates/xpc)

## Interprocess communication

- [Creating XPC services](/documentation/xpc/creating-xpc-services)
- [XPCListener](/documentation/xpc/xpclistener)

### Creating a listener

- [init(service: String, targetQueue: DispatchQueue?, options: XPCListener.InitializationOptions, incomingSessionHandler: (XPCListener.IncomingSessionRequest) -> XPCListener.IncomingSessionRequest.Decision) throws](/documentation/xpc/xpclistener/init(service:targetqueue:options:incomingsessionhandler:))
- [XPCListener.InitializationOptions](/documentation/xpc/xpclistener/initializationoptions)

#### Listener creation options

- [static let inactive: XPCListener.InitializationOptions](/documentation/xpc/xpclistener/initializationoptions/inactive)
- [static let none: XPCListener.InitializationOptions](/documentation/xpc/xpclistener/initializationoptions/none)
- [XPCListener.IncomingSessionRequest](/documentation/xpc/xpclistener/incomingsessionrequest)

#### Responding to client sessions requests

- [func accept<Handler>((XPCSession) -> Handler) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(_:)-73k8w)
- [func accept<Handler>((XPCSession) -> Handler) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(_:)-35eh9)
- [func accept<Handler>((XPCSession) -> Handler) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(_:)-tkrp)
- [func accept<Message>(incomingMessageHandler: (Message) -> (any Encodable)?, cancellationHandler: ((XPCRichError) -> Void)?) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-56fch)
- [func accept(incomingMessageHandler: (XPCReceivedMessage) -> (any Encodable)?, cancellationHandler: ((XPCRichError) -> Void)?) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-9oa3z)
- [func accept(incomingMessageHandler: (XPCDictionary) -> XPCDictionary?, cancellationHandler: ((XPCRichError) -> Void)?) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-8rodk)
- [func accept<Message>(incomingMessageHandler: (Message) -> (any Encodable)?, cancellationHandler: ((XPCRichError) -> Void)?) -> (XPCListener.IncomingSessionRequest.Decision, XPCSession)](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-50tzb)
- [func accept(incomingMessageHandler: (XPCReceivedMessage) -> (any Encodable)?, cancellationHandler: ((XPCRichError) -> Void)?) -> (XPCListener.IncomingSessionRequest.Decision, XPCSession)](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-6oelg)
- [func accept(incomingMessageHandler: (XPCDictionary) -> XPCDictionary?, cancellationHandler: ((XPCRichError) -> Void)?) -> (XPCListener.IncomingSessionRequest.Decision, XPCSession)](/documentation/xpc/xpclistener/incomingsessionrequest/accept(incomingmessagehandler:cancellationhandler:)-48c3k)
- [func reject(reason: String) -> XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/reject(reason:))
- [XPCListener.IncomingSessionRequest.Decision](/documentation/xpc/xpclistener/incomingsessionrequest/decision)

### Managing the life cycle

- [func activate() throws](/documentation/xpc/xpclistener/activate())
- [func cancel()](/documentation/xpc/xpclistener/cancel())

### Handling incoming messages

- [XPCPeerHandler](/documentation/xpc/xpcpeerhandler)

#### Receiving client messages

- [func handleIncomingRequest(Self.Input) -> Self.Output?](/documentation/xpc/xpcpeerhandler/handleincomingrequest(_:))
- [Input](/documentation/xpc/xpcpeerhandler/input)
- [Output](/documentation/xpc/xpcpeerhandler/output)

#### Responding to session cancellation

- [func handleCancellation(error: XPCRichError)](/documentation/xpc/xpcpeerhandler/handlecancellation(error:))

### Initializers

- [convenience init(service: String, targetQueue: DispatchQueue?, options: XPCListener.InitializationOptions, requirement: XPCPeerRequirement, incomingSessionHandler: (XPCListener.IncomingSessionRequest) -> XPCListener.IncomingSessionRequest.Decision) throws](/documentation/xpc/xpclistener/init(service:targetqueue:options:requirement:incomingsessionhandler:))
- [init(targetQueue: DispatchQueue?, options: XPCListener.InitializationOptions, incomingSessionHandler: (XPCListener.IncomingSessionRequest) -> XPCListener.IncomingSessionRequest.Decision)](/documentation/xpc/xpclistener/init(targetqueue:options:incomingsessionhandler:))

### Instance Properties

- [var endpoint: XPCEndpoint](/documentation/xpc/xpclistener/endpoint)
- [XPCSession](/documentation/xpc/xpcsession)

### Creating a session

- [convenience init<Message>(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((Message) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-407h2)
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCReceivedMessage) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-9f4u0)
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCDictionary) -> XPCDictionary?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-bel3)
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:cancellationhandler:))
- [convenience init<Message>(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((Message) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-l3rz)
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCReceivedMessage) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-2xuyi)
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCDictionary) -> XPCDictionary?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:incomingmessagehandler:cancellationhandler:)-6jz7y)
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:cancellationhandler:))
- [XPCSession.InitializationOptions](/documentation/xpc/xpcsession/initializationoptions)

#### Session creation options

- [static let inactive: XPCSession.InitializationOptions](/documentation/xpc/xpcsession/initializationoptions/inactive)
- [static let privileged: XPCSession.InitializationOptions](/documentation/xpc/xpcsession/initializationoptions/privileged)
- [static let none: XPCSession.InitializationOptions](/documentation/xpc/xpcsession/initializationoptions/none)
- [func setTargetQueue(DispatchQueue)](/documentation/xpc/xpcsession/settargetqueue(_:))

### Managing the life cycle

- [func activate() throws](/documentation/xpc/xpcsession/activate())
- [func setIncomingMessageHandler<Message>((Message) -> (any Encodable)?)](/documentation/xpc/xpcsession/setincomingmessagehandler(_:)-2ukdh)
- [func setIncomingMessageHandler((XPCReceivedMessage) -> (any Encodable)?)](/documentation/xpc/xpcsession/setincomingmessagehandler(_:)-5lu26)
- [func setIncomingMessageHandler((XPCDictionary) -> XPCDictionary?)](/documentation/xpc/xpcsession/setincomingmessagehandler(_:)-75ou9)
- [func cancel(reason: String)](/documentation/xpc/xpcsession/cancel(reason:))
- [func setCancellationHandler((XPCRichError) -> Void)](/documentation/xpc/xpcsession/setcancellationhandler(_:))

### Sending messages

- [func send<Message>(Message) throws](/documentation/xpc/xpcsession/send(_:))
- [func send<Message>(Message, replyHandler: (Result<XPCReceivedMessage, XPCRichError>) -> Void) throws](/documentation/xpc/xpcsession/send(_:replyhandler:)-3wjln)
- [func send<Message, Reply>(Message, replyHandler: (Result<Reply, any Error>) -> Void) throws](/documentation/xpc/xpcsession/send(_:replyhandler:)-9an0u)
- [func send(message: XPCDictionary) throws](/documentation/xpc/xpcsession/send(message:))
- [func send(message: XPCDictionary, replyHandler: (Result<XPCDictionary, XPCRichError>) -> Void)](/documentation/xpc/xpcsession/send(message:replyhandler:))
- [func sendSync<Message>(Message) throws -> XPCReceivedMessage](/documentation/xpc/xpcsession/sendsync(_:)-8a284)
- [func sendSync<Message, Reply>(Message) throws -> Reply](/documentation/xpc/xpcsession/sendsync(_:)-88u0s)
- [func sendSync(message: XPCDictionary) throws -> XPCDictionary](/documentation/xpc/xpcsession/sendsync(message:))

### Initializers

- [convenience init(endpoint: XPCEndpoint, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(endpoint:targetqueue:options:cancellationhandler:))
- [convenience init(endpoint: XPCEndpoint, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCDictionary) -> XPCDictionary?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(endpoint:targetqueue:options:incomingmessagehandler:cancellationhandler:)-2jmkk)
- [convenience init(endpoint: XPCEndpoint, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((XPCReceivedMessage) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(endpoint:targetqueue:options:incomingmessagehandler:cancellationhandler:)-546jo)
- [convenience init<Message>(endpoint: XPCEndpoint, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, incomingMessageHandler: ((Message) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(endpoint:targetqueue:options:incomingmessagehandler:cancellationhandler:)-6zd1x)
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:requirement:cancellationhandler:))
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((XPCDictionary) -> XPCDictionary?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-5pk9g)
- [convenience init<Message>(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((Message) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-7o5oq)
- [convenience init(machService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((XPCReceivedMessage) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(machservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-84ll1)
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:requirement:cancellationhandler:))
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((XPCDictionary) -> XPCDictionary?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-3p0jf)
- [convenience init(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((XPCReceivedMessage) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-6jxdc)
- [convenience init<Message>(xpcService: String, targetQueue: DispatchQueue?, options: XPCSession.InitializationOptions, requirement: XPCPeerRequirement, incomingMessageHandler: ((Message) -> (any Encodable)?)?, cancellationHandler: ((XPCRichError) -> Void)?) throws](/documentation/xpc/xpcsession/init(xpcservice:targetqueue:options:requirement:incomingmessagehandler:cancellationhandler:)-osu4)

### Instance Methods

- [func setPeerRequirement(XPCPeerRequirement)](/documentation/xpc/xpcsession/setpeerrequirement(_:))
- [XPCReceivedMessage](/documentation/xpc/xpcreceivedmessage)

### Accessing message content

- [func decode<T>(as: T.Type) throws -> T](/documentation/xpc/xpcreceivedmessage/decode(as:))
- [var isSync: Bool](/documentation/xpc/xpcreceivedmessage/issync)

### Replying to messages

- [var expectsReply: Bool](/documentation/xpc/xpcreceivedmessage/expectsreply)
- [func reply<Message>(Message)](/documentation/xpc/xpcreceivedmessage/reply(_:))
- [func handoffReply(to: DispatchQueue, () -> Void) -> (any Encodable)?](/documentation/xpc/xpcreceivedmessage/handoffreply(to:_:))

### Instance Methods

- [func senderSatisfies(XPCPeerRequirement) -> Bool](/documentation/xpc/xpcreceivedmessage/sendersatisfies(_:))
- [xpc_listener_t](/documentation/xpc/xpc_listener_t)

### Creating a listener

- [xpc_listener_incoming_session_handler_t](/documentation/xpc/xpc_listener_incoming_session_handler_t)

### Working with code signing

- [func xpc_listener_set_peer_code_signing_requirement(xpc_listener_t, UnsafePointer<CChar>) -> Int32](/documentation/xpc/xpc_listener_set_peer_code_signing_requirement(_:_:))
- [xpc_session_t](/documentation/xpc/xpc_session_t-10if0)

### Creating a session

- [xpc_session_t](/documentation/xpc/xpc_session_t-49tiv)
- [func xpc_session_create_mach_service(UnsafePointer<CChar>, dispatch_queue_t?, xpc_session_create_flags_t, AutoreleasingUnsafeMutablePointer<xpc_rich_error_t?>?) -> (any OS_xpc_object)?](/documentation/xpc/xpc_session_create_mach_service(_:_:_:_:))
- [func xpc_session_create_xpc_service(UnsafePointer<CChar>, dispatch_queue_t?, xpc_session_create_flags_t, AutoreleasingUnsafeMutablePointer<xpc_rich_error_t?>?) -> (any OS_xpc_object)?](/documentation/xpc/xpc_session_create_xpc_service(_:_:_:_:))
- [xpc_session_create_flags_t](/documentation/xpc/xpc_session_create_flags_t-swift.struct)

#### Type Properties

- [static let inactive: xpc_session_create_flags_t](/documentation/xpc/xpc_session_create_flags_t-swift.struct/inactive)
- [static let none: xpc_session_create_flags_t](/documentation/xpc/xpc_session_create_flags_t-swift.struct/none)
- [static let privileged: xpc_session_create_flags_t](/documentation/xpc/xpc_session_create_flags_t-swift.struct/privileged)
- [func xpc_session_copy_description(any OS_xpc_object) -> UnsafeMutablePointer<CChar>?](/documentation/xpc/xpc_session_copy_description(_:))
- [func xpc_session_set_target_queue(any OS_xpc_object, dispatch_queue_t?)](/documentation/xpc/xpc_session_set_target_queue(_:_:))

### Managing life cycle

- [func xpc_session_activate(any OS_xpc_object, AutoreleasingUnsafeMutablePointer<xpc_rich_error_t?>?) -> Bool](/documentation/xpc/xpc_session_activate(_:_:))
- [func xpc_session_cancel(any OS_xpc_object)](/documentation/xpc/xpc_session_cancel(_:))
- [func xpc_session_set_cancel_handler(any OS_xpc_object, xpc_session_cancel_handler_t)](/documentation/xpc/xpc_session_set_cancel_handler(_:_:))
- [func xpc_session_set_incoming_message_handler(any OS_xpc_object, xpc_session_incoming_message_handler_t)](/documentation/xpc/xpc_session_set_incoming_message_handler(_:_:))
- [xpc_session_incoming_message_handler_t](/documentation/xpc/xpc_session_incoming_message_handler_t-elj)
- [xpc_session_cancel_handler_t](/documentation/xpc/xpc_session_cancel_handler_t-65b6f)

### Sending messages

- [xpc_rich_error_t](/documentation/xpc/xpc_rich_error_t)
- [func xpc_rich_error_can_retry(xpc_rich_error_t) -> Bool](/documentation/xpc/xpc_rich_error_can_retry(_:))
- [func xpc_rich_error_copy_description(xpc_rich_error_t) -> UnsafeMutablePointer<CChar>?](/documentation/xpc/xpc_rich_error_copy_description(_:))
- [func xpc_session_send_message(any OS_xpc_object, xpc_object_t) -> xpc_rich_error_t?](/documentation/xpc/xpc_session_send_message(_:_:))
- [func xpc_session_send_message_with_reply_async(any OS_xpc_object, xpc_object_t, xpc_session_reply_handler_t)](/documentation/xpc/xpc_session_send_message_with_reply_async(_:_:_:))
- [xpc_session_reply_handler_t](/documentation/xpc/xpc_session_reply_handler_t-2hf7c)
- [func xpc_session_send_message_with_reply_sync(any OS_xpc_object, xpc_object_t, AutoreleasingUnsafeMutablePointer<xpc_rich_error_t?>?) -> xpc_object_t?](/documentation/xpc/xpc_session_send_message_with_reply_sync(_:_:_:))

### Working with code signing

- [func xpc_session_set_peer_code_signing_requirement(xpc_session_t, UnsafePointer<CChar>) -> Int32](/documentation/xpc/xpc_session_set_peer_code_signing_requirement(_:_:))

## Tasks

- [XPC activities](/documentation/xpc/xpc-activities)

### Registration

- [func xpc_activity_register(UnsafePointer<CChar>, xpc_object_t, xpc_activity_handler_t)](/documentation/xpc/xpc_activity_register(_:_:_:))
- [func xpc_activity_unregister(UnsafePointer<CChar>)](/documentation/xpc/xpc_activity_unregister(_:))
- [let XPC_ACTIVITY_CHECK_IN: xpc_object_t](/documentation/xpc/xpc_activity_check_in)
- [xpc_activity_t](/documentation/xpc/xpc_activity_t)
- [xpc_activity_handler_t](/documentation/xpc/xpc_activity_handler_t)

### State

- [func xpc_activity_get_state(xpc_activity_t) -> xpc_activity_state_t](/documentation/xpc/xpc_activity_get_state(_:))
- [func xpc_activity_set_state(xpc_activity_t, xpc_activity_state_t) -> Bool](/documentation/xpc/xpc_activity_set_state(_:_:))
- [func xpc_activity_should_defer(xpc_activity_t) -> Bool](/documentation/xpc/xpc_activity_should_defer(_:))
- [xpc_activity_state_t](/documentation/xpc/xpc-activity-state-t-swift-consts)

#### Constants

- [var XPC_ACTIVITY_STATE_CHECK_IN: Int](/documentation/xpc/xpc_activity_state_check_in)
- [var XPC_ACTIVITY_STATE_CONTINUE: Int](/documentation/xpc/xpc_activity_state_continue)
- [var XPC_ACTIVITY_STATE_DEFER: Int](/documentation/xpc/xpc_activity_state_defer)
- [var XPC_ACTIVITY_STATE_DONE: Int](/documentation/xpc/xpc_activity_state_done)
- [var XPC_ACTIVITY_STATE_RUN: Int](/documentation/xpc/xpc_activity_state_run)
- [var XPC_ACTIVITY_STATE_WAIT: Int](/documentation/xpc/xpc_activity_state_wait)
- [xpc_activity_state_t](/documentation/xpc/xpc_activity_state_t)
- [var XPC_ACTIVITY_STATE_CHECK_IN: Int](/documentation/xpc/xpc_activity_state_check_in)
- [var XPC_ACTIVITY_STATE_WAIT: Int](/documentation/xpc/xpc_activity_state_wait)
- [var XPC_ACTIVITY_STATE_RUN: Int](/documentation/xpc/xpc_activity_state_run)
- [var XPC_ACTIVITY_STATE_DEFER: Int](/documentation/xpc/xpc_activity_state_defer)
- [var XPC_ACTIVITY_STATE_CONTINUE: Int](/documentation/xpc/xpc_activity_state_continue)
- [var XPC_ACTIVITY_STATE_DONE: Int](/documentation/xpc/xpc_activity_state_done)

### Execution criteria

- [func xpc_activity_copy_criteria(xpc_activity_t) -> xpc_object_t?](/documentation/xpc/xpc_activity_copy_criteria(_:))
- [func xpc_activity_set_criteria(xpc_activity_t, xpc_object_t)](/documentation/xpc/xpc_activity_set_criteria(_:_:))

### Scheduling

- [let XPC_ACTIVITY_REPEATING: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_repeating)
- [let XPC_ACTIVITY_DELAY: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_delay)
- [let XPC_ACTIVITY_GRACE_PERIOD: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_grace_period)

### Time Intervals

- [let XPC_ACTIVITY_INTERVAL: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_interval)
- [let XPC_ACTIVITY_INTERVAL_1_MIN: Int64](/documentation/xpc/xpc_activity_interval_1_min)
- [let XPC_ACTIVITY_INTERVAL_5_MIN: Int64](/documentation/xpc/xpc_activity_interval_5_min)
- [let XPC_ACTIVITY_INTERVAL_15_MIN: Int64](/documentation/xpc/xpc_activity_interval_15_min)
- [let XPC_ACTIVITY_INTERVAL_30_MIN: Int64](/documentation/xpc/xpc_activity_interval_30_min)
- [let XPC_ACTIVITY_INTERVAL_1_HOUR: Int64](/documentation/xpc/xpc_activity_interval_1_hour)
- [let XPC_ACTIVITY_INTERVAL_4_HOURS: Int64](/documentation/xpc/xpc_activity_interval_4_hours)
- [let XPC_ACTIVITY_INTERVAL_8_HOURS: Int64](/documentation/xpc/xpc_activity_interval_8_hours)
- [let XPC_ACTIVITY_INTERVAL_1_DAY: Int64](/documentation/xpc/xpc_activity_interval_1_day)
- [let XPC_ACTIVITY_INTERVAL_7_DAYS: Int64](/documentation/xpc/xpc_activity_interval_7_days)

### Priority

- [let XPC_ACTIVITY_PRIORITY: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_priority)
- [let XPC_ACTIVITY_PRIORITY_MAINTENANCE: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_priority_maintenance)
- [let XPC_ACTIVITY_PRIORITY_UTILITY: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_priority_utility)

### Power consumption

- [let XPC_ACTIVITY_ALLOW_BATTERY: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_allow_battery)
- [let XPC_ACTIVITY_REQUIRE_SCREEN_SLEEP: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_require_screen_sleep)
- [let XPC_ACTIVITY_PREVENT_DEVICE_SLEEP: UnsafePointer<CChar>](/documentation/xpc/xpc_activity_prevent_device_sleep)

## Events

- [XPC events](/documentation/xpc/xpc-events)

### Event handling

- [func xpc_set_event_stream_handler(UnsafePointer<CChar>, dispatch_queue_t?, (xpc_object_t) -> Void)](/documentation/xpc/xpc_set_event_stream_handler(_:_:_:))
- [let XPC_EVENT_KEY_NAME: UnsafePointer<CChar>](/documentation/xpc/xpc_event_key_name-swift.var)

## Additional Types

- [XPC objects](/documentation/xpc/xpc-objects)

### Objects

- [xpc_object_t](/documentation/xpc/xpc_object_t)
- [xpc_type_t](/documentation/xpc/xpc_type_t)
- [OS_xpc_object](/documentation/xpc/os_xpc_object)
- [OS_xpc_listener](/documentation/xpc/os_xpc_listener-swift.class)

### Identity

- [func xpc_get_type(xpc_object_t) -> xpc_type_t](/documentation/xpc/xpc_get_type(_:))
- [func xpc_type_get_name(xpc_type_t) -> UnsafePointer<CChar>](/documentation/xpc/xpc_type_get_name(_:))
- [func xpc_hash(xpc_object_t) -> Int](/documentation/xpc/xpc_hash(_:))

### Comparison

- [func xpc_equal(xpc_object_t, xpc_object_t) -> Bool](/documentation/xpc/xpc_equal(_:_:))

### Copying

- [func xpc_copy(xpc_object_t) -> xpc_object_t?](/documentation/xpc/xpc_copy(_:))
- [func xpc_copy_description(xpc_object_t) -> UnsafeMutablePointer<CChar>](/documentation/xpc/xpc_copy_description(_:))

### Boolean objects

- [func xpc_bool_create(Bool) -> xpc_object_t](/documentation/xpc/xpc_bool_create(_:))
- [func xpc_bool_get_value(xpc_object_t) -> Bool](/documentation/xpc/xpc_bool_get_value(_:))
- [var XPC_BOOL_TRUE: xpc_object_t](/documentation/xpc/xpc_bool_true-swift.var)
- [var XPC_BOOL_FALSE: xpc_object_t](/documentation/xpc/xpc_bool_false-swift.var)

### Data objects

- [func xpc_data_create(UnsafeRawPointer?, Int) -> xpc_object_t](/documentation/xpc/xpc_data_create(_:_:))
- [func xpc_data_create_with_dispatch_data(dispatch_data_t) -> xpc_object_t](/documentation/xpc/xpc_data_create_with_dispatch_data(_:))
- [func xpc_data_get_bytes(xpc_object_t, UnsafeMutableRawPointer, Int, Int) -> Int](/documentation/xpc/xpc_data_get_bytes(_:_:_:_:))
- [func xpc_data_get_bytes_ptr(xpc_object_t) -> UnsafeRawPointer?](/documentation/xpc/xpc_data_get_bytes_ptr(_:))
- [func xpc_data_get_length(xpc_object_t) -> Int](/documentation/xpc/xpc_data_get_length(_:))

### Number objects

- [func xpc_double_create(Double) -> xpc_object_t](/documentation/xpc/xpc_double_create(_:))
- [func xpc_double_get_value(xpc_object_t) -> Double](/documentation/xpc/xpc_double_get_value(_:))
- [func xpc_int64_create(Int64) -> xpc_object_t](/documentation/xpc/xpc_int64_create(_:))
- [func xpc_int64_get_value(xpc_object_t) -> Int64](/documentation/xpc/xpc_int64_get_value(_:))
- [func xpc_uint64_create(UInt64) -> xpc_object_t](/documentation/xpc/xpc_uint64_create(_:))
- [func xpc_uint64_get_value(xpc_object_t) -> UInt64](/documentation/xpc/xpc_uint64_get_value(_:))

### Array objects

- [XPCArray](/documentation/xpc/xpcarray)

#### Creating an array

- [init()](/documentation/xpc/xpcarray/init())
- [init(xpc_object_t)](/documentation/xpc/xpcarray/init(_:))
- [func copy(into: XPCArray)](/documentation/xpc/xpcarray/copy(into:))

#### Inspecting an array

- [var isEmpty: Bool](/documentation/xpc/xpcarray/isempty)
- [var count: Int](/documentation/xpc/xpcarray/count)

#### Accessing elements

- [subscript(Int) -> XPCDictionary?](/documentation/xpc/xpcarray/subscript(_:)-1s7qq)
- [subscript(Int) -> String?](/documentation/xpc/xpcarray/subscript(_:)-6c9gh)
- [subscript(Int) -> Bool?](/documentation/xpc/xpcarray/subscript(_:)-i6v5)
- [subscript(Int) -> xpc_object_t?](/documentation/xpc/xpcarray/subscript(_:)-56wjj)
- [subscript<T>(Int) -> T?](/documentation/xpc/xpcarray/subscript(_:)-8wubg)
- [subscript<T>(Int) -> T?](/documentation/xpc/xpcarray/subscript(_:)-9x9ho)
- [subscript<T>(Int) -> T?](/documentation/xpc/xpcarray/subscript(_:)-2f94n)
- [subscript(Int, as _: XPCDictionary.Type) -> XPCDictionary?](/documentation/xpc/xpcarray/subscript(_:as:)-3ae6x)
- [subscript(Int, as _: String.Type) -> String?](/documentation/xpc/xpcarray/subscript(_:as:)-9ukjj)
- [subscript(Int, as _: Bool.Type) -> Bool?](/documentation/xpc/xpcarray/subscript(_:as:)-1bilh)
- [subscript(Int, as _: any OS_xpc_object.Type) -> xpc_object_t?](/documentation/xpc/xpcarray/subscript(_:as:)-931lh)
- [subscript(Int, as _: xpc_type_t) -> xpc_object_t?](/documentation/xpc/xpcarray/subscript(_:as:)-3tgp4)
- [subscript<T>(Int, as _: T.Type) -> T?](/documentation/xpc/xpcarray/subscript(_:as:)-2hql9)
- [subscript<T>(Int, as _: T.Type) -> T?](/documentation/xpc/xpcarray/subscript(_:as:)-6grs4)
- [subscript(Int, as _: Bool.Type, default _: @autoclosure () -> Bool) -> Bool](/documentation/xpc/xpcarray/subscript(_:as:default:)-2bn95)
- [subscript<T>(Int, as _: T.Type, default _: @autoclosure () -> T) -> T](/documentation/xpc/xpcarray/subscript(_:as:default:)-3k2qm)
- [func withUnsafeUnderlyingArray<ReturnType>((xpc_object_t) throws -> ReturnType) rethrows -> ReturnType](/documentation/xpc/xpcarray/withunsafeunderlyingarray(_:))

#### Iterating over an array’s elements

- [func forEach((XPCArray.IndexValuePair) throws -> Void) rethrows](/documentation/xpc/xpcarray/foreach(_:)-6obs3)
- [func forEach((Int, xpc_object_t) throws -> Void) rethrows](/documentation/xpc/xpcarray/foreach(_:)-2ib8a)

#### Transforming an array

- [func map<ReturnType>((XPCArray.IndexValuePair) throws -> ReturnType) rethrows -> [ReturnType]](/documentation/xpc/xpcarray/map(_:))

#### Supporting types

- [XPCArray.IndexValuePair](/documentation/xpc/xpcarray/indexvaluepair)
- [func xpc_array_create(UnsafePointer<xpc_object_t>?, Int) -> xpc_object_t](/documentation/xpc/xpc_array_create(_:_:))
- [func xpc_array_create_empty() -> xpc_object_t](/documentation/xpc/xpc_array_create_empty())
- [func xpc_array_create_connection(xpc_object_t, Int) -> xpc_connection_t?](/documentation/xpc/xpc_array_create_connection(_:_:))
- [func xpc_array_set_value(xpc_object_t, Int, xpc_object_t)](/documentation/xpc/xpc_array_set_value(_:_:_:))
- [func xpc_array_get_value(xpc_object_t, Int) -> xpc_object_t](/documentation/xpc/xpc_array_get_value(_:_:))
- [func xpc_array_append_value(xpc_object_t, xpc_object_t)](/documentation/xpc/xpc_array_append_value(_:_:))
- [func xpc_array_get_count(xpc_object_t) -> Int](/documentation/xpc/xpc_array_get_count(_:))
- [func xpc_array_apply(xpc_object_t, (Int, xpc_object_t) -> Bool) -> Bool](/documentation/xpc/xpc_array_apply(_:_:))
- [func xpc_array_dup_fd(xpc_object_t, Int) -> Int32](/documentation/xpc/xpc_array_dup_fd(_:_:))
- [func xpc_array_get_array(xpc_object_t, Int) -> xpc_object_t?](/documentation/xpc/xpc_array_get_array(_:_:))
- [func xpc_array_get_bool(xpc_object_t, Int) -> Bool](/documentation/xpc/xpc_array_get_bool(_:_:))
- [func xpc_array_get_data(xpc_object_t, Int, UnsafeMutablePointer<Int>?) -> UnsafeRawPointer?](/documentation/xpc/xpc_array_get_data(_:_:_:))
- [func xpc_array_get_date(xpc_object_t, Int) -> Int64](/documentation/xpc/xpc_array_get_date(_:_:))
- [func xpc_array_get_dictionary(xpc_object_t, Int) -> xpc_object_t?](/documentation/xpc/xpc_array_get_dictionary(_:_:))
- [func xpc_array_get_double(xpc_object_t, Int) -> Double](/documentation/xpc/xpc_array_get_double(_:_:))
- [func xpc_array_get_int64(xpc_object_t, Int) -> Int64](/documentation/xpc/xpc_array_get_int64(_:_:))
- [func xpc_array_get_string(xpc_object_t, Int) -> UnsafePointer<CChar>?](/documentation/xpc/xpc_array_get_string(_:_:))
- [func xpc_array_get_uint64(xpc_object_t, Int) -> UInt64](/documentation/xpc/xpc_array_get_uint64(_:_:))
- [func xpc_array_get_uuid(xpc_object_t, Int) -> UnsafePointer<UInt8>?](/documentation/xpc/xpc_array_get_uuid(_:_:))
- [func xpc_array_set_bool(xpc_object_t, Int, Bool)](/documentation/xpc/xpc_array_set_bool(_:_:_:))
- [func xpc_array_set_connection(xpc_object_t, Int, xpc_connection_t)](/documentation/xpc/xpc_array_set_connection(_:_:_:))
- [func xpc_array_set_data(xpc_object_t, Int, UnsafeRawPointer, Int)](/documentation/xpc/xpc_array_set_data(_:_:_:_:))
- [func xpc_array_set_date(xpc_object_t, Int, Int64)](/documentation/xpc/xpc_array_set_date(_:_:_:))
- [func xpc_array_set_double(xpc_object_t, Int, Double)](/documentation/xpc/xpc_array_set_double(_:_:_:))
- [func xpc_array_set_fd(xpc_object_t, Int, Int32)](/documentation/xpc/xpc_array_set_fd(_:_:_:))
- [func xpc_array_set_int64(xpc_object_t, Int, Int64)](/documentation/xpc/xpc_array_set_int64(_:_:_:))
- [func xpc_array_set_string(xpc_object_t, Int, UnsafePointer<CChar>)](/documentation/xpc/xpc_array_set_string(_:_:_:))
- [func xpc_array_set_uint64(xpc_object_t, Int, UInt64)](/documentation/xpc/xpc_array_set_uint64(_:_:_:))
- [func xpc_array_set_uuid(xpc_object_t, Int, UnsafePointer<UInt8>)](/documentation/xpc/xpc_array_set_uuid(_:_:_:))
- [xpc_array_applier_t](/documentation/xpc/xpc_array_applier_t)
- [var XPC_ARRAY_APPEND: size_t](/documentation/xpc/xpc_array_append-swift.var)

### Dictionary objects

- [XPCDictionary](/documentation/xpc/xpcdictionary)

#### Creating a dictionary

- [init()](/documentation/xpc/xpcdictionary/init())
- [init(xpc_object_t)](/documentation/xpc/xpcdictionary/init(_:))
- [func copy(into: XPCDictionary)](/documentation/xpc/xpcdictionary/copy(into:))

#### Replying to client messages

- [func reply(XPCDictionary)](/documentation/xpc/xpcdictionary/reply(_:))

#### Inspecting a dictionary

- [var isEmpty: Bool](/documentation/xpc/xpcdictionary/isempty)
- [var count: Int](/documentation/xpc/xpcdictionary/count)

#### Accessing keys and values

- [var keys: [String]](/documentation/xpc/xpcdictionary/keys)
- [var values: [xpc_object_t]](/documentation/xpc/xpcdictionary/values)
- [subscript(String) -> XPCDictionary?](/documentation/xpc/xpcdictionary/subscript(_:)-4hbmg)
- [subscript(String) -> String?](/documentation/xpc/xpcdictionary/subscript(_:)-80fs2)
- [subscript(String) -> Bool?](/documentation/xpc/xpcdictionary/subscript(_:)-gas6)
- [subscript(String) -> xpc_object_t?](/documentation/xpc/xpcdictionary/subscript(_:)-4j21u)
- [subscript<T>(String) -> T?](/documentation/xpc/xpcdictionary/subscript(_:)-8gyze)
- [subscript<T>(String) -> T?](/documentation/xpc/xpcdictionary/subscript(_:)-4vrsa)
- [subscript<T>(String) -> T?](/documentation/xpc/xpcdictionary/subscript(_:)-3i01t)
- [subscript(String, as _: XPCDictionary.Type) -> XPCDictionary?](/documentation/xpc/xpcdictionary/subscript(_:as:)-1mm7n)
- [subscript(String, as _: String.Type) -> String?](/documentation/xpc/xpcdictionary/subscript(_:as:)-4zxc8)
- [subscript(String, as _: Bool.Type) -> Bool?](/documentation/xpc/xpcdictionary/subscript(_:as:)-18db5)
- [subscript(String, as _: any OS_xpc_object.Type) -> xpc_object_t?](/documentation/xpc/xpcdictionary/subscript(_:as:)-5y39v)
- [subscript(String, as _: xpc_type_t) -> xpc_object_t?](/documentation/xpc/xpcdictionary/subscript(_:as:)-qjxa)
- [subscript<T>(String, as _: T.Type) -> T?](/documentation/xpc/xpcdictionary/subscript(_:as:)-3mzgc)
- [subscript<T>(String, as _: T.Type) -> T?](/documentation/xpc/xpcdictionary/subscript(_:as:)-119cl)
- [subscript(String, as _: Bool.Type, default _: @autoclosure () -> Bool) -> Bool](/documentation/xpc/xpcdictionary/subscript(_:as:default:)-5ufgs)
- [subscript<T>(String, as _: T.Type, default _: @autoclosure () -> T) -> T](/documentation/xpc/xpcdictionary/subscript(_:as:default:)-4ssx3)
- [func withUnsafeUnderlyingDictionary<ReturnType>((xpc_object_t) throws -> ReturnType) rethrows -> ReturnType](/documentation/xpc/xpcdictionary/withunsafeunderlyingdictionary(_:))

#### Removing keys and values

- [func removeValue(forKey: String) -> xpc_object_t?](/documentation/xpc/xpcdictionary/removevalue(forkey:))

#### Supporting types

- [XPCDictionary.KeyValuePair](/documentation/xpc/xpcdictionary/keyvaluepair)

#### Iterating over keys and values

- [func forEach((XPCDictionary.KeyValuePair) throws -> Void) rethrows](/documentation/xpc/xpcdictionary/foreach(_:)-9hufx)
- [func forEach((String, xpc_object_t) throws -> Void) rethrows](/documentation/xpc/xpcdictionary/foreach(_:)-6riqn)

#### Transforming a dictionary

- [func map<ReturnType>((XPCDictionary.KeyValuePair) throws -> ReturnType) rethrows -> [ReturnType]](/documentation/xpc/xpcdictionary/map(_:))

#### Subscripts

- [subscript(String) -> XPCEndpoint?](/documentation/xpc/xpcdictionary/subscript(_:)-2p7tp)
- [subscript(String, as _: XPCEndpoint.Type) -> XPCEndpoint?](/documentation/xpc/xpcdictionary/subscript(_:as:)-7rdzi)
- [func xpc_dictionary_create(UnsafePointer<UnsafePointer<CChar>>?, UnsafePointer<xpc_object_t?>?, Int) -> xpc_object_t](/documentation/xpc/xpc_dictionary_create(_:_:_:))
- [func xpc_dictionary_create_empty() -> xpc_object_t](/documentation/xpc/xpc_dictionary_create_empty())
- [func xpc_dictionary_create_connection(xpc_object_t, UnsafePointer<CChar>) -> xpc_connection_t?](/documentation/xpc/xpc_dictionary_create_connection(_:_:))
- [func xpc_dictionary_create_reply(xpc_object_t) -> xpc_object_t?](/documentation/xpc/xpc_dictionary_create_reply(_:))
- [func xpc_dictionary_set_value(xpc_object_t, UnsafePointer<CChar>, xpc_object_t?)](/documentation/xpc/xpc_dictionary_set_value(_:_:_:))
- [func xpc_dictionary_get_count(xpc_object_t) -> Int](/documentation/xpc/xpc_dictionary_get_count(_:))
- [func xpc_dictionary_get_value(xpc_object_t, UnsafePointer<CChar>) -> xpc_object_t?](/documentation/xpc/xpc_dictionary_get_value(_:_:))
- [func xpc_dictionary_apply(xpc_object_t, (UnsafePointer<CChar>, xpc_object_t) -> Bool) -> Bool](/documentation/xpc/xpc_dictionary_apply(_:_:))
- [func xpc_dictionary_dup_fd(xpc_object_t, UnsafePointer<CChar>) -> Int32](/documentation/xpc/xpc_dictionary_dup_fd(_:_:))
- [func xpc_dictionary_get_array(xpc_object_t, UnsafePointer<CChar>) -> xpc_object_t?](/documentation/xpc/xpc_dictionary_get_array(_:_:))
- [func xpc_dictionary_get_bool(xpc_object_t, UnsafePointer<CChar>) -> Bool](/documentation/xpc/xpc_dictionary_get_bool(_:_:))
- [func xpc_dictionary_get_data(xpc_object_t, UnsafePointer<CChar>, UnsafeMutablePointer<Int>?) -> UnsafeRawPointer?](/documentation/xpc/xpc_dictionary_get_data(_:_:_:))
- [func xpc_dictionary_get_date(xpc_object_t, UnsafePointer<CChar>) -> Int64](/documentation/xpc/xpc_dictionary_get_date(_:_:))
- [func xpc_dictionary_get_dictionary(xpc_object_t, UnsafePointer<CChar>) -> xpc_object_t?](/documentation/xpc/xpc_dictionary_get_dictionary(_:_:))
- [func xpc_dictionary_get_double(xpc_object_t, UnsafePointer<CChar>) -> Double](/documentation/xpc/xpc_dictionary_get_double(_:_:))
- [func xpc_dictionary_get_int64(xpc_object_t, UnsafePointer<CChar>) -> Int64](/documentation/xpc/xpc_dictionary_get_int64(_:_:))
- [func xpc_dictionary_get_remote_connection(xpc_object_t) -> xpc_connection_t?](/documentation/xpc/xpc_dictionary_get_remote_connection(_:))
- [func xpc_dictionary_get_string(xpc_object_t, UnsafePointer<CChar>) -> UnsafePointer<CChar>?](/documentation/xpc/xpc_dictionary_get_string(_:_:))
- [func xpc_dictionary_get_uint64(xpc_object_t, UnsafePointer<CChar>) -> UInt64](/documentation/xpc/xpc_dictionary_get_uint64(_:_:))
- [func xpc_dictionary_get_uuid(xpc_object_t, UnsafePointer<CChar>) -> UnsafePointer<UInt8>?](/documentation/xpc/xpc_dictionary_get_uuid(_:_:))
- [func xpc_dictionary_set_bool(xpc_object_t, UnsafePointer<CChar>, Bool)](/documentation/xpc/xpc_dictionary_set_bool(_:_:_:))
- [func xpc_dictionary_set_connection(xpc_object_t, UnsafePointer<CChar>, xpc_connection_t)](/documentation/xpc/xpc_dictionary_set_connection(_:_:_:))
- [func xpc_dictionary_set_data(xpc_object_t, UnsafePointer<CChar>, UnsafeRawPointer, Int)](/documentation/xpc/xpc_dictionary_set_data(_:_:_:_:))
- [func xpc_dictionary_set_date(xpc_object_t, UnsafePointer<CChar>, Int64)](/documentation/xpc/xpc_dictionary_set_date(_:_:_:))
- [func xpc_dictionary_set_double(xpc_object_t, UnsafePointer<CChar>, Double)](/documentation/xpc/xpc_dictionary_set_double(_:_:_:))
- [func xpc_dictionary_set_fd(xpc_object_t, UnsafePointer<CChar>, Int32)](/documentation/xpc/xpc_dictionary_set_fd(_:_:_:))
- [func xpc_dictionary_set_int64(xpc_object_t, UnsafePointer<CChar>, Int64)](/documentation/xpc/xpc_dictionary_set_int64(_:_:_:))
- [func xpc_dictionary_set_string(xpc_object_t, UnsafePointer<CChar>, UnsafePointer<CChar>)](/documentation/xpc/xpc_dictionary_set_string(_:_:_:))
- [func xpc_dictionary_set_uint64(xpc_object_t, UnsafePointer<CChar>, UInt64)](/documentation/xpc/xpc_dictionary_set_uint64(_:_:_:))
- [func xpc_dictionary_set_uuid(xpc_object_t, UnsafePointer<CChar>, UnsafePointer<UInt8>)](/documentation/xpc/xpc_dictionary_set_uuid(_:_:_:))
- [xpc_dictionary_applier_t](/documentation/xpc/xpc_dictionary_applier_t)
- [func xpc_dictionary_copy_mach_send(xpc_object_t, UnsafePointer<CChar>) -> mach_port_t](/documentation/xpc/xpc_dictionary_copy_mach_send(_:_:))
- [func xpc_dictionary_set_mach_send(xpc_object_t, UnsafePointer<CChar>, mach_port_t)](/documentation/xpc/xpc_dictionary_set_mach_send(_:_:_:))

### String objects

- [func xpc_string_create(UnsafePointer<CChar>) -> xpc_object_t](/documentation/xpc/xpc_string_create(_:))
- [func xpc_string_create_with_format_and_arguments(UnsafePointer<CChar>, CVaListPointer) -> xpc_object_t](/documentation/xpc/xpc_string_create_with_format_and_arguments(_:_:))
- [func xpc_string_get_length(xpc_object_t) -> Int](/documentation/xpc/xpc_string_get_length(_:))
- [func xpc_string_get_string_ptr(xpc_object_t) -> UnsafePointer<CChar>?](/documentation/xpc/xpc_string_get_string_ptr(_:))

### File Descriptor objects

- [func xpc_fd_create(Int32) -> xpc_object_t?](/documentation/xpc/xpc_fd_create(_:))
- [func xpc_fd_dup(xpc_object_t) -> Int32](/documentation/xpc/xpc_fd_dup(_:))

### Date objects

- [func xpc_date_create(Int64) -> xpc_object_t](/documentation/xpc/xpc_date_create(_:))
- [func xpc_date_create_from_current() -> xpc_object_t](/documentation/xpc/xpc_date_create_from_current())
- [func xpc_date_get_value(xpc_object_t) -> Int64](/documentation/xpc/xpc_date_get_value(_:))

### UUID objects

- [func xpc_uuid_create(UnsafePointer<UInt8>) -> xpc_object_t](/documentation/xpc/xpc_uuid_create(_:))
- [func xpc_uuid_get_bytes(xpc_object_t) -> UnsafePointer<UInt8>?](/documentation/xpc/xpc_uuid_get_bytes(_:))

### Shared memory objects

- [func xpc_shmem_create(UnsafeMutableRawPointer, Int) -> xpc_object_t](/documentation/xpc/xpc_shmem_create(_:_:))
- [func xpc_shmem_map(xpc_object_t, UnsafeMutablePointer<UnsafeMutableRawPointer?>) -> Int](/documentation/xpc/xpc_shmem_map(_:_:))

### Null objects

- [func xpc_null_create() -> xpc_object_t](/documentation/xpc/xpc_null_create())

### Object life cycle

- [func xpc_retain(xpc_object_t) -> xpc_object_t](/documentation/xpc/xpc_retain(_:))
- [func xpc_release(xpc_object_t)](/documentation/xpc/xpc_release(_:))

### Types of objects

- [var XPC_TYPE_ACTIVITY: xpc_type_t](/documentation/xpc/xpc_type_activity-swift.var)
- [var XPC_TYPE_ARRAY: xpc_type_t](/documentation/xpc/xpc_type_array-swift.var)
- [var XPC_TYPE_BOOL: xpc_type_t](/documentation/xpc/xpc_type_bool-swift.var)
- [var XPC_TYPE_CONNECTION: xpc_type_t](/documentation/xpc/xpc_type_connection-swift.var)
- [var XPC_TYPE_DATA: xpc_type_t](/documentation/xpc/xpc_type_data-swift.var)
- [var XPC_TYPE_DATE: xpc_type_t](/documentation/xpc/xpc_type_date-swift.var)
- [var XPC_TYPE_DICTIONARY: xpc_type_t](/documentation/xpc/xpc_type_dictionary-swift.var)
- [var XPC_TYPE_DOUBLE: xpc_type_t](/documentation/xpc/xpc_type_double-swift.var)
- [var XPC_TYPE_ENDPOINT: xpc_type_t](/documentation/xpc/xpc_type_endpoint-swift.var)
- [var XPC_TYPE_FD: xpc_type_t](/documentation/xpc/xpc_type_fd-swift.var)
- [var XPC_TYPE_INT64: xpc_type_t](/documentation/xpc/xpc_type_int64-swift.var)
- [var XPC_TYPE_NULL: xpc_type_t](/documentation/xpc/xpc_type_null-swift.var)
- [var XPC_TYPE_SHMEM: xpc_type_t](/documentation/xpc/xpc_type_shmem-swift.var)
- [var XPC_TYPE_STRING: xpc_type_t](/documentation/xpc/xpc_type_string-swift.var)
- [var XPC_TYPE_UINT64: xpc_type_t](/documentation/xpc/xpc_type_uint64-swift.var)
- [var XPC_TYPE_UUID: xpc_type_t](/documentation/xpc/xpc_type_uuid-swift.var)

### Errors

- [XPCRichError](/documentation/xpc/xpcricherror)

#### Error properties

- [var canRetry: Bool](/documentation/xpc/xpcricherror/canretry)
- [var XPC_TYPE_RICH_ERROR: xpc_type_t](/documentation/xpc/xpc_type_rich_error-swift.var)
- [var XPC_TYPE_ERROR: xpc_type_t](/documentation/xpc/xpc_type_error-swift.var)
- [let XPC_ERROR_KEY_DESCRIPTION: UnsafePointer<CChar>](/documentation/xpc/xpc_error_key_description-swift.var)
- [var XPC_ERROR_PEER_CODE_SIGNING_REQUIREMENT: xpc_object_t](/documentation/xpc/xpc_error_peer_code_signing_requirement-swift.var)
- [Utilities](/documentation/xpc/utilities)

### Debug Functions

- [func xpc_debugger_api_misuse_info() -> UnsafePointer<CChar>!](/documentation/xpc/xpc_debugger_api_misuse_info())

### Version Details

- [var XPC_API_VERSION: Int32](/documentation/xpc/xpc_api_version)
- [var IPHONE_SIMULATOR_HOST_MIN_VERSION_REQUIRED: Int32](/documentation/xpc/iphone_simulator_host_min_version_required)
- [XPC connections](/documentation/xpc/xpc-connections)

### Creation

- [xpc_connection_t](/documentation/xpc/xpc_connection_t)
- [func xpc_connection_create(UnsafePointer<CChar>?, dispatch_queue_t?) -> xpc_connection_t](/documentation/xpc/xpc_connection_create(_:_:))
- [func xpc_connection_create_from_endpoint(xpc_endpoint_t) -> xpc_connection_t](/documentation/xpc/xpc_connection_create_from_endpoint(_:))
- [func xpc_connection_create_mach_service(UnsafePointer<CChar>, dispatch_queue_t?, UInt64) -> xpc_connection_t](/documentation/xpc/xpc_connection_create_mach_service(_:_:_:))
- [func xpc_connection_set_target_queue(xpc_connection_t, dispatch_queue_t?)](/documentation/xpc/xpc_connection_set_target_queue(_:_:))
- [var XPC_CONNECTION_MACH_SERVICE_LISTENER: Int32](/documentation/xpc/xpc_connection_mach_service_listener)
- [var XPC_CONNECTION_MACH_SERVICE_PRIVILEGED: Int32](/documentation/xpc/xpc_connection_mach_service_privileged)

### Event handling

- [func xpc_connection_set_event_handler(xpc_connection_t, (xpc_object_t) -> Void)](/documentation/xpc/xpc_connection_set_event_handler(_:_:))
- [xpc_handler_t](/documentation/xpc/xpc_handler_t)
- [xpc_connection_handler_t](/documentation/xpc/xpc_connection_handler_t)

### Life cycle

- [func xpc_main(xpc_connection_handler_t) -> Never](/documentation/xpc/xpc_main(_:))
- [func xpc_connection_activate(xpc_connection_t)](/documentation/xpc/xpc_connection_activate(_:))
- [func xpc_connection_suspend(xpc_connection_t)](/documentation/xpc/xpc_connection_suspend(_:))
- [func xpc_connection_resume(xpc_connection_t)](/documentation/xpc/xpc_connection_resume(_:))
- [func xpc_connection_cancel(xpc_connection_t)](/documentation/xpc/xpc_connection_cancel(_:))
- [func xpc_transaction_begin()](/documentation/xpc/xpc_transaction_begin())
- [func xpc_transaction_end()](/documentation/xpc/xpc_transaction_end())
- [func xpc_connection_copy_invalidation_reason(xpc_connection_t) -> UnsafeMutablePointer<CChar>?](/documentation/xpc/xpc_connection_copy_invalidation_reason(_:))

### Messages

- [func xpc_connection_send_message(xpc_connection_t, xpc_object_t)](/documentation/xpc/xpc_connection_send_message(_:_:))
- [func xpc_connection_send_barrier(xpc_connection_t, () -> Void)](/documentation/xpc/xpc_connection_send_barrier(_:_:))
- [func xpc_connection_send_message_with_reply(xpc_connection_t, xpc_object_t, dispatch_queue_t?, (xpc_object_t) -> Void)](/documentation/xpc/xpc_connection_send_message_with_reply(_:_:_:_:))
- [func xpc_connection_send_message_with_reply_sync(xpc_connection_t, xpc_object_t) -> xpc_object_t](/documentation/xpc/xpc_connection_send_message_with_reply_sync(_:_:))
- [func xpc_main(xpc_connection_handler_t) -> Never](/documentation/xpc/xpc_main(_:))

### Remote peer information

- [func xpc_connection_get_name(xpc_connection_t) -> UnsafePointer<CChar>?](/documentation/xpc/xpc_connection_get_name(_:))
- [func xpc_connection_get_euid(xpc_connection_t) -> uid_t](/documentation/xpc/xpc_connection_get_euid(_:))
- [func xpc_connection_get_egid(xpc_connection_t) -> gid_t](/documentation/xpc/xpc_connection_get_egid(_:))
- [func xpc_connection_get_pid(xpc_connection_t) -> pid_t](/documentation/xpc/xpc_connection_get_pid(_:))
- [func xpc_connection_get_asid(xpc_connection_t) -> au_asid_t](/documentation/xpc/xpc_connection_get_asid(_:))
- [func xpc_connection_set_peer_entitlement_exists_requirement(xpc_connection_t, UnsafePointer<CChar>) -> Int32](/documentation/xpc/xpc_connection_set_peer_entitlement_exists_requirement(_:_:))
- [func xpc_connection_set_peer_entitlement_matches_value_requirement(xpc_connection_t, UnsafePointer<CChar>, xpc_object_t) -> Int32](/documentation/xpc/xpc_connection_set_peer_entitlement_matches_value_requirement(_:_:_:))
- [func xpc_connection_set_peer_lightweight_code_requirement(xpc_connection_t, xpc_object_t) -> Int32](/documentation/xpc/xpc_connection_set_peer_lightweight_code_requirement(_:_:))
- [func xpc_connection_set_peer_platform_identity_requirement(xpc_connection_t, UnsafePointer<CChar>?) -> Int32](/documentation/xpc/xpc_connection_set_peer_platform_identity_requirement(_:_:))
- [func xpc_connection_set_peer_team_identity_requirement(xpc_connection_t, UnsafePointer<CChar>?) -> Int32](/documentation/xpc/xpc_connection_set_peer_team_identity_requirement(_:_:))
- [func xpc_connection_set_peer_code_signing_requirement(xpc_connection_t, UnsafePointer<CChar>) -> Int32](/documentation/xpc/xpc_connection_set_peer_code_signing_requirement(_:_:))

### Context

- [func xpc_connection_set_context(xpc_connection_t, UnsafeMutableRawPointer?)](/documentation/xpc/xpc_connection_set_context(_:_:))
- [func xpc_connection_get_context(xpc_connection_t) -> UnsafeMutableRawPointer?](/documentation/xpc/xpc_connection_get_context(_:))
- [func xpc_connection_set_finalizer_f(xpc_connection_t, xpc_finalizer_t?)](/documentation/xpc/xpc_connection_set_finalizer_f(_:_:))
- [xpc_finalizer_t](/documentation/xpc/xpc_finalizer_t)

### Endpoints

- [func xpc_endpoint_create(xpc_connection_t) -> xpc_endpoint_t](/documentation/xpc/xpc_endpoint_create(_:))
- [xpc_endpoint_t](/documentation/xpc/xpc_endpoint_t)

### Errors

- [var XPC_ERROR_CONNECTION_INVALID: xpc_object_t](/documentation/xpc/xpc_error_connection_invalid-swift.var)
- [var XPC_ERROR_CONNECTION_INTERRUPTED: xpc_object_t](/documentation/xpc/xpc_error_connection_interrupted-swift.var)
- [var XPC_ERROR_TERMINATION_IMMINENT: xpc_object_t](/documentation/xpc/xpc_error_termination_imminent-swift.var)

## Classes

- [OS_xpc_session](/documentation/xpc/os_xpc_session-swift.class)

## Structures

- [XPCEndpoint](/documentation/xpc/xpcendpoint)
- [XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement)

### Initializers

- [init(lightweightCodeRequirements: XPCDictionary)](/documentation/xpc/xpcpeerrequirement/init(lightweightcoderequirements:))

### Type Methods

- [static func codeRequirement(ProcessCodeRequirement) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/coderequirement(_:))
- [static func entitlement(String, matches: String) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/entitlement(_:matches:)-2bray)
- [static func entitlement(String, matches: Int) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/entitlement(_:matches:)-2ubq1)
- [static func entitlement(String, matches: Bool) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/entitlement(_:matches:)-6h77e)
- [static func hasEntitlement(String) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/hasentitlement(_:))
- [static func isFromSameTeam(andMatchesSigningIdentifier: String?) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/isfromsameteam(andmatchessigningidentifier:))
- [static func isPlatformCode(andMatchesSigningIdentifier: String?) -> XPCPeerRequirement](/documentation/xpc/xpcpeerrequirement/isplatformcode(andmatchessigningidentifier:))

## Type Aliases

- [xpc_peer_requirement_t](/documentation/xpc/xpc_peer_requirement_t)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
