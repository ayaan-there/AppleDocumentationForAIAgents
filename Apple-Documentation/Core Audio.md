# Core Audio Documentation

Source: https://sosumi.ai/documentation/coreaudio

---
title: Core Audio
source: https://developer.apple.com/documentation/coreaudio
timestamp: 2026-02-13T18:55:10.115Z
---

## Drivers

- [Creating an Audio Server Driver Plug-in](/documentation/coreaudio/creating-an-audio-server-driver-plug-in)
- [Building an Audio Server Plug-in and Driver Extension](/documentation/coreaudio/building-an-audio-server-plug-in-and-driver-extension)
- [Capturing system audio with Core Audio taps](/documentation/coreaudio/capturing-system-audio-with-core-audio-taps)

## Reference

- [Core Audio Structures](/documentation/coreaudio/core-audio-structures)

### Structures

- [AudioHardwareIOProcStreamUsage](/documentation/coreaudio/audiohardwareioprocstreamusage)

#### Initializers

- [init(mIOProc: UnsafeMutableRawPointer, mNumberStreams: UInt32, mStreamIsOn: UInt32)](/documentation/coreaudio/audiohardwareioprocstreamusage/init(mioproc:mnumberstreams:mstreamison:))

#### Instance Properties

- [var mIOProc: UnsafeMutableRawPointer](/documentation/coreaudio/audiohardwareioprocstreamusage/mioproc)
- [var mNumberStreams: UInt32](/documentation/coreaudio/audiohardwareioprocstreamusage/mnumberstreams)
- [var mStreamIsOn: UInt32](/documentation/coreaudio/audiohardwareioprocstreamusage/mstreamison)
- [AudioObjectPropertyAddress](/documentation/coreaudio/audioobjectpropertyaddress)

#### Initializers

- [init()](/documentation/coreaudio/audioobjectpropertyaddress/init())
- [init(mSelector: AudioObjectPropertySelector, mScope: AudioObjectPropertyScope, mElement: AudioObjectPropertyElement)](/documentation/coreaudio/audioobjectpropertyaddress/init(mselector:mscope:melement:))

#### Instance Properties

- [var mElement: AudioObjectPropertyElement](/documentation/coreaudio/audioobjectpropertyaddress/melement)
- [var mScope: AudioObjectPropertyScope](/documentation/coreaudio/audioobjectpropertyaddress/mscope)
- [var mSelector: AudioObjectPropertySelector](/documentation/coreaudio/audioobjectpropertyaddress/mselector)
- [AudioStreamRangedDescription](/documentation/coreaudio/audiostreamrangeddescription)

#### Initializers

- [init()](/documentation/coreaudio/audiostreamrangeddescription/init())
- [init(mFormat: AudioStreamBasicDescription, mSampleRateRange: AudioValueRange)](/documentation/coreaudio/audiostreamrangeddescription/init(mformat:msampleraterange:))

#### Instance Properties

- [var mFormat: AudioStreamBasicDescription](/documentation/coreaudio/audiostreamrangeddescription/mformat)
- [var mSampleRateRange: AudioValueRange](/documentation/coreaudio/audiostreamrangeddescription/msampleraterange)
- [UnsafeMutableAudioBufferListPointer](/documentation/coreaudio/unsafemutableaudiobufferlistpointer)

#### Initializers

- [init(UnsafeMutablePointer<AudioBufferList>)](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/init(_:)-4a7c5)
- [init?(UnsafeMutablePointer<AudioBufferList>?)](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/init(_:)-6qwfh)

#### Instance Properties

- [var count: Int](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/count)
- [var unsafeMutablePointer: UnsafeMutablePointer<AudioBufferList>](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/unsafemutablepointer)
- [var unsafePointer: UnsafePointer<AudioBufferList>](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/unsafepointer)

#### Default Implementations

- [MutableCollection Implementations](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/mutablecollection-implementations)

##### Subscripts

- [subscript(UnsafeMutableAudioBufferListPointer.Index) -> UnsafeMutableAudioBufferListPointer.Element](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/subscript(_:))
- [RandomAccessCollection Implementations](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/randomaccesscollection-implementations)

##### Instance Properties

- [var endIndex: Int](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/endindex)
- [var startIndex: Int](/documentation/coreaudio/unsafemutableaudiobufferlistpointer/startindex)
- [Core Audio Data Types](/documentation/coreaudio/core-audio-data-types)

### Data Types

- [AudioClassID](/documentation/coreaudio/audioclassid)
- [AudioDeviceID](/documentation/coreaudio/audiodeviceid)
- [AudioDeviceIOBlock](/documentation/coreaudio/audiodeviceioblock)
- [AudioDeviceIOProc](/documentation/coreaudio/audiodeviceioproc)
- [AudioDeviceIOProcID](/documentation/coreaudio/audiodeviceioprocid)
- [AudioDevicePropertyID](/documentation/coreaudio/audiodevicepropertyid)
- [AudioDevicePropertyListenerProc](/documentation/coreaudio/audiodevicepropertylistenerproc)
- [AudioHardwarePropertyID](/documentation/coreaudio/audiohardwarepropertyid)
- [AudioHardwarePropertyListenerProc](/documentation/coreaudio/audiohardwarepropertylistenerproc)
- [AudioObjectID](/documentation/coreaudio/audioobjectid)
- [AudioObjectPropertyElement](/documentation/coreaudio/audioobjectpropertyelement)
- [AudioObjectPropertyListenerBlock](/documentation/coreaudio/audioobjectpropertylistenerblock)
- [AudioObjectPropertyListenerProc](/documentation/coreaudio/audioobjectpropertylistenerproc)
- [AudioObjectPropertyScope](/documentation/coreaudio/audioobjectpropertyscope)
- [AudioObjectPropertySelector](/documentation/coreaudio/audioobjectpropertyselector)
- [AudioStreamID](/documentation/coreaudio/audiostreamid)
- [AudioStreamPropertyListenerProc](/documentation/coreaudio/audiostreampropertylistenerproc)
- [Core Audio Functions](/documentation/coreaudio/core-audio-functions)

### Functions

- [func AudioConvertHostTimeToNanos(UInt64) -> UInt64](/documentation/coreaudio/audioconverthosttimetonanos(_:))
- [func AudioConvertNanosToHostTime(UInt64) -> UInt64](/documentation/coreaudio/audioconvertnanostohosttime(_:))
- [func AudioDeviceCreateIOProcID(AudioObjectID, AudioDeviceIOProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<AudioDeviceIOProcID?>) -> OSStatus](/documentation/coreaudio/audiodevicecreateioprocid(_:_:_:_:))
- [func AudioDeviceCreateIOProcIDWithBlock(UnsafeMutablePointer<AudioDeviceIOProcID?>, AudioObjectID, dispatch_queue_t?, AudioDeviceIOBlock) -> OSStatus](/documentation/coreaudio/audiodevicecreateioprocidwithblock(_:_:_:_:))
- [func AudioDeviceDestroyIOProcID(AudioObjectID, AudioDeviceIOProcID) -> OSStatus](/documentation/coreaudio/audiodevicedestroyioprocid(_:_:))
- [func AudioDeviceGetCurrentTime(AudioObjectID, UnsafeMutablePointer<AudioTimeStamp>) -> OSStatus](/documentation/coreaudio/audiodevicegetcurrenttime(_:_:))
- [func AudioDeviceGetNearestStartTime(AudioObjectID, UnsafeMutablePointer<AudioTimeStamp>, UInt32) -> OSStatus](/documentation/coreaudio/audiodevicegetneareststarttime(_:_:_:))
- [func AudioDeviceStart(AudioObjectID, AudioDeviceIOProcID?) -> OSStatus](/documentation/coreaudio/audiodevicestart(_:_:))
- [func AudioDeviceStartAtTime(AudioObjectID, AudioDeviceIOProcID?, UnsafeMutablePointer<AudioTimeStamp>, UInt32) -> OSStatus](/documentation/coreaudio/audiodevicestartattime(_:_:_:_:))
- [func AudioDeviceStop(AudioObjectID, AudioDeviceIOProcID?) -> OSStatus](/documentation/coreaudio/audiodevicestop(_:_:))
- [func AudioDeviceTranslateTime(AudioObjectID, UnsafePointer<AudioTimeStamp>, UnsafeMutablePointer<AudioTimeStamp>) -> OSStatus](/documentation/coreaudio/audiodevicetranslatetime(_:_:_:))
- [func AudioGetCurrentHostTime() -> UInt64](/documentation/coreaudio/audiogetcurrenthosttime())
- [func AudioGetHostClockFrequency() -> Float64](/documentation/coreaudio/audiogethostclockfrequency())
- [func AudioGetHostClockMinimumTimeDelta() -> UInt32](/documentation/coreaudio/audiogethostclockminimumtimedelta())
- [func AudioHardwareCreateAggregateDevice(CFDictionary, UnsafeMutablePointer<AudioObjectID>) -> OSStatus](/documentation/coreaudio/audiohardwarecreateaggregatedevice(_:_:))
- [func AudioHardwareDestroyAggregateDevice(AudioObjectID) -> OSStatus](/documentation/coreaudio/audiohardwaredestroyaggregatedevice(_:))
- [func AudioHardwareUnload() -> OSStatus](/documentation/coreaudio/audiohardwareunload())
- [func AudioObjectAddPropertyListener(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, AudioObjectPropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/coreaudio/audioobjectaddpropertylistener(_:_:_:_:))
- [func AudioObjectAddPropertyListenerBlock(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, dispatch_queue_t?, AudioObjectPropertyListenerBlock) -> OSStatus](/documentation/coreaudio/audioobjectaddpropertylistenerblock(_:_:_:_:))
- [func AudioObjectGetPropertyData(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/coreaudio/audioobjectgetpropertydata(_:_:_:_:_:_:))
- [func AudioObjectGetPropertyDataSize(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/coreaudio/audioobjectgetpropertydatasize(_:_:_:_:_:))
- [func AudioObjectHasProperty(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>) -> Bool](/documentation/coreaudio/audioobjecthasproperty(_:_:))
- [func AudioObjectIsPropertySettable(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/coreaudio/audioobjectispropertysettable(_:_:_:))
- [func AudioObjectRemovePropertyListener(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, AudioObjectPropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/coreaudio/audioobjectremovepropertylistener(_:_:_:_:))
- [func AudioObjectRemovePropertyListenerBlock(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, dispatch_queue_t?, AudioObjectPropertyListenerBlock) -> OSStatus](/documentation/coreaudio/audioobjectremovepropertylistenerblock(_:_:_:_:))
- [func AudioObjectSetPropertyData(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>, UInt32, UnsafeRawPointer?, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/coreaudio/audioobjectsetpropertydata(_:_:_:_:_:_:))
- [func AudioObjectShow(AudioObjectID)](/documentation/coreaudio/audioobjectshow(_:))
- [func AudioHardwareCreateProcessTap(CATapDescription!, UnsafeMutablePointer<AudioObjectID>!) -> OSStatus](/documentation/coreaudio/audiohardwarecreateprocesstap(_:_:))
- [func AudioHardwareDestroyProcessTap(AudioObjectID) -> OSStatus](/documentation/coreaudio/audiohardwaredestroyprocesstap(_:))
- [func PropertyAddress(AudioObjectPropertySelector, scope: AudioObjectPropertyScope, element: AudioObjectPropertyElement) -> AudioObjectPropertyAddress](/documentation/coreaudio/propertyaddress(_:scope:element:))
- [Core Audio Constants](/documentation/coreaudio/core-audio-constants)

### Constants

- [var kAudioAggregateDeviceClockDeviceKey: String](/documentation/coreaudio/kaudioaggregatedeviceclockdevicekey)
- [var kAudioAggregateDeviceIsPrivateKey: String](/documentation/coreaudio/kaudioaggregatedeviceisprivatekey)
- [var kAudioAggregateDeviceIsStackedKey: String](/documentation/coreaudio/kaudioaggregatedeviceisstackedkey)
- [var kAudioAggregateDeviceMainSubDeviceKey: String](/documentation/coreaudio/kaudioaggregatedevicemainsubdevicekey)
- [var kAudioAggregateDeviceMasterSubDeviceKey: String](/documentation/coreaudio/kaudioaggregatedevicemastersubdevicekey)
- [var kAudioAggregateDeviceNameKey: String](/documentation/coreaudio/kaudioaggregatedevicenamekey)
- [var kAudioAggregateDevicePropertyMainSubDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertymainsubdevice)
- [var kAudioAggregateDevicePropertySubTapList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertysubtaplist)
- [var kAudioAggregateDevicePropertyTapList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertytaplist)
- [var kAudioAggregateDeviceSubDeviceListKey: String](/documentation/coreaudio/kaudioaggregatedevicesubdevicelistkey)
- [var kAudioAggregateDeviceTapAutoStartKey: String](/documentation/coreaudio/kaudioaggregatedevicetapautostartkey)
- [var kAudioAggregateDeviceTapListKey: String](/documentation/coreaudio/kaudioaggregatedevicetaplistkey)
- [var kAudioAggregateDeviceUIDKey: String](/documentation/coreaudio/kaudioaggregatedeviceuidkey)
- [var kAudioDevicePropertyIOThreadOSWorkgroup: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyiothreadosworkgroup)
- [var kAudioDevicePropertyProcessMute: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyprocessmute)
- [var kAudioDevicePropertyVoiceActivityDetectionEnable: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvoiceactivitydetectionenable)
- [var kAudioDevicePropertyVoiceActivityDetectionState: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvoiceactivitydetectionstate)
- [var kAudioDeviceTransportTypeContinuityCapture: UInt32](/documentation/coreaudio/kaudiodevicetransporttypecontinuitycapture)
- [var kAudioDeviceTransportTypeContinuityCaptureWired: UInt32](/documentation/coreaudio/kaudiodevicetransporttypecontinuitycapturewired)
- [var kAudioDeviceTransportTypeContinuityCaptureWireless: UInt32](/documentation/coreaudio/kaudiodevicetransporttypecontinuitycapturewireless)
- [var kAudioEndPointDeviceEndPointListKey: String](/documentation/coreaudio/kaudioendpointdeviceendpointlistkey)
- [var kAudioEndPointDeviceIsPrivateKey: String](/documentation/coreaudio/kaudioendpointdeviceisprivatekey)
- [var kAudioEndPointDeviceMainEndPointKey: String](/documentation/coreaudio/kaudioendpointdevicemainendpointkey)
- [var kAudioEndPointDeviceMasterEndPointKey: String](/documentation/coreaudio/kaudioendpointdevicemasterendpointkey)
- [var kAudioEndPointDeviceNameKey: String](/documentation/coreaudio/kaudioendpointdevicenamekey)
- [var kAudioEndPointDeviceUIDKey: String](/documentation/coreaudio/kaudioendpointdeviceuidkey)
- [var kAudioEndPointInputChannelsKey: String](/documentation/coreaudio/kaudioendpointinputchannelskey)
- [var kAudioEndPointNameKey: String](/documentation/coreaudio/kaudioendpointnamekey)
- [var kAudioEndPointOutputChannelsKey: String](/documentation/coreaudio/kaudioendpointoutputchannelskey)
- [var kAudioEndPointUIDKey: String](/documentation/coreaudio/kaudioendpointuidkey)
- [var kAudioHardwareNotReadyError: OSStatus](/documentation/coreaudio/kaudiohardwarenotreadyerror)
- [var kAudioHardwarePropertyProcessInputMute: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyprocessinputmute)
- [var kAudioHardwarePropertyProcessIsMain: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyprocessismain)
- [var kAudioHardwarePropertyProcessObjectList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyprocessobjectlist)
- [var kAudioHardwarePropertyTapList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytaplist)
- [var kAudioHardwarePropertyTranslatePIDToProcessObject: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslatepidtoprocessobject)
- [var kAudioHardwarePropertyTranslateUIDToTap: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslateuidtotap)
- [var kAudioHardwareRunLoopMode: String](/documentation/coreaudio/kaudiohardwarerunloopmode)
- [var kAudioObjectPropertyElementMain: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyelementmain)
- [var kAudioProcessClassID: AudioClassID](/documentation/coreaudio/kaudioprocessclassid)
- [var kAudioSubDeviceDriftCompensationKey: String](/documentation/coreaudio/kaudiosubdevicedriftcompensationkey)
- [var kAudioSubDeviceDriftCompensationQualityKey: String](/documentation/coreaudio/kaudiosubdevicedriftcompensationqualitykey)
- [var kAudioSubDeviceExtraInputLatencyKey: String](/documentation/coreaudio/kaudiosubdeviceextrainputlatencykey)
- [var kAudioSubDeviceExtraOutputLatencyKey: String](/documentation/coreaudio/kaudiosubdeviceextraoutputlatencykey)
- [var kAudioSubDeviceInputChannelsKey: String](/documentation/coreaudio/kaudiosubdeviceinputchannelskey)
- [var kAudioSubDeviceNameKey: String](/documentation/coreaudio/kaudiosubdevicenamekey)
- [var kAudioSubDeviceOutputChannelsKey: String](/documentation/coreaudio/kaudiosubdeviceoutputchannelskey)
- [var kAudioSubDeviceUIDKey: String](/documentation/coreaudio/kaudiosubdeviceuidkey)
- [var kAudioSubTapDriftCompensationKey: String](/documentation/coreaudio/kaudiosubtapdriftcompensationkey)
- [var kAudioSubTapDriftCompensationQualityKey: String](/documentation/coreaudio/kaudiosubtapdriftcompensationqualitykey)
- [var kAudioSubTapExtraInputLatencyKey: String](/documentation/coreaudio/kaudiosubtapextrainputlatencykey)
- [var kAudioSubTapExtraOutputLatencyKey: String](/documentation/coreaudio/kaudiosubtapextraoutputlatencykey)
- [var kAudioSubTapUIDKey: String](/documentation/coreaudio/kaudiosubtapuidkey)
- [Core Audio Enumerations](/documentation/coreaudio/core-audio-enumerations)

### Enumerations

- [Anonymous](/documentation/coreaudio/1580748-anonymous)

#### Constants

- [var kAudioStreamPropertyOwningDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyowningdevice)
- [var kAudioStreamPropertyPhysicalFormatMatch: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyphysicalformatmatch)
- [var kAudioStreamPropertyPhysicalFormatSupported: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyphysicalformatsupported)
- [var kAudioStreamPropertyPhysicalFormats: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyphysicalformats)
- [Anonymous](/documentation/coreaudio/1580731-anonymous)

#### Constants

- [var kAudioDevicePropertyBufferSize: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertybuffersize)
- [var kAudioDevicePropertyBufferSizeRange: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertybuffersizerange)
- [var kAudioDevicePropertyChannelCategoryName: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelcategoryname)
- [var kAudioDevicePropertyChannelCategoryNameCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelcategorynamecfstring)
- [var kAudioDevicePropertyChannelName: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelname)
- [var kAudioDevicePropertyChannelNameCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnamecfstring)
- [var kAudioDevicePropertyChannelNominalLineLevelNameForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnominallinelevelnameforid)
- [var kAudioDevicePropertyChannelNumberName: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnumbername)
- [var kAudioDevicePropertyChannelNumberNameCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnumbernamecfstring)
- [var kAudioDevicePropertyClockSourceNameForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclocksourcenameforid)
- [var kAudioDevicePropertyDataSourceNameForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydatasourcenameforid)
- [var kAudioDevicePropertyDeviceManufacturer: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicemanufacturer)
- [var kAudioDevicePropertyDeviceManufacturerCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicemanufacturercfstring)
- [var kAudioDevicePropertyDeviceName: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicename)
- [var kAudioDevicePropertyDeviceNameCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicenamecfstring)
- [var kAudioDevicePropertyHighPassFilterSettingNameForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyhighpassfiltersettingnameforid)
- [var kAudioDevicePropertyPlayThruDestinationNameForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrudestinationnameforid)
- [var kAudioDevicePropertyRegisterBufferList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyregisterbufferlist)
- [var kAudioDevicePropertyStreamFormat: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreamformat)
- [var kAudioDevicePropertyStreamFormatMatch: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreamformatmatch)
- [var kAudioDevicePropertyStreamFormatSupported: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreamformatsupported)
- [var kAudioDevicePropertyStreamFormats: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreamformats)
- [var kAudioDevicePropertySupportsMixing: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysupportsmixing)
- [Anonymous](/documentation/coreaudio/1580722-anonymous)

#### Constants

- [var kAudioPropertyWildcardPropertyID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopropertywildcardpropertyid)
- [Anonymous](/documentation/coreaudio/1580720-anonymous)

#### Constants

- [var kAudioISubOwnerControlClassID: AudioClassID](/documentation/coreaudio/kaudioisubownercontrolclassid)
- [Anonymous](/documentation/coreaudio/1580736-anonymous)

#### Constants

- [var kAudioClockSourceControlPropertyItemKind: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclocksourcecontrolpropertyitemkind)
- [Anonymous](/documentation/coreaudio/1580737-anonymous)

#### Constants

- [var kAudioPropertyWildcardSection: UInt8](/documentation/coreaudio/kaudiopropertywildcardsection)
- [Anonymous](/documentation/coreaudio/1580746-anonymous)

#### Constants

- [var kAudioDeviceUnknown: AudioObjectID](/documentation/coreaudio/kaudiodeviceunknown)
- [Anonymous](/documentation/coreaudio/1580723-anonymous)

#### Constants

- [var kAudioHardwarePropertyDeviceForUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertydeviceforuid)
- [var kAudioHardwarePropertyPlugInForBundleID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertypluginforbundleid)
- [var kAudioHardwarePropertyRunLoop: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyrunloop)
- [Anonymous](/documentation/coreaudio/1580747-anonymous)

#### Constants

- [var kAudioDeviceTransportTypeAutoAggregate: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeautoaggregate)
- [Anonymous](/documentation/coreaudio/1580749-anonymous)

#### Constants

- [var kAudioStreamUnknown: AudioObjectID](/documentation/coreaudio/kaudiostreamunknown)
- [Anonymous](/documentation/coreaudio/1580719-anonymous)

#### Constants

- [var kAudioBootChimeVolumeControlClassID: AudioClassID](/documentation/coreaudio/kaudiobootchimevolumecontrolclassid)
- [Anonymous](/documentation/coreaudio/1580715-anonymous)

#### Constants

- [var kAudioDevicePropertyDriverShouldOwniSub: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydrivershouldownisub)
- [var kAudioDevicePropertyPlayThruVolumeDecibelsToScalarTransferFunction: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumedecibelstoscalartransferfunction)
- [var kAudioDevicePropertySubVolumeDecibelsToScalarTransferFunction: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumedecibelstoscalartransferfunction)
- [var kAudioDevicePropertyVolumeDecibelsToScalarTransferFunction: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumedecibelstoscalartransferfunction)
- [Anonymous](/documentation/coreaudio/1580740-anonymous)

#### Constants

- [var kAudioPropertyWildcardChannel: AudioObjectPropertyElement](/documentation/coreaudio/kaudiopropertywildcardchannel)
- [Anonymous](/documentation/coreaudio/1580741-anonymous)

#### Constants

- [var kAudioControlPropertyVariant: AudioObjectPropertySelector](/documentation/coreaudio/kaudiocontrolpropertyvariant)
- [Anonymous](/documentation/coreaudio/1580726-anonymous)

#### Constants

- [var kAudioDevicePropertyScopeInput: AudioObjectPropertyScope](/documentation/coreaudio/kaudiodevicepropertyscopeinput)
- [var kAudioDevicePropertyScopeOutput: AudioObjectPropertyScope](/documentation/coreaudio/kaudiodevicepropertyscopeoutput)
- [var kAudioDevicePropertyScopePlayThrough: AudioObjectPropertyScope](/documentation/coreaudio/kaudiodevicepropertyscopeplaythrough)
- [Anonymous](/documentation/coreaudio/1580738-anonymous)

#### Constants

- [var kAudioHardwarePropertyBootChimeVolumeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumedecibels)
- [var kAudioHardwarePropertyBootChimeVolumeDecibelsToScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumedecibelstoscalar)
- [var kAudioHardwarePropertyBootChimeVolumeDecibelsToScalarTransferFunction: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumedecibelstoscalartransferfunction)
- [var kAudioHardwarePropertyBootChimeVolumeRangeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumerangedecibels)
- [var kAudioHardwarePropertyBootChimeVolumeScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumescalar)
- [var kAudioHardwarePropertyBootChimeVolumeScalarToDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertybootchimevolumescalartodecibels)
- [Anonymous](/documentation/coreaudio/1580728-anonymous)

#### Constants

- [var kAudioLevelControlPropertyDecibelsToScalarTransferFunction: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertydecibelstoscalartransferfunction)
- [Anonymous](/documentation/coreaudio/1545857-anonymous)

#### Constants

- [var kAudioTransportManagerCreateEndPointDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotransportmanagercreateendpointdevice)
- [var kAudioTransportManagerDestroyEndPointDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotransportmanagerdestroyendpointdevice)
- [Anonymous](/documentation/coreaudio/1545849-anonymous)

#### Constants

- [var kAudioPlugInCreateAggregateDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioplugincreateaggregatedevice)
- [var kAudioPlugInDestroyAggregateDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioplugindestroyaggregatedevice)
- [Anonymous](/documentation/coreaudio/1545881-anonymous)

#### Constants

- [var kAudioDevicePropertyChannelNominalLineLevel: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnominallinelevel)
- [var kAudioDevicePropertyChannelNominalLineLevelNameForIDCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnominallinelevelnameforidcfstring)
- [var kAudioDevicePropertyChannelNominalLineLevels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertychannelnominallinelevels)
- [var kAudioDevicePropertyClipLight: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertycliplight)
- [var kAudioDevicePropertyClockSource: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclocksource)
- [var kAudioDevicePropertyClockSourceKindForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclocksourcekindforid)
- [var kAudioDevicePropertyClockSourceNameForIDCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclocksourcenameforidcfstring)
- [var kAudioDevicePropertyClockSources: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclocksources)
- [var kAudioDevicePropertyDataSource: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydatasource)
- [var kAudioDevicePropertyDataSourceKindForID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydatasourcekindforid)
- [var kAudioDevicePropertyDataSourceNameForIDCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydatasourcenameforidcfstring)
- [var kAudioDevicePropertyDataSources: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydatasources)
- [var kAudioDevicePropertyHighPassFilterSetting: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyhighpassfiltersetting)
- [var kAudioDevicePropertyHighPassFilterSettingNameForIDCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyhighpassfiltersettingnameforidcfstring)
- [var kAudioDevicePropertyHighPassFilterSettings: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyhighpassfiltersettings)
- [var kAudioDevicePropertyJackIsConnected: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyjackisconnected)
- [var kAudioDevicePropertyListenback: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertylistenback)
- [var kAudioDevicePropertyMute: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertymute)
- [var kAudioDevicePropertyPhantomPower: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyphantompower)
- [var kAudioDevicePropertyPhaseInvert: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyphaseinvert)
- [var kAudioDevicePropertyPlayThru: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythru)
- [var kAudioDevicePropertyPlayThruDestination: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrudestination)
- [var kAudioDevicePropertyPlayThruDestinationNameForIDCFString: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrudestinationnameforidcfstring)
- [var kAudioDevicePropertyPlayThruDestinations: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrudestinations)
- [var kAudioDevicePropertyPlayThruSolo: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrusolo)
- [var kAudioDevicePropertyPlayThruStereoPan: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrustereopan)
- [var kAudioDevicePropertyPlayThruStereoPanChannels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythrustereopanchannels)
- [var kAudioDevicePropertyPlayThruVolumeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumedecibels)
- [var kAudioDevicePropertyPlayThruVolumeDecibelsToScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumedecibelstoscalar)
- [var kAudioDevicePropertyPlayThruVolumeRangeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumerangedecibels)
- [var kAudioDevicePropertyPlayThruVolumeScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumescalar)
- [var kAudioDevicePropertyPlayThruVolumeScalarToDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplaythruvolumescalartodecibels)
- [var kAudioDevicePropertySolo: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysolo)
- [var kAudioDevicePropertyStereoPan: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystereopan)
- [var kAudioDevicePropertyStereoPanChannels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystereopanchannels)
- [var kAudioDevicePropertySubMute: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubmute)
- [var kAudioDevicePropertySubVolumeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumedecibels)
- [var kAudioDevicePropertySubVolumeDecibelsToScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumedecibelstoscalar)
- [var kAudioDevicePropertySubVolumeRangeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumerangedecibels)
- [var kAudioDevicePropertySubVolumeScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumescalar)
- [var kAudioDevicePropertySubVolumeScalarToDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysubvolumescalartodecibels)
- [var kAudioDevicePropertyTalkback: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertytalkback)
- [var kAudioDevicePropertyVolumeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumedecibels)
- [var kAudioDevicePropertyVolumeDecibelsToScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumedecibelstoscalar)
- [var kAudioDevicePropertyVolumeRangeDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumerangedecibels)
- [var kAudioDevicePropertyVolumeScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumescalar)
- [var kAudioDevicePropertyVolumeScalarToDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyvolumescalartodecibels)
- [Anonymous](/documentation/coreaudio/1545873-anonymous)

#### Constants

- [var kAudioObjectSystemObject: Int32](/documentation/coreaudio/kaudioobjectsystemobject)
- [Anonymous](/documentation/coreaudio/1545880-anonymous)

#### Constants

- [var kAudioSubDevicePropertyDriftCompensation: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubdevicepropertydriftcompensation)
- [var kAudioSubDevicePropertyDriftCompensationQuality: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubdevicepropertydriftcompensationquality)
- [var kAudioSubDevicePropertyExtraLatency: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubdevicepropertyextralatency)
- [Anonymous](/documentation/coreaudio/1545886-anonymous)

#### Constants

- [var kAudioHardwarePropertyBoxList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyboxlist)
- [var kAudioHardwarePropertyDefaultInputDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertydefaultinputdevice)
- [var kAudioHardwarePropertyDefaultOutputDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertydefaultoutputdevice)
- [var kAudioHardwarePropertyDefaultSystemOutputDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertydefaultsystemoutputdevice)
- [var kAudioHardwarePropertyDevices: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertydevices)
- [var kAudioHardwarePropertyHogModeIsAllowed: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyhogmodeisallowed)
- [var kAudioHardwarePropertyIsInitingOrExiting: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyisinitingorexiting)
- [var kAudioHardwarePropertyMixStereoToMono: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertymixstereotomono)
- [var kAudioHardwarePropertyPlugInList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertypluginlist)
- [var kAudioHardwarePropertyPowerHint: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertypowerhint)
- [var kAudioHardwarePropertyProcessIsAudible: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyprocessisaudible)
- [var kAudioHardwarePropertyProcessIsMaster: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyprocessismaster)
- [var kAudioHardwarePropertyServiceRestarted: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyservicerestarted)
- [var kAudioHardwarePropertySleepingIsAllowed: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertysleepingisallowed)
- [var kAudioHardwarePropertyTranslateBundleIDToPlugIn: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslatebundleidtoplugin)
- [var kAudioHardwarePropertyTranslateBundleIDToTransportManager: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslatebundleidtotransportmanager)
- [var kAudioHardwarePropertyTranslateUIDToBox: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslateuidtobox)
- [var kAudioHardwarePropertyTranslateUIDToDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslateuidtodevice)
- [var kAudioHardwarePropertyTransportManagerList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytransportmanagerlist)
- [var kAudioHardwarePropertyUnloadingIsAllowed: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyunloadingisallowed)
- [var kAudioHardwarePropertyUserIDChanged: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyuseridchanged)
- [var kAudioHardwarePropertyUserSessionIsActiveOrHeadless: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyusersessionisactiveorheadless)
- [var kAudioHardwarePropertyClockDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertyclockdevicelist)
- [var kAudioHardwarePropertyTranslateUIDToClockDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiohardwarepropertytranslateuidtoclockdevice)
- [Anonymous](/documentation/coreaudio/1545884-anonymous)

#### Constants

- [var kAudioAggregateDeviceClassID: AudioClassID](/documentation/coreaudio/kaudioaggregatedeviceclassid)
- [Anonymous](/documentation/coreaudio/1545866-anonymous)

#### Constants

- [var kAudioDeviceProcessorOverload: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodeviceprocessoroverload)
- [var kAudioDevicePropertyActualSampleRate: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyactualsamplerate)
- [var kAudioDevicePropertyBufferFrameSize: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertybufferframesize)
- [var kAudioDevicePropertyBufferFrameSizeRange: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertybufferframesizerange)
- [var kAudioDevicePropertyDeviceHasChanged: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicehaschanged)
- [var kAudioDevicePropertyDeviceIsRunningSomewhere: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydeviceisrunningsomewhere)
- [var kAudioDevicePropertyHogMode: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyhogmode)
- [var kAudioDevicePropertyIOCycleUsage: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyiocycleusage)
- [var kAudioDevicePropertyIOProcStreamUsage: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyioprocstreamusage)
- [var kAudioDevicePropertyIOStoppedAbnormally: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyiostoppedabnormally)
- [var kAudioDevicePropertyPlugIn: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyplugin)
- [var kAudioDevicePropertyStreamConfiguration: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreamconfiguration)
- [var kAudioDevicePropertyUsesVariableBufferFrameSizes: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyusesvariablebufferframesizes)
- [var kAudioDevicePropertyClockDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclockdevice)
- [Anonymous](/documentation/coreaudio/1545867-anonymous)

#### Constants

- [var kAudioSubDeviceClassID: AudioClassID](/documentation/coreaudio/kaudiosubdeviceclassid)
- [Anonymous](/documentation/coreaudio/1545874-anonymous)

#### Constants

- [var kAudioObjectPropertyCreator: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertycreator)
- [var kAudioObjectPropertyListenerAdded: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertylisteneradded)
- [var kAudioObjectPropertyListenerRemoved: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertylistenerremoved)
- [Anonymous](/documentation/coreaudio/1545875-anonymous)

#### Constants

- [var kAudioAggregateDevicePropertyActiveSubDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertyactivesubdevicelist)
- [var kAudioAggregateDevicePropertyComposition: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertycomposition)
- [var kAudioAggregateDevicePropertyFullSubDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertyfullsubdevicelist)
- [var kAudioAggregateDevicePropertyMasterSubDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertymastersubdevice)
- [var kAudioAggregateDevicePropertyClockDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertyclockdevice)
- [Anonymous](/documentation/coreaudio/1545861-anonymous)

#### Constants

- [var kAudioDeviceStartTimeDontConsultDeviceFlag: UInt32](/documentation/coreaudio/kaudiodevicestarttimedontconsultdeviceflag)
- [var kAudioDeviceStartTimeDontConsultHALFlag: UInt32](/documentation/coreaudio/kaudiodevicestarttimedontconsulthalflag)
- [var kAudioDeviceStartTimeIsInputFlag: UInt32](/documentation/coreaudio/kaudiodevicestarttimeisinputflag)
- [Anonymous](/documentation/coreaudio/1545865-anonymous)

#### Constants

- [var kAudioSystemObjectClassID: AudioClassID](/documentation/coreaudio/kaudiosystemobjectclassid)
- [Anonymous](/documentation/coreaudio/1545878-anonymous)

#### Constants

- [var kAudioSubDeviceDriftCompensationHighQuality: UInt32](/documentation/coreaudio/kaudiosubdevicedriftcompensationhighquality)
- [var kAudioSubDeviceDriftCompensationLowQuality: UInt32](/documentation/coreaudio/kaudiosubdevicedriftcompensationlowquality)
- [var kAudioSubDeviceDriftCompensationMaxQuality: UInt32](/documentation/coreaudio/kaudiosubdevicedriftcompensationmaxquality)
- [var kAudioSubDeviceDriftCompensationMediumQuality: UInt32](/documentation/coreaudio/kaudiosubdevicedriftcompensationmediumquality)
- [var kAudioSubDeviceDriftCompensationMinQuality: UInt32](/documentation/coreaudio/kaudiosubdevicedriftcompensationminquality)
- [Anonymous](/documentation/coreaudio/1494510-anonymous)

#### Constants

- [var kAudioSliderControlPropertyRange: AudioObjectPropertySelector](/documentation/coreaudio/kaudioslidercontrolpropertyrange)
- [var kAudioSliderControlPropertyValue: AudioObjectPropertySelector](/documentation/coreaudio/kaudioslidercontrolpropertyvalue)
- [Anonymous](/documentation/coreaudio/1494551-anonymous)

#### Constants

- [var kAudioBooleanControlPropertyValue: AudioObjectPropertySelector](/documentation/coreaudio/kaudiobooleancontrolpropertyvalue)
- [Anonymous](/documentation/coreaudio/1494557-anonymous)

#### Constants

- [var kAudioStereoPanControlPropertyPanningChannels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostereopancontrolpropertypanningchannels)
- [var kAudioStereoPanControlPropertyValue: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostereopancontrolpropertyvalue)
- [Anonymous](/documentation/coreaudio/1494489-anonymous)

#### Constants

- [var kAudioPlugInPropertyBoxList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertyboxlist)
- [var kAudioPlugInPropertyBundleID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertybundleid)
- [var kAudioPlugInPropertyDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertydevicelist)
- [var kAudioPlugInPropertyTranslateUIDToBox: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertytranslateuidtobox)
- [var kAudioPlugInPropertyTranslateUIDToDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertytranslateuidtodevice)
- [var kAudioPlugInPropertyClockDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertyclockdevicelist)
- [var kAudioPlugInPropertyTranslateUIDToClockDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiopluginpropertytranslateuidtoclockdevice)
- [Anonymous](/documentation/coreaudio/1494580-anonymous)

#### Constants

- [var kAudioDeviceTransportTypeAVB: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeavb)
- [var kAudioDeviceTransportTypeAggregate: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeaggregate)
- [var kAudioDeviceTransportTypeAirPlay: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeairplay)
- [var kAudioDeviceTransportTypeBluetooth: UInt32](/documentation/coreaudio/kaudiodevicetransporttypebluetooth)
- [var kAudioDeviceTransportTypeBluetoothLE: UInt32](/documentation/coreaudio/kaudiodevicetransporttypebluetoothle)
- [var kAudioDeviceTransportTypeBuiltIn: UInt32](/documentation/coreaudio/kaudiodevicetransporttypebuiltin)
- [var kAudioDeviceTransportTypeDisplayPort: UInt32](/documentation/coreaudio/kaudiodevicetransporttypedisplayport)
- [var kAudioDeviceTransportTypeFireWire: UInt32](/documentation/coreaudio/kaudiodevicetransporttypefirewire)
- [var kAudioDeviceTransportTypeHDMI: UInt32](/documentation/coreaudio/kaudiodevicetransporttypehdmi)
- [var kAudioDeviceTransportTypePCI: UInt32](/documentation/coreaudio/kaudiodevicetransporttypepci)
- [var kAudioDeviceTransportTypeThunderbolt: UInt32](/documentation/coreaudio/kaudiodevicetransporttypethunderbolt)
- [var kAudioDeviceTransportTypeUSB: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeusb)
- [var kAudioDeviceTransportTypeUnknown: UInt32](/documentation/coreaudio/kaudiodevicetransporttypeunknown)
- [var kAudioDeviceTransportTypeVirtual: UInt32](/documentation/coreaudio/kaudiodevicetransporttypevirtual)
- [Anonymous](/documentation/coreaudio/1494466-anonymous)

#### Constants

- [var kAudioTransportManagerPropertyEndPointList: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotransportmanagerpropertyendpointlist)
- [var kAudioTransportManagerPropertyTranslateUIDToEndPoint: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotransportmanagerpropertytranslateuidtoendpoint)
- [var kAudioTransportManagerPropertyTransportType: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotransportmanagerpropertytransporttype)
- [Anonymous](/documentation/coreaudio/1494573-anonymous)

#### Constants

- [var kAudioStreamClassID: AudioClassID](/documentation/coreaudio/kaudiostreamclassid)
- [Anonymous](/documentation/coreaudio/1494441-anonymous)

#### Constants

- [var kAudioEndPointDeviceClassID: AudioClassID](/documentation/coreaudio/kaudioendpointdeviceclassid)
- [Anonymous](/documentation/coreaudio/1494474-anonymous)

#### Constants

- [var kAudioControlClassID: AudioClassID](/documentation/coreaudio/kaudiocontrolclassid)
- [Anonymous](/documentation/coreaudio/1494430-anonymous)

#### Constants

- [var kAudioEndPointDevicePropertyComposition: AudioObjectPropertySelector](/documentation/coreaudio/kaudioendpointdevicepropertycomposition)
- [var kAudioEndPointDevicePropertyEndPointList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioendpointdevicepropertyendpointlist)
- [var kAudioEndPointDevicePropertyIsPrivate: AudioObjectPropertySelector](/documentation/coreaudio/kaudioendpointdevicepropertyisprivate)
- [Anonymous](/documentation/coreaudio/1494576-anonymous)

#### Constants

- [var kAudioObjectPropertyScopeWildcard: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyscopewildcard)
- [Anonymous](/documentation/coreaudio/1494528-anonymous)

#### Constants

- [var kAudioClockSourceItemKindInternal: UInt32](/documentation/coreaudio/kaudioclocksourceitemkindinternal)
- [Anonymous](/documentation/coreaudio/1494522-anonymous)

#### Constants

- [var kAudioBoxPropertyAcquired: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyacquired)
- [var kAudioBoxPropertyAcquisitionFailed: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyacquisitionfailed)
- [var kAudioBoxPropertyBoxUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyboxuid)
- [var kAudioBoxPropertyDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertydevicelist)
- [var kAudioBoxPropertyHasAudio: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyhasaudio)
- [var kAudioBoxPropertyHasMIDI: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyhasmidi)
- [var kAudioBoxPropertyHasVideo: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyhasvideo)
- [var kAudioBoxPropertyIsProtected: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyisprotected)
- [var kAudioBoxPropertyTransportType: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertytransporttype)
- [var kAudioBoxPropertyClockDeviceList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioboxpropertyclockdevicelist)
- [Anonymous](/documentation/coreaudio/1494472-anonymous)

#### Constants

- [var kAudioTransportManagerClassID: AudioClassID](/documentation/coreaudio/kaudiotransportmanagerclassid)
- [Anonymous](/documentation/coreaudio/1494571-anonymous)

#### Constants

- [var kAudioControlPropertyElement: AudioObjectPropertySelector](/documentation/coreaudio/kaudiocontrolpropertyelement)
- [var kAudioControlPropertyScope: AudioObjectPropertySelector](/documentation/coreaudio/kaudiocontrolpropertyscope)
- [Anonymous](/documentation/coreaudio/1494439-anonymous)

#### Constants

- [var kAudioObjectClassID: AudioClassID](/documentation/coreaudio/kaudioobjectclassid)
- [Anonymous](/documentation/coreaudio/1494512-anonymous)

#### Constants

- [var kAudioBooleanControlClassID: AudioClassID](/documentation/coreaudio/kaudiobooleancontrolclassid)
- [var kAudioClipLightControlClassID: AudioClassID](/documentation/coreaudio/kaudiocliplightcontrolclassid)
- [var kAudioJackControlClassID: AudioClassID](/documentation/coreaudio/kaudiojackcontrolclassid)
- [var kAudioLFEMuteControlClassID: AudioClassID](/documentation/coreaudio/kaudiolfemutecontrolclassid)
- [var kAudioListenbackControlClassID: AudioClassID](/documentation/coreaudio/kaudiolistenbackcontrolclassid)
- [var kAudioMuteControlClassID: AudioClassID](/documentation/coreaudio/kaudiomutecontrolclassid)
- [var kAudioPhantomPowerControlClassID: AudioClassID](/documentation/coreaudio/kaudiophantompowercontrolclassid)
- [var kAudioPhaseInvertControlClassID: AudioClassID](/documentation/coreaudio/kaudiophaseinvertcontrolclassid)
- [var kAudioSoloControlClassID: AudioClassID](/documentation/coreaudio/kaudiosolocontrolclassid)
- [var kAudioTalkbackControlClassID: AudioClassID](/documentation/coreaudio/kaudiotalkbackcontrolclassid)
- [Anonymous](/documentation/coreaudio/1646514-anonymous)

#### Constants

- [var kAudioClockDevicePropertyAvailableNominalSampleRates: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertyavailablenominalsamplerates)
- [var kAudioClockDevicePropertyClockDomain: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertyclockdomain)
- [var kAudioClockDevicePropertyControlList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertycontrollist)
- [var kAudioClockDevicePropertyDeviceIsAlive: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertydeviceisalive)
- [var kAudioClockDevicePropertyDeviceIsRunning: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertydeviceisrunning)
- [var kAudioClockDevicePropertyDeviceUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertydeviceuid)
- [var kAudioClockDevicePropertyLatency: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertylatency)
- [var kAudioClockDevicePropertyNominalSampleRate: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertynominalsamplerate)
- [var kAudioClockDevicePropertyTransportType: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdevicepropertytransporttype)
- [Anonymous](/documentation/coreaudio/1494595-anonymous)

#### Constants

- [var kAudioPlugInClassID: AudioClassID](/documentation/coreaudio/kaudiopluginclassid)
- [Anonymous](/documentation/coreaudio/1494454-anonymous)

#### Constants

- [var kAudioDevicePropertyAvailableNominalSampleRates: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyavailablenominalsamplerates)
- [var kAudioDevicePropertyClockDomain: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyclockdomain)
- [var kAudioDevicePropertyConfigurationApplication: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyconfigurationapplication)
- [var kAudioDevicePropertyDeviceCanBeDefaultDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicecanbedefaultdevice)
- [var kAudioDevicePropertyDeviceCanBeDefaultSystemDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydevicecanbedefaultsystemdevice)
- [var kAudioDevicePropertyDeviceIsAlive: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydeviceisalive)
- [var kAudioDevicePropertyDeviceIsRunning: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydeviceisrunning)
- [var kAudioDevicePropertyDeviceUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertydeviceuid)
- [var kAudioDevicePropertyIcon: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyicon)
- [var kAudioDevicePropertyIsHidden: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyishidden)
- [var kAudioDevicePropertyLatency: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertylatency)
- [var kAudioDevicePropertyModelUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertymodeluid)
- [var kAudioDevicePropertyNominalSampleRate: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertynominalsamplerate)
- [var kAudioDevicePropertyPreferredChannelLayout: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertypreferredchannellayout)
- [var kAudioDevicePropertyPreferredChannelsForStereo: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertypreferredchannelsforstereo)
- [var kAudioDevicePropertyRelatedDevices: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyrelateddevices)
- [var kAudioDevicePropertySafetyOffset: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertysafetyoffset)
- [var kAudioDevicePropertyStreams: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertystreams)
- [var kAudioDevicePropertyTransportType: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertytransporttype)
- [var kAudioObjectPropertyControlList: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertycontrollist)
- [Anonymous](/documentation/coreaudio/1494554-anonymous)

#### Constants

- [var kAudioClockSourceControlClassID: AudioClassID](/documentation/coreaudio/kaudioclocksourcecontrolclassid)
- [var kAudioDataDestinationControlClassID: AudioClassID](/documentation/coreaudio/kaudiodatadestinationcontrolclassid)
- [var kAudioDataSourceControlClassID: AudioClassID](/documentation/coreaudio/kaudiodatasourcecontrolclassid)
- [var kAudioHighPassFilterControlClassID: AudioClassID](/documentation/coreaudio/kaudiohighpassfiltercontrolclassid)
- [var kAudioLineLevelControlClassID: AudioClassID](/documentation/coreaudio/kaudiolinelevelcontrolclassid)
- [var kAudioSelectorControlClassID: AudioClassID](/documentation/coreaudio/kaudioselectorcontrolclassid)
- [Anonymous](/documentation/coreaudio/1494445-anonymous)

#### Constants

- [var kAudioStereoPanControlClassID: AudioClassID](/documentation/coreaudio/kaudiostereopancontrolclassid)
- [Anonymous](/documentation/coreaudio/1494533-anonymous)

#### Constants

- [var kAudioSliderControlClassID: AudioClassID](/documentation/coreaudio/kaudioslidercontrolclassid)
- [Anonymous](/documentation/coreaudio/1494591-anonymous)

#### Constants

- [var kAudioObjectPropertySelectorWildcard: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyselectorwildcard)
- [Anonymous](/documentation/coreaudio/1494569-anonymous)

#### Constants

- [var kAudioObjectClassIDWildcard: AudioClassID](/documentation/coreaudio/kaudioobjectclassidwildcard)
- [Anonymous](/documentation/coreaudio/1494461-anonymous)

#### Constants

- [var kAudioObjectUnknown: AudioObjectID](/documentation/coreaudio/kaudioobjectunknown)
- [Anonymous](/documentation/coreaudio/1494526-anonymous)

#### Constants

- [var kAudioBoxClassID: AudioClassID](/documentation/coreaudio/kaudioboxclassid)
- [Anonymous](/documentation/coreaudio/1494437-anonymous)

#### Constants

- [var kAudioObjectPropertyElementWildcard: AudioObjectPropertyElement](/documentation/coreaudio/kaudioobjectpropertyelementwildcard)
- [Anonymous](/documentation/coreaudio/1494531-anonymous)

#### Constants

- [var kAudioDevicePermissionsError: OSStatus](/documentation/coreaudio/kaudiodevicepermissionserror)
- [var kAudioDeviceUnsupportedFormatError: OSStatus](/documentation/coreaudio/kaudiodeviceunsupportedformaterror)
- [var kAudioHardwareBadDeviceError: OSStatus](/documentation/coreaudio/kaudiohardwarebaddeviceerror)
- [var kAudioHardwareBadObjectError: OSStatus](/documentation/coreaudio/kaudiohardwarebadobjecterror)
- [var kAudioHardwareBadPropertySizeError: OSStatus](/documentation/coreaudio/kaudiohardwarebadpropertysizeerror)
- [var kAudioHardwareBadStreamError: OSStatus](/documentation/coreaudio/kaudiohardwarebadstreamerror)
- [var kAudioHardwareIllegalOperationError: OSStatus](/documentation/coreaudio/kaudiohardwareillegaloperationerror)
- [var kAudioHardwareNoError: OSStatus](/documentation/coreaudio/kaudiohardwarenoerror)
- [var kAudioHardwareNotRunningError: OSStatus](/documentation/coreaudio/kaudiohardwarenotrunningerror)
- [var kAudioHardwareUnknownPropertyError: OSStatus](/documentation/coreaudio/kaudiohardwareunknownpropertyerror)
- [var kAudioHardwareUnspecifiedError: OSStatus](/documentation/coreaudio/kaudiohardwareunspecifiederror)
- [var kAudioHardwareUnsupportedOperationError: OSStatus](/documentation/coreaudio/kaudiohardwareunsupportedoperationerror)
- [Anonymous](/documentation/coreaudio/1494587-anonymous)

#### Constants

- [var kAudioEndPointClassID: AudioClassID](/documentation/coreaudio/kaudioendpointclassid)
- [Anonymous](/documentation/coreaudio/1494541-anonymous)

#### Constants

- [var kAudioStreamPropertyAvailablePhysicalFormats: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyavailablephysicalformats)
- [var kAudioStreamPropertyAvailableVirtualFormats: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyavailablevirtualformats)
- [var kAudioStreamPropertyDirection: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertydirection)
- [var kAudioStreamPropertyIsActive: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyisactive)
- [var kAudioStreamPropertyLatency: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertylatency)
- [var kAudioStreamPropertyPhysicalFormat: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyphysicalformat)
- [var kAudioStreamPropertyStartingChannel: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertystartingchannel)
- [var kAudioStreamPropertyTerminalType: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyterminaltype)
- [var kAudioStreamPropertyVirtualFormat: AudioObjectPropertySelector](/documentation/coreaudio/kaudiostreampropertyvirtualformat)
- [Anonymous](/documentation/coreaudio/1494594-anonymous)

#### Constants

- [var kAudioSelectorControlPropertyAvailableItems: AudioObjectPropertySelector](/documentation/coreaudio/kaudioselectorcontrolpropertyavailableitems)
- [var kAudioSelectorControlPropertyCurrentItem: AudioObjectPropertySelector](/documentation/coreaudio/kaudioselectorcontrolpropertycurrentitem)
- [var kAudioSelectorControlPropertyItemKind: AudioObjectPropertySelector](/documentation/coreaudio/kaudioselectorcontrolpropertyitemkind)
- [var kAudioSelectorControlPropertyItemName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioselectorcontrolpropertyitemname)
- [Anonymous](/documentation/coreaudio/1646515-anonymous)

#### Constants

- [var kAudioClockDeviceClassID: AudioObjectPropertySelector](/documentation/coreaudio/kaudioclockdeviceclassid)
- [Anonymous](/documentation/coreaudio/1494536-anonymous)

#### Constants

- [var kAudioLevelControlPropertyConvertDecibelsToScalar: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertyconvertdecibelstoscalar)
- [var kAudioLevelControlPropertyConvertScalarToDecibels: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertyconvertscalartodecibels)
- [var kAudioLevelControlPropertyDecibelRange: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertydecibelrange)
- [var kAudioLevelControlPropertyDecibelValue: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertydecibelvalue)
- [var kAudioLevelControlPropertyScalarValue: AudioObjectPropertySelector](/documentation/coreaudio/kaudiolevelcontrolpropertyscalarvalue)
- [Anonymous](/documentation/coreaudio/1494449-anonymous)

#### Constants

- [var kAudioObjectPropertyBaseClass: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertybaseclass)
- [var kAudioObjectPropertyClass: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyclass)
- [var kAudioObjectPropertyElementCategoryName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyelementcategoryname)
- [var kAudioObjectPropertyElementName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyelementname)
- [var kAudioObjectPropertyElementNumberName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyelementnumbername)
- [var kAudioObjectPropertyFirmwareVersion: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyfirmwareversion)
- [var kAudioObjectPropertyIdentify: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyidentify)
- [var kAudioObjectPropertyManufacturer: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertymanufacturer)
- [var kAudioObjectPropertyModelName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertymodelname)
- [var kAudioObjectPropertyName: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyname)
- [var kAudioObjectPropertyOwnedObjects: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyownedobjects)
- [var kAudioObjectPropertyOwner: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyowner)
- [var kAudioObjectPropertySerialNumber: AudioObjectPropertySelector](/documentation/coreaudio/kaudioobjectpropertyserialnumber)
- [Anonymous](/documentation/coreaudio/1494483-anonymous)

#### Constants

- [var kAudioDeviceClassID: AudioClassID](/documentation/coreaudio/kaudiodeviceclassid)
- [Anonymous](/documentation/coreaudio/1494464-anonymous)

#### Constants

- [var kAudioObjectPropertyElementMaster: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyelementmaster)
- [var kAudioObjectPropertyScopeGlobal: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyscopeglobal)
- [var kAudioObjectPropertyScopeInput: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyscopeinput)
- [var kAudioObjectPropertyScopeOutput: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyscopeoutput)
- [var kAudioObjectPropertyScopePlayThrough: AudioObjectPropertyScope](/documentation/coreaudio/kaudioobjectpropertyscopeplaythrough)
- [Anonymous](/documentation/coreaudio/1494503-anonymous)

#### Constants

- [var kAudioLFEVolumeControlClassID: AudioClassID](/documentation/coreaudio/kaudiolfevolumecontrolclassid)
- [var kAudioLevelControlClassID: AudioClassID](/documentation/coreaudio/kaudiolevelcontrolclassid)
- [var kAudioVolumeControlClassID: AudioClassID](/documentation/coreaudio/kaudiovolumecontrolclassid)
- [Anonymous](/documentation/coreaudio/1494543-anonymous)

#### Constants

- [var kAudioStreamTerminalTypeDigitalAudioInterface: UInt32](/documentation/coreaudio/kaudiostreamterminaltypedigitalaudiointerface)
- [var kAudioStreamTerminalTypeDisplayPort: UInt32](/documentation/coreaudio/kaudiostreamterminaltypedisplayport)
- [var kAudioStreamTerminalTypeHDMI: UInt32](/documentation/coreaudio/kaudiostreamterminaltypehdmi)
- [var kAudioStreamTerminalTypeHeadphones: UInt32](/documentation/coreaudio/kaudiostreamterminaltypeheadphones)
- [var kAudioStreamTerminalTypeHeadsetMicrophone: UInt32](/documentation/coreaudio/kaudiostreamterminaltypeheadsetmicrophone)
- [var kAudioStreamTerminalTypeLFESpeaker: UInt32](/documentation/coreaudio/kaudiostreamterminaltypelfespeaker)
- [var kAudioStreamTerminalTypeLine: UInt32](/documentation/coreaudio/kaudiostreamterminaltypeline)
- [var kAudioStreamTerminalTypeMicrophone: UInt32](/documentation/coreaudio/kaudiostreamterminaltypemicrophone)
- [var kAudioStreamTerminalTypeReceiverMicrophone: UInt32](/documentation/coreaudio/kaudiostreamterminaltypereceivermicrophone)
- [var kAudioStreamTerminalTypeReceiverSpeaker: UInt32](/documentation/coreaudio/kaudiostreamterminaltypereceiverspeaker)
- [var kAudioStreamTerminalTypeSpeaker: UInt32](/documentation/coreaudio/kaudiostreamterminaltypespeaker)
- [var kAudioStreamTerminalTypeTTY: UInt32](/documentation/coreaudio/kaudiostreamterminaltypetty)
- [var kAudioStreamTerminalTypeUnknown: UInt32](/documentation/coreaudio/kaudiostreamterminaltypeunknown)
- [Anonymous](/documentation/coreaudio/1494470-anonymous)

#### Constants

- [var kAudioSelectorControlItemKindSpacer: UInt32](/documentation/coreaudio/kaudioselectorcontrolitemkindspacer)
- [AudioHardwarePowerHint](/documentation/coreaudio/audiohardwarepowerhint)

#### Constants

- [case favorSavingPower](/documentation/coreaudio/audiohardwarepowerhint/favorsavingpower)
- [case none](/documentation/coreaudio/audiohardwarepowerhint/none)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coreaudio/audiohardwarepowerhint/init(rawvalue:))
- [AudioLevelControlTransferFunction](/documentation/coreaudio/audiolevelcontroltransferfunction)

#### Constants

- [case tranferFunction10Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction10over1)
- [case tranferFunction11Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction11over1)
- [case tranferFunction12Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction12over1)
- [case tranferFunction1Over2](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction1over2)
- [case tranferFunction1Over3](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction1over3)
- [case tranferFunction2Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction2over1)
- [case tranferFunction3Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction3over1)
- [case tranferFunction3Over2](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction3over2)
- [case tranferFunction3Over4](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction3over4)
- [case tranferFunction4Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction4over1)
- [case tranferFunction5Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction5over1)
- [case tranferFunction6Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction6over1)
- [case tranferFunction7Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction7over1)
- [case tranferFunction8Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction8over1)
- [case tranferFunction9Over1](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunction9over1)
- [case tranferFunctionLinear](/documentation/coreaudio/audiolevelcontroltransferfunction/tranferfunctionlinear)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coreaudio/audiolevelcontroltransferfunction/init(rawvalue:))
- [Anonymous](/documentation/coreaudio/3782865-anonymous)

#### Constants

- [var kAudioAggregateDevicePropertyMasterSubDevice: AudioObjectPropertySelector](/documentation/coreaudio/kaudioaggregatedevicepropertymastersubdevice)
- [Anonymous](/documentation/coreaudio/4160684-anonymous)

#### Constants

- [var kAudioAggregateDriftCompensationHighQuality: UInt32](/documentation/coreaudio/kaudioaggregatedriftcompensationhighquality)
- [var kAudioAggregateDriftCompensationLowQuality: UInt32](/documentation/coreaudio/kaudioaggregatedriftcompensationlowquality)
- [var kAudioAggregateDriftCompensationMaxQuality: UInt32](/documentation/coreaudio/kaudioaggregatedriftcompensationmaxquality)
- [var kAudioAggregateDriftCompensationMediumQuality: UInt32](/documentation/coreaudio/kaudioaggregatedriftcompensationmediumquality)
- [var kAudioAggregateDriftCompensationMinQuality: UInt32](/documentation/coreaudio/kaudioaggregatedriftcompensationminquality)
- [Anonymous](/documentation/coreaudio/4160685-anonymous)

#### Constants

- [var kAudioProcessClassID: AudioClassID](/documentation/coreaudio/kaudioprocessclassid)
- [Anonymous](/documentation/coreaudio/4160686-anonymous)

#### Constants

- [var kAudioProcessPropertyBundleID: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertybundleid)
- [var kAudioProcessPropertyDevices: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertydevices)
- [var kAudioProcessPropertyIsRunning: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertyisrunning)
- [var kAudioProcessPropertyIsRunningInput: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertyisrunninginput)
- [var kAudioProcessPropertyIsRunningOutput: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertyisrunningoutput)
- [var kAudioProcessPropertyPID: AudioObjectPropertySelector](/documentation/coreaudio/kaudioprocesspropertypid)
- [Anonymous](/documentation/coreaudio/4160687-anonymous)

#### Constants

- [var kAudioSubTapClassID: AudioClassID](/documentation/coreaudio/kaudiosubtapclassid)
- [Anonymous](/documentation/coreaudio/4160688-anonymous)

#### Constants

- [var kAudioSubTapPropertyDriftCompensation: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubtappropertydriftcompensation)
- [var kAudioSubTapPropertyDriftCompensationQuality: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubtappropertydriftcompensationquality)
- [var kAudioSubTapPropertyExtraLatency: AudioObjectPropertySelector](/documentation/coreaudio/kaudiosubtappropertyextralatency)
- [Anonymous](/documentation/coreaudio/4160689-anonymous)

#### Constants

- [var kAudioTapClassID: AudioClassID](/documentation/coreaudio/kaudiotapclassid)
- [Anonymous](/documentation/coreaudio/4160690-anonymous)

#### Constants

- [var kAudioTapPropertyDescription: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotappropertydescription)
- [var kAudioTapPropertyFormat: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotappropertyformat)
- [var kAudioTapPropertyUID: AudioObjectPropertySelector](/documentation/coreaudio/kaudiotappropertyuid)
- [AudioHardwareDirection](/documentation/coreaudio/audiohardwaredirection)

#### Enumeration Cases

- [case input](/documentation/coreaudio/audiohardwaredirection/input)
- [case output](/documentation/coreaudio/audiohardwaredirection/output)
- [CATapMuteBehavior](/documentation/coreaudio/catapmutebehavior)

#### Enumeration Cases

- [case muted](/documentation/coreaudio/catapmutebehavior/muted)
- [case mutedWhenTapped](/documentation/coreaudio/catapmutebehavior/mutedwhentapped)
- [case unmuted](/documentation/coreaudio/catapmutebehavior/unmuted)

#### Initializers

- [init?(rawValue: Int)](/documentation/coreaudio/catapmutebehavior/init(rawvalue:))

## Classes

- [AudioHardwareAggregateDevice](/documentation/coreaudio/audiohardwareaggregatedevice)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwareaggregatedevice/init(id:))

### Instance Properties

- [var activeSubdevices: [AudioHardwareClock]](/documentation/coreaudio/audiohardwareaggregatedevice/activesubdevices)
- [var activeSubtaps: [AudioHardwareTap]](/documentation/coreaudio/audiohardwareaggregatedevice/activesubtaps)
- [var clockSource: AudioHardwareObject?](/documentation/coreaudio/audiohardwareaggregatedevice/clocksource)
- [var composition: [String : Any]](/documentation/coreaudio/audiohardwareaggregatedevice/composition)
- [var subdevices: [AudioHardwareClock]](/documentation/coreaudio/audiohardwareaggregatedevice/subdevices)
- [var subtaps: [AudioHardwareTap]](/documentation/coreaudio/audiohardwareaggregatedevice/subtaps)

### Instance Methods

- [func setClockSource(AudioHardwareObject) throws](/documentation/coreaudio/audiohardwareaggregatedevice/setclocksource(_:))
- [func setComposition([String : Any]) throws](/documentation/coreaudio/audiohardwareaggregatedevice/setcomposition(_:))
- [func setSubdevices([AudioHardwareClock]) throws](/documentation/coreaudio/audiohardwareaggregatedevice/setsubdevices(_:))
- [func setSubtaps([AudioHardwareTap]) throws](/documentation/coreaudio/audiohardwareaggregatedevice/setsubtaps(_:))
- [AudioHardwareBox](/documentation/coreaudio/audiohardwarebox)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwarebox/init(id:))

### Instance Properties

- [var clocks: [AudioHardwareClock]](/documentation/coreaudio/audiohardwarebox/clocks)
- [var devices: [AudioHardwareDevice]](/documentation/coreaudio/audiohardwarebox/devices)
- [var enabled: Bool](/documentation/coreaudio/audiohardwarebox/enabled)
- [var hasAudio: Bool](/documentation/coreaudio/audiohardwarebox/hasaudio)
- [var hasMIDI: Bool](/documentation/coreaudio/audiohardwarebox/hasmidi)
- [var hasVideo: Bool](/documentation/coreaudio/audiohardwarebox/hasvideo)
- [var isProtected: Bool](/documentation/coreaudio/audiohardwarebox/isprotected)
- [var transportType: UInt32](/documentation/coreaudio/audiohardwarebox/transporttype)
- [var uid: String](/documentation/coreaudio/audiohardwarebox/uid)

### Instance Methods

- [func disable() throws](/documentation/coreaudio/audiohardwarebox/disable())
- [func enable() throws](/documentation/coreaudio/audiohardwarebox/enable())
- [AudioHardwareClock](/documentation/coreaudio/audiohardwareclock)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwareclock/init(id:))

### Instance Properties

- [var availableNominalSampleRates: [AudioValueRange]](/documentation/coreaudio/audiohardwareclock/availablenominalsamplerates)
- [var clockDomain: UInt32](/documentation/coreaudio/audiohardwareclock/clockdomain)
- [var controls: [AudioHardwareControl]](/documentation/coreaudio/audiohardwareclock/controls)
- [var inputLatency: Int](/documentation/coreaudio/audiohardwareclock/inputlatency)
- [var isAlive: Bool](/documentation/coreaudio/audiohardwareclock/isalive)
- [var isRunning: Bool](/documentation/coreaudio/audiohardwareclock/isrunning)
- [var nominalSampleRate: Double](/documentation/coreaudio/audiohardwareclock/nominalsamplerate)
- [var outputLatency: Int](/documentation/coreaudio/audiohardwareclock/outputlatency)
- [var transportType: UInt32](/documentation/coreaudio/audiohardwareclock/transporttype)
- [var uid: String](/documentation/coreaudio/audiohardwareclock/uid)

### Instance Methods

- [func setNominalSampleRate(Double) throws](/documentation/coreaudio/audiohardwareclock/setnominalsamplerate(_:))
- [AudioHardwareControl](/documentation/coreaudio/audiohardwarecontrol)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwarecontrol/init(id:))

### Instance Properties

- [var availableItems: [UInt32]](/documentation/coreaudio/audiohardwarecontrol/availableitems)
- [var booleanValue: Bool](/documentation/coreaudio/audiohardwarecontrol/booleanvalue)
- [var selectedItems: [UInt32]](/documentation/coreaudio/audiohardwarecontrol/selecteditems)
- [var sliderRange: [UInt32]](/documentation/coreaudio/audiohardwarecontrol/sliderrange)
- [var sliderValue: UInt32](/documentation/coreaudio/audiohardwarecontrol/slidervalue)
- [var stereoPanChannels: [UInt32]](/documentation/coreaudio/audiohardwarecontrol/stereopanchannels)
- [var stereoPanValue: Float](/documentation/coreaudio/audiohardwarecontrol/stereopanvalue)
- [var volumeDecibelRange: AudioValueRange](/documentation/coreaudio/audiohardwarecontrol/volumedecibelrange)
- [var volumeDecibelValue: Float](/documentation/coreaudio/audiohardwarecontrol/volumedecibelvalue)
- [var volumeScalarValue: Float](/documentation/coreaudio/audiohardwarecontrol/volumescalarvalue)

### Instance Methods

- [func convertToDecibels(fromScalar: Float) throws -> Float](/documentation/coreaudio/audiohardwarecontrol/converttodecibels(fromscalar:))
- [func convertToScalar(fromDecibels: Float) throws -> Float](/documentation/coreaudio/audiohardwarecontrol/converttoscalar(fromdecibels:))
- [func selectorItemKind(fromID: UInt32) throws -> UInt32](/documentation/coreaudio/audiohardwarecontrol/selectoritemkind(fromid:))
- [func selectorItemName(fromID: UInt32) throws -> String](/documentation/coreaudio/audiohardwarecontrol/selectoritemname(fromid:))
- [func setBooleanValue(Bool) throws](/documentation/coreaudio/audiohardwarecontrol/setbooleanvalue(_:))
- [func setSelectedItems([UInt32]) throws](/documentation/coreaudio/audiohardwarecontrol/setselecteditems(_:))
- [func setSliderValue(UInt32) throws](/documentation/coreaudio/audiohardwarecontrol/setslidervalue(_:))
- [func setStereoPanValue(Float) throws](/documentation/coreaudio/audiohardwarecontrol/setstereopanvalue(_:))
- [func setVolumeDecibelValue(Float) throws](/documentation/coreaudio/audiohardwarecontrol/setvolumedecibelvalue(_:))
- [func setVolumeScalarValue(Float) throws](/documentation/coreaudio/audiohardwarecontrol/setvolumescalarvalue(_:))
- [AudioHardwareDevice](/documentation/coreaudio/audiohardwaredevice)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwaredevice/init(id:))

### Instance Properties

- [var actualSampleRate: Double](/documentation/coreaudio/audiohardwaredevice/actualsamplerate)
- [var bufferFrameSize: Int](/documentation/coreaudio/audiohardwaredevice/bufferframesize)
- [var bufferFrameSizeRange: AudioValueRange](/documentation/coreaudio/audiohardwaredevice/bufferframesizerange)
- [var canBeDefaultInputDevice: Bool](/documentation/coreaudio/audiohardwaredevice/canbedefaultinputdevice)
- [var canBeDefaultOutputDevice: Bool](/documentation/coreaudio/audiohardwaredevice/canbedefaultoutputdevice)
- [var canBeDefaultSoundEffectsDevice: Bool](/documentation/coreaudio/audiohardwaredevice/canbedefaultsoundeffectsdevice)
- [var clock: AudioHardwareClock](/documentation/coreaudio/audiohardwaredevice/clock)
- [var configurationApplication: String](/documentation/coreaudio/audiohardwaredevice/configurationapplication)
- [var currentTime: AudioTimeStamp](/documentation/coreaudio/audiohardwaredevice/currenttime)
- [var hogModePID: pid_t](/documentation/coreaudio/audiohardwaredevice/hogmodepid)
- [var icon: URL?](/documentation/coreaudio/audiohardwaredevice/icon)
- [var inputSafetyOffset: Int](/documentation/coreaudio/audiohardwaredevice/inputsafetyoffset)
- [var inputStreamConfiguration: [AudioBuffer]](/documentation/coreaudio/audiohardwaredevice/inputstreamconfiguration)
- [var ioCycleUsage: Float](/documentation/coreaudio/audiohardwaredevice/iocycleusage)
- [var isHidden: Bool](/documentation/coreaudio/audiohardwaredevice/ishidden)
- [var isProcessInputMuted: Bool](/documentation/coreaudio/audiohardwaredevice/isprocessinputmuted)
- [var isProcessOutputMuted: Bool](/documentation/coreaudio/audiohardwaredevice/isprocessoutputmuted)
- [var isRunningInAProcess: Bool](/documentation/coreaudio/audiohardwaredevice/isrunninginaprocess)
- [var largestVariableBufferFrameSize: Int](/documentation/coreaudio/audiohardwaredevice/largestvariablebufferframesize)
- [var modelUID: String](/documentation/coreaudio/audiohardwaredevice/modeluid)
- [var outputSafetyOffset: Int](/documentation/coreaudio/audiohardwaredevice/outputsafetyoffset)
- [var outputStreamConfiguration: [AudioBuffer]](/documentation/coreaudio/audiohardwaredevice/outputstreamconfiguration)
- [var preferredInputChannelsForStereo: [UInt32]](/documentation/coreaudio/audiohardwaredevice/preferredinputchannelsforstereo)
- [var preferredOutputChannelsForStereo: [UInt32]](/documentation/coreaudio/audiohardwaredevice/preferredoutputchannelsforstereo)
- [var relatedDevices: [AudioHardwareDevice]](/documentation/coreaudio/audiohardwaredevice/relateddevices)
- [var streams: [AudioHardwareStream]](/documentation/coreaudio/audiohardwaredevice/streams)
- [var usesVariableBufferFrameSizes: Bool](/documentation/coreaudio/audiohardwaredevice/usesvariablebufferframesizes)
- [var workgroup: WorkGroup](/documentation/coreaudio/audiohardwaredevice/workgroup)

### Instance Methods

- [func nearestStartTime(atTime: AudioTimeStamp, withFlags: UInt32) throws -> AudioTimeStamp](/documentation/coreaudio/audiohardwaredevice/neareststarttime(attime:withflags:))
- [func setBufferFrameSize(Int) throws](/documentation/coreaudio/audiohardwaredevice/setbufferframesize(_:))
- [func setClock(AudioHardwareClock) throws](/documentation/coreaudio/audiohardwaredevice/setclock(_:))
- [func setIOCycleUsage(Float) throws](/documentation/coreaudio/audiohardwaredevice/setiocycleusage(_:))
- [func setIsProcessInputMuted(Bool) throws](/documentation/coreaudio/audiohardwaredevice/setisprocessinputmuted(_:))
- [func setIsProcessOutputMuted(Bool) throws](/documentation/coreaudio/audiohardwaredevice/setisprocessoutputmuted(_:))
- [func setPreferredInputChannelsForStereo([UInt32]) throws](/documentation/coreaudio/audiohardwaredevice/setpreferredinputchannelsforstereo(_:))
- [func setPreferredOutputChannelsForStereo([UInt32]) throws](/documentation/coreaudio/audiohardwaredevice/setpreferredoutputchannelsforstereo(_:))
- [func start(IOProcID: AudioDeviceIOProcID?) throws](/documentation/coreaudio/audiohardwaredevice/start(ioprocid:))
- [func start(at: AudioTimeStamp, flags: UInt32, IOProcID: AudioDeviceIOProcID?) throws -> AudioTimeStamp?](/documentation/coreaudio/audiohardwaredevice/start(at:flags:ioprocid:))
- [func stop(IOProcID: AudioDeviceIOProcID?) throws](/documentation/coreaudio/audiohardwaredevice/stop(ioprocid:))
- [func toggleHogMode() throws -> pid_t](/documentation/coreaudio/audiohardwaredevice/togglehogmode())
- [func translateTime(AudioTimeStamp) throws -> AudioTimeStamp](/documentation/coreaudio/audiohardwaredevice/translatetime(_:))
- [AudioHardwareObject](/documentation/coreaudio/audiohardwareobject)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwareobject/init(id:))

### Instance Properties

- [var baseClassID: AudioClassID](/documentation/coreaudio/audiohardwareobject/baseclassid)
- [var classID: AudioClassID](/documentation/coreaudio/audiohardwareobject/classid)
- [var creatorBundleID: String](/documentation/coreaudio/audiohardwareobject/creatorbundleid)
- [var delegates: [any PropertyListenerDelegate]](/documentation/coreaudio/audiohardwareobject/delegates)
- [var firmwareVersion: String](/documentation/coreaudio/audiohardwareobject/firmwareversion)
- [let id: AudioObjectID](/documentation/coreaudio/audiohardwareobject/id)
- [var isIdentifying: Bool](/documentation/coreaudio/audiohardwareobject/isidentifying)
- [var manufacturer: String](/documentation/coreaudio/audiohardwareobject/manufacturer)
- [var modelName: String](/documentation/coreaudio/audiohardwareobject/modelname)
- [var name: String](/documentation/coreaudio/audiohardwareobject/name)
- [var ownedObjects: [AudioHardwareObject]](/documentation/coreaudio/audiohardwareobject/ownedobjects)
- [var owner: AudioHardwareObject?](/documentation/coreaudio/audiohardwareobject/owner)
- [var serialNumber: String](/documentation/coreaudio/audiohardwareobject/serialnumber)

### Instance Methods

- [func addListener(forProperties: [AudioObjectPropertyAddress], dispatchQueue: dispatch_queue_t?) throws](/documentation/coreaudio/audiohardwareobject/addlistener(forproperties:dispatchqueue:))
- [func hasProperty(address: AudioObjectPropertyAddress) -> Bool](/documentation/coreaudio/audiohardwareobject/hasproperty(address:))
- [func isPropertySettable(address: AudioObjectPropertyAddress) throws -> Bool](/documentation/coreaudio/audiohardwareobject/ispropertysettable(address:))
- [func propertyData(address: AudioObjectPropertyAddress, qualifier: Data?) throws -> Data](/documentation/coreaudio/audiohardwareobject/propertydata(address:qualifier:))
- [func propertyDataSize(address: AudioObjectPropertyAddress, qualifier: Data?) throws -> Int](/documentation/coreaudio/audiohardwareobject/propertydatasize(address:qualifier:))
- [func removeListener(forProperties: [AudioObjectPropertyAddress], dispatchQueue: dispatch_queue_t?) throws](/documentation/coreaudio/audiohardwareobject/removelistener(forproperties:dispatchqueue:))
- [func setCreatorBundleID(String) throws](/documentation/coreaudio/audiohardwareobject/setcreatorbundleid(_:))
- [func setIsIdentifying(Bool) throws](/documentation/coreaudio/audiohardwareobject/setisidentifying(_:))
- [func setName(String) throws](/documentation/coreaudio/audiohardwareobject/setname(_:))
- [func setPropertyData(address: AudioObjectPropertyAddress, qualifier: Data?, data: Data) throws](/documentation/coreaudio/audiohardwareobject/setpropertydata(address:qualifier:data:)-4kzgv)
- [func setPropertyData(address: AudioObjectPropertyAddress, qualifier: Data?, data: inout Data) async throws](/documentation/coreaudio/audiohardwareobject/setpropertydata(address:qualifier:data:)-7cfn)
- [AudioHardwarePlugin](/documentation/coreaudio/audiohardwareplugin)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwareplugin/init(id:))

### Instance Properties

- [var boxes: [AudioHardwareBox]](/documentation/coreaudio/audiohardwareplugin/boxes)
- [var bundleID: String](/documentation/coreaudio/audiohardwareplugin/bundleid)
- [var clocks: [AudioHardwareClock]](/documentation/coreaudio/audiohardwareplugin/clocks)
- [var devices: [AudioHardwareDevice]](/documentation/coreaudio/audiohardwareplugin/devices)

### Instance Methods

- [func box(forUID: String) throws -> AudioHardwareBox?](/documentation/coreaudio/audiohardwareplugin/box(foruid:))
- [func clock(forUID: String) throws -> AudioHardwareClock?](/documentation/coreaudio/audiohardwareplugin/clock(foruid:))
- [func device(forUID: String) throws -> AudioHardwareDevice?](/documentation/coreaudio/audiohardwareplugin/device(foruid:))
- [AudioHardwareProcess](/documentation/coreaudio/audiohardwareprocess)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwareprocess/init(id:))

### Instance Properties

- [var bundleID: String?](/documentation/coreaudio/audiohardwareprocess/bundleid)
- [var devices: [AudioHardwareDevice]](/documentation/coreaudio/audiohardwareprocess/devices)
- [var isRunning: Bool](/documentation/coreaudio/audiohardwareprocess/isrunning)
- [var isRunningInput: Bool](/documentation/coreaudio/audiohardwareprocess/isrunninginput)
- [var isRunningOutput: Bool](/documentation/coreaudio/audiohardwareprocess/isrunningoutput)
- [var pid: pid_t](/documentation/coreaudio/audiohardwareprocess/pid)
- [AudioHardwareStream](/documentation/coreaudio/audiohardwarestream)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwarestream/init(id:))

### Instance Properties

- [var availablePhysicalFormats: [AudioStreamRangedDescription]](/documentation/coreaudio/audiohardwarestream/availablephysicalformats)
- [var availableVirtualFormats: [AudioStreamRangedDescription]](/documentation/coreaudio/audiohardwarestream/availablevirtualformats)
- [var direction: AudioHardwareDirection](/documentation/coreaudio/audiohardwarestream/direction)
- [var isActive: Bool](/documentation/coreaudio/audiohardwarestream/isactive)
- [var latency: Int](/documentation/coreaudio/audiohardwarestream/latency)
- [var physicalFormat: AudioStreamBasicDescription](/documentation/coreaudio/audiohardwarestream/physicalformat)
- [var startingChannel: Int](/documentation/coreaudio/audiohardwarestream/startingchannel)
- [var terminalType: UInt32](/documentation/coreaudio/audiohardwarestream/terminaltype)
- [var virtualFormat: AudioStreamBasicDescription](/documentation/coreaudio/audiohardwarestream/virtualformat)

### Instance Methods

- [func setIsActive(Bool) throws](/documentation/coreaudio/audiohardwarestream/setisactive(_:))
- [func setPhysicalFormat(AudioStreamBasicDescription) throws](/documentation/coreaudio/audiohardwarestream/setphysicalformat(_:))
- [func setVirtualFormat(AudioStreamBasicDescription) throws](/documentation/coreaudio/audiohardwarestream/setvirtualformat(_:))
- [AudioHardwareSystem](/documentation/coreaudio/audiohardwaresystem)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwaresystem/init(id:))

### Instance Properties

- [var allowsHogMode: Bool](/documentation/coreaudio/audiohardwaresystem/allowshogmode)
- [var allowsSleeping: Bool](/documentation/coreaudio/audiohardwaresystem/allowssleeping)
- [var allowsUnloading: Bool](/documentation/coreaudio/audiohardwaresystem/allowsunloading)
- [var boxes: [AudioHardwareBox]](/documentation/coreaudio/audiohardwaresystem/boxes)
- [var clocks: [AudioHardwareClock]](/documentation/coreaudio/audiohardwaresystem/clocks)
- [var defaultInputDevice: AudioHardwareDevice?](/documentation/coreaudio/audiohardwaresystem/defaultinputdevice)
- [var defaultOutputDevice: AudioHardwareDevice?](/documentation/coreaudio/audiohardwaresystem/defaultoutputdevice)
- [var defaultSoundEffectsDevice: AudioHardwareDevice?](/documentation/coreaudio/audiohardwaresystem/defaultsoundeffectsdevice)
- [var devices: [AudioHardwareDevice]](/documentation/coreaudio/audiohardwaresystem/devices)
- [var isInitializingOrExiting: Bool](/documentation/coreaudio/audiohardwaresystem/isinitializingorexiting)
- [var isProcessInputMuted: Bool](/documentation/coreaudio/audiohardwaresystem/isprocessinputmuted)
- [var plugins: [AudioHardwarePlugin]](/documentation/coreaudio/audiohardwaresystem/plugins)
- [var powerHint: AudioHardwarePowerHint](/documentation/coreaudio/audiohardwaresystem/powerhint)
- [var processes: [AudioHardwareProcess]](/documentation/coreaudio/audiohardwaresystem/processes)
- [var shouldMixStereoToMono: Bool](/documentation/coreaudio/audiohardwaresystem/shouldmixstereotomono)
- [var taps: [AudioHardwareTap]](/documentation/coreaudio/audiohardwaresystem/taps)

### Instance Methods

- [func box(forUID: String) throws -> AudioHardwareBox?](/documentation/coreaudio/audiohardwaresystem/box(foruid:))
- [func clock(forUID: String) throws -> AudioHardwareClock?](/documentation/coreaudio/audiohardwaresystem/clock(foruid:))
- [func destroyAggregateDevice(AudioHardwareAggregateDevice) throws](/documentation/coreaudio/audiohardwaresystem/destroyaggregatedevice(_:))
- [func destroyProcessTap(AudioHardwareTap) throws](/documentation/coreaudio/audiohardwaresystem/destroyprocesstap(_:))
- [func device(forUID: String) throws -> AudioHardwareDevice?](/documentation/coreaudio/audiohardwaresystem/device(foruid:))
- [func makeAggregateDevice(description: [String : Any]) throws -> AudioHardwareAggregateDevice?](/documentation/coreaudio/audiohardwaresystem/makeaggregatedevice(description:))
- [func makeProcessTap(description: CATapDescription) throws -> AudioHardwareTap?](/documentation/coreaudio/audiohardwaresystem/makeprocesstap(description:))
- [func plugin(forBundleID: String) throws -> AudioHardwarePlugin?](/documentation/coreaudio/audiohardwaresystem/plugin(forbundleid:))
- [func process(for: pid_t) throws -> AudioHardwareProcess?](/documentation/coreaudio/audiohardwaresystem/process(for:))
- [func setAllowsHogMode(Bool) throws](/documentation/coreaudio/audiohardwaresystem/setallowshogmode(_:))
- [func setAllowsSleeping(Bool) throws](/documentation/coreaudio/audiohardwaresystem/setallowssleeping(_:))
- [func setAllowsUnloading(Bool) throws](/documentation/coreaudio/audiohardwaresystem/setallowsunloading(_:))
- [func setDefaultInputDevice(AudioHardwareDevice) throws](/documentation/coreaudio/audiohardwaresystem/setdefaultinputdevice(_:))
- [func setDefaultOutputDevice(AudioHardwareDevice) throws](/documentation/coreaudio/audiohardwaresystem/setdefaultoutputdevice(_:))
- [func setDefaultSoundEffectsDevice(AudioHardwareDevice) throws](/documentation/coreaudio/audiohardwaresystem/setdefaultsoundeffectsdevice(_:))
- [func setIsProcessInputMuted(Bool) throws](/documentation/coreaudio/audiohardwaresystem/setisprocessinputmuted(_:))
- [func setPowerHint(AudioHardwarePowerHint) throws](/documentation/coreaudio/audiohardwaresystem/setpowerhint(_:))
- [func setShouldMixStereoToMono(Bool) throws](/documentation/coreaudio/audiohardwaresystem/setshouldmixstereotomono(_:))
- [func tap(forUID: String) throws -> AudioHardwareTap?](/documentation/coreaudio/audiohardwaresystem/tap(foruid:))
- [func unload() throws](/documentation/coreaudio/audiohardwaresystem/unload())

### Type Properties

- [static let shared: AudioHardwareSystem](/documentation/coreaudio/audiohardwaresystem/shared)
- [AudioHardwareTap](/documentation/coreaudio/audiohardwaretap)

### Initializers

- [init(id: AudioObjectID)](/documentation/coreaudio/audiohardwaretap/init(id:))

### Instance Properties

- [var description: CATapDescription](/documentation/coreaudio/audiohardwaretap/description)
- [var format: AudioStreamBasicDescription](/documentation/coreaudio/audiohardwaretap/format)
- [var uid: String](/documentation/coreaudio/audiohardwaretap/uid)

### Instance Methods

- [func setDescription(CATapDescription) throws](/documentation/coreaudio/audiohardwaretap/setdescription(_:))
- [CATapDescription](/documentation/coreaudio/catapdescription)

### Initializers

- [init()](/documentation/coreaudio/catapdescription/init())
- [convenience init(excludingProcesses: [AudioObjectID], deviceUID: String, stream: UInt)](/documentation/coreaudio/catapdescription/init(excludingprocesses:deviceuid:stream:))
- [convenience init(monoGlobalTapButExcludeProcesses: [AudioObjectID])](/documentation/coreaudio/catapdescription/init(monoglobaltapbutexcludeprocesses:))
- [convenience init(monoMixdownOfProcesses: [AudioObjectID])](/documentation/coreaudio/catapdescription/init(monomixdownofprocesses:))
- [convenience init(processes: [AudioObjectID], deviceUID: String, stream: UInt)](/documentation/coreaudio/catapdescription/init(processes:deviceuid:stream:))
- [convenience init(stereoGlobalTapButExcludeProcesses: [AudioObjectID])](/documentation/coreaudio/catapdescription/init(stereoglobaltapbutexcludeprocesses:))
- [convenience init(stereoMixdownOfProcesses: [AudioObjectID])](/documentation/coreaudio/catapdescription/init(stereomixdownofprocesses:))

### Instance Properties

- [var bundleIDs: [String]](/documentation/coreaudio/catapdescription/bundleids)
- [var deviceUID: String?](/documentation/coreaudio/catapdescription/deviceuid)
- [var isExclusive: Bool](/documentation/coreaudio/catapdescription/isexclusive)
- [var isMixdown: Bool](/documentation/coreaudio/catapdescription/ismixdown)
- [var isMono: Bool](/documentation/coreaudio/catapdescription/ismono)
- [var isPrivate: Bool](/documentation/coreaudio/catapdescription/isprivate)
- [var isProcessRestoreEnabled: Bool](/documentation/coreaudio/catapdescription/isprocessrestoreenabled)
- [var muteBehavior: CATapMuteBehavior](/documentation/coreaudio/catapdescription/mutebehavior)
- [var name: String](/documentation/coreaudio/catapdescription/name)
- [var processes: [AudioObjectID]](/documentation/coreaudio/catapdescription/processes-1m4cr)
- [var stream: UInt?](/documentation/coreaudio/catapdescription/stream-ajk3)
- [var uuid: UUID](/documentation/coreaudio/catapdescription/uuid)

## Protocols

- [PropertyListenerDelegate](/documentation/coreaudio/propertylistenerdelegate)

### Instance Methods

- [func propertiesChanged(properties: [AudioObjectPropertyAddress])](/documentation/coreaudio/propertylistenerdelegate/propertieschanged(properties:))

## Structures

- [AudioHardwareError](/documentation/coreaudio/audiohardwareerror)

### Initializers

- [init(OSStatus)](/documentation/coreaudio/audiohardwareerror/init(_:))

### Instance Properties

- [let error: OSStatus](/documentation/coreaudio/audiohardwareerror/error)
- [var errorDescription: String?](/documentation/coreaudio/audiohardwareerror/errordescription)
- [ManagedAudioChannelLayout](/documentation/coreaudio/managedaudiochannellayout)

### Structures

- [ManagedAudioChannelLayout.ChannelDescriptions](/documentation/coreaudio/managedaudiochannellayout/channeldescriptions-swift.struct)

### Initializers

- [init(audioChannelLayoutPointer: AudioChannelLayout.UnsafePointer, deallocator: (AudioChannelLayout.UnsafePointer) -> Void)](/documentation/coreaudio/managedaudiochannellayout/init(audiochannellayoutpointer:deallocator:))
- [init(channelDescriptions: [AudioChannelDescription])](/documentation/coreaudio/managedaudiochannellayout/init(channeldescriptions:))
- [init(maximumDescriptions: Int)](/documentation/coreaudio/managedaudiochannellayout/init(maximumdescriptions:))
- [init(tag: AudioChannelLayoutTag)](/documentation/coreaudio/managedaudiochannellayout/init(tag:))

### Instance Properties

- [var bitmap: AudioChannelBitmap](/documentation/coreaudio/managedaudiochannellayout/bitmap)
- [var channelDescriptions: ManagedAudioChannelLayout.ChannelDescriptions](/documentation/coreaudio/managedaudiochannellayout/channeldescriptions-swift.property)
- [var numberOfChannels: Int](/documentation/coreaudio/managedaudiochannellayout/numberofchannels)
- [var sizeInBytes: Int](/documentation/coreaudio/managedaudiochannellayout/sizeinbytes)
- [var tag: AudioChannelLayoutTag](/documentation/coreaudio/managedaudiochannellayout/tag)

### Instance Methods

- [func setAllToUnknown()](/documentation/coreaudio/managedaudiochannellayout/setalltounknown())
- [func withUnsafeMutablePointer<Result>((UnsafeMutablePointer<AudioChannelLayout>) throws -> Result) rethrows -> Result](/documentation/coreaudio/managedaudiochannellayout/withunsafemutablepointer(_:))
- [func withUnsafePointer<Result>((UnsafePointer<AudioChannelLayout>) throws -> Result) rethrows -> Result](/documentation/coreaudio/managedaudiochannellayout/withunsafepointer(_:))

## Variables

- [var kAudioDevicePropertyWantsControlsRestored: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertywantscontrolsrestored)
- [var kAudioDevicePropertyWantsStreamFormatsRestored: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertywantsstreamformatsrestored)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
