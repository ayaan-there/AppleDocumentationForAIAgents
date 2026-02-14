# Media Accessibility Documentation

Source: https://sosumi.ai/documentation/mediaaccessibility

---
title: Media Accessibility
source: https://developer.apple.com/documentation/mediaaccessibility
timestamp: 2026-02-13T18:59:20.900Z
---

## Features

- [Captions](/documentation/mediaaccessibility/captions)

### General settings

- [let kMACaptionAppearanceSettingsChangedNotification: CFString](/documentation/mediaaccessibility/kmacaptionappearancesettingschangednotification)
- [func MACaptionAppearanceDidDisplayCaptions(CFArray)](/documentation/mediaaccessibility/macaptionappearancediddisplaycaptions(_:))
- [func MACaptionAppearanceCopyPreferredCaptioningMediaCharacteristics(MACaptionAppearanceDomain) -> Unmanaged<CFArray>](/documentation/mediaaccessibility/macaptionappearancecopypreferredcaptioningmediacharacteristics(_:))
- [func MACaptionAppearanceGetDisplayType(MACaptionAppearanceDomain) -> MACaptionAppearanceDisplayType](/documentation/mediaaccessibility/macaptionappearancegetdisplaytype(_:))
- [func MACaptionAppearanceSetDisplayType(MACaptionAppearanceDomain, MACaptionAppearanceDisplayType)](/documentation/mediaaccessibility/macaptionappearancesetdisplaytype(_:_:))

### Language settings

- [func MACaptionAppearanceAddSelectedLanguage(MACaptionAppearanceDomain, CFString) -> Bool](/documentation/mediaaccessibility/macaptionappearanceaddselectedlanguage(_:_:))
- [func MACaptionAppearanceCopySelectedLanguages(MACaptionAppearanceDomain) -> Unmanaged<CFArray>](/documentation/mediaaccessibility/macaptionappearancecopyselectedlanguages(_:))

### Text settings

- [func MACaptionAppearanceCopyFontDescriptorForStyle(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?, MACaptionAppearanceFontStyle) -> Unmanaged<CTFontDescriptor>](/documentation/mediaaccessibility/macaptionappearancecopyfontdescriptorforstyle(_:_:_:))
- [func MACaptionAppearanceCopyForegroundColor(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> Unmanaged<CGColor>](/documentation/mediaaccessibility/macaptionappearancecopyforegroundcolor(_:_:))
- [func MACaptionAppearanceGetForegroundOpacity(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> CGFloat](/documentation/mediaaccessibility/macaptionappearancegetforegroundopacity(_:_:))
- [func MACaptionAppearanceGetRelativeCharacterSize(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> CGFloat](/documentation/mediaaccessibility/macaptionappearancegetrelativecharactersize(_:_:))
- [func MACaptionAppearanceGetTextEdgeStyle(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> MACaptionAppearanceTextEdgeStyle](/documentation/mediaaccessibility/macaptionappearancegettextedgestyle(_:_:))

### Text highlight settings

- [func MACaptionAppearanceCopyBackgroundColor(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> Unmanaged<CGColor>](/documentation/mediaaccessibility/macaptionappearancecopybackgroundcolor(_:_:))
- [func MACaptionAppearanceGetBackgroundOpacity(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> CGFloat](/documentation/mediaaccessibility/macaptionappearancegetbackgroundopacity(_:_:))

### Caption window settings

- [func MACaptionAppearanceCopyWindowColor(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> Unmanaged<CGColor>](/documentation/mediaaccessibility/macaptionappearancecopywindowcolor(_:_:))
- [func MACaptionAppearanceGetWindowOpacity(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> CGFloat](/documentation/mediaaccessibility/macaptionappearancegetwindowopacity(_:_:))
- [func MACaptionAppearanceGetWindowRoundedCornerRadius(MACaptionAppearanceDomain, UnsafeMutablePointer<MACaptionAppearanceBehavior>?) -> CGFloat](/documentation/mediaaccessibility/macaptionappearancegetwindowroundedcornerradius(_:_:))

### Image captioning settings

- [func MAImageCaptioningCopyCaption(CFURL, UnsafeMutablePointer<CFError?>?) -> CFString?](/documentation/mediaaccessibility/maimagecaptioningcopycaption(_:_:))
- [func MAImageCaptioningSetCaption(CFURL, CFString?, UnsafeMutablePointer<CFError?>?) -> Bool](/documentation/mediaaccessibility/maimagecaptioningsetcaption(_:_:_:))
- [func MAImageCaptioningCopyMetadataTagPath() -> CFString](/documentation/mediaaccessibility/maimagecaptioningcopymetadatatagpath())

### Audible media selection settings

- [let kMAAudibleMediaSettingsChangedNotification: CFString](/documentation/mediaaccessibility/kmaaudiblemediasettingschangednotification)
- [func MAAudibleMediaCopyPreferredCharacteristics() -> Unmanaged<CFArray>](/documentation/mediaaccessibility/maaudiblemediacopypreferredcharacteristics())
- [let MAMediaCharacteristicDescribesVideoForAccessibility: CFString](/documentation/mediaaccessibility/mamediacharacteristicdescribesvideoforaccessibility)
- [let MAMediaCharacteristicDescribesMusicAndSoundForAccessibility: CFString](/documentation/mediaaccessibility/mamediacharacteristicdescribesmusicandsoundforaccessibility)
- [let MAMediaCharacteristicTranscribesSpokenDialogForAccessibility: CFString](/documentation/mediaaccessibility/mamediacharacteristictranscribesspokendialogforaccessibility)

### Profile settings

- [func MACaptionAppearanceCopyProfileIDs() -> CFArray](/documentation/mediaaccessibility/macaptionappearancecopyprofileids())
- [func MACaptionAppearanceSetActiveProfileID(CFString)](/documentation/mediaaccessibility/macaptionappearancesetactiveprofileid(_:))
- [func MACaptionAppearanceCopyActiveProfileID() -> CFString](/documentation/mediaaccessibility/macaptionappearancecopyactiveprofileid())
- [func MACaptionAppearanceCopyProfileName(CFString) -> CFString](/documentation/mediaaccessibility/macaptionappearancecopyprofilename(_:))
- [func MACaptionAppearanceExecuteBlockForProfileID(CFString, () -> Void)](/documentation/mediaaccessibility/macaptionappearanceexecuteblockforprofileid(_:_:))

### Customization status

- [func MACaptionAppearanceIsCustomized(MACaptionAppearanceDomain) -> Bool](/documentation/mediaaccessibility/macaptionappearanceiscustomized(_:))

### Constants

- [MACaptionAppearanceDomain](/documentation/mediaaccessibility/macaptionappearancedomain)

#### Constants

- [case `default`](/documentation/mediaaccessibility/macaptionappearancedomain/default)
- [case user](/documentation/mediaaccessibility/macaptionappearancedomain/user)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/mediaaccessibility/macaptionappearancedomain/init(rawvalue:))
- [MACaptionAppearanceDisplayType](/documentation/mediaaccessibility/macaptionappearancedisplaytype)

#### Constants

- [case forcedOnly](/documentation/mediaaccessibility/macaptionappearancedisplaytype/forcedonly)
- [case automatic](/documentation/mediaaccessibility/macaptionappearancedisplaytype/automatic)
- [case alwaysOn](/documentation/mediaaccessibility/macaptionappearancedisplaytype/alwayson)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/mediaaccessibility/macaptionappearancedisplaytype/init(rawvalue:))
- [MACaptionAppearanceBehavior](/documentation/mediaaccessibility/macaptionappearancebehavior)

#### Constants

- [case useValue](/documentation/mediaaccessibility/macaptionappearancebehavior/usevalue)
- [case useContentIfAvailable](/documentation/mediaaccessibility/macaptionappearancebehavior/usecontentifavailable)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/mediaaccessibility/macaptionappearancebehavior/init(rawvalue:))
- [MACaptionAppearanceFontStyle](/documentation/mediaaccessibility/macaptionappearancefontstyle)

#### Constants

- [case `default`](/documentation/mediaaccessibility/macaptionappearancefontstyle/default)
- [case monospacedWithSerif](/documentation/mediaaccessibility/macaptionappearancefontstyle/monospacedwithserif)
- [case proportionalWithSerif](/documentation/mediaaccessibility/macaptionappearancefontstyle/proportionalwithserif)
- [case monospacedWithoutSerif](/documentation/mediaaccessibility/macaptionappearancefontstyle/monospacedwithoutserif)
- [case proportionalWithoutSerif](/documentation/mediaaccessibility/macaptionappearancefontstyle/proportionalwithoutserif)
- [case casual](/documentation/mediaaccessibility/macaptionappearancefontstyle/casual)
- [case cursive](/documentation/mediaaccessibility/macaptionappearancefontstyle/cursive)
- [case smallCapital](/documentation/mediaaccessibility/macaptionappearancefontstyle/smallcapital)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/mediaaccessibility/macaptionappearancefontstyle/init(rawvalue:))
- [MACaptionAppearanceTextEdgeStyle](/documentation/mediaaccessibility/macaptionappearancetextedgestyle)

#### Constants

- [case undefined](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/undefined)
- [case none](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/none)
- [case raised](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/raised)
- [case depressed](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/depressed)
- [case uniform](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/uniform)
- [case dropShadow](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/dropshadow)

#### Initializers

- [init?(rawValue: CFIndex)](/documentation/mediaaccessibility/macaptionappearancetextedgestyle/init(rawvalue:))
- [Flashing lights](/documentation/mediaaccessibility/flashing-lights)

### Dim flashing lights

- [Responding to changes in the flashing lights setting](/documentation/mediaaccessibility/responding-to-changes-in-the-flashing-lights-setting)
- [func MADimFlashingLightsEnabled() -> Bool](/documentation/mediaaccessibility/madimflashinglightsenabled())
- [let kMADimFlashingLightsChangedNotification: CFString](/documentation/mediaaccessibility/kmadimflashinglightschangednotification)
- [MAFlashingLightsProcessor](/documentation/mediaaccessibility/maflashinglightsprocessor)

#### Checking compatibility

- [func canProcessSurface(IOSurfaceRef) -> Bool](/documentation/mediaaccessibility/maflashinglightsprocessor/canprocesssurface(_:))

#### Processing video content

- [func processSurface(IOSurfaceRef, outSurface: inout IOSurfaceRef, timestamp: CFAbsoluteTime, options: [MAFlashingLightsProcessor.OptionKey : Any]?) -> MAFlashingLightsProcessor.Result](/documentation/mediaaccessibility/maflashinglightsprocessor/processsurface(_:outsurface:timestamp:options:))
- [MAFlashingLightsProcessor.Result](/documentation/mediaaccessibility/maflashinglightsprocessor/result)

##### Interpreting results from video processing

- [var surfaceProcessed: Bool](/documentation/mediaaccessibility/maflashinglightsprocessor/result/surfaceprocessed)
- [var intensityLevel: Float](/documentation/mediaaccessibility/maflashinglightsprocessor/result/intensitylevel)
- [var mitigationLevel: Float](/documentation/mediaaccessibility/maflashinglightsprocessor/result/mitigationlevel)
- [MAFlashingLightsProcessor.OptionKey](/documentation/mediaaccessibility/maflashinglightsprocessor/optionkey)

##### Creating an options structure

- [init(String)](/documentation/mediaaccessibility/maflashinglightsprocessor/optionkey/init(_:))
- [init(rawValue: String)](/documentation/mediaaccessibility/maflashinglightsprocessor/optionkey/init(rawvalue:))
- [Music Haptics](/documentation/mediaaccessibility/music-haptics)

### Music Haptics

- [MAMusicHapticsManager](/documentation/mediaaccessibility/mamusichapticsmanager)

#### Getting the shared haptics manager

- [class var shared: MAMusicHapticsManager](/documentation/mediaaccessibility/mamusichapticsmanager/shared)

#### Checking if Music Haptics is on

- [var isActive: Bool](/documentation/mediaaccessibility/mamusichapticsmanager/isactive)
- [class let activeStatusDidChangeNotification: NSNotification.Name](/documentation/mediaaccessibility/mamusichapticsmanager/activestatusdidchangenotification)

#### Checking haptic track availability

- [func checkHapticTrackAvailabilityForMedia(matchingCode: String, completionHandler: ((Bool) -> Void)?)](/documentation/mediaaccessibility/mamusichapticsmanager/checkhaptictrackavailabilityformedia(matchingcode:completionhandler:))

#### Observing haptic playback

- [func addStatusObserver((String, Bool) -> Void) -> (any NSCopying)?](/documentation/mediaaccessibility/mamusichapticsmanager/addstatusobserver(_:))
- [func removeStatusObserver(any NSCopying)](/documentation/mediaaccessibility/mamusichapticsmanager/removestatusobserver(_:))

#### Supporting types

- [MAMusicHaptics](/documentation/mediaaccessibility/mamusichaptics)

##### Initializers

- [init()](/documentation/mediaaccessibility/mamusichaptics/init())

##### Type Properties

- [static var enabledStatusDidChangeNotification: Notification.Name](/documentation/mediaaccessibility/mamusichaptics/enabledstatusdidchangenotification)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
