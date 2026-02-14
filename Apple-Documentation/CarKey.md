# CarKey Documentation

Source: https://sosumi.ai/documentation/carkey

---
title: CarKey
source: https://developer.apple.com/documentation/carkey
timestamp: 2026-02-13T18:54:39.024Z
---

## Setup

- [CarKeyRemoteControl](/documentation/carkey/carkeyremotecontrol)

### Creating the Session Object

- [class func start(delegate: any CarKeyRemoteControlSessionDelegate, subscriptionRange: ClosedRange<Int>?, with: DispatchQueue?) async throws -> CarKeyRemoteControlSession](/documentation/carkey/carkeyremotecontrol/start(delegate:subscriptionrange:with:))

### Type Methods

- [class func registerForLaunchOnCarKeyEvent() throws](/documentation/carkey/carkeyremotecontrol/registerforlaunchoncarkeyevent())
- [class func unregisterForLaunchOnCarKeyEvent() throws](/documentation/carkey/carkeyremotecontrol/unregisterforlaunchoncarkeyevent())
- [CarKeyRemoteControlSession](/documentation/carkey/carkeyremotecontrolsession)

### Performing Vehicle-Related Actions

- [func perform(RemoteKeylessEntryAction) throws -> RemoteKeylessEntryAction.ExecutionRequest](/documentation/carkey/carkeyremotecontrolsession/perform(_:)-8ac0c)
- [func perform(RemoteKeylessEntryEnduringAction) throws -> RemoteKeylessEntryEnduringAction.EnduringExecutionRequest](/documentation/carkey/carkeyremotecontrolsession/perform(_:)-7mpsy)

### Sending Data to the Vehicle

- [func sendPassthroughData(Data, toVehicle: String) throws](/documentation/carkey/carkeyremotecontrolsession/sendpassthroughdata(_:tovehicle:))

### Closing the Session

- [func end() throws](/documentation/carkey/carkeyremotecontrolsession/end())

### Getting Vehicle Information

- [var vehicleReports: [VehicleReport]](/documentation/carkey/carkeyremotecontrolsession/vehiclereports)
- [func isPassiveEntryAvailable(forVehicle: String) throws -> Bool](/documentation/carkey/carkeyremotecontrolsession/ispassiveentryavailable(forvehicle:))

### Structures

- [CarKeyRemoteControlSession.Attestation](/documentation/carkey/carkeyremotecontrolsession/attestation)

#### Instance Properties

- [let appBundleIdentifier: String](/documentation/carkey/carkeyremotecontrolsession/attestation/appbundleidentifier)
- [let nonce: Data](/documentation/carkey/carkeyremotecontrolsession/attestation/nonce)
- [let signature: Data](/documentation/carkey/carkeyremotecontrolsession/attestation/signature)
- [let signedData: Data](/documentation/carkey/carkeyremotecontrolsession/attestation/signeddata)

### Instance Methods

- [func perform(RemoteKeylessEntryConfigurableEnduringAction, continuationStrategy: CarKeyRemoteControlSession.ContinuationStrategy) throws -> RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest](/documentation/carkey/carkeyremotecontrolsession/perform(_:continuationstrategy:))
- [func sign(data: Data, forVehicle: String) throws -> CarKeyRemoteControlSession.Attestation](/documentation/carkey/carkeyremotecontrolsession/sign(data:forvehicle:))

### Enumerations

- [CarKeyRemoteControlSession.ContinuationStrategy](/documentation/carkey/carkeyremotecontrolsession/continuationstrategy)

#### Enumeration Cases

- [case automatic](/documentation/carkey/carkeyremotecontrolsession/continuationstrategy/automatic)
- [case manual](/documentation/carkey/carkeyremotecontrolsession/continuationstrategy/manual)
- [CarKeyRemoteControlSessionDelegate](/documentation/carkey/carkeyremotecontrolsessiondelegate)

### Receiving Data from the Vehicle

- [func remoteControlSession(CarKeyRemoteControlSession, vehicleDidUpdateReport: VehicleReport)](/documentation/carkey/carkeyremotecontrolsessiondelegate/remotecontrolsession(_:vehicledidupdatereport:))
- [func remoteControlSession(CarKeyRemoteControlSession, didReceivePassthroughData: Data, fromVehicle: String)](/documentation/carkey/carkeyremotecontrolsessiondelegate/remotecontrolsession(_:didreceivepassthroughdata:fromvehicle:))

### Handling Session Invalidation

- [func remoteControlSession(CarKeyRemoteControlSession, didInvalidateWithError: CarKeyErrorCode)](/documentation/carkey/carkeyremotecontrolsessiondelegate/remotecontrolsession(_:didinvalidatewitherror:))

### Instance Methods

- [func remoteControlSession(CarKeyRemoteControlSession, didCreateKey: String, forVehicle: String)](/documentation/carkey/carkeyremotecontrolsessiondelegate/remotecontrolsession(_:didcreatekey:forvehicle:))
- [VehicleReport](/documentation/carkey/vehiclereport)

### Getting the Vehicle Details

- [let identifier: String](/documentation/carkey/vehiclereport/identifier)
- [var isConnected: Bool](/documentation/carkey/vehiclereport/isconnected)

### Getting the Vehicle’s Supported Functions

- [var supportedFunctions: [FunctionIdentifier]](/documentation/carkey/vehiclereport/supportedfunctions)
- [func status(for: FunctionIdentifier) throws -> FunctionStatus?](/documentation/carkey/vehiclereport/status(for:))
- [FunctionStatus](/documentation/carkey/functionstatus)

#### Creating a Function Status Type

- [init(rawValue: Int)](/documentation/carkey/functionstatus/init(rawvalue:))
- [init(Int)](/documentation/carkey/functionstatus/init(_:))

#### Getting the Value

- [let rawValue: Int](/documentation/carkey/functionstatus/rawvalue)

### Fetching Data Sent by the Vehicle

- [func proprietaryData(for: FunctionIdentifier) throws -> Data?](/documentation/carkey/vehiclereport/proprietarydata(for:))

## Vehicle Actions

- [RemoteKeylessEntryAction](/documentation/carkey/remotekeylessentryaction)

### Creating the Action Request

- [init(functionID: FunctionIdentifier, actionID: ActionIdentifier, vehicleID: String)](/documentation/carkey/remotekeylessentryaction/init(functionid:actionid:vehicleid:))

### Receiving the Action’s Response

- [RemoteKeylessEntryAction.ExecutionRequest](/documentation/carkey/remotekeylessentryaction/executionrequest)

#### Getting the Vehicle’s Respose

- [func results() async throws -> ExecutionStatus](/documentation/carkey/remotekeylessentryaction/executionrequest/results())
- [ExecutionStatus](/documentation/carkey/executionstatus)

##### Creating the Execution Status

- [init(rawValue: Int)](/documentation/carkey/executionstatus/init(rawvalue:))
- [init(Int)](/documentation/carkey/executionstatus/init(_:))

##### Getting the Value

- [let rawValue: Int](/documentation/carkey/executionstatus/rawvalue)

### Getting the Action Details

- [let functionID: FunctionIdentifier](/documentation/carkey/remotekeylessentryaction/functionid)
- [let actionID: ActionIdentifier](/documentation/carkey/remotekeylessentryaction/actionid)
- [let recipientVehicleID: String](/documentation/carkey/remotekeylessentryaction/recipientvehicleid)
- [RemoteKeylessEntryEnduringAction](/documentation/carkey/remotekeylessentryenduringaction)

### Creating the Action Request

- [init(functionID: FunctionIdentifier, actionID: ActionIdentifier, vehicleID: String)](/documentation/carkey/remotekeylessentryenduringaction/init(functionid:actionid:vehicleid:))

### Receiving the Action’s Response

- [RemoteKeylessEntryEnduringAction.EnduringExecutionRequest](/documentation/carkey/remotekeylessentryenduringaction/enduringexecutionrequest)

#### Getting the Vehicle’s Respose

- [func results() async throws -> ExecutionStatus](/documentation/carkey/remotekeylessentryenduringaction/enduringexecutionrequest/results())
- [ExecutionStatus](/documentation/carkey/executionstatus)

##### Creating the Execution Status

- [init(rawValue: Int)](/documentation/carkey/executionstatus/init(rawvalue:))
- [init(Int)](/documentation/carkey/executionstatus/init(_:))

##### Getting the Value

- [let rawValue: Int](/documentation/carkey/executionstatus/rawvalue)

#### Cancelling an Action

- [func stop() throws](/documentation/carkey/remotekeylessentryenduringaction/enduringexecutionrequest/stop())

### Getting the Action Details

- [let functionID: FunctionIdentifier](/documentation/carkey/remotekeylessentryenduringaction/functionid)
- [let actionID: ActionIdentifier](/documentation/carkey/remotekeylessentryenduringaction/actionid)
- [let recipientVehicleID: String](/documentation/carkey/remotekeylessentryenduringaction/recipientvehicleid)
- [FunctionIdentifier](/documentation/carkey/functionidentifier)

### Creating a Function Identifier

- [init(rawValue: Int)](/documentation/carkey/functionidentifier/init(rawvalue:))
- [init(Int)](/documentation/carkey/functionidentifier/init(_:))

### Getting the Value

- [let rawValue: Int](/documentation/carkey/functionidentifier/rawvalue)
- [ActionIdentifier](/documentation/carkey/actionidentifier)

### Creating the Action Identifier

- [init(rawValue: Int)](/documentation/carkey/actionidentifier/init(rawvalue:))
- [init(Int)](/documentation/carkey/actionidentifier/init(_:))

### Getting the Value

- [let rawValue: Int](/documentation/carkey/actionidentifier/rawvalue)

## Error Codes

- [CarKeyErrorCode](/documentation/carkey/carkeyerrorcode)

### Getting the Error Code

- [case AnotherRequestInProgress](/documentation/carkey/carkeyerrorcode/anotherrequestinprogress)
- [case ClientInBackground](/documentation/carkey/carkeyerrorcode/clientinbackground)
- [case EnduringRequestUsingEventMethod](/documentation/carkey/carkeyerrorcode/enduringrequestusingeventmethod)
- [case FeatureNotSupported](/documentation/carkey/carkeyerrorcode/featurenotsupported)
- [case FunctionUnknown](/documentation/carkey/carkeyerrorcode/functionunknown)
- [case Internal](/documentation/carkey/carkeyerrorcode/internal)
- [case MessageTooLong](/documentation/carkey/carkeyerrorcode/messagetoolong)
- [case RequestNotInProgress](/documentation/carkey/carkeyerrorcode/requestnotinprogress)
- [case RequestTimedOut](/documentation/carkey/carkeyerrorcode/requesttimedout)
- [case SecurityViolation](/documentation/carkey/carkeyerrorcode/securityviolation)
- [case SessionNotActive](/documentation/carkey/carkeyerrorcode/sessionnotactive)
- [case VehicleNotConnected](/documentation/carkey/carkeyerrorcode/vehiclenotconnected)
- [case VehicleNotFound](/documentation/carkey/carkeyerrorcode/vehiclenotfound)

## Structures

- [ExecutionStatus](/documentation/carkey/executionstatus)

### Creating the Execution Status

- [init(rawValue: Int)](/documentation/carkey/executionstatus/init(rawvalue:))
- [init(Int)](/documentation/carkey/executionstatus/init(_:))

### Getting the Value

- [let rawValue: Int](/documentation/carkey/executionstatus/rawvalue)
- [RemoteKeylessEntryConfigurableEnduringAction](/documentation/carkey/remotekeylessentryconfigurableenduringaction)

### Classes

- [RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest)

#### Structures

- [RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest.ContinuationRequest](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/continuationrequest)

##### Instance Properties

- [let data: Data?](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/continuationrequest/data)

##### Instance Methods

- [func confirm(Data?) throws](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/continuationrequest/confirm(_:))

#### Instance Properties

- [var eventStream: AsyncStream<RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest.Event>](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/eventstream)

#### Instance Methods

- [func results() async throws -> ExecutionStatus](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/results())
- [func stop() throws](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/stop())

#### Enumerations

- [RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest.Event](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/event)

##### Enumeration Cases

- [case receivedContinuationRequest(RemoteKeylessEntryConfigurableEnduringAction.EnduringExecutionRequest.ContinuationRequest)](/documentation/carkey/remotekeylessentryconfigurableenduringaction/enduringexecutionrequest/event/receivedcontinuationrequest(_:))

### Initializers

- [init(functionID: FunctionIdentifier, actionID: ActionIdentifier, vehicleID: String)](/documentation/carkey/remotekeylessentryconfigurableenduringaction/init(functionid:actionid:vehicleid:))

### Instance Properties

- [let actionID: ActionIdentifier](/documentation/carkey/remotekeylessentryconfigurableenduringaction/actionid)
- [let functionID: FunctionIdentifier](/documentation/carkey/remotekeylessentryconfigurableenduringaction/functionid)
- [let recipientVehicleID: String](/documentation/carkey/remotekeylessentryconfigurableenduringaction/recipientvehicleid)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
