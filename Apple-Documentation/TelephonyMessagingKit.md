# TelephonyMessagingKit Documentation

Source: https://sosumi.ai/documentation/telephonymessagingkit

---
title: TelephonyMessagingKit
source: https://developer.apple.com/documentation/telephonymessagingkit
timestamp: 2026-02-13T19:03:05.464Z
---

## Essentials

- [Creating a carrier messaging app](/documentation/availability/creating-a-carrier-messaging-app)
- [TelephonyMessagingSession](/documentation/telephonymessagingkit/telephonymessagingsession)

### Obtaining the shared instance

- [static let shared: TelephonyMessagingSession](/documentation/telephonymessagingkit/telephonymessagingsession/shared)

### Determining service availability

- [var cellularServices: [CellularServiceState]](/documentation/telephonymessagingkit/telephonymessagingsession/cellularservices)
- [var cellularServiceStateUpdates: some AsyncSequence<CellularServiceState, Never>](/documentation/telephonymessagingkit/telephonymessagingsession/cellularservicestateupdates)
- [CellularServiceState](/documentation/telephonymessagingkit/cellularservicestate)

#### Accessing state properties

- [let id: CellularServiceID](/documentation/telephonymessagingkit/cellularservicestate/id)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let label: String](/documentation/telephonymessagingkit/cellularservicestate/label)

### Using Short Message Service (SMS)

- [var smsService: SMSService](/documentation/telephonymessagingkit/telephonymessagingsession/smsservice)
- [SMSService](/documentation/telephonymessagingkit/smsservice)

#### Determining service viabililty

- [func isViable(for: CellularServiceID) -> Bool](/documentation/telephonymessagingkit/smsservice/isviable(for:))
- [var viabilityNotifications: some AsyncSequence<SMSService.ViabilityNotification, Never>](/documentation/telephonymessagingkit/smsservice/viabilitynotifications)
- [SMSService.ViabilityNotification](/documentation/telephonymessagingkit/smsservice/viabilitynotification)

##### Accessing notification properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/smsservice/viabilitynotification/cellularserviceid)
- [let isViable: Bool](/documentation/telephonymessagingkit/smsservice/viabilitynotification/isviable)

#### Sending messages

- [func sendMessage(SMSMessage) async throws](/documentation/telephonymessagingkit/smsservice/sendmessage(_:))
- [SMSMessage](/documentation/telephonymessagingkit/smsmessage)

##### Creating an SMS message

- [init(cellularServiceID: CellularServiceID, handle: SMSHandle, messageID: SMSMessageID, content: SMSContent)](/documentation/telephonymessagingkit/smsmessage/init(cellularserviceid:handle:messageid:content:))

##### Accessing message content

- [let content: SMSContent](/documentation/telephonymessagingkit/smsmessage/content)
- [SMSContent](/documentation/telephonymessagingkit/smscontent)

###### Creating SMS content

- [init(body: String)](/documentation/telephonymessagingkit/smscontent/init(body:))

###### Accessing content properties

- [let body: String](/documentation/telephonymessagingkit/smscontent/body)

##### Accessing message properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/smsmessage/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let handle: SMSHandle](/documentation/telephonymessagingkit/smsmessage/handle)
- [SMSHandle](/documentation/telephonymessagingkit/smshandle)

###### Creating a handle

- [init(phoneNumber: String)](/documentation/telephonymessagingkit/smshandle/init(phonenumber:))

###### Accessing handle properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/smshandle/phonenumber)
- [let messageID: SMSMessageID](/documentation/telephonymessagingkit/smsmessage/messageid)
- [SMSMessageID](/documentation/telephonymessagingkit/smsmessageid)

###### Creating a message ID

- [init(rawValue: UInt32)](/documentation/telephonymessagingkit/smsmessageid/init(rawvalue:))

###### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/smsmessageid/description)

###### Working with raw values

- [let rawValue: UInt32](/documentation/telephonymessagingkit/smsmessageid/rawvalue)

#### Receiving messages

- [var incomingMessageNotifications: some AsyncSequence<SMSService.IncomingMessageNotification, Never>](/documentation/telephonymessagingkit/smsservice/incomingmessagenotifications)
- [SMSService.IncomingMessageNotification](/documentation/telephonymessagingkit/smsservice/incomingmessagenotification)

##### Inspecting notification properties

- [let message: SMSMessage](/documentation/telephonymessagingkit/smsservice/incomingmessagenotification/message)

#### Handling critical state changes

- [var criticalMessageStateNotifications: some AsyncSequence<SMSService.CriticalMessageStateNotification, Never>](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotifications)
- [SMSService.CriticalMessageStateNotification](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification)

##### Accessing message properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification/cellularserviceid)
- [let messageID: SMSMessageID](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification/messageid)
- [let state: SMSService.CriticalMessageStateNotification.State](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification/state-swift.property)
- [SMSService.CriticalMessageStateNotification.State](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification/state-swift.enum)

###### Inspecting message states

- [case sent](/documentation/telephonymessagingkit/smsservice/criticalmessagestatenotification/state-swift.enum/sent)

#### Reporting spam

- [func reportSpam(SMSMessage) async throws](/documentation/telephonymessagingkit/smsservice/reportspam(_:))

#### Handling errors

- [SMSService.Error](/documentation/telephonymessagingkit/smsservice/error)

##### Identifying errors

- [case notSupported](/documentation/telephonymessagingkit/smsservice/error/notsupported)
- [case permanentFailure](/documentation/telephonymessagingkit/smsservice/error/permanentfailure)
- [case temporaryFailure](/documentation/telephonymessagingkit/smsservice/error/temporaryfailure)
- [case unknown](/documentation/telephonymessagingkit/smsservice/error/unknown)

### Using Multimedia Messaging Service (MMS)

- [var mmsService: MMSService](/documentation/telephonymessagingkit/telephonymessagingsession/mmsservice)
- [MMSService](/documentation/telephonymessagingkit/mmsservice)

#### Determining service viabililty

- [func isViable(for: CellularServiceID) -> Bool](/documentation/telephonymessagingkit/mmsservice/isviable(for:))
- [var viabilityNotifications: some AsyncSequence<MMSService.ViabilityNotification, Never>](/documentation/telephonymessagingkit/mmsservice/viabilitynotifications)
- [MMSService.ViabilityNotification](/documentation/telephonymessagingkit/mmsservice/viabilitynotification)

##### Accessing notification properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/mmsservice/viabilitynotification/cellularserviceid)
- [let isViable: Bool](/documentation/telephonymessagingkit/mmsservice/viabilitynotification/isviable)

#### Managing MMS configuration

- [func configuration(for: CellularServiceID) async throws -> MMSService.Configuration](/documentation/telephonymessagingkit/mmsservice/configuration(for:))
- [MMSService.Configuration](/documentation/telephonymessagingkit/mmsservice/configuration)

##### Instance Properties

- [var maximumImageSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/mmsservice/configuration/maximumimagesize)
- [var maximumMessageSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/mmsservice/configuration/maximummessagesize)
- [var maximumRecipients: Int?](/documentation/telephonymessagingkit/mmsservice/configuration/maximumrecipients)
- [var maximumSubjectSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/mmsservice/configuration/maximumsubjectsize)
- [var smsSizeToBeSentAsMMSInstead: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/mmsservice/configuration/smssizetobesentasmmsinstead)

#### Sending messages

- [func sendMessage(MMSMessage) async throws](/documentation/telephonymessagingkit/mmsservice/sendmessage(_:))
- [MMSMessage](/documentation/telephonymessagingkit/mmsmessage)

##### Creating an MMS message

- [init(cellularServiceID: CellularServiceID, messageID: MMSMessageID, content: MMSContent)](/documentation/telephonymessagingkit/mmsmessage/init(cellularserviceid:messageid:content:))

##### Accessing message content

- [var content: MMSContent](/documentation/telephonymessagingkit/mmsmessage/content)
- [MMSContent](/documentation/telephonymessagingkit/mmscontent)

###### Creating an MMS content instance

- [init()](/documentation/telephonymessagingkit/mmscontent/init())
- [init(parts: [MMSPartContent], recipients: [MMSHandle], subject: String?)](/documentation/telephonymessagingkit/mmscontent/init(parts:recipients:subject:))

###### Accessing content properties

- [var parts: [MMSPartContent]](/documentation/telephonymessagingkit/mmscontent/parts)
- [MMSPartContent](/documentation/telephonymessagingkit/mmspartcontent)

###### Creating a content part

- [init(data: Data, contentType: UTType?, contentID: String, disposition: MMSPartContent.MMSDispositionType, fileName: String)](/documentation/telephonymessagingkit/mmspartcontent/init(data:contenttype:contentid:disposition:filename:))

###### Accessing part properties

- [var data: Data](/documentation/telephonymessagingkit/mmspartcontent/data)
- [var disposition: MMSPartContent.MMSDispositionType](/documentation/telephonymessagingkit/mmspartcontent/disposition)
- [MMSPartContent.MMSDispositionType](/documentation/telephonymessagingkit/mmspartcontent/mmsdispositiontype)

###### Working with disposition types

- [case attachment](/documentation/telephonymessagingkit/mmspartcontent/mmsdispositiontype/attachment)
- [case inline](/documentation/telephonymessagingkit/mmspartcontent/mmsdispositiontype/inline)
- [var filename: String](/documentation/telephonymessagingkit/mmspartcontent/filename)
- [var contentID: String](/documentation/telephonymessagingkit/mmspartcontent/contentid)
- [var contentType: UTType?](/documentation/telephonymessagingkit/mmspartcontent/contenttype)
- [UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct)

###### Working with custom headers

- [var customHeaders: [MMSPartContent.MMSCustomHeader]](/documentation/telephonymessagingkit/mmspartcontent/customheaders)
- [func addCustomHeader(MMSPartContent.MMSCustomHeader)](/documentation/telephonymessagingkit/mmspartcontent/addcustomheader(_:))
- [MMSPartContent.MMSCustomHeader](/documentation/telephonymessagingkit/mmspartcontent/mmscustomheader)

###### Accessing header properties

- [let key: String](/documentation/telephonymessagingkit/mmspartcontent/mmscustomheader/key)
- [let value: String](/documentation/telephonymessagingkit/mmspartcontent/mmscustomheader/value)
- [var subject: String?](/documentation/telephonymessagingkit/mmscontent/subject)
- [var headers: [String : String]](/documentation/telephonymessagingkit/mmscontent/headers)

###### Accessing message participants

- [var from: MMSHandle?](/documentation/telephonymessagingkit/mmscontent/from)
- [var recipients: [MMSHandle]](/documentation/telephonymessagingkit/mmscontent/recipients)
- [MMSHandle](/documentation/telephonymessagingkit/mmshandle)

###### Creating a handle

- [init(phoneNumber: String)](/documentation/telephonymessagingkit/mmshandle/init(phonenumber:))

###### Accessing handle properties

- [var phoneNumber: String](/documentation/telephonymessagingkit/mmshandle/phonenumber)

##### Accessing message properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/mmsmessage/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [var messageID: MMSMessageID](/documentation/telephonymessagingkit/mmsmessage/messageid)
- [MMSMessageID](/documentation/telephonymessagingkit/mmsmessageid)

###### Creating a message ID

- [init(rawValue: UInt32)](/documentation/telephonymessagingkit/mmsmessageid/init(rawvalue:))

###### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/mmsmessageid/description)

###### Working with raw values

- [let rawValue: UInt32](/documentation/telephonymessagingkit/mmsmessageid/rawvalue)
- [var totalSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/mmsmessage/totalsize)
- [var description: String](/documentation/telephonymessagingkit/mmsmessage/description)

#### Receiving messages

- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [MMSMessageID](/documentation/telephonymessagingkit/mmsmessageid)

##### Creating a message ID

- [init(rawValue: UInt32)](/documentation/telephonymessagingkit/mmsmessageid/init(rawvalue:))

##### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/mmsmessageid/description)

##### Working with raw values

- [let rawValue: UInt32](/documentation/telephonymessagingkit/mmsmessageid/rawvalue)
- [var incomingMessageNotifications: some AsyncSequence<MMSService.IncomingMessageNotification, Never>](/documentation/telephonymessagingkit/mmsservice/incomingmessagenotifications)
- [MMSService.IncomingMessageNotification](/documentation/telephonymessagingkit/mmsservice/incomingmessagenotification)

##### Inspecting notification properties

- [var message: MMSMessage](/documentation/telephonymessagingkit/mmsservice/incomingmessagenotification/message)

##### Deprecated properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/mmsservice/incomingmessagenotification/cellularserviceid)
- [var messageID: MMSMessageID](/documentation/telephonymessagingkit/mmsservice/incomingmessagenotification/messageid)

#### Reporting spam

- [func reportSpam(MMSMessage) async throws](/documentation/telephonymessagingkit/mmsservice/reportspam(_:))

#### Handling errors

- [MMSService.Error](/documentation/telephonymessagingkit/mmsservice/error)

##### Identifying errors

- [case unknown](/documentation/telephonymessagingkit/mmsservice/error/unknown)
- [case notSupported](/documentation/telephonymessagingkit/mmsservice/error/notsupported)
- [case invalidRecipient](/documentation/telephonymessagingkit/mmsservice/error/invalidrecipient)
- [case invalidMessageParts](/documentation/telephonymessagingkit/mmsservice/error/invalidmessageparts)
- [case internalError](/documentation/telephonymessagingkit/mmsservice/error/internalerror)
- [case mmsNotReady](/documentation/telephonymessagingkit/mmsservice/error/mmsnotready)
- [case mmsNotConfiguredForCarrier](/documentation/telephonymessagingkit/mmsservice/error/mmsnotconfiguredforcarrier)
- [case maximumSizeExceeded](/documentation/telephonymessagingkit/mmsservice/error/maximumsizeexceeded)

#### Deprecated symbols

- [func receiveMessage(using: CellularServiceID, messageID: MMSMessageID) async throws -> MMSMessage](/documentation/telephonymessagingkit/mmsservice/receivemessage(using:messageid:))

### Using Rich Communication Services (RCS)

- [var rcsService: RCSService](/documentation/telephonymessagingkit/telephonymessagingsession/rcsservice)
- [RCSService](/documentation/telephonymessagingkit/rcsservice)

#### Determining service viabililty

- [func isViable(for: CellularServiceID) -> Bool](/documentation/telephonymessagingkit/rcsservice/isviable(for:))
- [var viabilityNotifications: some AsyncSequence<RCSService.ViabilityNotification, Never>](/documentation/telephonymessagingkit/rcsservice/viabilitynotifications)
- [RCSService.ViabilityNotification](/documentation/telephonymessagingkit/rcsservice/viabilitynotification)

##### Instance Properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/viabilitynotification/cellularserviceid)
- [let isViable: Bool](/documentation/telephonymessagingkit/rcsservice/viabilitynotification/isviable)

#### Managing RCS configuration

- [func configuration(for: CellularServiceID) throws -> RCSService.Configuration](/documentation/telephonymessagingkit/rcsservice/configuration(for:))
- [RCSService.Configuration](/documentation/telephonymessagingkit/rcsservice/configuration)

##### Inspecting message configuration

- [var maximumTextMessageSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/configuration/maximumtextmessagesize)

##### Inspecting file transfer configuration

- [var maximumFileTransferSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/configuration/maximumfiletransfersize)
- [let fileTransferWarningSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/configuration/filetransferwarningsize)

##### Inspecting chat configuration

- [let chatRevokeTimeout: Duration?](/documentation/telephonymessagingkit/rcsservice/configuration/chatrevoketimeout)
- [var maximumGroupSize: Int?](/documentation/telephonymessagingkit/rcsservice/configuration/maximumgroupsize)

#### Sending messages

- [func sendMessage(RCSMessage.Text, to: RCSHandle, using: CellularServiceID, messageID: RCSMessageID) async throws](/documentation/telephonymessagingkit/rcsservice/sendmessage(_:to:using:messageid:)-70q7h)
- [RCSMessage.Text](/documentation/telephonymessagingkit/rcsmessage/text)

##### Creating a text instance

- [init(body: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(body:))
- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(stringliteral:))

##### Accessing text content

- [var body: String](/documentation/telephonymessagingkit/rcsmessage/text/body)
- [func sendMessage(RCSMessage.FileTransfer, to: RCSHandle, using: CellularServiceID, messageID: RCSMessageID) async throws](/documentation/telephonymessagingkit/rcsservice/sendmessage(_:to:using:messageid:)-63zct)
- [RCSMessage.FileTransfer](/documentation/telephonymessagingkit/rcsmessage/filetransfer)

##### Creating a file transfer instance

- [init(fileMetadata: RCSFileTransferMetadata, thumbnailMetadata: RCSFileTransferMetadata?)](/documentation/telephonymessagingkit/rcsmessage/filetransfer/init(filemetadata:thumbnailmetadata:))
- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

###### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

###### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

###### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)

##### Accessing file transfer properties

- [var fileMetadata: RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsmessage/filetransfer/filemetadata)
- [var thumbnailMetadata: RCSFileTransferMetadata?](/documentation/telephonymessagingkit/rcsmessage/filetransfer/thumbnailmetadata)
- [func sendMessage(RCSMessage.ComposingIndicator, to: RCSHandle, using: CellularServiceID, messageID: RCSMessageID) async throws](/documentation/telephonymessagingkit/rcsservice/sendmessage(_:to:using:messageid:)-9i178)
- [RCSMessage.ComposingIndicator](/documentation/telephonymessagingkit/rcsmessage/composingindicator)

##### Creating a composing indicator instance

- [init(state: RCSMessage.ComposingIndicator.State, lastActive: Date?, contentType: UTType?, refreshInterval: Duration?)](/documentation/telephonymessagingkit/rcsmessage/composingindicator/init(state:lastactive:contenttype:refreshinterval:))

##### Accessing composing indicator properties

- [var state: RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.property)
- [RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum)

###### Working with composing indicator states

- [case active](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/active)
- [case idle](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/idle)
- [var lastActive: Date?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/lastactive)
- [var contentType: UTType?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/contenttype)
- [UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct)
- [var refreshInterval: Duration?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/refreshinterval)
- [func sendMessage(RCSMessage.GeolocationPush, to: RCSHandle, using: CellularServiceID, messageID: RCSMessageID) async throws](/documentation/telephonymessagingkit/rcsservice/sendmessage(_:to:using:messageid:)-y1z)
- [RCSMessage.GeolocationPush](/documentation/telephonymessagingkit/rcsmessage/geolocationpush)

##### Accessing geolocation properties

- [var latitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/latitude)
- [var longitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/longitude)

##### Initializers

- [init(latitude: Double, longitude: Double, description: String?)](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/init(latitude:longitude:description:))

##### Instance Properties

- [var description: String?](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/description)
- [func sendMessage(RCSMessage.DispositionNotification, to: RCSHandle.URI, using: CellularServiceID, messageID: RCSMessageID, group: RCSHandle.Group?) async throws](/documentation/telephonymessagingkit/rcsservice/sendmessage(_:to:using:messageid:group:))
- [RCSMessage.DispositionNotification](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification)

##### Creating a disposition notification instance

- [init(disposition: RCSMessage.Disposition, disposedMessageID: RCSMessageID)](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/init(disposition:disposedmessageid:))

##### Accessing disposition notification properties

- [let disposition: RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposition)
- [RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/disposition)

###### Accessing disposition values

- [case delivered](/documentation/telephonymessagingkit/rcsmessage/disposition/delivered)
- [case deliveryFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/deliveryfailed)
- [case displayed](/documentation/telephonymessagingkit/rcsmessage/disposition/displayed)
- [case interworkingDelivered](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingdelivered)
- [case interworkingFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingfailed)
- [let disposedMessageID: RCSMessageID](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposedmessageid)
- [RCSHandle](/documentation/telephonymessagingkit/rcshandle)

##### Creating a handle

- [static func phoneNumber(String) -> RCSHandle?](/documentation/telephonymessagingkit/rcshandle/phonenumber(_:))

##### Accessing handle values

- [case uri(RCSHandle.URI)](/documentation/telephonymessagingkit/rcshandle/uri(_:))
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case group(RCSHandle.Group)](/documentation/telephonymessagingkit/rcshandle/group(_:))
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)

##### Describing an RCS handle

- [var description: String](/documentation/telephonymessagingkit/rcshandle/description)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [RCSMessageID](/documentation/telephonymessagingkit/rcsmessageid)

##### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/rcsmessageid/description)

#### Receiving messages

- [var incomingMessageNotifications: some AsyncSequence<RCSService.IncomingMessageNotification, Never>](/documentation/telephonymessagingkit/rcsservice/incomingmessagenotifications)
- [RCSService.IncomingMessageNotification](/documentation/telephonymessagingkit/rcsservice/incomingmessagenotification)

##### Inspecting notification properties

- [let message: RCSMessage](/documentation/telephonymessagingkit/rcsservice/incomingmessagenotification/message)
- [let groupContext: RCSGroupContext?](/documentation/telephonymessagingkit/rcsservice/incomingmessagenotification/groupcontext)
- [RCSGroupContext](/documentation/telephonymessagingkit/rcsgroupcontext)

###### Accessing group context properties

- [let handle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsgroupcontext/handle)
- [let suggestions: [RCSService.Business.Suggestion]](/documentation/telephonymessagingkit/rcsservice/incomingmessagenotification/suggestions)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)
- [RCSMessage](/documentation/telephonymessagingkit/rcsmessage)

##### Accessing message content

- [let content: RCSMessage.Content](/documentation/telephonymessagingkit/rcsmessage/content-swift.property)
- [RCSMessage.Content](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum)

###### Working with text content

- [case text(RCSMessage.Text)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/text(_:))
- [RCSMessage.Text](/documentation/telephonymessagingkit/rcsmessage/text)

###### Creating a text instance

- [init(body: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(body:))
- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(stringliteral:))

###### Accessing text content

- [var body: String](/documentation/telephonymessagingkit/rcsmessage/text/body)

###### Working with file transfers

- [case fileTransfer(RCSMessage.FileTransfer)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/filetransfer(_:))
- [RCSMessage.FileTransfer](/documentation/telephonymessagingkit/rcsmessage/filetransfer)

###### Creating a file transfer instance

- [init(fileMetadata: RCSFileTransferMetadata, thumbnailMetadata: RCSFileTransferMetadata?)](/documentation/telephonymessagingkit/rcsmessage/filetransfer/init(filemetadata:thumbnailmetadata:))
- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

###### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

###### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

###### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)

###### Accessing file transfer properties

- [var fileMetadata: RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsmessage/filetransfer/filemetadata)
- [var thumbnailMetadata: RCSFileTransferMetadata?](/documentation/telephonymessagingkit/rcsmessage/filetransfer/thumbnailmetadata)

###### Working with geolocation pushes

- [case geolocationPush(RCSMessage.GeolocationPush)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/geolocationpush(_:))
- [RCSMessage.GeolocationPush](/documentation/telephonymessagingkit/rcsmessage/geolocationpush)

###### Accessing geolocation properties

- [var latitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/latitude)
- [var longitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/longitude)

###### Initializers

- [init(latitude: Double, longitude: Double, description: String?)](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/init(latitude:longitude:description:))

###### Instance Properties

- [var description: String?](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/description)

###### Working with composing indicators

- [case composingIndicator(RCSMessage.ComposingIndicator)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/composingindicator(_:))
- [RCSMessage.ComposingIndicator](/documentation/telephonymessagingkit/rcsmessage/composingindicator)

###### Creating a composing indicator instance

- [init(state: RCSMessage.ComposingIndicator.State, lastActive: Date?, contentType: UTType?, refreshInterval: Duration?)](/documentation/telephonymessagingkit/rcsmessage/composingindicator/init(state:lastactive:contenttype:refreshinterval:))

###### Accessing composing indicator properties

- [var state: RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.property)
- [RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum)

###### Working with composing indicator states

- [case active](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/active)
- [case idle](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/idle)
- [var lastActive: Date?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/lastactive)
- [var contentType: UTType?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/contenttype)
- [UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct)
- [var refreshInterval: Duration?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/refreshinterval)

###### Working with disposition notifications

- [case dispositionNotification(RCSMessage.DispositionNotification)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/dispositionnotification(_:))
- [RCSMessage.DispositionNotification](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification)

###### Creating a disposition notification instance

- [init(disposition: RCSMessage.Disposition, disposedMessageID: RCSMessageID)](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/init(disposition:disposedmessageid:))

###### Accessing disposition notification properties

- [let disposition: RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposition)
- [RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/disposition)

###### Accessing disposition values

- [case delivered](/documentation/telephonymessagingkit/rcsmessage/disposition/delivered)
- [case deliveryFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/deliveryfailed)
- [case displayed](/documentation/telephonymessagingkit/rcsmessage/disposition/displayed)
- [case interworkingDelivered](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingdelivered)
- [case interworkingFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingfailed)
- [let disposedMessageID: RCSMessageID](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposedmessageid)

###### Working with business messages

- [case businessCard(RCSService.Business.Card)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/businesscard(_:))
- [RCSService.Business.Card](/documentation/telephonymessagingkit/rcsservice/business/card)

###### Accessing card properties

- [let content: RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.property)
- [RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct)

###### Accessing content properties

- [let media: RCSService.Business.Card.Media?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/media)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [let title: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/description)
- [let suggestions: [RCSService.Business.Suggestion]](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/suggestions)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)
- [let titleFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/titlefontstyle)
- [let descriptionFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/descriptionfontstyle)
- [RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle)

###### Determining font styles

- [static let italics: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/italics)
- [static let bold: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/bold)
- [static let underline: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/underline)
- [let imageAlignment: RCSService.Business.Card.ImageAlignment?](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.property)
- [RCSService.Business.Card.ImageAlignment](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum)

###### Determining image alignment

- [case left](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum/left)
- [case right](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum/right)
- [let orientation: RCSService.Business.Card.Orientation](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.property)
- [RCSService.Business.Card.Orientation](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum)

###### Determining orientation

- [case vertical](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum/vertical)
- [case horizontal](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum/horizontal)
- [let styleSheetURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/stylesheeturl)

###### Supporting types

- [RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/card/width)

###### Determining width

- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/width/medium)
- [case small](/documentation/telephonymessagingkit/rcsservice/business/card/width/small)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [case businessCardCarousel(RCSService.Business.CardCarousel)](/documentation/telephonymessagingkit/rcsmessage/content-swift.enum/businesscardcarousel(_:))
- [RCSService.Business.CardCarousel](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel)

###### Accessing card carousel properties

- [let width: RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/width)
- [RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/card/width)

###### Determining width

- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/width/medium)
- [case small](/documentation/telephonymessagingkit/rcsservice/business/card/width/small)
- [let titleFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/titlefontstyle)
- [let descriptionFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/descriptionfontstyle)
- [RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle)

###### Determining font styles

- [static let italics: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/italics)
- [static let bold: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/bold)
- [static let underline: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/underline)
- [let styleSheetURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/stylesheeturl)
- [let contents: [RCSService.Business.Card.Content]](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/contents)
- [RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct)

###### Accessing content properties

- [let media: RCSService.Business.Card.Media?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/media)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [let title: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/description)
- [let suggestions: [RCSService.Business.Suggestion]](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/suggestions)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)

##### Working with content types

- [RCSMessage.Text](/documentation/telephonymessagingkit/rcsmessage/text)

###### Creating a text instance

- [init(body: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(body:))
- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcsmessage/text/init(stringliteral:))

###### Accessing text content

- [var body: String](/documentation/telephonymessagingkit/rcsmessage/text/body)
- [RCSMessage.FileTransfer](/documentation/telephonymessagingkit/rcsmessage/filetransfer)

###### Creating a file transfer instance

- [init(fileMetadata: RCSFileTransferMetadata, thumbnailMetadata: RCSFileTransferMetadata?)](/documentation/telephonymessagingkit/rcsmessage/filetransfer/init(filemetadata:thumbnailmetadata:))
- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

###### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

###### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

###### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)

###### Accessing file transfer properties

- [var fileMetadata: RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsmessage/filetransfer/filemetadata)
- [var thumbnailMetadata: RCSFileTransferMetadata?](/documentation/telephonymessagingkit/rcsmessage/filetransfer/thumbnailmetadata)
- [RCSMessage.GeolocationPush](/documentation/telephonymessagingkit/rcsmessage/geolocationpush)

###### Accessing geolocation properties

- [var latitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/latitude)
- [var longitude: Double](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/longitude)

###### Initializers

- [init(latitude: Double, longitude: Double, description: String?)](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/init(latitude:longitude:description:))

###### Instance Properties

- [var description: String?](/documentation/telephonymessagingkit/rcsmessage/geolocationpush/description)
- [RCSMessage.DispositionNotification](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification)

###### Creating a disposition notification instance

- [init(disposition: RCSMessage.Disposition, disposedMessageID: RCSMessageID)](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/init(disposition:disposedmessageid:))

###### Accessing disposition notification properties

- [let disposition: RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposition)
- [RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/disposition)

###### Accessing disposition values

- [case delivered](/documentation/telephonymessagingkit/rcsmessage/disposition/delivered)
- [case deliveryFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/deliveryfailed)
- [case displayed](/documentation/telephonymessagingkit/rcsmessage/disposition/displayed)
- [case interworkingDelivered](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingdelivered)
- [case interworkingFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingfailed)
- [let disposedMessageID: RCSMessageID](/documentation/telephonymessagingkit/rcsmessage/dispositionnotification/disposedmessageid)
- [RCSMessage.Disposition](/documentation/telephonymessagingkit/rcsmessage/disposition)

###### Accessing disposition values

- [case delivered](/documentation/telephonymessagingkit/rcsmessage/disposition/delivered)
- [case deliveryFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/deliveryfailed)
- [case displayed](/documentation/telephonymessagingkit/rcsmessage/disposition/displayed)
- [case interworkingDelivered](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingdelivered)
- [case interworkingFailed](/documentation/telephonymessagingkit/rcsmessage/disposition/interworkingfailed)
- [RCSMessage.ComposingIndicator](/documentation/telephonymessagingkit/rcsmessage/composingindicator)

###### Creating a composing indicator instance

- [init(state: RCSMessage.ComposingIndicator.State, lastActive: Date?, contentType: UTType?, refreshInterval: Duration?)](/documentation/telephonymessagingkit/rcsmessage/composingindicator/init(state:lastactive:contenttype:refreshinterval:))

###### Accessing composing indicator properties

- [var state: RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.property)
- [RCSMessage.ComposingIndicator.State](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum)

###### Working with composing indicator states

- [case active](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/active)
- [case idle](/documentation/telephonymessagingkit/rcsmessage/composingindicator/state-swift.enum/idle)
- [var lastActive: Date?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/lastactive)
- [var contentType: UTType?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/contenttype)
- [UTType](/documentation/uniformtypeidentifiers/uttype-swift.struct)
- [var refreshInterval: Duration?](/documentation/telephonymessagingkit/rcsmessage/composingindicator/refreshinterval)

##### Accessing message properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsmessage/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let handle: RCSHandle](/documentation/telephonymessagingkit/rcsmessage/handle)
- [RCSHandle](/documentation/telephonymessagingkit/rcshandle)

###### Creating a handle

- [static func phoneNumber(String) -> RCSHandle?](/documentation/telephonymessagingkit/rcshandle/phonenumber(_:))

###### Accessing handle values

- [case uri(RCSHandle.URI)](/documentation/telephonymessagingkit/rcshandle/uri(_:))
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case group(RCSHandle.Group)](/documentation/telephonymessagingkit/rcshandle/group(_:))
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)

###### Describing an RCS handle

- [var description: String](/documentation/telephonymessagingkit/rcshandle/description)
- [let id: RCSMessageID](/documentation/telephonymessagingkit/rcsmessage/id)
- [RCSMessageID](/documentation/telephonymessagingkit/rcsmessageid)

###### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/rcsmessageid/description)

#### Revoking messages

- [func revokeMessage(RCSService.RevokeMessageRequest) async throws -> Bool](/documentation/telephonymessagingkit/rcsservice/revokemessage(_:))
- [RCSService.RevokeMessageRequest](/documentation/telephonymessagingkit/rcsservice/revokemessagerequest)

##### Creating a revoke request

- [init(cellularServiceID: CellularServiceID, handle: RCSHandle, messageID: RCSMessageID)](/documentation/telephonymessagingkit/rcsservice/revokemessagerequest/init(cellularserviceid:handle:messageid:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/revokemessagerequest/cellularserviceid)
- [var handle: RCSHandle](/documentation/telephonymessagingkit/rcsservice/revokemessagerequest/handle)
- [var messageID: RCSMessageID](/documentation/telephonymessagingkit/rcsservice/revokemessagerequest/messageid)

#### Transferring files

- [func upload(RCSService.FileUploadRequest) async throws -> RCSService.FileUploadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/upload(_:))
- [RCSService.FileUploadRequest](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest)

##### Creating a file upload request

- [init(cellularServiceID: CellularServiceID, fileURL: URL, contentType: UTType?, thumbnailURL: URL?, thumbnailContentType: UTType?)](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/init(cellularserviceid:fileurl:contenttype:thumbnailurl:thumbnailcontenttype:))

##### Accessing upload request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/cellularserviceid)
- [var fileURL: URL](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/fileurl)
- [var contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/contenttype)
- [var thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/thumbnailurl)
- [var thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/thumbnailcontenttype)

##### Accessing upload metadata

- [RCSService.FileUploadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata)

###### Accessing upload metadata

- [let transactionID: UUID](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/transactionid)
- [let fileMetadata: RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/filemetadata)
- [let thumbnailMetadata: RCSFileTransferMetadata?](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/thumbnailmetadata)
- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

###### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

###### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

###### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)
- [RCSService.FileUploadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata)

##### Accessing upload metadata

- [let transactionID: UUID](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/transactionid)
- [let fileMetadata: RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/filemetadata)
- [let thumbnailMetadata: RCSFileTransferMetadata?](/documentation/telephonymessagingkit/rcsservice/fileuploadrequest/metadata/thumbnailmetadata)
- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

###### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

###### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

###### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)
- [func download(RCSService.FileDownloadRequest) async throws -> RCSService.FileDownloadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/download(_:))
- [RCSService.FileDownloadRequest](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest)

##### Creating a download request

- [init(cellularServiceID: CellularServiceID, fileURL: URL, destinationFileURL: URL)](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/init(cellularserviceid:fileurl:destinationfileurl:))

##### Accessing download request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/cellularserviceid)
- [var fileURL: URL](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/fileurl)
- [var destinationFileURL: URL](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/destinationfileurl)

##### Accessing download metadata

- [RCSService.FileDownloadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata)

###### Accessing download request properties

- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata/contenttype)
- [let suggestedFileName: String?](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata/suggestedfilename)
- [RCSService.FileDownloadRequest.Metadata](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata)

##### Accessing download request properties

- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata/contenttype)
- [let suggestedFileName: String?](/documentation/telephonymessagingkit/rcsservice/filedownloadrequest/metadata/suggestedfilename)

#### Receiving handle updates

- [var remoteHandleUpdates: some AsyncSequence<RCSService.RemoteHandleUpdate, Never>](/documentation/telephonymessagingkit/rcsservice/remotehandleupdates)
- [RCSService.RemoteHandleUpdate](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate)

##### Accessing handle update properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let handle: RCSHandle](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate/handle)
- [let newHandle: RCSHandle?](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate/newhandle)
- [RCSHandle](/documentation/telephonymessagingkit/rcshandle)

###### Creating a handle

- [static func phoneNumber(String) -> RCSHandle?](/documentation/telephonymessagingkit/rcshandle/phonenumber(_:))

###### Accessing handle values

- [case uri(RCSHandle.URI)](/documentation/telephonymessagingkit/rcshandle/uri(_:))
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case group(RCSHandle.Group)](/documentation/telephonymessagingkit/rcshandle/group(_:))
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)

###### Describing an RCS handle

- [var description: String](/documentation/telephonymessagingkit/rcshandle/description)
- [let isBusinessHandle: Bool](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate/isbusinesshandle)
- [let capabilities: RCSService.RemoteCapabilities?](/documentation/telephonymessagingkit/rcsservice/remotehandleupdate/capabilities)

#### Reporting spam

- [func reportSpam(RCSService.ReportSpamRequest) async throws](/documentation/telephonymessagingkit/rcsservice/reportspam(_:))
- [RCSService.ReportSpamRequest](/documentation/telephonymessagingkit/rcsservice/reportspamrequest)

##### Creating a report spam request

- [init(message: RCSMessage, fileContent: Data?, category: RCSService.ReportSpamRequest.Category?, reason: String?)](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/init(message:filecontent:category:reason:))

##### Accessing request properties

- [var message: RCSMessage](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/message)
- [var fileContent: Data?](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/filecontent)
- [var category: RCSService.ReportSpamRequest.Category?](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.property)
- [RCSService.ReportSpamRequest.Category](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum)

###### Identifying spam categories

- [case invalid](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum/invalid)
- [case spam](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum/spam)
- [case fraud](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum/fraud)
- [case inappropriateContent](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum/inappropriatecontent)
- [case other](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/category-swift.enum/other)
- [var reason: String?](/documentation/telephonymessagingkit/rcsservice/reportspamrequest/reason)

#### Managing group chats

- [func createGroupChat(RCSService.CreateGroupChatRequest) async throws -> RCSService.CreateGroupChatRequest.Result](/documentation/telephonymessagingkit/rcsservice/creategroupchat(_:))
- [RCSService.CreateGroupChatRequest](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest)

##### Creating a group chat request

- [init(cellularServiceID: CellularServiceID, participants: [RCSHandle.URI], subject: String)](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/init(cellularserviceid:participants:subject:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/cellularserviceid)
- [var participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/participants)
- [var subject: String](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/subject)

##### Accessing the request result

- [RCSService.CreateGroupChatRequest.Result](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/result)

###### Accessing result properties

- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/result/grouphandle)
- [let participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/result/participants)
- [let subject: String?](/documentation/telephonymessagingkit/rcsservice/creategroupchatrequest/result/subject)
- [func leaveGroupChat(RCSService.LeaveGroupChatRequest) async throws](/documentation/telephonymessagingkit/rcsservice/leavegroupchat(_:))
- [RCSService.LeaveGroupChatRequest](/documentation/telephonymessagingkit/rcsservice/leavegroupchatrequest)

##### Creating a leave group chat request

- [init(cellularServiceID: CellularServiceID, groupHandle: RCSHandle.Group)](/documentation/telephonymessagingkit/rcsservice/leavegroupchatrequest/init(cellularserviceid:grouphandle:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/leavegroupchatrequest/cellularserviceid)
- [var groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/leavegroupchatrequest/grouphandle)
- [func addGroupChatParticipants(RCSService.AddGroupChatParticipantsRequest) async throws -> RCSService.AddGroupChatParticipantsRequest.Result](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipants(_:))
- [RCSService.AddGroupChatParticipantsRequest](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest)

##### Creating an add group chat participants request

- [init(cellularServiceID: CellularServiceID, groupHandle: RCSHandle.Group, participants: [RCSHandle.URI])](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/init(cellularserviceid:grouphandle:participants:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/cellularserviceid)
- [var groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/grouphandle)
- [var participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/participants)

##### Accessing the request result

- [RCSService.AddGroupChatParticipantsRequest.Result](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/result)

###### Accessing result properties

- [let added: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/addgroupchatparticipantsrequest/result/added)
- [func removeGroupChatParticipants(RCSService.RemoveGroupChatParticipantsRequest) async throws -> RCSService.RemoveGroupChatParticipantsRequest.Result](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipants(_:))
- [RCSService.RemoveGroupChatParticipantsRequest](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest)

##### Creating a remove group chat participants request

- [init(cellularServiceID: CellularServiceID, groupHandle: RCSHandle.Group, participants: [RCSHandle.URI])](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/init(cellularserviceid:grouphandle:participants:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/cellularserviceid)
- [var groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/grouphandle)
- [var participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/participants)

##### Accessing the request result

- [RCSService.RemoveGroupChatParticipantsRequest.Result](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/result)

###### Accessing result properties

- [let removed: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/removegroupchatparticipantsrequest/result/removed)
- [func changeGroupChatSubject(RCSService.ChangeGroupChatSubjectRequest) async throws](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubject(_:))
- [RCSService.ChangeGroupChatSubjectRequest](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubjectrequest)

##### Creating a change group chat subject request

- [init(cellularServiceID: CellularServiceID, groupHandle: RCSHandle.Group, newSubject: String)](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubjectrequest/init(cellularserviceid:grouphandle:newsubject:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubjectrequest/cellularserviceid)
- [var groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubjectrequest/grouphandle)
- [var newSubject: String](/documentation/telephonymessagingkit/rcsservice/changegroupchatsubjectrequest/newsubject)
- [var groupChatEvents: some AsyncSequence<RCSService.GroupChatEvent, Never>](/documentation/telephonymessagingkit/rcsservice/groupchatevents)
- [RCSService.GroupChatEvent](/documentation/telephonymessagingkit/rcsservice/groupchatevent)

##### Chat life cycle events

- [case started(RCSService.GroupChatStartedEvent)](/documentation/telephonymessagingkit/rcsservice/groupchatevent/started(_:))
- [RCSService.GroupChatStartedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent)

###### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/grouphandle)
- [let participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/participants)
- [let creator: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/creator)
- [let subject: String](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/subject)
- [case ended(RCSService.GroupChatEndedEvent)](/documentation/telephonymessagingkit/rcsservice/groupchatevent/ended(_:))
- [RCSService.GroupChatEndedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent)

###### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/grouphandle)
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)
- [let endedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/endedby)
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case subjectUpdated(RCSService.GroupChatSubjectUpdatedEvent)](/documentation/telephonymessagingkit/rcsservice/groupchatevent/subjectupdated(_:))
- [RCSService.GroupChatSubjectUpdatedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent)

###### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/grouphandle)
- [let newSubject: String](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/newsubject)
- [let changedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/changedby)

##### Participant events

- [case participantsAdded(RCSService.GroupChatParticipantsAddedEvent)](/documentation/telephonymessagingkit/rcsservice/groupchatevent/participantsadded(_:))
- [RCSService.GroupChatParticipantsAddedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent)

###### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/grouphandle)
- [let addedParticipants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/addedparticipants)
- [let addedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/addedby)
- [case participantsRemoved(RCSService.GroupChatParticipantsRemovedEvent)](/documentation/telephonymessagingkit/rcsservice/groupchatevent/participantsremoved(_:))
- [RCSService.GroupChatParticipantsRemovedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent)

###### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/grouphandle)
- [let removedParticipants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedparticipants)
- [let removedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedby)
- [let removedCurrentUser: Bool](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedcurrentuser)

#### Discovering remote capabilities

- [func remoteCapabilities(for: RCSService.RemoteCapabilitiesRequest) async throws -> RCSService.RemoteCapabilities?](/documentation/telephonymessagingkit/rcsservice/remotecapabilities(for:))
- [RCSService.RemoteCapabilitiesRequest](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest)

##### Creating a remote capabilities request

- [init(cellularServiceID: CellularServiceID, handle: RCSHandle, cachePolicy: RCSService.RemoteCapabilitiesRequest.CachePolicy)](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/init(cellularserviceid:handle:cachepolicy:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/cellularserviceid)
- [var handle: RCSHandle](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/handle)
- [var cachePolicy: RCSService.RemoteCapabilitiesRequest.CachePolicy](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/cachepolicy-swift.property)
- [RCSService.RemoteCapabilitiesRequest.CachePolicy](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/cachepolicy-swift.enum)

###### Accessing cache policies

- [case cacheOnly](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/cachepolicy-swift.enum/cacheonly)
- [case cacheOrRemote](/documentation/telephonymessagingkit/rcsservice/remotecapabilitiesrequest/cachepolicy-swift.enum/cacheorremote)
- [RCSService.RemoteCapabilities](/documentation/telephonymessagingkit/rcsservice/remotecapabilities)

##### Accessing handle metadata

- [let alternativeHandles: [RCSHandle]](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/alternativehandles)
- [RCSHandle](/documentation/telephonymessagingkit/rcshandle)

###### Creating a handle

- [static func phoneNumber(String) -> RCSHandle?](/documentation/telephonymessagingkit/rcshandle/phonenumber(_:))

###### Accessing handle values

- [case uri(RCSHandle.URI)](/documentation/telephonymessagingkit/rcshandle/uri(_:))
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case group(RCSHandle.Group)](/documentation/telephonymessagingkit/rcshandle/group(_:))
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)

###### Describing an RCS handle

- [var description: String](/documentation/telephonymessagingkit/rcshandle/description)
- [let isBusinessHandle: Bool](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/isbusinesshandle)

##### Accessing feature support

- [let supportsChat: Bool](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/supportschat)
- [let supportsFileTransfer: Bool](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/supportsfiletransfer)
- [let supportsGeolocation: Bool](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/supportsgeolocation)

##### Accessing availability

- [let availability: RCSService.RemoteCapabilities.Availability?](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/availability-swift.property)
- [RCSService.RemoteCapabilities.Availability](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/availability-swift.enum)

###### Determining availability

- [case available](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/availability-swift.enum/available)
- [case unavailable](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/availability-swift.enum/unavailable)

##### Determining capability validity

- [let validUntil: Date?](/documentation/telephonymessagingkit/rcsservice/remotecapabilities/validuntil)

#### Responding to business suggestions

- [func sendSuggestionResponse(RCSService.SuggestionResponse) async throws](/documentation/telephonymessagingkit/rcsservice/sendsuggestionresponse(_:))
- [RCSService.SuggestionResponse](/documentation/telephonymessagingkit/rcsservice/suggestionresponse)

##### Creating a suggestion response

- [init(cellularServiceID: CellularServiceID, destination: RCSHandle, messageID: RCSMessageID, originatingMessageID: RCSMessageID, suggestion: RCSService.Business.Suggestion)](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/init(cellularserviceid:destination:messageid:originatingmessageid:suggestion:))

##### Accessing response properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/cellularserviceid)
- [var destination: RCSHandle](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/destination)
- [RCSHandle](/documentation/telephonymessagingkit/rcshandle)

###### Creating a handle

- [static func phoneNumber(String) -> RCSHandle?](/documentation/telephonymessagingkit/rcshandle/phonenumber(_:))

###### Accessing handle values

- [case uri(RCSHandle.URI)](/documentation/telephonymessagingkit/rcshandle/uri(_:))
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [case group(RCSHandle.Group)](/documentation/telephonymessagingkit/rcshandle/group(_:))
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)

###### Describing an RCS handle

- [var description: String](/documentation/telephonymessagingkit/rcshandle/description)
- [var messageID: RCSMessageID](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/messageid)
- [var originatingMessageID: RCSMessageID](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/originatingmessageid)
- [RCSMessageID](/documentation/telephonymessagingkit/rcsmessageid)

###### Describing a message ID

- [var description: String](/documentation/telephonymessagingkit/rcsmessageid/description)
- [var suggestion: RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/suggestionresponse/suggestion)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)

#### Retrieving business information

- [func businessInformation(for: RCSService.BusinessInformationRequest) async throws -> RCSService.Business?](/documentation/telephonymessagingkit/rcsservice/businessinformation(for:))
- [RCSService.BusinessInformationRequest](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest)

##### Creating a business information request

- [init(cellularServiceID: CellularServiceID, handle: RCSHandle.URI, cachePolicy: RCSService.BusinessInformationRequest.CachePolicy)](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/init(cellularserviceid:handle:cachepolicy:))

##### Accessing request properties

- [var cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cellularserviceid)
- [var handle: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/handle)
- [var cachePolicy: RCSService.BusinessInformationRequest.CachePolicy](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cachepolicy-swift.property)
- [RCSService.BusinessInformationRequest.CachePolicy](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cachepolicy-swift.enum)

###### Inspecting cache policies

- [case cacheOnly](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cachepolicy-swift.enum/cacheonly)
- [case remoteOnly](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cachepolicy-swift.enum/remoteonly)
- [case cacheOrRemote](/documentation/telephonymessagingkit/rcsservice/businessinformationrequest/cachepolicy-swift.enum/cacheorremote)
- [RCSService.Business](/documentation/telephonymessagingkit/rcsservice/business)

##### Accessing business identity information

- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/description)
- [let providerName: String?](/documentation/telephonymessagingkit/rcsservice/business/providername)
- [let organizationNames: [RCSService.Business.OrganizationName]](/documentation/telephonymessagingkit/rcsservice/business/organizationnames)
- [RCSService.Business.OrganizationName](/documentation/telephonymessagingkit/rcsservice/business/organizationname)

###### Accessing organization name properties

- [let displayName: String](/documentation/telephonymessagingkit/rcsservice/business/organizationname/displayname)
- [let nameType: RCSService.Business.OrganizationName.NameType](/documentation/telephonymessagingkit/rcsservice/business/organizationname/nametype-swift.property)
- [RCSService.Business.OrganizationName.NameType](/documentation/telephonymessagingkit/rcsservice/business/organizationname/nametype-swift.enum)

###### Determining name type

- [case officialName](/documentation/telephonymessagingkit/rcsservice/business/organizationname/nametype-swift.enum/officialname)
- [let categoryNames: [String]](/documentation/telephonymessagingkit/rcsservice/business/categorynames)

##### Accessing business contact information

- [let communicationAddress: RCSService.Business.CommunicationAddress?](/documentation/telephonymessagingkit/rcsservice/business/communicationaddress-swift.property)
- [RCSService.Business.CommunicationAddress](/documentation/telephonymessagingkit/rcsservice/business/communicationaddress-swift.struct)

###### Accessing communication details

- [let telephoneDetails: RCSService.Business.TelephoneDetails](/documentation/telephonymessagingkit/rcsservice/business/communicationaddress-swift.struct/telephonedetails)
- [RCSService.Business.TelephoneDetails](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails)

###### Accessing telephone details

- [let label: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/label)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/phonenumber)
- [let phoneNumberType: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/phonenumbertype)
- [let uriEntries: [RCSService.Business.URIEntry]](/documentation/telephonymessagingkit/rcsservice/business/communicationaddress-swift.struct/urientries)
- [RCSService.Business.URIEntry](/documentation/telephonymessagingkit/rcsservice/business/urientry)

###### Accessing URI properties

- [let uri: URL](/documentation/telephonymessagingkit/rcsservice/business/urientry/uri)
- [let type: RCSService.Business.URIEntry.URIType](/documentation/telephonymessagingkit/rcsservice/business/urientry/type)
- [RCSService.Business.URIEntry.URIType](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype)

###### Determining URI type

- [case sip](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype/sip)
- [case other](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype/other)
- [let label: RCSService.Business.URIEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.property)
- [RCSService.Business.URIEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum)

###### Determining label type

- [case serviceID](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum/serviceid)
- [case sms](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum/sms)
- [let addressEntries: [RCSService.Business.AddressEntry]](/documentation/telephonymessagingkit/rcsservice/business/addressentries)
- [RCSService.Business.AddressEntry](/documentation/telephonymessagingkit/rcsservice/business/addressentry)

###### Accessing address details

- [let address: String](/documentation/telephonymessagingkit/rcsservice/business/addressentry/address)
- [let label: String](/documentation/telephonymessagingkit/rcsservice/business/addressentry/label)
- [let emailAddress: String?](/documentation/telephonymessagingkit/rcsservice/business/emailaddress)
- [let websiteURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/websiteurl)
- [let verificationDetails: RCSService.Business.VerificationDetails?](/documentation/telephonymessagingkit/rcsservice/business/verificationdetails-swift.property)
- [RCSService.Business.VerificationDetails](/documentation/telephonymessagingkit/rcsservice/business/verificationdetails-swift.struct)

###### Accessing verification properties

- [let isVerified: Bool](/documentation/telephonymessagingkit/rcsservice/business/verificationdetails-swift.struct/isverified)
- [let verifiedBy: String?](/documentation/telephonymessagingkit/rcsservice/business/verificationdetails-swift.struct/verifiedby)
- [let expirationDate: Date?](/documentation/telephonymessagingkit/rcsservice/business/verificationdetails-swift.struct/expirationdate)

##### Accessing terms and conditions

- [let termsAndConditionsURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/termsandconditionsurl)

##### Accessing display information

- [var themeColor: CGColor?](/documentation/telephonymessagingkit/rcsservice/business/themecolor)
- [let backgroundImageURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/backgroundimageurl)
- [let styleSheetTemplateURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/stylesheettemplateurl)
- [let persistentMenu: RCSService.Business.Menu?](/documentation/telephonymessagingkit/rcsservice/business/persistentmenu)
- [RCSService.Business.Menu](/documentation/telephonymessagingkit/rcsservice/business/menu)

###### Accessing menu properties

- [let title: String?](/documentation/telephonymessagingkit/rcsservice/business/menu/title)
- [let contents: [RCSService.Business.Menu.Content]](/documentation/telephonymessagingkit/rcsservice/business/menu/contents)
- [RCSService.Business.Menu.Content](/documentation/telephonymessagingkit/rcsservice/business/menu/content)

###### Determining content type

- [case submenu(RCSService.Business.Menu)](/documentation/telephonymessagingkit/rcsservice/business/menu/content/submenu(_:))
- [case suggestion(RCSService.Business.Suggestion)](/documentation/telephonymessagingkit/rcsservice/business/menu/content/suggestion(_:))
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)

##### Accessing media entries

- [let mediaEntries: [RCSService.Business.MediaEntry]](/documentation/telephonymessagingkit/rcsservice/business/mediaentries)
- [RCSService.Business.MediaEntry](/documentation/telephonymessagingkit/rcsservice/business/mediaentry)

###### Accessing media properties

- [let label: RCSService.Business.MediaEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/label-swift.property)
- [RCSService.Business.MediaEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/label-swift.enum)

###### Determining label type

- [case icon](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/label-swift.enum/icon)
- [let media: RCSService.Business.Media](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/media)
- [RCSService.Business.Media](/documentation/telephonymessagingkit/rcsservice/business/media)

###### Accessing media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/media/url)
- [let sha256Digest: String?](/documentation/telephonymessagingkit/rcsservice/business/media/sha256digest)
- [let contentType: RCSService.Business.MediaEntry.ContentType](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/contenttype-swift.property)
- [RCSService.Business.MediaEntry.ContentType](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/contenttype-swift.enum)

###### Determining content type

- [case logo](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/contenttype-swift.enum/logo)
- [case other](/documentation/telephonymessagingkit/rcsservice/business/mediaentry/contenttype-swift.enum/other)

##### Accessing version information

- [let version: String?](/documentation/telephonymessagingkit/rcsservice/business/version)

##### Supporting types

- [RCSService.Business.Card](/documentation/telephonymessagingkit/rcsservice/business/card)

###### Accessing card properties

- [let content: RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.property)
- [RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct)

###### Accessing content properties

- [let media: RCSService.Business.Card.Media?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/media)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [let title: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/description)
- [let suggestions: [RCSService.Business.Suggestion]](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/suggestions)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)
- [let titleFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/titlefontstyle)
- [let descriptionFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/descriptionfontstyle)
- [RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle)

###### Determining font styles

- [static let italics: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/italics)
- [static let bold: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/bold)
- [static let underline: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/underline)
- [let imageAlignment: RCSService.Business.Card.ImageAlignment?](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.property)
- [RCSService.Business.Card.ImageAlignment](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum)

###### Determining image alignment

- [case left](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum/left)
- [case right](/documentation/telephonymessagingkit/rcsservice/business/card/imagealignment-swift.enum/right)
- [let orientation: RCSService.Business.Card.Orientation](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.property)
- [RCSService.Business.Card.Orientation](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum)

###### Determining orientation

- [case vertical](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum/vertical)
- [case horizontal](/documentation/telephonymessagingkit/rcsservice/business/card/orientation-swift.enum/horizontal)
- [let styleSheetURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/stylesheeturl)

###### Supporting types

- [RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/card/width)

###### Determining width

- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/width/medium)
- [case small](/documentation/telephonymessagingkit/rcsservice/business/card/width/small)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [RCSService.Business.CardCarousel](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel)

###### Accessing card carousel properties

- [let width: RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/width)
- [RCSService.Business.Card.Width](/documentation/telephonymessagingkit/rcsservice/business/card/width)

###### Determining width

- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/width/medium)
- [case small](/documentation/telephonymessagingkit/rcsservice/business/card/width/small)
- [let titleFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/titlefontstyle)
- [let descriptionFontStyle: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/descriptionfontstyle)
- [RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle)

###### Determining font styles

- [static let italics: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/italics)
- [static let bold: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/bold)
- [static let underline: RCSService.Business.Card.FontStyle](/documentation/telephonymessagingkit/rcsservice/business/card/fontstyle/underline)
- [let styleSheetURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/stylesheeturl)
- [let contents: [RCSService.Business.Card.Content]](/documentation/telephonymessagingkit/rcsservice/business/cardcarousel/contents)
- [RCSService.Business.Card.Content](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct)

###### Accessing content properties

- [let media: RCSService.Business.Card.Media?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/media)
- [RCSService.Business.Card.Media](/documentation/telephonymessagingkit/rcsservice/business/card/media)

###### Accessing card media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/card/media/url)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/contenttype)
- [let fileSize: Measurement<UnitInformationStorage>](/documentation/telephonymessagingkit/rcsservice/business/card/media/filesize)
- [let thumbnailURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailurl)
- [let thumbnailContentType: UTType?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailcontenttype)
- [let thumbnailFileSize: Measurement<UnitInformationStorage>?](/documentation/telephonymessagingkit/rcsservice/business/card/media/thumbnailfilesize)
- [let displayHeight: RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/displayheight)
- [RCSService.Business.Card.Media.Height](/documentation/telephonymessagingkit/rcsservice/business/card/media/height)

###### Determining height

- [case short](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/short)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/medium)
- [case tall](/documentation/telephonymessagingkit/rcsservice/business/card/media/height/tall)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/media/description)
- [let title: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/description)
- [let suggestions: [RCSService.Business.Suggestion]](/documentation/telephonymessagingkit/rcsservice/business/card/content-swift.struct/suggestions)
- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)
- [RCSService.Business.Media](/documentation/telephonymessagingkit/rcsservice/business/media)

###### Accessing media properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/media/url)
- [let sha256Digest: String?](/documentation/telephonymessagingkit/rcsservice/business/media/sha256digest)
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)
- [RCSService.Business.TelephoneDetails](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails)

###### Accessing telephone details

- [let label: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/label)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/phonenumber)
- [let phoneNumberType: String](/documentation/telephonymessagingkit/rcsservice/business/telephonedetails/phonenumbertype)
- [RCSService.Business.URIEntry](/documentation/telephonymessagingkit/rcsservice/business/urientry)

###### Accessing URI properties

- [let uri: URL](/documentation/telephonymessagingkit/rcsservice/business/urientry/uri)
- [let type: RCSService.Business.URIEntry.URIType](/documentation/telephonymessagingkit/rcsservice/business/urientry/type)
- [RCSService.Business.URIEntry.URIType](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype)

###### Determining URI type

- [case sip](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype/sip)
- [case other](/documentation/telephonymessagingkit/rcsservice/business/urientry/uritype/other)
- [let label: RCSService.Business.URIEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.property)
- [RCSService.Business.URIEntry.Label](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum)

###### Determining label type

- [case serviceID](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum/serviceid)
- [case sms](/documentation/telephonymessagingkit/rcsservice/business/urientry/label-swift.enum/sms)

##### Enumerations

- [RCSService.Business.Suggestion](/documentation/telephonymessagingkit/rcsservice/business/suggestion)

###### Determining suggestion type

- [case action(RCSService.Business.SuggestedAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/action(_:))
- [RCSService.Business.SuggestedAction](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction)

###### Accessing suggested action properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/displaytext)
- [let action: RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.property)
- [RCSService.Business.SuggestedAction.Action](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum)

###### Handling URL and phone-dialing actions

- [case openURL(RCSService.Business.OpenURLAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/openurl(_:))
- [RCSService.Business.OpenURLAction](/documentation/telephonymessagingkit/rcsservice/business/openurlaction)

###### Accessing action properties

- [let url: URL](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/url)
- [let target: RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.property)
- [RCSService.Business.OpenURLAction.Target](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum)

###### Accessing targets

- [case defaultBrowser](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/defaultbrowser)
- [case inApp(detent: RCSService.Business.OpenURLAction.Detent)](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/target-swift.enum/inapp(detent:))
- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)

###### Supporting types

- [RCSService.Business.OpenURLAction.Detent](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent)

###### Accessing detent values

- [case large](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/large)
- [case medium](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/medium)
- [case mediumLarge](/documentation/telephonymessagingkit/rcsservice/business/openurlaction/detent/mediumlarge)
- [case dialPhoneNumber(RCSService.Business.DialPhoneNumberAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/dialphonenumber(_:))
- [RCSService.Business.DialPhoneNumberAction](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/phonenumber)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/dialphonenumberaction/fallbackurl)

###### Handling location actions

- [case showLocation(RCSService.Business.ShowLocationAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/showlocation(_:))
- [RCSService.Business.ShowLocationAction](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction)

###### Accessing action properties

- [let method: RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.property)
- [RCSService.Business.ShowLocationAction.Method](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum)

###### Determining location method

- [case coordinates(CLLocationCoordinate2D)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/coordinates(_:))
- [CLLocationCoordinate2D](/documentation/corelocation/cllocationcoordinate2d)
- [case query(String)](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/method-swift.enum/query(_:))
- [let label: String?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/label)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/showlocationaction/fallbackurl)
- [case sendLocation](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/sendlocation)

###### Handling calendar event actions

- [case createCalendarEvent(RCSService.Business.CreateCalendarEventAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/createcalendarevent(_:))
- [RCSService.Business.CreateCalendarEventAction](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction)

###### Accessing action properties

- [let startTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/starttime)
- [let endTime: Date](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/endtime)
- [let title: String](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/title)
- [let description: String?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/description)
- [let fallbackURL: URL?](/documentation/telephonymessagingkit/rcsservice/business/createcalendareventaction/fallbackurl)

###### Handling composition actions

- [case composeText(RCSService.Business.ComposeTextAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composetext(_:))
- [RCSService.Business.ComposeTextAction](/documentation/telephonymessagingkit/rcsservice/business/composetextaction)

###### Accessing action properties

- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/phonenumber)
- [let text: String](/documentation/telephonymessagingkit/rcsservice/business/composetextaction/text)
- [case composeRecording(RCSService.Business.ComposeRecordingAction)](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/composerecording(_:))
- [RCSService.Business.ComposeRecordingAction](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction)

###### Accessing action properties

- [let mediaType: RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.property)
- [RCSService.Business.ComposeRecordingAction.MediaType](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum)

###### Acccessing media types

- [case audio](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/audio)
- [case video](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/mediatype-swift.enum/video)
- [let phoneNumber: String](/documentation/telephonymessagingkit/rcsservice/business/composerecordingaction/phonenumber)

###### Handling local behavior actions

- [case sendDeviceSpecifics](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/senddevicespecifics)
- [case enableDisplayedNotifications](/documentation/telephonymessagingkit/rcsservice/business/suggestedaction/action-swift.enum/enabledisplayednotifications)
- [case reply(RCSService.Business.SuggestedReply)](/documentation/telephonymessagingkit/rcsservice/business/suggestion/reply(_:))
- [RCSService.Business.SuggestedReply](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply)

###### Accessing reply properties

- [let displayText: String](/documentation/telephonymessagingkit/rcsservice/business/suggestedreply/displaytext)

#### Handling errors

- [RCSService.Error](/documentation/telephonymessagingkit/rcsservice/error)

##### Identifying errors

- [case serviceUnavailable](/documentation/telephonymessagingkit/rcsservice/error/serviceunavailable)
- [case invalidArgument](/documentation/telephonymessagingkit/rcsservice/error/invalidargument)
- [case decodingFailed](/documentation/telephonymessagingkit/rcsservice/error/decodingfailed)
- [case notSupported](/documentation/telephonymessagingkit/rcsservice/error/notsupported)
- [case unknown](/documentation/telephonymessagingkit/rcsservice/error/unknown)
- [case temporaryError](/documentation/telephonymessagingkit/rcsservice/error/temporaryerror)
- [case permanentError](/documentation/telephonymessagingkit/rcsservice/error/permanenterror)
- [case internalError](/documentation/telephonymessagingkit/rcsservice/error/internalerror)
- [case notFound](/documentation/telephonymessagingkit/rcsservice/error/notfound)
- [case maximumSizeExceeded](/documentation/telephonymessagingkit/rcsservice/error/maximumsizeexceeded)

#### Supporting types

- [RCSService.GroupChatEndedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent)

##### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/cellularserviceid)
- [CellularServiceID](/documentation/telephonymessagingkit/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/grouphandle)
- [RCSHandle.Group](/documentation/telephonymessagingkit/rcshandle/group)

###### Accessing group properties

- [let focus: String](/documentation/telephonymessagingkit/rcshandle/group/focus)
- [let conversationID: String](/documentation/telephonymessagingkit/rcshandle/group/conversationid)
- [let endedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatendedevent/endedby)
- [RCSHandle.URI](/documentation/telephonymessagingkit/rcshandle/uri)

###### Creating a URI instance

- [init(stringLiteral: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(stringliteral:))

###### Working with raw values

- [init(rawValue: String)](/documentation/telephonymessagingkit/rcshandle/uri/init(rawvalue:))
- [let rawValue: String](/documentation/telephonymessagingkit/rcshandle/uri/rawvalue)
- [RCSService.GroupChatParticipantsAddedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent)

##### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/grouphandle)
- [let addedParticipants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/addedparticipants)
- [let addedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsaddedevent/addedby)
- [RCSService.GroupChatParticipantsRemovedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent)

##### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/grouphandle)
- [let removedParticipants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedparticipants)
- [let removedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedby)
- [let removedCurrentUser: Bool](/documentation/telephonymessagingkit/rcsservice/groupchatparticipantsremovedevent/removedcurrentuser)
- [RCSService.GroupChatStartedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent)

##### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/grouphandle)
- [let participants: [RCSHandle.URI]](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/participants)
- [let creator: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/creator)
- [let subject: String](/documentation/telephonymessagingkit/rcsservice/groupchatstartedevent/subject)
- [RCSService.GroupChatSubjectUpdatedEvent](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent)

##### Accessing event properties

- [let cellularServiceID: CellularServiceID](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/cellularserviceid)
- [let groupHandle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/grouphandle)
- [let newSubject: String](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/newsubject)
- [let changedBy: RCSHandle.URI](/documentation/telephonymessagingkit/rcsservice/groupchatsubjectupdatedevent/changedby)

#### Instance Methods

- [func sendDeviceSpecifics(to: RCSHandle.URI, using: CellularServiceID, messageID: RCSMessageID) async throws](/documentation/telephonymessagingkit/rcsservice/senddevicespecifics(to:using:messageid:))

### Accessing session properties

- [let id: UUID](/documentation/telephonymessagingkit/telephonymessagingsession/id)

### Handling errors

- [TelephonyMessagingSession.Error](/documentation/telephonymessagingkit/telephonymessagingsession/error)

#### Inspecting errors

- [case invalidSession](/documentation/telephonymessagingkit/telephonymessagingsession/error/invalidsession)
- [case serviceUnavailable](/documentation/telephonymessagingkit/telephonymessagingsession/error/serviceunavailable)
- [case invalidArgument](/documentation/telephonymessagingkit/telephonymessagingsession/error/invalidargument)
- [case internalError](/documentation/telephonymessagingkit/telephonymessagingsession/error/internalerror)

### Instance Properties

- [var isConfiguredForCarrierMessaging: Bool](/documentation/telephonymessagingkit/telephonymessagingsession/isconfiguredforcarriermessaging)
- [Default Carrier Messaging App](/documentation/bundleresources/entitlements/com.apple.developer.carrier-messaging-app)

## Supporting types

- [RCSFileTransferMetadata](/documentation/telephonymessagingkit/rcsfiletransfermetadata)

### Accessing file metadata

- [let url: URL](/documentation/telephonymessagingkit/rcsfiletransfermetadata/url)
- [let fileName: String?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filename)
- [let fileSize: Int](/documentation/telephonymessagingkit/rcsfiletransfermetadata/filesize)
- [let contentType: UTType?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/contenttype)
- [let expirationDate: Date](/documentation/telephonymessagingkit/rcsfiletransfermetadata/expirationdate)
- [var playbackLength: Duration?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/playbacklength)

### Working with file disposition

- [var disposition: RCSFileTransferMetadata.Disposition?](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.property)
- [RCSFileTransferMetadata.Disposition](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum)

#### Working with dispositions

- [case attachment](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/attachment)
- [case render](/documentation/telephonymessagingkit/rcsfiletransfermetadata/disposition-swift.enum/render)
- [RCSGroupContext](/documentation/telephonymessagingkit/rcsgroupcontext)

### Accessing group context properties

- [let handle: RCSHandle.Group](/documentation/telephonymessagingkit/rcsgroupcontext/handle)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
