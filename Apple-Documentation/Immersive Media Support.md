# Immersive Media Support Documentation

Source: https://sosumi.ai/documentation/immersivemediasupport

---
title: Immersive Media Support
source: https://developer.apple.com/documentation/immersivemediasupport
timestamp: 2026-02-13T18:58:10.866Z
---

## Essentials

- [Authoring Apple Immersive Video](/documentation/immersivemediasupport/authoring-apple-immersive-video)

## Camera metadata

- [VenueDescriptor](/documentation/immersivemediasupport/venuedescriptor)

### Creating a venue descriptor

- [init(device: (any MTLDevice)?)](/documentation/immersivemediasupport/venuedescriptor/init(device:))
- [convenience init(aimeURL: URL, device: (any MTLDevice)?) async throws](/documentation/immersivemediasupport/venuedescriptor/init(aimeurl:device:))

### Configuring cameras

- [var cameras: [ImmersiveCamera]](/documentation/immersivemediasupport/venuedescriptor/cameras)
- [func addCamera(ImmersiveCamera) throws](/documentation/immersivemediasupport/venuedescriptor/addcamera(_:))
- [func removeCamera(id: String) throws](/documentation/immersivemediasupport/venuedescriptor/removecamera(id:))
- [func cameraViewModel(for: String) -> ImmersiveCameraViewModel?](/documentation/immersivemediasupport/venuedescriptor/cameraviewmodel(for:))

### Saving a venue descriptor data

- [func save(to: URL) throws](/documentation/immersivemediasupport/venuedescriptor/save(to:))
- [var aimeData: Data?](/documentation/immersivemediasupport/venuedescriptor/aimedata)

### Initializers

- [init(aimeData: Data, device: (any MTLDevice)?) async throws](/documentation/immersivemediasupport/venuedescriptor/init(aimedata:device:))
- [ImmersiveCamera](/documentation/immersivemediasupport/immersivecamera)

### Initializers

- [init(id: String, calibration: ImmersiveCameraCalibration, type: ImmersiveCamera.CameraType, presentationFrameRate: Int, pose: Pose3DFloat)](/documentation/immersivemediasupport/immersivecamera/init(id:calibration:type:presentationframerate:pose:))

### Instance Properties

- [var calibration: ImmersiveCameraCalibration](/documentation/immersivemediasupport/immersivecamera/calibration)
- [var id: String](/documentation/immersivemediasupport/immersivecamera/id)
- [var pose: Pose3DFloat](/documentation/immersivemediasupport/immersivecamera/pose)
- [var presentationFrameRate: Int](/documentation/immersivemediasupport/immersivecamera/presentationframerate)
- [var type: ImmersiveCamera.CameraType](/documentation/immersivemediasupport/immersivecamera/type)

### Type Properties

- [static let defaultPresentationFrameRate: Int](/documentation/immersivemediasupport/immersivecamera/defaultpresentationframerate)

### Enumerations

- [ImmersiveCamera.CameraType](/documentation/immersivemediasupport/immersivecamera/cameratype)

#### Enumeration Cases

- [case stereoCamera](/documentation/immersivemediasupport/immersivecamera/cameratype/stereocamera)
- [ImmersiveCameraCalibration](/documentation/immersivemediasupport/immersivecameracalibration)

### Structures

- [ImmersiveCameraCalibration.CameraOrigin](/documentation/immersivemediasupport/immersivecameracalibration/cameraorigin)

#### Initializers

- [init(left: Point3DFloat, right: Point3DFloat)](/documentation/immersivemediasupport/immersivecameracalibration/cameraorigin/init(left:right:))

#### Type Properties

- [static let zero: ImmersiveCameraCalibration.CameraOrigin](/documentation/immersivemediasupport/immersivecameracalibration/cameraorigin/zero)
- [ImmersiveCameraCalibration.CameraTextureMapping](/documentation/immersivemediasupport/immersivecameracalibration/cameratexturemapping)

#### Initializers

- [init(left: matrix_float3x3, right: matrix_float3x3)](/documentation/immersivemediasupport/immersivecameracalibration/cameratexturemapping/init(left:right:))

#### Type Properties

- [static let identity: ImmersiveCameraCalibration.CameraTextureMapping](/documentation/immersivemediasupport/immersivecameracalibration/cameratexturemapping/identity)

### Enumerations

- [ImmersiveCameraCalibration.CalibrationType](/documentation/immersivemediasupport/immersivecameracalibration/calibrationtype)

#### Enumeration Cases

- [case immersiveCameraLensDefinition(ImmersiveCameraLensDefinition)](/documentation/immersivemediasupport/immersivecameracalibration/calibrationtype/immersivecameralensdefinition(_:))
- [case usdzMesh(ImmersiveCameraMeshCalibration)](/documentation/immersivemediasupport/immersivecameracalibration/calibrationtype/usdzmesh(_:))

### Initializers

- [init(name: String, type: ImmersiveCameraCalibration.CalibrationType, mask: ImmersiveCameraMask?, positionable: Bool, origin: ImmersiveCameraCalibration.CameraOrigin, textureMapping: ImmersiveCameraCalibration.CameraTextureMapping, environmentFilename: String?)](/documentation/immersivemediasupport/immersivecameracalibration/init(name:type:mask:positionable:origin:texturemapping:environmentfilename:))

### Instance Properties

- [var environmentFilename: String?](/documentation/immersivemediasupport/immersivecameracalibration/environmentfilename)
- [var mask: ImmersiveCameraMask?](/documentation/immersivemediasupport/immersivecameracalibration/mask)
- [var name: String](/documentation/immersivemediasupport/immersivecameracalibration/name)
- [var origin: ImmersiveCameraCalibration.CameraOrigin](/documentation/immersivemediasupport/immersivecameracalibration/origin)
- [var positionable: Bool](/documentation/immersivemediasupport/immersivecameracalibration/positionable)
- [var textureMapping: ImmersiveCameraCalibration.CameraTextureMapping](/documentation/immersivemediasupport/immersivecameracalibration/texturemapping)
- [var type: ImmersiveCameraCalibration.CalibrationType](/documentation/immersivemediasupport/immersivecameracalibration/type)
- [ImmersiveCameraMask](/documentation/immersivemediasupport/immersivecameramask)

### Enumeration Cases

- [case dynamic(ImmersiveDynamicMask)](/documentation/immersivemediasupport/immersivecameramask/dynamic(_:))
- [case image(ImmersiveImageMask)](/documentation/immersivemediasupport/immersivecameramask/image(_:))
- [ImmersiveDynamicMask](/documentation/immersivemediasupport/immersivedynamicmask)

### Instance Properties

- [var controlPointInterpolation: ImmersiveDynamicMask.ControlPointInterpolation](/documentation/immersivemediasupport/immersivedynamicmask/controlpointinterpolation-swift.property)
- [var edgeTreatment: ImmersiveDynamicMask.EdgeTreatment](/documentation/immersivemediasupport/immersivedynamicmask/edgetreatment-swift.property)
- [var edgeWidthInDegrees: Float](/documentation/immersivemediasupport/immersivedynamicmask/edgewidthindegrees)
- [var leftControlPoints: [Point3DFloat]](/documentation/immersivemediasupport/immersivedynamicmask/leftcontrolpoints)
- [var name: String](/documentation/immersivemediasupport/immersivedynamicmask/name)
- [var rightControlPoints: [Point3DFloat]](/documentation/immersivemediasupport/immersivedynamicmask/rightcontrolpoints)
- [var stereoRelation: ImmersiveDynamicMask.StereoRelation](/documentation/immersivemediasupport/immersivedynamicmask/stereorelation-swift.property)

### Enumerations

- [ImmersiveDynamicMask.ControlPointInterpolation](/documentation/immersivemediasupport/immersivedynamicmask/controlpointinterpolation-swift.enum)

#### Enumeration Cases

- [case cubicHermite](/documentation/immersivemediasupport/immersivedynamicmask/controlpointinterpolation-swift.enum/cubichermite)
- [case linear](/documentation/immersivemediasupport/immersivedynamicmask/controlpointinterpolation-swift.enum/linear)
- [ImmersiveDynamicMask.EdgeTreatment](/documentation/immersivemediasupport/immersivedynamicmask/edgetreatment-swift.enum)

#### Enumeration Cases

- [case easeInOut](/documentation/immersivemediasupport/immersivedynamicmask/edgetreatment-swift.enum/easeinout)
- [case linear](/documentation/immersivemediasupport/immersivedynamicmask/edgetreatment-swift.enum/linear)
- [ImmersiveDynamicMask.StereoRelation](/documentation/immersivemediasupport/immersivedynamicmask/stereorelation-swift.enum)

#### Enumeration Cases

- [case identical](/documentation/immersivemediasupport/immersivedynamicmask/stereorelation-swift.enum/identical)
- [case mirror](/documentation/immersivemediasupport/immersivedynamicmask/stereorelation-swift.enum/mirror)
- [case separate](/documentation/immersivemediasupport/immersivedynamicmask/stereorelation-swift.enum/separate)

### Initializers

- [init(name: String, stereoRelation: ImmersiveDynamicMask.StereoRelation, edgeTreatment: ImmersiveDynamicMask.EdgeTreatment, controlPointInterpolation: ImmersiveDynamicMask.ControlPointInterpolation, leftControlPoints: [Point3DFloat], rightControlPoints: [Point3DFloat], edgeWidthInDegrees: Float)](/documentation/immersivemediasupport/immersivedynamicmask/init(name:stereorelation:edgetreatment:controlpointinterpolation:leftcontrolpoints:rightcontrolpoints:edgewidthindegrees:))

## Presentation commands

- [PresentationCommand](/documentation/immersivemediasupport/presentationcommand)

### Instance Properties

- [var duration: CMTime](/documentation/immersivemediasupport/presentationcommand/duration)
- [var id: Int](/documentation/immersivemediasupport/presentationcommand/id)
- [var offset: CMTime?](/documentation/immersivemediasupport/presentationcommand/offset)
- [var time: CMTime](/documentation/immersivemediasupport/presentationcommand/time)

### Enumeration Cases

- [case fade(FadeCommand)](/documentation/immersivemediasupport/presentationcommand/fade(_:))
- [case fadeEnvironment(FadeEnvironmentCommand)](/documentation/immersivemediasupport/presentationcommand/fadeenvironment(_:))
- [case setCamera(SetCameraCommand)](/documentation/immersivemediasupport/presentationcommand/setcamera(_:))
- [case shotFlop(ShotFlopCommand)](/documentation/immersivemediasupport/presentationcommand/shotflop(_:))
- [FadeCommand](/documentation/immersivemediasupport/fadecommand)

### Initializers

- [init(from: any Decoder) throws](/documentation/immersivemediasupport/fadecommand/init(from:))
- [init(id: Int, time: CMTime, duration: CMTime, direction: FadeCommand.FadeDirection, color: simd_float3, offset: CMTime?)](/documentation/immersivemediasupport/fadecommand/init(id:time:duration:direction:color:offset:))

### Instance Properties

- [var color: simd_float3](/documentation/immersivemediasupport/fadecommand/color)
- [var direction: FadeCommand.FadeDirection](/documentation/immersivemediasupport/fadecommand/direction)
- [var duration: CMTime](/documentation/immersivemediasupport/fadecommand/duration)
- [var id: Int](/documentation/immersivemediasupport/fadecommand/id)
- [var offset: CMTime?](/documentation/immersivemediasupport/fadecommand/offset)
- [var time: CMTime](/documentation/immersivemediasupport/fadecommand/time)

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/immersivemediasupport/fadecommand/encode(to:))

### Enumerations

- [FadeCommand.FadeDirection](/documentation/immersivemediasupport/fadecommand/fadedirection)

#### Enumeration Cases

- [case `in`](/documentation/immersivemediasupport/fadecommand/fadedirection/in)
- [case out](/documentation/immersivemediasupport/fadecommand/fadedirection/out)
- [FadeEnvironmentCommand](/documentation/immersivemediasupport/fadeenvironmentcommand)

### Initializers

- [init(from: any Decoder) throws](/documentation/immersivemediasupport/fadeenvironmentcommand/init(from:))
- [init(id: Int, time: CMTime, duration: CMTime, direction: FadeEnvironmentCommand.FadeDirection, opacity: Float, offset: CMTime?)](/documentation/immersivemediasupport/fadeenvironmentcommand/init(id:time:duration:direction:opacity:offset:))

### Instance Properties

- [var direction: FadeEnvironmentCommand.FadeDirection](/documentation/immersivemediasupport/fadeenvironmentcommand/direction)
- [var duration: CMTime](/documentation/immersivemediasupport/fadeenvironmentcommand/duration)
- [var id: Int](/documentation/immersivemediasupport/fadeenvironmentcommand/id)
- [var offset: CMTime?](/documentation/immersivemediasupport/fadeenvironmentcommand/offset)
- [var opacity: Float](/documentation/immersivemediasupport/fadeenvironmentcommand/opacity)
- [var time: CMTime](/documentation/immersivemediasupport/fadeenvironmentcommand/time)

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/immersivemediasupport/fadeenvironmentcommand/encode(to:))

### Enumerations

- [FadeEnvironmentCommand.FadeDirection](/documentation/immersivemediasupport/fadeenvironmentcommand/fadedirection)

#### Enumeration Cases

- [case `in`](/documentation/immersivemediasupport/fadeenvironmentcommand/fadedirection/in)
- [case out](/documentation/immersivemediasupport/fadeenvironmentcommand/fadedirection/out)
- [SetCameraCommand](/documentation/immersivemediasupport/setcameracommand)

### Initializers

- [init(from: any Decoder) throws](/documentation/immersivemediasupport/setcameracommand/init(from:))
- [init(id: Int, time: CMTime, cameraID: String)](/documentation/immersivemediasupport/setcameracommand/init(id:time:cameraid:))

### Instance Properties

- [var cameraID: String](/documentation/immersivemediasupport/setcameracommand/cameraid)
- [var duration: CMTime](/documentation/immersivemediasupport/setcameracommand/duration)
- [var id: Int](/documentation/immersivemediasupport/setcameracommand/id)
- [var offset: CMTime?](/documentation/immersivemediasupport/setcameracommand/offset)
- [var time: CMTime](/documentation/immersivemediasupport/setcameracommand/time)

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/immersivemediasupport/setcameracommand/encode(to:))
- [ShotFlopCommand](/documentation/immersivemediasupport/shotflopcommand)

### Initializers

- [init(from: any Decoder) throws](/documentation/immersivemediasupport/shotflopcommand/init(from:))
- [init(id: Int, time: CMTime, duration: CMTime, offset: CMTime?)](/documentation/immersivemediasupport/shotflopcommand/init(id:time:duration:offset:))

### Instance Properties

- [var duration: CMTime](/documentation/immersivemediasupport/shotflopcommand/duration)
- [var id: Int](/documentation/immersivemediasupport/shotflopcommand/id)
- [var offset: CMTime?](/documentation/immersivemediasupport/shotflopcommand/offset)
- [var time: CMTime](/documentation/immersivemediasupport/shotflopcommand/time)

### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/immersivemediasupport/shotflopcommand/encode(to:))
- [PresentationDescriptor](/documentation/immersivemediasupport/presentationdescriptor)

### Initializers

- [init(commands: [PresentationCommand])](/documentation/immersivemediasupport/presentationdescriptor/init(commands:))
- [init(duration: CMTime?, commands: [PresentationCommand])](/documentation/immersivemediasupport/presentationdescriptor/init(duration:commands:))

### Instance Properties

- [var commands: [PresentationCommand]](/documentation/immersivemediasupport/presentationdescriptor/commands)
- [var duration: CMTime?](/documentation/immersivemediasupport/presentationdescriptor/duration)
- [PresentationDescriptorReader](/documentation/immersivemediasupport/presentationdescriptorreader)

### Initializers

- [init(presentationDescriptor: PresentationDescriptor, isSideloaded: Bool)](/documentation/immersivemediasupport/presentationdescriptorreader/init(presentationdescriptor:issideloaded:))

### Instance Properties

- [var cameraID: String?](/documentation/immersivemediasupport/presentationdescriptorreader/cameraid)
- [var colorFade: simd_float3](/documentation/immersivemediasupport/presentationdescriptorreader/colorfade)
- [var colorFadeOpacity: Float](/documentation/immersivemediasupport/presentationdescriptorreader/colorfadeopacity)
- [var environmentFadeOpacity: Float](/documentation/immersivemediasupport/presentationdescriptorreader/environmentfadeopacity)
- [var isShotFlopped: Bool](/documentation/immersivemediasupport/presentationdescriptorreader/isshotflopped)
- [var isSideloaded: Bool](/documentation/immersivemediasupport/presentationdescriptorreader/issideloaded)
- [var presentationCommands: [PresentationCommand]](/documentation/immersivemediasupport/presentationdescriptorreader/presentationcommands)
- [var presentationDescriptor: PresentationDescriptor](/documentation/immersivemediasupport/presentationdescriptorreader/presentationdescriptor)

### Instance Methods

- [func outputPresentationCommands(for: CMTime) -> [PresentationCommand]?](/documentation/immersivemediasupport/presentationdescriptorreader/outputpresentationcommands(for:))
- [func processPresentationCommands(for: CMTime)](/documentation/immersivemediasupport/presentationdescriptorreader/processpresentationcommands(for:))

## Parametric immersive support

- [ParametricImmersiveAssetInfo](/documentation/immersivemediasupport/parametricimmersiveassetinfo)

### Structures

- [ParametricImmersiveAssetInfo.Error](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error)

#### Instance Properties

- [var errorDescription: String?](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errordescription)
- [let errorType: ParametricImmersiveAssetInfo.Error.ErrorType](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errortype-swift.property)

#### Enumerations

- [ParametricImmersiveAssetInfo.Error.ErrorType](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errortype-swift.enum)

##### Enumeration Cases

- [case unsupportedAsset](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errortype-swift.enum/unsupportedasset)
- [case isAlreadyConverted](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errortype-swift.enum/isalreadyconverted)
- [case unconvertibleAsset](/documentation/immersivemediasupport/parametricimmersiveassetinfo/error/errortype-swift.enum/unconvertibleasset)

### Initializers

- [init(asset: AVURLAsset, computeFormatDescription: Bool) async throws](/documentation/immersivemediasupport/parametricimmersiveassetinfo/init(asset:computeformatdescription:))

### Instance Properties

- [var requiredFormatDescription: CMFormatDescription?](/documentation/immersivemediasupport/parametricimmersiveassetinfo/requiredformatdescription)
- [var conversionResult: Result<CMFormatDescription, ParametricImmersiveAssetInfo.Error>?](/documentation/immersivemediasupport/parametricimmersiveassetinfo/conversionresult)
- [var isAssetConvertible: Bool](/documentation/immersivemediasupport/parametricimmersiveassetinfo/isassetconvertible)

### Type Methods

- [class func isParametricImmersive(asset: AVURLAsset) async -> Bool](/documentation/immersivemediasupport/parametricimmersiveassetinfo/isparametricimmersive(asset:))

## Immersive video rendering support

- [ImmersiveCameraViewModel](/documentation/immersivemediasupport/immersivecameraviewmodel)

### Instance Properties

- [var cameraID: String](/documentation/immersivemediasupport/immersivecameraviewmodel/cameraid)
- [var environmentBackdrop: MDLAsset?](/documentation/immersivemediasupport/immersivecameraviewmodel/environmentbackdrop)
- [var leftEye: MDLMesh](/documentation/immersivemediasupport/immersivecameraviewmodel/lefteye)
- [var mask: ImmersiveVideoMask?](/documentation/immersivemediasupport/immersivecameraviewmodel/mask)
- [var rightEye: MDLMesh](/documentation/immersivemediasupport/immersivecameraviewmodel/righteye)
- [ImmersiveVideoMask](/documentation/immersivemediasupport/immersivevideomask)

### Instance Properties

- [var layout: ImmersiveVideoMask.Layout](/documentation/immersivemediasupport/immersivevideomask/layout-swift.property)
- [var texture: any MTLTexture](/documentation/immersivemediasupport/immersivevideomask/texture)
- [var isInEquirectangularProjection: Bool](/documentation/immersivemediasupport/immersivevideomask/isinequirectangularprojection)

### Enumerations

- [ImmersiveVideoMask.Layout](/documentation/immersivemediasupport/immersivevideomask/layout-swift.enum)

#### Enumeration Cases

- [case mono](/documentation/immersivemediasupport/immersivevideomask/layout-swift.enum/mono)
- [case overUnder](/documentation/immersivemediasupport/immersivevideomask/layout-swift.enum/overunder)
- [case separate](/documentation/immersivemediasupport/immersivevideomask/layout-swift.enum/separate)
- [case sideBySide](/documentation/immersivemediasupport/immersivevideomask/layout-swift.enum/sidebyside)

### Operators

- [static func == (ImmersiveVideoMask, ImmersiveVideoMask) -> Bool](/documentation/immersivemediasupport/immersivevideomask/==(_:_:))

### Initializers

- [init(layout: ImmersiveVideoMask.Layout, isInEquirectangularProjection: Bool, texture: any MTLTexture)](/documentation/immersivemediasupport/immersivevideomask/init(layout:isinequirectangularprojection:texture:))

## Preview

- [ImmersiveMediaPreviewMessagingProtocol](/documentation/immersivemediasupport/immersivemediapreviewmessagingprotocol)

### Type Properties

- [static let definition: NWProtocolFramer.Definition](/documentation/immersivemediasupport/immersivemediapreviewmessagingprotocol/definition)

## Validation

- [AIVUValidator](/documentation/immersivemediasupport/aivuvalidator)

### Type Methods

- [static func validate(url: URL) async throws -> Bool](/documentation/immersivemediasupport/aivuvalidator/validate(url:))

## Classes

- [ImmersiveCameraMeshCalibration](/documentation/immersivemediasupport/immersivecamerameshcalibration)

### Initializers

- [init(name: String, usdzData: Data)](/documentation/immersivemediasupport/immersivecamerameshcalibration/init(name:usdzdata:))

### Instance Properties

- [let name: String](/documentation/immersivemediasupport/immersivecamerameshcalibration/name)
- [let usdzData: Data](/documentation/immersivemediasupport/immersivecamerameshcalibration/usdzdata)
- [ImmersiveImageMask](/documentation/immersivemediasupport/immersiveimagemask)

### Initializers

- [init(name: String, maskData: Data?)](/documentation/immersivemediasupport/immersiveimagemask/init(name:maskdata:))
- [init(name: String, maskURL: URL)](/documentation/immersivemediasupport/immersiveimagemask/init(name:maskurl:))

### Instance Properties

- [let maskData: Data?](/documentation/immersivemediasupport/immersiveimagemask/maskdata)
- [let name: String](/documentation/immersivemediasupport/immersiveimagemask/name)
- [ImmersiveMediaRemotePreviewReceiver](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver)

### Initializers

- [init() async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/init())

### Instance Properties

- [var frame: ImmersiveVideoFrame?](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/frame)
- [var presentationDescriptor: PresentationDescriptor?](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/presentationdescriptor)
- [var states: some AsyncSequence<ImmersiveMediaRemotePreviewReceiver.Status, Never>](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/states)
- [var venueDescriptor: VenueDescriptor?](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/venuedescriptor)

### Instance Methods

- [func start(connection: NWConnection) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/start(connection:))
- [func stop()](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/stop())

### Enumerations

- [ImmersiveMediaRemotePreviewReceiver.Status](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/status)

#### Enumeration Cases

- [case failed](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/status/failed)
- [case started](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/status/started)
- [case starting](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/status/starting)
- [case stopped](/documentation/immersivemediasupport/immersivemediaremotepreviewreceiver/status/stopped)
- [ImmersiveMediaRemotePreviewSender](/documentation/immersivemediasupport/immersivemediaremotepreviewsender)

### Initializers

- [init(networkParameters: NWParameters?) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/init(networkparameters:))

### Instance Properties

- [var connectedReceiverNames: [String]](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/connectedreceivernames)
- [var isReadyToSendData: Bool](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/isreadytosenddata)
- [var preferredFrameRate: Int](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/preferredframerate)
- [var preferredVideoHeight: Int](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/preferredvideoheight)
- [var preferredVideoWidth: Int](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/preferredvideowidth)

### Instance Methods

- [func connectReceiver(name: String, endpoint: NWEndpoint) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/connectreceiver(name:endpoint:))
- [func disconnectReceiver(name: String) async](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/disconnectreceiver(name:))
- [func send(audioBuffer: CMSampleBuffer) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/send(audiobuffer:))
- [func send(taggedBuffers: [CMTaggedBuffer], presentationTimeStamp: CMTime, frameDuration: CMTime) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/send(taggedbuffers:presentationtimestamp:frameduration:))
- [func send(venueDescriptor: VenueDescriptor) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/send(venuedescriptor:))
- [func send(videoBuffer: CMSampleBuffer) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/send(videobuffer:))
- [func send(videoFrame: ImmersiveVideoFrame, presentationTimeStamp: CMTime, frameDuration: CMTime, metadata: [PresentationCommand]) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/send(videoframe:presentationtimestamp:frameduration:metadata:))
- [func sendVenueDescriptor(at: URL) async throws](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/sendvenuedescriptor(at:))
- [func start() async](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/start())
- [func stop() async](/documentation/immersivemediasupport/immersivemediaremotepreviewsender/stop())

## Structures

- [ImmersiveCameraLensDefinition](/documentation/immersivemediasupport/immersivecameralensdefinition)

### Initializers

- [init(from: Data) throws](/documentation/immersivemediasupport/immersivecameralensdefinition/init(from:))

### Instance Properties

- [var cameraID: String](/documentation/immersivemediasupport/immersivecameralensdefinition/cameraid)

### Instance Methods

- [func generateSTMap(device: any MTLDevice, cameraEye: ImmersiveCameraLensDefinition.Eye, stmapType: ImmersiveCameraLensDefinition.STMapType, into: any MTLTexture) async throws](/documentation/immersivemediasupport/immersivecameralensdefinition/generatestmap(device:cameraeye:stmaptype:into:))

### Enumerations

- [ImmersiveCameraLensDefinition.Eye](/documentation/immersivemediasupport/immersivecameralensdefinition/eye)

#### Enumeration Cases

- [case left](/documentation/immersivemediasupport/immersivecameralensdefinition/eye/left)
- [case right](/documentation/immersivemediasupport/immersivecameralensdefinition/eye/right)
- [ImmersiveCameraLensDefinition.STMapType](/documentation/immersivemediasupport/immersivecameralensdefinition/stmaptype)

#### Enumeration Cases

- [case equidistant](/documentation/immersivemediasupport/immersivecameralensdefinition/stmaptype/equidistant)
- [case equirectangular](/documentation/immersivemediasupport/immersivecameralensdefinition/stmaptype/equirectangular)
- [ImmersiveVideoFrame](/documentation/immersivemediasupport/immersivevideoframe)

### Initializers

- [init(leftEye: CVPixelBuffer, rightEye: CVPixelBuffer, presentationTime: CMTime)](/documentation/immersivemediasupport/immersivevideoframe/init(lefteye:righteye:presentationtime:))
- [init(pixelBuffer: CVPixelBuffer, presentationTime: CMTime, layout: ImmersiveVideoFrame.VideoLayout)](/documentation/immersivemediasupport/immersivevideoframe/init(pixelbuffer:presentationtime:layout:))

### Instance Properties

- [let layout: ImmersiveVideoFrame.VideoLayout](/documentation/immersivemediasupport/immersivevideoframe/layout)
- [let pixelBuffers: [CVPixelBuffer]](/documentation/immersivemediasupport/immersivevideoframe/pixelbuffers)
- [let presentationTime: CMTime](/documentation/immersivemediasupport/immersivevideoframe/presentationtime)

### Enumerations

- [ImmersiveVideoFrame.VideoLayout](/documentation/immersivemediasupport/immersivevideoframe/videolayout)

#### Enumeration Cases

- [case mono](/documentation/immersivemediasupport/immersivevideoframe/videolayout/mono)
- [case overUnder](/documentation/immersivemediasupport/immersivevideoframe/videolayout/overunder)
- [case separate](/documentation/immersivemediasupport/immersivevideoframe/videolayout/separate)
- [case sideBySide](/documentation/immersivemediasupport/immersivevideoframe/videolayout/sidebyside)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
