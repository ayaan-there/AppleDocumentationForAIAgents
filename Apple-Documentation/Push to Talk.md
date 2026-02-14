# Push to Talk Documentation

Source: https://sosumi.ai/documentation/pushtotalk

---
title: Push to Talk
source: https://developer.apple.com/documentation/pushtotalk
timestamp: 2026-02-13T19:00:52.075Z
---

## Essentials

- [Creating a Push to Talk app](/documentation/pushtotalk/creating-a-push-to-talk-app)
- [PTChannelManager](/documentation/pushtotalk/ptchannelmanager)

### Creating a channel manager

- [class func channelManager(delegate: any PTChannelManagerDelegate, restorationDelegate: any PTChannelRestorationDelegate, completionHandler: (PTChannelManager?, (any Error)?) -> Void)](/documentation/pushtotalk/ptchannelmanager/channelmanager(delegate:restorationdelegate:completionhandler:))

### Inspecting the channel manager

- [var activeChannelUUID: UUID?](/documentation/pushtotalk/ptchannelmanager/activechanneluuid)

### Joining and leaving a channel

- [func requestJoinChannel(channelUUID: UUID, descriptor: PTChannelDescriptor)](/documentation/pushtotalk/ptchannelmanager/requestjoinchannel(channeluuid:descriptor:))
- [func leaveChannel(channelUUID: UUID)](/documentation/pushtotalk/ptchannelmanager/leavechannel(channeluuid:))

### Setting the transmission mode

- [func setTransmissionMode(PTTransmissionMode, channelUUID: UUID, completionHandler: (((any Error)?) -> Void)?)](/documentation/pushtotalk/ptchannelmanager/settransmissionmode(_:channeluuid:completionhandler:))

### Starting and stopping transmission

- [func requestBeginTransmitting(channelUUID: UUID)](/documentation/pushtotalk/ptchannelmanager/requestbegintransmitting(channeluuid:))
- [func stopTransmitting(channelUUID: UUID)](/documentation/pushtotalk/ptchannelmanager/stoptransmitting(channeluuid:))
- [func setAccessoryButtonEventsEnabled(Bool, channelUUID: UUID, completionHandler: (((any Error)?) -> Void)?)](/documentation/pushtotalk/ptchannelmanager/setaccessorybuttoneventsenabled(_:channeluuid:completionhandler:))

### Setting participants

- [func setActiveRemoteParticipant(PTParticipant?, channelUUID: UUID, completionHandler: (((any Error)?) -> Void)?)](/documentation/pushtotalk/ptchannelmanager/setactiveremoteparticipant(_:channeluuid:completionhandler:))

### Setting the channel descriptor

- [func setChannelDescriptor(PTChannelDescriptor, channelUUID: UUID, completionHandler: (((any Error)?) -> Void)?)](/documentation/pushtotalk/ptchannelmanager/setchanneldescriptor(_:channeluuid:completionhandler:))

### Setting the service status

- [func setServiceStatus(PTServiceStatus, channelUUID: UUID, completionHandler: (((any Error)?) -> Void)?)](/documentation/pushtotalk/ptchannelmanager/setservicestatus(_:channeluuid:completionhandler:))

## Channel management

- [PTChannelManagerDelegate](/documentation/pushtotalk/ptchannelmanagerdelegate)

### Beginning or ending transmission

- [func channelManager(PTChannelManager, channelUUID: UUID, didBeginTransmittingFrom: PTChannelTransmitRequestSource)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:channeluuid:didbegintransmittingfrom:))
- [func channelManager(PTChannelManager, channelUUID: UUID, didEndTransmittingFrom: PTChannelTransmitRequestSource)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:channeluuid:didendtransmittingfrom:))
- [func channelManager(PTChannelManager, failedToBeginTransmittingInChannel: UUID, error: any Error)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:failedtobegintransmittinginchannel:error:))
- [func channelManager(PTChannelManager, failedToStopTransmittingInChannel: UUID, error: any Error)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:failedtostoptransmittinginchannel:error:))
- [func incomingServiceUpdatePush(channelManager: PTChannelManager, channelUUID: UUID, pushPayload: [String : Any], isHighPriority: Bool, remainingHighPriorityBudget: Int, completion: () -> Void)](/documentation/pushtotalk/ptchannelmanagerdelegate/incomingserviceupdatepush(channelmanager:channeluuid:pushpayload:ishighpriority:remaininghighprioritybudget:completion:))

### Activating and deactivating the audio session

- [func channelManager(PTChannelManager, didActivate: AVAudioSession)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:didactivate:))
- [func channelManager(PTChannelManager, didDeactivate: AVAudioSession)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:diddeactivate:))

### Joining and leaving a channel

- [func channelManager(PTChannelManager, didJoinChannel: UUID, reason: PTChannelJoinReason)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:didjoinchannel:reason:))
- [func channelManager(PTChannelManager, didLeaveChannel: UUID, reason: PTChannelLeaveReason)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:didleavechannel:reason:))
- [func channelManager(PTChannelManager, failedToJoinChannel: UUID, error: any Error)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:failedtojoinchannel:error:))
- [func channelManager(PTChannelManager, failedToLeaveChannel: UUID, error: any Error)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:failedtoleavechannel:error:))

### Getting a push token

- [func channelManager(PTChannelManager, receivedEphemeralPushToken: Data)](/documentation/pushtotalk/ptchannelmanagerdelegate/channelmanager(_:receivedephemeralpushtoken:))

### Handling the push result

- [func incomingPushResult(channelManager: PTChannelManager, channelUUID: UUID, pushPayload: [String : Any]) -> PTPushResult](/documentation/pushtotalk/ptchannelmanagerdelegate/incomingpushresult(channelmanager:channeluuid:pushpayload:))
- [PTTransmissionMode](/documentation/pushtotalk/pttransmissionmode)

### Modes

- [case fullDuplex](/documentation/pushtotalk/pttransmissionmode/fullduplex)
- [case halfDuplex](/documentation/pushtotalk/pttransmissionmode/halfduplex)
- [case listenOnly](/documentation/pushtotalk/pttransmissionmode/listenonly)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/pttransmissionmode/init(rawvalue:))
- [PTServiceStatus](/documentation/pushtotalk/ptservicestatus)

### Statuses

- [case ready](/documentation/pushtotalk/ptservicestatus/ready)
- [case connecting](/documentation/pushtotalk/ptservicestatus/connecting)
- [case unavailable](/documentation/pushtotalk/ptservicestatus/unavailable)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptservicestatus/init(rawvalue:))
- [PTChannelJoinReason](/documentation/pushtotalk/ptchanneljoinreason)

### Join reasons

- [case developerRequest](/documentation/pushtotalk/ptchanneljoinreason/developerrequest)
- [case channelRestoration](/documentation/pushtotalk/ptchanneljoinreason/channelrestoration)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptchanneljoinreason/init(rawvalue:))
- [PTChannelLeaveReason](/documentation/pushtotalk/ptchannelleavereason)

### Leave reasons

- [case userRequest](/documentation/pushtotalk/ptchannelleavereason/userrequest)
- [case developerRequest](/documentation/pushtotalk/ptchannelleavereason/developerrequest)
- [case systemPolicy](/documentation/pushtotalk/ptchannelleavereason/systempolicy)
- [case unknown](/documentation/pushtotalk/ptchannelleavereason/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptchannelleavereason/init(rawvalue:))
- [PTChannelTransmitRequestSource](/documentation/pushtotalk/ptchanneltransmitrequestsource)

### Transmission sources

- [case userRequest](/documentation/pushtotalk/ptchanneltransmitrequestsource/userrequest)
- [case developerRequest](/documentation/pushtotalk/ptchanneltransmitrequestsource/developerrequest)
- [case handsfreeButton](/documentation/pushtotalk/ptchanneltransmitrequestsource/handsfreebutton)
- [case unknown](/documentation/pushtotalk/ptchanneltransmitrequestsource/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptchanneltransmitrequestsource/init(rawvalue:))

## Channel restoration

- [PTChannelDescriptor](/documentation/pushtotalk/ptchanneldescriptor)

### Creating a channel descriptor

- [init(name: String, image: UIImage?)](/documentation/pushtotalk/ptchanneldescriptor/init(name:image:))

### Inspecting a channel descriptor

- [var name: String](/documentation/pushtotalk/ptchanneldescriptor/name)
- [var image: UIImage?](/documentation/pushtotalk/ptchanneldescriptor/image)
- [PTChannelRestorationDelegate](/documentation/pushtotalk/ptchannelrestorationdelegate)

### Getting the channel descriptor

- [func channelDescriptor(restoredChannelUUID: UUID) -> PTChannelDescriptor](/documentation/pushtotalk/ptchannelrestorationdelegate/channeldescriptor(restoredchanneluuid:))

## Channel participants

- [PTParticipant](/documentation/pushtotalk/ptparticipant)

### Creating a participant

- [init(name: String, image: UIImage?)](/documentation/pushtotalk/ptparticipant/init(name:image:))

### Inspecting a participant

- [var name: String](/documentation/pushtotalk/ptparticipant/name)
- [var image: UIImage?](/documentation/pushtotalk/ptparticipant/image)

## Push notification results

- [PTPushResult](/documentation/pushtotalk/ptpushresult)

### Updating the active participant

- [class func activeRemoteParticipant(PTParticipant) -> PTPushResult](/documentation/pushtotalk/ptpushresult/activeremoteparticipant(_:))

### Leaving the channel

- [class var leaveChannel: PTPushResult](/documentation/pushtotalk/ptpushresult/leavechannel)

## Push to Talk errors

- [PTChannelError](/documentation/pushtotalk/ptchannelerror-swift.struct)

### Inspecting a channel error

- [PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/code)

#### Error codes

- [case unknown](/documentation/pushtotalk/ptchannelerror-swift.struct/code/unknown)
- [case appNotForeground](/documentation/pushtotalk/ptchannelerror-swift.struct/code/appnotforeground)
- [case channelNotFound](/documentation/pushtotalk/ptchannelerror-swift.struct/code/channelnotfound)
- [case channelLimitReached](/documentation/pushtotalk/ptchannelerror-swift.struct/code/channellimitreached)
- [case callActive](/documentation/pushtotalk/ptchannelerror-swift.struct/code/callactive)
- [case transmissionInProgress](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissioninprogress)
- [case transmissionNotFound](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissionnotfound)
- [case deviceManagementRestriction](/documentation/pushtotalk/ptchannelerror-swift.struct/code/devicemanagementrestriction)
- [case screenTimeRestriction](/documentation/pushtotalk/ptchannelerror-swift.struct/code/screentimerestriction)
- [case transmissionNotAllowed](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissionnotallowed)

#### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptchannelerror-swift.struct/code/init(rawvalue:))
- [Error constants](/documentation/pushtotalk/ptchannelerror-error-constants)

#### Constants

- [static var unknown: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/unknown)
- [static var appNotForeground: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/appnotforeground)
- [static var channelNotFound: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/channelnotfound)
- [static var channelLimitReached: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/channellimitreached)
- [static var callActive: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/callactive)
- [static var transmissionInProgress: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/transmissioninprogress)
- [static var transmissionNotFound: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/transmissionnotfound)
- [static var deviceManagementRestriction: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/devicemanagementrestriction)
- [static var screenTimeRestriction: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/screentimerestriction)
- [static var transmissionNotAllowed: PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/transmissionnotallowed)

### Type Properties

- [static var errorDomain: String](/documentation/pushtotalk/ptchannelerror-swift.struct/errordomain)
- [PTChannelError.Code](/documentation/pushtotalk/ptchannelerror-swift.struct/code)

### Error codes

- [case unknown](/documentation/pushtotalk/ptchannelerror-swift.struct/code/unknown)
- [case appNotForeground](/documentation/pushtotalk/ptchannelerror-swift.struct/code/appnotforeground)
- [case channelNotFound](/documentation/pushtotalk/ptchannelerror-swift.struct/code/channelnotfound)
- [case channelLimitReached](/documentation/pushtotalk/ptchannelerror-swift.struct/code/channellimitreached)
- [case callActive](/documentation/pushtotalk/ptchannelerror-swift.struct/code/callactive)
- [case transmissionInProgress](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissioninprogress)
- [case transmissionNotFound](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissionnotfound)
- [case deviceManagementRestriction](/documentation/pushtotalk/ptchannelerror-swift.struct/code/devicemanagementrestriction)
- [case screenTimeRestriction](/documentation/pushtotalk/ptchannelerror-swift.struct/code/screentimerestriction)
- [case transmissionNotAllowed](/documentation/pushtotalk/ptchannelerror-swift.struct/code/transmissionnotallowed)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptchannelerror-swift.struct/code/init(rawvalue:))
- [PTInstantiationError](/documentation/pushtotalk/ptinstantiationerror-swift.struct)

### Inspecting an instantiation error

- [PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code)

#### Error codes

- [case unknown](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/unknown)
- [case invalidPlatform](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/invalidplatform)
- [case missingBackgroundMode](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingbackgroundmode)
- [case missingPushServerEnvironment](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingpushserverenvironment)
- [case missingEntitlement](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingentitlement)
- [case instantiationAlreadyInProgress](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/instantiationalreadyinprogress)

#### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/init(rawvalue:))
- [Error constants](/documentation/pushtotalk/ptinstantiation-error-constants)

#### Constants

- [static var unknown: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/unknown)
- [static var invalidPlatform: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/invalidplatform)
- [static var missingBackgroundMode: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/missingbackgroundmode)
- [static var missingPushServerEnvironment: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/missingpushserverenvironment)
- [static var missingEntitlement: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/missingentitlement)
- [static var instantiationAlreadyInProgress: PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/instantiationalreadyinprogress)

### Type Properties

- [static var errorDomain: String](/documentation/pushtotalk/ptinstantiationerror-swift.struct/errordomain)
- [PTInstantiationError.Code](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code)

### Error codes

- [case unknown](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/unknown)
- [case invalidPlatform](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/invalidplatform)
- [case missingBackgroundMode](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingbackgroundmode)
- [case missingPushServerEnvironment](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingpushserverenvironment)
- [case missingEntitlement](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/missingentitlement)
- [case instantiationAlreadyInProgress](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/instantiationalreadyinprogress)

### Initializers

- [init?(rawValue: Int)](/documentation/pushtotalk/ptinstantiationerror-swift.struct/code/init(rawvalue:))
- [let PTChannelErrorDomain: String](/documentation/pushtotalk/ptchannelerrordomain)
- [let PTInstantiationErrorDomain: String](/documentation/pushtotalk/ptinstantiationerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
