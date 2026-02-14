# MailKit Documentation

Source: https://sosumi.ai/documentation/mailkit

---
title: MailKit
source: https://developer.apple.com/documentation/mailkit
timestamp: 2026-02-13T18:58:59.211Z
---

## Essentials

- [MEExtension](/documentation/mailkit/meextension)

### Blocking Content

- [func handlerForContentBlocker() -> any MEContentBlocker](/documentation/mailkit/meextension/handlerforcontentblocker())

### Performing Actions on Messages

- [func handlerForMessageActions() -> any MEMessageActionHandler](/documentation/mailkit/meextension/handlerformessageactions())

### Enhancing the Compose Window

- [func handler(for: MEComposeSession) -> any MEComposeSessionHandler](/documentation/mailkit/meextension/handler(for:))

### Encrypting and Signing Messages

- [func handlerForMessageSecurity() -> any MEMessageSecurityHandler](/documentation/mailkit/meextension/handlerformessagesecurity())
- [Build Mail App Extensions](/documentation/mailkit/build-mail-app-extensions)

## Content Blockers

- [MEContentBlocker](/documentation/mailkit/mecontentblocker)

### Defining Rules to Block Content

- [func contentRulesJSON() -> Data](/documentation/mailkit/mecontentblocker/contentrulesjson())

## Message Actions

- [MEMessageActionHandler](/documentation/mailkit/memessageactionhandler)

### Performing Actions on Messages

- [func decideAction(for: MEMessage, completionHandler: (MEMessageActionDecision?) -> Void)](/documentation/mailkit/memessageactionhandler/decideaction(for:completionhandler:))
- [MEMessageAction](/documentation/mailkit/memessageaction)

#### Changing the Read Status

- [class var markAsRead: MEMessageAction](/documentation/mailkit/memessageaction/markasread)
- [class var markAsUnread: MEMessageAction](/documentation/mailkit/memessageaction/markasunread)

#### Transferring Messages

- [class var moveToArchive: MEMessageAction](/documentation/mailkit/memessageaction/movetoarchive)
- [class var moveToJunk: MEMessageAction](/documentation/mailkit/memessageaction/movetojunk)
- [class var moveToTrash: MEMessageAction](/documentation/mailkit/memessageaction/movetotrash)

#### Type Methods

- [class func flag(MEMessageAction.Flag) -> Self](/documentation/mailkit/memessageaction/flag(_:))
- [class func setBackgroundColor(MEMessageAction.MessageColor) -> Self](/documentation/mailkit/memessageaction/setbackgroundcolor(_:))

#### Enumerations

- [MEMessageAction.Flag](/documentation/mailkit/memessageaction/flag)

##### Enumeration Cases

- [case blue](/documentation/mailkit/memessageaction/flag/blue)
- [case defaultColor](/documentation/mailkit/memessageaction/flag/defaultcolor)
- [case gray](/documentation/mailkit/memessageaction/flag/gray)
- [case green](/documentation/mailkit/memessageaction/flag/green)
- [case none](/documentation/mailkit/memessageaction/flag/none)
- [case orange](/documentation/mailkit/memessageaction/flag/orange)
- [case purple](/documentation/mailkit/memessageaction/flag/purple)
- [case red](/documentation/mailkit/memessageaction/flag/red)
- [case yellow](/documentation/mailkit/memessageaction/flag/yellow)

##### Initializers

- [init?(rawValue: Int)](/documentation/mailkit/memessageaction/flag/init(rawvalue:))
- [MEMessageAction.MessageColor](/documentation/mailkit/memessageaction/messagecolor)

##### Specifying a Message Color

- [case green](/documentation/mailkit/memessageaction/messagecolor/green)
- [case yellow](/documentation/mailkit/memessageaction/messagecolor/yellow)
- [case orange](/documentation/mailkit/memessageaction/messagecolor/orange)
- [case red](/documentation/mailkit/memessageaction/messagecolor/red)
- [case purple](/documentation/mailkit/memessageaction/messagecolor/purple)
- [case blue](/documentation/mailkit/memessageaction/messagecolor/blue)
- [case gray](/documentation/mailkit/memessageaction/messagecolor/gray)
- [case none](/documentation/mailkit/memessageaction/messagecolor/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/mailkit/memessageaction/messagecolor/init(rawvalue:))
- [MEMessageActionDecision](/documentation/mailkit/memessageactiondecision)

#### Determining Actions to Perform on Messages

- [class var invokeAgainWithBody: MEMessageActionDecision](/documentation/mailkit/memessageactiondecision/invokeagainwithbody)

#### Type Methods

- [class func action(MEMessageAction) -> Self](/documentation/mailkit/memessageactiondecision/action(_:))
- [class func actions([MEMessageAction]) -> Self](/documentation/mailkit/memessageactiondecision/actions(_:))
- [MEMessageAction.MessageColor](/documentation/mailkit/memessageaction/messagecolor)

#### Specifying a Message Color

- [case green](/documentation/mailkit/memessageaction/messagecolor/green)
- [case yellow](/documentation/mailkit/memessageaction/messagecolor/yellow)
- [case orange](/documentation/mailkit/memessageaction/messagecolor/orange)
- [case red](/documentation/mailkit/memessageaction/messagecolor/red)
- [case purple](/documentation/mailkit/memessageaction/messagecolor/purple)
- [case blue](/documentation/mailkit/memessageaction/messagecolor/blue)
- [case gray](/documentation/mailkit/memessageaction/messagecolor/gray)
- [case none](/documentation/mailkit/memessageaction/messagecolor/none)

#### Initializers

- [init?(rawValue: Int)](/documentation/mailkit/memessageaction/messagecolor/init(rawvalue:))

### Instance Properties

- [var requiredHeaders: [String]](/documentation/mailkit/memessageactionhandler/requiredheaders)

## Compose Window Enhancements

- [MEComposeSessionHandler](/documentation/mailkit/mecomposesessionhandler)

### Handling Compose Sessions

- [MEComposeSession](/documentation/mailkit/mecomposesession)

#### Managing Compose Sessions

- [var sessionID: UUID](/documentation/mailkit/mecomposesession/sessionid)
- [func reload()](/documentation/mailkit/mecomposesession/reload())

#### Accessing Message Properties

- [var mailMessage: MEMessage](/documentation/mailkit/mecomposesession/mailmessage)

#### Instance Properties

- [var composeContext: MEComposeContext](/documentation/mailkit/mecomposesession/composecontext)
- [func mailComposeSessionDidBegin(MEComposeSession)](/documentation/mailkit/mecomposesessionhandler/mailcomposesessiondidbegin(_:))
- [func mailComposeSessionDidEnd(MEComposeSession)](/documentation/mailkit/mecomposesessionhandler/mailcomposesessiondidend(_:))
- [MEComposeSessionError](/documentation/mailkit/mecomposesessionerror)

#### Indicating Erroneous States

- [static var invalidBody: MEComposeSessionError.Code](/documentation/mailkit/mecomposesessionerror/invalidbody)
- [static var invalidHeaders: MEComposeSessionError.Code](/documentation/mailkit/mecomposesessionerror/invalidheaders)
- [static var invalidRecipients: MEComposeSessionError.Code](/documentation/mailkit/mecomposesessionerror/invalidrecipients)
- [let MEComposeSessionErrorDomain: String](/documentation/mailkit/mecomposesessionerrordomain)

#### Type Properties

- [static var errorDomain: String](/documentation/mailkit/mecomposesessionerror/errordomain)

### Annotating Email Address Tokens

- [func annotateAddressesForSession(MEComposeSession, completion: ([MEEmailAddress : MEAddressAnnotation]) -> Void)](/documentation/mailkit/mecomposesessionhandler/annotateaddressesforsession(_:completion:))
- [MEAddressAnnotation](/documentation/mailkit/meaddressannotation)

#### Specifying Email Address Validity

- [class func success(withLocalizedDescription: String) -> MEAddressAnnotation](/documentation/mailkit/meaddressannotation/success(withlocalizeddescription:))
- [class func warning(withLocalizedDescription: String) -> MEAddressAnnotation](/documentation/mailkit/meaddressannotation/warning(withlocalizeddescription:))
- [class func error(withLocalizedDescription: String) -> MEAddressAnnotation](/documentation/mailkit/meaddressannotation/error(withlocalizeddescription:))

### Extending the Compose Window Interface

- [func viewController(for: MEComposeSession) -> MEExtensionViewController](/documentation/mailkit/mecomposesessionhandler/viewcontroller(for:))

### Adding Custom Headers

- [func additionalHeaders(for: MEComposeSession) -> [String : [String]]](/documentation/mailkit/mecomposesessionhandler/additionalheaders(for:))

### Approving Message Delivery

- [func allowMessageSendForSession(MEComposeSession, completion: ((any Error)?) -> Void)](/documentation/mailkit/mecomposesessionhandler/allowmessagesendforsession(_:completion:))

## Message Encryption, Decryption, and Digital Signatures

- [MEMessageSecurityHandler](/documentation/mailkit/memessagesecurityhandler)

### Encrypting and Signing Messages

- [MEMessageEncoder](/documentation/mailkit/memessageencoder)

#### Instance Methods

- [func encode(MEMessage, composeContext: MEComposeContext, completionHandler: (MEMessageEncodingResult) -> Void)](/documentation/mailkit/memessageencoder/encode(_:composecontext:completionhandler:))
- [func getEncodingStatus(for: MEMessage, composeContext: MEComposeContext, completionHandler: (MEOutgoingMessageEncodingStatus) -> Void)](/documentation/mailkit/memessageencoder/getencodingstatus(for:composecontext:completionhandler:))
- [MEEncodedOutgoingMessage](/documentation/mailkit/meencodedoutgoingmessage)

#### Encoding Outgoing Messages

- [init(rawData: Data, isSigned: Bool, isEncrypted: Bool)](/documentation/mailkit/meencodedoutgoingmessage/init(rawdata:issigned:isencrypted:))
- [var isEncrypted: Bool](/documentation/mailkit/meencodedoutgoingmessage/isencrypted)
- [var isSigned: Bool](/documentation/mailkit/meencodedoutgoingmessage/issigned)
- [var rawData: Data](/documentation/mailkit/meencodedoutgoingmessage/rawdata)
- [MEOutgoingMessageEncodingStatus](/documentation/mailkit/meoutgoingmessageencodingstatus)

#### Providing Encoding Status

- [init(canSign: Bool, canEncrypt: Bool, securityError: (any Error)?, addressesFailingEncryption: [MEEmailAddress])](/documentation/mailkit/meoutgoingmessageencodingstatus/init(cansign:canencrypt:securityerror:addressesfailingencryption:))
- [var canSign: Bool](/documentation/mailkit/meoutgoingmessageencodingstatus/cansign)
- [var canEncrypt: Bool](/documentation/mailkit/meoutgoingmessageencodingstatus/canencrypt)
- [var securityError: (any Error)?](/documentation/mailkit/meoutgoingmessageencodingstatus/securityerror)
- [var addressesFailingEncryption: [MEEmailAddress]](/documentation/mailkit/meoutgoingmessageencodingstatus/addressesfailingencryption)
- [MEMessageEncodingResult](/documentation/mailkit/memessageencodingresult)

#### Providing an Encoding Result

- [init(encodedMessage: MEEncodedOutgoingMessage?, signingError: (any Error)?, encryptionError: (any Error)?)](/documentation/mailkit/memessageencodingresult/init(encodedmessage:signingerror:encryptionerror:))
- [var encodedMessage: MEEncodedOutgoingMessage?](/documentation/mailkit/memessageencodingresult/encodedmessage)
- [var encryptionError: (any Error)?](/documentation/mailkit/memessageencodingresult/encryptionerror)
- [var signingError: (any Error)?](/documentation/mailkit/memessageencodingresult/signingerror)

### Decrypting Messages and Verifying Signatures

- [MEMessageDecoder](/documentation/mailkit/memessagedecoder)

#### Decrypting Messages and Verifying Signatures

- [func decodedMessage(forMessageData: Data) -> MEDecodedMessage?](/documentation/mailkit/memessagedecoder/decodedmessage(formessagedata:))
- [MEDecodedMessage](/documentation/mailkit/medecodedmessage)

#### Decoding Messages

- [var rawData: Data?](/documentation/mailkit/medecodedmessage/rawdata)
- [var securityInformation: MEMessageSecurityInformation](/documentation/mailkit/medecodedmessage/securityinformation)

#### Initializers

- [init(data: Data?, securityInformation: MEMessageSecurityInformation, context: Data?)](/documentation/mailkit/medecodedmessage/init(data:securityinformation:context:))
- [init(data: Data?, securityInformation: MEMessageSecurityInformation, context: Data?, banner: MEDecodedMessageBanner?)](/documentation/mailkit/medecodedmessage/init(data:securityinformation:context:banner:))

#### Instance Properties

- [var banner: MEDecodedMessageBanner?](/documentation/mailkit/medecodedmessage/banner)
- [var context: Data?](/documentation/mailkit/medecodedmessage/context)
- [MEMessageSigner](/documentation/mailkit/memessagesigner)

#### Describing Message Signers

- [init(emailAddresses: [MEEmailAddress], signatureLabel: String, context: Data?)](/documentation/mailkit/memessagesigner/init(emailaddresses:signaturelabel:context:))
- [var emailAddresses: [MEEmailAddress]](/documentation/mailkit/memessagesigner/emailaddresses)
- [var label: String](/documentation/mailkit/memessagesigner/label)
- [var context: Data](/documentation/mailkit/memessagesigner/context)
- [MEMessageSecurityInformation](/documentation/mailkit/memessagesecurityinformation)

#### Describing Message Security Attributes

- [init(signers: [MEMessageSigner], isEncrypted: Bool, signingError: (any Error)?, encryptionError: (any Error)?)](/documentation/mailkit/memessagesecurityinformation/init(signers:isencrypted:signingerror:encryptionerror:))
- [var isEncrypted: Bool](/documentation/mailkit/memessagesecurityinformation/isencrypted)
- [var encryptionError: (any Error)?](/documentation/mailkit/memessagesecurityinformation/encryptionerror)
- [var signers: [MEMessageSigner]](/documentation/mailkit/memessagesecurityinformation/signers)
- [var signingError: (any Error)?](/documentation/mailkit/memessagesecurityinformation/signingerror)

#### Initializers

- [init(signers: [MEMessageSigner], isEncrypted: Bool, signingError: (any Error)?, encryptionError: (any Error)?, shouldBlockRemoteContent: Bool, localizedRemoteContentBlockingReason: String?)](/documentation/mailkit/memessagesecurityinformation/init(signers:isencrypted:signingerror:encryptionerror:shouldblockremotecontent:localizedremotecontentblockingreason:))

#### Instance Properties

- [var localizedRemoteContentBlockingReason: String?](/documentation/mailkit/memessagesecurityinformation/localizedremotecontentblockingreason)
- [var shouldBlockRemoteContent: Bool](/documentation/mailkit/memessagesecurityinformation/shouldblockremotecontent)

### Displaying Signature Details

- [func extensionViewController(signers: [MEMessageSigner]) -> MEExtensionViewController?](/documentation/mailkit/memessagesecurityhandler/extensionviewcontroller(signers:))

### Instance Methods

- [func extensionViewController(messageContext: Data) -> MEExtensionViewController?](/documentation/mailkit/memessagesecurityhandler/extensionviewcontroller(messagecontext:))
- [func primaryActionClicked(forMessageContext: Data, completionHandler: (MEExtensionViewController?) -> Void)](/documentation/mailkit/memessagesecurityhandler/primaryactionclicked(formessagecontext:completionhandler:))

## Message Properties

- [MEMessage](/documentation/mailkit/memessage)

### Accessing the Sender and Recipients

- [var fromAddress: MEEmailAddress](/documentation/mailkit/memessage/fromaddress)
- [var toAddresses: [MEEmailAddress]](/documentation/mailkit/memessage/toaddresses)
- [var ccAddresses: [MEEmailAddress]](/documentation/mailkit/memessage/ccaddresses)
- [var bccAddresses: [MEEmailAddress]](/documentation/mailkit/memessage/bccaddresses)
- [var replyToAddresses: [MEEmailAddress]](/documentation/mailkit/memessage/replytoaddresses)
- [var allRecipientAddresses: [MEEmailAddress]](/documentation/mailkit/memessage/allrecipientaddresses)

### Accessing the Message Subject

- [var subject: String](/documentation/mailkit/memessage/subject)

### Accessing Message Content

- [var headers: [String : [String]]?](/documentation/mailkit/memessage/headers)
- [var rawData: Data?](/documentation/mailkit/memessage/rawdata)

### Accessing Message State

- [var state: MEMessageState](/documentation/mailkit/memessage/state)

### Instance Properties

- [var encryptionState: MEMessageEncryptionState](/documentation/mailkit/memessage/encryptionstate)
- [MEMessageState](/documentation/mailkit/memessagestate)

### Determining Message State

- [case draft](/documentation/mailkit/memessagestate/draft)
- [case received](/documentation/mailkit/memessagestate/received)
- [case sending](/documentation/mailkit/memessagestate/sending)

### Initializers

- [init?(rawValue: Int)](/documentation/mailkit/memessagestate/init(rawvalue:))

## Custom View Controllers

- [MEExtensionViewController](/documentation/mailkit/meextensionviewcontroller)

## Structures

- [MEMessageSecurityError](/documentation/mailkit/memessagesecurityerror)

### Type Properties

- [static var decodingError: MEMessageSecurityError.Code](/documentation/mailkit/memessagesecurityerror/decodingerror)
- [static var encodingError: MEMessageSecurityError.Code](/documentation/mailkit/memessagesecurityerror/encodingerror)
- [static var errorDomain: String](/documentation/mailkit/memessagesecurityerror/errordomain)

### Enumerations

- [MEMessageSecurityError.Code](/documentation/mailkit/memessagesecurityerror/code)

#### Enumeration Cases

- [case decodingError](/documentation/mailkit/memessagesecurityerror/code/decodingerror)
- [case encodingError](/documentation/mailkit/memessagesecurityerror/code/encodingerror)

#### Initializers

- [init?(rawValue: Int)](/documentation/mailkit/memessagesecurityerror/code/init(rawvalue:))

## Classes

- [MEComposeContext](/documentation/mailkit/mecomposecontext)

### Instance Properties

- [var action: MEComposeUserAction](/documentation/mailkit/mecomposecontext/action)
- [var contextID: UUID](/documentation/mailkit/mecomposecontext/contextid)
- [var isEncrypted: Bool](/documentation/mailkit/mecomposecontext/isencrypted)
- [var isSigned: Bool](/documentation/mailkit/mecomposecontext/issigned)
- [var originalMessage: MEMessage?](/documentation/mailkit/mecomposecontext/originalmessage)
- [var shouldEncrypt: Bool](/documentation/mailkit/mecomposecontext/shouldencrypt)
- [var shouldSign: Bool](/documentation/mailkit/mecomposecontext/shouldsign)
- [MEDecodedMessageBanner](/documentation/mailkit/medecodedmessagebanner)

### Initializers

- [init(title: String, primaryActionTitle: String, dismissable: Bool)](/documentation/mailkit/medecodedmessagebanner/init(title:primaryactiontitle:dismissable:))

### Instance Properties

- [var isDismissable: Bool](/documentation/mailkit/medecodedmessagebanner/isdismissable)
- [var primaryActionTitle: String](/documentation/mailkit/medecodedmessagebanner/primaryactiontitle)
- [var title: String](/documentation/mailkit/medecodedmessagebanner/title)
- [MEEmailAddress](/documentation/mailkit/meemailaddress)

### Initializers

- [init(rawString: String)](/documentation/mailkit/meemailaddress/init(rawstring:))

### Instance Properties

- [var addressString: String?](/documentation/mailkit/meemailaddress/addressstring)
- [var rawString: String](/documentation/mailkit/meemailaddress/rawstring)
- [MEExtensionManager](/documentation/mailkit/meextensionmanager)

### Type Methods

- [class func reloadContentBlocker(withIdentifier: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/mailkit/meextensionmanager/reloadcontentblocker(withidentifier:completionhandler:))
- [class func reloadVisibleMessages(completionHandler: (((any Error)?) -> Void)?)](/documentation/mailkit/meextensionmanager/reloadvisiblemessages(completionhandler:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
