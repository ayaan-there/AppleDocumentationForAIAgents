# ScreenCaptureKit Documentation

Source: https://sosumi.ai/documentation/screencapturekit

---
title: ScreenCaptureKit
source: https://developer.apple.com/documentation/screencapturekit
timestamp: 2026-02-13T19:01:41.497Z
---

## Essentials

- [ScreenCaptureKit updates](/documentation/updates/screencapturekit)
- [Persistent Content Capture](/documentation/bundleresources/entitlements/com.apple.developer.persistent-content-capture)
- [Capturing screen content in macOS](/documentation/screencapturekit/capturing-screen-content-in-macos)

## Shareable content

- [SCShareableContent](/documentation/screencapturekit/scshareablecontent)

### Retrieving shareable content

- [class func getWithCompletionHandler((SCShareableContent?, (any Error)?) -> Void)](/documentation/screencapturekit/scshareablecontent/getwithcompletionhandler(_:))
- [class func getExcludingDesktopWindows(Bool, onScreenWindowsOnly: Bool, completionHandler: (SCShareableContent?, (any Error)?) -> Void)](/documentation/screencapturekit/scshareablecontent/getexcludingdesktopwindows(_:onscreenwindowsonly:completionhandler:))
- [class func getExcludingDesktopWindows(Bool, onScreenWindowsOnlyAbove: SCWindow, completionHandler: (SCShareableContent?, (any Error)?) -> Void)](/documentation/screencapturekit/scshareablecontent/getexcludingdesktopwindows(_:onscreenwindowsonlyabove:completionhandler:))
- [class func getExcludingDesktopWindows(Bool, onScreenWindowsOnlyBelow: SCWindow, completionHandler: (SCShareableContent?, (any Error)?) -> Void)](/documentation/screencapturekit/scshareablecontent/getexcludingdesktopwindows(_:onscreenwindowsonlybelow:completionhandler:))
- [class func info(for: SCContentFilter) -> SCShareableContentInfo](/documentation/screencapturekit/scshareablecontent/info(for:))

### Inspecting shareable content

- [var windows: [SCWindow]](/documentation/screencapturekit/scshareablecontent/windows)
- [var displays: [SCDisplay]](/documentation/screencapturekit/scshareablecontent/displays)
- [var applications: [SCRunningApplication]](/documentation/screencapturekit/scshareablecontent/applications)

### Type Methods

- [class func getCurrentProcessShareableContent(completionHandler: (SCShareableContent?, (any Error)?) -> Void)](/documentation/screencapturekit/scshareablecontent/getcurrentprocessshareablecontent(completionhandler:))
- [SCShareableContentInfo](/documentation/screencapturekit/scshareablecontentinfo)

### Shared content properties

- [var contentRect: CGRect](/documentation/screencapturekit/scshareablecontentinfo/contentrect)
- [var pointPixelScale: Float](/documentation/screencapturekit/scshareablecontentinfo/pointpixelscale)
- [var style: SCShareableContentStyle](/documentation/screencapturekit/scshareablecontentinfo/style)
- [SCShareableContentStyle](/documentation/screencapturekit/scshareablecontentstyle)

### Content styles

- [case application](/documentation/screencapturekit/scshareablecontentstyle/application)
- [case display](/documentation/screencapturekit/scshareablecontentstyle/display)
- [case none](/documentation/screencapturekit/scshareablecontentstyle/none)
- [case window](/documentation/screencapturekit/scshareablecontentstyle/window)

### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scshareablecontentstyle/init(rawvalue:))
- [SCDisplay](/documentation/screencapturekit/scdisplay)

### Identifying displays

- [var displayID: CGDirectDisplayID](/documentation/screencapturekit/scdisplay/displayid)

### Accessing dimensions

- [var frame: CGRect](/documentation/screencapturekit/scdisplay/frame)
- [var width: Int](/documentation/screencapturekit/scdisplay/width)
- [var height: Int](/documentation/screencapturekit/scdisplay/height)
- [SCRunningApplication](/documentation/screencapturekit/scrunningapplication)

### Inspecting an app

- [var processID: pid_t](/documentation/screencapturekit/scrunningapplication/processid)
- [var bundleIdentifier: String](/documentation/screencapturekit/scrunningapplication/bundleidentifier)
- [var applicationName: String](/documentation/screencapturekit/scrunningapplication/applicationname)
- [SCWindow](/documentation/screencapturekit/scwindow)

### Identifying windows

- [var windowID: CGWindowID](/documentation/screencapturekit/scwindow/windowid)
- [var title: String?](/documentation/screencapturekit/scwindow/title)
- [var owningApplication: SCRunningApplication?](/documentation/screencapturekit/scwindow/owningapplication)
- [var windowLayer: Int](/documentation/screencapturekit/scwindow/windowlayer)

### Accessing dimensions

- [var frame: CGRect](/documentation/screencapturekit/scwindow/frame)

### Determining visibility

- [var isOnScreen: Bool](/documentation/screencapturekit/scwindow/isonscreen)
- [var isActive: Bool](/documentation/screencapturekit/scwindow/isactive)

## Content capture

- [SCStream](/documentation/screencapturekit/scstream)

### Creating a stream

- [init(filter: SCContentFilter, configuration: SCStreamConfiguration, delegate: (any SCStreamDelegate)?)](/documentation/screencapturekit/scstream/init(filter:configuration:delegate:))

### Updating stream configuration

- [func updateConfiguration(SCStreamConfiguration, completionHandler: (((any Error)?) -> Void)?)](/documentation/screencapturekit/scstream/updateconfiguration(_:completionhandler:))
- [func updateContentFilter(SCContentFilter, completionHandler: (((any Error)?) -> Void)?)](/documentation/screencapturekit/scstream/updatecontentfilter(_:completionhandler:))

### Adding and removing stream output

- [func addStreamOutput(any SCStreamOutput, type: SCStreamOutputType, sampleHandlerQueue: dispatch_queue_t?) throws](/documentation/screencapturekit/scstream/addstreamoutput(_:type:samplehandlerqueue:))
- [func removeStreamOutput(any SCStreamOutput, type: SCStreamOutputType) throws](/documentation/screencapturekit/scstream/removestreamoutput(_:type:))

### Adding and removing recording output

- [func addRecordingOutput(SCRecordingOutput) throws](/documentation/screencapturekit/scstream/addrecordingoutput(_:))
- [func removeRecordingOutput(SCRecordingOutput) throws](/documentation/screencapturekit/scstream/removerecordingoutput(_:))
- [SCRecordingOutput](/documentation/screencapturekit/screcordingoutput)

#### Creating a recording output

- [init(configuration: SCRecordingOutputConfiguration, delegate: any SCRecordingOutputDelegate)](/documentation/screencapturekit/screcordingoutput/init(configuration:delegate:))
- [SCRecordingOutputConfiguration](/documentation/screencapturekit/screcordingoutputconfiguration)

##### Instance Properties

- [var availableOutputFileTypes: [AVFileType]](/documentation/screencapturekit/screcordingoutputconfiguration/availableoutputfiletypes)
- [var availableVideoCodecTypes: [AVVideoCodecType]](/documentation/screencapturekit/screcordingoutputconfiguration/availablevideocodectypes)
- [var outputFileType: AVFileType](/documentation/screencapturekit/screcordingoutputconfiguration/outputfiletype)
- [var outputURL: URL](/documentation/screencapturekit/screcordingoutputconfiguration/outputurl)
- [var videoCodecType: AVVideoCodecType](/documentation/screencapturekit/screcordingoutputconfiguration/videocodectype)
- [SCRecordingOutputDelegate](/documentation/screencapturekit/screcordingoutputdelegate)

##### Instance Methods

- [func recordingOutput(SCRecordingOutput, didFailWithError: any Error)](/documentation/screencapturekit/screcordingoutputdelegate/recordingoutput(_:didfailwitherror:))
- [func recordingOutputDidFinishRecording(SCRecordingOutput)](/documentation/screencapturekit/screcordingoutputdelegate/recordingoutputdidfinishrecording(_:))
- [func recordingOutputDidStartRecording(SCRecordingOutput)](/documentation/screencapturekit/screcordingoutputdelegate/recordingoutputdidstartrecording(_:))

#### Configuring the recording output

- [var recordedDuration: CMTime](/documentation/screencapturekit/screcordingoutput/recordedduration)
- [var recordedFileSize: Int](/documentation/screencapturekit/screcordingoutput/recordedfilesize)

### Starting and stopping a stream

- [func startCapture(completionHandler: (((any Error)?) -> Void)?)](/documentation/screencapturekit/scstream/startcapture(completionhandler:))
- [func stopCapture(completionHandler: (((any Error)?) -> Void)?)](/documentation/screencapturekit/scstream/stopcapture(completionhandler:))

### Stream synchronization

- [var synchronizationClock: CMClock?](/documentation/screencapturekit/scstream/synchronizationclock)
- [SCStreamConfiguration](/documentation/screencapturekit/scstreamconfiguration)

### Specifying dimensions

- [var width: Int](/documentation/screencapturekit/scstreamconfiguration/width)
- [var height: Int](/documentation/screencapturekit/scstreamconfiguration/height)
- [var scalesToFit: Bool](/documentation/screencapturekit/scstreamconfiguration/scalestofit)
- [var sourceRect: CGRect](/documentation/screencapturekit/scstreamconfiguration/sourcerect)
- [var destinationRect: CGRect](/documentation/screencapturekit/scstreamconfiguration/destinationrect)
- [var preservesAspectRatio: Bool](/documentation/screencapturekit/scstreamconfiguration/preservesaspectratio)

### Configuring colors

- [var pixelFormat: OSType](/documentation/screencapturekit/scstreamconfiguration/pixelformat)
- [var colorMatrix: CFString](/documentation/screencapturekit/scstreamconfiguration/colormatrix)
- [var colorSpaceName: CFString](/documentation/screencapturekit/scstreamconfiguration/colorspacename)
- [var backgroundColor: CGColor](/documentation/screencapturekit/scstreamconfiguration/backgroundcolor)

### Configuring captured elements

- [var showsCursor: Bool](/documentation/screencapturekit/scstreamconfiguration/showscursor)
- [var shouldBeOpaque: Bool](/documentation/screencapturekit/scstreamconfiguration/shouldbeopaque)
- [var capturesShadowsOnly: Bool](/documentation/screencapturekit/scstreamconfiguration/capturesshadowsonly)
- [var ignoreShadowsDisplay: Bool](/documentation/screencapturekit/scstreamconfiguration/ignoreshadowsdisplay)
- [var ignoreShadowsSingleWindow: Bool](/documentation/screencapturekit/scstreamconfiguration/ignoreshadowssinglewindow)
- [var ignoreGlobalClipDisplay: Bool](/documentation/screencapturekit/scstreamconfiguration/ignoreglobalclipdisplay)
- [var ignoreGlobalClipSingleWindow: Bool](/documentation/screencapturekit/scstreamconfiguration/ignoreglobalclipsinglewindow)

### Configuring captured frames

- [var queueDepth: Int](/documentation/screencapturekit/scstreamconfiguration/queuedepth)
- [var minimumFrameInterval: CMTime](/documentation/screencapturekit/scstreamconfiguration/minimumframeinterval)
- [var captureResolution: SCCaptureResolutionType](/documentation/screencapturekit/scstreamconfiguration/captureresolution)
- [SCCaptureResolutionType](/documentation/screencapturekit/sccaptureresolutiontype)

#### Resolutions

- [case automatic](/documentation/screencapturekit/sccaptureresolutiontype/automatic)
- [case best](/documentation/screencapturekit/sccaptureresolutiontype/best)
- [case nominal](/documentation/screencapturekit/sccaptureresolutiontype/nominal)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/sccaptureresolutiontype/init(rawvalue:))

### Configuring audio

- [var capturesAudio: Bool](/documentation/screencapturekit/scstreamconfiguration/capturesaudio)
- [var sampleRate: Int](/documentation/screencapturekit/scstreamconfiguration/samplerate)
- [var channelCount: Int](/documentation/screencapturekit/scstreamconfiguration/channelcount)
- [var excludesCurrentProcessAudio: Bool](/documentation/screencapturekit/scstreamconfiguration/excludescurrentprocessaudio)

### Identifying a stream

- [var streamName: String?](/documentation/screencapturekit/scstreamconfiguration/streamname)

### Notifying presenters

- [var presenterOverlayPrivacyAlertSetting: SCPresenterOverlayAlertSetting](/documentation/screencapturekit/scstreamconfiguration/presenteroverlayprivacyalertsetting)
- [SCPresenterOverlayAlertSetting](/documentation/screencapturekit/scpresenteroverlayalertsetting)

#### Alerting Presenters

- [case always](/documentation/screencapturekit/scpresenteroverlayalertsetting/always)
- [case never](/documentation/screencapturekit/scpresenteroverlayalertsetting/never)
- [case system](/documentation/screencapturekit/scpresenteroverlayalertsetting/system)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scpresenteroverlayalertsetting/init(rawvalue:))

### Enumerations

- [SCCaptureDynamicRange](/documentation/screencapturekit/sccapturedynamicrange)

#### Enumeration Cases

- [case SDR](/documentation/screencapturekit/sccapturedynamicrange/sdr)
- [case hdrCanonicalDisplay](/documentation/screencapturekit/sccapturedynamicrange/hdrcanonicaldisplay)
- [case hdrLocalDisplay](/documentation/screencapturekit/sccapturedynamicrange/hdrlocaldisplay)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/sccapturedynamicrange/init(rawvalue:))
- [SCStreamConfiguration.Preset](/documentation/screencapturekit/scstreamconfiguration/preset)

#### Enumeration Cases

- [case captureHDRRecordingPreservedSDRHDR10](/documentation/screencapturekit/scstreamconfiguration/preset/capturehdrrecordingpreservedsdrhdr10)
- [case captureHDRScreenshotCanonicalDisplay](/documentation/screencapturekit/scstreamconfiguration/preset/capturehdrscreenshotcanonicaldisplay)
- [case captureHDRScreenshotLocalDisplay](/documentation/screencapturekit/scstreamconfiguration/preset/capturehdrscreenshotlocaldisplay)
- [case captureHDRStreamCanonicalDisplay](/documentation/screencapturekit/scstreamconfiguration/preset/capturehdrstreamcanonicaldisplay)
- [case captureHDRStreamLocalDisplay](/documentation/screencapturekit/scstreamconfiguration/preset/capturehdrstreamlocaldisplay)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scstreamconfiguration/preset/init(rawvalue:))

### Initializers

- [convenience init(preset: SCStreamConfiguration.Preset)](/documentation/screencapturekit/scstreamconfiguration/init(preset:))

### Instance Properties

- [var captureDynamicRange: SCCaptureDynamicRange](/documentation/screencapturekit/scstreamconfiguration/capturedynamicrange)
- [var captureMicrophone: Bool](/documentation/screencapturekit/scstreamconfiguration/capturemicrophone)
- [var includeChildWindows: Bool](/documentation/screencapturekit/scstreamconfiguration/includechildwindows)
- [var microphoneCaptureDeviceID: String?](/documentation/screencapturekit/scstreamconfiguration/microphonecapturedeviceid)
- [var showMouseClicks: Bool](/documentation/screencapturekit/scstreamconfiguration/showmouseclicks)
- [SCContentFilter](/documentation/screencapturekit/sccontentfilter)

### Creating a filter

- [init(desktopIndependentWindow: SCWindow)](/documentation/screencapturekit/sccontentfilter/init(desktopindependentwindow:))
- [init(display: SCDisplay, including: [SCWindow])](/documentation/screencapturekit/sccontentfilter/init(display:including:))
- [init(display: SCDisplay, excludingWindows: [SCWindow])](/documentation/screencapturekit/sccontentfilter/init(display:excludingwindows:))
- [init(display: SCDisplay, including: [SCRunningApplication], exceptingWindows: [SCWindow])](/documentation/screencapturekit/sccontentfilter/init(display:including:exceptingwindows:))
- [init(display: SCDisplay, excludingApplications: [SCRunningApplication], exceptingWindows: [SCWindow])](/documentation/screencapturekit/sccontentfilter/init(display:excludingapplications:exceptingwindows:))

### Filter properties

- [var contentRect: CGRect](/documentation/screencapturekit/sccontentfilter/contentrect)
- [var pointPixelScale: Float](/documentation/screencapturekit/sccontentfilter/pointpixelscale)
- [var streamType: SCStreamType](/documentation/screencapturekit/sccontentfilter/streamtype)
- [SCStreamType](/documentation/screencapturekit/scstreamtype)

#### Client presentation

- [case display](/documentation/screencapturekit/scstreamtype/display)
- [case window](/documentation/screencapturekit/scstreamtype/window)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scstreamtype/init(rawvalue:))
- [var style: SCShareableContentStyle](/documentation/screencapturekit/sccontentfilter/style)

### Instance Properties

- [var includeMenuBar: Bool](/documentation/screencapturekit/sccontentfilter/includemenubar)
- [var includedApplications: [SCRunningApplication]](/documentation/screencapturekit/sccontentfilter/includedapplications)
- [var includedDisplays: [SCDisplay]](/documentation/screencapturekit/sccontentfilter/includeddisplays)
- [var includedWindows: [SCWindow]](/documentation/screencapturekit/sccontentfilter/includedwindows)
- [SCStreamDelegate](/documentation/screencapturekit/scstreamdelegate)

### Responding to Presenter Overlay

- [func outputVideoEffectDidStart(for: SCStream)](/documentation/screencapturekit/scstreamdelegate/outputvideoeffectdidstart(for:))
- [func outputVideoEffectDidStop(for: SCStream)](/documentation/screencapturekit/scstreamdelegate/outputvideoeffectdidstop(for:))

### Responding to stream stoppage

- [func stream(SCStream, didStopWithError: any Error)](/documentation/screencapturekit/scstreamdelegate/stream(_:didstopwitherror:))

### Instance Methods

- [func streamDidBecomeActive(SCStream)](/documentation/screencapturekit/scstreamdelegate/streamdidbecomeactive(_:))
- [func streamDidBecomeInactive(SCStream)](/documentation/screencapturekit/scstreamdelegate/streamdidbecomeinactive(_:))
- [SCScreenshotManager](/documentation/screencapturekit/scscreenshotmanager)

### Individual frame capture

- [class func captureImage(contentFilter: SCContentFilter, configuration: SCStreamConfiguration, completionHandler: ((CGImage?, (any Error)?) -> Void)?)](/documentation/screencapturekit/scscreenshotmanager/captureimage(contentfilter:configuration:completionhandler:))
- [class func captureSampleBuffer(contentFilter: SCContentFilter, configuration: SCStreamConfiguration, completionHandler: ((CMSampleBuffer?, (any Error)?) -> Void)?)](/documentation/screencapturekit/scscreenshotmanager/capturesamplebuffer(contentfilter:configuration:completionhandler:))

### Type Methods

- [class func captureImage(in: CGRect, completionHandler: ((CGImage?, (any Error)?) -> Void)?)](/documentation/screencapturekit/scscreenshotmanager/captureimage(in:completionhandler:))
- [class func captureScreenshot(contentFilter: SCContentFilter, configuration: SCScreenshotConfiguration, completionHandler: ((SCScreenshotOutput?, (any Error)?) -> Void)?)](/documentation/screencapturekit/scscreenshotmanager/capturescreenshot(contentfilter:configuration:completionhandler:))
- [class func captureScreenshot(rect: CGRect, configuration: SCScreenshotConfiguration, completionHandler: ((SCScreenshotOutput?, (any Error)?) -> Void)?)](/documentation/screencapturekit/scscreenshotmanager/capturescreenshot(rect:configuration:completionhandler:))
- [SCScreenshotConfiguration](/documentation/screencapturekit/scscreenshotconfiguration)

### Instance Properties

- [var contentType: UTTypeReference](/documentation/screencapturekit/scscreenshotconfiguration/contenttype)
- [var destinationRect: CGRect](/documentation/screencapturekit/scscreenshotconfiguration/destinationrect)
- [var displayIntent: SCScreenshotConfiguration.DisplayIntent](/documentation/screencapturekit/scscreenshotconfiguration/displayintent-swift.property)
- [var dynamicRange: SCScreenshotConfiguration.DynamicRange](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.property)
- [var fileURL: URL?](/documentation/screencapturekit/scscreenshotconfiguration/fileurl)
- [var height: Int](/documentation/screencapturekit/scscreenshotconfiguration/height)
- [var ignoreClipping: Bool](/documentation/screencapturekit/scscreenshotconfiguration/ignoreclipping)
- [var ignoreShadows: Bool](/documentation/screencapturekit/scscreenshotconfiguration/ignoreshadows)
- [var includeChildWindows: Bool](/documentation/screencapturekit/scscreenshotconfiguration/includechildwindows)
- [var showsCursor: Bool](/documentation/screencapturekit/scscreenshotconfiguration/showscursor)
- [var sourceRect: CGRect](/documentation/screencapturekit/scscreenshotconfiguration/sourcerect)
- [var width: Int](/documentation/screencapturekit/scscreenshotconfiguration/width)

### Type Properties

- [class var supportedContentTypes: [UTType]](/documentation/screencapturekit/scscreenshotconfiguration/supportedcontenttypes)

### Enumerations

- [SCScreenshotConfiguration.DisplayIntent](/documentation/screencapturekit/scscreenshotconfiguration/displayintent-swift.enum)

#### Enumeration Cases

- [case canonical](/documentation/screencapturekit/scscreenshotconfiguration/displayintent-swift.enum/canonical)
- [case local](/documentation/screencapturekit/scscreenshotconfiguration/displayintent-swift.enum/local)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scscreenshotconfiguration/displayintent-swift.enum/init(rawvalue:))
- [SCScreenshotConfiguration.DynamicRange](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.enum)

#### Enumeration Cases

- [case bothSDRAndHDR](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.enum/bothsdrandhdr)
- [case hdr](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.enum/hdr)
- [case sdr](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.enum/sdr)

#### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scscreenshotconfiguration/dynamicrange-swift.enum/init(rawvalue:))
- [SCScreenshotOutput](/documentation/screencapturekit/scscreenshotoutput)

### Instance Properties

- [var fileURL: NSURL?](/documentation/screencapturekit/scscreenshotoutput/fileurl)
- [var hdrImage: CGImage?](/documentation/screencapturekit/scscreenshotoutput/hdrimage)
- [var sdrImage: CGImage?](/documentation/screencapturekit/scscreenshotoutput/sdrimage)

## Output processing

- [SCStreamOutput](/documentation/screencapturekit/scstreamoutput)

### Receiving stream output

- [func stream(SCStream, didOutputSampleBuffer: CMSampleBuffer, of: SCStreamOutputType)](/documentation/screencapturekit/scstreamoutput/stream(_:didoutputsamplebuffer:of:))
- [SCStreamOutputType](/documentation/screencapturekit/scstreamoutputtype)

### Output types

- [case screen](/documentation/screencapturekit/scstreamoutputtype/screen)
- [case audio](/documentation/screencapturekit/scstreamoutputtype/audio)

### Enumeration Cases

- [case microphone](/documentation/screencapturekit/scstreamoutputtype/microphone)

### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scstreamoutputtype/init(rawvalue:))
- [SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo)

### Frame information constants

- [static let status: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/status)
- [static let displayTime: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/displaytime)
- [static let scaleFactor: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/scalefactor)
- [static let contentScale: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/contentscale)
- [static let contentRect: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/contentrect)
- [static let boundingRect: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/boundingrect)
- [static let screenRect: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/screenrect)
- [static let dirtyRects: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/dirtyrects)
- [static let presenterOverlayContentRect: SCStreamFrameInfo](/documentation/screencapturekit/scstreamframeinfo/presenteroverlaycontentrect)

### Initializers

- [init(rawValue: String)](/documentation/screencapturekit/scstreamframeinfo/init(rawvalue:))
- [SCFrameStatus](/documentation/screencapturekit/scframestatus)

### Status values

- [case complete](/documentation/screencapturekit/scframestatus/complete)
- [case idle](/documentation/screencapturekit/scframestatus/idle)
- [case blank](/documentation/screencapturekit/scframestatus/blank)
- [case started](/documentation/screencapturekit/scframestatus/started)
- [case suspended](/documentation/screencapturekit/scframestatus/suspended)
- [case stopped](/documentation/screencapturekit/scframestatus/stopped)

### Initializers

- [init?(rawValue: Int)](/documentation/screencapturekit/scframestatus/init(rawvalue:))

## System content-sharing picker

- [SCContentSharingPicker](/documentation/screencapturekit/sccontentsharingpicker)

### Shared system picker

- [class var shared: SCContentSharingPicker](/documentation/screencapturekit/sccontentsharingpicker/shared)

### Picker availability

- [var isActive: Bool](/documentation/screencapturekit/sccontentsharingpicker/isactive)

### Stream configuration

- [func setConfiguration(SCContentSharingPickerConfiguration?, for: SCStream)](/documentation/screencapturekit/sccontentsharingpicker/setconfiguration(_:for:))
- [var configuration: SCContentSharingPickerConfiguration?](/documentation/screencapturekit/sccontentsharingpicker/configuration)
- [var defaultConfiguration: SCContentSharingPickerConfiguration](/documentation/screencapturekit/sccontentsharingpicker/defaultconfiguration-94q2b)
- [var maximumStreamCount: Int?](/documentation/screencapturekit/sccontentsharingpicker/maximumstreamcount-2kuaa)

### Manage observers

- [func add(any SCContentSharingPickerObserver)](/documentation/screencapturekit/sccontentsharingpicker/add(_:))
- [func remove(any SCContentSharingPickerObserver)](/documentation/screencapturekit/sccontentsharingpicker/remove(_:))

### Picker display

- [func present()](/documentation/screencapturekit/sccontentsharingpicker/present())
- [func present(for: SCStream)](/documentation/screencapturekit/sccontentsharingpicker/present(for:))
- [func present(using: SCShareableContentStyle)](/documentation/screencapturekit/sccontentsharingpicker/present(using:))
- [func present(for: SCStream, using: SCShareableContentStyle)](/documentation/screencapturekit/sccontentsharingpicker/present(for:using:))
- [SCContentSharingPickerConfiguration](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct)

### Initializers

- [init()](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct/init())

### Control streaming selections

- [var allowedPickerModes: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct/allowedpickermodes)
- [var allowsChangingSelectedContent: Bool](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct/allowschangingselectedcontent)
- [var excludedBundleIDs: Array<String>](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct/excludedbundleids)
- [var excludedWindowIDs: Array<Int>](/documentation/screencapturekit/sccontentsharingpickerconfiguration-swift.struct/excludedwindowids)
- [SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode)

### Initializers

- [init(rawValue: UInt)](/documentation/screencapturekit/sccontentsharingpickermode/init(rawvalue:))

### Picker selection modes

- [static var multipleApplications: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode/multipleapplications)
- [static var multipleWindows: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode/multiplewindows)
- [static var singleApplication: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode/singleapplication)
- [static var singleDisplay: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode/singledisplay)
- [static var singleWindow: SCContentSharingPickerMode](/documentation/screencapturekit/sccontentsharingpickermode/singlewindow)
- [SCContentSharingPickerObserver](/documentation/screencapturekit/sccontentsharingpickerobserver)

### Observing events

- [func contentSharingPicker(SCContentSharingPicker, didCancelFor: SCStream?)](/documentation/screencapturekit/sccontentsharingpickerobserver/contentsharingpicker(_:didcancelfor:))
- [func contentSharingPicker(SCContentSharingPicker, didUpdateWith: SCContentFilter, for: SCStream?)](/documentation/screencapturekit/sccontentsharingpickerobserver/contentsharingpicker(_:didupdatewith:for:))

### Observing errors

- [func contentSharingPickerStartDidFailWithError(any Error)](/documentation/screencapturekit/sccontentsharingpickerobserver/contentsharingpickerstartdidfailwitherror(_:))

## Stream errors

- [let SCStreamErrorDomain: String](/documentation/screencapturekit/scstreamerrordomain)
- [SCStreamError](/documentation/screencapturekit/scstreamerror)

### Error inspection

- [Error Constants](/documentation/screencapturekit/error-constants)

#### User cancellation

- [static var userStopped: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/userstopped)

#### Privacy and entitlements

- [static var userDeclined: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/userdeclined)
- [static var missingEntitlements: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/missingentitlements)

#### Stream management

- [static var attemptToStartStreamState: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/attempttostartstreamstate)
- [static var attemptToStopStreamState: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/attempttostopstreamstate)
- [static var attemptToUpdateFilterState: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/attempttoupdatefilterstate)
- [static var attemptToConfigState: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/attempttoconfigstate)
- [static var failedToStart: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedtostart)
- [static var failedToStartAudioCapture: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedtostartaudiocapture)
- [static var failedToStopAudioCapture: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedtostopaudiocapture)
- [static var failedToStartMicrophoneCapture: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedtostartmicrophonecapture)
- [static var systemStoppedStream: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/systemstoppedstream)
- [static var internalError: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/internalerror)
- [static var removingStream: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/removingstream)

#### Shareable content

- [static var noCaptureSource: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/nocapturesource)
- [static var noDisplayList: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/nodisplaylist)
- [static var noWindowList: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/nowindowlist)
- [static var failedApplicationConnectionInvalid: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedapplicationconnectioninvalid)
- [static var failedApplicationConnectionInterrupted: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failedapplicationconnectioninterrupted)
- [static var failedNoMatchingApplicationContext: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/failednomatchingapplicationcontext)

#### Invalid parameters

- [static var invalidParameter: SCStreamError.Code](/documentation/screencapturekit/scstreamerror/invalidparameter)
- [SCStreamError.Code](/documentation/screencapturekit/scstreamerror/code)

#### User cancellation

- [case userStopped](/documentation/screencapturekit/scstreamerror/code/userstopped)

#### Privacy and entitlements

- [case userDeclined](/documentation/screencapturekit/scstreamerror/code/userdeclined)
- [case missingEntitlements](/documentation/screencapturekit/scstreamerror/code/missingentitlements)

#### Stream management

- [case attemptToStartStreamState](/documentation/screencapturekit/scstreamerror/code/attempttostartstreamstate)
- [case attemptToStopStreamState](/documentation/screencapturekit/scstreamerror/code/attempttostopstreamstate)
- [case attemptToUpdateFilterState](/documentation/screencapturekit/scstreamerror/code/attempttoupdatefilterstate)
- [case attemptToConfigState](/documentation/screencapturekit/scstreamerror/code/attempttoconfigstate)
- [case failedToStart](/documentation/screencapturekit/scstreamerror/code/failedtostart)
- [case removingStream](/documentation/screencapturekit/scstreamerror/code/removingstream)
- [case failedToStartAudioCapture](/documentation/screencapturekit/scstreamerror/code/failedtostartaudiocapture)
- [case failedToStopAudioCapture](/documentation/screencapturekit/scstreamerror/code/failedtostopaudiocapture)
- [case failedToStartMicrophoneCapture](/documentation/screencapturekit/scstreamerror/code/failedtostartmicrophonecapture)
- [case systemStoppedStream](/documentation/screencapturekit/scstreamerror/code/systemstoppedstream)
- [case internalError](/documentation/screencapturekit/scstreamerror/code/internalerror)

#### Shareable content

- [case noCaptureSource](/documentation/screencapturekit/scstreamerror/code/nocapturesource)
- [case noDisplayList](/documentation/screencapturekit/scstreamerror/code/nodisplaylist)
- [case noWindowList](/documentation/screencapturekit/scstreamerror/code/nowindowlist)
- [case failedApplicationConnectionInvalid](/documentation/screencapturekit/scstreamerror/code/failedapplicationconnectioninvalid)
- [case failedApplicationConnectionInterrupted](/documentation/screencapturekit/scstreamerror/code/failedapplicationconnectioninterrupted)
- [case failedNoMatchingApplicationContext](/documentation/screencapturekit/scstreamerror/code/failednomatchingapplicationcontext)

#### Invalid parameters

- [case invalidParameter](/documentation/screencapturekit/scstreamerror/code/invalidparameter)

#### Creating an error

- [init?(rawValue: Int)](/documentation/screencapturekit/scstreamerror/code/init(rawvalue:))
- [static var errorDomain: String](/documentation/screencapturekit/scstreamerror/errordomain)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
