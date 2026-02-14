# DockKit Documentation

Source: https://sosumi.ai/documentation/dockkit

---
title: DockKit
source: https://developer.apple.com/documentation/dockkit
timestamp: 2026-02-13T18:56:30.363Z
---

## Controlling the dock accessory

- [Controlling a DockKit accessory using your camera app](/documentation/dockkit/controlling-a-dockkit-accessory-using-your-camera-app)
- [DockAccessoryManager](/documentation/dockkit/dockaccessorymanager)

### Obtaining a manager

- [static let shared: DockAccessoryManager](/documentation/dockkit/dockaccessorymanager/shared)

### Controlling dock accessories

- [var accessoryStateChanges: DockAccessory.StateChanges](/documentation/dockkit/dockaccessorymanager/accessorystatechanges)

### Changing tracking behavior

- [var isSystemTrackingEnabled: Bool](/documentation/dockkit/dockaccessorymanager/issystemtrackingenabled)
- [func setSystemTrackingEnabled(Bool) async throws](/documentation/dockkit/dockaccessorymanager/setsystemtrackingenabled(_:))
- [DockAccessory](/documentation/dockkit/dockaccessory)

### Selecting and tracking

- [func selectSubject(at: CGPoint) async throws](/documentation/dockkit/dockaccessory/selectsubject(at:))
- [func track([AVMetadataObject], cameraInformation: DockAccessory.CameraInformation) async throws](/documentation/dockkit/dockaccessory/track(_:camerainformation:)-4yl9b)
- [func track([DockAccessory.Observation], cameraInformation: DockAccessory.CameraInformation) async throws](/documentation/dockkit/dockaccessory/track(_:camerainformation:)-44mwn)
- [DockAccessory.Observation](/documentation/dockkit/dockaccessory/observation)

#### Creating an observation

- [init(identifier: Int, type: DockAccessory.Observation.ObservationType, rect: CGRect, faceYawAngle: Measurement<UnitAngle>?)](/documentation/dockkit/dockaccessory/observation/init(identifier:type:rect:faceyawangle:))

#### Getting properties

- [let faceYawAngle: Measurement<UnitAngle>?](/documentation/dockkit/dockaccessory/observation/faceyawangle)
- [let rect: CGRect](/documentation/dockkit/dockaccessory/observation/rect)
- [let type: DockAccessory.Observation.ObservationType](/documentation/dockkit/dockaccessory/observation/type)
- [let identifier: Int](/documentation/dockkit/dockaccessory/observation/identifier)

#### Defining types

- [DockAccessory.Observation.ObservationType](/documentation/dockkit/dockaccessory/observation/observationtype)

##### Enumeration Cases

- [case humanBody](/documentation/dockkit/dockaccessory/observation/observationtype/humanbody)
- [case humanFace](/documentation/dockkit/dockaccessory/observation/observationtype/humanface)
- [case object](/documentation/dockkit/dockaccessory/observation/observationtype/object)
- [DockAccessory.CameraInformation](/documentation/dockkit/dockaccessory/camerainformation)

#### Creating the object

- [init(captureDevice: AVCaptureDevice.DeviceType, cameraPosition: AVCaptureDevice.Position, orientation: DockAccessory.CameraOrientation, cameraIntrinsics: matrix_float3x3?, referenceDimensions: CGSize?)](/documentation/dockkit/dockaccessory/camerainformation/init(capturedevice:cameraposition:orientation:cameraintrinsics:referencedimensions:))

#### Getting camera information

- [let cameraPosition: AVCaptureDevice.Position](/documentation/dockkit/dockaccessory/camerainformation/cameraposition)
- [let cameraIntrinsics: matrix_float3x3?](/documentation/dockkit/dockaccessory/camerainformation/cameraintrinsics)
- [let captureDevice: AVCaptureDevice.DeviceType](/documentation/dockkit/dockaccessory/camerainformation/capturedevice)
- [let orientation: DockAccessory.CameraOrientation](/documentation/dockkit/dockaccessory/camerainformation/orientation)
- [let referenceDimensions: CGSize?](/documentation/dockkit/dockaccessory/camerainformation/referencedimensions)
- [DockAccessory.CameraOrientation](/documentation/dockkit/dockaccessory/cameraorientation)

#### Getting camera orientation

- [case corrected](/documentation/dockkit/dockaccessory/cameraorientation/corrected)
- [case faceUp](/documentation/dockkit/dockaccessory/cameraorientation/faceup)
- [case faceDown](/documentation/dockkit/dockaccessory/cameraorientation/facedown)
- [case landscapeLeft](/documentation/dockkit/dockaccessory/cameraorientation/landscapeleft)
- [case landscapeRight](/documentation/dockkit/dockaccessory/cameraorientation/landscaperight)
- [case portrait](/documentation/dockkit/dockaccessory/cameraorientation/portrait)
- [case portraitUpsideDown](/documentation/dockkit/dockaccessory/cameraorientation/portraitupsidedown)
- [case unknown](/documentation/dockkit/dockaccessory/cameraorientation/unknown)

### Performing animation

- [func animate(motion: DockAccessory.Animation) async throws -> Progress](/documentation/dockkit/dockaccessory/animate(motion:))
- [func setRegionOfInterest(CGRect) async throws](/documentation/dockkit/dockaccessory/setregionofinterest(_:))
- [var regionOfInterest: CGRect](/documentation/dockkit/dockaccessory/regionofinterest)
- [DockAccessory.Animation](/documentation/dockkit/dockaccessory/animation)

#### Enumeration Cases

- [case kapow](/documentation/dockkit/dockaccessory/animation/kapow)
- [case no](/documentation/dockkit/dockaccessory/animation/no)
- [case wakeup](/documentation/dockkit/dockaccessory/animation/wakeup)
- [case yes](/documentation/dockkit/dockaccessory/animation/yes)

### Setting position and limits

- [func setLimits(DockAccessory.Limits) throws](/documentation/dockkit/dockaccessory/setlimits(_:))
- [func setOrientation(Vector3D, duration: Duration, relative: Bool) throws -> Progress](/documentation/dockkit/dockaccessory/setorientation(_:duration:relative:)-2epe2)
- [func setOrientation(Rotation3D, duration: Duration, relative: Bool) throws -> Progress](/documentation/dockkit/dockaccessory/setorientation(_:duration:relative:)-6b0fl)
- [func setAngularVelocity(Vector3D) async throws](/documentation/dockkit/dockaccessory/setangularvelocity(_:))

### Setting framing mode

- [func setFramingMode(DockAccessory.FramingMode) async throws](/documentation/dockkit/dockaccessory/setframingmode(_:))
- [var framingMode: DockAccessory.FramingMode](/documentation/dockkit/dockaccessory/framingmode-swift.property)
- [DockAccessory.FramingMode](/documentation/dockkit/dockaccessory/framingmode-swift.enum)

#### Defining the framing mode

- [case automatic](/documentation/dockkit/dockaccessory/framingmode-swift.enum/automatic)
- [case center](/documentation/dockkit/dockaccessory/framingmode-swift.enum/center)
- [case left](/documentation/dockkit/dockaccessory/framingmode-swift.enum/left)
- [case right](/documentation/dockkit/dockaccessory/framingmode-swift.enum/right)

### Getting position and limits

- [var motionStates: DockAccessory.MotionStates](/documentation/dockkit/dockaccessory/motionstates-swift.property)
- [var limits: DockAccessory.Limits](/documentation/dockkit/dockaccessory/limits-swift.property)
- [DockAccessory.MotionState](/documentation/dockkit/dockaccessory/motionstate)

#### Getting properties

- [let angularPositions: Vector3D](/documentation/dockkit/dockaccessory/motionstate/angularpositions)
- [let angularVelocities: Vector3D](/documentation/dockkit/dockaccessory/motionstate/angularvelocities)
- [let timestamp: TimeInterval](/documentation/dockkit/dockaccessory/motionstate/timestamp)
- [let error: (any Error)?](/documentation/dockkit/dockaccessory/motionstate/error)
- [DockAccessory.MotionStates](/documentation/dockkit/dockaccessory/motionstates-swift.struct)

#### Iterating over motion states

- [DockAccessory.MotionStates.Iterator](/documentation/dockkit/dockaccessory/motionstates-swift.struct/iterator)

##### Instance Methods

- [func next() async -> DockAccessory.MotionState?](/documentation/dockkit/dockaccessory/motionstates-swift.struct/iterator/next())
- [func makeAsyncIterator() -> DockAccessory.MotionStates.Iterator](/documentation/dockkit/dockaccessory/motionstates-swift.struct/makeasynciterator())
- [DockAccessory.MotionStates.Element](/documentation/dockkit/dockaccessory/motionstates-swift.struct/element)
- [DockAccessory.Limits](/documentation/dockkit/dockaccessory/limits-swift.struct)

#### Creating limits

- [init(yaw: DockAccessory.Limits.Limit?, pitch: DockAccessory.Limits.Limit?, roll: DockAccessory.Limits.Limit?)](/documentation/dockkit/dockaccessory/limits-swift.struct/init(yaw:pitch:roll:))

#### Specifying limits

- [DockAccessory.Limits.Limit](/documentation/dockkit/dockaccessory/limits-swift.struct/limit)

##### Limiting speed and position

- [let maximumSpeed: Double](/documentation/dockkit/dockaccessory/limits-swift.struct/limit/maximumspeed)
- [let positionRange: Range<Double>](/documentation/dockkit/dockaccessory/limits-swift.struct/limit/positionrange)

##### Initializers

- [init(positionRange: Range<Double>, maximumSpeed: Double) throws](/documentation/dockkit/dockaccessory/limits-swift.struct/limit/init(positionrange:maximumspeed:))

#### Getting properties

- [let pitch: DockAccessory.Limits.Limit?](/documentation/dockkit/dockaccessory/limits-swift.struct/pitch)
- [let roll: DockAccessory.Limits.Limit?](/documentation/dockkit/dockaccessory/limits-swift.struct/roll)
- [let yaw: DockAccessory.Limits.Limit?](/documentation/dockkit/dockaccessory/limits-swift.struct/yaw)

### Getting accessory information

- [var firmwareVersion: String?](/documentation/dockkit/dockaccessory/firmwareversion)
- [var hardwareModel: String?](/documentation/dockkit/dockaccessory/hardwaremodel)
- [let identifier: DockAccessory.Identifier](/documentation/dockkit/dockaccessory/identifier-swift.property)
- [DockAccessory.Identifier](/documentation/dockkit/dockaccessory/identifier-swift.struct)

#### Getting properties

- [let name: String](/documentation/dockkit/dockaccessory/identifier-swift.struct/name)
- [let category: DockAccessory.Category](/documentation/dockkit/dockaccessory/identifier-swift.struct/category)
- [let uuid: UUID](/documentation/dockkit/dockaccessory/identifier-swift.struct/uuid)
- [var debugDescription: String](/documentation/dockkit/dockaccessory/identifier-swift.struct/debugdescription)
- [DockAccessory.Category](/documentation/dockkit/dockaccessory/category)

#### Getting properties

- [case trackingStand](/documentation/dockkit/dockaccessory/category/trackingstand)
- [var debugDescription: String](/documentation/dockkit/dockaccessory/category/debugdescription)
- [DockAccessory.State](/documentation/dockkit/dockaccessory/state)

#### Getting properties

- [case docked](/documentation/dockkit/dockaccessory/state/docked)
- [case undocked](/documentation/dockkit/dockaccessory/state/undocked)
- [var debugDescription: String](/documentation/dockkit/dockaccessory/state/debugdescription)
- [DockAccessory.StateChange](/documentation/dockkit/dockaccessory/statechange)

#### Getting properties

- [let accessory: DockAccessory?](/documentation/dockkit/dockaccessory/statechange/accessory)
- [let state: DockAccessory.State](/documentation/dockkit/dockaccessory/statechange/state)

#### Instance Properties

- [let trackingButtonEnabled: Bool](/documentation/dockkit/dockaccessory/statechange/trackingbuttonenabled)
- [DockAccessory.StateChanges](/documentation/dockkit/dockaccessory/statechanges)

#### Iterating over state changes

- [DockAccessory.StateChanges.Iterator](/documentation/dockkit/dockaccessory/statechanges/iterator)

##### Iterating over state changes

- [func next() async -> DockAccessory.StateChange?](/documentation/dockkit/dockaccessory/statechanges/iterator/next())
- [func makeAsyncIterator() -> DockAccessory.StateChanges.Iterator](/documentation/dockkit/dockaccessory/statechanges/makeasynciterator())
- [DockAccessory.StateChanges.Element](/documentation/dockkit/dockaccessory/statechanges/element)

### Inspecting the object

- [func hash(into: inout Hasher)](/documentation/dockkit/dockaccessory/hash(into:))
- [var debugDescription: String](/documentation/dockkit/dockaccessory/debugdescription)

### Structures

- [DockAccessory.AccessoryEvents](/documentation/dockkit/dockaccessory/accessoryevents-swift.struct)

#### Structures

- [DockAccessory.AccessoryEvents.Iterator](/documentation/dockkit/dockaccessory/accessoryevents-swift.struct/iterator)

##### Instance Methods

- [func next() async -> DockAccessory.AccessoryEvent?](/documentation/dockkit/dockaccessory/accessoryevents-swift.struct/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> DockAccessory.AccessoryEvents.Iterator](/documentation/dockkit/dockaccessory/accessoryevents-swift.struct/makeasynciterator())

#### Type Aliases

- [DockAccessory.AccessoryEvents.Element](/documentation/dockkit/dockaccessory/accessoryevents-swift.struct/element)
- [DockAccessory.BatteryState](/documentation/dockkit/dockaccessory/batterystate)

#### Instance Properties

- [let batteryLevel: Double](/documentation/dockkit/dockaccessory/batterystate/batterylevel)
- [let chargeState: DockAccessory.BatteryChargeState](/documentation/dockkit/dockaccessory/batterystate/chargestate)
- [let lowBattery: Bool](/documentation/dockkit/dockaccessory/batterystate/lowbattery)
- [let name: String](/documentation/dockkit/dockaccessory/batterystate/name)
- [DockAccessory.BatteryStates](/documentation/dockkit/dockaccessory/batterystates-swift.struct)

#### Structures

- [DockAccessory.BatteryStates.Iterator](/documentation/dockkit/dockaccessory/batterystates-swift.struct/iterator)

##### Instance Methods

- [func next() async -> DockAccessory.BatteryState?](/documentation/dockkit/dockaccessory/batterystates-swift.struct/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> DockAccessory.BatteryStates.Iterator](/documentation/dockkit/dockaccessory/batterystates-swift.struct/makeasynciterator())

#### Type Aliases

- [DockAccessory.BatteryStates.Element](/documentation/dockkit/dockaccessory/batterystates-swift.struct/element)
- [DockAccessory.TrackedObject](/documentation/dockkit/dockaccessory/trackedobject)

#### Instance Properties

- [var identifier: UUID](/documentation/dockkit/dockaccessory/trackedobject/identifier)
- [var rect: CGRect](/documentation/dockkit/dockaccessory/trackedobject/rect)
- [var saliencyRank: Int?](/documentation/dockkit/dockaccessory/trackedobject/saliencyrank)
- [DockAccessory.TrackedPerson](/documentation/dockkit/dockaccessory/trackedperson)

#### Instance Properties

- [var identifier: UUID](/documentation/dockkit/dockaccessory/trackedperson/identifier)
- [var lookingAtCameraConfidence: Double?](/documentation/dockkit/dockaccessory/trackedperson/lookingatcameraconfidence)
- [var rect: CGRect](/documentation/dockkit/dockaccessory/trackedperson/rect)
- [var saliencyRank: Int?](/documentation/dockkit/dockaccessory/trackedperson/saliencyrank)
- [var speakingConfidence: Double?](/documentation/dockkit/dockaccessory/trackedperson/speakingconfidence)
- [DockAccessory.TrackingState](/documentation/dockkit/dockaccessory/trackingstate)

#### Instance Properties

- [var description: String](/documentation/dockkit/dockaccessory/trackingstate/description)
- [var time: Date](/documentation/dockkit/dockaccessory/trackingstate/time)
- [var trackedSubjects: [DockAccessory.TrackedSubjectType]](/documentation/dockkit/dockaccessory/trackingstate/trackedsubjects)
- [DockAccessory.TrackingStates](/documentation/dockkit/dockaccessory/trackingstates-swift.struct)

#### Structures

- [DockAccessory.TrackingStates.Iterator](/documentation/dockkit/dockaccessory/trackingstates-swift.struct/iterator)

##### Instance Methods

- [func next() async -> DockAccessory.TrackingState?](/documentation/dockkit/dockaccessory/trackingstates-swift.struct/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> DockAccessory.TrackingStates.Iterator](/documentation/dockkit/dockaccessory/trackingstates-swift.struct/makeasynciterator())

#### Type Aliases

- [DockAccessory.TrackingStates.Element](/documentation/dockkit/dockaccessory/trackingstates-swift.struct/element)

### Instance Properties

- [var accessoryEvents: DockAccessory.AccessoryEvents](/documentation/dockkit/dockaccessory/accessoryevents-swift.property)
- [var batteryStates: DockAccessory.BatteryStates](/documentation/dockkit/dockaccessory/batterystates-swift.property)
- [var trackingStates: DockAccessory.TrackingStates](/documentation/dockkit/dockaccessory/trackingstates-swift.property)

### Instance Methods

- [func selectSubjects([UUID]) async throws](/documentation/dockkit/dockaccessory/selectsubjects(_:))
- [func setOrientation(Rotation3D, duration: Duration, relative: Bool) async throws -> Progress](/documentation/dockkit/dockaccessory/setorientation(_:duration:relative:)-6h2ah)
- [func setOrientation(Vector3D, duration: Duration, relative: Bool) async throws -> Progress](/documentation/dockkit/dockaccessory/setorientation(_:duration:relative:)-84z7i)
- [func track([DockAccessory.Observation], cameraInformation: DockAccessory.CameraInformation, image: CVPixelBuffer) async throws](/documentation/dockkit/dockaccessory/track(_:camerainformation:image:)-3uuza)
- [func track([AVMetadataObject], cameraInformation: DockAccessory.CameraInformation, image: CVPixelBuffer) async throws](/documentation/dockkit/dockaccessory/track(_:camerainformation:image:)-82m61)

### Enumerations

- [DockAccessory.AccessoryEvent](/documentation/dockkit/dockaccessory/accessoryevent)

#### Enumeration Cases

- [case button(id: Int, pressed: Bool)](/documentation/dockkit/dockaccessory/accessoryevent/button(id:pressed:))
- [case cameraFlip](/documentation/dockkit/dockaccessory/accessoryevent/cameraflip)
- [case cameraShutter](/documentation/dockkit/dockaccessory/accessoryevent/camerashutter)
- [case cameraZoom(factor: Double)](/documentation/dockkit/dockaccessory/accessoryevent/camerazoom(factor:))
- [DockAccessory.BatteryChargeState](/documentation/dockkit/dockaccessory/batterychargestate)

#### Enumeration Cases

- [case charging](/documentation/dockkit/dockaccessory/batterychargestate/charging)
- [case notChargeable](/documentation/dockkit/dockaccessory/batterychargestate/notchargeable)
- [case notCharging](/documentation/dockkit/dockaccessory/batterychargestate/notcharging)
- [DockAccessory.TrackedSubjectType](/documentation/dockkit/dockaccessory/trackedsubjecttype)

#### Enumeration Cases

- [case object(DockAccessory.TrackedObject)](/documentation/dockkit/dockaccessory/trackedsubjecttype/object(_:))
- [case person(DockAccessory.TrackedPerson)](/documentation/dockkit/dockaccessory/trackedsubjecttype/person(_:))
- [DockKitError](/documentation/dockkit/dockkiterror)

### Getting errors

- [case invalidParameter](/documentation/dockkit/dockkiterror/invalidparameter)
- [case notConnected](/documentation/dockkit/dockkiterror/notconnected)
- [case notSupported](/documentation/dockkit/dockkiterror/notsupported)
- [case notSupportedByDevice](/documentation/dockkit/dockkiterror/notsupportedbydevice)

### Enumeration Cases

- [case cameraTCCMissing](/documentation/dockkit/dockkiterror/cameratccmissing)
- [case frameRateTooHigh](/documentation/dockkit/dockkiterror/frameratetoohigh)
- [case frameRateTooLow](/documentation/dockkit/dockkiterror/frameratetoolow)
- [case noSubjectFound](/documentation/dockkit/dockkiterror/nosubjectfound)

## Customizing tracking behavior

- [Modify rotation and positioning programmatically](/documentation/dockkit/modify-rotation-and-positioning-behavior-programmatically)
- [Track custom objects in a frame](/documentation/dockkit/track-custom-objects-in-a-frame)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
