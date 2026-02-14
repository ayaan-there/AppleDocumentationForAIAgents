# SafetyKit Documentation

Source: https://sosumi.ai/documentation/safetykit

---
title: SafetyKit
source: https://developer.apple.com/documentation/safetykit
timestamp: 2026-02-13T19:01:33.117Z
---

## Detecting a crash

- [SACrashDetectionManager](/documentation/safetykit/sacrashdetectionmanager)

### Determining availability

- [class var isAvailable: Bool](/documentation/safetykit/sacrashdetectionmanager/isavailable)
- [var authorizationStatus: SAAuthorizationStatus](/documentation/safetykit/sacrashdetectionmanager/authorizationstatus)

### Requesting authorization

- [var delegate: (any SACrashDetectionDelegate)?](/documentation/safetykit/sacrashdetectionmanager/delegate)
- [func requestAuthorization(completionHandler: (SAAuthorizationStatus, (any Error)?) -> Void)](/documentation/safetykit/sacrashdetectionmanager/requestauthorization(completionhandler:))
- [SAAuthorizationStatus](/documentation/safetykit/saauthorizationstatus)

### Obtaining status

- [case authorized](/documentation/safetykit/saauthorizationstatus/authorized)
- [case denied](/documentation/safetykit/saauthorizationstatus/denied)
- [case notDetermined](/documentation/safetykit/saauthorizationstatus/notdetermined)

### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/saauthorizationstatus/init(rawvalue:))

### Default Implementations

- [Equatable Implementations](/documentation/safetykit/saauthorizationstatus/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saauthorizationstatus/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/saauthorizationstatus/rawrepresentable-implementations)

#### Instance Properties

- [var hashValue: Int](/documentation/safetykit/saauthorizationstatus/hashvalue)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/saauthorizationstatus/hash(into:))
- [SACrashDetectionEvent](/documentation/safetykit/sacrashdetectionevent)

### Determining the event type

- [SACrashDetectionEvent.Response](/documentation/safetykit/sacrashdetectionevent/response-swift.enum)

#### Determining responses

- [case attempted](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/attempted)
- [case disabled](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/disabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/hash(into:))
- [var date: Date](/documentation/safetykit/sacrashdetectionevent/date)
- [var location: CLLocation?](/documentation/safetykit/sacrashdetectionevent/location)
- [var response: SACrashDetectionEvent.Response](/documentation/safetykit/sacrashdetectionevent/response-swift.property)
- [SACrashDetectionDelegate](/documentation/safetykit/sacrashdetectiondelegate)

### Obtaining a Crash Detection event

- [func crashDetectionManager(SACrashDetectionManager, didDetect: SACrashDetectionEvent)](/documentation/safetykit/sacrashdetectiondelegate/crashdetectionmanager(_:diddetect:))

## Responding to a crash

- [SAEmergencyResponseManager](/documentation/safetykit/saemergencyresponsemanager)

### Placing a voice call

- [SAEmergencyResponseManager.VoiceCallStatus](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus)

#### Determining call status

- [case active](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/active)
- [case dialing](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/dialing)
- [case disconnected](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/disconnected)
- [case failed](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/failed)

#### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/saemergencyresponsemanager/voicecallstatus/hash(into:))
- [func dialVoiceCall(toPhoneNumber: String, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/safetykit/saemergencyresponsemanager/dialvoicecall(tophonenumber:completionhandler:))
- [var delegate: (any SAEmergencyResponseDelegate)?](/documentation/safetykit/saemergencyresponsemanager/delegate)
- [SAEmergencyResponseDelegate](/documentation/safetykit/saemergencyresponsedelegate)

### Receiving voice call status

- [func emergencyResponseManager(SAEmergencyResponseManager, didUpdateVoiceCallStatus: SAEmergencyResponseManager.VoiceCallStatus)](/documentation/safetykit/saemergencyresponsedelegate/emergencyresponsemanager(_:didupdatevoicecallstatus:))
- [SACrashDetectionEvent.Response](/documentation/safetykit/sacrashdetectionevent/response-swift.enum)

### Determining responses

- [case attempted](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/attempted)
- [case disabled](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/disabled)

### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/init(rawvalue:))

### Default Implementations

- [Equatable Implementations](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/rawrepresentable-implementations)

#### Instance Properties

- [var hashValue: Int](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/hashvalue)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/sacrashdetectionevent/response-swift.enum/hash(into:))

## Handling errors

- [let SAErrorDomain: String](/documentation/safetykit/saerrordomain)
- [SAError.Code](/documentation/safetykit/saerror/code)

### Determining the error type

- [case invalidArgument](/documentation/safetykit/saerror/code/invalidargument)
- [case notAllowed](/documentation/safetykit/saerror/code/notallowed)
- [case notAuthorized](/documentation/safetykit/saerror/code/notauthorized)
- [case operationFailed](/documentation/safetykit/saerror/code/operationfailed)

### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/saerror/code/init(rawvalue:))

### Default Implementations

- [Equatable Implementations](/documentation/safetykit/saerror/code/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saerror/code/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/saerror/code/rawrepresentable-implementations)

#### Instance Properties

- [var hashValue: Int](/documentation/safetykit/saerror/code/hashvalue)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/saerror/code/hash(into:))
- [SAError](/documentation/safetykit/saerror)

### Inspecting error information

- [var localizedDescription: String](/documentation/safetykit/saerror/localizeddescription)
- [static var errorDomain: String](/documentation/safetykit/saerror/errordomain)

### Comparing errors

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saerror/!=(_:_:))

### Identifying an error cause

- [SAError.Code](/documentation/safetykit/saerror/code)

#### Determining the error type

- [case invalidArgument](/documentation/safetykit/saerror/code/invalidargument)
- [case notAllowed](/documentation/safetykit/saerror/code/notallowed)
- [case notAuthorized](/documentation/safetykit/saerror/code/notauthorized)
- [case operationFailed](/documentation/safetykit/saerror/code/operationfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/safetykit/saerror/code/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/safetykit/saerror/code/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saerror/code/!=(_:_:))
- [RawRepresentable Implementations](/documentation/safetykit/saerror/code/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/safetykit/saerror/code/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/safetykit/saerror/code/hash(into:))
- [let SAErrorDomain: String](/documentation/safetykit/saerrordomain)
- [static var invalidArgument: SAError.Code](/documentation/safetykit/saerror/invalidargument)
- [static var notAllowed: SAError.Code](/documentation/safetykit/saerror/notallowed)
- [static var notAuthorized: SAError.Code](/documentation/safetykit/saerror/notauthorized)
- [static var operationFailed: SAError.Code](/documentation/safetykit/saerror/operationfailed)

### Default Implementations

- [CustomNSError Implementations](/documentation/safetykit/saerror/customnserror-implementations)

#### Type Properties

- [static var errorDomain: String](/documentation/safetykit/saerror/errordomain-9bjqy)
- [Equatable Implementations](/documentation/safetykit/saerror/equatable-implementations)

#### Operators

- [static func != (Self, Self) -> Bool](/documentation/safetykit/saerror/!=(_:_:))
- [Error Implementations](/documentation/safetykit/saerror/error-implementations)

#### Instance Properties

- [var localizedDescription: String](/documentation/safetykit/saerror/localizeddescription)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
