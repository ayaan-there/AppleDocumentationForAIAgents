# GLKit Documentation

Source: https://sosumi.ai/documentation/glkit

---
title: GLKit
source: https://developer.apple.com/documentation/glkit
timestamp: 2026-02-13T18:57:40.462Z
---

## Texture Loading

- [GLKTextureInfo](/documentation/glkit/glktextureinfo)

### Reading Texture Information

- [var name: GLuint](/documentation/glkit/glktextureinfo/name-swift.property)
- [var target: GLenum](/documentation/glkit/glktextureinfo/target-swift.property)
- [var height: GLuint](/documentation/glkit/glktextureinfo/height-swift.property)
- [var width: GLuint](/documentation/glkit/glktextureinfo/width-swift.property)
- [var textureOrigin: GLKTextureInfoOrigin](/documentation/glkit/glktextureinfo/textureorigin-swift.property)
- [var alphaState: GLKTextureInfoAlphaState](/documentation/glkit/glktextureinfo/alphastate-swift.property)
- [var containsMipmaps: Bool](/documentation/glkit/glktextureinfo/containsmipmaps-swift.property)

### Constants

- [GLKTextureInfoAlphaState](/documentation/glkit/glktextureinfoalphastate)

#### Constants

- [case none](/documentation/glkit/glktextureinfoalphastate/none)
- [case nonPremultiplied](/documentation/glkit/glktextureinfoalphastate/nonpremultiplied)
- [case premultiplied](/documentation/glkit/glktextureinfoalphastate/premultiplied)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureinfoalphastate/init(rawvalue:))
- [GLKTextureInfoOrigin](/documentation/glkit/glktextureinfoorigin)

#### Constants

- [case unknown](/documentation/glkit/glktextureinfoorigin/unknown)
- [case topLeft](/documentation/glkit/glktextureinfoorigin/topleft)
- [case bottomLeft](/documentation/glkit/glktextureinfoorigin/bottomleft)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureinfoorigin/init(rawvalue:))

### Instance Properties

- [var arrayLength: GLuint](/documentation/glkit/glktextureinfo/arraylength-swift.property)
- [var depth: GLuint](/documentation/glkit/glktextureinfo/depth-swift.property)
- [var mimapLevelCount: GLuint](/documentation/glkit/glktextureinfo/mimaplevelcount-swift.property)
- [GLKTextureLoader](/documentation/glkit/glktextureloader)

### Initialization

- [init(sharegroup: EAGLSharegroup)](/documentation/glkit/glktextureloader/init(sharegroup:))
- [init(share: NSOpenGLContext)](/documentation/glkit/glktextureloader/init(share:))

### Loading Textures from Files

- [class func texture(withContentsOfFile: String, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/texture(withcontentsoffile:options:))
- [func texture(withContentsOfFile: String, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/texture(withcontentsoffile:options:queue:completionhandler:))

### Loading a Texture From a URL

- [class func texture(withContentsOf: URL, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/texture(withcontentsof:options:)-708ft)
- [func texture(withContentsOf: URL, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/texture(withcontentsof:options:queue:completionhandler:)-55187)

### Creating Textures from In-Memory Representations

- [class func texture(withContentsOf: Data, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/texture(withcontentsof:options:)-2ljxb)
- [func texture(withContentsOf: Data, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/texture(withcontentsof:options:queue:completionhandler:)-6n0cf)

### Creating Textures from CGImages

- [class func texture(with: CGImage, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/texture(with:options:))
- [func texture(with: CGImage, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/texture(with:options:queue:completionhandler:))

### Loading Cube Maps from Files

- [class func cubeMap(withContentsOfFile: String, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/cubemap(withcontentsoffile:options:))
- [func cubeMap(withContentsOfFile: String, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/cubemap(withcontentsoffile:options:queue:completionhandler:))
- [class func cubeMap(withContentsOfFiles: [Any], options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/cubemap(withcontentsoffiles:options:))

#### Related Documentation

- [func cubeMap(withContentsOf: URL, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/cubemap(withcontentsof:options:queue:completionhandler:))
- [func cubeMap(withContentsOfFiles: [Any], options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/cubemap(withcontentsoffiles:options:queue:completionhandler:))

### Loading Cube Maps from URLs

- [class func cubeMap(withContentsOf: URL, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/cubemap(withcontentsof:options:))
- [func cubeMap(withContentsOf: URL, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/cubemap(withcontentsof:options:queue:completionhandler:))

### Constants

- [GLKTextureLoaderCallback](/documentation/glkit/glktextureloadercallback)
- [Texture Loading Options](/documentation/glkit/texture-loading-options)

#### Constants

- [let GLKTextureLoaderApplyPremultiplication: String](/documentation/glkit/glktextureloaderapplypremultiplication)
- [let GLKTextureLoaderGenerateMipmaps: String](/documentation/glkit/glktextureloadergeneratemipmaps)
- [let GLKTextureLoaderOriginBottomLeft: String](/documentation/glkit/glktextureloaderoriginbottomleft)
- [let GLKTextureLoaderGrayscaleAsAlpha: String](/documentation/glkit/glktextureloadergrayscaleasalpha)
- [let GLKTextureLoaderSRGB: String](/documentation/glkit/glktextureloadersrgb)
- [Texture Error Handling](/documentation/glkit/texture-error-handling)

#### Constants

- [let GLKTextureLoaderErrorDomain: String](/documentation/glkit/glktextureloadererrordomain)
- [let GLKTextureLoaderErrorKey: String](/documentation/glkit/glktextureloadererrorkey)
- [let GLKTextureLoaderGLErrorKey: String](/documentation/glkit/glktextureloaderglerrorkey)
- [GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/code)

#### Initializers

- [init?(rawValue: GLuint)](/documentation/glkit/glktextureloadererror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [case alphaPremultiplicationFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/alphapremultiplicationfailure)
- [case compressedTextureUpload](/documentation/glkit/glktextureloadererror-swift.struct/code/compressedtextureupload)
- [case cubeMapInvalidNumFiles](/documentation/glkit/glktextureloadererror-swift.struct/code/cubemapinvalidnumfiles)
- [case dataPreprocessingFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/datapreprocessingfailure)
- [case fileOrURLNotFound](/documentation/glkit/glktextureloadererror-swift.struct/code/fileorurlnotfound)
- [case incompatibleFormatSRGB](/documentation/glkit/glktextureloadererror-swift.struct/code/incompatibleformatsrgb)
- [case invalidCGImage](/documentation/glkit/glktextureloadererror-swift.struct/code/invalidcgimage)
- [case invalidEAGLContext](/documentation/glkit/glktextureloadererror-swift.struct/code/invalideaglcontext)
- [case invalidNSData](/documentation/glkit/glktextureloadererror-swift.struct/code/invalidnsdata)
- [case mipmapUnsupported](/documentation/glkit/glktextureloadererror-swift.struct/code/mipmapunsupported)
- [case pvrAtlasUnsupported](/documentation/glkit/glktextureloadererror-swift.struct/code/pvratlasunsupported)
- [case reorientationFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/reorientationfailure)
- [case uncompressedTextureUpload](/documentation/glkit/glktextureloadererror-swift.struct/code/uncompressedtextureupload)
- [case unknownFileType](/documentation/glkit/glktextureloadererror-swift.struct/code/unknownfiletype)
- [case unknownPathType](/documentation/glkit/glktextureloadererror-swift.struct/code/unknownpathtype)
- [case unsupportedBitDepth](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedbitdepth)
- [case unsupportedCubeMapDimensions](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedcubemapdimensions)
- [case unsupportedOrientation](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedorientation)
- [case unsupportedPVRFormat](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedpvrformat)
- [case unsupportedTextureTarget](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedtexturetarget)

### Instance Methods

- [func texture(withName: String, scaleFactor: CGFloat, bundle: Bundle?, options: [String : NSNumber]?, queue: dispatch_queue_t?, completionHandler: (GLKTextureInfo?, (any Error)?) -> Void)](/documentation/glkit/glktextureloader/texture(withname:scalefactor:bundle:options:queue:completionhandler:))

### Type Methods

- [class func texture(withName: String, scaleFactor: CGFloat, bundle: Bundle?, options: [String : NSNumber]?) throws -> GLKTextureInfo](/documentation/glkit/glktextureloader/texture(withname:scalefactor:bundle:options:))

## OpenGL ES View Rendering

- [GLKView](/documentation/glkit/glkview)

### Initializing the View

- [init(frame: CGRect, context: EAGLContext)](/documentation/glkit/glkview/init(frame:context:))

### Delegate

- [var delegate: (any GLKViewDelegate)?](/documentation/glkit/glkview/delegate)

### Configuring the Framebuffer Object

- [var drawableColorFormat: GLKViewDrawableColorFormat](/documentation/glkit/glkview/drawablecolorformat)
- [var drawableDepthFormat: GLKViewDrawableDepthFormat](/documentation/glkit/glkview/drawabledepthformat)
- [var drawableStencilFormat: GLKViewDrawableStencilFormat](/documentation/glkit/glkview/drawablestencilformat)
- [var drawableMultisample: GLKViewDrawableMultisample](/documentation/glkit/glkview/drawablemultisample)

### Read-only Framebuffer Properties

- [var drawableHeight: Int](/documentation/glkit/glkview/drawableheight)
- [var drawableWidth: Int](/documentation/glkit/glkview/drawablewidth)

### Drawing Your View’s Contents

- [var context: EAGLContext](/documentation/glkit/glkview/context)
- [func bindDrawable()](/documentation/glkit/glkview/binddrawable())
- [var enableSetNeedsDisplay: Bool](/documentation/glkit/glkview/enablesetneedsdisplay)
- [func display()](/documentation/glkit/glkview/display())
- [var snapshot: UIImage](/documentation/glkit/glkview/snapshot)

### Deleting the View’s Underlying Framebuffer Object

- [func deleteDrawable()](/documentation/glkit/glkview/deletedrawable())

### Constants

- [GLKViewDrawableColorFormat](/documentation/glkit/glkviewdrawablecolorformat)

#### Constants

- [case RGBA8888](/documentation/glkit/glkviewdrawablecolorformat/rgba8888)
- [case RGB565](/documentation/glkit/glkviewdrawablecolorformat/rgb565)
- [case SRGBA8888](/documentation/glkit/glkviewdrawablecolorformat/srgba8888)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablecolorformat/init(rawvalue:))
- [GLKViewDrawableDepthFormat](/documentation/glkit/glkviewdrawabledepthformat)

#### Constants

- [case formatNone](/documentation/glkit/glkviewdrawabledepthformat/formatnone)
- [case format16](/documentation/glkit/glkviewdrawabledepthformat/format16)
- [case format24](/documentation/glkit/glkviewdrawabledepthformat/format24)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawabledepthformat/init(rawvalue:))
- [GLKViewDrawableStencilFormat](/documentation/glkit/glkviewdrawablestencilformat)

#### Constants

- [case formatNone](/documentation/glkit/glkviewdrawablestencilformat/formatnone)
- [case format8](/documentation/glkit/glkviewdrawablestencilformat/format8)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablestencilformat/init(rawvalue:))
- [GLKViewDrawableMultisample](/documentation/glkit/glkviewdrawablemultisample)

#### Constants

- [case multisampleNone](/documentation/glkit/glkviewdrawablemultisample/multisamplenone)
- [case multisample4X](/documentation/glkit/glkviewdrawablemultisample/multisample4x)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablemultisample/init(rawvalue:))
- [GLKViewDelegate](/documentation/glkit/glkviewdelegate)

### Drawing the View’s Contents

- [func glkView(GLKView, drawIn: CGRect)](/documentation/glkit/glkviewdelegate/glkview(_:drawin:))
- [GLKViewController](/documentation/glkit/glkviewcontroller)

### Configuring the Frame rate

- [var preferredFramesPerSecond: Int](/documentation/glkit/glkviewcontroller/preferredframespersecond)
- [var framesPerSecond: Int](/documentation/glkit/glkviewcontroller/framespersecond)

### Configuring the Delegate

- [var delegate: (any GLKViewControllerDelegate)?](/documentation/glkit/glkviewcontroller/delegate)

### Controlling Frame Updates

- [var isPaused: Bool](/documentation/glkit/glkviewcontroller/ispaused)
- [var pauseOnWillResignActive: Bool](/documentation/glkit/glkviewcontroller/pauseonwillresignactive)
- [var resumeOnDidBecomeActive: Bool](/documentation/glkit/glkviewcontroller/resumeondidbecomeactive)

### Obtaining Information About View Updates

- [var framesDisplayed: Int](/documentation/glkit/glkviewcontroller/framesdisplayed)
- [var timeSinceFirstResume: TimeInterval](/documentation/glkit/glkviewcontroller/timesincefirstresume)
- [var timeSinceLastResume: TimeInterval](/documentation/glkit/glkviewcontroller/timesincelastresume)
- [var timeSinceLastUpdate: TimeInterval](/documentation/glkit/glkviewcontroller/timesincelastupdate)
- [var timeSinceLastDraw: TimeInterval](/documentation/glkit/glkviewcontroller/timesincelastdraw)
- [GLKViewControllerDelegate](/documentation/glkit/glkviewcontrollerdelegate)

### Handling an Update Event

- [func glkViewControllerUpdate(GLKViewController)](/documentation/glkit/glkviewcontrollerdelegate/glkviewcontrollerupdate(_:))

### Pause and Resume Notifications

- [func glkViewController(GLKViewController, willPause: Bool)](/documentation/glkit/glkviewcontrollerdelegate/glkviewcontroller(_:willpause:))

## Mesh Data Management

- [GLKMesh](/documentation/glkit/glkmesh)

### Initializers

- [init(mesh: MDLMesh) throws](/documentation/glkit/glkmesh/init(mesh:))

### Instance Properties

- [var name: String](/documentation/glkit/glkmesh/name)
- [var submeshes: [GLKSubmesh]](/documentation/glkit/glkmesh/submeshes)
- [var vertexBuffers: [GLKMeshBuffer]](/documentation/glkit/glkmesh/vertexbuffers)
- [var vertexCount: Int](/documentation/glkit/glkmesh/vertexcount)
- [var vertexDescriptor: MDLVertexDescriptor](/documentation/glkit/glkmesh/vertexdescriptor)

### Type Methods

- [class func newMeshes(from: MDLAsset, sourceMeshes: AutoreleasingUnsafeMutablePointer<NSArray?>?) throws -> [GLKMesh]](/documentation/glkit/glkmesh/newmeshes(from:sourcemeshes:))
- [GLKMeshBuffer](/documentation/glkit/glkmeshbuffer)

### Instance Properties

- [var allocator: GLKMeshBufferAllocator](/documentation/glkit/glkmeshbuffer/allocator)
- [var glBufferName: GLuint](/documentation/glkit/glkmeshbuffer/glbuffername)
- [var length: Int](/documentation/glkit/glkmeshbuffer/length)
- [var offset: Int](/documentation/glkit/glkmeshbuffer/offset)
- [var type: MDLMeshBufferType](/documentation/glkit/glkmeshbuffer/type)

### Instance methods

- [func zone() -> (any MDLMeshBufferZone)?](/documentation/glkit/glkmeshbuffer/zone())
- [GLKMeshBufferAllocator](/documentation/glkit/glkmeshbufferallocator)
- [GLKSubmesh](/documentation/glkit/glksubmesh)

### Instance Properties

- [var elementBuffer: GLKMeshBuffer](/documentation/glkit/glksubmesh/elementbuffer)
- [var elementCount: GLsizei](/documentation/glkit/glksubmesh/elementcount)
- [var mesh: GLKMesh?](/documentation/glkit/glksubmesh/mesh)
- [var mode: GLenum](/documentation/glkit/glksubmesh/mode)
- [var name: String](/documentation/glkit/glksubmesh/name)
- [var type: GLenum](/documentation/glkit/glksubmesh/type)

## Shader-Based Rendering Effects

- [GLKNamedEffect](/documentation/glkit/glknamedeffect)

### Binding the Shader Program

- [func prepareToDraw()](/documentation/glkit/glknamedeffect/preparetodraw())
- [GLKBaseEffect](/documentation/glkit/glkbaseeffect)

### Naming the Effect

- [var label: String?](/documentation/glkit/glkbaseeffect/label)

### Configuring the Modelview Transform

- [var transform: GLKEffectPropertyTransform](/documentation/glkit/glkbaseeffect/transform)

### Configuring Lights

- [var lightingType: GLKLightingType](/documentation/glkit/glkbaseeffect/lightingtype)
- [var lightModelTwoSided: GLboolean](/documentation/glkit/glkbaseeffect/lightmodeltwosided)
- [var material: GLKEffectPropertyMaterial](/documentation/glkit/glkbaseeffect/material)
- [var lightModelAmbientColor: GLKVector4](/documentation/glkit/glkbaseeffect/lightmodelambientcolor)
- [var light0: GLKEffectPropertyLight](/documentation/glkit/glkbaseeffect/light0)
- [var light1: GLKEffectPropertyLight](/documentation/glkit/glkbaseeffect/light1)
- [var light2: GLKEffectPropertyLight](/documentation/glkit/glkbaseeffect/light2)

### Configuring Textures

- [var texture2d0: GLKEffectPropertyTexture](/documentation/glkit/glkbaseeffect/texture2d0)
- [var texture2d1: GLKEffectPropertyTexture](/documentation/glkit/glkbaseeffect/texture2d1)
- [var textureOrder: [GLKEffectPropertyTexture]?](/documentation/glkit/glkbaseeffect/textureorder)

### Configuring Fog

- [var fog: GLKEffectPropertyFog](/documentation/glkit/glkbaseeffect/fog)

### Configuring Color Information

- [var colorMaterialEnabled: GLboolean](/documentation/glkit/glkbaseeffect/colormaterialenabled)
- [var useConstantColor: GLboolean](/documentation/glkit/glkbaseeffect/useconstantcolor)
- [var constantColor: GLKVector4](/documentation/glkit/glkbaseeffect/constantcolor)

### Preparing the Effect for Drawing

- [func prepareToDraw()](/documentation/glkit/glkbaseeffect/preparetodraw())

### Type Aliases

- [GLKEffectPropertyPrvPtr](/documentation/glkit/glkeffectpropertyprvptr)
- [GLKReflectionMapEffect](/documentation/glkit/glkreflectionmapeffect)

### Preparing the Reflection Effect

- [func prepareToDraw()](/documentation/glkit/glkreflectionmapeffect/preparetodraw())

### Effect Properties

- [var textureCubeMap: GLKEffectPropertyTexture](/documentation/glkit/glkreflectionmapeffect/texturecubemap)
- [var matrix: GLKMatrix3](/documentation/glkit/glkreflectionmapeffect/matrix)
- [GLKSkyboxEffect](/documentation/glkit/glkskyboxeffect)

### Naming the Effect

- [var label: String?](/documentation/glkit/glkskyboxeffect/label)

### Preparing the Effect for Rendering

- [func prepareToDraw()](/documentation/glkit/glkskyboxeffect/preparetodraw())

### Drawing the Skybox

- [func draw()](/documentation/glkit/glkskyboxeffect/draw())

### Configuring the Skybox

- [var textureCubeMap: GLKEffectPropertyTexture](/documentation/glkit/glkskyboxeffect/texturecubemap)
- [var center: GLKVector3](/documentation/glkit/glkskyboxeffect/center)
- [var xSize: GLfloat](/documentation/glkit/glkskyboxeffect/xsize)
- [var ySize: GLfloat](/documentation/glkit/glkskyboxeffect/ysize)
- [var zSize: GLfloat](/documentation/glkit/glkskyboxeffect/zsize)

### Setting the Skybox Transform

- [var transform: GLKEffectPropertyTransform](/documentation/glkit/glkskyboxeffect/transform)

## Rendering Effect Parameters

- [GLKEffectProperty](/documentation/glkit/glkeffectproperty)
- [GLKEffectPropertyFog](/documentation/glkit/glkeffectpropertyfog)

### Enabling Fog

- [var enabled: GLboolean](/documentation/glkit/glkeffectpropertyfog/enabled)

### Choosing the Fog Mode

- [var mode: GLint](/documentation/glkit/glkeffectpropertyfog/mode)

#### Related Documentation

- [GLKFogMode](/documentation/glkit/glkfogmode)

##### Constants

- [case exp](/documentation/glkit/glkfogmode/exp)
- [case exp2](/documentation/glkit/glkfogmode/exp2)
- [case linear](/documentation/glkit/glkfogmode/linear)

##### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkfogmode/init(rawvalue:))

### Fog Properties

- [var color: GLKVector4](/documentation/glkit/glkeffectpropertyfog/color)
- [var density: GLfloat](/documentation/glkit/glkeffectpropertyfog/density)
- [var start: GLfloat](/documentation/glkit/glkeffectpropertyfog/start)
- [var end: GLfloat](/documentation/glkit/glkeffectpropertyfog/end)

### Constants

- [GLKFogMode](/documentation/glkit/glkfogmode)

#### Constants

- [case exp](/documentation/glkit/glkfogmode/exp)
- [case exp2](/documentation/glkit/glkfogmode/exp2)
- [case linear](/documentation/glkit/glkfogmode/linear)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkfogmode/init(rawvalue:))
- [GLKEffectPropertyLight](/documentation/glkit/glkeffectpropertylight)

### Configuring Common Lighting Properties

- [var enabled: GLboolean](/documentation/glkit/glkeffectpropertylight/enabled)
- [var position: GLKVector4](/documentation/glkit/glkeffectpropertylight/position)
- [var transform: GLKEffectPropertyTransform](/documentation/glkit/glkeffectpropertylight/transform)

### Configuring Light Colors

- [var ambientColor: GLKVector4](/documentation/glkit/glkeffectpropertylight/ambientcolor)
- [var diffuseColor: GLKVector4](/documentation/glkit/glkeffectpropertylight/diffusecolor)
- [var specularColor: GLKVector4](/documentation/glkit/glkeffectpropertylight/specularcolor)

### Configuring Lighting Attenuation

- [var constantAttenuation: GLfloat](/documentation/glkit/glkeffectpropertylight/constantattenuation)
- [var linearAttenuation: GLfloat](/documentation/glkit/glkeffectpropertylight/linearattenuation)
- [var quadraticAttenuation: GLfloat](/documentation/glkit/glkeffectpropertylight/quadraticattenuation)

### Configuring Spotlight Properties

- [var spotCutoff: GLfloat](/documentation/glkit/glkeffectpropertylight/spotcutoff)
- [var spotDirection: GLKVector3](/documentation/glkit/glkeffectpropertylight/spotdirection)
- [var spotExponent: GLfloat](/documentation/glkit/glkeffectpropertylight/spotexponent)

### Constants

- [GLKLightingType](/documentation/glkit/glklightingtype)

#### Constants

- [case perVertex](/documentation/glkit/glklightingtype/pervertex)
- [case perPixel](/documentation/glkit/glklightingtype/perpixel)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glklightingtype/init(rawvalue:))
- [GLKEffectPropertyTexture](/documentation/glkit/glkeffectpropertytexture)

### Configuring Texture Properties

- [var enabled: GLboolean](/documentation/glkit/glkeffectpropertytexture/enabled)
- [var envMode: GLKTextureEnvMode](/documentation/glkit/glkeffectpropertytexture/envmode)
- [var name: GLuint](/documentation/glkit/glkeffectpropertytexture/name)
- [var target: GLKTextureTarget](/documentation/glkit/glkeffectpropertytexture/target)

### Constants

- [GLKTextureTarget](/documentation/glkit/glktexturetarget)

#### Constants

- [case target2D](/documentation/glkit/glktexturetarget/target2d)
- [case targetCubeMap](/documentation/glkit/glktexturetarget/targetcubemap)
- [case targetCt](/documentation/glkit/glktexturetarget/targetct)

#### Initializers

- [init?(rawValue: GLenum)](/documentation/glkit/glktexturetarget/init(rawvalue:))
- [GLKTextureEnvMode](/documentation/glkit/glktextureenvmode)

#### Constants

- [case replace](/documentation/glkit/glktextureenvmode/replace)
- [case modulate](/documentation/glkit/glktextureenvmode/modulate)
- [case decal](/documentation/glkit/glktextureenvmode/decal)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureenvmode/init(rawvalue:))
- [GLKEffectPropertyMaterial](/documentation/glkit/glkeffectpropertymaterial)

### Material Properties

- [var ambientColor: GLKVector4](/documentation/glkit/glkeffectpropertymaterial/ambientcolor)
- [var diffuseColor: GLKVector4](/documentation/glkit/glkeffectpropertymaterial/diffusecolor)
- [var emissiveColor: GLKVector4](/documentation/glkit/glkeffectpropertymaterial/emissivecolor)
- [var shininess: GLfloat](/documentation/glkit/glkeffectpropertymaterial/shininess)
- [var specularColor: GLKVector4](/documentation/glkit/glkeffectpropertymaterial/specularcolor)
- [GLKEffectPropertyTransform](/documentation/glkit/glkeffectpropertytransform)

### Configuring Modelview Properties

- [var modelviewMatrix: GLKMatrix4](/documentation/glkit/glkeffectpropertytransform/modelviewmatrix)
- [var normalMatrix: GLKMatrix3](/documentation/glkit/glkeffectpropertytransform/normalmatrix)

### Configuring the Projection Matrix

- [var projectionMatrix: GLKMatrix4](/documentation/glkit/glkeffectpropertytransform/projectionmatrix)
- [GLKit Effects Constants](/documentation/glkit/glkit-effects-constants)

### Constants

- [GLKVertexAttrib](/documentation/glkit/glkvertexattrib)

#### Constants

- [case position](/documentation/glkit/glkvertexattrib/position)
- [case normal](/documentation/glkit/glkvertexattrib/normal)
- [case color](/documentation/glkit/glkvertexattrib/color)
- [case texCoord0](/documentation/glkit/glkvertexattrib/texcoord0)
- [case texCoord1](/documentation/glkit/glkvertexattrib/texcoord1)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkvertexattrib/init(rawvalue:))

## Math Utilties

- [GLKMatrixStack](/documentation/glkit/glkmatrixstack)
- [GLKMatrix3](/documentation/glkit/glkmatrix3-pcl)

### Creating Matrices

- [func GLKMatrix3Make(Float, Float, Float, Float, Float, Float, Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3make(_:_:_:_:_:_:_:_:_:))
- [func GLKMatrix3MakeAndTranspose(Float, Float, Float, Float, Float, Float, Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makeandtranspose(_:_:_:_:_:_:_:_:_:))
- [func GLKMatrix3MakeWithArray(UnsafeMutablePointer<Float>!) -> GLKMatrix3](/documentation/glkit/glkmatrix3makewitharray(_:))
- [func GLKMatrix3MakeWithArrayAndTranspose(UnsafeMutablePointer<Float>!) -> GLKMatrix3](/documentation/glkit/glkmatrix3makewitharrayandtranspose(_:))
- [func GLKMatrix3MakeWithColumns(GLKVector3, GLKVector3, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3makewithcolumns(_:_:_:))
- [func GLKMatrix3MakeWithRows(GLKVector3, GLKVector3, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3makewithrows(_:_:_:))
- [func GLKMatrix3MakeRotation(Float, Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makerotation(_:_:_:_:))
- [func GLKMatrix3MakeXRotation(Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makexrotation(_:))
- [func GLKMatrix3MakeYRotation(Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makeyrotation(_:))
- [func GLKMatrix3MakeZRotation(Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makezrotation(_:))
- [func GLKMatrix3MakeWithQuaternion(GLKQuaternion) -> GLKMatrix3](/documentation/glkit/glkmatrix3makewithquaternion(_:))
- [func GLKMatrix3MakeScale(Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3makescale(_:_:_:))

### Working With Parts of a Matrix

- [func GLKMatrix3GetMatrix2(GLKMatrix3) -> GLKMatrix2](/documentation/glkit/glkmatrix3getmatrix2(_:))
- [func GLKMatrix3GetColumn(GLKMatrix3, Int32) -> GLKVector3](/documentation/glkit/glkmatrix3getcolumn(_:_:))
- [func GLKMatrix3GetRow(GLKMatrix3, Int32) -> GLKVector3](/documentation/glkit/glkmatrix3getrow(_:_:))
- [func GLKMatrix3SetColumn(GLKMatrix3, Int32, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3setcolumn(_:_:_:))
- [func GLKMatrix3SetRow(GLKMatrix3, Int32, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3setrow(_:_:_:))

### Performing Mathematical Operations on Matrices

- [func GLKMatrix3Invert(GLKMatrix3, UnsafeMutablePointer<Bool>!) -> GLKMatrix3](/documentation/glkit/glkmatrix3invert(_:_:))
- [func GLKMatrix3Transpose(GLKMatrix3) -> GLKMatrix3](/documentation/glkit/glkmatrix3transpose(_:))
- [func GLKMatrix3InvertAndTranspose(GLKMatrix3, UnsafeMutablePointer<Bool>!) -> GLKMatrix3](/documentation/glkit/glkmatrix3invertandtranspose(_:_:))
- [func GLKMatrix3Multiply(GLKMatrix3, GLKMatrix3) -> GLKMatrix3](/documentation/glkit/glkmatrix3multiply(_:_:))
- [func GLKMatrix3Rotate(GLKMatrix3, Float, Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotate(_:_:_:_:_:))
- [func GLKMatrix3RotateWithVector3(GLKMatrix3, Float, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotatewithvector3(_:_:_:))
- [func GLKMatrix3RotateWithVector4(GLKMatrix3, Float, GLKVector4) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotatewithvector4(_:_:_:))
- [func GLKMatrix3RotateX(GLKMatrix3, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotatex(_:_:))
- [func GLKMatrix3RotateY(GLKMatrix3, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotatey(_:_:))
- [func GLKMatrix3RotateZ(GLKMatrix3, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3rotatez(_:_:))
- [func GLKMatrix3Scale(GLKMatrix3, Float, Float, Float) -> GLKMatrix3](/documentation/glkit/glkmatrix3scale(_:_:_:_:))
- [func GLKMatrix3ScaleWithVector3(GLKMatrix3, GLKVector3) -> GLKMatrix3](/documentation/glkit/glkmatrix3scalewithvector3(_:_:))
- [func GLKMatrix3ScaleWithVector4(GLKMatrix3, GLKVector4) -> GLKMatrix3](/documentation/glkit/glkmatrix3scalewithvector4(_:_:))
- [func GLKMatrix3Add(GLKMatrix3, GLKMatrix3) -> GLKMatrix3](/documentation/glkit/glkmatrix3add(_:_:))
- [func GLKMatrix3Subtract(GLKMatrix3, GLKMatrix3) -> GLKMatrix3](/documentation/glkit/glkmatrix3subtract(_:_:))

### Performing Mathematical Operations on Vectors

- [func GLKMatrix3MultiplyVector3(GLKMatrix3, GLKVector3) -> GLKVector3](/documentation/glkit/glkmatrix3multiplyvector3(_:_:))
- [func GLKMatrix3MultiplyVector3Array(GLKMatrix3, UnsafeMutablePointer<GLKVector3>, Int)](/documentation/glkit/glkmatrix3multiplyvector3array(_:_:_:))

### Data Types

- [GLKMatrix2](/documentation/glkit/glkmatrix2)
- [GLKMatrix3](/documentation/glkit/glkmatrix3)

### Constants

- [let GLKMatrix3Identity: GLKMatrix3](/documentation/glkit/glkmatrix3identity)
- [GLKMatrix4](/documentation/glkit/glkmatrix4-pce)

### Creating Matrices

- [func GLKMatrix4Make(Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4make(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func GLKMatrix4MakeAndTranspose(Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makeandtranspose(_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:_:))
- [func GLKMatrix4MakeWithArray(UnsafeMutablePointer<Float>!) -> GLKMatrix4](/documentation/glkit/glkmatrix4makewitharray(_:))
- [func GLKMatrix4MakeWithArrayAndTranspose(UnsafeMutablePointer<Float>!) -> GLKMatrix4](/documentation/glkit/glkmatrix4makewitharrayandtranspose(_:))
- [func GLKMatrix4MakeWithColumns(GLKVector4, GLKVector4, GLKVector4, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4makewithcolumns(_:_:_:_:))
- [func GLKMatrix4MakeWithRows(GLKVector4, GLKVector4, GLKVector4, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4makewithrows(_:_:_:_:))
- [func GLKMatrix4MakeRotation(Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makerotation(_:_:_:_:))
- [func GLKMatrix4MakeXRotation(Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makexrotation(_:))
- [func GLKMatrix4MakeYRotation(Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makeyrotation(_:))
- [func GLKMatrix4MakeZRotation(Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makezrotation(_:))
- [func GLKMatrix4MakeWithQuaternion(GLKQuaternion) -> GLKMatrix4](/documentation/glkit/glkmatrix4makewithquaternion(_:))
- [func GLKMatrix4MakeScale(Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makescale(_:_:_:))
- [func GLKMatrix4MakeTranslation(Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4maketranslation(_:_:_:))
- [func GLKMatrix4MakeLookAt(Float, Float, Float, Float, Float, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makelookat(_:_:_:_:_:_:_:_:_:))
- [func GLKMatrix4MakeOrtho(Float, Float, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makeortho(_:_:_:_:_:_:))
- [func GLKMatrix4MakePerspective(Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makeperspective(_:_:_:_:))
- [func GLKMatrix4MakeFrustum(Float, Float, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4makefrustum(_:_:_:_:_:_:))

### Working With Parts of a Matrix

- [func GLKMatrix4GetMatrix2(GLKMatrix4) -> GLKMatrix2](/documentation/glkit/glkmatrix4getmatrix2(_:))
- [func GLKMatrix4GetMatrix3(GLKMatrix4) -> GLKMatrix3](/documentation/glkit/glkmatrix4getmatrix3(_:))
- [func GLKMatrix4GetColumn(GLKMatrix4, Int32) -> GLKVector4](/documentation/glkit/glkmatrix4getcolumn(_:_:))
- [func GLKMatrix4GetRow(GLKMatrix4, Int32) -> GLKVector4](/documentation/glkit/glkmatrix4getrow(_:_:))
- [func GLKMatrix4SetColumn(GLKMatrix4, Int32, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4setcolumn(_:_:_:))
- [func GLKMatrix4SetRow(GLKMatrix4, Int32, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4setrow(_:_:_:))

### Performing Mathematical Operations on Matrices

- [func GLKMatrix4Invert(GLKMatrix4, UnsafeMutablePointer<Bool>?) -> GLKMatrix4](/documentation/glkit/glkmatrix4invert(_:_:))
- [func GLKMatrix4Transpose(GLKMatrix4) -> GLKMatrix4](/documentation/glkit/glkmatrix4transpose(_:))
- [func GLKMatrix4InvertAndTranspose(GLKMatrix4, UnsafeMutablePointer<Bool>?) -> GLKMatrix4](/documentation/glkit/glkmatrix4invertandtranspose(_:_:))
- [func GLKMatrix4Multiply(GLKMatrix4, GLKMatrix4) -> GLKMatrix4](/documentation/glkit/glkmatrix4multiply(_:_:))
- [func GLKMatrix4Rotate(GLKMatrix4, Float, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotate(_:_:_:_:_:))
- [func GLKMatrix4RotateWithVector3(GLKMatrix4, Float, GLKVector3) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotatewithvector3(_:_:_:))
- [func GLKMatrix4RotateWithVector4(GLKMatrix4, Float, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotatewithvector4(_:_:_:))
- [func GLKMatrix4RotateX(GLKMatrix4, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotatex(_:_:))
- [func GLKMatrix4RotateY(GLKMatrix4, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotatey(_:_:))
- [func GLKMatrix4RotateZ(GLKMatrix4, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4rotatez(_:_:))
- [func GLKMatrix4Scale(GLKMatrix4, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4scale(_:_:_:_:))
- [func GLKMatrix4ScaleWithVector3(GLKMatrix4, GLKVector3) -> GLKMatrix4](/documentation/glkit/glkmatrix4scalewithvector3(_:_:))
- [func GLKMatrix4ScaleWithVector4(GLKMatrix4, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4scalewithvector4(_:_:))
- [func GLKMatrix4Translate(GLKMatrix4, Float, Float, Float) -> GLKMatrix4](/documentation/glkit/glkmatrix4translate(_:_:_:_:))
- [func GLKMatrix4TranslateWithVector3(GLKMatrix4, GLKVector3) -> GLKMatrix4](/documentation/glkit/glkmatrix4translatewithvector3(_:_:))
- [func GLKMatrix4TranslateWithVector4(GLKMatrix4, GLKVector4) -> GLKMatrix4](/documentation/glkit/glkmatrix4translatewithvector4(_:_:))
- [func GLKMatrix4Add(GLKMatrix4, GLKMatrix4) -> GLKMatrix4](/documentation/glkit/glkmatrix4add(_:_:))
- [func GLKMatrix4Subtract(GLKMatrix4, GLKMatrix4) -> GLKMatrix4](/documentation/glkit/glkmatrix4subtract(_:_:))

### Performing Mathematical Operations on Vectors

- [func GLKMatrix4MultiplyVector3(GLKMatrix4, GLKVector3) -> GLKVector3](/documentation/glkit/glkmatrix4multiplyvector3(_:_:))
- [func GLKMatrix4MultiplyVector3Array(GLKMatrix4, UnsafeMutablePointer<GLKVector3>, Int)](/documentation/glkit/glkmatrix4multiplyvector3array(_:_:_:))
- [func GLKMatrix4MultiplyVector3WithTranslation(GLKMatrix4, GLKVector3) -> GLKVector3](/documentation/glkit/glkmatrix4multiplyvector3withtranslation(_:_:))
- [func GLKMatrix4MultiplyVector3ArrayWithTranslation(GLKMatrix4, UnsafeMutablePointer<GLKVector3>, Int)](/documentation/glkit/glkmatrix4multiplyvector3arraywithtranslation(_:_:_:))
- [func GLKMatrix4MultiplyVector4(GLKMatrix4, GLKVector4) -> GLKVector4](/documentation/glkit/glkmatrix4multiplyvector4(_:_:))
- [func GLKMatrix4MultiplyVector4Array(GLKMatrix4, UnsafeMutablePointer<GLKVector4>, Int)](/documentation/glkit/glkmatrix4multiplyvector4array(_:_:_:))
- [func GLKMatrix4MultiplyAndProjectVector3(GLKMatrix4, GLKVector3) -> GLKVector3](/documentation/glkit/glkmatrix4multiplyandprojectvector3(_:_:))
- [func GLKMatrix4MultiplyAndProjectVector3Array(GLKMatrix4, UnsafeMutablePointer<GLKVector3>, Int)](/documentation/glkit/glkmatrix4multiplyandprojectvector3array(_:_:_:))

### Data Types

- [GLKMatrix4](/documentation/glkit/glkmatrix4)

### Constants

- [let GLKMatrix4Identity: GLKMatrix4](/documentation/glkit/glkmatrix4identity)
- [GLKVector2](/documentation/glkit/glkvector2-pbj)

### Creating Vectors

- [func GLKVector2Make(Float, Float) -> GLKVector2](/documentation/glkit/glkvector2make(_:_:))
- [func GLKVector2MakeWithArray(UnsafeMutablePointer<Float>!) -> GLKVector2](/documentation/glkit/glkvector2makewitharray(_:))

### Retrieving Information About a Vector

- [func GLKVector2Length(GLKVector2) -> Float](/documentation/glkit/glkvector2length(_:))
- [func GLKVector2Distance(GLKVector2, GLKVector2) -> Float](/documentation/glkit/glkvector2distance(_:_:))

### Mathematical Operations Performed on Vectors

- [func GLKVector2Negate(GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2negate(_:))
- [func GLKVector2Normalize(GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2normalize(_:))
- [func GLKVector2AddScalar(GLKVector2, Float) -> GLKVector2](/documentation/glkit/glkvector2addscalar(_:_:))
- [func GLKVector2SubtractScalar(GLKVector2, Float) -> GLKVector2](/documentation/glkit/glkvector2subtractscalar(_:_:))
- [func GLKVector2MultiplyScalar(GLKVector2, Float) -> GLKVector2](/documentation/glkit/glkvector2multiplyscalar(_:_:))
- [func GLKVector2DivideScalar(GLKVector2, Float) -> GLKVector2](/documentation/glkit/glkvector2dividescalar(_:_:))
- [func GLKVector2Add(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2add(_:_:))
- [func GLKVector2Subtract(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2subtract(_:_:))
- [func GLKVector2Multiply(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2multiply(_:_:))
- [func GLKVector2Divide(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2divide(_:_:))
- [func GLKVector2DotProduct(GLKVector2, GLKVector2) -> Float](/documentation/glkit/glkvector2dotproduct(_:_:))
- [func GLKVector2Lerp(GLKVector2, GLKVector2, Float) -> GLKVector2](/documentation/glkit/glkvector2lerp(_:_:_:))
- [func GLKVector2Project(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2project(_:_:))
- [func GLKVector2Maximum(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2maximum(_:_:))
- [func GLKVector2Minimum(GLKVector2, GLKVector2) -> GLKVector2](/documentation/glkit/glkvector2minimum(_:_:))

### Comparison Operations

- [func GLKVector2AllEqualToScalar(GLKVector2, Float) -> Bool](/documentation/glkit/glkvector2allequaltoscalar(_:_:))
- [func GLKVector2AllEqualToVector2(GLKVector2, GLKVector2) -> Bool](/documentation/glkit/glkvector2allequaltovector2(_:_:))
- [func GLKVector2AllGreaterThanOrEqualToScalar(GLKVector2, Float) -> Bool](/documentation/glkit/glkvector2allgreaterthanorequaltoscalar(_:_:))
- [func GLKVector2AllGreaterThanOrEqualToVector2(GLKVector2, GLKVector2) -> Bool](/documentation/glkit/glkvector2allgreaterthanorequaltovector2(_:_:))
- [func GLKVector2AllGreaterThanScalar(GLKVector2, Float) -> Bool](/documentation/glkit/glkvector2allgreaterthanscalar(_:_:))
- [func GLKVector2AllGreaterThanVector2(GLKVector2, GLKVector2) -> Bool](/documentation/glkit/glkvector2allgreaterthanvector2(_:_:))

### Data Types

- [GLKVector2](/documentation/glkit/glkvector2)
- [GLKVector3](/documentation/glkit/glkvector3-pbt)

### Creating Vectors

- [func GLKVector3Make(Float, Float, Float) -> GLKVector3](/documentation/glkit/glkvector3make(_:_:_:))
- [func GLKVector3MakeWithArray(UnsafeMutablePointer<Float>!) -> GLKVector3](/documentation/glkit/glkvector3makewitharray(_:))

### Retrieving Information About a Vector

- [func GLKVector3Length(GLKVector3) -> Float](/documentation/glkit/glkvector3length(_:))
- [func GLKVector3Distance(GLKVector3, GLKVector3) -> Float](/documentation/glkit/glkvector3distance(_:_:))

### Mathematical Operations Performed on Vectors

- [func GLKVector3Negate(GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3negate(_:))
- [func GLKVector3Normalize(GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3normalize(_:))
- [func GLKVector3AddScalar(GLKVector3, Float) -> GLKVector3](/documentation/glkit/glkvector3addscalar(_:_:))
- [func GLKVector3SubtractScalar(GLKVector3, Float) -> GLKVector3](/documentation/glkit/glkvector3subtractscalar(_:_:))
- [func GLKVector3MultiplyScalar(GLKVector3, Float) -> GLKVector3](/documentation/glkit/glkvector3multiplyscalar(_:_:))
- [func GLKVector3DivideScalar(GLKVector3, Float) -> GLKVector3](/documentation/glkit/glkvector3dividescalar(_:_:))
- [func GLKVector3Add(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3add(_:_:))
- [func GLKVector3Subtract(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3subtract(_:_:))
- [func GLKVector3Multiply(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3multiply(_:_:))
- [func GLKVector3Divide(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3divide(_:_:))
- [func GLKVector3DotProduct(GLKVector3, GLKVector3) -> Float](/documentation/glkit/glkvector3dotproduct(_:_:))
- [func GLKVector3CrossProduct(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3crossproduct(_:_:))
- [func GLKVector3Lerp(GLKVector3, GLKVector3, Float) -> GLKVector3](/documentation/glkit/glkvector3lerp(_:_:_:))
- [func GLKVector3Project(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3project(_:_:))
- [func GLKVector3Maximum(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3maximum(_:_:))
- [func GLKVector3Minimum(GLKVector3, GLKVector3) -> GLKVector3](/documentation/glkit/glkvector3minimum(_:_:))

### Comparison Operations

- [func GLKVector3AllEqualToScalar(GLKVector3, Float) -> Bool](/documentation/glkit/glkvector3allequaltoscalar(_:_:))
- [func GLKVector3AllEqualToVector3(GLKVector3, GLKVector3) -> Bool](/documentation/glkit/glkvector3allequaltovector3(_:_:))
- [func GLKVector3AllGreaterThanOrEqualToScalar(GLKVector3, Float) -> Bool](/documentation/glkit/glkvector3allgreaterthanorequaltoscalar(_:_:))
- [func GLKVector3AllGreaterThanOrEqualToVector3(GLKVector3, GLKVector3) -> Bool](/documentation/glkit/glkvector3allgreaterthanorequaltovector3(_:_:))
- [func GLKVector3AllGreaterThanScalar(GLKVector3, Float) -> Bool](/documentation/glkit/glkvector3allgreaterthanscalar(_:_:))
- [func GLKVector3AllGreaterThanVector3(GLKVector3, GLKVector3) -> Bool](/documentation/glkit/glkvector3allgreaterthanvector3(_:_:))

### Data Types

- [GLKVector3](/documentation/glkit/glkvector3)
- [GLKVector4](/documentation/glkit/glkvector4-pbk)

### Creating Vectors

- [func GLKVector4Make(Float, Float, Float, Float) -> GLKVector4](/documentation/glkit/glkvector4make(_:_:_:_:))
- [func GLKVector4MakeWithArray(UnsafeMutablePointer<Float>!) -> GLKVector4](/documentation/glkit/glkvector4makewitharray(_:))
- [func GLKVector4MakeWithVector3(GLKVector3, Float) -> GLKVector4](/documentation/glkit/glkvector4makewithvector3(_:_:))

### Retrieving Information About a Vector

- [func GLKVector4Length(GLKVector4) -> Float](/documentation/glkit/glkvector4length(_:))
- [func GLKVector4Distance(GLKVector4, GLKVector4) -> Float](/documentation/glkit/glkvector4distance(_:_:))

### Mathematical Operations Performed on Vectors

- [func GLKVector4Negate(GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4negate(_:))
- [func GLKVector4Normalize(GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4normalize(_:))
- [func GLKVector4AddScalar(GLKVector4, Float) -> GLKVector4](/documentation/glkit/glkvector4addscalar(_:_:))
- [func GLKVector4SubtractScalar(GLKVector4, Float) -> GLKVector4](/documentation/glkit/glkvector4subtractscalar(_:_:))
- [func GLKVector4MultiplyScalar(GLKVector4, Float) -> GLKVector4](/documentation/glkit/glkvector4multiplyscalar(_:_:))
- [func GLKVector4DivideScalar(GLKVector4, Float) -> GLKVector4](/documentation/glkit/glkvector4dividescalar(_:_:))
- [func GLKVector4Add(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4add(_:_:))
- [func GLKVector4Subtract(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4subtract(_:_:))
- [func GLKVector4Multiply(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4multiply(_:_:))
- [func GLKVector4Divide(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4divide(_:_:))
- [func GLKVector4DotProduct(GLKVector4, GLKVector4) -> Float](/documentation/glkit/glkvector4dotproduct(_:_:))
- [func GLKVector4CrossProduct(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4crossproduct(_:_:))
- [func GLKVector4Lerp(GLKVector4, GLKVector4, Float) -> GLKVector4](/documentation/glkit/glkvector4lerp(_:_:_:))
- [func GLKVector4Project(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4project(_:_:))
- [func GLKVector4Maximum(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4maximum(_:_:))
- [func GLKVector4Minimum(GLKVector4, GLKVector4) -> GLKVector4](/documentation/glkit/glkvector4minimum(_:_:))

### Comparison Operations

- [func GLKVector4AllEqualToScalar(GLKVector4, Float) -> Bool](/documentation/glkit/glkvector4allequaltoscalar(_:_:))
- [func GLKVector4AllEqualToVector4(GLKVector4, GLKVector4) -> Bool](/documentation/glkit/glkvector4allequaltovector4(_:_:))
- [func GLKVector4AllGreaterThanOrEqualToScalar(GLKVector4, Float) -> Bool](/documentation/glkit/glkvector4allgreaterthanorequaltoscalar(_:_:))
- [func GLKVector4AllGreaterThanOrEqualToVector4(GLKVector4, GLKVector4) -> Bool](/documentation/glkit/glkvector4allgreaterthanorequaltovector4(_:_:))
- [func GLKVector4AllGreaterThanScalar(GLKVector4, Float) -> Bool](/documentation/glkit/glkvector4allgreaterthanscalar(_:_:))
- [func GLKVector4AllGreaterThanVector4(GLKVector4, GLKVector4) -> Bool](/documentation/glkit/glkvector4allgreaterthanvector4(_:_:))

### Data Types

- [GLKVector4](/documentation/glkit/glkvector4)
- [GLKQuaternion](/documentation/glkit/glkquaternion-pc6)

### Creating Quaternions

- [func GLKQuaternionMake(Float, Float, Float, Float) -> GLKQuaternion](/documentation/glkit/glkquaternionmake(_:_:_:_:))
- [func GLKQuaternionMakeWithArray(UnsafeMutablePointer<Float>!) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewitharray(_:))
- [func GLKQuaternionMakeWithVector3(GLKVector3, Float) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewithvector3(_:_:))
- [func GLKQuaternionMakeWithAngleAndAxis(Float, Float, Float, Float) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewithangleandaxis(_:_:_:_:))
- [func GLKQuaternionMakeWithAngleAndVector3Axis(Float, GLKVector3) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewithangleandvector3axis(_:_:))
- [func GLKQuaternionMakeWithMatrix3(GLKMatrix3) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewithmatrix3(_:))
- [func GLKQuaternionMakeWithMatrix4(GLKMatrix4) -> GLKQuaternion](/documentation/glkit/glkquaternionmakewithmatrix4(_:))

### Retrieving Information About a Quaternion

- [func GLKQuaternionLength(GLKQuaternion) -> Float](/documentation/glkit/glkquaternionlength(_:))
- [func GLKQuaternionAxis(GLKQuaternion) -> GLKVector3](/documentation/glkit/glkquaternionaxis(_:))
- [func GLKQuaternionAngle(GLKQuaternion) -> Float](/documentation/glkit/glkquaternionangle(_:))

### Performing Mathematical Operations on Quaternions

- [func GLKQuaternionNormalize(GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternionnormalize(_:))
- [func GLKQuaternionInvert(GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternioninvert(_:))
- [func GLKQuaternionConjugate(GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternionconjugate(_:))
- [func GLKQuaternionAdd(GLKQuaternion, GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternionadd(_:_:))
- [func GLKQuaternionSubtract(GLKQuaternion, GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternionsubtract(_:_:))
- [func GLKQuaternionMultiply(GLKQuaternion, GLKQuaternion) -> GLKQuaternion](/documentation/glkit/glkquaternionmultiply(_:_:))
- [func GLKQuaternionSlerp(GLKQuaternion, GLKQuaternion, Float) -> GLKQuaternion](/documentation/glkit/glkquaternionslerp(_:_:_:))

### Applying Quaternions to Vectors

- [func GLKQuaternionRotateVector3(GLKQuaternion, GLKVector3) -> GLKVector3](/documentation/glkit/glkquaternionrotatevector3(_:_:))
- [func GLKQuaternionRotateVector3Array(GLKQuaternion, UnsafeMutablePointer<GLKVector3>, Int)](/documentation/glkit/glkquaternionrotatevector3array(_:_:_:))
- [func GLKQuaternionRotateVector4(GLKQuaternion, GLKVector4) -> GLKVector4](/documentation/glkit/glkquaternionrotatevector4(_:_:))
- [func GLKQuaternionRotateVector4Array(GLKQuaternion, UnsafeMutablePointer<GLKVector4>, Int)](/documentation/glkit/glkquaternionrotatevector4array(_:_:_:))

### Data Types

- [GLKQuaternion](/documentation/glkit/glkquaternion)

### Constants

- [let GLKQuaternionIdentity: GLKQuaternion](/documentation/glkit/glkquaternionidentity)
- [GLKit Math Utilities](/documentation/glkit/glkit-math-utilities)

### Converting Angles

- [func GLKMathDegreesToRadians(Float) -> Float](/documentation/glkit/glkmathdegreestoradians(_:))
- [func GLKMathRadiansToDegrees(Float) -> Float](/documentation/glkit/glkmathradianstodegrees(_:))

### Projecting Vectors

- [func GLKMathProject(GLKVector3, GLKMatrix4, GLKMatrix4, UnsafeMutablePointer<Int32>) -> GLKVector3](/documentation/glkit/glkmathproject(_:_:_:_:))
- [func GLKMathUnproject(GLKVector3, GLKMatrix4, GLKMatrix4, UnsafeMutablePointer<Int32>, UnsafeMutablePointer<Bool>?) -> GLKVector3](/documentation/glkit/glkmathunproject(_:_:_:_:_:))

### Obtaining String Descriptions

- [func NSStringFromGLKMatrix2(GLKMatrix2) -> String](/documentation/glkit/nsstringfromglkmatrix2(_:))
- [func NSStringFromGLKMatrix3(GLKMatrix3) -> String](/documentation/glkit/nsstringfromglkmatrix3(_:))
- [func NSStringFromGLKMatrix4(GLKMatrix4) -> String](/documentation/glkit/nsstringfromglkmatrix4(_:))
- [func NSStringFromGLKVector2(GLKVector2) -> String](/documentation/glkit/nsstringfromglkvector2(_:))
- [func NSStringFromGLKVector3(GLKVector3) -> String](/documentation/glkit/nsstringfromglkvector3(_:))
- [func NSStringFromGLKVector4(GLKVector4) -> String](/documentation/glkit/nsstringfromglkvector4(_:))
- [func NSStringFromGLKQuaternion(GLKQuaternion) -> String](/documentation/glkit/nsstringfromglkquaternion(_:))

## Reference

- [GLKit Structures](/documentation/glkit/glkit-structures)

### Structures

- [GLKTextureLoaderError](/documentation/glkit/glktextureloadererror-swift.struct)

#### Type Properties

- [static var alphaPremultiplicationFailure: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/alphapremultiplicationfailure)
- [static var compressedTextureUpload: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/compressedtextureupload)
- [static var cubeMapInvalidNumFiles: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/cubemapinvalidnumfiles)
- [static var dataPreprocessingFailure: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/datapreprocessingfailure)
- [static var errorDomain: String](/documentation/glkit/glktextureloadererror-swift.struct/errordomain)
- [static var fileOrURLNotFound: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/fileorurlnotfound)
- [static var incompatibleFormatSRGB: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/incompatibleformatsrgb)
- [static var invalidCGImage: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/invalidcgimage)
- [static var invalidEAGLContext: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/invalideaglcontext)
- [static var invalidNSData: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/invalidnsdata)
- [static var mipmapUnsupported: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/mipmapunsupported)
- [static var pvrAtlasUnsupported: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/pvratlasunsupported)
- [static var reorientationFailure: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/reorientationfailure)
- [static var uncompressedTextureUpload: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/uncompressedtextureupload)
- [static var unknownFileType: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unknownfiletype)
- [static var unknownPathType: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unknownpathtype)
- [static var unsupportedBitDepth: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unsupportedbitdepth)
- [static var unsupportedCubeMapDimensions: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unsupportedcubemapdimensions)
- [static var unsupportedOrientation: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unsupportedorientation)
- [static var unsupportedPVRFormat: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unsupportedpvrformat)
- [static var unsupportedTextureTarget: GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/unsupportedtexturetarget)
- [GLKit Enumerations](/documentation/glkit/glkit-enumerations)

### Enumerations

- [GLKFogMode](/documentation/glkit/glkfogmode)

#### Constants

- [case exp](/documentation/glkit/glkfogmode/exp)
- [case exp2](/documentation/glkit/glkfogmode/exp2)
- [case linear](/documentation/glkit/glkfogmode/linear)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkfogmode/init(rawvalue:))
- [GLKLightingType](/documentation/glkit/glklightingtype)

#### Constants

- [case perVertex](/documentation/glkit/glklightingtype/pervertex)
- [case perPixel](/documentation/glkit/glklightingtype/perpixel)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glklightingtype/init(rawvalue:))
- [GLKTextureEnvMode](/documentation/glkit/glktextureenvmode)

#### Constants

- [case replace](/documentation/glkit/glktextureenvmode/replace)
- [case modulate](/documentation/glkit/glktextureenvmode/modulate)
- [case decal](/documentation/glkit/glktextureenvmode/decal)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureenvmode/init(rawvalue:))
- [GLKTextureInfoAlphaState](/documentation/glkit/glktextureinfoalphastate)

#### Constants

- [case none](/documentation/glkit/glktextureinfoalphastate/none)
- [case nonPremultiplied](/documentation/glkit/glktextureinfoalphastate/nonpremultiplied)
- [case premultiplied](/documentation/glkit/glktextureinfoalphastate/premultiplied)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureinfoalphastate/init(rawvalue:))
- [GLKTextureInfoOrigin](/documentation/glkit/glktextureinfoorigin)

#### Constants

- [case unknown](/documentation/glkit/glktextureinfoorigin/unknown)
- [case topLeft](/documentation/glkit/glktextureinfoorigin/topleft)
- [case bottomLeft](/documentation/glkit/glktextureinfoorigin/bottomleft)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glktextureinfoorigin/init(rawvalue:))
- [GLKTextureLoaderError.Code](/documentation/glkit/glktextureloadererror-swift.struct/code)

#### Initializers

- [init?(rawValue: GLuint)](/documentation/glkit/glktextureloadererror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [case alphaPremultiplicationFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/alphapremultiplicationfailure)
- [case compressedTextureUpload](/documentation/glkit/glktextureloadererror-swift.struct/code/compressedtextureupload)
- [case cubeMapInvalidNumFiles](/documentation/glkit/glktextureloadererror-swift.struct/code/cubemapinvalidnumfiles)
- [case dataPreprocessingFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/datapreprocessingfailure)
- [case fileOrURLNotFound](/documentation/glkit/glktextureloadererror-swift.struct/code/fileorurlnotfound)
- [case incompatibleFormatSRGB](/documentation/glkit/glktextureloadererror-swift.struct/code/incompatibleformatsrgb)
- [case invalidCGImage](/documentation/glkit/glktextureloadererror-swift.struct/code/invalidcgimage)
- [case invalidEAGLContext](/documentation/glkit/glktextureloadererror-swift.struct/code/invalideaglcontext)
- [case invalidNSData](/documentation/glkit/glktextureloadererror-swift.struct/code/invalidnsdata)
- [case mipmapUnsupported](/documentation/glkit/glktextureloadererror-swift.struct/code/mipmapunsupported)
- [case pvrAtlasUnsupported](/documentation/glkit/glktextureloadererror-swift.struct/code/pvratlasunsupported)
- [case reorientationFailure](/documentation/glkit/glktextureloadererror-swift.struct/code/reorientationfailure)
- [case uncompressedTextureUpload](/documentation/glkit/glktextureloadererror-swift.struct/code/uncompressedtextureupload)
- [case unknownFileType](/documentation/glkit/glktextureloadererror-swift.struct/code/unknownfiletype)
- [case unknownPathType](/documentation/glkit/glktextureloadererror-swift.struct/code/unknownpathtype)
- [case unsupportedBitDepth](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedbitdepth)
- [case unsupportedCubeMapDimensions](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedcubemapdimensions)
- [case unsupportedOrientation](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedorientation)
- [case unsupportedPVRFormat](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedpvrformat)
- [case unsupportedTextureTarget](/documentation/glkit/glktextureloadererror-swift.struct/code/unsupportedtexturetarget)
- [GLKTextureTarget](/documentation/glkit/glktexturetarget)

#### Constants

- [case target2D](/documentation/glkit/glktexturetarget/target2d)
- [case targetCubeMap](/documentation/glkit/glktexturetarget/targetcubemap)
- [case targetCt](/documentation/glkit/glktexturetarget/targetct)

#### Initializers

- [init?(rawValue: GLenum)](/documentation/glkit/glktexturetarget/init(rawvalue:))
- [GLKViewDrawableColorFormat](/documentation/glkit/glkviewdrawablecolorformat)

#### Constants

- [case RGBA8888](/documentation/glkit/glkviewdrawablecolorformat/rgba8888)
- [case RGB565](/documentation/glkit/glkviewdrawablecolorformat/rgb565)
- [case SRGBA8888](/documentation/glkit/glkviewdrawablecolorformat/srgba8888)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablecolorformat/init(rawvalue:))
- [GLKViewDrawableDepthFormat](/documentation/glkit/glkviewdrawabledepthformat)

#### Constants

- [case formatNone](/documentation/glkit/glkviewdrawabledepthformat/formatnone)
- [case format16](/documentation/glkit/glkviewdrawabledepthformat/format16)
- [case format24](/documentation/glkit/glkviewdrawabledepthformat/format24)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawabledepthformat/init(rawvalue:))
- [GLKViewDrawableMultisample](/documentation/glkit/glkviewdrawablemultisample)

#### Constants

- [case multisampleNone](/documentation/glkit/glkviewdrawablemultisample/multisamplenone)
- [case multisample4X](/documentation/glkit/glkviewdrawablemultisample/multisample4x)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablemultisample/init(rawvalue:))
- [GLKViewDrawableStencilFormat](/documentation/glkit/glkviewdrawablestencilformat)

#### Constants

- [case formatNone](/documentation/glkit/glkviewdrawablestencilformat/formatnone)
- [case format8](/documentation/glkit/glkviewdrawablestencilformat/format8)

#### Initializers

- [init?(rawValue: GLint)](/documentation/glkit/glkviewdrawablestencilformat/init(rawvalue:))
- [GLKit Constants](/documentation/glkit/glkit-constants)

### Constants

- [let GLKTextureLoaderApplyPremultiplication: String](/documentation/glkit/glktextureloaderapplypremultiplication)
- [let GLKTextureLoaderErrorDomain: String](/documentation/glkit/glktextureloadererrordomain)
- [let GLKTextureLoaderErrorKey: String](/documentation/glkit/glktextureloadererrorkey)
- [let GLKTextureLoaderGLErrorKey: String](/documentation/glkit/glktextureloaderglerrorkey)
- [let GLKTextureLoaderGenerateMipmaps: String](/documentation/glkit/glktextureloadergeneratemipmaps)
- [let GLKTextureLoaderGrayscaleAsAlpha: String](/documentation/glkit/glktextureloadergrayscaleasalpha)
- [let GLKTextureLoaderOriginBottomLeft: String](/documentation/glkit/glktextureloaderoriginbottomleft)
- [let GLKTextureLoaderSRGB: String](/documentation/glkit/glktextureloadersrgb)
- [var GLK_SSE3_INTRINSICS: Int32](/documentation/glkit/glk_sse3_intrinsics)
- [let kGLKModelErrorDomain: String](/documentation/glkit/kglkmodelerrordomain)
- [let kGLKModelErrorKey: String](/documentation/glkit/kglkmodelerrorkey)
- [GLKit Functions](/documentation/glkit/glkit-functions)

### Functions

- [func GLKMatrixStackCreate(CFAllocator?) -> Unmanaged<GLKMatrixStack>?](/documentation/glkit/glkmatrixstackcreate(_:))
- [func GLKMatrixStackGetMatrix2(GLKMatrixStack) -> GLKMatrix2](/documentation/glkit/glkmatrixstackgetmatrix2(_:))
- [func GLKMatrixStackGetMatrix3(GLKMatrixStack) -> GLKMatrix3](/documentation/glkit/glkmatrixstackgetmatrix3(_:))
- [func GLKMatrixStackGetMatrix3Inverse(GLKMatrixStack) -> GLKMatrix3](/documentation/glkit/glkmatrixstackgetmatrix3inverse(_:))
- [func GLKMatrixStackGetMatrix3InverseTranspose(GLKMatrixStack) -> GLKMatrix3](/documentation/glkit/glkmatrixstackgetmatrix3inversetranspose(_:))
- [func GLKMatrixStackGetMatrix4(GLKMatrixStack) -> GLKMatrix4](/documentation/glkit/glkmatrixstackgetmatrix4(_:))
- [func GLKMatrixStackGetMatrix4Inverse(GLKMatrixStack) -> GLKMatrix4](/documentation/glkit/glkmatrixstackgetmatrix4inverse(_:))
- [func GLKMatrixStackGetMatrix4InverseTranspose(GLKMatrixStack) -> GLKMatrix4](/documentation/glkit/glkmatrixstackgetmatrix4inversetranspose(_:))
- [func GLKMatrixStackGetTypeID() -> CFTypeID](/documentation/glkit/glkmatrixstackgettypeid())
- [func GLKMatrixStackLoadMatrix4(GLKMatrixStack, GLKMatrix4)](/documentation/glkit/glkmatrixstackloadmatrix4(_:_:))
- [func GLKMatrixStackMultiplyMatrix4(GLKMatrixStack, GLKMatrix4)](/documentation/glkit/glkmatrixstackmultiplymatrix4(_:_:))
- [func GLKMatrixStackMultiplyMatrixStack(GLKMatrixStack, GLKMatrixStack)](/documentation/glkit/glkmatrixstackmultiplymatrixstack(_:_:))
- [func GLKMatrixStackPop(GLKMatrixStack)](/documentation/glkit/glkmatrixstackpop(_:))
- [func GLKMatrixStackPush(GLKMatrixStack)](/documentation/glkit/glkmatrixstackpush(_:))
- [func GLKMatrixStackRotate(GLKMatrixStack, Float, Float, Float, Float)](/documentation/glkit/glkmatrixstackrotate(_:_:_:_:_:))
- [func GLKMatrixStackRotateWithVector3(GLKMatrixStack, Float, GLKVector3)](/documentation/glkit/glkmatrixstackrotatewithvector3(_:_:_:))
- [func GLKMatrixStackRotateWithVector4(GLKMatrixStack, Float, GLKVector4)](/documentation/glkit/glkmatrixstackrotatewithvector4(_:_:_:))
- [func GLKMatrixStackRotateX(GLKMatrixStack, Float)](/documentation/glkit/glkmatrixstackrotatex(_:_:))
- [func GLKMatrixStackRotateY(GLKMatrixStack, Float)](/documentation/glkit/glkmatrixstackrotatey(_:_:))
- [func GLKMatrixStackRotateZ(GLKMatrixStack, Float)](/documentation/glkit/glkmatrixstackrotatez(_:_:))
- [func GLKMatrixStackScale(GLKMatrixStack, Float, Float, Float)](/documentation/glkit/glkmatrixstackscale(_:_:_:_:))
- [func GLKMatrixStackScaleWithVector3(GLKMatrixStack, GLKVector3)](/documentation/glkit/glkmatrixstackscalewithvector3(_:_:))
- [func GLKMatrixStackScaleWithVector4(GLKMatrixStack, GLKVector4)](/documentation/glkit/glkmatrixstackscalewithvector4(_:_:))
- [func GLKMatrixStackSize(GLKMatrixStack) -> Int32](/documentation/glkit/glkmatrixstacksize(_:))
- [func GLKMatrixStackTranslate(GLKMatrixStack, Float, Float, Float)](/documentation/glkit/glkmatrixstacktranslate(_:_:_:_:))
- [func GLKMatrixStackTranslateWithVector3(GLKMatrixStack, GLKVector3)](/documentation/glkit/glkmatrixstacktranslatewithvector3(_:_:))
- [func GLKMatrixStackTranslateWithVector4(GLKMatrixStack, GLKVector4)](/documentation/glkit/glkmatrixstacktranslatewithvector4(_:_:))
- [func GLKVertexAttributeParametersFromModelIO(MDLVertexFormat) -> GLKVertexAttributeParameters](/documentation/glkit/glkvertexattributeparametersfrommodelio(_:))
- [GLKit Data Types](/documentation/glkit/glkit-data-types)

### Data Types

- [GLKTextureLoaderCallback](/documentation/glkit/glktextureloadercallback)
- [GLKVertexAttributeParameters](/documentation/glkit/glkvertexattributeparameters)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
