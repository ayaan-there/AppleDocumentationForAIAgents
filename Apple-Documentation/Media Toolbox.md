# Media Toolbox Documentation

Source: https://sosumi.ai/documentation/mediatoolbox

---
title: Media Toolbox
source: https://developer.apple.com/documentation/mediatoolbox
timestamp: 2026-02-13T18:59:29.180Z
---

## Professional video workflows

- [func MTRegisterProfessionalVideoWorkflowFormatReaders()](/documentation/mediatoolbox/mtregisterprofessionalvideoworkflowformatreaders())

## Audio Taps

- [func MTAudioProcessingTapCreate(CFAllocator?, UnsafePointer<MTAudioProcessingTapCallbacks>, MTAudioProcessingTapCreationFlags, UnsafeMutablePointer<MTAudioProcessingTap?>) -> OSStatus](/documentation/mediatoolbox/mtaudioprocessingtapcreate(_:_:_:_:))

### Flags

- [MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/mtaudioprocessingtapcreationflags)

#### Flags

- [var kMTAudioProcessingTapCreationFlag_PreEffects: MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/kmtaudioprocessingtapcreationflag_preeffects)
- [var kMTAudioProcessingTapCreationFlag_PostEffects: MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/kmtaudioprocessingtapcreationflag_posteffects)

### Callbacks

- [MTAudioProcessingTapCallbacks](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks)

#### Fields

- [var version: Int32](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/version)
- [var clientInfo: UnsafeMutableRawPointer?](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/clientinfo)
- [var `init`: MTAudioProcessingTapInitCallback?](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/init)
- [var finalize: MTAudioProcessingTapFinalizeCallback?](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/finalize)
- [var prepare: MTAudioProcessingTapPrepareCallback?](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/prepare)
- [var unprepare: MTAudioProcessingTapUnprepareCallback?](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/unprepare)
- [var process: MTAudioProcessingTapProcessCallback](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/process)

#### Callback functions

- [MTAudioProcessingTapInitCallback](/documentation/mediatoolbox/mtaudioprocessingtapinitcallback)
- [MTAudioProcessingTapPrepareCallback](/documentation/mediatoolbox/mtaudioprocessingtappreparecallback)
- [MTAudioProcessingTapProcessCallback](/documentation/mediatoolbox/mtaudioprocessingtapprocesscallback)
- [MTAudioProcessingTapUnprepareCallback](/documentation/mediatoolbox/mtaudioprocessingtapunpreparecallback)

##### Flags

- [MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/mtaudioprocessingtapcreationflags)

###### Flags

- [var kMTAudioProcessingTapCreationFlag_PreEffects: MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/kmtaudioprocessingtapcreationflag_preeffects)
- [var kMTAudioProcessingTapCreationFlag_PostEffects: MTAudioProcessingTapCreationFlags](/documentation/mediatoolbox/kmtaudioprocessingtapcreationflag_posteffects)
- [MTAudioProcessingTapFinalizeCallback](/documentation/mediatoolbox/mtaudioprocessingtapfinalizecallback)

#### Versions

- [var kMTAudioProcessingTapCallbacksVersion_0: Int32](/documentation/mediatoolbox/kmtaudioprocessingtapcallbacksversion_0)

#### Initializers

- [init(version: Int32, clientInfo: UnsafeMutableRawPointer?, init: MTAudioProcessingTapInitCallback?, finalize: MTAudioProcessingTapFinalizeCallback?, prepare: MTAudioProcessingTapPrepareCallback?, unprepare: MTAudioProcessingTapUnprepareCallback?, process: MTAudioProcessingTapProcessCallback)](/documentation/mediatoolbox/mtaudioprocessingtapcallbacks/init(version:clientinfo:init:finalize:prepare:unprepare:process:))
- [func MTAudioProcessingTapGetSourceAudio(MTAudioProcessingTap, CMItemCount, UnsafeMutablePointer<AudioBufferList>, UnsafeMutablePointer<MTAudioProcessingTapFlags>?, UnsafeMutablePointer<CMTimeRange>?, UnsafeMutablePointer<CMItemCount>?) -> OSStatus](/documentation/mediatoolbox/mtaudioprocessingtapgetsourceaudio(_:_:_:_:_:_:))
- [func MTAudioProcessingTapGetStorage(MTAudioProcessingTap) -> UnsafeMutableRawPointer](/documentation/mediatoolbox/mtaudioprocessingtapgetstorage(_:))
- [func MTAudioProcessingTapGetTypeID() -> CFTypeID](/documentation/mediatoolbox/mtaudioprocessingtapgettypeid())
- [MTAudioProcessingTapFlags](/documentation/mediatoolbox/mtaudioprocessingtapflags)

### Flags

- [var kMTAudioProcessingTapFlag_EndOfStream: MTAudioProcessingTapFlags](/documentation/mediatoolbox/kmtaudioprocessingtapflag_endofstream)
- [var kMTAudioProcessingTapFlag_StartOfStream: MTAudioProcessingTapFlags](/documentation/mediatoolbox/kmtaudioprocessingtapflag_startofstream)
- [MTAudioProcessingTap](/documentation/mediatoolbox/mtaudioprocessingtap)

## Utility

- [func MTCopyLocalizedNameForMediaType(CMMediaType) -> CFString?](/documentation/mediatoolbox/mtcopylocalizednameformediatype(_:))
- [func MTCopyLocalizedNameForMediaSubType(CMMediaType, FourCharCode) -> CFString?](/documentation/mediatoolbox/mtcopylocalizednameformediasubtype(_:_:))

## Enumerations

- [Anonymous Enumerations](/documentation/mediatoolbox/anonymous-enums)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
