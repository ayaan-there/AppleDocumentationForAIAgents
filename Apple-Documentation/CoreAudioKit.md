# CoreAudioKit Documentation

Source: https://sosumi.ai/documentation/coreaudiokit

---
title: CoreAudioKit
source: https://developer.apple.com/documentation/coreaudiokit
timestamp: 2026-02-13T18:55:54.191Z
---

## Audio Units

- [AUViewController](/documentation/coreaudiokit/auviewcontroller)
- [AUAudioUnitViewConfiguration](/documentation/coreaudiokit/auaudiounitviewconfiguration)

### Creating a Configuration

- [init(width: CGFloat, height: CGFloat, hostHasController: Bool)](/documentation/coreaudiokit/auaudiounitviewconfiguration/init(width:height:hosthascontroller:))

### Accessing Settings

- [var width: CGFloat](/documentation/coreaudiokit/auaudiounitviewconfiguration/width)
- [var height: CGFloat](/documentation/coreaudiokit/auaudiounitviewconfiguration/height)
- [var hostHasController: Bool](/documentation/coreaudiokit/auaudiounitviewconfiguration/hosthascontroller)
- [AUGenericView](/documentation/coreaudiokit/augenericview)

### Creating a Generic View

- [init(audioUnit: AudioUnit)](/documentation/coreaudiokit/augenericview/init(audiounit:))
- [init(audioUnit: AudioUnit, displayFlags: AUGenericViewDisplayFlags)](/documentation/coreaudiokit/augenericview/init(audiounit:displayflags:))

#### Display Flags

- [AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags)

##### Display Flags

- [static var viewParametersDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewparametersdisplayflag)
- [static var viewPropertiesDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewpropertiesdisplayflag)
- [static var viewTitleDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewtitledisplayflag)

##### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiokit/augenericviewdisplayflags/init(rawvalue:))

### Configuring a View

- [var showsExpertParameters: Bool](/documentation/coreaudiokit/augenericview/showsexpertparameters)

### Accessing the Audio Unit

- [var audioUnit: AudioUnit](/documentation/coreaudiokit/augenericview/audiounit)
- [AUPannerView](/documentation/coreaudiokit/aupannerview)

### Creating a Panner View

- [init(audioUnit: AudioUnit)](/documentation/coreaudiokit/aupannerview/init(audiounit:))

### Accessing the Audio Unit

- [var audioUnit: AudioUnit](/documentation/coreaudiokit/aupannerview/audiounit)
- [AUCustomViewPersistentData](/documentation/coreaudiokit/aucustomviewpersistentdata)

### Accessing View State

- [var customViewPersistentData: NSDictionary?](/documentation/coreaudiokit/aucustomviewpersistentdata/customviewpersistentdata)

## Bluetooth Devices

- [CABTLEMIDIWindowController](/documentation/coreaudiokit/cabtlemidiwindowcontroller)
- [CABTMIDICentralViewController](/documentation/coreaudiokit/cabtmidicentralviewcontroller)
- [CABTMIDILocalPeripheralViewController](/documentation/coreaudiokit/cabtmidilocalperipheralviewcontroller)

## Network Devices

- [CANetworkBrowserWindowController](/documentation/coreaudiokit/canetworkbrowserwindowcontroller)

### Creating a Window Controller

- [init()](/documentation/coreaudiokit/canetworkbrowserwindowcontroller/init())

### Determining Audio Video Bridging (AVB) Support

- [class func isAVBSupported() -> Bool](/documentation/coreaudiokit/canetworkbrowserwindowcontroller/isavbsupported())

## Inter-Device Audio

- [CAInterDeviceAudioViewController](/documentation/coreaudiokit/cainterdeviceaudioviewcontroller)

## Inter-App Audio

- [CAInterAppAudioSwitcherView](/documentation/coreaudiokit/cainterappaudioswitcherview)

### Configuring the View

- [var isShowingAppNames: Bool](/documentation/coreaudiokit/cainterappaudioswitcherview/isshowingappnames)
- [func contentWidth() -> CGFloat](/documentation/coreaudiokit/cainterappaudioswitcherview/contentwidth())
- [func setOutputAudioUnit(AudioUnit?)](/documentation/coreaudiokit/cainterappaudioswitcherview/setoutputaudiounit(_:))
- [CAInterAppAudioTransportView](/documentation/coreaudiokit/cainterappaudiotransportview)

### Configuring the View

- [var isConnected: Bool](/documentation/coreaudiokit/cainterappaudiotransportview/isconnected)
- [var currentTimeLabelFont: UIFont](/documentation/coreaudiokit/cainterappaudiotransportview/currenttimelabelfont)
- [var isEnabled: Bool](/documentation/coreaudiokit/cainterappaudiotransportview/isenabled)
- [var labelColor: UIColor](/documentation/coreaudiokit/cainterappaudiotransportview/labelcolor)
- [var pauseButtonColor: UIColor](/documentation/coreaudiokit/cainterappaudiotransportview/pausebuttoncolor)
- [var playButtonColor: UIColor](/documentation/coreaudiokit/cainterappaudiotransportview/playbuttoncolor)
- [var isPlaying: Bool](/documentation/coreaudiokit/cainterappaudiotransportview/isplaying)
- [var recordButtonColor: UIColor](/documentation/coreaudiokit/cainterappaudiotransportview/recordbuttoncolor)
- [var isRecording: Bool](/documentation/coreaudiokit/cainterappaudiotransportview/isrecording)
- [var rewindButtonColor: UIColor](/documentation/coreaudiokit/cainterappaudiotransportview/rewindbuttoncolor)
- [func setOutputAudioUnit(AudioUnit)](/documentation/coreaudiokit/cainterappaudiotransportview/setoutputaudiounit(_:))

## Deprecations

- [AUGenericViewInternal](/documentation/coreaudiokit/augenericviewinternal)

### Initializers

- [init?(coder: NSCoder)](/documentation/coreaudiokit/augenericviewinternal/init(coder:))
- [init(frame: CGRect)](/documentation/coreaudiokit/augenericviewinternal/init(frame:))

### Instance Properties

- [var auAudioUnit: AUAudioUnit?](/documentation/coreaudiokit/augenericviewinternal/auaudiounit)
- [var owningController: UIViewController?](/documentation/coreaudiokit/augenericviewinternal/owningcontroller)
- [var paramObserverToken: AUParameterObserverToken?](/documentation/coreaudiokit/augenericviewinternal/paramobservertoken)
- [var showSingleClumpIndex: Int?](/documentation/coreaudiokit/augenericviewinternal/showsingleclumpindex)

### Instance Methods

- [func removeFromSuperview()](/documentation/coreaudiokit/augenericviewinternal/removefromsuperview())
- [func removeScheduledUpdatesTimer()](/documentation/coreaudiokit/augenericviewinternal/removescheduledupdatestimer())
- [func traitCollectionDidChange(UITraitCollection?)](/documentation/coreaudiokit/augenericviewinternal/traitcollectiondidchange(_:))
- [AUGenericViewInternalBase](/documentation/coreaudiokit/augenericviewinternalbase)

## Classes

- [AUAppleCustomViewLoader](/documentation/coreaudiokit/auapplecustomviewloader)

### Initializers

- [init()](/documentation/coreaudiokit/auapplecustomviewloader/init())

### Instance Methods

- [func customViewController(for: AudioComponentDescription, audioUnit: AudioUnit, v3AU: AUAudioUnit?) -> UIViewController?](/documentation/coreaudiokit/auapplecustomviewloader/customviewcontroller(for:audiounit:v3au:))
- [AUGenericViewController](/documentation/coreaudiokit/augenericviewcontroller)

### Instance Properties

- [var auAudioUnit: AUAudioUnit?](/documentation/coreaudiokit/augenericviewcontroller/auaudiounit)

## Structures

- [AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags)

### Display Flags

- [static var viewParametersDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewparametersdisplayflag)
- [static var viewPropertiesDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewpropertiesdisplayflag)
- [static var viewTitleDisplayFlag: AUGenericViewDisplayFlags](/documentation/coreaudiokit/augenericviewdisplayflags/viewtitledisplayflag)

### Initializers

- [init(rawValue: UInt32)](/documentation/coreaudiokit/augenericviewdisplayflags/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
