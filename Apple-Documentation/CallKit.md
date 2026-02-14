# CallKit Documentation

Source: https://sosumi.ai/documentation/callkit

---
title: CallKit
source: https://developer.apple.com/documentation/callkit
timestamp: 2026-02-13T18:54:34.538Z
---

## Essentials

- [CXProvider](/documentation/callkit/cxprovider)

### Creating New Providers

- [init(configuration: CXProviderConfiguration)](/documentation/callkit/cxprovider/init(configuration:))

### Setting the Delegate

- [func setDelegate((any CXProviderDelegate)?, queue: dispatch_queue_t?)](/documentation/callkit/cxprovider/setdelegate(_:queue:))

### Accessing Provider Attributes

- [var configuration: CXProviderConfiguration](/documentation/callkit/cxprovider/configuration)

### Accessing Pending Transaction and Call Actions

- [var pendingTransactions: [CXTransaction]](/documentation/callkit/cxprovider/pendingtransactions)
- [func pendingCallActions(of: AnyClass, withCall: UUID) -> [CXCallAction]](/documentation/callkit/cxprovider/pendingcallactions(of:withcall:))

### Reporting Calls

- [func reportNewIncomingCall(with: UUID, update: CXCallUpdate, completion: ((any Error)?) -> Void)](/documentation/callkit/cxprovider/reportnewincomingcall(with:update:completion:))
- [class func reportNewIncomingVoIPPushPayload([AnyHashable : Any], completion: (((any Error)?) -> Void)?)](/documentation/callkit/cxprovider/reportnewincomingvoippushpayload(_:completion:))
- [com.apple.developer.usernotifications.filtering](/documentation/bundleresources/entitlements/com.apple.developer.usernotifications.filtering)
- [func reportOutgoingCall(with: UUID, startedConnectingAt: Date?)](/documentation/callkit/cxprovider/reportoutgoingcall(with:startedconnectingat:))
- [func reportOutgoingCall(with: UUID, connectedAt: Date?)](/documentation/callkit/cxprovider/reportoutgoingcall(with:connectedat:))
- [func reportCall(with: UUID, updated: CXCallUpdate)](/documentation/callkit/cxprovider/reportcall(with:updated:))
- [func reportCall(with: UUID, endedAt: Date?, reason: CXCallEndedReason)](/documentation/callkit/cxprovider/reportcall(with:endedat:reason:))

### Invalidating a Provider

- [func invalidate()](/documentation/callkit/cxprovider/invalidate())

### Handling Errors

- [CXCallEndedReason](/documentation/callkit/cxcallendedreason)

#### Constants

- [case failed](/documentation/callkit/cxcallendedreason/failed)
- [case remoteEnded](/documentation/callkit/cxcallendedreason/remoteended)
- [case unanswered](/documentation/callkit/cxcallendedreason/unanswered)
- [case answeredElsewhere](/documentation/callkit/cxcallendedreason/answeredelsewhere)
- [case declinedElsewhere](/documentation/callkit/cxcallendedreason/declinedelsewhere)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxcallendedreason/init(rawvalue:))
- [CXError](/documentation/callkit/cxerror)

#### Constants

- [static var invalidArgument: CXError.Code](/documentation/callkit/cxerror/invalidargument)
- [static var unentitled: CXError.Code](/documentation/callkit/cxerror/unentitled)
- [static var unknownError: CXError.Code](/documentation/callkit/cxerror/unknownerror)

#### Type Properties

- [static var missingVoIPBackgroundMode: CXError.Code](/documentation/callkit/cxerror/missingvoipbackgroundmode)
- [static var errorDomain: String](/documentation/callkit/cxerror/errordomain)

#### Enumerations

- [CXError.Code](/documentation/callkit/cxerror/code)

##### Constants

- [case invalidArgument](/documentation/callkit/cxerror/code/invalidargument)
- [case unentitled](/documentation/callkit/cxerror/code/unentitled)
- [case unknownError](/documentation/callkit/cxerror/code/unknownerror)

##### Enumeration Cases

- [case missingVoIPBackgroundMode](/documentation/callkit/cxerror/code/missingvoipbackgroundmode)

##### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerror/code/init(rawvalue:))
- [CXError.Code](/documentation/callkit/cxerror/code)

#### Constants

- [case invalidArgument](/documentation/callkit/cxerror/code/invalidargument)
- [case unentitled](/documentation/callkit/cxerror/code/unentitled)
- [case unknownError](/documentation/callkit/cxerror/code/unknownerror)

#### Enumeration Cases

- [case missingVoIPBackgroundMode](/documentation/callkit/cxerror/code/missingvoipbackgroundmode)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerror/code/init(rawvalue:))
- [CXErrorCodeIncomingCallError](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct)

#### Errors

- [static var callUUIDAlreadyExists: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/calluuidalreadyexists)
- [static var filteredByBlockList: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/filteredbyblocklist)
- [static var filteredByDoNotDisturb: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/filteredbydonotdisturb)
- [static var unentitled: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/unentitled)
- [static var unknown: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/unknown)

#### Type Properties

- [static var filteredDuringRestrictedSharingMode: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/filteredduringrestrictedsharingmode)
- [static var callIsProtected: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/callisprotected)
- [static var errorDomain: String](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/errordomain)
- [static var filteredBySensitiveParticipants: CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/filteredbysensitiveparticipants)

#### Enumerations

- [CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code)

##### Errors

- [case unknown](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/unknown)
- [case unentitled](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/unentitled)
- [case callUUIDAlreadyExists](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/calluuidalreadyexists)
- [case filteredByDoNotDisturb](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbydonotdisturb)
- [case filteredByBlockList](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbyblocklist)

##### Enumeration Cases

- [case filteredDuringRestrictedSharingMode](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredduringrestrictedsharingmode)
- [case callIsProtected](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/callisprotected)
- [case filteredBySensitiveParticipants](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbysensitiveparticipants)

##### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/init(rawvalue:))
- [CXErrorCodeIncomingCallError.Code](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code)

#### Errors

- [case unknown](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/unknown)
- [case unentitled](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/unentitled)
- [case callUUIDAlreadyExists](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/calluuidalreadyexists)
- [case filteredByDoNotDisturb](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbydonotdisturb)
- [case filteredByBlockList](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbyblocklist)

#### Enumeration Cases

- [case filteredDuringRestrictedSharingMode](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredduringrestrictedsharingmode)
- [case callIsProtected](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/callisprotected)
- [case filteredBySensitiveParticipants](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/filteredbysensitiveparticipants)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodeincomingcallerror-swift.struct/code/init(rawvalue:))
- [CXErrorCodeNotificationServiceExtensionError](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct)

#### Understanding Error Codes

- [static var invalidClientProcess: CXErrorCodeNotificationServiceExtensionError.Code](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/invalidclientprocess)
- [static var missingNotificationFilteringEntitlement: CXErrorCodeNotificationServiceExtensionError.Code](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/missingnotificationfilteringentitlement)
- [static var unknown: CXErrorCodeNotificationServiceExtensionError.Code](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/unknown)
- [CXErrorCodeNotificationServiceExtensionError.Code](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code)

##### Error Codes

- [case invalidClientProcess](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/invalidclientprocess)
- [case missingNotificationFilteringEntitlement](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/missingnotificationfilteringentitlement)
- [case unknown](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/unknown)

##### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/errordomain)
- [let CXErrorDomain: String](/documentation/callkit/cxerrordomain)
- [let CXErrorDomainIncomingCall: String](/documentation/callkit/cxerrordomainincomingcall)
- [CXProviderDelegate](/documentation/callkit/cxproviderdelegate)

### Handling Provider Events

- [func providerDidBegin(CXProvider)](/documentation/callkit/cxproviderdelegate/providerdidbegin(_:))
- [func providerDidReset(CXProvider)](/documentation/callkit/cxproviderdelegate/providerdidreset(_:))

### Determining the Execution of Transactions

- [func provider(CXProvider, execute: CXTransaction) -> Bool](/documentation/callkit/cxproviderdelegate/provider(_:execute:))

### Handling Call Actions

- [func provider(CXProvider, perform: CXStartCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-2lem5)
- [func provider(CXProvider, perform: CXAnswerCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-h4in)
- [func provider(CXProvider, perform: CXEndCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-9a0m)
- [func provider(CXProvider, perform: CXSetHeldCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-947b1)
- [func provider(CXProvider, perform: CXSetMutedCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-4u3yu)
- [func provider(CXProvider, perform: CXSetGroupCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-9masw)
- [func provider(CXProvider, perform: CXPlayDTMFCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-4htxt)
- [func provider(CXProvider, perform: CXSetTranslatingCallAction)](/documentation/callkit/cxproviderdelegate/provider(_:perform:)-43atg)
- [func provider(CXProvider, timedOutPerforming: CXAction)](/documentation/callkit/cxproviderdelegate/provider(_:timedoutperforming:))

### Handling Changes to Audio Session Activation State

- [func provider(CXProvider, didActivate: AVAudioSession)](/documentation/callkit/cxproviderdelegate/provider(_:didactivate:))
- [func provider(CXProvider, didDeactivate: AVAudioSession)](/documentation/callkit/cxproviderdelegate/provider(_:diddeactivate:))
- [CXProviderConfiguration](/documentation/callkit/cxproviderconfiguration)

### Creating New Configurations

- [init()](/documentation/callkit/cxproviderconfiguration/init())
- [convenience init(localizedName: String)](/documentation/callkit/cxproviderconfiguration/init(localizedname:))

### Configuring Native Call UI

- [var localizedName: String?](/documentation/callkit/cxproviderconfiguration/localizedname)
- [var ringtoneSound: String?](/documentation/callkit/cxproviderconfiguration/ringtonesound)
- [var iconTemplateImageData: Data?](/documentation/callkit/cxproviderconfiguration/icontemplateimagedata)

### Configuring Call Capabilities

- [var maximumCallGroups: Int](/documentation/callkit/cxproviderconfiguration/maximumcallgroups)
- [var maximumCallsPerCallGroup: Int](/documentation/callkit/cxproviderconfiguration/maximumcallspercallgroup)
- [var supportedHandleTypes: Set<CXHandle.HandleType>](/documentation/callkit/cxproviderconfiguration/supportedhandletypes-kd6i)
- [var supportsVideo: Bool](/documentation/callkit/cxproviderconfiguration/supportsvideo)
- [var includesCallsInRecents: Bool](/documentation/callkit/cxproviderconfiguration/includescallsinrecents)

### Instance Properties

- [var supportsAudioTranslation: Bool](/documentation/callkit/cxproviderconfiguration/supportsaudiotranslation)
- [Making and receiving VoIP calls](/documentation/callkit/making-and-receiving-voip-calls)
- [VoIP calling with CallKit](/documentation/callkit/voip-calling-with-callkit)
- [Preparing your app to be the default calling app](/documentation/callkit/preparing-your-app-to-be-the-default-calling-app)
- [CallKit updates](/documentation/updates/callkit)

## Incoming calls

- [Responding to VoIP Notifications from PushKit](/documentation/pushkit/responding-to-voip-notifications-from-pushkit)
- [CXCallUpdate](/documentation/callkit/cxcallupdate)

### Accessing Call Update Attributes

- [var localizedCallerName: String?](/documentation/callkit/cxcallupdate/localizedcallername)
- [var remoteHandle: CXHandle?](/documentation/callkit/cxcallupdate/remotehandle)
- [var hasVideo: Bool](/documentation/callkit/cxcallupdate/hasvideo)
- [var supportsGrouping: Bool](/documentation/callkit/cxcallupdate/supportsgrouping)
- [var supportsUngrouping: Bool](/documentation/callkit/cxcallupdate/supportsungrouping)
- [var supportsHolding: Bool](/documentation/callkit/cxcallupdate/supportsholding)
- [var supportsDTMF: Bool](/documentation/callkit/cxcallupdate/supportsdtmf)
- [CXAnswerCallAction](/documentation/callkit/cxanswercallaction)

### Completing Actions

- [func fulfill(withDateConnected: Date)](/documentation/callkit/cxanswercallaction/fulfill(withdateconnected:))

## Outgoing calls

- [Sending End-to-End Encrypted VoIP Calls](/documentation/callkit/sending-end-to-end-encrypted-voip-calls)
- [CXCallController](/documentation/callkit/cxcallcontroller)

### Creating New Call Controllers

- [convenience init()](/documentation/callkit/cxcallcontroller/init())
- [init(queue: dispatch_queue_t)](/documentation/callkit/cxcallcontroller/init(queue:))

### Accessing the Call Observer

- [var callObserver: CXCallObserver](/documentation/callkit/cxcallcontroller/callobserver)

### Requesting Transactions

- [func request(CXTransaction, completion: ((any Error)?) -> Void)](/documentation/callkit/cxcallcontroller/request(_:completion:))
- [func requestTransaction(with: CXAction, completion: ((any Error)?) -> Void)](/documentation/callkit/cxcallcontroller/requesttransaction(with:completion:)-ffme)
- [func requestTransaction(with: [CXAction], completion: ((any Error)?) -> Void)](/documentation/callkit/cxcallcontroller/requesttransaction(with:completion:)-4o1m4)

### Errors

- [CXErrorCodeRequestTransactionError](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct)

#### Constants

- [static var unknown: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/unknown)
- [static var unentitled: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/unentitled)
- [static var unknownCallProvider: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/unknowncallprovider)
- [static var emptyTransaction: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/emptytransaction)
- [static var unknownCallUUID: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/unknowncalluuid)
- [static var callUUIDAlreadyExists: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/calluuidalreadyexists)
- [static var invalidAction: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/invalidaction)
- [static var maximumCallGroupsReached: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/maximumcallgroupsreached)

#### Enumerations

- [CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code)

##### Constants

- [case unknown](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknown)
- [case unentitled](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unentitled)
- [case unknownCallProvider](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknowncallprovider)
- [case emptyTransaction](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/emptytransaction)
- [case unknownCallUUID](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknowncalluuid)
- [case callUUIDAlreadyExists](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/calluuidalreadyexists)
- [case invalidAction](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/invalidaction)
- [case maximumCallGroupsReached](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/maximumcallgroupsreached)

##### Enumeration Cases

- [case callIsProtected](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/callisprotected)

##### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [static var callIsProtected: CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/callisprotected)
- [static var errorDomain: String](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/errordomain)
- [CXErrorCodeRequestTransactionError.Code](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code)

#### Constants

- [case unknown](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknown)
- [case unentitled](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unentitled)
- [case unknownCallProvider](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknowncallprovider)
- [case emptyTransaction](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/emptytransaction)
- [case unknownCallUUID](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/unknowncalluuid)
- [case callUUIDAlreadyExists](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/calluuidalreadyexists)
- [case invalidAction](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/invalidaction)
- [case maximumCallGroupsReached](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/maximumcallgroupsreached)

#### Enumeration Cases

- [case callIsProtected](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/callisprotected)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcoderequesttransactionerror-swift.struct/code/init(rawvalue:))
- [let CXErrorDomainRequestTransaction: String](/documentation/callkit/cxerrordomainrequesttransaction)
- [CXTransaction](/documentation/callkit/cxtransaction)

### Creating New Transactions

- [convenience init(action: CXAction)](/documentation/callkit/cxtransaction/init(action:))
- [init(actions: [CXAction])](/documentation/callkit/cxtransaction/init(actions:))

### Accessing Transaction Attributes

- [var uuid: UUID](/documentation/callkit/cxtransaction/uuid)
- [var isComplete: Bool](/documentation/callkit/cxtransaction/iscomplete)
- [var actions: [CXAction]](/documentation/callkit/cxtransaction/actions)

### Adding Actions

- [func addAction(CXAction)](/documentation/callkit/cxtransaction/addaction(_:))
- [CXStartCallAction](/documentation/callkit/cxstartcallaction)

### Creating New Actions

- [init(call: UUID, handle: CXHandle)](/documentation/callkit/cxstartcallaction/init(call:handle:))
- [init?(coder: NSCoder)](/documentation/callkit/cxstartcallaction/init(coder:))

### Accessing Action Attributes

- [var isVideo: Bool](/documentation/callkit/cxstartcallaction/isvideo)
- [var contactIdentifier: String?](/documentation/callkit/cxstartcallaction/contactidentifier)
- [var handle: CXHandle](/documentation/callkit/cxstartcallaction/handle)

### Completing Actions

- [func fulfill(withDateStarted: Date)](/documentation/callkit/cxstartcallaction/fulfill(withdatestarted:))

## Call-related actions

- [CXAction](/documentation/callkit/cxaction)

### Creating an Action

- [init()](/documentation/callkit/cxaction/init())
- [init?(coder: NSCoder)](/documentation/callkit/cxaction/init(coder:))

### Accessing Action Attributes

- [var uuid: UUID](/documentation/callkit/cxaction/uuid)
- [var isComplete: Bool](/documentation/callkit/cxaction/iscomplete)
- [var timeoutDate: Date](/documentation/callkit/cxaction/timeoutdate)

### Completing Actions

- [func fulfill()](/documentation/callkit/cxaction/fulfill())
- [func fail()](/documentation/callkit/cxaction/fail())
- [CXCallAction](/documentation/callkit/cxcallaction)

### Creating New Call Actions

- [init(call: UUID)](/documentation/callkit/cxcallaction/init(call:))
- [init?(coder: NSCoder)](/documentation/callkit/cxcallaction/init(coder:))

### Accessing Call Action Attributes

- [var callUUID: UUID](/documentation/callkit/cxcallaction/calluuid)
- [CXEndCallAction](/documentation/callkit/cxendcallaction)

### Completing Actions

- [func fulfill(withDateEnded: Date)](/documentation/callkit/cxendcallaction/fulfill(withdateended:))
- [CXPlayDTMFCallAction](/documentation/callkit/cxplaydtmfcallaction)

### Creating New Actions

- [init(call: UUID, digits: String, type: CXPlayDTMFCallAction.ActionType)](/documentation/callkit/cxplaydtmfcallaction/init(call:digits:type:))
- [init?(coder: NSCoder)](/documentation/callkit/cxplaydtmfcallaction/init(coder:))

### Accessing Action Information

- [var digits: String](/documentation/callkit/cxplaydtmfcallaction/digits)
- [var type: CXPlayDTMFCallAction.ActionType](/documentation/callkit/cxplaydtmfcallaction/type)

### Constants

- [CXPlayDTMFCallAction.ActionType](/documentation/callkit/cxplaydtmfcallaction/actiontype)

#### Constants

- [case singleTone](/documentation/callkit/cxplaydtmfcallaction/actiontype/singletone)
- [case softPause](/documentation/callkit/cxplaydtmfcallaction/actiontype/softpause)
- [case hardPause](/documentation/callkit/cxplaydtmfcallaction/actiontype/hardpause)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxplaydtmfcallaction/actiontype/init(rawvalue:))
- [CXSetGroupCallAction](/documentation/callkit/cxsetgroupcallaction)

### Creating New Actions

- [init(call: UUID, callUUIDToGroupWith: UUID?)](/documentation/callkit/cxsetgroupcallaction/init(call:calluuidtogroupwith:))
- [init?(coder: NSCoder)](/documentation/callkit/cxsetgroupcallaction/init(coder:))

### Accessing Action Attributes

- [var callUUIDToGroupWith: UUID?](/documentation/callkit/cxsetgroupcallaction/calluuidtogroupwith)
- [CXSetHeldCallAction](/documentation/callkit/cxsetheldcallaction)

### Creating New Actions

- [init(call: UUID, onHold: Bool)](/documentation/callkit/cxsetheldcallaction/init(call:onhold:))
- [init?(coder: NSCoder)](/documentation/callkit/cxsetheldcallaction/init(coder:))

### Accessing Action Information

- [var isOnHold: Bool](/documentation/callkit/cxsetheldcallaction/isonhold)
- [CXSetMutedCallAction](/documentation/callkit/cxsetmutedcallaction)

### Creating New Actions

- [convenience init(call: UUID, muted: Bool)](/documentation/callkit/cxsetmutedcallaction/init(call:muted:))
- [init?(coder: NSCoder)](/documentation/callkit/cxsetmutedcallaction/init(coder:))

### Accessing Action Attributes

- [var isMuted: Bool](/documentation/callkit/cxsetmutedcallaction/ismuted)
- [CXSetTranslatingCallAction](/documentation/callkit/cxsettranslatingcallaction)

### Creating New Actions

- [init?(coder: NSCoder)](/documentation/callkit/cxsettranslatingcallaction/init(coder:))

### Accessing Action Attributes

- [var isTranslating: Bool](/documentation/callkit/cxsettranslatingcallaction/istranslating)

### Completing Actions

- [CXTranslationEngine](/documentation/callkit/cxtranslationengine)

#### Types

- [case `default`](/documentation/callkit/cxtranslationengine/default)

#### Enumeration Cases

- [case custom](/documentation/callkit/cxtranslationengine/custom)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxtranslationengine/init(rawvalue:))

### Initializers

- [init(call: UUID, isTranslating: Bool, localLanguage: String, remoteLanguage: String)](/documentation/callkit/cxsettranslatingcallaction/init(call:istranslating:locallanguage:remotelanguage:))

### Instance Properties

- [var localLanguage: String](/documentation/callkit/cxsettranslatingcallaction/locallanguage)
- [var remoteLanguage: String](/documentation/callkit/cxsettranslatingcallaction/remotelanguage)

### Instance Methods

- [func fulfill(using: CXTranslationEngine)](/documentation/callkit/cxsettranslatingcallaction/fulfill(using:))

## Call information

- [CXCall](/documentation/callkit/cxcall)

### Accessing Call Attributes

- [var uuid: UUID](/documentation/callkit/cxcall/uuid)
- [var isOutgoing: Bool](/documentation/callkit/cxcall/isoutgoing)
- [var hasConnected: Bool](/documentation/callkit/cxcall/hasconnected)
- [var hasEnded: Bool](/documentation/callkit/cxcall/hasended)
- [var isOnHold: Bool](/documentation/callkit/cxcall/isonhold)
- [CXCallObserver](/documentation/callkit/cxcallobserver)

### Setting a Delegate

- [func setDelegate((any CXCallObserverDelegate)?, queue: dispatch_queue_t?)](/documentation/callkit/cxcallobserver/setdelegate(_:queue:))

### Accessing Calls

- [var calls: [CXCall]](/documentation/callkit/cxcallobserver/calls)
- [CXCallObserverDelegate](/documentation/callkit/cxcallobserverdelegate)

### Responding to Changes in Call State

- [func callObserver(CXCallObserver, callChanged: CXCall)](/documentation/callkit/cxcallobserverdelegate/callobserver(_:callchanged:))
- [CXHandle](/documentation/callkit/cxhandle)

### Creating New Handles

- [init(type: CXHandle.HandleType, value: String)](/documentation/callkit/cxhandle/init(type:value:))

### Accessing Handle Attributes

- [var type: CXHandle.HandleType](/documentation/callkit/cxhandle/type)
- [var value: String](/documentation/callkit/cxhandle/value)

### Constants

- [CXHandle.HandleType](/documentation/callkit/cxhandle/handletype)

#### Constants

- [case generic](/documentation/callkit/cxhandle/handletype/generic)
- [case phoneNumber](/documentation/callkit/cxhandle/handletype/phonenumber)
- [case emailAddress](/documentation/callkit/cxhandle/handletype/emailaddress)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxhandle/handletype/init(rawvalue:))

## Caller ID

- [Identifying and blocking calls](/documentation/callkit/identifying-and-blocking-calls)
- [CXCallDirectoryProvider](/documentation/callkit/cxcalldirectoryprovider)

### Beginning a Request

- [func beginRequest(with: CXCallDirectoryExtensionContext)](/documentation/callkit/cxcalldirectoryprovider/beginrequest(with:))
- [CXCallDirectoryExtensionContext](/documentation/callkit/cxcalldirectoryextensioncontext)

### Setting the Delegate

- [var delegate: (any CXCallDirectoryExtensionContextDelegate)?](/documentation/callkit/cxcalldirectoryextensioncontext/delegate)

### Adding Entries

- [func addIdentificationEntry(withNextSequentialPhoneNumber: CXCallDirectoryPhoneNumber, label: String)](/documentation/callkit/cxcalldirectoryextensioncontext/addidentificationentry(withnextsequentialphonenumber:label:))
- [func addBlockingEntry(withNextSequentialPhoneNumber: CXCallDirectoryPhoneNumber)](/documentation/callkit/cxcalldirectoryextensioncontext/addblockingentry(withnextsequentialphonenumber:))

### Removing Entries

- [func removeAllBlockingEntries()](/documentation/callkit/cxcalldirectoryextensioncontext/removeallblockingentries())
- [func removeAllIdentificationEntries()](/documentation/callkit/cxcalldirectoryextensioncontext/removeallidentificationentries())
- [func removeBlockingEntry(withPhoneNumber: CXCallDirectoryPhoneNumber)](/documentation/callkit/cxcalldirectoryextensioncontext/removeblockingentry(withphonenumber:))
- [func removeIdentificationEntry(withPhoneNumber: CXCallDirectoryPhoneNumber)](/documentation/callkit/cxcalldirectoryextensioncontext/removeidentificationentry(withphonenumber:))

### Completing Requests

- [var isIncremental: Bool](/documentation/callkit/cxcalldirectoryextensioncontext/isincremental)
- [func completeRequest(completionHandler: ((Bool) -> Void)?)](/documentation/callkit/cxcalldirectoryextensioncontext/completerequest(completionhandler:))

### Types

- [CXCallDirectoryPhoneNumber](/documentation/callkit/cxcalldirectoryphonenumber)
- [let CXCallDirectoryPhoneNumberMax: CXCallDirectoryPhoneNumber](/documentation/callkit/cxcalldirectoryphonenumbermax)
- [CXCallDirectoryExtensionContextDelegate](/documentation/callkit/cxcalldirectoryextensioncontextdelegate)

### Handling Request Failures

- [func requestFailed(for: CXCallDirectoryExtensionContext, withError: any Error)](/documentation/callkit/cxcalldirectoryextensioncontextdelegate/requestfailed(for:witherror:))
- [CXCallDirectoryManager](/documentation/callkit/cxcalldirectorymanager)

### Accessing the Shared Instance

- [class var sharedInstance: CXCallDirectoryManager](/documentation/callkit/cxcalldirectorymanager/sharedinstance)

### Working with a Call Directory App Extension

- [func getEnabledStatusForExtension(withIdentifier: String, completionHandler: (CXCallDirectoryManager.EnabledStatus, (any Error)?) -> Void)](/documentation/callkit/cxcalldirectorymanager/getenabledstatusforextension(withidentifier:completionhandler:))
- [func reloadExtension(withIdentifier: String, completionHandler: (((any Error)?) -> Void)?)](/documentation/callkit/cxcalldirectorymanager/reloadextension(withidentifier:completionhandler:))
- [CXCallDirectoryManager.EnabledStatus](/documentation/callkit/cxcalldirectorymanager/enabledstatus)

#### Constants

- [case unknown](/documentation/callkit/cxcalldirectorymanager/enabledstatus/unknown)
- [case disabled](/documentation/callkit/cxcalldirectorymanager/enabledstatus/disabled)
- [case enabled](/documentation/callkit/cxcalldirectorymanager/enabledstatus/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxcalldirectorymanager/enabledstatus/init(rawvalue:))

### Opening the Settings App

- [func openSettings(completionHandler: (((any Error)?) -> Void)?)](/documentation/callkit/cxcalldirectorymanager/opensettings(completionhandler:))

### Errors

- [CXCallDirectoryManager.EnabledStatus](/documentation/callkit/cxcalldirectorymanager/enabledstatus)

#### Constants

- [case unknown](/documentation/callkit/cxcalldirectorymanager/enabledstatus/unknown)
- [case disabled](/documentation/callkit/cxcalldirectorymanager/enabledstatus/disabled)
- [case enabled](/documentation/callkit/cxcalldirectorymanager/enabledstatus/enabled)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxcalldirectorymanager/enabledstatus/init(rawvalue:))
- [CXErrorCodeCallDirectoryManagerError](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct)

#### Constants

- [static var unknown: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/unknown)
- [static var noExtensionFound: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/noextensionfound)
- [static var currentlyLoading: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/currentlyloading)
- [static var loadingInterrupted: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/loadinginterrupted)
- [static var entriesOutOfOrder: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/entriesoutoforder)
- [static var duplicateEntries: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/duplicateentries)
- [static var maximumEntriesExceeded: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/maximumentriesexceeded)
- [static var extensionDisabled: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/extensiondisabled)
- [static var unexpectedIncrementalRemoval: CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/unexpectedincrementalremoval)

#### Enumerations

- [CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code)

##### Constants

- [case unknown](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/unknown)
- [case noExtensionFound](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/noextensionfound)
- [case currentlyLoading](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/currentlyloading)
- [case loadingInterrupted](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/loadinginterrupted)
- [case entriesOutOfOrder](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/entriesoutoforder)
- [case duplicateEntries](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/duplicateentries)
- [case maximumEntriesExceeded](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/maximumentriesexceeded)
- [case extensionDisabled](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/extensiondisabled)
- [case unexpectedIncrementalRemoval](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/unexpectedincrementalremoval)

##### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/errordomain)
- [CXErrorCodeCallDirectoryManagerError.Code](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code)

#### Constants

- [case unknown](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/unknown)
- [case noExtensionFound](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/noextensionfound)
- [case currentlyLoading](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/currentlyloading)
- [case loadingInterrupted](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/loadinginterrupted)
- [case entriesOutOfOrder](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/entriesoutoforder)
- [case duplicateEntries](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/duplicateentries)
- [case maximumEntriesExceeded](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/maximumentriesexceeded)
- [case extensionDisabled](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/extensiondisabled)
- [case unexpectedIncrementalRemoval](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/unexpectedincrementalremoval)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodecalldirectorymanagererror-swift.struct/code/init(rawvalue:))
- [let CXErrorDomainCallDirectoryManager: String](/documentation/callkit/cxerrordomaincalldirectorymanager)

## Reference

- [CallKit Enumerations](/documentation/callkit/callkit-enumerations)

### Enumerations

- [CXErrorCodeNotificationServiceExtensionError.Code](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code)

#### Error Codes

- [case invalidClientProcess](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/invalidclientprocess)
- [case missingNotificationFilteringEntitlement](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/missingnotificationfilteringentitlement)
- [case unknown](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/unknown)

#### Initializers

- [init?(rawValue: Int)](/documentation/callkit/cxerrorcodenotificationserviceextensionerror-swift.struct/code/init(rawvalue:))
- [CallKit Constants](/documentation/callkit/callkit-constants)

### Constants

- [let CXErrorDomainNotificationServiceExtension: String](/documentation/callkit/cxerrordomainnotificationserviceextension)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
