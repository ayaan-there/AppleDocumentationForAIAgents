# Touch Controller Documentation

Source: https://sosumi.ai/documentation/touchcontroller

---
title: Touch Controller
source: https://developer.apple.com/documentation/touchcontroller
timestamp: 2026-02-13T19:03:11.467Z
---

## Essentials

- [TCTouchController](/documentation/touchcontroller/tctouchcontroller)

### Creating a touch controller

- [init(descriptor: TCTouchControllerDescriptor)](/documentation/touchcontroller/tctouchcontroller/init(descriptor:))
- [TCTouchControllerDescriptor](/documentation/touchcontroller/tctouchcontrollerdescriptor)

#### Creating a touch controller descriptor

- [init()](/documentation/touchcontroller/tctouchcontrollerdescriptor/init())
- [convenience init(mtkView: MTKView)](/documentation/touchcontroller/tctouchcontrollerdescriptor/init(mtkview:))

#### Inspecting the controller descriptor

- [var colorPixelFormat: MTLPixelFormat](/documentation/touchcontroller/tctouchcontrollerdescriptor/colorpixelformat)
- [var depthAttachmentPixelFormat: MTLPixelFormat](/documentation/touchcontroller/tctouchcontrollerdescriptor/depthattachmentpixelformat)
- [var device: any MTLDevice](/documentation/touchcontroller/tctouchcontrollerdescriptor/device)
- [var drawableSize: CGSize](/documentation/touchcontroller/tctouchcontrollerdescriptor/drawablesize)
- [var sampleCount: Int](/documentation/touchcontroller/tctouchcontrollerdescriptor/samplecount)
- [var size: CGSize](/documentation/touchcontroller/tctouchcontrollerdescriptor/size)
- [var stencilAttachmentPixelFormat: MTLPixelFormat](/documentation/touchcontroller/tctouchcontrollerdescriptor/stencilattachmentpixelformat)

### Inspecting the touch controller

- [var buttons: [TCButton]](/documentation/touchcontroller/tctouchcontroller/buttons)
- [var controls: [any TCControl]](/documentation/touchcontroller/tctouchcontroller/controls)
- [var device: any MTLDevice](/documentation/touchcontroller/tctouchcontroller/device)
- [var directionPads: [TCDirectionPad]](/documentation/touchcontroller/tctouchcontroller/directionpads)
- [var drawableSize: CGSize](/documentation/touchcontroller/tctouchcontroller/drawablesize)
- [var size: CGSize](/documentation/touchcontroller/tctouchcontroller/size)
- [var switches: [TCSwitch]](/documentation/touchcontroller/tctouchcontroller/switches)
- [var isConnected: Bool](/documentation/touchcontroller/tctouchcontroller/isconnected)
- [class var isSupported: Bool](/documentation/touchcontroller/tctouchcontroller/issupported)
- [var throttles: [TCThrottle]](/documentation/touchcontroller/tctouchcontroller/throttles)
- [var thumbsticks: [TCThumbstick]](/documentation/touchcontroller/tctouchcontroller/thumbsticks)
- [var touchpads: [TCTouchpad]](/documentation/touchcontroller/tctouchcontroller/touchpads)

### Getting the touch controller

- [var controller: GCController](/documentation/touchcontroller/tctouchcontroller/controller)

### Adding a button control

- [func addButton(descriptor: TCButtonDescriptor) -> TCButton](/documentation/touchcontroller/tctouchcontroller/addbutton(descriptor:))
- [TCButtonDescriptor](/documentation/touchcontroller/tcbuttondescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tcbuttondescriptor/init())

#### Inspecting the descriptor

- [var contents: TCControlContents?](/documentation/touchcontroller/tcbuttondescriptor/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcbuttondescriptor/highlightduration)
- [var zIndex: Int](/documentation/touchcontroller/tcbuttondescriptor/zindex)
- [var label: TCControlLabel](/documentation/touchcontroller/tcbuttondescriptor/label)
- [var offset: CGPoint](/documentation/touchcontroller/tcbuttondescriptor/offset)
- [var size: CGSize](/documentation/touchcontroller/tcbuttondescriptor/size)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tcbuttondescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tcbuttondescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcbuttondescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Adding a directional pad control

- [func addDirectionPad(descriptor: TCDirectionPadDescriptor) -> TCDirectionPad](/documentation/touchcontroller/tctouchcontroller/adddirectionpad(descriptor:))
- [TCDirectionPadDescriptor](/documentation/touchcontroller/tcdirectionpaddescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tcdirectionpaddescriptor/init())

#### Inspecting the descriptor

- [var compositeLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpaddescriptor/compositelabel)
- [var downContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpaddescriptor/downcontents)
- [var downLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpaddescriptor/downlabel)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcdirectionpaddescriptor/highlightduration)
- [var inputIsMutuallyExclusive: Bool](/documentation/touchcontroller/tcdirectionpaddescriptor/inputismutuallyexclusive)
- [var isDigital: Bool](/documentation/touchcontroller/tcdirectionpaddescriptor/isdigital)
- [var isRadial: Bool](/documentation/touchcontroller/tcdirectionpaddescriptor/isradial)
- [var leftContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpaddescriptor/leftcontents)
- [var leftLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpaddescriptor/leftlabel)
- [var offset: CGPoint](/documentation/touchcontroller/tcdirectionpaddescriptor/offset)
- [var rightContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpaddescriptor/rightcontents)
- [var rightLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpaddescriptor/rightlabel)
- [var size: CGSize](/documentation/touchcontroller/tcdirectionpaddescriptor/size)
- [var upContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpaddescriptor/upcontents)
- [var upLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpaddescriptor/uplabel)
- [var zIndex: Int](/documentation/touchcontroller/tcdirectionpaddescriptor/zindex)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tcdirectionpaddescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tcdirectionpaddescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcdirectionpaddescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Adding a switch control

- [func addSwitch(descriptor: TCSwitchDescriptor) -> TCSwitch](/documentation/touchcontroller/tctouchcontroller/addswitch(descriptor:))
- [TCSwitchDescriptor](/documentation/touchcontroller/tcswitchdescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tcswitchdescriptor/init())

#### Inspecting the descriptor

- [var contents: TCControlContents?](/documentation/touchcontroller/tcswitchdescriptor/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcswitchdescriptor/highlightduration)
- [var label: TCControlLabel](/documentation/touchcontroller/tcswitchdescriptor/label)
- [var offset: CGPoint](/documentation/touchcontroller/tcswitchdescriptor/offset)
- [var size: CGSize](/documentation/touchcontroller/tcswitchdescriptor/size)
- [var switchedOnContents: TCControlContents?](/documentation/touchcontroller/tcswitchdescriptor/switchedoncontents)
- [var zIndex: Int](/documentation/touchcontroller/tcswitchdescriptor/zindex)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tcswitchdescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tcswitchdescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcswitchdescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Adding a throttle control

- [func addThrottle(descriptor: TCThrottleDescriptor) -> TCThrottle](/documentation/touchcontroller/tctouchcontroller/addthrottle(descriptor:))
- [TCThrottleDescriptor](/documentation/touchcontroller/tcthrottledescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tcthrottledescriptor/init())

#### Inspecting the descriptor

- [var backgroundContents: TCControlContents?](/documentation/touchcontroller/tcthrottledescriptor/backgroundcontents)
- [var baseValue: CGFloat](/documentation/touchcontroller/tcthrottledescriptor/basevalue)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcthrottledescriptor/highlightduration)
- [var indicatorContents: TCControlContents?](/documentation/touchcontroller/tcthrottledescriptor/indicatorcontents)
- [var indicatorSize: CGSize](/documentation/touchcontroller/tcthrottledescriptor/indicatorsize)
- [var label: TCControlLabel](/documentation/touchcontroller/tcthrottledescriptor/label)
- [var offset: CGPoint](/documentation/touchcontroller/tcthrottledescriptor/offset)
- [var orientation: TCThrottle.Orientation](/documentation/touchcontroller/tcthrottledescriptor/orientation)
- [var size: CGSize](/documentation/touchcontroller/tcthrottledescriptor/size)
- [var snapsToBaseValue: Bool](/documentation/touchcontroller/tcthrottledescriptor/snapstobasevalue)
- [var throttleSize: CGSize](/documentation/touchcontroller/tcthrottledescriptor/throttlesize)
- [var zIndex: Int](/documentation/touchcontroller/tcthrottledescriptor/zindex)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tcthrottledescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tcthrottledescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcthrottledescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Adding a thumbstick control

- [func addThumbstick(descriptor: TCThumbstickDescriptor) -> TCThumbstick](/documentation/touchcontroller/tctouchcontroller/addthumbstick(descriptor:))
- [TCThumbstickDescriptor](/documentation/touchcontroller/tcthumbstickdescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tcthumbstickdescriptor/init())

#### Inspecting the descriptor

- [var backgroundContents: TCControlContents?](/documentation/touchcontroller/tcthumbstickdescriptor/backgroundcontents)
- [var hidesWhenNotPressed: Bool](/documentation/touchcontroller/tcthumbstickdescriptor/hideswhennotpressed)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcthumbstickdescriptor/highlightduration)
- [var label: TCControlLabel](/documentation/touchcontroller/tcthumbstickdescriptor/label)
- [var offset: CGPoint](/documentation/touchcontroller/tcthumbstickdescriptor/offset)
- [var size: CGSize](/documentation/touchcontroller/tcthumbstickdescriptor/size)
- [var stickContents: TCControlContents?](/documentation/touchcontroller/tcthumbstickdescriptor/stickcontents)
- [var stickSize: CGSize](/documentation/touchcontroller/tcthumbstickdescriptor/sticksize)
- [var zIndex: Int](/documentation/touchcontroller/tcthumbstickdescriptor/zindex)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tcthumbstickdescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tcthumbstickdescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcthumbstickdescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Adding a touchpad control

- [func addTouchpad(descriptor: TCTouchpadDescriptor) -> TCTouchpad](/documentation/touchcontroller/tctouchcontroller/addtouchpad(descriptor:))
- [TCTouchpadDescriptor](/documentation/touchcontroller/tctouchpaddescriptor)

#### Creating the descriptor

- [init()](/documentation/touchcontroller/tctouchpaddescriptor/init())

#### Inspecting the descriptor

- [var contents: TCControlContents?](/documentation/touchcontroller/tctouchpaddescriptor/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tctouchpaddescriptor/highlightduration)
- [var label: TCControlLabel](/documentation/touchcontroller/tctouchpaddescriptor/label)
- [var offset: CGPoint](/documentation/touchcontroller/tctouchpaddescriptor/offset)
- [var reportsRelativeValues: Bool](/documentation/touchcontroller/tctouchpaddescriptor/reportsrelativevalues)
- [var size: CGSize](/documentation/touchcontroller/tctouchpaddescriptor/size)
- [var zIndex: Int](/documentation/touchcontroller/tctouchpaddescriptor/zindex)

#### Accessing the anchor

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tctouchpaddescriptor/anchor)
- [TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayoutanchor)

##### Anchors

- [case bottomCenter](/documentation/touchcontroller/tccontrollayoutanchor/bottomcenter)
- [case bottomLeft](/documentation/touchcontroller/tccontrollayoutanchor/bottomleft)
- [case bottomRight](/documentation/touchcontroller/tccontrollayoutanchor/bottomright)
- [case center](/documentation/touchcontroller/tccontrollayoutanchor/center)
- [case centerLeft](/documentation/touchcontroller/tccontrollayoutanchor/centerleft)
- [case centerRight](/documentation/touchcontroller/tccontrollayoutanchor/centerright)
- [case topCenter](/documentation/touchcontroller/tccontrollayoutanchor/topcenter)
- [case topLeft](/documentation/touchcontroller/tccontrollayoutanchor/topleft)
- [case topRight](/documentation/touchcontroller/tccontrollayoutanchor/topright)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchor/init(rawvalue:))
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tctouchpaddescriptor/anchorcoordinatesystem)
- [TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem)

##### Anchors

- [case absolute](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/absolute)
- [case relative](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/relative)

##### Creating a layout anchor

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollayoutanchorcoordinatesystem/init(rawvalue:))

#### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tctouchpaddescriptor/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

##### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

##### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Connecting and disconnecting a controller

- [func connect()](/documentation/touchcontroller/tctouchcontroller/connect())
- [func disconnect()](/documentation/touchcontroller/tctouchcontroller/disconnect())

### Getting the controller at a point

- [func control(at: CGPoint) -> (any TCControl)?](/documentation/touchcontroller/tctouchcontroller/control(at:))

### Handling layout updates

- [func automaticallyLayoutControls(for: [TCControlLabel])](/documentation/touchcontroller/tctouchcontroller/automaticallylayoutcontrols(for:))
- [func render(using: any MTLRenderCommandEncoder)](/documentation/touchcontroller/tctouchcontroller/render(using:))

### Handling a touch

- [func handleTouchBegan(at: CGPoint, index: Int) -> Bool](/documentation/touchcontroller/tctouchcontroller/handletouchbegan(at:index:))
- [func handleTouchEnded(at: CGPoint, index: Int) -> Bool](/documentation/touchcontroller/tctouchcontroller/handletouchended(at:index:))
- [func handleTouchMoved(at: CGPoint, index: Int) -> Bool](/documentation/touchcontroller/tctouchcontroller/handletouchmoved(at:index:))

### Removing controls

- [func removeControl(any TCControl)](/documentation/touchcontroller/tctouchcontroller/removecontrol(_:))
- [func removeAllControls()](/documentation/touchcontroller/tctouchcontroller/removeallcontrols())

### Getting the touch controller category

- [let TCGameControllerProductCategoryTouchController: String](/documentation/touchcontroller/tcgamecontrollerproductcategorytouchcontroller)

## Controls

- [TCControl](/documentation/touchcontroller/tccontrol)

### Inspecting a control

- [var isEnabled: Bool](/documentation/touchcontroller/tccontrol/isenabled)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tccontrol/highlightduration)
- [var label: TCControlLabel](/documentation/touchcontroller/tccontrol/label)
- [TCControlLabel](/documentation/touchcontroller/tccontrollabel)

#### Creating a control label

- [init(name: String, role: TCControlLabel.Role)](/documentation/touchcontroller/tccontrollabel/init(name:role:))

#### Inspecting the control

- [var role: TCControlLabel.Role](/documentation/touchcontroller/tccontrollabel/role-swift.property)
- [TCControlLabel.Role](/documentation/touchcontroller/tccontrollabel/role-swift.enum)

##### Roles

- [case button](/documentation/touchcontroller/tccontrollabel/role-swift.enum/button)
- [case directionPad](/documentation/touchcontroller/tccontrollabel/role-swift.enum/directionpad)

##### Creating a role

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollabel/role-swift.enum/init(rawvalue:))
- [TCControlLabel.Role](/documentation/touchcontroller/tccontrollabel/role-swift.enum)

##### Roles

- [case button](/documentation/touchcontroller/tccontrollabel/role-swift.enum/button)
- [case directionPad](/documentation/touchcontroller/tccontrollabel/role-swift.enum/directionpad)

##### Creating a role

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrollabel/role-swift.enum/init(rawvalue:))

#### Accessing the controls

- [class var buttonA: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttona)
- [class var buttonB: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonb)
- [class var buttonLeftShoulder: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonleftshoulder)
- [class var buttonLeftTrigger: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonlefttrigger)
- [class var buttonMenu: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonmenu)
- [class var buttonOptions: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonoptions)
- [class var buttonRightShoulder: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonrightshoulder)
- [class var buttonRightTrigger: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonrighttrigger)
- [class var buttonX: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttonx)
- [class var buttonY: TCControlLabel](/documentation/touchcontroller/tccontrollabel/buttony)
- [class var directionPad: TCControlLabel](/documentation/touchcontroller/tccontrollabel/directionpad)
- [class var leftThumbstick: TCControlLabel](/documentation/touchcontroller/tccontrollabel/leftthumbstick)
- [class var leftThumbstickButton: TCControlLabel](/documentation/touchcontroller/tccontrollabel/leftthumbstickbutton)
- [class var rightThumbstick: TCControlLabel](/documentation/touchcontroller/tccontrollabel/rightthumbstick)
- [class var rightThumbstickButton: TCControlLabel](/documentation/touchcontroller/tccontrollabel/rightthumbstickbutton)

#### Instance Properties

- [var name: String](/documentation/touchcontroller/tccontrollabel/name)
- [var isPressed: Bool](/documentation/touchcontroller/tccontrol/ispressed)

### Handling touches

- [func handleTouchBegan(at: CGPoint)](/documentation/touchcontroller/tccontrol/handletouchbegan(at:))
- [func handleTouchMoved(at: CGPoint)](/documentation/touchcontroller/tccontrol/handletouchmoved(at:))
- [func handleTouchEnded(at: CGPoint)](/documentation/touchcontroller/tccontrol/handletouchended(at:))

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tccontrol/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))
- [TCButton](/documentation/touchcontroller/tcbutton)

### Inspecting a button

- [var contents: TCControlContents?](/documentation/touchcontroller/tcbutton/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcbutton/highlightduration)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcbutton/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))
- [TCDirectionPad](/documentation/touchcontroller/tcdirectionpad)

### Inspecting the direction pad

- [var compositeLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpad/compositelabel)
- [var downContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpad/downcontents)
- [var downLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpad/downlabel)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcdirectionpad/highlightduration)
- [var inputIsMutuallyExclusive: Bool](/documentation/touchcontroller/tcdirectionpad/inputismutuallyexclusive)
- [var isDigital: Bool](/documentation/touchcontroller/tcdirectionpad/isdigital)
- [var isRadial: Bool](/documentation/touchcontroller/tcdirectionpad/isradial)
- [var leftContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpad/leftcontents)
- [var leftLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpad/leftlabel)
- [var rightContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpad/rightcontents)
- [var rightLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpad/rightlabel)
- [var upContents: TCControlContents?](/documentation/touchcontroller/tcdirectionpad/upcontents)
- [var upLabel: TCControlLabel?](/documentation/touchcontroller/tcdirectionpad/uplabel)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcdirectionpad/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))
- [TCSwitch](/documentation/touchcontroller/tcswitch)

### Inspecting the switch

- [var contents: TCControlContents?](/documentation/touchcontroller/tcswitch/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcswitch/highlightduration)
- [var isSwitchedOn: Bool](/documentation/touchcontroller/tcswitch/isswitchedon)
- [var switchedOnContents: TCControlContents?](/documentation/touchcontroller/tcswitch/switchedoncontents)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcswitch/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))
- [TCThumbstick](/documentation/touchcontroller/tcthumbstick)

### Inspecting a thumbstick

- [var backgroundContents: TCControlContents?](/documentation/touchcontroller/tcthumbstick/backgroundcontents)
- [var hidesWhenNotPressed: Bool](/documentation/touchcontroller/tcthumbstick/hideswhennotpressed)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcthumbstick/highlightduration)
- [var stickContents: TCControlContents?](/documentation/touchcontroller/tcthumbstick/stickcontents)
- [var stickSize: CGSize](/documentation/touchcontroller/tcthumbstick/sticksize)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcthumbstick/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))
- [TCThrottle](/documentation/touchcontroller/tcthrottle)

### Inspecting the throttle

- [var backgroundContents: TCControlContents?](/documentation/touchcontroller/tcthrottle/backgroundcontents)
- [var baseValue: CGFloat](/documentation/touchcontroller/tcthrottle/basevalue)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tcthrottle/highlightduration)
- [var indicatorContents: TCControlContents?](/documentation/touchcontroller/tcthrottle/indicatorcontents)
- [var indicatorSize: CGSize](/documentation/touchcontroller/tcthrottle/indicatorsize)
- [var snapsToBaseValue: Bool](/documentation/touchcontroller/tcthrottle/snapstobasevalue)
- [var throttleSize: CGSize](/documentation/touchcontroller/tcthrottle/throttlesize)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tcthrottle/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

### Getting the orientation

- [var orientation: TCThrottle.Orientation](/documentation/touchcontroller/tcthrottle/orientation-swift.property)
- [TCThrottle.Orientation](/documentation/touchcontroller/tcthrottle/orientation-swift.enum)

#### Throttle orientations

- [case horizontal](/documentation/touchcontroller/tcthrottle/orientation-swift.enum/horizontal)
- [case vertical](/documentation/touchcontroller/tcthrottle/orientation-swift.enum/vertical)

#### Creating an orientation

- [init?(rawValue: Int)](/documentation/touchcontroller/tcthrottle/orientation-swift.enum/init(rawvalue:))
- [TCTouchpad](/documentation/touchcontroller/tctouchpad)

### Inspecting at touchpad

- [var contents: TCControlContents?](/documentation/touchcontroller/tctouchpad/contents)
- [var highlightDuration: TimeInterval](/documentation/touchcontroller/tctouchpad/highlightduration)
- [var reportsRelativeValues: Bool](/documentation/touchcontroller/tctouchpad/reportsrelativevalues)

### Getting the collider shape

- [var colliderShape: TCColliderShape](/documentation/touchcontroller/tctouchpad/collidershape)
- [TCColliderShape](/documentation/touchcontroller/tccollidershape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccollidershape/circle)
- [case leftSide](/documentation/touchcontroller/tccollidershape/leftside)
- [case rect](/documentation/touchcontroller/tccollidershape/rect)
- [case rightSide](/documentation/touchcontroller/tccollidershape/rightside)

#### Creating a collider shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccollidershape/init(rawvalue:))

## Visuals

- [TCControlContents](/documentation/touchcontroller/tccontrolcontents)

### Creating control contents

- [convenience init(images: [TCControlImage])](/documentation/touchcontroller/tccontrolcontents/init(images:))

### Getting the images

- [var images: [TCControlImage]](/documentation/touchcontroller/tccontrolcontents/images)

### Accessing button contents

- [class func buttonContents(forSystemImageNamed: String, size: CGSize, shape: TCControlContents.ButtonShape, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/buttoncontents(forsystemimagenamed:size:shape:controller:))
- [TCControlContents.ButtonShape](/documentation/touchcontroller/tccontrolcontents/buttonshape)

#### Shapes

- [case circle](/documentation/touchcontroller/tccontrolcontents/buttonshape/circle)
- [case rect](/documentation/touchcontroller/tccontrolcontents/buttonshape/rect)

#### Creating a button shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/buttonshape/init(rawvalue:))

### Accessing directional pad contents

- [class func directionPadContents(label: TCControlLabel, size: CGSize, style: TCControlContents.DpadElementStyle, direction: TCControlContents.DpadDirection, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/directionpadcontents(label:size:style:direction:controller:))
- [TCControlContents.DpadDirection](/documentation/touchcontroller/tccontrolcontents/dpaddirection)

#### Directions

- [case down](/documentation/touchcontroller/tccontrolcontents/dpaddirection/down)
- [case left](/documentation/touchcontroller/tccontrolcontents/dpaddirection/left)
- [case right](/documentation/touchcontroller/tccontrolcontents/dpaddirection/right)
- [case up](/documentation/touchcontroller/tccontrolcontents/dpaddirection/up)

#### Creating a dpad direction

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/dpaddirection/init(rawvalue:))
- [TCControlContents.DpadElementStyle](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle)

#### Styles

- [case circle](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/circle)
- [case pentagon](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/pentagon)

#### Creating an element style

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/init(rawvalue:))

### Accessing switch contents

- [class func switchedOnContents(forSystemImageNamed: String, size: CGSize, shape: TCControlContents.ButtonShape, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/switchedoncontents(forsystemimagenamed:size:shape:controller:))

### Accessing throttle contents

- [class func throttleBackgroundContents(size: CGSize, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/throttlebackgroundcontents(size:controller:))
- [class func throttleIndicatorContents(size: CGSize, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/throttleindicatorcontents(size:controller:))

### Accessing thumbstick contents

- [class func thumbstickStickBackgroundContents(size: CGSize, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/thumbstickstickbackgroundcontents(size:controller:))
- [class func thumbstickStickContents(size: CGSize, controller: TCTouchController) -> TCControlContents](/documentation/touchcontroller/tccontrolcontents/thumbstickstickcontents(size:controller:))
- [TCControlImage](/documentation/touchcontroller/tccontrolimage)

### Creating a control image

- [convenience init?(cgImage: CGImage, size: CGSize, device: any MTLDevice)](/documentation/touchcontroller/tccontrolimage/init(cgimage:size:device:))
- [convenience init(texture: any MTLTexture, size: CGSize)](/documentation/touchcontroller/tccontrolimage/init(texture:size:))
- [init(texture: any MTLTexture, size: CGSize, highlight: (any MTLTexture)?, offset: CGPoint, tintColor: CGColor)](/documentation/touchcontroller/tccontrolimage/init(texture:size:highlight:offset:tintcolor:))
- [convenience init?(uiImage: UIImage, size: CGSize, device: any MTLDevice)](/documentation/touchcontroller/tccontrolimage/init(uiimage:size:device:))

### Inspecting the control image

- [var highlightTexture: (any MTLTexture)?](/documentation/touchcontroller/tccontrolimage/highlighttexture)
- [var offset: CGPoint](/documentation/touchcontroller/tccontrolimage/offset)
- [var size: CGSize](/documentation/touchcontroller/tccontrolimage/size)
- [var texture: any MTLTexture](/documentation/touchcontroller/tccontrolimage/texture)
- [var tintColor: CGColor](/documentation/touchcontroller/tccontrolimage/tintcolor)
- [TCControlLayout](/documentation/touchcontroller/tccontrollayout)

### Inspecting the control layout

- [var anchor: TCControlLayoutAnchor](/documentation/touchcontroller/tccontrollayout/anchor)
- [var anchorCoordinateSystem: TCControlLayoutAnchorCoordinateSystem](/documentation/touchcontroller/tccontrollayout/anchorcoordinatesystem)
- [var offset: CGPoint](/documentation/touchcontroller/tccontrollayout/offset)
- [var position: CGPoint](/documentation/touchcontroller/tccontrollayout/position)
- [var size: CGSize](/documentation/touchcontroller/tccontrollayout/size)
- [var zIndex: Int](/documentation/touchcontroller/tccontrollayout/zindex)

## System content

- [TCControlContents.ButtonShape](/documentation/touchcontroller/tccontrolcontents/buttonshape)

### Shapes

- [case circle](/documentation/touchcontroller/tccontrolcontents/buttonshape/circle)
- [case rect](/documentation/touchcontroller/tccontrolcontents/buttonshape/rect)

### Creating a button shape

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/buttonshape/init(rawvalue:))
- [TCControlContents.DpadDirection](/documentation/touchcontroller/tccontrolcontents/dpaddirection)

### Directions

- [case down](/documentation/touchcontroller/tccontrolcontents/dpaddirection/down)
- [case left](/documentation/touchcontroller/tccontrolcontents/dpaddirection/left)
- [case right](/documentation/touchcontroller/tccontrolcontents/dpaddirection/right)
- [case up](/documentation/touchcontroller/tccontrolcontents/dpaddirection/up)

### Creating a dpad direction

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/dpaddirection/init(rawvalue:))
- [TCControlContents.DpadElementStyle](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle)

### Styles

- [case circle](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/circle)
- [case pentagon](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/pentagon)

### Creating an element style

- [init?(rawValue: Int)](/documentation/touchcontroller/tccontrolcontents/dpadelementstyle/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
