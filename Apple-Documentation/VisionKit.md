# VisionKit Documentation

Source: https://sosumi.ai/documentation/visionkit

---
title: VisionKit
source: https://developer.apple.com/documentation/visionkit
timestamp: 2026-02-13T19:03:43.445Z
---

## Content recognition and interaction in images

- [Enabling Live Text interactions with images](/documentation/visionkit/enabling-live-text-interactions-with-images)
- [ImageAnalyzer](/documentation/visionkit/imageanalyzer)

### Handling availability

- [class var isSupported: Bool](/documentation/visionkit/imageanalyzer/issupported)
- [class var supportedTextRecognitionLanguages: [String]](/documentation/visionkit/imageanalyzer/supportedtextrecognitionlanguages)

### Creating image analyzers

- [init()](/documentation/visionkit/imageanalyzer/init())

### Configuring image analyzers

- [ImageAnalyzer.Configuration](/documentation/visionkit/imageanalyzer/configuration)

#### Creating configurations

- [init(ImageAnalyzer.AnalysisTypes)](/documentation/visionkit/imageanalyzer/configuration/init(_:))
- [let analysisTypes: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/configuration/analysistypes)
- [ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes)

##### Specifying types to find

- [static let machineReadableCode: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/machinereadablecode)
- [static let text: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/text)
- [static let visualLookUp: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/visuallookup)

##### Managing sets

- [Set properties and methods](/documentation/visionkit/analysistypes-set-properties-and-methods)

###### Creating sets

- [init(rawValue: UInt)](/documentation/visionkit/imageanalyzer/analysistypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalyzer/analysistypes/rawvalue)

#### Recognizing languages

- [var locales: [String]](/documentation/visionkit/imageanalyzer/configuration/locales)

### Finding items in images

- [func analyze(UIImage, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:configuration:))
- [func analyze(NSImage, orientation: CGImagePropertyOrientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:orientation:configuration:)-5bs2w)
- [func analyze(CGImage, orientation: CGImagePropertyOrientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:orientation:configuration:)-ufrs)
- [func analyze(CVPixelBuffer, orientation: CGImagePropertyOrientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:orientation:configuration:)-2ezqw)
- [func analyze(CIImage, orientation: CGImagePropertyOrientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:orientation:configuration:)-4h43g)
- [func analyze(UIImage, orientation: UIImage.Orientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(_:orientation:configuration:)-fcjz)
- [func analyze(imageAt: URL, orientation: CGImagePropertyOrientation, configuration: ImageAnalyzer.Configuration) async throws -> ImageAnalysis](/documentation/visionkit/imageanalyzer/analyze(imageat:orientation:configuration:))

### Structures

- [ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes)

#### Specifying types to find

- [static let machineReadableCode: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/machinereadablecode)
- [static let text: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/text)
- [static let visualLookUp: ImageAnalyzer.AnalysisTypes](/documentation/visionkit/imageanalyzer/analysistypes/visuallookup)

#### Managing sets

- [Set properties and methods](/documentation/visionkit/analysistypes-set-properties-and-methods)

##### Creating sets

- [init(rawValue: UInt)](/documentation/visionkit/imageanalyzer/analysistypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalyzer/analysistypes/rawvalue)
- [ImageAnalysis](/documentation/visionkit/imageanalysis)

### Checking results

- [func hasResults(for: ImageAnalyzer.AnalysisTypes) -> Bool](/documentation/visionkit/imageanalysis/hasresults(for:))

### Getting the text

- [var transcript: String](/documentation/visionkit/imageanalysis/transcript)
- [ImageAnalysisInteraction](/documentation/visionkit/imageanalysisinteraction)

### Creating an image interaction

- [init()](/documentation/visionkit/imageanalysisinteraction/init())
- [convenience init(any ImageAnalysisInteractionDelegate)](/documentation/visionkit/imageanalysisinteraction/init(_:))

### Configuring an image interaction

- [var delegate: (any ImageAnalysisInteractionDelegate)?](/documentation/visionkit/imageanalysisinteraction/delegate)
- [var analysis: ImageAnalysis?](/documentation/visionkit/imageanalysisinteraction/analysis)
- [var view: UIView?](/documentation/visionkit/imageanalysisinteraction/view)
- [var preferredInteractionTypes: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/preferredinteractiontypes)
- [ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes)

#### Specifying types of interactions

- [static let automatic: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/automatic)
- [static let textSelection: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/textselection)
- [static let dataDetectors: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/datadetectors)
- [static let imageSubject: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/imagesubject)
- [static let visualLookUp: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/visuallookup)
- [static let automaticTextOnly: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/interactiontypes/automatictextonly)

#### Creating an interaction

- [init(rawValue: UInt)](/documentation/visionkit/imageanalysisinteraction/interactiontypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalysisinteraction/interactiontypes/rawvalue)

#### Managing sets

- [Set properties and methods](/documentation/visionkit/interactiontypes-set-properties-and-methods)

##### Creating sets

- [init(rawValue: UInt)](/documentation/visionkit/imageanalysisinteraction/interactiontypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalysisinteraction/interactiontypes/rawvalue)
- [var activeInteractionTypes: ImageAnalysisInteraction.InteractionTypes](/documentation/visionkit/imageanalysisinteraction/activeinteractiontypes)

### Responding to view events

- [func willMove(to: UIView?)](/documentation/visionkit/imageanalysisinteraction/willmove(to:))
- [func didMove(to: UIView?)](/documentation/visionkit/imageanalysisinteraction/didmove(to:))

### Accessing text information

- [var text: String](/documentation/visionkit/imageanalysisinteraction/text)
- [var selectedText: String](/documentation/visionkit/imageanalysisinteraction/selectedtext)
- [var selectedAttributedText: AttributedString](/documentation/visionkit/imageanalysisinteraction/selectedattributedtext)
- [func hasText(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisinteraction/hastext(at:))
- [var hasActiveTextSelection: Bool](/documentation/visionkit/imageanalysisinteraction/hasactivetextselection)
- [func analysisHasText(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisinteraction/analysishastext(at:))
- [func hasDataDetector(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisinteraction/hasdatadetector(at:))

### Managing text selection

- [var selectedRanges: [Range<String.Index>]](/documentation/visionkit/imageanalysisinteraction/selectedranges)
- [func resetTextSelection()](/documentation/visionkit/imageanalysisinteraction/resettextselection())

### Accessing image subjects

- [var subjects: Set<ImageAnalysisInteraction.Subject>](/documentation/visionkit/imageanalysisinteraction/subjects)
- [ImageAnalysisInteraction.Subject](/documentation/visionkit/imageanalysisinteraction/subject)

#### Acquiring the subject image

- [var image: UIImage](/documentation/visionkit/imageanalysisinteraction/subject/image)

#### Locating and sizing the subject

- [var bounds: CGRect](/documentation/visionkit/imageanalysisinteraction/subject/bounds)

#### Serializing a subject

- [func hash(into: inout Hasher)](/documentation/visionkit/imageanalysisinteraction/subject/hash(into:))
- [func image(for: Set<ImageAnalysisInteraction.Subject>) async throws -> UIImage](/documentation/visionkit/imageanalysisinteraction/image(for:))
- [func subject(at: CGPoint) async -> ImageAnalysisInteraction.Subject?](/documentation/visionkit/imageanalysisinteraction/subject(at:))

### Managing image subjects

- [var highlightedSubjects: Set<ImageAnalysisInteraction.Subject>](/documentation/visionkit/imageanalysisinteraction/highlightedsubjects)

### Querying the interface state

- [var liveTextButtonVisible: Bool](/documentation/visionkit/imageanalysisinteraction/livetextbuttonvisible)
- [var isSupplementaryInterfaceHidden: Bool](/documentation/visionkit/imageanalysisinteraction/issupplementaryinterfacehidden)
- [func hasInteractiveItem(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisinteraction/hasinteractiveitem(at:))
- [func hasSupplementaryInterface(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisinteraction/hassupplementaryinterface(at:))
- [var selectableItemsHighlighted: Bool](/documentation/visionkit/imageanalysisinteraction/selectableitemshighlighted)

### Customizing the interface

- [var allowLongPressForDataDetectorsInTextMode: Bool](/documentation/visionkit/imageanalysisinteraction/allowlongpressfordatadetectorsintextmode)
- [func setSupplementaryInterfaceHidden(Bool, animated: Bool)](/documentation/visionkit/imageanalysisinteraction/setsupplementaryinterfacehidden(_:animated:))
- [var supplementaryInterfaceContentInsets: UIEdgeInsets](/documentation/visionkit/imageanalysisinteraction/supplementaryinterfacecontentinsets)
- [var supplementaryInterfaceFont: UIFont?](/documentation/visionkit/imageanalysisinteraction/supplementaryinterfacefont)

### Managing custom image views

- [var contentsRect: CGRect](/documentation/visionkit/imageanalysisinteraction/contentsrect)
- [func setContentsRectNeedsUpdate()](/documentation/visionkit/imageanalysisinteraction/setcontentsrectneedsupdate())

### Errors

- [ImageAnalysisInteraction.SubjectUnavailable](/documentation/visionkit/imageanalysisinteraction/subjectunavailable)

#### Identifying an error cause

- [case imageUnavailable](/documentation/visionkit/imageanalysisinteraction/subjectunavailable/imageunavailable)
- [ImageAnalysisInteractionDelegate](/documentation/visionkit/imageanalysisinteractiondelegate)

### Providing interface details

- [func contentView(for: ImageAnalysisInteraction) -> UIView?](/documentation/visionkit/imageanalysisinteractiondelegate/contentview(for:))
- [func contentsRect(for: ImageAnalysisInteraction) -> CGRect](/documentation/visionkit/imageanalysisinteractiondelegate/contentsrect(for:))
- [func presentingViewController(for: ImageAnalysisInteraction) -> UIViewController?](/documentation/visionkit/imageanalysisinteractiondelegate/presentingviewcontroller(for:))

### Starting the interaction

- [func interaction(ImageAnalysisInteraction, shouldBeginAt: CGPoint, for: ImageAnalysisInteraction.InteractionTypes) -> Bool](/documentation/visionkit/imageanalysisinteractiondelegate/interaction(_:shouldbeginat:for:))

### Tracking interface changes

- [func interaction(ImageAnalysisInteraction, liveTextButtonDidChangeToVisible: Bool)](/documentation/visionkit/imageanalysisinteractiondelegate/interaction(_:livetextbuttondidchangetovisible:))
- [func interaction(ImageAnalysisInteraction, highlightSelectedItemsDidChange: Bool)](/documentation/visionkit/imageanalysisinteractiondelegate/interaction(_:highlightselecteditemsdidchange:))
- [func textSelectionDidChange(ImageAnalysisInteraction)](/documentation/visionkit/imageanalysisinteractiondelegate/textselectiondidchange(_:))
- [ImageAnalysisOverlayView](/documentation/visionkit/imageanalysisoverlayview)

### Creating overlay views

- [convenience init(any ImageAnalysisOverlayViewDelegate)](/documentation/visionkit/imageanalysisoverlayview/init(_:))
- [init(frame: NSRect)](/documentation/visionkit/imageanalysisoverlayview/init(frame:))
- [init?(coder: NSCoder)](/documentation/visionkit/imageanalysisoverlayview/init(coder:))

### Configuring overlay views

- [var delegate: (any ImageAnalysisOverlayViewDelegate)?](/documentation/visionkit/imageanalysisoverlayview/delegate)
- [var analysis: ImageAnalysis?](/documentation/visionkit/imageanalysisoverlayview/analysis)
- [var preferredInteractionTypes: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/preferredinteractiontypes)
- [ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes)

#### Specifying types of interactions

- [static let automatic: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/automatic)
- [static let textSelection: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/textselection)
- [static let dataDetectors: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/datadetectors)
- [static let imageSubject: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/imagesubject)
- [static let visualLookUp: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/visuallookup)
- [static let automaticTextOnly: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/automatictextonly)

#### Creating an interaction

- [init(rawValue: UInt)](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalysisoverlayview/interactiontypes/rawvalue)

#### Managing sets

- [Set properties and methods](/documentation/visionkit/interactiontypes-set-properties-and-methods)

##### Creating sets

- [init(rawValue: UInt)](/documentation/visionkit/imageanalysisinteraction/interactiontypes/init(rawvalue:))
- [var rawValue: UInt](/documentation/visionkit/imageanalysisinteraction/interactiontypes/rawvalue)
- [var trackingImageView: NSImageView?](/documentation/visionkit/imageanalysisoverlayview/trackingimageview)
- [var activeInteractionTypes: ImageAnalysisOverlayView.InteractionTypes](/documentation/visionkit/imageanalysisoverlayview/activeinteractiontypes)

### Responding to view events

- [func viewDidMoveToSuperview()](/documentation/visionkit/imageanalysisoverlayview/viewdidmovetosuperview())

### Accessing text information

- [var text: String](/documentation/visionkit/imageanalysisoverlayview/text)
- [var selectedText: String](/documentation/visionkit/imageanalysisoverlayview/selectedtext)
- [var selectedAttributedText: AttributedString](/documentation/visionkit/imageanalysisoverlayview/selectedattributedtext)
- [var hasActiveTextSelection: Bool](/documentation/visionkit/imageanalysisoverlayview/hasactivetextselection)
- [func analysisHasText(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayview/analysishastext(at:))
- [func hasText(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayview/hastext(at:))
- [func hasDataDetector(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayview/hasdatadetector(at:))

### Managing text selection

- [var selectedRanges: [Range<String.Index>]](/documentation/visionkit/imageanalysisoverlayview/selectedranges)
- [func resetSelection()](/documentation/visionkit/imageanalysisoverlayview/resetselection())

### Accessing image subjects

- [var subjects: Set<ImageAnalysisOverlayView.Subject>](/documentation/visionkit/imageanalysisoverlayview/subjects)
- [ImageAnalysisOverlayView.Subject](/documentation/visionkit/imageanalysisoverlayview/subject)

#### Acquiring the subject image

- [var image: NSImage](/documentation/visionkit/imageanalysisoverlayview/subject/image)

#### Locating and sizing the subject

- [var bounds: CGRect](/documentation/visionkit/imageanalysisoverlayview/subject/bounds)
- [func image(for: Set<ImageAnalysisOverlayView.Subject>) async throws -> NSImage](/documentation/visionkit/imageanalysisoverlayview/image(for:))
- [func subject(at: CGPoint) async -> ImageAnalysisOverlayView.Subject?](/documentation/visionkit/imageanalysisoverlayview/subject(at:))

### Managing image subjects

- [func beginSubjectAnalysisIfNecessary()](/documentation/visionkit/imageanalysisoverlayview/beginsubjectanalysisifnecessary())
- [var highlightedSubjects: Set<ImageAnalysisOverlayView.Subject>](/documentation/visionkit/imageanalysisoverlayview/highlightedsubjects)

### Querying the interface state

- [var liveTextButtonVisible: Bool](/documentation/visionkit/imageanalysisoverlayview/livetextbuttonvisible)
- [var isSupplementaryInterfaceHidden: Bool](/documentation/visionkit/imageanalysisoverlayview/issupplementaryinterfacehidden)
- [func hasInteractiveItem(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayview/hasinteractiveitem(at:))
- [func hasSupplementaryInterface(at: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayview/hassupplementaryinterface(at:))
- [var selectableItemsHighlighted: Bool](/documentation/visionkit/imageanalysisoverlayview/selectableitemshighlighted)

### Customizing the interface

- [func setSupplementaryInterfaceHidden(Bool, animated: Bool)](/documentation/visionkit/imageanalysisoverlayview/setsupplementaryinterfacehidden(_:animated:))
- [var supplementaryInterfaceContentInsets: NSEdgeInsets](/documentation/visionkit/imageanalysisoverlayview/supplementaryinterfacecontentinsets)
- [var supplementaryInterfaceFont: NSFont?](/documentation/visionkit/imageanalysisoverlayview/supplementaryinterfacefont)
- [ImageAnalysisOverlayView.MenuTag](/documentation/visionkit/imageanalysisoverlayview/menutag)

#### Manage Framework-provided menu items

- [static let copyImage: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/copyimage)
- [static let shareImage: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/shareimage)
- [static let copySubject: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/copysubject)
- [static let shareSubject: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/sharesubject)
- [static let lookupItem: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/lookupitem)

#### Create app-defined menu items

- [static let recommendedAppItems: Int](/documentation/visionkit/imageanalysisoverlayview/menutag/recommendedappitems)

### Managing custom image views

- [var contentsRect: CGRect](/documentation/visionkit/imageanalysisoverlayview/contentsrect)
- [func setContentsRectNeedsUpdate()](/documentation/visionkit/imageanalysisoverlayview/setcontentsrectneedsupdate())

### Errors

- [ImageAnalysisOverlayView.SubjectUnavailable](/documentation/visionkit/imageanalysisoverlayview/subjectunavailable)

#### Enumeration Cases

- [case imageUnavailable](/documentation/visionkit/imageanalysisoverlayview/subjectunavailable/imageunavailable)
- [ImageAnalysisOverlayViewDelegate](/documentation/visionkit/imageanalysisoverlayviewdelegate)

### Providing interface details

- [func contentView(for: ImageAnalysisOverlayView) -> NSView?](/documentation/visionkit/imageanalysisoverlayviewdelegate/contentview(for:))
- [func contentsRect(for: ImageAnalysisOverlayView) -> CGRect](/documentation/visionkit/imageanalysisoverlayviewdelegate/contentsrect(for:))

### Starting the interaction

- [func overlayView(ImageAnalysisOverlayView, shouldBeginAt: CGPoint, forAnalysisType: ImageAnalysisOverlayView.InteractionTypes) -> Bool](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:shouldbeginat:foranalysistype:))

### Tracking interface changes

- [func overlayView(ImageAnalysisOverlayView, liveTextButtonDidChangeToVisible: Bool)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:livetextbuttondidchangetovisible:))
- [func overlayView(ImageAnalysisOverlayView, highlightSelectedItemsDidChange: Bool)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:highlightselecteditemsdidchange:))
- [func textSelectionDidChange(ImageAnalysisOverlayView)](/documentation/visionkit/imageanalysisoverlayviewdelegate/textselectiondidchange(_:))

### Responding to key and menu events

- [func overlayView(ImageAnalysisOverlayView, shouldHandleKeyDownEvent: NSEvent) -> Bool](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:shouldhandlekeydownevent:))
- [func overlayView(ImageAnalysisOverlayView, shouldShowMenuForEvent: NSEvent, atPoint: CGPoint) -> Bool](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:shouldshowmenuforevent:atpoint:))
- [func overlayView(ImageAnalysisOverlayView, menu: NSMenu, willHighlight: NSMenuItem?)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:menu:willhighlight:))
- [func overlayView(ImageAnalysisOverlayView, willOpen: NSMenu)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:willopen:))
- [func overlayView(ImageAnalysisOverlayView, didClose: NSMenu)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:didclose:))
- [func overlayView(ImageAnalysisOverlayView, needsUpdate: NSMenu)](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:needsupdate:))
- [func overlayView(ImageAnalysisOverlayView, updatedMenuFor: NSMenu, for: NSEvent, at: CGPoint) -> NSMenu](/documentation/visionkit/imageanalysisoverlayviewdelegate/overlayview(_:updatedmenufor:for:at:))
- [CameraRegionView](/documentation/visionkit/cameraregionview)

### Creating a view

- [init(isContrastAndVibrancyEnhancementEnabled: Bool, pixelBufferProcessor: ((Result<CameraRegionView.PixelBufferProcessingContext, any Error>) async -> CVReadOnlyPixelBuffer?)?)](/documentation/visionkit/cameraregionview/init(iscontrastandvibrancyenhancementenabled:pixelbufferprocessor:))

### Setting up frame processing in your view

- [CameraRegionView.PixelBufferProcessingContext](/documentation/visionkit/cameraregionview/pixelbufferprocessingcontext)

#### Specifying the context properties

- [let pixelBuffer: CVReadOnlyPixelBuffer](/documentation/visionkit/cameraregionview/pixelbufferprocessingcontext/pixelbuffer)
- [let timestamp: TimeInterval](/documentation/visionkit/cameraregionview/pixelbufferprocessingcontext/timestamp)

## Barcode and text scanning through the camera

- [Scanning data with the camera](/documentation/visionkit/scanning-data-with-the-camera)
- [DataScannerViewController](/documentation/visionkit/datascannerviewcontroller)

### Handling availability

- [class var isSupported: Bool](/documentation/visionkit/datascannerviewcontroller/issupported)
- [class var isAvailable: Bool](/documentation/visionkit/datascannerviewcontroller/isavailable)
- [class var supportedTextRecognitionLanguages: [String]](/documentation/visionkit/datascannerviewcontroller/supportedtextrecognitionlanguages)
- [DataScannerViewController.ScanningUnavailable](/documentation/visionkit/datascannerviewcontroller/scanningunavailable)

#### Unavailable errors

- [case unsupported](/documentation/visionkit/datascannerviewcontroller/scanningunavailable/unsupported)
- [case cameraRestricted](/documentation/visionkit/datascannerviewcontroller/scanningunavailable/camerarestricted)

### Creating data scanners

- [init(recognizedDataTypes: Set<DataScannerViewController.RecognizedDataType>, qualityLevel: DataScannerViewController.QualityLevel, recognizesMultipleItems: Bool, isHighFrameRateTrackingEnabled: Bool, isPinchToZoomEnabled: Bool, isGuidanceEnabled: Bool, isHighlightingEnabled: Bool)](/documentation/visionkit/datascannerviewcontroller/init(recognizeddatatypes:qualitylevel:recognizesmultipleitems:ishighframeratetrackingenabled:ispinchtozoomenabled:isguidanceenabled:ishighlightingenabled:))
- [let recognizedDataTypes: Set<DataScannerViewController.RecognizedDataType>](/documentation/visionkit/datascannerviewcontroller/recognizeddatatypes)
- [DataScannerViewController.RecognizedDataType](/documentation/visionkit/datascannerviewcontroller/recognizeddatatype)

#### Recognizing text

- [static func text(languages: [String], textContentType: DataScannerViewController.TextContentType?) -> DataScannerViewController.RecognizedDataType](/documentation/visionkit/datascannerviewcontroller/recognizeddatatype/text(languages:textcontenttype:))
- [DataScannerViewController.TextContentType](/documentation/visionkit/datascannerviewcontroller/textcontenttype)

##### Identifying content types

- [case URL](/documentation/visionkit/datascannerviewcontroller/textcontenttype/url)
- [case dateTimeDuration](/documentation/visionkit/datascannerviewcontroller/textcontenttype/datetimeduration)
- [case emailAddress](/documentation/visionkit/datascannerviewcontroller/textcontenttype/emailaddress)
- [case flightNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/flightnumber)
- [case fullStreetAddress](/documentation/visionkit/datascannerviewcontroller/textcontenttype/fullstreetaddress)
- [case shipmentTrackingNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/shipmenttrackingnumber)
- [case telephoneNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/telephonenumber)
- [case currency](/documentation/visionkit/datascannerviewcontroller/textcontenttype/currency)

#### Recognizing machine-readable codes

- [static func barcode(symbologies: [VNBarcodeSymbology]) -> DataScannerViewController.RecognizedDataType](/documentation/visionkit/datascannerviewcontroller/recognizeddatatype/barcode(symbologies:))

#### Hashing and comparing

- [func hash(into: inout Hasher)](/documentation/visionkit/datascannerviewcontroller/recognizeddatatype/hash(into:))
- [static func == (DataScannerViewController.RecognizedDataType, DataScannerViewController.RecognizedDataType) -> Bool](/documentation/visionkit/datascannerviewcontroller/recognizeddatatype/==(_:_:))

### Configuring data scanners

- [var delegate: (any DataScannerViewControllerDelegate)?](/documentation/visionkit/datascannerviewcontroller/delegate)
- [let qualityLevel: DataScannerViewController.QualityLevel](/documentation/visionkit/datascannerviewcontroller/qualitylevel-swift.property)
- [DataScannerViewController.QualityLevel](/documentation/visionkit/datascannerviewcontroller/qualitylevel-swift.enum)

#### Identifying quality levels

- [case balanced](/documentation/visionkit/datascannerviewcontroller/qualitylevel-swift.enum/balanced)
- [case fast](/documentation/visionkit/datascannerviewcontroller/qualitylevel-swift.enum/fast)
- [case accurate](/documentation/visionkit/datascannerviewcontroller/qualitylevel-swift.enum/accurate)
- [let recognizesMultipleItems: Bool](/documentation/visionkit/datascannerviewcontroller/recognizesmultipleitems)
- [let isHighFrameRateTrackingEnabled: Bool](/documentation/visionkit/datascannerviewcontroller/ishighframeratetrackingenabled)
- [let isPinchToZoomEnabled: Bool](/documentation/visionkit/datascannerviewcontroller/ispinchtozoomenabled)
- [let isGuidanceEnabled: Bool](/documentation/visionkit/datascannerviewcontroller/isguidanceenabled)
- [let isHighlightingEnabled: Bool](/documentation/visionkit/datascannerviewcontroller/ishighlightingenabled)

### Zooming

- [var zoomFactor: Double](/documentation/visionkit/datascannerviewcontroller/zoomfactor)
- [var minZoomFactor: Double](/documentation/visionkit/datascannerviewcontroller/minzoomfactor)
- [var maxZoomFactor: Double](/documentation/visionkit/datascannerviewcontroller/maxzoomfactor)

### Scanning and recognizing items

- [func startScanning() throws](/documentation/visionkit/datascannerviewcontroller/startscanning())
- [func stopScanning()](/documentation/visionkit/datascannerviewcontroller/stopscanning())
- [var isScanning: Bool](/documentation/visionkit/datascannerviewcontroller/isscanning)
- [var recognizedItems: AsyncStream<[RecognizedItem]>](/documentation/visionkit/datascannerviewcontroller/recognizeditems)

### Capturing photos

- [func capturePhoto() async throws -> UIImage](/documentation/visionkit/datascannerviewcontroller/capturephoto())

### Customizing the interface

- [var overlayContainerView: UIView](/documentation/visionkit/datascannerviewcontroller/overlaycontainerview)
- [var regionOfInterest: CGRect?](/documentation/visionkit/datascannerviewcontroller/regionofinterest)

### Responding to view controller events

- [func loadView()](/documentation/visionkit/datascannerviewcontroller/loadview())
- [func viewDidLoad()](/documentation/visionkit/datascannerviewcontroller/viewdidload())
- [func viewWillAppear(Bool)](/documentation/visionkit/datascannerviewcontroller/viewwillappear(_:))
- [func viewDidDisappear(Bool)](/documentation/visionkit/datascannerviewcontroller/viewdiddisappear(_:))
- [func removeFromParent()](/documentation/visionkit/datascannerviewcontroller/removefromparent())

### Enumerations

- [DataScannerViewController.TextContentType](/documentation/visionkit/datascannerviewcontroller/textcontenttype)

#### Identifying content types

- [case URL](/documentation/visionkit/datascannerviewcontroller/textcontenttype/url)
- [case dateTimeDuration](/documentation/visionkit/datascannerviewcontroller/textcontenttype/datetimeduration)
- [case emailAddress](/documentation/visionkit/datascannerviewcontroller/textcontenttype/emailaddress)
- [case flightNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/flightnumber)
- [case fullStreetAddress](/documentation/visionkit/datascannerviewcontroller/textcontenttype/fullstreetaddress)
- [case shipmentTrackingNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/shipmenttrackingnumber)
- [case telephoneNumber](/documentation/visionkit/datascannerviewcontroller/textcontenttype/telephonenumber)
- [case currency](/documentation/visionkit/datascannerviewcontroller/textcontenttype/currency)
- [DataScannerViewControllerDelegate](/documentation/visionkit/datascannerviewcontrollerdelegate)

### Customizing highlighting

- [func dataScanner(DataScannerViewController, didAdd: [RecognizedItem], allItems: [RecognizedItem])](/documentation/visionkit/datascannerviewcontrollerdelegate/datascanner(_:didadd:allitems:))
- [func dataScanner(DataScannerViewController, didUpdate: [RecognizedItem], allItems: [RecognizedItem])](/documentation/visionkit/datascannerviewcontrollerdelegate/datascanner(_:didupdate:allitems:))
- [func dataScanner(DataScannerViewController, didRemove: [RecognizedItem], allItems: [RecognizedItem])](/documentation/visionkit/datascannerviewcontrollerdelegate/datascanner(_:didremove:allitems:))

### Zooming

- [func dataScannerDidZoom(DataScannerViewController)](/documentation/visionkit/datascannerviewcontrollerdelegate/datascannerdidzoom(_:))

### Tapping items

- [func dataScanner(DataScannerViewController, didTapOn: RecognizedItem)](/documentation/visionkit/datascannerviewcontrollerdelegate/datascanner(_:didtapon:))

### Handling errors

- [func dataScanner(DataScannerViewController, becameUnavailableWithError: DataScannerViewController.ScanningUnavailable)](/documentation/visionkit/datascannerviewcontrollerdelegate/datascanner(_:becameunavailablewitherror:))
- [RecognizedItem](/documentation/visionkit/recognizeditem)

### Machine-readable items

- [case barcode(RecognizedItem.Barcode)](/documentation/visionkit/recognizeditem/barcode(_:))
- [RecognizedItem.Barcode](/documentation/visionkit/recognizeditem/barcode)

#### Getting payloads

- [var payloadStringValue: String?](/documentation/visionkit/recognizeditem/barcode/payloadstringvalue)

#### Locating barcodes

- [var bounds: RecognizedItem.Bounds](/documentation/visionkit/recognizeditem/barcode/bounds)
- [var observation: VNBarcodeObservation](/documentation/visionkit/recognizeditem/barcode/observation)

#### Identifying barcodes

- [var id: UUID](/documentation/visionkit/recognizeditem/barcode/id)

### Text items

- [case text(RecognizedItem.Text)](/documentation/visionkit/recognizeditem/text(_:))
- [RecognizedItem.Text](/documentation/visionkit/recognizeditem/text)

#### Getting text strings

- [var transcript: String](/documentation/visionkit/recognizeditem/text/transcript)

#### Locating text

- [var bounds: RecognizedItem.Bounds](/documentation/visionkit/recognizeditem/text/bounds)
- [var observation: VNRecognizedTextObservation](/documentation/visionkit/recognizeditem/text/observation)

#### Identifying text

- [var id: UUID](/documentation/visionkit/recognizeditem/text/id)

### Item location

- [var bounds: RecognizedItem.Bounds](/documentation/visionkit/recognizeditem/bounds-swift.property)
- [RecognizedItem.Bounds](/documentation/visionkit/recognizeditem/bounds-swift.struct)

#### Getting the corners of items

- [var topLeft: CGPoint](/documentation/visionkit/recognizeditem/bounds-swift.struct/topleft)
- [var topRight: CGPoint](/documentation/visionkit/recognizeditem/bounds-swift.struct/topright)
- [var bottomRight: CGPoint](/documentation/visionkit/recognizeditem/bounds-swift.struct/bottomright)
- [var bottomLeft: CGPoint](/documentation/visionkit/recognizeditem/bounds-swift.struct/bottomleft)

### Item identification

- [var id: UUID](/documentation/visionkit/recognizeditem/id)

## Document scanning through the camera

- [Structuring Recognized Text on a Document](/documentation/visionkit/structuring_recognized_text_on_a_document)
- [VNDocumentCameraViewController](/documentation/visionkit/vndocumentcameraviewcontroller)

### Supporting the document camera

- [var delegate: (any VNDocumentCameraViewControllerDelegate)?](/documentation/visionkit/vndocumentcameraviewcontroller/delegate)
- [class var isSupported: Bool](/documentation/visionkit/vndocumentcameraviewcontroller/issupported)
- [VNDocumentCameraViewControllerDelegate](/documentation/visionkit/vndocumentcameraviewcontrollerdelegate)

### Determining scan results

- [func documentCameraViewController(VNDocumentCameraViewController, didFinishWith: VNDocumentCameraScan)](/documentation/visionkit/vndocumentcameraviewcontrollerdelegate/documentcameraviewcontroller(_:didfinishwith:))
- [func documentCameraViewControllerDidCancel(VNDocumentCameraViewController)](/documentation/visionkit/vndocumentcameraviewcontrollerdelegate/documentcameraviewcontrollerdidcancel(_:))
- [func documentCameraViewController(VNDocumentCameraViewController, didFailWithError: any Error)](/documentation/visionkit/vndocumentcameraviewcontrollerdelegate/documentcameraviewcontroller(_:didfailwitherror:))
- [VNDocumentCameraScan](/documentation/visionkit/vndocumentcamerascan)

### Reading the scanned document

- [var title: String](/documentation/visionkit/vndocumentcamerascan/title)
- [var pageCount: Int](/documentation/visionkit/vndocumentcamerascan/pagecount)
- [func imageOfPage(at: Int) -> UIImage](/documentation/visionkit/vndocumentcamerascan/imageofpage(at:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
