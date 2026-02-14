# Core Media Documentation

Source: https://sosumi.ai/documentation/coremedia

---
title: Core Media
source: https://developer.apple.com/documentation/coremedia
timestamp: 2026-02-13T18:55:26.652Z
---

## Sample Processing

- [CMSampleBuffer](/documentation/coremedia/cmsamplebuffer-api)

### Creating Sample Buffers

- [func CMSampleBufferCreateReady(allocator: CFAllocator?, dataBuffer: CMBlockBuffer?, formatDescription: CMFormatDescription?, sampleCount: CMItemCount, sampleTimingEntryCount: CMItemCount, sampleTimingArray: UnsafePointer<CMSampleTimingInfo>?, sampleSizeEntryCount: CMItemCount, sampleSizeArray: UnsafePointer<Int>?, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreateready(allocator:databuffer:formatdescription:samplecount:sampletimingentrycount:sampletimingarray:samplesizeentrycount:samplesizearray:samplebufferout:))
- [func CMSampleBufferCreateReadyWithImageBuffer(allocator: CFAllocator?, imageBuffer: CVImageBuffer, formatDescription: CMVideoFormatDescription, sampleTiming: UnsafePointer<CMSampleTimingInfo>, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreatereadywithimagebuffer(allocator:imagebuffer:formatdescription:sampletiming:samplebufferout:))
- [func CMAudioSampleBufferCreateReadyWithPacketDescriptions(allocator: CFAllocator?, dataBuffer: CMBlockBuffer, formatDescription: CMFormatDescription, sampleCount: CMItemCount, presentationTimeStamp: CMTime, packetDescriptions: UnsafePointer<AudioStreamPacketDescription>?, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmaudiosamplebuffercreatereadywithpacketdescriptions(allocator:databuffer:formatdescription:samplecount:presentationtimestamp:packetdescriptions:samplebufferout:))
- [func CMSampleBufferCreateWithMakeDataReadyHandler(CFAllocator?, CMBlockBuffer?, Bool, CMFormatDescription?, CMItemCount, CMItemCount, UnsafePointer<CMSampleTimingInfo>?, CMItemCount, UnsafePointer<Int>?, UnsafeMutablePointer<CMSampleBuffer?>, CMSampleBufferMakeDataReadyHandler?) -> OSStatus](/documentation/coremedia/cmsamplebuffercreatewithmakedatareadyhandler(_:_:_:_:_:_:_:_:_:_:_:))

#### Handlers

- [CMSampleBufferMakeDataReadyHandler](/documentation/coremedia/cmsamplebuffermakedatareadyhandler)
- [func CMSampleBufferCreateForImageBufferWithMakeDataReadyHandler(CFAllocator?, CVImageBuffer, Bool, CMVideoFormatDescription, UnsafePointer<CMSampleTimingInfo>, UnsafeMutablePointer<CMSampleBuffer?>, CMSampleBufferMakeDataReadyHandler?) -> OSStatus](/documentation/coremedia/cmsamplebuffercreateforimagebufferwithmakedatareadyhandler(_:_:_:_:_:_:_:))

#### Handlers

- [CMSampleBufferMakeDataReadyHandler](/documentation/coremedia/cmsamplebuffermakedatareadyhandler)
- [func CMAudioSampleBufferCreateWithPacketDescriptionsAndMakeDataReadyHandler(CFAllocator?, CMBlockBuffer?, Bool, CMFormatDescription, CMItemCount, CMTime, UnsafePointer<AudioStreamPacketDescription>?, UnsafeMutablePointer<CMSampleBuffer?>, CMSampleBufferMakeDataReadyHandler?) -> OSStatus](/documentation/coremedia/cmaudiosamplebuffercreatewithpacketdescriptionsandmakedatareadyhandler(_:_:_:_:_:_:_:_:_:))

#### Handlers

- [CMSampleBufferMakeDataReadyHandler](/documentation/coremedia/cmsamplebuffermakedatareadyhandler)
- [func CMSampleBufferCreate(allocator: CFAllocator?, dataBuffer: CMBlockBuffer?, dataReady: Bool, makeDataReadyCallback: CMSampleBufferMakeDataReadyCallback?, refcon: UnsafeMutableRawPointer?, formatDescription: CMFormatDescription?, sampleCount: CMItemCount, sampleTimingEntryCount: CMItemCount, sampleTimingArray: UnsafePointer<CMSampleTimingInfo>?, sampleSizeEntryCount: CMItemCount, sampleSizeArray: UnsafePointer<Int>?, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreate(allocator:databuffer:dataready:makedatareadycallback:refcon:formatdescription:samplecount:sampletimingentrycount:sampletimingarray:samplesizeentrycount:samplesizearray:samplebufferout:))

#### Callbacks

- [CMSampleBufferMakeDataReadyCallback](/documentation/coremedia/cmsamplebuffermakedatareadycallback)
- [func CMSampleBufferCreateForImageBuffer(allocator: CFAllocator?, imageBuffer: CVImageBuffer, dataReady: Bool, makeDataReadyCallback: CMSampleBufferMakeDataReadyCallback?, refcon: UnsafeMutableRawPointer?, formatDescription: CMVideoFormatDescription, sampleTiming: UnsafePointer<CMSampleTimingInfo>, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreateforimagebuffer(allocator:imagebuffer:dataready:makedatareadycallback:refcon:formatdescription:sampletiming:samplebufferout:))

#### Callbacks

- [CMSampleBufferMakeDataReadyCallback](/documentation/coremedia/cmsamplebuffermakedatareadycallback)
- [func CMAudioSampleBufferCreateWithPacketDescriptions(allocator: CFAllocator?, dataBuffer: CMBlockBuffer?, dataReady: Bool, makeDataReadyCallback: CMSampleBufferMakeDataReadyCallback?, refcon: UnsafeMutableRawPointer?, formatDescription: CMFormatDescription, sampleCount: CMItemCount, presentationTimeStamp: CMTime, packetDescriptions: UnsafePointer<AudioStreamPacketDescription>?, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmaudiosamplebuffercreatewithpacketdescriptions(allocator:databuffer:dataready:makedatareadycallback:refcon:formatdescription:samplecount:presentationtimestamp:packetdescriptions:samplebufferout:))

#### Callbacks

- [CMSampleBufferMakeDataReadyCallback](/documentation/coremedia/cmsamplebuffermakedatareadycallback)

### Copying Sample Buffers

- [func CMSampleBufferCreateCopy(allocator: CFAllocator?, sampleBuffer: CMSampleBuffer, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreatecopy(allocator:samplebuffer:samplebufferout:))
- [func CMSampleBufferCreateCopyWithNewTiming(allocator: CFAllocator?, sampleBuffer: CMSampleBuffer, sampleTimingEntryCount: CMItemCount, sampleTimingArray: UnsafePointer<CMSampleTimingInfo>?, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercreatecopywithnewtiming(allocator:samplebuffer:sampletimingentrycount:sampletimingarray:samplebufferout:))
- [func CMSampleBufferCopySampleBufferForRange(allocator: CFAllocator?, sampleBuffer: CMSampleBuffer, sampleRange: CFRange, sampleBufferOut: UnsafeMutablePointer<CMSampleBuffer?>) -> OSStatus](/documentation/coremedia/cmsamplebuffercopysamplebufferforrange(allocator:samplebuffer:samplerange:samplebufferout:))

### Determining Readiness

- [func CMSampleBufferDataIsReady(CMSampleBuffer) -> Bool](/documentation/coremedia/cmsamplebufferdataisready(_:))
- [func CMSampleBufferSetDataReady(CMSampleBuffer) -> OSStatus](/documentation/coremedia/cmsamplebuffersetdataready(_:))
- [func CMSampleBufferSetDataFailed(CMSampleBuffer, status: OSStatus) -> OSStatus](/documentation/coremedia/cmsamplebuffersetdatafailed(_:status:))
- [func CMSampleBufferHasDataFailed(CMSampleBuffer, statusOut: UnsafeMutablePointer<OSStatus>?) -> Bool](/documentation/coremedia/cmsamplebufferhasdatafailed(_:statusout:))
- [func CMSampleBufferMakeDataReady(CMSampleBuffer) -> OSStatus](/documentation/coremedia/cmsamplebuffermakedataready(_:))
- [func CMSampleBufferTrackDataReadiness(CMSampleBuffer, sampleBufferToTrack: CMSampleBuffer) -> OSStatus](/documentation/coremedia/cmsamplebuffertrackdatareadiness(_:samplebuffertotrack:))

### Invalidating Sample Buffers

- [func CMSampleBufferSetInvalidateHandler(CMSampleBuffer, invalidateHandler: CMSampleBufferInvalidateHandler) -> OSStatus](/documentation/coremedia/cmsamplebuffersetinvalidatehandler(_:invalidatehandler:))

#### Handlers

- [CMSampleBufferInvalidateHandler](/documentation/coremedia/cmsamplebufferinvalidatehandler)
- [func CMSampleBufferInvalidate(CMSampleBuffer) -> OSStatus](/documentation/coremedia/cmsamplebufferinvalidate(_:))
- [func CMSampleBufferIsValid(CMSampleBuffer) -> Bool](/documentation/coremedia/cmsamplebufferisvalid(_:))
- [func CMSampleBufferSetInvalidateCallback(CMSampleBuffer, callback: CMSampleBufferInvalidateCallback, refcon: UInt64) -> OSStatus](/documentation/coremedia/cmsamplebuffersetinvalidatecallback(_:callback:refcon:))

#### Callbacks

- [CMSampleBufferInvalidateCallback](/documentation/coremedia/cmsamplebufferinvalidatecallback)

### Inspecting Size Information

- [func CMSampleBufferGetNumSamples(CMSampleBuffer) -> CMItemCount](/documentation/coremedia/cmsamplebuffergetnumsamples(_:))
- [func CMSampleBufferGetTotalSampleSize(CMSampleBuffer) -> Int](/documentation/coremedia/cmsamplebuffergettotalsamplesize(_:))
- [func CMSampleBufferGetSampleSize(CMSampleBuffer, at: CMItemIndex) -> Int](/documentation/coremedia/cmsamplebuffergetsamplesize(_:at:))
- [func CMSampleBufferGetSampleSizeArray(CMSampleBuffer, entryCount: CMItemCount, arrayToFill: UnsafeMutablePointer<Int>?, entriesNeededOut: UnsafeMutablePointer<CMItemCount>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetsamplesizearray(_:entrycount:arraytofill:entriesneededout:))

### Inspecting Duration and Timing

- [func CMSampleBufferGetDuration(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetduration(_:))
- [func CMSampleBufferGetDecodeTimeStamp(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetdecodetimestamp(_:))
- [func CMSampleBufferGetPresentationTimeStamp(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetpresentationtimestamp(_:))
- [func CMSampleBufferGetOutputDuration(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetoutputduration(_:))
- [func CMSampleBufferGetOutputDecodeTimeStamp(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetoutputdecodetimestamp(_:))
- [func CMSampleBufferGetOutputPresentationTimeStamp(CMSampleBuffer) -> CMTime](/documentation/coremedia/cmsamplebuffergetoutputpresentationtimestamp(_:))
- [func CMSampleBufferSetOutputPresentationTimeStamp(CMSampleBuffer, newValue: CMTime) -> OSStatus](/documentation/coremedia/cmsamplebuffersetoutputpresentationtimestamp(_:newvalue:))
- [func CMSampleBufferGetSampleTimingInfo(CMSampleBuffer, at: CMItemIndex, timingInfoOut: UnsafeMutablePointer<CMSampleTimingInfo>) -> OSStatus](/documentation/coremedia/cmsamplebuffergetsampletiminginfo(_:at:timinginfoout:))
- [func CMSampleBufferGetSampleTimingInfoArray(CMSampleBuffer, entryCount: CMItemCount, arrayToFill: UnsafeMutablePointer<CMSampleTimingInfo>?, entriesNeededOut: UnsafeMutablePointer<CMItemCount>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetsampletiminginfoarray(_:entrycount:arraytofill:entriesneededout:))
- [func CMSampleBufferGetOutputSampleTimingInfoArray(CMSampleBuffer, entryCount: CMItemCount, arrayToFill: UnsafeMutablePointer<CMSampleTimingInfo>?, entriesNeededOut: UnsafeMutablePointer<CMItemCount>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetoutputsampletiminginfoarray(_:entrycount:arraytofill:entriesneededout:))

### Accessing the Format Description

- [func CMSampleBufferGetFormatDescription(CMSampleBuffer) -> CMFormatDescription?](/documentation/coremedia/cmsamplebuffergetformatdescription(_:))

### Modifying Sample Buffers

- [func CMSampleBufferGetDataBuffer(CMSampleBuffer) -> CMBlockBuffer?](/documentation/coremedia/cmsamplebuffergetdatabuffer(_:))
- [func CMSampleBufferSetDataBuffer(CMSampleBuffer, newValue: CMBlockBuffer) -> OSStatus](/documentation/coremedia/cmsamplebuffersetdatabuffer(_:newvalue:))
- [func CMSampleBufferGetImageBuffer(CMSampleBuffer) -> CVImageBuffer?](/documentation/coremedia/cmsamplebuffergetimagebuffer(_:))
- [func CMSampleBufferGetAudioBufferListWithRetainedBlockBuffer(CMSampleBuffer, bufferListSizeNeededOut: UnsafeMutablePointer<Int>?, bufferListOut: UnsafeMutablePointer<AudioBufferList>?, bufferListSize: Int, blockBufferAllocator: CFAllocator?, blockBufferMemoryAllocator: CFAllocator?, flags: UInt32, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetaudiobufferlistwithretainedblockbuffer(_:bufferlistsizeneededout:bufferlistout:bufferlistsize:blockbufferallocator:blockbuffermemoryallocator:flags:blockbufferout:))
- [func CMSampleBufferSetDataBufferFromAudioBufferList(CMSampleBuffer, blockBufferAllocator: CFAllocator?, blockBufferMemoryAllocator: CFAllocator?, flags: UInt32, bufferList: UnsafePointer<AudioBufferList>) -> OSStatus](/documentation/coremedia/cmsamplebuffersetdatabufferfromaudiobufferlist(_:blockbufferallocator:blockbuffermemoryallocator:flags:bufferlist:))
- [func CMSampleBufferCopyPCMDataIntoAudioBufferList(CMSampleBuffer, at: Int32, frameCount: Int32, into: UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/coremedia/cmsamplebuffercopypcmdataintoaudiobufferlist(_:at:framecount:into:))
- [func CMSampleBufferGetAudioStreamPacketDescriptions(CMSampleBuffer, allocatedSize: Int, packetDescriptionsOut: UnsafeMutablePointer<AudioStreamPacketDescription>?, packetDescriptionsSizeNeededOut: UnsafeMutablePointer<Int>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetaudiostreampacketdescriptions(_:allocatedsize:packetdescriptionsout:packetdescriptionssizeneededout:))
- [func CMSampleBufferGetAudioStreamPacketDescriptionsPtr(CMSampleBuffer, packetDescriptionsPointerOut: UnsafeMutablePointer<UnsafePointer<AudioStreamPacketDescription>?>?, sizeOut: UnsafeMutablePointer<Int>?) -> OSStatus](/documentation/coremedia/cmsamplebuffergetaudiostreampacketdescriptionsptr(_:packetdescriptionspointerout:sizeout:))

### Managing Attachments

- [func CMSampleBufferGetSampleAttachmentsArray(CMSampleBuffer, createIfNecessary: Bool) -> CFArray?](/documentation/coremedia/cmsamplebuffergetsampleattachmentsarray(_:createifnecessary:))
- [Sample Attachment Keys](/documentation/coremedia/sample-attachment-keys)

#### Sample Keys

- [let kCMSampleAttachmentKey_NotSync: CFString](/documentation/coremedia/kcmsampleattachmentkey_notsync)
- [let kCMSampleAttachmentKey_PartialSync: CFString](/documentation/coremedia/kcmsampleattachmentkey_partialsync)
- [let kCMSampleAttachmentKey_DependsOnOthers: CFString](/documentation/coremedia/kcmsampleattachmentkey_dependsonothers)
- [let kCMSampleAttachmentKey_IsDependedOnByOthers: CFString](/documentation/coremedia/kcmsampleattachmentkey_isdependedonbyothers)
- [let kCMSampleAttachmentKey_DisplayImmediately: CFString](/documentation/coremedia/kcmsampleattachmentkey_displayimmediately)
- [let kCMSampleAttachmentKey_DoNotDisplay: CFString](/documentation/coremedia/kcmsampleattachmentkey_donotdisplay)
- [let kCMSampleAttachmentKey_EarlierDisplayTimesAllowed: CFString](/documentation/coremedia/kcmsampleattachmentkey_earlierdisplaytimesallowed)
- [let kCMSampleAttachmentKey_HasRedundantCoding: CFString](/documentation/coremedia/kcmsampleattachmentkey_hasredundantcoding)
- [let kCMSampleAttachmentKey_PostDecodeProcessingMetadata: CFString](/documentation/coremedia/kcmsampleattachmentkey_postdecodeprocessingmetadata)

#### Sample Buffer Keys

- [let kCMSampleBufferAttachmentKey_DisplayEmptyMediaImmediately: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_displayemptymediaimmediately)
- [let kCMSampleBufferAttachmentKey_DrainAfterDecoding: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_drainafterdecoding)
- [let kCMSampleBufferAttachmentKey_DroppedFrameReason: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_droppedframereason)
- [let kCMSampleBufferDroppedFrameReason_FrameWasLate: CFString](/documentation/coremedia/kcmsamplebufferdroppedframereason_framewaslate)
- [let kCMSampleBufferDroppedFrameReason_OutOfBuffers: CFString](/documentation/coremedia/kcmsamplebufferdroppedframereason_outofbuffers)
- [let kCMSampleBufferDroppedFrameReason_Discontinuity: CFString](/documentation/coremedia/kcmsamplebufferdroppedframereason_discontinuity)
- [let kCMSampleBufferAttachmentKey_DroppedFrameReasonInfo: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_droppedframereasoninfo)
- [let kCMSampleBufferDroppedFrameReasonInfo_CameraModeSwitch: CFString](/documentation/coremedia/kcmsamplebufferdroppedframereasoninfo_cameramodeswitch)
- [let kCMSampleBufferAttachmentKey_EmptyMedia: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_emptymedia)
- [let kCMSampleBufferAttachmentKey_EndsPreviousSampleDuration: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_endsprevioussampleduration)
- [let kCMSampleBufferAttachmentKey_FillDiscontinuitiesWithSilence: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_filldiscontinuitieswithsilence)
- [let kCMSampleBufferAttachmentKey_ForceKeyFrame: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_forcekeyframe)
- [let kCMSampleBufferAttachmentKey_GradualDecoderRefresh: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_gradualdecoderrefresh)
- [let kCMSampleBufferAttachmentKey_PermanentEmptyMedia: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_permanentemptymedia)
- [let kCMSampleBufferAttachmentKey_PostNotificationWhenConsumed: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_postnotificationwhenconsumed)
- [let kCMSampleBufferAttachmentKey_ResetDecoderBeforeDecoding: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_resetdecoderbeforedecoding)
- [let kCMSampleBufferAttachmentKey_ResumeOutput: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_resumeoutput)
- [let kCMSampleBufferAttachmentKey_Reverse: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_reverse)
- [let kCMSampleBufferAttachmentKey_SampleReferenceByteOffset: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_samplereferencebyteoffset)
- [let kCMSampleBufferAttachmentKey_SampleReferenceURL: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_samplereferenceurl)
- [let kCMSampleBufferAttachmentKey_SpeedMultiplier: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_speedmultiplier)
- [let kCMSampleBufferAttachmentKey_StillImageLensStabilizationInfo: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_stillimagelensstabilizationinfo)
- [let kCMSampleBufferLensStabilizationInfo_Active: CFString](/documentation/coremedia/kcmsamplebufferlensstabilizationinfo_active)
- [let kCMSampleBufferLensStabilizationInfo_OutOfRange: CFString](/documentation/coremedia/kcmsamplebufferlensstabilizationinfo_outofrange)
- [let kCMSampleBufferLensStabilizationInfo_Unavailable: CFString](/documentation/coremedia/kcmsamplebufferlensstabilizationinfo_unavailable)
- [let kCMSampleBufferLensStabilizationInfo_Off: CFString](/documentation/coremedia/kcmsamplebufferlensstabilizationinfo_off)
- [let kCMSampleBufferAttachmentKey_TransitionID: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_transitionid)
- [let kCMSampleBufferAttachmentKey_TrimDurationAtEnd: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_trimdurationatend)
- [let kCMSampleBufferAttachmentKey_TrimDurationAtStart: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_trimdurationatstart)

### Processing Samples

- [func CMSampleBufferCallBlockForEachSample(CMSampleBuffer, (CMSampleBuffer, CMItemCount) -> OSStatus) -> OSStatus](/documentation/coremedia/cmsamplebuffercallblockforeachsample(_:_:))
- [func CMSampleBufferCallForEachSample(CMSampleBuffer, callback: (CMSampleBuffer, CMItemCount, UnsafeMutableRawPointer?) -> OSStatus, refcon: UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremedia/cmsamplebuffercallforeachsample(_:callback:refcon:))

### Accessing the Type Identifier

- [func CMSampleBufferGetTypeID() -> CFTypeID](/documentation/coremedia/cmsamplebuffergettypeid())

### Data Types

- [CMSampleBuffer](/documentation/coremedia/cmsamplebuffer)

#### Determining Readiness

- [var dataReadiness: CMSampleBuffer.DataReadiness](/documentation/coremedia/cmsamplebuffer/datareadiness-swift.property)
- [func setDataReadiness(CMSampleBuffer.DataReadiness) throws](/documentation/coremedia/cmsamplebuffer/setdatareadiness(_:))
- [CMSampleBuffer.DataReadiness](/documentation/coremedia/cmsamplebuffer/datareadiness-swift.enum)

##### States

- [case notReady](/documentation/coremedia/cmsamplebuffer/datareadiness-swift.enum/notready)
- [case ready](/documentation/coremedia/cmsamplebuffer/datareadiness-swift.enum/ready)
- [case failed(OSStatus)](/documentation/coremedia/cmsamplebuffer/datareadiness-swift.enum/failed(_:))
- [func makeDataReady() throws](/documentation/coremedia/cmsamplebuffer/makedataready())
- [func trackDataReadiness(CMSampleBuffer) throws](/documentation/coremedia/cmsamplebuffer/trackdatareadiness(_:))

#### Invalidating Sample Buffers

- [var isValid: Bool](/documentation/coremedia/cmsamplebuffer/isvalid)
- [func setInvalidateHandler((CMSampleBuffer) throws -> Void) throws](/documentation/coremedia/cmsamplebuffer/setinvalidatehandler(_:))
- [func invalidate() throws](/documentation/coremedia/cmsamplebuffer/invalidate())

#### Inspecting Size Information

- [var numSamples: Int](/documentation/coremedia/cmsamplebuffer/numsamples)
- [func sampleSizes() throws -> [Int]](/documentation/coremedia/cmsamplebuffer/samplesizes())
- [func sampleSize(at: Int) -> Int](/documentation/coremedia/cmsamplebuffer/samplesize(at:))
- [var totalSampleSize: Int](/documentation/coremedia/cmsamplebuffer/totalsamplesize)

#### Inspecting Duration and Timing

- [var duration: CMTime](/documentation/coremedia/cmsamplebuffer/duration)
- [var decodeTimeStamp: CMTime](/documentation/coremedia/cmsamplebuffer/decodetimestamp)
- [var presentationTimeStamp: CMTime](/documentation/coremedia/cmsamplebuffer/presentationtimestamp)
- [var outputDuration: CMTime](/documentation/coremedia/cmsamplebuffer/outputduration)
- [var outputDecodeTimeStamp: CMTime](/documentation/coremedia/cmsamplebuffer/outputdecodetimestamp)
- [var outputPresentationTimeStamp: CMTime](/documentation/coremedia/cmsamplebuffer/outputpresentationtimestamp)
- [func setOutputPresentationTimeStamp(CMTime) throws](/documentation/coremedia/cmsamplebuffer/setoutputpresentationtimestamp(_:))
- [func sampleTimingInfos() throws -> [CMSampleTimingInfo]](/documentation/coremedia/cmsamplebuffer/sampletiminginfos())
- [func sampleTimingInfo(at: CMItemIndex) throws -> CMSampleTimingInfo](/documentation/coremedia/cmsamplebuffer/sampletiminginfo(at:))
- [func outputSampleTimingInfos() throws -> [CMSampleTimingInfo]](/documentation/coremedia/cmsamplebuffer/outputsampletiminginfos())

#### Accessing the Format Description

- [var formatDescription: CMFormatDescription?](/documentation/coremedia/cmsamplebuffer/formatdescription)

#### Modifying Sample Buffers

- [var dataBuffer: CMBlockBuffer?](/documentation/coremedia/cmsamplebuffer/databuffer)
- [func setDataBuffer(CMBlockBuffer) throws](/documentation/coremedia/cmsamplebuffer/setdatabuffer(_:))
- [var imageBuffer: CVImageBuffer?](/documentation/coremedia/cmsamplebuffer/imagebuffer)
- [func withAudioBufferList<R>(blockBufferMemoryAllocator: CFAllocator?, flags: CMSampleBuffer.Flags, body: (UnsafeMutableAudioBufferListPointer, CMBlockBuffer) throws -> R) throws -> R](/documentation/coremedia/cmsamplebuffer/withaudiobufferlist(blockbuffermemoryallocator:flags:body:))
- [func setDataBuffer(fromAudioBufferList: UnsafePointer<AudioBufferList>, blockBufferMemoryAllocator: CFAllocator?, flags: CMSampleBuffer.Flags) throws](/documentation/coremedia/cmsamplebuffer/setdatabuffer(fromaudiobufferlist:blockbuffermemoryallocator:flags:))
- [func copyPCMData(fromRange: Range<Int>, into: UnsafeMutablePointer<AudioBufferList>) throws](/documentation/coremedia/cmsamplebuffer/copypcmdata(fromrange:into:))
- [func audioStreamPacketDescriptions() throws -> [AudioStreamPacketDescription]](/documentation/coremedia/cmsamplebuffer/audiostreampacketdescriptions())
- [func withUnsafeAudioStreamPacketDescriptions<R>((UnsafeBufferPointer<AudioStreamPacketDescription>) throws -> R) throws -> R](/documentation/coremedia/cmsamplebuffer/withunsafeaudiostreampacketdescriptions(_:))
- [func singleSampleBuffers() throws -> CMSampleBuffer.SingleSampleBuffers](/documentation/coremedia/cmsamplebuffer/singlesamplebuffers())
- [CMSampleBuffer.SingleSampleBuffers](/documentation/coremedia/cmsamplebuffer/singlesamplebuffers)

#### Managing Attachments

- [CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey)

##### Attachment Keys

- [static let cameraIntrinsicMatrix: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/cameraintrinsicmatrix)
- [static let displayEmptyMediaImmediately: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/displayemptymediaimmediately)
- [static let drainAfterDecoding: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/drainafterdecoding)
- [static let droppedFrameReason: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/droppedframereason)
- [static let droppedFrameReasonInfo: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/droppedframereasoninfo)
- [static let emptyMedia: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/emptymedia)
- [static let endsPreviousSampleDuration: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/endsprevioussampleduration)
- [static let fillDiscontinuitiesWithSilence: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/filldiscontinuitieswithsilence)
- [static let forceKeyFrame: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/forcekeyframe)
- [static let gradualDecoderRefresh: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/gradualdecoderrefresh)
- [static let permanentEmptyMedia: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/permanentemptymedia)
- [static let postNotificationWhenConsumed: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/postnotificationwhenconsumed)
- [static let resetDecoderBeforeDecoding: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/resetdecoderbeforedecoding)
- [static let resumeOutput: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/resumeoutput)
- [static let reverse: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/reverse)
- [static let sampleReferenceByteOffset: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/samplereferencebyteoffset)
- [static let sampleReferenceURL: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/samplereferenceurl)
- [static let speedMultiplier: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/speedmultiplier)
- [static let stillImageLensStabilizationInfo: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/stillimagelensstabilizationinfo)
- [static let transitionID: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/transitionid)
- [static let trimDurationAtEnd: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/trimdurationatend)
- [static let trimDurationAtStart: CMSampleBuffer.AttachmentKey](/documentation/coremedia/cmsamplebuffer/attachmentkey/trimdurationatstart)
- [var sampleAttachments: CMSampleBuffer.SampleAttachmentsArray](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.property)
- [CMSampleBuffer.SampleAttachmentsArray](/documentation/coremedia/cmsamplebuffer/sampleattachmentsarray)
- [CMSampleBuffer.PerSampleAttachmentsDictionary](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary)

##### Specifying Keys

- [CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key)

###### Keys

- [static let audioIndependentSampleDecoderRefreshCount: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/audioindependentsampledecoderrefreshcount)
- [static let dependsOnOthers: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/dependsonothers)
- [static let displayImmediately: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/displayimmediately)
- [static let doNotDisplay: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/donotdisplay)
- [static let earlierDisplayTimesAllowed: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/earlierdisplaytimesallowed)
- [static let hasRedundantCoding: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/hasredundantcoding)
- [static let hevcStepwiseTemporalSubLayerAccess: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/hevcstepwisetemporalsublayeraccess)
- [static let hevcSyncSampleNALUnitType: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/hevcsyncsamplenalunittype)
- [static let hevcTemporalLevelInfo: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/hevctemporallevelinfo)
- [static let hevcTemporalSubLayerAccess: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/hevctemporalsublayeraccess)
- [static let isDependedOnByOthers: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/isdependedonbyothers)
- [static let notSync: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/notsync)
- [static let partialSync: CMSampleBuffer.PerSampleAttachmentsDictionary.Key](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/key/partialsync)

##### Accessing Elements

- [subscript(CMSampleBuffer.PerSampleAttachmentsDictionary.Key) -> Any?](/documentation/coremedia/cmsamplebuffer/persampleattachmentsdictionary/subscript(_:))

#### Accessing the Type Identifier

- [static var typeID: CFTypeID](/documentation/coremedia/cmsamplebuffer/typeid)

#### Accessing Tagged Buffers

- [var taggedBuffers: [CMTaggedBuffer]?](/documentation/coremedia/cmsamplebuffer/taggedbuffers)

#### Constants

- [CMSampleBuffer.Error](/documentation/coremedia/cmsamplebuffer/error)

##### Errors

- [static let allocationFailed: NSError](/documentation/coremedia/cmsamplebuffer/error/allocationfailed)
- [static let alreadyHasDataBuffer: NSError](/documentation/coremedia/cmsamplebuffer/error/alreadyhasdatabuffer)
- [static let arrayTooSmall: NSError](/documentation/coremedia/cmsamplebuffer/error/arraytoosmall)
- [static let bufferHasNoSampleSizes: NSError](/documentation/coremedia/cmsamplebuffer/error/bufferhasnosamplesizes)
- [static let bufferHasNoSampleTimingInfo: NSError](/documentation/coremedia/cmsamplebuffer/error/bufferhasnosampletiminginfo)
- [static let bufferNotReady: NSError](/documentation/coremedia/cmsamplebuffer/error/buffernotready)
- [static let cannotSubdivide: NSError](/documentation/coremedia/cmsamplebuffer/error/cannotsubdivide)
- [static let dataCanceled: NSError](/documentation/coremedia/cmsamplebuffer/error/datacanceled)
- [static let dataFailed: NSError](/documentation/coremedia/cmsamplebuffer/error/datafailed)
- [static let invalidEntryCount: NSError](/documentation/coremedia/cmsamplebuffer/error/invalidentrycount)
- [static let invalidMediaFormat: NSError](/documentation/coremedia/cmsamplebuffer/error/invalidmediaformat)
- [static let invalidMediaTypeForOperation: NSError](/documentation/coremedia/cmsamplebuffer/error/invalidmediatypeforoperation)
- [static let invalidSampleData: NSError](/documentation/coremedia/cmsamplebuffer/error/invalidsampledata)
- [static let invalidated: NSError](/documentation/coremedia/cmsamplebuffer/error/invalidated)
- [static let requiredParameterMissing: NSError](/documentation/coremedia/cmsamplebuffer/error/requiredparametermissing)
- [static let sampleIndexOutOfRange: NSError](/documentation/coremedia/cmsamplebuffer/error/sampleindexoutofrange)
- [static let sampleTimingInfoInvalid: NSError](/documentation/coremedia/cmsamplebuffer/error/sampletiminginfoinvalid)
- [CMSampleBuffer.Flags](/documentation/coremedia/cmsamplebuffer/flags)

##### Flags

- [static let audioBufferListAssure16ByteAlignment: CMSampleBuffer.Flags](/documentation/coremedia/cmsamplebuffer/flags/audiobufferlistassure16bytealignment)
- [CMSampleBuffer.NotificationKey](/documentation/coremedia/cmsamplebuffer/notificationkey)

##### Keys

- [static let status: CMSampleBuffer.NotificationKey](/documentation/coremedia/cmsamplebuffer/notificationkey/status)

#### Notifications

- [static let dataBecameReady: NSNotification.Name](/documentation/coremedia/cmsamplebuffer/databecameready)
- [static let dataFailed: NSNotification.Name](/documentation/coremedia/cmsamplebuffer/datafailed)

#### Protocols

- [CMSampleBuffer.Content](/documentation/coremedia/cmsamplebuffer/content)
- [CMSampleBuffer.ContentWithFormatDescription](/documentation/coremedia/cmsamplebuffer/contentwithformatdescription)
- [CMSampleBuffer.MultiSampleContent](/documentation/coremedia/cmsamplebuffer/multisamplecontent)

#### Structures

- [CMSampleBuffer.HEVCTemporalInfo](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo)

##### Initializers

- [init(temporalLayerID: Int, profileSpace: Int, tierFlag: Int, profileIndex: Int, profileCompatibilityFlags: Data?, constraintIndicatorFlags: Data?, levelIndex: Int)](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/init(temporallayerid:profilespace:tierflag:profileindex:profilecompatibilityflags:constraintindicatorflags:levelindex:))

##### Instance Properties

- [var constraintIndicatorFlags: Data?](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/constraintindicatorflags)
- [var levelIndex: Int](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/levelindex)
- [var profileCompatibilityFlags: Data?](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/profilecompatibilityflags)
- [var profileIndex: Int](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/profileindex)
- [var profileSpace: Int](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/profilespace)
- [var temporalLayerID: Int](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/temporallayerid)
- [var tierFlag: Int](/documentation/coremedia/cmsamplebuffer/hevctemporalinfo/tierflag)
- [CMSampleBuffer.SampleAttachments](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct)

##### Initializers

- [init([String : any Sendable])](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/init(_:))

##### Instance Properties

- [var audioIndependentSampleDecoderRefreshCount: Int?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/audioindependentsampledecoderrefreshcount)
- [var cryptorSubsampleAuxiliaryData: Data?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/cryptorsubsampleauxiliarydata)
- [var dependsOnOthers: Bool?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/dependsonothers)
- [var dictionaryRepresentation: [String : any Sendable]](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/dictionaryrepresentation)
- [var displayImmediately: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/displayimmediately)
- [var doNotDisplay: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/donotdisplay)
- [var earlierDisplayTimesAllowed: Bool?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/earlierdisplaytimesallowed)
- [var hasRedundantCoding: Bool?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hasredundantcoding)
- [var hdr10PlusPerFrameData: Data?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hdr10plusperframedata)
- [var hevcStepwiseTemporalSubLayerAccess: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hevcstepwisetemporalsublayeraccess)
- [var hevcSyncSampleNALUnitType: Int?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hevcsyncsamplenalunittype)
- [var hevcTemporalInfo: CMSampleBuffer.HEVCTemporalInfo?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hevctemporalinfo)
- [var hevcTemporalSubLayerAccess: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/hevctemporalsublayeraccess)
- [var isDependedOnByOthers: Bool?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/isdependedonbyothers)
- [var isNotSync: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/isnotsync)
- [var isPartialSync: Bool](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/ispartialsync)
- [var postDecodeProcessingMetadata: [String : any Sendable]?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/postdecodeprocessingmetadata)

##### Subscripts

- [subscript(rawAttachment _: String) -> (any Sendable)?](/documentation/coremedia/cmsamplebuffer/sampleattachments-swift.struct/subscript(rawattachment:))
- [CMSampleBuffer.SampleProperties](/documentation/coremedia/cmsamplebuffer/sampleproperties)

##### Initializers

- [init(size: Int?, timing: CMSampleTimingInfo, attachments: CMSampleBuffer.SampleAttachments)](/documentation/coremedia/cmsamplebuffer/sampleproperties/init(size:timing:attachments:))

##### Instance Properties

- [var attachments: CMSampleBuffer.SampleAttachments](/documentation/coremedia/cmsamplebuffer/sampleproperties/attachments)
- [var size: Int?](/documentation/coremedia/cmsamplebuffer/sampleproperties/size)
- [var timing: CMSampleTimingInfo](/documentation/coremedia/cmsamplebuffer/sampleproperties/timing)
- [CMSampleBuffer.SamplePropertiesCollection](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection)

##### Initializers

- [init()](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/init())
- [init(some Collection<CMSampleBuffer.SampleProperties>)](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/init(_:))
- [init(sampleCount: Int, sizes: CMSampleBuffer.SizePerSample?, timings: CMSampleBuffer.TimingPerSample?, attachments: [CMSampleBuffer.SampleAttachments]?)](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/init(samplecount:sizes:timings:attachments:))

##### Instance Properties

- [var attachments: [CMSampleBuffer.SampleAttachments]?](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/attachments)
- [var count: Int](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/count)
- [var endIndex: Int](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/endindex)
- [var sizes: CMSampleBuffer.SizePerSample?](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/sizes)
- [var startIndex: Int](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/startindex)
- [var timings: CMSampleBuffer.TimingPerSample?](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/timings)

##### Subscripts

- [subscript(Int) -> CMSampleBuffer.SampleProperties](/documentation/coremedia/cmsamplebuffer/samplepropertiescollection/subscript(_:))

#### Initializers

- [init(referencing: CMSampleBuffer)](/documentation/coremedia/cmsamplebuffer/init(referencing:))

#### Instance Properties

- [var contentType: CMSampleBuffer.ContentType](/documentation/coremedia/cmsamplebuffer/contenttype-swift.property)

#### Type Aliases

- [CMSampleBuffer.T](/documentation/coremedia/cmsamplebuffer/t)

#### Enumerations

- [CMSampleBuffer.ContentType](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum)

##### Enumeration Cases

- [case dataBuffer](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum/databuffer)
- [case markerOnly](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum/markeronly)
- [case pixelBuffer](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum/pixelbuffer)
- [case sampleReference](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum/samplereference)
- [case taggedBuffers](/documentation/coremedia/cmsamplebuffer/contenttype-swift.enum/taggedbuffers)
- [CMSampleBuffer.DynamicContent](/documentation/coremedia/cmsamplebuffer/dynamiccontent)

##### Enumeration Cases

- [case dataBuffer(CMReadOnlyDataBlockBuffer)](/documentation/coremedia/cmsamplebuffer/dynamiccontent/databuffer(_:))
- [case markerOnly](/documentation/coremedia/cmsamplebuffer/dynamiccontent/markeronly)
- [case pixelBuffer(CVReadOnlyPixelBuffer)](/documentation/coremedia/cmsamplebuffer/dynamiccontent/pixelbuffer(_:))
- [case sampleReference(CMSampleDataReference)](/documentation/coremedia/cmsamplebuffer/dynamiccontent/samplereference(_:))
- [case taggedBuffers([CMTaggedDynamicBuffer])](/documentation/coremedia/cmsamplebuffer/dynamiccontent/taggedbuffers(_:))
- [CMSampleBuffer.SizePerSample](/documentation/coremedia/cmsamplebuffer/sizepersample)

##### Enumeration Cases

- [case distinct([Int])](/documentation/coremedia/cmsamplebuffer/sizepersample/distinct(_:))
- [case uniform(Int)](/documentation/coremedia/cmsamplebuffer/sizepersample/uniform(_:))
- [CMSampleBuffer.TimingPerSample](/documentation/coremedia/cmsamplebuffer/timingpersample)

##### Enumeration Cases

- [case distinct([CMSampleTimingInfo])](/documentation/coremedia/cmsamplebuffer/timingpersample/distinct(_:))
- [case sequential(startingAt: CMSampleTimingInfo)](/documentation/coremedia/cmsamplebuffer/timingpersample/sequential(startingat:))

##### Type Methods

- [static func sequential(presentationTimeOfFirstSample: CMTime, uniformDuration: CMTime, decodeTimeOfFirstSample: CMTime) -> CMSampleBuffer.TimingPerSample](/documentation/coremedia/cmsamplebuffer/timingpersample/sequential(presentationtimeoffirstsample:uniformduration:decodetimeoffirstsample:))
- [Sample Buffer Flags](/documentation/coremedia/sample-buffer-flags)

#### Constants

- [var kCMSampleBufferFlag_AudioBufferList_Assure16ByteAlignment: UInt32](/documentation/coremedia/kcmsamplebufferflag_audiobufferlist_assure16bytealignment)
- [CMSampleTimingInfo](/documentation/coremedia/cmsampletiminginfo)

#### Constants

- [static let invalid: CMSampleTimingInfo](/documentation/coremedia/cmsampletiminginfo/invalid)

#### Initializers

- [init()](/documentation/coremedia/cmsampletiminginfo/init())
- [init(duration: CMTime, presentationTimeStamp: CMTime, decodeTimeStamp: CMTime)](/documentation/coremedia/cmsampletiminginfo/init(duration:presentationtimestamp:decodetimestamp:))

#### Properties

- [var decodeTimeStamp: CMTime](/documentation/coremedia/cmsampletiminginfo/decodetimestamp)
- [var duration: CMTime](/documentation/coremedia/cmsampletiminginfo/duration)
- [var presentationTimeStamp: CMTime](/documentation/coremedia/cmsampletiminginfo/presentationtimestamp)
- [CMBuffer](/documentation/coremedia/cmbuffer)
- [CMBufferGetSizeCallback](/documentation/coremedia/cmbuffergetsizecallback)
- [CMItemIndex](/documentation/coremedia/cmitemindex)
- [CMItemCount](/documentation/coremedia/cmitemcount)
- [CMPersistentTrackID](/documentation/coremedia/cmpersistenttrackid)
- [CMMuxedStreamType](/documentation/coremedia/cmmuxedstreamtype)

#### Constants

- [var kCMMuxedStreamType_MPEG1System: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg1system)
- [var kCMMuxedStreamType_MPEG2Transport: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg2transport)
- [var kCMMuxedStreamType_MPEG2Program: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg2program)
- [var kCMMuxedStreamType_DV: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_dv)

### Notifications

- [Sample Buffer Notifications](/documentation/coremedia/sample-buffer-notifications)

#### Sample Buffer Notifications

- [let kCMSampleBufferNotification_DataBecameReady: CFString](/documentation/coremedia/kcmsamplebuffernotification_databecameready)
- [let kCMSampleBufferNotification_DataFailed: CFString](/documentation/coremedia/kcmsamplebuffernotification_datafailed)
- [let kCMSampleBufferNotificationParameter_OSStatus: CFString](/documentation/coremedia/kcmsamplebuffernotificationparameter_osstatus)
- [let kCMSampleBufferConsumerNotification_BufferConsumed: CFString](/documentation/coremedia/kcmsamplebufferconsumernotification_bufferconsumed)

#### Sample Buffer Conduit Notifications

- [let kCMSampleBufferConduitNotification_ResetOutput: CFString](/documentation/coremedia/kcmsamplebufferconduitnotification_resetoutput)
- [let kCMSampleBufferConduitNotification_InhibitOutputUntil: CFString](/documentation/coremedia/kcmsamplebufferconduitnotification_inhibitoutputuntil)
- [let kCMSampleBufferConduitNotification_UpcomingOutputPTSRangeChanged: CFString](/documentation/coremedia/kcmsamplebufferconduitnotification_upcomingoutputptsrangechanged)
- [let kCMSampleBufferConduitNotificationParameter_UpcomingOutputPTSRangeMayOverlapQueuedOutputPTSRange: CFString](/documentation/coremedia/kcmsamplebufferconduitnotificationparameter_upcomingoutputptsrangemayoverlapqueuedoutputptsrange)
- [let kCMSampleBufferConduitNotificationParameter_MinUpcomingOutputPTS: CFString](/documentation/coremedia/kcmsamplebufferconduitnotificationparameter_minupcomingoutputpts)
- [let kCMSampleBufferConduitNotificationParameter_MaxUpcomingOutputPTS: CFString](/documentation/coremedia/kcmsamplebufferconduitnotificationparameter_maxupcomingoutputpts)
- [let kCMSampleBufferConduitNotificationParameter_ResumeTag: CFString](/documentation/coremedia/kcmsamplebufferconduitnotificationparameter_resumetag)

### Errors

- [Sample Buffer Error Codes](/documentation/coremedia/sample-buffer-errors)

#### Error Codes

- [var kCMSampleBufferError_AllocationFailed: OSStatus](/documentation/coremedia/kcmsamplebuffererror_allocationfailed)
- [var kCMSampleBufferError_AlreadyHasDataBuffer: OSStatus](/documentation/coremedia/kcmsamplebuffererror_alreadyhasdatabuffer)
- [var kCMSampleBufferError_ArrayTooSmall: OSStatus](/documentation/coremedia/kcmsamplebuffererror_arraytoosmall)
- [var kCMSampleBufferError_BufferHasNoSampleSizes: OSStatus](/documentation/coremedia/kcmsamplebuffererror_bufferhasnosamplesizes)
- [var kCMSampleBufferError_BufferHasNoSampleTimingInfo: OSStatus](/documentation/coremedia/kcmsamplebuffererror_bufferhasnosampletiminginfo)
- [var kCMSampleBufferError_BufferNotReady: OSStatus](/documentation/coremedia/kcmsamplebuffererror_buffernotready)
- [var kCMSampleBufferError_CannotSubdivide: OSStatus](/documentation/coremedia/kcmsamplebuffererror_cannotsubdivide)
- [var kCMSampleBufferError_DataCanceled: OSStatus](/documentation/coremedia/kcmsamplebuffererror_datacanceled)
- [var kCMSampleBufferError_DataFailed: OSStatus](/documentation/coremedia/kcmsamplebuffererror_datafailed)
- [var kCMSampleBufferError_InvalidEntryCount: OSStatus](/documentation/coremedia/kcmsamplebuffererror_invalidentrycount)
- [var kCMSampleBufferError_InvalidMediaFormat: OSStatus](/documentation/coremedia/kcmsamplebuffererror_invalidmediaformat)
- [var kCMSampleBufferError_InvalidMediaTypeForOperation: OSStatus](/documentation/coremedia/kcmsamplebuffererror_invalidmediatypeforoperation)
- [var kCMSampleBufferError_InvalidSampleData: OSStatus](/documentation/coremedia/kcmsamplebuffererror_invalidsampledata)
- [var kCMSampleBufferError_Invalidated: OSStatus](/documentation/coremedia/kcmsamplebuffererror_invalidated)
- [var kCMSampleBufferError_RequiredParameterMissing: OSStatus](/documentation/coremedia/kcmsamplebuffererror_requiredparametermissing)
- [var kCMSampleBufferError_SampleIndexOutOfRange: OSStatus](/documentation/coremedia/kcmsamplebuffererror_sampleindexoutofrange)
- [var kCMSampleBufferError_SampleTimingInfoInvalid: OSStatus](/documentation/coremedia/kcmsamplebuffererror_sampletiminginfoinvalid)
- [var kCMPersistentTrackID_Invalid: CMPersistentTrackID](/documentation/coremedia/kcmpersistenttrackid_invalid)

### Functions

- [func CMTimeFoldIntoRange(CMTime, foldRange: CMTimeRange) -> CMTime](/documentation/coremedia/cmtimefoldintorange(_:foldrange:))
- [func CMVideoFormatDescriptionGetHEVCParameterSetAtIndex(CMFormatDescription, parameterSetIndex: Int, parameterSetPointerOut: UnsafeMutablePointer<UnsafePointer<UInt8>?>?, parameterSetSizeOut: UnsafeMutablePointer<Int>?, parameterSetCountOut: UnsafeMutablePointer<Int>?, nalUnitHeaderLengthOut: UnsafeMutablePointer<Int32>?) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptiongethevcparametersetatindex(_:parametersetindex:parametersetpointerout:parametersetsizeout:parametersetcountout:nalunitheaderlengthout:))
- [CMBlockBuffer](/documentation/coremedia/cmblockbuffer-api)

### Creating a Block Buffer

- [func CMBlockBufferCreateEmpty(allocator: CFAllocator?, capacity: UInt32, flags: CMBlockBufferFlags, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmblockbuffercreateempty(allocator:capacity:flags:blockbufferout:))
- [func CMBlockBufferCreateWithMemoryBlock(allocator: CFAllocator?, memoryBlock: UnsafeMutableRawPointer?, blockLength: Int, blockAllocator: CFAllocator?, customBlockSource: UnsafePointer<CMBlockBufferCustomBlockSource>?, offsetToData: Int, dataLength: Int, flags: CMBlockBufferFlags, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmblockbuffercreatewithmemoryblock(allocator:memoryblock:blocklength:blockallocator:customblocksource:offsettodata:datalength:flags:blockbufferout:))
- [func CMBlockBufferCreateWithBufferReference(allocator: CFAllocator?, referenceBuffer: CMBlockBuffer, offsetToData: Int, dataLength: Int, flags: CMBlockBufferFlags, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmblockbuffercreatewithbufferreference(allocator:referencebuffer:offsettodata:datalength:flags:blockbufferout:))
- [func CMBlockBufferCreateContiguous(allocator: CFAllocator?, sourceBuffer: CMBlockBuffer, blockAllocator: CFAllocator?, customBlockSource: UnsafePointer<CMBlockBufferCustomBlockSource>?, offsetToData: Int, dataLength: Int, flags: CMBlockBufferFlags, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmblockbuffercreatecontiguous(allocator:sourcebuffer:blockallocator:customblocksource:offsettodata:datalength:flags:blockbufferout:))
- [CMBlockBufferFlags](/documentation/coremedia/cmblockbufferflags)

#### Constants

- [var kCMBlockBufferAssureMemoryNowFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferassurememorynowflag)
- [var kCMBlockBufferAlwaysCopyDataFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferalwayscopydataflag)
- [var kCMBlockBufferDontOptimizeDepthFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferdontoptimizedepthflag)
- [var kCMBlockBufferPermitEmptyReferenceFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferpermitemptyreferenceflag)
- [Block Buffer Flags](/documentation/coremedia/block-buffer-flags)

#### Constants

- [var kCMBlockBufferAssureMemoryNowFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferassurememorynowflag)
- [var kCMBlockBufferAlwaysCopyDataFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferalwayscopydataflag)
- [var kCMBlockBufferDontOptimizeDepthFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferdontoptimizedepthflag)
- [var kCMBlockBufferPermitEmptyReferenceFlag: CMBlockBufferFlags](/documentation/coremedia/kcmblockbufferpermitemptyreferenceflag)
- [CMBlockBufferCustomBlockSource](/documentation/coremedia/cmblockbuffercustomblocksource)

#### Initializers

- [init()](/documentation/coremedia/cmblockbuffercustomblocksource/init())
- [init(version: UInt32, AllocateBlock: ((UnsafeMutableRawPointer?, Int) -> UnsafeMutableRawPointer?)?, FreeBlock: ((UnsafeMutableRawPointer?, UnsafeMutableRawPointer, Int) -> Void)?, refCon: UnsafeMutableRawPointer?)](/documentation/coremedia/cmblockbuffercustomblocksource/init(version:allocateblock:freeblock:refcon:))

#### Properties

- [var AllocateBlock: ((UnsafeMutableRawPointer?, Int) -> UnsafeMutableRawPointer?)?](/documentation/coremedia/cmblockbuffercustomblocksource/allocateblock)
- [var FreeBlock: ((UnsafeMutableRawPointer?, UnsafeMutableRawPointer, Int) -> Void)?](/documentation/coremedia/cmblockbuffercustomblocksource/freeblock)
- [var refCon: UnsafeMutableRawPointer?](/documentation/coremedia/cmblockbuffercustomblocksource/refcon)
- [var version: UInt32](/documentation/coremedia/cmblockbuffercustomblocksource/version)
- [Custom Block Source Version](/documentation/coremedia/custom-block-source-version)

#### Constants

- [var kCMBlockBufferCustomBlockSourceVersion: UInt32](/documentation/coremedia/kcmblockbuffercustomblocksourceversion)

### Modifying a Block Buffer

- [func CMBlockBufferAppendMemoryBlock(CMBlockBuffer, memoryBlock: UnsafeMutableRawPointer?, length: Int, blockAllocator: CFAllocator?, customBlockSource: UnsafePointer<CMBlockBufferCustomBlockSource>?, offsetToData: Int, dataLength: Int, flags: CMBlockBufferFlags) -> OSStatus](/documentation/coremedia/cmblockbufferappendmemoryblock(_:memoryblock:length:blockallocator:customblocksource:offsettodata:datalength:flags:))
- [func CMBlockBufferAppendBufferReference(CMBlockBuffer, targetBBuf: CMBlockBuffer, offsetToData: Int, dataLength: Int, flags: CMBlockBufferFlags) -> OSStatus](/documentation/coremedia/cmblockbufferappendbufferreference(_:targetbbuf:offsettodata:datalength:flags:))
- [func CMBlockBufferAssureBlockMemory(CMBlockBuffer) -> OSStatus](/documentation/coremedia/cmblockbufferassureblockmemory(_:))
- [func CMBlockBufferAccessDataBytes(CMBlockBuffer, atOffset: Int, length: Int, temporaryBlock: UnsafeMutableRawPointer, returnedPointerOut: UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>) -> OSStatus](/documentation/coremedia/cmblockbufferaccessdatabytes(_:atoffset:length:temporaryblock:returnedpointerout:))
- [func CMBlockBufferCopyDataBytes(CMBlockBuffer, atOffset: Int, dataLength: Int, destination: UnsafeMutableRawPointer) -> OSStatus](/documentation/coremedia/cmblockbuffercopydatabytes(_:atoffset:datalength:destination:))
- [func CMBlockBufferReplaceDataBytes(with: UnsafeRawPointer, blockBuffer: CMBlockBuffer, offsetIntoDestination: Int, dataLength: Int) -> OSStatus](/documentation/coremedia/cmblockbufferreplacedatabytes(with:blockbuffer:offsetintodestination:datalength:))
- [func CMBlockBufferFillDataBytes(with: CChar, blockBuffer: CMBlockBuffer, offsetIntoDestination: Int, dataLength: Int) -> OSStatus](/documentation/coremedia/cmblockbufferfilldatabytes(with:blockbuffer:offsetintodestination:datalength:))

### Inspecting a Block Buffer

- [func CMBlockBufferGetDataPointer(CMBlockBuffer, atOffset: Int, lengthAtOffsetOut: UnsafeMutablePointer<Int>?, totalLengthOut: UnsafeMutablePointer<Int>?, dataPointerOut: UnsafeMutablePointer<UnsafeMutablePointer<CChar>?>?) -> OSStatus](/documentation/coremedia/cmblockbuffergetdatapointer(_:atoffset:lengthatoffsetout:totallengthout:datapointerout:))
- [func CMBlockBufferGetDataLength(CMBlockBuffer) -> Int](/documentation/coremedia/cmblockbuffergetdatalength(_:))
- [func CMBlockBufferIsRangeContiguous(CMBlockBuffer, atOffset: Int, length: Int) -> Bool](/documentation/coremedia/cmblockbufferisrangecontiguous(_:atoffset:length:))
- [func CMBlockBufferIsEmpty(CMBlockBuffer) -> Bool](/documentation/coremedia/cmblockbufferisempty(_:))

### Accessing the Type Identifier

- [func CMBlockBufferGetTypeID() -> CFTypeID](/documentation/coremedia/cmblockbuffergettypeid())

### Data Types

- [CMBlockBuffer](/documentation/coremedia/cmblockbuffer)

#### Modifying a Block Buffer

- [func append(length: Int, allocator: CFAllocator?, range: Range<Int>?, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(length:allocator:range:flags:))
- [func append(buffer: UnsafeMutableRawBufferPointer, allocator: CFAllocator?, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(buffer:allocator:flags:)-28keu)
- [func append(buffer: Slice<UnsafeMutableRawBufferPointer>, allocator: CFAllocator?, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(buffer:allocator:flags:)-8fws8)
- [func append(length: Int, allocator: CMBlockBuffer.CustomBlockAllocator, deallocator: CMBlockBuffer.CustomBlockDeallocator, range: Range<Int>?, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(length:allocator:deallocator:range:flags:))
- [func append(buffer: UnsafeMutableRawBufferPointer, deallocator: CMBlockBuffer.CustomBlockDeallocator, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(buffer:deallocator:flags:)-3bfef)
- [func append(buffer: Slice<UnsafeMutableRawBufferPointer>, deallocator: CMBlockBuffer.CustomBlockDeallocator, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(buffer:deallocator:flags:)-1ibzz)
- [CMBlockBuffer.CustomBlockAllocator](/documentation/coremedia/cmblockbuffer/customblockallocator)
- [CMBlockBuffer.CustomBlockDeallocator](/documentation/coremedia/cmblockbuffer/customblockdeallocator)
- [func append<T>(bufferReference: T, flags: CMBlockBuffer.Flags) throws](/documentation/coremedia/cmblockbuffer/append(bufferreference:flags:))
- [func assureBlockMemory() throws](/documentation/coremedia/cmblockbuffer/assureblockmemory())
- [func withUnsafeMutableBytes<R>(atOffset: Int, (UnsafeMutableRawBufferPointer) throws -> R) throws -> R](/documentation/coremedia/cmblockbuffer/withunsafemutablebytes(atoffset:_:))

#### Inspecting a Block Buffer

- [var isEmpty: Bool](/documentation/coremedia/cmblockbuffer/isempty)

#### Accessing the Type Identifier

- [class var typeID: CFTypeID](/documentation/coremedia/cmblockbuffer/typeid)

#### Data Types

- [CMBlockBuffer.Error](/documentation/coremedia/cmblockbuffer/error)

##### Errors

- [static let badCustomBlockSource: NSError](/documentation/coremedia/cmblockbuffer/error/badcustomblocksource)
- [static let badLengthParameter: NSError](/documentation/coremedia/cmblockbuffer/error/badlengthparameter)
- [static let badOffsetParameter: NSError](/documentation/coremedia/cmblockbuffer/error/badoffsetparameter)
- [static let badPointerParameter: NSError](/documentation/coremedia/cmblockbuffer/error/badpointerparameter)
- [static let blockAllocationFailed: NSError](/documentation/coremedia/cmblockbuffer/error/blockallocationfailed)
- [static let emptyBlockBuffer: NSError](/documentation/coremedia/cmblockbuffer/error/emptyblockbuffer)
- [static let insufficientSpace: NSError](/documentation/coremedia/cmblockbuffer/error/insufficientspace)
- [static let structureAllocationFailed: NSError](/documentation/coremedia/cmblockbuffer/error/structureallocationfailed)
- [static let unallocatedBlock: NSError](/documentation/coremedia/cmblockbuffer/error/unallocatedblock)
- [CMBlockBuffer.Flags](/documentation/coremedia/cmblockbuffer/flags)

##### Type Properties

- [static let alwaysCopyData: CMBlockBuffer.Flags](/documentation/coremedia/cmblockbuffer/flags/alwayscopydata)
- [static let assureMemoryNow: CMBlockBuffer.Flags](/documentation/coremedia/cmblockbuffer/flags/assurememorynow)
- [static let dontOptimizeDepth: CMBlockBuffer.Flags](/documentation/coremedia/cmblockbuffer/flags/dontoptimizedepth)
- [static let permitEmptyReference: CMBlockBuffer.Flags](/documentation/coremedia/cmblockbuffer/flags/permitemptyreference)
- [CMBlockBuffer.Slice](/documentation/coremedia/cmblockbuffer/slice)

#### Initializers

- [init(referencing: CMBlockBuffer)](/documentation/coremedia/cmblockbuffer/init(referencing:))

#### Type Aliases

- [CMBlockBuffer.T](/documentation/coremedia/cmblockbuffer/t)
- [CMBlockBufferProtocol](/documentation/coremedia/cmblockbufferprotocol)

#### Modifying a Block Buffer

- [func copyDataBytes(to: UnsafeMutableRawBufferPointer) throws](/documentation/coremedia/cmblockbufferprotocol/copydatabytes(to:))
- [func dataBytes() throws -> Data](/documentation/coremedia/cmblockbufferprotocol/databytes())
- [func fillDataBytes(with: UInt8) throws](/documentation/coremedia/cmblockbufferprotocol/filldatabytes(with:))
- [func replaceDataBytes(with: UnsafeRawBufferPointer) throws](/documentation/coremedia/cmblockbufferprotocol/replacedatabytes(with:))
- [var isContiguous: Bool](/documentation/coremedia/cmblockbufferprotocol/iscontiguous)
- [func makeContiguous(allocator: CMBlockBuffer.CustomBlockAllocator, deallocator: CMBlockBuffer.CustomBlockDeallocator, flags: CMBlockBuffer.Flags) throws -> CMBlockBuffer](/documentation/coremedia/cmblockbufferprotocol/makecontiguous(allocator:deallocator:flags:))
- [func makeContiguous(allocator: CFAllocator?, flags: CMBlockBuffer.Flags) throws -> CMBlockBuffer](/documentation/coremedia/cmblockbufferprotocol/makecontiguous(allocator:flags:))
- [func withContiguousStorage<R>((UnsafeRawBufferPointer) throws -> R) throws -> R](/documentation/coremedia/cmblockbufferprotocol/withcontiguousstorage(_:))

#### Inspecting a Block Buffer

- [var dataLength: Int](/documentation/coremedia/cmblockbufferprotocol/datalength)
- [var startIndex: Int](/documentation/coremedia/cmblockbufferprotocol/startindex)
- [var endIndex: Int](/documentation/coremedia/cmblockbufferprotocol/endindex)
- [var owner: CMBlockBuffer](/documentation/coremedia/cmblockbufferprotocol/owner)

#### Subscripts

- [subscript(ClosedRange<Int>) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-7a30d)
- [subscript(Range<Int>) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-1go3)
- [subscript(PartialRangeFrom<Int>) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-9ntfs)
- [subscript(PartialRangeUpTo<Int>) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-6ghj4)
- [subscript(PartialRangeThrough<Int>) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-532k5)
- [subscript((UnboundedRange_) -> ()) -> CMBlockBuffer.Slice](/documentation/coremedia/cmblockbufferprotocol/subscript(_:)-8jilq)

### Errors

- [Block Buffer Error Codes](/documentation/coremedia/block-buffer-error-codes)

#### Errors

- [var kCMBlockBufferBadCustomBlockSourceErr: OSStatus](/documentation/coremedia/kcmblockbufferbadcustomblocksourceerr)
- [var kCMBlockBufferBadLengthParameterErr: OSStatus](/documentation/coremedia/kcmblockbufferbadlengthparametererr)
- [var kCMBlockBufferBadOffsetParameterErr: OSStatus](/documentation/coremedia/kcmblockbufferbadoffsetparametererr)
- [var kCMBlockBufferBadPointerParameterErr: OSStatus](/documentation/coremedia/kcmblockbufferbadpointerparametererr)
- [var kCMBlockBufferBlockAllocationFailedErr: OSStatus](/documentation/coremedia/kcmblockbufferblockallocationfailederr)
- [var kCMBlockBufferEmptyBBufErr: OSStatus](/documentation/coremedia/kcmblockbufferemptybbuferr)
- [var kCMBlockBufferInsufficientSpaceErr: OSStatus](/documentation/coremedia/kcmblockbufferinsufficientspaceerr)
- [var kCMBlockBufferStructureAllocationFailedErr: OSStatus](/documentation/coremedia/kcmblockbufferstructureallocationfailederr)
- [var kCMBlockBufferUnallocatedBlockErr: OSStatus](/documentation/coremedia/kcmblockbufferunallocatedblockerr)
- [var kCMBlockBufferNoErr: OSStatus](/documentation/coremedia/kcmblockbuffernoerr)
- [CMTaggedBufferGroup](/documentation/coremedia/cmtaggedbuffergroup)

### Types

- [CMTaggedBufferGroupFormatDescription](/documentation/coremedia/cmtaggedbuffergroupformatdescription)
- [CMTaggedBufferGroupFormatType](/documentation/coremedia/cmtaggedbuffergroupformattype)
- [CMFormatDescription](/documentation/coremedia/cmformatdescription-api)

### Creating Format Descriptions

- [func CMFormatDescriptionCreate(allocator: CFAllocator?, mediaType: CMMediaType, mediaSubType: FourCharCode, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMFormatDescription?>) -> OSStatus](/documentation/coremedia/cmformatdescriptioncreate(allocator:mediatype:mediasubtype:extensions:formatdescriptionout:))

### Comparing Format Descriptions

- [func CMFormatDescriptionEqual(CMFormatDescription?, otherFormatDescription: CMFormatDescription?) -> Bool](/documentation/coremedia/cmformatdescriptionequal(_:otherformatdescription:))
- [func CMFormatDescriptionEqualIgnoringExtensionKeys(CMFormatDescription?, otherFormatDescription: CMFormatDescription?, extensionKeysToIgnore: CFTypeRef?, sampleDescriptionExtensionAtomKeysToIgnore: CFTypeRef?) -> Bool](/documentation/coremedia/cmformatdescriptionequalignoringextensionkeys(_:otherformatdescription:extensionkeystoignore:sampledescriptionextensionatomkeystoignore:))

### Inspecting Format Descriptions

- [func CMFormatDescriptionGetMediaType(CMFormatDescription) -> CMMediaType](/documentation/coremedia/cmformatdescriptiongetmediatype(_:))
- [func CMFormatDescriptionGetMediaSubType(CMFormatDescription) -> FourCharCode](/documentation/coremedia/cmformatdescriptiongetmediasubtype(_:))
- [func CMFormatDescriptionGetExtension(CMFormatDescription, extensionKey: CFString) -> CFPropertyList?](/documentation/coremedia/cmformatdescriptiongetextension(_:extensionkey:))
- [func CMFormatDescriptionGetExtensions(CMFormatDescription) -> CFDictionary?](/documentation/coremedia/cmformatdescriptiongetextensions(_:))
- [func CMFormatDescriptionGetTypeID() -> CFTypeID](/documentation/coremedia/cmformatdescriptiongettypeid())

### Working with Audio Descriptions

- [CMSoundDescriptionFlavor](/documentation/coremedia/cmsounddescriptionflavor)

#### Sound Description Flavors

- [static let isoFamily: CMSoundDescriptionFlavor](/documentation/coremedia/cmsounddescriptionflavor/isofamily)
- [static let mobile3GPFamily: CMSoundDescriptionFlavor](/documentation/coremedia/cmsounddescriptionflavor/mobile3gpfamily)
- [static let quickTimeMovie: CMSoundDescriptionFlavor](/documentation/coremedia/cmsounddescriptionflavor/quicktimemovie)
- [static let quickTimeMovieV2: CMSoundDescriptionFlavor](/documentation/coremedia/cmsounddescriptionflavor/quicktimemoviev2)

#### Creating Sound Description Flavors

- [init(CFString)](/documentation/coremedia/cmsounddescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmsounddescriptionflavor/init(rawvalue:))
- [func CMAudioFormatDescriptionCreateSummary(allocator: CFAllocator?, formatDescriptionArray: CFArray, flags: UInt32, formatDescriptionOut: UnsafeMutablePointer<CMAudioFormatDescription?>) -> OSStatus](/documentation/coremedia/cmaudioformatdescriptioncreatesummary(allocator:formatdescriptionarray:flags:formatdescriptionout:))
- [func CMAudioFormatDescriptionCreate(allocator: CFAllocator?, asbd: UnsafePointer<AudioStreamBasicDescription>, layoutSize: Int, layout: UnsafePointer<AudioChannelLayout>?, magicCookieSize: Int, magicCookie: UnsafeRawPointer?, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMAudioFormatDescription?>) -> OSStatus](/documentation/coremedia/cmaudioformatdescriptioncreate(allocator:asbd:layoutsize:layout:magiccookiesize:magiccookie:extensions:formatdescriptionout:))
- [func CMAudioFormatDescriptionEqual(CMAudioFormatDescription, otherFormatDescription: CMAudioFormatDescription, equalityMask: CMAudioFormatDescriptionMask, equalityMaskOut: UnsafeMutablePointer<CMAudioFormatDescriptionMask>?) -> Bool](/documentation/coremedia/cmaudioformatdescriptionequal(_:otherformatdescription:equalitymask:equalitymaskout:))
- [func CMAudioFormatDescriptionGetChannelLayout(CMAudioFormatDescription, sizeOut: UnsafeMutablePointer<Int>?) -> UnsafePointer<AudioChannelLayout>?](/documentation/coremedia/cmaudioformatdescriptiongetchannellayout(_:sizeout:))
- [func CMAudioFormatDescriptionGetFormatList(CMAudioFormatDescription, sizeOut: UnsafeMutablePointer<Int>?) -> UnsafePointer<AudioFormatListItem>?](/documentation/coremedia/cmaudioformatdescriptiongetformatlist(_:sizeout:))
- [func CMAudioFormatDescriptionGetMagicCookie(CMAudioFormatDescription, sizeOut: UnsafeMutablePointer<Int>?) -> UnsafeRawPointer?](/documentation/coremedia/cmaudioformatdescriptiongetmagiccookie(_:sizeout:))
- [func CMAudioFormatDescriptionGetMostCompatibleFormat(CMAudioFormatDescription) -> UnsafePointer<AudioFormatListItem>?](/documentation/coremedia/cmaudioformatdescriptiongetmostcompatibleformat(_:))
- [func CMAudioFormatDescriptionGetRichestDecodableFormat(CMAudioFormatDescription) -> UnsafePointer<AudioFormatListItem>?](/documentation/coremedia/cmaudioformatdescriptiongetrichestdecodableformat(_:))
- [func CMAudioFormatDescriptionGetStreamBasicDescription(CMAudioFormatDescription) -> UnsafePointer<AudioStreamBasicDescription>?](/documentation/coremedia/cmaudioformatdescriptiongetstreambasicdescription(_:))
- [func CMDoesBigEndianSoundDescriptionRequireLegacyCBRSampleTableLayout(CMBlockBuffer, flavor: CMSoundDescriptionFlavor?) -> Bool](/documentation/coremedia/cmdoesbigendiansounddescriptionrequirelegacycbrsampletablelayout(_:flavor:))
- [func CMSwapBigEndianSoundDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendiansounddescriptiontohost(_:_:))
- [func CMSwapHostEndianSoundDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendiansounddescriptiontobig(_:_:))
- [func CMAudioFormatDescriptionCreateFromBigEndianSoundDescriptionData(allocator: CFAllocator?, bigEndianSoundDescriptionData: UnsafePointer<UInt8>, size: Int, flavor: CMSoundDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMAudioFormatDescription?>) -> OSStatus](/documentation/coremedia/cmaudioformatdescriptioncreatefrombigendiansounddescriptiondata(allocator:bigendiansounddescriptiondata:size:flavor:formatdescriptionout:))
- [func CMAudioFormatDescriptionCreateFromBigEndianSoundDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianSoundDescriptionBlockBuffer: CMBlockBuffer, flavor: CMSoundDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMAudioFormatDescription?>) -> OSStatus](/documentation/coremedia/cmaudioformatdescriptioncreatefrombigendiansounddescriptionblockbuffer(allocator:bigendiansounddescriptionblockbuffer:flavor:formatdescriptionout:))
- [func CMAudioFormatDescriptionCopyAsBigEndianSoundDescriptionBlockBuffer(allocator: CFAllocator?, audioFormatDescription: CMAudioFormatDescription, flavor: CMSoundDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmaudioformatdescriptioncopyasbigendiansounddescriptionblockbuffer(allocator:audioformatdescription:flavor:blockbufferout:))

### Working with Video Descriptions

- [CMImageDescriptionFlavor](/documentation/coremedia/cmimagedescriptionflavor)

#### Image Description Flavors

- [static let isoFamily: CMImageDescriptionFlavor](/documentation/coremedia/cmimagedescriptionflavor/isofamily)
- [static let mobile3GPFamily: CMImageDescriptionFlavor](/documentation/coremedia/cmimagedescriptionflavor/mobile3gpfamily)
- [static let quickTimeMovie: CMImageDescriptionFlavor](/documentation/coremedia/cmimagedescriptionflavor/quicktimemovie)

#### Creating Image Description Flavors

- [init(CFString)](/documentation/coremedia/cmimagedescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmimagedescriptionflavor/init(rawvalue:))

#### Type Properties

- [static let isoFamilyWithAppleExtensions: CMImageDescriptionFlavor](/documentation/coremedia/cmimagedescriptionflavor/isofamilywithappleextensions)
- [func CMVideoFormatDescriptionCreate(allocator: CFAllocator?, codecType: CMVideoCodecType, width: Int32, height: Int32, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMVideoFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreate(allocator:codectype:width:height:extensions:formatdescriptionout:))
- [func CMVideoFormatDescriptionCreateForImageBuffer(allocator: CFAllocator?, imageBuffer: CVImageBuffer, formatDescriptionOut: UnsafeMutablePointer<CMVideoFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreateforimagebuffer(allocator:imagebuffer:formatdescriptionout:))
- [func CMVideoFormatDescriptionGetCleanAperture(CMVideoFormatDescription, originIsAtTopLeft: Bool) -> CGRect](/documentation/coremedia/cmvideoformatdescriptiongetcleanaperture(_:originisattopleft:))
- [func CMVideoFormatDescriptionGetDimensions(CMVideoFormatDescription) -> CMVideoDimensions](/documentation/coremedia/cmvideoformatdescriptiongetdimensions(_:))
- [func CMVideoFormatDescriptionGetExtensionKeysCommonWithImageBuffers() -> CFArray](/documentation/coremedia/cmvideoformatdescriptiongetextensionkeyscommonwithimagebuffers())
- [func CMVideoFormatDescriptionGetPresentationDimensions(CMVideoFormatDescription, usePixelAspectRatio: Bool, useCleanAperture: Bool) -> CGSize](/documentation/coremedia/cmvideoformatdescriptiongetpresentationdimensions(_:usepixelaspectratio:usecleanaperture:))
- [func CMVideoFormatDescriptionMatchesImageBuffer(CMVideoFormatDescription, imageBuffer: CVImageBuffer) -> Bool](/documentation/coremedia/cmvideoformatdescriptionmatchesimagebuffer(_:imagebuffer:))
- [func CMVideoFormatDescriptionCreateFromH264ParameterSets(allocator: CFAllocator?, parameterSetCount: Int, parameterSetPointers: UnsafePointer<UnsafePointer<UInt8>>, parameterSetSizes: UnsafePointer<Int>, nalUnitHeaderLength: Int32, formatDescriptionOut: UnsafeMutablePointer<CMFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreatefromh264parametersets(allocator:parametersetcount:parametersetpointers:parametersetsizes:nalunitheaderlength:formatdescriptionout:))
- [func CMVideoFormatDescriptionCreateFromHEVCParameterSets(allocator: CFAllocator?, parameterSetCount: Int, parameterSetPointers: UnsafePointer<UnsafePointer<UInt8>>, parameterSetSizes: UnsafePointer<Int>, nalUnitHeaderLength: Int32, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreatefromhevcparametersets(allocator:parametersetcount:parametersetpointers:parametersetsizes:nalunitheaderlength:extensions:formatdescriptionout:))
- [func CMVideoFormatDescriptionGetH264ParameterSetAtIndex(CMFormatDescription, parameterSetIndex: Int, parameterSetPointerOut: UnsafeMutablePointer<UnsafePointer<UInt8>?>?, parameterSetSizeOut: UnsafeMutablePointer<Int>?, parameterSetCountOut: UnsafeMutablePointer<Int>?, nalUnitHeaderLengthOut: UnsafeMutablePointer<Int32>?) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptiongeth264parametersetatindex(_:parametersetindex:parametersetpointerout:parametersetsizeout:parametersetcountout:nalunitheaderlengthout:))
- [func CMVideoFormatDescriptionCopyAsBigEndianImageDescriptionBlockBuffer(allocator: CFAllocator?, videoFormatDescription: CMVideoFormatDescription, stringEncoding: CFStringEncoding, flavor: CMImageDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncopyasbigendianimagedescriptionblockbuffer(allocator:videoformatdescription:stringencoding:flavor:blockbufferout:))
- [func CMVideoFormatDescriptionCreateFromBigEndianImageDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianImageDescriptionBlockBuffer: CMBlockBuffer, stringEncoding: CFStringEncoding, flavor: CMImageDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMVideoFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreatefrombigendianimagedescriptionblockbuffer(allocator:bigendianimagedescriptionblockbuffer:stringencoding:flavor:formatdescriptionout:))
- [func CMVideoFormatDescriptionCreateFromBigEndianImageDescriptionData(allocator: CFAllocator?, bigEndianImageDescriptionData: UnsafePointer<UInt8>, size: Int, stringEncoding: CFStringEncoding, flavor: CMImageDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMVideoFormatDescription?>) -> OSStatus](/documentation/coremedia/cmvideoformatdescriptioncreatefrombigendianimagedescriptiondata(allocator:bigendianimagedescriptiondata:size:stringencoding:flavor:formatdescriptionout:))
- [func CMSwapBigEndianImageDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendianimagedescriptiontohost(_:_:))
- [func CMSwapHostEndianImageDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendianimagedescriptiontobig(_:_:))

### Working with Muxed Descriptions

- [func CMMuxedFormatDescriptionCreate(allocator: CFAllocator?, muxType: CMMuxedStreamType, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMMuxedFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmuxedformatdescriptioncreate(allocator:muxtype:extensions:formatdescriptionout:))

### Working with Metadata Descriptions

- [CMMetadataDescriptionFlavor](/documentation/coremedia/cmmetadatadescriptionflavor)

#### Creating Metadata Description Flavors

- [init(CFString)](/documentation/coremedia/cmmetadatadescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmmetadatadescriptionflavor/init(rawvalue:))
- [func CMMetadataFormatDescriptionCreateWithKeys(allocator: CFAllocator?, metadataType: CMMetadataFormatType, keys: CFArray?, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatewithkeys(allocator:metadatatype:keys:formatdescriptionout:))
- [func CMMetadataFormatDescriptionGetKeyWithLocalID(CMMetadataFormatDescription, localKeyID: OSType) -> CFDictionary?](/documentation/coremedia/cmmetadataformatdescriptiongetkeywithlocalid(_:localkeyid:))
- [func CMMetadataFormatDescriptionCopyAsBigEndianMetadataDescriptionBlockBuffer(allocator: CFAllocator?, metadataFormatDescription: CMMetadataFormatDescription, flavor: CMMetadataDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncopyasbigendianmetadatadescriptionblockbuffer(allocator:metadataformatdescription:flavor:blockbufferout:))
- [func CMMetadataFormatDescriptionCreateByMergingMetadataFormatDescriptions(allocator: CFAllocator?, sourceDescription: CMMetadataFormatDescription, otherSourceDescription: CMMetadataFormatDescription, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatebymergingmetadataformatdescriptions(allocator:sourcedescription:othersourcedescription:formatdescriptionout:))
- [func CMMetadataFormatDescriptionCreateFromBigEndianMetadataDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianMetadataDescriptionBlockBuffer: CMBlockBuffer, flavor: CMMetadataDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatefrombigendianmetadatadescriptionblockbuffer(allocator:bigendianmetadatadescriptionblockbuffer:flavor:formatdescriptionout:))
- [func CMMetadataFormatDescriptionCreateFromBigEndianMetadataDescriptionData(allocator: CFAllocator?, bigEndianMetadataDescriptionData: UnsafePointer<UInt8>, size: Int, flavor: CMMetadataDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatefrombigendianmetadatadescriptiondata(allocator:bigendianmetadatadescriptiondata:size:flavor:formatdescriptionout:))
- [func CMMetadataFormatDescriptionCreateWithMetadataFormatDescriptionAndMetadataSpecifications(allocator: CFAllocator?, sourceDescription: CMMetadataFormatDescription, metadataSpecifications: CFArray, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatewithmetadataformatdescriptionandmetadataspecifications(allocator:sourcedescription:metadataspecifications:formatdescriptionout:))
- [func CMMetadataFormatDescriptionCreateWithMetadataSpecifications(allocator: CFAllocator?, metadataType: CMMetadataFormatType, metadataSpecifications: CFArray, formatDescriptionOut: UnsafeMutablePointer<CMMetadataFormatDescription?>) -> OSStatus](/documentation/coremedia/cmmetadataformatdescriptioncreatewithmetadataspecifications(allocator:metadatatype:metadataspecifications:formatdescriptionout:))
- [func CMSwapBigEndianMetadataDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendianmetadatadescriptiontohost(_:_:))
- [func CMSwapHostEndianMetadataDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendianmetadatadescriptiontobig(_:_:))
- [func CMMetadataFormatDescriptionGetIdentifiers(CMMetadataFormatDescription) -> CFArray?](/documentation/coremedia/cmmetadataformatdescriptiongetidentifiers(_:))

### Working with Text Descriptions

- [CMTextDescriptionFlavor](/documentation/coremedia/cmtextdescriptionflavor)

#### Creating Text Description Flavors

- [init(CFString)](/documentation/coremedia/cmtextdescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmtextdescriptionflavor/init(rawvalue:))
- [func CMTextFormatDescriptionGetDefaultStyle(CMFormatDescription, localFontIDOut: UnsafeMutablePointer<UInt16>?, boldOut: UnsafeMutablePointer<DarwinBoolean>?, italicOut: UnsafeMutablePointer<DarwinBoolean>?, underlineOut: UnsafeMutablePointer<DarwinBoolean>?, fontSizeOut: UnsafeMutablePointer<CGFloat>?, colorComponentsOut: UnsafeMutablePointer<CGFloat>?) -> OSStatus](/documentation/coremedia/cmtextformatdescriptiongetdefaultstyle(_:localfontidout:boldout:italicout:underlineout:fontsizeout:colorcomponentsout:))
- [func CMTextFormatDescriptionGetDefaultTextBox(CMFormatDescription, originIsAtTopLeft: Bool, heightOfTextTrack: CGFloat, defaultTextBoxOut: UnsafeMutablePointer<CGRect>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptiongetdefaulttextbox(_:originisattopleft:heightoftexttrack:defaulttextboxout:))
- [func CMTextFormatDescriptionGetDisplayFlags(CMFormatDescription, displayFlagsOut: UnsafeMutablePointer<CMTextDisplayFlags>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptiongetdisplayflags(_:displayflagsout:))
- [func CMTextFormatDescriptionGetFontName(CMFormatDescription, localFontID: UInt16, fontNameOut: AutoreleasingUnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptiongetfontname(_:localfontid:fontnameout:))
- [func CMTextFormatDescriptionGetJustification(CMFormatDescription, horizontalOut: UnsafeMutablePointer<CMTextJustificationValue>?, verticalOut: UnsafeMutablePointer<CMTextJustificationValue>?) -> OSStatus](/documentation/coremedia/cmtextformatdescriptiongetjustification(_:horizontalout:verticalout:))
- [func CMTextFormatDescriptionCopyAsBigEndianTextDescriptionBlockBuffer(allocator: CFAllocator?, textFormatDescription: CMTextFormatDescription, flavor: CMTextDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptioncopyasbigendiantextdescriptionblockbuffer(allocator:textformatdescription:flavor:blockbufferout:))
- [func CMTextFormatDescriptionCreateFromBigEndianTextDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianTextDescriptionBlockBuffer: CMBlockBuffer, flavor: CMTextDescriptionFlavor?, mediaType: CMMediaType, formatDescriptionOut: UnsafeMutablePointer<CMTextFormatDescription?>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptioncreatefrombigendiantextdescriptionblockbuffer(allocator:bigendiantextdescriptionblockbuffer:flavor:mediatype:formatdescriptionout:))
- [func CMTextFormatDescriptionCreateFromBigEndianTextDescriptionData(allocator: CFAllocator?, bigEndianTextDescriptionData: UnsafePointer<UInt8>, size: Int, flavor: CMTextDescriptionFlavor?, mediaType: CMMediaType, formatDescriptionOut: UnsafeMutablePointer<CMTextFormatDescription?>) -> OSStatus](/documentation/coremedia/cmtextformatdescriptioncreatefrombigendiantextdescriptiondata(allocator:bigendiantextdescriptiondata:size:flavor:mediatype:formatdescriptionout:))
- [func CMSwapBigEndianTextDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendiantextdescriptiontohost(_:_:))
- [func CMSwapHostEndianTextDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendiantextdescriptiontobig(_:_:))

### Working with Time Code Descriptions

- [CMTimeCodeDescriptionFlavor](/documentation/coremedia/cmtimecodedescriptionflavor)

#### Creating a Timecode Description Flavor

- [init(CFString)](/documentation/coremedia/cmtimecodedescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmtimecodedescriptionflavor/init(rawvalue:))
- [func CMTimeCodeFormatDescriptionCreate(allocator: CFAllocator?, timeCodeFormatType: CMTimeCodeFormatType, frameDuration: CMTime, frameQuanta: UInt32, flags: UInt32, extensions: CFDictionary?, formatDescriptionOut: UnsafeMutablePointer<CMTimeCodeFormatDescription?>) -> OSStatus](/documentation/coremedia/cmtimecodeformatdescriptioncreate(allocator:timecodeformattype:frameduration:framequanta:flags:extensions:formatdescriptionout:))
- [func CMTimeCodeFormatDescriptionGetFrameDuration(CMTimeCodeFormatDescription) -> CMTime](/documentation/coremedia/cmtimecodeformatdescriptiongetframeduration(_:))
- [func CMTimeCodeFormatDescriptionGetFrameQuanta(CMTimeCodeFormatDescription) -> UInt32](/documentation/coremedia/cmtimecodeformatdescriptiongetframequanta(_:))
- [func CMTimeCodeFormatDescriptionGetTimeCodeFlags(CMTimeCodeFormatDescription) -> UInt32](/documentation/coremedia/cmtimecodeformatdescriptiongettimecodeflags(_:))
- [func CMTimeCodeFormatDescriptionCopyAsBigEndianTimeCodeDescriptionBlockBuffer(allocator: CFAllocator?, timeCodeFormatDescription: CMTimeCodeFormatDescription, flavor: CMTimeCodeDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmtimecodeformatdescriptioncopyasbigendiantimecodedescriptionblockbuffer(allocator:timecodeformatdescription:flavor:blockbufferout:))
- [func CMTimeCodeFormatDescriptionCreateFromBigEndianTimeCodeDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianTimeCodeDescriptionBlockBuffer: CMBlockBuffer, flavor: CMTimeCodeDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMTimeCodeFormatDescription?>) -> OSStatus](/documentation/coremedia/cmtimecodeformatdescriptioncreatefrombigendiantimecodedescriptionblockbuffer(allocator:bigendiantimecodedescriptionblockbuffer:flavor:formatdescriptionout:))
- [func CMTimeCodeFormatDescriptionCreateFromBigEndianTimeCodeDescriptionData(allocator: CFAllocator?, bigEndianTimeCodeDescriptionData: UnsafePointer<UInt8>, size: Int, flavor: CMTimeCodeDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMTimeCodeFormatDescription?>) -> OSStatus](/documentation/coremedia/cmtimecodeformatdescriptioncreatefrombigendiantimecodedescriptiondata(allocator:bigendiantimecodedescriptiondata:size:flavor:formatdescriptionout:))
- [func CMSwapBigEndianTimeCodeDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendiantimecodedescriptiontohost(_:_:))
- [func CMSwapHostEndianTimeCodeDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendiantimecodedescriptiontobig(_:_:))

### Working with Closed Captioning Descriptions

- [CMClosedCaptionDescriptionFlavor](/documentation/coremedia/cmclosedcaptiondescriptionflavor)

#### Initializers

- [init(CFString)](/documentation/coremedia/cmclosedcaptiondescriptionflavor/init(_:))
- [init(rawValue: CFString)](/documentation/coremedia/cmclosedcaptiondescriptionflavor/init(rawvalue:))
- [func CMClosedCaptionFormatDescriptionCopyAsBigEndianClosedCaptionDescriptionBlockBuffer(allocator: CFAllocator?, closedCaptionFormatDescription: CMClosedCaptionFormatDescription, flavor: CMClosedCaptionDescriptionFlavor?, blockBufferOut: UnsafeMutablePointer<CMBlockBuffer?>) -> OSStatus](/documentation/coremedia/cmclosedcaptionformatdescriptioncopyasbigendianclosedcaptiondescriptionblockbuffer(allocator:closedcaptionformatdescription:flavor:blockbufferout:))
- [func CMClosedCaptionFormatDescriptionCreateFromBigEndianClosedCaptionDescriptionBlockBuffer(allocator: CFAllocator?, bigEndianClosedCaptionDescriptionBlockBuffer: CMBlockBuffer, flavor: CMClosedCaptionDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMClosedCaptionFormatDescription?>) -> OSStatus](/documentation/coremedia/cmclosedcaptionformatdescriptioncreatefrombigendianclosedcaptiondescriptionblockbuffer(allocator:bigendianclosedcaptiondescriptionblockbuffer:flavor:formatdescriptionout:))
- [func CMClosedCaptionFormatDescriptionCreateFromBigEndianClosedCaptionDescriptionData(allocator: CFAllocator?, bigEndianClosedCaptionDescriptionData: UnsafePointer<UInt8>, size: Int, flavor: CMClosedCaptionDescriptionFlavor?, formatDescriptionOut: UnsafeMutablePointer<CMClosedCaptionFormatDescription?>) -> OSStatus](/documentation/coremedia/cmclosedcaptionformatdescriptioncreatefrombigendianclosedcaptiondescriptiondata(allocator:bigendianclosedcaptiondescriptiondata:size:flavor:formatdescriptionout:))
- [func CMSwapHostEndianClosedCaptionDescriptionToBig(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswaphostendianclosedcaptiondescriptiontobig(_:_:))
- [func CMSwapBigEndianClosedCaptionDescriptionToHost(UnsafeMutablePointer<UInt8>, Int) -> OSStatus](/documentation/coremedia/cmswapbigendianclosedcaptiondescriptiontohost(_:_:))

### Format Description Types

- [CMFormatDescription](/documentation/coremedia/cmformatdescription)

#### Inspecting Format Descriptions

- [var audioFormatList: [AudioFormatListItem]](/documentation/coremedia/cmformatdescription/audioformatlist)
- [var audioStreamBasicDescription: AudioStreamBasicDescription?](/documentation/coremedia/cmformatdescription/audiostreambasicdescription)
- [var audioChannelLayout: ManagedAudioChannelLayout?](/documentation/coremedia/cmformatdescription/audiochannellayout)
- [var dimensions: CMVideoDimensions](/documentation/coremedia/cmformatdescription/dimensions)
- [var extensions: CMFormatDescription.Extensions](/documentation/coremedia/cmformatdescription/extensions-swift.property)
- [var frameDuration: CMTime](/documentation/coremedia/cmformatdescription/frameduration)
- [var frameQuanta: UInt32](/documentation/coremedia/cmformatdescription/framequanta)
- [var identifiers: [String]](/documentation/coremedia/cmformatdescription/identifiers)
- [var magicCookie: Data?](/documentation/coremedia/cmformatdescription/magiccookie)
- [var mediaSubType: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.property)
- [var mediaType: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.property)
- [var mostCompatibleFormat: AudioFormatListItem?](/documentation/coremedia/cmformatdescription/mostcompatibleformat)
- [var nalUnitHeaderLength: Int?](/documentation/coremedia/cmformatdescription/nalunitheaderlength)
- [var parameterSets: CMFormatDescription.ParameterSetCollection](/documentation/coremedia/cmformatdescription/parametersets)
- [var richestDecodableFormat: AudioFormatListItem?](/documentation/coremedia/cmformatdescription/richestdecodableformat)
- [var timeCodeFlags: CMFormatDescription.TimeCode.Flag](/documentation/coremedia/cmformatdescription/timecodeflags)
- [var tagCollections: [[CMTag]]?](/documentation/coremedia/cmformatdescription/tagcollections)
- [func matchesTaggedBufferGroup([CMTaggedBuffer]) -> Bool](/documentation/coremedia/cmformatdescription/matchestaggedbuffergroup(_:))

#### Working with Audio Descriptions

- [func withMagicCookie<R>((UnsafeRawBufferPointer?) throws -> R) rethrows -> R](/documentation/coremedia/cmformatdescription/withmagiccookie(_:))

#### Working with Video Descriptions

- [func cleanAperture(originIsAtTopLeft: Bool) -> CGRect](/documentation/coremedia/cmformatdescription/cleanaperture(originisattopleft:))
- [func matchesImageBuffer(CVImageBuffer) -> Bool](/documentation/coremedia/cmformatdescription/matchesimagebuffer(_:))
- [func presentationDimensions(usePixelAspectRatio: Bool, useCleanAperture: Bool) -> CGSize](/documentation/coremedia/cmformatdescription/presentationdimensions(usepixelaspectratio:usecleanaperture:))

#### Working with Metadata Descriptions

- [func keyWithLocalID(OSType) -> [String : CFPropertyList]?](/documentation/coremedia/cmformatdescription/keywithlocalid(_:))

#### Working with Text Descriptions

- [func defaultStyle() throws -> (localFontID: Int, bold: Bool, italic: Bool, underline: Bool, fontSize: CGFloat, colorComponents: [CGFloat])](/documentation/coremedia/cmformatdescription/defaultstyle())
- [func defaultTextBox(originIsAtTopLeft: Bool, heightOfTextTrack: CGFloat) throws -> CGRect](/documentation/coremedia/cmformatdescription/defaulttextbox(originisattopleft:heightoftexttrack:))
- [func displayFlags() throws -> CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/displayflags())
- [func fontName(localFontID: Int) throws -> String](/documentation/coremedia/cmformatdescription/fontname(localfontid:))
- [func justification() throws -> (horizontal: CMFormatDescription.Extensions.Value.TextJustification, vertical: CMFormatDescription.Extensions.Value.TextJustification)](/documentation/coremedia/cmformatdescription/justification())

#### Comparing Format Descriptions

- [static func == (CMFormatDescription, CMFormatDescription) -> Bool](/documentation/coremedia/cmformatdescription/==(_:_:))
- [func equalTo(CMAudioFormatDescription, equalityMask: CMFormatDescription.EqualityMask) -> (Bool, equalityMask: CMFormatDescription.EqualityMask)](/documentation/coremedia/cmformatdescription/equalto(_:equalitymask:))
- [func equalTo(CMFormatDescription, extensionKeysToIgnore: [CMFormatDescription.Extensions.Key], sampleDescriptionExtensionAtomKeysToIgnore: [String]) -> Bool](/documentation/coremedia/cmformatdescription/equalto(_:extensionkeystoignore:sampledescriptionextensionatomkeystoignore:))

#### Errors

- [CMFormatDescription.Error](/documentation/coremedia/cmformatdescription/error)

##### Errors

- [static let allocationFailed: NSError](/documentation/coremedia/cmformatdescription/error/allocationfailed)
- [static let invalidParameter: NSError](/documentation/coremedia/cmformatdescription/error/invalidparameter)
- [static let valueNotAvailable: NSError](/documentation/coremedia/cmformatdescription/error/valuenotavailable)

#### Constants

- [static var extensionKeysCommonWithImageBuffers: [CMFormatDescription.Extensions.Key]](/documentation/coremedia/cmformatdescription/extensionkeyscommonwithimagebuffers)
- [static var typeID: CFTypeID](/documentation/coremedia/cmformatdescription/typeid)
- [CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct)

##### Media Types

- [static let audio: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/audio)
- [static let closedCaption: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/closedcaption)
- [static let metadata: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/metadata)
- [static let muxed: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/muxed)
- [static let subtitle: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/subtitle)
- [static let text: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/text)
- [static let timeCode: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/timecode)
- [static let video: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/video)
- [static let taggedBufferGroup: CMFormatDescription.MediaType](/documentation/coremedia/cmformatdescription/mediatype-swift.struct/taggedbuffergroup)
- [CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct)

##### Media Subtypes

- [static let aLaw: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/alaw)
- [static let aacAudibleProtected: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/aacaudibleprotected)
- [static let aacLCProtected: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/aaclcprotected)
- [static let ac3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/ac3)
- [static let aes3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/aes3)
- [static let amr: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/amr)
- [static let amr_WB: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/amr_wb)
- [static let animation: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/animation)
- [static let appleIMA4: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/appleima4)
- [static let appleLossless: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/applelossless)
- [static let atsc: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/atsc)
- [static let audible: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/audible)
- [static let boxed: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/boxed)
- [static let cea608: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/cea608)
- [static let cea708: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/cea708)
- [static let cinepak: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/cinepak)
- [static let counter32: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/counter32)
- [static let counter64: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/counter64)
- [static let dv: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dv)
- [static let dvcNTSC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcntsc)
- [static let dvcPAL: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcpal)
- [static let dvcPROHD1080i50: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd1080i50)
- [static let dvcPROHD1080i60: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd1080i60)
- [static let dvcPROHD1080p25: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd1080p25)
- [static let dvcPROHD1080p30: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd1080p30)
- [static let dvcPROHD720p50: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd720p50)
- [static let dvcPROHD720p60: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcprohd720p60)
- [static let dvcPro50NTSC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcpro50ntsc)
- [static let dvcPro50PAL: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcpro50pal)
- [static let dvcProPAL: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dvcpropal)
- [static let dviIntelIMA: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/dviintelima)
- [static let emsg: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/emsg)
- [static let enhancedAC3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/enhancedac3)
- [static let flac: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/flac)
- [static let h263: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/h263)
- [static let h264: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/h264)
- [static let hevc: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/hevc)
- [static let hevcWithAlpha: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/hevcwithalpha)
- [static let iLBC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/ilbc)
- [static let icy: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/icy)
- [static let id3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/id3)
- [static let iec60958AC3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/iec60958ac3)
- [static let jpeg: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/jpeg)
- [static let jpeg_OpenDML: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/jpeg_opendml)
- [static let linearPCM: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/linearpcm)
- [static let mace3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mace3)
- [static let mace6: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mace6)
- [static let microsoftGSM: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/microsoftgsm)
- [static let midiStream: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/midistream)
- [static let mobile3GPP: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mobile3gpp)
- [static let mpeg1System: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg1system)
- [static let mpeg1Video: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg1video)
- [static let mpeg2Program: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg2program)
- [static let mpeg2Transport: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg2transport)
- [static let mpeg2Video: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg2video)
- [static let mpeg4AAC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac)
- [static let mpeg4AAC_ELD: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_eld)
- [static let mpeg4AAC_ELD_SBR: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_eld_sbr)
- [static let mpeg4AAC_ELD_V2: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_eld_v2)
- [static let mpeg4AAC_HE: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_he)
- [static let mpeg4AAC_HE_V2: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_he_v2)
- [static let mpeg4AAC_LD: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_ld)
- [static let mpeg4AAC_Spatial: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4aac_spatial)
- [static let mpeg4CELP: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4celp)
- [static let mpeg4HVXC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4hvxc)
- [static let mpeg4TwinVQ: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4twinvq)
- [static let mpeg4Video: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeg4video)
- [static let mpegD_USAC: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpegd_usac)
- [static let mpegLayer1: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeglayer1)
- [static let mpegLayer2: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeglayer2)
- [static let mpegLayer3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/mpeglayer3)
- [static let opus: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/opus)
- [static let parameterValueStream: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/parametervaluestream)
- [static let pixelFormat_16BE555: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_16be555)
- [static let pixelFormat_16BE565: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_16be565)
- [static let pixelFormat_16LE555: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_16le555)
- [static let pixelFormat_16LE5551: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_16le5551)
- [static let pixelFormat_16LE565: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_16le565)
- [static let pixelFormat_24RGB: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_24rgb)
- [static let pixelFormat_32ARGB: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_32argb)
- [static let pixelFormat_32BGRA: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_32bgra)
- [static let pixelFormat_422YpCbCr10: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_422ypcbcr10)
- [static let pixelFormat_422YpCbCr16: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_422ypcbcr16)
- [static let pixelFormat_422YpCbCr8: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_422ypcbcr8)
- [static let pixelFormat_422YpCbCr8_yuvs: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_422ypcbcr8_yuvs)
- [static let pixelFormat_4444YpCbCrA8: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_4444ypcbcra8)
- [static let pixelFormat_444YpCbCr10: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_444ypcbcr10)
- [static let pixelFormat_444YpCbCr8: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_444ypcbcr8)
- [static let pixelFormat_8IndexedGray_WhiteIsZero: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/pixelformat_8indexedgray_whiteiszero)
- [static let proRes422: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores422)
- [static let proRes422HQ: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores422hq)
- [static let proRes422LT: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores422lt)
- [static let proRes422Proxy: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores422proxy)
- [static let proRes4444: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores4444)
- [static let proRes4444XQ: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/prores4444xq)
- [static let proResRAW: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/proresraw)
- [static let proResRAWHQ: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/proresrawhq)
- [static let qDesign: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/qdesign)
- [static let qDesign2: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/qdesign2)
- [static let qt: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/qt)
- [static let qualcomm: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/qualcomm)
- [static let sorensonVideo: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/sorensonvideo)
- [static let sorensonVideo3: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/sorensonvideo3)
- [static let timeCode: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/timecode)
- [static let timeCode32: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/timecode32)
- [static let timeCode64: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/timecode64)
- [static let uLaw: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/ulaw)
- [static let webVTT: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/webvtt)
- [static let embeddedDeviceScreenRecording: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/embeddeddevicescreenrecording)
- [static let tbgr: CMFormatDescription.MediaSubType](/documentation/coremedia/cmformatdescription/mediasubtype-swift.struct/tbgr)
- [CMFormatDescription.TimeCode](/documentation/coremedia/cmformatdescription/timecode)

##### Constants

- [CMFormatDescription.TimeCode.Flag](/documentation/coremedia/cmformatdescription/timecode/flag)

###### Time Code Flags

- [static let dropFrame: CMFormatDescription.TimeCode.Flag](/documentation/coremedia/cmformatdescription/timecode/flag/dropframe)
- [static let negTimesOK: CMFormatDescription.TimeCode.Flag](/documentation/coremedia/cmformatdescription/timecode/flag/negtimesok)
- [static let twentyFourHourMax: CMFormatDescription.TimeCode.Flag](/documentation/coremedia/cmformatdescription/timecode/flag/twentyfourhourmax)
- [CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask)

##### Equality Masks

- [static let all: CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask/all)
- [static let channelLayout: CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask/channellayout)
- [static let extensions: CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask/extensions)
- [static let magicCookie: CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask/magiccookie)
- [static let streamBasicDescription: CMFormatDescription.EqualityMask](/documentation/coremedia/cmformatdescription/equalitymask/streambasicdescription)
- [CMFormatDescription.Extensions](/documentation/coremedia/cmformatdescription/extensions-swift.struct)

##### Creating Extensions

- [init()](/documentation/coremedia/cmformatdescription/extensions-swift.struct/init())
- [init(base: [CFString : CFPropertyList]?)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/init(base:))

##### Finding Extension Elements

- [subscript(CFString) -> CFPropertyList?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/subscript(_:)-1c6vg)
- [subscript(CMFormatDescription.Extensions.Key) -> CMFormatDescription.Extensions.Value?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/subscript(_:)-80zh8)

##### Constants

- [CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key)

###### Extension Keys

- [static let alphaChannelMode: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/alphachannelmode)
- [static let alternativeTransferCharacteristics: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/alternativetransfercharacteristics)
- [static let ambientViewingEnvironment: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/ambientviewingenvironment)
- [static let auxiliaryTypeInfo: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/auxiliarytypeinfo)
- [static let backgroundColor: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/backgroundcolor)
- [static let bitsPerComponent: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/bitspercomponent)
- [static let bytesPerRow: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/bytesperrow)
- [static let chromaLocationBottomField: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/chromalocationbottomfield)
- [static let chromaLocationTopField: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/chromalocationtopfield)
- [static let cleanAperture: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/cleanaperture)
- [static let colorPrimaries: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/colorprimaries)
- [static let conformsToMPEG2VideoProfile: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/conformstompeg2videoprofile)
- [static let containsAlphaChannel: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/containsalphachannel)
- [static let contentLightLevelInfo: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/contentlightlevelinfo)
- [static let defaultFontName: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/defaultfontname)
- [static let defaultStyle: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/defaultstyle)
- [static let defaultTextBox: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/defaulttextbox)
- [static let depth: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/depth)
- [static let displayFlags: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/displayflags)
- [static let fieldCount: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/fieldcount)
- [static let fieldDetail: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/fielddetail)
- [static let fontTable: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/fonttable)
- [static let formatName: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/formatname)
- [static let fullRangeVideo: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/fullrangevideo)
- [static let gammaLevel: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/gammalevel)
- [static let horizontalJustification: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/horizontaljustification)
- [static let iccProfile: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/iccprofile)
- [static let masteringDisplayColorVolume: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/masteringdisplaycolorvolume)
- [static let metadataKeyTable: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/metadatakeytable)
- [static let originalCompressionSettings: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/originalcompressionsettings)
- [static let pixelAspectRatio: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/pixelaspectratio)
- [static let revisionLevel: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/revisionlevel)
- [static let sampleDescriptionExtensionAtoms: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/sampledescriptionextensionatoms)
- [static let sourceReferenceName: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/sourcereferencename)
- [static let spatialQuality: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/spatialquality)
- [static let temporalQuality: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/temporalquality)
- [static let textJustification: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/textjustification)
- [static let transferFunction: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/transferfunction)
- [static let vendor: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/vendor)
- [static let verbatimISOSampleEntry: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/verbatimisosampleentry)
- [static let verbatimSampleDescription: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/verbatimsampledescription)
- [static let version: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/version)
- [static let verticalJustification: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/verticaljustification)
- [static let yCbCrMatrix: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/ycbcrmatrix)

###### Initializers

- [init(rawValue: CFString)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/init(rawvalue:))

###### Type Properties

- [static let cameraCalibrationDataLensCollection: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/cameracalibrationdatalenscollection)
- [static var contentColorVolume: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/contentcolorvolume)
- [static let convertedFromExternalSphericalTags: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/convertedfromexternalsphericaltags)
- [static var hasAdditionalViews: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/hasadditionalviews)
- [static var hasLeftStereoEyeView: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/hasleftstereoeyeview)
- [static var hasRightStereoEyeView: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/hasrightstereoeyeview)
- [static var heroEye: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/heroeye)
- [static var horizontalDisparityAdjustment: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/horizontaldisparityadjustment)
- [static var horizontalFieldOfView: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/horizontalfieldofview)
- [static var logTransferFunction: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/logtransferfunction)
- [static var projectionKind: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/projectionkind)
- [static var protectedContentOriginalFormat: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/protectedcontentoriginalformat)
- [static var stereoCameraBaseline: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/stereocamerabaseline)
- [static let viewPackingKind: CMFormatDescription.Extensions.Key](/documentation/coremedia/cmformatdescription/extensions-swift.struct/key/viewpackingkind)
- [CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value)

###### Extension Values

- [static func alphaChannelMode(CMFormatDescription.Extensions.Value.AlphaChannelMode) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/alphachannelmode(_:))
- [static func chromaLocation(CMFormatDescription.Extensions.Value.ChromaLocation) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation(_:))
- [static func cleanAperture(width: (numerator: Int, denominator: Int), height: (numerator: Int, denominator: Int), horizontalOffet: (numerator: Int, denominator: Int), verticalOffset: (numerator: Int, denominator: Int)) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cleanaperture(width:height:horizontaloffet:verticaloffset:)-4b52p)
- [static func cleanAperture<Width, Height, Horizontal, Vertical>(width: Width, height: Height, horizontalOffet: Horizontal, verticalOffset: Vertical) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cleanaperture(width:height:horizontaloffet:verticaloffset:)-2r4iq)
- [static func colorPrimaries(CMFormatDescription.Extensions.Value.ColorPrimaries) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries(_:))
- [static func data(CFData) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/data(_:))
- [static func fieldDetail(CMFormatDescription.Extensions.Value.FieldDetail) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail(_:))
- [static func fontTable([Int : String]) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fonttable(_:))
- [static func mobile3GPPTextColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mobile3gpptextcolor(red:green:blue:alpha:))
- [static func mobile3GPPTextDefaultStyle(startChar: Int, endChar: Int, localFontID: Int, fontFace: CMFormatDescription.Extensions.Value.FontFace, fontSize: Int, foregroundColor: CMFormatDescription.Extensions.Value) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mobile3gpptextdefaultstyle(startchar:endchar:localfontid:fontface:fontsize:foregroundcolor:))
- [static func mpeg2VideoProfile(CMFormatDescription.Extensions.Value.MPEG2VideoProfile) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile(_:))
- [static func number<T>(T) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/number(_:))
- [static func pixelAspectRatio<Horizontal, Vertical>(horizontalSpacing: Horizontal, verticalSpacing: Vertical) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/pixelaspectratio(horizontalspacing:verticalspacing:))
- [static func qtTextColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/qttextcolor(red:green:blue:alpha:))
- [static func qtTextDefaultStyle(startChar: Int, height: Int, ascent: Int, localFontID: Int, fontFace: CMFormatDescription.Extensions.Value.FontFace, fontSize: Int, foregroundColor: CMFormatDescription.Extensions.Value, defaultFontName: String?) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/qttextdefaultstyle(startchar:height:ascent:localfontid:fontface:fontsize:foregroundcolor:defaultfontname:))
- [static func sourceReferenceName(value: String, langCode: Int) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/sourcereferencename(value:langcode:))
- [static func string(String) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/string(_:)-52jj4)
- [static func string(CFString) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/string(_:)-6y3ip)
- [static func textDisplayFlags(Set<CMFormatDescription.Extensions.Value.TextDisplayFlags>) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags(_:))
- [static func textJustification(CMFormatDescription.Extensions.Value.TextJustification) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification(_:))
- [static func textRect(top: Int, left: Int, bottom: Int, right: Int) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textrect(top:left:bottom:right:))
- [static func transferFunction(CMFormatDescription.Extensions.Value.TransferFunction) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction(_:))
- [static func vendor(CMFormatDescription.Extensions.Value.Vendor) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/vendor(_:)-1uvag)
- [static func vendor(String) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/vendor(_:)-5y6sw)
- [static func yCbCrMatrix(CMFormatDescription.Extensions.Value.YCbCrMatrix) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix(_:))

###### Inspecting Extension Values

- [var propertyListRepresentation: CFPropertyList](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/propertylistrepresentation)

###### Comparing Extension Values

- [static func == (CMFormatDescription, CMFormatDescription) -> Bool](/documentation/coremedia/cmformatdescription/==(_:_:))

###### Creating Extension Values

- [init(CFPropertyList)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/init(_:))

###### Constants

- [CMFormatDescription.Extensions.Value.AlphaChannelMode](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/alphachannelmode)

###### Alpha Channel Modes

- [static let premultipliedAlpha: CMFormatDescription.Extensions.Value.AlphaChannelMode](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/alphachannelmode/premultipliedalpha)
- [static let straightAlpha: CMFormatDescription.Extensions.Value.AlphaChannelMode](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/alphachannelmode/straightalpha)
- [CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation)

###### Chroma Locations

- [static let bottom: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/bottom)
- [static let bottomLeft: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/bottomleft)
- [static let center: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/center)
- [static let dv420: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/dv420)
- [static let left: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/left)
- [static let top: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/top)
- [static let topLeft: CMFormatDescription.Extensions.Value.ChromaLocation](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/chromalocation/topleft)
- [CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries)

###### Color Primaries

- [static let dci_P3: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/dci_p3)
- [static let ebu_3213: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/ebu_3213)
- [static let itu_R_2020: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/itu_r_2020)
- [static let itu_R_709_2: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/itu_r_709_2)
- [static let p22: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/p22)
- [static let p3_D65: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/p3_d65)
- [static let smpte_C: CMFormatDescription.Extensions.Value.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/colorprimaries/smpte_c)
- [CMFormatDescription.Extensions.Value.FieldDetail](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail)

###### Field Details

- [static let spatialFirstLineEarly: CMFormatDescription.Extensions.Value.FieldDetail](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail/spatialfirstlineearly)
- [static let spatialFirstLineLate: CMFormatDescription.Extensions.Value.FieldDetail](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail/spatialfirstlinelate)
- [static let temporalBottomFirst: CMFormatDescription.Extensions.Value.FieldDetail](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail/temporalbottomfirst)
- [static let temporalTopFirst: CMFormatDescription.Extensions.Value.FieldDetail](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fielddetail/temporaltopfirst)
- [CMFormatDescription.Extensions.Value.FontFace](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fontface)

###### Font Faces

- [static let all: CMFormatDescription.Extensions.Value.FontFace](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fontface/all)
- [static let bold: CMFormatDescription.Extensions.Value.FontFace](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fontface/bold)
- [static let italic: CMFormatDescription.Extensions.Value.FontFace](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fontface/italic)
- [static let underline: CMFormatDescription.Extensions.Value.FontFace](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/fontface/underline)
- [CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile)

###### Video Profiles

- [static let hdv_1080i50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_1080i50)
- [static let hdv_1080i60: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_1080i60)
- [static let hdv_1080p24: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_1080p24)
- [static let hdv_1080p25: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_1080p25)
- [static let hdv_1080p30: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_1080p30)
- [static let hdv_720p24: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_720p24)
- [static let hdv_720p25: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_720p25)
- [static let hdv_720p30: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_720p30)
- [static let hdv_720p50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_720p50)
- [static let hdv_720p60: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/hdv_720p60)
- [static let xdcam_EX_1080i50_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_1080i50_vbr35)
- [static let xdcam_EX_1080i60_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_1080i60_vbr35)
- [static let xdcam_EX_1080p24_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_1080p24_vbr35)
- [static let xdcam_EX_1080p25_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_1080p25_vbr35)
- [static let xdcam_EX_1080p30_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_1080p30_vbr35)
- [static let xdcam_EX_720p24_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_720p24_vbr35)
- [static let xdcam_EX_720p25_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_720p25_vbr35)
- [static let xdcam_EX_720p30_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_720p30_vbr35)
- [static let xdcam_EX_720p50_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_720p50_vbr35)
- [static let xdcam_EX_720p60_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_ex_720p60_vbr35)
- [static let xdcam_HD422_1080i50_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_1080i50_cbr50)
- [static let xdcam_HD422_1080i60_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_1080i60_cbr50)
- [static let xdcam_HD422_1080p24_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_1080p24_cbr50)
- [static let xdcam_HD422_1080p25_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_1080p25_cbr50)
- [static let xdcam_HD422_1080p30_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_1080p30_cbr50)
- [static let xdcam_HD422_540p: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_540p)
- [static let xdcam_HD422_720p24_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_720p24_cbr50)
- [static let xdcam_HD422_720p25_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_720p25_cbr50)
- [static let xdcam_HD422_720p30_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_720p30_cbr50)
- [static let xdcam_HD422_720p50_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_720p50_cbr50)
- [static let xdcam_HD422_720p60_CBR50: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd422_720p60_cbr50)
- [static let xdcam_HD_1080i50_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_1080i50_vbr35)
- [static let xdcam_HD_1080i60_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_1080i60_vbr35)
- [static let xdcam_HD_1080p24_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_1080p24_vbr35)
- [static let xdcam_HD_1080p25_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_1080p25_vbr35)
- [static let xdcam_HD_1080p30_VBR35: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_1080p30_vbr35)
- [static let xdcam_HD_540p: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xdcam_hd_540p)
- [static let xf: CMFormatDescription.Extensions.Value.MPEG2VideoProfile](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/xf)

###### Initializers

- [init(rawValue: Int32)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/mpeg2videoprofile/init(rawvalue:))
- [CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags)

###### Text Display Flags

- [static let allSubtitlesForced: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/allsubtitlesforced)
- [static let continuousKaraoke: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/continuouskaraoke)
- [static let fillTextRegion: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/filltextregion)
- [static let forcedSubtitlesPresent: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/forcedsubtitlespresent)
- [static let obeySubtitleFormatting: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/obeysubtitleformatting)
- [static let scrollDirectionMask: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirectionmask)
- [static let scrollDirection_bottomToTop: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirection_bottomtotop)
- [static let scrollDirection_leftToRight: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirection_lefttoright)
- [static let scrollDirection_rightToLeft: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirection_righttoleft)
- [static let scrollDirection_topToBottom: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirection_toptobottom)
- [static let scrollIn: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrollin)
- [static let scrollOut: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrollout)
- [static let writeTextVertically: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/writetextvertically)

###### Getting the Scroll Direction

- [var scrollDirection: CMFormatDescription.Extensions.Value.TextDisplayFlags](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textdisplayflags/scrolldirection)
- [CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification)

###### Text Justifications

- [static let bottom: CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification/bottom)
- [static let centered: CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification/centered)
- [static let left: CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification/left)
- [static let right: CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification/right)
- [static let top: CMFormatDescription.Extensions.Value.TextJustification](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/textjustification/top)
- [CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction)

###### Transfer Functions

- [static let itu_R_2020: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/itu_r_2020)
- [static let itu_R_2100_HLG: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/itu_r_2100_hlg)
- [static let itu_R_709_2: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/itu_r_709_2)
- [static let linear: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/linear)
- [static let sRGB: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/srgb)
- [static let smpte_240M_1995: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/smpte_240m_1995)
- [static let smpte_ST_2084_PQ: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/smpte_st_2084_pq)
- [static let smpte_ST_428_1: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/smpte_st_428_1)
- [static let useGamma: CMFormatDescription.Extensions.Value.TransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/transferfunction/usegamma)
- [CMFormatDescription.Extensions.Value.Vendor](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/vendor)

###### Vendors

- [static let apple: CMFormatDescription.Extensions.Value.Vendor](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/vendor/apple)
- [CMFormatDescription.Extensions.Value.YCbCrMatrix](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix)

###### Color Spaces

- [static let itu_R_2020: CMFormatDescription.Extensions.Value.YCbCrMatrix](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix/itu_r_2020)
- [static let itu_R_601_4: CMFormatDescription.Extensions.Value.YCbCrMatrix](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix/itu_r_601_4)
- [static let itu_R_709_2: CMFormatDescription.Extensions.Value.YCbCrMatrix](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix/itu_r_709_2)
- [static let smpted_240M_1995: CMFormatDescription.Extensions.Value.YCbCrMatrix](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/ycbcrmatrix/smpted_240m_1995)

###### Structures

- [CMFormatDescription.Extensions.Value.ContentColorVolume](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume)

###### Structures

- [CMFormatDescription.Extensions.Value.ContentColorVolume.ColorPrimaries](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorprimaries-swift.struct)

###### Initializers

- [init(x: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorVolume, y: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorVolume)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorprimaries-swift.struct/init(x:y:))

###### Instance Properties

- [var x: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorVolume](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorprimaries-swift.struct/x)
- [var y: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorVolume](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorprimaries-swift.struct/y)
- [CMFormatDescription.Extensions.Value.ContentColorVolume.ColorVolume](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorvolume)

###### Initializers

- [init(green: Int32, blue: Int32, red: Int32)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorvolume/init(green:blue:red:))

###### Instance Properties

- [var blue: Int32](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorvolume/blue)
- [var green: Int32](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorvolume/green)
- [var red: Int32](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorvolume/red)

###### Initializers

- [init(colorPrimaries: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorPrimaries?, minimumLuminance: UInt32?, maximumLuminance: UInt32?, averageLuminance: UInt32?)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/init(colorprimaries:minimumluminance:maximumluminance:averageluminance:))

###### Instance Properties

- [var averageLuminance: UInt32?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/averageluminance)
- [var colorPrimaries: CMFormatDescription.Extensions.Value.ContentColorVolume.ColorPrimaries?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/colorprimaries-swift.property)
- [var maximumLuminance: UInt32?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/maximumluminance)
- [var minimumLuminance: UInt32?](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/contentcolorvolume/minimumluminance)
- [CMFormatDescription.Extensions.Value.HeroEye](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/heroeye)

###### Type Properties

- [static let left: CMFormatDescription.Extensions.Value.HeroEye](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/heroeye/left)
- [static let right: CMFormatDescription.Extensions.Value.HeroEye](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/heroeye/right)
- [CMFormatDescription.Extensions.Value.LogTransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/logtransferfunction)

###### Type Properties

- [static let appleLog: CMFormatDescription.Extensions.Value.LogTransferFunction](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/logtransferfunction/applelog)
- [CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind)

###### Type Properties

- [static let appleImmersiveVideo: CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind/appleimmersivevideo)
- [static let equirectangular: CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind/equirectangular)
- [static let halfEquirectangular: CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind/halfequirectangular)
- [static let parametricImmersive: CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind/parametricimmersive)
- [static let rectilinear: CMFormatDescription.Extensions.Value.ProjectionKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind/rectilinear)
- [CMFormatDescription.Extensions.Value.ViewPackingKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/viewpackingkind)

###### Type Properties

- [static let overUnder: CMFormatDescription.Extensions.Value.ViewPackingKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/viewpackingkind/overunder)
- [static let sideBySide: CMFormatDescription.Extensions.Value.ViewPackingKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/viewpackingkind/sidebyside)

###### Type Methods

- [static func cameraCalibrationDataLensCollection(CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection(_:))
- [static func heroEye(CMFormatDescription.Extensions.Value.HeroEye) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/heroeye(_:))
- [static func logTransferFunction(CMFormatDescription.Extensions.Value.LogTransferFunction) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/logtransferfunction(_:))
- [static func projectionKind(CMFormatDescription.Extensions.Value.ProjectionKind) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/projectionkind(_:))
- [static func viewPackingKind(CMFormatDescription.Extensions.Value.ViewPackingKind) -> CMFormatDescription.Extensions.Value](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/viewpackingkind(_:))

###### Enumerations

- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection)

###### Structures

- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.Calibration](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration)

###### Initializers

- [init(algorithmKind: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.AlgorithmKind, identifier: Int32, domain: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensDomain, role: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensRole, distortionCoefficients: SIMD4<Float>, xFrameAdjustmentsPolynomial: SIMD3<Float>, yFrameAdjustmentsPolynomial: SIMD3<Float>, radialAngleLimit: Float, intrinsicMatrix: simd_float3x3, intrinsicMatrixProjectionOffset: Float, intrinsicMatrixReferenceDimensions: CGSize, extrinsicOriginSource: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.ExtrinsicOriginSource, extrinsicOrientationQuaternion: SIMD3<Float>)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/init(algorithmkind:identifier:domain:role:distortioncoefficients:xframeadjustmentspolynomial:yframeadjustmentspolynomial:radialanglelimit:intrinsicmatrix:intrinsicmatrixprojectionoffset:intrinsicmatrixreferencedimensions:extrinsicoriginsour-4ejrv)

###### Instance Properties

- [var algorithmKind: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.AlgorithmKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/algorithmkind)
- [var distortionCoefficients: SIMD4<Float>](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/distortioncoefficients)
- [var domain: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensDomain](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/domain)
- [var extrinsicOrientationQuaternion: SIMD3<Float>](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/extrinsicorientationquaternion)
- [var extrinsicOriginSource: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.ExtrinsicOriginSource](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/extrinsicoriginsource)
- [var identifier: Int32](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/identifier)
- [var intrinsicMatrix: simd_float3x3](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/intrinsicmatrix)
- [var intrinsicMatrixProjectionOffset: Float](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/intrinsicmatrixprojectionoffset)
- [var intrinsicMatrixReferenceDimensions: CGSize](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/intrinsicmatrixreferencedimensions)
- [var radialAngleLimit: Float](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/radialanglelimit)
- [var role: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensRole](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/role)
- [var xFrameAdjustmentsPolynomial: SIMD3<Float>](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/xframeadjustmentspolynomial)
- [var yFrameAdjustmentsPolynomial: SIMD3<Float>](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/calibration/yframeadjustmentspolynomial)

###### Enumeration Cases

- [case mono(CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.Calibration)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/mono(_:))
- [case stereo(left: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.Calibration, right: CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.Calibration)](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/stereo(left:right:))

###### Enumerations

- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.AlgorithmKind](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/algorithmkind)

###### Enumeration Cases

- [case parametric](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/algorithmkind/parametric)
- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.ExtrinsicOriginSource](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/extrinsicoriginsource)

###### Enumeration Cases

- [case stereoCameraSystemBaseline](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/extrinsicoriginsource/stereocamerasystembaseline)
- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensDomain](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensdomain)

###### Enumeration Cases

- [case color](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensdomain/color)
- [CMFormatDescription.Extensions.Value.CameraCalibrationDataLensCollection.LensRole](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensrole)

###### Enumeration Cases

- [case left](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensrole/left)
- [case mono](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensrole/mono)
- [case right](/documentation/coremedia/cmformatdescription/extensions-swift.struct/value/cameracalibrationdatalenscollection/lensrole/right)
- [CMFormatDescription.ParameterSetCollection](/documentation/coremedia/cmformatdescription/parametersetcollection)

#### Initializers

- [init(referencing: CMFormatDescription)](/documentation/coremedia/cmformatdescription/init(referencing:))

#### Type Aliases

- [CMFormatDescription.T](/documentation/coremedia/cmformatdescription/t)
- [CMAudioFormatDescription](/documentation/coremedia/cmaudioformatdescription)
- [CMClosedCaptionFormatDescription](/documentation/coremedia/cmclosedcaptionformatdescription)
- [CMMetadataFormatDescription](/documentation/coremedia/cmmetadataformatdescription)
- [CMMuxedFormatDescription](/documentation/coremedia/cmmuxedformatdescription)
- [CMTextFormatDescription](/documentation/coremedia/cmtextformatdescription)
- [CMTimeCodeFormatDescription](/documentation/coremedia/cmtimecodeformatdescription)
- [CMVideoFormatDescription](/documentation/coremedia/cmvideoformatdescription)

### Format Description Extension Keys

- [let kCMFormatDescriptionExtension_ContentColorVolume: CFString](/documentation/coremedia/kcmformatdescriptionextension_contentcolorvolume)
- [let kCMFormatDescriptionExtension_HasAdditionalViews: CFString](/documentation/coremedia/kcmformatdescriptionextension_hasadditionalviews)
- [let kCMFormatDescriptionExtension_HasLeftStereoEyeView: CFString](/documentation/coremedia/kcmformatdescriptionextension_hasleftstereoeyeview)
- [let kCMFormatDescriptionExtension_HasRightStereoEyeView: CFString](/documentation/coremedia/kcmformatdescriptionextension_hasrightstereoeyeview)
- [let kCMFormatDescriptionExtension_HeroEye: CFString](/documentation/coremedia/kcmformatdescriptionextension_heroeye)
- [let kCMFormatDescriptionExtension_HorizontalDisparityAdjustment: CFString](/documentation/coremedia/kcmformatdescriptionextension_horizontaldisparityadjustment)
- [let kCMFormatDescriptionExtension_LogTransferFunction: CFString](/documentation/coremedia/kcmformatdescriptionextension_logtransferfunction)
- [let kCMFormatDescriptionExtension_StereoCameraBaseline: CFString](/documentation/coremedia/kcmformatdescriptionextension_stereocamerabaseline)
- [let kCMFormatDescriptionHeroEye_Left: CFString](/documentation/coremedia/kcmformatdescriptionheroeye_left)
- [let kCMFormatDescriptionHeroEye_Right: CFString](/documentation/coremedia/kcmformatdescriptionheroeye_right)

### Format Types

- [CMClosedCaptionFormatType](/documentation/coremedia/cmclosedcaptionformattype)

#### Constants

- [var kCMClosedCaptionFormatType_CEA608: CMClosedCaptionFormatType](/documentation/coremedia/kcmclosedcaptionformattype_cea608)
- [var kCMClosedCaptionFormatType_CEA708: CMClosedCaptionFormatType](/documentation/coremedia/kcmclosedcaptionformattype_cea708)
- [CMMetadataFormatType](/documentation/coremedia/cmmetadataformattype)

#### Constants

- [var kCMMetadataFormatType_ICY: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_icy)
- [var kCMMetadataFormatType_ID3: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_id3)
- [var kCMMetadataFormatType_Boxed: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_boxed)
- [var kCMMetadataFormatType_EMSG: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_emsg)
- [Metadata Format Types](/documentation/coremedia/metadata-format-types)

#### Constants

- [var kCMMetadataFormatType_Boxed: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_boxed)
- [var kCMMetadataFormatType_ICY: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_icy)
- [var kCMMetadataFormatType_ID3: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_id3)
- [var kCMMetadataFormatType_EMSG: CMMetadataFormatType](/documentation/coremedia/kcmmetadataformattype_emsg)
- [CMSubtitleFormatType](/documentation/coremedia/cmsubtitleformattype)
- [Subtitle Format Types](/documentation/coremedia/subtitle-format-types)

#### Constants

- [var kCMSubtitleFormatType_3GText: CMSubtitleFormatType](/documentation/coremedia/kcmsubtitleformattype_3gtext)
- [var kCMSubtitleFormatType_WebVTT: CMSubtitleFormatType](/documentation/coremedia/kcmsubtitleformattype_webvtt)
- [CMTimeCodeFormatType](/documentation/coremedia/cmtimecodeformattype)

#### Constants

- [var kCMTimeCodeFormatType_TimeCode32: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_timecode32)
- [var kCMTimeCodeFormatType_TimeCode64: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_timecode64)
- [var kCMTimeCodeFormatType_Counter32: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_counter32)
- [var kCMTimeCodeFormatType_Counter64: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_counter64)
- [Time Code Formats](/documentation/coremedia/time-code-formats)

#### Constants

- [var kCMTimeCodeFormatType_Counter32: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_counter32)
- [var kCMTimeCodeFormatType_Counter64: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_counter64)
- [var kCMTimeCodeFormatType_TimeCode32: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_timecode32)
- [var kCMTimeCodeFormatType_TimeCode64: CMTimeCodeFormatType](/documentation/coremedia/kcmtimecodeformattype_timecode64)
- [CMTextFormatType](/documentation/coremedia/cmtextformattype)

#### Constants

- [var kCMTextFormatType_QTText: CMTextFormatType](/documentation/coremedia/kcmtextformattype_qttext)
- [var kCMTextFormatType_3GText: CMTextFormatType](/documentation/coremedia/kcmtextformattype_3gtext)
- [CMPixelFormatType](/documentation/coremedia/cmpixelformattype)

#### Constants

- [var kCMPixelFormat_32ARGB: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_32argb)
- [var kCMPixelFormat_32BGRA: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_32bgra)
- [var kCMPixelFormat_24RGB: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_24rgb)
- [var kCMPixelFormat_16BE555: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16be555)
- [var kCMPixelFormat_16BE565: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16be565)
- [var kCMPixelFormat_16LE555: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le555)
- [var kCMPixelFormat_16LE565: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le565)
- [var kCMPixelFormat_16LE5551: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le5551)
- [var kCMPixelFormat_422YpCbCr8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr8)
- [var kCMPixelFormat_422YpCbCr8_yuvs: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr8_yuvs)
- [var kCMPixelFormat_444YpCbCr8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_444ypcbcr8)
- [var kCMPixelFormat_4444YpCbCrA8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_4444ypcbcra8)
- [var kCMPixelFormat_422YpCbCr16: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr16)
- [var kCMPixelFormat_422YpCbCr10: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr10)
- [var kCMPixelFormat_444YpCbCr10: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_444ypcbcr10)
- [var kCMPixelFormat_8IndexedGray_WhiteIsZero: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_8indexedgray_whiteiszero)
- [Tagged Buffer Group Format Types](/documentation/coremedia/tagged-buffergroup-format-types)

### Data Types

- [CMVideoDimensions](/documentation/coremedia/cmvideodimensions)

#### Creating Video Dimensions

- [init()](/documentation/coremedia/cmvideodimensions/init())
- [init(width: Int32, height: Int32)](/documentation/coremedia/cmvideodimensions/init(width:height:))

#### Inspecting Video Dimensions

- [var height: Int32](/documentation/coremedia/cmvideodimensions/height)
- [var width: Int32](/documentation/coremedia/cmvideodimensions/width)
- [CMAudioFormatDescriptionMask](/documentation/coremedia/cmaudioformatdescriptionmask)
- [CMMediaType](/documentation/coremedia/cmmediatype)

#### Constants

- [var kCMMediaType_Audio: CMMediaType](/documentation/coremedia/kcmmediatype_audio)
- [var kCMMediaType_AuxiliaryPicture: CMMediaType](/documentation/coremedia/kcmmediatype_auxiliarypicture)
- [var kCMMediaType_ClosedCaption: CMMediaType](/documentation/coremedia/kcmmediatype_closedcaption)
- [var kCMMediaType_Metadata: CMMediaType](/documentation/coremedia/kcmmediatype_metadata)
- [var kCMMediaType_Muxed: CMMediaType](/documentation/coremedia/kcmmediatype_muxed)
- [var kCMMediaType_Subtitle: CMMediaType](/documentation/coremedia/kcmmediatype_subtitle)
- [var kCMMediaType_Text: CMMediaType](/documentation/coremedia/kcmmediatype_text)
- [var kCMMediaType_TimeCode: CMMediaType](/documentation/coremedia/kcmmediatype_timecode)
- [var kCMMediaType_Video: CMMediaType](/documentation/coremedia/kcmmediatype_video)
- [var kCMMediaType_TaggedBufferGroup: CMMediaType](/documentation/coremedia/kcmmediatype_taggedbuffergroup)
- [CMAudioCodecType](/documentation/coremedia/cmaudiocodectype)

#### Constants

- [var kCMAudioCodecType_AAC_LCProtected: CMAudioCodecType](/documentation/coremedia/kcmaudiocodectype_aac_lcprotected)
- [var kCMAudioCodecType_AAC_AudibleProtected: CMAudioCodecType](/documentation/coremedia/kcmaudiocodectype_aac_audibleprotected)
- [CMVideoCodecType](/documentation/coremedia/cmvideocodectype)

#### null

- [var kCMVideoCodecType_422YpCbCr8: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_422ypcbcr8)
- [var kCMVideoCodecType_422YpCbCr8: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_422ypcbcr8)
- [var kCMVideoCodecType_Animation: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_animation)
- [var kCMVideoCodecType_Animation: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_animation)
- [var kCMVideoCodecType_AppleProRes422: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422)
- [var kCMVideoCodecType_AppleProRes422HQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422hq)
- [var kCMVideoCodecType_AppleProRes422LT: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422lt)
- [var kCMVideoCodecType_AppleProRes422Proxy: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422proxy)
- [var kCMVideoCodecType_AppleProRes4444: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores4444)
- [var kCMVideoCodecType_AppleProRes4444XQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores4444xq)
- [var kCMVideoCodecType_AppleProResRAW: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleproresraw)
- [var kCMVideoCodecType_AppleProResRAWHQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleproresrawhq)
- [var kCMVideoCodecType_AV1: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_av1)
- [var kCMVideoCodecType_Cinepak: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_cinepak)
- [var kCMVideoCodecType_Cinepak: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_cinepak)
- [var kCMVideoCodecType_DepthHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_depthhevc)
- [var kCMVideoCodecType_DisparityHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_disparityhevc)
- [var kCMVideoCodecType_DolbyVisionHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dolbyvisionhevc)
- [var kCMVideoCodecType_DVCNTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcntsc)
- [var kCMVideoCodecType_DVCNTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcntsc)
- [var kCMVideoCodecType_DVCPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpal)
- [var kCMVideoCodecType_DVCPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpal)
- [var kCMVideoCodecType_DVCPro50NTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50ntsc)
- [var kCMVideoCodecType_DVCPro50NTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50ntsc)
- [var kCMVideoCodecType_DVCPro50PAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50pal)
- [var kCMVideoCodecType_DVCPro50PAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50pal)
- [var kCMVideoCodecType_DVCPROHD1080i50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i50)
- [var kCMVideoCodecType_DVCPROHD1080i50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i50)
- [var kCMVideoCodecType_DVCPROHD1080i60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i60)
- [var kCMVideoCodecType_DVCPROHD1080i60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i60)
- [var kCMVideoCodecType_DVCPROHD1080p25: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p25)
- [var kCMVideoCodecType_DVCPROHD1080p25: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p25)
- [var kCMVideoCodecType_DVCPROHD1080p30: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p30)
- [var kCMVideoCodecType_DVCPROHD1080p30: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p30)
- [var kCMVideoCodecType_DVCPROHD720p50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p50)
- [var kCMVideoCodecType_DVCPROHD720p50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p50)
- [var kCMVideoCodecType_DVCPROHD720p60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p60)
- [var kCMVideoCodecType_DVCPROHD720p60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p60)
- [var kCMVideoCodecType_DVCProPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpropal)
- [var kCMVideoCodecType_DVCProPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpropal)
- [var kCMVideoCodecType_H263: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h263)
- [var kCMVideoCodecType_H263: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h263)
- [var kCMVideoCodecType_H264: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h264)
- [var kCMVideoCodecType_H264: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h264)
- [var kCMVideoCodecType_HEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_hevc)
- [var kCMVideoCodecType_HEVCWithAlpha: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_hevcwithalpha)
- [var kCMVideoCodecType_JPEG_OpenDML: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_opendml)
- [var kCMVideoCodecType_JPEG_OpenDML: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_opendml)
- [var kCMVideoCodecType_JPEG_XL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_xl)
- [var kCMVideoCodecType_JPEG: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg)
- [var kCMVideoCodecType_JPEG: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg)
- [var kCMVideoCodecType_MPEG1Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg1video)
- [var kCMVideoCodecType_MPEG1Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg1video)
- [var kCMVideoCodecType_MPEG2Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg2video)
- [var kCMVideoCodecType_MPEG2Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg2video)
- [var kCMVideoCodecType_MPEG4Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg4video)
- [var kCMVideoCodecType_MPEG4Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg4video)
- [var kCMVideoCodecType_SorensonVideo3: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo3)
- [var kCMVideoCodecType_SorensonVideo3: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo3)
- [var kCMVideoCodecType_SorensonVideo: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo)
- [var kCMVideoCodecType_SorensonVideo: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo)
- [var kCMVideoCodecType_VP9: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_vp9)
- [CMTextDisplayFlags](/documentation/coremedia/cmtextdisplayflags)

#### Constants

- [var kCMTextDisplayFlag_scrollIn: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrollin)
- [var kCMTextDisplayFlag_scrollOut: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrollout)
- [var kCMTextDisplayFlag_scrollDirectionMask: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirectionmask)
- [var kCMTextDisplayFlag_scrollDirection_bottomToTop: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_bottomtotop)
- [var kCMTextDisplayFlag_scrollDirection_rightToLeft: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_righttoleft)
- [var kCMTextDisplayFlag_scrollDirection_topToBottom: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_toptobottom)
- [var kCMTextDisplayFlag_scrollDirection_leftToRight: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_lefttoright)
- [var kCMTextDisplayFlag_continuousKaraoke: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_continuouskaraoke)
- [var kCMTextDisplayFlag_writeTextVertically: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_writetextvertically)
- [var kCMTextDisplayFlag_fillTextRegion: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_filltextregion)
- [var kCMTextDisplayFlag_forcedSubtitlesPresent: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_forcedsubtitlespresent)
- [var kCMTextDisplayFlag_allSubtitlesForced: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_allsubtitlesforced)
- [CMTextJustificationValue](/documentation/coremedia/cmtextjustificationvalue)

#### Constants

- [var kCMTextJustification_left_top: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_left_top)
- [var kCMTextJustification_centered: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_centered)
- [var kCMTextJustification_bottom_right: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_bottom_right)
- [Media Type Constants](/documentation/coremedia/media-type-constants)

#### Constants

- [var kCMMediaType_Audio: CMMediaType](/documentation/coremedia/kcmmediatype_audio)
- [var kCMMediaType_AuxiliaryPicture: CMMediaType](/documentation/coremedia/kcmmediatype_auxiliarypicture)
- [var kCMMediaType_ClosedCaption: CMMediaType](/documentation/coremedia/kcmmediatype_closedcaption)
- [var kCMMediaType_Metadata: CMMediaType](/documentation/coremedia/kcmmediatype_metadata)
- [var kCMMediaType_Muxed: CMMediaType](/documentation/coremedia/kcmmediatype_muxed)
- [var kCMMediaType_Subtitle: CMMediaType](/documentation/coremedia/kcmmediatype_subtitle)
- [var kCMMediaType_Text: CMMediaType](/documentation/coremedia/kcmmediatype_text)
- [var kCMMediaType_TimeCode: CMMediaType](/documentation/coremedia/kcmmediatype_timecode)
- [var kCMMediaType_Video: CMMediaType](/documentation/coremedia/kcmmediatype_video)
- [var kCMMediaType_TaggedBufferGroup: CMMediaType](/documentation/coremedia/kcmmediatype_taggedbuffergroup)
- [Muxed Stream Types](/documentation/coremedia/muxed-stream-types)

#### Constants

- [var kCMMuxedStreamType_DV: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_dv)
- [var kCMMuxedStreamType_MPEG1System: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg1system)
- [var kCMMuxedStreamType_MPEG2Program: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg2program)
- [var kCMMuxedStreamType_MPEG2Transport: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_mpeg2transport)
- [var kCMMuxedStreamType_EmbeddedDeviceScreenRecording: CMMuxedStreamType](/documentation/coremedia/kcmmuxedstreamtype_embeddeddevicescreenrecording)
- [Audio Codec Types](/documentation/coremedia/audio-codec-types)

#### Constants

- [var kCMAudioCodecType_AAC_AudibleProtected: CMAudioCodecType](/documentation/coremedia/kcmaudiocodectype_aac_audibleprotected)
- [var kCMAudioCodecType_AAC_LCProtected: CMAudioCodecType](/documentation/coremedia/kcmaudiocodectype_aac_lcprotected)

### Constants

- [Audio Format Description Mask Codes](/documentation/coremedia/audio-format-desc-codes)

#### Constants

- [var kCMAudioFormatDescriptionMask_All: CMAudioFormatDescriptionMask](/documentation/coremedia/kcmaudioformatdescriptionmask_all)
- [var kCMAudioFormatDescriptionMask_ChannelLayout: CMAudioFormatDescriptionMask](/documentation/coremedia/kcmaudioformatdescriptionmask_channellayout)
- [var kCMAudioFormatDescriptionMask_Extensions: CMAudioFormatDescriptionMask](/documentation/coremedia/kcmaudioformatdescriptionmask_extensions)
- [var kCMAudioFormatDescriptionMask_MagicCookie: CMAudioFormatDescriptionMask](/documentation/coremedia/kcmaudioformatdescriptionmask_magiccookie)
- [var kCMAudioFormatDescriptionMask_StreamBasicDescription: CMAudioFormatDescriptionMask](/documentation/coremedia/kcmaudioformatdescriptionmask_streambasicdescription)
- [Chroma Location Extension Constants](/documentation/coremedia/chroma-location-extension-constants)

#### Constants

- [let kCMFormatDescriptionChromaLocation_Bottom: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_bottom-swift.var)
- [let kCMFormatDescriptionChromaLocation_BottomLeft: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_bottomleft-swift.var)
- [let kCMFormatDescriptionChromaLocation_Center: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_center-swift.var)
- [let kCMFormatDescriptionChromaLocation_DV420: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_dv420-swift.var)
- [let kCMFormatDescriptionChromaLocation_Left: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_left-swift.var)
- [let kCMFormatDescriptionChromaLocation_Top: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_top-swift.var)
- [let kCMFormatDescriptionChromaLocation_TopLeft: CFString](/documentation/coremedia/kcmformatdescriptionchromalocation_topleft-swift.var)
- [Clean Aperture Extension Constants](/documentation/coremedia/clean-aperture-extension-constants)

#### Constants

- [let kCMFormatDescriptionKey_CleanApertureHeight: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanapertureheight-swift.var)
- [let kCMFormatDescriptionKey_CleanApertureHeightRational: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanapertureheightrational)
- [let kCMFormatDescriptionKey_CleanApertureHorizontalOffset: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanaperturehorizontaloffset-swift.var)
- [let kCMFormatDescriptionKey_CleanApertureHorizontalOffsetRational: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanaperturehorizontaloffsetrational)
- [let kCMFormatDescriptionKey_CleanApertureVerticalOffset: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanapertureverticaloffset-swift.var)
- [let kCMFormatDescriptionKey_CleanApertureVerticalOffsetRational: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanapertureverticaloffsetrational)
- [let kCMFormatDescriptionKey_CleanApertureWidth: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanaperturewidth-swift.var)
- [let kCMFormatDescriptionKey_CleanApertureWidthRational: CFString](/documentation/coremedia/kcmformatdescriptionkey_cleanaperturewidthrational)
- [Closed Caption Format Type Constants](/documentation/coremedia/closed-caption-formats)

#### Constants

- [var kCMClosedCaptionFormatType_ATSC: CMClosedCaptionFormatType](/documentation/coremedia/kcmclosedcaptionformattype_atsc)
- [var kCMClosedCaptionFormatType_CEA608: CMClosedCaptionFormatType](/documentation/coremedia/kcmclosedcaptionformattype_cea608)
- [var kCMClosedCaptionFormatType_CEA708: CMClosedCaptionFormatType](/documentation/coremedia/kcmclosedcaptionformattype_cea708)
- [Color Primary Extension Constants](/documentation/coremedia/color-primary-extension-constants)

#### Constants

- [let kCMFormatDescriptionColorPrimaries_DCI_P3: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_dci_p3)
- [let kCMFormatDescriptionColorPrimaries_EBU_3213: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_ebu_3213-swift.var)
- [let kCMFormatDescriptionColorPrimaries_ITU_R_2020: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_itu_r_2020)
- [let kCMFormatDescriptionColorPrimaries_ITU_R_709_2: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_itu_r_709_2-swift.var)
- [let kCMFormatDescriptionColorPrimaries_P22: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_p22)
- [let kCMFormatDescriptionColorPrimaries_P3_D65: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_p3_d65)
- [let kCMFormatDescriptionColorPrimaries_SMPTE_C: CFString](/documentation/coremedia/kcmformatdescriptioncolorprimaries_smpte_c-swift.var)
- [Field Detail Extension Constants](/documentation/coremedia/field-detail-extension-constants)

#### Constants

- [let kCMFormatDescriptionFieldDetail_SpatialFirstLineEarly: CFString](/documentation/coremedia/kcmformatdescriptionfielddetail_spatialfirstlineearly-swift.var)
- [let kCMFormatDescriptionFieldDetail_SpatialFirstLineLate: CFString](/documentation/coremedia/kcmformatdescriptionfielddetail_spatialfirstlinelate-swift.var)
- [let kCMFormatDescriptionFieldDetail_TemporalTopFirst: CFString](/documentation/coremedia/kcmformatdescriptionfielddetail_temporaltopfirst-swift.var)
- [let kCMFormatDescriptionFieldDetail_TemporalBottomFirst: CFString](/documentation/coremedia/kcmformatdescriptionfielddetail_temporalbottomfirst-swift.var)
- [Format Description Bridge Error Codes](/documentation/coremedia/format-description-bridge-errors)

#### Constants

- [var kCMFormatDescriptionBridgeError_InvalidParameter: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_invalidparameter)
- [var kCMFormatDescriptionBridgeError_AllocationFailed: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_allocationfailed)
- [var kCMFormatDescriptionBridgeError_IncompatibleFormatDescription: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_incompatibleformatdescription)
- [var kCMFormatDescriptionBridgeError_InvalidFormatDescription: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_invalidformatdescription)
- [var kCMFormatDescriptionBridgeError_InvalidSerializedSampleDescription: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_invalidserializedsampledescription)
- [var kCMFormatDescriptionBridgeError_InvalidSlice: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_invalidslice)
- [var kCMFormatDescriptionBridgeError_UnsupportedSampleDescriptionFlavor: OSStatus](/documentation/coremedia/kcmformatdescriptionbridgeerror_unsupportedsampledescriptionflavor)
- [Format Description Constants](/documentation/coremedia/format-description-constants)

#### Description Constants

- [let kCMFormatDescriptionAlphaChannelMode_PremultipliedAlpha: CFString](/documentation/coremedia/kcmformatdescriptionalphachannelmode_premultipliedalpha)
- [let kCMFormatDescriptionAlphaChannelMode_StraightAlpha: CFString](/documentation/coremedia/kcmformatdescriptionalphachannelmode_straightalpha)
- [let kCMFormatDescriptionTransferFunction_ITU_R_2100_HLG: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_itu_r_2100_hlg)
- [let kCMFormatDescriptionTransferFunction_Linear: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_linear)
- [let kCMFormatDescriptionTransferFunction_SMPTE_ST_2084_PQ: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_smpte_st_2084_pq)
- [let kCMFormatDescriptionTransferFunction_sRGB: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_srgb)

#### Description Extension Keys

- [let kCMFormatDescriptionExtensionKey_MetadataKeyTable: CFString](/documentation/coremedia/kcmformatdescriptionextensionkey_metadatakeytable)

#### Description Extension Constants

- [let kCMFormatDescriptionExtension_AlphaChannelMode: CFString](/documentation/coremedia/kcmformatdescriptionextension_alphachannelmode)
- [let kCMFormatDescriptionExtension_AlternativeTransferCharacteristics: CFString](/documentation/coremedia/kcmformatdescriptionextension_alternativetransfercharacteristics)
- [let kCMFormatDescriptionExtension_AmbientViewingEnvironment: CFString](/documentation/coremedia/kcmformatdescriptionextension_ambientviewingenvironment)
- [let kCMFormatDescriptionExtension_AuxiliaryTypeInfo: CFString](/documentation/coremedia/kcmformatdescriptionextension_auxiliarytypeinfo)
- [let kCMFormatDescriptionExtension_BitsPerComponent: CFString](/documentation/coremedia/kcmformatdescriptionextension_bitspercomponent)
- [let kCMFormatDescriptionExtension_BytesPerRow: CFString](/documentation/coremedia/kcmformatdescriptionextension_bytesperrow)
- [let kCMFormatDescriptionExtension_ChromaLocationBottomField: CFString](/documentation/coremedia/kcmformatdescriptionextension_chromalocationbottomfield-swift.var)
- [let kCMFormatDescriptionExtension_ChromaLocationTopField: CFString](/documentation/coremedia/kcmformatdescriptionextension_chromalocationtopfield-swift.var)
- [let kCMFormatDescriptionExtension_CleanAperture: CFString](/documentation/coremedia/kcmformatdescriptionextension_cleanaperture-swift.var)
- [let kCMFormatDescriptionExtension_ColorPrimaries: CFString](/documentation/coremedia/kcmformatdescriptionextension_colorprimaries-swift.var)
- [let kCMFormatDescriptionExtension_ContainsAlphaChannel: CFString](/documentation/coremedia/kcmformatdescriptionextension_containsalphachannel)
- [let kCMFormatDescriptionExtension_ContentLightLevelInfo: CFString](/documentation/coremedia/kcmformatdescriptionextension_contentlightlevelinfo)
- [let kCMFormatDescriptionExtension_Depth: CFString](/documentation/coremedia/kcmformatdescriptionextension_depth)
- [let kCMFormatDescriptionExtension_FieldCount: CFString](/documentation/coremedia/kcmformatdescriptionextension_fieldcount-swift.var)
- [let kCMFormatDescriptionExtension_FieldDetail: CFString](/documentation/coremedia/kcmformatdescriptionextension_fielddetail-swift.var)
- [let kCMFormatDescriptionExtension_FormatName: CFString](/documentation/coremedia/kcmformatdescriptionextension_formatname)
- [let kCMFormatDescriptionExtension_FullRangeVideo: CFString](/documentation/coremedia/kcmformatdescriptionextension_fullrangevideo)
- [let kCMFormatDescriptionExtension_GammaLevel: CFString](/documentation/coremedia/kcmformatdescriptionextension_gammalevel-swift.var)
- [let kCMFormatDescriptionExtension_HorizontalFieldOfView: CFString](/documentation/coremedia/kcmformatdescriptionextension_horizontalfieldofview)
- [let kCMFormatDescriptionExtension_ICCProfile: CFString](/documentation/coremedia/kcmformatdescriptionextension_iccprofile)
- [let kCMFormatDescriptionExtension_MasteringDisplayColorVolume: CFString](/documentation/coremedia/kcmformatdescriptionextension_masteringdisplaycolorvolume)
- [let kCMFormatDescriptionExtension_OriginalCompressionSettings: CFString](/documentation/coremedia/kcmformatdescriptionextension_originalcompressionsettings)
- [let kCMFormatDescriptionExtension_PixelAspectRatio: CFString](/documentation/coremedia/kcmformatdescriptionextension_pixelaspectratio-swift.var)
- [let kCMFormatDescriptionExtension_ProtectedContentOriginalFormat: CFString](/documentation/coremedia/kcmformatdescriptionextension_protectedcontentoriginalformat)
- [let kCMFormatDescriptionExtension_SampleDescriptionExtensionAtoms: CFString](/documentation/coremedia/kcmformatdescriptionextension_sampledescriptionextensionatoms)
- [let kCMFormatDescriptionExtension_TransferFunction: CFString](/documentation/coremedia/kcmformatdescriptionextension_transferfunction-swift.var)
- [let kCMFormatDescriptionExtension_VerbatimISOSampleEntry: CFString](/documentation/coremedia/kcmformatdescriptionextension_verbatimisosampleentry)
- [let kCMFormatDescriptionExtension_VerbatimImageDescription: CFString](/documentation/coremedia/kcmformatdescriptionextension_verbatimimagedescription-swift.var)
- [let kCMFormatDescriptionExtension_VerbatimSampleDescription: CFString](/documentation/coremedia/kcmformatdescriptionextension_verbatimsampledescription)
- [let kCMFormatDescriptionExtension_YCbCrMatrix: CFString](/documentation/coremedia/kcmformatdescriptionextension_ycbcrmatrix-swift.var)
- [Format Description Error Codes](/documentation/coremedia/format-description-errors)

#### Constants

- [var kCMFormatDescriptionError_InvalidParameter: OSStatus](/documentation/coremedia/kcmformatdescriptionerror_invalidparameter)
- [var kCMFormatDescriptionError_AllocationFailed: OSStatus](/documentation/coremedia/kcmformatdescriptionerror_allocationfailed)
- [var kCMFormatDescriptionError_ValueNotAvailable: OSStatus](/documentation/coremedia/kcmformatdescriptionerror_valuenotavailable)
- [HEVC Temporal Level Info Constants](/documentation/coremedia/hevc-temporal-level-info-constants)

#### Constants

- [let kCMHEVCTemporalLevelInfoKey_ConstraintIndicatorFlags: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_constraintindicatorflags)
- [let kCMHEVCTemporalLevelInfoKey_LevelIndex: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_levelindex)
- [let kCMHEVCTemporalLevelInfoKey_ProfileCompatibilityFlags: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_profilecompatibilityflags)
- [let kCMHEVCTemporalLevelInfoKey_ProfileIndex: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_profileindex)
- [let kCMHEVCTemporalLevelInfoKey_ProfileSpace: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_profilespace)
- [let kCMHEVCTemporalLevelInfoKey_TemporalLevel: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_temporallevel)
- [let kCMHEVCTemporalLevelInfoKey_TierFlag: CFString](/documentation/coremedia/kcmhevctemporallevelinfokey_tierflag)
- [Metadata Format Description Constants](/documentation/coremedia/metadata-format-description-constants)

#### Constants

- [let kCMMetadataBaseDataType_AffineTransformF64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_affinetransformf64)
- [let kCMMetadataFormatDescriptionKey_ConformingDataTypes: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_conformingdatatypes)
- [let kCMMetadataFormatDescriptionKey_DataType: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_datatype)
- [let kCMMetadataFormatDescriptionKey_DataTypeNamespace: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_datatypenamespace)
- [let kCMMetadataFormatDescriptionKey_LanguageTag: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_languagetag)
- [let kCMMetadataFormatDescriptionKey_LocalID: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_localid)
- [let kCMMetadataFormatDescriptionKey_Namespace: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_namespace)
- [let kCMMetadataFormatDescriptionKey_SetupData: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_setupdata)
- [let kCMMetadataFormatDescriptionKey_StructuralDependency: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_structuraldependency)
- [let kCMMetadataFormatDescriptionKey_Value: CFString](/documentation/coremedia/kcmmetadataformatdescriptionkey_value)
- [let kCMMetadataFormatDescriptionMetadataSpecificationKey_DataType: CFString](/documentation/coremedia/kcmmetadataformatdescriptionmetadataspecificationkey_datatype)
- [let kCMMetadataFormatDescriptionMetadataSpecificationKey_ExtendedLanguageTag: CFString](/documentation/coremedia/kcmmetadataformatdescriptionmetadataspecificationkey_extendedlanguagetag)
- [let kCMMetadataFormatDescriptionMetadataSpecificationKey_Identifier: CFString](/documentation/coremedia/kcmmetadataformatdescriptionmetadataspecificationkey_identifier)
- [let kCMMetadataFormatDescriptionMetadataSpecificationKey_SetupData: CFString](/documentation/coremedia/kcmmetadataformatdescriptionmetadataspecificationkey_setupdata)
- [let kCMMetadataFormatDescriptionMetadataSpecificationKey_StructuralDependency: CFString](/documentation/coremedia/kcmmetadataformatdescriptionmetadataspecificationkey_structuraldependency)
- [let kCMMetadataFormatDescription_StructuralDependencyKey_DependencyIsInvalidFlag: CFString](/documentation/coremedia/kcmmetadataformatdescription_structuraldependencykey_dependencyisinvalidflag)
- [MPEG-2-conformant Formats](/documentation/coremedia/mpeg-2-conformant-formats)

#### Constants

- [let kCMFormatDescriptionConformsToMPEG2VideoProfile: CFString](/documentation/coremedia/kcmformatdescriptionconformstompeg2videoprofile)
- [let kCMFormatDescriptionExtension_TemporalQuality: CFString](/documentation/coremedia/kcmformatdescriptionextension_temporalquality)
- [let kCMFormatDescriptionExtension_SpatialQuality: CFString](/documentation/coremedia/kcmformatdescriptionextension_spatialquality)
- [let kCMFormatDescriptionExtension_Version: CFString](/documentation/coremedia/kcmformatdescriptionextension_version)
- [let kCMFormatDescriptionExtension_RevisionLevel: CFString](/documentation/coremedia/kcmformatdescriptionextension_revisionlevel)
- [let kCMFormatDescriptionExtension_Vendor: CFString](/documentation/coremedia/kcmformatdescriptionextension_vendor)
- [let kCMFormatDescriptionVendor_Apple: CFString](/documentation/coremedia/kcmformatdescriptionvendor_apple)
- [Pixel Aspect Ratio Extension Constants](/documentation/coremedia/pixel-aspect-ratio-extension-constants)

#### Constants

- [let kCMFormatDescriptionKey_PixelAspectRatioHorizontalSpacing: CFString](/documentation/coremedia/kcmformatdescriptionkey_pixelaspectratiohorizontalspacing-swift.var)
- [let kCMFormatDescriptionKey_PixelAspectRatioVerticalSpacing: CFString](/documentation/coremedia/kcmformatdescriptionkey_pixelaspectratioverticalspacing-swift.var)
- [Text Display Flags](/documentation/coremedia/text-display-flags)

#### Constants

- [var kCMTextDisplayFlag_allSubtitlesForced: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_allsubtitlesforced)
- [var kCMTextDisplayFlag_continuousKaraoke: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_continuouskaraoke)
- [var kCMTextDisplayFlag_fillTextRegion: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_filltextregion)
- [var kCMTextDisplayFlag_forcedSubtitlesPresent: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_forcedsubtitlespresent)
- [var kCMTextDisplayFlag_obeySubtitleFormatting: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_obeysubtitleformatting)
- [var kCMTextDisplayFlag_scrollDirectionMask: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirectionmask)
- [var kCMTextDisplayFlag_scrollDirection_bottomToTop: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_bottomtotop)
- [var kCMTextDisplayFlag_scrollDirection_leftToRight: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_lefttoright)
- [var kCMTextDisplayFlag_scrollDirection_rightToLeft: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_righttoleft)
- [var kCMTextDisplayFlag_scrollDirection_topToBottom: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrolldirection_toptobottom)
- [var kCMTextDisplayFlag_scrollIn: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrollin)
- [var kCMTextDisplayFlag_scrollOut: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_scrollout)
- [var kCMTextDisplayFlag_writeTextVertically: CMTextDisplayFlags](/documentation/coremedia/kcmtextdisplayflag_writetextvertically)
- [Text Format Constants](/documentation/coremedia/text-format-constants)

#### Constants

- [var kCMTextFormatType_3GText: CMTextFormatType](/documentation/coremedia/kcmtextformattype_3gtext)
- [var kCMTextFormatType_QTText: CMTextFormatType](/documentation/coremedia/kcmtextformattype_qttext)
- [Text Format Description Constants](/documentation/coremedia/text-format-description-constants)

#### Description Constants

- [let kCMTextFormatDescriptionColor_Red: CFString](/documentation/coremedia/kcmtextformatdescriptioncolor_red)
- [let kCMTextFormatDescriptionColor_Green: CFString](/documentation/coremedia/kcmtextformatdescriptioncolor_green)
- [let kCMTextFormatDescriptionColor_Blue: CFString](/documentation/coremedia/kcmtextformatdescriptioncolor_blue)
- [let kCMTextFormatDescriptionColor_Alpha: CFString](/documentation/coremedia/kcmtextformatdescriptioncolor_alpha)
- [let kCMTextFormatDescriptionRect_Top: CFString](/documentation/coremedia/kcmtextformatdescriptionrect_top)
- [let kCMTextFormatDescriptionRect_Left: CFString](/documentation/coremedia/kcmtextformatdescriptionrect_left)
- [let kCMTextFormatDescriptionRect_Bottom: CFString](/documentation/coremedia/kcmtextformatdescriptionrect_bottom)
- [let kCMTextFormatDescriptionRect_Right: CFString](/documentation/coremedia/kcmtextformatdescriptionrect_right)
- [let kCMTextFormatDescriptionStyle_StartChar: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_startchar)
- [let kCMTextFormatDescriptionStyle_Font: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_font)
- [let kCMTextFormatDescriptionStyle_FontFace: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_fontface)
- [let kCMTextFormatDescriptionStyle_ForegroundColor: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_foregroundcolor)
- [let kCMTextFormatDescriptionStyle_EndChar: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_endchar)
- [let kCMTextFormatDescriptionStyle_Height: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_height)
- [let kCMTextFormatDescriptionStyle_Ascent: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_ascent)
- [let kCMTextFormatDescriptionStyle_FontSize: CFString](/documentation/coremedia/kcmtextformatdescriptionstyle_fontsize)

#### Description Extension Constants

- [let kCMTextFormatDescriptionExtension_DisplayFlags: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_displayflags)
- [let kCMTextFormatDescriptionExtension_BackgroundColor: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_backgroundcolor)
- [let kCMTextFormatDescriptionExtension_DefaultTextBox: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_defaulttextbox)
- [let kCMTextFormatDescriptionExtension_DefaultStyle: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_defaultstyle)
- [let kCMTextFormatDescriptionExtension_HorizontalJustification: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_horizontaljustification)
- [let kCMTextFormatDescriptionExtension_VerticalJustification: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_verticaljustification)
- [let kCMTextFormatDescriptionExtension_FontTable: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_fonttable)
- [let kCMTextFormatDescriptionExtension_TextJustification: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_textjustification)
- [let kCMTextFormatDescriptionExtension_DefaultFontName: CFString](/documentation/coremedia/kcmtextformatdescriptionextension_defaultfontname)
- [Text Justification Constants](/documentation/coremedia/text-justification-constants)

#### Constants

- [var kCMTextJustification_bottom_right: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_bottom_right)
- [var kCMTextJustification_centered: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_centered)
- [var kCMTextJustification_left_top: CMTextJustificationValue](/documentation/coremedia/kcmtextjustification_left_top)
- [Time Code Flags](/documentation/coremedia/time-code-flags)

#### Constants

- [var kCMTimeCodeFlag_DropFrame: UInt32](/documentation/coremedia/kcmtimecodeflag_dropframe)
- [var kCMTimeCodeFlag_24HourMax: UInt32](/documentation/coremedia/kcmtimecodeflag_24hourmax)
- [var kCMTimeCodeFlag_NegTimesOK: UInt32](/documentation/coremedia/kcmtimecodeflag_negtimesok)
- [Time Code Format Description Constants](/documentation/coremedia/time-code-format-description-constants)

#### Constants

- [let kCMTimeCodeFormatDescriptionKey_LangCode: CFString](/documentation/coremedia/kcmtimecodeformatdescriptionkey_langcode)
- [let kCMTimeCodeFormatDescriptionKey_Value: CFString](/documentation/coremedia/kcmtimecodeformatdescriptionkey_value)
- [let kCMTimeCodeFormatDescriptionExtension_SourceReferenceName: CFString](/documentation/coremedia/kcmtimecodeformatdescriptionextension_sourcereferencename)
- [Transfer Function Extension Constants](/documentation/coremedia/transfer-function-extension-constants)

#### Constants

- [let kCMFormatDescriptionTransferFunction_ITU_R_2020: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_itu_r_2020)
- [let kCMFormatDescriptionTransferFunction_ITU_R_709_2: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_itu_r_709_2-swift.var)
- [let kCMFormatDescriptionTransferFunction_SMPTE_240M_1995: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_smpte_240m_1995-swift.var)
- [let kCMFormatDescriptionTransferFunction_SMPTE_ST_428_1: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_smpte_st_428_1)
- [let kCMFormatDescriptionTransferFunction_UseGamma: CFString](/documentation/coremedia/kcmformatdescriptiontransferfunction_usegamma-swift.var)
- [Video Codec Constants](/documentation/coremedia/video-codec-constants)

#### Constants

- [var kCMVideoCodecType_422YpCbCr8: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_422ypcbcr8)
- [var kCMVideoCodecType_422YpCbCr8: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_422ypcbcr8)
- [var kCMVideoCodecType_Animation: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_animation)
- [var kCMVideoCodecType_Animation: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_animation)
- [var kCMVideoCodecType_AppleProRes422: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422)
- [var kCMVideoCodecType_AppleProRes422HQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422hq)
- [var kCMVideoCodecType_AppleProRes422LT: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422lt)
- [var kCMVideoCodecType_AppleProRes422Proxy: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores422proxy)
- [var kCMVideoCodecType_AppleProRes4444: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores4444)
- [var kCMVideoCodecType_AppleProRes4444XQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleprores4444xq)
- [var kCMVideoCodecType_AppleProResRAW: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleproresraw)
- [var kCMVideoCodecType_AppleProResRAWHQ: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_appleproresrawhq)
- [var kCMVideoCodecType_AV1: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_av1)
- [var kCMVideoCodecType_Cinepak: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_cinepak)
- [var kCMVideoCodecType_Cinepak: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_cinepak)
- [var kCMVideoCodecType_DepthHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_depthhevc)
- [var kCMVideoCodecType_DisparityHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_disparityhevc)
- [var kCMVideoCodecType_DolbyVisionHEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dolbyvisionhevc)
- [var kCMVideoCodecType_DVCNTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcntsc)
- [var kCMVideoCodecType_DVCNTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcntsc)
- [var kCMVideoCodecType_DVCPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpal)
- [var kCMVideoCodecType_DVCPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpal)
- [var kCMVideoCodecType_DVCPro50NTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50ntsc)
- [var kCMVideoCodecType_DVCPro50NTSC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50ntsc)
- [var kCMVideoCodecType_DVCPro50PAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50pal)
- [var kCMVideoCodecType_DVCPro50PAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpro50pal)
- [var kCMVideoCodecType_DVCPROHD1080i50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i50)
- [var kCMVideoCodecType_DVCPROHD1080i50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i50)
- [var kCMVideoCodecType_DVCPROHD1080i60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i60)
- [var kCMVideoCodecType_DVCPROHD1080i60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080i60)
- [var kCMVideoCodecType_DVCPROHD1080p25: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p25)
- [var kCMVideoCodecType_DVCPROHD1080p25: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p25)
- [var kCMVideoCodecType_DVCPROHD1080p30: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p30)
- [var kCMVideoCodecType_DVCPROHD1080p30: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd1080p30)
- [var kCMVideoCodecType_DVCPROHD720p50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p50)
- [var kCMVideoCodecType_DVCPROHD720p50: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p50)
- [var kCMVideoCodecType_DVCPROHD720p60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p60)
- [var kCMVideoCodecType_DVCPROHD720p60: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcprohd720p60)
- [var kCMVideoCodecType_DVCProPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpropal)
- [var kCMVideoCodecType_DVCProPAL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_dvcpropal)
- [var kCMVideoCodecType_H263: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h263)
- [var kCMVideoCodecType_H263: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h263)
- [var kCMVideoCodecType_H264: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h264)
- [var kCMVideoCodecType_H264: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_h264)
- [var kCMVideoCodecType_HEVC: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_hevc)
- [var kCMVideoCodecType_HEVCWithAlpha: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_hevcwithalpha)
- [var kCMVideoCodecType_JPEG_OpenDML: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_opendml)
- [var kCMVideoCodecType_JPEG_OpenDML: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_opendml)
- [var kCMVideoCodecType_JPEG_XL: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg_xl)
- [var kCMVideoCodecType_JPEG: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg)
- [var kCMVideoCodecType_JPEG: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_jpeg)
- [var kCMVideoCodecType_MPEG1Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg1video)
- [var kCMVideoCodecType_MPEG1Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg1video)
- [var kCMVideoCodecType_MPEG2Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg2video)
- [var kCMVideoCodecType_MPEG2Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg2video)
- [var kCMVideoCodecType_MPEG4Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg4video)
- [var kCMVideoCodecType_MPEG4Video: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_mpeg4video)
- [var kCMVideoCodecType_SorensonVideo3: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo3)
- [var kCMVideoCodecType_SorensonVideo3: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo3)
- [var kCMVideoCodecType_SorensonVideo: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo)
- [var kCMVideoCodecType_SorensonVideo: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_sorensonvideo)
- [var kCMVideoCodecType_VP9: CMVideoCodecType](/documentation/coremedia/kcmvideocodectype_vp9)
- [Video Pixel Formats](/documentation/coremedia/video-pixel-formats)

#### Constants

- [var kCMPixelFormat_16BE555: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16be555)
- [var kCMPixelFormat_16BE565: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16be565)
- [var kCMPixelFormat_16LE555: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le555)
- [var kCMPixelFormat_16LE5551: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le5551)
- [var kCMPixelFormat_16LE565: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_16le565)
- [var kCMPixelFormat_24RGB: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_24rgb)
- [var kCMPixelFormat_32ARGB: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_32argb)
- [var kCMPixelFormat_32BGRA: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_32bgra)
- [var kCMPixelFormat_422YpCbCr10: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr10)
- [var kCMPixelFormat_422YpCbCr16: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr16)
- [var kCMPixelFormat_422YpCbCr8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr8)
- [var kCMPixelFormat_422YpCbCr8_yuvs: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_422ypcbcr8_yuvs)
- [var kCMPixelFormat_4444YpCbCrA8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_4444ypcbcra8)
- [var kCMPixelFormat_444YpCbCr10: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_444ypcbcr10)
- [var kCMPixelFormat_444YpCbCr8: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_444ypcbcr8)
- [var kCMPixelFormat_8IndexedGray_WhiteIsZero: CMPixelFormatType](/documentation/coremedia/kcmpixelformat_8indexedgray_whiteiszero)
- [Video Profile Constants](/documentation/coremedia/video-profile-constants)

#### Constants

- [var kCMMPEG2VideoProfile_HDV_720p30: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_720p30)
- [var kCMMPEG2VideoProfile_HDV_1080i60: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_1080i60)
- [var kCMMPEG2VideoProfile_HDV_1080i50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_1080i50)
- [var kCMMPEG2VideoProfile_HDV_720p24: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_720p24)
- [var kCMMPEG2VideoProfile_HDV_720p25: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_720p25)
- [var kCMMPEG2VideoProfile_HDV_1080p24: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_1080p24)
- [var kCMMPEG2VideoProfile_HDV_1080p25: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_1080p25)
- [var kCMMPEG2VideoProfile_HDV_1080p30: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_1080p30)
- [var kCMMPEG2VideoProfile_HDV_720p60: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_720p60)
- [var kCMMPEG2VideoProfile_HDV_720p50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_hdv_720p50)
- [var kCMMPEG2VideoProfile_XDCAM_HD_1080i60_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_1080i60_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_HD_1080i50_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_1080i50_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_HD_1080p24_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_1080p24_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_HD_1080p25_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_1080p25_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_HD_1080p30_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_1080p30_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_720p24_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_720p24_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_720p25_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_720p25_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_720p30_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_720p30_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_720p50_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_720p50_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_720p60_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_720p60_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_1080i60_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_1080i60_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_1080i50_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_1080i50_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_1080p24_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_1080p24_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_1080p25_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_1080p25_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_EX_1080p30_VBR35: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_ex_1080p30_vbr35)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_720p50_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_720p50_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_720p60_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_720p60_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_1080i60_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_1080i60_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_1080i50_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_1080i50_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_1080p24_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_1080p24_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_1080p25_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_1080p25_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_1080p30_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_1080p30_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD_540p: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd_540p)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_540p: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_540p)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_720p24_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_720p24_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_720p25_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_720p25_cbr50)
- [var kCMMPEG2VideoProfile_XDCAM_HD422_720p30_CBR50: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xdcam_hd422_720p30_cbr50)
- [var kCMMPEG2VideoProfile_XF: Int32](/documentation/coremedia/kcmmpeg2videoprofile_xf)
- [YCbCrMatrix Extension Constants](/documentation/coremedia/ycbcrmatrix-extension-constants)

#### Constants

- [let kCMFormatDescriptionYCbCrMatrix_ITU_R_2020: CFString](/documentation/coremedia/kcmformatdescriptionycbcrmatrix_itu_r_2020)
- [let kCMFormatDescriptionYCbCrMatrix_ITU_R_601_4: CFString](/documentation/coremedia/kcmformatdescriptionycbcrmatrix_itu_r_601_4-swift.var)
- [let kCMFormatDescriptionYCbCrMatrix_ITU_R_709_2: CFString](/documentation/coremedia/kcmformatdescriptionycbcrmatrix_itu_r_709_2-swift.var)
- [let kCMFormatDescriptionYCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/coremedia/kcmformatdescriptionycbcrmatrix_smpte_240m_1995-swift.var)
- [CMAttachment](/documentation/coremedia/cmattachment-api)

### Processing Attachments

- [func CMGetAttachment(CMAttachmentBearer, key: CFString, attachmentModeOut: UnsafeMutablePointer<CMAttachmentMode>?) -> CFTypeRef?](/documentation/coremedia/cmgetattachment(_:key:attachmentmodeout:))
- [func CMCopyDictionaryOfAttachments(allocator: CFAllocator?, target: CMAttachmentBearer, attachmentMode: CMAttachmentMode) -> sending CFDictionary?](/documentation/coremedia/cmcopydictionaryofattachments(allocator:target:attachmentmode:))
- [func CMSetAttachment(CMAttachmentBearer, key: CFString, value: CFTypeRef?, attachmentMode: CMAttachmentMode)](/documentation/coremedia/cmsetattachment(_:key:value:attachmentmode:))
- [func CMSetAttachments(CMAttachmentBearer, attachments: CFDictionary, attachmentMode: CMAttachmentMode)](/documentation/coremedia/cmsetattachments(_:attachments:attachmentmode:))
- [func CMRemoveAttachment(CMAttachmentBearer, key: CFString)](/documentation/coremedia/cmremoveattachment(_:key:))
- [func CMRemoveAllAttachments(CMAttachmentBearer)](/documentation/coremedia/cmremoveallattachments(_:))
- [func CMPropagateAttachments(CMAttachmentBearer, destination: CMAttachmentBearer)](/documentation/coremedia/cmpropagateattachments(_:destination:))

### Data Types

- [CMAttachmentBearerProtocol](/documentation/coremedia/cmattachmentbearerprotocol)

#### Processing Attachments

- [var attachments: CMAttachmentBearerAttachments](/documentation/coremedia/cmattachmentbearerprotocol/attachments)
- [func propagateAttachments<T>(to: T)](/documentation/coremedia/cmattachmentbearerprotocol/propagateattachments(to:))
- [CMAttachmentBearerAttachments](/documentation/coremedia/cmattachmentbearerattachments)

##### Inspecting Attachments

- [var propagated: [String : Any]](/documentation/coremedia/cmattachmentbearerattachments/propagated)
- [var nonPropagated: [String : Any]](/documentation/coremedia/cmattachmentbearerattachments/nonpropagated)

##### Accessing Attachments

- [subscript(String) -> CMAttachmentBearerAttachments.Value?](/documentation/coremedia/cmattachmentbearerattachments/subscript(_:)-8uau0)
- [subscript(CMSampleBuffer.AttachmentKey) -> CMAttachmentBearerAttachments.Value?](/documentation/coremedia/cmattachmentbearerattachments/subscript(_:)-74jgw)
- [CMAttachmentBearerAttachments.Value](/documentation/coremedia/cmattachmentbearerattachments/value)

###### Cases

- [case shouldPropagate(Any)](/documentation/coremedia/cmattachmentbearerattachments/value/shouldpropagate(_:))
- [case shouldNotPropagate(Any)](/documentation/coremedia/cmattachmentbearerattachments/value/shouldnotpropagate(_:))

###### Properties

- [var value: Any](/documentation/coremedia/cmattachmentbearerattachments/value/value)
- [var mode: CMAttachmentBearerAttachments.Mode](/documentation/coremedia/cmattachmentbearerattachments/value/mode)

##### Managing Attachments

- [func merge([String : Any], mode: CMAttachmentBearerAttachments.Mode)](/documentation/coremedia/cmattachmentbearerattachments/merge(_:mode:))
- [CMAttachmentBearerAttachments.Mode](/documentation/coremedia/cmattachmentbearerattachments/mode)

###### Cases

- [case shouldPropagate](/documentation/coremedia/cmattachmentbearerattachments/mode/shouldpropagate)
- [case shouldNotPropagate](/documentation/coremedia/cmattachmentbearerattachments/mode/shouldnotpropagate)
- [func removeAll()](/documentation/coremedia/cmattachmentbearerattachments/removeall())
- [CMAttachmentBearer](/documentation/coremedia/cmattachmentbearer)
- [CMAttachmentMode](/documentation/coremedia/cmattachmentmode)

#### Modes

- [var kCMAttachmentMode_ShouldNotPropagate: CMAttachmentMode](/documentation/coremedia/kcmattachmentmode_shouldnotpropagate)
- [var kCMAttachmentMode_ShouldPropagate: CMAttachmentMode](/documentation/coremedia/kcmattachmentmode_shouldpropagate)

### Constants

- [var kCMAttachmentMode_ShouldNotPropagate: CMAttachmentMode](/documentation/coremedia/kcmattachmentmode_shouldnotpropagate)
- [var kCMAttachmentMode_ShouldPropagate: CMAttachmentMode](/documentation/coremedia/kcmattachmentmode_shouldpropagate)
- [let kCMSampleAttachmentKey_HEVCTemporalLevelInfo: CFString](/documentation/coremedia/kcmsampleattachmentkey_hevctemporallevelinfo)
- [let kCMSampleAttachmentKey_HEVCTemporalSubLayerAccess: CFString](/documentation/coremedia/kcmsampleattachmentkey_hevctemporalsublayeraccess)
- [let kCMSampleAttachmentKey_HEVCStepwiseTemporalSubLayerAccess: CFString](/documentation/coremedia/kcmsampleattachmentkey_hevcstepwisetemporalsublayeraccess)
- [let kCMSampleAttachmentKey_HEVCSyncSampleNALUnitType: CFString](/documentation/coremedia/kcmsampleattachmentkey_hevcsyncsamplenalunittype)
- [let kCMSampleAttachmentKey_CryptorSubsampleAuxiliaryData: CFString](/documentation/coremedia/kcmsampleattachmentkey_cryptorsubsampleauxiliarydata)
- [let kCMSampleAttachmentKey_AudioIndependentSampleDecoderRefreshCount: CFString](/documentation/coremedia/kcmsampleattachmentkey_audioindependentsampledecoderrefreshcount)
- [let kCMSampleBufferAttachmentKey_CameraIntrinsicMatrix: CFString](/documentation/coremedia/kcmsamplebufferattachmentkey_cameraintrinsicmatrix)
- [CMTaggedBuffer](/documentation/coremedia/cmtaggedbuffer)

### Creating Tagged Buffers

- [init(tags: [CMTag], buffer: CMTaggedBuffer.Buffer)](/documentation/coremedia/cmtaggedbuffer/init(tags:buffer:))
- [init(tags: [CMTag], sampleBuffer: CMSampleBuffer)](/documentation/coremedia/cmtaggedbuffer/init(tags:samplebuffer:))
- [init(tags: [CMTag], pixelBuffer: CVPixelBuffer)](/documentation/coremedia/cmtaggedbuffer/init(tags:pixelbuffer:))

### Inspecting Data

- [let tags: [CMTag]](/documentation/coremedia/cmtaggedbuffer/tags)
- [let buffer: CMTaggedBuffer.Buffer](/documentation/coremedia/cmtaggedbuffer/buffer-swift.property)

### Buffer Wrappers

- [CMTaggedBuffer.Buffer](/documentation/coremedia/cmtaggedbuffer/buffer-swift.enum)

#### Wrapped Buffer Types

- [case pixelBuffer(CVPixelBuffer)](/documentation/coremedia/cmtaggedbuffer/buffer-swift.enum/pixelbuffer(_:))
- [case sampleBuffer(CMSampleBuffer)](/documentation/coremedia/cmtaggedbuffer/buffer-swift.enum/samplebuffer(_:))
- [CMMutableDataBlockBuffer](/documentation/coremedia/cmmutabledatablockbuffer)

### Classes

- [CMMutableDataBlockBuffer.MemoryPool](/documentation/coremedia/cmmutabledatablockbuffer/memorypool)

#### Initializers

- [init(ageOutDuration: TimeInterval)](/documentation/coremedia/cmmutabledatablockbuffer/memorypool/init(ageoutduration:))

#### Instance Methods

- [func flush()](/documentation/coremedia/cmmutabledatablockbuffer/memorypool/flush())
- [func makeBlockBuffer(copying: UnsafePointer<AudioBufferList>) -> CMMutableDataBlockBuffer](/documentation/coremedia/cmmutabledatablockbuffer/memorypool/makeblockbuffer(copying:))
- [func makeBlockBuffer(count: Int) -> CMMutableDataBlockBuffer](/documentation/coremedia/cmmutabledatablockbuffer/memorypool/makeblockbuffer(count:))

### Structures

- [CMMutableDataBlockBuffer.BlockRegion](/documentation/coremedia/cmmutabledatablockbuffer/blockregion)

#### Instance Properties

- [var count: Int](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/count)
- [var endIndex: Int](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/endindex)
- [var regions: CollectionOfOne<CMMutableDataBlockBuffer.BlockRegion>](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/regions)
- [let startIndex: Int](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/startindex)

#### Instance Methods

- [func withUnsafeBytes<ResultType>((UnsafeRawBufferPointer) throws -> ResultType) rethrows -> ResultType](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/withunsafebytes(_:))
- [func withUnsafeMutableBytes<ResultType>((UnsafeMutableRawBufferPointer) throws -> ResultType) rethrows -> ResultType](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/withunsafemutablebytes(_:))

#### Subscripts

- [subscript(CMMutableDataBlockBuffer.BlockRegion.Index) -> UInt8](/documentation/coremedia/cmmutabledatablockbuffer/blockregion/subscript(_:))
- [CMMutableDataBlockBuffer.BlockSource](/documentation/coremedia/cmmutabledatablockbuffer/blocksource)

#### Initializers

- [init(allocate: (Int) -> UnsafeMutableRawBufferPointer, deallocate: (UnsafeMutableRawBufferPointer) -> Void)](/documentation/coremedia/cmmutabledatablockbuffer/blocksource/init(allocate:deallocate:))

#### Instance Properties

- [var allocate: (Int) -> UnsafeMutableRawBufferPointer](/documentation/coremedia/cmmutabledatablockbuffer/blocksource/allocate)
- [var deallocate: (UnsafeMutableRawBufferPointer) -> Void](/documentation/coremedia/cmmutabledatablockbuffer/blocksource/deallocate)

### Operators

- [static func += (inout CMMutableDataBlockBuffer, consuming CMMutableDataBlockBuffer)](/documentation/coremedia/cmmutabledatablockbuffer/+=(_:_:))

### Initializers

- [init(copying: UnsafePointer<AudioBufferList>, blockSource: CMMutableDataBlockBuffer.BlockSource?)](/documentation/coremedia/cmmutabledatablockbuffer/init(copying:blocksource:))
- [init(count: Int, blockSource: CMMutableDataBlockBuffer.BlockSource?)](/documentation/coremedia/cmmutabledatablockbuffer/init(count:blocksource:))
- [init(subBlockCapacity: Int, blockSource: CMMutableDataBlockBuffer.BlockSource?)](/documentation/coremedia/cmmutabledatablockbuffer/init(subblockcapacity:blocksource:))
- [init(unsafeBlockBuffer: sending CMBlockBuffer)](/documentation/coremedia/cmmutabledatablockbuffer/init(unsafeblockbuffer:))

### Instance Properties

- [var count: Int](/documentation/coremedia/cmmutabledatablockbuffer/count)
- [var endIndex: Int](/documentation/coremedia/cmmutabledatablockbuffer/endindex)
- [var indices: CMMutableDataBlockBuffer.Indices](/documentation/coremedia/cmmutabledatablockbuffer/indices-swift.property)
- [var isContiguous: Bool](/documentation/coremedia/cmmutabledatablockbuffer/iscontiguous)
- [var isEmpty: Bool](/documentation/coremedia/cmmutabledatablockbuffer/isempty)
- [var startIndex: Int](/documentation/coremedia/cmmutabledatablockbuffer/startindex)

### Instance Methods

- [func append(referenceOf: consuming CMMutableDataBlockBuffer, range: Range<Int>?, optimizeDepth: Bool)](/documentation/coremedia/cmmutabledatablockbuffer/append(referenceof:range:optimizedepth:))
- [func copyBytes(to: UnsafeMutableRawBufferPointer)](/documentation/coremedia/cmmutabledatablockbuffer/copybytes(to:))
- [func copyBytes<R>(to: UnsafeMutableRawBufferPointer, from: R)](/documentation/coremedia/cmmutabledatablockbuffer/copybytes(to:from:))
- [func extend(by: Int)](/documentation/coremedia/cmmutabledatablockbuffer/extend(by:))
- [func isRangeContiguous(Range<Int>) -> Bool](/documentation/coremedia/cmmutabledatablockbuffer/israngecontiguous(_:))
- [func replaceAll(repeating: UInt8)](/documentation/coremedia/cmmutabledatablockbuffer/replaceall(repeating:))
- [func replaceAll(with: UnsafeRawBufferPointer)](/documentation/coremedia/cmmutabledatablockbuffer/replaceall(with:)-4sg07)
- [func replaceAll(with: some DataProtocol)](/documentation/coremedia/cmmutabledatablockbuffer/replaceall(with:)-6jidg)
- [func replaceSubrange(Range<Int>, repeating: UInt8)](/documentation/coremedia/cmmutabledatablockbuffer/replacesubrange(_:repeating:))
- [func replaceSubrange(Range<Int>, with: some DataProtocol)](/documentation/coremedia/cmmutabledatablockbuffer/replacesubrange(_:with:)-5w62q)
- [func replaceSubrange(Range<Int>, with: UnsafeRawBufferPointer)](/documentation/coremedia/cmmutabledatablockbuffer/replacesubrange(_:with:)-7rqdy)
- [func withContiguousMutableStorageIfAvailable<R>(in: Range<Int>?, (UnsafeMutableRawBufferPointer) throws -> sending R) rethrows -> sending R?](/documentation/coremedia/cmmutabledatablockbuffer/withcontiguousmutablestorageifavailable(in:_:))
- [func withContiguousStorageIfAvailable<R>(in: Range<Int>?, (UnsafeRawBufferPointer) throws -> sending R) rethrows -> sending R?](/documentation/coremedia/cmmutabledatablockbuffer/withcontiguousstorageifavailable(in:_:))
- [func withUnsafeBlockBuffer<R>((CMBlockBuffer) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmmutabledatablockbuffer/withunsafeblockbuffer(_:))
- [func withUnsafeBlockRegions<R>(([CMReadOnlyDataBlockBuffer.BlockRegion]) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmmutabledatablockbuffer/withunsafeblockregions(_:))
- [func withUnsafeMutableBlockRegions<R>(([CMMutableDataBlockBuffer.BlockRegion]) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmmutabledatablockbuffer/withunsafemutableblockregions(_:))

### Subscripts

- [subscript(Int) -> UInt8](/documentation/coremedia/cmmutabledatablockbuffer/subscript(_:))

### Type Aliases

- [CMMutableDataBlockBuffer.Index](/documentation/coremedia/cmmutabledatablockbuffer/index)
- [CMMutableDataBlockBuffer.Indices](/documentation/coremedia/cmmutabledatablockbuffer/indices-swift.typealias)
- [CMReadOnlyDataBlockBuffer](/documentation/coremedia/cmreadonlydatablockbuffer)

### Structures

- [CMReadOnlyDataBlockBuffer.BlockRegion](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion)

#### Instance Properties

- [var count: Int](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/count)
- [var endIndex: Int](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/endindex)
- [var regions: CollectionOfOne<CMReadOnlyDataBlockBuffer.BlockRegion>](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/regions)
- [let startIndex: Int](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/startindex)

#### Instance Methods

- [func withContiguousStorageIfAvailable<R>((UnsafeBufferPointer<UInt8>) throws -> R) rethrows -> R?](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/withcontiguousstorageifavailable(_:))
- [func withUnsafeBytes<ResultType>((UnsafeRawBufferPointer) throws -> ResultType) rethrows -> ResultType](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/withunsafebytes(_:))

#### Subscripts

- [subscript(CMReadOnlyDataBlockBuffer.BlockRegion.Index) -> UInt8](/documentation/coremedia/cmreadonlydatablockbuffer/blockregion/subscript(_:))

### Operators

- [static func + (CMReadOnlyDataBlockBuffer, CMReadOnlyDataBlockBuffer) -> CMReadOnlyDataBlockBuffer](/documentation/coremedia/cmreadonlydatablockbuffer/+(_:_:)-58lg4)
- [static func + (CMReadOnlyDataBlockBuffer, consuming CMMutableDataBlockBuffer) -> CMReadOnlyDataBlockBuffer](/documentation/coremedia/cmreadonlydatablockbuffer/+(_:_:)-92jke)
- [static func += (inout CMReadOnlyDataBlockBuffer, CMReadOnlyDataBlockBuffer)](/documentation/coremedia/cmreadonlydatablockbuffer/+=(_:_:)-67kx8)
- [static func += (inout CMReadOnlyDataBlockBuffer, consuming CMMutableDataBlockBuffer)](/documentation/coremedia/cmreadonlydatablockbuffer/+=(_:_:)-7fm8e)

### Initializers

- [init(consuming CMMutableDataBlockBuffer)](/documentation/coremedia/cmreadonlydatablockbuffer/init(_:)-5fdm2)
- [init(DispatchData)](/documentation/coremedia/cmreadonlydatablockbuffer/init(_:)-80jym)
- [init(Data)](/documentation/coremedia/cmreadonlydatablockbuffer/init(_:)-w7h3)
- [init(subBlockCapacity: Int)](/documentation/coremedia/cmreadonlydatablockbuffer/init(subblockcapacity:))
- [init(unsafeBlockBuffer: sending CMBlockBuffer)](/documentation/coremedia/cmreadonlydatablockbuffer/init(unsafeblockbuffer:))

### Instance Properties

- [var isContiguous: Bool](/documentation/coremedia/cmreadonlydatablockbuffer/iscontiguous)

### Instance Methods

- [func append(referenceOf: CMReadOnlyDataBlockBuffer, optimizeDepth: Bool)](/documentation/coremedia/cmreadonlydatablockbuffer/append(referenceof:optimizedepth:)-2x1ta)
- [func append(referenceOf: consuming CMMutableDataBlockBuffer, optimizeDepth: Bool)](/documentation/coremedia/cmreadonlydatablockbuffer/append(referenceof:optimizedepth:)-5g65c)
- [func withContiguousStorageIfAvailable<R>((UnsafeRawBufferPointer) throws -> sending R) rethrows -> sending R?](/documentation/coremedia/cmreadonlydatablockbuffer/withcontiguousstorageifavailable(_:)-7tacg)
- [func withUnsafeBlockBuffer<R>((CMBlockBuffer) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmreadonlydatablockbuffer/withunsafeblockbuffer(_:))

### Default Implementations

- [Collection Implementations](/documentation/coremedia/cmreadonlydatablockbuffer/collection-implementations)

#### Instance Properties

- [var count: Int](/documentation/coremedia/cmreadonlydatablockbuffer/count)
- [var isEmpty: Bool](/documentation/coremedia/cmreadonlydatablockbuffer/isempty)
- [DataProtocol Implementations](/documentation/coremedia/cmreadonlydatablockbuffer/dataprotocol-implementations)

#### Instance Properties

- [var regions: [CMReadOnlyDataBlockBuffer.BlockRegion]](/documentation/coremedia/cmreadonlydatablockbuffer/regions)
- [RandomAccessCollection Implementations](/documentation/coremedia/cmreadonlydatablockbuffer/randomaccesscollection-implementations)

#### Instance Properties

- [var endIndex: Int](/documentation/coremedia/cmreadonlydatablockbuffer/endindex)
- [var indices: Range<Int>](/documentation/coremedia/cmreadonlydatablockbuffer/indices)
- [var startIndex: Int](/documentation/coremedia/cmreadonlydatablockbuffer/startindex)

#### Subscripts

- [subscript(Range<CMReadOnlyDataBlockBuffer.Index>) -> CMReadOnlyDataBlockBuffer](/documentation/coremedia/cmreadonlydatablockbuffer/subscript(_:)-759gz)
- [subscript(CMReadOnlyDataBlockBuffer.Index) -> UInt8](/documentation/coremedia/cmreadonlydatablockbuffer/subscript(_:)-8htjr)
- [Sequence Implementations](/documentation/coremedia/cmreadonlydatablockbuffer/sequence-implementations)

#### Instance Methods

- [func withContiguousStorageIfAvailable<R>((UnsafeBufferPointer<UInt8>) throws -> R) rethrows -> R?](/documentation/coremedia/cmreadonlydatablockbuffer/withcontiguousstorageifavailable(_:)-9q5wv)
- [CMReadySampleBuffer](/documentation/coremedia/cmreadysamplebuffer)

### Initializers

- [init(CMReadySampleBuffer<some CMSampleBuffer.Content>)](/documentation/coremedia/cmreadysamplebuffer/init(_:)-35rzo)
- [init?(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>)](/documentation/coremedia/cmreadysamplebuffer/init(_:)-3rj25)
- [init?(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>)](/documentation/coremedia/cmreadysamplebuffer/init(_:)-3tjyq)
- [init?(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>)](/documentation/coremedia/cmreadysamplebuffer/init(_:)-4j97d)
- [init?(CMReadySampleBuffer<CMSampleBuffer.DynamicContent>)](/documentation/coremedia/cmreadysamplebuffer/init(_:)-6uyu8)
- [init(audioDataBuffer: Content, formatDescription: CMAudioFormatDescription, sampleCount: Int, presentationTimeStamp: CMTime)](/documentation/coremedia/cmreadysamplebuffer/init(audiodatabuffer:formatdescription:samplecount:presentationtimestamp:))
- [init(compressedAudioDataBuffer: Content, formatDescription: CMAudioFormatDescription, presentationTimeStamp: CMTime, packetDescriptions: [AudioStreamPacketDescription])](/documentation/coremedia/cmreadysamplebuffer/init(compressedaudiodatabuffer:formatdescription:presentationtimestamp:packetdescriptions:))
- [init(dataBuffer: Content, formatDescription: CMFormatDescription, sampleProperties: CMSampleBuffer.SamplePropertiesCollection)](/documentation/coremedia/cmreadysamplebuffer/init(databuffer:formatdescription:sampleproperties:))
- [init(markerAt: CMTime, duration: CMTime)](/documentation/coremedia/cmreadysamplebuffer/init(markerat:duration:))
- [init(pixelBuffer: Content, formatDescription: CMVideoFormatDescription?, presentationTimeStamp: CMTime, duration: CMTime)](/documentation/coremedia/cmreadysamplebuffer/init(pixelbuffer:formatdescription:presentationtimestamp:duration:))
- [init(sampleDataReference: Content, formatDescription: CMFormatDescription, sampleProperties: CMSampleBuffer.SamplePropertiesCollection)](/documentation/coremedia/cmreadysamplebuffer/init(sampledatareference:formatdescription:sampleproperties:))
- [init(taggedBuffers: Content, formatDescription: CMTaggedBufferGroupFormatDescription?, presentationTimeStamp: CMTime, duration: CMTime)](/documentation/coremedia/cmreadysamplebuffer/init(taggedbuffers:formatdescription:presentationtimestamp:duration:))
- [init(unsafeBuffer: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafebuffer:))
- [init(unsafeMarkerOnlySampleBuffer: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafemarkeronlysamplebuffer:))
- [init(unsafeSampleDataReferenceBuffer: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafesampledatareferencebuffer:))
- [init(unsafeWithDataBuffer: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafewithdatabuffer:))
- [init(unsafeWithPixelBuffer: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafewithpixelbuffer:))
- [init(unsafeWithTaggedBuffers: sending CMSampleBuffer)](/documentation/coremedia/cmreadysamplebuffer/init(unsafewithtaggedbuffers:))

### Instance Properties

- [var audioStreamPacketDescriptions: [AudioStreamPacketDescription]?](/documentation/coremedia/cmreadysamplebuffer/audiostreampacketdescriptions)
- [var content: CMSampleDataReference](/documentation/coremedia/cmreadysamplebuffer/content-12bds)
- [var content: CMSampleBuffer.DynamicContent](/documentation/coremedia/cmreadysamplebuffer/content-14qb7)
- [var content: CVReadOnlyPixelBuffer](/documentation/coremedia/cmreadysamplebuffer/content-4peot)
- [var content: Array<CMTaggedDynamicBuffer>](/documentation/coremedia/cmreadysamplebuffer/content-5fko2)
- [var content: CMReadOnlyDataBlockBuffer](/documentation/coremedia/cmreadysamplebuffer/content-6ihvr)
- [var contentType: CMSampleBuffer.ContentType](/documentation/coremedia/cmreadysamplebuffer/contenttype)
- [var decodeTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/decodetimestamp)
- [var duration: CMTime](/documentation/coremedia/cmreadysamplebuffer/duration-2ssr4)
- [var duration: CMTime](/documentation/coremedia/cmreadysamplebuffer/duration-54778)
- [var duration: CMTime](/documentation/coremedia/cmreadysamplebuffer/duration-94fnq)
- [var duration: CMTime](/documentation/coremedia/cmreadysamplebuffer/duration-9lx3g)
- [var formatDescription: CMFormatDescription](/documentation/coremedia/cmreadysamplebuffer/formatdescription-6rp0o)
- [var formatDescription: CMFormatDescription?](/documentation/coremedia/cmreadysamplebuffer/formatdescription-9i48t)
- [var markerTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/markertimestamp)
- [var outputDecodeTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/outputdecodetimestamp)
- [var outputDuration: CMTime](/documentation/coremedia/cmreadysamplebuffer/outputduration)
- [var outputPresentationTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/outputpresentationtimestamp)
- [var outputSampleTimings: CMSampleBuffer.TimingPerSample?](/documentation/coremedia/cmreadysamplebuffer/outputsampletimings)
- [var presentationTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/presentationtimestamp-19vwq)
- [var presentationTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/presentationtimestamp-266ka)
- [var presentationTimeStamp: CMTime](/documentation/coremedia/cmreadysamplebuffer/presentationtimestamp-7ea7z)
- [var sampleAttachments: CMSampleBuffer.SampleAttachments](/documentation/coremedia/cmreadysamplebuffer/sampleattachments-8g6nm)
- [var sampleAttachments: CMSampleBuffer.SampleAttachments](/documentation/coremedia/cmreadysamplebuffer/sampleattachments-9g3d5)
- [var sampleCount: Int](/documentation/coremedia/cmreadysamplebuffer/samplecount)
- [var sampleProperties: CMSampleBuffer.SamplePropertiesCollection](/documentation/coremedia/cmreadysamplebuffer/sampleproperties)
- [var totalSampleSize: Int](/documentation/coremedia/cmreadysamplebuffer/totalsamplesize)

### Instance Methods

- [func attach(contentKey: AVContentKey) throws](/documentation/coremedia/cmreadysamplebuffer/attach(contentkey:))
- [func copyPCMData(fromRange: Range<Int>, into: UnsafeMutablePointer<AudioBufferList>) throws](/documentation/coremedia/cmreadysamplebuffer/copypcmdata(fromrange:into:))
- [func splitSamples() -> [CMReadySampleBuffer<Content>]](/documentation/coremedia/cmreadysamplebuffer/splitsamples())
- [func withUnsafeSampleBuffer<R>((CMSampleBuffer) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmreadysamplebuffer/withunsafesamplebuffer(_:))
- [CMSampleDataReference](/documentation/coremedia/cmsampledatareference)

### Initializers

- [init(containerLocation: URL, byteOffset: Int)](/documentation/coremedia/cmsampledatareference/init(containerlocation:byteoffset:))

### Instance Properties

- [var byteOffset: Int](/documentation/coremedia/cmsampledatareference/byteoffset)
- [var containerLocation: URL](/documentation/coremedia/cmsampledatareference/containerlocation)
- [CMTaggedDynamicBuffer](/documentation/coremedia/cmtaggeddynamicbuffer)

### Initializers

- [init(tags: [CMTag], content: CVReadOnlyPixelBuffer)](/documentation/coremedia/cmtaggeddynamicbuffer/init(tags:content:)-1hscu)
- [init(tags: [CMTag], content: CMTaggedDynamicBuffer.Content)](/documentation/coremedia/cmtaggeddynamicbuffer/init(tags:content:)-1ttie)
- [init(tags: [CMTag], content: CMReadySampleBuffer<CVReadOnlyPixelBuffer>)](/documentation/coremedia/cmtaggeddynamicbuffer/init(tags:content:)-5jtjt)
- [init(tags: [CMTag], content: CMReadySampleBuffer<CMReadOnlyDataBlockBuffer>)](/documentation/coremedia/cmtaggeddynamicbuffer/init(tags:content:)-5xcim)
- [init(unsafeBuffer: sending CMTaggedBuffer)](/documentation/coremedia/cmtaggeddynamicbuffer/init(unsafebuffer:))

### Instance Properties

- [var content: CMTaggedDynamicBuffer.Content](/documentation/coremedia/cmtaggeddynamicbuffer/content-swift.property)
- [var tags: [CMTag]](/documentation/coremedia/cmtaggeddynamicbuffer/tags)

### Instance Methods

- [func withUnsafeTaggedBuffer<R>((CMTaggedBuffer) throws -> sending R) rethrows -> sending R](/documentation/coremedia/cmtaggeddynamicbuffer/withunsafetaggedbuffer(_:))

### Enumerations

- [CMTaggedDynamicBuffer.Content](/documentation/coremedia/cmtaggeddynamicbuffer/content-swift.enum)

#### Enumeration Cases

- [case dataSampleBuffer(CMReadySampleBuffer<CMReadOnlyDataBlockBuffer>)](/documentation/coremedia/cmtaggeddynamicbuffer/content-swift.enum/datasamplebuffer(_:))
- [case pixelBuffer(CVReadOnlyPixelBuffer)](/documentation/coremedia/cmtaggeddynamicbuffer/content-swift.enum/pixelbuffer(_:))
- [case pixelSampleBuffer(CMReadySampleBuffer<CVReadOnlyPixelBuffer>)](/documentation/coremedia/cmtaggeddynamicbuffer/content-swift.enum/pixelsamplebuffer(_:))

## Time Representation

- [CMTime](/documentation/coremedia/cmtime-api)

### Creating a Time

- [func CMTimeMake(value: Int64, timescale: Int32) -> CMTime](/documentation/coremedia/cmtimemake(value:timescale:))
- [func CMTimeMakeWithEpoch(value: Int64, timescale: Int32, epoch: Int64) -> CMTime](/documentation/coremedia/cmtimemakewithepoch(value:timescale:epoch:))
- [func CMTimeMakeWithSeconds(Float64, preferredTimescale: Int32) -> CMTime](/documentation/coremedia/cmtimemakewithseconds(_:preferredtimescale:))
- [func CMTimeMakeFromDictionary(CFDictionary?) -> CMTime](/documentation/coremedia/cmtimemakefromdictionary(_:))

### Inspecting a Time

- [func CMTimeGetSeconds(CMTime) -> Float64](/documentation/coremedia/cmtimegetseconds(_:))
- [func CMTimeAbsoluteValue(CMTime) -> CMTime](/documentation/coremedia/cmtimeabsolutevalue(_:))
- [func CMTIME_IS_VALID(CMTime) -> Bool](/documentation/coremedia/cmtime_is_valid(_:))
- [func CMTIME_IS_INVALID(CMTime) -> Bool](/documentation/coremedia/cmtime_is_invalid(_:))
- [func CMTIME_IS_POSITIVEINFINITY(CMTime) -> Bool](/documentation/coremedia/cmtime_is_positiveinfinity(_:))
- [func CMTIME_IS_NEGATIVEINFINITY(CMTime) -> Bool](/documentation/coremedia/cmtime_is_negativeinfinity(_:))
- [func CMTIME_IS_INDEFINITE(CMTime) -> Bool](/documentation/coremedia/cmtime_is_indefinite(_:))
- [func CMTIME_IS_NUMERIC(CMTime) -> Bool](/documentation/coremedia/cmtime_is_numeric(_:))
- [func CMTIME_HAS_BEEN_ROUNDED(CMTime) -> Bool](/documentation/coremedia/cmtime_has_been_rounded(_:))

### Performing Time Calculations

- [func CMTimeAdd(CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtimeadd(_:_:))
- [func CMTimeSubtract(CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtimesubtract(_:_:))
- [func CMTimeMultiply(CMTime, multiplier: Int32) -> CMTime](/documentation/coremedia/cmtimemultiply(_:multiplier:))
- [func CMTimeMultiplyByFloat64(CMTime, multiplier: Float64) -> CMTime](/documentation/coremedia/cmtimemultiplybyfloat64(_:multiplier:))
- [func CMTimeMultiplyByRatio(CMTime, multiplier: Int32, divisor: Int32) -> CMTime](/documentation/coremedia/cmtimemultiplybyratio(_:multiplier:divisor:))

### Changing the Timescale

- [func CMTimeConvertScale(CMTime, timescale: Int32, method: CMTimeRoundingMethod) -> CMTime](/documentation/coremedia/cmtimeconvertscale(_:timescale:method:))
- [CMTimeRoundingMethod](/documentation/coremedia/cmtimeroundingmethod)

#### Default Rounding Method

- [static var `default`: CMTimeRoundingMethod](/documentation/coremedia/cmtimeroundingmethod/default)

#### Rounding Methods

- [case roundHalfAwayFromZero](/documentation/coremedia/cmtimeroundingmethod/roundhalfawayfromzero)
- [case roundAwayFromZero](/documentation/coremedia/cmtimeroundingmethod/roundawayfromzero)
- [case roundTowardZero](/documentation/coremedia/cmtimeroundingmethod/roundtowardzero)
- [case quickTime](/documentation/coremedia/cmtimeroundingmethod/quicktime)
- [case roundTowardPositiveInfinity](/documentation/coremedia/cmtimeroundingmethod/roundtowardpositiveinfinity)
- [case roundTowardNegativeInfinity](/documentation/coremedia/cmtimeroundingmethod/roundtowardnegativeinfinity)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coremedia/cmtimeroundingmethod/init(rawvalue:))

### Comparing Times

- [func CMTimeCompare(CMTime, CMTime) -> Int32](/documentation/coremedia/cmtimecompare(_:_:))
- [func CMTimeMaximum(CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtimemaximum(_:_:))
- [func CMTimeMinimum(CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtimeminimum(_:_:))

### Representing Times

- [func CMTimeShow(CMTime)](/documentation/coremedia/cmtimeshow(_:))
- [func CMTimeCopyDescription(allocator: CFAllocator?, time: CMTime) -> CFString?](/documentation/coremedia/cmtimecopydescription(allocator:time:))
- [func CMTimeCopyAsDictionary(CMTime, allocator: CFAllocator?) -> CFDictionary?](/documentation/coremedia/cmtimecopyasdictionary(_:allocator:))

### Data Types

- [CMTime](/documentation/coremedia/cmtime)

#### Creating a Time

- [init(value: CMTimeValue, timescale: CMTimeScale)](/documentation/coremedia/cmtime/init(value:timescale:))
- [init(value: CMTimeValue, timescale: CMTimeScale, flags: CMTimeFlags, epoch: CMTimeEpoch)](/documentation/coremedia/cmtime/init(value:timescale:flags:epoch:))
- [init(seconds: Double, preferredTimescale: CMTimeScale)](/documentation/coremedia/cmtime/init(seconds:preferredtimescale:))
- [init()](/documentation/coremedia/cmtime/init())

#### Inspecting a Time

- [var seconds: Double](/documentation/coremedia/cmtime/seconds)
- [var hasBeenRounded: Bool](/documentation/coremedia/cmtime/hasbeenrounded)
- [var isValid: Bool](/documentation/coremedia/cmtime/isvalid)
- [var isNumeric: Bool](/documentation/coremedia/cmtime/isnumeric)
- [var isIndefinite: Bool](/documentation/coremedia/cmtime/isindefinite)
- [var isPositiveInfinity: Bool](/documentation/coremedia/cmtime/ispositiveinfinity)
- [var isNegativeInfinity: Bool](/documentation/coremedia/cmtime/isnegativeinfinity)

#### Performing Time Calcualtions

- [static func + (CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtime/+(_:_:))
- [static func - (CMTime, CMTime) -> CMTime](/documentation/coremedia/cmtime/-(_:_:))

#### Changing the Timescale

- [func convertScale(Int32, method: CMTimeRoundingMethod) -> CMTime](/documentation/coremedia/cmtime/convertscale(_:method:))
- [CMTimeRoundingMethod](/documentation/coremedia/cmtimeroundingmethod)

##### Default Rounding Method

- [static var `default`: CMTimeRoundingMethod](/documentation/coremedia/cmtimeroundingmethod/default)

##### Rounding Methods

- [case roundHalfAwayFromZero](/documentation/coremedia/cmtimeroundingmethod/roundhalfawayfromzero)
- [case roundAwayFromZero](/documentation/coremedia/cmtimeroundingmethod/roundawayfromzero)
- [case roundTowardZero](/documentation/coremedia/cmtimeroundingmethod/roundtowardzero)
- [case quickTime](/documentation/coremedia/cmtimeroundingmethod/quicktime)
- [case roundTowardPositiveInfinity](/documentation/coremedia/cmtimeroundingmethod/roundtowardpositiveinfinity)
- [case roundTowardNegativeInfinity](/documentation/coremedia/cmtimeroundingmethod/roundtowardnegativeinfinity)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/coremedia/cmtimeroundingmethod/init(rawvalue:))

#### Accessing Time Values

- [var value: CMTimeValue](/documentation/coremedia/cmtime/value)
- [var timescale: CMTimeScale](/documentation/coremedia/cmtime/timescale)
- [var flags: CMTimeFlags](/documentation/coremedia/cmtime/flags)
- [var epoch: CMTimeEpoch](/documentation/coremedia/cmtime/epoch)

#### Constants

- [static let zero: CMTime](/documentation/coremedia/cmtime/zero)
- [static let invalid: CMTime](/documentation/coremedia/cmtime/invalid)
- [static let indefinite: CMTime](/documentation/coremedia/cmtime/indefinite)
- [static let negativeInfinity: CMTime](/documentation/coremedia/cmtime/negativeinfinity)
- [static let positiveInfinity: CMTime](/documentation/coremedia/cmtime/positiveinfinity)

#### Operators

- [static func != (CMTime, CMTime) -> Bool](/documentation/coremedia/cmtime/!=(_:_:))
- [CMTimeValue](/documentation/coremedia/cmtimevalue)
- [CMTimeScale](/documentation/coremedia/cmtimescale)
- [CMTimeEpoch](/documentation/coremedia/cmtimeepoch)
- [CMTimeFlags](/documentation/coremedia/cmtimeflags)

#### Properties

- [static var valid: CMTimeFlags](/documentation/coremedia/cmtimeflags/valid)
- [static var hasBeenRounded: CMTimeFlags](/documentation/coremedia/cmtimeflags/hasbeenrounded)
- [static var positiveInfinity: CMTimeFlags](/documentation/coremedia/cmtimeflags/positiveinfinity)
- [static var negativeInfinity: CMTimeFlags](/documentation/coremedia/cmtimeflags/negativeinfinity)
- [static var indefinite: CMTimeFlags](/documentation/coremedia/cmtimeflags/indefinite)
- [static var impliedValueFlagsMask: CMTimeFlags](/documentation/coremedia/cmtimeflags/impliedvalueflagsmask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coremedia/cmtimeflags/init(rawvalue:))

### Constants

- [Time](/documentation/coremedia/cmtime-time)

#### Defined Times

- [static let invalid: CMTime](/documentation/coremedia/cmtime/invalid)
- [static let indefinite: CMTime](/documentation/coremedia/cmtime/indefinite)
- [static let positiveInfinity: CMTime](/documentation/coremedia/cmtime/positiveinfinity)
- [static let negativeInfinity: CMTime](/documentation/coremedia/cmtime/negativeinfinity)
- [static let zero: CMTime](/documentation/coremedia/cmtime/zero)
- [Timescale](/documentation/coremedia/cmtime-timescale)

#### Timescales

- [var kCMTimeMaxTimescale: Int](/documentation/coremedia/kcmtimemaxtimescale)
- [Dictionary Keys](/documentation/coremedia/cmtime-dictionary-keys)

#### Constants

- [let kCMTimeValueKey: CFString](/documentation/coremedia/kcmtimevaluekey)
- [let kCMTimeScaleKey: CFString](/documentation/coremedia/kcmtimescalekey)
- [let kCMTimeEpochKey: CFString](/documentation/coremedia/kcmtimeepochkey)
- [let kCMTimeFlagsKey: CFString](/documentation/coremedia/kcmtimeflagskey)
- [CMTimeRange](/documentation/coremedia/cmtimerange-api)

### Creating Time Ranges

- [func CMTimeRangeMake(start: CMTime, duration: CMTime) -> CMTimeRange](/documentation/coremedia/cmtimerangemake(start:duration:))
- [func CMTimeRangeMakeFromDictionary(CFDictionary) -> CMTimeRange](/documentation/coremedia/cmtimerangemakefromdictionary(_:))
- [func CMTimeRangeFromTimeToTime(start: CMTime, end: CMTime) -> CMTimeRange](/documentation/coremedia/cmtimerangefromtimetotime(start:end:))

### Comparing Time Ranges

- [func CMTimeRangeEqual(CMTimeRange, CMTimeRange) -> Bool](/documentation/coremedia/cmtimerangeequal(_:_:))
- [func CMTimeRangeContainsTime(CMTimeRange, time: CMTime) -> Bool](/documentation/coremedia/cmtimerangecontainstime(_:time:))
- [func CMTimeRangeContainsTimeRange(CMTimeRange, otherRange: CMTimeRange) -> Bool](/documentation/coremedia/cmtimerangecontainstimerange(_:otherrange:))

### Inspecting Time Ranges

- [func CMTIMERANGE_IS_EMPTY(CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange_is_empty(_:))
- [func CMTIMERANGE_IS_INDEFINITE(CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange_is_indefinite(_:))
- [func CMTIMERANGE_IS_INVALID(CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange_is_invalid(_:))
- [func CMTIMERANGE_IS_VALID(CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange_is_valid(_:))
- [func CMTimeRangeGetEnd(CMTimeRange) -> CMTime](/documentation/coremedia/cmtimerangegetend(_:))
- [func CMTimeRangeGetIntersection(CMTimeRange, otherRange: CMTimeRange) -> CMTimeRange](/documentation/coremedia/cmtimerangegetintersection(_:otherrange:))
- [func CMTimeRangeGetUnion(CMTimeRange, otherRange: CMTimeRange) -> CMTimeRange](/documentation/coremedia/cmtimerangegetunion(_:otherrange:))

### Utility Functions

- [func CMTimeClampToRange(CMTime, range: CMTimeRange) -> CMTime](/documentation/coremedia/cmtimeclamptorange(_:range:))
- [func CMTimeMapDurationFromRangeToRange(CMTime, fromRange: CMTimeRange, toRange: CMTimeRange) -> CMTime](/documentation/coremedia/cmtimemapdurationfromrangetorange(_:fromrange:torange:))
- [func CMTimeMapTimeFromRangeToRange(CMTime, fromRange: CMTimeRange, toRange: CMTimeRange) -> CMTime](/documentation/coremedia/cmtimemaptimefromrangetorange(_:fromrange:torange:))
- [func CMTimeRangeCopyAsDictionary(CMTimeRange, allocator: CFAllocator?) -> CFDictionary?](/documentation/coremedia/cmtimerangecopyasdictionary(_:allocator:))
- [func CMTimeRangeCopyDescription(allocator: CFAllocator?, range: CMTimeRange) -> CFString?](/documentation/coremedia/cmtimerangecopydescription(allocator:range:))
- [func CMTimeRangeShow(CMTimeRange)](/documentation/coremedia/cmtimerangeshow(_:))

### Data Types

- [CMTimeRange](/documentation/coremedia/cmtimerange)

#### Creating Time Ranges

- [init()](/documentation/coremedia/cmtimerange/init())
- [init(start: CMTime, duration: CMTime)](/documentation/coremedia/cmtimerange/init(start:duration:))
- [init(start: CMTime, end: CMTime)](/documentation/coremedia/cmtimerange/init(start:end:))

#### Inspecting Time Ranges

- [var start: CMTime](/documentation/coremedia/cmtimerange/start)
- [var end: CMTime](/documentation/coremedia/cmtimerange/end)
- [var duration: CMTime](/documentation/coremedia/cmtimerange/duration)
- [var isValid: Bool](/documentation/coremedia/cmtimerange/isvalid)
- [var isEmpty: Bool](/documentation/coremedia/cmtimerange/isempty)
- [var isIndefinite: Bool](/documentation/coremedia/cmtimerange/isindefinite)

#### Finding Elements

- [func containsTime(CMTime) -> Bool](/documentation/coremedia/cmtimerange/containstime(_:))
- [func containsTimeRange(CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange/containstimerange(_:))

#### Combining Time Ranges

- [func intersection(CMTimeRange) -> CMTimeRange](/documentation/coremedia/cmtimerange/intersection(_:))
- [func union(CMTimeRange) -> CMTimeRange](/documentation/coremedia/cmtimerange/union(_:))

#### Constants

- [static let zero: CMTimeRange](/documentation/coremedia/cmtimerange/zero)
- [static let invalid: CMTimeRange](/documentation/coremedia/cmtimerange/invalid)

#### Operators

- [static func != (CMTimeRange, CMTimeRange) -> Bool](/documentation/coremedia/cmtimerange/!=(_:_:))

### Constants

- [Dictionary Keys](/documentation/coremedia/cmtimerange-dictionary-keys)

#### Constants

- [let kCMTimeRangeStartKey: CFString](/documentation/coremedia/kcmtimerangestartkey)
- [let kCMTimeRangeDurationKey: CFString](/documentation/coremedia/kcmtimerangedurationkey)
- [Pre-Specified Time Ranges](/documentation/coremedia/pre-specified-time-ranges)

#### Constants

- [static let zero: CMTimeRange](/documentation/coremedia/cmtimerange/zero)
- [static let invalid: CMTimeRange](/documentation/coremedia/cmtimerange/invalid)
- [CMTimeMapping](/documentation/coremedia/cmtimemapping-api)

### Creating Time Mappings

- [func CMTimeMappingMake(source: CMTimeRange, target: CMTimeRange) -> CMTimeMapping](/documentation/coremedia/cmtimemappingmake(source:target:))
- [func CMTimeMappingMakeEmpty(target: CMTimeRange) -> CMTimeMapping](/documentation/coremedia/cmtimemappingmakeempty(target:))
- [func CMTimeMappingMakeFromDictionary(CFDictionary) -> CMTimeMapping](/documentation/coremedia/cmtimemappingmakefromdictionary(_:))

### Representing Time Mappings

- [func CMTimeMappingCopyAsDictionary(CMTimeMapping, allocator: CFAllocator?) -> CFDictionary?](/documentation/coremedia/cmtimemappingcopyasdictionary(_:allocator:))
- [func CMTimeMappingCopyDescription(allocator: CFAllocator?, mapping: CMTimeMapping) -> CFString?](/documentation/coremedia/cmtimemappingcopydescription(allocator:mapping:))
- [func CMTimeMappingShow(CMTimeMapping)](/documentation/coremedia/cmtimemappingshow(_:))

### Data Types

- [CMTimeMapping](/documentation/coremedia/cmtimemapping)

#### Creating a Timebase

- [init(source: CMTimeRange, target: CMTimeRange)](/documentation/coremedia/cmtimemapping/init(source:target:))
- [init()](/documentation/coremedia/cmtimemapping/init())

#### Accessing Time Ranges

- [var source: CMTimeRange](/documentation/coremedia/cmtimemapping/source)
- [var target: CMTimeRange](/documentation/coremedia/cmtimemapping/target)

#### Type Properties

- [static let invalid: CMTimeMapping](/documentation/coremedia/cmtimemapping/invalid)

### Constants

- [static let invalid: CMTimeMapping](/documentation/coremedia/cmtimemapping/invalid)
- [let kCMTimeMappingSourceKey: CFString](/documentation/coremedia/kcmtimemappingsourcekey)
- [let kCMTimeMappingTargetKey: CFString](/documentation/coremedia/kcmtimemappingtargetkey)

## Media Synchronization

- [CMClock](/documentation/coremedia/cmclock-api)

### Accessing the Host Clock

- [func CMClockGetHostTimeClock() -> CMClock](/documentation/coremedia/cmclockgethosttimeclock())

### Stopping the Clock

- [func CMClockInvalidate(CMClock)](/documentation/coremedia/cmclockinvalidate(_:))

### Accessing and Converting Time

- [func CMClockGetTime(CMClock) -> CMTime](/documentation/coremedia/cmclockgettime(_:))
- [func CMClockGetAnchorTime(CMClock, clockTimeOut: UnsafeMutablePointer<CMTime>, referenceClockTimeOut: UnsafeMutablePointer<CMTime>) -> OSStatus](/documentation/coremedia/cmclockgetanchortime(_:clocktimeout:referenceclocktimeout:))
- [func CMClockConvertHostTimeToSystemUnits(CMTime) -> UInt64](/documentation/coremedia/cmclockconverthosttimetosystemunits(_:))
- [func CMClockMakeHostTimeFromSystemUnits(UInt64) -> CMTime](/documentation/coremedia/cmclockmakehosttimefromsystemunits(_:))

### Getting and Syncing Time

- [func CMSyncGetTime(CMClockOrTimebase) -> CMTime](/documentation/coremedia/cmsyncgettime(_:))
- [func CMSyncGetRelativeRate(CMClockOrTimebase, relativeTo: CMClockOrTimebase) -> Float64](/documentation/coremedia/cmsyncgetrelativerate(_:relativeto:))
- [func CMSyncGetRelativeRateAndAnchorTime(CMClockOrTimebase, relativeTo: CMClockOrTimebase, relativeRateOut: UnsafeMutablePointer<Float64>?, anchorTimeOut: UnsafeMutablePointer<CMTime>?, relativeToAnchorTimeOut: UnsafeMutablePointer<CMTime>?) -> OSStatus](/documentation/coremedia/cmsyncgetrelativerateandanchortime(_:relativeto:relativerateout:anchortimeout:relativetoanchortimeout:))
- [func CMSyncConvertTime(CMTime, from: CMClockOrTimebase, to: CMClockOrTimebase) -> CMTime](/documentation/coremedia/cmsyncconverttime(_:from:to:))

### Determining Clock Drift

- [func CMClockMightDrift(CMClock, otherClock: CMClock) -> Bool](/documentation/coremedia/cmclockmightdrift(_:otherclock:))
- [func CMSyncMightDrift(CMClockOrTimebase, CMClockOrTimebase) -> Bool](/documentation/coremedia/cmsyncmightdrift(_:_:))

### Data Types

- [CMClock](/documentation/coremedia/cmclock)

#### Inspecting a Clock

- [var time: CMTime](/documentation/coremedia/cmclock/time)
- [static var typeID: CFTypeID](/documentation/coremedia/cmclock/typeid)

#### Stopping a Clock

- [func invalidate()](/documentation/coremedia/cmclock/invalidate())

#### Getting the Host Time

- [static var hostTimeClock: CMClock](/documentation/coremedia/cmclock/hosttimeclock)

#### Getting Time and Devices

- [func anchorTime() throws -> (anchorTime: CMTime, referenceTime: CMTime)](/documentation/coremedia/cmclock/anchortime())
- [func audioDevice() throws -> (deviceUID: String?, deviceID: AudioDeviceID, trackingDefaultDevice: Bool)](/documentation/coremedia/cmclock/audiodevice())
- [func setAudioDeviceID(AudioDeviceID) throws](/documentation/coremedia/cmclock/setaudiodeviceid(_:))
- [func setAudioDeviceUID(String?) throws](/documentation/coremedia/cmclock/setaudiodeviceuid(_:))

#### Determining Time Drift

- [func mightDrift(relativeTo: CMClock) -> Bool](/documentation/coremedia/cmclock/mightdrift(relativeto:))

#### Converting Time

- [static func convertHostTimeToSystemUnits(CMTime) -> UInt64](/documentation/coremedia/cmclock/converthosttimetosystemunits(_:))
- [static func convertSystemUnitsToHostTime(UInt64) -> CMTime](/documentation/coremedia/cmclock/convertsystemunitstohosttime(_:))

#### Constants

- [CMClock.Error](/documentation/coremedia/cmclock/error)

##### Constants

- [static let allocationFailed: NSError](/documentation/coremedia/cmclock/error/allocationfailed)
- [static let invalidParameter: NSError](/documentation/coremedia/cmclock/error/invalidparameter)
- [static let missingRequiredParameter: NSError](/documentation/coremedia/cmclock/error/missingrequiredparameter)
- [static let unsupportedOperation: NSError](/documentation/coremedia/cmclock/error/unsupportedoperation)

#### Initializers

- [init(referencing: CMClock)](/documentation/coremedia/cmclock/init(referencing:))

#### Type Aliases

- [CMClock.T](/documentation/coremedia/cmclock/t)

#### Default Implementations

- [CMSyncProtocol Implementations](/documentation/coremedia/cmclock/cmsyncprotocol-implementations)

##### Instance Properties

- [var time: CMTime](/documentation/coremedia/cmclock/time)
- [CMClockOrTimebase](/documentation/coremedia/cmclockortimebase)
- [func CMClockGetTypeID() -> CFTypeID](/documentation/coremedia/cmclockgettypeid())

### Constants

- [CMClock Error Codes](/documentation/coremedia/cmclock-error-codes)

#### Constants

- [var kCMClockError_MissingRequiredParameter: OSStatus](/documentation/coremedia/kcmclockerror_missingrequiredparameter)
- [var kCMClockError_InvalidParameter: OSStatus](/documentation/coremedia/kcmclockerror_invalidparameter)
- [var kCMClockError_AllocationFailed: OSStatus](/documentation/coremedia/kcmclockerror_allocationfailed)
- [var kCMClockError_UnsupportedOperation: OSStatus](/documentation/coremedia/kcmclockerror_unsupportedoperation)
- [CMTimebase Error Codes](/documentation/coremedia/cmtimebase-errors)

#### Constants

- [var kCMTimebaseError_MissingRequiredParameter: OSStatus](/documentation/coremedia/kcmtimebaseerror_missingrequiredparameter)
- [var kCMTimebaseError_InvalidParameter: OSStatus](/documentation/coremedia/kcmtimebaseerror_invalidparameter)
- [var kCMTimebaseError_AllocationFailed: OSStatus](/documentation/coremedia/kcmtimebaseerror_allocationfailed)
- [var kCMTimebaseError_TimerIntervalTooShort: OSStatus](/documentation/coremedia/kcmtimebaseerror_timerintervaltooshort)
- [var kCMTimebaseError_ReadOnly: OSStatus](/documentation/coremedia/kcmtimebaseerror_readonly)
- [CMSync error codes](/documentation/coremedia/cmsync-error-codes)

#### Constants

- [var kCMSyncError_MissingRequiredParameter: OSStatus](/documentation/coremedia/kcmsyncerror_missingrequiredparameter)
- [var kCMSyncError_InvalidParameter: OSStatus](/documentation/coremedia/kcmsyncerror_invalidparameter)
- [var kCMSyncError_AllocationFailed: OSStatus](/documentation/coremedia/kcmsyncerror_allocationfailed)
- [var kCMSyncError_RateMustBeNonZero: OSStatus](/documentation/coremedia/kcmsyncerror_ratemustbenonzero)
- [Timebase Notifications](/documentation/coremedia/timebase-notifications)

#### Constants

- [let kCMTimebaseNotification_EffectiveRateChanged: CFString](/documentation/coremedia/kcmtimebasenotification_effectiveratechanged)
- [let kCMTimebaseNotification_TimeJumped: CFString](/documentation/coremedia/kcmtimebasenotification_timejumped)
- [CMAudioClock](/documentation/coremedia/cmaudioclock-api)

### Creating Audio Clocks

- [func CMAudioClockCreate(allocator: CFAllocator?, clockOut: UnsafeMutablePointer<CMClock?>) -> OSStatus](/documentation/coremedia/cmaudioclockcreate(allocator:clockout:))
- [func CMAudioDeviceClockCreate(allocator: CFAllocator?, deviceUID: CFString?, clockOut: UnsafeMutablePointer<CMClock?>) -> OSStatus](/documentation/coremedia/cmaudiodeviceclockcreate(allocator:deviceuid:clockout:))
- [func CMAudioDeviceClockCreateFromAudioDeviceID(allocator: CFAllocator?, deviceID: AudioDeviceID, clockOut: UnsafeMutablePointer<CMClock?>) -> OSStatus](/documentation/coremedia/cmaudiodeviceclockcreatefromaudiodeviceid(allocator:deviceid:clockout:))

### Configuring Audio Clocks

- [func CMAudioDeviceClockGetAudioDevice(CMClock, deviceUIDOut: AutoreleasingUnsafeMutablePointer<CFString?>?, deviceIDOut: UnsafeMutablePointer<AudioDeviceID>?, trackingDefaultDeviceOut: UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/coremedia/cmaudiodeviceclockgetaudiodevice(_:deviceuidout:deviceidout:trackingdefaultdeviceout:))
- [func CMAudioDeviceClockSetAudioDeviceUID(CMClock, deviceUID: CFString?) -> OSStatus](/documentation/coremedia/cmaudiodeviceclocksetaudiodeviceuid(_:deviceuid:))
- [func CMAudioDeviceClockSetAudioDeviceID(CMClock, deviceID: AudioDeviceID) -> OSStatus](/documentation/coremedia/cmaudiodeviceclocksetaudiodeviceid(_:deviceid:))
- [CMTimebase](/documentation/coremedia/cmtimebase-api)

### Creating Timebases

- [func CMTimebaseCreateWithSourceClock(allocator: CFAllocator?, sourceClock: CMClock, timebaseOut: UnsafeMutablePointer<CMTimebase?>) -> OSStatus](/documentation/coremedia/cmtimebasecreatewithsourceclock(allocator:sourceclock:timebaseout:))
- [func CMTimebaseCreateWithSourceTimebase(allocator: CFAllocator?, sourceTimebase: CMTimebase, timebaseOut: UnsafeMutablePointer<CMTimebase?>) -> OSStatus](/documentation/coremedia/cmtimebasecreatewithsourcetimebase(allocator:sourcetimebase:timebaseout:))

### Copying Timebases

- [func CMTimebaseCopySource(CMTimebase) -> CMClockOrTimebase](/documentation/coremedia/cmtimebasecopysource(_:))
- [func CMTimebaseCopySourceClock(CMTimebase) -> CMClock?](/documentation/coremedia/cmtimebasecopysourceclock(_:))
- [func CMTimebaseCopySourceTimebase(CMTimebase) -> CMTimebase?](/documentation/coremedia/cmtimebasecopysourcetimebase(_:))
- [func CMTimebaseCopyUltimateSourceClock(CMTimebase) -> CMClock](/documentation/coremedia/cmtimebasecopyultimatesourceclock(_:))

### Getting and Setting Time

- [func CMTimebaseGetTime(CMTimebase) -> CMTime](/documentation/coremedia/cmtimebasegettime(_:))
- [func CMTimebaseGetTimeWithTimeScale(CMTimebase, timescale: CMTimeScale, method: CMTimeRoundingMethod) -> CMTime](/documentation/coremedia/cmtimebasegettimewithtimescale(_:timescale:method:))
- [func CMTimebaseGetTimeAndRate(CMTimebase, timeOut: UnsafeMutablePointer<CMTime>?, rateOut: UnsafeMutablePointer<Float64>?) -> OSStatus](/documentation/coremedia/cmtimebasegettimeandrate(_:timeout:rateout:))
- [func CMTimebaseSetTime(CMTimebase, time: CMTime) -> OSStatus](/documentation/coremedia/cmtimebasesettime(_:time:))
- [func CMTimebaseSetSourceClock(CMTimebase, CMClock) -> OSStatus](/documentation/coremedia/cmtimebasesetsourceclock(_:_:))
- [func CMTimebaseSetSourceTimebase(CMTimebase, CMTimebase) -> OSStatus](/documentation/coremedia/cmtimebasesetsourcetimebase(_:_:))
- [func CMTimebaseSetAnchorTime(CMTimebase, timebaseTime: CMTime, immediateSourceTime: CMTime) -> OSStatus](/documentation/coremedia/cmtimebasesetanchortime(_:timebasetime:immediatesourcetime:))

### Getting and Setting the Time Rate

- [func CMTimebaseGetRate(CMTimebase) -> Float64](/documentation/coremedia/cmtimebasegetrate(_:))
- [func CMTimebaseGetEffectiveRate(CMTimebase) -> Float64](/documentation/coremedia/cmtimebasegeteffectiverate(_:))
- [func CMTimebaseSetRate(CMTimebase, rate: Float64) -> OSStatus](/documentation/coremedia/cmtimebasesetrate(_:rate:))
- [func CMTimebaseSetRateAndAnchorTime(CMTimebase, rate: Float64, anchorTime: CMTime, immediateSourceTime: CMTime) -> OSStatus](/documentation/coremedia/cmtimebasesetrateandanchortime(_:rate:anchortime:immediatesourcetime:))

### Interacting with Timers

- [func CMTimebaseAddTimer(CMTimebase, timer: CFRunLoopTimer, runloop: CFRunLoop) -> OSStatus](/documentation/coremedia/cmtimebaseaddtimer(_:timer:runloop:))
- [func CMTimebaseAddTimerDispatchSource(CMTimebase, timerSource: dispatch_source_t) -> OSStatus](/documentation/coremedia/cmtimebaseaddtimerdispatchsource(_:timersource:))
- [func CMTimebaseRemoveTimer(CMTimebase, timer: CFRunLoopTimer) -> OSStatus](/documentation/coremedia/cmtimebaseremovetimer(_:timer:))
- [func CMTimebaseRemoveTimerDispatchSource(CMTimebase, timerSource: dispatch_source_t) -> OSStatus](/documentation/coremedia/cmtimebaseremovetimerdispatchsource(_:timersource:))
- [func CMTimebaseSetTimerNextFireTime(CMTimebase, timer: CFRunLoopTimer, fireTime: CMTime, flags: UInt32) -> OSStatus](/documentation/coremedia/cmtimebasesettimernextfiretime(_:timer:firetime:flags:))
- [func CMTimebaseSetTimerToFireImmediately(CMTimebase, timer: CFRunLoopTimer) -> OSStatus](/documentation/coremedia/cmtimebasesettimertofireimmediately(_:timer:))
- [func CMTimebaseSetTimerDispatchSourceNextFireTime(CMTimebase, timerSource: dispatch_source_t, fireTime: CMTime, flags: UInt32) -> OSStatus](/documentation/coremedia/cmtimebasesettimerdispatchsourcenextfiretime(_:timersource:firetime:flags:))
- [func CMTimebaseSetTimerDispatchSourceToFireImmediately(CMTimebase, timerSource: dispatch_source_t) -> OSStatus](/documentation/coremedia/cmtimebasesettimerdispatchsourcetofireimmediately(_:timersource:))

### Pausing Time Notifications

- [func CMTimebaseNotificationBarrier(CMTimebase) -> OSStatus](/documentation/coremedia/cmtimebasenotificationbarrier(_:))

### Data Types

- [CMTimebase](/documentation/coremedia/cmtimebase)

#### Timebases

- [static let farFuture: CFAbsoluteTime](/documentation/coremedia/cmtimebase/farfuture)
- [static let veryLongTimeInterval: CFTimeInterval](/documentation/coremedia/cmtimebase/verylongtimeinterval)

#### Inspecting Timebases

- [var time: CMTime](/documentation/coremedia/cmtimebase/time)
- [var rate: Double](/documentation/coremedia/cmtimebase/rate)
- [var source: any CMSyncProtocol](/documentation/coremedia/cmtimebase/source)
- [var sourceClock: CMClock?](/documentation/coremedia/cmtimebase/sourceclock)
- [var sourceTimebase: CMTimebase?](/documentation/coremedia/cmtimebase/sourcetimebase)
- [var effectiveRate: Double](/documentation/coremedia/cmtimebase/effectiverate)
- [var timeAndRate: (time: CMTime, rate: Double)](/documentation/coremedia/cmtimebase/timeandrate)
- [var ultimateSourceClock: CMClock](/documentation/coremedia/cmtimebase/ultimatesourceclock)

#### Adding and Removing Timers

- [func addTimer(Timer, on: RunLoop) throws](/documentation/coremedia/cmtimebase/addtimer(_:on:))
- [func addTimer<T>(T) throws](/documentation/coremedia/cmtimebase/addtimer(_:))
- [func removeTimer(Timer) throws](/documentation/coremedia/cmtimebase/removetimer(_:)-4f6re)
- [func removeTimer<T>(T) throws](/documentation/coremedia/cmtimebase/removetimer(_:)-448o2)

#### Getting and Setting Time

- [func setTime(CMTime) throws](/documentation/coremedia/cmtimebase/settime(_:))
- [func time(withTimescale: CMTimeScale, rounding: CMTimeRoundingMethod) -> CMTime](/documentation/coremedia/cmtimebase/time(withtimescale:rounding:))

#### Getting and Setting the Timebase Rate

- [func setRate(Double) throws](/documentation/coremedia/cmtimebase/setrate(_:))
- [func setRateAndAnchorTime(rate: Double, anchorTime: CMTime, referenceTime: CMTime) throws](/documentation/coremedia/cmtimebase/setrateandanchortime(rate:anchortime:referencetime:))

#### Setting Timers

- [func setTimerNextFireTime(Timer, fireTime: CMTime) throws](/documentation/coremedia/cmtimebase/settimernextfiretime(_:firetime:)-13hjt)
- [func setTimerNextFireTime<T>(T, fireTime: CMTime) throws](/documentation/coremedia/cmtimebase/settimernextfiretime(_:firetime:)-2yvaa)
- [func setTimerToFireImmediately(Timer) throws](/documentation/coremedia/cmtimebase/settimertofireimmediately(_:)-9t3wi)
- [func setTimerToFireImmediately<T>(T) throws](/documentation/coremedia/cmtimebase/settimertofireimmediately(_:)-4903g)

#### Pausing Time Notifications

- [func notificationBarrier() throws](/documentation/coremedia/cmtimebase/notificationbarrier())

#### Setting the Anchor Time

- [func setAnchorTime(CMTime, referenceTime: CMTime) throws](/documentation/coremedia/cmtimebase/setanchortime(_:referencetime:))

#### Notifications

- [static let effectiveRateChanged: NSNotification.Name](/documentation/coremedia/cmtimebase/effectiveratechanged)
- [static let timeJumped: NSNotification.Name](/documentation/coremedia/cmtimebase/timejumped)

#### Constants

- [CMTimebase.Error](/documentation/coremedia/cmtimebase/error)

##### Constants

- [static let allocationFailed: NSError](/documentation/coremedia/cmtimebase/error/allocationfailed)
- [static let invalidParameter: NSError](/documentation/coremedia/cmtimebase/error/invalidparameter)
- [static let missingRequiredParameter: NSError](/documentation/coremedia/cmtimebase/error/missingrequiredparameter)
- [static let readOnly: NSError](/documentation/coremedia/cmtimebase/error/readonly)
- [static let timerIntervalTooShort: NSError](/documentation/coremedia/cmtimebase/error/timerintervaltooshort)
- [CMTimebase.NotificationKey](/documentation/coremedia/cmtimebase/notificationkey)

##### Notification Keys

- [static let eventTime: CMTimebase.NotificationKey](/documentation/coremedia/cmtimebase/notificationkey/eventtime)
- [static var typeID: CFTypeID](/documentation/coremedia/cmtimebase/typeid)

#### Deprecations

- [var master: any CMSyncProtocol](/documentation/coremedia/cmtimebase/master)
- [var masterClock: CMClock?](/documentation/coremedia/cmtimebase/masterclock)
- [var masterTimebase: CMTimebase?](/documentation/coremedia/cmtimebase/mastertimebase)
- [var ultimateMasterClock: CMClock](/documentation/coremedia/cmtimebase/ultimatemasterclock)

#### Initializers

- [init(referencing: CMTimebase)](/documentation/coremedia/cmtimebase/init(referencing:))

#### Type Aliases

- [CMTimebase.T](/documentation/coremedia/cmtimebase/t)

#### Default Implementations

- [CMSyncProtocol Implementations](/documentation/coremedia/cmtimebase/cmsyncprotocol-implementations)

##### Instance Properties

- [var time: CMTime](/documentation/coremedia/cmtimebase/time)
- [CMSync](/documentation/coremedia/cmsync)

#### Constants

- [CMSync.Error](/documentation/coremedia/cmsync/error)

##### Constants

- [static let allocationFailed: NSError](/documentation/coremedia/cmsync/error/allocationfailed)
- [static let invalidParameter: NSError](/documentation/coremedia/cmsync/error/invalidparameter)
- [static let missingRequiredParameter: NSError](/documentation/coremedia/cmsync/error/missingrequiredparameter)
- [static let rateMustBeNonZero: NSError](/documentation/coremedia/cmsync/error/ratemustbenonzero)
- [CMSyncProtocol](/documentation/coremedia/cmsyncprotocol)

#### Getting the Time

- [var time: CMTime](/documentation/coremedia/cmsyncprotocol/time)

#### Converting Time

- [func convertTime<T>(CMTime, to: T) -> CMTime](/documentation/coremedia/cmsyncprotocol/converttime(_:to:))

#### Getting the Time Rate

- [func rate<T>(relativeTo: T) -> Double](/documentation/coremedia/cmsyncprotocol/rate(relativeto:))
- [func rateAndAnchorTime<T>(relativeTo: T) throws -> (rate: Double, anchorTime: CMTime, referenceTime: CMTime)](/documentation/coremedia/cmsyncprotocol/rateandanchortime(relativeto:))

#### Determining Time Drift

- [func mightDrift<T>(relativeTo: T) -> Bool](/documentation/coremedia/cmsyncprotocol/mightdrift(relativeto:))

### Timebase Errors

- [var kCMTimebaseError_MissingRequiredParameter: OSStatus](/documentation/coremedia/kcmtimebaseerror_missingrequiredparameter)
- [var kCMTimebaseError_InvalidParameter: OSStatus](/documentation/coremedia/kcmtimebaseerror_invalidparameter)
- [var kCMTimebaseError_AllocationFailed: OSStatus](/documentation/coremedia/kcmtimebaseerror_allocationfailed)
- [var kCMTimebaseError_TimerIntervalTooShort: OSStatus](/documentation/coremedia/kcmtimebaseerror_timerintervaltooshort)
- [var kCMTimebaseError_ReadOnly: OSStatus](/documentation/coremedia/kcmtimebaseerror_readonly)

### Constants

- [func CMTimebaseGetTypeID() -> CFTypeID](/documentation/coremedia/cmtimebasegettypeid())

### Notifications

- [let kCMTimebaseNotificationKey_EventTime: CFString](/documentation/coremedia/kcmtimebasenotificationkey_eventtime)

### Deprecations

- [func CMTimebaseSetRateAndAnchorTime(CMTimebase, rate: Double, anchorTime: CMTime, immediateMasterTime: CMTime)](/documentation/coremedia/cmtimebasesetrateandanchortime(_:rate:anchortime:immediatemastertime:))
- [func CMTimebaseGetMasterTimebase(CMTimebase) -> CMTimebase?](/documentation/coremedia/cmtimebasegetmastertimebase(_:))
- [func CMTimebaseGetMasterClock(CMTimebase) -> CMClock?](/documentation/coremedia/cmtimebasegetmasterclock(_:))
- [func CMTimebaseGetMaster(CMTimebase) -> CMClockOrTimebase?](/documentation/coremedia/cmtimebasegetmaster(_:))
- [func CMTimebaseGetUltimateMasterClock(CMTimebase) -> CMClock?](/documentation/coremedia/cmtimebasegetultimatemasterclock(_:))
- [func CMTimebaseSetMasterClock(CMTimebase, CMClock) -> OSStatus](/documentation/coremedia/cmtimebasesetmasterclock(_:_:))
- [func CMTimebaseSetMasterTimebase(CMTimebase, CMTimebase) -> OSStatus](/documentation/coremedia/cmtimebasesetmastertimebase(_:_:))
- [func CMTimebaseSetAnchorTime(CMTimebase, timebaseTime: CMTime, immediateMasterTime: CMTime)](/documentation/coremedia/cmtimebasesetanchortime(_:timebasetime:immediatemastertime:))
- [func CMTimebaseCopyMaster(CMTimebase) -> CMClockOrTimebase](/documentation/coremedia/cmtimebasecopymaster(_:))
- [func CMTimebaseCopyMasterClock(CMTimebase) -> CMClock?](/documentation/coremedia/cmtimebasecopymasterclock(_:))
- [func CMTimebaseCopyMasterTimebase(CMTimebase) -> CMTimebase?](/documentation/coremedia/cmtimebasecopymastertimebase(_:))
- [func CMTimebaseCopyUltimateMasterClock(CMTimebase) -> CMClock](/documentation/coremedia/cmtimebasecopyultimatemasterclock(_:))
- [func CMTimebaseCreateWithMasterClock(allocator: CFAllocator?, masterClock: CMClock, timebaseOut: UnsafeMutablePointer<CMTimebase?>) -> OSStatus](/documentation/coremedia/cmtimebasecreatewithmasterclock(allocator:masterclock:timebaseout:))
- [func CMTimebaseCreateWithMasterTimebase(allocator: CFAllocator?, masterTimebase: CMTimebase, timebaseOut: UnsafeMutablePointer<CMTimebase?>) -> OSStatus](/documentation/coremedia/cmtimebasecreatewithmastertimebase(allocator:mastertimebase:timebaseout:))

## Text Markup

- [CMTextMarkup](/documentation/coremedia/cmtextmarkup)

### Fonts

- [let kCMTextMarkupAttribute_FontFamilyName: CFString](/documentation/coremedia/kcmtextmarkupattribute_fontfamilyname)
- [let kCMTextMarkupAttribute_GenericFontFamilyName: CFString](/documentation/coremedia/kcmtextmarkupattribute_genericfontfamilyname)

#### Font Names

- [let kCMTextMarkupGenericFontName_Default: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_default)
- [let kCMTextMarkupGenericFontName_Serif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_serif)
- [let kCMTextMarkupGenericFontName_SansSerif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_sansserif)
- [let kCMTextMarkupGenericFontName_Monospace: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_monospace)
- [let kCMTextMarkupGenericFontName_MonospaceSerif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_monospaceserif)
- [let kCMTextMarkupGenericFontName_MonospaceSansSerif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_monospacesansserif)
- [let kCMTextMarkupGenericFontName_ProportionalSerif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_proportionalserif)
- [let kCMTextMarkupGenericFontName_ProportionalSansSerif: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_proportionalsansserif)
- [let kCMTextMarkupGenericFontName_SmallCapital: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_smallcapital)
- [let kCMTextMarkupGenericFontName_Casual: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_casual)
- [let kCMTextMarkupGenericFontName_Cursive: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_cursive)
- [let kCMTextMarkupGenericFontName_Fantasy: CFString](/documentation/coremedia/kcmtextmarkupgenericfontname_fantasy)
- [let kCMTextMarkupAttribute_BaseFontSizePercentageRelativeToVideoHeight: CFString](/documentation/coremedia/kcmtextmarkupattribute_basefontsizepercentagerelativetovideoheight)
- [let kCMTextMarkupAttribute_RelativeFontSize: CFString](/documentation/coremedia/kcmtextmarkupattribute_relativefontsize)

### Styles

- [let kCMTextMarkupAttribute_BoldStyle: CFString](/documentation/coremedia/kcmtextmarkupattribute_boldstyle)
- [let kCMTextMarkupAttribute_ItalicStyle: CFString](/documentation/coremedia/kcmtextmarkupattribute_italicstyle)
- [let kCMTextMarkupAttribute_UnderlineStyle: CFString](/documentation/coremedia/kcmtextmarkupattribute_underlinestyle)
- [let kCMTextMarkupAttribute_CharacterEdgeStyle: CFString](/documentation/coremedia/kcmtextmarkupattribute_characteredgestyle)

#### Edge Styles

- [let kCMTextMarkupCharacterEdgeStyle_None: CFString](/documentation/coremedia/kcmtextmarkupcharacteredgestyle_none)
- [let kCMTextMarkupCharacterEdgeStyle_Raised: CFString](/documentation/coremedia/kcmtextmarkupcharacteredgestyle_raised)
- [let kCMTextMarkupCharacterEdgeStyle_Depressed: CFString](/documentation/coremedia/kcmtextmarkupcharacteredgestyle_depressed)
- [let kCMTextMarkupCharacterEdgeStyle_Uniform: CFString](/documentation/coremedia/kcmtextmarkupcharacteredgestyle_uniform)
- [let kCMTextMarkupCharacterEdgeStyle_DropShadow: CFString](/documentation/coremedia/kcmtextmarkupcharacteredgestyle_dropshadow)

### Colors

- [let kCMTextMarkupAttribute_ForegroundColorARGB: CFString](/documentation/coremedia/kcmtextmarkupattribute_foregroundcolorargb)
- [let kCMTextMarkupAttribute_BackgroundColorARGB: CFString](/documentation/coremedia/kcmtextmarkupattribute_backgroundcolorargb)
- [let kCMTextMarkupAttribute_CharacterBackgroundColorARGB: CFString](/documentation/coremedia/kcmtextmarkupattribute_characterbackgroundcolorargb)

### Layout

- [let kCMTextMarkupAttribute_VerticalLayout: CFString](/documentation/coremedia/kcmtextmarkupattribute_verticallayout)

#### Layouts

- [let kCMTextVerticalLayout_LeftToRight: CFString](/documentation/coremedia/kcmtextverticallayout_lefttoright)
- [let kCMTextVerticalLayout_RightToLeft: CFString](/documentation/coremedia/kcmtextverticallayout_righttoleft)
- [let kCMTextMarkupAttribute_Alignment: CFString](/documentation/coremedia/kcmtextmarkupattribute_alignment)

#### Alignment Types

- [let kCMTextMarkupAlignmentType_Start: CFString](/documentation/coremedia/kcmtextmarkupalignmenttype_start)
- [let kCMTextMarkupAlignmentType_Middle: CFString](/documentation/coremedia/kcmtextmarkupalignmenttype_middle)
- [let kCMTextMarkupAlignmentType_End: CFString](/documentation/coremedia/kcmtextmarkupalignmenttype_end)
- [let kCMTextMarkupAlignmentType_Left: CFString](/documentation/coremedia/kcmtextmarkupalignmenttype_left)
- [let kCMTextMarkupAlignmentType_Right: CFString](/documentation/coremedia/kcmtextmarkupalignmenttype_right)
- [let kCMTextMarkupAttribute_TextPositionPercentageRelativeToWritingDirection: CFString](/documentation/coremedia/kcmtextmarkupattribute_textpositionpercentagerelativetowritingdirection)
- [let kCMTextMarkupAttribute_OrthogonalLinePositionPercentageRelativeToWritingDirection: CFString](/documentation/coremedia/kcmtextmarkupattribute_orthogonallinepositionpercentagerelativetowritingdirection)
- [let kCMTextMarkupAttribute_WritingDirectionSizePercentage: CFString](/documentation/coremedia/kcmtextmarkupattribute_writingdirectionsizepercentage)

## Metadata

- [CMMetadata](/documentation/coremedia/cmmetadata)

### Creating Metadata Identifiers

- [func CMMetadataCreateIdentifierForKeyAndKeySpace(allocator: CFAllocator?, key: CFTypeRef, keySpace: CFString, identifierOut: UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/coremedia/cmmetadatacreateidentifierforkeyandkeyspace(allocator:key:keyspace:identifierout:))
- [func CMMetadataCreateKeyFromIdentifier(allocator: CFAllocator?, identifier: CFString, keyOut: UnsafeMutablePointer<CFTypeRef?>) -> OSStatus](/documentation/coremedia/cmmetadatacreatekeyfromidentifier(allocator:identifier:keyout:))
- [func CMMetadataCreateKeyFromIdentifierAsCFData(allocator: CFAllocator?, identifier: CFString, keyOut: UnsafeMutablePointer<CFData?>) -> OSStatus](/documentation/coremedia/cmmetadatacreatekeyfromidentifierascfdata(allocator:identifier:keyout:))
- [func CMMetadataCreateKeySpaceFromIdentifier(allocator: CFAllocator?, identifier: CFString, keySpaceOut: UnsafeMutablePointer<CFString?>) -> OSStatus](/documentation/coremedia/cmmetadatacreatekeyspacefromidentifier(allocator:identifier:keyspaceout:))

### Registering Metadata

- [func CMMetadataDataTypeRegistryRegisterDataType(CFString, description: CFString, conformingDataTypes: CFArray) -> OSStatus](/documentation/coremedia/cmmetadatadatatyperegistryregisterdatatype(_:description:conformingdatatypes:))

### Inspecting Metadata

- [func CMMetadataDataTypeRegistryDataTypeIsRegistered(CFString) -> Bool](/documentation/coremedia/cmmetadatadatatyperegistrydatatypeisregistered(_:))
- [func CMMetadataDataTypeRegistryGetDataTypeDescription(CFString) -> CFString](/documentation/coremedia/cmmetadatadatatyperegistrygetdatatypedescription(_:))
- [func CMMetadataDataTypeRegistryGetConformingDataTypes(CFString) -> CFArray](/documentation/coremedia/cmmetadatadatatyperegistrygetconformingdatatypes(_:))
- [func CMMetadataDataTypeRegistryDataTypeConformsToDataType(CFString, conformsTo: CFString) -> Bool](/documentation/coremedia/cmmetadatadatatyperegistrydatatypeconformstodatatype(_:conformsto:))
- [func CMMetadataDataTypeRegistryDataTypeIsBaseDataType(CFString) -> Bool](/documentation/coremedia/cmmetadatadatatyperegistrydatatypeisbasedatatype(_:))
- [func CMMetadataDataTypeRegistryGetBaseDataTypeForConformingDataType(CFString) -> CFString](/documentation/coremedia/cmmetadatadatatyperegistrygetbasedatatypeforconformingdatatype(_:))
- [func CMMetadataDataTypeRegistryGetBaseDataTypes() -> CFArray?](/documentation/coremedia/cmmetadatadatatyperegistrygetbasedatatypes())

### Constants

- [Metadata Identifier Error Codes](/documentation/coremedia/metadata-identifier-errors)

#### Constants

- [var kCMMetadataIdentifierError_AllocationFailed: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_allocationfailed)
- [var kCMMetadataIdentifierError_BadIdentifier: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badidentifier)
- [var kCMMetadataIdentifierError_BadKey: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badkey)
- [var kCMMetadataIdentifierError_BadKeyLength: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badkeylength)
- [var kCMMetadataIdentifierError_BadKeySpace: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badkeyspace)
- [var kCMMetadataIdentifierError_BadKeyType: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badkeytype)
- [var kCMMetadataIdentifierError_BadNumberKey: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_badnumberkey)
- [var kCMMetadataIdentifierError_NoKeyValueAvailable: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_nokeyvalueavailable)
- [var kCMMetadataIdentifierError_RequiredParameterMissing: OSStatus](/documentation/coremedia/kcmmetadataidentifiererror_requiredparametermissing)
- [Metadata Registry Error Codes](/documentation/coremedia/metadata-registry-errors)

#### Constants

- [var kCMMetadataDataTypeRegistryError_AllocationFailed: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_allocationfailed)
- [var kCMMetadataDataTypeRegistryError_BadDataTypeIdentifier: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_baddatatypeidentifier)
- [var kCMMetadataDataTypeRegistryError_DataTypeAlreadyRegistered: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_datatypealreadyregistered)
- [var kCMMetadataDataTypeRegistryError_MultipleConformingBaseTypes: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_multipleconformingbasetypes)
- [var kCMMetadataDataTypeRegistryError_RequiredParameterMissing: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_requiredparametermissing)
- [var kCMMetadataDataTypeRegistryError_RequiresConformingBaseType: OSStatus](/documentation/coremedia/kcmmetadatadatatyperegistryerror_requiresconformingbasetype)
- [Metadata Identifier Keyspaces](/documentation/coremedia/metadata-identifier-keyspaces)

#### Constants

- [let kCMMetadataKeySpace_QuickTimeUserData: CFString](/documentation/coremedia/kcmmetadatakeyspace_quicktimeuserdata)
- [let kCMMetadataKeySpace_ISOUserData: CFString](/documentation/coremedia/kcmmetadatakeyspace_isouserdata)
- [let kCMMetadataKeySpace_QuickTimeMetadata: CFString](/documentation/coremedia/kcmmetadatakeyspace_quicktimemetadata)
- [let kCMMetadataKeySpace_iTunes: CFString](/documentation/coremedia/kcmmetadatakeyspace_itunes)
- [let kCMMetadataKeySpace_ID3: CFString](/documentation/coremedia/kcmmetadatakeyspace_id3)
- [let kCMMetadataKeySpace_Icy: CFString](/documentation/coremedia/kcmmetadatakeyspace_icy)
- [let kCMMetadataKeySpace_HLSDateRange: CFString](/documentation/coremedia/kcmmetadatakeyspace_hlsdaterange)
- [Metadata Identifiers](/documentation/coremedia/metadata-identifiers)

#### Constants

- [let kCMMetadataIdentifier_QuickTimeMetadataLocation_ISO6709: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatalocation_iso6709)
- [let kCMMetadataIdentifier_QuickTimeMetadataDirection_Facing: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatadirection_facing)
- [let kCMMetadataIdentifier_QuickTimeMetadataPreferredAffineTransform: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatapreferredaffinetransform)
- [let kCMMetadataIdentifier_QuickTimeMetadataVideoOrientation: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatavideoorientation)
- [let kCMMetadataIdentifier_QuickTimeMetadataLivePhotoStillImageTransformReferenceDimensions: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatalivephotostillimagetransformreferencedimensions)
- [let kCMMetadataIdentifier_QuickTimeMetadataLivePhotoStillImageTransform: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatalivephotostillimagetransform)
- [Metadata Base Data Types](/documentation/coremedia/metadata-base-data-types)

#### Constants

- [let kCMMetadataBaseDataType_RawData: CFString](/documentation/coremedia/kcmmetadatabasedatatype_rawdata)
- [let kCMMetadataBaseDataType_UTF8: CFString](/documentation/coremedia/kcmmetadatabasedatatype_utf8)
- [let kCMMetadataBaseDataType_UTF16: CFString](/documentation/coremedia/kcmmetadatabasedatatype_utf16)
- [let kCMMetadataBaseDataType_GIF: CFString](/documentation/coremedia/kcmmetadatabasedatatype_gif)
- [let kCMMetadataBaseDataType_JPEG: CFString](/documentation/coremedia/kcmmetadatabasedatatype_jpeg)
- [let kCMMetadataBaseDataType_PNG: CFString](/documentation/coremedia/kcmmetadatabasedatatype_png)
- [let kCMMetadataBaseDataType_BMP: CFString](/documentation/coremedia/kcmmetadatabasedatatype_bmp)
- [let kCMMetadataBaseDataType_Float32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_float32)
- [let kCMMetadataBaseDataType_Float64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_float64)
- [let kCMMetadataBaseDataType_SInt8: CFString](/documentation/coremedia/kcmmetadatabasedatatype_sint8)
- [let kCMMetadataBaseDataType_SInt16: CFString](/documentation/coremedia/kcmmetadatabasedatatype_sint16)
- [let kCMMetadataBaseDataType_SInt32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_sint32)
- [let kCMMetadataBaseDataType_SInt64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_sint64)
- [let kCMMetadataBaseDataType_UInt8: CFString](/documentation/coremedia/kcmmetadatabasedatatype_uint8)
- [let kCMMetadataBaseDataType_UInt16: CFString](/documentation/coremedia/kcmmetadatabasedatatype_uint16)
- [let kCMMetadataBaseDataType_UInt32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_uint32)
- [let kCMMetadataBaseDataType_UInt64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_uint64)
- [let kCMMetadataBaseDataType_PointF32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_pointf32)
- [let kCMMetadataBaseDataType_DimensionsF32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_dimensionsf32)
- [let kCMMetadataBaseDataType_RectF32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_rectf32)
- [let kCMMetadataBaseDataType_AffineTransformF64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_affinetransformf64)
- [let kCMMetadataBaseDataType_PerspectiveTransformF64: CFString](/documentation/coremedia/kcmmetadatabasedatatype_perspectivetransformf64)
- [let kCMMetadataBaseDataType_PolygonF32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_polygonf32)
- [let kCMMetadataBaseDataType_PolylineF32: CFString](/documentation/coremedia/kcmmetadatabasedatatype_polylinef32)
- [let kCMMetadataBaseDataType_JSON: CFString](/documentation/coremedia/kcmmetadatabasedatatype_json)
- [Metadata Data Types](/documentation/coremedia/metadata-data-types)

#### Constants

- [let kCMMetadataDataType_QuickTimeMetadataLocation_ISO6709: CFString](/documentation/coremedia/kcmmetadatadatatype_quicktimemetadatalocation_iso6709)
- [let kCMMetadataDataType_QuickTimeMetadataDirection: CFString](/documentation/coremedia/kcmmetadatadatatype_quicktimemetadatadirection)
- [CMTag](/documentation/coremedia/cmtag-api)

### Types

- [CMTag](/documentation/coremedia/cmtag-swift.class)

#### Creating Tags

- [static func channelID(Int64) -> CMTypedTag<Int64>](/documentation/coremedia/cmtag-swift.class/channelid(_:))
- [static func mediaSubType(CMFormatDescription.MediaSubType) -> CMTypedTag<CMFormatDescription.MediaSubType>](/documentation/coremedia/cmtag-swift.class/mediasubtype(_:))
- [static func mediaType(CMFormatDescription.MediaType) -> CMTypedTag<CMFormatDescription.MediaType>](/documentation/coremedia/cmtag-swift.class/mediatype(_:))
- [static func packingType(CMPackingType) -> CMTypedTag<CMPackingType>](/documentation/coremedia/cmtag-swift.class/packingtype(_:))
- [static func pixelFormat(OSType) -> CMTypedTag<OSType>](/documentation/coremedia/cmtag-swift.class/pixelformat(_:))
- [static func projectionType(CMProjectionType) -> CMTypedTag<CMProjectionType>](/documentation/coremedia/cmtag-swift.class/projectiontype(_:))
- [static func stereoView(CMStereoViewComponents) -> CMTypedTag<CMStereoViewComponents>](/documentation/coremedia/cmtag-swift.class/stereoview(_:))
- [static func stereoViewInterpretation(CMStereoViewInterpretationOptions) -> CMTypedTag<CMStereoViewInterpretationOptions>](/documentation/coremedia/cmtag-swift.class/stereoviewinterpretation(_:))
- [static func trackID(CMPersistentTrackID) -> CMTypedTag<CMPersistentTrackID>](/documentation/coremedia/cmtag-swift.class/trackid(_:))
- [static func videoLayerID(Int64) -> CMTypedTag<Int64>](/documentation/coremedia/cmtag-swift.class/videolayerid(_:))
- [init(rawCategory: CMTag.RawCategory, rawTagValue: CMTag.Value)](/documentation/coremedia/cmtag-swift.class/init(rawcategory:rawtagvalue:))

#### Inspecting Tags

- [let rawCategory: CMTag.RawCategory](/documentation/coremedia/cmtag-swift.class/rawcategory-swift.property)
- [let rawTagValue: CMTag.Value](/documentation/coremedia/cmtag-swift.class/rawtagvalue)
- [func value<T>(onlyIfMatching: CMTypedTag<T>.Category) -> T?](/documentation/coremedia/cmtag-swift.class/value(onlyifmatching:))

#### Wrapped Values

- [CMTag.Value](/documentation/coremedia/cmtag-swift.class/value)

##### Value Types

- [case int64(Int64)](/documentation/coremedia/cmtag-swift.class/value/int64(_:))
- [case float64(Float64)](/documentation/coremedia/cmtag-swift.class/value/float64(_:))
- [case flags(UInt64)](/documentation/coremedia/cmtag-swift.class/value/flags(_:))
- [case osType(OSType)](/documentation/coremedia/cmtag-swift.class/value/ostype(_:))

#### Type Aliases

- [CMTag.RawCategory](/documentation/coremedia/cmtag-swift.class/rawcategory-swift.typealias)

### Constants

- [Tag Values](/documentation/coremedia/tag-values)
- [CMTag](/documentation/coremedia/cmtag-swift.class)

### Creating Tags

- [static func channelID(Int64) -> CMTypedTag<Int64>](/documentation/coremedia/cmtag-swift.class/channelid(_:))
- [static func mediaSubType(CMFormatDescription.MediaSubType) -> CMTypedTag<CMFormatDescription.MediaSubType>](/documentation/coremedia/cmtag-swift.class/mediasubtype(_:))
- [static func mediaType(CMFormatDescription.MediaType) -> CMTypedTag<CMFormatDescription.MediaType>](/documentation/coremedia/cmtag-swift.class/mediatype(_:))
- [static func packingType(CMPackingType) -> CMTypedTag<CMPackingType>](/documentation/coremedia/cmtag-swift.class/packingtype(_:))
- [static func pixelFormat(OSType) -> CMTypedTag<OSType>](/documentation/coremedia/cmtag-swift.class/pixelformat(_:))
- [static func projectionType(CMProjectionType) -> CMTypedTag<CMProjectionType>](/documentation/coremedia/cmtag-swift.class/projectiontype(_:))
- [static func stereoView(CMStereoViewComponents) -> CMTypedTag<CMStereoViewComponents>](/documentation/coremedia/cmtag-swift.class/stereoview(_:))
- [static func stereoViewInterpretation(CMStereoViewInterpretationOptions) -> CMTypedTag<CMStereoViewInterpretationOptions>](/documentation/coremedia/cmtag-swift.class/stereoviewinterpretation(_:))
- [static func trackID(CMPersistentTrackID) -> CMTypedTag<CMPersistentTrackID>](/documentation/coremedia/cmtag-swift.class/trackid(_:))
- [static func videoLayerID(Int64) -> CMTypedTag<Int64>](/documentation/coremedia/cmtag-swift.class/videolayerid(_:))
- [init(rawCategory: CMTag.RawCategory, rawTagValue: CMTag.Value)](/documentation/coremedia/cmtag-swift.class/init(rawcategory:rawtagvalue:))

### Inspecting Tags

- [let rawCategory: CMTag.RawCategory](/documentation/coremedia/cmtag-swift.class/rawcategory-swift.property)
- [let rawTagValue: CMTag.Value](/documentation/coremedia/cmtag-swift.class/rawtagvalue)
- [func value<T>(onlyIfMatching: CMTypedTag<T>.Category) -> T?](/documentation/coremedia/cmtag-swift.class/value(onlyifmatching:))

### Wrapped Values

- [CMTag.Value](/documentation/coremedia/cmtag-swift.class/value)

#### Value Types

- [case int64(Int64)](/documentation/coremedia/cmtag-swift.class/value/int64(_:))
- [case float64(Float64)](/documentation/coremedia/cmtag-swift.class/value/float64(_:))
- [case flags(UInt64)](/documentation/coremedia/cmtag-swift.class/value/flags(_:))
- [case osType(OSType)](/documentation/coremedia/cmtag-swift.class/value/ostype(_:))

### Type Aliases

- [CMTag.RawCategory](/documentation/coremedia/cmtag-swift.class/rawcategory-swift.typealias)
- [CMTypedTag](/documentation/coremedia/cmtypedtag)

### Creating Typed Tags

- [init(category: CMTypedTag<TypedValue>.Category, value: TypedValue)](/documentation/coremedia/cmtypedtag/init(category:value:))

### Inspecting Typed Tags

- [let category: CMTypedTag<TypedValue>.Category](/documentation/coremedia/cmtypedtag/category-swift.property)
- [var value: TypedValue](/documentation/coremedia/cmtypedtag/value)

### Typed Tag Categories

- [CMTypedTag.Category](/documentation/coremedia/cmtypedtag/category-swift.struct)

#### Creating Typed Categories

- [static var channelID: CMTypedTag<Int64>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/channelid)
- [static var mediaSubType: CMTypedTag<CMFormatDescription.MediaSubType>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/mediasubtype)
- [static var mediaType: CMTypedTag<CMFormatDescription.MediaType>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/mediatype)
- [static var packingType: CMTypedTag<CMPackingType>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/packingtype)
- [static var pixelFormat: CMTypedTag<OSType>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/pixelformat)
- [static var projectionType: CMTypedTag<CMProjectionType>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/projectiontype)
- [static var stereoView: CMTypedTag<CMStereoViewComponents>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/stereoview)
- [static var stereoViewInterpretation: CMTypedTag<CMStereoViewInterpretationOptions>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/stereoviewinterpretation)
- [static var trackID: CMTypedTag<CMPersistentTrackID>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/trackid)
- [static var videoLayerID: CMTypedTag<Int64>.Category](/documentation/coremedia/cmtypedtag/category-swift.struct/videolayerid)

#### Getting Raw Categories

- [let rawCategory: CMTypedTag<TypedValue>.RawCategory](/documentation/coremedia/cmtypedtag/category-swift.struct/rawcategory)

#### Transforming Tag Values

- [func tagValue(for: TypedValue) -> CMTag.Value](/documentation/coremedia/cmtypedtag/category-swift.struct/tagvalue(for:))
- [func value(for: CMTag.Value) -> TypedValue?](/documentation/coremedia/cmtypedtag/category-swift.struct/value(for:))

#### Initializers

- [init(rawCategory: CMTypedTag<TypedValue>.RawCategory, valueForTagValue: (CMTag.Value) -> TypedValue?, tagValueForValue: (TypedValue) -> CMTag.Value)](/documentation/coremedia/cmtypedtag/category-swift.struct/init(rawcategory:valuefortagvalue:tagvalueforvalue:))
- [CMTagCollection](/documentation/coremedia/cmtagcollection)
- [CMProjectionType](/documentation/coremedia/cmprojectiontype)

### Projection Surfaces

- [case rectangular](/documentation/coremedia/cmprojectiontype/rectangular)
- [case equirectangular](/documentation/coremedia/cmprojectiontype/equirectangular)
- [case halfEquirectangular](/documentation/coremedia/cmprojectiontype/halfequirectangular)
- [case fisheye](/documentation/coremedia/cmprojectiontype/fisheye)

### Enumeration Cases

- [case parametricImmersive](/documentation/coremedia/cmprojectiontype/parametricimmersive)

### Initializers

- [init?(rawValue: UInt64)](/documentation/coremedia/cmprojectiontype/init(rawvalue:))
- [CMStereoViewComponents](/documentation/coremedia/cmstereoviewcomponents)

### Eye Layer

- [static var leftEye: CMStereoViewComponents](/documentation/coremedia/cmstereoviewcomponents/lefteye)
- [static var rightEye: CMStereoViewComponents](/documentation/coremedia/cmstereoviewcomponents/righteye)

### Initializers

- [init(rawValue: UInt64)](/documentation/coremedia/cmstereoviewcomponents/init(rawvalue:))
- [CMStereoViewInterpretationOptions](/documentation/coremedia/cmstereoviewinterpretationoptions)

### Stereo View Options

- [static var additionalViews: CMStereoViewInterpretationOptions](/documentation/coremedia/cmstereoviewinterpretationoptions/additionalviews)
- [static var stereoOrderReversed: CMStereoViewInterpretationOptions](/documentation/coremedia/cmstereoviewinterpretationoptions/stereoorderreversed)

### Initializers

- [init(rawValue: UInt64)](/documentation/coremedia/cmstereoviewinterpretationoptions/init(rawvalue:))
- [CMPackingType](/documentation/coremedia/cmpackingtype)

### Frame Arrangement

- [case none](/documentation/coremedia/cmpackingtype/none)
- [case sideBySide](/documentation/coremedia/cmpackingtype/sidebyside)
- [case overUnder](/documentation/coremedia/cmpackingtype/overunder)

### Initializers

- [init?(rawValue: UInt64)](/documentation/coremedia/cmpackingtype/init(rawvalue:))

## Queues

- [CMSimpleQueue](/documentation/coremedia/cmsimplequeue-api)

### Creating a Queue

- [func CMSimpleQueueCreate(allocator: CFAllocator?, capacity: Int32, queueOut: UnsafeMutablePointer<CMSimpleQueue?>) -> OSStatus](/documentation/coremedia/cmsimplequeuecreate(allocator:capacity:queueout:))

### Managing Queues

- [func CMSimpleQueueEnqueue(CMSimpleQueue, element: UnsafeRawPointer) -> OSStatus](/documentation/coremedia/cmsimplequeueenqueue(_:element:))
- [func CMSimpleQueueDequeue(CMSimpleQueue) -> UnsafeRawPointer?](/documentation/coremedia/cmsimplequeuedequeue(_:))
- [func CMSimpleQueueReset(CMSimpleQueue) -> OSStatus](/documentation/coremedia/cmsimplequeuereset(_:))

### Inspecting Queues

- [func CMSimpleQueueGetHead(CMSimpleQueue) -> UnsafeRawPointer?](/documentation/coremedia/cmsimplequeuegethead(_:))
- [func CMSimpleQueueGetCapacity(CMSimpleQueue) -> Int32](/documentation/coremedia/cmsimplequeuegetcapacity(_:))
- [func CMSimpleQueueGetCount(CMSimpleQueue) -> Int32](/documentation/coremedia/cmsimplequeuegetcount(_:))

### Accessing the Type Identifier

- [func CMSimpleQueueGetTypeID() -> CFTypeID](/documentation/coremedia/cmsimplequeuegettypeid())

### Data Types

- [CMSimpleQueue](/documentation/coremedia/cmsimplequeue)

#### Managing Queues

- [func enqueue(UnsafeRawPointer) throws](/documentation/coremedia/cmsimplequeue/enqueue(_:))
- [func dequeue() -> UnsafeRawPointer?](/documentation/coremedia/cmsimplequeue/dequeue())
- [func reset() throws](/documentation/coremedia/cmsimplequeue/reset())

#### Inspecting Queues

- [var head: UnsafeRawPointer?](/documentation/coremedia/cmsimplequeue/head)
- [var capacity: Int](/documentation/coremedia/cmsimplequeue/capacity)
- [var count: Int](/documentation/coremedia/cmsimplequeue/count)
- [var fullness: Float](/documentation/coremedia/cmsimplequeue/fullness)

#### Accessing the Type Identifier

- [static var typeID: CFTypeID](/documentation/coremedia/cmsimplequeue/typeid)

#### Errors

- [CMSimpleQueue.Error](/documentation/coremedia/cmsimplequeue/error)

##### Errors

- [static let allocationFailed: NSError](/documentation/coremedia/cmsimplequeue/error/allocationfailed)
- [static let queueIsFull: NSError](/documentation/coremedia/cmsimplequeue/error/queueisfull)
- [static let parameterOutOfRange: NSError](/documentation/coremedia/cmsimplequeue/error/parameteroutofrange)
- [static let requiredParameterMissing: NSError](/documentation/coremedia/cmsimplequeue/error/requiredparametermissing)

#### Initializers

- [init(referencing: CMSimpleQueue)](/documentation/coremedia/cmsimplequeue/init(referencing:))

#### Type Aliases

- [CMSimpleQueue.T](/documentation/coremedia/cmsimplequeue/t)

### Errors

- [Simple Queue Error Codes](/documentation/coremedia/simple-queue-errors)

#### Constants

- [var kCMSimpleQueueError_AllocationFailed: OSStatus](/documentation/coremedia/kcmsimplequeueerror_allocationfailed)
- [var kCMSimpleQueueError_QueueIsFull: OSStatus](/documentation/coremedia/kcmsimplequeueerror_queueisfull)
- [var kCMSimpleQueueError_ParameterOutOfRange: OSStatus](/documentation/coremedia/kcmsimplequeueerror_parameteroutofrange)
- [var kCMSimpleQueueError_RequiredParameterMissing: OSStatus](/documentation/coremedia/kcmsimplequeueerror_requiredparametermissing)
- [CMBufferQueue](/documentation/coremedia/cmbufferqueue-api)

### Creating a Queue

- [func CMBufferQueueCreateWithHandlers(CFAllocator?, CMItemCount, OpaquePointer, UnsafeMutablePointer<CMBufferQueue?>) -> OSStatus](/documentation/coremedia/cmbufferqueuecreatewithhandlers(_:_:_:_:))
- [func CMBufferQueueCreate(allocator: CFAllocator?, capacity: CMItemCount, callbacks: UnsafePointer<CMBufferCallbacks>, queueOut: UnsafeMutablePointer<CMBufferQueue?>) -> OSStatus](/documentation/coremedia/cmbufferqueuecreate(allocator:capacity:callbacks:queueout:))
- [CMBufferCallbacks](/documentation/coremedia/cmbuffercallbacks)

#### Properties

- [var compare: CMBufferCompareCallback?](/documentation/coremedia/cmbuffercallbacks/compare)
- [CMBufferCompareCallback](/documentation/coremedia/cmbuffercomparecallback)
- [CMBufferGetBooleanCallback](/documentation/coremedia/cmbuffergetbooleancallback)
- [CMBufferGetTimeCallback](/documentation/coremedia/cmbuffergettimecallback)
- [var dataBecameReadyNotification: Unmanaged<CFString>?](/documentation/coremedia/cmbuffercallbacks/databecamereadynotification)
- [var getDecodeTimeStamp: CMBufferGetTimeCallback?](/documentation/coremedia/cmbuffercallbacks/getdecodetimestamp)
- [var getDuration: CMBufferGetTimeCallback](/documentation/coremedia/cmbuffercallbacks/getduration)
- [var getPresentationTimeStamp: CMBufferGetTimeCallback?](/documentation/coremedia/cmbuffercallbacks/getpresentationtimestamp)
- [var getSize: CMBufferGetSizeCallback?](/documentation/coremedia/cmbuffercallbacks/getsize)
- [var isDataReady: CMBufferGetBooleanCallback?](/documentation/coremedia/cmbuffercallbacks/isdataready)
- [var refcon: UnsafeMutableRawPointer?](/documentation/coremedia/cmbuffercallbacks/refcon)
- [var version: UInt32](/documentation/coremedia/cmbuffercallbacks/version)

#### Initializers

- [init(version: UInt32, refcon: UnsafeMutableRawPointer?, getDecodeTimeStamp: CMBufferGetTimeCallback?, getPresentationTimeStamp: CMBufferGetTimeCallback?, getDuration: CMBufferGetTimeCallback, isDataReady: CMBufferGetBooleanCallback?, compare: CMBufferCompareCallback?, dataBecameReadyNotification: Unmanaged<CFString>?, getSize: CMBufferGetSizeCallback?)](/documentation/coremedia/cmbuffercallbacks/init(version:refcon:getdecodetimestamp:getpresentationtimestamp:getduration:isdataready:compare:databecamereadynotification:getsize:))

### Managing a Queue

- [func CMBufferQueueEnqueue(CMBufferQueue, buffer: CMBuffer) -> OSStatus](/documentation/coremedia/cmbufferqueueenqueue(_:buffer:))
- [func CMBufferQueueCallForEachBuffer(CMBufferQueue, callback: (CMBuffer, UnsafeMutableRawPointer?) -> OSStatus, refcon: UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremedia/cmbufferqueuecallforeachbuffer(_:callback:refcon:))
- [func CMBufferQueueDequeue(CMBufferQueue) -> CMBuffer?](/documentation/coremedia/cmbufferqueuedequeue(_:))
- [func CMBufferQueueDequeueIfDataReady(CMBufferQueue) -> CMBuffer?](/documentation/coremedia/cmbufferqueuedequeueifdataready(_:))
- [func CMBufferQueueMarkEndOfData(CMBufferQueue) -> OSStatus](/documentation/coremedia/cmbufferqueuemarkendofdata(_:))
- [func CMBufferQueueReset(CMBufferQueue) -> OSStatus](/documentation/coremedia/cmbufferqueuereset(_:))
- [func CMBufferQueueResetWithCallback(CMBufferQueue, callback: (CMBuffer, UnsafeMutableRawPointer?) -> Void, refcon: UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremedia/cmbufferqueueresetwithcallback(_:callback:refcon:))
- [func CMBufferQueueRemoveTrigger(CMBufferQueue, triggerToken: CMBufferQueueTriggerToken) -> OSStatus](/documentation/coremedia/cmbufferqueueremovetrigger(_:triggertoken:))

### Managing Triggers

- [func CMBufferQueueInstallTriggerHandler(CMBufferQueue, CMBufferQueueTriggerCondition, CMTime, UnsafeMutablePointer<CMBufferQueueTriggerToken?>?, CMBufferQueueTriggerHandler?) -> OSStatus](/documentation/coremedia/cmbufferqueueinstalltriggerhandler(_:_:_:_:_:))
- [func CMBufferQueueInstallTriggerHandlerWithIntegerThreshold(CMBufferQueue, CMBufferQueueTriggerCondition, CMItemCount, UnsafeMutablePointer<CMBufferQueueTriggerToken?>?, CMBufferQueueTriggerHandler?) -> OSStatus](/documentation/coremedia/cmbufferqueueinstalltriggerhandlerwithintegerthreshold(_:_:_:_:_:))
- [CMBufferQueueTriggerHandler](/documentation/coremedia/cmbufferqueuetriggerhandler)
- [CMBufferQueueTriggerToken](/documentation/coremedia/cmbufferqueuetriggertoken)
- [Buffer Trigger Conditions](/documentation/coremedia/buffer-trigger-conditions)

#### Constants

- [var kCMBufferQueueTrigger_WhenDurationBecomesLessThan: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendurationbecomeslessthan)
- [var kCMBufferQueueTrigger_WhenDurationBecomesLessThanOrEqualTo: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendurationbecomeslessthanorequalto)
- [var kCMBufferQueueTrigger_WhenDurationBecomesGreaterThan: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendurationbecomesgreaterthan)
- [var kCMBufferQueueTrigger_WhenDurationBecomesGreaterThanOrEqualTo: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendurationbecomesgreaterthanorequalto)
- [var kCMBufferQueueTrigger_WhenMinPresentationTimeStampChanges: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenminpresentationtimestampchanges)
- [var kCMBufferQueueTrigger_WhenMaxPresentationTimeStampChanges: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenmaxpresentationtimestampchanges)
- [var kCMBufferQueueTrigger_WhenDataBecomesReady: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendatabecomesready)
- [var kCMBufferQueueTrigger_WhenEndOfDataReached: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenendofdatareached)
- [var kCMBufferQueueTrigger_WhenReset: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenreset)
- [var kCMBufferQueueTrigger_WhenBufferCountBecomesLessThan: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenbuffercountbecomeslessthan)
- [var kCMBufferQueueTrigger_WhenBufferCountBecomesGreaterThan: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whenbuffercountbecomesgreaterthan)
- [var kCMBufferQueueTrigger_WhenDurationBecomesGreaterThanOrEqualToAndBufferCountBecomesGreaterThan: CMBufferQueueTriggerCondition](/documentation/coremedia/kcmbufferqueuetrigger_whendurationbecomesgreaterthanorequaltoandbuffercountbecomesgreaterthan)
- [func CMBufferQueueTestTrigger(CMBufferQueue, triggerToken: CMBufferQueueTriggerToken) -> Bool](/documentation/coremedia/cmbufferqueuetesttrigger(_:triggertoken:))
- [func CMBufferQueueInstallTrigger(CMBufferQueue, callback: CMBufferQueueTriggerCallback?, refcon: UnsafeMutableRawPointer?, condition: CMBufferQueueTriggerCondition, time: CMTime, triggerTokenOut: UnsafeMutablePointer<CMBufferQueueTriggerToken?>?) -> OSStatus](/documentation/coremedia/cmbufferqueueinstalltrigger(_:callback:refcon:condition:time:triggertokenout:))
- [func CMBufferQueueInstallTriggerWithIntegerThreshold(CMBufferQueue, callback: CMBufferQueueTriggerCallback?, refcon: UnsafeMutableRawPointer?, condition: CMBufferQueueTriggerCondition, threshold: CMItemCount, triggerTokenOut: UnsafeMutablePointer<CMBufferQueueTriggerToken?>?) -> OSStatus](/documentation/coremedia/cmbufferqueueinstalltriggerwithintegerthreshold(_:callback:refcon:condition:threshold:triggertokenout:))
- [CMBufferQueueTriggerCallback](/documentation/coremedia/cmbufferqueuetriggercallback)
- [CMBufferQueueTriggerCondition](/documentation/coremedia/cmbufferqueuetriggercondition)

### Inspecting Duration and Timing

- [func CMBufferQueueGetDuration(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetduration(_:))
- [func CMBufferQueueGetMinDecodeTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetmindecodetimestamp(_:))
- [func CMBufferQueueGetFirstDecodeTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetfirstdecodetimestamp(_:))
- [func CMBufferQueueGetMinPresentationTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetminpresentationtimestamp(_:))
- [func CMBufferQueueGetFirstPresentationTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetfirstpresentationtimestamp(_:))
- [func CMBufferQueueGetEndPresentationTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetendpresentationtimestamp(_:))
- [func CMBufferQueueGetMaxPresentationTimeStamp(CMBufferQueue) -> CMTime](/documentation/coremedia/cmbufferqueuegetmaxpresentationtimestamp(_:))
- [func CMBufferQueueGetCallbacksForSampleBuffersSortedByOutputPTS() -> UnsafePointer<CMBufferCallbacks>](/documentation/coremedia/cmbufferqueuegetcallbacksforsamplebufferssortedbyoutputpts())
- [func CMBufferQueueGetCallbacksForUnsortedSampleBuffers() -> UnsafePointer<CMBufferCallbacks>](/documentation/coremedia/cmbufferqueuegetcallbacksforunsortedsamplebuffers())

### Inspecting a Queue

- [func CMBufferQueueIsEmpty(CMBufferQueue) -> Bool](/documentation/coremedia/cmbufferqueueisempty(_:))
- [func CMBufferQueueGetBufferCount(CMBufferQueue) -> CMItemCount](/documentation/coremedia/cmbufferqueuegetbuffercount(_:))
- [func CMBufferQueueGetTotalSize(CMBufferQueue) -> Int](/documentation/coremedia/cmbufferqueuegettotalsize(_:))
- [func CMBufferQueueGetHead(CMBufferQueue) -> CMBuffer?](/documentation/coremedia/cmbufferqueuegethead(_:))
- [func CMBufferQueueContainsEndOfData(CMBufferQueue) -> Bool](/documentation/coremedia/cmbufferqueuecontainsendofdata(_:))
- [func CMBufferQueueIsAtEndOfData(CMBufferQueue) -> Bool](/documentation/coremedia/cmbufferqueueisatendofdata(_:))

### Validating a Queue

- [func CMBufferQueueSetValidationHandler(CMBufferQueue, CMBufferValidationHandler) -> OSStatus](/documentation/coremedia/cmbufferqueuesetvalidationhandler(_:_:))
- [CMBufferValidationHandler](/documentation/coremedia/cmbuffervalidationhandler)
- [func CMBufferQueueSetValidationCallback(CMBufferQueue, callback: CMBufferValidationCallback, refcon: UnsafeMutableRawPointer?) -> OSStatus](/documentation/coremedia/cmbufferqueuesetvalidationcallback(_:callback:refcon:))
- [CMBufferValidationCallback](/documentation/coremedia/cmbuffervalidationcallback)

### Accessing the Type Identifier

- [func CMBufferQueueGetTypeID() -> CFTypeID](/documentation/coremedia/cmbufferqueuegettypeid())

### Data Types

- [CMBufferQueue](/documentation/coremedia/cmbufferqueue)

#### Managing a Queue

- [func enqueue(CMBuffer) throws](/documentation/coremedia/cmbufferqueue/enqueue(_:))
- [func dequeue() -> CMBuffer?](/documentation/coremedia/cmbufferqueue/dequeue())
- [func dequeueIfDataReady() -> CMBuffer?](/documentation/coremedia/cmbufferqueue/dequeueifdataready())
- [func markEndOfData() throws](/documentation/coremedia/cmbufferqueue/markendofdata())
- [func reset() throws](/documentation/coremedia/cmbufferqueue/reset())
- [func reset((CMBuffer) throws -> ()) throws](/documentation/coremedia/cmbufferqueue/reset(_:))

#### Managing Triggers

- [func installTrigger(condition: CMBufferQueue.TriggerCondition, CMBufferQueueTriggerHandler?) throws -> CMBufferQueue.TriggerToken](/documentation/coremedia/cmbufferqueue/installtrigger(condition:_:))
- [func removeTrigger(CMBufferQueue.TriggerToken) throws](/documentation/coremedia/cmbufferqueue/removetrigger(_:))
- [func testTrigger(CMBufferQueue.TriggerToken) -> Bool](/documentation/coremedia/cmbufferqueue/testtrigger(_:))
- [CMBufferQueue.TriggerToken](/documentation/coremedia/cmbufferqueue/triggertoken)
- [CMBufferQueue.TriggerCondition](/documentation/coremedia/cmbufferqueue/triggercondition)

##### Conditions

- [case whenBufferCountBecomesGreaterThan(CMItemCount)](/documentation/coremedia/cmbufferqueue/triggercondition/whenbuffercountbecomesgreaterthan(_:))
- [case whenBufferCountBecomesLessThan(CMItemCount)](/documentation/coremedia/cmbufferqueue/triggercondition/whenbuffercountbecomeslessthan(_:))
- [case whenDataBecomesReady](/documentation/coremedia/cmbufferqueue/triggercondition/whendatabecomesready)
- [case whenDurationBecomesGreaterThan(CMTime)](/documentation/coremedia/cmbufferqueue/triggercondition/whendurationbecomesgreaterthan(_:))
- [case whenDurationBecomesGreaterThanOrEqualTo(CMTime)](/documentation/coremedia/cmbufferqueue/triggercondition/whendurationbecomesgreaterthanorequalto(_:))
- [case whenDurationBecomesLessThan(CMTime)](/documentation/coremedia/cmbufferqueue/triggercondition/whendurationbecomeslessthan(_:))
- [case whenDurationBecomesLessThanOrEqualTo(CMTime)](/documentation/coremedia/cmbufferqueue/triggercondition/whendurationbecomeslessthanorequalto(_:))
- [case whenEndOfDataReached](/documentation/coremedia/cmbufferqueue/triggercondition/whenendofdatareached)
- [case whenMaxPresentationTimeStampChanges](/documentation/coremedia/cmbufferqueue/triggercondition/whenmaxpresentationtimestampchanges)
- [case whenMinPresentationTimeStampChanges](/documentation/coremedia/cmbufferqueue/triggercondition/whenminpresentationtimestampchanges)
- [case whenReset](/documentation/coremedia/cmbufferqueue/triggercondition/whenreset)

#### Inspecting Duration and Timing

- [var duration: CMTime](/documentation/coremedia/cmbufferqueue/duration)
- [var totalSize: Int](/documentation/coremedia/cmbufferqueue/totalsize)
- [var firstDecodeTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/firstdecodetimestamp)
- [var firstPresentationTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/firstpresentationtimestamp)
- [var endPresentationTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/endpresentationtimestamp)
- [var minDecodeTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/mindecodetimestamp)
- [var minPresentationTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/minpresentationtimestamp)
- [var maxPresentationTimeStamp: CMTime](/documentation/coremedia/cmbufferqueue/maxpresentationtimestamp)

#### Inspecting a Queue

- [var isEmpty: Bool](/documentation/coremedia/cmbufferqueue/isempty)
- [var bufferCount: CMItemCount](/documentation/coremedia/cmbufferqueue/buffercount)
- [var head: CMBuffer?](/documentation/coremedia/cmbufferqueue/head)
- [var containsEndOfData: Bool](/documentation/coremedia/cmbufferqueue/containsendofdata)
- [var isAtEndOfData: Bool](/documentation/coremedia/cmbufferqueue/isatendofdata)

#### Validating a Queue

- [func setValidationHandler((CMBufferQueue, CMBuffer) throws -> Void)](/documentation/coremedia/cmbufferqueue/setvalidationhandler(_:))

#### Accessing Buffers

- [var buffers: CMBufferQueue.Buffers](/documentation/coremedia/cmbufferqueue/buffers-swift.property)

#### Accessing the Type Identifier

- [class var typeID: CFTypeID](/documentation/coremedia/cmbufferqueue/typeid)

#### Data Types

- [CMBufferQueue.Buffers](/documentation/coremedia/cmbufferqueue/buffers-swift.struct)
- [CMBufferQueue.Handlers](/documentation/coremedia/cmbufferqueue/handlers)

##### Initializers

- [init(withHandlers: (inout CMBufferQueue.Handlers.Builder) -> Void)](/documentation/coremedia/cmbufferqueue/handlers/init(withhandlers:))

##### Instance Properties

- [let compare: CMBufferCompareHandler?](/documentation/coremedia/cmbufferqueue/handlers/compare)
- [let dataBecameReadyNotification: String?](/documentation/coremedia/cmbufferqueue/handlers/databecamereadynotification)
- [let getDecodeTimeStamp: CMBufferGetTimeHandler?](/documentation/coremedia/cmbufferqueue/handlers/getdecodetimestamp)
- [let getDuration: CMBufferGetTimeHandler](/documentation/coremedia/cmbufferqueue/handlers/getduration)
- [let getPresentationTimeStamp: CMBufferGetTimeHandler?](/documentation/coremedia/cmbufferqueue/handlers/getpresentationtimestamp)
- [let getSize: CMBufferGetSizeHandler?](/documentation/coremedia/cmbufferqueue/handlers/getsize)
- [let isDataReady: CMBufferGetBooleanHandler?](/documentation/coremedia/cmbufferqueue/handlers/isdataready)

##### Type Properties

- [static let outputPTSSortedSampleBuffers: CMBufferQueue.Handlers](/documentation/coremedia/cmbufferqueue/handlers/outputptssortedsamplebuffers)
- [static let unsortedSampleBuffers: CMBufferQueue.Handlers](/documentation/coremedia/cmbufferqueue/handlers/unsortedsamplebuffers)

##### Instance Methods

- [func withHandlers((inout CMBufferQueue.Handlers.Builder) -> Void) -> CMBufferQueue.Handlers](/documentation/coremedia/cmbufferqueue/handlers/withhandlers(_:))

##### Structures

- [CMBufferQueue.Handlers.Builder](/documentation/coremedia/cmbufferqueue/handlers/builder)

###### Instance Properties

- [var dataBecameReadyNotification: String?](/documentation/coremedia/cmbufferqueue/handlers/builder/databecamereadynotification)

###### Instance Methods

- [func compare(CMBufferCompareHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/compare(_:))
- [func getDecodeTimeStamp(CMBufferGetTimeHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/getdecodetimestamp(_:))
- [func getDuration(CMBufferGetTimeHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/getduration(_:))
- [func getPresentationTimeStamp(CMBufferGetTimeHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/getpresentationtimestamp(_:))
- [func getSize(CMBufferGetSizeHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/getsize(_:))
- [func isDataReady(CMBufferGetBooleanHandler)](/documentation/coremedia/cmbufferqueue/handlers/builder/isdataready(_:))
- [CMBufferQueue.Error](/documentation/coremedia/cmbufferqueue/error)

##### Type Properties

- [static let allocationFailed: NSError](/documentation/coremedia/cmbufferqueue/error/allocationfailed)
- [static let badTriggerDuration: NSError](/documentation/coremedia/cmbufferqueue/error/badtriggerduration)
- [static let cannotModifyQueueFromTriggerCallback: NSError](/documentation/coremedia/cmbufferqueue/error/cannotmodifyqueuefromtriggercallback)
- [static let enqueueAfterEndOfData: NSError](/documentation/coremedia/cmbufferqueue/error/enqueueafterendofdata)
- [static let invalidBuffer: NSError](/documentation/coremedia/cmbufferqueue/error/invalidbuffer)
- [static let invalidCMBufferCallbacksStruct: NSError](/documentation/coremedia/cmbufferqueue/error/invalidcmbuffercallbacksstruct)
- [static let invalidTriggerCondition: NSError](/documentation/coremedia/cmbufferqueue/error/invalidtriggercondition)
- [static let invalidTriggerToken: NSError](/documentation/coremedia/cmbufferqueue/error/invalidtriggertoken)
- [static let queueIsFull: NSError](/documentation/coremedia/cmbufferqueue/error/queueisfull)
- [static let requiredParameterMissing: NSError](/documentation/coremedia/cmbufferqueue/error/requiredparametermissing)

#### Initializers

- [init(referencing: CMBufferQueue)](/documentation/coremedia/cmbufferqueue/init(referencing:))

#### Type Aliases

- [CMBufferQueue.T](/documentation/coremedia/cmbufferqueue/t)

### Error Codes

- [Buffer Queue Error Codes](/documentation/coremedia/buffer-queue-errors)

#### Error Codes

- [var kCMBufferQueueError_AllocationFailed: OSStatus](/documentation/coremedia/kcmbufferqueueerror_allocationfailed)
- [var kCMBufferQueueError_RequiredParameterMissing: OSStatus](/documentation/coremedia/kcmbufferqueueerror_requiredparametermissing)
- [var kCMBufferQueueError_InvalidCMBufferCallbacksStruct: OSStatus](/documentation/coremedia/kcmbufferqueueerror_invalidcmbuffercallbacksstruct)
- [var kCMBufferQueueError_EnqueueAfterEndOfData: OSStatus](/documentation/coremedia/kcmbufferqueueerror_enqueueafterendofdata)
- [var kCMBufferQueueError_QueueIsFull: OSStatus](/documentation/coremedia/kcmbufferqueueerror_queueisfull)
- [var kCMBufferQueueError_BadTriggerDuration: OSStatus](/documentation/coremedia/kcmbufferqueueerror_badtriggerduration)
- [var kCMBufferQueueError_CannotModifyQueueFromTriggerCallback: OSStatus](/documentation/coremedia/kcmbufferqueueerror_cannotmodifyqueuefromtriggercallback)
- [var kCMBufferQueueError_InvalidTriggerCondition: OSStatus](/documentation/coremedia/kcmbufferqueueerror_invalidtriggercondition)
- [var kCMBufferQueueError_InvalidTriggerToken: OSStatus](/documentation/coremedia/kcmbufferqueueerror_invalidtriggertoken)
- [var kCMBufferQueueError_InvalidBuffer: OSStatus](/documentation/coremedia/kcmbufferqueueerror_invalidbuffer)
- [CMMemoryPool](/documentation/coremedia/cmmemorypool-api)

### Creating a Memory Pool

- [func CMMemoryPoolCreate(options: CFDictionary?) -> CMMemoryPool](/documentation/coremedia/cmmemorypoolcreate(options:))

#### Creation Options

- [let kCMMemoryPoolOption_AgeOutPeriod: CFString](/documentation/coremedia/kcmmemorypooloption_ageoutperiod)

### Managing a Memory Pool

- [func CMMemoryPoolGetAllocator(CMMemoryPool) -> CFAllocator](/documentation/coremedia/cmmemorypoolgetallocator(_:))
- [func CMMemoryPoolFlush(CMMemoryPool)](/documentation/coremedia/cmmemorypoolflush(_:))
- [func CMMemoryPoolInvalidate(CMMemoryPool)](/documentation/coremedia/cmmemorypoolinvalidate(_:))

### Accessing the Type Identifier

- [func CMMemoryPoolGetTypeID() -> CFTypeID](/documentation/coremedia/cmmemorypoolgettypeid())

### Data Types

- [CMMemoryPool](/documentation/coremedia/cmmemorypool)

### Errors

- [var kCMMemoryPoolError_AllocationFailed: OSStatus](/documentation/coremedia/kcmmemorypoolerror_allocationfailed)
- [var kCMMemoryPoolError_InvalidParameter: OSStatus](/documentation/coremedia/kcmmemorypoolerror_invalidparameter)

## Reference

- [Core Media Constants](/documentation/coremedia/core-media-constants)

### Constants

- [var COREMEDIA_DECLARE_BRIDGED_TYPES: Bool](/documentation/coremedia/coremedia_declare_bridged_types)
- [var COREMEDIA_DECLARE_NULLABILITY: Bool](/documentation/coremedia/coremedia_declare_nullability)
- [var COREMEDIA_DECLARE_NULLABILITY_BEGIN_END: Bool](/documentation/coremedia/coremedia_declare_nullability_begin_end)
- [var COREMEDIA_DECLARE_RETURNS_NOT_RETAINED_ON_PARAMETERS: Bool](/documentation/coremedia/coremedia_declare_returns_not_retained_on_parameters)
- [var COREMEDIA_DECLARE_RETURNS_RETAINED: Bool](/documentation/coremedia/coremedia_declare_returns_retained)
- [var COREMEDIA_DECLARE_RETURNS_RETAINED_ON_PARAMETERS: Bool](/documentation/coremedia/coremedia_declare_returns_retained_on_parameters)
- [var COREMEDIA_USE_DERIVED_ENUMS_FOR_CONSTANTS: Bool](/documentation/coremedia/coremedia_use_derived_enums_for_constants)
- [var CMITEMCOUNT_MAX: Int](/documentation/coremedia/cmitemcount_max)
- [var COREMEDIA_CMBASECLASS_VERSION_IS_POINTER_ALIGNED: Bool](/documentation/coremedia/coremedia_cmbaseclass_version_is_pointer_aligned)
- [var COREMEDIA_DECLARE_RELEASES_ARGUMENT: Bool](/documentation/coremedia/coremedia_declare_releases_argument)
- [var COREMEDIA_FALSE: Bool](/documentation/coremedia/coremedia_false)
- [var COREMEDIA_TRUE: Bool](/documentation/coremedia/coremedia_true)
- [var COREMEDIA_USE_ALIGNED_CMBASECLASS_VERSION: Bool](/documentation/coremedia/coremedia_use_aligned_cmbaseclass_version)
- [var CMTIMEBASE_USE_SOURCE_TERMINOLOGY: Int32](/documentation/coremedia/cmtimebase_use_source_terminology)
- [var COREMEDIA_DECLARE_RETURNS_RETAINED_BLOCK: Bool](/documentation/coremedia/coremedia_declare_returns_retained_block)
- [let kCMFormatDescriptionExtension_ProjectionKind: CFString](/documentation/coremedia/kcmformatdescriptionextension_projectionkind)
- [let kCMFormatDescriptionExtension_ViewPackingKind: CFString](/documentation/coremedia/kcmformatdescriptionextension_viewpackingkind)
- [let kCMFormatDescriptionLogTransferFunction_AppleLog: CFString](/documentation/coremedia/kcmformatdescriptionlogtransferfunction_applelog)
- [let kCMFormatDescriptionProjectionKind_Rectilinear: CFString](/documentation/coremedia/kcmformatdescriptionprojectionkind_rectilinear)
- [let kCMFormatDescriptionViewPackingKind_OverUnder: CFString](/documentation/coremedia/kcmformatdescriptionviewpackingkind_overunder)
- [let kCMFormatDescriptionViewPackingKind_SideBySide: CFString](/documentation/coremedia/kcmformatdescriptionviewpackingkind_sidebyside)
- [let kCMMetadataDataType_QuickTimeMetadataMilliLux: CFString](/documentation/coremedia/kcmmetadatadatatype_quicktimemetadatamillilux)
- [let kCMMetadataDataType_QuickTimeMetadataUUID: CFString](/documentation/coremedia/kcmmetadatadatatype_quicktimemetadatauuid)
- [let kCMMetadataIdentifier_QuickTimeMetadataSceneIlluminance: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatasceneilluminance)
- [let kCMMetadataIdentifier_QuickTimeMetadataSegmentIdentifier: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatasegmentidentifier)
- [let kCMSampleAttachmentKey_HDR10PlusPerFrameData: CFString](/documentation/coremedia/kcmsampleattachmentkey_hdr10plusperframedata)
- [let kCMTagProjectionTypeHalfEquirectangular: __CMTag](/documentation/coremedia/kcmtagprojectiontypehalfequirectangular)
- [let kCMTextMarkupAttribute_FontFamilyNameList: CFString](/documentation/coremedia/kcmtextmarkupattribute_fontfamilynamelist)
- [let kCMFormatDescriptionExtension_ConvertedFromExternalSphericalTags: CFString](/documentation/coremedia/kcmformatdescriptionextension_convertedfromexternalsphericaltags)
- [let kCMFormatDescriptionProjectionKind_AppleImmersiveVideo: CFString](/documentation/coremedia/kcmformatdescriptionprojectionkind_appleimmersivevideo)
- [let kCMFormatDescriptionProjectionKind_Equirectangular: CFString](/documentation/coremedia/kcmformatdescriptionprojectionkind_equirectangular)
- [let kCMFormatDescriptionProjectionKind_HalfEquirectangular: CFString](/documentation/coremedia/kcmformatdescriptionprojectionkind_halfequirectangular)
- [let kCMFormatDescriptionProjectionKind_ParametricImmersive: CFString](/documentation/coremedia/kcmformatdescriptionprojectionkind_parametricimmersive)
- [let kCMMetadataBaseDataType_ExtendedRasterRectangleValue: CFString](/documentation/coremedia/kcmmetadatabasedatatype_extendedrasterrectanglevalue)
- [let kCMMetadataBaseDataType_RasterRectangleValue: CFString](/documentation/coremedia/kcmmetadatabasedatatype_rasterrectanglevalue)
- [let kCMMetadataIdentifier_QuickTimeMetadataDisplayMaskRectangleMono: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatadisplaymaskrectanglemono)
- [let kCMMetadataIdentifier_QuickTimeMetadataDisplayMaskRectangleStereoLeft: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatadisplaymaskrectanglestereoleft)
- [let kCMMetadataIdentifier_QuickTimeMetadataDisplayMaskRectangleStereoRight: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatadisplaymaskrectanglestereoright)
- [let kCMMetadataIdentifier_QuickTimeMetadataPresentationImmersiveMedia: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadatapresentationimmersivemedia)
- [let kCMMetadataIdentifier_QuickTimeMetadataSpatialAudioMix: CFString](/documentation/coremedia/kcmmetadataidentifier_quicktimemetadataspatialaudiomix)
- [Camera calibration](/documentation/coremedia/camera-calibration-constants)

#### Constants

- [let kCMFormatDescriptionExtension_CameraCalibrationDataLensCollection: CFString](/documentation/coremedia/kcmformatdescriptionextension_cameracalibrationdatalenscollection)
- [let kCMFormatDescriptionCameraCalibration_ExtrinsicOrientationQuaternion: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_extrinsicorientationquaternion)
- [let kCMFormatDescriptionCameraCalibration_ExtrinsicOriginSource: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_extrinsicoriginsource)
- [let kCMFormatDescriptionCameraCalibration_IntrinsicMatrix: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_intrinsicmatrix)
- [let kCMFormatDescriptionCameraCalibration_IntrinsicMatrixProjectionOffset: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_intrinsicmatrixprojectionoffset)
- [let kCMFormatDescriptionCameraCalibration_IntrinsicMatrixReferenceDimensions: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_intrinsicmatrixreferencedimensions)
- [let kCMFormatDescriptionCameraCalibration_LensAlgorithmKind: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensalgorithmkind)
- [let kCMFormatDescriptionCameraCalibration_LensDistortions: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensdistortions)
- [let kCMFormatDescriptionCameraCalibration_LensDomain: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensdomain)
- [let kCMFormatDescriptionCameraCalibration_LensFrameAdjustmentsPolynomialX: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensframeadjustmentspolynomialx)
- [let kCMFormatDescriptionCameraCalibration_LensFrameAdjustmentsPolynomialY: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensframeadjustmentspolynomialy)
- [let kCMFormatDescriptionCameraCalibration_LensIdentifier: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensidentifier)
- [let kCMFormatDescriptionCameraCalibration_LensRole: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_lensrole)
- [let kCMFormatDescriptionCameraCalibration_RadialAngleLimit: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibration_radialanglelimit)
- [let kCMFormatDescriptionCameraCalibrationExtrinsicOriginSource_StereoCameraSystemBaseline: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationextrinsicoriginsource_stereocamerasystembaseline)
- [let kCMFormatDescriptionCameraCalibrationLensAlgorithmKind_ParametricLens: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationlensalgorithmkind_parametriclens)
- [let kCMFormatDescriptionCameraCalibrationLensDomain_Color: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationlensdomain_color)
- [let kCMFormatDescriptionCameraCalibrationLensRole_Left: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationlensrole_left)
- [let kCMFormatDescriptionCameraCalibrationLensRole_Mono: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationlensrole_mono)
- [let kCMFormatDescriptionCameraCalibrationLensRole_Right: CFString](/documentation/coremedia/kcmformatdescriptioncameracalibrationlensrole_right)

### Type Aliases

- [CMBaseClassVersion](/documentation/coremedia/cmbaseclassversion)
- [CMStructVersion](/documentation/coremedia/cmstructversion)
- [Core Media Functions](/documentation/coremedia/core-media-functions)

### Functions

- [func CMBufferQueueCopyHead(CMBufferQueue) -> CMBuffer?](/documentation/coremedia/cmbufferqueuecopyhead(_:))
- [Core Media Type Aliases](/documentation/coremedia/core-media-type-aliases)

### Type Aliases

- [CMBufferCompareHandler](/documentation/coremedia/cmbuffercomparehandler)
- [CMBufferGetBooleanHandler](/documentation/coremedia/cmbuffergetbooleanhandler)
- [CMBufferGetSizeHandler](/documentation/coremedia/cmbuffergetsizehandler)
- [CMBufferGetTimeHandler](/documentation/coremedia/cmbuffergettimehandler)
- [CMTaggedBufferGroupFormatDescription](/documentation/coremedia/cmtaggedbuffergroupformatdescription)
- [CMTaggedBufferGroupFormatType](/documentation/coremedia/cmtaggedbuffergroupformattype)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
