# Message UI Documentation

Source: https://sosumi.ai/documentation/messageui

---
title: Message UI
source: https://developer.apple.com/documentation/messageui
timestamp: 2026-02-13T18:59:33.049Z
---

## Email composition interface

- [MFMailComposeViewController](/documentation/messageui/mfmailcomposeviewcontroller)

### Responding to the view controller dismissal

- [var mailComposeDelegate: (any MFMailComposeViewControllerDelegate)?](/documentation/messageui/mfmailcomposeviewcontroller/mailcomposedelegate)
- [MFMailComposeViewControllerDelegate](/documentation/messageui/mfmailcomposeviewcontrollerdelegate)

#### Responding to Email Completion

- [func mailComposeController(MFMailComposeViewController, didFinishWith: MFMailComposeResult, error: (any Error)?)](/documentation/messageui/mfmailcomposeviewcontrollerdelegate/mailcomposecontroller(_:didfinishwith:error:))
- [MFMailComposeResult](/documentation/messageui/mfmailcomposeresult)

##### Constants

- [case cancelled](/documentation/messageui/mfmailcomposeresult/cancelled)
- [case saved](/documentation/messageui/mfmailcomposeresult/saved)
- [case sent](/documentation/messageui/mfmailcomposeresult/sent)
- [case failed](/documentation/messageui/mfmailcomposeresult/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/messageui/mfmailcomposeresult/init(rawvalue:))

##### Default Implementations

- [Equatable Implementations](/documentation/messageui/mfmailcomposeresult/equatable-implementations)

###### Operators

- [static func != (Self, Self) -> Bool](/documentation/messageui/mfmailcomposeresult/!=(_:_:))
- [RawRepresentable Implementations](/documentation/messageui/mfmailcomposeresult/rawrepresentable-implementations)

###### Instance Properties

- [var hashValue: Int](/documentation/messageui/mfmailcomposeresult/hashvalue)

###### Instance Methods

- [func hash(into: inout Hasher)](/documentation/messageui/mfmailcomposeresult/hash(into:))

### Determining mail availability

- [class func canSendMail() -> Bool](/documentation/messageui/mfmailcomposeviewcontroller/cansendmail())

### Setting mail fields programmatically

- [func setSubject(String)](/documentation/messageui/mfmailcomposeviewcontroller/setsubject(_:))
- [func setToRecipients([String]?)](/documentation/messageui/mfmailcomposeviewcontroller/settorecipients(_:))
- [func setCcRecipients([String]?)](/documentation/messageui/mfmailcomposeviewcontroller/setccrecipients(_:))
- [func setBccRecipients([String]?)](/documentation/messageui/mfmailcomposeviewcontroller/setbccrecipients(_:))
- [func setMessageBody(String, isHTML: Bool)](/documentation/messageui/mfmailcomposeviewcontroller/setmessagebody(_:ishtml:))
- [func addAttachmentData(Data, mimeType: String, fileName: String)](/documentation/messageui/mfmailcomposeviewcontroller/addattachmentdata(_:mimetype:filename:))
- [func setPreferredSendingEmailAddress(String)](/documentation/messageui/mfmailcomposeviewcontroller/setpreferredsendingemailaddress(_:))

### Responding to errors

- [MFMailComposeError](/documentation/messageui/mfmailcomposeerror)

#### Errors

- [static var errorDomain: String](/documentation/messageui/mfmailcomposeerror/errordomain)
- [static var saveFailed: MFMailComposeError.Code](/documentation/messageui/mfmailcomposeerror/savefailed)
- [static var sendFailed: MFMailComposeError.Code](/documentation/messageui/mfmailcomposeerror/sendfailed)
- [MFMailComposeError.Code](/documentation/messageui/mfmailcomposeerror/code)

##### Constants

- [case saveFailed](/documentation/messageui/mfmailcomposeerror/code/savefailed)
- [case sendFailed](/documentation/messageui/mfmailcomposeerror/code/sendfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/messageui/mfmailcomposeerror/code/init(rawvalue:))

##### Default Implementations

- [Equatable Implementations](/documentation/messageui/mfmailcomposeerror/code/equatable-implementations)

###### Operators

- [static func != (Self, Self) -> Bool](/documentation/messageui/mfmailcomposeerror/code/!=(_:_:))
- [RawRepresentable Implementations](/documentation/messageui/mfmailcomposeerror/code/rawrepresentable-implementations)

###### Instance Properties

- [var hashValue: Int](/documentation/messageui/mfmailcomposeerror/code/hashvalue)

###### Instance Methods

- [func hash(into: inout Hasher)](/documentation/messageui/mfmailcomposeerror/code/hash(into:))

#### Error Configuration

- [static var errorDomain: String](/documentation/messageui/mfmailcomposeerror/errordomain)
- [var localizedDescription: String](/documentation/messageui/mfmailcomposeerror/localizeddescription)

#### Default Implementations

- [CustomNSError Implementations](/documentation/messageui/mfmailcomposeerror/customnserror-implementations)

##### Type Properties

- [static var errorDomain: String](/documentation/messageui/mfmailcomposeerror/errordomain-5sxor)
- [Equatable Implementations](/documentation/messageui/mfmailcomposeerror/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/messageui/mfmailcomposeerror/!=(_:_:))
- [Error Implementations](/documentation/messageui/mfmailcomposeerror/error-implementations)

##### Instance Properties

- [var localizedDescription: String](/documentation/messageui/mfmailcomposeerror/localizeddescription)
- [let MFMailComposeErrorDomain: String](/documentation/messageui/mfmailcomposeerrordomain)
- [MFMailComposeError.Code](/documentation/messageui/mfmailcomposeerror/code)

#### Constants

- [case saveFailed](/documentation/messageui/mfmailcomposeerror/code/savefailed)
- [case sendFailed](/documentation/messageui/mfmailcomposeerror/code/sendfailed)

#### Initializers

- [init?(rawValue: Int)](/documentation/messageui/mfmailcomposeerror/code/init(rawvalue:))

#### Default Implementations

- [Equatable Implementations](/documentation/messageui/mfmailcomposeerror/code/equatable-implementations)

##### Operators

- [static func != (Self, Self) -> Bool](/documentation/messageui/mfmailcomposeerror/code/!=(_:_:))
- [RawRepresentable Implementations](/documentation/messageui/mfmailcomposeerror/code/rawrepresentable-implementations)

##### Instance Properties

- [var hashValue: Int](/documentation/messageui/mfmailcomposeerror/code/hashvalue)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/messageui/mfmailcomposeerror/code/hash(into:))

### Instance Methods

- [func insertCollaborationItemProvider(NSItemProvider, completionHandler: (Bool) -> Void)](/documentation/messageui/mfmailcomposeviewcontroller/insertcollaborationitemprovider(_:completionhandler:))

## Message composition interface

- [MFMessageComposeViewController](/documentation/messageui/mfmessagecomposeviewcontroller)

### Responding to the view controller dismissal

- [var messageComposeDelegate: (any MFMessageComposeViewControllerDelegate)?](/documentation/messageui/mfmessagecomposeviewcontroller/messagecomposedelegate)
- [MFMessageComposeViewControllerDelegate](/documentation/messageui/mfmessagecomposeviewcontrollerdelegate)

#### Responding to the Message Completion

- [func messageComposeViewController(MFMessageComposeViewController, didFinishWith: MessageComposeResult)](/documentation/messageui/mfmessagecomposeviewcontrollerdelegate/messagecomposeviewcontroller(_:didfinishwith:))
- [MessageComposeResult](/documentation/messageui/messagecomposeresult)

##### Constants

- [case cancelled](/documentation/messageui/messagecomposeresult/cancelled)
- [case sent](/documentation/messageui/messagecomposeresult/sent)
- [case failed](/documentation/messageui/messagecomposeresult/failed)

##### Initializers

- [init?(rawValue: Int)](/documentation/messageui/messagecomposeresult/init(rawvalue:))

##### Default Implementations

- [Equatable Implementations](/documentation/messageui/messagecomposeresult/equatable-implementations)

###### Operators

- [static func != (Self, Self) -> Bool](/documentation/messageui/messagecomposeresult/!=(_:_:))
- [RawRepresentable Implementations](/documentation/messageui/messagecomposeresult/rawrepresentable-implementations)

###### Instance Properties

- [var hashValue: Int](/documentation/messageui/messagecomposeresult/hashvalue)

###### Instance Methods

- [func hash(into: inout Hasher)](/documentation/messageui/messagecomposeresult/hash(into:))

### Determining if message composition is available

- [class func canSendText() -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/cansendtext())
- [class func canSendAttachments() -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/cansendattachments())
- [class func canSendSubject() -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/cansendsubject())
- [class func isSupportedAttachmentUTI(String) -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/issupportedattachmentuti(_:))

### Setting the initial message information

- [var recipients: [String]?](/documentation/messageui/mfmessagecomposeviewcontroller/recipients)
- [var subject: String?](/documentation/messageui/mfmessagecomposeviewcontroller/subject)
- [var body: String?](/documentation/messageui/mfmessagecomposeviewcontroller/body)
- [var message: MSMessage?](/documentation/messageui/mfmessagecomposeviewcontroller/message)

### Managing attachments

- [func disableUserAttachments()](/documentation/messageui/mfmessagecomposeviewcontroller/disableuserattachments())
- [var attachments: [[AnyHashable : Any]]?](/documentation/messageui/mfmessagecomposeviewcontroller/attachments)
- [func addAttachmentURL(URL, withAlternateFilename: String?) -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/addattachmenturl(_:withalternatefilename:))
- [func addAttachmentData(Data, typeIdentifier: String, filename: String) -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/addattachmentdata(_:typeidentifier:filename:))
- [let MFMessageComposeViewControllerAttachmentURL: String](/documentation/messageui/mfmessagecomposeviewcontrollerattachmenturl)
- [let MFMessageComposeViewControllerAttachmentAlternateFilename: String](/documentation/messageui/mfmessagecomposeviewcontrollerattachmentalternatefilename)
- [func insertCollaborationItemProvider(NSItemProvider) -> Bool](/documentation/messageui/mfmessagecomposeviewcontroller/insertcollaborationitemprovider(_:))

### Handling notifications

- [static let MFMessageComposeViewControllerTextMessageAvailabilityDidChange: NSNotification.Name](/documentation/foundation/nsnotification/name-swift.struct/mfmessagecomposeviewcontrollertextmessageavailabilitydidchange)
- [let MFMessageComposeViewControllerTextMessageAvailabilityKey: String](/documentation/messageui/mfmessagecomposeviewcontrollertextmessageavailabilitykey)

### Configuring device validation

- [func setUPIVerificationCodeSendCompletion((Bool) -> Void)](/documentation/messageui/mfmessagecomposeviewcontroller/setupiverificationcodesendcompletion(_:))

## Enumerations

- [MFMailComposeControllerDeferredAction](/documentation/messageui/mfmailcomposecontrollerdeferredaction)

### Enumeration Cases

- [case addMissingRecipients](/documentation/messageui/mfmailcomposecontrollerdeferredaction/addmissingrecipients)
- [case adjustInsertionPoint](/documentation/messageui/mfmailcomposecontrollerdeferredaction/adjustinsertionpoint)
- [case none](/documentation/messageui/mfmailcomposecontrollerdeferredaction/none)

### Initializers

- [init?(rawValue: Int)](/documentation/messageui/mfmailcomposecontrollerdeferredaction/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
