# PaperKit Documentation

Source: https://sosumi.ai/documentation/paperkit

---
title: PaperKit
source: https://developer.apple.com/documentation/paperkit
timestamp: 2026-02-13T19:00:22.554Z
---

## View controllers

- [PaperMarkupViewController](/documentation/paperkit/papermarkupviewcontroller)

### Protocols

- [PaperMarkupViewController.Delegate](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.protocol)

#### Instance Methods

- [func paperMarkupViewControllerDidBeginDrawing(PaperMarkupViewController)](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.protocol/papermarkupviewcontrollerdidbegindrawing(_:))
- [func paperMarkupViewControllerDidChangeContentVisibleFrame(PaperMarkupViewController)](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.protocol/papermarkupviewcontrollerdidchangecontentvisibleframe(_:))
- [func paperMarkupViewControllerDidChangeMarkup(PaperMarkupViewController)](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.protocol/papermarkupviewcontrollerdidchangemarkup(_:))
- [func paperMarkupViewControllerDidChangeSelection(PaperMarkupViewController)](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.protocol/papermarkupviewcontrollerdidchangeselection(_:))

### Initializers

- [init(markup: PaperMarkup?, supportedFeatureSet: FeatureSet)](/documentation/paperkit/papermarkupviewcontroller/init(markup:supportedfeatureset:))

### Instance Properties

- [var acceptsFirstResponder: Bool](/documentation/paperkit/papermarkupviewcontroller/acceptsfirstresponder)
- [var canBecomeFirstResponder: Bool](/documentation/paperkit/papermarkupviewcontroller/canbecomefirstresponder)
- [var contentView: UIView?](/documentation/paperkit/papermarkupviewcontroller/contentview-4aeda)
- [var contentView: NSView?](/documentation/paperkit/papermarkupviewcontroller/contentview-4hbkf)
- [var contentVisibleFrame: CGRect](/documentation/paperkit/papermarkupviewcontroller/contentvisibleframe)
- [var delegate: (any PaperMarkupViewController.Delegate)?](/documentation/paperkit/papermarkupviewcontroller/delegate-swift.property)
- [var directTouchAutomaticallyDraws: Bool](/documentation/paperkit/papermarkupviewcontroller/directtouchautomaticallydraws)
- [var directTouchMode: PaperMarkupViewController.TouchMode](/documentation/paperkit/papermarkupviewcontroller/directtouchmode)
- [var drawingTool: any PKTool](/documentation/paperkit/papermarkupviewcontroller/drawingtool)
- [var indirectPointerTouchMode: PaperMarkupViewController.TouchMode](/documentation/paperkit/papermarkupviewcontroller/indirectpointertouchmode)
- [var isEditable: Bool](/documentation/paperkit/papermarkupviewcontroller/iseditable)
- [var isRulerActive: Bool](/documentation/paperkit/papermarkupviewcontroller/isruleractive)
- [var markup: PaperMarkup?](/documentation/paperkit/papermarkupviewcontroller/markup)
- [var selectedMarkup: PaperMarkup](/documentation/paperkit/papermarkupviewcontroller/selectedmarkup)
- [var showsHorizontalScrollIndicator: Bool](/documentation/paperkit/papermarkupviewcontroller/showshorizontalscrollindicator)
- [var showsVerticalScrollIndicator: Bool](/documentation/paperkit/papermarkupviewcontroller/showsverticalscrollindicator)
- [var supportedFeatureSet: FeatureSet](/documentation/paperkit/papermarkupviewcontroller/supportedfeatureset)
- [var undoManager: UndoManager?](/documentation/paperkit/papermarkupviewcontroller/undomanager)
- [var zoomRange: ClosedRange<CGFloat>](/documentation/paperkit/papermarkupviewcontroller/zoomrange)

### Instance Methods

- [func loadView()](/documentation/paperkit/papermarkupviewcontroller/loadview())
- [func setContentVisibleFrame(CGRect, animated: Bool)](/documentation/paperkit/papermarkupviewcontroller/setcontentvisibleframe(_:animated:))
- [func suggestedFrameForInserting(contentInFrame: CGRect) -> CGRect](/documentation/paperkit/papermarkupviewcontroller/suggestedframeforinserting(contentinframe:))
- [func viewDidAppear()](/documentation/paperkit/papermarkupviewcontroller/viewdidappear())
- [func viewDidLayout()](/documentation/paperkit/papermarkupviewcontroller/viewdidlayout())
- [func viewDidLoad()](/documentation/paperkit/papermarkupviewcontroller/viewdidload())

### Enumerations

- [PaperMarkupViewController.TouchMode](/documentation/paperkit/papermarkupviewcontroller/touchmode)

#### Enumeration Cases

- [case drawing](/documentation/paperkit/papermarkupviewcontroller/touchmode/drawing)
- [case selection](/documentation/paperkit/papermarkupviewcontroller/touchmode/selection)
- [MarkupEditViewController](/documentation/paperkit/markupeditviewcontroller)

### Protocols

- [MarkupEditViewController.Delegate](/documentation/paperkit/markupeditviewcontroller/delegate-swift.protocol)

#### Instance Methods

- [func markupEditViewController(MarkupEditViewController, insertNewContents: PaperMarkup)](/documentation/paperkit/markupeditviewcontroller/delegate-swift.protocol/markupeditviewcontroller(_:insertnewcontents:))
- [func markupEditViewController(MarkupEditViewController, insertNewLineWithStartMarker: Bool, endMarker: Bool)](/documentation/paperkit/markupeditviewcontroller/delegate-swift.protocol/markupeditviewcontroller(_:insertnewlinewithstartmarker:endmarker:))
- [func markupEditViewController(MarkupEditViewController, insertNewShape: ShapeConfiguration.Shape)](/documentation/paperkit/markupeditviewcontroller/delegate-swift.protocol/markupeditviewcontroller(_:insertnewshape:))
- [func markupEditViewControllerInsertNewTextbox(MarkupEditViewController)](/documentation/paperkit/markupeditviewcontroller/delegate-swift.protocol/markupeditviewcontrollerinsertnewtextbox(_:))

### Initializers

- [init(supportedFeatureSet: FeatureSet, additionalActions: [UIMenuElement])](/documentation/paperkit/markupeditviewcontroller/init(supportedfeatureset:additionalactions:))

### Instance Properties

- [var delegate: (any MarkupEditViewController.Delegate)?](/documentation/paperkit/markupeditviewcontroller/delegate-swift.property)
- [let supportedFeatureSet: FeatureSet](/documentation/paperkit/markupeditviewcontroller/supportedfeatureset)

### Instance Methods

- [func viewDidLoad()](/documentation/paperkit/markupeditviewcontroller/viewdidload())
- [MarkupToolbarViewController](/documentation/paperkit/markuptoolbarviewcontroller)

### Protocols

- [MarkupToolbarViewController.Delegate](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol)

#### Instance Methods

- [func markupToolbarViewController(MarkupToolbarViewController, insertNewContents: PaperMarkup)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontroller(_:insertnewcontents:))
- [func markupToolbarViewController(MarkupToolbarViewController, insertNewLineWithStartMarker: Bool, endMarker: Bool)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontroller(_:insertnewlinewithstartmarker:endmarker:))
- [func markupToolbarViewController(MarkupToolbarViewController, insertNewShape: ShapeConfiguration.Shape)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontroller(_:insertnewshape:))
- [func markupToolbarViewControllerInsertNewTextbox(MarkupToolbarViewController)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontrollerinsertnewtextbox(_:))
- [func markupToolbarViewControllerSelectedDrawingToolChanged(MarkupToolbarViewController)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontrollerselecteddrawingtoolchanged(_:))
- [func markupToolbarViewControllerSelectedIndirectPointerTouchModeChanged(MarkupToolbarViewController)](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.protocol/markuptoolbarviewcontrollerselectedindirectpointertouchmodechanged(_:))

### Initializers

- [init?(coder: NSCoder)](/documentation/paperkit/markuptoolbarviewcontroller/init(coder:))
- [init(supportedFeatureSet: FeatureSet)](/documentation/paperkit/markuptoolbarviewcontroller/init(supportedfeatureset:))

### Instance Properties

- [var delegate: (any MarkupToolbarViewController.Delegate)?](/documentation/paperkit/markuptoolbarviewcontroller/delegate-swift.property)
- [var indirectPointerTouchModes: [PaperMarkupViewController.TouchMode]](/documentation/paperkit/markuptoolbarviewcontroller/indirectpointertouchmodes)
- [var selectedDrawingTool: any PKTool](/documentation/paperkit/markuptoolbarviewcontroller/selecteddrawingtool)
- [var selectedDrawingToolItem: PKToolPickerItem](/documentation/paperkit/markuptoolbarviewcontroller/selecteddrawingtoolitem)
- [var selectedIndirectPointerTouchMode: PaperMarkupViewController.TouchMode](/documentation/paperkit/markuptoolbarviewcontroller/selectedindirectpointertouchmode)
- [let supportedFeatureSet: FeatureSet](/documentation/paperkit/markuptoolbarviewcontroller/supportedfeatureset)

### Instance Methods

- [func viewDidLoad()](/documentation/paperkit/markuptoolbarviewcontroller/viewdidload())

## Configuration

- [FeatureSet](/documentation/paperkit/featureset)

### Structures

- [FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.struct)

#### Type Properties

- [static let all: FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.struct/all)
- [static let double: FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.struct/double)
- [static let plain: FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.struct/plain)
- [static let single: FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.struct/single)

### Instance Properties

- [var colorMaximumLinearExposure: CGFloat](/documentation/paperkit/featureset/colormaximumlinearexposure)
- [var contentVersion: FeatureSet.ContentVersion](/documentation/paperkit/featureset/contentversion-swift.property)
- [var features: Set<FeatureSet.Feature>](/documentation/paperkit/featureset/features)
- [var inks: Set<PKInkingTool.InkType>](/documentation/paperkit/featureset/inks)
- [var lineMarkerPositions: FeatureSet.LineMarkerPositions](/documentation/paperkit/featureset/linemarkerpositions-swift.property)
- [var shapes: Set<ShapeConfiguration.Shape>](/documentation/paperkit/featureset/shapes)

### Instance Methods

- [func contains(FeatureSet.Feature) -> Bool](/documentation/paperkit/featureset/contains(_:))
- [func insert(FeatureSet.Feature)](/documentation/paperkit/featureset/insert(_:))
- [func isSubset(of: FeatureSet) -> Bool](/documentation/paperkit/featureset/issubset(of:))
- [func remove(FeatureSet.Feature)](/documentation/paperkit/featureset/remove(_:))

### Type Properties

- [static var empty: FeatureSet](/documentation/paperkit/featureset/empty)
- [static var latest: FeatureSet](/documentation/paperkit/featureset/latest)
- [static var version1: FeatureSet](/documentation/paperkit/featureset/version1)

### Enumerations

- [FeatureSet.ContentVersion](/documentation/paperkit/featureset/contentversion-swift.enum)

#### Enumeration Cases

- [case version1](/documentation/paperkit/featureset/contentversion-swift.enum/version1)

#### Instance Properties

- [var pencilKitContentVersion: PKContentVersion](/documentation/paperkit/featureset/contentversion-swift.enum/pencilkitcontentversion)

#### Type Properties

- [static var latest: FeatureSet.ContentVersion](/documentation/paperkit/featureset/contentversion-swift.enum/latest)
- [FeatureSet.Feature](/documentation/paperkit/featureset/feature)

#### Enumeration Cases

- [case drawing](/documentation/paperkit/featureset/feature/drawing)
- [case images](/documentation/paperkit/featureset/feature/images)
- [case links](/documentation/paperkit/featureset/feature/links)
- [case loupes](/documentation/paperkit/featureset/feature/loupes)
- [case shapeFills](/documentation/paperkit/featureset/feature/shapefills)
- [case shapeOpacity](/documentation/paperkit/featureset/feature/shapeopacity)
- [case shapeStrokes](/documentation/paperkit/featureset/feature/shapestrokes)
- [case stickers](/documentation/paperkit/featureset/feature/stickers)
- [case text](/documentation/paperkit/featureset/feature/text)
- [ShapeConfiguration](/documentation/paperkit/shapeconfiguration)

### Initializers

- [init(type: ShapeConfiguration.Shape, fillColor: CGColor?, strokeColor: CGColor?, lineWidth: CGFloat)](/documentation/paperkit/shapeconfiguration/init(type:fillcolor:strokecolor:linewidth:))

### Instance Properties

- [var fillColor: CGColor?](/documentation/paperkit/shapeconfiguration/fillcolor)
- [var lineWidth: CGFloat](/documentation/paperkit/shapeconfiguration/linewidth)
- [var strokeColor: CGColor?](/documentation/paperkit/shapeconfiguration/strokecolor)
- [var type: ShapeConfiguration.Shape](/documentation/paperkit/shapeconfiguration/type)

### Enumerations

- [ShapeConfiguration.Shape](/documentation/paperkit/shapeconfiguration/shape)

#### Enumeration Cases

- [case arrowShape](/documentation/paperkit/shapeconfiguration/shape/arrowshape)
- [case chatBubble](/documentation/paperkit/shapeconfiguration/shape/chatbubble)
- [case ellipse](/documentation/paperkit/shapeconfiguration/shape/ellipse)
- [case line](/documentation/paperkit/shapeconfiguration/shape/line)
- [case rectangle](/documentation/paperkit/shapeconfiguration/shape/rectangle)
- [case regularPolygon](/documentation/paperkit/shapeconfiguration/shape/regularpolygon)
- [case roundedRectangle](/documentation/paperkit/shapeconfiguration/shape/roundedrectangle)
- [case star](/documentation/paperkit/shapeconfiguration/shape/star)
- [RenderingOptions](/documentation/paperkit/renderingoptions)

### Initializers

- [init(darkUserInterfaceStyle: Bool, layoutRightToLeft: Bool)](/documentation/paperkit/renderingoptions/init(darkuserinterfacestyle:layoutrighttoleft:))
- [init(traitCollection: UITraitCollection)](/documentation/paperkit/renderingoptions/init(traitcollection:))

### Instance Properties

- [var darkUserInterfaceStyle: Bool](/documentation/paperkit/renderingoptions/darkuserinterfacestyle)
- [var rightToLeftLayoutDirection: Bool](/documentation/paperkit/renderingoptions/righttoleftlayoutdirection)

## Data model

- [PaperMarkup](/documentation/paperkit/papermarkup)

### Initializers

- [init(bounds: CGRect)](/documentation/paperkit/papermarkup/init(bounds:))
- [init(dataRepresentation: Data) throws](/documentation/paperkit/papermarkup/init(datarepresentation:))

### Instance Properties

- [var bounds: CGRect](/documentation/paperkit/papermarkup/bounds)
- [var contentsRenderFrame: CGRect](/documentation/paperkit/papermarkup/contentsrenderframe)
- [var featureSet: FeatureSet](/documentation/paperkit/papermarkup/featureset)
- [var indexableContent: String?](/documentation/paperkit/papermarkup/indexablecontent)

### Instance Methods

- [func append(contentsOf: PaperMarkup)](/documentation/paperkit/papermarkup/append(contentsof:)-5668)
- [func append(contentsOf: PKDrawing)](/documentation/paperkit/papermarkup/append(contentsof:)-5tgti)
- [func dataRepresentation() async throws -> Data](/documentation/paperkit/papermarkup/datarepresentation())
- [func draw(in: CGContext, frame: CGRect, options: RenderingOptions) async](/documentation/paperkit/papermarkup/draw(in:frame:options:))
- [func insertNewImage(CGImage, frame: CGRect, rotation: CGFloat)](/documentation/paperkit/papermarkup/insertnewimage(_:frame:rotation:))
- [func insertNewLine(configuration: ShapeConfiguration, from: CGPoint, to: CGPoint, startMarker: Bool, endMarker: Bool)](/documentation/paperkit/papermarkup/insertnewline(configuration:from:to:startmarker:endmarker:))
- [func insertNewShape(configuration: ShapeConfiguration, frame: CGRect, rotation: CGFloat)](/documentation/paperkit/papermarkup/insertnewshape(configuration:frame:rotation:))
- [func insertNewTextbox(attributedText: AttributedString, frame: CGRect, rotation: CGFloat)](/documentation/paperkit/papermarkup/insertnewtextbox(attributedtext:frame:rotation:)-53rs)
- [func insertNewTextbox(attributedText: NSAttributedString, frame: CGRect, rotation: CGFloat)](/documentation/paperkit/papermarkup/insertnewtextbox(attributedtext:frame:rotation:)-67igk)
- [func removeContentUnsupported(by: FeatureSet)](/documentation/paperkit/papermarkup/removecontentunsupported(by:))
- [func transformContent(CGAffineTransform)](/documentation/paperkit/papermarkup/transformcontent(_:))

## Error handling

- [MarkupError](/documentation/paperkit/markuperror)

### Enumeration Cases

- [case incompatibleFormatTooNew](/documentation/paperkit/markuperror/incompatibleformattoonew)
- [case incorrectFormat](/documentation/paperkit/markuperror/incorrectformat)
- [case malformedData](/documentation/paperkit/markuperror/malformeddata)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
