# Create ML Documentation

Source: https://sosumi.ai/documentation/createml

---
title: Create ML
source: https://developer.apple.com/documentation/createml
timestamp: 2026-02-13T18:55:56.333Z
---

## Image models

- [Creating an Image Classifier Model](/documentation/createml/creating-an-image-classifier-model)
- [MLImageClassifier](/documentation/createml/mlimageclassifier)

### Training an image classifier asynchronously

- [static func makeTrainingSession(trainingData: MLImageClassifier.DataSource, parameters: MLImageClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLImageClassifier>](/documentation/createml/mlimageclassifier/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func train(trainingData: MLImageClassifier.DataSource, parameters: MLImageClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLImageClassifier>](/documentation/createml/mlimageclassifier/train(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLImageClassifier>) throws -> MLJob<MLImageClassifier>](/documentation/createml/mlimageclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLImageClassifier>](/documentation/createml/mlimageclassifier/restoretrainingsession(sessionparameters:))

### Creating an image classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlimageclassifier/init(checkpoint:))

### Training an image classifier synchronously

- [init(trainingData:parameters:)](/documentation/createml/mlimageclassifier/init(trainingdata:parameters:))

### Evaluating an image classifier

- [func evaluation(on:)](/documentation/createml/mlimageclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlimageclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlimageclassifier/validationmetrics)

### Testing an image classifier

- [func prediction(from:)](/documentation/createml/mlimageclassifier/prediction(from:))
- [func predictions(from: [URL]) throws -> [String]](/documentation/createml/mlimageclassifier/predictions(from:))

### Saving an image classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlimageclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlimageclassifier/write(tofile:metadata:))

### Inspecting an image classifier model

- [var model: MLModel](/documentation/createml/mlimageclassifier/model)
- [let modelParameters: MLImageClassifier.ModelParameters](/documentation/createml/mlimageclassifier/modelparameters-swift.property)

### Describing an image classifier

- [var description: String](/documentation/createml/mlimageclassifier/description)
- [var debugDescription: String](/documentation/createml/mlimageclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/playgrounddescription)

### Supporting types

- [MLImageClassifier.DataSource](/documentation/createml/mlimageclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlimageclassifier/datasource/labeleddirectories(at:))
- [case labeledFiles(at: URL)](/documentation/createml/mlimageclassifier/datasource/labeledfiles(at:))

#### Retrieving the data

- [func labeledImages() throws -> [String : [URL]]](/documentation/createml/mlimageclassifier/datasource/labeledimages())
- [case filesByLabel([String : [URL]])](/documentation/createml/mlimageclassifier/datasource/filesbylabel(_:))

#### Splitting the data

- [func stratifiedSplit(proportions: [Double], seed: Int) throws -> [[String : [URL]]]](/documentation/createml/mlimageclassifier/datasource/stratifiedsplit(proportions:seed:))
- [func stratifiedSplit<RNG>(proportions: [Double], generator: inout RNG) throws -> [[String : [URL]]]](/documentation/createml/mlimageclassifier/datasource/stratifiedsplit(proportions:generator:))
- [MLImageClassifier.ModelParameters](/documentation/createml/mlimageclassifier/modelparameters-swift.struct)

#### Creating parameters

- [init(validation: MLImageClassifier.ModelParameters.ValidationData, maxIterations: Int, augmentation: MLImageClassifier.ImageAugmentationOptions, algorithm: MLImageClassifier.ModelParameters.ModelAlgorithmType)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/init(validation:maxiterations:augmentation:algorithm:))
- [init(featureExtractor: MLImageClassifier.FeatureExtractorType, validation: MLImageClassifier.ModelParameters.ValidationData, maxIterations: Int, augmentationOptions: MLImageClassifier.ImageAugmentationOptions)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/init(featureextractor:validation:maxiterations:augmentationoptions:))
- [init(featureExtractor:validationData:maxIterations:augmentationOptions:)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/init(featureextractor:validationdata:maxiterations:augmentationoptions:))
- [MLImageClassifier.ModelParameters.ClassifierType](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/classifiertype)

##### Designating an algorithm’s classifier

- [case logisticRegressor](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/classifiertype/logisticregressor)
- [case multilayerPerceptron(layerSizes: [Int])](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/classifiertype/multilayerperceptron(layersizes:))
- [MLImageClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/modelalgorithmtype)

##### Designating an algorithm type

- [case transferLearning(featureExtractor: MLImageClassifier.FeatureExtractorType, classifier: MLImageClassifier.ModelParameters.ClassifierType)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/modelalgorithmtype/transferlearning(featureextractor:classifier:))

#### Accessing the training parameters

- [var algorithm: MLImageClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/algorithm)
- [var featureExtractor: MLImageClassifier.FeatureExtractorType](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/featureextractor)
- [var validation: MLImageClassifier.ModelParameters.ValidationData](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validation)
- [var maxIterations: Int](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/maxiterations)
- [var augmentationOptions: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/augmentationoptions)
- [var validationData: [String : [URL]]?](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.property)

#### Describing parameters

- [var description: String](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/playgrounddescription)

#### Supporting types

- [MLImageClassifier.FeatureExtractorType](/documentation/createml/mlimageclassifier/featureextractortype)

##### Selecting a feature extractor type

- [case scenePrint(revision: Int?)](/documentation/createml/mlimageclassifier/featureextractortype/sceneprint(revision:))
- [case custom(MLImageClassifier.CustomFeatureExtractor)](/documentation/createml/mlimageclassifier/featureextractortype/custom(_:))
- [MLImageClassifier.CustomFeatureExtractor](/documentation/createml/mlimageclassifier/customfeatureextractor)

###### Creating a custom feature extractor

- [init(modelPath: URL, outputName: String?)](/documentation/createml/mlimageclassifier/customfeatureextractor/init(modelpath:outputname:))

###### Configuring a custom feature extractor

- [var modelPath: URL](/documentation/createml/mlimageclassifier/customfeatureextractor/modelpath)
- [var outputName: String?](/documentation/createml/mlimageclassifier/customfeatureextractor/outputname)

##### Describing a feature extractor type

- [var description: String](/documentation/createml/mlimageclassifier/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mlimageclassifier/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/featureextractortype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlimageclassifier/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlimageclassifier/featureextractortype/description)
- [MLImageClassifier.ModelParameters.ValidationData](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.enum)

##### Designating validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case dataSource(MLImageClassifier.DataSource)](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.enum/datasource(_:))
- [case dictionary([String : [URL]])](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.enum/dictionary(_:))
- [case none](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)
- [MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions)

##### Selecting augmentation options

- [static let crop: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/crop)
- [static let rotation: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/rotation)
- [static let blur: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/blur)
- [static let exposure: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/exposure)
- [static let noise: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/noise)
- [static let flip: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/flip)

##### Creating augmentation options

- [init(rawValue: Int)](/documentation/createml/mlimageclassifier/imageaugmentationoptions/init(rawvalue:))

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlimageclassifier/modelparameters-swift.struct/description)
- [MLImageClassifier.FeatureExtractorType](/documentation/createml/mlimageclassifier/featureextractortype)

#### Selecting a feature extractor type

- [case scenePrint(revision: Int?)](/documentation/createml/mlimageclassifier/featureextractortype/sceneprint(revision:))
- [case custom(MLImageClassifier.CustomFeatureExtractor)](/documentation/createml/mlimageclassifier/featureextractortype/custom(_:))
- [MLImageClassifier.CustomFeatureExtractor](/documentation/createml/mlimageclassifier/customfeatureextractor)

##### Creating a custom feature extractor

- [init(modelPath: URL, outputName: String?)](/documentation/createml/mlimageclassifier/customfeatureextractor/init(modelpath:outputname:))

##### Configuring a custom feature extractor

- [var modelPath: URL](/documentation/createml/mlimageclassifier/customfeatureextractor/modelpath)
- [var outputName: String?](/documentation/createml/mlimageclassifier/customfeatureextractor/outputname)

#### Describing a feature extractor type

- [var description: String](/documentation/createml/mlimageclassifier/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mlimageclassifier/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/featureextractortype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlimageclassifier/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlimageclassifier/featureextractortype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlimageclassifier/featureextractortype/description)
- [MLImageClassifier.CustomFeatureExtractor](/documentation/createml/mlimageclassifier/customfeatureextractor)

#### Creating a custom feature extractor

- [init(modelPath: URL, outputName: String?)](/documentation/createml/mlimageclassifier/customfeatureextractor/init(modelpath:outputname:))

#### Configuring a custom feature extractor

- [var modelPath: URL](/documentation/createml/mlimageclassifier/customfeatureextractor/modelpath)
- [var outputName: String?](/documentation/createml/mlimageclassifier/customfeatureextractor/outputname)
- [MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions)

#### Selecting augmentation options

- [static let crop: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/crop)
- [static let rotation: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/rotation)
- [static let blur: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/blur)
- [static let exposure: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/exposure)
- [static let noise: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/noise)
- [static let flip: MLImageClassifier.ImageAugmentationOptions](/documentation/createml/mlimageclassifier/imageaugmentationoptions/flip)

#### Creating augmentation options

- [init(rawValue: Int)](/documentation/createml/mlimageclassifier/imageaugmentationoptions/init(rawvalue:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlimageclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlimageclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlimageclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlimageclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlimageclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlimageclassifier/description)
- [MLObjectDetector](/documentation/createml/mlobjectdetector)

### Creating a data source

- [Building an object detector data source](/documentation/createml/building-an-object-detector-data-source)

### Training an object detector asynchronously

- [static func train(trainingData: MLObjectDetector.DataSource, annotationType: MLObjectDetector.AnnotationType, parameters: MLObjectDetector.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLObjectDetector>](/documentation/createml/mlobjectdetector/train(trainingdata:annotationtype:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLObjectDetector.DataSource, annotationType: MLObjectDetector.AnnotationType, parameters: MLObjectDetector.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLObjectDetector>](/documentation/createml/mlobjectdetector/maketrainingsession(trainingdata:annotationtype:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLObjectDetector>) throws -> MLJob<MLObjectDetector>](/documentation/createml/mlobjectdetector/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLObjectDetector>](/documentation/createml/mlobjectdetector/restoretrainingsession(sessionparameters:))

### Creating an object detector from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlobjectdetector/init(checkpoint:))

### Training an object detector synchronously

- [init(trainingData: MLObjectDetector.DataSource, parameters: MLObjectDetector.ModelParameters, annotationType: MLObjectDetector.AnnotationType) throws](/documentation/createml/mlobjectdetector/init(trainingdata:parameters:annotationtype:))
- [init(trainingData: MLDataTable, imageColumn: String, annotationColumn: String, annotationType: MLObjectDetector.AnnotationType, parameters: MLObjectDetector.ModelParameters) throws](/documentation/createml/mlobjectdetector/init(trainingdata:imagecolumn:annotationcolumn:annotationtype:parameters:))

### Evaluating an object detector

- [func evaluation(on: MLObjectDetector.DataSource) -> MLObjectDetectorMetrics](/documentation/createml/mlobjectdetector/evaluation(on:))
- [func evaluation(on: MLDataTable, imageColumn: String, annotationColumn: String) -> MLObjectDetectorMetrics](/documentation/createml/mlobjectdetector/evaluation(on:imagecolumn:annotationcolumn:))
- [var trainingMetrics: MLObjectDetectorMetrics](/documentation/createml/mlobjectdetector/trainingmetrics)
- [var validationMetrics: MLObjectDetectorMetrics](/documentation/createml/mlobjectdetector/validationmetrics)

### Testing an object detector

- [func prediction(from: URL) throws -> MLObjectDetector.DetectedObjects](/documentation/createml/mlobjectdetector/prediction(from:))
- [func predictions(from: [URL]) throws -> [MLObjectDetector.DetectedObjects]](/documentation/createml/mlobjectdetector/predictions(from:))
- [MLObjectDetector.DetectedObjects](/documentation/createml/mlobjectdetector/detectedobjects)
- [MLObjectDetector.ObjectAnnotation](/documentation/createml/mlobjectdetector/objectannotation)

#### Creating an annotation

- [init(label: String, boundingBox: CGRect, confidence: Double)](/documentation/createml/mlobjectdetector/objectannotation/init(label:boundingbox:confidence:))

#### Inspecting an annotation

- [var label: String](/documentation/createml/mlobjectdetector/objectannotation/label)
- [var boundingBox: CGRect](/documentation/createml/mlobjectdetector/objectannotation/boundingbox)
- [var confidence: Double](/documentation/createml/mlobjectdetector/objectannotation/confidence)

#### Describing an annotation

- [var description: String](/documentation/createml/mlobjectdetector/objectannotation/description)
- [var debugDescription: String](/documentation/createml/mlobjectdetector/objectannotation/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/objectannotation/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlobjectdetector/objectannotation/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlobjectdetector/objectannotation/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlobjectdetector/objectannotation/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/objectannotation/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlobjectdetector/objectannotation/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlobjectdetector/objectannotation/description)

### Saving an object detector

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlobjectdetector/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlobjectdetector/write(tofile:metadata:))

### Inspecting an object detector model

- [var model: MLModel](/documentation/createml/mlobjectdetector/model)
- [let modelParameters: MLObjectDetector.ModelParameters](/documentation/createml/mlobjectdetector/modelparameters-swift.property)

### Describing an object detector

- [var description: String](/documentation/createml/mlobjectdetector/description)
- [var debugDescription: String](/documentation/createml/mlobjectdetector/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/playgrounddescription)

### Supporting types

- [MLObjectDetector.DataSource](/documentation/createml/mlobjectdetector/datasource)

#### Creating a data source

- [case directoryWithImagesAndJsonAnnotation(at: URL)](/documentation/createml/mlobjectdetector/datasource/directorywithimagesandjsonannotation(at:))
- [case directoryWithImages(at: URL, annotationFile: URL)](/documentation/createml/mlobjectdetector/datasource/directorywithimages(at:annotationfile:))
- [case table(MLDataTable, imageColumn: String, annotationColumn: String)](/documentation/createml/mlobjectdetector/datasource/table(_:imagecolumn:annotationcolumn:))

#### Getting the annotated file names

- [func gatherAnnotatedFileNames() throws -> DataFrame](/documentation/createml/mlobjectdetector/datasource/gatherannotatedfilenames())

#### Getting the data frame

- [case frame(DataFrame, imageColumn: String, annotationColumn: String)](/documentation/createml/mlobjectdetector/datasource/frame(_:imagecolumn:annotationcolumn:))

#### Retrieving the data

- [func imagesWithObjectAnnotations() throws -> MLDataTable](/documentation/createml/mlobjectdetector/datasource/imageswithobjectannotations())

#### Splitting the data

- [func stratifiedSplit(proportions: [Double], seed: Int, annotationColumn: String) throws -> MLDataTable](/documentation/createml/mlobjectdetector/datasource/stratifiedsplit(proportions:seed:annotationcolumn:))
- [MLObjectDetector.AnnotationType](/documentation/createml/mlobjectdetector/annotationtype)

#### Bounding box annotations

- [case boundingBox(units: MLBoundingBoxUnits, origin: MLBoundingBoxCoordinatesOrigin, anchor: MLBoundingBoxAnchor)](/documentation/createml/mlobjectdetector/annotationtype/boundingbox(units:origin:anchor:))
- [MLBoundingBoxUnits](/documentation/createml/mlboundingboxunits)

##### Designating units

- [case pixel](/documentation/createml/mlboundingboxunits/pixel)
- [case normalized](/documentation/createml/mlboundingboxunits/normalized)
- [MLBoundingBoxAnchor](/documentation/createml/mlboundingboxanchor)

##### Designating anchors

- [case center](/documentation/createml/mlboundingboxanchor/center)
- [case topLeft](/documentation/createml/mlboundingboxanchor/topleft)
- [case bottomLeft](/documentation/createml/mlboundingboxanchor/bottomleft)
- [MLBoundingBoxCoordinatesOrigin](/documentation/createml/mlboundingboxcoordinatesorigin)

##### Designating origins

- [case topLeft](/documentation/createml/mlboundingboxcoordinatesorigin/topleft)
- [case bottomLeft](/documentation/createml/mlboundingboxcoordinatesorigin/bottomleft)
- [MLObjectDetector.ModelParameters](/documentation/createml/mlobjectdetector/modelparameters-swift.struct)

#### Creating object detector parameters

- [init(validation: MLObjectDetector.ModelParameters.ValidationData, batchSize: Int?, maxIterations: Int?)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/init(validation:batchsize:maxiterations:))
- [init(validation: MLObjectDetector.ModelParameters.ValidationData, batchSize: Int?, maxIterations: Int?, gridSize: CGSize, algorithm: MLObjectDetector.ModelParameters.ModelAlgorithmType)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/init(validation:batchsize:maxiterations:gridsize:algorithm:))
- [init(validationData: MLObjectDetector.DataSource, batchSize: Int?, maxIterations: Int?) throws](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/init(validationdata:batchsize:maxiterations:))

#### Accessing the training parameters

- [var validation: MLObjectDetector.ModelParameters.ValidationData](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validation)
- [var batchSize: Int?](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/batchsize)
- [var maxIterations: Int?](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/maxiterations)
- [var algorithm: MLObjectDetector.ModelParameters.ModelAlgorithmType](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/algorithm)
- [var gridSize: CGSize](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/gridsize)

#### Describing the model parameters

- [var description: String](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/playgrounddescription)

#### Supporting types

- [MLObjectDetector.ModelParameters.ValidationData](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata)

##### Designating validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata/split(strategy:))
- [case dataFrame(DataFrame, imageColumn: String, annotationColumn: String)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata/dataframe(_:imagecolumn:annotationcolumn:))
- [case dataSource(MLObjectDetector.DataSource)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata/datasource(_:))
- [case table(MLDataTable, imageColumn: String, annotationColumn: String)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata/table(_:imagecolumn:annotationcolumn:))
- [case none](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/validationdata/none)
- [MLObjectDetector.ModelParameters.ModelAlgorithmType](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/modelalgorithmtype)

##### Designating an algorithm

- [case darknetYolo](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/modelalgorithmtype/darknetyolo)
- [case transferLearning(MLObjectDetector.ModelParameters.FeatureExtractorType)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/modelalgorithmtype/transferlearning(_:))
- [MLObjectDetector.ModelParameters.FeatureExtractorType](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/featureextractortype)

###### Designating a feature extractor

- [case objectPrint(revision: Int)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/featureextractortype/objectprint(revision:))

##### Comparing algorithms

- [static func == (MLObjectDetector.ModelParameters.ModelAlgorithmType, MLObjectDetector.ModelParameters.ModelAlgorithmType) -> Bool](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/modelalgorithmtype/==(_:_:))
- [MLObjectDetector.ModelParameters.FeatureExtractorType](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/featureextractortype)

##### Designating a feature extractor

- [case objectPrint(revision: Int)](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/featureextractortype/objectprint(revision:))

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlobjectdetector/modelparameters-swift.struct/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlobjectdetector/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlobjectdetector/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlobjectdetector/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlobjectdetector/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlobjectdetector/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlobjectdetector/description)
- [MLHandPoseClassifier](/documentation/createml/mlhandposeclassifier)

### Training a hand pose classifier asynchronously

- [static func train(trainingData: MLHandPoseClassifier.DataSource, parameters: MLHandPoseClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLHandPoseClassifier>](/documentation/createml/mlhandposeclassifier/train(trainingdata:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLHandPoseClassifier.DataSource, parameters: MLHandPoseClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLHandPoseClassifier>](/documentation/createml/mlhandposeclassifier/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLHandPoseClassifier>) throws -> MLJob<MLHandPoseClassifier>](/documentation/createml/mlhandposeclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLHandPoseClassifier>](/documentation/createml/mlhandposeclassifier/restoretrainingsession(sessionparameters:))

### Creating a hand pose classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlhandposeclassifier/init(checkpoint:))

### Training a hand pose classifier synchronously

- [init(trainingData: MLHandPoseClassifier.DataSource, parameters: MLHandPoseClassifier.ModelParameters) throws](/documentation/createml/mlhandposeclassifier/init(trainingdata:parameters:))

### Evaluating a hand pose classifier

- [func evaluation(on: MLHandPoseClassifier.DataSource) throws -> MLClassifierMetrics](/documentation/createml/mlhandposeclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlhandposeclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlhandposeclassifier/validationmetrics)

### Testing a hand pose classifier

- [func prediction(from: URL) throws -> [(label: String, confidence: Double)]](/documentation/createml/mlhandposeclassifier/prediction(from:))
- [func predictions(from: [URL]) throws -> [[(label: String, confidence: Double)]]](/documentation/createml/mlhandposeclassifier/predictions(from:))

### Saving a hand pose classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlhandposeclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlhandposeclassifier/write(tofile:metadata:))

### Inspecting a hand pose classifier model

- [var model: MLModel](/documentation/createml/mlhandposeclassifier/model)
- [let modelParameters: MLHandPoseClassifier.ModelParameters](/documentation/createml/mlhandposeclassifier/modelparameters-swift.property)

### Describing a hand pose classifier

- [var description: String](/documentation/createml/mlhandposeclassifier/description)
- [var debugDescription: String](/documentation/createml/mlhandposeclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlhandposeclassifier/playgrounddescription)

### Supporting types

- [MLHandPoseClassifier.DataSource](/documentation/createml/mlhandposeclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlhandposeclassifier/datasource/labeleddirectories(at:))
- [case labeledFiles(at: URL)](/documentation/createml/mlhandposeclassifier/datasource/labeledfiles(at:))
- [case directoryWithImagesAndAnnotation(at: URL, annotationFile: URL, imageColumn: String, labelColumn: String)](/documentation/createml/mlhandposeclassifier/datasource/directorywithimagesandannotation(at:annotationfile:imagecolumn:labelcolumn:))
- [case labeledImageDataFrame(DataFrame, imageColumn: String, labelColumn: String)](/documentation/createml/mlhandposeclassifier/datasource/labeledimagedataframe(_:imagecolumn:labelcolumn:))
- [case labeledKeypointsDataFrame(DataFrame, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlhandposeclassifier/datasource/labeledkeypointsdataframe(_:sessionidcolumn:labelcolumn:featurecolumn:))
- [case labeledImageData(table: MLDataTable, imageColumn: String, labelColumn: String)](/documentation/createml/mlhandposeclassifier/datasource/labeledimagedata(table:imagecolumn:labelcolumn:))
- [case labeledKeypointsData(table: MLDataTable, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlhandposeclassifier/datasource/labeledkeypointsdata(table:sessionidcolumn:labelcolumn:featurecolumn:))

#### Extracting keypoints

- [func extractKeypoints() throws -> DataFrame](/documentation/createml/mlhandposeclassifier/datasource/extractkeypoints())

#### Getting annotated file names

- [func gatherAnnotatedFileNames() throws -> DataFrame?](/documentation/createml/mlhandposeclassifier/datasource/gatherannotatedfilenames())

#### Exporting a data source

- [func labeledMedia() throws -> [String : [URL]]](/documentation/createml/mlhandposeclassifier/datasource/labeledmedia())
- [func imagesWithAnnotations() throws -> MLDataTable](/documentation/createml/mlhandposeclassifier/datasource/imageswithannotations())
- [func keypointsWithAnnotations() throws -> MLDataTable](/documentation/createml/mlhandposeclassifier/datasource/keypointswithannotations())
- [func stratifiedSplit(proportions: [Double], seed: Int, labelColumn: String) throws -> MLDataTable](/documentation/createml/mlhandposeclassifier/datasource/stratifiedsplit(proportions:seed:labelcolumn:))
- [MLHandPoseClassifier.ModelParameters](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct)

#### Creating hand pose model parameters

- [init(validation: MLHandPoseClassifier.ModelParameters.ValidationData, batchSize: Int, maximumIterations: Int, augmentationOptions: MLHandPoseClassifier.ImageAugmentationOptions, algorithm: MLHandPoseClassifier.ModelParameters.ModelAlgorithmType)](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/init(validation:batchsize:maximumiterations:augmentationoptions:algorithm:))

#### Accessing hand pose training parameters

- [var maximumIterations: Int](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/maximumiterations)
- [var batchSize: Int](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/batchsize)
- [var algorithm: MLHandPoseClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/algorithm)
- [var augmentationOptions: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/augmentationoptions)
- [var validation: MLHandPoseClassifier.ModelParameters.ValidationData](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/validation)

#### Describing hand pose model parameters

- [var description: String](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/playgrounddescription)

#### Parameter supporting types

- [MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions)

##### Augmentations supporting types

- [static let horizontallyFlip: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/horizontallyflip)
- [static let rotate: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/rotate)
- [static let scale: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/scale)
- [static let translate: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/translate)
- [Option set support](/documentation/createml/option-set-support)

###### Creating an augmentation

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))

##### Creating image augmentation options

- [init(rawValue: Int)](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/init(rawvalue:))
- [MLHandPoseClassifier.ModelParameters.ValidationData](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/validationdata)

##### Designating validation data

- [case dataSource(MLHandPoseClassifier.DataSource)](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/validationdata/datasource(_:))
- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/validationdata/split(strategy:))
- [case none](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/validationdata/none)
- [MLHandPoseClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/modelalgorithmtype)

##### Choosing an algorithm type

- [case gcn](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/modelalgorithmtype/gcn)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlhandposeclassifier/modelparameters-swift.struct/description)
- [MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions)

#### Augmentations supporting types

- [static let horizontallyFlip: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/horizontallyflip)
- [static let rotate: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/rotate)
- [static let scale: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/scale)
- [static let translate: MLHandPoseClassifier.ImageAugmentationOptions](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/translate)
- [Option set support](/documentation/createml/option-set-support)

##### Creating an augmentation

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))

#### Creating image augmentation options

- [init(rawValue: Int)](/documentation/createml/mlhandposeclassifier/imageaugmentationoptions/init(rawvalue:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlhandposeclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlhandposeclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlhandposeclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlhandposeclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlhandposeclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlhandposeclassifier/description)

## Video models

- [Creating an Action Classifier Model](/documentation/createml/creating-an-action-classifier-model)

### Action Classifier Data Sources

- [Gathering Training Videos for an Action Classifier](/documentation/createml/gathering-training-videos-for-an-action-classifier)
- [Building an Action Classifier Data Source](/documentation/createml/building-an-action-classifier-data-source)
- [Detecting human actions in a live video feed](/documentation/createml/detecting-human-actions-in-a-live-video-feed)
- [MLActionClassifier](/documentation/createml/mlactionclassifier)

### Training an action classifier asynchronously

- [static func train(trainingData: MLActionClassifier.DataSource, parameters: MLActionClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLActionClassifier>](/documentation/createml/mlactionclassifier/train(trainingdata:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLActionClassifier.DataSource, parameters: MLActionClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLActionClassifier>](/documentation/createml/mlactionclassifier/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLActionClassifier>) throws -> MLJob<MLActionClassifier>](/documentation/createml/mlactionclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLActionClassifier>](/documentation/createml/mlactionclassifier/restoretrainingsession(sessionparameters:))

### Creating an action classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlactionclassifier/init(checkpoint:))

### Training an action classifier synchronously

- [init(trainingData: MLActionClassifier.DataSource, parameters: MLActionClassifier.ModelParameters) throws](/documentation/createml/mlactionclassifier/init(trainingdata:parameters:))

### Evaluating an action classifier

- [func evaluation(on: MLActionClassifier.DataSource) throws -> MLClassifierMetrics](/documentation/createml/mlactionclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlactionclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlactionclassifier/validationmetrics)

### Testing an action classifier

- [func prediction(from: URL) throws -> [MLActionClassifier.Prediction]](/documentation/createml/mlactionclassifier/prediction(from:))
- [func predictions(from: [URL]) throws -> [[MLActionClassifier.Prediction]]](/documentation/createml/mlactionclassifier/predictions(from:))
- [MLActionClassifier.Prediction](/documentation/createml/mlactionclassifier/prediction)

#### Inspecting a prediction

- [var results: [(label: String, confidence: Double)]](/documentation/createml/mlactionclassifier/prediction/results)
- [var frameRange: Range<Int>](/documentation/createml/mlactionclassifier/prediction/framerange)

### Saving an action classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlactionclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlactionclassifier/write(tofile:metadata:))

### Inspecting an action classifier model

- [var model: MLModel](/documentation/createml/mlactionclassifier/model)
- [let modelParameters: MLActionClassifier.ModelParameters](/documentation/createml/mlactionclassifier/modelparameters-swift.property)

### Describing an action classifier

- [var description: String](/documentation/createml/mlactionclassifier/description)
- [var debugDescription: String](/documentation/createml/mlactionclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlactionclassifier/playgrounddescription)

### Supporting types

- [MLActionClassifier.DataSource](/documentation/createml/mlactionclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlactionclassifier/datasource/labeleddirectories(at:))
- [case labeledFiles(at: URL)](/documentation/createml/mlactionclassifier/datasource/labeledfiles(at:))
- [case directoryWithVideosAndAnnotation(at: URL, annotationFile: URL, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlactionclassifier/datasource/directorywithvideosandannotation(at:annotationfile:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))
- [case labeledVideoData(table: MLDataTable, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlactionclassifier/datasource/labeledvideodata(table:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))

#### Extracting key points

- [func extractKeypoints(targetFrameRate: Double) throws -> DataFrame](/documentation/createml/mlactionclassifier/datasource/extractkeypoints(targetframerate:))
- [case labeledKeypointsDataFrame(DataFrame, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlactionclassifier/datasource/labeledkeypointsdataframe(_:sessionidcolumn:labelcolumn:featurecolumn:))
- [case labeledKeypointsData(table: MLDataTable, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlactionclassifier/datasource/labeledkeypointsdata(table:sessionidcolumn:labelcolumn:featurecolumn:))
- [case labeledVideoDataFrame(DataFrame, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlactionclassifier/datasource/labeledvideodataframe(_:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))

#### Getting annotated file names

- [func gatherAnnotatedFileNames() throws -> DataFrame?](/documentation/createml/mlactionclassifier/datasource/gatherannotatedfilenames())

#### Generating data tables from a data source

- [func videosWithAnnotations() throws -> MLDataTable](/documentation/createml/mlactionclassifier/datasource/videoswithannotations())
- [func keypointsWithAnnotations(targetFrameRate: Double) throws -> MLDataTable](/documentation/createml/mlactionclassifier/datasource/keypointswithannotations(targetframerate:))
- [func stratifiedSplit(proportions: [Double], seed: Int, labelColumn: String) throws -> MLDataTable](/documentation/createml/mlactionclassifier/datasource/stratifiedsplit(proportions:seed:labelcolumn:))
- [MLActionClassifier.ModelParameters](/documentation/createml/mlactionclassifier/modelparameters-swift.struct)

#### Creating action classifier parameters

- [init(validation: MLActionClassifier.ModelParameters.ValidationData, batchSize: Int, maximumIterations: Int, predictionWindowSize: Int, augmentationOptions: MLActionClassifier.VideoAugmentationOptions, algorithm: MLActionClassifier.ModelParameters.ModelAlgorithmType, targetFrameRate: Double)](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/init(validation:batchsize:maximumiterations:predictionwindowsize:augmentationoptions:algorithm:targetframerate:))

#### Accessing the training parameters

- [var maximumIterations: Int](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/maximumiterations)
- [var batchSize: Int](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/batchsize)
- [var targetFrameRate: Double](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/targetframerate)
- [var predictionWindowSize: Int](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/predictionwindowsize)
- [var algorithm: MLActionClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/algorithm)
- [var augmentationOptions: MLActionClassifier.VideoAugmentationOptions](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/augmentationoptions)
- [var validation: MLActionClassifier.ModelParameters.ValidationData](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/validation)

#### Describing the model parameters

- [var description: String](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/playgrounddescription)

#### Supporting types

- [MLActionClassifier.ModelParameters.ValidationData](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/validationdata)

##### Designating validation data

- [case dataSource(MLActionClassifier.DataSource)](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/validationdata/datasource(_:))
- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/validationdata/split(strategy:))
- [case none](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/validationdata/none)
- [MLActionClassifier.VideoAugmentationOptions](/documentation/createml/mlactionclassifier/videoaugmentationoptions)

##### Designating video augmentation options

- [static let horizontalFlip: MLActionClassifier.VideoAugmentationOptions](/documentation/createml/mlactionclassifier/videoaugmentationoptions/horizontalflip)

##### Creating augmentation options

- [init(rawValue: Int)](/documentation/createml/mlactionclassifier/videoaugmentationoptions/init(rawvalue:))
- [MLActionClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/modelalgorithmtype)

##### Designating an algorithm

- [case stgcn](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/modelalgorithmtype/stgcn)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlactionclassifier/modelparameters-swift.struct/description)
- [MLActionClassifier.VideoAugmentationOptions](/documentation/createml/mlactionclassifier/videoaugmentationoptions)

#### Designating video augmentation options

- [static let horizontalFlip: MLActionClassifier.VideoAugmentationOptions](/documentation/createml/mlactionclassifier/videoaugmentationoptions/horizontalflip)

#### Creating augmentation options

- [init(rawValue: Int)](/documentation/createml/mlactionclassifier/videoaugmentationoptions/init(rawvalue:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlactionclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlactionclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlactionclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlactionclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlactionclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlactionclassifier/description)
- [MLHandActionClassifier](/documentation/createml/mlhandactionclassifier)

### Training a hand action classifier asynchronously

- [static func train(trainingData: MLHandActionClassifier.DataSource, parameters: MLHandActionClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLHandActionClassifier>](/documentation/createml/mlhandactionclassifier/train(trainingdata:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLHandActionClassifier.DataSource, parameters: MLHandActionClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLHandActionClassifier>](/documentation/createml/mlhandactionclassifier/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLHandActionClassifier>) throws -> MLJob<MLHandActionClassifier>](/documentation/createml/mlhandactionclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLHandActionClassifier>](/documentation/createml/mlhandactionclassifier/restoretrainingsession(sessionparameters:))

### Creating a hand action classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlhandactionclassifier/init(checkpoint:))

### Training a hand action classifier synchronously

- [init(trainingData: MLHandActionClassifier.DataSource, parameters: MLHandActionClassifier.ModelParameters) throws](/documentation/createml/mlhandactionclassifier/init(trainingdata:parameters:))

### Evaluating a hand action classifier

- [func evaluation(on: MLHandActionClassifier.DataSource) throws -> MLClassifierMetrics](/documentation/createml/mlhandactionclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlhandactionclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlhandactionclassifier/validationmetrics)

### Testing a hand action classifier

- [func prediction(from: URL) throws -> [MLHandActionClassifier.Prediction]](/documentation/createml/mlhandactionclassifier/prediction(from:))
- [func predictions(from: [URL]) throws -> [[MLHandActionClassifier.Prediction]]](/documentation/createml/mlhandactionclassifier/predictions(from:))
- [MLHandActionClassifier.Prediction](/documentation/createml/mlhandactionclassifier/prediction)

#### Inspecting a prediction

- [var results: [(label: String, confidence: Double)]](/documentation/createml/mlhandactionclassifier/prediction/results)
- [var frameRange: Range<Int>](/documentation/createml/mlhandactionclassifier/prediction/framerange)

### Saving a hand action classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlhandactionclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlhandactionclassifier/write(tofile:metadata:))

### Inspecting a hand action classifier model

- [var model: MLModel](/documentation/createml/mlhandactionclassifier/model)
- [let modelParameters: MLHandActionClassifier.ModelParameters](/documentation/createml/mlhandactionclassifier/modelparameters-swift.property)

### Describing a hand action classifier

- [var description: String](/documentation/createml/mlhandactionclassifier/description)
- [var debugDescription: String](/documentation/createml/mlhandactionclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlhandactionclassifier/playgrounddescription)

### Supporting types

- [MLHandActionClassifier.DataSource](/documentation/createml/mlhandactionclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlhandactionclassifier/datasource/labeleddirectories(at:))
- [case labeledFiles(at: URL)](/documentation/createml/mlhandactionclassifier/datasource/labeledfiles(at:))
- [case directoryWithVideosAndAnnotation(at: URL, annotationFile: URL, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlhandactionclassifier/datasource/directorywithvideosandannotation(at:annotationfile:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))
- [case labeledVideoDataFrame(DataFrame, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlhandactionclassifier/datasource/labeledvideodataframe(_:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))
- [case labeledVideoData(table: MLDataTable, videoColumn: String, labelColumn: String, startTimeColumn: String?, endTimeColumn: String?)](/documentation/createml/mlhandactionclassifier/datasource/labeledvideodata(table:videocolumn:labelcolumn:starttimecolumn:endtimecolumn:))
- [case labeledKeypointsDataFrame(DataFrame, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlhandactionclassifier/datasource/labeledkeypointsdataframe(_:sessionidcolumn:labelcolumn:featurecolumn:))
- [case labeledKeypointsData(table: MLDataTable, sessionIdColumn: String, labelColumn: String, featureColumn: String)](/documentation/createml/mlhandactionclassifier/datasource/labeledkeypointsdata(table:sessionidcolumn:labelcolumn:featurecolumn:))

#### Exporting a data source

- [func labeledMedia() throws -> [String : [URL]]](/documentation/createml/mlhandactionclassifier/datasource/labeledmedia())
- [func videosWithAnnotations() throws -> MLDataTable](/documentation/createml/mlhandactionclassifier/datasource/videoswithannotations())
- [func keypointsWithAnnotations(targetFrameRate: Double) throws -> MLDataTable](/documentation/createml/mlhandactionclassifier/datasource/keypointswithannotations(targetframerate:))
- [func stratifiedSplit(proportions: [Double], seed: Int, labelColumn: String) throws -> MLDataTable](/documentation/createml/mlhandactionclassifier/datasource/stratifiedsplit(proportions:seed:labelcolumn:))
- [func extractKeypoints(targetFrameRate: Double) throws -> DataFrame](/documentation/createml/mlhandactionclassifier/datasource/extractkeypoints(targetframerate:))
- [func gatherAnnotatedFileNames() throws -> DataFrame?](/documentation/createml/mlhandactionclassifier/datasource/gatherannotatedfilenames())
- [MLHandActionClassifier.ModelParameters](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct)

#### Creating hand action model parameters

- [init(validation: MLHandActionClassifier.ModelParameters.ValidationData, batchSize: Int, maximumIterations: Int, predictionWindowSize: Int, augmentationOptions: MLHandActionClassifier.VideoAugmentationOptions, algorithm: MLHandActionClassifier.ModelParameters.ModelAlgorithmType, targetFrameRate: Double)](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/init(validation:batchsize:maximumiterations:predictionwindowsize:augmentationoptions:algorithm:targetframerate:))

#### Accessing hand action training parameters

- [var maximumIterations: Int](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/maximumiterations)
- [var batchSize: Int](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/batchsize)
- [var targetFrameRate: Double](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/targetframerate)
- [var predictionWindowSize: Int](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/predictionwindowsize)
- [var algorithm: MLHandActionClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/algorithm)
- [var augmentationOptions: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/augmentationoptions)
- [var validation: MLHandActionClassifier.ModelParameters.ValidationData](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/validation)

#### Describing hand action model parameters

- [var description: String](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/playgrounddescription)

#### Parameter supporting types

- [MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions)

##### Augmentations supporting types

- [static let dropFrames: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/dropframes)
- [static let horizontallyFlip: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/horizontallyflip)
- [static let interpolateFrames: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/interpolateframes)
- [static let rotate: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/rotate)
- [static let scale: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/scale)
- [static let translate: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/translate)
- [Option set support](/documentation/createml/option-set-support)

###### Creating an augmentation

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))

##### Initializers

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))
- [MLHandActionClassifier.ModelParameters.ValidationData](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/validationdata)

##### Designating validation data

- [case dataSource(MLHandActionClassifier.DataSource)](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/validationdata/datasource(_:))
- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/validationdata/split(strategy:))
- [case none](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/validationdata/none)
- [MLHandActionClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/modelalgorithmtype)

##### Choosing an algorithm type

- [case gcn](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/modelalgorithmtype/gcn)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlhandactionclassifier/modelparameters-swift.struct/description)
- [MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions)

#### Augmentations supporting types

- [static let dropFrames: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/dropframes)
- [static let horizontallyFlip: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/horizontallyflip)
- [static let interpolateFrames: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/interpolateframes)
- [static let rotate: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/rotate)
- [static let scale: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/scale)
- [static let translate: MLHandActionClassifier.VideoAugmentationOptions](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/translate)
- [Option set support](/documentation/createml/option-set-support)

##### Creating an augmentation

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))

#### Initializers

- [init(rawValue: Int)](/documentation/createml/mlhandactionclassifier/videoaugmentationoptions/init(rawvalue:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlhandactionclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlhandactionclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlhandactionclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlhandactionclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlhandactionclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlhandactionclassifier/description)
- [MLStyleTransfer](/documentation/createml/mlstyletransfer)

### Training a style transfer model asynchronously

- [static func train(trainingData: MLStyleTransfer.DataSource, parameters: MLStyleTransfer.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLStyleTransfer>](/documentation/createml/mlstyletransfer/train(trainingdata:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLStyleTransfer.DataSource, parameters: MLStyleTransfer.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLStyleTransfer>](/documentation/createml/mlstyletransfer/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLStyleTransfer>) throws -> MLJob<MLStyleTransfer>](/documentation/createml/mlstyletransfer/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLStyleTransfer>](/documentation/createml/mlstyletransfer/restoretrainingsession(sessionparameters:))

### Creating a style transfer model from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlstyletransfer/init(checkpoint:))

### Training a style transfer model synchronously

- [init(trainingData: MLStyleTransfer.DataSource, parameters: MLStyleTransfer.ModelParameters) throws](/documentation/createml/mlstyletransfer/init(trainingdata:parameters:))

### Stylizing an image

- [func stylize(image: CGImage) throws -> CGImage?](/documentation/createml/mlstyletransfer/stylize(image:))

### Saving a style transfer model

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlstyletransfer/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlstyletransfer/write(tofile:metadata:))

### Downloading model assets

- [static func downloadAssets() throws](/documentation/createml/mlstyletransfer/downloadassets())

### Describing a style transfer model

- [var description: String](/documentation/createml/mlstyletransfer/description)
- [var debugDescription: String](/documentation/createml/mlstyletransfer/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/playgrounddescription)

### Supporting types

- [MLStyleTransfer.DataSource](/documentation/createml/mlstyletransfer/datasource)

#### Creating a data source

- [case images(styleImage: URL, contentDirectory: URL, processingOption: VNImageCropAndScaleOption?)](/documentation/createml/mlstyletransfer/datasource/images(styleimage:contentdirectory:processingoption:))

#### Stylizing images

- [func processImages(textelDensity: Int, styleImageDestination: URL?, contentImagesDestination: URL?) throws -> (processedStyleImage: URL, processedContentImages: URL)](/documentation/createml/mlstyletransfer/datasource/processimages(texteldensity:styleimagedestination:contentimagesdestination:))
- [MLStyleTransfer.ModelParameters](/documentation/createml/mlstyletransfer/modelparameters)

#### Creating parameters

- [init(algorithm: MLStyleTransfer.ModelParameters.ModelAlgorithmType, validation: MLStyleTransfer.ModelParameters.ValidationData, maxIterations: Int, textelDensity: Int, styleStrength: Int)](/documentation/createml/mlstyletransfer/modelparameters/init(algorithm:validation:maxiterations:texteldensity:stylestrength:))

#### Setting style transfer parameters

- [var algorithm: MLStyleTransfer.ModelParameters.ModelAlgorithmType](/documentation/createml/mlstyletransfer/modelparameters/algorithm)
- [var debugDescription: String](/documentation/createml/mlstyletransfer/modelparameters/debugdescription)
- [var description: String](/documentation/createml/mlstyletransfer/modelparameters/description)
- [var maxIterations: Int](/documentation/createml/mlstyletransfer/modelparameters/maxiterations)
- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/modelparameters/playgrounddescription)
- [var styleStrength: Int](/documentation/createml/mlstyletransfer/modelparameters/stylestrength)
- [var textelDensity: Int](/documentation/createml/mlstyletransfer/modelparameters/texteldensity)
- [var validation: MLStyleTransfer.ModelParameters.ValidationData](/documentation/createml/mlstyletransfer/modelparameters/validation)

#### Describing parameters

- [MLStyleTransfer.ModelParameters.ModelAlgorithmType](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype)

##### Selecting an algorithm type

- [case cnn](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/cnn)
- [case cnnLite](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/cnnlite)

##### Describing an algorithm type

- [var description: String](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlstyletransfer/modelparameters/modelalgorithmtype/description)
- [MLStyleTransfer.ModelParameters.ValidationData](/documentation/createml/mlstyletransfer/modelparameters/validationdata)

##### Designating validation data

- [case content(URL)](/documentation/createml/mlstyletransfer/modelparameters/validationdata/content(_:))
- [case none](/documentation/createml/mlstyletransfer/modelparameters/validationdata/none)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlstyletransfer/modelparameters/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/modelparameters/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlstyletransfer/modelparameters/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlstyletransfer/modelparameters/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlstyletransfer/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlstyletransfer/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlstyletransfer/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlstyletransfer/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlstyletransfer/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlstyletransfer/description)

## Text models

- [Creating a text classifier model](/documentation/createml/creating-a-text-classifier-model)
- [Creating a word tagger model](/documentation/createml/creating-a-word-tagger-model)
- [MLTextClassifier](/documentation/createml/mltextclassifier)

### Creating and training a text classifier

- [init(trainingData:parameters:)](/documentation/createml/mltextclassifier/init(trainingdata:parameters:))
- [init(trainingData:textColumn:labelColumn:parameters:)](/documentation/createml/mltextclassifier/init(trainingdata:textcolumn:labelcolumn:parameters:))
- [MLTextClassifier.DataSource](/documentation/createml/mltextclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mltextclassifier/datasource/labeleddirectories(at:))

#### Retrieving the data

- [func labeledTexts() throws -> [String : [String]]](/documentation/createml/mltextclassifier/datasource/labeledtexts())
- [func stratifiedSplit(proportions: [Double], seed: Int, labelColumn: String, textColumn: String) throws -> MLDataTable](/documentation/createml/mltextclassifier/datasource/stratifiedsplit(proportions:seed:labelcolumn:textcolumn:))
- [MLTextClassifier.ModelParameters](/documentation/createml/mltextclassifier/modelparameters-swift.struct)

#### Creating parameters

- [init(validation: MLTextClassifier.ModelParameters.ValidationData, algorithm: MLTextClassifier.ModelAlgorithmType, language: NLLanguage?)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/init(validation:algorithm:language:))
- [NLLanguage](/documentation/naturallanguage/nllanguage)
- [MLTextClassifier.ModelAlgorithmType](/documentation/createml/mltextclassifier/modelalgorithmtype)

##### Selecting an algorithm type

- [case crf(revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/crf(revision:))
- [case maxEnt(revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/maxent(revision:))
- [case transferLearning(MLTextClassifier.FeatureExtractorType, revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/transferlearning(_:revision:))
- [MLTextClassifier.FeatureExtractorType](/documentation/createml/mltextclassifier/featureextractortype)

###### Selecting a feature extractor type

- [case customEmbedding(URL)](/documentation/createml/mltextclassifier/featureextractortype/customembedding(_:))
- [case staticEmbedding](/documentation/createml/mltextclassifier/featureextractortype/staticembedding)
- [case bertEmbedding](/documentation/createml/mltextclassifier/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mltextclassifier/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mltextclassifier/featureextractortype/dynamicembedding)

###### Describing a feature extractor type

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)

###### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)

##### Describing an algorithm type

- [var description: String](/documentation/createml/mltextclassifier/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelalgorithmtype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/modelalgorithmtype/description)
- [MLTextClassifier.ModelParameters.ValidationData](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum)

##### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable, textColumn: String, labelColumn: String)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:textcolumn:labelcolumn:))
- [case dataFrame(DataFrame, textColumn: String, labelColumn: String)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:textcolumn:labelcolumn:))
- [case dataSource(MLTextClassifier.DataSource)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/datasource(_:))
- [case dictionary([String : [String]])](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/dictionary(_:))
- [case none](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

#### Accessing parameters

- [var algorithm: MLTextClassifier.ModelAlgorithmType](/documentation/createml/mltextclassifier/modelparameters-swift.struct/algorithm)
- [var language: NLLanguage?](/documentation/createml/mltextclassifier/modelparameters-swift.struct/language)
- [var validation: MLTextClassifier.ModelParameters.ValidationData](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validation)
- [var maxIterations: Int?](/documentation/createml/mltextclassifier/modelparameters-swift.struct/maxiterations)

#### Describing parameters

- [var description: String](/documentation/createml/mltextclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelparameters-swift.struct/playgrounddescription)

#### Deprecated

- [init(validationData:algorithm:language:)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/init(validationdata:algorithm:language:))
- [init(validationData: MLDataTable?, algorithm: MLTextClassifier.ModelAlgorithmType, language: NLLanguage?, textColumnValidationData: String?, labelColumnValidationData: String?)](/documentation/createml/mltextclassifier/modelparameters-swift.struct/init(validationdata:algorithm:language:textcolumnvalidationdata:labelcolumnvalidationdata:))
- [var validationData: MLDataTable?](/documentation/createml/mltextclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var textColumnValidationData: String?](/documentation/createml/mltextclassifier/modelparameters-swift.struct/textcolumnvalidationdata)
- [var labelColumnValidationData: String?](/documentation/createml/mltextclassifier/modelparameters-swift.struct/labelcolumnvalidationdata)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLTextClassifier.ModelParameters](/documentation/createml/mltextclassifier/modelparameters-swift.property)

### Evaluating a text classifier

- [func evaluation(on:)](/documentation/createml/mltextclassifier/evaluation(on:))
- [func evaluation(on:textColumn:labelColumn:)](/documentation/createml/mltextclassifier/evaluation(on:textcolumn:labelcolumn:))
- [let trainingMetrics: MLClassifierMetrics](/documentation/createml/mltextclassifier/trainingmetrics)
- [let validationMetrics: MLClassifierMetrics](/documentation/createml/mltextclassifier/validationmetrics)

### Testing a text classifier

- [func prediction(from: String) throws -> String](/documentation/createml/mltextclassifier/prediction(from:))
- [func predictions(from:)](/documentation/createml/mltextclassifier/predictions(from:))
- [func predictionWithConfidence(from: String) throws -> [String : Double]](/documentation/createml/mltextclassifier/predictionwithconfidence(from:))
- [func predictionsWithConfidence(from:)](/documentation/createml/mltextclassifier/predictionswithconfidence(from:))

### Saving a text classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mltextclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mltextclassifier/write(tofile:metadata:))

### Describing a text classifier

- [var model: MLModel](/documentation/createml/mltextclassifier/model)
- [var description: String](/documentation/createml/mltextclassifier/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/playgrounddescription)

### Supporting types

- [MLTextClassifier.FeatureExtractorType](/documentation/createml/mltextclassifier/featureextractortype)

#### Selecting a feature extractor type

- [case customEmbedding(URL)](/documentation/createml/mltextclassifier/featureextractortype/customembedding(_:))
- [case staticEmbedding](/documentation/createml/mltextclassifier/featureextractortype/staticembedding)
- [case bertEmbedding](/documentation/createml/mltextclassifier/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mltextclassifier/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mltextclassifier/featureextractortype/dynamicembedding)

#### Describing a feature extractor type

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)
- [MLTextClassifier.ModelAlgorithmType](/documentation/createml/mltextclassifier/modelalgorithmtype)

#### Selecting an algorithm type

- [case crf(revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/crf(revision:))
- [case maxEnt(revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/maxent(revision:))
- [case transferLearning(MLTextClassifier.FeatureExtractorType, revision: Int?)](/documentation/createml/mltextclassifier/modelalgorithmtype/transferlearning(_:revision:))
- [MLTextClassifier.FeatureExtractorType](/documentation/createml/mltextclassifier/featureextractortype)

##### Selecting a feature extractor type

- [case customEmbedding(URL)](/documentation/createml/mltextclassifier/featureextractortype/customembedding(_:))
- [case staticEmbedding](/documentation/createml/mltextclassifier/featureextractortype/staticembedding)
- [case bertEmbedding](/documentation/createml/mltextclassifier/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mltextclassifier/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mltextclassifier/featureextractortype/dynamicembedding)

##### Describing a feature extractor type

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/featureextractortype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/featureextractortype/description)

#### Describing an algorithm type

- [var description: String](/documentation/createml/mltextclassifier/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mltextclassifier/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelalgorithmtype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/modelalgorithmtype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/modelalgorithmtype/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mltextclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mltextclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mltextclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mltextclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mltextclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mltextclassifier/description)
- [MLWordTagger](/documentation/createml/mlwordtagger)

### Creating and training a word tagger

- [init(trainingData: [(tokens: [MLWordTagger.Token], labels: [String])], parameters: MLWordTagger.ModelParameters) throws](/documentation/createml/mlwordtagger/init(trainingdata:parameters:))
- [init(trainingData:tokenColumn:labelColumn:parameters:)](/documentation/createml/mlwordtagger/init(trainingdata:tokencolumn:labelcolumn:parameters:))
- [MLWordTagger.Token](/documentation/createml/mlwordtagger/token)
- [MLWordTagger.ModelParameters](/documentation/createml/mlwordtagger/modelparameters-swift.struct)

#### Creating parameters

- [init(validation: MLWordTagger.ModelParameters.ValidationData, algorithm: MLWordTagger.ModelAlgorithmType, language: NLLanguage?)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/init(validation:algorithm:language:))
- [MLWordTagger.ModelAlgorithmType](/documentation/createml/mlwordtagger/modelalgorithmtype)

##### Selecting an algorithm type

- [case crf(revision: Int?)](/documentation/createml/mlwordtagger/modelalgorithmtype/crf(revision:))
- [case transferLearning(MLWordTagger.FeatureExtractorType, revision: Int)](/documentation/createml/mlwordtagger/modelalgorithmtype/transferlearning(_:revision:))
- [MLWordTagger.FeatureExtractorType](/documentation/createml/mlwordtagger/featureextractortype)

###### Selecting a feature extractor type

- [case bertEmbedding](/documentation/createml/mlwordtagger/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mlwordtagger/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mlwordtagger/featureextractortype/dynamicembedding)

###### Describing a feature extractor type

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)

###### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)

##### Describing an algorithm type

- [var description: String](/documentation/createml/mlwordtagger/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelalgorithmtype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/modelalgorithmtype/description)
- [MLWordTagger.ModelParameters.ValidationData](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum)

##### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable, tokenColumn: String, labelColumn: String)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum/table(_:tokencolumn:labelcolumn:))
- [case dataFrame(DataFrame, tokenColumn: String, labelColumn: String)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:tokencolumn:labelcolumn:))
- [case tuples([(tokens: [MLWordTagger.Token], labels: [String])])](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum/tuples(_:))
- [case none](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.enum/none)

#### Accessing parameters

- [var algorithm: MLWordTagger.ModelAlgorithmType](/documentation/createml/mlwordtagger/modelparameters-swift.struct/algorithm)
- [var language: NLLanguage?](/documentation/createml/mlwordtagger/modelparameters-swift.struct/language)
- [var validation: MLWordTagger.ModelParameters.ValidationData](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validation)
- [var maxIterations: Int?](/documentation/createml/mlwordtagger/modelparameters-swift.struct/maxiterations)

#### Describing parameters

- [var description: String](/documentation/createml/mlwordtagger/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelparameters-swift.struct/playgrounddescription)

#### Deprecated

- [init(validationData: MLDataTable?, algorithm: MLWordTagger.ModelAlgorithmType, language: NLLanguage?, tokenColumnValidationData: String?, labelColumnValidationData: String?)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/init(validationdata:algorithm:language:tokencolumnvalidationdata:labelcolumnvalidationdata:))
- [init(validationData: [(tokens: [MLWordTagger.Token], labels: [String])], algorithm: MLWordTagger.ModelAlgorithmType, language: NLLanguage?)](/documentation/createml/mlwordtagger/modelparameters-swift.struct/init(validationdata:algorithm:language:))
- [var validationData: MLDataTable?](/documentation/createml/mlwordtagger/modelparameters-swift.struct/validationdata-swift.property)
- [var tokenColumnValidationData: String?](/documentation/createml/mlwordtagger/modelparameters-swift.struct/tokencolumnvalidationdata)
- [var labelColumnValidationData: String?](/documentation/createml/mlwordtagger/modelparameters-swift.struct/labelcolumnvalidationdata)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/modelparameters-swift.struct/description)
- [let modelParameters: MLWordTagger.ModelParameters](/documentation/createml/mlwordtagger/modelparameters-swift.property)

### Evaluating a word tagger

- [func evaluation(on:tokenColumn:labelColumn:)](/documentation/createml/mlwordtagger/evaluation(on:tokencolumn:labelcolumn:))
- [func evaluation(on: [(tokens: [MLWordTagger.Token], labels: [String])]) -> MLWordTaggerMetrics](/documentation/createml/mlwordtagger/evaluation(on:))
- [let trainingMetrics: MLWordTaggerMetrics](/documentation/createml/mlwordtagger/trainingmetrics)
- [let validationMetrics: MLWordTaggerMetrics](/documentation/createml/mlwordtagger/validationmetrics)
- [MLWordTaggerMetrics](/documentation/createml/mlwordtaggermetrics)

#### Analyzing the tagger’s performance

- [var taggingError: Double](/documentation/createml/mlwordtaggermetrics/taggingerror)
- [var precisionRecall: MLDataTable](/documentation/createml/mlwordtaggermetrics/precisionrecall)
- [var confusion: MLDataTable](/documentation/createml/mlwordtaggermetrics/confusion)

#### Handling errors

- [var isValid: Bool](/documentation/createml/mlwordtaggermetrics/isvalid)
- [var error: (any Error)?](/documentation/createml/mlwordtaggermetrics/error)

#### Describing metrics

- [var description: String](/documentation/createml/mlwordtaggermetrics/description)
- [var debugDescription: String](/documentation/createml/mlwordtaggermetrics/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtaggermetrics/playgrounddescription)
- [var confusionDataFrame: DataFrame](/documentation/createml/mlwordtaggermetrics/confusiondataframe)
- [var precisionRecallDataFrame: DataFrame](/documentation/createml/mlwordtaggermetrics/precisionrecalldataframe)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtaggermetrics/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtaggermetrics/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlwordtaggermetrics/description)

### Testing a word tagger

- [func prediction(from:)](/documentation/createml/mlwordtagger/prediction(from:))
- [func predictions(from:)](/documentation/createml/mlwordtagger/predictions(from:))
- [func predictionWithConfidence(from:)](/documentation/createml/mlwordtagger/predictionwithconfidence(from:))

### Saving a word tagger

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlwordtagger/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlwordtagger/write(tofile:metadata:))

### Describing a word tagger

- [var model: MLModel](/documentation/createml/mlwordtagger/model)
- [var description: String](/documentation/createml/mlwordtagger/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/playgrounddescription)

### Supporting types

- [MLWordTagger.FeatureExtractorType](/documentation/createml/mlwordtagger/featureextractortype)

#### Selecting a feature extractor type

- [case bertEmbedding](/documentation/createml/mlwordtagger/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mlwordtagger/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mlwordtagger/featureextractortype/dynamicembedding)

#### Describing a feature extractor type

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)
- [MLWordTagger.ModelAlgorithmType](/documentation/createml/mlwordtagger/modelalgorithmtype)

#### Selecting an algorithm type

- [case crf(revision: Int?)](/documentation/createml/mlwordtagger/modelalgorithmtype/crf(revision:))
- [case transferLearning(MLWordTagger.FeatureExtractorType, revision: Int)](/documentation/createml/mlwordtagger/modelalgorithmtype/transferlearning(_:revision:))
- [MLWordTagger.FeatureExtractorType](/documentation/createml/mlwordtagger/featureextractortype)

##### Selecting a feature extractor type

- [case bertEmbedding](/documentation/createml/mlwordtagger/featureextractortype/bertembedding)
- [case elmoEmbedding](/documentation/createml/mlwordtagger/featureextractortype/elmoembedding)
- [case dynamicEmbedding](/documentation/createml/mlwordtagger/featureextractortype/dynamicembedding)

##### Describing a feature extractor type

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/featureextractortype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/featureextractortype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/featureextractortype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/featureextractortype/description)

#### Describing an algorithm type

- [var description: String](/documentation/createml/mlwordtagger/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mlwordtagger/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelalgorithmtype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/modelalgorithmtype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/modelalgorithmtype/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtagger/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtagger/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtagger/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtagger/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtagger/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlwordtagger/description)
- [MLGazetteer](/documentation/createml/mlgazetteer)

### Creating a gazetteer

- [init(dictionary: [String : [String]], parameters: MLGazetteer.ModelParameters) throws](/documentation/createml/mlgazetteer/init(dictionary:parameters:))
- [init(labeledData: MLDataTable, textColumn: String, labelColumn: String, parameters: MLGazetteer.ModelParameters) throws](/documentation/createml/mlgazetteer/init(labeleddata:textcolumn:labelcolumn:parameters:))
- [MLGazetteer.ModelParameters](/documentation/createml/mlgazetteer/modelparameters-swift.struct)

#### Creating parameters

- [init(language: NLLanguage?)](/documentation/createml/mlgazetteer/modelparameters-swift.struct/init(language:))

#### Accessing parameters

- [var language: NLLanguage?](/documentation/createml/mlgazetteer/modelparameters-swift.struct/language)

#### Describing parameters

- [var description: String](/documentation/createml/mlgazetteer/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlgazetteer/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlgazetteer/modelparameters-swift.struct/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlgazetteer/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlgazetteer/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlgazetteer/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlgazetteer/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlgazetteer/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlgazetteer/modelparameters-swift.struct/description)
- [let modelParameters: MLGazetteer.ModelParameters](/documentation/createml/mlgazetteer/modelparameters-swift.property)

### Testing a gazetteer

- [func prediction(from: String) throws -> String](/documentation/createml/mlgazetteer/prediction(from:))
- [func predictions(from:)](/documentation/createml/mlgazetteer/predictions(from:))
- [func predictions(from: [String]) throws -> [String]](/documentation/createml/mlgazetteer/predictions(from:)-2rej)
- [func predictions(from: MLDataColumn<String>) throws -> MLDataColumn<String>](/documentation/createml/mlgazetteer/predictions(from:)-2jaui)

### Saving a gazetteer

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlgazetteer/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlgazetteer/write(tofile:metadata:))

### Describing a gazetteer

- [var model: MLModel](/documentation/createml/mlgazetteer/model)
- [var description: String](/documentation/createml/mlgazetteer/description)
- [var debugDescription: String](/documentation/createml/mlgazetteer/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlgazetteer/playgrounddescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlgazetteer/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlgazetteer/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlgazetteer/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlgazetteer/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlgazetteer/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlgazetteer/description)
- [MLWordEmbedding](/documentation/createml/mlwordembedding)

### Creating a word embedding

- [init(dictionary: [String : [Double]], parameters: MLWordEmbedding.ModelParameters) throws](/documentation/createml/mlwordembedding/init(dictionary:parameters:))
- [MLWordEmbedding.ModelParameters](/documentation/createml/mlwordembedding/modelparameters-swift.struct)

#### Creating parameters

- [init(language: NLLanguage?, revision: Int)](/documentation/createml/mlwordembedding/modelparameters-swift.struct/init(language:revision:))

#### Accessing parameters

- [var revision: Int](/documentation/createml/mlwordembedding/modelparameters-swift.struct/revision)
- [var language: NLLanguage?](/documentation/createml/mlwordembedding/modelparameters-swift.struct/language)

#### Describing parameters

- [var description: String](/documentation/createml/mlwordembedding/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlwordembedding/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordembedding/modelparameters-swift.struct/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordembedding/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordembedding/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordembedding/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordembedding/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordembedding/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlwordembedding/modelparameters-swift.struct/description)
- [let modelParameters: MLWordEmbedding.ModelParameters](/documentation/createml/mlwordembedding/modelparameters-swift.property)

### Testing a word embedding

- [func prediction(from: String, maxCount: Int, maxDistance: Double, distanceType: NLDistanceType) throws -> [(text: String, distance: Double)]](/documentation/createml/mlwordembedding/prediction(from:maxcount:maxdistance:distancetype:))
- [func distance(between: String, and: String, distanceType: NLDistanceType) -> Double](/documentation/createml/mlwordembedding/distance(between:and:distancetype:))
- [NLDistanceType](/documentation/naturallanguage/nldistancetype)
- [func contains(String) -> Bool](/documentation/createml/mlwordembedding/contains(_:))
- [func vector(for: String) -> [Double]?](/documentation/createml/mlwordembedding/vector(for:))

### Saving a word embedding

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlwordembedding/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlwordembedding/write(tofile:metadata:))

### Describing a word embedding

- [let dimension: Int](/documentation/createml/mlwordembedding/dimension)
- [let vocabularySize: Int](/documentation/createml/mlwordembedding/vocabularysize)
- [var model: MLModel](/documentation/createml/mlwordembedding/model)
- [var description: String](/documentation/createml/mlwordembedding/description)
- [var debugDescription: String](/documentation/createml/mlwordembedding/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordembedding/playgrounddescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordembedding/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordembedding/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordembedding/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordembedding/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordembedding/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlwordembedding/description)

## Sound models

- [MLSoundClassifier](/documentation/createml/mlsoundclassifier)

### Training a sound classifier asynchronously

- [static train(trainingData:parameters:sessionParameters:)](/documentation/createml/mlsoundclassifier/train(trainingdata:parameters:sessionparameters:))
- [static func makeTrainingSession(trainingData: MLSoundClassifier.DataSource, parameters: MLSoundClassifier.ModelParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLSoundClassifier>](/documentation/createml/mlsoundclassifier/maketrainingsession(trainingdata:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLSoundClassifier>) throws -> MLJob<MLSoundClassifier>](/documentation/createml/mlsoundclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLSoundClassifier>](/documentation/createml/mlsoundclassifier/restoretrainingsession(sessionparameters:))
- [static func extractFeatures(trainingData: MLSoundClassifier.DataSource, parameters: MLSoundClassifier.FeatureExtractionParameters, sessionParameters: MLTrainingSessionParameters) throws -> MLJob<MLSoundClassifier.DataSource>](/documentation/createml/mlsoundclassifier/extractfeatures(trainingdata:parameters:sessionparameters:))
- [MLSoundClassifier.FeatureExtractionParameters](/documentation/createml/mlsoundclassifier/featureextractionparameters)

#### Creating feature extraction parameters

- [init(overlapFactor: Double, featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType, featureExtractionTimeWindowSize: TimeInterval?)](/documentation/createml/mlsoundclassifier/featureextractionparameters/init(overlapfactor:featureextractor:featureextractiontimewindowsize:))
- [init(overlapFactor: Double, featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType)](/documentation/createml/mlsoundclassifier/featureextractionparameters/init(overlapfactor:featureextractor:))

#### Accessing feature extraction parameters

- [var overlapFactor: Double](/documentation/createml/mlsoundclassifier/featureextractionparameters/overlapfactor)
- [var featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType](/documentation/createml/mlsoundclassifier/featureextractionparameters/featureextractor)
- [var featureExtractionTimeWindowSize: TimeInterval](/documentation/createml/mlsoundclassifier/featureextractionparameters/featureextractiontimewindowsize)

### Creating a sound classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlsoundclassifier/init(checkpoint:))

### Training a sound classifier synchronously

- [init(trainingData:parameters:)](/documentation/createml/mlsoundclassifier/init(trainingdata:parameters:))

### Evaluating a sound classifier

- [func evaluation(on:)](/documentation/createml/mlsoundclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlsoundclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlsoundclassifier/validationmetrics)

### Testing a sound classifier

- [func predictions(from: [URL]) throws -> [String]](/documentation/createml/mlsoundclassifier/predictions(from:))
- [func predictions(from: [URL], overlapFactor: Double, predictionTimeWindowSize: TimeInterval) throws -> [String]](/documentation/createml/mlsoundclassifier/predictions(from:overlapfactor:predictiontimewindowsize:))

### Saving a sound classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlsoundclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlsoundclassifier/write(tofile:metadata:))

### Inspecting a sound classifier model

- [var model: MLModel](/documentation/createml/mlsoundclassifier/model)
- [let modelParameters: MLSoundClassifier.ModelParameters](/documentation/createml/mlsoundclassifier/modelparameters-swift.property)

### Describing a sound classifier

- [var description: String](/documentation/createml/mlsoundclassifier/description)
- [var debugDescription: String](/documentation/createml/mlsoundclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlsoundclassifier/playgrounddescription)

### Supporting types

- [MLSoundClassifier.DataSource](/documentation/createml/mlsoundclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlsoundclassifier/datasource/labeleddirectories(at:))
- [case labeledFiles(at: URL)](/documentation/createml/mlsoundclassifier/datasource/labeledfiles(at:))
- [case filesByLabel([String : [URL]])](/documentation/createml/mlsoundclassifier/datasource/filesbylabel(_:))
- [case features(table: MLDataTable, featureColumn: String, labelColumn: String, parameters: MLSoundClassifier.FeatureExtractionParameters)](/documentation/createml/mlsoundclassifier/datasource/features(table:featurecolumn:labelcolumn:parameters:))
- [case featuresDataFrame(DataFrame, featureColumn: String, labelColumn: String, parameters: MLSoundClassifier.FeatureExtractionParameters)](/documentation/createml/mlsoundclassifier/datasource/featuresdataframe(_:featurecolumn:labelcolumn:parameters:))
- [MLSoundClassifier.FeatureExtractionParameters](/documentation/createml/mlsoundclassifier/featureextractionparameters)

##### Creating feature extraction parameters

- [init(overlapFactor: Double, featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType, featureExtractionTimeWindowSize: TimeInterval?)](/documentation/createml/mlsoundclassifier/featureextractionparameters/init(overlapfactor:featureextractor:featureextractiontimewindowsize:))
- [init(overlapFactor: Double, featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType)](/documentation/createml/mlsoundclassifier/featureextractionparameters/init(overlapfactor:featureextractor:))

##### Accessing feature extraction parameters

- [var overlapFactor: Double](/documentation/createml/mlsoundclassifier/featureextractionparameters/overlapfactor)
- [var featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType](/documentation/createml/mlsoundclassifier/featureextractionparameters/featureextractor)
- [var featureExtractionTimeWindowSize: TimeInterval](/documentation/createml/mlsoundclassifier/featureextractionparameters/featureextractiontimewindowsize)

#### Retrieving the data

- [func labeledSounds() throws -> [String : [URL]]](/documentation/createml/mlsoundclassifier/datasource/labeledsounds())

#### Partitioning the data

- [func stratifiedSplit(proportions: [Double], seed: Int) throws -> [[String : [URL]]]](/documentation/createml/mlsoundclassifier/datasource/stratifiedsplit(proportions:seed:))
- [func stratifiedSplit<RNG>(proportions: [Double], generator: inout RNG) throws -> [[String : [URL]]]](/documentation/createml/mlsoundclassifier/datasource/stratifiedsplit(proportions:generator:))
- [MLSoundClassifier.ModelParameters](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct)

#### Creating parameters

- [init(validation: MLSoundClassifier.ModelParameters.ValidationData, maxIterations: Int, overlapFactor: Double)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/init(validation:maxiterations:overlapfactor:))
- [init(validation: MLSoundClassifier.ModelParameters.ValidationData, maxIterations: Int, overlapFactor: Double, algorithm: MLSoundClassifier.ModelParameters.ModelAlgorithmType)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/init(validation:maxiterations:overlapfactor:algorithm:))
- [init(validation: MLSoundClassifier.ModelParameters.ValidationData, maxIterations: Int, overlapFactor: Double, algorithm: MLSoundClassifier.ModelParameters.ModelAlgorithmType, featureExtractionTimeWindowSize: TimeInterval)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/init(validation:maxiterations:overlapfactor:algorithm:featureextractiontimewindowsize:))

#### Accessing the training parameters

- [var validation: MLSoundClassifier.ModelParameters.ValidationData](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validation)
- [var maxIterations: Int](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/maxiterations)
- [var overlapFactor: Double](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/overlapfactor)
- [var algorithm: MLSoundClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/algorithm)
- [var featureExtractionTimeWindowSize: TimeInterval](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractiontimewindowsize)

#### Describing parameters

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/playgrounddescription)

#### Supporting types

- [MLSoundClassifier.ModelParameters.ValidationData](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validationdata)

##### Designating validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validationdata/split(strategy:))
- [case dataSource(MLSoundClassifier.DataSource)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validationdata/datasource(_:))
- [case dictionary([String : [URL]])](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validationdata/dictionary(_:))
- [case none](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/validationdata/none)
- [MLSoundClassifier.ModelParameters.ModelAlgorithmType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/modelalgorithmtype)

##### Designating an algorithm

- [case transferLearning(featureExtractor: MLSoundClassifier.ModelParameters.FeatureExtractorType, classifier: MLSoundClassifier.ModelParameters.ClassifierType)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/modelalgorithmtype/transferlearning(featureextractor:classifier:))
- [MLSoundClassifier.ModelParameters.FeatureExtractorType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype)

###### Designating a feature extractor

- [case audioFeaturePrint(type: MLSoundClassifier.ModelParameters.FeaturePrintType, revision: Int)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/audiofeatureprint(type:revision:))
- [MLSoundClassifier.ModelParameters.FeaturePrintType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype)

###### Designating a feature-print type

- [case sound](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/sound)

###### Describing a feature-print type

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/description)
- [case vggish(revision: Int)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/vggish(revision:))

###### Describing a feature extractor

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/description)
- [MLSoundClassifier.ModelParameters.ClassifierType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype)

###### Designating an algorithm’s classifier

- [case logisticRegressor](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/logisticregressor)
- [case multilayerPerceptron(layerSizes: [Int])](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/multilayerperceptron(layersizes:))

###### Describing a classifier type

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/description)

##### Describing an algorithm

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/modelalgorithmtype/description)
- [MLSoundClassifier.ModelParameters.ClassifierType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype)

##### Designating an algorithm’s classifier

- [case logisticRegressor](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/logisticregressor)
- [case multilayerPerceptron(layerSizes: [Int])](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/multilayerperceptron(layersizes:))

##### Describing a classifier type

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/classifiertype/description)
- [MLSoundClassifier.ModelParameters.FeatureExtractorType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype)

##### Designating a feature extractor

- [case audioFeaturePrint(type: MLSoundClassifier.ModelParameters.FeaturePrintType, revision: Int)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/audiofeatureprint(type:revision:))
- [MLSoundClassifier.ModelParameters.FeaturePrintType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype)

###### Designating a feature-print type

- [case sound](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/sound)

###### Describing a feature-print type

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/description)
- [case vggish(revision: Int)](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/vggish(revision:))

##### Describing a feature extractor

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureextractortype/description)
- [MLSoundClassifier.ModelParameters.FeaturePrintType](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype)

##### Designating a feature-print type

- [case sound](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/sound)

##### Describing a feature-print type

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/featureprinttype/description)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlsoundclassifier/modelparameters-swift.struct/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlsoundclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlsoundclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlsoundclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlsoundclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlsoundclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlsoundclassifier/description)

## Motion models

- [MLActivityClassifier](/documentation/createml/mlactivityclassifier)

### Training an activity classifier asynchronously

- [static train(trainingData:featureColumns:labelColumn:recordingFileColumn:parameters:sessionParameters:)](/documentation/createml/mlactivityclassifier/train(trainingdata:featurecolumns:labelcolumn:recordingfilecolumn:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:featureColumns:labelColumn:recordingFileColumn:parameters:sessionParameters:)](/documentation/createml/mlactivityclassifier/maketrainingsession(trainingdata:featurecolumns:labelcolumn:recordingfilecolumn:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLActivityClassifier>) throws -> MLJob<MLActivityClassifier>](/documentation/createml/mlactivityclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLActivityClassifier>](/documentation/createml/mlactivityclassifier/restoretrainingsession(sessionparameters:))

### Creating an activity classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlactivityclassifier/init(checkpoint:))

### Training an activity classifier synchronously

- [init(trainingData:featureColumns:labelColumn:recordingFileColumn:parameters:)](/documentation/createml/mlactivityclassifier/init(trainingdata:featurecolumns:labelcolumn:recordingfilecolumn:parameters:))

### Evaluating an activity classifier

- [func evaluation(on:featureColumns:labelColumn:recordingFileColumn:)](/documentation/createml/mlactivityclassifier/evaluation(on:featurecolumns:labelcolumn:recordingfilecolumn:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlactivityclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlactivityclassifier/validationmetrics)
- [func evaluation(on:featureColumns:labelColumn:recordingFileColumn:)](/documentation/createml/mlactivityclassifier/evaluation(on:featurecolumns:labelcolumn:recordingfilecolumn:))

### Testing an activity classifier

- [func predictions(from:perWindowPrediction:)](/documentation/createml/mlactivityclassifier/predictions(from:perwindowprediction:))

### Saving an activity classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlactivityclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlactivityclassifier/write(tofile:metadata:))

### Inspecting an activity classifier model

- [var model: MLModel](/documentation/createml/mlactivityclassifier/model)
- [let modelParameters: MLActivityClassifier.ModelParameters](/documentation/createml/mlactivityclassifier/modelparameters-swift.property)
- [var featureColumns: [String]](/documentation/createml/mlactivityclassifier/featurecolumns)
- [var labelColumn: String](/documentation/createml/mlactivityclassifier/labelcolumn)
- [var recordingFileColumn: String](/documentation/createml/mlactivityclassifier/recordingfilecolumn)

### Describing an activity classifier

- [var description: String](/documentation/createml/mlactivityclassifier/description)
- [var debugDescription: String](/documentation/createml/mlactivityclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlactivityclassifier/playgrounddescription)

### Supporting types

- [MLActivityClassifier.DataSource](/documentation/createml/mlactivityclassifier/datasource)

#### Creating a data source

- [case labeledDirectories(at: URL)](/documentation/createml/mlactivityclassifier/datasource/labeleddirectories(at:))
- [case directoryWithDataAndAnnotation(at: URL, annotationFileName: String, timeStampColumn: String, labelStartTimeColumn: String, labelEndTimeColumn: String)](/documentation/createml/mlactivityclassifier/datasource/directorywithdataandannotation(at:annotationfilename:timestampcolumn:labelstarttimecolumn:labelendtimecolumn:))

#### Generating data tables from a data source

- [func labeledSensorData(featureColumns: [String], labelColumn: String?, recordingFileColumn: String?) throws -> MLDataTable](/documentation/createml/mlactivityclassifier/datasource/labeledsensordata(featurecolumns:labelcolumn:recordingfilecolumn:))
- [func stratifiedSplit(proportions: [Double], seed: Int, featureColumns: [String], labelColumn: String, recordingFileColumn: String) throws -> MLDataTable](/documentation/createml/mlactivityclassifier/datasource/stratifiedsplit(proportions:seed:featurecolumns:labelcolumn:recordingfilecolumn:))

#### Gathering annotated features

- [func gatherAnnotatedFeatures(featureColumns: [String], labelColumn: String, recordingFileColumn: String?) throws -> DataFrame](/documentation/createml/mlactivityclassifier/datasource/gatherannotatedfeatures(featurecolumns:labelcolumn:recordingfilecolumn:))

#### Getting the data frame

- [case dataFrame(DataFrame)](/documentation/createml/mlactivityclassifier/datasource/dataframe(_:))
- [MLActivityClassifier.ModelParameters](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct)

#### Creating parameters

- [init(validation: MLActivityClassifier.ModelParameters.Validation, batchSize: Int?, maximumIterations: Int?, predictionWindowSize: Int?)](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/init(validation:batchsize:maximumiterations:predictionwindowsize:))
- [init(validationData:batchSize:maximumIterations:predictionWindowSize:)](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/init(validationdata:batchsize:maximumiterations:predictionwindowsize:))
- [MLActivityClassifier.ModelParameters.Validation](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validation-swift.enum)

##### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validation-swift.enum/split(strategy:))
- [case dataSource(MLActivityClassifier.DataSource)](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validation-swift.enum/datasource(_:))
- [case none](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validation-swift.enum/none)

#### Accessing the training parameters

- [var validationData: MLDataTable?](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validationdata)
- [var batchSize: Int?](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/batchsize)
- [var maximumIterations: Int?](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/maximumiterations)
- [var predictionWindowSize: Int?](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/predictionwindowsize)
- [var validation: MLActivityClassifier.ModelParameters.Validation](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/validation-swift.property)

#### Describing parameters

- [var description: String](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlactivityclassifier/modelparameters-swift.struct/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlactivityclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlactivityclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlactivityclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlactivityclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlactivityclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlactivityclassifier/description)

## Tabular models

- [Creating a model from tabular data](/documentation/createml/creating-a-model-from-tabular-data)
- [MLClassifier](/documentation/createml/mlclassifier)

### Creating and training a classifier

- [init(trainingData:targetColumn:featureColumns:)](/documentation/createml/mlclassifier/init(trainingdata:targetcolumn:featurecolumns:))
- [var targetColumn: String](/documentation/createml/mlclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlclassifier/featurecolumns)

### Evaluating a classifier

- [func evaluation(on:)](/documentation/createml/mlclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlclassifier/validationmetrics)

### Testing a classifier

- [func predictions(from:)](/documentation/createml/mlclassifier/predictions(from:))

### Saving a classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlclassifier/write(tofile:metadata:))

### Describing a model

- [var model: MLModel](/documentation/createml/mlclassifier/model)
- [var description: String](/documentation/createml/mlclassifier/description)
- [var debugDescription: String](/documentation/createml/mlclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlclassifier/playgrounddescription)

### Classifier cases

- [case decisionTree(MLDecisionTreeClassifier)](/documentation/createml/mlclassifier/decisiontree(_:))
- [case randomForest(MLRandomForestClassifier)](/documentation/createml/mlclassifier/randomforest(_:))
- [case boostedTree(MLBoostedTreeClassifier)](/documentation/createml/mlclassifier/boostedtree(_:))
- [case logisticRegression(MLLogisticRegressionClassifier)](/documentation/createml/mlclassifier/logisticregression(_:))
- [case supportVector(MLSupportVectorClassifier)](/documentation/createml/mlclassifier/supportvector(_:))

### Supporting classifier types

- [MLDecisionTreeClassifier](/documentation/createml/mldecisiontreeclassifier)

#### Training a decision tree classifier asynchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mldecisiontreeclassifier/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mldecisiontreeclassifier/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLDecisionTreeClassifier>) throws -> MLJob<MLDecisionTreeClassifier>](/documentation/createml/mldecisiontreeclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLDecisionTreeClassifier>](/documentation/createml/mldecisiontreeclassifier/restoretrainingsession(sessionparameters:))

#### Creating a decision tree classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mldecisiontreeclassifier/init(checkpoint:))

#### Training a decision tree classifier synchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mldecisiontreeclassifier/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [var targetColumn: String](/documentation/createml/mldecisiontreeclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mldecisiontreeclassifier/featurecolumns)

#### Evaluating a decision tree classifier

- [func evaluation(on:)](/documentation/createml/mldecisiontreeclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mldecisiontreeclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mldecisiontreeclassifier/validationmetrics)

#### Testing a decision tree classifier

- [func predictions(from:)](/documentation/createml/mldecisiontreeclassifier/predictions(from:))

#### Saving a decision tree classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mldecisiontreeclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mldecisiontreeclassifier/write(tofile:metadata:))

#### Inspecting a decision tree classifier

- [var model: MLModel](/documentation/createml/mldecisiontreeclassifier/model)
- [MLDecisionTreeClassifier.ModelParameters](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLDecisionTreeClassifier.ModelParameters.ValidationData, maxDepth: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int)](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/init(validation:maxdepth:minlossreduction:minchildweight:randomseed:))
- [init(validationData: MLDataTable?, maxDepth: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int)](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/init(validationdata:maxdepth:minlossreduction:minchildweight:randomseed:))
- [MLDecisionTreeClassifier.ModelParameters.ValidationData](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var validationData: MLDataTable?](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var maxDepth: Int](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/maxdepth)
- [var minLossReduction: Double](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/minlossreduction)
- [var minChildWeight: Double](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/minchildweight)
- [var randomSeed: Int](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/randomseed)
- [var validation: MLDecisionTreeClassifier.ModelParameters.ValidationData](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLDecisionTreeClassifier.ModelParameters](/documentation/createml/mldecisiontreeclassifier/modelparameters-swift.property)

#### Describing a decision tree classifier

- [var description: String](/documentation/createml/mldecisiontreeclassifier/description)
- [var debugDescription: String](/documentation/createml/mldecisiontreeclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeclassifier/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mldecisiontreeclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldecisiontreeclassifier/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mldecisiontreeclassifier/description)
- [MLRandomForestClassifier](/documentation/createml/mlrandomforestclassifier)

#### Creating a random forest classifier asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlrandomforestclassifier/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlrandomforestclassifier/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLRandomForestClassifier>) throws -> MLJob<MLRandomForestClassifier>](/documentation/createml/mlrandomforestclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLRandomForestClassifier>](/documentation/createml/mlrandomforestclassifier/restoretrainingsession(sessionparameters:))

#### Creating a random forest classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlrandomforestclassifier/init(checkpoint:))

#### Creating a random forest classifier synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mlrandomforestclassifier/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mlrandomforestclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlrandomforestclassifier/featurecolumns)

#### Evaluating a random forest classifier

- [func evaluation(on:)](/documentation/createml/mlrandomforestclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlrandomforestclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlrandomforestclassifier/validationmetrics)

#### Testing a random forest classifier

- [func predictions(from:)](/documentation/createml/mlrandomforestclassifier/predictions(from:))

#### Saving a random forest classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlrandomforestclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlrandomforestclassifier/write(tofile:metadata:))

#### Inspecting a random forest classifier

- [var model: MLModel](/documentation/createml/mlrandomforestclassifier/model)
- [MLRandomForestClassifier.ModelParameters](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLRandomForestClassifier.ModelParameters.ValidationData, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/init(validation:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:rowsubsample:columnsubsample:))
- [init(validationData: MLDataTable?, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/init(validationdata:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:rowsubsample:columnsubsample:))
- [MLRandomForestClassifier.ModelParameters.ValidationData](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var columnSubsample: Double](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/columnsubsample)
- [var maxDepth: Int](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/maxdepth)
- [var maxIterations: Int](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/maxiterations)
- [var minChildWeight: Double](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/minchildweight)
- [var minLossReduction: Double](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/minlossreduction)
- [var randomSeed: Int](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/randomseed)
- [var rowSubsample: Double](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/rowsubsample)
- [var validationData: MLDataTable?](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLRandomForestClassifier.ModelParameters.ValidationData](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLRandomForestClassifier.ModelParameters](/documentation/createml/mlrandomforestclassifier/modelparameters-swift.property)

#### Describing a random forest classifier

- [var description: String](/documentation/createml/mlrandomforestclassifier/description)
- [var debugDescription: String](/documentation/createml/mlrandomforestclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrandomforestclassifier/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrandomforestclassifier/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrandomforestclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrandomforestclassifier/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrandomforestclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrandomforestclassifier/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlrandomforestclassifier/description)
- [MLBoostedTreeClassifier](/documentation/createml/mlboostedtreeclassifier)

#### Training a boosted tree classifier asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlboostedtreeclassifier/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlboostedtreeclassifier/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLBoostedTreeClassifier>) throws -> MLJob<MLBoostedTreeClassifier>](/documentation/createml/mlboostedtreeclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLBoostedTreeClassifier>](/documentation/createml/mlboostedtreeclassifier/restoretrainingsession(sessionparameters:))

#### Creating a boosted tree classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlboostedtreeclassifier/init(checkpoint:))

#### Training a boosted tree classifier synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mlboostedtreeclassifier/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mlboostedtreeclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlboostedtreeclassifier/featurecolumns)

#### Evaluating a boosted tree classifier

- [func evaluation(on:)](/documentation/createml/mlboostedtreeclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlboostedtreeclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlboostedtreeclassifier/validationmetrics)

#### Testing a boosted tree classifier

- [func predictions(from:)](/documentation/createml/mlboostedtreeclassifier/predictions(from:))

#### Saving a boosted tree classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlboostedtreeclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlboostedtreeclassifier/write(tofile:metadata:))

#### Inspecting a boosted tree classifier

- [var model: MLModel](/documentation/createml/mlboostedtreeclassifier/model)
- [MLBoostedTreeClassifier.ModelParameters](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLBoostedTreeClassifier.ModelParameters.ValidationData, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, stepSize: Double, earlyStoppingRounds: Int?, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/init(validation:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:stepsize:earlystoppingrounds:rowsubsample:columnsubsample:))
- [init(validationData: MLDataTable?, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, stepSize: Double, earlyStoppingRounds: Int?, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/init(validationdata:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:stepsize:earlystoppingrounds:rowsubsample:columnsubsample:))
- [MLBoostedTreeClassifier.ModelParameters.ValidationData](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var validationData: MLDataTable?](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var maxDepth: Int](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/maxdepth)
- [var maxIterations: Int](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/maxiterations)
- [var minLossReduction: Double](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/minlossreduction)
- [var minChildWeight: Double](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/minchildweight)
- [var randomSeed: Int](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/randomseed)
- [var stepSize: Double](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/stepsize)
- [var earlyStoppingRounds: Int?](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/earlystoppingrounds)
- [var rowSubsample: Double](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/rowsubsample)
- [var columnSubsample: Double](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/columnsubsample)
- [var validation: MLBoostedTreeClassifier.ModelParameters.ValidationData](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLBoostedTreeClassifier.ModelParameters](/documentation/createml/mlboostedtreeclassifier/modelparameters-swift.property)

#### Describing a boosted tree classifier

- [var description: String](/documentation/createml/mlboostedtreeclassifier/description)
- [var debugDescription: String](/documentation/createml/mlboostedtreeclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeclassifier/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlboostedtreeclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlboostedtreeclassifier/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlboostedtreeclassifier/description)
- [MLLogisticRegressionClassifier](/documentation/createml/mllogisticregressionclassifier)

#### Training a logistic regression classifier asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mllogisticregressionclassifier/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mllogisticregressionclassifier/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLLogisticRegressionClassifier>) throws -> MLJob<MLLogisticRegressionClassifier>](/documentation/createml/mllogisticregressionclassifier/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLLogisticRegressionClassifier>](/documentation/createml/mllogisticregressionclassifier/restoretrainingsession(sessionparameters:))

#### Creating a logistic regression classifier from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mllogisticregressionclassifier/init(checkpoint:))

#### Training a logistic regression classifier synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mllogisticregressionclassifier/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mllogisticregressionclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mllogisticregressionclassifier/featurecolumns)

#### Evaluating a logistic regression classifier

- [func evaluation(on:)](/documentation/createml/mllogisticregressionclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mllogisticregressionclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mllogisticregressionclassifier/validationmetrics)

#### Testing a logistic regression classifier

- [func predictions(from:)](/documentation/createml/mllogisticregressionclassifier/predictions(from:))

#### Saving a logistic regression classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mllogisticregressionclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mllogisticregressionclassifier/write(tofile:metadata:))

#### Inspecting a boosted tree classifier

- [var model: MLModel](/documentation/createml/mllogisticregressionclassifier/model)
- [MLLogisticRegressionClassifier.ModelParameters](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLLogisticRegressionClassifier.ModelParameters.ValidationData, maxIterations: Int, l1Penalty: Double, l2Penalty: Double, stepSize: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/init(validation:maxiterations:l1penalty:l2penalty:stepsize:convergencethreshold:featurerescaling:))
- [init(validationData: MLDataTable?, maxIterations: Int, l1Penalty: Double, l2Penalty: Double, stepSize: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/init(validationdata:maxiterations:l1penalty:l2penalty:stepsize:convergencethreshold:featurerescaling:))
- [MLLogisticRegressionClassifier.ModelParameters.ValidationData](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var convergenceThreshold: Double](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/convergencethreshold)
- [var featureRescaling: Bool](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/featurerescaling)
- [var l1Penalty: Double](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/l1penalty)
- [var l2Penalty: Double](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/l2penalty)
- [var maxIterations: Int](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/maxiterations)
- [var stepSize: Double](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/stepsize)
- [var validationData: MLDataTable?](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLLogisticRegressionClassifier.ModelParameters.ValidationData](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLLogisticRegressionClassifier.ModelParameters](/documentation/createml/mllogisticregressionclassifier/modelparameters-swift.property)

#### Describing a logistic regression classifier

- [var description: String](/documentation/createml/mllogisticregressionclassifier/description)
- [var debugDescription: String](/documentation/createml/mllogisticregressionclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mllogisticregressionclassifier/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mllogisticregressionclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mllogisticregressionclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mllogisticregressionclassifier/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mllogisticregressionclassifier/description)
- [MLSupportVectorClassifier](/documentation/createml/mlsupportvectorclassifier)

#### Creating and training a support vector classifier

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mlsupportvectorclassifier/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [MLSupportVectorClassifier.ModelParameters](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLSupportVectorClassifier.ModelParameters.ValidationData, maxIterations: Int, penalty: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/init(validation:maxiterations:penalty:convergencethreshold:featurerescaling:))
- [init(validationData: MLDataTable?, maxIterations: Int, penalty: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/init(validationdata:maxiterations:penalty:convergencethreshold:featurerescaling:))
- [MLSupportVectorClassifier.ModelParameters.ValidationData](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var convergenceThreshold: Double](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/convergencethreshold)
- [var featureRescaling: Bool](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/featurerescaling)
- [var maxIterations: Int](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/maxiterations)
- [var penalty: Double](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/penalty)
- [var validationData: MLDataTable?](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLSupportVectorClassifier.ModelParameters.ValidationData](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.struct/description)
- [let modelParameters: MLSupportVectorClassifier.ModelParameters](/documentation/createml/mlsupportvectorclassifier/modelparameters-swift.property)
- [var targetColumn: String](/documentation/createml/mlsupportvectorclassifier/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlsupportvectorclassifier/featurecolumns)

#### Evaluating a support vector classifier

- [func evaluation(on:)](/documentation/createml/mlsupportvectorclassifier/evaluation(on:))
- [var trainingMetrics: MLClassifierMetrics](/documentation/createml/mlsupportvectorclassifier/trainingmetrics)
- [var validationMetrics: MLClassifierMetrics](/documentation/createml/mlsupportvectorclassifier/validationmetrics)

#### Testing a support vector classifier

- [func predictions(from:)](/documentation/createml/mlsupportvectorclassifier/predictions(from:))

#### Saving a support vector classifier

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlsupportvectorclassifier/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlsupportvectorclassifier/write(tofile:metadata:))

#### Describing a support vector classifier

- [var model: MLModel](/documentation/createml/mlsupportvectorclassifier/model)
- [var description: String](/documentation/createml/mlsupportvectorclassifier/description)
- [var debugDescription: String](/documentation/createml/mlsupportvectorclassifier/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlsupportvectorclassifier/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlsupportvectorclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlsupportvectorclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlsupportvectorclassifier/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlsupportvectorclassifier/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlclassifier/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlclassifier/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlclassifier/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlclassifier/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlclassifier/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlclassifier/description)
- [MLRegressor](/documentation/createml/mlregressor)

### Creating and training a regressor

- [init(trainingData:targetColumn:featureColumns:)](/documentation/createml/mlregressor/init(trainingdata:targetcolumn:featurecolumns:))
- [var targetColumn: String](/documentation/createml/mlregressor/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlregressor/featurecolumns)

### Evaluating a regressor

- [func evaluation(on:)](/documentation/createml/mlregressor/evaluation(on:))
- [var trainingMetrics: MLRegressorMetrics](/documentation/createml/mlregressor/trainingmetrics)
- [var validationMetrics: MLRegressorMetrics](/documentation/createml/mlregressor/validationmetrics)

### Testing a regressor

- [func predictions(from:)](/documentation/createml/mlregressor/predictions(from:))

### Saving a regressor

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlregressor/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlregressor/write(tofile:metadata:))

### Describing a regressor

- [var model: MLModel](/documentation/createml/mlregressor/model)
- [var description: String](/documentation/createml/mlregressor/description)
- [var debugDescription: String](/documentation/createml/mlregressor/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlregressor/playgrounddescription)

### Regressor cases

- [case linear(MLLinearRegressor)](/documentation/createml/mlregressor/linear(_:))
- [case decisionTree(MLDecisionTreeRegressor)](/documentation/createml/mlregressor/decisiontree(_:))
- [case boostedTree(MLBoostedTreeRegressor)](/documentation/createml/mlregressor/boostedtree(_:))
- [case randomForest(MLRandomForestRegressor)](/documentation/createml/mlregressor/randomforest(_:))

### Supporting regressor types

- [MLLinearRegressor](/documentation/createml/mllinearregressor)

#### Creating a linear regressor asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mllinearregressor/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mllinearregressor/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLLinearRegressor>) throws -> MLJob<MLLinearRegressor>](/documentation/createml/mllinearregressor/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLLinearRegressor>](/documentation/createml/mllinearregressor/restoretrainingsession(sessionparameters:))

#### Creating a linear regressor from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mllinearregressor/init(checkpoint:))

#### Training a linear regressor synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mllinearregressor/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mllinearregressor/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mllinearregressor/featurecolumns)

#### Evaluating a linear regressor

- [func evaluation(on:)](/documentation/createml/mllinearregressor/evaluation(on:))
- [var trainingMetrics: MLRegressorMetrics](/documentation/createml/mllinearregressor/trainingmetrics)
- [var validationMetrics: MLRegressorMetrics](/documentation/createml/mllinearregressor/validationmetrics)

#### Testing a linear regressor

- [func predictions(from:)](/documentation/createml/mllinearregressor/predictions(from:))

#### Saving a linear regressor

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mllinearregressor/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mllinearregressor/write(tofile:metadata:))

#### Inspecting a linear regressor

- [var model: MLModel](/documentation/createml/mllinearregressor/model)
- [MLLinearRegressor.ModelParameters](/documentation/createml/mllinearregressor/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLLinearRegressor.ModelParameters.ValidationData, maxIterations: Int, l1Penalty: Double, l2Penalty: Double, stepSize: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mllinearregressor/modelparameters-swift.struct/init(validation:maxiterations:l1penalty:l2penalty:stepsize:convergencethreshold:featurerescaling:))
- [init(validationData: MLDataTable?, maxIterations: Int, l1Penalty: Double, l2Penalty: Double, stepSize: Double, convergenceThreshold: Double, featureRescaling: Bool)](/documentation/createml/mllinearregressor/modelparameters-swift.struct/init(validationdata:maxiterations:l1penalty:l2penalty:stepsize:convergencethreshold:featurerescaling:))
- [MLLinearRegressor.ModelParameters.ValidationData](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var validationData: MLDataTable?](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validationdata-swift.property)
- [var maxIterations: Int](/documentation/createml/mllinearregressor/modelparameters-swift.struct/maxiterations)
- [var l1Penalty: Double](/documentation/createml/mllinearregressor/modelparameters-swift.struct/l1penalty)
- [var l2Penalty: Double](/documentation/createml/mllinearregressor/modelparameters-swift.struct/l2penalty)
- [var stepSize: Double](/documentation/createml/mllinearregressor/modelparameters-swift.struct/stepsize)
- [var convergenceThreshold: Double](/documentation/createml/mllinearregressor/modelparameters-swift.struct/convergencethreshold)
- [var featureRescaling: Bool](/documentation/createml/mllinearregressor/modelparameters-swift.struct/featurerescaling)
- [var validation: MLLinearRegressor.ModelParameters.ValidationData](/documentation/createml/mllinearregressor/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mllinearregressor/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mllinearregressor/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mllinearregressor/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mllinearregressor/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mllinearregressor/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mllinearregressor/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mllinearregressor/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mllinearregressor/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mllinearregressor/modelparameters-swift.struct/description)
- [let modelParameters: MLLinearRegressor.ModelParameters](/documentation/createml/mllinearregressor/modelparameters-swift.property)

#### Describing a linear regressor

- [var description: String](/documentation/createml/mllinearregressor/description)
- [var debugDescription: String](/documentation/createml/mllinearregressor/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mllinearregressor/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mllinearregressor/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mllinearregressor/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mllinearregressor/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mllinearregressor/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mllinearregressor/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mllinearregressor/description)
- [MLDecisionTreeRegressor](/documentation/createml/mldecisiontreeregressor)

#### Training a decision tree regressor asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mldecisiontreeregressor/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mldecisiontreeregressor/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLDecisionTreeRegressor>) throws -> MLJob<MLDecisionTreeRegressor>](/documentation/createml/mldecisiontreeregressor/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLDecisionTreeRegressor>](/documentation/createml/mldecisiontreeregressor/restoretrainingsession(sessionparameters:))

#### Creating a decision tree regressor from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mldecisiontreeregressor/init(checkpoint:))

#### Training a decision tree regressor synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mldecisiontreeregressor/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mldecisiontreeregressor/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mldecisiontreeregressor/featurecolumns)

#### Evaluating a decision tree regressor

- [func evaluation(on:)](/documentation/createml/mldecisiontreeregressor/evaluation(on:))
- [var trainingMetrics: MLRegressorMetrics](/documentation/createml/mldecisiontreeregressor/trainingmetrics)
- [var validationMetrics: MLRegressorMetrics](/documentation/createml/mldecisiontreeregressor/validationmetrics)

#### Testing a decision tree regressor

- [func predictions(from:)](/documentation/createml/mldecisiontreeregressor/predictions(from:))

#### Saving a decision tree regressor

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mldecisiontreeregressor/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mldecisiontreeregressor/write(tofile:metadata:))

#### Inspecting a decision tree regressor

- [var model: MLModel](/documentation/createml/mldecisiontreeregressor/model)
- [MLDecisionTreeRegressor.ModelParameters](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLDecisionTreeRegressor.ModelParameters.ValidationData, maxDepth: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int)](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/init(validation:maxdepth:minlossreduction:minchildweight:randomseed:))
- [init(validationData: MLDataTable?, maxDepth: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int)](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/init(validationdata:maxdepth:minlossreduction:minchildweight:randomseed:))
- [MLDecisionTreeRegressor.ModelParameters.ValidationData](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var maxDepth: Int](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/maxdepth)
- [var minChildWeight: Double](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/minchildweight)
- [var minLossReduction: Double](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/minlossreduction)
- [var randomSeed: Int](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/randomseed)
- [var validationData: MLDataTable?](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLDecisionTreeRegressor.ModelParameters.ValidationData](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.struct/description)
- [let modelParameters: MLDecisionTreeRegressor.ModelParameters](/documentation/createml/mldecisiontreeregressor/modelparameters-swift.property)

#### Describing a decision tree regressor

- [var description: String](/documentation/createml/mldecisiontreeregressor/description)
- [var debugDescription: String](/documentation/createml/mldecisiontreeregressor/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeregressor/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldecisiontreeregressor/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mldecisiontreeregressor/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldecisiontreeregressor/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldecisiontreeregressor/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldecisiontreeregressor/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mldecisiontreeregressor/description)
- [MLRandomForestRegressor](/documentation/createml/mlrandomforestregressor)

#### Training a random forest regressor

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlrandomforestregressor/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlrandomforestregressor/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLRandomForestRegressor>) throws -> MLJob<MLRandomForestRegressor>](/documentation/createml/mlrandomforestregressor/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLRandomForestRegressor>](/documentation/createml/mlrandomforestregressor/restoretrainingsession(sessionparameters:))

#### Creating a random forest regressor from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlrandomforestregressor/init(checkpoint:))

#### Training a random forest regressor synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mlrandomforestregressor/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mlrandomforestregressor/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlrandomforestregressor/featurecolumns)

#### Evaluating a random forest regressor

- [func evaluation(on:)](/documentation/createml/mlrandomforestregressor/evaluation(on:))
- [var trainingMetrics: MLRegressorMetrics](/documentation/createml/mlrandomforestregressor/trainingmetrics)
- [var validationMetrics: MLRegressorMetrics](/documentation/createml/mlrandomforestregressor/validationmetrics)

#### Testing a Random Forest Regressor

- [func predictions(from:)](/documentation/createml/mlrandomforestregressor/predictions(from:))

#### Saving a Random Forest Regressor

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlrandomforestregressor/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlrandomforestregressor/write(tofile:metadata:))

#### Inspecting a random forest regressor

- [var model: MLModel](/documentation/createml/mlrandomforestregressor/model)
- [MLRandomForestRegressor.ModelParameters](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLRandomForestRegressor.ModelParameters.ValidationData, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/init(validation:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:rowsubsample:columnsubsample:))
- [init(validationData: MLDataTable?, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/init(validationdata:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:rowsubsample:columnsubsample:))
- [MLRandomForestRegressor.ModelParameters.ValidationData](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var columnSubsample: Double](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/columnsubsample)
- [var maxDepth: Int](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/maxdepth)
- [var maxIterations: Int](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/maxiterations)
- [var minChildWeight: Double](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/minchildweight)
- [var minLossReduction: Double](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/minlossreduction)
- [var randomSeed: Int](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/randomseed)
- [var rowSubsample: Double](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/rowsubsample)
- [var validationData: MLDataTable?](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLRandomForestRegressor.ModelParameters.ValidationData](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlrandomforestregressor/modelparameters-swift.struct/description)
- [let modelParameters: MLRandomForestRegressor.ModelParameters](/documentation/createml/mlrandomforestregressor/modelparameters-swift.property)

#### Describing a random forest regressor

- [var description: String](/documentation/createml/mlrandomforestregressor/description)
- [var debugDescription: String](/documentation/createml/mlrandomforestregressor/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrandomforestregressor/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrandomforestregressor/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrandomforestregressor/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrandomforestregressor/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrandomforestregressor/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrandomforestregressor/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlrandomforestregressor/description)
- [MLBoostedTreeRegressor](/documentation/createml/mlboostedtreeregressor)

#### Training a boosted tree regressor asynchronously

- [static train(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlboostedtreeregressor/train(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static makeTrainingSession(trainingData:targetColumn:featureColumns:parameters:sessionParameters:)](/documentation/createml/mlboostedtreeregressor/maketrainingsession(trainingdata:targetcolumn:featurecolumns:parameters:sessionparameters:))
- [static func resume(MLTrainingSession<MLBoostedTreeRegressor>) throws -> MLJob<MLBoostedTreeRegressor>](/documentation/createml/mlboostedtreeregressor/resume(_:))
- [static func restoreTrainingSession(sessionParameters: MLTrainingSessionParameters) throws -> MLTrainingSession<MLBoostedTreeRegressor>](/documentation/createml/mlboostedtreeregressor/restoretrainingsession(sessionparameters:))

#### Creating a boosted tree regressor from a checkpoint

- [init(checkpoint: MLCheckpoint) throws](/documentation/createml/mlboostedtreeregressor/init(checkpoint:))

#### Training a boosted tree regressor synchronously

- [init(trainingData:targetColumn:featureColumns:parameters:)](/documentation/createml/mlboostedtreeregressor/init(trainingdata:targetcolumn:featurecolumns:parameters:))
- [var targetColumn: String](/documentation/createml/mlboostedtreeregressor/targetcolumn)
- [var featureColumns: [String]](/documentation/createml/mlboostedtreeregressor/featurecolumns)

#### Evaluating a boosted tree regressor

- [func evaluation(on:)](/documentation/createml/mlboostedtreeregressor/evaluation(on:))
- [var trainingMetrics: MLRegressorMetrics](/documentation/createml/mlboostedtreeregressor/trainingmetrics)
- [var validationMetrics: MLRegressorMetrics](/documentation/createml/mlboostedtreeregressor/validationmetrics)

#### Testing a boosted tree regressor

- [func predictions(from:)](/documentation/createml/mlboostedtreeregressor/predictions(from:))

#### Saving a boosted tree regressor

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlboostedtreeregressor/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlboostedtreeregressor/write(tofile:metadata:))

#### Inspecting a boosted tree regressor

- [var model: MLModel](/documentation/createml/mlboostedtreeregressor/model)
- [MLBoostedTreeRegressor.ModelParameters](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct)

##### Creating parameters

- [init(validation: MLBoostedTreeRegressor.ModelParameters.ValidationData, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, stepSize: Double, earlyStoppingRounds: Int?, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/init(validation:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:stepsize:earlystoppingrounds:rowsubsample:columnsubsample:))
- [init(validationData: MLDataTable?, maxDepth: Int, maxIterations: Int, minLossReduction: Double, minChildWeight: Double, randomSeed: Int, stepSize: Double, earlyStoppingRounds: Int?, rowSubsample: Double, columnSubsample: Double)](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/init(validationdata:maxdepth:maxiterations:minlossreduction:minchildweight:randomseed:stepsize:earlystoppingrounds:rowsubsample:columnsubsample:))
- [MLBoostedTreeRegressor.ModelParameters.ValidationData](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.enum)

###### Specifying validation data

- [case split(strategy: MLSplitStrategy)](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.enum/split(strategy:))
- [case table(MLDataTable)](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.enum/table(_:))
- [case dataFrame(DataFrame)](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.enum/dataframe(_:))
- [case none](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.enum/none)

##### Accessing parameters

- [var columnSubsample: Double](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/columnsubsample)
- [var earlyStoppingRounds: Int?](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/earlystoppingrounds)
- [var maxDepth: Int](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/maxdepth)
- [var maxIterations: Int](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/maxiterations)
- [var minChildWeight: Double](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/minchildweight)
- [var minLossReduction: Double](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/minlossreduction)
- [var randomSeed: Int](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/randomseed)
- [var rowSubsample: Double](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/rowsubsample)
- [var stepSize: Double](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/stepsize)
- [var validationData: MLDataTable?](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validationdata-swift.property)
- [var validation: MLBoostedTreeRegressor.ModelParameters.ValidationData](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/validation)

##### Describing parameters

- [var description: String](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/description)
- [var debugDescription: String](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.struct/description)
- [let modelParameters: MLBoostedTreeRegressor.ModelParameters](/documentation/createml/mlboostedtreeregressor/modelparameters-swift.property)

#### Describing a boosted tree regressor

- [var description: String](/documentation/createml/mlboostedtreeregressor/description)
- [var debugDescription: String](/documentation/createml/mlboostedtreeregressor/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeregressor/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlboostedtreeregressor/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlboostedtreeregressor/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlboostedtreeregressor/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlboostedtreeregressor/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlboostedtreeregressor/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlboostedtreeregressor/description)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlregressor/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlregressor/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlregressor/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlregressor/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlregressor/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlregressor/description)
- [MLRecommender](/documentation/createml/mlrecommender)

### Creating and training a recommender

- [init(trainingData:userColumn:itemColumn:ratingColumn:parameters:)](/documentation/createml/mlrecommender/init(trainingdata:usercolumn:itemcolumn:ratingcolumn:parameters:))
- [MLRecommender.ModelParameters](/documentation/createml/mlrecommender/modelparameters-swift.struct)

#### Creating parameters

- [init(algorithm: MLRecommender.ModelAlgorithmType, threshold: Double, maxCount: Int, nearestItemsDataFrame: DataFrame?, maxSimilarityIterations: Int)](/documentation/createml/mlrecommender/modelparameters-swift.struct/init(algorithm:threshold:maxcount:nearestitemsdataframe:maxsimilarityiterations:))
- [init(algorithm: MLRecommender.ModelAlgorithmType, threshold: Double, maxCount: Int, nearestItems: MLDataTable?, maxSimilarityIterations: Int)](/documentation/createml/mlrecommender/modelparameters-swift.struct/init(algorithm:threshold:maxcount:nearestitems:maxsimilarityiterations:))
- [MLRecommender.ModelAlgorithmType](/documentation/createml/mlrecommender/modelalgorithmtype)

##### Recommender algorithms

- [case itemSimilarity(MLRecommender.SimilarityType)](/documentation/createml/mlrecommender/modelalgorithmtype/itemsimilarity(_:))
- [MLRecommender.SimilarityType](/documentation/createml/mlrecommender/similaritytype)

###### Similarity types

- [case jaccard](/documentation/createml/mlrecommender/similaritytype/jaccard)
- [case cosine](/documentation/createml/mlrecommender/similaritytype/cosine)
- [case pearson](/documentation/createml/mlrecommender/similaritytype/pearson)

###### Similarity type descriptions

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)
- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)

###### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)

##### Algorithm descriptions

- [var description: String](/documentation/createml/mlrecommender/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mlrecommender/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrecommender/modelalgorithmtype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrecommender/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrecommender/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlrecommender/modelalgorithmtype/description)

#### Configuring the parameters

- [var algorithm: MLRecommender.ModelAlgorithmType](/documentation/createml/mlrecommender/modelparameters-swift.struct/algorithm)
- [var maxCount: Int](/documentation/createml/mlrecommender/modelparameters-swift.struct/maxcount)
- [var maxSimilarityIterations: Int](/documentation/createml/mlrecommender/modelparameters-swift.struct/maxsimilarityiterations)
- [var threshold: Double](/documentation/createml/mlrecommender/modelparameters-swift.struct/threshold)
- [var nearestItems: MLDataTable?](/documentation/createml/mlrecommender/modelparameters-swift.struct/nearestitems)
- [var nearestItemsDataFrame: DataFrame?](/documentation/createml/mlrecommender/modelparameters-swift.struct/nearestitemsdataframe)
- [let modelParameters: MLRecommender.ModelParameters](/documentation/createml/mlrecommender/modelparameters-swift.property)
- [var userIdentifierColumn: String](/documentation/createml/mlrecommender/useridentifiercolumn)
- [var itemIdentifierColumn: String](/documentation/createml/mlrecommender/itemidentifiercolumn)
- [var ratingColumn: String?](/documentation/createml/mlrecommender/ratingcolumn)

### Evaluating a recommender

- [func evaluation(on:userColumn:itemColumn:ratingColumn:cutoffs:excludingObserved:)](/documentation/createml/mlrecommender/evaluation(on:usercolumn:itemcolumn:ratingcolumn:cutoffs:excludingobserved:))
- [MLRecommenderMetrics](/documentation/createml/mlrecommendermetrics)

#### Assessing the model

- [let excludingObserved: Bool](/documentation/createml/mlrecommendermetrics/excludingobserved)
- [var precisionRecall: MLDataTable](/documentation/createml/mlrecommendermetrics/precisionrecall)
- [var precisionRecallDataFrame: DataFrame](/documentation/createml/mlrecommendermetrics/precisionrecalldataframe)

#### Handling errors

- [var isValid: Bool](/documentation/createml/mlrecommendermetrics/isvalid)
- [let error: (any Error)?](/documentation/createml/mlrecommendermetrics/error)

#### Creating metrics

- [init(precisionRecall: MLDataTable, excludingObserved: Bool)](/documentation/createml/mlrecommendermetrics/init(precisionrecall:excludingobserved:))

### Testing a recommender

- [func recommendations(fromUsers:maxCount:restrictingToItems:excluding:excludingObserved:)](/documentation/createml/mlrecommender/recommendations(fromusers:maxcount:restrictingtoitems:excluding:excludingobserved:))
- [MLIdentifier](/documentation/createml/mlidentifier)

#### Getting an identifier

- [var identifierValue: MLDataValue](/documentation/createml/mlidentifier/identifiervalue)
- [func getSimilarItems(fromItems:maxCount:)](/documentation/createml/mlrecommender/getsimilaritems(fromitems:maxcount:))

### Saving a recommender

- [func write(to: URL, metadata: MLModelMetadata?) throws](/documentation/createml/mlrecommender/write(to:metadata:))
- [func write(toFile: String, metadata: MLModelMetadata?) throws](/documentation/createml/mlrecommender/write(tofile:metadata:))

### Describing a recommender

- [var model: MLModel](/documentation/createml/mlrecommender/model)

### Supporting types

- [MLRecommender.ModelAlgorithmType](/documentation/createml/mlrecommender/modelalgorithmtype)

#### Recommender algorithms

- [case itemSimilarity(MLRecommender.SimilarityType)](/documentation/createml/mlrecommender/modelalgorithmtype/itemsimilarity(_:))
- [MLRecommender.SimilarityType](/documentation/createml/mlrecommender/similaritytype)

##### Similarity types

- [case jaccard](/documentation/createml/mlrecommender/similaritytype/jaccard)
- [case cosine](/documentation/createml/mlrecommender/similaritytype/cosine)
- [case pearson](/documentation/createml/mlrecommender/similaritytype/pearson)

##### Similarity type descriptions

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)
- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)

#### Algorithm descriptions

- [var description: String](/documentation/createml/mlrecommender/modelalgorithmtype/description)
- [var debugDescription: String](/documentation/createml/mlrecommender/modelalgorithmtype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrecommender/modelalgorithmtype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrecommender/modelalgorithmtype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrecommender/modelalgorithmtype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrecommender/modelalgorithmtype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlrecommender/modelalgorithmtype/description)
- [MLRecommender.SimilarityType](/documentation/createml/mlrecommender/similaritytype)

#### Similarity types

- [case jaccard](/documentation/createml/mlrecommender/similaritytype/jaccard)
- [case cosine](/documentation/createml/mlrecommender/similaritytype/cosine)
- [case pearson](/documentation/createml/mlrecommender/similaritytype/pearson)

#### Similarity type descriptions

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)
- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mlrecommender/similaritytype/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlrecommender/similaritytype/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlrecommender/similaritytype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mlrecommender/similaritytype/description)

## Tabular data

- [MLDataTable](/documentation/createml/mldatatable)

### Creating a data table

- [Creating a model from tabular data](/documentation/createml/creating-a-model-from-tabular-data)
- [init(contentsOf: URL, options: MLDataTable.ParsingOptions) throws](/documentation/createml/mldatatable/init(contentsof:options:))

#### Parsing options

- [Creating a text classifier model](/documentation/createml/creating-a-text-classifier-model)
- [MLDataTable.ParsingOptions](/documentation/createml/mldatatable/parsingoptions)

##### Creating the CSV parsing options

- [init(containsHeader: Bool, delimiter: String, comment: String, escape: String, doubleQuote: Bool, quote: String, skipInitialSpaces: Bool, missingValues: [String], lineTerminator: String, selectColumns: [String]?, maxRows: Int?, skipRows: Int)](/documentation/createml/mldatatable/parsingoptions/init(containsheader:delimiter:comment:escape:doublequote:quote:skipinitialspaces:missingvalues:lineterminator:selectcolumns:maxrows:skiprows:))

##### Specifying the CSV file format

- [var containsHeader: Bool](/documentation/createml/mldatatable/parsingoptions/containsheader)
- [var delimiter: String](/documentation/createml/mldatatable/parsingoptions/delimiter)
- [var lineTerminator: String](/documentation/createml/mldatatable/parsingoptions/lineterminator)

##### Handling special characters

- [var escape: String](/documentation/createml/mldatatable/parsingoptions/escape)
- [var quote: String](/documentation/createml/mldatatable/parsingoptions/quote)
- [var doubleQuote: Bool](/documentation/createml/mldatatable/parsingoptions/doublequote)

##### Ignoring CSV components

- [var skipRows: Int](/documentation/createml/mldatatable/parsingoptions/skiprows)
- [var skipInitialSpaces: Bool](/documentation/createml/mldatatable/parsingoptions/skipinitialspaces)
- [var comment: String](/documentation/createml/mldatatable/parsingoptions/comment)

##### Limiting rows and columns

- [var maxRows: Int?](/documentation/createml/mldatatable/parsingoptions/maxrows)
- [var selectColumns: [String]?](/documentation/createml/mldatatable/parsingoptions/selectcolumns)

##### Representing missing values

- [var missingValues: [String]](/documentation/createml/mldatatable/parsingoptions/missingvalues)
- [init(dictionary: [String : any MLDataValueConvertible]) throws](/documentation/createml/mldatatable/init(dictionary:))
- [init(namedColumns: [String : MLUntypedColumn]) throws](/documentation/createml/mldatatable/init(namedcolumns:))
- [init()](/documentation/createml/mldatatable/init())
- [MLDataTable.ParsingOptions](/documentation/createml/mldatatable/parsingoptions)

#### Creating the CSV parsing options

- [init(containsHeader: Bool, delimiter: String, comment: String, escape: String, doubleQuote: Bool, quote: String, skipInitialSpaces: Bool, missingValues: [String], lineTerminator: String, selectColumns: [String]?, maxRows: Int?, skipRows: Int)](/documentation/createml/mldatatable/parsingoptions/init(containsheader:delimiter:comment:escape:doublequote:quote:skipinitialspaces:missingvalues:lineterminator:selectcolumns:maxrows:skiprows:))

#### Specifying the CSV file format

- [var containsHeader: Bool](/documentation/createml/mldatatable/parsingoptions/containsheader)
- [var delimiter: String](/documentation/createml/mldatatable/parsingoptions/delimiter)
- [var lineTerminator: String](/documentation/createml/mldatatable/parsingoptions/lineterminator)

#### Handling special characters

- [var escape: String](/documentation/createml/mldatatable/parsingoptions/escape)
- [var quote: String](/documentation/createml/mldatatable/parsingoptions/quote)
- [var doubleQuote: Bool](/documentation/createml/mldatatable/parsingoptions/doublequote)

#### Ignoring CSV components

- [var skipRows: Int](/documentation/createml/mldatatable/parsingoptions/skiprows)
- [var skipInitialSpaces: Bool](/documentation/createml/mldatatable/parsingoptions/skipinitialspaces)
- [var comment: String](/documentation/createml/mldatatable/parsingoptions/comment)

#### Limiting rows and columns

- [var maxRows: Int?](/documentation/createml/mldatatable/parsingoptions/maxrows)
- [var selectColumns: [String]?](/documentation/createml/mldatatable/parsingoptions/selectcolumns)

#### Representing missing values

- [var missingValues: [String]](/documentation/createml/mldatatable/parsingoptions/missingvalues)

### Getting the size of a data table

- [var size: (rows: Int, columns: Int)](/documentation/createml/mldatatable/size)

### Transforming rows to generate a data column

- [func map(_:)](/documentation/createml/mldatatable/map(_:))

### Adding columns

- [func addColumn(_:named:)](/documentation/createml/mldatatable/addcolumn(_:named:))
- [MLDataColumn](/documentation/createml/mldatacolumn)

#### Creating a data column

- [init(repeating:count:)](/documentation/createml/mldatacolumn/init(repeating:count:))
- [init<S>(S)](/documentation/createml/mldatacolumn/init(_:))
- [init()](/documentation/createml/mldatacolumn/init())

#### Creating a data column by converting another column

- [func map<T>(to: T.Type) -> MLDataColumn<T>](/documentation/createml/mldatacolumn/map(to:))
- [init(column:)](/documentation/createml/mldatacolumn/init(column:))
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-5rg9u)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-2rxtu)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-86ge9)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-23pmx)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-ztkv)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-8uzuq)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-855l9)
- [init<T>(column: MLDataColumn<T>)](/documentation/createml/mldatacolumn/init(column:)-s8g5)

#### Getting the number of elements

- [var count: Int](/documentation/createml/mldatacolumn/count)
- [var isEmpty: Bool](/documentation/createml/mldatacolumn/isempty)

#### Getting an element

- [subscript(_:)](/documentation/createml/mldatacolumn/subscript(_:))
- [func element(at: Int) -> Element?](/documentation/createml/mldatacolumn/element(at:))

#### Appending to a data column

- [func append(contentsOf: MLDataColumn<Element>)](/documentation/createml/mldatacolumn/append(contentsof:))

#### Duplicating a column

- [func copy() -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/copy())

#### Sorting elements to generate a column

- [func sort(byIncreasingOrder: Bool) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/sort(byincreasingorder:))

#### Transforming elements to generate a column

- [func map(_:)](/documentation/createml/mldatacolumn/map(_:))
- [func mapMissing<T>((Element?) -> T?) -> MLDataColumn<T>](/documentation/createml/mldatacolumn/mapmissing(_:))

#### Masking elements to generate a column

- [subscript(MLDataColumn<Bool>) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/subscript(_:)-78irf)
- [subscript(MLUntypedColumn) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/subscript(_:)-1n3x)

#### Discarding elements to generate a column

- [func dropMissing() -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/dropmissing())
- [func dropDuplicates() -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/dropduplicates())

#### Selecting elements to generate a column

- [subscript(Range<Int>) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/subscript(_:)-pp34)
- [subscript<R>(R) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/subscript(_:)-5mczv)
- [func prefix(Int) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/prefix(_:))
- [func suffix(Int) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/suffix(_:))

#### Filling in missing elements to generate a column

- [func fillMissing(with: Element) -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/fillmissing(with:))

#### Evaluating elements to generate a column

- [func materialize() throws -> MLDataColumn<Element>](/documentation/createml/mldatacolumn/materialize())

#### Combining columns

- [static +(_:_:)](/documentation/createml/mldatacolumn/+(_:_:))
- [static -(_:_:)](/documentation/createml/mldatacolumn/-(_:_:))
- [static *(_:_:)](/documentation/createml/mldatacolumn/*(_:_:))
- [static /(_:_:)](/documentation/createml/mldatacolumn/_(_:_:)-8hxiv)

#### Combining columns to generate a column

- [static func + (MLDataColumn<Int>, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/+(_:_:)-24g38)
- [static func + (MLDataColumn<Double>, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/+(_:_:)-q5bb)
- [static func - (MLDataColumn<Int>, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/-(_:_:)-11hbf)
- [static func - (MLDataColumn<Double>, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/-(_:_:)-3mwsr)
- [static func * (MLDataColumn<Int>, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/*(_:_:)-40smy)
- [static func * (MLDataColumn<Double>, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/*(_:_:)-lchb)
- [static func / (MLDataColumn<Int>, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/_(_:_:)-5uxby)
- [static func / (MLDataColumn<Double>, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/_(_:_:)-69vgc)

#### Combining a column with a value to generate a column

- [static func + (MLDataColumn<Int>, Int) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/+(_:_:)-7tghu)
- [static func + (MLDataColumn<Double>, Double) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/+(_:_:)-4se2l)
- [static func - (MLDataColumn<Int>, Int) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/-(_:_:)-2sddu)
- [static func - (MLDataColumn<Double>, Double) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/-(_:_:)-9smok)
- [static func * (MLDataColumn<Int>, Int) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/*(_:_:)-2zih0)
- [static func * (MLDataColumn<Double>, Double) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/*(_:_:)-4ilhj)
- [static func / (MLDataColumn<Int>, Int) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/_(_:_:)-3ea6t)
- [static func / (MLDataColumn<Double>, Double) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/_(_:_:)-8k8ao)

#### Combining a value with a column to generate a column

- [static func + (Int, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/+(_:_:)-2zcp)
- [static func + (Double, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/+(_:_:)-9r67n)
- [static func - (Int, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/-(_:_:)-507l8)
- [static func - (Double, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/-(_:_:)-2e7k4)
- [static func * (Int, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/*(_:_:)-48xte)
- [static func * (Double, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/*(_:_:)-9sysp)
- [static func / (Int, MLDataColumn<Int>) -> MLDataColumn<Int>](/documentation/createml/mldatacolumn/_(_:_:)-9ew9w)
- [static func / (Double, MLDataColumn<Double>) -> MLDataColumn<Double>](/documentation/createml/mldatacolumn/_(_:_:)-121w8)

#### Comparing columns

- [static ==(_:_:)](/documentation/createml/mldatacolumn/==(_:_:))
- [static !=(_:_:)](/documentation/createml/mldatacolumn/!=(_:_:))
- [static <(_:_:)](/documentation/createml/mldatacolumn/_(_:_:)-81qel)
- [static <=(_:_:)](/documentation/createml/mldatacolumn/_=(_:_:)-8eq6v)
- [static >(_:_:)](/documentation/createml/mldatacolumn/_(_:_:)-g252)
- [static >=(_:_:)](/documentation/createml/mldatacolumn/_=(_:_:)-64izf)

#### Comparing columns to generate a column of booleans

- [static func == (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/==(_:_:)-9e3tx)
- [static func != (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/!=(_:_:)-1vu4e)
- [static func < (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-3om6w)
- [static func <= (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-6s5v1)
- [static func > (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-2dym4)
- [static func >= (MLDataColumn<Element>, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-4w60p)

#### Comparing a column with a value to generate a column of booleans

- [static func == (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/==(_:_:)-7clbs)
- [static func != (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/!=(_:_:)-4jp0y)
- [static func < (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-4ujss)
- [static func <= (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-86x3a)
- [static func > (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-ebgq)
- [static func >= (MLDataColumn<Element>, Element) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-1ctuz)

#### Comparing a value with a column to generate a column of booleans

- [static func == (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/==(_:_:)-6zz2o)
- [static func != (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/!=(_:_:)-4477j)
- [static func < (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-33lwa)
- [static func <= (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-3fx6w)
- [static func > (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_(_:_:)-6irjn)
- [static func >= (Element, MLDataColumn<Element>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/_=(_:_:)-8e3ur)

#### Combining columns of booleans to generate a column of booleans

- [static func && (MLDataColumn<Bool>, MLDataColumn<Bool>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/&&(_:_:))
- [static func || (MLDataColumn<Bool>, MLDataColumn<Bool>) -> MLDataColumn<Bool>](/documentation/createml/mldatacolumn/__(_:_:))

#### Getting the min and max element values

- [func min()](/documentation/createml/mldatacolumn/min())
- [func max()](/documentation/createml/mldatacolumn/max())

#### Getting sum, mean, and standard deviation values

- [func sum()](/documentation/createml/mldatacolumn/sum())
- [func mean()](/documentation/createml/mldatacolumn/mean())
- [func std()](/documentation/createml/mldatacolumn/std())
- [func stdev()](/documentation/createml/mldatacolumn/stdev())

#### Visualizing a column

- [func show() -> any MLStreamingVisualizable](/documentation/createml/mldatacolumn/show())

#### Getting a description of a data column

- [var description: String](/documentation/createml/mldatacolumn/description)
- [var playgroundDescription: Any](/documentation/createml/mldatacolumn/playgrounddescription)
- [var debugDescription: String](/documentation/createml/mldatacolumn/debugdescription)

#### Handling data column errors

- [var isValid: Bool](/documentation/createml/mldatacolumn/isvalid)
- [var error: (any Error)?](/documentation/createml/mldatacolumn/error)

#### Supporting types

- [MLUntypedColumn](/documentation/createml/mluntypedcolumn)

##### Creating an untyped column

- [init(repeating:count:)](/documentation/createml/mluntypedcolumn/init(repeating:count:))
- [init<T>(repeating: T, count: Int)](/documentation/createml/mluntypedcolumn/init(repeating:count:)-7ttf1)
- [init(repeating: MLDataValue, count: Int)](/documentation/createml/mluntypedcolumn/init(repeating:count:)-q8yk)
- [init(_:)](/documentation/createml/mluntypedcolumn/init(_:))
- [init(Range<Int>)](/documentation/createml/mluntypedcolumn/init(_:)-33tcv)
- [init(ClosedRange<Int>)](/documentation/createml/mluntypedcolumn/init(_:)-9no5)
- [init<S>(S)](/documentation/createml/mluntypedcolumn/init(_:)-ag8f)
- [init<S>(S)](/documentation/createml/mluntypedcolumn/init(_:)-5by2g)
- [init()](/documentation/createml/mluntypedcolumn/init())

##### Creating an untyped column by converting another column

- [init(ints: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(ints:))
- [init(doubles: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(doubles:))
- [init(strings: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(strings:))
- [init(sequences: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(sequences:))
- [init(dictionaries: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(dictionaries:))
- [init(multiArrays: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(multiarrays:))

##### Getting the number of elements

- [var count: Int](/documentation/createml/mluntypedcolumn/count)
- [var isEmpty: Bool](/documentation/createml/mluntypedcolumn/isempty)

##### Getting an element

- [subscript(Int) -> MLDataValue](/documentation/createml/mluntypedcolumn/subscript(_:)-6j6rb)

##### Appending to an untyped column

- [func append(contentsOf: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/append(contentsof:))

##### Duplicating a column

- [func copy() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/copy())

##### Sorting elements to generate a column

- [func sort(byIncreasingOrder: Bool) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/sort(byincreasingorder:))

##### Converting a column to generate a data column

- [func map<T>(to: T.Type) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(to:))

##### Exposing the underlying type to generate a data column

- [var type: MLDataValue.ValueType](/documentation/createml/mluntypedcolumn/type)
- [var ints: MLDataColumn<Int>?](/documentation/createml/mluntypedcolumn/ints)
- [var doubles: MLDataColumn<Double>?](/documentation/createml/mluntypedcolumn/doubles)
- [var strings: MLDataColumn<String>?](/documentation/createml/mluntypedcolumn/strings)
- [var sequences: MLDataColumn<MLDataValue.SequenceType>?](/documentation/createml/mluntypedcolumn/sequences)
- [var dictionaries: MLDataColumn<MLDataValue.DictionaryType>?](/documentation/createml/mluntypedcolumn/dictionaries)
- [var multiArrays: MLDataColumn<MLDataValue.MultiArrayType>?](/documentation/createml/mluntypedcolumn/multiarrays)
- [func column<T>(type: T.Type) -> MLDataColumn<T>?](/documentation/createml/mluntypedcolumn/column(type:))

##### Transforming elements to generate a data column

- [func map(_:)](/documentation/createml/mluntypedcolumn/map(_:))
- [func map<T>((MLDataValue) -> T) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(_:)-139qy)
- [func map<T>((MLDataValue) -> T?) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(_:)-9v61j)
- [func mapMissing<T>((MLDataValue) -> T?) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/mapmissing(_:))

##### Masking elements to generate an untyped column

- [subscript(_:)](/documentation/createml/mluntypedcolumn/subscript(_:))
- [subscript(MLDataColumn<Bool>) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-8ot43)
- [subscript(MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-9hr32)

##### Discarding elements to generate an untyped column

- [func dropMissing() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/dropmissing())
- [func dropDuplicates() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/dropduplicates())

##### Selecting elements to generate an untyped column

- [subscript(Range<Int>) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-33ua2)
- [subscript<R>(R) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-9dpy7)
- [func prefix(Int) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/prefix(_:))
- [func suffix(Int) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/suffix(_:))

##### Filling in missing elements to generate an untyped column

- [func fillMissing(with: MLDataValue) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/fillmissing(with:))

##### Evaluating elements to generate an untyped column

- [func materialize() throws -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/materialize())

##### Combining columns

- [static +(_:_:)](/documentation/createml/mluntypedcolumn/+(_:_:))
- [static -(_:_:)](/documentation/createml/mluntypedcolumn/-(_:_:))
- [static *(_:_:)](/documentation/createml/mluntypedcolumn/*(_:_:))
- [static /(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-20v6v)

##### Combining columns to generate an untyped column

- [static func + (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-bcc5)
- [static func - (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-3h4o4)
- [static func * (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-2p6nm)
- [static func / (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-45tpp)

##### Combining a column with a value to generate an untyped column

- [static func + (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-4vnbk)
- [static func - (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-4uigi)
- [static func * (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-6gnlx)
- [static func / (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-18srk)

##### Combining a value with a column to generate an untyped column

- [static func + (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-miqp)
- [static func - (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-9gm9i)
- [static func * (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-7svdc)
- [static func / (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-aw9o)

##### Comparing columns

- [static ==(_:_:)](/documentation/createml/mluntypedcolumn/==(_:_:))
- [static !=(_:_:)](/documentation/createml/mluntypedcolumn/!=(_:_:))
- [static >(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-1hr3j)
- [static <(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-9ke05)
- [static <=(_:_:)](/documentation/createml/mluntypedcolumn/_=(_:_:)-2i3xz)
- [static >=(_:_:)](/documentation/createml/mluntypedcolumn/_=(_:_:)-221lt)

##### Comparing columns to generate an untyped column of booleans

- [static func == (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-3o7mo)
- [static func != (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-86hu4)
- [static func > (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-9r2zq)
- [static func < (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-7zms0)
- [static func <= (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-5xmwz)
- [static func >= (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-4u3ir)

##### Comparing a column with a value to generate an untyped column of booleans

- [static func == (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-7xysh)
- [static func != (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-7do9)
- [static func > (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-2mdrt)
- [static func < (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-8w60f)
- [static func <= (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-1wkt3)
- [static func >= (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-2vu3g)

##### Comparing a value with a column to generate an untyped column of booleans

- [static func == (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-6z88q)
- [static func != (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-6k3p6)
- [static func > (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-52drj)
- [static func < (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-6qou9)
- [static func <= (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-t4bt)
- [static func >= (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-6yycf)

##### Combining columns of booleans to generate an untyped column of booleans

- [static func && (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/&&(_:_:))
- [static func || (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/__(_:_:))

##### Visualizing a column

- [func show() -> any MLStreamingVisualizable](/documentation/createml/mluntypedcolumn/show())

##### Getting a description of an untyped column

- [var description: String](/documentation/createml/mluntypedcolumn/description)
- [var playgroundDescription: Any](/documentation/createml/mluntypedcolumn/playgrounddescription)
- [var debugDescription: String](/documentation/createml/mluntypedcolumn/debugdescription)
- [var customMirror: Mirror](/documentation/createml/mluntypedcolumn/custommirror)

##### Handling untyped column errors

- [var isValid: Bool](/documentation/createml/mluntypedcolumn/isvalid)
- [var error: (any Error)?](/documentation/createml/mluntypedcolumn/error)

##### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mluntypedcolumn/customdebugstringconvertible-implementations)

###### Instance Properties

- [var debugDescription: String](/documentation/createml/mluntypedcolumn/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mluntypedcolumn/customplaygrounddisplayconvertible-implementations)

###### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mluntypedcolumn/playgrounddescription)
- [CustomReflectable Implementations](/documentation/createml/mluntypedcolumn/customreflectable-implementations)

###### Instance Properties

- [var customMirror: Mirror](/documentation/createml/mluntypedcolumn/custommirror)
- [CustomStringConvertible Implementations](/documentation/createml/mluntypedcolumn/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/createml/mluntypedcolumn/description)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldatacolumn/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mldatacolumn/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldatacolumn/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldatacolumn/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldatacolumn/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mldatacolumn/description)
- [MLUntypedColumn](/documentation/createml/mluntypedcolumn)

#### Creating an untyped column

- [init(repeating:count:)](/documentation/createml/mluntypedcolumn/init(repeating:count:))
- [init<T>(repeating: T, count: Int)](/documentation/createml/mluntypedcolumn/init(repeating:count:)-7ttf1)
- [init(repeating: MLDataValue, count: Int)](/documentation/createml/mluntypedcolumn/init(repeating:count:)-q8yk)
- [init(_:)](/documentation/createml/mluntypedcolumn/init(_:))
- [init(Range<Int>)](/documentation/createml/mluntypedcolumn/init(_:)-33tcv)
- [init(ClosedRange<Int>)](/documentation/createml/mluntypedcolumn/init(_:)-9no5)
- [init<S>(S)](/documentation/createml/mluntypedcolumn/init(_:)-ag8f)
- [init<S>(S)](/documentation/createml/mluntypedcolumn/init(_:)-5by2g)
- [init()](/documentation/createml/mluntypedcolumn/init())

#### Creating an untyped column by converting another column

- [init(ints: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(ints:))
- [init(doubles: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(doubles:))
- [init(strings: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(strings:))
- [init(sequences: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(sequences:))
- [init(dictionaries: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(dictionaries:))
- [init(multiArrays: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/init(multiarrays:))

#### Getting the number of elements

- [var count: Int](/documentation/createml/mluntypedcolumn/count)
- [var isEmpty: Bool](/documentation/createml/mluntypedcolumn/isempty)

#### Getting an element

- [subscript(Int) -> MLDataValue](/documentation/createml/mluntypedcolumn/subscript(_:)-6j6rb)

#### Appending to an untyped column

- [func append(contentsOf: MLUntypedColumn)](/documentation/createml/mluntypedcolumn/append(contentsof:))

#### Duplicating a column

- [func copy() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/copy())

#### Sorting elements to generate a column

- [func sort(byIncreasingOrder: Bool) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/sort(byincreasingorder:))

#### Converting a column to generate a data column

- [func map<T>(to: T.Type) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(to:))

#### Exposing the underlying type to generate a data column

- [var type: MLDataValue.ValueType](/documentation/createml/mluntypedcolumn/type)
- [var ints: MLDataColumn<Int>?](/documentation/createml/mluntypedcolumn/ints)
- [var doubles: MLDataColumn<Double>?](/documentation/createml/mluntypedcolumn/doubles)
- [var strings: MLDataColumn<String>?](/documentation/createml/mluntypedcolumn/strings)
- [var sequences: MLDataColumn<MLDataValue.SequenceType>?](/documentation/createml/mluntypedcolumn/sequences)
- [var dictionaries: MLDataColumn<MLDataValue.DictionaryType>?](/documentation/createml/mluntypedcolumn/dictionaries)
- [var multiArrays: MLDataColumn<MLDataValue.MultiArrayType>?](/documentation/createml/mluntypedcolumn/multiarrays)
- [func column<T>(type: T.Type) -> MLDataColumn<T>?](/documentation/createml/mluntypedcolumn/column(type:))

#### Transforming elements to generate a data column

- [func map(_:)](/documentation/createml/mluntypedcolumn/map(_:))
- [func map<T>((MLDataValue) -> T) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(_:)-139qy)
- [func map<T>((MLDataValue) -> T?) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/map(_:)-9v61j)
- [func mapMissing<T>((MLDataValue) -> T?) -> MLDataColumn<T>](/documentation/createml/mluntypedcolumn/mapmissing(_:))

#### Masking elements to generate an untyped column

- [subscript(_:)](/documentation/createml/mluntypedcolumn/subscript(_:))
- [subscript(MLDataColumn<Bool>) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-8ot43)
- [subscript(MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-9hr32)

#### Discarding elements to generate an untyped column

- [func dropMissing() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/dropmissing())
- [func dropDuplicates() -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/dropduplicates())

#### Selecting elements to generate an untyped column

- [subscript(Range<Int>) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-33ua2)
- [subscript<R>(R) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/subscript(_:)-9dpy7)
- [func prefix(Int) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/prefix(_:))
- [func suffix(Int) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/suffix(_:))

#### Filling in missing elements to generate an untyped column

- [func fillMissing(with: MLDataValue) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/fillmissing(with:))

#### Evaluating elements to generate an untyped column

- [func materialize() throws -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/materialize())

#### Combining columns

- [static +(_:_:)](/documentation/createml/mluntypedcolumn/+(_:_:))
- [static -(_:_:)](/documentation/createml/mluntypedcolumn/-(_:_:))
- [static *(_:_:)](/documentation/createml/mluntypedcolumn/*(_:_:))
- [static /(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-20v6v)

#### Combining columns to generate an untyped column

- [static func + (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-bcc5)
- [static func - (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-3h4o4)
- [static func * (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-2p6nm)
- [static func / (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-45tpp)

#### Combining a column with a value to generate an untyped column

- [static func + (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-4vnbk)
- [static func - (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-4uigi)
- [static func * (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-6gnlx)
- [static func / (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-18srk)

#### Combining a value with a column to generate an untyped column

- [static func + (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/+(_:_:)-miqp)
- [static func - (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/-(_:_:)-9gm9i)
- [static func * (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/*(_:_:)-7svdc)
- [static func / (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-aw9o)

#### Comparing columns

- [static ==(_:_:)](/documentation/createml/mluntypedcolumn/==(_:_:))
- [static !=(_:_:)](/documentation/createml/mluntypedcolumn/!=(_:_:))
- [static >(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-1hr3j)
- [static <(_:_:)](/documentation/createml/mluntypedcolumn/_(_:_:)-9ke05)
- [static <=(_:_:)](/documentation/createml/mluntypedcolumn/_=(_:_:)-2i3xz)
- [static >=(_:_:)](/documentation/createml/mluntypedcolumn/_=(_:_:)-221lt)

#### Comparing columns to generate an untyped column of booleans

- [static func == (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-3o7mo)
- [static func != (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-86hu4)
- [static func > (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-9r2zq)
- [static func < (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-7zms0)
- [static func <= (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-5xmwz)
- [static func >= (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-4u3ir)

#### Comparing a column with a value to generate an untyped column of booleans

- [static func == (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-7xysh)
- [static func != (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-7do9)
- [static func > (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-2mdrt)
- [static func < (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-8w60f)
- [static func <= (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-1wkt3)
- [static func >= (MLUntypedColumn, any MLDataValueConvertible) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-2vu3g)

#### Comparing a value with a column to generate an untyped column of booleans

- [static func == (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/==(_:_:)-6z88q)
- [static func != (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/!=(_:_:)-6k3p6)
- [static func > (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-52drj)
- [static func < (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_(_:_:)-6qou9)
- [static func <= (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-t4bt)
- [static func >= (any MLDataValueConvertible, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/_=(_:_:)-6yycf)

#### Combining columns of booleans to generate an untyped column of booleans

- [static func && (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/&&(_:_:))
- [static func || (MLUntypedColumn, MLUntypedColumn) -> MLUntypedColumn](/documentation/createml/mluntypedcolumn/__(_:_:))

#### Visualizing a column

- [func show() -> any MLStreamingVisualizable](/documentation/createml/mluntypedcolumn/show())

#### Getting a description of an untyped column

- [var description: String](/documentation/createml/mluntypedcolumn/description)
- [var playgroundDescription: Any](/documentation/createml/mluntypedcolumn/playgrounddescription)
- [var debugDescription: String](/documentation/createml/mluntypedcolumn/debugdescription)
- [var customMirror: Mirror](/documentation/createml/mluntypedcolumn/custommirror)

#### Handling untyped column errors

- [var isValid: Bool](/documentation/createml/mluntypedcolumn/isvalid)
- [var error: (any Error)?](/documentation/createml/mluntypedcolumn/error)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mluntypedcolumn/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mluntypedcolumn/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mluntypedcolumn/customplaygrounddisplayconvertible-implementations)

##### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mluntypedcolumn/playgrounddescription)
- [CustomReflectable Implementations](/documentation/createml/mluntypedcolumn/customreflectable-implementations)

##### Instance Properties

- [var customMirror: Mirror](/documentation/createml/mluntypedcolumn/custommirror)
- [CustomStringConvertible Implementations](/documentation/createml/mluntypedcolumn/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mluntypedcolumn/description)

### Accessing columns

- [subscript(_:)](/documentation/createml/mldatatable/subscript(_:))
- [subscript<T>(String, T.Type) -> MLDataColumn<T>?](/documentation/createml/mldatatable/subscript(_:_:))

### Renaming columns

- [func renameColumn(named: String, to: String)](/documentation/createml/mldatatable/renamecolumn(named:to:))

### Removing columns

- [func removeColumn(named: String)](/documentation/createml/mldatatable/removecolumn(named:))

### Appending to a data table

- [func append(contentsOf: MLDataTable)](/documentation/createml/mldatatable/append(contentsof:))

### Generating new data tables

- [Data table derivation operations](/documentation/createml/data-table-derivation-operations)

#### Aggregating rows

- [func group<S>(columnsNamed: String..., aggregators: S) -> MLDataTable](/documentation/createml/mldatatable/group(columnsnamed:aggregators:))
- [MLDataTable.Aggregator](/documentation/createml/mldatatable/aggregator)

##### Creating an aggregator

- [init(operations: MLDataTable.Aggregator.Operations..., of: String)](/documentation/createml/mldatatable/aggregator/init(operations:of:))

##### Configuring an aggregator

- [var columnName: String](/documentation/createml/mldatatable/aggregator/columnname)
- [var operations: [MLDataTable.Aggregator.Operations]](/documentation/createml/mldatatable/aggregator/operations-swift.property)
- [MLDataTable.Aggregator.Operations](/documentation/createml/mldatatable/aggregator/operations-swift.enum)

###### Aggregation operations

- [case min](/documentation/createml/mldatatable/aggregator/operations-swift.enum/min)
- [case max](/documentation/createml/mldatatable/aggregator/operations-swift.enum/max)
- [case sum](/documentation/createml/mldatatable/aggregator/operations-swift.enum/sum)
- [case mean](/documentation/createml/mldatatable/aggregator/operations-swift.enum/mean)
- [case stdev](/documentation/createml/mldatatable/aggregator/operations-swift.enum/stdev)
- [case variance](/documentation/createml/mldatatable/aggregator/operations-swift.enum/variance)
- [case count](/documentation/createml/mldatatable/aggregator/operations-swift.enum/count)
- [case distinctCount](/documentation/createml/mldatatable/aggregator/operations-swift.enum/distinctcount)
- [case randomlySelectOne](/documentation/createml/mldatatable/aggregator/operations-swift.enum/randomlyselectone)
- [case sequenceMerge](/documentation/createml/mldatatable/aggregator/operations-swift.enum/sequencemerge)
- [case dictionaryMerge(valueColumn: String)](/documentation/createml/mldatatable/aggregator/operations-swift.enum/dictionarymerge(valuecolumn:))
- [case argmin(outputColumn: String)](/documentation/createml/mldatatable/aggregator/operations-swift.enum/argmin(outputcolumn:))
- [case argmax(outputColumn: String)](/documentation/createml/mldatatable/aggregator/operations-swift.enum/argmax(outputcolumn:))

#### Sorting rows

- [func sort(columnNamed: String, byIncreasingOrder: Bool) -> MLDataTable](/documentation/createml/mldatatable/sort(columnnamed:byincreasingorder:))

#### Splitting a data table

- [func randomSplit(by: Double, seed: Int) -> (MLDataTable, MLDataTable)](/documentation/createml/mldatatable/randomsplit(by:seed:))

#### Merging data tables

- [func join(with: MLDataTable, on: String..., type: MLDataTable.JoinType) -> MLDataTable](/documentation/createml/mldatatable/join(with:on:type:))
- [MLDataTable.JoinType](/documentation/createml/mldatatable/jointype)

##### Selecting a joining operation

- [case inner](/documentation/createml/mldatatable/jointype/inner)
- [case left](/documentation/createml/mldatatable/jointype/left)
- [case right](/documentation/createml/mldatatable/jointype/right)
- [case outer](/documentation/createml/mldatatable/jointype/outer)

#### Filling in missing values

- [func fillMissing(columnNamed: String, with: MLDataValue) -> MLDataTable](/documentation/createml/mldatatable/fillmissing(columnnamed:with:))

#### Masking rows

- [subscript(MLDataColumn<Bool>) -> MLDataTable](/documentation/createml/mldatatable/subscript(_:)-3opgl)
- [subscript(MLUntypedColumn) -> MLDataTable](/documentation/createml/mldatatable/subscript(_:)-10r4l)

#### Discarding rows

- [func dropMissing() -> MLDataTable](/documentation/createml/mldatatable/dropmissing())
- [func dropDuplicates() -> MLDataTable](/documentation/createml/mldatatable/dropduplicates())
- [func exclude<T>(T..., of: String) -> MLDataTable](/documentation/createml/mldatatable/exclude(_:of:))
- [func randomSample(by: Double, seed: Int) -> MLDataTable](/documentation/createml/mldatatable/randomsample(by:seed:))

#### Selecting rows

- [subscript(Range<Int>) -> MLDataTable](/documentation/createml/mldatatable/subscript(_:)-7h4j3)
- [subscript<R>(R) -> MLDataTable](/documentation/createml/mldatatable/subscript(_:)-5le8a)
- [func prefix(Int) -> MLDataTable](/documentation/createml/mldatatable/prefix(_:))
- [func suffix(Int) -> MLDataTable](/documentation/createml/mldatatable/suffix(_:))
- [func intersect<T>(T..., of: String) -> MLDataTable](/documentation/createml/mldatatable/intersect(_:of:))

#### Selecting columns

- [subscript<S>(S) -> MLDataTable](/documentation/createml/mldatatable/subscript(_:)-2wkan)

#### Compacting rows

- [func condense(columnNamed: String, to: String) -> MLDataTable](/documentation/createml/mldatatable/condense(columnnamed:to:))

#### Expanding rows

- [func expand(columnNamed: String, to: String) -> MLDataTable](/documentation/createml/mldatatable/expand(columnnamed:to:))

#### Compacting columns

- [func pack(columnsNamed: String..., to: String, type: MLDataTable.PackType, filling: MLDataValue) -> MLDataTable](/documentation/createml/mldatatable/pack(columnsnamed:to:type:filling:))
- [MLDataTable.PackType](/documentation/createml/mldatatable/packtype)

##### Selecting a packing operation

- [case sequence](/documentation/createml/mldatatable/packtype/sequence)
- [case dictionary](/documentation/createml/mldatatable/packtype/dictionary)

#### Expanding columns

- [func unpack(columnNamed: String, valueTypes: [MLDataValue.ValueType]?, indexSubset: [Int]?, keySubset: [String]?) -> MLDataTable](/documentation/createml/mldatatable/unpack(columnnamed:valuetypes:indexsubset:keysubset:))

### Splitting a data table

- [func randomSplitBySequence(proportion: Double, by: String, on: String, seed: Int) -> (MLDataTable, remaining: MLDataTable)](/documentation/createml/mldatatable/randomsplitbysequence(proportion:by:on:seed:))
- [func stratifiedSplit<RNG>(proportions: [Double], on: String, generator: inout RNG) throws -> MLDataTable](/documentation/createml/mldatatable/stratifiedsplit(proportions:on:generator:))
- [func stratifiedSplit(proportions: [Double], on: String, seed: Int) throws -> MLDataTable](/documentation/createml/mldatatable/stratifiedsplit(proportions:on:seed:))
- [func stratifiedSplitBySequence<RNG>(proportions: [Double], by: String, on: String, generator: inout RNG) throws -> MLDataTable](/documentation/createml/mldatatable/stratifiedsplitbysequence(proportions:by:on:generator:))
- [func stratifiedSplitBySequence(proportions: [Double], by: String, on: String, seed: Int) throws -> MLDataTable](/documentation/createml/mldatatable/stratifiedsplitbysequence(proportions:by:on:seed:))

### Getting information about a data table’s rows

- [MLDataTable.Row](/documentation/createml/mldatatable/row)

#### Accessing parameters

- [var keys: MLDataTable.Row.Keys](/documentation/createml/mldatatable/row/keys-swift.property)
- [var values: MLDataTable.Row.Values](/documentation/createml/mldatatable/row/values-swift.property)
- [MLDataTable.Row.Key](/documentation/createml/mldatatable/row/key)
- [MLDataTable.Row.Keys](/documentation/createml/mldatatable/row/keys-swift.typealias)
- [MLDataTable.Row.Value](/documentation/createml/mldatatable/row/value)
- [MLDataTable.Row.Values](/documentation/createml/mldatatable/row/values-swift.struct)

##### Accessing columns

- [subscript(MLDataTable.Row.Key) -> MLDataTable.Row.Value?](/documentation/createml/mldatatable/row/subscript(_:))

#### Getting a row

- [func index(forKey: MLDataTable.Row.Key) -> MLDataTable.Row.Index?](/documentation/createml/mldatatable/row/index(forkey:))

#### Accessing rows

- [subscript(MLDataTable.Row.Key) -> MLDataTable.Row.Value?](/documentation/createml/mldatatable/row/subscript(_:))
- [subscript<T>(MLDataTable.Row.Key, T.Type) -> T?](/documentation/createml/mldatatable/row/subscript(_:_:))
- [var rows: MLDataTable.Rows](/documentation/createml/mldatatable/rows-swift.property)
- [MLDataTable.Rows](/documentation/createml/mldatatable/rows-swift.struct)

#### Accessing rows

- [subscript(Int) -> MLDataTable.Rows.Element](/documentation/createml/mldatatable/rows-swift.struct/subscript(_:))

#### Manipulating indices

- [var startIndex: Int](/documentation/createml/mldatatable/rows-swift.struct/startindex)
- [var endIndex: Int](/documentation/createml/mldatatable/rows-swift.struct/endindex)

#### Supporting types

- [MLDataTable.Row](/documentation/createml/mldatatable/row)

##### Accessing parameters

- [var keys: MLDataTable.Row.Keys](/documentation/createml/mldatatable/row/keys-swift.property)
- [var values: MLDataTable.Row.Values](/documentation/createml/mldatatable/row/values-swift.property)
- [MLDataTable.Row.Key](/documentation/createml/mldatatable/row/key)
- [MLDataTable.Row.Keys](/documentation/createml/mldatatable/row/keys-swift.typealias)
- [MLDataTable.Row.Value](/documentation/createml/mldatatable/row/value)
- [MLDataTable.Row.Values](/documentation/createml/mldatatable/row/values-swift.struct)

###### Accessing columns

- [subscript(MLDataTable.Row.Key) -> MLDataTable.Row.Value?](/documentation/createml/mldatatable/row/subscript(_:))

##### Getting a row

- [func index(forKey: MLDataTable.Row.Key) -> MLDataTable.Row.Index?](/documentation/createml/mldatatable/row/index(forkey:))

##### Accessing rows

- [subscript(MLDataTable.Row.Key) -> MLDataTable.Row.Value?](/documentation/createml/mldatatable/row/subscript(_:))
- [subscript<T>(MLDataTable.Row.Key, T.Type) -> T?](/documentation/createml/mldatatable/row/subscript(_:_:))
- [MLDataTable.Rows.Element](/documentation/createml/mldatatable/rows-swift.struct/element)

#### Default Implementations

- [RandomAccessCollection Implementations](/documentation/createml/mldatatable/rows-swift.struct/randomaccesscollection-implementations)

##### Instance Properties

- [var endIndex: Int](/documentation/createml/mldatatable/rows-swift.struct/endindex)
- [var startIndex: Int](/documentation/createml/mldatatable/rows-swift.struct/startindex)

##### Subscripts

- [subscript(Int) -> MLDataTable.Rows.Element](/documentation/createml/mldatatable/rows-swift.struct/subscript(_:))

##### Type Aliases

- [MLDataTable.Rows.Element](/documentation/createml/mldatatable/rows-swift.struct/element)

### Getting information about a data table’s columns

- [var columnNames: MLDataTable.ColumnNames](/documentation/createml/mldatatable/columnnames-swift.property)
- [MLDataTable.ColumnNames](/documentation/createml/mldatatable/columnnames-swift.struct)

#### Accessing columns

- [subscript(_:)](/documentation/createml/mldatatable/subscript(_:))
- [var columnTypes: [String : MLDataValue.ValueType]](/documentation/createml/mldatatable/columntypes)

### Saving a data table

- [func write(to: URL) throws](/documentation/createml/mldatatable/write(to:))
- [func write(toDirectory: String) throws](/documentation/createml/mldatatable/write(todirectory:))
- [func writeCSV(to: URL) throws](/documentation/createml/mldatatable/writecsv(to:))
- [func writeCSV(toFile: String) throws](/documentation/createml/mldatatable/writecsv(tofile:))

### Visualizing a data table

- [func show() -> any MLStreamingVisualizable](/documentation/createml/mldatatable/show())

### Describing a data table

- [var description: String](/documentation/createml/mldatatable/description)
- [var playgroundDescription: Any](/documentation/createml/mldatatable/playgrounddescription)

### Handling data table errors

- [var isValid: Bool](/documentation/createml/mldatatable/isvalid)
- [var error: (any Error)?](/documentation/createml/mldatatable/error)

### Default Implementations

- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mldatatable/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mldatatable/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldatatable/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mldatatable/description)
- [MLDataValue](/documentation/createml/mldatavalue)

### Converting between types and data values

- [MLDataValueConvertible](/documentation/createml/mldatavalueconvertible)

#### Converting from a data value to a type’s instance

- [init()](/documentation/createml/mldatavalueconvertible/init())
- [init?(from: MLDataValue)](/documentation/createml/mldatavalueconvertible/init(from:))

#### Converting from a type’s instance to a data value

- [var dataValue: MLDataValue](/documentation/createml/mldatavalueconvertible/datavalue)
- [static var dataValueType: MLDataValue.ValueType](/documentation/createml/mldatavalueconvertible/datavaluetype)

### Creating a data value

- [case int(Int)](/documentation/createml/mldatavalue/int(_:))
- [case double(Double)](/documentation/createml/mldatavalue/double(_:))
- [case string(String)](/documentation/createml/mldatavalue/string(_:))
- [case dictionary(MLDataValue.DictionaryType)](/documentation/createml/mldatavalue/dictionary(_:))
- [case sequence(MLDataValue.SequenceType)](/documentation/createml/mldatavalue/sequence(_:))
- [case multiArray(MLDataValue.MultiArrayType)](/documentation/createml/mldatavalue/multiarray(_:))

### Inspecting the type

- [var type: MLDataValue.ValueType](/documentation/createml/mldatavalue/type)
- [MLDataValue.ValueType](/documentation/createml/mldatavalue/valuetype)

#### Supported values

- [case int](/documentation/createml/mldatavalue/valuetype/int)
- [case double](/documentation/createml/mldatavalue/valuetype/double)
- [case string](/documentation/createml/mldatavalue/valuetype/string)
- [case dictionary](/documentation/createml/mldatavalue/valuetype/dictionary)
- [case sequence](/documentation/createml/mldatavalue/valuetype/sequence)
- [case multiArray](/documentation/createml/mldatavalue/valuetype/multiarray)
- [case invalid](/documentation/createml/mldatavalue/valuetype/invalid)

#### Describing a data value type

- [var description: String](/documentation/createml/mldatavalue/valuetype/description)
- [var debugDescription: String](/documentation/createml/mldatavalue/valuetype/debugdescription)

#### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldatavalue/valuetype/customdebugstringconvertible-implementations)

##### Instance Properties

- [var debugDescription: String](/documentation/createml/mldatavalue/valuetype/debugdescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldatavalue/valuetype/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/createml/mldatavalue/valuetype/description)

### Accessing numeric values

- [var intValue: Int?](/documentation/createml/mldatavalue/intvalue)
- [var doubleValue: Double?](/documentation/createml/mldatavalue/doublevalue)

### Accessing string values

- [var stringValue: String?](/documentation/createml/mldatavalue/stringvalue)

### Accessing dictionary values

- [var dictionaryValue: MLDataValue.DictionaryType?](/documentation/createml/mldatavalue/dictionaryvalue)
- [MLDataValue.DictionaryType](/documentation/createml/mldatavalue/dictionarytype)

#### Creating a dictionary type

- [init([MLDataValue : MLDataValue])](/documentation/createml/mldatavalue/dictionarytype/init(_:))
- [init<S>(uniqueKeysWithValues: S)](/documentation/createml/mldatavalue/dictionarytype/init(uniquekeyswithvalues:))
- [MLDataValue.DictionaryType.Key](/documentation/createml/mldatavalue/dictionarytype/key)
- [MLDataValue.DictionaryType.Value](/documentation/createml/mldatavalue/dictionarytype/value)

#### Getting an element

- [subscript(MLDataValue.DictionaryType.Key) -> MLDataValue.DictionaryType.Value?](/documentation/createml/mldatavalue/dictionarytype/subscript(_:))

#### Default Implementations

- [MLDataValueConvertible Implementations](/documentation/createml/mldatavalue/dictionarytype/mldatavalueconvertible-implementations)

##### Initializers

- [init?(from: MLDataValue)](/documentation/createml/mldatavalue/dictionarytype/init(from:))

##### Instance Properties

- [var dataValue: MLDataValue](/documentation/createml/mldatavalue/dictionarytype/datavalue)

##### Type Properties

- [static var dataValueType: MLDataValue.ValueType](/documentation/createml/mldatavalue/dictionarytype/datavaluetype)

### Accessing array values

- [var sequenceValue: MLDataValue.SequenceType?](/documentation/createml/mldatavalue/sequencevalue)
- [MLDataValue.SequenceType](/documentation/createml/mldatavalue/sequencetype)

#### Creating a dictionary type

- [init(_:)](/documentation/createml/mldatavalue/sequencetype/init(_:))

#### Default Implementations

- [MLDataValueConvertible Implementations](/documentation/createml/mldatavalue/sequencetype/mldatavalueconvertible-implementations)

##### Initializers

- [init?(from: MLDataValue)](/documentation/createml/mldatavalue/sequencetype/init(from:))

##### Instance Properties

- [var dataValue: MLDataValue](/documentation/createml/mldatavalue/sequencetype/datavalue)

##### Type Properties

- [static var dataValueType: MLDataValue.ValueType](/documentation/createml/mldatavalue/sequencetype/datavaluetype)
- [var multiArrayValue: MLDataValue.MultiArrayType?](/documentation/createml/mldatavalue/multiarrayvalue)
- [MLDataValue.MultiArrayType](/documentation/createml/mldatavalue/multiarraytype)

#### Creating an array type

- [init(MLMultiArray)](/documentation/createml/mldatavalue/multiarraytype/init(_:))
- [init(shape: [Int])](/documentation/createml/mldatavalue/multiarraytype/init(shape:))

#### Getting the array

- [var mlMultiArray: MLMultiArray](/documentation/createml/mldatavalue/multiarraytype/mlmultiarray)

#### Getting an element

- [subscript(_:)](/documentation/createml/mldatavalue/multiarraytype/subscript(_:))

#### Default Implementations

- [MLDataValueConvertible Implementations](/documentation/createml/mldatavalue/multiarraytype/mldatavalueconvertible-implementations)

##### Initializers

- [init?(from: MLDataValue)](/documentation/createml/mldatavalue/multiarraytype/init(from:))

##### Instance Properties

- [var dataValue: MLDataValue](/documentation/createml/mldatavalue/multiarraytype/datavalue)

##### Type Properties

- [static var dataValueType: MLDataValue.ValueType](/documentation/createml/mldatavalue/multiarraytype/datavaluetype)

### Comparing data values

- [static func == (MLDataValue, MLDataValue) -> Bool](/documentation/createml/mldatavalue/==(_:_:))

### Describing a data value

- [var description: String](/documentation/createml/mldatavalue/description)
- [var debugDescription: String](/documentation/createml/mldatavalue/debugdescription)

### Handling errors

- [case invalid](/documentation/createml/mldatavalue/invalid)
- [var isValid: Bool](/documentation/createml/mldatavalue/isvalid)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mldatavalue/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mldatavalue/debugdescription)
- [CustomStringConvertible Implementations](/documentation/createml/mldatavalue/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mldatavalue/description)
- [Equatable Implementations](/documentation/createml/mldatavalue/equatable-implementations)

#### Operators

- [static func == (MLDataValue, MLDataValue) -> Bool](/documentation/createml/mldatavalue/==(_:_:))
- [Data visualizations](/documentation/createml/data-visualizations)

### Table visualizations

- [func show(MLDataTable) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-2dkfz)

### Column visualizations

- [func show<Element>(MLDataColumn<Element>) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-5r938)
- [func show(MLUntypedColumn) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-9645r)

### Plot visualizations

- [func show<ElementX, ElementY>(MLDataColumn<ElementX>, MLDataColumn<ElementY>) -> any MLStreamingVisualizable](/documentation/createml/show(_:_:)-537qb)
- [func show(MLUntypedColumn, MLUntypedColumn) -> any MLStreamingVisualizable](/documentation/createml/show(_:_:)-2tmbf)

### Visualization protocols

- [MLVisualizable](/documentation/createml/mlvisualizable)

#### Seeing the visualization

- [var cgImage: CGImage?](/documentation/createml/mlvisualizable/cgimage)
- [MLStreamingVisualizable](/documentation/createml/mlstreamingvisualizable)

#### Seeing the next visualization

- [var hasFinishedStreaming: Bool](/documentation/createml/mlstreamingvisualizable/hasfinishedstreaming)
- [func nextIteration()](/documentation/createml/mlstreamingvisualizable/nextiteration())

## Model accuracy

- [Improving Your Model’s Accuracy](/documentation/createml/improving-your-model-s-accuracy)
- [MLClassifierMetrics](/documentation/createml/mlclassifiermetrics)

### Understanding the model

- [var classificationError: Double](/documentation/createml/mlclassifiermetrics/classificationerror)
- [var precisionRecall: MLDataTable](/documentation/createml/mlclassifiermetrics/precisionrecall)
- [var confusion: MLDataTable](/documentation/createml/mlclassifiermetrics/confusion)
- [var confusionDataFrame: DataFrame](/documentation/createml/mlclassifiermetrics/confusiondataframe)
- [var precisionRecallDataFrame: DataFrame](/documentation/createml/mlclassifiermetrics/precisionrecalldataframe)

### Handling errors

- [var isValid: Bool](/documentation/createml/mlclassifiermetrics/isvalid)
- [var error: (any Error)?](/documentation/createml/mlclassifiermetrics/error)

### Creating metrics

- [init(classificationError: Double, confusion: MLDataTable, precisionRecall: MLDataTable)](/documentation/createml/mlclassifiermetrics/init(classificationerror:confusion:precisionrecall:))

### Describing metrics

- [var description: String](/documentation/createml/mlclassifiermetrics/description)
- [var debugDescription: String](/documentation/createml/mlclassifiermetrics/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlclassifiermetrics/playgrounddescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlclassifiermetrics/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlclassifiermetrics/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlclassifiermetrics/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlclassifiermetrics/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlclassifiermetrics/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlclassifiermetrics/description)
- [MLRegressorMetrics](/documentation/createml/mlregressormetrics)

### Understanding the model

- [var maximumError: Double](/documentation/createml/mlregressormetrics/maximumerror)
- [var rootMeanSquaredError: Double](/documentation/createml/mlregressormetrics/rootmeansquarederror)

### Handling errors

- [var isValid: Bool](/documentation/createml/mlregressormetrics/isvalid)
- [var error: (any Error)?](/documentation/createml/mlregressormetrics/error)

### Creating metrics

- [init(maximumError: Double, rootMeanSquaredError: Double)](/documentation/createml/mlregressormetrics/init(maximumerror:rootmeansquarederror:))

### Describing metrics

- [var description: String](/documentation/createml/mlregressormetrics/description)
- [var debugDescription: String](/documentation/createml/mlregressormetrics/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlregressormetrics/playgrounddescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlregressormetrics/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlregressormetrics/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlregressormetrics/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlregressormetrics/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlregressormetrics/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlregressormetrics/description)
- [MLWordTaggerMetrics](/documentation/createml/mlwordtaggermetrics)

### Analyzing the tagger’s performance

- [var taggingError: Double](/documentation/createml/mlwordtaggermetrics/taggingerror)
- [var precisionRecall: MLDataTable](/documentation/createml/mlwordtaggermetrics/precisionrecall)
- [var confusion: MLDataTable](/documentation/createml/mlwordtaggermetrics/confusion)

### Handling errors

- [var isValid: Bool](/documentation/createml/mlwordtaggermetrics/isvalid)
- [var error: (any Error)?](/documentation/createml/mlwordtaggermetrics/error)

### Describing metrics

- [var description: String](/documentation/createml/mlwordtaggermetrics/description)
- [var debugDescription: String](/documentation/createml/mlwordtaggermetrics/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlwordtaggermetrics/playgrounddescription)
- [var confusionDataFrame: DataFrame](/documentation/createml/mlwordtaggermetrics/confusiondataframe)
- [var precisionRecallDataFrame: DataFrame](/documentation/createml/mlwordtaggermetrics/precisionrecalldataframe)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlwordtaggermetrics/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlwordtaggermetrics/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlwordtaggermetrics/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlwordtaggermetrics/description)
- [MLRecommenderMetrics](/documentation/createml/mlrecommendermetrics)

### Assessing the model

- [let excludingObserved: Bool](/documentation/createml/mlrecommendermetrics/excludingobserved)
- [var precisionRecall: MLDataTable](/documentation/createml/mlrecommendermetrics/precisionrecall)
- [var precisionRecallDataFrame: DataFrame](/documentation/createml/mlrecommendermetrics/precisionrecalldataframe)

### Handling errors

- [var isValid: Bool](/documentation/createml/mlrecommendermetrics/isvalid)
- [let error: (any Error)?](/documentation/createml/mlrecommendermetrics/error)

### Creating metrics

- [init(precisionRecall: MLDataTable, excludingObserved: Bool)](/documentation/createml/mlrecommendermetrics/init(precisionrecall:excludingobserved:))
- [MLObjectDetectorMetrics](/documentation/createml/mlobjectdetectormetrics)

### Creating metrics

- [init(averagePrecision: (variedIoU: [String : Double], IoU50: [String : Double]), meanAveragePrecision: (variedIoU: Double, IoU50: Double))](/documentation/createml/mlobjectdetectormetrics/init(averageprecision:meanaverageprecision:))

### Assessing the model

- [var averagePrecision: (variedIoU: [String : Double], IoU50: [String : Double])](/documentation/createml/mlobjectdetectormetrics/averageprecision)
- [var meanAveragePrecision: (variedIoU: Double, IoU50: Double)](/documentation/createml/mlobjectdetectormetrics/meanaverageprecision)

### Handling errors

- [var isValid: Bool](/documentation/createml/mlobjectdetectormetrics/isvalid)
- [var error: (any Error)?](/documentation/createml/mlobjectdetectormetrics/error)

### Describing metrics

- [var description: String](/documentation/createml/mlobjectdetectormetrics/description)
- [var debugDescription: String](/documentation/createml/mlobjectdetectormetrics/debugdescription)
- [var playgroundDescription: Any](/documentation/createml/mlobjectdetectormetrics/playgrounddescription)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlobjectdetectormetrics/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlobjectdetectormetrics/debugdescription)
- [CustomPlaygroundDisplayConvertible Implementations](/documentation/createml/mlobjectdetectormetrics/customplaygrounddisplayconvertible-implementations)

#### Instance Properties

- [var playgroundDescription: Any](/documentation/createml/mlobjectdetectormetrics/playgrounddescription)
- [CustomStringConvertible Implementations](/documentation/createml/mlobjectdetectormetrics/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlobjectdetectormetrics/description)

## Model training Control

- [MLJob](/documentation/createml/mljob)

### Receiving progress updates

- [var checkpoints: AnyPublisher<MLCheckpoint, Never>](/documentation/createml/mljob/checkpoints)
- [var result: AnyPublisher<Result, any Error>](/documentation/createml/mljob/result)
- [var phase: AnyPublisher<MLPhase, Never>](/documentation/createml/mljob/phase)

### Managing a job

- [func cancel()](/documentation/createml/mljob/cancel())
- [var isCanceled: Bool](/documentation/createml/mljob/iscanceled)

### Inspecting a job

- [let startDate: Date](/documentation/createml/mljob/startdate)
- [let progress: Progress](/documentation/createml/mljob/progress)
- [MLProgress](/documentation/createml/mlprogress)

#### Creating a training progress update

- [init(phase: MLPhase)](/documentation/createml/mlprogress/init(phase:))
- [init?(progress: Progress)](/documentation/createml/mlprogress/init(progress:))

#### Inspecting a session’s progress

- [var elapsedTime: TimeInterval](/documentation/createml/mlprogress/elapsedtime)
- [var phase: MLPhase](/documentation/createml/mlprogress/phase)
- [var itemCount: Int](/documentation/createml/mlprogress/itemcount)
- [var totalItemCount: Int?](/documentation/createml/mlprogress/totalitemcount)
- [var metrics: [MLProgress.Metric : Any]](/documentation/createml/mlprogress/metrics)
- [MLProgress.Metric](/documentation/createml/mlprogress/metric)

##### Retrieving metric keys

- [case accuracy](/documentation/createml/mlprogress/metric/accuracy)
- [case contentLoss](/documentation/createml/mlprogress/metric/contentloss)
- [case loss](/documentation/createml/mlprogress/metric/loss)
- [case maximumError](/documentation/createml/mlprogress/metric/maximumerror)
- [case rootMeanSquaredError](/documentation/createml/mlprogress/metric/rootmeansquarederror)
- [case styleLoss](/documentation/createml/mlprogress/metric/styleloss)
- [case stylizedImageURL](/documentation/createml/mlprogress/metric/stylizedimageurl)
- [case validationAccuracy](/documentation/createml/mlprogress/metric/validationaccuracy)
- [case validationLoss](/documentation/createml/mlprogress/metric/validationloss)
- [case validationMaximumError](/documentation/createml/mlprogress/metric/validationmaximumerror)
- [case validationRootMeanSquaredError](/documentation/createml/mlprogress/metric/validationrootmeansquarederror)

#### Accessing general information

- [static let elapsedTimeKey: ProgressUserInfoKey](/documentation/createml/mlprogress/elapsedtimekey)
- [static let phaseKey: ProgressUserInfoKey](/documentation/createml/mlprogress/phasekey)
- [static let itemCountKey: ProgressUserInfoKey](/documentation/createml/mlprogress/itemcountkey)
- [static let totalItemCountKey: ProgressUserInfoKey](/documentation/createml/mlprogress/totalitemcountkey)

#### Accessing assessment metrics

- [static let accuracyKey: ProgressUserInfoKey](/documentation/createml/mlprogress/accuracykey)
- [static let lossKey: ProgressUserInfoKey](/documentation/createml/mlprogress/losskey)
- [static let validationAccuracyKey: ProgressUserInfoKey](/documentation/createml/mlprogress/validationaccuracykey)
- [static let validationLossKey: ProgressUserInfoKey](/documentation/createml/mlprogress/validationlosskey)

#### Accessing style transfer metrics

- [static let contentLossKey: ProgressUserInfoKey](/documentation/createml/mlprogress/contentlosskey)
- [static let styleLossKey: ProgressUserInfoKey](/documentation/createml/mlprogress/stylelosskey)
- [static let stylizedImageKey: ProgressUserInfoKey](/documentation/createml/mlprogress/stylizedimagekey)

#### Accessing error information

- [static let maximumErrorKey: ProgressUserInfoKey](/documentation/createml/mlprogress/maximumerrorkey)
- [static let rootMeanSquaredErrorKey: ProgressUserInfoKey](/documentation/createml/mlprogress/rootmeansquarederrorkey)
- [static let validationMaximumErrorKey: ProgressUserInfoKey](/documentation/createml/mlprogress/validationmaximumerrorkey)
- [static let validationRootMeanSquaredErrorKey: ProgressUserInfoKey](/documentation/createml/mlprogress/validationrootmeansquarederrorkey)

#### Encoding and decoding a session’s progress

- [func encode(to: any Encoder) throws](/documentation/createml/mlprogress/encode(to:))
- [init(from: any Decoder) throws](/documentation/createml/mlprogress/init(from:))
- [MLTrainingSession](/documentation/createml/mltrainingsession)

### Checking a training session’s progress

- [var phase: MLPhase](/documentation/createml/mltrainingsession/phase)
- [MLPhase](/documentation/createml/mlphase)

#### Retrieving session phases

- [case initialized](/documentation/createml/mlphase/initialized)
- [case extractingFeatures](/documentation/createml/mlphase/extractingfeatures)
- [case training](/documentation/createml/mlphase/training)
- [case evaluating](/documentation/createml/mlphase/evaluating)
- [case inferencing](/documentation/createml/mlphase/inferencing)
- [var iteration: Int](/documentation/createml/mltrainingsession/iteration)
- [var checkpoints: [MLCheckpoint]](/documentation/createml/mltrainingsession/checkpoints)

### Removing checkpoints

- [func removeCheckpoints((MLCheckpoint) -> Bool) throws](/documentation/createml/mltrainingsession/removecheckpoints(_:))

### Reusing features from a previous session

- [func reuseExtractedFeatures(from: MLTrainingSession<Task>) throws](/documentation/createml/mltrainingsession/reuseextractedfeatures(from:))

### Inspecting a session

- [var date: Date](/documentation/createml/mltrainingsession/date)
- [let parameters: MLTrainingSessionParameters](/documentation/createml/mltrainingsession/parameters)
- [MLTrainingSessionParameters](/documentation/createml/mltrainingsessionparameters)

### Creating a session’s parameters

- [init(sessionDirectory: URL?, reportInterval: Int, checkpointInterval: Int, iterations: Int)](/documentation/createml/mltrainingsessionparameters/init(sessiondirectory:reportinterval:checkpointinterval:iterations:))

### Configuring the session’s parameters

- [let sessionDirectory: URL?](/documentation/createml/mltrainingsessionparameters/sessiondirectory)
- [var reportInterval: Int](/documentation/createml/mltrainingsessionparameters/reportinterval)
- [var checkpointInterval: Int](/documentation/createml/mltrainingsessionparameters/checkpointinterval)
- [var iterations: Int](/documentation/createml/mltrainingsessionparameters/iterations)
- [MLCheckpoint](/documentation/createml/mlcheckpoint)

### Inspecting a checkpoint

- [var phase: MLPhase](/documentation/createml/mlcheckpoint/phase)
- [var iteration: Int](/documentation/createml/mlcheckpoint/iteration)
- [var date: Date](/documentation/createml/mlcheckpoint/date)
- [var url: URL](/documentation/createml/mlcheckpoint/url)

### Assessing a checkpoint

- [var metrics: [MLProgress.Metric : Any]](/documentation/createml/mlcheckpoint/metrics)
- [MLProgress.Metric](/documentation/createml/mlprogress/metric)

#### Retrieving metric keys

- [case accuracy](/documentation/createml/mlprogress/metric/accuracy)
- [case contentLoss](/documentation/createml/mlprogress/metric/contentloss)
- [case loss](/documentation/createml/mlprogress/metric/loss)
- [case maximumError](/documentation/createml/mlprogress/metric/maximumerror)
- [case rootMeanSquaredError](/documentation/createml/mlprogress/metric/rootmeansquarederror)
- [case styleLoss](/documentation/createml/mlprogress/metric/styleloss)
- [case stylizedImageURL](/documentation/createml/mlprogress/metric/stylizedimageurl)
- [case validationAccuracy](/documentation/createml/mlprogress/metric/validationaccuracy)
- [case validationLoss](/documentation/createml/mlprogress/metric/validationloss)
- [case validationMaximumError](/documentation/createml/mlprogress/metric/validationmaximumerror)
- [case validationRootMeanSquaredError](/documentation/createml/mlprogress/metric/validationrootmeansquarederror)

### Encoding and decoding a checkpoint

- [func encode(to: any Encoder) throws](/documentation/createml/mlcheckpoint/encode(to:))
- [init(from: any Decoder) throws](/documentation/createml/mlcheckpoint/init(from:))

## Supporting types

- [MLCreateError](/documentation/createml/mlcreateerror)

### Identifying errors

- [case cancelled](/documentation/createml/mlcreateerror/cancelled)
- [case incompatibleParameters(parameter: String, originalValue: String, newValue: String)](/documentation/createml/mlcreateerror/incompatibleparameters(parameter:originalvalue:newvalue:))
- [case modifiedTrainingData](/documentation/createml/mlcreateerror/modifiedtrainingdata)
- [case io(reason: String)](/documentation/createml/mlcreateerror/io(reason:))
- [case type(reason: String)](/documentation/createml/mlcreateerror/type(reason:))
- [case generic(reason: String)](/documentation/createml/mlcreateerror/generic(reason:))
- [let MLCreateErrorDomain: String](/documentation/createml/mlcreateerrordomain)

### Describing errors

- [var description: String](/documentation/createml/mlcreateerror/description)
- [var debugDescription: String](/documentation/createml/mlcreateerror/debugdescription)

### Describing errors in a user interface

- [var errorCode: Int](/documentation/createml/mlcreateerror/errorcode)
- [var errorUserInfo: [String : Any]](/documentation/createml/mlcreateerror/erroruserinfo)
- [var errorDescription: String?](/documentation/createml/mlcreateerror/errordescription)
- [var failureReason: String?](/documentation/createml/mlcreateerror/failurereason)

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/createml/mlcreateerror/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/createml/mlcreateerror/debugdescription)
- [CustomNSError Implementations](/documentation/createml/mlcreateerror/customnserror-implementations)

#### Instance Properties

- [var errorCode: Int](/documentation/createml/mlcreateerror/errorcode)
- [var errorUserInfo: [String : Any]](/documentation/createml/mlcreateerror/erroruserinfo)
- [CustomStringConvertible Implementations](/documentation/createml/mlcreateerror/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/createml/mlcreateerror/description)
- [LocalizedError Implementations](/documentation/createml/mlcreateerror/localizederror-implementations)

#### Instance Properties

- [var errorDescription: String?](/documentation/createml/mlcreateerror/errordescription)
- [var failureReason: String?](/documentation/createml/mlcreateerror/failurereason)
- [MLModelMetadata](/documentation/createml/mlmodelmetadata)

### Creating metadata

- [init(author: String, shortDescription: String, license: String?, version: String, additional: [String : String]?)](/documentation/createml/mlmodelmetadata/init(author:shortdescription:license:version:additional:))

### Accessing metadata

- [var author: String](/documentation/createml/mlmodelmetadata/author)
- [var shortDescription: String](/documentation/createml/mlmodelmetadata/shortdescription)
- [var license: String?](/documentation/createml/mlmodelmetadata/license)
- [var version: String](/documentation/createml/mlmodelmetadata/version)
- [var additional: [String : String]?](/documentation/createml/mlmodelmetadata/additional)
- [MLSplitStrategy](/documentation/createml/mlsplitstrategy)

### Partitioning data

- [case automatic](/documentation/createml/mlsplitstrategy/automatic)
- [case fixed(ratio: Double, seed: Int?)](/documentation/createml/mlsplitstrategy/fixed(ratio:seed:))
- [func resolve(count: Int) -> (ratio: Double, seed: Int)](/documentation/createml/mlsplitstrategy/resolve(count:))

### Creating a random seed

- [func timestampSeed() -> Int](/documentation/createml/timestampseed())

## Articles

- [Data visualizations](/documentation/createml/create-ml-utilties)

### Table visualizations

- [func show(MLDataTable) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-2dkfz)

### Column visualizations

- [func show<Element>(MLDataColumn<Element>) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-5r938)
- [func show(MLUntypedColumn) -> any MLStreamingVisualizable](/documentation/createml/show(_:)-9645r)

### Plot visualizations

- [func show<ElementX, ElementY>(MLDataColumn<ElementX>, MLDataColumn<ElementY>) -> any MLStreamingVisualizable](/documentation/createml/show(_:_:)-537qb)
- [func show(MLUntypedColumn, MLUntypedColumn) -> any MLStreamingVisualizable](/documentation/createml/show(_:_:)-2tmbf)

### Visualization protocols

- [MLVisualizable](/documentation/createml/mlvisualizable)

#### Seeing the visualization

- [var cgImage: CGImage?](/documentation/createml/mlvisualizable/cgimage)
- [MLStreamingVisualizable](/documentation/createml/mlstreamingvisualizable)

#### Seeing the next visualization

- [var hasFinishedStreaming: Bool](/documentation/createml/mlstreamingvisualizable/hasfinishedstreaming)
- [func nextIteration()](/documentation/createml/mlstreamingvisualizable/nextiteration())
- [Detecting human actions in a live video feed](/documentation/createml/detecting-human-actions-in-a-live-video-feed)
- [Gathering Training Videos for an Action Classifier](/documentation/createml/recording-or-choosing-training-videos)

## Functions

- [func show(_:)](/documentation/createml/show(_:))
- [func show(_:_:)](/documentation/createml/show(_:_:))

## Enumerations

- [MLBoundingBoxAnchor](/documentation/createml/mlboundingboxanchor)

### Designating anchors

- [case center](/documentation/createml/mlboundingboxanchor/center)
- [case topLeft](/documentation/createml/mlboundingboxanchor/topleft)
- [case bottomLeft](/documentation/createml/mlboundingboxanchor/bottomleft)
- [MLBoundingBoxCoordinatesOrigin](/documentation/createml/mlboundingboxcoordinatesorigin)

### Designating origins

- [case topLeft](/documentation/createml/mlboundingboxcoordinatesorigin/topleft)
- [case bottomLeft](/documentation/createml/mlboundingboxcoordinatesorigin/bottomleft)
- [MLBoundingBoxUnits](/documentation/createml/mlboundingboxunits)

### Designating units

- [case pixel](/documentation/createml/mlboundingboxunits/pixel)
- [case normalized](/documentation/createml/mlboundingboxunits/normalized)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
