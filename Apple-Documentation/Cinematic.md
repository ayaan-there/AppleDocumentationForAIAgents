# Cinematic Documentation

Source: https://sosumi.ai/documentation/cinematic

---
title: Cinematic
source: https://developer.apple.com/documentation/cinematic
timestamp: 2026-02-13T18:54:45.523Z
---

## Essentials

- [Playing and editing Cinematic mode video](/documentation/cinematic/playing-and-editing-cinematic-mode-video)
- [CNScript](/documentation/cinematic/cnscript-1ispe)

### Structures

- [CNScript.Changes](/documentation/cinematic/cnscript-1ispe/changes)

#### Initializers

- [init?(dataRepresentation: Data)](/documentation/cinematic/cnscript-1ispe/changes/init(datarepresentation:))

#### Instance Properties

- [var addedDetectionTracks: [CNDetectionTrack]](/documentation/cinematic/cnscript-1ispe/changes/addeddetectiontracks)
- [var dataRepresentation: Data](/documentation/cinematic/cnscript-1ispe/changes/datarepresentation)
- [var fNumber: Float](/documentation/cinematic/cnscript-1ispe/changes/fnumber)
- [var userDecisions: [CNDecision]](/documentation/cinematic/cnscript-1ispe/changes/userdecisions)
- [CNScript.Frame](/documentation/cinematic/cnscript-1ispe/frame)

#### Instance Properties

- [var allDetections: [CNDetection]](/documentation/cinematic/cnscript-1ispe/frame/alldetections)
- [var focusDetection: CNDetection](/documentation/cinematic/cnscript-1ispe/frame/focusdetection)
- [var focusDisparity: Float](/documentation/cinematic/cnscript-1ispe/frame/focusdisparity)
- [var time: CMTime](/documentation/cinematic/cnscript-1ispe/frame/time)

#### Instance Methods

- [func bestDetection(for: CNDetectionGroupID) -> CNDetection?](/documentation/cinematic/cnscript-1ispe/frame/bestdetection(for:))
- [func detection(for: CNDetectionID) -> CNDetection?](/documentation/cinematic/cnscript-1ispe/frame/detection(for:))

### Initializers

- [init(asset: AVAsset, changes: CNScript.Changes?, progress: Progress?) async throws](/documentation/cinematic/cnscript-1ispe/init(asset:changes:progress:))

### Instance Properties

- [var addedDetectionTracks: [CNDetectionTrack]](/documentation/cinematic/cnscript-1ispe/addeddetectiontracks)
- [var fNumber: Float](/documentation/cinematic/cnscript-1ispe/fnumber)
- [var timeRange: CMTimeRange](/documentation/cinematic/cnscript-1ispe/timerange)

### Instance Methods

- [func addDetectionTrack(CNDetectionTrack) -> CNDetectionID](/documentation/cinematic/cnscript-1ispe/adddetectiontrack(_:))
- [func addUserDecision(CNDecision) -> Bool](/documentation/cinematic/cnscript-1ispe/adduserdecision(_:))
- [func baseDecisions(in: CMTimeRange) -> [CNDecision]](/documentation/cinematic/cnscript-1ispe/basedecisions(in:))
- [func changes() -> CNScript.Changes](/documentation/cinematic/cnscript-1ispe/changes())
- [func changes(trimmedBy: CMTimeRange) -> CNScript.Changes](/documentation/cinematic/cnscript-1ispe/changes(trimmedby:))
- [func decision(after: CMTime) -> CNDecision?](/documentation/cinematic/cnscript-1ispe/decision(after:))
- [func decision(at: CMTime, tolerance: CMTime) -> CNDecision?](/documentation/cinematic/cnscript-1ispe/decision(at:tolerance:))
- [func decision(before: CMTime) -> CNDecision?](/documentation/cinematic/cnscript-1ispe/decision(before:))
- [func decisions(in: CMTimeRange) -> [CNDecision]](/documentation/cinematic/cnscript-1ispe/decisions(in:))
- [func detectionTrack(for: CNDecision) -> CNDetectionTrack?](/documentation/cinematic/cnscript-1ispe/detectiontrack(for:)-1xvsa)
- [func detectionTrack(for: CNDetectionID) -> CNDetectionTrack?](/documentation/cinematic/cnscript-1ispe/detectiontrack(for:)-6f8mk)
- [func frame(at: CMTime, tolerance: CMTime) -> CNScript.Frame?](/documentation/cinematic/cnscript-1ispe/frame(at:tolerance:))
- [func frames(in: CMTimeRange) -> [CNScript.Frame]](/documentation/cinematic/cnscript-1ispe/frames(in:))
- [func primaryDecision(at: CMTime) -> CNDecision?](/documentation/cinematic/cnscript-1ispe/primarydecision(at:))
- [func reload(changes: CNScript.Changes?)](/documentation/cinematic/cnscript-1ispe/reload(changes:))
- [func removeAllUserDecisions()](/documentation/cinematic/cnscript-1ispe/removealluserdecisions())
- [func removeDetectionTrack(CNDetectionTrack) -> Bool](/documentation/cinematic/cnscript-1ispe/removedetectiontrack(_:))
- [func removeUserDecision(CNDecision) -> Bool](/documentation/cinematic/cnscript-1ispe/removeuserdecision(_:))
- [func secondaryDecision(at: CMTime) -> CNDecision?](/documentation/cinematic/cnscript-1ispe/secondarydecision(at:))
- [func timeRangeOfTransition(after: CNDecision) -> CMTimeRange](/documentation/cinematic/cnscript-1ispe/timerangeoftransition(after:))
- [func timeRangeOfTransition(before: CNDecision) -> CMTimeRange](/documentation/cinematic/cnscript-1ispe/timerangeoftransition(before:))
- [func userDecisions(in: CMTimeRange) -> [CNDecision]](/documentation/cinematic/cnscript-1ispe/userdecisions(in:))

## Reading and rendering

- [CNAssetInfo](/documentation/cinematic/cnassetinfo-2ata2)

### Initializers

- [init(asset: AVAsset) async throws](/documentation/cinematic/cnassetinfo-2ata2/init(asset:))

### Instance Properties

- [var allCinematicTracks: [AVAssetTrack]](/documentation/cinematic/cnassetinfo-2ata2/allcinematictracks)
- [let asset: AVAsset](/documentation/cinematic/cnassetinfo-2ata2/asset)
- [var cinematicDisparityTrack: AVAssetTrack](/documentation/cinematic/cnassetinfo-2ata2/cinematicdisparitytrack)
- [var cinematicMetadataTrack: AVAssetTrack](/documentation/cinematic/cnassetinfo-2ata2/cinematicmetadatatrack)
- [var cinematicVideoTrack: AVAssetTrack](/documentation/cinematic/cnassetinfo-2ata2/cinematicvideotrack)
- [var frameTimingTrack: AVAssetTrack](/documentation/cinematic/cnassetinfo-2ata2/frametimingtrack)
- [var naturalSize: CGSize](/documentation/cinematic/cnassetinfo-2ata2/naturalsize)
- [var preferredSize: CGSize](/documentation/cinematic/cnassetinfo-2ata2/preferredsize)
- [var preferredTransform: CGAffineTransform](/documentation/cinematic/cnassetinfo-2ata2/preferredtransform)
- [var sampleDataTrackIDs: [CMPersistentTrackID]](/documentation/cinematic/cnassetinfo-2ata2/sampledatatrackids)
- [var timeRange: CMTimeRange](/documentation/cinematic/cnassetinfo-2ata2/timerange)
- [var videoCompositionTrackIDs: [CMPersistentTrackID]](/documentation/cinematic/cnassetinfo-2ata2/videocompositiontrackids)
- [var videoCompositionTracks: [AVAssetTrack]](/documentation/cinematic/cnassetinfo-2ata2/videocompositiontracks)

### Type Methods

- [class func isCinematic(asset: AVAsset) async -> Bool](/documentation/cinematic/cnassetinfo-2ata2/iscinematic(asset:))
- [CNCompositionInfo](/documentation/cinematic/cncompositioninfo-7eunn)

### Instance Methods

- [func insertTimeRange(CMTimeRange, of: CNAssetInfo, at: CMTime) throws](/documentation/cinematic/cncompositioninfo-7eunn/inserttimerange(_:of:at:))
- [CNRenderingSession](/documentation/cinematic/cnrenderingsession-1hzh8)

### Structures

- [CNRenderingSession.Attributes](/documentation/cinematic/cnrenderingsession-1hzh8/attributes)

#### Initializers

- [init(asset: AVAsset) async throws](/documentation/cinematic/cnrenderingsession-1hzh8/attributes/init(asset:))

#### Instance Properties

- [let renderingVersion: Int](/documentation/cinematic/cnrenderingsession-1hzh8/attributes/renderingversion)
- [CNRenderingSession.FrameAttributes](/documentation/cinematic/cnrenderingsession-1hzh8/frameattributes)

#### Initializers

- [init?(sampleBuffer: CMSampleBuffer, sessionAttributes: CNRenderingSession.Attributes)](/documentation/cinematic/cnrenderingsession-1hzh8/frameattributes/init(samplebuffer:sessionattributes:))
- [init?(timedMetadataGroup: AVTimedMetadataGroup, sessionAttributes: CNRenderingSession.Attributes)](/documentation/cinematic/cnrenderingsession-1hzh8/frameattributes/init(timedmetadatagroup:sessionattributes:))

#### Instance Properties

- [var fNumber: Float](/documentation/cinematic/cnrenderingsession-1hzh8/frameattributes/fnumber)
- [var focusDisparity: Float](/documentation/cinematic/cnrenderingsession-1hzh8/frameattributes/focusdisparity)

### Initializers

- [init(commandQueue: any MTLCommandQueue, sessionAttributes: CNRenderingSession.Attributes, preferredTransform: CGAffineTransform, quality: CNRenderingQuality)](/documentation/cinematic/cnrenderingsession-1hzh8/init(commandqueue:sessionattributes:preferredtransform:quality:))

### Instance Properties

- [let commandQueue: any MTLCommandQueue](/documentation/cinematic/cnrenderingsession-1hzh8/commandqueue)
- [let preferredTransform: CGAffineTransform](/documentation/cinematic/cnrenderingsession-1hzh8/preferredtransform)
- [let quality: CNRenderingQuality](/documentation/cinematic/cnrenderingsession-1hzh8/quality)
- [let sessionAttributes: CNRenderingSession.Attributes](/documentation/cinematic/cnrenderingsession-1hzh8/sessionattributes)

### Instance Methods

- [func encodeRender(to: any MTLCommandBuffer, frameAttributes: CNRenderingSession.FrameAttributes, sourceImage: CVPixelBuffer, sourceDisparity: CVPixelBuffer, destinationImage: CVPixelBuffer) -> Bool](/documentation/cinematic/cnrenderingsession-1hzh8/encoderender(to:frameattributes:sourceimage:sourcedisparity:destinationimage:))
- [func encodeRender(to: any MTLCommandBuffer, frameAttributes: CNRenderingSession.FrameAttributes, sourceImage: CVPixelBuffer, sourceDisparity: CVPixelBuffer, destinationLuma: any MTLTexture, destinationChroma: any MTLTexture) -> Bool](/documentation/cinematic/cnrenderingsession-1hzh8/encoderender(to:frameattributes:sourceimage:sourcedisparity:destinationluma:destinationchroma:))
- [func encodeRender(to: any MTLCommandBuffer, frameAttributes: CNRenderingSession.FrameAttributes, sourceImage: CVPixelBuffer, sourceDisparity: CVPixelBuffer, destinationRGBA: any MTLTexture) -> Bool](/documentation/cinematic/cnrenderingsession-1hzh8/encoderender(to:frameattributes:sourceimage:sourcedisparity:destinationrgba:))

### Type Properties

- [static var destinationPixelFormatTypes: [OSType]](/documentation/cinematic/cnrenderingsession-1hzh8/destinationpixelformattypes)
- [static var sourcePixelFormatTypes: [OSType]](/documentation/cinematic/cnrenderingsession-1hzh8/sourcepixelformattypes)

## Editing

- [Editing Spatial Audio with an audio mix](/documentation/cinematic/editing-spatial-audio-with-an-audio-mix)
- [CNDetection](/documentation/cinematic/cndetection-swift.struct)

### Initializers

- [init(time: CMTime, detectionType: CNDetectionType, normalizedRect: CGRect, focusDisparity: Float)](/documentation/cinematic/cndetection-swift.struct/init(time:detectiontype:normalizedrect:focusdisparity:))

### Instance Properties

- [var detectionGroupID: CNDetectionGroupID?](/documentation/cinematic/cndetection-swift.struct/detectiongroupid)
- [var detectionID: CNDetectionID?](/documentation/cinematic/cndetection-swift.struct/detectionid)
- [var detectionType: CNDetectionType](/documentation/cinematic/cndetection-swift.struct/detectiontype)
- [var focusDisparity: Float](/documentation/cinematic/cndetection-swift.struct/focusdisparity)
- [var normalizedRect: CGRect](/documentation/cinematic/cndetection-swift.struct/normalizedrect)
- [var time: CMTime](/documentation/cinematic/cndetection-swift.struct/time)

### Type Methods

- [static func accessibilityLabel(for: CNDetectionType) -> String](/documentation/cinematic/cndetection-swift.struct/accessibilitylabel(for:))
- [static func disparity(in: CGRect, sourceDisparity: CVPixelBuffer, detectionType: CNDetectionType, priorDisparity: Float?) -> Float](/documentation/cinematic/cndetection-swift.struct/disparity(in:sourcedisparity:detectiontype:priordisparity:))
- [CNDecision](/documentation/cinematic/cndecision-swift.struct)

### Initializers

- [init(time: CMTime, detectionGroupID: CNDetectionGroupID, strong: Bool)](/documentation/cinematic/cndecision-swift.struct/init(time:detectiongroupid:strong:))
- [init(time: CMTime, detectionID: CNDetectionID, strong: Bool)](/documentation/cinematic/cndecision-swift.struct/init(time:detectionid:strong:))

### Instance Properties

- [var focusDetectionID: CNDecision.FocusDetectionID](/documentation/cinematic/cndecision-swift.struct/focusdetectionid-swift.property)
- [var isStrongDecision: Bool](/documentation/cinematic/cndecision-swift.struct/isstrongdecision)
- [var isUserDecision: Bool](/documentation/cinematic/cndecision-swift.struct/isuserdecision)
- [var time: CMTime](/documentation/cinematic/cndecision-swift.struct/time)

### Enumerations

- [CNDecision.FocusDetectionID](/documentation/cinematic/cndecision-swift.struct/focusdetectionid-swift.enum)

#### Enumeration Casese

- [case group(CNDetectionGroupID)](/documentation/cinematic/cndecision-swift.struct/focusdetectionid-swift.enum/group(_:))
- [case single(CNDetectionID)](/documentation/cinematic/cndecision-swift.struct/focusdetectionid-swift.enum/single(_:))
- [CNDetectionTrack](/documentation/cinematic/cndetectiontrack-2bxtd)

### Instance Properties

- [var detectionGroupID: CNDetectionGroupID](/documentation/cinematic/cndetectiontrack-2bxtd/detectiongroupid)
- [var detectionID: CNDetectionID](/documentation/cinematic/cndetectiontrack-2bxtd/detectionid)
- [var detectionType: CNDetectionType](/documentation/cinematic/cndetectiontrack-2bxtd/detectiontype)
- [var isDiscrete: Bool](/documentation/cinematic/cndetectiontrack-2bxtd/isdiscrete)
- [var isUserCreated: Bool](/documentation/cinematic/cndetectiontrack-2bxtd/isusercreated)

### Instance Methods

- [func detection(atOrBefore: CMTime) -> CNDetection?](/documentation/cinematic/cndetectiontrack-2bxtd/detection(atorbefore:))
- [func detection(nearest: CMTime) -> CNDetection?](/documentation/cinematic/cndetectiontrack-2bxtd/detection(nearest:))
- [func detections(in: CMTimeRange) -> [CNDetection]](/documentation/cinematic/cndetectiontrack-2bxtd/detections(in:))
- [CNFixedDetectionTrack](/documentation/cinematic/cnfixeddetectiontrack-93rrw)

### Initializers

- [init(focusDisparity: Float)](/documentation/cinematic/cnfixeddetectiontrack-93rrw/init(focusdisparity:))
- [init(originalDetection: CNDetection)](/documentation/cinematic/cnfixeddetectiontrack-93rrw/init(originaldetection:))

### Instance Properties

- [var focusDisparity: Float](/documentation/cinematic/cnfixeddetectiontrack-93rrw/focusdisparity)
- [var originalDetection: CNDetection?](/documentation/cinematic/cnfixeddetectiontrack-93rrw/originaldetection)
- [CNCustomDetectionTrack](/documentation/cinematic/cncustomdetectiontrack-9a2zo)

### Initializers

- [init(detections: [CNDetection], smooth: Bool)](/documentation/cinematic/cncustomdetectiontrack-9a2zo/init(detections:smooth:))

### Instance Properties

- [var allDetections: [CNDetection]](/documentation/cinematic/cncustomdetectiontrack-9a2zo/alldetections)
- [CNDetectionType](/documentation/cinematic/cndetectiontype)

### Enumeration Cases

- [case autoFocus](/documentation/cinematic/cndetectiontype/autofocus)
- [case catBody](/documentation/cinematic/cndetectiontype/catbody)
- [case catHead](/documentation/cinematic/cndetectiontype/cathead)
- [case custom](/documentation/cinematic/cndetectiontype/custom)
- [case dogBody](/documentation/cinematic/cndetectiontype/dogbody)
- [case dogHead](/documentation/cinematic/cndetectiontype/doghead)
- [case fixedFocus](/documentation/cinematic/cndetectiontype/fixedfocus)
- [case humanFace](/documentation/cinematic/cndetectiontype/humanface)
- [case humanHead](/documentation/cinematic/cndetectiontype/humanhead)
- [case humanTorso](/documentation/cinematic/cndetectiontype/humantorso)
- [case sportsBall](/documentation/cinematic/cndetectiontype/sportsball)
- [case unknown](/documentation/cinematic/cndetectiontype/unknown)

### Initializers

- [init?(rawValue: Int)](/documentation/cinematic/cndetectiontype/init(rawvalue:))

## Custom Object Tracking

- [CNBoundsPrediction](/documentation/cinematic/cnboundsprediction-swift.struct)

### Instance Properties

- [var confidence: Float](/documentation/cinematic/cnboundsprediction-swift.struct/confidence)
- [var normalizedBounds: CGRect](/documentation/cinematic/cnboundsprediction-swift.struct/normalizedbounds)
- [CNObjectTracker](/documentation/cinematic/cnobjecttracker-1n598)

### Initializers

- [init(commandQueue: any MTLCommandQueue)](/documentation/cinematic/cnobjecttracker-1n598/init(commandqueue:))

### Instance Methods

- [func continueTracking(at: CMTime, sourceImage: CVPixelBuffer, sourceDisparity: CVPixelBuffer) -> CNBoundsPrediction?](/documentation/cinematic/cnobjecttracker-1n598/continuetracking(at:sourceimage:sourcedisparity:))
- [func findObject(at: CGPoint, sourceImage: CVPixelBuffer) -> CNBoundsPrediction?](/documentation/cinematic/cnobjecttracker-1n598/findobject(at:sourceimage:))
- [func finishDetectionTrack() -> CNDetectionTrack](/documentation/cinematic/cnobjecttracker-1n598/finishdetectiontrack())
- [func resetDetectionTrack()](/documentation/cinematic/cnobjecttracker-1n598/resetdetectiontrack())
- [func startTracking(at: CMTime, within: CGRect, sourceImage: CVPixelBuffer, sourceDisparity: CVPixelBuffer) -> Bool](/documentation/cinematic/cnobjecttracker-1n598/starttracking(at:within:sourceimage:sourcedisparity:))

### Type Properties

- [static var isSupported: Bool](/documentation/cinematic/cnobjecttracker-1n598/issupported)

## Structures

- [CNCinematicError](/documentation/cinematic/cncinematicerror)

### Type Properties

- [static var cancelled: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/cancelled)
- [static var errorDomain: String](/documentation/cinematic/cncinematicerror/errordomain)
- [static var incompatible: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/incompatible)
- [static var incomplete: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/incomplete)
- [static var malformed: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/malformed)
- [static var unknown: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/unknown)
- [static var unreadable: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/unreadable)
- [static var unsupported: CNCinematicError.Code](/documentation/cinematic/cncinematicerror/unsupported)

## Reference

- [Cinematic Enumerations](/documentation/cinematic/cinematic-enumerations)

### Enumerations

- [CNRenderingQuality](/documentation/cinematic/cnrenderingquality)

#### Enumeration Cases

- [case export](/documentation/cinematic/cnrenderingquality/export)
- [case exportHigh](/documentation/cinematic/cnrenderingquality/exporthigh)
- [case preview](/documentation/cinematic/cnrenderingquality/preview)
- [case thumbnail](/documentation/cinematic/cnrenderingquality/thumbnail)

#### Initializers

- [init?(rawValue: Int)](/documentation/cinematic/cnrenderingquality/init(rawvalue:))
- [CNCinematicError.Code](/documentation/cinematic/cncinematicerror/code)

#### Enumeration Cases

- [case cancelled](/documentation/cinematic/cncinematicerror/code/cancelled)
- [case incompatible](/documentation/cinematic/cncinematicerror/code/incompatible)
- [case incomplete](/documentation/cinematic/cncinematicerror/code/incomplete)
- [case malformed](/documentation/cinematic/cncinematicerror/code/malformed)
- [case unknown](/documentation/cinematic/cncinematicerror/code/unknown)
- [case unreadable](/documentation/cinematic/cncinematicerror/code/unreadable)
- [case unsupported](/documentation/cinematic/cncinematicerror/code/unsupported)

#### Initializers

- [init?(rawValue: Int)](/documentation/cinematic/cncinematicerror/code/init(rawvalue:))
- [Cinematic Constants](/documentation/cinematic/cinematic-constants)

### Enumerations

- [let CNCinematicErrorDomain: String](/documentation/cinematic/cncinematicerrordomain)
- [Cinematic Data Types](/documentation/cinematic/cinematic-data-types)

### Data Types

- [CNDetectionGroupID](/documentation/cinematic/cndetectiongroupid)

#### Initializers

- [init(Int64)](/documentation/cinematic/cndetectiongroupid/init(_:))
- [init(rawValue: Int64)](/documentation/cinematic/cndetectiongroupid/init(rawvalue:))
- [CNDetectionID](/documentation/cinematic/cndetectionid)

#### Initializers

- [init(Int64)](/documentation/cinematic/cndetectionid/init(_:))
- [init(rawValue: Int64)](/documentation/cinematic/cndetectionid/init(rawvalue:))

## Classes

- [CNAssetSpatialAudioInfo](/documentation/cinematic/cnassetspatialaudioinfo-7hdev)

### Initializers

- [init(asset: AVAsset) async throws](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/init(asset:))

### Instance Properties

- [var defaultEffectIntensity: Float32](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/defaulteffectintensity)
- [var defaultRenderingStyle: CNSpatialAudioRenderingStyle](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/defaultrenderingstyle)
- [var defaultSpatialAudioTrack: AVAssetTrack](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/defaultspatialaudiotrack)
- [var spatialAudioMixMetadata: Data](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/spatialaudiomixmetadata)

### Instance Methods

- [func assetReaderOutputSettings(for: CNSpatialAudioContentType) -> Dictionary<String, Any>](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/assetreaderoutputsettings(for:))
- [func assetWriterInputSettings(for: CNSpatialAudioContentType) -> Dictionary<String, Any>](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/assetwriterinputsettings(for:))
- [func audioMix(effectIntensity: Float32, renderingStyle: CNSpatialAudioRenderingStyle) -> AVAudioMix](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/audiomix(effectintensity:renderingstyle:))

### Type Properties

- [static var isSupported: Bool](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/issupported)

### Type Methods

- [class func assetContainsSpatialAudio(asset: AVAsset) async -> Bool](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/assetcontainsspatialaudio(asset:))
- [class func checkIfContainsSpatialAudio(asset: AVAsset, completionHandler: (Bool) -> Void)](/documentation/cinematic/cnassetspatialaudioinfo-7hdev/checkifcontainsspatialaudio(asset:completionhandler:))

## Enumerations

- [CNSpatialAudioContentType](/documentation/cinematic/cnspatialaudiocontenttype)

### Enumeration Cases

- [case spatial](/documentation/cinematic/cnspatialaudiocontenttype/spatial)
- [case stereo](/documentation/cinematic/cnspatialaudiocontenttype/stereo)

### Initializers

- [init?(rawValue: Int)](/documentation/cinematic/cnspatialaudiocontenttype/init(rawvalue:))
- [CNSpatialAudioRenderingStyle](/documentation/cinematic/cnspatialaudiorenderingstyle)

### Enumeration Cases

- [case cinematic](/documentation/cinematic/cnspatialaudiorenderingstyle/cinematic)
- [case cinematicBackgroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/cinematicbackgroundstem)
- [case cinematicForegroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/cinematicforegroundstem)
- [case inFrame](/documentation/cinematic/cnspatialaudiorenderingstyle/inframe)
- [case inFrameBackgroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/inframebackgroundstem)
- [case inFrameForegroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/inframeforegroundstem)
- [case standard](/documentation/cinematic/cnspatialaudiorenderingstyle/standard)
- [case studio](/documentation/cinematic/cnspatialaudiorenderingstyle/studio)
- [case studioBackgroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/studiobackgroundstem)
- [case studioForegroundStem](/documentation/cinematic/cnspatialaudiorenderingstyle/studioforegroundstem)

### Initializers

- [init?(rawValue: Int)](/documentation/cinematic/cnspatialaudiorenderingstyle/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
