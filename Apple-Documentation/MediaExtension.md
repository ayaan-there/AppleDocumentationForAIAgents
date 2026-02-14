# MediaExtension Documentation

Source: https://sosumi.ai/documentation/mediaextension

---
title: MediaExtension
source: https://developer.apple.com/documentation/mediaextension
timestamp: 2026-02-13T18:59:31.150Z
---

## Format readers

- [MEFormatReader](/documentation/mediaextension/meformatreader)

### Reading and parsing media assets

- [func loadFileInfo(completionHandler: (MEFileInfo?, (any Error)?) -> Void)](/documentation/mediaextension/meformatreader/loadfileinfo(completionhandler:))
- [func loadMetadata(completionHandler: ([AVMetadataItem]?, (any Error)?) -> Void)](/documentation/mediaextension/meformatreader/loadmetadata(completionhandler:))
- [func loadTrackReaders(completionHandler: ([any METrackReader]?, (any Error)?) -> Void)](/documentation/mediaextension/meformatreader/loadtrackreaders(completionhandler:))
- [func parseAdditionalFragments(completionHandler: (MEFormatReaderParseAdditionalFragmentsStatus, (any Error)?) -> Void)](/documentation/mediaextension/meformatreader/parseadditionalfragments(completionhandler:))
- [MEFormatReaderParseAdditionalFragmentsStatus](/documentation/mediaextension/meformatreaderparseadditionalfragmentsstatus)

#### Creating informational status flags

- [init(rawValue: UInt)](/documentation/mediaextension/meformatreaderparseadditionalfragmentsstatus/init(rawvalue:))

#### Evaluating a fragment parsing operation

- [static var sizeIncreased: MEFormatReaderParseAdditionalFragmentsStatus](/documentation/mediaextension/meformatreaderparseadditionalfragmentsstatus/sizeincreased)
- [static var fragmentAdded: MEFormatReaderParseAdditionalFragmentsStatus](/documentation/mediaextension/meformatreaderparseadditionalfragmentsstatus/fragmentadded)
- [static var fragmentsComplete: MEFormatReaderParseAdditionalFragmentsStatus](/documentation/mediaextension/meformatreaderparseadditionalfragmentsstatus/fragmentscomplete)

### Extension requirements

- [Format reader property list dictionaries](/documentation/mediaextension/format-reader-property-list-dictionaries)

#### Property list keys

- [var kMEFormatReaderClassImplementationIDKey: String](/documentation/mediaextension/kmeformatreaderclassimplementationidkey)
- [var kMEFormatReaderExtensionPointName: String](/documentation/mediaextension/kmeformatreaderextensionpointname)
- [var kMEFormatReaderFileNameExtensionArrayKey: String](/documentation/mediaextension/kmeformatreaderfilenameextensionarraykey)
- [var kMEFormatReaderUTTypeArrayKey: String](/documentation/mediaextension/kmeformatreaderuttypearraykey)
- [var kMEFormatReaderObjectNameKey: String](/documentation/mediaextension/kmeformatreaderobjectnamekey)
- [Format reader entitlement](/documentation/mediaextension/format-reader-entitlement)
- [MEFormatReaderExtension](/documentation/mediaextension/meformatreaderextension)

### Creating a format reader

- [init()](/documentation/mediaextension/meformatreaderextension/init())
- [func formatReader(with: MEByteSource, options: MEFormatReaderInstantiationOptions?) throws -> any MEFormatReader](/documentation/mediaextension/meformatreaderextension/formatreader(with:options:))
- [MEFormatReaderInstantiationOptions](/documentation/mediaextension/meformatreaderinstantiationoptions)

### Inspecting format reader extension options

- [var allowIncrementalFragmentParsing: Bool](/documentation/mediaextension/meformatreaderinstantiationoptions/allowincrementalfragmentparsing)
- [MEFileInfo](/documentation/mediaextension/mefileinfo)

### Inspecting file properties

- [var duration: CMTime](/documentation/mediaextension/mefileinfo/duration)
- [var fragmentsStatus: MEFileInfo.FragmentsStatus](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.property)
- [MEFileInfo.FragmentsStatus](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum)

#### File fragment status values

- [case couldNotContainFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/couldnotcontainfragments)
- [case containsFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/containsfragments)
- [case couldContainButDoesNotContainFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/couldcontainbutdoesnotcontainfragments)
- [case couldNotContainFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/couldnotcontainfragments)
- [case containsFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/containsfragments)
- [case couldContainButDoesNotContainFragments](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/couldcontainbutdoesnotcontainfragments)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaextension/mefileinfo/fragmentsstatus-swift.enum/init(rawvalue:))

### Instance Properties

- [var sidecarFileName: String?](/documentation/mediaextension/mefileinfo/sidecarfilename)
- [Format reader property list dictionaries](/documentation/mediaextension/format-reader-property-list-dictionaries)

### Property list keys

- [var kMEFormatReaderClassImplementationIDKey: String](/documentation/mediaextension/kmeformatreaderclassimplementationidkey)
- [var kMEFormatReaderExtensionPointName: String](/documentation/mediaextension/kmeformatreaderextensionpointname)
- [var kMEFormatReaderFileNameExtensionArrayKey: String](/documentation/mediaextension/kmeformatreaderfilenameextensionarraykey)
- [var kMEFormatReaderUTTypeArrayKey: String](/documentation/mediaextension/kmeformatreaderuttypearraykey)
- [var kMEFormatReaderObjectNameKey: String](/documentation/mediaextension/kmeformatreaderobjectnamekey)
- [Format reader entitlement](/documentation/mediaextension/format-reader-entitlement)

## Track readers

- [METrackReader](/documentation/mediaextension/metrackreader)

### Getting track information

- [func loadTrackInfo(completionHandler: (METrackInfo?, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/loadtrackinfo(completionhandler:))
- [func generateSampleCursor(atPresentationTimeStamp: CMTime, completionHandler: ((any MESampleCursor)?, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/generatesamplecursor(atpresentationtimestamp:completionhandler:))
- [func generateSampleCursorAtFirstSampleInDecodeOrder(completionHandler: ((any MESampleCursor)?, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/generatesamplecursoratfirstsampleindecodeorder(completionhandler:))
- [func generateSampleCursorAtLastSampleInDecodeOrder(completionHandler: ((any MESampleCursor)?, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/generatesamplecursoratlastsampleindecodeorder(completionhandler:))
- [func loadUneditedDuration(completionHandler: (CMTime, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/loaduneditedduration(completionhandler:))
- [func loadTotalSampleDataLength(completionHandler: (Int64, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/loadtotalsampledatalength(completionhandler:))
- [func loadEstimatedDataRate(completionHandler: (Float32, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/loadestimateddatarate(completionhandler:))
- [func loadMetadata(completionHandler: ([AVMetadataItem]?, (any Error)?) -> Void)](/documentation/mediaextension/metrackreader/loadmetadata(completionhandler:))
- [METrackInfo](/documentation/mediaextension/metrackinfo)

### Inspecting track information

- [var mediaType: CMMediaType](/documentation/mediaextension/metrackinfo/mediatype)
- [var trackID: CMPersistentTrackID](/documentation/mediaextension/metrackinfo/trackid)
- [var isEnabled: Bool](/documentation/mediaextension/metrackinfo/isenabled)
- [var naturalTimescale: CMTimeScale](/documentation/mediaextension/metrackinfo/naturaltimescale)
- [var extendedLanguageTag: String?](/documentation/mediaextension/metrackinfo/extendedlanguagetag)
- [var naturalSize: CGSize](/documentation/mediaextension/metrackinfo/naturalsize)
- [var preferredTransform: CGAffineTransform](/documentation/mediaextension/metrackinfo/preferredtransform)
- [var nominalFrameRate: Float32](/documentation/mediaextension/metrackinfo/nominalframerate)
- [var requiresFrameReordering: Bool](/documentation/mediaextension/metrackinfo/requiresframereordering)

## Sample cursors

- [MESampleCursor](/documentation/mediaextension/mesamplecursor)

### Inspecting a sample cursor

- [var presentationTimeStamp: CMTime](/documentation/mediaextension/mesamplecursor/presentationtimestamp)
- [var decodeTimeStamp: CMTime](/documentation/mediaextension/mesamplecursor/decodetimestamp)
- [var currentSampleDuration: CMTime](/documentation/mediaextension/mesamplecursor/currentsampleduration)
- [var currentSampleFormatDescription: CMFormatDescription?](/documentation/mediaextension/mesamplecursor/currentsampleformatdescription)
- [var syncInfo: AVSampleCursorSyncInfo](/documentation/mediaextension/mesamplecursor/syncinfo)
- [var dependencyInfo: AVSampleCursorDependencyInfo](/documentation/mediaextension/mesamplecursor/dependencyinfo)
- [var hevcDependencyInfo: MEHEVCDependencyInfo](/documentation/mediaextension/mesamplecursor/hevcdependencyinfo)
- [var decodeTimeOfLastSampleReachableByForwardSteppingThatIsAlreadyLoadedByByteSource: CMTime](/documentation/mediaextension/mesamplecursor/decodetimeoflastsamplereachablebyforwardsteppingthatisalreadyloadedbybytesource)

### Stepping through samples

- [func samplesWithEarlierDTSsMayHaveLaterPTSs(than: any MESampleCursor) -> Bool](/documentation/mediaextension/mesamplecursor/sampleswithearlierdtssmayhavelaterptss(than:))
- [func samplesWithLaterDTSsMayHaveEarlierPTSs(than: any MESampleCursor) -> Bool](/documentation/mediaextension/mesamplecursor/sampleswithlaterdtssmayhaveearlierptss(than:))
- [func estimatedSampleLocation() throws -> MEEstimatedSampleLocation](/documentation/mediaextension/mesamplecursor/estimatedsamplelocation())
- [func refineSampleLocation(AVSampleCursorStorageRange, refinementData: UnsafePointer<UInt8>, refinementDataLength: Int, refinedLocation: UnsafeMutablePointer<AVSampleCursorStorageRange>) throws](/documentation/mediaextension/mesamplecursor/refinesamplelocation(_:refinementdata:refinementdatalength:refinedlocation:))
- [func stepByDecodeTime(CMTime, completionHandler: (CMTime, Bool, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/stepbydecodetime(_:completionhandler:))
- [func stepByPresentationTime(CMTime, completionHandler: (CMTime, Bool, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/stepbypresentationtime(_:completionhandler:))
- [func stepInDecodeOrder(by: Int64, completionHandler: (Int64, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/stepindecodeorder(by:completionhandler:))
- [func stepInPresentationOrder(by: Int64, completionHandler: (Int64, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/stepinpresentationorder(by:completionhandler:))

### Sending samples to a pipeline

- [func chunkDetails() throws -> MESampleCursorChunk](/documentation/mediaextension/mesamplecursor/chunkdetails())
- [func sampleLocation() throws -> MESampleLocation](/documentation/mediaextension/mesamplecursor/samplelocation())
- [func loadSampleBufferContainingSamples(to: (any MESampleCursor)?, completionHandler: (CMSampleBuffer?, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/loadsamplebuffercontainingsamples(to:completionhandler:))

### RAW processing metadata

- [func loadPostDecodeProcessingMetadata(completionHandler: ([String : any Sendable]?, (any Error)?) -> Void)](/documentation/mediaextension/mesamplecursor/loadpostdecodeprocessingmetadata(completionhandler:))
- [MESampleLocation](/documentation/mediaextension/mesamplelocation)

### Creating a sample location

- [init(byteSource: MEByteSource, sampleLocation: AVSampleCursorStorageRange)](/documentation/mediaextension/mesamplelocation/init(bytesource:samplelocation:))

### Inspecting a sample location

- [var byteSource: MEByteSource](/documentation/mediaextension/mesamplelocation/bytesource)
- [var sampleLocation: AVSampleCursorStorageRange](/documentation/mediaextension/mesamplelocation/samplelocation)
- [MESampleCursorChunk](/documentation/mediaextension/mesamplecursorchunk)

### Creating a sample cursor chunk

- [init(byteSource: MEByteSource, chunkStorageRange: AVSampleCursorStorageRange, chunkInfo: AVSampleCursorChunkInfo, sampleIndexWithinChunk: CFIndex)](/documentation/mediaextension/mesamplecursorchunk/init(bytesource:chunkstoragerange:chunkinfo:sampleindexwithinchunk:))

### Inspecting a chunk

- [var byteSource: MEByteSource](/documentation/mediaextension/mesamplecursorchunk/bytesource)
- [var chunkStorageRange: AVSampleCursorStorageRange](/documentation/mediaextension/mesamplecursorchunk/chunkstoragerange)
- [var chunkInfo: AVSampleCursorChunkInfo](/documentation/mediaextension/mesamplecursorchunk/chunkinfo)
- [var sampleIndexWithinChunk: CFIndex](/documentation/mediaextension/mesamplecursorchunk/sampleindexwithinchunk)
- [MEEstimatedSampleLocation](/documentation/mediaextension/meestimatedsamplelocation)

### Creating an estimated sample location

- [init(byteSource: MEByteSource, estimatedSampleLocation: AVSampleCursorStorageRange, refinementDataLocation: AVSampleCursorStorageRange)](/documentation/mediaextension/meestimatedsamplelocation/init(bytesource:estimatedsamplelocation:refinementdatalocation:))

### Inspecting an estimated sample location

- [var byteSource: MEByteSource](/documentation/mediaextension/meestimatedsamplelocation/bytesource)
- [var estimatedSampleLocation: AVSampleCursorStorageRange](/documentation/mediaextension/meestimatedsamplelocation/estimatedsamplelocation)
- [var refinementDataLocation: AVSampleCursorStorageRange](/documentation/mediaextension/meestimatedsamplelocation/refinementdatalocation)
- [MEHEVCDependencyInfo](/documentation/mediaextension/mehevcdependencyinfo)

### Inspecting the HEVC dependency attributes of a sample

- [var hasTemporalSubLayerAccess: Bool](/documentation/mediaextension/mehevcdependencyinfo/hastemporalsublayeraccess)
- [var hasStepwiseTemporalSubLayerAccess: Bool](/documentation/mediaextension/mehevcdependencyinfo/hasstepwisetemporalsublayeraccess)
- [var syncSampleNALUnitType: Int16](/documentation/mediaextension/mehevcdependencyinfo/syncsamplenalunittype)
- [var temporalLevel: Int16](/documentation/mediaextension/mehevcdependencyinfo/temporallevel)
- [var profileSpace: Int16](/documentation/mediaextension/mehevcdependencyinfo/profilespace)
- [var tierFlag: Int16](/documentation/mediaextension/mehevcdependencyinfo/tierflag)
- [var profileIndex: Int16](/documentation/mediaextension/mehevcdependencyinfo/profileindex)
- [var profileCompatibilityFlags: Data?](/documentation/mediaextension/mehevcdependencyinfo/profilecompatibilityflags)
- [var constraintIndicatorFlags: Data?](/documentation/mediaextension/mehevcdependencyinfo/constraintindicatorflags)
- [var levelIndex: Int16](/documentation/mediaextension/mehevcdependencyinfo/levelindex)

## Byte sources

- [MEByteSource](/documentation/mediaextension/mebytesource)

### Inspecting a byte source

- [var fileName: String](/documentation/mediaextension/mebytesource/filename)
- [var fileLength: Int64](/documentation/mediaextension/mebytesource/filelength)
- [var contentType: UTType?](/documentation/mediaextension/mebytesource/contenttype)
- [var relatedFileNamesInSameDirectory: [String]](/documentation/mediaextension/mebytesource/relatedfilenamesinsamedirectory)

### Performing operations on a byte source

- [func availableLength(at: Int64) -> Int64](/documentation/mediaextension/mebytesource/availablelength(at:))
- [func byteSourceForRelatedFileName(String) throws -> MEByteSource](/documentation/mediaextension/mebytesource/bytesourceforrelatedfilename(_:))
- [func read(length: Int, from: Int64, completionHandler: (Data?, (any Error)?) -> Void)](/documentation/mediaextension/mebytesource/read(length:from:completionhandler:))

## Video decoders

- [MEVideoDecoder](/documentation/mediaextension/mevideodecoder)

### Inspecting a video decoder

- [var contentHasInterframeDependencies: Bool](/documentation/mediaextension/mevideodecoder/contenthasinterframedependencies)
- [var recommendedThreadCount: Int](/documentation/mediaextension/mevideodecoder/recommendedthreadcount)
- [var actualThreadCount: Int](/documentation/mediaextension/mevideodecoder/actualthreadcount)
- [var supportedPixelFormatsOrderedByQuality: [NSNumber]](/documentation/mediaextension/mevideodecoder/supportedpixelformatsorderedbyquality)
- [var reducedResolution: CGSize](/documentation/mediaextension/mevideodecoder/reducedresolution)
- [var pixelFormatsWithReducedResolutionDecodeSupport: [NSNumber]](/documentation/mediaextension/mevideodecoder/pixelformatswithreducedresolutiondecodesupport)
- [var producesRAWOutput: Bool](/documentation/mediaextension/mevideodecoder/producesrawoutput)
- [var isReadyForMoreMediaData: Bool](/documentation/mediaextension/mevideodecoder/isreadyformoremediadata)

### Decoding frames

- [func canAccept(CMFormatDescription) -> Bool](/documentation/mediaextension/mevideodecoder/canaccept(_:))
- [func decodeFrame(from: CMSampleBuffer, options: MEDecodeFrameOptions, completionHandler: (CVImageBuffer?, MEDecodeFrameStatus, (any Error)?) -> Void)](/documentation/mediaextension/mevideodecoder/decodeframe(from:options:completionhandler:))
- [MEDecodeFrameStatus](/documentation/mediaextension/medecodeframestatus)

#### Creating a status

- [init(rawValue: UInt)](/documentation/mediaextension/medecodeframestatus/init(rawvalue:))

#### Inspecting a status

- [static var frameDropped: MEDecodeFrameStatus](/documentation/mediaextension/medecodeframestatus/framedropped)

### Extension requirements

- [Video decoder property list dictionary](/documentation/mediaextension/video-decoder-property-list-dictionary)

#### Property list keys

- [var kMEVideoDecoderClassImplementationIDKey: String](/documentation/mediaextension/kmevideodecoderclassimplementationidkey)
- [var kMEVideoDecoderExtensionPointName: String](/documentation/mediaextension/kmevideodecoderextensionpointname)
- [var kMEVideoDecoderObjectNameKey: String](/documentation/mediaextension/kmevideodecoderobjectnamekey)
- [var kMEVideoDecoderCodecInfoKey: String](/documentation/mediaextension/kmevideodecodercodecinfokey)
- [var kMEVideoDecoderCodecTypeKey: String](/documentation/mediaextension/kmevideodecodercodectypekey)
- [var kMEVideoDecoderCodecNameKey: String](/documentation/mediaextension/kmevideodecodercodecnamekey)
- [Video decoder entitlement](/documentation/mediaextension/video-decoder-entitlement)
- [MEVideoDecoderExtension](/documentation/mediaextension/mevideodecoderextension)

### Creating a video decoder

- [init()](/documentation/mediaextension/mevideodecoderextension/init())
- [func makeVideoDecoder(codecType: CMVideoCodecType, videoFormatDescription: CMVideoFormatDescription, videoDecoderSpecifications: [String : Any], pixelBufferManager: MEVideoDecoderPixelBufferManager) throws -> any MEVideoDecoder](/documentation/mediaextension/mevideodecoderextension/makevideodecoder(codectype:videoformatdescription:videodecoderspecifications:pixelbuffermanager:))
- [MEDecodeFrameOptions](/documentation/mediaextension/medecodeframeoptions)

### Inspecting frame decoding options

- [var doNotOutputFrame: Bool](/documentation/mediaextension/medecodeframeoptions/donotoutputframe)
- [var realTimePlayback: Bool](/documentation/mediaextension/medecodeframeoptions/realtimeplayback)
- [MEVideoDecoderPixelBufferManager](/documentation/mediaextension/mevideodecoderpixelbuffermanager)

### Creating a pixel buffer

- [var pixelBufferAttributes: [String : Any]](/documentation/mediaextension/mevideodecoderpixelbuffermanager/pixelbufferattributes)
- [func makePixelBuffer() throws -> CVPixelBuffer](/documentation/mediaextension/mevideodecoderpixelbuffermanager/makepixelbuffer())

### Registering Custom Pixel Formats

- [func registerCustomPixelFormat([String : Any])](/documentation/mediaextension/mevideodecoderpixelbuffermanager/registercustompixelformat(_:))
- [Video decoder property list dictionary](/documentation/mediaextension/video-decoder-property-list-dictionary)

### Property list keys

- [var kMEVideoDecoderClassImplementationIDKey: String](/documentation/mediaextension/kmevideodecoderclassimplementationidkey)
- [var kMEVideoDecoderExtensionPointName: String](/documentation/mediaextension/kmevideodecoderextensionpointname)
- [var kMEVideoDecoderObjectNameKey: String](/documentation/mediaextension/kmevideodecoderobjectnamekey)
- [var kMEVideoDecoderCodecInfoKey: String](/documentation/mediaextension/kmevideodecodercodecinfokey)
- [var kMEVideoDecoderCodecTypeKey: String](/documentation/mediaextension/kmevideodecodercodectypekey)
- [var kMEVideoDecoderCodecNameKey: String](/documentation/mediaextension/kmevideodecodercodecnamekey)
- [Video decoder entitlement](/documentation/mediaextension/video-decoder-entitlement)

## RAW processors

- [MERAWProcessor](/documentation/mediaextension/merawprocessor)

### Inspecting a RAW processor

- [var metalDeviceRegistryID: UInt64](/documentation/mediaextension/merawprocessor/metaldeviceregistryid)
- [var outputColorAttachments: [String : Any]](/documentation/mediaextension/merawprocessor/outputcolorattachments)
- [var processingParameters: [MERAWProcessingParameter]](/documentation/mediaextension/merawprocessor/processingparameters)
- [var isReadyForMoreMediaData: Bool](/documentation/mediaextension/merawprocessor/isreadyformoremediadata)

### Processing RAW frame

- [func processFrame(fromImageBuffer: CVPixelBuffer, completionHandler: (CVPixelBuffer?, (any Error)?) -> Void)](/documentation/mediaextension/merawprocessor/processframe(fromimagebuffer:completionhandler:))

### Extension requirements

- [RAW processor property list dictionary](/documentation/mediaextension/raw-processor-property-list-dictionary)

#### Property list keys

- [var kMEVideoDecoderClassImplementationIDKey: String](/documentation/mediaextension/kmevideodecoderclassimplementationidkey)
- [var kMERAWProcessorExtensionPointName: String](/documentation/mediaextension/kmerawprocessorextensionpointname)
- [var kMEVideoDecoderObjectNameKey: String](/documentation/mediaextension/kmevideodecoderobjectnamekey)
- [var kMEVideoDecoderCodecInfoKey: String](/documentation/mediaextension/kmevideodecodercodecinfokey)
- [var kMEVideoDecoderCodecTypeKey: String](/documentation/mediaextension/kmevideodecodercodectypekey)
- [var kMEVideoDecoderCodecNameKey: String](/documentation/mediaextension/kmevideodecodercodecnamekey)
- [RAW processor entitlement](/documentation/mediaextension/raw-processor-entitlement)

### Instance Properties

- [var metadataForSidecarFile: Data](/documentation/mediaextension/merawprocessor/metadataforsidecarfile)
- [MERAWProcessorExtension](/documentation/mediaextension/merawprocessorextension)

### Creating an extension

- [init()](/documentation/mediaextension/merawprocessorextension/init())

### Creating a RAW processor

- [func makeProcessor(formatDescription: CMVideoFormatDescription, pixelBufferManager: MERAWProcessorPixelBufferManager) throws -> any MERAWProcessor](/documentation/mediaextension/merawprocessorextension/makeprocessor(formatdescription:pixelbuffermanager:))
- [MERAWProcessorPixelBufferManager](/documentation/mediaextension/merawprocessorpixelbuffermanager)

### Creating a pixel buffer

- [var pixelBufferAttributes: [String : any Sendable]](/documentation/mediaextension/merawprocessorpixelbuffermanager/pixelbufferattributes-4fe69)
- [func makePixelBuffer() throws -> CVPixelBuffer](/documentation/mediaextension/merawprocessorpixelbuffermanager/makepixelbuffer())
- [MERAWProcessingParameter](/documentation/mediaextension/merawprocessingparameter)

### Inspecting a processing parameter

- [var enabled: Bool](/documentation/mediaextension/merawprocessingparameter/enabled)
- [var key: String](/documentation/mediaextension/merawprocessingparameter/key)
- [var longDescription: String](/documentation/mediaextension/merawprocessingparameter/longdescription)
- [var name: String](/documentation/mediaextension/merawprocessingparameter/name)

### Processing parameters

- [MERAWProcessingParameter.Boolean](/documentation/mediaextension/merawprocessingparameter/boolean)

#### Creating a boolean parameter object

- [convenience init(name: String, key: String, description: String, initialValue: Bool, neutralValue: Bool?, cameraValue: Bool?)](/documentation/mediaextension/merawprocessingparameter/boolean/init(name:key:description:initialvalue:neutralvalue:cameravalue:))

#### Properties

- [var currentValue: Bool](/documentation/mediaextension/merawprocessingparameter/boolean/currentvalue)
- [var initialValue: Bool](/documentation/mediaextension/merawprocessingparameter/boolean/initialvalue)

#### Instance Properties

- [var cameraValue: Bool?](/documentation/mediaextension/merawprocessingparameter/boolean/cameravalue)
- [var neutralValue: Bool?](/documentation/mediaextension/merawprocessingparameter/boolean/neutralvalue)
- [MERAWProcessingParameter.FloatingPoint](/documentation/mediaextension/merawprocessingparameter/floatingpoint)

#### Creating a floating-point parameter object

- [convenience init(name: String, key: String, description: String, initialValue: Float, maximum: Float, minimum: Float, neutralValue: Float?, cameraValue: Float?)](/documentation/mediaextension/merawprocessingparameter/floatingpoint/init(name:key:description:initialvalue:maximum:minimum:neutralvalue:cameravalue:))

#### Properties

- [var currentValue: Float](/documentation/mediaextension/merawprocessingparameter/floatingpoint/currentvalue)
- [var initialValue: Float](/documentation/mediaextension/merawprocessingparameter/floatingpoint/initialvalue)
- [var maximumValue: Float](/documentation/mediaextension/merawprocessingparameter/floatingpoint/maximumvalue)
- [var minimumValue: Float](/documentation/mediaextension/merawprocessingparameter/floatingpoint/minimumvalue)

#### Instance Properties

- [var cameraValue: Float?](/documentation/mediaextension/merawprocessingparameter/floatingpoint/cameravalue)
- [var neutralValue: Float?](/documentation/mediaextension/merawprocessingparameter/floatingpoint/neutralvalue)
- [MERAWProcessingParameter.Integer](/documentation/mediaextension/merawprocessingparameter/integer)

#### Creating an integer parameter object

- [convenience init(name: String, key: String, description: String, initialValue: Int, maximum: Int, minimum: Int, neutralValue: Int?, cameraValue: Int?)](/documentation/mediaextension/merawprocessingparameter/integer/init(name:key:description:initialvalue:maximum:minimum:neutralvalue:cameravalue:))

#### Properties

- [var currentValue: Int](/documentation/mediaextension/merawprocessingparameter/integer/currentvalue)
- [var initialValue: Int](/documentation/mediaextension/merawprocessingparameter/integer/initialvalue)
- [var maximumValue: Int](/documentation/mediaextension/merawprocessingparameter/integer/maximumvalue)
- [var minimumValue: Int](/documentation/mediaextension/merawprocessingparameter/integer/minimumvalue)

#### Instance Properties

- [var cameraValue: Int?](/documentation/mediaextension/merawprocessingparameter/integer/cameravalue)
- [var neutralValue: Int?](/documentation/mediaextension/merawprocessingparameter/integer/neutralvalue)
- [MERAWProcessingParameter.List](/documentation/mediaextension/merawprocessingparameter/list)

#### Creating a list parameter object

- [convenience init(name: String, key: String, description: String, list: [MERAWProcessingParameter.ListElement], initialValue: Int, neutralValue: Int?, cameraValue: Int?)](/documentation/mediaextension/merawprocessingparameter/list/init(name:key:description:list:initialvalue:neutralvalue:cameravalue:))

#### Properties

- [var currentValue: Int](/documentation/mediaextension/merawprocessingparameter/list/currentvalue)
- [var initialValue: Int](/documentation/mediaextension/merawprocessingparameter/list/initialvalue)
- [var listElements: [MERAWProcessingParameter.ListElement]](/documentation/mediaextension/merawprocessingparameter/list/listelements)

#### Instance Properties

- [var cameraValue: Int?](/documentation/mediaextension/merawprocessingparameter/list/cameravalue)
- [var neutralValue: Int?](/documentation/mediaextension/merawprocessingparameter/list/neutralvalue)
- [MERAWProcessingParameter.ListElement](/documentation/mediaextension/merawprocessingparameter/listelement)

#### Creating a list element parameter object

- [init(name: String, description: String, elementID: Int)](/documentation/mediaextension/merawprocessingparameter/listelement/init(name:description:elementid:))

#### Properties

- [var listElementID: Int](/documentation/mediaextension/merawprocessingparameter/listelement/listelementid)
- [MERAWProcessingParameter.SubGroup](/documentation/mediaextension/merawprocessingparameter/subgroup)

#### Creating a sub group parameter object

- [init(name: String, description: String, parameters: [MERAWProcessingParameter])](/documentation/mediaextension/merawprocessingparameter/subgroup/init(name:description:parameters:))

#### Properties

- [var subGroupParameters: [MERAWProcessingParameter]](/documentation/mediaextension/merawprocessingparameter/subgroup/subgroupparameters)

### Class methods

- [class func boolean(name: String, key: String, description: String, initialValue: Bool, neutralValue: Bool?, cameraValue: Bool?) -> MERAWProcessingParameter.Boolean](/documentation/mediaextension/merawprocessingparameter/boolean(name:key:description:initialvalue:neutralvalue:cameravalue:))
- [class func integer(name: String, key: String, description: String, initialValue: Int, maximum: Int, minimum: Int, neutralValue: Int?, cameraValue: Int?) -> MERAWProcessingParameter.Integer](/documentation/mediaextension/merawprocessingparameter/integer(name:key:description:initialvalue:maximum:minimum:neutralvalue:cameravalue:))
- [class func list(name: String, key: String, description: String, list: [MERAWProcessingParameter.ListElement], initialValue: Int, neutralValue: Int?, cameraValue: Int?) -> MERAWProcessingParameter.List](/documentation/mediaextension/merawprocessingparameter/list(name:key:description:list:initialvalue:neutralvalue:cameravalue:))
- [class func listElement(name: String, description: String, elementID: Int) -> MERAWProcessingParameter.ListElement](/documentation/mediaextension/merawprocessingparameter/listelement(name:description:elementid:))
- [class func subGroup(name: String, description: String, parameters: [MERAWProcessingParameter]) -> MERAWProcessingParameter.SubGroup](/documentation/mediaextension/merawprocessingparameter/subgroup(name:description:parameters:))
- [class func float(name: String, key: String, description: String, initialValue: Float, maximum: Float, minimum: Float, neutralValue: Float?, cameraValue: Float?) -> MERAWProcessingParameter.FloatingPoint](/documentation/mediaextension/merawprocessingparameter/float(name:key:description:initialvalue:maximum:minimum:neutralvalue:cameravalue:))
- [MERAWProcessorNotification](/documentation/mediaextension/merawprocessornotification)

### Type Properties

- [static let readyForMoreMediaDataDidChange: NSNotification.Name](/documentation/mediaextension/merawprocessornotification/readyformoremediadatadidchange)
- [static let valuesDidChange: NSNotification.Name](/documentation/mediaextension/merawprocessornotification/valuesdidchange)
- [RAW processor property list dictionary](/documentation/mediaextension/raw-processor-property-list-dictionary)

### Property list keys

- [var kMEVideoDecoderClassImplementationIDKey: String](/documentation/mediaextension/kmevideodecoderclassimplementationidkey)
- [var kMERAWProcessorExtensionPointName: String](/documentation/mediaextension/kmerawprocessorextensionpointname)
- [var kMEVideoDecoderObjectNameKey: String](/documentation/mediaextension/kmevideodecoderobjectnamekey)
- [var kMEVideoDecoderCodecInfoKey: String](/documentation/mediaextension/kmevideodecodercodecinfokey)
- [var kMEVideoDecoderCodecTypeKey: String](/documentation/mediaextension/kmevideodecodercodectypekey)
- [var kMEVideoDecoderCodecNameKey: String](/documentation/mediaextension/kmevideodecodercodecnamekey)
- [RAW processor entitlement](/documentation/mediaextension/raw-processor-entitlement)

## Errors

- [let MediaExtensionErrorDomain: String](/documentation/mediaextension/mediaextensionerrordomain)
- [MEError](/documentation/mediaextension/meerror-swift.struct)

### Identifying the error domain and codes

- [static var allocationFailure: MEError.Code](/documentation/mediaextension/meerror-swift.struct/allocationfailure)
- [static var endOfStream: MEError.Code](/documentation/mediaextension/meerror-swift.struct/endofstream)
- [static var internalFailure: MEError.Code](/documentation/mediaextension/meerror-swift.struct/internalfailure)
- [static var invalidParameter: MEError.Code](/documentation/mediaextension/meerror-swift.struct/invalidparameter)
- [static var locationNotAvailable: MEError.Code](/documentation/mediaextension/meerror-swift.struct/locationnotavailable)
- [static var noSamples: MEError.Code](/documentation/mediaextension/meerror-swift.struct/nosamples)
- [static var noSuchEdit: MEError.Code](/documentation/mediaextension/meerror-swift.struct/nosuchedit)
- [static var parsingFailure: MEError.Code](/documentation/mediaextension/meerror-swift.struct/parsingfailure)
- [static var permissionDenied: MEError.Code](/documentation/mediaextension/meerror-swift.struct/permissiondenied)
- [static var propertyNotSupported: MEError.Code](/documentation/mediaextension/meerror-swift.struct/propertynotsupported)
- [static var referenceMissing: MEError.Code](/documentation/mediaextension/meerror-swift.struct/referencemissing)
- [static var unsupportedFeature: MEError.Code](/documentation/mediaextension/meerror-swift.struct/unsupportedfeature)

### Inspecting an error

- [var code: Int](/documentation/foundation/nserror/code)
- [var errorCode: Int](/documentation/foundation/customnserror/errorcode)
- [var errorUserInfo: [String : Any]](/documentation/foundation/customnserror/erroruserinfo)
- [var hashValue: Int](/documentation/swift/hashable/hashvalue)
- [var userInfo: [String : Any]](/documentation/foundation/nserror/userinfo)
- [static func != (Self, Self) -> Bool](/documentation/swift/equatable/!=(_:_:))
- [MEError.Code](/documentation/mediaextension/meerror-swift.struct/code)

#### Error codes

- [case allocationFailure](/documentation/mediaextension/meerror-swift.struct/code/allocationfailure)
- [case endOfStream](/documentation/mediaextension/meerror-swift.struct/code/endofstream)
- [case internalFailure](/documentation/mediaextension/meerror-swift.struct/code/internalfailure)
- [case invalidParameter](/documentation/mediaextension/meerror-swift.struct/code/invalidparameter)
- [case locationNotAvailable](/documentation/mediaextension/meerror-swift.struct/code/locationnotavailable)
- [case noSamples](/documentation/mediaextension/meerror-swift.struct/code/nosamples)
- [case noSuchEdit](/documentation/mediaextension/meerror-swift.struct/code/nosuchedit)
- [case parsingFailure](/documentation/mediaextension/meerror-swift.struct/code/parsingfailure)
- [case permissionDenied](/documentation/mediaextension/meerror-swift.struct/code/permissiondenied)
- [case propertyNotSupported](/documentation/mediaextension/meerror-swift.struct/code/propertynotsupported)
- [case referenceMissing](/documentation/mediaextension/meerror-swift.struct/code/referencemissing)
- [case unsupportedFeature](/documentation/mediaextension/meerror-swift.struct/code/unsupportedfeature)

#### Initializers

- [init?(rawValue: Int)](/documentation/mediaextension/meerror-swift.struct/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/mediaextension/meerror-swift.struct/errordomain)
- [MEError.Code](/documentation/mediaextension/meerror-swift.struct/code)

### Error codes

- [case allocationFailure](/documentation/mediaextension/meerror-swift.struct/code/allocationfailure)
- [case endOfStream](/documentation/mediaextension/meerror-swift.struct/code/endofstream)
- [case internalFailure](/documentation/mediaextension/meerror-swift.struct/code/internalfailure)
- [case invalidParameter](/documentation/mediaextension/meerror-swift.struct/code/invalidparameter)
- [case locationNotAvailable](/documentation/mediaextension/meerror-swift.struct/code/locationnotavailable)
- [case noSamples](/documentation/mediaextension/meerror-swift.struct/code/nosamples)
- [case noSuchEdit](/documentation/mediaextension/meerror-swift.struct/code/nosuchedit)
- [case parsingFailure](/documentation/mediaextension/meerror-swift.struct/code/parsingfailure)
- [case permissionDenied](/documentation/mediaextension/meerror-swift.struct/code/permissiondenied)
- [case propertyNotSupported](/documentation/mediaextension/meerror-swift.struct/code/propertynotsupported)
- [case referenceMissing](/documentation/mediaextension/meerror-swift.struct/code/referencemissing)
- [case unsupportedFeature](/documentation/mediaextension/meerror-swift.struct/code/unsupportedfeature)

### Initializers

- [init?(rawValue: Int)](/documentation/mediaextension/meerror-swift.struct/code/init(rawvalue:))

## Variables

- [var kMERAWProcessorClassImplementationIDKey: String](/documentation/mediaextension/kmerawprocessorclassimplementationidkey)
- [var kMERAWProcessorCodecNameKey: String](/documentation/mediaextension/kmerawprocessorcodecnamekey)
- [var kMERAWProcessorCodecTypeKey: String](/documentation/mediaextension/kmerawprocessorcodectypekey)
- [var kMERAWProcessorObjectNameKey: String](/documentation/mediaextension/kmerawprocessorobjectnamekey)
- [var kMERAWProcessorProcessorInfoKey: String](/documentation/mediaextension/kmerawprocessorprocessorinfokey)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
