# Vision Documentation

Source: https://sosumi.ai/documentation/vision

---
title: Vision
source: https://developer.apple.com/documentation/vision
timestamp: 2026-02-13T19:24:40.697Z
---

## Text and document analysis

- [Locating and displaying recognized text](/documentation/vision/locating-and-displaying-recognized-text)
- [Recognizing tables within a document](/documentation/vision/recognize-tables-within-a-document)
- [DetectBarcodesRequest](/documentation/vision/detectbarcodesrequest)

### Creating a request

- [init(DetectBarcodesRequest.Revision?)](/documentation/vision/detectbarcodesrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [BarcodeObservation](/documentation/vision/barcodeobservation)

#### Creating an observation

- [init(VNBarcodeObservation)](/documentation/vision/barcodeobservation/init(_:))

#### Getting the bounding region

- [var boundingRegion: NormalizedRegion](/documentation/vision/barcodeobservation/boundingregion)

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let isColorInverted: Bool](/documentation/vision/barcodeobservation/iscolorinverted)
- [let isGS1DataCarrier: Bool](/documentation/vision/barcodeobservation/isgs1datacarrier)

#### Getting the payload

- [let payloadData: Data?](/documentation/vision/barcodeobservation/payloaddata)
- [let payloadString: String?](/documentation/vision/barcodeobservation/payloadstring)
- [let supplementalPayloadData: Data?](/documentation/vision/barcodeobservation/supplementalpayloaddata)
- [let supplementalPayloadString: String?](/documentation/vision/barcodeobservation/supplementalpayloadstring)

#### Getting the symbology

- [let symbology: BarcodeSymbology](/documentation/vision/barcodeobservation/symbology)
- [BarcodeSymbology](/documentation/vision/barcodesymbology)

##### Getting the symbologies

- [case aztec](/documentation/vision/barcodesymbology/aztec)
- [case codabar](/documentation/vision/barcodesymbology/codabar)
- [case code128](/documentation/vision/barcodesymbology/code128)
- [case code39](/documentation/vision/barcodesymbology/code39)
- [case code39Checksum](/documentation/vision/barcodesymbology/code39checksum)
- [case code39FullASCII](/documentation/vision/barcodesymbology/code39fullascii)
- [case code39FullASCIIChecksum](/documentation/vision/barcodesymbology/code39fullasciichecksum)
- [case code93](/documentation/vision/barcodesymbology/code93)
- [case code93i](/documentation/vision/barcodesymbology/code93i)
- [case dataMatrix](/documentation/vision/barcodesymbology/datamatrix)
- [case ean13](/documentation/vision/barcodesymbology/ean13)
- [case ean8](/documentation/vision/barcodesymbology/ean8)
- [case gs1DataBar](/documentation/vision/barcodesymbology/gs1databar)
- [case gs1DataBarExpanded](/documentation/vision/barcodesymbology/gs1databarexpanded)
- [case gs1DataBarLimited](/documentation/vision/barcodesymbology/gs1databarlimited)
- [case i2of5](/documentation/vision/barcodesymbology/i2of5)
- [case i2of5Checksum](/documentation/vision/barcodesymbology/i2of5checksum)
- [case itf14](/documentation/vision/barcodesymbology/itf14)
- [case microPDF417](/documentation/vision/barcodesymbology/micropdf417)
- [case microQR](/documentation/vision/barcodesymbology/microqr)
- [case msiPlessey](/documentation/vision/barcodesymbology/msiplessey)
- [case pdf417](/documentation/vision/barcodesymbology/pdf417)
- [case qr](/documentation/vision/barcodesymbology/qr)
- [case upce](/documentation/vision/barcodesymbology/upce)

#### Getting the composite type

- [let supplementalCompositeType: BarcodeObservation.CompositeType?](/documentation/vision/barcodeobservation/supplementalcompositetype)
- [BarcodeObservation.CompositeType](/documentation/vision/barcodeobservation/compositetype)

##### Getting the composite types

- [case gs1TypeA](/documentation/vision/barcodeobservation/compositetype/gs1typea)
- [case gs1TypeB](/documentation/vision/barcodeobservation/compositetype/gs1typeb)
- [case gs1TypeC](/documentation/vision/barcodeobservation/compositetype/gs1typec)
- [case linked](/documentation/vision/barcodeobservation/compositetype/linked)

### Configuring a request

- [var symbologies: [BarcodeSymbology]](/documentation/vision/detectbarcodesrequest/symbologies)
- [var supportedSymbologies: [BarcodeSymbology]](/documentation/vision/detectbarcodesrequest/supportedsymbologies)
- [BarcodeSymbology](/documentation/vision/barcodesymbology)

#### Getting the symbologies

- [case aztec](/documentation/vision/barcodesymbology/aztec)
- [case codabar](/documentation/vision/barcodesymbology/codabar)
- [case code128](/documentation/vision/barcodesymbology/code128)
- [case code39](/documentation/vision/barcodesymbology/code39)
- [case code39Checksum](/documentation/vision/barcodesymbology/code39checksum)
- [case code39FullASCII](/documentation/vision/barcodesymbology/code39fullascii)
- [case code39FullASCIIChecksum](/documentation/vision/barcodesymbology/code39fullasciichecksum)
- [case code93](/documentation/vision/barcodesymbology/code93)
- [case code93i](/documentation/vision/barcodesymbology/code93i)
- [case dataMatrix](/documentation/vision/barcodesymbology/datamatrix)
- [case ean13](/documentation/vision/barcodesymbology/ean13)
- [case ean8](/documentation/vision/barcodesymbology/ean8)
- [case gs1DataBar](/documentation/vision/barcodesymbology/gs1databar)
- [case gs1DataBarExpanded](/documentation/vision/barcodesymbology/gs1databarexpanded)
- [case gs1DataBarLimited](/documentation/vision/barcodesymbology/gs1databarlimited)
- [case i2of5](/documentation/vision/barcodesymbology/i2of5)
- [case i2of5Checksum](/documentation/vision/barcodesymbology/i2of5checksum)
- [case itf14](/documentation/vision/barcodesymbology/itf14)
- [case microPDF417](/documentation/vision/barcodesymbology/micropdf417)
- [case microQR](/documentation/vision/barcodesymbology/microqr)
- [case msiPlessey](/documentation/vision/barcodesymbology/msiplessey)
- [case pdf417](/documentation/vision/barcodesymbology/pdf417)
- [case qr](/documentation/vision/barcodesymbology/qr)
- [case upce](/documentation/vision/barcodesymbology/upce)
- [var coalescesCompositeSymbologies: Bool](/documentation/vision/detectbarcodesrequest/coalescescompositesymbologies)

### Getting the revision

- [let revision: DetectBarcodesRequest.Revision](/documentation/vision/detectbarcodesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectBarcodesRequest.Revision]](/documentation/vision/detectbarcodesrequest/supportedrevisions)
- [DetectBarcodesRequest.Revision](/documentation/vision/detectbarcodesrequest/revision-swift.enum)

#### Getting the revision

- [case revision4](/documentation/vision/detectbarcodesrequest/revision-swift.enum/revision4)
- [DetectDocumentSegmentationRequest](/documentation/vision/detectdocumentsegmentationrequest)

### Creating a request

- [init(DetectDocumentSegmentationRequest.Revision?)](/documentation/vision/detectdocumentsegmentationrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [DetectedDocumentObservation](/documentation/vision/detecteddocumentobservation)

#### Creating an observation

- [init?(VNRectangleObservation)](/documentation/vision/detecteddocumentobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var globalSegmentationMask: PixelBufferObservation](/documentation/vision/detecteddocumentobservation/globalsegmentationmask)
- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

##### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

##### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

##### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))

### Getting the revision

- [let revision: DetectDocumentSegmentationRequest.Revision](/documentation/vision/detectdocumentsegmentationrequest/revision-swift.property)
- [static let supportedRevisions: [DetectDocumentSegmentationRequest.Revision]](/documentation/vision/detectdocumentsegmentationrequest/supportedrevisions)
- [DetectDocumentSegmentationRequest.Revision](/documentation/vision/detectdocumentsegmentationrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detectdocumentsegmentationrequest/revision-swift.enum/revision1)
- [DetectTextRectanglesRequest](/documentation/vision/detecttextrectanglesrequest)

### Creating a request

- [init(DetectTextRectanglesRequest.Revision?)](/documentation/vision/detecttextrectanglesrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [TextObservation](/documentation/vision/textobservation)

#### Creating an observation

- [init(VNTextObservation)](/documentation/vision/textobservation/init(_:))

#### Inspecting an observation

- [let characterBoxes: [RectangleObservation]?](/documentation/vision/textobservation/characterboxes)
- [RectangleObservation](/documentation/vision/rectangleobservation)

##### Creating an observation

- [init(VNRectangleObservation)](/documentation/vision/rectangleobservation/init(_:))
- [init(topLeft: NormalizedPoint, topRight: NormalizedPoint, bottomRight: NormalizedPoint, bottomLeft: NormalizedPoint)](/documentation/vision/rectangleobservation/init(topleft:topright:bottomright:bottomleft:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Configuring a request

- [var reportCharacterBoxes: Bool](/documentation/vision/detecttextrectanglesrequest/reportcharacterboxes)

### Getting the revision

- [let revision: DetectTextRectanglesRequest.Revision](/documentation/vision/detecttextrectanglesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectTextRectanglesRequest.Revision]](/documentation/vision/detecttextrectanglesrequest/supportedrevisions)
- [DetectTextRectanglesRequest.Revision](/documentation/vision/detecttextrectanglesrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detecttextrectanglesrequest/revision-swift.enum/revision1)
- [RecognizeDocumentsRequest](/documentation/vision/recognizedocumentsrequest)

### Creating a request

- [init(RecognizeDocumentsRequest.Revision?)](/documentation/vision/recognizedocumentsrequest/init(_:))

### Understanding the result

- [DocumentObservation](/documentation/vision/documentobservation)

#### Inspecting an observation

- [let uuid: UUID](/documentation/vision/documentobservation/uuid)
- [let confidence: Float](/documentation/vision/documentobservation/confidence)
- [let document: DocumentObservation.Container](/documentation/vision/documentobservation/document)
- [let timeRange: CMTimeRange?](/documentation/vision/documentobservation/timerange)

#### Getting the recognized text

- [DocumentObservation.Container](/documentation/vision/documentobservation/container)

##### Getting the sections in a document

- [DocumentObservation.Container.List](/documentation/vision/documentobservation/container/list)

###### Accessing a list

- [DocumentObservation.Container.List.Item](/documentation/vision/documentobservation/container/list/item)

###### Inspecting an item

- [var content: DocumentObservation.Container](/documentation/vision/documentobservation/container/list/item/content)
- [var itemString: String](/documentation/vision/documentobservation/container/list/item/itemstring)
- [var markerString: String](/documentation/vision/documentobservation/container/list/item/markerstring)
- [var markerType: DocumentObservation.Container.List.Marker?](/documentation/vision/documentobservation/container/list/item/markertype)

###### Inspecting a list

- [var boundingRegion: NormalizedRegion](/documentation/vision/documentobservation/container/list/boundingregion)
- [var items: [DocumentObservation.Container.List.Item]](/documentation/vision/documentobservation/container/list/items)
- [DocumentObservation.Container.List.Marker](/documentation/vision/documentobservation/container/list/marker)

###### Getting the list marker types

- [case bullet](/documentation/vision/documentobservation/container/list/marker/bullet)
- [case compositeDecimal](/documentation/vision/documentobservation/container/list/marker/compositedecimal)
- [case decimal](/documentation/vision/documentobservation/container/list/marker/decimal)
- [case decorativeDecimal](/documentation/vision/documentobservation/container/list/marker/decorativedecimal)
- [case hyphen](/documentation/vision/documentobservation/container/list/marker/hyphen)
- [case lowercaseLatin](/documentation/vision/documentobservation/container/list/marker/lowercaselatin)
- [case uppercaseLatin](/documentation/vision/documentobservation/container/list/marker/uppercaselatin)
- [DocumentObservation.Container.Table](/documentation/vision/documentobservation/container/table)

###### Accessing a table

- [DocumentObservation.Container.Table.Cell](/documentation/vision/documentobservation/container/table/cell)

###### Inspecting a cell

- [var columnRange: ClosedRange<Int>](/documentation/vision/documentobservation/container/table/cell/columnrange)
- [var content: DocumentObservation.Container](/documentation/vision/documentobservation/container/table/cell/content)
- [var rowRange: ClosedRange<Int>](/documentation/vision/documentobservation/container/table/cell/rowrange)

###### Inspecting a table

- [var boundingRegion: NormalizedRegion](/documentation/vision/documentobservation/container/table/boundingregion)
- [var columns: [[DocumentObservation.Container.Table.Cell]]](/documentation/vision/documentobservation/container/table/columns)
- [var rows: [[DocumentObservation.Container.Table.Cell]]](/documentation/vision/documentobservation/container/table/rows)

###### Getting the cell

- [func cell(row: Int, col: Int) -> DocumentObservation.Container.Table.Cell?](/documentation/vision/documentobservation/container/table/cell(row:col:))
- [DocumentObservation.Container.Text](/documentation/vision/documentobservation/container/text-swift.struct)

###### Accessing the text

- [var detectedData: [DocumentObservation.Container.DataDetectorMatch]](/documentation/vision/documentobservation/container/text-swift.struct/detecteddata)
- [var lines: [RecognizedTextObservation]](/documentation/vision/documentobservation/container/text-swift.struct/lines)
- [var transcript: String](/documentation/vision/documentobservation/container/text-swift.struct/transcript)
- [var words: [RecognizedTextObservation]?](/documentation/vision/documentobservation/container/text-swift.struct/words)

###### Inspecting the text

- [var boundingRegion: NormalizedRegion](/documentation/vision/documentobservation/container/text-swift.struct/boundingregion)
- [var textAlignment: DocumentObservation.Container.Text.Alignment?](/documentation/vision/documentobservation/container/text-swift.struct/textalignment)
- [DocumentObservation.Container.Text.Alignment](/documentation/vision/documentobservation/container/text-swift.struct/alignment)

###### Getting the alignment

- [case center](/documentation/vision/documentobservation/container/text-swift.struct/alignment/center)
- [case leading](/documentation/vision/documentobservation/container/text-swift.struct/alignment/leading)
- [case trailing](/documentation/vision/documentobservation/container/text-swift.struct/alignment/trailing)

###### Getting the bounding region

- [func boundingRegion(for: Range<String.Index>) -> NormalizedRegion?](/documentation/vision/documentobservation/container/text-swift.struct/boundingregion(for:))

##### Accessing specific content within a document

- [DocumentObservation.Container.DataDetectorMatch](/documentation/vision/documentobservation/container/datadetectormatch)

###### Getting the detected data

- [var match: DataDetector.Match](/documentation/vision/documentobservation/container/datadetectormatch/match)
- [var barcodes: [BarcodeObservation]](/documentation/vision/documentobservation/container/barcodes)
- [var lists: [DocumentObservation.Container.List]](/documentation/vision/documentobservation/container/lists)
- [var paragraphs: [DocumentObservation.Container.Text]](/documentation/vision/documentobservation/container/paragraphs)
- [var tables: [DocumentObservation.Container.Table]](/documentation/vision/documentobservation/container/tables)
- [var text: DocumentObservation.Container.Text](/documentation/vision/documentobservation/container/text-swift.property)
- [var title: DocumentObservation.Container.Text?](/documentation/vision/documentobservation/container/title)

### Configuring a request

- [RecognizeDocumentsRequest.BarcodeDetectionOptions](/documentation/vision/recognizedocumentsrequest/barcodedetectionoptions-swift.struct)

#### Getting the symbology

- [var coalesceCompositeSymbologies: Bool](/documentation/vision/recognizedocumentsrequest/barcodedetectionoptions-swift.struct/coalescecompositesymbologies)
- [var enabled: Bool](/documentation/vision/recognizedocumentsrequest/barcodedetectionoptions-swift.struct/enabled)
- [var symbologies: [BarcodeSymbology]](/documentation/vision/recognizedocumentsrequest/barcodedetectionoptions-swift.struct/symbologies)
- [RecognizeDocumentsRequest.TextRecognitionOptions](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct)

#### Inspecting the recognized text

- [var automaticallyDetectLanguage: Bool](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/automaticallydetectlanguage)
- [var customWords: [String]](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/customwords)
- [var maximumCandidateCount: Int](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/maximumcandidatecount)
- [var minimumTextHeightFraction: Float](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/minimumtextheightfraction)
- [var recognitionLanguages: [Locale.Language]](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/recognitionlanguages)
- [var useLanguageCorrection: Bool](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.struct/uselanguagecorrection)
- [var barcodeDetectionOptions: RecognizeDocumentsRequest.BarcodeDetectionOptions](/documentation/vision/recognizedocumentsrequest/barcodedetectionoptions-swift.property)
- [var textRecognitionOptions: RecognizeDocumentsRequest.TextRecognitionOptions](/documentation/vision/recognizedocumentsrequest/textrecognitionoptions-swift.property)
- [var supportedBarcodeSymbologies: [BarcodeSymbology]](/documentation/vision/recognizedocumentsrequest/supportedbarcodesymbologies)
- [var supportedRecognitionLanguages: [Locale.Language]](/documentation/vision/recognizedocumentsrequest/supportedrecognitionlanguages)

### Getting the revision

- [let revision: RecognizeDocumentsRequest.Revision](/documentation/vision/recognizedocumentsrequest/revision-swift.property)
- [static let supportedRevisions: [RecognizeDocumentsRequest.Revision]](/documentation/vision/recognizedocumentsrequest/supportedrevisions)
- [RecognizeDocumentsRequest.Revision](/documentation/vision/recognizedocumentsrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/recognizedocumentsrequest/revision-swift.enum/revision1)
- [RecognizeTextRequest](/documentation/vision/recognizetextrequest)

### Creating a request

- [init(RecognizeTextRequest.Revision?)](/documentation/vision/recognizetextrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [RecognizedTextObservation](/documentation/vision/recognizedtextobservation)

#### Creating an observation

- [init(VNRecognizedTextObservation)](/documentation/vision/recognizedtextobservation/init(_:))

#### Inspecting an observation

- [var boundingRegion: NormalizedRegion](/documentation/vision/recognizedtextobservation/boundingregion)
- [let isTitle: Bool](/documentation/vision/recognizedtextobservation/istitle)
- [let recognitionLanguages: [Locale.Language]](/documentation/vision/recognizedtextobservation/recognitionlanguages)
- [let shouldWrapToNextLine: Bool?](/documentation/vision/recognizedtextobservation/shouldwraptonextline)
- [let textDirection: RecognizedTextObservation.Direction?](/documentation/vision/recognizedtextobservation/textdirection)
- [RecognizedTextObservation.Direction](/documentation/vision/recognizedtextobservation/direction)

##### Directions

- [case leftToRight](/documentation/vision/recognizedtextobservation/direction/lefttoright)
- [case rightToLeft](/documentation/vision/recognizedtextobservation/direction/righttoleft)
- [case topToBottom](/documentation/vision/recognizedtextobservation/direction/toptobottom)
- [var transcript: String](/documentation/vision/recognizedtextobservation/transcript)

#### Getting the recognized text

- [func topCandidates(Int) -> [RecognizedText]](/documentation/vision/recognizedtextobservation/topcandidates(_:))
- [RecognizedText](/documentation/vision/recognizedtext)

##### Getting the bounding box

- [func boundingBox(for: Range<String.Index>) -> RectangleObservation?](/documentation/vision/recognizedtext/boundingbox(for:))

##### Inspecting the recognized text

- [var string: String](/documentation/vision/recognizedtext/string)
- [var confidence: Float](/documentation/vision/recognizedtext/confidence)

### Configuring a request

- [var automaticallyDetectsLanguage: Bool](/documentation/vision/recognizetextrequest/automaticallydetectslanguage)
- [var usesLanguageCorrection: Bool](/documentation/vision/recognizetextrequest/useslanguagecorrection)
- [var supportedRecognitionLanguages: [Locale.Language]](/documentation/vision/recognizetextrequest/supportedrecognitionlanguages)
- [var customWords: [String]](/documentation/vision/recognizetextrequest/customwords)
- [var minimumTextHeightFraction: Float](/documentation/vision/recognizetextrequest/minimumtextheightfraction)
- [var recognitionLanguages: [Locale.Language]](/documentation/vision/recognizetextrequest/recognitionlanguages)
- [var recognitionLevel: RecognizeTextRequest.RecognitionLevel](/documentation/vision/recognizetextrequest/recognitionlevel-swift.property)
- [RecognizeTextRequest.RecognitionLevel](/documentation/vision/recognizetextrequest/recognitionlevel-swift.enum)

#### Getting the recognition levels

- [case accurate](/documentation/vision/recognizetextrequest/recognitionlevel-swift.enum/accurate)
- [case fast](/documentation/vision/recognizetextrequest/recognitionlevel-swift.enum/fast)

### Getting the revision

- [let revision: RecognizeTextRequest.Revision](/documentation/vision/recognizetextrequest/revision-swift.property)
- [static let supportedRevisions: [RecognizeTextRequest.Revision]](/documentation/vision/recognizetextrequest/supportedrevisions)
- [RecognizeTextRequest.Revision](/documentation/vision/recognizetextrequest/revision-swift.enum)

#### Getting the revision

- [case revision3](/documentation/vision/recognizetextrequest/revision-swift.enum/revision3)

## Facial analysis

- [Analyzing a selfie and visualizing its content](/documentation/vision/analyzing-a-selfie-and-visualizing-its-content)
- [DetectFaceCaptureQualityRequest](/documentation/vision/detectfacecapturequalityrequest)

### Creating a request

- [init(DetectFaceCaptureQualityRequest.Revision?)](/documentation/vision/detectfacecapturequalityrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [FaceObservation](/documentation/vision/faceobservation)

#### Creating an observation

- [init(VNFaceObservation)](/documentation/vision/faceobservation/init(_:))
- [init(boundingBox: NormalizedRect, revision: DetectFaceRectanglesRequest.Revision?)](/documentation/vision/faceobservation/init(boundingbox:revision:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [FaceObservation.Landmarks2D](/documentation/vision/faceobservation/landmarks2d)

##### Getting the landmarks

- [var faceContour: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/facecontour)
- [var innerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/innerlips)
- [var leftEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteye)
- [var leftEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteyebrow)
- [var leftPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/leftpupil)
- [var medianLine: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/medianline)
- [var nose: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nose)
- [var noseCrest: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nosecrest)
- [var outerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/outerlips)
- [var rightEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteye)
- [var rightEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteyebrow)
- [var rightPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/rightpupil)

##### Inspecting a landmark

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/originatingrequestdescriptor)

##### Getting all landmarks

- [var allPoints: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/allpoints)
- [FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/region)

###### Inspecting a region

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/region/originatingrequestdescriptor)
- [let points: [NormalizedPoint]](/documentation/vision/faceobservation/landmarks2d/region/points)
- [let pointsClassification: FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.property)
- [FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum)

###### Getting the point classifications

- [case closedPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/closedpath)
- [case disconnected](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/disconnected)
- [case openPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/openpath)
- [let precisionEstimatesPerPoint: [Float]?](/documentation/vision/faceobservation/landmarks2d/region/precisionestimatesperpoint)

###### Getting the points

- [func pointsInImageCoordinates(CGSize, origin: CoordinateOrigin) -> [CGPoint]](/documentation/vision/faceobservation/landmarks2d/region/pointsinimagecoordinates(_:origin:))
- [var landmarks: FaceObservation.Landmarks2D?](/documentation/vision/faceobservation/landmarks)
- [let pitch: Measurement<UnitAngle>](/documentation/vision/faceobservation/pitch)
- [let roll: Measurement<UnitAngle>](/documentation/vision/faceobservation/roll)
- [let yaw: Measurement<UnitAngle>](/documentation/vision/faceobservation/yaw)

#### Getting the capture quality

- [var captureQuality: FaceObservation.CaptureQuality?](/documentation/vision/faceobservation/capturequality-swift.property)
- [FaceObservation.CaptureQuality](/documentation/vision/faceobservation/capturequality-swift.struct)

##### Getting the score

- [let score: Float](/documentation/vision/faceobservation/capturequality-swift.struct/score)

##### Accessing the originating descriptor

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/capturequality-swift.struct/originatingrequestdescriptor)

### Configuring a request

- [var inputFaceObservations: [FaceObservation]?](/documentation/vision/detectfacecapturequalityrequest/inputfaceobservations)

### Getting the revision

- [let revision: DetectFaceCaptureQualityRequest.Revision](/documentation/vision/detectfacecapturequalityrequest/revision-swift.property)
- [static let supportedRevisions: [DetectFaceCaptureQualityRequest.Revision]](/documentation/vision/detectfacecapturequalityrequest/supportedrevisions)
- [DetectFaceCaptureQualityRequest.Revision](/documentation/vision/detectfacecapturequalityrequest/revision-swift.enum)

#### Getting the revision

- [case revision3](/documentation/vision/detectfacecapturequalityrequest/revision-swift.enum/revision3)
- [DetectFaceLandmarksRequest](/documentation/vision/detectfacelandmarksrequest)

### Creating a request

- [init(DetectFaceLandmarksRequest.Revision?)](/documentation/vision/detectfacelandmarksrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [FaceObservation](/documentation/vision/faceobservation)

#### Creating an observation

- [init(VNFaceObservation)](/documentation/vision/faceobservation/init(_:))
- [init(boundingBox: NormalizedRect, revision: DetectFaceRectanglesRequest.Revision?)](/documentation/vision/faceobservation/init(boundingbox:revision:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [FaceObservation.Landmarks2D](/documentation/vision/faceobservation/landmarks2d)

##### Getting the landmarks

- [var faceContour: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/facecontour)
- [var innerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/innerlips)
- [var leftEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteye)
- [var leftEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteyebrow)
- [var leftPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/leftpupil)
- [var medianLine: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/medianline)
- [var nose: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nose)
- [var noseCrest: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nosecrest)
- [var outerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/outerlips)
- [var rightEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteye)
- [var rightEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteyebrow)
- [var rightPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/rightpupil)

##### Inspecting a landmark

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/originatingrequestdescriptor)

##### Getting all landmarks

- [var allPoints: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/allpoints)
- [FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/region)

###### Inspecting a region

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/region/originatingrequestdescriptor)
- [let points: [NormalizedPoint]](/documentation/vision/faceobservation/landmarks2d/region/points)
- [let pointsClassification: FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.property)
- [FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum)

###### Getting the point classifications

- [case closedPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/closedpath)
- [case disconnected](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/disconnected)
- [case openPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/openpath)
- [let precisionEstimatesPerPoint: [Float]?](/documentation/vision/faceobservation/landmarks2d/region/precisionestimatesperpoint)

###### Getting the points

- [func pointsInImageCoordinates(CGSize, origin: CoordinateOrigin) -> [CGPoint]](/documentation/vision/faceobservation/landmarks2d/region/pointsinimagecoordinates(_:origin:))
- [var landmarks: FaceObservation.Landmarks2D?](/documentation/vision/faceobservation/landmarks)
- [let pitch: Measurement<UnitAngle>](/documentation/vision/faceobservation/pitch)
- [let roll: Measurement<UnitAngle>](/documentation/vision/faceobservation/roll)
- [let yaw: Measurement<UnitAngle>](/documentation/vision/faceobservation/yaw)

#### Getting the capture quality

- [var captureQuality: FaceObservation.CaptureQuality?](/documentation/vision/faceobservation/capturequality-swift.property)
- [FaceObservation.CaptureQuality](/documentation/vision/faceobservation/capturequality-swift.struct)

##### Getting the score

- [let score: Float](/documentation/vision/faceobservation/capturequality-swift.struct/score)

##### Accessing the originating descriptor

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/capturequality-swift.struct/originatingrequestdescriptor)

### Configuring a request

- [var inputFaceObservations: [FaceObservation]?](/documentation/vision/detectfacelandmarksrequest/inputfaceobservations)

### Getting the revision

- [let revision: DetectFaceLandmarksRequest.Revision](/documentation/vision/detectfacelandmarksrequest/revision-swift.property)
- [static let supportedRevisions: [DetectFaceLandmarksRequest.Revision]](/documentation/vision/detectfacelandmarksrequest/supportedrevisions)
- [DetectFaceLandmarksRequest.Revision](/documentation/vision/detectfacelandmarksrequest/revision-swift.enum)

#### Getting the revision

- [case revision3](/documentation/vision/detectfacelandmarksrequest/revision-swift.enum/revision3)
- [DetectFaceRectanglesRequest](/documentation/vision/detectfacerectanglesrequest)

### Creating a request

- [init(DetectFaceRectanglesRequest.Revision?)](/documentation/vision/detectfacerectanglesrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [FaceObservation](/documentation/vision/faceobservation)

#### Creating an observation

- [init(VNFaceObservation)](/documentation/vision/faceobservation/init(_:))
- [init(boundingBox: NormalizedRect, revision: DetectFaceRectanglesRequest.Revision?)](/documentation/vision/faceobservation/init(boundingbox:revision:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [FaceObservation.Landmarks2D](/documentation/vision/faceobservation/landmarks2d)

##### Getting the landmarks

- [var faceContour: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/facecontour)
- [var innerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/innerlips)
- [var leftEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteye)
- [var leftEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/lefteyebrow)
- [var leftPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/leftpupil)
- [var medianLine: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/medianline)
- [var nose: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nose)
- [var noseCrest: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/nosecrest)
- [var outerLips: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/outerlips)
- [var rightEye: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteye)
- [var rightEyebrow: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/righteyebrow)
- [var rightPupil: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/rightpupil)

##### Inspecting a landmark

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/originatingrequestdescriptor)

##### Getting all landmarks

- [var allPoints: FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/allpoints)
- [FaceObservation.Landmarks2D.Region](/documentation/vision/faceobservation/landmarks2d/region)

###### Inspecting a region

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/landmarks2d/region/originatingrequestdescriptor)
- [let points: [NormalizedPoint]](/documentation/vision/faceobservation/landmarks2d/region/points)
- [let pointsClassification: FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.property)
- [FaceObservation.Landmarks2D.Region.PointsClassification](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum)

###### Getting the point classifications

- [case closedPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/closedpath)
- [case disconnected](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/disconnected)
- [case openPath](/documentation/vision/faceobservation/landmarks2d/region/pointsclassification-swift.enum/openpath)
- [let precisionEstimatesPerPoint: [Float]?](/documentation/vision/faceobservation/landmarks2d/region/precisionestimatesperpoint)

###### Getting the points

- [func pointsInImageCoordinates(CGSize, origin: CoordinateOrigin) -> [CGPoint]](/documentation/vision/faceobservation/landmarks2d/region/pointsinimagecoordinates(_:origin:))
- [var landmarks: FaceObservation.Landmarks2D?](/documentation/vision/faceobservation/landmarks)
- [let pitch: Measurement<UnitAngle>](/documentation/vision/faceobservation/pitch)
- [let roll: Measurement<UnitAngle>](/documentation/vision/faceobservation/roll)
- [let yaw: Measurement<UnitAngle>](/documentation/vision/faceobservation/yaw)

#### Getting the capture quality

- [var captureQuality: FaceObservation.CaptureQuality?](/documentation/vision/faceobservation/capturequality-swift.property)
- [FaceObservation.CaptureQuality](/documentation/vision/faceobservation/capturequality-swift.struct)

##### Getting the score

- [let score: Float](/documentation/vision/faceobservation/capturequality-swift.struct/score)

##### Accessing the originating descriptor

- [let originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/faceobservation/capturequality-swift.struct/originatingrequestdescriptor)

### Getting the revision

- [let revision: DetectFaceRectanglesRequest.Revision](/documentation/vision/detectfacerectanglesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectFaceRectanglesRequest.Revision]](/documentation/vision/detectfacerectanglesrequest/supportedrevisions)
- [DetectFaceRectanglesRequest.Revision](/documentation/vision/detectfacerectanglesrequest/revision-swift.enum)

#### Getting the revision

- [case revision3](/documentation/vision/detectfacerectanglesrequest/revision-swift.enum/revision3)

## Image segmentation and subject lifting

- [GenerateForegroundInstanceMaskRequest](/documentation/vision/generateforegroundinstancemaskrequest)

### Creating a request

- [init(GenerateForegroundInstanceMaskRequest.Revision?)](/documentation/vision/generateforegroundinstancemaskrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [InstanceMaskObservation](/documentation/vision/instancemaskobservation)

#### Creating an observation

- [init?(VNInstanceMaskObservation)](/documentation/vision/instancemaskobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

#### Generating a mask

- [func generateMask(for: IndexSet) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatemask(for:))
- [func generateMaskedImage(for: IndexSet, imageFrom: ImageRequestHandler, croppedToInstancesExtent: Bool) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatemaskedimage(for:imagefrom:croppedtoinstancesextent:))
- [func generateScaledMask(for: IndexSet, scaledToImageFrom: ImageRequestHandler) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatescaledmask(for:scaledtoimagefrom:))

#### Getting instances

- [func instanceAtPoint(NormalizedPoint) -> IndexSet](/documentation/vision/instancemaskobservation/instanceatpoint(_:))
- [let allInstances: IndexSet](/documentation/vision/instancemaskobservation/allinstances)
- [let allInstancesMask: PixelBufferObservation](/documentation/vision/instancemaskobservation/allinstancesmask)
- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

##### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

##### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

##### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))

### Getting the revision

- [let revision: GenerateForegroundInstanceMaskRequest.Revision](/documentation/vision/generateforegroundinstancemaskrequest/revision-swift.property)
- [static let supportedRevisions: [GenerateForegroundInstanceMaskRequest.Revision]](/documentation/vision/generateforegroundinstancemaskrequest/supportedrevisions)
- [GenerateForegroundInstanceMaskRequest.Revision](/documentation/vision/generateforegroundinstancemaskrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/generateforegroundinstancemaskrequest/revision-swift.enum/revision1)
- [GeneratePersonInstanceMaskRequest](/documentation/vision/generatepersoninstancemaskrequest)

### Creating a request

- [init(GeneratePersonInstanceMaskRequest.Revision?)](/documentation/vision/generatepersoninstancemaskrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [InstanceMaskObservation](/documentation/vision/instancemaskobservation)

#### Creating an observation

- [init?(VNInstanceMaskObservation)](/documentation/vision/instancemaskobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

#### Generating a mask

- [func generateMask(for: IndexSet) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatemask(for:))
- [func generateMaskedImage(for: IndexSet, imageFrom: ImageRequestHandler, croppedToInstancesExtent: Bool) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatemaskedimage(for:imagefrom:croppedtoinstancesextent:))
- [func generateScaledMask(for: IndexSet, scaledToImageFrom: ImageRequestHandler) throws -> CVPixelBuffer](/documentation/vision/instancemaskobservation/generatescaledmask(for:scaledtoimagefrom:))

#### Getting instances

- [func instanceAtPoint(NormalizedPoint) -> IndexSet](/documentation/vision/instancemaskobservation/instanceatpoint(_:))
- [let allInstances: IndexSet](/documentation/vision/instancemaskobservation/allinstances)
- [let allInstancesMask: PixelBufferObservation](/documentation/vision/instancemaskobservation/allinstancesmask)
- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

##### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

##### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

##### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))

### Getting the revision

- [let revision: GeneratePersonInstanceMaskRequest.Revision](/documentation/vision/generatepersoninstancemaskrequest/revision-swift.property)
- [static let supportedRevisions: [GeneratePersonInstanceMaskRequest.Revision]](/documentation/vision/generatepersoninstancemaskrequest/supportedrevisions)
- [GeneratePersonInstanceMaskRequest.Revision](/documentation/vision/generatepersoninstancemaskrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/generatepersoninstancemaskrequest/revision-swift.enum/revision1)
- [GeneratePersonSegmentationRequest](/documentation/vision/generatepersonsegmentationrequest)

### Creating a request

- [init(GeneratePersonSegmentationRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/generatepersonsegmentationrequest/init(_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

#### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

#### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

#### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))

### Configuring a request

- [var qualityLevel: GeneratePersonSegmentationRequest.QualityLevel](/documentation/vision/generatepersonsegmentationrequest/qualitylevel-swift.property)
- [GeneratePersonSegmentationRequest.QualityLevel](/documentation/vision/generatepersonsegmentationrequest/qualitylevel-swift.enum)

#### Getting the quality levels

- [case accurate](/documentation/vision/generatepersonsegmentationrequest/qualitylevel-swift.enum/accurate)
- [case balanced](/documentation/vision/generatepersonsegmentationrequest/qualitylevel-swift.enum/balanced)
- [case fast](/documentation/vision/generatepersonsegmentationrequest/qualitylevel-swift.enum/fast)
- [var outputPixelFormatType: OSType](/documentation/vision/generatepersonsegmentationrequest/outputpixelformattype)
- [var supportedOutputPixelFormats: [OSType]](/documentation/vision/generatepersonsegmentationrequest/supportedoutputpixelformats)

### Getting the revision

- [let revision: GeneratePersonSegmentationRequest.Revision](/documentation/vision/generatepersonsegmentationrequest/revision-swift.property)
- [static let supportedRevisions: [GeneratePersonSegmentationRequest.Revision]](/documentation/vision/generatepersonsegmentationrequest/supportedrevisions)
- [GeneratePersonSegmentationRequest.Revision](/documentation/vision/generatepersonsegmentationrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/generatepersonsegmentationrequest/revision-swift.enum/revision1)

## Pose analysis

- [DetectAnimalBodyPoseRequest](/documentation/vision/detectanimalbodyposerequest)

### Creating a request

- [init(DetectAnimalBodyPoseRequest.Revision?)](/documentation/vision/detectanimalbodyposerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [AnimalBodyPoseObservation](/documentation/vision/animalbodyposeobservation)

#### Creating an observation

- [init(VNAnimalBodyPoseObservation)](/documentation/vision/animalbodyposeobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

#### Getting the joints

- [AnimalBodyPoseObservation.JointName](/documentation/vision/animalbodyposeobservation/jointname)

##### Getting the joint names

- [case leftBackElbow](/documentation/vision/animalbodyposeobservation/jointname/leftbackelbow)
- [case leftBackKnee](/documentation/vision/animalbodyposeobservation/jointname/leftbackknee)
- [case leftBackPaw](/documentation/vision/animalbodyposeobservation/jointname/leftbackpaw)
- [case leftEarBottom](/documentation/vision/animalbodyposeobservation/jointname/leftearbottom)
- [case leftEarMiddle](/documentation/vision/animalbodyposeobservation/jointname/leftearmiddle)
- [case leftEarTop](/documentation/vision/animalbodyposeobservation/jointname/lefteartop)
- [case leftEye](/documentation/vision/animalbodyposeobservation/jointname/lefteye)
- [case leftFrontElbow](/documentation/vision/animalbodyposeobservation/jointname/leftfrontelbow)
- [case leftFrontKnee](/documentation/vision/animalbodyposeobservation/jointname/leftfrontknee)
- [case leftFrontPaw](/documentation/vision/animalbodyposeobservation/jointname/leftfrontpaw)
- [case neck](/documentation/vision/animalbodyposeobservation/jointname/neck)
- [case nose](/documentation/vision/animalbodyposeobservation/jointname/nose)
- [case rightBackElbow](/documentation/vision/animalbodyposeobservation/jointname/rightbackelbow)
- [case rightBackKnee](/documentation/vision/animalbodyposeobservation/jointname/rightbackknee)
- [case rightBackPaw](/documentation/vision/animalbodyposeobservation/jointname/rightbackpaw)
- [case rightEarBottom](/documentation/vision/animalbodyposeobservation/jointname/rightearbottom)
- [case rightEarMiddle](/documentation/vision/animalbodyposeobservation/jointname/rightearmiddle)
- [case rightEarTop](/documentation/vision/animalbodyposeobservation/jointname/righteartop)
- [case rightEye](/documentation/vision/animalbodyposeobservation/jointname/righteye)
- [case rightFrontElbow](/documentation/vision/animalbodyposeobservation/jointname/rightfrontelbow)
- [case rightFrontKnee](/documentation/vision/animalbodyposeobservation/jointname/rightfrontknee)
- [case rightFrontPaw](/documentation/vision/animalbodyposeobservation/jointname/rightfrontpaw)
- [case tailBottom](/documentation/vision/animalbodyposeobservation/jointname/tailbottom)
- [case tailMiddle](/documentation/vision/animalbodyposeobservation/jointname/tailmiddle)
- [case tailTop](/documentation/vision/animalbodyposeobservation/jointname/tailtop)
- [AnimalBodyPoseObservation.JointsGroupName](/documentation/vision/animalbodyposeobservation/jointsgroupname)

##### Getting the group names

- [case forelegs](/documentation/vision/animalbodyposeobservation/jointsgroupname/forelegs)
- [case head](/documentation/vision/animalbodyposeobservation/jointsgroupname/head)
- [case hindlegs](/documentation/vision/animalbodyposeobservation/jointsgroupname/hindlegs)
- [case tail](/documentation/vision/animalbodyposeobservation/jointsgroupname/tail)
- [case trunk](/documentation/vision/animalbodyposeobservation/jointsgroupname/trunk)

### Configuring a request

- [var supportedJointNames: [AnimalBodyPoseObservation.JointName]](/documentation/vision/detectanimalbodyposerequest/supportedjointnames)
- [var supportedJointsGroupNames: [AnimalBodyPoseObservation.JointsGroupName]](/documentation/vision/detectanimalbodyposerequest/supportedjointsgroupnames)

### Getting the revision

- [let revision: DetectAnimalBodyPoseRequest.Revision](/documentation/vision/detectanimalbodyposerequest/revision-swift.property)
- [static let supportedRevisions: [DetectAnimalBodyPoseRequest.Revision]](/documentation/vision/detectanimalbodyposerequest/supportedrevisions)
- [DetectAnimalBodyPoseRequest.Revision](/documentation/vision/detectanimalbodyposerequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detectanimalbodyposerequest/revision-swift.enum/revision1)
- [DetectHumanBodyPose3DRequest](/documentation/vision/detecthumanbodypose3drequest)

### Creating a request

- [init(DetectHumanBodyPose3DRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/detecthumanbodypose3drequest/init(_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [HumanBodyPose3DObservation](/documentation/vision/humanbodypose3dobservation)

#### Creating an observation

- [init(VNHumanBodyPose3DObservation)](/documentation/vision/humanbodypose3dobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let bodyHeight: Measurement<UnitLength>](/documentation/vision/humanbodypose3dobservation/bodyheight)
- [let cameraOriginMatrix: simd_float4x4](/documentation/vision/humanbodypose3dobservation/cameraoriginmatrix)
- [HumanBodyPose3DObservation.EstimationTechnique](/documentation/vision/humanbodypose3dobservation/estimationtechnique)

##### Getting estimation techniques

- [case measured](/documentation/vision/humanbodypose3dobservation/estimationtechnique/measured)
- [case reference](/documentation/vision/humanbodypose3dobservation/estimationtechnique/reference)
- [let heightEstimationTechnique: HumanBodyPose3DObservation.EstimationTechnique](/documentation/vision/humanbodypose3dobservation/heightestimationtechnique)

#### Getting the joints

- [func allJoints(in: HumanBodyPose3DObservation.JointsGroupName?) -> [HumanBodyPose3DObservation.JointName : Joint3D]](/documentation/vision/humanbodypose3dobservation/alljoints(in:))
- [var availableJointsGroupNames: [HumanBodyPose3DObservation.JointsGroupName]](/documentation/vision/humanbodypose3dobservation/availablejointsgroupnames)
- [HumanBodyPose3DObservation.JointsGroupName](/documentation/vision/humanbodypose3dobservation/jointsgroupname)

##### Getting the group names

- [case head](/documentation/vision/humanbodypose3dobservation/jointsgroupname/head)
- [case leftArm](/documentation/vision/humanbodypose3dobservation/jointsgroupname/leftarm)
- [case leftLeg](/documentation/vision/humanbodypose3dobservation/jointsgroupname/leftleg)
- [case rightArm](/documentation/vision/humanbodypose3dobservation/jointsgroupname/rightarm)
- [case rightLeg](/documentation/vision/humanbodypose3dobservation/jointsgroupname/rightleg)
- [case torso](/documentation/vision/humanbodypose3dobservation/jointsgroupname/torso)
- [func joint(for: HumanBodyPose3DObservation.JointName) -> Joint3D?](/documentation/vision/humanbodypose3dobservation/joint(for:))
- [var availableJointNames: [HumanBodyPose3DObservation.JointName]](/documentation/vision/humanbodypose3dobservation/availablejointnames)
- [HumanBodyPose3DObservation.JointName](/documentation/vision/humanbodypose3dobservation/jointname)

##### Getting the joint names

- [case centerHead](/documentation/vision/humanbodypose3dobservation/jointname/centerhead)
- [case centerShoulder](/documentation/vision/humanbodypose3dobservation/jointname/centershoulder)
- [case leftAnkle](/documentation/vision/humanbodypose3dobservation/jointname/leftankle)
- [case leftElbow](/documentation/vision/humanbodypose3dobservation/jointname/leftelbow)
- [case leftHip](/documentation/vision/humanbodypose3dobservation/jointname/lefthip)
- [case leftKnee](/documentation/vision/humanbodypose3dobservation/jointname/leftknee)
- [case leftShoulder](/documentation/vision/humanbodypose3dobservation/jointname/leftshoulder)
- [case leftWrist](/documentation/vision/humanbodypose3dobservation/jointname/leftwrist)
- [case rightAnkle](/documentation/vision/humanbodypose3dobservation/jointname/rightankle)
- [case rightElbow](/documentation/vision/humanbodypose3dobservation/jointname/rightelbow)
- [case rightHip](/documentation/vision/humanbodypose3dobservation/jointname/righthip)
- [case rightKnee](/documentation/vision/humanbodypose3dobservation/jointname/rightknee)
- [case rightShoulder](/documentation/vision/humanbodypose3dobservation/jointname/rightshoulder)
- [case rightWrist](/documentation/vision/humanbodypose3dobservation/jointname/rightwrist)
- [case root](/documentation/vision/humanbodypose3dobservation/jointname/root)
- [case spine](/documentation/vision/humanbodypose3dobservation/jointname/spine)
- [case topHead](/documentation/vision/humanbodypose3dobservation/jointname/tophead)

#### Getting the joint name

- [func parentJointName(for: HumanBodyPose3DObservation.JointName) -> HumanBodyPose3DObservation.JointName](/documentation/vision/humanbodypose3dobservation/parentjointname(for:))

#### Getting the camera position

- [func cameraRelativePosition(for: HumanBodyPose3DObservation.JointName) -> simd_float4x4](/documentation/vision/humanbodypose3dobservation/camerarelativeposition(for:))

#### Getting the joint position

- [func pointInImage(for: HumanBodyPose3DObservation.JointName) -> NormalizedPoint](/documentation/vision/humanbodypose3dobservation/pointinimage(for:))

### Configuring a request

- [var supportedJointNames: [HumanBodyPose3DObservation.JointName]](/documentation/vision/detecthumanbodypose3drequest/supportedjointnames)
- [var supportedJointsGroupNames: [HumanBodyPose3DObservation.JointsGroupName]](/documentation/vision/detecthumanbodypose3drequest/supportedjointsgroupnames)

### Getting the revision

- [let revision: DetectHumanBodyPose3DRequest.Revision](/documentation/vision/detecthumanbodypose3drequest/revision-swift.property)
- [static let supportedRevisions: [DetectHumanBodyPose3DRequest.Revision]](/documentation/vision/detecthumanbodypose3drequest/supportedrevisions)
- [DetectHumanBodyPose3DRequest.Revision](/documentation/vision/detecthumanbodypose3drequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detecthumanbodypose3drequest/revision-swift.enum/revision1)
- [DetectHumanBodyPoseRequest](/documentation/vision/detecthumanbodyposerequest)

### Creating a request

- [init(DetectHumanBodyPoseRequest.Revision?)](/documentation/vision/detecthumanbodyposerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [HumanBodyPoseObservation](/documentation/vision/humanbodyposeobservation)

#### Creating an observation

- [init(VNHumanBodyPoseObservation)](/documentation/vision/humanbodyposeobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let leftHand: HumanHandPoseObservation?](/documentation/vision/humanbodyposeobservation/lefthand)
- [let rightHand: HumanHandPoseObservation?](/documentation/vision/humanbodyposeobservation/righthand)
- [HumanHandPoseObservation](/documentation/vision/humanhandposeobservation)

##### Creating an observation

- [init(VNHumanHandPoseObservation)](/documentation/vision/humanhandposeobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let chirality: HumanHandPoseObservation.Chirality?](/documentation/vision/humanhandposeobservation/chirality-swift.property)
- [HumanHandPoseObservation.Chirality](/documentation/vision/humanhandposeobservation/chirality-swift.enum)

###### Getting the handedness

- [case left](/documentation/vision/humanhandposeobservation/chirality-swift.enum/left)
- [case right](/documentation/vision/humanhandposeobservation/chirality-swift.enum/right)
- [var keypoints: MLMultiArray](/documentation/vision/humanhandposeobservation/keypoints)

##### Getting the joints

- [HumanHandPoseObservation.JointsGroupName](/documentation/vision/humanhandposeobservation/jointsgroupname)

###### Getting the group name

- [case indexFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/indexfinger)
- [case littleFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/littlefinger)
- [case middleFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/middlefinger)
- [case ringFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/ringfinger)
- [case thumb](/documentation/vision/humanhandposeobservation/jointsgroupname/thumb)
- [HumanHandPoseObservation.JointName](/documentation/vision/humanhandposeobservation/jointname)

###### Getting the thumb finger joint name

- [case thumbCMC](/documentation/vision/humanhandposeobservation/jointname/thumbcmc)
- [case thumbIP](/documentation/vision/humanhandposeobservation/jointname/thumbip)
- [case thumbMP](/documentation/vision/humanhandposeobservation/jointname/thumbmp)
- [case thumbTip](/documentation/vision/humanhandposeobservation/jointname/thumbtip)

###### Getting the index finger joint name

- [case indexDIP](/documentation/vision/humanhandposeobservation/jointname/indexdip)
- [case indexMCP](/documentation/vision/humanhandposeobservation/jointname/indexmcp)
- [case indexPIP](/documentation/vision/humanhandposeobservation/jointname/indexpip)
- [case indexTip](/documentation/vision/humanhandposeobservation/jointname/indextip)

###### Getting the middle finger joint name

- [case middleDIP](/documentation/vision/humanhandposeobservation/jointname/middledip)
- [case middleMCP](/documentation/vision/humanhandposeobservation/jointname/middlemcp)
- [case middlePIP](/documentation/vision/humanhandposeobservation/jointname/middlepip)
- [case middleTip](/documentation/vision/humanhandposeobservation/jointname/middletip)

###### Getting the ring finger joint name

- [case ringDIP](/documentation/vision/humanhandposeobservation/jointname/ringdip)
- [case ringMCP](/documentation/vision/humanhandposeobservation/jointname/ringmcp)
- [case ringPIP](/documentation/vision/humanhandposeobservation/jointname/ringpip)
- [case ringTip](/documentation/vision/humanhandposeobservation/jointname/ringtip)

###### Getting the little finger joint name

- [case littleDIP](/documentation/vision/humanhandposeobservation/jointname/littledip)
- [case littleMCP](/documentation/vision/humanhandposeobservation/jointname/littlemcp)
- [case littlePIP](/documentation/vision/humanhandposeobservation/jointname/littlepip)
- [case littleTip](/documentation/vision/humanhandposeobservation/jointname/littletip)

###### Getting the wrist joint name

- [case wrist](/documentation/vision/humanhandposeobservation/jointname/wrist)
- [var keypoints: MLMultiArray](/documentation/vision/humanbodyposeobservation/keypoints)

#### Getting the joints

- [HumanBodyPoseObservation.JointsGroupName](/documentation/vision/humanbodyposeobservation/jointsgroupname)

##### Getting the group names

- [case face](/documentation/vision/humanbodyposeobservation/jointsgroupname/face)
- [case leftArm](/documentation/vision/humanbodyposeobservation/jointsgroupname/leftarm)
- [case leftLeg](/documentation/vision/humanbodyposeobservation/jointsgroupname/leftleg)
- [case rightArm](/documentation/vision/humanbodyposeobservation/jointsgroupname/rightarm)
- [case rightLeg](/documentation/vision/humanbodyposeobservation/jointsgroupname/rightleg)
- [case torso](/documentation/vision/humanbodyposeobservation/jointsgroupname/torso)
- [HumanBodyPoseObservation.JointName](/documentation/vision/humanbodyposeobservation/jointname)

##### Getting the joint names

- [case leftAnkle](/documentation/vision/humanbodyposeobservation/jointname/leftankle)
- [case leftEar](/documentation/vision/humanbodyposeobservation/jointname/leftear)
- [case leftElbow](/documentation/vision/humanbodyposeobservation/jointname/leftelbow)
- [case leftEye](/documentation/vision/humanbodyposeobservation/jointname/lefteye)
- [case leftHip](/documentation/vision/humanbodyposeobservation/jointname/lefthip)
- [case leftKnee](/documentation/vision/humanbodyposeobservation/jointname/leftknee)
- [case leftShoulder](/documentation/vision/humanbodyposeobservation/jointname/leftshoulder)
- [case leftWrist](/documentation/vision/humanbodyposeobservation/jointname/leftwrist)
- [case neck](/documentation/vision/humanbodyposeobservation/jointname/neck)
- [case nose](/documentation/vision/humanbodyposeobservation/jointname/nose)
- [case rightAnkle](/documentation/vision/humanbodyposeobservation/jointname/rightankle)
- [case rightEar](/documentation/vision/humanbodyposeobservation/jointname/rightear)
- [case rightElbow](/documentation/vision/humanbodyposeobservation/jointname/rightelbow)
- [case rightEye](/documentation/vision/humanbodyposeobservation/jointname/righteye)
- [case rightHip](/documentation/vision/humanbodyposeobservation/jointname/righthip)
- [case rightKnee](/documentation/vision/humanbodyposeobservation/jointname/rightknee)
- [case rightShoulder](/documentation/vision/humanbodyposeobservation/jointname/rightshoulder)
- [case rightWrist](/documentation/vision/humanbodyposeobservation/jointname/rightwrist)
- [case root](/documentation/vision/humanbodyposeobservation/jointname/root)

### Configuring a request

- [var detectsHands: Bool](/documentation/vision/detecthumanbodyposerequest/detectshands)
- [var supportedJointNames: [HumanBodyPoseObservation.JointName]](/documentation/vision/detecthumanbodyposerequest/supportedjointnames)
- [var supportedJointsGroupNames: [HumanBodyPoseObservation.JointsGroupName]](/documentation/vision/detecthumanbodyposerequest/supportedjointsgroupnames)

### Getting the revision

- [let revision: DetectHumanBodyPoseRequest.Revision](/documentation/vision/detecthumanbodyposerequest/revision-swift.property)
- [static let supportedRevisions: [DetectHumanBodyPoseRequest.Revision]](/documentation/vision/detecthumanbodyposerequest/supportedrevisions)
- [DetectHumanBodyPoseRequest.Revision](/documentation/vision/detecthumanbodyposerequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/detecthumanbodyposerequest/revision-swift.enum/revision2)
- [DetectHumanHandPoseRequest](/documentation/vision/detecthumanhandposerequest)

### Creating a request

- [init(DetectHumanHandPoseRequest.Revision?)](/documentation/vision/detecthumanhandposerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [HumanHandPoseObservation](/documentation/vision/humanhandposeobservation)

#### Creating an observation

- [init(VNHumanHandPoseObservation)](/documentation/vision/humanhandposeobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let chirality: HumanHandPoseObservation.Chirality?](/documentation/vision/humanhandposeobservation/chirality-swift.property)
- [HumanHandPoseObservation.Chirality](/documentation/vision/humanhandposeobservation/chirality-swift.enum)

##### Getting the handedness

- [case left](/documentation/vision/humanhandposeobservation/chirality-swift.enum/left)
- [case right](/documentation/vision/humanhandposeobservation/chirality-swift.enum/right)
- [var keypoints: MLMultiArray](/documentation/vision/humanhandposeobservation/keypoints)

#### Getting the joints

- [HumanHandPoseObservation.JointsGroupName](/documentation/vision/humanhandposeobservation/jointsgroupname)

##### Getting the group name

- [case indexFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/indexfinger)
- [case littleFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/littlefinger)
- [case middleFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/middlefinger)
- [case ringFinger](/documentation/vision/humanhandposeobservation/jointsgroupname/ringfinger)
- [case thumb](/documentation/vision/humanhandposeobservation/jointsgroupname/thumb)
- [HumanHandPoseObservation.JointName](/documentation/vision/humanhandposeobservation/jointname)

##### Getting the thumb finger joint name

- [case thumbCMC](/documentation/vision/humanhandposeobservation/jointname/thumbcmc)
- [case thumbIP](/documentation/vision/humanhandposeobservation/jointname/thumbip)
- [case thumbMP](/documentation/vision/humanhandposeobservation/jointname/thumbmp)
- [case thumbTip](/documentation/vision/humanhandposeobservation/jointname/thumbtip)

##### Getting the index finger joint name

- [case indexDIP](/documentation/vision/humanhandposeobservation/jointname/indexdip)
- [case indexMCP](/documentation/vision/humanhandposeobservation/jointname/indexmcp)
- [case indexPIP](/documentation/vision/humanhandposeobservation/jointname/indexpip)
- [case indexTip](/documentation/vision/humanhandposeobservation/jointname/indextip)

##### Getting the middle finger joint name

- [case middleDIP](/documentation/vision/humanhandposeobservation/jointname/middledip)
- [case middleMCP](/documentation/vision/humanhandposeobservation/jointname/middlemcp)
- [case middlePIP](/documentation/vision/humanhandposeobservation/jointname/middlepip)
- [case middleTip](/documentation/vision/humanhandposeobservation/jointname/middletip)

##### Getting the ring finger joint name

- [case ringDIP](/documentation/vision/humanhandposeobservation/jointname/ringdip)
- [case ringMCP](/documentation/vision/humanhandposeobservation/jointname/ringmcp)
- [case ringPIP](/documentation/vision/humanhandposeobservation/jointname/ringpip)
- [case ringTip](/documentation/vision/humanhandposeobservation/jointname/ringtip)

##### Getting the little finger joint name

- [case littleDIP](/documentation/vision/humanhandposeobservation/jointname/littledip)
- [case littleMCP](/documentation/vision/humanhandposeobservation/jointname/littlemcp)
- [case littlePIP](/documentation/vision/humanhandposeobservation/jointname/littlepip)
- [case littleTip](/documentation/vision/humanhandposeobservation/jointname/littletip)

##### Getting the wrist joint name

- [case wrist](/documentation/vision/humanhandposeobservation/jointname/wrist)

### Configuring a request

- [var maximumHandCount: Int](/documentation/vision/detecthumanhandposerequest/maximumhandcount)
- [var supportedJointNames: [HumanHandPoseObservation.JointName]](/documentation/vision/detecthumanhandposerequest/supportedjointnames)
- [var supportedJointsGroupNames: [HumanHandPoseObservation.JointsGroupName]](/documentation/vision/detecthumanhandposerequest/supportedjointsgroupnames)

### Getting the revision

- [let revision: DetectHumanHandPoseRequest.Revision](/documentation/vision/detecthumanhandposerequest/revision-swift.property)
- [static let supportedRevisions: [DetectHumanHandPoseRequest.Revision]](/documentation/vision/detecthumanhandposerequest/supportedrevisions)
- [DetectHumanHandPoseRequest.Revision](/documentation/vision/detecthumanhandposerequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detecthumanhandposerequest/revision-swift.enum/revision1)
- [Supporting Pose Types](/documentation/vision/supporting-pose-types)

### Joints

- [Joint](/documentation/vision/joint)

#### Inspecting a joint

- [let confidence: Float](/documentation/vision/joint/confidence)
- [let jointName: String](/documentation/vision/joint/jointname)
- [let location: NormalizedPoint](/documentation/vision/joint/location)

#### Getting the distance to a joint

- [func distance(to: Joint) -> CGFloat](/documentation/vision/joint/distance(to:))
- [Joint3D](/documentation/vision/joint3d)

#### Creating a joint

- [init(position: simd_float4x4, localPosition: simd_float4x4, identifer: String, parentJoint: String)](/documentation/vision/joint3d/init(position:localposition:identifer:parentjoint:))

#### Inspecting a joint

- [let localPosition: simd_float4x4](/documentation/vision/joint3d/localposition)
- [let position: simd_float4x4](/documentation/vision/joint3d/position)
- [let parentJoint: String](/documentation/vision/joint3d/parentjoint)
- [let identifier: String](/documentation/vision/joint3d/identifier)

### Handedness

- [Chirality](/documentation/vision/chirality)

#### Getting the hand sidedness

- [case left](/documentation/vision/chirality/left)
- [case right](/documentation/vision/chirality/right)

## Image classification and recognition

- [Classifying images for categorization and search](/documentation/vision/classifying-images-for-categorization-and-search)
- [ClassifyImageRequest](/documentation/vision/classifyimagerequest)

### Creating a request

- [init(ClassifyImageRequest.Revision?)](/documentation/vision/classifyimagerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [ClassificationObservation](/documentation/vision/classificationobservation)

#### Creating an observation

- [init(VNClassificationObservation)](/documentation/vision/classificationobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var hasPrecisionRecallCurve: Bool](/documentation/vision/classificationobservation/hasprecisionrecallcurve)
- [let identifier: String](/documentation/vision/classificationobservation/identifier)

#### Determining precision and recall

- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumrecall(_:forprecision:))

### Configuring a request

- [var cropAndScaleAction: ImageCropAndScaleAction](/documentation/vision/classifyimagerequest/cropandscaleaction)
- [ImageCropAndScaleAction](/documentation/vision/imagecropandscaleaction)

#### Getting the actions

- [case centerCrop](/documentation/vision/imagecropandscaleaction/centercrop)
- [case scaleToFit](/documentation/vision/imagecropandscaleaction/scaletofit)
- [case scaleToFill](/documentation/vision/imagecropandscaleaction/scaletofill)
- [case scaleToFitPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofitplus90ccwrotation)
- [case scaleToFillPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofillplus90ccwrotation)
- [var supportedIdentifiers: [String]](/documentation/vision/classifyimagerequest/supportedidentifiers)

### Getting the revision

- [let revision: ClassifyImageRequest.Revision](/documentation/vision/classifyimagerequest/revision-swift.property)
- [static let supportedRevisions: [ClassifyImageRequest.Revision]](/documentation/vision/classifyimagerequest/supportedrevisions)
- [ClassifyImageRequest.Revision](/documentation/vision/classifyimagerequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/classifyimagerequest/revision-swift.enum/revision2)
- [DetectHumanRectanglesRequest](/documentation/vision/detecthumanrectanglesrequest)

### Creating a request

- [init(DetectHumanRectanglesRequest.Revision?)](/documentation/vision/detecthumanrectanglesrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [HumanObservation](/documentation/vision/humanobservation)

#### Creating an observation

- [init(VNHumanObservation)](/documentation/vision/humanobservation/init(_:))
- [init(boundingBox: NormalizedRect, revision: DetectHumanRectanglesRequest.Revision?)](/documentation/vision/humanobservation/init(boundingbox:revision:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let isUpperBodyOnly: Bool](/documentation/vision/humanobservation/isupperbodyonly)

### Configuring a request

- [var upperBodyOnly: Bool](/documentation/vision/detecthumanrectanglesrequest/upperbodyonly)

### Getting the revision

- [let revision: DetectHumanRectanglesRequest.Revision](/documentation/vision/detecthumanrectanglesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectHumanRectanglesRequest.Revision]](/documentation/vision/detecthumanrectanglesrequest/supportedrevisions)
- [DetectHumanRectanglesRequest.Revision](/documentation/vision/detecthumanrectanglesrequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/detecthumanrectanglesrequest/revision-swift.enum/revision2)
- [RecognizeAnimalsRequest](/documentation/vision/recognizeanimalsrequest)

### Creating a request

- [init(RecognizeAnimalsRequest.Revision?)](/documentation/vision/recognizeanimalsrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [RecognizedObjectObservation](/documentation/vision/recognizedobjectobservation)

#### Creating an observation

- [init(VNRecognizedObjectObservation)](/documentation/vision/recognizedobjectobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let labels: [ClassificationObservation]](/documentation/vision/recognizedobjectobservation/labels)
- [ClassificationObservation](/documentation/vision/classificationobservation)

##### Creating an observation

- [init(VNClassificationObservation)](/documentation/vision/classificationobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var hasPrecisionRecallCurve: Bool](/documentation/vision/classificationobservation/hasprecisionrecallcurve)
- [let identifier: String](/documentation/vision/classificationobservation/identifier)

##### Determining precision and recall

- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumrecall(_:forprecision:))

### Configuring a request

- [var supportedAnimals: [RecognizeAnimalsRequest.Animal]](/documentation/vision/recognizeanimalsrequest/supportedanimals)
- [RecognizeAnimalsRequest.Animal](/documentation/vision/recognizeanimalsrequest/animal)

#### Getting the animals

- [case cat](/documentation/vision/recognizeanimalsrequest/animal/cat)
- [case dog](/documentation/vision/recognizeanimalsrequest/animal/dog)

### Getting the revision

- [let revision: RecognizeAnimalsRequest.Revision](/documentation/vision/recognizeanimalsrequest/revision-swift.property)
- [static let supportedRevisions: [RecognizeAnimalsRequest.Revision]](/documentation/vision/recognizeanimalsrequest/supportedrevisions)
- [RecognizeAnimalsRequest.Revision](/documentation/vision/recognizeanimalsrequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/recognizeanimalsrequest/revision-swift.enum/revision2)

## Shape and edge detection

- [DetectContoursRequest](/documentation/vision/detectcontoursrequest)

### Creating a request

- [init(DetectContoursRequest.Revision?)](/documentation/vision/detectcontoursrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [ContoursObservation](/documentation/vision/contoursobservation)

#### Creating an observation

- [init(VNContoursObservation)](/documentation/vision/contoursobservation/init(_:))

#### Inspecting an observation

- [var contourCount: Int](/documentation/vision/contoursobservation/contourcount)
- [var normalizedPath: CGPath](/documentation/vision/contoursobservation/normalizedpath)
- [var topLevelContours: [ContoursObservation.Contour]](/documentation/vision/contoursobservation/toplevelcontours)

#### Getting the contours

- [ContoursObservation.Contour](/documentation/vision/contoursobservation/contour)

##### Inspecting a contour

- [var aspectRatio: Float](/documentation/vision/contoursobservation/contour/aspectratio)
- [var boundingBox: NormalizedRect](/documentation/vision/contoursobservation/contour/boundingbox)
- [var boundingQuad: RectangleObservation](/documentation/vision/contoursobservation/contour/boundingquad)
- [var childContours: [ContoursObservation.Contour]](/documentation/vision/contoursobservation/contour/childcontours)
- [var indexPath: IndexPath](/documentation/vision/contoursobservation/contour/indexpath)
- [var normalizedPath: CGPath](/documentation/vision/contoursobservation/contour/normalizedpath)
- [var normalizedPoints: [simd_float2]](/documentation/vision/contoursobservation/contour/normalizedpoints)
- [var pointCount: Int](/documentation/vision/contoursobservation/contour/pointcount)
- [var points: [NormalizedPoint]](/documentation/vision/contoursobservation/contour/points)

##### Calculating area and perimeter

- [func calculateArea(useOrientedArea: Bool) -> Double](/documentation/vision/contoursobservation/contour/calculatearea(useorientedarea:))
- [func calculatePerimeter() -> Double](/documentation/vision/contoursobservation/contour/calculateperimeter())

##### Getting the bounding circle

- [func boundingCircle() -> NormalizedCircle](/documentation/vision/contoursobservation/contour/boundingcircle())

##### Getting the approximation

- [func polygonApproximation(epsilon: Float) throws -> ContoursObservation.Contour](/documentation/vision/contoursobservation/contour/polygonapproximation(epsilon:))
- [func contourAtIndex(Int) -> ContoursObservation.Contour?](/documentation/vision/contoursobservation/contouratindex(_:))
- [func countourAtIndexPath(IndexPath) -> ContoursObservation.Contour?](/documentation/vision/contoursobservation/countouratindexpath(_:))

### Configuring a request

- [var contrastAdjustment: Float](/documentation/vision/detectcontoursrequest/contrastadjustment)
- [var contrastPivot: Float?](/documentation/vision/detectcontoursrequest/contrastpivot)
- [var detectsDarkOnLight: Bool](/documentation/vision/detectcontoursrequest/detectsdarkonlight)
- [var maximumImageDimension: Int](/documentation/vision/detectcontoursrequest/maximumimagedimension)

### Getting the revision

- [let revision: DetectContoursRequest.Revision](/documentation/vision/detectcontoursrequest/revision-swift.property)
- [static let supportedRevisions: [DetectContoursRequest.Revision]](/documentation/vision/detectcontoursrequest/supportedrevisions)
- [DetectContoursRequest.Revision](/documentation/vision/detectcontoursrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detectcontoursrequest/revision-swift.enum/revision1)
- [DetectHorizonRequest](/documentation/vision/detecthorizonrequest)

### Creating a request

- [init(DetectHorizonRequest.Revision?)](/documentation/vision/detecthorizonrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [HorizonObservation](/documentation/vision/horizonobservation)

#### Creating an observation

- [init(VNHorizonObservation)](/documentation/vision/horizonobservation/init(_:))

#### Inspecting an observation

- [let angle: Measurement<UnitAngle>](/documentation/vision/horizonobservation/angle)

#### Getting the transform

- [let transform: CGAffineTransform](/documentation/vision/horizonobservation/transform)
- [func transform(for: CGSize) -> CGAffineTransform](/documentation/vision/horizonobservation/transform(for:))

### Getting the revision

- [let revision: DetectHorizonRequest.Revision](/documentation/vision/detecthorizonrequest/revision-swift.property)
- [static let supportedRevisions: [DetectHorizonRequest.Revision]](/documentation/vision/detecthorizonrequest/supportedrevisions)
- [DetectHorizonRequest.Revision](/documentation/vision/detecthorizonrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detecthorizonrequest/revision-swift.enum/revision1)
- [DetectRectanglesRequest](/documentation/vision/detectrectanglesrequest)

### Creating a request

- [init(DetectRectanglesRequest.Revision?)](/documentation/vision/detectrectanglesrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [RectangleObservation](/documentation/vision/rectangleobservation)

#### Creating an observation

- [init(VNRectangleObservation)](/documentation/vision/rectangleobservation/init(_:))
- [init(topLeft: NormalizedPoint, topRight: NormalizedPoint, bottomRight: NormalizedPoint, bottomLeft: NormalizedPoint)](/documentation/vision/rectangleobservation/init(topleft:topright:bottomright:bottomleft:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Configuring a request

- [var maximumAspectRatio: Float](/documentation/vision/detectrectanglesrequest/maximumaspectratio)
- [var maximumObservations: Int](/documentation/vision/detectrectanglesrequest/maximumobservations)
- [var minimumAspectRatio: Float](/documentation/vision/detectrectanglesrequest/minimumaspectratio)
- [var minimumConfidence: Float](/documentation/vision/detectrectanglesrequest/minimumconfidence)
- [var minimumSize: Float](/documentation/vision/detectrectanglesrequest/minimumsize)
- [var quadratureToleranceDegrees: Float](/documentation/vision/detectrectanglesrequest/quadraturetolerancedegrees)

### Getting the revision

- [let revision: DetectRectanglesRequest.Revision](/documentation/vision/detectrectanglesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectRectanglesRequest.Revision]](/documentation/vision/detectrectanglesrequest/supportedrevisions)
- [DetectRectanglesRequest.Revision](/documentation/vision/detectrectanglesrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detectrectanglesrequest/revision-swift.enum/revision1)

## Image quality and saliency analysis

- [Generating high-quality thumbnails from videos](/documentation/vision/generating-thumbnails-from-videos)
- [CalculateImageAestheticsScoresRequest](/documentation/vision/calculateimageaestheticsscoresrequest)

### Creating a request

- [init(CalculateImageAestheticsScoresRequest.Revision?)](/documentation/vision/calculateimageaestheticsscoresrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [ImageAestheticsScoresObservation](/documentation/vision/imageaestheticsscoresobservation)

#### Creating an observation

- [init(VNImageAestheticsScoresObservation)](/documentation/vision/imageaestheticsscoresobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let isUtility: Bool](/documentation/vision/imageaestheticsscoresobservation/isutility)
- [let overallScore: Float](/documentation/vision/imageaestheticsscoresobservation/overallscore)

### Configuring a request

- [var cropAndScaleAction: ImageCropAndScaleAction](/documentation/vision/calculateimageaestheticsscoresrequest/cropandscaleaction)
- [ImageCropAndScaleAction](/documentation/vision/imagecropandscaleaction)

#### Getting the actions

- [case centerCrop](/documentation/vision/imagecropandscaleaction/centercrop)
- [case scaleToFit](/documentation/vision/imagecropandscaleaction/scaletofit)
- [case scaleToFill](/documentation/vision/imagecropandscaleaction/scaletofill)
- [case scaleToFitPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofitplus90ccwrotation)
- [case scaleToFillPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofillplus90ccwrotation)

### Getting the revision

- [let revision: CalculateImageAestheticsScoresRequest.Revision](/documentation/vision/calculateimageaestheticsscoresrequest/revision-swift.property)
- [static let supportedRevisions: [CalculateImageAestheticsScoresRequest.Revision]](/documentation/vision/calculateimageaestheticsscoresrequest/supportedrevisions)
- [CalculateImageAestheticsScoresRequest.Revision](/documentation/vision/calculateimageaestheticsscoresrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/calculateimageaestheticsscoresrequest/revision-swift.enum/revision1)
- [DetectLensSmudgeRequest](/documentation/vision/detectlenssmudgerequest)

### Creating a request

- [init(DetectLensSmudgeRequest.Revision?)](/documentation/vision/detectlenssmudgerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [SmudgeObservation](/documentation/vision/smudgeobservation)

#### Inspecting an observation

- [var description: String](/documentation/vision/smudgeobservation/description)
- [let confidence: Float](/documentation/vision/smudgeobservation/confidence)
- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Configuring a request

- [var cropAndScaleAction: ImageCropAndScaleAction](/documentation/vision/detectlenssmudgerequest/cropandscaleaction)
- [ImageCropAndScaleAction](/documentation/vision/imagecropandscaleaction)

#### Getting the actions

- [case centerCrop](/documentation/vision/imagecropandscaleaction/centercrop)
- [case scaleToFit](/documentation/vision/imagecropandscaleaction/scaletofit)
- [case scaleToFill](/documentation/vision/imagecropandscaleaction/scaletofill)
- [case scaleToFitPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofitplus90ccwrotation)
- [case scaleToFillPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofillplus90ccwrotation)

### Getting the revision

- [let revision: DetectLensSmudgeRequest.Revision](/documentation/vision/detectlenssmudgerequest/revision-swift.property)
- [static var supportedRevisions: [DetectLensSmudgeRequest.Revision]](/documentation/vision/detectlenssmudgerequest/supportedrevisions)
- [DetectLensSmudgeRequest.Revision](/documentation/vision/detectlenssmudgerequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detectlenssmudgerequest/revision-swift.enum/revision1)
- [GenerateAttentionBasedSaliencyImageRequest](/documentation/vision/generateattentionbasedsaliencyimagerequest)

### Creating a request

- [init(GenerateAttentionBasedSaliencyImageRequest.Revision?)](/documentation/vision/generateattentionbasedsaliencyimagerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [SaliencyImageObservation](/documentation/vision/saliencyimageobservation)

#### Creating an observation

- [init?(VNSaliencyImageObservation)](/documentation/vision/saliencyimageobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let heatMap: PixelBufferObservation](/documentation/vision/saliencyimageobservation/heatmap)
- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

##### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

##### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

##### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))
- [let salientObjects: [RectangleObservation]](/documentation/vision/saliencyimageobservation/salientobjects)
- [RectangleObservation](/documentation/vision/rectangleobservation)

##### Creating an observation

- [init(VNRectangleObservation)](/documentation/vision/rectangleobservation/init(_:))
- [init(topLeft: NormalizedPoint, topRight: NormalizedPoint, bottomRight: NormalizedPoint, bottomLeft: NormalizedPoint)](/documentation/vision/rectangleobservation/init(topleft:topright:bottomright:bottomleft:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Getting the revision

- [let revision: GenerateAttentionBasedSaliencyImageRequest.Revision](/documentation/vision/generateattentionbasedsaliencyimagerequest/revision-swift.property)
- [static let supportedRevisions: [GenerateAttentionBasedSaliencyImageRequest.Revision]](/documentation/vision/generateattentionbasedsaliencyimagerequest/supportedrevisions)
- [GenerateAttentionBasedSaliencyImageRequest.Revision](/documentation/vision/generateattentionbasedsaliencyimagerequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/generateattentionbasedsaliencyimagerequest/revision-swift.enum/revision2)
- [GenerateObjectnessBasedSaliencyImageRequest](/documentation/vision/generateobjectnessbasedsaliencyimagerequest)

### Creating a request

- [init(GenerateObjectnessBasedSaliencyImageRequest.Revision?)](/documentation/vision/generateobjectnessbasedsaliencyimagerequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [SaliencyImageObservation](/documentation/vision/saliencyimageobservation)

#### Creating an observation

- [init?(VNSaliencyImageObservation)](/documentation/vision/saliencyimageobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [let heatMap: PixelBufferObservation](/documentation/vision/saliencyimageobservation/heatmap)
- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

##### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

##### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

##### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))
- [let salientObjects: [RectangleObservation]](/documentation/vision/saliencyimageobservation/salientobjects)
- [RectangleObservation](/documentation/vision/rectangleobservation)

##### Creating an observation

- [init(VNRectangleObservation)](/documentation/vision/rectangleobservation/init(_:))
- [init(topLeft: NormalizedPoint, topRight: NormalizedPoint, bottomRight: NormalizedPoint, bottomLeft: NormalizedPoint)](/documentation/vision/rectangleobservation/init(topleft:topright:bottomright:bottomleft:))

##### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

###### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

###### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

###### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

###### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

###### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

###### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

###### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

###### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

###### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

###### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

###### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

###### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

###### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Getting the revision

- [let revision: GenerateObjectnessBasedSaliencyImageRequest.Revision](/documentation/vision/generateobjectnessbasedsaliencyimagerequest/revision-swift.property)
- [static let supportedRevisions: [GenerateObjectnessBasedSaliencyImageRequest.Revision]](/documentation/vision/generateobjectnessbasedsaliencyimagerequest/supportedrevisions)
- [GenerateObjectnessBasedSaliencyImageRequest.Revision](/documentation/vision/generateobjectnessbasedsaliencyimagerequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/generateobjectnessbasedsaliencyimagerequest/revision-swift.enum/revision2)

## Motion and object tracking

- [DetectTrajectoriesRequest](/documentation/vision/detecttrajectoriesrequest)

### Creating a request

- [init(trajectoryLength: Int, DetectTrajectoriesRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/detecttrajectoriesrequest/init(trajectorylength:_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [TrajectoryObservation](/documentation/vision/trajectoryobservation)

#### Creating an observation

- [init(VNTrajectoryObservation)](/documentation/vision/trajectoryobservation/init(_:))

#### Inspecting an observation

- [let detectedPoints: [NormalizedPoint]](/documentation/vision/trajectoryobservation/detectedpoints)
- [let projectedPoints: [NormalizedPoint]](/documentation/vision/trajectoryobservation/projectedpoints)
- [let equationCoefficients: simd_float3](/documentation/vision/trajectoryobservation/equationcoefficients)
- [let movingAverageRadius: CGFloat](/documentation/vision/trajectoryobservation/movingaverageradius)

### Configuring a request

- [var objectMaximumNormalizedRadius: Float](/documentation/vision/detecttrajectoriesrequest/objectmaximumnormalizedradius)
- [var objectMinimumNormalizedRadius: Float](/documentation/vision/detecttrajectoriesrequest/objectminimumnormalizedradius)
- [var targetFrameTime: CMTime](/documentation/vision/detecttrajectoriesrequest/targetframetime)
- [let trajectoryLength: Int](/documentation/vision/detecttrajectoriesrequest/trajectorylength)

### Getting the revision

- [let revision: DetectTrajectoriesRequest.Revision](/documentation/vision/detecttrajectoriesrequest/revision-swift.property)
- [static let supportedRevisions: [DetectTrajectoriesRequest.Revision]](/documentation/vision/detecttrajectoriesrequest/supportedrevisions)
- [DetectTrajectoriesRequest.Revision](/documentation/vision/detecttrajectoriesrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/detecttrajectoriesrequest/revision-swift.enum/revision1)
- [TrackObjectRequest](/documentation/vision/trackobjectrequest)

### Creating a request

- [init(detectedObject: any BoundingBoxProviding & VisionObservation, TrackObjectRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/trackobjectrequest/init(detectedobject:_:frameanalysisspacing:))
- [BoundingBoxProviding](/documentation/vision/boundingboxproviding)

#### Getting the bounding box

- [var boundingBox: NormalizedRect](/documentation/vision/boundingboxproviding/boundingbox)

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [DetectedObjectObservation](/documentation/vision/detectedobjectobservation)

#### Creating an observation

- [init(VNDetectedObjectObservation)](/documentation/vision/detectedobjectobservation/init(_:))
- [init(boundingBox: NormalizedRect)](/documentation/vision/detectedobjectobservation/init(boundingbox:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Configuring a request

- [let inputObservation: any BoundingBoxProviding & VisionObservation](/documentation/vision/trackobjectrequest/inputobservation)

### Getting the revision

- [let revision: TrackObjectRequest.Revision](/documentation/vision/trackobjectrequest/revision-swift.property)
- [static let supportedRevisions: [TrackObjectRequest.Revision]](/documentation/vision/trackobjectrequest/supportedrevisions)
- [TrackObjectRequest.Revision](/documentation/vision/trackobjectrequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/trackobjectrequest/revision-swift.enum/revision2)
- [TrackOpticalFlowRequest](/documentation/vision/trackopticalflowrequest)

### Creating a request

- [init(TrackOpticalFlowRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/trackopticalflowrequest/init(_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [OpticalFlowObservation](/documentation/vision/opticalflowobservation)

#### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/opticalflowobservation/init(_:))

#### Inspecting an observation

- [var pixelFormat: OSType](/documentation/vision/opticalflowobservation/pixelformat)
- [var size: CGSize](/documentation/vision/opticalflowobservation/size)

#### Getting the optical flow

- [func flow(at: NormalizedPoint) -> (Float, Float)](/documentation/vision/opticalflowobservation/flow(at:))

#### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/opticalflowobservation/withunsafepointer(_:))

### Configuring a request

- [var computationAccuracy: TrackOpticalFlowRequest.ComputationAccuracy](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.property)
- [TrackOpticalFlowRequest.ComputationAccuracy](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.enum)

#### Getting the accuracies

- [case high](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.enum/high)
- [case low](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.enum/low)
- [case medium](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.enum/medium)
- [case veryHigh](/documentation/vision/trackopticalflowrequest/computationaccuracy-swift.enum/veryhigh)
- [var outputPixelFormatType: OSType](/documentation/vision/trackopticalflowrequest/outputpixelformattype)
- [var supportedOutputPixelFormatTypes: [OSType]](/documentation/vision/trackopticalflowrequest/supportedoutputpixelformattypes)

### Getting the revision

- [let revision: TrackOpticalFlowRequest.Revision](/documentation/vision/trackopticalflowrequest/revision-swift.property)
- [static let supportedRevisions: [TrackOpticalFlowRequest.Revision]](/documentation/vision/trackopticalflowrequest/supportedrevisions)
- [TrackOpticalFlowRequest.Revision](/documentation/vision/trackopticalflowrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/trackopticalflowrequest/revision-swift.enum/revision1)
- [TrackRectangleRequest](/documentation/vision/trackrectanglerequest)

### Creating a request

- [init(detectedRectangle: any QuadrilateralProviding & VisionObservation, TrackRectangleRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/trackrectanglerequest/init(detectedrectangle:_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [RectangleObservation](/documentation/vision/rectangleobservation)

#### Creating an observation

- [init(VNRectangleObservation)](/documentation/vision/rectangleobservation/init(_:))
- [init(topLeft: NormalizedPoint, topRight: NormalizedPoint, bottomRight: NormalizedPoint, bottomLeft: NormalizedPoint)](/documentation/vision/rectangleobservation/init(topleft:topright:bottomright:bottomleft:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

### Configuring a request

- [let inputObservation: any QuadrilateralProviding & VisionObservation](/documentation/vision/trackrectanglerequest/inputobservation)
- [QuadrilateralProviding](/documentation/vision/quadrilateralproviding)

#### Getting the normalized points

- [var bottomLeft: NormalizedPoint](/documentation/vision/quadrilateralproviding/bottomleft)
- [var bottomRight: NormalizedPoint](/documentation/vision/quadrilateralproviding/bottomright)
- [var topLeft: NormalizedPoint](/documentation/vision/quadrilateralproviding/topleft)
- [var topRight: NormalizedPoint](/documentation/vision/quadrilateralproviding/topright)
- [var trackingLevel: TrackRectangleRequest.TrackingLevel](/documentation/vision/trackrectanglerequest/trackinglevel-swift.property)
- [TrackRectangleRequest.TrackingLevel](/documentation/vision/trackrectanglerequest/trackinglevel-swift.enum)

#### Getting the tracking levels

- [case accurate](/documentation/vision/trackrectanglerequest/trackinglevel-swift.enum/accurate)
- [case fast](/documentation/vision/trackrectanglerequest/trackinglevel-swift.enum/fast)

### Getting the revision

- [let revision: TrackRectangleRequest.Revision](/documentation/vision/trackrectanglerequest/revision-swift.property)
- [static let supportedRevisions: [TrackRectangleRequest.Revision]](/documentation/vision/trackrectanglerequest/supportedrevisions)
- [TrackRectangleRequest.Revision](/documentation/vision/trackrectanglerequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/trackrectanglerequest/revision-swift.enum/revision1)

## Image registration and comparison

- [GenerateImageFeaturePrintRequest](/documentation/vision/generateimagefeatureprintrequest)

### Creating a request

- [init(GenerateImageFeaturePrintRequest.Revision?)](/documentation/vision/generateimagefeatureprintrequest/init(_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [FeaturePrintObservation](/documentation/vision/featureprintobservation)

#### Creating an observation

- [init(VNFeaturePrintObservation)](/documentation/vision/featureprintobservation/init(_:))

#### Inspecting an observation

- [let data: Data](/documentation/vision/featureprintobservation/data)
- [let elementCount: Int](/documentation/vision/featureprintobservation/elementcount)
- [let elementType: ElementType](/documentation/vision/featureprintobservation/elementtype)
- [ElementType](/documentation/vision/elementtype)

##### Getting the element types

- [case double](/documentation/vision/elementtype/double)
- [case float](/documentation/vision/elementtype/float)

#### Getting the distance

- [func distance(to: FeaturePrintObservation) throws -> Double](/documentation/vision/featureprintobservation/distance(to:))

### Configuring a request

- [var cropAndScaleAction: ImageCropAndScaleAction](/documentation/vision/generateimagefeatureprintrequest/cropandscaleaction)
- [ImageCropAndScaleAction](/documentation/vision/imagecropandscaleaction)

#### Getting the actions

- [case centerCrop](/documentation/vision/imagecropandscaleaction/centercrop)
- [case scaleToFit](/documentation/vision/imagecropandscaleaction/scaletofit)
- [case scaleToFill](/documentation/vision/imagecropandscaleaction/scaletofill)
- [case scaleToFitPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofitplus90ccwrotation)
- [case scaleToFillPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofillplus90ccwrotation)

### Getting the revision

- [let revision: GenerateImageFeaturePrintRequest.Revision](/documentation/vision/generateimagefeatureprintrequest/revision-swift.property)
- [static let supportedRevisions: [GenerateImageFeaturePrintRequest.Revision]](/documentation/vision/generateimagefeatureprintrequest/supportedrevisions)
- [GenerateImageFeaturePrintRequest.Revision](/documentation/vision/generateimagefeatureprintrequest/revision-swift.enum)

#### Getting the revision

- [case revision2](/documentation/vision/generateimagefeatureprintrequest/revision-swift.enum/revision2)
- [TrackHomographicImageRegistrationRequest](/documentation/vision/trackhomographicimageregistrationrequest)

### Creating a request

- [init(TrackHomographicImageRegistrationRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/trackhomographicimageregistrationrequest/init(_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [ImageHomographicAlignmentObservation](/documentation/vision/imagehomographicalignmentobservation)

#### Creating an observation

- [init(VNImageHomographicAlignmentObservation)](/documentation/vision/imagehomographicalignmentobservation/init(_:))

#### Inspecting an observation

- [let warpTransform: matrix_float3x3](/documentation/vision/imagehomographicalignmentobservation/warptransform)

#### Applying a transform

- [func applyTransform(to: CIImage) -> CIImage](/documentation/vision/imagehomographicalignmentobservation/applytransform(to:))

### Getting the revision

- [let revision: TrackHomographicImageRegistrationRequest.Revision](/documentation/vision/trackhomographicimageregistrationrequest/revision-swift.property)
- [static let supportedRevisions: [TrackHomographicImageRegistrationRequest.Revision]](/documentation/vision/trackhomographicimageregistrationrequest/supportedrevisions)
- [TrackHomographicImageRegistrationRequest.Revision](/documentation/vision/trackhomographicimageregistrationrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/trackhomographicimageregistrationrequest/revision-swift.enum/revision1)
- [TrackTranslationalImageRegistrationRequest](/documentation/vision/tracktranslationalimageregistrationrequest)

### Creating a request

- [init(TrackTranslationalImageRegistrationRequest.Revision?, frameAnalysisSpacing: CMTime?)](/documentation/vision/tracktranslationalimageregistrationrequest/init(_:frameanalysisspacing:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [ImageTranslationAlignmentObservation](/documentation/vision/imagetranslationalignmentobservation)

#### Creating an observation

- [init(VNImageTranslationAlignmentObservation)](/documentation/vision/imagetranslationalignmentobservation/init(_:))

#### Inspecting an observation

- [let alignmentTransform: CGAffineTransform](/documentation/vision/imagetranslationalignmentobservation/alignmenttransform)

#### Applying a transform

- [func applyTransform(to: CIImage) -> CIImage](/documentation/vision/imagetranslationalignmentobservation/applytransform(to:))

### Configuring a request

- [ComputeStage](/documentation/vision/computestage)

#### Getting the compute stages

- [case main](/documentation/vision/computestage/main)
- [case postProcessing](/documentation/vision/computestage/postprocessing)

### Getting the revision

- [let revision: TrackTranslationalImageRegistrationRequest.Revision](/documentation/vision/tracktranslationalimageregistrationrequest/revision-swift.property)
- [static let supportedRevisions: [TrackTranslationalImageRegistrationRequest.Revision]](/documentation/vision/tracktranslationalimageregistrationrequest/supportedrevisions)
- [TrackTranslationalImageRegistrationRequest.Revision](/documentation/vision/tracktranslationalimageregistrationrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/tracktranslationalimageregistrationrequest/revision-swift.enum/revision1)

## Custom Core ML integration

- [CoreMLRequest](/documentation/vision/coremlrequest)

### Creating a request

- [init(model: CoreMLModelContainer, CoreMLRequest.Revision?)](/documentation/vision/coremlrequest/init(model:_:))

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)

### Understanding the result

- [PixelBufferObservation](/documentation/vision/pixelbufferobservation)

#### Creating an observation

- [init?(VNPixelBufferObservation)](/documentation/vision/pixelbufferobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var cgImage: CGImage](/documentation/vision/pixelbufferobservation/cgimage)
- [var pixelFormat: OSType](/documentation/vision/pixelbufferobservation/pixelformat)
- [var size: CGSize](/documentation/vision/pixelbufferobservation/size)

#### Getting pixel data

- [func pixel(at: NormalizedPoint) -> Float](/documentation/vision/pixelbufferobservation/pixel(at:))

#### Accessing the memory

- [func withUnsafePointer<R>((UnsafeRawPointer) -> R) -> R](/documentation/vision/pixelbufferobservation/withunsafepointer(_:))
- [ClassificationObservation](/documentation/vision/classificationobservation)

#### Creating an observation

- [init(VNClassificationObservation)](/documentation/vision/classificationobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var hasPrecisionRecallCurve: Bool](/documentation/vision/classificationobservation/hasprecisionrecallcurve)
- [let identifier: String](/documentation/vision/classificationobservation/identifier)

#### Determining precision and recall

- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/classificationobservation/hasminimumrecall(_:forprecision:))
- [CoreMLFeatureValueObservation](/documentation/vision/coremlfeaturevalueobservation)

#### Creating an observation

- [init?(VNCoreMLFeatureValueObservation)](/documentation/vision/coremlfeaturevalueobservation/init(_:))

#### Inspecting an observation

- [RequestDescriptor](/documentation/vision/requestdescriptor)

##### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

##### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

##### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

##### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

##### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

##### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

##### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

##### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

##### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

##### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

##### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

##### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

##### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))

#### Getting the feature name and value

- [let featureName: String](/documentation/vision/coremlfeaturevalueobservation/featurename)
- [let featureValue: MLSendableFeatureValue](/documentation/vision/coremlfeaturevalueobservation/featurevalue)

### Configuring a request

- [var supportedIdentifiers: [String]?](/documentation/vision/coremlrequest/supportedidentifiers)
- [let modelContainer: CoreMLModelContainer](/documentation/vision/coremlrequest/modelcontainer)
- [CoreMLModelContainer](/documentation/vision/coremlmodelcontainer)

#### Creating a model container

- [init(model: MLModel, featureProvider: (any MLFeatureProvider)?) throws](/documentation/vision/coremlmodelcontainer/init(model:featureprovider:))

#### Getting the feature name

- [var inputImageFeatureName: String](/documentation/vision/coremlmodelcontainer/inputimagefeaturename)
- [ComputeStage](/documentation/vision/computestage)

#### Getting the compute stages

- [case main](/documentation/vision/computestage/main)
- [case postProcessing](/documentation/vision/computestage/postprocessing)
- [var cropAndScaleAction: ImageCropAndScaleAction](/documentation/vision/coremlrequest/cropandscaleaction)
- [ImageCropAndScaleAction](/documentation/vision/imagecropandscaleaction)

#### Getting the actions

- [case centerCrop](/documentation/vision/imagecropandscaleaction/centercrop)
- [case scaleToFit](/documentation/vision/imagecropandscaleaction/scaletofit)
- [case scaleToFill](/documentation/vision/imagecropandscaleaction/scaletofill)
- [case scaleToFitPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofitplus90ccwrotation)
- [case scaleToFillPlus90CCWRotation](/documentation/vision/imagecropandscaleaction/scaletofillplus90ccwrotation)

### Getting the revision

- [let revision: CoreMLRequest.Revision](/documentation/vision/coremlrequest/revision-swift.property)
- [static let supportedRevisions: [CoreMLRequest.Revision]](/documentation/vision/coremlrequest/supportedrevisions)
- [CoreMLRequest.Revision](/documentation/vision/coremlrequest/revision-swift.enum)

#### Getting the revision

- [case revision1](/documentation/vision/coremlrequest/revision-swift.enum/revision1)

## Protocols

- [ImageProcessingRequest](/documentation/vision/imageprocessingrequest)

### Setting the region

- [var regionOfInterest: NormalizedRect](/documentation/vision/imageprocessingrequest/regionofinterest)

### Performing a request

- [func perform(on: URL, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-80bya)
- [func perform(on: Data, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3f3f1)
- [func perform(on: CGImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-qxxx)
- [func perform(on: CVPixelBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-xspx)
- [func perform(on: CMSampleBuffer, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-3hddl)
- [func perform(on: CIImage, orientation: CGImagePropertyOrientation?) async throws -> Self.Result](/documentation/vision/imageprocessingrequest/perform(on:orientation:)-85ex1)
- [PoseProviding](/documentation/vision/poseproviding)

### Getting the joints

- [func joint(for: Self.PoseJointName) -> Joint?](/documentation/vision/poseproviding/joint(for:))
- [func allJoints(in: Self.PoseJointsGroupName?) -> [Self.PoseJointName : Joint]](/documentation/vision/poseproviding/alljoints(in:))

### Getting the joint names

- [var availableJointNames: [Self.PoseJointName]](/documentation/vision/poseproviding/availablejointnames)
- [PoseJointName](/documentation/vision/poseproviding/posejointname)

### Getting the joint group names

- [var availableJointsGroupNames: [Self.PoseJointsGroupName]](/documentation/vision/poseproviding/availablejointsgroupnames)
- [PoseJointsGroupName](/documentation/vision/poseproviding/posejointsgroupname)
- [StatefulRequest](/documentation/vision/statefulrequest)

### Inspecting the request

- [var frameAnalysisSpacing: CMTime](/documentation/vision/statefulrequest/frameanalysisspacing)
- [var minimumLatencyFrameCount: Int](/documentation/vision/statefulrequest/minimumlatencyframecount)

### Comparing the request

- [static func == (Self, Self) -> Bool](/documentation/vision/statefulrequest/==(_:_:))

### Hashing the request

- [func hash(into: inout Hasher)](/documentation/vision/statefulrequest/hash(into:))

### Default Implementations

- [Equatable Implementations](/documentation/vision/statefulrequest/equatable-implementations)

#### Operators

- [static func == (Self, Self) -> Bool](/documentation/vision/statefulrequest/==(_:_:))
- [Hashable Implementations](/documentation/vision/statefulrequest/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/vision/statefulrequest/hash(into:))
- [TargetedRequest](/documentation/vision/targetedrequest)
- [VisionObservation](/documentation/vision/visionobservation)

### Inspecting an observation

- [var uuid: UUID](/documentation/vision/visionobservation/uuid)
- [var confidence: Float](/documentation/vision/visionobservation/confidence)
- [var description: String](/documentation/vision/visionobservation/description)
- [var originatingRequestDescriptor: RequestDescriptor?](/documentation/vision/visionobservation/originatingrequestdescriptor)
- [RequestDescriptor](/documentation/vision/requestdescriptor)

#### Getting the still-image descriptor

- [case classifyImageRequest(ClassifyImageRequest.Revision)](/documentation/vision/requestdescriptor/classifyimagerequest(_:))
- [case detectLensSmudgeRequest(DetectLensSmudgeRequest.Revision)](/documentation/vision/requestdescriptor/detectlenssmudgerequest(_:))

#### Getting the image sequence descriptor

- [case detectDocumentSegmentationRequest(DetectDocumentSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/detectdocumentsegmentationrequest(_:))
- [case recognizeDocumentsRequest(RecognizeDocumentsRequest.Revision)](/documentation/vision/requestdescriptor/recognizedocumentsrequest(_:))
- [case generatePersonInstanceMaskRequest(GeneratePersonInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generatepersoninstancemaskrequest(_:))
- [case generatePersonSegmentationRequest(GeneratePersonSegmentationRequest.Revision)](/documentation/vision/requestdescriptor/generatepersonsegmentationrequest(_:))

#### Getting the image aesthetics descriptor

- [case calculateImageAestheticsScoresRequest(CalculateImageAestheticsScoresRequest.Revision)](/documentation/vision/requestdescriptor/calculateimageaestheticsscoresrequest(_:))

#### Getting the saliency descriptor

- [case generateAttentionBasedSaliencyImageRequest(GenerateAttentionBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateattentionbasedsaliencyimagerequest(_:))
- [case generateObjectnessBasedSaliencyImageRequest(GenerateObjectnessBasedSaliencyImageRequest.Revision)](/documentation/vision/requestdescriptor/generateobjectnessbasedsaliencyimagerequest(_:))

#### Getting the object-tracking descriptor

- [case trackObjectRequest(TrackObjectRequest.Revision)](/documentation/vision/requestdescriptor/trackobjectrequest(_:))
- [case trackRectangleRequest(TrackRectangleRequest.Revision)](/documentation/vision/requestdescriptor/trackrectanglerequest(_:))

#### Getting the face and body detection descriptor

- [case detectFaceCaptureQualityRequest(DetectFaceCaptureQualityRequest.Revision)](/documentation/vision/requestdescriptor/detectfacecapturequalityrequest(_:))
- [case detectFaceLandmarksRequest(DetectFaceLandmarksRequest.Revision)](/documentation/vision/requestdescriptor/detectfacelandmarksrequest(_:))
- [case detectFaceRectanglesRequest(DetectFaceRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectfacerectanglesrequest(_:))
- [case detectHumanRectanglesRequest(DetectHumanRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanrectanglesrequest(_:))

#### Getting the body and hand pose detection descriptor

- [case detectHumanBodyPoseRequest(DetectHumanBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodyposerequest(_:))
- [case detectHumanHandPoseRequest(DetectHumanHandPoseRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanhandposerequest(_:))
- [case detectHumanBodyPose3DRequest(DetectHumanBodyPose3DRequest.Revision)](/documentation/vision/requestdescriptor/detecthumanbodypose3drequest(_:))

#### Getting the animal detection descriptor

- [case detectAnimalBodyPoseRequest(DetectAnimalBodyPoseRequest.Revision)](/documentation/vision/requestdescriptor/detectanimalbodyposerequest(_:))
- [case recognizeAnimalsRequest(RecognizeAnimalsRequest.Revision)](/documentation/vision/requestdescriptor/recognizeanimalsrequest(_:))

#### Getting the text descriptor

- [case detectTextRectanglesRequest(DetectTextRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detecttextrectanglesrequest(_:))
- [case recognizeTextRequest(RecognizeTextRequest.Revision)](/documentation/vision/requestdescriptor/recognizetextrequest(_:))

#### Getting the image alignment, feature print, and background removal descriptor

- [case trackTranslationalImageRegistrationRequest(TrackTranslationalImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/tracktranslationalimageregistrationrequest(_:))
- [case trackHomographicImageRegistrationRequest(TrackHomographicImageRegistrationRequest.Revision)](/documentation/vision/requestdescriptor/trackhomographicimageregistrationrequest(_:))
- [case generateForegroundInstanceMaskRequest(GenerateForegroundInstanceMaskRequest.Revision)](/documentation/vision/requestdescriptor/generateforegroundinstancemaskrequest(_:))
- [case generateImageFeaturePrintRequest(GenerateImageFeaturePrintRequest.Revision)](/documentation/vision/requestdescriptor/generateimagefeatureprintrequest(_:))

#### Getting the trajectory, contour, and horizon detection descriptor

- [case detectTrajectoriesRequest(DetectTrajectoriesRequest.Revision)](/documentation/vision/requestdescriptor/detecttrajectoriesrequest(_:))
- [case detectContoursRequest(DetectContoursRequest.Revision)](/documentation/vision/requestdescriptor/detectcontoursrequest(_:))
- [case detectHorizonRequest(DetectHorizonRequest.Revision)](/documentation/vision/requestdescriptor/detecthorizonrequest(_:))

#### Getting the optical flow, rectangle and barcode detection descriptor

- [case trackOpticalFlowRequest(TrackOpticalFlowRequest.Revision)](/documentation/vision/requestdescriptor/trackopticalflowrequest(_:))
- [case detectRectanglesRequest(DetectRectanglesRequest.Revision)](/documentation/vision/requestdescriptor/detectrectanglesrequest(_:))
- [case detectBarcodesRequest(DetectBarcodesRequest.Revision)](/documentation/vision/requestdescriptor/detectbarcodesrequest(_:))

#### Getting the machine learning image-analysis descriptor

- [case coreMLRequest(CoreMLRequest.Revision)](/documentation/vision/requestdescriptor/coremlrequest(_:))
- [var timeRange: CMTimeRange?](/documentation/vision/visionobservation/timerange)

### Hashing the observation

- [func hash(into: inout Hasher)](/documentation/vision/visionobservation/hash(into:))

### Default Implementations

- [Hashable Implementations](/documentation/vision/visionobservation/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/vision/visionobservation/hash(into:)-8aqw6)
- [VisionRequest](/documentation/vision/visionrequest)

### Getting the compute device

- [func computeDevice(for: ComputeStage) -> MLComputeDevice?](/documentation/vision/visionrequest/computedevice(for:))
- [var supportedComputeStageDevices: [ComputeStage : [MLComputeDevice]]](/documentation/vision/visionrequest/supportedcomputestagedevices)
- [ComputeStage](/documentation/vision/computestage)

#### Getting the compute stages

- [case main](/documentation/vision/computestage/main)
- [case postProcessing](/documentation/vision/computestage/postprocessing)

### Setting the compute device

- [func setComputeDevice(MLComputeDevice?, for: ComputeStage)](/documentation/vision/visionrequest/setcomputedevice(_:for:))

### Getting the descriptor

- [var descriptor: RequestDescriptor](/documentation/vision/visionrequest/descriptor)

### Performing the request

- [Result](/documentation/vision/visionrequest/result)
- [VisionResult](/documentation/vision/visionresult)

#### Getting the still-image result

- [case classifyImage(ClassifyImageRequest, [ClassificationObservation])](/documentation/vision/visionresult/classifyimage(_:_:))

#### Getting the image sequence result

- [case generatePersonInstanceMask(GeneratePersonInstanceMaskRequest, InstanceMaskObservation?)](/documentation/vision/visionresult/generatepersoninstancemask(_:_:))
- [case generatePersonSegmentation(GeneratePersonSegmentationRequest, PixelBufferObservation)](/documentation/vision/visionresult/generatepersonsegmentation(_:_:))
- [case detectDocumentSegmentation(DetectDocumentSegmentationRequest, DetectedDocumentObservation?)](/documentation/vision/visionresult/detectdocumentsegmentation(_:_:))
- [case recognizeDocuments(RecognizeDocumentsRequest, [DocumentObservation])](/documentation/vision/visionresult/recognizedocuments(_:_:))

#### Getting the image aesthetics and lens smudge result

- [case calculateImageAestheticsScores(CalculateImageAestheticsScoresRequest, ImageAestheticsScoresObservation)](/documentation/vision/visionresult/calculateimageaestheticsscores(_:_:))
- [case detectLensSmudge(DetectLensSmudgeRequest, SmudgeObservation)](/documentation/vision/visionresult/detectlenssmudge(_:_:))

#### Getting the saliency result

- [case generateObjectnessBasedSaliencyImage(GenerateObjectnessBasedSaliencyImageRequest, SaliencyImageObservation)](/documentation/vision/visionresult/generateobjectnessbasedsaliencyimage(_:_:))
- [case generateAttentionBasedSaliencyImage(GenerateAttentionBasedSaliencyImageRequest, SaliencyImageObservation)](/documentation/vision/visionresult/generateattentionbasedsaliencyimage(_:_:))

#### Getting the object-tracking result

- [case trackRectangle(TrackRectangleRequest, RectangleObservation?)](/documentation/vision/visionresult/trackrectangle(_:_:))
- [case trackObject(TrackObjectRequest, DetectedObjectObservation?)](/documentation/vision/visionresult/trackobject(_:_:))

#### Getting the face and body detection result

- [case detectFaceCaptureQuality(DetectFaceCaptureQualityRequest, [FaceObservation])](/documentation/vision/visionresult/detectfacecapturequality(_:_:))
- [case detectFaceLandmarks(DetectFaceLandmarksRequest, [FaceObservation])](/documentation/vision/visionresult/detectfacelandmarks(_:_:))
- [case detectFaceRectangles(DetectFaceRectanglesRequest, [FaceObservation])](/documentation/vision/visionresult/detectfacerectangles(_:_:))
- [case detectHumanRectangles(DetectHumanRectanglesRequest, [HumanObservation])](/documentation/vision/visionresult/detecthumanrectangles(_:_:))

#### Getting the body and hand pose detection result

- [case detectHumanBodyPose(DetectHumanBodyPoseRequest, [HumanBodyPoseObservation])](/documentation/vision/visionresult/detecthumanbodypose(_:_:))
- [case detectHumanHandPose(DetectHumanHandPoseRequest, [HumanHandPoseObservation])](/documentation/vision/visionresult/detecthumanhandpose(_:_:))
- [case detectHumanBodyPose3D(DetectHumanBodyPose3DRequest, [HumanBodyPose3DObservation])](/documentation/vision/visionresult/detecthumanbodypose3d(_:_:))

#### Getting the animal detection result

- [case recognizeAnimals(RecognizeAnimalsRequest, [RecognizedObjectObservation])](/documentation/vision/visionresult/recognizeanimals(_:_:))
- [case detectAnimalBodyPose(DetectAnimalBodyPoseRequest, [AnimalBodyPoseObservation])](/documentation/vision/visionresult/detectanimalbodypose(_:_:))

#### Getting the text result

- [case detectTextRectangles(DetectTextRectanglesRequest, [TextObservation])](/documentation/vision/visionresult/detecttextrectangles(_:_:))
- [case recognizeText(RecognizeTextRequest, [RecognizedTextObservation])](/documentation/vision/visionresult/recognizetext(_:_:))

#### Getting the image alignment, feature print, and background removal result

- [case trackTranslationalImageRegistration(TrackTranslationalImageRegistrationRequest, ImageTranslationAlignmentObservation)](/documentation/vision/visionresult/tracktranslationalimageregistration(_:_:))
- [case trackHomographicImageRegistration(TrackHomographicImageRegistrationRequest, ImageHomographicAlignmentObservation)](/documentation/vision/visionresult/trackhomographicimageregistration(_:_:))
- [case generateForegroundInstanceMask(GenerateForegroundInstanceMaskRequest, InstanceMaskObservation?)](/documentation/vision/visionresult/generateforegroundinstancemask(_:_:))
- [case generateImageFeaturePrint(GenerateImageFeaturePrintRequest, FeaturePrintObservation)](/documentation/vision/visionresult/generateimagefeatureprint(_:_:))

#### Getting the trajectory, contour, and horizon detection result

- [case detectTrajectories(DetectTrajectoriesRequest, [TrajectoryObservation])](/documentation/vision/visionresult/detecttrajectories(_:_:))
- [case detectContours(DetectContoursRequest, ContoursObservation)](/documentation/vision/visionresult/detectcontours(_:_:))
- [case detectHorizon(DetectHorizonRequest, HorizonObservation?)](/documentation/vision/visionresult/detecthorizon(_:_:))

#### Getting the optical flow, rectangle and barcode detection result

- [case trackOpticalFlow(TrackOpticalFlowRequest, OpticalFlowObservation?)](/documentation/vision/visionresult/trackopticalflow(_:_:))
- [case detectRectangles(DetectRectanglesRequest, [RectangleObservation])](/documentation/vision/visionresult/detectrectangles(_:_:))
- [case detectBarcodes(DetectBarcodesRequest, [BarcodeObservation])](/documentation/vision/visionresult/detectbarcodes(_:_:))

#### Getting the machine learning image-analysis result

- [case coreML(CoreMLRequest, [any VisionObservation])](/documentation/vision/visionresult/coreml(_:_:))

#### Getting the error result

- [case error(any VisionRequest, any Error)](/documentation/vision/visionresult/error(_:_:))

### Default Implementations

- [CustomStringConvertible Implementations](/documentation/vision/visionrequest/customstringconvertible-implementations)

#### Instance Properties

- [var description: String](/documentation/vision/visionrequest/description)

## Request handlers

- [ImageRequestHandler](/documentation/vision/imagerequesthandler)

### Creating a request handler

- [convenience init(URL, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:orientation:)-6imw8)
- [convenience init(Data, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:orientation:)-8cwes)
- [convenience init(CGImage, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:orientation:)-8nodt)
- [convenience init(CVPixelBuffer, depthData: AVDepthData?, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:depthdata:orientation:)-3ebxg)
- [convenience init(CMSampleBuffer, depthData: AVDepthData?, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:depthdata:orientation:)-5itte)
- [convenience init(CIImage, orientation: CGImagePropertyOrientation?)](/documentation/vision/imagerequesthandler/init(_:orientation:)-2hvfr)

### Performing the request

- [func perform<each T>(repeat each T) async throws -> (repeat (each T).Result)](/documentation/vision/imagerequesthandler/perform(_:)-l6er)
- [func perform<T>(T) async throws -> T.Result](/documentation/vision/imagerequesthandler/perform(_:)-7b6g5)
- [func performAll(some Collection<any VisionRequest>) -> some AsyncSequence<VisionResult, Never>
](/documentation/vision/imagerequesthandler/performall(_:))
- [TargetedImageRequestHandler](/documentation/vision/targetedimagerequesthandler)

### Creating a request handler

- [convenience init(sourceURL: URL, targetURL: URL, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(sourceurl:targeturl:orientation:))
- [convenience init(source: Data, target: Data, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(source:target:orientation:)-4wr1c)
- [convenience init(source: CGImage, target: CGImage, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(source:target:orientation:)-66ft9)
- [convenience init(source: CVPixelBuffer, target: CVPixelBuffer, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(source:target:orientation:)-64lxw)
- [convenience init(source: CMSampleBuffer, target: CMSampleBuffer, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(source:target:orientation:)-9u6ta)
- [convenience init(source: CIImage, target: CIImage, orientation: CGImagePropertyOrientation?)](/documentation/vision/targetedimagerequesthandler/init(source:target:orientation:)-1nk14)

### Performing the request

- [func perform<each T>(repeat each T) async throws -> (repeat (each T).Result)](/documentation/vision/targetedimagerequesthandler/perform(_:)-1i4di)
- [func perform<T>(T) async throws -> T.Result](/documentation/vision/targetedimagerequesthandler/perform(_:)-2r0k8)
- [func performAll(some Collection<any TargetedRequest>) -> some AsyncSequence<VisionResult, Never>
](/documentation/vision/targetedimagerequesthandler/performall(_:))
- [VideoProcessor](/documentation/vision/videoprocessor)

### Creating a video processor

- [init(URL)](/documentation/vision/videoprocessor/init(_:))

### Adding and removing a request

- [func addRequest<T>(T, cadence: VideoProcessor.Cadence?) async throws -> some AsyncSequence<T.Result, any Error>
](/documentation/vision/videoprocessor/addrequest(_:cadence:))
- [VideoProcessor.Cadence](/documentation/vision/videoprocessor/cadence)

#### Getting the intervals

- [case timeInterval(CMTime)](/documentation/vision/videoprocessor/cadence/timeinterval(_:))
- [case frameInterval(Int)](/documentation/vision/videoprocessor/cadence/frameinterval(_:))
- [func removeRequest(any VisionRequest) async -> Bool](/documentation/vision/videoprocessor/removerequest(_:))

### Starting the analysis

- [func startAnalysis(of: CMTimeRange?)](/documentation/vision/videoprocessor/startanalysis(of:))

### Cancelling the analysis

- [func cancel() async](/documentation/vision/videoprocessor/cancel())

## Image locations and regions

- [NormalizedPoint](/documentation/vision/normalizedpoint)

### Creating a normalized point

- [init(x: CGFloat, y: CGFloat)](/documentation/vision/normalizedpoint/init(x:y:))
- [init(normalizedPoint: CGPoint)](/documentation/vision/normalizedpoint/init(normalizedpoint:))
- [init(imagePoint: CGPoint, in: CGSize)](/documentation/vision/normalizedpoint/init(imagepoint:in:))
- [init(imagePoint: CGPoint, in: CGSize, normalizedTo: NormalizedRect)](/documentation/vision/normalizedpoint/init(imagepoint:in:normalizedto:))
- [static var zero: NormalizedPoint](/documentation/vision/normalizedpoint/zero)

### Inspecting a normalized point

- [let cgPoint: CGPoint](/documentation/vision/normalizedpoint/cgpoint)
- [var x: CGFloat](/documentation/vision/normalizedpoint/x)
- [var y: CGFloat](/documentation/vision/normalizedpoint/y)

### Converting points

- [func toImageCoordinates(from: NormalizedRect, imageSize: CGSize, origin: CoordinateOrigin) -> CGPoint](/documentation/vision/normalizedpoint/toimagecoordinates(from:imagesize:origin:))
- [func toImageCoordinates(CGSize, origin: CoordinateOrigin) -> CGPoint](/documentation/vision/normalizedpoint/toimagecoordinates(_:origin:))

### Flipping a normalized point

- [func verticallyFlipped() -> NormalizedPoint](/documentation/vision/normalizedpoint/verticallyflipped())
- [NormalizedRect](/documentation/vision/normalizedrect)

### Creating a normalized rectangle

- [init(x: CGFloat, y: CGFloat, width: CGFloat, height: CGFloat)](/documentation/vision/normalizedrect/init(x:y:width:height:))
- [init(imageRect: CGRect, in: CGSize)](/documentation/vision/normalizedrect/init(imagerect:in:))
- [init(imageRect: CGRect, in: CGSize, normalizedTo: NormalizedRect)](/documentation/vision/normalizedrect/init(imagerect:in:normalizedto:))
- [init(normalizedRect: CGRect)](/documentation/vision/normalizedrect/init(normalizedrect:))
- [static var fullImage: NormalizedRect](/documentation/vision/normalizedrect/fullimage)

### Inspecting a normalized rectangle

- [let cgRect: CGRect](/documentation/vision/normalizedrect/cgrect)
- [var origin: CGPoint](/documentation/vision/normalizedrect/origin)
- [var width: CGFloat](/documentation/vision/normalizedrect/width)
- [var height: CGFloat](/documentation/vision/normalizedrect/height)

### Converting rectangles

- [func toImageCoordinates(CGSize, origin: CoordinateOrigin) -> CGRect](/documentation/vision/normalizedrect/toimagecoordinates(_:origin:))
- [func toImageCoordinates(from: NormalizedRect, imageSize: CGSize, origin: CoordinateOrigin) -> CGRect](/documentation/vision/normalizedrect/toimagecoordinates(from:imagesize:origin:))

### Flipping a normalized rectangle

- [func verticallyFlipped() -> NormalizedRect](/documentation/vision/normalizedrect/verticallyflipped())
- [NormalizedRegion](/documentation/vision/normalizedregion)
- [NormalizedCircle](/documentation/vision/normalizedcircle)

### Creating a normalized circle

- [init(center: NormalizedPoint, radius: CGFloat)](/documentation/vision/normalizedcircle/init(center:radius:))
- [static var zero: NormalizedCircle](/documentation/vision/normalizedcircle/zero)

### Inspecting a normalized circle

- [let center: NormalizedPoint](/documentation/vision/normalizedcircle/center)
- [let radius: CGFloat](/documentation/vision/normalizedcircle/radius)

### Determining whether the circle contains a point

- [func contains(NormalizedPoint) -> Bool](/documentation/vision/normalizedcircle/contains(_:))
- [func contains(NormalizedPoint, inCircumferentialRingOfWidth: CGFloat) -> Bool](/documentation/vision/normalizedcircle/contains(_:incircumferentialringofwidth:))

### Getting the bounding circle

- [static func boundingCircle(for: [NormalizedPoint]) -> NormalizedCircle](/documentation/vision/normalizedcircle/boundingcircle(for:))
- [BoundingBoxProviding](/documentation/vision/boundingboxproviding)

### Getting the bounding box

- [var boundingBox: NormalizedRect](/documentation/vision/boundingboxproviding/boundingbox)
- [BoundingRegionProviding](/documentation/vision/boundingregionproviding)

### Getting the bounding region

- [var boundingRegion: NormalizedRegion](/documentation/vision/boundingregionproviding/boundingregion)
- [QuadrilateralProviding](/documentation/vision/quadrilateralproviding)

### Getting the normalized points

- [var bottomLeft: NormalizedPoint](/documentation/vision/quadrilateralproviding/bottomleft)
- [var bottomRight: NormalizedPoint](/documentation/vision/quadrilateralproviding/bottomright)
- [var topLeft: NormalizedPoint](/documentation/vision/quadrilateralproviding/topleft)
- [var topRight: NormalizedPoint](/documentation/vision/quadrilateralproviding/topright)
- [CoordinateOrigin](/documentation/vision/coordinateorigin)

### Getting the origins

- [case upperLeft](/documentation/vision/coordinateorigin/upperleft)
- [case lowerLeft](/documentation/vision/coordinateorigin/lowerleft)

## Errors

- [VisionError](/documentation/vision/visionerror)

### Getting the error

- [case internalError(String)](/documentation/vision/visionerror/internalerror(_:))
- [case ioError(String)](/documentation/vision/visionerror/ioerror(_:))
- [case operationFailed(String)](/documentation/vision/visionerror/operationfailed(_:))
- [case outOfBoundsError(String)](/documentation/vision/visionerror/outofboundserror(_:))
- [case outOfMemory(String)](/documentation/vision/visionerror/outofmemory(_:))
- [case pixelBufferCreationFailed(CVReturn)](/documentation/vision/visionerror/pixelbuffercreationfailed(_:))
- [case requestCancelled(String)](/documentation/vision/visionerror/requestcancelled(_:))
- [case timeStampNotFound(String)](/documentation/vision/visionerror/timestampnotfound(_:))
- [case timeout(String)](/documentation/vision/visionerror/timeout(_:))

### Getting the invalid error

- [case invalidArgument(String)](/documentation/vision/visionerror/invalidargument(_:))
- [case invalidFormat(String)](/documentation/vision/visionerror/invalidformat(_:))
- [case invalidImage(String)](/documentation/vision/visionerror/invalidimage(_:))
- [case invalidModel(String)](/documentation/vision/visionerror/invalidmodel(_:))
- [case invalidOperation(String)](/documentation/vision/visionerror/invalidoperation(_:))

### Getting the data-unavailable error

- [case dataUnavailable(String)](/documentation/vision/visionerror/dataunavailable(_:))

### Getting the unsupported error

- [case unsupportedComputeDevice(String)](/documentation/vision/visionerror/unsupportedcomputedevice(_:))
- [case unsupportedComputeStage(String)](/documentation/vision/visionerror/unsupportedcomputestage(_:))
- [case unsupportedRequest(String)](/documentation/vision/visionerror/unsupportedrequest(_:))
- [case unsupportedRevision(String)](/documentation/vision/visionerror/unsupportedrevision(_:))

### Getting the error description

- [var description: String](/documentation/vision/visionerror/description)

## Legacy API

- [Original Objective-C and Swift API](/documentation/vision/original-objective-c-and-swift-api)

### Essentials

- [Building a feature-rich app for sports analysis](/documentation/vision/building-a-feature-rich-app-for-sports-analysis)

### Still-image analysis

- [Detecting Objects in Still Images](/documentation/vision/detecting-objects-in-still-images)
- [Classifying images for categorization and search](/documentation/vision/classifying-images-for-categorization-and-search)
- [Analyzing Image Similarity with Feature Print](/documentation/vision/analyzing-image-similarity-with-feature-print)
- [VNRequest](/documentation/vision/vnrequest)

#### Initializing a Request

- [convenience init()](/documentation/vision/vnrequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vnrequest/init(completionhandler:))

#### Configuring a Request

- [VNRequestCompletionHandler](/documentation/vision/vnrequestcompletionhandler)
- [var completionHandler: VNRequestCompletionHandler?](/documentation/vision/vnrequest/completionhandler)
- [var preferBackgroundProcessing: Bool](/documentation/vision/vnrequest/preferbackgroundprocessing)
- [var results: [VNObservation]?](/documentation/vision/vnrequest/results)
- [var revision: Int](/documentation/vision/vnrequest/revision)
- [var usesCPUOnly: Bool](/documentation/vision/vnrequest/usescpuonly)

#### Configuring the Compute Device

- [func setComputeDevice(MLComputeDevice?, for: VNComputeStage)](/documentation/vision/vnrequest/setcomputedevice(_:for:))
- [func computeDevice(for: VNComputeStage) -> MLComputeDevice?](/documentation/vision/vnrequest/computedevice(for:))
- [var supportedComputeStageDevices: [VNComputeStage : [MLComputeDevice]]](/documentation/vision/vnrequest/supportedcomputestagedevices)

#### Canceling a Request

- [func cancel()](/documentation/vision/vnrequest/cancel())

#### Executing a Completion Handler

- [VNRequestCompletionHandler](/documentation/vision/vnrequestcompletionhandler)

#### Determining the Revision

- [VNRequestRevisionProviding](/documentation/vision/vnrequestrevisionproviding)

##### Specifying Revision Number

- [var requestRevision: Int](/documentation/vision/vnrequestrevisionproviding/requestrevision)

##### Determining Revision Type

- [let VNRequestRevisionUnspecified: Int](/documentation/vision/vnrequestrevisionunspecified)
- [let VNDetectRectanglesRequestRevision1: Int](/documentation/vision/vndetectrectanglesrequestrevision1)
- [let VNTrackRectangleRequestRevision1: Int](/documentation/vision/vntrackrectanglerequestrevision1)
- [let VNTrackObjectRequestRevision1: Int](/documentation/vision/vntrackobjectrequestrevision1)
- [let VNDetectFaceRectanglesRequestRevision2: Int](/documentation/vision/vndetectfacerectanglesrequestrevision2)
- [let VNDetectFaceRectanglesRequestRevision1: Int](/documentation/vision/vndetectfacerectanglesrequestrevision1)
- [let VNDetectFaceLandmarksRequestRevision3: Int](/documentation/vision/vndetectfacelandmarksrequestrevision3)
- [let VNDetectFaceLandmarksRequestRevision2: Int](/documentation/vision/vndetectfacelandmarksrequestrevision2)
- [let VNDetectFaceLandmarksRequestRevision1: Int](/documentation/vision/vndetectfacelandmarksrequestrevision1)
- [let VNRecognizeTextRequestRevision1: Int](/documentation/vision/vnrecognizetextrequestrevision1)
- [let VNDetectTextRectanglesRequestRevision1: Int](/documentation/vision/vndetecttextrectanglesrequestrevision1)
- [let VNDetectBarcodesRequestRevision1: Int](/documentation/vision/vndetectbarcodesrequestrevision1)
- [let VNDetectHorizonRequestRevision1: Int](/documentation/vision/vndetecthorizonrequestrevision1)
- [let VNTranslationalImageRegistrationRequestRevision1: Int](/documentation/vision/vntranslationalimageregistrationrequestrevision1)
- [let VNHomographicImageRegistrationRequestRevision1: Int](/documentation/vision/vnhomographicimageregistrationrequestrevision1)
- [let VNCoreMLRequestRevision1: Int](/documentation/vision/vncoremlrequestrevision1)
- [let VNGenerateAttentionBasedSaliencyImageRequestRevision1: Int](/documentation/vision/vngenerateattentionbasedsaliencyimagerequestrevision1)
- [let VNGenerateObjectnessBasedSaliencyImageRequestRevision1: Int](/documentation/vision/vngenerateobjectnessbasedsaliencyimagerequestrevision1)
- [let VNClassifyImageRequestRevision1: Int](/documentation/vision/vnclassifyimagerequestrevision1)
- [let VNGenerateImageFeaturePrintRequestRevision1: Int](/documentation/vision/vngenerateimagefeatureprintrequestrevision1)
- [let VNDetectFaceCaptureQualityRequestRevision1: Int](/documentation/vision/vndetectfacecapturequalityrequestrevision1)
- [let VNDetectHumanRectanglesRequestRevision1: Int](/documentation/vision/vndetecthumanrectanglesrequestrevision1)
- [class var currentRevision: Int](/documentation/vision/vnrequest/currentrevision)
- [class var defaultRevision: Int](/documentation/vision/vnrequest/defaultrevision)
- [class var supportedRevisions: IndexSet](/documentation/vision/vnrequest/supportedrevisions)
- [VNImageBasedRequest](/documentation/vision/vnimagebasedrequest)

#### Configuring a Request

- [var regionOfInterest: CGRect](/documentation/vision/vnimagebasedrequest/regionofinterest)
- [VNClassifyImageRequest](/documentation/vision/vnclassifyimagerequest)

#### Accessing Results

- [func supportedIdentifiers() throws -> [String]](/documentation/vision/vnclassifyimagerequest/supportedidentifiers())
- [var results: [VNClassificationObservation]?](/documentation/vision/vnclassifyimagerequest/results)
- [VNClassificationObservation](/documentation/vision/vnclassificationobservation)

##### Determining Classification

- [var identifier: String](/documentation/vision/vnclassificationobservation/identifier)

##### Measuring Confidence and Precision

- [var hasPrecisionRecallCurve: Bool](/documentation/vision/vnclassificationobservation/hasprecisionrecallcurve)
- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumrecall(_:forprecision:))
- [class func knownClassifications(forRevision: Int) throws -> [VNClassificationObservation]](/documentation/vision/vnclassifyimagerequest/knownclassifications(forrevision:))

#### Specifying Algorithm Revision

- [let VNClassifyImageRequestRevision1: Int](/documentation/vision/vnclassifyimagerequestrevision1)
- [VNGenerateImageFeaturePrintRequest](/documentation/vision/vngenerateimagefeatureprintrequest)

#### Scaling and Cropping Images

- [var imageCropAndScaleOption: VNImageCropAndScaleOption](/documentation/vision/vngenerateimagefeatureprintrequest/imagecropandscaleoption)
- [VNImageCropAndScaleOption](/documentation/vision/vnimagecropandscaleoption)

##### Crop and Scale Options

- [case centerCrop](/documentation/vision/vnimagecropandscaleoption/centercrop)
- [case scaleFit](/documentation/vision/vnimagecropandscaleoption/scalefit)
- [case scaleFill](/documentation/vision/vnimagecropandscaleoption/scalefill)
- [case scaleFitRotate90CCW](/documentation/vision/vnimagecropandscaleoption/scalefitrotate90ccw)
- [case scaleFillRotate90CCW](/documentation/vision/vnimagecropandscaleoption/scalefillrotate90ccw)

##### Creating a Scale Option

- [init?(rawValue: UInt)](/documentation/vision/vnimagecropandscaleoption/init(rawvalue:))

#### Accessing the Results

- [var results: [VNFeaturePrintObservation]?](/documentation/vision/vngenerateimagefeatureprintrequest/results)
- [VNFeaturePrintObservation](/documentation/vision/vnfeatureprintobservation)

##### Fetching Feature Print Data

- [var data: Data](/documentation/vision/vnfeatureprintobservation/data)
- [var elementCount: Int](/documentation/vision/vnfeatureprintobservation/elementcount)

##### Determining Types of Feature Prints

- [var elementType: VNElementType](/documentation/vision/vnfeatureprintobservation/elementtype)
- [VNElementType](/documentation/vision/vnelementtype)

###### Element Types

- [case unknown](/documentation/vision/vnelementtype/unknown)
- [case float](/documentation/vision/vnelementtype/float)
- [case double](/documentation/vision/vnelementtype/double)

###### Creating an Element Type

- [init?(rawValue: UInt)](/documentation/vision/vnelementtype/init(rawvalue:))
- [func VNElementTypeSize(VNElementType) -> Int](/documentation/vision/vnelementtypesize(_:))

##### Computing Distance Between Features

- [func computeDistance(UnsafeMutablePointer<Float>, to: VNFeaturePrintObservation) throws](/documentation/vision/vnfeatureprintobservation/computedistance(_:to:))

#### Identifying Request Revisions

- [let VNGenerateImageFeaturePrintRequestRevision1: Int](/documentation/vision/vngenerateimagefeatureprintrequestrevision1)
- [VNFeaturePrintObservation](/documentation/vision/vnfeatureprintobservation)

#### Fetching Feature Print Data

- [var data: Data](/documentation/vision/vnfeatureprintobservation/data)
- [var elementCount: Int](/documentation/vision/vnfeatureprintobservation/elementcount)

#### Determining Types of Feature Prints

- [var elementType: VNElementType](/documentation/vision/vnfeatureprintobservation/elementtype)
- [VNElementType](/documentation/vision/vnelementtype)

##### Element Types

- [case unknown](/documentation/vision/vnelementtype/unknown)
- [case float](/documentation/vision/vnelementtype/float)
- [case double](/documentation/vision/vnelementtype/double)

##### Creating an Element Type

- [init?(rawValue: UInt)](/documentation/vision/vnelementtype/init(rawvalue:))
- [func VNElementTypeSize(VNElementType) -> Int](/documentation/vision/vnelementtypesize(_:))

#### Computing Distance Between Features

- [func computeDistance(UnsafeMutablePointer<Float>, to: VNFeaturePrintObservation) throws](/documentation/vision/vnfeatureprintobservation/computedistance(_:to:))
- [VNImageRequestHandler](/documentation/vision/vnimagerequesthandler)

#### Creating a Request Handler

- [init(cgImage: CGImage, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cgimage:options:))
- [init(cgImage: CGImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cgimage:orientation:options:))
- [init(ciImage: CIImage, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(ciimage:options:))
- [init(ciImage: CIImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(ciimage:orientation:options:))
- [init(cvPixelBuffer: CVPixelBuffer, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cvpixelbuffer:options:))
- [init(cvPixelBuffer: CVPixelBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cvpixelbuffer:orientation:options:))
- [init(cvPixelBuffer: CVPixelBuffer, depthData: AVDepthData, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cvpixelbuffer:depthdata:orientation:options:))
- [init(cmSampleBuffer: CMSampleBuffer, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cmsamplebuffer:options:))
- [init(cmSampleBuffer: CMSampleBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cmsamplebuffer:orientation:options:))
- [init(cmSampleBuffer: CMSampleBuffer, depthData: AVDepthData, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(cmsamplebuffer:depthdata:orientation:options:))
- [init(data: Data, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(data:options:))
- [init(data: Data, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(data:orientation:options:))
- [init(url: URL, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(url:options:))
- [init(url: URL, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any])](/documentation/vision/vnimagerequesthandler/init(url:orientation:options:))

#### Executing a Request Handler

- [func perform([VNRequest]) throws](/documentation/vision/vnimagerequesthandler/perform(_:))

#### Setting Image Options

- [VNImageOption](/documentation/vision/vnimageoption)

##### Initializers

- [init(rawValue: String)](/documentation/vision/vnimageoption/init(rawvalue:))

##### Options Dictionary Keys

- [static let properties: VNImageOption](/documentation/vision/vnimageoption/properties)
- [static let cameraIntrinsics: VNImageOption](/documentation/vision/vnimageoption/cameraintrinsics)
- [static let ciContext: VNImageOption](/documentation/vision/vnimageoption/cicontext)
- [VNObservation](/documentation/vision/vnobservation)

#### Tracking Observations

- [var uuid: UUID](/documentation/vision/vnobservation/uuid)

#### Evaluating Observations

- [var timeRange: CMTimeRange](/documentation/vision/vnobservation/timerange)
- [var confidence: VNConfidence](/documentation/vision/vnobservation/confidence)
- [VNConfidence](/documentation/vision/vnconfidence)

### Image sequence analysis

- [Applying Matte Effects to People in Images and Video](/documentation/vision/applying-matte-effects-to-people-in-images-and-video)
- [Detecting human actions in a live video feed](/documentation/createml/detecting-human-actions-in-a-live-video-feed)
- [Segmenting and colorizing individuals from a surrounding scene](/documentation/vision/segmenting-and-colorizing-individuals-from-a-surrounding-scene)
- [VNStatefulRequest](/documentation/vision/vnstatefulrequest)

#### Initializing a Request

- [init(frameAnalysisSpacing: CMTime, completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vnstatefulrequest/init(frameanalysisspacing:completionhandler:))

#### Configuring the Request

- [var minimumLatencyFrameCount: Int](/documentation/vision/vnstatefulrequest/minimumlatencyframecount)
- [var frameAnalysisSpacing: CMTime](/documentation/vision/vnstatefulrequest/frameanalysisspacing)
- [VNGeneratePersonSegmentationRequest](/documentation/vision/vngeneratepersonsegmentationrequest)

#### Creating a Request

- [init()](/documentation/vision/vngeneratepersonsegmentationrequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vngeneratepersonsegmentationrequest/init(completionhandler:))

#### Configuring the Request

- [var outputPixelFormat: OSType](/documentation/vision/vngeneratepersonsegmentationrequest/outputpixelformat)
- [var qualityLevel: VNGeneratePersonSegmentationRequest.QualityLevel](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.property)
- [VNGeneratePersonSegmentationRequest.QualityLevel](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.enum)

##### Quality Levels

- [case accurate](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.enum/accurate)
- [case balanced](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.enum/balanced)
- [case fast](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.enum/fast)

##### Creating a Quality Level

- [init?(rawValue: UInt)](/documentation/vision/vngeneratepersonsegmentationrequest/qualitylevel-swift.enum/init(rawvalue:))

#### Getting the supported output pixel formats

- [func supportedOutputPixelFormats() throws -> [NSNumber]](/documentation/vision/vngeneratepersonsegmentationrequest/supportedoutputpixelformats())

#### Accessing the Results

- [var results: [VNPixelBufferObservation]?](/documentation/vision/vngeneratepersonsegmentationrequest/results)
- [VNPixelBufferObservation](/documentation/vision/vnpixelbufferobservation)

##### Parsing Observation Content

- [var pixelBuffer: CVPixelBuffer](/documentation/vision/vnpixelbufferobservation/pixelbuffer)
- [var featureName: String?](/documentation/vision/vnpixelbufferobservation/featurename)

##### Getting the supported pixel formats

- [func supportedOutputPixelFormats() throws -> [NSNumber]](/documentation/vision/vngeneratepersonsegmentationrequest/supportedoutputpixelformats())

#### Identifying Request Revisions

- [let VNGeneratePersonSegmentationRequestRevision1: Int](/documentation/vision/vngeneratepersonsegmentationrequestrevision1)
- [VNGeneratePersonInstanceMaskRequest](/documentation/vision/vngeneratepersoninstancemaskrequest)

#### Accessing the Results

- [var results: [VNInstanceMaskObservation]?](/documentation/vision/vngeneratepersoninstancemaskrequest/results)

#### Identifying Request Revisions

- [let VNGeneratePersonInstanceMaskRequestRevision1: Int](/documentation/vision/vngeneratepersoninstancemaskrequestrevision1)
- [VNDetectDocumentSegmentationRequest](/documentation/vision/vndetectdocumentsegmentationrequest)

#### Accessing the Results

- [var results: [VNRectangleObservation]?](/documentation/vision/vndetectdocumentsegmentationrequest/results)
- [VNRectangleObservation](/documentation/vision/vnrectangleobservation)

##### Creating an Observation

- [convenience init(requestRevision: Int, topLeft: CGPoint, topRight: CGPoint, bottomRight: CGPoint, bottomLeft: CGPoint)](/documentation/vision/vnrectangleobservation/init(requestrevision:topleft:topright:bottomright:bottomleft:))
- [convenience init(requestRevision: Int, topLeft: CGPoint, bottomLeft: CGPoint, bottomRight: CGPoint, topRight: CGPoint)](/documentation/vision/vnrectangleobservation/init(requestrevision:topleft:bottomleft:bottomright:topright:))

##### Accessing the Coordinates

- [var bottomLeft: CGPoint](/documentation/vision/vnrectangleobservation/bottomleft)
- [var bottomRight: CGPoint](/documentation/vision/vnrectangleobservation/bottomright)
- [var topLeft: CGPoint](/documentation/vision/vnrectangleobservation/topleft)
- [var topRight: CGPoint](/documentation/vision/vnrectangleobservation/topright)

#### Identifying Request Revisions

- [let VNDetectDocumentSegmentationRequestRevision1: Int](/documentation/vision/vndetectdocumentsegmentationrequestrevision1)
- [VNSequenceRequestHandler](/documentation/vision/vnsequencerequesthandler)

#### Initializing a Sequence Request

- [init()](/documentation/vision/vnsequencerequesthandler/init())

#### Performing a Sequence Request

- [func perform([VNRequest], on: CGImage) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:)-3zt7l)
- [func perform([VNRequest], on: CGImage, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:orientation:)-3gcmv)
- [func perform([VNRequest], on: CIImage) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:)-9jtgj)
- [func perform([VNRequest], on: CIImage, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:orientation:)-1bkm1)
- [func perform([VNRequest], on: CVPixelBuffer) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:)-3d7nt)
- [func perform([VNRequest], on: CVPixelBuffer, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:orientation:)-2wvt8)
- [func perform([VNRequest], on: CMSampleBuffer) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:)-45e73)
- [func perform([VNRequest], on: CMSampleBuffer, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:on:orientation:)-6b7rk)
- [func perform([VNRequest], onImageData: Data) throws](/documentation/vision/vnsequencerequesthandler/perform(_:onimagedata:))
- [func perform([VNRequest], onImageData: Data, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:onimagedata:orientation:))
- [func perform([VNRequest], onImageURL: URL) throws](/documentation/vision/vnsequencerequesthandler/perform(_:onimageurl:))
- [func perform([VNRequest], onImageURL: URL, orientation: CGImagePropertyOrientation) throws](/documentation/vision/vnsequencerequesthandler/perform(_:onimageurl:orientation:))

### Image aesthetics analysis

- [VNCalculateImageAestheticsScoresRequest](/documentation/vision/vncalculateimageaestheticsscoresrequest)

#### Accessing the results

- [var results: [VNImageAestheticsScoresObservation]?](/documentation/vision/vncalculateimageaestheticsscoresrequest/results)
- [VNImageAestheticsScoresObservation](/documentation/vision/vnimageaestheticsscoresobservation)

##### Parsing Observation Content

- [var overallScore: Float](/documentation/vision/vnimageaestheticsscoresobservation/overallscore)
- [var isUtility: Bool](/documentation/vision/vnimageaestheticsscoresobservation/isutility)

### Saliency analysis

- [Cropping Images Using Saliency](/documentation/vision/cropping-images-using-saliency)
- [Highlighting Areas of Interest in an Image Using Saliency](/documentation/vision/highlighting-areas-of-interest-in-an-image-using-saliency)
- [VNGenerateAttentionBasedSaliencyImageRequest](/documentation/vision/vngenerateattentionbasedsaliencyimagerequest)

#### Accessing the Results

- [var results: [VNSaliencyImageObservation]?](/documentation/vision/vngenerateattentionbasedsaliencyimagerequest/results)

#### Identifying Request Revisions

- [let VNGenerateAttentionBasedSaliencyImageRequestRevision1: Int](/documentation/vision/vngenerateattentionbasedsaliencyimagerequestrevision1)
- [VNGenerateObjectnessBasedSaliencyImageRequest](/documentation/vision/vngenerateobjectnessbasedsaliencyimagerequest)

#### Accessing the Results

- [var results: [VNSaliencyImageObservation]?](/documentation/vision/vngenerateobjectnessbasedsaliencyimagerequest/results)

#### Identifying Request Revisions

- [let VNGenerateObjectnessBasedSaliencyImageRequestRevision1: Int](/documentation/vision/vngenerateobjectnessbasedsaliencyimagerequestrevision1)
- [VNSaliencyImageObservation](/documentation/vision/vnsaliencyimageobservation)

#### Locating Salient Regions

- [var salientObjects: [VNRectangleObservation]?](/documentation/vision/vnsaliencyimageobservation/salientobjects)

### Object tracking

- [Tracking the User’s Face in Real Time](/documentation/vision/tracking-the-user-s-face-in-real-time)
- [Tracking Multiple Objects or Rectangles in Video](/documentation/vision/tracking-multiple-objects-or-rectangles-in-video)
- [VNTrackingRequest](/documentation/vision/vntrackingrequest)

#### Configuring a Tracking Request

- [VNRequestTrackingLevel](/documentation/vision/vnrequesttrackinglevel)

##### Enumeration Cases

- [case accurate](/documentation/vision/vnrequesttrackinglevel/accurate)
- [case fast](/documentation/vision/vnrequesttrackinglevel/fast)

##### Creating a Tracking Level

- [init?(rawValue: UInt)](/documentation/vision/vnrequesttrackinglevel/init(rawvalue:))
- [var inputObservation: VNDetectedObjectObservation](/documentation/vision/vntrackingrequest/inputobservation)
- [var trackingLevel: VNRequestTrackingLevel](/documentation/vision/vntrackingrequest/trackinglevel)
- [var isLastFrame: Bool](/documentation/vision/vntrackingrequest/islastframe)

#### Getting the Number of Trackers

- [func supportedNumber(ofTrackersAndReturnError: NSErrorPointer) -> Int](/documentation/vision/vntrackingrequest/supportednumber(oftrackersandreturnerror:))
- [VNTrackRectangleRequest](/documentation/vision/vntrackrectanglerequest)

#### Initializing a Rectangle Tracking Request

- [convenience init(rectangleObservation: VNRectangleObservation)](/documentation/vision/vntrackrectanglerequest/init(rectangleobservation:))
- [init(rectangleObservation: VNRectangleObservation, completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntrackrectanglerequest/init(rectangleobservation:completionhandler:))

#### Identifying Request Revisions

- [let VNTrackRectangleRequestRevision1: Int](/documentation/vision/vntrackrectanglerequestrevision1)
- [VNTrackObjectRequest](/documentation/vision/vntrackobjectrequest)

#### Initializing an Object Tracking Request

- [init(detectedObjectObservation: VNDetectedObjectObservation)](/documentation/vision/vntrackobjectrequest/init(detectedobjectobservation:))
- [init(detectedObjectObservation: VNDetectedObjectObservation, completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntrackobjectrequest/init(detectedobjectobservation:completionhandler:))

#### Identifying Request Revisions

- [let VNTrackObjectRequestRevision2: Int](/documentation/vision/vntrackobjectrequestrevision2)
- [let VNTrackObjectRequestRevision1: Int](/documentation/vision/vntrackobjectrequestrevision1)
- [VNDetectedObjectObservation](/documentation/vision/vndetectedobjectobservation)

#### Creating an Observation

- [convenience init(boundingBox: CGRect)](/documentation/vision/vndetectedobjectobservation/init(boundingbox:))
- [convenience init(requestRevision: Int, boundingBox: CGRect)](/documentation/vision/vndetectedobjectobservation/init(requestrevision:boundingbox:))

#### Locating a Detected Object

- [var boundingBox: CGRect](/documentation/vision/vndetectedobjectobservation/boundingbox)

#### Accessing an Image Mask

- [var globalSegmentationMask: VNPixelBufferObservation?](/documentation/vision/vndetectedobjectobservation/globalsegmentationmask)

### Rectangle detection

- [VNDetectRectanglesRequest](/documentation/vision/vndetectrectanglesrequest)

#### Configuring Detection

- [var minimumAspectRatio: VNAspectRatio](/documentation/vision/vndetectrectanglesrequest/minimumaspectratio)
- [var maximumAspectRatio: VNAspectRatio](/documentation/vision/vndetectrectanglesrequest/maximumaspectratio)
- [VNAspectRatio](/documentation/vision/vnaspectratio)
- [var quadratureTolerance: VNDegrees](/documentation/vision/vndetectrectanglesrequest/quadraturetolerance)
- [VNDegrees](/documentation/vision/vndegrees)
- [var minimumSize: Float](/documentation/vision/vndetectrectanglesrequest/minimumsize)
- [var minimumConfidence: VNConfidence](/documentation/vision/vndetectrectanglesrequest/minimumconfidence)
- [VNConfidence](/documentation/vision/vnconfidence)
- [var maximumObservations: Int](/documentation/vision/vndetectrectanglesrequest/maximumobservations)

#### Accessing the Results

- [var results: [VNRectangleObservation]?](/documentation/vision/vndetectrectanglesrequest/results)
- [VNRectangleObservation](/documentation/vision/vnrectangleobservation)

##### Creating an Observation

- [convenience init(requestRevision: Int, topLeft: CGPoint, topRight: CGPoint, bottomRight: CGPoint, bottomLeft: CGPoint)](/documentation/vision/vnrectangleobservation/init(requestrevision:topleft:topright:bottomright:bottomleft:))
- [convenience init(requestRevision: Int, topLeft: CGPoint, bottomLeft: CGPoint, bottomRight: CGPoint, topRight: CGPoint)](/documentation/vision/vnrectangleobservation/init(requestrevision:topleft:bottomleft:bottomright:topright:))

##### Accessing the Coordinates

- [var bottomLeft: CGPoint](/documentation/vision/vnrectangleobservation/bottomleft)
- [var bottomRight: CGPoint](/documentation/vision/vnrectangleobservation/bottomright)
- [var topLeft: CGPoint](/documentation/vision/vnrectangleobservation/topleft)
- [var topRight: CGPoint](/documentation/vision/vnrectangleobservation/topright)

#### Identifying Request Revisions

- [let VNDetectRectanglesRequestRevision1: Int](/documentation/vision/vndetectrectanglesrequestrevision1)

### Face and body detection

- [Selecting a selfie based on capture quality](/documentation/vision/selecting-a-selfie-based-on-capture-quality)
- [VNDetectFaceCaptureQualityRequest](/documentation/vision/vndetectfacecapturequalityrequest)

#### Accessing the Results

- [var results: [VNFaceObservation]?](/documentation/vision/vndetectfacecapturequalityrequest/results)
- [VNFaceObservation](/documentation/vision/vnfaceobservation)

##### Creating an Observation

- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?, pitch: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:pitch:))
- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:))

##### Identifying Landmarks

- [var landmarks: VNFaceLandmarks2D?](/documentation/vision/vnfaceobservation/landmarks)
- [VNFaceLandmarks2D](/documentation/vision/vnfacelandmarks2d)

###### Face Landmark Points

- [var allPoints: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/allpoints)
- [var faceContour: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/facecontour)
- [var leftEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteye)
- [var rightEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteye)
- [var leftEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteyebrow)
- [var rightEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteyebrow)
- [var nose: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nose)
- [var noseCrest: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nosecrest)
- [var medianLine: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/medianline)
- [var outerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/outerlips)
- [var innerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/innerlips)
- [var leftPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/leftpupil)
- [var rightPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/rightpupil)
- [VNFaceLandmarkRegion2D](/documentation/vision/vnfacelandmarkregion2d)

###### Describing Region Points

- [var pointsClassification: VNPointsClassification](/documentation/vision/vnfacelandmarkregion2d/pointsclassification)
- [VNPointsClassification](/documentation/vision/vnpointsclassification)

###### Enumeration Cases

- [case closedPath](/documentation/vision/vnpointsclassification/closedpath)
- [case disconnected](/documentation/vision/vnpointsclassification/disconnected)
- [case openPath](/documentation/vision/vnpointsclassification/openpath)

###### Creating a Classification

- [init?(rawValue: Int)](/documentation/vision/vnpointsclassification/init(rawvalue:))

###### Specifying Region Properties

- [var normalizedPoints: [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/normalizedpoints-7s7im)
- [var precisionEstimatesPerPoint: [Float]?](/documentation/vision/vnfacelandmarkregion2d/precisionestimatesperpoint-5jl22)

###### Computing Feature Points

- [func pointsInImage(imageSize: CGSize) -> [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/pointsinimage(imagesize:))
- [VNFaceLandmarks](/documentation/vision/vnfacelandmarks)

###### Determining Accuracy

- [var confidence: VNConfidence](/documentation/vision/vnfacelandmarks/confidence)
- [VNFaceLandmarkRegion](/documentation/vision/vnfacelandmarkregion)

###### Instance Properties

- [var pointCount: Int](/documentation/vision/vnfacelandmarkregion/pointcount)

##### Determining Facial Orientation

- [var roll: NSNumber?](/documentation/vision/vnfaceobservation/roll)
- [var yaw: NSNumber?](/documentation/vision/vnfaceobservation/yaw)
- [var pitch: NSNumber?](/documentation/vision/vnfaceobservation/pitch)

##### Determining Capture Quality

- [var faceCaptureQuality: Float?](/documentation/vision/vnfaceobservation/facecapturequality-bjg5)

#### Identifying Request Revisions

- [let VNDetectFaceCaptureQualityRequestRevision2: Int](/documentation/vision/vndetectfacecapturequalityrequestrevision2)
- [let VNDetectFaceCaptureQualityRequestRevision1: Int](/documentation/vision/vndetectfacecapturequalityrequestrevision1)
- [VNDetectFaceLandmarksRequest](/documentation/vision/vndetectfacelandmarksrequest)

#### Configuring a Face Landmarks Request

- [VNFaceObservationAccepting](/documentation/vision/vnfaceobservationaccepting)

##### Providing Face Observations

- [var inputFaceObservations: [VNFaceObservation]?](/documentation/vision/vnfaceobservationaccepting/inputfaceobservations)

#### Accessing the Results

- [var results: [VNFaceObservation]?](/documentation/vision/vndetectfacelandmarksrequest/results)
- [VNFaceObservation](/documentation/vision/vnfaceobservation)

##### Creating an Observation

- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?, pitch: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:pitch:))
- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:))

##### Identifying Landmarks

- [var landmarks: VNFaceLandmarks2D?](/documentation/vision/vnfaceobservation/landmarks)
- [VNFaceLandmarks2D](/documentation/vision/vnfacelandmarks2d)

###### Face Landmark Points

- [var allPoints: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/allpoints)
- [var faceContour: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/facecontour)
- [var leftEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteye)
- [var rightEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteye)
- [var leftEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteyebrow)
- [var rightEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteyebrow)
- [var nose: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nose)
- [var noseCrest: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nosecrest)
- [var medianLine: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/medianline)
- [var outerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/outerlips)
- [var innerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/innerlips)
- [var leftPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/leftpupil)
- [var rightPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/rightpupil)
- [VNFaceLandmarkRegion2D](/documentation/vision/vnfacelandmarkregion2d)

###### Describing Region Points

- [var pointsClassification: VNPointsClassification](/documentation/vision/vnfacelandmarkregion2d/pointsclassification)
- [VNPointsClassification](/documentation/vision/vnpointsclassification)

###### Enumeration Cases

- [case closedPath](/documentation/vision/vnpointsclassification/closedpath)
- [case disconnected](/documentation/vision/vnpointsclassification/disconnected)
- [case openPath](/documentation/vision/vnpointsclassification/openpath)

###### Creating a Classification

- [init?(rawValue: Int)](/documentation/vision/vnpointsclassification/init(rawvalue:))

###### Specifying Region Properties

- [var normalizedPoints: [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/normalizedpoints-7s7im)
- [var precisionEstimatesPerPoint: [Float]?](/documentation/vision/vnfacelandmarkregion2d/precisionestimatesperpoint-5jl22)

###### Computing Feature Points

- [func pointsInImage(imageSize: CGSize) -> [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/pointsinimage(imagesize:))
- [VNFaceLandmarks](/documentation/vision/vnfacelandmarks)

###### Determining Accuracy

- [var confidence: VNConfidence](/documentation/vision/vnfacelandmarks/confidence)
- [VNFaceLandmarkRegion](/documentation/vision/vnfacelandmarkregion)

###### Instance Properties

- [var pointCount: Int](/documentation/vision/vnfacelandmarkregion/pointcount)

##### Determining Facial Orientation

- [var roll: NSNumber?](/documentation/vision/vnfaceobservation/roll)
- [var yaw: NSNumber?](/documentation/vision/vnfaceobservation/yaw)
- [var pitch: NSNumber?](/documentation/vision/vnfaceobservation/pitch)

##### Determining Capture Quality

- [var faceCaptureQuality: Float?](/documentation/vision/vnfaceobservation/facecapturequality-bjg5)

#### Locating Face Landmarks

- [var constellation: VNRequestFaceLandmarksConstellation](/documentation/vision/vndetectfacelandmarksrequest/constellation)
- [VNRequestFaceLandmarksConstellation](/documentation/vision/vnrequestfacelandmarksconstellation)

##### Types of Constellations

- [case constellationNotDefined](/documentation/vision/vnrequestfacelandmarksconstellation/constellationnotdefined)
- [case constellation65Points](/documentation/vision/vnrequestfacelandmarksconstellation/constellation65points)
- [case constellation76Points](/documentation/vision/vnrequestfacelandmarksconstellation/constellation76points)

##### Creating a Constellation

- [init?(rawValue: UInt)](/documentation/vision/vnrequestfacelandmarksconstellation/init(rawvalue:))

#### Identifying Request Revisions

- [class func revision(Int, supportsConstellation: VNRequestFaceLandmarksConstellation) -> Bool](/documentation/vision/vndetectfacelandmarksrequest/revision(_:supportsconstellation:))
- [let VNDetectFaceLandmarksRequestRevision3: Int](/documentation/vision/vndetectfacelandmarksrequestrevision3)
- [let VNDetectFaceLandmarksRequestRevision2: Int](/documentation/vision/vndetectfacelandmarksrequestrevision2)
- [let VNDetectFaceLandmarksRequestRevision1: Int](/documentation/vision/vndetectfacelandmarksrequestrevision1)
- [VNDetectFaceRectanglesRequest](/documentation/vision/vndetectfacerectanglesrequest)

#### Accessing the Results

- [var results: [VNFaceObservation]?](/documentation/vision/vndetectfacerectanglesrequest/results)
- [VNFaceObservation](/documentation/vision/vnfaceobservation)

##### Creating an Observation

- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?, pitch: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:pitch:))
- [convenience init(requestRevision: Int, boundingBox: CGRect, roll: NSNumber?, yaw: NSNumber?)](/documentation/vision/vnfaceobservation/init(requestrevision:boundingbox:roll:yaw:))

##### Identifying Landmarks

- [var landmarks: VNFaceLandmarks2D?](/documentation/vision/vnfaceobservation/landmarks)
- [VNFaceLandmarks2D](/documentation/vision/vnfacelandmarks2d)

###### Face Landmark Points

- [var allPoints: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/allpoints)
- [var faceContour: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/facecontour)
- [var leftEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteye)
- [var rightEye: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteye)
- [var leftEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/lefteyebrow)
- [var rightEyebrow: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/righteyebrow)
- [var nose: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nose)
- [var noseCrest: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/nosecrest)
- [var medianLine: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/medianline)
- [var outerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/outerlips)
- [var innerLips: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/innerlips)
- [var leftPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/leftpupil)
- [var rightPupil: VNFaceLandmarkRegion2D?](/documentation/vision/vnfacelandmarks2d/rightpupil)
- [VNFaceLandmarkRegion2D](/documentation/vision/vnfacelandmarkregion2d)

###### Describing Region Points

- [var pointsClassification: VNPointsClassification](/documentation/vision/vnfacelandmarkregion2d/pointsclassification)
- [VNPointsClassification](/documentation/vision/vnpointsclassification)

###### Enumeration Cases

- [case closedPath](/documentation/vision/vnpointsclassification/closedpath)
- [case disconnected](/documentation/vision/vnpointsclassification/disconnected)
- [case openPath](/documentation/vision/vnpointsclassification/openpath)

###### Creating a Classification

- [init?(rawValue: Int)](/documentation/vision/vnpointsclassification/init(rawvalue:))

###### Specifying Region Properties

- [var normalizedPoints: [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/normalizedpoints-7s7im)
- [var precisionEstimatesPerPoint: [Float]?](/documentation/vision/vnfacelandmarkregion2d/precisionestimatesperpoint-5jl22)

###### Computing Feature Points

- [func pointsInImage(imageSize: CGSize) -> [CGPoint]](/documentation/vision/vnfacelandmarkregion2d/pointsinimage(imagesize:))
- [VNFaceLandmarks](/documentation/vision/vnfacelandmarks)

###### Determining Accuracy

- [var confidence: VNConfidence](/documentation/vision/vnfacelandmarks/confidence)
- [VNFaceLandmarkRegion](/documentation/vision/vnfacelandmarkregion)

###### Instance Properties

- [var pointCount: Int](/documentation/vision/vnfacelandmarkregion/pointcount)

##### Determining Facial Orientation

- [var roll: NSNumber?](/documentation/vision/vnfaceobservation/roll)
- [var yaw: NSNumber?](/documentation/vision/vnfaceobservation/yaw)
- [var pitch: NSNumber?](/documentation/vision/vnfaceobservation/pitch)

##### Determining Capture Quality

- [var faceCaptureQuality: Float?](/documentation/vision/vnfaceobservation/facecapturequality-bjg5)

#### Identifying Request Revisions

- [let VNDetectFaceRectanglesRequestRevision3: Int](/documentation/vision/vndetectfacerectanglesrequestrevision3)
- [let VNDetectFaceRectanglesRequestRevision2: Int](/documentation/vision/vndetectfacerectanglesrequestrevision2)
- [let VNDetectFaceRectanglesRequestRevision1: Int](/documentation/vision/vndetectfacerectanglesrequestrevision1)
- [VNDetectHumanRectanglesRequest](/documentation/vision/vndetecthumanrectanglesrequest)

#### Configuring the Request

- [var upperBodyOnly: Bool](/documentation/vision/vndetecthumanrectanglesrequest/upperbodyonly)

#### Accessing the Results

- [var results: [VNHumanObservation]?](/documentation/vision/vndetecthumanrectanglesrequest/results)

#### Identifying Request Revisions

- [let VNDetectHumanRectanglesRequestRevision2: Int](/documentation/vision/vndetecthumanrectanglesrequestrevision2)
- [let VNDetectHumanRectanglesRequestRevision1: Int](/documentation/vision/vndetecthumanrectanglesrequestrevision1)
- [VNHumanObservation](/documentation/vision/vnhumanobservation)

#### Inspecting the Observation

- [var upperBodyOnly: Bool](/documentation/vision/vnhumanobservation/upperbodyonly)

### Body and hand pose detection

- [Detecting Human Body Poses in Images](/documentation/vision/detecting-human-body-poses-in-images)
- [Detecting Hand Poses with Vision](/documentation/vision/detecting-hand-poses-with-vision)
- [VNDetectHumanBodyPoseRequest](/documentation/vision/vndetecthumanbodyposerequest)

#### Determining Supported Joints

- [var supportedJointNames: [VNHumanBodyPoseObservation.JointName]](/documentation/vision/vndetecthumanbodyposerequest/supportedjointnames)
- [class func supportedJointNames(forRevision: Int) throws -> [VNHumanBodyPoseObservation.JointName]](/documentation/vision/vndetecthumanbodyposerequest/supportedjointnames(forrevision:))
- [var supportedJointsGroupNames: [VNHumanBodyPoseObservation.JointsGroupName]](/documentation/vision/vndetecthumanbodyposerequest/supportedjointsgroupnames)
- [class func supportedJointsGroupNames(forRevision: Int) throws -> [VNHumanBodyPoseObservation.JointsGroupName]](/documentation/vision/vndetecthumanbodyposerequest/supportedjointsgroupnames(forrevision:))

#### Accessing the Results

- [var results: [VNHumanBodyPoseObservation]?](/documentation/vision/vndetecthumanbodyposerequest/results)

#### Identifying Body Pose Revisions

- [let VNDetectHumanBodyPoseRequestRevision1: Int](/documentation/vision/vndetecthumanbodyposerequestrevision1)
- [VNDetectHumanHandPoseRequest](/documentation/vision/vndetecthumanhandposerequest)

#### Configuring the Request

- [var maximumHandCount: Int](/documentation/vision/vndetecthumanhandposerequest/maximumhandcount)

#### Determining Supported Joints

- [var supportedJointNames: [VNHumanHandPoseObservation.JointName]](/documentation/vision/vndetecthumanhandposerequest/supportedjointnames)
- [class func supportedJointNames(forRevision: Int) throws -> [VNHumanHandPoseObservation.JointName]](/documentation/vision/vndetecthumanhandposerequest/supportedjointnames(forrevision:))
- [var supportedJointsGroupNames: [VNHumanHandPoseObservation.JointsGroupName]](/documentation/vision/vndetecthumanhandposerequest/supportedjointsgroupnames)
- [class func supportedJointsGroupNames(forRevision: Int) throws -> [VNHumanHandPoseObservation.JointsGroupName]](/documentation/vision/vndetecthumanhandposerequest/supportedjointsgroupnames(forrevision:))

#### Accessing the Results

- [var results: [VNHumanHandPoseObservation]?](/documentation/vision/vndetecthumanhandposerequest/results)

#### Identifying Hand Pose Revisions

- [let VNDetectHumanHandPoseRequestRevision1: Int](/documentation/vision/vndetecthumanhandposerequestrevision1)
- [VNRecognizedPointsObservation](/documentation/vision/vnrecognizedpointsobservation)

#### Inspecting the Observation

- [var availableKeys: [VNRecognizedPointKey]](/documentation/vision/vnrecognizedpointsobservation/availablekeys)
- [var availableGroupKeys: [VNRecognizedPointGroupKey]](/documentation/vision/vnrecognizedpointsobservation/availablegroupkeys)
- [func recognizedPoint(forKey: VNRecognizedPointKey) throws -> VNRecognizedPoint](/documentation/vision/vnrecognizedpointsobservation/recognizedpoint(forkey:))
- [func recognizedPoints(forGroupKey: VNRecognizedPointGroupKey) throws -> [VNRecognizedPointKey : VNRecognizedPoint]](/documentation/vision/vnrecognizedpointsobservation/recognizedpoints(forgroupkey:))

#### Converting Points for Core ML

- [func keypointsMultiArray() throws -> MLMultiArray](/documentation/vision/vnrecognizedpointsobservation/keypointsmultiarray())
- [VNHumanBodyPoseObservation](/documentation/vision/vnhumanbodyposeobservation)

#### Accessing Points

- [var availableJointNames: [VNHumanBodyPoseObservation.JointName]](/documentation/vision/vnhumanbodyposeobservation/availablejointnames)
- [VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname)

##### Head

- [static let leftEar: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftear)
- [static let leftEye: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/lefteye)
- [static let rightEar: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightear)
- [static let rightEye: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/righteye)
- [static let neck: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/neck)
- [static let nose: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/nose)

##### Arms

- [static let leftShoulder: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftshoulder)
- [static let leftElbow: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftelbow)
- [static let leftWrist: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftwrist)
- [static let rightShoulder: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightshoulder)
- [static let rightElbow: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightelbow)
- [static let rightWrist: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightwrist)

##### Waist

- [static let root: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/root)

##### Legs

- [static let leftHip: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/lefthip)
- [static let leftKnee: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftknee)
- [static let leftAnkle: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/leftankle)
- [static let rightHip: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/righthip)
- [static let rightKnee: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightknee)
- [static let rightAnkle: VNHumanBodyPoseObservation.JointName](/documentation/vision/vnhumanbodyposeobservation/jointname/rightankle)

##### Initializers

- [init(rawValue: VNRecognizedPointKey)](/documentation/vision/vnhumanbodyposeobservation/jointname/init(rawvalue:))
- [var availableJointsGroupNames: [VNHumanBodyPoseObservation.JointsGroupName]](/documentation/vision/vnhumanbodyposeobservation/availablejointsgroupnames)
- [VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname)

##### Head

- [static let face: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/face)

##### Body

- [static let torso: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/torso)

##### Arms

- [static let leftArm: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/leftarm)
- [static let rightArm: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/rightarm)

##### Legs

- [static let leftLeg: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/leftleg)
- [static let rightLeg: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/rightleg)

##### All

- [static let all: VNHumanBodyPoseObservation.JointsGroupName](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/all)

##### Initializers

- [init(rawValue: VNRecognizedPointGroupKey)](/documentation/vision/vnhumanbodyposeobservation/jointsgroupname/init(rawvalue:))
- [func recognizedPoint(VNHumanBodyPoseObservation.JointName) throws -> VNRecognizedPoint](/documentation/vision/vnhumanbodyposeobservation/recognizedpoint(_:))
- [func recognizedPoints(VNHumanBodyPoseObservation.JointsGroupName) throws -> [VNHumanBodyPoseObservation.JointName : VNRecognizedPoint]](/documentation/vision/vnhumanbodyposeobservation/recognizedpoints(_:))
- [VNHumanHandPoseObservation](/documentation/vision/vnhumanhandposeobservation)

#### Retrieving Points

- [var availableJointNames: [VNHumanHandPoseObservation.JointName]](/documentation/vision/vnhumanhandposeobservation/availablejointnames)
- [VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname)

##### Thumb

- [static let thumbTip: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/thumbtip)
- [static let thumbIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/thumbip)
- [static let thumbMP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/thumbmp)
- [static let thumbCMC: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/thumbcmc)

##### Index

- [static let indexTip: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/indextip)
- [static let indexDIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/indexdip)
- [static let indexPIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/indexpip)
- [static let indexMCP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/indexmcp)

##### Middle

- [static let middleTip: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/middletip)
- [static let middleDIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/middledip)
- [static let middlePIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/middlepip)
- [static let middleMCP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/middlemcp)

##### Ring

- [static let ringTip: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/ringtip)
- [static let ringDIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/ringdip)
- [static let ringPIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/ringpip)
- [static let ringMCP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/ringmcp)

##### Little

- [static let littleTip: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/littletip)
- [static let littleDIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/littledip)
- [static let littlePIP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/littlepip)
- [static let littleMCP: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/littlemcp)

##### Wrist

- [static let wrist: VNHumanHandPoseObservation.JointName](/documentation/vision/vnhumanhandposeobservation/jointname/wrist)

##### Initializers

- [init(rawValue: VNRecognizedPointKey)](/documentation/vision/vnhumanhandposeobservation/jointname/init(rawvalue:))
- [var availableJointsGroupNames: [VNHumanHandPoseObservation.JointsGroupName]](/documentation/vision/vnhumanhandposeobservation/availablejointsgroupnames)
- [VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname)

##### Group Names

- [static let thumb: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/thumb)
- [static let indexFinger: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/indexfinger)
- [static let littleFinger: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/littlefinger)
- [static let middleFinger: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/middlefinger)
- [static let ringFinger: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/ringfinger)
- [static let all: VNHumanHandPoseObservation.JointsGroupName](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/all)

##### Initializers

- [init(rawValue: VNRecognizedPointGroupKey)](/documentation/vision/vnhumanhandposeobservation/jointsgroupname/init(rawvalue:))
- [func recognizedPoint(VNHumanHandPoseObservation.JointName) throws -> VNRecognizedPoint](/documentation/vision/vnhumanhandposeobservation/recognizedpoint(_:))
- [func recognizedPoints(VNHumanHandPoseObservation.JointsGroupName) throws -> [VNHumanHandPoseObservation.JointName : VNRecognizedPoint]](/documentation/vision/vnhumanhandposeobservation/recognizedpoints(_:))

#### Determining the Chirality

- [var chirality: VNChirality](/documentation/vision/vnhumanhandposeobservation/chirality)
- [VNChirality](/documentation/vision/vnchirality)

##### Chirality Values

- [case left](/documentation/vision/vnchirality/left)
- [case right](/documentation/vision/vnchirality/right)
- [case unknown](/documentation/vision/vnchirality/unknown)

##### Creating a Chirality

- [init?(rawValue: Int)](/documentation/vision/vnchirality/init(rawvalue:))
- [VNPoint](/documentation/vision/vnpoint)

#### Creating a Point

- [init(x: Double, y: Double)](/documentation/vision/vnpoint/init(x:y:))
- [convenience init(location: CGPoint)](/documentation/vision/vnpoint/init(location:))
- [class func apply(VNVector, to: VNPoint) -> VNPoint](/documentation/vision/vnpoint/apply(_:to:))
- [class var zero: VNPoint](/documentation/vision/vnpoint/zero)

#### Inspecting a Point

- [var x: Double](/documentation/vision/vnpoint/x)
- [var y: Double](/documentation/vision/vnpoint/y)
- [var location: CGPoint](/documentation/vision/vnpoint/location)

#### Calculating Distance

- [func distance(VNPoint) -> Double](/documentation/vision/vnpoint/distance(_:))
- [class func distance(VNPoint, VNPoint) -> Double](/documentation/vision/vnpoint/distance(_:_:))
- [VNDetectedPoint](/documentation/vision/vndetectedpoint)

#### Inspecting a Point

- [var confidence: VNConfidence](/documentation/vision/vndetectedpoint/confidence)
- [VNRecognizedPoint](/documentation/vision/vnrecognizedpoint)

#### Inspecting a Point

- [var identifier: VNRecognizedPointKey](/documentation/vision/vnrecognizedpoint/identifier)
- [VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey)

#### Landmarks

- [Body Landmarks](/documentation/vision/body-landmarks)

##### Head

- [static let bodyLandmarkKeyLeftEye: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeylefteye)
- [static let bodyLandmarkKeyRightEye: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrighteye)
- [static let bodyLandmarkKeyLeftEar: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftear)
- [static let bodyLandmarkKeyRightEar: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightear)
- [static let bodyLandmarkKeyNose: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeynose)
- [static let bodyLandmarkRegionKeyFace: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyface)

##### Torso

- [static let bodyLandmarkKeyNeck: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyneck)
- [static let bodyLandmarkKeyLeftShoulder: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftshoulder)
- [static let bodyLandmarkKeyRightShoulder: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightshoulder)
- [static let bodyLandmarkKeyLeftHip: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeylefthip)
- [static let bodyLandmarkKeyRightHip: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrighthip)
- [static let bodyLandmarkKeyRoot: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyroot)
- [static let bodyLandmarkRegionKeyTorso: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeytorso)

##### Arms

- [static let bodyLandmarkKeyRightWrist: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightwrist)
- [static let bodyLandmarkKeyRightElbow: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightelbow)
- [static let bodyLandmarkRegionKeyRightArm: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyrightarm)
- [static let bodyLandmarkKeyLeftWrist: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftwrist)
- [static let bodyLandmarkKeyLeftElbow: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftelbow)
- [static let bodyLandmarkRegionKeyLeftArm: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyleftarm)

##### Legs

- [static let bodyLandmarkKeyRightKnee: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightknee)
- [static let bodyLandmarkKeyRightAnkle: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyrightankle)
- [static let bodyLandmarkRegionKeyRightLeg: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyrightleg)
- [static let bodyLandmarkKeyLeftKnee: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftknee)
- [static let bodyLandmarkKeyLeftAnkle: VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey/bodylandmarkkeyleftankle)
- [static let bodyLandmarkRegionKeyLeftLeg: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyleftleg)

##### All Landmarks

- [static let all: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/all)
- [Hand Landmarks](/documentation/vision/hand-landmarks)

##### All Landmarks

- [static let all: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/all)

#### Initializers

- [init(rawValue: String)](/documentation/vision/vnrecognizedpointkey/init(rawvalue:))
- [VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey)

#### Body Regions

- [static let bodyLandmarkRegionKeyFace: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyface)
- [static let bodyLandmarkRegionKeyTorso: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeytorso)
- [static let bodyLandmarkRegionKeyRightArm: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyrightarm)
- [static let bodyLandmarkRegionKeyLeftArm: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyleftarm)
- [static let bodyLandmarkRegionKeyRightLeg: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyrightleg)
- [static let bodyLandmarkRegionKeyLeftLeg: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/bodylandmarkregionkeyleftleg)

#### All Regions

- [static let all: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/all)
- [static let point3DGroupKeyAll: VNRecognizedPointGroupKey](/documentation/vision/vnrecognizedpointgroupkey/point3dgroupkeyall)

#### Initializers

- [init(rawValue: String)](/documentation/vision/vnrecognizedpointgroupkey/init(rawvalue:))

### 3D body pose detection

- [Identifying 3D human body poses in images](/documentation/vision/identifying-3d-human-body-poses-in-images)
- [Detecting human body poses in 3D with Vision](/documentation/vision/detecting-human-body-poses-in-3d-with-vision)
- [VNDetectHumanBodyPose3DRequest](/documentation/vision/vndetecthumanbodypose3drequest)

#### Initializing a Request

- [init()](/documentation/vision/vndetecthumanbodypose3drequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vndetecthumanbodypose3drequest/init(completionhandler:))

#### Determining Supported Joints

- [var supportedJointsGroupNames: [VNHumanBodyPose3DObservation.JointsGroupName]](/documentation/vision/vndetecthumanbodypose3drequest/supportedjointsgroupnames)
- [var supportedJointNames: [VNHumanBodyPose3DObservation.JointName]](/documentation/vision/vndetecthumanbodypose3drequest/supportedjointnames)

#### Accessing the Results

- [var results: [VNHumanBodyPose3DObservation]?](/documentation/vision/vndetecthumanbodypose3drequest/results)
- [VNHumanBodyPose3DObservation](/documentation/vision/vnhumanbodypose3dobservation)

#### Accessing Points

- [var availableJointNames: [VNHumanBodyPose3DObservation.JointName]](/documentation/vision/vnhumanbodypose3dobservation/availablejointnames)
- [VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname)

##### Getting the Head Joint Names

- [static let topHead: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/tophead)
- [static let centerHead: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/centerhead)

##### Getting the Arm Joint Names

- [static let centerShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/centershoulder)
- [static let leftShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftshoulder)
- [static let rightShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightshoulder)
- [static let leftElbow: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftelbow)
- [static let rightElbow: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightelbow)
- [static let leftWrist: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftwrist)
- [static let rightWrist: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightwrist)

##### Getting the Leg Joint Names

- [static let leftHip: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/lefthip)
- [static let rightHip: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/righthip)
- [static let leftKnee: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftknee)
- [static let rightKnee: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightknee)
- [static let leftAnkle: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftankle)
- [static let rightAnkle: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightankle)

##### Getting the Root Joint Name

- [static let root: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/root)

##### Getting the Spine

- [static let spine: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/spine)

##### Creating a Joint Name

- [init(rawValue: VNRecognizedPointKey)](/documentation/vision/vnhumanbodypose3dobservation/jointname/init(rawvalue:))
- [var availableJointsGroupNames: [VNHumanBodyPose3DObservation.JointsGroupName]](/documentation/vision/vnhumanbodypose3dobservation/availablejointsgroupnames)
- [VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname)

##### Getting the Group Names

- [static let all: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/all)
- [static let head: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/head)
- [static let leftArm: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/leftarm)
- [static let leftLeg: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/leftleg)
- [static let rightArm: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/rightarm)
- [static let rightLeg: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/rightleg)
- [static let torso: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/torso)

##### Creating a Group Name

- [init(rawValue: VNRecognizedPointGroupKey)](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/init(rawvalue:))
- [func recognizedPoint(VNHumanBodyPose3DObservation.JointName) throws -> VNHumanBodyRecognizedPoint3D](/documentation/vision/vnhumanbodypose3dobservation/recognizedpoint(_:))
- [func recognizedPoints(VNHumanBodyPose3DObservation.JointsGroupName) throws -> [VNHumanBodyPose3DObservation.JointName : VNHumanBodyRecognizedPoint3D]](/documentation/vision/vnhumanbodypose3dobservation/recognizedpoints(_:))

#### Getting the Joint Position

- [func pointInImage(VNHumanBodyPose3DObservation.JointName) throws -> VNPoint](/documentation/vision/vnhumanbodypose3dobservation/pointinimage(_:))

#### Getting the Parent Joint Name

- [func parentJointName(VNHumanBodyPose3DObservation.JointName) -> VNHumanBodyPose3DObservation.JointName?](/documentation/vision/vnhumanbodypose3dobservation/parentjointname(_:))

#### Getting the Body Height

- [var heightEstimation: VNHumanBodyPose3DObservation.HeightEstimation](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.property)
- [VNHumanBodyPose3DObservation.HeightEstimation](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum)

##### Techniques

- [case measured](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum/measured)
- [case reference](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum/reference)
- [case measured](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum/measured)
- [case reference](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum/reference)

##### Creating a Technique

- [init?(rawValue: Int)](/documentation/vision/vnhumanbodypose3dobservation/heightestimation-swift.enum/init(rawvalue:))
- [var bodyHeight: Float](/documentation/vision/vnhumanbodypose3dobservation/bodyheight)

#### Getting the Camera Position

- [var cameraOriginMatrix: simd_float4x4](/documentation/vision/vnhumanbodypose3dobservation/cameraoriginmatrix)
- [func cameraRelativePosition(VNHumanBodyPose3DObservation.JointName) throws -> simd_float4x4](/documentation/vision/vnhumanbodypose3dobservation/camerarelativeposition(_:))
- [VNRecognizedPoints3DObservation](/documentation/vision/vnrecognizedpoints3dobservation)

#### Inspecting the Observation

- [var availableKeys: [VNRecognizedPointKey]](/documentation/vision/vnrecognizedpoints3dobservation/availablekeys)
- [var availableGroupKeys: [VNRecognizedPointGroupKey]](/documentation/vision/vnrecognizedpoints3dobservation/availablegroupkeys)
- [func recognizedPoint(forKey: VNRecognizedPointKey) throws -> VNRecognizedPoint3D](/documentation/vision/vnrecognizedpoints3dobservation/recognizedpoint(forkey:))
- [func recognizedPoints(forGroupKey: VNRecognizedPointGroupKey) throws -> [VNRecognizedPointKey : VNRecognizedPoint3D]](/documentation/vision/vnrecognizedpoints3dobservation/recognizedpoints(forgroupkey:))
- [VNHumanBodyRecognizedPoint3D](/documentation/vision/vnhumanbodyrecognizedpoint3d)

#### Getting the Position

- [var localPosition: simd_float4x4](/documentation/vision/vnhumanbodyrecognizedpoint3d/localposition)

#### Getting the Parent Joint

- [var parentJoint: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodyrecognizedpoint3d/parentjoint)
- [VNPoint3D](/documentation/vision/vnpoint3d)

#### Creating a Point

- [init?(position: simd_float4x4)](/documentation/vision/vnpoint3d/init(position:))

#### Getting the Position

- [var position: simd_float4x4](/documentation/vision/vnpoint3d/position)
- [VNRecognizedPoint3D](/documentation/vision/vnrecognizedpoint3d)

#### Getting the Identifier

- [var identifier: VNRecognizedPointKey](/documentation/vision/vnrecognizedpoint3d/identifier)
- [VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname)

#### Getting the Head Joint Names

- [static let topHead: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/tophead)
- [static let centerHead: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/centerhead)

#### Getting the Arm Joint Names

- [static let centerShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/centershoulder)
- [static let leftShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftshoulder)
- [static let rightShoulder: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightshoulder)
- [static let leftElbow: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftelbow)
- [static let rightElbow: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightelbow)
- [static let leftWrist: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftwrist)
- [static let rightWrist: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightwrist)

#### Getting the Leg Joint Names

- [static let leftHip: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/lefthip)
- [static let rightHip: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/righthip)
- [static let leftKnee: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftknee)
- [static let rightKnee: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightknee)
- [static let leftAnkle: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/leftankle)
- [static let rightAnkle: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/rightankle)

#### Getting the Root Joint Name

- [static let root: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/root)

#### Getting the Spine

- [static let spine: VNHumanBodyPose3DObservation.JointName](/documentation/vision/vnhumanbodypose3dobservation/jointname/spine)

#### Creating a Joint Name

- [init(rawValue: VNRecognizedPointKey)](/documentation/vision/vnhumanbodypose3dobservation/jointname/init(rawvalue:))
- [VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname)

#### Getting the Group Names

- [static let all: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/all)
- [static let head: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/head)
- [static let leftArm: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/leftarm)
- [static let leftLeg: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/leftleg)
- [static let rightArm: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/rightarm)
- [static let rightLeg: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/rightleg)
- [static let torso: VNHumanBodyPose3DObservation.JointsGroupName](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/torso)

#### Creating a Group Name

- [init(rawValue: VNRecognizedPointGroupKey)](/documentation/vision/vnhumanbodypose3dobservation/jointsgroupname/init(rawvalue:))

### Animal detection

- [VNRecognizeAnimalsRequest](/documentation/vision/vnrecognizeanimalsrequest)

#### Accessing the Results

- [var results: [VNRecognizedObjectObservation]?](/documentation/vision/vnrecognizeanimalsrequest/results)

#### Identifying Animals

- [func supportedIdentifiers() throws -> [VNAnimalIdentifier]](/documentation/vision/vnrecognizeanimalsrequest/supportedidentifiers())
- [VNAnimalIdentifier](/documentation/vision/vnanimalidentifier)

##### Animals

- [static let cat: VNAnimalIdentifier](/documentation/vision/vnanimalidentifier/cat)
- [static let dog: VNAnimalIdentifier](/documentation/vision/vnanimalidentifier/dog)

##### Initializers

- [init(rawValue: String)](/documentation/vision/vnanimalidentifier/init(rawvalue:))
- [class func knownAnimalIdentifiers(forRevision: Int) throws -> [VNAnimalIdentifier]](/documentation/vision/vnrecognizeanimalsrequest/knownanimalidentifiers(forrevision:))

#### Identifying Request Revisions

- [let VNRecognizeAnimalsRequestRevision2: Int](/documentation/vision/vnrecognizeanimalsrequestrevision2)
- [let VNRecognizeAnimalsRequestRevision1: Int](/documentation/vision/vnrecognizeanimalsrequestrevision1)

### Animal body pose detection

- [Detecting animal body poses with Vision](/documentation/vision/detecting-animal-body-poses-with-vision)
- [VNDetectAnimalBodyPoseRequest](/documentation/vision/vndetectanimalbodyposerequest)

#### Determining Supported Joints

- [var supportedJointNames: [VNAnimalBodyPoseObservation.JointName]](/documentation/vision/vndetectanimalbodyposerequest/supportedjointnames)
- [var supportedJointsGroupNames: [VNAnimalBodyPoseObservation.JointsGroupName]](/documentation/vision/vndetectanimalbodyposerequest/supportedjointsgroupnames)

#### Accessing the Results

- [var results: [VNAnimalBodyPoseObservation]?](/documentation/vision/vndetectanimalbodyposerequest/results)
- [VNAnimalBodyPoseObservation](/documentation/vision/vnanimalbodyposeobservation)

#### Accessing Points

- [var availableJointNames: [VNAnimalBodyPoseObservation.JointName]](/documentation/vision/vnanimalbodyposeobservation/availablejointnames)
- [VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname)

##### Getting the Head Joint Names

- [static let leftEarTop: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/lefteartop)
- [static let leftEarMiddle: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftearmiddle)
- [static let leftEarBottom: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftearbottom)
- [static let leftEye: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/lefteye)
- [static let neck: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/neck)
- [static let nose: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/nose)
- [static let rightEye: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/righteye)
- [static let rightEarTop: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/righteartop)
- [static let rightEarMiddle: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightearmiddle)
- [static let rightEarBottom: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightearbottom)

##### Getting the Leg Joint Names

- [static let leftBackElbow: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftbackelbow)
- [static let leftFrontElbow: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftfrontelbow)
- [static let rightFrontElbow: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightfrontelbow)
- [static let rightBackElbow: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightbackelbow)
- [static let leftBackKnee: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftbackknee)
- [static let leftFrontKnee: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftfrontknee)
- [static let rightBackKnee: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightbackknee)
- [static let rightFrontKnee: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightfrontknee)
- [static let leftBackPaw: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftbackpaw)
- [static let leftFrontPaw: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/leftfrontpaw)
- [static let rightBackPaw: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightbackpaw)
- [static let rightFrontPaw: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/rightfrontpaw)

##### Getting the Tail Joint Names

- [static let tailTop: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/tailtop)
- [static let tailMiddle: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/tailmiddle)
- [static let tailBottom: VNAnimalBodyPoseObservation.JointName](/documentation/vision/vnanimalbodyposeobservation/jointname/tailbottom)

##### Creating a Joint Name

- [init(rawValue: VNRecognizedPointKey)](/documentation/vision/vnanimalbodyposeobservation/jointname/init(rawvalue:))
- [var availableJointGroupNames: [VNAnimalBodyPoseObservation.JointsGroupName]](/documentation/vision/vnanimalbodyposeobservation/availablejointgroupnames)
- [VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname)

##### Getting the Group Names

- [static let all: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/all)
- [static let forelegs: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/forelegs)
- [static let head: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/head)
- [static let hindlegs: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/hindlegs)
- [static let tail: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/tail)
- [static let trunk: VNAnimalBodyPoseObservation.JointsGroupName](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/trunk)

##### Creating a Group Name

- [init(rawValue: VNRecognizedPointGroupKey)](/documentation/vision/vnanimalbodyposeobservation/jointsgroupname/init(rawvalue:))
- [func recognizedPoint(VNAnimalBodyPoseObservation.JointName) throws -> VNRecognizedPoint](/documentation/vision/vnanimalbodyposeobservation/recognizedpoint(_:))
- [func recognizedPoints(VNAnimalBodyPoseObservation.JointsGroupName) throws -> [VNAnimalBodyPoseObservation.JointName : VNRecognizedPoint]](/documentation/vision/vnanimalbodyposeobservation/recognizedpoints(_:))

### Trajectory detection

- [Identifying Trajectories in Video](/documentation/vision/identifying-trajectories-in-video)
- [Detecting moving objects in a video](/documentation/vision/detecting-moving-objects-in-a-video)
- [VNDetectTrajectoriesRequest](/documentation/vision/vndetecttrajectoriesrequest)

#### Creating a Request

- [init(frameAnalysisSpacing: CMTime, trajectoryLength: Int, completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vndetecttrajectoriesrequest/init(frameanalysisspacing:trajectorylength:completionhandler:))

#### Configuring the Request

- [var targetFrameTime: CMTime](/documentation/vision/vndetecttrajectoriesrequest/targetframetime)
- [var trajectoryLength: Int](/documentation/vision/vndetecttrajectoriesrequest/trajectorylength)
- [var objectMinimumNormalizedRadius: Float](/documentation/vision/vndetecttrajectoriesrequest/objectminimumnormalizedradius)
- [var objectMaximumNormalizedRadius: Float](/documentation/vision/vndetecttrajectoriesrequest/objectmaximumnormalizedradius)
- [var minimumObjectSize: Float](/documentation/vision/vndetecttrajectoriesrequest/minimumobjectsize)
- [var maximumObjectSize: Float](/documentation/vision/vndetecttrajectoriesrequest/maximumobjectsize)

#### Inspecting the Results

- [var results: [VNTrajectoryObservation]?](/documentation/vision/vndetecttrajectoriesrequest/results)
- [VNTrajectoryObservation](/documentation/vision/vntrajectoryobservation)

##### Evaluating an Observation

- [var detectedPoints: [VNPoint]](/documentation/vision/vntrajectoryobservation/detectedpoints)
- [var projectedPoints: [VNPoint]](/documentation/vision/vntrajectoryobservation/projectedpoints)
- [var equationCoefficients: simd_float3](/documentation/vision/vntrajectoryobservation/equationcoefficients)
- [var movingAverageRadius: CGFloat](/documentation/vision/vntrajectoryobservation/movingaverageradius)

#### Identifying Request Revisions

- [let VNDetectTrajectoriesRequestRevision1: Int](/documentation/vision/vndetecttrajectoriesrequestrevision1)

### Contour detection

- [VNDetectContoursRequest](/documentation/vision/vndetectcontoursrequest)

#### Configuring the Request

- [var contrastAdjustment: Float](/documentation/vision/vndetectcontoursrequest/contrastadjustment)
- [var contrastPivot: NSNumber?](/documentation/vision/vndetectcontoursrequest/contrastpivot)
- [var detectsDarkOnLight: Bool](/documentation/vision/vndetectcontoursrequest/detectsdarkonlight)
- [var maximumImageDimension: Int](/documentation/vision/vndetectcontoursrequest/maximumimagedimension)
- [var detectDarkOnLight: Bool](/documentation/vision/vndetectcontoursrequest/detectdarkonlight)

#### Accessing the Results

- [var results: [VNContoursObservation]?](/documentation/vision/vndetectcontoursrequest/results)
- [VNContoursObservation](/documentation/vision/vncontoursobservation)

##### Inspecting the Observation

- [var contourCount: Int](/documentation/vision/vncontoursobservation/contourcount)
- [var normalizedPath: CGPath](/documentation/vision/vncontoursobservation/normalizedpath)
- [var topLevelContours: [VNContour]](/documentation/vision/vncontoursobservation/toplevelcontours)
- [var topLevelContourCount: Int](/documentation/vision/vncontoursobservation/toplevelcontourcount)
- [func contour(at: Int) throws -> VNContour](/documentation/vision/vncontoursobservation/contour(at:)-9on0y)
- [func contour(at: IndexPath) throws -> VNContour](/documentation/vision/vncontoursobservation/contour(at:)-52odo)
- [VNContour](/documentation/vision/vncontour)

###### Inspecting the Contour

- [var aspectRatio: Float](/documentation/vision/vncontour/aspectratio)
- [var indexPath: IndexPath](/documentation/vision/vncontour/indexpath)
- [var normalizedPath: CGPath](/documentation/vision/vncontour/normalizedpath)
- [var pointCount: Int](/documentation/vision/vncontour/pointcount)
- [var normalizedPoints: [simd_float2]](/documentation/vision/vncontour/normalizedpoints-8n2s5)
- [func polygonApproximation(epsilon: Float) throws -> VNContour](/documentation/vision/vncontour/polygonapproximation(epsilon:))

###### Accessing Child Contours

- [var childContourCount: Int](/documentation/vision/vncontour/childcontourcount)
- [var childContours: [VNContour]](/documentation/vision/vncontour/childcontours)
- [func childContour(at: Int) throws -> VNContour](/documentation/vision/vncontour/childcontour(at:))

#### Identifying Request Revisions

- [let VNDetectContourRequestRevision1: Int](/documentation/vision/vndetectcontourrequestrevision1)

### Optical flow

- [VNGenerateOpticalFlowRequest](/documentation/vision/vngenerateopticalflowrequest)

#### Configuring the Request

- [var computationAccuracy: VNGenerateOpticalFlowRequest.ComputationAccuracy](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.property)
- [VNGenerateOpticalFlowRequest.ComputationAccuracy](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum)

##### Accuracy Levels

- [case low](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum/low)
- [case medium](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum/medium)
- [case high](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum/high)
- [case veryHigh](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum/veryhigh)

##### Creating an Accuracy Level

- [init?(rawValue: UInt)](/documentation/vision/vngenerateopticalflowrequest/computationaccuracy-swift.enum/init(rawvalue:))
- [var outputPixelFormat: OSType](/documentation/vision/vngenerateopticalflowrequest/outputpixelformat)
- [var keepNetworkOutput: Bool](/documentation/vision/vngenerateopticalflowrequest/keepnetworkoutput)

#### Accessing the Results

- [var results: [VNPixelBufferObservation]?](/documentation/vision/vngenerateopticalflowrequest/results)

#### Identifying Request Revisions

- [let VNGenerateOpticalFlowRequestRevision2: Int](/documentation/vision/vngenerateopticalflowrequestrevision2)
- [let VNGenerateOpticalFlowRequestRevision1: Int](/documentation/vision/vngenerateopticalflowrequestrevision1)
- [VNTrackOpticalFlowRequest](/documentation/vision/vntrackopticalflowrequest)

#### Creating an Optical Flow

- [init()](/documentation/vision/vntrackopticalflowrequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntrackopticalflowrequest/init(completionhandler:))

#### Configuring the Request

- [var computationAccuracy: VNTrackOpticalFlowRequest.ComputationAccuracy](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.property)
- [VNTrackOpticalFlowRequest.ComputationAccuracy](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum)

##### Options

- [case low](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/low)
- [case medium](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/medium)
- [case high](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/high)
- [case veryHigh](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/veryhigh)
- [case low](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/low)
- [case medium](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/medium)
- [case high](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/high)
- [case veryHigh](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/veryhigh)

##### Creating an Accuracy Option

- [init?(rawValue: UInt)](/documentation/vision/vntrackopticalflowrequest/computationaccuracy-swift.enum/init(rawvalue:))
- [var keepNetworkOutput: Bool](/documentation/vision/vntrackopticalflowrequest/keepnetworkoutput)
- [var outputPixelFormat: OSType](/documentation/vision/vntrackopticalflowrequest/outputpixelformat)

#### Accessing the Results

- [var results: [VNPixelBufferObservation]?](/documentation/vision/vntrackopticalflowrequest/results)

### Barcode detection

- [VNDetectBarcodesRequest](/documentation/vision/vndetectbarcodesrequest)

#### Specifying Symbologies

- [func supportedSymbologies() throws -> [VNBarcodeSymbology]](/documentation/vision/vndetectbarcodesrequest/supportedsymbologies())
- [var symbologies: [VNBarcodeSymbology]](/documentation/vision/vndetectbarcodesrequest/symbologies)
- [var coalesceCompositeSymbologies: Bool](/documentation/vision/vndetectbarcodesrequest/coalescecompositesymbologies)
- [VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology)

##### Supported Symbologies

- [static let aztec: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/aztec-s3va)
- [static let codabar: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/codabar)
- [static let code39: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39-2ggrb)
- [static let code39Checksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39checksum-3jdl6)
- [static let code39FullASCII: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39fullascii-942jj)
- [static let code39FullASCIIChecksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39fullasciichecksum-6700)
- [static let code93: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code93-2geph)
- [static let code93i: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code93i-t5q5)
- [static let code128: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code128-1lkm2)
- [static let dataMatrix: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/datamatrix-6tg7m)
- [static let ean8: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/ean8-9qg0n)
- [static let ean13: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/ean13-7gb2d)
- [static let gs1DataBar: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/gs1databar)
- [static let gs1DataBarExpanded: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/gs1databarexpanded)
- [static let gs1DataBarLimited: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/gs1databarlimited)
- [static let i2of5: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/i2of5-cyk4)
- [static let i2of5Checksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/i2of5checksum-999jm)
- [static let itf14: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/itf14-9mbkq)
- [static let microPDF417: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/micropdf417)
- [static let microQR: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/microqr)
- [static let msiPlessey: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/msiplessey)
- [static let pdf417: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/pdf417-8n3oh)
- [static let qr: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/qr-2l1ve)
- [static let upce: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/upce-1jtoc)

##### Deprecated Symbols

- [static var Aztec: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/aztec-6g0vi)
- [static var Code128: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code128-7spp7)
- [static var Code39: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39-34358)
- [static var Code39Checksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39checksum-2jrn)
- [static var Code39FullASCII: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39fullascii-m5wd)
- [static var Code39FullASCIIChecksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code39fullasciichecksum-5xnfs)
- [static var Code93: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code93-67nn0)
- [static var Code93i: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/code93i-84cmv)
- [static var DataMatrix: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/datamatrix-2fgc9)
- [static var EAN8: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/ean8-4rzbb)
- [static var EAN13: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/ean13-8ir8e)
- [static var I2of5: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/i2of5-1r8e7)
- [static var I2of5Checksum: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/i2of5checksum-832s5)
- [static var ITF14: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/itf14-1wp9s)
- [static var PDF417: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/pdf417-56ney)
- [static var QR: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/qr-2zqax)
- [static var UPCE: VNBarcodeSymbology](/documentation/vision/vnbarcodesymbology/upce-7qps5)

##### Initializers

- [init(rawValue: String)](/documentation/vision/vnbarcodesymbology/init(rawvalue:))
- [class var supportedSymbologies: [VNBarcodeSymbology]](/documentation/vision/vndetectbarcodesrequest/supportedsymbologies)

#### Accessing the Results

- [var results: [VNBarcodeObservation]?](/documentation/vision/vndetectbarcodesrequest/results)
- [VNBarcodeObservation](/documentation/vision/vnbarcodeobservation)

##### Parsing the Payload

- [var payloadStringValue: String?](/documentation/vision/vnbarcodeobservation/payloadstringvalue)
- [var payloadData: Data?](/documentation/vision/vnbarcodeobservation/payloaddata)
- [var supplementalPayloadString: String?](/documentation/vision/vnbarcodeobservation/supplementalpayloadstring)
- [var supplementalPayloadData: Data?](/documentation/vision/vnbarcodeobservation/supplementalpayloaddata)
- [var supplementalCompositeType: VNBarcodeCompositeType](/documentation/vision/vnbarcodeobservation/supplementalcompositetype)
- [var isGS1DataCarrier: Bool](/documentation/vision/vnbarcodeobservation/isgs1datacarrier)

##### Reading Barcode Descriptors

- [var barcodeDescriptor: CIBarcodeDescriptor?](/documentation/vision/vnbarcodeobservation/barcodedescriptor)

##### Identifying Barcode Types

- [var symbology: VNBarcodeSymbology](/documentation/vision/vnbarcodeobservation/symbology)

##### Identifying Barcode Colors

- [var isColorInverted: Bool](/documentation/vision/vnbarcodeobservation/iscolorinverted)

#### Identifying Request Revisions

- [let VNDetectBarcodesRequestRevision3: Int](/documentation/vision/vndetectbarcodesrequestrevision3)
- [let VNDetectBarcodesRequestRevision2: Int](/documentation/vision/vndetectbarcodesrequestrevision2)
- [let VNDetectBarcodesRequestRevision1: Int](/documentation/vision/vndetectbarcodesrequestrevision1)
- [VNBarcodeCompositeType](/documentation/vision/vnbarcodecompositetype)

#### Composite Types

- [case gs1TypeA](/documentation/vision/vnbarcodecompositetype/gs1typea)
- [case gs1TypeB](/documentation/vision/vnbarcodecompositetype/gs1typeb)
- [case gs1TypeC](/documentation/vision/vnbarcodecompositetype/gs1typec)
- [case linked](/documentation/vision/vnbarcodecompositetype/linked)
- [case none](/documentation/vision/vnbarcodecompositetype/none)

#### Creating a Composite Type

- [init?(rawValue: Int)](/documentation/vision/vnbarcodecompositetype/init(rawvalue:))

### Text detection

- [VNDetectTextRectanglesRequest](/documentation/vision/vndetecttextrectanglesrequest)

#### Configuring a Request

- [var reportCharacterBoxes: Bool](/documentation/vision/vndetecttextrectanglesrequest/reportcharacterboxes)

#### Accessing the Results

- [var results: [VNTextObservation]?](/documentation/vision/vndetecttextrectanglesrequest/results)

#### Identifying Request Revisions

- [let VNDetectTextRectanglesRequestRevision1: Int](/documentation/vision/vndetecttextrectanglesrequestrevision1)
- [VNTextObservation](/documentation/vision/vntextobservation)

#### Finding Individual Characters

- [var characterBoxes: [VNRectangleObservation]?](/documentation/vision/vntextobservation/characterboxes)

### Text recognition

- [Recognizing Text in Images](/documentation/vision/recognizing-text-in-images)
- [Structuring Recognized Text on a Document](/documentation/visionkit/structuring_recognized_text_on_a_document)
- [Extracting phone numbers from text in images](/documentation/vision/extracting-phone-numbers-from-text-in-images)
- [Locating and displaying recognized text](/documentation/vision/locating-and-displaying-recognized-text)
- [VNRecognizeTextRequest](/documentation/vision/vnrecognizetextrequest)

#### Customizing Recognition Constraints

- [var minimumTextHeight: Float](/documentation/vision/vnrecognizetextrequest/minimumtextheight)
- [var recognitionLevel: VNRequestTextRecognitionLevel](/documentation/vision/vnrecognizetextrequest/recognitionlevel)
- [VNRequestTextRecognitionLevel](/documentation/vision/vnrequesttextrecognitionlevel)

##### Recognition Levels

- [case fast](/documentation/vision/vnrequesttextrecognitionlevel/fast)
- [case accurate](/documentation/vision/vnrequesttextrecognitionlevel/accurate)

##### Creating a Recognition Level

- [init?(rawValue: Int)](/documentation/vision/vnrequesttextrecognitionlevel/init(rawvalue:))

#### Accessing the Results

- [var results: [VNRecognizedTextObservation]?](/documentation/vision/vnrecognizetextrequest/results)

#### Specifying the Language

- [var automaticallyDetectsLanguage: Bool](/documentation/vision/vnrecognizetextrequest/automaticallydetectslanguage)
- [var recognitionLanguages: [String]](/documentation/vision/vnrecognizetextrequest/recognitionlanguages)
- [var usesLanguageCorrection: Bool](/documentation/vision/vnrecognizetextrequest/useslanguagecorrection)
- [var customWords: [String]](/documentation/vision/vnrecognizetextrequest/customwords)
- [func supportedRecognitionLanguages() throws -> [String]](/documentation/vision/vnrecognizetextrequest/supportedrecognitionlanguages())
- [class func supportedRecognitionLanguages(for: VNRequestTextRecognitionLevel, revision: Int) throws -> [String]](/documentation/vision/vnrecognizetextrequest/supportedrecognitionlanguages(for:revision:))

#### Identifying Request Revisions

- [let VNRecognizeTextRequestRevision3: Int](/documentation/vision/vnrecognizetextrequestrevision3)
- [let VNRecognizeTextRequestRevision2: Int](/documentation/vision/vnrecognizetextrequestrevision2)
- [let VNRecognizeTextRequestRevision1: Int](/documentation/vision/vnrecognizetextrequestrevision1)
- [VNRecognizedTextObservation](/documentation/vision/vnrecognizedtextobservation)

#### Obtaining Recognized Text

- [func topCandidates(Int) -> [VNRecognizedText]](/documentation/vision/vnrecognizedtextobservation/topcandidates(_:))
- [VNRecognizedText](/documentation/vision/vnrecognizedtext)

##### Determining Recognized Text

- [var string: String](/documentation/vision/vnrecognizedtext/string)
- [var confidence: VNConfidence](/documentation/vision/vnrecognizedtext/confidence)

##### Locating Recognized Text

- [func boundingBox(for: Range<String.Index>) throws -> VNRectangleObservation?](/documentation/vision/vnrecognizedtext/boundingbox(for:))

### Object recognition

- [Recognizing Objects in Live Capture](/documentation/vision/recognizing-objects-in-live-capture)
- [Understanding a Dice Roll with Vision and Object Detection](/documentation/coreml/understanding-a-dice-roll-with-vision-and-object-detection)
- [VNRecognizedObjectObservation](/documentation/vision/vnrecognizedobjectobservation)

#### Classifying a Recognized Object

- [var labels: [VNClassificationObservation]](/documentation/vision/vnrecognizedobjectobservation/labels)
- [VNClassificationObservation](/documentation/vision/vnclassificationobservation)

##### Determining Classification

- [var identifier: String](/documentation/vision/vnclassificationobservation/identifier)

##### Measuring Confidence and Precision

- [var hasPrecisionRecallCurve: Bool](/documentation/vision/vnclassificationobservation/hasprecisionrecallcurve)
- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumrecall(_:forprecision:))

### Request progress tracking

- [VNRequestProgressProviding](/documentation/vision/vnrequestprogressproviding)

#### Tracking Progress

- [var progressHandler: VNRequestProgressHandler](/documentation/vision/vnrequestprogressproviding/progresshandler)
- [var indeterminate: Bool](/documentation/vision/vnrequestprogressproviding/indeterminate)
- [VNRequestProgressHandler](/documentation/vision/vnrequestprogresshandler)

### Horizon detection

- [VNDetectHorizonRequest](/documentation/vision/vndetecthorizonrequest)

#### Accessing the Results

- [var results: [VNHorizonObservation]?](/documentation/vision/vndetecthorizonrequest/results)

#### Identifying Request Revisions

- [let VNDetectHorizonRequestRevision1: Int](/documentation/vision/vndetecthorizonrequestrevision1)
- [VNHorizonObservation](/documentation/vision/vnhorizonobservation)

#### Evaluating the Horizon

- [var angle: CGFloat](/documentation/vision/vnhorizonobservation/angle)
- [var transform: CGAffineTransform](/documentation/vision/vnhorizonobservation/transform)
- [func transform(forImageWidth: Int, height: Int) -> CGAffineTransform](/documentation/vision/vnhorizonobservation/transform(forimagewidth:height:))

### Image alignment

- [Aligning Similar Images](/documentation/vision/aligning-similar-images)
- [VNTargetedImageRequest](/documentation/vision/vntargetedimagerequest)

#### Creating a Request

- [init(targetedCGImage: CGImage, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcgimage:options:completionhandler:))
- [init(targetedCGImage: CGImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcgimage:orientation:options:completionhandler:))
- [init(targetedCIImage: CIImage, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedciimage:options:completionhandler:))
- [init(targetedCIImage: CIImage, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedciimage:orientation:options:completionhandler:))
- [init(targetedCVPixelBuffer: CVPixelBuffer, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcvpixelbuffer:options:completionhandler:))
- [init(targetedCVPixelBuffer: CVPixelBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcvpixelbuffer:orientation:options:completionhandler:))
- [init(targetedCMSampleBuffer: CMSampleBuffer, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcmsamplebuffer:options:completionhandler:))
- [init(targetedCMSampleBuffer: CMSampleBuffer, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedcmsamplebuffer:orientation:options:completionhandler:))
- [init(targetedImageData: Data, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedimagedata:options:completionhandler:))
- [init(targetedImageData: Data, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedimagedata:orientation:options:completionhandler:))
- [init(targetedImageURL: URL, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedimageurl:options:completionhandler:))
- [init(targetedImageURL: URL, orientation: CGImagePropertyOrientation, options: [VNImageOption : Any], completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntargetedimagerequest/init(targetedimageurl:orientation:options:completionhandler:))
- [VNImageRegistrationRequest](/documentation/vision/vnimageregistrationrequest)
- [VNTranslationalImageRegistrationRequest](/documentation/vision/vntranslationalimageregistrationrequest)

#### Accessing the Results

- [var results: [VNImageTranslationAlignmentObservation]?](/documentation/vision/vntranslationalimageregistrationrequest/results)
- [VNTrackTranslationalImageRegistrationRequest](/documentation/vision/vntracktranslationalimageregistrationrequest)

#### Creating a Translational Image

- [init()](/documentation/vision/vntracktranslationalimageregistrationrequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntracktranslationalimageregistrationrequest/init(completionhandler:))

#### Accessing the Results

- [var results: [VNImageTranslationAlignmentObservation]?](/documentation/vision/vntracktranslationalimageregistrationrequest/results)
- [VNHomographicImageRegistrationRequest](/documentation/vision/vnhomographicimageregistrationrequest)

#### Accessing the Results

- [var results: [VNImageHomographicAlignmentObservation]?](/documentation/vision/vnhomographicimageregistrationrequest/results)

#### Identifying Request Revisions

- [let VNHomographicImageRegistrationRequestRevision1: Int](/documentation/vision/vnhomographicimageregistrationrequestrevision1)
- [VNTrackHomographicImageRegistrationRequest](/documentation/vision/vntrackhomographicimageregistrationrequest)

#### Creating a Homographic Image

- [init()](/documentation/vision/vntrackhomographicimageregistrationrequest/init())
- [init(completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vntrackhomographicimageregistrationrequest/init(completionhandler:))

#### Accessing the Results

- [var results: [VNImageHomographicAlignmentObservation]?](/documentation/vision/vntrackhomographicimageregistrationrequest/results)
- [VNImageAlignmentObservation](/documentation/vision/vnimagealignmentobservation)
- [VNImageTranslationAlignmentObservation](/documentation/vision/vnimagetranslationalignmentobservation)

#### Determining Alignment

- [var alignmentTransform: CGAffineTransform](/documentation/vision/vnimagetranslationalignmentobservation/alignmenttransform)

#### Identifying Request Revisions

- [let VNTranslationalImageRegistrationRequestRevision1: Int](/documentation/vision/vntranslationalimageregistrationrequestrevision1)
- [VNImageHomographicAlignmentObservation](/documentation/vision/vnimagehomographicalignmentobservation)

#### Accessing the Transform

- [var warpTransform: matrix_float3x3](/documentation/vision/vnimagehomographicalignmentobservation/warptransform)

### Image background removal

- [Applying visual effects to foreground subjects](/documentation/vision/applying-visual-effects-to-foreground-subjects)
- [VNInstanceMaskObservation](/documentation/vision/vninstancemaskobservation)

#### Accessing Instances

- [var allInstances: IndexSet](/documentation/vision/vninstancemaskobservation/allinstances)
- [var instanceMask: CVPixelBuffer](/documentation/vision/vninstancemaskobservation/instancemask)

#### Creating a Mask

- [func generateMask(forInstances: IndexSet) throws -> CVPixelBuffer](/documentation/vision/vninstancemaskobservation/generatemask(forinstances:))
- [func generateMaskedImage(ofInstances: IndexSet, from: VNImageRequestHandler, croppedToInstancesExtent: Bool) throws -> CVPixelBuffer](/documentation/vision/vninstancemaskobservation/generatemaskedimage(ofinstances:from:croppedtoinstancesextent:))
- [func generateScaledMaskForImage(forInstances: IndexSet, from: VNImageRequestHandler) throws -> CVPixelBuffer](/documentation/vision/vninstancemaskobservation/generatescaledmaskforimage(forinstances:from:))
- [VNGenerateForegroundInstanceMaskRequest](/documentation/vision/vngenerateforegroundinstancemaskrequest)

#### Accessing the Results

- [var results: [VNInstanceMaskObservation]?](/documentation/vision/vngenerateforegroundinstancemaskrequest/results)
- [let VNGenerateForegroundInstanceMaskRequestRevision1: Int](/documentation/vision/vngenerateforegroundinstancemaskrequestrevision1)

### Machine learning image analysis

- [Classifying Images with Vision and Core ML](/documentation/coreml/classifying-images-with-vision-and-core-ml)
- [Training a Create ML Model to Classify Flowers](/documentation/vision/training-a-create-ml-model-to-classify-flowers)
- [VNCoreMLRequest](/documentation/vision/vncoremlrequest)

#### Initializing with a Core ML Model

- [convenience init(model: VNCoreMLModel)](/documentation/vision/vncoremlrequest/init(model:))
- [init(model: VNCoreMLModel, completionHandler: VNRequestCompletionHandler?)](/documentation/vision/vncoremlrequest/init(model:completionhandler:))
- [var model: VNCoreMLModel](/documentation/vision/vncoremlrequest/model)
- [VNCoreMLModel](/documentation/vision/vncoremlmodel)

##### Initializing a Model

- [convenience init(for: MLModel) throws](/documentation/vision/vncoremlmodel/init(for:))

##### Providing Features

- [var featureProvider: (any MLFeatureProvider)?](/documentation/vision/vncoremlmodel/featureprovider)
- [var inputImageFeatureName: String](/documentation/vision/vncoremlmodel/inputimagefeaturename)

#### Configuring Image Options

- [var imageCropAndScaleOption: VNImageCropAndScaleOption](/documentation/vision/vncoremlrequest/imagecropandscaleoption)
- [VNImageCropAndScaleOption](/documentation/vision/vnimagecropandscaleoption)

##### Crop and Scale Options

- [case centerCrop](/documentation/vision/vnimagecropandscaleoption/centercrop)
- [case scaleFit](/documentation/vision/vnimagecropandscaleoption/scalefit)
- [case scaleFill](/documentation/vision/vnimagecropandscaleoption/scalefill)
- [case scaleFitRotate90CCW](/documentation/vision/vnimagecropandscaleoption/scalefitrotate90ccw)
- [case scaleFillRotate90CCW](/documentation/vision/vnimagecropandscaleoption/scalefillrotate90ccw)

##### Creating a Scale Option

- [init?(rawValue: UInt)](/documentation/vision/vnimagecropandscaleoption/init(rawvalue:))

#### Identifying Request Revisions

- [let VNCoreMLRequestRevision1: Int](/documentation/vision/vncoremlrequestrevision1)
- [VNClassificationObservation](/documentation/vision/vnclassificationobservation)

#### Determining Classification

- [var identifier: String](/documentation/vision/vnclassificationobservation/identifier)

#### Measuring Confidence and Precision

- [var hasPrecisionRecallCurve: Bool](/documentation/vision/vnclassificationobservation/hasprecisionrecallcurve)
- [func hasMinimumPrecision(Float, forRecall: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumprecision(_:forrecall:))
- [func hasMinimumRecall(Float, forPrecision: Float) -> Bool](/documentation/vision/vnclassificationobservation/hasminimumrecall(_:forprecision:))
- [VNPixelBufferObservation](/documentation/vision/vnpixelbufferobservation)

#### Parsing Observation Content

- [var pixelBuffer: CVPixelBuffer](/documentation/vision/vnpixelbufferobservation/pixelbuffer)
- [var featureName: String?](/documentation/vision/vnpixelbufferobservation/featurename)

#### Getting the supported pixel formats

- [func supportedOutputPixelFormats() throws -> [NSNumber]](/documentation/vision/vngeneratepersonsegmentationrequest/supportedoutputpixelformats())
- [VNCoreMLFeatureValueObservation](/documentation/vision/vncoremlfeaturevalueobservation)

#### Obtaining Feature Values

- [var featureValue: MLFeatureValue](/documentation/vision/vncoremlfeaturevalueobservation/featurevalue)
- [var featureName: String](/documentation/vision/vncoremlfeaturevalueobservation/featurename)

### Coordinate conversion

- [func VNImagePointForNormalizedPoint(CGPoint, Int, Int) -> CGPoint](/documentation/vision/vnimagepointfornormalizedpoint(_:_:_:))
- [func VNNormalizedPointForImagePoint(CGPoint, Int, Int) -> CGPoint](/documentation/vision/vnnormalizedpointforimagepoint(_:_:_:))
- [func VNImagePointForNormalizedPointUsingRegionOfInterest(CGPoint, Int, Int, CGRect) -> CGPoint](/documentation/vision/vnimagepointfornormalizedpointusingregionofinterest(_:_:_:_:))
- [func VNNormalizedPointForImagePointUsingRegionOfInterest(CGPoint, Int, Int, CGRect) -> CGPoint](/documentation/vision/vnnormalizedpointforimagepointusingregionofinterest(_:_:_:_:))
- [func VNImageRectForNormalizedRect(CGRect, Int, Int) -> CGRect](/documentation/vision/vnimagerectfornormalizedrect(_:_:_:))
- [func VNNormalizedRectForImageRect(CGRect, Int, Int) -> CGRect](/documentation/vision/vnnormalizedrectforimagerect(_:_:_:))
- [func VNImageRectForNormalizedRectUsingRegionOfInterest(CGRect, Int, Int, CGRect) -> CGRect](/documentation/vision/vnimagerectfornormalizedrectusingregionofinterest(_:_:_:_:))
- [func VNNormalizedRectForImageRectUsingRegionOfInterest(CGRect, Int, Int, CGRect) -> CGRect](/documentation/vision/vnnormalizedrectforimagerectusingregionofinterest(_:_:_:_:))
- [let VNNormalizedIdentityRect: CGRect](/documentation/vision/vnnormalizedidentityrect)
- [func VNNormalizedRectIsIdentityRect(CGRect) -> Bool](/documentation/vision/vnnormalizedrectisidentityrect(_:))
- [func VNImagePointForFaceLandmarkPoint(vector_float2, CGRect, Int, Int) -> CGPoint](/documentation/vision/vnimagepointforfacelandmarkpoint(_:_:_:_:))
- [func VNNormalizedFaceBoundingBoxPointForLandmarkPoint(vector_float2, CGRect, Int, Int) -> CGPoint](/documentation/vision/vnnormalizedfaceboundingboxpointforlandmarkpoint(_:_:_:_:))

### Utilities

- [VNComputeStage](/documentation/vision/vncomputestage)

#### Get the Compute Stages

- [static let main: VNComputeStage](/documentation/vision/vncomputestage/main)
- [static let postProcessing: VNComputeStage](/documentation/vision/vncomputestage/postprocessing)

#### Create a Compute Stage

- [init(rawValue: String)](/documentation/vision/vncomputestage/init(rawvalue:))
- [VNGeometryUtils](/documentation/vision/vngeometryutils)

#### Calculating Bounding Circles

- [class func boundingCircle(for: VNContour) throws -> VNCircle](/documentation/vision/vngeometryutils/boundingcircle(for:)-423ll)
- [class func boundingCircle(for: [VNPoint]) throws -> VNCircle](/documentation/vision/vngeometryutils/boundingcircle(for:)-9dggv)
- [class func boundingCircle(forSIMDPoints: UnsafePointer<simd_float2>, pointCount: Int) throws -> VNCircle](/documentation/vision/vngeometryutils/boundingcircle(forsimdpoints:pointcount:))

#### Calculating Area and Perimeter

- [class func calculateArea(UnsafeMutablePointer<Double>, for: VNContour, orientedArea: Bool) throws](/documentation/vision/vngeometryutils/calculatearea(_:for:orientedarea:))
- [class func calculatePerimeter(UnsafeMutablePointer<Double>, for: VNContour) throws](/documentation/vision/vngeometryutils/calculateperimeter(_:for:))
- [VNVideoProcessor](/documentation/vision/vnvideoprocessor)

#### Creating a Video Processor

- [init(url: URL)](/documentation/vision/vnvideoprocessor/init(url:))

#### Performing Requests

- [func addRequest(VNRequest, processingOptions: VNVideoProcessor.RequestProcessingOptions) throws](/documentation/vision/vnvideoprocessor/addrequest(_:processingoptions:))
- [VNVideoProcessor.RequestProcessingOptions](/documentation/vision/vnvideoprocessor/requestprocessingoptions)

##### Configuring Options

- [var cadence: VNVideoProcessor.Cadence?](/documentation/vision/vnvideoprocessor/requestprocessingoptions/cadence)
- [VNVideoProcessor.Cadence](/documentation/vision/vnvideoprocessor/cadence)
- [VNVideoProcessor.FrameRateCadence](/documentation/vision/vnvideoprocessor/frameratecadence)

###### Creating a Cadence

- [init(Int)](/documentation/vision/vnvideoprocessor/frameratecadence/init(_:))

###### Inspecting the Frame Rate

- [var frameRate: Int](/documentation/vision/vnvideoprocessor/frameratecadence/framerate)
- [VNVideoProcessor.TimeIntervalCadence](/documentation/vision/vnvideoprocessor/timeintervalcadence)

###### Creating a Cadence

- [init(CFTimeInterval)](/documentation/vision/vnvideoprocessor/timeintervalcadence/init(_:))

###### Inspecting the Time Interval

- [var timeInterval: CFTimeInterval](/documentation/vision/vnvideoprocessor/timeintervalcadence/timeinterval)
- [func removeRequest(VNRequest) throws](/documentation/vision/vnvideoprocessor/removerequest(_:))
- [func analyze(CMTimeRange) throws](/documentation/vision/vnvideoprocessor/analyze(_:))
- [func cancel()](/documentation/vision/vnvideoprocessor/cancel())
- [func add(VNRequest, withProcessingOptions: [VNVideoProcessingOption : Any]) throws](/documentation/vision/vnvideoprocessor/add(_:withprocessingoptions:))

##### Video Processing Options

- [VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption)

###### Options

- [static let frameCadence: VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption/framecadence)
- [static let timeInterval: VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption/timeinterval)

###### Initializers

- [init(rawValue: String)](/documentation/vision/vnvideoprocessingoption/init(rawvalue:))
- [func analyze(with: CMTimeRange) throws](/documentation/vision/vnvideoprocessor/analyze(with:))
- [VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption)

#### Options

- [static let frameCadence: VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption/framecadence)
- [static let timeInterval: VNVideoProcessingOption](/documentation/vision/vnvideoprocessingoption/timeinterval)

#### Initializers

- [init(rawValue: String)](/documentation/vision/vnvideoprocessingoption/init(rawvalue:))

### Common data types

- [VNCircle](/documentation/vision/vncircle)

#### Creating a Circle

- [init(center: VNPoint, radius: Double)](/documentation/vision/vncircle/init(center:radius:))
- [convenience init(center: VNPoint, diameter: Double)](/documentation/vision/vncircle/init(center:diameter:))
- [class var zero: VNCircle](/documentation/vision/vncircle/zero)

#### Inspecting a Circle

- [var center: VNPoint](/documentation/vision/vncircle/center)
- [var diameter: Double](/documentation/vision/vncircle/diameter)
- [var radius: Double](/documentation/vision/vncircle/radius)
- [func contains(VNPoint) -> Bool](/documentation/vision/vncircle/contains(_:))
- [func contains(VNPoint, inCircumferentialRingOfWidth: Double) -> Bool](/documentation/vision/vncircle/contains(_:incircumferentialringofwidth:))
- [VNVector](/documentation/vision/vnvector)

#### Creating a Vector

- [init(byAdding: VNVector, to: VNVector)](/documentation/vision/vnvector/init(byadding:to:))
- [init(bySubtracting: VNVector, from: VNVector)](/documentation/vision/vnvector/init(bysubtracting:from:))
- [init(byMultiplying: VNVector, byScalar: Double)](/documentation/vision/vnvector/init(bymultiplying:byscalar:))
- [convenience init(r: Double, theta: Double)](/documentation/vision/vnvector/init(r:theta:))
- [convenience init(vectorHead: VNPoint, tail: VNPoint)](/documentation/vision/vnvector/init(vectorhead:tail:))
- [init(xComponent: Double, yComponent: Double)](/documentation/vision/vnvector/init(xcomponent:ycomponent:))
- [class var zero: VNVector](/documentation/vision/vnvector/zero)

#### Inspecting a Vector

- [var length: Double](/documentation/vision/vnvector/length)
- [var r: Double](/documentation/vision/vnvector/r)
- [var theta: Double](/documentation/vision/vnvector/theta)
- [var squaredLength: Double](/documentation/vision/vnvector/squaredlength)
- [var x: Double](/documentation/vision/vnvector/x)
- [var y: Double](/documentation/vision/vnvector/y)
- [class func dotProduct(of: VNVector, vector: VNVector) -> Double](/documentation/vision/vnvector/dotproduct(of:vector:))
- [class func unitVector(for: VNVector) -> VNVector](/documentation/vision/vnvector/unitvector(for:))

### Errors

- [let VNErrorDomain: String](/documentation/vision/vnerrordomain)
- [VNErrorCode](/documentation/vision/vnerrorcode)

#### Error Codes

- [case turiCoreErrorCode](/documentation/vision/vnerrorcode/turicoreerrorcode)
- [case OK](/documentation/vision/vnerrorcode/ok)
- [case dataUnavailable](/documentation/vision/vnerrorcode/dataunavailable)
- [case internalError](/documentation/vision/vnerrorcode/internalerror)
- [case invalidArgument](/documentation/vision/vnerrorcode/invalidargument)
- [case invalidFormat](/documentation/vision/vnerrorcode/invalidformat)
- [case invalidImage](/documentation/vision/vnerrorcode/invalidimage)
- [case invalidModel](/documentation/vision/vnerrorcode/invalidmodel)
- [case invalidOperation](/documentation/vision/vnerrorcode/invalidoperation)
- [case invalidOption](/documentation/vision/vnerrorcode/invalidoption)
- [case ioError](/documentation/vision/vnerrorcode/ioerror)
- [case missingOption](/documentation/vision/vnerrorcode/missingoption)
- [case notImplemented](/documentation/vision/vnerrorcode/notimplemented)
- [case operationFailed](/documentation/vision/vnerrorcode/operationfailed)
- [case outOfBoundsError](/documentation/vision/vnerrorcode/outofboundserror)
- [case outOfMemory](/documentation/vision/vnerrorcode/outofmemory)
- [case requestCancelled](/documentation/vision/vnerrorcode/requestcancelled)
- [case timeStampNotFound](/documentation/vision/vnerrorcode/timestampnotfound)
- [case unknownError](/documentation/vision/vnerrorcode/unknownerror)
- [case unsupportedRevision](/documentation/vision/vnerrorcode/unsupportedrevision)
- [case unsupportedRequest](/documentation/vision/vnerrorcode/unsupportedrequest)
- [case unsupportedComputeDevice](/documentation/vision/vnerrorcode/unsupportedcomputedevice)
- [case unsupportedComputeStage](/documentation/vision/vnerrorcode/unsupportedcomputestage)
- [case timeout](/documentation/vision/vnerrorcode/timeout)

#### Creating an Error Code

- [init?(rawValue: Int)](/documentation/vision/vnerrorcode/init(rawvalue:))

### Version and revision numbers

- [var VNVisionVersionNumber: Double](/documentation/vision/vnvisionversionnumber)
- [let VNDetectAnimalBodyPoseRequestRevision1: Int](/documentation/vision/vndetectanimalbodyposerequestrevision1)
- [let VNDetectHumanBodyPose3DRequestRevision1: Int](/documentation/vision/vndetecthumanbodypose3drequestrevision1)
- [let VNTrackHomographicImageRegistrationRequestRevision1: Int](/documentation/vision/vntrackhomographicimageregistrationrequestrevision1)
- [let VNTrackTranslationalImageRegistrationRequestRevision1: Int](/documentation/vision/vntracktranslationalimageregistrationrequestrevision1)
- [let VNTrackOpticalFlowRequestRevision1: Int](/documentation/vision/vntrackopticalflowrequestrevision1)
- [let VNClassifyImageRequestRevision1: Int](/documentation/vision/vnclassifyimagerequestrevision1)
- [let VNClassifyImageRequestRevision2: Int](/documentation/vision/vnclassifyimagerequestrevision2)
- [let VNGenerateObjectnessBasedSaliencyImageRequestRevision2: Int](/documentation/vision/vngenerateobjectnessbasedsaliencyimagerequestrevision2)
- [let VNGenerateAttentionBasedSaliencyImageRequestRevision2: Int](/documentation/vision/vngenerateattentionbasedsaliencyimagerequestrevision2)
- [let VNGenerateImageFeaturePrintRequestRevision1: Int](/documentation/vision/vngenerateimagefeatureprintrequestrevision1)
- [let VNGenerateImageFeaturePrintRequestRevision2: Int](/documentation/vision/vngenerateimagefeatureprintrequestrevision2)
- [let VNDetectFaceCaptureQualityRequestRevision3: Int](/documentation/vision/vndetectfacecapturequalityrequestrevision3)
- [let VNDetectBarcodesRequestRevision4: Int](/documentation/vision/vndetectbarcodesrequestrevision4)
- [let VNCalculateImageAestheticsScoresRequestRevision1: Int](/documentation/vision/vncalculateimageaestheticsscoresrequestrevision1)
- [let VNRequestRevisionUnspecified: Int](/documentation/vision/vnrequestrevisionunspecified)

### Macros

- [Macros](/documentation/vision/vision-macros)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
