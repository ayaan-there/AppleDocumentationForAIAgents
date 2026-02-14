# SpriteKit Documentation

Source: https://sosumi.ai/documentation/spritekit

---
title: SpriteKit
source: https://developer.apple.com/documentation/spritekit
timestamp: 2026-02-13T19:02:31.775Z
---

## Essentials

- [Drawing SpriteKit Content in a View](/documentation/spritekit/drawing-spritekit-content-in-a-view)
- [SKScene](/documentation/spritekit/skscene)

### Creating a Scene from a File

- [Creating a Scene from a File](/documentation/spritekit/creating-a-scene-from-a-file)

### Creating a Scene Programmatically

- [init(size: CGSize)](/documentation/spritekit/skscene/init(size:))
- [var size: CGSize](/documentation/spritekit/skscene/size)

### Stretching Content to Fit the View

- [Scaling a Scene’s Content to Fit the View](/documentation/spritekit/scaling-a-scene-s-content-to-fit-the-view)
- [var scaleMode: SKSceneScaleMode](/documentation/spritekit/skscene/scalemode)
- [SKSceneScaleMode](/documentation/spritekit/skscenescalemode)

#### Constants

- [case fill](/documentation/spritekit/skscenescalemode/fill)
- [case aspectFill](/documentation/spritekit/skscenescalemode/aspectfill)
- [case aspectFit](/documentation/spritekit/skscenescalemode/aspectfit)
- [case resizeFill](/documentation/spritekit/skscenescalemode/resizefill)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skscenescalemode/init(rawvalue:))

### Configuring the Viewport

- [Positioning a Scene’s Origin Within its View](/documentation/spritekit/positioning-a-scene-s-origin-within-its-view)
- [var camera: SKCameraNode?](/documentation/spritekit/skscene/camera)
- [var anchorPoint: CGPoint](/documentation/spritekit/skscene/anchorpoint)

### Responding to Loading and Resizing Events

- [func sceneDidLoad()](/documentation/spritekit/skscene/scenedidload())
- [func didChangeSize(CGSize)](/documentation/spritekit/skscene/didchangesize(_:))
- [func willMove(from: SKView)](/documentation/spritekit/skscene/willmove(from:))
- [func didMove(to: SKView)](/documentation/spritekit/skscene/didmove(to:))

### Responding to Frame-Cycle Events

- [Responding to Frame-Cycle Events](/documentation/spritekit/responding-to-frame-cycle-events)
- [func update(TimeInterval)](/documentation/spritekit/skscene/update(_:))
- [func didEvaluateActions()](/documentation/spritekit/skscene/didevaluateactions())
- [func didSimulatePhysics()](/documentation/spritekit/skscene/didsimulatephysics())
- [func didApplyConstraints()](/documentation/spritekit/skscene/didapplyconstraints())
- [func didFinishUpdate()](/documentation/spritekit/skscene/didfinishupdate())

### Configuring a Delegate

- [Subclassing Scenes Versus Assigning a Delegate](/documentation/spritekit/subclassing-scenes-versus-assigning-a-delegate)
- [var delegate: (any SKSceneDelegate)?](/documentation/spritekit/skscene/delegate)
- [SKSceneDelegate](/documentation/spritekit/skscenedelegate)

#### Handling Animation Events

- [Use SpriteKit Objects within Scene Delegate Callbacks](/documentation/spritekit/use-spritekit-objects-within-scene-delegate-callbacks)
- [func update(TimeInterval, for: SKScene)](/documentation/spritekit/skscenedelegate/update(_:for:))
- [func didEvaluateActions(for: SKScene)](/documentation/spritekit/skscenedelegate/didevaluateactions(for:))
- [func didSimulatePhysics(for: SKScene)](/documentation/spritekit/skscenedelegate/didsimulatephysics(for:))
- [func didApplyConstraints(for: SKScene)](/documentation/spritekit/skscenedelegate/didapplyconstraints(for:))
- [func didFinishUpdate(for: SKScene)](/documentation/spritekit/skscenedelegate/didfinishupdate(for:))

### Setting the Background Appearance

- [Creating a Scene with a Transparent Background](/documentation/spritekit/creating-a-scene-with-a-transparent-background)
- [var view: SKView?](/documentation/spritekit/skscene/view)
- [var backgroundColor: UIColor](/documentation/spritekit/skscene/backgroundcolor)

### Configuring Physics Properties

- [var physicsWorld: SKPhysicsWorld](/documentation/spritekit/skscene/physicsworld)

### Adding Positional Audio

- [Using Audio Nodes with the Scene’s Listener](/documentation/spritekit/using-audio-nodes-with-the-scene-s-listener)
- [var listener: SKNode?](/documentation/spritekit/skscene/listener)
- [var audioEngine: AVAudioEngine](/documentation/spritekit/skscene/audioengine)

### Converting Between Coordinate Systems

- [func convertPoint(fromView: CGPoint) -> CGPoint](/documentation/spritekit/skscene/convertpoint(fromview:))
- [func convertPoint(toView: CGPoint) -> CGPoint](/documentation/spritekit/skscene/convertpoint(toview:))
- [Nodes for Scene Building](/documentation/spritekit/nodes-for-scene-building)

### Base Nodes

- [Using Base Nodes to Lay Out SpriteKit Content](/documentation/spritekit/using-base-nodes-to-lay-out-spritekit-content)
- [SKNode](/documentation/spritekit/sknode)

#### First Steps

- [Getting Started with Nodes](/documentation/spritekit/getting-started-with-nodes)
- [init()](/documentation/spritekit/sknode/init())
- [convenience init?(fileNamed: String)](/documentation/spritekit/sknode/init(filenamed:))
- [init?(coder: NSCoder)](/documentation/spritekit/sknode/init(coder:))
- [convenience init(fileNamed: String, securelyWithClasses: Set<AnyHashable>) throws](/documentation/spritekit/sknode/init(filenamed:securelywithclasses:))

#### Positioning Content in a Scene

- [var position: CGPoint](/documentation/spritekit/sknode/position)

#### Querying the Content Size

- [var frame: CGRect](/documentation/spritekit/sknode/frame)
- [func calculateAccumulatedFrame() -> CGRect](/documentation/spritekit/sknode/calculateaccumulatedframe())

#### Configuring Draw Order

- [About Node Drawing Order](/documentation/spritekit/about-node-drawing-order)
- [var zPosition: CGFloat](/documentation/spritekit/sknode/zposition)

#### Scaling and Rotating

- [var zRotation: CGFloat](/documentation/spritekit/sknode/zrotation)
- [func setScale(CGFloat)](/documentation/spritekit/sknode/setscale(_:))
- [var xScale: CGFloat](/documentation/spritekit/sknode/xscale)
- [var yScale: CGFloat](/documentation/spritekit/sknode/yscale)

#### Accessing Related Nodes

- [About SpriteKit Coordinate Systems](/documentation/spritekit/about-spritekit-coordinate-systems)
- [var scene: SKScene?](/documentation/spritekit/sknode/scene)
- [var parent: SKNode?](/documentation/spritekit/sknode/parent)
- [var children: [SKNode]](/documentation/spritekit/sknode/children)

#### Modifying the Node Tree

- [Accessing and Modifying the Node Tree](/documentation/spritekit/accessing-and-modifying-the-node-tree)
- [func addChild(SKNode)](/documentation/spritekit/sknode/addchild(_:))
- [func insertChild(SKNode, at: Int)](/documentation/spritekit/sknode/insertchild(_:at:))
- [func isEqual(to: SKNode) -> Bool](/documentation/spritekit/sknode/isequal(to:))
- [func move(toParent: SKNode)](/documentation/spritekit/sknode/move(toparent:))
- [func removeFromParent()](/documentation/spritekit/sknode/removefromparent())
- [func removeAllChildren()](/documentation/spritekit/sknode/removeallchildren())
- [func removeChildren(in: [SKNode])](/documentation/spritekit/sknode/removechildren(in:))
- [func inParentHierarchy(SKNode) -> Bool](/documentation/spritekit/sknode/inparenthierarchy(_:))

#### Customizing Nodes

- [Customizing the Behavior of a Node](/documentation/spritekit/customizing-the-behavior-of-a-node)

#### Propagating Properties to Children

- [About Node Property Propagation](/documentation/spritekit/about-node-property-propagation)

#### Accessing Nodes by Name

- [Searching the Node Tree](/documentation/spritekit/searching-the-node-tree)
- [var name: String?](/documentation/spritekit/sknode/name)
- [func childNode(withName: String) -> SKNode?](/documentation/spritekit/sknode/childnode(withname:))
- [func enumerateChildNodes(withName: String, using: (SKNode, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/spritekit/sknode/enumeratechildnodes(withname:using:))
- [subscript(String) -> [SKNode]](/documentation/spritekit/sknode/subscript(_:))

#### Altering Node Visibility

- [var alpha: CGFloat](/documentation/spritekit/sknode/alpha)
- [var isHidden: Bool](/documentation/spritekit/sknode/ishidden)

#### Running Actions

- [Getting Started with Actions](/documentation/spritekit/getting-started-with-actions)
- [func run(SKAction)](/documentation/spritekit/sknode/run(_:))
- [func run(SKAction, completion: () -> Void)](/documentation/spritekit/sknode/run(_:completion:))
- [func run(SKAction, withKey: String)](/documentation/spritekit/sknode/run(_:withkey:))
- [var speed: CGFloat](/documentation/spritekit/sknode/speed)
- [var isPaused: Bool](/documentation/spritekit/sknode/ispaused)
- [func action(forKey: String) -> SKAction?](/documentation/spritekit/sknode/action(forkey:))
- [func hasActions() -> Bool](/documentation/spritekit/sknode/hasactions())
- [func removeAllActions()](/documentation/spritekit/sknode/removeallactions())
- [func removeAction(forKey: String)](/documentation/spritekit/sknode/removeaction(forkey:))

#### Adding Physics Behaviors

- [Getting Started with Physics Bodies](/documentation/spritekit/getting-started-with-physics-bodies)
- [var physicsBody: SKPhysicsBody?](/documentation/spritekit/sknode/physicsbody)

#### Constraining Node Position or Rotation

- [var constraints: [SKConstraint]?](/documentation/spritekit/sknode/constraints)
- [var reachConstraints: SKReachConstraints?](/documentation/spritekit/sknode/reachconstraints)

#### Detecting Collisions Manually

- [func intersects(SKNode) -> Bool](/documentation/spritekit/sknode/intersects(_:))

#### Adding GameplayKit Behaviors

- [var entity: GKEntity?](/documentation/spritekit/sknode/entity)
- [class func obstacles(fromNodeBounds: [SKNode]) -> [GKPolygonObstacle]](/documentation/spritekit/sknode/obstacles(fromnodebounds:))
- [class func obstacles(fromNodePhysicsBodies: [SKNode]) -> [GKPolygonObstacle]](/documentation/spritekit/sknode/obstacles(fromnodephysicsbodies:))
- [class func obstacles(fromSpriteTextures: [SKNode], accuracy: Float) -> [GKPolygonObstacle]](/documentation/spritekit/sknode/obstacles(fromspritetextures:accuracy:))

#### Handling User Input

- [Controlling User Interaction on Nodes](/documentation/spritekit/controlling-user-interaction-on-nodes)
- [var isUserInteractionEnabled: Bool](/documentation/spritekit/sknode/isuserinteractionenabled)
- [var focusBehavior: SKNodeFocusBehavior](/documentation/spritekit/sknode/focusbehavior)

#### Hit Testing

- [Understanding Hit-Testing](/documentation/spritekit/understanding-hit-testing)
- [func contains(CGPoint) -> Bool](/documentation/spritekit/sknode/contains(_:))
- [func atPoint(CGPoint) -> SKNode](/documentation/spritekit/sknode/atpoint(_:))
- [func nodes(at: CGPoint) -> [SKNode]](/documentation/spritekit/sknode/nodes(at:))

#### Converting Between Coordinate Systems of Different Nodes

- [Converting Coordinate Spaces](/documentation/spritekit/converting-coordinate-spaces)
- [func convert(CGPoint, from: SKNode) -> CGPoint](/documentation/spritekit/sknode/convert(_:from:))
- [func convert(CGPoint, to: SKNode) -> CGPoint](/documentation/spritekit/sknode/convert(_:to:))

#### Adding Custom Data Without Subclassing

- [var userData: NSMutableDictionary?](/documentation/spritekit/sknode/userdata)

#### Providing Accessibility

- [var accessibilityChildren: [Any]?](/documentation/spritekit/sknode/accessibilitychildren)
- [var accessibilityFrame: CGRect](/documentation/spritekit/sknode/accessibilityframe)
- [var accessibilityHelp: String?](/documentation/spritekit/sknode/accessibilityhelp)
- [var accessibilityLabel: String?](/documentation/spritekit/sknode/accessibilitylabel)
- [var accessibilityParent: AnyObject?](/documentation/spritekit/sknode/accessibilityparent)
- [var accessibilityRole: String?](/documentation/spritekit/sknode/accessibilityrole)
- [var accessibilityRoleDescription: String?](/documentation/spritekit/sknode/accessibilityroledescription)
- [var accessibilitySubrole: String?](/documentation/spritekit/sknode/accessibilitysubrole)
- [var isAccessibilityElement: Bool](/documentation/spritekit/sknode/isaccessibilityelement)
- [var isAccessibilityEnabled: Bool](/documentation/spritekit/sknode/isaccessibilityenabled)
- [func accessibilityHitTest(CGPoint) -> Any?](/documentation/spritekit/sknode/accessibilityhittest(_:))

#### Setting a Node’s Unique Attributes for a Shader

- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/sknode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/sknode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/sknode/value(forattributenamed:))
- [SKCameraNode](/documentation/spritekit/skcameranode)

#### First Steps

- [Getting Started with a Camera](/documentation/spritekit/getting-started-with-a-camera)

#### Node Visibility

- [func containedNodeSet() -> Set<SKNode>](/documentation/spritekit/skcameranode/containednodeset())
- [func contains(SKNode) -> Bool](/documentation/spritekit/skcameranode/contains(_:))
- [SKReferenceNode](/documentation/spritekit/skreferencenode)

#### Initializers

- [convenience init(url: URL)](/documentation/spritekit/skreferencenode/init(url:)-3jryz)
- [init(url: URL?)](/documentation/spritekit/skreferencenode/init(url:)-429mo)
- [convenience init(fileNamed: String)](/documentation/spritekit/skreferencenode/init(filenamed:)-77gs0)
- [init(fileNamed: String?)](/documentation/spritekit/skreferencenode/init(filenamed:)-2yeh2)
- [init?(coder: NSCoder)](/documentation/spritekit/skreferencenode/init(coder:))

#### Regenerating

- [func resolve()](/documentation/spritekit/skreferencenode/resolve())

#### Loading Callback

- [func didLoad(SKNode?)](/documentation/spritekit/skreferencenode/didload(_:))

### Nodes that Draw

- [Maximizing Node Drawing Performance](/documentation/spritekit/maximizing-node-drawing-performance)
- [SKSpriteNode](/documentation/spritekit/skspritenode)

#### Creating a Sprite from an Image Filename

- [Getting Started with Sprite Nodes](/documentation/spritekit/getting-started-with-sprite-nodes)
- [convenience init(imageNamed: String)](/documentation/spritekit/skspritenode/init(imagenamed:))
- [convenience init(imageNamed: String, normalMapped: Bool)](/documentation/spritekit/skspritenode/init(imagenamed:normalmapped:))

#### Creating a Sprite from a Texture

- [convenience init(texture: SKTexture?)](/documentation/spritekit/skspritenode/init(texture:))
- [init(texture: SKTexture?, color: UIColor, size: CGSize)](/documentation/spritekit/skspritenode/init(texture:color:size:))
- [convenience init(texture: SKTexture?, size: CGSize)](/documentation/spritekit/skspritenode/init(texture:size:))
- [convenience init(texture: SKTexture?, normalMap: SKTexture?)](/documentation/spritekit/skspritenode/init(texture:normalmap:))
- [var texture: SKTexture?](/documentation/spritekit/skspritenode/texture)

#### Creating a Solid-Color Sprite

- [convenience init(color: UIColor, size: CGSize)](/documentation/spritekit/skspritenode/init(color:size:))

#### Initializing a Sprite from an Archive

- [init?(coder: NSCoder)](/documentation/spritekit/skspritenode/init(coder:))

#### Setting a Sprite’s Size and Position

- [Using the Anchor Point to Move a Sprite](/documentation/spritekit/using-the-anchor-point-to-move-a-sprite)
- [var size: CGSize](/documentation/spritekit/skspritenode/size)
- [func scale(to: CGSize)](/documentation/spritekit/skspritenode/scale(to:))
- [var anchorPoint: CGPoint](/documentation/spritekit/skspritenode/anchorpoint)

#### Scaling a Sprite in Nine Parts

- [Resizing a Sprite in Nine Parts](/documentation/spritekit/resizing-a-sprite-in-nine-parts)
- [var centerRect: CGRect](/documentation/spritekit/skspritenode/centerrect)

#### Tinting a Sprite

- [Tinting a Sprite](/documentation/spritekit/tinting-a-sprite)
- [var color: UIColor](/documentation/spritekit/skspritenode/color)
- [var colorBlendFactor: CGFloat](/documentation/spritekit/skspritenode/colorblendfactor)

#### Configuring Alpha Blendling

- [Blending a Sprite with Different Interpretations of Alpha](/documentation/spritekit/blending-a-sprite-with-different-interpretations-of-alpha)
- [var blendMode: SKBlendMode](/documentation/spritekit/skspritenode/blendmode)
- [SKBlendMode](/documentation/spritekit/skblendmode)

##### Constants

- [case alpha](/documentation/spritekit/skblendmode/alpha)
- [case add](/documentation/spritekit/skblendmode/add)
- [case subtract](/documentation/spritekit/skblendmode/subtract)
- [case multiply](/documentation/spritekit/skblendmode/multiply)
- [case multiplyX2](/documentation/spritekit/skblendmode/multiplyx2)
- [case screen](/documentation/spritekit/skblendmode/screen)
- [case replace](/documentation/spritekit/skblendmode/replace)

##### Enumeration Cases

- [case multiplyAlpha](/documentation/spritekit/skblendmode/multiplyalpha)

##### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skblendmode/init(rawvalue:))

#### Lighting a Sprite

- [Lighting a Sprite with Light Nodes](/documentation/spritekit/lighting-a-sprite-with-light-nodes)
- [var lightingBitMask: UInt32](/documentation/spritekit/skspritenode/lightingbitmask)
- [var shadowedBitMask: UInt32](/documentation/spritekit/skspritenode/shadowedbitmask)
- [var shadowCastBitMask: UInt32](/documentation/spritekit/skspritenode/shadowcastbitmask)
- [var normalTexture: SKTexture?](/documentation/spritekit/skspritenode/normaltexture)

#### Adding a Custom Shader to a Sprite

- [Applying Shaders to a Sprite](/documentation/spritekit/applying-shaders-to-a-sprite)
- [var shader: SKShader?](/documentation/spritekit/skspritenode/shader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/skspritenode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/skspritenode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/skspritenode/value(forattributenamed:))

#### Animating a Sprite by Changing its Texture

- [Animating a Sprite by Changing its Texture](/documentation/spritekit/animating-a-sprite-by-changing-its-texture)

#### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/spritekit/skspritenode/customplaygroundquicklook)
- [SKShapeNode](/documentation/spritekit/skshapenode)

#### First Steps

- [Getting Started with Shape Nodes](/documentation/spritekit/getting-started-with-shape-nodes)

#### Creating a Shape from a Path

- [convenience init(path: CGPath)](/documentation/spritekit/skshapenode/init(path:))
- [convenience init(path: CGPath, centered: Bool)](/documentation/spritekit/skshapenode/init(path:centered:))
- [var path: CGPath?](/documentation/spritekit/skshapenode/path)

#### Creating a Shape from a Rectangle

- [convenience init(rect: CGRect)](/documentation/spritekit/skshapenode/init(rect:))
- [convenience init(rectOf: CGSize)](/documentation/spritekit/skshapenode/init(rectof:))
- [convenience init(rect: CGRect, cornerRadius: CGFloat)](/documentation/spritekit/skshapenode/init(rect:cornerradius:))
- [convenience init(rectOf: CGSize, cornerRadius: CGFloat)](/documentation/spritekit/skshapenode/init(rectof:cornerradius:))

#### Creating a Circle Shape

- [convenience init(circleOfRadius: CGFloat)](/documentation/spritekit/skshapenode/init(circleofradius:))

#### Creating an Ellipse Shape

- [convenience init(ellipseOf: CGSize)](/documentation/spritekit/skshapenode/init(ellipseof:))
- [convenience init(ellipseIn: CGRect)](/documentation/spritekit/skshapenode/init(ellipsein:))

#### Creating a Shape from an Array of Points

- [Creating a Shape Node from an Array of Points](/documentation/spritekit/creating-a-shape-node-from-an-array-of-points)
- [convenience init(points: UnsafeMutablePointer<CGPoint>, count: Int)](/documentation/spritekit/skshapenode/init(points:count:))
- [convenience init(splinePoints: UnsafeMutablePointer<CGPoint>, count: Int)](/documentation/spritekit/skshapenode/init(splinepoints:count:))

#### Filling a Shape

- [var fillColor: UIColor](/documentation/spritekit/skshapenode/fillcolor)
- [var fillTexture: SKTexture?](/documentation/spritekit/skshapenode/filltexture)

#### Stroking a Shape

- [var lineWidth: CGFloat](/documentation/spritekit/skshapenode/linewidth)
- [var strokeColor: UIColor](/documentation/spritekit/skshapenode/strokecolor)
- [var strokeTexture: SKTexture?](/documentation/spritekit/skshapenode/stroketexture)
- [var glowWidth: CGFloat](/documentation/spritekit/skshapenode/glowwidth)
- [var lineCap: CGLineCap](/documentation/spritekit/skshapenode/linecap)
- [var lineJoin: CGLineJoin](/documentation/spritekit/skshapenode/linejoin)
- [var miterLimit: CGFloat](/documentation/spritekit/skshapenode/miterlimit)
- [var isAntialiased: Bool](/documentation/spritekit/skshapenode/isantialiased)

#### Configuring Alpha Blending

- [var blendMode: SKBlendMode](/documentation/spritekit/skshapenode/blendmode)

#### Controlling or Animating Sroke Length

- [var lineLength: CGFloat](/documentation/spritekit/skshapenode/linelength)

#### Customizing Stroking or Fill Drawing

- [Controlling Shape Drawing with Shaders](/documentation/spritekit/controlling-shape-drawing-with-shaders)
- [var strokeShader: SKShader?](/documentation/spritekit/skshapenode/strokeshader)
- [var fillShader: SKShader?](/documentation/spritekit/skshapenode/fillshader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/skshapenode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/skshapenode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/skshapenode/value(forattributenamed:))

#### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/spritekit/skshapenode/customplaygroundquicklook)
- [SKEmitterNode](/documentation/spritekit/skemitternode)

#### First Steps

- [Creating Particle Effects](/documentation/spritekit/creating-particle-effects)

#### Choosing Which Node in the Scene Emits Particles

- [Changing the Location of Particles in Your Scene](/documentation/spritekit/changing-the-location-of-particles-in-your-scene)
- [var targetNode: SKNode?](/documentation/spritekit/skemitternode/targetnode)

#### Controlling When Particles Are Created

- [func advanceSimulationTime(TimeInterval)](/documentation/spritekit/skemitternode/advancesimulationtime(_:))
- [func resetSimulation()](/documentation/spritekit/skemitternode/resetsimulation())
- [var particleBirthRate: CGFloat](/documentation/spritekit/skemitternode/particlebirthrate)
- [var numParticlesToEmit: Int](/documentation/spritekit/skemitternode/numparticlestoemit)

#### Controlling the Rendering Order of an Emitter’s Particles

- [var particleRenderOrder: SKParticleRenderOrder](/documentation/spritekit/skemitternode/particlerenderorder)
- [SKParticleRenderOrder](/documentation/spritekit/skparticlerenderorder)

##### Constants

- [case oldestLast](/documentation/spritekit/skparticlerenderorder/oldestlast)
- [case oldestFirst](/documentation/spritekit/skparticlerenderorder/oldestfirst)
- [case dontCare](/documentation/spritekit/skparticlerenderorder/dontcare)

##### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/skparticlerenderorder/init(rawvalue:))

#### Controlling Particle Lifetime

- [var particleLifetime: CGFloat](/documentation/spritekit/skemitternode/particlelifetime)
- [var particleLifetimeRange: CGFloat](/documentation/spritekit/skemitternode/particlelifetimerange)

#### Controlling Particle Position

- [var particlePosition: CGPoint](/documentation/spritekit/skemitternode/particleposition)
- [var particlePositionRange: CGVector](/documentation/spritekit/skemitternode/particlepositionrange)
- [var particleZPosition: CGFloat](/documentation/spritekit/skemitternode/particlezposition)
- [var particleZPositionRange: CGFloat](/documentation/spritekit/skemitternode/particlezpositionrange)

#### Controlling Particle Velocity and Acceleration

- [var particleSpeed: CGFloat](/documentation/spritekit/skemitternode/particlespeed)
- [var particleSpeedRange: CGFloat](/documentation/spritekit/skemitternode/particlespeedrange)
- [var emissionAngle: CGFloat](/documentation/spritekit/skemitternode/emissionangle)
- [var emissionAngleRange: CGFloat](/documentation/spritekit/skemitternode/emissionanglerange)
- [var xAcceleration: CGFloat](/documentation/spritekit/skemitternode/xacceleration)
- [var yAcceleration: CGFloat](/documentation/spritekit/skemitternode/yacceleration)
- [var particleZPositionSpeed: CGFloat](/documentation/spritekit/skemitternode/particlezpositionspeed)

#### Adjusting a Particle’s Rotation

- [var particleRotation: CGFloat](/documentation/spritekit/skemitternode/particlerotation)
- [var particleRotationRange: CGFloat](/documentation/spritekit/skemitternode/particlerotationrange)
- [var particleRotationSpeed: CGFloat](/documentation/spritekit/skemitternode/particlerotationspeed)

#### Scaling Particles by a Factor

- [var particleScale: CGFloat](/documentation/spritekit/skemitternode/particlescale)
- [var particleScaleRange: CGFloat](/documentation/spritekit/skemitternode/particlescalerange)
- [var particleScaleSpeed: CGFloat](/documentation/spritekit/skemitternode/particlescalespeed)
- [var particleScaleSequence: SKKeyframeSequence?](/documentation/spritekit/skemitternode/particlescalesequence)

#### Changing a Particle’s Source Image and Size

- [var particleTexture: SKTexture?](/documentation/spritekit/skemitternode/particletexture)
- [var particleSize: CGSize](/documentation/spritekit/skemitternode/particlesize)

#### Configuring Particle Color

- [var particleColorSequence: SKKeyframeSequence?](/documentation/spritekit/skemitternode/particlecolorsequence)
- [var particleColor: UIColor](/documentation/spritekit/skemitternode/particlecolor)
- [var particleColorAlphaRange: CGFloat](/documentation/spritekit/skemitternode/particlecoloralpharange)
- [var particleColorBlueRange: CGFloat](/documentation/spritekit/skemitternode/particlecolorbluerange)
- [var particleColorGreenRange: CGFloat](/documentation/spritekit/skemitternode/particlecolorgreenrange)
- [var particleColorRedRange: CGFloat](/documentation/spritekit/skemitternode/particlecolorredrange)
- [var particleColorAlphaSpeed: CGFloat](/documentation/spritekit/skemitternode/particlecoloralphaspeed)
- [var particleColorBlueSpeed: CGFloat](/documentation/spritekit/skemitternode/particlecolorbluespeed)
- [var particleColorGreenSpeed: CGFloat](/documentation/spritekit/skemitternode/particlecolorgreenspeed)
- [var particleColorRedSpeed: CGFloat](/documentation/spritekit/skemitternode/particlecolorredspeed)

#### Controlling How the Texture is Blended with Particle Color

- [var particleColorBlendFactorSequence: SKKeyframeSequence?](/documentation/spritekit/skemitternode/particlecolorblendfactorsequence)
- [var particleColorBlendFactor: CGFloat](/documentation/spritekit/skemitternode/particlecolorblendfactor)
- [var particleColorBlendFactorRange: CGFloat](/documentation/spritekit/skemitternode/particlecolorblendfactorrange)
- [var particleColorBlendFactorSpeed: CGFloat](/documentation/spritekit/skemitternode/particlecolorblendfactorspeed)

#### Blending Particles with the Framebuffer

- [var particleBlendMode: SKBlendMode](/documentation/spritekit/skemitternode/particleblendmode)
- [var particleAlphaSequence: SKKeyframeSequence?](/documentation/spritekit/skemitternode/particlealphasequence)
- [var particleAlpha: CGFloat](/documentation/spritekit/skemitternode/particlealpha)
- [var particleAlphaRange: CGFloat](/documentation/spritekit/skemitternode/particlealpharange)
- [var particleAlphaSpeed: CGFloat](/documentation/spritekit/skemitternode/particlealphaspeed)

#### Animating Particles

- [Animating Particle Properties Across Disparate Values](/documentation/spritekit/animating-particle-properties-across-disparate-values)
- [var particleAction: SKAction?](/documentation/spritekit/skemitternode/particleaction)

#### Applying Physics Fields to the Particles

- [var fieldBitMask: UInt32](/documentation/spritekit/skemitternode/fieldbitmask)

#### Taking Full Control of Particle Drawing with a Shader

- [Getting Started with Particle Shaders](/documentation/spritekit/getting-started-with-particle-shaders)
- [var shader: SKShader?](/documentation/spritekit/skemitternode/shader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/skemitternode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/skemitternode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/skemitternode/value(forattributenamed:))

#### Maximizing Particle Run-Time Performance

- [Optimizing Emitter Node Performance](/documentation/spritekit/optimizing-emitter-node-performance)
- [SKLabelNode](/documentation/spritekit/sklabelnode)

#### Getting Started with Labels

- [Adding Text to a Scene](/documentation/spritekit/adding-text-to-a-scene)

#### Creating a Label

- [init(fontNamed: String?)](/documentation/spritekit/sklabelnode/init(fontnamed:))
- [convenience init(text: String?)](/documentation/spritekit/sklabelnode/init(text:))
- [convenience init(attributedText: NSAttributedString?)](/documentation/spritekit/sklabelnode/init(attributedtext:))

#### Setting a Label’s Text

- [var text: String?](/documentation/spritekit/sklabelnode/text)
- [var attributedText: NSAttributedString?](/documentation/spritekit/sklabelnode/attributedtext)

#### Specifying a Label’s Font

- [var fontColor: UIColor?](/documentation/spritekit/sklabelnode/fontcolor)
- [var fontName: String?](/documentation/spritekit/sklabelnode/fontname)
- [var fontSize: CGFloat](/documentation/spritekit/sklabelnode/fontsize)

#### Controlling a Label’s Alignment

- [var verticalAlignmentMode: SKLabelVerticalAlignmentMode](/documentation/spritekit/sklabelnode/verticalalignmentmode)
- [SKLabelVerticalAlignmentMode](/documentation/spritekit/sklabelverticalalignmentmode)

##### Constants

- [case baseline](/documentation/spritekit/sklabelverticalalignmentmode/baseline)
- [case center](/documentation/spritekit/sklabelverticalalignmentmode/center)
- [case top](/documentation/spritekit/sklabelverticalalignmentmode/top)
- [case bottom](/documentation/spritekit/sklabelverticalalignmentmode/bottom)

##### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sklabelverticalalignmentmode/init(rawvalue:))
- [var horizontalAlignmentMode: SKLabelHorizontalAlignmentMode](/documentation/spritekit/sklabelnode/horizontalalignmentmode)
- [SKLabelHorizontalAlignmentMode](/documentation/spritekit/sklabelhorizontalalignmentmode)

##### Constants

- [case center](/documentation/spritekit/sklabelhorizontalalignmentmode/center)
- [case left](/documentation/spritekit/sklabelhorizontalalignmentmode/left)
- [case right](/documentation/spritekit/sklabelhorizontalalignmentmode/right)

##### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sklabelhorizontalalignmentmode/init(rawvalue:))

#### Defining a Label’s Line-Breaking Behavior

- [var preferredMaxLayoutWidth: CGFloat](/documentation/spritekit/sklabelnode/preferredmaxlayoutwidth)
- [var lineBreakMode: NSLineBreakMode](/documentation/spritekit/sklabelnode/linebreakmode)
- [var numberOfLines: Int](/documentation/spritekit/sklabelnode/numberoflines)

#### Colorizing a Label

- [var color: UIColor?](/documentation/spritekit/sklabelnode/color)
- [var colorBlendFactor: CGFloat](/documentation/spritekit/sklabelnode/colorblendfactor)

#### Configuring Alpha Blending

- [var blendMode: SKBlendMode](/documentation/spritekit/sklabelnode/blendmode)
- [SKVideoNode](/documentation/spritekit/skvideonode)

#### Getting Started with Video

- [Adding a Video to a Scene](/documentation/spritekit/adding-a-video-to-a-scene)

#### Creating a Video Node

- [init(avPlayer: AVPlayer)](/documentation/spritekit/skvideonode/init(avplayer:))
- [init(fileNamed: String)](/documentation/spritekit/skvideonode/init(filenamed:))
- [init(url: URL)](/documentation/spritekit/skvideonode/init(url:))
- [init?(coder: NSCoder)](/documentation/spritekit/skvideonode/init(coder:))
- [init(videoFileNamed: String)](/documentation/spritekit/skvideonode/init(videofilenamed:))
- [init(videoURL: URL)](/documentation/spritekit/skvideonode/init(videourl:))

#### Setting the Video Node’s Visual Properties

- [var anchorPoint: CGPoint](/documentation/spritekit/skvideonode/anchorpoint)
- [var size: CGSize](/documentation/spritekit/skvideonode/size)

#### Controlling Video Playback

- [func play()](/documentation/spritekit/skvideonode/play())
- [func pause()](/documentation/spritekit/skvideonode/pause())
- [SKTileMapNode](/documentation/spritekit/sktilemapnode)

#### Creating a Tile Map Programmatically

- [Creating a Tile Map Programmatically](/documentation/spritekit/creating-a-tile-map-programmatically)

##### Creating a Tile Map

- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize)](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:))
- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, fillWith: SKTileGroup)](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:fillwith:))
- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, tileGroupLayout: [SKTileGroup])](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:tilegrouplayout:))
- [class func tileMapNodes(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, from: GKNoiseMap, tileTypeNoiseMapThresholds: [NSNumber]) -> [SKTileMapNode]](/documentation/spritekit/sktilemapnode/tilemapnodes(tileset:columns:rows:tilesize:from:tiletypenoisemapthresholds:))

##### Defining a Tile Map’s Contents

- [var enableAutomapping: Bool](/documentation/spritekit/sktilemapnode/enableautomapping)
- [func fill(with: SKTileGroup?)](/documentation/spritekit/sktilemapnode/fill(with:))
- [func setTileGroup(SKTileGroup, andTileDefinition: SKTileDefinition, forColumn: Int, row: Int)](/documentation/spritekit/sktilemapnode/settilegroup(_:andtiledefinition:forcolumn:row:))
- [func setTileGroup(SKTileGroup?, forColumn: Int, row: Int)](/documentation/spritekit/sktilemapnode/settilegroup(_:forcolumn:row:))

#### Controlling a Tile Map’s On-Screen Position Relative to its Origin

- [var anchorPoint: CGPoint](/documentation/spritekit/sktilemapnode/anchorpoint)

#### Reading or Manually Configuring the Tile Map’s Size

- [var tileSize: CGSize](/documentation/spritekit/sktilemapnode/tilesize)
- [var tileSet: SKTileSet](/documentation/spritekit/sktilemapnode/tileset)
- [var numberOfColumns: Int](/documentation/spritekit/sktilemapnode/numberofcolumns)
- [var numberOfRows: Int](/documentation/spritekit/sktilemapnode/numberofrows)

#### Querying the Tile Map’s Properties

- [func centerOfTile(atColumn: Int, row: Int) -> CGPoint](/documentation/spritekit/sktilemapnode/centeroftile(atcolumn:row:))
- [func tileColumnIndex(fromPosition: CGPoint) -> Int](/documentation/spritekit/sktilemapnode/tilecolumnindex(fromposition:))
- [func tileDefinition(atColumn: Int, row: Int) -> SKTileDefinition?](/documentation/spritekit/sktilemapnode/tiledefinition(atcolumn:row:))
- [func tileGroup(atColumn: Int, row: Int) -> SKTileGroup?](/documentation/spritekit/sktilemapnode/tilegroup(atcolumn:row:))
- [func tileRowIndex(fromPosition: CGPoint) -> Int](/documentation/spritekit/sktilemapnode/tilerowindex(fromposition:))
- [var mapSize: CGSize](/documentation/spritekit/sktilemapnode/mapsize)

#### Tinting a Tile Map

- [var color: UIColor](/documentation/spritekit/sktilemapnode/color)
- [var colorBlendFactor: CGFloat](/documentation/spritekit/sktilemapnode/colorblendfactor)

#### Lighting a Tile Map

- [var lightingBitMask: UInt32](/documentation/spritekit/sktilemapnode/lightingbitmask)

#### Configuring How Alpha Values Blend the Sprite

- [var blendMode: SKBlendMode](/documentation/spritekit/sktilemapnode/blendmode)

#### Working with Custom Shaders

- [var shader: SKShader?](/documentation/spritekit/sktilemapnode/shader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/sktilemapnode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/sktilemapnode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/sktilemapnode/value(forattributenamed:))
- [SK3DNode](/documentation/spritekit/sk3dnode)

#### Getting Started with 3D Node

- [Displaying 3D Content in a SpriteKit Scene](/documentation/spritekit/displaying-3d-content-in-a-spritekit-scene)

#### Creating 3D Nodes

- [init(viewportSize: CGSize)](/documentation/spritekit/sk3dnode/init(viewportsize:))
- [init?(coder: NSCoder)](/documentation/spritekit/sk3dnode/init(coder:))

#### Configuring a 3D Node

- [var viewportSize: CGSize](/documentation/spritekit/sk3dnode/viewportsize)
- [var scnScene: SCNScene?](/documentation/spritekit/sk3dnode/scnscene)
- [var pointOfView: SCNNode?](/documentation/spritekit/sk3dnode/pointofview)
- [var autoenablesDefaultLighting: Bool](/documentation/spritekit/sk3dnode/autoenablesdefaultlighting)

#### Animating a 3D Node’s Content in Scene Kit

- [var isPlaying: Bool](/documentation/spritekit/sk3dnode/isplaying)
- [var loops: Bool](/documentation/spritekit/sk3dnode/loops)
- [var sceneTime: TimeInterval](/documentation/spritekit/sk3dnode/scenetime)

#### Projecting Points and Performing Hit-Testing

- [func hitTest(CGPoint, options: [String : Any]?) -> [SCNHitTestResult]](/documentation/spritekit/sk3dnode/hittest(_:options:))
- [func projectPoint(vector_float3) -> vector_float3](/documentation/spritekit/sk3dnode/projectpoint(_:))
- [func unprojectPoint(vector_float3) -> vector_float3](/documentation/spritekit/sk3dnode/unprojectpoint(_:))

### Nodes for Environmental Effects

- [SKAudioNode](/documentation/spritekit/skaudionode)

#### First Steps

- [Using Audio Nodes with the Scene’s Listener](/documentation/spritekit/using-audio-nodes-with-the-scene-s-listener)

#### Initializing Audio Nodes

- [init(avAudioNode: AVAudioNode?)](/documentation/spritekit/skaudionode/init(avaudionode:))
- [convenience init(fileNamed: String)](/documentation/spritekit/skaudionode/init(filenamed:))
- [convenience init(url: URL)](/documentation/spritekit/skaudionode/init(url:))
- [init?(coder: NSCoder)](/documentation/spritekit/skaudionode/init(coder:))

#### Configuring Audio Nodes

- [var avAudioNode: AVAudioNode?](/documentation/spritekit/skaudionode/avaudionode)
- [var isPositional: Bool](/documentation/spritekit/skaudionode/ispositional)
- [var autoplayLooped: Bool](/documentation/spritekit/skaudionode/autoplaylooped)
- [SKLightNode](/documentation/spritekit/sklightnode)

#### First Steps

- [Lighting a Sprite with Light Nodes](/documentation/spritekit/lighting-a-sprite-with-light-nodes)

#### Determining Whether a Light Node Is Active

- [var isEnabled: Bool](/documentation/spritekit/sklightnode/isenabled)
- [var categoryBitMask: UInt32](/documentation/spritekit/sklightnode/categorybitmask)

#### Configuring the Lighting Properties

- [var ambientColor: UIColor](/documentation/spritekit/sklightnode/ambientcolor)
- [var lightColor: UIColor](/documentation/spritekit/sklightnode/lightcolor)
- [var shadowColor: UIColor](/documentation/spritekit/sklightnode/shadowcolor)
- [var falloff: CGFloat](/documentation/spritekit/sklightnode/falloff)
- [SKFieldNode](/documentation/spritekit/skfieldnode)

#### Getting Started with Field Nodes

- [Adding Physics Fields to a Scene](/documentation/spritekit/adding-physics-fields-to-a-scene)

#### Creating Field Nodes

- [class func dragField() -> SKFieldNode](/documentation/spritekit/skfieldnode/dragfield())
- [class func electricField() -> SKFieldNode](/documentation/spritekit/skfieldnode/electricfield())
- [class func linearGravityField(withVector: vector_float3) -> SKFieldNode](/documentation/spritekit/skfieldnode/lineargravityfield(withvector:))
- [class func magneticField() -> SKFieldNode](/documentation/spritekit/skfieldnode/magneticfield())
- [class func noiseField(withSmoothness: CGFloat, animationSpeed: CGFloat) -> SKFieldNode](/documentation/spritekit/skfieldnode/noisefield(withsmoothness:animationspeed:))
- [class func radialGravityField() -> SKFieldNode](/documentation/spritekit/skfieldnode/radialgravityfield())
- [class func springField() -> SKFieldNode](/documentation/spritekit/skfieldnode/springfield())
- [class func turbulenceField(withSmoothness: CGFloat, animationSpeed: CGFloat) -> SKFieldNode](/documentation/spritekit/skfieldnode/turbulencefield(withsmoothness:animationspeed:))
- [class func velocityField(with: SKTexture) -> SKFieldNode](/documentation/spritekit/skfieldnode/velocityfield(with:))
- [class func velocityField(withVector: vector_float3) -> SKFieldNode](/documentation/spritekit/skfieldnode/velocityfield(withvector:))
- [class func vortexField() -> SKFieldNode](/documentation/spritekit/skfieldnode/vortexfield())
- [class func customField(evaluationBlock: SKFieldForceEvaluator) -> SKFieldNode](/documentation/spritekit/skfieldnode/customfield(evaluationblock:))
- [SKFieldForceEvaluator](/documentation/spritekit/skfieldforceevaluator)

#### Determining Which Physics Bodies Are Affected by the Field

- [var isEnabled: Bool](/documentation/spritekit/skfieldnode/isenabled)
- [var isExclusive: Bool](/documentation/spritekit/skfieldnode/isexclusive)
- [var region: SKRegion?](/documentation/spritekit/skfieldnode/region)
- [var minimumRadius: Float](/documentation/spritekit/skfieldnode/minimumradius)
- [var categoryBitMask: UInt32](/documentation/spritekit/skfieldnode/categorybitmask)

#### Configuring the Strength of the Field

- [var strength: Float](/documentation/spritekit/skfieldnode/strength)
- [var falloff: Float](/documentation/spritekit/skfieldnode/falloff)

#### Configuring Other Field Properties

- [var animationSpeed: Float](/documentation/spritekit/skfieldnode/animationspeed)
- [var smoothness: Float](/documentation/spritekit/skfieldnode/smoothness)
- [var direction: vector_float3](/documentation/spritekit/skfieldnode/direction)
- [var texture: SKTexture?](/documentation/spritekit/skfieldnode/texture)

### Nodes that Modify Drawing

- [SKEffectNode](/documentation/spritekit/skeffectnode)

#### Applying Core Image Filters with an Effect Node

- [Applying Special Effects to a Node’s Children](/documentation/spritekit/applying-special-effects-to-a-node-s-children)
- [var filter: CIFilter?](/documentation/spritekit/skeffectnode/filter)
- [var shouldEnableEffects: Bool](/documentation/spritekit/skeffectnode/shouldenableeffects)
- [var shouldCenterFilter: Bool](/documentation/spritekit/skeffectnode/shouldcenterfilter)

#### Warping Nodes with an Effect Node

- [Warping SpriteKit Content By Using an Effect Node](/documentation/spritekit/warping-spritekit-content-by-using-an-effect-node)

#### Applying a Shader with an Effect Node

- [var shader: SKShader?](/documentation/spritekit/skeffectnode/shader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/skeffectnode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/skeffectnode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/skeffectnode/value(forattributenamed:))

#### Flattening an Effect Node’s Child Tree for Performance Improvement

- [Improving the Performance of Static Content](/documentation/spritekit/improving-the-performance-of-static-content)
- [var shouldRasterize: Bool](/documentation/spritekit/skeffectnode/shouldrasterize)

#### Configuring Alpha Blending

- [var blendMode: SKBlendMode](/documentation/spritekit/skeffectnode/blendmode)
- [SKCropNode](/documentation/spritekit/skcropnode)

#### First Steps

- [Cropping Nodes](/documentation/spritekit/cropping-nodes)

#### Setting the Mask Filter

- [var maskNode: SKNode?](/documentation/spritekit/skcropnode/masknode)
- [SKTransformNode](/documentation/spritekit/sktransformnode)

#### Rotating Child Nodes

- [var xRotation: CGFloat](/documentation/spritekit/sktransformnode/xrotation)
- [var yRotation: CGFloat](/documentation/spritekit/sktransformnode/yrotation)
- [func setEulerAngles(vector_float3)](/documentation/spritekit/sktransformnode/seteulerangles(_:))
- [func setQuaternion(simd_quatf)](/documentation/spritekit/sktransformnode/setquaternion(_:))
- [func setRotationMatrix(matrix_float3x3)](/documentation/spritekit/sktransformnode/setrotationmatrix(_:))

#### Reading the Current Rotation

- [func eulerAngles() -> vector_float3](/documentation/spritekit/sktransformnode/eulerangles())
- [func quaternion() -> simd_quatf](/documentation/spritekit/sktransformnode/quaternion())
- [func rotationMatrix() -> matrix_float3x3](/documentation/spritekit/sktransformnode/rotationmatrix())

## Scene Renderers

- [Choosing a SpriteKit Scene Renderer](/documentation/spritekit/choosing-a-spritekit-scene-renderer)
- [SKView](/documentation/spritekit/skview)

### Displaying a Scene

- [var scene: SKScene?](/documentation/spritekit/skview/scene)
- [func presentScene(SKScene?)](/documentation/spritekit/skview/presentscene(_:))
- [func presentScene(SKScene, transition: SKTransition)](/documentation/spritekit/skview/presentscene(_:transition:))
- [SKTransition](/documentation/spritekit/sktransition)

#### Creating Transitions

- [Transitioning Between Two Scenes](/documentation/spritekit/transitioning-between-two-scenes)
- [Configuring Whether Animations Play During the Transition](/documentation/spritekit/configuring-whether-animations-play-during-the-transition)
- [class func crossFade(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/crossfade(withduration:))
- [class func doorsCloseHorizontal(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/doorsclosehorizontal(withduration:))
- [class func doorsCloseVertical(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/doorsclosevertical(withduration:))
- [class func doorsOpenHorizontal(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/doorsopenhorizontal(withduration:))
- [class func doorsOpenVertical(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/doorsopenvertical(withduration:))
- [class func doorway(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/doorway(withduration:))
- [class func fade(with: UIColor, duration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/fade(with:duration:))
- [class func fade(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/fade(withduration:))
- [class func flipHorizontal(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/fliphorizontal(withduration:))
- [class func flipVertical(withDuration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/flipvertical(withduration:))
- [class func moveIn(with: SKTransitionDirection, duration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/movein(with:duration:))
- [class func push(with: SKTransitionDirection, duration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/push(with:duration:))
- [class func reveal(with: SKTransitionDirection, duration: TimeInterval) -> SKTransition](/documentation/spritekit/sktransition/reveal(with:duration:))
- [init(ciFilter: CIFilter, duration: TimeInterval)](/documentation/spritekit/sktransition/init(cifilter:duration:))

#### Pausing

- [var pausesIncomingScene: Bool](/documentation/spritekit/sktransition/pausesincomingscene)
- [var pausesOutgoingScene: Bool](/documentation/spritekit/sktransition/pausesoutgoingscene)

#### Constants

- [SKTransitionDirection](/documentation/spritekit/sktransitiondirection)

##### Constants

- [case up](/documentation/spritekit/sktransitiondirection/up)
- [case down](/documentation/spritekit/sktransitiondirection/down)
- [case right](/documentation/spritekit/sktransitiondirection/right)
- [case left](/documentation/spritekit/sktransitiondirection/left)

##### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sktransitiondirection/init(rawvalue:))

### Controlling the Timing of a Scene’s Rendering

- [var isPaused: Bool](/documentation/spritekit/skview/ispaused)
- [var preferredFramesPerSecond: Int](/documentation/spritekit/skview/preferredframespersecond)
- [var delegate: (any SKViewDelegate)?](/documentation/spritekit/skview/delegate)
- [SKViewDelegate](/documentation/spritekit/skviewdelegate)

#### Instance Methods

- [func view(SKView, shouldRenderAtTime: TimeInterval) -> Bool](/documentation/spritekit/skviewdelegate/view(_:shouldrenderattime:))
- [var frameInterval: Int](/documentation/spritekit/skview/frameinterval)
- [var preferredFrameRate: Float](/documentation/spritekit/skview/preferredframerate)

### Configuring Performance Related Toggles

- [var ignoresSiblingOrder: Bool](/documentation/spritekit/skview/ignoressiblingorder)
- [var shouldCullNonVisibleNodes: Bool](/documentation/spritekit/skview/shouldcullnonvisiblenodes)
- [var allowsTransparency: Bool](/documentation/spritekit/skview/allowstransparency)
- [var isAsynchronous: Bool](/documentation/spritekit/skview/isasynchronous)

### Enabling Visual Statistics for Debugging

- [var showsFPS: Bool](/documentation/spritekit/skview/showsfps)
- [var showsNodeCount: Bool](/documentation/spritekit/skview/showsnodecount)
- [var showsDrawCount: Bool](/documentation/spritekit/skview/showsdrawcount)
- [var showsQuadCount: Bool](/documentation/spritekit/skview/showsquadcount)
- [var showsPhysics: Bool](/documentation/spritekit/skview/showsphysics)
- [var showsFields: Bool](/documentation/spritekit/skview/showsfields)

### Converting Between View and Scene Coordinates

- [func convert(CGPoint, from: SKScene) -> CGPoint](/documentation/spritekit/skview/convert(_:from:))
- [func convert(CGPoint, to: SKScene) -> CGPoint](/documentation/spritekit/skview/convert(_:to:))

### Snapshotting Nodes to a Texture

- [func texture(from: SKNode, crop: CGRect) -> SKTexture?](/documentation/spritekit/skview/texture(from:crop:))
- [func texture(from: SKNode) -> SKTexture?](/documentation/spritekit/skview/texture(from:))
- [Creating a New Node By Rendering To a Texture](/documentation/spritekit/creating-a-new-node-by-rendering-to-a-texture)

### Switching Renderers

- [Requesting the OpenGL Renderer](/documentation/spritekit/requesting-the-opengl-renderer)

### Instance Properties

- [var disableDepthStencilBuffer: Bool](/documentation/spritekit/skview/disabledepthstencilbuffer)
- [SKRenderer](/documentation/spritekit/skrenderer)

### First Steps

- [init(device: any MTLDevice)](/documentation/spritekit/skrenderer/init(device:))
- [var scene: SKScene?](/documentation/spritekit/skrenderer/scene)

### Rendering the Scene

- [func render(withViewport: CGRect, commandBuffer: any MTLCommandBuffer, renderPassDescriptor: MTLRenderPassDescriptor)](/documentation/spritekit/skrenderer/render(withviewport:commandbuffer:renderpassdescriptor:))
- [func render(withViewport: CGRect, renderCommandEncoder: any MTLRenderCommandEncoder, renderPassDescriptor: MTLRenderPassDescriptor, commandQueue: any MTLCommandQueue)](/documentation/spritekit/skrenderer/render(withviewport:rendercommandencoder:renderpassdescriptor:commandqueue:))

### Driving the Scene’s Update Cycle

- [func update(atTime: TimeInterval)](/documentation/spritekit/skrenderer/update(attime:))

### Configuring Performance Related Toggles

- [var ignoresSiblingOrder: Bool](/documentation/spritekit/skrenderer/ignoressiblingorder)
- [var shouldCullNonVisibleNodes: Bool](/documentation/spritekit/skrenderer/shouldcullnonvisiblenodes)

### Enabling Visual Statistics for Debugging

- [var showsNodeCount: Bool](/documentation/spritekit/skrenderer/showsnodecount)
- [var showsDrawCount: Bool](/documentation/spritekit/skrenderer/showsdrawcount)
- [var showsQuadCount: Bool](/documentation/spritekit/skrenderer/showsquadcount)
- [var showsPhysics: Bool](/documentation/spritekit/skrenderer/showsphysics)
- [var showsFields: Bool](/documentation/spritekit/skrenderer/showsfields)
- [WKInterfaceSKScene](/documentation/watchkit/wkinterfaceskscene)

## Textures

- [Maximizing Texture Performance](/documentation/spritekit/maximizing-texture-performance)
- [SKTexture](/documentation/spritekit/sktexture)

### First Steps

- [Loading and Using Textures](/documentation/spritekit/loading-and-using-textures)
- [Texture Initializers](/documentation/spritekit/texture-initializers)

#### Filename Initializer

- [convenience init(imageNamed: String)](/documentation/spritekit/sktexture/init(imagenamed:))

#### Texture Within a Texture

- [convenience init(rect: CGRect, in: SKTexture)](/documentation/spritekit/sktexture/init(rect:in:))

#### Texture from Image

- [convenience init(image: UIImage)](/documentation/spritekit/sktexture/init(image:))
- [convenience init(cgImage: CGImage)](/documentation/spritekit/sktexture/init(cgimage:))

#### Texture with Effects

- [func applying(CIFilter) -> Self](/documentation/spritekit/sktexture/applying(_:))

#### Texture from Data

- [convenience init(data: Data, size: CGSize)](/documentation/spritekit/sktexture/init(data:size:))
- [convenience init(data: Data, size: CGSize, rowLength: UInt32, alignment: UInt32)](/documentation/spritekit/sktexture/init(data:size:rowlength:alignment:))
- [convenience init(data: Data, size: CGSize, flipped: Bool)](/documentation/spritekit/sktexture/init(data:size:flipped:))

#### Texture from Normal Map

- [func generatingNormalMap() -> Self](/documentation/spritekit/sktexture/generatingnormalmap())
- [func generatingNormalMap(withSmoothness: CGFloat, contrast: CGFloat) -> Self](/documentation/spritekit/sktexture/generatingnormalmap(withsmoothness:contrast:))

#### Noise Textures

- [convenience init(vectorNoiseWithSmoothness: CGFloat, size: CGSize)](/documentation/spritekit/sktexture/init(vectornoisewithsmoothness:size:))
- [convenience init(noiseWithSmoothness: CGFloat, size: CGSize, grayscale: Bool)](/documentation/spritekit/sktexture/init(noisewithsmoothness:size:grayscale:))

#### Texture from Noise Map

- [convenience init(noiseMap: GKNoiseMap)](/documentation/spritekit/sktexture/init(noisemap:))

### Reading a Texture’s Size and Optional Source Location

- [func size() -> CGSize](/documentation/spritekit/sktexture/size())
- [func textureRect() -> CGRect](/documentation/spritekit/sktexture/texturerect())

### Configuring a Texture’s Behavior for Scaling

- [var filteringMode: SKTextureFilteringMode](/documentation/spritekit/sktexture/filteringmode)
- [SKTextureFilteringMode](/documentation/spritekit/sktexturefilteringmode)

#### Constants

- [case nearest](/documentation/spritekit/sktexturefilteringmode/nearest)
- [case linear](/documentation/spritekit/sktexturefilteringmode/linear)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sktexturefilteringmode/init(rawvalue:))
- [var usesMipmaps: Bool](/documentation/spritekit/sktexture/usesmipmaps)

### Getting a Texture’s Underlying Image

- [func cgImage() -> CGImage](/documentation/spritekit/sktexture/cgimage())

### Preloading a Texture for Performance

- [Preloading Textures into Memory](/documentation/spritekit/preloading-textures-into-memory)
- [func preload(completionHandler: () -> Void)](/documentation/spritekit/sktexture/preload(completionhandler:))
- [class func preload([SKTexture], withCompletionHandler: () -> Void)](/documentation/spritekit/sktexture/preload(_:withcompletionhandler:))

### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/spritekit/sktexture/customplaygroundquicklook)
- [SKTextureAtlas](/documentation/spritekit/sktextureatlas)

### First Steps

- [About Texture Atlases](/documentation/spritekit/about-texture-atlases)

### Accessing Textures

- [func textureNamed(String) -> SKTexture](/documentation/spritekit/sktextureatlas/texturenamed(_:))

### Creating a Texture Atlas Programmatically

- [convenience init(named: String)](/documentation/spritekit/sktextureatlas/init(named:))
- [convenience init(dictionary: [String : Any])](/documentation/spritekit/sktextureatlas/init(dictionary:))

### Preloading Textures

- [func preload(completionHandler: () -> Void)](/documentation/spritekit/sktextureatlas/preload(completionhandler:))
- [class func preloadTextureAtlases([SKTextureAtlas], withCompletionHandler: () -> Void)](/documentation/spritekit/sktextureatlas/preloadtextureatlases(_:withcompletionhandler:))
- [class func preloadTextureAtlasesNamed([String], withCompletionHandler: ((any Error)?, [SKTextureAtlas]) -> Void)](/documentation/spritekit/sktextureatlas/preloadtextureatlasesnamed(_:withcompletionhandler:))

### Reading Source Image Filenames

- [var textureNames: [String]](/documentation/spritekit/sktextureatlas/texturenames)

### Instance Properties

- [var customPlaygroundQuickLook: PlaygroundQuickLook](/documentation/spritekit/sktextureatlas/customplaygroundquicklook)
- [SKMutableTexture](/documentation/spritekit/skmutabletexture)

### Creating an Empty Mutable Texture

- [init(size: CGSize, pixelFormat: Int32)](/documentation/spritekit/skmutabletexture/init(size:pixelformat:))
- [init(size: CGSize)](/documentation/spritekit/skmutabletexture/init(size:))

### Modifying a Mutable Texture’s Contents

- [func modifyPixelData((UnsafeMutableRawPointer?, Int) -> Void)](/documentation/spritekit/skmutabletexture/modifypixeldata(_:))

## Animation

- [Getting Started with Actions](/documentation/spritekit/getting-started-with-actions)
- [SKAction](/documentation/spritekit/skaction)

### First Steps

- [Getting Started with Actions](/documentation/spritekit/getting-started-with-actions)
- [Action Initializers](/documentation/spritekit/action-initializers)

#### Animating a Node’s Position in a Linear Path

- [class func moveBy(x: CGFloat, y: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/moveby(x:y:duration:))
- [class func move(by: CGVector, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/move(by:duration:))
- [class func move(to: CGPoint, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/move(to:duration:))
- [class func moveTo(x: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/moveto(x:duration:))
- [class func moveTo(y: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/moveto(y:duration:))

#### Animating a Node’s Position Along a Custom Path

- [class func follow(CGPath, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/follow(_:duration:))
- [class func follow(CGPath, speed: CGFloat) -> SKAction](/documentation/spritekit/skaction/follow(_:speed:))
- [class func follow(CGPath, asOffset: Bool, orientToPath: Bool, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/follow(_:asoffset:orienttopath:duration:))
- [class func follow(CGPath, asOffset: Bool, orientToPath: Bool, speed: CGFloat) -> SKAction](/documentation/spritekit/skaction/follow(_:asoffset:orienttopath:speed:))

#### Animating the Rotation of a Node

- [class func rotate(byAngle: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/rotate(byangle:duration:))
- [class func rotate(toAngle: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/rotate(toangle:duration:))
- [class func rotate(toAngle: CGFloat, duration: TimeInterval, shortestUnitArc: Bool) -> SKAction](/documentation/spritekit/skaction/rotate(toangle:duration:shortestunitarc:))

#### Controlling the Action’s Speed

- [class func speed(by: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/speed(by:duration:))
- [class func speed(to: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/speed(to:duration:))

#### Animating the Scaling of a Node

- [class func scale(by: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scale(by:duration:))
- [class func scale(to: CGSize, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scale(to:duration:)-43bz6)
- [class func scale(to: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scale(to:duration:)-1xyzs)
- [class func scaleX(by: CGFloat, y: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scalex(by:y:duration:))
- [class func scaleX(to: CGFloat, y: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scalex(to:y:duration:))
- [class func scaleX(to: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scalex(to:duration:))
- [class func scaleY(to: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/scaley(to:duration:))

#### Animating the Transparency of a Node

- [class func fadeIn(withDuration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/fadein(withduration:))
- [class func fadeOut(withDuration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/fadeout(withduration:))
- [class func fadeAlpha(by: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/fadealpha(by:duration:))
- [class func fadeAlpha(to: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/fadealpha(to:duration:))

#### Animating a Node’s Texture

- [class func resize(byWidth: CGFloat, height: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/resize(bywidth:height:duration:))
- [class func resize(toHeight: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/resize(toheight:duration:))
- [class func resize(toWidth: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/resize(towidth:duration:))
- [class func resize(toWidth: CGFloat, height: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/resize(towidth:height:duration:))
- [class func setTexture(SKTexture) -> SKAction](/documentation/spritekit/skaction/settexture(_:))
- [class func setTexture(SKTexture, resize: Bool) -> SKAction](/documentation/spritekit/skaction/settexture(_:resize:))
- [class func animate(with: [SKTexture], timePerFrame: TimeInterval) -> SKAction](/documentation/spritekit/skaction/animate(with:timeperframe:))
- [class func animate(with: [SKTexture], timePerFrame: TimeInterval, resize: Bool, restore: Bool) -> SKAction](/documentation/spritekit/skaction/animate(with:timeperframe:resize:restore:))
- [class func setNormalTexture(SKTexture) -> SKAction](/documentation/spritekit/skaction/setnormaltexture(_:))
- [class func setNormalTexture(SKTexture, resize: Bool) -> SKAction](/documentation/spritekit/skaction/setnormaltexture(_:resize:))
- [class func animate(withNormalTextures: [SKTexture], timePerFrame: TimeInterval) -> SKAction](/documentation/spritekit/skaction/animate(withnormaltextures:timeperframe:))
- [class func animate(withNormalTextures: [SKTexture], timePerFrame: TimeInterval, resize: Bool, restore: Bool) -> SKAction](/documentation/spritekit/skaction/animate(withnormaltextures:timeperframe:resize:restore:))
- [class func colorize(with: UIColor, colorBlendFactor: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/colorize(with:colorblendfactor:duration:))
- [class func colorize(withColorBlendFactor: CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/colorize(withcolorblendfactor:duration:))

#### Animating Properties of a Node’s Physics Body

- [class func applyForce(CGVector, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyforce(_:duration:))
- [class func applyTorque(CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applytorque(_:duration:))
- [class func applyForce(CGVector, at: CGPoint, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyforce(_:at:duration:))
- [class func applyImpulse(CGVector, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyimpulse(_:duration:))
- [class func applyAngularImpulse(CGFloat, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyangularimpulse(_:duration:))
- [class func applyImpulse(CGVector, at: CGPoint, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyimpulse(_:at:duration:))
- [class func applyImpulse(CGVector, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/applyimpulse(_:duration:))
- [class func changeCharge(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changecharge(to:duration:))
- [class func changeCharge(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changecharge(by:duration:))
- [class func changeMass(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changemass(to:duration:))
- [class func changeMass(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changemass(by:duration:))
- [class func strength(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/strength(to:duration:))
- [class func strength(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/strength(by:duration:))
- [class func falloff(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/falloff(to:duration:))
- [class func falloff(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/falloff(by:duration:))

#### Reversing an Animation

- [func reversed() -> SKAction](/documentation/spritekit/skaction/reversed())

#### Animate the Warping of a Node

- [class func animate(withWarps: [SKWarpGeometry], times: [NSNumber]) -> SKAction?](/documentation/spritekit/skaction/animate(withwarps:times:))
- [class func animate(withWarps: [SKWarpGeometry], times: [NSNumber], restore: Bool) -> SKAction?](/documentation/spritekit/skaction/animate(withwarps:times:restore:))
- [class func warp(to: SKWarpGeometry, duration: TimeInterval) -> SKAction?](/documentation/spritekit/skaction/warp(to:duration:))

#### Controlling the Audio of a Node

- [class func playSoundFileNamed(String, waitForCompletion: Bool) -> SKAction](/documentation/spritekit/skaction/playsoundfilenamed(_:waitforcompletion:))
- [class func play() -> SKAction](/documentation/spritekit/skaction/play())
- [class func pause() -> SKAction](/documentation/spritekit/skaction/pause())
- [class func stop() -> SKAction](/documentation/spritekit/skaction/stop())
- [class func changePlaybackRate(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeplaybackrate(to:duration:))
- [class func changePlaybackRate(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeplaybackrate(by:duration:))
- [class func changeVolume(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changevolume(to:duration:))
- [class func changeVolume(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changevolume(by:duration:))
- [class func changeObstruction(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeobstruction(to:duration:))
- [class func changeObstruction(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeobstruction(by:duration:))
- [class func changeOcclusion(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeocclusion(to:duration:))
- [class func changeOcclusion(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changeocclusion(by:duration:))
- [class func changeReverb(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changereverb(to:duration:))
- [class func changeReverb(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/changereverb(by:duration:))
- [class func stereoPan(to: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/stereopan(to:duration:))
- [class func stereoPan(by: Float, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/stereopan(by:duration:))

#### Removing a Node from the Scene

- [class func removeFromParent() -> SKAction](/documentation/spritekit/skaction/removefromparent())

#### Running Actions on Children

- [class func run(SKAction, onChildWithName: String) -> SKAction](/documentation/spritekit/skaction/run(_:onchildwithname:))

#### Chaining Actions

- [class func group([SKAction]) -> SKAction](/documentation/spritekit/skaction/group(_:))
- [class func sequence([SKAction]) -> SKAction](/documentation/spritekit/skaction/sequence(_:))
- [class func `repeat`(SKAction, count: Int) -> SKAction](/documentation/spritekit/skaction/repeat(_:count:))
- [class func repeatForever(SKAction) -> SKAction](/documentation/spritekit/skaction/repeatforever(_:))

#### Delaying Actions

- [class func wait(forDuration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/wait(forduration:))
- [class func wait(forDuration: TimeInterval, withRange: TimeInterval) -> SKAction](/documentation/spritekit/skaction/wait(forduration:withrange:))

#### Performing Inverse Kinematics

- [Working with Inverse Kinematics](/documentation/spritekit/working-with-inverse-kinematics)
- [class func reach(to: CGPoint, rootNode: SKNode, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/reach(to:rootnode:duration:)-9gdvl)
- [class func reach(to: CGPoint, rootNode: SKNode, velocity: CGFloat) -> SKAction](/documentation/spritekit/skaction/reach(to:rootnode:velocity:)-8xv45)
- [class func reach(to: SKNode, rootNode: SKNode, duration: TimeInterval) -> SKAction](/documentation/spritekit/skaction/reach(to:rootnode:duration:)-1db76)
- [class func reach(to: SKNode, rootNode: SKNode, velocity: CGFloat) -> SKAction](/documentation/spritekit/skaction/reach(to:rootnode:velocity:)-7gbvx)

#### Creating Custom Actions

- [init?(named: String)](/documentation/spritekit/skaction/init(named:))
- [init?(named: String, duration: TimeInterval)](/documentation/spritekit/skaction/init(named:duration:))
- [init?(named: String, fromURL: URL)](/documentation/spritekit/skaction/init(named:fromurl:))
- [init?(named: String, fromURL: URL, duration: TimeInterval)](/documentation/spritekit/skaction/init(named:fromurl:duration:))
- [class func customAction(withDuration: TimeInterval, actionBlock: (SKNode, CGFloat) -> Void) -> SKAction](/documentation/spritekit/skaction/customaction(withduration:actionblock:))
- [class func perform(Selector, onTarget: Any) -> SKAction](/documentation/spritekit/skaction/perform(_:ontarget:))
- [class func run(() -> Void) -> SKAction](/documentation/spritekit/skaction/run(_:))
- [class func run(() -> Void, queue: dispatch_queue_t) -> SKAction](/documentation/spritekit/skaction/run(_:queue:))

#### Controlling Node Visibility

- [class func unhide() -> SKAction](/documentation/spritekit/skaction/unhide())
- [class func hide() -> SKAction](/documentation/spritekit/skaction/hide())

### Controlling Action Timing

- [Configuring Action Timing](/documentation/spritekit/configuring-action-timing)
- [var duration: TimeInterval](/documentation/spritekit/skaction/duration)
- [var timingMode: SKActionTimingMode](/documentation/spritekit/skaction/timingmode)
- [SKActionTimingMode](/documentation/spritekit/skactiontimingmode)

#### Constants

- [case linear](/documentation/spritekit/skactiontimingmode/linear)
- [case easeIn](/documentation/spritekit/skactiontimingmode/easein)
- [case easeOut](/documentation/spritekit/skactiontimingmode/easeout)
- [case easeInEaseOut](/documentation/spritekit/skactiontimingmode/easeineaseout)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skactiontimingmode/init(rawvalue:))
- [var timingFunction: SKActionTimingFunction](/documentation/spritekit/skaction/timingfunction)
- [SKActionTimingFunction](/documentation/spritekit/skactiontimingfunction)
- [var speed: CGFloat](/documentation/spritekit/skaction/speed)

### Using Action Names

- [Controlling Actions Precisely by Using Names](/documentation/spritekit/controlling-actions-precisely-by-using-names)

### Observing Live Changes

- [Detecting Changes at Each Step of an Animation](/documentation/spritekit/detecting-changes-at-each-step-of-an-animation)

## Constraints

- [SKConstraint](/documentation/spritekit/skconstraint)

### Creating Position Constraints

- [Creating Position Constraints](/documentation/spritekit/creating-position-constraints)
- [class func positionX(SKRange, y: SKRange) -> Self](/documentation/spritekit/skconstraint/positionx(_:y:))
- [class func positionX(SKRange) -> Self](/documentation/spritekit/skconstraint/positionx(_:))
- [class func positionY(SKRange) -> Self](/documentation/spritekit/skconstraint/positiony(_:))

### Creating Orientation Constraints

- [Creating a Look-At Constraint](/documentation/spritekit/creating-a-look-at-constraint)
- [class func orient(to: SKNode, offset: SKRange) -> Self](/documentation/spritekit/skconstraint/orient(to:offset:)-1h1tw)
- [class func orient(to: CGPoint, offset: SKRange) -> Self](/documentation/spritekit/skconstraint/orient(to:offset:)-9lq3h)
- [class func orient(to: CGPoint, in: SKNode, offset: SKRange) -> Self](/documentation/spritekit/skconstraint/orient(to:in:offset:))
- [class func zRotation(SKRange) -> Self](/documentation/spritekit/skconstraint/zrotation(_:))

### Creating Distance Constraints

- [class func distance(SKRange, to: SKNode) -> Self](/documentation/spritekit/skconstraint/distance(_:to:)-6507j)
- [class func distance(SKRange, to: CGPoint) -> Self](/documentation/spritekit/skconstraint/distance(_:to:)-7yk7n)
- [class func distance(SKRange, to: CGPoint, in: SKNode) -> Self](/documentation/spritekit/skconstraint/distance(_:to:in:))

### Controlling the Coordinate System Where a Constraint is Applied

- [var referenceNode: SKNode?](/documentation/spritekit/skconstraint/referencenode)

### Enabling and Disabling a Constraint

- [var enabled: Bool](/documentation/spritekit/skconstraint/enabled)
- [SKReachConstraints](/documentation/spritekit/skreachconstraints)

### Working with Reach Constraints

- [init(lowerAngleLimit: CGFloat, upperAngleLimit: CGFloat)](/documentation/spritekit/skreachconstraints/init(loweranglelimit:upperanglelimit:))
- [var lowerAngleLimit: CGFloat](/documentation/spritekit/skreachconstraints/loweranglelimit)
- [var upperAngleLimit: CGFloat](/documentation/spritekit/skreachconstraints/upperanglelimit)

## Mathematical Tools

- [SKKeyframeSequence](/documentation/spritekit/skkeyframesequence)

### First Steps

- [Using Keyframe Sequence to effect Custom Interpolation](/documentation/spritekit/using-keyframe-sequence-to-effect-custom-interpolation)
- [init(keyframeValues: [Any], times: [NSNumber])](/documentation/spritekit/skkeyframesequence/init(keyframevalues:times:))
- [convenience init(capacity: Int)](/documentation/spritekit/skkeyframesequence/init(capacity:))
- [init?(coder: NSCoder)](/documentation/spritekit/skkeyframesequence/init(coder:))

### Sequence Building

- [func addKeyframeValue(Any, time: CGFloat)](/documentation/spritekit/skkeyframesequence/addkeyframevalue(_:time:))
- [func removeKeyframe(at: Int)](/documentation/spritekit/skkeyframesequence/removekeyframe(at:))
- [func removeLastKeyframe()](/documentation/spritekit/skkeyframesequence/removelastkeyframe())
- [func setKeyframeTime(CGFloat, for: Int)](/documentation/spritekit/skkeyframesequence/setkeyframetime(_:for:))
- [func setKeyframeValue(Any, for: Int)](/documentation/spritekit/skkeyframesequence/setkeyframevalue(_:for:))
- [func setKeyframeValue(Any, time: CGFloat, for: Int)](/documentation/spritekit/skkeyframesequence/setkeyframevalue(_:time:for:))

### Sequence Running

- [func sample(atTime: CGFloat) -> Any?](/documentation/spritekit/skkeyframesequence/sample(attime:))

### Sequence Information

- [func count() -> Int](/documentation/spritekit/skkeyframesequence/count())
- [func getKeyframeTime(for: Int) -> CGFloat](/documentation/spritekit/skkeyframesequence/getkeyframetime(for:))
- [func getKeyframeValue(for: Int) -> Any](/documentation/spritekit/skkeyframesequence/getkeyframevalue(for:))

### Interpolation Modifiers

- [var interpolationMode: SKInterpolationMode](/documentation/spritekit/skkeyframesequence/interpolationmode)
- [var repeatMode: SKRepeatMode](/documentation/spritekit/skkeyframesequence/repeatmode)

### Constants

- [SKInterpolationMode](/documentation/spritekit/skinterpolationmode)

#### Constants

- [case linear](/documentation/spritekit/skinterpolationmode/linear)
- [case spline](/documentation/spritekit/skinterpolationmode/spline)
- [case step](/documentation/spritekit/skinterpolationmode/step)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skinterpolationmode/init(rawvalue:))
- [SKRepeatMode](/documentation/spritekit/skrepeatmode)

#### Constants

- [case clamp](/documentation/spritekit/skrepeatmode/clamp)
- [case loop](/documentation/spritekit/skrepeatmode/loop)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skrepeatmode/init(rawvalue:))
- [SKRange](/documentation/spritekit/skrange)

### Creating a Range Object

- [convenience init(value: CGFloat, variance: CGFloat)](/documentation/spritekit/skrange/init(value:variance:))
- [class func withNoLimits() -> Self](/documentation/spritekit/skrange/withnolimits())
- [convenience init(lowerLimit: CGFloat)](/documentation/spritekit/skrange/init(lowerlimit:))
- [convenience init(upperLimit: CGFloat)](/documentation/spritekit/skrange/init(upperlimit:))
- [convenience init(constantValue: CGFloat)](/documentation/spritekit/skrange/init(constantvalue:))
- [init(lowerLimit: CGFloat, upperLimit: CGFloat)](/documentation/spritekit/skrange/init(lowerlimit:upperlimit:))

### Inspecting a Range Object’s Limits

- [var lowerLimit: CGFloat](/documentation/spritekit/skrange/lowerlimit)
- [var upperLimit: CGFloat](/documentation/spritekit/skrange/upperlimit)
- [SKRegion](/documentation/spritekit/skregion)

### Creating and Initializing Region Objects

- [class func infinite() -> Self](/documentation/spritekit/skregion/infinite())
- [init(size: CGSize)](/documentation/spritekit/skregion/init(size:))
- [init(radius: Float)](/documentation/spritekit/skregion/init(radius:))
- [init(path: CGPath)](/documentation/spritekit/skregion/init(path:))
- [func inverse() -> Self](/documentation/spritekit/skregion/inverse())
- [func byDifference(from: SKRegion) -> Self](/documentation/spritekit/skregion/bydifference(from:))
- [func byIntersection(with: SKRegion) -> Self](/documentation/spritekit/skregion/byintersection(with:))
- [func byUnion(with: SKRegion) -> Self](/documentation/spritekit/skregion/byunion(with:))

### Interacting with a Region

- [var path: CGPath?](/documentation/spritekit/skregion/path)
- [func contains(CGPoint) -> Bool](/documentation/spritekit/skregion/contains(_:))

## Physics Simulation

- [Getting Started with Physics](/documentation/spritekit/getting-started-with-physics)
- [SKPhysicsWorld](/documentation/spritekit/skphysicsworld)

### Configuring the Physics World

- [var gravity: CGVector](/documentation/spritekit/skphysicsworld/gravity)
- [var speed: CGFloat](/documentation/spritekit/skphysicsworld/speed)

### Joining Physics Bodies with Joints

- [func add(SKPhysicsJoint)](/documentation/spritekit/skphysicsworld/add(_:))
- [func removeAllJoints()](/documentation/spritekit/skphysicsworld/removealljoints())
- [func remove(SKPhysicsJoint)](/documentation/spritekit/skphysicsworld/remove(_:))

### Detecting Collisions

- [var contactDelegate: (any SKPhysicsContactDelegate)?](/documentation/spritekit/skphysicsworld/contactdelegate)

### Searching the Scene for Physics Bodies

- [Searching the World for Physics Bodies](/documentation/spritekit/searching-the-world-for-physics-bodies)
- [func body(alongRayStart: CGPoint, end: CGPoint) -> SKPhysicsBody?](/documentation/spritekit/skphysicsworld/body(alongraystart:end:))
- [func body(at: CGPoint) -> SKPhysicsBody?](/documentation/spritekit/skphysicsworld/body(at:))
- [func body(in: CGRect) -> SKPhysicsBody?](/documentation/spritekit/skphysicsworld/body(in:))
- [func enumerateBodies(alongRayStart: CGPoint, end: CGPoint, using: (SKPhysicsBody, CGPoint, CGVector, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/spritekit/skphysicsworld/enumeratebodies(alongraystart:end:using:))
- [func enumerateBodies(at: CGPoint, using: (SKPhysicsBody, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/spritekit/skphysicsworld/enumeratebodies(at:using:))
- [func enumerateBodies(in: CGRect, using: (SKPhysicsBody, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/spritekit/skphysicsworld/enumeratebodies(in:using:))

### Sampling Physics Fields

- [func sampleFields(at: vector_float3) -> vector_float3](/documentation/spritekit/skphysicsworld/samplefields(at:))
- [SKPhysicsBody](/documentation/spritekit/skphysicsbody)

### First Steps

- [Getting Started with Physics Bodies](/documentation/spritekit/getting-started-with-physics-bodies)

### Creating a Body from a Shape

- [init(circleOfRadius: CGFloat)](/documentation/spritekit/skphysicsbody/init(circleofradius:))
- [init(circleOfRadius: CGFloat, center: CGPoint)](/documentation/spritekit/skphysicsbody/init(circleofradius:center:))
- [init(rectangleOf: CGSize)](/documentation/spritekit/skphysicsbody/init(rectangleof:))
- [init(rectangleOf: CGSize, center: CGPoint)](/documentation/spritekit/skphysicsbody/init(rectangleof:center:))
- [init(polygonFrom: CGPath)](/documentation/spritekit/skphysicsbody/init(polygonfrom:))

### Creating a Body from a Texture

- [Shaping a Physics Body to Match a Node’s Graphics](/documentation/spritekit/shaping-a-physics-body-to-match-a-node-s-graphics)
- [init(texture: SKTexture, size: CGSize)](/documentation/spritekit/skphysicsbody/init(texture:size:))
- [init(texture: SKTexture, alphaThreshold: Float, size: CGSize)](/documentation/spritekit/skphysicsbody/init(texture:alphathreshold:size:))

### Creating a Body from a Collection of Bodies

- [init(bodies: [SKPhysicsBody])](/documentation/spritekit/skphysicsbody/init(bodies:))

### Creating an Edge-Based Physics Body

- [Creating an Edge Loop Around a Scene](/documentation/spritekit/creating-an-edge-loop-around-a-scene)
- [init(edgeLoopFrom: CGRect)](/documentation/spritekit/skphysicsbody/init(edgeloopfrom:)-8sqfy)
- [init(edgeFrom: CGPoint, to: CGPoint)](/documentation/spritekit/skphysicsbody/init(edgefrom:to:))
- [init(edgeLoopFrom: CGPath)](/documentation/spritekit/skphysicsbody/init(edgeloopfrom:)-5grxu)
- [init(edgeChainFrom: CGPath)](/documentation/spritekit/skphysicsbody/init(edgechainfrom:))

### Defining How Forces Affect a Physics Body

- [var affectedByGravity: Bool](/documentation/spritekit/skphysicsbody/affectedbygravity)
- [var allowsRotation: Bool](/documentation/spritekit/skphysicsbody/allowsrotation)
- [var isDynamic: Bool](/documentation/spritekit/skphysicsbody/isdynamic)

### Defining a Physics Body’s Physical Properties

- [Configuring a Physics Body](/documentation/spritekit/configuring-a-physics-body)
- [var mass: CGFloat](/documentation/spritekit/skphysicsbody/mass)
- [var density: CGFloat](/documentation/spritekit/skphysicsbody/density)
- [var area: CGFloat](/documentation/spritekit/skphysicsbody/area)
- [var friction: CGFloat](/documentation/spritekit/skphysicsbody/friction)
- [var restitution: CGFloat](/documentation/spritekit/skphysicsbody/restitution)
- [var linearDamping: CGFloat](/documentation/spritekit/skphysicsbody/lineardamping)
- [var angularDamping: CGFloat](/documentation/spritekit/skphysicsbody/angulardamping)

### Working with Collisions and Contacts

- [About Collisions and Contacts](/documentation/spritekit/about-collisions-and-contacts)
- [var categoryBitMask: UInt32](/documentation/spritekit/skphysicsbody/categorybitmask)
- [var collisionBitMask: UInt32](/documentation/spritekit/skphysicsbody/collisionbitmask)
- [var usesPreciseCollisionDetection: Bool](/documentation/spritekit/skphysicsbody/usesprecisecollisiondetection)
- [var contactTestBitMask: UInt32](/documentation/spritekit/skphysicsbody/contacttestbitmask)
- [func allContactedBodies() -> [SKPhysicsBody]](/documentation/spritekit/skphysicsbody/allcontactedbodies())

### Applying Forces and Impulses to a Physics Body

- [Making Physics Bodies Move](/documentation/spritekit/making-physics-bodies-move)
- [func applyForce(CGVector)](/documentation/spritekit/skphysicsbody/applyforce(_:))
- [func applyTorque(CGFloat)](/documentation/spritekit/skphysicsbody/applytorque(_:))
- [func applyForce(CGVector, at: CGPoint)](/documentation/spritekit/skphysicsbody/applyforce(_:at:))
- [func applyImpulse(CGVector)](/documentation/spritekit/skphysicsbody/applyimpulse(_:))
- [func applyAngularImpulse(CGFloat)](/documentation/spritekit/skphysicsbody/applyangularimpulse(_:))
- [func applyImpulse(CGVector, at: CGPoint)](/documentation/spritekit/skphysicsbody/applyimpulse(_:at:))

### Inspecting a Physics Body’s Position and Velocity

- [var velocity: CGVector](/documentation/spritekit/skphysicsbody/velocity)
- [var angularVelocity: CGFloat](/documentation/spritekit/skphysicsbody/angularvelocity)
- [var isResting: Bool](/documentation/spritekit/skphysicsbody/isresting)

### Reading a Physics Body’s Node

- [var node: SKNode?](/documentation/spritekit/skphysicsbody/node)

### Determining Which Joints Are Connected to a Physics Body

- [var joints: [SKPhysicsJoint]](/documentation/spritekit/skphysicsbody/joints)

### Interacting with Physics Fields

- [var fieldBitMask: UInt32](/documentation/spritekit/skphysicsbody/fieldbitmask)
- [var charge: CGFloat](/documentation/spritekit/skphysicsbody/charge)

### Pinning a Physics Body to a Node’s Parent

- [Pinning and Rotating Physics Bodies](/documentation/spritekit/pinning-and-rotating-physics-bodies)
- [var pinned: Bool](/documentation/spritekit/skphysicsbody/pinned)
- [SKPhysicsContact](/documentation/spritekit/skphysicscontact)

### Inspecting the Contact Properties

- [var bodyA: SKPhysicsBody](/documentation/spritekit/skphysicscontact/bodya)
- [var bodyB: SKPhysicsBody](/documentation/spritekit/skphysicscontact/bodyb)
- [var contactPoint: CGPoint](/documentation/spritekit/skphysicscontact/contactpoint)
- [var collisionImpulse: CGFloat](/documentation/spritekit/skphysicscontact/collisionimpulse)
- [var contactNormal: CGVector](/documentation/spritekit/skphysicscontact/contactnormal)
- [SKPhysicsContactDelegate](/documentation/spritekit/skphysicscontactdelegate)

### Responding to Contact Events

- [func didBegin(SKPhysicsContact)](/documentation/spritekit/skphysicscontactdelegate/didbegin(_:))
- [func didEnd(SKPhysicsContact)](/documentation/spritekit/skphysicscontactdelegate/didend(_:))
- [SKFieldNode](/documentation/spritekit/skfieldnode)

### Getting Started with Field Nodes

- [Adding Physics Fields to a Scene](/documentation/spritekit/adding-physics-fields-to-a-scene)

### Creating Field Nodes

- [class func dragField() -> SKFieldNode](/documentation/spritekit/skfieldnode/dragfield())
- [class func electricField() -> SKFieldNode](/documentation/spritekit/skfieldnode/electricfield())
- [class func linearGravityField(withVector: vector_float3) -> SKFieldNode](/documentation/spritekit/skfieldnode/lineargravityfield(withvector:))
- [class func magneticField() -> SKFieldNode](/documentation/spritekit/skfieldnode/magneticfield())
- [class func noiseField(withSmoothness: CGFloat, animationSpeed: CGFloat) -> SKFieldNode](/documentation/spritekit/skfieldnode/noisefield(withsmoothness:animationspeed:))
- [class func radialGravityField() -> SKFieldNode](/documentation/spritekit/skfieldnode/radialgravityfield())
- [class func springField() -> SKFieldNode](/documentation/spritekit/skfieldnode/springfield())
- [class func turbulenceField(withSmoothness: CGFloat, animationSpeed: CGFloat) -> SKFieldNode](/documentation/spritekit/skfieldnode/turbulencefield(withsmoothness:animationspeed:))
- [class func velocityField(with: SKTexture) -> SKFieldNode](/documentation/spritekit/skfieldnode/velocityfield(with:))
- [class func velocityField(withVector: vector_float3) -> SKFieldNode](/documentation/spritekit/skfieldnode/velocityfield(withvector:))
- [class func vortexField() -> SKFieldNode](/documentation/spritekit/skfieldnode/vortexfield())
- [class func customField(evaluationBlock: SKFieldForceEvaluator) -> SKFieldNode](/documentation/spritekit/skfieldnode/customfield(evaluationblock:))
- [SKFieldForceEvaluator](/documentation/spritekit/skfieldforceevaluator)

### Determining Which Physics Bodies Are Affected by the Field

- [var isEnabled: Bool](/documentation/spritekit/skfieldnode/isenabled)
- [var isExclusive: Bool](/documentation/spritekit/skfieldnode/isexclusive)
- [var region: SKRegion?](/documentation/spritekit/skfieldnode/region)
- [var minimumRadius: Float](/documentation/spritekit/skfieldnode/minimumradius)
- [var categoryBitMask: UInt32](/documentation/spritekit/skfieldnode/categorybitmask)

### Configuring the Strength of the Field

- [var strength: Float](/documentation/spritekit/skfieldnode/strength)
- [var falloff: Float](/documentation/spritekit/skfieldnode/falloff)

### Configuring Other Field Properties

- [var animationSpeed: Float](/documentation/spritekit/skfieldnode/animationspeed)
- [var smoothness: Float](/documentation/spritekit/skfieldnode/smoothness)
- [var direction: vector_float3](/documentation/spritekit/skfieldnode/direction)
- [var texture: SKTexture?](/documentation/spritekit/skfieldnode/texture)

## Physics Joints

- [Working with Inverse Kinematics](/documentation/spritekit/working-with-inverse-kinematics)
- [SKPhysicsJoint](/documentation/spritekit/skphysicsjoint)

### Connecting Bodies with Joints

- [Connecting Bodies with Joints](/documentation/spritekit/connecting-bodies-with-joints)

### Disconnecting Bodies from Joints

- [Disconnecting Bodies from Joints](/documentation/spritekit/disconnecting-bodies-from-joints)

### Accessing or Setting a Joint’s Bodies

- [var bodyA: SKPhysicsBody](/documentation/spritekit/skphysicsjoint/bodya)
- [var bodyB: SKPhysicsBody](/documentation/spritekit/skphysicsjoint/bodyb)

### Reading the Stress and Speed that Are Currently Applied to a Joint

- [var reactionForce: CGVector](/documentation/spritekit/skphysicsjoint/reactionforce)
- [var reactionTorque: CGFloat](/documentation/spritekit/skphysicsjoint/reactiontorque)
- [SKPhysicsJointFixed](/documentation/spritekit/skphysicsjointfixed)

### Creating a Fixed Joint

- [class func joint(withBodyA: SKPhysicsBody, bodyB: SKPhysicsBody, anchor: CGPoint) -> SKPhysicsJointFixed](/documentation/spritekit/skphysicsjointfixed/joint(withbodya:bodyb:anchor:))
- [SKPhysicsJointLimit](/documentation/spritekit/skphysicsjointlimit)

### Creating a Limit Joint

- [class func joint(withBodyA: SKPhysicsBody, bodyB: SKPhysicsBody, anchorA: CGPoint, anchorB: CGPoint) -> SKPhysicsJointLimit](/documentation/spritekit/skphysicsjointlimit/joint(withbodya:bodyb:anchora:anchorb:))

### Configuring a Limit Joint

- [var maxLength: CGFloat](/documentation/spritekit/skphysicsjointlimit/maxlength)
- [SKPhysicsJointPin](/documentation/spritekit/skphysicsjointpin)

### Creating a Pin Joint

- [class func joint(withBodyA: SKPhysicsBody, bodyB: SKPhysicsBody, anchor: CGPoint) -> SKPhysicsJointPin](/documentation/spritekit/skphysicsjointpin/joint(withbodya:bodyb:anchor:))

### Configuring a Pin Joint

- [var rotationSpeed: CGFloat](/documentation/spritekit/skphysicsjointpin/rotationspeed)
- [var shouldEnableLimits: Bool](/documentation/spritekit/skphysicsjointpin/shouldenablelimits)
- [var lowerAngleLimit: CGFloat](/documentation/spritekit/skphysicsjointpin/loweranglelimit)
- [var upperAngleLimit: CGFloat](/documentation/spritekit/skphysicsjointpin/upperanglelimit)
- [var frictionTorque: CGFloat](/documentation/spritekit/skphysicsjointpin/frictiontorque)
- [SKPhysicsJointSliding](/documentation/spritekit/skphysicsjointsliding)

### Creating a Sliding Joint

- [class func joint(withBodyA: SKPhysicsBody, bodyB: SKPhysicsBody, anchor: CGPoint, axis: CGVector) -> SKPhysicsJointSliding](/documentation/spritekit/skphysicsjointsliding/joint(withbodya:bodyb:anchor:axis:))

### Configuring a Sliding Joint

- [var shouldEnableLimits: Bool](/documentation/spritekit/skphysicsjointsliding/shouldenablelimits)
- [var lowerDistanceLimit: CGFloat](/documentation/spritekit/skphysicsjointsliding/lowerdistancelimit)
- [var upperDistanceLimit: CGFloat](/documentation/spritekit/skphysicsjointsliding/upperdistancelimit)
- [SKPhysicsJointSpring](/documentation/spritekit/skphysicsjointspring)

### First Steps

- [Getting Started with Spring Joints](/documentation/spritekit/getting-started-with-spring-joints)

### Creating a Spring Joint

- [class func joint(withBodyA: SKPhysicsBody, bodyB: SKPhysicsBody, anchorA: CGPoint, anchorB: CGPoint) -> SKPhysicsJointSpring](/documentation/spritekit/skphysicsjointspring/joint(withbodya:bodyb:anchora:anchorb:))

### Configuring a Spring Joint

- [var damping: CGFloat](/documentation/spritekit/skphysicsjointspring/damping)
- [var frequency: CGFloat](/documentation/spritekit/skphysicsjointspring/frequency)

## Tiling

- [SKTileMapNode](/documentation/spritekit/sktilemapnode)

### Creating a Tile Map Programmatically

- [Creating a Tile Map Programmatically](/documentation/spritekit/creating-a-tile-map-programmatically)

#### Creating a Tile Map

- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize)](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:))
- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, fillWith: SKTileGroup)](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:fillwith:))
- [init(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, tileGroupLayout: [SKTileGroup])](/documentation/spritekit/sktilemapnode/init(tileset:columns:rows:tilesize:tilegrouplayout:))
- [class func tileMapNodes(tileSet: SKTileSet, columns: Int, rows: Int, tileSize: CGSize, from: GKNoiseMap, tileTypeNoiseMapThresholds: [NSNumber]) -> [SKTileMapNode]](/documentation/spritekit/sktilemapnode/tilemapnodes(tileset:columns:rows:tilesize:from:tiletypenoisemapthresholds:))

#### Defining a Tile Map’s Contents

- [var enableAutomapping: Bool](/documentation/spritekit/sktilemapnode/enableautomapping)
- [func fill(with: SKTileGroup?)](/documentation/spritekit/sktilemapnode/fill(with:))
- [func setTileGroup(SKTileGroup, andTileDefinition: SKTileDefinition, forColumn: Int, row: Int)](/documentation/spritekit/sktilemapnode/settilegroup(_:andtiledefinition:forcolumn:row:))
- [func setTileGroup(SKTileGroup?, forColumn: Int, row: Int)](/documentation/spritekit/sktilemapnode/settilegroup(_:forcolumn:row:))

### Controlling a Tile Map’s On-Screen Position Relative to its Origin

- [var anchorPoint: CGPoint](/documentation/spritekit/sktilemapnode/anchorpoint)

### Reading or Manually Configuring the Tile Map’s Size

- [var tileSize: CGSize](/documentation/spritekit/sktilemapnode/tilesize)
- [var tileSet: SKTileSet](/documentation/spritekit/sktilemapnode/tileset)
- [var numberOfColumns: Int](/documentation/spritekit/sktilemapnode/numberofcolumns)
- [var numberOfRows: Int](/documentation/spritekit/sktilemapnode/numberofrows)

### Querying the Tile Map’s Properties

- [func centerOfTile(atColumn: Int, row: Int) -> CGPoint](/documentation/spritekit/sktilemapnode/centeroftile(atcolumn:row:))
- [func tileColumnIndex(fromPosition: CGPoint) -> Int](/documentation/spritekit/sktilemapnode/tilecolumnindex(fromposition:))
- [func tileDefinition(atColumn: Int, row: Int) -> SKTileDefinition?](/documentation/spritekit/sktilemapnode/tiledefinition(atcolumn:row:))
- [func tileGroup(atColumn: Int, row: Int) -> SKTileGroup?](/documentation/spritekit/sktilemapnode/tilegroup(atcolumn:row:))
- [func tileRowIndex(fromPosition: CGPoint) -> Int](/documentation/spritekit/sktilemapnode/tilerowindex(fromposition:))
- [var mapSize: CGSize](/documentation/spritekit/sktilemapnode/mapsize)

### Tinting a Tile Map

- [var color: UIColor](/documentation/spritekit/sktilemapnode/color)
- [var colorBlendFactor: CGFloat](/documentation/spritekit/sktilemapnode/colorblendfactor)

### Lighting a Tile Map

- [var lightingBitMask: UInt32](/documentation/spritekit/sktilemapnode/lightingbitmask)

### Configuring How Alpha Values Blend the Sprite

- [var blendMode: SKBlendMode](/documentation/spritekit/sktilemapnode/blendmode)

### Working with Custom Shaders

- [var shader: SKShader?](/documentation/spritekit/sktilemapnode/shader)
- [var attributeValues: [String : SKAttributeValue]](/documentation/spritekit/sktilemapnode/attributevalues)
- [func setValue(SKAttributeValue, forAttribute: String)](/documentation/spritekit/sktilemapnode/setvalue(_:forattribute:))
- [func value(forAttributeNamed: String) -> SKAttributeValue?](/documentation/spritekit/sktilemapnode/value(forattributenamed:))
- [SKTileDefinition](/documentation/spritekit/sktiledefinition)

### Creating a Tile with a Texture

- [init(texture: SKTexture)](/documentation/spritekit/sktiledefinition/init(texture:))

### Creating a Tile with a Normal Texture

- [init(texture: SKTexture, normalTexture: SKTexture, size: CGSize)](/documentation/spritekit/sktiledefinition/init(texture:normaltexture:size:))

### Creating a Tile with a Size

- [init(texture: SKTexture, size: CGSize)](/documentation/spritekit/sktiledefinition/init(texture:size:))

### Creating an Animated Tile

- [init(textures: [SKTexture], normalTextures: [SKTexture], size: CGSize, timePerFrame: CGFloat)](/documentation/spritekit/sktiledefinition/init(textures:normaltextures:size:timeperframe:))
- [init(textures: [SKTexture], size: CGSize, timePerFrame: CGFloat)](/documentation/spritekit/sktiledefinition/init(textures:size:timeperframe:))

### Flipping a Tile Vertically or Horizontally

- [var flipHorizontally: Bool](/documentation/spritekit/sktiledefinition/fliphorizontally)
- [var flipVertically: Bool](/documentation/spritekit/sktiledefinition/flipvertically)

### Rotating a Tile

- [var rotation: SKTileDefinitionRotation](/documentation/spritekit/sktiledefinition/rotation)
- [SKTileDefinitionRotation](/documentation/spritekit/sktiledefinitionrotation)

#### Enumeration Cases

- [case rotation0](/documentation/spritekit/sktiledefinitionrotation/rotation0)
- [case rotation180](/documentation/spritekit/sktiledefinitionrotation/rotation180)
- [case rotation270](/documentation/spritekit/sktiledefinitionrotation/rotation270)
- [case rotation90](/documentation/spritekit/sktiledefinitionrotation/rotation90)

#### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/sktiledefinitionrotation/init(rawvalue:))

### Configure Animated Tile Properties

- [var textures: [SKTexture]](/documentation/spritekit/sktiledefinition/textures)
- [var normalTextures: [SKTexture]](/documentation/spritekit/sktiledefinition/normaltextures)
- [var timePerFrame: CGFloat](/documentation/spritekit/sktiledefinition/timeperframe)

### Reading or Adding a Tile’s Custom Data

- [var userData: NSMutableDictionary?](/documentation/spritekit/sktiledefinition/userdata)

### Reading or Adjusting a Tile’s Instance Properties

- [var name: String?](/documentation/spritekit/sktiledefinition/name)
- [var placementWeight: Int](/documentation/spritekit/sktiledefinition/placementweight)
- [var size: CGSize](/documentation/spritekit/sktiledefinition/size)
- [SKTileGroup](/documentation/spritekit/sktilegroup)

### Creating Tile Groups

- [Creating Tile Groups Programmatically](/documentation/spritekit/creating-tile-groups-programmatically)
- [init(tileDefinition: SKTileDefinition)](/documentation/spritekit/sktilegroup/init(tiledefinition:))
- [init(rules: [SKTileGroupRule])](/documentation/spritekit/sktilegroup/init(rules:))

### Accessing or Setting a Tile Group’s Properties

- [var name: String?](/documentation/spritekit/sktilegroup/name)
- [var rules: [SKTileGroupRule]](/documentation/spritekit/sktilegroup/rules)

### Creating an Empty Tile Group

- [class func empty() -> Self](/documentation/spritekit/sktilegroup/empty())
- [SKTileGroupRule](/documentation/spritekit/sktilegrouprule)

### Creating a Tile Group Rule

- [init(adjacency: SKTileAdjacencyMask, tileDefinitions: [SKTileDefinition])](/documentation/spritekit/sktilegrouprule/init(adjacency:tiledefinitions:))

### Accessing or Setting Tile Group Rule Properties

- [var adjacency: SKTileAdjacencyMask](/documentation/spritekit/sktilegrouprule/adjacency)
- [SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask)

#### Initializers

- [init(rawValue: UInt)](/documentation/spritekit/sktileadjacencymask/init(rawvalue:))

#### Masks

- [static var adjacencyAll: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyall)
- [static var adjacencyDown: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencydown)
- [static var adjacencyDownEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencydownedge)
- [static var adjacencyLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyleft)
- [static var adjacencyLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyleftedge)
- [static var adjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleft)
- [static var adjacencyLowerLeftCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleftcorner)
- [static var adjacencyLowerLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleftedge)
- [static var adjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerright)
- [static var adjacencyLowerRightCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerrightcorner)
- [static var adjacencyLowerRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerrightedge)
- [static var adjacencyRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyright)
- [static var adjacencyRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyrightedge)
- [static var adjacencyUp: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyup)
- [static var adjacencyUpEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupedge)
- [static var adjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleft)
- [static var adjacencyUpperLeftCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleftcorner)
- [static var adjacencyUpperLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleftedge)
- [static var adjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperright)
- [static var adjacencyUpperRightCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperrightcorner)
- [static var adjacencyUpperRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperrightedge)
- [static var hexFlatAdjacencyAll: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyall)
- [static var hexFlatAdjacencyDown: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencydown)
- [static var hexFlatAdjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencylowerleft)
- [static var hexFlatAdjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencylowerright)
- [static var hexFlatAdjacencyUp: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyup)
- [static var hexFlatAdjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyupperleft)
- [static var hexFlatAdjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyupperright)
- [static var hexPointyAdjacencyAdd: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyadd)
- [static var hexPointyAdjacencyLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyleft)
- [static var hexPointyAdjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencylowerleft)
- [static var hexPointyAdjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencylowerright)
- [static var hexPointyAdjacencyRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyright)
- [static var hexPointyAdjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyupperleft)
- [static var hexPointyAdjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyupperright)
- [var name: String?](/documentation/spritekit/sktilegrouprule/name)
- [var tileDefinitions: [SKTileDefinition]](/documentation/spritekit/sktilegrouprule/tiledefinitions)
- [SKTileSet](/documentation/spritekit/sktileset)

### Creating a Tile Set from a File

- [convenience init?(named: String)](/documentation/spritekit/sktileset/init(named:))
- [convenience init?(from: URL)](/documentation/spritekit/sktileset/init(from:))

### Creating a Tile Set Programmatically

- [init(tileGroups: [SKTileGroup])](/documentation/spritekit/sktileset/init(tilegroups:))
- [init(tileGroups: [SKTileGroup], tileSetType: SKTileSetType)](/documentation/spritekit/sktileset/init(tilegroups:tilesettype:))

### Accessing or Reading a Tile Set’s Properties

- [var defaultTileGroup: SKTileGroup?](/documentation/spritekit/sktileset/defaulttilegroup)
- [var defaultTileSize: CGSize](/documentation/spritekit/sktileset/defaulttilesize)
- [var name: String?](/documentation/spritekit/sktileset/name)
- [var tileGroups: [SKTileGroup]](/documentation/spritekit/sktileset/tilegroups)
- [var type: SKTileSetType](/documentation/spritekit/sktileset/type)
- [SKTileSetType](/documentation/spritekit/sktilesettype)

#### Enumeration Cases

- [case grid](/documentation/spritekit/sktilesettype/grid)
- [case hexagonalFlat](/documentation/spritekit/sktilesettype/hexagonalflat)
- [case hexagonalPointy](/documentation/spritekit/sktilesettype/hexagonalpointy)
- [case isometric](/documentation/spritekit/sktilesettype/isometric)

#### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/sktilesettype/init(rawvalue:))

## Shaders

- [SKShader](/documentation/spritekit/skshader)

### Creating a Shader

- [Creating a Custom Fragment Shader](/documentation/spritekit/creating-a-custom-fragment-shader)
- [convenience init(fileNamed: String)](/documentation/spritekit/skshader/init(filenamed:))
- [init(source: String, uniforms: [SKUniform])](/documentation/spritekit/skshader/init(source:uniforms:))
- [init(source: String)](/documentation/spritekit/skshader/init(source:))

### Providing Uniform Data to a Shader

- [func addUniform(SKUniform)](/documentation/spritekit/skshader/adduniform(_:))
- [func removeUniformNamed(String)](/documentation/spritekit/skshader/removeuniformnamed(_:))
- [var uniforms: [SKUniform]](/documentation/spritekit/skshader/uniforms)
- [func uniformNamed(String) -> SKUniform?](/documentation/spritekit/skshader/uniformnamed(_:))

### Providing Attribute Data to a Shader

- [var attributes: [SKAttribute]](/documentation/spritekit/skshader/attributes)

### Accessing or Setting a Shader’s Source Code

- [var source: String?](/documentation/spritekit/skshader/source)

### Executing Shaders in Metal and OpenGL

- [Executing Shaders in Metal and OpenGL](/documentation/spritekit/executing-shaders-in-metal-and-opengl)
- [SKAttribute](/documentation/spritekit/skattribute)

### Constants

- [SKAttributeType](/documentation/spritekit/skattributetype)

#### Enumeration Cases

- [case float](/documentation/spritekit/skattributetype/float)
- [case halfFloat](/documentation/spritekit/skattributetype/halffloat)
- [case none](/documentation/spritekit/skattributetype/none)
- [case vectorFloat2](/documentation/spritekit/skattributetype/vectorfloat2)
- [case vectorFloat3](/documentation/spritekit/skattributetype/vectorfloat3)
- [case vectorFloat4](/documentation/spritekit/skattributetype/vectorfloat4)
- [case vectorHalfFloat2](/documentation/spritekit/skattributetype/vectorhalffloat2)
- [case vectorHalfFloat3](/documentation/spritekit/skattributetype/vectorhalffloat3)
- [case vectorHalfFloat4](/documentation/spritekit/skattributetype/vectorhalffloat4)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skattributetype/init(rawvalue:))

### Initializers

- [init(name: String, type: SKAttributeType)](/documentation/spritekit/skattribute/init(name:type:))

### Instance Properties

- [var name: String](/documentation/spritekit/skattribute/name)
- [var type: SKAttributeType](/documentation/spritekit/skattribute/type)
- [SKAttributeValue](/documentation/spritekit/skattributevalue)

### Initializers

- [init()](/documentation/spritekit/skattributevalue/init())
- [convenience init(float: Float)](/documentation/spritekit/skattributevalue/init(float:))
- [convenience init(vectorFloat2: vector_float2)](/documentation/spritekit/skattributevalue/init(vectorfloat2:))
- [convenience init(vectorFloat3: vector_float3)](/documentation/spritekit/skattributevalue/init(vectorfloat3:))
- [convenience init(vectorFloat4: vector_float4)](/documentation/spritekit/skattributevalue/init(vectorfloat4:))

### Instance Properties

- [var floatValue: Float](/documentation/spritekit/skattributevalue/floatvalue)
- [var vectorFloat2Value: vector_float2](/documentation/spritekit/skattributevalue/vectorfloat2value)
- [var vectorFloat3Value: vector_float3](/documentation/spritekit/skattributevalue/vectorfloat3value)
- [var vectorFloat4Value: vector_float4](/documentation/spritekit/skattributevalue/vectorfloat4value)
- [SKUniform](/documentation/spritekit/skuniform)

### Creating and Initializing Uniform Objects

- [init(name: String)](/documentation/spritekit/skuniform/init(name:))
- [init(name: String, float: Float)](/documentation/spritekit/skuniform/init(name:float:)-48rln)
- [init(name: String, float: GLKVector2)](/documentation/spritekit/skuniform/init(name:float:)-9g5vj)
- [init(name: String, float: GLKVector3)](/documentation/spritekit/skuniform/init(name:float:)-9g6a7)
- [init(name: String, float: GLKVector4)](/documentation/spritekit/skuniform/init(name:float:)-9g7j7)
- [init(name: String, float: GLKMatrix2)](/documentation/spritekit/skuniform/init(name:float:)-6110m)
- [init(name: String, float: GLKMatrix3)](/documentation/spritekit/skuniform/init(name:float:)-611hs)
- [init(name: String, float: GLKMatrix4)](/documentation/spritekit/skuniform/init(name:float:)-60zbm)
- [init(name: String, texture: SKTexture?)](/documentation/spritekit/skuniform/init(name:texture:))

### Reading Information About a Uniform

- [var name: String](/documentation/spritekit/skuniform/name)
- [var uniformType: SKUniformType](/documentation/spritekit/skuniform/uniformtype)

### Reading and Writing an Uniform Object’s Value

- [var floatValue: Float](/documentation/spritekit/skuniform/floatvalue)
- [var floatVector2Value: GLKVector2](/documentation/spritekit/skuniform/floatvector2value)
- [var floatVector3Value: GLKVector3](/documentation/spritekit/skuniform/floatvector3value)
- [var floatVector4Value: GLKVector4](/documentation/spritekit/skuniform/floatvector4value)
- [var floatMatrix2Value: GLKMatrix2](/documentation/spritekit/skuniform/floatmatrix2value)
- [var floatMatrix3Value: GLKMatrix3](/documentation/spritekit/skuniform/floatmatrix3value)
- [var floatMatrix4Value: GLKMatrix4](/documentation/spritekit/skuniform/floatmatrix4value)
- [var textureValue: SKTexture?](/documentation/spritekit/skuniform/texturevalue)

### Constants

- [SKUniformType](/documentation/spritekit/skuniformtype)

#### Constants

- [case none](/documentation/spritekit/skuniformtype/none)
- [case float](/documentation/spritekit/skuniformtype/float)
- [case floatVector2](/documentation/spritekit/skuniformtype/floatvector2)
- [case floatVector3](/documentation/spritekit/skuniformtype/floatvector3)
- [case floatVector4](/documentation/spritekit/skuniformtype/floatvector4)
- [case floatMatrix2](/documentation/spritekit/skuniformtype/floatmatrix2)
- [case floatMatrix3](/documentation/spritekit/skuniformtype/floatmatrix3)
- [case floatMatrix4](/documentation/spritekit/skuniformtype/floatmatrix4)
- [case texture](/documentation/spritekit/skuniformtype/texture)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skuniformtype/init(rawvalue:))

### Initializers

- [init(name: String, matrixFloat2x2: matrix_float2x2)](/documentation/spritekit/skuniform/init(name:matrixfloat2x2:))
- [init(name: String, matrixFloat3x3: matrix_float3x3)](/documentation/spritekit/skuniform/init(name:matrixfloat3x3:))
- [init(name: String, matrixFloat4x4: matrix_float4x4)](/documentation/spritekit/skuniform/init(name:matrixfloat4x4:))
- [init(name: String, vectorFloat2: vector_float2)](/documentation/spritekit/skuniform/init(name:vectorfloat2:))
- [init(name: String, vectorFloat3: vector_float3)](/documentation/spritekit/skuniform/init(name:vectorfloat3:))
- [init(name: String, vectorFloat4: vector_float4)](/documentation/spritekit/skuniform/init(name:vectorfloat4:))

### Instance Properties

- [var matrixFloat2x2Value: matrix_float2x2](/documentation/spritekit/skuniform/matrixfloat2x2value)
- [var matrixFloat3x3Value: matrix_float3x3](/documentation/spritekit/skuniform/matrixfloat3x3value)
- [var matrixFloat4x4Value: matrix_float4x4](/documentation/spritekit/skuniform/matrixfloat4x4value)
- [var vectorFloat2Value: vector_float2](/documentation/spritekit/skuniform/vectorfloat2value)
- [var vectorFloat3Value: vector_float3](/documentation/spritekit/skuniform/vectorfloat3value)
- [var vectorFloat4Value: vector_float4](/documentation/spritekit/skuniform/vectorfloat4value)

## Warping

- [SKWarpGeometry](/documentation/spritekit/skwarpgeometry)
- [SKWarpGeometryGrid](/documentation/spritekit/skwarpgeometrygrid)

### Creating a Warp Geometry Grid

- [convenience init(columns: Int, rows: Int)](/documentation/spritekit/skwarpgeometrygrid/init(columns:rows:))
- [convenience init(columns: Int, rows: Int, sourcePositions: [SIMD2<Float>], destinationPositions: [SIMD2<Float>])](/documentation/spritekit/skwarpgeometrygrid/init(columns:rows:sourcepositions:destinationpositions:))
- [init?(coder: NSCoder)](/documentation/spritekit/skwarpgeometrygrid/init(coder:))

### Animating Warping

- [Animate the Warping of a Sprite](/documentation/spritekit/animate-the-warping-of-a-sprite)

### Accessing or Setting Warp Geometry Grid Size

- [var numberOfColumns: Int](/documentation/spritekit/skwarpgeometrygrid/numberofcolumns)
- [var numberOfRows: Int](/documentation/spritekit/skwarpgeometrygrid/numberofrows)
- [var vertexCount: Int](/documentation/spritekit/skwarpgeometrygrid/vertexcount)

### Accessing or Setting Grid Vertices

- [func destPosition(at: Int) -> vector_float2](/documentation/spritekit/skwarpgeometrygrid/destposition(at:))
- [func replacingByDestinationPositions(positions: [SIMD2<Float>]) -> SKWarpGeometryGrid](/documentation/spritekit/skwarpgeometrygrid/replacingbydestinationpositions(positions:))
- [func replacingBySourcePositions(positions: [SIMD2<Float>]) -> SKWarpGeometryGrid](/documentation/spritekit/skwarpgeometrygrid/replacingbysourcepositions(positions:))
- [func sourcePosition(at: Int) -> vector_float2](/documentation/spritekit/skwarpgeometrygrid/sourceposition(at:))
- [SKWarpable](/documentation/spritekit/skwarpable)

### Instance Properties

- [var subdivisionLevels: Int](/documentation/spritekit/skwarpable/subdivisionlevels)
- [var warpGeometry: SKWarpGeometry?](/documentation/spritekit/skwarpable/warpgeometry)

## Reference

- [SpriteKit Enumerations](/documentation/spritekit/spritekit-enumerations)

### Enumerations

- [SKActionTimingMode](/documentation/spritekit/skactiontimingmode)

#### Constants

- [case linear](/documentation/spritekit/skactiontimingmode/linear)
- [case easeIn](/documentation/spritekit/skactiontimingmode/easein)
- [case easeOut](/documentation/spritekit/skactiontimingmode/easeout)
- [case easeInEaseOut](/documentation/spritekit/skactiontimingmode/easeineaseout)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skactiontimingmode/init(rawvalue:))
- [SKAttributeType](/documentation/spritekit/skattributetype)

#### Enumeration Cases

- [case float](/documentation/spritekit/skattributetype/float)
- [case halfFloat](/documentation/spritekit/skattributetype/halffloat)
- [case none](/documentation/spritekit/skattributetype/none)
- [case vectorFloat2](/documentation/spritekit/skattributetype/vectorfloat2)
- [case vectorFloat3](/documentation/spritekit/skattributetype/vectorfloat3)
- [case vectorFloat4](/documentation/spritekit/skattributetype/vectorfloat4)
- [case vectorHalfFloat2](/documentation/spritekit/skattributetype/vectorhalffloat2)
- [case vectorHalfFloat3](/documentation/spritekit/skattributetype/vectorhalffloat3)
- [case vectorHalfFloat4](/documentation/spritekit/skattributetype/vectorhalffloat4)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skattributetype/init(rawvalue:))
- [SKBlendMode](/documentation/spritekit/skblendmode)

#### Constants

- [case alpha](/documentation/spritekit/skblendmode/alpha)
- [case add](/documentation/spritekit/skblendmode/add)
- [case subtract](/documentation/spritekit/skblendmode/subtract)
- [case multiply](/documentation/spritekit/skblendmode/multiply)
- [case multiplyX2](/documentation/spritekit/skblendmode/multiplyx2)
- [case screen](/documentation/spritekit/skblendmode/screen)
- [case replace](/documentation/spritekit/skblendmode/replace)

#### Enumeration Cases

- [case multiplyAlpha](/documentation/spritekit/skblendmode/multiplyalpha)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skblendmode/init(rawvalue:))
- [SKInterpolationMode](/documentation/spritekit/skinterpolationmode)

#### Constants

- [case linear](/documentation/spritekit/skinterpolationmode/linear)
- [case spline](/documentation/spritekit/skinterpolationmode/spline)
- [case step](/documentation/spritekit/skinterpolationmode/step)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skinterpolationmode/init(rawvalue:))
- [SKLabelHorizontalAlignmentMode](/documentation/spritekit/sklabelhorizontalalignmentmode)

#### Constants

- [case center](/documentation/spritekit/sklabelhorizontalalignmentmode/center)
- [case left](/documentation/spritekit/sklabelhorizontalalignmentmode/left)
- [case right](/documentation/spritekit/sklabelhorizontalalignmentmode/right)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sklabelhorizontalalignmentmode/init(rawvalue:))
- [SKLabelVerticalAlignmentMode](/documentation/spritekit/sklabelverticalalignmentmode)

#### Constants

- [case baseline](/documentation/spritekit/sklabelverticalalignmentmode/baseline)
- [case center](/documentation/spritekit/sklabelverticalalignmentmode/center)
- [case top](/documentation/spritekit/sklabelverticalalignmentmode/top)
- [case bottom](/documentation/spritekit/sklabelverticalalignmentmode/bottom)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sklabelverticalalignmentmode/init(rawvalue:))
- [SKParticleRenderOrder](/documentation/spritekit/skparticlerenderorder)

#### Constants

- [case oldestLast](/documentation/spritekit/skparticlerenderorder/oldestlast)
- [case oldestFirst](/documentation/spritekit/skparticlerenderorder/oldestfirst)
- [case dontCare](/documentation/spritekit/skparticlerenderorder/dontcare)

#### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/skparticlerenderorder/init(rawvalue:))
- [SKRepeatMode](/documentation/spritekit/skrepeatmode)

#### Constants

- [case clamp](/documentation/spritekit/skrepeatmode/clamp)
- [case loop](/documentation/spritekit/skrepeatmode/loop)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skrepeatmode/init(rawvalue:))
- [SKSceneScaleMode](/documentation/spritekit/skscenescalemode)

#### Constants

- [case fill](/documentation/spritekit/skscenescalemode/fill)
- [case aspectFill](/documentation/spritekit/skscenescalemode/aspectfill)
- [case aspectFit](/documentation/spritekit/skscenescalemode/aspectfit)
- [case resizeFill](/documentation/spritekit/skscenescalemode/resizefill)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skscenescalemode/init(rawvalue:))
- [SKTextureFilteringMode](/documentation/spritekit/sktexturefilteringmode)

#### Constants

- [case nearest](/documentation/spritekit/sktexturefilteringmode/nearest)
- [case linear](/documentation/spritekit/sktexturefilteringmode/linear)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sktexturefilteringmode/init(rawvalue:))
- [SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask)

#### Initializers

- [init(rawValue: UInt)](/documentation/spritekit/sktileadjacencymask/init(rawvalue:))

#### Masks

- [static var adjacencyAll: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyall)
- [static var adjacencyDown: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencydown)
- [static var adjacencyDownEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencydownedge)
- [static var adjacencyLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyleft)
- [static var adjacencyLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyleftedge)
- [static var adjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleft)
- [static var adjacencyLowerLeftCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleftcorner)
- [static var adjacencyLowerLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerleftedge)
- [static var adjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerright)
- [static var adjacencyLowerRightCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerrightcorner)
- [static var adjacencyLowerRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencylowerrightedge)
- [static var adjacencyRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyright)
- [static var adjacencyRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyrightedge)
- [static var adjacencyUp: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyup)
- [static var adjacencyUpEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupedge)
- [static var adjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleft)
- [static var adjacencyUpperLeftCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleftcorner)
- [static var adjacencyUpperLeftEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperleftedge)
- [static var adjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperright)
- [static var adjacencyUpperRightCorner: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperrightcorner)
- [static var adjacencyUpperRightEdge: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/adjacencyupperrightedge)
- [static var hexFlatAdjacencyAll: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyall)
- [static var hexFlatAdjacencyDown: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencydown)
- [static var hexFlatAdjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencylowerleft)
- [static var hexFlatAdjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencylowerright)
- [static var hexFlatAdjacencyUp: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyup)
- [static var hexFlatAdjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyupperleft)
- [static var hexFlatAdjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexflatadjacencyupperright)
- [static var hexPointyAdjacencyAdd: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyadd)
- [static var hexPointyAdjacencyLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyleft)
- [static var hexPointyAdjacencyLowerLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencylowerleft)
- [static var hexPointyAdjacencyLowerRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencylowerright)
- [static var hexPointyAdjacencyRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyright)
- [static var hexPointyAdjacencyUpperLeft: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyupperleft)
- [static var hexPointyAdjacencyUpperRight: SKTileAdjacencyMask](/documentation/spritekit/sktileadjacencymask/hexpointyadjacencyupperright)
- [SKTileDefinitionRotation](/documentation/spritekit/sktiledefinitionrotation)

#### Enumeration Cases

- [case rotation0](/documentation/spritekit/sktiledefinitionrotation/rotation0)
- [case rotation180](/documentation/spritekit/sktiledefinitionrotation/rotation180)
- [case rotation270](/documentation/spritekit/sktiledefinitionrotation/rotation270)
- [case rotation90](/documentation/spritekit/sktiledefinitionrotation/rotation90)

#### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/sktiledefinitionrotation/init(rawvalue:))
- [SKTileSetType](/documentation/spritekit/sktilesettype)

#### Enumeration Cases

- [case grid](/documentation/spritekit/sktilesettype/grid)
- [case hexagonalFlat](/documentation/spritekit/sktilesettype/hexagonalflat)
- [case hexagonalPointy](/documentation/spritekit/sktilesettype/hexagonalpointy)
- [case isometric](/documentation/spritekit/sktilesettype/isometric)

#### Initializers

- [init?(rawValue: UInt)](/documentation/spritekit/sktilesettype/init(rawvalue:))
- [SKTransitionDirection](/documentation/spritekit/sktransitiondirection)

#### Constants

- [case up](/documentation/spritekit/sktransitiondirection/up)
- [case down](/documentation/spritekit/sktransitiondirection/down)
- [case right](/documentation/spritekit/sktransitiondirection/right)
- [case left](/documentation/spritekit/sktransitiondirection/left)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sktransitiondirection/init(rawvalue:))
- [SKUniformType](/documentation/spritekit/skuniformtype)

#### Constants

- [case none](/documentation/spritekit/skuniformtype/none)
- [case float](/documentation/spritekit/skuniformtype/float)
- [case floatVector2](/documentation/spritekit/skuniformtype/floatvector2)
- [case floatVector3](/documentation/spritekit/skuniformtype/floatvector3)
- [case floatVector4](/documentation/spritekit/skuniformtype/floatvector4)
- [case floatMatrix2](/documentation/spritekit/skuniformtype/floatmatrix2)
- [case floatMatrix3](/documentation/spritekit/skuniformtype/floatmatrix3)
- [case floatMatrix4](/documentation/spritekit/skuniformtype/floatmatrix4)
- [case texture](/documentation/spritekit/skuniformtype/texture)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/skuniformtype/init(rawvalue:))
- [SKNodeFocusBehavior](/documentation/spritekit/sknodefocusbehavior)

#### Enumeration Cases

- [case none](/documentation/spritekit/sknodefocusbehavior/none)
- [case occluding](/documentation/spritekit/sknodefocusbehavior/occluding)
- [case focusable](/documentation/spritekit/sknodefocusbehavior/focusable)

#### Initializers

- [init?(rawValue: Int)](/documentation/spritekit/sknodefocusbehavior/init(rawvalue:))
- [SpriteKit Data Types](/documentation/spritekit/spritekit-data-types)

### Data Types

- [SKActionTimingFunction](/documentation/spritekit/skactiontimingfunction)
- [SKFieldForceEvaluator](/documentation/spritekit/skfieldforceevaluator)
- [SpriteKit Constants](/documentation/spritekit/spritekit-constants)

### Constants

- [var PHYSICSKIT_MINUS_GL_IMPORTS: Int32](/documentation/spritekit/physicskit_minus_gl_imports)
- [SpriteKit Type Aliases](/documentation/spritekit/spritekit-type-aliases)

### Type Aliases

- [SKColor](/documentation/spritekit/skcolor-swift.typealias)
- [SpriteKit Variables](/documentation/spritekit/spritekit-variables)

### Global variables

- [var SKVIEW_AVAILABLE: Int32](/documentation/spritekit/skview_available)
- [var SK_VERSION: Int32](/documentation/spritekit/sk_version)

## Structures

- [SpriteView](/documentation/spritekit/spriteview)

### Creating a Sprite View

- [init(scene: SKScene, transition: SKTransition?, isPaused: Bool, preferredFramesPerSecond: Int)](/documentation/spritekit/spriteview/init(scene:transition:ispaused:preferredframespersecond:))
- [init(scene: SKScene, transition: SKTransition?, isPaused: Bool, preferredFramesPerSecond: Int, options: SpriteView.Options, shouldRender: (TimeInterval) -> Bool)](/documentation/spritekit/spriteview/init(scene:transition:ispaused:preferredframespersecond:options:shouldrender:))
- [init(scene: SKScene, transition: SKTransition?, isPaused: Bool, preferredFramesPerSecond: Int, options: SpriteView.Options, debugOptions: SpriteView.DebugOptions, shouldRender: (TimeInterval) -> Bool)](/documentation/spritekit/spriteview/init(scene:transition:ispaused:preferredframespersecond:options:debugoptions:shouldrender:))
- [SpriteView.Options](/documentation/spritekit/spriteview/options)

#### Type Properties

- [static let allowsTransparency: SpriteView.Options](/documentation/spritekit/spriteview/options/allowstransparency)
- [static let ignoresSiblingOrder: SpriteView.Options](/documentation/spritekit/spriteview/options/ignoressiblingorder)
- [static let shouldCullNonVisibleNodes: SpriteView.Options](/documentation/spritekit/spriteview/options/shouldcullnonvisiblenodes)
- [SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions)

#### Type Properties

- [static let showsDrawCount: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsdrawcount)
- [static let showsFPS: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsfps)
- [static let showsFields: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsfields)
- [static let showsNodeCount: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsnodecount)
- [static let showsPhysics: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsphysics)
- [static let showsQuadCount: SpriteView.DebugOptions](/documentation/spritekit/spriteview/debugoptions/showsquadcount)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
