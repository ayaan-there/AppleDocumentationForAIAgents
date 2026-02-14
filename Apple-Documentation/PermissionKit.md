# PermissionKit Documentation

Source: https://sosumi.ai/documentation/permissionkit

---
title: PermissionKit
source: https://developer.apple.com/documentation/permissionkit
timestamp: 2026-02-13T19:00:35.472Z
---

## Essentials

- [Creating a communication experience](/documentation/permissionkit/creating-a-communication-experience)
- [AskCenter](/documentation/permissionkit/askcenter)

### Getting the shared instance

- [static let shared: AskCenter](/documentation/permissionkit/askcenter/shared)

### Making permission requests

- [func ask(PermissionQuestion<SignificantAppUpdateTopic>, in: NSWindow) async throws](/documentation/permissionkit/askcenter/ask(_:in:)-39vi7)
- [func ask(PermissionQuestion<CommunicationTopic>, in: NSWindow) async throws](/documentation/permissionkit/askcenter/ask(_:in:)-3znb6)
- [func ask(PermissionQuestion<CommunicationTopic>, in: UIViewController) async throws](/documentation/permissionkit/askcenter/ask(_:in:)-6xupo)
- [func ask(PermissionQuestion<SignificantAppUpdateTopic>, in: UIViewController) async throws](/documentation/permissionkit/askcenter/ask(_:in:)-8ks48)

### Receiving responses

- [func responses<Topic>(for: Topic.Type) -> some AsyncSequence<PermissionResponse<Topic>, Never>
](/documentation/permissionkit/askcenter/responses(for:))
- [PermissionQuestion](/documentation/permissionkit/permissionquestion)

### Creating permission requests

- [convenience init(handle: CommunicationHandle)](/documentation/permissionkit/permissionquestion/init(handle:))
- [convenience init(handles: [CommunicationHandle])](/documentation/permissionkit/permissionquestion/init(handles:))
- [convenience init(communicationTopic: Topic)](/documentation/permissionkit/permissionquestion/init(communicationtopic:))
- [convenience init(significantAppUpdateTopic: Topic)](/documentation/permissionkit/permissionquestion/init(significantappupdatetopic:))

### Working with choices

- [var choices: [PermissionChoice]](/documentation/permissionkit/permissionquestion/choices)
- [var defaultChoice: PermissionChoice](/documentation/permissionkit/permissionquestion/defaultchoice)

### Accessing properties

- [let id: UUID](/documentation/permissionkit/permissionquestion/id)
- [let topic: Topic](/documentation/permissionkit/permissionquestion/topic)
- [var expirationDate: Date?](/documentation/permissionkit/permissionquestion/expirationdate)

## Permission topics

- [SignificantAppUpdateTopic](/documentation/permissionkit/significantappupdatetopic)

### Creating topics

- [init(description: String)](/documentation/permissionkit/significantappupdatetopic/init(description:))

### Accessing properties

- [let description: String](/documentation/permissionkit/significantappupdatetopic/description)
- [static let id: String](/documentation/permissionkit/significantappupdatetopic/id)
- [CommunicationTopic](/documentation/permissionkit/communicationtopic)

### Working with supporting types

- [CommunicationTopic.Action](/documentation/permissionkit/communicationtopic/action)

#### Specifying communication actions

- [case audioCall](/documentation/permissionkit/communicationtopic/action/audiocall)
- [case call](/documentation/permissionkit/communicationtopic/action/call)
- [case follow](/documentation/permissionkit/communicationtopic/action/follow)
- [case friend](/documentation/permissionkit/communicationtopic/action/friend)
- [case message](/documentation/permissionkit/communicationtopic/action/message)
- [case beFollowed](/documentation/permissionkit/communicationtopic/action/befollowed)
- [case chat](/documentation/permissionkit/communicationtopic/action/chat)
- [case communicate](/documentation/permissionkit/communicationtopic/action/communicate)
- [case connect](/documentation/permissionkit/communicationtopic/action/connect)
- [case videoCall](/documentation/permissionkit/communicationtopic/action/videocall)
- [CommunicationTopic.PersonInformation](/documentation/permissionkit/communicationtopic/personinformation-swift.struct)

#### Creating contact details

- [init(handle: CommunicationHandle, nameComponents: PersonNameComponents?, avatarImage: CGImage?)](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/init(handle:namecomponents:avatarimage:))
- [init(from: any Decoder) throws](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/init(from:))

#### Accessing properties

- [var avatarImage: CGImage?](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/avatarimage)
- [var handle: CommunicationHandle](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/handle)
- [var nameComponents: PersonNameComponents?](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/namecomponents)

#### Encoding

- [func encode(to: any Encoder) throws](/documentation/permissionkit/communicationtopic/personinformation-swift.struct/encode(to:))

### Creating topics

- [init(personInformation: [CommunicationTopic.PersonInformation])](/documentation/permissionkit/communicationtopic/init(personinformation:))
- [init(personInformation: [CommunicationTopic.PersonInformation], actions: Set<CommunicationTopic.Action>)](/documentation/permissionkit/communicationtopic/init(personinformation:actions:))

### Accessing properties

- [var actions: Set<CommunicationTopic.Action>](/documentation/permissionkit/communicationtopic/actions)
- [var personInformation: [CommunicationTopic.PersonInformation]](/documentation/permissionkit/communicationtopic/personinformation-swift.property)
- [static let id: String](/documentation/permissionkit/communicationtopic/id)

## Presentation

- [PermissionButton](/documentation/permissionkit/permissionbutton)

### Creating buttons

- [init(question: PermissionQuestion<Topic>, label: () -> Label)](/documentation/permissionkit/permissionbutton/init(question:label:)-25jfa)
- [init(question: PermissionQuestion<Topic>, label: () -> Label)](/documentation/permissionkit/permissionbutton/init(question:label:)-8291n)

### Accessing properties

- [let question: PermissionQuestion<Topic>](/documentation/permissionkit/permissionbutton/question)
- [var body: some View](/documentation/permissionkit/permissionbutton/body)

## Response management

- [func responses<Topic>(for: Topic.Type) -> some AsyncSequence<PermissionResponse<Topic>, Never>
](/documentation/permissionkit/askcenter/responses(for:))
- [PermissionResponse](/documentation/permissionkit/permissionresponse)

### Getting response information

- [let choice: PermissionChoice](/documentation/permissionkit/permissionresponse/choice)
- [let question: PermissionQuestion<Topic>](/documentation/permissionkit/permissionresponse/question)
- [CommunicationHandle](/documentation/permissionkit/communicationhandle)

### Specifying handle types

- [CommunicationHandle.Kind](/documentation/permissionkit/communicationhandle/kind-swift.enum)

#### Identifying a handle type

- [case phoneNumber](/documentation/permissionkit/communicationhandle/kind-swift.enum/phonenumber)
- [case emailAddress](/documentation/permissionkit/communicationhandle/kind-swift.enum/emailaddress)
- [case custom](/documentation/permissionkit/communicationhandle/kind-swift.enum/custom)

### Creating handles

- [init(value: String, kind: CommunicationHandle.Kind)](/documentation/permissionkit/communicationhandle/init(value:kind:))

### Accessing properties

- [var value: String](/documentation/permissionkit/communicationhandle/value)
- [var kind: CommunicationHandle.Kind](/documentation/permissionkit/communicationhandle/kind-swift.property)
- [PermissionChoice](/documentation/permissionkit/permissionchoice)

### Accessing answers

- [var answer: PermissionChoice.Answer](/documentation/permissionkit/permissionchoice/answer-swift.property)
- [PermissionChoice.Answer](/documentation/permissionkit/permissionchoice/answer-swift.enum)

#### Determining the permission request response

- [case approval](/documentation/permissionkit/permissionchoice/answer-swift.enum/approval)
- [case denial](/documentation/permissionkit/permissionchoice/answer-swift.enum/denial)
- [static let approve: PermissionChoice](/documentation/permissionkit/permissionchoice/approve)
- [static let decline: PermissionChoice](/documentation/permissionkit/permissionchoice/decline)

### Identifying permissions

- [var id: String](/documentation/permissionkit/permissionchoice/id)
- [var title: String](/documentation/permissionkit/permissionchoice/title)

### Computing hashes

- [func hash(into: inout Hasher)](/documentation/permissionkit/permissionchoice/hash(into:))
- [static func == (PermissionChoice, PermissionChoice) -> Bool](/documentation/permissionkit/permissionchoice/==(_:_:))
- [CommunicationLimits](/documentation/permissionkit/communicationlimits)

### Accessing communication limits

- [static let current: CommunicationLimits](/documentation/permissionkit/communicationlimits/current)

### Checking known handles

- [func isKnownHandle(CommunicationHandle) async -> Bool](/documentation/permissionkit/communicationlimits/isknownhandle(_:))
- [func knownHandles(in: Set<CommunicationHandle>) async -> Set<CommunicationHandle>](/documentation/permissionkit/communicationlimits/knownhandles(in:))

### Deprecated APIs

- [var updates: some AsyncSequence<PermissionResponse<CommunicationTopic>, Never>](/documentation/permissionkit/communicationlimits/updates)
- [func ask(PermissionQuestion<CommunicationTopic>, in: NSWindow) async throws](/documentation/permissionkit/communicationlimits/ask(_:in:)-5tzyy)
- [func ask(PermissionQuestion<CommunicationTopic>, in: UIViewController) async throws](/documentation/permissionkit/communicationlimits/ask(_:in:)-5ou06)

## Supporting types

- [QuestionTopic](/documentation/permissionkit/questiontopic)

### Getting the topic identifier

- [static var id: String](/documentation/permissionkit/questiontopic/id)

## Errors

- [AskError](/documentation/permissionkit/askerror)

### Handling errors

- [case unknown](/documentation/permissionkit/askerror/unknown)
- [case communicationLimitsNotEnabled](/documentation/permissionkit/askerror/communicationlimitsnotenabled)
- [case contactSyncNotSetup](/documentation/permissionkit/askerror/contactsyncnotsetup)
- [case invalidQuestion](/documentation/permissionkit/askerror/invalidquestion)
- [case systemError(underlyingError: any Error)](/documentation/permissionkit/askerror/systemerror(underlyingerror:))

### Enumeration Cases

- [case notAvailable](/documentation/permissionkit/askerror/notavailable)

### Instance Properties

- [var errorDescription: String?](/documentation/permissionkit/askerror/errordescription)

## Deprecated APIs

- [CommunicationLimitsButton](/documentation/permissionkit/communicationlimitsbutton)

### Creating a view

- [init(question: PermissionQuestion<CommunicationTopic>, label: () -> Label)](/documentation/permissionkit/communicationlimitsbutton/init(question:label:))
- [var body: some View](/documentation/permissionkit/communicationlimitsbutton/body)
- [let question: PermissionQuestion<CommunicationTopic>](/documentation/permissionkit/communicationlimitsbutton/question)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
