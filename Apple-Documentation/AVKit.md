# AVKit Documentation

Source: https://sosumi.ai/documentation/avkit

---
title: AVKit
source: https://developer.apple.com/documentation/avkit
timestamp: 2026-02-13T19:22:57.245Z
---

## iOS playback and capture

- [Playing video content in a standard user interface](/documentation/avkit/playing-video-content-in-a-standard-user-interface)
- [AVPlayerViewController](/documentation/avkit/avplayerviewcontroller)

### Configuring presentation

- [var showsPlaybackControls: Bool](/documentation/avkit/avplayerviewcontroller/showsplaybackcontrols)
- [var contentOverlayView: UIView?](/documentation/avkit/avplayerviewcontroller/contentoverlayview)
- [var videoGravity: AVLayerVideoGravity](/documentation/avkit/avplayerviewcontroller/videogravity)
- [var videoBounds: CGRect](/documentation/avkit/avplayerviewcontroller/videobounds)
- [var showsTimecodes: Bool](/documentation/avkit/avplayerviewcontroller/showstimecodes)
- [var appliesPreferredDisplayCriteriaAutomatically: Bool](/documentation/avkit/avplayerviewcontroller/appliespreferreddisplaycriteriaautomatically)

### Customizing the tvOS player UI

- [var playbackControlsIncludeTransportBar: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludetransportbar)
- [var playbackControlsIncludeInfoViews: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludeinfoviews)
- [var transportBarIncludesTitleView: Bool](/documentation/avkit/avplayerviewcontroller/transportbarincludestitleview)
- [var transportBarCustomMenuItems: [UIMenuElement]](/documentation/avkit/avplayerviewcontroller/transportbarcustommenuitems)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var customOverlayViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/customoverlayviewcontroller)
- [var unobscuredContentGuide: UILayoutGuide](/documentation/avkit/avplayerviewcontroller/unobscuredcontentguide)
- [var customInfoViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/custominfoviewcontroller)

### Configuring the visionOS player UI

- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var contextualActionsInfoView: UIView](/documentation/avkit/avplayerviewcontroller/contextualactionsinfoview)
- [var contextualActionsPreviewImage: UIImage?](/documentation/avkit/avplayerviewcontroller/contextualactionspreviewimage)
- [var requiresMonoscopicViewingMode: Bool](/documentation/avkit/avplayerviewcontroller/requiresmonoscopicviewingmode)
- [var experienceController: AVExperienceController](/documentation/avkit/avplayerviewcontroller/experiencecontroller)
- [var groupExperienceCoordinator: AVGroupExperienceCoordinator](/documentation/avkit/avplayerviewcontroller/groupexperiencecoordinator)

### Presenting the visionOS trimming UI

- [var canBeginTrimming: Bool](/documentation/avkit/avplayerviewcontroller/canbegintrimming)
- [func beginTrimming(completionHandler: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontroller/begintrimming(completionhandler:))

### Configuring frame analysis

- [var allowsVideoFrameAnalysis: Bool](/documentation/avkit/avplayerviewcontroller/allowsvideoframeanalysis)
- [var toggleLookupAction: UIAction](/documentation/avkit/avplayerviewcontroller/togglelookupaction)
- [var videoFrameAnalysisTypes: AVVideoFrameAnalysisType](/documentation/avkit/avplayerviewcontroller/videoframeanalysistypes)
- [AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype)

#### Analysis types

- [static var `default`: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/default)
- [static var text: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/text)
- [static var subject: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/subject)
- [static var visualSearch: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/visualsearch)
- [static var machineReadableCode: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/machinereadablecode)

#### Initializers

- [init(rawValue: UInt)](/documentation/avkit/avvideoframeanalysistype/init(rawvalue:))

### Configuring playback speed

- [var speeds: [AVPlaybackSpeed]](/documentation/avkit/avplayerviewcontroller/speeds)
- [var selectedSpeed: AVPlaybackSpeed?](/documentation/avkit/avplayerviewcontroller/selectedspeed)
- [func selectSpeed(AVPlaybackSpeed)](/documentation/avkit/avplayerviewcontroller/selectspeed(_:))
- [AVPlaybackSpeed](/documentation/avkit/avplaybackspeed)

#### Retrieving Default Speeds

- [class var systemDefaultSpeeds: [AVPlaybackSpeed]](/documentation/avkit/avplaybackspeed/systemdefaultspeeds)

#### Creating a Playback Speed

- [init(rate: Float, localizedName: String)](/documentation/avkit/avplaybackspeed/init(rate:localizedname:))

#### Inspecting Speed Details

- [var rate: Float](/documentation/avkit/avplaybackspeed/rate)
- [var localizedName: String](/documentation/avkit/avplaybackspeed/localizedname)
- [var localizedNumericName: String](/documentation/avkit/avplaybackspeed/localizednumericname)

### Configuring Picture in Picture

- [var allowsPictureInPicturePlayback: Bool](/documentation/avkit/avplayerviewcontroller/allowspictureinpictureplayback)
- [var canStartPictureInPictureAutomaticallyFromInline: Bool](/documentation/avkit/avplayerviewcontroller/canstartpictureinpictureautomaticallyfrominline)

### Managing full-screen behavior

- [var entersFullScreenWhenPlaybackBegins: Bool](/documentation/avkit/avplayerviewcontroller/entersfullscreenwhenplaybackbegins)
- [var exitsFullScreenWhenPlaybackEnds: Bool](/documentation/avkit/avplayerviewcontroller/exitsfullscreenwhenplaybackends)

### Managing subtitles

- [var allowedSubtitleOptionLanguages: [String]?](/documentation/avkit/avplayerviewcontroller/allowedsubtitleoptionlanguages)
- [var requiresFullSubtitles: Bool](/documentation/avkit/avplayerviewcontroller/requiresfullsubtitles)

### Preventing navigation

- [var requiresLinearPlayback: Bool](/documentation/avkit/avplayerviewcontroller/requireslinearplayback)

### Configuring skipping behavior

- [var isSkipForwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipforwardenabled)
- [var isSkipBackwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipbackwardenabled)
- [var skippingBehavior: AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontroller/skippingbehavior)
- [AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontrollerskippingbehavior)

#### Skipping Behaviors

- [case `default`](/documentation/avkit/avplayerviewcontrollerskippingbehavior/default)
- [case skipItem](/documentation/avkit/avplayerviewcontrollerskippingbehavior/skipitem)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avplayerviewcontrollerskippingbehavior/init(rawvalue:))

### Determining display readiness

- [var isReadyForDisplay: Bool](/documentation/avkit/avplayerviewcontroller/isreadyfordisplay)

### Updating Now Playing information

- [var updatesNowPlayingInfoCenter: Bool](/documentation/avkit/avplayerviewcontroller/updatesnowplayinginfocenter)

### Proposing additional content

- [var contentProposalViewController: AVContentProposalViewController!](/documentation/avkit/avplayerviewcontroller/contentproposalviewcontroller)

### Accessing the player

- [var player: AVPlayer?](/documentation/avkit/avplayerviewcontroller/player)

### Accessing the delegate object

- [var delegate: (any AVPlayerViewControllerDelegate)?](/documentation/avkit/avplayerviewcontroller/delegate)

### Configuring pixel buffers

- [var pixelBufferAttributes: [String : Any]?](/documentation/avkit/avplayerviewcontroller/pixelbufferattributes)

### High dynamic range

- [var preferredDisplayDynamicRange: AVDisplayDynamicRange](/documentation/avkit/avplayerviewcontroller/preferreddisplaydynamicrange)
- [AVDisplayDynamicRange](/documentation/avkit/avdisplaydynamicrange)

#### Enumeration Cases

- [case automatic](/documentation/avkit/avdisplaydynamicrange/automatic)
- [case constrainedHigh](/documentation/avkit/avdisplaydynamicrange/constrainedhigh)
- [case high](/documentation/avkit/avdisplaydynamicrange/high)
- [case standard](/documentation/avkit/avdisplaydynamicrange/standard)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avdisplaydynamicrange/init(rawvalue:))

### Type Properties

- [class var mediaCharacteristicsForSupportedCustomMediaSelectionSchemes: [AVMediaCharacteristic]](/documentation/avkit/avplayerviewcontroller/mediacharacteristicsforsupportedcustommediaselectionschemes)
- [AVPlayerViewControllerDelegate](/documentation/avkit/avplayerviewcontrollerdelegate)

### Dismissing the Player View Controller

- [func playerViewControllerShouldDismiss(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershoulddismiss(_:))
- [func playerViewControllerWillBeginDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillbegindismissaltransition(_:))
- [func playerViewControllerDidEndDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidenddismissaltransition(_:))

### Responding to Picture in Picture Life Cycle Events

- [func playerViewControllerShouldAutomaticallyDismissAtPictureInPictureStart(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershouldautomaticallydismissatpictureinpicturestart(_:))
- [func playerViewControllerWillStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstartpictureinpicture(_:))
- [func playerViewControllerDidStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstartpictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, failedToStartPictureInPictureWithError: any Error)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:failedtostartpictureinpicturewitherror:))
- [func playerViewControllerWillStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstoppictureinpicture(_:))
- [func playerViewControllerDidStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstoppictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForPictureInPictureStopWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforpictureinpicturestopwithcompletionhandler:))

### Responding to Navigation Events

- [func playerViewController(AVPlayerViewController, timeToSeekAfterUserNavigatedFrom: CMTime, to: CMTime) -> CMTime](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:timetoseekafterusernavigatedfrom:to:))
- [func playerViewController(AVPlayerViewController, willResumePlaybackAfterUserNavigatedFrom: CMTime, to: CMTime)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willresumeplaybackafterusernavigatedfrom:to:))
- [func skipToPreviousItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptopreviousitem(for:))
- [func skipToNextItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptonextitem(for:))

### Responding to Interstitial Content Playback Events

- [func playerViewController(AVPlayerViewController, willPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willpresent:))
- [func playerViewController(AVPlayerViewController, didPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didpresent:))

### Responding to Content Proposals

- [func playerViewController(AVPlayerViewController, shouldPresent: AVContentProposal) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:shouldpresent:))
- [func playerViewController(AVPlayerViewController, didAccept: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didaccept:))
- [func playerViewController(AVPlayerViewController, didReject: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didreject:))

### Responding to Media Selection

- [func playerViewController(AVPlayerViewController, didSelect: AVMediaSelectionOption?, in: AVMediaSelectionGroup)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didselect:in:))

### Responding to Transport Bar Changes

- [func playerViewController(AVPlayerViewController, willTransitionToVisibilityOfTransportBar: Bool, with: any AVPlayerViewControllerAnimationCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willtransitiontovisibilityoftransportbar:with:))
- [AVPlayerViewControllerAnimationCoordinator](/documentation/avkit/avplayerviewcontrolleranimationcoordinator)

#### Coordinating Animations

- [func addCoordinatedAnimations((() -> Void)?, completion: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontrolleranimationcoordinator/addcoordinatedanimations(_:completion:))

### Responding to Channel Changes

- [func playerViewController(AVPlayerViewController, skipToNextChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptonextchannel:))
- [func playerViewController(AVPlayerViewController, skipToPreviousChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptopreviouschannel:))
- [func nextChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/nextchannelinterstitialviewcontroller(for:))
- [func previousChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/previouschannelinterstitialviewcontroller(for:))

### Responding to Full-Screen Presentations

- [func playerViewController(AVPlayerViewController, willBeginFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willbeginfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, willEndFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willendfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForFullScreenExitWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforfullscreenexitwithcompletionhandler:))
- [AVCaptureEventInteraction](/documentation/avkit/avcaptureeventinteraction)

### Creating an interaction

- [init(handler: (AVCaptureEvent) -> Void)](/documentation/avkit/avcaptureeventinteraction/init(handler:))
- [init(primary: (AVCaptureEvent) -> Void, secondary: (AVCaptureEvent) -> Void)](/documentation/avkit/avcaptureeventinteraction/init(primary:secondary:))

### Inspecting the interaction

- [var isEnabled: Bool](/documentation/avkit/avcaptureeventinteraction/isenabled)
- [class var defaultCaptureSoundDisabled: Bool](/documentation/avkit/avcaptureeventinteraction/defaultcapturesounddisabled)
- [AVCaptureEvent](/documentation/avkit/avcaptureevent)

### Inspecting the event

- [var phase: AVCaptureEventPhase](/documentation/avkit/avcaptureevent/phase)
- [AVCaptureEventPhase](/documentation/avkit/avcaptureeventphase)

#### Event phases

- [case began](/documentation/avkit/avcaptureeventphase/began)
- [case ended](/documentation/avkit/avcaptureeventphase/ended)
- [case cancelled](/documentation/avkit/avcaptureeventphase/cancelled)

#### Initializers

- [init?(rawValue: UInt)](/documentation/avkit/avcaptureeventphase/init(rawvalue:))

### Playing a sound

- [var shouldPlaySound: Bool](/documentation/avkit/avcaptureevent/shouldplaysound)
- [func play(AVCaptureEventSound) -> Bool](/documentation/avkit/avcaptureevent/play(_:))
- [AVCaptureEventSound](/documentation/avkit/avcaptureeventsound)

### Creating a sound

- [init(url: URL) throws](/documentation/avkit/avcaptureeventsound/init(url:))

### Accessing default sounds

- [class var cameraShutter: AVCaptureEventSound](/documentation/avkit/avcaptureeventsound/camerashutter)
- [class var beginVideoRecording: AVCaptureEventSound](/documentation/avkit/avcaptureeventsound/beginvideorecording)
- [class var endVideoRecording: AVCaptureEventSound](/documentation/avkit/avcaptureeventsound/endvideorecording)
- [AVInputPickerInteraction](/documentation/avkit/avinputpickerinteraction)

### Creating an input picker

- [init()](/documentation/avkit/avinputpickerinteraction/init())
- [init(audioSession: AVAudioSession?)](/documentation/avkit/avinputpickerinteraction/init(audiosession:))

### Managing presentation

- [var isPresented: Bool](/documentation/avkit/avinputpickerinteraction/ispresented)
- [func present()](/documentation/avkit/avinputpickerinteraction/present())
- [func dismiss()](/documentation/avkit/avinputpickerinteraction/dismiss())

### Setting the delegate

- [var delegate: (any AVInputPickerInteraction.Delegate)?](/documentation/avkit/avinputpickerinteraction/delegate-swift.property)
- [AVInputPickerInteraction.Delegate](/documentation/avkit/avinputpickerinteraction/delegate-swift.protocol)

#### Responding to life cycle events

- [func inputPickerInteractionWillBeginPresenting(AVInputPickerInteraction)](/documentation/avkit/avinputpickerinteraction/delegate-swift.protocol/inputpickerinteractionwillbeginpresenting(_:))
- [func inputPickerInteractionDidEndPresenting(AVInputPickerInteraction)](/documentation/avkit/avinputpickerinteraction/delegate-swift.protocol/inputpickerinteractiondidendpresenting(_:))
- [func inputPickerInteractionWillBeginDismissing(AVInputPickerInteraction)](/documentation/avkit/avinputpickerinteraction/delegate-swift.protocol/inputpickerinteractionwillbegindismissing(_:))
- [func inputPickerInteractionDidEndDismissing(AVInputPickerInteraction)](/documentation/avkit/avinputpickerinteraction/delegate-swift.protocol/inputpickerinteractiondidenddismissing(_:))

### Accessing the audio session

- [var audioSession: AVAudioSession](/documentation/avkit/avinputpickerinteraction/audiosession)

## tvOS playback and capture

- [Customizing the tvOS Playback Experience](/documentation/avkit/customizing-the-tvos-playback-experience)
- [Presenting Navigation Markers](/documentation/avkit/presenting-navigation-markers)
- [Working with Interstitial Content](/documentation/avkit/working-with-interstitial-content)
- [Presenting Content Proposals in tvOS](/documentation/avkit/presenting-content-proposals-in-tvos)
- [Working with Overlays and Parental Controls in tvOS](/documentation/avkit/working-with-overlays-and-parental-controls-in-tvos)
- [Supporting Continuity Camera in your tvOS app](/documentation/avkit/supporting-continuity-camera-in-your-tvos-app)
- [AVPlayerViewController](/documentation/avkit/avplayerviewcontroller)

### Configuring presentation

- [var showsPlaybackControls: Bool](/documentation/avkit/avplayerviewcontroller/showsplaybackcontrols)
- [var contentOverlayView: UIView?](/documentation/avkit/avplayerviewcontroller/contentoverlayview)
- [var videoGravity: AVLayerVideoGravity](/documentation/avkit/avplayerviewcontroller/videogravity)
- [var videoBounds: CGRect](/documentation/avkit/avplayerviewcontroller/videobounds)
- [var showsTimecodes: Bool](/documentation/avkit/avplayerviewcontroller/showstimecodes)
- [var appliesPreferredDisplayCriteriaAutomatically: Bool](/documentation/avkit/avplayerviewcontroller/appliespreferreddisplaycriteriaautomatically)

### Customizing the tvOS player UI

- [var playbackControlsIncludeTransportBar: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludetransportbar)
- [var playbackControlsIncludeInfoViews: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludeinfoviews)
- [var transportBarIncludesTitleView: Bool](/documentation/avkit/avplayerviewcontroller/transportbarincludestitleview)
- [var transportBarCustomMenuItems: [UIMenuElement]](/documentation/avkit/avplayerviewcontroller/transportbarcustommenuitems)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var customOverlayViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/customoverlayviewcontroller)
- [var unobscuredContentGuide: UILayoutGuide](/documentation/avkit/avplayerviewcontroller/unobscuredcontentguide)
- [var customInfoViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/custominfoviewcontroller)

### Configuring the visionOS player UI

- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var contextualActionsInfoView: UIView](/documentation/avkit/avplayerviewcontroller/contextualactionsinfoview)
- [var contextualActionsPreviewImage: UIImage?](/documentation/avkit/avplayerviewcontroller/contextualactionspreviewimage)
- [var requiresMonoscopicViewingMode: Bool](/documentation/avkit/avplayerviewcontroller/requiresmonoscopicviewingmode)
- [var experienceController: AVExperienceController](/documentation/avkit/avplayerviewcontroller/experiencecontroller)
- [var groupExperienceCoordinator: AVGroupExperienceCoordinator](/documentation/avkit/avplayerviewcontroller/groupexperiencecoordinator)

### Presenting the visionOS trimming UI

- [var canBeginTrimming: Bool](/documentation/avkit/avplayerviewcontroller/canbegintrimming)
- [func beginTrimming(completionHandler: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontroller/begintrimming(completionhandler:))

### Configuring frame analysis

- [var allowsVideoFrameAnalysis: Bool](/documentation/avkit/avplayerviewcontroller/allowsvideoframeanalysis)
- [var toggleLookupAction: UIAction](/documentation/avkit/avplayerviewcontroller/togglelookupaction)
- [var videoFrameAnalysisTypes: AVVideoFrameAnalysisType](/documentation/avkit/avplayerviewcontroller/videoframeanalysistypes)
- [AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype)

#### Analysis types

- [static var `default`: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/default)
- [static var text: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/text)
- [static var subject: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/subject)
- [static var visualSearch: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/visualsearch)
- [static var machineReadableCode: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/machinereadablecode)

#### Initializers

- [init(rawValue: UInt)](/documentation/avkit/avvideoframeanalysistype/init(rawvalue:))

### Configuring playback speed

- [var speeds: [AVPlaybackSpeed]](/documentation/avkit/avplayerviewcontroller/speeds)
- [var selectedSpeed: AVPlaybackSpeed?](/documentation/avkit/avplayerviewcontroller/selectedspeed)
- [func selectSpeed(AVPlaybackSpeed)](/documentation/avkit/avplayerviewcontroller/selectspeed(_:))
- [AVPlaybackSpeed](/documentation/avkit/avplaybackspeed)

#### Retrieving Default Speeds

- [class var systemDefaultSpeeds: [AVPlaybackSpeed]](/documentation/avkit/avplaybackspeed/systemdefaultspeeds)

#### Creating a Playback Speed

- [init(rate: Float, localizedName: String)](/documentation/avkit/avplaybackspeed/init(rate:localizedname:))

#### Inspecting Speed Details

- [var rate: Float](/documentation/avkit/avplaybackspeed/rate)
- [var localizedName: String](/documentation/avkit/avplaybackspeed/localizedname)
- [var localizedNumericName: String](/documentation/avkit/avplaybackspeed/localizednumericname)

### Configuring Picture in Picture

- [var allowsPictureInPicturePlayback: Bool](/documentation/avkit/avplayerviewcontroller/allowspictureinpictureplayback)
- [var canStartPictureInPictureAutomaticallyFromInline: Bool](/documentation/avkit/avplayerviewcontroller/canstartpictureinpictureautomaticallyfrominline)

### Managing full-screen behavior

- [var entersFullScreenWhenPlaybackBegins: Bool](/documentation/avkit/avplayerviewcontroller/entersfullscreenwhenplaybackbegins)
- [var exitsFullScreenWhenPlaybackEnds: Bool](/documentation/avkit/avplayerviewcontroller/exitsfullscreenwhenplaybackends)

### Managing subtitles

- [var allowedSubtitleOptionLanguages: [String]?](/documentation/avkit/avplayerviewcontroller/allowedsubtitleoptionlanguages)
- [var requiresFullSubtitles: Bool](/documentation/avkit/avplayerviewcontroller/requiresfullsubtitles)

### Preventing navigation

- [var requiresLinearPlayback: Bool](/documentation/avkit/avplayerviewcontroller/requireslinearplayback)

### Configuring skipping behavior

- [var isSkipForwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipforwardenabled)
- [var isSkipBackwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipbackwardenabled)
- [var skippingBehavior: AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontroller/skippingbehavior)
- [AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontrollerskippingbehavior)

#### Skipping Behaviors

- [case `default`](/documentation/avkit/avplayerviewcontrollerskippingbehavior/default)
- [case skipItem](/documentation/avkit/avplayerviewcontrollerskippingbehavior/skipitem)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avplayerviewcontrollerskippingbehavior/init(rawvalue:))

### Determining display readiness

- [var isReadyForDisplay: Bool](/documentation/avkit/avplayerviewcontroller/isreadyfordisplay)

### Updating Now Playing information

- [var updatesNowPlayingInfoCenter: Bool](/documentation/avkit/avplayerviewcontroller/updatesnowplayinginfocenter)

### Proposing additional content

- [var contentProposalViewController: AVContentProposalViewController!](/documentation/avkit/avplayerviewcontroller/contentproposalviewcontroller)

### Accessing the player

- [var player: AVPlayer?](/documentation/avkit/avplayerviewcontroller/player)

### Accessing the delegate object

- [var delegate: (any AVPlayerViewControllerDelegate)?](/documentation/avkit/avplayerviewcontroller/delegate)

### Configuring pixel buffers

- [var pixelBufferAttributes: [String : Any]?](/documentation/avkit/avplayerviewcontroller/pixelbufferattributes)

### High dynamic range

- [var preferredDisplayDynamicRange: AVDisplayDynamicRange](/documentation/avkit/avplayerviewcontroller/preferreddisplaydynamicrange)
- [AVDisplayDynamicRange](/documentation/avkit/avdisplaydynamicrange)

#### Enumeration Cases

- [case automatic](/documentation/avkit/avdisplaydynamicrange/automatic)
- [case constrainedHigh](/documentation/avkit/avdisplaydynamicrange/constrainedhigh)
- [case high](/documentation/avkit/avdisplaydynamicrange/high)
- [case standard](/documentation/avkit/avdisplaydynamicrange/standard)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avdisplaydynamicrange/init(rawvalue:))

### Type Properties

- [class var mediaCharacteristicsForSupportedCustomMediaSelectionSchemes: [AVMediaCharacteristic]](/documentation/avkit/avplayerviewcontroller/mediacharacteristicsforsupportedcustommediaselectionschemes)
- [AVPlayerViewControllerDelegate](/documentation/avkit/avplayerviewcontrollerdelegate)

### Dismissing the Player View Controller

- [func playerViewControllerShouldDismiss(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershoulddismiss(_:))
- [func playerViewControllerWillBeginDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillbegindismissaltransition(_:))
- [func playerViewControllerDidEndDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidenddismissaltransition(_:))

### Responding to Picture in Picture Life Cycle Events

- [func playerViewControllerShouldAutomaticallyDismissAtPictureInPictureStart(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershouldautomaticallydismissatpictureinpicturestart(_:))
- [func playerViewControllerWillStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstartpictureinpicture(_:))
- [func playerViewControllerDidStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstartpictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, failedToStartPictureInPictureWithError: any Error)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:failedtostartpictureinpicturewitherror:))
- [func playerViewControllerWillStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstoppictureinpicture(_:))
- [func playerViewControllerDidStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstoppictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForPictureInPictureStopWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforpictureinpicturestopwithcompletionhandler:))

### Responding to Navigation Events

- [func playerViewController(AVPlayerViewController, timeToSeekAfterUserNavigatedFrom: CMTime, to: CMTime) -> CMTime](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:timetoseekafterusernavigatedfrom:to:))
- [func playerViewController(AVPlayerViewController, willResumePlaybackAfterUserNavigatedFrom: CMTime, to: CMTime)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willresumeplaybackafterusernavigatedfrom:to:))
- [func skipToPreviousItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptopreviousitem(for:))
- [func skipToNextItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptonextitem(for:))

### Responding to Interstitial Content Playback Events

- [func playerViewController(AVPlayerViewController, willPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willpresent:))
- [func playerViewController(AVPlayerViewController, didPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didpresent:))

### Responding to Content Proposals

- [func playerViewController(AVPlayerViewController, shouldPresent: AVContentProposal) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:shouldpresent:))
- [func playerViewController(AVPlayerViewController, didAccept: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didaccept:))
- [func playerViewController(AVPlayerViewController, didReject: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didreject:))

### Responding to Media Selection

- [func playerViewController(AVPlayerViewController, didSelect: AVMediaSelectionOption?, in: AVMediaSelectionGroup)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didselect:in:))

### Responding to Transport Bar Changes

- [func playerViewController(AVPlayerViewController, willTransitionToVisibilityOfTransportBar: Bool, with: any AVPlayerViewControllerAnimationCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willtransitiontovisibilityoftransportbar:with:))
- [AVPlayerViewControllerAnimationCoordinator](/documentation/avkit/avplayerviewcontrolleranimationcoordinator)

#### Coordinating Animations

- [func addCoordinatedAnimations((() -> Void)?, completion: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontrolleranimationcoordinator/addcoordinatedanimations(_:completion:))

### Responding to Channel Changes

- [func playerViewController(AVPlayerViewController, skipToNextChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptonextchannel:))
- [func playerViewController(AVPlayerViewController, skipToPreviousChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptopreviouschannel:))
- [func nextChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/nextchannelinterstitialviewcontroller(for:))
- [func previousChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/previouschannelinterstitialviewcontroller(for:))

### Responding to Full-Screen Presentations

- [func playerViewController(AVPlayerViewController, willBeginFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willbeginfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, willEndFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willendfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForFullScreenExitWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforfullscreenexitwithcompletionhandler:))
- [AVInterstitialTimeRange](/documentation/avkit/avinterstitialtimerange)

### Creating an Interstitial Time Range

- [init(timeRange: CMTimeRange)](/documentation/avkit/avinterstitialtimerange/init(timerange:))

### Inspecting an Interstitial Time Range

- [var timeRange: CMTimeRange](/documentation/avkit/avinterstitialtimerange/timerange)
- [AVNavigationMarkersGroup](/documentation/avkit/avnavigationmarkersgroup)

### Creating a Navigation Marker Group

- [init(title: String?, timedNavigationMarkers: [AVTimedMetadataGroup])](/documentation/avkit/avnavigationmarkersgroup/init(title:timednavigationmarkers:))
- [init(title: String?, dateRangeNavigationMarkers: [AVDateRangeMetadataGroup])](/documentation/avkit/avnavigationmarkersgroup/init(title:daterangenavigationmarkers:))

### Inspecting Navigation Metadata

- [var title: String?](/documentation/avkit/avnavigationmarkersgroup/title)
- [var timedNavigationMarkers: [AVTimedMetadataGroup]?](/documentation/avkit/avnavigationmarkersgroup/timednavigationmarkers)
- [var dateRangeNavigationMarkers: [AVDateRangeMetadataGroup]?](/documentation/avkit/avnavigationmarkersgroup/daterangenavigationmarkers)
- [AVContentProposalViewController](/documentation/avkit/avcontentproposalviewcontroller)

### Configuring the Proposal

- [var contentProposal: AVContentProposal?](/documentation/avkit/avcontentproposalviewcontroller/contentproposal)
- [AVContentProposal](/documentation/avkit/avcontentproposal)

#### Creating a Content Proposal

- [init(contentTimeForTransition: CMTime, title: String, previewImage: UIImage?)](/documentation/avkit/avcontentproposal/init(contenttimefortransition:title:previewimage:))

#### Configuring the Content Proposal

- [var contentTimeForTransition: CMTime](/documentation/avkit/avcontentproposal/contenttimefortransition)
- [var title: String](/documentation/avkit/avcontentproposal/title)
- [var previewImage: UIImage?](/documentation/avkit/avcontentproposal/previewimage)
- [var metadata: [AVMetadataItem]](/documentation/avkit/avcontentproposal/metadata)
- [var automaticAcceptanceInterval: TimeInterval](/documentation/avkit/avcontentproposal/automaticacceptanceinterval)
- [var url: URL?](/documentation/avkit/avcontentproposal/url)
- [var dateOfAutomaticAcceptance: Date?](/documentation/avkit/avcontentproposalviewcontroller/dateofautomaticacceptance)
- [var playerLayoutGuide: UILayoutGuide](/documentation/avkit/avcontentproposalviewcontroller/playerlayoutguide)
- [var preferredPlayerViewFrame: CGRect](/documentation/avkit/avcontentproposalviewcontroller/preferredplayerviewframe)

### Dismissing the Proposal

- [func dismissContentProposal(for: AVContentProposalAction, animated: Bool, completion: (() -> Void)?)](/documentation/avkit/avcontentproposalviewcontroller/dismisscontentproposal(for:animated:completion:))
- [AVContentProposalAction](/documentation/avkit/avcontentproposalaction)

#### Actions

- [case accept](/documentation/avkit/avcontentproposalaction/accept)
- [case reject](/documentation/avkit/avcontentproposalaction/reject)
- [case `defer`](/documentation/avkit/avcontentproposalaction/defer)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avcontentproposalaction/init(rawvalue:))

### Accessing the Player View Controller

- [var playerViewController: AVPlayerViewController?](/documentation/avkit/avcontentproposalviewcontroller/playerviewcontroller)
- [AVDisplayManager](/documentation/avkit/avdisplaymanager)

### Matching a Video’s Native Display Mode

- [var preferredDisplayCriteria: AVDisplayCriteria?](/documentation/avkit/avdisplaymanager/preferreddisplaycriteria)
- [var isDisplayCriteriaMatchingEnabled: Bool](/documentation/avkit/avdisplaymanager/isdisplaycriteriamatchingenabled)
- [var isDisplayModeSwitchInProgress: Bool](/documentation/avkit/avdisplaymanager/isdisplaymodeswitchinprogress)
- [AVContinuityDevicePickerViewController](/documentation/avkit/avcontinuitydevicepickerviewcontroller)

### Checking for feature support

- [class var isSupported: Bool](/documentation/avkit/avcontinuitydevicepickerviewcontroller/issupported)

### Designating a delegate

- [var delegate: (any AVContinuityDevicePickerViewControllerDelegate)?](/documentation/avkit/avcontinuitydevicepickerviewcontroller/delegate)
- [AVContinuityDevicePickerViewControllerDelegate](/documentation/avkit/avcontinuitydevicepickerviewcontrollerdelegate)

### Responding to continuity device events

- [func continuityDevicePickerWillBeginPresenting(AVContinuityDevicePickerViewController)](/documentation/avkit/avcontinuitydevicepickerviewcontrollerdelegate/continuitydevicepickerwillbeginpresenting(_:))
- [func continuityDevicePickerDidCancel(AVContinuityDevicePickerViewController)](/documentation/avkit/avcontinuitydevicepickerviewcontrollerdelegate/continuitydevicepickerdidcancel(_:))
- [func continuityDevicePicker(AVContinuityDevicePickerViewController, didConnect: AVContinuityDevice)](/documentation/avkit/avcontinuitydevicepickerviewcontrollerdelegate/continuitydevicepicker(_:didconnect:))
- [func continuityDevicePickerDidEndPresenting(AVContinuityDevicePickerViewController)](/documentation/avkit/avcontinuitydevicepickerviewcontrollerdelegate/continuitydevicepickerdidendpresenting(_:))

## visionOS playback

- [Playing immersive media with AVKit](/documentation/avkit/playing-immersive-media-with-avkit)
- [Creating a multiview video playback experience in visionOS](/documentation/avkit/creating-a-multiview-video-playback-experience-in-visionos)
- [Adopting the system player interface in visionOS](/documentation/avkit/adopting-the-system-player-interface-in-visionos)
- [Trimming and exporting media in visionOS](/documentation/avkit/trimming-and-exporting-media-in-visionos)
- [AVPlayerViewController](/documentation/avkit/avplayerviewcontroller)

### Configuring presentation

- [var showsPlaybackControls: Bool](/documentation/avkit/avplayerviewcontroller/showsplaybackcontrols)
- [var contentOverlayView: UIView?](/documentation/avkit/avplayerviewcontroller/contentoverlayview)
- [var videoGravity: AVLayerVideoGravity](/documentation/avkit/avplayerviewcontroller/videogravity)
- [var videoBounds: CGRect](/documentation/avkit/avplayerviewcontroller/videobounds)
- [var showsTimecodes: Bool](/documentation/avkit/avplayerviewcontroller/showstimecodes)
- [var appliesPreferredDisplayCriteriaAutomatically: Bool](/documentation/avkit/avplayerviewcontroller/appliespreferreddisplaycriteriaautomatically)

### Customizing the tvOS player UI

- [var playbackControlsIncludeTransportBar: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludetransportbar)
- [var playbackControlsIncludeInfoViews: Bool](/documentation/avkit/avplayerviewcontroller/playbackcontrolsincludeinfoviews)
- [var transportBarIncludesTitleView: Bool](/documentation/avkit/avplayerviewcontroller/transportbarincludestitleview)
- [var transportBarCustomMenuItems: [UIMenuElement]](/documentation/avkit/avplayerviewcontroller/transportbarcustommenuitems)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var customOverlayViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/customoverlayviewcontroller)
- [var unobscuredContentGuide: UILayoutGuide](/documentation/avkit/avplayerviewcontroller/unobscuredcontentguide)
- [var customInfoViewController: UIViewController?](/documentation/avkit/avplayerviewcontroller/custominfoviewcontroller)

### Configuring the visionOS player UI

- [var infoViewActions: [UIAction]!](/documentation/avkit/avplayerviewcontroller/infoviewactions)
- [var customInfoViewControllers: [UIViewController]](/documentation/avkit/avplayerviewcontroller/custominfoviewcontrollers)
- [var contextualActions: [UIAction]](/documentation/avkit/avplayerviewcontroller/contextualactions)
- [var contextualActionsInfoView: UIView](/documentation/avkit/avplayerviewcontroller/contextualactionsinfoview)
- [var contextualActionsPreviewImage: UIImage?](/documentation/avkit/avplayerviewcontroller/contextualactionspreviewimage)
- [var requiresMonoscopicViewingMode: Bool](/documentation/avkit/avplayerviewcontroller/requiresmonoscopicviewingmode)
- [var experienceController: AVExperienceController](/documentation/avkit/avplayerviewcontroller/experiencecontroller)
- [var groupExperienceCoordinator: AVGroupExperienceCoordinator](/documentation/avkit/avplayerviewcontroller/groupexperiencecoordinator)

### Presenting the visionOS trimming UI

- [var canBeginTrimming: Bool](/documentation/avkit/avplayerviewcontroller/canbegintrimming)
- [func beginTrimming(completionHandler: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontroller/begintrimming(completionhandler:))

### Configuring frame analysis

- [var allowsVideoFrameAnalysis: Bool](/documentation/avkit/avplayerviewcontroller/allowsvideoframeanalysis)
- [var toggleLookupAction: UIAction](/documentation/avkit/avplayerviewcontroller/togglelookupaction)
- [var videoFrameAnalysisTypes: AVVideoFrameAnalysisType](/documentation/avkit/avplayerviewcontroller/videoframeanalysistypes)
- [AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype)

#### Analysis types

- [static var `default`: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/default)
- [static var text: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/text)
- [static var subject: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/subject)
- [static var visualSearch: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/visualsearch)
- [static var machineReadableCode: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/machinereadablecode)

#### Initializers

- [init(rawValue: UInt)](/documentation/avkit/avvideoframeanalysistype/init(rawvalue:))

### Configuring playback speed

- [var speeds: [AVPlaybackSpeed]](/documentation/avkit/avplayerviewcontroller/speeds)
- [var selectedSpeed: AVPlaybackSpeed?](/documentation/avkit/avplayerviewcontroller/selectedspeed)
- [func selectSpeed(AVPlaybackSpeed)](/documentation/avkit/avplayerviewcontroller/selectspeed(_:))
- [AVPlaybackSpeed](/documentation/avkit/avplaybackspeed)

#### Retrieving Default Speeds

- [class var systemDefaultSpeeds: [AVPlaybackSpeed]](/documentation/avkit/avplaybackspeed/systemdefaultspeeds)

#### Creating a Playback Speed

- [init(rate: Float, localizedName: String)](/documentation/avkit/avplaybackspeed/init(rate:localizedname:))

#### Inspecting Speed Details

- [var rate: Float](/documentation/avkit/avplaybackspeed/rate)
- [var localizedName: String](/documentation/avkit/avplaybackspeed/localizedname)
- [var localizedNumericName: String](/documentation/avkit/avplaybackspeed/localizednumericname)

### Configuring Picture in Picture

- [var allowsPictureInPicturePlayback: Bool](/documentation/avkit/avplayerviewcontroller/allowspictureinpictureplayback)
- [var canStartPictureInPictureAutomaticallyFromInline: Bool](/documentation/avkit/avplayerviewcontroller/canstartpictureinpictureautomaticallyfrominline)

### Managing full-screen behavior

- [var entersFullScreenWhenPlaybackBegins: Bool](/documentation/avkit/avplayerviewcontroller/entersfullscreenwhenplaybackbegins)
- [var exitsFullScreenWhenPlaybackEnds: Bool](/documentation/avkit/avplayerviewcontroller/exitsfullscreenwhenplaybackends)

### Managing subtitles

- [var allowedSubtitleOptionLanguages: [String]?](/documentation/avkit/avplayerviewcontroller/allowedsubtitleoptionlanguages)
- [var requiresFullSubtitles: Bool](/documentation/avkit/avplayerviewcontroller/requiresfullsubtitles)

### Preventing navigation

- [var requiresLinearPlayback: Bool](/documentation/avkit/avplayerviewcontroller/requireslinearplayback)

### Configuring skipping behavior

- [var isSkipForwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipforwardenabled)
- [var isSkipBackwardEnabled: Bool](/documentation/avkit/avplayerviewcontroller/isskipbackwardenabled)
- [var skippingBehavior: AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontroller/skippingbehavior)
- [AVPlayerViewControllerSkippingBehavior](/documentation/avkit/avplayerviewcontrollerskippingbehavior)

#### Skipping Behaviors

- [case `default`](/documentation/avkit/avplayerviewcontrollerskippingbehavior/default)
- [case skipItem](/documentation/avkit/avplayerviewcontrollerskippingbehavior/skipitem)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avplayerviewcontrollerskippingbehavior/init(rawvalue:))

### Determining display readiness

- [var isReadyForDisplay: Bool](/documentation/avkit/avplayerviewcontroller/isreadyfordisplay)

### Updating Now Playing information

- [var updatesNowPlayingInfoCenter: Bool](/documentation/avkit/avplayerviewcontroller/updatesnowplayinginfocenter)

### Proposing additional content

- [var contentProposalViewController: AVContentProposalViewController!](/documentation/avkit/avplayerviewcontroller/contentproposalviewcontroller)

### Accessing the player

- [var player: AVPlayer?](/documentation/avkit/avplayerviewcontroller/player)

### Accessing the delegate object

- [var delegate: (any AVPlayerViewControllerDelegate)?](/documentation/avkit/avplayerviewcontroller/delegate)

### Configuring pixel buffers

- [var pixelBufferAttributes: [String : Any]?](/documentation/avkit/avplayerviewcontroller/pixelbufferattributes)

### High dynamic range

- [var preferredDisplayDynamicRange: AVDisplayDynamicRange](/documentation/avkit/avplayerviewcontroller/preferreddisplaydynamicrange)
- [AVDisplayDynamicRange](/documentation/avkit/avdisplaydynamicrange)

#### Enumeration Cases

- [case automatic](/documentation/avkit/avdisplaydynamicrange/automatic)
- [case constrainedHigh](/documentation/avkit/avdisplaydynamicrange/constrainedhigh)
- [case high](/documentation/avkit/avdisplaydynamicrange/high)
- [case standard](/documentation/avkit/avdisplaydynamicrange/standard)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avdisplaydynamicrange/init(rawvalue:))

### Type Properties

- [class var mediaCharacteristicsForSupportedCustomMediaSelectionSchemes: [AVMediaCharacteristic]](/documentation/avkit/avplayerviewcontroller/mediacharacteristicsforsupportedcustommediaselectionschemes)
- [AVPlayerViewControllerDelegate](/documentation/avkit/avplayerviewcontrollerdelegate)

### Dismissing the Player View Controller

- [func playerViewControllerShouldDismiss(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershoulddismiss(_:))
- [func playerViewControllerWillBeginDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillbegindismissaltransition(_:))
- [func playerViewControllerDidEndDismissalTransition(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidenddismissaltransition(_:))

### Responding to Picture in Picture Life Cycle Events

- [func playerViewControllerShouldAutomaticallyDismissAtPictureInPictureStart(AVPlayerViewController) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollershouldautomaticallydismissatpictureinpicturestart(_:))
- [func playerViewControllerWillStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstartpictureinpicture(_:))
- [func playerViewControllerDidStartPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstartpictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, failedToStartPictureInPictureWithError: any Error)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:failedtostartpictureinpicturewitherror:))
- [func playerViewControllerWillStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerwillstoppictureinpicture(_:))
- [func playerViewControllerDidStopPictureInPicture(AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontrollerdidstoppictureinpicture(_:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForPictureInPictureStopWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforpictureinpicturestopwithcompletionhandler:))

### Responding to Navigation Events

- [func playerViewController(AVPlayerViewController, timeToSeekAfterUserNavigatedFrom: CMTime, to: CMTime) -> CMTime](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:timetoseekafterusernavigatedfrom:to:))
- [func playerViewController(AVPlayerViewController, willResumePlaybackAfterUserNavigatedFrom: CMTime, to: CMTime)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willresumeplaybackafterusernavigatedfrom:to:))
- [func skipToPreviousItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptopreviousitem(for:))
- [func skipToNextItem(for: AVPlayerViewController)](/documentation/avkit/avplayerviewcontrollerdelegate/skiptonextitem(for:))

### Responding to Interstitial Content Playback Events

- [func playerViewController(AVPlayerViewController, willPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willpresent:))
- [func playerViewController(AVPlayerViewController, didPresent: AVInterstitialTimeRange)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didpresent:))

### Responding to Content Proposals

- [func playerViewController(AVPlayerViewController, shouldPresent: AVContentProposal) -> Bool](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:shouldpresent:))
- [func playerViewController(AVPlayerViewController, didAccept: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didaccept:))
- [func playerViewController(AVPlayerViewController, didReject: AVContentProposal)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didreject:))

### Responding to Media Selection

- [func playerViewController(AVPlayerViewController, didSelect: AVMediaSelectionOption?, in: AVMediaSelectionGroup)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:didselect:in:))

### Responding to Transport Bar Changes

- [func playerViewController(AVPlayerViewController, willTransitionToVisibilityOfTransportBar: Bool, with: any AVPlayerViewControllerAnimationCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willtransitiontovisibilityoftransportbar:with:))
- [AVPlayerViewControllerAnimationCoordinator](/documentation/avkit/avplayerviewcontrolleranimationcoordinator)

#### Coordinating Animations

- [func addCoordinatedAnimations((() -> Void)?, completion: ((Bool) -> Void)?)](/documentation/avkit/avplayerviewcontrolleranimationcoordinator/addcoordinatedanimations(_:completion:))

### Responding to Channel Changes

- [func playerViewController(AVPlayerViewController, skipToNextChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptonextchannel:))
- [func playerViewController(AVPlayerViewController, skipToPreviousChannel: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:skiptopreviouschannel:))
- [func nextChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/nextchannelinterstitialviewcontroller(for:))
- [func previousChannelInterstitialViewController(for: AVPlayerViewController) -> UIViewController](/documentation/avkit/avplayerviewcontrollerdelegate/previouschannelinterstitialviewcontroller(for:))

### Responding to Full-Screen Presentations

- [func playerViewController(AVPlayerViewController, willBeginFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willbeginfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, willEndFullScreenPresentationWithAnimationCoordinator: any UIViewControllerTransitionCoordinator)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:willendfullscreenpresentationwithanimationcoordinator:))
- [func playerViewController(AVPlayerViewController, restoreUserInterfaceForFullScreenExitWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewcontrollerdelegate/playerviewcontroller(_:restoreuserinterfaceforfullscreenexitwithcompletionhandler:))
- [AVExperienceController](/documentation/avkit/avexperiencecontroller)

### Configuring the experience

- [var allowedExperiences: AVExperienceController.Experiences](/documentation/avkit/avexperiencecontroller/allowedexperiences)
- [var availableExperiences: AVExperienceController.Experiences](/documentation/avkit/avexperiencecontroller/availableexperiences)
- [AVExperienceController.Experiences](/documentation/avkit/avexperiencecontroller/experiences)

#### Defining experiences

- [static func only<C>(C) -> AVExperienceController.Experiences](/documentation/avkit/avexperiencecontroller/experiences/only(_:))
- [static func recommended<C>(excluding: C, including: C) -> AVExperienceController.Experiences](/documentation/avkit/avexperiencecontroller/experiences/recommended(excluding:including:))
- [var experience: AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/experience-swift.property)
- [AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/experience-swift.enum)

#### Supported experiences

- [case embedded](/documentation/avkit/avexperiencecontroller/experience-swift.enum/embedded)
- [case expanded](/documentation/avkit/avexperiencecontroller/experience-swift.enum/expanded)
- [case multiview](/documentation/avkit/avexperiencecontroller/experience-swift.enum/multiview)

#### Enumeration Cases

- [case immersive](/documentation/avkit/avexperiencecontroller/experience-swift.enum/immersive)
- [var configuration: AVExperienceController.Configuration](/documentation/avkit/avexperiencecontroller/configuration-swift.property)
- [AVExperienceController.Configuration](/documentation/avkit/avexperiencecontroller/configuration-swift.struct)

#### Configuring experiences

- [var expanded: AVExperienceController.ExpandedConfiguration](/documentation/avkit/avexperiencecontroller/configuration-swift.struct/expanded)
- [AVExperienceController.ExpandedConfiguration](/documentation/avkit/avexperiencecontroller/expandedconfiguration)

##### Creating an expanded configuration

- [init(fallbackPlacement: AVExperienceController.ExpandedConfiguration.Placement)](/documentation/avkit/avexperiencecontroller/expandedconfiguration/init(fallbackplacement:))

##### Specifying placement

- [var fallbackPlacement: AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/fallbackplacement)
- [AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement)

###### Placements

- [static func over(scene: UIScene) -> AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement/over(scene:))
- [static var unspecified: AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement/unspecified)

##### Instance Properties

- [var automaticTransitionToImmersive: AVExperienceController.ExpandedConfiguration.AutomaticTransitionToImmersive](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.property)

##### Enumerations

- [AVExperienceController.ExpandedConfiguration.AutomaticTransitionToImmersive](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum)

###### Enumeration Cases

- [case `default`](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum/default)
- [case none](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum/none)

#### Structures

- [AVExperienceController.Configuration.Placement](/documentation/avkit/avexperiencecontroller/configuration-swift.struct/placement-swift.struct)

##### Type Properties

- [static var unspecified: AVExperienceController.Configuration.Placement](/documentation/avkit/avexperiencecontroller/configuration-swift.struct/placement-swift.struct/unspecified)

##### Type Methods

- [static func over(scene: UIScene) -> AVExperienceController.Configuration.Placement](/documentation/avkit/avexperiencecontroller/configuration-swift.struct/placement-swift.struct/over(scene:))

#### Instance Properties

- [var placement: AVExperienceController.Configuration.Placement](/documentation/avkit/avexperiencecontroller/configuration-swift.struct/placement-swift.property)

### Transitioning experiences

- [func transition(to: AVExperienceController.Experience) async -> AVExperienceController.TransitionContext.TransitionResult](/documentation/avkit/avexperiencecontroller/transition(to:))

### Configuring a delegate

- [var delegate: (any AVExperienceController.Delegate)?](/documentation/avkit/avexperiencecontroller/delegate-swift.property)
- [AVExperienceController.Delegate](/documentation/avkit/avexperiencecontroller/delegate-swift.protocol)

#### Responding to experience changes

- [func experienceController(AVExperienceController, didChangeAvailableExperiences: AVExperienceController.Experiences)](/documentation/avkit/avexperiencecontroller/delegate-swift.protocol/experiencecontroller(_:didchangeavailableexperiences:))
- [func experienceController(AVExperienceController, prepareForTransitionUsing: AVExperienceController.TransitionContext) async](/documentation/avkit/avexperiencecontroller/delegate-swift.protocol/experiencecontroller(_:preparefortransitionusing:))
- [func experienceController(AVExperienceController, didChangeTransitionContext: AVExperienceController.TransitionContext)](/documentation/avkit/avexperiencecontroller/delegate-swift.protocol/experiencecontroller(_:didchangetransitioncontext:))
- [AVExperienceController.TransitionContext](/documentation/avkit/avexperiencecontroller/transitioncontext)

##### Instance Properties

- [let fromExperience: AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/transitioncontext/fromexperience)
- [let status: AVExperienceController.TransitionContext.Status](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.property)
- [let toExperience: AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/transitioncontext/toexperience)

##### Enumerations

- [AVExperienceController.TransitionContext.ReversedReason](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason)

###### Enumeration Cases

- [case invalidConfiguration](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/invalidconfiguration)
- [case invalidExperience](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/invalidexperience)
- [case transitionCancelled](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitioncancelled)
- [case transitionFailed](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitionfailed)
- [case transitionInProgress](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitioninprogress)
- [AVExperienceController.TransitionContext.Status](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum)

###### Enumeration Cases

- [case finished(result: AVExperienceController.TransitionContext.TransitionResult)](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/finished(result:))
- [case preparing](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/preparing)
- [case transitioning](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/transitioning)
- [AVExperienceController.TransitionContext.TransitionResult](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult)

###### Enumeration Cases

- [case completed](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult/completed)
- [case reversed(reason: AVExperienceController.TransitionContext.ReversedReason)](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult/reversed(reason:))

### Structures

- [AVExperienceController.ExpandedConfiguration](/documentation/avkit/avexperiencecontroller/expandedconfiguration)

#### Creating an expanded configuration

- [init(fallbackPlacement: AVExperienceController.ExpandedConfiguration.Placement)](/documentation/avkit/avexperiencecontroller/expandedconfiguration/init(fallbackplacement:))

#### Specifying placement

- [var fallbackPlacement: AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/fallbackplacement)
- [AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement)

##### Placements

- [static func over(scene: UIScene) -> AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement/over(scene:))
- [static var unspecified: AVExperienceController.ExpandedConfiguration.Placement](/documentation/avkit/avexperiencecontroller/expandedconfiguration/placement/unspecified)

#### Instance Properties

- [var automaticTransitionToImmersive: AVExperienceController.ExpandedConfiguration.AutomaticTransitionToImmersive](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.property)

#### Enumerations

- [AVExperienceController.ExpandedConfiguration.AutomaticTransitionToImmersive](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum)

##### Enumeration Cases

- [case `default`](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum/default)
- [case none](/documentation/avkit/avexperiencecontroller/expandedconfiguration/automatictransitiontoimmersive-swift.enum/none)
- [AVExperienceController.TransitionContext](/documentation/avkit/avexperiencecontroller/transitioncontext)

#### Instance Properties

- [let fromExperience: AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/transitioncontext/fromexperience)
- [let status: AVExperienceController.TransitionContext.Status](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.property)
- [let toExperience: AVExperienceController.Experience](/documentation/avkit/avexperiencecontroller/transitioncontext/toexperience)

#### Enumerations

- [AVExperienceController.TransitionContext.ReversedReason](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason)

##### Enumeration Cases

- [case invalidConfiguration](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/invalidconfiguration)
- [case invalidExperience](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/invalidexperience)
- [case transitionCancelled](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitioncancelled)
- [case transitionFailed](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitionfailed)
- [case transitionInProgress](/documentation/avkit/avexperiencecontroller/transitioncontext/reversedreason/transitioninprogress)
- [AVExperienceController.TransitionContext.Status](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum)

##### Enumeration Cases

- [case finished(result: AVExperienceController.TransitionContext.TransitionResult)](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/finished(result:))
- [case preparing](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/preparing)
- [case transitioning](/documentation/avkit/avexperiencecontroller/transitioncontext/status-swift.enum/transitioning)
- [AVExperienceController.TransitionContext.TransitionResult](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult)

##### Enumeration Cases

- [case completed](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult/completed)
- [case reversed(reason: AVExperienceController.TransitionContext.ReversedReason)](/documentation/avkit/avexperiencecontroller/transitioncontext/transitionresult/reversed(reason:))
- [AVMultiviewManager](/documentation/avkit/avmultiviewmanager)

### Accessing the default instance

- [static var `default`: AVMultiviewManager](/documentation/avkit/avmultiviewmanager/default)

### Providing additional UI

- [var contentSelectionViewController: AVContentSelectionViewController?](/documentation/avkit/avmultiviewmanager/contentselectionviewcontroller)
- [AVContentSelectionViewController](/documentation/avkit/avcontentselectionviewcontroller)

#### Creating a view controller.

- [init?(coder: NSCoder)](/documentation/avkit/avcontentselectionviewcontroller/init(coder:))
- [init(nibName: String?, bundle: Bundle?)](/documentation/avkit/avcontentselectionviewcontroller/init(nibname:bundle:))

### Dismissing the multiview experience

- [func dismiss()](/documentation/avkit/avmultiviewmanager/dismiss())
- [AVGroupExperienceCoordinator](/documentation/avkit/avgroupexperiencecoordinator)

### Coordinating state changes

- [func coordinateWithSession<T>(GroupSession<T>)](/documentation/avkit/avgroupexperiencecoordinator/coordinatewithsession(_:))

## macOS playback and capture

- [Implementing Trimming in a macOS Player](/documentation/avkit/implementing-trimming-in-a-macos-player)
- [AVPlayerView](/documentation/avkit/avplayerview)

### Customizing the user interface

- [var controlsStyle: AVPlayerViewControlsStyle](/documentation/avkit/avplayerview/controlsstyle)
- [AVPlayerViewControlsStyle](/documentation/avkit/avplayerviewcontrolsstyle)

#### Controls Styles

- [case none](/documentation/avkit/avplayerviewcontrolsstyle/none)
- [case inline](/documentation/avkit/avplayerviewcontrolsstyle/inline)
- [case floating](/documentation/avkit/avplayerviewcontrolsstyle/floating)
- [case minimal](/documentation/avkit/avplayerviewcontrolsstyle/minimal)
- [static var `default`: AVPlayerViewControlsStyle](/documentation/avkit/avplayerviewcontrolsstyle/default)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avplayerviewcontrolsstyle/init(rawvalue:))
- [var showsFrameSteppingButtons: Bool](/documentation/avkit/avplayerview/showsframesteppingbuttons)
- [var showsSharingServiceButton: Bool](/documentation/avkit/avplayerview/showssharingservicebutton)
- [var showsFullScreenToggleButton: Bool](/documentation/avkit/avplayerview/showsfullscreentogglebutton)
- [var showsTimecodes: Bool](/documentation/avkit/avplayerview/showstimecodes)
- [var contentOverlayView: NSView?](/documentation/avkit/avplayerview/contentoverlayview)
- [var actionPopUpButtonMenu: NSMenu?](/documentation/avkit/avplayerview/actionpopupbuttonmenu)
- [var updatesNowPlayingInfoCenter: Bool](/documentation/avkit/avplayerview/updatesnowplayinginfocenter)

### Customizing the video presentation

- [var isReadyForDisplay: Bool](/documentation/avkit/avplayerview/isreadyfordisplay)
- [var videoBounds: NSRect](/documentation/avkit/avplayerview/videobounds)
- [var videoGravity: AVLayerVideoGravity](/documentation/avkit/avplayerview/videogravity)

### Configuring frame analysis

- [var allowsVideoFrameAnalysis: Bool](/documentation/avkit/avplayerview/allowsvideoframeanalysis)
- [var videoFrameAnalysisTypes: AVVideoFrameAnalysisType](/documentation/avkit/avplayerview/videoframeanalysistypes)
- [AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype)

#### Analysis types

- [static var `default`: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/default)
- [static var text: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/text)
- [static var subject: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/subject)
- [static var visualSearch: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/visualsearch)
- [static var machineReadableCode: AVVideoFrameAnalysisType](/documentation/avkit/avvideoframeanalysistype/machinereadablecode)

#### Initializers

- [init(rawValue: UInt)](/documentation/avkit/avvideoframeanalysistype/init(rawvalue:))

### Configuring the playback speed

- [var speeds: [AVPlaybackSpeed]](/documentation/avkit/avplayerview/speeds)
- [var selectedSpeed: AVPlaybackSpeed?](/documentation/avkit/avplayerview/selectedspeed)
- [func selectSpeed(AVPlaybackSpeed)](/documentation/avkit/avplayerview/selectspeed(_:))
- [AVPlaybackSpeed](/documentation/avkit/avplaybackspeed)

#### Retrieving Default Speeds

- [class var systemDefaultSpeeds: [AVPlaybackSpeed]](/documentation/avkit/avplaybackspeed/systemdefaultspeeds)

#### Creating a Playback Speed

- [init(rate: Float, localizedName: String)](/documentation/avkit/avplaybackspeed/init(rate:localizedname:))

#### Inspecting Speed Details

- [var rate: Float](/documentation/avkit/avplaybackspeed/rate)
- [var localizedName: String](/documentation/avkit/avplaybackspeed/localizedname)
- [var localizedNumericName: String](/documentation/avkit/avplaybackspeed/localizednumericname)

### Configuring picture in picture

- [var allowsPictureInPicturePlayback: Bool](/documentation/avkit/avplayerview/allowspictureinpictureplayback)
- [var pictureInPictureDelegate: (any AVPlayerViewPictureInPictureDelegate)?](/documentation/avkit/avplayerview/pictureinpicturedelegate)
- [AVPlayerViewPictureInPictureDelegate](/documentation/avkit/avplayerviewpictureinpicturedelegate)

#### Responding to Picture in Picture Playback Events

- [func playerViewWillStartPicture(inPicture: AVPlayerView)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerviewwillstartpicture(inpicture:))
- [func playerViewDidStartPicture(inPicture: AVPlayerView)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerviewdidstartpicture(inpicture:))
- [func playerViewWillStopPicture(inPicture: AVPlayerView)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerviewwillstoppicture(inpicture:))
- [func playerViewDidStopPicture(inPicture: AVPlayerView)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerviewdidstoppicture(inpicture:))
- [func playerView(AVPlayerView, failedToStartPictureInPictureWithError: any Error)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerview(_:failedtostartpictureinpicturewitherror:))
- [func playerView(AVPlayerView, restoreUserInterfaceForPictureInPictureStopWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerview(_:restoreuserinterfaceforpictureinpicturestopwithcompletionhandler:))
- [func playerViewShouldAutomaticallyDismissAtPicture(inPictureStart: AVPlayerView) -> Bool](/documentation/avkit/avplayerviewpictureinpicturedelegate/playerviewshouldautomaticallydismissatpicture(inpicturestart:))

### Magnifying video

- [var allowsMagnification: Bool](/documentation/avkit/avplayerview/allowsmagnification)
- [var magnification: CGFloat](/documentation/avkit/avplayerview/magnification)
- [func setMagnification(CGFloat, centeredAt: CGPoint)](/documentation/avkit/avplayerview/setmagnification(_:centeredat:))

### Displaying the chapter and title

- [func flashChapterNumber(Int, chapterTitle: String?)](/documentation/avkit/avplayerview/flashchapternumber(_:chaptertitle:))

### Trimming media

- [var canBeginTrimming: Bool](/documentation/avkit/avplayerview/canbegintrimming)
- [func beginTrimming(completionHandler: ((AVPlayerViewTrimResult) -> Void)?)](/documentation/avkit/avplayerview/begintrimming(completionhandler:))
- [AVPlayerViewTrimResult](/documentation/avkit/avplayerviewtrimresult)

#### Trim Results

- [case okButton](/documentation/avkit/avplayerviewtrimresult/okbutton)
- [case cancelButton](/documentation/avkit/avplayerviewtrimresult/cancelbutton)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avplayerviewtrimresult/init(rawvalue:))

### Setting the player object

- [var player: AVPlayer?](/documentation/avkit/avplayerview/player)

### Setting the delegate object

- [var delegate: (any AVPlayerViewDelegate)?](/documentation/avkit/avplayerview/delegate)
- [AVPlayerViewDelegate](/documentation/avkit/avplayerviewdelegate)

#### Responding to Full Screen Events

- [func playerViewWillEnterFullScreen(AVPlayerView)](/documentation/avkit/avplayerviewdelegate/playerviewwillenterfullscreen(_:))
- [func playerViewDidEnterFullScreen(AVPlayerView)](/documentation/avkit/avplayerviewdelegate/playerviewdidenterfullscreen(_:))
- [func playerViewWillExitFullScreen(AVPlayerView)](/documentation/avkit/avplayerviewdelegate/playerviewwillexitfullscreen(_:))
- [func playerViewDidExitFullScreen(AVPlayerView)](/documentation/avkit/avplayerviewdelegate/playerviewdidexitfullscreen(_:))
- [func playerView(AVPlayerView, restoreUserInterfaceForFullScreenExitWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avplayerviewdelegate/playerview(_:restoreuserinterfaceforfullscreenexitwithcompletionhandler:))

### High dynamic range

- [var preferredDisplayDynamicRange: AVDisplayDynamicRange](/documentation/avkit/avplayerview/preferreddisplaydynamicrange)
- [AVDisplayDynamicRange](/documentation/avkit/avdisplaydynamicrange)

#### Enumeration Cases

- [case automatic](/documentation/avkit/avdisplaydynamicrange/automatic)
- [case constrainedHigh](/documentation/avkit/avdisplaydynamicrange/constrainedhigh)
- [case high](/documentation/avkit/avdisplaydynamicrange/high)
- [case standard](/documentation/avkit/avdisplaydynamicrange/standard)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avdisplaydynamicrange/init(rawvalue:))
- [AVCaptureView](/documentation/avkit/avcaptureview)

### Configuring the Capture Session

- [var session: AVCaptureSession?](/documentation/avkit/avcaptureview/session)
- [func setSession(AVCaptureSession?, showVideoPreview: Bool, showAudioPreview: Bool)](/documentation/avkit/avcaptureview/setsession(_:showvideopreview:showaudiopreview:))

### Customizing the View

- [var controlsStyle: AVCaptureViewControlsStyle](/documentation/avkit/avcaptureview/controlsstyle)
- [AVCaptureViewControlsStyle](/documentation/avkit/avcaptureviewcontrolsstyle)

#### Controls Styles

- [case inline](/documentation/avkit/avcaptureviewcontrolsstyle/inline)
- [case floating](/documentation/avkit/avcaptureviewcontrolsstyle/floating)
- [case inlineDeviceSelection](/documentation/avkit/avcaptureviewcontrolsstyle/inlinedeviceselection)
- [static var `default`: AVCaptureViewControlsStyle](/documentation/avkit/avcaptureviewcontrolsstyle/default)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avcaptureviewcontrolsstyle/init(rawvalue:))
- [var videoGravity: AVLayerVideoGravity](/documentation/avkit/avcaptureview/videogravity)

### Configuring the Delegate

- [var delegate: (any AVCaptureViewDelegate)?](/documentation/avkit/avcaptureview/delegate)
- [AVCaptureViewDelegate](/documentation/avkit/avcaptureviewdelegate)

#### Starting a New Recording

- [func captureView(AVCaptureView, startRecordingTo: AVCaptureFileOutput)](/documentation/avkit/avcaptureviewdelegate/captureview(_:startrecordingto:))

### Recording Media

- [var fileOutput: AVCaptureFileOutput?](/documentation/avkit/avcaptureview/fileoutput)

## Multiplatform playback and capture

- [VideoPlayer](/documentation/avkit/videoplayer)

### Creating a video player

- [init(player: AVPlayer?)](/documentation/avkit/videoplayer/init(player:))
- [init(player: AVPlayer?, videoOverlay: () -> VideoOverlay)](/documentation/avkit/videoplayer/init(player:videooverlay:))

## Picture in Picture

- [Adopting Picture in Picture Playback in tvOS](/documentation/avkit/adopting-picture-in-picture-playback-in-tvos)
- [Adopting Picture in Picture in a Standard Player](/documentation/avkit/adopting-picture-in-picture-in-a-standard-player)
- [Adopting Picture in Picture in a Custom Player](/documentation/avkit/adopting-picture-in-picture-in-a-custom-player)
- [Adopting Picture in Picture for video calls](/documentation/avkit/adopting-picture-in-picture-for-video-calls)
- [Accessing the camera while multitasking on iPad](/documentation/avkit/accessing-the-camera-while-multitasking-on-ipad)
- [AVPictureInPictureController](/documentation/avkit/avpictureinpicturecontroller)

### Creating a Controller

- [init(contentSource: AVPictureInPictureController.ContentSource)](/documentation/avkit/avpictureinpicturecontroller/init(contentsource:))
- [convenience init?(playerLayer: AVPlayerLayer)](/documentation/avkit/avpictureinpicturecontroller/init(playerlayer:))

### Configuring the Content Source

- [var contentSource: AVPictureInPictureController.ContentSource?](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.property)
- [AVPictureInPictureController.ContentSource](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class)

#### Creating a Content Source

- [init(playerLayer: AVPlayerLayer)](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/init(playerlayer:))
- [init(sampleBufferDisplayLayer: AVSampleBufferDisplayLayer, playbackDelegate: any AVPictureInPictureSampleBufferPlaybackDelegate)](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/init(samplebufferdisplaylayer:playbackdelegate:))
- [init(activeVideoCallSourceView: UIView, contentViewController: AVPictureInPictureVideoCallViewController)](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/init(activevideocallsourceview:contentviewcontroller:))

#### Accessing the Presentation Layer

- [var playerLayer: AVPlayerLayer?](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/playerlayer)
- [var sampleBufferDisplayLayer: AVSampleBufferDisplayLayer?](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/samplebufferdisplaylayer)

#### Accessing the Active Call Presentation

- [var activeVideoCallSourceView: UIView?](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/activevideocallsourceview)
- [var activeVideoCallContentViewController: AVPictureInPictureVideoCallViewController](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/activevideocallcontentviewcontroller)
- [AVPictureInPictureVideoCallViewController](/documentation/avkit/avpictureinpicturevideocallviewcontroller)

#### Configuring the Delegate

- [var sampleBufferPlaybackDelegate: (any AVPictureInPictureSampleBufferPlaybackDelegate)?](/documentation/avkit/avpictureinpicturecontroller/contentsource-swift.class/samplebufferplaybackdelegate)
- [AVPictureInPictureSampleBufferPlaybackDelegate](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate)

##### Responding to Playback Events

- [func pictureInPictureController(AVPictureInPictureController, setPlaying: Bool)](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontroller(_:setplaying:))
- [func pictureInPictureControllerTimeRangeForPlayback(AVPictureInPictureController) -> CMTimeRange](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontrollertimerangeforplayback(_:))
- [func pictureInPictureControllerIsPlaybackPaused(AVPictureInPictureController) -> Bool](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontrollerisplaybackpaused(_:))
- [func pictureInPictureController(AVPictureInPictureController, didTransitionToRenderSize: CMVideoDimensions)](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontroller(_:didtransitiontorendersize:))
- [func pictureInPictureController(AVPictureInPictureController, skipByInterval: CMTime, completion: () -> Void)](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontroller(_:skipbyinterval:completion:))
- [func pictureInPictureControllerShouldProhibitBackgroundAudioPlayback(AVPictureInPictureController) -> Bool](/documentation/avkit/avpictureinpicturesamplebufferplaybackdelegate/pictureinpicturecontrollershouldprohibitbackgroundaudioplayback(_:))

#### Invalidating State

- [func invalidatePlaybackState()](/documentation/avkit/avpictureinpicturecontroller/invalidateplaybackstate())

### Accessing the Player Layer

- [var playerLayer: AVPlayerLayer](/documentation/avkit/avpictureinpicturecontroller/playerlayer)

### Configuring Playback Behavior

- [var requiresLinearPlayback: Bool](/documentation/avkit/avpictureinpicturecontroller/requireslinearplayback)

### Accessing the Delegate Object

- [var delegate: (any AVPictureInPictureControllerDelegate)?](/documentation/avkit/avpictureinpicturecontroller/delegate)
- [AVPictureInPictureControllerDelegate](/documentation/avkit/avpictureinpicturecontrollerdelegate)

#### Restoring the User Interface

- [func pictureInPictureController(AVPictureInPictureController, restoreUserInterfaceForPictureInPictureStopWithCompletionHandler: (Bool) -> Void)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontroller(_:restoreuserinterfaceforpictureinpicturestopwithcompletionhandler:))

#### Responding to Picture in Picture Lifecycle Events

- [func pictureInPictureControllerWillStartPictureInPicture(AVPictureInPictureController)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontrollerwillstartpictureinpicture(_:))
- [func pictureInPictureControllerDidStartPictureInPicture(AVPictureInPictureController)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontrollerdidstartpictureinpicture(_:))
- [func pictureInPictureController(AVPictureInPictureController, failedToStartPictureInPictureWithError: any Error)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontroller(_:failedtostartpictureinpicturewitherror:))
- [func pictureInPictureControllerWillStopPictureInPicture(AVPictureInPictureController)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontrollerwillstoppictureinpicture(_:))
- [func pictureInPictureControllerDidStopPictureInPicture(AVPictureInPictureController)](/documentation/avkit/avpictureinpicturecontrollerdelegate/pictureinpicturecontrollerdidstoppictureinpicture(_:))

### Accessing Picture in Picture State

- [class func isPictureInPictureSupported() -> Bool](/documentation/avkit/avpictureinpicturecontroller/ispictureinpicturesupported())
- [var isPictureInPicturePossible: Bool](/documentation/avkit/avpictureinpicturecontroller/ispictureinpicturepossible)
- [var isPictureInPictureActive: Bool](/documentation/avkit/avpictureinpicturecontroller/ispictureinpictureactive)
- [var isPictureInPictureSuspended: Bool](/documentation/avkit/avpictureinpicturecontroller/ispictureinpicturesuspended)

### Controlling Picture in Picture Playback

- [var canStopPictureInPicture: Bool](/documentation/avkit/avpictureinpicturecontroller/canstoppictureinpicture)
- [var canStartPictureInPictureAutomaticallyFromInline: Bool](/documentation/avkit/avpictureinpicturecontroller/canstartpictureinpictureautomaticallyfrominline)
- [func startPictureInPicture()](/documentation/avkit/avpictureinpicturecontroller/startpictureinpicture())
- [func stopPictureInPicture()](/documentation/avkit/avpictureinpicturecontroller/stoppictureinpicture())

### Retrieving Picture in Picture Template Images

- [class var pictureInPictureButtonStartImage: UIImage](/documentation/avkit/avpictureinpicturecontroller/pictureinpicturebuttonstartimage)
- [class var pictureInPictureButtonStopImage: UIImage](/documentation/avkit/avpictureinpicturecontroller/pictureinpicturebuttonstopimage)
- [class func pictureInPictureButtonStartImage(compatibleWith: UITraitCollection?) -> UIImage](/documentation/avkit/avpictureinpicturecontroller/pictureinpicturebuttonstartimage(compatiblewith:))
- [class func pictureInPictureButtonStopImage(compatibleWith: UITraitCollection?) -> UIImage](/documentation/avkit/avpictureinpicturecontroller/pictureinpicturebuttonstopimage(compatiblewith:))

### Instance Methods

- [func invalidatePlaybackState()](/documentation/avkit/avpictureinpicturecontroller/invalidateplaybackstate())

## Playback route selection

- [AVRoutePickerView](/documentation/avkit/avroutepickerview)

### Configuring the delegate

- [var delegate: (any AVRoutePickerViewDelegate)?](/documentation/avkit/avroutepickerview/delegate)
- [AVRoutePickerViewDelegate](/documentation/avkit/avroutepickerviewdelegate)

#### Presenting Routes

- [func routePickerViewWillBeginPresentingRoutes(AVRoutePickerView)](/documentation/avkit/avroutepickerviewdelegate/routepickerviewwillbeginpresentingroutes(_:))
- [func routePickerViewDidEndPresentingRoutes(AVRoutePickerView)](/documentation/avkit/avroutepickerviewdelegate/routepickerviewdidendpresentingroutes(_:))

### Configuring the route picker view

- [var activeTintColor: UIColor!](/documentation/avkit/avroutepickerview/activetintcolor)
- [var isRoutePickerButtonBordered: Bool](/documentation/avkit/avroutepickerview/isroutepickerbuttonbordered)
- [var prioritizesVideoDevices: Bool](/documentation/avkit/avroutepickerview/prioritizesvideodevices)
- [var routePickerButtonStyle: AVRoutePickerViewButtonStyle](/documentation/avkit/avroutepickerview/routepickerbuttonstyle)
- [AVRoutePickerViewButtonStyle](/documentation/avkit/avroutepickerviewbuttonstyle)

#### Button Styles

- [case custom](/documentation/avkit/avroutepickerviewbuttonstyle/custom)
- [case plain](/documentation/avkit/avroutepickerviewbuttonstyle/plain)
- [case system](/documentation/avkit/avroutepickerviewbuttonstyle/system)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avroutepickerviewbuttonstyle/init(rawvalue:))
- [func routePickerButtonColor(for: AVRoutePickerView.ButtonState) -> NSColor](/documentation/avkit/avroutepickerview/routepickerbuttoncolor(for:))
- [func setRoutePickerButtonColor(NSColor?, for: AVRoutePickerView.ButtonState)](/documentation/avkit/avroutepickerview/setroutepickerbuttoncolor(_:for:))
- [AVRoutePickerView.ButtonState](/documentation/avkit/avroutepickerview/buttonstate)

#### Button States

- [case normal](/documentation/avkit/avroutepickerview/buttonstate/normal)
- [case normalHighlighted](/documentation/avkit/avroutepickerview/buttonstate/normalhighlighted)
- [case active](/documentation/avkit/avroutepickerview/buttonstate/active)
- [case activeHighlighted](/documentation/avkit/avroutepickerview/buttonstate/activehighlighted)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avroutepickerview/buttonstate/init(rawvalue:))

### Accessing the player

- [var player: AVPlayer?](/documentation/avkit/avroutepickerview/player)

### Setting a custom routing controller

- [var customRoutingController: AVCustomRoutingController?](/documentation/avkit/avroutepickerview/customroutingcontroller)

## Metadata

- [AVKit Metadata Identifiers](/documentation/avkit/avkit-metadata-identifiers)

### Displayed Metadata

- [let AVKitMetadataIdentifierExactStartDate: String](/documentation/avkit/avkitmetadataidentifierexactstartdate)
- [let AVKitMetadataIdentifierExactEndDate: String](/documentation/avkit/avkitmetadataidentifierexactenddate)
- [let AVKitMetadataIdentifierApproximateStartDate: String](/documentation/avkit/avkitmetadataidentifierapproximatestartdate)
- [let AVKitMetadataIdentifierApproximateEndDate: String](/documentation/avkit/avkitmetadataidentifierapproximateenddate)

### Nondisplayed Metadata

- [let AVKitMetadataIdentifierPlaybackProgress: String](/documentation/avkit/avkitmetadataidentifierplaybackprogress)
- [let AVKitMetadataIdentifierExternalContentIdentifier: String](/documentation/avkit/avkitmetadataidentifierexternalcontentidentifier)
- [let AVKitMetadataIdentifierExternalUserProfileIdentifier: String](/documentation/avkit/avkitmetadataidentifierexternaluserprofileidentifier)
- [let AVKitMetadataIdentifierServiceIdentifier: String](/documentation/avkit/avkitmetadataidentifierserviceidentifier)

## Errors

- [let AVKitErrorDomain: String](/documentation/avkit/avkiterrordomain)
- [AVKitError](/documentation/avkit/avkiterror-swift.struct)

### Inspecting an Error

- [static var errorDomain: String](/documentation/avkit/avkiterror-swift.struct/errordomain)
- [AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/code)

#### Error Codes

- [case unknown](/documentation/avkit/avkiterror-swift.struct/code/unknown)
- [case contentRatingUnknown](/documentation/avkit/avkiterror-swift.struct/code/contentratingunknown)
- [case contentDisallowedByPasscode](/documentation/avkit/avkiterror-swift.struct/code/contentdisallowedbypasscode)
- [case pictureInPictureStartFailed](/documentation/avkit/avkiterror-swift.struct/code/pictureinpicturestartfailed)
- [case contentDisallowedByProfile](/documentation/avkit/avkiterror-swift.struct/code/contentdisallowedbyprofile)

#### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avkiterror-swift.struct/code/init(rawvalue:))
- [Error Constants](/documentation/avkit/error-constants)

#### Error Code Constants

- [static var unknown: AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/unknown)
- [static var contentRatingUnknown: AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/contentratingunknown)
- [static var contentDisallowedByPasscode: AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/contentdisallowedbypasscode)
- [static var contentDisallowedByProfile: AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/contentdisallowedbyprofile)
- [static var pictureInPictureStartFailed: AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/pictureinpicturestartfailed)
- [AVKitError.Code](/documentation/avkit/avkiterror-swift.struct/code)

### Error Codes

- [case unknown](/documentation/avkit/avkiterror-swift.struct/code/unknown)
- [case contentRatingUnknown](/documentation/avkit/avkiterror-swift.struct/code/contentratingunknown)
- [case contentDisallowedByPasscode](/documentation/avkit/avkiterror-swift.struct/code/contentdisallowedbypasscode)
- [case pictureInPictureStartFailed](/documentation/avkit/avkiterror-swift.struct/code/pictureinpicturestartfailed)
- [case contentDisallowedByProfile](/documentation/avkit/avkiterror-swift.struct/code/contentdisallowedbyprofile)

### Initializers

- [init?(rawValue: Int)](/documentation/avkit/avkiterror-swift.struct/code/init(rawvalue:))

## Macros

- [Macros](/documentation/avkit/avkit-macros)

### Macros

- [var PLATFORM_SUPPORTS_AVKITCORE: Bool](/documentation/avkit/platform_supports_avkitcore)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
