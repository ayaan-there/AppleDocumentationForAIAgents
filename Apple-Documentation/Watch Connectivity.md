# Watch Connectivity Documentation

Source: https://sosumi.ai/documentation/watchconnectivity

---
title: Watch Connectivity
source: https://developer.apple.com/documentation/watchconnectivity
timestamp: 2026-02-13T19:03:56.664Z
---

## Essentials

- [WCSession](/documentation/watchconnectivity/wcsession)

### Getting the Default Session

- [class func isSupported() -> Bool](/documentation/watchconnectivity/wcsession/issupported())
- [class var `default`: WCSession](/documentation/watchconnectivity/wcsession/default)

### Configuring the Session

- [var delegate: (any WCSessionDelegate)?](/documentation/watchconnectivity/wcsession/delegate)
- [func activate()](/documentation/watchconnectivity/wcsession/activate())
- [var activationState: WCSessionActivationState](/documentation/watchconnectivity/wcsession/activationstate)

### Getting the Paired Device Information

- [var isPaired: Bool](/documentation/watchconnectivity/wcsession/ispaired)
- [var iOSDeviceNeedsUnlockAfterRebootForReachability: Bool](/documentation/watchconnectivity/wcsession/iosdeviceneedsunlockafterrebootforreachability)
- [var isWatchAppInstalled: Bool](/documentation/watchconnectivity/wcsession/iswatchappinstalled)
- [var isCompanionAppInstalled: Bool](/documentation/watchconnectivity/wcsession/iscompanionappinstalled)
- [var isComplicationEnabled: Bool](/documentation/watchconnectivity/wcsession/iscomplicationenabled)
- [var watchDirectoryURL: URL?](/documentation/watchconnectivity/wcsession/watchdirectoryurl)

### Determining the Session’s Reachability

- [var isReachable: Bool](/documentation/watchconnectivity/wcsession/isreachable)

### Managing Background Updates

- [func updateApplicationContext([String : Any]) throws](/documentation/watchconnectivity/wcsession/updateapplicationcontext(_:))
- [var applicationContext: [String : Any]](/documentation/watchconnectivity/wcsession/applicationcontext)
- [var receivedApplicationContext: [String : Any]](/documentation/watchconnectivity/wcsession/receivedapplicationcontext)

### Sending Messages

- [func sendMessage([String : Any], replyHandler: (([String : Any]) -> Void)?, errorHandler: ((any Error) -> Void)?)](/documentation/watchconnectivity/wcsession/sendmessage(_:replyhandler:errorhandler:))
- [func sendMessageData(Data, replyHandler: ((Data) -> Void)?, errorHandler: ((any Error) -> Void)?)](/documentation/watchconnectivity/wcsession/sendmessagedata(_:replyhandler:errorhandler:))

### Updating Complication Data

- [var remainingComplicationUserInfoTransfers: Int](/documentation/watchconnectivity/wcsession/remainingcomplicationuserinfotransfers)
- [func transferCurrentComplicationUserInfo([String : Any]) -> WCSessionUserInfoTransfer](/documentation/watchconnectivity/wcsession/transfercurrentcomplicationuserinfo(_:))

### Transferring Data in the Background

- [func transferUserInfo([String : Any]) -> WCSessionUserInfoTransfer](/documentation/watchconnectivity/wcsession/transferuserinfo(_:))
- [var outstandingUserInfoTransfers: [WCSessionUserInfoTransfer]](/documentation/watchconnectivity/wcsession/outstandinguserinfotransfers)

### Transferring Files in the Background

- [func transferFile(URL, metadata: [String : Any]?) -> WCSessionFileTransfer](/documentation/watchconnectivity/wcsession/transferfile(_:metadata:))
- [var outstandingFileTransfers: [WCSessionFileTransfer]](/documentation/watchconnectivity/wcsession/outstandingfiletransfers)
- [var hasContentPending: Bool](/documentation/watchconnectivity/wcsession/hascontentpending)

### Constants

- [WCSessionActivationState](/documentation/watchconnectivity/wcsessionactivationstate)

#### Constants

- [case notActivated](/documentation/watchconnectivity/wcsessionactivationstate/notactivated)
- [case inactive](/documentation/watchconnectivity/wcsessionactivationstate/inactive)
- [case activated](/documentation/watchconnectivity/wcsessionactivationstate/activated)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchconnectivity/wcsessionactivationstate/init(rawvalue:))
- [let WCErrorDomain: String](/documentation/watchconnectivity/wcerrordomain)
- [WCError](/documentation/watchconnectivity/wcerror)

#### Understanding Error Codes

- [static var genericError: WCError.Code](/documentation/watchconnectivity/wcerror/genericerror)
- [static var sessionNotSupported: WCError.Code](/documentation/watchconnectivity/wcerror/sessionnotsupported)
- [static var sessionMissingDelegate: WCError.Code](/documentation/watchconnectivity/wcerror/sessionmissingdelegate)
- [static var sessionNotActivated: WCError.Code](/documentation/watchconnectivity/wcerror/sessionnotactivated)
- [static var deviceNotPaired: WCError.Code](/documentation/watchconnectivity/wcerror/devicenotpaired)
- [static var watchAppNotInstalled: WCError.Code](/documentation/watchconnectivity/wcerror/watchappnotinstalled)
- [static var notReachable: WCError.Code](/documentation/watchconnectivity/wcerror/notreachable)
- [static var invalidParameter: WCError.Code](/documentation/watchconnectivity/wcerror/invalidparameter)
- [static var payloadTooLarge: WCError.Code](/documentation/watchconnectivity/wcerror/payloadtoolarge)
- [static var payloadUnsupportedTypes: WCError.Code](/documentation/watchconnectivity/wcerror/payloadunsupportedtypes)
- [static var messageReplyFailed: WCError.Code](/documentation/watchconnectivity/wcerror/messagereplyfailed)
- [static var messageReplyTimedOut: WCError.Code](/documentation/watchconnectivity/wcerror/messagereplytimedout)
- [static var fileAccessDenied: WCError.Code](/documentation/watchconnectivity/wcerror/fileaccessdenied)
- [static var deliveryFailed: WCError.Code](/documentation/watchconnectivity/wcerror/deliveryfailed)
- [static var insufficientSpace: WCError.Code](/documentation/watchconnectivity/wcerror/insufficientspace)
- [static var sessionInactive: WCError.Code](/documentation/watchconnectivity/wcerror/sessioninactive)
- [static var transferTimedOut: WCError.Code](/documentation/watchconnectivity/wcerror/transfertimedout)
- [static var companionAppNotInstalled: WCError.Code](/documentation/watchconnectivity/wcerror/companionappnotinstalled)
- [static var watchOnlyApp: WCError.Code](/documentation/watchconnectivity/wcerror/watchonlyapp)

#### Enumerations

- [WCError.Code](/documentation/watchconnectivity/wcerror/code)

##### Error Codes

- [case genericError](/documentation/watchconnectivity/wcerror/code/genericerror)
- [case sessionNotSupported](/documentation/watchconnectivity/wcerror/code/sessionnotsupported)
- [case sessionMissingDelegate](/documentation/watchconnectivity/wcerror/code/sessionmissingdelegate)
- [case sessionNotActivated](/documentation/watchconnectivity/wcerror/code/sessionnotactivated)
- [case deviceNotPaired](/documentation/watchconnectivity/wcerror/code/devicenotpaired)
- [case watchAppNotInstalled](/documentation/watchconnectivity/wcerror/code/watchappnotinstalled)
- [case notReachable](/documentation/watchconnectivity/wcerror/code/notreachable)
- [case invalidParameter](/documentation/watchconnectivity/wcerror/code/invalidparameter)
- [case payloadTooLarge](/documentation/watchconnectivity/wcerror/code/payloadtoolarge)
- [case payloadUnsupportedTypes](/documentation/watchconnectivity/wcerror/code/payloadunsupportedtypes)
- [case messageReplyFailed](/documentation/watchconnectivity/wcerror/code/messagereplyfailed)
- [case messageReplyTimedOut](/documentation/watchconnectivity/wcerror/code/messagereplytimedout)
- [case fileAccessDenied](/documentation/watchconnectivity/wcerror/code/fileaccessdenied)
- [case deliveryFailed](/documentation/watchconnectivity/wcerror/code/deliveryfailed)
- [case insufficientSpace](/documentation/watchconnectivity/wcerror/code/insufficientspace)
- [case sessionInactive](/documentation/watchconnectivity/wcerror/code/sessioninactive)
- [case transferTimedOut](/documentation/watchconnectivity/wcerror/code/transfertimedout)
- [case companionAppNotInstalled](/documentation/watchconnectivity/wcerror/code/companionappnotinstalled)
- [case watchOnlyApp](/documentation/watchconnectivity/wcerror/code/watchonlyapp)

##### Initializers

- [init?(rawValue: Int)](/documentation/watchconnectivity/wcerror/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/watchconnectivity/wcerror/errordomain)
- [WCError.Code](/documentation/watchconnectivity/wcerror/code)

#### Error Codes

- [case genericError](/documentation/watchconnectivity/wcerror/code/genericerror)
- [case sessionNotSupported](/documentation/watchconnectivity/wcerror/code/sessionnotsupported)
- [case sessionMissingDelegate](/documentation/watchconnectivity/wcerror/code/sessionmissingdelegate)
- [case sessionNotActivated](/documentation/watchconnectivity/wcerror/code/sessionnotactivated)
- [case deviceNotPaired](/documentation/watchconnectivity/wcerror/code/devicenotpaired)
- [case watchAppNotInstalled](/documentation/watchconnectivity/wcerror/code/watchappnotinstalled)
- [case notReachable](/documentation/watchconnectivity/wcerror/code/notreachable)
- [case invalidParameter](/documentation/watchconnectivity/wcerror/code/invalidparameter)
- [case payloadTooLarge](/documentation/watchconnectivity/wcerror/code/payloadtoolarge)
- [case payloadUnsupportedTypes](/documentation/watchconnectivity/wcerror/code/payloadunsupportedtypes)
- [case messageReplyFailed](/documentation/watchconnectivity/wcerror/code/messagereplyfailed)
- [case messageReplyTimedOut](/documentation/watchconnectivity/wcerror/code/messagereplytimedout)
- [case fileAccessDenied](/documentation/watchconnectivity/wcerror/code/fileaccessdenied)
- [case deliveryFailed](/documentation/watchconnectivity/wcerror/code/deliveryfailed)
- [case insufficientSpace](/documentation/watchconnectivity/wcerror/code/insufficientspace)
- [case sessionInactive](/documentation/watchconnectivity/wcerror/code/sessioninactive)
- [case transferTimedOut](/documentation/watchconnectivity/wcerror/code/transfertimedout)
- [case companionAppNotInstalled](/documentation/watchconnectivity/wcerror/code/companionappnotinstalled)
- [case watchOnlyApp](/documentation/watchconnectivity/wcerror/code/watchonlyapp)

#### Initializers

- [init?(rawValue: Int)](/documentation/watchconnectivity/wcerror/code/init(rawvalue:))
- [WCSessionDelegate](/documentation/watchconnectivity/wcsessiondelegate)

### Managing Session Activation

- [func session(WCSession, activationDidCompleteWith: WCSessionActivationState, error: (any Error)?)](/documentation/watchconnectivity/wcsessiondelegate/session(_:activationdidcompletewith:error:))
- [func sessionDidBecomeInactive(WCSession)](/documentation/watchconnectivity/wcsessiondelegate/sessiondidbecomeinactive(_:))
- [func sessionDidDeactivate(WCSession)](/documentation/watchconnectivity/wcsessiondelegate/sessiondiddeactivate(_:))

### Managing State Changes

- [func sessionWatchStateDidChange(WCSession)](/documentation/watchconnectivity/wcsessiondelegate/sessionwatchstatedidchange(_:))
- [func sessionReachabilityDidChange(WCSession)](/documentation/watchconnectivity/wcsessiondelegate/sessionreachabilitydidchange(_:))
- [func sessionCompanionAppInstalledDidChange(WCSession)](/documentation/watchconnectivity/wcsessiondelegate/sessioncompanionappinstalleddidchange(_:))

### Receiving Context Data

- [func session(WCSession, didReceiveApplicationContext: [String : Any])](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceiveapplicationcontext:))

### Receiving Immediate Messages

- [func session(WCSession, didReceiveMessage: [String : Any])](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceivemessage:))
- [func session(WCSession, didReceiveMessage: [String : Any], replyHandler: ([String : Any]) -> Void)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceivemessage:replyhandler:))
- [func session(WCSession, didReceiveMessageData: Data)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceivemessagedata:))
- [func session(WCSession, didReceiveMessageData: Data, replyHandler: (Data) -> Void)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceivemessagedata:replyhandler:))

### Managing Data Dictionary Transfers

- [func session(WCSession, didReceiveUserInfo: [String : Any])](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceiveuserinfo:))
- [func session(WCSession, didFinish: WCSessionUserInfoTransfer, error: (any Error)?)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didfinish:error:)-8627b)

### Managing File Transfers

- [func session(WCSession, didReceive: WCSessionFile)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didreceive:))
- [func session(WCSession, didFinish: WCSessionFileTransfer, error: (any Error)?)](/documentation/watchconnectivity/wcsessiondelegate/session(_:didfinish:error:)-6dtcu)

## Data Objects

- [WCSessionFile](/documentation/watchconnectivity/wcsessionfile)

### Getting the File Information

- [var fileURL: URL](/documentation/watchconnectivity/wcsessionfile/fileurl)
- [var metadata: [String : Any]?](/documentation/watchconnectivity/wcsessionfile/metadata)
- [WCSessionFileTransfer](/documentation/watchconnectivity/wcsessionfiletransfer)

### Getting the File Information

- [var file: WCSessionFile](/documentation/watchconnectivity/wcsessionfiletransfer/file)

### Managing the File Transfer

- [var isTransferring: Bool](/documentation/watchconnectivity/wcsessionfiletransfer/istransferring)
- [var progress: Progress](/documentation/watchconnectivity/wcsessionfiletransfer/progress)
- [func cancel()](/documentation/watchconnectivity/wcsessionfiletransfer/cancel())
- [WCSessionUserInfoTransfer](/documentation/watchconnectivity/wcsessionuserinfotransfer)

### Getting the Transfer Information

- [var isCurrentComplicationInfo: Bool](/documentation/watchconnectivity/wcsessionuserinfotransfer/iscurrentcomplicationinfo)
- [var userInfo: [String : Any]](/documentation/watchconnectivity/wcsessionuserinfotransfer/userinfo)

### Managing the Transfer Operation

- [var isTransferring: Bool](/documentation/watchconnectivity/wcsessionuserinfotransfer/istransferring)
- [func cancel()](/documentation/watchconnectivity/wcsessionuserinfotransfer/cancel())

## Sample Code

- [Transferring data with Watch Connectivity](/documentation/watchconnectivity/transferring-data-with-watch-connectivity)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
