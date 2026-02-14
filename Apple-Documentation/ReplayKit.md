# ReplayKit Documentation

Source: https://sosumi.ai/documentation/replaykit

---
title: ReplayKit
source: https://developer.apple.com/documentation/replaykit
timestamp: 2026-02-13T19:01:14.783Z
---

## Replay Sharing

- [Recording and Streaming Your macOS App](/documentation/replaykit/recording-and-streaming-your-macos-app)
- [RPScreenRecorder](/documentation/replaykit/rpscreenrecorder)

### Accessing the Shared Recorder

- [class func shared() -> RPScreenRecorder](/documentation/replaykit/rpscreenrecorder/shared())

### Inspecting a Screen Recorder

- [var isAvailable: Bool](/documentation/replaykit/rpscreenrecorder/isavailable)
- [var isRecording: Bool](/documentation/replaykit/rpscreenrecorder/isrecording)
- [var isMicrophoneEnabled: Bool](/documentation/replaykit/rpscreenrecorder/ismicrophoneenabled)
- [var isCameraEnabled: Bool](/documentation/replaykit/rpscreenrecorder/iscameraenabled)
- [var cameraPreviewView: UIView?](/documentation/replaykit/rpscreenrecorder/camerapreviewview)
- [var cameraPosition: RPCameraPosition](/documentation/replaykit/rpscreenrecorder/cameraposition)
- [RPCameraPosition](/documentation/replaykit/rpcameraposition)

#### Enumeration Cases

- [case back](/documentation/replaykit/rpcameraposition/back)
- [case front](/documentation/replaykit/rpcameraposition/front)

#### Initializers

- [init?(rawValue: Int)](/documentation/replaykit/rpcameraposition/init(rawvalue:))
- [var delegate: (any RPScreenRecorderDelegate)?](/documentation/replaykit/rpscreenrecorder/delegate)
- [RPScreenRecorderDelegate](/documentation/replaykit/rpscreenrecorderdelegate)

#### Responding to Recording Changes

- [func screenRecorder(RPScreenRecorder, didStopRecordingWith: RPPreviewViewController?, error: (any Error)?)](/documentation/replaykit/rpscreenrecorderdelegate/screenrecorder(_:didstoprecordingwith:error:))
- [func screenRecorderDidChangeAvailability(RPScreenRecorder)](/documentation/replaykit/rpscreenrecorderdelegate/screenrecorderdidchangeavailability(_:))
- [func screenRecorder(RPScreenRecorder, didStopRecordingWithError: any Error, previewViewController: RPPreviewViewController?)](/documentation/replaykit/rpscreenrecorderdelegate/screenrecorder(_:didstoprecordingwitherror:previewviewcontroller:))

### Controlling App Recording

- [func startRecording(handler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/startrecording(handler:))
- [func stopRecording(handler: ((RPPreviewViewController?, (any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/stoprecording(handler:))
- [func stopRecording(withOutput: URL, completionHandler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/stoprecording(withoutput:completionhandler:))
- [func startCapture(handler: ((CMSampleBuffer, RPSampleBufferType, (any Error)?) -> Void)?, completionHandler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/startcapture(handler:completionhandler:))
- [RPSampleBufferType](/documentation/replaykit/rpsamplebuffertype)

#### Sample Buffer Types

- [case audioApp](/documentation/replaykit/rpsamplebuffertype/audioapp)
- [case audioMic](/documentation/replaykit/rpsamplebuffertype/audiomic)
- [case video](/documentation/replaykit/rpsamplebuffertype/video)

#### Initializers

- [init?(rawValue: Int)](/documentation/replaykit/rpsamplebuffertype/init(rawvalue:))
- [func stopCapture(handler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/stopcapture(handler:))
- [func discardRecording(handler: () -> Void)](/documentation/replaykit/rpscreenrecorder/discardrecording(handler:))
- [func startRecording(withMicrophoneEnabled: Bool, handler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/startrecording(withmicrophoneenabled:handler:))

### Performing Clip Recording

- [func startClipBuffering(completionHandler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/startclipbuffering(completionhandler:))
- [func stopClipBuffering(completionHandler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/stopclipbuffering(completionhandler:))
- [func exportClip(to: URL, duration: TimeInterval, completionHandler: (((any Error)?) -> Void)?)](/documentation/replaykit/rpscreenrecorder/exportclip(to:duration:completionhandler:))
- [RPPreviewViewController](/documentation/replaykit/rppreviewviewcontroller)

### Displaying the Preview UI

- [var mode: RPPreviewViewControllerMode](/documentation/replaykit/rppreviewviewcontroller/mode)
- [RPPreviewViewControllerMode](/documentation/replaykit/rppreviewviewcontrollermode)

#### Constants

- [case preview](/documentation/replaykit/rppreviewviewcontrollermode/preview)
- [case share](/documentation/replaykit/rppreviewviewcontrollermode/share)

#### Initializers

- [init?(rawValue: Int)](/documentation/replaykit/rppreviewviewcontrollermode/init(rawvalue:))
- [var previewControllerDelegate: (any RPPreviewViewControllerDelegate)?](/documentation/replaykit/rppreviewviewcontroller/previewcontrollerdelegate)
- [RPPreviewViewControllerDelegate](/documentation/replaykit/rppreviewviewcontrollerdelegate)

#### Dismissing the View Controller

- [func previewControllerDidFinish(RPPreviewViewController)](/documentation/replaykit/rppreviewviewcontrollerdelegate/previewcontrollerdidfinish(_:))
- [func previewController(RPPreviewViewController, didFinishWithActivityTypes: Set<String>)](/documentation/replaykit/rppreviewviewcontrollerdelegate/previewcontroller(_:didfinishwithactivitytypes:))

## Media Clip Processing

- [RPBroadcastController](/documentation/replaykit/rpbroadcastcontroller)

### Controlling the Broadcast

- [var broadcastURL: URL](/documentation/replaykit/rpbroadcastcontroller/broadcasturl)
- [func startBroadcast(handler: ((any Error)?) -> Void)](/documentation/replaykit/rpbroadcastcontroller/startbroadcast(handler:))
- [func pauseBroadcast()](/documentation/replaykit/rpbroadcastcontroller/pausebroadcast())
- [func resumeBroadcast()](/documentation/replaykit/rpbroadcastcontroller/resumebroadcast())
- [func finishBroadcast(handler: ((any Error)?) -> Void)](/documentation/replaykit/rpbroadcastcontroller/finishbroadcast(handler:))
- [var serviceInfo: [String : any NSCoding & NSObjectProtocol]?](/documentation/replaykit/rpbroadcastcontroller/serviceinfo)

### Retrieving Information About the Broadcast

- [var broadcastExtensionBundleID: String?](/documentation/replaykit/rpbroadcastcontroller/broadcastextensionbundleid)
- [var isBroadcasting: Bool](/documentation/replaykit/rpbroadcastcontroller/isbroadcasting)
- [var isPaused: Bool](/documentation/replaykit/rpbroadcastcontroller/ispaused)

### Getting the Delegate

- [var delegate: (any RPBroadcastControllerDelegate)?](/documentation/replaykit/rpbroadcastcontroller/delegate)
- [RPBroadcastControllerDelegate](/documentation/replaykit/rpbroadcastcontrollerdelegate)

#### Finishing a Broadcast

- [func broadcastController(RPBroadcastController, didFinishWithError: (any Error)?)](/documentation/replaykit/rpbroadcastcontrollerdelegate/broadcastcontroller(_:didfinishwitherror:))

#### Updating a Broadcast

- [func broadcastController(RPBroadcastController, didUpdateServiceInfo: [String : any NSCoding & NSObjectProtocol])](/documentation/replaykit/rpbroadcastcontrollerdelegate/broadcastcontroller(_:didupdateserviceinfo:))
- [func broadcastController(RPBroadcastController, didUpdateBroadcast: URL)](/documentation/replaykit/rpbroadcastcontrollerdelegate/broadcastcontroller(_:didupdatebroadcast:))
- [RPBroadcastHandler](/documentation/replaykit/rpbroadcasthandler)

### Updating Current Broadcast Information

- [func updateServiceInfo([String : any NSCoding & NSObjectProtocol])](/documentation/replaykit/rpbroadcasthandler/updateserviceinfo(_:))
- [func updateBroadcast(URL)](/documentation/replaykit/rpbroadcasthandler/updatebroadcast(_:))
- [RPBroadcastSampleHandler](/documentation/replaykit/rpbroadcastsamplehandler)

### Handling Sample Buffer Clips

- [func broadcastStarted(withSetupInfo: [String : NSObject]?)](/documentation/replaykit/rpbroadcastsamplehandler/broadcaststarted(withsetupinfo:))
- [func broadcastPaused()](/documentation/replaykit/rpbroadcastsamplehandler/broadcastpaused())
- [func broadcastResumed()](/documentation/replaykit/rpbroadcastsamplehandler/broadcastresumed())
- [func broadcastFinished()](/documentation/replaykit/rpbroadcastsamplehandler/broadcastfinished())
- [func broadcastAnnotated(withApplicationInfo: [AnyHashable : Any])](/documentation/replaykit/rpbroadcastsamplehandler/broadcastannotated(withapplicationinfo:))
- [let RPApplicationInfoBundleIdentifierKey: String](/documentation/replaykit/rpapplicationinfobundleidentifierkey)
- [func processSampleBuffer(CMSampleBuffer, with: RPSampleBufferType)](/documentation/replaykit/rpbroadcastsamplehandler/processsamplebuffer(_:with:))
- [let RPVideoSampleOrientationKey: String](/documentation/replaykit/rpvideosampleorientationkey)
- [func finishBroadcastWithError(any Error)](/documentation/replaykit/rpbroadcastsamplehandler/finishbroadcastwitherror(_:))
- [RPBroadcastMP4ClipHandler](/documentation/replaykit/rpbroadcastmp4cliphandler)

### Processing MP4 Movie Clips

- [func finishedProcessingMP4Clip(withUpdatedBroadcastConfiguration: RPBroadcastConfiguration?, error: (any Error)?)](/documentation/replaykit/rpbroadcastmp4cliphandler/finishedprocessingmp4clip(withupdatedbroadcastconfiguration:error:))
- [func processMP4Clip(with: URL?, setupInfo: [String : NSObject]?, finished: Bool)](/documentation/replaykit/rpbroadcastmp4cliphandler/processmp4clip(with:setupinfo:finished:))

## Live Broadcast Implementation

- [RPBroadcastActivityViewController](/documentation/replaykit/rpbroadcastactivityviewcontroller)

### Presenting the Broadcast Activity UI

- [class func load(handler: (RPBroadcastActivityViewController?, (any Error)?) -> Void)](/documentation/replaykit/rpbroadcastactivityviewcontroller/load(handler:))
- [class func load(withPreferredExtension: String?, handler: (RPBroadcastActivityViewController?, (any Error)?) -> Void)](/documentation/replaykit/rpbroadcastactivityviewcontroller/load(withpreferredextension:handler:))

### Getting the Delegate

- [var delegate: (any RPBroadcastActivityViewControllerDelegate)?](/documentation/replaykit/rpbroadcastactivityviewcontroller/delegate)
- [RPBroadcastActivityViewControllerDelegate](/documentation/replaykit/rpbroadcastactivityviewcontrollerdelegate)

#### Connecting to a Service

- [func broadcastActivityViewController(RPBroadcastActivityViewController, didFinishWith: RPBroadcastController?, error: (any Error)?)](/documentation/replaykit/rpbroadcastactivityviewcontrollerdelegate/broadcastactivityviewcontroller(_:didfinishwith:error:))
- [RPSystemBroadcastPickerView](/documentation/replaykit/rpsystembroadcastpickerview)

### Configuring the Broadcast Picker

- [var preferredExtension: String?](/documentation/replaykit/rpsystembroadcastpickerview/preferredextension)
- [var showsMicrophoneButton: Bool](/documentation/replaykit/rpsystembroadcastpickerview/showsmicrophonebutton)
- [RPBroadcastActivityController](/documentation/replaykit/rpbroadcastactivitycontroller)

### Showing a Broadcast Picker

- [class func showBroadcastPicker(at: CGPoint, from: NSWindow?, preferredExtensionIdentifier: String?, completionHandler: (RPBroadcastActivityController?, (any Error)?) -> Void)](/documentation/replaykit/rpbroadcastactivitycontroller/showbroadcastpicker(at:from:preferredextensionidentifier:completionhandler:))

### Accessing the Delegate Object

- [var delegate: (any RPBroadcastActivityControllerDelegate)?](/documentation/replaykit/rpbroadcastactivitycontroller/delegate)
- [RPBroadcastActivityControllerDelegate](/documentation/replaykit/rpbroadcastactivitycontrollerdelegate)

### Responding to User Selection

- [func broadcastActivityController(RPBroadcastActivityController, didFinishWith: RPBroadcastController?, error: (any Error)?)](/documentation/replaykit/rpbroadcastactivitycontrollerdelegate/broadcastactivitycontroller(_:didfinishwith:error:))
- [RPBroadcastConfiguration](/documentation/replaykit/rpbroadcastconfiguration)

### Configuring Movie Clips

- [var clipDuration: TimeInterval](/documentation/replaykit/rpbroadcastconfiguration/clipduration)
- [var videoCompressionProperties: [String : any NSSecureCoding & NSObjectProtocol]?](/documentation/replaykit/rpbroadcastconfiguration/videocompressionproperties)

## Errors

- [RPRecordingErrorCode](/documentation/replaykit/rprecordingerrorcode)

### Errors

- [case activePhoneCall](/documentation/replaykit/rprecordingerrorcode/activephonecall)
- [case attemptToStartInRecordingState](/documentation/replaykit/rprecordingerrorcode/attempttostartinrecordingstate)
- [case attemptToStopNonRecording](/documentation/replaykit/rprecordingerrorcode/attempttostopnonrecording)
- [case broadcastInvalidSession](/documentation/replaykit/rprecordingerrorcode/broadcastinvalidsession)
- [case broadcastSetupFailed](/documentation/replaykit/rprecordingerrorcode/broadcastsetupfailed)
- [case carPlay](/documentation/replaykit/rprecordingerrorcode/carplay)
- [case codeSuccessful](/documentation/replaykit/rprecordingerrorcode/codesuccessful)
- [case contentResize](/documentation/replaykit/rprecordingerrorcode/contentresize)
- [case disabled](/documentation/replaykit/rprecordingerrorcode/disabled)
- [case entitlements](/documentation/replaykit/rprecordingerrorcode/entitlements)
- [case failed](/documentation/replaykit/rprecordingerrorcode/failed)
- [case failedApplicationConnectionInterrupted](/documentation/replaykit/rprecordingerrorcode/failedapplicationconnectioninterrupted)
- [case failedApplicationConnectionInvalid](/documentation/replaykit/rprecordingerrorcode/failedapplicationconnectioninvalid)
- [case failedAssetWriterExportCanceled](/documentation/replaykit/rprecordingerrorcode/failedassetwriterexportcanceled)
- [case failedAssetWriterExportFailed](/documentation/replaykit/rprecordingerrorcode/failedassetwriterexportfailed)
- [case failedAssetWriterFailedToSave](/documentation/replaykit/rprecordingerrorcode/failedassetwriterfailedtosave)
- [case failedAssetWriterInWrongState](/documentation/replaykit/rprecordingerrorcode/failedassetwriterinwrongstate)
- [case failedIncorrectTimeStamps](/documentation/replaykit/rprecordingerrorcode/failedincorrecttimestamps)
- [case failedMediaServicesFailure](/documentation/replaykit/rprecordingerrorcode/failedmediaservicesfailure)
- [case failedNoAssetWriter](/documentation/replaykit/rprecordingerrorcode/failednoassetwriter)
- [case failedNoMatchingApplicationContext](/documentation/replaykit/rprecordingerrorcode/failednomatchingapplicationcontext)
- [case failedToObtainURL](/documentation/replaykit/rprecordingerrorcode/failedtoobtainurl)
- [case failedToProcessFirstSample](/documentation/replaykit/rprecordingerrorcode/failedtoprocessfirstsample)
- [case failedToRemoveFile](/documentation/replaykit/rprecordingerrorcode/failedtoremovefile)
- [case failedToStartCaptureStack](/documentation/replaykit/rprecordingerrorcode/failedtostartcapturestack)
- [case failedToStart](/documentation/replaykit/rprecordingerrorcode/failedtostart)
- [case failedToSave](/documentation/replaykit/rprecordingerrorcode/failedtosave)
- [case filePermissions](/documentation/replaykit/rprecordingerrorcode/filepermissions)
- [case insufficientStorage](/documentation/replaykit/rprecordingerrorcode/insufficientstorage)
- [case interrupted](/documentation/replaykit/rprecordingerrorcode/interrupted)
- [case invalidParameter](/documentation/replaykit/rprecordingerrorcode/invalidparameter)
- [case photoFailure](/documentation/replaykit/rprecordingerrorcode/photofailure)
- [case recordingInvalidSession](/documentation/replaykit/rprecordingerrorcode/recordinginvalidsession)
- [case systemDormancy](/documentation/replaykit/rprecordingerrorcode/systemdormancy)
- [case unknown](/documentation/replaykit/rprecordingerrorcode/unknown)
- [case userDeclined](/documentation/replaykit/rprecordingerrorcode/userdeclined)
- [case videoMixingFailure](/documentation/replaykit/rprecordingerrorcode/videomixingfailure)

### Enumeration Cases

- [case exportClipToURLInProgress](/documentation/replaykit/rprecordingerrorcode/exportcliptourlinprogress)

### Initializers

- [init?(rawValue: Int)](/documentation/replaykit/rprecordingerrorcode/init(rawvalue:))
- [let RPRecordingErrorDomain: String](/documentation/replaykit/rprecordingerrordomain)
- [let SCStreamErrorDomain: String](/documentation/replaykit/scstreamerrordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
