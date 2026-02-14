# Core Graphics Documentation

Source: https://sosumi.ai/documentation/coregraphics

---
title: Core Graphics
source: https://developer.apple.com/documentation/coregraphics
timestamp: 2026-02-13T19:23:09.357Z
---

## Geometric Data Types

- [CGFloat](/documentation/corefoundation/cgfloat-swift.struct)
- [CGPoint](/documentation/corefoundation/cgpoint)
- [CGSize](/documentation/corefoundation/cgsize)
- [CGRect](/documentation/corefoundation/cgrect)
- [CGVector](/documentation/corefoundation/cgvector)
- [CGAffineTransform](/documentation/corefoundation/cgaffinetransform)

## 2D Drawing

- [CGContext](/documentation/coregraphics/cgcontext)

### Creating Bitmap Graphics Contexts

- [CGBitmapContextReleaseDataCallback](/documentation/coregraphics/cgbitmapcontextreleasedatacallback)

### Creating PDF Graphics Contexts

- [init?(CFURL, mediaBox: UnsafePointer<CGRect>?, CFDictionary?)](/documentation/coregraphics/cgcontext/init(_:mediabox:_:))
- [init?(consumer: CGDataConsumer, mediaBox: UnsafePointer<CGRect>?, CFDictionary?)](/documentation/coregraphics/cgcontext/init(consumer:mediabox:_:))
- [Auxiliary Dictionary Keys](/documentation/coregraphics/auxiliary-dictionary-keys)

#### Metadata Keys

- [let kCGPDFContextAuthor: CFString](/documentation/coregraphics/kcgpdfcontextauthor)
- [let kCGPDFContextCreator: CFString](/documentation/coregraphics/kcgpdfcontextcreator)
- [let kCGPDFContextTitle: CFString](/documentation/coregraphics/kcgpdfcontexttitle)
- [let kCGPDFContextOwnerPassword: CFString](/documentation/coregraphics/kcgpdfcontextownerpassword)
- [let kCGPDFContextUserPassword: CFString](/documentation/coregraphics/kcgpdfcontextuserpassword)
- [let kCGPDFContextAllowsPrinting: CFString](/documentation/coregraphics/kcgpdfcontextallowsprinting)
- [let kCGPDFContextAllowsCopying: CFString](/documentation/coregraphics/kcgpdfcontextallowscopying)
- [let kCGPDFContextOutputIntent: CFString](/documentation/coregraphics/kcgpdfcontextoutputintent)
- [let kCGPDFContextOutputIntents: CFString](/documentation/coregraphics/kcgpdfcontextoutputintents)
- [let kCGPDFContextSubject: CFString](/documentation/coregraphics/kcgpdfcontextsubject)
- [let kCGPDFContextKeywords: CFString](/documentation/coregraphics/kcgpdfcontextkeywords)
- [let kCGPDFContextEncryptionKeyLength: CFString](/documentation/coregraphics/kcgpdfcontextencryptionkeylength)

#### Box Keys

- [let kCGPDFContextMediaBox: CFString](/documentation/coregraphics/kcgpdfcontextmediabox)
- [let kCGPDFContextCropBox: CFString](/documentation/coregraphics/kcgpdfcontextcropbox)
- [let kCGPDFContextBleedBox: CFString](/documentation/coregraphics/kcgpdfcontextbleedbox)
- [let kCGPDFContextTrimBox: CFString](/documentation/coregraphics/kcgpdfcontexttrimbox)
- [let kCGPDFContextArtBox: CFString](/documentation/coregraphics/kcgpdfcontextartbox)

#### Output Intent Keys

- [let kCGPDFXOutputIntentSubtype: CFString](/documentation/coregraphics/kcgpdfxoutputintentsubtype)
- [let kCGPDFXOutputConditionIdentifier: CFString](/documentation/coregraphics/kcgpdfxoutputconditionidentifier)
- [let kCGPDFXOutputCondition: CFString](/documentation/coregraphics/kcgpdfxoutputcondition)
- [let kCGPDFXRegistryName: CFString](/documentation/coregraphics/kcgpdfxregistryname)
- [let kCGPDFXInfo: CFString](/documentation/coregraphics/kcgpdfxinfo)
- [let kCGPDFXDestinationOutputProfile: CFString](/documentation/coregraphics/kcgpdfxdestinationoutputprofile)

### Converting Between Coordinate Spaces

- [var userSpaceToDeviceSpaceTransform: CGAffineTransform](/documentation/coregraphics/cgcontext/userspacetodevicespacetransform)
- [func convertToDeviceSpace(CGPoint) -> CGPoint](/documentation/coregraphics/cgcontext/converttodevicespace(_:)-53m7u)
- [func convertToUserSpace(CGPoint) -> CGPoint](/documentation/coregraphics/cgcontext/converttouserspace(_:)-3mtg3)
- [func convertToDeviceSpace(CGRect) -> CGRect](/documentation/coregraphics/cgcontext/converttodevicespace(_:)-91x5g)
- [func convertToUserSpace(CGRect) -> CGRect](/documentation/coregraphics/cgcontext/converttouserspace(_:)-1hk5r)
- [func convertToDeviceSpace(CGSize) -> CGSize](/documentation/coregraphics/cgcontext/converttodevicespace(_:)-224h2)
- [func convertToUserSpace(CGSize) -> CGSize](/documentation/coregraphics/cgcontext/converttouserspace(_:)-693ur)

### Constructing a Current Graphics Path

- [func beginPath()](/documentation/coregraphics/cgcontext/beginpath())
- [CGContextMoveToPoint](/documentation/coregraphics/cgcontext/move(to:))
- [CGContextAddLineToPoint](/documentation/coregraphics/cgcontext/addline(to:))
- [CGContextAddLines](/documentation/coregraphics/cgcontext/addlines(between:))
- [func addRect(CGRect)](/documentation/coregraphics/cgcontext/addrect(_:))
- [CGContextAddRects](/documentation/coregraphics/cgcontext/addrects(_:))
- [func addEllipse(in: CGRect)](/documentation/coregraphics/cgcontext/addellipse(in:))
- [func addArc(center: CGPoint, radius: CGFloat, startAngle: CGFloat, endAngle: CGFloat, clockwise: Bool)](/documentation/coregraphics/cgcontext/addarc(center:radius:startangle:endangle:clockwise:))
- [CGContextAddArcToPoint](/documentation/coregraphics/cgcontext/addarc(tangent1end:tangent2end:radius:))
- [CGContextAddCurveToPoint](/documentation/coregraphics/cgcontext/addcurve(to:control1:control2:))
- [CGContextAddQuadCurveToPoint](/documentation/coregraphics/cgcontext/addquadcurve(to:control:))
- [func addPath(CGPath)](/documentation/coregraphics/cgcontext/addpath(_:))
- [func closePath()](/documentation/coregraphics/cgcontext/closepath())
- [var path: CGPath?](/documentation/coregraphics/cgcontext/path)
- [func replacePathWithStrokedPath()](/documentation/coregraphics/cgcontext/replacepathwithstrokedpath())

### Examining the Current Graphics Path

- [var boundingBoxOfPath: CGRect](/documentation/coregraphics/cgcontext/boundingboxofpath)
- [var currentPointOfPath: CGPoint](/documentation/coregraphics/cgcontext/currentpointofpath)
- [var isPathEmpty: Bool](/documentation/coregraphics/cgcontext/ispathempty)
- [func pathContains(CGPoint, mode: CGPathDrawingMode) -> Bool](/documentation/coregraphics/cgcontext/pathcontains(_:mode:))

### Drawing the Current Graphics Path

- [func drawPath(using: CGPathDrawingMode)](/documentation/coregraphics/cgcontext/drawpath(using:))
- [CGPathDrawingMode](/documentation/coregraphics/cgpathdrawingmode)

#### Constants

- [case fill](/documentation/coregraphics/cgpathdrawingmode/fill)
- [case eoFill](/documentation/coregraphics/cgpathdrawingmode/eofill)
- [case stroke](/documentation/coregraphics/cgpathdrawingmode/stroke)
- [case fillStroke](/documentation/coregraphics/cgpathdrawingmode/fillstroke)
- [case eoFillStroke](/documentation/coregraphics/cgpathdrawingmode/eofillstroke)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpathdrawingmode/init(rawvalue:))
- [func fillPath(using: CGPathFillRule)](/documentation/coregraphics/cgcontext/fillpath(using:))
- [func strokePath()](/documentation/coregraphics/cgcontext/strokepath())

### Drawing Shapes

- [func clear(CGRect)](/documentation/coregraphics/cgcontext/clear(_:))
- [func fill(CGRect)](/documentation/coregraphics/cgcontext/fill(_:)-7a0rk)
- [func fill([CGRect])](/documentation/coregraphics/cgcontext/fill(_:)-6jc4y)
- [func fillEllipse(in: CGRect)](/documentation/coregraphics/cgcontext/fillellipse(in:))
- [func stroke(CGRect)](/documentation/coregraphics/cgcontext/stroke(_:))
- [func stroke(CGRect, width: CGFloat)](/documentation/coregraphics/cgcontext/stroke(_:width:))
- [func strokeEllipse(in: CGRect)](/documentation/coregraphics/cgcontext/strokeellipse(in:))
- [CGContextStrokeLineSegments](/documentation/coregraphics/cgcontext/strokelinesegments(between:))

### Drawing Images and PDF Content

- [func draw(CGImage, in: CGRect, byTiling: Bool)](/documentation/coregraphics/cgcontext/draw(_:in:bytiling:))
- [func drawPDFPage(CGPDFPage)](/documentation/coregraphics/cgcontext/drawpdfpage(_:))
- [var interpolationQuality: CGInterpolationQuality](/documentation/coregraphics/cgcontext/interpolationquality)
- [CGInterpolationQuality](/documentation/coregraphics/cginterpolationquality)

#### Constants

- [case `default`](/documentation/coregraphics/cginterpolationquality/default)
- [case none](/documentation/coregraphics/cginterpolationquality/none)
- [case low](/documentation/coregraphics/cginterpolationquality/low)
- [case medium](/documentation/coregraphics/cginterpolationquality/medium)
- [case high](/documentation/coregraphics/cginterpolationquality/high)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cginterpolationquality/init(rawvalue:))

### Drawing Gradients and Shadings

- [func drawLinearGradient(CGGradient, start: CGPoint, end: CGPoint, options: CGGradientDrawingOptions)](/documentation/coregraphics/cgcontext/drawlineargradient(_:start:end:options:))
- [func drawRadialGradient(CGGradient, startCenter: CGPoint, startRadius: CGFloat, endCenter: CGPoint, endRadius: CGFloat, options: CGGradientDrawingOptions)](/documentation/coregraphics/cgcontext/drawradialgradient(_:startcenter:startradius:endcenter:endradius:options:))
- [CGGradientDrawingOptions](/documentation/coregraphics/cggradientdrawingoptions)

#### Constants

- [static var drawsBeforeStartLocation: CGGradientDrawingOptions](/documentation/coregraphics/cggradientdrawingoptions/drawsbeforestartlocation)
- [static var drawsAfterEndLocation: CGGradientDrawingOptions](/documentation/coregraphics/cggradientdrawingoptions/drawsafterendlocation)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cggradientdrawingoptions/init(rawvalue:))
- [func drawShading(CGShading)](/documentation/coregraphics/cgcontext/drawshading(_:))

### Drawing Text

- [var textMatrix: CGAffineTransform](/documentation/coregraphics/cgcontext/textmatrix)
- [var textPosition: CGPoint](/documentation/coregraphics/cgcontext/textposition)
- [func selectFont(name: UnsafePointer<CChar>, size: CGFloat, textEncoding: CGTextEncoding)](/documentation/coregraphics/cgcontext/selectfont(name:size:textencoding:))
- [func setCharacterSpacing(CGFloat)](/documentation/coregraphics/cgcontext/setcharacterspacing(_:))
- [func setFont(CGFont)](/documentation/coregraphics/cgcontext/setfont(_:))
- [func setFontSize(CGFloat)](/documentation/coregraphics/cgcontext/setfontsize(_:))
- [func setTextDrawingMode(CGTextDrawingMode)](/documentation/coregraphics/cgcontext/settextdrawingmode(_:))
- [func setAllowsFontSmoothing(Bool)](/documentation/coregraphics/cgcontext/setallowsfontsmoothing(_:))
- [func setAllowsFontSubpixelPositioning(Bool)](/documentation/coregraphics/cgcontext/setallowsfontsubpixelpositioning(_:))
- [func setAllowsFontSubpixelQuantization(Bool)](/documentation/coregraphics/cgcontext/setallowsfontsubpixelquantization(_:))
- [func setShouldSmoothFonts(Bool)](/documentation/coregraphics/cgcontext/setshouldsmoothfonts(_:))
- [func setShouldSubpixelPositionFonts(Bool)](/documentation/coregraphics/cgcontext/setshouldsubpixelpositionfonts(_:))
- [func setShouldSubpixelQuantizeFonts(Bool)](/documentation/coregraphics/cgcontext/setshouldsubpixelquantizefonts(_:))
- [func showGlyphs(g: UnsafePointer<CGGlyph>?, count: Int)](/documentation/coregraphics/cgcontext/showglyphs(g:count:))
- [CGContextShowGlyphsAtPositions](/documentation/coregraphics/cgcontext/showglyphs(_:at:))
- [func showGlyphsAtPoint(x: CGFloat, y: CGFloat, glyphs: UnsafePointer<CGGlyph>?, count: Int)](/documentation/coregraphics/cgcontext/showglyphsatpoint(x:y:glyphs:count:))
- [func showGlyphsWithAdvances(glyphs: UnsafePointer<CGGlyph>?, advances: UnsafePointer<CGSize>?, count: Int)](/documentation/coregraphics/cgcontext/showglyphswithadvances(glyphs:advances:count:))
- [func showText(string: UnsafePointer<CChar>, length: Int)](/documentation/coregraphics/cgcontext/showtext(string:length:))
- [func showTextAtPoint(x: CGFloat, y: CGFloat, string: UnsafePointer<CChar>, length: Int)](/documentation/coregraphics/cgcontext/showtextatpoint(x:y:string:length:))
- [CGTextDrawingMode](/documentation/coregraphics/cgtextdrawingmode)

#### Constants

- [case fill](/documentation/coregraphics/cgtextdrawingmode/fill)
- [case stroke](/documentation/coregraphics/cgtextdrawingmode/stroke)
- [case fillStroke](/documentation/coregraphics/cgtextdrawingmode/fillstroke)
- [case invisible](/documentation/coregraphics/cgtextdrawingmode/invisible)
- [case fillClip](/documentation/coregraphics/cgtextdrawingmode/fillclip)
- [case strokeClip](/documentation/coregraphics/cgtextdrawingmode/strokeclip)
- [case fillStrokeClip](/documentation/coregraphics/cgtextdrawingmode/fillstrokeclip)
- [case clip](/documentation/coregraphics/cgtextdrawingmode/clip)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgtextdrawingmode/init(rawvalue:))

### Drawing Core Graphics Layers

- [CGContextDrawLayerAtPoint](/documentation/coregraphics/cgcontext/draw(_:at:))
- [CGContextDrawLayerInRect](/documentation/coregraphics/cgcontext/draw(_:in:))

### Setting Fill, Stroke, and Shadow Colors

- [func setFillColor(CGColor)](/documentation/coregraphics/cgcontext/setfillcolor(_:)-8lhn8)
- [func setFillColor(UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcontext/setfillcolor(_:)-756dy)
- [func setFillColor(cyan: CGFloat, magenta: CGFloat, yellow: CGFloat, black: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setfillcolor(cyan:magenta:yellow:black:alpha:))
- [func setFillColor(gray: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setfillcolor(gray:alpha:))
- [func setFillColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setfillcolor(red:green:blue:alpha:))
- [func setFillColorSpace(CGColorSpace)](/documentation/coregraphics/cgcontext/setfillcolorspace(_:))
- [func setShadow(offset: CGSize, blur: CGFloat)](/documentation/coregraphics/cgcontext/setshadow(offset:blur:))
- [func setShadow(offset: CGSize, blur: CGFloat, color: CGColor?)](/documentation/coregraphics/cgcontext/setshadow(offset:blur:color:))
- [func setStrokeColor(CGColor)](/documentation/coregraphics/cgcontext/setstrokecolor(_:)-1sskg)
- [func setStrokeColor(UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcontext/setstrokecolor(_:)-4pd8p)
- [func setStrokeColor(cyan: CGFloat, magenta: CGFloat, yellow: CGFloat, black: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setstrokecolor(cyan:magenta:yellow:black:alpha:))
- [func setStrokeColor(gray: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setstrokecolor(gray:alpha:))
- [func setStrokeColor(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcontext/setstrokecolor(red:green:blue:alpha:))
- [func setStrokeColorSpace(CGColorSpace)](/documentation/coregraphics/cgcontext/setstrokecolorspace(_:))
- [func setStrokePattern(CGPattern, colorComponents: UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcontext/setstrokepattern(_:colorcomponents:))
- [func setAlpha(CGFloat)](/documentation/coregraphics/cgcontext/setalpha(_:))

### Working with the Current Clipping Path

- [func clip(using: CGPathFillRule)](/documentation/coregraphics/cgcontext/clip(using:))
- [func clip(to: CGRect)](/documentation/coregraphics/cgcontext/clip(to:)-7cbwq)
- [func clip(to: [CGRect])](/documentation/coregraphics/cgcontext/clip(to:)-2eg0)
- [func clip(to: CGRect, mask: CGImage)](/documentation/coregraphics/cgcontext/clip(to:mask:))
- [var boundingBoxOfClipPath: CGRect](/documentation/coregraphics/cgcontext/boundingboxofclippath)

### Working with Transparency Layers

- [func beginTransparencyLayer(in: CGRect, auxiliaryInfo: CFDictionary?)](/documentation/coregraphics/cgcontext/begintransparencylayer(in:auxiliaryinfo:))
- [func beginTransparencyLayer(auxiliaryInfo: CFDictionary?)](/documentation/coregraphics/cgcontext/begintransparencylayer(auxiliaryinfo:))
- [func endTransparencyLayer()](/documentation/coregraphics/cgcontext/endtransparencylayer())

### Working with the Current Transformation Matrix

- [var ctm: CGAffineTransform](/documentation/coregraphics/cgcontext/ctm)
- [func rotate(by: CGFloat)](/documentation/coregraphics/cgcontext/rotate(by:))
- [func scaleBy(x: CGFloat, y: CGFloat)](/documentation/coregraphics/cgcontext/scaleby(x:y:))
- [func translateBy(x: CGFloat, y: CGFloat)](/documentation/coregraphics/cgcontext/translateby(x:y:))
- [func concatenate(CGAffineTransform)](/documentation/coregraphics/cgcontext/concatenate(_:))

### Setting Path Drawing Options

- [func setAllowsAntialiasing(Bool)](/documentation/coregraphics/cgcontext/setallowsantialiasing(_:))
- [func setFlatness(CGFloat)](/documentation/coregraphics/cgcontext/setflatness(_:))
- [func setLineCap(CGLineCap)](/documentation/coregraphics/cgcontext/setlinecap(_:))
- [CGContextSetLineDash](/documentation/coregraphics/cgcontext/setlinedash(phase:lengths:))
- [func setLineJoin(CGLineJoin)](/documentation/coregraphics/cgcontext/setlinejoin(_:))
- [func setLineWidth(CGFloat)](/documentation/coregraphics/cgcontext/setlinewidth(_:))
- [func setMiterLimit(CGFloat)](/documentation/coregraphics/cgcontext/setmiterlimit(_:))
- [func setPatternPhase(CGSize)](/documentation/coregraphics/cgcontext/setpatternphase(_:))
- [func setFillPattern(CGPattern, colorComponents: UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcontext/setfillpattern(_:colorcomponents:))
- [func setShouldAntialias(Bool)](/documentation/coregraphics/cgcontext/setshouldantialias(_:))

### Saving and Restoring Graphics State

- [func saveGState()](/documentation/coregraphics/cgcontext/savegstate())
- [func restoreGState()](/documentation/coregraphics/cgcontext/restoregstate())

### Managing a Graphics Context

- [func flush()](/documentation/coregraphics/cgcontext/flush())
- [func synchronize()](/documentation/coregraphics/cgcontext/synchronize())
- [func setBlendMode(CGBlendMode)](/documentation/coregraphics/cgcontext/setblendmode(_:))
- [CGBlendMode](/documentation/coregraphics/cgblendmode)

#### Constants

- [case normal](/documentation/coregraphics/cgblendmode/normal)
- [case multiply](/documentation/coregraphics/cgblendmode/multiply)
- [case screen](/documentation/coregraphics/cgblendmode/screen)
- [case overlay](/documentation/coregraphics/cgblendmode/overlay)
- [case darken](/documentation/coregraphics/cgblendmode/darken)
- [case lighten](/documentation/coregraphics/cgblendmode/lighten)
- [case colorDodge](/documentation/coregraphics/cgblendmode/colordodge)
- [case colorBurn](/documentation/coregraphics/cgblendmode/colorburn)
- [case softLight](/documentation/coregraphics/cgblendmode/softlight)
- [case hardLight](/documentation/coregraphics/cgblendmode/hardlight)
- [case difference](/documentation/coregraphics/cgblendmode/difference)
- [case exclusion](/documentation/coregraphics/cgblendmode/exclusion)
- [case hue](/documentation/coregraphics/cgblendmode/hue)
- [case saturation](/documentation/coregraphics/cgblendmode/saturation)
- [case color](/documentation/coregraphics/cgblendmode/color)
- [case luminosity](/documentation/coregraphics/cgblendmode/luminosity)
- [case clear](/documentation/coregraphics/cgblendmode/clear)
- [case copy](/documentation/coregraphics/cgblendmode/copy)
- [case sourceIn](/documentation/coregraphics/cgblendmode/sourcein)
- [case sourceOut](/documentation/coregraphics/cgblendmode/sourceout)
- [case sourceAtop](/documentation/coregraphics/cgblendmode/sourceatop)
- [case destinationOver](/documentation/coregraphics/cgblendmode/destinationover)
- [case destinationIn](/documentation/coregraphics/cgblendmode/destinationin)
- [case destinationOut](/documentation/coregraphics/cgblendmode/destinationout)
- [case destinationAtop](/documentation/coregraphics/cgblendmode/destinationatop)
- [case xor](/documentation/coregraphics/cgblendmode/xor)
- [case plusDarker](/documentation/coregraphics/cgblendmode/plusdarker)
- [case plusLighter](/documentation/coregraphics/cgblendmode/pluslighter)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgblendmode/init(rawvalue:))
- [func setRenderingIntent(CGColorRenderingIntent)](/documentation/coregraphics/cgcontext/setrenderingintent(_:))

### Managing a Bitmap Graphics Context

- [var bitmapInfo: CGBitmapInfo](/documentation/coregraphics/cgcontext/bitmapinfo)
- [var alphaInfo: CGImageAlphaInfo](/documentation/coregraphics/cgcontext/alphainfo)
- [var bitsPerComponent: Int](/documentation/coregraphics/cgcontext/bitspercomponent)
- [var bitsPerPixel: Int](/documentation/coregraphics/cgcontext/bitsperpixel)
- [var bytesPerRow: Int](/documentation/coregraphics/cgcontext/bytesperrow)
- [var colorSpace: CGColorSpace?](/documentation/coregraphics/cgcontext/colorspace)
- [var data: UnsafeMutableRawPointer?](/documentation/coregraphics/cgcontext/data)
- [var height: Int](/documentation/coregraphics/cgcontext/height)
- [var width: Int](/documentation/coregraphics/cgcontext/width)
- [func makeImage() -> CGImage?](/documentation/coregraphics/cgcontext/makeimage())

### Managing a PDF Graphics Context

- [func beginPDFPage(CFDictionary?)](/documentation/coregraphics/cgcontext/beginpdfpage(_:))
- [func endPDFPage()](/documentation/coregraphics/cgcontext/endpdfpage())
- [func addDestination(CFString, at: CGPoint)](/documentation/coregraphics/cgcontext/adddestination(_:at:))
- [func setDestination(CFString, for: CGRect)](/documentation/coregraphics/cgcontext/setdestination(_:for:))
- [func setURL(CFURL, for: CGRect)](/documentation/coregraphics/cgcontext/seturl(_:for:))
- [func addDocumentMetadata(CFData?)](/documentation/coregraphics/cgcontext/adddocumentmetadata(_:))
- [func closePDF()](/documentation/coregraphics/cgcontext/closepdf())

### Managing a Page-Based Graphics Context

- [func beginPage(mediaBox: UnsafePointer<CGRect>?)](/documentation/coregraphics/cgcontext/beginpage(mediabox:))
- [func endPage()](/documentation/coregraphics/cgcontext/endpage())

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgcontext/typeid)

### Constants

- [CGPathFillRule](/documentation/coregraphics/cgpathfillrule)

#### Enumeration Cases

- [case evenOdd](/documentation/coregraphics/cgpathfillrule/evenodd)
- [case winding](/documentation/coregraphics/cgpathfillrule/winding)
- [CGTextEncoding](/documentation/coregraphics/cgtextencoding)

#### Constants

- [case encodingFontSpecific](/documentation/coregraphics/cgtextencoding/encodingfontspecific)
- [case encodingMacRoman](/documentation/coregraphics/cgtextencoding/encodingmacroman)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgtextencoding/init(rawvalue:))

### Instance Methods

- [func draw(CGImage, in: CGRect, by: CGToneMapping, options: CFDictionary?) -> Bool](/documentation/coregraphics/cgcontext/draw(_:in:by:options:))
- [func resetClip()](/documentation/coregraphics/cgcontext/resetclip())
- [func setEDRTargetHeadroom(Float) -> Bool](/documentation/coregraphics/cgcontext/setedrtargetheadroom(_:))
- [func synchronizeAttributes()](/documentation/coregraphics/cgcontext/synchronizeattributes())

### Structures

- [CGContext.AuxiliaryInfo](/documentation/coregraphics/cgcontext/auxiliaryinfo)

#### Initializers

- [init()](/documentation/coregraphics/cgcontext/auxiliaryinfo/init())
- [init(maximumBitDepth: CGComponent)](/documentation/coregraphics/cgcontext/auxiliaryinfo/init(maximumbitdepth:))

#### Instance Properties

- [var maximumBitDepth: CGComponent](/documentation/coregraphics/cgcontext/auxiliaryinfo/maximumbitdepth)

### Initializers

- [init?(data: UnsafeMutableRawPointer?, width: Int, height: Int, bitsPerComponent: Int, bytesPerRow: Int, space: CGColorSpace?, bitmapInfo: CGBitmapInfo)](/documentation/coregraphics/cgcontext/init(data:width:height:bitspercomponent:bytesperrow:space:bitmapinfo:)-10b3i)
- [init?(data: UnsafeMutableRawPointer?, width: Int, height: Int, bitsPerComponent: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: UInt32)](/documentation/coregraphics/cgcontext/init(data:width:height:bitspercomponent:bytesperrow:space:bitmapinfo:)-4fkaf)
- [init?(data: UnsafeMutableRawPointer?, width: Int, height: Int, bitsPerComponent: Int, bytesPerRow: Int, space: CGColorSpace?, bitmapInfo: CGBitmapInfo, releaseCallback: CGBitmapContextReleaseDataCallback?, releaseInfo: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgcontext/init(data:width:height:bitspercomponent:bytesperrow:space:bitmapinfo:releasecallback:releaseinfo:)-4yzt5)
- [init?(data: UnsafeMutableRawPointer?, width: Int, height: Int, bitsPerComponent: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: UInt32, releaseCallback: CGBitmapContextReleaseDataCallback?, releaseInfo: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgcontext/init(data:width:height:bitspercomponent:bytesperrow:space:bitmapinfo:releasecallback:releaseinfo:)-71ea9)

### Instance Properties

- [var contentToneMappingInfo: CGContentToneMappingInfo](/documentation/coregraphics/cgcontext/contenttonemappinginfo)
- [CGImage](/documentation/coregraphics/cgimage)

### Creating images

- [init?(width: Int, height: Int, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: CGBitmapInfo, provider: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)](/documentation/coregraphics/cgimage/init(width:height:bitspercomponent:bitsperpixel:bytesperrow:space:bitmapinfo:provider:decode:shouldinterpolate:intent:))
- [init?(jpegDataProviderSource: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)](/documentation/coregraphics/cgimage/init(jpegdataprovidersource:decode:shouldinterpolate:intent:))
- [init?(pngDataProviderSource: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)](/documentation/coregraphics/cgimage/init(pngdataprovidersource:decode:shouldinterpolate:intent:))
- [init?(headroom: Float, width: Int, height: Int, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: CGBitmapInfo, provider: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)](/documentation/coregraphics/cgimage/init(headroom:width:height:bitspercomponent:bitsperpixel:bytesperrow:space:bitmapinfo:provider:decode:shouldinterpolate:intent:))

### Examining an image

- [var isMask: Bool](/documentation/coregraphics/cgimage/ismask)
- [var width: Int](/documentation/coregraphics/cgimage/width)
- [var height: Int](/documentation/coregraphics/cgimage/height)
- [var bitsPerComponent: Int](/documentation/coregraphics/cgimage/bitspercomponent)
- [var bitsPerPixel: Int](/documentation/coregraphics/cgimage/bitsperpixel)
- [var bytesPerRow: Int](/documentation/coregraphics/cgimage/bytesperrow)
- [var colorSpace: CGColorSpace?](/documentation/coregraphics/cgimage/colorspace)
- [var alphaInfo: CGImageAlphaInfo](/documentation/coregraphics/cgimage/alphainfo)
- [CGImageAlphaInfo](/documentation/coregraphics/cgimagealphainfo)

#### Constants

- [case first](/documentation/coregraphics/cgimagealphainfo/first)
- [case last](/documentation/coregraphics/cgimagealphainfo/last)
- [case none](/documentation/coregraphics/cgimagealphainfo/none)
- [case noneSkipFirst](/documentation/coregraphics/cgimagealphainfo/noneskipfirst)
- [case alphaOnly](/documentation/coregraphics/cgimagealphainfo/alphaonly)
- [case noneSkipLast](/documentation/coregraphics/cgimagealphainfo/noneskiplast)
- [case premultipliedFirst](/documentation/coregraphics/cgimagealphainfo/premultipliedfirst)
- [case premultipliedLast](/documentation/coregraphics/cgimagealphainfo/premultipliedlast)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgimagealphainfo/init(rawvalue:))
- [var dataProvider: CGDataProvider?](/documentation/coregraphics/cgimage/dataprovider)
- [var decode: UnsafePointer<CGFloat>?](/documentation/coregraphics/cgimage/decode)
- [var shouldInterpolate: Bool](/documentation/coregraphics/cgimage/shouldinterpolate)
- [var renderingIntent: CGColorRenderingIntent](/documentation/coregraphics/cgimage/renderingintent)
- [var bitmapInfo: CGBitmapInfo](/documentation/coregraphics/cgimage/bitmapinfo)
- [CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo)

#### Constants

- [static var alphaInfoMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/alphainfomask)
- [static var floatComponents: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/floatcomponents)
- [static var byteOrderMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteordermask)
- [static var byteOrderDefault: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorderdefault)
- [static var byteOrder16Little: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder16little)
- [static var byteOrder32Little: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder32little)
- [static var byteOrder16Big: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder16big)
- [static var byteOrder32Big: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder32big)
- [static var floatInfoMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/floatinfomask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgbitmapinfo/init(rawvalue:))
- [init(some Sequence<CGBitmapInfo>)](/documentation/coregraphics/cgbitmapinfo/init(_:))
- [init(alpha: CGImageAlphaInfo, component: CGImageComponentInfo, byteOrder: CGImageByteOrderInfo)](/documentation/coregraphics/cgbitmapinfo/init(alpha:component:byteorder:))
- [init(alpha: CGImageAlphaInfo, component: CGImageComponentInfo, byteOrder: CGImageByteOrderInfo, pixelFormat: CGImagePixelFormatInfo)](/documentation/coregraphics/cgbitmapinfo/init(alpha:component:byteorder:pixelformat:))
- [init(arrayLiteral: CGBitmapInfo...)](/documentation/coregraphics/cgbitmapinfo/init(arrayliteral:))

#### Instance Properties

- [var alpha: CGImageAlphaInfo](/documentation/coregraphics/cgbitmapinfo/alpha)
- [var byteOrder: CGImageByteOrderInfo](/documentation/coregraphics/cgbitmapinfo/byteorder)
- [var component: CGImageComponentInfo](/documentation/coregraphics/cgbitmapinfo/component)
- [var isEmpty: Bool](/documentation/coregraphics/cgbitmapinfo/isempty)
- [var pixelFormat: CGImagePixelFormatInfo](/documentation/coregraphics/cgbitmapinfo/pixelformat)

#### Instance Methods

- [func formIntersection(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formintersection(_:))
- [func formSymmetricDifference(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formsymmetricdifference(_:))
- [func formUnion(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formunion(_:))
- [func insert(CGBitmapInfo) -> (inserted: Bool, memberAfterInsert: CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/insert(_:))
- [func intersection(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/intersection(_:))
- [func isDisjoint(with: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/isdisjoint(with:))
- [func isSubset(of: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/issubset(of:))
- [func isSuperset(of: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/issuperset(of:))
- [func remove(CGBitmapInfo) -> CGBitmapInfo?](/documentation/coregraphics/cgbitmapinfo/remove(_:))
- [func subtract(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/subtract(_:))
- [func subtracting(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/subtracting(_:))
- [func symmetricDifference(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/symmetricdifference(_:))
- [func update(with: CGBitmapInfo) -> CGBitmapInfo?](/documentation/coregraphics/cgbitmapinfo/update(with:))
- [var utType: CFString?](/documentation/coregraphics/cgimage/uttype)

### Copying an image

- [func copy() -> CGImage?](/documentation/coregraphics/cgimage/copy())
- [func copy(colorSpace: CGColorSpace) -> CGImage?](/documentation/coregraphics/cgimage/copy(colorspace:))

### Creating images by modifying an image

- [func cropping(to: CGRect) -> CGImage?](/documentation/coregraphics/cgimage/cropping(to:))
- [func masking(CGImage) -> CGImage?](/documentation/coregraphics/cgimage/masking(_:))
- [CGImageCreateWithMaskingColors](/documentation/coregraphics/cgimage/copy(maskingcolorcomponents:))

### Creating image masks

- [init?(maskWidth: Int, height: Int, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int, provider: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool)](/documentation/coregraphics/cgimage/init(maskwidth:height:bitspercomponent:bitsperpixel:bytesperrow:provider:decode:shouldinterpolate:))

### Adopting high dynamic range (HDR)

- [Enhancing high dynamic range image rendering](/documentation/coregraphics/adopting-advancements-in-hdr-image-rendering)
- [var contentHeadroom: Float](/documentation/coregraphics/cgimage/contentheadroom)
- [var calculatedContentHeadroom: Float](/documentation/coregraphics/cgimage/calculatedcontentheadroom)
- [var contentAverageLightLevel: Float](/documentation/coregraphics/cgimage/contentaveragelightlevel)
- [var calculatedContentAverageLightLevel: Float](/documentation/coregraphics/cgimage/calculatedcontentaveragelightlevel)
- [func copy(contentAverageLightLevel: Float) -> CGImage?](/documentation/coregraphics/cgimage/copy(contentaveragelightlevel:))
- [func copyWithCalculatedHDRStats() -> CGImage?](/documentation/coregraphics/cgimage/copywithcalculatedhdrstats())

### Constants

- [CGImageAlphaInfo](/documentation/coregraphics/cgimagealphainfo)

#### Constants

- [case first](/documentation/coregraphics/cgimagealphainfo/first)
- [case last](/documentation/coregraphics/cgimagealphainfo/last)
- [case none](/documentation/coregraphics/cgimagealphainfo/none)
- [case noneSkipFirst](/documentation/coregraphics/cgimagealphainfo/noneskipfirst)
- [case alphaOnly](/documentation/coregraphics/cgimagealphainfo/alphaonly)
- [case noneSkipLast](/documentation/coregraphics/cgimagealphainfo/noneskiplast)
- [case premultipliedFirst](/documentation/coregraphics/cgimagealphainfo/premultipliedfirst)
- [case premultipliedLast](/documentation/coregraphics/cgimagealphainfo/premultipliedlast)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgimagealphainfo/init(rawvalue:))
- [CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo)

#### Constants

- [static var alphaInfoMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/alphainfomask)
- [static var floatComponents: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/floatcomponents)
- [static var byteOrderMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteordermask)
- [static var byteOrderDefault: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorderdefault)
- [static var byteOrder16Little: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder16little)
- [static var byteOrder32Little: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder32little)
- [static var byteOrder16Big: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder16big)
- [static var byteOrder32Big: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/byteorder32big)
- [static var floatInfoMask: CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/floatinfomask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgbitmapinfo/init(rawvalue:))
- [init(some Sequence<CGBitmapInfo>)](/documentation/coregraphics/cgbitmapinfo/init(_:))
- [init(alpha: CGImageAlphaInfo, component: CGImageComponentInfo, byteOrder: CGImageByteOrderInfo)](/documentation/coregraphics/cgbitmapinfo/init(alpha:component:byteorder:))
- [init(alpha: CGImageAlphaInfo, component: CGImageComponentInfo, byteOrder: CGImageByteOrderInfo, pixelFormat: CGImagePixelFormatInfo)](/documentation/coregraphics/cgbitmapinfo/init(alpha:component:byteorder:pixelformat:))
- [init(arrayLiteral: CGBitmapInfo...)](/documentation/coregraphics/cgbitmapinfo/init(arrayliteral:))

#### Instance Properties

- [var alpha: CGImageAlphaInfo](/documentation/coregraphics/cgbitmapinfo/alpha)
- [var byteOrder: CGImageByteOrderInfo](/documentation/coregraphics/cgbitmapinfo/byteorder)
- [var component: CGImageComponentInfo](/documentation/coregraphics/cgbitmapinfo/component)
- [var isEmpty: Bool](/documentation/coregraphics/cgbitmapinfo/isempty)
- [var pixelFormat: CGImagePixelFormatInfo](/documentation/coregraphics/cgbitmapinfo/pixelformat)

#### Instance Methods

- [func formIntersection(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formintersection(_:))
- [func formSymmetricDifference(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formsymmetricdifference(_:))
- [func formUnion(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/formunion(_:))
- [func insert(CGBitmapInfo) -> (inserted: Bool, memberAfterInsert: CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/insert(_:))
- [func intersection(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/intersection(_:))
- [func isDisjoint(with: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/isdisjoint(with:))
- [func isSubset(of: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/issubset(of:))
- [func isSuperset(of: CGBitmapInfo) -> Bool](/documentation/coregraphics/cgbitmapinfo/issuperset(of:))
- [func remove(CGBitmapInfo) -> CGBitmapInfo?](/documentation/coregraphics/cgbitmapinfo/remove(_:))
- [func subtract(CGBitmapInfo)](/documentation/coregraphics/cgbitmapinfo/subtract(_:))
- [func subtracting(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/subtracting(_:))
- [func symmetricDifference(CGBitmapInfo) -> CGBitmapInfo](/documentation/coregraphics/cgbitmapinfo/symmetricdifference(_:))
- [func update(with: CGBitmapInfo) -> CGBitmapInfo?](/documentation/coregraphics/cgbitmapinfo/update(with:))
- [Host Endian Bitmap Formats](/documentation/coregraphics/host-endian-bitmap-formats)

#### Constants

- [let kCGBitmapByteOrder16Host: CGBitmapInfo](/documentation/coregraphics/kcgbitmapbyteorder16host)
- [let kCGBitmapByteOrder32Host: CGBitmapInfo](/documentation/coregraphics/kcgbitmapbyteorder32host)

### Working with Core Foundation types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgimage/typeid)

### Instance properties

- [var byteOrderInfo: CGImageByteOrderInfo](/documentation/coregraphics/cgimage/byteorderinfo)
- [var containsImageSpecificToneMappingMetadata: Bool](/documentation/coregraphics/cgimage/containsimagespecifictonemappingmetadata)
- [var contentHeadroom: Float](/documentation/coregraphics/cgimage/contentheadroom)
- [var pixelFormatInfo: CGImagePixelFormatInfo](/documentation/coregraphics/cgimage/pixelformatinfo)
- [var shouldToneMap: Bool](/documentation/coregraphics/cgimage/shouldtonemap)
- [CGPath](/documentation/coregraphics/cgpath)

### Creating Graphics Paths

- [init(rect: CGRect, transform: UnsafePointer<CGAffineTransform>?)](/documentation/coregraphics/cgpath/init(rect:transform:))
- [init(ellipseIn: CGRect, transform: UnsafePointer<CGAffineTransform>?)](/documentation/coregraphics/cgpath/init(ellipsein:transform:))
- [init(roundedRect: CGRect, cornerWidth: CGFloat, cornerHeight: CGFloat, transform: UnsafePointer<CGAffineTransform>?)](/documentation/coregraphics/cgpath/init(roundedrect:cornerwidth:cornerheight:transform:))

### Copying a Graphics Path

- [func copy() -> CGPath?](/documentation/coregraphics/cgpath/copy())
- [func copy(using: UnsafePointer<CGAffineTransform>?) -> CGPath?](/documentation/coregraphics/cgpath/copy(using:))
- [CGPathCreateCopyByDashingPath](/documentation/coregraphics/cgpath/copy(dashingwithphase:lengths:transform:))
- [CGPathCreateCopyByStrokingPath](/documentation/coregraphics/cgpath/copy(strokingwithwidth:linecap:linejoin:miterlimit:transform:))
- [func mutableCopy() -> CGMutablePath?](/documentation/coregraphics/cgpath/mutablecopy())
- [func mutableCopy(using: UnsafePointer<CGAffineTransform>?) -> CGMutablePath?](/documentation/coregraphics/cgpath/mutablecopy(using:))

### Examining a Graphics Path

- [var boundingBox: CGRect](/documentation/coregraphics/cgpath/boundingbox)
- [var boundingBoxOfPath: CGRect](/documentation/coregraphics/cgpath/boundingboxofpath)
- [var currentPoint: CGPoint](/documentation/coregraphics/cgpath/currentpoint)
- [func contains(CGPoint, using: CGPathFillRule, transform: CGAffineTransform) -> Bool](/documentation/coregraphics/cgpath/contains(_:using:transform:))
- [var isEmpty: Bool](/documentation/coregraphics/cgpath/isempty)
- [func isRect(UnsafeMutablePointer<CGRect>?) -> Bool](/documentation/coregraphics/cgpath/isrect(_:))

### Applying a Function to the Elements of a Path

- [func apply(info: UnsafeMutableRawPointer?, function: CGPathApplierFunction)](/documentation/coregraphics/cgpath/apply(info:function:))
- [CGPathApplierFunction](/documentation/coregraphics/cgpathapplierfunction)
- [CGPathElement](/documentation/coregraphics/cgpathelement)

#### Initializers

- [init(type: CGPathElementType, points: UnsafeMutablePointer<CGPoint>)](/documentation/coregraphics/cgpathelement/init(type:points:))

#### Instance Properties

- [var points: UnsafeMutablePointer<CGPoint>](/documentation/coregraphics/cgpathelement/points)
- [var type: CGPathElementType](/documentation/coregraphics/cgpathelement/type)
- [CGPathElementType](/documentation/coregraphics/cgpathelementtype)

#### Constants

- [case moveToPoint](/documentation/coregraphics/cgpathelementtype/movetopoint)
- [case addLineToPoint](/documentation/coregraphics/cgpathelementtype/addlinetopoint)
- [case addQuadCurveToPoint](/documentation/coregraphics/cgpathelementtype/addquadcurvetopoint)
- [case addCurveToPoint](/documentation/coregraphics/cgpathelementtype/addcurvetopoint)
- [case closeSubpath](/documentation/coregraphics/cgpathelementtype/closesubpath)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpathelementtype/init(rawvalue:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgpath/typeid)

### Instance Methods

- [func applyWithBlock((UnsafePointer<CGPathElement>) -> Void)](/documentation/coregraphics/cgpath/applywithblock(_:))
- [func componentsSeparated(using: CGPathFillRule) -> [CGPath]](/documentation/coregraphics/cgpath/componentsseparated(using:))
- [func flattened(threshold: CGFloat) -> CGPath](/documentation/coregraphics/cgpath/flattened(threshold:))
- [func intersection(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/intersection(_:using:))
- [func intersects(CGPath, using: CGPathFillRule) -> Bool](/documentation/coregraphics/cgpath/intersects(_:using:))
- [func lineIntersection(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/lineintersection(_:using:))
- [func lineSubtracting(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/linesubtracting(_:using:))
- [func normalized(using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/normalized(using:))
- [func subtracting(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/subtracting(_:using:))
- [func symmetricDifference(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/symmetricdifference(_:using:))
- [func union(CGPath, using: CGPathFillRule) -> CGPath](/documentation/coregraphics/cgpath/union(_:using:))
- [CGMutablePath](/documentation/coregraphics/cgmutablepath)

### Creating Graphics Paths

- [init()](/documentation/coregraphics/cgmutablepath/init())

### Copying a Graphics Path

- [func mutableCopy() -> CGMutablePath?](/documentation/coregraphics/cgpath/mutablecopy())
- [func mutableCopy(using: UnsafePointer<CGAffineTransform>?) -> CGMutablePath?](/documentation/coregraphics/cgpath/mutablecopy(using:))

### Constructing a Graphics Path

- [CGPathMoveToPoint](/documentation/coregraphics/cgmutablepath/move(to:transform:))
- [func addLine(to: CGPoint, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addline(to:transform:))
- [func addLines(between: [CGPoint], transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addlines(between:transform:))
- [func addRect(CGRect, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addrect(_:transform:))
- [func addRects([CGRect], transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addrects(_:transform:))
- [func addEllipse(in: CGRect, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addellipse(in:transform:))
- [func addRoundedRect(in: CGRect, cornerWidth: CGFloat, cornerHeight: CGFloat, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addroundedrect(in:cornerwidth:cornerheight:transform:))
- [func addArc(center: CGPoint, radius: CGFloat, startAngle: CGFloat, endAngle: CGFloat, clockwise: Bool, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addarc(center:radius:startangle:endangle:clockwise:transform:))
- [func addArc(tangent1End: CGPoint, tangent2End: CGPoint, radius: CGFloat, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addarc(tangent1end:tangent2end:radius:transform:))
- [func addRelativeArc(center: CGPoint, radius: CGFloat, startAngle: CGFloat, delta: CGFloat, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addrelativearc(center:radius:startangle:delta:transform:))
- [func addCurve(to: CGPoint, control1: CGPoint, control2: CGPoint, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addcurve(to:control1:control2:transform:))
- [func addQuadCurve(to: CGPoint, control: CGPoint, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addquadcurve(to:control:transform:))
- [func addPath(CGPath, transform: CGAffineTransform)](/documentation/coregraphics/cgmutablepath/addpath(_:transform:))
- [func closeSubpath()](/documentation/coregraphics/cgmutablepath/closesubpath())
- [CGLayer](/documentation/coregraphics/cglayer)

### Creating Layer Objects

- [init?(CGContext, size: CGSize, auxiliaryInfo: CFDictionary?)](/documentation/coregraphics/cglayer/init(_:size:auxiliaryinfo:))

### Examining a Layer

- [var context: CGContext?](/documentation/coregraphics/cglayer/context)
- [var size: CGSize](/documentation/coregraphics/cglayer/size)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cglayer/typeid)

## Colors and Fonts

- [CGColor](/documentation/coregraphics/cgcolor)

### Creating Colors

- [func copy() -> CGColor?](/documentation/coregraphics/cgcolor/copy())
- [func copy(alpha: CGFloat) -> CGColor?](/documentation/coregraphics/cgcolor/copy(alpha:))
- [init(genericCMYKCyan: CGFloat, magenta: CGFloat, yellow: CGFloat, black: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(genericcmykcyan:magenta:yellow:black:alpha:))
- [init(gray: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(gray:alpha:))
- [init(genericGrayGamma2_2Gray: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(genericgraygamma2_2gray:alpha:))
- [init(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(red:green:blue:alpha:))
- [init(srgbRed: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(srgbred:green:blue:alpha:))
- [init?(colorSpace: CGColorSpace, components: UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcolor/init(colorspace:components:))
- [init?(patternSpace: CGColorSpace, pattern: CGPattern, components: UnsafePointer<CGFloat>)](/documentation/coregraphics/cgcolor/init(patternspace:pattern:components:))

### Getting System Colors

- [kCGColorBlack](/documentation/coregraphics/cgcolor/black)
- [kCGColorWhite](/documentation/coregraphics/cgcolor/white)
- [kCGColorClear](/documentation/coregraphics/cgcolor/clear)

### Examining a Color

- [var alpha: CGFloat](/documentation/coregraphics/cgcolor/alpha)
- [var colorSpace: CGColorSpace?](/documentation/coregraphics/cgcolor/colorspace)
- [var components: [CGFloat]?](/documentation/coregraphics/cgcolor/components)
- [var numberOfComponents: Int](/documentation/coregraphics/cgcolor/numberofcomponents)
- [var pattern: CGPattern?](/documentation/coregraphics/cgcolor/pattern)

### Converting Between Color Spaces

- [class let conversionTRCSize: CFString](/documentation/coregraphics/cgcolor/conversiontrcsize)
- [func converted(to: CGColorSpace, intent: CGColorRenderingIntent, options: CFDictionary?) -> CGColor?](/documentation/coregraphics/cgcolor/converted(to:intent:options:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgcolor/typeid)

### Type Properties

- [class let conversionBlackPointCompensation: CFString](/documentation/coregraphics/cgcolor/conversionblackpointcompensation)

### Initializers

- [init?(headroom: Float, colorSpace: CGColorSpace, red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(headroom:colorspace:red:green:blue:alpha:))

### Instance Properties

- [var contentHeadroom: Float](/documentation/coregraphics/cgcolor/contentheadroom)
- [CGColorConversionInfo](/documentation/coregraphics/cgcolorconversioninfo)

### Creating a Color Conversion

- [init?(src: CGColorSpace, dst: CGColorSpace)](/documentation/coregraphics/cgcolorconversioninfo/init(src:dst:))
- [init?(optionsSrc: CGColorSpace, dst: CGColorSpace, options: CFDictionary?)](/documentation/coregraphics/cgcolorconversioninfo/init(optionssrc:dst:options:))
- [CGColorConversionInfoTransformType](/documentation/coregraphics/cgcolorconversioninfotransformtype)

#### Enumeration Cases

- [case transformApplySpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformapplyspace)
- [case transformFromSpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformfromspace)
- [case transformToSpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformtospace)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgcolorconversioninfotransformtype/init(rawvalue:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgcolorconversioninfo/typeid)

### Instance Methods

- [func convert(width: Int, height: Int, to: UnsafeMutableRawPointer, format: CGColorBufferFormat, from: UnsafeRawPointer, format: CGColorBufferFormat, options: CFDictionary?) -> Bool](/documentation/coregraphics/cgcolorconversioninfo/convert(width:height:to:format:from:format:options:))

### Initializers

- [init?(src: CGColorSpace, srcHeadroom: Float, dst: CGColorSpace, dstHeadroom: Float, toneMapping: CGToneMapping, options: CFDictionary?, UnsafeMutablePointer<Unmanaged<CFError>?>?)](/documentation/coregraphics/cgcolorconversioninfo/init(src:srcheadroom:dst:dstheadroom:tonemapping:options:_:))
- [CGColorSpace](/documentation/coregraphics/cgcolorspace)

### Creating Color Spaces

- [init?(calibratedGrayWhitePoint: UnsafePointer<CGFloat>, blackPoint: UnsafePointer<CGFloat>?, gamma: CGFloat)](/documentation/coregraphics/cgcolorspace/init(calibratedgraywhitepoint:blackpoint:gamma:))
- [init?(calibratedRGBWhitePoint: UnsafePointer<CGFloat>, blackPoint: UnsafePointer<CGFloat>?, gamma: UnsafePointer<CGFloat>?, matrix: UnsafePointer<CGFloat>?)](/documentation/coregraphics/cgcolorspace/init(calibratedrgbwhitepoint:blackpoint:gamma:matrix:))
- [init?(iccBasedNComponents: Int, range: UnsafePointer<CGFloat>?, profile: CGDataProvider, alternate: CGColorSpace?)](/documentation/coregraphics/cgcolorspace/init(iccbasedncomponents:range:profile:alternate:))
- [init?(indexedBaseSpace: CGColorSpace, last: Int, colorTable: UnsafePointer<UInt8>)](/documentation/coregraphics/cgcolorspace/init(indexedbasespace:last:colortable:))
- [init?(labWhitePoint: UnsafePointer<CGFloat>, blackPoint: UnsafePointer<CGFloat>?, range: UnsafePointer<CGFloat>?)](/documentation/coregraphics/cgcolorspace/init(labwhitepoint:blackpoint:range:))
- [init?(patternBaseSpace: CGColorSpace?)](/documentation/coregraphics/cgcolorspace/init(patternbasespace:))
- [init?(name: CFString)](/documentation/coregraphics/cgcolorspace/init(name:))
- [init?(platformColorSpaceRef: UnsafeRawPointer)](/documentation/coregraphics/cgcolorspace/init(platformcolorspaceref:))
- [init?(iccData: CFTypeRef)](/documentation/coregraphics/cgcolorspace/init(iccdata:))
- [init?(propertyListPlist: CFPropertyList)](/documentation/coregraphics/cgcolorspace/init(propertylistplist:))
- [func CGColorSpaceCreateDeviceRGB() -> CGColorSpace](/documentation/coregraphics/cgcolorspacecreatedevicergb())
- [func CGColorSpaceCreateDeviceCMYK() -> CGColorSpace](/documentation/coregraphics/cgcolorspacecreatedevicecmyk())
- [func CGColorSpaceCreateDeviceGray() -> CGColorSpace](/documentation/coregraphics/cgcolorspacecreatedevicegray())
- [init?(iccProfileData: CFData)](/documentation/coregraphics/cgcolorspace/init(iccprofiledata:))

### Examining a Color Space

- [var baseColorSpace: CGColorSpace?](/documentation/coregraphics/cgcolorspace/basecolorspace)
- [var numberOfComponents: Int](/documentation/coregraphics/cgcolorspace/numberofcomponents)
- [var model: CGColorSpaceModel](/documentation/coregraphics/cgcolorspace/model)
- [CGColorSpaceModel](/documentation/coregraphics/cgcolorspacemodel)

#### Constants

- [case unknown](/documentation/coregraphics/cgcolorspacemodel/unknown)
- [case monochrome](/documentation/coregraphics/cgcolorspacemodel/monochrome)
- [case rgb](/documentation/coregraphics/cgcolorspacemodel/rgb)
- [case cmyk](/documentation/coregraphics/cgcolorspacemodel/cmyk)
- [case lab](/documentation/coregraphics/cgcolorspacemodel/lab)
- [case deviceN](/documentation/coregraphics/cgcolorspacemodel/devicen)
- [case indexed](/documentation/coregraphics/cgcolorspacemodel/indexed)
- [case pattern](/documentation/coregraphics/cgcolorspacemodel/pattern)
- [case XYZ](/documentation/coregraphics/cgcolorspacemodel/xyz)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgcolorspacemodel/init(rawvalue:))
- [var colorTable: [UInt8]?](/documentation/coregraphics/cgcolorspace/colortable)
- [func copyICCData() -> CFData?](/documentation/coregraphics/cgcolorspace/copyiccdata())
- [func copyPropertyList() -> CFPropertyList?](/documentation/coregraphics/cgcolorspace/copypropertylist())
- [var iccData: CFData?](/documentation/coregraphics/cgcolorspace/iccdata)
- [var name: CFString?](/documentation/coregraphics/cgcolorspace/name)
- [var supportsOutput: Bool](/documentation/coregraphics/cgcolorspace/supportsoutput)
- [var isWideGamutRGB: Bool](/documentation/coregraphics/cgcolorspace/iswidegamutrgb)

### Accessing System-Defined Color Spaces

- [class let displayP3: CFString](/documentation/coregraphics/cgcolorspace/displayp3)
- [class let displayP3_HLG: CFString](/documentation/coregraphics/cgcolorspace/displayp3_hlg)
- [class let displayP3_PQ_EOTF: CFString](/documentation/coregraphics/cgcolorspace/displayp3_pq_eotf)
- [class let extendedLinearDisplayP3: CFString](/documentation/coregraphics/cgcolorspace/extendedlineardisplayp3)
- [class let sRGB: CFString](/documentation/coregraphics/cgcolorspace/srgb)
- [class let linearSRGB: CFString](/documentation/coregraphics/cgcolorspace/linearsrgb)
- [class let extendedSRGB: CFString](/documentation/coregraphics/cgcolorspace/extendedsrgb)
- [class let extendedLinearSRGB: CFString](/documentation/coregraphics/cgcolorspace/extendedlinearsrgb)
- [class let genericGrayGamma2_2: CFString](/documentation/coregraphics/cgcolorspace/genericgraygamma2_2)
- [class let extendedGray: CFString](/documentation/coregraphics/cgcolorspace/extendedgray)
- [class let linearGray: CFString](/documentation/coregraphics/cgcolorspace/lineargray)
- [class let extendedLinearGray: CFString](/documentation/coregraphics/cgcolorspace/extendedlineargray)
- [class let genericCMYK: CFString](/documentation/coregraphics/cgcolorspace/genericcmyk)
- [class let genericRGBLinear: CFString](/documentation/coregraphics/cgcolorspace/genericrgblinear)
- [class let genericXYZ: CFString](/documentation/coregraphics/cgcolorspace/genericxyz)
- [class let genericLab: CFString](/documentation/coregraphics/cgcolorspace/genericlab)
- [class let acescgLinear: CFString](/documentation/coregraphics/cgcolorspace/acescglinear)
- [class let adobeRGB1998: CFString](/documentation/coregraphics/cgcolorspace/adobergb1998)
- [class let dcip3: CFString](/documentation/coregraphics/cgcolorspace/dcip3)
- [class let itur_709: CFString](/documentation/coregraphics/cgcolorspace/itur_709)
- [class let rommrgb: CFString](/documentation/coregraphics/cgcolorspace/rommrgb)
- [class let itur_2020: CFString](/documentation/coregraphics/cgcolorspace/itur_2020)
- [class let itur_2020_HLG: CFString](/documentation/coregraphics/cgcolorspace/itur_2020_hlg)
- [class let itur_2020_PQ_EOTF: CFString](/documentation/coregraphics/cgcolorspace/itur_2020_pq_eotf)
- [class let extendedLinearITUR_2020: CFString](/documentation/coregraphics/cgcolorspace/extendedlinearitur_2020)
- [class let coreMedia709: CFString](/documentation/coregraphics/cgcolorspace/coremedia709)
- [class let displayP3_PQ: CFString](/documentation/coregraphics/cgcolorspace/displayp3_pq)
- [class let extendedDisplayP3: CFString](/documentation/coregraphics/cgcolorspace/extendeddisplayp3)
- [class let extendedITUR_2020: CFString](/documentation/coregraphics/cgcolorspace/extendeditur_2020)
- [class let itur_2020_PQ: CFString](/documentation/coregraphics/cgcolorspace/itur_2020_pq)
- [class let itur_2020_sRGBGamma: CFString](/documentation/coregraphics/cgcolorspace/itur_2020_srgbgamma)
- [class let itur_2100_HLG: CFString](/documentation/coregraphics/cgcolorspace/itur_2100_hlg)
- [class let itur_2100_PQ: CFString](/documentation/coregraphics/cgcolorspace/itur_2100_pq)
- [class let itur_709_HLG: CFString](/documentation/coregraphics/cgcolorspace/itur_709_hlg)
- [class let itur_709_PQ: CFString](/documentation/coregraphics/cgcolorspace/itur_709_pq)
- [class let linearDisplayP3: CFString](/documentation/coregraphics/cgcolorspace/lineardisplayp3)
- [class let linearITUR_2020: CFString](/documentation/coregraphics/cgcolorspace/linearitur_2020)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgcolorspace/typeid)

### Data Types

- [CGColorRenderingIntent](/documentation/coregraphics/cgcolorrenderingintent)

#### Constants

- [case defaultIntent](/documentation/coregraphics/cgcolorrenderingintent/defaultintent)
- [case absoluteColorimetric](/documentation/coregraphics/cgcolorrenderingintent/absolutecolorimetric)
- [case relativeColorimetric](/documentation/coregraphics/cgcolorrenderingintent/relativecolorimetric)
- [case perceptual](/documentation/coregraphics/cgcolorrenderingintent/perceptual)
- [case saturation](/documentation/coregraphics/cgcolorrenderingintent/saturation)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgcolorrenderingintent/init(rawvalue:))

### Instance Methods

- [func isHDR() -> Bool](/documentation/coregraphics/cgcolorspace/ishdr())
- [CGFont](/documentation/coregraphics/cgfont)

### Creating Font Objects

- [init?(CGDataProvider)](/documentation/coregraphics/cgfont/init(_:)-9aour)
- [init?(CFString)](/documentation/coregraphics/cgfont/init(_:)-1p4b)

### Examining Font Metadata

- [var fullName: CFString?](/documentation/coregraphics/cgfont/fullname)

### Examining Font Metrics

- [var ascent: Int32](/documentation/coregraphics/cgfont/ascent)
- [var capHeight: Int32](/documentation/coregraphics/cgfont/capheight)
- [var descent: Int32](/documentation/coregraphics/cgfont/descent)
- [var fontBBox: CGRect](/documentation/coregraphics/cgfont/fontbbox)
- [var italicAngle: CGFloat](/documentation/coregraphics/cgfont/italicangle)
- [var leading: Int32](/documentation/coregraphics/cgfont/leading)
- [var stemV: CGFloat](/documentation/coregraphics/cgfont/stemv)
- [var unitsPerEm: Int32](/documentation/coregraphics/cgfont/unitsperem)
- [var xHeight: Int32](/documentation/coregraphics/cgfont/xheight)

### Working with PostScript Fonts

- [var postScriptName: CFString?](/documentation/coregraphics/cgfont/postscriptname)
- [func canCreatePostScriptSubset(CGFontPostScriptFormat) -> Bool](/documentation/coregraphics/cgfont/cancreatepostscriptsubset(_:))
- [func createPostScriptSubset(subsetName: CFString, format: CGFontPostScriptFormat, glyphs: UnsafePointer<CGGlyph>?, count: Int, encoding: UnsafePointer<CGGlyph>?) -> CFData?](/documentation/coregraphics/cgfont/createpostscriptsubset(subsetname:format:glyphs:count:encoding:))
- [CGFontPostScriptFormat](/documentation/coregraphics/cgfontpostscriptformat)

#### Constants

- [case type1](/documentation/coregraphics/cgfontpostscriptformat/type1)
- [case type3](/documentation/coregraphics/cgfontpostscriptformat/type3)
- [case type42](/documentation/coregraphics/cgfontpostscriptformat/type42)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgfontpostscriptformat/init(rawvalue:))
- [func createPostScriptEncoding(encoding: UnsafePointer<CGGlyph>?) -> CFData?](/documentation/coregraphics/cgfont/createpostscriptencoding(encoding:))

### Working with Font Tables

- [var tableTags: CFArray?](/documentation/coregraphics/cgfont/tabletags)
- [func table(for: UInt32) -> CFData?](/documentation/coregraphics/cgfont/table(for:))
- [Font Table Index Values](/documentation/coregraphics/font-table-index-values)

#### Constants

- [let kCGFontIndexMax: CGFontIndex](/documentation/coregraphics/kcgfontindexmax)
- [let kCGFontIndexInvalid: CGFontIndex](/documentation/coregraphics/kcgfontindexinvalid)
- [let kCGGlyphMax: CGFontIndex](/documentation/coregraphics/kcgglyphmax)
- [Obsolete Font Table Index Values](/documentation/coregraphics/obsolete-font-table-index-values)

#### Constants

- [case min](/documentation/coregraphics/cgglyphdeprecatedenum/min)
- [case max](/documentation/coregraphics/cgglyphdeprecatedenum/max)

### Working with Variations

- [func copy(withVariations: CFDictionary?) -> CGFont?](/documentation/coregraphics/cgfont/copy(withvariations:))
- [var variations: CFDictionary?](/documentation/coregraphics/cgfont/variations)
- [var variationAxes: CFArray?](/documentation/coregraphics/cgfont/variationaxes)
- [Font Variation Axis Keys](/documentation/coregraphics/font-variation-axis-keys)

#### Constants

- [class let variationAxisName: CFString](/documentation/coregraphics/cgfont/variationaxisname)
- [class let variationAxisMinValue: CFString](/documentation/coregraphics/cgfont/variationaxisminvalue)
- [class let variationAxisMaxValue: CFString](/documentation/coregraphics/cgfont/variationaxismaxvalue)
- [class let variationAxisDefaultValue: CFString](/documentation/coregraphics/cgfont/variationaxisdefaultvalue)

### Working with Glyphs

- [var numberOfGlyphs: Int](/documentation/coregraphics/cgfont/numberofglyphs)
- [func name(for: CGGlyph) -> CFString?](/documentation/coregraphics/cgfont/name(for:))
- [func getGlyphWithGlyphName(name: CFString) -> CGGlyph](/documentation/coregraphics/cgfont/getglyphwithglyphname(name:))
- [func getGlyphBBoxes(glyphs: UnsafePointer<CGGlyph>, count: Int, bboxes: UnsafeMutablePointer<CGRect>) -> Bool](/documentation/coregraphics/cgfont/getglyphbboxes(glyphs:count:bboxes:))
- [func getGlyphAdvances(glyphs: UnsafePointer<CGGlyph>, count: Int, advances: UnsafeMutablePointer<Int32>) -> Bool](/documentation/coregraphics/cgfont/getglyphadvances(glyphs:count:advances:))
- [CGGlyph](/documentation/coregraphics/cgglyph)
- [let kCGGlyphMax: CGFontIndex](/documentation/coregraphics/kcgglyphmax)
- [CGFontIndex](/documentation/coregraphics/cgfontindex)
- [let kCGFontIndexMax: CGFontIndex](/documentation/coregraphics/kcgfontindexmax)
- [let kCGFontIndexInvalid: CGFontIndex](/documentation/coregraphics/kcgfontindexinvalid)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgfont/typeid)

## Working with PDF Documents

- [CGPDFDocument](/documentation/coregraphics/cgpdfdocument)

### Creating PDF Documents

- [init?(CGDataProvider)](/documentation/coregraphics/cgpdfdocument/init(_:)-gbq6)
- [init?(CFURL)](/documentation/coregraphics/cgpdfdocument/init(_:)-2gtsd)

### Examining a PDF Document

- [var catalog: CGPDFDictionaryRef?](/documentation/coregraphics/cgpdfdocument/catalog)
- [var fileIdentifier: CGPDFArrayRef?](/documentation/coregraphics/cgpdfdocument/fileidentifier)
- [var info: CGPDFDictionaryRef?](/documentation/coregraphics/cgpdfdocument/info)
- [var numberOfPages: Int](/documentation/coregraphics/cgpdfdocument/numberofpages)
- [func getVersion(majorVersion: UnsafeMutablePointer<Int32>, minorVersion: UnsafeMutablePointer<Int32>)](/documentation/coregraphics/cgpdfdocument/getversion(majorversion:minorversion:))
- [func page(at: Int) -> CGPDFPage?](/documentation/coregraphics/cgpdfdocument/page(at:))

### Working with an Encrypted PDF Document

- [var isEncrypted: Bool](/documentation/coregraphics/cgpdfdocument/isencrypted)
- [var allowsCopying: Bool](/documentation/coregraphics/cgpdfdocument/allowscopying)
- [var allowsPrinting: Bool](/documentation/coregraphics/cgpdfdocument/allowsprinting)
- [var isUnlocked: Bool](/documentation/coregraphics/cgpdfdocument/isunlocked)
- [func unlockWithPassword(UnsafePointer<CChar>) -> Bool](/documentation/coregraphics/cgpdfdocument/unlockwithpassword(_:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgpdfdocument/typeid)

### Abstract Types for PDF Document Content

- [CGPDFPage](/documentation/coregraphics/cgpdfpage)

#### Getting Page Information

- [func getBoxRect(CGPDFBox) -> CGRect](/documentation/coregraphics/cgpdfpage/getboxrect(_:))
- [var dictionary: CGPDFDictionaryRef?](/documentation/coregraphics/cgpdfpage/dictionary)
- [var document: CGPDFDocument?](/documentation/coregraphics/cgpdfpage/document)
- [var pageNumber: Int](/documentation/coregraphics/cgpdfpage/pagenumber)
- [var rotationAngle: Int32](/documentation/coregraphics/cgpdfpage/rotationangle)
- [func getDrawingTransform(CGPDFBox, rect: CGRect, rotate: Int32, preserveAspectRatio: Bool) -> CGAffineTransform](/documentation/coregraphics/cgpdfpage/getdrawingtransform(_:rect:rotate:preserveaspectratio:))

#### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgpdfpage/typeid)

#### Constants

- [CGPDFBox](/documentation/coregraphics/cgpdfbox)

##### Constants

- [case mediaBox](/documentation/coregraphics/cgpdfbox/mediabox)
- [case cropBox](/documentation/coregraphics/cgpdfbox/cropbox)
- [case bleedBox](/documentation/coregraphics/cgpdfbox/bleedbox)
- [case trimBox](/documentation/coregraphics/cgpdfbox/trimbox)
- [case artBox](/documentation/coregraphics/cgpdfbox/artbox)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpdfbox/init(rawvalue:))
- [CGPDFArray](/documentation/coregraphics/cgpdfarray)

#### Getting Data from a PDF Array

- [func CGPDFArrayGetArray(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFArrayRef?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetarray(_:_:_:))
- [func CGPDFArrayGetBoolean(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFBoolean>?) -> Bool](/documentation/coregraphics/cgpdfarraygetboolean(_:_:_:))
- [func CGPDFArrayGetCount(CGPDFArrayRef) -> Int](/documentation/coregraphics/cgpdfarraygetcount(_:))
- [func CGPDFArrayGetDictionary(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFDictionaryRef?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetdictionary(_:_:_:))
- [func CGPDFArrayGetInteger(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFInteger>?) -> Bool](/documentation/coregraphics/cgpdfarraygetinteger(_:_:_:))
- [func CGPDFArrayGetName(CGPDFArrayRef, Int, UnsafeMutablePointer<UnsafePointer<CChar>?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetname(_:_:_:))
- [func CGPDFArrayGetNull(CGPDFArrayRef, Int) -> Bool](/documentation/coregraphics/cgpdfarraygetnull(_:_:))
- [func CGPDFArrayGetNumber(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFReal>?) -> Bool](/documentation/coregraphics/cgpdfarraygetnumber(_:_:_:))
- [func CGPDFArrayGetObject(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFObjectRef?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetobject(_:_:_:))
- [func CGPDFArrayGetStream(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFStreamRef?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetstream(_:_:_:))
- [func CGPDFArrayGetString(CGPDFArrayRef, Int, UnsafeMutablePointer<CGPDFStringRef?>?) -> Bool](/documentation/coregraphics/cgpdfarraygetstring(_:_:_:))

#### Data Types

- [CGPDFArrayRef](/documentation/coregraphics/cgpdfarrayref)

##### Initializers

- [init(OpaquePointer)](/documentation/coregraphics/cgpdfarrayref/init(_:))
- [init(rawValue: OpaquePointer)](/documentation/coregraphics/cgpdfarrayref/init(rawvalue:))
- [CGPDFObject](/documentation/coregraphics/cgpdfobject)

#### Getting Object Types and Values

- [func CGPDFObjectGetType(CGPDFObjectRef) -> CGPDFObjectType](/documentation/coregraphics/cgpdfobjectgettype(_:))
- [func CGPDFObjectGetValue(CGPDFObjectRef, CGPDFObjectType, UnsafeMutableRawPointer?) -> Bool](/documentation/coregraphics/cgpdfobjectgetvalue(_:_:_:))

#### Data Types

- [CGPDFObjectRef](/documentation/coregraphics/cgpdfobjectref)

##### Initializers

- [init(OpaquePointer)](/documentation/coregraphics/cgpdfobjectref/init(_:))
- [init(rawValue: OpaquePointer)](/documentation/coregraphics/cgpdfobjectref/init(rawvalue:))
- [CGPDFBoolean](/documentation/coregraphics/cgpdfboolean)
- [CGPDFInteger](/documentation/coregraphics/cgpdfinteger)
- [CGPDFReal](/documentation/coregraphics/cgpdfreal)

#### Constants

- [CGPDFObjectType](/documentation/coregraphics/cgpdfobjecttype)

##### Constants

- [case null](/documentation/coregraphics/cgpdfobjecttype/null)
- [case boolean](/documentation/coregraphics/cgpdfobjecttype/boolean)
- [case integer](/documentation/coregraphics/cgpdfobjecttype/integer)
- [case real](/documentation/coregraphics/cgpdfobjecttype/real)
- [case name](/documentation/coregraphics/cgpdfobjecttype/name)
- [case string](/documentation/coregraphics/cgpdfobjecttype/string)
- [case array](/documentation/coregraphics/cgpdfobjecttype/array)
- [case dictionary](/documentation/coregraphics/cgpdfobjecttype/dictionary)
- [case stream](/documentation/coregraphics/cgpdfobjecttype/stream)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpdfobjecttype/init(rawvalue:))
- [CGPDFStream](/documentation/coregraphics/cgpdfstream)

#### Getting Data from a PDF Stream

- [func CGPDFStreamCopyData(CGPDFStreamRef, UnsafeMutablePointer<CGPDFDataFormat>) -> CFData?](/documentation/coregraphics/cgpdfstreamcopydata(_:_:))
- [func CGPDFStreamGetDictionary(CGPDFStreamRef) -> CGPDFDictionaryRef?](/documentation/coregraphics/cgpdfstreamgetdictionary(_:))

#### Data Types

- [CGPDFStreamRef](/documentation/coregraphics/cgpdfstreamref)

##### Initializers

- [init(OpaquePointer)](/documentation/coregraphics/cgpdfstreamref/init(_:))
- [init(rawValue: OpaquePointer)](/documentation/coregraphics/cgpdfstreamref/init(rawvalue:))

#### Constants

- [CGPDFDataFormat](/documentation/coregraphics/cgpdfdataformat)

##### Constants

- [case raw](/documentation/coregraphics/cgpdfdataformat/raw)
- [case jpegEncoded](/documentation/coregraphics/cgpdfdataformat/jpegencoded)
- [case JPEG2000](/documentation/coregraphics/cgpdfdataformat/jpeg2000)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpdfdataformat/init(rawvalue:))
- [CGPDFString](/documentation/coregraphics/cgpdfstring)

#### Converting PDF Strings

- [func CGPDFStringCopyTextString(CGPDFStringRef) -> CFString?](/documentation/coregraphics/cgpdfstringcopytextstring(_:))
- [func CGPDFStringCopyDate(CGPDFStringRef) -> CFDate?](/documentation/coregraphics/cgpdfstringcopydate(_:))

#### Getting PDF String Data

- [func CGPDFStringGetBytePtr(CGPDFStringRef) -> UnsafePointer<UInt8>?](/documentation/coregraphics/cgpdfstringgetbyteptr(_:))
- [func CGPDFStringGetLength(CGPDFStringRef) -> Int](/documentation/coregraphics/cgpdfstringgetlength(_:))

#### Data Types

- [CGPDFStringRef](/documentation/coregraphics/cgpdfstringref)

##### Initializers

- [init(OpaquePointer)](/documentation/coregraphics/cgpdfstringref/init(_:))
- [init(rawValue: OpaquePointer)](/documentation/coregraphics/cgpdfstringref/init(rawvalue:))
- [CGPDFScanner](/documentation/coregraphics/cgpdfscanner)

#### Creating a PDF Scanner Object

- [func CGPDFScannerCreate(CGPDFContentStreamRef, CGPDFOperatorTableRef?, UnsafeMutableRawPointer?) -> CGPDFScannerRef](/documentation/coregraphics/cgpdfscannercreate(_:_:_:))

#### Retaining and Releasing PDF Scanner Objects

- [func CGPDFScannerRetain(CGPDFScannerRef) -> CGPDFScannerRef](/documentation/coregraphics/cgpdfscannerretain(_:))
- [func CGPDFScannerRelease(CGPDFScannerRef)](/documentation/coregraphics/cgpdfscannerrelease(_:))

#### Parsing Content

- [func CGPDFScannerScan(CGPDFScannerRef) -> Bool](/documentation/coregraphics/cgpdfscannerscan(_:))
- [func CGPDFScannerGetContentStream(CGPDFScannerRef) -> CGPDFContentStreamRef](/documentation/coregraphics/cgpdfscannergetcontentstream(_:))

#### Getting PDF Objects from the Scanner Stack

- [func CGPDFScannerPopObject(CGPDFScannerRef, UnsafeMutablePointer<CGPDFObjectRef?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopobject(_:_:))
- [func CGPDFScannerPopBoolean(CGPDFScannerRef, UnsafeMutablePointer<CGPDFBoolean>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopboolean(_:_:))
- [func CGPDFScannerPopInteger(CGPDFScannerRef, UnsafeMutablePointer<CGPDFInteger>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopinteger(_:_:))
- [func CGPDFScannerPopNumber(CGPDFScannerRef, UnsafeMutablePointer<CGPDFReal>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopnumber(_:_:))
- [func CGPDFScannerPopName(CGPDFScannerRef, UnsafeMutablePointer<UnsafePointer<CChar>?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopname(_:_:))
- [func CGPDFScannerPopString(CGPDFScannerRef, UnsafeMutablePointer<CGPDFStringRef?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopstring(_:_:))
- [func CGPDFScannerPopArray(CGPDFScannerRef, UnsafeMutablePointer<CGPDFArrayRef?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpoparray(_:_:))
- [func CGPDFScannerPopDictionary(CGPDFScannerRef, UnsafeMutablePointer<CGPDFDictionaryRef?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopdictionary(_:_:))
- [func CGPDFScannerPopStream(CGPDFScannerRef, UnsafeMutablePointer<CGPDFStreamRef?>?) -> Bool](/documentation/coregraphics/cgpdfscannerpopstream(_:_:))

#### Data Types

- [CGPDFScannerRef](/documentation/coregraphics/cgpdfscannerref)
- [CGPDFDictionary](/documentation/coregraphics/cgpdfdictionary)

#### Applying a Function to All Entries

- [func CGPDFDictionaryApplyFunction(CGPDFDictionaryRef, CGPDFDictionaryApplierFunction, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgpdfdictionaryapplyfunction(_:_:_:))

#### Getting Data from a Dictionary

- [func CGPDFDictionaryGetArray(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFArrayRef?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetarray(_:_:_:))
- [func CGPDFDictionaryGetBoolean(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFBoolean>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetboolean(_:_:_:))
- [func CGPDFDictionaryGetCount(CGPDFDictionaryRef) -> Int](/documentation/coregraphics/cgpdfdictionarygetcount(_:))
- [func CGPDFDictionaryGetDictionary(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFDictionaryRef?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetdictionary(_:_:_:))
- [func CGPDFDictionaryGetInteger(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFInteger>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetinteger(_:_:_:))
- [func CGPDFDictionaryGetName(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<UnsafePointer<CChar>?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetname(_:_:_:))
- [func CGPDFDictionaryGetNumber(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFReal>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetnumber(_:_:_:))
- [func CGPDFDictionaryGetObject(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFObjectRef?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetobject(_:_:_:))
- [func CGPDFDictionaryGetStream(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFStreamRef?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetstream(_:_:_:))
- [func CGPDFDictionaryGetString(CGPDFDictionaryRef, UnsafePointer<CChar>, UnsafeMutablePointer<CGPDFStringRef?>?) -> Bool](/documentation/coregraphics/cgpdfdictionarygetstring(_:_:_:))

#### Callbacks

- [CGPDFDictionaryApplierFunction](/documentation/coregraphics/cgpdfdictionaryapplierfunction)

#### Data Types

- [CGPDFDictionaryRef](/documentation/coregraphics/cgpdfdictionaryref)

##### Initializers

- [init(OpaquePointer)](/documentation/coregraphics/cgpdfdictionaryref/init(_:))
- [init(rawValue: OpaquePointer)](/documentation/coregraphics/cgpdfdictionaryref/init(rawvalue:))
- [CGPDFContentStream](/documentation/coregraphics/cgpdfcontentstream)

#### Creating a PDF Content Stream Object

- [func CGPDFContentStreamCreateWithPage(CGPDFPage) -> CGPDFContentStreamRef](/documentation/coregraphics/cgpdfcontentstreamcreatewithpage(_:))
- [func CGPDFContentStreamCreateWithStream(CGPDFStreamRef, CGPDFDictionaryRef, CGPDFContentStreamRef) -> CGPDFContentStreamRef](/documentation/coregraphics/cgpdfcontentstreamcreatewithstream(_:_:_:))

#### Getting Data from a PDF Content Stream Object

- [func CGPDFContentStreamGetStreams(CGPDFContentStreamRef) -> CFArray?](/documentation/coregraphics/cgpdfcontentstreamgetstreams(_:))
- [func CGPDFContentStreamGetResource(CGPDFContentStreamRef, UnsafePointer<CChar>, UnsafePointer<CChar>) -> CGPDFObjectRef?](/documentation/coregraphics/cgpdfcontentstreamgetresource(_:_:_:))

#### Retaining and Releasing a PDF Content Stream Object

- [func CGPDFContentStreamRetain(CGPDFContentStreamRef) -> CGPDFContentStreamRef](/documentation/coregraphics/cgpdfcontentstreamretain(_:))
- [func CGPDFContentStreamRelease(CGPDFContentStreamRef)](/documentation/coregraphics/cgpdfcontentstreamrelease(_:))

#### Data Types

- [CGPDFContentStreamRef](/documentation/coregraphics/cgpdfcontentstreamref)
- [CGPDFOperatorTable](/documentation/coregraphics/cgpdfoperatortable)

#### Creating a PDF Operator Table

- [func CGPDFOperatorTableCreate() -> CGPDFOperatorTableRef?](/documentation/coregraphics/cgpdfoperatortablecreate())

#### Setting Callback Functions

- [func CGPDFOperatorTableSetCallback(CGPDFOperatorTableRef, UnsafePointer<CChar>, CGPDFOperatorCallback)](/documentation/coregraphics/cgpdfoperatortablesetcallback(_:_:_:))

#### Retaining and Releasing a PDF Operator Table

- [func CGPDFOperatorTableRetain(CGPDFOperatorTableRef) -> CGPDFOperatorTableRef](/documentation/coregraphics/cgpdfoperatortableretain(_:))
- [func CGPDFOperatorTableRelease(CGPDFOperatorTableRef)](/documentation/coregraphics/cgpdfoperatortablerelease(_:))

#### Callbacks

- [CGPDFOperatorCallback](/documentation/coregraphics/cgpdfoperatorcallback)

#### Data Types

- [CGPDFOperatorTableRef](/documentation/coregraphics/cgpdfoperatortableref)

### Instance Properties

- [var accessPermissions: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfdocument/accesspermissions)
- [var outline: CFDictionary?](/documentation/coregraphics/cgpdfdocument/outline)

## Utility and Support Classes

- [CGDataConsumer](/documentation/coregraphics/cgdataconsumer)

### Creating Data Consumers

- [init?(info: UnsafeMutableRawPointer?, cbks: UnsafePointer<CGDataConsumerCallbacks>)](/documentation/coregraphics/cgdataconsumer/init(info:cbks:))
- [init?(url: CFURL)](/documentation/coregraphics/cgdataconsumer/init(url:))
- [init?(data: CFMutableData)](/documentation/coregraphics/cgdataconsumer/init(data:))
- [CGDataConsumerCallbacks](/documentation/coregraphics/cgdataconsumercallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgdataconsumercallbacks/init())
- [init(putBytes: CGDataConsumerPutBytesCallback?, releaseConsumer: CGDataConsumerReleaseInfoCallback?)](/documentation/coregraphics/cgdataconsumercallbacks/init(putbytes:releaseconsumer:))

#### Instance Properties

- [var putBytes: CGDataConsumerPutBytesCallback?](/documentation/coregraphics/cgdataconsumercallbacks/putbytes)
- [var releaseConsumer: CGDataConsumerReleaseInfoCallback?](/documentation/coregraphics/cgdataconsumercallbacks/releaseconsumer)
- [CGDataConsumerPutBytesCallback](/documentation/coregraphics/cgdataconsumerputbytescallback)
- [CGDataConsumerReleaseInfoCallback](/documentation/coregraphics/cgdataconsumerreleaseinfocallback)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgdataconsumer/typeid)
- [CGDataProvider](/documentation/coregraphics/cgdataprovider)

### Creating Sequential-Access Data Providers

- [init?(sequentialInfo: UnsafeMutableRawPointer?, callbacks: UnsafePointer<CGDataProviderSequentialCallbacks>)](/documentation/coregraphics/cgdataprovider/init(sequentialinfo:callbacks:))
- [CGDataProviderSequentialCallbacks](/documentation/coregraphics/cgdataprovidersequentialcallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgdataprovidersequentialcallbacks/init())
- [init(version: UInt32, getBytes: CGDataProviderGetBytesCallback?, skipForward: CGDataProviderSkipForwardCallback?, rewind: CGDataProviderRewindCallback?, releaseInfo: CGDataProviderReleaseInfoCallback?)](/documentation/coregraphics/cgdataprovidersequentialcallbacks/init(version:getbytes:skipforward:rewind:releaseinfo:))

#### Instance Properties

- [var getBytes: CGDataProviderGetBytesCallback?](/documentation/coregraphics/cgdataprovidersequentialcallbacks/getbytes)
- [var releaseInfo: CGDataProviderReleaseInfoCallback?](/documentation/coregraphics/cgdataprovidersequentialcallbacks/releaseinfo)
- [var rewind: CGDataProviderRewindCallback?](/documentation/coregraphics/cgdataprovidersequentialcallbacks/rewind)
- [var skipForward: CGDataProviderSkipForwardCallback?](/documentation/coregraphics/cgdataprovidersequentialcallbacks/skipforward)
- [var version: UInt32](/documentation/coregraphics/cgdataprovidersequentialcallbacks/version)
- [CGDataProviderRewindCallback](/documentation/coregraphics/cgdataproviderrewindcallback)
- [CGDataProviderGetBytesCallback](/documentation/coregraphics/cgdataprovidergetbytescallback)
- [CGDataProviderSkipForwardCallback](/documentation/coregraphics/cgdataproviderskipforwardcallback)
- [CGDataProviderReleaseInfoCallback](/documentation/coregraphics/cgdataproviderreleaseinfocallback)

### Creating Direct-Access Data Providers

- [init?(directInfo: UnsafeMutableRawPointer?, size: off_t, callbacks: UnsafePointer<CGDataProviderDirectCallbacks>)](/documentation/coregraphics/cgdataprovider/init(directinfo:size:callbacks:))
- [init?(data: CFData)](/documentation/coregraphics/cgdataprovider/init(data:))
- [init?(url: CFURL)](/documentation/coregraphics/cgdataprovider/init(url:))
- [init?(dataInfo: UnsafeMutableRawPointer?, data: UnsafeRawPointer, size: Int, releaseData: CGDataProviderReleaseDataCallback)](/documentation/coregraphics/cgdataprovider/init(datainfo:data:size:releasedata:))
- [init?(filename: UnsafePointer<CChar>)](/documentation/coregraphics/cgdataprovider/init(filename:))
- [CGDataProviderDirectCallbacks](/documentation/coregraphics/cgdataproviderdirectcallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgdataproviderdirectcallbacks/init())
- [init(version: UInt32, getBytePointer: CGDataProviderGetBytePointerCallback?, releaseBytePointer: CGDataProviderReleaseBytePointerCallback?, getBytesAtPosition: CGDataProviderGetBytesAtPositionCallback?, releaseInfo: CGDataProviderReleaseInfoCallback?)](/documentation/coregraphics/cgdataproviderdirectcallbacks/init(version:getbytepointer:releasebytepointer:getbytesatposition:releaseinfo:))

#### Instance Properties

- [var getBytePointer: CGDataProviderGetBytePointerCallback?](/documentation/coregraphics/cgdataproviderdirectcallbacks/getbytepointer)
- [var getBytesAtPosition: CGDataProviderGetBytesAtPositionCallback?](/documentation/coregraphics/cgdataproviderdirectcallbacks/getbytesatposition)
- [var releaseBytePointer: CGDataProviderReleaseBytePointerCallback?](/documentation/coregraphics/cgdataproviderdirectcallbacks/releasebytepointer)
- [var releaseInfo: CGDataProviderReleaseInfoCallback?](/documentation/coregraphics/cgdataproviderdirectcallbacks/releaseinfo)
- [var version: UInt32](/documentation/coregraphics/cgdataproviderdirectcallbacks/version)
- [CGDataProviderGetBytePointerCallback](/documentation/coregraphics/cgdataprovidergetbytepointercallback)
- [CGDataProviderGetBytesAtPositionCallback](/documentation/coregraphics/cgdataprovidergetbytesatpositioncallback)
- [CGDataProviderReleaseBytePointerCallback](/documentation/coregraphics/cgdataproviderreleasebytepointercallback)
- [CGDataProviderReleaseInfoCallback](/documentation/coregraphics/cgdataproviderreleaseinfocallback)
- [CGDataProviderReleaseDataCallback](/documentation/coregraphics/cgdataproviderreleasedatacallback)

### Getting Data from a Data Provider

- [var data: CFData?](/documentation/coregraphics/cgdataprovider/data)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgdataprovider/typeid)

### Instance Properties

- [var info: UnsafeMutableRawPointer?](/documentation/coregraphics/cgdataprovider/info)
- [CGShading](/documentation/coregraphics/cgshading)

### Creating Shading Objects

- [init?(axialSpace: CGColorSpace, start: CGPoint, end: CGPoint, function: CGFunction, extendStart: Bool, extendEnd: Bool)](/documentation/coregraphics/cgshading/init(axialspace:start:end:function:extendstart:extendend:))
- [init?(radialSpace: CGColorSpace, start: CGPoint, startRadius: CGFloat, end: CGPoint, endRadius: CGFloat, function: CGFunction, extendStart: Bool, extendEnd: Bool)](/documentation/coregraphics/cgshading/init(radialspace:start:startradius:end:endradius:function:extendstart:extendend:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgshading/typeid)

### Initializers

- [init?(axialHeadroom: Float, space: CGColorSpace, start: CGPoint, end: CGPoint, function: CGFunction, extendStart: Bool, extendEnd: Bool)](/documentation/coregraphics/cgshading/init(axialheadroom:space:start:end:function:extendstart:extendend:))
- [init?(radialHeadroom: Float, space: CGColorSpace, start: CGPoint, startRadius: CGFloat, end: CGPoint, endRadius: CGFloat, function: CGFunction, extendStart: Bool, extendEnd: Bool)](/documentation/coregraphics/cgshading/init(radialheadroom:space:start:startradius:end:endradius:function:extendstart:extendend:))

### Instance Properties

- [var contentHeadroom: Float](/documentation/coregraphics/cgshading/contentheadroom)
- [CGGradient](/documentation/coregraphics/cggradient)

### Creating Gradient Instances

- [init?(colorSpace: CGColorSpace, colorComponents: UnsafePointer<CGFloat>, locations: UnsafePointer<CGFloat>?, count: Int)](/documentation/coregraphics/cggradient/init(colorspace:colorcomponents:locations:count:))
- [init?(colorsSpace: CGColorSpace?, colors: CFArray, locations: UnsafePointer<CGFloat>?)](/documentation/coregraphics/cggradient/init(colorsspace:colors:locations:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cggradient/typeid)

### Initializers

- [init?(headroom: Float, colorSpace: CGColorSpace, colorComponents: UnsafePointer<CGFloat>, locations: UnsafePointer<CGFloat>?, count: Int)](/documentation/coregraphics/cggradient/init(headroom:colorspace:colorcomponents:locations:count:))

### Instance Properties

- [var contentHeadroom: Float](/documentation/coregraphics/cggradient/contentheadroom)
- [CGFunction](/documentation/coregraphics/cgfunction)

### Creating Function Objects

- [init?(info: UnsafeMutableRawPointer?, domainDimension: Int, domain: UnsafePointer<CGFloat>?, rangeDimension: Int, range: UnsafePointer<CGFloat>?, callbacks: UnsafePointer<CGFunctionCallbacks>)](/documentation/coregraphics/cgfunction/init(info:domaindimension:domain:rangedimension:range:callbacks:))

### Callbacks

- [CGFunctionCallbacks](/documentation/coregraphics/cgfunctioncallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgfunctioncallbacks/init())
- [init(version: UInt32, evaluate: CGFunctionEvaluateCallback?, releaseInfo: CGFunctionReleaseInfoCallback?)](/documentation/coregraphics/cgfunctioncallbacks/init(version:evaluate:releaseinfo:))

#### Instance Properties

- [var evaluate: CGFunctionEvaluateCallback?](/documentation/coregraphics/cgfunctioncallbacks/evaluate)
- [var releaseInfo: CGFunctionReleaseInfoCallback?](/documentation/coregraphics/cgfunctioncallbacks/releaseinfo)
- [var version: UInt32](/documentation/coregraphics/cgfunctioncallbacks/version)
- [CGFunctionEvaluateCallback](/documentation/coregraphics/cgfunctionevaluatecallback)
- [CGFunctionReleaseInfoCallback](/documentation/coregraphics/cgfunctionreleaseinfocallback)

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgfunction/typeid)
- [CGPattern](/documentation/coregraphics/cgpattern)

### Creating a Pattern

- [init?(info: UnsafeMutableRawPointer?, bounds: CGRect, matrix: CGAffineTransform, xStep: CGFloat, yStep: CGFloat, tiling: CGPatternTiling, isColored: Bool, callbacks: UnsafePointer<CGPatternCallbacks>)](/documentation/coregraphics/cgpattern/init(info:bounds:matrix:xstep:ystep:tiling:iscolored:callbacks:))

### Callbacks

- [CGPatternCallbacks](/documentation/coregraphics/cgpatterncallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgpatterncallbacks/init())
- [init(version: UInt32, drawPattern: CGPatternDrawPatternCallback?, releaseInfo: CGPatternReleaseInfoCallback?)](/documentation/coregraphics/cgpatterncallbacks/init(version:drawpattern:releaseinfo:))

#### Instance Properties

- [var drawPattern: CGPatternDrawPatternCallback?](/documentation/coregraphics/cgpatterncallbacks/drawpattern)
- [var releaseInfo: CGPatternReleaseInfoCallback?](/documentation/coregraphics/cgpatterncallbacks/releaseinfo)
- [var version: UInt32](/documentation/coregraphics/cgpatterncallbacks/version)
- [CGPatternDrawPatternCallback](/documentation/coregraphics/cgpatterndrawpatterncallback)
- [CGPatternReleaseInfoCallback](/documentation/coregraphics/cgpatternreleaseinfocallback)

### Constants

- [CGPatternTiling](/documentation/coregraphics/cgpatterntiling)

#### Constants

- [case noDistortion](/documentation/coregraphics/cgpatterntiling/nodistortion)
- [case constantSpacingMinimalDistortion](/documentation/coregraphics/cgpatterntiling/constantspacingminimaldistortion)
- [case constantSpacing](/documentation/coregraphics/cgpatterntiling/constantspacing)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpatterntiling/init(rawvalue:))

### Working with Core Foundation Types

- [class var typeID: CFTypeID](/documentation/coregraphics/cgpattern/typeid)

## Services

- [Quartz Display Services](/documentation/coregraphics/quartz-display-services)

### Finding Displays

- [func CGMainDisplayID() -> CGDirectDisplayID](/documentation/coregraphics/cgmaindisplayid())
- [func CGGetOnlineDisplayList(UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetonlinedisplaylist(_:_:_:))
- [func CGGetActiveDisplayList(UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetactivedisplaylist(_:_:_:))
- [func CGGetDisplaysWithOpenGLDisplayMask(CGOpenGLDisplayMask, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithopengldisplaymask(_:_:_:_:))
- [func CGGetDisplaysWithPoint(CGPoint, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithpoint(_:_:_:_:))
- [func CGGetDisplaysWithRect(CGRect, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithrect(_:_:_:_:))
- [func CGOpenGLDisplayMaskToDisplayID(CGOpenGLDisplayMask) -> CGDirectDisplayID](/documentation/coregraphics/cgopengldisplaymasktodisplayid(_:))
- [func CGDisplayIDToOpenGLDisplayMask(CGDirectDisplayID) -> CGOpenGLDisplayMask](/documentation/coregraphics/cgdisplayidtoopengldisplaymask(_:))

### Capturing and Releasing Displays

- [func CGDisplayCapture(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplaycapture(_:))
- [func CGDisplayCaptureWithOptions(CGDirectDisplayID, CGCaptureOptions) -> CGError](/documentation/coregraphics/cgdisplaycapturewithoptions(_:_:))
- [func CGDisplayRelease(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayrelease(_:))
- [func CGDisplayIsCaptured(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayiscaptured(_:))
- [func CGCaptureAllDisplays() -> CGError](/documentation/coregraphics/cgcapturealldisplays())
- [func CGCaptureAllDisplaysWithOptions(CGCaptureOptions) -> CGError](/documentation/coregraphics/cgcapturealldisplayswithoptions(_:))
- [func CGReleaseAllDisplays() -> CGError](/documentation/coregraphics/cgreleasealldisplays())
- [func CGShieldingWindowID(CGDirectDisplayID) -> CGWindowID](/documentation/coregraphics/cgshieldingwindowid(_:))
- [func CGShieldingWindowLevel() -> CGWindowLevel](/documentation/coregraphics/cgshieldingwindowlevel())
- [func CGDisplayGetDrawingContext(CGDirectDisplayID) -> CGContext?](/documentation/coregraphics/cgdisplaygetdrawingcontext(_:))

### Creating Images from the Display

- [func CGDisplayCreateImage(CGDirectDisplayID) -> CGImage?](/documentation/coregraphics/cgdisplaycreateimage(_:))
- [func CGDisplayCreateImage(CGDirectDisplayID, rect: CGRect) -> CGImage?](/documentation/coregraphics/cgdisplaycreateimage(_:rect:))

### Configuring Displays

- [func CGBeginDisplayConfiguration(UnsafeMutablePointer<CGDisplayConfigRef?>?) -> CGError](/documentation/coregraphics/cgbegindisplayconfiguration(_:))
- [func CGCancelDisplayConfiguration(CGDisplayConfigRef?) -> CGError](/documentation/coregraphics/cgcanceldisplayconfiguration(_:))
- [func CGCompleteDisplayConfiguration(CGDisplayConfigRef?, CGConfigureOption) -> CGError](/documentation/coregraphics/cgcompletedisplayconfiguration(_:_:))
- [func CGConfigureDisplayMirrorOfDisplay(CGDisplayConfigRef?, CGDirectDisplayID, CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgconfiguredisplaymirrorofdisplay(_:_:_:))
- [func CGConfigureDisplayMode(CGDisplayConfigRef?, CGDirectDisplayID, CFDictionary?) -> CGError](/documentation/coregraphics/cgconfiguredisplaymode(_:_:_:))
- [func CGConfigureDisplayOrigin(CGDisplayConfigRef?, CGDirectDisplayID, Int32, Int32) -> CGError](/documentation/coregraphics/cgconfiguredisplayorigin(_:_:_:_:))
- [func CGRestorePermanentDisplayConfiguration()](/documentation/coregraphics/cgrestorepermanentdisplayconfiguration())
- [func CGConfigureDisplayStereoOperation(CGDisplayConfigRef?, CGDirectDisplayID, boolean_t, boolean_t) -> CGError](/documentation/coregraphics/cgconfiguredisplaystereooperation(_:_:_:_:))
- [func CGDisplaySetStereoOperation(CGDirectDisplayID, boolean_t, boolean_t, CGConfigureOption) -> CGError](/documentation/coregraphics/cgdisplaysetstereooperation(_:_:_:_:))
- [func CGConfigureDisplayWithDisplayMode(CGDisplayConfigRef?, CGDirectDisplayID, CGDisplayMode?, CFDictionary?) -> CGError](/documentation/coregraphics/cgconfiguredisplaywithdisplaymode(_:_:_:_:))

### Getting the Display Configuration

- [func CGDisplayCopyColorSpace(CGDirectDisplayID) -> CGColorSpace](/documentation/coregraphics/cgdisplaycopycolorspace(_:))
- [func CGDisplayIOServicePort(CGDirectDisplayID) -> io_service_t](/documentation/coregraphics/cgdisplayioserviceport(_:))
- [func CGDisplayIsActive(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisactive(_:))
- [func CGDisplayIsAlwaysInMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisalwaysinmirrorset(_:))
- [func CGDisplayIsAsleep(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisasleep(_:))
- [func CGDisplayIsBuiltin(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisbuiltin(_:))
- [func CGDisplayIsInHWMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisinhwmirrorset(_:))
- [func CGDisplayIsInMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisinmirrorset(_:))
- [func CGDisplayIsMain(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayismain(_:))
- [func CGDisplayIsOnline(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisonline(_:))
- [func CGDisplayIsStereo(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisstereo(_:))
- [func CGDisplayMirrorsDisplay(CGDirectDisplayID) -> CGDirectDisplayID](/documentation/coregraphics/cgdisplaymirrorsdisplay(_:))
- [func CGDisplayModelNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplaymodelnumber(_:))
- [func CGDisplayPrimaryDisplay(CGDirectDisplayID) -> CGDirectDisplayID](/documentation/coregraphics/cgdisplayprimarydisplay(_:))
- [func CGDisplayRotation(CGDirectDisplayID) -> Double](/documentation/coregraphics/cgdisplayrotation(_:))
- [func CGDisplayScreenSize(CGDirectDisplayID) -> CGSize](/documentation/coregraphics/cgdisplayscreensize(_:))
- [func CGDisplaySerialNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayserialnumber(_:))
- [func CGDisplayUnitNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayunitnumber(_:))
- [func CGDisplayUsesOpenGLAcceleration(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayusesopenglacceleration(_:))
- [func CGDisplayVendorNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayvendornumber(_:))

### Registering for Notification of Display Configuration Changes

- [func CGDisplayRegisterReconfigurationCallback(CGDisplayReconfigurationCallBack?, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgdisplayregisterreconfigurationcallback(_:_:))
- [func CGDisplayRemoveReconfigurationCallback(CGDisplayReconfigurationCallBack?, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgdisplayremovereconfigurationcallback(_:_:))

### Retrieving Display Parameters

- [func CGDisplayBounds(CGDirectDisplayID) -> CGRect](/documentation/coregraphics/cgdisplaybounds(_:))
- [func CGDisplayPixelsHigh(CGDirectDisplayID) -> Int](/documentation/coregraphics/cgdisplaypixelshigh(_:))
- [func CGDisplayPixelsWide(CGDirectDisplayID) -> Int](/documentation/coregraphics/cgdisplaypixelswide(_:))

### Creating and Managing Display Modes

- [func CGDisplayAvailableModes(CGDirectDisplayID) -> CFArray?](/documentation/coregraphics/cgdisplayavailablemodes(_:))
- [func CGDisplayBestModeForParameters(CGDirectDisplayID, Int, Int, Int, UnsafeMutablePointer<boolean_t>?) -> CFDictionary?](/documentation/coregraphics/cgdisplaybestmodeforparameters(_:_:_:_:_:))
- [func CGDisplayBestModeForParametersAndRefreshRate(CGDirectDisplayID, Int, Int, Int, CGRefreshRate, UnsafeMutablePointer<boolean_t>?) -> CFDictionary?](/documentation/coregraphics/cgdisplaybestmodeforparametersandrefreshrate(_:_:_:_:_:_:))
- [func CGDisplayCurrentMode(CGDirectDisplayID) -> CFDictionary?](/documentation/coregraphics/cgdisplaycurrentmode(_:))
- [func CGDisplaySwitchToMode(CGDirectDisplayID, CFDictionary?) -> CGError](/documentation/coregraphics/cgdisplayswitchtomode(_:_:))
- [func CGDisplayCopyDisplayMode(CGDirectDisplayID) -> CGDisplayMode?](/documentation/coregraphics/cgdisplaycopydisplaymode(_:))
- [func CGDisplayCopyAllDisplayModes(CGDirectDisplayID, CFDictionary?) -> CFArray?](/documentation/coregraphics/cgdisplaycopyalldisplaymodes(_:_:))
- [func CGDisplaySetDisplayMode(CGDirectDisplayID, CGDisplayMode?, CFDictionary?) -> CGError](/documentation/coregraphics/cgdisplaysetdisplaymode(_:_:_:))

### Getting Information About a Display Mode

- [var width: Int](/documentation/coregraphics/cgdisplaymode/width)
- [var height: Int](/documentation/coregraphics/cgdisplaymode/height)
- [var pixelEncoding: CFString?](/documentation/coregraphics/cgdisplaymode/pixelencoding)
- [var refreshRate: Double](/documentation/coregraphics/cgdisplaymode/refreshrate)
- [var ioFlags: UInt32](/documentation/coregraphics/cgdisplaymode/ioflags)
- [var ioDisplayModeID: Int32](/documentation/coregraphics/cgdisplaymode/iodisplaymodeid)
- [func isUsableForDesktopGUI() -> Bool](/documentation/coregraphics/cgdisplaymode/isusablefordesktopgui())
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaymode/typeid)

### Adjusting the Display Gamma

- [func CGSetDisplayTransferByFormula(CGDirectDisplayID, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbyformula(_:_:_:_:_:_:_:_:_:_:))
- [func CGGetDisplayTransferByFormula(CGDirectDisplayID, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?) -> CGError](/documentation/coregraphics/cggetdisplaytransferbyformula(_:_:_:_:_:_:_:_:_:_:))
- [func CGSetDisplayTransferByTable(CGDirectDisplayID, UInt32, UnsafePointer<CGGammaValue>?, UnsafePointer<CGGammaValue>?, UnsafePointer<CGGammaValue>?) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbytable(_:_:_:_:_:))
- [func CGGetDisplayTransferByTable(CGDirectDisplayID, UInt32, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplaytransferbytable(_:_:_:_:_:_:))
- [func CGSetDisplayTransferByByteTable(CGDirectDisplayID, UInt32, UnsafePointer<UInt8>, UnsafePointer<UInt8>, UnsafePointer<UInt8>) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbybytetable(_:_:_:_:_:))
- [func CGDisplayRestoreColorSyncSettings()](/documentation/coregraphics/cgdisplayrestorecolorsyncsettings())
- [func CGDisplayGammaTableCapacity(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplaygammatablecapacity(_:))

### Display Fade Effects

- [func CGConfigureDisplayFadeEffect(CGDisplayConfigRef?, CGDisplayFadeInterval, CGDisplayFadeInterval, Float, Float, Float) -> CGError](/documentation/coregraphics/cgconfiguredisplayfadeeffect(_:_:_:_:_:_:))
- [func CGAcquireDisplayFadeReservation(CGDisplayReservationInterval, UnsafeMutablePointer<CGDisplayFadeReservationToken>?) -> CGError](/documentation/coregraphics/cgacquiredisplayfadereservation(_:_:))
- [func CGDisplayFade(CGDisplayFadeReservationToken, CGDisplayFadeInterval, CGDisplayBlendFraction, CGDisplayBlendFraction, Float, Float, Float, boolean_t) -> CGError](/documentation/coregraphics/cgdisplayfade(_:_:_:_:_:_:_:_:))
- [func CGDisplayFadeOperationInProgress() -> boolean_t](/documentation/coregraphics/cgdisplayfadeoperationinprogress())
- [func CGReleaseDisplayFadeReservation(CGDisplayFadeReservationToken) -> CGError](/documentation/coregraphics/cgreleasedisplayfadereservation(_:))

### Controlling the Mouse Cursor

- [func CGDisplayHideCursor(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayhidecursor(_:))
- [func CGDisplayShowCursor(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayshowcursor(_:))
- [func CGDisplayMoveCursorToPoint(CGDirectDisplayID, CGPoint) -> CGError](/documentation/coregraphics/cgdisplaymovecursortopoint(_:_:))
- [func CGCursorIsVisible() -> boolean_t](/documentation/coregraphics/cgcursorisvisible())
- [func CGCursorIsDrawnInFramebuffer() -> boolean_t](/documentation/coregraphics/cgcursorisdrawninframebuffer())
- [func CGAssociateMouseAndMouseCursorPosition(boolean_t) -> CGError](/documentation/coregraphics/cgassociatemouseandmousecursorposition(_:))
- [func CGWarpMouseCursorPosition(CGPoint) -> CGError](/documentation/coregraphics/cgwarpmousecursorposition(_:))
- [func CGGetLastMouseDelta() -> (x: Int32, y: Int32)](/documentation/coregraphics/cggetlastmousedelta())

### Getting Window Server Information

- [func CGSessionCopyCurrentDictionary() -> CFDictionary?](/documentation/coregraphics/cgsessioncopycurrentdictionary())
- [func CGWindowServerCFMachPort() -> CFMachPort?](/documentation/coregraphics/cgwindowservercfmachport())
- [func CGWindowLevelForKey(CGWindowLevelKey) -> CGWindowLevel](/documentation/coregraphics/cgwindowlevelforkey(_:))

### Getting Information About Refresh and Move Operations

- [func CGRegisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgregisterscreenrefreshcallback(_:_:))
- [func CGUnregisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgunregisterscreenrefreshcallback(_:_:))
- [func CGWaitForScreenRefreshRects(UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cgwaitforscreenrefreshrects(_:_:))
- [func CGScreenRegisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgscreenregistermovecallback(_:_:))
- [func CGScreenUnregisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgscreenunregistermovecallback(_:_:))
- [func CGWaitForScreenUpdateRects(CGScreenUpdateOperation, UnsafeMutablePointer<CGScreenUpdateOperation>?, UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<CGScreenUpdateMoveDelta>?) -> CGError](/documentation/coregraphics/cgwaitforscreenupdaterects(_:_:_:_:_:))
- [func CGReleaseScreenRefreshRects(UnsafeMutablePointer<CGRect>?)](/documentation/coregraphics/cgreleasescreenrefreshrects(_:))

### Streaming the Contents of a Display

- [init?(display: CGDirectDisplayID, outputWidth: Int, outputHeight: Int, pixelFormat: Int32, properties: CFDictionary?, handler: CGDisplayStreamFrameAvailableHandler?)](/documentation/coregraphics/cgdisplaystream/init(display:outputwidth:outputheight:pixelformat:properties:handler:))
- [init?(dispatchQueueDisplay: CGDirectDisplayID, outputWidth: Int, outputHeight: Int, pixelFormat: Int32, properties: CFDictionary?, queue: dispatch_queue_t, handler: CGDisplayStreamFrameAvailableHandler?)](/documentation/coregraphics/cgdisplaystream/init(dispatchqueuedisplay:outputwidth:outputheight:pixelformat:properties:queue:handler:))
- [func start() -> CGError](/documentation/coregraphics/cgdisplaystream/start())
- [func stop() -> CGError](/documentation/coregraphics/cgdisplaystream/stop())
- [var runLoopSource: CFRunLoopSource?](/documentation/coregraphics/cgdisplaystream/runloopsource)
- [func getRects(CGDisplayStreamUpdateRectType, rectCount: UnsafeMutablePointer<Int>) -> UnsafePointer<CGRect>?](/documentation/coregraphics/cgdisplaystreamupdate/getrects(_:rectcount:))
- [init?(mergedUpdateFirstUpdate: CGDisplayStreamUpdate?, secondUpdate: CGDisplayStreamUpdate?)](/documentation/coregraphics/cgdisplaystreamupdate/init(mergedupdatefirstupdate:secondupdate:))
- [func getMovedRectsDelta(dx: UnsafeMutablePointer<CGFloat>, dy: UnsafeMutablePointer<CGFloat>)](/documentation/coregraphics/cgdisplaystreamupdate/getmovedrectsdelta(dx:dy:))
- [var dropCount: Int](/documentation/coregraphics/cgdisplaystreamupdate/dropcount)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaystream/typeid)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaystreamupdate/typeid)

### Callbacks

- [CGDisplayReconfigurationCallBack](/documentation/coregraphics/cgdisplayreconfigurationcallback)
- [CGScreenRefreshCallback](/documentation/coregraphics/cgscreenrefreshcallback)
- [CGScreenUpdateMoveCallback](/documentation/coregraphics/cgscreenupdatemovecallback)

### Data Types

- [CGDirectDisplayID](/documentation/coregraphics/cgdirectdisplayid)
- [CGDisplayBlendFraction](/documentation/coregraphics/cgdisplayblendfraction)
- [CGDisplayConfigRef](/documentation/coregraphics/cgdisplayconfigref)
- [CGDisplayCount](/documentation/coregraphics/cgdisplaycount)
- [CGDisplayErr](/documentation/coregraphics/cgdisplayerr)
- [CGDisplayFadeInterval](/documentation/coregraphics/cgdisplayfadeinterval)
- [CGDisplayFadeReservationToken](/documentation/coregraphics/cgdisplayfadereservationtoken)
- [CGDisplayMode](/documentation/coregraphics/cgdisplaymode)

#### Instance Properties

- [var height: Int](/documentation/coregraphics/cgdisplaymode/height)
- [var ioDisplayModeID: Int32](/documentation/coregraphics/cgdisplaymode/iodisplaymodeid)
- [var ioFlags: UInt32](/documentation/coregraphics/cgdisplaymode/ioflags)
- [var pixelHeight: Int](/documentation/coregraphics/cgdisplaymode/pixelheight)
- [var pixelWidth: Int](/documentation/coregraphics/cgdisplaymode/pixelwidth)
- [var refreshRate: Double](/documentation/coregraphics/cgdisplaymode/refreshrate)
- [var width: Int](/documentation/coregraphics/cgdisplaymode/width)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaymode/typeid)

#### Instance Methods

- [var pixelEncoding: CFString?](/documentation/coregraphics/cgdisplaymode/pixelencoding)
- [func isUsableForDesktopGUI() -> Bool](/documentation/coregraphics/cgdisplaymode/isusablefordesktopgui())
- [CGDisplayReservationInterval](/documentation/coregraphics/cgdisplayreservationinterval)
- [CGGammaValue](/documentation/coregraphics/cggammavalue)
- [CGOpenGLDisplayMask](/documentation/coregraphics/cgopengldisplaymask)
- [CGRectCount](/documentation/coregraphics/cgrectcount)
- [CGRefreshRate](/documentation/coregraphics/cgrefreshrate)
- [CGScreenUpdateMoveDelta](/documentation/coregraphics/cgscreenupdatemovedelta)

#### Initializers

- [init()](/documentation/coregraphics/cgscreenupdatemovedelta/init())
- [init(dX: Int32, dY: Int32)](/documentation/coregraphics/cgscreenupdatemovedelta/init(dx:dy:))

#### Instance Properties

- [var dX: Int32](/documentation/coregraphics/cgscreenupdatemovedelta/dx)
- [var dY: Int32](/documentation/coregraphics/cgscreenupdatemovedelta/dy)
- [CGWindowLevel](/documentation/coregraphics/cgwindowlevel)

#### Window levels

- [CGWindowLevelKey](/documentation/coregraphics/cgwindowlevelkey)

##### Constants

- [case baseWindow](/documentation/coregraphics/cgwindowlevelkey/basewindow)
- [case minimumWindow](/documentation/coregraphics/cgwindowlevelkey/minimumwindow)
- [case desktopWindow](/documentation/coregraphics/cgwindowlevelkey/desktopwindow)
- [case backstopMenu](/documentation/coregraphics/cgwindowlevelkey/backstopmenu)
- [case normalWindow](/documentation/coregraphics/cgwindowlevelkey/normalwindow)
- [case floatingWindow](/documentation/coregraphics/cgwindowlevelkey/floatingwindow)
- [case tornOffMenuWindow](/documentation/coregraphics/cgwindowlevelkey/tornoffmenuwindow)
- [case dockWindow](/documentation/coregraphics/cgwindowlevelkey/dockwindow)
- [case mainMenuWindow](/documentation/coregraphics/cgwindowlevelkey/mainmenuwindow)
- [case statusWindow](/documentation/coregraphics/cgwindowlevelkey/statuswindow)
- [case modalPanelWindow](/documentation/coregraphics/cgwindowlevelkey/modalpanelwindow)
- [case popUpMenuWindow](/documentation/coregraphics/cgwindowlevelkey/popupmenuwindow)
- [case draggingWindow](/documentation/coregraphics/cgwindowlevelkey/draggingwindow)
- [case screenSaverWindow](/documentation/coregraphics/cgwindowlevelkey/screensaverwindow)
- [case maximumWindow](/documentation/coregraphics/cgwindowlevelkey/maximumwindow)
- [case overlayWindow](/documentation/coregraphics/cgwindowlevelkey/overlaywindow)
- [case helpWindow](/documentation/coregraphics/cgwindowlevelkey/helpwindow)
- [case utilityWindow](/documentation/coregraphics/cgwindowlevelkey/utilitywindow)
- [case desktopIconWindow](/documentation/coregraphics/cgwindowlevelkey/desktopiconwindow)
- [case cursorWindow](/documentation/coregraphics/cgwindowlevelkey/cursorwindow)
- [case assistiveTechHighWindow](/documentation/coregraphics/cgwindowlevelkey/assistivetechhighwindow)
- [case numberOfWindowLevelKeys](/documentation/coregraphics/cgwindowlevelkey/numberofwindowlevelkeys)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgwindowlevelkey/init(rawvalue:))
- [CGDisplayStream](/documentation/coregraphics/cgdisplaystream)

#### Type Properties

- [class let yCbCrMatrix_ITU_R_601_4: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_601_4)
- [class let yCbCrMatrix_ITU_R_709_2: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_709_2)
- [class let yCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_smpte_240m_1995)
- [CGDisplayStreamUpdate](/documentation/coregraphics/cgdisplaystreamupdate)
- [CGDisplayStreamFrameAvailableHandler](/documentation/coregraphics/cgdisplaystreamframeavailablehandler)

### Constants

- [CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions)

#### Constants

- [static var noFill: CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions/nofill)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgcaptureoptions/init(rawvalue:))
- [CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags)

#### Constants

- [static var beginConfigurationFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/beginconfigurationflag)
- [static var movedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/movedflag)
- [static var setMainFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmainflag)
- [static var setModeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmodeflag)
- [static var addFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/addflag)
- [static var removeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/removeflag)
- [static var enabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/enabledflag)
- [static var disabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/disabledflag)
- [static var mirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/mirrorflag)
- [static var unMirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/unmirrorflag)
- [static var desktopShapeChangedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/desktopshapechangedflag)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgdisplaychangesummaryflags/init(rawvalue:))
- [CGConfigureOption](/documentation/coregraphics/cgconfigureoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgconfigureoption/init(rawvalue:))

#### Type Properties

- [static var forAppOnly: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forapponly)
- [static var forSession: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forsession)
- [static var permanently: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/permanently)
- [Display Fade Blend Fractions](/documentation/coregraphics/display-fade-blend-fractions)

#### Constants

- [var kCGDisplayBlendNormal: Double](/documentation/coregraphics/kcgdisplayblendnormal)
- [var kCGDisplayBlendSolidColor: Double](/documentation/coregraphics/kcgdisplayblendsolidcolor)
- [Display Fade Constants](/documentation/coregraphics/display-fade-constants)

#### Constants

- [var kCGDisplayFadeReservationInvalidToken: Int32](/documentation/coregraphics/kcgdisplayfadereservationinvalidtoken)
- [Display ID Defaults](/documentation/coregraphics/display-id-defaults)

#### Constants

- [var kCGNullDirectDisplay: CGDirectDisplayID](/documentation/coregraphics/kcgnulldirectdisplay)
- [Display Mode Standard Properties](/documentation/coregraphics/display-mode-standard-properties)

#### Constants

- [var kCGDisplayWidth: String](/documentation/coregraphics/kcgdisplaywidth)
- [var kCGDisplayHeight: String](/documentation/coregraphics/kcgdisplayheight)
- [var kCGDisplayMode: String](/documentation/coregraphics/kcgdisplaymode)
- [var kCGDisplayBitsPerPixel: String](/documentation/coregraphics/kcgdisplaybitsperpixel)
- [var kCGDisplayBitsPerSample: String](/documentation/coregraphics/kcgdisplaybitspersample)
- [var kCGDisplaySamplesPerPixel: String](/documentation/coregraphics/kcgdisplaysamplesperpixel)
- [var kCGDisplayRefreshRate: String](/documentation/coregraphics/kcgdisplayrefreshrate)
- [var kCGDisplayModeUsableForDesktopGUI: String](/documentation/coregraphics/kcgdisplaymodeusablefordesktopgui)
- [var kCGDisplayIOFlags: String](/documentation/coregraphics/kcgdisplayioflags)
- [var kCGDisplayBytesPerRow: String](/documentation/coregraphics/kcgdisplaybytesperrow)
- [Display Mode Optional Properties](/documentation/coregraphics/display-mode-optional-properties)

#### Constants

- [var kCGDisplayModeIsSafeForHardware: String](/documentation/coregraphics/kcgdisplaymodeissafeforhardware)
- [var kCGDisplayModeIsInterlaced: String](/documentation/coregraphics/kcgdisplaymodeisinterlaced)
- [var kCGDisplayModeIsStretched: String](/documentation/coregraphics/kcgdisplaymodeisstretched)
- [var kCGDisplayModeIsTelevisionOutput: String](/documentation/coregraphics/kcgdisplaymodeistelevisionoutput)
- [Reserved Window Levels](/documentation/coregraphics/reserved-window-levels)

#### Constants

- [var kCGNumReservedWindowLevels: Int32](/documentation/coregraphics/kcgnumreservedwindowlevels)
- [CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation)

#### Constants

- [static var refresh: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/refresh)
- [static var move: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/move)
- [static var reducedDirtyRectangleCount: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/reduceddirtyrectanglecount)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgscreenupdateoperation/init(rawvalue:))
- [CGWindowLevelKey](/documentation/coregraphics/cgwindowlevelkey)

#### Constants

- [case baseWindow](/documentation/coregraphics/cgwindowlevelkey/basewindow)
- [case minimumWindow](/documentation/coregraphics/cgwindowlevelkey/minimumwindow)
- [case desktopWindow](/documentation/coregraphics/cgwindowlevelkey/desktopwindow)
- [case backstopMenu](/documentation/coregraphics/cgwindowlevelkey/backstopmenu)
- [case normalWindow](/documentation/coregraphics/cgwindowlevelkey/normalwindow)
- [case floatingWindow](/documentation/coregraphics/cgwindowlevelkey/floatingwindow)
- [case tornOffMenuWindow](/documentation/coregraphics/cgwindowlevelkey/tornoffmenuwindow)
- [case dockWindow](/documentation/coregraphics/cgwindowlevelkey/dockwindow)
- [case mainMenuWindow](/documentation/coregraphics/cgwindowlevelkey/mainmenuwindow)
- [case statusWindow](/documentation/coregraphics/cgwindowlevelkey/statuswindow)
- [case modalPanelWindow](/documentation/coregraphics/cgwindowlevelkey/modalpanelwindow)
- [case popUpMenuWindow](/documentation/coregraphics/cgwindowlevelkey/popupmenuwindow)
- [case draggingWindow](/documentation/coregraphics/cgwindowlevelkey/draggingwindow)
- [case screenSaverWindow](/documentation/coregraphics/cgwindowlevelkey/screensaverwindow)
- [case maximumWindow](/documentation/coregraphics/cgwindowlevelkey/maximumwindow)
- [case overlayWindow](/documentation/coregraphics/cgwindowlevelkey/overlaywindow)
- [case helpWindow](/documentation/coregraphics/cgwindowlevelkey/helpwindow)
- [case utilityWindow](/documentation/coregraphics/cgwindowlevelkey/utilitywindow)
- [case desktopIconWindow](/documentation/coregraphics/cgwindowlevelkey/desktopiconwindow)
- [case cursorWindow](/documentation/coregraphics/cgwindowlevelkey/cursorwindow)
- [case assistiveTechHighWindow](/documentation/coregraphics/cgwindowlevelkey/assistivetechhighwindow)
- [case numberOfWindowLevelKeys](/documentation/coregraphics/cgwindowlevelkey/numberofwindowlevelkeys)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgwindowlevelkey/init(rawvalue:))
- [Window Server Session Properties](/documentation/coregraphics/window-server-session-properties)

#### Constants

- [var kCGSessionUserIDKey: String](/documentation/coregraphics/kcgsessionuseridkey)
- [var kCGSessionUserNameKey: String](/documentation/coregraphics/kcgsessionusernamekey)
- [var kCGSessionConsoleSetKey: String](/documentation/coregraphics/kcgsessionconsolesetkey)
- [var kCGSessionOnConsoleKey: String](/documentation/coregraphics/kcgsessiononconsolekey)
- [var kCGSessionLoginDoneKey: String](/documentation/coregraphics/kcgsessionlogindonekey)
- [CGDisplayStreamUpdateRectType](/documentation/coregraphics/cgdisplaystreamupdaterecttype)

#### Constants

- [case refreshedRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/refreshedrects)
- [case movedRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/movedrects)
- [case dirtyRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/dirtyrects)
- [case reducedDirtyRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/reduceddirtyrects)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgdisplaystreamupdaterecttype/init(rawvalue:))
- [CGDisplayStreamFrameStatus](/documentation/coregraphics/cgdisplaystreamframestatus)

#### Constants

- [case frameComplete](/documentation/coregraphics/cgdisplaystreamframestatus/framecomplete)
- [case frameIdle](/documentation/coregraphics/cgdisplaystreamframestatus/frameidle)
- [case frameBlank](/documentation/coregraphics/cgdisplaystreamframestatus/frameblank)
- [case stopped](/documentation/coregraphics/cgdisplaystreamframestatus/stopped)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgdisplaystreamframestatus/init(rawvalue:))
- [Display Stream Optional Property Keys](/documentation/coregraphics/display-stream-optional-property-keys)

#### Constants

- [class let sourceRect: CFString](/documentation/coregraphics/cgdisplaystream/sourcerect)
- [class let destinationRect: CFString](/documentation/coregraphics/cgdisplaystream/destinationrect)
- [class let preserveAspectRatio: CFString](/documentation/coregraphics/cgdisplaystream/preserveaspectratio)
- [class let colorSpace: CFString](/documentation/coregraphics/cgdisplaystream/colorspace)
- [class let minimumFrameTime: CFString](/documentation/coregraphics/cgdisplaystream/minimumframetime)
- [class let showCursor: CFString](/documentation/coregraphics/cgdisplaystream/showcursor)
- [class let queueDepth: CFString](/documentation/coregraphics/cgdisplaystream/queuedepth)
- [class let yCbCrMatrix: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix)
- [Display Stream YCbCr to RGB conversion Matrix Options](/documentation/coregraphics/display-stream-ycbcr-to-rgb-conversion-matrix-options)

#### Constants

- [class let yCbCrMatrix_ITU_R_709_2: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_709_2)
- [class let yCbCrMatrix_ITU_R_601_4: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_601_4)
- [class let yCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_smpte_240m_1995)
- [Quartz Event Services](/documentation/coregraphics/quartz-event-services)

### Working With Events

- [class var typeID: CFTypeID](/documentation/coregraphics/cgevent/typeid)
- [init?(source: CGEventSource?)](/documentation/coregraphics/cgevent/init(source:))
- [init?(withDataAllocator: CFAllocator?, data: CFData?)](/documentation/coregraphics/cgevent/init(withdataallocator:data:))
- [init?(mouseEventSource: CGEventSource?, mouseType: CGEventType, mouseCursorPosition: CGPoint, mouseButton: CGMouseButton)](/documentation/coregraphics/cgevent/init(mouseeventsource:mousetype:mousecursorposition:mousebutton:))
- [init?(keyboardEventSource: CGEventSource?, virtualKey: CGKeyCode, keyDown: Bool)](/documentation/coregraphics/cgevent/init(keyboardeventsource:virtualkey:keydown:))
- [func copy() -> CGEvent?](/documentation/coregraphics/cgevent/copy())
- [init?(event: CGEvent?)](/documentation/coregraphics/cgeventsource/init(event:))
- [func setSource(CGEventSource?)](/documentation/coregraphics/cgevent/setsource(_:))
- [var type: CGEventType](/documentation/coregraphics/cgevent/type)
- [var timestamp: CGEventTimestamp](/documentation/coregraphics/cgevent/timestamp)
- [var location: CGPoint](/documentation/coregraphics/cgevent/location)
- [var unflippedLocation: CGPoint](/documentation/coregraphics/cgevent/unflippedlocation)
- [var flags: CGEventFlags](/documentation/coregraphics/cgevent/flags)
- [func keyboardGetUnicodeString(maxStringLength: Int, actualStringLength: UnsafeMutablePointer<Int>?, unicodeString: UnsafeMutablePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardgetunicodestring(maxstringlength:actualstringlength:unicodestring:))
- [func keyboardSetUnicodeString(stringLength: Int, unicodeString: UnsafePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardsetunicodestring(stringlength:unicodestring:))
- [func getIntegerValueField(CGEventField) -> Int64](/documentation/coregraphics/cgevent/getintegervaluefield(_:))
- [func setIntegerValueField(CGEventField, value: Int64)](/documentation/coregraphics/cgevent/setintegervaluefield(_:value:))
- [func getDoubleValueField(CGEventField) -> Double](/documentation/coregraphics/cgevent/getdoublevaluefield(_:))
- [func setDoubleValueField(CGEventField, value: Double)](/documentation/coregraphics/cgevent/setdoublevaluefield(_:value:))

### Working With Event Taps

- [class func tapCreate(tap: CGEventTapLocation, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreate(tap:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPSN(processSerialNumber: UnsafeMutableRawPointer, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpsn(processserialnumber:place:options:eventsofinterest:callback:userinfo:))
- [class func tapEnable(tap: CFMachPort, enable: Bool)](/documentation/coregraphics/cgevent/tapenable(tap:enable:))
- [class func tapIsEnabled(tap: CFMachPort) -> Bool](/documentation/coregraphics/cgevent/tapisenabled(tap:))
- [func tapPostEvent(CGEventTapProxy?)](/documentation/coregraphics/cgevent/tappostevent(_:))
- [func post(tap: CGEventTapLocation)](/documentation/coregraphics/cgevent/post(tap:))
- [func postToPSN(processSerialNumber: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgevent/posttopsn(processserialnumber:))
- [func CGGetEventTapList(UInt32, UnsafeMutablePointer<CGEventTapInformation>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggeteventtaplist(_:_:_:))

### Working With Event Sources

- [class var typeID: CFTypeID](/documentation/coregraphics/cgeventsource/typeid)
- [init?(stateID: CGEventSourceStateID)](/documentation/coregraphics/cgeventsource/init(stateid:))
- [var keyboardType: CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsource/keyboardtype)
- [var sourceStateID: CGEventSourceStateID](/documentation/coregraphics/cgeventsource/sourcestateid)
- [class func buttonState(CGEventSourceStateID, button: CGMouseButton) -> Bool](/documentation/coregraphics/cgeventsource/buttonstate(_:button:))
- [class func keyState(CGEventSourceStateID, key: CGKeyCode) -> Bool](/documentation/coregraphics/cgeventsource/keystate(_:key:))
- [class func flagsState(CGEventSourceStateID) -> CGEventFlags](/documentation/coregraphics/cgeventsource/flagsstate(_:))
- [class func secondsSinceLastEventType(CGEventSourceStateID, eventType: CGEventType) -> CFTimeInterval](/documentation/coregraphics/cgeventsource/secondssincelasteventtype(_:eventtype:))
- [class func counterForEventType(CGEventSourceStateID, eventType: CGEventType) -> UInt32](/documentation/coregraphics/cgeventsource/counterforeventtype(_:eventtype:))
- [var userData: Int64](/documentation/coregraphics/cgeventsource/userdata)
- [func getLocalEventsFilterDuringSuppressionState(CGEventSuppressionState) -> CGEventFilterMask](/documentation/coregraphics/cgeventsource/getlocaleventsfilterduringsuppressionstate(_:))
- [func setLocalEventsFilterDuringSuppressionState(CGEventFilterMask, state: CGEventSuppressionState)](/documentation/coregraphics/cgeventsource/setlocaleventsfilterduringsuppressionstate(_:state:))
- [var localEventsSuppressionInterval: CFTimeInterval](/documentation/coregraphics/cgeventsource/localeventssuppressioninterval)
- [var pixelsPerLine: Double](/documentation/coregraphics/cgeventsource/pixelsperline)

### Callbacks

- [CGEventTapCallBack](/documentation/coregraphics/cgeventtapcallback)

### Data Types

- [CGButtonCount](/documentation/coregraphics/cgbuttoncount)
- [CGCharCode](/documentation/coregraphics/cgcharcode)
- [CGEventMask](/documentation/coregraphics/cgeventmask)
- [CGEvent](/documentation/coregraphics/cgevent)

#### Initializers

- [func copy() -> CGEvent?](/documentation/coregraphics/cgevent/copy())
- [init?(keyboardEventSource: CGEventSource?, virtualKey: CGKeyCode, keyDown: Bool)](/documentation/coregraphics/cgevent/init(keyboardeventsource:virtualkey:keydown:))
- [init?(mouseEventSource: CGEventSource?, mouseType: CGEventType, mouseCursorPosition: CGPoint, mouseButton: CGMouseButton)](/documentation/coregraphics/cgevent/init(mouseeventsource:mousetype:mousecursorposition:mousebutton:))
- [init?(source: CGEventSource?)](/documentation/coregraphics/cgevent/init(source:))
- [init?(withDataAllocator: CFAllocator?, data: CFData?)](/documentation/coregraphics/cgevent/init(withdataallocator:data:))
- [init?(scrollWheelEvent2Source: CGEventSource?, units: CGScrollEventUnit, wheelCount: UInt32, wheel1: Int32, wheel2: Int32, wheel3: Int32)](/documentation/coregraphics/cgevent/init(scrollwheelevent2source:units:wheelcount:wheel1:wheel2:wheel3:))

#### Instance Properties

- [var flags: CGEventFlags](/documentation/coregraphics/cgevent/flags)
- [var location: CGPoint](/documentation/coregraphics/cgevent/location)
- [var timestamp: CGEventTimestamp](/documentation/coregraphics/cgevent/timestamp)
- [var type: CGEventType](/documentation/coregraphics/cgevent/type)
- [var unflippedLocation: CGPoint](/documentation/coregraphics/cgevent/unflippedlocation)
- [var data: CFData?](/documentation/coregraphics/cgevent/data)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgevent/typeid)

#### Instance Methods

- [func getDoubleValueField(CGEventField) -> Double](/documentation/coregraphics/cgevent/getdoublevaluefield(_:))
- [func getIntegerValueField(CGEventField) -> Int64](/documentation/coregraphics/cgevent/getintegervaluefield(_:))
- [func keyboardGetUnicodeString(maxStringLength: Int, actualStringLength: UnsafeMutablePointer<Int>?, unicodeString: UnsafeMutablePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardgetunicodestring(maxstringlength:actualstringlength:unicodestring:))
- [func keyboardSetUnicodeString(stringLength: Int, unicodeString: UnsafePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardsetunicodestring(stringlength:unicodestring:))
- [func post(tap: CGEventTapLocation)](/documentation/coregraphics/cgevent/post(tap:))
- [func postToPSN(processSerialNumber: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgevent/posttopsn(processserialnumber:))
- [func postToPid(pid_t)](/documentation/coregraphics/cgevent/posttopid(_:))
- [func setDoubleValueField(CGEventField, value: Double)](/documentation/coregraphics/cgevent/setdoublevaluefield(_:value:))
- [func setIntegerValueField(CGEventField, value: Int64)](/documentation/coregraphics/cgevent/setintegervaluefield(_:value:))
- [func setSource(CGEventSource?)](/documentation/coregraphics/cgevent/setsource(_:))
- [func tapPostEvent(CGEventTapProxy?)](/documentation/coregraphics/cgevent/tappostevent(_:))

#### Type Methods

- [class func tapCreate(tap: CGEventTapLocation, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreate(tap:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPSN(processSerialNumber: UnsafeMutableRawPointer, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpsn(processserialnumber:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPid(pid: pid_t, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpid(pid:place:options:eventsofinterest:callback:userinfo:))
- [class func tapEnable(tap: CFMachPort, enable: Bool)](/documentation/coregraphics/cgevent/tapenable(tap:enable:))
- [class func tapIsEnabled(tap: CFMachPort) -> Bool](/documentation/coregraphics/cgevent/tapisenabled(tap:))
- [CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsourcekeyboardtype)
- [CGEventSource](/documentation/coregraphics/cgeventsource)

#### Initializers

- [init?(event: CGEvent?)](/documentation/coregraphics/cgeventsource/init(event:))
- [init?(stateID: CGEventSourceStateID)](/documentation/coregraphics/cgeventsource/init(stateid:))

#### Instance Properties

- [var keyboardType: CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsource/keyboardtype)
- [var localEventsSuppressionInterval: CFTimeInterval](/documentation/coregraphics/cgeventsource/localeventssuppressioninterval)
- [var pixelsPerLine: Double](/documentation/coregraphics/cgeventsource/pixelsperline)
- [var sourceStateID: CGEventSourceStateID](/documentation/coregraphics/cgeventsource/sourcestateid)
- [var userData: Int64](/documentation/coregraphics/cgeventsource/userdata)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgeventsource/typeid)

#### Instance Methods

- [func getLocalEventsFilterDuringSuppressionState(CGEventSuppressionState) -> CGEventFilterMask](/documentation/coregraphics/cgeventsource/getlocaleventsfilterduringsuppressionstate(_:))
- [func setLocalEventsFilterDuringSuppressionState(CGEventFilterMask, state: CGEventSuppressionState)](/documentation/coregraphics/cgeventsource/setlocaleventsfilterduringsuppressionstate(_:state:))

#### Type Methods

- [class func buttonState(CGEventSourceStateID, button: CGMouseButton) -> Bool](/documentation/coregraphics/cgeventsource/buttonstate(_:button:))
- [class func counterForEventType(CGEventSourceStateID, eventType: CGEventType) -> UInt32](/documentation/coregraphics/cgeventsource/counterforeventtype(_:eventtype:))
- [class func flagsState(CGEventSourceStateID) -> CGEventFlags](/documentation/coregraphics/cgeventsource/flagsstate(_:))
- [class func keyState(CGEventSourceStateID, key: CGKeyCode) -> Bool](/documentation/coregraphics/cgeventsource/keystate(_:key:))
- [class func secondsSinceLastEventType(CGEventSourceStateID, eventType: CGEventType) -> CFTimeInterval](/documentation/coregraphics/cgeventsource/secondssincelasteventtype(_:eventtype:))
- [CGEventTapInformation](/documentation/coregraphics/cgeventtapinformation)
- [CGEventTapProxy](/documentation/coregraphics/cgeventtapproxy)
- [CGEventTimestamp](/documentation/coregraphics/cgeventtimestamp)
- [CGKeyCode](/documentation/coregraphics/cgkeycode)
- [CGWheelCount](/documentation/coregraphics/cgwheelcount)

### Constants

- [CGEventField](/documentation/coregraphics/cgeventfield)

#### Constants

- [case mouseEventNumber](/documentation/coregraphics/cgeventfield/mouseeventnumber)
- [case mouseEventClickState](/documentation/coregraphics/cgeventfield/mouseeventclickstate)
- [case mouseEventPressure](/documentation/coregraphics/cgeventfield/mouseeventpressure)
- [case mouseEventButtonNumber](/documentation/coregraphics/cgeventfield/mouseeventbuttonnumber)
- [case mouseEventDeltaX](/documentation/coregraphics/cgeventfield/mouseeventdeltax)
- [case mouseEventDeltaY](/documentation/coregraphics/cgeventfield/mouseeventdeltay)
- [case mouseEventInstantMouser](/documentation/coregraphics/cgeventfield/mouseeventinstantmouser)
- [case mouseEventSubtype](/documentation/coregraphics/cgeventfield/mouseeventsubtype)
- [case keyboardEventAutorepeat](/documentation/coregraphics/cgeventfield/keyboardeventautorepeat)
- [case keyboardEventKeycode](/documentation/coregraphics/cgeventfield/keyboardeventkeycode)
- [case keyboardEventKeyboardType](/documentation/coregraphics/cgeventfield/keyboardeventkeyboardtype)
- [case scrollWheelEventDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis1)
- [case scrollWheelEventDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis2)
- [case scrollWheelEventDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis3)
- [case scrollWheelEventFixedPtDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis1)
- [case scrollWheelEventFixedPtDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis2)
- [case scrollWheelEventFixedPtDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis3)
- [case scrollWheelEventPointDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis1)
- [case scrollWheelEventPointDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis2)
- [case scrollWheelEventPointDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis3)
- [case scrollWheelEventInstantMouser](/documentation/coregraphics/cgeventfield/scrollwheeleventinstantmouser)
- [case tabletEventPointX](/documentation/coregraphics/cgeventfield/tableteventpointx)
- [case tabletEventPointY](/documentation/coregraphics/cgeventfield/tableteventpointy)
- [case tabletEventPointZ](/documentation/coregraphics/cgeventfield/tableteventpointz)
- [case tabletEventPointButtons](/documentation/coregraphics/cgeventfield/tableteventpointbuttons)
- [case tabletEventPointPressure](/documentation/coregraphics/cgeventfield/tableteventpointpressure)
- [case tabletEventTiltX](/documentation/coregraphics/cgeventfield/tableteventtiltx)
- [case tabletEventTiltY](/documentation/coregraphics/cgeventfield/tableteventtilty)
- [case tabletEventRotation](/documentation/coregraphics/cgeventfield/tableteventrotation)
- [case tabletEventTangentialPressure](/documentation/coregraphics/cgeventfield/tableteventtangentialpressure)
- [case tabletEventDeviceID](/documentation/coregraphics/cgeventfield/tableteventdeviceid)
- [case tabletEventVendor1](/documentation/coregraphics/cgeventfield/tableteventvendor1)
- [case tabletEventVendor2](/documentation/coregraphics/cgeventfield/tableteventvendor2)
- [case tabletEventVendor3](/documentation/coregraphics/cgeventfield/tableteventvendor3)
- [case tabletProximityEventVendorID](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorid)
- [case tabletProximityEventTabletID](/documentation/coregraphics/cgeventfield/tabletproximityeventtabletid)
- [case tabletProximityEventPointerID](/documentation/coregraphics/cgeventfield/tabletproximityeventpointerid)
- [case tabletProximityEventDeviceID](/documentation/coregraphics/cgeventfield/tabletproximityeventdeviceid)
- [case tabletProximityEventSystemTabletID](/documentation/coregraphics/cgeventfield/tabletproximityeventsystemtabletid)
- [case tabletProximityEventVendorPointerType](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorpointertype)
- [case tabletProximityEventVendorPointerSerialNumber](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorpointerserialnumber)
- [case tabletProximityEventVendorUniqueID](/documentation/coregraphics/cgeventfield/tabletproximityeventvendoruniqueid)
- [case tabletProximityEventCapabilityMask](/documentation/coregraphics/cgeventfield/tabletproximityeventcapabilitymask)
- [case tabletProximityEventPointerType](/documentation/coregraphics/cgeventfield/tabletproximityeventpointertype)
- [case tabletProximityEventEnterProximity](/documentation/coregraphics/cgeventfield/tabletproximityevententerproximity)
- [case eventTargetProcessSerialNumber](/documentation/coregraphics/cgeventfield/eventtargetprocessserialnumber)
- [case eventTargetUnixProcessID](/documentation/coregraphics/cgeventfield/eventtargetunixprocessid)
- [case eventSourceUnixProcessID](/documentation/coregraphics/cgeventfield/eventsourceunixprocessid)
- [case eventSourceUserData](/documentation/coregraphics/cgeventfield/eventsourceuserdata)
- [case eventSourceUserID](/documentation/coregraphics/cgeventfield/eventsourceuserid)
- [case eventSourceGroupID](/documentation/coregraphics/cgeventfield/eventsourcegroupid)
- [case eventSourceStateID](/documentation/coregraphics/cgeventfield/eventsourcestateid)
- [case scrollWheelEventIsContinuous](/documentation/coregraphics/cgeventfield/scrollwheeleventiscontinuous)
- [case mouseEventWindowUnderMousePointer](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointer)
- [case mouseEventWindowUnderMousePointerThatCanHandleThisEvent](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointerthatcanhandlethisevent)
- [case scrollWheelEventMomentumPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumphase)
- [case scrollWheelEventScrollCount](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollcount)
- [case scrollWheelEventScrollPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollphase)

#### Enumeration Cases

- [case mouseEventWindowUnderMousePointer](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointer)
- [case mouseEventWindowUnderMousePointerThatCanHandleThisEvent](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointerthatcanhandlethisevent)
- [case scrollWheelEventMomentumPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumphase)
- [case scrollWheelEventScrollCount](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollcount)
- [case scrollWheelEventScrollPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollphase)
- [case eventUnacceleratedPointerMovementX](/documentation/coregraphics/cgeventfield/eventunacceleratedpointermovementx)
- [case eventUnacceleratedPointerMovementY](/documentation/coregraphics/cgeventfield/eventunacceleratedpointermovementy)
- [case scrollWheelEventAcceleratedDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventaccelerateddeltaaxis1)
- [case scrollWheelEventAcceleratedDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventaccelerateddeltaaxis2)
- [case scrollWheelEventMomentumOptionPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumoptionphase)
- [case scrollWheelEventRawDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventrawdeltaaxis1)
- [case scrollWheelEventRawDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventrawdeltaaxis2)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventfield/init(rawvalue:))
- [CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgeventfiltermask/init(rawvalue:))

#### Type Properties

- [static var permitLocalKeyboardEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalkeyboardevents)
- [static var permitLocalMouseEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalmouseevents)
- [static var permitSystemDefinedEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitsystemdefinedevents)
- [CGEventFlags](/documentation/coregraphics/cgeventflags)

#### Constants

- [static var maskAlphaShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalphashift)
- [static var maskShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskshift)
- [static var maskControl: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcontrol)
- [static var maskAlternate: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalternate)
- [static var maskCommand: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcommand)
- [static var maskHelp: CGEventFlags](/documentation/coregraphics/cgeventflags/maskhelp)
- [static var maskSecondaryFn: CGEventFlags](/documentation/coregraphics/cgeventflags/masksecondaryfn)
- [static var maskNumericPad: CGEventFlags](/documentation/coregraphics/cgeventflags/masknumericpad)
- [static var maskNonCoalesced: CGEventFlags](/documentation/coregraphics/cgeventflags/masknoncoalesced)

#### Initializers

- [init(rawValue: UInt64)](/documentation/coregraphics/cgeventflags/init(rawvalue:))
- [CGEventSourceStateID](/documentation/coregraphics/cgeventsourcestateid)

#### Constants

- [case privateState](/documentation/coregraphics/cgeventsourcestateid/privatestate)
- [case combinedSessionState](/documentation/coregraphics/cgeventsourcestateid/combinedsessionstate)
- [case hidSystemState](/documentation/coregraphics/cgeventsourcestateid/hidsystemstate)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgeventsourcestateid/init(rawvalue:))
- [Event Source Token](/documentation/coregraphics/event-source-token)
- [CGEventSuppressionState](/documentation/coregraphics/cgeventsuppressionstate)

#### Constants

- [case eventSuppressionStateSuppressionInterval](/documentation/coregraphics/cgeventsuppressionstate/eventsuppressionstatesuppressioninterval)
- [case eventSuppressionStateRemoteMouseDrag](/documentation/coregraphics/cgeventsuppressionstate/eventsuppressionstateremotemousedrag)
- [case numberOfEventSuppressionStates](/documentation/coregraphics/cgeventsuppressionstate/numberofeventsuppressionstates)

#### Enumeration Cases

- [case numberOfEventSuppressionStates](/documentation/coregraphics/cgeventsuppressionstate/numberofeventsuppressionstates)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventsuppressionstate/init(rawvalue:))
- [CGEventTapLocation](/documentation/coregraphics/cgeventtaplocation)

#### Constants

- [case cghidEventTap](/documentation/coregraphics/cgeventtaplocation/cghideventtap)
- [case cgSessionEventTap](/documentation/coregraphics/cgeventtaplocation/cgsessioneventtap)
- [case cgAnnotatedSessionEventTap](/documentation/coregraphics/cgeventtaplocation/cgannotatedsessioneventtap)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtaplocation/init(rawvalue:))
- [CGEventTapOptions](/documentation/coregraphics/cgeventtapoptions)

#### Constants

- [case defaultTap](/documentation/coregraphics/cgeventtapoptions/defaulttap)
- [case listenOnly](/documentation/coregraphics/cgeventtapoptions/listenonly)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtapoptions/init(rawvalue:))
- [CGEventTapPlacement](/documentation/coregraphics/cgeventtapplacement)

#### Constants

- [case headInsertEventTap](/documentation/coregraphics/cgeventtapplacement/headinserteventtap)
- [case tailAppendEventTap](/documentation/coregraphics/cgeventtapplacement/tailappendeventtap)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtapplacement/init(rawvalue:))
- [CGEventType](/documentation/coregraphics/cgeventtype)

#### Constants

- [case null](/documentation/coregraphics/cgeventtype/null)
- [case leftMouseDown](/documentation/coregraphics/cgeventtype/leftmousedown)
- [case leftMouseUp](/documentation/coregraphics/cgeventtype/leftmouseup)
- [case rightMouseDown](/documentation/coregraphics/cgeventtype/rightmousedown)
- [case rightMouseUp](/documentation/coregraphics/cgeventtype/rightmouseup)
- [case mouseMoved](/documentation/coregraphics/cgeventtype/mousemoved)
- [case leftMouseDragged](/documentation/coregraphics/cgeventtype/leftmousedragged)
- [case rightMouseDragged](/documentation/coregraphics/cgeventtype/rightmousedragged)
- [case keyDown](/documentation/coregraphics/cgeventtype/keydown)
- [case keyUp](/documentation/coregraphics/cgeventtype/keyup)
- [case flagsChanged](/documentation/coregraphics/cgeventtype/flagschanged)
- [case scrollWheel](/documentation/coregraphics/cgeventtype/scrollwheel)
- [case tabletPointer](/documentation/coregraphics/cgeventtype/tabletpointer)
- [case tabletProximity](/documentation/coregraphics/cgeventtype/tabletproximity)
- [case otherMouseDown](/documentation/coregraphics/cgeventtype/othermousedown)
- [case otherMouseUp](/documentation/coregraphics/cgeventtype/othermouseup)
- [case otherMouseDragged](/documentation/coregraphics/cgeventtype/othermousedragged)
- [case tapDisabledByTimeout](/documentation/coregraphics/cgeventtype/tapdisabledbytimeout)
- [case tapDisabledByUserInput](/documentation/coregraphics/cgeventtype/tapdisabledbyuserinput)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtype/init(rawvalue:))
- [Event Type Mask](/documentation/coregraphics/event-type-mask)
- [CGMouseButton](/documentation/coregraphics/cgmousebutton)

#### Constants

- [case left](/documentation/coregraphics/cgmousebutton/left)
- [case right](/documentation/coregraphics/cgmousebutton/right)
- [case center](/documentation/coregraphics/cgmousebutton/center)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgmousebutton/init(rawvalue:))
- [CGEventMouseSubtype](/documentation/coregraphics/cgeventmousesubtype)

#### Constants

- [case defaultType](/documentation/coregraphics/cgeventmousesubtype/defaulttype)
- [case tabletPoint](/documentation/coregraphics/cgeventmousesubtype/tabletpoint)
- [case tabletProximity](/documentation/coregraphics/cgeventmousesubtype/tabletproximity)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventmousesubtype/init(rawvalue:))
- [CGScrollEventUnit](/documentation/coregraphics/cgscrolleventunit)

#### Constants

- [case pixel](/documentation/coregraphics/cgscrolleventunit/pixel)
- [case line](/documentation/coregraphics/cgscrolleventunit/line)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgscrolleventunit/init(rawvalue:))

### Deprecated Functions

- [func CGPostKeyboardEvent(CGCharCode, CGKeyCode, boolean_t) -> CGError](/documentation/coregraphics/cgpostkeyboardevent(_:_:_:))
- [func CGEnableEventStateCombining(boolean_t) -> CGError](/documentation/coregraphics/cgenableeventstatecombining(_:))
- [func CGInhibitLocalEvents(boolean_t) -> CGError](/documentation/coregraphics/cginhibitlocalevents(_:))
- [func CGSetLocalEventsFilterDuringSuppressionState(CGEventFilterMask, CGEventSuppressionState) -> CGError](/documentation/coregraphics/cgsetlocaleventsfilterduringsuppressionstate(_:_:))
- [func CGSetLocalEventsSuppressionInterval(CFTimeInterval) -> CGError](/documentation/coregraphics/cgsetlocaleventssuppressioninterval(_:))
- [Quartz Window Services](/documentation/coregraphics/quartz-window-services)

### Getting Window Information

- [func CGWindowListCopyWindowInfo(CGWindowListOption, CGWindowID) -> CFArray?](/documentation/coregraphics/cgwindowlistcopywindowinfo(_:_:))
- [func CGWindowListCreateDescriptionFromArray(CFArray?) -> CFArray?](/documentation/coregraphics/cgwindowlistcreatedescriptionfromarray(_:))
- [func CGWindowListCreateImage(CGRect, CGWindowListOption, CGWindowID, CGWindowImageOption) -> CGImage?](/documentation/coregraphics/cgwindowlistcreateimage(_:_:_:_:))
- [init?(windowListFromArrayScreenBounds: CGRect, windowArray: CFArray, imageOption: CGWindowImageOption)](/documentation/coregraphics/cgimage/init(windowlistfromarrayscreenbounds:windowarray:imageoption:))

### Data Types

- [CGWindowID](/documentation/coregraphics/cgwindowid)
- [CGWindowListOption](/documentation/coregraphics/cgwindowlistoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowlistoption/init(rawvalue:))

#### Type Properties

- [static var excludeDesktopElements: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/excludedesktopelements)
- [static var optionAll: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionall)
- [static var optionIncludingWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionincludingwindow)
- [static var optionOnScreenAboveWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenabovewindow)
- [static var optionOnScreenBelowWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenbelowwindow)
- [static var optionOnScreenOnly: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenonly)
- [CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowimageoption/init(rawvalue:))

#### Type Properties

- [static var bestResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/bestresolution)
- [static var boundsIgnoreFraming: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/boundsignoreframing)
- [static var nominalResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/nominalresolution)
- [static var onlyShadows: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/onlyshadows)
- [static var shouldBeOpaque: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/shouldbeopaque)
- [CGWindowSharingType](/documentation/coregraphics/cgwindowsharingtype)

#### Constants

- [case none](/documentation/coregraphics/cgwindowsharingtype/none)
- [case readOnly](/documentation/coregraphics/cgwindowsharingtype/readonly)
- [case readWrite](/documentation/coregraphics/cgwindowsharingtype/readwrite)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgwindowsharingtype/init(rawvalue:))
- [CGWindowBackingType](/documentation/coregraphics/cgwindowbackingtype)

#### Constants

- [case backingStoreBuffered](/documentation/coregraphics/cgwindowbackingtype/backingstorebuffered)
- [case backingStoreNonretained](/documentation/coregraphics/cgwindowbackingtype/backingstorenonretained)
- [case backingStoreRetained](/documentation/coregraphics/cgwindowbackingtype/backingstoreretained)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgwindowbackingtype/init(rawvalue:))

### Constants

- [Window Sharing Constants](/documentation/coregraphics/window-sharing-constants)

#### Constants

- [case none](/documentation/coregraphics/cgwindowsharingtype/none)
- [case readOnly](/documentation/coregraphics/cgwindowsharingtype/readonly)
- [case readWrite](/documentation/coregraphics/cgwindowsharingtype/readwrite)
- [Backing Store Types](/documentation/coregraphics/backing-store-types)

#### Constants

- [case backingStoreRetained](/documentation/coregraphics/cgwindowbackingtype/backingstoreretained)
- [case backingStoreNonretained](/documentation/coregraphics/cgwindowbackingtype/backingstorenonretained)
- [case backingStoreBuffered](/documentation/coregraphics/cgwindowbackingtype/backingstorebuffered)
- [Window List Option Constants](/documentation/coregraphics/window-list-option-constants)

#### Constants

- [static var optionAll: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionall)
- [static var optionOnScreenOnly: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenonly)
- [static var optionOnScreenAboveWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenabovewindow)
- [static var optionOnScreenBelowWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenbelowwindow)
- [static var optionIncludingWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionincludingwindow)
- [static var excludeDesktopElements: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/excludedesktopelements)
- [Window Image Types](/documentation/coregraphics/window-image-types)

#### Constants

- [static var boundsIgnoreFraming: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/boundsignoreframing)
- [static var shouldBeOpaque: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/shouldbeopaque)
- [static var onlyShadows: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/onlyshadows)
- [static var bestResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/bestresolution)
- [static var nominalResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/nominalresolution)
- [CGWindowID Encoding Type](/documentation/coregraphics/cgwindowid-encoding-type)
- [Null Window](/documentation/coregraphics/null-window)

#### Constants

- [var kCGNullWindowID: CGWindowID](/documentation/coregraphics/kcgnullwindowid)
- [Window Sharing Encoding Type](/documentation/coregraphics/window-sharing-encoding-type)
- [Window Backing Encoding Type](/documentation/coregraphics/window-backing-encoding-type)
- [Required Window List Keys](/documentation/coregraphics/required-window-list-keys)

#### Constants

- [let kCGWindowNumber: CFString](/documentation/coregraphics/kcgwindownumber)
- [let kCGWindowStoreType: CFString](/documentation/coregraphics/kcgwindowstoretype)
- [let kCGWindowLayer: CFString](/documentation/coregraphics/kcgwindowlayer)
- [let kCGWindowBounds: CFString](/documentation/coregraphics/kcgwindowbounds)
- [let kCGWindowSharingState: CFString](/documentation/coregraphics/kcgwindowsharingstate)
- [let kCGWindowAlpha: CFString](/documentation/coregraphics/kcgwindowalpha)
- [let kCGWindowOwnerPID: CFString](/documentation/coregraphics/kcgwindowownerpid)
- [let kCGWindowMemoryUsage: CFString](/documentation/coregraphics/kcgwindowmemoryusage)
- [Optional Window List Keys](/documentation/coregraphics/optional-window-list-keys)

#### Constants

- [let kCGWindowWorkspace: CFString](/documentation/coregraphics/kcgwindowworkspace)
- [let kCGWindowOwnerName: CFString](/documentation/coregraphics/kcgwindowownername)
- [let kCGWindowName: CFString](/documentation/coregraphics/kcgwindowname)
- [let kCGWindowIsOnscreen: CFString](/documentation/coregraphics/kcgwindowisonscreen)
- [let kCGWindowBackingLocationVideoMemory: CFString](/documentation/coregraphics/kcgwindowbackinglocationvideomemory)

## Reference

- [Core Graphics Structures](/documentation/coregraphics/core-graphics-structures)

### Structures

- [CGPSConverter](/documentation/coregraphics/cgpsconverter)

#### Initializers

- [init?(info: UnsafeMutableRawPointer?, callbacks: UnsafePointer<CGPSConverterCallbacks>, options: CFDictionary?)](/documentation/coregraphics/cgpsconverter/init(info:callbacks:options:))

#### Instance Properties

- [var isConverting: Bool](/documentation/coregraphics/cgpsconverter/isconverting)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgpsconverter/typeid)

#### Instance Methods

- [func abort() -> Bool](/documentation/coregraphics/cgpsconverter/abort())
- [func convert(CGDataProvider, consumer: CGDataConsumer, options: CFDictionary?) -> Bool](/documentation/coregraphics/cgpsconverter/convert(_:consumer:options:))
- [CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions)

#### Constants

- [static var noFill: CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions/nofill)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgcaptureoptions/init(rawvalue:))
- [CGConfigureOption](/documentation/coregraphics/cgconfigureoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgconfigureoption/init(rawvalue:))

#### Type Properties

- [static var forAppOnly: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forapponly)
- [static var forSession: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forsession)
- [static var permanently: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/permanently)
- [CGDeviceColor](/documentation/coregraphics/cgdevicecolor)

#### Initializers

- [init()](/documentation/coregraphics/cgdevicecolor/init())
- [init(red: Float, green: Float, blue: Float)](/documentation/coregraphics/cgdevicecolor/init(red:green:blue:))

#### Instance Properties

- [var blue: Float](/documentation/coregraphics/cgdevicecolor/blue)
- [var green: Float](/documentation/coregraphics/cgdevicecolor/green)
- [var red: Float](/documentation/coregraphics/cgdevicecolor/red)
- [CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags)

#### Constants

- [static var beginConfigurationFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/beginconfigurationflag)
- [static var movedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/movedflag)
- [static var setMainFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmainflag)
- [static var setModeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmodeflag)
- [static var addFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/addflag)
- [static var removeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/removeflag)
- [static var enabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/enabledflag)
- [static var disabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/disabledflag)
- [static var mirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/mirrorflag)
- [static var unMirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/unmirrorflag)
- [static var desktopShapeChangedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/desktopshapechangedflag)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgdisplaychangesummaryflags/init(rawvalue:))
- [CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgeventfiltermask/init(rawvalue:))

#### Type Properties

- [static var permitLocalKeyboardEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalkeyboardevents)
- [static var permitLocalMouseEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalmouseevents)
- [static var permitSystemDefinedEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitsystemdefinedevents)
- [CGEventFlags](/documentation/coregraphics/cgeventflags)

#### Constants

- [static var maskAlphaShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalphashift)
- [static var maskShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskshift)
- [static var maskControl: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcontrol)
- [static var maskAlternate: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalternate)
- [static var maskCommand: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcommand)
- [static var maskHelp: CGEventFlags](/documentation/coregraphics/cgeventflags/maskhelp)
- [static var maskSecondaryFn: CGEventFlags](/documentation/coregraphics/cgeventflags/masksecondaryfn)
- [static var maskNumericPad: CGEventFlags](/documentation/coregraphics/cgeventflags/masknumericpad)
- [static var maskNonCoalesced: CGEventFlags](/documentation/coregraphics/cgeventflags/masknoncoalesced)

#### Initializers

- [init(rawValue: UInt64)](/documentation/coregraphics/cgeventflags/init(rawvalue:))
- [CGEventTapInformation](/documentation/coregraphics/cgeventtapinformation)
- [CGScreenUpdateMoveDelta](/documentation/coregraphics/cgscreenupdatemovedelta)

#### Initializers

- [init()](/documentation/coregraphics/cgscreenupdatemovedelta/init())
- [init(dX: Int32, dY: Int32)](/documentation/coregraphics/cgscreenupdatemovedelta/init(dx:dy:))

#### Instance Properties

- [var dX: Int32](/documentation/coregraphics/cgscreenupdatemovedelta/dx)
- [var dY: Int32](/documentation/coregraphics/cgscreenupdatemovedelta/dy)
- [CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation)

#### Constants

- [static var refresh: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/refresh)
- [static var move: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/move)
- [static var reducedDirtyRectangleCount: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/reduceddirtyrectanglecount)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgscreenupdateoperation/init(rawvalue:))
- [CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowimageoption/init(rawvalue:))

#### Type Properties

- [static var bestResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/bestresolution)
- [static var boundsIgnoreFraming: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/boundsignoreframing)
- [static var nominalResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/nominalresolution)
- [static var onlyShadows: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/onlyshadows)
- [static var shouldBeOpaque: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/shouldbeopaque)
- [CGWindowListOption](/documentation/coregraphics/cgwindowlistoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowlistoption/init(rawvalue:))

#### Type Properties

- [static var excludeDesktopElements: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/excludedesktopelements)
- [static var optionAll: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionall)
- [static var optionIncludingWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionincludingwindow)
- [static var optionOnScreenAboveWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenabovewindow)
- [static var optionOnScreenBelowWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenbelowwindow)
- [static var optionOnScreenOnly: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenonly)
- [CGColorBufferFormat](/documentation/coregraphics/cgcolorbufferformat)

#### Initializers

- [init()](/documentation/coregraphics/cgcolorbufferformat/init())
- [init(version: UInt32, bitmapInfo: CGBitmapInfo, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int)](/documentation/coregraphics/cgcolorbufferformat/init(version:bitmapinfo:bitspercomponent:bitsperpixel:bytesperrow:))

#### Instance Properties

- [var bitmapInfo: CGBitmapInfo](/documentation/coregraphics/cgcolorbufferformat/bitmapinfo)
- [var bitsPerComponent: Int](/documentation/coregraphics/cgcolorbufferformat/bitspercomponent)
- [var bitsPerPixel: Int](/documentation/coregraphics/cgcolorbufferformat/bitsperpixel)
- [var bytesPerRow: Int](/documentation/coregraphics/cgcolorbufferformat/bytesperrow)
- [var version: UInt32](/documentation/coregraphics/cgcolorbufferformat/version)
- [CGColorDataFormat](/documentation/coregraphics/cgcolordataformat)

#### Initializers

- [init()](/documentation/coregraphics/cgcolordataformat/init())
- [init(version: UInt32, colorspace_info: Unmanaged<CFTypeRef>!, bitmap_info: CGBitmapInfo, bits_per_component: Int, bytes_per_row: Int, intent: CGColorRenderingIntent, decode: UnsafeMutablePointer<CGFloat>!)](/documentation/coregraphics/cgcolordataformat/init(version:colorspace_info:bitmap_info:bits_per_component:bytes_per_row:intent:decode:))

#### Instance Properties

- [var bitmap_info: CGBitmapInfo](/documentation/coregraphics/cgcolordataformat/bitmap_info)
- [var bits_per_component: Int](/documentation/coregraphics/cgcolordataformat/bits_per_component)
- [var bytes_per_row: Int](/documentation/coregraphics/cgcolordataformat/bytes_per_row)
- [var colorspace_info: Unmanaged<CFTypeRef>!](/documentation/coregraphics/cgcolordataformat/colorspace_info)
- [var decode: UnsafeMutablePointer<CGFloat>!](/documentation/coregraphics/cgcolordataformat/decode)
- [var intent: CGColorRenderingIntent](/documentation/coregraphics/cgcolordataformat/intent)
- [var version: UInt32](/documentation/coregraphics/cgcolordataformat/version)
- [CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgpdfaccesspermissions/init(rawvalue:))

#### Type Properties

- [static var allowsCommenting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscommenting)
- [static var allowsContentAccessibility: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscontentaccessibility)
- [static var allowsContentCopying: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscontentcopying)
- [static var allowsDocumentAssembly: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsdocumentassembly)
- [static var allowsDocumentChanges: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsdocumentchanges)
- [static var allowsFormFieldEntry: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsformfieldentry)
- [static var allowsHighQualityPrinting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowshighqualityprinting)
- [static var allowsLowQualityPrinting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowslowqualityprinting)
- [CGPSConverterCallbacks](/documentation/coregraphics/cgpsconvertercallbacks)

#### Initializers

- [init()](/documentation/coregraphics/cgpsconvertercallbacks/init())
- [init(version: UInt32, beginDocument: CGPSConverterBeginDocumentCallback?, endDocument: CGPSConverterEndDocumentCallback?, beginPage: CGPSConverterBeginPageCallback?, endPage: CGPSConverterEndPageCallback?, noteProgress: CGPSConverterProgressCallback?, noteMessage: CGPSConverterMessageCallback?, releaseInfo: CGPSConverterReleaseInfoCallback?)](/documentation/coregraphics/cgpsconvertercallbacks/init(version:begindocument:enddocument:beginpage:endpage:noteprogress:notemessage:releaseinfo:))

#### Instance Properties

- [var beginDocument: CGPSConverterBeginDocumentCallback?](/documentation/coregraphics/cgpsconvertercallbacks/begindocument)
- [var beginPage: CGPSConverterBeginPageCallback?](/documentation/coregraphics/cgpsconvertercallbacks/beginpage)
- [var endDocument: CGPSConverterEndDocumentCallback?](/documentation/coregraphics/cgpsconvertercallbacks/enddocument)
- [var endPage: CGPSConverterEndPageCallback?](/documentation/coregraphics/cgpsconvertercallbacks/endpage)
- [var noteMessage: CGPSConverterMessageCallback?](/documentation/coregraphics/cgpsconvertercallbacks/notemessage)
- [var noteProgress: CGPSConverterProgressCallback?](/documentation/coregraphics/cgpsconvertercallbacks/noteprogress)
- [var releaseInfo: CGPSConverterReleaseInfoCallback?](/documentation/coregraphics/cgpsconvertercallbacks/releaseinfo)
- [var version: UInt32](/documentation/coregraphics/cgpsconvertercallbacks/version)
- [ColorSyncProfile](/documentation/coregraphics/colorsyncprofile)
- [IOSurfaceRef](/documentation/coregraphics/iosurfaceref)
- [Core Graphics Enumerations](/documentation/coregraphics/core-graphics-enumerations)

### Enumerations

- [CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions)

#### Constants

- [static var noFill: CGCaptureOptions](/documentation/coregraphics/cgcaptureoptions/nofill)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgcaptureoptions/init(rawvalue:))
- [CGColorConversionInfoTransformType](/documentation/coregraphics/cgcolorconversioninfotransformtype)

#### Enumeration Cases

- [case transformApplySpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformapplyspace)
- [case transformFromSpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformfromspace)
- [case transformToSpace](/documentation/coregraphics/cgcolorconversioninfotransformtype/transformtospace)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgcolorconversioninfotransformtype/init(rawvalue:))
- [CGColorRenderingIntent](/documentation/coregraphics/cgcolorrenderingintent)

#### Constants

- [case defaultIntent](/documentation/coregraphics/cgcolorrenderingintent/defaultintent)
- [case absoluteColorimetric](/documentation/coregraphics/cgcolorrenderingintent/absolutecolorimetric)
- [case relativeColorimetric](/documentation/coregraphics/cgcolorrenderingintent/relativecolorimetric)
- [case perceptual](/documentation/coregraphics/cgcolorrenderingintent/perceptual)
- [case saturation](/documentation/coregraphics/cgcolorrenderingintent/saturation)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgcolorrenderingintent/init(rawvalue:))
- [CGConfigureOption](/documentation/coregraphics/cgconfigureoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgconfigureoption/init(rawvalue:))

#### Type Properties

- [static var forAppOnly: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forapponly)
- [static var forSession: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/forsession)
- [static var permanently: CGConfigureOption](/documentation/coregraphics/cgconfigureoption/permanently)
- [CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags)

#### Constants

- [static var beginConfigurationFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/beginconfigurationflag)
- [static var movedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/movedflag)
- [static var setMainFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmainflag)
- [static var setModeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/setmodeflag)
- [static var addFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/addflag)
- [static var removeFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/removeflag)
- [static var enabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/enabledflag)
- [static var disabledFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/disabledflag)
- [static var mirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/mirrorflag)
- [static var unMirrorFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/unmirrorflag)
- [static var desktopShapeChangedFlag: CGDisplayChangeSummaryFlags](/documentation/coregraphics/cgdisplaychangesummaryflags/desktopshapechangedflag)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgdisplaychangesummaryflags/init(rawvalue:))
- [CGDisplayStreamFrameStatus](/documentation/coregraphics/cgdisplaystreamframestatus)

#### Constants

- [case frameComplete](/documentation/coregraphics/cgdisplaystreamframestatus/framecomplete)
- [case frameIdle](/documentation/coregraphics/cgdisplaystreamframestatus/frameidle)
- [case frameBlank](/documentation/coregraphics/cgdisplaystreamframestatus/frameblank)
- [case stopped](/documentation/coregraphics/cgdisplaystreamframestatus/stopped)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgdisplaystreamframestatus/init(rawvalue:))
- [CGDisplayStreamUpdateRectType](/documentation/coregraphics/cgdisplaystreamupdaterecttype)

#### Constants

- [case refreshedRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/refreshedrects)
- [case movedRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/movedrects)
- [case dirtyRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/dirtyrects)
- [case reducedDirtyRects](/documentation/coregraphics/cgdisplaystreamupdaterecttype/reduceddirtyrects)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgdisplaystreamupdaterecttype/init(rawvalue:))
- [CGError](/documentation/coregraphics/cgerror)

#### Constants

- [case cannotComplete](/documentation/coregraphics/cgerror/cannotcomplete)
- [case failure](/documentation/coregraphics/cgerror/failure)
- [case illegalArgument](/documentation/coregraphics/cgerror/illegalargument)
- [case invalidConnection](/documentation/coregraphics/cgerror/invalidconnection)
- [case invalidContext](/documentation/coregraphics/cgerror/invalidcontext)
- [case invalidOperation](/documentation/coregraphics/cgerror/invalidoperation)
- [case noneAvailable](/documentation/coregraphics/cgerror/noneavailable)
- [case notImplemented](/documentation/coregraphics/cgerror/notimplemented)
- [case rangeCheck](/documentation/coregraphics/cgerror/rangecheck)
- [case success](/documentation/coregraphics/cgerror/success)
- [case typeCheck](/documentation/coregraphics/cgerror/typecheck)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgerror/init(rawvalue:))
- [CGEventField](/documentation/coregraphics/cgeventfield)

#### Constants

- [case mouseEventNumber](/documentation/coregraphics/cgeventfield/mouseeventnumber)
- [case mouseEventClickState](/documentation/coregraphics/cgeventfield/mouseeventclickstate)
- [case mouseEventPressure](/documentation/coregraphics/cgeventfield/mouseeventpressure)
- [case mouseEventButtonNumber](/documentation/coregraphics/cgeventfield/mouseeventbuttonnumber)
- [case mouseEventDeltaX](/documentation/coregraphics/cgeventfield/mouseeventdeltax)
- [case mouseEventDeltaY](/documentation/coregraphics/cgeventfield/mouseeventdeltay)
- [case mouseEventInstantMouser](/documentation/coregraphics/cgeventfield/mouseeventinstantmouser)
- [case mouseEventSubtype](/documentation/coregraphics/cgeventfield/mouseeventsubtype)
- [case keyboardEventAutorepeat](/documentation/coregraphics/cgeventfield/keyboardeventautorepeat)
- [case keyboardEventKeycode](/documentation/coregraphics/cgeventfield/keyboardeventkeycode)
- [case keyboardEventKeyboardType](/documentation/coregraphics/cgeventfield/keyboardeventkeyboardtype)
- [case scrollWheelEventDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis1)
- [case scrollWheelEventDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis2)
- [case scrollWheelEventDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventdeltaaxis3)
- [case scrollWheelEventFixedPtDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis1)
- [case scrollWheelEventFixedPtDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis2)
- [case scrollWheelEventFixedPtDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventfixedptdeltaaxis3)
- [case scrollWheelEventPointDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis1)
- [case scrollWheelEventPointDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis2)
- [case scrollWheelEventPointDeltaAxis3](/documentation/coregraphics/cgeventfield/scrollwheeleventpointdeltaaxis3)
- [case scrollWheelEventInstantMouser](/documentation/coregraphics/cgeventfield/scrollwheeleventinstantmouser)
- [case tabletEventPointX](/documentation/coregraphics/cgeventfield/tableteventpointx)
- [case tabletEventPointY](/documentation/coregraphics/cgeventfield/tableteventpointy)
- [case tabletEventPointZ](/documentation/coregraphics/cgeventfield/tableteventpointz)
- [case tabletEventPointButtons](/documentation/coregraphics/cgeventfield/tableteventpointbuttons)
- [case tabletEventPointPressure](/documentation/coregraphics/cgeventfield/tableteventpointpressure)
- [case tabletEventTiltX](/documentation/coregraphics/cgeventfield/tableteventtiltx)
- [case tabletEventTiltY](/documentation/coregraphics/cgeventfield/tableteventtilty)
- [case tabletEventRotation](/documentation/coregraphics/cgeventfield/tableteventrotation)
- [case tabletEventTangentialPressure](/documentation/coregraphics/cgeventfield/tableteventtangentialpressure)
- [case tabletEventDeviceID](/documentation/coregraphics/cgeventfield/tableteventdeviceid)
- [case tabletEventVendor1](/documentation/coregraphics/cgeventfield/tableteventvendor1)
- [case tabletEventVendor2](/documentation/coregraphics/cgeventfield/tableteventvendor2)
- [case tabletEventVendor3](/documentation/coregraphics/cgeventfield/tableteventvendor3)
- [case tabletProximityEventVendorID](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorid)
- [case tabletProximityEventTabletID](/documentation/coregraphics/cgeventfield/tabletproximityeventtabletid)
- [case tabletProximityEventPointerID](/documentation/coregraphics/cgeventfield/tabletproximityeventpointerid)
- [case tabletProximityEventDeviceID](/documentation/coregraphics/cgeventfield/tabletproximityeventdeviceid)
- [case tabletProximityEventSystemTabletID](/documentation/coregraphics/cgeventfield/tabletproximityeventsystemtabletid)
- [case tabletProximityEventVendorPointerType](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorpointertype)
- [case tabletProximityEventVendorPointerSerialNumber](/documentation/coregraphics/cgeventfield/tabletproximityeventvendorpointerserialnumber)
- [case tabletProximityEventVendorUniqueID](/documentation/coregraphics/cgeventfield/tabletproximityeventvendoruniqueid)
- [case tabletProximityEventCapabilityMask](/documentation/coregraphics/cgeventfield/tabletproximityeventcapabilitymask)
- [case tabletProximityEventPointerType](/documentation/coregraphics/cgeventfield/tabletproximityeventpointertype)
- [case tabletProximityEventEnterProximity](/documentation/coregraphics/cgeventfield/tabletproximityevententerproximity)
- [case eventTargetProcessSerialNumber](/documentation/coregraphics/cgeventfield/eventtargetprocessserialnumber)
- [case eventTargetUnixProcessID](/documentation/coregraphics/cgeventfield/eventtargetunixprocessid)
- [case eventSourceUnixProcessID](/documentation/coregraphics/cgeventfield/eventsourceunixprocessid)
- [case eventSourceUserData](/documentation/coregraphics/cgeventfield/eventsourceuserdata)
- [case eventSourceUserID](/documentation/coregraphics/cgeventfield/eventsourceuserid)
- [case eventSourceGroupID](/documentation/coregraphics/cgeventfield/eventsourcegroupid)
- [case eventSourceStateID](/documentation/coregraphics/cgeventfield/eventsourcestateid)
- [case scrollWheelEventIsContinuous](/documentation/coregraphics/cgeventfield/scrollwheeleventiscontinuous)
- [case mouseEventWindowUnderMousePointer](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointer)
- [case mouseEventWindowUnderMousePointerThatCanHandleThisEvent](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointerthatcanhandlethisevent)
- [case scrollWheelEventMomentumPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumphase)
- [case scrollWheelEventScrollCount](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollcount)
- [case scrollWheelEventScrollPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollphase)

#### Enumeration Cases

- [case mouseEventWindowUnderMousePointer](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointer)
- [case mouseEventWindowUnderMousePointerThatCanHandleThisEvent](/documentation/coregraphics/cgeventfield/mouseeventwindowundermousepointerthatcanhandlethisevent)
- [case scrollWheelEventMomentumPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumphase)
- [case scrollWheelEventScrollCount](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollcount)
- [case scrollWheelEventScrollPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventscrollphase)
- [case eventUnacceleratedPointerMovementX](/documentation/coregraphics/cgeventfield/eventunacceleratedpointermovementx)
- [case eventUnacceleratedPointerMovementY](/documentation/coregraphics/cgeventfield/eventunacceleratedpointermovementy)
- [case scrollWheelEventAcceleratedDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventaccelerateddeltaaxis1)
- [case scrollWheelEventAcceleratedDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventaccelerateddeltaaxis2)
- [case scrollWheelEventMomentumOptionPhase](/documentation/coregraphics/cgeventfield/scrollwheeleventmomentumoptionphase)
- [case scrollWheelEventRawDeltaAxis1](/documentation/coregraphics/cgeventfield/scrollwheeleventrawdeltaaxis1)
- [case scrollWheelEventRawDeltaAxis2](/documentation/coregraphics/cgeventfield/scrollwheeleventrawdeltaaxis2)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventfield/init(rawvalue:))
- [CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgeventfiltermask/init(rawvalue:))

#### Type Properties

- [static var permitLocalKeyboardEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalkeyboardevents)
- [static var permitLocalMouseEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitlocalmouseevents)
- [static var permitSystemDefinedEvents: CGEventFilterMask](/documentation/coregraphics/cgeventfiltermask/permitsystemdefinedevents)
- [CGEventFlags](/documentation/coregraphics/cgeventflags)

#### Constants

- [static var maskAlphaShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalphashift)
- [static var maskShift: CGEventFlags](/documentation/coregraphics/cgeventflags/maskshift)
- [static var maskControl: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcontrol)
- [static var maskAlternate: CGEventFlags](/documentation/coregraphics/cgeventflags/maskalternate)
- [static var maskCommand: CGEventFlags](/documentation/coregraphics/cgeventflags/maskcommand)
- [static var maskHelp: CGEventFlags](/documentation/coregraphics/cgeventflags/maskhelp)
- [static var maskSecondaryFn: CGEventFlags](/documentation/coregraphics/cgeventflags/masksecondaryfn)
- [static var maskNumericPad: CGEventFlags](/documentation/coregraphics/cgeventflags/masknumericpad)
- [static var maskNonCoalesced: CGEventFlags](/documentation/coregraphics/cgeventflags/masknoncoalesced)

#### Initializers

- [init(rawValue: UInt64)](/documentation/coregraphics/cgeventflags/init(rawvalue:))
- [CGEventMouseSubtype](/documentation/coregraphics/cgeventmousesubtype)

#### Constants

- [case defaultType](/documentation/coregraphics/cgeventmousesubtype/defaulttype)
- [case tabletPoint](/documentation/coregraphics/cgeventmousesubtype/tabletpoint)
- [case tabletProximity](/documentation/coregraphics/cgeventmousesubtype/tabletproximity)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventmousesubtype/init(rawvalue:))
- [CGEventSourceStateID](/documentation/coregraphics/cgeventsourcestateid)

#### Constants

- [case privateState](/documentation/coregraphics/cgeventsourcestateid/privatestate)
- [case combinedSessionState](/documentation/coregraphics/cgeventsourcestateid/combinedsessionstate)
- [case hidSystemState](/documentation/coregraphics/cgeventsourcestateid/hidsystemstate)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgeventsourcestateid/init(rawvalue:))
- [CGEventSuppressionState](/documentation/coregraphics/cgeventsuppressionstate)

#### Constants

- [case eventSuppressionStateSuppressionInterval](/documentation/coregraphics/cgeventsuppressionstate/eventsuppressionstatesuppressioninterval)
- [case eventSuppressionStateRemoteMouseDrag](/documentation/coregraphics/cgeventsuppressionstate/eventsuppressionstateremotemousedrag)
- [case numberOfEventSuppressionStates](/documentation/coregraphics/cgeventsuppressionstate/numberofeventsuppressionstates)

#### Enumeration Cases

- [case numberOfEventSuppressionStates](/documentation/coregraphics/cgeventsuppressionstate/numberofeventsuppressionstates)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventsuppressionstate/init(rawvalue:))
- [CGEventTapLocation](/documentation/coregraphics/cgeventtaplocation)

#### Constants

- [case cghidEventTap](/documentation/coregraphics/cgeventtaplocation/cghideventtap)
- [case cgSessionEventTap](/documentation/coregraphics/cgeventtaplocation/cgsessioneventtap)
- [case cgAnnotatedSessionEventTap](/documentation/coregraphics/cgeventtaplocation/cgannotatedsessioneventtap)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtaplocation/init(rawvalue:))
- [CGEventTapOptions](/documentation/coregraphics/cgeventtapoptions)

#### Constants

- [case defaultTap](/documentation/coregraphics/cgeventtapoptions/defaulttap)
- [case listenOnly](/documentation/coregraphics/cgeventtapoptions/listenonly)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtapoptions/init(rawvalue:))
- [CGEventTapPlacement](/documentation/coregraphics/cgeventtapplacement)

#### Constants

- [case headInsertEventTap](/documentation/coregraphics/cgeventtapplacement/headinserteventtap)
- [case tailAppendEventTap](/documentation/coregraphics/cgeventtapplacement/tailappendeventtap)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtapplacement/init(rawvalue:))
- [CGEventType](/documentation/coregraphics/cgeventtype)

#### Constants

- [case null](/documentation/coregraphics/cgeventtype/null)
- [case leftMouseDown](/documentation/coregraphics/cgeventtype/leftmousedown)
- [case leftMouseUp](/documentation/coregraphics/cgeventtype/leftmouseup)
- [case rightMouseDown](/documentation/coregraphics/cgeventtype/rightmousedown)
- [case rightMouseUp](/documentation/coregraphics/cgeventtype/rightmouseup)
- [case mouseMoved](/documentation/coregraphics/cgeventtype/mousemoved)
- [case leftMouseDragged](/documentation/coregraphics/cgeventtype/leftmousedragged)
- [case rightMouseDragged](/documentation/coregraphics/cgeventtype/rightmousedragged)
- [case keyDown](/documentation/coregraphics/cgeventtype/keydown)
- [case keyUp](/documentation/coregraphics/cgeventtype/keyup)
- [case flagsChanged](/documentation/coregraphics/cgeventtype/flagschanged)
- [case scrollWheel](/documentation/coregraphics/cgeventtype/scrollwheel)
- [case tabletPointer](/documentation/coregraphics/cgeventtype/tabletpointer)
- [case tabletProximity](/documentation/coregraphics/cgeventtype/tabletproximity)
- [case otherMouseDown](/documentation/coregraphics/cgeventtype/othermousedown)
- [case otherMouseUp](/documentation/coregraphics/cgeventtype/othermouseup)
- [case otherMouseDragged](/documentation/coregraphics/cgeventtype/othermousedragged)
- [case tapDisabledByTimeout](/documentation/coregraphics/cgeventtype/tapdisabledbytimeout)
- [case tapDisabledByUserInput](/documentation/coregraphics/cgeventtype/tapdisabledbyuserinput)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgeventtype/init(rawvalue:))
- [CGGesturePhase](/documentation/coregraphics/cggesturephase)

#### Constants

- [case began](/documentation/coregraphics/cggesturephase/began)
- [case cancelled](/documentation/coregraphics/cggesturephase/cancelled)
- [case changed](/documentation/coregraphics/cggesturephase/changed)
- [case ended](/documentation/coregraphics/cggesturephase/ended)
- [case mayBegin](/documentation/coregraphics/cggesturephase/maybegin)
- [case none](/documentation/coregraphics/cggesturephase/none)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cggesturephase/init(rawvalue:))
- [CGGlyphDeprecatedEnum](/documentation/coregraphics/cgglyphdeprecatedenum)

#### Constants

- [case max](/documentation/coregraphics/cgglyphdeprecatedenum/max)
- [case min](/documentation/coregraphics/cgglyphdeprecatedenum/min)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgglyphdeprecatedenum/init(rawvalue:))
- [CGImageByteOrderInfo](/documentation/coregraphics/cgimagebyteorderinfo)

#### Constants

- [case order16Big](/documentation/coregraphics/cgimagebyteorderinfo/order16big)
- [case order16Little](/documentation/coregraphics/cgimagebyteorderinfo/order16little)
- [case order32Big](/documentation/coregraphics/cgimagebyteorderinfo/order32big)
- [case order32Little](/documentation/coregraphics/cgimagebyteorderinfo/order32little)
- [case orderMask](/documentation/coregraphics/cgimagebyteorderinfo/ordermask)
- [case orderDefault](/documentation/coregraphics/cgimagebyteorderinfo/orderdefault)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgimagebyteorderinfo/init(rawvalue:))

#### Type Properties

- [static var order16Host: CGImageByteOrderInfo](/documentation/coregraphics/cgimagebyteorderinfo/order16host)
- [static var order32Host: CGImageByteOrderInfo](/documentation/coregraphics/cgimagebyteorderinfo/order32host)
- [CGMomentumScrollPhase](/documentation/coregraphics/cgmomentumscrollphase)

#### Constants

- [case begin](/documentation/coregraphics/cgmomentumscrollphase/begin)
- [case continuous](/documentation/coregraphics/cgmomentumscrollphase/continuous)
- [case end](/documentation/coregraphics/cgmomentumscrollphase/end)
- [case none](/documentation/coregraphics/cgmomentumscrollphase/none)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgmomentumscrollphase/init(rawvalue:))
- [CGMouseButton](/documentation/coregraphics/cgmousebutton)

#### Constants

- [case left](/documentation/coregraphics/cgmousebutton/left)
- [case right](/documentation/coregraphics/cgmousebutton/right)
- [case center](/documentation/coregraphics/cgmousebutton/center)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgmousebutton/init(rawvalue:))
- [CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation)

#### Constants

- [static var refresh: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/refresh)
- [static var move: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/move)
- [static var reducedDirtyRectangleCount: CGScreenUpdateOperation](/documentation/coregraphics/cgscreenupdateoperation/reduceddirtyrectanglecount)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgscreenupdateoperation/init(rawvalue:))
- [CGScrollEventUnit](/documentation/coregraphics/cgscrolleventunit)

#### Constants

- [case pixel](/documentation/coregraphics/cgscrolleventunit/pixel)
- [case line](/documentation/coregraphics/cgscrolleventunit/line)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgscrolleventunit/init(rawvalue:))
- [CGScrollPhase](/documentation/coregraphics/cgscrollphase)

#### Constants

- [case began](/documentation/coregraphics/cgscrollphase/began)
- [case cancelled](/documentation/coregraphics/cgscrollphase/cancelled)
- [case changed](/documentation/coregraphics/cgscrollphase/changed)
- [case ended](/documentation/coregraphics/cgscrollphase/ended)
- [case mayBegin](/documentation/coregraphics/cgscrollphase/maybegin)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgscrollphase/init(rawvalue:))
- [CGWindowBackingType](/documentation/coregraphics/cgwindowbackingtype)

#### Constants

- [case backingStoreBuffered](/documentation/coregraphics/cgwindowbackingtype/backingstorebuffered)
- [case backingStoreNonretained](/documentation/coregraphics/cgwindowbackingtype/backingstorenonretained)
- [case backingStoreRetained](/documentation/coregraphics/cgwindowbackingtype/backingstoreretained)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgwindowbackingtype/init(rawvalue:))
- [CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowimageoption/init(rawvalue:))

#### Type Properties

- [static var bestResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/bestresolution)
- [static var boundsIgnoreFraming: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/boundsignoreframing)
- [static var nominalResolution: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/nominalresolution)
- [static var onlyShadows: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/onlyshadows)
- [static var shouldBeOpaque: CGWindowImageOption](/documentation/coregraphics/cgwindowimageoption/shouldbeopaque)
- [CGWindowLevelKey](/documentation/coregraphics/cgwindowlevelkey)

#### Constants

- [case baseWindow](/documentation/coregraphics/cgwindowlevelkey/basewindow)
- [case minimumWindow](/documentation/coregraphics/cgwindowlevelkey/minimumwindow)
- [case desktopWindow](/documentation/coregraphics/cgwindowlevelkey/desktopwindow)
- [case backstopMenu](/documentation/coregraphics/cgwindowlevelkey/backstopmenu)
- [case normalWindow](/documentation/coregraphics/cgwindowlevelkey/normalwindow)
- [case floatingWindow](/documentation/coregraphics/cgwindowlevelkey/floatingwindow)
- [case tornOffMenuWindow](/documentation/coregraphics/cgwindowlevelkey/tornoffmenuwindow)
- [case dockWindow](/documentation/coregraphics/cgwindowlevelkey/dockwindow)
- [case mainMenuWindow](/documentation/coregraphics/cgwindowlevelkey/mainmenuwindow)
- [case statusWindow](/documentation/coregraphics/cgwindowlevelkey/statuswindow)
- [case modalPanelWindow](/documentation/coregraphics/cgwindowlevelkey/modalpanelwindow)
- [case popUpMenuWindow](/documentation/coregraphics/cgwindowlevelkey/popupmenuwindow)
- [case draggingWindow](/documentation/coregraphics/cgwindowlevelkey/draggingwindow)
- [case screenSaverWindow](/documentation/coregraphics/cgwindowlevelkey/screensaverwindow)
- [case maximumWindow](/documentation/coregraphics/cgwindowlevelkey/maximumwindow)
- [case overlayWindow](/documentation/coregraphics/cgwindowlevelkey/overlaywindow)
- [case helpWindow](/documentation/coregraphics/cgwindowlevelkey/helpwindow)
- [case utilityWindow](/documentation/coregraphics/cgwindowlevelkey/utilitywindow)
- [case desktopIconWindow](/documentation/coregraphics/cgwindowlevelkey/desktopiconwindow)
- [case cursorWindow](/documentation/coregraphics/cgwindowlevelkey/cursorwindow)
- [case assistiveTechHighWindow](/documentation/coregraphics/cgwindowlevelkey/assistivetechhighwindow)
- [case numberOfWindowLevelKeys](/documentation/coregraphics/cgwindowlevelkey/numberofwindowlevelkeys)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgwindowlevelkey/init(rawvalue:))
- [CGWindowListOption](/documentation/coregraphics/cgwindowlistoption)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgwindowlistoption/init(rawvalue:))

#### Type Properties

- [static var excludeDesktopElements: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/excludedesktopelements)
- [static var optionAll: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionall)
- [static var optionIncludingWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optionincludingwindow)
- [static var optionOnScreenAboveWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenabovewindow)
- [static var optionOnScreenBelowWindow: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenbelowwindow)
- [static var optionOnScreenOnly: CGWindowListOption](/documentation/coregraphics/cgwindowlistoption/optiononscreenonly)
- [CGWindowSharingType](/documentation/coregraphics/cgwindowsharingtype)

#### Constants

- [case none](/documentation/coregraphics/cgwindowsharingtype/none)
- [case readOnly](/documentation/coregraphics/cgwindowsharingtype/readonly)
- [case readWrite](/documentation/coregraphics/cgwindowsharingtype/readwrite)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgwindowsharingtype/init(rawvalue:))
- [CGImagePixelFormatInfo](/documentation/coregraphics/cgimagepixelformatinfo)

#### Enumeration Cases

- [case RGB101010](/documentation/coregraphics/cgimagepixelformatinfo/rgb101010)
- [case RGB555](/documentation/coregraphics/cgimagepixelformatinfo/rgb555)
- [case RGB565](/documentation/coregraphics/cgimagepixelformatinfo/rgb565)
- [case RGBCIF10](/documentation/coregraphics/cgimagepixelformatinfo/rgbcif10)
- [case mask](/documentation/coregraphics/cgimagepixelformatinfo/mask)
- [case packed](/documentation/coregraphics/cgimagepixelformatinfo/packed)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgimagepixelformatinfo/init(rawvalue:))
- [CGLineCap](/documentation/coregraphics/cglinecap)

#### Constants

- [case butt](/documentation/coregraphics/cglinecap/butt)
- [case round](/documentation/coregraphics/cglinecap/round)
- [case square](/documentation/coregraphics/cglinecap/square)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cglinecap/init(rawvalue:))
- [CGLineJoin](/documentation/coregraphics/cglinejoin)

#### Constants

- [case miter](/documentation/coregraphics/cglinejoin/miter)
- [case round](/documentation/coregraphics/cglinejoin/round)
- [case bevel](/documentation/coregraphics/cglinejoin/bevel)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cglinejoin/init(rawvalue:))
- [CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgpdfaccesspermissions/init(rawvalue:))

#### Type Properties

- [static var allowsCommenting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscommenting)
- [static var allowsContentAccessibility: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscontentaccessibility)
- [static var allowsContentCopying: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowscontentcopying)
- [static var allowsDocumentAssembly: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsdocumentassembly)
- [static var allowsDocumentChanges: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsdocumentchanges)
- [static var allowsFormFieldEntry: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowsformfieldentry)
- [static var allowsHighQualityPrinting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowshighqualityprinting)
- [static var allowsLowQualityPrinting: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfaccesspermissions/allowslowqualityprinting)
- [CGPDFTagType](/documentation/coregraphics/cgpdftagtype)

#### Enumeration Cases

- [case TOC](/documentation/coregraphics/cgpdftagtype/toc)
- [case TOCI](/documentation/coregraphics/cgpdftagtype/toci)
- [case annotation](/documentation/coregraphics/cgpdftagtype/annotation)
- [case art](/documentation/coregraphics/cgpdftagtype/art)
- [case bibliography](/documentation/coregraphics/cgpdftagtype/bibliography)
- [case blockQuote](/documentation/coregraphics/cgpdftagtype/blockquote)
- [case caption](/documentation/coregraphics/cgpdftagtype/caption)
- [case code](/documentation/coregraphics/cgpdftagtype/code)
- [case div](/documentation/coregraphics/cgpdftagtype/div)
- [case document](/documentation/coregraphics/cgpdftagtype/document)
- [case figure](/documentation/coregraphics/cgpdftagtype/figure)
- [case form](/documentation/coregraphics/cgpdftagtype/form)
- [case formula](/documentation/coregraphics/cgpdftagtype/formula)
- [case header](/documentation/coregraphics/cgpdftagtype/header)
- [case header1](/documentation/coregraphics/cgpdftagtype/header1)
- [case header2](/documentation/coregraphics/cgpdftagtype/header2)
- [case header3](/documentation/coregraphics/cgpdftagtype/header3)
- [case header4](/documentation/coregraphics/cgpdftagtype/header4)
- [case header5](/documentation/coregraphics/cgpdftagtype/header5)
- [case header6](/documentation/coregraphics/cgpdftagtype/header6)
- [case index](/documentation/coregraphics/cgpdftagtype/index)
- [case label](/documentation/coregraphics/cgpdftagtype/label)
- [case link](/documentation/coregraphics/cgpdftagtype/link)
- [case list](/documentation/coregraphics/cgpdftagtype/list)
- [case listBody](/documentation/coregraphics/cgpdftagtype/listbody)
- [case listItem](/documentation/coregraphics/cgpdftagtype/listitem)
- [case nonStructure](/documentation/coregraphics/cgpdftagtype/nonstructure)
- [case note](/documentation/coregraphics/cgpdftagtype/note)
- [case object](/documentation/coregraphics/cgpdftagtype/object)
- [case paragraph](/documentation/coregraphics/cgpdftagtype/paragraph)
- [case part](/documentation/coregraphics/cgpdftagtype/part)
- [case `private`](/documentation/coregraphics/cgpdftagtype/private)
- [case quote](/documentation/coregraphics/cgpdftagtype/quote)
- [case reference](/documentation/coregraphics/cgpdftagtype/reference)
- [case ruby](/documentation/coregraphics/cgpdftagtype/ruby)
- [case rubyAnnotationText](/documentation/coregraphics/cgpdftagtype/rubyannotationtext)
- [case rubyBaseText](/documentation/coregraphics/cgpdftagtype/rubybasetext)
- [case rubyPunctuation](/documentation/coregraphics/cgpdftagtype/rubypunctuation)
- [case section](/documentation/coregraphics/cgpdftagtype/section)
- [case span](/documentation/coregraphics/cgpdftagtype/span)
- [case table](/documentation/coregraphics/cgpdftagtype/table)
- [case tableBody](/documentation/coregraphics/cgpdftagtype/tablebody)
- [case tableDataCell](/documentation/coregraphics/cgpdftagtype/tabledatacell)
- [case tableFooter](/documentation/coregraphics/cgpdftagtype/tablefooter)
- [case tableHeader](/documentation/coregraphics/cgpdftagtype/tableheader)
- [case tableHeaderCell](/documentation/coregraphics/cgpdftagtype/tableheadercell)
- [case tableRow](/documentation/coregraphics/cgpdftagtype/tablerow)
- [case warichu](/documentation/coregraphics/cgpdftagtype/warichu)
- [case warichuPunctiation](/documentation/coregraphics/cgpdftagtype/warichupunctiation)
- [case warichuText](/documentation/coregraphics/cgpdftagtype/warichutext)

#### Instance Properties

- [var name: UnsafePointer<CChar>](/documentation/coregraphics/cgpdftagtype/name)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgpdftagtype/init(rawvalue:))
- [CGTextEncoding](/documentation/coregraphics/cgtextencoding)

#### Constants

- [case encodingFontSpecific](/documentation/coregraphics/cgtextencoding/encodingfontspecific)
- [case encodingMacRoman](/documentation/coregraphics/cgtextencoding/encodingmacroman)

#### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgtextencoding/init(rawvalue:))
- [CGToneMapping](/documentation/coregraphics/cgtonemapping)

#### Enumeration Cases

- [case `default`](/documentation/coregraphics/cgtonemapping/default)
- [case exrGamma](/documentation/coregraphics/cgtonemapping/exrgamma)
- [case imageSpecificLumaScaling](/documentation/coregraphics/cgtonemapping/imagespecificlumascaling)
- [case ituRecommended](/documentation/coregraphics/cgtonemapping/iturecommended)
- [case none](/documentation/coregraphics/cgtonemapping/none)
- [case referenceWhiteBased](/documentation/coregraphics/cgtonemapping/referencewhitebased)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgtonemapping/init(rawvalue:))
- [CGPathFillRule](/documentation/coregraphics/cgpathfillrule)

#### Enumeration Cases

- [case evenOdd](/documentation/coregraphics/cgpathfillrule/evenodd)
- [case winding](/documentation/coregraphics/cgpathfillrule/winding)
- [Core Graphics Constants](/documentation/coregraphics/core-graphics-constants)

### Constants

- [class let colorSpace: CFString](/documentation/coregraphics/cgdisplaystream/colorspace)
- [class let conversionBlackPointCompensation: CFString](/documentation/coregraphics/cgcolor/conversionblackpointcompensation)
- [var kCGDisplayBitsPerPixel: String](/documentation/coregraphics/kcgdisplaybitsperpixel)
- [var kCGDisplayBitsPerSample: String](/documentation/coregraphics/kcgdisplaybitspersample)
- [var kCGDisplayBlendNormal: Double](/documentation/coregraphics/kcgdisplayblendnormal)
- [var kCGDisplayBlendSolidColor: Double](/documentation/coregraphics/kcgdisplayblendsolidcolor)
- [var kCGDisplayBytesPerRow: String](/documentation/coregraphics/kcgdisplaybytesperrow)
- [var kCGDisplayFadeReservationInvalidToken: Int32](/documentation/coregraphics/kcgdisplayfadereservationinvalidtoken)
- [var kCGDisplayHeight: String](/documentation/coregraphics/kcgdisplayheight)
- [var kCGDisplayIOFlags: String](/documentation/coregraphics/kcgdisplayioflags)
- [var kCGDisplayMode: String](/documentation/coregraphics/kcgdisplaymode)
- [var kCGDisplayModeIsInterlaced: String](/documentation/coregraphics/kcgdisplaymodeisinterlaced)
- [var kCGDisplayModeIsSafeForHardware: String](/documentation/coregraphics/kcgdisplaymodeissafeforhardware)
- [var kCGDisplayModeIsStretched: String](/documentation/coregraphics/kcgdisplaymodeisstretched)
- [var kCGDisplayModeIsTelevisionOutput: String](/documentation/coregraphics/kcgdisplaymodeistelevisionoutput)
- [var kCGDisplayModeUsableForDesktopGUI: String](/documentation/coregraphics/kcgdisplaymodeusablefordesktopgui)
- [var kCGDisplayRefreshRate: String](/documentation/coregraphics/kcgdisplayrefreshrate)
- [var kCGDisplaySamplesPerPixel: String](/documentation/coregraphics/kcgdisplaysamplesperpixel)
- [let kCGDisplayShowDuplicateLowResolutionModes: CFString](/documentation/coregraphics/kcgdisplayshowduplicatelowresolutionmodes)
- [class let destinationRect: CFString](/documentation/coregraphics/cgdisplaystream/destinationrect)
- [class let minimumFrameTime: CFString](/documentation/coregraphics/cgdisplaystream/minimumframetime)
- [class let queueDepth: CFString](/documentation/coregraphics/cgdisplaystream/queuedepth)
- [class let showCursor: CFString](/documentation/coregraphics/cgdisplaystream/showcursor)
- [class let sourceRect: CFString](/documentation/coregraphics/cgdisplaystream/sourcerect)
- [class let yCbCrMatrix: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix)
- [class let yCbCrMatrix_ITU_R_601_4: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_601_4)
- [class let yCbCrMatrix_ITU_R_709_2: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_709_2)
- [class let yCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_smpte_240m_1995)
- [var kCGDisplayWidth: String](/documentation/coregraphics/kcgdisplaywidth)
- [let kCGFontIndexInvalid: CGFontIndex](/documentation/coregraphics/kcgfontindexinvalid)
- [let kCGFontIndexMax: CGFontIndex](/documentation/coregraphics/kcgfontindexmax)
- [let kCGGlyphMax: CGFontIndex](/documentation/coregraphics/kcgglyphmax)
- [var kCGIODisplayModeID: String](/documentation/coregraphics/kcgiodisplaymodeid)
- [var kCGMouseDownEventMaskingDeadSwitchTimeout: Double](/documentation/coregraphics/kcgmousedowneventmaskingdeadswitchtimeout)
- [var kCGNotifyEventTapAdded: String](/documentation/coregraphics/kcgnotifyeventtapadded)
- [var kCGNotifyEventTapRemoved: String](/documentation/coregraphics/kcgnotifyeventtapremoved)
- [var kCGNotifyGUIConsoleSessionChanged: String](/documentation/coregraphics/kcgnotifyguiconsolesessionchanged)
- [var kCGNotifyGUISessionUserChanged: String](/documentation/coregraphics/kcgnotifyguisessionuserchanged)
- [var kCGNumReservedWindowLevels: Int32](/documentation/coregraphics/kcgnumreservedwindowlevels)
- [var kCGSessionConsoleSetKey: String](/documentation/coregraphics/kcgsessionconsolesetkey)
- [var kCGSessionLoginDoneKey: String](/documentation/coregraphics/kcgsessionlogindonekey)
- [var kCGSessionOnConsoleKey: String](/documentation/coregraphics/kcgsessiononconsolekey)
- [var kCGSessionUserIDKey: String](/documentation/coregraphics/kcgsessionuseridkey)
- [var kCGSessionUserNameKey: String](/documentation/coregraphics/kcgsessionusernamekey)
- [let kCGWindowAlpha: CFString](/documentation/coregraphics/kcgwindowalpha)
- [let kCGWindowBackingLocationVideoMemory: CFString](/documentation/coregraphics/kcgwindowbackinglocationvideomemory)
- [let kCGWindowBounds: CFString](/documentation/coregraphics/kcgwindowbounds)
- [let kCGWindowIsOnscreen: CFString](/documentation/coregraphics/kcgwindowisonscreen)
- [let kCGWindowLayer: CFString](/documentation/coregraphics/kcgwindowlayer)
- [let kCGWindowMemoryUsage: CFString](/documentation/coregraphics/kcgwindowmemoryusage)
- [let kCGWindowName: CFString](/documentation/coregraphics/kcgwindowname)
- [let kCGWindowNumber: CFString](/documentation/coregraphics/kcgwindownumber)
- [let kCGWindowOwnerName: CFString](/documentation/coregraphics/kcgwindowownername)
- [let kCGWindowOwnerPID: CFString](/documentation/coregraphics/kcgwindowownerpid)
- [let kCGWindowSharingState: CFString](/documentation/coregraphics/kcgwindowsharingstate)
- [let kCGWindowStoreType: CFString](/documentation/coregraphics/kcgwindowstoretype)
- [let CGPointZero: CGPoint](/documentation/coregraphics/cgpointzero)
- [let CGRectZero: CGRect](/documentation/coregraphics/cgrectzero)
- [let CGSizeZero: CGSize](/documentation/coregraphics/cgsizezero)
- [let kCGWindowWorkspace: CFString](/documentation/coregraphics/kcgwindowworkspace)
- [class let preserveAspectRatio: CFString](/documentation/coregraphics/cgdisplaystream/preserveaspectratio)
- [var CG_HDR_BT_2100: Int32](/documentation/coregraphics/cg_hdr_bt_2100)
- [let kCGBitmapByteOrder16Host: CGBitmapInfo](/documentation/coregraphics/kcgbitmapbyteorder16host)
- [let kCGBitmapByteOrder32Host: CGBitmapInfo](/documentation/coregraphics/kcgbitmapbyteorder32host)
- [let kCGColorSpaceExtendedRange: CFString](/documentation/coregraphics/kcgcolorspaceextendedrange)
- [var kCGDefaultHDRImageContentHeadroom: Float](/documentation/coregraphics/kcgdefaulthdrimagecontentheadroom)
- [let kCGEXRToneMappingGammaDefog: CFString](/documentation/coregraphics/kcgexrtonemappinggammadefog)
- [let kCGEXRToneMappingGammaExposure: CFString](/documentation/coregraphics/kcgexrtonemappinggammaexposure)
- [let kCGEXRToneMappingGammaKneeHigh: CFString](/documentation/coregraphics/kcgexrtonemappinggammakneehigh)
- [let kCGEXRToneMappingGammaKneeLow: CFString](/documentation/coregraphics/kcgexrtonemappinggammakneelow)
- [var kCGNullDirectDisplay: CGDirectDisplayID](/documentation/coregraphics/kcgnulldirectdisplay)
- [var kCGNullWindowID: CGWindowID](/documentation/coregraphics/kcgnullwindowid)
- [var kCGNumReservedBaseWindowLevels: Int32](/documentation/coregraphics/kcgnumreservedbasewindowlevels)
- [let kCGPDFContextAccessPermissions: CFString](/documentation/coregraphics/kcgpdfcontextaccesspermissions)
- [let kCGPDFContextCreateLinearizedPDF: CFString](/documentation/coregraphics/kcgpdfcontextcreatelinearizedpdf)
- [let kCGPDFContextCreatePDFA: CFString](/documentation/coregraphics/kcgpdfcontextcreatepdfa)
- [let kCGPDFOutlineChildren: CFString](/documentation/coregraphics/kcgpdfoutlinechildren)
- [let kCGPDFOutlineDestination: CFString](/documentation/coregraphics/kcgpdfoutlinedestination)
- [let kCGPDFOutlineDestinationRect: CFString](/documentation/coregraphics/kcgpdfoutlinedestinationrect)
- [let kCGPDFOutlineTitle: CFString](/documentation/coregraphics/kcgpdfoutlinetitle)
- [let kCGSkipBoostToHDR: CFString](/documentation/coregraphics/kcgskipboosttohdr)
- [let kCGUse100nitsHLGOOTF: CFString](/documentation/coregraphics/kcguse100nitshlgootf)
- [let kCGUseBT1886ForCoreVideoGamma: CFString](/documentation/coregraphics/kcgusebt1886forcorevideogamma)
- [let kCGUseLegacyHDREcosystem: CFString](/documentation/coregraphics/kcguselegacyhdrecosystem)
- [var kCGAssistiveTechHighWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgassistivetechhighwindowlevel)
- [var kCGBackstopMenuLevel: CGWindowLevel](/documentation/coregraphics/kcgbackstopmenulevel)
- [var kCGDockWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgdockwindowlevel)
- [var kCGDraggingWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgdraggingwindowlevel)
- [var kCGFloatingWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgfloatingwindowlevel)
- [var kCGHelpWindowLevel: CGWindowLevel](/documentation/coregraphics/kcghelpwindowlevel)
- [var kCGMainMenuWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgmainmenuwindowlevel)
- [var kCGModalPanelWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgmodalpanelwindowlevel)
- [var kCGNormalWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgnormalwindowlevel)
- [var kCGOverlayWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgoverlaywindowlevel)
- [var kCGPopUpMenuWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgpopupmenuwindowlevel)
- [var kCGScreenSaverWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgscreensaverwindowlevel)
- [var kCGStatusWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgstatuswindowlevel)
- [var kCGTornOffMenuWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgtornoffmenuwindowlevel)
- [var kCGUtilityWindowLevel: CGWindowLevel](/documentation/coregraphics/kcgutilitywindowlevel)
- [Core Graphics Functions](/documentation/coregraphics/core-graphics-functions)

### Functions

- [func CGAcquireDisplayFadeReservation(CGDisplayReservationInterval, UnsafeMutablePointer<CGDisplayFadeReservationToken>?) -> CGError](/documentation/coregraphics/cgacquiredisplayfadereservation(_:_:))
- [func CGAssociateMouseAndMouseCursorPosition(boolean_t) -> CGError](/documentation/coregraphics/cgassociatemouseandmousecursorposition(_:))
- [func CGBeginDisplayConfiguration(UnsafeMutablePointer<CGDisplayConfigRef?>?) -> CGError](/documentation/coregraphics/cgbegindisplayconfiguration(_:))
- [func CGCancelDisplayConfiguration(CGDisplayConfigRef?) -> CGError](/documentation/coregraphics/cgcanceldisplayconfiguration(_:))
- [func CGCaptureAllDisplays() -> CGError](/documentation/coregraphics/cgcapturealldisplays())
- [func CGCaptureAllDisplaysWithOptions(CGCaptureOptions) -> CGError](/documentation/coregraphics/cgcapturealldisplayswithoptions(_:))
- [func CGCompleteDisplayConfiguration(CGDisplayConfigRef?, CGConfigureOption) -> CGError](/documentation/coregraphics/cgcompletedisplayconfiguration(_:_:))
- [func CGConfigureDisplayFadeEffect(CGDisplayConfigRef?, CGDisplayFadeInterval, CGDisplayFadeInterval, Float, Float, Float) -> CGError](/documentation/coregraphics/cgconfiguredisplayfadeeffect(_:_:_:_:_:_:))
- [func CGConfigureDisplayMirrorOfDisplay(CGDisplayConfigRef?, CGDirectDisplayID, CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgconfiguredisplaymirrorofdisplay(_:_:_:))
- [func CGConfigureDisplayMode(CGDisplayConfigRef?, CGDirectDisplayID, CFDictionary?) -> CGError](/documentation/coregraphics/cgconfiguredisplaymode(_:_:_:))
- [func CGConfigureDisplayOrigin(CGDisplayConfigRef?, CGDirectDisplayID, Int32, Int32) -> CGError](/documentation/coregraphics/cgconfiguredisplayorigin(_:_:_:_:))
- [func CGConfigureDisplayStereoOperation(CGDisplayConfigRef?, CGDirectDisplayID, boolean_t, boolean_t) -> CGError](/documentation/coregraphics/cgconfiguredisplaystereooperation(_:_:_:_:))
- [func CGConfigureDisplayWithDisplayMode(CGDisplayConfigRef?, CGDirectDisplayID, CGDisplayMode?, CFDictionary?) -> CGError](/documentation/coregraphics/cgconfiguredisplaywithdisplaymode(_:_:_:_:))
- [func CGCursorIsDrawnInFramebuffer() -> boolean_t](/documentation/coregraphics/cgcursorisdrawninframebuffer())
- [func CGCursorIsVisible() -> boolean_t](/documentation/coregraphics/cgcursorisvisible())
- [func CGDirectDisplayCopyCurrentMetalDevice(CGDirectDisplayID) -> (any MTLDevice)?](/documentation/coregraphics/cgdirectdisplaycopycurrentmetaldevice(_:))
- [func CGDisplayAvailableModes(CGDirectDisplayID) -> CFArray?](/documentation/coregraphics/cgdisplayavailablemodes(_:))
- [func CGDisplayBestModeForParameters(CGDirectDisplayID, Int, Int, Int, UnsafeMutablePointer<boolean_t>?) -> CFDictionary?](/documentation/coregraphics/cgdisplaybestmodeforparameters(_:_:_:_:_:))
- [func CGDisplayBestModeForParametersAndRefreshRate(CGDirectDisplayID, Int, Int, Int, CGRefreshRate, UnsafeMutablePointer<boolean_t>?) -> CFDictionary?](/documentation/coregraphics/cgdisplaybestmodeforparametersandrefreshrate(_:_:_:_:_:_:))
- [func CGDisplayBounds(CGDirectDisplayID) -> CGRect](/documentation/coregraphics/cgdisplaybounds(_:))
- [func CGDisplayCapture(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplaycapture(_:))
- [func CGDisplayCaptureWithOptions(CGDirectDisplayID, CGCaptureOptions) -> CGError](/documentation/coregraphics/cgdisplaycapturewithoptions(_:_:))
- [func CGDisplayCopyAllDisplayModes(CGDirectDisplayID, CFDictionary?) -> CFArray?](/documentation/coregraphics/cgdisplaycopyalldisplaymodes(_:_:))
- [func CGDisplayCopyColorSpace(CGDirectDisplayID) -> CGColorSpace](/documentation/coregraphics/cgdisplaycopycolorspace(_:))
- [func CGDisplayCopyDisplayMode(CGDirectDisplayID) -> CGDisplayMode?](/documentation/coregraphics/cgdisplaycopydisplaymode(_:))
- [func CGDisplayCreateImage(CGDirectDisplayID) -> CGImage?](/documentation/coregraphics/cgdisplaycreateimage(_:))
- [func CGDisplayCreateImage(CGDirectDisplayID, rect: CGRect) -> CGImage?](/documentation/coregraphics/cgdisplaycreateimage(_:rect:))
- [func CGDisplayCurrentMode(CGDirectDisplayID) -> CFDictionary?](/documentation/coregraphics/cgdisplaycurrentmode(_:))
- [func CGDisplayFade(CGDisplayFadeReservationToken, CGDisplayFadeInterval, CGDisplayBlendFraction, CGDisplayBlendFraction, Float, Float, Float, boolean_t) -> CGError](/documentation/coregraphics/cgdisplayfade(_:_:_:_:_:_:_:_:))
- [func CGDisplayFadeOperationInProgress() -> boolean_t](/documentation/coregraphics/cgdisplayfadeoperationinprogress())
- [func CGDisplayGammaTableCapacity(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplaygammatablecapacity(_:))
- [func CGDisplayGetDrawingContext(CGDirectDisplayID) -> CGContext?](/documentation/coregraphics/cgdisplaygetdrawingcontext(_:))
- [func CGDisplayHideCursor(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayhidecursor(_:))
- [func CGDisplayIDToOpenGLDisplayMask(CGDirectDisplayID) -> CGOpenGLDisplayMask](/documentation/coregraphics/cgdisplayidtoopengldisplaymask(_:))
- [func CGDisplayIOServicePort(CGDirectDisplayID) -> io_service_t](/documentation/coregraphics/cgdisplayioserviceport(_:))
- [func CGDisplayIsActive(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisactive(_:))
- [func CGDisplayIsAlwaysInMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisalwaysinmirrorset(_:))
- [func CGDisplayIsAsleep(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisasleep(_:))
- [func CGDisplayIsBuiltin(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisbuiltin(_:))
- [func CGDisplayIsCaptured(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayiscaptured(_:))
- [func CGDisplayIsInHWMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisinhwmirrorset(_:))
- [func CGDisplayIsInMirrorSet(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisinmirrorset(_:))
- [func CGDisplayIsMain(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayismain(_:))
- [func CGDisplayIsOnline(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisonline(_:))
- [func CGDisplayIsStereo(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayisstereo(_:))
- [func CGDisplayMirrorsDisplay(CGDirectDisplayID) -> CGDirectDisplayID](/documentation/coregraphics/cgdisplaymirrorsdisplay(_:))
- [var pixelEncoding: CFString?](/documentation/coregraphics/cgdisplaymode/pixelencoding)
- [var height: Int](/documentation/coregraphics/cgdisplaymode/height)
- [var ioDisplayModeID: Int32](/documentation/coregraphics/cgdisplaymode/iodisplaymodeid)
- [var ioFlags: UInt32](/documentation/coregraphics/cgdisplaymode/ioflags)
- [var pixelWidth: Int](/documentation/coregraphics/cgdisplaymode/pixelwidth)
- [var refreshRate: Double](/documentation/coregraphics/cgdisplaymode/refreshrate)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaymode/typeid)
- [var width: Int](/documentation/coregraphics/cgdisplaymode/width)
- [func isUsableForDesktopGUI() -> Bool](/documentation/coregraphics/cgdisplaymode/isusablefordesktopgui())
- [func CGDisplayModelNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplaymodelnumber(_:))
- [func CGDisplayMoveCursorToPoint(CGDirectDisplayID, CGPoint) -> CGError](/documentation/coregraphics/cgdisplaymovecursortopoint(_:_:))
- [func CGDisplayPixelsHigh(CGDirectDisplayID) -> Int](/documentation/coregraphics/cgdisplaypixelshigh(_:))
- [func CGDisplayPixelsWide(CGDirectDisplayID) -> Int](/documentation/coregraphics/cgdisplaypixelswide(_:))
- [func CGDisplayPrimaryDisplay(CGDirectDisplayID) -> CGDirectDisplayID](/documentation/coregraphics/cgdisplayprimarydisplay(_:))
- [func CGDisplayRegisterReconfigurationCallback(CGDisplayReconfigurationCallBack?, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgdisplayregisterreconfigurationcallback(_:_:))
- [func CGDisplayRelease(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayrelease(_:))
- [func CGDisplayRemoveReconfigurationCallback(CGDisplayReconfigurationCallBack?, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgdisplayremovereconfigurationcallback(_:_:))
- [func CGDisplayRestoreColorSyncSettings()](/documentation/coregraphics/cgdisplayrestorecolorsyncsettings())
- [func CGDisplayRotation(CGDirectDisplayID) -> Double](/documentation/coregraphics/cgdisplayrotation(_:))
- [func CGDisplayScreenSize(CGDirectDisplayID) -> CGSize](/documentation/coregraphics/cgdisplayscreensize(_:))
- [func CGDisplaySerialNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayserialnumber(_:))
- [func CGDisplaySetDisplayMode(CGDirectDisplayID, CGDisplayMode?, CFDictionary?) -> CGError](/documentation/coregraphics/cgdisplaysetdisplaymode(_:_:_:))
- [func CGDisplaySetStereoOperation(CGDirectDisplayID, boolean_t, boolean_t, CGConfigureOption) -> CGError](/documentation/coregraphics/cgdisplaysetstereooperation(_:_:_:_:))
- [func CGDisplayShowCursor(CGDirectDisplayID) -> CGError](/documentation/coregraphics/cgdisplayshowcursor(_:))
- [init?(display: CGDirectDisplayID, outputWidth: Int, outputHeight: Int, pixelFormat: Int32, properties: CFDictionary?, handler: CGDisplayStreamFrameAvailableHandler?)](/documentation/coregraphics/cgdisplaystream/init(display:outputwidth:outputheight:pixelformat:properties:handler:))
- [init?(dispatchQueueDisplay: CGDirectDisplayID, outputWidth: Int, outputHeight: Int, pixelFormat: Int32, properties: CFDictionary?, queue: dispatch_queue_t, handler: CGDisplayStreamFrameAvailableHandler?)](/documentation/coregraphics/cgdisplaystream/init(dispatchqueuedisplay:outputwidth:outputheight:pixelformat:properties:queue:handler:))
- [var runLoopSource: CFRunLoopSource?](/documentation/coregraphics/cgdisplaystream/runloopsource)
- [func start() -> CGError](/documentation/coregraphics/cgdisplaystream/start())
- [func stop() -> CGError](/documentation/coregraphics/cgdisplaystream/stop())
- [init?(mergedUpdateFirstUpdate: CGDisplayStreamUpdate?, secondUpdate: CGDisplayStreamUpdate?)](/documentation/coregraphics/cgdisplaystreamupdate/init(mergedupdatefirstupdate:secondupdate:))
- [var dropCount: Int](/documentation/coregraphics/cgdisplaystreamupdate/dropcount)
- [func getMovedRectsDelta(dx: UnsafeMutablePointer<CGFloat>, dy: UnsafeMutablePointer<CGFloat>)](/documentation/coregraphics/cgdisplaystreamupdate/getmovedrectsdelta(dx:dy:))
- [func getRects(CGDisplayStreamUpdateRectType, rectCount: UnsafeMutablePointer<Int>) -> UnsafePointer<CGRect>?](/documentation/coregraphics/cgdisplaystreamupdate/getrects(_:rectcount:))
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaystreamupdate/typeid)
- [func CGDisplaySwitchToMode(CGDirectDisplayID, CFDictionary?) -> CGError](/documentation/coregraphics/cgdisplayswitchtomode(_:_:))
- [func CGDisplayUnitNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayunitnumber(_:))
- [func CGDisplayUsesOpenGLAcceleration(CGDirectDisplayID) -> boolean_t](/documentation/coregraphics/cgdisplayusesopenglacceleration(_:))
- [func CGDisplayVendorNumber(CGDirectDisplayID) -> UInt32](/documentation/coregraphics/cgdisplayvendornumber(_:))
- [func CGEnableEventStateCombining(boolean_t) -> CGError](/documentation/coregraphics/cgenableeventstatecombining(_:))
- [init?(source: CGEventSource?)](/documentation/coregraphics/cgevent/init(source:))
- [func copy() -> CGEvent?](/documentation/coregraphics/cgevent/copy())
- [init?(withDataAllocator: CFAllocator?, data: CFData?)](/documentation/coregraphics/cgevent/init(withdataallocator:data:))
- [init?(keyboardEventSource: CGEventSource?, virtualKey: CGKeyCode, keyDown: Bool)](/documentation/coregraphics/cgevent/init(keyboardeventsource:virtualkey:keydown:))
- [init?(mouseEventSource: CGEventSource?, mouseType: CGEventType, mouseCursorPosition: CGPoint, mouseButton: CGMouseButton)](/documentation/coregraphics/cgevent/init(mouseeventsource:mousetype:mousecursorposition:mousebutton:))
- [init?(event: CGEvent?)](/documentation/coregraphics/cgeventsource/init(event:))
- [func getDoubleValueField(CGEventField) -> Double](/documentation/coregraphics/cgevent/getdoublevaluefield(_:))
- [var flags: CGEventFlags](/documentation/coregraphics/cgevent/flags)
- [func getIntegerValueField(CGEventField) -> Int64](/documentation/coregraphics/cgevent/getintegervaluefield(_:))
- [var location: CGPoint](/documentation/coregraphics/cgevent/location)
- [var timestamp: CGEventTimestamp](/documentation/coregraphics/cgevent/timestamp)
- [var type: CGEventType](/documentation/coregraphics/cgevent/type)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgevent/typeid)
- [var unflippedLocation: CGPoint](/documentation/coregraphics/cgevent/unflippedlocation)
- [func keyboardGetUnicodeString(maxStringLength: Int, actualStringLength: UnsafeMutablePointer<Int>?, unicodeString: UnsafeMutablePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardgetunicodestring(maxstringlength:actualstringlength:unicodestring:))
- [func keyboardSetUnicodeString(stringLength: Int, unicodeString: UnsafePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardsetunicodestring(stringlength:unicodestring:))
- [func post(tap: CGEventTapLocation)](/documentation/coregraphics/cgevent/post(tap:))
- [func postToPSN(processSerialNumber: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgevent/posttopsn(processserialnumber:))
- [func postToPid(pid_t)](/documentation/coregraphics/cgevent/posttopid(_:))
- [func setDoubleValueField(CGEventField, value: Double)](/documentation/coregraphics/cgevent/setdoublevaluefield(_:value:))
- [func setIntegerValueField(CGEventField, value: Int64)](/documentation/coregraphics/cgevent/setintegervaluefield(_:value:))
- [func setSource(CGEventSource?)](/documentation/coregraphics/cgevent/setsource(_:))
- [class func buttonState(CGEventSourceStateID, button: CGMouseButton) -> Bool](/documentation/coregraphics/cgeventsource/buttonstate(_:button:))
- [class func counterForEventType(CGEventSourceStateID, eventType: CGEventType) -> UInt32](/documentation/coregraphics/cgeventsource/counterforeventtype(_:eventtype:))
- [init?(stateID: CGEventSourceStateID)](/documentation/coregraphics/cgeventsource/init(stateid:))
- [class func flagsState(CGEventSourceStateID) -> CGEventFlags](/documentation/coregraphics/cgeventsource/flagsstate(_:))
- [var keyboardType: CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsource/keyboardtype)
- [func getLocalEventsFilterDuringSuppressionState(CGEventSuppressionState) -> CGEventFilterMask](/documentation/coregraphics/cgeventsource/getlocaleventsfilterduringsuppressionstate(_:))
- [var pixelsPerLine: Double](/documentation/coregraphics/cgeventsource/pixelsperline)
- [var sourceStateID: CGEventSourceStateID](/documentation/coregraphics/cgeventsource/sourcestateid)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgeventsource/typeid)
- [var userData: Int64](/documentation/coregraphics/cgeventsource/userdata)
- [class func keyState(CGEventSourceStateID, key: CGKeyCode) -> Bool](/documentation/coregraphics/cgeventsource/keystate(_:key:))
- [class func secondsSinceLastEventType(CGEventSourceStateID, eventType: CGEventType) -> CFTimeInterval](/documentation/coregraphics/cgeventsource/secondssincelasteventtype(_:eventtype:))
- [func setLocalEventsFilterDuringSuppressionState(CGEventFilterMask, state: CGEventSuppressionState)](/documentation/coregraphics/cgeventsource/setlocaleventsfilterduringsuppressionstate(_:state:))
- [class func tapCreate(tap: CGEventTapLocation, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreate(tap:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPSN(processSerialNumber: UnsafeMutableRawPointer, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpsn(processserialnumber:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPid(pid: pid_t, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpid(pid:place:options:eventsofinterest:callback:userinfo:))
- [class func tapEnable(tap: CFMachPort, enable: Bool)](/documentation/coregraphics/cgevent/tapenable(tap:enable:))
- [class func tapIsEnabled(tap: CFMachPort) -> Bool](/documentation/coregraphics/cgevent/tapisenabled(tap:))
- [func tapPostEvent(CGEventTapProxy?)](/documentation/coregraphics/cgevent/tappostevent(_:))
- [func CGGetActiveDisplayList(UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetactivedisplaylist(_:_:_:))
- [func CGGetDisplayTransferByFormula(CGDirectDisplayID, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?) -> CGError](/documentation/coregraphics/cggetdisplaytransferbyformula(_:_:_:_:_:_:_:_:_:_:))
- [func CGGetDisplayTransferByTable(CGDirectDisplayID, UInt32, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<CGGammaValue>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplaytransferbytable(_:_:_:_:_:_:))
- [func CGGetDisplaysWithOpenGLDisplayMask(CGOpenGLDisplayMask, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithopengldisplaymask(_:_:_:_:))
- [func CGGetDisplaysWithPoint(CGPoint, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithpoint(_:_:_:_:))
- [func CGGetDisplaysWithRect(CGRect, UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetdisplayswithrect(_:_:_:_:))
- [func CGGetEventTapList(UInt32, UnsafeMutablePointer<CGEventTapInformation>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggeteventtaplist(_:_:_:))
- [func CGGetLastMouseDelta() -> (x: Int32, y: Int32)](/documentation/coregraphics/cggetlastmousedelta())
- [func CGGetOnlineDisplayList(UInt32, UnsafeMutablePointer<CGDirectDisplayID>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cggetonlinedisplaylist(_:_:_:))
- [var utType: CFString?](/documentation/coregraphics/cgimage/uttype)
- [func CGInhibitLocalEvents(boolean_t) -> CGError](/documentation/coregraphics/cginhibitlocalevents(_:))
- [func CGMainDisplayID() -> CGDirectDisplayID](/documentation/coregraphics/cgmaindisplayid())
- [func CGOpenGLDisplayMaskToDisplayID(CGOpenGLDisplayMask) -> CGDirectDisplayID](/documentation/coregraphics/cgopengldisplaymasktodisplayid(_:))
- [func CGPointEqualToPoint(CGPoint, CGPoint) -> Bool](/documentation/coregraphics/cgpointequaltopoint(_:_:))
- [func CGPostKeyboardEvent(CGCharCode, CGKeyCode, boolean_t) -> CGError](/documentation/coregraphics/cgpostkeyboardevent(_:_:_:))
- [func CGRegisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgregisterscreenrefreshcallback(_:_:))
- [func CGReleaseAllDisplays() -> CGError](/documentation/coregraphics/cgreleasealldisplays())
- [func CGReleaseDisplayFadeReservation(CGDisplayFadeReservationToken) -> CGError](/documentation/coregraphics/cgreleasedisplayfadereservation(_:))
- [func CGReleaseScreenRefreshRects(UnsafeMutablePointer<CGRect>?)](/documentation/coregraphics/cgreleasescreenrefreshrects(_:))
- [func CGRestorePermanentDisplayConfiguration()](/documentation/coregraphics/cgrestorepermanentdisplayconfiguration())
- [func CGScreenRegisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgscreenregistermovecallback(_:_:))
- [func CGScreenUnregisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgscreenunregistermovecallback(_:_:))
- [func CGSessionCopyCurrentDictionary() -> CFDictionary?](/documentation/coregraphics/cgsessioncopycurrentdictionary())
- [func CGSetDisplayTransferByByteTable(CGDirectDisplayID, UInt32, UnsafePointer<UInt8>, UnsafePointer<UInt8>, UnsafePointer<UInt8>) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbybytetable(_:_:_:_:_:))
- [func CGSetDisplayTransferByFormula(CGDirectDisplayID, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue, CGGammaValue) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbyformula(_:_:_:_:_:_:_:_:_:_:))
- [func CGSetDisplayTransferByTable(CGDirectDisplayID, UInt32, UnsafePointer<CGGammaValue>?, UnsafePointer<CGGammaValue>?, UnsafePointer<CGGammaValue>?) -> CGError](/documentation/coregraphics/cgsetdisplaytransferbytable(_:_:_:_:_:))
- [func CGSetLocalEventsFilterDuringSuppressionState(CGEventFilterMask, CGEventSuppressionState) -> CGError](/documentation/coregraphics/cgsetlocaleventsfilterduringsuppressionstate(_:_:))
- [func CGSetLocalEventsSuppressionInterval(CFTimeInterval) -> CGError](/documentation/coregraphics/cgsetlocaleventssuppressioninterval(_:))
- [func CGShieldingWindowID(CGDirectDisplayID) -> CGWindowID](/documentation/coregraphics/cgshieldingwindowid(_:))
- [func CGShieldingWindowLevel() -> CGWindowLevel](/documentation/coregraphics/cgshieldingwindowlevel())
- [func CGSizeEqualToSize(CGSize, CGSize) -> Bool](/documentation/coregraphics/cgsizeequaltosize(_:_:))
- [func CGUnregisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgunregisterscreenrefreshcallback(_:_:))
- [func CGWaitForScreenRefreshRects(UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cgwaitforscreenrefreshrects(_:_:))
- [func CGWaitForScreenUpdateRects(CGScreenUpdateOperation, UnsafeMutablePointer<CGScreenUpdateOperation>?, UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<CGScreenUpdateMoveDelta>?) -> CGError](/documentation/coregraphics/cgwaitforscreenupdaterects(_:_:_:_:_:))
- [func CGWarpMouseCursorPosition(CGPoint) -> CGError](/documentation/coregraphics/cgwarpmousecursorposition(_:))
- [func CGWindowLevelForKey(CGWindowLevelKey) -> CGWindowLevel](/documentation/coregraphics/cgwindowlevelforkey(_:))
- [func CGWindowListCopyWindowInfo(CGWindowListOption, CGWindowID) -> CFArray?](/documentation/coregraphics/cgwindowlistcopywindowinfo(_:_:))
- [func CGWindowListCreateDescriptionFromArray(CFArray?) -> CFArray?](/documentation/coregraphics/cgwindowlistcreatedescriptionfromarray(_:))
- [func CGWindowListCreateImage(CGRect, CGWindowListOption, CGWindowID, CGWindowImageOption) -> CGImage?](/documentation/coregraphics/cgwindowlistcreateimage(_:_:_:_:))
- [init?(windowListFromArrayScreenBounds: CGRect, windowArray: CFArray, imageOption: CGWindowImageOption)](/documentation/coregraphics/cgimage/init(windowlistfromarrayscreenbounds:windowarray:imageoption:))
- [func CGWindowServerCFMachPort() -> CFMachPort?](/documentation/coregraphics/cgwindowservercfmachport())
- [func CGWindowServerCreateServerPort() -> CFMachPort?](/documentation/coregraphics/cgwindowservercreateserverport())
- [func acos(CGFloat) -> CGFloat](/documentation/coregraphics/acos(_:))
- [func acosh(CGFloat) -> CGFloat](/documentation/coregraphics/acosh(_:))
- [func asin(CGFloat) -> CGFloat](/documentation/coregraphics/asin(_:))
- [func asinh(CGFloat) -> CGFloat](/documentation/coregraphics/asinh(_:))
- [func atan(CGFloat) -> CGFloat](/documentation/coregraphics/atan(_:))
- [func atan2(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/atan2(_:_:))
- [func atanh(CGFloat) -> CGFloat](/documentation/coregraphics/atanh(_:))
- [func cbrt(CGFloat) -> CGFloat](/documentation/coregraphics/cbrt(_:))
- [func copysign(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/copysign(_:_:))
- [func cos(CGFloat) -> CGFloat](/documentation/coregraphics/cos(_:))
- [func cosh(CGFloat) -> CGFloat](/documentation/coregraphics/cosh(_:))
- [func erf(CGFloat) -> CGFloat](/documentation/coregraphics/erf(_:))
- [func erfc(CGFloat) -> CGFloat](/documentation/coregraphics/erfc(_:))
- [func exp(CGFloat) -> CGFloat](/documentation/coregraphics/exp(_:))
- [func exp2(CGFloat) -> CGFloat](/documentation/coregraphics/exp2(_:))
- [func expm1(CGFloat) -> CGFloat](/documentation/coregraphics/expm1(_:))
- [func fdim(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/fdim(_:_:))
- [func fmax(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/fmax(_:_:))
- [func fmin(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/fmin(_:_:))
- [func hypot(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/hypot(_:_:))
- [func ilogb(CGFloat) -> Int](/documentation/coregraphics/ilogb(_:))
- [func CGColorSpaceCreateLinearized(CGColorSpace) -> CGColorSpace?](/documentation/coregraphics/cgcolorspacecreatelinearized(_:))
- [init?(src: CGColorSpace, dst: CGColorSpace)](/documentation/coregraphics/cgcolorconversioninfo/init(src:dst:))
- [func j0(CGFloat) -> CGFloat](/documentation/coregraphics/j0(_:))
- [func j1(CGFloat) -> CGFloat](/documentation/coregraphics/j1(_:))
- [func jn(Int, CGFloat) -> CGFloat](/documentation/coregraphics/jn(_:_:))
- [func ldexp(CGFloat, Int) -> CGFloat](/documentation/coregraphics/ldexp(_:_:))
- [func lgamma(CGFloat) -> (CGFloat, Int)](/documentation/coregraphics/lgamma(_:))
- [func log(CGFloat) -> CGFloat](/documentation/coregraphics/log(_:))
- [func log10(CGFloat) -> CGFloat](/documentation/coregraphics/log10(_:))
- [func log1p(CGFloat) -> CGFloat](/documentation/coregraphics/log1p(_:))
- [func log2(CGFloat) -> CGFloat](/documentation/coregraphics/log2(_:))
- [func logb(CGFloat) -> CGFloat](/documentation/coregraphics/logb(_:))
- [func nan(String) -> CGFloat](/documentation/coregraphics/nan(_:))
- [func nearbyint(CGFloat) -> CGFloat](/documentation/coregraphics/nearbyint(_:))
- [func nextafter(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/nextafter(_:_:))
- [func pow(CGFloat, CGFloat) -> CGFloat](/documentation/coregraphics/pow(_:_:))
- [func remquo(CGFloat, CGFloat) -> (CGFloat, Int)](/documentation/coregraphics/remquo(_:_:))
- [func rint(CGFloat) -> CGFloat](/documentation/coregraphics/rint(_:))
- [func sin(CGFloat) -> CGFloat](/documentation/coregraphics/sin(_:))
- [func sinh(CGFloat) -> CGFloat](/documentation/coregraphics/sinh(_:))
- [func tan(CGFloat) -> CGFloat](/documentation/coregraphics/tan(_:))
- [func tanh(CGFloat) -> CGFloat](/documentation/coregraphics/tanh(_:))
- [func tgamma(CGFloat) -> CGFloat](/documentation/coregraphics/tgamma(_:))
- [var localEventsSuppressionInterval: CFTimeInterval](/documentation/coregraphics/cgeventsource/localeventssuppressioninterval)
- [var pixelHeight: Int](/documentation/coregraphics/cgdisplaymode/pixelheight)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaystream/typeid)
- [class var typeID: CFTypeID](/documentation/coregraphics/cgcolorconversioninfo/typeid)
- [func y0(CGFloat) -> CGFloat](/documentation/coregraphics/y0(_:))
- [func y1(CGFloat) -> CGFloat](/documentation/coregraphics/y1(_:))
- [func yn(Int, CGFloat) -> CGFloat](/documentation/coregraphics/yn(_:_:))
- [func CGAffineTransformMake(CGFloat, CGFloat, CGFloat, CGFloat, CGFloat, CGFloat) -> CGAffineTransform](/documentation/coregraphics/cgaffinetransformmake(_:_:_:_:_:_:))
- [func CGColorSpaceCopyBaseColorSpace(CGColorSpace) -> CGColorSpace](/documentation/coregraphics/cgcolorspacecopybasecolorspace(_:))
- [func CGColorSpaceCreateCopyWithStandardRange(CGColorSpace) -> CGColorSpace](/documentation/coregraphics/cgcolorspacecreatecopywithstandardrange(_:))
- [func CGColorSpaceCreateExtended(CGColorSpace) -> CGColorSpace?](/documentation/coregraphics/cgcolorspacecreateextended(_:))
- [func CGColorSpaceCreateExtendedLinearized(CGColorSpace) -> CGColorSpace?](/documentation/coregraphics/cgcolorspacecreateextendedlinearized(_:))
- [func CGColorSpaceCreateWithColorSyncProfile(ColorSyncProfile?, CFDictionary?) -> CGColorSpace?](/documentation/coregraphics/cgcolorspacecreatewithcolorsyncprofile(_:_:))
- [func CGColorSpaceIsHLGBased(CGColorSpace) -> Bool](/documentation/coregraphics/cgcolorspaceishlgbased(_:))
- [func CGColorSpaceIsPQBased(CGColorSpace) -> Bool](/documentation/coregraphics/cgcolorspaceispqbased(_:))
- [func CGColorSpaceUsesITUR_2100TF(CGColorSpace) -> Bool](/documentation/coregraphics/cgcolorspaceusesitur_2100tf(_:))
- [func CGContextDrawConicGradient(CGContext, CGGradient?, CGPoint, CGFloat)](/documentation/coregraphics/cgcontextdrawconicgradient(_:_:_:_:))
- [func CGContextGetEDRTargetHeadroom(CGContext) -> Float](/documentation/coregraphics/cgcontextgetedrtargetheadroom(_:))
- [func CGConvertColorDataWithFormat(Int, Int, UnsafeMutableRawPointer!, CGColorDataFormat, UnsafeMutableRawPointer!, CGColorDataFormat, CFDictionary!) -> Bool](/documentation/coregraphics/cgconvertcolordatawithformat(_:_:_:_:_:_:_:))
- [func CGEnableEventStateCombining(boolean_t) -> CGError](/documentation/coregraphics/cgenableeventstatecombining(_:))
- [func CGErrorSetCallback(CGErrorCallback!)](/documentation/coregraphics/cgerrorsetcallback(_:))
- [func CGImageCreateCopyWithContentHeadroom(Float, CGImage) -> CGImage?](/documentation/coregraphics/cgimagecreatecopywithcontentheadroom(_:_:))
- [func CGInhibitLocalEvents(boolean_t) -> CGError](/documentation/coregraphics/cginhibitlocalevents(_:))
- [func CGPDFArrayApplyBlock(CGPDFArrayRef, (Int, CGPDFObjectRef, UnsafeMutableRawPointer?) -> Bool, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgpdfarrayapplyblock(_:_:_:))
- [func CGPDFContextBeginTag(CGContext, CGPDFTagType, CFDictionary)](/documentation/coregraphics/cgpdfcontextbegintag(_:_:_:))
- [func CGPDFContextEndTag(CGContext)](/documentation/coregraphics/cgpdfcontextendtag(_:))
- [func CGPDFContextSetIDTree(CGContext, CGPDFDictionaryRef)](/documentation/coregraphics/cgpdfcontextsetidtree(_:_:))
- [func CGPDFContextSetOutline(CGContext, CFDictionary?)](/documentation/coregraphics/cgpdfcontextsetoutline(_:_:))
- [func CGPDFContextSetPageTagStructureTree(CGContext, CFDictionary)](/documentation/coregraphics/cgpdfcontextsetpagetagstructuretree(_:_:))
- [func CGPDFContextSetParentTree(CGContext, CGPDFDictionaryRef)](/documentation/coregraphics/cgpdfcontextsetparenttree(_:_:))
- [func CGPDFDictionaryApplyBlock(CGPDFDictionaryRef, (UnsafePointer<CChar>, CGPDFObjectRef, UnsafeMutableRawPointer?) -> Bool, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgpdfdictionaryapplyblock(_:_:_:))
- [func CGPDFScannerStop(CGPDFScannerRef)](/documentation/coregraphics/cgpdfscannerstop(_:))
- [func CGPointMake(CGFloat, CGFloat) -> CGPoint](/documentation/coregraphics/cgpointmake(_:_:))
- [func CGPointMakeWithDictionaryRepresentation(CFDictionary, UnsafeMutablePointer<CGPoint>) -> Bool](/documentation/coregraphics/cgpointmakewithdictionaryrepresentation(_:_:))
- [func CGPostKeyboardEvent(CGCharCode, CGKeyCode, boolean_t) -> CGError](/documentation/coregraphics/cgpostkeyboardevent(_:_:_:))
- [func CGPreflightListenEventAccess() -> Bool](/documentation/coregraphics/cgpreflightlisteneventaccess())
- [func CGPreflightPostEventAccess() -> Bool](/documentation/coregraphics/cgpreflightposteventaccess())
- [func CGPreflightScreenCaptureAccess() -> Bool](/documentation/coregraphics/cgpreflightscreencaptureaccess())
- [func CGRectMake(CGFloat, CGFloat, CGFloat, CGFloat) -> CGRect](/documentation/coregraphics/cgrectmake(_:_:_:_:))
- [func CGRectMakeWithDictionaryRepresentation(CFDictionary, UnsafeMutablePointer<CGRect>) -> Bool](/documentation/coregraphics/cgrectmakewithdictionaryrepresentation(_:_:))
- [func CGRegisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgregisterscreenrefreshcallback(_:_:))
- [func CGReleaseScreenRefreshRects(UnsafeMutablePointer<CGRect>?)](/documentation/coregraphics/cgreleasescreenrefreshrects(_:))
- [func CGRequestListenEventAccess() -> Bool](/documentation/coregraphics/cgrequestlisteneventaccess())
- [func CGRequestPostEventAccess() -> Bool](/documentation/coregraphics/cgrequestposteventaccess())
- [func CGRequestScreenCaptureAccess() -> Bool](/documentation/coregraphics/cgrequestscreencaptureaccess())
- [func CGScreenRegisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?) -> CGError](/documentation/coregraphics/cgscreenregistermovecallback(_:_:))
- [func CGScreenUnregisterMoveCallback(CGScreenUpdateMoveCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgscreenunregistermovecallback(_:_:))
- [func CGSetLocalEventsFilterDuringSuppressionState(CGEventFilterMask, CGEventSuppressionState) -> CGError](/documentation/coregraphics/cgsetlocaleventsfilterduringsuppressionstate(_:_:))
- [func CGSetLocalEventsSuppressionInterval(CFTimeInterval) -> CGError](/documentation/coregraphics/cgsetlocaleventssuppressioninterval(_:))
- [func CGSizeMake(CGFloat, CGFloat) -> CGSize](/documentation/coregraphics/cgsizemake(_:_:))
- [func CGSizeMakeWithDictionaryRepresentation(CFDictionary, UnsafeMutablePointer<CGSize>) -> Bool](/documentation/coregraphics/cgsizemakewithdictionaryrepresentation(_:_:))
- [func CGUnregisterScreenRefreshCallback(CGScreenRefreshCallback, UnsafeMutableRawPointer?)](/documentation/coregraphics/cgunregisterscreenrefreshcallback(_:_:))
- [func CGVectorMake(CGFloat, CGFloat) -> CGVector](/documentation/coregraphics/cgvectormake(_:_:))
- [func CGWaitForScreenRefreshRects(UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<UInt32>?) -> CGError](/documentation/coregraphics/cgwaitforscreenrefreshrects(_:_:))
- [func CGWaitForScreenUpdateRects(CGScreenUpdateOperation, UnsafeMutablePointer<CGScreenUpdateOperation>?, UnsafeMutablePointer<UnsafeMutablePointer<CGRect>?>?, UnsafeMutablePointer<Int>?, UnsafeMutablePointer<CGScreenUpdateMoveDelta>?) -> CGError](/documentation/coregraphics/cgwaitforscreenupdaterects(_:_:_:_:_:))
- [var accessPermissions: CGPDFAccessPermissions](/documentation/coregraphics/cgpdfdocument/accesspermissions)
- [func applyWithBlock((UnsafePointer<CGPathElement>) -> Void)](/documentation/coregraphics/cgpath/applywithblock(_:))
- [var byteOrderInfo: CGImageByteOrderInfo](/documentation/coregraphics/cgimage/byteorderinfo)
- [var containsImageSpecificToneMappingMetadata: Bool](/documentation/coregraphics/cgimage/containsimagespecifictonemappingmetadata)
- [var contentHeadroom: Float](/documentation/coregraphics/cgimage/contentheadroom)
- [func convert(width: Int, height: Int, to: UnsafeMutableRawPointer, format: CGColorBufferFormat, from: UnsafeRawPointer, format: CGColorBufferFormat, options: CFDictionary?) -> Bool](/documentation/coregraphics/cgcolorconversioninfo/convert(width:height:to:format:from:format:options:))
- [func copyPropertyList() -> CFPropertyList?](/documentation/coregraphics/cgcolorspace/copypropertylist())
- [var info: UnsafeMutableRawPointer?](/documentation/coregraphics/cgdataprovider/info)
- [init(genericGrayGamma2_2Gray: CGFloat, alpha: CGFloat)](/documentation/coregraphics/cgcolor/init(genericgraygamma2_2gray:alpha:))
- [init?(headroom: Float, width: Int, height: Int, bitsPerComponent: Int, bitsPerPixel: Int, bytesPerRow: Int, space: CGColorSpace, bitmapInfo: CGBitmapInfo, provider: CGDataProvider, decode: UnsafePointer<CGFloat>?, shouldInterpolate: Bool, intent: CGColorRenderingIntent)](/documentation/coregraphics/cgimage/init(headroom:width:height:bitspercomponent:bitsperpixel:bytesperrow:space:bitmapinfo:provider:decode:shouldinterpolate:intent:))
- [init?(iccData: CFTypeRef)](/documentation/coregraphics/cgcolorspace/init(iccdata:))
- [init?(optionsSrc: CGColorSpace, dst: CGColorSpace, options: CFDictionary?)](/documentation/coregraphics/cgcolorconversioninfo/init(optionssrc:dst:options:))
- [init?(propertyListPlist: CFPropertyList)](/documentation/coregraphics/cgcolorspace/init(propertylistplist:))
- [init?(scrollWheelEvent2Source: CGEventSource?, units: CGScrollEventUnit, wheelCount: UInt32, wheel1: Int32, wheel2: Int32, wheel3: Int32)](/documentation/coregraphics/cgevent/init(scrollwheelevent2source:units:wheelcount:wheel1:wheel2:wheel3:))
- [func isHDR() -> Bool](/documentation/coregraphics/cgcolorspace/ishdr())
- [var name: UnsafePointer<CChar>](/documentation/coregraphics/cgpdftagtype/name)
- [var outline: CFDictionary?](/documentation/coregraphics/cgpdfdocument/outline)
- [var pixelFormatInfo: CGImagePixelFormatInfo](/documentation/coregraphics/cgimage/pixelformatinfo)
- [func resetClip()](/documentation/coregraphics/cgcontext/resetclip())
- [func setEDRTargetHeadroom(Float) -> Bool](/documentation/coregraphics/cgcontext/setedrtargetheadroom(_:))
- [var shouldToneMap: Bool](/documentation/coregraphics/cgimage/shouldtonemap)
- [func CGColorSpaceUsesExtendedRange(CGColorSpace) -> Bool](/documentation/coregraphics/cgcolorspaceusesextendedrange(_:))
- [Core Graphics Data Types](/documentation/coregraphics/core-graphics-data-types)

### Data Types

- [CGButtonCount](/documentation/coregraphics/cgbuttoncount)
- [CGCharCode](/documentation/coregraphics/cgcharcode)
- [CGDirectDisplayID](/documentation/coregraphics/cgdirectdisplayid)
- [CGDisplayBlendFraction](/documentation/coregraphics/cgdisplayblendfraction)
- [CGDisplayConfigRef](/documentation/coregraphics/cgdisplayconfigref)
- [CGDisplayCount](/documentation/coregraphics/cgdisplaycount)
- [CGDisplayErr](/documentation/coregraphics/cgdisplayerr)
- [CGDisplayFadeInterval](/documentation/coregraphics/cgdisplayfadeinterval)
- [CGDisplayFadeReservationToken](/documentation/coregraphics/cgdisplayfadereservationtoken)
- [CGDisplayMode](/documentation/coregraphics/cgdisplaymode)

#### Instance Properties

- [var height: Int](/documentation/coregraphics/cgdisplaymode/height)
- [var ioDisplayModeID: Int32](/documentation/coregraphics/cgdisplaymode/iodisplaymodeid)
- [var ioFlags: UInt32](/documentation/coregraphics/cgdisplaymode/ioflags)
- [var pixelHeight: Int](/documentation/coregraphics/cgdisplaymode/pixelheight)
- [var pixelWidth: Int](/documentation/coregraphics/cgdisplaymode/pixelwidth)
- [var refreshRate: Double](/documentation/coregraphics/cgdisplaymode/refreshrate)
- [var width: Int](/documentation/coregraphics/cgdisplaymode/width)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgdisplaymode/typeid)

#### Instance Methods

- [var pixelEncoding: CFString?](/documentation/coregraphics/cgdisplaymode/pixelencoding)
- [func isUsableForDesktopGUI() -> Bool](/documentation/coregraphics/cgdisplaymode/isusablefordesktopgui())
- [CGDisplayReconfigurationCallBack](/documentation/coregraphics/cgdisplayreconfigurationcallback)
- [CGDisplayReservationInterval](/documentation/coregraphics/cgdisplayreservationinterval)
- [CGDisplayStream](/documentation/coregraphics/cgdisplaystream)

#### Type Properties

- [class let yCbCrMatrix_ITU_R_601_4: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_601_4)
- [class let yCbCrMatrix_ITU_R_709_2: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_itu_r_709_2)
- [class let yCbCrMatrix_SMPTE_240M_1995: CFString](/documentation/coregraphics/cgdisplaystream/ycbcrmatrix_smpte_240m_1995)
- [CGDisplayStreamFrameAvailableHandler](/documentation/coregraphics/cgdisplaystreamframeavailablehandler)
- [CGDisplayStreamUpdate](/documentation/coregraphics/cgdisplaystreamupdate)
- [CGEvent](/documentation/coregraphics/cgevent)

#### Initializers

- [func copy() -> CGEvent?](/documentation/coregraphics/cgevent/copy())
- [init?(keyboardEventSource: CGEventSource?, virtualKey: CGKeyCode, keyDown: Bool)](/documentation/coregraphics/cgevent/init(keyboardeventsource:virtualkey:keydown:))
- [init?(mouseEventSource: CGEventSource?, mouseType: CGEventType, mouseCursorPosition: CGPoint, mouseButton: CGMouseButton)](/documentation/coregraphics/cgevent/init(mouseeventsource:mousetype:mousecursorposition:mousebutton:))
- [init?(source: CGEventSource?)](/documentation/coregraphics/cgevent/init(source:))
- [init?(withDataAllocator: CFAllocator?, data: CFData?)](/documentation/coregraphics/cgevent/init(withdataallocator:data:))
- [init?(scrollWheelEvent2Source: CGEventSource?, units: CGScrollEventUnit, wheelCount: UInt32, wheel1: Int32, wheel2: Int32, wheel3: Int32)](/documentation/coregraphics/cgevent/init(scrollwheelevent2source:units:wheelcount:wheel1:wheel2:wheel3:))

#### Instance Properties

- [var flags: CGEventFlags](/documentation/coregraphics/cgevent/flags)
- [var location: CGPoint](/documentation/coregraphics/cgevent/location)
- [var timestamp: CGEventTimestamp](/documentation/coregraphics/cgevent/timestamp)
- [var type: CGEventType](/documentation/coregraphics/cgevent/type)
- [var unflippedLocation: CGPoint](/documentation/coregraphics/cgevent/unflippedlocation)
- [var data: CFData?](/documentation/coregraphics/cgevent/data)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgevent/typeid)

#### Instance Methods

- [func getDoubleValueField(CGEventField) -> Double](/documentation/coregraphics/cgevent/getdoublevaluefield(_:))
- [func getIntegerValueField(CGEventField) -> Int64](/documentation/coregraphics/cgevent/getintegervaluefield(_:))
- [func keyboardGetUnicodeString(maxStringLength: Int, actualStringLength: UnsafeMutablePointer<Int>?, unicodeString: UnsafeMutablePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardgetunicodestring(maxstringlength:actualstringlength:unicodestring:))
- [func keyboardSetUnicodeString(stringLength: Int, unicodeString: UnsafePointer<UniChar>?)](/documentation/coregraphics/cgevent/keyboardsetunicodestring(stringlength:unicodestring:))
- [func post(tap: CGEventTapLocation)](/documentation/coregraphics/cgevent/post(tap:))
- [func postToPSN(processSerialNumber: UnsafeMutableRawPointer?)](/documentation/coregraphics/cgevent/posttopsn(processserialnumber:))
- [func postToPid(pid_t)](/documentation/coregraphics/cgevent/posttopid(_:))
- [func setDoubleValueField(CGEventField, value: Double)](/documentation/coregraphics/cgevent/setdoublevaluefield(_:value:))
- [func setIntegerValueField(CGEventField, value: Int64)](/documentation/coregraphics/cgevent/setintegervaluefield(_:value:))
- [func setSource(CGEventSource?)](/documentation/coregraphics/cgevent/setsource(_:))
- [func tapPostEvent(CGEventTapProxy?)](/documentation/coregraphics/cgevent/tappostevent(_:))

#### Type Methods

- [class func tapCreate(tap: CGEventTapLocation, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreate(tap:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPSN(processSerialNumber: UnsafeMutableRawPointer, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpsn(processserialnumber:place:options:eventsofinterest:callback:userinfo:))
- [class func tapCreateForPid(pid: pid_t, place: CGEventTapPlacement, options: CGEventTapOptions, eventsOfInterest: CGEventMask, callback: CGEventTapCallBack, userInfo: UnsafeMutableRawPointer?) -> CFMachPort?](/documentation/coregraphics/cgevent/tapcreateforpid(pid:place:options:eventsofinterest:callback:userinfo:))
- [class func tapEnable(tap: CFMachPort, enable: Bool)](/documentation/coregraphics/cgevent/tapenable(tap:enable:))
- [class func tapIsEnabled(tap: CFMachPort) -> Bool](/documentation/coregraphics/cgevent/tapisenabled(tap:))
- [CGEventErr](/documentation/coregraphics/cgeventerr)
- [CGEventMask](/documentation/coregraphics/cgeventmask)
- [CGEventSource](/documentation/coregraphics/cgeventsource)

#### Initializers

- [init?(event: CGEvent?)](/documentation/coregraphics/cgeventsource/init(event:))
- [init?(stateID: CGEventSourceStateID)](/documentation/coregraphics/cgeventsource/init(stateid:))

#### Instance Properties

- [var keyboardType: CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsource/keyboardtype)
- [var localEventsSuppressionInterval: CFTimeInterval](/documentation/coregraphics/cgeventsource/localeventssuppressioninterval)
- [var pixelsPerLine: Double](/documentation/coregraphics/cgeventsource/pixelsperline)
- [var sourceStateID: CGEventSourceStateID](/documentation/coregraphics/cgeventsource/sourcestateid)
- [var userData: Int64](/documentation/coregraphics/cgeventsource/userdata)

#### Type Properties

- [class var typeID: CFTypeID](/documentation/coregraphics/cgeventsource/typeid)

#### Instance Methods

- [func getLocalEventsFilterDuringSuppressionState(CGEventSuppressionState) -> CGEventFilterMask](/documentation/coregraphics/cgeventsource/getlocaleventsfilterduringsuppressionstate(_:))
- [func setLocalEventsFilterDuringSuppressionState(CGEventFilterMask, state: CGEventSuppressionState)](/documentation/coregraphics/cgeventsource/setlocaleventsfilterduringsuppressionstate(_:state:))

#### Type Methods

- [class func buttonState(CGEventSourceStateID, button: CGMouseButton) -> Bool](/documentation/coregraphics/cgeventsource/buttonstate(_:button:))
- [class func counterForEventType(CGEventSourceStateID, eventType: CGEventType) -> UInt32](/documentation/coregraphics/cgeventsource/counterforeventtype(_:eventtype:))
- [class func flagsState(CGEventSourceStateID) -> CGEventFlags](/documentation/coregraphics/cgeventsource/flagsstate(_:))
- [class func keyState(CGEventSourceStateID, key: CGKeyCode) -> Bool](/documentation/coregraphics/cgeventsource/keystate(_:key:))
- [class func secondsSinceLastEventType(CGEventSourceStateID, eventType: CGEventType) -> CFTimeInterval](/documentation/coregraphics/cgeventsource/secondssincelasteventtype(_:eventtype:))
- [CGEventSourceKeyboardType](/documentation/coregraphics/cgeventsourcekeyboardtype)
- [CGEventTapCallBack](/documentation/coregraphics/cgeventtapcallback)
- [CGEventTapInformation](/documentation/coregraphics/cgeventtapinformation)
- [CGEventTapProxy](/documentation/coregraphics/cgeventtapproxy)
- [CGEventTimestamp](/documentation/coregraphics/cgeventtimestamp)
- [CGGammaValue](/documentation/coregraphics/cggammavalue)
- [CGKeyCode](/documentation/coregraphics/cgkeycode)
- [CGOpenGLDisplayMask](/documentation/coregraphics/cgopengldisplaymask)
- [CGRectCount](/documentation/coregraphics/cgrectcount)
- [CGRefreshRate](/documentation/coregraphics/cgrefreshrate)
- [CGScreenRefreshCallback](/documentation/coregraphics/cgscreenrefreshcallback)
- [CGScreenUpdateMoveCallback](/documentation/coregraphics/cgscreenupdatemovecallback)
- [CGWheelCount](/documentation/coregraphics/cgwheelcount)
- [CGWindowID](/documentation/coregraphics/cgwindowid)
- [CGWindowLevel](/documentation/coregraphics/cgwindowlevel)

#### Window levels

- [CGWindowLevelKey](/documentation/coregraphics/cgwindowlevelkey)

##### Constants

- [case baseWindow](/documentation/coregraphics/cgwindowlevelkey/basewindow)
- [case minimumWindow](/documentation/coregraphics/cgwindowlevelkey/minimumwindow)
- [case desktopWindow](/documentation/coregraphics/cgwindowlevelkey/desktopwindow)
- [case backstopMenu](/documentation/coregraphics/cgwindowlevelkey/backstopmenu)
- [case normalWindow](/documentation/coregraphics/cgwindowlevelkey/normalwindow)
- [case floatingWindow](/documentation/coregraphics/cgwindowlevelkey/floatingwindow)
- [case tornOffMenuWindow](/documentation/coregraphics/cgwindowlevelkey/tornoffmenuwindow)
- [case dockWindow](/documentation/coregraphics/cgwindowlevelkey/dockwindow)
- [case mainMenuWindow](/documentation/coregraphics/cgwindowlevelkey/mainmenuwindow)
- [case statusWindow](/documentation/coregraphics/cgwindowlevelkey/statuswindow)
- [case modalPanelWindow](/documentation/coregraphics/cgwindowlevelkey/modalpanelwindow)
- [case popUpMenuWindow](/documentation/coregraphics/cgwindowlevelkey/popupmenuwindow)
- [case draggingWindow](/documentation/coregraphics/cgwindowlevelkey/draggingwindow)
- [case screenSaverWindow](/documentation/coregraphics/cgwindowlevelkey/screensaverwindow)
- [case maximumWindow](/documentation/coregraphics/cgwindowlevelkey/maximumwindow)
- [case overlayWindow](/documentation/coregraphics/cgwindowlevelkey/overlaywindow)
- [case helpWindow](/documentation/coregraphics/cgwindowlevelkey/helpwindow)
- [case utilityWindow](/documentation/coregraphics/cgwindowlevelkey/utilitywindow)
- [case desktopIconWindow](/documentation/coregraphics/cgwindowlevelkey/desktopiconwindow)
- [case cursorWindow](/documentation/coregraphics/cgwindowlevelkey/cursorwindow)
- [case assistiveTechHighWindow](/documentation/coregraphics/cgwindowlevelkey/assistivetechhighwindow)
- [case numberOfWindowLevelKeys](/documentation/coregraphics/cgwindowlevelkey/numberofwindowlevelkeys)

##### Initializers

- [init?(rawValue: Int32)](/documentation/coregraphics/cgwindowlevelkey/init(rawvalue:))
- [CGErrorCallback](/documentation/coregraphics/cgerrorcallback)
- [CGPDFArrayApplierBlock](/documentation/coregraphics/cgpdfarrayapplierblock)
- [CGPDFDictionaryApplierBlock](/documentation/coregraphics/cgpdfdictionaryapplierblock)
- [CGPDFTagProperty](/documentation/coregraphics/cgpdftagproperty)

#### Initializers

- [init(rawValue: CFString)](/documentation/coregraphics/cgpdftagproperty/init(rawvalue:))

#### Type Properties

- [static let actualText: CGPDFTagProperty](/documentation/coregraphics/cgpdftagproperty/actualtext)
- [static let alternativeText: CGPDFTagProperty](/documentation/coregraphics/cgpdftagproperty/alternativetext)
- [static let languageText: CGPDFTagProperty](/documentation/coregraphics/cgpdftagproperty/languagetext)
- [static let titleText: CGPDFTagProperty](/documentation/coregraphics/cgpdftagproperty/titletext)
- [CGPSConverterBeginDocumentCallback](/documentation/coregraphics/cgpsconverterbegindocumentcallback)
- [CGPSConverterBeginPageCallback](/documentation/coregraphics/cgpsconverterbeginpagecallback)
- [CGPSConverterEndDocumentCallback](/documentation/coregraphics/cgpsconverterenddocumentcallback)
- [CGPSConverterEndPageCallback](/documentation/coregraphics/cgpsconverterendpagecallback)
- [CGPSConverterMessageCallback](/documentation/coregraphics/cgpsconvertermessagecallback)
- [CGPSConverterProgressCallback](/documentation/coregraphics/cgpsconverterprogresscallback)
- [CGPSConverterReleaseInfoCallback](/documentation/coregraphics/cgpsconverterreleaseinfocallback)
- [CGPathApplyBlock](/documentation/coregraphics/cgpathapplyblock)

## Classes

- [CGRenderingBufferProvider](/documentation/coregraphics/cgrenderingbufferprovider)

### Protocols

- [CGRenderingBufferProvider.Info](/documentation/coregraphics/cgrenderingbufferprovider/info)

#### Instance Methods

- [func lock() -> UnsafeMutableRawPointer?](/documentation/coregraphics/cgrenderingbufferprovider/info/lock())
- [func unlock(UnsafeMutableRawPointer)](/documentation/coregraphics/cgrenderingbufferprovider/info/unlock(_:))

## Structures

- [CGBitmapParameters](/documentation/coregraphics/cgbitmapparameters-4v8wo)

### Instance Properties

- [var colorSpace: CGColorSpace](/documentation/coregraphics/cgbitmapparameters-4v8wo/colorspace)

### Subscripts

- [subscript<T>(dynamicMember _: WritableKeyPath<__CGBitmapParameters, T>) -> T](/documentation/coregraphics/cgbitmapparameters-4v8wo/subscript(dynamicmember:)-9hrsu)
- [subscript<T>(dynamicMember _: KeyPath<__CGBitmapParameters, T>) -> T](/documentation/coregraphics/cgbitmapparameters-4v8wo/subscript(dynamicmember:)-psx7)
- [CGColorModel](/documentation/coregraphics/cgcolormodel)

### Initializers

- [init(rawValue: UInt32)](/documentation/coregraphics/cgcolormodel/init(rawvalue:))

### Type Properties

- [static var cmyk: CGColorModel](/documentation/coregraphics/cgcolormodel/cmyk)
- [static var deviceN: CGColorModel](/documentation/coregraphics/cgcolormodel/devicen)
- [static var gray: CGColorModel](/documentation/coregraphics/cgcolormodel/gray)
- [static var lab: CGColorModel](/documentation/coregraphics/cgcolormodel/lab)
- [static var rgb: CGColorModel](/documentation/coregraphics/cgcolormodel/rgb)
- [CGContentInfo](/documentation/coregraphics/cgcontentinfo)

### Initializers

- [init()](/documentation/coregraphics/cgcontentinfo/init())
- [init(deepestImageComponent: CGComponent, contentColorModels: CGColorModel, hasWideGamut: Bool, hasTransparency: Bool, largestContentHeadroom: Float)](/documentation/coregraphics/cgcontentinfo/init(deepestimagecomponent:contentcolormodels:haswidegamut:hastransparency:largestcontentheadroom:))

### Instance Properties

- [var contentColorModels: CGColorModel](/documentation/coregraphics/cgcontentinfo/contentcolormodels)
- [var deepestImageComponent: CGComponent](/documentation/coregraphics/cgcontentinfo/deepestimagecomponent)
- [var hasTransparency: Bool](/documentation/coregraphics/cgcontentinfo/hastransparency)
- [var hasWideGamut: Bool](/documentation/coregraphics/cgcontentinfo/haswidegamut)
- [var largestContentHeadroom: Float](/documentation/coregraphics/cgcontentinfo/largestcontentheadroom)

## Enumerations

- [CGBitmapLayout](/documentation/coregraphics/cgbitmaplayout)

### Enumeration Cases

- [case abgr](/documentation/coregraphics/cgbitmaplayout/abgr)
- [case alphaOnly](/documentation/coregraphics/cgbitmaplayout/alphaonly)
- [case argb](/documentation/coregraphics/cgbitmaplayout/argb)
- [case bgra](/documentation/coregraphics/cgbitmaplayout/bgra)
- [case bgrx](/documentation/coregraphics/cgbitmaplayout/bgrx)
- [case cmyk](/documentation/coregraphics/cgbitmaplayout/cmyk)
- [case gray](/documentation/coregraphics/cgbitmaplayout/gray)
- [case grayAlpha](/documentation/coregraphics/cgbitmaplayout/grayalpha)
- [case rgba](/documentation/coregraphics/cgbitmaplayout/rgba)
- [case rgbx](/documentation/coregraphics/cgbitmaplayout/rgbx)
- [case xbgr](/documentation/coregraphics/cgbitmaplayout/xbgr)
- [case xrgb](/documentation/coregraphics/cgbitmaplayout/xrgb)

### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgbitmaplayout/init(rawvalue:))
- [CGComponent](/documentation/coregraphics/cgcomponent)

### Enumeration Cases

- [case float16Bit](/documentation/coregraphics/cgcomponent/float16bit)
- [case float32Bit](/documentation/coregraphics/cgcomponent/float32bit)
- [case integer10Bit](/documentation/coregraphics/cgcomponent/integer10bit)
- [case integer16Bit](/documentation/coregraphics/cgcomponent/integer16bit)
- [case integer32Bit](/documentation/coregraphics/cgcomponent/integer32bit)
- [case integer8Bit](/documentation/coregraphics/cgcomponent/integer8bit)
- [case unknown](/documentation/coregraphics/cgcomponent/unknown)

### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgcomponent/init(rawvalue:))
- [CGContentToneMappingInfo](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum)

### Structures

- [CGContentToneMappingInfo.DefaultOptions](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/defaultoptions)

#### Initializers

- [init()](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/defaultoptions/init())
- [init(contentAverageLightLevel: CGContentToneMappingInfo.LightLevel, preferredDynamicRange: CGContentToneMappingInfo.DynamicRange)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/defaultoptions/init(contentaveragelightlevel:preferreddynamicrange:))

#### Instance Properties

- [var contentAverageLightLevel: CGContentToneMappingInfo.LightLevel](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/defaultoptions/contentaveragelightlevel)
- [var preferredDynamicRange: CGContentToneMappingInfo.DynamicRange](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/defaultoptions/preferreddynamicrange)
- [CGContentToneMappingInfo.EXRGammaOptions](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions)

#### Initializers

- [init()](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/init())
- [init(defog: Float, exposure: Float, kneeHigh: Float, kneeLow: Float)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/init(defog:exposure:kneehigh:kneelow:))

#### Instance Properties

- [var defog: Float](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/defog)
- [var exposure: Float](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/exposure)
- [var kneeHigh: Float](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/kneehigh)
- [var kneeLow: Float](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgammaoptions/kneelow)
- [CGContentToneMappingInfo.ITURecommendedOptions](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions)

#### Initializers

- [init()](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/init())
- [init(skipBoostToHDR: Bool, use100nitsHLGOOTF: Bool, useBT1886ForCoreVideoGamma: Bool, useLegacyHDREcosystem: Bool)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/init(skipboosttohdr:use100nitshlgootf:usebt1886forcorevideogamma:uselegacyhdrecosystem:))

#### Instance Properties

- [var skipBoostToHDR: Bool](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/skipboosttohdr)
- [var use100nitsHLGOOTF: Bool](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/use100nitshlgootf)
- [var useBT1886ForCoreVideoGamma: Bool](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/usebt1886forcorevideogamma)
- [var useLegacyHDREcosystem: Bool](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommendedoptions/uselegacyhdrecosystem)

### Enumeration Cases

- [case `default`(CGContentToneMappingInfo.DefaultOptions)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/default(_:))
- [case exrGamma(CGContentToneMappingInfo.EXRGammaOptions)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/exrgamma(_:))
- [case imageSpecificLumaScaling(CGContentToneMappingInfo.DefaultOptions)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/imagespecificlumascaling(_:))
- [case ituRecommended(CGContentToneMappingInfo.ITURecommendedOptions)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/iturecommended(_:))
- [case none](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/none)
- [case referenceWhiteBased(CGContentToneMappingInfo.DefaultOptions)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/referencewhitebased(_:))

### Enumerations

- [CGContentToneMappingInfo.DynamicRange](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/dynamicrange)

#### Enumeration Cases

- [case constrained](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/dynamicrange/constrained)
- [case high](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/dynamicrange/high)
- [case standard](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/dynamicrange/standard)
- [CGContentToneMappingInfo.LightLevel](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/lightlevel)

#### Enumeration Cases

- [case nits(Int)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/lightlevel/nits(_:))
- [case relative(Float)](/documentation/coregraphics/cgcontenttonemappinginfo-swift.enum/lightlevel/relative(_:))
- [CGImageComponentInfo](/documentation/coregraphics/cgimagecomponentinfo)

### Enumeration Cases

- [case float](/documentation/coregraphics/cgimagecomponentinfo/float)
- [case integer](/documentation/coregraphics/cgimagecomponentinfo/integer)

### Initializers

- [init?(rawValue: UInt32)](/documentation/coregraphics/cgimagecomponentinfo/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
