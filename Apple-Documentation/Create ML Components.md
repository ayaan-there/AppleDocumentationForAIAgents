# Create ML Components Documentation

Source: https://sosumi.ai/documentation/createmlcomponents

---
title: Create ML Components
source: https://developer.apple.com/documentation/createmlcomponents
timestamp: 2026-02-13T18:55:58.922Z
---

## Image components

- [Augmenting images to expand your training data](/documentation/createmlcomponents/augmenting-images-to-expand-your-training-data)
- [Creating a multi-label image classifier](/documentation/createmlcomponents/creating-a-multi-label-image-classifier)
- [ImageReader](/documentation/createmlcomponents/imagereader)

### Creating the transformer

- [init()](/documentation/createmlcomponents/imagereader/init())

### Reading an image

- [static func read(url: URL) throws -> CIImage](/documentation/createmlcomponents/imagereader/read(url:))

### Performing the transformation

- [func applied(to: URL, eventHandler: EventHandler?) throws -> CIImage](/documentation/createmlcomponents/imagereader/applied(to:eventhandler:))
- [ImageFeatureExtractor](/documentation/createmlcomponents/imagefeatureextractor)
- [ImageCropper](/documentation/createmlcomponents/imagecropper)

### Creating the transformer

- [init(cropRectangle: CGRect)](/documentation/createmlcomponents/imagecropper/init(croprectangle:))

### Getting the properties

- [var cropRectangle: CGRect](/documentation/createmlcomponents/imagecropper/croprectangle)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) throws -> CIImage](/documentation/createmlcomponents/imagecropper/applied(to:eventhandler:))
- [ImageScaler](/documentation/createmlcomponents/imagescaler)

### Creating a transformer

- [init(targetSize: CGSize)](/documentation/createmlcomponents/imagescaler/init(targetsize:))
- [init(targetHeight: Double)](/documentation/createmlcomponents/imagescaler/init(targetheight:))
- [init(targetWidth: Double)](/documentation/createmlcomponents/imagescaler/init(targetwidth:))

### Getting the target image size

- [var targetSize: CGSize](/documentation/createmlcomponents/imagescaler/targetsize)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) throws -> CIImage](/documentation/createmlcomponents/imagescaler/applied(to:eventhandler:))
- [ImageFeaturePrint](/documentation/createmlcomponents/imagefeatureprint)

### Creating the extractor

- [init(cropAndScale: VNImageCropAndScaleOption, context: CIContext)](/documentation/createmlcomponents/imagefeatureprint/init(cropandscale:context:))
- [init(revision: Int, cropAndScale: VNImageCropAndScaleOption, context: CIContext)](/documentation/createmlcomponents/imagefeatureprint/init(revision:cropandscale:context:))

### Getting the properties

- [let cropAndScale: VNImageCropAndScaleOption](/documentation/createmlcomponents/imagefeatureprint/cropandscale)
- [var revision: Int](/documentation/createmlcomponents/imagefeatureprint/revision)
- [static let latestRevision: Int](/documentation/createmlcomponents/imagefeatureprint/latestrevision)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) async throws -> MLShapedArray<Float>](/documentation/createmlcomponents/imagefeatureprint/applied(to:eventhandler:))
- [ImageBlur](/documentation/createmlcomponents/imageblur)

### Creating an image blur

- [init(radius: Double)](/documentation/createmlcomponents/imageblur/init(radius:))

### Getting the radius

- [var radius: Double](/documentation/createmlcomponents/imageblur/radius)

### Applying the blur

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/imageblur/applied(to:eventhandler:))
- [ImageColorTransformer](/documentation/createmlcomponents/imagecolortransformer)

### Creating a color transformer

- [init(brightness: Float?, contrast: Float?, hue: Float?, saturation: Float?)](/documentation/createmlcomponents/imagecolortransformer/init(brightness:contrast:hue:saturation:))

### Getting the properties

- [var brightness: Float?](/documentation/createmlcomponents/imagecolortransformer/brightness)
- [var contrast: Float?](/documentation/createmlcomponents/imagecolortransformer/contrast)
- [var hue: Float?](/documentation/createmlcomponents/imagecolortransformer/hue)
- [var saturation: Float?](/documentation/createmlcomponents/imagecolortransformer/saturation)

### Applying the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/imagecolortransformer/applied(to:eventhandler:))
- [ImageExposureAdjuster](/documentation/createmlcomponents/imageexposureadjuster)

### Creating an exposure adjuster

- [init(amount: Double)](/documentation/createmlcomponents/imageexposureadjuster/init(amount:))

### Getting the amount

- [var amount: Double](/documentation/createmlcomponents/imageexposureadjuster/amount)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/imageexposureadjuster/applied(to:eventhandler:))
- [ImageFlipper](/documentation/createmlcomponents/imageflipper)

### Creating a transformer

- [init(orientation: ImageFlipper.Orientation)](/documentation/createmlcomponents/imageflipper/init(orientation:))
- [ImageFlipper.Orientation](/documentation/createmlcomponents/imageflipper/orientation-swift.enum)

#### Image orientations

- [case horizontal](/documentation/createmlcomponents/imageflipper/orientation-swift.enum/horizontal)
- [case vertical](/documentation/createmlcomponents/imageflipper/orientation-swift.enum/vertical)

### Getting the orientation

- [var orientation: ImageFlipper.Orientation](/documentation/createmlcomponents/imageflipper/orientation-swift.property)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/imageflipper/applied(to:eventhandler:))
- [ImageRotator](/documentation/createmlcomponents/imagerotator)

### Creating the transformer

- [init(angle: Double)](/documentation/createmlcomponents/imagerotator/init(angle:))

### Getting the angle

- [var angle: Double](/documentation/createmlcomponents/imagerotator/angle)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/imagerotator/applied(to:eventhandler:))
- [RandomImageNoiseGenerator](/documentation/createmlcomponents/randomimagenoisegenerator)

### Creating a noise generator

- [init(intensity: Double)](/documentation/createmlcomponents/randomimagenoisegenerator/init(intensity:))

### Getting the intensity

- [var intensity: Double](/documentation/createmlcomponents/randomimagenoisegenerator/intensity)

### Performing the transformation

- [func applied(to: CIImage, eventHandler: EventHandler?) -> CIImage](/documentation/createmlcomponents/randomimagenoisegenerator/applied(to:eventhandler:))
- [MLModelImageFeatureExtractor](/documentation/createmlcomponents/mlmodelimagefeatureextractor)

### Creating the extractor

- [init(model: MLModel, inputName: String, outputName: String, context: CIContext) throws](/documentation/createmlcomponents/mlmodelimagefeatureextractor/init(model:inputname:outputname:context:))
- [init(contentsOf: URL, configuration: MLModelConfiguration, inputName: String, outputName: String, context: CIContext) async throws](/documentation/createmlcomponents/mlmodelimagefeatureextractor/init(contentsof:configuration:inputname:outputname:context:))

### Getting the properties

- [let inputName: String](/documentation/createmlcomponents/mlmodelimagefeatureextractor/inputname)
- [let model: MLModel](/documentation/createmlcomponents/mlmodelimagefeatureextractor/model)
- [let outputName: String](/documentation/createmlcomponents/mlmodelimagefeatureextractor/outputname)

### Applying

- [func applied(to: CIImage, eventHandler: EventHandler?) async throws -> MLShapedArray<Float>](/documentation/createmlcomponents/mlmodelimagefeatureextractor/applied(to:eventhandler:))
- [MLModelImageFeatureExtractor.Error](/documentation/createmlcomponents/mlmodelimagefeatureextractor/error)

#### Analyzing the error

- [case invalidInput(String)](/documentation/createmlcomponents/mlmodelimagefeatureextractor/error/invalidinput(_:))
- [case invalidOutput(String)](/documentation/createmlcomponents/mlmodelimagefeatureextractor/error/invalidoutput(_:))

#### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/mlmodelimagefeatureextractor/error/debugdescription)

## Pose components

- [Counting human body action repetitions in a live video feed](/documentation/createmlcomponents/counting-human-body-action-repetitions-in-a-live-video-feed)
- [Pose](/documentation/createmlcomponents/pose)

### Creating a pose

- [init(VNRecognizedPointsObservation) throws](/documentation/createmlcomponents/pose/init(_:))
- [init(from: [JointKey : JointPoint])](/documentation/createmlcomponents/pose/init(from:)-8rvl5)

### Getting the key points

- [var keypoints: [JointKey : JointPoint]](/documentation/createmlcomponents/pose/keypoints)

### Computing the bounding box

- [func boundingBoxArea(confidenceThreshold: Float) -> Float](/documentation/createmlcomponents/pose/boundingboxarea(confidencethreshold:))

### Default Implementations

- [Decodable Implementations](/documentation/createmlcomponents/pose/decodable-implementations)

#### Initializers

- [init(from:)](/documentation/createmlcomponents/pose/init(from:))
- [init(from: any Decoder) throws](/documentation/createmlcomponents/pose/init(from:)-9ijwh)
- [Encodable Implementations](/documentation/createmlcomponents/pose/encodable-implementations)

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/createmlcomponents/pose/encode(to:))
- [JointKey](/documentation/createmlcomponents/jointkey)

### Getting elbow properties

- [static let leftElbow: JointKey](/documentation/createmlcomponents/jointkey/leftelbow)
- [static let rightElbow: JointKey](/documentation/createmlcomponents/jointkey/rightelbow)

### Getting head properties

- [static let leftEye: JointKey](/documentation/createmlcomponents/jointkey/lefteye)
- [static let rightEye: JointKey](/documentation/createmlcomponents/jointkey/righteye)
- [static let leftEar: JointKey](/documentation/createmlcomponents/jointkey/leftear)
- [static let rightEar: JointKey](/documentation/createmlcomponents/jointkey/rightear)
- [static let nose: JointKey](/documentation/createmlcomponents/jointkey/nose)

### Getting index finger properties

- [static let indexDIP: JointKey](/documentation/createmlcomponents/jointkey/indexdip)
- [static let indexMCP: JointKey](/documentation/createmlcomponents/jointkey/indexmcp)
- [static let indexPIP: JointKey](/documentation/createmlcomponents/jointkey/indexpip)
- [static let indexTip: JointKey](/documentation/createmlcomponents/jointkey/indextip)

### Getting little finger properties

- [static let littleDIP: JointKey](/documentation/createmlcomponents/jointkey/littledip)
- [static let littleMCP: JointKey](/documentation/createmlcomponents/jointkey/littlemcp)
- [static let littlePIP: JointKey](/documentation/createmlcomponents/jointkey/littlepip)
- [static let littleTip: JointKey](/documentation/createmlcomponents/jointkey/littletip)

### Getting middle finger properties

- [static let middleDIP: JointKey](/documentation/createmlcomponents/jointkey/middledip)
- [static let middleMCP: JointKey](/documentation/createmlcomponents/jointkey/middlemcp)
- [static let middlePIP: JointKey](/documentation/createmlcomponents/jointkey/middlepip)
- [static let middleTip: JointKey](/documentation/createmlcomponents/jointkey/middletip)

### Getting ring finger properties

- [static let ringDIP: JointKey](/documentation/createmlcomponents/jointkey/ringdip)
- [static let ringMCP: JointKey](/documentation/createmlcomponents/jointkey/ringmcp)
- [static let ringPIP: JointKey](/documentation/createmlcomponents/jointkey/ringpip)
- [static let ringTip: JointKey](/documentation/createmlcomponents/jointkey/ringtip)

### Getting thumb properties

- [static let thumbCMC: JointKey](/documentation/createmlcomponents/jointkey/thumbcmc)
- [static let thumbIP: JointKey](/documentation/createmlcomponents/jointkey/thumbip)
- [static let thumbMP: JointKey](/documentation/createmlcomponents/jointkey/thumbmp)
- [static let thumbTip: JointKey](/documentation/createmlcomponents/jointkey/thumbtip)

### Getting wrist properties

- [static let leftWrist: JointKey](/documentation/createmlcomponents/jointkey/leftwrist)
- [static let rightWrist: JointKey](/documentation/createmlcomponents/jointkey/rightwrist)
- [static let wrist: JointKey](/documentation/createmlcomponents/jointkey/wrist)

### Getting neck and shoulder properties

- [static let neck: JointKey](/documentation/createmlcomponents/jointkey/neck)
- [static let leftShoulder: JointKey](/documentation/createmlcomponents/jointkey/leftshoulder)
- [static let rightShoulder: JointKey](/documentation/createmlcomponents/jointkey/rightshoulder)

### Getting hip, knee, and ankle properties

- [static let leftHip: JointKey](/documentation/createmlcomponents/jointkey/lefthip)
- [static let leftKnee: JointKey](/documentation/createmlcomponents/jointkey/leftknee)
- [static let rightHip: JointKey](/documentation/createmlcomponents/jointkey/righthip)
- [static let rightKnee: JointKey](/documentation/createmlcomponents/jointkey/rightknee)
- [static let leftAnkle: JointKey](/documentation/createmlcomponents/jointkey/leftankle)
- [static let rightAnkle: JointKey](/documentation/createmlcomponents/jointkey/rightankle)

### Getting root and raw Properties

- [static let root: JointKey](/documentation/createmlcomponents/jointkey/root)
- [JointPoint](/documentation/createmlcomponents/jointpoint)

### Creating a joint point

- [init(JointKey, location: CGPoint, confidence: Float)](/documentation/createmlcomponents/jointpoint/init(_:location:confidence:))

### Getting the detection confidence

- [var confidence: Float](/documentation/createmlcomponents/jointpoint/confidence)

### Getting the key name

- [let key: JointKey](/documentation/createmlcomponents/jointpoint/key)

### Getting the joint location

- [var location: CGPoint](/documentation/createmlcomponents/jointpoint/location)
- [PoseSelector](/documentation/createmlcomponents/poseselector)

### Creating a selector

- [init()](/documentation/createmlcomponents/poseselector/init())
- [init(strategy: PoseSelectionStrategy)](/documentation/createmlcomponents/poseselector/init(strategy:))
- [init(strategy: PoseSelectionStrategy, confidenceThreshold: Float)](/documentation/createmlcomponents/poseselector/init(strategy:confidencethreshold:))

### Getting the properties

- [var confidenceThreshold: Float](/documentation/createmlcomponents/poseselector/confidencethreshold)
- [var strategy: PoseSelectionStrategy](/documentation/createmlcomponents/poseselector/strategy)

### Performing the transformation

- [func applied(to: [Pose], eventHandler: EventHandler?) -> Pose](/documentation/createmlcomponents/poseselector/applied(to:eventhandler:))
- [PoseSelectionStrategy](/documentation/createmlcomponents/poseselectionstrategy)

### Selection strategies

- [case maximumBoundingBoxArea](/documentation/createmlcomponents/poseselectionstrategy/maximumboundingboxarea)
- [case highestJointLocation](/documentation/createmlcomponents/poseselectionstrategy/highestjointlocation)
- [case leftmostJointLocation](/documentation/createmlcomponents/poseselectionstrategy/leftmostjointlocation)
- [case lowestJointLocation](/documentation/createmlcomponents/poseselectionstrategy/lowestjointlocation)
- [case rightmostJointLocation](/documentation/createmlcomponents/poseselectionstrategy/rightmostjointlocation)
- [JointsSelector](/documentation/createmlcomponents/jointsselector)

### Creating a selector

- [init(ignoredJoints: [JointKey])](/documentation/createmlcomponents/jointsselector/init(ignoredjoints:))
- [init(selectedJoints: [JointKey])](/documentation/createmlcomponents/jointsselector/init(selectedjoints:))

### Getting the properties

- [var ignoredJoints: [JointKey]?](/documentation/createmlcomponents/jointsselector/ignoredjoints)
- [var selectedJoints: [JointKey]?](/documentation/createmlcomponents/jointsselector/selectedjoints)

### Performing the selector

- [func applied(to: Pose, eventHandler: EventHandler?) -> Pose](/documentation/createmlcomponents/jointsselector/applied(to:eventhandler:))
- [HumanBodyPoseExtractor](/documentation/createmlcomponents/humanbodyposeextractor)

### Creating the extractor

- [init()](/documentation/createmlcomponents/humanbodyposeextractor/init())

### Extracting the body pose

- [func applied(to: CIImage, eventHandler: EventHandler?) async throws -> [Pose]](/documentation/createmlcomponents/humanbodyposeextractor/applied(to:eventhandler:))
- [HumanHandPoseExtractor](/documentation/createmlcomponents/humanhandposeextractor)

### Creating the extractor

- [init()](/documentation/createmlcomponents/humanhandposeextractor/init())

### Extracting the hand pose

- [func applied(to: CIImage, eventHandler: EventHandler?) async throws -> [Pose]](/documentation/createmlcomponents/humanhandposeextractor/applied(to:eventhandler:))
- [HumanBodyActionCounter](/documentation/createmlcomponents/humanbodyactioncounter)

### Creating a transformer

- [init()](/documentation/createmlcomponents/humanbodyactioncounter/init())

### Performing the transformation

- [func applied<S>(to: S, eventHandler: EventHandler?) async throws -> HumanBodyActionCounter.OutputSequence](/documentation/createmlcomponents/humanbodyactioncounter/applied(to:eventhandler:))
- [HumanBodyActionCounter.CumulativeSumSequence](/documentation/createmlcomponents/humanbodyactioncounter/cumulativesumsequence)

#### Getting the count

- [var count: Int?](/documentation/createmlcomponents/humanbodyactioncounter/cumulativesumsequence/count)

#### Creating an iterator

- [func makeAsyncIterator() -> HumanBodyActionCounter.CumulativeSumSequence.Iterator](/documentation/createmlcomponents/humanbodyactioncounter/cumulativesumsequence/makeasynciterator())
- [HumanBodyActionCounter.CumulativeSumSequence.Iterator](/documentation/createmlcomponents/humanbodyactioncounter/cumulativesumsequence/iterator)

##### Getting the next element

- [func next() async throws -> TemporalFeature<Float>?](/documentation/createmlcomponents/humanbodyactioncounter/cumulativesumsequence/iterator/next())
- [HumanBodyActionPeriodPredictor](/documentation/createmlcomponents/humanbodyactionperiodpredictor)

### Creating a transformer

- [init()](/documentation/createmlcomponents/humanbodyactionperiodpredictor/init())

### Performing the transformation

- [func applied(to: [Pose], eventHandler: EventHandler?) async throws -> [HumanBodyActionPeriodPredictor.Prediction]](/documentation/createmlcomponents/humanbodyactionperiodpredictor/applied(to:eventhandler:))
- [HumanBodyActionPeriodPredictor.Prediction](/documentation/createmlcomponents/humanbodyactionperiodpredictor/prediction)

#### Creating a prediction

- [init(period: Float, periodicity: Float)](/documentation/createmlcomponents/humanbodyactionperiodpredictor/prediction/init(period:periodicity:))

#### Getting the properties

- [var period: Float](/documentation/createmlcomponents/humanbodyactionperiodpredictor/prediction/period)
- [var periodicity: Float](/documentation/createmlcomponents/humanbodyactionperiodpredictor/prediction/periodicity)

## Audio components

- [AudioReader](/documentation/createmlcomponents/audioreader)

### Creating an audio reader

- [init(configuration: AudioReader.Configuration)](/documentation/createmlcomponents/audioreader/init(configuration:))

### Getting the properties

- [var configuration: AudioReader.Configuration](/documentation/createmlcomponents/audioreader/configuration-swift.property)

### Managing buffers

- [AudioReader.AsyncBuffers](/documentation/createmlcomponents/audioreader/asyncbuffers)

#### Getting the count

- [let count: Int?](/documentation/createmlcomponents/audioreader/asyncbuffers/count)

#### Getting the url

- [let url: URL](/documentation/createmlcomponents/audioreader/asyncbuffers/url)

#### Creating an iterator

- [func makeAsyncIterator() -> AudioReader.AsyncBuffers.Iterator](/documentation/createmlcomponents/audioreader/asyncbuffers/makeasynciterator())
- [AudioReader.AsyncBuffers.Iterator](/documentation/createmlcomponents/audioreader/asyncbuffers/iterator)
- [AudioReader.Configuration](/documentation/createmlcomponents/audioreader/configuration-swift.struct)

#### Creating a configuration

- [init()](/documentation/createmlcomponents/audioreader/configuration-swift.struct/init())
- [init(frameCount: Int)](/documentation/createmlcomponents/audioreader/configuration-swift.struct/init(framecount:))

#### Getting the frame count

- [var frameCount: Int](/documentation/createmlcomponents/audioreader/configuration-swift.struct/framecount)
- [AudioReader.MicrophoneAsyncBuffers](/documentation/createmlcomponents/audioreader/microphoneasyncbuffers)

#### Getting the count

- [var count: Int?](/documentation/createmlcomponents/audioreader/microphoneasyncbuffers/count)

#### Creating an iterator

- [func makeAsyncIterator() -> AudioReader.MicrophoneAsyncBuffers.Iterator](/documentation/createmlcomponents/audioreader/microphoneasyncbuffers/makeasynciterator())
- [AudioReader.MicrophoneAsyncBuffers.Iterator](/documentation/createmlcomponents/audioreader/microphoneasyncbuffers/iterator)

##### Getting the next element

- [func next() async throws -> TemporalFeature<AudioReader.MicrophoneAsyncBuffers.Feature>?](/documentation/createmlcomponents/audioreader/microphoneasyncbuffers/iterator/next())

### Reading audio

- [static func read(contentsOf: URL, configuration: AudioReader.Configuration) throws -> AudioReader.AsyncBuffers](/documentation/createmlcomponents/audioreader/read(contentsof:configuration:))
- [static read(_:configuration:)](/documentation/createmlcomponents/audioreader/read(_:configuration:))
- [static func readMicrophone(configuration: AudioReader.Configuration) async throws -> AudioReader.MicrophoneAsyncBuffers](/documentation/createmlcomponents/audioreader/readmicrophone(configuration:))

### Applying

- [func applied(to: URL, eventHandler: EventHandler?) throws -> AudioReader.AsyncBuffers](/documentation/createmlcomponents/audioreader/applied(to:eventhandler:))
- [AudioFeaturePrint](/documentation/createmlcomponents/audiofeatureprint)

### Creating a transformer

- [init(windowDuration: TimeInterval, overlapFactor: Double)](/documentation/createmlcomponents/audiofeatureprint/init(windowduration:overlapfactor:))

### Getting the properties

- [let overlapFactor: Double](/documentation/createmlcomponents/audiofeatureprint/overlapfactor)
- [let windowDuration: TimeInterval](/documentation/createmlcomponents/audiofeatureprint/windowduration)

### Performing the transformation

- [func applied<S>(to: S, eventHandler: EventHandler?) throws -> AudioFeaturePrint.FeatureSequence](/documentation/createmlcomponents/audiofeatureprint/applied(to:eventhandler:))
- [AudioFeaturePrint.FeatureSequence](/documentation/createmlcomponents/audiofeatureprint/featuresequence)

#### Getting the count

- [var count: Int?](/documentation/createmlcomponents/audiofeatureprint/featuresequence/count)

#### Creating an iterator

- [func makeAsyncIterator() -> AudioFeaturePrint.FeatureSequence.AsyncIterator](/documentation/createmlcomponents/audiofeatureprint/featuresequence/makeasynciterator())
- [AudioFeaturePrint.FeatureSequence.Iterator](/documentation/createmlcomponents/audiofeatureprint/featuresequence/iterator)
- [AudioConvertingTransformer](/documentation/createmlcomponents/audioconvertingtransformer)

### Creating the transformer

- [init(targetFormat: AVAudioFormat)](/documentation/createmlcomponents/audioconvertingtransformer/init(targetformat:))

### Getting the properties

- [let targetFormat: AVAudioFormat](/documentation/createmlcomponents/audioconvertingtransformer/targetformat)

### Applying the transformer

- [func applied(to: AVAudioPCMBuffer, eventHandler: EventHandler?) throws -> AVAudioPCMBuffer](/documentation/createmlcomponents/audioconvertingtransformer/applied(to:eventhandler:))

## Time-based components

- [Creating a time-series classifier](/documentation/createmlcomponents/creating-a-time-series-classifier)
- [Creating a time-series forecaster](/documentation/createmlcomponents/creating-a-time-series-forecaster)
- [DateFeatures](/documentation/createmlcomponents/datefeatures)

### Features

- [static let day: DateFeatures](/documentation/createmlcomponents/datefeatures/day)
- [static let dayOfYear: DateFeatures](/documentation/createmlcomponents/datefeatures/dayofyear)
- [static let hour: DateFeatures](/documentation/createmlcomponents/datefeatures/hour)
- [static let minute: DateFeatures](/documentation/createmlcomponents/datefeatures/minute)
- [static let month: DateFeatures](/documentation/createmlcomponents/datefeatures/month)
- [static let second: DateFeatures](/documentation/createmlcomponents/datefeatures/second)
- [static let weekOfMonth: DateFeatures](/documentation/createmlcomponents/datefeatures/weekofmonth)
- [static let weekOfYear: DateFeatures](/documentation/createmlcomponents/datefeatures/weekofyear)
- [static let weekday: DateFeatures](/documentation/createmlcomponents/datefeatures/weekday)

### Creating a date feature type

- [init(rawValue: Int)](/documentation/createmlcomponents/datefeatures/init(rawvalue:))
- [DateFeatureExtractor](/documentation/createmlcomponents/datefeatureextractor)

### Creating a data feature extractor

- [init(features: DateFeatures, calendar: Calendar)](/documentation/createmlcomponents/datefeatureextractor/init(features:calendar:))

### Applying a data feature extractor

- [func applied(to: Date, eventHandler: EventHandler?) -> [Scalar]](/documentation/createmlcomponents/datefeatureextractor/applied(to:eventhandler:))

### Inspecting a data feature extractor

- [let calendar: Calendar](/documentation/createmlcomponents/datefeatureextractor/calendar)
- [let features: DateFeatures](/documentation/createmlcomponents/datefeatureextractor/features)
- [LinearTimeSeriesForecaster](/documentation/createmlcomponents/lineartimeseriesforecaster)

### Creating a linear time series forecaster

- [init(configuration: LinearTimeSeriesForecaster<Scalar>.Configuration)](/documentation/createmlcomponents/lineartimeseriesforecaster/init(configuration:))

### Inspecting a linear time series forecaster

- [let configuration: LinearTimeSeriesForecaster<Scalar>.Configuration](/documentation/createmlcomponents/lineartimeseriesforecaster/configuration-swift.property)
- [var forecastWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/forecastwindowsize)
- [var inputWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/inputwindowsize)

### Updating and fitting

- [func update(inout LinearTimeSeriesForecaster<Scalar>.Transformer, with: AnnotatedBatch<Scalar>) async throws -> Scalar](/documentation/createmlcomponents/lineartimeseriesforecaster/update(_:with:))
- [func update(inout LinearTimeSeriesForecaster<Scalar>.Model, withWindows: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/lineartimeseriesforecaster/update(_:withwindows:eventhandler:))
- [func fitted(to: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws -> LinearTimeSeriesForecaster<Scalar>.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/fitted(to:eventhandler:))
- [func fitted(to: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, validateOn: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws -> LinearTimeSeriesForecaster<Scalar>.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/fitted(to:validateon:eventhandler:))
- [func fitted(toWindows: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws -> LinearTimeSeriesForecaster<Scalar>.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/fitted(towindows:eventhandler:))
- [func fitted(toWindows: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, validateOn: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws -> LinearTimeSeriesForecaster<Scalar>.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/fitted(towindows:validateon:eventhandler:))

### Supporting types

- [LinearTimeSeriesForecaster.Configuration](/documentation/createmlcomponents/lineartimeseriesforecaster/configuration-swift.typealias)
- [LinearTimeSeriesForecaster.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/model)

#### Inspecting the model

- [var annotationSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/model/annotationsize)
- [var bias: MLShapedArray<Scalar>?](/documentation/createmlcomponents/lineartimeseriesforecaster/model/bias)
- [var featureSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/model/featuresize)
- [var forecastWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/model/forecastwindowsize)
- [var inputWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/model/inputwindowsize)
- [var stride: Int](/documentation/createmlcomponents/lineartimeseriesforecaster/model/stride)
- [var weight: MLShapedArray<Scalar>](/documentation/createmlcomponents/lineartimeseriesforecaster/model/weight)

#### Applying the model

- [func applied(to:eventHandler:)](/documentation/createmlcomponents/lineartimeseriesforecaster/model/applied(to:eventhandler:))
- [func applied(toWindow: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> MLShapedArray<Scalar>](/documentation/createmlcomponents/lineartimeseriesforecaster/model/applied(towindow:eventhandler:))

#### Exporting the model

- [func export(to: URL) throws](/documentation/createmlcomponents/lineartimeseriesforecaster/model/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/lineartimeseriesforecaster/model/export(to:metadata:))

#### Default Implementations

- [TemporalTransformer Implementations](/documentation/createmlcomponents/lineartimeseriesforecaster/model/temporaltransformer-implementations)

##### Instance Methods

- [func applied(to: some TemporalSequence<MLShapedArray<Scalar>>, eventHandler: EventHandler?) async throws -> AnyTemporalSequence<MLShapedArray<Scalar>>](/documentation/createmlcomponents/lineartimeseriesforecaster/model/applied(to:eventhandler:)-3h2wx)

### Default Implementations

- [SupervisedEstimator Implementations](/documentation/createmlcomponents/lineartimeseriesforecaster/supervisedestimator-implementations)

#### Instance Methods

- [func decode(from: inout any EstimatorDecoder) throws -> LinearTimeSeriesForecaster<Scalar>.Transformer](/documentation/createmlcomponents/lineartimeseriesforecaster/decode(from:))
- [func encode(LinearTimeSeriesForecaster<Scalar>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/lineartimeseriesforecaster/encode(_:to:))
- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/lineartimeseriesforecaster/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> LinearTimeSeriesForecaster<Scalar>.Transformer](/documentation/createmlcomponents/lineartimeseriesforecaster/decodewithoptimizer(from:))
- [func encodeWithOptimizer(LinearTimeSeriesForecaster<Scalar>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/lineartimeseriesforecaster/encodewithoptimizer(_:to:))
- [func makeTransformer() -> LinearTimeSeriesForecaster<Scalar>.Model](/documentation/createmlcomponents/lineartimeseriesforecaster/maketransformer())
- [func update(inout LinearTimeSeriesForecaster<Scalar>.Model, with: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/lineartimeseriesforecaster/update(_:with:eventhandler:))
- [LinearTimeSeriesForecasterConfiguration](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration)

### Creating a linear time series forecasater configuration

- [init(inputWindowSize: Int, forecastWindowSize: Int)](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/init(inputwindowsize:forecastwindowsize:))

### Inspecting a linear time series forecasater configuration

- [var batchSize: Int](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/batchsize)
- [var earlyStoppingIterationCount: Int](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/earlystoppingiterationcount)
- [var earlyStoppingTolerance: Float](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/earlystoppingtolerance)
- [var forecastWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/forecastwindowsize)
- [var inputWindowSize: Int](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/inputwindowsize)
- [var learningRate: Float](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/learningrate)
- [var maximumIterationCount: Int](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/maximumiterationcount)
- [var randomSeed: Int?](/documentation/createmlcomponents/lineartimeseriesforecasterconfiguration/randomseed)
- [TimeSeriesForecasterBatches](/documentation/createmlcomponents/timeseriesforecasterbatches)

### Creating a time series forecaster batch

- [init(features: MLShapedArray<Scalar>, annotations: MLShapedArray<Scalar>, batchSize: Int, inputWindowSize: Int, forecastWindowSize: Int, shufflesBatches: Bool) throws](/documentation/createmlcomponents/timeseriesforecasterbatches/init(features:annotations:batchsize:inputwindowsize:forecastwindowsize:shufflesbatches:))

### Inspecting a time series forecaster batch

- [let annotations: MLShapedArray<Scalar>](/documentation/createmlcomponents/timeseriesforecasterbatches/annotations)
- [let batchSize: Int](/documentation/createmlcomponents/timeseriesforecasterbatches/batchsize)
- [let features: MLShapedArray<Scalar>](/documentation/createmlcomponents/timeseriesforecasterbatches/features)
- [let forecastWindowSize: Int](/documentation/createmlcomponents/timeseriesforecasterbatches/forecastwindowsize)
- [let inputWindowSize: Int](/documentation/createmlcomponents/timeseriesforecasterbatches/inputwindowsize)
- [var shufflesBatches: Bool](/documentation/createmlcomponents/timeseriesforecasterbatches/shufflesbatches)

### Default Implementations

- [Sequence Implementations](/documentation/createmlcomponents/timeseriesforecasterbatches/sequence-implementations)

#### Structures

- [TimeSeriesForecasterBatches.Iterator](/documentation/createmlcomponents/timeseriesforecasterbatches/iterator)
- [TimeSeriesForecasterAnnotatedWindows](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows)

### Creating a time series forecaster annotated window

- [init(features: MLShapedArray<Scalar>, annotations: MLShapedArray<Scalar>, inputWindowSize: Int, forecastWindowSize: Int, stride: Int, shufflesElements: Bool) throws](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/init(features:annotations:inputwindowsize:forecastwindowsize:stride:shuffleselements:))

### Inspecting a time series forecaster annotated window

- [let annotations: MLShapedArray<Scalar>](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/annotations)
- [let features: MLShapedArray<Scalar>](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/features)
- [let forecastWindowSize: Int](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/forecastwindowsize)
- [let inputWindowSize: Int](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/inputwindowsize)
- [var shufflesElements: Bool](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/shuffleselements)
- [var stride: Int](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/stride)

### Default Implementations

- [Sequence Implementations](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/sequence-implementations)

#### Structures

- [TimeSeriesForecasterAnnotatedWindows.Iterator](/documentation/createmlcomponents/timeseriesforecasterannotatedwindows/iterator)
- [TemporalFeature](/documentation/createmlcomponents/temporalfeature)

### Creating a temporal feature

- [init(id: TemporalSegmentIdentifier, feature: Feature)](/documentation/createmlcomponents/temporalfeature/init(id:feature:))

### Getting the properties

- [var feature: Feature](/documentation/createmlcomponents/temporalfeature/feature)
- [var id: TemporalSegmentIdentifier](/documentation/createmlcomponents/temporalfeature/id)
- [TemporalSequence](/documentation/createmlcomponents/temporalsequence)

### Getting the sequence count

- [var count: Int?](/documentation/createmlcomponents/temporalsequence/count)

### Associating the types

- [Feature](/documentation/createmlcomponents/temporalsequence/feature)
- [TemporalSegmentIdentifier](/documentation/createmlcomponents/temporalsegmentidentifier)

### Creating a segment identifier

- [init(source: String, range: Range<Int>, timescale: Int)](/documentation/createmlcomponents/temporalsegmentidentifier/init(source:range:timescale:))

### Getting the properties

- [var durationInSeconds: TimeInterval](/documentation/createmlcomponents/temporalsegmentidentifier/durationinseconds)
- [var range: Range<Int>](/documentation/createmlcomponents/temporalsegmentidentifier/range)
- [var rangeInSeconds: Range<TimeInterval>](/documentation/createmlcomponents/temporalsegmentidentifier/rangeinseconds)
- [var source: String](/documentation/createmlcomponents/temporalsegmentidentifier/source)
- [var timescale: Int](/documentation/createmlcomponents/temporalsegmentidentifier/timescale)
- [SlidingWindows](/documentation/createmlcomponents/slidingwindows)

### Creating a sliding window

- [init(input: MLShapedArray<Scalar>, length: Int, stride: Int) throws](/documentation/createmlcomponents/slidingwindows/init(input:length:stride:))

### Inspecting the sliding window

- [var endIndex: Int](/documentation/createmlcomponents/slidingwindows/endindex)
- [let input: MLShapedArray<Scalar>](/documentation/createmlcomponents/slidingwindows/input)
- [let length: Int](/documentation/createmlcomponents/slidingwindows/length)
- [var startIndex: Int](/documentation/createmlcomponents/slidingwindows/startindex)
- [let stride: Int](/documentation/createmlcomponents/slidingwindows/stride)

### Getting the index

- [func index(Int, offsetBy: Int) -> Int](/documentation/createmlcomponents/slidingwindows/index(_:offsetby:))
- [func index(after: Int) -> Int](/documentation/createmlcomponents/slidingwindows/index(after:))
- [func index(before: Int) -> Int](/documentation/createmlcomponents/slidingwindows/index(before:))

### Getting the subscript

- [subscript(_:)](/documentation/createmlcomponents/slidingwindows/subscript(_:))
- [SlidingWindowTransformer](/documentation/createmlcomponents/slidingwindowtransformer)

### Creating a transformer

- [init(stride: Int, length: Int)](/documentation/createmlcomponents/slidingwindowtransformer/init(stride:length:))

### Getting the properties

- [let length: Int](/documentation/createmlcomponents/slidingwindowtransformer/length)
- [let stride: Int](/documentation/createmlcomponents/slidingwindowtransformer/stride)

### Performing the transformation

- [func applied<S>(to: S, eventHandler: EventHandler?) throws -> SlidingWindowTransformer<Input>.WindowSequence](/documentation/createmlcomponents/slidingwindowtransformer/applied(to:eventhandler:))
- [SlidingWindowTransformer.WindowSequence](/documentation/createmlcomponents/slidingwindowtransformer/windowsequence)

#### Getting the count

- [var count: Int?](/documentation/createmlcomponents/slidingwindowtransformer/windowsequence/count)

#### Creating an iterator

- [SlidingWindowTransformer.WindowSequence.Iterator](/documentation/createmlcomponents/slidingwindowtransformer/windowsequence/iterator)
- [Downsampler](/documentation/createmlcomponents/downsampler)

### Creating a transformer

- [init(factor: Int)](/documentation/createmlcomponents/downsampler/init(factor:))

### Getting the sample factor

- [let factor: Int](/documentation/createmlcomponents/downsampler/factor)

### Performing the transformation

- [func applied<S>(to: S, eventHandler: EventHandler?) throws -> Downsampler<Input>.DownStreamSequence](/documentation/createmlcomponents/downsampler/applied(to:eventhandler:))
- [Downsampler.DownStreamSequence](/documentation/createmlcomponents/downsampler/downstreamsequence)

#### Getting the count

- [var count: Int?](/documentation/createmlcomponents/downsampler/downstreamsequence/count)

#### Creating an iterator

- [Downsampler.DownStreamSequence.Iterator](/documentation/createmlcomponents/downsampler/downstreamsequence/iterator)
- [VideoReader](/documentation/createmlcomponents/videoreader)

### Creating the reader

- [init()](/documentation/createmlcomponents/videoreader/init())

### Reading

- [static read(_:)](/documentation/createmlcomponents/videoreader/read(_:))
- [static func readCamera(configuration: VideoReader.CameraConfiguration) async throws -> VideoReader.CameraAsyncBuffers](/documentation/createmlcomponents/videoreader/readcamera(configuration:))
- [static func read(contentsOf: URL) async throws -> VideoReader.AsyncFrames](/documentation/createmlcomponents/videoreader/read(contentsof:))
- [VideoReader.AsyncFrames](/documentation/createmlcomponents/videoreader/asyncframes)

#### Getting the properties

- [var count: Int?](/documentation/createmlcomponents/videoreader/asyncframes/count)
- [let frameSize: CGSize](/documentation/createmlcomponents/videoreader/asyncframes/framesize)
- [let nominalFrameRate: Float](/documentation/createmlcomponents/videoreader/asyncframes/nominalframerate)
- [let timescale: CMTimeScale](/documentation/createmlcomponents/videoreader/asyncframes/timescale)
- [let url: URL](/documentation/createmlcomponents/videoreader/asyncframes/url)
- [let videoDuration: CMTime](/documentation/createmlcomponents/videoreader/asyncframes/videoduration)

#### Creating an iterator

- [func makeAsyncIterator() -> VideoReader.AsyncFrames.Iterator](/documentation/createmlcomponents/videoreader/asyncframes/makeasynciterator())
- [VideoReader.AsyncFrames.Iterator](/documentation/createmlcomponents/videoreader/asyncframes/iterator)
- [VideoReader.CameraAsyncBuffers](/documentation/createmlcomponents/videoreader/cameraasyncbuffers)

#### Getting the capture session

- [var captureSession: AVCaptureSession](/documentation/createmlcomponents/videoreader/cameraasyncbuffers/capturesession)

#### Getting the buffer count

- [var count: Int?](/documentation/createmlcomponents/videoreader/cameraasyncbuffers/count)

#### Creating an iterator

- [func makeAsyncIterator() -> VideoReader.CameraAsyncBuffers.Iterator](/documentation/createmlcomponents/videoreader/cameraasyncbuffers/makeasynciterator())
- [VideoReader.CameraAsyncBuffers.Iterator](/documentation/createmlcomponents/videoreader/cameraasyncbuffers/iterator)

##### Getting the next element

- [func next() async throws -> TemporalFeature<CIImage>?](/documentation/createmlcomponents/videoreader/cameraasyncbuffers/iterator/next())
- [VideoReader.CameraConfiguration](/documentation/createmlcomponents/videoreader/cameraconfiguration)

#### Creating a camera configuration

- [init()](/documentation/createmlcomponents/videoreader/cameraconfiguration/init())
- [init(position: VideoReader.CameraConfiguration.Position, pixelFormat: VideoReader.CameraConfiguration.PixelFormat, resolution: VideoReader.CameraConfiguration.Resolution, frameRate: Double)](/documentation/createmlcomponents/videoreader/cameraconfiguration/init(position:pixelformat:resolution:framerate:))
- [VideoReader.CameraConfiguration.PixelFormat](/documentation/createmlcomponents/videoreader/cameraconfiguration/pixelformat-swift.enum)

##### Pixel formats

- [case bgra32](/documentation/createmlcomponents/videoreader/cameraconfiguration/pixelformat-swift.enum/bgra32)
- [case yCbCr8BiPlanarFullRange420](/documentation/createmlcomponents/videoreader/cameraconfiguration/pixelformat-swift.enum/ycbcr8biplanarfullrange420)
- [VideoReader.CameraConfiguration.Position](/documentation/createmlcomponents/videoreader/cameraconfiguration/position-swift.enum)

##### Camera positions

- [case back](/documentation/createmlcomponents/videoreader/cameraconfiguration/position-swift.enum/back)
- [case front](/documentation/createmlcomponents/videoreader/cameraconfiguration/position-swift.enum/front)
- [VideoReader.CameraConfiguration.Resolution](/documentation/createmlcomponents/videoreader/cameraconfiguration/resolution-swift.enum)

##### Camera resolutions

- [case high](/documentation/createmlcomponents/videoreader/cameraconfiguration/resolution-swift.enum/high)
- [case low](/documentation/createmlcomponents/videoreader/cameraconfiguration/resolution-swift.enum/low)
- [case medium](/documentation/createmlcomponents/videoreader/cameraconfiguration/resolution-swift.enum/medium)

#### Getting the properties

- [var cameraPosition: VideoReader.CameraConfiguration.Position](/documentation/createmlcomponents/videoreader/cameraconfiguration/cameraposition)
- [var frameRate: Double](/documentation/createmlcomponents/videoreader/cameraconfiguration/framerate)
- [var pixelFormat: VideoReader.CameraConfiguration.PixelFormat](/documentation/createmlcomponents/videoreader/cameraconfiguration/pixelformat-swift.property)
- [var position: VideoReader.CameraConfiguration.Position](/documentation/createmlcomponents/videoreader/cameraconfiguration/position-swift.property)
- [var resolution: VideoReader.CameraConfiguration.Resolution](/documentation/createmlcomponents/videoreader/cameraconfiguration/resolution-swift.property)

### Applying

- [func applied(to: URL, eventHandler: EventHandler?) async throws -> VideoReader.AsyncFrames](/documentation/createmlcomponents/videoreader/applied(to:eventhandler:))
- [TemporalFileSegment](/documentation/createmlcomponents/temporalfilesegment)

### Creating a file segment

- [init(url: URL, range: Range<TimeInterval>)](/documentation/createmlcomponents/temporalfilesegment/init(url:range:))

### Getting the properties

- [var range: Range<TimeInterval>](/documentation/createmlcomponents/temporalfilesegment/range)
- [var url: URL](/documentation/createmlcomponents/temporalfilesegment/url)
- [AnyTemporalIterator](/documentation/createmlcomponents/anytemporaliterator)
- [AnyTemporalSequence](/documentation/createmlcomponents/anytemporalsequence)

### Creating a sequence

- [init<S>(S)](/documentation/createmlcomponents/anytemporalsequence/init(_:))
- [init<S>(S, count: Int?)](/documentation/createmlcomponents/anytemporalsequence/init(_:count:))
- [PreprocessedFeatureSequence](/documentation/createmlcomponents/preprocessedfeaturesequence)

### Creating a sequence

- [init<S>(S) async throws](/documentation/createmlcomponents/preprocessedfeaturesequence/init(_:))

### Getting the properties

- [var count: Int?](/documentation/createmlcomponents/preprocessedfeaturesequence/count)
- [var features: [TemporalFeature<Feature>]](/documentation/createmlcomponents/preprocessedfeaturesequence/features)

## Object detection components

- [DetectedObject](/documentation/createmlcomponents/detectedobject)

### Creating a detected object

- [init(boundingBox: CGRect, label: Label, probability: Float)](/documentation/createmlcomponents/detectedobject/init(boundingbox:label:probability:))

### Getting the properties

- [var boundingBox: CGRect](/documentation/createmlcomponents/detectedobject/boundingbox)
- [var confidence: Float](/documentation/createmlcomponents/detectedobject/confidence)
- [var label: Label](/documentation/createmlcomponents/detectedobject/label)
- [ObjectDetectionAnnotation](/documentation/createmlcomponents/objectdetectionannotation)

### Getting the properties

- [let imageFileName: String](/documentation/createmlcomponents/objectdetectionannotation/imagefilename)
- [let objects: [ObjectDetectionAnnotation<Label>.Annotation]](/documentation/createmlcomponents/objectdetectionannotation/objects)
- [ObjectDetectionAnnotation.Annotation](/documentation/createmlcomponents/objectdetectionannotation/annotation)

#### Getting the properties

- [let boundingBox: CGRect](/documentation/createmlcomponents/objectdetectionannotation/annotation/boundingbox)
- [let label: Label](/documentation/createmlcomponents/objectdetectionannotation/annotation/label)

#### Encoding and decoding

- [ObjectDetectionAnnotation.Annotation.CodingKeys](/documentation/createmlcomponents/objectdetectionannotation/annotation/codingkeys)

##### Coding keys

- [case boundingBox](/documentation/createmlcomponents/objectdetectionannotation/annotation/codingkeys/boundingbox)
- [case label](/documentation/createmlcomponents/objectdetectionannotation/annotation/codingkeys/label)
- [let prominentObject: Label](/documentation/createmlcomponents/objectdetectionannotation/prominentobject)

### Encoding and decoding

- [ObjectDetectionAnnotation.CodingKeys](/documentation/createmlcomponents/objectdetectionannotation/codingkeys)

#### Coding keys

- [case imageFileName](/documentation/createmlcomponents/objectdetectionannotation/codingkeys/imagefilename)
- [case objects](/documentation/createmlcomponents/objectdetectionannotation/codingkeys/objects)
- [case prominentObject](/documentation/createmlcomponents/objectdetectionannotation/codingkeys/prominentobject)

### Default Implementations

- [Identifiable Implementations](/documentation/createmlcomponents/objectdetectionannotation/identifiable-implementations)

#### Instance Properties

- [var id: String](/documentation/createmlcomponents/objectdetectionannotation/id)
- [ObjectDetectionMetrics](/documentation/createmlcomponents/objectdetectionmetrics)

### Creating a metrics object

- [init()](/documentation/createmlcomponents/objectdetectionmetrics/init())

### Getting the properties Properties

- [var defaultConfidenceThreshold: Float](/documentation/createmlcomponents/objectdetectionmetrics/defaultconfidencethreshold)
- [var labels: Set<Label>](/documentation/createmlcomponents/objectdetectionmetrics/labels)

### Calculating the precision

- [func averageOfAveragePrecisionAtVariedThresholds<Scalar>(predictions: [[DetectedObject<Label>]], annotations: [ObjectDetectionAnnotation<Label>], confidenceThresholds: [Label : Float]) -> [Label : Scalar]](/documentation/createmlcomponents/objectdetectionmetrics/averageofaverageprecisionatvariedthresholds(predictions:annotations:confidencethresholds:))
- [func averageOfMeanAveragePrecisionAtVariedThresholds<Scalar>(predictions: [[DetectedObject<Label>]], annotations: [ObjectDetectionAnnotation<Label>], confidenceThresholds: [Label : Float]) -> Scalar](/documentation/createmlcomponents/objectdetectionmetrics/averageofmeanaverageprecisionatvariedthresholds(predictions:annotations:confidencethresholds:))
- [func averagePrecision<Scalar>(predictions: [[DetectedObject<Label>]], annotations: [ObjectDetectionAnnotation<Label>], confidenceThresholds: [Label : Float], overlapThreshold: Double) -> [Label : Scalar]](/documentation/createmlcomponents/objectdetectionmetrics/averageprecision(predictions:annotations:confidencethresholds:overlapthreshold:))
- [func meanAveragePrecision<Scalar>(predictions: [[DetectedObject<Label>]], annotations: [ObjectDetectionAnnotation<Label>], confidenceThresholds: [Label : Float], overlapThreshold: Double) -> Scalar](/documentation/createmlcomponents/objectdetectionmetrics/meanaverageprecision(predictions:annotations:confidencethresholds:overlapthreshold:))

### Extracting labels

- [static func extractLabels(from: [ObjectDetectionAnnotation<Label>]) -> Set<Label>](/documentation/createmlcomponents/objectdetectionmetrics/extractlabels(from:))

## Tabular components

- [TabularTransformer](/documentation/createmlcomponents/tabulartransformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/tabulartransformer/appending(_:))

### Adapting

- [func adaptedAsEstimator() -> TabularTransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/tabulartransformer/adaptedasestimator())
- [func adaptedAsUpdatableEstimator() -> TabularTransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/tabulartransformer/adaptedasupdatableestimator())

### Transforming

- [func callAsFunction(DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/tabulartransformer/callasfunction(_:eventhandler:))

### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/tabulartransformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/tabulartransformer/export(to:metadata:))
- [TabularEstimator](/documentation/createmlcomponents/tabularestimator)

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/tabularestimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/tabularestimator/write(_:to:overwrite:))
- [Transformer](/documentation/createmlcomponents/tabularestimator/transformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/tabularestimator/appending(_:))

### Adapting and fitting

- [func adaptedAsSupervised<Annotation>(annotationColumnID: ColumnID<Annotation>) -> TabularEstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/tabularestimator/adaptedassupervised(annotationcolumnid:))
- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/tabularestimator/fitted(to:eventhandler:))
- [func fitted(to:)](/documentation/createmlcomponents/tabularestimator/fitted(to:))

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/tabularestimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/tabularestimator/decode(from:))
- [SupervisedTabularEstimator](/documentation/createmlcomponents/supervisedtabularestimator)

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtabularestimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/supervisedtabularestimator/write(_:to:overwrite:))
- [Annotation](/documentation/createmlcomponents/supervisedtabularestimator/annotation)
- [var annotationColumnID: ColumnID<Self.Annotation>](/documentation/createmlcomponents/supervisedtabularestimator/annotationcolumnid)
- [Transformer](/documentation/createmlcomponents/supervisedtabularestimator/transformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/supervisedtabularestimator/appending(_:))

### Fitting

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtabularestimator/fitted(to:validateon:eventhandler:))
- [func fitted(to: DataFrame, validateOn: DataFrame?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtabularestimator/fitted(to:validateon:))

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/supervisedtabularestimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtabularestimator/decode(from:))
- [ColumnSelector](/documentation/createmlcomponents/columnselector)

### Creating the selection

- [init(columns: [String], estimator: Estimator)](/documentation/createmlcomponents/columnselector/init(columns:estimator:))
- [init(ColumnSelection, estimator: Estimator)](/documentation/createmlcomponents/columnselector/init(_:estimator:))
- [init<T>(ColumnSelection, transformer: T)](/documentation/createmlcomponents/columnselector/init(_:transformer:))

### Getting the properties

- [var columnSelection: ColumnSelection](/documentation/createmlcomponents/columnselector/columnselection)
- [var estimator: Estimator](/documentation/createmlcomponents/columnselector/estimator)

### Encoding and decoding

- [func encode(ColumnSelector<Estimator, UnwrappedInput>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/columnselector/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> ColumnSelector<Estimator, UnwrappedInput>.Transformer](/documentation/createmlcomponents/columnselector/decode(from:))

### Fitting a transformer

- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> ColumnSelector<Estimator, UnwrappedInput>.Transformer](/documentation/createmlcomponents/columnselector/fitted(to:eventhandler:))
- [ColumnSelector.Input](/documentation/createmlcomponents/columnselector/input)
- [ColumnSelector.Output](/documentation/createmlcomponents/columnselector/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

### Default Implementations

- [UpdatableTabularEstimator Implementations](/documentation/createmlcomponents/columnselector/updatabletabularestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> ColumnSelector<Estimator, UnwrappedInput>.Transformer](/documentation/createmlcomponents/columnselector/decodewithoptimizer(from:))
- [func encodeWithOptimizer(ColumnSelector<Estimator, UnwrappedInput>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/columnselector/encodewithoptimizer(_:to:))
- [func makeTransformer() -> ColumnSelectorTransformer<Estimator.Transformer, UnwrappedInput>](/documentation/createmlcomponents/columnselector/maketransformer())
- [func update(inout ColumnSelector<Estimator, UnwrappedInput>.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/columnselector/update(_:with:eventhandler:))
- [ColumnSelectorTransformer](/documentation/createmlcomponents/columnselectortransformer)

### Creating the transformer

- [init(transformers: [String : Base], columnMapping: [String : String])](/documentation/createmlcomponents/columnselectortransformer/init(transformers:columnmapping:))

### Getting the properties

- [var columnMapping: [String : String]](/documentation/createmlcomponents/columnselectortransformer/columnmapping)
- [var transformers: [String : Base]](/documentation/createmlcomponents/columnselectortransformer/transformers)

### Applying a transformation

- [func applied(to: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/columnselectortransformer/applied(to:eventhandler:))
- [ColumnSelection](/documentation/createmlcomponents/columnselection)

### Column selection types

- [case all](/documentation/createmlcomponents/columnselection/all)
- [case exclude(columnNames: [String])](/documentation/createmlcomponents/columnselection/exclude(columnnames:))
- [case include(columnNames: [String])](/documentation/createmlcomponents/columnselection/include(columnnames:))
- [case numeric](/documentation/createmlcomponents/columnselection/numeric)
- [ColumnConcatenator](/documentation/createmlcomponents/columnconcatenator)

### Creating the concatenator

- [init(columnSelection: ColumnSelection, concatenatedColumnName: String)](/documentation/createmlcomponents/columnconcatenator/init(columnselection:concatenatedcolumnname:))

### Getting the properties

- [var columnSelection: ColumnSelection](/documentation/createmlcomponents/columnconcatenator/columnselection)
- [var concatenatedColumnName: String](/documentation/createmlcomponents/columnconcatenator/concatenatedcolumnname)

### Applying

- [func applied(to: DataFrame, eventHandler: EventHandler?) throws -> DataFrame](/documentation/createmlcomponents/columnconcatenator/applied(to:eventhandler:))
- [PreprocessingSupervisedTabularEstimator](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/init(_:_:))

### Getting the properties

- [var annotationColumnID: ColumnID<Estimator.Annotation>](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/annotationcolumnid)
- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/preprocessor)

### Preprocesing and fitting

- [func preprocessed(from: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/preprocessed(from:eventhandler:))
- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/fitted(to:validateon:eventhandler:))
- [func fitted(toPreprocessed: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/fitted(topreprocessed:validateon:eventhandler:))
- [PreprocessingSupervisedTabularEstimator.Annotation](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/annotation)
- [PreprocessingSupervisedTabularEstimator.Input](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/input)
- [PreprocessingSupervisedTabularEstimator.Intermediate](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/intermediate)
- [PreprocessingSupervisedTabularEstimator.Output](/documentation/createmlcomponents/preprocessingsupervisedtabularestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingTabularEstimator](/documentation/createmlcomponents/preprocessingtabularestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingtabularestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingtabularestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingtabularestimator/preprocessor)

### Preprocesing and fitting

- [func preprocessed(from: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/preprocessingtabularestimator/preprocessed(from:eventhandler:))
- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> PreprocessingTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingtabularestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: DataFrame, eventHandler: EventHandler?) async throws -> PreprocessingTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingtabularestimator/fitted(topreprocessed:eventhandler:))
- [PreprocessingTabularEstimator.Input](/documentation/createmlcomponents/preprocessingtabularestimator/input)
- [PreprocessingTabularEstimator.Intermediate](/documentation/createmlcomponents/preprocessingtabularestimator/intermediate)
- [PreprocessingTabularEstimator.Output](/documentation/createmlcomponents/preprocessingtabularestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableSupervisedTabularEstimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/init(_:_:))

### Getting the properties

- [var annotationColumnID: ColumnID<Estimator.Annotation>](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/annotationcolumnid)
- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/preprocessor)

### Encoding and decoding

- [func encodeWithOptimizer(PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/decodewithoptimizer(from:))

### Preprocesing and fitting

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/fitted(to:validateon:eventhandler:))
- [func fitted(toPreprocessed: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/fitted(topreprocessed:validateon:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/maketransformer())
- [func preprocessed(from: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/preprocessed(from:eventhandler:))
- [func update(inout PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/update(_:with:eventhandler:))
- [func update(inout PreprocessingUpdatableSupervisedTabularEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/update(_:withpreprocessed:eventhandler:))
- [PreprocessingUpdatableSupervisedTabularEstimator.Annotation](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/annotation)
- [PreprocessingUpdatableSupervisedTabularEstimator.Input](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/input)
- [PreprocessingUpdatableSupervisedTabularEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/intermediate)
- [PreprocessingUpdatableSupervisedTabularEstimator.Output](/documentation/createmlcomponents/preprocessingupdatablesupervisedtabularestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableTabularEstimator](/documentation/createmlcomponents/preprocessingupdatabletabularestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/preprocessor)

### Encoding and decoding

- [func encodeWithOptimizer(PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/decodewithoptimizer(from:))

### Preprocesing and fitting

- [func preprocessed(from: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/preprocessed(from:eventhandler:))
- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: DataFrame, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/fitted(topreprocessed:eventhandler:))
- [func update(inout PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/update(_:with:eventhandler:))
- [func update(inout PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/update(_:withpreprocessed:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableTabularEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/maketransformer())
- [PreprocessingUpdatableTabularEstimator.Input](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/input)
- [PreprocessingUpdatableTabularEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/intermediate)
- [PreprocessingUpdatableTabularEstimator.Output](/documentation/createmlcomponents/preprocessingupdatabletabularestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

## Protocols

- [Transformer](/documentation/createmlcomponents/transformer)

### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [TemporalTransformer](/documentation/createmlcomponents/temporaltransformer)

### Applying and adapting

- [func applied<S>(to: S, eventHandler: EventHandler?) async throws -> Self.OutputSequence](/documentation/createmlcomponents/temporaltransformer/applied(to:eventhandler:))
- [func adaptedAsEstimator() -> TemporalTransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/temporaltransformer/adaptedasestimator())
- [func adaptedAsUpdatableEstimator() -> TemporalTransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/temporaltransformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/temporaltransformer/input)
- [Output](/documentation/createmlcomponents/temporaltransformer/output)
- [OutputSequence](/documentation/createmlcomponents/temporaltransformer/outputsequence)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/temporaltransformer/appending(_:))

### Transforming and predicting

- [func callAsFunction<S>(S, eventHandler: EventHandler?) async throws -> Self.OutputSequence](/documentation/createmlcomponents/temporaltransformer/callasfunction(_:eventhandler:))
- [func callAsFunction<S>(to: S, eventHandler: EventHandler?) async throws -> [Self.OutputSequence]](/documentation/createmlcomponents/temporaltransformer/callasfunction(to:eventhandler:))
- [func prediction<S, Label>(from: S) async throws -> Self.OutputSequence](/documentation/createmlcomponents/temporaltransformer/prediction(from:))

### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/temporaltransformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/temporaltransformer/export(to:metadata:))
- [RandomTransformer](/documentation/createmlcomponents/randomtransformer)

### Performing the transformation

- [func applied(to: Self.Input, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/randomtransformer/applied(to:generator:eventhandler:))
- [Input](/documentation/createmlcomponents/randomtransformer/input)
- [Output](/documentation/createmlcomponents/randomtransformer/output)
- [Estimator](/documentation/createmlcomponents/estimator)

### Getting the properties

- [Transformer](/documentation/createmlcomponents/estimator/transformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/estimator/appending(_:))

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/estimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/estimator/decode(from:))

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/estimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/estimator/write(_:to:overwrite:))

### Fitting and adapting

- [func adaptedAsSupervised<Annotation>(annotationType: Annotation.Type) -> EstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/estimator/adaptedassupervised(annotationtype:))
- [func adaptedAsTemporal() -> EstimatorToTemporalAdaptor<Self>](/documentation/createmlcomponents/estimator/adaptedastemporal())
- [func fitted<S>(to: S, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/estimator/fitted(to:eventhandler:))
- [func fitted<S>(to: S) async throws -> Self.Transformer](/documentation/createmlcomponents/estimator/fitted(to:))
- [TemporalEstimator](/documentation/createmlcomponents/temporalestimator)

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/temporalestimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/temporalestimator/write(_:to:overwrite:))

### Appending

- [func appending(_:)](/documentation/createmlcomponents/temporalestimator/appending(_:))

### Adapting and fitting

- [func adaptedAsSupervised<Annotation>(annotationType: Annotation.Type) -> TemporalEstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/temporalestimator/adaptedassupervised(annotationtype:))
- [func fitted<InputSequence>(to: InputSequence) async throws -> Self.Transformer](/documentation/createmlcomponents/temporalestimator/fitted(to:))
- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/temporalestimator/fitted(to:eventhandler:))
- [Transformer](/documentation/createmlcomponents/temporalestimator/transformer)

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/temporalestimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/temporalestimator/decode(from:))
- [SupervisedEstimator](/documentation/createmlcomponents/supervisedestimator)

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/supervisedestimator/write(_:to:overwrite:))
- [Annotation](/documentation/createmlcomponents/supervisedestimator/annotation)
- [Transformer](/documentation/createmlcomponents/supervisedestimator/transformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/supervisedestimator/appending(_:))

### Adapting and fitting

- [func adaptedAsTemporal() -> SupervisedEstimatorToTemporalAdaptor<Self>](/documentation/createmlcomponents/supervisedestimator/adaptedastemporal())
- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/fitted(to:validateon:eventhandler:))
- [func fitted<Input>(to: Input) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/fitted(to:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/fitted(to:validateon:))

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/supervisedestimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedestimator/decode(from:))
- [SupervisedTemporalEstimator](/documentation/createmlcomponents/supervisedtemporalestimator)

### Reading and writing

- [func read(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/read(from:))
- [func write(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/supervisedtemporalestimator/write(_:to:overwrite:))
- [Annotation](/documentation/createmlcomponents/supervisedtemporalestimator/annotation)
- [Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/transformer)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/supervisedtemporalestimator/appending(_:))

### Fitting

- [func fitted<InputSequence, FeatureSequence>(to: InputSequence) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/fitted(to:))
- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/fitted(to:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/fitted(to:validateon:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/fitted(to:validateon:eventhandler:))
- [Annotation](/documentation/createmlcomponents/supervisedtemporalestimator/annotation)
- [Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/transformer)

### Encoding and decoding

- [func encode(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/supervisedtemporalestimator/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/supervisedtemporalestimator/decode(from:))
- [UpdatableEstimator](/documentation/createmlcomponents/updatableestimator)

### Adapting

- [func adaptedAsSupervised<Annotation>(annotationType: Annotation.Type) -> UpdatableEstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/updatableestimator/adaptedassupervised(annotationtype:))
- [func adaptedAsTemporal() -> UpdatableEstimatorToTemporalAdaptor<Self>](/documentation/createmlcomponents/updatableestimator/adaptedastemporal())

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatableestimator/appending(_:))

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatableestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatableestimator/decodewithoptimizer(from:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatableestimator/maketransformer())
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatableestimator/update(_:with:eventhandler:))
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence) async throws](/documentation/createmlcomponents/updatableestimator/update(_:with:))
- [UpdatableSupervisedEstimator](/documentation/createmlcomponents/updatablesupervisedestimator)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatablesupervisedestimator/appending(_:))

### Adapting

- [func adaptedAsTemporal() -> UpdatableSupervisedEstimatorToTemporalAdaptor<Self>](/documentation/createmlcomponents/updatablesupervisedestimator/adaptedastemporal())

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatablesupervisedestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedestimator/decodewithoptimizer(from:))

### Reading and writing

- [func readWithOptimizer(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedestimator/readwithoptimizer(from:))
- [func writeWithOptimizer(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/updatablesupervisedestimator/writewithoptimizer(_:to:overwrite:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedestimator/maketransformer())
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatablesupervisedestimator/update(_:with:eventhandler:))
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence) async throws](/documentation/createmlcomponents/updatablesupervisedestimator/update(_:with:))
- [UpdatableSupervisedTemporalEstimator](/documentation/createmlcomponents/updatablesupervisedtemporalestimator)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/appending(_:))

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/decodewithoptimizer(from:))

### Reading and writing

- [func readWithOptimizer(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/readwithoptimizer(from:))
- [func writeWithOptimizer(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/writewithoptimizer(_:to:overwrite:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/maketransformer())
- [func update<InputSequence, FeatureSequence>(inout Self.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/update(_:with:eventhandler:))
- [func update<InputSequence, FeatureSequence>(inout Self.Transformer, with: InputSequence) async throws](/documentation/createmlcomponents/updatablesupervisedtemporalestimator/update(_:with:))
- [UpdatableSupervisedTabularEstimator](/documentation/createmlcomponents/updatablesupervisedtabularestimator)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatablesupervisedtabularestimator/appending(_:))

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatablesupervisedtabularestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtabularestimator/decodewithoptimizer(from:))

### Reading and writing

- [func readWithOptimizer(from: URL) throws -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtabularestimator/readwithoptimizer(from:))
- [func writeWithOptimizer(Self.Transformer, to: URL, overwrite: Bool) throws](/documentation/createmlcomponents/updatablesupervisedtabularestimator/writewithoptimizer(_:to:overwrite:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatablesupervisedtabularestimator/maketransformer())
- [func update(inout Self.Transformer, with: DataFrame) async throws](/documentation/createmlcomponents/updatablesupervisedtabularestimator/update(_:with:))
- [func update(inout Self.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatablesupervisedtabularestimator/update(_:with:eventhandler:))
- [UpdatableTemporalEstimator](/documentation/createmlcomponents/updatabletemporalestimator)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatabletemporalestimator/appending(_:))

### Adapting

- [func adaptedAsSupervised<Annotation>(annotationType: Annotation.Type) -> UpdatableTemporalEstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/updatabletemporalestimator/adaptedassupervised(annotationtype:))

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletemporalestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatabletemporalestimator/decodewithoptimizer(from:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatabletemporalestimator/maketransformer())
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatabletemporalestimator/update(_:with:eventhandler:))
- [func update<InputSequence>(inout Self.Transformer, with: InputSequence) async throws](/documentation/createmlcomponents/updatabletemporalestimator/update(_:with:))
- [UpdatableTabularEstimator](/documentation/createmlcomponents/updatabletabularestimator)

### Appending

- [func appending(_:)](/documentation/createmlcomponents/updatabletabularestimator/appending(_:))

### Adapting

- [func adaptedAsSupervised<Annotation>(annotationColumnID: ColumnID<Annotation>) -> UpdatableTabularEstimatorToSupervisedAdaptor<Self, Annotation>](/documentation/createmlcomponents/updatabletabularestimator/adaptedassupervised(annotationcolumnid:))

### Encoding and decoding

- [func encodeWithOptimizer(Self.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletabularestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Self.Transformer](/documentation/createmlcomponents/updatabletabularestimator/decodewithoptimizer(from:))

### Transforming

- [func makeTransformer() -> Self.Transformer](/documentation/createmlcomponents/updatabletabularestimator/maketransformer())
- [func update(inout Self.Transformer, with: DataFrame) async throws](/documentation/createmlcomponents/updatabletabularestimator/update(_:with:))
- [func update(inout Self.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatabletabularestimator/update(_:with:eventhandler:))

## Core ML adaptors

- [MLModelTransformerAdaptor](/documentation/createmlcomponents/mlmodeltransformeradaptor)

### Creating an adaptor

- [init(model: MLModel) throws](/documentation/createmlcomponents/mlmodeltransformeradaptor/init(model:))
- [init(contentsOf: URL, configuration: MLModelConfiguration) throws](/documentation/createmlcomponents/mlmodeltransformeradaptor/init(contentsof:configuration:))

### Getting the model

- [let model: MLModel](/documentation/createmlcomponents/mlmodeltransformeradaptor/model)

### Performing the transformation

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> MLShapedArray<Scalar>](/documentation/createmlcomponents/mlmodeltransformeradaptor/applied(to:eventhandler:))
- [MLModelClassifierAdaptor](/documentation/createmlcomponents/mlmodelclassifieradaptor)

### Creating a transformer

- [init(model: MLModel) throws](/documentation/createmlcomponents/mlmodelclassifieradaptor/init(model:))
- [init(contentsOf: URL, configuration: MLModelConfiguration) throws](/documentation/createmlcomponents/mlmodelclassifieradaptor/init(contentsof:configuration:))

### Getting the model

- [let model: MLModel](/documentation/createmlcomponents/mlmodelclassifieradaptor/model)

### Performing the transformation

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> ClassificationDistribution<MLModelClassifierAdaptor<Scalar>.Label>](/documentation/createmlcomponents/mlmodelclassifieradaptor/applied(to:eventhandler:))
- [MLModelClassifierAdaptor.Label](/documentation/createmlcomponents/mlmodelclassifieradaptor/label)

#### Label types

- [case int(Int)](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/int(_:))
- [case string(String)](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/string(_:))

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/debugdescription)
- [ExpressibleByIntegerLiteral Implementations](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/expressiblebyintegerliteral-implementations)

##### Initializers

- [init(integerLiteral: Int)](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/init(integerliteral:))
- [ExpressibleByStringLiteral Implementations](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/expressiblebystringliteral-implementations)

##### Initializers

- [init(stringLiteral: String)](/documentation/createmlcomponents/mlmodelclassifieradaptor/label/init(stringliteral:))
- [MLModelRegressorAdaptor](/documentation/createmlcomponents/mlmodelregressoradaptor)

### Creating an adaptor

- [init(model: MLModel) throws](/documentation/createmlcomponents/mlmodelregressoradaptor/init(model:))
- [init(contentsOf: URL, configuration: MLModelConfiguration) throws](/documentation/createmlcomponents/mlmodelregressoradaptor/init(contentsof:configuration:))

### Getting the model

- [let model: MLModel](/documentation/createmlcomponents/mlmodelregressoradaptor/model)

### Performing the prediction

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> Double](/documentation/createmlcomponents/mlmodelregressoradaptor/applied(to:eventhandler:))
- [ModelMetadata](/documentation/createmlcomponents/modelmetadata)

### Creating a model

- [init(description: String, version: String, author: String, license: String, creatorDefined: [String : String])](/documentation/createmlcomponents/modelmetadata/init(description:version:author:license:creatordefined:))

### Getting the properties

- [var author: String](/documentation/createmlcomponents/modelmetadata/author)
- [var creatorDefined: [String : String]](/documentation/createmlcomponents/modelmetadata/creatordefined)
- [var description: String](/documentation/createmlcomponents/modelmetadata/description)
- [var license: String](/documentation/createmlcomponents/modelmetadata/license)
- [var version: String](/documentation/createmlcomponents/modelmetadata/version)

## Annotations

- [AnnotatedFiles](/documentation/createmlcomponents/annotatedfiles)

### Creating the feature

- [init(labeledBySubdirectoryNamesAt: URL, type: UTType, continueOnFailure: Bool) throws](/documentation/createmlcomponents/annotatedfiles/init(labeledbysubdirectorynamesat:type:continueonfailure:))
- [init(labeledByNamesAt: URL, separator: Character, index: Int, type: UTType, continueOnFailure: Bool) throws](/documentation/createmlcomponents/annotatedfiles/init(labeledbynamesat:separator:index:type:continueonfailure:))
- [AnnotatedBatch](/documentation/createmlcomponents/annotatedbatch)

### Creating an annotated batch

- [init(features: MLShapedArray<Scalar>, annotations: MLShapedArray<Scalar>)](/documentation/createmlcomponents/annotatedbatch/init(features:annotations:))

### Inspecting an annotated batch

- [var annotations: MLShapedArray<Scalar>](/documentation/createmlcomponents/annotatedbatch/annotations)
- [var count: Int](/documentation/createmlcomponents/annotatedbatch/count)
- [var features: MLShapedArray<Scalar>](/documentation/createmlcomponents/annotatedbatch/features)
- [AnnotatedFeature](/documentation/createmlcomponents/annotatedfeature)

### Creating the feature

- [init(feature: Feature, annotation: Annotation)](/documentation/createmlcomponents/annotatedfeature/init(feature:annotation:))

### Getting the properties

- [var annotation: Annotation](/documentation/createmlcomponents/annotatedfeature/annotation)
- [var feature: Feature](/documentation/createmlcomponents/annotatedfeature/feature)
- [AnnotatedFeatureProvider](/documentation/createmlcomponents/annotatedfeatureprovider)

### Creating the provider

- [init(Base, annotationsColumnName: String, featuresColumnName: String, resultsColumnName: String)](/documentation/createmlcomponents/annotatedfeatureprovider/init(_:annotationscolumnname:featurescolumnname:resultscolumnname:))

### Getting the properties

- [var annotationColumnID: ColumnID<AnnotatedFeatureProvider<Base, UnwrappedInput>.Annotation>](/documentation/createmlcomponents/annotatedfeatureprovider/annotationcolumnid)
- [AnnotatedFeatureProvider.Annotation](/documentation/createmlcomponents/annotatedfeatureprovider/annotation)
- [var base: Base](/documentation/createmlcomponents/annotatedfeatureprovider/base)
- [var featuresColumnName: String](/documentation/createmlcomponents/annotatedfeatureprovider/featurescolumnname)
- [var resultsColumnName: String](/documentation/createmlcomponents/annotatedfeatureprovider/resultscolumnname)

### Encoding and decoding

- [func encode(AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/annotatedfeatureprovider/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer](/documentation/createmlcomponents/annotatedfeatureprovider/decode(from:))

### Fitting

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> ColumnSelectorTransformer<Base.Transformer, UnwrappedInput>](/documentation/createmlcomponents/annotatedfeatureprovider/fitted(to:validateon:eventhandler:))
- [AnnotatedFeatureProvider.Transformer](/documentation/createmlcomponents/annotatedfeatureprovider/transformer)

### Default Implementations

- [UpdatableSupervisedTabularEstimator Implementations](/documentation/createmlcomponents/annotatedfeatureprovider/updatablesupervisedtabularestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer](/documentation/createmlcomponents/annotatedfeatureprovider/decodewithoptimizer(from:))
- [func encodeWithOptimizer(AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/annotatedfeatureprovider/encodewithoptimizer(_:to:))
- [func makeTransformer() -> AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer](/documentation/createmlcomponents/annotatedfeatureprovider/maketransformer())
- [func update(inout AnnotatedFeatureProvider<Base, UnwrappedInput>.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/annotatedfeatureprovider/update(_:with:eventhandler:))
- [AnnotatedPrediction](/documentation/createmlcomponents/annotatedprediction)

### Creating an annotated prediction

- [init(prediction: Prediction, annotation: Annotation)](/documentation/createmlcomponents/annotatedprediction/init(prediction:annotation:))

### Getting the properties

- [var annotation: Annotation](/documentation/createmlcomponents/annotatedprediction/annotation)
- [var prediction: Prediction](/documentation/createmlcomponents/annotatedprediction/prediction)
- [DataFrameTemporalAnnotationParameters](/documentation/createmlcomponents/dataframetemporalannotationparameters)

### Creating the parameters

- [init()](/documentation/createmlcomponents/dataframetemporalannotationparameters/init())

### Getting the properties

- [var annotationColumnID: ColumnID<Annotation>](/documentation/createmlcomponents/dataframetemporalannotationparameters/annotationcolumnid)
- [var endTimeColumnID: ColumnID<Double>?](/documentation/createmlcomponents/dataframetemporalannotationparameters/endtimecolumnid)
- [var filePathColumnID: ColumnID<String>](/documentation/createmlcomponents/dataframetemporalannotationparameters/filepathcolumnid)
- [var filePathType: DataFrameTemporalAnnotationParameters<Annotation>.FilePathType](/documentation/createmlcomponents/dataframetemporalannotationparameters/filepathtype-swift.property)
- [var startTimeColumnID: ColumnID<Double>?](/documentation/createmlcomponents/dataframetemporalannotationparameters/starttimecolumnid)

### Specifying the path type

- [DataFrameTemporalAnnotationParameters.FilePathType](/documentation/createmlcomponents/dataframetemporalannotationparameters/filepathtype-swift.enum)

#### File path types

- [case absolute](/documentation/createmlcomponents/dataframetemporalannotationparameters/filepathtype-swift.enum/absolute)
- [case relative(baseURL: URL)](/documentation/createmlcomponents/dataframetemporalannotationparameters/filepathtype-swift.enum/relative(baseurl:))

## Augmentations

- [ApplyEachRandomly](/documentation/createmlcomponents/applyeachrandomly)

### Creating an augmentation

- [init<RandomTransformer>(probability: Double, () -> RandomTransformer)](/documentation/createmlcomponents/applyeachrandomly/init(probability:_:))

### Getting the probability

- [let probability: Double](/documentation/createmlcomponents/applyeachrandomly/probability)

### Applying transformers

- [func applied(to: Element, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> Element](/documentation/createmlcomponents/applyeachrandomly/applied(to:generator:eventhandler:))
- [ApplyRandomly](/documentation/createmlcomponents/applyrandomly)

### Creating an augmentation

- [init<Input>(probability: Double, () -> RandomTransformer)](/documentation/createmlcomponents/applyrandomly/init(probability:_:))

### Getting the probability

- [let probability: Double](/documentation/createmlcomponents/applyrandomly/probability)

### Applying transformers

- [func applied(to: RandomTransformer.Input, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> RandomTransformer.Output](/documentation/createmlcomponents/applyrandomly/applied(to:generator:eventhandler:))
- [AugmentationBuilder](/documentation/createmlcomponents/augmentationbuilder)

### Building augmentations

- [static buildPartialBlock(accumulated:next:)](/documentation/createmlcomponents/augmentationbuilder/buildpartialblock(accumulated:next:))
- [static buildPartialBlock(first:)](/documentation/createmlcomponents/augmentationbuilder/buildpartialblock(first:))
- [AugmentationSequence](/documentation/createmlcomponents/augmentationsequence)

### Getting the transformer

- [var transformer: RandomTransformer](/documentation/createmlcomponents/augmentationsequence/transformer)

### Batching an augmentation sequence

- [func batches(ofSize: Int, dropsLastPartialBatch: Bool) -> AugmentationSequence<Base, RandomTransformer, RandomNumberGenerator, Annotation>.BatchedSequence](/documentation/createmlcomponents/augmentationsequence/batches(ofsize:dropslastpartialbatch:))
- [AugmentationSequence.BatchedSequence](/documentation/createmlcomponents/augmentationsequence/batchedsequence)

#### Creating an iterator

- [func makeAsyncIterator() -> AugmentationSequence<Base, RandomTransformer, RandomNumberGenerator, Annotation>.BatchedSequence.AsyncIterator](/documentation/createmlcomponents/augmentationsequence/batchedsequence/makeasynciterator())
- [AugmentationSequence.Element](/documentation/createmlcomponents/augmentationsequence/element)

#### Default Implementations

- [AsyncSequence Implementations](/documentation/createmlcomponents/augmentationsequence/batchedsequence/asyncsequence-implementations)

##### Structures

- [AugmentationSequence.BatchedSequence.AsyncIterator](/documentation/createmlcomponents/augmentationsequence/batchedsequence/asynciterator)

###### Getting the next element

- [func next() async throws -> [AugmentationSequence<Base, RandomTransformer, RandomNumberGenerator, Annotation>.Element]?](/documentation/createmlcomponents/augmentationsequence/batchedsequence/asynciterator/next())

### Creating an iterator

- [func makeAsyncIterator() -> AugmentationSequence<Base, RandomTransformer, RandomNumberGenerator, Annotation>.AsyncIterator](/documentation/createmlcomponents/augmentationsequence/makeasynciterator())
- [AugmentationSequence.Element](/documentation/createmlcomponents/augmentationsequence/element)

### Default Implementations

- [AsyncSequence Implementations](/documentation/createmlcomponents/augmentationsequence/asyncsequence-implementations)

#### Structures

- [AugmentationSequence.AsyncIterator](/documentation/createmlcomponents/augmentationsequence/asynciterator)

##### Getting the next element

- [func next() async throws -> Base.Element?](/documentation/createmlcomponents/augmentationsequence/asynciterator/next())
- [Augmenter](/documentation/createmlcomponents/augmenter)

### Creating an augmenter

- [init<Input>(generator: RandomNumberGenerator, () -> RandomTransformer)](/documentation/createmlcomponents/augmenter/init(generator:_:))

### Applying an augmentation

- [func applied<S, Annotation>(to: S) -> AugmentationSequence<S, RandomTransformer, RandomNumberGenerator, Annotation>](/documentation/createmlcomponents/augmenter/applied(to:))
- [func applied<C, Annotation>(to: C, upsampledBy: Int) -> UpsampledAugmentationSequence<C, RandomTransformer, RandomNumberGenerator, Annotation>](/documentation/createmlcomponents/augmenter/applied(to:upsampledby:))
- [ChooseRandomly](/documentation/createmlcomponents/chooserandomly)

### Creating an augmentation

- [init<RandomTransformer>(() -> RandomTransformer)](/documentation/createmlcomponents/chooserandomly/init(_:))

### Applying transformers

- [func applied(to: Element, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> Element](/documentation/createmlcomponents/chooserandomly/applied(to:generator:eventhandler:))
- [RandomImageCropper](/documentation/createmlcomponents/randomimagecropper)

### Creating an image cropper

- [init(scale: ClosedRange<Double>, aspectRatio: Double?)](/documentation/createmlcomponents/randomimagecropper/init(scale:aspectratio:))
- [init(targetSize: CGSize)](/documentation/createmlcomponents/randomimagecropper/init(targetsize:))
- [init(targetWidth: Double, targetHeight: Double)](/documentation/createmlcomponents/randomimagecropper/init(targetwidth:targetheight:))

### Performing the augmentation

- [func applied(to: CIImage, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> CIImage](/documentation/createmlcomponents/randomimagecropper/applied(to:generator:eventhandler:))
- [ShuffleRandomly](/documentation/createmlcomponents/shufflerandomly)

### Creating a transformer

- [init<RandomTransformer>(() -> RandomTransformer)](/documentation/createmlcomponents/shufflerandomly/init(_:))

### Performing the transformation

- [func applied(to: Element, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> Element](/documentation/createmlcomponents/shufflerandomly/applied(to:generator:eventhandler:))
- [UniformRandomFloatingPointParameter](/documentation/createmlcomponents/uniformrandomfloatingpointparameter)

### Creating a transformer

- [init<Input>(range: ClosedRange<Parameter>, (Parameter) -> RandomTransformer)](/documentation/createmlcomponents/uniformrandomfloatingpointparameter/init(range:_:))

### Getting the range

- [var range: ClosedRange<Parameter>](/documentation/createmlcomponents/uniformrandomfloatingpointparameter/range)

### Applying

- [func applied(to: RandomTransformer.Input, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> RandomTransformer.Output](/documentation/createmlcomponents/uniformrandomfloatingpointparameter/applied(to:generator:eventhandler:))
- [UniformRandomIntegerParameter](/documentation/createmlcomponents/uniformrandomintegerparameter)

### Creating a transformer

- [init(range:_:)](/documentation/createmlcomponents/uniformrandomintegerparameter/init(range:_:))

### Getting the range

- [var range: Range<Parameter>](/documentation/createmlcomponents/uniformrandomintegerparameter/range)

### Applying

- [func applied(to: RandomTransformer.Input, generator: inout some RandomNumberGenerator, eventHandler: EventHandler?) async throws -> RandomTransformer.Output](/documentation/createmlcomponents/uniformrandomintegerparameter/applied(to:generator:eventhandler:))
- [UpsampledAugmentationSequence](/documentation/createmlcomponents/upsampledaugmentationsequence)

### Getting the transformer

- [let transformer: RandomTransformer](/documentation/createmlcomponents/upsampledaugmentationsequence/transformer)

### Creating an iterator

- [func makeAsyncIterator() -> UpsampledAugmentationSequence<Base, RandomTransformer, RandomNumberGenerator, Annotation>.AsyncIterator](/documentation/createmlcomponents/upsampledaugmentationsequence/makeasynciterator())
- [UpsampledAugmentationSequence.Element](/documentation/createmlcomponents/upsampledaugmentationsequence/element)

### Default Implementations

- [AsyncSequence Implementations](/documentation/createmlcomponents/upsampledaugmentationsequence/asyncsequence-implementations)

#### Structures

- [UpsampledAugmentationSequence.AsyncIterator](/documentation/createmlcomponents/upsampledaugmentationsequence/asynciterator)

##### Getting the next element

- [func next() async throws -> Base.Element?](/documentation/createmlcomponents/upsampledaugmentationsequence/asynciterator/next())

## Event handling

- [Event](/documentation/createmlcomponents/event)

### Creating the event

- [init(origin: String, itemCount: Int, totalItemCount: Int?, metrics: [MetricsKey : any Sendable])](/documentation/createmlcomponents/event/init(origin:itemcount:totalitemcount:metrics:))

### Getting the properties

- [var itemCount: Int](/documentation/createmlcomponents/event/itemcount)
- [var metrics: [MetricsKey : any Sendable]](/documentation/createmlcomponents/event/metrics)
- [var origin: String](/documentation/createmlcomponents/event/origin)
- [var totalItemCount: Int?](/documentation/createmlcomponents/event/totalitemcount)
- [EventHandler](/documentation/createmlcomponents/eventhandler)
- [MetricsKey](/documentation/createmlcomponents/metricskey)

### Getting the properties

- [static let source: MetricsKey](/documentation/createmlcomponents/metricskey/source)
- [static let trainingAccuracy: MetricsKey](/documentation/createmlcomponents/metricskey/trainingaccuracy)
- [static let trainingError: MetricsKey](/documentation/createmlcomponents/metricskey/trainingerror)
- [static let trainingLoss: MetricsKey](/documentation/createmlcomponents/metricskey/trainingloss)
- [static let trainingMaximumError: MetricsKey](/documentation/createmlcomponents/metricskey/trainingmaximumerror)
- [static let trainingMeanAveragePrecision: MetricsKey](/documentation/createmlcomponents/metricskey/trainingmeanaverageprecision)
- [static let validationAccuracy: MetricsKey](/documentation/createmlcomponents/metricskey/validationaccuracy)
- [static let validationError: MetricsKey](/documentation/createmlcomponents/metricskey/validationerror)
- [static let validationLoss: MetricsKey](/documentation/createmlcomponents/metricskey/validationloss)
- [static let validationMaximumError: MetricsKey](/documentation/createmlcomponents/metricskey/validationmaximumerror)
- [static let validationMeanAveragePrecision: MetricsKey](/documentation/createmlcomponents/metricskey/validationmeanaverageprecision)

## Scalers

- [StandardScaler](/documentation/createmlcomponents/standardscaler)

### Creating an estimator

- [init()](/documentation/createmlcomponents/standardscaler/init())

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> StandardScaler<Element>.Transformer](/documentation/createmlcomponents/standardscaler/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/standardscaler/estimator-implementations)

#### Structures

- [StandardScaler.Transformer](/documentation/createmlcomponents/standardscaler/transformer)

##### Creating a transformer

- [init(mean: Element, standardDeviation: Element)](/documentation/createmlcomponents/standardscaler/transformer/init(mean:standarddeviation:))

##### Getting the properties

- [var mean: Element](/documentation/createmlcomponents/standardscaler/transformer/mean)
- [var standardDeviation: Element](/documentation/createmlcomponents/standardscaler/transformer/standarddeviation)

##### Performing the transformation

- [func applied(to: Element, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/standardscaler/transformer/applied(to:eventhandler:))
- [UpdatableEstimator Implementations](/documentation/createmlcomponents/standardscaler/updatableestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> StandardScaler<Element>.Transformer](/documentation/createmlcomponents/standardscaler/decodewithoptimizer(from:))
- [func encodeWithOptimizer(StandardScaler<Element>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/standardscaler/encodewithoptimizer(_:to:))
- [func makeTransformer() -> StandardScaler<Element>.Transformer](/documentation/createmlcomponents/standardscaler/maketransformer())
- [func update(inout StandardScaler<Element>.Transformer, with: some Sequence<Element>, eventHandler: EventHandler?)](/documentation/createmlcomponents/standardscaler/update(_:with:eventhandler:))
- [MaxAbsScaler](/documentation/createmlcomponents/maxabsscaler)

### Creating an estimator

- [init()](/documentation/createmlcomponents/maxabsscaler/init())

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> MaxAbsScaler<Element>.Transformer](/documentation/createmlcomponents/maxabsscaler/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/maxabsscaler/estimator-implementations)

#### Structures

- [MaxAbsScaler.Transformer](/documentation/createmlcomponents/maxabsscaler/transformer)

##### Creating a transformer

- [init(maximumAbsoluteValue: Element)](/documentation/createmlcomponents/maxabsscaler/transformer/init(maximumabsolutevalue:))

##### Getting the absolute value

- [var maximumAbsoluteValue: Element](/documentation/createmlcomponents/maxabsscaler/transformer/maximumabsolutevalue)

##### Performing the transformation

- [func applied(to: Element, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/maxabsscaler/transformer/applied(to:eventhandler:))
- [MinMaxScaler](/documentation/createmlcomponents/minmaxscaler)

### Creating an estimator

- [init(range: ClosedRange<Element>)](/documentation/createmlcomponents/minmaxscaler/init(range:))

### Getting the properties

- [var range: ClosedRange<Element>](/documentation/createmlcomponents/minmaxscaler/range)

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> MinMaxScaler<Element>.Transformer](/documentation/createmlcomponents/minmaxscaler/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/minmaxscaler/estimator-implementations)

#### Structures

- [MinMaxScaler.Transformer](/documentation/createmlcomponents/minmaxscaler/transformer)

##### Creating a transformer

- [init(desiredRange: ClosedRange<Element>, fittedRange: ClosedRange<Element>)](/documentation/createmlcomponents/minmaxscaler/transformer/init(desiredrange:fittedrange:))

##### Getting the properties

- [var desiredRange: ClosedRange<Element>](/documentation/createmlcomponents/minmaxscaler/transformer/desiredrange)
- [var fittedRange: ClosedRange<Element>](/documentation/createmlcomponents/minmaxscaler/transformer/fittedrange)

##### Performing the transformation

- [func applied(to: Element, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/minmaxscaler/transformer/applied(to:eventhandler:))
- [NormalizationScaler](/documentation/createmlcomponents/normalizationscaler)

### Creating a scaler

- [init(norm: NormalizationScaler<Element>.NormalizationStrategy)](/documentation/createmlcomponents/normalizationscaler/init(norm:))
- [NormalizationScaler.NormalizationStrategy](/documentation/createmlcomponents/normalizationscaler/normalizationstrategy)

#### Normalization strategies

- [case l1](/documentation/createmlcomponents/normalizationscaler/normalizationstrategy/l1)
- [case l2](/documentation/createmlcomponents/normalizationscaler/normalizationstrategy/l2)

### Getting the normalization

- [var norm: NormalizationScaler<Element>.NormalizationStrategy](/documentation/createmlcomponents/normalizationscaler/norm)

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> NormalizationScaler<Element>.Transformer](/documentation/createmlcomponents/normalizationscaler/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/normalizationscaler/estimator-implementations)

#### Structures

- [NormalizationScaler.Transformer](/documentation/createmlcomponents/normalizationscaler/transformer)

##### Creating a transformer

- [init(scale: Element)](/documentation/createmlcomponents/normalizationscaler/transformer/init(scale:))

##### Getting the scale

- [var scale: Element](/documentation/createmlcomponents/normalizationscaler/transformer/scale)

##### Performing the transformation

- [func applied(to: Element, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/normalizationscaler/transformer/applied(to:eventhandler:))
- [RobustScaler](/documentation/createmlcomponents/robustscaler)

### Creating an estimator

- [init(quantileRange: ClosedRange<Element>)](/documentation/createmlcomponents/robustscaler/init(quantilerange:))

### Getting the properties

- [var quantileRange: ClosedRange<Element>](/documentation/createmlcomponents/robustscaler/quantilerange)

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> RobustScaler<Element>.Transformer](/documentation/createmlcomponents/robustscaler/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/robustscaler/estimator-implementations)

#### Structures

- [RobustScaler.Transformer](/documentation/createmlcomponents/robustscaler/transformer)

##### Creating a transformer

- [init(median: Element, interQuartileRange: Element)](/documentation/createmlcomponents/robustscaler/transformer/init(median:interquartilerange:))

##### Getting the properties

- [var interQuartileRange: Element](/documentation/createmlcomponents/robustscaler/transformer/interquartilerange)
- [var median: Element](/documentation/createmlcomponents/robustscaler/transformer/median)

##### Performing the transformation

- [func applied(to: Element, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/robustscaler/transformer/applied(to:eventhandler:))

## Preprocessors

- [LinearTransformer](/documentation/createmlcomponents/lineartransformer)

### Creating a regressor

- [init(scale: Element, offset: Element)](/documentation/createmlcomponents/lineartransformer/init(scale:offset:))

### Getting the properties

- [var offset: Element](/documentation/createmlcomponents/lineartransformer/offset)
- [var scale: Element](/documentation/createmlcomponents/lineartransformer/scale)

### Performing the transformation

- [func applied(to:eventHandler:)](/documentation/createmlcomponents/lineartransformer/applied(to:eventhandler:))
- [ImputeTransformer](/documentation/createmlcomponents/imputetransformer)

### Creating a transformer

- [init(value: Element)](/documentation/createmlcomponents/imputetransformer/init(value:))

### Getting the impute value

- [var value: Element](/documentation/createmlcomponents/imputetransformer/value)

### Performing the transformation

- [func applied(to: Element?, eventHandler: EventHandler?) -> Element](/documentation/createmlcomponents/imputetransformer/applied(to:eventhandler:))
- [OneHotEncoder](/documentation/createmlcomponents/onehotencoder)

### Creating the estimator

- [init()](/documentation/createmlcomponents/onehotencoder/init())

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> OneHotEncoder<Category>.Transformer](/documentation/createmlcomponents/onehotencoder/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/onehotencoder/estimator-implementations)

#### Structures

- [OneHotEncoder.Transformer](/documentation/createmlcomponents/onehotencoder/transformer)

##### Creating a transformer

- [init(categories: Set<Category?>)](/documentation/createmlcomponents/onehotencoder/transformer/init(categories:))

##### Getting the categories

- [var categories: Set<Category?>](/documentation/createmlcomponents/onehotencoder/transformer/categories)
- [func category(at: Int) -> Category?](/documentation/createmlcomponents/onehotencoder/transformer/category(at:))

##### Performing the transformation

- [func applied<S>(S, eventHandler: EventHandler?) throws -> [[Int]]](/documentation/createmlcomponents/onehotencoder/transformer/applied(_:eventhandler:))
- [func applied(to: Category?, eventHandler: EventHandler?) throws -> [Int]](/documentation/createmlcomponents/onehotencoder/transformer/applied(to:eventhandler:))

##### Default Implementations

- [Decodable Implementations](/documentation/createmlcomponents/onehotencoder/transformer/decodable-implementations)

###### Initializers

- [init(from: any Decoder) throws](/documentation/createmlcomponents/onehotencoder/transformer/init(from:))
- [Encodable Implementations](/documentation/createmlcomponents/onehotencoder/transformer/encodable-implementations)

###### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/createmlcomponents/onehotencoder/transformer/encode(to:))
- [UpdatableEstimator Implementations](/documentation/createmlcomponents/onehotencoder/updatableestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> OneHotEncoder<Category>.Transformer](/documentation/createmlcomponents/onehotencoder/decodewithoptimizer(from:))
- [func encodeWithOptimizer(OneHotEncoder<Category>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/onehotencoder/encodewithoptimizer(_:to:))
- [func makeTransformer() -> OneHotEncoder<Category>.Transformer](/documentation/createmlcomponents/onehotencoder/maketransformer())
- [func update(inout OneHotEncoder<Category>.Transformer, with: some Sequence<Optional<Category>>, eventHandler: EventHandler?) throws](/documentation/createmlcomponents/onehotencoder/update(_:with:eventhandler:))
- [OrdinalEncoder](/documentation/createmlcomponents/ordinalencoder)

### Creating an encoder

- [init()](/documentation/createmlcomponents/ordinalencoder/init())

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) throws -> OrdinalEncoder<Category>.Transformer](/documentation/createmlcomponents/ordinalencoder/fitted(to:eventhandler:))

### Default Implementations

- [Estimator Implementations](/documentation/createmlcomponents/ordinalencoder/estimator-implementations)

#### Structures

- [OrdinalEncoder.Transformer](/documentation/createmlcomponents/ordinalencoder/transformer)

##### Creating a transformer

- [init(categories: Set<Category?>)](/documentation/createmlcomponents/ordinalencoder/transformer/init(categories:))

##### Getting the categories

- [var categories: Set<Category?>](/documentation/createmlcomponents/ordinalencoder/transformer/categories)
- [func category(at: Int) -> Category?](/documentation/createmlcomponents/ordinalencoder/transformer/category(at:))

##### Applying the transformation

- [func applied<S>(S, eventHandler: EventHandler?) throws -> [Int]](/documentation/createmlcomponents/ordinalencoder/transformer/applied(_:eventhandler:))
- [func applied(to: Category?, eventHandler: EventHandler?) throws -> Int](/documentation/createmlcomponents/ordinalencoder/transformer/applied(to:eventhandler:))

##### Default Implementations

- [Decodable Implementations](/documentation/createmlcomponents/ordinalencoder/transformer/decodable-implementations)

###### Initializers

- [init(from: any Decoder) throws](/documentation/createmlcomponents/ordinalencoder/transformer/init(from:))
- [Encodable Implementations](/documentation/createmlcomponents/ordinalencoder/transformer/encodable-implementations)

###### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/createmlcomponents/ordinalencoder/transformer/encode(to:))
- [UpdatableEstimator Implementations](/documentation/createmlcomponents/ordinalencoder/updatableestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> OrdinalEncoder<Category>.Transformer](/documentation/createmlcomponents/ordinalencoder/decodewithoptimizer(from:))
- [func encodeWithOptimizer(OrdinalEncoder<Category>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/ordinalencoder/encodewithoptimizer(_:to:))
- [func makeTransformer() -> OrdinalEncoder<Category>.Transformer](/documentation/createmlcomponents/ordinalencoder/maketransformer())
- [func update(inout OrdinalEncoder<Category>.Transformer, with: some Sequence<Optional<Category>>, eventHandler: EventHandler?) throws](/documentation/createmlcomponents/ordinalencoder/update(_:with:eventhandler:))
- [NumericImputer](/documentation/createmlcomponents/numericimputer)

### Creating an estimator

- [init(NumericImputer<Element>.Strategy)](/documentation/createmlcomponents/numericimputer/init(_:))
- [init(constant: Element)](/documentation/createmlcomponents/numericimputer/init(constant:))

### Getting the properties

- [var strategy: NumericImputer<Element>.Strategy](/documentation/createmlcomponents/numericimputer/strategy-swift.property)

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) -> NumericImputer<Element>.Transformer](/documentation/createmlcomponents/numericimputer/fitted(to:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [NumericImputer.Strategy](/documentation/createmlcomponents/numericimputer/strategy-swift.enum)

#### Imputer strategies

- [case constant(Element)](/documentation/createmlcomponents/numericimputer/strategy-swift.enum/constant(_:))
- [case mean](/documentation/createmlcomponents/numericimputer/strategy-swift.enum/mean)
- [case median](/documentation/createmlcomponents/numericimputer/strategy-swift.enum/median)

### Default Implementations

- [UpdatableEstimator Implementations](/documentation/createmlcomponents/numericimputer/updatableestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> NumericImputer<Element>.Transformer](/documentation/createmlcomponents/numericimputer/decodewithoptimizer(from:))
- [func encodeWithOptimizer(NumericImputer<Element>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/numericimputer/encodewithoptimizer(_:to:))
- [func makeTransformer() -> NumericImputer<Element>.Transformer](/documentation/createmlcomponents/numericimputer/maketransformer())
- [func update(inout ImputeTransformer<Element>, with: some Sequence<Optional<Element>>, eventHandler: EventHandler?) throws](/documentation/createmlcomponents/numericimputer/update(_:with:eventhandler:))
- [Reshaper](/documentation/createmlcomponents/reshaper)

### Creating a transformer

- [init(shape: [Int])](/documentation/createmlcomponents/reshaper/init(shape:))

### Getting the shape

- [var shape: [Int]](/documentation/createmlcomponents/reshaper/shape)

### Performing the transformation

- [func applied<S>(S, eventHandler: EventHandler?) throws -> [MLShapedArray<Scalar>]](/documentation/createmlcomponents/reshaper/applied(_:eventhandler:))
- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) throws -> MLShapedArray<Scalar>](/documentation/createmlcomponents/reshaper/applied(to:eventhandler:))
- [CategoricalImputer](/documentation/createmlcomponents/categoricalimputer)

### Creating an estimator

- [init(CategoricalImputer<Element>.Strategy)](/documentation/createmlcomponents/categoricalimputer/init(_:))
- [init(constant: Element)](/documentation/createmlcomponents/categoricalimputer/init(constant:))

### Getting the properties

- [var strategy: CategoricalImputer<Element>.Strategy](/documentation/createmlcomponents/categoricalimputer/strategy-swift.property)

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) -> CategoricalImputer<Element>.Transformer](/documentation/createmlcomponents/categoricalimputer/fitted(to:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [CategoricalImputer.Strategy](/documentation/createmlcomponents/categoricalimputer/strategy-swift.enum)

#### Imputer strategies

- [case constant(Element)](/documentation/createmlcomponents/categoricalimputer/strategy-swift.enum/constant(_:))
- [case mode](/documentation/createmlcomponents/categoricalimputer/strategy-swift.enum/mode)
- [OptionalUnwrapper](/documentation/createmlcomponents/optionalunwrapper)

### Creating a transformer

- [init()](/documentation/createmlcomponents/optionalunwrapper/init())

### Performing the transformation

- [func applied(to: Element?, eventHandler: EventHandler?) throws -> Element](/documentation/createmlcomponents/optionalunwrapper/applied(to:eventhandler:))

## Regressors

- [Regressor](/documentation/createmlcomponents/regressor)

### Performing the prediction

- [func prediction(from:)](/documentation/createmlcomponents/regressor/prediction(from:))
- [LinearRegressor](/documentation/createmlcomponents/linearregressor)

### Creating a regressor

- [init(configuration: LinearRegressor<Scalar>.Configuration)](/documentation/createmlcomponents/linearregressor/init(configuration:))
- [LinearRegressor.Configuration](/documentation/createmlcomponents/linearregressor/configuration-swift.struct)

#### Creating a configuration

- [init()](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/init())

#### Getting the properties

- [var convergenceThreshold: Double](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/convergencethreshold)
- [var earlyStopIterationCount: Int](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/earlystopiterationcount)
- [var l1Penalty: Double](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/l1penalty)
- [var l2Penalty: Double](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/l2penalty)
- [var maximumIterations: Int](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/maximumiterations)
- [var optimizationStrategy: OptimizationStrategy](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/optimizationstrategy)
- [var scaleFeatures: Bool](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/scalefeatures)
- [var stepSize: Double](/documentation/createmlcomponents/linearregressor/configuration-swift.struct/stepsize)

### Getting the configuration

- [var configuration: LinearRegressor<Scalar>.Configuration](/documentation/createmlcomponents/linearregressor/configuration-swift.property)

### Encoding and decoding

- [func encodeWithOptimizer(LinearRegressorModel<Scalar>, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/linearregressor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> LinearRegressorModel<Scalar>](/documentation/createmlcomponents/linearregressor/decodewithoptimizer(from:))

### Fitting

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> LinearRegressorModel<Scalar>](/documentation/createmlcomponents/linearregressor/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> LinearRegressorModel<Scalar>](/documentation/createmlcomponents/linearregressor/fitted(to:validateon:eventhandler:))
- [LinearRegressor.Annotation](/documentation/createmlcomponents/linearregressor/annotation)
- [LinearRegressor.Transformer](/documentation/createmlcomponents/linearregressor/transformer)

### Default Implementations

- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/linearregressor/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> LinearRegressorModel<Scalar>](/documentation/createmlcomponents/linearregressor/decodewithoptimizer(from:))
- [func encodeWithOptimizer(LinearRegressorModel<Scalar>, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/linearregressor/encodewithoptimizer(_:to:))
- [func makeTransformer() -> LinearRegressorModel<Scalar>](/documentation/createmlcomponents/linearregressor/maketransformer())
- [func update<InputSequence>(inout LinearRegressor<Scalar>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/linearregressor/update(_:with:eventhandler:))
- [LinearRegressorModel](/documentation/createmlcomponents/linearregressormodel)

### Creating a regressor model

- [init(coefficients: some Sequence<Scalar>)](/documentation/createmlcomponents/linearregressormodel/init(coefficients:))

### Getting the properties

- [var featureCount: Int](/documentation/createmlcomponents/linearregressormodel/featurecount)
- [var coefficients: [Scalar]](/documentation/createmlcomponents/linearregressormodel/coefficients)

### Performing the regression

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> Scalar](/documentation/createmlcomponents/linearregressormodel/applied(to:eventhandler:))
- [MultivariateLinearRegressor](/documentation/createmlcomponents/multivariatelinearregressor)

### Creating a regressor

- [init(configuration: MultivariateLinearRegressor<Scalar>.Configuration)](/documentation/createmlcomponents/multivariatelinearregressor/init(configuration:))

### Getting the configuration

- [var configuration: MultivariateLinearRegressor<Scalar>.Configuration](/documentation/createmlcomponents/multivariatelinearregressor/configuration-swift.property)

### Fitting

- [func fitted(to: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws -> MultivariateLinearRegressor<Scalar>.Model](/documentation/createmlcomponents/multivariatelinearregressor/fitted(to:eventhandler:))
- [func fitted(to:validateOn:eventHandler:)](/documentation/createmlcomponents/multivariatelinearregressor/fitted(to:validateon:eventhandler:))

### Fitting Progressively

- [func makeTransformer() -> MultivariateLinearRegressor<Scalar>.Model](/documentation/createmlcomponents/multivariatelinearregressor/maketransformer())
- [func update(inout MultivariateLinearRegressor<Scalar>.Model, with: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/multivariatelinearregressor/update(_:with:eventhandler:))
- [func update(inout MultivariateLinearRegressor<Scalar>.Model, with: AnnotatedBatch<Scalar>) async throws -> Scalar](/documentation/createmlcomponents/multivariatelinearregressor/update(_:with:))

### Encoding and decoding

- [func encodeWithOptimizer(MultivariateLinearRegressor<Scalar>.Model, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/multivariatelinearregressor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> MultivariateLinearRegressor<Scalar>.Model](/documentation/createmlcomponents/multivariatelinearregressor/decodewithoptimizer(from:))

### Supporting types

- [MultivariateLinearRegressor.Model](/documentation/createmlcomponents/multivariatelinearregressor/model)

#### Creating a regressor model

- [init(weight: MLShapedArray<Scalar>, bias: MLShapedArray<Scalar>?)](/documentation/createmlcomponents/multivariatelinearregressor/model/init(weight:bias:))

#### Getting the properties

- [var inputSize: Int](/documentation/createmlcomponents/multivariatelinearregressor/model/inputsize)
- [var outputSize: Int](/documentation/createmlcomponents/multivariatelinearregressor/model/outputsize)
- [var weight: MLShapedArray<Scalar>](/documentation/createmlcomponents/multivariatelinearregressor/model/weight)
- [var bias: MLShapedArray<Scalar>?](/documentation/createmlcomponents/multivariatelinearregressor/model/bias)

#### Performing the regression

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> MLShapedArray<Scalar>](/documentation/createmlcomponents/multivariatelinearregressor/model/applied(to:eventhandler:))
- [MultivariateLinearRegressor.Annotation](/documentation/createmlcomponents/multivariatelinearregressor/annotation)
- [MultivariateLinearRegressor.Configuration](/documentation/createmlcomponents/multivariatelinearregressor/configuration-swift.typealias)
- [MultivariateLinearRegressor.Feature](/documentation/createmlcomponents/multivariatelinearregressor/feature)
- [MultivariateLinearRegressor.Transformer](/documentation/createmlcomponents/multivariatelinearregressor/transformer)

### Default Implementations

- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/multivariatelinearregressor/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> MultivariateLinearRegressor<Scalar>.Model](/documentation/createmlcomponents/multivariatelinearregressor/decodewithoptimizer(from:))
- [func encodeWithOptimizer(MultivariateLinearRegressor<Scalar>.Model, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/multivariatelinearregressor/encodewithoptimizer(_:to:))
- [func makeTransformer() -> MultivariateLinearRegressor<Scalar>.Model](/documentation/createmlcomponents/multivariatelinearregressor/maketransformer())
- [func update(inout MultivariateLinearRegressor<Scalar>.Model, with: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, MLShapedArray<Scalar>>>, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/multivariatelinearregressor/update(_:with:eventhandler:))
- [MultivariateLinearRegressorConfiguration](/documentation/createmlcomponents/multivariatelinearregressorconfiguration)

### Creating a configuration

- [init()](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/init())

### Getting the properties

- [var batchSize: Int](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/batchsize)
- [var maximumIterationCount: Int](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/maximumiterationcount)
- [var earlyStoppingTolerance: Float](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/earlystoppingtolerance)
- [var earlyStoppingIterationCount: Int](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/earlystoppingiterationcount)
- [var learningRate: Float](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/learningrate)
- [var randomSeed: Int?](/documentation/createmlcomponents/multivariatelinearregressorconfiguration/randomseed)
- [MultivariateLinearRegressor.Model](/documentation/createmlcomponents/multivariatelinearregressor/model)

### Creating a regressor model

- [init(weight: MLShapedArray<Scalar>, bias: MLShapedArray<Scalar>?)](/documentation/createmlcomponents/multivariatelinearregressor/model/init(weight:bias:))

### Getting the properties

- [var inputSize: Int](/documentation/createmlcomponents/multivariatelinearregressor/model/inputsize)
- [var outputSize: Int](/documentation/createmlcomponents/multivariatelinearregressor/model/outputsize)
- [var weight: MLShapedArray<Scalar>](/documentation/createmlcomponents/multivariatelinearregressor/model/weight)
- [var bias: MLShapedArray<Scalar>?](/documentation/createmlcomponents/multivariatelinearregressor/model/bias)

### Performing the regression

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> MLShapedArray<Scalar>](/documentation/createmlcomponents/multivariatelinearregressor/model/applied(to:eventhandler:))
- [FullyConnectedNetworkRegressor](/documentation/createmlcomponents/fullyconnectednetworkregressor)

### Creating the regressor

- [init(configuration: FullyConnectedNetworkConfiguration)](/documentation/createmlcomponents/fullyconnectednetworkregressor/init(configuration:))

### Getting the configuration

- [var configuration: FullyConnectedNetworkConfiguration](/documentation/createmlcomponents/fullyconnectednetworkregressor/configuration)

### Decoding a regressor

- [func decode(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkRegressorModel<Scalar>](/documentation/createmlcomponents/fullyconnectednetworkregressor/decode(from:))

### Fitting a regressor

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkRegressor<Scalar>.Transformer](/documentation/createmlcomponents/fullyconnectednetworkregressor/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkRegressorModel<Scalar>](/documentation/createmlcomponents/fullyconnectednetworkregressor/fitted(to:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

### Default Implementations

- [SupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkregressor/supervisedestimator-implementations)

#### Instance Methods

- [func decode(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkRegressorModel<Scalar>](/documentation/createmlcomponents/fullyconnectednetworkregressor/decode(from:))
- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkregressor/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkRegressor<Scalar>.Transformer](/documentation/createmlcomponents/fullyconnectednetworkregressor/decodewithoptimizer(from:))
- [func encodeWithOptimizer(FullyConnectedNetworkRegressor<Scalar>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/fullyconnectednetworkregressor/encodewithoptimizer(_:to:))
- [func makeTransformer() -> FullyConnectedNetworkRegressorModel<Scalar>](/documentation/createmlcomponents/fullyconnectednetworkregressor/maketransformer())
- [func update<InputSequence>(inout FullyConnectedNetworkRegressorModel<Scalar>, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/fullyconnectednetworkregressor/update(_:with:eventhandler:))
- [FullyConnectedNetworkRegressorModel](/documentation/createmlcomponents/fullyconnectednetworkregressormodel)

### Performing a regression

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkRegressorModel<Scalar>.Target](/documentation/createmlcomponents/fullyconnectednetworkregressormodel/applied(to:eventhandler:))
- [FullyConnectedNetworkRegressorModel.Target](/documentation/createmlcomponents/fullyconnectednetworkregressormodel/target)
- [BoostedTreeRegressor](/documentation/createmlcomponents/boostedtreeregressor)

### Creating a regressor

- [init(annotationColumnName: String, featureColumnNames: [String], configuration: BoostedTreeConfiguration)](/documentation/createmlcomponents/boostedtreeregressor/init(annotationcolumnname:featurecolumnnames:configuration:))

### Getting the properties

- [var annotationColumnID: ColumnID<Annotation>](/documentation/createmlcomponents/boostedtreeregressor/annotationcolumnid)
- [var configuration: BoostedTreeConfiguration](/documentation/createmlcomponents/boostedtreeregressor/configuration)
- [var featureColumnNames: [String]](/documentation/createmlcomponents/boostedtreeregressor/featurecolumnnames)

### Fitting a regressor model

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> TreeRegressorModel](/documentation/createmlcomponents/boostedtreeregressor/fitted(to:validateon:eventhandler:))
- [BoostedTreeRegressor.Transformer](/documentation/createmlcomponents/boostedtreeregressor/transformer)

### Encoding and decoding a regressor

- [func encodeWithOptimizer(TreeRegressorModel, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/boostedtreeregressor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> TreeRegressorModel](/documentation/createmlcomponents/boostedtreeregressor/decodewithoptimizer(from:))

### Default Implementations

- [UpdatableSupervisedTabularEstimator Implementations](/documentation/createmlcomponents/boostedtreeregressor/updatablesupervisedtabularestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> TreeRegressorModel](/documentation/createmlcomponents/boostedtreeregressor/decodewithoptimizer(from:))
- [func encodeWithOptimizer(TreeRegressorModel, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/boostedtreeregressor/encodewithoptimizer(_:to:))
- [func makeTransformer() -> TreeRegressorModel](/documentation/createmlcomponents/boostedtreeregressor/maketransformer())
- [func update(inout TreeRegressorModel, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/boostedtreeregressor/update(_:with:eventhandler:))
- [TreeRegressorModel](/documentation/createmlcomponents/treeregressormodel)

### Getting the column names

- [var featureColumnNames: [String]](/documentation/createmlcomponents/treeregressormodel/featurecolumnnames)
- [var predictionColumnName: String](/documentation/createmlcomponents/treeregressormodel/predictioncolumnname)

### Applying

- [func applied(to: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/treeregressormodel/applied(to:eventhandler:))
- [OptimizationStrategy](/documentation/createmlcomponents/optimizationstrategy)

### Optimization strategies

- [case automatic](/documentation/createmlcomponents/optimizationstrategy/automatic)
- [case fast](/documentation/createmlcomponents/optimizationstrategy/fast)
- [case lowMemory](/documentation/createmlcomponents/optimizationstrategy/lowmemory)
- [case nonSmooth](/documentation/createmlcomponents/optimizationstrategy/nonsmooth)

## Serializers

- [EstimatorDecoder](/documentation/createmlcomponents/estimatordecoder)

### Decoding values

- [func decode<T>(T.Type) throws -> T](/documentation/createmlcomponents/estimatordecoder/decode(_:))
- [func decodeOptimizer<T>(T.Type) throws -> T](/documentation/createmlcomponents/estimatordecoder/decodeoptimizer(_:))
- [EstimatorEncoder](/documentation/createmlcomponents/estimatorencoder)

### Encoding values

- [func encode<T>(T) throws](/documentation/createmlcomponents/estimatorencoder/encode(_:))
- [func encodeOptimizer<T>(T) throws](/documentation/createmlcomponents/estimatorencoder/encodeoptimizer(_:))

## Classifiers

- [Classifier](/documentation/createmlcomponents/classifier)

### Getting the properties

- [Label](/documentation/createmlcomponents/classifier/label)
- [LogisticRegressionClassifier](/documentation/createmlcomponents/logisticregressionclassifier)

### Creating a classifier

- [init(labels: Set<Label>, configuration: LogisticRegressionClassifier<Scalar, Label>.Configuration)](/documentation/createmlcomponents/logisticregressionclassifier/init(labels:configuration:))
- [LogisticRegressionClassifier.Configuration](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct)

#### Creating a configuration

- [init()](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/init())

#### Getting the properties

- [var convergenceThreshold: Double](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/convergencethreshold)
- [var earlyStopIterationCount: Int](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/earlystopiterationcount)
- [var l1Penalty: Double](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/l1penalty)
- [var l2Penalty: Double](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/l2penalty)
- [var maximumIterations: Int](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/maximumiterations)
- [var optimizationStrategy: OptimizationStrategy](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/optimizationstrategy)
- [var scaleFeatures: Bool](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/scalefeatures)
- [var stepSize: Double](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.struct/stepsize)

### Getting the properties

- [var configuration: LogisticRegressionClassifier<Scalar, Label>.Configuration](/documentation/createmlcomponents/logisticregressionclassifier/configuration-swift.property)
- [var labels: Set<Label>](/documentation/createmlcomponents/logisticregressionclassifier/labels)

### Encoding and decoding

- [func encodeWithOptimizer(LogisticRegressionClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/logisticregressionclassifier/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> LogisticRegressionClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/logisticregressionclassifier/decodewithoptimizer(from:))

### Fitting

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> LogisticRegressionClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/logisticregressionclassifier/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> LogisticRegressionClassifierModel<Scalar, Label>](/documentation/createmlcomponents/logisticregressionclassifier/fitted(to:validateon:eventhandler:))
- [LogisticRegressionClassifier.Annotation](/documentation/createmlcomponents/logisticregressionclassifier/annotation)
- [LogisticRegressionClassifier.Transformer](/documentation/createmlcomponents/logisticregressionclassifier/transformer)

### Default Implementations

- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/logisticregressionclassifier/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> LogisticRegressionClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/logisticregressionclassifier/decodewithoptimizer(from:))
- [func encodeWithOptimizer(LogisticRegressionClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/logisticregressionclassifier/encodewithoptimizer(_:to:))
- [func makeTransformer() -> LogisticRegressionClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/logisticregressionclassifier/maketransformer())
- [func update<InputSequence>(inout LogisticRegressionClassifier<Scalar, Label>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/logisticregressionclassifier/update(_:with:eventhandler:))
- [LogisticRegressionClassifierModel](/documentation/createmlcomponents/logisticregressionclassifiermodel)

### Creating a regression model

- [init(coefficients: some Sequence<Scalar>, labels: Set<Label>)](/documentation/createmlcomponents/logisticregressionclassifiermodel/init(coefficients:labels:))

### Getting the properties

- [var coefficients: [Scalar]](/documentation/createmlcomponents/logisticregressionclassifiermodel/coefficients)
- [var featureCount: Int](/documentation/createmlcomponents/logisticregressionclassifiermodel/featurecount)

### Performing the classification

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> ClassificationDistribution<Label>](/documentation/createmlcomponents/logisticregressionclassifiermodel/applied(to:eventhandler:))
- [BoostedTreeClassifier](/documentation/createmlcomponents/boostedtreeclassifier)

### Creating a classifier

- [init(labels: Set<Label?>, annotationColumnName: String, featureColumnNames: [String], configuration: BoostedTreeConfiguration)](/documentation/createmlcomponents/boostedtreeclassifier/init(labels:annotationcolumnname:featurecolumnnames:configuration:))

### Getting the properties

- [var annotationColumnID: ColumnID<Label>](/documentation/createmlcomponents/boostedtreeclassifier/annotationcolumnid)
- [var featureColumnNames: [String]](/documentation/createmlcomponents/boostedtreeclassifier/featurecolumnnames)
- [var configuration: BoostedTreeConfiguration](/documentation/createmlcomponents/boostedtreeclassifier/configuration)
- [var labels: Set<Label?>](/documentation/createmlcomponents/boostedtreeclassifier/labels)

### Fitting the classifier

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> TreeClassifierModel<Label>](/documentation/createmlcomponents/boostedtreeclassifier/fitted(to:validateon:eventhandler:))
- [BoostedTreeClassifier.Annotation](/documentation/createmlcomponents/boostedtreeclassifier/annotation)
- [BoostedTreeClassifier.Transformer](/documentation/createmlcomponents/boostedtreeclassifier/transformer)

### Encoding the classifier labels

- [func encodeLabels(some Collection<Optional<Label>>) throws -> (labels: [String?], encoded: [Int])](/documentation/createmlcomponents/boostedtreeclassifier/encodelabels(_:))

### Default Implementations

- [UpdatableSupervisedTabularEstimator Implementations](/documentation/createmlcomponents/boostedtreeclassifier/updatablesupervisedtabularestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> TreeClassifierModel<Label>](/documentation/createmlcomponents/boostedtreeclassifier/decodewithoptimizer(from:))
- [func encodeWithOptimizer(TreeClassifierModel<Label>, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/boostedtreeclassifier/encodewithoptimizer(_:to:))
- [func makeTransformer() -> TreeClassifierModel<Label>](/documentation/createmlcomponents/boostedtreeclassifier/maketransformer())
- [func update(inout TreeClassifierModel<Label>, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/boostedtreeclassifier/update(_:with:eventhandler:))
- [BoostedTreeConfiguration](/documentation/createmlcomponents/boostedtreeconfiguration)

### Creating a configuration

- [init()](/documentation/createmlcomponents/boostedtreeconfiguration/init())

### Inspecting the configuration

- [var columnSubsample: Double](/documentation/createmlcomponents/boostedtreeconfiguration/columnsubsample)
- [var earlyStoppingIterationCount: Int?](/documentation/createmlcomponents/boostedtreeconfiguration/earlystoppingiterationcount)
- [var learningRate: Double](/documentation/createmlcomponents/boostedtreeconfiguration/learningrate)
- [var maximumDepth: Int](/documentation/createmlcomponents/boostedtreeconfiguration/maximumdepth)
- [var maximumIterations: Int](/documentation/createmlcomponents/boostedtreeconfiguration/maximumiterations)
- [var minimumChildWeight: Double](/documentation/createmlcomponents/boostedtreeconfiguration/minimumchildweight)
- [var minimumLossReduction: Double](/documentation/createmlcomponents/boostedtreeconfiguration/minimumlossreduction)
- [var parallelTreeCount: Int](/documentation/createmlcomponents/boostedtreeconfiguration/paralleltreecount)
- [var randomSeed: Int](/documentation/createmlcomponents/boostedtreeconfiguration/randomseed)
- [var rowSubsample: Double](/documentation/createmlcomponents/boostedtreeconfiguration/rowsubsample)
- [var stepSize: Double](/documentation/createmlcomponents/boostedtreeconfiguration/stepsize)
- [FullyConnectedNetworkClassifier](/documentation/createmlcomponents/fullyconnectednetworkclassifier)

### Creating the classifier

- [init(labels: Set<Label>, configuration: FullyConnectedNetworkConfiguration)](/documentation/createmlcomponents/fullyconnectednetworkclassifier/init(labels:configuration:))

### Getting the properties

- [var labels: Set<Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/labels)
- [var configuration: FullyConnectedNetworkConfiguration](/documentation/createmlcomponents/fullyconnectednetworkclassifier/configuration)

### Encoding and decoding

- [func encodeWithOptimizer(FullyConnectedNetworkClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/fullyconnectednetworkclassifier/encodewithoptimizer(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/decode(from:))

### Fitting a classifier

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/fitted(to:validateon:eventhandler:))
- [FullyConnectedNetworkClassifier.Annotation](/documentation/createmlcomponents/fullyconnectednetworkclassifier/annotation)
- [FullyConnectedNetworkClassifier.Transformer](/documentation/createmlcomponents/fullyconnectednetworkclassifier/transformer)

### Default Implementations

- [SupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkclassifier/supervisedestimator-implementations)

#### Instance Methods

- [func decode(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/decode(from:))
- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkclassifier/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/fullyconnectednetworkclassifier/decodewithoptimizer(from:))
- [func encodeWithOptimizer(FullyConnectedNetworkClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/fullyconnectednetworkclassifier/encodewithoptimizer(_:to:))
- [func makeTransformer() -> FullyConnectedNetworkClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifier/maketransformer())
- [func update<InputSequence>(inout FullyConnectedNetworkClassifierModel<Scalar, Label>, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/fullyconnectednetworkclassifier/update(_:with:eventhandler:))
- [FullyConnectedNetworkClassifierModel](/documentation/createmlcomponents/fullyconnectednetworkclassifiermodel)

### Applying a classification

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) async throws -> ClassificationDistribution<Label>](/documentation/createmlcomponents/fullyconnectednetworkclassifiermodel/applied(to:eventhandler:))
- [FullyConnectedNetworkMultiLabelClassifier](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier)

### Creating a classifier

- [init(labels: Set<Label>, configuration: FullyConnectedNetworkConfiguration)](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/init(labels:configuration:))

### Getting the properties

- [var configuration: FullyConnectedNetworkConfiguration](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/configuration)
- [static var defaultConfiguration: FullyConnectedNetworkConfiguration](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/defaultconfiguration)
- [var labels: Set<Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/labels)

### Fitting a classifier

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkMultiLabelClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> FullyConnectedNetworkMultiLabelClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/fitted(to:validateon:eventhandler:))
- [FullyConnectedNetworkMultiLabelClassifier.Annotation](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/annotation)
- [FullyConnectedNetworkMultiLabelClassifier.Transformer](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/transformer)

### Default Implementations

- [SupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/supervisedestimator-implementations)

#### Instance Methods

- [func decode(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkMultiLabelClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/decode(from:))
- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> FullyConnectedNetworkMultiLabelClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/decodewithoptimizer(from:))
- [func encodeWithOptimizer(FullyConnectedNetworkMultiLabelClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/encodewithoptimizer(_:to:))
- [func makeTransformer() -> FullyConnectedNetworkMultiLabelClassifierModel<Scalar, Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/maketransformer())
- [func update<InputSequence>(inout FullyConnectedNetworkMultiLabelClassifierModel<Scalar, Label>, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifier/update(_:with:eventhandler:))
- [FullyConnectedNetworkMultiLabelClassifierModel](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifiermodel)

### Performing a classification

- [func applied(to: MLShapedArray<Scalar>, eventHandler: EventHandler?) throws -> ClassificationDistribution<Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifiermodel/applied(to:eventhandler:))

### Computing evaluation metrics

- [func evaluation(on: some Collection<AnnotatedFeature<MLShapedArray<Scalar>, Set<Label>>>, confidenceThresholds: [Label : Float]) throws -> MultiLabelClassificationMetrics<Label>](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifiermodel/evaluation(on:confidencethresholds:))

### Performing a prediction

- [func prediction(from:confidenceThresholds:)](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifiermodel/prediction(from:confidencethresholds:))

### Updating the precision recall curve

- [func updatePrecisionRecallCurves(some Collection<AnnotatedFeature<MLShapedArray<Scalar>, Set<Label>>>) async throws](/documentation/createmlcomponents/fullyconnectednetworkmultilabelclassifiermodel/updateprecisionrecallcurves(_:))
- [FullyConnectedNetworkConfiguration](/documentation/createmlcomponents/fullyconnectednetworkconfiguration)

### Creating a network configuration

- [init()](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/init())

### Getting the properties

- [var batchSize: Int](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/batchsize)
- [var dropoutProbability: Float](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/dropoutprobability)
- [var earlyStopIterationCount: Int](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/earlystopiterationcount)
- [var earlyStoppingTolerance: Double](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/earlystoppingtolerance)
- [var hiddenUnitCounts: [Int]](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/hiddenunitcounts)
- [var learningRate: Float](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/learningrate)
- [var maximumIterations: Int](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/maximumiterations)
- [var randomSeed: Int](/documentation/createmlcomponents/fullyconnectednetworkconfiguration/randomseed)
- [TreeClassifierModel](/documentation/createmlcomponents/treeclassifiermodel)

### Getting the properties

- [var classCount: Int](/documentation/createmlcomponents/treeclassifiermodel/classcount)
- [var featureColumnNames: [String]](/documentation/createmlcomponents/treeclassifiermodel/featurecolumnnames)
- [var predictionColumnName: String](/documentation/createmlcomponents/treeclassifiermodel/predictioncolumnname)

### Building a data frame

- [func buildDataFrame([ClassificationDistribution<Label>]) -> DataFrame](/documentation/createmlcomponents/treeclassifiermodel/builddataframe(_:))

### Applying

- [func applied(to: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/treeclassifiermodel/applied(to:eventhandler:))
- [TimeSeriesClassifier](/documentation/createmlcomponents/timeseriesclassifier)

### Creating a time series classifier

- [init(labels: Set<Label>, configuration: TimeSeriesClassifierConfiguration)](/documentation/createmlcomponents/timeseriesclassifier/init(labels:configuration:))

### Inspecting a time series classifier

- [var configuration: TimeSeriesClassifierConfiguration](/documentation/createmlcomponents/timeseriesclassifier/configuration-swift.property)
- [var labels: Set<Label>](/documentation/createmlcomponents/timeseriesclassifier/labels)

### Fitting a time series classifier

- [func fitted(to: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, Label>>, eventHandler: EventHandler?) async throws -> TimeSeriesClassifier<Scalar, Label>.Model](/documentation/createmlcomponents/timeseriesclassifier/fitted(to:eventhandler:))
- [func fitted(to: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, Label>>, validateOn: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, Label>>, eventHandler: EventHandler?) async throws -> TimeSeriesClassifier<Scalar, Label>.Model](/documentation/createmlcomponents/timeseriesclassifier/fitted(to:validateon:eventhandler:))

### Supporting types

- [TimeSeriesClassifier.Configuration](/documentation/createmlcomponents/timeseriesclassifier/configuration-swift.typealias)
- [TimeSeriesClassifier.Model](/documentation/createmlcomponents/timeseriesclassifier/model)

#### Getting the stride

- [var stride: Int](/documentation/createmlcomponents/timeseriesclassifier/model/stride)

#### Applying and exporting

- [func applied(to:eventHandler:)](/documentation/createmlcomponents/timeseriesclassifier/model/applied(to:eventhandler:))
- [func export(to: URL) throws](/documentation/createmlcomponents/timeseriesclassifier/model/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/timeseriesclassifier/model/export(to:metadata:))

#### Default Implementations

- [TemporalTransformer Implementations](/documentation/createmlcomponents/timeseriesclassifier/model/temporaltransformer-implementations)

##### Instance Methods

- [func applied(to: some TemporalSequence<MLShapedArray<Scalar>>, eventHandler: EventHandler?) async throws -> AnyTemporalSequence<ClassificationDistribution<Label>>](/documentation/createmlcomponents/timeseriesclassifier/model/applied(to:eventhandler:)-3hpop)

### Default Implementations

- [UpdatableSupervisedEstimator Implementations](/documentation/createmlcomponents/timeseriesclassifier/updatablesupervisedestimator-implementations)

#### Instance Methods

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> TimeSeriesClassifier<Scalar, Label>.Transformer](/documentation/createmlcomponents/timeseriesclassifier/decodewithoptimizer(from:))
- [func encodeWithOptimizer(TimeSeriesClassifier<Scalar, Label>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/timeseriesclassifier/encodewithoptimizer(_:to:))
- [func makeTransformer() -> TimeSeriesClassifier<Scalar, Label>.Model](/documentation/createmlcomponents/timeseriesclassifier/maketransformer())
- [func update(inout TimeSeriesClassifier<Scalar, Label>.Model, with: some Sequence<AnnotatedFeature<MLShapedArray<Scalar>, Label>>, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/timeseriesclassifier/update(_:with:eventhandler:))
- [TimeSeriesClassifierConfiguration](/documentation/createmlcomponents/timeseriesclassifierconfiguration)

### Creating a time series classifier configuration

- [init()](/documentation/createmlcomponents/timeseriesclassifierconfiguration/init())

### Inspecting a time series classifier configuration

- [var batchSize: Int](/documentation/createmlcomponents/timeseriesclassifierconfiguration/batchsize)
- [var earlyStoppingIterationCount: Int](/documentation/createmlcomponents/timeseriesclassifierconfiguration/earlystoppingiterationcount)
- [var earlyStoppingTolerance: Float](/documentation/createmlcomponents/timeseriesclassifierconfiguration/earlystoppingtolerance)
- [var learningRate: Float](/documentation/createmlcomponents/timeseriesclassifierconfiguration/learningrate)
- [var maximumIterationCount: Int](/documentation/createmlcomponents/timeseriesclassifierconfiguration/maximumiterationcount)
- [var maximumSequenceLength: Int](/documentation/createmlcomponents/timeseriesclassifierconfiguration/maximumsequencelength)
- [var minimumSequenceLength: Int](/documentation/createmlcomponents/timeseriesclassifierconfiguration/minimumsequencelength)
- [var randomSeed: Int?](/documentation/createmlcomponents/timeseriesclassifierconfiguration/randomseed)

## Metrics

- [Classification](/documentation/createmlcomponents/classification)

### Creating the item

- [init(label: Label, probability: Float)](/documentation/createmlcomponents/classification/init(label:probability:))

### Getting the properties

- [var label: Label](/documentation/createmlcomponents/classification/label)
- [var probability: Float](/documentation/createmlcomponents/classification/probability)
- [ClassificationDistribution](/documentation/createmlcomponents/classificationdistribution)

### Creating the distribution

- [init<C>(C)](/documentation/createmlcomponents/classificationdistribution/init(_:))

### Getting the properties

- [var endIndex: Int](/documentation/createmlcomponents/classificationdistribution/endindex)
- [var labelsSortedByProbability: [Label]](/documentation/createmlcomponents/classificationdistribution/labelssortedbyprobability)
- [var mostLikelyLabel: Label?](/documentation/createmlcomponents/classificationdistribution/mostlikelylabel)
- [var startIndex: Int](/documentation/createmlcomponents/classificationdistribution/startindex)

### Getting the index

- [func index(after: Int) -> Int](/documentation/createmlcomponents/classificationdistribution/index(after:))
- [func index(before: Int) -> Int](/documentation/createmlcomponents/classificationdistribution/index(before:))

### Labeling and mapping

- [func topLabels(Int) -> [Label]](/documentation/createmlcomponents/classificationdistribution/toplabels(_:))
- [func map<T>((Classification<Label>) throws -> Classification<T>) rethrows -> ClassificationDistribution<T>](/documentation/createmlcomponents/classificationdistribution/map(_:))

### Accessing by subscript

- [subscript(_:)](/documentation/createmlcomponents/classificationdistribution/subscript(_:))
- [ClassificationMetrics](/documentation/createmlcomponents/classificationmetrics)

### Creating the distribution

- [init<Predicted, Correct>(Predicted, Correct)](/documentation/createmlcomponents/classificationmetrics/init(_:_:))
- [init()](/documentation/createmlcomponents/classificationmetrics/init())
- [init(_:)](/documentation/createmlcomponents/classificationmetrics/init(_:))
- [init(some Sequence<(predicted: Label, label: Label)>, labels: Set<Label>)](/documentation/createmlcomponents/classificationmetrics/init(_:labels:))
- [init<Predicted, Correct>(predicted: Predicted, groundTruth: Correct, labels: Set<Label>)](/documentation/createmlcomponents/classificationmetrics/init(predicted:groundtruth:labels:))

### Getting the properties

- [var accuracy: Double](/documentation/createmlcomponents/classificationmetrics/accuracy)
- [var exampleCount: Int](/documentation/createmlcomponents/classificationmetrics/examplecount)
- [var labels: Set<Label>](/documentation/createmlcomponents/classificationmetrics/labels)
- [var restrictToKnownLabels: Bool](/documentation/createmlcomponents/classificationmetrics/restricttoknownlabels)

### Computing and scoring

- [func makeConfusionMatrix() -> MLShapedArray<Float>](/documentation/createmlcomponents/classificationmetrics/makeconfusionmatrix())
- [func precisionScore(label: Label) -> Double](/documentation/createmlcomponents/classificationmetrics/precisionscore(label:))
- [func recallScore(label: Label) -> Double](/documentation/createmlcomponents/classificationmetrics/recallscore(label:))
- [func count(label: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/count(label:))
- [func count(predicted: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/count(predicted:))
- [func count(predicted: Label, label: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/count(predicted:label:))
- [func trueNegativeCount(of: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/truenegativecount(of:))
- [func truePositiveCount(of: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/truepositivecount(of:))
- [func falseNegativeCount(of: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/falsenegativecount(of:))
- [func falsePositiveCount(of: Label) -> Int](/documentation/createmlcomponents/classificationmetrics/falsepositivecount(of:))
- [func f1Score(label: Label) -> Double](/documentation/createmlcomponents/classificationmetrics/f1score(label:))
- [func mapLabels<T>((Label) throws -> T) rethrows -> ClassificationMetrics<T>](/documentation/createmlcomponents/classificationmetrics/maplabels(_:))

### Updating the metrics

- [func add(some Sequence<(predicted: Label, label: Label)>)](/documentation/createmlcomponents/classificationmetrics/add(_:))
- [func add(predicted: some Sequence<Label>, groundTruth: some Sequence<Label>)](/documentation/createmlcomponents/classificationmetrics/add(predicted:groundtruth:))
- [MultiLabelClassificationMetrics](/documentation/createmlcomponents/multilabelclassificationmetrics)

### Creating the distribution

- [init(some Sequence<(classification: ClassificationDistribution<Label>, labels: Set<Label>)>, strategy: MultiLabelClassificationMetrics<Label>.ThresholdSelectionStrategy) throws](/documentation/createmlcomponents/multilabelclassificationmetrics/init(_:strategy:))
- [init(some Sequence<(classification: ClassificationDistribution<Label>, labels: Set<Label>)>, strategy: MultiLabelClassificationMetrics<Label>.ThresholdSelectionStrategy, labels: Set<Label>) throws](/documentation/createmlcomponents/multilabelclassificationmetrics/init(_:strategy:labels:))
- [init(classifications: some Sequence<ClassificationDistribution<Label>>, groundTruth: some Sequence<Set<Label>>, strategy: MultiLabelClassificationMetrics<Label>.ThresholdSelectionStrategy) throws](/documentation/createmlcomponents/multilabelclassificationmetrics/init(classifications:groundtruth:strategy:))
- [init(classifications: some Sequence<ClassificationDistribution<Label>>, groundTruth: some Sequence<Set<Label>>, strategy: MultiLabelClassificationMetrics<Label>.ThresholdSelectionStrategy, labels: Set<Label>) throws](/documentation/createmlcomponents/multilabelclassificationmetrics/init(classifications:groundtruth:strategy:labels:))
- [init(confidenceThresholds: [Label : Float])](/documentation/createmlcomponents/multilabelclassificationmetrics/init(confidencethresholds:))
- [MultiLabelClassificationMetrics.ThresholdSelectionStrategy](/documentation/createmlcomponents/multilabelclassificationmetrics/thresholdselectionstrategy)

#### Selection strategies

- [case balancedPrecisionAndRecall](/documentation/createmlcomponents/multilabelclassificationmetrics/thresholdselectionstrategy/balancedprecisionandrecall)
- [case fixed([Label : Float])](/documentation/createmlcomponents/multilabelclassificationmetrics/thresholdselectionstrategy/fixed(_:))
- [case precision(Float, minimumRecall: Float)](/documentation/createmlcomponents/multilabelclassificationmetrics/thresholdselectionstrategy/precision(_:minimumrecall:))
- [case recall(Float, minimumPrecision: Float)](/documentation/createmlcomponents/multilabelclassificationmetrics/thresholdselectionstrategy/recall(_:minimumprecision:))

### Getting the properties

- [var confidenceThresholds: [Label : Float]](/documentation/createmlcomponents/multilabelclassificationmetrics/confidencethresholds)
- [var exampleCount: Int](/documentation/createmlcomponents/multilabelclassificationmetrics/examplecount)
- [var labels: Set<Label>](/documentation/createmlcomponents/multilabelclassificationmetrics/labels)
- [var meanAveragePrecision: Float](/documentation/createmlcomponents/multilabelclassificationmetrics/meanaverageprecision)

### Computing and scoring

- [func count(of: Label) -> Int](/documentation/createmlcomponents/multilabelclassificationmetrics/count(of:))
- [func f1Score(for: Label) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/f1score(for:))
- [func falseNegativeCount(of: Label) -> Int](/documentation/createmlcomponents/multilabelclassificationmetrics/falsenegativecount(of:))
- [func falsePositiveCount(of: Label) -> Int](/documentation/createmlcomponents/multilabelclassificationmetrics/falsepositivecount(of:))
- [func precisionScore(for: Label) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/precisionscore(for:))
- [func recallScore(for: Label) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/recallscore(for:))
- [func trueNegativeCount(of: Label) -> Int](/documentation/createmlcomponents/multilabelclassificationmetrics/truenegativecount(of:))
- [func truePositiveCount(of: Label) -> Int](/documentation/createmlcomponents/multilabelclassificationmetrics/truepositivecount(of:))

### Updating the metrics

- [func add(some Sequence<(classification: ClassificationDistribution<Label>, labels: Set<Label>)>)](/documentation/createmlcomponents/multilabelclassificationmetrics/add(_:))
- [func add(classifications: some Sequence<ClassificationDistribution<Label>>, groundTruth: some Sequence<Set<Label>>)](/documentation/createmlcomponents/multilabelclassificationmetrics/add(classifications:groundtruth:))

### Computing the precision

- [static func meanAveragePrecisionScore(some Sequence<(classification: ClassificationDistribution<Label>, labels: Set<Label>)>) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/meanaverageprecisionscore(_:))
- [static func meanAveragePrecisionScore(some Sequence<(classification: ClassificationDistribution<Label>, labels: Set<Label>)>, labels: Set<Label>) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/meanaverageprecisionscore(_:labels:))
- [static func meanAveragePrecisionScore(classifications: some Sequence<ClassificationDistribution<Label>>, groundTruth: some Sequence<Set<Label>>) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/meanaverageprecisionscore(classifications:groundtruth:))
- [static func meanAveragePrecisionScore(classifications: some Sequence<ClassificationDistribution<Label>>, groundTruth: some Sequence<Set<Label>>, labels: Set<Label>) -> Float](/documentation/createmlcomponents/multilabelclassificationmetrics/meanaverageprecisionscore(classifications:groundtruth:labels:))
- [func rootMeanSquaredError<T>([AnnotatedPrediction<T, T>]) -> T](/documentation/createmlcomponents/rootmeansquarederror(_:))
- [func rootMeanSquaredError<T>(some Collection, some Collection) -> T](/documentation/createmlcomponents/rootmeansquarederror(_:_:))
- [func maximumAbsoluteError<T>([AnnotatedPrediction<T, T>]) -> T](/documentation/createmlcomponents/maximumabsoluteerror(_:))
- [func maximumAbsoluteError<T>(some Collection, some Collection) -> T](/documentation/createmlcomponents/maximumabsoluteerror(_:_:))
- [func meanAbsoluteError<T>([AnnotatedPrediction<T, T>]) -> T](/documentation/createmlcomponents/meanabsoluteerror(_:))
- [func meanAbsoluteError<T>(some Collection, some Collection) -> T](/documentation/createmlcomponents/meanabsoluteerror(_:_:))
- [func meanAbsolutePercentageError<T>([AnnotatedPrediction<T, T>]) -> T](/documentation/createmlcomponents/meanabsolutepercentageerror(_:))
- [func meanSquaredError<T>([AnnotatedPrediction<T, T>]) -> T](/documentation/createmlcomponents/meansquarederror(_:))
- [func meanSquaredError<T>(some Collection, some Collection) -> T](/documentation/createmlcomponents/meansquarederror(_:_:))

## Transformer adaptors

- [TransformerToEstimatorAdaptor](/documentation/createmlcomponents/transformertoestimatoradaptor)

### Creating a feature

- [init(Transformer)](/documentation/createmlcomponents/transformertoestimatoradaptor/init(_:))

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/transformertoestimatoradaptor/transformer)

### Encoding and Decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/transformertoestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/transformertoestimatoradaptor/decode(from:))

### Fitting

- [func fitted<S>(to: S, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/transformertoestimatoradaptor/fitted(to:eventhandler:))
- [TransformerToTemporalAdaptor](/documentation/createmlcomponents/transformertotemporaladaptor)

### Creating a transformer

- [init(Base)](/documentation/createmlcomponents/transformertotemporaladaptor/init(_:))

### Applying

- [func applied<S>(to: S, eventHandler: EventHandler?) async throws -> AnyTemporalSequence<TransformerToTemporalAdaptor<Base>.Output>](/documentation/createmlcomponents/transformertotemporaladaptor/applied(to:eventhandler:))
- [TransformerToTemporalAdaptor.Input](/documentation/createmlcomponents/transformertotemporaladaptor/input)
- [TransformerToTemporalAdaptor.Output](/documentation/createmlcomponents/transformertotemporaladaptor/output)
- [TransformerToTemporalAdaptor.OutputSequence](/documentation/createmlcomponents/transformertotemporaladaptor/outputsequence)
- [TransformerToUpdatableEstimatorAdaptor](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor)

### Creating an estimator

- [init(Transformer)](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/init(_:))

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/transformer)

### Encoding and decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/decode(from:))
- [func encodeWithOptimizer(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/decodewithoptimizer(from:))

### Fitting and updating

- [func fitted<S>(to: S, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/fitted(to:eventhandler:))
- [func makeTransformer() -> Transformer](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/maketransformer())
- [func update<InputSequence>(inout Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/transformertoupdatableestimatoradaptor/update(_:with:eventhandler:))

## Updatable adaptors

- [UpdatableEstimatorToTemporalAdaptor](/documentation/createmlcomponents/updatableestimatortotemporaladaptor)

### Creating an adaptor

- [init(Base)](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/init(_:))

### Encoding and decoding

- [func encode(UpdatableEstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> UpdatableEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/decode(from:))
- [func encodeWithOptimizer(UpdatableEstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> UpdatableEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/decodewithoptimizer(from:))

### Fitting and updating

- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> UpdatableEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/fitted(to:eventhandler:))
- [func makeTransformer() -> UpdatableEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/maketransformer())
- [func update<InputSequence>(inout UpdatableEstimatorToTemporalAdaptor<Base>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/update(_:with:eventhandler:))
- [UpdatableEstimatorToTemporalAdaptor.Input](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/input)
- [UpdatableEstimatorToTemporalAdaptor.Output](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/output)
- [UpdatableEstimatorToTemporalAdaptor.Transformer](/documentation/createmlcomponents/updatableestimatortotemporaladaptor/transformer)
- [UpdatableEstimatorToSupervisedAdaptor](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor)

### Creating an adaptor

- [init(Estimator)](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/init(_:))

### Getting the estimator

- [let estimator: Estimator](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/decode(from:))
- [func encodeWithOptimizer(UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/decodewithoptimizer(from:))

### Fitting and Updating

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> UpdatableEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [func makeTransformer() -> Estimator.Transformer](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/maketransformer())
- [func update<InputSequence>(inout Estimator.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/update(_:with:eventhandler:))
- [func update<InputSequence, Validation>(inout Estimator.Transformer, with: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatableestimatortosupervisedadaptor/update(_:with:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [UpdatableSupervisedEstimatorToTemporalAdaptor](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor)

### Creating an adaptor

- [init(Base)](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/init(_:))

### Encoding and decoding

- [func encode(UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/decode(from:))
- [func encodeWithOptimizer(UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/decodewithoptimizer(from:))

### Fitting and updating

- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/fitted(to:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/fitted(to:validateon:eventhandler:))
- [func makeTransformer() -> UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/maketransformer())
- [func update<InputSequence, FeatureSequence>(inout UpdatableSupervisedEstimatorToTemporalAdaptor<Base>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/update(_:with:eventhandler:))
- [UpdatableSupervisedEstimatorToTemporalAdaptor.Annotation](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/annotation)
- [UpdatableSupervisedEstimatorToTemporalAdaptor.Input](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/input)
- [UpdatableSupervisedEstimatorToTemporalAdaptor.Output](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/output)
- [UpdatableSupervisedEstimatorToTemporalAdaptor.Transformer](/documentation/createmlcomponents/updatablesupervisedestimatortotemporaladaptor/transformer)
- [UpdatableTemporalEstimatorToSupervisedAdaptor](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor)

### Creating an adaptor

- [init(Estimator)](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/init(_:))

### Getting the estimator

- [let estimator: Estimator](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/decode(from:))
- [func encodeWithOptimizer(UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/decodewithoptimizer(from:))

### Fitting and updating

- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/fitted(to:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [func makeTransformer() -> Estimator.Transformer](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/maketransformer())
- [func update<InputSequence, FeatureSequence>(inout UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/update(_:with:eventhandler:))
- [func update<InputSequence, Validation, FeatureSequence>(inout UpdatableTemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, with: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatabletemporalestimatortosupervisedadaptor/update(_:with:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

## Estimator adaptors

- [EstimatorToSupervisedAdaptor](/documentation/createmlcomponents/estimatortosupervisedadaptor)

### Creating the adaptor

- [init(Estimator)](/documentation/createmlcomponents/estimatortosupervisedadaptor/init(_:))

### Getting the properties

- [let estimator: Estimator](/documentation/createmlcomponents/estimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(EstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/estimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> EstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/estimatortosupervisedadaptor/decode(from:))

### Fitting a transformer

- [func fitted<Input>(to: Input, eventHandler: EventHandler?) async throws -> EstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/estimatortosupervisedadaptor/fitted(to:eventhandler:))
- [func fitted<Input, Validation>(to: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> EstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/estimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [EstimatorToTemporalAdaptor](/documentation/createmlcomponents/estimatortotemporaladaptor)

### Creating the estimator

- [init(Base)](/documentation/createmlcomponents/estimatortotemporaladaptor/init(_:))

### Encoding and decoding

- [func encode(EstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/estimatortotemporaladaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> EstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/estimatortotemporaladaptor/decode(from:))

### Fitting a transformer

- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> EstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/estimatortotemporaladaptor/fitted(to:eventhandler:))
- [EstimatorToTemporalAdaptor.Input](/documentation/createmlcomponents/estimatortotemporaladaptor/input)
- [EstimatorToTemporalAdaptor.Output](/documentation/createmlcomponents/estimatortotemporaladaptor/output)
- [EstimatorToTemporalAdaptor.Transformer](/documentation/createmlcomponents/estimatortotemporaladaptor/transformer)
- [SupervisedEstimatorToTemporalAdaptor](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor)

### Creating an estimator

- [init(Base)](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/init(_:))

### Encoding and decoding

- [func encode(SupervisedEstimatorToTemporalAdaptor<Base>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> SupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/decode(from:))

### Fitting

- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> SupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/fitted(to:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> SupervisedEstimatorToTemporalAdaptor<Base>.Transformer](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/fitted(to:validateon:eventhandler:))
- [SupervisedEstimatorToTemporalAdaptor.Annotation](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/annotation)
- [SupervisedEstimatorToTemporalAdaptor.Input](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/input)
- [SupervisedEstimatorToTemporalAdaptor.Output](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/output)
- [SupervisedEstimatorToTemporalAdaptor.Transformer](/documentation/createmlcomponents/supervisedestimatortotemporaladaptor/transformer)

## Tabular adaptors

- [TabularEstimatorToSupervisedAdaptor](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor)

### Creating an adaptor

- [init(Estimator, annotationColumnID: ColumnID<Annotation>)](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/init(_:annotationcolumnid:))

### Getting the properties

- [var annotationColumnID: ColumnID<Annotation>](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/annotationcolumnid)
- [let estimator: Estimator](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(Estimator.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Estimator.Transformer](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/decode(from:))

### Fitting

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> Estimator.Transformer](/documentation/createmlcomponents/tabularestimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [TabularTransformerToEstimatorAdaptor](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor)

### Creating an estimator

- [init(Transformer)](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor/init(_:))

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor/transformer)

### Encoding and decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor/decode(from:))

### Fitting

- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/tabulartransformertoestimatoradaptor/fitted(to:eventhandler:))
- [TabularTransformerToUpdatableEstimatorAdaptor](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor)

### Creating an estimator

- [init(Transformer)](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/init(_:))

### Creating a default transformer

- [func makeTransformer() -> Transformer](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/maketransformer())

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/transformer)

### Encoding and decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/decode(from:))
- [func encodeWithOptimizer(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/decodewithoptimizer(from:))

### Fitting

- [func fitted(to: DataFrame, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/fitted(to:eventhandler:))
- [func update(inout Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/tabulartransformertoupdatableestimatoradaptor/update(_:with:eventhandler:))
- [UpdatableTabularEstimatorToSupervisedAdaptor](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor)

### Creating an adaptor

- [init(Estimator, annotationColumnID: ColumnID<Annotation>)](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/init(_:annotationcolumnid:))

### Getting the properties

- [var annotationColumnID: ColumnID<Annotation>](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/annotationcolumnid)
- [let estimator: Estimator](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/decode(from:))
- [func encodeWithOptimizer(UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/decodewithoptimizer(from:))

### Fitting

- [func fitted(to: DataFrame, validateOn: DataFrame?, eventHandler: EventHandler?) async throws -> UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [func makeTransformer() -> Estimator.Transformer](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/maketransformer())
- [func update(inout UpdatableTabularEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, with: DataFrame, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/updatabletabularestimatortosupervisedadaptor/update(_:with:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

## Temporal adaptors

- [TemporalAdaptor](/documentation/createmlcomponents/temporaladaptor)

### Creating a temporal adaptor

- [init(Base)](/documentation/createmlcomponents/temporaladaptor/init(_:))

### Applying a temporal adapter

- [func applied(to: some TemporalSequence<Base.Input>, eventHandler: EventHandler?) async throws -> AnyTemporalSequence<TemporalAdaptor<Base>.Output>](/documentation/createmlcomponents/temporaladaptor/applied(to:eventhandler:))

### Supporting types

- [TemporalAdaptor.Input](/documentation/createmlcomponents/temporaladaptor/input)
- [TemporalAdaptor.Output](/documentation/createmlcomponents/temporaladaptor/output)
- [TemporalAdaptor.OutputSequence](/documentation/createmlcomponents/temporaladaptor/outputsequence)
- [TemporalTransformerToEstimatorAdaptor](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor)

### Creating an estimator

- [init(Transformer)](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor/init(_:))

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor/transformer)

### Encoding and decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor/decode(from:))

### Fitting

- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/temporaltransformertoestimatoradaptor/fitted(to:eventhandler:))
- [TemporalEstimatorToSupervisedAdaptor](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor)

### Creating an adaptor

- [init(Estimator)](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/init(_:))

### Getting the estimator

- [let estimator: Estimator](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/estimator)

### Encoding and decoding

- [func encode(TemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> TemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/decode(from:))

### Fitting

- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> TemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/fitted(to:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> TemporalEstimatorToSupervisedAdaptor<Estimator, Annotation>.Transformer](/documentation/createmlcomponents/temporalestimatortosupervisedadaptor/fitted(to:validateon:eventhandler:))
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [TemporalTransformerToUpdatableEstimatorAdaptor](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor)

### Creating an estimator

- [init(Transformer)](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/init(_:))

### Getting the transformer

- [let transformer: Transformer](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/transformer)

### Encoding and decoding

- [func encode(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/encode(_:to:))
- [func decode(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/decode(from:))
- [func encodeWithOptimizer(Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> Transformer](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/decodewithoptimizer(from:))

### Fitting and updating

- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> Transformer](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/fitted(to:eventhandler:))
- [func makeTransformer() -> Transformer](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/maketransformer())
- [func update<InputSequence>(inout Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/temporaltransformertoupdatableestimatoradaptor/update(_:with:eventhandler:))

## Composition with preprocessing

- [PreprocessingEstimator](/documentation/createmlcomponents/preprocessingestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingestimator/preprocessor)

### Preprocesing and fitting

- [func preprocessed<S>(from: S, eventHandler: EventHandler?) async throws -> [Preprocessor.Output]](/documentation/createmlcomponents/preprocessingestimator/preprocessed(from:eventhandler:))
- [func fitted<S>(to: S, eventHandler: EventHandler?) async throws -> PreprocessingEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingestimator/fitted(to:eventhandler:))
- [func fitted<S>(toPreprocessed: S, eventHandler: EventHandler?) async throws -> PreprocessingEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingestimator/fitted(topreprocessed:eventhandler:))
- [PreprocessingEstimator.Input](/documentation/createmlcomponents/preprocessingestimator/input)
- [PreprocessingEstimator.Intermediate](/documentation/createmlcomponents/preprocessingestimator/intermediate)
- [PreprocessingEstimator.Output](/documentation/createmlcomponents/preprocessingestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingTemporalEstimator](/documentation/createmlcomponents/preprocessingtemporalestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingtemporalestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingtemporalestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingtemporalestimator/preprocessor)

### Preprocesing and fitting

- [func preprocessed<InputSequence>(from: InputSequence, eventHandler: EventHandler?) async throws -> [PreprocessedFeatureSequence<Preprocessor.Output>]](/documentation/createmlcomponents/preprocessingtemporalestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingtemporalestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: [PreprocessedFeatureSequence<Preprocessor.Output>], eventHandler: EventHandler?) async throws -> PreprocessingTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingtemporalestimator/fitted(topreprocessed:eventhandler:))
- [PreprocessingTemporalEstimator.Input](/documentation/createmlcomponents/preprocessingtemporalestimator/input)
- [PreprocessingTemporalEstimator.Intermediate](/documentation/createmlcomponents/preprocessingtemporalestimator/intermediate)
- [PreprocessingTemporalEstimator.Output](/documentation/createmlcomponents/preprocessingtemporalestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingSupervisedEstimator](/documentation/createmlcomponents/preprocessingsupervisedestimator)

### Creating the estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingsupervisedestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingsupervisedestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingsupervisedestimator/preprocessor)

### Preprocessing and fitting

- [func preprocessed<S>(from: S, eventHandler: EventHandler?) async throws -> AnySequence<AnnotatedFeature<Preprocessor.Output, PreprocessingSupervisedEstimator<Preprocessor, Estimator>.Annotation>>](/documentation/createmlcomponents/preprocessingsupervisedestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedestimator/fitted(to:eventhandler:))
- [func fitted<S>(toPreprocessed: S, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedestimator/fitted(topreprocessed:eventhandler:))
- [func fitted<InputSequence, Validation>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedestimator/fitted(to:validateon:eventhandler:))
- [func fitted<Input, Validation>(toPreprocessed: Input, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedestimator/fitted(topreprocessed:validateon:eventhandler:))
- [PreprocessingSupervisedEstimator.Annotation](/documentation/createmlcomponents/preprocessingsupervisedestimator/annotation)
- [PreprocessingSupervisedEstimator.Input](/documentation/createmlcomponents/preprocessingsupervisedestimator/input)
- [PreprocessingSupervisedEstimator.Intermediate](/documentation/createmlcomponents/preprocessingsupervisedestimator/intermediate)
- [PreprocessingSupervisedEstimator.Output](/documentation/createmlcomponents/preprocessingsupervisedestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingSupervisedTemporalEstimator](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/preprocessor)

### Preprocesing and Fitting

- [func preprocessed<InputSequence, FeatureSequence>(from: InputSequence, eventHandler: EventHandler?) async throws -> [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>]](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/fitted(topreprocessed:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/fitted(to:validateon:eventhandler:))
- [func fitted(toPreprocessed: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], validateOn: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], eventHandler: EventHandler?) async throws -> PreprocessingSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/fitted(topreprocessed:validateon:eventhandler:))
- [PreprocessingSupervisedTemporalEstimator.Annotation](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/annotation)
- [PreprocessingSupervisedTemporalEstimator.Input](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/input)
- [PreprocessingSupervisedTemporalEstimator.Intermediate](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/intermediate)
- [PreprocessingSupervisedTemporalEstimator.Output](/documentation/createmlcomponents/preprocessingsupervisedtemporalestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableEstimator](/documentation/createmlcomponents/preprocessingupdatableestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatableestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatableestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatableestimator/preprocessor)

### Encoding and decoding

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatableestimator/decodewithoptimizer(from:))
- [func encodeWithOptimizer(PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatableestimator/encodewithoptimizer(_:to:))

### Preprocesing and fitting

- [func preprocessed<S>(from: S, eventHandler: EventHandler?) async throws -> [Preprocessor.Output]](/documentation/createmlcomponents/preprocessingupdatableestimator/preprocessed(from:eventhandler:))
- [func fitted<S>(to: S, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatableestimator/fitted(to:eventhandler:))
- [func fitted<S>(toPreprocessed: S, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatableestimator/fitted(topreprocessed:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatableestimator/maketransformer())
- [func update<InputSequence>(inout PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatableestimator/update(_:with:eventhandler:))
- [func update<InputSequence>(inout PreprocessingUpdatableEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatableestimator/update(_:withpreprocessed:eventhandler:))
- [PreprocessingUpdatableEstimator.Input](/documentation/createmlcomponents/preprocessingupdatableestimator/input)
- [PreprocessingUpdatableEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatableestimator/intermediate)
- [PreprocessingUpdatableEstimator.Output](/documentation/createmlcomponents/preprocessingupdatableestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableTemporalEstimator](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/preprocessor)

### Encoding and decoding

- [func encodeWithOptimizer(PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/encodewithoptimizer(_:to:))
- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/decodewithoptimizer(from:))

### Preprocesing and fitting

- [func preprocessed<InputSequence>(from: InputSequence, eventHandler: EventHandler?) async throws -> [PreprocessedFeatureSequence<Preprocessor.Output>]](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: [PreprocessedFeatureSequence<Preprocessor.Output>], eventHandler: EventHandler?) async throws -> PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/fitted(topreprocessed:eventhandler:))
- [func update<InputSequence>(inout PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/update(_:withpreprocessed:eventhandler:))
- [func update<InputSequence>(inout PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/update(_:with:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/maketransformer())
- [PreprocessingUpdatableTemporalEstimator.Input](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/input)
- [PreprocessingUpdatableTemporalEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/intermediate)
- [PreprocessingUpdatableTemporalEstimator.Output](/documentation/createmlcomponents/preprocessingupdatabletemporalestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableSupervisedEstimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator)

### Creating the estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/preprocessor)

### Encoding and decoding

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/decodewithoptimizer(from:))
- [func encodeWithOptimizer(PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/encodewithoptimizer(_:to:))

### Preprocesing and fitting

- [func preprocessed<S>(from: S, eventHandler: EventHandler?) async throws -> AnySequence<AnnotatedFeature<Preprocessor.Output, PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Annotation>>](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/fitted(to:eventhandler:))
- [func fitted<S>(toPreprocessed: S, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/fitted(topreprocessed:eventhandler:))
- [func fitted<InputSequence, Validation>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/fitted(to:validateon:eventhandler:))
- [func fitted<InputSequence, Validation>(toPreprocessed: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/fitted(topreprocessed:validateon:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/maketransformer())
- [func update<InputSequence>(inout PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/update(_:with:eventhandler:))
- [func update<InputSequence>(inout PreprocessingUpdatableSupervisedEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/update(_:withpreprocessed:eventhandler:))
- [PreprocessingUpdatableSupervisedEstimator.Annotation](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/annotation)
- [PreprocessingUpdatableSupervisedEstimator.Input](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/input)
- [PreprocessingUpdatableSupervisedEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/intermediate)
- [PreprocessingUpdatableSupervisedEstimator.Output](/documentation/createmlcomponents/preprocessingupdatablesupervisedestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))
- [PreprocessingUpdatableSupervisedTemporalEstimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator)

### Creating an estimator

- [init(Preprocessor, Estimator)](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/init(_:_:))

### Getting the properties

- [var estimator: Estimator](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/estimator)
- [var preprocessor: Preprocessor](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/preprocessor)

### Encoding and decoding

- [func decodeWithOptimizer(from: inout any EstimatorDecoder) throws -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/decodewithoptimizer(from:))
- [func encodeWithOptimizer(PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer, to: inout any EstimatorEncoder) throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/encodewithoptimizer(_:to:))

### Preprocesing and fitting

- [func preprocessed<InputSequence, FeatureSequence>(from: InputSequence, eventHandler: EventHandler?) async throws -> [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>]](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/preprocessed(from:eventhandler:))
- [func fitted<InputSequence, FeatureSequence>(to: InputSequence, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/fitted(to:eventhandler:))
- [func fitted(toPreprocessed: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/fitted(topreprocessed:eventhandler:))
- [func fitted<InputSequence, Validation, FeatureSequence>(to: InputSequence, validateOn: Validation, eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/fitted(to:validateon:eventhandler:))
- [func fitted(toPreprocessed: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], validateOn: [AnnotatedFeature<PreprocessedFeatureSequence<Preprocessor.Output>, PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Annotation>], eventHandler: EventHandler?) async throws -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/fitted(topreprocessed:validateon:eventhandler:))
- [func makeTransformer() -> PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/maketransformer())
- [func update<InputSequence, FeatureSequence>(inout PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer, with: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/update(_:with:eventhandler:))
- [func update<InputSequence, FeatureSequence>(inout PreprocessingUpdatableSupervisedTemporalEstimator<Preprocessor, Estimator>.Transformer, withPreprocessed: InputSequence, eventHandler: EventHandler?) async throws](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/update(_:withpreprocessed:eventhandler:))
- [PreprocessingUpdatableSupervisedTemporalEstimator.Annotation](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/annotation)
- [PreprocessingUpdatableSupervisedTemporalEstimator.Input](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/input)
- [PreprocessingUpdatableSupervisedTemporalEstimator.Intermediate](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/intermediate)
- [PreprocessingUpdatableSupervisedTemporalEstimator.Output](/documentation/createmlcomponents/preprocessingupdatablesupervisedtemporalestimator/output)
- [Transformer](/documentation/createmlcomponents/transformer)

#### Applying and adapting

- [func applied(to: Self.Input, eventHandler: EventHandler?) async throws -> Self.Output](/documentation/createmlcomponents/transformer/applied(to:eventhandler:))
- [func adaptedAsAnnotatedFeatureTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedFeature<Self.Input, Annotation>, AnnotatedFeature<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedfeaturetransformer(annotationtype:))
- [func adaptedAsAnnotatedPredictionTransformer<Annotation>(annotationType: Annotation.Type) -> some Transformer<AnnotatedPrediction<Self.Input, Annotation>, AnnotatedPrediction<Self.Output, Annotation>>
](/documentation/createmlcomponents/transformer/adaptedasannotatedpredictiontransformer(annotationtype:))
- [func adaptedAsEstimator() -> TransformerToEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasestimator())
- [func adaptedAsRandomTransformer() -> some RandomTransformer<Self.Input, Self.Output>
](/documentation/createmlcomponents/transformer/adaptedasrandomtransformer())
- [func adaptedAsTemporal()](/documentation/createmlcomponents/transformer/adaptedastemporal())
- [func adaptedAsUpdatableEstimator() -> TransformerToUpdatableEstimatorAdaptor<Self>](/documentation/createmlcomponents/transformer/adaptedasupdatableestimator())
- [Input](/documentation/createmlcomponents/transformer/input)
- [Output](/documentation/createmlcomponents/transformer/output)

#### Appending

- [func appending(_:)](/documentation/createmlcomponents/transformer/appending(_:))

#### Transforming and predicting

- [func callAsFunction(_:eventHandler:)](/documentation/createmlcomponents/transformer/callasfunction(_:eventhandler:))
- [func prediction(from:)](/documentation/createmlcomponents/transformer/prediction(from:))
- [func prediction<S, Annotation>(from: S, eventHandler: EventHandler?) async throws -> [AnnotatedPrediction<Self.Output, Annotation>]](/documentation/createmlcomponents/transformer/prediction(from:eventhandler:))

#### Exporting

- [func export(to: URL) throws](/documentation/createmlcomponents/transformer/export(to:))
- [func export(to: URL, metadata: ModelMetadata) throws](/documentation/createmlcomponents/transformer/export(to:metadata:))

## Composition

- [ComposedTransformer](/documentation/createmlcomponents/composedtransformer)

### Creating the transformer

- [init(Inner, Outer)](/documentation/createmlcomponents/composedtransformer/init(_:_:))

### Getting the properties

- [var inner: Inner](/documentation/createmlcomponents/composedtransformer/inner)
- [var outer: Outer](/documentation/createmlcomponents/composedtransformer/outer)

### Performing the transformation

- [func applied(to: ComposedTransformer<Inner, Outer>.Input, eventHandler: EventHandler?) async throws -> ComposedTransformer<Inner, Outer>.Output](/documentation/createmlcomponents/composedtransformer/applied(to:eventhandler:))
- [ComposedTransformer.Input](/documentation/createmlcomponents/composedtransformer/input)
- [ComposedTransformer.Intermediate](/documentation/createmlcomponents/composedtransformer/intermediate)
- [ComposedTransformer.Output](/documentation/createmlcomponents/composedtransformer/output)
- [ComposedTemporalTransformer](/documentation/createmlcomponents/composedtemporaltransformer)

### Creating the transformer

- [init(Inner, Outer)](/documentation/createmlcomponents/composedtemporaltransformer/init(_:_:))

### Getting the properties

- [var inner: Inner](/documentation/createmlcomponents/composedtemporaltransformer/inner)
- [var outer: Outer](/documentation/createmlcomponents/composedtemporaltransformer/outer)

### Applying a transformer

- [func applied<S>(to: S, eventHandler: EventHandler?) async throws -> ComposedTemporalTransformer<Inner, Outer>.OutputSequence](/documentation/createmlcomponents/composedtemporaltransformer/applied(to:eventhandler:))
- [ComposedTemporalTransformer.Intermediate](/documentation/createmlcomponents/composedtemporaltransformer/intermediate)
- [ComposedTemporalTransformer.Input](/documentation/createmlcomponents/composedtemporaltransformer/input)
- [ComposedTemporalTransformer.Output](/documentation/createmlcomponents/composedtemporaltransformer/output)
- [ComposedTemporalTransformer.OutputSequence](/documentation/createmlcomponents/composedtemporaltransformer/outputsequence)
- [ComposedTabularTransformer](/documentation/createmlcomponents/composedtabulartransformer)

### Creating the transformer

- [init(Inner, Outer)](/documentation/createmlcomponents/composedtabulartransformer/init(_:_:))

### Getting the properties

- [var inner: Inner](/documentation/createmlcomponents/composedtabulartransformer/inner)
- [var outer: Outer](/documentation/createmlcomponents/composedtabulartransformer/outer)

### Applying a transformation

- [func applied(to: DataFrame, eventHandler: EventHandler?) async throws -> DataFrame](/documentation/createmlcomponents/composedtabulartransformer/applied(to:eventhandler:))

## Errors

- [AudioPreprocessingError](/documentation/createmlcomponents/audiopreprocessingerror)

### Analyzing the error

- [case incompatibleTargetFormatForConversion(inputFormat: AVAudioFormat, targetFormat: AVAudioFormat)](/documentation/createmlcomponents/audiopreprocessingerror/incompatibletargetformatforconversion(inputformat:targetformat:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/audiopreprocessingerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/audiopreprocessingerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/audiopreprocessingerror/debugdescription)
- [AudioReaderError](/documentation/createmlcomponents/audioreadererror)

### Analyzing the error

- [case microphoneAuthorizationDenied](/documentation/createmlcomponents/audioreadererror/microphoneauthorizationdenied)
- [case microphoneAuthorizationRestricted](/documentation/createmlcomponents/audioreadererror/microphoneauthorizationrestricted)
- [case sourceDeviceNotAvailable](/documentation/createmlcomponents/audioreadererror/sourcedevicenotavailable)

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/audioreadererror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/audioreadererror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/audioreadererror/debugdescription)
- [CompatibilityError](/documentation/createmlcomponents/compatibilityerror)

### Analyzing the Error

- [case unsupportedRevision(Int)](/documentation/createmlcomponents/compatibilityerror/unsupportedrevision(_:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/compatibilityerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/compatibilityerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/compatibilityerror/debugdescription)
- [ConcatenationError](/documentation/createmlcomponents/concatenationerror)

### Analyzing the error

- [case mismatchedShapes](/documentation/createmlcomponents/concatenationerror/mismatchedshapes)
- [case nonUniformShapes(columnName: String)](/documentation/createmlcomponents/concatenationerror/nonuniformshapes(columnname:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/concatenationerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/concatenationerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/concatenationerror/debugdescription)
- [DatasetError](/documentation/createmlcomponents/dataseterror)

### Analyzing the error

- [case incompatibleDataFormat(URL, debugDescription: String)](/documentation/createmlcomponents/dataseterror/incompatibledataformat(_:debugdescription:))
- [case incorrectName(URL, debugDescription: String)](/documentation/createmlcomponents/dataseterror/incorrectname(_:debugdescription:))
- [case missingResource(URL)](/documentation/createmlcomponents/dataseterror/missingresource(_:))
- [case unreadableResource(URL)](/documentation/createmlcomponents/dataseterror/unreadableresource(_:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/dataseterror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/dataseterror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/dataseterror/debugdescription)
- [EstimatorEncodingError](/documentation/createmlcomponents/estimatorencodingerror)

### Analyzing the error

- [case invalidState(debugDescription: String)](/documentation/createmlcomponents/estimatorencodingerror/invalidstate(debugdescription:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/estimatorencodingerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/estimatorencodingerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/estimatorencodingerror/debugdescription)
- [ModelCompatibilityError](/documentation/createmlcomponents/modelcompatibilityerror)

### Analyzing the error

- [case incompatibleInputCount(expected: Int, actual: Int)](/documentation/createmlcomponents/modelcompatibilityerror/incompatibleinputcount(expected:actual:))
- [case incompatibleInputDataFormat(expected: MLFeatureType, actual: MLFeatureType)](/documentation/createmlcomponents/modelcompatibilityerror/incompatibleinputdataformat(expected:actual:))
- [case incompatibleInputMultiArrayDataType(MLMultiArrayDataType)](/documentation/createmlcomponents/modelcompatibilityerror/incompatibleinputmultiarraydatatype(_:))
- [case incompatibleLabelType](/documentation/createmlcomponents/modelcompatibilityerror/incompatiblelabeltype)
- [case incompatibleMetadataKey(name: String)](/documentation/createmlcomponents/modelcompatibilityerror/incompatiblemetadatakey(name:))
- [case incompatibleOutputCount(expected: Int, actual: Int)](/documentation/createmlcomponents/modelcompatibilityerror/incompatibleoutputcount(expected:actual:))
- [case incompatibleOutputDataFormat(expected: MLFeatureType, actual: MLFeatureType)](/documentation/createmlcomponents/modelcompatibilityerror/incompatibleoutputdataformat(expected:actual:))
- [case missingInput(name: String)](/documentation/createmlcomponents/modelcompatibilityerror/missinginput(name:))
- [case missingLabel](/documentation/createmlcomponents/modelcompatibilityerror/missinglabel)
- [case missingLabelProbabilities](/documentation/createmlcomponents/modelcompatibilityerror/missinglabelprobabilities)
- [case missingOutput(name: String)](/documentation/createmlcomponents/modelcompatibilityerror/missingoutput(name:))
- [case missingPredictedFeature](/documentation/createmlcomponents/modelcompatibilityerror/missingpredictedfeature)

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/modelcompatibilityerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/modelcompatibilityerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/modelcompatibilityerror/debugdescription)
- [ModelUpdateError](/documentation/createmlcomponents/modelupdateerror)

### Analyzing the error

- [case invalidState(debugDescription: String)](/documentation/createmlcomponents/modelupdateerror/invalidstate(debugdescription:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/modelupdateerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/modelupdateerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/modelupdateerror/debugdescription)
- [OptimizationError](/documentation/createmlcomponents/optimizationerror)

### Analyzing the error

- [case numericOverflow](/documentation/createmlcomponents/optimizationerror/numericoverflow)
- [case numericUnderflow](/documentation/createmlcomponents/optimizationerror/numericunderflow)
- [case unsupportedPlatform](/documentation/createmlcomponents/optimizationerror/unsupportedplatform)

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/optimizationerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/optimizationerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/optimizationerror/debugdescription)
- [PipelineDataError](/documentation/createmlcomponents/pipelinedataerror)

### Analyzing the error

- [case emptyInput(operation: String)](/documentation/createmlcomponents/pipelinedataerror/emptyinput(operation:))
- [case incompatibleConfiguration(operation: String, debugDescription: String)](/documentation/createmlcomponents/pipelinedataerror/incompatibleconfiguration(operation:debugdescription:))
- [case incompatibleDataFormat(operation: String, debugDescription: String)](/documentation/createmlcomponents/pipelinedataerror/incompatibledataformat(operation:debugdescription:))
- [case incompatibleShape([Int], debugDescription: String)](/documentation/createmlcomponents/pipelinedataerror/incompatibleshape(_:debugdescription:))
- [case missingAnnotation(operation: String)](/documentation/createmlcomponents/pipelinedataerror/missingannotation(operation:))
- [case missingValue(operation: String)](/documentation/createmlcomponents/pipelinedataerror/missingvalue(operation:))
- [case unrecognizedCategory(operation: String, category: String)](/documentation/createmlcomponents/pipelinedataerror/unrecognizedcategory(operation:category:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/pipelinedataerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/pipelinedataerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/pipelinedataerror/debugdescription)
- [SerializationError](/documentation/createmlcomponents/serializationerror)

### Analyzing the error

- [case notRepresentableAsCoreML(debugDescription: String)](/documentation/createmlcomponents/serializationerror/notrepresentableascoreml(debugdescription:))
- [case packageAlreadyExists(URL)](/documentation/createmlcomponents/serializationerror/packagealreadyexists(_:))
- [case packageNotFound(URL)](/documentation/createmlcomponents/serializationerror/packagenotfound(_:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/serializationerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/serializationerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/serializationerror/debugdescription)
- [TabularPipelineDataError](/documentation/createmlcomponents/tabularpipelinedataerror)

### Getting the cases

- [case incorrectType(operation: String, columnName: String, actual: String, expected: String)](/documentation/createmlcomponents/tabularpipelinedataerror/incorrecttype(operation:columnname:actual:expected:))
- [case missingColumn(operation: String, columnName: String)](/documentation/createmlcomponents/tabularpipelinedataerror/missingcolumn(operation:columnname:))
- [case missingValues(operation: String, columnName: String)](/documentation/createmlcomponents/tabularpipelinedataerror/missingvalues(operation:columnname:))

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/tabularpipelinedataerror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/tabularpipelinedataerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/tabularpipelinedataerror/debugdescription)
- [VideoReaderError](/documentation/createmlcomponents/videoreadererror)

### Analyzing the error

- [case cameraAuthorizationDenied](/documentation/createmlcomponents/videoreadererror/cameraauthorizationdenied)
- [case cameraAuthorizationRestricted](/documentation/createmlcomponents/videoreadererror/cameraauthorizationrestricted)
- [case frameRateNotSupported(Double)](/documentation/createmlcomponents/videoreadererror/frameratenotsupported(_:))
- [case missingVideoTrack(URL)](/documentation/createmlcomponents/videoreadererror/missingvideotrack(_:))
- [case sourceCameraNotAvailable](/documentation/createmlcomponents/videoreadererror/sourcecameranotavailable)
- [case captureSessionStopped](/documentation/createmlcomponents/videoreadererror/capturesessionstopped)

### Getting the debug description

- [var debugDescription: String](/documentation/createmlcomponents/videoreadererror/debugdescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createmlcomponents/videoreadererror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createmlcomponents/videoreadererror/debugdescription)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
