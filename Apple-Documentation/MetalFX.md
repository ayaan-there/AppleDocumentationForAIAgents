# MetalFX Documentation

Source: https://sosumi.ai/documentation/metalfx

---
title: MetalFX
source: https://developer.apple.com/documentation/metalfx
timestamp: 2026-02-13T18:59:41.127Z
---

## Temporal scaling

- [Applying temporal antialiasing and upscaling using MetalFX](/documentation/metalfx/applying-temporal-antialiasing-and-upscaling-using-metalfx)
- [MTLFXTemporalScaler](/documentation/metalfx/mtlfxtemporalscaler)

### Encoding a temporal scaling effect

- [func encode(commandBuffer: any MTLCommandBuffer)](/documentation/metalfx/mtlfxtemporalscaler/encode(commandbuffer:))
- [MTLFXTemporalScalerDescriptor](/documentation/metalfx/mtlfxtemporalscalerdescriptor)

### Checking a GPU device’s scaling support

- [class func supportsDevice(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/supportsdevice(_:))
- [class func supportedInputContentMinScale(device: any MTLDevice) -> Float](/documentation/metalfx/mtlfxtemporalscalerdescriptor/supportedinputcontentminscale(device:))
- [class func supportedInputContentMaxScale(device: any MTLDevice) -> Float](/documentation/metalfx/mtlfxtemporalscalerdescriptor/supportedinputcontentmaxscale(device:))

### Configuring a temporal effect’s input

- [var inputWidth: Int](/documentation/metalfx/mtlfxtemporalscalerdescriptor/inputwidth)
- [var inputHeight: Int](/documentation/metalfx/mtlfxtemporalscalerdescriptor/inputheight)
- [var isInputContentPropertiesEnabled: Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/isinputcontentpropertiesenabled)
- [var inputContentMinScale: Float](/documentation/metalfx/mtlfxtemporalscalerdescriptor/inputcontentminscale)
- [var inputContentMaxScale: Float](/documentation/metalfx/mtlfxtemporalscalerdescriptor/inputcontentmaxscale)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerdescriptor/colortextureformat)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerdescriptor/motiontextureformat)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerdescriptor/depthtextureformat)
- [var isAutoExposureEnabled: Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/isautoexposureenabled)
- [var requiresSynchronousInitialization: Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/requiressynchronousinitialization)
- [var isReactiveMaskTextureEnabled: Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/isreactivemasktextureenabled)
- [var reactiveMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerdescriptor/reactivemasktextureformat)

### Configuring a temporal effect’s output

- [var outputWidth: Int](/documentation/metalfx/mtlfxtemporalscalerdescriptor/outputwidth)
- [var outputHeight: Int](/documentation/metalfx/mtlfxtemporalscalerdescriptor/outputheight)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerdescriptor/outputtextureformat)

### Creating temporal scaling effect instances

- [func makeTemporalScaler(device: any MTLDevice) -> (any MTLFXTemporalScaler)?](/documentation/metalfx/mtlfxtemporalscalerdescriptor/maketemporalscaler(device:))

### Instance Methods

- [func makeTemporalScaler(device: any MTLDevice, compiler: any MTL4Compiler) -> (any MTL4FXTemporalScaler)?](/documentation/metalfx/mtlfxtemporalscalerdescriptor/maketemporalscaler(device:compiler:))

### Type Methods

- [class func supportsMetal4FX(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxtemporalscalerdescriptor/supportsmetal4fx(_:))

## Spatial scaling

- [MTLFXSpatialScaler](/documentation/metalfx/mtlfxspatialscaler)

### Encoding a spatial scaler

- [func encode(commandBuffer: any MTLCommandBuffer)](/documentation/metalfx/mtlfxspatialscaler/encode(commandbuffer:))
- [MTLFXSpatialScalerDescriptor](/documentation/metalfx/mtlfxspatialscalerdescriptor)

### Checking a GPU device’s scaling support

- [class func supportsDevice(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxspatialscalerdescriptor/supportsdevice(_:))

### Configuring a spatial scaler’s input

- [var inputWidth: Int](/documentation/metalfx/mtlfxspatialscalerdescriptor/inputwidth)
- [var inputHeight: Int](/documentation/metalfx/mtlfxspatialscalerdescriptor/inputheight)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxspatialscalerdescriptor/colortextureformat)
- [var colorProcessingMode: MTLFXSpatialScalerColorProcessingMode](/documentation/metalfx/mtlfxspatialscalerdescriptor/colorprocessingmode)

### Configuring a spatial scaler’s output

- [var outputWidth: Int](/documentation/metalfx/mtlfxspatialscalerdescriptor/outputwidth)
- [var outputHeight: Int](/documentation/metalfx/mtlfxspatialscalerdescriptor/outputheight)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxspatialscalerdescriptor/outputtextureformat)

### Creating spatial scaler instances

- [func makeSpatialScaler(device: any MTLDevice) -> (any MTLFXSpatialScaler)?](/documentation/metalfx/mtlfxspatialscalerdescriptor/makespatialscaler(device:))

### Instance Methods

- [func makeSpatialScaler(device: any MTLDevice, compiler: any MTL4Compiler) -> (any MTL4FXSpatialScaler)?](/documentation/metalfx/mtlfxspatialscalerdescriptor/makespatialscaler(device:compiler:))

### Type Methods

- [class func supportsMetal4FX(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxspatialscalerdescriptor/supportsmetal4fx(_:))
- [MTLFXSpatialScalerColorProcessingMode](/documentation/metalfx/mtlfxspatialscalercolorprocessingmode)

### Color space modes

- [case linear](/documentation/metalfx/mtlfxspatialscalercolorprocessingmode/linear)
- [case perceptual](/documentation/metalfx/mtlfxspatialscalercolorprocessingmode/perceptual)
- [case hdr](/documentation/metalfx/mtlfxspatialscalercolorprocessingmode/hdr)

### Initializers

- [init?(rawValue: Int)](/documentation/metalfx/mtlfxspatialscalercolorprocessingmode/init(rawvalue:))

## Classes

- [MTLFXFrameInterpolatorDescriptor](/documentation/metalfx/mtlfxframeinterpolatordescriptor)

### Instance Properties

- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatordescriptor/colortextureformat)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatordescriptor/depthtextureformat)
- [var inputHeight: Int](/documentation/metalfx/mtlfxframeinterpolatordescriptor/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxframeinterpolatordescriptor/inputwidth)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatordescriptor/motiontextureformat)
- [var outputHeight: Int](/documentation/metalfx/mtlfxframeinterpolatordescriptor/outputheight)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatordescriptor/outputtextureformat)
- [var outputWidth: Int](/documentation/metalfx/mtlfxframeinterpolatordescriptor/outputwidth)
- [var scaler: (any MTLFXFrameInterpolatableScaler)?](/documentation/metalfx/mtlfxframeinterpolatordescriptor/scaler)
- [var uiTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatordescriptor/uitextureformat)

### Instance Methods

- [func makeFrameInterpolator(device: any MTLDevice) -> (any MTLFXFrameInterpolator)?](/documentation/metalfx/mtlfxframeinterpolatordescriptor/makeframeinterpolator(device:))
- [func makeFrameInterpolator(device: any MTLDevice, compiler: any MTL4Compiler) -> (any MTL4FXFrameInterpolator)?](/documentation/metalfx/mtlfxframeinterpolatordescriptor/makeframeinterpolator(device:compiler:))

### Type Methods

- [class func supportsDevice(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxframeinterpolatordescriptor/supportsdevice(_:))
- [class func supportsMetal4FX(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxframeinterpolatordescriptor/supportsmetal4fx(_:))
- [MTLFXTemporalDenoisedScalerDescriptor](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor)

### Instance Properties

- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/colortextureformat)
- [var denoiseStrengthMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/denoisestrengthmasktextureformat)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/depthtextureformat)
- [var diffuseAlbedoTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/diffusealbedotextureformat)
- [var inputHeight: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/inputwidth)
- [var isAutoExposureEnabled: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/isautoexposureenabled)
- [var isDenoiseStrengthMaskTextureEnabled: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/isdenoisestrengthmasktextureenabled)
- [var isReactiveMaskTextureEnabled: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/isreactivemasktextureenabled)
- [var isSpecularHitDistanceTextureEnabled: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/isspecularhitdistancetextureenabled)
- [var isTransparencyOverlayTextureEnabled: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/istransparencyoverlaytextureenabled)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/motiontextureformat)
- [var normalTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/normaltextureformat)
- [var outputHeight: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/outputheight)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/outputtextureformat)
- [var outputWidth: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/outputwidth)
- [var reactiveMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/reactivemasktextureformat)
- [var requiresSynchronousInitialization: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/requiressynchronousinitialization)
- [var roughnessTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/roughnesstextureformat)
- [var specularAlbedoTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/specularalbedotextureformat)
- [var specularHitDistanceTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/specularhitdistancetextureformat)
- [var transparencyOverlayTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/transparencyoverlaytextureformat)

### Instance Methods

- [func makeTemporalDenoisedScaler(device: any MTLDevice) -> (any MTLFXTemporalDenoisedScaler)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/maketemporaldenoisedscaler(device:))
- [func makeTemporalDenoisedScaler(device: any MTLDevice, compiler: any MTL4Compiler) -> (any MTL4FXTemporalDenoisedScaler)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/maketemporaldenoisedscaler(device:compiler:))

### Type Methods

- [class func supportedInputContentMaxScale(device: any MTLDevice) -> Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/supportedinputcontentmaxscale(device:))
- [class func supportedInputContentMinScale(device: any MTLDevice) -> Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/supportedinputcontentminscale(device:))
- [class func supportsDevice(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/supportsdevice(_:))
- [class func supportsMetal4FX(any MTLDevice) -> Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerdescriptor/supportsmetal4fx(_:))

## Protocols

- [MTL4FXFrameInterpolator](/documentation/metalfx/mtl4fxframeinterpolator)

### Instance Methods

- [func encode(commandBuffer: any MTL4CommandBuffer)](/documentation/metalfx/mtl4fxframeinterpolator/encode(commandbuffer:))
- [MTL4FXSpatialScaler](/documentation/metalfx/mtl4fxspatialscaler)

### Instance Methods

- [func encode(commandBuffer: any MTL4CommandBuffer)](/documentation/metalfx/mtl4fxspatialscaler/encode(commandbuffer:))
- [MTL4FXTemporalDenoisedScaler](/documentation/metalfx/mtl4fxtemporaldenoisedscaler)

### Instance Methods

- [func encode(commandBuffer: any MTL4CommandBuffer)](/documentation/metalfx/mtl4fxtemporaldenoisedscaler/encode(commandbuffer:))
- [MTL4FXTemporalScaler](/documentation/metalfx/mtl4fxtemporalscaler)

### Instance Methods

- [func encode(commandBuffer: any MTL4CommandBuffer)](/documentation/metalfx/mtl4fxtemporalscaler/encode(commandbuffer:))
- [MTLFXFrameInterpolatableScaler](/documentation/metalfx/mtlfxframeinterpolatablescaler)
- [MTLFXFrameInterpolator](/documentation/metalfx/mtlfxframeinterpolator)

### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer)](/documentation/metalfx/mtlfxframeinterpolator/encode(commandbuffer:))
- [MTLFXFrameInterpolatorBase](/documentation/metalfx/mtlfxframeinterpolatorbase)

### Instance Properties

- [var aspectRatio: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/aspectratio)
- [var colorTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/colortexture)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatorbase/colortextureformat)
- [var colorTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxframeinterpolatorbase/colortextureusage)
- [var deltaTime: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/deltatime)
- [var depthTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/depthtexture)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatorbase/depthtextureformat)
- [var depthTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxframeinterpolatorbase/depthtextureusage)
- [var farPlane: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/farplane)
- [var fence: (any MTLFence)?](/documentation/metalfx/mtlfxframeinterpolatorbase/fence)
- [var fieldOfView: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/fieldofview)
- [var inputHeight: Int](/documentation/metalfx/mtlfxframeinterpolatorbase/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxframeinterpolatorbase/inputwidth)
- [var isDepthReversed: Bool](/documentation/metalfx/mtlfxframeinterpolatorbase/isdepthreversed)
- [var isUITextureComposited: Bool](/documentation/metalfx/mtlfxframeinterpolatorbase/isuitexturecomposited)
- [var jitterOffsetX: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/jitteroffsetx)
- [var jitterOffsetY: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/jitteroffsety)
- [var motionTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/motiontexture)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatorbase/motiontextureformat)
- [var motionTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxframeinterpolatorbase/motiontextureusage)
- [var motionVectorScaleX: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/motionvectorscalex)
- [var motionVectorScaleY: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/motionvectorscaley)
- [var nearPlane: Float](/documentation/metalfx/mtlfxframeinterpolatorbase/nearplane)
- [var outputHeight: Int](/documentation/metalfx/mtlfxframeinterpolatorbase/outputheight)
- [var outputTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/outputtexture)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatorbase/outputtextureformat)
- [var outputTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxframeinterpolatorbase/outputtextureusage)
- [var outputWidth: Int](/documentation/metalfx/mtlfxframeinterpolatorbase/outputwidth)
- [var prevColorTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/prevcolortexture)
- [var shouldResetHistory: Bool](/documentation/metalfx/mtlfxframeinterpolatorbase/shouldresethistory)
- [var uiTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxframeinterpolatorbase/uitexture)
- [var uiTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxframeinterpolatorbase/uitextureformat)
- [var uiTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxframeinterpolatorbase/uitextureusage)
- [MTLFXSpatialScalerBase](/documentation/metalfx/mtlfxspatialscalerbase)

### Instance Properties

- [var colorProcessingMode: MTLFXSpatialScalerColorProcessingMode](/documentation/metalfx/mtlfxspatialscalerbase/colorprocessingmode)
- [var colorTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxspatialscalerbase/colortexture)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxspatialscalerbase/colortextureformat)
- [var colorTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxspatialscalerbase/colortextureusage)
- [var fence: (any MTLFence)?](/documentation/metalfx/mtlfxspatialscalerbase/fence)
- [var inputContentHeight: Int](/documentation/metalfx/mtlfxspatialscalerbase/inputcontentheight)
- [var inputContentWidth: Int](/documentation/metalfx/mtlfxspatialscalerbase/inputcontentwidth)
- [var inputHeight: Int](/documentation/metalfx/mtlfxspatialscalerbase/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxspatialscalerbase/inputwidth)
- [var outputHeight: Int](/documentation/metalfx/mtlfxspatialscalerbase/outputheight)
- [var outputTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxspatialscalerbase/outputtexture)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxspatialscalerbase/outputtextureformat)
- [var outputTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxspatialscalerbase/outputtextureusage)
- [var outputWidth: Int](/documentation/metalfx/mtlfxspatialscalerbase/outputwidth)
- [MTLFXTemporalDenoisedScaler](/documentation/metalfx/mtlfxtemporaldenoisedscaler)

### Instance Methods

- [func encode(commandBuffer: any MTLCommandBuffer)](/documentation/metalfx/mtlfxtemporaldenoisedscaler/encode(commandbuffer:))
- [MTLFXTemporalDenoisedScalerBase](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase)

### Instance Properties

- [var colorTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/colortexture)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/colortextureformat)
- [var colorTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/colortextureusage)
- [var denoiseStrengthMaskTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/denoisestrengthmasktexture)
- [var denoiseStrengthMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/denoisestrengthmasktextureformat)
- [var denoiseStrengthMaskTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/denoisestrengthmasktextureusage)
- [var depthTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/depthtexture)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/depthtextureformat)
- [var depthTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/depthtextureusage)
- [var diffuseAlbedoTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/diffusealbedotexture)
- [var diffuseAlbedoTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/diffusealbedotextureformat)
- [var diffuseAlbedoTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/diffusealbedotextureusage)
- [var exposureTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/exposuretexture)
- [var fence: (any MTLFence)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/fence)
- [var inputContentMaxScale: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/inputcontentmaxscale)
- [var inputContentMinScale: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/inputcontentminscale)
- [var inputHeight: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/inputwidth)
- [var isDepthReversed: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/isdepthreversed)
- [var jitterOffsetX: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/jitteroffsetx)
- [var jitterOffsetY: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/jitteroffsety)
- [var motionTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/motiontexture)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/motiontextureformat)
- [var motionTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/motiontextureusage)
- [var motionVectorScaleX: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/motionvectorscalex)
- [var motionVectorScaleY: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/motionvectorscaley)
- [var normalTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/normaltexture)
- [var normalTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/normaltextureformat)
- [var normalTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/normaltextureusage)
- [var outputHeight: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/outputheight)
- [var outputTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/outputtexture)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/outputtextureformat)
- [var outputTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/outputtextureusage)
- [var outputWidth: Int](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/outputwidth)
- [var preExposure: Float](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/preexposure)
- [var reactiveMaskTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/reactivemasktexture)
- [var reactiveMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/reactivemasktextureformat)
- [var reactiveTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/reactivetextureusage)
- [var roughnessTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/roughnesstexture)
- [var roughnessTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/roughnesstextureformat)
- [var roughnessTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/roughnesstextureusage)
- [var shouldResetHistory: Bool](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/shouldresethistory)
- [var specularAlbedoTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularalbedotexture)
- [var specularAlbedoTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularalbedotextureformat)
- [var specularAlbedoTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularalbedotextureusage)
- [var specularHitDistanceTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularhitdistancetexture)
- [var specularHitDistanceTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularhitdistancetextureformat)
- [var specularHitDistanceTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/specularhitdistancetextureusage)
- [var transparencyOverlayTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/transparencyoverlaytexture)
- [var transparencyOverlayTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/transparencyoverlaytextureformat)
- [var transparencyOverlayTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/transparencyoverlaytextureusage)
- [var viewToClipMatrix: simd_float4x4](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/viewtoclipmatrix)
- [var worldToViewMatrix: simd_float4x4](/documentation/metalfx/mtlfxtemporaldenoisedscalerbase/worldtoviewmatrix)
- [MTLFXTemporalScalerBase](/documentation/metalfx/mtlfxtemporalscalerbase)

### Instance Properties

- [var colorTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/colortexture)
- [var colorTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerbase/colortextureformat)
- [var colorTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporalscalerbase/colortextureusage)
- [var depthTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/depthtexture)
- [var depthTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerbase/depthtextureformat)
- [var depthTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporalscalerbase/depthtextureusage)
- [var exposureTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/exposuretexture)
- [var fence: (any MTLFence)?](/documentation/metalfx/mtlfxtemporalscalerbase/fence)
- [var inputContentHeight: Int](/documentation/metalfx/mtlfxtemporalscalerbase/inputcontentheight)
- [var inputContentMaxScale: Float](/documentation/metalfx/mtlfxtemporalscalerbase/inputcontentmaxscale)
- [var inputContentMinScale: Float](/documentation/metalfx/mtlfxtemporalscalerbase/inputcontentminscale)
- [var inputContentWidth: Int](/documentation/metalfx/mtlfxtemporalscalerbase/inputcontentwidth)
- [var inputHeight: Int](/documentation/metalfx/mtlfxtemporalscalerbase/inputheight)
- [var inputWidth: Int](/documentation/metalfx/mtlfxtemporalscalerbase/inputwidth)
- [var isDepthReversed: Bool](/documentation/metalfx/mtlfxtemporalscalerbase/isdepthreversed)
- [var jitterOffsetX: Float](/documentation/metalfx/mtlfxtemporalscalerbase/jitteroffsetx)
- [var jitterOffsetY: Float](/documentation/metalfx/mtlfxtemporalscalerbase/jitteroffsety)
- [var motionTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/motiontexture)
- [var motionTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerbase/motiontextureformat)
- [var motionTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporalscalerbase/motiontextureusage)
- [var motionVectorScaleX: Float](/documentation/metalfx/mtlfxtemporalscalerbase/motionvectorscalex)
- [var motionVectorScaleY: Float](/documentation/metalfx/mtlfxtemporalscalerbase/motionvectorscaley)
- [var outputHeight: Int](/documentation/metalfx/mtlfxtemporalscalerbase/outputheight)
- [var outputTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/outputtexture)
- [var outputTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerbase/outputtextureformat)
- [var outputTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporalscalerbase/outputtextureusage)
- [var outputWidth: Int](/documentation/metalfx/mtlfxtemporalscalerbase/outputwidth)
- [var preExposure: Float](/documentation/metalfx/mtlfxtemporalscalerbase/preexposure)
- [var reactiveMaskTexture: (any MTLTexture)?](/documentation/metalfx/mtlfxtemporalscalerbase/reactivemasktexture)
- [var reactiveMaskTextureFormat: MTLPixelFormat](/documentation/metalfx/mtlfxtemporalscalerbase/reactivemasktextureformat)
- [var reactiveTextureUsage: MTLTextureUsage](/documentation/metalfx/mtlfxtemporalscalerbase/reactivetextureusage)
- [var reset: Bool](/documentation/metalfx/mtlfxtemporalscalerbase/reset)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
