# Compositor Services Documentation

Source: https://sosumi.ai/documentation/compositorservices

---
title: Compositor Services
source: https://developer.apple.com/documentation/compositorservices
timestamp: 2026-02-13T18:55:02.019Z
---

## App integration

- [Drawing fully immersive content using Metal](/documentation/compositorservices/drawing-fully-immersive-content-using-metal)
- [Interacting with virtual content blended with passthrough](/documentation/compositorservices/interacting-with-virtual-content-blended-with-passthrough)
- [Rendering hover effects in Metal immersive apps](/documentation/compositorservices/rendering_hover_effects_in_metal_immersive_apps)
- [CompositorLayer](/documentation/compositorservices/compositorlayer)

### Initializers

- [init(configuration: any CompositorLayerConfiguration, renderer: (LayerRenderer) -> Void)](/documentation/compositorservices/compositorlayer/init(configuration:renderer:)-2uxn7)
- [init(configuration: any CompositorLayerConfiguration, renderer: (LayerRenderer, NWEndpoint?) -> Void)](/documentation/compositorservices/compositorlayer/init(configuration:renderer:)-81vbz)
- [init(configuration: any CompositorLayerConfiguration, renderer: (LayerRenderer) -> Void, Void)](/documentation/compositorservices/compositorlayer/init(configuration:renderer:_:))
- [CompositorLayerConfiguration](/documentation/compositorservices/compositorlayerconfiguration)

### Specifying the custom options

- [func makeConfiguration(capabilities: LayerRenderer.Capabilities, configuration: inout LayerRenderer.Configuration)](/documentation/compositorservices/compositorlayerconfiguration/makeconfiguration(capabilities:configuration:))

### Getting the default options

- [static var `default`: DefaultCompositorLayerConfiguration](/documentation/compositorservices/compositorlayerconfiguration/default)
- [DefaultCompositorLayerConfiguration](/documentation/compositorservices/defaultcompositorlayerconfiguration)

## Render-loop setup

- [LayerRenderer](/documentation/compositorservices/layerrenderer)

### Configuring the layer renderer

- [var configuration: LayerRenderer.Configuration](/documentation/compositorservices/layerrenderer/configuration-swift.property)
- [LayerRenderer.Configuration](/documentation/compositorservices/layerrenderer/configuration-swift.struct)

#### Configuring the color textures

- [var colorFormat: MTLPixelFormat](/documentation/compositorservices/layerrenderer/configuration-swift.struct/colorformat)
- [var colorUsage: MTLTextureUsage](/documentation/compositorservices/layerrenderer/configuration-swift.struct/colorusage)

#### Configuring the depth information

- [var depthFormat: MTLPixelFormat](/documentation/compositorservices/layerrenderer/configuration-swift.struct/depthformat)
- [var depthUsage: MTLTextureUsage](/documentation/compositorservices/layerrenderer/configuration-swift.struct/depthusage)
- [var defaultDepthRange: SIMD2<Float>](/documentation/compositorservices/layerrenderer/configuration-swift.struct/defaultdepthrange)

#### Configuring the texture layout

- [var layout: LayerRenderer.Layout](/documentation/compositorservices/layerrenderer/configuration-swift.struct/layout)
- [LayerRenderer.Layout](/documentation/compositorservices/layerrenderer/layout)

##### Getting the texture layouts

- [case dedicated](/documentation/compositorservices/layerrenderer/layout/dedicated)
- [case shared](/documentation/compositorservices/layerrenderer/layout/shared)
- [case layered](/documentation/compositorservices/layerrenderer/layout/layered)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/layout/init(rawvalue:))

#### Configuring the foveation setting

- [var isFoveationEnabled: Bool](/documentation/compositorservices/layerrenderer/configuration-swift.struct/isfoveationenabled)
- [var generateFlippedRasterizationRateMaps: Bool](/documentation/compositorservices/layerrenderer/configuration-swift.struct/generateflippedrasterizationratemaps)

#### Configurating the render context

- [var drawableRenderContextStencilFormat: MTLPixelFormat](/documentation/compositorservices/layerrenderer/configuration-swift.struct/drawablerendercontextstencilformat)
- [var drawableRenderContextRasterSampleCount: Int](/documentation/compositorservices/layerrenderer/configuration-swift.struct/drawablerendercontextrastersamplecount)

#### Configuring quality level

- [var maxRenderQuality: LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/configuration-swift.struct/maxrenderquality)

#### Instance Properties

- [var supportsMTL4: Bool](/documentation/compositorservices/layerrenderer/configuration-swift.struct/supportsmtl4)
- [var trackingAreasFormat: MTLPixelFormat](/documentation/compositorservices/layerrenderer/configuration-swift.struct/trackingareasformat)
- [var trackingAreasUsage: MTLTextureUsage](/documentation/compositorservices/layerrenderer/configuration-swift.struct/trackingareasusage)
- [LayerRenderer.Capabilities](/documentation/compositorservices/layerrenderer/capabilities)

#### Getting the supported formats

- [var supportedColorFormats: [MTLPixelFormat]](/documentation/compositorservices/layerrenderer/capabilities/supportedcolorformats)
- [var supportedDepthFormats: [MTLPixelFormat]](/documentation/compositorservices/layerrenderer/capabilities/supporteddepthformats)

#### Getting the supported layouts

- [func supportedLayouts(options: LayerRenderer.Capabilities.SupportedLayoutsOptions) -> [LayerRenderer.Layout]](/documentation/compositorservices/layerrenderer/capabilities/supportedlayouts(options:))
- [LayerRenderer.Capabilities.SupportedLayoutsOptions](/documentation/compositorservices/layerrenderer/capabilities/supportedlayoutsoptions)

##### Getting the options

- [static let foveationEnabled: LayerRenderer.Capabilities.SupportedLayoutsOptions](/documentation/compositorservices/layerrenderer/capabilities/supportedlayoutsoptions/foveationenabled)

##### Type Properties

- [static let progressiveImmersionEnabled: LayerRenderer.Capabilities.SupportedLayoutsOptions](/documentation/compositorservices/layerrenderer/capabilities/supportedlayoutsoptions/progressiveimmersionenabled)

#### Getting the supported layer features

- [var supportsFoveation: Bool](/documentation/compositorservices/layerrenderer/capabilities/supportsfoveation)

#### Getting the minimum near plane distance

- [var supportedMinimumNearPlaneDistance: Float](/documentation/compositorservices/layerrenderer/capabilities/supportedminimumnearplanedistance)

#### Determining supported stencil formats

- [var drawableRenderContextSupportedStencilFormats: [MTLPixelFormat]](/documentation/compositorservices/layerrenderer/capabilities/drawablerendercontextsupportedstencilformats)

#### Getting render quality

- [var defaultRenderQuality: LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/capabilities/defaultrenderquality)

#### Structures

- [LayerRenderer.Capabilities.SupportedColorFormatsOptions](/documentation/compositorservices/layerrenderer/capabilities/supportedcolorformatsoptions)

##### Type Properties

- [static let progressiveImmersionEnabled: LayerRenderer.Capabilities.SupportedColorFormatsOptions](/documentation/compositorservices/layerrenderer/capabilities/supportedcolorformatsoptions/progressiveimmersionenabled)

#### Instance Properties

- [var supportedTrackingAreasFormats: [MTLPixelFormat]](/documentation/compositorservices/layerrenderer/capabilities/supportedtrackingareasformats)

#### Instance Methods

- [func supportedColorFormats(options: LayerRenderer.Capabilities.SupportedColorFormatsOptions) -> [MTLPixelFormat]](/documentation/compositorservices/layerrenderer/capabilities/supportedcolorformats(options:))

### Getting the layer renderer properties

- [var properties: LayerRenderer.Properties](/documentation/compositorservices/layerrenderer/properties-swift.property)
- [LayerRenderer.Properties](/documentation/compositorservices/layerrenderer/properties-swift.struct)

#### Creating representative properties

- [init(configuration: LayerRenderer.Configuration) throws](/documentation/compositorservices/layerrenderer/properties-swift.struct/init(configuration:))

#### Getting view port information

- [var viewCount: Int](/documentation/compositorservices/layerrenderer/properties-swift.struct/viewcount)

#### Getting the layer’s texture topology

- [var textureTopologies: [TextureTopology]](/documentation/compositorservices/layerrenderer/properties-swift.struct/texturetopologies)
- [TextureTopology](/documentation/compositorservices/texturetopology)

##### Getting the topology type

- [var textureType: MTLTextureType](/documentation/compositorservices/texturetopology/texturetype)

##### Getting the array length

- [var arrayLength: UInt64](/documentation/compositorservices/texturetopology/arraylength)

##### Creating a topology

- [init()](/documentation/compositorservices/texturetopology/init())

#### Instance Properties

- [var trackingAreasMaxValue: LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/properties-swift.struct/trackingareasmaxvalue)

### Getting the GPU device

- [var device: any MTLDevice](/documentation/compositorservices/layerrenderer/device)

### Managing the rendering loop

- [var state: LayerRenderer.State](/documentation/compositorservices/layerrenderer/state-swift.property)
- [func waitUntilRunning()](/documentation/compositorservices/layerrenderer/waituntilrunning())
- [LayerRenderer.State](/documentation/compositorservices/layerrenderer/state-swift.enum)

#### Getting the states

- [case paused](/documentation/compositorservices/layerrenderer/state-swift.enum/paused)
- [case running](/documentation/compositorservices/layerrenderer/state-swift.enum/running)
- [case invalidated](/documentation/compositorservices/layerrenderer/state-swift.enum/invalidated)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/state-swift.enum/init(rawvalue:))
- [LayerRenderer.Clock](/documentation/compositorservices/layerrenderer/clock)

#### Putting the current thread to sleep

- [func wait(until: LayerRenderer.Clock.Instant, tolerance: Duration?)](/documentation/compositorservices/layerrenderer/clock/wait(until:tolerance:))

#### Creating a clock

- [init()](/documentation/compositorservices/layerrenderer/clock/init())

### Drawing a frame of content

- [func queryNextFrame() -> LayerRenderer.Frame?](/documentation/compositorservices/layerrenderer/querynextframe())
- [LayerRenderer.Frame](/documentation/compositorservices/layerrenderer/frame)

#### Getting timing information

- [func predictTiming() -> LayerRenderer.Frame.Timing?](/documentation/compositorservices/layerrenderer/frame/predicttiming())
- [LayerRenderer.Frame.Timing](/documentation/compositorservices/layerrenderer/frame/timing)

##### Updating the frame contents

- [var optimalInputTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/optimalinputtime)

##### Rendering the frame

- [var renderingDeadline: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/renderingdeadline)

##### Displaying the frame

- [var presentationTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/presentationtime)

##### Creating the timing details

- [init()](/documentation/compositorservices/layerrenderer/frame/timing/init())

##### Instance Properties

- [var trackableAnchorTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/trackableanchortime)

#### Reporting frame update times

- [func startUpdate()](/documentation/compositorservices/layerrenderer/frame/startupdate())
- [func endUpdate()](/documentation/compositorservices/layerrenderer/frame/endupdate())

#### Getting the drawable environment

- [func queryDrawables() -> [LayerRenderer.Drawable]](/documentation/compositorservices/layerrenderer/frame/querydrawables())
- [func queryDrawable() -> LayerRenderer.Drawable?](/documentation/compositorservices/layerrenderer/frame/querydrawable())

#### Reporting frame submission times

- [func startSubmission()](/documentation/compositorservices/layerrenderer/frame/startsubmission())
- [func endSubmission()](/documentation/compositorservices/layerrenderer/frame/endsubmission())

#### Getting frame-related details

- [var frameIndex: LayerFrameIndex](/documentation/compositorservices/layerrenderer/frame/frameindex)
- [LayerFrameIndex](/documentation/compositorservices/layerframeindex)
- [CompositorFrameIndex](/documentation/compositorservices/compositorframeindex)

#### Creating a frame

- [init()](/documentation/compositorservices/layerrenderer/frame/init())

#### Instance Methods

- [func binocularFrustumMatrix(convention: AxisDirectionConvention, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/binocularfrustummatrix(convention:increasetangents:depthrange:))
- [func binocularFrustumMatrixForDrawableTarget(drawableTarget: LayerRenderer.Drawable.Target, convention: AxisDirectionConvention, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/binocularfrustummatrixfordrawabletarget(drawabletarget:convention:increasetangents:depthrange:))
- [func drawableTargetViewCount(target: LayerRenderer.Drawable.Target) -> Int](/documentation/compositorservices/layerrenderer/frame/drawabletargetviewcount(target:))
- [func monocularFrustumMatrix(convention: AxisDirectionConvention, viewIndex: Int, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/monocularfrustummatrix(convention:viewindex:increasetangents:depthrange:))
- [func monocularFrustumMatrixForDrawableTarget(drawableTarget: LayerRenderer.Drawable.Target, convention: AxisDirectionConvention, viewIndex: Int, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/monocularfrustummatrixfordrawabletarget(drawabletarget:convention:viewindex:increasetangents:depthrange:))
- [LayerRenderer.Drawable](/documentation/compositorservices/layerrenderer/drawable)

#### Getting the views

- [var views: [LayerRenderer.Drawable.View]](/documentation/compositorservices/layerrenderer/drawable/views)
- [LayerRenderer.Drawable.View](/documentation/compositorservices/layerrenderer/drawable/view)

##### Getting the view’s texture map

- [var textureMap: LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.property)
- [LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct)

###### Getting the viewport

- [var viewport: MTLViewport](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/viewport)

###### Getting the texture indices

- [var sliceIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/sliceindex)
- [var textureIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/textureindex)

###### Creating a texture map

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/init())

##### Getting the transformations

- [var transform: simd_float4x4](/documentation/compositorservices/layerrenderer/drawable/view/transform)
- [var tangents: simd_float4](/documentation/compositorservices/layerrenderer/drawable/view/tangents)

##### Creating a view

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/init())

#### Accessing the device orientation

- [var deviceAnchor: DeviceAnchor?](/documentation/compositorservices/layerrenderer/drawable/deviceanchor)

#### Getting the render textures

- [var colorTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/colortextures)
- [var depthTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/depthtextures)

#### Enqueueing a command buffer

- [func encodePresent(commandBuffer: any MTLCommandBuffer)](/documentation/compositorservices/layerrenderer/drawable/encodepresent(commandbuffer:))

#### Getting the rasterization rate map

- [var rasterizationRateMaps: [any MTLRasterizationRateMap]](/documentation/compositorservices/layerrenderer/drawable/rasterizationratemaps)
- [var flippedRasterizationRateMaps: [any MTLRasterizationRateMap]](/documentation/compositorservices/layerrenderer/drawable/flippedrasterizationratemaps)

#### Getting the projection matrix

- [AxisDirectionConvention](/documentation/compositorservices/axisdirectionconvention)

##### Getting the axis directions

- [case rightUpBack](/documentation/compositorservices/axisdirectionconvention/rightupback)
- [case rightUpForward](/documentation/compositorservices/axisdirectionconvention/rightupforward)
- [case rightDownBack](/documentation/compositorservices/axisdirectionconvention/rightdownback)
- [case rightDownForward](/documentation/compositorservices/axisdirectionconvention/rightdownforward)

##### Initializers

- [init?(rawValue: UInt8)](/documentation/compositorservices/axisdirectionconvention/init(rawvalue:))

#### Accessing pixel depth information

- [var depthRange: simd_float2](/documentation/compositorservices/layerrenderer/drawable/depthrange)

#### Managing the state machine

- [var state: LayerRenderer.Drawable.State](/documentation/compositorservices/layerrenderer/drawable/state-swift.property)
- [LayerRenderer.Drawable.State](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum)

##### Getting the states

- [case available](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/available)
- [case presenting](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/presenting)
- [case rendering](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/rendering)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/init(rawvalue:))

#### Synchronizing the drawing operation

- [var frameTiming: LayerRenderer.Frame.Timing](/documentation/compositorservices/layerrenderer/drawable/frametiming)
- [var presentationFrameIndex: CompositorFrameIndex](/documentation/compositorservices/layerrenderer/drawable/presentationframeindex)

#### Retrieving the target

- [var target: LayerRenderer.Drawable.Target](/documentation/compositorservices/layerrenderer/drawable/target-swift.property)
- [LayerRenderer.Drawable.Target](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum)

##### Enumeration Cases

- [case builtIn](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/builtin)
- [case capture](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/capture)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/init(rawvalue:))

#### Creating a drawable

- [init()](/documentation/compositorservices/layerrenderer/drawable/init())

#### Adding a render context

- [LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/rendercontext)

##### Rendering with Metal 4

- [func drawMaskOnStencilAttachment(commandEncoder: any MTL4RenderCommandEncoder, value: UInt8)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/drawmaskonstencilattachment(commandencoder:value:)-7npim)
- [func endEncoding(commandEncoder: any MTL4RenderCommandEncoder)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/endencoding(commandencoder:)-2l6lk)

##### Rendering with Metal

- [func drawMaskOnStencilAttachment(commandEncoder: any MTLRenderCommandEncoder, value: UInt8)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/drawmaskonstencilattachment(commandencoder:value:)-65i67)
- [func endEncoding(commandEncoder: any MTLRenderCommandEncoder)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/endencoding(commandencoder:)-4hx0m)

##### Initializers

- [init()](/documentation/compositorservices/layerrenderer/drawable/rendercontext/init())
- [func addRenderContext(commandBuffer: any MTLCommandBuffer) -> LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/addrendercontext(commandbuffer:))
- [func addRenderContext() -> LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/addrendercontext())

#### Structures

- [LayerRenderer.Drawable.TrackingArea](/documentation/compositorservices/layerrenderer/drawable/trackingarea)

##### Structures

- [LayerRenderer.Drawable.TrackingArea.HoverEffect](/documentation/compositorservices/layerrenderer/drawable/trackingarea/hovereffect)

###### Type Properties

- [static let automatic: LayerRenderer.Drawable.TrackingArea.HoverEffect](/documentation/compositorservices/layerrenderer/drawable/trackingarea/hovereffect/automatic)
- [LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct)

###### Initializers

- [init(UInt64)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/init(_:))
- [init(rawValue: UInt64)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/init(rawvalue:))

###### Type Properties

- [static let invalid: LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/invalid)
- [LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct)

###### Initializers

- [init(UInt16)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/init(_:))
- [init(rawValue: UInt16)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/init(rawvalue:))

###### Type Properties

- [static let invalid: LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/invalid)

##### Initializers

- [init()](/documentation/compositorservices/layerrenderer/drawable/trackingarea/init())

##### Instance Properties

- [var identifier: LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.property)
- [var renderValue: LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.property)

##### Instance Methods

- [func addHoverEffect(LayerRenderer.Drawable.TrackingArea.HoverEffect)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/addhovereffect(_:))

#### Instance Properties

- [var isContentCaptureProtected: Bool](/documentation/compositorservices/layerrenderer/drawable/iscontentcaptureprotected)
- [var trackingAreasTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/trackingareastextures)

#### Instance Methods

- [func addTrackingArea(identifier: LayerRenderer.Drawable.TrackingArea.Identifier) -> LayerRenderer.Drawable.TrackingArea](/documentation/compositorservices/layerrenderer/drawable/addtrackingarea(identifier:))
- [func computeProjection(convention: AxisDirectionConvention, viewIndex: Int) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/drawable/computeprojection(convention:viewindex:))
- [func encodePresent()](/documentation/compositorservices/layerrenderer/drawable/encodepresent())

### Configuring the frame update rate

- [var minimumFrameRepeatCount: Int32](/documentation/compositorservices/layerrenderer/minimumframerepeatcount)

### Defining quality level

- [var renderQuality: LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/renderquality-swift.property)
- [var defaultRenderQuality: LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/capabilities/defaultrenderquality)
- [var maxRenderQuality: LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/configuration-swift.struct/maxrenderquality)
- [Defining layer renderer quality](/documentation/compositorservices/defining-layer-renderer-quality)

### Structures

- [LayerRenderer.RenderQuality](/documentation/compositorservices/layerrenderer/renderquality-swift.struct)

#### Initializers

- [init(Float)](/documentation/compositorservices/layerrenderer/renderquality-swift.struct/init(_:))
- [init(rawValue: Float)](/documentation/compositorservices/layerrenderer/renderquality-swift.struct/init(rawvalue:))

### Instance Properties

- [var commandQueue: any MTL4CommandQueue](/documentation/compositorservices/layerrenderer/commandqueue)
- [var onSpatialEvent: (SpatialEventCollection) -> Void](/documentation/compositorservices/layerrenderer/onspatialevent-2jg60)
- [var onSpatialEvent: (SpatialEventCollection) -> Void](/documentation/compositorservices/layerrenderer/onspatialevent-inq8)
- [LayerRenderer.Frame](/documentation/compositorservices/layerrenderer/frame)

### Getting timing information

- [func predictTiming() -> LayerRenderer.Frame.Timing?](/documentation/compositorservices/layerrenderer/frame/predicttiming())
- [LayerRenderer.Frame.Timing](/documentation/compositorservices/layerrenderer/frame/timing)

#### Updating the frame contents

- [var optimalInputTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/optimalinputtime)

#### Rendering the frame

- [var renderingDeadline: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/renderingdeadline)

#### Displaying the frame

- [var presentationTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/presentationtime)

#### Creating the timing details

- [init()](/documentation/compositorservices/layerrenderer/frame/timing/init())

#### Instance Properties

- [var trackableAnchorTime: LayerRenderer.Clock.Instant](/documentation/compositorservices/layerrenderer/frame/timing/trackableanchortime)

### Reporting frame update times

- [func startUpdate()](/documentation/compositorservices/layerrenderer/frame/startupdate())
- [func endUpdate()](/documentation/compositorservices/layerrenderer/frame/endupdate())

### Getting the drawable environment

- [func queryDrawables() -> [LayerRenderer.Drawable]](/documentation/compositorservices/layerrenderer/frame/querydrawables())
- [func queryDrawable() -> LayerRenderer.Drawable?](/documentation/compositorservices/layerrenderer/frame/querydrawable())

### Reporting frame submission times

- [func startSubmission()](/documentation/compositorservices/layerrenderer/frame/startsubmission())
- [func endSubmission()](/documentation/compositorservices/layerrenderer/frame/endsubmission())

### Getting frame-related details

- [var frameIndex: LayerFrameIndex](/documentation/compositorservices/layerrenderer/frame/frameindex)
- [LayerFrameIndex](/documentation/compositorservices/layerframeindex)
- [CompositorFrameIndex](/documentation/compositorservices/compositorframeindex)

### Creating a frame

- [init()](/documentation/compositorservices/layerrenderer/frame/init())

### Instance Methods

- [func binocularFrustumMatrix(convention: AxisDirectionConvention, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/binocularfrustummatrix(convention:increasetangents:depthrange:))
- [func binocularFrustumMatrixForDrawableTarget(drawableTarget: LayerRenderer.Drawable.Target, convention: AxisDirectionConvention, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/binocularfrustummatrixfordrawabletarget(drawabletarget:convention:increasetangents:depthrange:))
- [func drawableTargetViewCount(target: LayerRenderer.Drawable.Target) -> Int](/documentation/compositorservices/layerrenderer/frame/drawabletargetviewcount(target:))
- [func monocularFrustumMatrix(convention: AxisDirectionConvention, viewIndex: Int, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/monocularfrustummatrix(convention:viewindex:increasetangents:depthrange:))
- [func monocularFrustumMatrixForDrawableTarget(drawableTarget: LayerRenderer.Drawable.Target, convention: AxisDirectionConvention, viewIndex: Int, increaseTangents: SIMD4<Float>, depthRange: SIMD2<Float>) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/frame/monocularfrustummatrixfordrawabletarget(drawabletarget:convention:viewindex:increasetangents:depthrange:))

## Drawing environment

- [LayerRenderer.Drawable](/documentation/compositorservices/layerrenderer/drawable)

### Getting the views

- [var views: [LayerRenderer.Drawable.View]](/documentation/compositorservices/layerrenderer/drawable/views)
- [LayerRenderer.Drawable.View](/documentation/compositorservices/layerrenderer/drawable/view)

#### Getting the view’s texture map

- [var textureMap: LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.property)
- [LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct)

##### Getting the viewport

- [var viewport: MTLViewport](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/viewport)

##### Getting the texture indices

- [var sliceIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/sliceindex)
- [var textureIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/textureindex)

##### Creating a texture map

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/init())

#### Getting the transformations

- [var transform: simd_float4x4](/documentation/compositorservices/layerrenderer/drawable/view/transform)
- [var tangents: simd_float4](/documentation/compositorservices/layerrenderer/drawable/view/tangents)

#### Creating a view

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/init())

### Accessing the device orientation

- [var deviceAnchor: DeviceAnchor?](/documentation/compositorservices/layerrenderer/drawable/deviceanchor)

### Getting the render textures

- [var colorTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/colortextures)
- [var depthTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/depthtextures)

### Enqueueing a command buffer

- [func encodePresent(commandBuffer: any MTLCommandBuffer)](/documentation/compositorservices/layerrenderer/drawable/encodepresent(commandbuffer:))

### Getting the rasterization rate map

- [var rasterizationRateMaps: [any MTLRasterizationRateMap]](/documentation/compositorservices/layerrenderer/drawable/rasterizationratemaps)
- [var flippedRasterizationRateMaps: [any MTLRasterizationRateMap]](/documentation/compositorservices/layerrenderer/drawable/flippedrasterizationratemaps)

### Getting the projection matrix

- [AxisDirectionConvention](/documentation/compositorservices/axisdirectionconvention)

#### Getting the axis directions

- [case rightUpBack](/documentation/compositorservices/axisdirectionconvention/rightupback)
- [case rightUpForward](/documentation/compositorservices/axisdirectionconvention/rightupforward)
- [case rightDownBack](/documentation/compositorservices/axisdirectionconvention/rightdownback)
- [case rightDownForward](/documentation/compositorservices/axisdirectionconvention/rightdownforward)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/compositorservices/axisdirectionconvention/init(rawvalue:))

### Accessing pixel depth information

- [var depthRange: simd_float2](/documentation/compositorservices/layerrenderer/drawable/depthrange)

### Managing the state machine

- [var state: LayerRenderer.Drawable.State](/documentation/compositorservices/layerrenderer/drawable/state-swift.property)
- [LayerRenderer.Drawable.State](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum)

#### Getting the states

- [case available](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/available)
- [case presenting](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/presenting)
- [case rendering](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/rendering)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/drawable/state-swift.enum/init(rawvalue:))

### Synchronizing the drawing operation

- [var frameTiming: LayerRenderer.Frame.Timing](/documentation/compositorservices/layerrenderer/drawable/frametiming)
- [var presentationFrameIndex: CompositorFrameIndex](/documentation/compositorservices/layerrenderer/drawable/presentationframeindex)

### Retrieving the target

- [var target: LayerRenderer.Drawable.Target](/documentation/compositorservices/layerrenderer/drawable/target-swift.property)
- [LayerRenderer.Drawable.Target](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum)

#### Enumeration Cases

- [case builtIn](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/builtin)
- [case capture](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/capture)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/compositorservices/layerrenderer/drawable/target-swift.enum/init(rawvalue:))

### Creating a drawable

- [init()](/documentation/compositorservices/layerrenderer/drawable/init())

### Adding a render context

- [LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/rendercontext)

#### Rendering with Metal 4

- [func drawMaskOnStencilAttachment(commandEncoder: any MTL4RenderCommandEncoder, value: UInt8)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/drawmaskonstencilattachment(commandencoder:value:)-7npim)
- [func endEncoding(commandEncoder: any MTL4RenderCommandEncoder)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/endencoding(commandencoder:)-2l6lk)

#### Rendering with Metal

- [func drawMaskOnStencilAttachment(commandEncoder: any MTLRenderCommandEncoder, value: UInt8)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/drawmaskonstencilattachment(commandencoder:value:)-65i67)
- [func endEncoding(commandEncoder: any MTLRenderCommandEncoder)](/documentation/compositorservices/layerrenderer/drawable/rendercontext/endencoding(commandencoder:)-4hx0m)

#### Initializers

- [init()](/documentation/compositorservices/layerrenderer/drawable/rendercontext/init())
- [func addRenderContext(commandBuffer: any MTLCommandBuffer) -> LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/addrendercontext(commandbuffer:))
- [func addRenderContext() -> LayerRenderer.Drawable.RenderContext](/documentation/compositorservices/layerrenderer/drawable/addrendercontext())

### Structures

- [LayerRenderer.Drawable.TrackingArea](/documentation/compositorservices/layerrenderer/drawable/trackingarea)

#### Structures

- [LayerRenderer.Drawable.TrackingArea.HoverEffect](/documentation/compositorservices/layerrenderer/drawable/trackingarea/hovereffect)

##### Type Properties

- [static let automatic: LayerRenderer.Drawable.TrackingArea.HoverEffect](/documentation/compositorservices/layerrenderer/drawable/trackingarea/hovereffect/automatic)
- [LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct)

##### Initializers

- [init(UInt64)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/init(_:))
- [init(rawValue: UInt64)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/init(rawvalue:))

##### Type Properties

- [static let invalid: LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.struct/invalid)
- [LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct)

##### Initializers

- [init(UInt16)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/init(_:))
- [init(rawValue: UInt16)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/init(rawvalue:))

##### Type Properties

- [static let invalid: LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.struct/invalid)

#### Initializers

- [init()](/documentation/compositorservices/layerrenderer/drawable/trackingarea/init())

#### Instance Properties

- [var identifier: LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/compositorservices/layerrenderer/drawable/trackingarea/identifier-swift.property)
- [var renderValue: LayerRenderer.Drawable.TrackingArea.RenderValue](/documentation/compositorservices/layerrenderer/drawable/trackingarea/rendervalue-swift.property)

#### Instance Methods

- [func addHoverEffect(LayerRenderer.Drawable.TrackingArea.HoverEffect)](/documentation/compositorservices/layerrenderer/drawable/trackingarea/addhovereffect(_:))

### Instance Properties

- [var isContentCaptureProtected: Bool](/documentation/compositorservices/layerrenderer/drawable/iscontentcaptureprotected)
- [var trackingAreasTextures: [any MTLTexture]](/documentation/compositorservices/layerrenderer/drawable/trackingareastextures)

### Instance Methods

- [func addTrackingArea(identifier: LayerRenderer.Drawable.TrackingArea.Identifier) -> LayerRenderer.Drawable.TrackingArea](/documentation/compositorservices/layerrenderer/drawable/addtrackingarea(identifier:))
- [func computeProjection(convention: AxisDirectionConvention, viewIndex: Int) -> matrix_float4x4](/documentation/compositorservices/layerrenderer/drawable/computeprojection(convention:viewindex:))
- [func encodePresent()](/documentation/compositorservices/layerrenderer/drawable/encodepresent())
- [LayerRenderer.Drawable.View](/documentation/compositorservices/layerrenderer/drawable/view)

### Getting the view’s texture map

- [var textureMap: LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.property)
- [LayerRenderer.Drawable.View.TextureMap](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct)

#### Getting the viewport

- [var viewport: MTLViewport](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/viewport)

#### Getting the texture indices

- [var sliceIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/sliceindex)
- [var textureIndex: Int](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/textureindex)

#### Creating a texture map

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/texturemap-swift.struct/init())

### Getting the transformations

- [var transform: simd_float4x4](/documentation/compositorservices/layerrenderer/drawable/view/transform)
- [var tangents: simd_float4](/documentation/compositorservices/layerrenderer/drawable/view/tangents)

### Creating a view

- [init()](/documentation/compositorservices/layerrenderer/drawable/view/init())

## Errors

- [LayerRendererConfigurationError](/documentation/compositorservices/layerrendererconfigurationerror)

### Getting the configuration errors

- [case layoutNotSupported](/documentation/compositorservices/layerrendererconfigurationerror/layoutnotsupported)
- [case missingConfiguration](/documentation/compositorservices/layerrendererconfigurationerror/missingconfiguration)
- [case notEnoughFramesRequested](/documentation/compositorservices/layerrendererconfigurationerror/notenoughframesrequested)
- [case temporalAntiAliasingNotSupported](/documentation/compositorservices/layerrendererconfigurationerror/temporalantialiasingnotsupported)
- [case tooManyFramesRequested](/documentation/compositorservices/layerrendererconfigurationerror/toomanyframesrequested)
- [case unsupportedForwardDepthRange](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedforwarddepthrange)
- [case unsupportedNearPlaneDistance](/documentation/compositorservices/layerrendererconfigurationerror/unsupportednearplanedistance)
- [case variableRasterizationRateIsNotSupported](/documentation/compositorservices/layerrendererconfigurationerror/variablerasterizationrateisnotsupported)
- [case unsupportedColorFormat](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedcolorformat)
- [case unsupportedColorUsage](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedcolorusage)
- [case unsupportedDepthFormat](/documentation/compositorservices/layerrendererconfigurationerror/unsupporteddepthformat)
- [case unsupportedDepthUsage](/documentation/compositorservices/layerrendererconfigurationerror/unsupporteddepthusage)
- [case unsupportedDrawableRenderContextStencilFormat](/documentation/compositorservices/layerrendererconfigurationerror/unsupporteddrawablerendercontextstencilformat)
- [case unsupportedRenderQuality](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedrenderquality)

### Getting the error details

- [var description: String](/documentation/compositorservices/layerrendererconfigurationerror/description)

### Enumeration Cases

- [case unsupportedTrackingAreasFormat](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedtrackingareasformat)
- [case unsupportedTrackingAreasUsage](/documentation/compositorservices/layerrendererconfigurationerror/unsupportedtrackingareasusage)

## Articles

- [CompositorServices Functions](/documentation/compositorservices/compositorservices-functions)

### Functions

- [Controlling Metal rendering immersion level](/documentation/compositorservices/controlling-metal-rendering-immersion-level)

## Structures

- [TextureTopology](/documentation/compositorservices/texturetopology)

### Getting the topology type

- [var textureType: MTLTextureType](/documentation/compositorservices/texturetopology/texturetype)

### Getting the array length

- [var arrayLength: UInt64](/documentation/compositorservices/texturetopology/arraylength)

### Creating a topology

- [init()](/documentation/compositorservices/texturetopology/init())

## Type Aliases

- [cp_drawable_array_t](/documentation/compositorservices/cp_drawable_array_t)
- [cp_hover_effect_t](/documentation/compositorservices/cp_hover_effect_t)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
