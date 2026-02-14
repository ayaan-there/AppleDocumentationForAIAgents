# MetalKit Documentation

Source: https://sosumi.ai/documentation/metalkit

---
title: MetalKit
source: https://developer.apple.com/documentation/metalkit
timestamp: 2026-02-13T18:59:43.211Z
---

## View Management

- [MTKView](/documentation/metalkit/mtkview)

### Creating a View

- [init(coder: NSCoder)](/documentation/metalkit/mtkview/init(coder:))
- [init(frame: CGRect, device: (any MTLDevice)?)](/documentation/metalkit/mtkview/init(frame:device:))

### Configuring the Delegate

- [var delegate: (any MTKViewDelegate)?](/documentation/metalkit/mtkview/delegate)

### Configuring the Metal Device

- [var device: (any MTLDevice)?](/documentation/metalkit/mtkview/device)
- [var preferredDevice: (any MTLDevice)?](/documentation/metalkit/mtkview/preferreddevice)

### Configuring the Color Render Target

- [var colorPixelFormat: MTLPixelFormat](/documentation/metalkit/mtkview/colorpixelformat)
- [var colorspace: CGColorSpace?](/documentation/metalkit/mtkview/colorspace)
- [var framebufferOnly: Bool](/documentation/metalkit/mtkview/framebufferonly)
- [var drawableSize: CGSize](/documentation/metalkit/mtkview/drawablesize)
- [var preferredDrawableSize: CGSize](/documentation/metalkit/mtkview/preferreddrawablesize)
- [var autoResizeDrawable: Bool](/documentation/metalkit/mtkview/autoresizedrawable)
- [var clearColor: MTLClearColor](/documentation/metalkit/mtkview/clearcolor)

### Configuring the Render Target Properties

- [var depthStencilPixelFormat: MTLPixelFormat](/documentation/metalkit/mtkview/depthstencilpixelformat)
- [var depthStencilAttachmentTextureUsage: MTLTextureUsage](/documentation/metalkit/mtkview/depthstencilattachmenttextureusage)
- [var clearDepth: Double](/documentation/metalkit/mtkview/cleardepth)
- [var clearStencil: UInt32](/documentation/metalkit/mtkview/clearstencil)

### Configuring Multisampling

- [var sampleCount: Int](/documentation/metalkit/mtkview/samplecount)
- [var multisampleColorAttachmentTextureUsage: MTLTextureUsage](/documentation/metalkit/mtkview/multisamplecolorattachmenttextureusage)

### Retrieving Render Target Information

- [var currentRenderPassDescriptor: MTLRenderPassDescriptor?](/documentation/metalkit/mtkview/currentrenderpassdescriptor)
- [var currentDrawable: (any CAMetalDrawable)?](/documentation/metalkit/mtkview/currentdrawable)
- [var depthStencilTexture: (any MTLTexture)?](/documentation/metalkit/mtkview/depthstenciltexture)
- [var depthStencilStorageMode: MTLStorageMode](/documentation/metalkit/mtkview/depthstencilstoragemode)
- [var multisampleColorTexture: (any MTLTexture)?](/documentation/metalkit/mtkview/multisamplecolortexture)

### Configuring Drawing Behavior

- [var preferredFramesPerSecond: Int](/documentation/metalkit/mtkview/preferredframespersecond)
- [var isPaused: Bool](/documentation/metalkit/mtkview/ispaused)
- [var enableSetNeedsDisplay: Bool](/documentation/metalkit/mtkview/enablesetneedsdisplay)
- [func draw()](/documentation/metalkit/mtkview/draw())
- [var presentsWithTransaction: Bool](/documentation/metalkit/mtkview/presentswithtransaction)

### Releasing Memory

- [func releaseDrawables()](/documentation/metalkit/mtkview/releasedrawables())

### Instance Properties

- [var currentMTL4RenderPassDescriptor: MTL4RenderPassDescriptor?](/documentation/metalkit/mtkview/currentmtl4renderpassdescriptor)
- [MTKViewDelegate](/documentation/metalkit/mtkviewdelegate)

### Changing the View’s Layout

- [func mtkView(MTKView, drawableSizeWillChange: CGSize)](/documentation/metalkit/mtkviewdelegate/mtkview(_:drawablesizewillchange:))

### Drawing the View’s Contents

- [func draw(in: MTKView)](/documentation/metalkit/mtkviewdelegate/draw(in:))

## Texture Loading

- [MTKTextureLoader](/documentation/metalkit/mtktextureloader)

### Creating a Texture Loader

- [init(device: any MTLDevice)](/documentation/metalkit/mtktextureloader/init(device:))
- [var device: any MTLDevice](/documentation/metalkit/mtktextureloader/device)

### Loading Textures from URLs

- [func newTexture(URL: URL, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(url:options:))
- [func newTexture(URL: URL, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(url:options:completionhandler:))
- [func newTextures(URLs: [URL], options: [MTKTextureLoader.Option : Any]?, error: NSErrorPointer) -> [any MTLTexture]](/documentation/metalkit/mtktextureloader/newtextures(urls:options:error:))
- [func newTextures(URLs: [URL], options: [MTKTextureLoader.Option : Any]?, completionHandler: ([any MTLTexture], (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtextures(urls:options:completionhandler:))

### Loading Textures from Asset Catalogs

- [func newTexture(name: String, scaleFactor: CGFloat, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(name:scalefactor:bundle:options:))
- [func newTexture(name: String, scaleFactor: CGFloat, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(name:scalefactor:bundle:options:completionhandler:))
- [func newTextures(names: [String], scaleFactor: CGFloat, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?, completionHandler: ([any MTLTexture], (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtextures(names:scalefactor:bundle:options:completionhandler:))
- [func newTexture(name: String, scaleFactor: CGFloat, displayGamut: NSDisplayGamut, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(name:scalefactor:displaygamut:bundle:options:))
- [func newTexture(name: String, scaleFactor: CGFloat, displayGamut: NSDisplayGamut, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(name:scalefactor:displaygamut:bundle:options:completionhandler:))
- [func newTextures(names: [String], scaleFactor: CGFloat, displayGamut: NSDisplayGamut, bundle: Bundle?, options: [MTKTextureLoader.Option : Any]?, completionHandler: ([any MTLTexture], (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtextures(names:scalefactor:displaygamut:bundle:options:completionhandler:))

### Loading Textures from Core Graphics Images

- [func newTexture(cgImage: CGImage, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(cgimage:options:))
- [func newTexture(cgImage: CGImage, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(cgimage:options:completionhandler:))

### Loading Textures from In-Memory Data Representations

- [func newTexture(data: Data, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(data:options:))
- [func newTexture(data: Data, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(data:options:completionhandler:))

### Loading Textures from Model I/O Representations

- [func newTexture(texture: MDLTexture, options: [MTKTextureLoader.Option : Any]?) throws -> any MTLTexture](/documentation/metalkit/mtktextureloader/newtexture(texture:options:))
- [func newTexture(texture: MDLTexture, options: [MTKTextureLoader.Option : Any]?, completionHandler: ((any MTLTexture)?, (any Error)?) -> Void)](/documentation/metalkit/mtktextureloader/newtexture(texture:options:completionhandler:))

### Specifying Loading Options

- [MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option)

#### Creating Texture Loading Options

- [init(rawValue: String)](/documentation/metalkit/mtktextureloader/option/init(rawvalue:))

#### Specifying Mipmap Options

- [static let allocateMipmaps: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/allocatemipmaps)
- [static let generateMipmaps: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/generatemipmaps)

#### Specifying Resource Options

- [static let textureCPUCacheMode: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/texturecpucachemode)
- [static let textureStorageMode: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/texturestoragemode)
- [static let textureUsage: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/textureusage)

#### Specifying Origin Information

- [static let origin: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/origin)
- [MTKTextureLoader.Origin](/documentation/metalkit/mtktextureloader/origin)

##### Creating Texture Origin Options

- [init(rawValue: String)](/documentation/metalkit/mtktextureloader/origin/init(rawvalue:))

##### Specifying Texture Origin Options

- [static let topLeft: MTKTextureLoader.Origin](/documentation/metalkit/mtktextureloader/origin/topleft)
- [static let bottomLeft: MTKTextureLoader.Origin](/documentation/metalkit/mtktextureloader/origin/bottomleft)
- [static let flippedVertically: MTKTextureLoader.Origin](/documentation/metalkit/mtktextureloader/origin/flippedvertically)

#### Specifying Cube Layout

- [static let cubeLayout: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/cubelayout)
- [MTKTextureLoader.CubeLayout](/documentation/metalkit/mtktextureloader/cubelayout)

##### Creating Cube Texture Layout Options

- [init(rawValue: String)](/documentation/metalkit/mtktextureloader/cubelayout/init(rawvalue:))

##### Specifying Cube Texture Layout Options

- [static let vertical: MTKTextureLoader.CubeLayout](/documentation/metalkit/mtktextureloader/cubelayout/vertical)

#### Specifying sRGB Options

- [static let SRGB: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/srgb)

#### Type Properties

- [static let loadAsArray: MTKTextureLoader.Option](/documentation/metalkit/mtktextureloader/option/loadasarray)

### Completing a Texture Loading Operation

- [MTKTextureLoader.ArrayCallback](/documentation/metalkit/mtktextureloader/arraycallback)
- [MTKTextureLoader.Callback](/documentation/metalkit/mtktextureloader/callback)

### Handling Errors

- [MTKTextureLoader.Error](/documentation/metalkit/mtktextureloader/error)

#### Initializers

- [init(rawValue: String)](/documentation/metalkit/mtktextureloader/error/init(rawvalue:))

#### Keys

- [static let domain: MTKTextureLoader.Error](/documentation/metalkit/mtktextureloader/error/domain)
- [static let key: MTKTextureLoader.Error](/documentation/metalkit/mtktextureloader/error/key)

## Model Handling

- [MTKMesh](/documentation/metalkit/mtkmesh)

### Initialization

- [init(mesh: MDLMesh, device: any MTLDevice) throws](/documentation/metalkit/mtkmesh/init(mesh:device:))

### Loading Meshes from an Asset

- [class func newMeshes(asset: MDLAsset, device: any MTLDevice) throws -> (modelIOMeshes: [MDLMesh], metalKitMeshes: [MTKMesh])](/documentation/metalkit/mtkmesh/newmeshes(asset:device:))

### Submeshes

- [var submeshes: [MTKSubmesh]](/documentation/metalkit/mtkmesh/submeshes)

### Vertex Properties

- [var vertexBuffers: [MTKMeshBuffer]](/documentation/metalkit/mtkmesh/vertexbuffers)
- [var vertexCount: Int](/documentation/metalkit/mtkmesh/vertexcount)
- [var vertexDescriptor: MDLVertexDescriptor](/documentation/metalkit/mtkmesh/vertexdescriptor)

### Identifying Properties

- [var name: String](/documentation/metalkit/mtkmesh/name)

### Constants

- [Mesh Error Handling](/documentation/metalkit/mesh-error-handling)

#### Constants

- [static let domain: MTKModelError](/documentation/metalkit/mtkmodelerror/domain)
- [static let key: MTKModelError](/documentation/metalkit/mtkmodelerror/key)
- [MTKMeshBuffer](/documentation/metalkit/mtkmeshbuffer)

### Originating Objects

- [var allocator: MTKMeshBufferAllocator](/documentation/metalkit/mtkmeshbuffer/allocator)
- [var type: MDLMeshBufferType](/documentation/metalkit/mtkmeshbuffer/type)

### Metal Buffer Properties

- [var buffer: any MTLBuffer](/documentation/metalkit/mtkmeshbuffer/buffer)
- [var length: Int](/documentation/metalkit/mtkmeshbuffer/length)
- [var offset: Int](/documentation/metalkit/mtkmeshbuffer/offset)

### Instance Methods

- [func zone() -> (any MDLMeshBufferZone)?](/documentation/metalkit/mtkmeshbuffer/zone())
- [MTKMeshBufferAllocator](/documentation/metalkit/mtkmeshbufferallocator)

### Initialization

- [init(device: any MTLDevice)](/documentation/metalkit/mtkmeshbufferallocator/init(device:))

### Device

- [var device: any MTLDevice](/documentation/metalkit/mtkmeshbufferallocator/device)
- [MTKSubmesh](/documentation/metalkit/mtksubmesh)

### Parent Mesh

- [var mesh: MTKMesh?](/documentation/metalkit/mtksubmesh/mesh)

### Properties used to Draw Indexed Primitives

- [var indexBuffer: MTKMeshBuffer](/documentation/metalkit/mtksubmesh/indexbuffer)
- [var indexCount: Int](/documentation/metalkit/mtksubmesh/indexcount)
- [var indexType: MTLIndexType](/documentation/metalkit/mtksubmesh/indextype)
- [var primitiveType: MTLPrimitiveType](/documentation/metalkit/mtksubmesh/primitivetype)

### Identifying Properties

- [var name: String](/documentation/metalkit/mtksubmesh/name)
- [Conversion Functions](/documentation/metalkit/conversion-functions)

### Converting Between Model I/O and Metal Vertex Descriptors

- [func MTKMetalVertexDescriptorFromModelIO(MDLVertexDescriptor) -> MTLVertexDescriptor?](/documentation/metalkit/mtkmetalvertexdescriptorfrommodelio(_:))
- [func MTKModelIOVertexDescriptorFromMetal(MTLVertexDescriptor) -> MDLVertexDescriptor](/documentation/metalkit/mtkmodeliovertexdescriptorfrommetal(_:))

### Converting Between Model I/O and Metal Vertex Formats

- [func MTKMetalVertexFormatFromModelIO(MDLVertexFormat) -> MTLVertexFormat](/documentation/metalkit/mtkmetalvertexformatfrommodelio(_:))
- [func MTKModelIOVertexFormatFromMetal(MTLVertexFormat) -> MDLVertexFormat](/documentation/metalkit/mtkmodeliovertexformatfrommetal(_:))
- [Model Errors](/documentation/metalkit/model-errors)

### Error Handling

- [MTKModelError](/documentation/metalkit/mtkmodelerror)

#### Initializing a Raw Constant

- [init(rawValue: String)](/documentation/metalkit/mtkmodelerror/init(rawvalue:))

#### Finding Model Error Constants

- [static let domain: MTKModelError](/documentation/metalkit/mtkmodelerror/domain)
- [static let key: MTKModelError](/documentation/metalkit/mtkmodelerror/key)

## Reference

- [MetalKit Functions](/documentation/metalkit/metalkit-functions)

### Functions

- [func MTKMetalVertexDescriptorFromModelIOWithError(MDLVertexDescriptor) throws -> MTLVertexDescriptor?](/documentation/metalkit/mtkmetalvertexdescriptorfrommodeliowitherror(_:))
- [func MTKModelIOVertexDescriptorFromMetalWithError(MTLVertexDescriptor) throws -> MDLVertexDescriptor](/documentation/metalkit/mtkmodeliovertexdescriptorfrommetalwitherror(_:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
