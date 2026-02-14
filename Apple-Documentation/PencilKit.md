# PencilKit Documentation

Source: https://sosumi.ai/documentation/pencilkit

---
title: PencilKit
source: https://developer.apple.com/documentation/pencilkit
timestamp: 2026-02-13T19:00:33.552Z
---

## Canvas

- [Drawing with PencilKit](/documentation/pencilkit/drawing-with-pencilkit)
- [Customizing Scribble with Interactions](/documentation/pencilkit/customizing-scribble-with-interactions)
- [Inspecting, Modifying, and Constructing PencilKit Drawings](/documentation/pencilkit/inspecting-modifying-and-constructing-pencilkit-drawings)
- [PKCanvasView](/documentation/pencilkit/pkcanvasview)

### Responding to drawing-related changes

- [var delegate: (any PKCanvasViewDelegate)?](/documentation/pencilkit/pkcanvasview/delegate)
- [PKCanvasViewDelegate](/documentation/pencilkit/pkcanvasviewdelegate)

#### Responding to drawing-related changes

- [func canvasViewDrawingDidChange(PKCanvasView)](/documentation/pencilkit/pkcanvasviewdelegate/canvasviewdrawingdidchange(_:))
- [func canvasViewDidFinishRendering(PKCanvasView)](/documentation/pencilkit/pkcanvasviewdelegate/canvasviewdidfinishrendering(_:))

#### Responding to new event sequences

- [func canvasViewDidBeginUsingTool(PKCanvasView)](/documentation/pencilkit/pkcanvasviewdelegate/canvasviewdidbeginusingtool(_:))
- [func canvasViewDidEndUsingTool(PKCanvasView)](/documentation/pencilkit/pkcanvasviewdelegate/canvasviewdidendusingtool(_:))

### Configuring the drawing environment

- [var tool: any PKTool](/documentation/pencilkit/pkcanvasview/tool-1kj57)
- [var isRulerActive: Bool](/documentation/pencilkit/pkcanvasview/isruleractive)
- [var allowsFingerDrawing: Bool](/documentation/pencilkit/pkcanvasview/allowsfingerdrawing)
- [var drawingPolicy: PKCanvasViewDrawingPolicy](/documentation/pencilkit/pkcanvasview/drawingpolicy)
- [PKCanvasViewDrawingPolicy](/documentation/pencilkit/pkcanvasviewdrawingpolicy)

#### Drawing policies

- [case `default`](/documentation/pencilkit/pkcanvasviewdrawingpolicy/default)
- [case anyInput](/documentation/pencilkit/pkcanvasviewdrawingpolicy/anyinput)
- [case pencilOnly](/documentation/pencilkit/pkcanvasviewdrawingpolicy/pencilonly)

#### Initializers

- [init?(rawValue: UInt)](/documentation/pencilkit/pkcanvasviewdrawingpolicy/init(rawvalue:))

### Getting the drawing gesture recognizer

- [var drawingGestureRecognizer: UIGestureRecognizer](/documentation/pencilkit/pkcanvasview/drawinggesturerecognizer)

### Getting the captured data

- [var drawing: PKDrawing](/documentation/pencilkit/pkcanvasview/drawing)

### Supporting PencilKit versions

- [var maximumSupportedContentVersion: PKContentVersion](/documentation/pencilkit/pkcanvasview/maximumsupportedcontentversion)

### Instance Properties

- [var isDrawingEnabled: Bool](/documentation/pencilkit/pkcanvasview/isdrawingenabled)
- [PKDrawing](/documentation/pencilkit/pkdrawing-swift.struct)

### Creating a drawing object

- [init<S>(strokes: S)](/documentation/pencilkit/pkdrawing-swift.struct/init(strokes:))
- [init(data: Data) throws](/documentation/pencilkit/pkdrawing-swift.struct/init(data:))
- [init()](/documentation/pencilkit/pkdrawing-swift.struct/init())

### Getting the canvas bounds

- [var bounds: CGRect](/documentation/pencilkit/pkdrawing-swift.struct/bounds)

### Generating an image

- [func image(from: CGRect, scale: CGFloat) -> UIImage](/documentation/pencilkit/pkdrawing-swift.struct/image(from:scale:)-220d0)
- [func image(from: CGRect, scale: CGFloat) -> NSImage](/documentation/pencilkit/pkdrawing-swift.struct/image(from:scale:)-6p3zc)

### Getting the drawing data

- [var strokes: [PKStroke]](/documentation/pencilkit/pkdrawing-swift.struct/strokes)
- [func dataRepresentation() -> Data](/documentation/pencilkit/pkdrawing-swift.struct/datarepresentation())
- [let PKAppleDrawingTypeIdentifier: CFString](/documentation/pencilkit/pkappledrawingtypeidentifier)

### Modifying the drawing

- [func transform(using: CGAffineTransform)](/documentation/pencilkit/pkdrawing-swift.struct/transform(using:))
- [func transformed(using: CGAffineTransform) -> PKDrawing](/documentation/pencilkit/pkdrawing-swift.struct/transformed(using:))
- [func append(PKDrawing)](/documentation/pencilkit/pkdrawing-swift.struct/append(_:))
- [func appending(PKDrawing) -> PKDrawing](/documentation/pencilkit/pkdrawing-swift.struct/appending(_:))

### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkdrawing-swift.struct/requiredcontentversion)

### Using reference types

- [PKDrawingReference](/documentation/pencilkit/pkdrawingreference)

#### Creating a drawing object

- [init(data: Data) throws](/documentation/pencilkit/pkdrawingreference/init(data:))
- [convenience init(strokes: [PKStroke])](/documentation/pencilkit/pkdrawingreference/init(strokes:))
- [init()](/documentation/pencilkit/pkdrawingreference/init())

#### Getting the canvas bounds

- [var bounds: CGRect](/documentation/pencilkit/pkdrawingreference/bounds)

#### Generating an image

- [func image(from: CGRect, scale: CGFloat) -> UIImage](/documentation/pencilkit/pkdrawingreference/image(from:scale:))

#### Getting the drawing data

- [var strokes: [PKStroke]](/documentation/pencilkit/pkdrawingreference/strokes)
- [func dataRepresentation() -> Data](/documentation/pencilkit/pkdrawingreference/datarepresentation())
- [let PKAppleDrawingTypeIdentifier: CFString](/documentation/pencilkit/pkappledrawingtypeidentifier)

#### Modifying the drawing

- [func applying(CGAffineTransform) -> PKDrawing](/documentation/pencilkit/pkdrawingreference/applying(_:))
- [func appendingStrokes([PKStroke]) -> PKDrawing](/documentation/pencilkit/pkdrawingreference/appendingstrokes(_:))
- [func appending(PKDrawing) -> PKDrawing](/documentation/pencilkit/pkdrawingreference/appending(_:))

#### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkdrawingreference/requiredcontentversion)

### Instance Methods

- [func draw(in: CGContext, frame: CGRect, from: CGRect, darkUserInterfaceStyle: Bool) async](/documentation/pencilkit/pkdrawing-swift.struct/draw(in:frame:from:darkuserinterfacestyle:))
- [PKStroke](/documentation/pencilkit/pkstroke-swift.struct)

### Creating a stroke object

- [init(ink: PKInk, path: PKStrokePath, transform: CGAffineTransform, mask: UIBezierPath?)](/documentation/pencilkit/pkstroke-swift.struct/init(ink:path:transform:mask:)-1imp6)
- [init(ink: PKInk, path: PKStrokePath, transform: CGAffineTransform, mask: NSBezierPath?)](/documentation/pencilkit/pkstroke-swift.struct/init(ink:path:transform:mask:)-w7ti)
- [init(ink: PKInk, path: PKStrokePath, transform: CGAffineTransform, mask: UIBezierPath?, randomSeed: UInt32)](/documentation/pencilkit/pkstroke-swift.struct/init(ink:path:transform:mask:randomseed:)-10m5j)
- [init(ink: PKInk, path: PKStrokePath, transform: CGAffineTransform, mask: NSBezierPath?, randomSeed: UInt32)](/documentation/pencilkit/pkstroke-swift.struct/init(ink:path:transform:mask:randomseed:)-epus)

### Getting the stroke properties

- [var ink: PKInk](/documentation/pencilkit/pkstroke-swift.struct/ink)
- [var mask: UIBezierPath?](/documentation/pencilkit/pkstroke-swift.struct/mask-8g6sx)
- [var mask: NSBezierPath?](/documentation/pencilkit/pkstroke-swift.struct/mask-16kkz)
- [var maskedPathRanges: [ClosedRange<CGFloat>]](/documentation/pencilkit/pkstroke-swift.struct/maskedpathranges)
- [var path: PKStrokePath](/documentation/pencilkit/pkstroke-swift.struct/path)
- [var renderBounds: CGRect](/documentation/pencilkit/pkstroke-swift.struct/renderbounds)
- [var transform: CGAffineTransform](/documentation/pencilkit/pkstroke-swift.struct/transform)
- [var randomSeed: UInt32](/documentation/pencilkit/pkstroke-swift.struct/randomseed)

### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkstroke-swift.struct/requiredcontentversion)

### Using reference types

- [PKStrokeReference](/documentation/pencilkit/pkstrokereference)

#### Creating a stroke object

- [init(ink: PKInk, strokePath: PKStrokePath, transform: CGAffineTransform, mask: UIBezierPath?)](/documentation/pencilkit/pkstrokereference/init(ink:strokepath:transform:mask:))
- [init(ink: PKInk, strokePath: PKStrokePath, transform: CGAffineTransform, mask: UIBezierPath?, randomSeed: UInt32)](/documentation/pencilkit/pkstrokereference/init(ink:strokepath:transform:mask:randomseed:))

#### Getting the stroke properties

- [var ink: PKInk](/documentation/pencilkit/pkstrokereference/ink)
- [var mask: UIBezierPath?](/documentation/pencilkit/pkstrokereference/mask)
- [var maskedPathRanges: [__PKFloatRange]](/documentation/pencilkit/pkstrokereference/maskedpathranges)
- [var path: PKStrokePath](/documentation/pencilkit/pkstrokereference/path)
- [var renderBounds: CGRect](/documentation/pencilkit/pkstrokereference/renderbounds)
- [var transform: CGAffineTransform](/documentation/pencilkit/pkstrokereference/transform)
- [var randomSeed: UInt32](/documentation/pencilkit/pkstrokereference/randomseed)

#### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkstrokereference/requiredcontentversion)
- [PKStrokePath](/documentation/pencilkit/pkstrokepath-swift.struct)

### Creating a new stroke path

- [init()](/documentation/pencilkit/pkstrokepath-swift.struct/init())
- [init<T>(controlPoints: T, creationDate: Date)](/documentation/pencilkit/pkstrokepath-swift.struct/init(controlpoints:creationdate:))

### Getting the stroke path properties

- [var creationDate: Date](/documentation/pencilkit/pkstrokepath-swift.struct/creationdate)

### Accessing and interpolating points

- [func interpolatedPoints(in: ClosedRange<CGFloat>?, by: PKStrokePath.InterpolatedSlice.Stride) -> PKStrokePath.InterpolatedSlice](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedpoints(in:by:))
- [func interpolatedLocation(at: CGFloat) -> CGPoint](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedlocation(at:))
- [func interpolatedPoint(at: CGFloat) -> PKStrokePoint](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedpoint(at:))
- [func parametricValue(CGFloat, offsetBy: PKStrokePath.InterpolatedSlice.Stride) -> CGFloat](/documentation/pencilkit/pkstrokepath-swift.struct/parametricvalue(_:offsetby:))

### Supporting types

- [PKStrokePath.InterpolatedSlice](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedslice)

#### Traversing slices

- [PKStrokePath.InterpolatedSlice.Stride](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedslice/stride)

##### Stride types

- [case distance(CGFloat)](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedslice/stride/distance(_:))
- [case parametricStep(CGFloat)](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedslice/stride/parametricstep(_:))
- [case time(TimeInterval)](/documentation/pencilkit/pkstrokepath-swift.struct/interpolatedslice/stride/time(_:))

#### Supporting protocol requirements

- [Protocol implementations](/documentation/pencilkit/interpolatedslice-protocol-implementations)

### Supporting protocol requirements

- [Protocol implementations](/documentation/pencilkit/pkstrokepath-protocol-implementations)

### Using reference types

- [PKStrokePathReference](/documentation/pencilkit/pkstrokepathreference)

#### Creating a new stroke path

- [init(controlPoints: [PKStrokePoint], creationDate: Date)](/documentation/pencilkit/pkstrokepathreference/init(controlpoints:creationdate:))

#### Getting the stroke path properties

- [var count: Int](/documentation/pencilkit/pkstrokepathreference/count)
- [var creationDate: Date](/documentation/pencilkit/pkstrokepathreference/creationdate)

#### Accessing and interpolating points

- [func enumerateInterpolatedPoints(in: __PKFloatRange, strideByDistance: CGFloat, using: (PKStrokePoint, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/pencilkit/pkstrokepathreference/enumerateinterpolatedpoints(in:stridebydistance:using:))
- [func enumerateInterpolatedPoints(in: __PKFloatRange, strideByParametricStep: CGFloat, using: (PKStrokePoint, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/pencilkit/pkstrokepathreference/enumerateinterpolatedpoints(in:stridebyparametricstep:using:))
- [func enumerateInterpolatedPoints(in: __PKFloatRange, strideByTime: TimeInterval, using: (PKStrokePoint, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/pencilkit/pkstrokepathreference/enumerateinterpolatedpoints(in:stridebytime:using:))
- [func interpolatedLocation(at: CGFloat) -> CGPoint](/documentation/pencilkit/pkstrokepathreference/interpolatedlocation(at:))
- [func interpolatedPoint(at: CGFloat) -> PKStrokePoint](/documentation/pencilkit/pkstrokepathreference/interpolatedpoint(at:))
- [func parametricValue(CGFloat, offsetByDistance: CGFloat) -> CGFloat](/documentation/pencilkit/pkstrokepathreference/parametricvalue(_:offsetbydistance:))
- [func parametricValue(CGFloat, offsetByTime: TimeInterval) -> CGFloat](/documentation/pencilkit/pkstrokepathreference/parametricvalue(_:offsetbytime:))
- [func point(at: Int) -> PKStrokePoint](/documentation/pencilkit/pkstrokepathreference/point(at:))
- [subscript(Int) -> PKStrokePoint](/documentation/pencilkit/pkstrokepathreference/subscript(_:))
- [PKStrokePoint](/documentation/pencilkit/pkstrokepoint-swift.struct)

### Creating a stroke point object

- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat)](/documentation/pencilkit/pkstrokepoint-swift.struct/init(location:timeoffset:size:opacity:force:azimuth:altitude:))
- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat, secondaryScale: CGFloat)](/documentation/pencilkit/pkstrokepoint-swift.struct/init(location:timeoffset:size:opacity:force:azimuth:altitude:secondaryscale:))

### Getting the point’s location

- [var location: CGPoint](/documentation/pencilkit/pkstrokepoint-swift.struct/location)
- [var timeOffset: TimeInterval](/documentation/pencilkit/pkstrokepoint-swift.struct/timeoffset)

### Getting the point’s touch data

- [var altitude: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/altitude)
- [var azimuth: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/azimuth)
- [var force: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/force)

### Getting the point’s drawing data

- [var size: CGSize](/documentation/pencilkit/pkstrokepoint-swift.struct/size)
- [var opacity: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/opacity)
- [var secondaryScale: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/secondaryscale)

### Using reference types

- [PKStrokePointReference](/documentation/pencilkit/pkstrokepointreference)

#### Creating a stroke point object

- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat)](/documentation/pencilkit/pkstrokepointreference/init(location:timeoffset:size:opacity:force:azimuth:altitude:))
- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat, secondaryScale: CGFloat)](/documentation/pencilkit/pkstrokepointreference/init(location:timeoffset:size:opacity:force:azimuth:altitude:secondaryscale:))

#### Getting the point’s location

- [var location: CGPoint](/documentation/pencilkit/pkstrokepointreference/location)
- [var timeOffset: TimeInterval](/documentation/pencilkit/pkstrokepointreference/timeoffset)

#### Getting the point’s touch data

- [var altitude: CGFloat](/documentation/pencilkit/pkstrokepointreference/altitude)
- [var azimuth: CGFloat](/documentation/pencilkit/pkstrokepointreference/azimuth)
- [var force: CGFloat](/documentation/pencilkit/pkstrokepointreference/force)

#### Getting the point’s drawing data

- [var size: CGSize](/documentation/pencilkit/pkstrokepointreference/size)
- [var opacity: CGFloat](/documentation/pencilkit/pkstrokepointreference/opacity)
- [var secondaryScale: CGFloat](/documentation/pencilkit/pkstrokepointreference/secondaryscale)

#### Initializers

- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat, secondaryScale: CGFloat, threshold: CGFloat)](/documentation/pencilkit/pkstrokepointreference/init(location:timeoffset:size:opacity:force:azimuth:altitude:secondaryscale:threshold:))

#### Instance Properties

- [var threshold: CGFloat](/documentation/pencilkit/pkstrokepointreference/threshold)

### Initializers

- [init(location: CGPoint, timeOffset: TimeInterval, size: CGSize, opacity: CGFloat, force: CGFloat, azimuth: CGFloat, altitude: CGFloat, secondaryScale: CGFloat, threshold: CGFloat)](/documentation/pencilkit/pkstrokepoint-swift.struct/init(location:timeoffset:size:opacity:force:azimuth:altitude:secondaryscale:threshold:))

### Instance Properties

- [var threshold: CGFloat](/documentation/pencilkit/pkstrokepoint-swift.struct/threshold)
- [PKInk](/documentation/pencilkit/pkink-swift.struct)

### Creating an ink object

- [init(PKInk.InkType, color: UIColor)](/documentation/pencilkit/pkink-swift.struct/init(_:color:)-2rx09)
- [init(PKInk.InkType, color: NSColor)](/documentation/pencilkit/pkink-swift.struct/init(_:color:)-7w46l)
- [PKInk.InkType](/documentation/pencilkit/pkink-swift.struct/inktype-swift.typealias)

### Getting the ink attributes

- [var color: UIColor](/documentation/pencilkit/pkink-swift.struct/color-cg6f)
- [var color: NSColor](/documentation/pencilkit/pkink-swift.struct/color-6lmjp)
- [var inkType: PKInk.InkType](/documentation/pencilkit/pkink-swift.struct/inktype-swift.property)

### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkink-swift.struct/requiredcontentversion)

### Using reference types

- [PKInkReference](/documentation/pencilkit/pkinkreference)

#### Creating an ink

- [init(inkType: __PKInkType, color: UIColor)](/documentation/pencilkit/pkinkreference/init(inktype:color:))

#### Getting the ink attributes

- [var color: UIColor](/documentation/pencilkit/pkinkreference/color)
- [var inkType: __PKInkType](/documentation/pencilkit/pkinkreference/inktype)

#### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkinkreference/requiredcontentversion)

## Tools

- [Configuring the PencilKit tool picker](/documentation/pencilkit/configuring-the-pencilkit-tool-picker)
- [PKToolPicker](/documentation/pencilkit/pktoolpicker)

### Creating a tool picker

- [init()](/documentation/pencilkit/pktoolpicker/init())
- [init(toolItems: [PKToolPickerItem])](/documentation/pencilkit/pktoolpicker/init(toolitems:))
- [PKToolPickerInkingItem](/documentation/pencilkit/pktoolpickerinkingitem)

#### Accessing the inking tool

- [var inkingTool: PKInkingTool](/documentation/pencilkit/pktoolpickerinkingitem/inkingtool-1hcet)

#### Initializers

- [convenience init(type: PKInkingTool.InkType, color: UIColor?, width: CGFloat?, azimuth: CGFloat?, identifier: String?)](/documentation/pencilkit/pktoolpickerinkingitem/init(type:color:width:azimuth:identifier:)-7gkxh)
- [convenience init(type: PKInkingTool.InkType, color: NSColor?, width: CGFloat?, azimuth: CGFloat?, identifier: String?)](/documentation/pencilkit/pktoolpickerinkingitem/init(type:color:width:azimuth:identifier:)-y8h5)
- [convenience init(type: PKInkingTool.InkType, color: NSColor?, width: CGFloat?, identifier: String?)](/documentation/pencilkit/pktoolpickerinkingitem/init(type:color:width:identifier:)-1tsup)
- [convenience init(type: PKInkingTool.InkType, color: UIColor?, width: CGFloat?, identifier: String?)](/documentation/pencilkit/pktoolpickerinkingitem/init(type:color:width:identifier:)-7kzdq)

#### Instance Properties

- [var allowsColorSelection: Bool](/documentation/pencilkit/pktoolpickerinkingitem/allowscolorselection)
- [PKToolPickerEraserItem](/documentation/pencilkit/pktoolpickereraseritem)

#### Creating an eraser item

- [convenience init(type: PKEraserTool.EraserType)](/documentation/pencilkit/pktoolpickereraseritem/init(type:))
- [convenience init(type: PKEraserTool.EraserType, width: CGFloat)](/documentation/pencilkit/pktoolpickereraseritem/init(type:width:))

#### Accessing the eraser tool

- [var eraserTool: PKEraserTool](/documentation/pencilkit/pktoolpickereraseritem/erasertool-92wqj)
- [PKToolPickerLassoItem](/documentation/pencilkit/pktoolpickerlassoitem)

#### Creating a lasso item

- [init()](/documentation/pencilkit/pktoolpickerlassoitem/init())

#### Accessing the lasso tool

- [var lassoTool: PKLassoTool](/documentation/pencilkit/pktoolpickerlassoitem/lassotool-2xuhy)
- [PKToolPickerRulerItem](/documentation/pencilkit/pktoolpickerruleritem)

#### Creating a ruler item

- [init()](/documentation/pencilkit/pktoolpickerruleritem/init())
- [PKToolPickerScribbleItem](/documentation/pencilkit/pktoolpickerscribbleitem)

#### Creating a Scribble item

- [init()](/documentation/pencilkit/pktoolpickerscribbleitem/init())
- [PKToolPickerCustomItem](/documentation/pencilkit/pktoolpickercustomitem)

#### Creating a custom item

- [convenience init(configuration: PKToolPickerCustomItem.Configuration)](/documentation/pencilkit/pktoolpickercustomitem/init(configuration:))

#### Configuring the custom item

- [var color: UIColor](/documentation/pencilkit/pktoolpickercustomitem/color)
- [var width: CGFloat](/documentation/pencilkit/pktoolpickercustomitem/width)
- [var configuration: PKToolPickerCustomItem.Configuration](/documentation/pencilkit/pktoolpickercustomitem/configuration-41nm4)
- [PKToolPickerCustomItem.Configuration](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct)

##### Creating a configuration

- [init(identifier: String, name: String)](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/init(identifier:name:))

##### Identifying the custom tool

- [var identifier: String](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/identifier)
- [var name: String](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/name)

##### Customizing color

- [var defaultColor: UIColor](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/defaultcolor)
- [var allowsColorSelection: Bool](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/allowscolorselection)

##### Customizing width

- [var defaultWidth: CGFloat](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/defaultwidth)
- [var widthVariants: [CGFloat : UIImage]](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/widthvariants)

##### Providing an image for the tool

- [var imageProvider: ((PKToolPickerCustomItem) -> UIImage)?](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/imageprovider)

##### Providing a custom view controller for the tool

- [var viewControllerProvider: ((PKToolPickerCustomItem) -> UIViewController)?](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/viewcontrollerprovider)

##### Instance Properties

- [var toolAttributeControls: PKToolPickerCustomItem.ControlOptions](/documentation/pencilkit/pktoolpickercustomitem/configuration-swift.struct/toolattributecontrols)

#### Reloading the custom item image

- [func reloadImage()](/documentation/pencilkit/pktoolpickercustomitem/reloadimage())

#### Structures

- [PKToolPickerCustomItem.ControlOptions](/documentation/pencilkit/pktoolpickercustomitem/controloptions)

##### Initializers

- [init(rawValue: UInt)](/documentation/pencilkit/pktoolpickercustomitem/controloptions/init(rawvalue:))

##### Type Properties

- [static var opacity: PKToolPickerCustomItem.ControlOptions](/documentation/pencilkit/pktoolpickercustomitem/controloptions/opacity)
- [static var width: PKToolPickerCustomItem.ControlOptions](/documentation/pencilkit/pktoolpickercustomitem/controloptions/width)

#### Instance Properties

- [var allowsColorSelection: Bool](/documentation/pencilkit/pktoolpickercustomitem/allowscolorselection)
- [PKToolPickerItem](/documentation/pencilkit/pktoolpickeritem)

#### Identifying the item

- [var identifier: String](/documentation/pencilkit/pktoolpickeritem/identifier)

#### Instance Properties

- [var tool: (any PKTool)?](/documentation/pencilkit/pktoolpickeritem/tool-2ji9h)

### Accessing the picker’s tools

- [var toolItems: [PKToolPickerItem]](/documentation/pencilkit/pktoolpicker/toolitems)

### Detecting changes to the picker

- [func addObserver(any PKToolPickerObserver)](/documentation/pencilkit/pktoolpicker/addobserver(_:))
- [func removeObserver(any PKToolPickerObserver)](/documentation/pencilkit/pktoolpicker/removeobserver(_:))
- [PKToolPickerObserver](/documentation/pencilkit/pktoolpickerobserver)

#### Detecting tool configuration changes

- [func toolPickerSelectedToolItemDidChange(PKToolPicker)](/documentation/pencilkit/pktoolpickerobserver/toolpickerselectedtoolitemdidchange(_:))
- [func toolPickerIsRulerActiveDidChange(PKToolPicker)](/documentation/pencilkit/pktoolpickerobserver/toolpickerisruleractivedidchange(_:))

#### Monitoring visibility changes

- [func toolPickerVisibilityDidChange(PKToolPicker)](/documentation/pencilkit/pktoolpickerobserver/toolpickervisibilitydidchange(_:))
- [func toolPickerFramesObscuredDidChange(PKToolPicker)](/documentation/pencilkit/pktoolpickerobserver/toolpickerframesobscureddidchange(_:))

#### Deprecated

- [func toolPickerSelectedToolDidChange(PKToolPicker)](/documentation/pencilkit/pktoolpickerobserver/toolpickerselectedtooldidchange(_:))

### Coordinating the visibility of the picker

- [func setVisible(Bool, forFirstResponder: UIResponder)](/documentation/pencilkit/pktoolpicker/setvisible(_:forfirstresponder:))
- [var isVisible: Bool](/documentation/pencilkit/pktoolpicker/isvisible)
- [func frameObscured(in: UIView) -> CGRect](/documentation/pencilkit/pktoolpicker/frameobscured(in:))

### Managing selected tools

- [var selectedToolItem: PKToolPickerItem](/documentation/pencilkit/pktoolpicker/selectedtoolitem)
- [var selectedToolItemIdentifier: String](/documentation/pencilkit/pktoolpicker/selectedtoolitemidentifier)

### Customizing picker behavior

- [var isRulerActive: Bool](/documentation/pencilkit/pktoolpicker/isruleractive)
- [var colorUserInterfaceStyle: UIUserInterfaceStyle](/documentation/pencilkit/pktoolpicker/coloruserinterfacestyle)
- [var overrideUserInterfaceStyle: UIUserInterfaceStyle](/documentation/pencilkit/pktoolpicker/overrideuserinterfacestyle)
- [var showsDrawingPolicyControls: Bool](/documentation/pencilkit/pktoolpicker/showsdrawingpolicycontrols)
- [var stateAutosaveName: String?](/documentation/pencilkit/pktoolpicker/stateautosavename)

### Configuring the accessory item

- [var accessoryItem: UIBarButtonItem?](/documentation/pencilkit/pktoolpicker/accessoryitem)

### Supporting PencilKit versions

- [var maximumSupportedContentVersion: PKContentVersion](/documentation/pencilkit/pktoolpicker/maximumsupportedcontentversion)

### Deprecated

- [class func shared(for: UIWindow) -> PKToolPicker?](/documentation/pencilkit/pktoolpicker/shared(for:))
- [var selectedTool: any PKTool](/documentation/pencilkit/pktoolpicker/selectedtool-2lptq)

### Protocols

- [PKToolPicker.Delegate](/documentation/pencilkit/pktoolpicker/delegate-swift.protocol)

#### Instance Methods

- [func toolPickerWillDismiss(PKToolPicker) -> Bool](/documentation/pencilkit/pktoolpicker/delegate-swift.protocol/toolpickerwilldismiss(_:))

### Instance Properties

- [var colorMaximumLinearExposure: CGFloat](/documentation/pencilkit/pktoolpicker/colormaximumlinearexposure)
- [var delegate: (any PKToolPicker.Delegate)?](/documentation/pencilkit/pktoolpicker/delegate-swift.property)
- [var prefersDismissControlVisible: Bool](/documentation/pencilkit/pktoolpicker/prefersdismisscontrolvisible)

### Type Properties

- [class var defaultToolItems: [PKToolPickerItem]](/documentation/pencilkit/pktoolpicker/defaulttoolitems)
- [PKInkingTool](/documentation/pencilkit/pkinkingtool-swift.struct)

### Creating an inking tool

- [init(PKInkingTool.InkType, color: UIColor, width: CGFloat?)](/documentation/pencilkit/pkinkingtool-swift.struct/init(_:color:width:)-2l7v)
- [init(PKInkingTool.InkType, color: NSColor, width: CGFloat?)](/documentation/pencilkit/pkinkingtool-swift.struct/init(_:color:width:)-4i3ft)
- [init(ink: PKInk, width: CGFloat)](/documentation/pencilkit/pkinkingtool-swift.struct/init(ink:width:))

### Getting the width information

- [var defaultWidth: CGFloat](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/defaultwidth)
- [var validWidthRange: ClosedRange<CGFloat>](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/validwidthrange)

### Getting the inking tool attributes

- [var color: UIColor](/documentation/pencilkit/pkinkingtool-swift.struct/color-5xmlo)
- [var color: NSColor](/documentation/pencilkit/pkinkingtool-swift.struct/color-22zaw)
- [var width: CGFloat](/documentation/pencilkit/pkinkingtool-swift.struct/width)
- [var ink: PKInk](/documentation/pencilkit/pkinkingtool-swift.struct/ink)

### Getting the tool type

- [var inkType: PKInkingTool.InkType](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.property)
- [PKInkingTool.InkType](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum)

#### Choosing ink types

- [case marker](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/marker)
- [case pen](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/pen)
- [case pencil](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/pencil)
- [case monoline](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/monoline)
- [case fountainPen](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/fountainpen)
- [case watercolor](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/watercolor)
- [case crayon](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/crayon)

#### Getting the width information

- [var defaultWidth: CGFloat](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/defaultwidth)
- [var validWidthRange: ClosedRange<CGFloat>](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/validwidthrange)

#### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/requiredcontentversion)

#### Enumeration Cases

- [case reed](/documentation/pencilkit/pkinkingtool-swift.struct/inktype-swift.enum/reed)

### Working with colors

- [static func convertColor(UIColor, from: UIUserInterfaceStyle, to: UIUserInterfaceStyle) -> UIColor](/documentation/pencilkit/pkinkingtool-swift.struct/convertcolor(_:from:to:))

### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkinkingtool-swift.struct/requiredcontentversion)

### Using reference types

- [PKInkingToolReference](/documentation/pencilkit/pkinkingtoolreference)

#### Creating an inking tool

- [init(inkType: __PKInkType, color: UIColor, width: CGFloat)](/documentation/pencilkit/pkinkingtoolreference/init(inktype:color:width:))
- [convenience init(inkType: __PKInkType, color: UIColor)](/documentation/pencilkit/pkinkingtoolreference/init(inktype:color:))
- [convenience init(ink: PKInk, width: CGFloat)](/documentation/pencilkit/pkinkingtoolreference/init(ink:width:))

#### Getting the inking tool attributes

- [var color: UIColor](/documentation/pencilkit/pkinkingtoolreference/color)
- [var width: CGFloat](/documentation/pencilkit/pkinkingtoolreference/width)
- [var ink: PKInk](/documentation/pencilkit/pkinkingtoolreference/ink)

#### Getting the tool type

- [var inkType: __PKInkType](/documentation/pencilkit/pkinkingtoolreference/inktype)

#### Working with colors

- [class func convert(UIColor, from: UIUserInterfaceStyle, to: UIUserInterfaceStyle) -> UIColor](/documentation/pencilkit/pkinkingtoolreference/convert(_:from:to:))

#### Getting the standard ink widths

- [class func defaultWidth(forInkType: __PKInkType) -> CGFloat](/documentation/pencilkit/pkinkingtoolreference/defaultwidth(forinktype:))
- [class func minimumWidth(forInkType: __PKInkType) -> CGFloat](/documentation/pencilkit/pkinkingtoolreference/minimumwidth(forinktype:))
- [class func maximumWidth(forInkType: __PKInkType) -> CGFloat](/documentation/pencilkit/pkinkingtoolreference/maximumwidth(forinktype:))

#### Supporting backward compatibility

- [var requiredContentVersion: PKContentVersion](/documentation/pencilkit/pkinkingtoolreference/requiredcontentversion)

#### Initializers

- [init(inkType: __PKInkType, color: UIColor, width: CGFloat, azimuth: CGFloat)](/documentation/pencilkit/pkinkingtoolreference/init(inktype:color:width:azimuth:))

#### Instance Properties

- [var azimuth: CGFloat](/documentation/pencilkit/pkinkingtoolreference/azimuth)

#### Type Methods

- [class func invertColor(CGColor) -> Unmanaged<CGColor>](/documentation/pencilkit/pkinkingtoolreference/invertcolor(_:))

### Initializers

- [init(PKInkingTool.InkType, color: UIColor, width: CGFloat?, azimuth: CGFloat)](/documentation/pencilkit/pkinkingtool-swift.struct/init(_:color:width:azimuth:)-24rf4)
- [init(PKInkingTool.InkType, color: NSColor, width: CGFloat?, azimuth: CGFloat)](/documentation/pencilkit/pkinkingtool-swift.struct/init(_:color:width:azimuth:)-5dtjs)

### Instance Properties

- [var azimuth: CGFloat](/documentation/pencilkit/pkinkingtool-swift.struct/azimuth)
- [PKEraserTool](/documentation/pencilkit/pkerasertool-swift.struct)

### Creating an eraser tool

- [init(PKEraserTool.EraserType)](/documentation/pencilkit/pkerasertool-swift.struct/init(_:))
- [init(PKEraserTool.EraserType, width: CGFloat)](/documentation/pencilkit/pkerasertool-swift.struct/init(_:width:))

### Getting the eraser type

- [var eraserType: PKEraserTool.EraserType](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.property)
- [PKEraserTool.EraserType](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum)

#### Eraser types

- [case vector](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum/vector)
- [case bitmap](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum/bitmap)
- [case fixedWidthBitmap](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum/fixedwidthbitmap)

#### Getting the width information

- [var defaultWidth: CGFloat](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum/defaultwidth)
- [var validWidthRange: ClosedRange<CGFloat>](/documentation/pencilkit/pkerasertool-swift.struct/erasertype-swift.enum/validwidthrange)

### Specifying the width

- [var width: CGFloat](/documentation/pencilkit/pkerasertool-swift.struct/width)

### Using reference types

- [PKEraserToolReference](/documentation/pencilkit/pkerasertoolreference)

#### Creating an eraser tool

- [init(eraserType: __PKEraserType)](/documentation/pencilkit/pkerasertoolreference/init(erasertype:))
- [init(eraserType: __PKEraserType, width: CGFloat)](/documentation/pencilkit/pkerasertoolreference/init(erasertype:width:))

#### Getting the eraser type

- [var eraserType: __PKEraserType](/documentation/pencilkit/pkerasertoolreference/erasertype)

#### Getting the width information

- [var width: CGFloat](/documentation/pencilkit/pkerasertoolreference/width)
- [class func defaultWidth(for: __PKEraserType) -> CGFloat](/documentation/pencilkit/pkerasertoolreference/defaultwidth(for:))
- [class func minimumWidth(for: __PKEraserType) -> CGFloat](/documentation/pencilkit/pkerasertoolreference/minimumwidth(for:))
- [class func maximumWidth(for: __PKEraserType) -> CGFloat](/documentation/pencilkit/pkerasertoolreference/maximumwidth(for:))
- [PKLassoTool](/documentation/pencilkit/pklassotool-swift.struct)

### Creating a lasso tool

- [init()](/documentation/pencilkit/pklassotool-swift.struct/init())

### Using reference types

- [PKLassoToolReference](/documentation/pencilkit/pklassotoolreference)

#### Creating a lasso tool

- [init()](/documentation/pencilkit/pklassotoolreference/init())
- [PKTool](/documentation/pencilkit/pktool-swift.protocol)

## Backward compatibility

- [Supporting backward compatibility for ink types](/documentation/pencilkit/supporting-backward-compatibility-for-ink-types)
- [PKContentVersion](/documentation/pencilkit/pkcontentversion)

### Latest version

- [static var latest: PKContentVersion](/documentation/pencilkit/pkcontentversion/latest)

### Specific versions

- [case version1](/documentation/pencilkit/pkcontentversion/version1)
- [case version2](/documentation/pencilkit/pkcontentversion/version2)
- [case version3](/documentation/pencilkit/pkcontentversion/version3)

### Enumeration Cases

- [case version4](/documentation/pencilkit/pkcontentversion/version4)

### Initializers

- [init?(rawValue: Int)](/documentation/pencilkit/pkcontentversion/init(rawvalue:))

## Classes

- [PKResponderState](/documentation/pencilkit/pkresponderstate)

### Instance Properties

- [var activeToolPicker: PKToolPicker?](/documentation/pencilkit/pkresponderstate/activetoolpicker)
- [var toolPickerVisibility: PKToolPickerVisibility?](/documentation/pencilkit/pkresponderstate/toolpickervisibility-7cj3c)

## Enumerations

- [PKToolPickerVisibility](/documentation/pencilkit/pktoolpickervisibility)

### Enumeration Cases

- [case hidden](/documentation/pencilkit/pktoolpickervisibility/hidden)
- [case inactive](/documentation/pencilkit/pktoolpickervisibility/inactive)
- [case visible](/documentation/pencilkit/pktoolpickervisibility/visible)

### Initializers

- [init?(rawValue: Int)](/documentation/pencilkit/pktoolpickervisibility/init(rawvalue:))

### Instance Methods

- [func toggle()](/documentation/pencilkit/pktoolpickervisibility/toggle())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
