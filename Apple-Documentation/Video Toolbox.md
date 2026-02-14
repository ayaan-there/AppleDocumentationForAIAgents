# Video Toolbox Documentation

Source: https://sosumi.ai/documentation/videotoolbox

---
title: Video Toolbox
source: https://developer.apple.com/documentation/videotoolbox
timestamp: 2026-02-13T19:03:39.231Z
---

## Frame Processing

- [Frame processing](/documentation/videotoolbox/frame-processing)

### Frame processor

- [Enhancing your app with machine learning-based video effects](/documentation/videotoolbox/enhancing-your-app-with-machine-learning-based-video-effects)
- [VTFrameProcessor](/documentation/videotoolbox/vtframeprocessor)

#### Creating a frame processor

- [init()](/documentation/videotoolbox/vtframeprocessor/init())

#### Processing frames

- [func startSession(configuration: any VTFrameProcessorConfiguration) throws](/documentation/videotoolbox/vtframeprocessor/startsession(configuration:))
- [func process(parameters: any VTFrameProcessorParameters) -> some AsyncSequence<VTFrameProcessorFrame.ReadOnlyFrame, any Error>
](/documentation/videotoolbox/vtframeprocessor/process(parameters:))
- [func process(parameters: any VTFrameProcessorParameters, completionHandler: (any VTFrameProcessorParameters, (any Error)?) -> Void)](/documentation/videotoolbox/vtframeprocessor/process(parameters:completionhandler:))
- [func process(with: any MTLCommandBuffer, parameters: any VTFrameProcessorParameters)](/documentation/videotoolbox/vtframeprocessor/process(with:parameters:))
- [func endSession()](/documentation/videotoolbox/vtframeprocessor/endsession())
- [VTFrameProcessorConfiguration](/documentation/videotoolbox/vtframeprocessorconfiguration)

#### Determining processor availability

- [static var isSupported: Bool](/documentation/videotoolbox/vtframeprocessorconfiguration/issupported)

#### Inspecting dimension constraints

- [static var maximumDimensions: CMVideoDimensions?](/documentation/videotoolbox/vtframeprocessorconfiguration/maximumdimensions-4vmra)
- [static var minimumDimensions: CMVideoDimensions?](/documentation/videotoolbox/vtframeprocessorconfiguration/minimumdimensions-42b0h)

#### Inspecting pixel buffer attributes

- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtframeprocessorconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtframeprocessorconfiguration/destinationpixelbufferattributes)

#### Inspecting frame requirements

- [var nextFrameCount: Int?](/documentation/videotoolbox/vtframeprocessorconfiguration/nextframecount-18e47)
- [var previousFrameCount: Int?](/documentation/videotoolbox/vtframeprocessorconfiguration/previousframecount-1crhc)
- [VTFrameProcessorFrame](/documentation/videotoolbox/vtframeprocessorframe)

#### Creating a frame object

- [init?(buffer: CVPixelBuffer, presentationTimeStamp: CMTime)](/documentation/videotoolbox/vtframeprocessorframe/init(buffer:presentationtimestamp:))

#### Inspecting the frame

- [var buffer: CVPixelBuffer](/documentation/videotoolbox/vtframeprocessorframe/buffer)
- [var presentationTimeStamp: CMTime](/documentation/videotoolbox/vtframeprocessorframe/presentationtimestamp)

#### Structures

- [VTFrameProcessorFrame.ReadOnlyFrame](/documentation/videotoolbox/vtframeprocessorframe/readonlyframe)

##### Initializers

- [init(frame: CVReadOnlyPixelBuffer, timeStamp: CMTime)](/documentation/videotoolbox/vtframeprocessorframe/readonlyframe/init(frame:timestamp:))

##### Instance Properties

- [var frame: CVReadOnlyPixelBuffer](/documentation/videotoolbox/vtframeprocessorframe/readonlyframe/frame)
- [var timeStamp: CMTime](/documentation/videotoolbox/vtframeprocessorframe/readonlyframe/timestamp)
- [VTFrameProcessorParameters](/documentation/videotoolbox/vtframeprocessorparameters)

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtframeprocessorparameters/sourceframe)
- [var destinationFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtframeprocessorparameters/destinationframe-5suam)
- [var destinationFrames: [VTFrameProcessorFrame]?](/documentation/videotoolbox/vtframeprocessorparameters/destinationframes-46ken)

### Frame rate conversion

- [VTFrameRateConversionConfiguration](/documentation/videotoolbox/vtframerateconversionconfiguration)

#### Creating a frame rate conversion configuration

- [init?(frameWidth: Int, frameHeight: Int, usePrecomputedFlow: Bool, qualityPrioritization: VTFrameRateConversionConfiguration.QualityPrioritization, revision: VTFrameRateConversionConfiguration.Revision)](/documentation/videotoolbox/vtframerateconversionconfiguration/init(framewidth:frameheight:useprecomputedflow:qualityprioritization:revision:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtframerateconversionconfiguration/issupported)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtframerateconversionconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtframerateconversionconfiguration/frameheight)
- [var usePrecomputedFlow: Bool](/documentation/videotoolbox/vtframerateconversionconfiguration/useprecomputedflow)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtframerateconversionconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtframerateconversionconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtframerateconversionconfiguration/supportedpixelformats)
- [var qualityPrioritization: VTFrameRateConversionConfiguration.QualityPrioritization](/documentation/videotoolbox/vtframerateconversionconfiguration/qualityprioritization-swift.property)
- [VTFrameRateConversionConfiguration.QualityPrioritization](/documentation/videotoolbox/vtframerateconversionconfiguration/qualityprioritization-swift.enum)

##### Priorities

- [case normal](/documentation/videotoolbox/vtframerateconversionconfiguration/qualityprioritization-swift.enum/normal)
- [case quality](/documentation/videotoolbox/vtframerateconversionconfiguration/qualityprioritization-swift.enum/quality)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtframerateconversionconfiguration/qualityprioritization-swift.enum/init(rawvalue:))

#### Inspecting revision information

- [var revision: VTFrameRateConversionConfiguration.Revision](/documentation/videotoolbox/vtframerateconversionconfiguration/revision-swift.property)
- [class var defaultRevision: VTFrameRateConversionConfiguration.Revision](/documentation/videotoolbox/vtframerateconversionconfiguration/defaultrevision)
- [class var supportedRevisions: IndexSet](/documentation/videotoolbox/vtframerateconversionconfiguration/supportedrevisions)
- [VTFrameRateConversionConfiguration.Revision](/documentation/videotoolbox/vtframerateconversionconfiguration/revision-swift.enum)

##### Revisions

- [case revision1](/documentation/videotoolbox/vtframerateconversionconfiguration/revision-swift.enum/revision1)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtframerateconversionconfiguration/revision-swift.enum/init(rawvalue:))

#### Deprecated

- [class var processorSupported: Bool](/documentation/videotoolbox/vtframerateconversionconfiguration/processorsupported)
- [var frameSupportedPixelFormats: [NSNumber]](/documentation/videotoolbox/vtframerateconversionconfiguration/framesupportedpixelformats-54soi)
- [VTFrameRateConversionParameters](/documentation/videotoolbox/vtframerateconversionparameters)

#### Creating conversion parameters

- [convenience init?(sourceFrame: VTFrameProcessorFrame, nextFrame: VTFrameProcessorFrame, opticalFlow: VTFrameProcessorOpticalFlow?, interpolationPhase: [Float], submissionMode: VTFrameRateConversionParameters.SubmissionMode, destinationFrames: [VTFrameProcessorFrame])](/documentation/videotoolbox/vtframerateconversionparameters/init(sourceframe:nextframe:opticalflow:interpolationphase:submissionmode:destinationframes:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtframerateconversionparameters/sourceframe)
- [var nextFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtframerateconversionparameters/nextframe)
- [var opticalFlow: VTFrameProcessorOpticalFlow?](/documentation/videotoolbox/vtframerateconversionparameters/opticalflow)
- [var interpolationPhase: [Float]](/documentation/videotoolbox/vtframerateconversionparameters/interpolationphase-2jky5)
- [var submissionMode: VTFrameRateConversionParameters.SubmissionMode](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.property)
- [VTFrameRateConversionParameters.SubmissionMode](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.enum)

##### Submission modes

- [case random](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.enum/random)
- [case sequential](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.enum/sequential)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.enum/init(rawvalue:))

##### Enumeration Cases

- [case sequentialReferencesUnchanged](/documentation/videotoolbox/vtframerateconversionparameters/submissionmode-swift.enum/sequentialreferencesunchanged)

### Low-latency frame interpolation

- [VTLowLatencyFrameInterpolationConfiguration](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration)

#### Creating a frame interpolation configuration

- [init?(frameWidth: Int, frameHeight: Int, numberOfInterpolatedFrames: Int)](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/init(framewidth:frameheight:numberofinterpolatedframes:))
- [init?(frameWidth: Int, frameHeight: Int, spatialScaleFactor: Int)](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/init(framewidth:frameheight:spatialscalefactor:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/issupported)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/frameheight)
- [var numberOfInterpolatedFrames: Int](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/numberofinterpolatedframes)
- [var spatialScaleFactor: Int](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/spatialscalefactor)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtlowlatencyframeinterpolationconfiguration/supportedpixelformats)
- [VTLowLatencyFrameInterpolationParameters](/documentation/videotoolbox/vtlowlatencyframeinterpolationparameters)

#### Creating a parameters object

- [convenience init?(sourceFrame: VTFrameProcessorFrame, previousFrame: VTFrameProcessorFrame, interpolationPhase: [Float], destinationFrames: [VTFrameProcessorFrame])](/documentation/videotoolbox/vtlowlatencyframeinterpolationparameters/init(sourceframe:previousframe:interpolationphase:destinationframes:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtlowlatencyframeinterpolationparameters/sourceframe)
- [var previousFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtlowlatencyframeinterpolationparameters/previousframe)
- [var interpolationPhase: [Float]](/documentation/videotoolbox/vtlowlatencyframeinterpolationparameters/interpolationphase-886vi)

### Low-latency super resolution

- [VTLowLatencySuperResolutionScalerConfiguration](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration)

#### Creating a super resolution scaler configuration

- [init(frameWidth: Int, frameHeight: Int, scaleFactor: Float)](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/init(framewidth:frameheight:scalefactor:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/issupported)
- [class func supportedScaleFactors(frameWidth: Int, frameHeight: Int) -> [Float]](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/supportedscalefactors(framewidth:frameheight:))

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/frameheight)
- [var scaleFactor: Float](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/scalefactor)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerconfiguration/supportedpixelformats)
- [VTLowLatencySuperResolutionScalerParameters](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerparameters)

#### Creating a parameters object

- [init(sourceFrame: VTFrameProcessorFrame, destinationFrame: VTFrameProcessorFrame)](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerparameters/init(sourceframe:destinationframe:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtlowlatencysuperresolutionscalerparameters/sourceframe)

### Motion blur

- [VTMotionBlurConfiguration](/documentation/videotoolbox/vtmotionblurconfiguration)

#### Creating a motion blur configuration

- [init?(frameWidth: Int, frameHeight: Int, usePrecomputedFlow: Bool, qualityPrioritization: VTMotionBlurConfiguration.QualityPrioritization, revision: VTMotionBlurConfiguration.Revision)](/documentation/videotoolbox/vtmotionblurconfiguration/init(framewidth:frameheight:useprecomputedflow:qualityprioritization:revision:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtmotionblurconfiguration/issupported)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtmotionblurconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtmotionblurconfiguration/frameheight)
- [var usePrecomputedFlow: Bool](/documentation/videotoolbox/vtmotionblurconfiguration/useprecomputedflow)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtmotionblurconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtmotionblurconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtmotionblurconfiguration/supportedpixelformats)
- [var qualityPrioritization: VTMotionBlurConfiguration.QualityPrioritization](/documentation/videotoolbox/vtmotionblurconfiguration/qualityprioritization-swift.property)
- [VTMotionBlurConfiguration.QualityPrioritization](/documentation/videotoolbox/vtmotionblurconfiguration/qualityprioritization-swift.enum)

##### Priorities

- [case normal](/documentation/videotoolbox/vtmotionblurconfiguration/qualityprioritization-swift.enum/normal)
- [case quality](/documentation/videotoolbox/vtmotionblurconfiguration/qualityprioritization-swift.enum/quality)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtmotionblurconfiguration/qualityprioritization-swift.enum/init(rawvalue:))

#### Inspecting revision information

- [var revision: VTMotionBlurConfiguration.Revision](/documentation/videotoolbox/vtmotionblurconfiguration/revision-swift.property)
- [class var defaultRevision: VTMotionBlurConfiguration.Revision](/documentation/videotoolbox/vtmotionblurconfiguration/defaultrevision)
- [class var supportedRevisions: IndexSet](/documentation/videotoolbox/vtmotionblurconfiguration/supportedrevisions)
- [VTMotionBlurConfiguration.Revision](/documentation/videotoolbox/vtmotionblurconfiguration/revision-swift.enum)

##### Revisions

- [case revision1](/documentation/videotoolbox/vtmotionblurconfiguration/revision-swift.enum/revision1)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtmotionblurconfiguration/revision-swift.enum/init(rawvalue:))

#### Deprecated

- [class var processorSupported: Bool](/documentation/videotoolbox/vtmotionblurconfiguration/processorsupported)
- [var frameSupportedPixelFormats: [NSNumber]](/documentation/videotoolbox/vtmotionblurconfiguration/framesupportedpixelformats-1n4uq)
- [VTMotionBlurParameters](/documentation/videotoolbox/vtmotionblurparameters)

#### Creating a parameters object

- [init?(sourceFrame: VTFrameProcessorFrame, nextFrame: VTFrameProcessorFrame?, previousFrame: VTFrameProcessorFrame?, nextOpticalFlow: VTFrameProcessorOpticalFlow?, previousOpticalFlow: VTFrameProcessorOpticalFlow?, motionBlurStrength: Int, submissionMode: VTMotionBlurParameters.SubmissionMode, destinationFrame: VTFrameProcessorFrame)](/documentation/videotoolbox/vtmotionblurparameters/init(sourceframe:nextframe:previousframe:nextopticalflow:previousopticalflow:motionblurstrength:submissionmode:destinationframe:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtmotionblurparameters/sourceframe)
- [var nextFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtmotionblurparameters/nextframe)
- [var previousFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtmotionblurparameters/previousframe)
- [var motionBlurStrength: Int](/documentation/videotoolbox/vtmotionblurparameters/motionblurstrength)
- [var nextOpticalFlow: VTFrameProcessorOpticalFlow?](/documentation/videotoolbox/vtmotionblurparameters/nextopticalflow)
- [var previousOpticalFlow: VTFrameProcessorOpticalFlow?](/documentation/videotoolbox/vtmotionblurparameters/previousopticalflow)
- [var submissionMode: VTMotionBlurParameters.SubmissionMode](/documentation/videotoolbox/vtmotionblurparameters/submissionmode-swift.property)
- [VTMotionBlurParameters.SubmissionMode](/documentation/videotoolbox/vtmotionblurparameters/submissionmode-swift.enum)

##### Submission modes

- [case random](/documentation/videotoolbox/vtmotionblurparameters/submissionmode-swift.enum/random)
- [case sequential](/documentation/videotoolbox/vtmotionblurparameters/submissionmode-swift.enum/sequential)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtmotionblurparameters/submissionmode-swift.enum/init(rawvalue:))

### Optical flow

- [VTFrameProcessorOpticalFlow](/documentation/videotoolbox/vtframeprocessoropticalflow)

#### Creating an optical flow configuration

- [init?(forwardFlow: CVPixelBuffer, backwardFlow: CVPixelBuffer)](/documentation/videotoolbox/vtframeprocessoropticalflow/init(forwardflow:backwardflow:))

#### Inspecting the configuration

- [var backwardFlow: CVPixelBuffer](/documentation/videotoolbox/vtframeprocessoropticalflow/backwardflow)
- [var forwardFlow: CVPixelBuffer](/documentation/videotoolbox/vtframeprocessoropticalflow/forwardflow)
- [VTOpticalFlowConfiguration](/documentation/videotoolbox/vtopticalflowconfiguration)

#### Creating an optical flow configuration

- [init?(frameWidth: Int, frameHeight: Int, qualityPrioritization: VTOpticalFlowConfiguration.QualityPrioritization, revision: VTOpticalFlowConfiguration.Revision)](/documentation/videotoolbox/vtopticalflowconfiguration/init(framewidth:frameheight:qualityprioritization:revision:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtopticalflowconfiguration/issupported)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtopticalflowconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtopticalflowconfiguration/frameheight)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtopticalflowconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtopticalflowconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtopticalflowconfiguration/supportedpixelformats)
- [var qualityPrioritization: VTOpticalFlowConfiguration.QualityPrioritization](/documentation/videotoolbox/vtopticalflowconfiguration/qualityprioritization-swift.property)
- [VTOpticalFlowConfiguration.QualityPrioritization](/documentation/videotoolbox/vtopticalflowconfiguration/qualityprioritization-swift.enum)

##### Enumeration Cases

- [case normal](/documentation/videotoolbox/vtopticalflowconfiguration/qualityprioritization-swift.enum/normal)
- [case quality](/documentation/videotoolbox/vtopticalflowconfiguration/qualityprioritization-swift.enum/quality)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtopticalflowconfiguration/qualityprioritization-swift.enum/init(rawvalue:))

#### Inspecting revision information

- [var revision: VTOpticalFlowConfiguration.Revision](/documentation/videotoolbox/vtopticalflowconfiguration/revision-swift.property)
- [class var defaultRevision: VTOpticalFlowConfiguration.Revision](/documentation/videotoolbox/vtopticalflowconfiguration/defaultrevision)
- [class var supportedRevisions: IndexSet](/documentation/videotoolbox/vtopticalflowconfiguration/supportedrevisions)
- [VTOpticalFlowConfiguration.Revision](/documentation/videotoolbox/vtopticalflowconfiguration/revision-swift.enum)

##### Enumeration Cases

- [case revision1](/documentation/videotoolbox/vtopticalflowconfiguration/revision-swift.enum/revision1)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtopticalflowconfiguration/revision-swift.enum/init(rawvalue:))

#### Deprecated

- [class var processorSupported: Bool](/documentation/videotoolbox/vtopticalflowconfiguration/processorsupported)
- [var frameSupportedPixelFormats: [NSNumber]](/documentation/videotoolbox/vtopticalflowconfiguration/framesupportedpixelformats-gm6u)
- [VTOpticalFlowParameters](/documentation/videotoolbox/vtopticalflowparameters)

#### Creating a parameters object

- [init?(sourceFrame: VTFrameProcessorFrame, nextFrame: VTFrameProcessorFrame, submissionMode: VTOpticalFlowParameters.SubmissionMode, destinationOpticalFlow: VTFrameProcessorOpticalFlow)](/documentation/videotoolbox/vtopticalflowparameters/init(sourceframe:nextframe:submissionmode:destinationopticalflow:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtopticalflowparameters/sourceframe)
- [var nextFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtopticalflowparameters/nextframe)
- [var destinationOpticalFlow: VTFrameProcessorOpticalFlow](/documentation/videotoolbox/vtopticalflowparameters/destinationopticalflow)
- [var submissionMode: VTOpticalFlowParameters.SubmissionMode](/documentation/videotoolbox/vtopticalflowparameters/submissionmode-swift.property)
- [VTOpticalFlowParameters.SubmissionMode](/documentation/videotoolbox/vtopticalflowparameters/submissionmode-swift.enum)

##### Enumeration Cases

- [case random](/documentation/videotoolbox/vtopticalflowparameters/submissionmode-swift.enum/random)
- [case sequential](/documentation/videotoolbox/vtopticalflowparameters/submissionmode-swift.enum/sequential)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtopticalflowparameters/submissionmode-swift.enum/init(rawvalue:))

### Super resolution

- [VTSuperResolutionScalerConfiguration](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration)

#### Creating a super resolution scaler configuration

- [init?(frameWidth: Int, frameHeight: Int, scaleFactor: Int, inputType: VTSuperResolutionScalerConfiguration.InputType, usePrecomputedFlow: Bool, qualityPrioritization: VTSuperResolutionScalerConfiguration.QualityPrioritization, revision: VTSuperResolutionScalerConfiguration.Revision)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/init(framewidth:frameheight:scalefactor:inputtype:useprecomputedflow:qualityprioritization:revision:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/issupported)
- [class var supportedScaleFactors: [Int]](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/supportedscalefactors-7ucur)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/frameheight)
- [var scaleFactor: Int](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/scalefactor)
- [var inputType: VTSuperResolutionScalerConfiguration.InputType](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/inputtype-swift.property)
- [VTSuperResolutionScalerConfiguration.InputType](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/inputtype-swift.enum)

##### Enumeration Cases

- [case image](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/inputtype-swift.enum/image)
- [case video](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/inputtype-swift.enum/video)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/inputtype-swift.enum/init(rawvalue:))
- [var usesPrecomputedFlow: Bool](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/usesprecomputedflow)
- [var usesPrecomputedFlow: Bool](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/usesprecomputedflow)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/supportedpixelformats)
- [var qualityPrioritization: VTSuperResolutionScalerConfiguration.QualityPrioritization](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/qualityprioritization-swift.property)
- [VTSuperResolutionScalerConfiguration.QualityPrioritization](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/qualityprioritization-swift.enum)

##### Enumeration Cases

- [case normal](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/qualityprioritization-swift.enum/normal)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/qualityprioritization-swift.enum/init(rawvalue:))

#### Managing the configuration model

- [var configurationModelStatus: VTSuperResolutionScalerConfiguration.ModelStatus](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/configurationmodelstatus)
- [VTSuperResolutionScalerConfiguration.ModelStatus](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/modelstatus)

##### Enumeration Cases

- [case downloadRequired](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/modelstatus/downloadrequired)
- [case downloading](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/modelstatus/downloading)
- [case ready](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/modelstatus/ready)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/modelstatus/init(rawvalue:))
- [var configurationModelPercentageAvailable: Float](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/configurationmodelpercentageavailable)
- [func downloadConfigurationModel(completionHandler: ((any Error)?) -> Void)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/downloadconfigurationmodel(completionhandler:))

#### Inspecting revision information

- [var revision: VTSuperResolutionScalerConfiguration.Revision](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/revision-swift.property)
- [class var defaultRevision: VTSuperResolutionScalerConfiguration.Revision](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/defaultrevision)
- [class var supportedRevisions: IndexSet](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/supportedrevisions)
- [VTSuperResolutionScalerConfiguration.Revision](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/revision-swift.enum)

##### Enumeration Cases

- [case revision1](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/revision-swift.enum/revision1)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtsuperresolutionscalerconfiguration/revision-swift.enum/init(rawvalue:))
- [VTSuperResolutionScalerParameters](/documentation/videotoolbox/vtsuperresolutionscalerparameters)

#### Creating a parameters object

- [init?(sourceFrame: VTFrameProcessorFrame, previousFrame: VTFrameProcessorFrame?, previousOutputFrame: VTFrameProcessorFrame?, opticalFlow: VTFrameProcessorOpticalFlow?, submissionMode: VTSuperResolutionScalerParameters.SubmissionMode, destinationFrame: VTFrameProcessorFrame)](/documentation/videotoolbox/vtsuperresolutionscalerparameters/init(sourceframe:previousframe:previousoutputframe:opticalflow:submissionmode:destinationframe:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vtsuperresolutionscalerparameters/sourceframe)
- [var previousFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtsuperresolutionscalerparameters/previousframe)
- [var previousOutputFrame: VTFrameProcessorFrame?](/documentation/videotoolbox/vtsuperresolutionscalerparameters/previousoutputframe)
- [var opticalFlow: VTFrameProcessorOpticalFlow?](/documentation/videotoolbox/vtsuperresolutionscalerparameters/opticalflow)
- [var submissionMode: VTSuperResolutionScalerParameters.SubmissionMode](/documentation/videotoolbox/vtsuperresolutionscalerparameters/submissionmode-swift.property)
- [VTSuperResolutionScalerParameters.SubmissionMode](/documentation/videotoolbox/vtsuperresolutionscalerparameters/submissionmode-swift.enum)

##### Enumeration Cases

- [case random](/documentation/videotoolbox/vtsuperresolutionscalerparameters/submissionmode-swift.enum/random)
- [case sequential](/documentation/videotoolbox/vtsuperresolutionscalerparameters/submissionmode-swift.enum/sequential)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtsuperresolutionscalerparameters/submissionmode-swift.enum/init(rawvalue:))

### Temporal noise filter

- [VTTemporalNoiseFilterConfiguration](/documentation/videotoolbox/vttemporalnoisefilterconfiguration)

#### Creating a temporal noise filter configuration

- [init?(frameWidth: Int, frameHeight: Int, sourcePixelFormat: OSType)](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/init(framewidth:frameheight:sourcepixelformat:))

#### Determining processor availability

- [class var isSupported: Bool](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/issupported)

#### Inspecting the configuration

- [var frameWidth: Int](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/framewidth)
- [var frameHeight: Int](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/frameheight)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/sourcepixelbufferattributes)
- [var destinationPixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/destinationpixelbufferattributes)
- [var supportedPixelFormats: [OSType]](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/supportedpixelformats)
- [class var supportedSourcePixelFormats: [OSType]](/documentation/videotoolbox/vttemporalnoisefilterconfiguration/supportedsourcepixelformats-4ipcg)
- [VTTemporalNoiseFilterParameters](/documentation/videotoolbox/vttemporalnoisefilterparameters)

#### Creating a parameters object

- [init?(sourceFrame: VTFrameProcessorFrame, nextFrames: [VTFrameProcessorFrame], previousFrames: [VTFrameProcessorFrame], destinationFrame: VTFrameProcessorFrame, filterStrength: Float, hasDiscontinuity: Bool)](/documentation/videotoolbox/vttemporalnoisefilterparameters/init(sourceframe:nextframes:previousframes:destinationframe:filterstrength:hasdiscontinuity:))

#### Inspecting the parameters

- [var sourceFrame: VTFrameProcessorFrame](/documentation/videotoolbox/vttemporalnoisefilterparameters/sourceframe)
- [var nextFrames: [VTFrameProcessorFrame]](/documentation/videotoolbox/vttemporalnoisefilterparameters/nextframes)
- [var previousFrames: [VTFrameProcessorFrame]](/documentation/videotoolbox/vttemporalnoisefilterparameters/previousframes)
- [var filterStrength: Float](/documentation/videotoolbox/vttemporalnoisefilterparameters/filterstrength)
- [var hasDiscontinuity: Bool](/documentation/videotoolbox/vttemporalnoisefilterparameters/hasdiscontinuity)

### Errors

- [VTFrameProcessorError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct)

#### Error domain

- [static var errorDomain: String](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/errordomain)
- [let VTFrameProcessorErrorDomain: String](/documentation/videotoolbox/vtframeprocessorerrordomain)

#### Error information

- [var code: Self.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code-swift.property)
- [var errorCode: Int](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/errorcode)
- [var errorUserInfo: [String : Any]](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/erroruserinfo)
- [var userInfo: [String : Any]](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/userinfo)

#### Errors

- [static var assetDownloadFailed: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/assetdownloadfailed)
- [static var fatalError: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/fatalerror)
- [static var initializationFailed: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/initializationfailed)
- [static var invalidFrameTiming: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/invalidframetiming)
- [static var invalidParameterError: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/invalidparametererror)
- [static var memoryAllocationFailure: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/memoryallocationfailure)
- [static var processingError: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/processingerror)
- [static var revisionNotSupported: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/revisionnotsupported)
- [static var sessionAlreadyActive: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/sessionalreadyactive)
- [static var sessionLevelError: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/sessionlevelerror)
- [static var sessionNotStarted: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/sessionnotstarted)
- [static var unknownError: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/unknownerror)
- [static var unsupportedInput: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/unsupportedinput)
- [static var unsupportedResolution: VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/unsupportedresolution)

#### Enumerations

- [VTFrameProcessorError.Code](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code)

##### Enumeration Cases

- [case fatalError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/fatalerror)
- [case initializationFailed](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/initializationfailed)
- [case invalidFrameTiming](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/invalidframetiming)
- [case invalidParameterError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/invalidparametererror)
- [case memoryAllocationFailure](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/memoryallocationfailure)
- [case processingError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/processingerror)
- [case revisionNotSupported](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/revisionnotsupported)
- [case sessionAlreadyActive](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/sessionalreadyactive)
- [case sessionLevelError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/sessionlevelerror)
- [case sessionNotStarted](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/sessionnotstarted)
- [case unknownError](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/unknownerror)
- [case unsupportedInput](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/unsupportedinput)
- [case unsupportedResolution](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/unsupportedresolution)
- [case assetDownloadFailed](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/assetdownloadfailed)

##### Initializers

- [init?(rawValue: Int)](/documentation/videotoolbox/vtframeprocessorerror-swift.struct/code/init(rawvalue:))
- [let VTFrameProcessorErrorDomain: String](/documentation/videotoolbox/vtframeprocessorerrordomain)

## Motion Estimation

- [VTMotionEstimationSession](/documentation/videotoolbox/vtmotionestimationsession)

### Creating a motion estimation session

- [init(width: UInt32, height: UInt32, motionVectorSize: VTMotionEstimationSession.BlockSize, useMultiPassSearch: Bool, label: String?) throws](/documentation/videotoolbox/vtmotionestimationsession/init(width:height:motionvectorsize:usemultipasssearch:label:))

### Estimating motion

- [func motion(of: CVReadOnlyPixelBuffer, comparedTo: CVReadOnlyPixelBuffer, flags: VTMotionEstimationSession.FrameFlags) async throws -> VTMotionEstimationSession.Motion](/documentation/videotoolbox/vtmotionestimationsession/motion(of:comparedto:flags:))
- [VTMotionEstimationSession.FrameFlags](/documentation/videotoolbox/vtmotionestimationsession/frameflags)

#### Type Properties

- [static let currentBufferWillBeNextReferenceBuffer: VTMotionEstimationSession.FrameFlags](/documentation/videotoolbox/vtmotionestimationsession/frameflags/currentbufferwillbenextreferencebuffer)

### Inspecting the session

- [var label: String?](/documentation/videotoolbox/vtmotionestimationsession/label)
- [var motionVectorSize: VTMotionEstimationSession.BlockSize](/documentation/videotoolbox/vtmotionestimationsession/motionvectorsize)
- [var sourcePixelBufferAttributes: [String : any Sendable]](/documentation/videotoolbox/vtmotionestimationsession/sourcepixelbufferattributes)
- [var useMultiPassSearch: Bool](/documentation/videotoolbox/vtmotionestimationsession/usemultipasssearch)

### Inspecting the motion result

- [VTMotionEstimationSession.Motion](/documentation/videotoolbox/vtmotionestimationsession/motion)

#### Instance Properties

- [var motionVector: CVReadOnlyPixelBuffer](/documentation/videotoolbox/vtmotionestimationsession/motion/motionvector)
- [VTMotionEstimationSession.BlockSize](/documentation/videotoolbox/vtmotionestimationsession/blocksize)

#### Enumeration Cases

- [case blockSize16x16](/documentation/videotoolbox/vtmotionestimationsession/blocksize/blocksize16x16)
- [case blockSize4x4](/documentation/videotoolbox/vtmotionestimationsession/blocksize/blocksize4x4)

## Compression

- [Encoding video for low-latency conferencing](/documentation/videotoolbox/encoding-video-for-low-latency-conferencing)
- [Encoding video for live streaming](/documentation/videotoolbox/encoding-video-for-live-streaming)
- [Encoding video for offline transcoding](/documentation/videotoolbox/encoding-video-for-offline-transcoding)
- [VTCompressionSession](/documentation/videotoolbox/vtcompressionsession-api-collection)

### Creating a Session

- [func VTCompressionSessionCreate(allocator: CFAllocator?, width: Int32, height: Int32, codecType: CMVideoCodecType, encoderSpecification: CFDictionary?, imageBufferAttributes: CFDictionary?, compressedDataAllocator: CFAllocator?, outputCallback: VTCompressionOutputCallback?, refcon: UnsafeMutableRawPointer?, compressionSessionOut: UnsafeMutablePointer<VTCompressionSession?>) -> OSStatus](/documentation/videotoolbox/vtcompressionsessioncreate(allocator:width:height:codectype:encoderspecification:imagebufferattributes:compresseddataallocator:outputcallback:refcon:compressionsessionout:))

#### Callbacks

- [VTCompressionOutputCallback](/documentation/videotoolbox/vtcompressionoutputcallback)
- [VTCompressionOutputHandler](/documentation/videotoolbox/vtcompressionoutputhandler)

### Configuring a Session

- [Compression Properties](/documentation/videotoolbox/compression-properties)

#### Bitstream Configuration

- [let kVTCompressionPropertyKey_Depth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_depth)
- [let kVTCompressionPropertyKey_H264EntropyMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_h264entropymode)

##### Entropy Modes

- [let kVTH264EntropyMode_CAVLC: CFString](/documentation/videotoolbox/kvth264entropymode_cavlc)
- [let kVTH264EntropyMode_CABAC: CFString](/documentation/videotoolbox/kvth264entropymode_cabac)
- [let kVTCompressionPropertyKey_HDRMetadataInsertionMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hdrmetadatainsertionmode)

##### Insertion Modes

- [let kVTHDRMetadataInsertionMode_Auto: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_auto)
- [let kVTHDRMetadataInsertionMode_None: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_none)
- [let kVTHDRMetadataInsertionMode_RequestSDRRangePreservation: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_requestsdrrangepreservation)
- [let kVTCompressionPropertyKey_OutputBitDepth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_outputbitdepth)
- [let kVTCompressionPropertyKey_PreserveAlphaChannel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservealphachannel)
- [let kVTCompressionPropertyKey_PreserveDynamicHDRMetadata: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservedynamichdrmetadata)
- [let kVTCompressionPropertyKey_ProfileLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_profilelevel)

##### HEVC

- [let kVTProfileLevel_HEVC_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main_autolevel)
- [let kVTProfileLevel_HEVC_Main10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main10_autolevel)
- [let kVTProfileLevel_HEVC_Main42210_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main42210_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome10_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome_autolevel)

##### H.264

- [let kVTProfileLevel_H264_Baseline_1_3: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_1_3)
- [let kVTProfileLevel_H264_Baseline_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_0)
- [let kVTProfileLevel_H264_Baseline_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_1)
- [let kVTProfileLevel_H264_Baseline_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_2)
- [let kVTProfileLevel_H264_Baseline_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_0)
- [let kVTProfileLevel_H264_Baseline_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_1)
- [let kVTProfileLevel_H264_Baseline_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_2)
- [let kVTProfileLevel_H264_Baseline_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_0)
- [let kVTProfileLevel_H264_Baseline_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_1)
- [let kVTProfileLevel_H264_Baseline_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_2)
- [let kVTProfileLevel_H264_Baseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedBaseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedbaseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedHigh_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedhigh_autolevel)
- [let kVTProfileLevel_H264_Extended_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_5_0)
- [let kVTProfileLevel_H264_Extended_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_autolevel)
- [let kVTProfileLevel_H264_High_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_0)
- [let kVTProfileLevel_H264_High_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_1)
- [let kVTProfileLevel_H264_High_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_2)
- [let kVTProfileLevel_H264_High_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_0)
- [let kVTProfileLevel_H264_High_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_1)
- [let kVTProfileLevel_H264_High_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_2)
- [let kVTProfileLevel_H264_High_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_0)
- [let kVTProfileLevel_H264_High_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_1)
- [let kVTProfileLevel_H264_High_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_2)
- [let kVTProfileLevel_H264_High_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_autolevel)
- [let kVTProfileLevel_H264_Main_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_0)
- [let kVTProfileLevel_H264_Main_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_1)
- [let kVTProfileLevel_H264_Main_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_2)
- [let kVTProfileLevel_H264_Main_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_0)
- [let kVTProfileLevel_H264_Main_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_1)
- [let kVTProfileLevel_H264_Main_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_2)
- [let kVTProfileLevel_H264_Main_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_0)
- [let kVTProfileLevel_H264_Main_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_1)
- [let kVTProfileLevel_H264_Main_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_2)
- [let kVTProfileLevel_H264_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_autolevel)

##### MP4V

- [let kVTProfileLevel_MP4V_Simple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l0)
- [let kVTProfileLevel_MP4V_Simple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l1)
- [let kVTProfileLevel_MP4V_Simple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l2)
- [let kVTProfileLevel_MP4V_Simple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l0)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l1)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l2)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l4)
- [let kVTProfileLevel_MP4V_Main_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l2)
- [let kVTProfileLevel_MP4V_Main_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l3)
- [let kVTProfileLevel_MP4V_Main_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l4)

##### H.263

- [let kVTProfileLevel_H263_Profile0_Level10: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level10)
- [let kVTProfileLevel_H263_Profile0_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level45)
- [let kVTProfileLevel_H263_Profile3_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile3_level45)

#### Buffers

- [let kVTCompressionPropertyKey_NumberOfPendingFrames: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_numberofpendingframes)
- [let kVTCompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelbufferpoolisshared)
- [let kVTCompressionPropertyKey_VideoEncoderPixelBufferAttributes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_videoencoderpixelbufferattributes)

#### Camera Calibration

- [let kVTCompressionPropertyKey_CameraCalibrationDataLensCollection: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cameracalibrationdatalenscollection)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOrientationQuaternion: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicorientationquaternion)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOriginSource: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicoriginsource)

##### Origin Source Values

- [let kVTCameraCalibrationExtrinsicOriginSource_StereoCameraSystemBaseline: CFString](/documentation/videotoolbox/kvtcameracalibrationextrinsicoriginsource_stereocamerasystembaseline)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrix)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixProjectionOffset: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixprojectionoffset)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixReferenceDimensions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixreferencedimensions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensAlgorithmKind: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensalgorithmkind)

##### Algorithm Kinds

- [let kVTCameraCalibrationLensAlgorithmKind_ParametricLens: CFString](/documentation/videotoolbox/kvtcameracalibrationlensalgorithmkind_parametriclens)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDistortions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdistortions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDomain: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdomain)

##### Lens Domains

- [let kVTCameraCalibrationLensDomain_Color: CFString](/documentation/videotoolbox/kvtcameracalibrationlensdomain_color)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialX: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialx)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialY: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialy)
- [let kVTCompressionPropertyCameraCalibrationKey_LensIdentifier: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensidentifier)
- [let kVTCompressionPropertyCameraCalibrationKey_LensRole: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensrole)

##### Lens Roles

- [let kVTCameraCalibrationLensRole_Left: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_left)
- [let kVTCameraCalibrationLensRole_Mono: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_mono)
- [let kVTCameraCalibrationLensRole_Right: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_right)
- [let kVTCompressionPropertyCameraCalibrationKey_RadialAngleLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_radialanglelimit)

#### Clean Aperture and Pixel Aspect Ratio

- [let kVTCompressionPropertyKey_AspectRatio16x9: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_aspectratio16x9)
- [let kVTCompressionPropertyKey_CleanAperture: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cleanaperture)
- [let kVTCompressionPropertyKey_FieldCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fieldcount)
- [let kVTCompressionPropertyKey_FieldDetail: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fielddetail)
- [let kVTCompressionPropertyKey_PixelAspectRatio: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelaspectratio)
- [let kVTCompressionPropertyKey_ProgressiveScan: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_progressivescan)

#### Color

- [let kVTCompressionPropertyKey_AlphaChannelMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_alphachannelmode)

##### Modes

- [let kVTAlphaChannelMode_StraightAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_straightalpha)
- [let kVTAlphaChannelMode_PremultipliedAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_premultipliedalpha)
- [let kVTCompressionPropertyKey_ColorPrimaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_colorprimaries)
- [let kVTCompressionPropertyKey_ContentLightLevelInfo: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_contentlightlevelinfo)
- [let kVTCompressionPropertyKey_GammaLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_gammalevel)
- [let kVTCompressionPropertyKey_ICCProfile: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_iccprofile)
- [let kVTCompressionPropertyKey_MasteringDisplayColorVolume: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_masteringdisplaycolorvolume)
- [let kVTCompressionPropertyKey_TransferFunction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_transferfunction)
- [let kVTCompressionPropertyKey_YCbCrMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_ycbcrmatrix)

#### Compression Presets

- [let kVTCompressionPreset_Balanced: CFString](/documentation/videotoolbox/kvtcompressionpreset_balanced)
- [let kVTCompressionPreset_HighQuality: CFString](/documentation/videotoolbox/kvtcompressionpreset_highquality)
- [let kVTCompressionPreset_HighSpeed: CFString](/documentation/videotoolbox/kvtcompressionpreset_highspeed)
- [let kVTCompressionPreset_VideoConferencing: CFString](/documentation/videotoolbox/kvtcompressionpreset_videoconferencing)
- [let kVTCompressionPropertyKey_SupportedPresetDictionaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportedpresetdictionaries)

#### Encoder Selection

- [let kVTCompressionPropertyKey_EncoderID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_encoderid)
- [let kVTVideoEncoderSpecification_EnableHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablehardwareacceleratedvideoencoder)
- [let kVTVideoEncoderSpecification_EnableLowLatencyRateControl: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablelowlatencyratecontrol)
- [let kVTVideoEncoderSpecification_EncoderID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_encoderid)
- [let kVTVideoEncoderSpecification_PreferredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_preferredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequiredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requiredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequireHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requirehardwareacceleratedvideoencoder)

#### Encoding Hints

- [let kVTCompressionPropertyKey_ExpectedDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedduration)
- [let kVTCompressionPropertyKey_ExpectedFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedframerate)
- [let kVTCompressionPropertyKey_MaximumRealTimeFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximumrealtimeframerate)
- [let kVTCompressionPropertyKey_PrioritizeEncodingSpeedOverQuality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_prioritizeencodingspeedoverquality)
- [let kVTCompressionPropertyKey_ReferenceBufferCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_referencebuffercount)
- [let kVTCompressionPropertyKey_SourceFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_sourceframecount)
- [let kVTCompressionPropertyKey_SuggestedLookAheadFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_suggestedlookaheadframecount)

#### Frame Dependency

- [let kVTCompressionPropertyKey_AllowFrameReordering: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowframereordering)
- [let kVTCompressionPropertyKey_AllowOpenGOP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowopengop)
- [let kVTCompressionPropertyKey_AllowTemporalCompression: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowtemporalcompression)
- [let kVTCompressionPropertyKey_MaxKeyFrameInterval: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeinterval)
- [let kVTCompressionPropertyKey_MaxKeyFrameIntervalDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeintervalduration)

#### Hardware Acceleration

- [let kVTCompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinggpuregistryid)
- [let kVTCompressionPropertyKey_UsingHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinghardwareacceleratedvideoencoder)

#### Long-Term Reference

- [let kVTCompressionPropertyKey_EnableLTR: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_enableltr)
- [let kVTEncodeFrameOptionKey_AcknowledgedLTRTokens: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_acknowledgedltrtokens)
- [let kVTEncodeFrameOptionKey_ForceLTRRefresh: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forceltrrefresh)
- [let kVTSampleAttachmentKey_RequireLTRAcknowledgementToken: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_requireltracknowledgementtoken)

#### Multipass Storage

- [let kVTCompressionPropertyKey_MultiPassStorage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_multipassstorage)

#### Multiview Compression

- [let kVTCompressionPropertyKey_MVHEVCLeftAndRightViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcleftandrightviewids)
- [let kVTCompressionPropertyKey_MVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcvideolayerids)
- [let kVTCompressionPropertyKey_MVHEVCViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcviewids)

#### Parallelization

- [let kVTCompressionPropertyKey_RecommendedParallelizationLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizationlimit)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumduration)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumframecount)

#### Per-Frame Configuration

- [let kVTEncodeFrameOptionKey_BaseFrameQP: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_baseframeqp)
- [let kVTEncodeFrameOptionKey_ForceKeyFrame: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forcekeyframe)

#### Precompression Processing

- [let kVTCompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixeltransferproperties)

#### Quality Metrics

- [let kVTCompressionPropertyKey_CalculateMeanSquaredError: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_calculatemeansquarederror)
- [let kVTSampleAttachmentKey_QualityMetrics: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_qualitymetrics)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaBlueMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromabluemeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaRedMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromaredmeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_LumaMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_lumameansquarederror)

#### Quantization

- [let kVTCompressionPropertyKey_MaxAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxallowedframeqp)
- [let kVTCompressionPropertyKey_MinAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_minallowedframeqp)
- [let kVTCompressionPropertyKey_SpatialAdaptiveQPLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_spatialadaptiveqplevel)

##### Levels

- [var kVTQPModulationLevel_Default: Int](/documentation/videotoolbox/kvtqpmodulationlevel_default)
- [var kVTQPModulationLevel_Disable: Int](/documentation/videotoolbox/kvtqpmodulationlevel_disable)
- [let kVTCompressionPropertyKey_SupportsBaseFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportsbaseframeqp)

#### Rate Control

- [let kVTCompressionPropertyKey_AverageBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_averagebitrate)
- [let kVTCompressionPropertyKey_ConstantBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_constantbitrate)
- [let kVTCompressionPropertyKey_DataRateLimits: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_dataratelimits)
- [let kVTCompressionPropertyKey_EstimatedAverageBytesPerFrame: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_estimatedaveragebytesperframe)
- [let kVTCompressionPropertyKey_MoreFramesAfterEnd: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesafterend)
- [let kVTCompressionPropertyKey_MoreFramesBeforeStart: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesbeforestart)
- [let kVTCompressionPropertyKey_Quality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_quality)
- [let kVTCompressionPropertyKey_TargetQualityForAlpha: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_targetqualityforalpha)
- [let kVTCompressionPropertyKey_VariableBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_variablebitrate)
- [let kVTCompressionPropertyKey_VBVBufferDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvbufferduration)
- [let kVTCompressionPropertyKey_VBVInitialDelayPercentage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvinitialdelaypercentage)
- [let kVTCompressionPropertyKey_VBVMaxBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvmaxbitrate)

#### Runtime Restrictions

- [let kVTCompressionPropertyKey_MaxFrameDelayCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxframedelaycount)

##### Delay Counts

- [var kVTUnlimitedFrameDelayCount: Int](/documentation/videotoolbox/kvtunlimitedframedelaycount)
- [let kVTCompressionPropertyKey_MaxH264SliceBytes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxh264slicebytes)
- [let kVTCompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximizepowerefficiency)
- [let kVTCompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_realtime)

#### Temporal Scalability

- [let kVTCompressionPropertyKey_BaseLayerBitRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerbitratefraction)
- [let kVTCompressionPropertyKey_BaseLayerFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframerate)
- [let kVTCompressionPropertyKey_BaseLayerFrameRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframeratefraction)

#### Video Extended Usage (VEXU) Signaling

- [let kVTCompressionPropertyKey_HasLeftStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasleftstereoeyeview)
- [let kVTCompressionPropertyKey_HasRightStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasrightstereoeyeview)
- [let kVTCompressionPropertyKey_HeroEye: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_heroeye)

##### Hero Eye Values

- [let kVTHeroEye_Left: CFString](/documentation/videotoolbox/kvtheroeye_left)
- [let kVTHeroEye_Right: CFString](/documentation/videotoolbox/kvtheroeye_right)
- [let kVTCompressionPropertyKey_HorizontalDisparityAdjustment: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontaldisparityadjustment)
- [let kVTCompressionPropertyKey_HorizontalFieldOfView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontalfieldofview)
- [let kVTCompressionPropertyKey_ProjectionKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_projectionkind)

##### Projection Kinds

- [let kVTProjectionKind_Rectilinear: CFString](/documentation/videotoolbox/kvtprojectionkind_rectilinear)
- [let kVTProjectionKind_Equirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_equirectangular)
- [let kVTProjectionKind_HalfEquirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_halfequirectangular)
- [let kVTProjectionKind_ParametricImmersive: CFString](/documentation/videotoolbox/kvtprojectionkind_parametricimmersive)
- [let kVTCompressionPropertyKey_StereoCameraBaseline: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_stereocamerabaseline)
- [let kVTCompressionPropertyKey_ViewPackingKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_viewpackingkind)

##### View Packing Kinds

- [let kVTViewPackingKind_SideBySide: CFString](/documentation/videotoolbox/kvtviewpackingkind_sidebyside)
- [let kVTViewPackingKind_OverUnder: CFString](/documentation/videotoolbox/kvtviewpackingkind_overunder)

### Encoding Frames

- [func VTCompressionSessionGetPixelBufferPool(VTCompressionSession) -> CVPixelBufferPool?](/documentation/videotoolbox/vtcompressionsessiongetpixelbufferpool(_:))
- [func VTCompressionSessionPrepareToEncodeFrames(VTCompressionSession) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionpreparetoencodeframes(_:))
- [func VTCompressionSessionEncodeFrame(VTCompressionSession, imageBuffer: CVImageBuffer, presentationTimeStamp: CMTime, duration: CMTime, frameProperties: CFDictionary?, sourceFrameRefcon: UnsafeMutableRawPointer?, infoFlagsOut: UnsafeMutablePointer<VTEncodeInfoFlags>?) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionencodeframe(_:imagebuffer:presentationtimestamp:duration:frameproperties:sourceframerefcon:infoflagsout:))
- [func VTCompressionSessionEncodeFrame(VTCompressionSession, imageBuffer: CVImageBuffer, presentationTimeStamp: CMTime, duration: CMTime, frameProperties: CFDictionary?, infoFlagsOut: UnsafeMutablePointer<VTEncodeInfoFlags>?, outputHandler: VTCompressionOutputHandler) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionencodeframe(_:imagebuffer:presentationtimestamp:duration:frameproperties:infoflagsout:outputhandler:))
- [func VTCompressionSessionCompleteFrames(VTCompressionSession, untilPresentationTimeStamp: CMTime) -> OSStatus](/documentation/videotoolbox/vtcompressionsessioncompleteframes(_:untilpresentationtimestamp:))

### Encoding Multi-Image Frames

- [func VTIsStereoMVHEVCEncodeSupported() -> Bool](/documentation/videotoolbox/vtisstereomvhevcencodesupported())
- [func VTCompressionSessionEncodeMultiImageFrame(VTCompressionSession, taggedBuffers: [CMTaggedBuffer], presentationTimeStamp: CMTime, duration: CMTime, frameProperties: CFDictionary?, infoFlagsOut: UnsafeMutablePointer<VTEncodeInfoFlags>?, outputHandler: VTCompressionOutputHandler) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionencodemultiimageframe(_:taggedbuffers:presentationtimestamp:duration:frameproperties:infoflagsout:outputhandler:))

### Performing Multiple Passes

- [func VTCompressionSessionBeginPass(VTCompressionSession, flags: VTCompressionSessionOptionFlags, UnsafeMutablePointer<UInt32>?) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionbeginpass(_:flags:_:))

#### Option Flags

- [VTCompressionSessionOptionFlags](/documentation/videotoolbox/vtcompressionsessionoptionflags)

##### Option Flags

- [static var beginFinalPass: VTCompressionSessionOptionFlags](/documentation/videotoolbox/vtcompressionsessionoptionflags/beginfinalpass)

##### Initializers

- [init(rawValue: UInt32)](/documentation/videotoolbox/vtcompressionsessionoptionflags/init(rawvalue:))
- [func VTCompressionSessionEndPass(VTCompressionSession, furtherPassesRequestedOut: UnsafeMutablePointer<DarwinBoolean>?, UnsafeMutablePointer<UInt32>?) -> OSStatus](/documentation/videotoolbox/vtcompressionsessionendpass(_:furtherpassesrequestedout:_:))
- [func VTCompressionSessionGetTimeRangesForNextPass(VTCompressionSession, timeRangeCountOut: UnsafeMutablePointer<CMItemCount>, timeRangeArrayOut: UnsafeMutablePointer<UnsafePointer<CMTimeRange>?>) -> OSStatus](/documentation/videotoolbox/vtcompressionsessiongettimerangesfornextpass(_:timerangecountout:timerangearrayout:))

### Invalidating a Session

- [func VTCompressionSessionInvalidate(VTCompressionSession)](/documentation/videotoolbox/vtcompressionsessioninvalidate(_:))

### Accessing the Type Identifier

- [func VTCompressionSessionGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtcompressionsessiongettypeid())

### Data Types

- [VTCompressionSession](/documentation/videotoolbox/vtcompressionsession)
- [VTEncodeInfoFlags](/documentation/videotoolbox/vtencodeinfoflags)

#### Info Flags

- [static var asynchronous: VTEncodeInfoFlags](/documentation/videotoolbox/vtencodeinfoflags/asynchronous)
- [static var frameDropped: VTEncodeInfoFlags](/documentation/videotoolbox/vtencodeinfoflags/framedropped)

#### Initializers

- [init(rawValue: UInt32)](/documentation/videotoolbox/vtencodeinfoflags/init(rawvalue:))
- [VTDecompressionSession](/documentation/videotoolbox/vtdecompressionsession-api-collection)

### Creating a Session

- [func VTDecompressionSessionCreate(allocator: CFAllocator?, formatDescription: CMVideoFormatDescription, decoderSpecification: CFDictionary?, imageBufferAttributes: CFDictionary?, decompressionSessionOut: UnsafeMutablePointer<VTDecompressionSession?>) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessioncreate(allocator:formatdescription:decoderspecification:imagebufferattributes:decompressionsessionout:))
- [func VTDecompressionSessionCreate(allocator: CFAllocator?, formatDescription: CMVideoFormatDescription, decoderSpecification: CFDictionary?, imageBufferAttributes: CFDictionary?, outputCallback: UnsafePointer<VTDecompressionOutputCallbackRecord>?, decompressionSessionOut: UnsafeMutablePointer<VTDecompressionSession?>) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessioncreate(allocator:formatdescription:decoderspecification:imagebufferattributes:outputcallback:decompressionsessionout:))

### Configuring a Session

- [Decompression Properties](/documentation/videotoolbox/decompression-properties)

#### Asynchronous State

- [let kVTDecompressionPropertyKey_MaxOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maxoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_MinOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_minoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_NumberOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_numberofframesbeingdecoded)

#### Content

- [let kVTDecompressionPropertyKey_ContentHasInterframeDependencies: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_contenthasinterframedependencies)

#### Decoder Behavior

- [let kVTDecompressionProperty_TemporalLevelLimit: CFString](/documentation/videotoolbox/kvtdecompressionproperty_temporallevellimit)
- [let kVTDecompressionPropertyKey_AllowBitstreamToChangeFrameDimensions: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_allowbitstreamtochangeframedimensions)
- [let kVTDecompressionPropertyKey_DeinterlaceMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_deinterlacemode)

##### Deinterlace Modes

- [let kVTDecompressionProperty_DeinterlaceMode_VerticalFilter: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_verticalfilter)
- [let kVTDecompressionProperty_DeinterlaceMode_Temporal: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_temporal)
- [let kVTDecompressionPropertyKey_FieldMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_fieldmode)

##### Field Modes

- [let kVTDecompressionProperty_FieldMode_BothFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bothfields)
- [let kVTDecompressionProperty_FieldMode_BottomFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bottomfieldonly)
- [let kVTDecompressionProperty_FieldMode_DeinterlaceFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_deinterlacefields)
- [let kVTDecompressionProperty_FieldMode_SingleField: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_singlefield)
- [let kVTDecompressionProperty_FieldMode_TopFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_topfieldonly)
- [let kVTDecompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maximizepowerefficiency)
- [let kVTDecompressionPropertyKey_OnlyTheseFrames: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_onlytheseframes)

##### Frame Constants

- [let kVTDecompressionProperty_OnlyTheseFrames_AllFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_allframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_IFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_iframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_KeyFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_keyframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_NonDroppableFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_nondroppableframes)
- [let kVTDecompressionPropertyKey_PixelFormatsWithReducedResolutionSupport: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelformatswithreducedresolutionsupport)
- [let kVTDecompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_realtime)
- [let kVTDecompressionPropertyKey_ReducedCoefficientDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedcoefficientdecode)
- [let kVTDecompressionPropertyKey_ReducedFrameDelivery: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedframedelivery)
- [let kVTDecompressionPropertyKey_ReducedResolutionDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedresolutiondecode)

##### Resolutions

- [let kVTDecompressionResolutionKey_Width: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_width)
- [let kVTDecompressionResolutionKey_Height: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_height)
- [let kVTDecompressionPropertyKey_SuggestedQualityOfServiceTiers: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_suggestedqualityofservicetiers)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByPerformance: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyperformance)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByQuality: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyquality)
- [let kVTDecompressionPropertyKey_ThreadCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_threadcount)

#### Hardware Acceleration

- [let kVTDecompressionPropertyKey_UsingHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinghardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_EnableHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_enablehardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_RequireHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requirehardwareacceleratedvideodecoder)

#### Multi-Image Decompression

- [let kVTDecompressionPropertyKey_RequestedMVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestedmvhevcvideolayerids)

#### Per-Frame Decoder Options

- [let kVTDecodeFrameOptionKey_ContentAnalyzerCropRectangle: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzercroprectangle)
- [let kVTDecodeFrameOptionKey_ContentAnalyzerRotation: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzerrotation)

#### Pixel Buffer Pools

- [let kVTDecompressionPropertyKey_OutputPoolRequestedMinimumBufferCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_outputpoolrequestedminimumbuffercount)
- [let kVTDecompressionPropertyKey_PixelBufferPool: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpool)
- [let kVTDecompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpoolisshared)

#### Post-Decompression Processing

- [let kVTDecompressionPropertyKey_DecoderProducesRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_decoderproducesrawoutput)
- [let kVTDecompressionPropertyKey_GeneratePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_generateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixeltransferproperties)
- [let kVTDecompressionPropertyKey_PropagatePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_propagateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_RequestRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestrawoutput)
- [let kVTDecompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinggpuregistryid)
- [let kVTVideoDecoderSpecification_PreferredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_preferreddecodergpuregistryid)
- [let kVTVideoDecoderSpecification_RequiredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requireddecodergpuregistryid)
- [func VTVideoDecoderExtensionProperties(CMFormatDescription) throws -> [VTExtensionPropertiesKey : Any]](/documentation/videotoolbox/vtvideodecoderextensionproperties(_:))

### Decoding Frames

- [func VTDecompressionSessionCanAcceptFormatDescription(VTDecompressionSession, formatDescription: CMFormatDescription) -> Bool](/documentation/videotoolbox/vtdecompressionsessioncanacceptformatdescription(_:formatdescription:))
- [func VTDecompressionSessionDecodeFrame(VTDecompressionSession, sampleBuffer: CMSampleBuffer, flags: VTDecodeFrameFlags, frameRefcon: UnsafeMutableRawPointer?, infoFlagsOut: UnsafeMutablePointer<VTDecodeInfoFlags>?) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessiondecodeframe(_:samplebuffer:flags:framerefcon:infoflagsout:))
- [func VTDecompressionSessionDecodeFrame(VTDecompressionSession, sampleBuffer: CMSampleBuffer, flags: VTDecodeFrameFlags, frameOptions: CFDictionary?, frameRefcon: UnsafeMutableRawPointer?, infoFlagsOut: UnsafeMutablePointer<VTDecodeInfoFlags>?) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessiondecodeframe(_:samplebuffer:flags:frameoptions:framerefcon:infoflagsout:))
- [func VTDecompressionSessionDecodeFrame(VTDecompressionSession, sampleBuffer: CMSampleBuffer, flags: VTDecodeFrameFlags, infoFlagsOut: UnsafeMutablePointer<VTDecodeInfoFlags>?, outputHandler: VTDecompressionOutputHandler) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessiondecodeframe(_:samplebuffer:flags:infoflagsout:outputhandler:))
- [func VTDecompressionSessionDecodeFrame(VTDecompressionSession, sampleBuffer: CMSampleBuffer, flags: VTDecodeFrameFlags, frameOptions: CFDictionary?, infoFlagsOut: UnsafeMutablePointer<VTDecodeInfoFlags>?, outputHandler: VTDecompressionOutputHandler) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessiondecodeframe(_:samplebuffer:flags:frameoptions:infoflagsout:outputhandler:))
- [func VTDecompressionSessionDecodeFrame(VTDecompressionSession, sampleBuffer: CMSampleBuffer, flags: VTDecodeFrameFlags, infoFlagsOut: UnsafeMutablePointer<VTDecodeInfoFlags>?, completionHandler: (OSStatus, VTDecodeInfoFlags, CVImageBuffer?, [CMTaggedBuffer]?, CMTime, CMTime) -> Void) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessiondecodeframe(_:samplebuffer:flags:infoflagsout:completionhandler:))
- [func VTDecompressionSessionFinishDelayedFrames(VTDecompressionSession) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessionfinishdelayedframes(_:))
- [func VTDecompressionSessionWaitForAsynchronousFrames(VTDecompressionSession) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessionwaitforasynchronousframes(_:))
- [func VTDecompressionSessionCopyBlackPixelBuffer(VTDecompressionSession, pixelBufferOut: UnsafeMutablePointer<CVPixelBuffer?>) -> OSStatus](/documentation/videotoolbox/vtdecompressionsessioncopyblackpixelbuffer(_:pixelbufferout:))

### Decoding Multi-Image Frames

- [func VTIsStereoMVHEVCDecodeSupported() -> Bool](/documentation/videotoolbox/vtisstereomvhevcdecodesupported())
- [VTDecompressionMultiImageCapableOutputHandler](/documentation/videotoolbox/vtdecompressionmultiimagecapableoutputhandler)

### Invalidating a Session

- [func VTDecompressionSessionInvalidate(VTDecompressionSession)](/documentation/videotoolbox/vtdecompressionsessioninvalidate(_:))

### Accessing the Type Identifier

- [func VTDecompressionSessionGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtdecompressionsessiongettypeid())

### Data Types

- [VTDecompressionSession](/documentation/videotoolbox/vtdecompressionsession)
- [VTDecodeFrameFlags](/documentation/videotoolbox/vtdecodeframeflags)

#### Flags

- [init(rawValue: UInt32)](/documentation/videotoolbox/vtdecodeframeflags/init(rawvalue:))
- [VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags)

#### Flag values

- [static var asynchronous: VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags/asynchronous)
- [static var frameDropped: VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags/framedropped)
- [static var skippedLeadingFrameDropped: VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags/skippedleadingframedropped)
- [static var imageBufferModifiable: VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags/imagebuffermodifiable)

#### Initializers

- [init(rawValue: UInt32)](/documentation/videotoolbox/vtdecodeinfoflags/init(rawvalue:))

#### Type Properties

- [static var frameInterrupted: VTDecodeInfoFlags](/documentation/videotoolbox/vtdecodeinfoflags/frameinterrupted)
- [VTDecompressionOutputCallback](/documentation/videotoolbox/vtdecompressionoutputcallback)
- [VTDecompressionOutputCallbackRecord](/documentation/videotoolbox/vtdecompressionoutputcallbackrecord)

#### Initializers

- [init()](/documentation/videotoolbox/vtdecompressionoutputcallbackrecord/init())
- [init(decompressionOutputCallback: VTDecompressionOutputCallback?, decompressionOutputRefCon: UnsafeMutableRawPointer?)](/documentation/videotoolbox/vtdecompressionoutputcallbackrecord/init(decompressionoutputcallback:decompressionoutputrefcon:))

#### Instance Properties

- [var decompressionOutputCallback: VTDecompressionOutputCallback?](/documentation/videotoolbox/vtdecompressionoutputcallbackrecord/decompressionoutputcallback)
- [var decompressionOutputRefCon: UnsafeMutableRawPointer?](/documentation/videotoolbox/vtdecompressionoutputcallbackrecord/decompressionoutputrefcon)
- [VTDecompressionOutputHandler](/documentation/videotoolbox/vtdecompressionoutputhandler)
- [VTFrameSilo](/documentation/videotoolbox/vtframesilo-api-collection)

### Creating Frame Silos

- [func VTFrameSiloCreate(allocator: CFAllocator?, fileURL: CFURL?, timeRange: CMTimeRange, options: CFDictionary?, frameSiloOut: UnsafeMutablePointer<VTFrameSilo?>) -> OSStatus](/documentation/videotoolbox/vtframesilocreate(allocator:fileurl:timerange:options:framesiloout:))

### Configuring Frame Silos

- [func VTFrameSiloAddSampleBuffer(VTFrameSilo, sampleBuffer: CMSampleBuffer) -> OSStatus](/documentation/videotoolbox/vtframesiloaddsamplebuffer(_:samplebuffer:))
- [func VTFrameSiloSetTimeRangesForNextPass(VTFrameSilo, timeRangeCount: CMItemCount, timeRangeArray: UnsafePointer<CMTimeRange>) -> OSStatus](/documentation/videotoolbox/vtframesilosettimerangesfornextpass(_:timerangecount:timerangearray:))
- [func VTFrameSiloCallBlockForEachSampleBuffer(VTFrameSilo, in: CMTimeRange, handler: (CMSampleBuffer) -> OSStatus) -> OSStatus](/documentation/videotoolbox/vtframesilocallblockforeachsamplebuffer(_:in:handler:))
- [func VTFrameSiloCallFunctionForEachSampleBuffer(VTFrameSilo, in: CMTimeRange, refcon: UnsafeMutableRawPointer?, callback: (UnsafeMutableRawPointer?, CMSampleBuffer) -> OSStatus) -> OSStatus](/documentation/videotoolbox/vtframesilocallfunctionforeachsamplebuffer(_:in:refcon:callback:))

### Inspecting Frame Silos

- [func VTFrameSiloGetProgressOfCurrentPass(VTFrameSilo, progressOut: UnsafeMutablePointer<Float32>) -> OSStatus](/documentation/videotoolbox/vtframesilogetprogressofcurrentpass(_:progressout:))
- [func VTFrameSiloGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtframesilogettypeid())

### Data Types

- [VTFrameSilo](/documentation/videotoolbox/vtframesilo)
- [VTMultiPassStorage](/documentation/videotoolbox/vtmultipassstorage-api-collection)

### Creating Storage Objects

- [func VTMultiPassStorageCreate(allocator: CFAllocator?, fileURL: CFURL?, timeRange: CMTimeRange, options: CFDictionary?, multiPassStorageOut: UnsafeMutablePointer<VTMultiPassStorage?>) -> OSStatus](/documentation/videotoolbox/vtmultipassstoragecreate(allocator:fileurl:timerange:options:multipassstorageout:))

### Closing Storage Objects

- [func VTMultiPassStorageClose(VTMultiPassStorage) -> OSStatus](/documentation/videotoolbox/vtmultipassstorageclose(_:))

### Inspecting Storage Objects

- [func VTMultiPassStorageGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtmultipassstoragegettypeid())

### Data Types

- [VTMultiPassStorage](/documentation/videotoolbox/vtmultipassstorage)

### Constants

- [let kVTMultiPassStorageCreationOption_DoNotDelete: CFString](/documentation/videotoolbox/kvtmultipassstoragecreationoption_donotdelete)

## Transformation

- [VTPixelTransferSession](/documentation/videotoolbox/vtpixeltransfersession-api-collection)

### Creating Sessions

- [func VTPixelTransferSessionCreate(allocator: CFAllocator?, pixelTransferSessionOut: UnsafeMutablePointer<VTPixelTransferSession?>) -> OSStatus](/documentation/videotoolbox/vtpixeltransfersessioncreate(allocator:pixeltransfersessionout:))

### Configuring Sessions

- [Pixel Transfer Properties](/documentation/videotoolbox/pixel-transfer-properties)

#### Configuration

- [let kVTPixelTransferPropertyKey_ScalingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_scalingmode)
- [Scaling Mode Constants](/documentation/videotoolbox/scaling-mode-constants)

##### Scaling Modes

- [let kVTScalingMode_Normal: CFString](/documentation/videotoolbox/kvtscalingmode_normal)
- [let kVTScalingMode_CropSourceToCleanAperture: CFString](/documentation/videotoolbox/kvtscalingmode_cropsourcetocleanaperture)
- [let kVTScalingMode_Letterbox: CFString](/documentation/videotoolbox/kvtscalingmode_letterbox)
- [let kVTScalingMode_Trim: CFString](/documentation/videotoolbox/kvtscalingmode_trim)
- [let kVTPixelTransferPropertyKey_DestinationCleanAperture: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcleanaperture)
- [let kVTPixelTransferPropertyKey_DestinationPixelAspectRatio: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationpixelaspectratio)
- [let kVTPixelTransferPropertyKey_DownsamplingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_downsamplingmode)
- [Downsampling Mode Constants](/documentation/videotoolbox/downsampling-mode-constants)

##### Downsampling Modes

- [let kVTDownsamplingMode_Average: CFString](/documentation/videotoolbox/kvtdownsamplingmode_average)
- [let kVTDownsamplingMode_Decimate: CFString](/documentation/videotoolbox/kvtdownsamplingmode_decimate)
- [let kVTPixelTransferPropertyKey_DestinationColorPrimaries: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcolorprimaries)
- [let kVTPixelTransferPropertyKey_DestinationTransferFunction: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationtransferfunction)
- [let kVTPixelTransferPropertyKey_DestinationICCProfile: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationiccprofile)
- [let kVTPixelTransferPropertyKey_DestinationYCbCrMatrix: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationycbcrmatrix)
- [let kVTPixelTransferPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_realtime)

### Converting Image Data

- [func VTPixelTransferSessionTransferImage(VTPixelTransferSession, from: CVPixelBuffer, to: CVPixelBuffer) -> OSStatus](/documentation/videotoolbox/vtpixeltransfersessiontransferimage(_:from:to:))

### Inspecting Sessions

- [func VTPixelTransferSessionGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtpixeltransfersessiongettypeid())

### Ending Sessions

- [func VTPixelTransferSessionInvalidate(VTPixelTransferSession)](/documentation/videotoolbox/vtpixeltransfersessioninvalidate(_:))

### Data Types

- [VTPixelTransferSession](/documentation/videotoolbox/vtpixeltransfersession)
- [VTPixelRotationSession](/documentation/videotoolbox/vtpixelrotationsession-api-collection)

### Managing a Session

- [func VTPixelRotationSessionCreate(CFAllocator?, UnsafeMutablePointer<VTPixelRotationSession?>) -> OSStatus](/documentation/videotoolbox/vtpixelrotationsessioncreate(_:_:))
- [func VTPixelRotationSessionInvalidate(VTPixelRotationSession)](/documentation/videotoolbox/vtpixelrotationsessioninvalidate(_:))

### Configuring a Session

- [Pixel Rotation Properties](/documentation/videotoolbox/pixel-rotation-properties)

#### Configuration

- [let kVTPixelRotationPropertyKey_Rotation: CFString](/documentation/videotoolbox/kvtpixelrotationpropertykey_rotation)

##### Rotations

- [let kVTRotation_0: CFString](/documentation/videotoolbox/kvtrotation_0)
- [let kVTRotation_CW90: CFString](/documentation/videotoolbox/kvtrotation_cw90)
- [let kVTRotation_180: CFString](/documentation/videotoolbox/kvtrotation_180)
- [let kVTRotation_CCW90: CFString](/documentation/videotoolbox/kvtrotation_ccw90)
- [let kVTPixelRotationPropertyKey_FlipVerticalOrientation: CFString](/documentation/videotoolbox/kvtpixelrotationpropertykey_flipverticalorientation)
- [let kVTPixelRotationPropertyKey_FlipHorizontalOrientation: CFString](/documentation/videotoolbox/kvtpixelrotationpropertykey_fliphorizontalorientation)

### Rotating an Image

- [func VTPixelRotationSessionRotateImage(VTPixelRotationSession, CVPixelBuffer, CVPixelBuffer) -> OSStatus](/documentation/videotoolbox/vtpixelrotationsessionrotateimage(_:_:_:))

### Inspecting the Type Identifier

- [func VTPixelRotationSessionGetTypeID() -> CFTypeID](/documentation/videotoolbox/vtpixelrotationsessiongettypeid())

### Data Types

- [VTPixelRotationSession](/documentation/videotoolbox/vtpixelrotationsession)

## RAW Processing

- [VTRAWProcessingSession](/documentation/videotoolbox/vtrawprocessingsession)

### Configuring parameters

- [func parameters() -> any AsyncSequence<[VTRAWProcessingSession.Parameter], Never>](/documentation/videotoolbox/vtrawprocessingsession/parameters())
- [func updateParameter(values: [String : Any]) throws](/documentation/videotoolbox/vtrawprocessingsession/updateparameter(values:))
- [var processingParameters: [VTRAWProcessingSession.Parameter]](/documentation/videotoolbox/vtrawprocessingsession/processingparameters)
- [VTRAWProcessingSession.Parameter](/documentation/videotoolbox/vtrawprocessingsession/parameter)

#### Parameters

- [VTRAWProcessingSession.Parameter.BooleanParameter](/documentation/videotoolbox/vtrawprocessingsession/parameter/booleanparameter)

##### Instance Properties

- [var details: VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/booleanparameter/details)
- [var key: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/booleanparameter/key)
- [var values: VTRAWProcessingSession.Parameter.Values<Bool>](/documentation/videotoolbox/vtrawprocessingsession/parameter/booleanparameter/values)
- [VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/details)

##### Instance Properties

- [var description: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/details/description)
- [var isEnabled: Bool](/documentation/videotoolbox/vtrawprocessingsession/parameter/details/isenabled)
- [var name: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/details/name)
- [VTRAWProcessingSession.Parameter.FloatParameter](/documentation/videotoolbox/vtrawprocessingsession/parameter/floatparameter)

##### Instance Properties

- [var details: VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/floatparameter/details)
- [var key: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/floatparameter/key)
- [var values: VTRAWProcessingSession.Parameter.Values<Float>](/documentation/videotoolbox/vtrawprocessingsession/parameter/floatparameter/values)
- [VTRAWProcessingSession.Parameter.IntegerParameter](/documentation/videotoolbox/vtrawprocessingsession/parameter/integerparameter)

##### Instance Properties

- [var details: VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/integerparameter/details)
- [var key: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/integerparameter/key)
- [var values: VTRAWProcessingSession.Parameter.Values<Int>](/documentation/videotoolbox/vtrawprocessingsession/parameter/integerparameter/values)
- [VTRAWProcessingSession.Parameter.ListParameter](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter)

##### Structures

- [VTRAWProcessingSession.Parameter.ListParameter.Element](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/element)

###### Instance Properties

- [var details: VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/element/details)
- [var id: Int](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/element/id)

##### Instance Properties

- [var details: VTRAWProcessingSession.Parameter.Details](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/details)
- [var elements: [VTRAWProcessingSession.Parameter.ListParameter.Element]](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/elements)
- [var key: String](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/key)
- [var values: VTRAWProcessingSession.Parameter.Values<Int>](/documentation/videotoolbox/vtrawprocessingsession/parameter/listparameter/values)
- [VTRAWProcessingSession.Parameter.Values](/documentation/videotoolbox/vtrawprocessingsession/parameter/values)

##### Instance Properties

- [var camera: Value?](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/camera)
- [var current: Value](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/current)
- [var initial: Value](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/initial)
- [var maximum: Value?](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/maximum)
- [var minimum: Value?](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/minimum)
- [var neutral: Value?](/documentation/videotoolbox/vtrawprocessingsession/parameter/values/neutral)

#### Enumeration Cases

- [case bool(VTRAWProcessingSession.Parameter.BooleanParameter)](/documentation/videotoolbox/vtrawprocessingsession/parameter/bool(_:))
- [case float(VTRAWProcessingSession.Parameter.FloatParameter)](/documentation/videotoolbox/vtrawprocessingsession/parameter/float(_:))
- [case int(VTRAWProcessingSession.Parameter.IntegerParameter)](/documentation/videotoolbox/vtrawprocessingsession/parameter/int(_:))
- [case list(VTRAWProcessingSession.Parameter.ListParameter)](/documentation/videotoolbox/vtrawprocessingsession/parameter/list(_:))
- [case subgroup(details: VTRAWProcessingSession.Parameter.Details, elements: [VTRAWProcessingSession.Parameter])](/documentation/videotoolbox/vtrawprocessingsession/parameter/subgroup(details:elements:))

### Processing frames

- [func process(frame: CVPixelBuffer) async throws -> CVPixelBuffer](/documentation/videotoolbox/vtrawprocessingsession/process(frame:))

### Configuring the Metal device

- [var metalDevice: (any MTLDevice)?](/documentation/videotoolbox/vtrawprocessingsession/metaldevice)

### Initializers

- [init(referencing: VTRAWProcessingSession)](/documentation/videotoolbox/vtrawprocessingsession/init(referencing:))

### Type Aliases

- [VTRAWProcessingSession.T](/documentation/videotoolbox/vtrawprocessingsession/t)

## Media Extension

- [VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey)

### Keys

- [static let containingBundleName: VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey/containingbundlename)
- [static let containingBundleURL: VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey/containingbundleurl)
- [static let extensionIdentifier: VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey/extensionidentifier)
- [static let extensionName: VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey/extensionname)
- [static let extensionURL: VTExtensionPropertiesKey](/documentation/videotoolbox/vtextensionpropertieskey/extensionurl)

### Initializers

- [init(rawValue: CFString)](/documentation/videotoolbox/vtextensionpropertieskey/init(rawvalue:))

## HDR Metadata

- [VTHDRPerFrameMetadataGenerationSession](/documentation/videotoolbox/vthdrperframemetadatagenerationsession)

### Creating a session

- [init(framesPerSecond: Float, hdrFormats: [VTHDRPerFrameMetadataGenerationSession.HDRFormat]?) throws](/documentation/videotoolbox/vthdrperframemetadatagenerationsession/init(framespersecond:hdrformats:))

### Attaching metadata

- [func attachMetadata(to: CVPixelBuffer, sceneChange: Bool) throws](/documentation/videotoolbox/vthdrperframemetadatagenerationsession/attachmetadata(to:scenechange:))

### HDR Formats

- [VTHDRPerFrameMetadataGenerationSession.HDRFormat](/documentation/videotoolbox/vthdrperframemetadatagenerationsession/hdrformat)

#### Formats

- [case dolbyVision](/documentation/videotoolbox/vthdrperframemetadatagenerationsession/hdrformat/dolbyvision)

## Codec Support

- [func VTIsHardwareDecodeSupported(CMVideoCodecType) -> Bool](/documentation/videotoolbox/vtishardwaredecodesupported(_:))
- [func VTRegisterProfessionalVideoWorkflowVideoEncoders()](/documentation/videotoolbox/vtregisterprofessionalvideoworkflowvideoencoders())
- [func VTRegisterProfessionalVideoWorkflowVideoDecoders()](/documentation/videotoolbox/vtregisterprofessionalvideoworkflowvideodecoders())
- [func VTRegisterSupplementalVideoDecoderIfAvailable(CMVideoCodecType)](/documentation/videotoolbox/vtregistersupplementalvideodecoderifavailable(_:))
- [func VTCopySupportedPropertyDictionaryForEncoder(width: Int32, height: Int32, codecType: CMVideoCodecType, encoderSpecification: CFDictionary?, encoderIDOut: UnsafeMutablePointer<CFString?>?, supportedPropertiesOut: UnsafeMutablePointer<CFDictionary?>?) -> OSStatus](/documentation/videotoolbox/vtcopysupportedpropertydictionaryforencoder(width:height:codectype:encoderspecification:encoderidout:supportedpropertiesout:))
- [func VTCopyVideoEncoderList(CFDictionary?, UnsafeMutablePointer<CFArray?>) -> OSStatus](/documentation/videotoolbox/vtcopyvideoencoderlist(_:_:))
- [Video Encoder List Keys](/documentation/videotoolbox/video-encoder-list-keys)

### Encoder Keys

- [let kVTVideoEncoderList_EncoderID: CFString](/documentation/videotoolbox/kvtvideoencoderlist_encoderid)
- [let kVTVideoEncoderList_EncoderName: CFString](/documentation/videotoolbox/kvtvideoencoderlist_encodername)
- [let kVTVideoEncoderList_DisplayName: CFString](/documentation/videotoolbox/kvtvideoencoderlist_displayname)
- [let kVTVideoEncoderList_CodecType: CFString](/documentation/videotoolbox/kvtvideoencoderlist_codectype)
- [let kVTVideoEncoderList_CodecName: CFString](/documentation/videotoolbox/kvtvideoencoderlist_codecname)
- [let kVTVideoEncoderList_GPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderlist_gpuregistryid)
- [let kVTVideoEncoderList_InstanceLimit: CFString](/documentation/videotoolbox/kvtvideoencoderlist_instancelimit)
- [let kVTVideoEncoderList_IsHardwareAccelerated: CFString](/documentation/videotoolbox/kvtvideoencoderlist_ishardwareaccelerated)
- [let kVTVideoEncoderList_PerformanceRating: CFString](/documentation/videotoolbox/kvtvideoencoderlist_performancerating)
- [let kVTVideoEncoderList_QualityRating: CFString](/documentation/videotoolbox/kvtvideoencoderlist_qualityrating)
- [let kVTVideoEncoderList_SupportedSelectionProperties: CFString](/documentation/videotoolbox/kvtvideoencoderlist_supportedselectionproperties)
- [let kVTVideoEncoderList_SupportsFrameReordering: CFString](/documentation/videotoolbox/kvtvideoencoderlist_supportsframereordering)
- [let kVTVideoEncoderListOption_IncludeStandardDefinitionDVEncoders: CFString](/documentation/videotoolbox/kvtvideoencoderlistoption_includestandarddefinitiondvencoders)

## Utilities

- [func VTCreateCGImageFromCVPixelBuffer(CVPixelBuffer, options: CFDictionary?, imageOut: UnsafeMutablePointer<CGImage?>) -> OSStatus](/documentation/videotoolbox/vtcreatecgimagefromcvpixelbuffer(_:options:imageout:))

## Data Types

- [VTSession](/documentation/videotoolbox/vtsession-api-collection)

### Setting Properties

- [func VTSessionSetProperty(VTSession, key: CFString, value: CFTypeRef?) -> OSStatus](/documentation/videotoolbox/vtsessionsetproperty(_:key:value:))

#### Related Documentation

- [Compression Properties](/documentation/videotoolbox/compression-properties)

##### Bitstream Configuration

- [let kVTCompressionPropertyKey_Depth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_depth)
- [let kVTCompressionPropertyKey_H264EntropyMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_h264entropymode)

###### Entropy Modes

- [let kVTH264EntropyMode_CAVLC: CFString](/documentation/videotoolbox/kvth264entropymode_cavlc)
- [let kVTH264EntropyMode_CABAC: CFString](/documentation/videotoolbox/kvth264entropymode_cabac)
- [let kVTCompressionPropertyKey_HDRMetadataInsertionMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hdrmetadatainsertionmode)

###### Insertion Modes

- [let kVTHDRMetadataInsertionMode_Auto: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_auto)
- [let kVTHDRMetadataInsertionMode_None: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_none)
- [let kVTHDRMetadataInsertionMode_RequestSDRRangePreservation: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_requestsdrrangepreservation)
- [let kVTCompressionPropertyKey_OutputBitDepth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_outputbitdepth)
- [let kVTCompressionPropertyKey_PreserveAlphaChannel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservealphachannel)
- [let kVTCompressionPropertyKey_PreserveDynamicHDRMetadata: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservedynamichdrmetadata)
- [let kVTCompressionPropertyKey_ProfileLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_profilelevel)

###### HEVC

- [let kVTProfileLevel_HEVC_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main_autolevel)
- [let kVTProfileLevel_HEVC_Main10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main10_autolevel)
- [let kVTProfileLevel_HEVC_Main42210_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main42210_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome10_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome_autolevel)

###### H.264

- [let kVTProfileLevel_H264_Baseline_1_3: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_1_3)
- [let kVTProfileLevel_H264_Baseline_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_0)
- [let kVTProfileLevel_H264_Baseline_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_1)
- [let kVTProfileLevel_H264_Baseline_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_2)
- [let kVTProfileLevel_H264_Baseline_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_0)
- [let kVTProfileLevel_H264_Baseline_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_1)
- [let kVTProfileLevel_H264_Baseline_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_2)
- [let kVTProfileLevel_H264_Baseline_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_0)
- [let kVTProfileLevel_H264_Baseline_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_1)
- [let kVTProfileLevel_H264_Baseline_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_2)
- [let kVTProfileLevel_H264_Baseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedBaseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedbaseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedHigh_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedhigh_autolevel)
- [let kVTProfileLevel_H264_Extended_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_5_0)
- [let kVTProfileLevel_H264_Extended_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_autolevel)
- [let kVTProfileLevel_H264_High_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_0)
- [let kVTProfileLevel_H264_High_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_1)
- [let kVTProfileLevel_H264_High_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_2)
- [let kVTProfileLevel_H264_High_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_0)
- [let kVTProfileLevel_H264_High_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_1)
- [let kVTProfileLevel_H264_High_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_2)
- [let kVTProfileLevel_H264_High_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_0)
- [let kVTProfileLevel_H264_High_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_1)
- [let kVTProfileLevel_H264_High_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_2)
- [let kVTProfileLevel_H264_High_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_autolevel)
- [let kVTProfileLevel_H264_Main_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_0)
- [let kVTProfileLevel_H264_Main_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_1)
- [let kVTProfileLevel_H264_Main_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_2)
- [let kVTProfileLevel_H264_Main_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_0)
- [let kVTProfileLevel_H264_Main_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_1)
- [let kVTProfileLevel_H264_Main_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_2)
- [let kVTProfileLevel_H264_Main_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_0)
- [let kVTProfileLevel_H264_Main_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_1)
- [let kVTProfileLevel_H264_Main_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_2)
- [let kVTProfileLevel_H264_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_autolevel)

###### MP4V

- [let kVTProfileLevel_MP4V_Simple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l0)
- [let kVTProfileLevel_MP4V_Simple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l1)
- [let kVTProfileLevel_MP4V_Simple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l2)
- [let kVTProfileLevel_MP4V_Simple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l0)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l1)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l2)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l4)
- [let kVTProfileLevel_MP4V_Main_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l2)
- [let kVTProfileLevel_MP4V_Main_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l3)
- [let kVTProfileLevel_MP4V_Main_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l4)

###### H.263

- [let kVTProfileLevel_H263_Profile0_Level10: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level10)
- [let kVTProfileLevel_H263_Profile0_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level45)
- [let kVTProfileLevel_H263_Profile3_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile3_level45)

##### Buffers

- [let kVTCompressionPropertyKey_NumberOfPendingFrames: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_numberofpendingframes)
- [let kVTCompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelbufferpoolisshared)
- [let kVTCompressionPropertyKey_VideoEncoderPixelBufferAttributes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_videoencoderpixelbufferattributes)

##### Camera Calibration

- [let kVTCompressionPropertyKey_CameraCalibrationDataLensCollection: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cameracalibrationdatalenscollection)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOrientationQuaternion: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicorientationquaternion)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOriginSource: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicoriginsource)

###### Origin Source Values

- [let kVTCameraCalibrationExtrinsicOriginSource_StereoCameraSystemBaseline: CFString](/documentation/videotoolbox/kvtcameracalibrationextrinsicoriginsource_stereocamerasystembaseline)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrix)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixProjectionOffset: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixprojectionoffset)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixReferenceDimensions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixreferencedimensions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensAlgorithmKind: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensalgorithmkind)

###### Algorithm Kinds

- [let kVTCameraCalibrationLensAlgorithmKind_ParametricLens: CFString](/documentation/videotoolbox/kvtcameracalibrationlensalgorithmkind_parametriclens)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDistortions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdistortions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDomain: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdomain)

###### Lens Domains

- [let kVTCameraCalibrationLensDomain_Color: CFString](/documentation/videotoolbox/kvtcameracalibrationlensdomain_color)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialX: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialx)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialY: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialy)
- [let kVTCompressionPropertyCameraCalibrationKey_LensIdentifier: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensidentifier)
- [let kVTCompressionPropertyCameraCalibrationKey_LensRole: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensrole)

###### Lens Roles

- [let kVTCameraCalibrationLensRole_Left: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_left)
- [let kVTCameraCalibrationLensRole_Mono: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_mono)
- [let kVTCameraCalibrationLensRole_Right: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_right)
- [let kVTCompressionPropertyCameraCalibrationKey_RadialAngleLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_radialanglelimit)

##### Clean Aperture and Pixel Aspect Ratio

- [let kVTCompressionPropertyKey_AspectRatio16x9: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_aspectratio16x9)
- [let kVTCompressionPropertyKey_CleanAperture: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cleanaperture)
- [let kVTCompressionPropertyKey_FieldCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fieldcount)
- [let kVTCompressionPropertyKey_FieldDetail: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fielddetail)
- [let kVTCompressionPropertyKey_PixelAspectRatio: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelaspectratio)
- [let kVTCompressionPropertyKey_ProgressiveScan: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_progressivescan)

##### Color

- [let kVTCompressionPropertyKey_AlphaChannelMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_alphachannelmode)

###### Modes

- [let kVTAlphaChannelMode_StraightAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_straightalpha)
- [let kVTAlphaChannelMode_PremultipliedAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_premultipliedalpha)
- [let kVTCompressionPropertyKey_ColorPrimaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_colorprimaries)
- [let kVTCompressionPropertyKey_ContentLightLevelInfo: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_contentlightlevelinfo)
- [let kVTCompressionPropertyKey_GammaLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_gammalevel)
- [let kVTCompressionPropertyKey_ICCProfile: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_iccprofile)
- [let kVTCompressionPropertyKey_MasteringDisplayColorVolume: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_masteringdisplaycolorvolume)
- [let kVTCompressionPropertyKey_TransferFunction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_transferfunction)
- [let kVTCompressionPropertyKey_YCbCrMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_ycbcrmatrix)

##### Compression Presets

- [let kVTCompressionPreset_Balanced: CFString](/documentation/videotoolbox/kvtcompressionpreset_balanced)
- [let kVTCompressionPreset_HighQuality: CFString](/documentation/videotoolbox/kvtcompressionpreset_highquality)
- [let kVTCompressionPreset_HighSpeed: CFString](/documentation/videotoolbox/kvtcompressionpreset_highspeed)
- [let kVTCompressionPreset_VideoConferencing: CFString](/documentation/videotoolbox/kvtcompressionpreset_videoconferencing)
- [let kVTCompressionPropertyKey_SupportedPresetDictionaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportedpresetdictionaries)

##### Encoder Selection

- [let kVTCompressionPropertyKey_EncoderID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_encoderid)
- [let kVTVideoEncoderSpecification_EnableHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablehardwareacceleratedvideoencoder)
- [let kVTVideoEncoderSpecification_EnableLowLatencyRateControl: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablelowlatencyratecontrol)
- [let kVTVideoEncoderSpecification_EncoderID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_encoderid)
- [let kVTVideoEncoderSpecification_PreferredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_preferredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequiredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requiredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequireHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requirehardwareacceleratedvideoencoder)

##### Encoding Hints

- [let kVTCompressionPropertyKey_ExpectedDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedduration)
- [let kVTCompressionPropertyKey_ExpectedFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedframerate)
- [let kVTCompressionPropertyKey_MaximumRealTimeFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximumrealtimeframerate)
- [let kVTCompressionPropertyKey_PrioritizeEncodingSpeedOverQuality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_prioritizeencodingspeedoverquality)
- [let kVTCompressionPropertyKey_ReferenceBufferCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_referencebuffercount)
- [let kVTCompressionPropertyKey_SourceFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_sourceframecount)
- [let kVTCompressionPropertyKey_SuggestedLookAheadFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_suggestedlookaheadframecount)

##### Frame Dependency

- [let kVTCompressionPropertyKey_AllowFrameReordering: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowframereordering)
- [let kVTCompressionPropertyKey_AllowOpenGOP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowopengop)
- [let kVTCompressionPropertyKey_AllowTemporalCompression: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowtemporalcompression)
- [let kVTCompressionPropertyKey_MaxKeyFrameInterval: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeinterval)
- [let kVTCompressionPropertyKey_MaxKeyFrameIntervalDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeintervalduration)

##### Hardware Acceleration

- [let kVTCompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinggpuregistryid)
- [let kVTCompressionPropertyKey_UsingHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinghardwareacceleratedvideoencoder)

##### Long-Term Reference

- [let kVTCompressionPropertyKey_EnableLTR: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_enableltr)
- [let kVTEncodeFrameOptionKey_AcknowledgedLTRTokens: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_acknowledgedltrtokens)
- [let kVTEncodeFrameOptionKey_ForceLTRRefresh: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forceltrrefresh)
- [let kVTSampleAttachmentKey_RequireLTRAcknowledgementToken: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_requireltracknowledgementtoken)

##### Multipass Storage

- [let kVTCompressionPropertyKey_MultiPassStorage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_multipassstorage)

##### Multiview Compression

- [let kVTCompressionPropertyKey_MVHEVCLeftAndRightViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcleftandrightviewids)
- [let kVTCompressionPropertyKey_MVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcvideolayerids)
- [let kVTCompressionPropertyKey_MVHEVCViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcviewids)

##### Parallelization

- [let kVTCompressionPropertyKey_RecommendedParallelizationLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizationlimit)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumduration)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumframecount)

##### Per-Frame Configuration

- [let kVTEncodeFrameOptionKey_BaseFrameQP: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_baseframeqp)
- [let kVTEncodeFrameOptionKey_ForceKeyFrame: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forcekeyframe)

##### Precompression Processing

- [let kVTCompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixeltransferproperties)

##### Quality Metrics

- [let kVTCompressionPropertyKey_CalculateMeanSquaredError: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_calculatemeansquarederror)
- [let kVTSampleAttachmentKey_QualityMetrics: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_qualitymetrics)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaBlueMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromabluemeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaRedMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromaredmeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_LumaMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_lumameansquarederror)

##### Quantization

- [let kVTCompressionPropertyKey_MaxAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxallowedframeqp)
- [let kVTCompressionPropertyKey_MinAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_minallowedframeqp)
- [let kVTCompressionPropertyKey_SpatialAdaptiveQPLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_spatialadaptiveqplevel)

###### Levels

- [var kVTQPModulationLevel_Default: Int](/documentation/videotoolbox/kvtqpmodulationlevel_default)
- [var kVTQPModulationLevel_Disable: Int](/documentation/videotoolbox/kvtqpmodulationlevel_disable)
- [let kVTCompressionPropertyKey_SupportsBaseFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportsbaseframeqp)

##### Rate Control

- [let kVTCompressionPropertyKey_AverageBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_averagebitrate)
- [let kVTCompressionPropertyKey_ConstantBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_constantbitrate)
- [let kVTCompressionPropertyKey_DataRateLimits: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_dataratelimits)
- [let kVTCompressionPropertyKey_EstimatedAverageBytesPerFrame: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_estimatedaveragebytesperframe)
- [let kVTCompressionPropertyKey_MoreFramesAfterEnd: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesafterend)
- [let kVTCompressionPropertyKey_MoreFramesBeforeStart: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesbeforestart)
- [let kVTCompressionPropertyKey_Quality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_quality)
- [let kVTCompressionPropertyKey_TargetQualityForAlpha: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_targetqualityforalpha)
- [let kVTCompressionPropertyKey_VariableBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_variablebitrate)
- [let kVTCompressionPropertyKey_VBVBufferDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvbufferduration)
- [let kVTCompressionPropertyKey_VBVInitialDelayPercentage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvinitialdelaypercentage)
- [let kVTCompressionPropertyKey_VBVMaxBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvmaxbitrate)

##### Runtime Restrictions

- [let kVTCompressionPropertyKey_MaxFrameDelayCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxframedelaycount)

###### Delay Counts

- [var kVTUnlimitedFrameDelayCount: Int](/documentation/videotoolbox/kvtunlimitedframedelaycount)
- [let kVTCompressionPropertyKey_MaxH264SliceBytes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxh264slicebytes)
- [let kVTCompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximizepowerefficiency)
- [let kVTCompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_realtime)

##### Temporal Scalability

- [let kVTCompressionPropertyKey_BaseLayerBitRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerbitratefraction)
- [let kVTCompressionPropertyKey_BaseLayerFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframerate)
- [let kVTCompressionPropertyKey_BaseLayerFrameRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframeratefraction)

##### Video Extended Usage (VEXU) Signaling

- [let kVTCompressionPropertyKey_HasLeftStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasleftstereoeyeview)
- [let kVTCompressionPropertyKey_HasRightStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasrightstereoeyeview)
- [let kVTCompressionPropertyKey_HeroEye: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_heroeye)

###### Hero Eye Values

- [let kVTHeroEye_Left: CFString](/documentation/videotoolbox/kvtheroeye_left)
- [let kVTHeroEye_Right: CFString](/documentation/videotoolbox/kvtheroeye_right)
- [let kVTCompressionPropertyKey_HorizontalDisparityAdjustment: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontaldisparityadjustment)
- [let kVTCompressionPropertyKey_HorizontalFieldOfView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontalfieldofview)
- [let kVTCompressionPropertyKey_ProjectionKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_projectionkind)

###### Projection Kinds

- [let kVTProjectionKind_Rectilinear: CFString](/documentation/videotoolbox/kvtprojectionkind_rectilinear)
- [let kVTProjectionKind_Equirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_equirectangular)
- [let kVTProjectionKind_HalfEquirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_halfequirectangular)
- [let kVTProjectionKind_ParametricImmersive: CFString](/documentation/videotoolbox/kvtprojectionkind_parametricimmersive)
- [let kVTCompressionPropertyKey_StereoCameraBaseline: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_stereocamerabaseline)
- [let kVTCompressionPropertyKey_ViewPackingKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_viewpackingkind)

###### View Packing Kinds

- [let kVTViewPackingKind_SideBySide: CFString](/documentation/videotoolbox/kvtviewpackingkind_sidebyside)
- [let kVTViewPackingKind_OverUnder: CFString](/documentation/videotoolbox/kvtviewpackingkind_overunder)
- [Decompression Properties](/documentation/videotoolbox/decompression-properties)

##### Asynchronous State

- [let kVTDecompressionPropertyKey_MaxOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maxoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_MinOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_minoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_NumberOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_numberofframesbeingdecoded)

##### Content

- [let kVTDecompressionPropertyKey_ContentHasInterframeDependencies: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_contenthasinterframedependencies)

##### Decoder Behavior

- [let kVTDecompressionProperty_TemporalLevelLimit: CFString](/documentation/videotoolbox/kvtdecompressionproperty_temporallevellimit)
- [let kVTDecompressionPropertyKey_AllowBitstreamToChangeFrameDimensions: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_allowbitstreamtochangeframedimensions)
- [let kVTDecompressionPropertyKey_DeinterlaceMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_deinterlacemode)

###### Deinterlace Modes

- [let kVTDecompressionProperty_DeinterlaceMode_VerticalFilter: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_verticalfilter)
- [let kVTDecompressionProperty_DeinterlaceMode_Temporal: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_temporal)
- [let kVTDecompressionPropertyKey_FieldMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_fieldmode)

###### Field Modes

- [let kVTDecompressionProperty_FieldMode_BothFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bothfields)
- [let kVTDecompressionProperty_FieldMode_BottomFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bottomfieldonly)
- [let kVTDecompressionProperty_FieldMode_DeinterlaceFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_deinterlacefields)
- [let kVTDecompressionProperty_FieldMode_SingleField: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_singlefield)
- [let kVTDecompressionProperty_FieldMode_TopFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_topfieldonly)
- [let kVTDecompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maximizepowerefficiency)
- [let kVTDecompressionPropertyKey_OnlyTheseFrames: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_onlytheseframes)

###### Frame Constants

- [let kVTDecompressionProperty_OnlyTheseFrames_AllFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_allframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_IFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_iframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_KeyFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_keyframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_NonDroppableFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_nondroppableframes)
- [let kVTDecompressionPropertyKey_PixelFormatsWithReducedResolutionSupport: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelformatswithreducedresolutionsupport)
- [let kVTDecompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_realtime)
- [let kVTDecompressionPropertyKey_ReducedCoefficientDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedcoefficientdecode)
- [let kVTDecompressionPropertyKey_ReducedFrameDelivery: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedframedelivery)
- [let kVTDecompressionPropertyKey_ReducedResolutionDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedresolutiondecode)

###### Resolutions

- [let kVTDecompressionResolutionKey_Width: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_width)
- [let kVTDecompressionResolutionKey_Height: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_height)
- [let kVTDecompressionPropertyKey_SuggestedQualityOfServiceTiers: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_suggestedqualityofservicetiers)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByPerformance: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyperformance)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByQuality: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyquality)
- [let kVTDecompressionPropertyKey_ThreadCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_threadcount)

##### Hardware Acceleration

- [let kVTDecompressionPropertyKey_UsingHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinghardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_EnableHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_enablehardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_RequireHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requirehardwareacceleratedvideodecoder)

##### Multi-Image Decompression

- [let kVTDecompressionPropertyKey_RequestedMVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestedmvhevcvideolayerids)

##### Per-Frame Decoder Options

- [let kVTDecodeFrameOptionKey_ContentAnalyzerCropRectangle: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzercroprectangle)
- [let kVTDecodeFrameOptionKey_ContentAnalyzerRotation: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzerrotation)

##### Pixel Buffer Pools

- [let kVTDecompressionPropertyKey_OutputPoolRequestedMinimumBufferCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_outputpoolrequestedminimumbuffercount)
- [let kVTDecompressionPropertyKey_PixelBufferPool: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpool)
- [let kVTDecompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpoolisshared)

##### Post-Decompression Processing

- [let kVTDecompressionPropertyKey_DecoderProducesRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_decoderproducesrawoutput)
- [let kVTDecompressionPropertyKey_GeneratePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_generateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixeltransferproperties)
- [let kVTDecompressionPropertyKey_PropagatePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_propagateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_RequestRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestrawoutput)
- [let kVTDecompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinggpuregistryid)
- [let kVTVideoDecoderSpecification_PreferredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_preferreddecodergpuregistryid)
- [let kVTVideoDecoderSpecification_RequiredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requireddecodergpuregistryid)
- [Pixel Transfer Properties](/documentation/videotoolbox/pixel-transfer-properties)

##### Configuration

- [let kVTPixelTransferPropertyKey_ScalingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_scalingmode)
- [Scaling Mode Constants](/documentation/videotoolbox/scaling-mode-constants)

###### Scaling Modes

- [let kVTScalingMode_Normal: CFString](/documentation/videotoolbox/kvtscalingmode_normal)
- [let kVTScalingMode_CropSourceToCleanAperture: CFString](/documentation/videotoolbox/kvtscalingmode_cropsourcetocleanaperture)
- [let kVTScalingMode_Letterbox: CFString](/documentation/videotoolbox/kvtscalingmode_letterbox)
- [let kVTScalingMode_Trim: CFString](/documentation/videotoolbox/kvtscalingmode_trim)
- [let kVTPixelTransferPropertyKey_DestinationCleanAperture: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcleanaperture)
- [let kVTPixelTransferPropertyKey_DestinationPixelAspectRatio: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationpixelaspectratio)
- [let kVTPixelTransferPropertyKey_DownsamplingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_downsamplingmode)
- [Downsampling Mode Constants](/documentation/videotoolbox/downsampling-mode-constants)

###### Downsampling Modes

- [let kVTDownsamplingMode_Average: CFString](/documentation/videotoolbox/kvtdownsamplingmode_average)
- [let kVTDownsamplingMode_Decimate: CFString](/documentation/videotoolbox/kvtdownsamplingmode_decimate)
- [let kVTPixelTransferPropertyKey_DestinationColorPrimaries: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcolorprimaries)
- [let kVTPixelTransferPropertyKey_DestinationTransferFunction: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationtransferfunction)
- [let kVTPixelTransferPropertyKey_DestinationICCProfile: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationiccprofile)
- [let kVTPixelTransferPropertyKey_DestinationYCbCrMatrix: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationycbcrmatrix)
- [let kVTPixelTransferPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_realtime)
- [func VTSessionSetProperties(VTSession, propertyDictionary: CFDictionary) -> OSStatus](/documentation/videotoolbox/vtsessionsetproperties(_:propertydictionary:))

#### Related Documentation

- [Compression Properties](/documentation/videotoolbox/compression-properties)

##### Bitstream Configuration

- [let kVTCompressionPropertyKey_Depth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_depth)
- [let kVTCompressionPropertyKey_H264EntropyMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_h264entropymode)

###### Entropy Modes

- [let kVTH264EntropyMode_CAVLC: CFString](/documentation/videotoolbox/kvth264entropymode_cavlc)
- [let kVTH264EntropyMode_CABAC: CFString](/documentation/videotoolbox/kvth264entropymode_cabac)
- [let kVTCompressionPropertyKey_HDRMetadataInsertionMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hdrmetadatainsertionmode)

###### Insertion Modes

- [let kVTHDRMetadataInsertionMode_Auto: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_auto)
- [let kVTHDRMetadataInsertionMode_None: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_none)
- [let kVTHDRMetadataInsertionMode_RequestSDRRangePreservation: CFString](/documentation/videotoolbox/kvthdrmetadatainsertionmode_requestsdrrangepreservation)
- [let kVTCompressionPropertyKey_OutputBitDepth: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_outputbitdepth)
- [let kVTCompressionPropertyKey_PreserveAlphaChannel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservealphachannel)
- [let kVTCompressionPropertyKey_PreserveDynamicHDRMetadata: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_preservedynamichdrmetadata)
- [let kVTCompressionPropertyKey_ProfileLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_profilelevel)

###### HEVC

- [let kVTProfileLevel_HEVC_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main_autolevel)
- [let kVTProfileLevel_HEVC_Main10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main10_autolevel)
- [let kVTProfileLevel_HEVC_Main42210_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_main42210_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome10_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome10_autolevel)
- [let kVTProfileLevel_HEVC_Monochrome_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_hevc_monochrome_autolevel)

###### H.264

- [let kVTProfileLevel_H264_Baseline_1_3: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_1_3)
- [let kVTProfileLevel_H264_Baseline_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_0)
- [let kVTProfileLevel_H264_Baseline_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_1)
- [let kVTProfileLevel_H264_Baseline_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_3_2)
- [let kVTProfileLevel_H264_Baseline_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_0)
- [let kVTProfileLevel_H264_Baseline_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_1)
- [let kVTProfileLevel_H264_Baseline_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_4_2)
- [let kVTProfileLevel_H264_Baseline_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_0)
- [let kVTProfileLevel_H264_Baseline_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_1)
- [let kVTProfileLevel_H264_Baseline_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_5_2)
- [let kVTProfileLevel_H264_Baseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_baseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedBaseline_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedbaseline_autolevel)
- [let kVTProfileLevel_H264_ConstrainedHigh_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_constrainedhigh_autolevel)
- [let kVTProfileLevel_H264_Extended_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_5_0)
- [let kVTProfileLevel_H264_Extended_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_extended_autolevel)
- [let kVTProfileLevel_H264_High_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_0)
- [let kVTProfileLevel_H264_High_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_1)
- [let kVTProfileLevel_H264_High_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_3_2)
- [let kVTProfileLevel_H264_High_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_0)
- [let kVTProfileLevel_H264_High_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_1)
- [let kVTProfileLevel_H264_High_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_4_2)
- [let kVTProfileLevel_H264_High_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_0)
- [let kVTProfileLevel_H264_High_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_1)
- [let kVTProfileLevel_H264_High_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_5_2)
- [let kVTProfileLevel_H264_High_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_high_autolevel)
- [let kVTProfileLevel_H264_Main_3_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_0)
- [let kVTProfileLevel_H264_Main_3_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_1)
- [let kVTProfileLevel_H264_Main_3_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_3_2)
- [let kVTProfileLevel_H264_Main_4_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_0)
- [let kVTProfileLevel_H264_Main_4_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_1)
- [let kVTProfileLevel_H264_Main_4_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_4_2)
- [let kVTProfileLevel_H264_Main_5_0: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_0)
- [let kVTProfileLevel_H264_Main_5_1: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_1)
- [let kVTProfileLevel_H264_Main_5_2: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_5_2)
- [let kVTProfileLevel_H264_Main_AutoLevel: CFString](/documentation/videotoolbox/kvtprofilelevel_h264_main_autolevel)

###### MP4V

- [let kVTProfileLevel_MP4V_Simple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l0)
- [let kVTProfileLevel_MP4V_Simple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l1)
- [let kVTProfileLevel_MP4V_Simple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l2)
- [let kVTProfileLevel_MP4V_Simple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_simple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L0: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l0)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L1: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l1)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l2)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l3)
- [let kVTProfileLevel_MP4V_AdvancedSimple_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_advancedsimple_l4)
- [let kVTProfileLevel_MP4V_Main_L2: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l2)
- [let kVTProfileLevel_MP4V_Main_L3: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l3)
- [let kVTProfileLevel_MP4V_Main_L4: CFString](/documentation/videotoolbox/kvtprofilelevel_mp4v_main_l4)

###### H.263

- [let kVTProfileLevel_H263_Profile0_Level10: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level10)
- [let kVTProfileLevel_H263_Profile0_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile0_level45)
- [let kVTProfileLevel_H263_Profile3_Level45: CFString](/documentation/videotoolbox/kvtprofilelevel_h263_profile3_level45)

##### Buffers

- [let kVTCompressionPropertyKey_NumberOfPendingFrames: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_numberofpendingframes)
- [let kVTCompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelbufferpoolisshared)
- [let kVTCompressionPropertyKey_VideoEncoderPixelBufferAttributes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_videoencoderpixelbufferattributes)

##### Camera Calibration

- [let kVTCompressionPropertyKey_CameraCalibrationDataLensCollection: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cameracalibrationdatalenscollection)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOrientationQuaternion: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicorientationquaternion)
- [let kVTCompressionPropertyCameraCalibrationKey_ExtrinsicOriginSource: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_extrinsicoriginsource)

###### Origin Source Values

- [let kVTCameraCalibrationExtrinsicOriginSource_StereoCameraSystemBaseline: CFString](/documentation/videotoolbox/kvtcameracalibrationextrinsicoriginsource_stereocamerasystembaseline)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrix)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixProjectionOffset: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixprojectionoffset)
- [let kVTCompressionPropertyCameraCalibrationKey_IntrinsicMatrixReferenceDimensions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_intrinsicmatrixreferencedimensions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensAlgorithmKind: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensalgorithmkind)

###### Algorithm Kinds

- [let kVTCameraCalibrationLensAlgorithmKind_ParametricLens: CFString](/documentation/videotoolbox/kvtcameracalibrationlensalgorithmkind_parametriclens)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDistortions: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdistortions)
- [let kVTCompressionPropertyCameraCalibrationKey_LensDomain: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensdomain)

###### Lens Domains

- [let kVTCameraCalibrationLensDomain_Color: CFString](/documentation/videotoolbox/kvtcameracalibrationlensdomain_color)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialX: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialx)
- [let kVTCompressionPropertyCameraCalibrationKey_LensFrameAdjustmentsPolynomialY: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensframeadjustmentspolynomialy)
- [let kVTCompressionPropertyCameraCalibrationKey_LensIdentifier: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensidentifier)
- [let kVTCompressionPropertyCameraCalibrationKey_LensRole: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_lensrole)

###### Lens Roles

- [let kVTCameraCalibrationLensRole_Left: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_left)
- [let kVTCameraCalibrationLensRole_Mono: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_mono)
- [let kVTCameraCalibrationLensRole_Right: CFString](/documentation/videotoolbox/kvtcameracalibrationlensrole_right)
- [let kVTCompressionPropertyCameraCalibrationKey_RadialAngleLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertycameracalibrationkey_radialanglelimit)

##### Clean Aperture and Pixel Aspect Ratio

- [let kVTCompressionPropertyKey_AspectRatio16x9: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_aspectratio16x9)
- [let kVTCompressionPropertyKey_CleanAperture: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_cleanaperture)
- [let kVTCompressionPropertyKey_FieldCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fieldcount)
- [let kVTCompressionPropertyKey_FieldDetail: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_fielddetail)
- [let kVTCompressionPropertyKey_PixelAspectRatio: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixelaspectratio)
- [let kVTCompressionPropertyKey_ProgressiveScan: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_progressivescan)

##### Color

- [let kVTCompressionPropertyKey_AlphaChannelMode: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_alphachannelmode)

###### Modes

- [let kVTAlphaChannelMode_StraightAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_straightalpha)
- [let kVTAlphaChannelMode_PremultipliedAlpha: CFString](/documentation/videotoolbox/kvtalphachannelmode_premultipliedalpha)
- [let kVTCompressionPropertyKey_ColorPrimaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_colorprimaries)
- [let kVTCompressionPropertyKey_ContentLightLevelInfo: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_contentlightlevelinfo)
- [let kVTCompressionPropertyKey_GammaLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_gammalevel)
- [let kVTCompressionPropertyKey_ICCProfile: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_iccprofile)
- [let kVTCompressionPropertyKey_MasteringDisplayColorVolume: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_masteringdisplaycolorvolume)
- [let kVTCompressionPropertyKey_TransferFunction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_transferfunction)
- [let kVTCompressionPropertyKey_YCbCrMatrix: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_ycbcrmatrix)

##### Compression Presets

- [let kVTCompressionPreset_Balanced: CFString](/documentation/videotoolbox/kvtcompressionpreset_balanced)
- [let kVTCompressionPreset_HighQuality: CFString](/documentation/videotoolbox/kvtcompressionpreset_highquality)
- [let kVTCompressionPreset_HighSpeed: CFString](/documentation/videotoolbox/kvtcompressionpreset_highspeed)
- [let kVTCompressionPreset_VideoConferencing: CFString](/documentation/videotoolbox/kvtcompressionpreset_videoconferencing)
- [let kVTCompressionPropertyKey_SupportedPresetDictionaries: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportedpresetdictionaries)

##### Encoder Selection

- [let kVTCompressionPropertyKey_EncoderID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_encoderid)
- [let kVTVideoEncoderSpecification_EnableHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablehardwareacceleratedvideoencoder)
- [let kVTVideoEncoderSpecification_EnableLowLatencyRateControl: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_enablelowlatencyratecontrol)
- [let kVTVideoEncoderSpecification_EncoderID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_encoderid)
- [let kVTVideoEncoderSpecification_PreferredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_preferredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequiredEncoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requiredencodergpuregistryid)
- [let kVTVideoEncoderSpecification_RequireHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtvideoencoderspecification_requirehardwareacceleratedvideoencoder)

##### Encoding Hints

- [let kVTCompressionPropertyKey_ExpectedDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedduration)
- [let kVTCompressionPropertyKey_ExpectedFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_expectedframerate)
- [let kVTCompressionPropertyKey_MaximumRealTimeFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximumrealtimeframerate)
- [let kVTCompressionPropertyKey_PrioritizeEncodingSpeedOverQuality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_prioritizeencodingspeedoverquality)
- [let kVTCompressionPropertyKey_ReferenceBufferCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_referencebuffercount)
- [let kVTCompressionPropertyKey_SourceFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_sourceframecount)
- [let kVTCompressionPropertyKey_SuggestedLookAheadFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_suggestedlookaheadframecount)

##### Frame Dependency

- [let kVTCompressionPropertyKey_AllowFrameReordering: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowframereordering)
- [let kVTCompressionPropertyKey_AllowOpenGOP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowopengop)
- [let kVTCompressionPropertyKey_AllowTemporalCompression: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_allowtemporalcompression)
- [let kVTCompressionPropertyKey_MaxKeyFrameInterval: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeinterval)
- [let kVTCompressionPropertyKey_MaxKeyFrameIntervalDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxkeyframeintervalduration)

##### Hardware Acceleration

- [let kVTCompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinggpuregistryid)
- [let kVTCompressionPropertyKey_UsingHardwareAcceleratedVideoEncoder: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_usinghardwareacceleratedvideoencoder)

##### Long-Term Reference

- [let kVTCompressionPropertyKey_EnableLTR: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_enableltr)
- [let kVTEncodeFrameOptionKey_AcknowledgedLTRTokens: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_acknowledgedltrtokens)
- [let kVTEncodeFrameOptionKey_ForceLTRRefresh: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forceltrrefresh)
- [let kVTSampleAttachmentKey_RequireLTRAcknowledgementToken: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_requireltracknowledgementtoken)

##### Multipass Storage

- [let kVTCompressionPropertyKey_MultiPassStorage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_multipassstorage)

##### Multiview Compression

- [let kVTCompressionPropertyKey_MVHEVCLeftAndRightViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcleftandrightviewids)
- [let kVTCompressionPropertyKey_MVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcvideolayerids)
- [let kVTCompressionPropertyKey_MVHEVCViewIDs: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_mvhevcviewids)

##### Parallelization

- [let kVTCompressionPropertyKey_RecommendedParallelizationLimit: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizationlimit)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumduration)
- [let kVTCompressionPropertyKey_RecommendedParallelizedSubdivisionMinimumFrameCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_recommendedparallelizedsubdivisionminimumframecount)

##### Per-Frame Configuration

- [let kVTEncodeFrameOptionKey_BaseFrameQP: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_baseframeqp)
- [let kVTEncodeFrameOptionKey_ForceKeyFrame: CFString](/documentation/videotoolbox/kvtencodeframeoptionkey_forcekeyframe)

##### Precompression Processing

- [let kVTCompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_pixeltransferproperties)

##### Quality Metrics

- [let kVTCompressionPropertyKey_CalculateMeanSquaredError: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_calculatemeansquarederror)
- [let kVTSampleAttachmentKey_QualityMetrics: CFString](/documentation/videotoolbox/kvtsampleattachmentkey_qualitymetrics)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaBlueMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromabluemeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_ChromaRedMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_chromaredmeansquarederror)
- [let kVTSampleAttachmentQualityMetricsKey_LumaMeanSquaredError: CFString](/documentation/videotoolbox/kvtsampleattachmentqualitymetricskey_lumameansquarederror)

##### Quantization

- [let kVTCompressionPropertyKey_MaxAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxallowedframeqp)
- [let kVTCompressionPropertyKey_MinAllowedFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_minallowedframeqp)
- [let kVTCompressionPropertyKey_SpatialAdaptiveQPLevel: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_spatialadaptiveqplevel)

###### Levels

- [var kVTQPModulationLevel_Default: Int](/documentation/videotoolbox/kvtqpmodulationlevel_default)
- [var kVTQPModulationLevel_Disable: Int](/documentation/videotoolbox/kvtqpmodulationlevel_disable)
- [let kVTCompressionPropertyKey_SupportsBaseFrameQP: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_supportsbaseframeqp)

##### Rate Control

- [let kVTCompressionPropertyKey_AverageBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_averagebitrate)
- [let kVTCompressionPropertyKey_ConstantBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_constantbitrate)
- [let kVTCompressionPropertyKey_DataRateLimits: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_dataratelimits)
- [let kVTCompressionPropertyKey_EstimatedAverageBytesPerFrame: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_estimatedaveragebytesperframe)
- [let kVTCompressionPropertyKey_MoreFramesAfterEnd: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesafterend)
- [let kVTCompressionPropertyKey_MoreFramesBeforeStart: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_moreframesbeforestart)
- [let kVTCompressionPropertyKey_Quality: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_quality)
- [let kVTCompressionPropertyKey_TargetQualityForAlpha: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_targetqualityforalpha)
- [let kVTCompressionPropertyKey_VariableBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_variablebitrate)
- [let kVTCompressionPropertyKey_VBVBufferDuration: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvbufferduration)
- [let kVTCompressionPropertyKey_VBVInitialDelayPercentage: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvinitialdelaypercentage)
- [let kVTCompressionPropertyKey_VBVMaxBitRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_vbvmaxbitrate)

##### Runtime Restrictions

- [let kVTCompressionPropertyKey_MaxFrameDelayCount: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxframedelaycount)

###### Delay Counts

- [var kVTUnlimitedFrameDelayCount: Int](/documentation/videotoolbox/kvtunlimitedframedelaycount)
- [let kVTCompressionPropertyKey_MaxH264SliceBytes: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maxh264slicebytes)
- [let kVTCompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_maximizepowerefficiency)
- [let kVTCompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_realtime)

##### Temporal Scalability

- [let kVTCompressionPropertyKey_BaseLayerBitRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerbitratefraction)
- [let kVTCompressionPropertyKey_BaseLayerFrameRate: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframerate)
- [let kVTCompressionPropertyKey_BaseLayerFrameRateFraction: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_baselayerframeratefraction)

##### Video Extended Usage (VEXU) Signaling

- [let kVTCompressionPropertyKey_HasLeftStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasleftstereoeyeview)
- [let kVTCompressionPropertyKey_HasRightStereoEyeView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_hasrightstereoeyeview)
- [let kVTCompressionPropertyKey_HeroEye: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_heroeye)

###### Hero Eye Values

- [let kVTHeroEye_Left: CFString](/documentation/videotoolbox/kvtheroeye_left)
- [let kVTHeroEye_Right: CFString](/documentation/videotoolbox/kvtheroeye_right)
- [let kVTCompressionPropertyKey_HorizontalDisparityAdjustment: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontaldisparityadjustment)
- [let kVTCompressionPropertyKey_HorizontalFieldOfView: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_horizontalfieldofview)
- [let kVTCompressionPropertyKey_ProjectionKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_projectionkind)

###### Projection Kinds

- [let kVTProjectionKind_Rectilinear: CFString](/documentation/videotoolbox/kvtprojectionkind_rectilinear)
- [let kVTProjectionKind_Equirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_equirectangular)
- [let kVTProjectionKind_HalfEquirectangular: CFString](/documentation/videotoolbox/kvtprojectionkind_halfequirectangular)
- [let kVTProjectionKind_ParametricImmersive: CFString](/documentation/videotoolbox/kvtprojectionkind_parametricimmersive)
- [let kVTCompressionPropertyKey_StereoCameraBaseline: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_stereocamerabaseline)
- [let kVTCompressionPropertyKey_ViewPackingKind: CFString](/documentation/videotoolbox/kvtcompressionpropertykey_viewpackingkind)

###### View Packing Kinds

- [let kVTViewPackingKind_SideBySide: CFString](/documentation/videotoolbox/kvtviewpackingkind_sidebyside)
- [let kVTViewPackingKind_OverUnder: CFString](/documentation/videotoolbox/kvtviewpackingkind_overunder)
- [Decompression Properties](/documentation/videotoolbox/decompression-properties)

##### Asynchronous State

- [let kVTDecompressionPropertyKey_MaxOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maxoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_MinOutputPresentationTimeStampOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_minoutputpresentationtimestampofframesbeingdecoded)
- [let kVTDecompressionPropertyKey_NumberOfFramesBeingDecoded: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_numberofframesbeingdecoded)

##### Content

- [let kVTDecompressionPropertyKey_ContentHasInterframeDependencies: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_contenthasinterframedependencies)

##### Decoder Behavior

- [let kVTDecompressionProperty_TemporalLevelLimit: CFString](/documentation/videotoolbox/kvtdecompressionproperty_temporallevellimit)
- [let kVTDecompressionPropertyKey_AllowBitstreamToChangeFrameDimensions: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_allowbitstreamtochangeframedimensions)
- [let kVTDecompressionPropertyKey_DeinterlaceMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_deinterlacemode)

###### Deinterlace Modes

- [let kVTDecompressionProperty_DeinterlaceMode_VerticalFilter: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_verticalfilter)
- [let kVTDecompressionProperty_DeinterlaceMode_Temporal: CFString](/documentation/videotoolbox/kvtdecompressionproperty_deinterlacemode_temporal)
- [let kVTDecompressionPropertyKey_FieldMode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_fieldmode)

###### Field Modes

- [let kVTDecompressionProperty_FieldMode_BothFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bothfields)
- [let kVTDecompressionProperty_FieldMode_BottomFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_bottomfieldonly)
- [let kVTDecompressionProperty_FieldMode_DeinterlaceFields: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_deinterlacefields)
- [let kVTDecompressionProperty_FieldMode_SingleField: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_singlefield)
- [let kVTDecompressionProperty_FieldMode_TopFieldOnly: CFString](/documentation/videotoolbox/kvtdecompressionproperty_fieldmode_topfieldonly)
- [let kVTDecompressionPropertyKey_MaximizePowerEfficiency: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_maximizepowerefficiency)
- [let kVTDecompressionPropertyKey_OnlyTheseFrames: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_onlytheseframes)

###### Frame Constants

- [let kVTDecompressionProperty_OnlyTheseFrames_AllFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_allframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_IFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_iframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_KeyFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_keyframes)
- [let kVTDecompressionProperty_OnlyTheseFrames_NonDroppableFrames: CFString](/documentation/videotoolbox/kvtdecompressionproperty_onlytheseframes_nondroppableframes)
- [let kVTDecompressionPropertyKey_PixelFormatsWithReducedResolutionSupport: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelformatswithreducedresolutionsupport)
- [let kVTDecompressionPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_realtime)
- [let kVTDecompressionPropertyKey_ReducedCoefficientDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedcoefficientdecode)
- [let kVTDecompressionPropertyKey_ReducedFrameDelivery: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedframedelivery)
- [let kVTDecompressionPropertyKey_ReducedResolutionDecode: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_reducedresolutiondecode)

###### Resolutions

- [let kVTDecompressionResolutionKey_Width: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_width)
- [let kVTDecompressionResolutionKey_Height: CFString](/documentation/videotoolbox/kvtdecompressionresolutionkey_height)
- [let kVTDecompressionPropertyKey_SuggestedQualityOfServiceTiers: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_suggestedqualityofservicetiers)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByPerformance: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyperformance)
- [let kVTDecompressionPropertyKey_SupportedPixelFormatsOrderedByQuality: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_supportedpixelformatsorderedbyquality)
- [let kVTDecompressionPropertyKey_ThreadCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_threadcount)

##### Hardware Acceleration

- [let kVTDecompressionPropertyKey_UsingHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinghardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_EnableHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_enablehardwareacceleratedvideodecoder)
- [let kVTVideoDecoderSpecification_RequireHardwareAcceleratedVideoDecoder: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requirehardwareacceleratedvideodecoder)

##### Multi-Image Decompression

- [let kVTDecompressionPropertyKey_RequestedMVHEVCVideoLayerIDs: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestedmvhevcvideolayerids)

##### Per-Frame Decoder Options

- [let kVTDecodeFrameOptionKey_ContentAnalyzerCropRectangle: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzercroprectangle)
- [let kVTDecodeFrameOptionKey_ContentAnalyzerRotation: CFString](/documentation/videotoolbox/kvtdecodeframeoptionkey_contentanalyzerrotation)

##### Pixel Buffer Pools

- [let kVTDecompressionPropertyKey_OutputPoolRequestedMinimumBufferCount: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_outputpoolrequestedminimumbuffercount)
- [let kVTDecompressionPropertyKey_PixelBufferPool: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpool)
- [let kVTDecompressionPropertyKey_PixelBufferPoolIsShared: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixelbufferpoolisshared)

##### Post-Decompression Processing

- [let kVTDecompressionPropertyKey_DecoderProducesRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_decoderproducesrawoutput)
- [let kVTDecompressionPropertyKey_GeneratePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_generateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_PixelTransferProperties: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_pixeltransferproperties)
- [let kVTDecompressionPropertyKey_PropagatePerFrameHDRDisplayMetadata: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_propagateperframehdrdisplaymetadata)
- [let kVTDecompressionPropertyKey_RequestRAWOutput: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_requestrawoutput)
- [let kVTDecompressionPropertyKey_UsingGPURegistryID: CFString](/documentation/videotoolbox/kvtdecompressionpropertykey_usinggpuregistryid)
- [let kVTVideoDecoderSpecification_PreferredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_preferreddecodergpuregistryid)
- [let kVTVideoDecoderSpecification_RequiredDecoderGPURegistryID: CFString](/documentation/videotoolbox/kvtvideodecoderspecification_requireddecodergpuregistryid)
- [Pixel Transfer Properties](/documentation/videotoolbox/pixel-transfer-properties)

##### Configuration

- [let kVTPixelTransferPropertyKey_ScalingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_scalingmode)
- [Scaling Mode Constants](/documentation/videotoolbox/scaling-mode-constants)

###### Scaling Modes

- [let kVTScalingMode_Normal: CFString](/documentation/videotoolbox/kvtscalingmode_normal)
- [let kVTScalingMode_CropSourceToCleanAperture: CFString](/documentation/videotoolbox/kvtscalingmode_cropsourcetocleanaperture)
- [let kVTScalingMode_Letterbox: CFString](/documentation/videotoolbox/kvtscalingmode_letterbox)
- [let kVTScalingMode_Trim: CFString](/documentation/videotoolbox/kvtscalingmode_trim)
- [let kVTPixelTransferPropertyKey_DestinationCleanAperture: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcleanaperture)
- [let kVTPixelTransferPropertyKey_DestinationPixelAspectRatio: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationpixelaspectratio)
- [let kVTPixelTransferPropertyKey_DownsamplingMode: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_downsamplingmode)
- [Downsampling Mode Constants](/documentation/videotoolbox/downsampling-mode-constants)

###### Downsampling Modes

- [let kVTDownsamplingMode_Average: CFString](/documentation/videotoolbox/kvtdownsamplingmode_average)
- [let kVTDownsamplingMode_Decimate: CFString](/documentation/videotoolbox/kvtdownsamplingmode_decimate)
- [let kVTPixelTransferPropertyKey_DestinationColorPrimaries: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationcolorprimaries)
- [let kVTPixelTransferPropertyKey_DestinationTransferFunction: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationtransferfunction)
- [let kVTPixelTransferPropertyKey_DestinationICCProfile: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationiccprofile)
- [let kVTPixelTransferPropertyKey_DestinationYCbCrMatrix: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_destinationycbcrmatrix)
- [let kVTPixelTransferPropertyKey_RealTime: CFString](/documentation/videotoolbox/kvtpixeltransferpropertykey_realtime)

### Getting Properties

- [func VTSessionCopyProperty(VTSession, key: CFString, allocator: CFAllocator?, valueOut: UnsafeMutableRawPointer?) -> OSStatus](/documentation/videotoolbox/vtsessioncopyproperty(_:key:allocator:valueout:))
- [func VTSessionCopySerializableProperties(VTSession, allocator: CFAllocator?, dictionaryOut: UnsafeMutablePointer<CFDictionary?>) -> OSStatus](/documentation/videotoolbox/vtsessioncopyserializableproperties(_:allocator:dictionaryout:))
- [func VTSessionCopySupportedPropertyDictionary(VTSession, supportedPropertyDictionaryOut: UnsafeMutablePointer<CFDictionary?>) -> OSStatus](/documentation/videotoolbox/vtsessioncopysupportedpropertydictionary(_:supportedpropertydictionaryout:))
- [Supported Property Dictionary Constants](/documentation/videotoolbox/supported-dictionary-constants)

#### Properties

- [let kVTPropertyTypeKey: CFString](/documentation/videotoolbox/kvtpropertytypekey)
- [Property Type Constants](/documentation/videotoolbox/property-type-constants)

##### Property Types

- [let kVTPropertyType_Boolean: CFString](/documentation/videotoolbox/kvtpropertytype_boolean)
- [let kVTPropertyType_Enumeration: CFString](/documentation/videotoolbox/kvtpropertytype_enumeration)
- [let kVTPropertyType_Number: CFString](/documentation/videotoolbox/kvtpropertytype_number)
- [let kVTPropertyReadWriteStatusKey: CFString](/documentation/videotoolbox/kvtpropertyreadwritestatuskey)
- [Read/Write Status Constants](/documentation/videotoolbox/read-write-status-constants)

##### Status Constants

- [let kVTPropertyReadWriteStatus_ReadOnly: CFString](/documentation/videotoolbox/kvtpropertyreadwritestatus_readonly)
- [let kVTPropertyReadWriteStatus_ReadWrite: CFString](/documentation/videotoolbox/kvtpropertyreadwritestatus_readwrite)
- [let kVTPropertyShouldBeSerializedKey: CFString](/documentation/videotoolbox/kvtpropertyshouldbeserializedkey)
- [let kVTPropertySupportedValueListKey: CFString](/documentation/videotoolbox/kvtpropertysupportedvaluelistkey)
- [let kVTPropertySupportedValueMaximumKey: CFString](/documentation/videotoolbox/kvtpropertysupportedvaluemaximumkey)
- [let kVTPropertySupportedValueMinimumKey: CFString](/documentation/videotoolbox/kvtpropertysupportedvalueminimumkey)
- [let kVTPropertyDocumentationKey: CFString](/documentation/videotoolbox/kvtpropertydocumentationkey)

### Data Types

- [VTSession](/documentation/videotoolbox/vtsession)

### Enumerations

- [Frame Delay](/documentation/videotoolbox/1441330-frame-delay)

#### Constants

- [var kVTUnlimitedFrameDelayCount: Int](/documentation/videotoolbox/kvtunlimitedframedelaycount)
- [VTInt32Point](/documentation/videotoolbox/vtint32point)

### Creating a Point

- [init()](/documentation/videotoolbox/vtint32point/init())
- [init(x: Int32, y: Int32)](/documentation/videotoolbox/vtint32point/init(x:y:))

### Accessing the Coordinates

- [var x: Int32](/documentation/videotoolbox/vtint32point/x)
- [var y: Int32](/documentation/videotoolbox/vtint32point/y)
- [VTInt32Size](/documentation/videotoolbox/vtint32size)

### Creating a Size

- [init()](/documentation/videotoolbox/vtint32size/init())
- [init(width: Int32, height: Int32)](/documentation/videotoolbox/vtint32size/init(width:height:))

### Accessing the Dimensions

- [var width: Int32](/documentation/videotoolbox/vtint32size/width)
- [var height: Int32](/documentation/videotoolbox/vtint32size/height)

## Errors

- [Error Code Constants](/documentation/videotoolbox/1490398-error-code-constants)

### Errors Codes

- [var kVTAllocationFailedErr: OSStatus](/documentation/videotoolbox/kvtallocationfailederr)
- [var kVTColorCorrectionImageRotationFailedErr: OSStatus](/documentation/videotoolbox/kvtcolorcorrectionimagerotationfailederr)
- [var kVTColorCorrectionPixelTransferFailedErr: OSStatus](/documentation/videotoolbox/kvtcolorcorrectionpixeltransferfailederr)
- [var kVTColorSyncTransformConvertFailedErr: OSStatus](/documentation/videotoolbox/kvtcolorsynctransformconvertfailederr)
- [var kVTCouldNotCreateColorCorrectionDataErr: OSStatus](/documentation/videotoolbox/kvtcouldnotcreatecolorcorrectiondataerr)
- [var kVTCouldNotCreateInstanceErr: OSStatus](/documentation/videotoolbox/kvtcouldnotcreateinstanceerr)
- [var kVTCouldNotFindExtensionErr: OSStatus](/documentation/videotoolbox/kvtcouldnotfindextensionerr)
- [var kVTCouldNotFindTemporalFilterErr: OSStatus](/documentation/videotoolbox/kvtcouldnotfindtemporalfiltererr)
- [var kVTCouldNotFindVideoDecoderErr: OSStatus](/documentation/videotoolbox/kvtcouldnotfindvideodecodererr)
- [var kVTCouldNotFindVideoEncoderErr: OSStatus](/documentation/videotoolbox/kvtcouldnotfindvideoencodererr)
- [var kVTCouldNotOutputTaggedBufferGroupErr: OSStatus](/documentation/videotoolbox/kvtcouldnotoutputtaggedbuffergrouperr)
- [var kVTExtensionConflictErr: OSStatus](/documentation/videotoolbox/kvtextensionconflicterr)
- [var kVTExtensionDisabledErr: OSStatus](/documentation/videotoolbox/kvtextensiondisablederr)
- [var kVTFormatDescriptionChangeNotSupportedErr: OSStatus](/documentation/videotoolbox/kvtformatdescriptionchangenotsupportederr)
- [var kVTFrameSiloInvalidTimeRangeErr: OSStatus](/documentation/videotoolbox/kvtframesiloinvalidtimerangeerr)
- [var kVTFrameSiloInvalidTimeStampErr: OSStatus](/documentation/videotoolbox/kvtframesiloinvalidtimestamperr)
- [var kVTImageRotationNotSupportedErr: OSStatus](/documentation/videotoolbox/kvtimagerotationnotsupportederr)
- [var kVTInsufficientSourceColorDataErr: OSStatus](/documentation/videotoolbox/kvtinsufficientsourcecolordataerr)
- [var kVTInvalidSessionErr: OSStatus](/documentation/videotoolbox/kvtinvalidsessionerr)
- [var kVTMultiPassStorageIdentifierMismatchErr: OSStatus](/documentation/videotoolbox/kvtmultipassstorageidentifiermismatcherr)
- [var kVTMultiPassStorageInvalidErr: OSStatus](/documentation/videotoolbox/kvtmultipassstorageinvaliderr)
- [var kVTParameterErr: OSStatus](/documentation/videotoolbox/kvtparametererr)
- [var kVTPixelRotationNotSupportedErr: OSStatus](/documentation/videotoolbox/kvtpixelrotationnotsupportederr)
- [var kVTPixelTransferNotPermittedErr: OSStatus](/documentation/videotoolbox/kvtpixeltransfernotpermittederr)
- [var kVTPixelTransferNotSupportedErr: OSStatus](/documentation/videotoolbox/kvtpixeltransfernotsupportederr)
- [var kVTPropertyNotSupportedErr: OSStatus](/documentation/videotoolbox/kvtpropertynotsupportederr)
- [var kVTPropertyReadOnlyErr: OSStatus](/documentation/videotoolbox/kvtpropertyreadonlyerr)
- [var kVTSessionMalfunctionErr: OSStatus](/documentation/videotoolbox/kvtsessionmalfunctionerr)
- [var kVTVideoDecoderAuthorizationErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderauthorizationerr)
- [var kVTVideoDecoderBadDataErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderbaddataerr)
- [var kVTVideoDecoderCallbackMessagingErr: OSStatus](/documentation/videotoolbox/kvtvideodecodercallbackmessagingerr)
- [var kVTVideoDecoderMalfunctionErr: OSStatus](/documentation/videotoolbox/kvtvideodecodermalfunctionerr)
- [var kVTVideoDecoderNeedsRosettaErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderneedsrosettaerr)
- [var kVTVideoDecoderNotAvailableNowErr: OSStatus](/documentation/videotoolbox/kvtvideodecodernotavailablenowerr)
- [var kVTVideoDecoderReferenceMissingErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderreferencemissingerr)
- [var kVTVideoDecoderRemovedErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderremovederr)
- [var kVTVideoDecoderUnknownErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderunknownerr)
- [var kVTVideoDecoderUnsupportedDataFormatErr: OSStatus](/documentation/videotoolbox/kvtvideodecoderunsupporteddataformaterr)
- [var kVTVideoEncoderAuthorizationErr: OSStatus](/documentation/videotoolbox/kvtvideoencoderauthorizationerr)
- [var kVTVideoEncoderAutoWhiteBalanceNotLockedErr: OSStatus](/documentation/videotoolbox/kvtvideoencoderautowhitebalancenotlockederr)
- [var kVTVideoEncoderMVHEVCVideoLayerIDsMismatchErr: OSStatus](/documentation/videotoolbox/kvtvideoencodermvhevcvideolayeridsmismatcherr)
- [var kVTVideoEncoderMalfunctionErr: OSStatus](/documentation/videotoolbox/kvtvideoencodermalfunctionerr)
- [var kVTVideoEncoderNeedsRosettaErr: OSStatus](/documentation/videotoolbox/kvtvideoencoderneedsrosettaerr)
- [var kVTVideoEncoderNotAvailableNowErr: OSStatus](/documentation/videotoolbox/kvtvideoencodernotavailablenowerr)

## Reference

- [VideoToolbox Reference](/documentation/videotoolbox/videotoolbox-reference)

### Macros

- [var VT_SUPPORT_COLORSYNC_PIXEL_TRANSFER: Bool](/documentation/videotoolbox/vt_support_colorsync_pixel_transfer)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
