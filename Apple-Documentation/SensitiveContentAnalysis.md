# SensitiveContentAnalysis Documentation

Source: https://sosumi.ai/documentation/sensitivecontentanalysis

---
title: SensitiveContentAnalysis
source: https://developer.apple.com/documentation/sensitivecontentanalysis
timestamp: 2026-02-13T19:01:57.441Z
---

## Setup

- [Detecting nudity in media and providing intervention options](/documentation/sensitivecontentanalysis/detecting-nudity-in-media-and-providing-intervention-options)

## Authorization

- [com.apple.developer.sensitivecontentanalysis.client](/documentation/bundleresources/entitlements/com.apple.developer.sensitivecontentanalysis.client)

## Image and video file analysis

- [SCSensitivityAnalyzer](/documentation/sensitivecontentanalysis/scsensitivityanalyzer)

### Creating a sensitivity analyzer

- [init()](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/init())

### Determining a nudity detection strategy

- [var analysisPolicy: SCSensitivityAnalysisPolicy](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/analysispolicy)

### Analyzing images

- [func analyzeImage(CGImage, completionHandler: (SCSensitivityAnalysis?, (any Error)?) -> Void)](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/analyzeimage(_:completionhandler:))
- [func analyzeImage(at: URL, completionHandler: (SCSensitivityAnalysis?, (any Error)?) -> Void)](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/analyzeimage(at:completionhandler:))

### Analyzing video

- [func videoAnalysis(forFileAt: URL) -> SCSensitivityAnalyzer.VideoAnalysisHandler](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/videoanalysis(forfileat:))
- [SCSensitivityAnalyzer.VideoAnalysisHandler](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/videoanalysishandler)

#### Checking progress

- [var progress: Progress](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/videoanalysishandler/progress)

#### Determining sensitivity

- [func hasSensitiveContent() async throws -> SCSensitivityAnalysis](/documentation/sensitivecontentanalysis/scsensitivityanalyzer/videoanalysishandler/hassensitivecontent())
- [SCSensitivityAnalysisPolicy](/documentation/sensitivecontentanalysis/scsensitivityanalysispolicy)

### Checking and intervention strategies

- [case disabled](/documentation/sensitivecontentanalysis/scsensitivityanalysispolicy/disabled)
- [case simpleInterventions](/documentation/sensitivecontentanalysis/scsensitivityanalysispolicy/simpleinterventions)
- [case descriptiveInterventions](/documentation/sensitivecontentanalysis/scsensitivityanalysispolicy/descriptiveinterventions)

### Creating an analysis policy value

- [init?(rawValue: Int)](/documentation/sensitivecontentanalysis/scsensitivityanalysispolicy/init(rawvalue:))

## Video stream analysis

- [SCVideoStreamAnalyzer](/documentation/sensitivecontentanalysis/scvideostreamanalyzer)

### Creating a video stream analyzer

- [init(participantUUID: String, streamDirection: SCVideoStreamAnalyzer.StreamDirection) throws](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/init(participantuuid:streamdirection:))
- [SCVideoStreamAnalyzer.StreamDirection](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/streamdirection)

#### Identifying a stream direction

- [case incoming](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/streamdirection/incoming)
- [case outgoing](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/streamdirection/outgoing)

#### Initializing a stream direction

- [init?(rawValue: Int)](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/streamdirection/init(rawvalue:))

### Analyzing a video stream

- [func analyze(CVPixelBuffer)](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/analyze(_:))
- [func beginAnalysis(of: AVCaptureDeviceInput) throws](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/beginanalysis(of:)-78qm)
- [func beginAnalysis(of: VTDecompressionSession) throws](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/beginanalysis(of:)-9ehkx)
- [var analysisChanges: some AsyncSequence<SCSensitivityAnalysis, any Error>](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/analysischanges)
- [func endAnalysis()](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/endanalysis())

### Responding to sensitive content

- [var analysis: SCSensitivityAnalysis?](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/analysis)
- [func continueStream()](/documentation/sensitivecontentanalysis/scvideostreamanalyzer/continuestream())

## Analysis results

- [SCSensitivityAnalysis](/documentation/sensitivecontentanalysis/scsensitivityanalysis)

### Confirming the presence of sensitive content

- [var isSensitive: Bool](/documentation/sensitivecontentanalysis/scsensitivityanalysis/issensitive)

### Receiving intervention guidance

- [var shouldIndicateSensitivity: Bool](/documentation/sensitivecontentanalysis/scsensitivityanalysis/shouldindicatesensitivity)
- [var shouldInterruptVideo: Bool](/documentation/sensitivecontentanalysis/scsensitivityanalysis/shouldinterruptvideo)
- [var shouldMuteAudio: Bool](/documentation/sensitivecontentanalysis/scsensitivityanalysis/shouldmuteaudio)

## Testing

- [Testing your app’s response to sensitive media](/documentation/sensitivecontentanalysis/testing-your-app-s-response-to-sensitive-media)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
