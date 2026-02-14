# SceneKit Documentation

Source: https://sosumi.ai/documentation/scenekit

---
title: SceneKit
source: https://developer.apple.com/documentation/scenekit
timestamp: 2026-02-13T19:24:12.158Z
---

## Essentials

- [SCNScene](/documentation/scenekit/scnscene)

### Creating a Scene from a File

- [convenience init?(named: String)](/documentation/scenekit/scnscene/init(named:))
- [convenience init?(named: String, inDirectory: String?, options: [SCNSceneSource.LoadingOption : Any]?)](/documentation/scenekit/scnscene/init(named:indirectory:options:))
- [convenience init(url: URL, options: [SCNSceneSource.LoadingOption : Any]?) throws](/documentation/scenekit/scnscene/init(url:options:))

### Managing Animated Effects in a Scene

- [var isPaused: Bool](/documentation/scenekit/scnscene/ispaused)

### Accessing Scene Contents

- [var rootNode: SCNNode](/documentation/scenekit/scnscene/rootnode)
- [var background: SCNMaterialProperty](/documentation/scenekit/scnscene/background)
- [var lightingEnvironment: SCNMaterialProperty](/documentation/scenekit/scnscene/lightingenvironment)

### Managing Scene Attributes

- [func attribute(forKey: String) -> Any?](/documentation/scenekit/scnscene/attribute(forkey:))
- [func setAttribute(Any?, forKey: String)](/documentation/scenekit/scnscene/setattribute(_:forkey:))
- [SCNScene.Attribute](/documentation/scenekit/scnscene/attribute)

#### Type Properties

- [static let endTime: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/endtime)
- [static let frameRate: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/framerate)
- [static let startTime: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/starttime)
- [static let upAxis: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/upaxis)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnscene/attribute/init(rawvalue:))

### Exporting a Scene File

- [func write(to: URL, options: [String : Any]?, delegate: (any SCNSceneExportDelegate)?, progressHandler: SCNSceneExportProgressHandler?) -> Bool](/documentation/scenekit/scnscene/write(to:options:delegate:progresshandler:))
- [SCNSceneExportDelegate](/documentation/scenekit/scnsceneexportdelegate)

#### Writing Image Attachments

- [func write(UIImage, withSceneDocumentURL: URL, originalImageURL: URL?) -> URL?](/documentation/scenekit/scnsceneexportdelegate/write(_:withscenedocumenturl:originalimageurl:))

### Adding Fog to a Scene

- [var fogStartDistance: CGFloat](/documentation/scenekit/scnscene/fogstartdistance)
- [var fogEndDistance: CGFloat](/documentation/scenekit/scnscene/fogenddistance)
- [var fogDensityExponent: CGFloat](/documentation/scenekit/scnscene/fogdensityexponent)
- [var fogColor: Any](/documentation/scenekit/scnscene/fogcolor)

### Working With Physics in the Scene

- [var physicsWorld: SCNPhysicsWorld](/documentation/scenekit/scnscene/physicsworld)

### Working with Particle Systems in the Scene

- [func addParticleSystem(SCNParticleSystem, transform: SCNMatrix4)](/documentation/scenekit/scnscene/addparticlesystem(_:transform:))
- [var particleSystems: [SCNParticleSystem]?](/documentation/scenekit/scnscene/particlesystems)
- [func removeParticleSystem(SCNParticleSystem)](/documentation/scenekit/scnscene/removeparticlesystem(_:))
- [func removeAllParticleSystems()](/documentation/scenekit/scnscene/removeallparticlesystems())

### Constants

- [Scene Attributes](/documentation/scenekit/scene-attributes)

#### Constants

- [static let endTime: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/endtime)
- [static let frameRate: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/framerate)
- [static let startTime: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/starttime)
- [static let upAxis: SCNScene.Attribute](/documentation/scenekit/scnscene/attribute/upaxis)
- [Scene Export Options](/documentation/scenekit/scene-export-options)

#### Constants

- [let SCNSceneExportDestinationURL: String](/documentation/scenekit/scnsceneexportdestinationurl)
- [SCNSceneExportProgressHandler](/documentation/scenekit/scnsceneexportprogresshandler)

### Instance Properties

- [var screenSpaceReflectionMaximumDistance: CGFloat](/documentation/scenekit/scnscene/screenspacereflectionmaximumdistance)
- [var screenSpaceReflectionSampleCount: Int](/documentation/scenekit/scnscene/screenspacereflectionsamplecount)
- [var screenSpaceReflectionStride: CGFloat](/documentation/scenekit/scnscene/screenspacereflectionstride)
- [var wantsScreenSpaceReflection: Bool](/documentation/scenekit/scnscene/wantsscreenspacereflection)
- [SCNView](/documentation/scenekit/scnview)

### Initializing a SceneKit View

- [init(frame: CGRect, options: [String : Any]?)](/documentation/scenekit/scnview/init(frame:options:))
- [SCNView.Option](/documentation/scenekit/scnview/option)

#### View Options

- [static let preferLowPowerDevice: SCNView.Option](/documentation/scenekit/scnview/option/preferlowpowerdevice)
- [static let preferredDevice: SCNView.Option](/documentation/scenekit/scnview/option/preferreddevice)
- [static let preferredRenderingAPI: SCNView.Option](/documentation/scenekit/scnview/option/preferredrenderingapi)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnview/option/init(rawvalue:))

### Specifying a Scene

- [var scene: SCNScene?](/documentation/scenekit/scnview/scene)

### Configuring a View

- [var backgroundColor: NSColor](/documentation/scenekit/scnview/backgroundcolor)
- [var preferredFramesPerSecond: Int](/documentation/scenekit/scnview/preferredframespersecond)
- [var rendersContinuously: Bool](/documentation/scenekit/scnview/renderscontinuously)
- [var antialiasingMode: SCNAntialiasingMode](/documentation/scenekit/scnview/antialiasingmode)
- [SCNAntialiasingMode](/documentation/scenekit/scnantialiasingmode)

#### Constants

- [case none](/documentation/scenekit/scnantialiasingmode/none)
- [case multisampling2X](/documentation/scenekit/scnantialiasingmode/multisampling2x)
- [case multisampling4X](/documentation/scenekit/scnantialiasingmode/multisampling4x)
- [case multisampling8X](/documentation/scenekit/scnantialiasingmode/multisampling8x)
- [case multisampling16X](/documentation/scenekit/scnantialiasingmode/multisampling16x)

#### Initializers

- [init?(rawValue: UInt)](/documentation/scenekit/scnantialiasingmode/init(rawvalue:))

### Managing Camera Controls

- [var allowsCameraControl: Bool](/documentation/scenekit/scnview/allowscameracontrol)
- [var cameraControlConfiguration: any SCNCameraControlConfiguration](/documentation/scenekit/scnview/cameracontrolconfiguration)
- [SCNCameraControlConfiguration](/documentation/scenekit/scncameracontrolconfiguration)

#### Instance Properties

- [var allowsTranslation: Bool](/documentation/scenekit/scncameracontrolconfiguration/allowstranslation)
- [var autoSwitchToFreeCamera: Bool](/documentation/scenekit/scncameracontrolconfiguration/autoswitchtofreecamera)
- [var flyModeVelocity: CGFloat](/documentation/scenekit/scncameracontrolconfiguration/flymodevelocity)
- [var panSensitivity: CGFloat](/documentation/scenekit/scncameracontrolconfiguration/pansensitivity)
- [var rotationSensitivity: CGFloat](/documentation/scenekit/scncameracontrolconfiguration/rotationsensitivity)
- [var truckSensitivity: CGFloat](/documentation/scenekit/scncameracontrolconfiguration/trucksensitivity)
- [var defaultCameraController: SCNCameraController](/documentation/scenekit/scnview/defaultcameracontroller)
- [SCNCameraController](/documentation/scenekit/scncameracontroller)

#### Responding to Control Events

- [var delegate: (any SCNCameraControllerDelegate)?](/documentation/scenekit/scncameracontroller/delegate)
- [SCNCameraControllerDelegate](/documentation/scenekit/scncameracontrollerdelegate)

##### Instance Methods

- [func cameraInertiaDidEnd(for: SCNCameraController)](/documentation/scenekit/scncameracontrollerdelegate/camerainertiadidend(for:))
- [func cameraInertiaWillStart(for: SCNCameraController)](/documentation/scenekit/scncameracontrollerdelegate/camerainertiawillstart(for:))

#### Supporting Types

- [SCNInteractionMode](/documentation/scenekit/scninteractionmode)

##### Enumeration Cases

- [case fly](/documentation/scenekit/scninteractionmode/fly)
- [case orbitAngleMapping](/documentation/scenekit/scninteractionmode/orbitanglemapping)
- [case orbitArcball](/documentation/scenekit/scninteractionmode/orbitarcball)
- [case orbitCenteredArcball](/documentation/scenekit/scninteractionmode/orbitcenteredarcball)
- [case orbitTurntable](/documentation/scenekit/scninteractionmode/orbitturntable)
- [case pan](/documentation/scenekit/scninteractionmode/pan)
- [case truck](/documentation/scenekit/scninteractionmode/truck)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scninteractionmode/init(rawvalue:))

#### Instance Properties

- [var automaticTarget: Bool](/documentation/scenekit/scncameracontroller/automatictarget)
- [var inertiaEnabled: Bool](/documentation/scenekit/scncameracontroller/inertiaenabled)
- [var inertiaFriction: Float](/documentation/scenekit/scncameracontroller/inertiafriction)
- [var interactionMode: SCNInteractionMode](/documentation/scenekit/scncameracontroller/interactionmode)
- [var isInertiaRunning: Bool](/documentation/scenekit/scncameracontroller/isinertiarunning)
- [var maximumHorizontalAngle: Float](/documentation/scenekit/scncameracontroller/maximumhorizontalangle)
- [var maximumVerticalAngle: Float](/documentation/scenekit/scncameracontroller/maximumverticalangle)
- [var minimumHorizontalAngle: Float](/documentation/scenekit/scncameracontroller/minimumhorizontalangle)
- [var minimumVerticalAngle: Float](/documentation/scenekit/scncameracontroller/minimumverticalangle)
- [var pointOfView: SCNNode?](/documentation/scenekit/scncameracontroller/pointofview)
- [var target: SCNVector3](/documentation/scenekit/scncameracontroller/target)
- [var worldUp: SCNVector3](/documentation/scenekit/scncameracontroller/worldup)

#### Instance Methods

- [func beginInteraction(CGPoint, withViewport: CGSize)](/documentation/scenekit/scncameracontroller/begininteraction(_:withviewport:))
- [func clearRoll()](/documentation/scenekit/scncameracontroller/clearroll())
- [func continueInteraction(CGPoint, withViewport: CGSize, sensitivity: CGFloat)](/documentation/scenekit/scncameracontroller/continueinteraction(_:withviewport:sensitivity:))
- [func dolly(by: Float, onScreenPoint: CGPoint, viewport: CGSize)](/documentation/scenekit/scncameracontroller/dolly(by:onscreenpoint:viewport:))
- [func dolly(toTarget: Float)](/documentation/scenekit/scncameracontroller/dolly(totarget:))
- [func endInteraction(CGPoint, withViewport: CGSize, velocity: CGPoint)](/documentation/scenekit/scncameracontroller/endinteraction(_:withviewport:velocity:))
- [func frameNodes([SCNNode])](/documentation/scenekit/scncameracontroller/framenodes(_:))
- [func roll(by: Float, aroundScreenPoint: CGPoint, viewport: CGSize)](/documentation/scenekit/scncameracontroller/roll(by:aroundscreenpoint:viewport:))
- [func rollAroundTarget(Float)](/documentation/scenekit/scncameracontroller/rollaroundtarget(_:))
- [func rotateBy(x: Float, y: Float)](/documentation/scenekit/scncameracontroller/rotateby(x:y:))
- [func stopInertia()](/documentation/scenekit/scncameracontroller/stopinertia())
- [func translateInCameraSpaceBy(x: Float, y: Float, z: Float)](/documentation/scenekit/scncameracontroller/translateincameraspaceby(x:y:z:))

### Playing Action and Animation in a View’s Scene

- [func pause(Any?)](/documentation/scenekit/scnview/pause(_:))
- [func play(Any?)](/documentation/scenekit/scnview/play(_:))
- [func stop(Any?)](/documentation/scenekit/scnview/stop(_:))

### Capturing a View Snapshot

- [func snapshot() -> UIImage](/documentation/scenekit/scnview/snapshot())

### Working with a View’s OpenGL ES Context

- [var eaglContext: EAGLContext?](/documentation/scenekit/scnview/eaglcontext)

### Working with a View’s OpenGL Context

- [var openGLContext: NSOpenGLContext?](/documentation/scenekit/scnview/openglcontext)
- [var pixelFormat: NSOpenGLPixelFormat?](/documentation/scenekit/scnview/pixelformat)

### Instance Properties

- [var drawableResizesAsynchronously: Bool](/documentation/scenekit/scnview/drawableresizesasynchronously)
- [SceneView](/documentation/scenekit/sceneview)

### Creating a Scene View

- [init(scene: SCNScene?, pointOfView: SCNNode?, options: SceneView.Options, preferredFramesPerSecond: Int, antialiasingMode: SCNAntialiasingMode, delegate: (any SCNSceneRendererDelegate)?, technique: SCNTechnique?)](/documentation/scenekit/sceneview/init(scene:pointofview:options:preferredframespersecond:antialiasingmode:delegate:technique:))
- [SceneView.Options](/documentation/scenekit/sceneview/options)

#### Type Properties

- [static let allowsCameraControl: SceneView.Options](/documentation/scenekit/sceneview/options/allowscameracontrol)
- [static let autoenablesDefaultLighting: SceneView.Options](/documentation/scenekit/sceneview/options/autoenablesdefaultlighting)
- [static let jitteringEnabled: SceneView.Options](/documentation/scenekit/sceneview/options/jitteringenabled)
- [static let rendersContinuously: SceneView.Options](/documentation/scenekit/sceneview/options/renderscontinuously)
- [static let temporalAntialiasingEnabled: SceneView.Options](/documentation/scenekit/sceneview/options/temporalantialiasingenabled)

## Scene Structure

- [Organizing a Scene with Nodes](/documentation/scenekit/organizing-a-scene-with-nodes)
- [SCNNode](/documentation/scenekit/scnnode)

### Creating a Node

- [init(geometry: SCNGeometry?)](/documentation/scenekit/scnnode/init(geometry:))

### Managing the Node’s Transform

- [var simdTransform: simd_float4x4](/documentation/scenekit/scnnode/simdtransform)
- [var simdPosition: simd_float3](/documentation/scenekit/scnnode/simdposition)
- [var simdRotation: simd_float4](/documentation/scenekit/scnnode/simdrotation)
- [var simdEulerAngles: simd_float3](/documentation/scenekit/scnnode/simdeulerangles)
- [var simdOrientation: simd_quatf](/documentation/scenekit/scnnode/simdorientation)
- [var simdScale: simd_float3](/documentation/scenekit/scnnode/simdscale)
- [var simdPivot: simd_float4x4](/documentation/scenekit/scnnode/simdpivot)

### Managing Node Content

- [var name: String?](/documentation/scenekit/scnnode/name)
- [var light: SCNLight?](/documentation/scenekit/scnnode/light)
- [var camera: SCNCamera?](/documentation/scenekit/scnnode/camera)
- [var geometry: SCNGeometry?](/documentation/scenekit/scnnode/geometry)
- [var morpher: SCNMorpher?](/documentation/scenekit/scnnode/morpher)
- [var skinner: SCNSkinner?](/documentation/scenekit/scnnode/skinner)
- [var categoryBitMask: Int](/documentation/scenekit/scnnode/categorybitmask)
- [SCNBoundingVolume](/documentation/scenekit/scnboundingvolume)

#### Measuring an Object’s Bounding Volume

- [var boundingBox: (min: SCNVector3, max: SCNVector3)](/documentation/scenekit/scnboundingvolume/boundingbox)
- [var boundingSphere: (center: SCNVector3, radius: Float)](/documentation/scenekit/scnboundingvolume/boundingsphere)

### Constraining Node Behavior

- [var constraints: [SCNConstraint]?](/documentation/scenekit/scnnode/constraints)

### Working with Node Animation

- [var presentation: SCNNode](/documentation/scenekit/scnnode/presentation)
- [var isPaused: Bool](/documentation/scenekit/scnnode/ispaused)

### Modifying the Node Visibility

- [var isHidden: Bool](/documentation/scenekit/scnnode/ishidden)
- [var opacity: CGFloat](/documentation/scenekit/scnnode/opacity)
- [var renderingOrder: Int](/documentation/scenekit/scnnode/renderingorder)
- [var castsShadow: Bool](/documentation/scenekit/scnnode/castsshadow)
- [var movabilityHint: SCNMovabilityHint](/documentation/scenekit/scnnode/movabilityhint)
- [SCNMovabilityHint](/documentation/scenekit/scnmovabilityhint)

#### Constants

- [case fixed](/documentation/scenekit/scnmovabilityhint/fixed)
- [case movable](/documentation/scenekit/scnmovabilityhint/movable)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnmovabilityhint/init(rawvalue:))

### Managing the Node Hierarchy

- [var parent: SCNNode?](/documentation/scenekit/scnnode/parent)
- [var childNodes: [SCNNode]](/documentation/scenekit/scnnode/childnodes)
- [func addChildNode(SCNNode)](/documentation/scenekit/scnnode/addchildnode(_:))
- [func insertChildNode(SCNNode, at: Int)](/documentation/scenekit/scnnode/insertchildnode(_:at:))
- [func removeFromParentNode()](/documentation/scenekit/scnnode/removefromparentnode())
- [func replaceChildNode(SCNNode, with: SCNNode)](/documentation/scenekit/scnnode/replacechildnode(_:with:))

### Searching the Node Hierarchy

- [func childNodes(passingTest: (SCNNode, UnsafeMutablePointer<ObjCBool>) -> Bool) -> [SCNNode]](/documentation/scenekit/scnnode/childnodes(passingtest:))
- [func childNode(withName: String, recursively: Bool) -> SCNNode?](/documentation/scenekit/scnnode/childnode(withname:recursively:))
- [func enumerateChildNodes((SCNNode, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/scenekit/scnnode/enumeratechildnodes(_:))
- [func enumerateHierarchy((SCNNode, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/scenekit/scnnode/enumeratehierarchy(_:))

### Customizing Node Rendering

- [var filters: [CIFilter]?](/documentation/scenekit/scnnode/filters)
- [var rendererDelegate: (any SCNNodeRendererDelegate)?](/documentation/scenekit/scnnode/rendererdelegate)

### Adding Physics to a Node

- [var physicsBody: SCNPhysicsBody?](/documentation/scenekit/scnnode/physicsbody)
- [var physicsField: SCNPhysicsField?](/documentation/scenekit/scnnode/physicsfield)

### Working with Particle Systems

- [func addParticleSystem(SCNParticleSystem)](/documentation/scenekit/scnnode/addparticlesystem(_:))
- [var particleSystems: [SCNParticleSystem]?](/documentation/scenekit/scnnode/particlesystems)
- [func removeParticleSystem(SCNParticleSystem)](/documentation/scenekit/scnnode/removeparticlesystem(_:))
- [func removeAllParticleSystems()](/documentation/scenekit/scnnode/removeallparticlesystems())

### Working with Positional Audio

- [func addAudioPlayer(SCNAudioPlayer)](/documentation/scenekit/scnnode/addaudioplayer(_:))
- [var audioPlayers: [SCNAudioPlayer]](/documentation/scenekit/scnnode/audioplayers)
- [func removeAudioPlayer(SCNAudioPlayer)](/documentation/scenekit/scnnode/removeaudioplayer(_:))
- [func removeAllAudioPlayers()](/documentation/scenekit/scnnode/removeallaudioplayers())

### Copying a Node

- [func clone() -> Self](/documentation/scenekit/scnnode/clone())
- [func flattenedClone() -> Self](/documentation/scenekit/scnnode/flattenedclone())

### Hit-Testing

- [func hitTestWithSegment(from: SCNVector3, to: SCNVector3, options: [String : Any]?) -> [SCNHitTestResult]](/documentation/scenekit/scnnode/hittestwithsegment(from:to:options:))
- [SCNHitTestOption](/documentation/scenekit/scnhittestoption)

#### Options

- [static let backFaceCulling: SCNHitTestOption](/documentation/scenekit/scnhittestoption/backfaceculling)
- [static let boundingBoxOnly: SCNHitTestOption](/documentation/scenekit/scnhittestoption/boundingboxonly)
- [static let categoryBitMask: SCNHitTestOption](/documentation/scenekit/scnhittestoption/categorybitmask)
- [static let clipToZRange: SCNHitTestOption](/documentation/scenekit/scnhittestoption/cliptozrange)
- [static let ignoreChildNodes: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorechildnodes)
- [static let ignoreHiddenNodes: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorehiddennodes)
- [static let rootNode: SCNHitTestOption](/documentation/scenekit/scnhittestoption/rootnode)
- [static let searchMode: SCNHitTestOption](/documentation/scenekit/scnhittestoption/searchmode)
- [SCNHitTestSearchMode](/documentation/scenekit/scnhittestsearchmode)

##### Search Modes

- [case all](/documentation/scenekit/scnhittestsearchmode/all)
- [case any](/documentation/scenekit/scnhittestsearchmode/any)
- [case closest](/documentation/scenekit/scnhittestsearchmode/closest)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnhittestsearchmode/init(rawvalue:))

#### Deprecated

- [static let firstFoundOnly: SCNHitTestOption](/documentation/scenekit/scnhittestoption/firstfoundonly)
- [static let sortResults: SCNHitTestOption](/documentation/scenekit/scnhittestoption/sortresults)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnhittestoption/init(rawvalue:))

#### Type Properties

- [static let ignoreLightArea: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorelightarea)

### Performing Node-Relative Operations

- [func simdRotate(by: simd_quatf, aroundTarget: simd_float3)](/documentation/scenekit/scnnode/simdrotate(by:aroundtarget:))
- [func simdLocalTranslate(by: simd_float3)](/documentation/scenekit/scnnode/simdlocaltranslate(by:))
- [func simdLocalRotate(by: simd_quatf)](/documentation/scenekit/scnnode/simdlocalrotate(by:))
- [func simdLook(at: simd_float3)](/documentation/scenekit/scnnode/simdlook(at:))
- [func simdLook(at: simd_float3, up: simd_float3, localFront: simd_float3)](/documentation/scenekit/scnnode/simdlook(at:up:localfront:))

### Calculating Node-Relative Transforms

- [class var simdLocalRight: simd_float3](/documentation/scenekit/scnnode/simdlocalright)
- [class var simdLocalUp: simd_float3](/documentation/scenekit/scnnode/simdlocalup)
- [class var simdLocalFront: simd_float3](/documentation/scenekit/scnnode/simdlocalfront)
- [var simdWorldRight: simd_float3](/documentation/scenekit/scnnode/simdworldright)
- [var simdWorldUp: simd_float3](/documentation/scenekit/scnnode/simdworldup)
- [var simdWorldFront: simd_float3](/documentation/scenekit/scnnode/simdworldfront)

### Managing Transforms in World Space

- [var simdWorldTransform: simd_float4x4](/documentation/scenekit/scnnode/simdworldtransform)
- [var simdWorldOrientation: simd_quatf](/documentation/scenekit/scnnode/simdworldorientation)
- [var simdWorldPosition: simd_float3](/documentation/scenekit/scnnode/simdworldposition)

### Converting Between Coordinate Spaces

- [func simdConvertPosition(simd_float3, from: SCNNode?) -> simd_float3](/documentation/scenekit/scnnode/simdconvertposition(_:from:))
- [func simdConvertPosition(simd_float3, to: SCNNode?) -> simd_float3](/documentation/scenekit/scnnode/simdconvertposition(_:to:))
- [func simdConvertTransform(simd_float4x4, from: SCNNode?) -> simd_float4x4](/documentation/scenekit/scnnode/simdconverttransform(_:from:))
- [func simdConvertTransform(simd_float4x4, to: SCNNode?) -> simd_float4x4](/documentation/scenekit/scnnode/simdconverttransform(_:to:))
- [func simdConvertVector(simd_float3, from: SCNNode?) -> simd_float3](/documentation/scenekit/scnnode/simdconvertvector(_:from:))
- [func simdConvertVector(simd_float3, to: SCNNode?) -> simd_float3](/documentation/scenekit/scnnode/simdconvertvector(_:to:))

### Handling UI Focus

- [var focusBehavior: SCNNodeFocusBehavior](/documentation/scenekit/scnnode/focusbehavior)
- [SCNNodeFocusBehavior](/documentation/scenekit/scnnodefocusbehavior)

#### Enumeration Cases

- [case none](/documentation/scenekit/scnnodefocusbehavior/none)
- [case occluding](/documentation/scenekit/scnnodefocusbehavior/occluding)
- [case focusable](/documentation/scenekit/scnnodefocusbehavior/focusable)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnnodefocusbehavior/init(rawvalue:))

### Working with GameplayKit

- [var entity: GKEntity?](/documentation/scenekit/scnnode/entity)

### Managing the Node’s Transform (SceneKit Types)

- [var transform: SCNMatrix4](/documentation/scenekit/scnnode/transform)
- [var position: SCNVector3](/documentation/scenekit/scnnode/position)
- [var rotation: SCNVector4](/documentation/scenekit/scnnode/rotation)
- [var eulerAngles: SCNVector3](/documentation/scenekit/scnnode/eulerangles)
- [var orientation: SCNQuaternion](/documentation/scenekit/scnnode/orientation)
- [var scale: SCNVector3](/documentation/scenekit/scnnode/scale)
- [var pivot: SCNMatrix4](/documentation/scenekit/scnnode/pivot)

### Performing Node-Relative Operations (SceneKit Types)

- [func rotate(by: SCNQuaternion, aroundTarget: SCNVector3)](/documentation/scenekit/scnnode/rotate(by:aroundtarget:))
- [func localTranslate(by: SCNVector3)](/documentation/scenekit/scnnode/localtranslate(by:))
- [func localRotate(by: SCNQuaternion)](/documentation/scenekit/scnnode/localrotate(by:))
- [func look(at: SCNVector3)](/documentation/scenekit/scnnode/look(at:))
- [func look(at: SCNVector3, up: SCNVector3, localFront: SCNVector3)](/documentation/scenekit/scnnode/look(at:up:localfront:))

### Calculating Node-Relative Transforms (SceneKit Types)

- [class var localRight: SCNVector3](/documentation/scenekit/scnnode/localright)
- [class var localUp: SCNVector3](/documentation/scenekit/scnnode/localup)
- [class var localFront: SCNVector3](/documentation/scenekit/scnnode/localfront)
- [var worldRight: SCNVector3](/documentation/scenekit/scnnode/worldright)
- [var worldUp: SCNVector3](/documentation/scenekit/scnnode/worldup)
- [var worldFront: SCNVector3](/documentation/scenekit/scnnode/worldfront)

### Managing Transforms in World Space (SceneKit Types)

- [var worldTransform: SCNMatrix4](/documentation/scenekit/scnnode/worldtransform)
- [func setWorldTransform(SCNMatrix4)](/documentation/scenekit/scnnode/setworldtransform(_:))
- [var worldOrientation: SCNQuaternion](/documentation/scenekit/scnnode/worldorientation)
- [var worldPosition: SCNVector3](/documentation/scenekit/scnnode/worldposition)

### Converting Between Coordinate Spaces (SceneKit Types)

- [func convertPosition(SCNVector3, from: SCNNode?) -> SCNVector3](/documentation/scenekit/scnnode/convertposition(_:from:))
- [func convertPosition(SCNVector3, to: SCNNode?) -> SCNVector3](/documentation/scenekit/scnnode/convertposition(_:to:))
- [func convertTransform(SCNMatrix4, from: SCNNode?) -> SCNMatrix4](/documentation/scenekit/scnnode/converttransform(_:from:))
- [func convertTransform(SCNMatrix4, to: SCNNode?) -> SCNMatrix4](/documentation/scenekit/scnnode/converttransform(_:to:))
- [func convertVector(SCNVector3, from: SCNNode?) -> SCNVector3](/documentation/scenekit/scnnode/convertvector(_:from:))
- [func convertVector(SCNVector3, to: SCNNode?) -> SCNVector3](/documentation/scenekit/scnnode/convertvector(_:to:))
- [SCNReferenceNode](/documentation/scenekit/scnreferencenode)

### Creating a Reference Node

- [init?(url: URL)](/documentation/scenekit/scnreferencenode/init(url:))

### Loading and Unloading a Reference Node’s Content

- [var referenceURL: URL](/documentation/scenekit/scnreferencenode/referenceurl)
- [var loadingPolicy: SCNReferenceLoadingPolicy](/documentation/scenekit/scnreferencenode/loadingpolicy)
- [func load()](/documentation/scenekit/scnreferencenode/load())
- [var isLoaded: Bool](/documentation/scenekit/scnreferencenode/isloaded)
- [func unload()](/documentation/scenekit/scnreferencenode/unload())

### Constants

- [SCNReferenceLoadingPolicy](/documentation/scenekit/scnreferenceloadingpolicy)

#### Constants

- [case immediate](/documentation/scenekit/scnreferenceloadingpolicy/immediate)
- [case onDemand](/documentation/scenekit/scnreferenceloadingpolicy/ondemand)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnreferenceloadingpolicy/init(rawvalue:))

### Initializers

- [init?(coder: NSCoder)](/documentation/scenekit/scnreferencenode/init(coder:))

## Display and Interactivity

- [SCNSceneRenderer](/documentation/scenekit/scnscenerenderer)

### Presenting a Scene

- [var scene: SCNScene?](/documentation/scenekit/scnscenerenderer/scene)
- [func present(SCNScene, with: SKTransition, incomingPointOfView: SCNNode?, completionHandler: (() -> Void)?)](/documentation/scenekit/scnscenerenderer/present(_:with:incomingpointofview:completionhandler:))

### Managing Scene Display

- [var pointOfView: SCNNode?](/documentation/scenekit/scnscenerenderer/pointofview)
- [var autoenablesDefaultLighting: Bool](/documentation/scenekit/scnscenerenderer/autoenablesdefaultlighting)
- [var isJitteringEnabled: Bool](/documentation/scenekit/scnscenerenderer/isjitteringenabled)
- [var showsStatistics: Bool](/documentation/scenekit/scnscenerenderer/showsstatistics)
- [var debugOptions: SCNDebugOptions](/documentation/scenekit/scnscenerenderer/debugoptions)
- [var renderingAPI: SCNRenderingAPI](/documentation/scenekit/scnscenerenderer/renderingapi)
- [SCNDebugOptions](/documentation/scenekit/scndebugoptions)

#### Debugging Geometry and Animation

- [static var showBoundingBoxes: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showboundingboxes)
- [static var showWireframe: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showwireframe)
- [static var renderAsWireframe: SCNDebugOptions](/documentation/scenekit/scndebugoptions/renderaswireframe)
- [static var showSkeletons: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showskeletons)
- [static var showCreases: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showcreases)
- [static var showConstraints: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showconstraints)

#### Debugging Cameras and Lighting

- [static var showCameras: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showcameras)
- [static var showLightInfluences: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showlightinfluences)
- [static var showLightExtents: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showlightextents)

#### Debugging Physics

- [static var showPhysicsShapes: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showphysicsshapes)
- [static var showPhysicsFields: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showphysicsfields)

#### Initializers

- [init(rawValue: UInt)](/documentation/scenekit/scndebugoptions/init(rawvalue:))

#### Type Properties

- [static let showFeaturePoints: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showfeaturepoints)
- [static let showWorldOrigin: SCNDebugOptions](/documentation/scenekit/scndebugoptions/showworldorigin)
- [SCNRenderingAPI](/documentation/scenekit/scnrenderingapi)

#### Constants

- [case metal](/documentation/scenekit/scnrenderingapi/metal)
- [case openGLES2](/documentation/scenekit/scnrenderingapi/opengles2)
- [case openGLLegacy](/documentation/scenekit/scnrenderingapi/opengllegacy)
- [case openGLCore32](/documentation/scenekit/scnrenderingapi/openglcore32)
- [case openGLCore41](/documentation/scenekit/scnrenderingapi/openglcore41)

#### Initializers

- [init?(rawValue: UInt)](/documentation/scenekit/scnrenderingapi/init(rawvalue:))

### Managing Scene Animation Timing

- [var sceneTime: TimeInterval](/documentation/scenekit/scnscenerenderer/scenetime)
- [var isPlaying: Bool](/documentation/scenekit/scnscenerenderer/isplaying)
- [var loops: Bool](/documentation/scenekit/scnscenerenderer/loops)

### Preloading Renderer Resources

- [func prepare(Any, shouldAbortBlock: (() -> Bool)?) -> Bool](/documentation/scenekit/scnscenerenderer/prepare(_:shouldabortblock:))
- [func prepare([Any], completionHandler: ((Bool) -> Void)?)](/documentation/scenekit/scnscenerenderer/prepare(_:completionhandler:))

### Working With Projected Scene Contents

- [func hitTest(CGPoint, options: [SCNHitTestOption : Any]?) -> [SCNHitTestResult]](/documentation/scenekit/scnscenerenderer/hittest(_:options:))
- [SCNHitTestOption](/documentation/scenekit/scnhittestoption)

#### Options

- [static let backFaceCulling: SCNHitTestOption](/documentation/scenekit/scnhittestoption/backfaceculling)
- [static let boundingBoxOnly: SCNHitTestOption](/documentation/scenekit/scnhittestoption/boundingboxonly)
- [static let categoryBitMask: SCNHitTestOption](/documentation/scenekit/scnhittestoption/categorybitmask)
- [static let clipToZRange: SCNHitTestOption](/documentation/scenekit/scnhittestoption/cliptozrange)
- [static let ignoreChildNodes: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorechildnodes)
- [static let ignoreHiddenNodes: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorehiddennodes)
- [static let rootNode: SCNHitTestOption](/documentation/scenekit/scnhittestoption/rootnode)
- [static let searchMode: SCNHitTestOption](/documentation/scenekit/scnhittestoption/searchmode)
- [SCNHitTestSearchMode](/documentation/scenekit/scnhittestsearchmode)

##### Search Modes

- [case all](/documentation/scenekit/scnhittestsearchmode/all)
- [case any](/documentation/scenekit/scnhittestsearchmode/any)
- [case closest](/documentation/scenekit/scnhittestsearchmode/closest)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnhittestsearchmode/init(rawvalue:))

#### Deprecated

- [static let firstFoundOnly: SCNHitTestOption](/documentation/scenekit/scnhittestoption/firstfoundonly)
- [static let sortResults: SCNHitTestOption](/documentation/scenekit/scnhittestoption/sortresults)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnhittestoption/init(rawvalue:))

#### Type Properties

- [static let ignoreLightArea: SCNHitTestOption](/documentation/scenekit/scnhittestoption/ignorelightarea)
- [func isNode(SCNNode, insideFrustumOf: SCNNode) -> Bool](/documentation/scenekit/scnscenerenderer/isnode(_:insidefrustumof:))
- [func nodesInsideFrustum(of: SCNNode) -> [SCNNode]](/documentation/scenekit/scnscenerenderer/nodesinsidefrustum(of:))
- [func projectPoint(SCNVector3) -> SCNVector3](/documentation/scenekit/scnscenerenderer/projectpoint(_:))
- [func unprojectPoint(SCNVector3) -> SCNVector3](/documentation/scenekit/scnscenerenderer/unprojectpoint(_:))

### Participating in the Scene Rendering Process

- [var delegate: (any SCNSceneRendererDelegate)?](/documentation/scenekit/scnscenerenderer/delegate)

### Customizing Scene Rendering with Metal

- [var currentRenderCommandEncoder: (any MTLRenderCommandEncoder)?](/documentation/scenekit/scnscenerenderer/currentrendercommandencoder)
- [var device: (any MTLDevice)?](/documentation/scenekit/scnscenerenderer/device)
- [var commandQueue: (any MTLCommandQueue)?](/documentation/scenekit/scnscenerenderer/commandqueue)
- [var colorPixelFormat: MTLPixelFormat](/documentation/scenekit/scnscenerenderer/colorpixelformat)
- [var depthPixelFormat: MTLPixelFormat](/documentation/scenekit/scnscenerenderer/depthpixelformat)
- [var stencilPixelFormat: MTLPixelFormat](/documentation/scenekit/scnscenerenderer/stencilpixelformat)

### Customizing Scene Rendering with OpenGL

- [var context: UnsafeMutableRawPointer?](/documentation/scenekit/scnscenerenderer/context)

### Rendering Sprite Kit Content over a Scene

- [var overlaySKScene: SKScene?](/documentation/scenekit/scnscenerenderer/overlayskscene)

### Working With Positional Audio

- [var audioListener: SCNNode?](/documentation/scenekit/scnscenerenderer/audiolistener)
- [var audioEnvironmentNode: AVAudioEnvironmentNode](/documentation/scenekit/scnscenerenderer/audioenvironmentnode)
- [var audioEngine: AVAudioEngine](/documentation/scenekit/scnscenerenderer/audioengine)

### Instance Properties

- [var currentRenderPassDescriptor: MTLRenderPassDescriptor](/documentation/scenekit/scnscenerenderer/currentrenderpassdescriptor)
- [var currentTime: TimeInterval](/documentation/scenekit/scnscenerenderer/currenttime)
- [var currentViewport: CGRect](/documentation/scenekit/scnscenerenderer/currentviewport)
- [var isTemporalAntialiasingEnabled: Bool](/documentation/scenekit/scnscenerenderer/istemporalantialiasingenabled)
- [var usesReverseZ: Bool](/documentation/scenekit/scnscenerenderer/usesreversez)
- [var workingColorSpace: CGColorSpace](/documentation/scenekit/scnscenerenderer/workingcolorspace)
- [SCNSceneRendererDelegate](/documentation/scenekit/scnscenerendererdelegate)

### Adding Custom Logic to the Rendering Loop

- [func renderer(any SCNSceneRenderer, updateAtTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:updateattime:))
- [func renderer(any SCNSceneRenderer, didApplyAnimationsAtTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:didapplyanimationsattime:))
- [func renderer(any SCNSceneRenderer, didSimulatePhysicsAtTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:didsimulatephysicsattime:))

### Rendering Custom Scene Content

- [func renderer(any SCNSceneRenderer, willRenderScene: SCNScene, atTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:willrenderscene:attime:))
- [func renderer(any SCNSceneRenderer, didRenderScene: SCNScene, atTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:didrenderscene:attime:))

### Instance Methods

- [func renderer(any SCNSceneRenderer, didApplyConstraintsAtTime: TimeInterval)](/documentation/scenekit/scnscenerendererdelegate/renderer(_:didapplyconstraintsattime:))
- [SCNLayer](/documentation/scenekit/scnlayer)

### Specifying a Scene

- [var scene: SCNScene?](/documentation/scenekit/scnlayer/scene)
- [SCNRenderer](/documentation/scenekit/scnrenderer)

### Creating a Renderer

- [convenience init(device: (any MTLDevice)?, options: [AnyHashable : Any]?)](/documentation/scenekit/scnrenderer/init(device:options:))
- [convenience init(context: EAGLContext?, options: [AnyHashable : Any]?)](/documentation/scenekit/scnrenderer/init(context:options:))

### Specifying a Scene

- [var scene: SCNScene?](/documentation/scenekit/scnrenderer/scene)

### Managing Animation Timing

- [var nextFrameTime: CFTimeInterval](/documentation/scenekit/scnrenderer/nextframetime)

### Rendering a Scene Using Metal

- [func render(atTime: CFTimeInterval, viewport: CGRect, commandBuffer: any MTLCommandBuffer, passDescriptor: MTLRenderPassDescriptor)](/documentation/scenekit/scnrenderer/render(attime:viewport:commandbuffer:passdescriptor:))

### Rendering a Scene Using OpenGL

- [func render()](/documentation/scenekit/scnrenderer/render())
- [func render(atTime: CFTimeInterval)](/documentation/scenekit/scnrenderer/render(attime:))

### Capturing a Snapshot

- [func snapshot(atTime: CFTimeInterval, with: CGSize, antialiasingMode: SCNAntialiasingMode) -> UIImage](/documentation/scenekit/scnrenderer/snapshot(attime:with:antialiasingmode:))

### Instance Methods

- [func render(withViewport: CGRect, commandBuffer: any MTLCommandBuffer, passDescriptor: MTLRenderPassDescriptor)](/documentation/scenekit/scnrenderer/render(withviewport:commandbuffer:passdescriptor:))
- [func update(atTime: CFTimeInterval)](/documentation/scenekit/scnrenderer/update(attime:))
- [func updateProbes([SCNNode], atTime: CFTimeInterval)](/documentation/scenekit/scnrenderer/updateprobes(_:attime:))
- [SCNHitTestResult](/documentation/scenekit/scnhittestresult)

### Retrieving Information About a Hit-Test Result

- [var node: SCNNode](/documentation/scenekit/scnhittestresult/node)
- [var geometryIndex: Int](/documentation/scenekit/scnhittestresult/geometryindex)
- [var faceIndex: Int](/documentation/scenekit/scnhittestresult/faceindex)
- [var localCoordinates: SCNVector3](/documentation/scenekit/scnhittestresult/localcoordinates)
- [var worldCoordinates: SCNVector3](/documentation/scenekit/scnhittestresult/worldcoordinates)
- [var localNormal: SCNVector3](/documentation/scenekit/scnhittestresult/localnormal)
- [var worldNormal: SCNVector3](/documentation/scenekit/scnhittestresult/worldnormal)
- [var modelTransform: SCNMatrix4](/documentation/scenekit/scnhittestresult/modeltransform)
- [func textureCoordinates(withMappingChannel: Int) -> CGPoint](/documentation/scenekit/scnhittestresult/texturecoordinates(withmappingchannel:))

### Instance Properties

- [var boneNode: SCNNode?](/documentation/scenekit/scnhittestresult/bonenode)
- [var simdLocalCoordinates: simd_float3](/documentation/scenekit/scnhittestresult/simdlocalcoordinates)
- [var simdLocalNormal: simd_float3](/documentation/scenekit/scnhittestresult/simdlocalnormal)
- [var simdModelTransform: simd_float4x4](/documentation/scenekit/scnhittestresult/simdmodeltransform)
- [var simdWorldCoordinates: simd_float3](/documentation/scenekit/scnhittestresult/simdworldcoordinates)
- [var simdWorldNormal: simd_float3](/documentation/scenekit/scnhittestresult/simdworldnormal)

## Lighting, Cameras, and Shading

- [SCNLight](/documentation/scenekit/scnlight)

### Modifying a Light’s Appearance

- [var type: SCNLight.LightType](/documentation/scenekit/scnlight/type)
- [SCNLight.LightType](/documentation/scenekit/scnlight/lighttype)

#### Type Properties

- [static let IES: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/ies)
- [static let ambient: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/ambient)
- [static let directional: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/directional)
- [static let omni: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/omni)
- [static let probe: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/probe)
- [static let spot: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/spot)
- [static let area: SCNLight.LightType](/documentation/scenekit/scnlight/lighttype/area)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnlight/lighttype/init(rawvalue:))
- [var color: Any](/documentation/scenekit/scnlight/color)
- [var temperature: CGFloat](/documentation/scenekit/scnlight/temperature)
- [var intensity: CGFloat](/documentation/scenekit/scnlight/intensity)
- [var sphericalHarmonicsCoefficients: Data](/documentation/scenekit/scnlight/sphericalharmonicscoefficients)

### Managing Light Attributes

- [var name: String?](/documentation/scenekit/scnlight/name)
- [func attribute(forKey: String) -> Any?](/documentation/scenekit/scnlight/attribute(forkey:))
- [func setAttribute(Any?, forKey: String)](/documentation/scenekit/scnlight/setattribute(_:forkey:))
- [Lighting Attribute Keys](/documentation/scenekit/lighting-attribute-keys)

#### Constants

- [let SCNLightAttenuationStartKey: String](/documentation/scenekit/scnlightattenuationstartkey)
- [let SCNLightAttenuationEndKey: String](/documentation/scenekit/scnlightattenuationendkey)
- [let SCNLightAttenuationFalloffExponentKey: String](/documentation/scenekit/scnlightattenuationfalloffexponentkey)
- [let SCNLightSpotInnerAngleKey: String](/documentation/scenekit/scnlightspotinneranglekey)
- [let SCNLightSpotOuterAngleKey: String](/documentation/scenekit/scnlightspotouteranglekey)
- [let SCNLightShadowFarClippingKey: String](/documentation/scenekit/scnlightshadowfarclippingkey)
- [let SCNLightShadowNearClippingKey: String](/documentation/scenekit/scnlightshadownearclippingkey)

### Managing Light Attenuation

- [var attenuationStartDistance: CGFloat](/documentation/scenekit/scnlight/attenuationstartdistance)
- [var attenuationEndDistance: CGFloat](/documentation/scenekit/scnlight/attenuationenddistance)
- [var attenuationFalloffExponent: CGFloat](/documentation/scenekit/scnlight/attenuationfalloffexponent)

### Managing Spotlight Extent

- [var spotInnerAngle: CGFloat](/documentation/scenekit/scnlight/spotinnerangle)
- [var spotOuterAngle: CGFloat](/documentation/scenekit/scnlight/spotouterangle)
- [var gobo: SCNMaterialProperty?](/documentation/scenekit/scnlight/gobo)

### Managing Shadows Cast by the Light

- [var castsShadow: Bool](/documentation/scenekit/scnlight/castsshadow)
- [var shadowRadius: CGFloat](/documentation/scenekit/scnlight/shadowradius)
- [var shadowColor: Any](/documentation/scenekit/scnlight/shadowcolor)
- [var shadowMapSize: CGSize](/documentation/scenekit/scnlight/shadowmapsize)
- [var shadowSampleCount: Int](/documentation/scenekit/scnlight/shadowsamplecount)
- [var shadowMode: SCNShadowMode](/documentation/scenekit/scnlight/shadowmode)
- [SCNShadowMode](/documentation/scenekit/scnshadowmode)

#### Constants

- [case forward](/documentation/scenekit/scnshadowmode/forward)
- [case deferred](/documentation/scenekit/scnshadowmode/deferred)
- [case modulated](/documentation/scenekit/scnshadowmode/modulated)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnshadowmode/init(rawvalue:))
- [var shadowBias: CGFloat](/documentation/scenekit/scnlight/shadowbias)
- [var orthographicScale: CGFloat](/documentation/scenekit/scnlight/orthographicscale)
- [var zFar: CGFloat](/documentation/scenekit/scnlight/zfar)
- [var zNear: CGFloat](/documentation/scenekit/scnlight/znear)

### Choosing Nodes to be Illuminated by the Light

- [var categoryBitMask: Int](/documentation/scenekit/scnlight/categorybitmask)

### Managing Photometric Lights

- [var iesProfileURL: URL?](/documentation/scenekit/scnlight/iesprofileurl)

### Instance Properties

- [var areaExtents: simd_float3](/documentation/scenekit/scnlight/areaextents)
- [var areaPolygonVertices: [NSValue]?](/documentation/scenekit/scnlight/areapolygonvertices)
- [var areaType: SCNLightAreaType](/documentation/scenekit/scnlight/areatype)
- [var automaticallyAdjustsShadowProjection: Bool](/documentation/scenekit/scnlight/automaticallyadjustsshadowprojection)
- [var doubleSided: Bool](/documentation/scenekit/scnlight/doublesided)
- [var drawsArea: Bool](/documentation/scenekit/scnlight/drawsarea)
- [var forcesBackFaceCasters: Bool](/documentation/scenekit/scnlight/forcesbackfacecasters)
- [var maximumShadowDistance: CGFloat](/documentation/scenekit/scnlight/maximumshadowdistance)
- [var parallaxCenterOffset: simd_float3](/documentation/scenekit/scnlight/parallaxcenteroffset)
- [var parallaxCorrectionEnabled: Bool](/documentation/scenekit/scnlight/parallaxcorrectionenabled)
- [var parallaxExtentsFactor: simd_float3](/documentation/scenekit/scnlight/parallaxextentsfactor)
- [var probeEnvironment: SCNMaterialProperty?](/documentation/scenekit/scnlight/probeenvironment)
- [var probeExtents: simd_float3](/documentation/scenekit/scnlight/probeextents)
- [var probeOffset: simd_float3](/documentation/scenekit/scnlight/probeoffset)
- [var probeType: SCNLightProbeType](/documentation/scenekit/scnlight/probetype)
- [var probeUpdateType: SCNLightProbeUpdateType](/documentation/scenekit/scnlight/probeupdatetype)
- [var sampleDistributedShadowMaps: Bool](/documentation/scenekit/scnlight/sampledistributedshadowmaps)
- [var shadowCascadeCount: Int](/documentation/scenekit/scnlight/shadowcascadecount)
- [var shadowCascadeSplittingFactor: CGFloat](/documentation/scenekit/scnlight/shadowcascadesplittingfactor)
- [SCNCamera](/documentation/scenekit/scncamera)

### Managing Camera Attributes

- [var name: String?](/documentation/scenekit/scncamera/name)

### Adjusting Camera Perspective

- [var zNear: Double](/documentation/scenekit/scncamera/znear)
- [var zFar: Double](/documentation/scenekit/scncamera/zfar)
- [var automaticallyAdjustsZRange: Bool](/documentation/scenekit/scncamera/automaticallyadjustszrange)

### Managing Field of View

- [var fieldOfView: CGFloat](/documentation/scenekit/scncamera/fieldofview)
- [var focalLength: CGFloat](/documentation/scenekit/scncamera/focallength)
- [var sensorHeight: CGFloat](/documentation/scenekit/scncamera/sensorheight)
- [var projectionDirection: SCNCameraProjectionDirection](/documentation/scenekit/scncamera/projectiondirection)
- [SCNCameraProjectionDirection](/documentation/scenekit/scncameraprojectiondirection)

#### Projection Directions

- [case vertical](/documentation/scenekit/scncameraprojectiondirection/vertical)
- [case horizontal](/documentation/scenekit/scncameraprojectiondirection/horizontal)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scncameraprojectiondirection/init(rawvalue:))

### Managing the Projection Transform

- [var projectionTransform: SCNMatrix4](/documentation/scenekit/scncamera/projectiontransform)
- [var usesOrthographicProjection: Bool](/documentation/scenekit/scncamera/usesorthographicprojection)
- [var orthographicScale: Double](/documentation/scenekit/scncamera/orthographicscale)

### Choosing Nodes to Be Visible to the Camera

- [var categoryBitMask: Int](/documentation/scenekit/scncamera/categorybitmask)

### Adding Depth-of-Field Effects

- [var wantsDepthOfField: Bool](/documentation/scenekit/scncamera/wantsdepthoffield)
- [var focusDistance: CGFloat](/documentation/scenekit/scncamera/focusdistance)
- [var fStop: CGFloat](/documentation/scenekit/scncamera/fstop)
- [var apertureBladeCount: Int](/documentation/scenekit/scncamera/aperturebladecount)
- [var focalBlurSampleCount: Int](/documentation/scenekit/scncamera/focalblursamplecount)

### Adding Motion Blur Effects

- [var motionBlurIntensity: CGFloat](/documentation/scenekit/scncamera/motionblurintensity)

### Adding High Dynamic Range Effects

- [var wantsHDR: Bool](/documentation/scenekit/scncamera/wantshdr)
- [var exposureOffset: CGFloat](/documentation/scenekit/scncamera/exposureoffset)
- [var averageGray: CGFloat](/documentation/scenekit/scncamera/averagegray)
- [var whitePoint: CGFloat](/documentation/scenekit/scncamera/whitepoint)
- [var minimumExposure: CGFloat](/documentation/scenekit/scncamera/minimumexposure)
- [var maximumExposure: CGFloat](/documentation/scenekit/scncamera/maximumexposure)

### Adding Automatic HDR Exposure Adaptation

- [var wantsExposureAdaptation: Bool](/documentation/scenekit/scncamera/wantsexposureadaptation)
- [var exposureAdaptationBrighteningSpeedFactor: CGFloat](/documentation/scenekit/scncamera/exposureadaptationbrighteningspeedfactor)
- [var exposureAdaptationDarkeningSpeedFactor: CGFloat](/documentation/scenekit/scncamera/exposureadaptationdarkeningspeedfactor)

### Adjusting Rendered Colors

- [var contrast: CGFloat](/documentation/scenekit/scncamera/contrast)
- [var saturation: CGFloat](/documentation/scenekit/scncamera/saturation)
- [var colorGrading: SCNMaterialProperty](/documentation/scenekit/scncamera/colorgrading)

### Adding Stylistic Visual Effects

- [var bloomIntensity: CGFloat](/documentation/scenekit/scncamera/bloomintensity)
- [var bloomThreshold: CGFloat](/documentation/scenekit/scncamera/bloomthreshold)
- [var bloomBlurRadius: CGFloat](/documentation/scenekit/scncamera/bloomblurradius)
- [var colorFringeIntensity: CGFloat](/documentation/scenekit/scncamera/colorfringeintensity)
- [var colorFringeStrength: CGFloat](/documentation/scenekit/scncamera/colorfringestrength)
- [var vignettingIntensity: CGFloat](/documentation/scenekit/scncamera/vignettingintensity)
- [var vignettingPower: CGFloat](/documentation/scenekit/scncamera/vignettingpower)

### Adding Screen-Space Ambient Occlusion

- [var screenSpaceAmbientOcclusionIntensity: CGFloat](/documentation/scenekit/scncamera/screenspaceambientocclusionintensity)
- [var screenSpaceAmbientOcclusionRadius: CGFloat](/documentation/scenekit/scncamera/screenspaceambientocclusionradius)
- [var screenSpaceAmbientOcclusionBias: CGFloat](/documentation/scenekit/scncamera/screenspaceambientocclusionbias)
- [var screenSpaceAmbientOcclusionDepthThreshold: CGFloat](/documentation/scenekit/scncamera/screenspaceambientocclusiondepththreshold)
- [var screenSpaceAmbientOcclusionNormalThreshold: CGFloat](/documentation/scenekit/scncamera/screenspaceambientocclusionnormalthreshold)

### Deprecated

- [var yFov: Double](/documentation/scenekit/scncamera/yfov)
- [var xFov: Double](/documentation/scenekit/scncamera/xfov)
- [var focalDistance: CGFloat](/documentation/scenekit/scncamera/focaldistance)
- [var focalSize: CGFloat](/documentation/scenekit/scncamera/focalsize)
- [var focalBlurRadius: CGFloat](/documentation/scenekit/scncamera/focalblurradius)
- [var aperture: CGFloat](/documentation/scenekit/scncamera/aperture)

### Instance Properties

- [var bloomIterationCount: Int](/documentation/scenekit/scncamera/bloomiterationcount)
- [var bloomIterationSpread: CGFloat](/documentation/scenekit/scncamera/bloomiterationspread)
- [var grainIntensity: CGFloat](/documentation/scenekit/scncamera/grainintensity)
- [var grainIsColored: Bool](/documentation/scenekit/scncamera/grainiscolored)
- [var grainScale: CGFloat](/documentation/scenekit/scncamera/grainscale)
- [var whiteBalanceTemperature: CGFloat](/documentation/scenekit/scncamera/whitebalancetemperature)
- [var whiteBalanceTint: CGFloat](/documentation/scenekit/scncamera/whitebalancetint)

### Instance Methods

- [func projectionTransform(withViewportSize: CGSize) -> SCNMatrix4](/documentation/scenekit/scncamera/projectiontransform(withviewportsize:))
- [SCNMaterial](/documentation/scenekit/scnmaterial)

### Creating a Material

- [var name: String?](/documentation/scenekit/scnmaterial/name)

### Choosing a Shading Model

- [var lightingModel: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.property)
- [SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct)

#### Type Properties

- [static let blinn: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/blinn)
- [static let constant: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/constant)
- [static let lambert: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/lambert)
- [static let phong: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/phong)
- [static let physicallyBased: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/physicallybased)
- [static let shadowOnly: SCNMaterial.LightingModel](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/shadowonly)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnmaterial/lightingmodel-swift.struct/init(rawvalue:))

### Visual Properties for Physically Based Shading

- [var diffuse: SCNMaterialProperty](/documentation/scenekit/scnmaterial/diffuse)
- [var metalness: SCNMaterialProperty](/documentation/scenekit/scnmaterial/metalness)
- [var roughness: SCNMaterialProperty](/documentation/scenekit/scnmaterial/roughness)

### Visual Properties for Special Effects

- [var normal: SCNMaterialProperty](/documentation/scenekit/scnmaterial/normal)
- [var displacement: SCNMaterialProperty](/documentation/scenekit/scnmaterial/displacement)
- [var emission: SCNMaterialProperty](/documentation/scenekit/scnmaterial/emission)
- [var selfIllumination: SCNMaterialProperty](/documentation/scenekit/scnmaterial/selfillumination)
- [var ambientOcclusion: SCNMaterialProperty](/documentation/scenekit/scnmaterial/ambientocclusion)

### Visual Properties for Basic Shading

- [var diffuse: SCNMaterialProperty](/documentation/scenekit/scnmaterial/diffuse)
- [var ambient: SCNMaterialProperty](/documentation/scenekit/scnmaterial/ambient)
- [var specular: SCNMaterialProperty](/documentation/scenekit/scnmaterial/specular)
- [var reflective: SCNMaterialProperty](/documentation/scenekit/scnmaterial/reflective)
- [var multiply: SCNMaterialProperty](/documentation/scenekit/scnmaterial/multiply)
- [var transparent: SCNMaterialProperty](/documentation/scenekit/scnmaterial/transparent)
- [var shininess: CGFloat](/documentation/scenekit/scnmaterial/shininess)
- [var fresnelExponent: CGFloat](/documentation/scenekit/scnmaterial/fresnelexponent)
- [var locksAmbientWithDiffuse: Bool](/documentation/scenekit/scnmaterial/locksambientwithdiffuse)

### Managing Opacity and Blending

- [var transparency: CGFloat](/documentation/scenekit/scnmaterial/transparency)
- [var transparencyMode: SCNTransparencyMode](/documentation/scenekit/scnmaterial/transparencymode)
- [SCNTransparencyMode](/documentation/scenekit/scntransparencymode)

#### Constants

- [case aOne](/documentation/scenekit/scntransparencymode/aone)
- [case rgbZero](/documentation/scenekit/scntransparencymode/rgbzero)

#### Enumeration Cases

- [case dualLayer](/documentation/scenekit/scntransparencymode/duallayer)
- [case singleLayer](/documentation/scenekit/scntransparencymode/singlelayer)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scntransparencymode/init(rawvalue:))

#### Type Properties

- [static var `default`: SCNTransparencyMode](/documentation/scenekit/scntransparencymode/default)
- [var blendMode: SCNBlendMode](/documentation/scenekit/scnmaterial/blendmode)
- [SCNBlendMode](/documentation/scenekit/scnblendmode)

#### Constants

- [case alpha](/documentation/scenekit/scnblendmode/alpha)
- [case add](/documentation/scenekit/scnblendmode/add)
- [case subtract](/documentation/scenekit/scnblendmode/subtract)
- [case multiply](/documentation/scenekit/scnblendmode/multiply)
- [case screen](/documentation/scenekit/scnblendmode/screen)
- [case replace](/documentation/scenekit/scnblendmode/replace)

#### Enumeration Cases

- [case max](/documentation/scenekit/scnblendmode/max)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnblendmode/init(rawvalue:))

### Customizing Rendered Appearance

- [var isLitPerPixel: Bool](/documentation/scenekit/scnmaterial/islitperpixel)
- [var isDoubleSided: Bool](/documentation/scenekit/scnmaterial/isdoublesided)
- [var cullMode: SCNCullMode](/documentation/scenekit/scnmaterial/cullmode)
- [SCNCullMode](/documentation/scenekit/scncullmode)

#### Enumeration Cases

- [case back](/documentation/scenekit/scncullmode/back)
- [case front](/documentation/scenekit/scncullmode/front)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scncullmode/init(rawvalue:))
- [var fillMode: SCNFillMode](/documentation/scenekit/scnmaterial/fillmode)
- [SCNFillMode](/documentation/scenekit/scnfillmode)

#### Enumeration Cases

- [case fill](/documentation/scenekit/scnfillmode/fill)
- [case lines](/documentation/scenekit/scnfillmode/lines)

#### Initializers

- [init?(rawValue: UInt)](/documentation/scenekit/scnfillmode/init(rawvalue:))

### Managing Render Targets

- [var writesToDepthBuffer: Bool](/documentation/scenekit/scnmaterial/writestodepthbuffer)
- [var readsFromDepthBuffer: Bool](/documentation/scenekit/scnmaterial/readsfromdepthbuffer)
- [var colorBufferWriteMask: SCNColorMask](/documentation/scenekit/scnmaterial/colorbufferwritemask)
- [SCNColorMask](/documentation/scenekit/scncolormask)

#### Initializers

- [init(rawValue: Int)](/documentation/scenekit/scncolormask/init(rawvalue:))

#### Type Properties

- [static var all: SCNColorMask](/documentation/scenekit/scncolormask/all)
- [static var alpha: SCNColorMask](/documentation/scenekit/scncolormask/alpha)
- [static var blue: SCNColorMask](/documentation/scenekit/scncolormask/blue)
- [static var green: SCNColorMask](/documentation/scenekit/scncolormask/green)
- [static var red: SCNColorMask](/documentation/scenekit/scncolormask/red)

### Instance Properties

- [var clearCoat: SCNMaterialProperty](/documentation/scenekit/scnmaterial/clearcoat)
- [var clearCoatNormal: SCNMaterialProperty](/documentation/scenekit/scnmaterial/clearcoatnormal)
- [var clearCoatRoughness: SCNMaterialProperty](/documentation/scenekit/scnmaterial/clearcoatroughness)
- [SCNMaterialProperty](/documentation/scenekit/scnmaterialproperty)

### Creating a Material Property

- [convenience init(contents: Any)](/documentation/scenekit/scnmaterialproperty/init(contents:))

### Working with Material Property Contents

- [var contents: Any?](/documentation/scenekit/scnmaterialproperty/contents)
- [var intensity: CGFloat](/documentation/scenekit/scnmaterialproperty/intensity)

### Configuring Texture Mapping Attributes

- [var contentsTransform: SCNMatrix4](/documentation/scenekit/scnmaterialproperty/contentstransform)
- [var wrapS: SCNWrapMode](/documentation/scenekit/scnmaterialproperty/wraps)
- [var wrapT: SCNWrapMode](/documentation/scenekit/scnmaterialproperty/wrapt)
- [SCNWrapMode](/documentation/scenekit/scnwrapmode)

#### Constants

- [case clamp](/documentation/scenekit/scnwrapmode/clamp)
- [case `repeat`](/documentation/scenekit/scnwrapmode/repeat)
- [case clampToBorder](/documentation/scenekit/scnwrapmode/clamptoborder)
- [case mirror](/documentation/scenekit/scnwrapmode/mirror)
- [SCNClamp](/documentation/scenekit/scnclamp)
- [SCNRepeat](/documentation/scenekit/scnrepeat)
- [SCNClampToBorder](/documentation/scenekit/scnclamptoborder)
- [SCNMirror](/documentation/scenekit/scnmirror)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnwrapmode/init(rawvalue:))
- [var minificationFilter: SCNFilterMode](/documentation/scenekit/scnmaterialproperty/minificationfilter)
- [var magnificationFilter: SCNFilterMode](/documentation/scenekit/scnmaterialproperty/magnificationfilter)
- [var mipFilter: SCNFilterMode](/documentation/scenekit/scnmaterialproperty/mipfilter)
- [SCNFilterMode](/documentation/scenekit/scnfiltermode)

#### Constants

- [case none](/documentation/scenekit/scnfiltermode/none)
- [case nearest](/documentation/scenekit/scnfiltermode/nearest)
- [case linear](/documentation/scenekit/scnfiltermode/linear)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnfiltermode/init(rawvalue:))
- [var maxAnisotropy: CGFloat](/documentation/scenekit/scnmaterialproperty/maxanisotropy)
- [var mappingChannel: Int](/documentation/scenekit/scnmaterialproperty/mappingchannel)
- [var borderColor: Any?](/documentation/scenekit/scnmaterialproperty/bordercolor)

### Instance Properties

- [var textureComponents: SCNColorMask](/documentation/scenekit/scnmaterialproperty/texturecomponents)

### Type Methods

- [class func precomputedLightingEnvironmentContents(with: Data) throws -> Any](/documentation/scenekit/scnmaterialproperty/precomputedlightingenvironmentcontents(with:)-2cwpt)
- [class func precomputedLightingEnvironmentContents(with: URL) throws -> Any](/documentation/scenekit/scnmaterialproperty/precomputedlightingenvironmentcontents(with:)-5f6ar)
- [class func precomputedLightingEnvironmentData(forContents: Any, device: (any MTLDevice)?) throws -> Data](/documentation/scenekit/scnmaterialproperty/precomputedlightingenvironmentdata(forcontents:device:))

## Geometry

- [SCNGeometry](/documentation/scenekit/scngeometry)

### Creating a Geometry Object

- [convenience init(sources: [SCNGeometrySource], elements: [SCNGeometryElement]?)](/documentation/scenekit/scngeometry/init(sources:elements:))

### Managing Geometry Attributes

- [var name: String?](/documentation/scenekit/scngeometry/name)
- [SCNBoundingVolume](/documentation/scenekit/scnboundingvolume)

#### Measuring an Object’s Bounding Volume

- [var boundingBox: (min: SCNVector3, max: SCNVector3)](/documentation/scenekit/scnboundingvolume/boundingbox)
- [var boundingSphere: (center: SCNVector3, radius: Float)](/documentation/scenekit/scnboundingvolume/boundingsphere)

### Managing a Geometry’s Materials

- [var materials: [SCNMaterial]](/documentation/scenekit/scngeometry/materials)
- [var firstMaterial: SCNMaterial?](/documentation/scenekit/scngeometry/firstmaterial)
- [func material(named: String) -> SCNMaterial?](/documentation/scenekit/scngeometry/material(named:))
- [func insertMaterial(SCNMaterial, at: Int)](/documentation/scenekit/scngeometry/insertmaterial(_:at:))
- [func removeMaterial(at: Int)](/documentation/scenekit/scngeometry/removematerial(at:))
- [func replaceMaterial(at: Int, with: SCNMaterial)](/documentation/scenekit/scngeometry/replacematerial(at:with:))

### Managing Geometry Data

- [var elements: [SCNGeometryElement]](/documentation/scenekit/scngeometry/elements)
- [var sources: [SCNGeometrySource]](/documentation/scenekit/scngeometry/sources)
- [var elementCount: Int](/documentation/scenekit/scngeometry/elementcount)
- [func element(at: Int) -> SCNGeometryElement](/documentation/scenekit/scngeometry/element(at:))
- [func sources(for: SCNGeometrySource.Semantic) -> [SCNGeometrySource]](/documentation/scenekit/scngeometry/sources(for:))

### Optimizing Level of Detail

- [var levelsOfDetail: [SCNLevelOfDetail]?](/documentation/scenekit/scngeometry/levelsofdetail)
- [SCNLevelOfDetail](/documentation/scenekit/scnlevelofdetail)

#### Creating a Level of Detail

- [convenience init(geometry: SCNGeometry?, screenSpaceRadius: CGFloat)](/documentation/scenekit/scnlevelofdetail/init(geometry:screenspaceradius:))
- [convenience init(geometry: SCNGeometry?, worldSpaceDistance: CGFloat)](/documentation/scenekit/scnlevelofdetail/init(geometry:worldspacedistance:))

#### Inspecting a Level of Detail

- [var geometry: SCNGeometry?](/documentation/scenekit/scnlevelofdetail/geometry)
- [var screenSpaceRadius: CGFloat](/documentation/scenekit/scnlevelofdetail/screenspaceradius)
- [var worldSpaceDistance: CGFloat](/documentation/scenekit/scnlevelofdetail/worldspacedistance)

### Smoothing and Subdividing Geometry

- [var subdivisionLevel: Int](/documentation/scenekit/scngeometry/subdivisionlevel)
- [var edgeCreasesElement: SCNGeometryElement?](/documentation/scenekit/scngeometry/edgecreaseselement)
- [var edgeCreasesSource: SCNGeometrySource?](/documentation/scenekit/scngeometry/edgecreasessource)
- [var wantsAdaptiveSubdivision: Bool](/documentation/scenekit/scngeometry/wantsadaptivesubdivision)

### Managing Tessellation

- [var tessellator: SCNGeometryTessellator?](/documentation/scenekit/scngeometry/tessellator)
- [SCNGeometryTessellator](/documentation/scenekit/scngeometrytessellator)

#### Choosing a Smoothing Algorithm

- [var smoothingMode: SCNTessellationSmoothingMode](/documentation/scenekit/scngeometrytessellator/smoothingmode)
- [SCNTessellationSmoothingMode](/documentation/scenekit/scntessellationsmoothingmode)

##### Enumeration Cases

- [case none](/documentation/scenekit/scntessellationsmoothingmode/none)
- [case phong](/documentation/scenekit/scntessellationsmoothingmode/phong)
- [case pnTriangles](/documentation/scenekit/scntessellationsmoothingmode/pntriangles)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scntessellationsmoothingmode/init(rawvalue:))

#### Instance Properties

- [var edgeTessellationFactor: CGFloat](/documentation/scenekit/scngeometrytessellator/edgetessellationfactor)
- [var insideTessellationFactor: CGFloat](/documentation/scenekit/scngeometrytessellator/insidetessellationfactor)
- [var isAdaptive: Bool](/documentation/scenekit/scngeometrytessellator/isadaptive)
- [var isScreenSpace: Bool](/documentation/scenekit/scngeometrytessellator/isscreenspace)
- [var maximumEdgeLength: CGFloat](/documentation/scenekit/scngeometrytessellator/maximumedgelength)
- [var tessellationFactorScale: CGFloat](/documentation/scenekit/scngeometrytessellator/tessellationfactorscale)
- [var tessellationPartitionMode: MTLTessellationPartitionMode](/documentation/scenekit/scngeometrytessellator/tessellationpartitionmode)

### Initializers

- [convenience init(sources: [SCNGeometrySource], elements: [SCNGeometryElement]?, sourceChannels: [NSNumber]?)](/documentation/scenekit/scngeometry/init(sources:elements:sourcechannels:))

### Instance Properties

- [var geometrySourceChannels: [NSNumber]?](/documentation/scenekit/scngeometry/geometrysourcechannels)
- [SCNGeometrySource](/documentation/scenekit/scngeometrysource)

### Creating Geometry Sources

- [convenience init(data: Data, semantic: SCNGeometrySource.Semantic, vectorCount: Int, usesFloatComponents: Bool, componentsPerVector: Int, bytesPerComponent: Int, dataOffset: Int, dataStride: Int)](/documentation/scenekit/scngeometrysource/init(data:semantic:vectorcount:usesfloatcomponents:componentspervector:bytespercomponent:dataoffset:datastride:))
- [convenience init(vertices: [SCNVector3])](/documentation/scenekit/scngeometrysource/init(vertices:))
- [convenience init(normals: [SCNVector3])](/documentation/scenekit/scngeometrysource/init(normals:))
- [convenience init(textureCoordinates: [CGPoint])](/documentation/scenekit/scngeometrysource/init(texturecoordinates:))

### Inspecting a Geometry Source

- [var data: Data](/documentation/scenekit/scngeometrysource/data)
- [var semantic: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.property)
- [var vectorCount: Int](/documentation/scenekit/scngeometrysource/vectorcount)
- [var usesFloatComponents: Bool](/documentation/scenekit/scngeometrysource/usesfloatcomponents)
- [var componentsPerVector: Int](/documentation/scenekit/scngeometrysource/componentspervector)
- [var bytesPerComponent: Int](/documentation/scenekit/scngeometrysource/bytespercomponent)
- [var dataOffset: Int](/documentation/scenekit/scngeometrysource/dataoffset)
- [var dataStride: Int](/documentation/scenekit/scngeometrysource/datastride)

### Creating GPU-Mutable Geometry Sources

- [convenience init(buffer: any MTLBuffer, vertexFormat: MTLVertexFormat, semantic: SCNGeometrySource.Semantic, vertexCount: Int, dataOffset: Int, dataStride: Int)](/documentation/scenekit/scngeometrysource/init(buffer:vertexformat:semantic:vertexcount:dataoffset:datastride:))

### Geometry Source Semantics

- [SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct)

#### Basic Geometry Semantics

- [static let vertex: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/vertex)
- [static let normal: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/normal)
- [static let texcoord: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/texcoord)

#### Advanced Shading Semantics

- [static let color: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/color)
- [static let tangent: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/tangent)

#### Surface Subdivision Semantics

- [static let edgeCrease: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/edgecrease)
- [static let vertexCrease: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/vertexcrease)

#### Skeletal Animation Semantics

- [static let boneIndices: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/boneindices)
- [static let boneWeights: SCNGeometrySource.Semantic](/documentation/scenekit/scngeometrysource/semantic-swift.struct/boneweights)

#### Initializers

- [init(String)](/documentation/scenekit/scngeometrysource/semantic-swift.struct/init(_:))
- [init(rawValue: String)](/documentation/scenekit/scngeometrysource/semantic-swift.struct/init(rawvalue:))
- [SCNGeometryElement](/documentation/scenekit/scngeometryelement)

### Creating a Geometry Element

- [convenience init<IndexType>(indices: [IndexType], primitiveType: SCNGeometryPrimitiveType)](/documentation/scenekit/scngeometryelement/init(indices:primitivetype:))
- [convenience init(data: Data?, primitiveType: SCNGeometryPrimitiveType, primitiveCount: Int, bytesPerIndex: Int)](/documentation/scenekit/scngeometryelement/init(data:primitivetype:primitivecount:bytesperindex:))

### Working with Indexes

- [var data: Data](/documentation/scenekit/scngeometryelement/data)
- [var bytesPerIndex: Int](/documentation/scenekit/scngeometryelement/bytesperindex)
- [var primitiveType: SCNGeometryPrimitiveType](/documentation/scenekit/scngeometryelement/primitivetype)
- [SCNGeometryPrimitiveType](/documentation/scenekit/scngeometryprimitivetype)

#### Constants

- [case triangles](/documentation/scenekit/scngeometryprimitivetype/triangles)
- [case triangleStrip](/documentation/scenekit/scngeometryprimitivetype/trianglestrip)
- [case line](/documentation/scenekit/scngeometryprimitivetype/line)
- [case point](/documentation/scenekit/scngeometryprimitivetype/point)

#### Enumeration Cases

- [case polygon](/documentation/scenekit/scngeometryprimitivetype/polygon)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scngeometryprimitivetype/init(rawvalue:))
- [var primitiveCount: Int](/documentation/scenekit/scngeometryelement/primitivecount)
- [var primitiveRange: NSRange](/documentation/scenekit/scngeometryelement/primitiverange)

### Rendering Point Clouds

- [var pointSize: CGFloat](/documentation/scenekit/scngeometryelement/pointsize)
- [var minimumPointScreenSpaceRadius: CGFloat](/documentation/scenekit/scngeometryelement/minimumpointscreenspaceradius)
- [var maximumPointScreenSpaceRadius: CGFloat](/documentation/scenekit/scngeometryelement/maximumpointscreenspaceradius)

### Initializers

- [convenience init(buffer: any MTLBuffer, primitiveType: SCNGeometryPrimitiveType, primitiveCount: Int, bytesPerIndex: Int)](/documentation/scenekit/scngeometryelement/init(buffer:primitivetype:primitivecount:bytesperindex:))
- [convenience init(buffer: any MTLBuffer, primitiveType: SCNGeometryPrimitiveType, primitiveCount: Int, indicesChannelCount: Int, interleavedIndicesChannels: Bool, bytesPerIndex: Int)](/documentation/scenekit/scngeometryelement/init(buffer:primitivetype:primitivecount:indiceschannelcount:interleavedindiceschannels:bytesperindex:))
- [convenience init(data: Data?, primitiveType: SCNGeometryPrimitiveType, primitiveCount: Int, indicesChannelCount: Int, interleavedIndicesChannels: Bool, bytesPerIndex: Int)](/documentation/scenekit/scngeometryelement/init(data:primitivetype:primitivecount:indiceschannelcount:interleavedindiceschannels:bytesperindex:))

### Instance Properties

- [var hasInterleavedIndicesChannels: Bool](/documentation/scenekit/scngeometryelement/hasinterleavedindiceschannels)
- [var indicesChannelCount: Int](/documentation/scenekit/scngeometryelement/indiceschannelcount)
- [Built-in Geometry Types](/documentation/scenekit/built-in-geometry-types)

### Parametric Geometry

- [SCNText](/documentation/scenekit/scntext)

#### Creating a Text Geometry

- [convenience init(string: Any?, extrusionDepth: CGFloat)](/documentation/scenekit/scntext/init(string:extrusiondepth:))

#### Managing the Geometry’s Text Content

- [var string: Any?](/documentation/scenekit/scntext/string)
- [var font: UIFont!](/documentation/scenekit/scntext/font)

#### Managing Text Layout

- [var containerFrame: CGRect](/documentation/scenekit/scntext/containerframe)
- [var isWrapped: Bool](/documentation/scenekit/scntext/iswrapped)
- [var alignmentMode: String](/documentation/scenekit/scntext/alignmentmode)
- [var truncationMode: String](/documentation/scenekit/scntext/truncationmode)
- [var textSize: CGSize](/documentation/scenekit/scntext/textsize)

#### Managing the Text’s 3D Representation

- [var flatness: CGFloat](/documentation/scenekit/scntext/flatness)
- [var extrusionDepth: CGFloat](/documentation/scenekit/scntext/extrusiondepth)
- [var chamferRadius: CGFloat](/documentation/scenekit/scntext/chamferradius)
- [var chamferProfile: UIBezierPath?](/documentation/scenekit/scntext/chamferprofile)
- [SCNShape](/documentation/scenekit/scnshape)

#### Creating a Shape

- [convenience init(path: UIBezierPath?, extrusionDepth: CGFloat)](/documentation/scenekit/scnshape/init(path:extrusiondepth:))

#### Modifying a Shape

- [var extrusionDepth: CGFloat](/documentation/scenekit/scnshape/extrusiondepth)
- [var path: UIBezierPath?](/documentation/scenekit/scnshape/path)

#### Chamfering a Shape

- [var chamferMode: SCNChamferMode](/documentation/scenekit/scnshape/chamfermode)
- [SCNChamferMode](/documentation/scenekit/scnchamfermode)

##### Constants

- [case both](/documentation/scenekit/scnchamfermode/both)
- [case front](/documentation/scenekit/scnchamfermode/front)
- [case back](/documentation/scenekit/scnchamfermode/back)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnchamfermode/init(rawvalue:))
- [var chamferProfile: UIBezierPath?](/documentation/scenekit/scnshape/chamferprofile)
- [var chamferRadius: CGFloat](/documentation/scenekit/scnshape/chamferradius)

### Basic Shapes

- [SCNFloor](/documentation/scenekit/scnfloor)

#### Adding Reflections to a Floor

- [var reflectivity: CGFloat](/documentation/scenekit/scnfloor/reflectivity)
- [var reflectionFalloffEnd: CGFloat](/documentation/scenekit/scnfloor/reflectionfalloffend)
- [var reflectionFalloffStart: CGFloat](/documentation/scenekit/scnfloor/reflectionfalloffstart)
- [var reflectionResolutionScaleFactor: CGFloat](/documentation/scenekit/scnfloor/reflectionresolutionscalefactor)
- [var reflectionCategoryBitMask: Int](/documentation/scenekit/scnfloor/reflectioncategorybitmask)

#### Adjusting a Floor’s Size

- [var width: CGFloat](/documentation/scenekit/scnfloor/width)
- [var length: CGFloat](/documentation/scenekit/scnfloor/length)
- [SCNBox](/documentation/scenekit/scnbox)

#### Creating a Box

- [convenience init(width: CGFloat, height: CGFloat, length: CGFloat, chamferRadius: CGFloat)](/documentation/scenekit/scnbox/init(width:height:length:chamferradius:))

#### Adjusting a Box’s Dimensions

- [var width: CGFloat](/documentation/scenekit/scnbox/width)
- [var height: CGFloat](/documentation/scenekit/scnbox/height)
- [var length: CGFloat](/documentation/scenekit/scnbox/length)

#### Configuring Box Properties

- [var widthSegmentCount: Int](/documentation/scenekit/scnbox/widthsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scnbox/heightsegmentcount)
- [var lengthSegmentCount: Int](/documentation/scenekit/scnbox/lengthsegmentcount)

#### Adding Rounded Edges and Corners

- [var chamferRadius: CGFloat](/documentation/scenekit/scnbox/chamferradius)
- [var chamferSegmentCount: Int](/documentation/scenekit/scnbox/chamfersegmentcount)
- [SCNCapsule](/documentation/scenekit/scncapsule)

#### Creating a Capsule

- [convenience init(capRadius: CGFloat, height: CGFloat)](/documentation/scenekit/scncapsule/init(capradius:height:))

#### Adjusting a Capsule’s Dimensions

- [var capRadius: CGFloat](/documentation/scenekit/scncapsule/capradius)
- [var height: CGFloat](/documentation/scenekit/scncapsule/height)

#### Adjusting Geometric Detail

- [var radialSegmentCount: Int](/documentation/scenekit/scncapsule/radialsegmentcount)
- [var capSegmentCount: Int](/documentation/scenekit/scncapsule/capsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scncapsule/heightsegmentcount)
- [SCNCone](/documentation/scenekit/scncone)

#### Creating a Cone

- [convenience init(topRadius: CGFloat, bottomRadius: CGFloat, height: CGFloat)](/documentation/scenekit/scncone/init(topradius:bottomradius:height:))

#### Adjusting a Cone’s Dimensions

- [var topRadius: CGFloat](/documentation/scenekit/scncone/topradius)
- [var bottomRadius: CGFloat](/documentation/scenekit/scncone/bottomradius)
- [var height: CGFloat](/documentation/scenekit/scncone/height)

#### Adjusting Geometric Detail

- [var radialSegmentCount: Int](/documentation/scenekit/scncone/radialsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scncone/heightsegmentcount)
- [SCNCylinder](/documentation/scenekit/scncylinder)

#### Creating a Cylinder

- [convenience init(radius: CGFloat, height: CGFloat)](/documentation/scenekit/scncylinder/init(radius:height:))

#### Adjusting a Cylinder’s Dimensions

- [var radius: CGFloat](/documentation/scenekit/scncylinder/radius)
- [var height: CGFloat](/documentation/scenekit/scncylinder/height)

#### Adjusting Geometric Detail

- [var radialSegmentCount: Int](/documentation/scenekit/scncylinder/radialsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scncylinder/heightsegmentcount)
- [SCNPlane](/documentation/scenekit/scnplane)

#### Creating a Plane

- [convenience init(width: CGFloat, height: CGFloat)](/documentation/scenekit/scnplane/init(width:height:))

#### Adjusting a Plane’s Dimensions

- [var width: CGFloat](/documentation/scenekit/scnplane/width)
- [var height: CGFloat](/documentation/scenekit/scnplane/height)

#### Adjusting Geometric Detail

- [var widthSegmentCount: Int](/documentation/scenekit/scnplane/widthsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scnplane/heightsegmentcount)

#### Adding Rounded Corners

- [var cornerRadius: CGFloat](/documentation/scenekit/scnplane/cornerradius)
- [var cornerSegmentCount: Int](/documentation/scenekit/scnplane/cornersegmentcount)
- [SCNPyramid](/documentation/scenekit/scnpyramid)

#### Creating a Pyramid

- [convenience init(width: CGFloat, height: CGFloat, length: CGFloat)](/documentation/scenekit/scnpyramid/init(width:height:length:))

#### Adjusting a Pyramid’s Dimensions

- [var width: CGFloat](/documentation/scenekit/scnpyramid/width)
- [var height: CGFloat](/documentation/scenekit/scnpyramid/height)
- [var length: CGFloat](/documentation/scenekit/scnpyramid/length)

#### Adjusting Geometric Detail

- [var widthSegmentCount: Int](/documentation/scenekit/scnpyramid/widthsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scnpyramid/heightsegmentcount)
- [var lengthSegmentCount: Int](/documentation/scenekit/scnpyramid/lengthsegmentcount)
- [SCNSphere](/documentation/scenekit/scnsphere)

#### Creating a Sphere

- [convenience init(radius: CGFloat)](/documentation/scenekit/scnsphere/init(radius:))

#### Adjusting a Sphere’s Dimensions

- [var radius: CGFloat](/documentation/scenekit/scnsphere/radius)

#### Adjusting Geometric Detail

- [var isGeodesic: Bool](/documentation/scenekit/scnsphere/isgeodesic)
- [var segmentCount: Int](/documentation/scenekit/scnsphere/segmentcount)
- [SCNTorus](/documentation/scenekit/scntorus)

#### Creating a Torus

- [convenience init(ringRadius: CGFloat, pipeRadius: CGFloat)](/documentation/scenekit/scntorus/init(ringradius:piperadius:))

#### Adjusting a Torus’ Dimensions

- [var ringRadius: CGFloat](/documentation/scenekit/scntorus/ringradius)
- [var pipeRadius: CGFloat](/documentation/scenekit/scntorus/piperadius)

#### Configuring Torus Properties

- [var ringSegmentCount: Int](/documentation/scenekit/scntorus/ringsegmentcount)
- [var pipeSegmentCount: Int](/documentation/scenekit/scntorus/pipesegmentcount)
- [SCNTube](/documentation/scenekit/scntube)

#### Creating a Tube

- [convenience init(innerRadius: CGFloat, outerRadius: CGFloat, height: CGFloat)](/documentation/scenekit/scntube/init(innerradius:outerradius:height:))

#### Adjusting a Tube’s Dimensions

- [var outerRadius: CGFloat](/documentation/scenekit/scntube/outerradius)
- [var innerRadius: CGFloat](/documentation/scenekit/scntube/innerradius)
- [var height: CGFloat](/documentation/scenekit/scntube/height)

#### Adjusting Geometric Detail

- [var radialSegmentCount: Int](/documentation/scenekit/scntube/radialsegmentcount)
- [var heightSegmentCount: Int](/documentation/scenekit/scntube/heightsegmentcount)

## Animation and Constraints

- [Animation](/documentation/scenekit/animation)

### First Steps

- [Animating SceneKit Content](/documentation/scenekit/animating-scenekit-content)

### Actions

- [SCNAction](/documentation/scenekit/scnaction)

#### Creating Actions That Move a Node

- [class func moveBy(x: CGFloat, y: CGFloat, z: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/moveby(x:y:z:duration:))
- [class func move(by: SCNVector3, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/move(by:duration:))
- [class func move(to: SCNVector3, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/move(to:duration:))

#### Creating Actions That Rotate a Node

- [class func rotateBy(x: CGFloat, y: CGFloat, z: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/rotateby(x:y:z:duration:))
- [class func rotateTo(x: CGFloat, y: CGFloat, z: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/rotateto(x:y:z:duration:))
- [class func rotateTo(x: CGFloat, y: CGFloat, z: CGFloat, duration: TimeInterval, usesShortestUnitArc: Bool) -> SCNAction](/documentation/scenekit/scnaction/rotateto(x:y:z:duration:usesshortestunitarc:))
- [class func rotate(by: CGFloat, around: SCNVector3, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/rotate(by:around:duration:))
- [class func rotate(toAxisAngle: SCNVector4, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/rotate(toaxisangle:duration:))

#### Creating Actions That Change a Node’s Scale

- [class func scale(by: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/scale(by:duration:))
- [class func scale(to: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/scale(to:duration:))

#### Creating Actions That Change a Node’s Opacity

- [class func fadeIn(duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/fadein(duration:))
- [class func fadeOut(duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/fadeout(duration:))
- [class func fadeOpacity(by: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/fadeopacity(by:duration:))
- [class func fadeOpacity(to: CGFloat, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/fadeopacity(to:duration:))

#### Creating Actions That Change a Node’s Visibility

- [class func hide() -> SCNAction](/documentation/scenekit/scnaction/hide())
- [class func unhide() -> SCNAction](/documentation/scenekit/scnaction/unhide())

#### Creating Actions That Remove Nodes from the Scene

- [class func removeFromParentNode() -> SCNAction](/documentation/scenekit/scnaction/removefromparentnode())

#### Creating Actions That Play Audio

- [class func playAudio(SCNAudioSource, waitForCompletion: Bool) -> SCNAction](/documentation/scenekit/scnaction/playaudio(_:waitforcompletion:))

#### Creating Actions That Combine or Repeat Other Actions

- [class func group([SCNAction]) -> SCNAction](/documentation/scenekit/scnaction/group(_:))
- [class func sequence([SCNAction]) -> SCNAction](/documentation/scenekit/scnaction/sequence(_:))
- [class func `repeat`(SCNAction, count: Int) -> SCNAction](/documentation/scenekit/scnaction/repeat(_:count:))
- [class func repeatForever(SCNAction) -> SCNAction](/documentation/scenekit/scnaction/repeatforever(_:))

#### Creating Actions That Add Delays to Action Sequences

- [class func wait(duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/wait(duration:))
- [class func wait(duration: TimeInterval, withRange: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/wait(duration:withrange:))

#### Creating Custom Actions

- [class func run((SCNNode) -> Void) -> SCNAction](/documentation/scenekit/scnaction/run(_:))
- [class func run((SCNNode) -> Void, queue: dispatch_queue_t) -> SCNAction](/documentation/scenekit/scnaction/run(_:queue:))
- [class func customAction(duration: TimeInterval, action: (SCNNode, CGFloat) -> Void) -> SCNAction](/documentation/scenekit/scnaction/customaction(duration:action:))
- [class func javaScriptAction(withScript: String, duration: TimeInterval) -> SCNAction](/documentation/scenekit/scnaction/javascriptaction(withscript:duration:))

#### Reversing an Action

- [func reversed() -> SCNAction](/documentation/scenekit/scnaction/reversed())

#### Adjusting an Action’s Animation Properties

- [var duration: TimeInterval](/documentation/scenekit/scnaction/duration)
- [var speed: CGFloat](/documentation/scenekit/scnaction/speed)
- [var timingMode: SCNActionTimingMode](/documentation/scenekit/scnaction/timingmode)
- [var timingFunction: SCNActionTimingFunction?](/documentation/scenekit/scnaction/timingfunction)

#### Constants

- [SCNActionTimingMode](/documentation/scenekit/scnactiontimingmode)

##### Constants

- [case linear](/documentation/scenekit/scnactiontimingmode/linear)
- [case easeIn](/documentation/scenekit/scnactiontimingmode/easein)
- [case easeOut](/documentation/scenekit/scnactiontimingmode/easeout)
- [case easeInEaseOut](/documentation/scenekit/scnactiontimingmode/easeineaseout)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnactiontimingmode/init(rawvalue:))
- [SCNActionTimingFunction](/documentation/scenekit/scnactiontimingfunction)
- [SCNActionable](/documentation/scenekit/scnactionable)

#### Running Actions

- [func runAction(SCNAction)](/documentation/scenekit/scnactionable/runaction(_:))
- [func runAction(SCNAction, completionHandler: (() -> Void)?)](/documentation/scenekit/scnactionable/runaction(_:completionhandler:))
- [func runAction(SCNAction, forKey: String?)](/documentation/scenekit/scnactionable/runaction(_:forkey:))
- [func runAction(SCNAction, forKey: String?, completionHandler: (() -> Void)?)](/documentation/scenekit/scnactionable/runaction(_:forkey:completionhandler:))

#### Inspecting a Node’s Running Actions

- [func action(forKey: String) -> SCNAction?](/documentation/scenekit/scnactionable/action(forkey:))
- [var hasActions: Bool](/documentation/scenekit/scnactionable/hasactions)
- [var actionKeys: [String]](/documentation/scenekit/scnactionable/actionkeys)

#### Canceling a Node’s Running Actions

- [func removeAction(forKey: String)](/documentation/scenekit/scnactionable/removeaction(forkey:))
- [func removeAllActions()](/documentation/scenekit/scnactionable/removeallactions())

### Implicit Animation

- [SCNTransaction](/documentation/scenekit/scntransaction)

#### Creating and Committing Transactions

- [class func begin()](/documentation/scenekit/scntransaction/begin())
- [class func commit()](/documentation/scenekit/scntransaction/commit())
- [class func flush()](/documentation/scenekit/scntransaction/flush())

#### Overriding Animation Duration and Timing

- [class var animationDuration: CFTimeInterval](/documentation/scenekit/scntransaction/animationduration)
- [class var animationTimingFunction: CAMediaTimingFunction?](/documentation/scenekit/scntransaction/animationtimingfunction)

#### Temporarily Disabling Property Animations

- [class var disableActions: Bool](/documentation/scenekit/scntransaction/disableactions)

#### Getting and Setting Completion Block Objects

- [class var completionBlock: (() -> Void)?](/documentation/scenekit/scntransaction/completionblock)

#### Managing Concurrency

- [class func lock()](/documentation/scenekit/scntransaction/lock())
- [class func unlock()](/documentation/scenekit/scntransaction/unlock())

#### Getting and Setting Transaction Properties

- [class func setValue(Any?, forKey: String)](/documentation/scenekit/scntransaction/setvalue(_:forkey:))
- [class func value(forKey: String) -> Any?](/documentation/scenekit/scntransaction/value(forkey:))

### Explicit Animation

- [SCNAnimatable](/documentation/scenekit/scnanimatable)

#### Managing Animations

- [func addAnimation(any SCNAnimationProtocol, forKey: String?)](/documentation/scenekit/scnanimatable/addanimation(_:forkey:))
- [func animation(forKey: String) -> CAAnimation?](/documentation/scenekit/scnanimatable/animation(forkey:))
- [var animationKeys: [String]](/documentation/scenekit/scnanimatable/animationkeys)
- [func removeAllAnimations()](/documentation/scenekit/scnanimatable/removeallanimations())
- [func removeAnimation(forKey: String)](/documentation/scenekit/scnanimatable/removeanimation(forkey:))
- [func removeAnimation(forKey: String, fadeOutDuration: CGFloat)](/documentation/scenekit/scnanimatable/removeanimation(forkey:fadeoutduration:))

#### Pausing and Resuming Animations

- [func pauseAnimation(forKey: String)](/documentation/scenekit/scnanimatable/pauseanimation(forkey:))
- [func resumeAnimation(forKey: String)](/documentation/scenekit/scnanimatable/resumeanimation(forkey:))
- [func isAnimationPaused(forKey: String) -> Bool](/documentation/scenekit/scnanimatable/isanimationpaused(forkey:))

#### Instance Methods

- [func addAnimationPlayer(SCNAnimationPlayer, forKey: String?)](/documentation/scenekit/scnanimatable/addanimationplayer(_:forkey:))
- [func animationPlayer(forKey: String) -> SCNAnimationPlayer?](/documentation/scenekit/scnanimatable/animationplayer(forkey:))
- [func removeAllAnimations(withBlendOutDuration: CGFloat)](/documentation/scenekit/scnanimatable/removeallanimations(withblendoutduration:))
- [func removeAnimation(forKey: String, blendOutDuration: CGFloat)](/documentation/scenekit/scnanimatable/removeanimation(forkey:blendoutduration:))
- [func setAnimationSpeed(CGFloat, forKey: String)](/documentation/scenekit/scnanimatable/setanimationspeed(_:forkey:))
- [SCNAnimationEvent](/documentation/scenekit/scnanimationevent)

#### Creating an Animation Event

- [convenience init(keyTime: CGFloat, block: SCNAnimationEventBlock)](/documentation/scenekit/scnanimationevent/init(keytime:block:))

#### Constants

- [SCNAnimationEventBlock](/documentation/scenekit/scnanimationeventblock)
- [SCNAnimation](/documentation/scenekit/scnanimation-swift.class)

#### Supporting Types

- [SCNAnimationDidStartBlock](/documentation/scenekit/scnanimationdidstartblock)
- [SCNAnimationDidStopBlock](/documentation/scenekit/scnanimationdidstopblock)

#### Initializers

- [init(caAnimation: CAAnimation)](/documentation/scenekit/scnanimation-swift.class/init(caanimation:))
- [init(contentsOf: URL)](/documentation/scenekit/scnanimation-swift.class/init(contentsof:))
- [init(named: String)](/documentation/scenekit/scnanimation-swift.class/init(named:))

#### Instance Properties

- [var animationDidStart: SCNAnimationDidStartBlock?](/documentation/scenekit/scnanimation-swift.class/animationdidstart)
- [var animationDidStop: SCNAnimationDidStopBlock?](/documentation/scenekit/scnanimation-swift.class/animationdidstop)
- [var animationEvents: [SCNAnimationEvent]?](/documentation/scenekit/scnanimation-swift.class/animationevents)
- [var autoreverses: Bool](/documentation/scenekit/scnanimation-swift.class/autoreverses)
- [var blendInDuration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/blendinduration)
- [var blendOutDuration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/blendoutduration)
- [var duration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/duration)
- [var fillsBackward: Bool](/documentation/scenekit/scnanimation-swift.class/fillsbackward)
- [var fillsForward: Bool](/documentation/scenekit/scnanimation-swift.class/fillsforward)
- [var isAdditive: Bool](/documentation/scenekit/scnanimation-swift.class/isadditive)
- [var isAppliedOnCompletion: Bool](/documentation/scenekit/scnanimation-swift.class/isappliedoncompletion)
- [var isCumulative: Bool](/documentation/scenekit/scnanimation-swift.class/iscumulative)
- [var isRemovedOnCompletion: Bool](/documentation/scenekit/scnanimation-swift.class/isremovedoncompletion)
- [var keyPath: String?](/documentation/scenekit/scnanimation-swift.class/keypath)
- [var repeatCount: CGFloat](/documentation/scenekit/scnanimation-swift.class/repeatcount)
- [var startDelay: TimeInterval](/documentation/scenekit/scnanimation-swift.class/startdelay)
- [var timeOffset: TimeInterval](/documentation/scenekit/scnanimation-swift.class/timeoffset)
- [var timingFunction: SCNTimingFunction](/documentation/scenekit/scnanimation-swift.class/timingfunction)
- [var usesSceneTimeBase: Bool](/documentation/scenekit/scnanimation-swift.class/usesscenetimebase)
- [SCNAnimationPlayer](/documentation/scenekit/scnanimationplayer)

#### Initializers

- [init(animation: SCNAnimation)](/documentation/scenekit/scnanimationplayer/init(animation:))

#### Instance Properties

- [var animation: SCNAnimation](/documentation/scenekit/scnanimationplayer/animation)
- [var blendFactor: CGFloat](/documentation/scenekit/scnanimationplayer/blendfactor)
- [var paused: Bool](/documentation/scenekit/scnanimationplayer/paused)
- [var speed: CGFloat](/documentation/scenekit/scnanimationplayer/speed)

#### Instance Methods

- [func play()](/documentation/scenekit/scnanimationplayer/play())
- [func stop()](/documentation/scenekit/scnanimationplayer/stop())
- [func stop(withBlendOutDuration: TimeInterval)](/documentation/scenekit/scnanimationplayer/stop(withblendoutduration:))
- [SCNTimingFunction](/documentation/scenekit/scntimingfunction)

#### Initializers

- [init(caMediaTimingFunction: CAMediaTimingFunction)](/documentation/scenekit/scntimingfunction/init(camediatimingfunction:))
- [init(timingMode: SCNActionTimingMode)](/documentation/scenekit/scntimingfunction/init(timingmode:))
- [SCNAnimationProtocol](/documentation/scenekit/scnanimationprotocol)
- [SCNAnimation](/documentation/scenekit/scnanimation-swift.class)

#### Supporting Types

- [SCNAnimationDidStartBlock](/documentation/scenekit/scnanimationdidstartblock)
- [SCNAnimationDidStopBlock](/documentation/scenekit/scnanimationdidstopblock)

#### Initializers

- [init(caAnimation: CAAnimation)](/documentation/scenekit/scnanimation-swift.class/init(caanimation:))
- [init(contentsOf: URL)](/documentation/scenekit/scnanimation-swift.class/init(contentsof:))
- [init(named: String)](/documentation/scenekit/scnanimation-swift.class/init(named:))

#### Instance Properties

- [var animationDidStart: SCNAnimationDidStartBlock?](/documentation/scenekit/scnanimation-swift.class/animationdidstart)
- [var animationDidStop: SCNAnimationDidStopBlock?](/documentation/scenekit/scnanimation-swift.class/animationdidstop)
- [var animationEvents: [SCNAnimationEvent]?](/documentation/scenekit/scnanimation-swift.class/animationevents)
- [var autoreverses: Bool](/documentation/scenekit/scnanimation-swift.class/autoreverses)
- [var blendInDuration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/blendinduration)
- [var blendOutDuration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/blendoutduration)
- [var duration: TimeInterval](/documentation/scenekit/scnanimation-swift.class/duration)
- [var fillsBackward: Bool](/documentation/scenekit/scnanimation-swift.class/fillsbackward)
- [var fillsForward: Bool](/documentation/scenekit/scnanimation-swift.class/fillsforward)
- [var isAdditive: Bool](/documentation/scenekit/scnanimation-swift.class/isadditive)
- [var isAppliedOnCompletion: Bool](/documentation/scenekit/scnanimation-swift.class/isappliedoncompletion)
- [var isCumulative: Bool](/documentation/scenekit/scnanimation-swift.class/iscumulative)
- [var isRemovedOnCompletion: Bool](/documentation/scenekit/scnanimation-swift.class/isremovedoncompletion)
- [var keyPath: String?](/documentation/scenekit/scnanimation-swift.class/keypath)
- [var repeatCount: CGFloat](/documentation/scenekit/scnanimation-swift.class/repeatcount)
- [var startDelay: TimeInterval](/documentation/scenekit/scnanimation-swift.class/startdelay)
- [var timeOffset: TimeInterval](/documentation/scenekit/scnanimation-swift.class/timeoffset)
- [var timingFunction: SCNTimingFunction](/documentation/scenekit/scnanimation-swift.class/timingfunction)
- [var usesSceneTimeBase: Bool](/documentation/scenekit/scnanimation-swift.class/usesscenetimebase)
- [Constraints](/documentation/scenekit/constraints)

### First Steps

- [SCNConstraint](/documentation/scenekit/scnconstraint)

#### Tuning a Constraint’s Effect on Nodes

- [var influenceFactor: CGFloat](/documentation/scenekit/scnconstraint/influencefactor)

#### Instance Properties

- [var isEnabled: Bool](/documentation/scenekit/scnconstraint/isenabled)
- [var isIncremental: Bool](/documentation/scenekit/scnconstraint/isincremental)

### Orientation Constraints

- [SCNBillboardConstraint](/documentation/scenekit/scnbillboardconstraint)

#### Working with a Constraint’s Degrees of Freedom

- [var freeAxes: SCNBillboardAxis](/documentation/scenekit/scnbillboardconstraint/freeaxes)

#### Constants

- [SCNBillboardAxis](/documentation/scenekit/scnbillboardaxis)

##### Constants

- [static var X: SCNBillboardAxis](/documentation/scenekit/scnbillboardaxis/x)
- [static var Y: SCNBillboardAxis](/documentation/scenekit/scnbillboardaxis/y)
- [static var Z: SCNBillboardAxis](/documentation/scenekit/scnbillboardaxis/z)
- [static var all: SCNBillboardAxis](/documentation/scenekit/scnbillboardaxis/all)

##### Initializers

- [init(rawValue: UInt)](/documentation/scenekit/scnbillboardaxis/init(rawvalue:))
- [SCNLookAtConstraint](/documentation/scenekit/scnlookatconstraint)

#### Creating a Look-At Constraint

- [convenience init(target: SCNNode?)](/documentation/scenekit/scnlookatconstraint/init(target:))

#### Modifying a Constraint

- [var isGimbalLockEnabled: Bool](/documentation/scenekit/scnlookatconstraint/isgimballockenabled)
- [var target: SCNNode?](/documentation/scenekit/scnlookatconstraint/target)

#### Instance Properties

- [var localFront: SCNVector3](/documentation/scenekit/scnlookatconstraint/localfront)
- [var targetOffset: SCNVector3](/documentation/scenekit/scnlookatconstraint/targetoffset)
- [var worldUp: SCNVector3](/documentation/scenekit/scnlookatconstraint/worldup)

### Position Constraints

- [SCNDistanceConstraint](/documentation/scenekit/scndistanceconstraint)

#### Initializers

- [convenience init(target: SCNNode?)](/documentation/scenekit/scndistanceconstraint/init(target:))

#### Instance Properties

- [var maximumDistance: CGFloat](/documentation/scenekit/scndistanceconstraint/maximumdistance)
- [var minimumDistance: CGFloat](/documentation/scenekit/scndistanceconstraint/minimumdistance)
- [var target: SCNNode?](/documentation/scenekit/scndistanceconstraint/target)
- [SCNAvoidOccluderConstraint](/documentation/scenekit/scnavoidoccluderconstraint)

#### Creating a Constraint

- [convenience init(target: SCNNode?)](/documentation/scenekit/scnavoidoccluderconstraint/init(target:))

#### Configuring Constraint Behavior

- [var bias: CGFloat](/documentation/scenekit/scnavoidoccluderconstraint/bias)
- [var occluderCategoryBitMask: Int](/documentation/scenekit/scnavoidoccluderconstraint/occludercategorybitmask)
- [var target: SCNNode?](/documentation/scenekit/scnavoidoccluderconstraint/target)
- [var delegate: any SCNAvoidOccluderConstraintDelegate](/documentation/scenekit/scnavoidoccluderconstraint/delegate)
- [SCNAvoidOccluderConstraintDelegate](/documentation/scenekit/scnavoidoccluderconstraintdelegate)

##### Instance Methods

- [func avoidOccluderConstraint(SCNAvoidOccluderConstraint, didAvoidOccluder: SCNNode, for: SCNNode)](/documentation/scenekit/scnavoidoccluderconstraintdelegate/avoidoccluderconstraint(_:didavoidoccluder:for:))
- [func avoidOccluderConstraint(SCNAvoidOccluderConstraint, shouldAvoidOccluder: SCNNode, for: SCNNode) -> Bool](/documentation/scenekit/scnavoidoccluderconstraintdelegate/avoidoccluderconstraint(_:shouldavoidoccluder:for:))

### Motion Constraints

- [SCNAccelerationConstraint](/documentation/scenekit/scnaccelerationconstraint)

#### Instance Properties

- [var damping: CGFloat](/documentation/scenekit/scnaccelerationconstraint/damping)
- [var decelerationDistance: CGFloat](/documentation/scenekit/scnaccelerationconstraint/decelerationdistance)
- [var maximumLinearAcceleration: CGFloat](/documentation/scenekit/scnaccelerationconstraint/maximumlinearacceleration)
- [var maximumLinearVelocity: CGFloat](/documentation/scenekit/scnaccelerationconstraint/maximumlinearvelocity)
- [SCNSliderConstraint](/documentation/scenekit/scnsliderconstraint)

#### Instance Properties

- [var collisionCategoryBitMask: Int](/documentation/scenekit/scnsliderconstraint/collisioncategorybitmask)
- [var offset: SCNVector3](/documentation/scenekit/scnsliderconstraint/offset)
- [var radius: CGFloat](/documentation/scenekit/scnsliderconstraint/radius)

### Synchronization

- [SCNReplicatorConstraint](/documentation/scenekit/scnreplicatorconstraint)

#### Initializers

- [convenience init(target: SCNNode?)](/documentation/scenekit/scnreplicatorconstraint/init(target:))

#### Instance Properties

- [var orientationOffset: SCNQuaternion](/documentation/scenekit/scnreplicatorconstraint/orientationoffset)
- [var positionOffset: SCNVector3](/documentation/scenekit/scnreplicatorconstraint/positionoffset)
- [var replicatesOrientation: Bool](/documentation/scenekit/scnreplicatorconstraint/replicatesorientation)
- [var replicatesPosition: Bool](/documentation/scenekit/scnreplicatorconstraint/replicatesposition)
- [var replicatesScale: Bool](/documentation/scenekit/scnreplicatorconstraint/replicatesscale)
- [var scaleOffset: SCNVector3](/documentation/scenekit/scnreplicatorconstraint/scaleoffset)
- [var target: SCNNode?](/documentation/scenekit/scnreplicatorconstraint/target)

### Inverse Kinematics

- [SCNIKConstraint](/documentation/scenekit/scnikconstraint)

#### Creating an Inverse Kinematics Constraint

- [init(chainRootNode: SCNNode)](/documentation/scenekit/scnikconstraint/init(chainrootnode:))
- [class func inverseKinematicsConstraint(chainRootNode: SCNNode) -> Self](/documentation/scenekit/scnikconstraint/inversekinematicsconstraint(chainrootnode:))

#### Adjusting the Constraint’s Limits of Motion

- [var chainRootNode: SCNNode](/documentation/scenekit/scnikconstraint/chainrootnode)
- [func maxAllowedRotationAngle(forJoint: SCNNode) -> CGFloat](/documentation/scenekit/scnikconstraint/maxallowedrotationangle(forjoint:))
- [func setMaxAllowedRotationAngle(CGFloat, forJoint: SCNNode)](/documentation/scenekit/scnikconstraint/setmaxallowedrotationangle(_:forjoint:))

#### Applying Inverse Kinematics to the Constrained Node

- [var targetPosition: SCNVector3](/documentation/scenekit/scnikconstraint/targetposition)

### Customization

- [SCNTransformConstraint](/documentation/scenekit/scntransformconstraint)

#### Creating a Transform Constraint

- [convenience init(inWorldSpace: Bool, with: (SCNNode, SCNMatrix4) -> SCNMatrix4)](/documentation/scenekit/scntransformconstraint/init(inworldspace:with:))

#### Type Methods

- [class func orientationConstraint(inWorldSpace: Bool, with: (SCNNode, SCNQuaternion) -> SCNQuaternion) -> Self](/documentation/scenekit/scntransformconstraint/orientationconstraint(inworldspace:with:))
- [class func positionConstraint(inWorldSpace: Bool, with: (SCNNode, SCNVector3) -> SCNVector3) -> Self](/documentation/scenekit/scntransformconstraint/positionconstraint(inworldspace:with:))
- [SCNSkinner](/documentation/scenekit/scnskinner)

### Creating a Skinner Object

- [convenience init(baseGeometry: SCNGeometry?, bones: [SCNNode], boneInverseBindTransforms: [NSValue]?, boneWeights: SCNGeometrySource, boneIndices: SCNGeometrySource)](/documentation/scenekit/scnskinner/init(basegeometry:bones:boneinversebindtransforms:boneweights:boneindices:))

### Working with a Skinned Geometry

- [var baseGeometry: SCNGeometry?](/documentation/scenekit/scnskinner/basegeometry)
- [var baseGeometryBindTransform: SCNMatrix4](/documentation/scenekit/scnskinner/basegeometrybindtransform)

### Working with an Animation Skeleton

- [var skeleton: SCNNode?](/documentation/scenekit/scnskinner/skeleton)
- [var bones: [SCNNode]](/documentation/scenekit/scnskinner/bones)
- [var boneInverseBindTransforms: [NSValue]?](/documentation/scenekit/scnskinner/boneinversebindtransforms)
- [var boneWeights: SCNGeometrySource](/documentation/scenekit/scnskinner/boneweights)
- [var boneIndices: SCNGeometrySource](/documentation/scenekit/scnskinner/boneindices)
- [SCNMorpher](/documentation/scenekit/scnmorpher)

### Specifying Morph Targets

- [var targets: [SCNGeometry]](/documentation/scenekit/scnmorpher/targets)

### Blending between Morph Targets

- [func weight(forTargetAt: Int) -> CGFloat](/documentation/scenekit/scnmorpher/weight(fortargetat:))
- [func setWeight(CGFloat, forTargetAt: Int)](/documentation/scenekit/scnmorpher/setweight(_:fortargetat:))

### Changing Interpolation Mode

- [var calculationMode: SCNMorpherCalculationMode](/documentation/scenekit/scnmorpher/calculationmode)

### Constants

- [SCNMorpherCalculationMode](/documentation/scenekit/scnmorphercalculationmode)

#### Constants

- [case normalized](/documentation/scenekit/scnmorphercalculationmode/normalized)
- [case additive](/documentation/scenekit/scnmorphercalculationmode/additive)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnmorphercalculationmode/init(rawvalue:))

### Instance Properties

- [var unifiesNormals: Bool](/documentation/scenekit/scnmorpher/unifiesnormals)
- [var weights: [NSNumber]](/documentation/scenekit/scnmorpher/weights)

### Instance Methods

- [func setWeight(CGFloat, forTargetNamed: String)](/documentation/scenekit/scnmorpher/setweight(_:fortargetnamed:))
- [func weight(forTargetNamed: String) -> CGFloat](/documentation/scenekit/scnmorpher/weight(fortargetnamed:))

## Physics

- [Physics Simulation](/documentation/scenekit/physics-simulation)

### Physics Bodies

- [SCNPhysicsBody](/documentation/scenekit/scnphysicsbody)

#### Creating Physics Bodies

- [convenience init(type: SCNPhysicsBodyType, shape: SCNPhysicsShape?)](/documentation/scenekit/scnphysicsbody/init(type:shape:))
- [class func `static`() -> Self](/documentation/scenekit/scnphysicsbody/static())
- [class func dynamic() -> Self](/documentation/scenekit/scnphysicsbody/dynamic())
- [class func kinematic() -> Self](/documentation/scenekit/scnphysicsbody/kinematic())

#### Defining How Forces Affect a Physics Body

- [var physicsShape: SCNPhysicsShape?](/documentation/scenekit/scnphysicsbody/physicsshape)
- [var type: SCNPhysicsBodyType](/documentation/scenekit/scnphysicsbody/type)
- [SCNPhysicsBodyType](/documentation/scenekit/scnphysicsbodytype)

##### Constants

- [case `static`](/documentation/scenekit/scnphysicsbodytype/static)
- [case dynamic](/documentation/scenekit/scnphysicsbodytype/dynamic)
- [case kinematic](/documentation/scenekit/scnphysicsbodytype/kinematic)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnphysicsbodytype/init(rawvalue:))
- [var velocityFactor: SCNVector3](/documentation/scenekit/scnphysicsbody/velocityfactor)
- [var angularVelocityFactor: SCNVector3](/documentation/scenekit/scnphysicsbody/angularvelocityfactor)
- [var isAffectedByGravity: Bool](/documentation/scenekit/scnphysicsbody/isaffectedbygravity)

#### Defining a Body’s Physical Properties

- [var mass: CGFloat](/documentation/scenekit/scnphysicsbody/mass)
- [var charge: CGFloat](/documentation/scenekit/scnphysicsbody/charge)
- [var friction: CGFloat](/documentation/scenekit/scnphysicsbody/friction)
- [var rollingFriction: CGFloat](/documentation/scenekit/scnphysicsbody/rollingfriction)
- [var restitution: CGFloat](/documentation/scenekit/scnphysicsbody/restitution)
- [var damping: CGFloat](/documentation/scenekit/scnphysicsbody/damping)
- [var angularDamping: CGFloat](/documentation/scenekit/scnphysicsbody/angulardamping)
- [var momentOfInertia: SCNVector3](/documentation/scenekit/scnphysicsbody/momentofinertia)
- [var usesDefaultMomentOfInertia: Bool](/documentation/scenekit/scnphysicsbody/usesdefaultmomentofinertia)
- [var centerOfMassOffset: SCNVector3](/documentation/scenekit/scnphysicsbody/centerofmassoffset)

#### Working with Contacts and Collisions

- [var categoryBitMask: Int](/documentation/scenekit/scnphysicsbody/categorybitmask)
- [var contactTestBitMask: Int](/documentation/scenekit/scnphysicsbody/contacttestbitmask)
- [var collisionBitMask: Int](/documentation/scenekit/scnphysicsbody/collisionbitmask)
- [SCNPhysicsCollisionCategory](/documentation/scenekit/scnphysicscollisioncategory)

##### Constants

- [static var `default`: SCNPhysicsCollisionCategory](/documentation/scenekit/scnphysicscollisioncategory/default)
- [static var `static`: SCNPhysicsCollisionCategory](/documentation/scenekit/scnphysicscollisioncategory/static)
- [static var all: SCNPhysicsCollisionCategory](/documentation/scenekit/scnphysicscollisioncategory/all)

##### Initializers

- [init(rawValue: UInt)](/documentation/scenekit/scnphysicscollisioncategory/init(rawvalue:))
- [var continuousCollisionDetectionThreshold: CGFloat](/documentation/scenekit/scnphysicsbody/continuouscollisiondetectionthreshold)

#### Applying Forces, Impulses, and Torques

- [func applyForce(SCNVector3, asImpulse: Bool)](/documentation/scenekit/scnphysicsbody/applyforce(_:asimpulse:))
- [func applyForce(SCNVector3, at: SCNVector3, asImpulse: Bool)](/documentation/scenekit/scnphysicsbody/applyforce(_:at:asimpulse:))
- [func applyTorque(SCNVector4, asImpulse: Bool)](/documentation/scenekit/scnphysicsbody/applytorque(_:asimpulse:))
- [func clearAllForces()](/documentation/scenekit/scnphysicsbody/clearallforces())

#### Interacting with Bodies in Motion

- [var velocity: SCNVector3](/documentation/scenekit/scnphysicsbody/velocity)
- [var angularVelocity: SCNVector4](/documentation/scenekit/scnphysicsbody/angularvelocity)

#### Defining When a Body Can Move

- [var isResting: Bool](/documentation/scenekit/scnphysicsbody/isresting)
- [var allowsResting: Bool](/documentation/scenekit/scnphysicsbody/allowsresting)
- [func setResting(Bool)](/documentation/scenekit/scnphysicsbody/setresting(_:))

#### Synchronizing a Physics Body with its Node

- [func resetTransform()](/documentation/scenekit/scnphysicsbody/resettransform())

#### Instance Properties

- [var angularRestingThreshold: CGFloat](/documentation/scenekit/scnphysicsbody/angularrestingthreshold)
- [var linearRestingThreshold: CGFloat](/documentation/scenekit/scnphysicsbody/linearrestingthreshold)
- [SCNPhysicsShape](/documentation/scenekit/scnphysicsshape)

#### Creating Physics Shapes

- [convenience init(geometry: SCNGeometry, options: [SCNPhysicsShape.Option : Any]?)](/documentation/scenekit/scnphysicsshape/init(geometry:options:))
- [convenience init(node: SCNNode, options: [SCNPhysicsShape.Option : Any]?)](/documentation/scenekit/scnphysicsshape/init(node:options:))

#### Combining Physics Shapes

- [convenience init(shapes: [SCNPhysicsShape], transforms: [NSValue]?)](/documentation/scenekit/scnphysicsshape/init(shapes:transforms:))

#### Getting Information About a Shape

- [var sourceObject: Any](/documentation/scenekit/scnphysicsshape/sourceobject)
- [var options: [SCNPhysicsShape.Option : Any]?](/documentation/scenekit/scnphysicsshape/options)
- [var transforms: [NSValue]?](/documentation/scenekit/scnphysicsshape/transforms)

#### Shape Options

- [SCNPhysicsShape.Option](/documentation/scenekit/scnphysicsshape/option)

##### Type Properties

- [static let collisionMargin: SCNPhysicsShape.Option](/documentation/scenekit/scnphysicsshape/option/collisionmargin)
- [static let keepAsCompound: SCNPhysicsShape.Option](/documentation/scenekit/scnphysicsshape/option/keepascompound)
- [static let scale: SCNPhysicsShape.Option](/documentation/scenekit/scnphysicsshape/option/scale)
- [static let type: SCNPhysicsShape.Option](/documentation/scenekit/scnphysicsshape/option/type)
- [SCNPhysicsShape.ShapeType](/documentation/scenekit/scnphysicsshape/shapetype)

###### Type Properties

- [static let boundingBox: SCNPhysicsShape.ShapeType](/documentation/scenekit/scnphysicsshape/shapetype/boundingbox)
- [static let concavePolyhedron: SCNPhysicsShape.ShapeType](/documentation/scenekit/scnphysicsshape/shapetype/concavepolyhedron)
- [static let convexHull: SCNPhysicsShape.ShapeType](/documentation/scenekit/scnphysicsshape/shapetype/convexhull)

###### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnphysicsshape/shapetype/init(rawvalue:))

##### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnphysicsshape/option/init(rawvalue:))

### Collision and Contact Detection

- [SCNPhysicsContactDelegate](/documentation/scenekit/scnphysicscontactdelegate)

#### Responding to Contact Events

- [func physicsWorld(SCNPhysicsWorld, didBegin: SCNPhysicsContact)](/documentation/scenekit/scnphysicscontactdelegate/physicsworld(_:didbegin:))
- [func physicsWorld(SCNPhysicsWorld, didUpdate: SCNPhysicsContact)](/documentation/scenekit/scnphysicscontactdelegate/physicsworld(_:didupdate:))
- [func physicsWorld(SCNPhysicsWorld, didEnd: SCNPhysicsContact)](/documentation/scenekit/scnphysicscontactdelegate/physicsworld(_:didend:))
- [SCNPhysicsContact](/documentation/scenekit/scnphysicscontact)

#### Inspecting the Contact Properties

- [var nodeA: SCNNode](/documentation/scenekit/scnphysicscontact/nodea)
- [var nodeB: SCNNode](/documentation/scenekit/scnphysicscontact/nodeb)
- [var contactPoint: SCNVector3](/documentation/scenekit/scnphysicscontact/contactpoint)
- [var contactNormal: SCNVector3](/documentation/scenekit/scnphysicscontact/contactnormal)
- [var collisionImpulse: CGFloat](/documentation/scenekit/scnphysicscontact/collisionimpulse)
- [var penetrationDistance: CGFloat](/documentation/scenekit/scnphysicscontact/penetrationdistance)

#### Instance Properties

- [var sweepTestFraction: CGFloat](/documentation/scenekit/scnphysicscontact/sweeptestfraction)

### Physics in a Scene

- [SCNPhysicsWorld](/documentation/scenekit/scnphysicsworld)

#### Managing the Physics Simulation

- [var gravity: SCNVector3](/documentation/scenekit/scnphysicsworld/gravity)
- [var speed: CGFloat](/documentation/scenekit/scnphysicsworld/speed)
- [var timeStep: TimeInterval](/documentation/scenekit/scnphysicsworld/timestep)
- [func updateCollisionPairs()](/documentation/scenekit/scnphysicsworld/updatecollisionpairs())

#### Registering Physics Behaviors

- [func addBehavior(SCNPhysicsBehavior)](/documentation/scenekit/scnphysicsworld/addbehavior(_:))
- [func removeBehavior(SCNPhysicsBehavior)](/documentation/scenekit/scnphysicsworld/removebehavior(_:))
- [var allBehaviors: [SCNPhysicsBehavior]](/documentation/scenekit/scnphysicsworld/allbehaviors)
- [func removeAllBehaviors()](/documentation/scenekit/scnphysicsworld/removeallbehaviors())

#### Detecting Contacts Between Physics Bodies

- [var contactDelegate: (any SCNPhysicsContactDelegate)?](/documentation/scenekit/scnphysicsworld/contactdelegate)
- [func contactTestBetween(SCNPhysicsBody, SCNPhysicsBody, options: [SCNPhysicsWorld.TestOption : Any]?) -> [SCNPhysicsContact]](/documentation/scenekit/scnphysicsworld/contacttestbetween(_:_:options:))
- [func contactTest(with: SCNPhysicsBody, options: [SCNPhysicsWorld.TestOption : Any]?) -> [SCNPhysicsContact]](/documentation/scenekit/scnphysicsworld/contacttest(with:options:))

#### Searching for Physics Bodies

- [func rayTestWithSegment(from: SCNVector3, to: SCNVector3, options: [SCNPhysicsWorld.TestOption : Any]?) -> [SCNHitTestResult]](/documentation/scenekit/scnphysicsworld/raytestwithsegment(from:to:options:))
- [func convexSweepTest(with: SCNPhysicsShape, from: SCNMatrix4, to: SCNMatrix4, options: [SCNPhysicsWorld.TestOption : Any]?) -> [SCNPhysicsContact]](/documentation/scenekit/scnphysicsworld/convexsweeptest(with:from:to:options:))

#### Search Options

- [SCNPhysicsWorld.TestOption](/documentation/scenekit/scnphysicsworld/testoption)

##### Type Properties

- [static let backfaceCulling: SCNPhysicsWorld.TestOption](/documentation/scenekit/scnphysicsworld/testoption/backfaceculling)
- [static let collisionBitMask: SCNPhysicsWorld.TestOption](/documentation/scenekit/scnphysicsworld/testoption/collisionbitmask)
- [static let searchMode: SCNPhysicsWorld.TestOption](/documentation/scenekit/scnphysicsworld/testoption/searchmode)
- [SCNPhysicsWorld.TestSearchMode](/documentation/scenekit/scnphysicsworld/testsearchmode)

###### Type Properties

- [static let all: SCNPhysicsWorld.TestSearchMode](/documentation/scenekit/scnphysicsworld/testsearchmode/all)
- [static let any: SCNPhysicsWorld.TestSearchMode](/documentation/scenekit/scnphysicsworld/testsearchmode/any)
- [static let closest: SCNPhysicsWorld.TestSearchMode](/documentation/scenekit/scnphysicsworld/testsearchmode/closest)

###### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnphysicsworld/testsearchmode/init(rawvalue:))

##### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnphysicsworld/testoption/init(rawvalue:))
- [SCNPhysicsField](/documentation/scenekit/scnphysicsfield)

#### Creating Physics Fields

- [class func drag() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/drag())
- [class func vortex() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/vortex())
- [class func radialGravity() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/radialgravity())
- [class func linearGravity() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/lineargravity())
- [class func noiseField(smoothness: CGFloat, animationSpeed: CGFloat) -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/noisefield(smoothness:animationspeed:))
- [class func turbulenceField(smoothness: CGFloat, animationSpeed: CGFloat) -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/turbulencefield(smoothness:animationspeed:))
- [class func spring() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/spring())
- [class func electric() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/electric())
- [class func magnetic() -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/magnetic())

#### Creating Custom Physics Fields

- [class func customField(evaluationBlock: SCNFieldForceEvaluator) -> SCNPhysicsField](/documentation/scenekit/scnphysicsfield/customfield(evaluationblock:))

#### Specifying a Field’s Area of Effect

- [var halfExtent: SCNVector3](/documentation/scenekit/scnphysicsfield/halfextent)
- [var scope: SCNPhysicsFieldScope](/documentation/scenekit/scnphysicsfield/scope)
- [var usesEllipsoidalExtent: Bool](/documentation/scenekit/scnphysicsfield/usesellipsoidalextent)
- [var offset: SCNVector3](/documentation/scenekit/scnphysicsfield/offset)
- [var direction: SCNVector3](/documentation/scenekit/scnphysicsfield/direction)

#### Specifying a Field’s Behavior

- [var strength: CGFloat](/documentation/scenekit/scnphysicsfield/strength)
- [var falloffExponent: CGFloat](/documentation/scenekit/scnphysicsfield/falloffexponent)
- [var minimumDistance: CGFloat](/documentation/scenekit/scnphysicsfield/minimumdistance)
- [var isActive: Bool](/documentation/scenekit/scnphysicsfield/isactive)
- [var isExclusive: Bool](/documentation/scenekit/scnphysicsfield/isexclusive)

#### Choosing Physics Bodies to Be Affected by the Field

- [var categoryBitMask: Int](/documentation/scenekit/scnphysicsfield/categorybitmask)

#### Constants

- [SCNFieldForceEvaluator](/documentation/scenekit/scnfieldforceevaluator)
- [SCNPhysicsFieldScope](/documentation/scenekit/scnphysicsfieldscope)

##### Constants

- [case insideExtent](/documentation/scenekit/scnphysicsfieldscope/insideextent)
- [case outsideExtent](/documentation/scenekit/scnphysicsfieldscope/outsideextent)

##### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnphysicsfieldscope/init(rawvalue:))
- [SCNPhysicsBehavior](/documentation/scenekit/scnphysicsbehavior)

### Joints

- [SCNPhysicsHingeJoint](/documentation/scenekit/scnphysicshingejoint)

#### Creating a Hinge Joint

- [convenience init(bodyA: SCNPhysicsBody, axisA: SCNVector3, anchorA: SCNVector3, bodyB: SCNPhysicsBody, axisB: SCNVector3, anchorB: SCNVector3)](/documentation/scenekit/scnphysicshingejoint/init(bodya:axisa:anchora:bodyb:axisb:anchorb:))
- [convenience init(body: SCNPhysicsBody, axis: SCNVector3, anchor: SCNVector3)](/documentation/scenekit/scnphysicshingejoint/init(body:axis:anchor:))

#### Managing the Characteristics of a Hinge Joint

- [var bodyA: SCNPhysicsBody](/documentation/scenekit/scnphysicshingejoint/bodya)
- [var axisA: SCNVector3](/documentation/scenekit/scnphysicshingejoint/axisa)
- [var anchorA: SCNVector3](/documentation/scenekit/scnphysicshingejoint/anchora)
- [var bodyB: SCNPhysicsBody?](/documentation/scenekit/scnphysicshingejoint/bodyb)
- [var axisB: SCNVector3](/documentation/scenekit/scnphysicshingejoint/axisb)
- [var anchorB: SCNVector3](/documentation/scenekit/scnphysicshingejoint/anchorb)
- [SCNPhysicsSliderJoint](/documentation/scenekit/scnphysicssliderjoint)

#### Creating a Slider Joint

- [convenience init(bodyA: SCNPhysicsBody, axisA: SCNVector3, anchorA: SCNVector3, bodyB: SCNPhysicsBody, axisB: SCNVector3, anchorB: SCNVector3)](/documentation/scenekit/scnphysicssliderjoint/init(bodya:axisa:anchora:bodyb:axisb:anchorb:))
- [convenience init(body: SCNPhysicsBody, axis: SCNVector3, anchor: SCNVector3)](/documentation/scenekit/scnphysicssliderjoint/init(body:axis:anchor:))

#### Managing the Characteristics of a Slider Joint

- [var bodyA: SCNPhysicsBody](/documentation/scenekit/scnphysicssliderjoint/bodya)
- [var axisA: SCNVector3](/documentation/scenekit/scnphysicssliderjoint/axisa)
- [var anchorA: SCNVector3](/documentation/scenekit/scnphysicssliderjoint/anchora)
- [var bodyB: SCNPhysicsBody?](/documentation/scenekit/scnphysicssliderjoint/bodyb)
- [var axisB: SCNVector3](/documentation/scenekit/scnphysicssliderjoint/axisb)
- [var anchorB: SCNVector3](/documentation/scenekit/scnphysicssliderjoint/anchorb)

#### Limiting the Motion of a Slider Joint

- [var minimumLinearLimit: CGFloat](/documentation/scenekit/scnphysicssliderjoint/minimumlinearlimit)
- [var maximumLinearLimit: CGFloat](/documentation/scenekit/scnphysicssliderjoint/maximumlinearlimit)
- [var minimumAngularLimit: CGFloat](/documentation/scenekit/scnphysicssliderjoint/minimumangularlimit)
- [var maximumAngularLimit: CGFloat](/documentation/scenekit/scnphysicssliderjoint/maximumangularlimit)

#### Applying Forces and Torques

- [var motorTargetLinearVelocity: CGFloat](/documentation/scenekit/scnphysicssliderjoint/motortargetlinearvelocity)
- [var motorMaximumForce: CGFloat](/documentation/scenekit/scnphysicssliderjoint/motormaximumforce)
- [var motorTargetAngularVelocity: CGFloat](/documentation/scenekit/scnphysicssliderjoint/motortargetangularvelocity)
- [var motorMaximumTorque: CGFloat](/documentation/scenekit/scnphysicssliderjoint/motormaximumtorque)
- [SCNPhysicsBallSocketJoint](/documentation/scenekit/scnphysicsballsocketjoint)

#### Creating a Ball and Socket Joint

- [convenience init(bodyA: SCNPhysicsBody, anchorA: SCNVector3, bodyB: SCNPhysicsBody, anchorB: SCNVector3)](/documentation/scenekit/scnphysicsballsocketjoint/init(bodya:anchora:bodyb:anchorb:))
- [convenience init(body: SCNPhysicsBody, anchor: SCNVector3)](/documentation/scenekit/scnphysicsballsocketjoint/init(body:anchor:))

#### Managing the Characteristics of a Ball and Socket Joint

- [var bodyA: SCNPhysicsBody](/documentation/scenekit/scnphysicsballsocketjoint/bodya)
- [var anchorA: SCNVector3](/documentation/scenekit/scnphysicsballsocketjoint/anchora)
- [var bodyB: SCNPhysicsBody?](/documentation/scenekit/scnphysicsballsocketjoint/bodyb)
- [var anchorB: SCNVector3](/documentation/scenekit/scnphysicsballsocketjoint/anchorb)
- [SCNPhysicsConeTwistJoint](/documentation/scenekit/scnphysicsconetwistjoint)

#### Initializers

- [convenience init(body: SCNPhysicsBody, frame: SCNMatrix4)](/documentation/scenekit/scnphysicsconetwistjoint/init(body:frame:))
- [convenience init(bodyA: SCNPhysicsBody, frameA: SCNMatrix4, bodyB: SCNPhysicsBody, frameB: SCNMatrix4)](/documentation/scenekit/scnphysicsconetwistjoint/init(bodya:framea:bodyb:frameb:))

#### Instance Properties

- [var bodyA: SCNPhysicsBody](/documentation/scenekit/scnphysicsconetwistjoint/bodya)
- [var bodyB: SCNPhysicsBody?](/documentation/scenekit/scnphysicsconetwistjoint/bodyb)
- [var frameA: SCNMatrix4](/documentation/scenekit/scnphysicsconetwistjoint/framea)
- [var frameB: SCNMatrix4](/documentation/scenekit/scnphysicsconetwistjoint/frameb)
- [var maximumAngularLimit1: CGFloat](/documentation/scenekit/scnphysicsconetwistjoint/maximumangularlimit1)
- [var maximumAngularLimit2: CGFloat](/documentation/scenekit/scnphysicsconetwistjoint/maximumangularlimit2)
- [var maximumTwistAngle: CGFloat](/documentation/scenekit/scnphysicsconetwistjoint/maximumtwistangle)

### Vehicle Simulation

- [SCNPhysicsVehicle](/documentation/scenekit/scnphysicsvehicle)

#### Creating a Vehicle

- [convenience init(chassisBody: SCNPhysicsBody, wheels: [SCNPhysicsVehicleWheel])](/documentation/scenekit/scnphysicsvehicle/init(chassisbody:wheels:))

#### Working with a Vehicle’s Physical Characteristics

- [var chassisBody: SCNPhysicsBody](/documentation/scenekit/scnphysicsvehicle/chassisbody)
- [var wheels: [SCNPhysicsVehicleWheel]](/documentation/scenekit/scnphysicsvehicle/wheels)

#### Driving a Vehicle

- [func applyEngineForce(CGFloat, forWheelAt: Int)](/documentation/scenekit/scnphysicsvehicle/applyengineforce(_:forwheelat:))
- [func applyBrakingForce(CGFloat, forWheelAt: Int)](/documentation/scenekit/scnphysicsvehicle/applybrakingforce(_:forwheelat:))
- [func setSteeringAngle(CGFloat, forWheelAt: Int)](/documentation/scenekit/scnphysicsvehicle/setsteeringangle(_:forwheelat:))
- [var speedInKilometersPerHour: CGFloat](/documentation/scenekit/scnphysicsvehicle/speedinkilometersperhour)
- [SCNPhysicsVehicleWheel](/documentation/scenekit/scnphysicsvehiclewheel)

#### Creating a Wheel

- [convenience init(node: SCNNode)](/documentation/scenekit/scnphysicsvehiclewheel/init(node:))

#### Managing a Wheel’s Connection to a Vehicle

- [var connectionPosition: SCNVector3](/documentation/scenekit/scnphysicsvehiclewheel/connectionposition)
- [var axle: SCNVector3](/documentation/scenekit/scnphysicsvehiclewheel/axle)
- [var steeringAxis: SCNVector3](/documentation/scenekit/scnphysicsvehiclewheel/steeringaxis)

#### Simulating Wheel Size

- [var radius: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/radius)

#### Simulating Traction

- [var frictionSlip: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/frictionslip)

#### Simulating Suspension

- [var suspensionStiffness: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/suspensionstiffness)
- [var suspensionCompression: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/suspensioncompression)
- [var suspensionDamping: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/suspensiondamping)
- [var maximumSuspensionTravel: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/maximumsuspensiontravel)
- [var maximumSuspensionForce: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/maximumsuspensionforce)
- [var suspensionRestLength: CGFloat](/documentation/scenekit/scnphysicsvehiclewheel/suspensionrestlength)

#### Inspecting the Wheel Node

- [var node: SCNNode](/documentation/scenekit/scnphysicsvehiclewheel/node)

## Particle Systems

- [SCNParticleSystem](/documentation/scenekit/scnparticlesystem)

### Creating a Particle System

- [convenience init?(named: String, inDirectory: String?)](/documentation/scenekit/scnparticlesystem/init(named:indirectory:))

### Managing Particle Emission Timing

- [var emissionDuration: CGFloat](/documentation/scenekit/scnparticlesystem/emissionduration)
- [var emissionDurationVariation: CGFloat](/documentation/scenekit/scnparticlesystem/emissiondurationvariation)
- [var idleDuration: CGFloat](/documentation/scenekit/scnparticlesystem/idleduration)
- [var idleDurationVariation: CGFloat](/documentation/scenekit/scnparticlesystem/idledurationvariation)
- [var loops: Bool](/documentation/scenekit/scnparticlesystem/loops)
- [var warmupDuration: CGFloat](/documentation/scenekit/scnparticlesystem/warmupduration)
- [var birthRate: CGFloat](/documentation/scenekit/scnparticlesystem/birthrate)
- [var birthRateVariation: CGFloat](/documentation/scenekit/scnparticlesystem/birthratevariation)

### Managing Particle Emission Locations

- [var emitterShape: SCNGeometry?](/documentation/scenekit/scnparticlesystem/emittershape)
- [var birthLocation: SCNParticleBirthLocation](/documentation/scenekit/scnparticlesystem/birthlocation)
- [SCNParticleBirthLocation](/documentation/scenekit/scnparticlebirthlocation)

#### Constants

- [case surface](/documentation/scenekit/scnparticlebirthlocation/surface)
- [case volume](/documentation/scenekit/scnparticlebirthlocation/volume)
- [case vertex](/documentation/scenekit/scnparticlebirthlocation/vertex)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticlebirthlocation/init(rawvalue:))
- [var birthDirection: SCNParticleBirthDirection](/documentation/scenekit/scnparticlesystem/birthdirection)
- [SCNParticleBirthDirection](/documentation/scenekit/scnparticlebirthdirection)

#### Constants

- [case constant](/documentation/scenekit/scnparticlebirthdirection/constant)
- [case surfaceNormal](/documentation/scenekit/scnparticlebirthdirection/surfacenormal)
- [case random](/documentation/scenekit/scnparticlebirthdirection/random)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticlebirthdirection/init(rawvalue:))
- [var emittingDirection: SCNVector3](/documentation/scenekit/scnparticlesystem/emittingdirection)
- [var spreadingAngle: CGFloat](/documentation/scenekit/scnparticlesystem/spreadingangle)

### Managing Particle Motion

- [var particleAngle: CGFloat](/documentation/scenekit/scnparticlesystem/particleangle)
- [var particleAngleVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particleanglevariation)
- [var particleVelocity: CGFloat](/documentation/scenekit/scnparticlesystem/particlevelocity)
- [var particleVelocityVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlevelocityvariation)
- [var particleAngularVelocity: CGFloat](/documentation/scenekit/scnparticlesystem/particleangularvelocity)
- [var particleAngularVelocityVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particleangularvelocityvariation)
- [var particleLifeSpan: CGFloat](/documentation/scenekit/scnparticlesystem/particlelifespan)
- [var particleLifeSpanVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlelifespanvariation)

### Specifying Particle Appearance

- [var particleSize: CGFloat](/documentation/scenekit/scnparticlesystem/particlesize)
- [var particleSizeVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlesizevariation)
- [var particleColor: UIColor](/documentation/scenekit/scnparticlesystem/particlecolor)
- [var particleColorVariation: SCNVector4](/documentation/scenekit/scnparticlesystem/particlecolorvariation)
- [var particleImage: Any?](/documentation/scenekit/scnparticlesystem/particleimage)
- [var fresnelExponent: CGFloat](/documentation/scenekit/scnparticlesystem/fresnelexponent)
- [var stretchFactor: CGFloat](/documentation/scenekit/scnparticlesystem/stretchfactor)

### Animating Particle Images

- [var imageSequenceRowCount: Int](/documentation/scenekit/scnparticlesystem/imagesequencerowcount)
- [var imageSequenceColumnCount: Int](/documentation/scenekit/scnparticlesystem/imagesequencecolumncount)
- [var imageSequenceInitialFrame: CGFloat](/documentation/scenekit/scnparticlesystem/imagesequenceinitialframe)
- [var imageSequenceInitialFrameVariation: CGFloat](/documentation/scenekit/scnparticlesystem/imagesequenceinitialframevariation)
- [var imageSequenceFrameRate: CGFloat](/documentation/scenekit/scnparticlesystem/imagesequenceframerate)
- [var imageSequenceFrameRateVariation: CGFloat](/documentation/scenekit/scnparticlesystem/imagesequenceframeratevariation)
- [var imageSequenceAnimationMode: SCNParticleImageSequenceAnimationMode](/documentation/scenekit/scnparticlesystem/imagesequenceanimationmode)
- [SCNParticleImageSequenceAnimationMode](/documentation/scenekit/scnparticleimagesequenceanimationmode)

#### Constants

- [case `repeat`](/documentation/scenekit/scnparticleimagesequenceanimationmode/repeat)
- [case clamp](/documentation/scenekit/scnparticleimagesequenceanimationmode/clamp)
- [case autoReverse](/documentation/scenekit/scnparticleimagesequenceanimationmode/autoreverse)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticleimagesequenceanimationmode/init(rawvalue:))

### Simulating Physics for Particles

- [var isAffectedByGravity: Bool](/documentation/scenekit/scnparticlesystem/isaffectedbygravity)
- [var isAffectedByPhysicsFields: Bool](/documentation/scenekit/scnparticlesystem/isaffectedbyphysicsfields)
- [var colliderNodes: [SCNNode]?](/documentation/scenekit/scnparticlesystem/collidernodes)
- [var particleDiesOnCollision: Bool](/documentation/scenekit/scnparticlesystem/particlediesoncollision)
- [var acceleration: SCNVector3](/documentation/scenekit/scnparticlesystem/acceleration)
- [var dampingFactor: CGFloat](/documentation/scenekit/scnparticlesystem/dampingfactor)
- [var particleMass: CGFloat](/documentation/scenekit/scnparticlesystem/particlemass)
- [var particleMassVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlemassvariation)
- [var particleCharge: CGFloat](/documentation/scenekit/scnparticlesystem/particlecharge)
- [var particleChargeVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlechargevariation)
- [var particleBounce: CGFloat](/documentation/scenekit/scnparticlesystem/particlebounce)
- [var particleBounceVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlebouncevariation)
- [var particleFriction: CGFloat](/documentation/scenekit/scnparticlesystem/particlefriction)
- [var particleFrictionVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particlefrictionvariation)

### Spawning Additional Particle Systems

- [var systemSpawnedOnCollision: SCNParticleSystem?](/documentation/scenekit/scnparticlesystem/systemspawnedoncollision)
- [var systemSpawnedOnDying: SCNParticleSystem?](/documentation/scenekit/scnparticlesystem/systemspawnedondying)
- [var systemSpawnedOnLiving: SCNParticleSystem?](/documentation/scenekit/scnparticlesystem/systemspawnedonliving)

### Managing Particle Rendering

- [var blendMode: SCNParticleBlendMode](/documentation/scenekit/scnparticlesystem/blendmode)
- [SCNParticleBlendMode](/documentation/scenekit/scnparticleblendmode)

#### Constants

- [case additive](/documentation/scenekit/scnparticleblendmode/additive)
- [case subtract](/documentation/scenekit/scnparticleblendmode/subtract)
- [case multiply](/documentation/scenekit/scnparticleblendmode/multiply)
- [case screen](/documentation/scenekit/scnparticleblendmode/screen)
- [case alpha](/documentation/scenekit/scnparticleblendmode/alpha)
- [case replace](/documentation/scenekit/scnparticleblendmode/replace)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticleblendmode/init(rawvalue:))
- [var orientationMode: SCNParticleOrientationMode](/documentation/scenekit/scnparticlesystem/orientationmode)
- [SCNParticleOrientationMode](/documentation/scenekit/scnparticleorientationmode)

#### Constants

- [case billboardScreenAligned](/documentation/scenekit/scnparticleorientationmode/billboardscreenaligned)
- [case billboardViewAligned](/documentation/scenekit/scnparticleorientationmode/billboardviewaligned)
- [case free](/documentation/scenekit/scnparticleorientationmode/free)
- [case billboardYAligned](/documentation/scenekit/scnparticleorientationmode/billboardyaligned)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticleorientationmode/init(rawvalue:))
- [var sortingMode: SCNParticleSortingMode](/documentation/scenekit/scnparticlesystem/sortingmode)
- [SCNParticleSortingMode](/documentation/scenekit/scnparticlesortingmode)

#### Constants

- [case none](/documentation/scenekit/scnparticlesortingmode/none)
- [case projectedDepth](/documentation/scenekit/scnparticlesortingmode/projecteddepth)
- [case distance](/documentation/scenekit/scnparticlesortingmode/distance)
- [case oldestFirst](/documentation/scenekit/scnparticlesortingmode/oldestfirst)
- [case youngestFirst](/documentation/scenekit/scnparticlesortingmode/youngestfirst)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticlesortingmode/init(rawvalue:))
- [var isLightingEnabled: Bool](/documentation/scenekit/scnparticlesystem/islightingenabled)
- [var isBlackPassEnabled: Bool](/documentation/scenekit/scnparticlesystem/isblackpassenabled)

### Controlling Particle Simulation

- [var isLocal: Bool](/documentation/scenekit/scnparticlesystem/islocal)
- [func reset()](/documentation/scenekit/scnparticlesystem/reset())
- [var speedFactor: CGFloat](/documentation/scenekit/scnparticlesystem/speedfactor)

### Modifying Particles in Response to Particle System Events

- [func handle(SCNParticleEvent, forProperties: [SCNParticleSystem.ParticleProperty], handler: SCNParticleEventBlock)](/documentation/scenekit/scnparticlesystem/handle(_:forproperties:handler:))
- [SCNParticleEvent](/documentation/scenekit/scnparticleevent)

#### Constants

- [case birth](/documentation/scenekit/scnparticleevent/birth)
- [case death](/documentation/scenekit/scnparticleevent/death)
- [case collision](/documentation/scenekit/scnparticleevent/collision)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticleevent/init(rawvalue:))
- [SCNParticleEventBlock](/documentation/scenekit/scnparticleeventblock)

### Modifying Particles Over Time

- [var propertyControllers: [SCNParticleSystem.ParticleProperty : SCNParticlePropertyController]?](/documentation/scenekit/scnparticlesystem/propertycontrollers)
- [func addModifier(forProperties: [SCNParticleSystem.ParticleProperty], at: SCNParticleModifierStage, modifier: SCNParticleModifierBlock)](/documentation/scenekit/scnparticlesystem/addmodifier(forproperties:at:modifier:))
- [func removeModifiers(at: SCNParticleModifierStage)](/documentation/scenekit/scnparticlesystem/removemodifiers(at:))
- [func removeAllModifiers()](/documentation/scenekit/scnparticlesystem/removeallmodifiers())
- [SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty)

#### Type Properties

- [static let angle: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/angle)
- [static let angularVelocity: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/angularvelocity)
- [static let bounce: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/bounce)
- [static let charge: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/charge)
- [static let color: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/color)
- [static let contactNormal: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/contactnormal)
- [static let contactPoint: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/contactpoint)
- [static let frame: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/frame)
- [static let frameRate: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/framerate)
- [static let friction: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/friction)
- [static let life: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/life)
- [static let opacity: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/opacity)
- [static let position: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/position)
- [static let rotationAxis: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/rotationaxis)
- [static let size: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/size)
- [static let velocity: SCNParticleSystem.ParticleProperty](/documentation/scenekit/scnparticlesystem/particleproperty/velocity)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnparticlesystem/particleproperty/init(rawvalue:))
- [SCNParticleModifierStage](/documentation/scenekit/scnparticlemodifierstage)

#### Constants

- [case preDynamics](/documentation/scenekit/scnparticlemodifierstage/predynamics)
- [case postDynamics](/documentation/scenekit/scnparticlemodifierstage/postdynamics)
- [case preCollision](/documentation/scenekit/scnparticlemodifierstage/precollision)
- [case postCollision](/documentation/scenekit/scnparticlemodifierstage/postcollision)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticlemodifierstage/init(rawvalue:))
- [SCNParticleModifierBlock](/documentation/scenekit/scnparticlemodifierblock)

### Sample Code

- [Building a document browser app for custom file formats](/documentation/uikit/building-a-document-browser-app-for-custom-file-formats)

### Instance Properties

- [var orientationDirection: SCNVector3](/documentation/scenekit/scnparticlesystem/orientationdirection)
- [var particleIntensity: CGFloat](/documentation/scenekit/scnparticlesystem/particleintensity)
- [var particleIntensityVariation: CGFloat](/documentation/scenekit/scnparticlesystem/particleintensityvariation)
- [var writesToDepthBuffer: Bool](/documentation/scenekit/scnparticlesystem/writestodepthbuffer)
- [SCNParticlePropertyController](/documentation/scenekit/scnparticlepropertycontroller)

### Creating a Property Controller

- [convenience init(animation: CAAnimation)](/documentation/scenekit/scnparticlepropertycontroller/init(animation:))

### Managing the Controller’s Animation

- [var animation: CAAnimation](/documentation/scenekit/scnparticlepropertycontroller/animation)
- [var inputMode: SCNParticleInputMode](/documentation/scenekit/scnparticlepropertycontroller/inputmode)
- [var inputBias: CGFloat](/documentation/scenekit/scnparticlepropertycontroller/inputbias)
- [var inputScale: CGFloat](/documentation/scenekit/scnparticlepropertycontroller/inputscale)
- [var inputOrigin: SCNNode?](/documentation/scenekit/scnparticlepropertycontroller/inputorigin)
- [var inputProperty: SCNParticleSystem.ParticleProperty?](/documentation/scenekit/scnparticlepropertycontroller/inputproperty)

### Constants

- [SCNParticleInputMode](/documentation/scenekit/scnparticleinputmode)

#### Constants

- [case overLife](/documentation/scenekit/scnparticleinputmode/overlife)
- [case overDistance](/documentation/scenekit/scnparticleinputmode/overdistance)
- [case overOtherProperty](/documentation/scenekit/scnparticleinputmode/overotherproperty)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnparticleinputmode/init(rawvalue:))

## Audio

- [SCNAudioSource](/documentation/scenekit/scnaudiosource)

### Creating an Audio Source

- [convenience init?(named: String)](/documentation/scenekit/scnaudiosource/init(named:))
- [convenience init?(fileNamed: String)](/documentation/scenekit/scnaudiosource/init(filenamed:))
- [init?(url: URL)](/documentation/scenekit/scnaudiosource/init(url:))

### Controlling 3D Audio Spatialization

- [var isPositional: Bool](/documentation/scenekit/scnaudiosource/ispositional)

### Preloading Audio Data

- [func load()](/documentation/scenekit/scnaudiosource/load())

### Setting Default Playback Parameters

- [var volume: Float](/documentation/scenekit/scnaudiosource/volume)
- [var rate: Float](/documentation/scenekit/scnaudiosource/rate)
- [var reverbBlend: Float](/documentation/scenekit/scnaudiosource/reverbblend)
- [var loops: Bool](/documentation/scenekit/scnaudiosource/loops)
- [var shouldStream: Bool](/documentation/scenekit/scnaudiosource/shouldstream)
- [SCNAudioPlayer](/documentation/scenekit/scnaudioplayer)

### Creating an Audio Player

- [init(source: SCNAudioSource)](/documentation/scenekit/scnaudioplayer/init(source:))
- [init(avAudioNode: AVAudioNode)](/documentation/scenekit/scnaudioplayer/init(avaudionode:))

### Working with Audio Sources

- [var audioSource: SCNAudioSource?](/documentation/scenekit/scnaudioplayer/audiosource)
- [var audioNode: AVAudioNode?](/documentation/scenekit/scnaudioplayer/audionode)

### Responding to Playback

- [var willStartPlayback: (() -> Void)?](/documentation/scenekit/scnaudioplayer/willstartplayback)
- [var didFinishPlayback: (() -> Void)?](/documentation/scenekit/scnaudioplayer/didfinishplayback)

## Renderer Customization

- [SCNShadable](/documentation/scenekit/scnshadable)

### Assigning a Custom Shader Program

- [var program: SCNProgram?](/documentation/scenekit/scnshadable/program)

### Customizing SceneKit’s Shader Programs

- [var shaderModifiers: [SCNShaderModifierEntryPoint : String]?](/documentation/scenekit/scnshadable/shadermodifiers)

### Handling Parameters in Custom OpenGL Shader Programs

- [func handleBinding(ofSymbol: String, handler: SCNBindingBlock?)](/documentation/scenekit/scnshadable/handlebinding(ofsymbol:handler:))
- [func handleUnbinding(ofSymbol: String, handler: SCNBindingBlock?)](/documentation/scenekit/scnshadable/handleunbinding(ofsymbol:handler:))

### Constants

- [SCNBindingBlock](/documentation/scenekit/scnbindingblock)
- [SCNShaderModifierEntryPoint](/documentation/scenekit/scnshadermodifierentrypoint)

#### Type Properties

- [static let fragment: SCNShaderModifierEntryPoint](/documentation/scenekit/scnshadermodifierentrypoint/fragment)
- [static let geometry: SCNShaderModifierEntryPoint](/documentation/scenekit/scnshadermodifierentrypoint/geometry)
- [static let lightingModel: SCNShaderModifierEntryPoint](/documentation/scenekit/scnshadermodifierentrypoint/lightingmodel)
- [static let surface: SCNShaderModifierEntryPoint](/documentation/scenekit/scnshadermodifierentrypoint/surface)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnshadermodifierentrypoint/init(rawvalue:))

### Instance Properties

- [var minimumLanguageVersion: NSNumber?](/documentation/scenekit/scnshadable/minimumlanguageversion)
- [SCNProgram](/documentation/scenekit/scnprogram)

### Working with OpenGL Shader Source Code

- [var vertexShader: String?](/documentation/scenekit/scnprogram/vertexshader)
- [var fragmentShader: String?](/documentation/scenekit/scnprogram/fragmentshader)
- [var geometryShader: String?](/documentation/scenekit/scnprogram/geometryshader)
- [var tessellationControlShader: String?](/documentation/scenekit/scnprogram/tessellationcontrolshader)
- [var tessellationEvaluationShader: String?](/documentation/scenekit/scnprogram/tessellationevaluationshader)

### Mapping GLSL Symbols to SceneKit Semantics

- [func setSemantic(String?, forSymbol: String, options: [String : Any]?)](/documentation/scenekit/scnprogram/setsemantic(_:forsymbol:options:))
- [let SCNProgramMappingChannelKey: String](/documentation/scenekit/scnprogrammappingchannelkey)
- [func semantic(forSymbol: String) -> String?](/documentation/scenekit/scnprogram/semantic(forsymbol:))
- [let SCNModelTransform: String](/documentation/scenekit/scnmodeltransform)
- [let SCNModelViewProjectionTransform: String](/documentation/scenekit/scnmodelviewprojectiontransform)
- [let SCNModelViewTransform: String](/documentation/scenekit/scnmodelviewtransform)
- [let SCNNormalTransform: String](/documentation/scenekit/scnnormaltransform)
- [let SCNProjectionTransform: String](/documentation/scenekit/scnprojectiontransform)
- [let SCNViewTransform: String](/documentation/scenekit/scnviewtransform)

### Providing a Delegate Object

- [var delegate: (any SCNProgramDelegate)?](/documentation/scenekit/scnprogram/delegate)
- [SCNProgramDelegate](/documentation/scenekit/scnprogramdelegate)

#### Handling Shader Compilation Errors

- [func program(SCNProgram, handleError: any Error)](/documentation/scenekit/scnprogramdelegate/program(_:handleerror:))
- [let SCNErrorDomain: String](/documentation/scenekit/scnerrordomain)
- [SceneKit Error Codes](/documentation/scenekit/1409723-scenekit-error-codes)

##### Constants

- [var SCNProgramCompilationError: Int](/documentation/scenekit/scnprogramcompilationerror)

#### Finding Fragment Opaqueness

- [func programIsOpaque(SCNProgram) -> Bool](/documentation/scenekit/scnprogramdelegate/programisopaque(_:))

#### Binding and Unbinding Values

- [func program(SCNProgram, bindValueForSymbol: String, atLocation: UInt32, programID: UInt32, renderer: SCNRenderer) -> Bool](/documentation/scenekit/scnprogramdelegate/program(_:bindvalueforsymbol:atlocation:programid:renderer:))
- [func program(SCNProgram, unbindValueForSymbol: String, atLocation: UInt32, programID: UInt32, renderer: SCNRenderer)](/documentation/scenekit/scnprogramdelegate/program(_:unbindvalueforsymbol:atlocation:programid:renderer:))

### Managing Opacity

- [var isOpaque: Bool](/documentation/scenekit/scnprogram/isopaque)

### Providing Input for Metal Shaders

- [func handleBinding(ofBufferNamed: String, frequency: SCNBufferFrequency, handler: SCNBufferBindingBlock)](/documentation/scenekit/scnprogram/handlebinding(ofbuffernamed:frequency:handler:))
- [SCNBufferFrequency](/documentation/scenekit/scnbufferfrequency)

#### Constants

- [case perFrame](/documentation/scenekit/scnbufferfrequency/perframe)
- [case perNode](/documentation/scenekit/scnbufferfrequency/pernode)
- [case perShadable](/documentation/scenekit/scnbufferfrequency/pershadable)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnbufferfrequency/init(rawvalue:))
- [SCNBufferBindingBlock](/documentation/scenekit/scnbufferbindingblock)

### Working With Metal Shaders

- [var vertexFunctionName: String?](/documentation/scenekit/scnprogram/vertexfunctionname)
- [var fragmentFunctionName: String?](/documentation/scenekit/scnprogram/fragmentfunctionname)
- [var library: (any MTLLibrary)?](/documentation/scenekit/scnprogram/library)
- [SCNBufferStream](/documentation/scenekit/scnbufferstream)

### Writing Data to a Buffer

- [func writeBytes(UnsafeRawPointer, count: Int)](/documentation/scenekit/scnbufferstream/writebytes(_:count:))
- [SCNTechnique](/documentation/scenekit/scntechnique)

### Creating a Technique

- [init?(dictionary: [String : Any])](/documentation/scenekit/scntechnique/init(dictionary:))

### Combining Techniques

- [init?(bySequencingTechniques: [SCNTechnique])](/documentation/scenekit/scntechnique/init(bysequencingtechniques:))

### Retrieving a Technique’s Definition

- [var dictionaryRepresentation: [String : Any]](/documentation/scenekit/scntechnique/dictionaryrepresentation)

### Handling Parameters for a Technique’s Shader Programs

- [func handleBinding(ofSymbol: String, using: SCNBindingBlock?)](/documentation/scenekit/scntechnique/handlebinding(ofsymbol:using:))
- [func setObject(Any?, forKeyedSubscript: any NSCopying)](/documentation/scenekit/scntechnique/setobject(_:forkeyedsubscript:))
- [subscript(Any) -> Any?](/documentation/scenekit/scntechnique/subscript(_:))

### Instance Properties

- [var library: (any MTLLibrary)?](/documentation/scenekit/scntechnique/library)
- [SCNTechniqueSupport](/documentation/scenekit/scntechniquesupport)

### Specifying a Technique

- [var technique: SCNTechnique?](/documentation/scenekit/scntechniquesupport/technique)
- [SCNNodeRendererDelegate](/documentation/scenekit/scnnoderendererdelegate)

### Customizing the Rendering of a Node

- [func renderNode(SCNNode, renderer: SCNRenderer, arguments: [String : Any])](/documentation/scenekit/scnnoderendererdelegate/rendernode(_:renderer:arguments:))
- [Postprocessing a Scene With Custom Symbols](/documentation/scenekit/postprocessing-a-scene-with-custom-symbols)

## Scene Asset Import

- [SCNSceneSource](/documentation/scenekit/scnscenesource)

### Creating a Scene Source

- [init?(url: URL, options: [SCNSceneSource.LoadingOption : Any]?)](/documentation/scenekit/scnscenesource/init(url:options:))
- [init?(data: Data, options: [SCNSceneSource.LoadingOption : Any]?)](/documentation/scenekit/scnscenesource/init(data:options:))

### Loading a Complete Scene

- [func scene(options: [SCNSceneSource.LoadingOption : Any]?, statusHandler: SCNSceneSourceStatusHandler?) -> SCNScene?](/documentation/scenekit/scnscenesource/scene(options:statushandler:))
- [func scene(options: [SCNSceneSource.LoadingOption : Any]?) throws -> SCNScene](/documentation/scenekit/scnscenesource/scene(options:))

### Loading and Inspecting Scene Elements

- [func identifiersOfEntries(withClass: AnyClass) -> [String]](/documentation/scenekit/scnscenesource/identifiersofentries(withclass:))
- [func entryWithIdentifier<T>(String, withClass: T.Type) -> T?](/documentation/scenekit/scnscenesource/entrywithidentifier(_:withclass:))
- [func entries(passingTest: (Any, String, UnsafeMutablePointer<ObjCBool>) -> Bool) -> [Any]](/documentation/scenekit/scnscenesource/entries(passingtest:))

### Getting Information about the Scene

- [var url: URL?](/documentation/scenekit/scnscenesource/url)
- [var data: Data?](/documentation/scenekit/scnscenesource/data)
- [func property(forKey: String) -> Any?](/documentation/scenekit/scnscenesource/property(forkey:))

### Constants

- [SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption)

#### Type Properties

- [static let animationImportPolicy: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/animationimportpolicy)
- [SCNSceneSource.AnimationImportPolicy](/documentation/scenekit/scnscenesource/animationimportpolicy)

##### Type Properties

- [static let doNotPlay: SCNSceneSource.AnimationImportPolicy](/documentation/scenekit/scnscenesource/animationimportpolicy/donotplay)
- [static let play: SCNSceneSource.AnimationImportPolicy](/documentation/scenekit/scnscenesource/animationimportpolicy/play)
- [static let playRepeatedly: SCNSceneSource.AnimationImportPolicy](/documentation/scenekit/scnscenesource/animationimportpolicy/playrepeatedly)
- [static let playUsingSceneTimeBase: SCNSceneSource.AnimationImportPolicy](/documentation/scenekit/scnscenesource/animationimportpolicy/playusingscenetimebase)

##### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnscenesource/animationimportpolicy/init(rawvalue:))
- [static let assetDirectoryURLs: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/assetdirectoryurls)
- [static let checkConsistency: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/checkconsistency)
- [static let convertToYUp: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/converttoyup)
- [static let convertUnitsToMeters: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/convertunitstometers)
- [static let createNormalsIfAbsent: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/createnormalsifabsent)
- [static let flattenScene: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/flattenscene)
- [static let overrideAssetURLs: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/overrideasseturls)
- [static let preserveOriginalTopology: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/preserveoriginaltopology)
- [static let strictConformance: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/strictconformance)
- [static let useSafeMode: SCNSceneSource.LoadingOption](/documentation/scenekit/scnscenesource/loadingoption/usesafemode)

#### Initializers

- [init(rawValue: String)](/documentation/scenekit/scnscenesource/loadingoption/init(rawvalue:))
- [Scene Source Properties](/documentation/scenekit/scene-source-properties)

#### Constants

- [let SCNSceneSourceAssetContributorsKey: String](/documentation/scenekit/scnscenesourceassetcontributorskey)
- [let SCNSceneSourceAssetCreatedDateKey: String](/documentation/scenekit/scnscenesourceassetcreateddatekey)
- [let SCNSceneSourceAssetModifiedDateKey: String](/documentation/scenekit/scnscenesourceassetmodifieddatekey)
- [let SCNSceneSourceAssetUpAxisKey: String](/documentation/scenekit/scnscenesourceassetupaxiskey)
- [let SCNSceneSourceAssetUnitKey: String](/documentation/scenekit/scnscenesourceassetunitkey)
- [Contributor Keys](/documentation/scenekit/contributor-keys)

#### Constants

- [let SCNSceneSourceAssetAuthoringToolKey: String](/documentation/scenekit/scnscenesourceassetauthoringtoolkey)
- [let SCNSceneSourceAssetAuthorKey: String](/documentation/scenekit/scnscenesourceassetauthorkey)
- [Unit Dictionary Keys](/documentation/scenekit/unit-dictionary-keys)

#### Constants

- [let SCNSceneSourceAssetUnitNameKey: String](/documentation/scenekit/scnscenesourceassetunitnamekey)
- [let SCNSceneSourceAssetUnitMeterKey: String](/documentation/scenekit/scnscenesourceassetunitmeterkey)
- [Scene Loading Error Keys](/documentation/scenekit/scene-loading-error-keys)

#### Constants

- [let SCNDetailedErrorsKey: String](/documentation/scenekit/scndetailederrorskey)
- [Scene File Consistency Error Keys](/documentation/scenekit/scene-file-consistency-error-keys)

#### Constants

- [let SCNConsistencyElementIDErrorKey: String](/documentation/scenekit/scnconsistencyelementiderrorkey)
- [let SCNConsistencyElementTypeErrorKey: String](/documentation/scenekit/scnconsistencyelementtypeerrorkey)
- [let SCNConsistencyLineNumberErrorKey: String](/documentation/scenekit/scnconsistencylinenumbererrorkey)
- [Scene File Consistency Check Error Codes](/documentation/scenekit/1573761-scene-file-consistency-check-err)

#### Constants

- [var SCNConsistencyInvalidURIError: Int](/documentation/scenekit/scnconsistencyinvalidurierror)
- [var SCNConsistencyInvalidCountError: Int](/documentation/scenekit/scnconsistencyinvalidcounterror)
- [var SCNConsistencyInvalidArgumentError: Int](/documentation/scenekit/scnconsistencyinvalidargumenterror)
- [var SCNConsistencyMissingElementError: Int](/documentation/scenekit/scnconsistencymissingelementerror)
- [var SCNConsistencyMissingAttributeError: Int](/documentation/scenekit/scnconsistencymissingattributeerror)
- [var SCNConsistencyXMLSchemaValidationError: Int](/documentation/scenekit/scnconsistencyxmlschemavalidationerror)
- [SCNSceneSourceStatusHandler](/documentation/scenekit/scnscenesourcestatushandler)
- [SCNSceneSourceStatus](/documentation/scenekit/scnscenesourcestatus)

#### Constants

- [case error](/documentation/scenekit/scnscenesourcestatus/error)
- [case parsing](/documentation/scenekit/scnscenesourcestatus/parsing)
- [case validating](/documentation/scenekit/scnscenesourcestatus/validating)
- [case processing](/documentation/scenekit/scnscenesourcestatus/processing)
- [case complete](/documentation/scenekit/scnscenesourcestatus/complete)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnscenesourcestatus/init(rawvalue:))

## JavaScript

- [func SCNExportJavaScriptModule(JSContext)](/documentation/scenekit/scnexportjavascriptmodule(_:))

## SceneKit Data Types

- [SceneKit 3D Data Types](/documentation/scenekit/scenekit-3d-data-types)

### Vectors

- [SCNVector3](/documentation/scenekit/scnvector3)

#### Components

- [var x: Float](/documentation/scenekit/scnvector3/x)
- [var y: Float](/documentation/scenekit/scnvector3/y)
- [var z: Float](/documentation/scenekit/scnvector3/z)

#### Creating Vectors

- [func SCNVector3Make(Float, Float, Float) -> SCNVector3](/documentation/scenekit/scnvector3make(_:_:_:))

#### Converting Vector Types

- [func SCNVector3FromGLKVector3(GLKVector3) -> SCNVector3](/documentation/scenekit/scnvector3fromglkvector3(_:))
- [func SCNVector3ToGLKVector3(SCNVector3) -> GLKVector3](/documentation/scenekit/scnvector3toglkvector3(_:))

#### Comparing Vectors

- [func SCNVector3EqualToVector3(SCNVector3, SCNVector3) -> Bool](/documentation/scenekit/scnvector3equaltovector3(_:_:))

#### Zero Constant

- [let SCNVector3Zero: SCNVector3](/documentation/scenekit/scnvector3zero)

#### Initializers

- [init()](/documentation/scenekit/scnvector3/init())
- [init(SIMD3<Double>)](/documentation/scenekit/scnvector3/init(_:)-10rap)
- [init(SIMD3<Float>)](/documentation/scenekit/scnvector3/init(_:)-9wg16)
- [init(Int, Int, Int)](/documentation/scenekit/scnvector3/init(_:_:_:)-2hhr6)
- [init(CGFloat, CGFloat, CGFloat)](/documentation/scenekit/scnvector3/init(_:_:_:)-50jm7)
- [init(Double, Double, Double)](/documentation/scenekit/scnvector3/init(_:_:_:)-7clbx)
- [init(Float, Float, Float)](/documentation/scenekit/scnvector3/init(_:_:_:)-8cwh7)
- [init(x: CGFloat, y: CGFloat, z: CGFloat)](/documentation/scenekit/scnvector3/init(x:y:z:)-28n6q)
- [init(x: Float, y: Float, z: Float)](/documentation/scenekit/scnvector3/init(x:y:z:)-mn27)
- [SCNVector4](/documentation/scenekit/scnvector4)

#### Components

- [var x: Float](/documentation/scenekit/scnvector4/x)
- [var y: Float](/documentation/scenekit/scnvector4/y)
- [var z: Float](/documentation/scenekit/scnvector4/z)
- [var w: Float](/documentation/scenekit/scnvector4/w)

#### Creating Vectors

- [func SCNVector4Make(Float, Float, Float, Float) -> SCNVector4](/documentation/scenekit/scnvector4make(_:_:_:_:))

#### Converting Vector Types

- [func SCNVector4FromGLKVector4(GLKVector4) -> SCNVector4](/documentation/scenekit/scnvector4fromglkvector4(_:))
- [func SCNVector4ToGLKVector4(SCNVector4) -> GLKVector4](/documentation/scenekit/scnvector4toglkvector4(_:))

#### Comparing Vectors

- [func SCNVector4EqualToVector4(SCNVector4, SCNVector4) -> Bool](/documentation/scenekit/scnvector4equaltovector4(_:_:))

#### Zero Constant

- [let SCNVector4Zero: SCNVector4](/documentation/scenekit/scnvector4zero)

#### Initializers

- [init()](/documentation/scenekit/scnvector4/init())
- [init(SIMD4<Double>)](/documentation/scenekit/scnvector4/init(_:)-5q2cx)
- [init(SIMD4<Float>)](/documentation/scenekit/scnvector4/init(_:)-6w6mx)
- [init(Int, Int, Int, Int)](/documentation/scenekit/scnvector4/init(_:_:_:_:)-6otq6)
- [init(Double, Double, Double, Double)](/documentation/scenekit/scnvector4/init(_:_:_:_:)-85e6w)
- [init(CGFloat, CGFloat, CGFloat, CGFloat)](/documentation/scenekit/scnvector4/init(_:_:_:_:)-93hx1)
- [init(Float, Float, Float, Float)](/documentation/scenekit/scnvector4/init(_:_:_:_:)-pk7r)
- [init(x: Float, y: Float, z: Float, w: Float)](/documentation/scenekit/scnvector4/init(x:y:z:w:)-37b3a)
- [init(x: CGFloat, y: CGFloat, z: CGFloat, w: CGFloat)](/documentation/scenekit/scnvector4/init(x:y:z:w:)-7hxmu)

### Transforms and Rotations

- [SCNMatrix4](/documentation/scenekit/scnmatrix4-swift.struct)

#### Creating Transform Matrices

- [func SCNMatrix4MakeTranslation(Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4maketranslation(_:_:_:))
- [func SCNMatrix4MakeRotation(Float, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4makerotation(_:_:_:_:))
- [func SCNMatrix4MakeScale(Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4makescale(_:_:_:))

#### Creating Matrices from Elements

- [init()](/documentation/scenekit/scnmatrix4-swift.struct/init())
- [init(double4x4)](/documentation/scenekit/scnmatrix4-swift.struct/init(_:)-bqz6)
- [init(double4x4)](/documentation/quartzcore/catransform3d/init(_:)-6euzs)
- [init(float4x4)](/documentation/scenekit/scnmatrix4-swift.struct/init(_:)-98ce8)
- [init(float4x4)](/documentation/quartzcore/catransform3d/init(_:)-6awvy)
- [init(m11: Float, m12: Float, m13: Float, m14: Float, m21: Float, m22: Float, m23: Float, m24: Float, m31: Float, m32: Float, m33: Float, m34: Float, m41: Float, m42: Float, m43: Float, m44: Float)](/documentation/scenekit/scnmatrix4-swift.struct/init(m11:m12:m13:m14:m21:m22:m23:m24:m31:m32:m33:m34:m41:m42:m43:m44:))

#### Performing Matrix Operations

- [func SCNMatrix4Translate(SCNMatrix4, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4translate(_:_:_:_:))
- [func SCNMatrix4Rotate(SCNMatrix4, Float, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4rotate(_:_:_:_:_:))
- [func SCNMatrix4Scale(SCNMatrix4, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4scale(_:_:_:_:))
- [func SCNMatrix4Invert(SCNMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4invert(_:))
- [func SCNMatrix4Mult(SCNMatrix4, SCNMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4mult(_:_:))

#### Converting Matrix Types

- [func SCNMatrix4FromGLKMatrix4(GLKMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4fromglkmatrix4(_:))
- [func SCNMatrix4ToGLKMatrix4(SCNMatrix4) -> GLKMatrix4](/documentation/scenekit/scnmatrix4toglkmatrix4(_:))

#### Comparing Matrices

- [func SCNMatrix4EqualToMatrix4(SCNMatrix4, SCNMatrix4) -> Bool](/documentation/scenekit/scnmatrix4equaltomatrix4(_:_:))
- [func SCNMatrix4IsIdentity(SCNMatrix4) -> Bool](/documentation/scenekit/scnmatrix4isidentity(_:))

#### Identity Constant

- [let SCNMatrix4Identity: SCNMatrix4](/documentation/scenekit/scnmatrix4identity)

#### Matrix Elements

- [var m11: Float](/documentation/scenekit/scnmatrix4-swift.struct/m11)
- [var m12: Float](/documentation/scenekit/scnmatrix4-swift.struct/m12)
- [var m13: Float](/documentation/scenekit/scnmatrix4-swift.struct/m13)
- [var m14: Float](/documentation/scenekit/scnmatrix4-swift.struct/m14)
- [var m21: Float](/documentation/scenekit/scnmatrix4-swift.struct/m21)
- [var m22: Float](/documentation/scenekit/scnmatrix4-swift.struct/m22)
- [var m23: Float](/documentation/scenekit/scnmatrix4-swift.struct/m23)
- [var m24: Float](/documentation/scenekit/scnmatrix4-swift.struct/m24)
- [var m31: Float](/documentation/scenekit/scnmatrix4-swift.struct/m31)
- [var m32: Float](/documentation/scenekit/scnmatrix4-swift.struct/m32)
- [var m33: Float](/documentation/scenekit/scnmatrix4-swift.struct/m33)
- [var m34: Float](/documentation/scenekit/scnmatrix4-swift.struct/m34)
- [var m41: Float](/documentation/scenekit/scnmatrix4-swift.struct/m41)
- [var m42: Float](/documentation/scenekit/scnmatrix4-swift.struct/m42)
- [var m43: Float](/documentation/scenekit/scnmatrix4-swift.struct/m43)
- [var m44: Float](/documentation/scenekit/scnmatrix4-swift.struct/m44)
- [SCNMatrix4](/documentation/scenekit/scnmatrix4-swift.typealias)

#### Creating Transform Matrices

- [func SCNMatrix4MakeTranslation(Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4maketranslation(_:_:_:))
- [func SCNMatrix4MakeRotation(Float, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4makerotation(_:_:_:_:))
- [func SCNMatrix4MakeScale(Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4makescale(_:_:_:))

#### Performing Matrix Operations

- [func SCNMatrix4Translate(SCNMatrix4, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4translate(_:_:_:_:))
- [func SCNMatrix4Rotate(SCNMatrix4, Float, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4rotate(_:_:_:_:_:))
- [func SCNMatrix4Scale(SCNMatrix4, Float, Float, Float) -> SCNMatrix4](/documentation/scenekit/scnmatrix4scale(_:_:_:_:))
- [func SCNMatrix4Invert(SCNMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4invert(_:))
- [func SCNMatrix4Mult(SCNMatrix4, SCNMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4mult(_:_:))

#### Converting Matrix Types

- [func SCNMatrix4FromGLKMatrix4(GLKMatrix4) -> SCNMatrix4](/documentation/scenekit/scnmatrix4fromglkmatrix4(_:))
- [func SCNMatrix4ToGLKMatrix4(SCNMatrix4) -> GLKMatrix4](/documentation/scenekit/scnmatrix4toglkmatrix4(_:))

#### Comparing Matrices

- [func SCNMatrix4EqualToMatrix4(SCNMatrix4, SCNMatrix4) -> Bool](/documentation/scenekit/scnmatrix4equaltomatrix4(_:_:))
- [func SCNMatrix4IsIdentity(SCNMatrix4) -> Bool](/documentation/scenekit/scnmatrix4isidentity(_:))

#### Identity Constant

- [let SCNMatrix4Identity: SCNMatrix4](/documentation/scenekit/scnmatrix4identity)

#### Matrix Elements

- [var m11: Float](/documentation/scenekit/scnmatrix4-swift.struct/m11)
- [var m12: Float](/documentation/scenekit/scnmatrix4-swift.struct/m12)
- [var m13: Float](/documentation/scenekit/scnmatrix4-swift.struct/m13)
- [var m14: Float](/documentation/scenekit/scnmatrix4-swift.struct/m14)
- [var m21: Float](/documentation/scenekit/scnmatrix4-swift.struct/m21)
- [var m22: Float](/documentation/scenekit/scnmatrix4-swift.struct/m22)
- [var m23: Float](/documentation/scenekit/scnmatrix4-swift.struct/m23)
- [var m24: Float](/documentation/scenekit/scnmatrix4-swift.struct/m24)
- [var m31: Float](/documentation/scenekit/scnmatrix4-swift.struct/m31)
- [var m32: Float](/documentation/scenekit/scnmatrix4-swift.struct/m32)
- [var m33: Float](/documentation/scenekit/scnmatrix4-swift.struct/m33)
- [var m34: Float](/documentation/scenekit/scnmatrix4-swift.struct/m34)
- [var m41: Float](/documentation/scenekit/scnmatrix4-swift.struct/m41)
- [var m42: Float](/documentation/scenekit/scnmatrix4-swift.struct/m42)
- [var m43: Float](/documentation/scenekit/scnmatrix4-swift.struct/m43)
- [var m44: Float](/documentation/scenekit/scnmatrix4-swift.struct/m44)
- [SCNQuaternion](/documentation/scenekit/scnquaternion)

### Scalars

- [SCNFloat](/documentation/scenekit/scnfloat)

## Macros

- [Macros](/documentation/scenekit/scenekit-macros)

### Macros

- [var SCN_ENABLE_METAL: Int32](/documentation/scenekit/scn_enable_metal)
- [var SCN_ENABLE_OPENGL: Int32](/documentation/scenekit/scn_enable_opengl)

## Reference

- [SceneKit Enumerations](/documentation/scenekit/scenekit-enumerations)

### Enumerations

- [SCNLightAreaType](/documentation/scenekit/scnlightareatype)

#### Enumeration Cases

- [case polygon](/documentation/scenekit/scnlightareatype/polygon)
- [case rectangle](/documentation/scenekit/scnlightareatype/rectangle)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnlightareatype/init(rawvalue:))
- [SCNLightProbeType](/documentation/scenekit/scnlightprobetype)

#### Enumeration Cases

- [case irradiance](/documentation/scenekit/scnlightprobetype/irradiance)
- [case radiance](/documentation/scenekit/scnlightprobetype/radiance)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnlightprobetype/init(rawvalue:))
- [SCNLightProbeUpdateType](/documentation/scenekit/scnlightprobeupdatetype)

#### Enumeration Cases

- [case never](/documentation/scenekit/scnlightprobeupdatetype/never)
- [case realtime](/documentation/scenekit/scnlightprobeupdatetype/realtime)

#### Initializers

- [init?(rawValue: Int)](/documentation/scenekit/scnlightprobeupdatetype/init(rawvalue:))
- [SceneKit Constants](/documentation/scenekit/scenekit-constants)

### Constants

- [var SCN_ENABLE_METAL: Int32](/documentation/scenekit/scn_enable_metal)
- [var SCN_ENABLE_OPENGL: Int32](/documentation/scenekit/scn_enable_opengl)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
