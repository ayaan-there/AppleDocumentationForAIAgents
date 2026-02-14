# Messages Documentation

Source: https://sosumi.ai/documentation/messages

---
title: Messages
source: https://developer.apple.com/documentation/messages
timestamp: 2026-02-13T18:59:35.013Z
---

## Default messaging app

- [Preparing your app to be the default messaging app](/documentation/messages/preparing-your-app-to-be-the-default-messaging-app)

## Custom sticker packs

- [Adding Sticker packs and iMessage apps to the system Stickers app, Messages camera, and FaceTime](/documentation/messages/adding-sticker-packs-and-imessage-apps-to-the-system-stickers-app-messages-camera-and-facetime)
- [Adding your sticker packs to Messages](/documentation/messages/adding-your-sticker-packs-to-messages)
- [MSStickerBrowserViewController](/documentation/messages/msstickerbrowserviewcontroller)

### Working with Stickers

- [init(stickerSize: MSStickerSize)](/documentation/messages/msstickerbrowserviewcontroller/init(stickersize:))
- [var stickerBrowserView: MSStickerBrowserView](/documentation/messages/msstickerbrowserviewcontroller/stickerbrowserview)
- [var stickerSize: MSStickerSize](/documentation/messages/msstickerbrowserviewcontroller/stickersize)
- [MSStickerBrowserView](/documentation/messages/msstickerbrowserview)

### Creating Sticker Browser Views

- [init(frame: CGRect)](/documentation/messages/msstickerbrowserview/init(frame:))
- [init(frame: CGRect, stickerSize: MSStickerSize)](/documentation/messages/msstickerbrowserview/init(frame:stickersize:))

### Managing the Sticker Collection Contents

- [var dataSource: (any MSStickerBrowserViewDataSource)?](/documentation/messages/msstickerbrowserview/datasource)
- [MSStickerBrowserViewDataSource](/documentation/messages/msstickerbrowserviewdatasource)

#### Providing Stickers

- [func numberOfStickers(in: MSStickerBrowserView) -> Int](/documentation/messages/msstickerbrowserviewdatasource/numberofstickers(in:))
- [func stickerBrowserView(MSStickerBrowserView, stickerAt: Int) -> MSSticker](/documentation/messages/msstickerbrowserviewdatasource/stickerbrowserview(_:stickerat:))
- [func reloadData()](/documentation/messages/msstickerbrowserview/reloaddata())

### Managing the Browser’s Appearance

- [var contentInset: UIEdgeInsets](/documentation/messages/msstickerbrowserview/contentinset)
- [var contentOffset: CGPoint](/documentation/messages/msstickerbrowserview/contentoffset)
- [func setContentOffset(CGPoint, animated: Bool)](/documentation/messages/msstickerbrowserview/setcontentoffset(_:animated:))
- [var stickerSize: MSStickerSize](/documentation/messages/msstickerbrowserview/stickersize)

### Constants

- [MSStickerSize](/documentation/messages/msstickersize)

#### Constants

- [case small](/documentation/messages/msstickersize/small)
- [case regular](/documentation/messages/msstickersize/regular)
- [case large](/documentation/messages/msstickersize/large)

#### Initializers

- [init?(rawValue: Int)](/documentation/messages/msstickersize/init(rawvalue:))
- [MSStickerView](/documentation/messages/msstickerview)

### Working with Sticker Views

- [init(frame: CGRect, sticker: MSSticker?)](/documentation/messages/msstickerview/init(frame:sticker:))
- [var sticker: MSSticker?](/documentation/messages/msstickerview/sticker)

### Controlling Sticker Animation

- [var animationDuration: TimeInterval](/documentation/messages/msstickerview/animationduration)
- [func isAnimating() -> Bool](/documentation/messages/msstickerview/isanimating())
- [func startAnimating()](/documentation/messages/msstickerview/startanimating())
- [func stopAnimating()](/documentation/messages/msstickerview/stopanimating())
- [MSStickerSize](/documentation/messages/msstickersize)

### Constants

- [case small](/documentation/messages/msstickersize/small)
- [case regular](/documentation/messages/msstickersize/regular)
- [case large](/documentation/messages/msstickersize/large)

### Initializers

- [init?(rawValue: Int)](/documentation/messages/msstickersize/init(rawvalue:))

## Custom iMessage app interface

- [IceCreamBuilder: Building an iMessage Extension](/documentation/messages/icecreambuilder-building-an-imessage-extension)
- [Creating a Sticker App with a Custom Layout](/documentation/messages/creating-a-sticker-app-with-a-custom-layout)
- [MSMessagesAppViewController](/documentation/messages/msmessagesappviewcontroller)

### Managing the Extension’s State

- [var activeConversation: MSConversation?](/documentation/messages/msmessagesappviewcontroller/activeconversation)
- [func dismiss()](/documentation/messages/msmessagesappviewcontroller/dismiss())
- [func willBecomeActive(with: MSConversation)](/documentation/messages/msmessagesappviewcontroller/willbecomeactive(with:))
- [func didBecomeActive(with: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didbecomeactive(with:))
- [func willResignActive(with: MSConversation)](/documentation/messages/msmessagesappviewcontroller/willresignactive(with:))
- [func didResignActive(with: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didresignactive(with:))

### Tracking Messages

- [func willSelect(MSMessage, conversation: MSConversation)](/documentation/messages/msmessagesappviewcontroller/willselect(_:conversation:))
- [func didSelect(MSMessage, conversation: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didselect(_:conversation:))
- [func didReceive(MSMessage, conversation: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didreceive(_:conversation:))
- [func didStartSending(MSMessage, conversation: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didstartsending(_:conversation:))
- [func didCancelSending(MSMessage, conversation: MSConversation)](/documentation/messages/msmessagesappviewcontroller/didcancelsending(_:conversation:))

### Working with Presentation Styles and Contexts

- [var presentationStyle: MSMessagesAppPresentationStyle](/documentation/messages/msmessagesappviewcontroller/presentationstyle)
- [func requestPresentationStyle(MSMessagesAppPresentationStyle)](/documentation/messages/msmessagesappviewcontroller/requestpresentationstyle(_:))
- [func willTransition(to: MSMessagesAppPresentationStyle)](/documentation/messages/msmessagesappviewcontroller/willtransition(to:))
- [func didTransition(to: MSMessagesAppPresentationStyle)](/documentation/messages/msmessagesappviewcontroller/didtransition(to:))
- [MSMessagesAppPresentationStyle](/documentation/messages/msmessagesapppresentationstyle)

#### Presentation Styles

- [case compact](/documentation/messages/msmessagesapppresentationstyle/compact)
- [case expanded](/documentation/messages/msmessagesapppresentationstyle/expanded)
- [case transcript](/documentation/messages/msmessagesapppresentationstyle/transcript)

#### Initializers

- [init?(rawValue: UInt)](/documentation/messages/msmessagesapppresentationstyle/init(rawvalue:))
- [var presentationContext: MSMessagesAppPresentationContext](/documentation/messages/msmessagesappviewcontroller/presentationcontext)
- [MSMessagesAppPresentationContext](/documentation/messages/msmessagesapppresentationcontext)

#### Presentation Contexts

- [case media](/documentation/messages/msmessagesapppresentationcontext/media)
- [case messages](/documentation/messages/msmessagesapppresentationcontext/messages)

#### Initializers

- [init?(rawValue: UInt)](/documentation/messages/msmessagesapppresentationcontext/init(rawvalue:))
- [MSMessagesAppTranscriptPresentation](/documentation/messages/msmessagesapptranscriptpresentation)

### Providing the Content’s Size

- [func contentSizeThatFits(CGSize) -> CGSize](/documentation/messages/msmessagesapptranscriptpresentation/contentsizethatfits(_:))

### Instance Properties

- [var messageCornerRadius: CGFloat](/documentation/messages/msmessagesapptranscriptpresentation/messagecornerradius)
- [var messageTintColor: UIColor?](/documentation/messages/msmessagesapptranscriptpresentation/messagetintcolor)

### Instance Methods

- [func invalidateMessageTintColor()](/documentation/messages/msmessagesapptranscriptpresentation/invalidatemessagetintcolor())
- [MSMessagesAppPresentationStyle](/documentation/messages/msmessagesapppresentationstyle)

### Presentation Styles

- [case compact](/documentation/messages/msmessagesapppresentationstyle/compact)
- [case expanded](/documentation/messages/msmessagesapppresentationstyle/expanded)
- [case transcript](/documentation/messages/msmessagesapppresentationstyle/transcript)

### Initializers

- [init?(rawValue: UInt)](/documentation/messages/msmessagesapppresentationstyle/init(rawvalue:))

## Message content

- [MSConversation](/documentation/messages/msconversation)

### Accessing the Selected Message

- [var selectedMessage: MSMessage?](/documentation/messages/msconversation/selectedmessage)

### Accessing Participants

- [var localParticipantIdentifier: UUID](/documentation/messages/msconversation/localparticipantidentifier)
- [var remoteParticipantIdentifiers: [UUID]](/documentation/messages/msconversation/remoteparticipantidentifiers)

### Inserting Content into the Input Field

- [func insertAttachment(URL, withAlternateFilename: String?, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/insertattachment(_:withalternatefilename:completionhandler:))
- [func insert(MSMessage, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/insert(_:completionhandler:)-3g248)
- [func insert(MSSticker, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/insert(_:completionhandler:)-7fpdd)
- [func insertText(String, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/inserttext(_:completionhandler:))

### Directly Sending a Message

- [func sendAttachment(URL, withAlternateFilename: String?, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/sendattachment(_:withalternatefilename:completionhandler:))
- [func send(MSMessage, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/send(_:completionhandler:)-9krz)
- [func send(MSSticker, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/send(_:completionhandler:)-4kje0)
- [func sendText(String, completionHandler: (((any Error)?) -> Void)?)](/documentation/messages/msconversation/sendtext(_:completionhandler:))
- [MSSticker](/documentation/messages/mssticker)

### Creating Stickers

- [init(contentsOfFileURL: URL, localizedDescription: String) throws](/documentation/messages/mssticker/init(contentsoffileurl:localizeddescription:))

### Reading Sticker Data

- [var imageFileURL: URL](/documentation/messages/mssticker/imagefileurl)
- [var localizedDescription: String](/documentation/messages/mssticker/localizeddescription)

## Interactive messages

- [MSMessage](/documentation/messages/msmessage)

### Creating Messages

- [init()](/documentation/messages/msmessage/init())
- [init(session: MSSession)](/documentation/messages/msmessage/init(session:))

### Message Properties

- [var accessibilityLabel: String?](/documentation/messages/msmessage/accessibilitylabel)
- [var error: (any Error)?](/documentation/messages/msmessage/error)
- [var isPending: Bool](/documentation/messages/msmessage/ispending)
- [var layout: MSMessageLayout?](/documentation/messages/msmessage/layout)
- [var senderParticipantIdentifier: UUID](/documentation/messages/msmessage/senderparticipantidentifier)
- [var session: MSSession?](/documentation/messages/msmessage/session)
- [var shouldExpire: Bool](/documentation/messages/msmessage/shouldexpire)
- [var summaryText: String?](/documentation/messages/msmessage/summarytext)
- [var url: URL?](/documentation/messages/msmessage/url)
- [MSSession](/documentation/messages/mssession)
- [MSMessageLayout](/documentation/messages/msmessagelayout)
- [MSMessageTemplateLayout](/documentation/messages/msmessagetemplatelayout)

### Assigning Visual Elements

- [var image: UIImage?](/documentation/messages/msmessagetemplatelayout/image)
- [var mediaFileURL: URL?](/documentation/messages/msmessagetemplatelayout/mediafileurl)
- [var imageTitle: String?](/documentation/messages/msmessagetemplatelayout/imagetitle)
- [var imageSubtitle: String?](/documentation/messages/msmessagetemplatelayout/imagesubtitle)
- [var caption: String?](/documentation/messages/msmessagetemplatelayout/caption)
- [var subcaption: String?](/documentation/messages/msmessagetemplatelayout/subcaption)
- [var trailingCaption: String?](/documentation/messages/msmessagetemplatelayout/trailingcaption)
- [var trailingSubcaption: String?](/documentation/messages/msmessagetemplatelayout/trailingsubcaption)
- [MSMessageLiveLayout](/documentation/messages/msmessagelivelayout)

### Creating Live Layouts

- [init(alternateLayout: MSMessageTemplateLayout)](/documentation/messages/msmessagelivelayout/init(alternatelayout:))

### Accessing Properties

- [var alternateLayout: MSMessageTemplateLayout](/documentation/messages/msmessagelivelayout/alternatelayout)

## Critical messages

- [Sending SMS messages from an app](/documentation/messages/critical-messaging-api)
- [MSCriticalSMSMessenger](/documentation/messages/mscriticalsmsmessenger)

### Determining the maximum allowed recipients

- [var maximumCriticalMessagingRecipients: Int](/documentation/messages/mscriticalsmsmessenger/maximumcriticalmessagingrecipients)

### Requesting authorization

- [func requestAuthorization(for: [MSRecipient]) async throws -> [MSRecipient : MSCriticalMessagingAuthorizationStatus]](/documentation/messages/mscriticalsmsmessenger/requestauthorization(for:))

### Checking authorization status

- [func checkAuthorizationStatus(for: [MSRecipient]) async throws -> [MSRecipient : MSCriticalMessagingAuthorizationStatus]](/documentation/messages/mscriticalsmsmessenger/checkauthorizationstatus(for:))

### Sending critical messages

- [func send(MSCriticalMessage, to: MSRecipient) async throws -> Bool](/documentation/messages/mscriticalsmsmessenger/send(_:to:))

### Instance Methods

- [init()](/documentation/messages/mscriticalsmsmessenger/init())
- [MSRecipient](/documentation/messages/msrecipient)

### Creating recipients

- [init(phoneNumber: String)](/documentation/messages/msrecipient/init(phonenumber:))

### Properties

- [var phoneNumber: String](/documentation/messages/msrecipient/phonenumber)
- [MSCriticalMessage](/documentation/messages/mscriticalmessage)

### Initializers

- [init(messageText: String)](/documentation/messages/mscriticalmessage/init(messagetext:))

### Instance Properties

- [var messageText: String](/documentation/messages/mscriticalmessage/messagetext)
- [MSCriticalMessagingAuthorizationStatus](/documentation/messages/mscriticalmessagingauthorizationstatus)

### Authorization statuses

- [case unknown](/documentation/messages/mscriticalmessagingauthorizationstatus/unknown)
- [case denied](/documentation/messages/mscriticalmessagingauthorizationstatus/denied)
- [case approved](/documentation/messages/mscriticalmessagingauthorizationstatus/approved)

## Errors

- [let MSStickersErrorDomain: String](/documentation/messages/msstickerserrordomain)
- [let MSMessagesErrorDomain: String](/documentation/messages/msmessageserrordomain)
- [MSMessageErrorCode](/documentation/messages/msmessageerrorcode)

### Error Codes

- [case fileNotFound](/documentation/messages/msmessageerrorcode/filenotfound)
- [case fileUnreadable](/documentation/messages/msmessageerrorcode/fileunreadable)
- [case improperFileType](/documentation/messages/msmessageerrorcode/improperfiletype)
- [case improperFileURL](/documentation/messages/msmessageerrorcode/improperfileurl)
- [case stickerFileImproperFileAttributes](/documentation/messages/msmessageerrorcode/stickerfileimproperfileattributes)
- [case stickerFileImproperFileSize](/documentation/messages/msmessageerrorcode/stickerfileimproperfilesize)
- [case stickerFileImproperFileFormat](/documentation/messages/msmessageerrorcode/stickerfileimproperfileformat)
- [case urlExceedsMaxSize](/documentation/messages/msmessageerrorcode/urlexceedsmaxsize)
- [case sendWhileNotVisible](/documentation/messages/msmessageerrorcode/sendwhilenotvisible)
- [case sendWithoutRecentInteraction](/documentation/messages/msmessageerrorcode/sendwithoutrecentinteraction)
- [case apiUnavailableInPresentationContext](/documentation/messages/msmessageerrorcode/apiunavailableinpresentationcontext)
- [case unknown](/documentation/messages/msmessageerrorcode/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/messages/msmessageerrorcode/init(rawvalue:))
- [MSCriticalMessagingError](/documentation/messages/mscriticalmessagingerror)

### Error codes

- [case unknown](/documentation/messages/mscriticalmessagingerror/unknown)
- [case invalidAuthenticationRequest](/documentation/messages/mscriticalmessagingerror/invalidauthenticationrequest)
- [case notSupported](/documentation/messages/mscriticalmessagingerror/notsupported)
- [case notAuthorized](/documentation/messages/mscriticalmessagingerror/notauthorized)
- [case sendFailed](/documentation/messages/mscriticalmessagingerror/sendfailed)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
