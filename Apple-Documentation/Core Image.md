# Core Image Documentation

Source: https://sosumi.ai/documentation/coreimage

---
title: Core Image
source: https://developer.apple.com/documentation/coreimage
timestamp: 2026-02-13T18:55:22.592Z
---

## Essentials

- [Processing an Image Using Built-in Filters](/documentation/coreimage/processing-an-image-using-built-in-filters)
- [CIContext](/documentation/coreimage/cicontext)

### Creating a Context Without Specifying a Destination

- [init()](/documentation/coreimage/cicontext/init())

### Creating a Context for CPU-Based Rendering

- [init(cgContext: CGContext, options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(cgcontext:options:))

### Creating a Context for GPU-Based Rendering

- [init(mtlDevice: any MTLDevice)](/documentation/coreimage/cicontext/init(mtldevice:))
- [init(mtlDevice: any MTLDevice, options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(mtldevice:options:))
- [init(mtlCommandQueue: any MTLCommandQueue)](/documentation/coreimage/cicontext/init(mtlcommandqueue:))
- [init(mtlCommandQueue: any MTLCommandQueue, options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(mtlcommandqueue:options:))

### Rendering Images

- [func createCGImage(CIImage, from: CGRect) -> CGImage?](/documentation/coreimage/cicontext/createcgimage(_:from:))
- [func createCGImage(CIImage, from: CGRect, format: CIFormat, colorSpace: CGColorSpace?) -> CGImage?](/documentation/coreimage/cicontext/createcgimage(_:from:format:colorspace:))
- [func createCGImage(CIImage, from: CGRect, format: CIFormat, colorSpace: CGColorSpace?, deferred: Bool) -> CGImage?](/documentation/coreimage/cicontext/createcgimage(_:from:format:colorspace:deferred:))
- [func render(CIImage, toBitmap: UnsafeMutableRawPointer, rowBytes: Int, bounds: CGRect, format: CIFormat, colorSpace: CGColorSpace?)](/documentation/coreimage/cicontext/render(_:tobitmap:rowbytes:bounds:format:colorspace:))
- [func render(CIImage, to: CVPixelBuffer)](/documentation/coreimage/cicontext/render(_:to:))
- [func render(CIImage, to: CVPixelBuffer, bounds: CGRect, colorSpace: CGColorSpace?)](/documentation/coreimage/cicontext/render(_:to:bounds:colorspace:)-2k8l2)
- [func render(CIImage, to: IOSurfaceRef, bounds: CGRect, colorSpace: CGColorSpace?)](/documentation/coreimage/cicontext/render(_:to:bounds:colorspace:)-54b9l)
- [func render(CIImage, to: any MTLTexture, commandBuffer: (any MTLCommandBuffer)?, bounds: CGRect, colorSpace: CGColorSpace)](/documentation/coreimage/cicontext/render(_:to:commandbuffer:bounds:colorspace:))

### Drawing Images

- [func draw(CIImage, in: CGRect, from: CGRect)](/documentation/coreimage/cicontext/draw(_:in:from:))

### Determining the Allowed Extents for Images Used by a Context

- [func inputImageMaximumSize() -> CGSize](/documentation/coreimage/cicontext/inputimagemaximumsize())
- [func outputImageMaximumSize() -> CGSize](/documentation/coreimage/cicontext/outputimagemaximumsize())

### Managing Resources

- [func clearCaches()](/documentation/coreimage/cicontext/clearcaches())
- [func reclaimResources()](/documentation/coreimage/cicontext/reclaimresources())
- [class func offlineGPUCount() -> UInt32](/documentation/coreimage/cicontext/offlinegpucount())
- [var workingColorSpace: CGColorSpace?](/documentation/coreimage/cicontext/workingcolorspace)
- [var workingFormat: CIFormat](/documentation/coreimage/cicontext/workingformat)

### Rendering Images for Data or File Export

- [func tiffRepresentation(of: CIImage, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) -> Data?](/documentation/coreimage/cicontext/tiffrepresentation(of:format:colorspace:options:))
- [func jpegRepresentation(of: CIImage, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) -> Data?](/documentation/coreimage/cicontext/jpegrepresentation(of:colorspace:options:))
- [func pngRepresentation(of: CIImage, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) -> Data?](/documentation/coreimage/cicontext/pngrepresentation(of:format:colorspace:options:))
- [func heifRepresentation(of: CIImage, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) -> Data?](/documentation/coreimage/cicontext/heifrepresentation(of:format:colorspace:options:))
- [func heif10Representation(of: CIImage, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws -> Data](/documentation/coreimage/cicontext/heif10representation(of:colorspace:options:))
- [func openEXRRepresentation(of: CIImage, options: [CIImageRepresentationOption : Any]) throws -> Data](/documentation/coreimage/cicontext/openexrrepresentation(of:options:))
- [func writeTIFFRepresentation(of: CIImage, to: URL, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writetiffrepresentation(of:to:format:colorspace:options:))
- [func writeJPEGRepresentation(of: CIImage, to: URL, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writejpegrepresentation(of:to:colorspace:options:))
- [func writePNGRepresentation(of: CIImage, to: URL, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writepngrepresentation(of:to:format:colorspace:options:))
- [func writeHEIFRepresentation(of: CIImage, to: URL, format: CIFormat, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writeheifrepresentation(of:to:format:colorspace:options:))
- [func writeHEIF10Representation(of: CIImage, to: URL, colorSpace: CGColorSpace, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writeheif10representation(of:to:colorspace:options:))
- [func writeOpenEXRRepresentation(of: CIImage, to: URL, options: [CIImageRepresentationOption : Any]) throws](/documentation/coreimage/cicontext/writeopenexrrepresentation(of:to:options:))
- [CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/ciimagerepresentationoption/init(rawvalue:))

#### Type Properties

- [static let avDepthData: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/avdepthdata)
- [static let avPortraitEffectsMatte: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/avportraiteffectsmatte)
- [static let avSemanticSegmentationMattes: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/avsemanticsegmentationmattes)
- [static let depthImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/depthimage)
- [static let disparityImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/disparityimage)
- [static let portraitEffectsMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/portraiteffectsmatteimage)
- [static let semanticSegmentationGlassesMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/semanticsegmentationglassesmatteimage)
- [static let semanticSegmentationHairMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/semanticsegmentationhairmatteimage)
- [static let semanticSegmentationSkinMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/semanticsegmentationskinmatteimage)
- [static let semanticSegmentationSkyMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/semanticsegmentationskymatteimage)
- [static let semanticSegmentationTeethMatteImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/semanticsegmentationteethmatteimage)
- [static let hdrImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/hdrimage)
- [static let hdrGainMapAsRGB: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/hdrgainmapasrgb)
- [static let hdrGainMapImage: CIImageRepresentationOption](/documentation/coreimage/ciimagerepresentationoption/hdrgainmapimage)

### Creating Depth Blur Filters

- [func depthBlurEffectFilter(for: CIImage, disparityImage: CIImage, portraitEffectsMatte: CIImage?, hairSemanticSegmentation: CIImage?, glassesMatte: CIImage?, gainMap: CIImage?, orientation: CGImagePropertyOrientation, options: [AnyHashable : Any]?) -> CIFilter?](/documentation/coreimage/cicontext/depthblureffectfilter(for:disparityimage:portraiteffectsmatte:hairsemanticsegmentation:glassesmatte:gainmap:orientation:options:))
- [func depthBlurEffectFilter(for: CIImage, disparityImage: CIImage, portraitEffectsMatte: CIImage?, hairSemanticSegmentation: CIImage?, orientation: CGImagePropertyOrientation, options: [AnyHashable : Any]?) -> CIFilter?](/documentation/coreimage/cicontext/depthblureffectfilter(for:disparityimage:portraiteffectsmatte:hairsemanticsegmentation:orientation:options:))
- [func depthBlurEffectFilter(for: CIImage, disparityImage: CIImage, portraitEffectsMatte: CIImage?, orientation: CGImagePropertyOrientation, options: [AnyHashable : Any]?) -> CIFilter?](/documentation/coreimage/cicontext/depthblureffectfilter(for:disparityimage:portraiteffectsmatte:orientation:options:))
- [func depthBlurEffectFilter(forImageData: Data, options: [AnyHashable : Any]?) -> CIFilter?](/documentation/coreimage/cicontext/depthblureffectfilter(forimagedata:options:))
- [func depthBlurEffectFilter(forImageURL: URL, options: [AnyHashable : Any]?) -> CIFilter?](/documentation/coreimage/cicontext/depthblureffectfilter(forimageurl:options:))

### Constants

- [CIContextOption](/documentation/coreimage/cicontextoption)

#### Type Properties

- [static let allowLowPower: CIContextOption](/documentation/coreimage/cicontextoption/allowlowpower)
- [static let cacheIntermediates: CIContextOption](/documentation/coreimage/cicontextoption/cacheintermediates)
- [static let highQualityDownsample: CIContextOption](/documentation/coreimage/cicontextoption/highqualitydownsample)
- [static let memoryTarget: CIContextOption](/documentation/coreimage/cicontextoption/memorytarget)
- [static let name: CIContextOption](/documentation/coreimage/cicontextoption/name)
- [static let outputColorSpace: CIContextOption](/documentation/coreimage/cicontextoption/outputcolorspace)
- [static let outputPremultiplied: CIContextOption](/documentation/coreimage/cicontextoption/outputpremultiplied)
- [static let priorityRequestLow: CIContextOption](/documentation/coreimage/cicontextoption/priorityrequestlow)
- [static let useSoftwareRenderer: CIContextOption](/documentation/coreimage/cicontextoption/usesoftwarerenderer)
- [static let workingColorSpace: CIContextOption](/documentation/coreimage/cicontextoption/workingcolorspace)
- [static let workingFormat: CIContextOption](/documentation/coreimage/cicontextoption/workingformat)
- [static let cvMetalTextureCache: CIContextOption](/documentation/coreimage/cicontextoption/cvmetaltexturecache)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/cicontextoption/init(rawvalue:))

### Customizing Render Destination

- [func prepareRender(CIImage, from: CGRect, to: CIRenderDestination, at: CGPoint) throws](/documentation/coreimage/cicontext/preparerender(_:from:to:at:))
- [func startTask(toClear: CIRenderDestination) throws -> CIRenderTask](/documentation/coreimage/cicontext/starttask(toclear:))
- [func startTask(toRender: CIImage, from: CGRect, to: CIRenderDestination, at: CGPoint) throws -> CIRenderTask](/documentation/coreimage/cicontext/starttask(torender:from:to:at:))
- [func startTask(toRender: CIImage, to: CIRenderDestination) throws -> CIRenderTask](/documentation/coreimage/cicontext/starttask(torender:to:))

### Deprecated

- [init(cglContext: CGLContextObj, pixelFormat: CGLPixelFormatObj?, colorSpace: CGColorSpace?, options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(cglcontext:pixelformat:colorspace:options:))
- [init(eaglContext: EAGLContext)](/documentation/coreimage/cicontext/init(eaglcontext:))
- [init(eaglContext: EAGLContext, options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(eaglcontext:options:))
- [init?(forOfflineGPUAtIndex: UInt32)](/documentation/coreimage/cicontext/init(forofflinegpuatindex:))
- [init?(forOfflineGPUAtIndex: UInt32, colorSpace: CGColorSpace?, options: [CIContextOption : Any]?, sharedContext: CGLContextObj?)](/documentation/coreimage/cicontext/init(forofflinegpuatindex:colorspace:options:sharedcontext:))
- [func createCGLayer(with: CGSize, info: CFDictionary?) -> CGLayer?](/documentation/coreimage/cicontext/createcglayer(with:info:))
- [func draw(CIImage, at: CGPoint, from: CGRect)](/documentation/coreimage/cicontext/draw(_:at:from:))

### Initializers

- [init(options: [CIContextOption : Any]?)](/documentation/coreimage/cicontext/init(options:))

### Instance Methods

- [func calculateHDRStats(for: CGImage) -> CGImage](/documentation/coreimage/cicontext/calculatehdrstats(for:)-3ia7r)
- [func calculateHDRStats(for: IOSurfaceRef)](/documentation/coreimage/cicontext/calculatehdrstats(for:)-6lwmz)
- [func calculateHDRStats(for: CVPixelBuffer)](/documentation/coreimage/cicontext/calculatehdrstats(for:)-7bcki)
- [func calculateHDRStats(for: CIImage) -> CIImage?](/documentation/coreimage/cicontext/calculatehdrstats(for:)-l1rj)
- [func createCGImage(CIImage, from: CGRect, format: CIFormat, colorSpace: CGColorSpace?, deferred: Bool, calculateHDRStats: Bool) -> CGImage?](/documentation/coreimage/cicontext/createcgimage(_:from:format:colorspace:deferred:calculatehdrstats:))
- [CIImage](/documentation/coreimage/ciimage)

### Creating an Image

- [class func empty() -> CIImage](/documentation/coreimage/ciimage/empty())
- [init?(image: UIImage)](/documentation/coreimage/ciimage/init(image:))
- [init?(image: UIImage, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(image:options:))
- [init?(contentsOf: URL)](/documentation/coreimage/ciimage/init(contentsof:))
- [init?(contentsOf: URL, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(contentsof:options:))
- [init(cgImage: CGImage)](/documentation/coreimage/ciimage/init(cgimage:))
- [init(cgImage: CGImage, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(cgimage:options:))
- [init(cgImageSource: CGImageSource, index: Int, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(cgimagesource:index:options:))
- [init?(data: Data)](/documentation/coreimage/ciimage/init(data:))
- [init?(data: Data, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(data:options:))
- [init(bitmapData: Data, bytesPerRow: Int, size: CGSize, format: CIFormat, colorSpace: CGColorSpace?)](/documentation/coreimage/ciimage/init(bitmapdata:bytesperrow:size:format:colorspace:))
- [init?(bitmapImageRep: NSBitmapImageRep)](/documentation/coreimage/ciimage/init(bitmapimagerep:))
- [init(imageProvider: Any, size: Int, Int, format: CIFormat, colorSpace: CGColorSpace?, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(imageprovider:size:_:format:colorspace:options:))
- [init?(depthData: AVDepthData)](/documentation/coreimage/ciimage/init(depthdata:))
- [init?(depthData: AVDepthData, options: [String : Any]?)](/documentation/coreimage/ciimage/init(depthdata:options:))
- [init?(portaitEffectsMatte: AVPortraitEffectsMatte)](/documentation/coreimage/ciimage/init(portaiteffectsmatte:))
- [init?(portaitEffectsMatte: AVPortraitEffectsMatte, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(portaiteffectsmatte:options:))
- [init?(semanticSegmentationMatte: AVSemanticSegmentationMatte)](/documentation/coreimage/ciimage/init(semanticsegmentationmatte:))
- [init?(semanticSegmentationMatte: AVSemanticSegmentationMatte, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(semanticsegmentationmatte:options:))
- [init(cvImageBuffer: CVImageBuffer)](/documentation/coreimage/ciimage/init(cvimagebuffer:))
- [init(cvImageBuffer: CVImageBuffer, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(cvimagebuffer:options:))
- [init(cvPixelBuffer: CVPixelBuffer)](/documentation/coreimage/ciimage/init(cvpixelbuffer:))
- [init(cvPixelBuffer: CVPixelBuffer, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(cvpixelbuffer:options:))
- [init?(mtlTexture: any MTLTexture, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(mtltexture:options:))
- [init(ioSurface: IOSurfaceRef)](/documentation/coreimage/ciimage/init(iosurface:))
- [init(ioSurface: IOSurfaceRef, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(iosurface:options:))

### Creating an Image by Modifying an Existing Image

- [func applyingFilter(String, parameters: [String : Any]) -> CIImage](/documentation/coreimage/ciimage/applyingfilter(_:parameters:))
- [func applyingFilter(String) -> CIImage](/documentation/coreimage/ciimage/applyingfilter(_:))
- [func transformed(by: CGAffineTransform) -> CIImage](/documentation/coreimage/ciimage/transformed(by:))
- [func transformed(by: CGAffineTransform, highQualityDownsample: Bool) -> CIImage](/documentation/coreimage/ciimage/transformed(by:highqualitydownsample:))
- [func cropped(to: CGRect) -> CIImage](/documentation/coreimage/ciimage/cropped(to:))
- [func oriented(forExifOrientation: Int32) -> CIImage](/documentation/coreimage/ciimage/oriented(forexiforientation:))
- [func clampedToExtent() -> CIImage](/documentation/coreimage/ciimage/clampedtoextent())
- [func clamped(to: CGRect) -> CIImage](/documentation/coreimage/ciimage/clamped(to:))
- [func composited(over: CIImage) -> CIImage](/documentation/coreimage/ciimage/composited(over:))
- [func convertingWorkingSpaceToLab() -> CIImage](/documentation/coreimage/ciimage/convertingworkingspacetolab())
- [func convertingLabToWorkingSpace() -> CIImage](/documentation/coreimage/ciimage/convertinglabtoworkingspace())
- [func matchedToWorkingSpace(from: CGColorSpace) -> CIImage?](/documentation/coreimage/ciimage/matchedtoworkingspace(from:))
- [func matchedFromWorkingSpace(to: CGColorSpace) -> CIImage?](/documentation/coreimage/ciimage/matchedfromworkingspace(to:))
- [func premultiplyingAlpha() -> CIImage](/documentation/coreimage/ciimage/premultiplyingalpha())
- [func unpremultiplyingAlpha() -> CIImage](/documentation/coreimage/ciimage/unpremultiplyingalpha())
- [func settingAlphaOne(in: CGRect) -> CIImage](/documentation/coreimage/ciimage/settingalphaone(in:))
- [func applyingGaussianBlur(sigma: Double) -> CIImage](/documentation/coreimage/ciimage/applyinggaussianblur(sigma:))
- [func settingProperties([AnyHashable : Any]) -> CIImage](/documentation/coreimage/ciimage/settingproperties(_:))
- [func insertingIntermediate() -> CIImage](/documentation/coreimage/ciimage/insertingintermediate())
- [func insertingIntermediate(cache: Bool) -> CIImage](/documentation/coreimage/ciimage/insertingintermediate(cache:))

### Creating Solid Colors

- [init(color: CIColor)](/documentation/coreimage/ciimage/init(color:))
- [class var black: CIImage](/documentation/coreimage/ciimage/black)
- [class var blue: CIImage](/documentation/coreimage/ciimage/blue)
- [class var clear: CIImage](/documentation/coreimage/ciimage/clear)
- [class var cyan: CIImage](/documentation/coreimage/ciimage/cyan)
- [class var gray: CIImage](/documentation/coreimage/ciimage/gray)
- [class var green: CIImage](/documentation/coreimage/ciimage/green)
- [class var magenta: CIImage](/documentation/coreimage/ciimage/magenta)
- [class var red: CIImage](/documentation/coreimage/ciimage/red)
- [class var white: CIImage](/documentation/coreimage/ciimage/white)
- [class var yellow: CIImage](/documentation/coreimage/ciimage/yellow)

### Getting Image Information

- [var definition: CIFilterShape](/documentation/coreimage/ciimage/definition)
- [var extent: CGRect](/documentation/coreimage/ciimage/extent)
- [var properties: [String : Any]](/documentation/coreimage/ciimage/properties)
- [var url: URL?](/documentation/coreimage/ciimage/url)
- [var colorSpace: CGColorSpace?](/documentation/coreimage/ciimage/colorspace)
- [func orientationTransform(forExifOrientation: Int32) -> CGAffineTransform](/documentation/coreimage/ciimage/orientationtransform(forexiforientation:))

### Drawing Images

- [func draw(at: NSPoint, from: NSRect, operation: NSCompositingOperation, fraction: CGFloat)](/documentation/coreimage/ciimage/draw(at:from:operation:fraction:))
- [func draw(in: NSRect, from: NSRect, operation: NSCompositingOperation, fraction: CGFloat)](/documentation/coreimage/ciimage/draw(in:from:operation:fraction:))

### Getting Autoadjustment Filters

- [func autoAdjustmentFilters() -> [CIFilter]](/documentation/coreimage/ciimage/autoadjustmentfilters())
- [func autoAdjustmentFilters(options: [CIImageAutoAdjustmentOption : Any]?) -> [CIFilter]](/documentation/coreimage/ciimage/autoadjustmentfilters(options:))
- [Autoadjustment Keys](/documentation/coreimage/autoadjustment-keys)

#### Constants

- [static let enhance: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/enhance)
- [static let redEye: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/redeye)
- [static let features: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/features)
- [static let crop: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/crop)
- [static let level: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/level)

### Working with Filter Regions of Interest

- [func regionOfInterest(for: CIImage, in: CGRect) -> CGRect](/documentation/coreimage/ciimage/regionofinterest(for:in:))

### Working with Orientation

- [func oriented(CGImagePropertyOrientation) -> CIImage](/documentation/coreimage/ciimage/oriented(_:))
- [func orientationTransform(for: CGImagePropertyOrientation) -> CGAffineTransform](/documentation/coreimage/ciimage/orientationtransform(for:))

### Sampling the Image

- [func samplingNearest() -> CIImage](/documentation/coreimage/ciimage/samplingnearest())
- [func samplingLinear() -> CIImage](/documentation/coreimage/ciimage/samplinglinear())

### Accessing Original Image Content

- [var cgImage: CGImage?](/documentation/coreimage/ciimage/cgimage)
- [var pixelBuffer: CVPixelBuffer?](/documentation/coreimage/ciimage/pixelbuffer)
- [var depthData: AVDepthData?](/documentation/coreimage/ciimage/depthdata)
- [var portraitEffectsMatte: AVPortraitEffectsMatte?](/documentation/coreimage/ciimage/portraiteffectsmatte)
- [var semanticSegmentationMatte: AVSemanticSegmentationMatte?](/documentation/coreimage/ciimage/semanticsegmentationmatte)

### Image Dictionary Keys

- [CIImageOption](/documentation/coreimage/ciimageoption)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/ciimageoption/init(rawvalue:))

#### Type Properties

- [static let applyOrientationProperty: CIImageOption](/documentation/coreimage/ciimageoption/applyorientationproperty)
- [static let auxiliaryDepth: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarydepth)
- [static let auxiliaryDisparity: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarydisparity)
- [static let auxiliaryHDRGainMap: CIImageOption](/documentation/coreimage/ciimageoption/auxiliaryhdrgainmap)
- [static let auxiliaryPortraitEffectsMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliaryportraiteffectsmatte)
- [static let auxiliarySemanticSegmentationGlassesMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarysemanticsegmentationglassesmatte)
- [static let auxiliarySemanticSegmentationHairMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarysemanticsegmentationhairmatte)
- [static let auxiliarySemanticSegmentationSkinMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarysemanticsegmentationskinmatte)
- [static let auxiliarySemanticSegmentationSkyMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarysemanticsegmentationskymatte)
- [static let auxiliarySemanticSegmentationTeethMatte: CIImageOption](/documentation/coreimage/ciimageoption/auxiliarysemanticsegmentationteethmatte)
- [static let cacheImmediately: CIImageOption](/documentation/coreimage/ciimageoption/cacheimmediately)
- [static let colorSpace: CIImageOption](/documentation/coreimage/ciimageoption/colorspace)
- [static let expandToHDR: CIImageOption](/documentation/coreimage/ciimageoption/expandtohdr)
- [static let nearestSampling: CIImageOption](/documentation/coreimage/ciimageoption/nearestsampling)
- [static let properties: CIImageOption](/documentation/coreimage/ciimageoption/properties)
- [static let providerTileSize: CIImageOption](/documentation/coreimage/ciimageoption/providertilesize)
- [static let providerUserInfo: CIImageOption](/documentation/coreimage/ciimageoption/provideruserinfo)
- [static let textureFormat: CIImageOption](/documentation/coreimage/ciimageoption/textureformat)
- [static let textureTarget: CIImageOption](/documentation/coreimage/ciimageoption/texturetarget)
- [static let toneMapHDRtoSDR: CIImageOption](/documentation/coreimage/ciimageoption/tonemaphdrtosdr)
- [static let contentHeadroom: CIImageOption](/documentation/coreimage/ciimageoption/contentheadroom)
- [static let applyCleanAperture: CIImageOption](/documentation/coreimage/ciimageoption/applycleanaperture)
- [static let contentAverageLightLevel: CIImageOption](/documentation/coreimage/ciimageoption/contentaveragelightlevel)

### AutoAdjustment Keys

- [CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/ciimageautoadjustmentoption/init(rawvalue:))

#### Type Properties

- [static let crop: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/crop)
- [static let enhance: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/enhance)
- [static let features: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/features)
- [static let level: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/level)
- [static let redEye: CIImageAutoAdjustmentOption](/documentation/coreimage/ciimageautoadjustmentoption/redeye)

### Deprecated

- [init(cgLayer: CGLayer)](/documentation/coreimage/ciimage/init(cglayer:))
- [init(cgLayer: CGLayer, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(cglayer:options:))
- [init(texture: UInt32, size: CGSize, flipped: Bool, colorSpace: CGColorSpace?)](/documentation/coreimage/ciimage/init(texture:size:flipped:colorspace:))
- [init(texture: UInt32, size: CGSize, flipped: Bool, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(texture:size:flipped:options:))
- [init(ioSurface: IOSurfaceRef, plane: Int, format: CIFormat, options: [CIImageOption : Any]?)](/documentation/coreimage/ciimage/init(iosurface:plane:format:options:))
- [static let textureTarget: CIImageOption](/documentation/coreimage/ciimageoption/texturetarget)
- [static let textureFormat: CIImageOption](/documentation/coreimage/ciimageoption/textureformat)

### Instance Properties

- [var contentHeadroom: Float](/documentation/coreimage/ciimage/contentheadroom)
- [var isOpaque: Bool](/documentation/coreimage/ciimage/isopaque)
- [var metalTexture: (any MTLTexture)?](/documentation/coreimage/ciimage/metaltexture)
- [var contentAverageLightLevel: Float](/documentation/coreimage/ciimage/contentaveragelightlevel)

### Instance Methods

- [func applyingGainMap(CIImage) -> CIImage](/documentation/coreimage/ciimage/applyinggainmap(_:))
- [func applyingGainMap(CIImage, headroom: Float) -> CIImage](/documentation/coreimage/ciimage/applyinggainmap(_:headroom:))
- [func insertingTiledIntermediate() -> CIImage](/documentation/coreimage/ciimage/insertingtiledintermediate())
- [func settingContentAverageLightLevel(Float) -> CIImage](/documentation/coreimage/ciimage/settingcontentaveragelightlevel(_:))
- [func settingContentHeadroom(Float) -> CIImage](/documentation/coreimage/ciimage/settingcontentheadroom(_:))

## Filters

- [CIFilter](/documentation/coreimage/cifilter-swift.class)

### Creating a filter

- [init?(name: String)](/documentation/coreimage/cifilter-swift.class/init(name:))
- [init?(name: String, withInputParameters: [String : Any]?)](/documentation/coreimage/cifilter-swift.class/init(name:withinputparameters:))

### Configuring type-safe filters

- [CIFilterProtocol](/documentation/coreimage/cifilterprotocol)

#### Instance Properties

- [var outputImage: CIImage?](/documentation/coreimage/cifilterprotocol/outputimage)

#### Type Methods

- [static func customAttributes() -> [String : Any]?](/documentation/coreimage/cifilterprotocol/customattributes())
- [Blur Filters](/documentation/coreimage/blur-filters)

#### Filters

- [class func bokehBlur() -> any CIFilter & CIBokehBlur](/documentation/coreimage/cifilter-swift.class/bokehblur())
- [class func boxBlur() -> any CIFilter & CIBoxBlur](/documentation/coreimage/cifilter-swift.class/boxblur())
- [class func discBlur() -> any CIFilter & CIDiscBlur](/documentation/coreimage/cifilter-swift.class/discblur())
- [class func gaussianBlur() -> any CIFilter & CIGaussianBlur](/documentation/coreimage/cifilter-swift.class/gaussianblur())
- [class func maskedVariableBlur() -> any CIFilter & CIMaskedVariableBlur](/documentation/coreimage/cifilter-swift.class/maskedvariableblur())
- [class func median() -> any CIFilter & CIMedian](/documentation/coreimage/cifilter-swift.class/median())
- [class func morphologyGradient() -> any CIFilter & CIMorphologyGradient](/documentation/coreimage/cifilter-swift.class/morphologygradient())
- [class func morphologyMaximum() -> any CIFilter & CIMorphologyMaximum](/documentation/coreimage/cifilter-swift.class/morphologymaximum())
- [class func morphologyMinimum() -> any CIFilter & CIMorphologyMinimum](/documentation/coreimage/cifilter-swift.class/morphologyminimum())
- [class func morphologyRectangleMaximum() -> any CIFilter & CIMorphologyRectangleMaximum](/documentation/coreimage/cifilter-swift.class/morphologyrectanglemaximum())
- [class func morphologyRectangleMinimum() -> any CIFilter & CIMorphologyRectangleMinimum](/documentation/coreimage/cifilter-swift.class/morphologyrectangleminimum())
- [class func motionBlur() -> any CIFilter & CIMotionBlur](/documentation/coreimage/cifilter-swift.class/motionblur())
- [class func noiseReduction() -> any CIFilter & CINoiseReduction](/documentation/coreimage/cifilter-swift.class/noisereduction())
- [class func zoomBlur() -> any CIFilter & CIZoomBlur](/documentation/coreimage/cifilter-swift.class/zoomblur())

#### Protocols

- [CIBokehBlur](/documentation/coreimage/cibokehblur)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cibokehblur/inputimage)
- [var radius: Float](/documentation/coreimage/cibokehblur/radius)
- [var ringAmount: Float](/documentation/coreimage/cibokehblur/ringamount)
- [var ringSize: Float](/documentation/coreimage/cibokehblur/ringsize)
- [var softness: Float](/documentation/coreimage/cibokehblur/softness)
- [CIBoxBlur](/documentation/coreimage/ciboxblur)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciboxblur/inputimage)
- [var radius: Float](/documentation/coreimage/ciboxblur/radius)
- [CIDiscBlur](/documentation/coreimage/cidiscblur)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidiscblur/inputimage)
- [var radius: Float](/documentation/coreimage/cidiscblur/radius)
- [CIGaussianBlur](/documentation/coreimage/cigaussianblur)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigaussianblur/inputimage)
- [var radius: Float](/documentation/coreimage/cigaussianblur/radius)
- [CIMaskedVariableBlur](/documentation/coreimage/cimaskedvariableblur)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimaskedvariableblur/inputimage)
- [var mask: CIImage?](/documentation/coreimage/cimaskedvariableblur/mask)
- [var radius: Float](/documentation/coreimage/cimaskedvariableblur/radius)
- [CIMedian](/documentation/coreimage/cimedian)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimedian/inputimage)
- [CIMorphologyGradient](/documentation/coreimage/cimorphologygradient)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologygradient/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologygradient/radius)
- [CIMorphologyMaximum](/documentation/coreimage/cimorphologymaximum)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologymaximum/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologymaximum/radius)
- [CIMorphologyMinimum](/documentation/coreimage/cimorphologyminimum)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyminimum/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologyminimum/radius)
- [CIMorphologyRectangleMaximum](/documentation/coreimage/cimorphologyrectanglemaximum)

##### Instance Properties

- [var height: Float](/documentation/coreimage/cimorphologyrectanglemaximum/height)
- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyrectanglemaximum/inputimage)
- [var width: Float](/documentation/coreimage/cimorphologyrectanglemaximum/width)
- [CIMorphologyRectangleMinimum](/documentation/coreimage/cimorphologyrectangleminimum)

##### Instance Properties

- [var height: Float](/documentation/coreimage/cimorphologyrectangleminimum/height)
- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyrectangleminimum/inputimage)
- [var width: Float](/documentation/coreimage/cimorphologyrectangleminimum/width)
- [CIMotionBlur](/documentation/coreimage/cimotionblur)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cimotionblur/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cimotionblur/inputimage)
- [var radius: Float](/documentation/coreimage/cimotionblur/radius)
- [CINoiseReduction](/documentation/coreimage/cinoisereduction)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cinoisereduction/inputimage)
- [var noiseLevel: Float](/documentation/coreimage/cinoisereduction/noiselevel)
- [var sharpness: Float](/documentation/coreimage/cinoisereduction/sharpness)
- [CIZoomBlur](/documentation/coreimage/cizoomblur)

##### Instance Properties

- [var amount: Float](/documentation/coreimage/cizoomblur/amount)
- [var center: CGPoint](/documentation/coreimage/cizoomblur/center)
- [var inputImage: CIImage?](/documentation/coreimage/cizoomblur/inputimage)
- [Color Adjustment Filters](/documentation/coreimage/color-adjustment-filters)

#### Filters

- [class func colorAbsoluteDifference() -> any CIFilter & CIColorAbsoluteDifference](/documentation/coreimage/cifilter-swift.class/colorabsolutedifference())
- [class func colorClamp() -> any CIFilter & CIColorClamp](/documentation/coreimage/cifilter-swift.class/colorclamp())
- [class func colorControls() -> any CIFilter & CIColorControls](/documentation/coreimage/cifilter-swift.class/colorcontrols())
- [class func colorMatrix() -> any CIFilter & CIColorMatrix](/documentation/coreimage/cifilter-swift.class/colormatrix())
- [class func colorPolynomial() -> any CIFilter & CIColorPolynomial](/documentation/coreimage/cifilter-swift.class/colorpolynomial())
- [class func colorThreshold() -> any CIFilter & CIColorThreshold](/documentation/coreimage/cifilter-swift.class/colorthreshold())
- [class func colorThresholdOtsu() -> any CIFilter & CIColorThresholdOtsu](/documentation/coreimage/cifilter-swift.class/colorthresholdotsu())
- [class func depthToDisparity() -> any CIFilter & CIDepthToDisparity](/documentation/coreimage/cifilter-swift.class/depthtodisparity())
- [class func disparityToDepth() -> any CIFilter & CIDisparityToDepth](/documentation/coreimage/cifilter-swift.class/disparitytodepth())
- [class func exposureAdjust() -> any CIFilter & CIExposureAdjust](/documentation/coreimage/cifilter-swift.class/exposureadjust())
- [class func gammaAdjust() -> any CIFilter & CIGammaAdjust](/documentation/coreimage/cifilter-swift.class/gammaadjust())
- [class func hueAdjust() -> any CIFilter & CIHueAdjust](/documentation/coreimage/cifilter-swift.class/hueadjust())
- [class func linearToSRGBToneCurve() -> any CIFilter & CILinearToSRGBToneCurve](/documentation/coreimage/cifilter-swift.class/lineartosrgbtonecurve())
- [class func sRGBToneCurveToLinear() -> any CIFilter & CISRGBToneCurveToLinear](/documentation/coreimage/cifilter-swift.class/srgbtonecurvetolinear())
- [class func temperatureAndTint() -> any CIFilter & CITemperatureAndTint](/documentation/coreimage/cifilter-swift.class/temperatureandtint())
- [class func toneCurve() -> any CIFilter & CIToneCurve](/documentation/coreimage/cifilter-swift.class/tonecurve())
- [class func vibrance() -> any CIFilter & CIVibrance](/documentation/coreimage/cifilter-swift.class/vibrance())
- [class func whitePointAdjust() -> any CIFilter & CIWhitePointAdjust](/documentation/coreimage/cifilter-swift.class/whitepointadjust())

#### Protocols

- [CIColorAbsoluteDifference](/documentation/coreimage/cicolorabsolutedifference)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorabsolutedifference/inputimage)
- [var inputImage2: CIImage?](/documentation/coreimage/cicolorabsolutedifference/inputimage2)
- [CIColorClamp](/documentation/coreimage/cicolorclamp)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorclamp/inputimage)
- [var maxComponents: CIVector](/documentation/coreimage/cicolorclamp/maxcomponents)
- [var minComponents: CIVector](/documentation/coreimage/cicolorclamp/mincomponents)
- [CIColorControls](/documentation/coreimage/cicolorcontrols)

##### Instance Properties

- [var brightness: Float](/documentation/coreimage/cicolorcontrols/brightness)
- [var contrast: Float](/documentation/coreimage/cicolorcontrols/contrast)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcontrols/inputimage)
- [var saturation: Float](/documentation/coreimage/cicolorcontrols/saturation)
- [CIColorMatrix](/documentation/coreimage/cicolormatrix)

##### Instance Properties

- [var aVector: CIVector](/documentation/coreimage/cicolormatrix/avector)
- [var bVector: CIVector](/documentation/coreimage/cicolormatrix/bvector)
- [var gVector: CIVector](/documentation/coreimage/cicolormatrix/gvector)
- [var rVector: CIVector](/documentation/coreimage/cicolormatrix/rvector)
- [var biasVector: CIVector](/documentation/coreimage/cicolormatrix/biasvector)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormatrix/inputimage)
- [CIColorPolynomial](/documentation/coreimage/cicolorpolynomial)

##### Instance Properties

- [var alphaCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/alphacoefficients)
- [var blueCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/bluecoefficients)
- [var greenCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/greencoefficients)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorpolynomial/inputimage)
- [var redCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/redcoefficients)
- [CIColorThreshold](/documentation/coreimage/cicolorthreshold)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorthreshold/inputimage)
- [var threshold: Float](/documentation/coreimage/cicolorthreshold/threshold)
- [CIColorThresholdOtsu](/documentation/coreimage/cicolorthresholdotsu)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorthresholdotsu/inputimage)
- [CIDepthToDisparity](/documentation/coreimage/cidepthtodisparity)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidepthtodisparity/inputimage)
- [CIDisparityToDepth](/documentation/coreimage/cidisparitytodepth)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidisparitytodepth/inputimage)
- [CIExposureAdjust](/documentation/coreimage/ciexposureadjust)

##### Instance Properties

- [var ev: Float](/documentation/coreimage/ciexposureadjust/ev)
- [var inputImage: CIImage?](/documentation/coreimage/ciexposureadjust/inputimage)
- [CIGammaAdjust](/documentation/coreimage/cigammaadjust)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigammaadjust/inputimage)
- [var power: Float](/documentation/coreimage/cigammaadjust/power)
- [CIHueAdjust](/documentation/coreimage/cihueadjust)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cihueadjust/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cihueadjust/inputimage)
- [CILinearToSRGBToneCurve](/documentation/coreimage/cilineartosrgbtonecurve)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cilineartosrgbtonecurve/inputimage)
- [CISRGBToneCurveToLinear](/documentation/coreimage/cisrgbtonecurvetolinear)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisrgbtonecurvetolinear/inputimage)
- [CISystemToneMap](/documentation/coreimage/cisystemtonemap)

##### Instance Properties

- [var displayHeadroom: Float](/documentation/coreimage/cisystemtonemap/displayheadroom)
- [var inputImage: CIImage?](/documentation/coreimage/cisystemtonemap/inputimage)
- [var preferredDynamicRange: CIDynamicRangeOption?](/documentation/coreimage/cisystemtonemap/preferreddynamicrange)
- [CITemperatureAndTint](/documentation/coreimage/citemperatureandtint)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citemperatureandtint/inputimage)
- [var neutral: CIVector](/documentation/coreimage/citemperatureandtint/neutral)
- [var targetNeutral: CIVector](/documentation/coreimage/citemperatureandtint/targetneutral)
- [CIToneCurve](/documentation/coreimage/citonecurve)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citonecurve/inputimage)
- [var point0: CGPoint](/documentation/coreimage/citonecurve/point0)
- [var point1: CGPoint](/documentation/coreimage/citonecurve/point1)
- [var point2: CGPoint](/documentation/coreimage/citonecurve/point2)
- [var point3: CGPoint](/documentation/coreimage/citonecurve/point3)
- [var point4: CGPoint](/documentation/coreimage/citonecurve/point4)
- [var extrapolate: Bool](/documentation/coreimage/citonecurve/extrapolate)
- [CIVibrance](/documentation/coreimage/civibrance)

##### Instance Properties

- [var amount: Float](/documentation/coreimage/civibrance/amount)
- [var inputImage: CIImage?](/documentation/coreimage/civibrance/inputimage)
- [CIWhitePointAdjust](/documentation/coreimage/ciwhitepointadjust)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciwhitepointadjust/color)
- [var inputImage: CIImage?](/documentation/coreimage/ciwhitepointadjust/inputimage)
- [Color Effect Filters](/documentation/coreimage/color-effect-filters)

#### Color Effect Filters

- [class func colorCrossPolynomial() -> any CIFilter & CIColorCrossPolynomial](/documentation/coreimage/cifilter-swift.class/colorcrosspolynomial())
- [class func colorCube() -> any CIFilter & CIColorCube](/documentation/coreimage/cifilter-swift.class/colorcube())
- [class func colorCubeWithColorSpace() -> any CIFilter & CIColorCubeWithColorSpace](/documentation/coreimage/cifilter-swift.class/colorcubewithcolorspace())
- [class func colorCubesMixedWithMask() -> any CIFilter & CIColorCubesMixedWithMask](/documentation/coreimage/cifilter-swift.class/colorcubesmixedwithmask())
- [class func colorCurves() -> any CIFilter & CIColorCurves](/documentation/coreimage/cifilter-swift.class/colorcurves())
- [class func colorInvert() -> any CIFilter & CIColorInvert](/documentation/coreimage/cifilter-swift.class/colorinvert())
- [class func colorMap() -> any CIFilter & CIColorMap](/documentation/coreimage/cifilter-swift.class/colormap())
- [class func colorMonochrome() -> any CIFilter & CIColorMonochrome](/documentation/coreimage/cifilter-swift.class/colormonochrome())
- [class func colorPosterize() -> any CIFilter & CIColorPosterize](/documentation/coreimage/cifilter-swift.class/colorposterize())
- [class func convertLabToRGB() -> any CIFilter & CIConvertLab](/documentation/coreimage/cifilter-swift.class/convertlabtorgb())
- [class func convertRGBtoLab() -> any CIFilter & CIConvertLab](/documentation/coreimage/cifilter-swift.class/convertrgbtolab())
- [class func dither() -> any CIFilter & CIDither](/documentation/coreimage/cifilter-swift.class/dither())
- [class func documentEnhancer() -> any CIFilter & CIDocumentEnhancer](/documentation/coreimage/cifilter-swift.class/documentenhancer())
- [class func falseColor() -> any CIFilter & CIFalseColor](/documentation/coreimage/cifilter-swift.class/falsecolor())
- [class func labDeltaE() -> any CIFilter & CILabDeltaE](/documentation/coreimage/cifilter-swift.class/labdeltae())
- [class func maskToAlpha() -> any CIFilter & CIMaskToAlpha](/documentation/coreimage/cifilter-swift.class/masktoalpha())
- [class func maximumComponent() -> any CIFilter & CIMaximumComponent](/documentation/coreimage/cifilter-swift.class/maximumcomponent())
- [class func minimumComponent() -> any CIFilter & CIMinimumComponent](/documentation/coreimage/cifilter-swift.class/minimumcomponent())
- [class func paletteCentroid() -> any CIFilter & CIPaletteCentroid](/documentation/coreimage/cifilter-swift.class/palettecentroid())
- [class func palettize() -> any CIFilter & CIPalettize](/documentation/coreimage/cifilter-swift.class/palettize())
- [class func photoEffectChrome() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectchrome())
- [class func photoEffectFade() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectfade())
- [class func photoEffectInstant() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectinstant())
- [class func photoEffectMono() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectmono())
- [class func photoEffectNoir() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectnoir())
- [class func photoEffectProcess() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectprocess())
- [class func photoEffectTonal() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffecttonal())
- [class func photoEffectTransfer() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffecttransfer())
- [class func sepiaTone() -> any CIFilter & CISepiaTone](/documentation/coreimage/cifilter-swift.class/sepiatone())
- [class func thermal() -> any CIFilter & CIThermal](/documentation/coreimage/cifilter-swift.class/thermal())
- [class func vignette() -> any CIFilter & CIVignette](/documentation/coreimage/cifilter-swift.class/vignette())
- [class func vignetteEffect() -> any CIFilter & CIVignetteEffect](/documentation/coreimage/cifilter-swift.class/vignetteeffect())
- [class func xRay() -> any CIFilter & CIXRay](/documentation/coreimage/cifilter-swift.class/xray())

#### Protocols

- [CIColorCrossPolynomial](/documentation/coreimage/cicolorcrosspolynomial)

##### Instance Properties

- [var blueCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/bluecoefficients)
- [var greenCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/greencoefficients)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcrosspolynomial/inputimage)
- [var redCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/redcoefficients)
- [CIColorCube](/documentation/coreimage/cicolorcube)

##### Instance Properties

- [var cubeData: Data](/documentation/coreimage/cicolorcube/cubedata)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcube/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcube/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcube/extrapolate)
- [CIColorCubeWithColorSpace](/documentation/coreimage/cicolorcubewithcolorspace)

##### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcubewithcolorspace/colorspace)
- [var cubeData: Data](/documentation/coreimage/cicolorcubewithcolorspace/cubedata)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcubewithcolorspace/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcubewithcolorspace/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcubewithcolorspace/extrapolate)
- [CIColorCubesMixedWithMask](/documentation/coreimage/cicolorcubesmixedwithmask)

##### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcubesmixedwithmask/colorspace)
- [var cube0Data: Data](/documentation/coreimage/cicolorcubesmixedwithmask/cube0data)
- [var cube1Data: Data](/documentation/coreimage/cicolorcubesmixedwithmask/cube1data)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcubesmixedwithmask/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcubesmixedwithmask/inputimage)
- [var maskImage: CIImage?](/documentation/coreimage/cicolorcubesmixedwithmask/maskimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcubesmixedwithmask/extrapolate)
- [CIColorCurves](/documentation/coreimage/cicolorcurves)

##### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcurves/colorspace)
- [var curvesData: Data](/documentation/coreimage/cicolorcurves/curvesdata)
- [var curvesDomain: CIVector](/documentation/coreimage/cicolorcurves/curvesdomain)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcurves/inputimage)
- [CIColorInvert](/documentation/coreimage/cicolorinvert)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorinvert/inputimage)
- [CIColorMap](/documentation/coreimage/cicolormap)

##### Instance Properties

- [var gradientImage: CIImage?](/documentation/coreimage/cicolormap/gradientimage)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormap/inputimage)
- [CIColorMonochrome](/documentation/coreimage/cicolormonochrome)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/cicolormonochrome/color)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormonochrome/inputimage)
- [var intensity: Float](/documentation/coreimage/cicolormonochrome/intensity)
- [CIConvertLab](/documentation/coreimage/ciconvertlab)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciconvertlab/inputimage)
- [var normalize: Bool](/documentation/coreimage/ciconvertlab/normalize)
- [CIDither](/documentation/coreimage/cidither)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidither/inputimage)
- [var intensity: Float](/documentation/coreimage/cidither/intensity)
- [CIColorPosterize](/documentation/coreimage/cicolorposterize)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorposterize/inputimage)
- [var levels: Float](/documentation/coreimage/cicolorposterize/levels)
- [CIDocumentEnhancer](/documentation/coreimage/cidocumentenhancer)

##### Instance Properties

- [var amount: Float](/documentation/coreimage/cidocumentenhancer/amount)
- [var inputImage: CIImage?](/documentation/coreimage/cidocumentenhancer/inputimage)
- [CIFalseColor](/documentation/coreimage/cifalsecolor)

##### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cifalsecolor/color0)
- [var color1: CIColor](/documentation/coreimage/cifalsecolor/color1)
- [var inputImage: CIImage?](/documentation/coreimage/cifalsecolor/inputimage)
- [CILabDeltaE](/documentation/coreimage/cilabdeltae)

##### Instance Properties

- [var image2: CIImage?](/documentation/coreimage/cilabdeltae/image2)
- [var inputImage: CIImage?](/documentation/coreimage/cilabdeltae/inputimage)
- [CIMaskToAlpha](/documentation/coreimage/cimasktoalpha)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimasktoalpha/inputimage)
- [CIMaximumComponent](/documentation/coreimage/cimaximumcomponent)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimaximumcomponent/inputimage)
- [CIMinimumComponent](/documentation/coreimage/ciminimumcomponent)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciminimumcomponent/inputimage)
- [CIPaletteCentroid](/documentation/coreimage/cipalettecentroid)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipalettecentroid/inputimage)
- [var paletteImage: CIImage?](/documentation/coreimage/cipalettecentroid/paletteimage)
- [var perceptual: Bool](/documentation/coreimage/cipalettecentroid/perceptual)
- [CIPalettize](/documentation/coreimage/cipalettize)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipalettize/inputimage)
- [var paletteImage: CIImage?](/documentation/coreimage/cipalettize/paletteimage)
- [var perceptual: Bool](/documentation/coreimage/cipalettize/perceptual)
- [CIPhotoEffect](/documentation/coreimage/ciphotoeffect)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciphotoeffect/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/ciphotoeffect/extrapolate)
- [CISepiaTone](/documentation/coreimage/cisepiatone)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisepiatone/inputimage)
- [var intensity: Float](/documentation/coreimage/cisepiatone/intensity)
- [CIThermal](/documentation/coreimage/cithermal)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cithermal/inputimage)
- [CIVignette](/documentation/coreimage/civignette)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/civignette/inputimage)
- [var intensity: Float](/documentation/coreimage/civignette/intensity)
- [var radius: Float](/documentation/coreimage/civignette/radius)
- [CIVignetteEffect](/documentation/coreimage/civignetteeffect)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/civignetteeffect/center)
- [var falloff: Float](/documentation/coreimage/civignetteeffect/falloff)
- [var inputImage: CIImage?](/documentation/coreimage/civignetteeffect/inputimage)
- [var intensity: Float](/documentation/coreimage/civignetteeffect/intensity)
- [var radius: Float](/documentation/coreimage/civignetteeffect/radius)
- [CIXRay](/documentation/coreimage/cixray)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cixray/inputimage)
- [Composite Operations](/documentation/coreimage/composite-operations)

#### Filters

- [class func additionCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/additioncompositing())
- [class func colorBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colorblendmode())
- [class func colorBurnBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colorburnblendmode())
- [class func colorDodgeBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colordodgeblendmode())
- [class func darkenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/darkenblendmode())
- [class func differenceBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/differenceblendmode())
- [class func divideBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/divideblendmode())
- [class func exclusionBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/exclusionblendmode())
- [class func hardLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/hardlightblendmode())
- [class func hueBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/hueblendmode())
- [class func lightenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/lightenblendmode())
- [class func linearBurnBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/linearburnblendmode())
- [class func linearDodgeBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/lineardodgeblendmode())
- [class func linearLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/linearlightblendmode())
- [class func luminosityBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/luminosityblendmode())
- [class func minimumCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/minimumcompositing())
- [class func maximumCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/maximumcompositing())
- [class func multiplyBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/multiplyblendmode())
- [class func multiplyCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/multiplycompositing())
- [class func overlayBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/overlayblendmode())
- [class func pinLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/pinlightblendmode())
- [class func saturationBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/saturationblendmode())
- [class func screenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/screenblendmode())
- [class func softLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/softlightblendmode())
- [class func sourceAtopCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceatopcompositing())
- [class func sourceInCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceincompositing())
- [class func sourceOutCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceoutcompositing())
- [class func sourceOverCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceovercompositing())
- [class func subtractBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/subtractblendmode())
- [class func vividLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/vividlightblendmode())

#### Protocols

- [CICompositeOperation](/documentation/coreimage/cicompositeoperation)

##### Instance Properties

- [var backgroundImage: CIImage?](/documentation/coreimage/cicompositeoperation/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/cicompositeoperation/inputimage)
- [Convolution Filters](/documentation/coreimage/convolution-filters)

#### Filters

- [class func convolution3X3() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution3x3())
- [class func convolution5X5() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution5x5())
- [class func convolution7X7() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution7x7())
- [class func convolution9Horizontal() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution9horizontal())
- [class func convolution9Vertical() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution9vertical())
- [class func convolutionRGB3X3() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb3x3())
- [class func convolutionRGB5X5() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb5x5())
- [class func convolutionRGB7X7() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb7x7())
- [class func convolutionRGB9Horizontal() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb9horizontal())
- [class func convolutionRGB9Vertical() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb9vertical())

#### Protocols

- [CIConvolution](/documentation/coreimage/ciconvolution)

##### Instance Properties

- [var bias: Float](/documentation/coreimage/ciconvolution/bias)
- [var inputImage: CIImage?](/documentation/coreimage/ciconvolution/inputimage)
- [var weights: CIVector](/documentation/coreimage/ciconvolution/weights)
- [Distortion Filters](/documentation/coreimage/distortion-filters)

#### Filters

- [class func bumpDistortion() -> any CIFilter & CIBumpDistortion](/documentation/coreimage/cifilter-swift.class/bumpdistortion())
- [class func bumpDistortionLinear() -> any CIFilter & CIBumpDistortionLinear](/documentation/coreimage/cifilter-swift.class/bumpdistortionlinear())
- [class func circleSplashDistortion() -> any CIFilter & CICircleSplashDistortion](/documentation/coreimage/cifilter-swift.class/circlesplashdistortion())
- [class func circularWrap() -> any CIFilter & CICircularWrap](/documentation/coreimage/cifilter-swift.class/circularwrap())
- [class func displacementDistortion() -> any CIFilter & CIDisplacementDistortion](/documentation/coreimage/cifilter-swift.class/displacementdistortion())
- [class func droste() -> any CIFilter & CIDroste](/documentation/coreimage/cifilter-swift.class/droste())
- [class func glassDistortion() -> any CIFilter & CIGlassDistortion](/documentation/coreimage/cifilter-swift.class/glassdistortion())
- [class func glassLozenge() -> any CIFilter & CIGlassLozenge](/documentation/coreimage/cifilter-swift.class/glasslozenge())
- [class func holeDistortion() -> any CIFilter & CIHoleDistortion](/documentation/coreimage/cifilter-swift.class/holedistortion())
- [class func lightTunnel() -> any CIFilter & CILightTunnel](/documentation/coreimage/cifilter-swift.class/lighttunnel())
- [class func ninePartStretched() -> any CIFilter & CINinePartStretched](/documentation/coreimage/cifilter-swift.class/ninepartstretched())
- [class func ninePartTiled() -> any CIFilter & CINinePartTiled](/documentation/coreimage/cifilter-swift.class/nineparttiled())
- [class func pinchDistortion() -> any CIFilter & CIPinchDistortion](/documentation/coreimage/cifilter-swift.class/pinchdistortion())
- [class func stretchCrop() -> any CIFilter & CIStretchCrop](/documentation/coreimage/cifilter-swift.class/stretchcrop())
- [class func torusLensDistortion() -> any CIFilter & CITorusLensDistortion](/documentation/coreimage/cifilter-swift.class/toruslensdistortion())
- [class func twirlDistortion() -> any CIFilter & CITwirlDistortion](/documentation/coreimage/cifilter-swift.class/twirldistortion())
- [class func vortexDistortion() -> any CIFilter & CIVortexDistortion](/documentation/coreimage/cifilter-swift.class/vortexdistortion())

#### Protocols

- [CIBumpDistortion](/documentation/coreimage/cibumpdistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cibumpdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cibumpdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cibumpdistortion/radius)
- [var scale: Float](/documentation/coreimage/cibumpdistortion/scale)
- [CIBumpDistortionLinear](/documentation/coreimage/cibumpdistortionlinear)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cibumpdistortionlinear/angle)
- [var center: CGPoint](/documentation/coreimage/cibumpdistortionlinear/center)
- [var inputImage: CIImage?](/documentation/coreimage/cibumpdistortionlinear/inputimage)
- [var radius: Float](/documentation/coreimage/cibumpdistortionlinear/radius)
- [var scale: Float](/documentation/coreimage/cibumpdistortionlinear/scale)
- [CICircleSplashDistortion](/documentation/coreimage/cicirclesplashdistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicirclesplashdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicirclesplashdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cicirclesplashdistortion/radius)
- [CICircularWrap](/documentation/coreimage/cicircularwrap)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cicircularwrap/angle)
- [var center: CGPoint](/documentation/coreimage/cicircularwrap/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicircularwrap/inputimage)
- [var radius: Float](/documentation/coreimage/cicircularwrap/radius)
- [CIDisplacementDistortion](/documentation/coreimage/cidisplacementdistortion)

##### Instance Properties

- [var displacementImage: CIImage?](/documentation/coreimage/cidisplacementdistortion/displacementimage)
- [var inputImage: CIImage?](/documentation/coreimage/cidisplacementdistortion/inputimage)
- [var scale: Float](/documentation/coreimage/cidisplacementdistortion/scale)
- [CIDroste](/documentation/coreimage/cidroste)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidroste/inputimage)
- [var insetPoint0: CGPoint](/documentation/coreimage/cidroste/insetpoint0)
- [var insetPoint1: CGPoint](/documentation/coreimage/cidroste/insetpoint1)
- [var periodicity: Float](/documentation/coreimage/cidroste/periodicity)
- [var rotation: Float](/documentation/coreimage/cidroste/rotation)
- [var strands: Float](/documentation/coreimage/cidroste/strands)
- [var zoom: Float](/documentation/coreimage/cidroste/zoom)
- [CIGlassDistortion](/documentation/coreimage/ciglassdistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciglassdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciglassdistortion/inputimage)
- [var scale: Float](/documentation/coreimage/ciglassdistortion/scale)
- [var textureImage: CIImage?](/documentation/coreimage/ciglassdistortion/textureimage)
- [CIGlassLozenge](/documentation/coreimage/ciglasslozenge)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciglasslozenge/inputimage)
- [var point0: CGPoint](/documentation/coreimage/ciglasslozenge/point0)
- [var point1: CGPoint](/documentation/coreimage/ciglasslozenge/point1)
- [var radius: Float](/documentation/coreimage/ciglasslozenge/radius)
- [var refraction: Float](/documentation/coreimage/ciglasslozenge/refraction)
- [CIHoleDistortion](/documentation/coreimage/ciholedistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciholedistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciholedistortion/inputimage)
- [var radius: Float](/documentation/coreimage/ciholedistortion/radius)
- [CILightTunnel](/documentation/coreimage/cilighttunnel)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cilighttunnel/center)
- [var inputImage: CIImage?](/documentation/coreimage/cilighttunnel/inputimage)
- [var radius: Float](/documentation/coreimage/cilighttunnel/radius)
- [var rotation: Float](/documentation/coreimage/cilighttunnel/rotation)
- [CINinePartStretched](/documentation/coreimage/cininepartstretched)

##### Instance Properties

- [var breakpoint0: CGPoint](/documentation/coreimage/cininepartstretched/breakpoint0)
- [var breakpoint1: CGPoint](/documentation/coreimage/cininepartstretched/breakpoint1)
- [var growAmount: CGPoint](/documentation/coreimage/cininepartstretched/growamount)
- [var inputImage: CIImage?](/documentation/coreimage/cininepartstretched/inputimage)
- [CINinePartTiled](/documentation/coreimage/cinineparttiled)

##### Instance Properties

- [var breakpoint0: CGPoint](/documentation/coreimage/cinineparttiled/breakpoint0)
- [var breakpoint1: CGPoint](/documentation/coreimage/cinineparttiled/breakpoint1)
- [var flipYTiles: Bool](/documentation/coreimage/cinineparttiled/flipytiles)
- [var growAmount: CGPoint](/documentation/coreimage/cinineparttiled/growamount)
- [var inputImage: CIImage?](/documentation/coreimage/cinineparttiled/inputimage)
- [CIPinchDistortion](/documentation/coreimage/cipinchdistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipinchdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipinchdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cipinchdistortion/radius)
- [var scale: Float](/documentation/coreimage/cipinchdistortion/scale)
- [CIStretchCrop](/documentation/coreimage/cistretchcrop)

##### Instance Properties

- [var centerStretchAmount: Float](/documentation/coreimage/cistretchcrop/centerstretchamount)
- [var cropAmount: Float](/documentation/coreimage/cistretchcrop/cropamount)
- [var inputImage: CIImage?](/documentation/coreimage/cistretchcrop/inputimage)
- [var size: CGPoint](/documentation/coreimage/cistretchcrop/size)
- [CITorusLensDistortion](/documentation/coreimage/citoruslensdistortion)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/citoruslensdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/citoruslensdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/citoruslensdistortion/radius)
- [var refraction: Float](/documentation/coreimage/citoruslensdistortion/refraction)
- [var width: Float](/documentation/coreimage/citoruslensdistortion/width)
- [CITwirlDistortion](/documentation/coreimage/citwirldistortion)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/citwirldistortion/angle)
- [var center: CGPoint](/documentation/coreimage/citwirldistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/citwirldistortion/inputimage)
- [var radius: Float](/documentation/coreimage/citwirldistortion/radius)
- [CIVortexDistortion](/documentation/coreimage/civortexdistortion)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/civortexdistortion/angle)
- [var center: CGPoint](/documentation/coreimage/civortexdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/civortexdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/civortexdistortion/radius)
- [Generator Filters](/documentation/coreimage/generator-filters)

#### Filters

- [class func attributedTextImageGenerator() -> any CIFilter & CIAttributedTextImageGenerator](/documentation/coreimage/cifilter-swift.class/attributedtextimagegenerator())
- [class func aztecCodeGenerator() -> any CIFilter & CIAztecCodeGenerator](/documentation/coreimage/cifilter-swift.class/azteccodegenerator())
- [class func barcodeGenerator() -> any CIFilter & CIBarcodeGenerator](/documentation/coreimage/cifilter-swift.class/barcodegenerator())
- [class func blurredRectangleGenerator() -> any CIFilter & CIBlurredRectangleGenerator](/documentation/coreimage/cifilter-swift.class/blurredrectanglegenerator())
- [class func checkerboardGenerator() -> any CIFilter & CICheckerboardGenerator](/documentation/coreimage/cifilter-swift.class/checkerboardgenerator())
- [class func code128BarcodeGenerator() -> any CIFilter & CICode128BarcodeGenerator](/documentation/coreimage/cifilter-swift.class/code128barcodegenerator())
- [class func lenticularHaloGenerator() -> any CIFilter & CILenticularHaloGenerator](/documentation/coreimage/cifilter-swift.class/lenticularhalogenerator())
- [class func meshGenerator() -> any CIFilter & CIMeshGenerator](/documentation/coreimage/cifilter-swift.class/meshgenerator())
- [class func pdf417BarcodeGenerator() -> any CIFilter & CIPDF417BarcodeGenerator](/documentation/coreimage/cifilter-swift.class/pdf417barcodegenerator())
- [class func qrCodeGenerator() -> any CIFilter & CIQRCodeGenerator](/documentation/coreimage/cifilter-swift.class/qrcodegenerator())
- [class func randomGenerator() -> any CIFilter & CIRandomGenerator](/documentation/coreimage/cifilter-swift.class/randomgenerator())
- [class func roundedRectangleGenerator() -> any CIFilter & CIRoundedRectangleGenerator](/documentation/coreimage/cifilter-swift.class/roundedrectanglegenerator())
- [class func roundedRectangleStrokeGenerator() -> any CIFilter & CIRoundedRectangleStrokeGenerator](/documentation/coreimage/cifilter-swift.class/roundedrectanglestrokegenerator())
- [class func starShineGenerator() -> any CIFilter & CIStarShineGenerator](/documentation/coreimage/cifilter-swift.class/starshinegenerator())
- [class func stripesGenerator() -> any CIFilter & CIStripesGenerator](/documentation/coreimage/cifilter-swift.class/stripesgenerator())
- [class func sunbeamsGenerator() -> any CIFilter & CISunbeamsGenerator](/documentation/coreimage/cifilter-swift.class/sunbeamsgenerator())
- [class func textImageGenerator() -> any CIFilter & CITextImageGenerator](/documentation/coreimage/cifilter-swift.class/textimagegenerator())

#### Protocols

- [CICode128BarcodeGenerator](/documentation/coreimage/cicode128barcodegenerator)

##### Instance Properties

- [var barcodeHeight: Float](/documentation/coreimage/cicode128barcodegenerator/barcodeheight)
- [var message: Data](/documentation/coreimage/cicode128barcodegenerator/message)
- [var quietSpace: Float](/documentation/coreimage/cicode128barcodegenerator/quietspace)
- [CIAttributedTextImageGenerator](/documentation/coreimage/ciattributedtextimagegenerator)

##### Instance Properties

- [var scaleFactor: Float](/documentation/coreimage/ciattributedtextimagegenerator/scalefactor)
- [var text: NSAttributedString](/documentation/coreimage/ciattributedtextimagegenerator/text)
- [var padding: Float](/documentation/coreimage/ciattributedtextimagegenerator/padding)
- [CIAztecCodeGenerator](/documentation/coreimage/ciazteccodegenerator)

##### Instance Properties

- [var compactStyle: Float](/documentation/coreimage/ciazteccodegenerator/compactstyle)
- [var correctionLevel: Float](/documentation/coreimage/ciazteccodegenerator/correctionlevel)
- [var layers: Float](/documentation/coreimage/ciazteccodegenerator/layers)
- [var message: Data](/documentation/coreimage/ciazteccodegenerator/message)
- [CIBarcodeGenerator](/documentation/coreimage/cibarcodegenerator)

##### Instance Properties

- [var barcodeDescriptor: CIBarcodeDescriptor](/documentation/coreimage/cibarcodegenerator/barcodedescriptor)
- [CIBlurredRectangleGenerator](/documentation/coreimage/ciblurredrectanglegenerator)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciblurredrectanglegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciblurredrectanglegenerator/extent)
- [var sigma: Float](/documentation/coreimage/ciblurredrectanglegenerator/sigma)
- [CIRoundedRectangleStrokeGenerator](/documentation/coreimage/ciroundedrectanglestrokegenerator)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglestrokegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglestrokegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/radius)
- [var width: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/width)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/smoothness)
- [CICheckerboardGenerator](/documentation/coreimage/cicheckerboardgenerator)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicheckerboardgenerator/center)
- [var color0: CIColor](/documentation/coreimage/cicheckerboardgenerator/color0)
- [var color1: CIColor](/documentation/coreimage/cicheckerboardgenerator/color1)
- [var sharpness: Float](/documentation/coreimage/cicheckerboardgenerator/sharpness)
- [var width: Float](/documentation/coreimage/cicheckerboardgenerator/width)
- [CILenticularHaloGenerator](/documentation/coreimage/cilenticularhalogenerator)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cilenticularhalogenerator/center)
- [var color: CIColor](/documentation/coreimage/cilenticularhalogenerator/color)
- [var haloOverlap: Float](/documentation/coreimage/cilenticularhalogenerator/halooverlap)
- [var haloRadius: Float](/documentation/coreimage/cilenticularhalogenerator/haloradius)
- [var haloWidth: Float](/documentation/coreimage/cilenticularhalogenerator/halowidth)
- [var striationContrast: Float](/documentation/coreimage/cilenticularhalogenerator/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/cilenticularhalogenerator/striationstrength)
- [var time: Float](/documentation/coreimage/cilenticularhalogenerator/time)
- [CIMeshGenerator](/documentation/coreimage/cimeshgenerator)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/cimeshgenerator/color)
- [var mesh: [Any]](/documentation/coreimage/cimeshgenerator/mesh)
- [var width: Float](/documentation/coreimage/cimeshgenerator/width)
- [CIPDF417BarcodeGenerator](/documentation/coreimage/cipdf417barcodegenerator)

##### Instance Properties

- [var alwaysSpecifyCompaction: Float](/documentation/coreimage/cipdf417barcodegenerator/alwaysspecifycompaction)
- [var compactStyle: Float](/documentation/coreimage/cipdf417barcodegenerator/compactstyle)
- [var compactionMode: Float](/documentation/coreimage/cipdf417barcodegenerator/compactionmode)
- [var correctionLevel: Float](/documentation/coreimage/cipdf417barcodegenerator/correctionlevel)
- [var dataColumns: Float](/documentation/coreimage/cipdf417barcodegenerator/datacolumns)
- [var maxHeight: Float](/documentation/coreimage/cipdf417barcodegenerator/maxheight)
- [var maxWidth: Float](/documentation/coreimage/cipdf417barcodegenerator/maxwidth)
- [var message: Data](/documentation/coreimage/cipdf417barcodegenerator/message)
- [var minHeight: Float](/documentation/coreimage/cipdf417barcodegenerator/minheight)
- [var minWidth: Float](/documentation/coreimage/cipdf417barcodegenerator/minwidth)
- [var preferredAspectRatio: Float](/documentation/coreimage/cipdf417barcodegenerator/preferredaspectratio)
- [var rows: Float](/documentation/coreimage/cipdf417barcodegenerator/rows)
- [CIQRCodeGenerator](/documentation/coreimage/ciqrcodegenerator)

##### Instance Properties

- [var correctionLevel: String](/documentation/coreimage/ciqrcodegenerator/correctionlevel)
- [var message: Data](/documentation/coreimage/ciqrcodegenerator/message)
- [CIRandomGenerator](/documentation/coreimage/cirandomgenerator)
- [CIRoundedRectangleGenerator](/documentation/coreimage/ciroundedrectanglegenerator)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglegenerator/radius)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglegenerator/smoothness)
- [CIRoundedRectangleStrokeGenerator](/documentation/coreimage/ciroundedrectanglestrokegenerator)

##### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglestrokegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglestrokegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/radius)
- [var width: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/width)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/smoothness)
- [CIStarShineGenerator](/documentation/coreimage/cistarshinegenerator)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cistarshinegenerator/center)
- [var color: CIColor](/documentation/coreimage/cistarshinegenerator/color)
- [var crossAngle: Float](/documentation/coreimage/cistarshinegenerator/crossangle)
- [var crossOpacity: Float](/documentation/coreimage/cistarshinegenerator/crossopacity)
- [var crossScale: Float](/documentation/coreimage/cistarshinegenerator/crossscale)
- [var crossWidth: Float](/documentation/coreimage/cistarshinegenerator/crosswidth)
- [var epsilon: Float](/documentation/coreimage/cistarshinegenerator/epsilon)
- [var radius: Float](/documentation/coreimage/cistarshinegenerator/radius)
- [CIStripesGenerator](/documentation/coreimage/cistripesgenerator)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cistripesgenerator/center)
- [var color0: CIColor](/documentation/coreimage/cistripesgenerator/color0)
- [var color1: CIColor](/documentation/coreimage/cistripesgenerator/color1)
- [var sharpness: Float](/documentation/coreimage/cistripesgenerator/sharpness)
- [var width: Float](/documentation/coreimage/cistripesgenerator/width)
- [CISunbeamsGenerator](/documentation/coreimage/cisunbeamsgenerator)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cisunbeamsgenerator/center)
- [var color: CIColor](/documentation/coreimage/cisunbeamsgenerator/color)
- [var maxStriationRadius: Float](/documentation/coreimage/cisunbeamsgenerator/maxstriationradius)
- [var striationContrast: Float](/documentation/coreimage/cisunbeamsgenerator/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/cisunbeamsgenerator/striationstrength)
- [var sunRadius: Float](/documentation/coreimage/cisunbeamsgenerator/sunradius)
- [var time: Float](/documentation/coreimage/cisunbeamsgenerator/time)
- [CITextImageGenerator](/documentation/coreimage/citextimagegenerator)

##### Instance Properties

- [var fontName: String](/documentation/coreimage/citextimagegenerator/fontname)
- [var fontSize: Float](/documentation/coreimage/citextimagegenerator/fontsize)
- [var scaleFactor: Float](/documentation/coreimage/citextimagegenerator/scalefactor)
- [var text: String](/documentation/coreimage/citextimagegenerator/text)
- [var padding: Float](/documentation/coreimage/citextimagegenerator/padding)
- [Geometry Adjustment Filters](/documentation/coreimage/geometry-adjustment-filters)

#### Filters

- [class func bicubicScaleTransform() -> any CIFilter & CIBicubicScaleTransform](/documentation/coreimage/cifilter-swift.class/bicubicscaletransform())
- [class func edgePreserveUpsample() -> any CIFilter & CIEdgePreserveUpsample](/documentation/coreimage/cifilter-swift.class/edgepreserveupsample())
- [class func keystoneCorrectionCombined() -> any CIFilter & CIKeystoneCorrectionCombined](/documentation/coreimage/cifilter-swift.class/keystonecorrectioncombined())
- [class func keystoneCorrectionHorizontal() -> any CIFilter & CIKeystoneCorrectionHorizontal](/documentation/coreimage/cifilter-swift.class/keystonecorrectionhorizontal())
- [class func keystoneCorrectionVertical() -> any CIFilter & CIKeystoneCorrectionVertical](/documentation/coreimage/cifilter-swift.class/keystonecorrectionvertical())
- [class func lanczosScaleTransform() -> any CIFilter & CILanczosScaleTransform](/documentation/coreimage/cifilter-swift.class/lanczosscaletransform())
- [class func perspectiveCorrection() -> any CIFilter & CIPerspectiveCorrection](/documentation/coreimage/cifilter-swift.class/perspectivecorrection())
- [class func perspectiveRotate() -> any CIFilter & CIPerspectiveRotate](/documentation/coreimage/cifilter-swift.class/perspectiverotate())
- [class func perspectiveTransform() -> any CIFilter & CIPerspectiveTransform](/documentation/coreimage/cifilter-swift.class/perspectivetransform())
- [class func perspectiveTransformWithExtent() -> any CIFilter & CIPerspectiveTransformWithExtent](/documentation/coreimage/cifilter-swift.class/perspectivetransformwithextent())
- [class func straighten() -> any CIFilter & CIStraighten](/documentation/coreimage/cifilter-swift.class/straighten())

#### Protocols

- [CIBicubicScaleTransform](/documentation/coreimage/cibicubicscaletransform)

##### Instance Properties

- [var aspectRatio: Float](/documentation/coreimage/cibicubicscaletransform/aspectratio)
- [var inputImage: CIImage?](/documentation/coreimage/cibicubicscaletransform/inputimage)
- [var parameterB: Float](/documentation/coreimage/cibicubicscaletransform/parameterb)
- [var parameterC: Float](/documentation/coreimage/cibicubicscaletransform/parameterc)
- [var scale: Float](/documentation/coreimage/cibicubicscaletransform/scale)
- [CIEdgePreserveUpsample](/documentation/coreimage/ciedgepreserveupsample)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedgepreserveupsample/inputimage)
- [var lumaSigma: Float](/documentation/coreimage/ciedgepreserveupsample/lumasigma)
- [var smallImage: CIImage?](/documentation/coreimage/ciedgepreserveupsample/smallimage)
- [var spatialSigma: Float](/documentation/coreimage/ciedgepreserveupsample/spatialsigma)
- [CIFourCoordinateGeometryFilter](/documentation/coreimage/cifourcoordinategeometryfilter)

##### Instance Properties

- [var bottomLeft: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/bottomleft)
- [var bottomRight: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/bottomright)
- [var inputImage: CIImage?](/documentation/coreimage/cifourcoordinategeometryfilter/inputimage)
- [var topLeft: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/topleft)
- [var topRight: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/topright)
- [CIKeystoneCorrectionCombined](/documentation/coreimage/cikeystonecorrectioncombined)

##### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectioncombined/focallength)
- [CIKeystoneCorrectionHorizontal](/documentation/coreimage/cikeystonecorrectionhorizontal)

##### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectionhorizontal/focallength)
- [CIKeystoneCorrectionVertical](/documentation/coreimage/cikeystonecorrectionvertical)

##### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectionvertical/focallength)
- [CILanczosScaleTransform](/documentation/coreimage/cilanczosscaletransform)

##### Instance Properties

- [var aspectRatio: Float](/documentation/coreimage/cilanczosscaletransform/aspectratio)
- [var inputImage: CIImage?](/documentation/coreimage/cilanczosscaletransform/inputimage)
- [var scale: Float](/documentation/coreimage/cilanczosscaletransform/scale)
- [CIPerspectiveCorrection](/documentation/coreimage/ciperspectivecorrection)

##### Instance Properties

- [var crop: Bool](/documentation/coreimage/ciperspectivecorrection/crop)
- [CIPerspectiveRotate](/documentation/coreimage/ciperspectiverotate)

##### Instance Properties

- [var focalLength: Float](/documentation/coreimage/ciperspectiverotate/focallength)
- [var inputImage: CIImage?](/documentation/coreimage/ciperspectiverotate/inputimage)
- [var pitch: Float](/documentation/coreimage/ciperspectiverotate/pitch)
- [var roll: Float](/documentation/coreimage/ciperspectiverotate/roll)
- [var yaw: Float](/documentation/coreimage/ciperspectiverotate/yaw)
- [CIPerspectiveTransform](/documentation/coreimage/ciperspectivetransform)
- [CIPerspectiveTransformWithExtent](/documentation/coreimage/ciperspectivetransformwithextent)

##### Instance Properties

- [var extent: CGRect](/documentation/coreimage/ciperspectivetransformwithextent/extent)
- [CIStraighten](/documentation/coreimage/cistraighten)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cistraighten/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cistraighten/inputimage)
- [Gradient Filters](/documentation/coreimage/gradient-filters)

#### Filters

- [class func gaussianGradient() -> any CIFilter & CIGaussianGradient](/documentation/coreimage/cifilter-swift.class/gaussiangradient())
- [class func hueSaturationValueGradient() -> any CIFilter & CIHueSaturationValueGradient](/documentation/coreimage/cifilter-swift.class/huesaturationvaluegradient())
- [class func linearGradient() -> any CIFilter & CILinearGradient](/documentation/coreimage/cifilter-swift.class/lineargradient())
- [class func radialGradient() -> any CIFilter & CIRadialGradient](/documentation/coreimage/cifilter-swift.class/radialgradient())
- [class func smoothLinearGradient() -> any CIFilter & CISmoothLinearGradient](/documentation/coreimage/cifilter-swift.class/smoothlineargradient())

#### Protocols

- [CIGaussianGradient](/documentation/coreimage/cigaussiangradient)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cigaussiangradient/center)
- [var color0: CIColor](/documentation/coreimage/cigaussiangradient/color0)
- [var color1: CIColor](/documentation/coreimage/cigaussiangradient/color1)
- [var radius: Float](/documentation/coreimage/cigaussiangradient/radius)
- [CIHueSaturationValueGradient](/documentation/coreimage/cihuesaturationvaluegradient)

##### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cihuesaturationvaluegradient/colorspace)
- [var dither: Float](/documentation/coreimage/cihuesaturationvaluegradient/dither)
- [var radius: Float](/documentation/coreimage/cihuesaturationvaluegradient/radius)
- [var softness: Float](/documentation/coreimage/cihuesaturationvaluegradient/softness)
- [var value: Float](/documentation/coreimage/cihuesaturationvaluegradient/value)
- [CILinearGradient](/documentation/coreimage/cilineargradient)

##### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cilineargradient/color0)
- [var color1: CIColor](/documentation/coreimage/cilineargradient/color1)
- [var point0: CGPoint](/documentation/coreimage/cilineargradient/point0)
- [var point1: CGPoint](/documentation/coreimage/cilineargradient/point1)
- [CIRadialGradient](/documentation/coreimage/ciradialgradient)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciradialgradient/center)
- [var color0: CIColor](/documentation/coreimage/ciradialgradient/color0)
- [var color1: CIColor](/documentation/coreimage/ciradialgradient/color1)
- [var radius0: Float](/documentation/coreimage/ciradialgradient/radius0)
- [var radius1: Float](/documentation/coreimage/ciradialgradient/radius1)
- [CISmoothLinearGradient](/documentation/coreimage/cismoothlineargradient)

##### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cismoothlineargradient/color0)
- [var color1: CIColor](/documentation/coreimage/cismoothlineargradient/color1)
- [var point0: CGPoint](/documentation/coreimage/cismoothlineargradient/point0)
- [var point1: CGPoint](/documentation/coreimage/cismoothlineargradient/point1)
- [Halftone Effect Filters](/documentation/coreimage/halftone-effect-filters)

#### Filters

- [class func circularScreen() -> any CIFilter & CICircularScreen](/documentation/coreimage/cifilter-swift.class/circularscreen())
- [class func cmykHalftone() -> any CIFilter & CICMYKHalftone](/documentation/coreimage/cifilter-swift.class/cmykhalftone())
- [class func dotScreen() -> any CIFilter & CIDotScreen](/documentation/coreimage/cifilter-swift.class/dotscreen())
- [class func hatchedScreen() -> any CIFilter & CIHatchedScreen](/documentation/coreimage/cifilter-swift.class/hatchedscreen())
- [class func lineScreen() -> any CIFilter & CILineScreen](/documentation/coreimage/cifilter-swift.class/linescreen())

#### Protocols

- [CICircularScreen](/documentation/coreimage/cicircularscreen)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicircularscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicircularscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cicircularscreen/sharpness)
- [var width: Float](/documentation/coreimage/cicircularscreen/width)
- [CICMYKHalftone](/documentation/coreimage/cicmykhalftone)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cicmykhalftone/angle)
- [var center: CGPoint](/documentation/coreimage/cicmykhalftone/center)
- [var grayComponentReplacement: Float](/documentation/coreimage/cicmykhalftone/graycomponentreplacement)
- [var inputImage: CIImage?](/documentation/coreimage/cicmykhalftone/inputimage)
- [var sharpness: Float](/documentation/coreimage/cicmykhalftone/sharpness)
- [var underColorRemoval: Float](/documentation/coreimage/cicmykhalftone/undercolorremoval)
- [var width: Float](/documentation/coreimage/cicmykhalftone/width)
- [CIDotScreen](/documentation/coreimage/cidotscreen)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cidotscreen/angle)
- [var center: CGPoint](/documentation/coreimage/cidotscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cidotscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cidotscreen/sharpness)
- [var width: Float](/documentation/coreimage/cidotscreen/width)
- [CIHatchedScreen](/documentation/coreimage/cihatchedscreen)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cihatchedscreen/angle)
- [var center: CGPoint](/documentation/coreimage/cihatchedscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cihatchedscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cihatchedscreen/sharpness)
- [var width: Float](/documentation/coreimage/cihatchedscreen/width)
- [CILineScreen](/documentation/coreimage/cilinescreen)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cilinescreen/angle)
- [var center: CGPoint](/documentation/coreimage/cilinescreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cilinescreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cilinescreen/sharpness)
- [var width: Float](/documentation/coreimage/cilinescreen/width)
- [Reduction Filters](/documentation/coreimage/reduction-filters)

#### Filters

- [class func areaAverage() -> any CIFilter & CIAreaAverage](/documentation/coreimage/cifilter-swift.class/areaaverage())
- [class func areaHistogram() -> any CIFilter & CIAreaHistogram](/documentation/coreimage/cifilter-swift.class/areahistogram())
- [class func areaLogarithmicHistogram() -> any CIFilter & CIAreaLogarithmicHistogram](/documentation/coreimage/cifilter-swift.class/arealogarithmichistogram())
- [class func areaMaximum() -> any CIFilter & CIAreaMaximum](/documentation/coreimage/cifilter-swift.class/areamaximum())
- [class func areaMaximumAlpha() -> any CIFilter & CIAreaMaximumAlpha](/documentation/coreimage/cifilter-swift.class/areamaximumalpha())
- [class func areaMinimum() -> any CIFilter & CIAreaMinimum](/documentation/coreimage/cifilter-swift.class/areaminimum())
- [class func areaMinimumAlpha() -> any CIFilter & CIAreaMinimumAlpha](/documentation/coreimage/cifilter-swift.class/areaminimumalpha())
- [class func areaMinMax() -> any CIFilter & CIAreaMinMax](/documentation/coreimage/cifilter-swift.class/areaminmax())
- [class func areaMinMaxRed() -> any CIFilter & CIAreaMinMaxRed](/documentation/coreimage/cifilter-swift.class/areaminmaxred())
- [class func columnAverage() -> any CIFilter & CIColumnAverage](/documentation/coreimage/cifilter-swift.class/columnaverage())
- [class func histogramDisplay() -> any CIFilter & CIHistogramDisplay](/documentation/coreimage/cifilter-swift.class/histogramdisplay())
- [class func kMeans() -> any CIFilter & CIKMeans](/documentation/coreimage/cifilter-swift.class/kmeans())
- [class func rowAverage() -> any CIFilter & CIRowAverage](/documentation/coreimage/cifilter-swift.class/rowaverage())

#### Protocols

- [CIAreaAverage](/documentation/coreimage/ciareaaverage)
- [CIAreaHistogram](/documentation/coreimage/ciareahistogram)

##### Instance Properties

- [var count: Int](/documentation/coreimage/ciareahistogram/count)
- [var scale: Float](/documentation/coreimage/ciareahistogram/scale)
- [CIAreaLogarithmicHistogram](/documentation/coreimage/ciarealogarithmichistogram)

##### Instance Properties

- [var count: Int](/documentation/coreimage/ciarealogarithmichistogram/count)
- [var maximumStop: Float](/documentation/coreimage/ciarealogarithmichistogram/maximumstop)
- [var minimumStop: Float](/documentation/coreimage/ciarealogarithmichistogram/minimumstop)
- [var scale: Float](/documentation/coreimage/ciarealogarithmichistogram/scale)
- [CIAreaMaximum](/documentation/coreimage/ciareamaximum)
- [CIAreaMaximumAlpha](/documentation/coreimage/ciareamaximumalpha)
- [CIAreaMinMax](/documentation/coreimage/ciareaminmax)
- [CIAreaMinMaxRed](/documentation/coreimage/ciareaminmaxred)
- [CIAreaMinimum](/documentation/coreimage/ciareaminimum)
- [CIAreaMinimumAlpha](/documentation/coreimage/ciareaminimumalpha)
- [CIAreaReductionFilter](/documentation/coreimage/ciareareductionfilter)

##### Instance Properties

- [var extent: CGRect](/documentation/coreimage/ciareareductionfilter/extent)
- [var inputImage: CIImage?](/documentation/coreimage/ciareareductionfilter/inputimage)
- [CIColumnAverage](/documentation/coreimage/cicolumnaverage)
- [CIHistogramDisplay](/documentation/coreimage/cihistogramdisplay)

##### Instance Properties

- [var height: Float](/documentation/coreimage/cihistogramdisplay/height)
- [var highLimit: Float](/documentation/coreimage/cihistogramdisplay/highlimit)
- [var inputImage: CIImage?](/documentation/coreimage/cihistogramdisplay/inputimage)
- [var lowLimit: Float](/documentation/coreimage/cihistogramdisplay/lowlimit)
- [CIKMeans](/documentation/coreimage/cikmeans)

##### Instance Properties

- [var count: Int](/documentation/coreimage/cikmeans/count)
- [var inputMeans: CIImage?](/documentation/coreimage/cikmeans/inputmeans)
- [var passes: Float](/documentation/coreimage/cikmeans/passes)
- [var perceptual: Bool](/documentation/coreimage/cikmeans/perceptual)
- [CIRowAverage](/documentation/coreimage/cirowaverage)
- [Sharpening Filters](/documentation/coreimage/sharpening-filters)

#### Filters

- [class func sharpenLuminance() -> any CIFilter & CISharpenLuminance](/documentation/coreimage/cifilter-swift.class/sharpenluminance())
- [class func unsharpMask() -> any CIFilter & CIUnsharpMask](/documentation/coreimage/cifilter-swift.class/unsharpmask())

#### Protocols

- [CISharpenLuminance](/documentation/coreimage/cisharpenluminance)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisharpenluminance/inputimage)
- [var radius: Float](/documentation/coreimage/cisharpenluminance/radius)
- [var sharpness: Float](/documentation/coreimage/cisharpenluminance/sharpness)
- [CIUnsharpMask](/documentation/coreimage/ciunsharpmask)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciunsharpmask/inputimage)
- [var intensity: Float](/documentation/coreimage/ciunsharpmask/intensity)
- [var radius: Float](/documentation/coreimage/ciunsharpmask/radius)
- [Stylizing Filters](/documentation/coreimage/stylizing-filters)

#### Filters

- [class func blendWithAlphaMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithalphamask())
- [class func blendWithBlueMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithbluemask())
- [class func blendWithMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithmask())
- [class func blendWithRedMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithredmask())
- [class func bloom() -> any CIFilter & CIBloom](/documentation/coreimage/cifilter-swift.class/bloom())
- [class func cannyEdgeDetector() -> any CIFilter & CICannyEdgeDetector](/documentation/coreimage/cifilter-swift.class/cannyedgedetector())
- [class func comicEffect() -> any CIFilter & CIComicEffect](/documentation/coreimage/cifilter-swift.class/comiceffect())
- [class func coreMLModel() -> any CIFilter & CICoreMLModel](/documentation/coreimage/cifilter-swift.class/coremlmodel())
- [class func crystallize() -> any CIFilter & CICrystallize](/documentation/coreimage/cifilter-swift.class/crystallize())
- [class func depthOfField() -> any CIFilter & CIDepthOfField](/documentation/coreimage/cifilter-swift.class/depthoffield())
- [class func edges() -> any CIFilter & CIEdges](/documentation/coreimage/cifilter-swift.class/edges())
- [class func edgeWork() -> any CIFilter & CIEdgeWork](/documentation/coreimage/cifilter-swift.class/edgework())
- [class func gaborGradients() -> any CIFilter & CIGaborGradients](/documentation/coreimage/cifilter-swift.class/gaborgradients())
- [class func gloom() -> any CIFilter & CIGloom](/documentation/coreimage/cifilter-swift.class/gloom())
- [class func heightFieldFromMask() -> any CIFilter & CIHeightFieldFromMask](/documentation/coreimage/cifilter-swift.class/heightfieldfrommask())
- [class func hexagonalPixellate() -> any CIFilter & CIHexagonalPixellate](/documentation/coreimage/cifilter-swift.class/hexagonalpixellate())
- [class func highlightShadowAdjust() -> any CIFilter & CIHighlightShadowAdjust](/documentation/coreimage/cifilter-swift.class/highlightshadowadjust())
- [class func lineOverlay() -> any CIFilter & CILineOverlay](/documentation/coreimage/cifilter-swift.class/lineoverlay())
- [class func mix() -> any CIFilter & CIMix](/documentation/coreimage/cifilter-swift.class/mix())
- [class func personSegmentation() -> any CIFilter & CIPersonSegmentation](/documentation/coreimage/cifilter-swift.class/personsegmentation())
- [class func pixellate() -> any CIFilter & CIPixellate](/documentation/coreimage/cifilter-swift.class/pixellate())
- [class func pointillize() -> any CIFilter & CIPointillize](/documentation/coreimage/cifilter-swift.class/pointillize())
- [class func saliencyMap() -> any CIFilter & CISaliencyMap](/documentation/coreimage/cifilter-swift.class/saliencymap())
- [class func shadedMaterial() -> any CIFilter & CIShadedMaterial](/documentation/coreimage/cifilter-swift.class/shadedmaterial())
- [class func sobelGradients() -> any CIFilter & CISobelGradients](/documentation/coreimage/cifilter-swift.class/sobelgradients())
- [class func spotColor() -> any CIFilter & CISpotColor](/documentation/coreimage/cifilter-swift.class/spotcolor())
- [class func spotLight() -> any CIFilter & CISpotLight](/documentation/coreimage/cifilter-swift.class/spotlight())
- [class func cannyEdgeDetector() -> any CIFilter & CICannyEdgeDetector](/documentation/coreimage/cifilter-swift.class/cannyedgedetector())

#### Protocols

- [CIBlendWithMask](/documentation/coreimage/ciblendwithmask)

##### Instance Properties

- [var backgroundImage: CIImage?](/documentation/coreimage/ciblendwithmask/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/ciblendwithmask/inputimage)
- [var maskImage: CIImage?](/documentation/coreimage/ciblendwithmask/maskimage)
- [CIBloom](/documentation/coreimage/cibloom)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cibloom/inputimage)
- [var intensity: Float](/documentation/coreimage/cibloom/intensity)
- [var radius: Float](/documentation/coreimage/cibloom/radius)
- [CICannyEdgeDetector](/documentation/coreimage/cicannyedgedetector)

##### Instance Properties

- [var gaussianSigma: Float](/documentation/coreimage/cicannyedgedetector/gaussiansigma)
- [var hysteresisPasses: Int](/documentation/coreimage/cicannyedgedetector/hysteresispasses)
- [var inputImage: CIImage?](/documentation/coreimage/cicannyedgedetector/inputimage)
- [var perceptual: Bool](/documentation/coreimage/cicannyedgedetector/perceptual)
- [var thresholdHigh: Float](/documentation/coreimage/cicannyedgedetector/thresholdhigh)
- [var thresholdLow: Float](/documentation/coreimage/cicannyedgedetector/thresholdlow)
- [CIComicEffect](/documentation/coreimage/cicomiceffect)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicomiceffect/inputimage)
- [CICoreMLModel](/documentation/coreimage/cicoremlmodel)

##### Instance Properties

- [var headIndex: Float](/documentation/coreimage/cicoremlmodel/headindex)
- [var inputImage: CIImage?](/documentation/coreimage/cicoremlmodel/inputimage)
- [var model: MLModel](/documentation/coreimage/cicoremlmodel/model)
- [var softmaxNormalization: Bool](/documentation/coreimage/cicoremlmodel/softmaxnormalization)
- [CICrystallize](/documentation/coreimage/cicrystallize)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicrystallize/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicrystallize/inputimage)
- [var radius: Float](/documentation/coreimage/cicrystallize/radius)
- [CIDepthOfField](/documentation/coreimage/cidepthoffield)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidepthoffield/inputimage)
- [var point0: CGPoint](/documentation/coreimage/cidepthoffield/point0)
- [var point1: CGPoint](/documentation/coreimage/cidepthoffield/point1)
- [var radius: Float](/documentation/coreimage/cidepthoffield/radius)
- [var saturation: Float](/documentation/coreimage/cidepthoffield/saturation)
- [var unsharpMaskIntensity: Float](/documentation/coreimage/cidepthoffield/unsharpmaskintensity)
- [var unsharpMaskRadius: Float](/documentation/coreimage/cidepthoffield/unsharpmaskradius)
- [CIEdgeWork](/documentation/coreimage/ciedgework)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedgework/inputimage)
- [var radius: Float](/documentation/coreimage/ciedgework/radius)
- [CIEdges](/documentation/coreimage/ciedges)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedges/inputimage)
- [var intensity: Float](/documentation/coreimage/ciedges/intensity)
- [CIGaborGradients](/documentation/coreimage/cigaborgradients)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigaborgradients/inputimage)
- [CIGloom](/documentation/coreimage/cigloom)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigloom/inputimage)
- [var intensity: Float](/documentation/coreimage/cigloom/intensity)
- [var radius: Float](/documentation/coreimage/cigloom/radius)
- [CIHeightFieldFromMask](/documentation/coreimage/ciheightfieldfrommask)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciheightfieldfrommask/inputimage)
- [var radius: Float](/documentation/coreimage/ciheightfieldfrommask/radius)
- [CIHexagonalPixellate](/documentation/coreimage/cihexagonalpixellate)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cihexagonalpixellate/center)
- [var inputImage: CIImage?](/documentation/coreimage/cihexagonalpixellate/inputimage)
- [var scale: Float](/documentation/coreimage/cihexagonalpixellate/scale)
- [CIHighlightShadowAdjust](/documentation/coreimage/cihighlightshadowadjust)

##### Instance Properties

- [var highlightAmount: Float](/documentation/coreimage/cihighlightshadowadjust/highlightamount)
- [var inputImage: CIImage?](/documentation/coreimage/cihighlightshadowadjust/inputimage)
- [var radius: Float](/documentation/coreimage/cihighlightshadowadjust/radius)
- [var shadowAmount: Float](/documentation/coreimage/cihighlightshadowadjust/shadowamount)
- [CILineOverlay](/documentation/coreimage/cilineoverlay)

##### Instance Properties

- [var nrNoiseLevel: Float](/documentation/coreimage/cilineoverlay/nrnoiselevel)
- [var nrSharpness: Float](/documentation/coreimage/cilineoverlay/nrsharpness)
- [var contrast: Float](/documentation/coreimage/cilineoverlay/contrast)
- [var edgeIntensity: Float](/documentation/coreimage/cilineoverlay/edgeintensity)
- [var inputImage: CIImage?](/documentation/coreimage/cilineoverlay/inputimage)
- [var threshold: Float](/documentation/coreimage/cilineoverlay/threshold)
- [CIMix](/documentation/coreimage/cimix)

##### Instance Properties

- [var amount: Float](/documentation/coreimage/cimix/amount)
- [var backgroundImage: CIImage?](/documentation/coreimage/cimix/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/cimix/inputimage)
- [CIPersonSegmentation](/documentation/coreimage/cipersonsegmentation)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipersonsegmentation/inputimage)
- [var qualityLevel: Int](/documentation/coreimage/cipersonsegmentation/qualitylevel)
- [CIPixellate](/documentation/coreimage/cipixellate)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipixellate/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipixellate/inputimage)
- [var scale: Float](/documentation/coreimage/cipixellate/scale)
- [CIPointillize](/documentation/coreimage/cipointillize)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipointillize/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipointillize/inputimage)
- [var radius: Float](/documentation/coreimage/cipointillize/radius)
- [CISaliencyMap](/documentation/coreimage/cisaliencymap)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisaliencymap/inputimage)
- [CIShadedMaterial](/documentation/coreimage/cishadedmaterial)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cishadedmaterial/inputimage)
- [var scale: Float](/documentation/coreimage/cishadedmaterial/scale)
- [var shadingImage: CIImage?](/documentation/coreimage/cishadedmaterial/shadingimage)
- [CISobelGradients](/documentation/coreimage/cisobelgradients)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisobelgradients/inputimage)
- [CISpotColor](/documentation/coreimage/cispotcolor)

##### Instance Properties

- [var centerColor1: CIColor](/documentation/coreimage/cispotcolor/centercolor1)
- [var centerColor2: CIColor](/documentation/coreimage/cispotcolor/centercolor2)
- [var centerColor3: CIColor](/documentation/coreimage/cispotcolor/centercolor3)
- [var closeness1: Float](/documentation/coreimage/cispotcolor/closeness1)
- [var closeness2: Float](/documentation/coreimage/cispotcolor/closeness2)
- [var closeness3: Float](/documentation/coreimage/cispotcolor/closeness3)
- [var contrast1: Float](/documentation/coreimage/cispotcolor/contrast1)
- [var contrast2: Float](/documentation/coreimage/cispotcolor/contrast2)
- [var contrast3: Float](/documentation/coreimage/cispotcolor/contrast3)
- [var inputImage: CIImage?](/documentation/coreimage/cispotcolor/inputimage)
- [var replacementColor1: CIColor](/documentation/coreimage/cispotcolor/replacementcolor1)
- [var replacementColor2: CIColor](/documentation/coreimage/cispotcolor/replacementcolor2)
- [var replacementColor3: CIColor](/documentation/coreimage/cispotcolor/replacementcolor3)
- [CISpotLight](/documentation/coreimage/cispotlight)

##### Instance Properties

- [var brightness: Float](/documentation/coreimage/cispotlight/brightness)
- [var color: CIColor](/documentation/coreimage/cispotlight/color)
- [var concentration: Float](/documentation/coreimage/cispotlight/concentration)
- [var inputImage: CIImage?](/documentation/coreimage/cispotlight/inputimage)
- [var lightPointsAt: CIVector](/documentation/coreimage/cispotlight/lightpointsat)
- [var lightPosition: CIVector](/documentation/coreimage/cispotlight/lightposition)
- [Tile Effect Filters](/documentation/coreimage/tile-effect-filters)

#### Filters

- [class func affineClamp() -> any CIFilter & CIAffineClamp](/documentation/coreimage/cifilter-swift.class/affineclamp())
- [class func affineTile() -> any CIFilter & CIAffineTile](/documentation/coreimage/cifilter-swift.class/affinetile())
- [class func eightfoldReflectedTile() -> any CIFilter & CIEightfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/eightfoldreflectedtile())
- [class func fourfoldReflectedTile() -> any CIFilter & CIFourfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/fourfoldreflectedtile())
- [class func fourfoldRotatedTile() -> any CIFilter & CIFourfoldRotatedTile](/documentation/coreimage/cifilter-swift.class/fourfoldrotatedtile())
- [class func fourfoldTranslatedTile() -> any CIFilter & CIFourfoldTranslatedTile](/documentation/coreimage/cifilter-swift.class/fourfoldtranslatedtile())
- [class func glideReflectedTile() -> any CIFilter & CIGlideReflectedTile](/documentation/coreimage/cifilter-swift.class/glidereflectedtile())
- [class func kaleidoscope() -> any CIFilter & CIKaleidoscope](/documentation/coreimage/cifilter-swift.class/kaleidoscope())
- [class func opTile() -> any CIFilter & CIOpTile](/documentation/coreimage/cifilter-swift.class/optile())
- [class func parallelogramTile() -> any CIFilter & CIParallelogramTile](/documentation/coreimage/cifilter-swift.class/parallelogramtile())
- [class func perspectiveTile() -> any CIFilter & CIPerspectiveTile](/documentation/coreimage/cifilter-swift.class/perspectivetile())
- [class func sixfoldReflectedTile() -> any CIFilter & CISixfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/sixfoldreflectedtile())
- [class func sixfoldRotatedTile() -> any CIFilter & CISixfoldRotatedTile](/documentation/coreimage/cifilter-swift.class/sixfoldrotatedtile())
- [class func triangleKaleidoscope() -> any CIFilter & CITriangleKaleidoscope](/documentation/coreimage/cifilter-swift.class/trianglekaleidoscope())
- [class func triangleTile() -> any CIFilter & CITriangleTile](/documentation/coreimage/cifilter-swift.class/triangletile())
- [class func twelvefoldReflectedTile() -> any CIFilter & CITwelvefoldReflectedTile](/documentation/coreimage/cifilter-swift.class/twelvefoldreflectedtile())

#### Protocols

- [CIAffineClamp](/documentation/coreimage/ciaffineclamp)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciaffineclamp/inputimage)
- [var transform: CGAffineTransform](/documentation/coreimage/ciaffineclamp/transform)
- [CIAffineTile](/documentation/coreimage/ciaffinetile)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciaffinetile/inputimage)
- [var transform: CGAffineTransform](/documentation/coreimage/ciaffinetile/transform)
- [CIEightfoldReflectedTile](/documentation/coreimage/cieightfoldreflectedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cieightfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cieightfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cieightfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cieightfoldreflectedtile/width)
- [CIFourfoldReflectedTile](/documentation/coreimage/cifourfoldreflectedtile)

##### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/cifourfoldreflectedtile/acuteangle)
- [var angle: Float](/documentation/coreimage/cifourfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldreflectedtile/width)
- [CIFourfoldRotatedTile](/documentation/coreimage/cifourfoldrotatedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cifourfoldrotatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldrotatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldrotatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldrotatedtile/width)
- [CIFourfoldTranslatedTile](/documentation/coreimage/cifourfoldtranslatedtile)

##### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/cifourfoldtranslatedtile/acuteangle)
- [var angle: Float](/documentation/coreimage/cifourfoldtranslatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldtranslatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldtranslatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldtranslatedtile/width)
- [CIGlideReflectedTile](/documentation/coreimage/ciglidereflectedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/ciglidereflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/ciglidereflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciglidereflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/ciglidereflectedtile/width)
- [CIKaleidoscope](/documentation/coreimage/cikaleidoscope)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cikaleidoscope/angle)
- [var center: CGPoint](/documentation/coreimage/cikaleidoscope/center)
- [var count: Int](/documentation/coreimage/cikaleidoscope/count)
- [var inputImage: CIImage?](/documentation/coreimage/cikaleidoscope/inputimage)
- [CIOpTile](/documentation/coreimage/cioptile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cioptile/angle)
- [var center: CGPoint](/documentation/coreimage/cioptile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cioptile/inputimage)
- [var scale: Float](/documentation/coreimage/cioptile/scale)
- [var width: Float](/documentation/coreimage/cioptile/width)
- [CIParallelogramTile](/documentation/coreimage/ciparallelogramtile)

##### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/ciparallelogramtile/acuteangle)
- [var angle: Float](/documentation/coreimage/ciparallelogramtile/angle)
- [var center: CGPoint](/documentation/coreimage/ciparallelogramtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciparallelogramtile/inputimage)
- [var width: Float](/documentation/coreimage/ciparallelogramtile/width)
- [CIPerspectiveTile](/documentation/coreimage/ciperspectivetile)

##### Instance Properties

- [var bottomLeft: CGPoint](/documentation/coreimage/ciperspectivetile/bottomleft)
- [var bottomRight: CGPoint](/documentation/coreimage/ciperspectivetile/bottomright)
- [var inputImage: CIImage?](/documentation/coreimage/ciperspectivetile/inputimage)
- [var topLeft: CGPoint](/documentation/coreimage/ciperspectivetile/topleft)
- [var topRight: CGPoint](/documentation/coreimage/ciperspectivetile/topright)
- [CISixfoldReflectedTile](/documentation/coreimage/cisixfoldreflectedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cisixfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cisixfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cisixfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cisixfoldreflectedtile/width)
- [CISixfoldRotatedTile](/documentation/coreimage/cisixfoldrotatedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cisixfoldrotatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cisixfoldrotatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cisixfoldrotatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cisixfoldrotatedtile/width)
- [CITriangleKaleidoscope](/documentation/coreimage/citrianglekaleidoscope)

##### Instance Properties

- [var decay: Float](/documentation/coreimage/citrianglekaleidoscope/decay)
- [var inputImage: CIImage?](/documentation/coreimage/citrianglekaleidoscope/inputimage)
- [var point: CGPoint](/documentation/coreimage/citrianglekaleidoscope/point)
- [var rotation: Float](/documentation/coreimage/citrianglekaleidoscope/rotation)
- [var size: Float](/documentation/coreimage/citrianglekaleidoscope/size)
- [CITriangleTile](/documentation/coreimage/citriangletile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/citriangletile/angle)
- [var center: CGPoint](/documentation/coreimage/citriangletile/center)
- [var inputImage: CIImage?](/documentation/coreimage/citriangletile/inputimage)
- [var width: Float](/documentation/coreimage/citriangletile/width)
- [CITwelvefoldReflectedTile](/documentation/coreimage/citwelvefoldreflectedtile)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/citwelvefoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/citwelvefoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/citwelvefoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/citwelvefoldreflectedtile/width)
- [Transition Filters](/documentation/coreimage/transition-filters)

#### Filters

- [class func accordionFoldTransition() -> any CIFilter & CIAccordionFoldTransition](/documentation/coreimage/cifilter-swift.class/accordionfoldtransition())
- [class func barsSwipeTransition() -> any CIFilter & CIBarsSwipeTransition](/documentation/coreimage/cifilter-swift.class/barsswipetransition())
- [class func copyMachineTransition() -> any CIFilter & CICopyMachineTransition](/documentation/coreimage/cifilter-swift.class/copymachinetransition())
- [class func disintegrateWithMaskTransition() -> any CIFilter & CIDisintegrateWithMaskTransition](/documentation/coreimage/cifilter-swift.class/disintegratewithmasktransition())
- [class func dissolveTransition() -> any CIFilter & CIDissolveTransition](/documentation/coreimage/cifilter-swift.class/dissolvetransition())
- [class func flashTransition() -> any CIFilter & CIFlashTransition](/documentation/coreimage/cifilter-swift.class/flashtransition())
- [class func modTransition() -> any CIFilter & CIModTransition](/documentation/coreimage/cifilter-swift.class/modtransition())
- [class func pageCurlTransition() -> any CIFilter & CIPageCurlTransition](/documentation/coreimage/cifilter-swift.class/pagecurltransition())
- [class func pageCurlWithShadowTransition() -> any CIFilter & CIPageCurlWithShadowTransition](/documentation/coreimage/cifilter-swift.class/pagecurlwithshadowtransition())
- [class func rippleTransition() -> any CIFilter & CIRippleTransition](/documentation/coreimage/cifilter-swift.class/rippletransition())
- [class func swipeTransition() -> any CIFilter & CISwipeTransition](/documentation/coreimage/cifilter-swift.class/swipetransition())

#### Protocols

- [CITransitionFilter](/documentation/coreimage/citransitionfilter)

##### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citransitionfilter/inputimage)
- [var targetImage: CIImage?](/documentation/coreimage/citransitionfilter/targetimage)
- [var time: Float](/documentation/coreimage/citransitionfilter/time)
- [CIBarsSwipeTransition](/documentation/coreimage/cibarsswipetransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cibarsswipetransition/angle)
- [var barOffset: Float](/documentation/coreimage/cibarsswipetransition/baroffset)
- [var width: Float](/documentation/coreimage/cibarsswipetransition/width)
- [CIAccordionFoldTransition](/documentation/coreimage/ciaccordionfoldtransition)

##### Instance Properties

- [var bottomHeight: Float](/documentation/coreimage/ciaccordionfoldtransition/bottomheight)
- [var foldShadowAmount: Float](/documentation/coreimage/ciaccordionfoldtransition/foldshadowamount)
- [var numberOfFolds: Float](/documentation/coreimage/ciaccordionfoldtransition/numberoffolds)
- [CICopyMachineTransition](/documentation/coreimage/cicopymachinetransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cicopymachinetransition/angle)
- [var color: CIColor](/documentation/coreimage/cicopymachinetransition/color)
- [var extent: CGRect](/documentation/coreimage/cicopymachinetransition/extent)
- [var opacity: Float](/documentation/coreimage/cicopymachinetransition/opacity)
- [var width: Float](/documentation/coreimage/cicopymachinetransition/width)
- [CIDisintegrateWithMaskTransition](/documentation/coreimage/cidisintegratewithmasktransition)

##### Instance Properties

- [var maskImage: CIImage?](/documentation/coreimage/cidisintegratewithmasktransition/maskimage)
- [var shadowDensity: Float](/documentation/coreimage/cidisintegratewithmasktransition/shadowdensity)
- [var shadowOffset: CGPoint](/documentation/coreimage/cidisintegratewithmasktransition/shadowoffset)
- [var shadowRadius: Float](/documentation/coreimage/cidisintegratewithmasktransition/shadowradius)
- [CIDissolveTransition](/documentation/coreimage/cidissolvetransition)
- [CIFlashTransition](/documentation/coreimage/ciflashtransition)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciflashtransition/center)
- [var color: CIColor](/documentation/coreimage/ciflashtransition/color)
- [var extent: CGRect](/documentation/coreimage/ciflashtransition/extent)
- [var fadeThreshold: Float](/documentation/coreimage/ciflashtransition/fadethreshold)
- [var maxStriationRadius: Float](/documentation/coreimage/ciflashtransition/maxstriationradius)
- [var striationContrast: Float](/documentation/coreimage/ciflashtransition/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/ciflashtransition/striationstrength)
- [CIModTransition](/documentation/coreimage/cimodtransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cimodtransition/angle)
- [var center: CGPoint](/documentation/coreimage/cimodtransition/center)
- [var compression: Float](/documentation/coreimage/cimodtransition/compression)
- [var radius: Float](/documentation/coreimage/cimodtransition/radius)
- [CIPageCurlTransition](/documentation/coreimage/cipagecurltransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cipagecurltransition/angle)
- [var backsideImage: CIImage?](/documentation/coreimage/cipagecurltransition/backsideimage)
- [var extent: CGRect](/documentation/coreimage/cipagecurltransition/extent)
- [var radius: Float](/documentation/coreimage/cipagecurltransition/radius)
- [var shadingImage: CIImage?](/documentation/coreimage/cipagecurltransition/shadingimage)
- [CIPageCurlWithShadowTransition](/documentation/coreimage/cipagecurlwithshadowtransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/cipagecurlwithshadowtransition/angle)
- [var backsideImage: CIImage?](/documentation/coreimage/cipagecurlwithshadowtransition/backsideimage)
- [var extent: CGRect](/documentation/coreimage/cipagecurlwithshadowtransition/extent)
- [var radius: Float](/documentation/coreimage/cipagecurlwithshadowtransition/radius)
- [var shadowAmount: Float](/documentation/coreimage/cipagecurlwithshadowtransition/shadowamount)
- [var shadowExtent: CGRect](/documentation/coreimage/cipagecurlwithshadowtransition/shadowextent)
- [var shadowSize: Float](/documentation/coreimage/cipagecurlwithshadowtransition/shadowsize)
- [CIRippleTransition](/documentation/coreimage/cirippletransition)

##### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cirippletransition/center)
- [var extent: CGRect](/documentation/coreimage/cirippletransition/extent)
- [var scale: Float](/documentation/coreimage/cirippletransition/scale)
- [var shadingImage: CIImage?](/documentation/coreimage/cirippletransition/shadingimage)
- [var width: Float](/documentation/coreimage/cirippletransition/width)
- [CISwipeTransition](/documentation/coreimage/ciswipetransition)

##### Instance Properties

- [var angle: Float](/documentation/coreimage/ciswipetransition/angle)
- [var color: CIColor](/documentation/coreimage/ciswipetransition/color)
- [var extent: CGRect](/documentation/coreimage/ciswipetransition/extent)
- [var opacity: Float](/documentation/coreimage/ciswipetransition/opacity)
- [var width: Float](/documentation/coreimage/ciswipetransition/width)

### Accessing registered filters

- [class func filterNames(inCategories: [String]?) -> [String]](/documentation/coreimage/cifilter-swift.class/filternames(incategories:))
- [class func filterNames(inCategory: String?) -> [String]](/documentation/coreimage/cifilter-swift.class/filternames(incategory:))

### Registering a filter

- [class func registerName(String, constructor: any CIFilterConstructor, classAttributes: [String : Any])](/documentation/coreimage/cifilter-swift.class/registername(_:constructor:classattributes:))

### Getting filter parameters and attributes

- [var name: String](/documentation/coreimage/cifilter-swift.class/name)
- [var isEnabled: Bool](/documentation/coreimage/cifilter-swift.class/isenabled)
- [var attributes: [String : Any]](/documentation/coreimage/cifilter-swift.class/attributes)
- [var inputKeys: [String]](/documentation/coreimage/cifilter-swift.class/inputkeys)
- [var outputKeys: [String]](/documentation/coreimage/cifilter-swift.class/outputkeys)
- [var outputImage: CIImage?](/documentation/coreimage/cifilter-swift.class/outputimage)

### Setting default values

- [func setDefaults()](/documentation/coreimage/cifilter-swift.class/setdefaults())

### Applying a filter

- [func apply(CIKernel, arguments: [Any]?, options: [String : Any]?) -> CIImage?](/documentation/coreimage/cifilter-swift.class/apply(_:arguments:options:))

### Getting localized information for registered filters

- [class func localizedName(forFilterName: String) -> String?](/documentation/coreimage/cifilter-swift.class/localizedname(forfiltername:))
- [class func localizedName(forCategory: String) -> String](/documentation/coreimage/cifilter-swift.class/localizedname(forcategory:))
- [class func localizedDescription(forFilterName: String) -> String?](/documentation/coreimage/cifilter-swift.class/localizeddescription(forfiltername:))
- [class func localizedReferenceDocumentation(forFilterName: String) -> URL?](/documentation/coreimage/cifilter-swift.class/localizedreferencedocumentation(forfiltername:))

### Creating a configuration view for a filter

- [func view(forUIConfiguration: [AnyHashable : Any]!, excludedKeys: [Any]!) -> IKFilterUIView!](/documentation/coreimage/cifilter-swift.class/view(foruiconfiguration:excludedkeys:))

### Applying system tone mapping modes

- [CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption)

#### Enumeration Cases

- [static let standard: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/standard)
- [static let constrainedHigh: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/constrainedhigh)
- [static let high: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/high)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/cidynamicrangeoption/init(rawvalue:))

### Constants

- [Filter Attribute Keys](/documentation/coreimage/filter-attribute-keys)

#### Constants

- [let kCIAttributeFilterName: String](/documentation/coreimage/kciattributefiltername)
- [let kCIAttributeFilterDisplayName: String](/documentation/coreimage/kciattributefilterdisplayname)
- [let kCIAttributeDescription: String](/documentation/coreimage/kciattributedescription)
- [let kCIAttributeFilterAvailable_Mac: String](/documentation/coreimage/kciattributefilteravailable_mac)
- [let kCIAttributeFilterAvailable_iOS: String](/documentation/coreimage/kciattributefilteravailable_ios)
- [let kCIAttributeReferenceDocumentation: String](/documentation/coreimage/kciattributereferencedocumentation)
- [let kCIAttributeFilterCategories: String](/documentation/coreimage/kciattributefiltercategories)
- [let kCIAttributeClass: String](/documentation/coreimage/kciattributeclass)
- [let kCIAttributeType: String](/documentation/coreimage/kciattributetype)
- [let kCIAttributeMin: String](/documentation/coreimage/kciattributemin)
- [let kCIAttributeMax: String](/documentation/coreimage/kciattributemax)
- [let kCIAttributeSliderMin: String](/documentation/coreimage/kciattributeslidermin)
- [let kCIAttributeSliderMax: String](/documentation/coreimage/kciattributeslidermax)
- [let kCIAttributeDefault: String](/documentation/coreimage/kciattributedefault)
- [let kCIAttributeIdentity: String](/documentation/coreimage/kciattributeidentity)
- [let kCIAttributeName: String](/documentation/coreimage/kciattributename)
- [let kCIAttributeDisplayName: String](/documentation/coreimage/kciattributedisplayname)
- [Data Type Attributes](/documentation/coreimage/data-type-attributes)

#### Constants

- [let kCIAttributeTypeTime: String](/documentation/coreimage/kciattributetypetime)
- [let kCIAttributeTypeScalar: String](/documentation/coreimage/kciattributetypescalar)
- [let kCIAttributeTypeDistance: String](/documentation/coreimage/kciattributetypedistance)
- [let kCIAttributeTypeAngle: String](/documentation/coreimage/kciattributetypeangle)
- [let kCIAttributeTypeBoolean: String](/documentation/coreimage/kciattributetypeboolean)
- [let kCIAttributeTypeInteger: String](/documentation/coreimage/kciattributetypeinteger)
- [let kCIAttributeTypeCount: String](/documentation/coreimage/kciattributetypecount)
- [Vector Quantity Attributes](/documentation/coreimage/vector-quantity-attributes)

#### Constants

- [let kCIAttributeTypePosition: String](/documentation/coreimage/kciattributetypeposition)
- [let kCIAttributeTypeOffset: String](/documentation/coreimage/kciattributetypeoffset)
- [let kCIAttributeTypePosition3: String](/documentation/coreimage/kciattributetypeposition3)
- [let kCIAttributeTypeRectangle: String](/documentation/coreimage/kciattributetyperectangle)
- [Color Attribute Keys](/documentation/coreimage/color-attribute-keys)

#### Constants

- [let kCIAttributeTypeOpaqueColor: String](/documentation/coreimage/kciattributetypeopaquecolor)
- [let kCIAttributeTypeGradient: String](/documentation/coreimage/kciattributetypegradient)
- [let kCIAttributeTypeColor: String](/documentation/coreimage/kciattributetypecolor)
- [Image Attribute Keys](/documentation/coreimage/image-attribute-keys)

#### Constants

- [let kCIAttributeTypeImage: String](/documentation/coreimage/kciattributetypeimage)
- [let kCIAttributeTypeTransform: String](/documentation/coreimage/kciattributetypetransform)
- [Filter Category Keys](/documentation/coreimage/filter-category-keys)

#### Constants

- [let kCICategoryDistortionEffect: String](/documentation/coreimage/kcicategorydistortioneffect)
- [let kCICategoryGeometryAdjustment: String](/documentation/coreimage/kcicategorygeometryadjustment)
- [let kCICategoryCompositeOperation: String](/documentation/coreimage/kcicategorycompositeoperation)
- [let kCICategoryHalftoneEffect: String](/documentation/coreimage/kcicategoryhalftoneeffect)
- [let kCICategoryColorAdjustment: String](/documentation/coreimage/kcicategorycoloradjustment)
- [let kCICategoryColorEffect: String](/documentation/coreimage/kcicategorycoloreffect)
- [let kCICategoryTransition: String](/documentation/coreimage/kcicategorytransition)
- [let kCICategoryTileEffect: String](/documentation/coreimage/kcicategorytileeffect)
- [let kCICategoryGenerator: String](/documentation/coreimage/kcicategorygenerator)
- [let kCICategoryReduction: String](/documentation/coreimage/kcicategoryreduction)
- [let kCICategoryGradient: String](/documentation/coreimage/kcicategorygradient)
- [let kCICategoryStylize: String](/documentation/coreimage/kcicategorystylize)
- [let kCICategorySharpen: String](/documentation/coreimage/kcicategorysharpen)
- [let kCICategoryBlur: String](/documentation/coreimage/kcicategoryblur)
- [let kCICategoryVideo: String](/documentation/coreimage/kcicategoryvideo)
- [let kCICategoryStillImage: String](/documentation/coreimage/kcicategorystillimage)
- [let kCICategoryInterlaced: String](/documentation/coreimage/kcicategoryinterlaced)
- [let kCICategoryNonSquarePixels: String](/documentation/coreimage/kcicategorynonsquarepixels)
- [let kCICategoryHighDynamicRange: String](/documentation/coreimage/kcicategoryhighdynamicrange)
- [let kCICategoryBuiltIn: String](/documentation/coreimage/kcicategorybuiltin)
- [let kCICategoryFilterGenerator: String](/documentation/coreimage/kcicategoryfiltergenerator)
- [Options for Applying a Filter](/documentation/coreimage/options-for-applying-a-filter)

#### Constants

- [let kCIApplyOptionExtent: String](/documentation/coreimage/kciapplyoptionextent)
- [let kCIApplyOptionDefinition: String](/documentation/coreimage/kciapplyoptiondefinition)
- [let kCIApplyOptionUserInfo: String](/documentation/coreimage/kciapplyoptionuserinfo)
- [let kCIApplyOptionColorSpace: String](/documentation/coreimage/kciapplyoptioncolorspace)
- [User Interface Control Options](/documentation/coreimage/user-interface-control-options)

#### Constants

- [let kCIUIParameterSet: String](/documentation/coreimage/kciuiparameterset)
- [let kCIUISetBasic: String](/documentation/coreimage/kciuisetbasic)
- [let kCIUISetIntermediate: String](/documentation/coreimage/kciuisetintermediate)
- [let kCIUISetAdvanced: String](/documentation/coreimage/kciuisetadvanced)
- [let kCIUISetDevelopment: String](/documentation/coreimage/kciuisetdevelopment)
- [User Interface Options](/documentation/coreimage/user-interface-options)

#### Constants

- [let IKUISizeFlavor: String](/documentation/quartz/ikuisizeflavor)
- [let IKUISizeMini: String](/documentation/quartz/ikuisizemini)
- [let IKUISizeSmall: String](/documentation/quartz/ikuisizesmall)
- [let IKUISizeRegular: String](/documentation/quartz/ikuisizeregular)
- [let IKUImaxSize: String](/documentation/quartz/ikuimaxsize)
- [let IKUIFlavorAllowFallback: String](/documentation/quartz/ikuiflavorallowfallback)
- [Filter Parameter Keys](/documentation/coreimage/filter-parameter-keys)

#### Constants

- [let kCIOutputImageKey: String](/documentation/coreimage/kcioutputimagekey)
- [let kCIInputAmountKey: String](/documentation/coreimage/kciinputamountkey)
- [let kCIInputBackgroundImageKey: String](/documentation/coreimage/kciinputbackgroundimagekey)
- [let kCIInputImageKey: String](/documentation/coreimage/kciinputimagekey)
- [let kCIInputTimeKey: String](/documentation/coreimage/kciinputtimekey)
- [let kCIInputDepthImageKey: String](/documentation/coreimage/kciinputdepthimagekey)
- [let kCIInputDisparityImageKey: String](/documentation/coreimage/kciinputdisparityimagekey)
- [let kCIInputTransformKey: String](/documentation/coreimage/kciinputtransformkey)
- [let kCIInputScaleKey: String](/documentation/coreimage/kciinputscalekey)
- [let kCIInputAspectRatioKey: String](/documentation/coreimage/kciinputaspectratiokey)
- [let kCIInputCenterKey: String](/documentation/coreimage/kciinputcenterkey)
- [let kCIInputRadiusKey: String](/documentation/coreimage/kciinputradiuskey)
- [let kCIInputAngleKey: String](/documentation/coreimage/kciinputanglekey)
- [let kCIInputRefractionKey: String](/documentation/coreimage/kciinputrefractionkey)
- [let kCIInputWidthKey: String](/documentation/coreimage/kciinputwidthkey)
- [let kCIInputSharpnessKey: String](/documentation/coreimage/kciinputsharpnesskey)
- [let kCIInputIntensityKey: String](/documentation/coreimage/kciinputintensitykey)
- [let kCIInputEVKey: String](/documentation/coreimage/kciinputevkey)
- [let kCIInputSaturationKey: String](/documentation/coreimage/kciinputsaturationkey)
- [let kCIInputColorKey: String](/documentation/coreimage/kciinputcolorkey)
- [let kCIInputBrightnessKey: String](/documentation/coreimage/kciinputbrightnesskey)
- [let kCIInputContrastKey: String](/documentation/coreimage/kciinputcontrastkey)
- [let kCIInputWeightsKey: String](/documentation/coreimage/kciinputweightskey)
- [let kCIInputGradientImageKey: String](/documentation/coreimage/kciinputgradientimagekey)
- [let kCIInputMaskImageKey: String](/documentation/coreimage/kciinputmaskimagekey)
- [let kCIInputMatteImageKey: String](/documentation/coreimage/kciinputmatteimagekey)
- [let kCIInputShadingImageKey: String](/documentation/coreimage/kciinputshadingimagekey)
- [let kCIInputTargetImageKey: String](/documentation/coreimage/kciinputtargetimagekey)
- [let kCIInputExtentKey: String](/documentation/coreimage/kciinputextentkey)
- [let kCIInputVersionKey: String](/documentation/coreimage/kciinputversionkey)
- [static let standard: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/standard)
- [static let constrainedHigh: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/constrainedhigh)
- [static let high: CIDynamicRangeOption](/documentation/coreimage/cidynamicrangeoption/high)
- [static let baselineExposure: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/baselineexposure)
- [static let disableGamutMap: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/disablegamutmap)
- [static let moireAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/moireamount)
- [RAW Image Options](/documentation/coreimage/raw-image-options)

#### Constants

- [static let decoderVersion: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/decoderversion)
- [static let supportedDecoderVersions: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/supporteddecoderversions)
- [static let boostAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/boostamount)
- [static let neutralChromaticityX: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutralchromaticityx)
- [static let neutralChromaticityY: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutralchromaticityy)
- [static let neutralTemperature: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutraltemperature)
- [static let neutralTint: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutraltint)
- [static let neutralLocation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutrallocation)
- [static let scaleFactor: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/scalefactor)
- [static let allowDraftMode: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/allowdraftmode)
- [static let ignoreImageOrientation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/ignoreimageorientation)
- [static let imageOrientation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/imageorientation)
- [static let enableSharpening: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablesharpening)
- [static let enableChromaticNoiseTracking: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablechromaticnoisetracking)
- [static let noiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductionamount)
- [static let enableVendorLensCorrection: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablevendorlenscorrection)
- [static let luminanceNoiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/luminancenoisereductionamount)
- [static let colorNoiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/colornoisereductionamount)
- [static let noiseReductionSharpnessAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductionsharpnessamount)
- [static let noiseReductionContrastAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductioncontrastamount)
- [static let noiseReductionDetailAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductiondetailamount)
- [static let boostShadowAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/boostshadowamount)
- [let kCIInputBiasKey: String](/documentation/coreimage/kciinputbiaskey)
- [static let linearSpaceFilter: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/linearspacefilter)
- [static let outputNativeSize: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/outputnativesize)
- [static let activeKeys: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/activekeys)

### Deprecated

- [init!(CVPixelBuffer: CVPixelBuffer!, properties: [AnyHashable : Any]!, options: [CIRAWFilterOption : Any]!)](/documentation/coreimage/cifilter-swift.class/init(cvpixelbuffer:properties:options:))
- [init!(imageData: Data!, options: [CIRAWFilterOption : Any]!)](/documentation/coreimage/cifilter-swift.class/init(imagedata:options:))
- [init!(imageURL: URL!, options: [CIRAWFilterOption : Any]!)](/documentation/coreimage/cifilter-swift.class/init(imageurl:options:))
- [CIRAWFilterOption](/documentation/coreimage/cirawfilteroption)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/cirawfilteroption/init(rawvalue:))

#### Type Properties

- [static let activeKeys: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/activekeys)
- [static let allowDraftMode: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/allowdraftmode)
- [static let baselineExposure: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/baselineexposure)
- [static let boostAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/boostamount)
- [static let boostShadowAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/boostshadowamount)
- [static let ciInputEnableEDRModeKey: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/ciinputenableedrmodekey)
- [static let ciInputLocalToneMapAmountKey: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/ciinputlocaltonemapamountkey)
- [static let colorNoiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/colornoisereductionamount)
- [static let decoderVersion: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/decoderversion)
- [static let disableGamutMap: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/disablegamutmap)
- [static let enableChromaticNoiseTracking: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablechromaticnoisetracking)
- [static let enableSharpening: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablesharpening)
- [static let enableVendorLensCorrection: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/enablevendorlenscorrection)
- [static let ignoreImageOrientation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/ignoreimageorientation)
- [static let imageOrientation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/imageorientation)
- [static let linearSpaceFilter: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/linearspacefilter)
- [static let luminanceNoiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/luminancenoisereductionamount)
- [static let moireAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/moireamount)
- [static let neutralChromaticityX: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutralchromaticityx)
- [static let neutralChromaticityY: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutralchromaticityy)
- [static let neutralLocation: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutrallocation)
- [static let neutralTemperature: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutraltemperature)
- [static let neutralTint: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/neutraltint)
- [static let noiseReductionAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductionamount)
- [static let noiseReductionContrastAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductioncontrastamount)
- [static let noiseReductionDetailAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductiondetailamount)
- [static let noiseReductionSharpnessAmount: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/noisereductionsharpnessamount)
- [static let outputNativeSize: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/outputnativesize)
- [static let propertiesKey: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/propertieskey)
- [static let scaleFactor: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/scalefactor)
- [static let supportedDecoderVersions: CIRAWFilterOption](/documentation/coreimage/cirawfilteroption/supporteddecoderversions)
- [class func serializedXMP(from: [CIFilter], inputImageExtent: CGRect) -> Data?](/documentation/coreimage/cifilter-swift.class/serializedxmp(from:inputimageextent:))
- [class func filterArray(fromSerializedXMP: Data, inputImageExtent: CGRect, error: NSErrorPointer) -> [CIFilter]](/documentation/coreimage/cifilter-swift.class/filterarray(fromserializedxmp:inputimageextent:error:))
- [class func supportedRawCameraModels() -> [String]!](/documentation/coreimage/cifilter-swift.class/supportedrawcameramodels())

### Type methods

- [class func areaAlphaWeightedHistogram() -> any CIFilter & CIAreaHistogram](/documentation/coreimage/cifilter-swift.class/areaalphaweightedhistogram())
- [class func areaBoundsRed() -> any CIFilter & CIAreaBoundsRed](/documentation/coreimage/cifilter-swift.class/areaboundsred())
- [class func maximumScaleTransform() -> any CIFilter & CIMaximumScaleTransform](/documentation/coreimage/cifilter-swift.class/maximumscaletransform())
- [class func toneMapHeadroom() -> any CIFilter & CIToneMapHeadroom](/documentation/coreimage/cifilter-swift.class/tonemapheadroom())

### Type Methods

- [class func areaAverageMaximumRed() -> any CIFilter & CIAreaAverageMaximumRed](/documentation/coreimage/cifilter-swift.class/areaaveragemaximumred())
- [class func blurredRoundedRectangleGenerator() -> any CIFilter & CIBlurredRoundedRectangleGenerator](/documentation/coreimage/cifilter-swift.class/blurredroundedrectanglegenerator())
- [class func distanceGradientFromRedMask() -> any CIFilter & CIDistanceGradientFromRedMask](/documentation/coreimage/cifilter-swift.class/distancegradientfromredmask())
- [class func roundedQRCodeGenerator() -> any CIFilter & CIRoundedQRCodeGenerator](/documentation/coreimage/cifilter-swift.class/roundedqrcodegenerator())
- [class func signedDistanceGradientFromRedMask() -> any CIFilter & CISignedDistanceGradientFromRedMask](/documentation/coreimage/cifilter-swift.class/signeddistancegradientfromredmask())
- [class func systemToneMap() -> any CIFilter & CISystemToneMap](/documentation/coreimage/cifilter-swift.class/systemtonemap())
- [CIRAWFilter](/documentation/coreimage/cirawfilter)

### Creating a filter

- [convenience init?(cvPixelBuffer: CVPixelBuffer, properties: [AnyHashable : Any])](/documentation/coreimage/cirawfilter/init(cvpixelbuffer:properties:))
- [convenience init?(imageData: Data, identifierHint: String?)](/documentation/coreimage/cirawfilter/init(imagedata:identifierhint:))
- [convenience init?(imageURL: URL)](/documentation/coreimage/cirawfilter/init(imageurl:))

### Inspecting supported camera models, decoders, and filters

- [class var supportedCameraModels: [String]](/documentation/coreimage/cirawfilter/supportedcameramodels)
- [var supportedDecoderVersions: [CIRAWDecoderVersion]](/documentation/coreimage/cirawfilter/supporteddecoderversions)
- [CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion)

#### Initializers

- [init(rawValue: String)](/documentation/coreimage/cirawdecoderversion/init(rawvalue:))

#### Type Properties

- [static let none: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/none)
- [static let version6: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version6)
- [static let version6DNG: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version6dng)
- [static let version7: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version7)
- [static let version7DNG: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version7dng)
- [static let version8: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version8)
- [static let version8DNG: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version8dng)
- [static let version9: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version9)
- [static let version9DNG: CIRAWDecoderVersion](/documentation/coreimage/cirawdecoderversion/version9dng)
- [var isColorNoiseReductionSupported: Bool](/documentation/coreimage/cirawfilter/iscolornoisereductionsupported)
- [var isContrastSupported: Bool](/documentation/coreimage/cirawfilter/iscontrastsupported)
- [var isDetailSupported: Bool](/documentation/coreimage/cirawfilter/isdetailsupported)
- [var isLensCorrectionSupported: Bool](/documentation/coreimage/cirawfilter/islenscorrectionsupported)
- [var isLocalToneMapSupported: Bool](/documentation/coreimage/cirawfilter/islocaltonemapsupported)
- [var isLuminanceNoiseReductionSupported: Bool](/documentation/coreimage/cirawfilter/isluminancenoisereductionsupported)
- [var isMoireReductionSupported: Bool](/documentation/coreimage/cirawfilter/ismoirereductionsupported)
- [var isSharpnessSupported: Bool](/documentation/coreimage/cirawfilter/issharpnesssupported)
- [var nativeSize: CGSize](/documentation/coreimage/cirawfilter/nativesize)

### Configuring a filter

- [var baselineExposure: Float](/documentation/coreimage/cirawfilter/baselineexposure)
- [var boostAmount: Float](/documentation/coreimage/cirawfilter/boostamount)
- [var boostShadowAmount: Float](/documentation/coreimage/cirawfilter/boostshadowamount)
- [var colorNoiseReductionAmount: Float](/documentation/coreimage/cirawfilter/colornoisereductionamount)
- [var contrastAmount: Float](/documentation/coreimage/cirawfilter/contrastamount)
- [var decoderVersion: CIRAWDecoderVersion](/documentation/coreimage/cirawfilter/decoderversion)
- [var detailAmount: Float](/documentation/coreimage/cirawfilter/detailamount)
- [var exposure: Float](/documentation/coreimage/cirawfilter/exposure)
- [var extendedDynamicRangeAmount: Float](/documentation/coreimage/cirawfilter/extendeddynamicrangeamount)
- [var isDraftModeEnabled: Bool](/documentation/coreimage/cirawfilter/isdraftmodeenabled)
- [var isGamutMappingEnabled: Bool](/documentation/coreimage/cirawfilter/isgamutmappingenabled)
- [var isLensCorrectionEnabled: Bool](/documentation/coreimage/cirawfilter/islenscorrectionenabled)
- [var linearSpaceFilter: CIFilter?](/documentation/coreimage/cirawfilter/linearspacefilter)
- [var localToneMapAmount: Float](/documentation/coreimage/cirawfilter/localtonemapamount)
- [var luminanceNoiseReductionAmount: Float](/documentation/coreimage/cirawfilter/luminancenoisereductionamount)
- [var moireReductionAmount: Float](/documentation/coreimage/cirawfilter/moirereductionamount)
- [var neutralChromaticity: CGPoint](/documentation/coreimage/cirawfilter/neutralchromaticity)
- [var neutralLocation: CGPoint](/documentation/coreimage/cirawfilter/neutrallocation)
- [var neutralTemperature: Float](/documentation/coreimage/cirawfilter/neutraltemperature)
- [var neutralTint: Float](/documentation/coreimage/cirawfilter/neutraltint)
- [var orientation: CGImagePropertyOrientation](/documentation/coreimage/cirawfilter/orientation)
- [var portraitEffectsMatte: CIImage?](/documentation/coreimage/cirawfilter/portraiteffectsmatte)
- [var previewImage: CIImage?](/documentation/coreimage/cirawfilter/previewimage)
- [var properties: [AnyHashable : Any]](/documentation/coreimage/cirawfilter/properties)
- [var scaleFactor: Float](/documentation/coreimage/cirawfilter/scalefactor)
- [var semanticSegmentationGlassesMatte: CIImage?](/documentation/coreimage/cirawfilter/semanticsegmentationglassesmatte)
- [var semanticSegmentationHairMatte: CIImage?](/documentation/coreimage/cirawfilter/semanticsegmentationhairmatte)
- [var semanticSegmentationSkinMatte: CIImage?](/documentation/coreimage/cirawfilter/semanticsegmentationskinmatte)
- [var semanticSegmentationSkyMatte: CIImage?](/documentation/coreimage/cirawfilter/semanticsegmentationskymatte)
- [var semanticSegmentationTeethMatte: CIImage?](/documentation/coreimage/cirawfilter/semanticsegmentationteethmatte)
- [var shadowBias: Float](/documentation/coreimage/cirawfilter/shadowbias)
- [var sharpnessAmount: Float](/documentation/coreimage/cirawfilter/sharpnessamount)

### Instance Properties

- [var isHighlightRecoveryEnabled: Bool](/documentation/coreimage/cirawfilter/ishighlightrecoveryenabled)
- [var isHighlightRecoverySupported: Bool](/documentation/coreimage/cirawfilter/ishighlightrecoverysupported)
- [CIColor](/documentation/coreimage/cicolor)

### Initializing Color Objects

- [init(cgColor: CGColor)](/documentation/coreimage/cicolor/init(cgcolor:))
- [convenience init(color: UIColor)](/documentation/coreimage/cicolor/init(color:))
- [convenience init(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat)](/documentation/coreimage/cicolor/init(red:green:blue:alpha:))
- [convenience init?(red: CGFloat, green: CGFloat, blue: CGFloat, colorSpace: CGColorSpace)](/documentation/coreimage/cicolor/init(red:green:blue:colorspace:))
- [convenience init?(red: CGFloat, green: CGFloat, blue: CGFloat, alpha: CGFloat, colorSpace: CGColorSpace)](/documentation/coreimage/cicolor/init(red:green:blue:alpha:colorspace:))

### Creating Color Objects

- [convenience init(red: CGFloat, green: CGFloat, blue: CGFloat)](/documentation/coreimage/cicolor/init(red:green:blue:))
- [convenience init(string: String)](/documentation/coreimage/cicolor/init(string:))

### Getting Color Components

- [var colorSpace: CGColorSpace](/documentation/coreimage/cicolor/colorspace)
- [var components: UnsafePointer<CGFloat>](/documentation/coreimage/cicolor/components)
- [var numberOfComponents: Int](/documentation/coreimage/cicolor/numberofcomponents)
- [var red: CGFloat](/documentation/coreimage/cicolor/red-swift.property)
- [var green: CGFloat](/documentation/coreimage/cicolor/green-swift.property)
- [var blue: CGFloat](/documentation/coreimage/cicolor/blue-swift.property)
- [var alpha: CGFloat](/documentation/coreimage/cicolor/alpha)
- [var stringRepresentation: String](/documentation/coreimage/cicolor/stringrepresentation)

### Creating a CIColor Object with Preset Components

- [class var black: CIColor](/documentation/coreimage/cicolor/black)
- [class var blue: CIColor](/documentation/coreimage/cicolor/blue-swift.type.property)
- [class var clear: CIColor](/documentation/coreimage/cicolor/clear)
- [class var cyan: CIColor](/documentation/coreimage/cicolor/cyan)
- [class var gray: CIColor](/documentation/coreimage/cicolor/gray)
- [class var green: CIColor](/documentation/coreimage/cicolor/green-swift.type.property)
- [class var magenta: CIColor](/documentation/coreimage/cicolor/magenta)
- [class var red: CIColor](/documentation/coreimage/cicolor/red-swift.type.property)
- [class var white: CIColor](/documentation/coreimage/cicolor/white)
- [class var yellow: CIColor](/documentation/coreimage/cicolor/yellow)
- [CIVector](/documentation/coreimage/civector)

### Initializing a Vector

- [init(values: UnsafePointer<CGFloat>, count: Int)](/documentation/coreimage/civector/init(values:count:))
- [convenience init(x: CGFloat)](/documentation/coreimage/civector/init(x:))
- [convenience init(x: CGFloat, y: CGFloat)](/documentation/coreimage/civector/init(x:y:))
- [convenience init(x: CGFloat, y: CGFloat, z: CGFloat)](/documentation/coreimage/civector/init(x:y:z:))
- [convenience init(x: CGFloat, y: CGFloat, z: CGFloat, w: CGFloat)](/documentation/coreimage/civector/init(x:y:z:w:))
- [convenience init(string: String)](/documentation/coreimage/civector/init(string:))
- [convenience init(cgAffineTransform: CGAffineTransform)](/documentation/coreimage/civector/init(cgaffinetransform:))
- [convenience init(cgPoint: CGPoint)](/documentation/coreimage/civector/init(cgpoint:))
- [convenience init(cgRect: CGRect)](/documentation/coreimage/civector/init(cgrect:))

### Getting Values From a Vector

- [func value(at: Int) -> CGFloat](/documentation/coreimage/civector/value(at:))
- [var count: Int](/documentation/coreimage/civector/count)
- [var x: CGFloat](/documentation/coreimage/civector/x)
- [var y: CGFloat](/documentation/coreimage/civector/y)
- [var z: CGFloat](/documentation/coreimage/civector/z)
- [var w: CGFloat](/documentation/coreimage/civector/w)
- [var stringRepresentation: String](/documentation/coreimage/civector/stringrepresentation)
- [var cgAffineTransformValue: CGAffineTransform](/documentation/coreimage/civector/cgaffinetransformvalue)
- [var cgPointValue: CGPoint](/documentation/coreimage/civector/cgpointvalue)
- [var cgRectValue: CGRect](/documentation/coreimage/civector/cgrectvalue)

## Filter Catalog

- [Blur Filters](/documentation/coreimage/blur-filters)

### Filters

- [class func bokehBlur() -> any CIFilter & CIBokehBlur](/documentation/coreimage/cifilter-swift.class/bokehblur())
- [class func boxBlur() -> any CIFilter & CIBoxBlur](/documentation/coreimage/cifilter-swift.class/boxblur())
- [class func discBlur() -> any CIFilter & CIDiscBlur](/documentation/coreimage/cifilter-swift.class/discblur())
- [class func gaussianBlur() -> any CIFilter & CIGaussianBlur](/documentation/coreimage/cifilter-swift.class/gaussianblur())
- [class func maskedVariableBlur() -> any CIFilter & CIMaskedVariableBlur](/documentation/coreimage/cifilter-swift.class/maskedvariableblur())
- [class func median() -> any CIFilter & CIMedian](/documentation/coreimage/cifilter-swift.class/median())
- [class func morphologyGradient() -> any CIFilter & CIMorphologyGradient](/documentation/coreimage/cifilter-swift.class/morphologygradient())
- [class func morphologyMaximum() -> any CIFilter & CIMorphologyMaximum](/documentation/coreimage/cifilter-swift.class/morphologymaximum())
- [class func morphologyMinimum() -> any CIFilter & CIMorphologyMinimum](/documentation/coreimage/cifilter-swift.class/morphologyminimum())
- [class func morphologyRectangleMaximum() -> any CIFilter & CIMorphologyRectangleMaximum](/documentation/coreimage/cifilter-swift.class/morphologyrectanglemaximum())
- [class func morphologyRectangleMinimum() -> any CIFilter & CIMorphologyRectangleMinimum](/documentation/coreimage/cifilter-swift.class/morphologyrectangleminimum())
- [class func motionBlur() -> any CIFilter & CIMotionBlur](/documentation/coreimage/cifilter-swift.class/motionblur())
- [class func noiseReduction() -> any CIFilter & CINoiseReduction](/documentation/coreimage/cifilter-swift.class/noisereduction())
- [class func zoomBlur() -> any CIFilter & CIZoomBlur](/documentation/coreimage/cifilter-swift.class/zoomblur())

### Protocols

- [CIBokehBlur](/documentation/coreimage/cibokehblur)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cibokehblur/inputimage)
- [var radius: Float](/documentation/coreimage/cibokehblur/radius)
- [var ringAmount: Float](/documentation/coreimage/cibokehblur/ringamount)
- [var ringSize: Float](/documentation/coreimage/cibokehblur/ringsize)
- [var softness: Float](/documentation/coreimage/cibokehblur/softness)
- [CIBoxBlur](/documentation/coreimage/ciboxblur)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciboxblur/inputimage)
- [var radius: Float](/documentation/coreimage/ciboxblur/radius)
- [CIDiscBlur](/documentation/coreimage/cidiscblur)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidiscblur/inputimage)
- [var radius: Float](/documentation/coreimage/cidiscblur/radius)
- [CIGaussianBlur](/documentation/coreimage/cigaussianblur)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigaussianblur/inputimage)
- [var radius: Float](/documentation/coreimage/cigaussianblur/radius)
- [CIMaskedVariableBlur](/documentation/coreimage/cimaskedvariableblur)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimaskedvariableblur/inputimage)
- [var mask: CIImage?](/documentation/coreimage/cimaskedvariableblur/mask)
- [var radius: Float](/documentation/coreimage/cimaskedvariableblur/radius)
- [CIMedian](/documentation/coreimage/cimedian)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimedian/inputimage)
- [CIMorphologyGradient](/documentation/coreimage/cimorphologygradient)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologygradient/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologygradient/radius)
- [CIMorphologyMaximum](/documentation/coreimage/cimorphologymaximum)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologymaximum/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologymaximum/radius)
- [CIMorphologyMinimum](/documentation/coreimage/cimorphologyminimum)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyminimum/inputimage)
- [var radius: Float](/documentation/coreimage/cimorphologyminimum/radius)
- [CIMorphologyRectangleMaximum](/documentation/coreimage/cimorphologyrectanglemaximum)

#### Instance Properties

- [var height: Float](/documentation/coreimage/cimorphologyrectanglemaximum/height)
- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyrectanglemaximum/inputimage)
- [var width: Float](/documentation/coreimage/cimorphologyrectanglemaximum/width)
- [CIMorphologyRectangleMinimum](/documentation/coreimage/cimorphologyrectangleminimum)

#### Instance Properties

- [var height: Float](/documentation/coreimage/cimorphologyrectangleminimum/height)
- [var inputImage: CIImage?](/documentation/coreimage/cimorphologyrectangleminimum/inputimage)
- [var width: Float](/documentation/coreimage/cimorphologyrectangleminimum/width)
- [CIMotionBlur](/documentation/coreimage/cimotionblur)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cimotionblur/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cimotionblur/inputimage)
- [var radius: Float](/documentation/coreimage/cimotionblur/radius)
- [CINoiseReduction](/documentation/coreimage/cinoisereduction)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cinoisereduction/inputimage)
- [var noiseLevel: Float](/documentation/coreimage/cinoisereduction/noiselevel)
- [var sharpness: Float](/documentation/coreimage/cinoisereduction/sharpness)
- [CIZoomBlur](/documentation/coreimage/cizoomblur)

#### Instance Properties

- [var amount: Float](/documentation/coreimage/cizoomblur/amount)
- [var center: CGPoint](/documentation/coreimage/cizoomblur/center)
- [var inputImage: CIImage?](/documentation/coreimage/cizoomblur/inputimage)
- [Color Adjustment Filters](/documentation/coreimage/color-adjustment-filters)

### Filters

- [class func colorAbsoluteDifference() -> any CIFilter & CIColorAbsoluteDifference](/documentation/coreimage/cifilter-swift.class/colorabsolutedifference())
- [class func colorClamp() -> any CIFilter & CIColorClamp](/documentation/coreimage/cifilter-swift.class/colorclamp())
- [class func colorControls() -> any CIFilter & CIColorControls](/documentation/coreimage/cifilter-swift.class/colorcontrols())
- [class func colorMatrix() -> any CIFilter & CIColorMatrix](/documentation/coreimage/cifilter-swift.class/colormatrix())
- [class func colorPolynomial() -> any CIFilter & CIColorPolynomial](/documentation/coreimage/cifilter-swift.class/colorpolynomial())
- [class func colorThreshold() -> any CIFilter & CIColorThreshold](/documentation/coreimage/cifilter-swift.class/colorthreshold())
- [class func colorThresholdOtsu() -> any CIFilter & CIColorThresholdOtsu](/documentation/coreimage/cifilter-swift.class/colorthresholdotsu())
- [class func depthToDisparity() -> any CIFilter & CIDepthToDisparity](/documentation/coreimage/cifilter-swift.class/depthtodisparity())
- [class func disparityToDepth() -> any CIFilter & CIDisparityToDepth](/documentation/coreimage/cifilter-swift.class/disparitytodepth())
- [class func exposureAdjust() -> any CIFilter & CIExposureAdjust](/documentation/coreimage/cifilter-swift.class/exposureadjust())
- [class func gammaAdjust() -> any CIFilter & CIGammaAdjust](/documentation/coreimage/cifilter-swift.class/gammaadjust())
- [class func hueAdjust() -> any CIFilter & CIHueAdjust](/documentation/coreimage/cifilter-swift.class/hueadjust())
- [class func linearToSRGBToneCurve() -> any CIFilter & CILinearToSRGBToneCurve](/documentation/coreimage/cifilter-swift.class/lineartosrgbtonecurve())
- [class func sRGBToneCurveToLinear() -> any CIFilter & CISRGBToneCurveToLinear](/documentation/coreimage/cifilter-swift.class/srgbtonecurvetolinear())
- [class func temperatureAndTint() -> any CIFilter & CITemperatureAndTint](/documentation/coreimage/cifilter-swift.class/temperatureandtint())
- [class func toneCurve() -> any CIFilter & CIToneCurve](/documentation/coreimage/cifilter-swift.class/tonecurve())
- [class func vibrance() -> any CIFilter & CIVibrance](/documentation/coreimage/cifilter-swift.class/vibrance())
- [class func whitePointAdjust() -> any CIFilter & CIWhitePointAdjust](/documentation/coreimage/cifilter-swift.class/whitepointadjust())

### Protocols

- [CIColorAbsoluteDifference](/documentation/coreimage/cicolorabsolutedifference)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorabsolutedifference/inputimage)
- [var inputImage2: CIImage?](/documentation/coreimage/cicolorabsolutedifference/inputimage2)
- [CIColorClamp](/documentation/coreimage/cicolorclamp)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorclamp/inputimage)
- [var maxComponents: CIVector](/documentation/coreimage/cicolorclamp/maxcomponents)
- [var minComponents: CIVector](/documentation/coreimage/cicolorclamp/mincomponents)
- [CIColorControls](/documentation/coreimage/cicolorcontrols)

#### Instance Properties

- [var brightness: Float](/documentation/coreimage/cicolorcontrols/brightness)
- [var contrast: Float](/documentation/coreimage/cicolorcontrols/contrast)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcontrols/inputimage)
- [var saturation: Float](/documentation/coreimage/cicolorcontrols/saturation)
- [CIColorMatrix](/documentation/coreimage/cicolormatrix)

#### Instance Properties

- [var aVector: CIVector](/documentation/coreimage/cicolormatrix/avector)
- [var bVector: CIVector](/documentation/coreimage/cicolormatrix/bvector)
- [var gVector: CIVector](/documentation/coreimage/cicolormatrix/gvector)
- [var rVector: CIVector](/documentation/coreimage/cicolormatrix/rvector)
- [var biasVector: CIVector](/documentation/coreimage/cicolormatrix/biasvector)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormatrix/inputimage)
- [CIColorPolynomial](/documentation/coreimage/cicolorpolynomial)

#### Instance Properties

- [var alphaCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/alphacoefficients)
- [var blueCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/bluecoefficients)
- [var greenCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/greencoefficients)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorpolynomial/inputimage)
- [var redCoefficients: CIVector](/documentation/coreimage/cicolorpolynomial/redcoefficients)
- [CIColorThreshold](/documentation/coreimage/cicolorthreshold)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorthreshold/inputimage)
- [var threshold: Float](/documentation/coreimage/cicolorthreshold/threshold)
- [CIColorThresholdOtsu](/documentation/coreimage/cicolorthresholdotsu)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorthresholdotsu/inputimage)
- [CIDepthToDisparity](/documentation/coreimage/cidepthtodisparity)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidepthtodisparity/inputimage)
- [CIDisparityToDepth](/documentation/coreimage/cidisparitytodepth)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidisparitytodepth/inputimage)
- [CIExposureAdjust](/documentation/coreimage/ciexposureadjust)

#### Instance Properties

- [var ev: Float](/documentation/coreimage/ciexposureadjust/ev)
- [var inputImage: CIImage?](/documentation/coreimage/ciexposureadjust/inputimage)
- [CIGammaAdjust](/documentation/coreimage/cigammaadjust)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigammaadjust/inputimage)
- [var power: Float](/documentation/coreimage/cigammaadjust/power)
- [CIHueAdjust](/documentation/coreimage/cihueadjust)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cihueadjust/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cihueadjust/inputimage)
- [CILinearToSRGBToneCurve](/documentation/coreimage/cilineartosrgbtonecurve)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cilineartosrgbtonecurve/inputimage)
- [CISRGBToneCurveToLinear](/documentation/coreimage/cisrgbtonecurvetolinear)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisrgbtonecurvetolinear/inputimage)
- [CISystemToneMap](/documentation/coreimage/cisystemtonemap)

#### Instance Properties

- [var displayHeadroom: Float](/documentation/coreimage/cisystemtonemap/displayheadroom)
- [var inputImage: CIImage?](/documentation/coreimage/cisystemtonemap/inputimage)
- [var preferredDynamicRange: CIDynamicRangeOption?](/documentation/coreimage/cisystemtonemap/preferreddynamicrange)
- [CITemperatureAndTint](/documentation/coreimage/citemperatureandtint)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citemperatureandtint/inputimage)
- [var neutral: CIVector](/documentation/coreimage/citemperatureandtint/neutral)
- [var targetNeutral: CIVector](/documentation/coreimage/citemperatureandtint/targetneutral)
- [CIToneCurve](/documentation/coreimage/citonecurve)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citonecurve/inputimage)
- [var point0: CGPoint](/documentation/coreimage/citonecurve/point0)
- [var point1: CGPoint](/documentation/coreimage/citonecurve/point1)
- [var point2: CGPoint](/documentation/coreimage/citonecurve/point2)
- [var point3: CGPoint](/documentation/coreimage/citonecurve/point3)
- [var point4: CGPoint](/documentation/coreimage/citonecurve/point4)
- [var extrapolate: Bool](/documentation/coreimage/citonecurve/extrapolate)
- [CIVibrance](/documentation/coreimage/civibrance)

#### Instance Properties

- [var amount: Float](/documentation/coreimage/civibrance/amount)
- [var inputImage: CIImage?](/documentation/coreimage/civibrance/inputimage)
- [CIWhitePointAdjust](/documentation/coreimage/ciwhitepointadjust)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciwhitepointadjust/color)
- [var inputImage: CIImage?](/documentation/coreimage/ciwhitepointadjust/inputimage)
- [Color Effect Filters](/documentation/coreimage/color-effect-filters)

### Color Effect Filters

- [class func colorCrossPolynomial() -> any CIFilter & CIColorCrossPolynomial](/documentation/coreimage/cifilter-swift.class/colorcrosspolynomial())
- [class func colorCube() -> any CIFilter & CIColorCube](/documentation/coreimage/cifilter-swift.class/colorcube())
- [class func colorCubeWithColorSpace() -> any CIFilter & CIColorCubeWithColorSpace](/documentation/coreimage/cifilter-swift.class/colorcubewithcolorspace())
- [class func colorCubesMixedWithMask() -> any CIFilter & CIColorCubesMixedWithMask](/documentation/coreimage/cifilter-swift.class/colorcubesmixedwithmask())
- [class func colorCurves() -> any CIFilter & CIColorCurves](/documentation/coreimage/cifilter-swift.class/colorcurves())
- [class func colorInvert() -> any CIFilter & CIColorInvert](/documentation/coreimage/cifilter-swift.class/colorinvert())
- [class func colorMap() -> any CIFilter & CIColorMap](/documentation/coreimage/cifilter-swift.class/colormap())
- [class func colorMonochrome() -> any CIFilter & CIColorMonochrome](/documentation/coreimage/cifilter-swift.class/colormonochrome())
- [class func colorPosterize() -> any CIFilter & CIColorPosterize](/documentation/coreimage/cifilter-swift.class/colorposterize())
- [class func convertLabToRGB() -> any CIFilter & CIConvertLab](/documentation/coreimage/cifilter-swift.class/convertlabtorgb())
- [class func convertRGBtoLab() -> any CIFilter & CIConvertLab](/documentation/coreimage/cifilter-swift.class/convertrgbtolab())
- [class func dither() -> any CIFilter & CIDither](/documentation/coreimage/cifilter-swift.class/dither())
- [class func documentEnhancer() -> any CIFilter & CIDocumentEnhancer](/documentation/coreimage/cifilter-swift.class/documentenhancer())
- [class func falseColor() -> any CIFilter & CIFalseColor](/documentation/coreimage/cifilter-swift.class/falsecolor())
- [class func labDeltaE() -> any CIFilter & CILabDeltaE](/documentation/coreimage/cifilter-swift.class/labdeltae())
- [class func maskToAlpha() -> any CIFilter & CIMaskToAlpha](/documentation/coreimage/cifilter-swift.class/masktoalpha())
- [class func maximumComponent() -> any CIFilter & CIMaximumComponent](/documentation/coreimage/cifilter-swift.class/maximumcomponent())
- [class func minimumComponent() -> any CIFilter & CIMinimumComponent](/documentation/coreimage/cifilter-swift.class/minimumcomponent())
- [class func paletteCentroid() -> any CIFilter & CIPaletteCentroid](/documentation/coreimage/cifilter-swift.class/palettecentroid())
- [class func palettize() -> any CIFilter & CIPalettize](/documentation/coreimage/cifilter-swift.class/palettize())
- [class func photoEffectChrome() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectchrome())
- [class func photoEffectFade() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectfade())
- [class func photoEffectInstant() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectinstant())
- [class func photoEffectMono() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectmono())
- [class func photoEffectNoir() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectnoir())
- [class func photoEffectProcess() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffectprocess())
- [class func photoEffectTonal() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffecttonal())
- [class func photoEffectTransfer() -> any CIFilter & CIPhotoEffect](/documentation/coreimage/cifilter-swift.class/photoeffecttransfer())
- [class func sepiaTone() -> any CIFilter & CISepiaTone](/documentation/coreimage/cifilter-swift.class/sepiatone())
- [class func thermal() -> any CIFilter & CIThermal](/documentation/coreimage/cifilter-swift.class/thermal())
- [class func vignette() -> any CIFilter & CIVignette](/documentation/coreimage/cifilter-swift.class/vignette())
- [class func vignetteEffect() -> any CIFilter & CIVignetteEffect](/documentation/coreimage/cifilter-swift.class/vignetteeffect())
- [class func xRay() -> any CIFilter & CIXRay](/documentation/coreimage/cifilter-swift.class/xray())

### Protocols

- [CIColorCrossPolynomial](/documentation/coreimage/cicolorcrosspolynomial)

#### Instance Properties

- [var blueCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/bluecoefficients)
- [var greenCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/greencoefficients)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcrosspolynomial/inputimage)
- [var redCoefficients: CIVector](/documentation/coreimage/cicolorcrosspolynomial/redcoefficients)
- [CIColorCube](/documentation/coreimage/cicolorcube)

#### Instance Properties

- [var cubeData: Data](/documentation/coreimage/cicolorcube/cubedata)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcube/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcube/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcube/extrapolate)
- [CIColorCubeWithColorSpace](/documentation/coreimage/cicolorcubewithcolorspace)

#### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcubewithcolorspace/colorspace)
- [var cubeData: Data](/documentation/coreimage/cicolorcubewithcolorspace/cubedata)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcubewithcolorspace/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcubewithcolorspace/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcubewithcolorspace/extrapolate)
- [CIColorCubesMixedWithMask](/documentation/coreimage/cicolorcubesmixedwithmask)

#### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcubesmixedwithmask/colorspace)
- [var cube0Data: Data](/documentation/coreimage/cicolorcubesmixedwithmask/cube0data)
- [var cube1Data: Data](/documentation/coreimage/cicolorcubesmixedwithmask/cube1data)
- [var cubeDimension: Float](/documentation/coreimage/cicolorcubesmixedwithmask/cubedimension)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcubesmixedwithmask/inputimage)
- [var maskImage: CIImage?](/documentation/coreimage/cicolorcubesmixedwithmask/maskimage)
- [var extrapolate: Bool](/documentation/coreimage/cicolorcubesmixedwithmask/extrapolate)
- [CIColorCurves](/documentation/coreimage/cicolorcurves)

#### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cicolorcurves/colorspace)
- [var curvesData: Data](/documentation/coreimage/cicolorcurves/curvesdata)
- [var curvesDomain: CIVector](/documentation/coreimage/cicolorcurves/curvesdomain)
- [var inputImage: CIImage?](/documentation/coreimage/cicolorcurves/inputimage)
- [CIColorInvert](/documentation/coreimage/cicolorinvert)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorinvert/inputimage)
- [CIColorMap](/documentation/coreimage/cicolormap)

#### Instance Properties

- [var gradientImage: CIImage?](/documentation/coreimage/cicolormap/gradientimage)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormap/inputimage)
- [CIColorMonochrome](/documentation/coreimage/cicolormonochrome)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/cicolormonochrome/color)
- [var inputImage: CIImage?](/documentation/coreimage/cicolormonochrome/inputimage)
- [var intensity: Float](/documentation/coreimage/cicolormonochrome/intensity)
- [CIConvertLab](/documentation/coreimage/ciconvertlab)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciconvertlab/inputimage)
- [var normalize: Bool](/documentation/coreimage/ciconvertlab/normalize)
- [CIDither](/documentation/coreimage/cidither)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidither/inputimage)
- [var intensity: Float](/documentation/coreimage/cidither/intensity)
- [CIColorPosterize](/documentation/coreimage/cicolorposterize)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicolorposterize/inputimage)
- [var levels: Float](/documentation/coreimage/cicolorposterize/levels)
- [CIDocumentEnhancer](/documentation/coreimage/cidocumentenhancer)

#### Instance Properties

- [var amount: Float](/documentation/coreimage/cidocumentenhancer/amount)
- [var inputImage: CIImage?](/documentation/coreimage/cidocumentenhancer/inputimage)
- [CIFalseColor](/documentation/coreimage/cifalsecolor)

#### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cifalsecolor/color0)
- [var color1: CIColor](/documentation/coreimage/cifalsecolor/color1)
- [var inputImage: CIImage?](/documentation/coreimage/cifalsecolor/inputimage)
- [CILabDeltaE](/documentation/coreimage/cilabdeltae)

#### Instance Properties

- [var image2: CIImage?](/documentation/coreimage/cilabdeltae/image2)
- [var inputImage: CIImage?](/documentation/coreimage/cilabdeltae/inputimage)
- [CIMaskToAlpha](/documentation/coreimage/cimasktoalpha)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimasktoalpha/inputimage)
- [CIMaximumComponent](/documentation/coreimage/cimaximumcomponent)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cimaximumcomponent/inputimage)
- [CIMinimumComponent](/documentation/coreimage/ciminimumcomponent)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciminimumcomponent/inputimage)
- [CIPaletteCentroid](/documentation/coreimage/cipalettecentroid)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipalettecentroid/inputimage)
- [var paletteImage: CIImage?](/documentation/coreimage/cipalettecentroid/paletteimage)
- [var perceptual: Bool](/documentation/coreimage/cipalettecentroid/perceptual)
- [CIPalettize](/documentation/coreimage/cipalettize)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipalettize/inputimage)
- [var paletteImage: CIImage?](/documentation/coreimage/cipalettize/paletteimage)
- [var perceptual: Bool](/documentation/coreimage/cipalettize/perceptual)
- [CIPhotoEffect](/documentation/coreimage/ciphotoeffect)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciphotoeffect/inputimage)
- [var extrapolate: Bool](/documentation/coreimage/ciphotoeffect/extrapolate)
- [CISepiaTone](/documentation/coreimage/cisepiatone)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisepiatone/inputimage)
- [var intensity: Float](/documentation/coreimage/cisepiatone/intensity)
- [CIThermal](/documentation/coreimage/cithermal)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cithermal/inputimage)
- [CIVignette](/documentation/coreimage/civignette)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/civignette/inputimage)
- [var intensity: Float](/documentation/coreimage/civignette/intensity)
- [var radius: Float](/documentation/coreimage/civignette/radius)
- [CIVignetteEffect](/documentation/coreimage/civignetteeffect)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/civignetteeffect/center)
- [var falloff: Float](/documentation/coreimage/civignetteeffect/falloff)
- [var inputImage: CIImage?](/documentation/coreimage/civignetteeffect/inputimage)
- [var intensity: Float](/documentation/coreimage/civignetteeffect/intensity)
- [var radius: Float](/documentation/coreimage/civignetteeffect/radius)
- [CIXRay](/documentation/coreimage/cixray)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cixray/inputimage)
- [Composite Operations](/documentation/coreimage/composite-operations)

### Filters

- [class func additionCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/additioncompositing())
- [class func colorBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colorblendmode())
- [class func colorBurnBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colorburnblendmode())
- [class func colorDodgeBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/colordodgeblendmode())
- [class func darkenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/darkenblendmode())
- [class func differenceBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/differenceblendmode())
- [class func divideBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/divideblendmode())
- [class func exclusionBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/exclusionblendmode())
- [class func hardLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/hardlightblendmode())
- [class func hueBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/hueblendmode())
- [class func lightenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/lightenblendmode())
- [class func linearBurnBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/linearburnblendmode())
- [class func linearDodgeBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/lineardodgeblendmode())
- [class func linearLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/linearlightblendmode())
- [class func luminosityBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/luminosityblendmode())
- [class func minimumCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/minimumcompositing())
- [class func maximumCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/maximumcompositing())
- [class func multiplyBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/multiplyblendmode())
- [class func multiplyCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/multiplycompositing())
- [class func overlayBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/overlayblendmode())
- [class func pinLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/pinlightblendmode())
- [class func saturationBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/saturationblendmode())
- [class func screenBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/screenblendmode())
- [class func softLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/softlightblendmode())
- [class func sourceAtopCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceatopcompositing())
- [class func sourceInCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceincompositing())
- [class func sourceOutCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceoutcompositing())
- [class func sourceOverCompositing() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/sourceovercompositing())
- [class func subtractBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/subtractblendmode())
- [class func vividLightBlendMode() -> any CIFilter & CICompositeOperation](/documentation/coreimage/cifilter-swift.class/vividlightblendmode())

### Protocols

- [CICompositeOperation](/documentation/coreimage/cicompositeoperation)

#### Instance Properties

- [var backgroundImage: CIImage?](/documentation/coreimage/cicompositeoperation/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/cicompositeoperation/inputimage)
- [Convolution Filters](/documentation/coreimage/convolution-filters)

### Filters

- [class func convolution3X3() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution3x3())
- [class func convolution5X5() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution5x5())
- [class func convolution7X7() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution7x7())
- [class func convolution9Horizontal() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution9horizontal())
- [class func convolution9Vertical() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolution9vertical())
- [class func convolutionRGB3X3() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb3x3())
- [class func convolutionRGB5X5() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb5x5())
- [class func convolutionRGB7X7() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb7x7())
- [class func convolutionRGB9Horizontal() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb9horizontal())
- [class func convolutionRGB9Vertical() -> any CIFilter & CIConvolution](/documentation/coreimage/cifilter-swift.class/convolutionrgb9vertical())

### Protocols

- [CIConvolution](/documentation/coreimage/ciconvolution)

#### Instance Properties

- [var bias: Float](/documentation/coreimage/ciconvolution/bias)
- [var inputImage: CIImage?](/documentation/coreimage/ciconvolution/inputimage)
- [var weights: CIVector](/documentation/coreimage/ciconvolution/weights)
- [Distortion Filters](/documentation/coreimage/distortion-filters)

### Filters

- [class func bumpDistortion() -> any CIFilter & CIBumpDistortion](/documentation/coreimage/cifilter-swift.class/bumpdistortion())
- [class func bumpDistortionLinear() -> any CIFilter & CIBumpDistortionLinear](/documentation/coreimage/cifilter-swift.class/bumpdistortionlinear())
- [class func circleSplashDistortion() -> any CIFilter & CICircleSplashDistortion](/documentation/coreimage/cifilter-swift.class/circlesplashdistortion())
- [class func circularWrap() -> any CIFilter & CICircularWrap](/documentation/coreimage/cifilter-swift.class/circularwrap())
- [class func displacementDistortion() -> any CIFilter & CIDisplacementDistortion](/documentation/coreimage/cifilter-swift.class/displacementdistortion())
- [class func droste() -> any CIFilter & CIDroste](/documentation/coreimage/cifilter-swift.class/droste())
- [class func glassDistortion() -> any CIFilter & CIGlassDistortion](/documentation/coreimage/cifilter-swift.class/glassdistortion())
- [class func glassLozenge() -> any CIFilter & CIGlassLozenge](/documentation/coreimage/cifilter-swift.class/glasslozenge())
- [class func holeDistortion() -> any CIFilter & CIHoleDistortion](/documentation/coreimage/cifilter-swift.class/holedistortion())
- [class func lightTunnel() -> any CIFilter & CILightTunnel](/documentation/coreimage/cifilter-swift.class/lighttunnel())
- [class func ninePartStretched() -> any CIFilter & CINinePartStretched](/documentation/coreimage/cifilter-swift.class/ninepartstretched())
- [class func ninePartTiled() -> any CIFilter & CINinePartTiled](/documentation/coreimage/cifilter-swift.class/nineparttiled())
- [class func pinchDistortion() -> any CIFilter & CIPinchDistortion](/documentation/coreimage/cifilter-swift.class/pinchdistortion())
- [class func stretchCrop() -> any CIFilter & CIStretchCrop](/documentation/coreimage/cifilter-swift.class/stretchcrop())
- [class func torusLensDistortion() -> any CIFilter & CITorusLensDistortion](/documentation/coreimage/cifilter-swift.class/toruslensdistortion())
- [class func twirlDistortion() -> any CIFilter & CITwirlDistortion](/documentation/coreimage/cifilter-swift.class/twirldistortion())
- [class func vortexDistortion() -> any CIFilter & CIVortexDistortion](/documentation/coreimage/cifilter-swift.class/vortexdistortion())

### Protocols

- [CIBumpDistortion](/documentation/coreimage/cibumpdistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cibumpdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cibumpdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cibumpdistortion/radius)
- [var scale: Float](/documentation/coreimage/cibumpdistortion/scale)
- [CIBumpDistortionLinear](/documentation/coreimage/cibumpdistortionlinear)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cibumpdistortionlinear/angle)
- [var center: CGPoint](/documentation/coreimage/cibumpdistortionlinear/center)
- [var inputImage: CIImage?](/documentation/coreimage/cibumpdistortionlinear/inputimage)
- [var radius: Float](/documentation/coreimage/cibumpdistortionlinear/radius)
- [var scale: Float](/documentation/coreimage/cibumpdistortionlinear/scale)
- [CICircleSplashDistortion](/documentation/coreimage/cicirclesplashdistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicirclesplashdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicirclesplashdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cicirclesplashdistortion/radius)
- [CICircularWrap](/documentation/coreimage/cicircularwrap)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cicircularwrap/angle)
- [var center: CGPoint](/documentation/coreimage/cicircularwrap/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicircularwrap/inputimage)
- [var radius: Float](/documentation/coreimage/cicircularwrap/radius)
- [CIDisplacementDistortion](/documentation/coreimage/cidisplacementdistortion)

#### Instance Properties

- [var displacementImage: CIImage?](/documentation/coreimage/cidisplacementdistortion/displacementimage)
- [var inputImage: CIImage?](/documentation/coreimage/cidisplacementdistortion/inputimage)
- [var scale: Float](/documentation/coreimage/cidisplacementdistortion/scale)
- [CIDroste](/documentation/coreimage/cidroste)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidroste/inputimage)
- [var insetPoint0: CGPoint](/documentation/coreimage/cidroste/insetpoint0)
- [var insetPoint1: CGPoint](/documentation/coreimage/cidroste/insetpoint1)
- [var periodicity: Float](/documentation/coreimage/cidroste/periodicity)
- [var rotation: Float](/documentation/coreimage/cidroste/rotation)
- [var strands: Float](/documentation/coreimage/cidroste/strands)
- [var zoom: Float](/documentation/coreimage/cidroste/zoom)
- [CIGlassDistortion](/documentation/coreimage/ciglassdistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciglassdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciglassdistortion/inputimage)
- [var scale: Float](/documentation/coreimage/ciglassdistortion/scale)
- [var textureImage: CIImage?](/documentation/coreimage/ciglassdistortion/textureimage)
- [CIGlassLozenge](/documentation/coreimage/ciglasslozenge)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciglasslozenge/inputimage)
- [var point0: CGPoint](/documentation/coreimage/ciglasslozenge/point0)
- [var point1: CGPoint](/documentation/coreimage/ciglasslozenge/point1)
- [var radius: Float](/documentation/coreimage/ciglasslozenge/radius)
- [var refraction: Float](/documentation/coreimage/ciglasslozenge/refraction)
- [CIHoleDistortion](/documentation/coreimage/ciholedistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciholedistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciholedistortion/inputimage)
- [var radius: Float](/documentation/coreimage/ciholedistortion/radius)
- [CILightTunnel](/documentation/coreimage/cilighttunnel)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cilighttunnel/center)
- [var inputImage: CIImage?](/documentation/coreimage/cilighttunnel/inputimage)
- [var radius: Float](/documentation/coreimage/cilighttunnel/radius)
- [var rotation: Float](/documentation/coreimage/cilighttunnel/rotation)
- [CINinePartStretched](/documentation/coreimage/cininepartstretched)

#### Instance Properties

- [var breakpoint0: CGPoint](/documentation/coreimage/cininepartstretched/breakpoint0)
- [var breakpoint1: CGPoint](/documentation/coreimage/cininepartstretched/breakpoint1)
- [var growAmount: CGPoint](/documentation/coreimage/cininepartstretched/growamount)
- [var inputImage: CIImage?](/documentation/coreimage/cininepartstretched/inputimage)
- [CINinePartTiled](/documentation/coreimage/cinineparttiled)

#### Instance Properties

- [var breakpoint0: CGPoint](/documentation/coreimage/cinineparttiled/breakpoint0)
- [var breakpoint1: CGPoint](/documentation/coreimage/cinineparttiled/breakpoint1)
- [var flipYTiles: Bool](/documentation/coreimage/cinineparttiled/flipytiles)
- [var growAmount: CGPoint](/documentation/coreimage/cinineparttiled/growamount)
- [var inputImage: CIImage?](/documentation/coreimage/cinineparttiled/inputimage)
- [CIPinchDistortion](/documentation/coreimage/cipinchdistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipinchdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipinchdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/cipinchdistortion/radius)
- [var scale: Float](/documentation/coreimage/cipinchdistortion/scale)
- [CIStretchCrop](/documentation/coreimage/cistretchcrop)

#### Instance Properties

- [var centerStretchAmount: Float](/documentation/coreimage/cistretchcrop/centerstretchamount)
- [var cropAmount: Float](/documentation/coreimage/cistretchcrop/cropamount)
- [var inputImage: CIImage?](/documentation/coreimage/cistretchcrop/inputimage)
- [var size: CGPoint](/documentation/coreimage/cistretchcrop/size)
- [CITorusLensDistortion](/documentation/coreimage/citoruslensdistortion)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/citoruslensdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/citoruslensdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/citoruslensdistortion/radius)
- [var refraction: Float](/documentation/coreimage/citoruslensdistortion/refraction)
- [var width: Float](/documentation/coreimage/citoruslensdistortion/width)
- [CITwirlDistortion](/documentation/coreimage/citwirldistortion)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/citwirldistortion/angle)
- [var center: CGPoint](/documentation/coreimage/citwirldistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/citwirldistortion/inputimage)
- [var radius: Float](/documentation/coreimage/citwirldistortion/radius)
- [CIVortexDistortion](/documentation/coreimage/civortexdistortion)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/civortexdistortion/angle)
- [var center: CGPoint](/documentation/coreimage/civortexdistortion/center)
- [var inputImage: CIImage?](/documentation/coreimage/civortexdistortion/inputimage)
- [var radius: Float](/documentation/coreimage/civortexdistortion/radius)
- [Generator Filters](/documentation/coreimage/generator-filters)

### Filters

- [class func attributedTextImageGenerator() -> any CIFilter & CIAttributedTextImageGenerator](/documentation/coreimage/cifilter-swift.class/attributedtextimagegenerator())
- [class func aztecCodeGenerator() -> any CIFilter & CIAztecCodeGenerator](/documentation/coreimage/cifilter-swift.class/azteccodegenerator())
- [class func barcodeGenerator() -> any CIFilter & CIBarcodeGenerator](/documentation/coreimage/cifilter-swift.class/barcodegenerator())
- [class func blurredRectangleGenerator() -> any CIFilter & CIBlurredRectangleGenerator](/documentation/coreimage/cifilter-swift.class/blurredrectanglegenerator())
- [class func checkerboardGenerator() -> any CIFilter & CICheckerboardGenerator](/documentation/coreimage/cifilter-swift.class/checkerboardgenerator())
- [class func code128BarcodeGenerator() -> any CIFilter & CICode128BarcodeGenerator](/documentation/coreimage/cifilter-swift.class/code128barcodegenerator())
- [class func lenticularHaloGenerator() -> any CIFilter & CILenticularHaloGenerator](/documentation/coreimage/cifilter-swift.class/lenticularhalogenerator())
- [class func meshGenerator() -> any CIFilter & CIMeshGenerator](/documentation/coreimage/cifilter-swift.class/meshgenerator())
- [class func pdf417BarcodeGenerator() -> any CIFilter & CIPDF417BarcodeGenerator](/documentation/coreimage/cifilter-swift.class/pdf417barcodegenerator())
- [class func qrCodeGenerator() -> any CIFilter & CIQRCodeGenerator](/documentation/coreimage/cifilter-swift.class/qrcodegenerator())
- [class func randomGenerator() -> any CIFilter & CIRandomGenerator](/documentation/coreimage/cifilter-swift.class/randomgenerator())
- [class func roundedRectangleGenerator() -> any CIFilter & CIRoundedRectangleGenerator](/documentation/coreimage/cifilter-swift.class/roundedrectanglegenerator())
- [class func roundedRectangleStrokeGenerator() -> any CIFilter & CIRoundedRectangleStrokeGenerator](/documentation/coreimage/cifilter-swift.class/roundedrectanglestrokegenerator())
- [class func starShineGenerator() -> any CIFilter & CIStarShineGenerator](/documentation/coreimage/cifilter-swift.class/starshinegenerator())
- [class func stripesGenerator() -> any CIFilter & CIStripesGenerator](/documentation/coreimage/cifilter-swift.class/stripesgenerator())
- [class func sunbeamsGenerator() -> any CIFilter & CISunbeamsGenerator](/documentation/coreimage/cifilter-swift.class/sunbeamsgenerator())
- [class func textImageGenerator() -> any CIFilter & CITextImageGenerator](/documentation/coreimage/cifilter-swift.class/textimagegenerator())

### Protocols

- [CICode128BarcodeGenerator](/documentation/coreimage/cicode128barcodegenerator)

#### Instance Properties

- [var barcodeHeight: Float](/documentation/coreimage/cicode128barcodegenerator/barcodeheight)
- [var message: Data](/documentation/coreimage/cicode128barcodegenerator/message)
- [var quietSpace: Float](/documentation/coreimage/cicode128barcodegenerator/quietspace)
- [CIAttributedTextImageGenerator](/documentation/coreimage/ciattributedtextimagegenerator)

#### Instance Properties

- [var scaleFactor: Float](/documentation/coreimage/ciattributedtextimagegenerator/scalefactor)
- [var text: NSAttributedString](/documentation/coreimage/ciattributedtextimagegenerator/text)
- [var padding: Float](/documentation/coreimage/ciattributedtextimagegenerator/padding)
- [CIAztecCodeGenerator](/documentation/coreimage/ciazteccodegenerator)

#### Instance Properties

- [var compactStyle: Float](/documentation/coreimage/ciazteccodegenerator/compactstyle)
- [var correctionLevel: Float](/documentation/coreimage/ciazteccodegenerator/correctionlevel)
- [var layers: Float](/documentation/coreimage/ciazteccodegenerator/layers)
- [var message: Data](/documentation/coreimage/ciazteccodegenerator/message)
- [CIBarcodeGenerator](/documentation/coreimage/cibarcodegenerator)

#### Instance Properties

- [var barcodeDescriptor: CIBarcodeDescriptor](/documentation/coreimage/cibarcodegenerator/barcodedescriptor)
- [CIBlurredRectangleGenerator](/documentation/coreimage/ciblurredrectanglegenerator)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciblurredrectanglegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciblurredrectanglegenerator/extent)
- [var sigma: Float](/documentation/coreimage/ciblurredrectanglegenerator/sigma)
- [CIRoundedRectangleStrokeGenerator](/documentation/coreimage/ciroundedrectanglestrokegenerator)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglestrokegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglestrokegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/radius)
- [var width: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/width)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/smoothness)
- [CICheckerboardGenerator](/documentation/coreimage/cicheckerboardgenerator)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicheckerboardgenerator/center)
- [var color0: CIColor](/documentation/coreimage/cicheckerboardgenerator/color0)
- [var color1: CIColor](/documentation/coreimage/cicheckerboardgenerator/color1)
- [var sharpness: Float](/documentation/coreimage/cicheckerboardgenerator/sharpness)
- [var width: Float](/documentation/coreimage/cicheckerboardgenerator/width)
- [CILenticularHaloGenerator](/documentation/coreimage/cilenticularhalogenerator)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cilenticularhalogenerator/center)
- [var color: CIColor](/documentation/coreimage/cilenticularhalogenerator/color)
- [var haloOverlap: Float](/documentation/coreimage/cilenticularhalogenerator/halooverlap)
- [var haloRadius: Float](/documentation/coreimage/cilenticularhalogenerator/haloradius)
- [var haloWidth: Float](/documentation/coreimage/cilenticularhalogenerator/halowidth)
- [var striationContrast: Float](/documentation/coreimage/cilenticularhalogenerator/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/cilenticularhalogenerator/striationstrength)
- [var time: Float](/documentation/coreimage/cilenticularhalogenerator/time)
- [CIMeshGenerator](/documentation/coreimage/cimeshgenerator)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/cimeshgenerator/color)
- [var mesh: [Any]](/documentation/coreimage/cimeshgenerator/mesh)
- [var width: Float](/documentation/coreimage/cimeshgenerator/width)
- [CIPDF417BarcodeGenerator](/documentation/coreimage/cipdf417barcodegenerator)

#### Instance Properties

- [var alwaysSpecifyCompaction: Float](/documentation/coreimage/cipdf417barcodegenerator/alwaysspecifycompaction)
- [var compactStyle: Float](/documentation/coreimage/cipdf417barcodegenerator/compactstyle)
- [var compactionMode: Float](/documentation/coreimage/cipdf417barcodegenerator/compactionmode)
- [var correctionLevel: Float](/documentation/coreimage/cipdf417barcodegenerator/correctionlevel)
- [var dataColumns: Float](/documentation/coreimage/cipdf417barcodegenerator/datacolumns)
- [var maxHeight: Float](/documentation/coreimage/cipdf417barcodegenerator/maxheight)
- [var maxWidth: Float](/documentation/coreimage/cipdf417barcodegenerator/maxwidth)
- [var message: Data](/documentation/coreimage/cipdf417barcodegenerator/message)
- [var minHeight: Float](/documentation/coreimage/cipdf417barcodegenerator/minheight)
- [var minWidth: Float](/documentation/coreimage/cipdf417barcodegenerator/minwidth)
- [var preferredAspectRatio: Float](/documentation/coreimage/cipdf417barcodegenerator/preferredaspectratio)
- [var rows: Float](/documentation/coreimage/cipdf417barcodegenerator/rows)
- [CIQRCodeGenerator](/documentation/coreimage/ciqrcodegenerator)

#### Instance Properties

- [var correctionLevel: String](/documentation/coreimage/ciqrcodegenerator/correctionlevel)
- [var message: Data](/documentation/coreimage/ciqrcodegenerator/message)
- [CIRandomGenerator](/documentation/coreimage/cirandomgenerator)
- [CIRoundedRectangleGenerator](/documentation/coreimage/ciroundedrectanglegenerator)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglegenerator/radius)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglegenerator/smoothness)
- [CIRoundedRectangleStrokeGenerator](/documentation/coreimage/ciroundedrectanglestrokegenerator)

#### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciroundedrectanglestrokegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciroundedrectanglestrokegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/radius)
- [var width: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/width)
- [var smoothness: Float](/documentation/coreimage/ciroundedrectanglestrokegenerator/smoothness)
- [CIStarShineGenerator](/documentation/coreimage/cistarshinegenerator)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cistarshinegenerator/center)
- [var color: CIColor](/documentation/coreimage/cistarshinegenerator/color)
- [var crossAngle: Float](/documentation/coreimage/cistarshinegenerator/crossangle)
- [var crossOpacity: Float](/documentation/coreimage/cistarshinegenerator/crossopacity)
- [var crossScale: Float](/documentation/coreimage/cistarshinegenerator/crossscale)
- [var crossWidth: Float](/documentation/coreimage/cistarshinegenerator/crosswidth)
- [var epsilon: Float](/documentation/coreimage/cistarshinegenerator/epsilon)
- [var radius: Float](/documentation/coreimage/cistarshinegenerator/radius)
- [CIStripesGenerator](/documentation/coreimage/cistripesgenerator)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cistripesgenerator/center)
- [var color0: CIColor](/documentation/coreimage/cistripesgenerator/color0)
- [var color1: CIColor](/documentation/coreimage/cistripesgenerator/color1)
- [var sharpness: Float](/documentation/coreimage/cistripesgenerator/sharpness)
- [var width: Float](/documentation/coreimage/cistripesgenerator/width)
- [CISunbeamsGenerator](/documentation/coreimage/cisunbeamsgenerator)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cisunbeamsgenerator/center)
- [var color: CIColor](/documentation/coreimage/cisunbeamsgenerator/color)
- [var maxStriationRadius: Float](/documentation/coreimage/cisunbeamsgenerator/maxstriationradius)
- [var striationContrast: Float](/documentation/coreimage/cisunbeamsgenerator/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/cisunbeamsgenerator/striationstrength)
- [var sunRadius: Float](/documentation/coreimage/cisunbeamsgenerator/sunradius)
- [var time: Float](/documentation/coreimage/cisunbeamsgenerator/time)
- [CITextImageGenerator](/documentation/coreimage/citextimagegenerator)

#### Instance Properties

- [var fontName: String](/documentation/coreimage/citextimagegenerator/fontname)
- [var fontSize: Float](/documentation/coreimage/citextimagegenerator/fontsize)
- [var scaleFactor: Float](/documentation/coreimage/citextimagegenerator/scalefactor)
- [var text: String](/documentation/coreimage/citextimagegenerator/text)
- [var padding: Float](/documentation/coreimage/citextimagegenerator/padding)
- [Geometry Adjustment Filters](/documentation/coreimage/geometry-adjustment-filters)

### Filters

- [class func bicubicScaleTransform() -> any CIFilter & CIBicubicScaleTransform](/documentation/coreimage/cifilter-swift.class/bicubicscaletransform())
- [class func edgePreserveUpsample() -> any CIFilter & CIEdgePreserveUpsample](/documentation/coreimage/cifilter-swift.class/edgepreserveupsample())
- [class func keystoneCorrectionCombined() -> any CIFilter & CIKeystoneCorrectionCombined](/documentation/coreimage/cifilter-swift.class/keystonecorrectioncombined())
- [class func keystoneCorrectionHorizontal() -> any CIFilter & CIKeystoneCorrectionHorizontal](/documentation/coreimage/cifilter-swift.class/keystonecorrectionhorizontal())
- [class func keystoneCorrectionVertical() -> any CIFilter & CIKeystoneCorrectionVertical](/documentation/coreimage/cifilter-swift.class/keystonecorrectionvertical())
- [class func lanczosScaleTransform() -> any CIFilter & CILanczosScaleTransform](/documentation/coreimage/cifilter-swift.class/lanczosscaletransform())
- [class func perspectiveCorrection() -> any CIFilter & CIPerspectiveCorrection](/documentation/coreimage/cifilter-swift.class/perspectivecorrection())
- [class func perspectiveRotate() -> any CIFilter & CIPerspectiveRotate](/documentation/coreimage/cifilter-swift.class/perspectiverotate())
- [class func perspectiveTransform() -> any CIFilter & CIPerspectiveTransform](/documentation/coreimage/cifilter-swift.class/perspectivetransform())
- [class func perspectiveTransformWithExtent() -> any CIFilter & CIPerspectiveTransformWithExtent](/documentation/coreimage/cifilter-swift.class/perspectivetransformwithextent())
- [class func straighten() -> any CIFilter & CIStraighten](/documentation/coreimage/cifilter-swift.class/straighten())

### Protocols

- [CIBicubicScaleTransform](/documentation/coreimage/cibicubicscaletransform)

#### Instance Properties

- [var aspectRatio: Float](/documentation/coreimage/cibicubicscaletransform/aspectratio)
- [var inputImage: CIImage?](/documentation/coreimage/cibicubicscaletransform/inputimage)
- [var parameterB: Float](/documentation/coreimage/cibicubicscaletransform/parameterb)
- [var parameterC: Float](/documentation/coreimage/cibicubicscaletransform/parameterc)
- [var scale: Float](/documentation/coreimage/cibicubicscaletransform/scale)
- [CIEdgePreserveUpsample](/documentation/coreimage/ciedgepreserveupsample)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedgepreserveupsample/inputimage)
- [var lumaSigma: Float](/documentation/coreimage/ciedgepreserveupsample/lumasigma)
- [var smallImage: CIImage?](/documentation/coreimage/ciedgepreserveupsample/smallimage)
- [var spatialSigma: Float](/documentation/coreimage/ciedgepreserveupsample/spatialsigma)
- [CIFourCoordinateGeometryFilter](/documentation/coreimage/cifourcoordinategeometryfilter)

#### Instance Properties

- [var bottomLeft: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/bottomleft)
- [var bottomRight: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/bottomright)
- [var inputImage: CIImage?](/documentation/coreimage/cifourcoordinategeometryfilter/inputimage)
- [var topLeft: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/topleft)
- [var topRight: CGPoint](/documentation/coreimage/cifourcoordinategeometryfilter/topright)
- [CIKeystoneCorrectionCombined](/documentation/coreimage/cikeystonecorrectioncombined)

#### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectioncombined/focallength)
- [CIKeystoneCorrectionHorizontal](/documentation/coreimage/cikeystonecorrectionhorizontal)

#### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectionhorizontal/focallength)
- [CIKeystoneCorrectionVertical](/documentation/coreimage/cikeystonecorrectionvertical)

#### Instance Properties

- [var focalLength: Float](/documentation/coreimage/cikeystonecorrectionvertical/focallength)
- [CILanczosScaleTransform](/documentation/coreimage/cilanczosscaletransform)

#### Instance Properties

- [var aspectRatio: Float](/documentation/coreimage/cilanczosscaletransform/aspectratio)
- [var inputImage: CIImage?](/documentation/coreimage/cilanczosscaletransform/inputimage)
- [var scale: Float](/documentation/coreimage/cilanczosscaletransform/scale)
- [CIPerspectiveCorrection](/documentation/coreimage/ciperspectivecorrection)

#### Instance Properties

- [var crop: Bool](/documentation/coreimage/ciperspectivecorrection/crop)
- [CIPerspectiveRotate](/documentation/coreimage/ciperspectiverotate)

#### Instance Properties

- [var focalLength: Float](/documentation/coreimage/ciperspectiverotate/focallength)
- [var inputImage: CIImage?](/documentation/coreimage/ciperspectiverotate/inputimage)
- [var pitch: Float](/documentation/coreimage/ciperspectiverotate/pitch)
- [var roll: Float](/documentation/coreimage/ciperspectiverotate/roll)
- [var yaw: Float](/documentation/coreimage/ciperspectiverotate/yaw)
- [CIPerspectiveTransform](/documentation/coreimage/ciperspectivetransform)
- [CIPerspectiveTransformWithExtent](/documentation/coreimage/ciperspectivetransformwithextent)

#### Instance Properties

- [var extent: CGRect](/documentation/coreimage/ciperspectivetransformwithextent/extent)
- [CIStraighten](/documentation/coreimage/cistraighten)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cistraighten/angle)
- [var inputImage: CIImage?](/documentation/coreimage/cistraighten/inputimage)
- [Gradient Filters](/documentation/coreimage/gradient-filters)

### Filters

- [class func gaussianGradient() -> any CIFilter & CIGaussianGradient](/documentation/coreimage/cifilter-swift.class/gaussiangradient())
- [class func hueSaturationValueGradient() -> any CIFilter & CIHueSaturationValueGradient](/documentation/coreimage/cifilter-swift.class/huesaturationvaluegradient())
- [class func linearGradient() -> any CIFilter & CILinearGradient](/documentation/coreimage/cifilter-swift.class/lineargradient())
- [class func radialGradient() -> any CIFilter & CIRadialGradient](/documentation/coreimage/cifilter-swift.class/radialgradient())
- [class func smoothLinearGradient() -> any CIFilter & CISmoothLinearGradient](/documentation/coreimage/cifilter-swift.class/smoothlineargradient())

### Protocols

- [CIGaussianGradient](/documentation/coreimage/cigaussiangradient)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cigaussiangradient/center)
- [var color0: CIColor](/documentation/coreimage/cigaussiangradient/color0)
- [var color1: CIColor](/documentation/coreimage/cigaussiangradient/color1)
- [var radius: Float](/documentation/coreimage/cigaussiangradient/radius)
- [CIHueSaturationValueGradient](/documentation/coreimage/cihuesaturationvaluegradient)

#### Instance Properties

- [var colorSpace: CGColorSpace?](/documentation/coreimage/cihuesaturationvaluegradient/colorspace)
- [var dither: Float](/documentation/coreimage/cihuesaturationvaluegradient/dither)
- [var radius: Float](/documentation/coreimage/cihuesaturationvaluegradient/radius)
- [var softness: Float](/documentation/coreimage/cihuesaturationvaluegradient/softness)
- [var value: Float](/documentation/coreimage/cihuesaturationvaluegradient/value)
- [CILinearGradient](/documentation/coreimage/cilineargradient)

#### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cilineargradient/color0)
- [var color1: CIColor](/documentation/coreimage/cilineargradient/color1)
- [var point0: CGPoint](/documentation/coreimage/cilineargradient/point0)
- [var point1: CGPoint](/documentation/coreimage/cilineargradient/point1)
- [CIRadialGradient](/documentation/coreimage/ciradialgradient)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciradialgradient/center)
- [var color0: CIColor](/documentation/coreimage/ciradialgradient/color0)
- [var color1: CIColor](/documentation/coreimage/ciradialgradient/color1)
- [var radius0: Float](/documentation/coreimage/ciradialgradient/radius0)
- [var radius1: Float](/documentation/coreimage/ciradialgradient/radius1)
- [CISmoothLinearGradient](/documentation/coreimage/cismoothlineargradient)

#### Instance Properties

- [var color0: CIColor](/documentation/coreimage/cismoothlineargradient/color0)
- [var color1: CIColor](/documentation/coreimage/cismoothlineargradient/color1)
- [var point0: CGPoint](/documentation/coreimage/cismoothlineargradient/point0)
- [var point1: CGPoint](/documentation/coreimage/cismoothlineargradient/point1)
- [Halftone Effect Filters](/documentation/coreimage/halftone-effect-filters)

### Filters

- [class func circularScreen() -> any CIFilter & CICircularScreen](/documentation/coreimage/cifilter-swift.class/circularscreen())
- [class func cmykHalftone() -> any CIFilter & CICMYKHalftone](/documentation/coreimage/cifilter-swift.class/cmykhalftone())
- [class func dotScreen() -> any CIFilter & CIDotScreen](/documentation/coreimage/cifilter-swift.class/dotscreen())
- [class func hatchedScreen() -> any CIFilter & CIHatchedScreen](/documentation/coreimage/cifilter-swift.class/hatchedscreen())
- [class func lineScreen() -> any CIFilter & CILineScreen](/documentation/coreimage/cifilter-swift.class/linescreen())

### Protocols

- [CICircularScreen](/documentation/coreimage/cicircularscreen)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicircularscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicircularscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cicircularscreen/sharpness)
- [var width: Float](/documentation/coreimage/cicircularscreen/width)
- [CICMYKHalftone](/documentation/coreimage/cicmykhalftone)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cicmykhalftone/angle)
- [var center: CGPoint](/documentation/coreimage/cicmykhalftone/center)
- [var grayComponentReplacement: Float](/documentation/coreimage/cicmykhalftone/graycomponentreplacement)
- [var inputImage: CIImage?](/documentation/coreimage/cicmykhalftone/inputimage)
- [var sharpness: Float](/documentation/coreimage/cicmykhalftone/sharpness)
- [var underColorRemoval: Float](/documentation/coreimage/cicmykhalftone/undercolorremoval)
- [var width: Float](/documentation/coreimage/cicmykhalftone/width)
- [CIDotScreen](/documentation/coreimage/cidotscreen)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cidotscreen/angle)
- [var center: CGPoint](/documentation/coreimage/cidotscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cidotscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cidotscreen/sharpness)
- [var width: Float](/documentation/coreimage/cidotscreen/width)
- [CIHatchedScreen](/documentation/coreimage/cihatchedscreen)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cihatchedscreen/angle)
- [var center: CGPoint](/documentation/coreimage/cihatchedscreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cihatchedscreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cihatchedscreen/sharpness)
- [var width: Float](/documentation/coreimage/cihatchedscreen/width)
- [CILineScreen](/documentation/coreimage/cilinescreen)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cilinescreen/angle)
- [var center: CGPoint](/documentation/coreimage/cilinescreen/center)
- [var inputImage: CIImage?](/documentation/coreimage/cilinescreen/inputimage)
- [var sharpness: Float](/documentation/coreimage/cilinescreen/sharpness)
- [var width: Float](/documentation/coreimage/cilinescreen/width)
- [Reduction Filters](/documentation/coreimage/reduction-filters)

### Filters

- [class func areaAverage() -> any CIFilter & CIAreaAverage](/documentation/coreimage/cifilter-swift.class/areaaverage())
- [class func areaHistogram() -> any CIFilter & CIAreaHistogram](/documentation/coreimage/cifilter-swift.class/areahistogram())
- [class func areaLogarithmicHistogram() -> any CIFilter & CIAreaLogarithmicHistogram](/documentation/coreimage/cifilter-swift.class/arealogarithmichistogram())
- [class func areaMaximum() -> any CIFilter & CIAreaMaximum](/documentation/coreimage/cifilter-swift.class/areamaximum())
- [class func areaMaximumAlpha() -> any CIFilter & CIAreaMaximumAlpha](/documentation/coreimage/cifilter-swift.class/areamaximumalpha())
- [class func areaMinimum() -> any CIFilter & CIAreaMinimum](/documentation/coreimage/cifilter-swift.class/areaminimum())
- [class func areaMinimumAlpha() -> any CIFilter & CIAreaMinimumAlpha](/documentation/coreimage/cifilter-swift.class/areaminimumalpha())
- [class func areaMinMax() -> any CIFilter & CIAreaMinMax](/documentation/coreimage/cifilter-swift.class/areaminmax())
- [class func areaMinMaxRed() -> any CIFilter & CIAreaMinMaxRed](/documentation/coreimage/cifilter-swift.class/areaminmaxred())
- [class func columnAverage() -> any CIFilter & CIColumnAverage](/documentation/coreimage/cifilter-swift.class/columnaverage())
- [class func histogramDisplay() -> any CIFilter & CIHistogramDisplay](/documentation/coreimage/cifilter-swift.class/histogramdisplay())
- [class func kMeans() -> any CIFilter & CIKMeans](/documentation/coreimage/cifilter-swift.class/kmeans())
- [class func rowAverage() -> any CIFilter & CIRowAverage](/documentation/coreimage/cifilter-swift.class/rowaverage())

### Protocols

- [CIAreaAverage](/documentation/coreimage/ciareaaverage)
- [CIAreaHistogram](/documentation/coreimage/ciareahistogram)

#### Instance Properties

- [var count: Int](/documentation/coreimage/ciareahistogram/count)
- [var scale: Float](/documentation/coreimage/ciareahistogram/scale)
- [CIAreaLogarithmicHistogram](/documentation/coreimage/ciarealogarithmichistogram)

#### Instance Properties

- [var count: Int](/documentation/coreimage/ciarealogarithmichistogram/count)
- [var maximumStop: Float](/documentation/coreimage/ciarealogarithmichistogram/maximumstop)
- [var minimumStop: Float](/documentation/coreimage/ciarealogarithmichistogram/minimumstop)
- [var scale: Float](/documentation/coreimage/ciarealogarithmichistogram/scale)
- [CIAreaMaximum](/documentation/coreimage/ciareamaximum)
- [CIAreaMaximumAlpha](/documentation/coreimage/ciareamaximumalpha)
- [CIAreaMinMax](/documentation/coreimage/ciareaminmax)
- [CIAreaMinMaxRed](/documentation/coreimage/ciareaminmaxred)
- [CIAreaMinimum](/documentation/coreimage/ciareaminimum)
- [CIAreaMinimumAlpha](/documentation/coreimage/ciareaminimumalpha)
- [CIAreaReductionFilter](/documentation/coreimage/ciareareductionfilter)

#### Instance Properties

- [var extent: CGRect](/documentation/coreimage/ciareareductionfilter/extent)
- [var inputImage: CIImage?](/documentation/coreimage/ciareareductionfilter/inputimage)
- [CIColumnAverage](/documentation/coreimage/cicolumnaverage)
- [CIHistogramDisplay](/documentation/coreimage/cihistogramdisplay)

#### Instance Properties

- [var height: Float](/documentation/coreimage/cihistogramdisplay/height)
- [var highLimit: Float](/documentation/coreimage/cihistogramdisplay/highlimit)
- [var inputImage: CIImage?](/documentation/coreimage/cihistogramdisplay/inputimage)
- [var lowLimit: Float](/documentation/coreimage/cihistogramdisplay/lowlimit)
- [CIKMeans](/documentation/coreimage/cikmeans)

#### Instance Properties

- [var count: Int](/documentation/coreimage/cikmeans/count)
- [var inputMeans: CIImage?](/documentation/coreimage/cikmeans/inputmeans)
- [var passes: Float](/documentation/coreimage/cikmeans/passes)
- [var perceptual: Bool](/documentation/coreimage/cikmeans/perceptual)
- [CIRowAverage](/documentation/coreimage/cirowaverage)
- [Sharpening Filters](/documentation/coreimage/sharpening-filters)

### Filters

- [class func sharpenLuminance() -> any CIFilter & CISharpenLuminance](/documentation/coreimage/cifilter-swift.class/sharpenluminance())
- [class func unsharpMask() -> any CIFilter & CIUnsharpMask](/documentation/coreimage/cifilter-swift.class/unsharpmask())

### Protocols

- [CISharpenLuminance](/documentation/coreimage/cisharpenluminance)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisharpenluminance/inputimage)
- [var radius: Float](/documentation/coreimage/cisharpenluminance/radius)
- [var sharpness: Float](/documentation/coreimage/cisharpenluminance/sharpness)
- [CIUnsharpMask](/documentation/coreimage/ciunsharpmask)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciunsharpmask/inputimage)
- [var intensity: Float](/documentation/coreimage/ciunsharpmask/intensity)
- [var radius: Float](/documentation/coreimage/ciunsharpmask/radius)
- [Stylizing Filters](/documentation/coreimage/stylizing-filters)

### Filters

- [class func blendWithAlphaMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithalphamask())
- [class func blendWithBlueMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithbluemask())
- [class func blendWithMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithmask())
- [class func blendWithRedMask() -> any CIFilter & CIBlendWithMask](/documentation/coreimage/cifilter-swift.class/blendwithredmask())
- [class func bloom() -> any CIFilter & CIBloom](/documentation/coreimage/cifilter-swift.class/bloom())
- [class func cannyEdgeDetector() -> any CIFilter & CICannyEdgeDetector](/documentation/coreimage/cifilter-swift.class/cannyedgedetector())
- [class func comicEffect() -> any CIFilter & CIComicEffect](/documentation/coreimage/cifilter-swift.class/comiceffect())
- [class func coreMLModel() -> any CIFilter & CICoreMLModel](/documentation/coreimage/cifilter-swift.class/coremlmodel())
- [class func crystallize() -> any CIFilter & CICrystallize](/documentation/coreimage/cifilter-swift.class/crystallize())
- [class func depthOfField() -> any CIFilter & CIDepthOfField](/documentation/coreimage/cifilter-swift.class/depthoffield())
- [class func edges() -> any CIFilter & CIEdges](/documentation/coreimage/cifilter-swift.class/edges())
- [class func edgeWork() -> any CIFilter & CIEdgeWork](/documentation/coreimage/cifilter-swift.class/edgework())
- [class func gaborGradients() -> any CIFilter & CIGaborGradients](/documentation/coreimage/cifilter-swift.class/gaborgradients())
- [class func gloom() -> any CIFilter & CIGloom](/documentation/coreimage/cifilter-swift.class/gloom())
- [class func heightFieldFromMask() -> any CIFilter & CIHeightFieldFromMask](/documentation/coreimage/cifilter-swift.class/heightfieldfrommask())
- [class func hexagonalPixellate() -> any CIFilter & CIHexagonalPixellate](/documentation/coreimage/cifilter-swift.class/hexagonalpixellate())
- [class func highlightShadowAdjust() -> any CIFilter & CIHighlightShadowAdjust](/documentation/coreimage/cifilter-swift.class/highlightshadowadjust())
- [class func lineOverlay() -> any CIFilter & CILineOverlay](/documentation/coreimage/cifilter-swift.class/lineoverlay())
- [class func mix() -> any CIFilter & CIMix](/documentation/coreimage/cifilter-swift.class/mix())
- [class func personSegmentation() -> any CIFilter & CIPersonSegmentation](/documentation/coreimage/cifilter-swift.class/personsegmentation())
- [class func pixellate() -> any CIFilter & CIPixellate](/documentation/coreimage/cifilter-swift.class/pixellate())
- [class func pointillize() -> any CIFilter & CIPointillize](/documentation/coreimage/cifilter-swift.class/pointillize())
- [class func saliencyMap() -> any CIFilter & CISaliencyMap](/documentation/coreimage/cifilter-swift.class/saliencymap())
- [class func shadedMaterial() -> any CIFilter & CIShadedMaterial](/documentation/coreimage/cifilter-swift.class/shadedmaterial())
- [class func sobelGradients() -> any CIFilter & CISobelGradients](/documentation/coreimage/cifilter-swift.class/sobelgradients())
- [class func spotColor() -> any CIFilter & CISpotColor](/documentation/coreimage/cifilter-swift.class/spotcolor())
- [class func spotLight() -> any CIFilter & CISpotLight](/documentation/coreimage/cifilter-swift.class/spotlight())
- [class func cannyEdgeDetector() -> any CIFilter & CICannyEdgeDetector](/documentation/coreimage/cifilter-swift.class/cannyedgedetector())

### Protocols

- [CIBlendWithMask](/documentation/coreimage/ciblendwithmask)

#### Instance Properties

- [var backgroundImage: CIImage?](/documentation/coreimage/ciblendwithmask/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/ciblendwithmask/inputimage)
- [var maskImage: CIImage?](/documentation/coreimage/ciblendwithmask/maskimage)
- [CIBloom](/documentation/coreimage/cibloom)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cibloom/inputimage)
- [var intensity: Float](/documentation/coreimage/cibloom/intensity)
- [var radius: Float](/documentation/coreimage/cibloom/radius)
- [CICannyEdgeDetector](/documentation/coreimage/cicannyedgedetector)

#### Instance Properties

- [var gaussianSigma: Float](/documentation/coreimage/cicannyedgedetector/gaussiansigma)
- [var hysteresisPasses: Int](/documentation/coreimage/cicannyedgedetector/hysteresispasses)
- [var inputImage: CIImage?](/documentation/coreimage/cicannyedgedetector/inputimage)
- [var perceptual: Bool](/documentation/coreimage/cicannyedgedetector/perceptual)
- [var thresholdHigh: Float](/documentation/coreimage/cicannyedgedetector/thresholdhigh)
- [var thresholdLow: Float](/documentation/coreimage/cicannyedgedetector/thresholdlow)
- [CIComicEffect](/documentation/coreimage/cicomiceffect)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cicomiceffect/inputimage)
- [CICoreMLModel](/documentation/coreimage/cicoremlmodel)

#### Instance Properties

- [var headIndex: Float](/documentation/coreimage/cicoremlmodel/headindex)
- [var inputImage: CIImage?](/documentation/coreimage/cicoremlmodel/inputimage)
- [var model: MLModel](/documentation/coreimage/cicoremlmodel/model)
- [var softmaxNormalization: Bool](/documentation/coreimage/cicoremlmodel/softmaxnormalization)
- [CICrystallize](/documentation/coreimage/cicrystallize)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cicrystallize/center)
- [var inputImage: CIImage?](/documentation/coreimage/cicrystallize/inputimage)
- [var radius: Float](/documentation/coreimage/cicrystallize/radius)
- [CIDepthOfField](/documentation/coreimage/cidepthoffield)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidepthoffield/inputimage)
- [var point0: CGPoint](/documentation/coreimage/cidepthoffield/point0)
- [var point1: CGPoint](/documentation/coreimage/cidepthoffield/point1)
- [var radius: Float](/documentation/coreimage/cidepthoffield/radius)
- [var saturation: Float](/documentation/coreimage/cidepthoffield/saturation)
- [var unsharpMaskIntensity: Float](/documentation/coreimage/cidepthoffield/unsharpmaskintensity)
- [var unsharpMaskRadius: Float](/documentation/coreimage/cidepthoffield/unsharpmaskradius)
- [CIEdgeWork](/documentation/coreimage/ciedgework)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedgework/inputimage)
- [var radius: Float](/documentation/coreimage/ciedgework/radius)
- [CIEdges](/documentation/coreimage/ciedges)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciedges/inputimage)
- [var intensity: Float](/documentation/coreimage/ciedges/intensity)
- [CIGaborGradients](/documentation/coreimage/cigaborgradients)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigaborgradients/inputimage)
- [CIGloom](/documentation/coreimage/cigloom)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cigloom/inputimage)
- [var intensity: Float](/documentation/coreimage/cigloom/intensity)
- [var radius: Float](/documentation/coreimage/cigloom/radius)
- [CIHeightFieldFromMask](/documentation/coreimage/ciheightfieldfrommask)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciheightfieldfrommask/inputimage)
- [var radius: Float](/documentation/coreimage/ciheightfieldfrommask/radius)
- [CIHexagonalPixellate](/documentation/coreimage/cihexagonalpixellate)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cihexagonalpixellate/center)
- [var inputImage: CIImage?](/documentation/coreimage/cihexagonalpixellate/inputimage)
- [var scale: Float](/documentation/coreimage/cihexagonalpixellate/scale)
- [CIHighlightShadowAdjust](/documentation/coreimage/cihighlightshadowadjust)

#### Instance Properties

- [var highlightAmount: Float](/documentation/coreimage/cihighlightshadowadjust/highlightamount)
- [var inputImage: CIImage?](/documentation/coreimage/cihighlightshadowadjust/inputimage)
- [var radius: Float](/documentation/coreimage/cihighlightshadowadjust/radius)
- [var shadowAmount: Float](/documentation/coreimage/cihighlightshadowadjust/shadowamount)
- [CILineOverlay](/documentation/coreimage/cilineoverlay)

#### Instance Properties

- [var nrNoiseLevel: Float](/documentation/coreimage/cilineoverlay/nrnoiselevel)
- [var nrSharpness: Float](/documentation/coreimage/cilineoverlay/nrsharpness)
- [var contrast: Float](/documentation/coreimage/cilineoverlay/contrast)
- [var edgeIntensity: Float](/documentation/coreimage/cilineoverlay/edgeintensity)
- [var inputImage: CIImage?](/documentation/coreimage/cilineoverlay/inputimage)
- [var threshold: Float](/documentation/coreimage/cilineoverlay/threshold)
- [CIMix](/documentation/coreimage/cimix)

#### Instance Properties

- [var amount: Float](/documentation/coreimage/cimix/amount)
- [var backgroundImage: CIImage?](/documentation/coreimage/cimix/backgroundimage)
- [var inputImage: CIImage?](/documentation/coreimage/cimix/inputimage)
- [CIPersonSegmentation](/documentation/coreimage/cipersonsegmentation)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cipersonsegmentation/inputimage)
- [var qualityLevel: Int](/documentation/coreimage/cipersonsegmentation/qualitylevel)
- [CIPixellate](/documentation/coreimage/cipixellate)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipixellate/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipixellate/inputimage)
- [var scale: Float](/documentation/coreimage/cipixellate/scale)
- [CIPointillize](/documentation/coreimage/cipointillize)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cipointillize/center)
- [var inputImage: CIImage?](/documentation/coreimage/cipointillize/inputimage)
- [var radius: Float](/documentation/coreimage/cipointillize/radius)
- [CISaliencyMap](/documentation/coreimage/cisaliencymap)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisaliencymap/inputimage)
- [CIShadedMaterial](/documentation/coreimage/cishadedmaterial)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cishadedmaterial/inputimage)
- [var scale: Float](/documentation/coreimage/cishadedmaterial/scale)
- [var shadingImage: CIImage?](/documentation/coreimage/cishadedmaterial/shadingimage)
- [CISobelGradients](/documentation/coreimage/cisobelgradients)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisobelgradients/inputimage)
- [CISpotColor](/documentation/coreimage/cispotcolor)

#### Instance Properties

- [var centerColor1: CIColor](/documentation/coreimage/cispotcolor/centercolor1)
- [var centerColor2: CIColor](/documentation/coreimage/cispotcolor/centercolor2)
- [var centerColor3: CIColor](/documentation/coreimage/cispotcolor/centercolor3)
- [var closeness1: Float](/documentation/coreimage/cispotcolor/closeness1)
- [var closeness2: Float](/documentation/coreimage/cispotcolor/closeness2)
- [var closeness3: Float](/documentation/coreimage/cispotcolor/closeness3)
- [var contrast1: Float](/documentation/coreimage/cispotcolor/contrast1)
- [var contrast2: Float](/documentation/coreimage/cispotcolor/contrast2)
- [var contrast3: Float](/documentation/coreimage/cispotcolor/contrast3)
- [var inputImage: CIImage?](/documentation/coreimage/cispotcolor/inputimage)
- [var replacementColor1: CIColor](/documentation/coreimage/cispotcolor/replacementcolor1)
- [var replacementColor2: CIColor](/documentation/coreimage/cispotcolor/replacementcolor2)
- [var replacementColor3: CIColor](/documentation/coreimage/cispotcolor/replacementcolor3)
- [CISpotLight](/documentation/coreimage/cispotlight)

#### Instance Properties

- [var brightness: Float](/documentation/coreimage/cispotlight/brightness)
- [var color: CIColor](/documentation/coreimage/cispotlight/color)
- [var concentration: Float](/documentation/coreimage/cispotlight/concentration)
- [var inputImage: CIImage?](/documentation/coreimage/cispotlight/inputimage)
- [var lightPointsAt: CIVector](/documentation/coreimage/cispotlight/lightpointsat)
- [var lightPosition: CIVector](/documentation/coreimage/cispotlight/lightposition)
- [Tile Effect Filters](/documentation/coreimage/tile-effect-filters)

### Filters

- [class func affineClamp() -> any CIFilter & CIAffineClamp](/documentation/coreimage/cifilter-swift.class/affineclamp())
- [class func affineTile() -> any CIFilter & CIAffineTile](/documentation/coreimage/cifilter-swift.class/affinetile())
- [class func eightfoldReflectedTile() -> any CIFilter & CIEightfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/eightfoldreflectedtile())
- [class func fourfoldReflectedTile() -> any CIFilter & CIFourfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/fourfoldreflectedtile())
- [class func fourfoldRotatedTile() -> any CIFilter & CIFourfoldRotatedTile](/documentation/coreimage/cifilter-swift.class/fourfoldrotatedtile())
- [class func fourfoldTranslatedTile() -> any CIFilter & CIFourfoldTranslatedTile](/documentation/coreimage/cifilter-swift.class/fourfoldtranslatedtile())
- [class func glideReflectedTile() -> any CIFilter & CIGlideReflectedTile](/documentation/coreimage/cifilter-swift.class/glidereflectedtile())
- [class func kaleidoscope() -> any CIFilter & CIKaleidoscope](/documentation/coreimage/cifilter-swift.class/kaleidoscope())
- [class func opTile() -> any CIFilter & CIOpTile](/documentation/coreimage/cifilter-swift.class/optile())
- [class func parallelogramTile() -> any CIFilter & CIParallelogramTile](/documentation/coreimage/cifilter-swift.class/parallelogramtile())
- [class func perspectiveTile() -> any CIFilter & CIPerspectiveTile](/documentation/coreimage/cifilter-swift.class/perspectivetile())
- [class func sixfoldReflectedTile() -> any CIFilter & CISixfoldReflectedTile](/documentation/coreimage/cifilter-swift.class/sixfoldreflectedtile())
- [class func sixfoldRotatedTile() -> any CIFilter & CISixfoldRotatedTile](/documentation/coreimage/cifilter-swift.class/sixfoldrotatedtile())
- [class func triangleKaleidoscope() -> any CIFilter & CITriangleKaleidoscope](/documentation/coreimage/cifilter-swift.class/trianglekaleidoscope())
- [class func triangleTile() -> any CIFilter & CITriangleTile](/documentation/coreimage/cifilter-swift.class/triangletile())
- [class func twelvefoldReflectedTile() -> any CIFilter & CITwelvefoldReflectedTile](/documentation/coreimage/cifilter-swift.class/twelvefoldreflectedtile())

### Protocols

- [CIAffineClamp](/documentation/coreimage/ciaffineclamp)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciaffineclamp/inputimage)
- [var transform: CGAffineTransform](/documentation/coreimage/ciaffineclamp/transform)
- [CIAffineTile](/documentation/coreimage/ciaffinetile)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/ciaffinetile/inputimage)
- [var transform: CGAffineTransform](/documentation/coreimage/ciaffinetile/transform)
- [CIEightfoldReflectedTile](/documentation/coreimage/cieightfoldreflectedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cieightfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cieightfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cieightfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cieightfoldreflectedtile/width)
- [CIFourfoldReflectedTile](/documentation/coreimage/cifourfoldreflectedtile)

#### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/cifourfoldreflectedtile/acuteangle)
- [var angle: Float](/documentation/coreimage/cifourfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldreflectedtile/width)
- [CIFourfoldRotatedTile](/documentation/coreimage/cifourfoldrotatedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cifourfoldrotatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldrotatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldrotatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldrotatedtile/width)
- [CIFourfoldTranslatedTile](/documentation/coreimage/cifourfoldtranslatedtile)

#### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/cifourfoldtranslatedtile/acuteangle)
- [var angle: Float](/documentation/coreimage/cifourfoldtranslatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cifourfoldtranslatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cifourfoldtranslatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cifourfoldtranslatedtile/width)
- [CIGlideReflectedTile](/documentation/coreimage/ciglidereflectedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/ciglidereflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/ciglidereflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciglidereflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/ciglidereflectedtile/width)
- [CIKaleidoscope](/documentation/coreimage/cikaleidoscope)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cikaleidoscope/angle)
- [var center: CGPoint](/documentation/coreimage/cikaleidoscope/center)
- [var count: Int](/documentation/coreimage/cikaleidoscope/count)
- [var inputImage: CIImage?](/documentation/coreimage/cikaleidoscope/inputimage)
- [CIOpTile](/documentation/coreimage/cioptile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cioptile/angle)
- [var center: CGPoint](/documentation/coreimage/cioptile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cioptile/inputimage)
- [var scale: Float](/documentation/coreimage/cioptile/scale)
- [var width: Float](/documentation/coreimage/cioptile/width)
- [CIParallelogramTile](/documentation/coreimage/ciparallelogramtile)

#### Instance Properties

- [var acuteAngle: Float](/documentation/coreimage/ciparallelogramtile/acuteangle)
- [var angle: Float](/documentation/coreimage/ciparallelogramtile/angle)
- [var center: CGPoint](/documentation/coreimage/ciparallelogramtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/ciparallelogramtile/inputimage)
- [var width: Float](/documentation/coreimage/ciparallelogramtile/width)
- [CIPerspectiveTile](/documentation/coreimage/ciperspectivetile)

#### Instance Properties

- [var bottomLeft: CGPoint](/documentation/coreimage/ciperspectivetile/bottomleft)
- [var bottomRight: CGPoint](/documentation/coreimage/ciperspectivetile/bottomright)
- [var inputImage: CIImage?](/documentation/coreimage/ciperspectivetile/inputimage)
- [var topLeft: CGPoint](/documentation/coreimage/ciperspectivetile/topleft)
- [var topRight: CGPoint](/documentation/coreimage/ciperspectivetile/topright)
- [CISixfoldReflectedTile](/documentation/coreimage/cisixfoldreflectedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cisixfoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cisixfoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cisixfoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/cisixfoldreflectedtile/width)
- [CISixfoldRotatedTile](/documentation/coreimage/cisixfoldrotatedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cisixfoldrotatedtile/angle)
- [var center: CGPoint](/documentation/coreimage/cisixfoldrotatedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/cisixfoldrotatedtile/inputimage)
- [var width: Float](/documentation/coreimage/cisixfoldrotatedtile/width)
- [CITriangleKaleidoscope](/documentation/coreimage/citrianglekaleidoscope)

#### Instance Properties

- [var decay: Float](/documentation/coreimage/citrianglekaleidoscope/decay)
- [var inputImage: CIImage?](/documentation/coreimage/citrianglekaleidoscope/inputimage)
- [var point: CGPoint](/documentation/coreimage/citrianglekaleidoscope/point)
- [var rotation: Float](/documentation/coreimage/citrianglekaleidoscope/rotation)
- [var size: Float](/documentation/coreimage/citrianglekaleidoscope/size)
- [CITriangleTile](/documentation/coreimage/citriangletile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/citriangletile/angle)
- [var center: CGPoint](/documentation/coreimage/citriangletile/center)
- [var inputImage: CIImage?](/documentation/coreimage/citriangletile/inputimage)
- [var width: Float](/documentation/coreimage/citriangletile/width)
- [CITwelvefoldReflectedTile](/documentation/coreimage/citwelvefoldreflectedtile)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/citwelvefoldreflectedtile/angle)
- [var center: CGPoint](/documentation/coreimage/citwelvefoldreflectedtile/center)
- [var inputImage: CIImage?](/documentation/coreimage/citwelvefoldreflectedtile/inputimage)
- [var width: Float](/documentation/coreimage/citwelvefoldreflectedtile/width)
- [Transition Filters](/documentation/coreimage/transition-filters)

### Filters

- [class func accordionFoldTransition() -> any CIFilter & CIAccordionFoldTransition](/documentation/coreimage/cifilter-swift.class/accordionfoldtransition())
- [class func barsSwipeTransition() -> any CIFilter & CIBarsSwipeTransition](/documentation/coreimage/cifilter-swift.class/barsswipetransition())
- [class func copyMachineTransition() -> any CIFilter & CICopyMachineTransition](/documentation/coreimage/cifilter-swift.class/copymachinetransition())
- [class func disintegrateWithMaskTransition() -> any CIFilter & CIDisintegrateWithMaskTransition](/documentation/coreimage/cifilter-swift.class/disintegratewithmasktransition())
- [class func dissolveTransition() -> any CIFilter & CIDissolveTransition](/documentation/coreimage/cifilter-swift.class/dissolvetransition())
- [class func flashTransition() -> any CIFilter & CIFlashTransition](/documentation/coreimage/cifilter-swift.class/flashtransition())
- [class func modTransition() -> any CIFilter & CIModTransition](/documentation/coreimage/cifilter-swift.class/modtransition())
- [class func pageCurlTransition() -> any CIFilter & CIPageCurlTransition](/documentation/coreimage/cifilter-swift.class/pagecurltransition())
- [class func pageCurlWithShadowTransition() -> any CIFilter & CIPageCurlWithShadowTransition](/documentation/coreimage/cifilter-swift.class/pagecurlwithshadowtransition())
- [class func rippleTransition() -> any CIFilter & CIRippleTransition](/documentation/coreimage/cifilter-swift.class/rippletransition())
- [class func swipeTransition() -> any CIFilter & CISwipeTransition](/documentation/coreimage/cifilter-swift.class/swipetransition())

### Protocols

- [CITransitionFilter](/documentation/coreimage/citransitionfilter)

#### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citransitionfilter/inputimage)
- [var targetImage: CIImage?](/documentation/coreimage/citransitionfilter/targetimage)
- [var time: Float](/documentation/coreimage/citransitionfilter/time)
- [CIBarsSwipeTransition](/documentation/coreimage/cibarsswipetransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cibarsswipetransition/angle)
- [var barOffset: Float](/documentation/coreimage/cibarsswipetransition/baroffset)
- [var width: Float](/documentation/coreimage/cibarsswipetransition/width)
- [CIAccordionFoldTransition](/documentation/coreimage/ciaccordionfoldtransition)

#### Instance Properties

- [var bottomHeight: Float](/documentation/coreimage/ciaccordionfoldtransition/bottomheight)
- [var foldShadowAmount: Float](/documentation/coreimage/ciaccordionfoldtransition/foldshadowamount)
- [var numberOfFolds: Float](/documentation/coreimage/ciaccordionfoldtransition/numberoffolds)
- [CICopyMachineTransition](/documentation/coreimage/cicopymachinetransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cicopymachinetransition/angle)
- [var color: CIColor](/documentation/coreimage/cicopymachinetransition/color)
- [var extent: CGRect](/documentation/coreimage/cicopymachinetransition/extent)
- [var opacity: Float](/documentation/coreimage/cicopymachinetransition/opacity)
- [var width: Float](/documentation/coreimage/cicopymachinetransition/width)
- [CIDisintegrateWithMaskTransition](/documentation/coreimage/cidisintegratewithmasktransition)

#### Instance Properties

- [var maskImage: CIImage?](/documentation/coreimage/cidisintegratewithmasktransition/maskimage)
- [var shadowDensity: Float](/documentation/coreimage/cidisintegratewithmasktransition/shadowdensity)
- [var shadowOffset: CGPoint](/documentation/coreimage/cidisintegratewithmasktransition/shadowoffset)
- [var shadowRadius: Float](/documentation/coreimage/cidisintegratewithmasktransition/shadowradius)
- [CIDissolveTransition](/documentation/coreimage/cidissolvetransition)
- [CIFlashTransition](/documentation/coreimage/ciflashtransition)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/ciflashtransition/center)
- [var color: CIColor](/documentation/coreimage/ciflashtransition/color)
- [var extent: CGRect](/documentation/coreimage/ciflashtransition/extent)
- [var fadeThreshold: Float](/documentation/coreimage/ciflashtransition/fadethreshold)
- [var maxStriationRadius: Float](/documentation/coreimage/ciflashtransition/maxstriationradius)
- [var striationContrast: Float](/documentation/coreimage/ciflashtransition/striationcontrast)
- [var striationStrength: Float](/documentation/coreimage/ciflashtransition/striationstrength)
- [CIModTransition](/documentation/coreimage/cimodtransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cimodtransition/angle)
- [var center: CGPoint](/documentation/coreimage/cimodtransition/center)
- [var compression: Float](/documentation/coreimage/cimodtransition/compression)
- [var radius: Float](/documentation/coreimage/cimodtransition/radius)
- [CIPageCurlTransition](/documentation/coreimage/cipagecurltransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cipagecurltransition/angle)
- [var backsideImage: CIImage?](/documentation/coreimage/cipagecurltransition/backsideimage)
- [var extent: CGRect](/documentation/coreimage/cipagecurltransition/extent)
- [var radius: Float](/documentation/coreimage/cipagecurltransition/radius)
- [var shadingImage: CIImage?](/documentation/coreimage/cipagecurltransition/shadingimage)
- [CIPageCurlWithShadowTransition](/documentation/coreimage/cipagecurlwithshadowtransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/cipagecurlwithshadowtransition/angle)
- [var backsideImage: CIImage?](/documentation/coreimage/cipagecurlwithshadowtransition/backsideimage)
- [var extent: CGRect](/documentation/coreimage/cipagecurlwithshadowtransition/extent)
- [var radius: Float](/documentation/coreimage/cipagecurlwithshadowtransition/radius)
- [var shadowAmount: Float](/documentation/coreimage/cipagecurlwithshadowtransition/shadowamount)
- [var shadowExtent: CGRect](/documentation/coreimage/cipagecurlwithshadowtransition/shadowextent)
- [var shadowSize: Float](/documentation/coreimage/cipagecurlwithshadowtransition/shadowsize)
- [CIRippleTransition](/documentation/coreimage/cirippletransition)

#### Instance Properties

- [var center: CGPoint](/documentation/coreimage/cirippletransition/center)
- [var extent: CGRect](/documentation/coreimage/cirippletransition/extent)
- [var scale: Float](/documentation/coreimage/cirippletransition/scale)
- [var shadingImage: CIImage?](/documentation/coreimage/cirippletransition/shadingimage)
- [var width: Float](/documentation/coreimage/cirippletransition/width)
- [CISwipeTransition](/documentation/coreimage/ciswipetransition)

#### Instance Properties

- [var angle: Float](/documentation/coreimage/ciswipetransition/angle)
- [var color: CIColor](/documentation/coreimage/ciswipetransition/color)
- [var extent: CGRect](/documentation/coreimage/ciswipetransition/extent)
- [var opacity: Float](/documentation/coreimage/ciswipetransition/opacity)
- [var width: Float](/documentation/coreimage/ciswipetransition/width)

## Filter Recipes

- [Applying a Chroma Key Effect](/documentation/coreimage/applying-a-chroma-key-effect)
- [Selectively Focusing on an Image](/documentation/coreimage/selectively-focusing-on-an-image)
- [Customizing Image Transitions](/documentation/coreimage/customizing-image-transitions)
- [Simulating Scratchy Analog Film](/documentation/coreimage/simulating-scratchy-analog-film)

## Custom Filters

- [Writing Custom Kernels](/documentation/coreimage/writing-custom-kernels)
- [CIKernel](/documentation/coreimage/cikernel)

### Creating a Kernel Using Metal Shading Language

- [convenience init(functionName: String, fromMetalLibraryData: Data) throws](/documentation/coreimage/cikernel/init(functionname:frommetallibrarydata:))
- [convenience init(functionName: String, fromMetalLibraryData: Data, outputPixelFormat: CIFormat) throws](/documentation/coreimage/cikernel/init(functionname:frommetallibrarydata:outputpixelformat:))
- [class func kernelNames(fromMetalLibraryData: Data) -> [String]](/documentation/coreimage/cikernel/kernelnames(frommetallibrarydata:))
- [class func kernels(withMetalString: String) throws -> [CIKernel]](/documentation/coreimage/cikernel/kernels(withmetalstring:))

### Getting a Kernel Name

- [var name: String](/documentation/coreimage/cikernel/name)

### Identifying the Region of Interest for the Kernel

- [func setROISelector(Selector)](/documentation/coreimage/cikernel/setroiselector(_:))

### Applying a Kernel to Filter an Image

- [func apply(extent: CGRect, roiCallback: CIKernelROICallback, arguments: [Any]) -> CIImage?](/documentation/coreimage/cikernel/apply(extent:roicallback:arguments:))
- [CIKernelROICallback](/documentation/coreimage/cikernelroicallback)

### Deprecated

- [convenience init?(source: String)](/documentation/coreimage/cikernel/init(source:))
- [class func makeKernels(source: String) -> [CIKernel]?](/documentation/coreimage/cikernel/makekernels(source:))
- [CIColorKernel](/documentation/coreimage/cicolorkernel)

### Creating a Kernel

- [convenience init?(source: String)](/documentation/coreimage/cicolorkernel/init(source:))

### Applying a Kernel to Filter an Image

- [func apply(extent: CGRect, arguments: [Any]) -> CIImage?](/documentation/coreimage/cicolorkernel/apply(extent:arguments:))
- [CIWarpKernel](/documentation/coreimage/ciwarpkernel)

### Creating a Kernel

- [convenience init?(source: String)](/documentation/coreimage/ciwarpkernel/init(source:))

### Applying a Kernel to Filter an Image

- [func apply(extent: CGRect, roiCallback: CIKernelROICallback, image: CIImage, arguments: [Any]) -> CIImage?](/documentation/coreimage/ciwarpkernel/apply(extent:roicallback:image:arguments:))
- [CIBlendKernel](/documentation/coreimage/ciblendkernel)

### Creating a Kernel

- [convenience init?(source: String)](/documentation/coreimage/ciblendkernel/init(source:))

### Applying a Kernel to Filter an Image

- [func apply(foreground: CIImage, background: CIImage) -> CIImage?](/documentation/coreimage/ciblendkernel/apply(foreground:background:))

### Builtin Blend Kernels

- [class var clear: CIBlendKernel](/documentation/coreimage/ciblendkernel/clear)
- [class var color: CIBlendKernel](/documentation/coreimage/ciblendkernel/color)
- [class var colorBurn: CIBlendKernel](/documentation/coreimage/ciblendkernel/colorburn)
- [class var colorDodge: CIBlendKernel](/documentation/coreimage/ciblendkernel/colordodge)
- [class var componentAdd: CIBlendKernel](/documentation/coreimage/ciblendkernel/componentadd)
- [class var componentMax: CIBlendKernel](/documentation/coreimage/ciblendkernel/componentmax)
- [class var componentMin: CIBlendKernel](/documentation/coreimage/ciblendkernel/componentmin)
- [class var componentMultiply: CIBlendKernel](/documentation/coreimage/ciblendkernel/componentmultiply)
- [class var darken: CIBlendKernel](/documentation/coreimage/ciblendkernel/darken)
- [class var darkerColor: CIBlendKernel](/documentation/coreimage/ciblendkernel/darkercolor)
- [class var destination: CIBlendKernel](/documentation/coreimage/ciblendkernel/destination)
- [class var destinationAtop: CIBlendKernel](/documentation/coreimage/ciblendkernel/destinationatop)
- [class var destinationIn: CIBlendKernel](/documentation/coreimage/ciblendkernel/destinationin)
- [class var destinationOut: CIBlendKernel](/documentation/coreimage/ciblendkernel/destinationout)
- [class var destinationOver: CIBlendKernel](/documentation/coreimage/ciblendkernel/destinationover)
- [class var difference: CIBlendKernel](/documentation/coreimage/ciblendkernel/difference)
- [class var divide: CIBlendKernel](/documentation/coreimage/ciblendkernel/divide)
- [class var exclusion: CIBlendKernel](/documentation/coreimage/ciblendkernel/exclusion)
- [class var exclusiveOr: CIBlendKernel](/documentation/coreimage/ciblendkernel/exclusiveor)
- [class var hardLight: CIBlendKernel](/documentation/coreimage/ciblendkernel/hardlight)
- [class var hardMix: CIBlendKernel](/documentation/coreimage/ciblendkernel/hardmix)
- [class var hue: CIBlendKernel](/documentation/coreimage/ciblendkernel/hue)
- [class var lighten: CIBlendKernel](/documentation/coreimage/ciblendkernel/lighten)
- [class var lighterColor: CIBlendKernel](/documentation/coreimage/ciblendkernel/lightercolor)
- [class var linearBurn: CIBlendKernel](/documentation/coreimage/ciblendkernel/linearburn)
- [class var linearDodge: CIBlendKernel](/documentation/coreimage/ciblendkernel/lineardodge)
- [class var linearLight: CIBlendKernel](/documentation/coreimage/ciblendkernel/linearlight)
- [class var luminosity: CIBlendKernel](/documentation/coreimage/ciblendkernel/luminosity)
- [class var multiply: CIBlendKernel](/documentation/coreimage/ciblendkernel/multiply)
- [class var overlay: CIBlendKernel](/documentation/coreimage/ciblendkernel/overlay)
- [class var pinLight: CIBlendKernel](/documentation/coreimage/ciblendkernel/pinlight)
- [class var saturation: CIBlendKernel](/documentation/coreimage/ciblendkernel/saturation)
- [class var screen: CIBlendKernel](/documentation/coreimage/ciblendkernel/screen)
- [class var softLight: CIBlendKernel](/documentation/coreimage/ciblendkernel/softlight)
- [class var source: CIBlendKernel](/documentation/coreimage/ciblendkernel/source)
- [class var sourceAtop: CIBlendKernel](/documentation/coreimage/ciblendkernel/sourceatop)
- [class var sourceIn: CIBlendKernel](/documentation/coreimage/ciblendkernel/sourcein)
- [class var sourceOut: CIBlendKernel](/documentation/coreimage/ciblendkernel/sourceout)
- [class var sourceOver: CIBlendKernel](/documentation/coreimage/ciblendkernel/sourceover)
- [class var subtract: CIBlendKernel](/documentation/coreimage/ciblendkernel/subtract)
- [class var vividLight: CIBlendKernel](/documentation/coreimage/ciblendkernel/vividlight)

### Instance Methods

- [func apply(foreground: CIImage, background: CIImage, colorSpace: CGColorSpace) -> CIImage?](/documentation/coreimage/ciblendkernel/apply(foreground:background:colorspace:))
- [CISampler](/documentation/coreimage/cisampler)

### Initializing a Sampler

- [convenience init(image: CIImage)](/documentation/coreimage/cisampler/init(image:))
- [init(image: CIImage, options: [AnyHashable : Any]?)](/documentation/coreimage/cisampler/init(image:options:))

### Getting Information About the Sampler Object

- [var definition: CIFilterShape](/documentation/coreimage/cisampler/definition)
- [var extent: CGRect](/documentation/coreimage/cisampler/extent)

### Constants

- [Sampler Option Keys](/documentation/coreimage/sampler-option-keys)

#### Constants

- [let kCISamplerAffineMatrix: String](/documentation/coreimage/kcisampleraffinematrix)
- [let kCISamplerWrapMode: String](/documentation/coreimage/kcisamplerwrapmode)
- [let kCISamplerFilterMode: String](/documentation/coreimage/kcisamplerfiltermode)
- [let kCISamplerColorSpace: String](/documentation/coreimage/kcisamplercolorspace)
- [Sampler Option Values](/documentation/coreimage/sampler-option-values)

#### Constants

- [let kCISamplerWrapBlack: String](/documentation/coreimage/kcisamplerwrapblack)
- [let kCISamplerWrapClamp: String](/documentation/coreimage/kcisamplerwrapclamp)
- [let kCISamplerFilterNearest: String](/documentation/coreimage/kcisamplerfilternearest)
- [let kCISamplerFilterLinear: String](/documentation/coreimage/kcisamplerfilterlinear)
- [CIFilterShape](/documentation/coreimage/cifiltershape)

### Initializing a Filter Shape

- [init(rect: CGRect)](/documentation/coreimage/cifiltershape/init(rect:))

### Inspecting a Filter Shape

- [var extent: CGRect](/documentation/coreimage/cifiltershape/extent)

### Modifying a Filter Shape

- [func insetBy(x: Int32, y: Int32) -> CIFilterShape](/documentation/coreimage/cifiltershape/insetby(x:y:))
- [func intersect(with: CIFilterShape) -> CIFilterShape](/documentation/coreimage/cifiltershape/intersect(with:)-8iw)
- [func intersect(with: CGRect) -> CIFilterShape](/documentation/coreimage/cifiltershape/intersect(with:)-2o2n8)
- [func transform(by: CGAffineTransform, interior: Bool) -> CIFilterShape](/documentation/coreimage/cifiltershape/transform(by:interior:))
- [func union(with: CIFilterShape) -> CIFilterShape](/documentation/coreimage/cifiltershape/union(with:)-52mnd)
- [func union(with: CGRect) -> CIFilterShape](/documentation/coreimage/cifiltershape/union(with:)-75ebo)
- [CIFormat](/documentation/coreimage/ciformat)

### Image Formats

- [static let A16: CIFormat](/documentation/coreimage/ciformat/a16)
- [static let A8: CIFormat](/documentation/coreimage/ciformat/a8)
- [static let ABGR8: CIFormat](/documentation/coreimage/ciformat/abgr8)
- [static let ARGB8: CIFormat](/documentation/coreimage/ciformat/argb8)
- [static let Af: CIFormat](/documentation/coreimage/ciformat/af)
- [static let Ah: CIFormat](/documentation/coreimage/ciformat/ah)
- [static let BGRA8: CIFormat](/documentation/coreimage/ciformat/bgra8)
- [static let R16: CIFormat](/documentation/coreimage/ciformat/r16)
- [static let R8: CIFormat](/documentation/coreimage/ciformat/r8)
- [static let RG16: CIFormat](/documentation/coreimage/ciformat/rg16)
- [static let RG8: CIFormat](/documentation/coreimage/ciformat/rg8)
- [static let RGB10: CIFormat](/documentation/coreimage/ciformat/rgb10)
- [static let RGBA16: CIFormat](/documentation/coreimage/ciformat/rgba16)
- [static let RGBX16: CIFormat](/documentation/coreimage/ciformat/rgbx16)
- [static let RGBA8: CIFormat](/documentation/coreimage/ciformat/rgba8)
- [static let RGBAf: CIFormat](/documentation/coreimage/ciformat/rgbaf)
- [static let rgbXf: CIFormat](/documentation/coreimage/ciformat/rgbxf)
- [static let RGBAh: CIFormat](/documentation/coreimage/ciformat/rgbah)
- [static let rgbXh: CIFormat](/documentation/coreimage/ciformat/rgbxh)
- [static let RGf: CIFormat](/documentation/coreimage/ciformat/rgf)
- [static let RGh: CIFormat](/documentation/coreimage/ciformat/rgh)
- [static let Rf: CIFormat](/documentation/coreimage/ciformat/rf)
- [static let Rh: CIFormat](/documentation/coreimage/ciformat/rh)
- [static let L16: CIFormat](/documentation/coreimage/ciformat/l16)
- [static let L8: CIFormat](/documentation/coreimage/ciformat/l8)
- [static let LA16: CIFormat](/documentation/coreimage/ciformat/la16)
- [static let LA8: CIFormat](/documentation/coreimage/ciformat/la8)
- [static let LAf: CIFormat](/documentation/coreimage/ciformat/laf)
- [static let LAh: CIFormat](/documentation/coreimage/ciformat/lah)
- [static let Lf: CIFormat](/documentation/coreimage/ciformat/lf)
- [static let Lh: CIFormat](/documentation/coreimage/ciformat/lh)

### Initializers

- [init(rawValue: Int32)](/documentation/coreimage/ciformat/init(rawvalue:))

### Type Properties

- [static let RGBX8: CIFormat](/documentation/coreimage/ciformat/rgbx8)

## Custom Image Processors

- [CIImageProcessorKernel](/documentation/coreimage/ciimageprocessorkernel)

### Type Properties

- [class var outputFormat: CIFormat](/documentation/coreimage/ciimageprocessorkernel/outputformat)
- [class var outputIsOpaque: Bool](/documentation/coreimage/ciimageprocessorkernel/outputisopaque)
- [class var synchronizeInputs: Bool](/documentation/coreimage/ciimageprocessorkernel/synchronizeinputs)

### Type Methods

- [class func apply(withExtent: CGRect, inputs: [CIImage]?, arguments: [String : Any]?) throws -> CIImage](/documentation/coreimage/ciimageprocessorkernel/apply(withextent:inputs:arguments:))
- [class func formatForInput(at: Int32) -> CIFormat](/documentation/coreimage/ciimageprocessorkernel/formatforinput(at:))
- [class func process(with: [any CIImageProcessorInput]?, arguments: [String : Any]?, output: any CIImageProcessorOutput) throws](/documentation/coreimage/ciimageprocessorkernel/process(with:arguments:output:))
- [class func roi(forInput: Int32, arguments: [String : Any]?, outputRect: CGRect) -> CGRect](/documentation/coreimage/ciimageprocessorkernel/roi(forinput:arguments:outputrect:))
- [class func roiTileArray(forInput: Int32, arguments: [String : Any]?, outputRect: CGRect) -> [CIVector]](/documentation/coreimage/ciimageprocessorkernel/roitilearray(forinput:arguments:outputrect:))
- [class func apply(withExtents: [CIVector], inputs: [CIImage]?, arguments: [String : Any]?) throws -> [CIImage]](/documentation/coreimage/ciimageprocessorkernel/apply(withextents:inputs:arguments:))
- [class func outputFormat(at: Int32, arguments: [String : Any]?) -> CIFormat](/documentation/coreimage/ciimageprocessorkernel/outputformat(at:arguments:))
- [class func process(with: [any CIImageProcessorInput]?, arguments: [String : Any]?, outputs: [any CIImageProcessorOutput]) throws](/documentation/coreimage/ciimageprocessorkernel/process(with:arguments:outputs:))
- [CIImageProcessorInput](/documentation/coreimage/ciimageprocessorinput)

### Accessing Input Image Data

- [var baseAddress: UnsafeRawPointer](/documentation/coreimage/ciimageprocessorinput/baseaddress)
- [var metalTexture: (any MTLTexture)?](/documentation/coreimage/ciimageprocessorinput/metaltexture)
- [var pixelBuffer: CVPixelBuffer?](/documentation/coreimage/ciimageprocessorinput/pixelbuffer)
- [var surface: IOSurfaceRef](/documentation/coreimage/ciimageprocessorinput/surface)

### Getting Supplemental Information for Image Processing

- [var region: CGRect](/documentation/coreimage/ciimageprocessorinput/region)
- [var bytesPerRow: Int](/documentation/coreimage/ciimageprocessorinput/bytesperrow)
- [var format: CIFormat](/documentation/coreimage/ciimageprocessorinput/format)

### Instance Properties

- [var digest: UInt64](/documentation/coreimage/ciimageprocessorinput/digest)
- [var roiTileCount: Int](/documentation/coreimage/ciimageprocessorinput/roitilecount)
- [var roiTileIndex: Int](/documentation/coreimage/ciimageprocessorinput/roitileindex)
- [CIImageProcessorOutput](/documentation/coreimage/ciimageprocessoroutput)

### Providing Output Image Data

- [var baseAddress: UnsafeMutableRawPointer](/documentation/coreimage/ciimageprocessoroutput/baseaddress)
- [var metalTexture: (any MTLTexture)?](/documentation/coreimage/ciimageprocessoroutput/metaltexture)
- [var pixelBuffer: CVPixelBuffer?](/documentation/coreimage/ciimageprocessoroutput/pixelbuffer)
- [var surface: IOSurfaceRef](/documentation/coreimage/ciimageprocessoroutput/surface)

### Getting Supplemental Information for Image Processing

- [var region: CGRect](/documentation/coreimage/ciimageprocessoroutput/region)
- [var metalCommandBuffer: (any MTLCommandBuffer)?](/documentation/coreimage/ciimageprocessoroutput/metalcommandbuffer)
- [var bytesPerRow: Int](/documentation/coreimage/ciimageprocessoroutput/bytesperrow)
- [var format: CIFormat](/documentation/coreimage/ciimageprocessoroutput/format)

### Instance Properties

- [var digest: UInt64](/documentation/coreimage/ciimageprocessoroutput/digest)

## Custom Render Destination

- [Generating an animation with a Core Image Render Destination](/documentation/coreimage/generating-an-animation-with-a-core-image-render-destination)
- [CIRenderDestination](/documentation/coreimage/cirenderdestination)

### Creating a Render Destination

- [init(pixelBuffer: CVPixelBuffer)](/documentation/coreimage/cirenderdestination/init(pixelbuffer:))
- [init(ioSurface: IOSurface)](/documentation/coreimage/cirenderdestination/init(iosurface:))
- [init(mtlTexture: any MTLTexture, commandBuffer: (any MTLCommandBuffer)?)](/documentation/coreimage/cirenderdestination/init(mtltexture:commandbuffer:))
- [init(width: Int, height: Int, pixelFormat: MTLPixelFormat, commandBuffer: (any MTLCommandBuffer)?, mtlTextureProvider: (() -> any MTLTexture)?)](/documentation/coreimage/cirenderdestination/init(width:height:pixelformat:commandbuffer:mtltextureprovider:))
- [init(glTexture: UInt32, target: UInt32, width: Int, height: Int)](/documentation/coreimage/cirenderdestination/init(gltexture:target:width:height:))
- [init(bitmapData: UnsafeMutableRawPointer, width: Int, height: Int, bytesPerRow: Int, format: CIFormat)](/documentation/coreimage/cirenderdestination/init(bitmapdata:width:height:bytesperrow:format:))

### Customizing Rendering

- [var alphaMode: CIRenderDestinationAlphaMode](/documentation/coreimage/cirenderdestination/alphamode)
- [CIRenderDestinationAlphaMode](/documentation/coreimage/cirenderdestinationalphamode)

#### Enumeration Cases

- [case none](/documentation/coreimage/cirenderdestinationalphamode/none)
- [case premultiplied](/documentation/coreimage/cirenderdestinationalphamode/premultiplied)
- [case unpremultiplied](/documentation/coreimage/cirenderdestinationalphamode/unpremultiplied)

#### Initializers

- [init?(rawValue: UInt)](/documentation/coreimage/cirenderdestinationalphamode/init(rawvalue:))
- [var blendKernel: CIBlendKernel?](/documentation/coreimage/cirenderdestination/blendkernel)
- [var blendsInDestinationColorSpace: Bool](/documentation/coreimage/cirenderdestination/blendsindestinationcolorspace)
- [var colorSpace: CGColorSpace?](/documentation/coreimage/cirenderdestination/colorspace)
- [var width: Int](/documentation/coreimage/cirenderdestination/width)
- [var height: Int](/documentation/coreimage/cirenderdestination/height)
- [var isClamped: Bool](/documentation/coreimage/cirenderdestination/isclamped)
- [var isDithered: Bool](/documentation/coreimage/cirenderdestination/isdithered)
- [var isFlipped: Bool](/documentation/coreimage/cirenderdestination/isflipped)

### Instance Properties

- [var captureTraceURL: URL?](/documentation/coreimage/cirenderdestination/capturetraceurl)
- [CIRenderInfo](/documentation/coreimage/cirenderinfo)

### Instance Properties

- [var kernelExecutionTime: TimeInterval](/documentation/coreimage/cirenderinfo/kernelexecutiontime)
- [var passCount: Int](/documentation/coreimage/cirenderinfo/passcount)
- [var pixelsProcessed: Int](/documentation/coreimage/cirenderinfo/pixelsprocessed)
- [var kernelCompileTime: TimeInterval](/documentation/coreimage/cirenderinfo/kernelcompiletime)
- [CIRenderTask](/documentation/coreimage/cirendertask)

### Instance Methods

- [func waitUntilCompleted() throws -> CIRenderInfo](/documentation/coreimage/cirendertask/waituntilcompleted())
- [CIRenderDestinationAlphaMode](/documentation/coreimage/cirenderdestinationalphamode)

### Enumeration Cases

- [case none](/documentation/coreimage/cirenderdestinationalphamode/none)
- [case premultiplied](/documentation/coreimage/cirenderdestinationalphamode/premultiplied)
- [case unpremultiplied](/documentation/coreimage/cirenderdestinationalphamode/unpremultiplied)

### Initializers

- [init?(rawValue: UInt)](/documentation/coreimage/cirenderdestinationalphamode/init(rawvalue:))

## Feedback-Based Processing

- [CIImageAccumulator](/documentation/coreimage/ciimageaccumulator)

### Initializing an Image Accumulator

- [init?(extent: CGRect, format: CIFormat)](/documentation/coreimage/ciimageaccumulator/init(extent:format:))
- [init?(extent: CGRect, format: CIFormat, colorSpace: CGColorSpace)](/documentation/coreimage/ciimageaccumulator/init(extent:format:colorspace:))

### Setting an Image

- [func setImage(CIImage)](/documentation/coreimage/ciimageaccumulator/setimage(_:))
- [func setImage(CIImage, dirtyRect: CGRect)](/documentation/coreimage/ciimageaccumulator/setimage(_:dirtyrect:))

### Obtaining Data From an Image Accumulator

- [var extent: CGRect](/documentation/coreimage/ciimageaccumulator/extent)
- [var format: CIFormat](/documentation/coreimage/ciimageaccumulator/format)
- [func image() -> CIImage](/documentation/coreimage/ciimageaccumulator/image())

### Resetting an Accumulator

- [func clear()](/documentation/coreimage/ciimageaccumulator/clear())

## Barcode Descriptions

- [CIBarcodeDescriptor](/documentation/coreimage/cibarcodedescriptor)
- [CIQRCodeDescriptor](/documentation/coreimage/ciqrcodedescriptor)

### Creating a Descriptor

- [init?(payload: Data, symbolVersion: Int, maskPattern: UInt8, errorCorrectionLevel: CIQRCodeDescriptor.ErrorCorrectionLevel)](/documentation/coreimage/ciqrcodedescriptor/init(payload:symbolversion:maskpattern:errorcorrectionlevel:))

### Examining a Descriptor

- [var errorCorrectedPayload: Data](/documentation/coreimage/ciqrcodedescriptor/errorcorrectedpayload-swift.property)
- [var symbolVersion: Int](/documentation/coreimage/ciqrcodedescriptor/symbolversion-swift.property)
- [var maskPattern: UInt8](/documentation/coreimage/ciqrcodedescriptor/maskpattern-swift.property)
- [var errorCorrectionLevel: CIQRCodeDescriptor.ErrorCorrectionLevel](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.property)

### Error Correction Constants

- [CIQRCodeDescriptor.ErrorCorrectionLevel](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum)

#### Enumeration Cases

- [case levelH](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum/levelh)
- [case levelL](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum/levell)
- [case levelM](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum/levelm)
- [case levelQ](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum/levelq)

#### Initializers

- [init?(rawValue: Int)](/documentation/coreimage/ciqrcodedescriptor/errorcorrectionlevel-swift.enum/init(rawvalue:))
- [CIAztecCodeDescriptor](/documentation/coreimage/ciazteccodedescriptor)

### Creating a Descriptor

- [init?(payload: Data, isCompact: Bool, layerCount: Int, dataCodewordCount: Int)](/documentation/coreimage/ciazteccodedescriptor/init(payload:iscompact:layercount:datacodewordcount:))

### Examining a Descriptor

- [var errorCorrectedPayload: Data](/documentation/coreimage/ciazteccodedescriptor/errorcorrectedpayload-swift.property)
- [var isCompact: Bool](/documentation/coreimage/ciazteccodedescriptor/iscompact-swift.property)
- [var layerCount: Int](/documentation/coreimage/ciazteccodedescriptor/layercount-swift.property)
- [var dataCodewordCount: Int](/documentation/coreimage/ciazteccodedescriptor/datacodewordcount-swift.property)
- [CIPDF417CodeDescriptor](/documentation/coreimage/cipdf417codedescriptor)

### Creating a Descriptor

- [init?(payload: Data, isCompact: Bool, rowCount: Int, columnCount: Int)](/documentation/coreimage/cipdf417codedescriptor/init(payload:iscompact:rowcount:columncount:))

### Examining a Descriptor

- [var errorCorrectedPayload: Data](/documentation/coreimage/cipdf417codedescriptor/errorcorrectedpayload-swift.property)
- [var isCompact: Bool](/documentation/coreimage/cipdf417codedescriptor/iscompact-swift.property)
- [var rowCount: Int](/documentation/coreimage/cipdf417codedescriptor/rowcount-swift.property)
- [var columnCount: Int](/documentation/coreimage/cipdf417codedescriptor/columncount-swift.property)
- [CIDataMatrixCodeDescriptor](/documentation/coreimage/cidatamatrixcodedescriptor)

### Creating a Descriptor

- [init?(payload: Data, rowCount: Int, columnCount: Int, eccVersion: CIDataMatrixCodeDescriptor.ECCVersion)](/documentation/coreimage/cidatamatrixcodedescriptor/init(payload:rowcount:columncount:eccversion:))

### Examining a Descriptor

- [var errorCorrectedPayload: Data](/documentation/coreimage/cidatamatrixcodedescriptor/errorcorrectedpayload-swift.property)
- [var rowCount: Int](/documentation/coreimage/cidatamatrixcodedescriptor/rowcount-swift.property)
- [var columnCount: Int](/documentation/coreimage/cidatamatrixcodedescriptor/columncount-swift.property)
- [var eccVersion: CIDataMatrixCodeDescriptor.ECCVersion](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.property)

### Error Correction Constants

- [CIDataMatrixCodeDescriptor.ECCVersion](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum)

#### Enumeration Cases

- [case v000](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v000)
- [case v050](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v050)
- [case v080](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v080)
- [case v100](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v100)
- [case v140](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v140)
- [case v200](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/v200)

#### Initializers

- [init?(rawValue: Int)](/documentation/coreimage/cidatamatrixcodedescriptor/eccversion-swift.enum/init(rawvalue:))

## Image Feature Detection

- [CIDetector](/documentation/coreimage/cidetector)

### Creating a Detector Object

- [init?(ofType: String, context: CIContext?, options: [String : Any]?)](/documentation/coreimage/cidetector/init(oftype:context:options:))

### Using a Detector Object to Find Features

- [func features(in: CIImage) -> [CIFeature]](/documentation/coreimage/cidetector/features(in:))
- [func features(in: CIImage, options: [String : Any]?) -> [CIFeature]](/documentation/coreimage/cidetector/features(in:options:))

### Constants

- [Detector Types](/documentation/coreimage/detector-types)

#### Constants

- [let CIDetectorTypeFace: String](/documentation/coreimage/cidetectortypeface)
- [let CIDetectorTypeRectangle: String](/documentation/coreimage/cidetectortyperectangle)
- [let CIDetectorTypeQRCode: String](/documentation/coreimage/cidetectortypeqrcode)
- [let CIDetectorTypeText: String](/documentation/coreimage/cidetectortypetext)
- [Detector Configuration Keys](/documentation/coreimage/detector-configuration-keys)

#### Constants

- [let CIDetectorAccuracy: String](/documentation/coreimage/cidetectoraccuracy)
- [let CIDetectorTracking: String](/documentation/coreimage/cidetectortracking)
- [let CIDetectorMinFeatureSize: String](/documentation/coreimage/cidetectorminfeaturesize)
- [let CIDetectorNumberOfAngles: String](/documentation/coreimage/cidetectornumberofangles)
- [let CIDetectorMaxFeatureCount: String](/documentation/coreimage/cidetectormaxfeaturecount)
- [Detector Accuracy Options](/documentation/coreimage/detector-accuracy-options)

#### Constants

- [let CIDetectorAccuracyLow: String](/documentation/coreimage/cidetectoraccuracylow)
- [let CIDetectorAccuracyHigh: String](/documentation/coreimage/cidetectoraccuracyhigh)
- [Feature Detection Keys](/documentation/coreimage/feature-detection-keys)

#### Constants

- [let CIDetectorImageOrientation: String](/documentation/coreimage/cidetectorimageorientation)
- [let CIDetectorEyeBlink: String](/documentation/coreimage/cidetectoreyeblink)
- [let CIDetectorSmile: String](/documentation/coreimage/cidetectorsmile)
- [let CIDetectorFocalLength: String](/documentation/coreimage/cidetectorfocallength)
- [let CIDetectorAspectRatio: String](/documentation/coreimage/cidetectoraspectratio)
- [let CIDetectorReturnSubFeatures: String](/documentation/coreimage/cidetectorreturnsubfeatures)
- [CIFeature](/documentation/coreimage/cifeature)

### Feature Properties

- [var bounds: CGRect](/documentation/coreimage/cifeature/bounds)
- [var type: String](/documentation/coreimage/cifeature/type)

### Feature Types

- [let CIFeatureTypeFace: String](/documentation/coreimage/cifeaturetypeface)
- [let CIFeatureTypeRectangle: String](/documentation/coreimage/cifeaturetyperectangle)
- [let CIFeatureTypeQRCode: String](/documentation/coreimage/cifeaturetypeqrcode)
- [let CIFeatureTypeText: String](/documentation/coreimage/cifeaturetypetext)
- [CIFaceFeature](/documentation/coreimage/cifacefeature)

### Locating Faces

- [var bounds: CGRect](/documentation/coreimage/cifacefeature/bounds-swift.property)
- [var hasFaceAngle: Bool](/documentation/coreimage/cifacefeature/hasfaceangle-swift.property)
- [var faceAngle: Float](/documentation/coreimage/cifacefeature/faceangle-swift.property)

### Identifying Facial Features

- [var hasLeftEyePosition: Bool](/documentation/coreimage/cifacefeature/haslefteyeposition-swift.property)
- [var hasRightEyePosition: Bool](/documentation/coreimage/cifacefeature/hasrighteyeposition-swift.property)
- [var hasMouthPosition: Bool](/documentation/coreimage/cifacefeature/hasmouthposition-swift.property)
- [var leftEyePosition: CGPoint](/documentation/coreimage/cifacefeature/lefteyeposition-swift.property)
- [var rightEyePosition: CGPoint](/documentation/coreimage/cifacefeature/righteyeposition-swift.property)
- [var mouthPosition: CGPoint](/documentation/coreimage/cifacefeature/mouthposition-swift.property)
- [var hasSmile: Bool](/documentation/coreimage/cifacefeature/hassmile-swift.property)
- [var leftEyeClosed: Bool](/documentation/coreimage/cifacefeature/lefteyeclosed-swift.property)
- [var rightEyeClosed: Bool](/documentation/coreimage/cifacefeature/righteyeclosed-swift.property)

### Tracking Distinct Faces in Video

- [var hasTrackingID: Bool](/documentation/coreimage/cifacefeature/hastrackingid-swift.property)
- [var trackingID: Int32](/documentation/coreimage/cifacefeature/trackingid-swift.property)
- [var hasTrackingFrameCount: Bool](/documentation/coreimage/cifacefeature/hastrackingframecount-swift.property)
- [var trackingFrameCount: Int32](/documentation/coreimage/cifacefeature/trackingframecount-swift.property)
- [CIRectangleFeature](/documentation/coreimage/cirectanglefeature)

### Locating a Detected Feature

- [var bounds: CGRect](/documentation/coreimage/cirectanglefeature/bounds-swift.property)

### Identifying the Corners of a Detected Rectangle

- [var bottomLeft: CGPoint](/documentation/coreimage/cirectanglefeature/bottomleft-swift.property)
- [var bottomRight: CGPoint](/documentation/coreimage/cirectanglefeature/bottomright-swift.property)
- [var topLeft: CGPoint](/documentation/coreimage/cirectanglefeature/topleft-swift.property)
- [var topRight: CGPoint](/documentation/coreimage/cirectanglefeature/topright-swift.property)
- [CITextFeature](/documentation/coreimage/citextfeature)

### Locating a Detected Feature

- [var bounds: CGRect](/documentation/coreimage/citextfeature/bounds)

### Locating Features Within a Detected Region

- [var subFeatures: [Any]?](/documentation/coreimage/citextfeature/subfeatures)

### Identifying the Corners of a Detected Text Region

- [var bottomLeft: CGPoint](/documentation/coreimage/citextfeature/bottomleft)
- [var bottomRight: CGPoint](/documentation/coreimage/citextfeature/bottomright)
- [var topLeft: CGPoint](/documentation/coreimage/citextfeature/topleft)
- [var topRight: CGPoint](/documentation/coreimage/citextfeature/topright)
- [CIQRCodeFeature](/documentation/coreimage/ciqrcodefeature)

### Locating a Detected Feature

- [var bounds: CGRect](/documentation/coreimage/ciqrcodefeature/bounds-swift.property)

### Decoding a Detected Barcode

- [var messageString: String?](/documentation/coreimage/ciqrcodefeature/messagestring)
- [var symbolDescriptor: CIQRCodeDescriptor?](/documentation/coreimage/ciqrcodefeature/symboldescriptor-swift.property)

### Identifying the Corners of a Detected Barcode

- [var bottomLeft: CGPoint](/documentation/coreimage/ciqrcodefeature/bottomleft-swift.property)
- [var bottomRight: CGPoint](/documentation/coreimage/ciqrcodefeature/bottomright-swift.property)
- [var topLeft: CGPoint](/documentation/coreimage/ciqrcodefeature/topleft-swift.property)
- [var topRight: CGPoint](/documentation/coreimage/ciqrcodefeature/topright-swift.property)

## Image Units

- [CIPlugIn](/documentation/coreimage/ciplugin)

### Loading Plug-ins

- [class func loadNonExecutablePlugIns()](/documentation/coreimage/ciplugin/loadnonexecutableplugins())
- [class func loadNonExecutablePlugIn(URL!)](/documentation/coreimage/ciplugin/loadnonexecutableplugin(_:))

### Deprecated

- [class func loadAllPlugIns()](/documentation/coreimage/ciplugin/loadallplugins())
- [class func load(URL!, allowExecutableCode: Bool)](/documentation/coreimage/ciplugin/load(_:allowexecutablecode:))
- [CIFilterGenerator](/documentation/coreimage/cifiltergenerator)

### Initializing a Filter Generator Object

- [init?(contentsOf: URL)](/documentation/coreimage/cifiltergenerator/init(contentsof:))

### Connecting and Disconnecting Objects

- [func connect(Any, withKey: String?, to: Any, withKey: String)](/documentation/coreimage/cifiltergenerator/connect(_:withkey:to:withkey:))
- [func disconnectObject(Any, withKey: String, to: Any, withKey: String)](/documentation/coreimage/cifiltergenerator/disconnectobject(_:withkey:to:withkey:))

### Managing Exported Keys

- [var exportedKeys: [AnyHashable : Any]](/documentation/coreimage/cifiltergenerator/exportedkeys)
- [func exportKey(String, from: Any, withName: String?)](/documentation/coreimage/cifiltergenerator/exportkey(_:from:withname:))
- [func removeExportedKey(String)](/documentation/coreimage/cifiltergenerator/removeexportedkey(_:))
- [func setAttributes([AnyHashable : Any], forExportedKey: String)](/documentation/coreimage/cifiltergenerator/setattributes(_:forexportedkey:))

### Setting and Getting Class Attributes

- [var classAttributes: [AnyHashable : Any]](/documentation/coreimage/cifiltergenerator/classattributes)

### Archiving a Filter Generator Object

- [func write(to: URL, atomically: Bool) -> Bool](/documentation/coreimage/cifiltergenerator/write(to:atomically:))

### Registering a Filter Chain

- [func registerFilterName(String)](/documentation/coreimage/cifiltergenerator/registerfiltername(_:))

### Creating a Filter from a Filter Chain

- [func filter() -> CIFilter](/documentation/coreimage/cifiltergenerator/filter())

### Constants

- [Exported Keys](/documentation/coreimage/exported-keys)

#### Constants

- [let kCIFilterGeneratorExportedKeyName: String](/documentation/coreimage/kcifiltergeneratorexportedkeyname)
- [let kCIFilterGeneratorExportedKey: String](/documentation/coreimage/kcifiltergeneratorexportedkey)
- [let kCIFilterGeneratorExportedKeyTargetObject: String](/documentation/coreimage/kcifiltergeneratorexportedkeytargetobject)
- [CIPlugInRegistration](/documentation/coreimage/cipluginregistration)

### Initializing Plug-ins

- [func load(UnsafeMutableRawPointer!) -> Bool](/documentation/coreimage/cipluginregistration/load(_:))
- [CIFilterConstructor](/documentation/coreimage/cifilterconstructor)

### Providing Filter Objects

- [func filter(withName: String) -> CIFilter?](/documentation/coreimage/cifilterconstructor/filter(withname:))

## Protocols

- [CIAreaBoundsRed](/documentation/coreimage/ciareaboundsred)
- [CIMaximumScaleTransform](/documentation/coreimage/cimaximumscaletransform)

### Instance Properties

- [var aspectRatio: Float](/documentation/coreimage/cimaximumscaletransform/aspectratio)
- [var inputImage: CIImage?](/documentation/coreimage/cimaximumscaletransform/inputimage)
- [var scale: Float](/documentation/coreimage/cimaximumscaletransform/scale)
- [CIToneMapHeadroom](/documentation/coreimage/citonemapheadroom)

### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/citonemapheadroom/inputimage)
- [var sourceHeadroom: Float](/documentation/coreimage/citonemapheadroom/sourceheadroom)
- [var targetHeadroom: Float](/documentation/coreimage/citonemapheadroom/targetheadroom)
- [CIAreaAverageMaximumRed](/documentation/coreimage/ciareaaveragemaximumred)
- [CIBlurredRoundedRectangleGenerator](/documentation/coreimage/ciblurredroundedrectanglegenerator)

### Instance Properties

- [var color: CIColor](/documentation/coreimage/ciblurredroundedrectanglegenerator/color)
- [var extent: CGRect](/documentation/coreimage/ciblurredroundedrectanglegenerator/extent)
- [var radius: Float](/documentation/coreimage/ciblurredroundedrectanglegenerator/radius)
- [var sigma: Float](/documentation/coreimage/ciblurredroundedrectanglegenerator/sigma)
- [var smoothness: Float](/documentation/coreimage/ciblurredroundedrectanglegenerator/smoothness)
- [CIDistanceGradientFromRedMask](/documentation/coreimage/cidistancegradientfromredmask)

### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cidistancegradientfromredmask/inputimage)
- [var maximumDistance: Float](/documentation/coreimage/cidistancegradientfromredmask/maximumdistance)
- [CIRoundedQRCodeGenerator](/documentation/coreimage/ciroundedqrcodegenerator)

### Instance Properties

- [var centerSpaceSize: Float](/documentation/coreimage/ciroundedqrcodegenerator/centerspacesize)
- [var color0: CIColor](/documentation/coreimage/ciroundedqrcodegenerator/color0)
- [var color1: CIColor](/documentation/coreimage/ciroundedqrcodegenerator/color1)
- [var correctionLevel: String](/documentation/coreimage/ciroundedqrcodegenerator/correctionlevel)
- [var message: Data](/documentation/coreimage/ciroundedqrcodegenerator/message)
- [var roundedData: Bool](/documentation/coreimage/ciroundedqrcodegenerator/roundeddata)
- [var roundedMarkers: Int](/documentation/coreimage/ciroundedqrcodegenerator/roundedmarkers)
- [var scale: Float](/documentation/coreimage/ciroundedqrcodegenerator/scale)
- [CISignedDistanceGradientFromRedMask](/documentation/coreimage/cisigneddistancegradientfromredmask)

### Instance Properties

- [var inputImage: CIImage?](/documentation/coreimage/cisigneddistancegradientfromredmask/inputimage)
- [var maximumDistance: Float](/documentation/coreimage/cisigneddistancegradientfromredmask/maximumdistance)

## Reference

- [Core Image Constants](/documentation/coreimage/core-image-constants)

### Variables

- [var COREIMAGE_SUPPORTS_IOSURFACE: Int32](/documentation/coreimage/coreimage_supports_iosurface)
- [var COREIMAGE_SUPPORTS_OPENGLES: Int32](/documentation/coreimage/coreimage_supports_opengles)
- [var UNIFIED_CORE_IMAGE: Int32](/documentation/coreimage/unified_core_image)

## Variables

- [let kCIInputBacksideImageKey: String](/documentation/coreimage/kciinputbacksideimagekey)
- [let kCIInputBiasVectorKey: String](/documentation/coreimage/kciinputbiasvectorkey)
- [let kCIInputColor0Key: String](/documentation/coreimage/kciinputcolor0key)
- [let kCIInputColor1Key: String](/documentation/coreimage/kciinputcolor1key)
- [let kCIInputColorSpaceKey: String](/documentation/coreimage/kciinputcolorspacekey)
- [let kCIInputCountKey: String](/documentation/coreimage/kciinputcountkey)
- [let kCIInputExtrapolateKey: String](/documentation/coreimage/kciinputextrapolatekey)
- [let kCIInputPaletteImageKey: String](/documentation/coreimage/kciinputpaletteimagekey)
- [let kCIInputPerceptualKey: String](/documentation/coreimage/kciinputperceptualkey)
- [let kCIInputPoint0Key: String](/documentation/coreimage/kciinputpoint0key)
- [let kCIInputPoint1Key: String](/documentation/coreimage/kciinputpoint1key)
- [let kCIInputRadius0Key: String](/documentation/coreimage/kciinputradius0key)
- [let kCIInputRadius1Key: String](/documentation/coreimage/kciinputradius1key)
- [let kCIInputThresholdKey: String](/documentation/coreimage/kciinputthresholdkey)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
