# Distributed Documentation

Source: https://sosumi.ai/documentation/distributed

---
title: Distributed
source: https://developer.apple.com/documentation/distributed
timestamp: 2026-02-13T18:56:24.317Z
---

## Essentials

- [TicTacFish: Implementing a game using distributed actors](/documentation/swift/tictacfish_implementing_a_game_using_distributed_actors)

## Distributed Actors

- [DistributedActor](/documentation/distributed/distributedactor)

### Associated Types

- [ActorSystem](/documentation/distributed/distributedactor/actorsystem-swift.associatedtype)
- [SerializationRequirement](/documentation/distributed/distributedactor/serializationrequirement)

### Initializers

- [init(from: any Decoder) throws](/documentation/distributed/distributedactor/init(from:))

### Instance Properties

- [var actorSystem: Self.ActorSystem](/documentation/distributed/distributedactor/actorsystem-swift.property)
- [var asLocalActor: any Actor](/documentation/distributed/distributedactor/aslocalactor)
- [var id: Self.ID](/documentation/distributed/distributedactor/id)
- [var unownedExecutor: UnownedSerialExecutor](/documentation/distributed/distributedactor/unownedexecutor)

### Instance Methods

- [func assertIsolated(@autoclosure () -> String, file: StaticString, line: UInt)](/documentation/distributed/distributedactor/assertisolated(_:file:line:))
- [func assumeIsolated<T>((isolated Self) throws -> T, file: StaticString, line: UInt) rethrows -> T](/documentation/distributed/distributedactor/assumeisolated(_:file:line:))
- [func encode(to: any Encoder) throws](/documentation/distributed/distributedactor/encode(to:))
- [func preconditionIsolated(@autoclosure () -> String, file: StaticString, line: UInt)](/documentation/distributed/distributedactor/preconditionisolated(_:file:line:))
- [func whenLocal<T, E>((isolated Self) async throws(E) -> T) async throws(E) -> T?](/documentation/distributed/distributedactor/whenlocal(_:))

### Type Methods

- [static func resolve(id: Self.ID, using: Self.ActorSystem) throws -> Self](/documentation/distributed/distributedactor/resolve(id:using:))
- [DistributedActorSystem](/documentation/distributed/distributedactorsystem)

### Associated Types

- [ActorID](/documentation/distributed/distributedactorsystem/actorid)
- [InvocationDecoder](/documentation/distributed/distributedactorsystem/invocationdecoder)
- [InvocationEncoder](/documentation/distributed/distributedactorsystem/invocationencoder)
- [ResultHandler](/documentation/distributed/distributedactorsystem/resulthandler)
- [SerializationRequirement](/documentation/distributed/distributedactorsystem/serializationrequirement)

### Instance Methods

- [func actorReady<Act>(Act)](/documentation/distributed/distributedactorsystem/actorready(_:))
- [func assignID<Act>(Act.Type) -> Self.ActorID](/documentation/distributed/distributedactorsystem/assignid(_:))
- [func executeDistributedTarget<Act>(on: Act, target: RemoteCallTarget, invocationDecoder: inout Self.InvocationDecoder, handler: Self.ResultHandler) async throws](/documentation/distributed/distributedactorsystem/executedistributedtarget(on:target:invocationdecoder:handler:))
- [func invokeHandlerOnReturn(handler: Self.ResultHandler, resultBuffer: UnsafeRawPointer, metatype: any Any.Type) async throws](/documentation/distributed/distributedactorsystem/invokehandleronreturn(handler:resultbuffer:metatype:))
- [func makeInvocationEncoder() -> Self.InvocationEncoder](/documentation/distributed/distributedactorsystem/makeinvocationencoder())
- [func remoteCall<Act, Err, Res>(on: Act, target: RemoteCallTarget, invocation: inout Self.InvocationEncoder, throwing: Err.Type, returning: Res.Type) async throws -> Res](/documentation/distributed/distributedactorsystem/remotecall(on:target:invocation:throwing:returning:))
- [func remoteCallVoid<Act, Err>(on: Act, target: RemoteCallTarget, invocation: inout Self.InvocationEncoder, throwing: Err.Type) async throws](/documentation/distributed/distributedactorsystem/remotecallvoid(on:target:invocation:throwing:))
- [func resignID(Self.ActorID)](/documentation/distributed/distributedactorsystem/resignid(_:))
- [func resolve<Act>(id: Self.ActorID, as: Act.Type) throws -> Act?](/documentation/distributed/distributedactorsystem/resolve(id:as:))
- [macro Resolvable()](/documentation/distributed/resolvable())
- [func buildDefaultDistributedRemoteActorExecutor<Act>(Act) -> UnownedSerialExecutor](/documentation/distributed/builddefaultdistributedremoteactorexecutor(_:))

## Remote Calls

- [RemoteCallTarget](/documentation/distributed/remotecalltarget)

### Initializers

- [init(String)](/documentation/distributed/remotecalltarget/init(_:))

### Instance Properties

- [var description: String](/documentation/distributed/remotecalltarget/description)
- [var identifier: String](/documentation/distributed/remotecalltarget/identifier)
- [RemoteCallArgument](/documentation/distributed/remotecallargument)

### Initializers

- [init(label: String?, name: String, value: Value)](/documentation/distributed/remotecallargument/init(label:name:value:))

### Instance Properties

- [var effectiveLabel: String](/documentation/distributed/remotecallargument/effectivelabel)
- [let label: String?](/documentation/distributed/remotecallargument/label)
- [let name: String](/documentation/distributed/remotecallargument/name)
- [let value: Value](/documentation/distributed/remotecallargument/value)
- [DistributedTargetInvocationEncoder](/documentation/distributed/distributedtargetinvocationencoder)

### Associated Types

- [SerializationRequirement](/documentation/distributed/distributedtargetinvocationencoder/serializationrequirement)

### Instance Methods

- [func doneRecording() throws](/documentation/distributed/distributedtargetinvocationencoder/donerecording())
- [func recordArgument<Value>(RemoteCallArgument<Value>) throws](/documentation/distributed/distributedtargetinvocationencoder/recordargument(_:))
- [func recordErrorType<E>(E.Type) throws](/documentation/distributed/distributedtargetinvocationencoder/recorderrortype(_:))
- [func recordGenericSubstitution<T>(T.Type) throws](/documentation/distributed/distributedtargetinvocationencoder/recordgenericsubstitution(_:))
- [func recordReturnType<R>(R.Type) throws](/documentation/distributed/distributedtargetinvocationencoder/recordreturntype(_:))
- [DistributedTargetInvocationDecoder](/documentation/distributed/distributedtargetinvocationdecoder)

### Associated Types

- [SerializationRequirement](/documentation/distributed/distributedtargetinvocationdecoder/serializationrequirement)

### Instance Methods

- [func decodeErrorType() throws -> (any Any.Type)?](/documentation/distributed/distributedtargetinvocationdecoder/decodeerrortype())
- [func decodeGenericSubstitutions() throws -> [any Any.Type]](/documentation/distributed/distributedtargetinvocationdecoder/decodegenericsubstitutions())
- [func decodeNextArgument<Argument>() throws -> Argument](/documentation/distributed/distributedtargetinvocationdecoder/decodenextargument())
- [func decodeReturnType() throws -> (any Any.Type)?](/documentation/distributed/distributedtargetinvocationdecoder/decodereturntype())
- [DistributedTargetInvocationResultHandler](/documentation/distributed/distributedtargetinvocationresulthandler)

### Associated Types

- [SerializationRequirement](/documentation/distributed/distributedtargetinvocationresulthandler/serializationrequirement)

### Instance Methods

- [func onReturn<Success>(value: Success) async throws](/documentation/distributed/distributedtargetinvocationresulthandler/onreturn(value:))
- [func onReturnVoid() async throws](/documentation/distributed/distributedtargetinvocationresulthandler/onreturnvoid())
- [func onThrow<Err>(error: Err) async throws](/documentation/distributed/distributedtargetinvocationresulthandler/onthrow(error:))

## Local Testing

- [LocalTestingDistributedActorSystem](/documentation/distributed/localtestingdistributedactorsystem)

### Initializers

- [init()](/documentation/distributed/localtestingdistributedactorsystem/init())
- [LocalTestingActorID](/documentation/distributed/localtestingactorid)

### Initializers

- [init(id: String)](/documentation/distributed/localtestingactorid/init(id:))
- [init(parse: String)](/documentation/distributed/localtestingactorid/init(parse:))

### Instance Properties

- [var address: String](/documentation/distributed/localtestingactorid/address)
- [let id: String](/documentation/distributed/localtestingactorid/id)
- [LocalTestingActorAddress](/documentation/distributed/localtestingactoraddress)
- [LocalTestingInvocationEncoder](/documentation/distributed/localtestinginvocationencoder)
- [LocalTestingInvocationDecoder](/documentation/distributed/localtestinginvocationdecoder)
- [LocalTestingInvocationResultHandler](/documentation/distributed/localtestinginvocationresulthandler)

## Errors

- [DistributedActorCodingError](/documentation/distributed/distributedactorcodingerror)

### Initializers

- [init(message: String)](/documentation/distributed/distributedactorcodingerror/init(message:))

### Instance Properties

- [let message: String](/documentation/distributed/distributedactorcodingerror/message)

### Type Methods

- [static func missingActorSystemUserInfo<Act>(Act.Type) -> DistributedActorCodingError](/documentation/distributed/distributedactorcodingerror/missingactorsystemuserinfo(_:))
- [DistributedActorSystemError](/documentation/distributed/distributedactorsystemerror)
- [ExecuteDistributedTargetError](/documentation/distributed/executedistributedtargeterror)

### Initializers

- [init(message: String)](/documentation/distributed/executedistributedtargeterror/init(message:))
- [init(message: String, errorCode: ExecuteDistributedTargetError.ErrorCode)](/documentation/distributed/executedistributedtargeterror/init(message:errorcode:))

### Instance Properties

- [let errorCode: ExecuteDistributedTargetError.ErrorCode](/documentation/distributed/executedistributedtargeterror/errorcode-swift.property)
- [let message: String](/documentation/distributed/executedistributedtargeterror/message)

### Enumerations

- [ExecuteDistributedTargetError.ErrorCode](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum)

#### Enumeration Cases

- [case invalidGenericSubstitutions](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/invalidgenericsubstitutions)
- [case invalidParameterCount](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/invalidparametercount)
- [case missingGenericSubstitutions](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/missinggenericsubstitutions)
- [case other](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/other)
- [case targetAccessorNotFound](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/targetaccessornotfound)
- [case typeDeserializationFailure](/documentation/distributed/executedistributedtargeterror/errorcode-swift.enum/typedeserializationfailure)
- [LocalTestingDistributedActorSystemError](/documentation/distributed/localtestingdistributedactorsystemerror)

### Initializers

- [init(message: String)](/documentation/distributed/localtestingdistributedactorsystemerror/init(message:))

### Instance Properties

- [let message: String](/documentation/distributed/localtestingdistributedactorsystemerror/message)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
