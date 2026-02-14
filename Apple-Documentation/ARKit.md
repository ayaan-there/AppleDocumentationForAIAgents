# ARKit Documentation

Source: https://sosumi.ai/documentation/arkit

---
title: ARKit
source: https://developer.apple.com/documentation/arkit
timestamp: 2026-02-13T19:22:53.031Z
---

## visionOS

- [Setting up access to ARKit data](/documentation/visionos/setting-up-access-to-arkit-data)
- [ARKitSession](/documentation/arkit/arkitsession)

### Starting and stopping a session

- [convenience init()](/documentation/arkit/arkitsession/init())
- [func run([any DataProvider]) async throws](/documentation/arkit/arkitsession/run(_:))
- [func stop()](/documentation/arkit/arkitsession/stop())
- [ARKitSession.Error](/documentation/arkit/arkitsession/error)

#### Inspecting ARKit errors

- [let dataProvider: (any DataProvider)?](/documentation/arkit/arkitsession/error/dataprovider)
- [var code: ARKitSession.Error.Code](/documentation/arkit/arkitsession/error/code-swift.property)
- [ARKitSession.Error.Code](/documentation/arkit/arkitsession/error/code-swift.enum)

##### Determining the cause of session errors

- [case dataProviderFailedToRun](/documentation/arkit/arkitsession/error/code-swift.enum/dataproviderfailedtorun)
- [case dataProviderNotAuthorized](/documentation/arkit/arkitsession/error/code-swift.enum/dataprovidernotauthorized)

##### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/error/code-swift.enum/description)
- [var errorDescription: String?](/documentation/arkit/arkitsession/error/errordescription)

#### Providing recovery suggestions

- [var recoverySuggestion: String?](/documentation/arkit/arkitsession/error/recoverysuggestion)
- [var failureReason: String?](/documentation/arkit/arkitsession/error/failurereason)

#### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/error/description)

### Getting authorization

- [func requestAuthorization(for: [ARKitSession.AuthorizationType]) async -> [ARKitSession.AuthorizationType : ARKitSession.AuthorizationStatus]](/documentation/arkit/arkitsession/requestauthorization(for:))
- [ARKitSession.AuthorizationType](/documentation/arkit/arkitsession/authorizationtype)

#### Requesting authorization

- [case handTracking](/documentation/arkit/arkitsession/authorizationtype/handtracking)
- [case worldSensing](/documentation/arkit/arkitsession/authorizationtype/worldsensing)
- [case cameraAccess](/documentation/arkit/arkitsession/authorizationtype/cameraaccess)

#### Enumeration Cases

- [case accessoryTracking](/documentation/arkit/arkitsession/authorizationtype/accessorytracking)

#### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/authorizationtype/description)
- [func queryAuthorization(for: [ARKitSession.AuthorizationType]) async -> [ARKitSession.AuthorizationType : ARKitSession.AuthorizationStatus]](/documentation/arkit/arkitsession/queryauthorization(for:))
- [ARKitSession.AuthorizationStatus](/documentation/arkit/arkitsession/authorizationstatus)

#### Getting authorization states

- [case notDetermined](/documentation/arkit/arkitsession/authorizationstatus/notdetermined)
- [case allowed](/documentation/arkit/arkitsession/authorizationstatus/allowed)
- [case denied](/documentation/arkit/arkitsession/authorizationstatus/denied)

#### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/authorizationstatus/description)

### Observing a session

- [var events: ARKitSession.Events](/documentation/arkit/arkitsession/events-swift.property)
- [ARKitSession.Events](/documentation/arkit/arkitsession/events-swift.struct)

#### Structures

- [ARKitSession.Events.Iterator](/documentation/arkit/arkitsession/events-swift.struct/iterator)

##### Type aliases

- [ARKitSession.Events.Element](/documentation/arkit/arkitsession/events-swift.struct/element)

##### Instance methods

- [func next() async -> ARKitSession.Events.Element?](/documentation/arkit/arkitsession/events-swift.struct/iterator/next())

#### Instance Methods

- [func makeAsyncIterator() -> ARKitSession.Events.Iterator](/documentation/arkit/arkitsession/events-swift.struct/makeasynciterator())

#### Type Aliases

- [ARKitSession.Events.Element](/documentation/arkit/arkitsession/events-swift.struct/element)
- [ARKitSession.Event](/documentation/arkit/arkitsession/event)

#### Enumeration Cases

- [case authorizationChanged(type: ARKitSession.AuthorizationType, status: ARKitSession.AuthorizationStatus)](/documentation/arkit/arkitsession/event/authorizationchanged(type:status:))
- [case dataProviderStateChanged(dataProviders: [any DataProvider], newState: DataProviderState, error: ARKitSession.Error?)](/documentation/arkit/arkitsession/event/dataproviderstatechanged(dataproviders:newstate:error:))

#### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/event/description)
- [var description: String](/documentation/arkit/arkitsession/description)

### Initializers

- [convenience init(device: RemoteDeviceIdentifier)](/documentation/arkit/arkitsession/init(device:))

### Instance Properties

- [var dataProviders: [any DataProvider]](/documentation/arkit/arkitsession/dataproviders)
- [DataProvider](/documentation/arkit/dataprovider)

### Inspecting a data provider

- [var state: DataProviderState](/documentation/arkit/dataprovider/state)

### Inspecting a data provider type

- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/dataprovider/requiredauthorizations)
- [static var isSupported: Bool](/documentation/arkit/dataprovider/issupported)
- [Anchor](/documentation/arkit/anchor)

### Inspecting an anchor

- [var id: UUID](/documentation/arkit/anchor/id)
- [var timestamp: TimeInterval](/documentation/arkit/anchor/timestamp)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/anchor/originfromanchortransform)

### Tracking anchors over time

- [AnchorUpdate](/documentation/arkit/anchorupdate)

#### Inspecting anchor updates

- [let anchor: AnchorType](/documentation/arkit/anchorupdate/anchor)
- [var timestamp: TimeInterval](/documentation/arkit/anchorupdate/timestamp)
- [let event: AnchorUpdate<AnchorType>.Event](/documentation/arkit/anchorupdate/event-swift.property)
- [AnchorUpdate.Event](/documentation/arkit/anchorupdate/event-swift.enum)

##### Inspecting anchor update events

- [case added](/documentation/arkit/anchorupdate/event-swift.enum/added)
- [case updated](/documentation/arkit/anchorupdate/event-swift.enum/updated)
- [case removed](/documentation/arkit/anchorupdate/event-swift.enum/removed)

##### Instance Properties

- [var description: String](/documentation/arkit/anchorupdate/event-swift.enum/description)
- [var description: String](/documentation/arkit/anchorupdate/description)
- [AnchorUpdateSequence](/documentation/arkit/anchorupdatesequence)

#### Performing sequence operations

- [AnchorUpdateSequence.Iterator](/documentation/arkit/anchorupdatesequence/iterator)
- [ARKit in visionOS](/documentation/arkit/arkit-in-visionos)

### Setup

- [Setting up access to ARKit data](/documentation/visionos/setting-up-access-to-arkit-data)
- [ARKitSession](/documentation/arkit/arkitsession)

#### Starting and stopping a session

- [convenience init()](/documentation/arkit/arkitsession/init())
- [func run([any DataProvider]) async throws](/documentation/arkit/arkitsession/run(_:))
- [func stop()](/documentation/arkit/arkitsession/stop())
- [ARKitSession.Error](/documentation/arkit/arkitsession/error)

##### Inspecting ARKit errors

- [let dataProvider: (any DataProvider)?](/documentation/arkit/arkitsession/error/dataprovider)
- [var code: ARKitSession.Error.Code](/documentation/arkit/arkitsession/error/code-swift.property)
- [ARKitSession.Error.Code](/documentation/arkit/arkitsession/error/code-swift.enum)

###### Determining the cause of session errors

- [case dataProviderFailedToRun](/documentation/arkit/arkitsession/error/code-swift.enum/dataproviderfailedtorun)
- [case dataProviderNotAuthorized](/documentation/arkit/arkitsession/error/code-swift.enum/dataprovidernotauthorized)

###### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/error/code-swift.enum/description)
- [var errorDescription: String?](/documentation/arkit/arkitsession/error/errordescription)

##### Providing recovery suggestions

- [var recoverySuggestion: String?](/documentation/arkit/arkitsession/error/recoverysuggestion)
- [var failureReason: String?](/documentation/arkit/arkitsession/error/failurereason)

##### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/error/description)

#### Getting authorization

- [func requestAuthorization(for: [ARKitSession.AuthorizationType]) async -> [ARKitSession.AuthorizationType : ARKitSession.AuthorizationStatus]](/documentation/arkit/arkitsession/requestauthorization(for:))
- [ARKitSession.AuthorizationType](/documentation/arkit/arkitsession/authorizationtype)

##### Requesting authorization

- [case handTracking](/documentation/arkit/arkitsession/authorizationtype/handtracking)
- [case worldSensing](/documentation/arkit/arkitsession/authorizationtype/worldsensing)
- [case cameraAccess](/documentation/arkit/arkitsession/authorizationtype/cameraaccess)

##### Enumeration Cases

- [case accessoryTracking](/documentation/arkit/arkitsession/authorizationtype/accessorytracking)

##### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/authorizationtype/description)
- [func queryAuthorization(for: [ARKitSession.AuthorizationType]) async -> [ARKitSession.AuthorizationType : ARKitSession.AuthorizationStatus]](/documentation/arkit/arkitsession/queryauthorization(for:))
- [ARKitSession.AuthorizationStatus](/documentation/arkit/arkitsession/authorizationstatus)

##### Getting authorization states

- [case notDetermined](/documentation/arkit/arkitsession/authorizationstatus/notdetermined)
- [case allowed](/documentation/arkit/arkitsession/authorizationstatus/allowed)
- [case denied](/documentation/arkit/arkitsession/authorizationstatus/denied)

##### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/authorizationstatus/description)

#### Observing a session

- [var events: ARKitSession.Events](/documentation/arkit/arkitsession/events-swift.property)
- [ARKitSession.Events](/documentation/arkit/arkitsession/events-swift.struct)

##### Structures

- [ARKitSession.Events.Iterator](/documentation/arkit/arkitsession/events-swift.struct/iterator)

###### Type aliases

- [ARKitSession.Events.Element](/documentation/arkit/arkitsession/events-swift.struct/element)

###### Instance methods

- [func next() async -> ARKitSession.Events.Element?](/documentation/arkit/arkitsession/events-swift.struct/iterator/next())

##### Instance Methods

- [func makeAsyncIterator() -> ARKitSession.Events.Iterator](/documentation/arkit/arkitsession/events-swift.struct/makeasynciterator())

##### Type Aliases

- [ARKitSession.Events.Element](/documentation/arkit/arkitsession/events-swift.struct/element)
- [ARKitSession.Event](/documentation/arkit/arkitsession/event)

##### Enumeration Cases

- [case authorizationChanged(type: ARKitSession.AuthorizationType, status: ARKitSession.AuthorizationStatus)](/documentation/arkit/arkitsession/event/authorizationchanged(type:status:))
- [case dataProviderStateChanged(dataProviders: [any DataProvider], newState: DataProviderState, error: ARKitSession.Error?)](/documentation/arkit/arkitsession/event/dataproviderstatechanged(dataproviders:newstate:error:))

##### Instance Properties

- [var description: String](/documentation/arkit/arkitsession/event/description)
- [var description: String](/documentation/arkit/arkitsession/description)

#### Initializers

- [convenience init(device: RemoteDeviceIdentifier)](/documentation/arkit/arkitsession/init(device:))

#### Instance Properties

- [var dataProviders: [any DataProvider]](/documentation/arkit/arkitsession/dataproviders)
- [DataProvider](/documentation/arkit/dataprovider)

#### Inspecting a data provider

- [var state: DataProviderState](/documentation/arkit/dataprovider/state)

#### Inspecting a data provider type

- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/dataprovider/requiredauthorizations)
- [static var isSupported: Bool](/documentation/arkit/dataprovider/issupported)
- [DataProviderState](/documentation/arkit/dataproviderstate)

#### Getting the state of a data provider

- [case initialized](/documentation/arkit/dataproviderstate/initialized)
- [case running](/documentation/arkit/dataproviderstate/running)
- [case stopped](/documentation/arkit/dataproviderstate/stopped)
- [case paused](/documentation/arkit/dataproviderstate/paused)

#### Comparing data provider states

- [var description: String](/documentation/arkit/dataproviderstate/description)
- [Anchor](/documentation/arkit/anchor)

#### Inspecting an anchor

- [var id: UUID](/documentation/arkit/anchor/id)
- [var timestamp: TimeInterval](/documentation/arkit/anchor/timestamp)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/anchor/originfromanchortransform)

#### Tracking anchors over time

- [AnchorUpdate](/documentation/arkit/anchorupdate)

##### Inspecting anchor updates

- [let anchor: AnchorType](/documentation/arkit/anchorupdate/anchor)
- [var timestamp: TimeInterval](/documentation/arkit/anchorupdate/timestamp)
- [let event: AnchorUpdate<AnchorType>.Event](/documentation/arkit/anchorupdate/event-swift.property)
- [AnchorUpdate.Event](/documentation/arkit/anchorupdate/event-swift.enum)

###### Inspecting anchor update events

- [case added](/documentation/arkit/anchorupdate/event-swift.enum/added)
- [case updated](/documentation/arkit/anchorupdate/event-swift.enum/updated)
- [case removed](/documentation/arkit/anchorupdate/event-swift.enum/removed)

###### Instance Properties

- [var description: String](/documentation/arkit/anchorupdate/event-swift.enum/description)
- [var description: String](/documentation/arkit/anchorupdate/description)
- [AnchorUpdateSequence](/documentation/arkit/anchorupdatesequence)

##### Performing sequence operations

- [AnchorUpdateSequence.Iterator](/documentation/arkit/anchorupdatesequence/iterator)
- [TrackableAnchor](/documentation/arkit/trackableanchor)

#### Checking an anchor’s tracking state

- [var isTracked: Bool](/documentation/arkit/trackableanchor/istracked)
- [ARKitCoordinateSpace](/documentation/arkit/arkitcoordinatespace)

#### Instance Properties

- [var ancestorSpace: WorldReferenceCoordinateSpace?](/documentation/arkit/arkitcoordinatespace/ancestorspace)

#### Instance Methods

- [func ancestorFromSpaceTransformFloat() -> ProjectiveTransform3DFloat](/documentation/arkit/arkitcoordinatespace/ancestorfromspacetransformfloat())

#### Enumerations

- [ARKitCoordinateSpace.Correction](/documentation/arkit/arkitcoordinatespace/correction)

##### Enumeration Cases

- [case none](/documentation/arkit/arkitcoordinatespace/correction/none)
- [case rendered](/documentation/arkit/arkitcoordinatespace/correction/rendered)

##### Instance Properties

- [var description: String](/documentation/arkit/arkitcoordinatespace/correction/description)

### Barcode detection

- [BarcodeDetectionProvider](/documentation/arkit/barcodedetectionprovider)

#### Creating a barcode detection provider

- [init(symbologies: [BarcodeAnchor.Symbology])](/documentation/arkit/barcodedetectionprovider/init(symbologies:))

#### Inspecting a barcode detection provider

- [var anchorUpdates: AnchorUpdateSequence<BarcodeAnchor>](/documentation/arkit/barcodedetectionprovider/anchorupdates)
- [var description: String](/documentation/arkit/barcodedetectionprovider/description)
- [var state: DataProviderState](/documentation/arkit/barcodedetectionprovider/state)

#### Type properties

- [static var isSupported: Bool](/documentation/arkit/barcodedetectionprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/barcodedetectionprovider/requiredauthorizations)
- [BarcodeAnchor](/documentation/arkit/barcodeanchor)

#### Getting barcode information

- [var extent: SIMD3<Float>](/documentation/arkit/barcodeanchor/extent)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/barcodeanchor/originfromanchortransform)
- [var payloadData: Data](/documentation/arkit/barcodeanchor/payloaddata)
- [var payloadString: String?](/documentation/arkit/barcodeanchor/payloadstring)
- [var symbology: BarcodeAnchor.Symbology](/documentation/arkit/barcodeanchor/symbology-swift.property)
- [BarcodeAnchor.Symbology](/documentation/arkit/barcodeanchor/symbology-swift.enum)

##### Barcode symbologies

- [case aztec](/documentation/arkit/barcodeanchor/symbology-swift.enum/aztec)
- [case codabar](/documentation/arkit/barcodeanchor/symbology-swift.enum/codabar)
- [case code128](/documentation/arkit/barcodeanchor/symbology-swift.enum/code128)
- [case code39](/documentation/arkit/barcodeanchor/symbology-swift.enum/code39)
- [case code39Checksum](/documentation/arkit/barcodeanchor/symbology-swift.enum/code39checksum)
- [case code39FullAscii](/documentation/arkit/barcodeanchor/symbology-swift.enum/code39fullascii)
- [case code39FullAsciiChecksum](/documentation/arkit/barcodeanchor/symbology-swift.enum/code39fullasciichecksum)
- [case code93](/documentation/arkit/barcodeanchor/symbology-swift.enum/code93)
- [case code93i](/documentation/arkit/barcodeanchor/symbology-swift.enum/code93i)
- [case dataMatrix](/documentation/arkit/barcodeanchor/symbology-swift.enum/datamatrix)
- [case ean13](/documentation/arkit/barcodeanchor/symbology-swift.enum/ean13)
- [case ean8](/documentation/arkit/barcodeanchor/symbology-swift.enum/ean8)
- [case gs1DataBar](/documentation/arkit/barcodeanchor/symbology-swift.enum/gs1databar)
- [case gs1DataBarExpanded](/documentation/arkit/barcodeanchor/symbology-swift.enum/gs1databarexpanded)
- [case gs1DataBarLimited](/documentation/arkit/barcodeanchor/symbology-swift.enum/gs1databarlimited)
- [case itf](/documentation/arkit/barcodeanchor/symbology-swift.enum/itf)
- [case itf14](/documentation/arkit/barcodeanchor/symbology-swift.enum/itf14)
- [case itfChecksum](/documentation/arkit/barcodeanchor/symbology-swift.enum/itfchecksum)
- [case microPDF417](/documentation/arkit/barcodeanchor/symbology-swift.enum/micropdf417)
- [case microQR](/documentation/arkit/barcodeanchor/symbology-swift.enum/microqr)
- [case msiPlessey](/documentation/arkit/barcodeanchor/symbology-swift.enum/msiplessey)
- [case pdf417](/documentation/arkit/barcodeanchor/symbology-swift.enum/pdf417)
- [case qr](/documentation/arkit/barcodeanchor/symbology-swift.enum/qr)
- [case upce](/documentation/arkit/barcodeanchor/symbology-swift.enum/upce)

##### Instance Properties

- [var description: String](/documentation/arkit/barcodeanchor/symbology-swift.enum/description)
- [var id: UUID](/documentation/arkit/barcodeanchor/id)

#### Instance Properties

- [var description: String](/documentation/arkit/barcodeanchor/description)

### Camera sampling

- [CameraFrameProvider](/documentation/arkit/cameraframeprovider)

#### Creating a camera frame provider

- [init()](/documentation/arkit/cameraframeprovider/init())

#### Getting information about the camera frame provider

- [var description: String](/documentation/arkit/cameraframeprovider/description)
- [var state: DataProviderState](/documentation/arkit/cameraframeprovider/state)

#### Getting camera frame updates

- [func cameraFrameUpdates(for: CameraVideoFormat) -> CameraFrameProvider.CameraFrameUpdates?](/documentation/arkit/cameraframeprovider/cameraframeupdates(for:))
- [CameraFrameProvider.CameraFrameUpdates](/documentation/arkit/cameraframeprovider/cameraframeupdates)

##### Instance properties

- [static var isSupported: Bool](/documentation/arkit/cameraframeprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/cameraframeprovider/requiredauthorizations)

##### Instance methods

- [func makeAsyncIterator() -> CameraFrameProvider.CameraFrameUpdates.Iterator](/documentation/arkit/cameraframeprovider/cameraframeupdates/makeasynciterator())

##### Iterating over camera updates

- [CameraFrameProvider.CameraFrameUpdates.Iterator](/documentation/arkit/cameraframeprovider/cameraframeupdates/iterator)

###### Type methods

- [func next() async -> CameraFrameProvider.CameraFrameUpdates.Element?](/documentation/arkit/cameraframeprovider/cameraframeupdates/iterator/next())

###### Type aliases

- [CameraFrameProvider.CameraFrameUpdates.Element](/documentation/arkit/cameraframeprovider/cameraframeupdates/element)

##### Type aliases

- [CameraFrameProvider.CameraFrameUpdates.Element](/documentation/arkit/cameraframeprovider/cameraframeupdates/element)

#### Enumerations

- [CameraFrameProvider.CameraPosition](/documentation/arkit/cameraframeprovider/cameraposition)

##### Camera positions

- [case left](/documentation/arkit/cameraframeprovider/cameraposition/left)

##### Enumeration Cases

- [case right](/documentation/arkit/cameraframeprovider/cameraposition/right)

##### Instance Properties

- [var description: String](/documentation/arkit/cameraframeprovider/cameraposition/description)
- [CameraFrameProvider.CameraType](/documentation/arkit/cameraframeprovider/cameratype)

##### Camera types

- [case main](/documentation/arkit/cameraframeprovider/cameratype/main)

##### Instance Properties

- [var description: String](/documentation/arkit/cameraframeprovider/cameratype/description)
- [CameraFrameProvider.CameraRectification](/documentation/arkit/cameraframeprovider/camerarectification)

##### Enumeration Cases

- [case mono](/documentation/arkit/cameraframeprovider/camerarectification/mono)
- [case stereoCorrected](/documentation/arkit/cameraframeprovider/camerarectification/stereocorrected)

##### Instance Properties

- [var description: String](/documentation/arkit/cameraframeprovider/camerarectification/description)

#### Type Properties

- [static var isSupported: Bool](/documentation/arkit/cameraframeprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/cameraframeprovider/requiredauthorizations)
- [CameraFrame](/documentation/arkit/cameraframe)

#### Getting camera frame information

- [var primarySample: CameraFrame.Sample](/documentation/arkit/cameraframe/primarysample)
- [CameraFrame.Sample](/documentation/arkit/cameraframe/sample)

##### Inspecting camera frame samples

- [var parameters: CameraFrame.Sample.Parameters](/documentation/arkit/cameraframe/sample/parameters-swift.property)
- [CameraFrame.Sample.Parameters](/documentation/arkit/cameraframe/sample/parameters-swift.struct)

###### Getting frame parameters

- [var cameraPosition: CameraFrameProvider.CameraPosition](/documentation/arkit/cameraframe/sample/parameters-swift.struct/cameraposition)
- [var cameraType: CameraFrameProvider.CameraType](/documentation/arkit/cameraframe/sample/parameters-swift.struct/cameratype)
- [var captureTimestamp: TimeInterval](/documentation/arkit/cameraframe/sample/parameters-swift.struct/capturetimestamp)
- [var colorTemperature: Int](/documentation/arkit/cameraframe/sample/parameters-swift.struct/colortemperature)
- [var exposureDuration: TimeInterval](/documentation/arkit/cameraframe/sample/parameters-swift.struct/exposureduration)
- [var extrinsics: simd_float4x4](/documentation/arkit/cameraframe/sample/parameters-swift.struct/extrinsics)
- [var intrinsics: simd_float3x3](/documentation/arkit/cameraframe/sample/parameters-swift.struct/intrinsics)
- [var midExposureTimestamp: TimeInterval](/documentation/arkit/cameraframe/sample/parameters-swift.struct/midexposuretimestamp)

###### Instance Properties

- [var description: String](/documentation/arkit/cameraframe/sample/parameters-swift.struct/description)
- [var pixelBuffer: CVPixelBuffer](/documentation/arkit/cameraframe/sample/pixelbuffer)

##### Instance Properties

- [var buffer: CVReadOnlyPixelBuffer](/documentation/arkit/cameraframe/sample/buffer)
- [var description: String](/documentation/arkit/cameraframe/sample/description)
- [func sample(for: CameraFrameProvider.CameraPosition) -> CameraFrame.Sample?](/documentation/arkit/cameraframe/sample(for:))
- [var description: String](/documentation/arkit/cameraframe/description)

#### Instance Properties

- [var samples: [CameraFrame.Sample]](/documentation/arkit/cameraframe/samples)
- [CameraVideoFormat](/documentation/arkit/cameravideoformat)

#### Getting camera video format information

- [var cameraPositions: [CameraFrameProvider.CameraPosition]](/documentation/arkit/cameravideoformat/camerapositions)
- [var cameraType: CameraFrameProvider.CameraType](/documentation/arkit/cameravideoformat/cameratype)
- [var frameSize: CGSize](/documentation/arkit/cameravideoformat/framesize)
- [var pixelFormat: OSType](/documentation/arkit/cameravideoformat/pixelformat)
- [var maxFrameDuration: Float](/documentation/arkit/cameravideoformat/maxframeduration)
- [var minFrameDuration: Float](/documentation/arkit/cameravideoformat/minframeduration)
- [static func supportedVideoFormats(for: CameraFrameProvider.CameraType, cameraPositions: [CameraFrameProvider.CameraPosition]) -> [CameraVideoFormat]](/documentation/arkit/cameravideoformat/supportedvideoformats(for:camerapositions:))
- [var description: String](/documentation/arkit/cameravideoformat/description)

#### Instance Properties

- [var cameraRectification: CameraFrameProvider.CameraRectification](/documentation/arkit/cameravideoformat/camerarectification)

### Rendering

- [StereoPropertiesProvider](/documentation/arkit/stereopropertiesprovider)

#### Initializers

- [init()](/documentation/arkit/stereopropertiesprovider/init())

#### Instance Properties

- [var description: String](/documentation/arkit/stereopropertiesprovider/description)
- [var latestViewpointProperties: ViewpointProperties?](/documentation/arkit/stereopropertiesprovider/latestviewpointproperties)
- [var state: DataProviderState](/documentation/arkit/stereopropertiesprovider/state)

#### Type Properties

- [static var isSupported: Bool](/documentation/arkit/stereopropertiesprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/stereopropertiesprovider/requiredauthorizations)
- [ViewpointProperties](/documentation/arkit/viewpointproperties)

#### Instance Properties

- [var description: String](/documentation/arkit/viewpointproperties/description)
- [var deviceFromLeftViewpointTransform: simd_float4x4](/documentation/arkit/viewpointproperties/devicefromleftviewpointtransform)
- [var deviceFromRightViewpointTransform: simd_float4x4](/documentation/arkit/viewpointproperties/devicefromrightviewpointtransform)

### Camera region

- [CameraRegionProvider](/documentation/arkit/cameraregionprovider)

#### Structures

- [CameraRegionProvider.Error](/documentation/arkit/cameraregionprovider/error)

##### Instance Properties

- [var code: CameraRegionProvider.Error.Code](/documentation/arkit/cameraregionprovider/error/code-swift.property)
- [let dataProvider: (any DataProvider)?](/documentation/arkit/cameraregionprovider/error/dataprovider)
- [var description: String](/documentation/arkit/cameraregionprovider/error/description)
- [var errorDescription: String?](/documentation/arkit/cameraregionprovider/error/errordescription)
- [var failureReason: String?](/documentation/arkit/cameraregionprovider/error/failurereason)
- [var recoverySuggestion: String?](/documentation/arkit/cameraregionprovider/error/recoverysuggestion)

##### Enumerations

- [CameraRegionProvider.Error.Code](/documentation/arkit/cameraregionprovider/error/code-swift.enum)

###### Enumeration Cases

- [case addAnchorFailed](/documentation/arkit/cameraregionprovider/error/code-swift.enum/addanchorfailed)
- [case anchorLimitReached](/documentation/arkit/cameraregionprovider/error/code-swift.enum/anchorlimitreached)
- [case removeAnchorFailed](/documentation/arkit/cameraregionprovider/error/code-swift.enum/removeanchorfailed)

###### Instance Properties

- [var description: String](/documentation/arkit/cameraregionprovider/error/code-swift.enum/description)

#### Initializers

- [init()](/documentation/arkit/cameraregionprovider/init())

#### Instance Properties

- [var description: String](/documentation/arkit/cameraregionprovider/description)
- [var state: DataProviderState](/documentation/arkit/cameraregionprovider/state)

#### Instance Methods

- [func addAnchor(CameraRegionAnchor) async throws](/documentation/arkit/cameraregionprovider/addanchor(_:))
- [func anchorUpdates(forID: UUID) -> AnchorUpdateSequence<CameraRegionAnchor>](/documentation/arkit/cameraregionprovider/anchorupdates(forid:))
- [func removeAnchor(CameraRegionAnchor) async throws](/documentation/arkit/cameraregionprovider/removeanchor(_:))
- [func removeAnchor(forID: UUID) async throws](/documentation/arkit/cameraregionprovider/removeanchor(forid:))

#### Type Properties

- [static var isSupported: Bool](/documentation/arkit/cameraregionprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/cameraregionprovider/requiredauthorizations)
- [CameraRegionAnchor](/documentation/arkit/cameraregionanchor)

#### Initializers

- [init(originFromAnchorTransform: simd_float4x4, width: Float, height: Float, cameraEnhancement: CameraRegionAnchor.CameraEnhancement)](/documentation/arkit/cameraregionanchor/init(originfromanchortransform:width:height:cameraenhancement:))

#### Instance Properties

- [var cameraEnhancement: CameraRegionAnchor.CameraEnhancement](/documentation/arkit/cameraregionanchor/cameraenhancement-swift.property)
- [var description: String](/documentation/arkit/cameraregionanchor/description)
- [var height: Float](/documentation/arkit/cameraregionanchor/height)
- [var id: UUID](/documentation/arkit/cameraregionanchor/id)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/cameraregionanchor/originfromanchortransform)
- [var pixelBuffer: CVReadOnlyPixelBuffer?](/documentation/arkit/cameraregionanchor/pixelbuffer)
- [var width: Float](/documentation/arkit/cameraregionanchor/width)

#### Enumerations

- [CameraRegionAnchor.CameraEnhancement](/documentation/arkit/cameraregionanchor/cameraenhancement-swift.enum)

##### Enumeration Cases

- [case contrastAndVibrancy](/documentation/arkit/cameraregionanchor/cameraenhancement-swift.enum/contrastandvibrancy)
- [case stabilization](/documentation/arkit/cameraregionanchor/cameraenhancement-swift.enum/stabilization)

##### Instance Properties

- [var description: String](/documentation/arkit/cameraregionanchor/cameraenhancement-swift.enum/description)

### Plane detection

- [Placing content on detected planes](/documentation/visionos/placing-content-on-detected-planes)
- [PlaneDetectionProvider](/documentation/arkit/planedetectionprovider)

#### Detecting planes

- [init(alignments: [PlaneAnchor.Alignment])](/documentation/arkit/planedetectionprovider/init(alignments:))
- [var allAnchors: [PlaneAnchor]](/documentation/arkit/planedetectionprovider/allanchors)
- [var anchorUpdates: AnchorUpdateSequence<PlaneAnchor>](/documentation/arkit/planedetectionprovider/anchorupdates)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/planedetectionprovider/requiredauthorizations)
- [static var isSupported: Bool](/documentation/arkit/planedetectionprovider/issupported)

#### Inspecting a plane detection provider

- [var alignments: [PlaneAnchor.Alignment]](/documentation/arkit/planedetectionprovider/alignments)
- [var state: DataProviderState](/documentation/arkit/planedetectionprovider/state)
- [var description: String](/documentation/arkit/planedetectionprovider/description)
- [PlaneAnchor](/documentation/arkit/planeanchor)

#### Inspecting a plane anchor

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/planeanchor/originfromanchortransform)
- [var alignment: PlaneAnchor.Alignment](/documentation/arkit/planeanchor/alignment-swift.property)
- [PlaneAnchor.Alignment](/documentation/arkit/planeanchor/alignment-swift.enum)

##### Alignment Values

- [case horizontal](/documentation/arkit/planeanchor/alignment-swift.enum/horizontal)
- [case vertical](/documentation/arkit/planeanchor/alignment-swift.enum/vertical)

##### Enumeration Cases

- [case slanted](/documentation/arkit/planeanchor/alignment-swift.enum/slanted)

##### Instance Properties

- [var description: String](/documentation/arkit/planeanchor/alignment-swift.enum/description)
- [var classification: PlaneAnchor.Classification](/documentation/arkit/planeanchor/classification-swift.property)
- [PlaneAnchor.Classification](/documentation/arkit/planeanchor/classification-swift.enum)

##### Getting known classifications

- [case ceiling](/documentation/arkit/planeanchor/classification-swift.enum/ceiling)
- [case door](/documentation/arkit/planeanchor/classification-swift.enum/door)
- [case floor](/documentation/arkit/planeanchor/classification-swift.enum/floor)
- [case seat](/documentation/arkit/planeanchor/classification-swift.enum/seat)
- [case table](/documentation/arkit/planeanchor/classification-swift.enum/table)
- [case wall](/documentation/arkit/planeanchor/classification-swift.enum/wall)
- [case window](/documentation/arkit/planeanchor/classification-swift.enum/window)

##### Getting unknown classifications

- [case notAvailable](/documentation/arkit/planeanchor/classification-swift.enum/notavailable)
- [case undetermined](/documentation/arkit/planeanchor/classification-swift.enum/undetermined)
- [case unknown](/documentation/arkit/planeanchor/classification-swift.enum/unknown)

##### Instance Properties

- [var description: String](/documentation/arkit/planeanchor/classification-swift.enum/description)
- [var description: String](/documentation/arkit/planeanchor/description)

#### Getting the shape of a plane anchor

- [var geometry: PlaneAnchor.Geometry](/documentation/arkit/planeanchor/geometry-swift.property)
- [PlaneAnchor.Geometry](/documentation/arkit/planeanchor/geometry-swift.struct)

##### Inspecting plane geometry

- [var meshFaces: GeometryElement](/documentation/arkit/planeanchor/geometry-swift.struct/meshfaces)
- [var meshVertices: GeometrySource](/documentation/arkit/planeanchor/geometry-swift.struct/meshvertices)
- [var extent: PlaneAnchor.Geometry.Extent](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.property)
- [PlaneAnchor.Geometry.Extent](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.struct)

###### Inspecting a plane extent

- [var width: Float](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.struct/width)
- [var height: Float](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.struct/height)
- [var anchorFromExtentTransform: simd_float4x4](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.struct/anchorfromextenttransform)

###### Instance Properties

- [var description: String](/documentation/arkit/planeanchor/geometry-swift.struct/extent-swift.struct/description)

##### Instance Properties

- [var description: String](/documentation/arkit/planeanchor/geometry-swift.struct/description)

#### Identifying a plane anchor

- [var id: UUID](/documentation/arkit/planeanchor/id)

#### Instance Properties

- [var surfaceClassification: SurfaceClassification](/documentation/arkit/planeanchor/surfaceclassification)

### World tracking

- [Tracking specific points in world space](/documentation/visionos/tracking-points-in-world-space)
- [WorldTrackingProvider](/documentation/arkit/worldtrackingprovider)

#### Tracking objects

- [init()](/documentation/arkit/worldtrackingprovider/init())
- [var anchorUpdates: AnchorUpdateSequence<WorldAnchor>](/documentation/arkit/worldtrackingprovider/anchorupdates)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/worldtrackingprovider/requiredauthorizations)
- [static var isSupported: Bool](/documentation/arkit/worldtrackingprovider/issupported)
- [var allAnchors: [WorldAnchor]?](/documentation/arkit/worldtrackingprovider/allanchors)
- [func addAnchor(WorldAnchor) async throws](/documentation/arkit/worldtrackingprovider/addanchor(_:))
- [WorldTrackingProvider.Error](/documentation/arkit/worldtrackingprovider/error)

##### Inspecting world-tracking errors

- [let anchor: WorldAnchor?](/documentation/arkit/worldtrackingprovider/error/anchor)
- [var code: WorldTrackingProvider.Error.Code](/documentation/arkit/worldtrackingprovider/error/code-swift.property)
- [WorldTrackingProvider.Error.Code](/documentation/arkit/worldtrackingprovider/error/code-swift.enum)

###### Determining causes for tracking failures

- [case addWorldAnchorFailed](/documentation/arkit/worldtrackingprovider/error/code-swift.enum/addworldanchorfailed)
- [case removeWorldAnchorFailed](/documentation/arkit/worldtrackingprovider/error/code-swift.enum/removeworldanchorfailed)
- [case worldAnchorLimitReached](/documentation/arkit/worldtrackingprovider/error/code-swift.enum/worldanchorlimitreached)

###### Instance Properties

- [var description: String](/documentation/arkit/worldtrackingprovider/error/code-swift.enum/description)
- [var errorDescription: String?](/documentation/arkit/worldtrackingprovider/error/errordescription)

##### Providing recovery suggestions

- [var recoverySuggestion: String?](/documentation/arkit/worldtrackingprovider/error/recoverysuggestion)
- [var failureReason: String?](/documentation/arkit/worldtrackingprovider/error/failurereason)

##### Instance Properties

- [var description: String](/documentation/arkit/worldtrackingprovider/error/description)

#### Stopping object tracking

- [func removeAnchor(WorldAnchor) async throws](/documentation/arkit/worldtrackingprovider/removeanchor(_:))
- [func removeAnchor(forID: UUID) async throws](/documentation/arkit/worldtrackingprovider/removeanchor(forid:))

#### Predicting device pose

- [func queryDeviceAnchor(atTimestamp: TimeInterval) -> DeviceAnchor?](/documentation/arkit/worldtrackingprovider/querydeviceanchor(attimestamp:))

#### Inspecting a world-tracking provider

- [var state: DataProviderState](/documentation/arkit/worldtrackingprovider/state)
- [var description: String](/documentation/arkit/worldtrackingprovider/description)

#### Instance Properties

- [var worldAnchorSharingAvailability: some AsyncSequence<WorldTrackingProvider.WorldAnchorSharingAvailability, Never>](/documentation/arkit/worldtrackingprovider/worldanchorsharingavailability-swift.property)

#### Instance Methods

- [func removeAllAnchors() async throws](/documentation/arkit/worldtrackingprovider/removeallanchors())

#### Enumerations

- [WorldTrackingProvider.WorldAnchorSharingAvailability](/documentation/arkit/worldtrackingprovider/worldanchorsharingavailability-swift.enum)

##### Enumeration Cases

- [case available](/documentation/arkit/worldtrackingprovider/worldanchorsharingavailability-swift.enum/available)
- [case unavailable](/documentation/arkit/worldtrackingprovider/worldanchorsharingavailability-swift.enum/unavailable)
- [WorldAnchor](/documentation/arkit/worldanchor)

#### Creating a world anchor

- [init(originFromAnchorTransform: simd_float4x4)](/documentation/arkit/worldanchor/init(originfromanchortransform:))

#### Identifying a world anchor

- [var id: UUID](/documentation/arkit/worldanchor/id)

#### Inspecting a world anchor

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/worldanchor/originfromanchortransform)
- [var isTracked: Bool](/documentation/arkit/worldanchor/istracked)
- [var description: String](/documentation/arkit/worldanchor/description)

#### Initializers

- [init(originFromAnchorTransform: simd_float4x4, sharedWithNearbyParticipants: Bool)](/documentation/arkit/worldanchor/init(originfromanchortransform:sharedwithnearbyparticipants:))

#### Instance Properties

- [var isSharedWithNearbyParticipants: Bool](/documentation/arkit/worldanchor/issharedwithnearbyparticipants)
- [DeviceAnchor](/documentation/arkit/deviceanchor)

#### Inspecting a device anchor

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/deviceanchor/originfromanchortransform)
- [var trackingState: DeviceAnchor.TrackingState](/documentation/arkit/deviceanchor/trackingstate-swift.property)
- [DeviceAnchor.TrackingState](/documentation/arkit/deviceanchor/trackingstate-swift.enum)

##### Tracking states

- [case orientationTracked](/documentation/arkit/deviceanchor/trackingstate-swift.enum/orientationtracked)
- [case tracked](/documentation/arkit/deviceanchor/trackingstate-swift.enum/tracked)
- [case untracked](/documentation/arkit/deviceanchor/trackingstate-swift.enum/untracked)
- [var isTracked: Bool](/documentation/arkit/deviceanchor/istracked)
- [var description: String](/documentation/arkit/deviceanchor/description)
- [var id: UUID](/documentation/arkit/deviceanchor/id)

### Hand tracking

- [Happy Beam](/documentation/visionos/happybeam)
- [HandTrackingProvider](/documentation/arkit/handtrackingprovider)

#### Creating a hand-tracking provider

- [init()](/documentation/arkit/handtrackingprovider/init())
- [static var isSupported: Bool](/documentation/arkit/handtrackingprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/handtrackingprovider/requiredauthorizations)

#### Observing hand anchor data

- [var anchorUpdates: AnchorUpdateSequence<HandAnchor>](/documentation/arkit/handtrackingprovider/anchorupdates)
- [var latestAnchors: (leftHand: HandAnchor?, rightHand: HandAnchor?)](/documentation/arkit/handtrackingprovider/latestanchors)

#### Inspecting a hand-tracking provider

- [var state: DataProviderState](/documentation/arkit/handtrackingprovider/state)
- [var description: String](/documentation/arkit/handtrackingprovider/description)
- [func handAnchors(at: TimeInterval) -> (leftHand: HandAnchor?, rightHand: HandAnchor?)](/documentation/arkit/handtrackingprovider/handanchors(at:))
- [HandAnchor](/documentation/arkit/handanchor)

#### Getting hand information

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/handanchor/originfromanchortransform)
- [var handSkeleton: HandSkeleton?](/documentation/arkit/handanchor/handskeleton)
- [var chirality: HandAnchor.Chirality](/documentation/arkit/handanchor/chirality-swift.property)
- [HandAnchor.Chirality](/documentation/arkit/handanchor/chirality-swift.enum)

##### Getting hand chirality

- [case left](/documentation/arkit/handanchor/chirality-swift.enum/left)
- [case right](/documentation/arkit/handanchor/chirality-swift.enum/right)

##### Instance Properties

- [var description: String](/documentation/arkit/handanchor/chirality-swift.enum/description)
- [var isTracked: Bool](/documentation/arkit/handanchor/istracked)
- [var description: String](/documentation/arkit/handanchor/description)

#### Identifying hand anchors

- [var id: UUID](/documentation/arkit/handanchor/id)

#### Instance Properties

- [var fidelity: HandAnchor.Fidelity](/documentation/arkit/handanchor/fidelity-swift.property)

#### Enumerations

- [HandAnchor.Fidelity](/documentation/arkit/handanchor/fidelity-swift.enum)

##### Enumeration Cases

- [case high](/documentation/arkit/handanchor/fidelity-swift.enum/high)
- [case nominal](/documentation/arkit/handanchor/fidelity-swift.enum/nominal)

##### Instance Properties

- [var description: String](/documentation/arkit/handanchor/fidelity-swift.enum/description)
- [HandSkeleton](/documentation/arkit/handskeleton)

#### Retrieving specific hand joints

- [func joint(HandSkeleton.JointName) -> HandSkeleton.Joint](/documentation/arkit/handskeleton/joint(_:))
- [HandSkeleton.Joint](/documentation/arkit/handskeleton/joint)

##### Inspecting hand joints

- [var name: HandSkeleton.JointName](/documentation/arkit/handskeleton/joint/name)
- [var parentJoint: HandSkeleton.Joint?](/documentation/arkit/handskeleton/joint/parentjoint)

##### Tracking the position of hand joints

- [var anchorFromJointTransform: simd_float4x4](/documentation/arkit/handskeleton/joint/anchorfromjointtransform)
- [var parentFromJointTransform: simd_float4x4](/documentation/arkit/handskeleton/joint/parentfromjointtransform)
- [var isTracked: Bool](/documentation/arkit/handskeleton/joint/istracked)

##### Instance Properties

- [var description: String](/documentation/arkit/handskeleton/joint/description)
- [HandSkeleton.JointName](/documentation/arkit/handskeleton/jointname)

##### Forearm joints

- [case forearmArm](/documentation/arkit/handskeleton/jointname/forearmarm)
- [case forearmWrist](/documentation/arkit/handskeleton/jointname/forearmwrist)
- [case wrist](/documentation/arkit/handskeleton/jointname/wrist)

##### Thumb joints

- [case thumbIntermediateBase](/documentation/arkit/handskeleton/jointname/thumbintermediatebase)
- [case thumbIntermediateTip](/documentation/arkit/handskeleton/jointname/thumbintermediatetip)
- [case thumbKnuckle](/documentation/arkit/handskeleton/jointname/thumbknuckle)
- [case thumbTip](/documentation/arkit/handskeleton/jointname/thumbtip)

##### Index finger joints

- [case indexFingerIntermediateBase](/documentation/arkit/handskeleton/jointname/indexfingerintermediatebase)
- [case indexFingerIntermediateTip](/documentation/arkit/handskeleton/jointname/indexfingerintermediatetip)
- [case indexFingerKnuckle](/documentation/arkit/handskeleton/jointname/indexfingerknuckle)
- [case indexFingerMetacarpal](/documentation/arkit/handskeleton/jointname/indexfingermetacarpal)
- [case indexFingerTip](/documentation/arkit/handskeleton/jointname/indexfingertip)

##### Middle finger joints

- [case middleFingerIntermediateBase](/documentation/arkit/handskeleton/jointname/middlefingerintermediatebase)
- [case middleFingerIntermediateTip](/documentation/arkit/handskeleton/jointname/middlefingerintermediatetip)
- [case middleFingerKnuckle](/documentation/arkit/handskeleton/jointname/middlefingerknuckle)
- [case middleFingerMetacarpal](/documentation/arkit/handskeleton/jointname/middlefingermetacarpal)
- [case middleFingerTip](/documentation/arkit/handskeleton/jointname/middlefingertip)

##### Ring finger joints

- [case ringFingerIntermediateBase](/documentation/arkit/handskeleton/jointname/ringfingerintermediatebase)
- [case ringFingerIntermediateTip](/documentation/arkit/handskeleton/jointname/ringfingerintermediatetip)
- [case ringFingerKnuckle](/documentation/arkit/handskeleton/jointname/ringfingerknuckle)
- [case ringFingerMetacarpal](/documentation/arkit/handskeleton/jointname/ringfingermetacarpal)
- [case ringFingerTip](/documentation/arkit/handskeleton/jointname/ringfingertip)

##### Little finger joints

- [case littleFingerIntermediateBase](/documentation/arkit/handskeleton/jointname/littlefingerintermediatebase)
- [case littleFingerIntermediateTip](/documentation/arkit/handskeleton/jointname/littlefingerintermediatetip)
- [case littleFingerKnuckle](/documentation/arkit/handskeleton/jointname/littlefingerknuckle)
- [case littleFingerMetacarpal](/documentation/arkit/handskeleton/jointname/littlefingermetacarpal)
- [case littleFingerTip](/documentation/arkit/handskeleton/jointname/littlefingertip)

##### Instance Properties

- [var description: String](/documentation/arkit/handskeleton/jointname/description)

#### Inspecting hand skeletons

- [var allJoints: [HandSkeleton.Joint]](/documentation/arkit/handskeleton/alljoints)
- [static var neutralPose: HandSkeleton](/documentation/arkit/handskeleton/neutralpose)
- [var description: String](/documentation/arkit/handskeleton/description)

### Scene reconstruction

- [Incorporating real-world surroundings in an immersive experience](/documentation/visionos/incorporating-real-world-surroundings-in-an-immersive-experience)
- [SceneReconstructionProvider](/documentation/arkit/scenereconstructionprovider)

#### Creating a scene reconstruction provider

- [init(modes: [SceneReconstructionProvider.Mode])](/documentation/arkit/scenereconstructionprovider/init(modes:))
- [let modes: [SceneReconstructionProvider.Mode]](/documentation/arkit/scenereconstructionprovider/modes)
- [SceneReconstructionProvider.Mode](/documentation/arkit/scenereconstructionprovider/mode)

##### Scene reconstruction modes

- [case classification](/documentation/arkit/scenereconstructionprovider/mode/classification)

##### Instance Properties

- [var description: String](/documentation/arkit/scenereconstructionprovider/mode/description)
- [static var isSupported: Bool](/documentation/arkit/scenereconstructionprovider/issupported)

#### Observing scene reconstruction

- [var anchorUpdates: AnchorUpdateSequence<MeshAnchor>](/documentation/arkit/scenereconstructionprovider/anchorupdates)
- [var state: DataProviderState](/documentation/arkit/scenereconstructionprovider/state)

#### Inspecting a scene reconstruction provider

- [var description: String](/documentation/arkit/scenereconstructionprovider/description)
- [var allAnchors: [MeshAnchor]](/documentation/arkit/scenereconstructionprovider/allanchors)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/scenereconstructionprovider/requiredauthorizations)
- [MeshAnchor](/documentation/arkit/meshanchor)

#### Getting mesh information

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/meshanchor/originfromanchortransform)
- [var geometry: MeshAnchor.Geometry](/documentation/arkit/meshanchor/geometry-swift.property)
- [MeshAnchor.Geometry](/documentation/arkit/meshanchor/geometry-swift.struct)

##### Inspecting mesh geometry

- [var faces: GeometryElement](/documentation/arkit/meshanchor/geometry-swift.struct/faces)
- [var vertices: GeometrySource](/documentation/arkit/meshanchor/geometry-swift.struct/vertices)
- [var normals: GeometrySource](/documentation/arkit/meshanchor/geometry-swift.struct/normals)
- [var classifications: GeometrySource?](/documentation/arkit/meshanchor/geometry-swift.struct/classifications)

##### Instance Properties

- [var description: String](/documentation/arkit/meshanchor/geometry-swift.struct/description)
- [MeshAnchor.MeshClassification](/documentation/arkit/meshanchor/meshclassification)

##### Getting architecture classifications

- [case ceiling](/documentation/arkit/meshanchor/meshclassification/ceiling)
- [case door](/documentation/arkit/meshanchor/meshclassification/door)
- [case floor](/documentation/arkit/meshanchor/meshclassification/floor)
- [case stairs](/documentation/arkit/meshanchor/meshclassification/stairs)
- [case wall](/documentation/arkit/meshanchor/meshclassification/wall)
- [case window](/documentation/arkit/meshanchor/meshclassification/window)

##### Getting furniture classifications

- [case bed](/documentation/arkit/meshanchor/meshclassification/bed)
- [case cabinet](/documentation/arkit/meshanchor/meshclassification/cabinet)
- [case homeAppliance](/documentation/arkit/meshanchor/meshclassification/homeappliance)
- [case seat](/documentation/arkit/meshanchor/meshclassification/seat)
- [case table](/documentation/arkit/meshanchor/meshclassification/table)

##### Getting decoration classifications

- [case plant](/documentation/arkit/meshanchor/meshclassification/plant)
- [case tv](/documentation/arkit/meshanchor/meshclassification/tv)

##### Getting unknown classifications

- [case none](/documentation/arkit/meshanchor/meshclassification/none)

#### Inspecting mesh anchors

- [var id: UUID](/documentation/arkit/meshanchor/id)
- [var description: String](/documentation/arkit/meshanchor/description)

### Image tracking

- [Tracking and altering images](/documentation/arkit/tracking-and-altering-images)
- [Detecting Images in an AR Experience](/documentation/arkit/detecting-images-in-an-ar-experience)
- [Tracking preregistered images in 3D space](/documentation/visionos/tracking-images-in-3d-space)
- [ImageTrackingProvider](/documentation/arkit/imagetrackingprovider)

#### Creating an image-tracking provider

- [init(referenceImages: [ReferenceImage])](/documentation/arkit/imagetrackingprovider/init(referenceimages:))
- [static var isSupported: Bool](/documentation/arkit/imagetrackingprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/imagetrackingprovider/requiredauthorizations)

#### Tracking images

- [var anchorUpdates: AnchorUpdateSequence<ImageAnchor>](/documentation/arkit/imagetrackingprovider/anchorupdates)

#### Inspecting an image-tracking provider

- [var state: DataProviderState](/documentation/arkit/imagetrackingprovider/state)
- [var description: String](/documentation/arkit/imagetrackingprovider/description)
- [var allAnchors: [ImageAnchor]](/documentation/arkit/imagetrackingprovider/allanchors)
- [ImageAnchor](/documentation/arkit/imageanchor)

#### Getting image information

- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/imageanchor/originfromanchortransform)
- [var referenceImage: ReferenceImage](/documentation/arkit/imageanchor/referenceimage)
- [var estimatedScaleFactor: Float](/documentation/arkit/imageanchor/estimatedscalefactor)
- [var isTracked: Bool](/documentation/arkit/imageanchor/istracked)
- [var description: String](/documentation/arkit/imageanchor/description)
- [var id: UUID](/documentation/arkit/imageanchor/id)
- [ReferenceImage](/documentation/arkit/referenceimage)

#### Creating a reference image

- [init(cgimage: CGImage, physicalSize: CGSize, orientation: CGImagePropertyOrientation)](/documentation/arkit/referenceimage/init(cgimage:physicalsize:orientation:))
- [init(pixelBuffer: CVPixelBuffer, physicalSize: CGSize, orientation: CGImagePropertyOrientation)](/documentation/arkit/referenceimage/init(pixelbuffer:physicalsize:orientation:))
- [static func loadReferenceImages(inGroupNamed: String, bundle: Bundle?) -> [ReferenceImage]](/documentation/arkit/referenceimage/loadreferenceimages(ingroupnamed:bundle:))

#### Inspecting a reference image

- [var physicalSize: CGSize](/documentation/arkit/referenceimage/physicalsize)
- [var name: String?](/documentation/arkit/referenceimage/name)
- [var resourceGroupName: String?](/documentation/arkit/referenceimage/resourcegroupname)
- [var description: String](/documentation/arkit/referenceimage/description)

### Geometry

- [GeometryElement](/documentation/arkit/geometryelement)

#### Rendering geometry elements

- [var buffer: any MTLBuffer](/documentation/arkit/geometryelement/buffer)
- [var primitive: GeometryElement.Primitive](/documentation/arkit/geometryelement/primitive-swift.property)
- [GeometryElement.Primitive](/documentation/arkit/geometryelement/primitive-swift.enum)

##### Primitive shapes

- [case line](/documentation/arkit/geometryelement/primitive-swift.enum/line)
- [case triangle](/documentation/arkit/geometryelement/primitive-swift.enum/triangle)

##### Inspecting geometry primitives

- [var indexCount: Int](/documentation/arkit/geometryelement/primitive-swift.enum/indexcount)

##### Instance Properties

- [var description: String](/documentation/arkit/geometryelement/primitive-swift.enum/description)
- [var count: Int](/documentation/arkit/geometryelement/count)
- [var bytesPerIndex: Int](/documentation/arkit/geometryelement/bytesperindex)
- [var description: String](/documentation/arkit/geometryelement/description)
- [GeometrySource](/documentation/arkit/geometrysource)

#### Inspecting geometry data

- [var buffer: any MTLBuffer](/documentation/arkit/geometrysource/buffer)
- [var count: Int](/documentation/arkit/geometrysource/count)
- [var format: MTLVertexFormat](/documentation/arkit/geometrysource/format)
- [var componentsPerVector: Int](/documentation/arkit/geometrysource/componentspervector)
- [var offset: Int](/documentation/arkit/geometrysource/offset)
- [var stride: Int](/documentation/arkit/geometrysource/stride)
- [var description: String](/documentation/arkit/geometrysource/description)

### Lighting estimation

- [EnvironmentLightEstimationProvider](/documentation/arkit/environmentlightestimationprovider)

#### Creating an environment light estimation provider

- [convenience init()](/documentation/arkit/environmentlightestimationprovider/init())

#### Inspecting the environment light estimation provider

- [var anchorUpdates: AnchorUpdateSequence<EnvironmentProbeAnchor>](/documentation/arkit/environmentlightestimationprovider/anchorupdates)
- [var description: String](/documentation/arkit/environmentlightestimationprovider/description)
- [var state: DataProviderState](/documentation/arkit/environmentlightestimationprovider/state)

#### Type properties

- [static var isSupported: Bool](/documentation/arkit/environmentlightestimationprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/environmentlightestimationprovider/requiredauthorizations)
- [EnvironmentProbeAnchor](/documentation/arkit/environmentprobeanchor)

#### Getting anchor information

- [var environmentTexture: (any MTLTexture)?](/documentation/arkit/environmentprobeanchor/environmenttexture)
- [var cameraScaleReference: Float](/documentation/arkit/environmentprobeanchor/camerascalereference)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/environmentprobeanchor/originfromanchortransform)

#### Comparing environment probe anchors

- [var id: UUID](/documentation/arkit/environmentprobeanchor/id)
- [var description: String](/documentation/arkit/environmentprobeanchor/description)

### Object tracking

- [ObjectTrackingProvider](/documentation/arkit/objecttrackingprovider)

#### Creating an object-tracking provider

- [init(referenceObjects: [ReferenceObject], trackingConfiguration: ObjectTrackingProvider.TrackingConfiguration?)](/documentation/arkit/objecttrackingprovider/init(referenceobjects:trackingconfiguration:))

#### Checking availability

- [static var isSupported: Bool](/documentation/arkit/objecttrackingprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/objecttrackingprovider/requiredauthorizations)

#### Configuring object-tracking

- [var trackingConfiguration: ObjectTrackingProvider.TrackingConfiguration](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.property)
- [ObjectTrackingProvider.TrackingConfiguration](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct)

##### Creating a tracking configuration

- [init()](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/init())

##### Inspecting a tracking configuration

- [var detectionRate: Float](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/detectionrate)
- [var maximumInstancesPerReferenceObject: Int](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/maximuminstancesperreferenceobject)
- [var maximumTrackableInstances: Int](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/maximumtrackableinstances)
- [var movingObjectTrackingRate: Float](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/movingobjecttrackingrate)
- [var stationaryObjectTrackingRate: Float](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/stationaryobjecttrackingrate)

##### Instance Properties

- [var description: String](/documentation/arkit/objecttrackingprovider/trackingconfiguration-swift.struct/description)

#### Inspecting an object-tracking provider

- [var state: DataProviderState](/documentation/arkit/objecttrackingprovider/state)
- [var allAnchors: [ObjectAnchor]](/documentation/arkit/objecttrackingprovider/allanchors)
- [var anchorUpdates: AnchorUpdateSequence<ObjectAnchor>](/documentation/arkit/objecttrackingprovider/anchorupdates)
- [ObjectTrackingProvider.Error](/documentation/arkit/objecttrackingprovider/error)

##### Describing an error

- [var code: ObjectTrackingProvider.Error.Code](/documentation/arkit/objecttrackingprovider/error/code-swift.property)
- [ObjectTrackingProvider.Error.Code](/documentation/arkit/objecttrackingprovider/error/code-swift.enum)

###### Error codes

- [case referenceObjectLoadingFailed](/documentation/arkit/objecttrackingprovider/error/code-swift.enum/referenceobjectloadingfailed)

###### Instance Properties

- [var description: String](/documentation/arkit/objecttrackingprovider/error/code-swift.enum/description)
- [var errorDescription: String?](/documentation/arkit/objecttrackingprovider/error/errordescription)
- [var failureReason: String?](/documentation/arkit/objecttrackingprovider/error/failurereason)

##### Inspecting an error

- [let bundle: Bundle?](/documentation/arkit/objecttrackingprovider/error/bundle)
- [let name: String?](/documentation/arkit/objecttrackingprovider/error/name)
- [var recoverySuggestion: String?](/documentation/arkit/objecttrackingprovider/error/recoverysuggestion)
- [let url: URL?](/documentation/arkit/objecttrackingprovider/error/url)

##### Instance Properties

- [var description: String](/documentation/arkit/objecttrackingprovider/error/description)
- [var description: String](/documentation/arkit/objecttrackingprovider/description)
- [ObjectAnchor](/documentation/arkit/objectanchor)

#### Inspecting an object anchor

- [var boundingBox: ObjectAnchor.AxisAlignedBoundingBox](/documentation/arkit/objectanchor/boundingbox)
- [ObjectAnchor.AxisAlignedBoundingBox](/documentation/arkit/objectanchor/axisalignedboundingbox)

##### Inspecting the bounding box

- [var center: SIMD3<Float>](/documentation/arkit/objectanchor/axisalignedboundingbox/center)
- [var extent: SIMD3<Float>](/documentation/arkit/objectanchor/axisalignedboundingbox/extent)
- [var max: SIMD3<Float>](/documentation/arkit/objectanchor/axisalignedboundingbox/max)
- [var min: SIMD3<Float>](/documentation/arkit/objectanchor/axisalignedboundingbox/min)
- [var description: String](/documentation/arkit/objectanchor/description)
- [var isTracked: Bool](/documentation/arkit/objectanchor/istracked)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/objectanchor/originfromanchortransform)
- [var referenceObject: ReferenceObject](/documentation/arkit/objectanchor/referenceobject)
- [var inputFile: URL?](/documentation/arkit/referenceobject/inputfile)
- [var usdzFile: URL?](/documentation/arkit/referenceobject/usdzfile)
- [ReferenceObject](/documentation/arkit/referenceobject)

##### Creating reference objects

- [init(from: URL) async throws](/documentation/arkit/referenceobject/init(from:))
- [init(named: String, from: Bundle?) async throws](/documentation/arkit/referenceobject/init(named:from:))

##### Inspecting a reference object

- [var id: UUID](/documentation/arkit/referenceobject/id-swift.property)
- [ReferenceObject.ID](/documentation/arkit/referenceobject/id-swift.typealias)
- [var inputFile: URL?](/documentation/arkit/referenceobject/inputfile)
- [var usdzFile: URL?](/documentation/arkit/referenceobject/usdzfile)
- [var name: String](/documentation/arkit/referenceobject/name)
- [var description: String](/documentation/arkit/referenceobject/description)

#### Inspecting and comparing anchors

- [var id: UUID](/documentation/arkit/objectanchor/id-swift.property)
- [ObjectAnchor.ID](/documentation/arkit/objectanchor/id-swift.typealias)
- [Exploring object tracking with ARKit](/documentation/visionos/exploring_object_tracking_with_arkit)
- [Implementing object tracking in your visionOS app](/documentation/visionos/implementing-object-tracking-in-your-visionos-app)

### Accessory tracking

- [AccessoryTrackingProvider](/documentation/arkit/accessorytrackingprovider)

#### Structures

- [AccessoryTrackingProvider.Error](/documentation/arkit/accessorytrackingprovider/error)

##### Instance Properties

- [var code: AccessoryTrackingProvider.Error.Code](/documentation/arkit/accessorytrackingprovider/error/code-swift.property)
- [var description: String](/documentation/arkit/accessorytrackingprovider/error/description)
- [var errorDescription: String?](/documentation/arkit/accessorytrackingprovider/error/errordescription)
- [var failureReason: String?](/documentation/arkit/accessorytrackingprovider/error/failurereason)
- [var recoverySuggestion: String?](/documentation/arkit/accessorytrackingprovider/error/recoverysuggestion)
- [let source: Accessory.Source?](/documentation/arkit/accessorytrackingprovider/error/source)

##### Enumerations

- [AccessoryTrackingProvider.Error.Code](/documentation/arkit/accessorytrackingprovider/error/code-swift.enum)

###### Enumeration Cases

- [case accessoryLoadingFailed](/documentation/arkit/accessorytrackingprovider/error/code-swift.enum/accessoryloadingfailed)

###### Instance Properties

- [var description: String](/documentation/arkit/accessorytrackingprovider/error/code-swift.enum/description)

#### Initializers

- [convenience init(accessories: [Accessory])](/documentation/arkit/accessorytrackingprovider/init(accessories:))

#### Instance Properties

- [var anchorUpdates: AnchorUpdateSequence<AccessoryAnchor>](/documentation/arkit/accessorytrackingprovider/anchorupdates)
- [var description: String](/documentation/arkit/accessorytrackingprovider/description)
- [var latestAnchors: [AccessoryAnchor]](/documentation/arkit/accessorytrackingprovider/latestanchors)
- [var state: DataProviderState](/documentation/arkit/accessorytrackingprovider/state)

#### Instance Methods

- [func predictAnchor(for: AccessoryAnchor, at: TimeInterval) -> AccessoryAnchor?](/documentation/arkit/accessorytrackingprovider/predictanchor(for:at:))

#### Type Properties

- [static var isSupported: Bool](/documentation/arkit/accessorytrackingprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/accessorytrackingprovider/requiredauthorizations)
- [Accessory](/documentation/arkit/accessory)

#### Structures

- [Accessory.LocationName](/documentation/arkit/accessory/locationname)

##### Initializers

- [init(String)](/documentation/arkit/accessory/locationname/init(_:))
- [init(rawValue: String)](/documentation/arkit/accessory/locationname/init(rawvalue:))

##### Instance Properties

- [var description: String](/documentation/arkit/accessory/locationname/description)
- [let rawValue: String](/documentation/arkit/accessory/locationname/rawvalue)

##### Type Properties

- [static let aim: Accessory.LocationName](/documentation/arkit/accessory/locationname/aim)
- [static let grip: Accessory.LocationName](/documentation/arkit/accessory/locationname/grip)
- [static let gripSurface: Accessory.LocationName](/documentation/arkit/accessory/locationname/gripsurface)

#### Initializers

- [init(device: any GCDevice) async throws](/documentation/arkit/accessory/init(device:))

#### Instance Properties

- [var description: String](/documentation/arkit/accessory/description)
- [var id: UUID](/documentation/arkit/accessory/id)
- [var inherentChirality: Accessory.Chirality](/documentation/arkit/accessory/inherentchirality)
- [var locations: [Accessory.LocationName]](/documentation/arkit/accessory/locations)
- [var name: String](/documentation/arkit/accessory/name)
- [var source: Accessory.Source](/documentation/arkit/accessory/source-swift.property)
- [var usdzFile: URL?](/documentation/arkit/accessory/usdzfile)

#### Enumerations

- [Accessory.Chirality](/documentation/arkit/accessory/chirality)

##### Enumeration Cases

- [case left](/documentation/arkit/accessory/chirality/left)
- [case right](/documentation/arkit/accessory/chirality/right)
- [case unspecified](/documentation/arkit/accessory/chirality/unspecified)

##### Instance Properties

- [var description: String](/documentation/arkit/accessory/chirality/description)
- [Accessory.Source](/documentation/arkit/accessory/source-swift.enum)

##### Enumeration Cases

- [case device(any GCDevice)](/documentation/arkit/accessory/source-swift.enum/device(_:))

##### Instance Properties

- [var description: String](/documentation/arkit/accessory/source-swift.enum/description)
- [AccessoryAnchor](/documentation/arkit/accessoryanchor)

#### Instance Properties

- [var accessory: Accessory](/documentation/arkit/accessoryanchor/accessory)
- [var angularVelocity: SIMD3<Float>](/documentation/arkit/accessoryanchor/angularvelocity)
- [var description: String](/documentation/arkit/accessoryanchor/description)
- [var heldChirality: Accessory.Chirality?](/documentation/arkit/accessoryanchor/heldchirality)
- [var id: UUID](/documentation/arkit/accessoryanchor/id)
- [var isTracked: Bool](/documentation/arkit/accessoryanchor/istracked)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/accessoryanchor/originfromanchortransform)
- [var trackingState: AccessoryAnchor.TrackingState](/documentation/arkit/accessoryanchor/trackingstate-swift.property)
- [var velocity: SIMD3<Float>](/documentation/arkit/accessoryanchor/velocity)

#### Instance Methods

- [func coordinateSpace(correction: ARKitCoordinateSpace.Correction) -> ARKitCoordinateSpace](/documentation/arkit/accessoryanchor/coordinatespace(correction:))
- [func coordinateSpace(for: Accessory.LocationName, correction: ARKitCoordinateSpace.Correction) -> ARKitCoordinateSpace](/documentation/arkit/accessoryanchor/coordinatespace(for:correction:))

#### Enumerations

- [AccessoryAnchor.TrackingState](/documentation/arkit/accessoryanchor/trackingstate-swift.enum)

##### Enumeration Cases

- [case orientationTracked](/documentation/arkit/accessoryanchor/trackingstate-swift.enum/orientationtracked)
- [case positionOrientationTracked](/documentation/arkit/accessoryanchor/trackingstate-swift.enum/positionorientationtracked)
- [case positionOrientationTrackedLowAccuracy](/documentation/arkit/accessoryanchor/trackingstate-swift.enum/positionorientationtrackedlowaccuracy)
- [case untracked](/documentation/arkit/accessoryanchor/trackingstate-swift.enum/untracked)
- [Tracking accessories in volumetric windows](/documentation/arkit/tracking-accessories-in-volumetric-windows)
- [Tracking a handheld accessory as a virtual sculpting tool](/documentation/arkit/tracking-a-handheld-accessory-as-a-virtual-sculpting-tool)

### Room tracking

- [RoomTrackingProvider](/documentation/arkit/roomtrackingprovider)

#### Creating a room-tracking provider

- [init()](/documentation/arkit/roomtrackingprovider/init())

#### Inspecting a room-tracking provider

- [var allAnchors: [RoomAnchor]](/documentation/arkit/roomtrackingprovider/allanchors)
- [var anchorUpdates: AnchorUpdateSequence<RoomAnchor>](/documentation/arkit/roomtrackingprovider/anchorupdates)
- [var currentRoomAnchor: RoomAnchor?](/documentation/arkit/roomtrackingprovider/currentroomanchor)
- [var description: String](/documentation/arkit/roomtrackingprovider/description)
- [var state: DataProviderState](/documentation/arkit/roomtrackingprovider/state)

#### Type properties

- [static var isSupported: Bool](/documentation/arkit/roomtrackingprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/roomtrackingprovider/requiredauthorizations)
- [RoomAnchor](/documentation/arkit/roomanchor)

#### Getting information about a room anchor

- [var geometry: MeshAnchor.Geometry](/documentation/arkit/roomanchor/geometry)
- [var id: UUID](/documentation/arkit/roomanchor/id)
- [var isCurrentRoom: Bool](/documentation/arkit/roomanchor/iscurrentroom)
- [var meshAnchorIDs: [UUID]](/documentation/arkit/roomanchor/meshanchorids)
- [var originFromAnchorTransform: simd_float4x4](/documentation/arkit/roomanchor/originfromanchortransform)
- [var planeAnchorIDs: [UUID]](/documentation/arkit/roomanchor/planeanchorids)

#### Inspecting a room anchor

- [func contains(SIMD3<Float>) -> Bool](/documentation/arkit/roomanchor/contains(_:))
- [func geometries(of: MeshAnchor.MeshClassification) -> [MeshAnchor.Geometry]](/documentation/arkit/roomanchor/geometries(of:))
- [var description: String](/documentation/arkit/roomanchor/description)

#### Instance Methods

- [func geometries(classifiedAs: SurfaceClassification) -> [MeshAnchor.Geometry]](/documentation/arkit/roomanchor/geometries(classifiedas:))
- [SurfaceClassification](/documentation/arkit/surfaceclassification)

#### Enumeration Cases

- [case bed](/documentation/arkit/surfaceclassification/bed)
- [case cabinet](/documentation/arkit/surfaceclassification/cabinet)
- [case ceiling](/documentation/arkit/surfaceclassification/ceiling)
- [case door](/documentation/arkit/surfaceclassification/door)
- [case floor](/documentation/arkit/surfaceclassification/floor)
- [case homeAppliance](/documentation/arkit/surfaceclassification/homeappliance)
- [case none](/documentation/arkit/surfaceclassification/none)
- [case plant](/documentation/arkit/surfaceclassification/plant)
- [case seat](/documentation/arkit/surfaceclassification/seat)
- [case stairs](/documentation/arkit/surfaceclassification/stairs)
- [case table](/documentation/arkit/surfaceclassification/table)
- [case tv](/documentation/arkit/surfaceclassification/tv)
- [case wall](/documentation/arkit/surfaceclassification/wall)
- [case window](/documentation/arkit/surfaceclassification/window)

#### Instance Properties

- [var description: String](/documentation/arkit/surfaceclassification/description)
- [Building local experiences with room tracking](/documentation/visionos/building-local-experiences-with-room-tracking)

### Shared coordinate spaces

- [SharedCoordinateSpaceProvider](/documentation/arkit/sharedcoordinatespaceprovider)

#### Structures

- [SharedCoordinateSpaceProvider.CoordinateSpaceData](/documentation/arkit/sharedcoordinatespaceprovider/coordinatespacedata)

##### Initializers

- [init?(data: Data)](/documentation/arkit/sharedcoordinatespaceprovider/coordinatespacedata/init(data:))

##### Instance Properties

- [var data: Data](/documentation/arkit/sharedcoordinatespaceprovider/coordinatespacedata/data)
- [var recipientIdentifiers: [UUID]](/documentation/arkit/sharedcoordinatespaceprovider/coordinatespacedata/recipientidentifiers)

#### Initializers

- [init()](/documentation/arkit/sharedcoordinatespaceprovider/init())

#### Instance Properties

- [var description: String](/documentation/arkit/sharedcoordinatespaceprovider/description)
- [var eventUpdates: some AsyncSequence<SharedCoordinateSpaceProvider.Event, Never>](/documentation/arkit/sharedcoordinatespaceprovider/eventupdates)
- [var nextCoordinateSpaceData: SharedCoordinateSpaceProvider.CoordinateSpaceData?](/documentation/arkit/sharedcoordinatespaceprovider/nextcoordinatespacedata)
- [var participantIdentifier: UUID](/documentation/arkit/sharedcoordinatespaceprovider/participantidentifier)
- [var state: DataProviderState](/documentation/arkit/sharedcoordinatespaceprovider/state)

#### Instance Methods

- [func push(data: SharedCoordinateSpaceProvider.CoordinateSpaceData)](/documentation/arkit/sharedcoordinatespaceprovider/push(data:))

#### Type Properties

- [static var isSupported: Bool](/documentation/arkit/sharedcoordinatespaceprovider/issupported)
- [static var requiredAuthorizations: [ARKitSession.AuthorizationType]](/documentation/arkit/sharedcoordinatespaceprovider/requiredauthorizations)

#### Enumerations

- [SharedCoordinateSpaceProvider.Event](/documentation/arkit/sharedcoordinatespaceprovider/event)

##### Enumeration Cases

- [case connectedParticipantIdentifiers(participants: [UUID])](/documentation/arkit/sharedcoordinatespaceprovider/event/connectedparticipantidentifiers(participants:))
- [case sharingDisabled](/documentation/arkit/sharedcoordinatespaceprovider/event/sharingdisabled)
- [case sharingEnabled](/documentation/arkit/sharedcoordinatespaceprovider/event/sharingenabled)

##### Instance Properties

- [var description: String](/documentation/arkit/sharedcoordinatespaceprovider/event/description)

## iOS

- [Verifying Device Support and User Permission](/documentation/arkit/verifying-device-support-and-user-permission)
- [ARSession](/documentation/arkit/arsession)

### Configuring and running a session

- [func run(ARConfiguration, options: ARSession.RunOptions)](/documentation/arkit/arsession/run(_:options:))
- [var identifier: UUID](/documentation/arkit/arsession/identifier)
- [ARSession.RunOptions](/documentation/arkit/arsession/runoptions)

#### Creating Run Options

- [init(rawValue: UInt)](/documentation/arkit/arsession/runoptions/init(rawvalue:))

#### Run Options

- [static var resetTracking: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/resettracking)
- [static var removeExistingAnchors: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/removeexistinganchors)
- [static var stopTrackedRaycasts: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/stoptrackedraycasts)
- [static var resetSceneReconstruction: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/resetscenereconstruction)
- [var configuration: ARConfiguration?](/documentation/arkit/arsession/configuration)
- [func pause()](/documentation/arkit/arsession/pause())

### Responding to events

- [var delegate: (any ARSessionDelegate)?](/documentation/arkit/arsession/delegate)
- [var delegateQueue: dispatch_queue_t?](/documentation/arkit/arsession/delegatequeue)
- [ARSessionDelegate](/documentation/arkit/arsessiondelegate)

#### Receiving Camera Frames

- [func session(ARSession, didUpdate: ARFrame)](/documentation/arkit/arsessiondelegate/session(_:didupdate:)-9v2kw)

#### Handling Content Updates

- [func session(ARSession, didAdd: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didadd:))
- [func session(ARSession, didUpdate: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didupdate:)-3qtt8)
- [func session(ARSession, didRemove: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didremove:))
- [ARSessionObserver](/documentation/arkit/arsessionobserver)

#### Responding to Tracking Quality Changes

- [func session(ARSession, cameraDidChangeTrackingState: ARCamera)](/documentation/arkit/arsessionobserver/session(_:cameradidchangetrackingstate:))
- [func session(ARSession, didChange: ARGeoTrackingStatus)](/documentation/arkit/arsessionobserver/session(_:didchange:))

#### Handling Interruptions

- [func sessionWasInterrupted(ARSession)](/documentation/arkit/arsessionobserver/sessionwasinterrupted(_:))
- [func sessionInterruptionEnded(ARSession)](/documentation/arkit/arsessionobserver/sessioninterruptionended(_:))
- [func sessionShouldAttemptRelocalization(ARSession) -> Bool](/documentation/arkit/arsessionobserver/sessionshouldattemptrelocalization(_:))

#### Receiving Audio Data

- [func session(ARSession, didOutputAudioSampleBuffer: CMSampleBuffer)](/documentation/arkit/arsessionobserver/session(_:didoutputaudiosamplebuffer:))

#### Handling Errors

- [func session(ARSession, didFailWithError: any Error)](/documentation/arkit/arsessionobserver/session(_:didfailwitherror:))
- [let ARErrorDomain: String](/documentation/arkit/arerrordomain)

#### Managing Collaboration

- [func session(ARSession, didOutputCollaborationData: ARSession.CollaborationData)](/documentation/arkit/arsessionobserver/session(_:didoutputcollaborationdata:))

### Managing anchors

- [func add(anchor: ARAnchor)](/documentation/arkit/arsession/add(anchor:))
- [func remove(anchor: ARAnchor)](/documentation/arkit/arsession/remove(anchor:))

### Saving or sharing state

- [func getCurrentWorldMap(completionHandler: (ARWorldMap?, (any Error)?) -> Void)](/documentation/arkit/arsession/getcurrentworldmap(completionhandler:))
- [Recording and Replaying AR Session Data](/documentation/arkit/recording-and-replaying-ar-session-data)

### Scanning 3D objects

- [func createReferenceObject(transform: simd_float4x4, center: simd_float3, extent: simd_float3, completionHandler: (ARReferenceObject?, (any Error)?) -> Void)](/documentation/arkit/arsession/createreferenceobject(transform:center:extent:completionhandler:))

### Updating the world origin

- [func setWorldOrigin(relativeTransform: simd_float4x4)](/documentation/arkit/arsession/setworldorigin(relativetransform:))

### Finding real-world surfaces

- [func raycast(ARRaycastQuery) -> [ARRaycastResult]](/documentation/arkit/arsession/raycast(_:))
- [func trackedRaycast(ARRaycastQuery, updateHandler: ([ARRaycastResult]) -> Void) -> ARTrackedRaycast?](/documentation/arkit/arsession/trackedraycast(_:updatehandler:))

### Converting local coordinates to geographic coordinates

- [func getGeoLocation(forPoint: simd_float3, completionHandler: (CLLocationCoordinate2D, CLLocationDistance, (any Error)?) -> Void)](/documentation/arkit/arsession/getgeolocation(forpoint:completionhandler:))

### Accessing the camera frame

- [var currentFrame: ARFrame?](/documentation/arkit/arsession/currentframe)
- [ARFrame](/documentation/arkit/arframe)

#### Accessing camera data

- [var camera: ARCamera](/documentation/arkit/arframe/camera)
- [var capturedImage: CVPixelBuffer](/documentation/arkit/arframe/capturedimage)
- [var timestamp: TimeInterval](/documentation/arkit/arframe/timestamp)
- [var cameraGrainIntensity: Float](/documentation/arkit/arframe/cameragrainintensity)
- [var cameraGrainTexture: (any MTLTexture)?](/documentation/arkit/arframe/cameragraintexture)
- [var exifData: [String : Any]](/documentation/arkit/arframe/exifdata)

#### Accessing scene data

- [var lightEstimate: ARLightEstimate?](/documentation/arkit/arframe/lightestimate)
- [func displayTransform(for: UIInterfaceOrientation, viewportSize: CGSize) -> CGAffineTransform](/documentation/arkit/arframe/displaytransform(for:viewportsize:))
- [var rawFeaturePoints: ARPointCloud?](/documentation/arkit/arframe/rawfeaturepoints)
- [var capturedDepthData: AVDepthData?](/documentation/arkit/arframe/captureddepthdata)
- [var capturedDepthDataTimestamp: TimeInterval](/documentation/arkit/arframe/captureddepthdatatimestamp)
- [var sceneDepth: ARDepthData?](/documentation/arkit/arframe/scenedepth)
- [var smoothedSceneDepth: ARDepthData?](/documentation/arkit/arframe/smoothedscenedepth)

#### Tracking and interacting with the real world

- [var anchors: [ARAnchor]](/documentation/arkit/arframe/anchors)
- [func raycastQuery(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> ARRaycastQuery](/documentation/arkit/arframe/raycastquery(from:allowing:alignment:))
- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/arkit/arframe/hittest(_:types:))

#### Checking world-mapping status

- [var worldMappingStatus: ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.property)
- [ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.enum)

##### Enumeration Cases

- [case extending](/documentation/arkit/arframe/worldmappingstatus-swift.enum/extending)
- [case limited](/documentation/arkit/arframe/worldmappingstatus-swift.enum/limited)
- [case mapped](/documentation/arkit/arframe/worldmappingstatus-swift.enum/mapped)
- [case notAvailable](/documentation/arkit/arframe/worldmappingstatus-swift.enum/notavailable)

##### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arframe/worldmappingstatus-swift.enum/init(rawvalue:))

#### Checking for people

- [var detectedBody: ARBody2D?](/documentation/arkit/arframe/detectedbody)
- [ARBody2D](/documentation/arkit/arbody2d)

##### Getting Joint Information

- [var skeleton: ARSkeleton2D](/documentation/arkit/arbody2d/skeleton)
- [var segmentationBuffer: CVPixelBuffer?](/documentation/arkit/arframe/segmentationbuffer)
- [var estimatedDepthData: CVPixelBuffer?](/documentation/arkit/arframe/estimateddepthdata)
- [ARFrame.SegmentationClass](/documentation/arkit/arframe/segmentationclass)

##### Classifying Pixels

- [case person](/documentation/arkit/arframe/segmentationclass/person)
- [case none](/documentation/arkit/arframe/segmentationclass/none)

##### Initializers

- [init?(rawValue: UInt8)](/documentation/arkit/arframe/segmentationclass/init(rawvalue:))

#### Assessing geo-tracking condition

- [var geoTrackingStatus: ARGeoTrackingStatus?](/documentation/arkit/arframe/geotrackingstatus)
- [ARGeoTrackingStatus](/documentation/arkit/argeotrackingstatus)

##### Checking State

- [var state: ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.property)
- [ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.enum)

###### States

- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)
- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/state-swift.enum/init(rawvalue:))

##### Determining the Reason

- [var stateReason: ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.property)
- [ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.enum)

###### Status Reasons

- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)
- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/init(rawvalue:))

##### Judging Accuracy

- [var accuracy: ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.property)
- [ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum)

###### Accuracies

- [case high](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/high)
- [case undetermined](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/undetermined)
- [case low](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/low)
- [case medium](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/medium)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/init(rawvalue:))
- [func captureHighResolutionFrame(completion: (ARFrame?, (any Error)?) -> Void)](/documentation/arkit/arsession/capturehighresolutionframe(completion:))

### Managing collaboration

- [func update(with: ARSession.CollaborationData)](/documentation/arkit/arsession/update(with:))
- [ARSession.CollaborationData](/documentation/arkit/arsession/collaborationdata)

#### Observing Priority

- [var priority: ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.property)
- [ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.enum)

##### Enumeration Cases

- [case critical](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/critical)
- [case optional](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/optional)

##### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/init(rawvalue:))

### Providing a session

- [ARSessionProviding](/documentation/arkit/arsessionproviding)

#### Providing a Session

- [var session: ARSession](/documentation/arkit/arsessionproviding/session)

### Instance Methods

- [func captureHighResolutionFrame(using: AVCapturePhotoSettings?, completion: (ARFrame?, (any Error)?) -> Void)](/documentation/arkit/arsession/capturehighresolutionframe(using:completion:))
- [ARAnchor](/documentation/arkit/aranchor)

### Creating Anchors

- [init(transform: simd_float4x4)](/documentation/arkit/aranchor/init(transform:))
- [init(name: String, transform: simd_float4x4)](/documentation/arkit/aranchor/init(name:transform:))
- [var name: String?](/documentation/arkit/aranchor/name)

### Tracking Anchors

- [var identifier: UUID](/documentation/arkit/aranchor/identifier)
- [var sessionIdentifier: UUID?](/documentation/arkit/aranchor/sessionidentifier)
- [var transform: simd_float4x4](/documentation/arkit/aranchor/transform)
- [ARKit in iOS](/documentation/arkit/arkit-in-ios)

### Essentials

- [Verifying Device Support and User Permission](/documentation/arkit/verifying-device-support-and-user-permission)
- [OpenUSD schemas for AR](/documentation/usd/usd-schemas-for-ar)

### Setup

- [Choosing Which Camera Feed to Augment](/documentation/arkit/choosing-which-camera-feed-to-augment)
- [Managing Session Life Cycle and Tracking Quality](/documentation/arkit/managing-session-life-cycle-and-tracking-quality)
- [Displaying an AR Experience with Metal](/documentation/arkit/displaying-an-ar-experience-with-metal)
- [ARSession](/documentation/arkit/arsession)

#### Configuring and running a session

- [func run(ARConfiguration, options: ARSession.RunOptions)](/documentation/arkit/arsession/run(_:options:))
- [var identifier: UUID](/documentation/arkit/arsession/identifier)
- [ARSession.RunOptions](/documentation/arkit/arsession/runoptions)

##### Creating Run Options

- [init(rawValue: UInt)](/documentation/arkit/arsession/runoptions/init(rawvalue:))

##### Run Options

- [static var resetTracking: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/resettracking)
- [static var removeExistingAnchors: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/removeexistinganchors)
- [static var stopTrackedRaycasts: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/stoptrackedraycasts)
- [static var resetSceneReconstruction: ARSession.RunOptions](/documentation/arkit/arsession/runoptions/resetscenereconstruction)
- [var configuration: ARConfiguration?](/documentation/arkit/arsession/configuration)
- [func pause()](/documentation/arkit/arsession/pause())

#### Responding to events

- [var delegate: (any ARSessionDelegate)?](/documentation/arkit/arsession/delegate)
- [var delegateQueue: dispatch_queue_t?](/documentation/arkit/arsession/delegatequeue)
- [ARSessionDelegate](/documentation/arkit/arsessiondelegate)

##### Receiving Camera Frames

- [func session(ARSession, didUpdate: ARFrame)](/documentation/arkit/arsessiondelegate/session(_:didupdate:)-9v2kw)

##### Handling Content Updates

- [func session(ARSession, didAdd: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didadd:))
- [func session(ARSession, didUpdate: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didupdate:)-3qtt8)
- [func session(ARSession, didRemove: [ARAnchor])](/documentation/arkit/arsessiondelegate/session(_:didremove:))
- [ARSessionObserver](/documentation/arkit/arsessionobserver)

##### Responding to Tracking Quality Changes

- [func session(ARSession, cameraDidChangeTrackingState: ARCamera)](/documentation/arkit/arsessionobserver/session(_:cameradidchangetrackingstate:))
- [func session(ARSession, didChange: ARGeoTrackingStatus)](/documentation/arkit/arsessionobserver/session(_:didchange:))

##### Handling Interruptions

- [func sessionWasInterrupted(ARSession)](/documentation/arkit/arsessionobserver/sessionwasinterrupted(_:))
- [func sessionInterruptionEnded(ARSession)](/documentation/arkit/arsessionobserver/sessioninterruptionended(_:))
- [func sessionShouldAttemptRelocalization(ARSession) -> Bool](/documentation/arkit/arsessionobserver/sessionshouldattemptrelocalization(_:))

##### Receiving Audio Data

- [func session(ARSession, didOutputAudioSampleBuffer: CMSampleBuffer)](/documentation/arkit/arsessionobserver/session(_:didoutputaudiosamplebuffer:))

##### Handling Errors

- [func session(ARSession, didFailWithError: any Error)](/documentation/arkit/arsessionobserver/session(_:didfailwitherror:))
- [let ARErrorDomain: String](/documentation/arkit/arerrordomain)

##### Managing Collaboration

- [func session(ARSession, didOutputCollaborationData: ARSession.CollaborationData)](/documentation/arkit/arsessionobserver/session(_:didoutputcollaborationdata:))

#### Managing anchors

- [func add(anchor: ARAnchor)](/documentation/arkit/arsession/add(anchor:))
- [func remove(anchor: ARAnchor)](/documentation/arkit/arsession/remove(anchor:))

#### Saving or sharing state

- [func getCurrentWorldMap(completionHandler: (ARWorldMap?, (any Error)?) -> Void)](/documentation/arkit/arsession/getcurrentworldmap(completionhandler:))
- [Recording and Replaying AR Session Data](/documentation/arkit/recording-and-replaying-ar-session-data)

#### Scanning 3D objects

- [func createReferenceObject(transform: simd_float4x4, center: simd_float3, extent: simd_float3, completionHandler: (ARReferenceObject?, (any Error)?) -> Void)](/documentation/arkit/arsession/createreferenceobject(transform:center:extent:completionhandler:))

#### Updating the world origin

- [func setWorldOrigin(relativeTransform: simd_float4x4)](/documentation/arkit/arsession/setworldorigin(relativetransform:))

#### Finding real-world surfaces

- [func raycast(ARRaycastQuery) -> [ARRaycastResult]](/documentation/arkit/arsession/raycast(_:))
- [func trackedRaycast(ARRaycastQuery, updateHandler: ([ARRaycastResult]) -> Void) -> ARTrackedRaycast?](/documentation/arkit/arsession/trackedraycast(_:updatehandler:))

#### Converting local coordinates to geographic coordinates

- [func getGeoLocation(forPoint: simd_float3, completionHandler: (CLLocationCoordinate2D, CLLocationDistance, (any Error)?) -> Void)](/documentation/arkit/arsession/getgeolocation(forpoint:completionhandler:))

#### Accessing the camera frame

- [var currentFrame: ARFrame?](/documentation/arkit/arsession/currentframe)
- [ARFrame](/documentation/arkit/arframe)

##### Accessing camera data

- [var camera: ARCamera](/documentation/arkit/arframe/camera)
- [var capturedImage: CVPixelBuffer](/documentation/arkit/arframe/capturedimage)
- [var timestamp: TimeInterval](/documentation/arkit/arframe/timestamp)
- [var cameraGrainIntensity: Float](/documentation/arkit/arframe/cameragrainintensity)
- [var cameraGrainTexture: (any MTLTexture)?](/documentation/arkit/arframe/cameragraintexture)
- [var exifData: [String : Any]](/documentation/arkit/arframe/exifdata)

##### Accessing scene data

- [var lightEstimate: ARLightEstimate?](/documentation/arkit/arframe/lightestimate)
- [func displayTransform(for: UIInterfaceOrientation, viewportSize: CGSize) -> CGAffineTransform](/documentation/arkit/arframe/displaytransform(for:viewportsize:))
- [var rawFeaturePoints: ARPointCloud?](/documentation/arkit/arframe/rawfeaturepoints)
- [var capturedDepthData: AVDepthData?](/documentation/arkit/arframe/captureddepthdata)
- [var capturedDepthDataTimestamp: TimeInterval](/documentation/arkit/arframe/captureddepthdatatimestamp)
- [var sceneDepth: ARDepthData?](/documentation/arkit/arframe/scenedepth)
- [var smoothedSceneDepth: ARDepthData?](/documentation/arkit/arframe/smoothedscenedepth)

##### Tracking and interacting with the real world

- [var anchors: [ARAnchor]](/documentation/arkit/arframe/anchors)
- [func raycastQuery(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> ARRaycastQuery](/documentation/arkit/arframe/raycastquery(from:allowing:alignment:))
- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/arkit/arframe/hittest(_:types:))

##### Checking world-mapping status

- [var worldMappingStatus: ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.property)
- [ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.enum)

###### Enumeration Cases

- [case extending](/documentation/arkit/arframe/worldmappingstatus-swift.enum/extending)
- [case limited](/documentation/arkit/arframe/worldmappingstatus-swift.enum/limited)
- [case mapped](/documentation/arkit/arframe/worldmappingstatus-swift.enum/mapped)
- [case notAvailable](/documentation/arkit/arframe/worldmappingstatus-swift.enum/notavailable)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arframe/worldmappingstatus-swift.enum/init(rawvalue:))

##### Checking for people

- [var detectedBody: ARBody2D?](/documentation/arkit/arframe/detectedbody)
- [ARBody2D](/documentation/arkit/arbody2d)

###### Getting Joint Information

- [var skeleton: ARSkeleton2D](/documentation/arkit/arbody2d/skeleton)
- [var segmentationBuffer: CVPixelBuffer?](/documentation/arkit/arframe/segmentationbuffer)
- [var estimatedDepthData: CVPixelBuffer?](/documentation/arkit/arframe/estimateddepthdata)
- [ARFrame.SegmentationClass](/documentation/arkit/arframe/segmentationclass)

###### Classifying Pixels

- [case person](/documentation/arkit/arframe/segmentationclass/person)
- [case none](/documentation/arkit/arframe/segmentationclass/none)

###### Initializers

- [init?(rawValue: UInt8)](/documentation/arkit/arframe/segmentationclass/init(rawvalue:))

##### Assessing geo-tracking condition

- [var geoTrackingStatus: ARGeoTrackingStatus?](/documentation/arkit/arframe/geotrackingstatus)
- [ARGeoTrackingStatus](/documentation/arkit/argeotrackingstatus)

###### Checking State

- [var state: ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.property)
- [ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.enum)

###### States

- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)
- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/state-swift.enum/init(rawvalue:))

###### Determining the Reason

- [var stateReason: ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.property)
- [ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.enum)

###### Status Reasons

- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)
- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/init(rawvalue:))

###### Judging Accuracy

- [var accuracy: ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.property)
- [ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum)

###### Accuracies

- [case high](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/high)
- [case undetermined](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/undetermined)
- [case low](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/low)
- [case medium](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/medium)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/init(rawvalue:))
- [func captureHighResolutionFrame(completion: (ARFrame?, (any Error)?) -> Void)](/documentation/arkit/arsession/capturehighresolutionframe(completion:))

#### Managing collaboration

- [func update(with: ARSession.CollaborationData)](/documentation/arkit/arsession/update(with:))
- [ARSession.CollaborationData](/documentation/arkit/arsession/collaborationdata)

##### Observing Priority

- [var priority: ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.property)
- [ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.enum)

###### Enumeration Cases

- [case critical](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/critical)
- [case optional](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/optional)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/init(rawvalue:))

#### Providing a session

- [ARSessionProviding](/documentation/arkit/arsessionproviding)

##### Providing a Session

- [var session: ARSession](/documentation/arkit/arsessionproviding/session)

#### Instance Methods

- [func captureHighResolutionFrame(using: AVCapturePhotoSettings?, completion: (ARFrame?, (any Error)?) -> Void)](/documentation/arkit/arsession/capturehighresolutionframe(using:completion:))
- [Configuration Objects](/documentation/arkit/configuration-objects)

#### Common Configuration Details

- [ARConfiguration](/documentation/arkit/arconfiguration)

##### Verifying device support

- [class var isSupported: Bool](/documentation/arkit/arconfiguration/issupported)

##### Enabling frame features

- [var frameSemantics: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.property)
- [ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct)

###### Creating a Feature

- [init(rawValue: UInt)](/documentation/arkit/arconfiguration/framesemantics-swift.struct/init(rawvalue:))

###### Tracking Bodies in 2D

- [static var bodyDetection: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct/bodydetection)

###### Occluding Virtual Content with People

- [static var personSegmentation: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct/personsegmentation)
- [static var personSegmentationWithDepth: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct/personsegmentationwithdepth)

###### Accessing Depth

- [static var sceneDepth: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct/scenedepth)
- [static var smoothedSceneDepth: ARConfiguration.FrameSemantics](/documentation/arkit/arconfiguration/framesemantics-swift.struct/smoothedscenedepth)
- [class func supportsFrameSemantics(ARConfiguration.FrameSemantics) -> Bool](/documentation/arkit/arconfiguration/supportsframesemantics(_:))

##### Configuring the AR session

- [var isLightEstimationEnabled: Bool](/documentation/arkit/arconfiguration/islightestimationenabled)
- [var worldAlignment: ARConfiguration.WorldAlignment](/documentation/arkit/arconfiguration/worldalignment-swift.property)
- [ARConfiguration.WorldAlignment](/documentation/arkit/arconfiguration/worldalignment-swift.enum)

###### Alignments

- [case gravity](/documentation/arkit/arconfiguration/worldalignment-swift.enum/gravity)
- [case gravityAndHeading](/documentation/arkit/arconfiguration/worldalignment-swift.enum/gravityandheading)
- [case camera](/documentation/arkit/arconfiguration/worldalignment-swift.enum/camera)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arconfiguration/worldalignment-swift.enum/init(rawvalue:))

##### Managing video capture options

- [var videoFormat: ARConfiguration.VideoFormat](/documentation/arkit/arconfiguration/videoformat-swift.property)
- [class var supportedVideoFormats: [ARConfiguration.VideoFormat]](/documentation/arkit/arconfiguration/supportedvideoformats)
- [ARConfiguration.VideoFormat](/documentation/arkit/arconfiguration/videoformat-swift.class)

###### Accessing format information

- [var framesPerSecond: Int](/documentation/arkit/arconfiguration/videoformat-swift.class/framespersecond)
- [var imageResolution: CGSize](/documentation/arkit/arconfiguration/videoformat-swift.class/imageresolution)
- [var isRecommendedForHighResolutionFrameCapturing: Bool](/documentation/arkit/arconfiguration/videoformat-swift.class/isrecommendedforhighresolutionframecapturing)
- [var isVideoHDRSupported: Bool](/documentation/arkit/arconfiguration/videoformat-swift.class/isvideohdrsupported)

###### Inspecting the video source

- [var captureDevicePosition: AVCaptureDevice.Position](/documentation/arkit/arconfiguration/videoformat-swift.class/capturedeviceposition)
- [AVCaptureDevice.Position](/documentation/avfoundation/avcapturedevice/position-swift.enum)
- [var captureDeviceType: AVCaptureDevice.DeviceType](/documentation/arkit/arconfiguration/videoformat-swift.class/capturedevicetype)

###### Instance Properties

- [var defaultColorSpace: AVCaptureColorSpace](/documentation/arkit/arconfiguration/videoformat-swift.class/defaultcolorspace)
- [var defaultPhotoSettings: AVCapturePhotoSettings](/documentation/arkit/arconfiguration/videoformat-swift.class/defaultphotosettings)
- [var videoHDRAllowed: Bool](/documentation/arkit/arconfiguration/videohdrallowed)
- [class var configurableCaptureDeviceForPrimaryCamera: AVCaptureDevice?](/documentation/arkit/arconfiguration/configurablecapturedeviceforprimarycamera)
- [class var recommendedVideoFormatFor4KResolution: ARConfiguration.VideoFormat?](/documentation/arkit/arconfiguration/recommendedvideoformatfor4kresolution)
- [class var recommendedVideoFormatForHighResolutionFrameCapturing: ARConfiguration.VideoFormat?](/documentation/arkit/arconfiguration/recommendedvideoformatforhighresolutionframecapturing)

##### Recording Audio

- [var providesAudioData: Bool](/documentation/arkit/arconfiguration/providesaudiodata)

##### Reconstructing the Scene

- [ARConfiguration.SceneReconstruction](/documentation/arkit/arconfiguration/scenereconstruction)

###### Modeling the Environment

- [init(rawValue: UInt)](/documentation/arkit/arconfiguration/scenereconstruction/init(rawvalue:))
- [static var mesh: ARConfiguration.SceneReconstruction](/documentation/arkit/arconfiguration/scenereconstruction/mesh)
- [static var meshWithClassification: ARConfiguration.SceneReconstruction](/documentation/arkit/arconfiguration/scenereconstruction/meshwithclassification)

#### Spatial Tracking

- [Understanding World Tracking](/documentation/arkit/understanding-world-tracking)
- [ARWorldTrackingConfiguration](/documentation/arkit/arworldtrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arworldtrackingconfiguration/init())
- [var initialWorldMap: ARWorldMap?](/documentation/arkit/arworldtrackingconfiguration/initialworldmap)

##### Tracking Surfaces

- [var planeDetection: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.property)
- [ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct)

###### Plane Detection Option Creation

- [init(rawValue: UInt)](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/init(rawvalue:))

###### Plane Detection Options

- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)
- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)
- [var sceneReconstruction: ARConfiguration.SceneReconstruction](/documentation/arkit/arworldtrackingconfiguration/scenereconstruction)
- [class func supportsSceneReconstruction(ARConfiguration.SceneReconstruction) -> Bool](/documentation/arkit/arworldtrackingconfiguration/supportsscenereconstruction(_:))

##### Detecting or Tracking Images

- [var detectionImages: Set<ARReferenceImage>!](/documentation/arkit/arworldtrackingconfiguration/detectionimages)
- [var maximumNumberOfTrackedImages: Int](/documentation/arkit/arworldtrackingconfiguration/maximumnumberoftrackedimages)
- [var automaticImageScaleEstimationEnabled: Bool](/documentation/arkit/arworldtrackingconfiguration/automaticimagescaleestimationenabled)

##### Detecting 3D Objects

- [var detectionObjects: Set<ARReferenceObject>](/documentation/arkit/arworldtrackingconfiguration/detectionobjects)

##### Tracking the User’s Face

- [var userFaceTrackingEnabled: Bool](/documentation/arkit/arworldtrackingconfiguration/userfacetrackingenabled)
- [class var supportsUserFaceTracking: Bool](/documentation/arkit/arworldtrackingconfiguration/supportsuserfacetracking)

##### Creating Realistic Reflections

- [var environmentTexturing: ARWorldTrackingConfiguration.EnvironmentTexturing](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.property)
- [ARWorldTrackingConfiguration.EnvironmentTexturing](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum)

###### Enumeration Cases

- [case automatic](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/automatic)
- [case manual](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/manual)
- [case none](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/init(rawvalue:))
- [AREnvironmentProbeAnchor](/documentation/arkit/arenvironmentprobeanchor)

###### Creating Probe Anchors

- [init(transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(transform:extent:))
- [init(name: String, transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(name:transform:extent:))

###### Accessing Texture Maps

- [var environmentTexture: (any MTLTexture)?](/documentation/arkit/arenvironmentprobeanchor/environmenttexture)

###### Examining a Probe Anchor

- [var extent: simd_float3](/documentation/arkit/arenvironmentprobeanchor/extent)
- [var wantsHDREnvironmentTextures: Bool](/documentation/arkit/arworldtrackingconfiguration/wantshdrenvironmenttextures)

##### Managing Device Camera Behavior

- [var isAutoFocusEnabled: Bool](/documentation/arkit/arworldtrackingconfiguration/isautofocusenabled)

##### Enabling Collaboration

- [var isCollaborationEnabled: Bool](/documentation/arkit/arworldtrackingconfiguration/iscollaborationenabled)

##### Accessing App Clip Codes

- [Interacting with App Clip Codes in AR](/documentation/appclip/interacting-with-app-clip-codes-in-ar)
- [class var supportsAppClipCodeTracking: Bool](/documentation/arkit/arworldtrackingconfiguration/supportsappclipcodetracking)
- [var appClipCodeTrackingEnabled: Bool](/documentation/arkit/arworldtrackingconfiguration/appclipcodetrackingenabled)
- [ARAppClipCodeAnchor](/documentation/arkit/arappclipcodeanchor)

###### Decoding the URL

- [var url: URL?](/documentation/arkit/arappclipcodeanchor/url)
- [var urlDecodingState: ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.property)
- [ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum)

###### States

- [case decoded](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoded)
- [case decoding](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoding)
- [case failed](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/failed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/init(rawvalue:))

###### Measuring Physical Size

- [var radius: Float](/documentation/arkit/arappclipcodeanchor/radius)
- [ARGeoTrackingConfiguration](/documentation/arkit/argeotrackingconfiguration)

##### Creating a configuration

- [init()](/documentation/arkit/argeotrackingconfiguration/init())

##### Checking availability

- [class func checkAvailability(completionHandler: (Bool, (any Error)?) -> Void)](/documentation/arkit/argeotrackingconfiguration/checkavailability(completionhandler:))
- [class func checkAvailability(at: CLLocationCoordinate2D, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/arkit/argeotrackingconfiguration/checkavailability(at:completionhandler:))

##### Tracking surfaces

- [var planeDetection: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/argeotrackingconfiguration/planedetection)
- [ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct)

###### Plane Detection Option Creation

- [init(rawValue: UInt)](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/init(rawvalue:))

###### Plane Detection Options

- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)
- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)

##### Detecting or tracking images

- [var detectionImages: Set<ARReferenceImage>!](/documentation/arkit/argeotrackingconfiguration/detectionimages)
- [var maximumNumberOfTrackedImages: Int](/documentation/arkit/argeotrackingconfiguration/maximumnumberoftrackedimages)
- [var automaticImageScaleEstimationEnabled: Bool](/documentation/arkit/argeotrackingconfiguration/automaticimagescaleestimationenabled)

##### Detecting real-world objects

- [var detectionObjects: Set<ARReferenceObject>](/documentation/arkit/argeotrackingconfiguration/detectionobjects)

##### Creating realistic reflections

- [var environmentTexturing: ARWorldTrackingConfiguration.EnvironmentTexturing](/documentation/arkit/argeotrackingconfiguration/environmenttexturing)
- [ARWorldTrackingConfiguration.EnvironmentTexturing](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum)

###### Enumeration Cases

- [case automatic](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/automatic)
- [case manual](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/manual)
- [case none](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arworldtrackingconfiguration/environmenttexturing-swift.enum/init(rawvalue:))
- [AREnvironmentProbeAnchor](/documentation/arkit/arenvironmentprobeanchor)

###### Creating Probe Anchors

- [init(transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(transform:extent:))
- [init(name: String, transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(name:transform:extent:))

###### Accessing Texture Maps

- [var environmentTexture: (any MTLTexture)?](/documentation/arkit/arenvironmentprobeanchor/environmenttexture)

###### Examining a Probe Anchor

- [var extent: simd_float3](/documentation/arkit/arenvironmentprobeanchor/extent)
- [var wantsHDREnvironmentTextures: Bool](/documentation/arkit/argeotrackingconfiguration/wantshdrenvironmenttextures)

##### Accessing app clip codes

- [Interacting with App Clip Codes in AR](/documentation/appclip/interacting-with-app-clip-codes-in-ar)
- [class var supportsAppClipCodeTracking: Bool](/documentation/arkit/argeotrackingconfiguration/supportsappclipcodetracking)
- [var appClipCodeTrackingEnabled: Bool](/documentation/arkit/argeotrackingconfiguration/appclipcodetrackingenabled)
- [ARAppClipCodeAnchor](/documentation/arkit/arappclipcodeanchor)

###### Decoding the URL

- [var url: URL?](/documentation/arkit/arappclipcodeanchor/url)
- [var urlDecodingState: ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.property)
- [ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum)

###### States

- [case decoded](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoded)
- [case decoding](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoding)
- [case failed](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/failed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/init(rawvalue:))

###### Measuring Physical Size

- [var radius: Float](/documentation/arkit/arappclipcodeanchor/radius)
- [AROrientationTrackingConfiguration](/documentation/arkit/arorientationtrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arorientationtrackingconfiguration/init())

##### Managing Device Camera Behavior

- [var isAutoFocusEnabled: Bool](/documentation/arkit/arorientationtrackingconfiguration/isautofocusenabled)
- [ARPositionalTrackingConfiguration](/documentation/arkit/arpositionaltrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arpositionaltrackingconfiguration/init())
- [var initialWorldMap: ARWorldMap?](/documentation/arkit/arpositionaltrackingconfiguration/initialworldmap)

##### Detecting Real-World Surfaces

- [var planeDetection: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arpositionaltrackingconfiguration/planedetection)

#### Body and Face Tracking

- [ARBodyTrackingConfiguration](/documentation/arkit/arbodytrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arbodytrackingconfiguration/init())
- [var initialWorldMap: ARWorldMap?](/documentation/arkit/arbodytrackingconfiguration/initialworldmap)

##### Estimating Body Scale

- [var automaticSkeletonScaleEstimationEnabled: Bool](/documentation/arkit/arbodytrackingconfiguration/automaticskeletonscaleestimationenabled)

##### Enabling Auto Focus

- [var isAutoFocusEnabled: Bool](/documentation/arkit/arbodytrackingconfiguration/isautofocusenabled)

##### Enabling Plane Detection

- [var planeDetection: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arbodytrackingconfiguration/planedetection)
- [ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct)

###### Plane Detection Option Creation

- [init(rawValue: UInt)](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/init(rawvalue:))

###### Plane Detection Options

- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)
- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)

##### Enabling Image Tracking

- [var automaticImageScaleEstimationEnabled: Bool](/documentation/arkit/arbodytrackingconfiguration/automaticimagescaleestimationenabled)
- [var detectionImages: Set<ARReferenceImage>](/documentation/arkit/arbodytrackingconfiguration/detectionimages)
- [var maximumNumberOfTrackedImages: Int](/documentation/arkit/arbodytrackingconfiguration/maximumnumberoftrackedimages)

##### Adding Realistic Reflections

- [var wantsHDREnvironmentTextures: Bool](/documentation/arkit/arbodytrackingconfiguration/wantshdrenvironmenttextures)
- [var environmentTexturing: ARWorldTrackingConfiguration.EnvironmentTexturing](/documentation/arkit/arbodytrackingconfiguration/environmenttexturing)

##### Accessing App Clip Codes

- [Interacting with App Clip Codes in AR](/documentation/appclip/interacting-with-app-clip-codes-in-ar)
- [class var supportsAppClipCodeTracking: Bool](/documentation/arkit/arbodytrackingconfiguration/supportsappclipcodetracking)
- [var appClipCodeTrackingEnabled: Bool](/documentation/arkit/arbodytrackingconfiguration/appclipcodetrackingenabled)
- [ARAppClipCodeAnchor](/documentation/arkit/arappclipcodeanchor)

###### Decoding the URL

- [var url: URL?](/documentation/arkit/arappclipcodeanchor/url)
- [var urlDecodingState: ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.property)
- [ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum)

###### States

- [case decoded](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoded)
- [case decoding](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoding)
- [case failed](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/failed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/init(rawvalue:))

###### Measuring Physical Size

- [var radius: Float](/documentation/arkit/arappclipcodeanchor/radius)
- [ARFaceTrackingConfiguration](/documentation/arkit/arfacetrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arfacetrackingconfiguration/init())

##### Enabling World Tracking

- [class var supportsWorldTracking: Bool](/documentation/arkit/arfacetrackingconfiguration/supportsworldtracking)
- [var isWorldTrackingEnabled: Bool](/documentation/arkit/arfacetrackingconfiguration/isworldtrackingenabled)

##### Tracking Multiple Faces

- [var maximumNumberOfTrackedFaces: Int](/documentation/arkit/arfacetrackingconfiguration/maximumnumberoftrackedfaces)
- [class var supportedNumberOfTrackedFaces: Int](/documentation/arkit/arfacetrackingconfiguration/supportednumberoftrackedfaces)

#### Image Recognition

- [ARImageTrackingConfiguration](/documentation/arkit/arimagetrackingconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arimagetrackingconfiguration/init())

##### Choosing Images to Track

- [var trackingImages: Set<ARReferenceImage>](/documentation/arkit/arimagetrackingconfiguration/trackingimages)
- [var maximumNumberOfTrackedImages: Int](/documentation/arkit/arimagetrackingconfiguration/maximumnumberoftrackedimages)

##### Managing Device Camera Behavior

- [var isAutoFocusEnabled: Bool](/documentation/arkit/arimagetrackingconfiguration/isautofocusenabled)

#### Object Detection

- [ARObjectScanningConfiguration](/documentation/arkit/arobjectscanningconfiguration)

##### Creating a Configuration

- [init()](/documentation/arkit/arobjectscanningconfiguration/init())

##### Enabling Plane Detection

- [var planeDetection: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arobjectscanningconfiguration/planedetection)
- [ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct)

###### Plane Detection Option Creation

- [init(rawValue: UInt)](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/init(rawvalue:))

###### Plane Detection Options

- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)
- [static var horizontal: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/horizontal)
- [static var vertical: ARWorldTrackingConfiguration.PlaneDetection](/documentation/arkit/arworldtrackingconfiguration/planedetection-swift.struct/vertical)

##### Managing Device Camera Behavior

- [var isAutoFocusEnabled: Bool](/documentation/arkit/arobjectscanningconfiguration/isautofocusenabled)

### Views

- [RealityView](/documentation/realitykit/realityview)
- [ARView](/documentation/realitykit/arview)
- [ARSCNView](/documentation/arkit/arscnview)

#### Essentials

- [Providing 3D Virtual Content with SceneKit](/documentation/arkit/providing-3d-virtual-content-with-scenekit)
- [var session: ARSession](/documentation/arkit/arscnview/session)
- [var scene: SCNScene](/documentation/arkit/arscnview/scene)

#### Responding to AR Updates

- [var delegate: (any ARSCNViewDelegate)?](/documentation/arkit/arscnview/delegate)
- [ARSCNViewDelegate](/documentation/arkit/arscnviewdelegate)

##### Handling Content Updates

- [func renderer(any SCNSceneRenderer, nodeFor: ARAnchor) -> SCNNode?](/documentation/arkit/arscnviewdelegate/renderer(_:nodefor:))
- [func renderer(any SCNSceneRenderer, didAdd: SCNNode, for: ARAnchor)](/documentation/arkit/arscnviewdelegate/renderer(_:didadd:for:))
- [func renderer(any SCNSceneRenderer, willUpdate: SCNNode, for: ARAnchor)](/documentation/arkit/arscnviewdelegate/renderer(_:willupdate:for:))
- [func renderer(any SCNSceneRenderer, didUpdate: SCNNode, for: ARAnchor)](/documentation/arkit/arscnviewdelegate/renderer(_:didupdate:for:))
- [func renderer(any SCNSceneRenderer, didRemove: SCNNode, for: ARAnchor)](/documentation/arkit/arscnviewdelegate/renderer(_:didremove:for:))

#### Finding Real-World Surfaces

- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/arkit/arscnview/hittest(_:types:))
- [func raycastQuery(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> ARRaycastQuery?](/documentation/arkit/arscnview/raycastquery(from:allowing:alignment:))

#### Mapping Content to Real-World Positions

- [func anchor(for: SCNNode) -> ARAnchor?](/documentation/arkit/arscnview/anchor(for:))
- [func node(for: ARAnchor) -> SCNNode?](/documentation/arkit/arscnview/node(for:))
- [func unprojectPoint(CGPoint, ontoPlane: simd_float4x4) -> simd_float3?](/documentation/arkit/arscnview/unprojectpoint(_:ontoplane:))

#### Managing Lighting

- [var automaticallyUpdatesLighting: Bool](/documentation/arkit/arscnview/automaticallyupdateslighting)

#### Debugging AR Display

- [ARSCNDebugOptions](/documentation/arkit/arscndebugoptions)

#### Managing Rendering Effects

- [var rendersMotionBlur: Bool](/documentation/arkit/arscnview/rendersmotionblur)
- [var rendersCameraGrain: Bool](/documentation/arkit/arscnview/renderscameragrain)
- [ARSKView](/documentation/arkit/arskview)

#### First Steps

- [Providing 2D Virtual Content with SpriteKit](/documentation/arkit/providing-2d-virtual-content-with-spritekit)
- [var session: ARSession](/documentation/arkit/arskview/session)

#### Responding to AR Updates

- [var delegate: (any ARSKViewDelegate)?](/documentation/arkit/arskview/delegate)
- [ARSKViewDelegate](/documentation/arkit/arskviewdelegate)

##### Handling Content Updates

- [func view(ARSKView, nodeFor: ARAnchor) -> SKNode?](/documentation/arkit/arskviewdelegate/view(_:nodefor:))
- [func view(ARSKView, didAdd: SKNode, for: ARAnchor)](/documentation/arkit/arskviewdelegate/view(_:didadd:for:))
- [func view(ARSKView, willUpdate: SKNode, for: ARAnchor)](/documentation/arkit/arskviewdelegate/view(_:willupdate:for:))
- [func view(ARSKView, didUpdate: SKNode, for: ARAnchor)](/documentation/arkit/arskviewdelegate/view(_:didupdate:for:))
- [func view(ARSKView, didRemove: SKNode, for: ARAnchor)](/documentation/arkit/arskviewdelegate/view(_:didremove:for:))

#### Finding Real-World Surfaces

- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/arkit/arskview/hittest(_:types:))

#### Mapping Content to Real-World Positions

- [func anchor(for: SKNode) -> ARAnchor?](/documentation/arkit/arskview/anchor(for:))
- [func node(for: ARAnchor) -> SKNode?](/documentation/arkit/arskview/node(for:))
- [ARCoachingOverlayView](/documentation/arkit/arcoachingoverlayview)

#### Delegating Events

- [var delegate: (any ARCoachingOverlayViewDelegate)?](/documentation/arkit/arcoachingoverlayview/delegate)
- [ARCoachingOverlayViewDelegate](/documentation/arkit/arcoachingoverlayviewdelegate)

##### Enabling Coaching

- [func coachingOverlayViewWillActivate(ARCoachingOverlayView)](/documentation/arkit/arcoachingoverlayviewdelegate/coachingoverlayviewwillactivate(_:))
- [func coachingOverlayViewDidDeactivate(ARCoachingOverlayView)](/documentation/arkit/arcoachingoverlayviewdelegate/coachingoverlayviewdiddeactivate(_:))

##### Restarting the Session

- [func coachingOverlayViewDidRequestSessionReset(ARCoachingOverlayView)](/documentation/arkit/arcoachingoverlayviewdelegate/coachingoverlayviewdidrequestsessionreset(_:))

#### Defining a Goal

- [var goal: ARCoachingOverlayView.Goal](/documentation/arkit/arcoachingoverlayview/goal-swift.property)
- [ARCoachingOverlayView.Goal](/documentation/arkit/arcoachingoverlayview/goal-swift.enum)

##### Defining a Goal

- [case anyPlane](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/anyplane)
- [case horizontalPlane](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/horizontalplane)
- [case tracking](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/tracking)
- [case verticalPlane](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/verticalplane)
- [case geoTracking](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/geotracking)

##### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arcoachingoverlayview/goal-swift.enum/init(rawvalue:))

#### Activating the View

- [var activatesAutomatically: Bool](/documentation/arkit/arcoachingoverlayview/activatesautomatically)
- [var isActive: Bool](/documentation/arkit/arcoachingoverlayview/isactive)
- [func setActive(Bool, animated: Bool)](/documentation/arkit/arcoachingoverlayview/setactive(_:animated:))

#### Providing the Session

- [var session: ARSession?](/documentation/arkit/arcoachingoverlayview/session)
- [var sessionProvider: (any ARSessionProviding)?](/documentation/arkit/arcoachingoverlayview/sessionprovider)

### Virtual Content

- [Content Anchors](/documentation/arkit/content-anchors)

#### Surface Detection

- [Tracking and visualizing planes](/documentation/arkit/tracking-and-visualizing-planes)
- [ARPlaneAnchor](/documentation/arkit/arplaneanchor)

##### Orientation

- [var alignment: ARPlaneAnchor.Alignment](/documentation/arkit/arplaneanchor/alignment-swift.property)
- [ARPlaneAnchor.Alignment](/documentation/arkit/arplaneanchor/alignment-swift.enum)

###### Alignment Values

- [case horizontal](/documentation/arkit/arplaneanchor/alignment-swift.enum/horizontal)
- [case vertical](/documentation/arkit/arplaneanchor/alignment-swift.enum/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arplaneanchor/alignment-swift.enum/init(rawvalue:))

##### Geometry

- [var geometry: ARPlaneGeometry](/documentation/arkit/arplaneanchor/geometry)
- [ARPlaneGeometry](/documentation/arkit/arplanegeometry)

###### Accessing Mesh Data

- [var vertices: [simd_float3]](/documentation/arkit/arplanegeometry/vertices-43kle)
- [var textureCoordinates: [vector_float2]](/documentation/arkit/arplanegeometry/texturecoordinates-p801)
- [var triangleCount: Int](/documentation/arkit/arplanegeometry/trianglecount)
- [var triangleIndices: [Int16]](/documentation/arkit/arplanegeometry/triangleindices-64epx)

###### Finding Boundary Points

- [var boundaryVertices: [simd_float3]](/documentation/arkit/arplanegeometry/boundaryvertices-3h98l)
- [ARSCNPlaneGeometry](/documentation/arkit/arscnplanegeometry)

###### Creating a Geometry

- [convenience init?(device: any MTLDevice)](/documentation/arkit/arscnplanegeometry/init(device:))

###### Updating the Geometry

- [func update(from: ARPlaneGeometry)](/documentation/arkit/arscnplanegeometry/update(from:))

##### Dimensions

- [var center: simd_float3](/documentation/arkit/arplaneanchor/center)
- [var planeExtent: ARPlaneExtent](/documentation/arkit/arplaneanchor/planeextent)
- [ARPlaneExtent](/documentation/arkit/arplaneextent)

###### Inspecting Plane Size

- [var width: Float](/documentation/arkit/arplaneextent/width)
- [var height: Float](/documentation/arkit/arplaneextent/height)

###### Inspecting Plane Y-Rotation

- [var rotationOnYAxis: Float](/documentation/arkit/arplaneextent/rotationonyaxis)
- [var extent: simd_float3](/documentation/arkit/arplaneanchor/extent)

##### Classifying a Plane

- [class var isClassificationSupported: Bool](/documentation/arkit/arplaneanchor/isclassificationsupported)
- [var classification: ARPlaneAnchor.Classification](/documentation/arkit/arplaneanchor/classification-2r4x8)
- [ARPlaneAnchor.Classification](/documentation/arkit/arplaneanchor/classification-swift.enum)

###### Plane Classifications

- [case wall](/documentation/arkit/arplaneanchor/classification-swift.enum/wall)
- [case floor](/documentation/arkit/arplaneanchor/classification-swift.enum/floor)
- [case ceiling](/documentation/arkit/arplaneanchor/classification-swift.enum/ceiling)
- [case table](/documentation/arkit/arplaneanchor/classification-swift.enum/table)
- [case seat](/documentation/arkit/arplaneanchor/classification-swift.enum/seat)
- [case door](/documentation/arkit/arplaneanchor/classification-swift.enum/door)
- [case window](/documentation/arkit/arplaneanchor/classification-swift.enum/window)

###### Missing Classification Status

- [case none(ARPlaneAnchor.Classification.Status)](/documentation/arkit/arplaneanchor/classification-swift.enum/none(_:))
- [ARPlaneAnchor.Classification.Status](/documentation/arkit/arplaneanchor/classification-swift.enum/status)

###### Classification Status

- [case notAvailable](/documentation/arkit/arplaneanchor/classification-swift.enum/status/notavailable)
- [case undetermined](/documentation/arkit/arplaneanchor/classification-swift.enum/status/undetermined)
- [case unknown](/documentation/arkit/arplaneanchor/classification-swift.enum/status/unknown)
- [ARMeshAnchor](/documentation/arkit/armeshanchor)

##### Accessing the Mesh

- [var geometry: ARMeshGeometry](/documentation/arkit/armeshanchor/geometry)
- [ARMeshGeometry](/documentation/arkit/armeshgeometry)

###### Accessing Geometry Data

- [var vertices: ARGeometrySource](/documentation/arkit/armeshgeometry/vertices)
- [ARGeometrySource](/documentation/arkit/argeometrysource)

###### Accessing Geometry

- [subscript(Int32) -> (Float, Float, Float)](/documentation/arkit/argeometrysource/subscript(_:)-3v98f)
- [subscript(Int32) -> CUnsignedChar](/documentation/arkit/argeometrysource/subscript(_:)-7jf4y)
- [var buffer: any MTLBuffer](/documentation/arkit/argeometrysource/buffer)

###### Getting Geometry Information

- [var componentsPerVector: Int](/documentation/arkit/argeometrysource/componentspervector)
- [var count: Int](/documentation/arkit/argeometrysource/count)
- [var format: MTLVertexFormat](/documentation/arkit/argeometrysource/format)
- [var offset: Int](/documentation/arkit/argeometrysource/offset)
- [var stride: Int](/documentation/arkit/argeometrysource/stride)

###### Getting Geometry Information

- [var classification: ARGeometrySource?](/documentation/arkit/armeshgeometry/classification)
- [ARMeshClassification](/documentation/arkit/armeshclassification)

###### Options

- [case ceiling](/documentation/arkit/armeshclassification/ceiling)
- [case door](/documentation/arkit/armeshclassification/door)
- [case floor](/documentation/arkit/armeshclassification/floor)
- [case none](/documentation/arkit/armeshclassification/none)
- [case seat](/documentation/arkit/armeshclassification/seat)
- [case table](/documentation/arkit/armeshclassification/table)
- [case wall](/documentation/arkit/armeshclassification/wall)
- [case window](/documentation/arkit/armeshclassification/window)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/armeshclassification/init(rawvalue:))
- [var faces: ARGeometryElement](/documentation/arkit/armeshgeometry/faces)
- [ARGeometryElement](/documentation/arkit/argeometryelement)

###### Accessing Index Data

- [subscript(Int) -> [Int32]](/documentation/arkit/argeometryelement/subscript(_:))
- [var buffer: any MTLBuffer](/documentation/arkit/argeometryelement/buffer)

###### Getting Index Information

- [var bytesPerIndex: Int](/documentation/arkit/argeometryelement/bytesperindex)
- [var count: Int](/documentation/arkit/argeometryelement/count)
- [var indexCountPerPrimitive: Int](/documentation/arkit/argeometryelement/indexcountperprimitive)
- [var primitiveType: ARGeometryPrimitiveType](/documentation/arkit/argeometryelement/primitivetype)
- [ARGeometryPrimitiveType](/documentation/arkit/argeometryprimitivetype)

###### Type of Connection

- [case line](/documentation/arkit/argeometryprimitivetype/line)
- [case triangle](/documentation/arkit/argeometryprimitivetype/triangle)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeometryprimitivetype/init(rawvalue:))
- [var normals: ARGeometrySource](/documentation/arkit/armeshgeometry/normals)

#### Image Detection

- [Tracking and altering images](/documentation/arkit/tracking-and-altering-images)
- [Detecting Images in an AR Experience](/documentation/arkit/detecting-images-in-an-ar-experience)
- [ARImageAnchor](/documentation/arkit/arimageanchor)

##### Identifying Detected Images

- [var referenceImage: ARReferenceImage](/documentation/arkit/arimageanchor/referenceimage)

##### Estimating Scale

- [var estimatedScaleFactor: CGFloat](/documentation/arkit/arimageanchor/estimatedscalefactor)
- [ARReferenceImage](/documentation/arkit/arreferenceimage)

##### Loading Reference Images

- [class func referenceImages(inGroupNamed: String, bundle: Bundle?) -> Set<ARReferenceImage>?](/documentation/arkit/arreferenceimage/referenceimages(ingroupnamed:bundle:))

##### Examining a Reference Image

- [var name: String?](/documentation/arkit/arreferenceimage/name)
- [var physicalSize: CGSize](/documentation/arkit/arreferenceimage/physicalsize)
- [var resourceGroupName: String?](/documentation/arkit/arreferenceimage/resourcegroupname)

##### Creating Reference Images

- [init(CGImage, orientation: CGImagePropertyOrientation, physicalWidth: CGFloat)](/documentation/arkit/arreferenceimage/init(_:orientation:physicalwidth:)-8b3bs)
- [init(CVPixelBuffer, orientation: CGImagePropertyOrientation, physicalWidth: CGFloat)](/documentation/arkit/arreferenceimage/init(_:orientation:physicalwidth:)-ir2z)

##### Validating Reference Images

- [func validate(completionHandler: ((any Error)?) -> Void)](/documentation/arkit/arreferenceimage/validate(completionhandler:))

#### Physical Objects

- [Visualizing and interacting with a reconstructed scene](/documentation/arkit/visualizing-and-interacting-with-a-reconstructed-scene)
- [Scanning and Detecting 3D Objects](/documentation/arkit/scanning-and-detecting-3d-objects)
- [ARObjectAnchor](/documentation/arkit/arobjectanchor)

##### Identifying Detected Objects

- [var referenceObject: ARReferenceObject](/documentation/arkit/arobjectanchor/referenceobject)
- [ARReferenceObject](/documentation/arkit/arreferenceobject)

##### Loading Reference Objects

- [init(archiveURL: URL) throws](/documentation/arkit/arreferenceobject/init(archiveurl:))
- [class func referenceObjects(inGroupNamed: String, bundle: Bundle?) -> Set<ARReferenceObject>?](/documentation/arkit/arreferenceobject/referenceobjects(ingroupnamed:bundle:))

##### Examining a Reference Object

- [var name: String?](/documentation/arkit/arreferenceobject/name)
- [var resourceGroupName: String?](/documentation/arkit/arreferenceobject/resourcegroupname)
- [var center: simd_float3](/documentation/arkit/arreferenceobject/center)
- [var extent: simd_float3](/documentation/arkit/arreferenceobject/extent)
- [var scale: simd_float3](/documentation/arkit/arreferenceobject/scale)

##### Saving Recorded Objects

- [func export(to: URL, previewImage: UIImage?) throws](/documentation/arkit/arreferenceobject/export(to:previewimage:))
- [class let archiveExtension: String](/documentation/arkit/arreferenceobject/archiveextension)

##### Creating Derivative Reference Objects

- [func applyingTransform(simd_float4x4) -> ARReferenceObject](/documentation/arkit/arreferenceobject/applyingtransform(_:))
- [func merging(ARReferenceObject) throws -> ARReferenceObject](/documentation/arkit/arreferenceobject/merging(_:))

##### Debugging a Reference Object

- [var rawFeaturePoints: ARPointCloud](/documentation/arkit/arreferenceobject/rawfeaturepoints)

#### Body Position Tracking

- [Capturing Body Motion in 3D](/documentation/arkit/capturing-body-motion-in-3d)
- [Rigging a Model for Motion Capture](/documentation/arkit/rigging-a-model-for-motion-capture)
- [Validating a Model for Motion Capture](/documentation/arkit/validating-a-model-for-motion-capture)
- [ARBodyAnchor](/documentation/arkit/arbodyanchor)

##### Interpreting 3D Motion

- [var skeleton: ARSkeleton3D](/documentation/arkit/arbodyanchor/skeleton)

##### Getting Scale Information

- [var estimatedScaleFactor: CGFloat](/documentation/arkit/arbodyanchor/estimatedscalefactor)

#### Face Tracking

- [Tracking and visualizing faces](/documentation/arkit/tracking-and-visualizing-faces)
- [Combining user face-tracking and world tracking](/documentation/arkit/combining-user-face-tracking-and-world-tracking)
- [ARFaceAnchor](/documentation/arkit/arfaceanchor)

##### Using Face Geometry

- [var geometry: ARFaceGeometry](/documentation/arkit/arfaceanchor/geometry)

##### Using Blend Shapes

- [var blendShapes: [ARFaceAnchor.BlendShapeLocation : NSNumber]](/documentation/arkit/arfaceanchor/blendshapes)
- [ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation)

###### Left Eye

- [static let eyeBlinkLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyeblinkleft)
- [static let eyeLookDownLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookdownleft)
- [static let eyeLookInLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookinleft)
- [static let eyeLookOutLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookoutleft)
- [static let eyeLookUpLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookupleft)
- [static let eyeSquintLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyesquintleft)
- [static let eyeWideLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyewideleft)

###### Right Eye

- [static let eyeBlinkRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyeblinkright)
- [static let eyeLookDownRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookdownright)
- [static let eyeLookInRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookinright)
- [static let eyeLookOutRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookoutright)
- [static let eyeLookUpRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyelookupright)
- [static let eyeSquintRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyesquintright)
- [static let eyeWideRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/eyewideright)

###### Mouth and Jaw

- [static let jawForward: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/jawforward)
- [static let jawLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/jawleft)
- [static let jawRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/jawright)
- [static let jawOpen: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/jawopen)
- [static let mouthClose: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthclose)
- [static let mouthFunnel: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthfunnel)
- [static let mouthPucker: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthpucker)
- [static let mouthLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthleft)
- [static let mouthRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthright)
- [static let mouthSmileLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthsmileleft)
- [static let mouthSmileRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthsmileright)
- [static let mouthFrownLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthfrownleft)
- [static let mouthFrownRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthfrownright)
- [static let mouthDimpleLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthdimpleleft)
- [static let mouthDimpleRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthdimpleright)
- [static let mouthStretchLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthstretchleft)
- [static let mouthStretchRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthstretchright)
- [static let mouthRollLower: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthrolllower)
- [static let mouthRollUpper: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthrollupper)
- [static let mouthShrugLower: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthshruglower)
- [static let mouthShrugUpper: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthshrugupper)
- [static let mouthPressLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthpressleft)
- [static let mouthPressRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthpressright)
- [static let mouthLowerDownLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthlowerdownleft)
- [static let mouthLowerDownRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthlowerdownright)
- [static let mouthUpperUpLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthupperupleft)
- [static let mouthUpperUpRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/mouthupperupright)

###### Eyebrows, Cheeks, and Nose

- [static let browDownLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/browdownleft)
- [static let browDownRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/browdownright)
- [static let browInnerUp: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/browinnerup)
- [static let browOuterUpLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/browouterupleft)
- [static let browOuterUpRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/browouterupright)
- [static let cheekPuff: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/cheekpuff)
- [static let cheekSquintLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/cheeksquintleft)
- [static let cheekSquintRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/cheeksquintright)
- [static let noseSneerLeft: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/nosesneerleft)
- [static let noseSneerRight: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/nosesneerright)

###### Tongue

- [static let tongueOut: ARFaceAnchor.BlendShapeLocation](/documentation/arkit/arfaceanchor/blendshapelocation/tongueout)

###### Creating a Blend Shape Location

- [init(rawValue: String)](/documentation/arkit/arfaceanchor/blendshapelocation/init(rawvalue:))

##### Tracking Eye Movement

- [var leftEyeTransform: simd_float4x4](/documentation/arkit/arfaceanchor/lefteyetransform)
- [var rightEyeTransform: simd_float4x4](/documentation/arkit/arfaceanchor/righteyetransform)
- [var lookAtPoint: simd_float3](/documentation/arkit/arfaceanchor/lookatpoint)

#### Geotracking

- [Tracking geographic locations in AR](/documentation/arkit/tracking-geographic-locations-in-ar)
- [ARGeoAnchor](/documentation/arkit/argeoanchor)

##### Creating a Geo Anchor

- [convenience init(coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance?)](/documentation/arkit/argeoanchor/init(coordinate:altitude:))
- [init(name: String, coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance)](/documentation/arkit/argeoanchor/init(name:coordinate:altitude:)-8sbh4)
- [convenience init(name: String, coordinate: CLLocationCoordinate2D, altitude: CLLocationDistance?)](/documentation/arkit/argeoanchor/init(name:coordinate:altitude:)-csze)

##### Accessing Latitude and Longitude

- [var coordinate: CLLocationCoordinate2D](/documentation/arkit/argeoanchor/coordinate)

##### Defining Altitude

- [var altitude: CLLocationDistance?](/documentation/arkit/argeoanchor/altitude-89k4x)
- [var altitudeSource: ARGeoAnchor.AltitudeSource](/documentation/arkit/argeoanchor/altitudesource-swift.property)
- [ARGeoAnchor.AltitudeSource](/documentation/arkit/argeoanchor/altitudesource-swift.enum)

###### Sources

- [case precise](/documentation/arkit/argeoanchor/altitudesource-swift.enum/precise)
- [case coarse](/documentation/arkit/argeoanchor/altitudesource-swift.enum/coarse)
- [case userDefined](/documentation/arkit/argeoanchor/altitudesource-swift.enum/userdefined)
- [case unknown](/documentation/arkit/argeoanchor/altitudesource-swift.enum/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeoanchor/altitudesource-swift.enum/init(rawvalue:))

#### Multiuser Experiences

- [ARParticipantAnchor](/documentation/arkit/arparticipantanchor)

#### App Clip Codes

- [Interacting with App Clip Codes in AR](/documentation/appclip/interacting-with-app-clip-codes-in-ar)
- [ARAppClipCodeAnchor](/documentation/arkit/arappclipcodeanchor)

##### Decoding the URL

- [var url: URL?](/documentation/arkit/arappclipcodeanchor/url)
- [var urlDecodingState: ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.property)
- [ARAppClipCodeAnchor.URLDecodingState](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum)

###### States

- [case decoded](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoded)
- [case decoding](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/decoding)
- [case failed](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/failed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arappclipcodeanchor/urldecodingstate-swift.enum/init(rawvalue:))

##### Measuring Physical Size

- [var radius: Float](/documentation/arkit/arappclipcodeanchor/radius)

#### Text Annotations

- [Creating screen annotations for objects in an AR experience](/documentation/arkit/creating-screen-annotations-for-objects-in-an-ar-experience)
- [Recognizing and Labeling Arbitrary Objects](/documentation/arkit/recognizing-and-labeling-arbitrary-objects)

#### Common Types

- [ARAnchor](/documentation/arkit/aranchor)

##### Creating Anchors

- [init(transform: simd_float4x4)](/documentation/arkit/aranchor/init(transform:))
- [init(name: String, transform: simd_float4x4)](/documentation/arkit/aranchor/init(name:transform:))
- [var name: String?](/documentation/arkit/aranchor/name)

##### Tracking Anchors

- [var identifier: UUID](/documentation/arkit/aranchor/identifier)
- [var sessionIdentifier: UUID?](/documentation/arkit/aranchor/sessionidentifier)
- [var transform: simd_float4x4](/documentation/arkit/aranchor/transform)
- [ARAnchorCopying](/documentation/arkit/aranchorcopying)

##### Copying Anchors

- [init(anchor: ARAnchor)](/documentation/arkit/aranchorcopying/init(anchor:))
- [ARTrackable](/documentation/arkit/artrackable)

##### Monitoring Tracking State

- [var isTracked: Bool](/documentation/arkit/artrackable/istracked)
- [Environmental Analysis](/documentation/arkit/environmental-analysis)

#### Video Frame Analysis

- [Displaying a point cloud using scene depth](/documentation/arkit/displaying-a-point-cloud-using-scene-depth)
- [Creating a fog effect using scene depth](/documentation/arkit/creating-a-fog-effect-using-scene-depth)
- [ARFrame](/documentation/arkit/arframe)

##### Accessing camera data

- [var camera: ARCamera](/documentation/arkit/arframe/camera)
- [var capturedImage: CVPixelBuffer](/documentation/arkit/arframe/capturedimage)
- [var timestamp: TimeInterval](/documentation/arkit/arframe/timestamp)
- [var cameraGrainIntensity: Float](/documentation/arkit/arframe/cameragrainintensity)
- [var cameraGrainTexture: (any MTLTexture)?](/documentation/arkit/arframe/cameragraintexture)
- [var exifData: [String : Any]](/documentation/arkit/arframe/exifdata)

##### Accessing scene data

- [var lightEstimate: ARLightEstimate?](/documentation/arkit/arframe/lightestimate)
- [func displayTransform(for: UIInterfaceOrientation, viewportSize: CGSize) -> CGAffineTransform](/documentation/arkit/arframe/displaytransform(for:viewportsize:))
- [var rawFeaturePoints: ARPointCloud?](/documentation/arkit/arframe/rawfeaturepoints)
- [var capturedDepthData: AVDepthData?](/documentation/arkit/arframe/captureddepthdata)
- [var capturedDepthDataTimestamp: TimeInterval](/documentation/arkit/arframe/captureddepthdatatimestamp)
- [var sceneDepth: ARDepthData?](/documentation/arkit/arframe/scenedepth)
- [var smoothedSceneDepth: ARDepthData?](/documentation/arkit/arframe/smoothedscenedepth)

##### Tracking and interacting with the real world

- [var anchors: [ARAnchor]](/documentation/arkit/arframe/anchors)
- [func raycastQuery(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> ARRaycastQuery](/documentation/arkit/arframe/raycastquery(from:allowing:alignment:))
- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/arkit/arframe/hittest(_:types:))

##### Checking world-mapping status

- [var worldMappingStatus: ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.property)
- [ARFrame.WorldMappingStatus](/documentation/arkit/arframe/worldmappingstatus-swift.enum)

###### Enumeration Cases

- [case extending](/documentation/arkit/arframe/worldmappingstatus-swift.enum/extending)
- [case limited](/documentation/arkit/arframe/worldmappingstatus-swift.enum/limited)
- [case mapped](/documentation/arkit/arframe/worldmappingstatus-swift.enum/mapped)
- [case notAvailable](/documentation/arkit/arframe/worldmappingstatus-swift.enum/notavailable)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arframe/worldmappingstatus-swift.enum/init(rawvalue:))

##### Checking for people

- [var detectedBody: ARBody2D?](/documentation/arkit/arframe/detectedbody)
- [ARBody2D](/documentation/arkit/arbody2d)

###### Getting Joint Information

- [var skeleton: ARSkeleton2D](/documentation/arkit/arbody2d/skeleton)
- [var segmentationBuffer: CVPixelBuffer?](/documentation/arkit/arframe/segmentationbuffer)
- [var estimatedDepthData: CVPixelBuffer?](/documentation/arkit/arframe/estimateddepthdata)
- [ARFrame.SegmentationClass](/documentation/arkit/arframe/segmentationclass)

###### Classifying Pixels

- [case person](/documentation/arkit/arframe/segmentationclass/person)
- [case none](/documentation/arkit/arframe/segmentationclass/none)

###### Initializers

- [init?(rawValue: UInt8)](/documentation/arkit/arframe/segmentationclass/init(rawvalue:))

##### Assessing geo-tracking condition

- [var geoTrackingStatus: ARGeoTrackingStatus?](/documentation/arkit/arframe/geotrackingstatus)
- [ARGeoTrackingStatus](/documentation/arkit/argeotrackingstatus)

###### Checking State

- [var state: ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.property)
- [ARGeoTrackingStatus.State](/documentation/arkit/argeotrackingstatus/state-swift.enum)

###### States

- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)
- [case initializing](/documentation/arkit/argeotrackingstatus/state-swift.enum/initializing)
- [case localized](/documentation/arkit/argeotrackingstatus/state-swift.enum/localized)
- [case localizing](/documentation/arkit/argeotrackingstatus/state-swift.enum/localizing)
- [case notAvailable](/documentation/arkit/argeotrackingstatus/state-swift.enum/notavailable)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/state-swift.enum/init(rawvalue:))

###### Determining the Reason

- [var stateReason: ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.property)
- [ARGeoTrackingStatus.StateReason](/documentation/arkit/argeotrackingstatus/statereason-swift.enum)

###### Status Reasons

- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)
- [case none](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/none)
- [case notAvailableAtLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/notavailableatlocation)
- [case needLocationPermissions](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/needlocationpermissions)
- [case devicePointedTooLow](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/devicepointedtoolow)
- [case worldTrackingUnstable](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/worldtrackingunstable)
- [case waitingForLocation](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforlocation)
- [case waitingForAvailabilityCheck](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/waitingforavailabilitycheck)
- [case geoDataNotLoaded](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/geodatanotloaded)
- [case visualLocalizationFailed](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/visuallocalizationfailed)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/statereason-swift.enum/init(rawvalue:))

###### Judging Accuracy

- [var accuracy: ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.property)
- [ARGeoTrackingStatus.Accuracy](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum)

###### Accuracies

- [case high](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/high)
- [case undetermined](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/undetermined)
- [case low](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/low)
- [case medium](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/medium)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/argeotrackingstatus/accuracy-swift.enum/init(rawvalue:))
- [ARPointCloud](/documentation/arkit/arpointcloud)

##### Identifying Feature Points

- [var points: [simd_float3]](/documentation/arkit/arpointcloud/points-4vkif)
- [var identifiers: [UInt64]](/documentation/arkit/arpointcloud/identifiers-508tf)
- [ARDepthData](/documentation/arkit/ardepthdata)

##### Depth Information

- [var depthMap: CVPixelBuffer](/documentation/arkit/ardepthdata/depthmap)
- [var confidenceMap: CVPixelBuffer?](/documentation/arkit/ardepthdata/confidencemap)
- [ARConfidenceLevel](/documentation/arkit/arconfidencelevel)

###### Levels

- [case low](/documentation/arkit/arconfidencelevel/low)
- [case medium](/documentation/arkit/arconfidencelevel/medium)
- [case high](/documentation/arkit/arconfidencelevel/high)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arconfidencelevel/init(rawvalue:))

#### Raycasting

- [Placing objects and handling 3D interaction](/documentation/arkit/placing-objects-and-handling-3d-interaction)
- [ARRaycastQuery](/documentation/arkit/arraycastquery)

##### Creating a Raycast Query

- [init(origin: simd_float3, direction: simd_float3, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment)](/documentation/arkit/arraycastquery/init(origin:direction:allowing:alignment:))

##### Specifying the Target

- [var target: ARRaycastQuery.Target](/documentation/arkit/arraycastquery/target-swift.property)
- [ARRaycastQuery.Target](/documentation/arkit/arraycastquery/target-swift.enum)

###### Targets

- [case estimatedPlane](/documentation/arkit/arraycastquery/target-swift.enum/estimatedplane)
- [case existingPlaneGeometry](/documentation/arkit/arraycastquery/target-swift.enum/existingplanegeometry)
- [case existingPlaneInfinite](/documentation/arkit/arraycastquery/target-swift.enum/existingplaneinfinite)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arraycastquery/target-swift.enum/init(rawvalue:))
- [var targetAlignment: ARRaycastQuery.TargetAlignment](/documentation/arkit/arraycastquery/targetalignment-swift.property)
- [ARRaycastQuery.TargetAlignment](/documentation/arkit/arraycastquery/targetalignment-swift.enum)

###### Enumeration Cases

- [case any](/documentation/arkit/arraycastquery/targetalignment-swift.enum/any)
- [case horizontal](/documentation/arkit/arraycastquery/targetalignment-swift.enum/horizontal)
- [case vertical](/documentation/arkit/arraycastquery/targetalignment-swift.enum/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arraycastquery/targetalignment-swift.enum/init(rawvalue:))

##### Interpreting the Ray

- [var direction: simd_float3](/documentation/arkit/arraycastquery/direction)
- [var origin: simd_float3](/documentation/arkit/arraycastquery/origin)
- [ARTrackedRaycast](/documentation/arkit/artrackedraycast)

##### Stopping Tracking

- [func stopTracking()](/documentation/arkit/artrackedraycast/stoptracking())
- [ARRaycastResult](/documentation/arkit/arraycastresult)

##### Identifying Results

- [var worldTransform: simd_float4x4](/documentation/arkit/arraycastresult/worldtransform)
- [var anchor: ARAnchor?](/documentation/arkit/arraycastresult/anchor)
- [var target: ARRaycastQuery.Target](/documentation/arkit/arraycastresult/target)
- [ARRaycastQuery.Target](/documentation/arkit/arraycastquery/target-swift.enum)

###### Targets

- [case estimatedPlane](/documentation/arkit/arraycastquery/target-swift.enum/estimatedplane)
- [case existingPlaneGeometry](/documentation/arkit/arraycastquery/target-swift.enum/existingplanegeometry)
- [case existingPlaneInfinite](/documentation/arkit/arraycastquery/target-swift.enum/existingplaneinfinite)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arraycastquery/target-swift.enum/init(rawvalue:))
- [var targetAlignment: ARRaycastQuery.TargetAlignment](/documentation/arkit/arraycastresult/targetalignment)
- [ARRaycastQuery.TargetAlignment](/documentation/arkit/arraycastquery/targetalignment-swift.enum)

###### Enumeration Cases

- [case any](/documentation/arkit/arraycastquery/targetalignment-swift.enum/any)
- [case horizontal](/documentation/arkit/arraycastquery/targetalignment-swift.enum/horizontal)
- [case vertical](/documentation/arkit/arraycastquery/targetalignment-swift.enum/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arraycastquery/targetalignment-swift.enum/init(rawvalue:))

#### Hit-Testing

- [ARHitTestResult](/documentation/arkit/arhittestresult)

##### Identifying Results

- [var type: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/type)
- [ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype)

###### Creating a Result Type

- [init(rawValue: UInt)](/documentation/arkit/arhittestresult/resulttype/init(rawvalue:))

###### Result Types

- [static var featurePoint: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/featurepoint)
- [static var estimatedHorizontalPlane: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/estimatedhorizontalplane)
- [static var estimatedVerticalPlane: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/estimatedverticalplane)
- [static var existingPlane: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/existingplane)
- [static var existingPlaneUsingExtent: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/existingplaneusingextent)
- [static var existingPlaneUsingGeometry: ARHitTestResult.ResultType](/documentation/arkit/arhittestresult/resulttype/existingplaneusinggeometry)
- [var anchor: ARAnchor?](/documentation/arkit/arhittestresult/anchor)

##### Examining Result Geometry

- [var distance: CGFloat](/documentation/arkit/arhittestresult/distance)
- [var worldTransform: simd_float4x4](/documentation/arkit/arhittestresult/worldtransform)
- [var localTransform: simd_float4x4](/documentation/arkit/arhittestresult/localtransform)
- [Camera, Lighting, and Effects](/documentation/arkit/camera-lighting-and-effects)

#### Camera

- [ARCamera](/documentation/arkit/arcamera)

##### Handling Tracking Status

- [var trackingState: ARCamera.TrackingState](/documentation/arkit/arcamera/trackingstate-6i3pt)
- [ARCamera.TrackingState](/documentation/arkit/arcamera/trackingstate-swift.enum)

###### Determining the camera tracking status

- [case notAvailable](/documentation/arkit/arcamera/trackingstate-swift.enum/notavailable)
- [case limited(ARCamera.TrackingState.Reason)](/documentation/arkit/arcamera/trackingstate-swift.enum/limited(_:))
- [ARCamera.TrackingState.Reason](/documentation/arkit/arcamera/trackingstate-swift.enum/reason)

###### Inhibitors of Tracking Quality

- [case initializing](/documentation/arkit/arcamera/trackingstate-swift.enum/reason/initializing)
- [case relocalizing](/documentation/arkit/arcamera/trackingstate-swift.enum/reason/relocalizing)
- [case excessiveMotion](/documentation/arkit/arcamera/trackingstate-swift.enum/reason/excessivemotion)
- [case insufficientFeatures](/documentation/arkit/arcamera/trackingstate-swift.enum/reason/insufficientfeatures)
- [case normal](/documentation/arkit/arcamera/trackingstate-swift.enum/normal)

##### Examining Camera Geometry

- [var transform: simd_float4x4](/documentation/arkit/arcamera/transform)
- [var eulerAngles: simd_float3](/documentation/arkit/arcamera/eulerangles)

##### Examining Imaging Parameters

- [var imageResolution: CGSize](/documentation/arkit/arcamera/imageresolution)
- [var intrinsics: simd_float3x3](/documentation/arkit/arcamera/intrinsics)

##### Applying Camera Geometry

- [var projectionMatrix: simd_float4x4](/documentation/arkit/arcamera/projectionmatrix)
- [func projectionMatrix(for: UIInterfaceOrientation, viewportSize: CGSize, zNear: CGFloat, zFar: CGFloat) -> simd_float4x4](/documentation/arkit/arcamera/projectionmatrix(for:viewportsize:znear:zfar:))
- [func viewMatrix(for: UIInterfaceOrientation) -> simd_float4x4](/documentation/arkit/arcamera/viewmatrix(for:))
- [func projectPoint(simd_float3, orientation: UIInterfaceOrientation, viewportSize: CGSize) -> CGPoint](/documentation/arkit/arcamera/projectpoint(_:orientation:viewportsize:))
- [func unprojectPoint(CGPoint, ontoPlane: simd_float4x4, orientation: UIInterfaceOrientation, viewportSize: CGSize) -> simd_float3?](/documentation/arkit/arcamera/unprojectpoint(_:ontoplane:orientation:viewportsize:))

##### Applying Motion Blur

- [var exposureDuration: TimeInterval](/documentation/arkit/arcamera/exposureduration)

##### Applying Post-Processed Lighting

- [var exposureOffset: Float](/documentation/arkit/arcamera/exposureoffset)

#### Lighting Effects

- [Adding realistic reflections to an AR experience](/documentation/arkit/adding-realistic-reflections-to-an-ar-experience)
- [AREnvironmentProbeAnchor](/documentation/arkit/arenvironmentprobeanchor)

##### Creating Probe Anchors

- [init(transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(transform:extent:))
- [init(name: String, transform: simd_float4x4, extent: simd_float3)](/documentation/arkit/arenvironmentprobeanchor/init(name:transform:extent:))

##### Accessing Texture Maps

- [var environmentTexture: (any MTLTexture)?](/documentation/arkit/arenvironmentprobeanchor/environmenttexture)

##### Examining a Probe Anchor

- [var extent: simd_float3](/documentation/arkit/arenvironmentprobeanchor/extent)
- [ARLightEstimate](/documentation/arkit/arlightestimate)

##### Examining Light Parameters

- [var ambientIntensity: CGFloat](/documentation/arkit/arlightestimate/ambientintensity)
- [var ambientColorTemperature: CGFloat](/documentation/arkit/arlightestimate/ambientcolortemperature)
- [ARDirectionalLightEstimate](/documentation/arkit/ardirectionallightestimate)

##### Examining Light Parameters

- [var sphericalHarmonicsCoefficients: Data](/documentation/arkit/ardirectionallightestimate/sphericalharmonicscoefficients)
- [var primaryLightDirection: simd_float3](/documentation/arkit/ardirectionallightestimate/primarylightdirection)
- [var primaryLightIntensity: CGFloat](/documentation/arkit/ardirectionallightestimate/primarylightintensity)

#### Occlusion

- [Occluding virtual content with people](/documentation/arkit/occluding-virtual-content-with-people)
- [Effecting People Occlusion in Custom Renderers](/documentation/arkit/effecting-people-occlusion-in-custom-renderers)
- [Visualizing and interacting with a reconstructed scene](/documentation/arkit/visualizing-and-interacting-with-a-reconstructed-scene)
- [ARMatteGenerator](/documentation/arkit/armattegenerator)

##### Creating a Matte Generator

- [init(device: any MTLDevice, matteResolution: ARMatteGenerator.Resolution)](/documentation/arkit/armattegenerator/init(device:matteresolution:))

##### Creating an Alpha Matte Texture

- [func generateMatte(from: ARFrame, commandBuffer: any MTLCommandBuffer) -> any MTLTexture](/documentation/arkit/armattegenerator/generatematte(from:commandbuffer:))

##### Creating a Depth Texture

- [func generateDilatedDepth(from: ARFrame, commandBuffer: any MTLCommandBuffer) -> any MTLTexture](/documentation/arkit/armattegenerator/generatedilateddepth(from:commandbuffer:))

##### Controlling Resolution

- [ARMatteGenerator.Resolution](/documentation/arkit/armattegenerator/resolution)

###### Choosing a Resolution Option

- [case full](/documentation/arkit/armattegenerator/resolution/full)
- [case half](/documentation/arkit/armattegenerator/resolution/half)

###### Initializers

- [init?(rawValue: Int)](/documentation/arkit/armattegenerator/resolution/init(rawvalue:))
- [Data Management](/documentation/arkit/data-management)

#### Body Data

- [Capturing Body Motion in 3D](/documentation/arkit/capturing-body-motion-in-3d)
- [ARBody2D](/documentation/arkit/arbody2d)

##### Getting Joint Information

- [var skeleton: ARSkeleton2D](/documentation/arkit/arbody2d/skeleton)
- [ARSkeleton3D](/documentation/arkit/arskeleton3d)

##### Getting a Joint’s Pose

- [var jointLocalTransforms: [simd_float4x4]](/documentation/arkit/arskeleton3d/jointlocaltransforms-66gbm)
- [var jointModelTransforms: [simd_float4x4]](/documentation/arkit/arskeleton3d/jointmodeltransforms-i6yu)
- [func localTransform(for: ARSkeleton.JointName) -> simd_float4x4?](/documentation/arkit/arskeleton3d/localtransform(for:))
- [func modelTransform(for: ARSkeleton.JointName) -> simd_float4x4?](/documentation/arkit/arskeleton3d/modeltransform(for:))
- [ARSkeleton2D](/documentation/arkit/arskeleton2d)

##### Getting Joint Landmarks

- [var jointLandmarks: [simd_float2]](/documentation/arkit/arskeleton2d/jointlandmarks-12vkw)
- [func landmark(for: ARSkeleton.JointName) -> simd_float2?](/documentation/arkit/arskeleton2d/landmark(for:))
- [ARSkeleton](/documentation/arkit/arskeleton)

##### Getting Joint Information

- [var definition: ARSkeletonDefinition](/documentation/arkit/arskeleton/definition)
- [func isJointTracked(Int) -> Bool](/documentation/arkit/arskeleton/isjointtracked(_:))
- [ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname)

###### Creating a Joint Name

- [init(rawValue: String)](/documentation/arkit/arskeleton/jointname/init(rawvalue:))
- [init?(VNRecognizedPointKey)](/documentation/arkit/arskeleton/jointname/init(_:))
- [VNRecognizedPointKey](/documentation/vision/vnrecognizedpointkey)

###### Identifying Joints

- [static let root: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/root)
- [static let head: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/head)
- [static let leftFoot: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/leftfoot)
- [static let leftHand: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/lefthand)
- [static let leftShoulder: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/leftshoulder)
- [static let rightFoot: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/rightfoot)
- [static let rightHand: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/righthand)
- [static let rightShoulder: ARSkeleton.JointName](/documentation/arkit/arskeleton/jointname/rightshoulder)
- [ARSkeletonDefinition](/documentation/arkit/arskeletondefinition)

##### Locating in the Physical Environment

- [var neutralBodySkeleton3D: ARSkeleton3D?](/documentation/arkit/arskeletondefinition/neutralbodyskeleton3d)
- [class var defaultBody3D: ARSkeletonDefinition](/documentation/arkit/arskeletondefinition/defaultbody3d)

##### Locating in Screen Space

- [class var defaultBody2D: ARSkeletonDefinition](/documentation/arkit/arskeletondefinition/defaultbody2d)

##### Getting Joint Information

- [var jointNames: [String]](/documentation/arkit/arskeletondefinition/jointnames)
- [var jointCount: Int](/documentation/arkit/arskeletondefinition/jointcount)
- [func index(for: ARSkeleton.JointName) -> Int](/documentation/arkit/arskeletondefinition/index(for:))
- [var parentIndices: [Int]](/documentation/arkit/arskeletondefinition/parentindices-u2u9)

#### Face Data

- [Tracking and visualizing faces](/documentation/arkit/tracking-and-visualizing-faces)
- [Combining user face-tracking and world tracking](/documentation/arkit/combining-user-face-tracking-and-world-tracking)
- [ARFaceGeometry](/documentation/arkit/arfacegeometry)

##### Accessing Mesh Data

- [var vertices: [simd_float3]](/documentation/arkit/arfacegeometry/vertices-7qq1y)
- [var textureCoordinates: [vector_float2]](/documentation/arkit/arfacegeometry/texturecoordinates-u42d)
- [var triangleCount: Int](/documentation/arkit/arfacegeometry/trianglecount)
- [var triangleIndices: [Int16]](/documentation/arkit/arfacegeometry/triangleindices-8isy8)

##### Creating a Mesh from Blend Shapes

- [init?(blendShapes: [ARFaceAnchor.BlendShapeLocation : NSNumber])](/documentation/arkit/arfacegeometry/init(blendshapes:))
- [ARSCNFaceGeometry](/documentation/arkit/arscnfacegeometry)

##### Creating a Geometry

- [convenience init?(device: any MTLDevice)](/documentation/arkit/arscnfacegeometry/init(device:))
- [convenience init?(device: any MTLDevice, fillMesh: Bool)](/documentation/arkit/arscnfacegeometry/init(device:fillmesh:))

##### Updating the Geometry

- [func update(from: ARFaceGeometry)](/documentation/arkit/arscnfacegeometry/update(from:))

#### World Data

- [Saving and loading world data](/documentation/arkit/saving-and-loading-world-data)
- [ARWorldMap](/documentation/arkit/arworldmap)

##### Examining a World Map

- [var anchors: [ARAnchor]](/documentation/arkit/arworldmap/anchors)
- [var center: simd_float3](/documentation/arkit/arworldmap/center)
- [var extent: simd_float3](/documentation/arkit/arworldmap/extent)

##### Debugging a World Map

- [var rawFeaturePoints: ARPointCloud](/documentation/arkit/arworldmap/rawfeaturepoints)
- [Creating USD files for Apple devices](/documentation/usd/creating-usd-files-for-apple-devices)

### AR Quick Look

- [Previewing a Model with AR Quick Look](/documentation/arkit/previewing-a-model-with-ar-quick-look)
- [Adding Visual Effects in AR Quick Look and RealityKit](/documentation/arkit/adding-visual-effects-in-ar-quick-look-and-realitykit)
- [Adding an Apple Pay Button or a Custom Action in AR Quick Look](/documentation/arkit/adding-an-apple-pay-button-or-a-custom-action-in-ar-quick-look)
- [OpenUSD schemas for AR](/documentation/usd/usd-schemas-for-ar)
- [Specifying a lighting environment in AR Quick Look](/documentation/arkit/specifying-a-lighting-environment-in-ar-quick-look)

### Shared Experiences

- [Streaming an AR experience](/documentation/arkit/streaming-an-ar-experience)
- [Creating a collaborative session](/documentation/arkit/creating-a-collaborative-session)
- [Creating a multiuser AR experience](/documentation/arkit/creating-a-multiuser-ar-experience)
- [ARParticipantAnchor](/documentation/arkit/arparticipantanchor)
- [ARSession.CollaborationData](/documentation/arkit/arsession/collaborationdata)

#### Observing Priority

- [var priority: ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.property)
- [ARSession.CollaborationData.Priority](/documentation/arkit/arsession/collaborationdata/priority-swift.enum)

##### Enumeration Cases

- [case critical](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/critical)
- [case optional](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/optional)

##### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arsession/collaborationdata/priority-swift.enum/init(rawvalue:))

### Audio

- [Creating an immersive ar experience with audio](/documentation/arkit/creating-an-immersive-ar-experience-with-audio)

### Errors

- [ARError](/documentation/arkit/arerror)

#### Inspecting error information

- [static var errorDomain: String](/documentation/arkit/arerror/errordomain)

#### Identifying an error cause

- [ARError.Code](/documentation/arkit/arerror/code)

##### Errors

- [case requestFailed](/documentation/arkit/arerror/code/requestfailed)
- [case cameraUnauthorized](/documentation/arkit/arerror/code/cameraunauthorized)
- [case fileIOFailed](/documentation/arkit/arerror/code/fileiofailed)
- [case insufficientFeatures](/documentation/arkit/arerror/code/insufficientfeatures)
- [case invalidCollaborationData](/documentation/arkit/arerror/code/invalidcollaborationdata)
- [case invalidConfiguration](/documentation/arkit/arerror/code/invalidconfiguration)
- [case invalidReferenceImage](/documentation/arkit/arerror/code/invalidreferenceimage)
- [case invalidReferenceObject](/documentation/arkit/arerror/code/invalidreferenceobject)
- [case invalidWorldMap](/documentation/arkit/arerror/code/invalidworldmap)
- [case microphoneUnauthorized](/documentation/arkit/arerror/code/microphoneunauthorized)
- [case objectMergeFailed](/documentation/arkit/arerror/code/objectmergefailed)
- [case sensorFailed](/documentation/arkit/arerror/code/sensorfailed)
- [case sensorUnavailable](/documentation/arkit/arerror/code/sensorunavailable)
- [case unsupportedConfiguration](/documentation/arkit/arerror/code/unsupportedconfiguration)
- [case worldTrackingFailed](/documentation/arkit/arerror/code/worldtrackingfailed)
- [case geoTrackingFailed](/documentation/arkit/arerror/code/geotrackingfailed)
- [case geoTrackingNotAvailableAtLocation](/documentation/arkit/arerror/code/geotrackingnotavailableatlocation)
- [case locationUnauthorized](/documentation/arkit/arerror/code/locationunauthorized)
- [case highResolutionFrameCaptureFailed](/documentation/arkit/arerror/code/highresolutionframecapturefailed)
- [case highResolutionFrameCaptureInProgress](/documentation/arkit/arerror/code/highresolutionframecaptureinprogress)

##### Enumeration Cases

- [case networkConnectionFailure](/documentation/arkit/arerror/code/networkconnectionfailure)

##### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arerror/code/init(rawvalue:))
- [static var requestFailed: ARError.Code](/documentation/arkit/arerror/requestfailed)
- [static var cameraUnauthorized: ARError.Code](/documentation/arkit/arerror/cameraunauthorized)
- [static var fileIOFailed: ARError.Code](/documentation/arkit/arerror/fileiofailed)
- [static var insufficientFeatures: ARError.Code](/documentation/arkit/arerror/insufficientfeatures)
- [static var invalidCollaborationData: ARError.Code](/documentation/arkit/arerror/invalidcollaborationdata)
- [static var invalidConfiguration: ARError.Code](/documentation/arkit/arerror/invalidconfiguration)
- [static var invalidReferenceImage: ARError.Code](/documentation/arkit/arerror/invalidreferenceimage)
- [static var invalidReferenceObject: ARError.Code](/documentation/arkit/arerror/invalidreferenceobject)
- [static var invalidWorldMap: ARError.Code](/documentation/arkit/arerror/invalidworldmap)
- [static var microphoneUnauthorized: ARError.Code](/documentation/arkit/arerror/microphoneunauthorized)
- [static var objectMergeFailed: ARError.Code](/documentation/arkit/arerror/objectmergefailed)
- [static var sensorFailed: ARError.Code](/documentation/arkit/arerror/sensorfailed)
- [static var sensorUnavailable: ARError.Code](/documentation/arkit/arerror/sensorunavailable)
- [static var unsupportedConfiguration: ARError.Code](/documentation/arkit/arerror/unsupportedconfiguration)
- [static var worldTrackingFailed: ARError.Code](/documentation/arkit/arerror/worldtrackingfailed)
- [static var geoTrackingFailed: ARError.Code](/documentation/arkit/arerror/geotrackingfailed)
- [static var geoTrackingNotAvailableAtLocation: ARError.Code](/documentation/arkit/arerror/geotrackingnotavailableatlocation)
- [static var locationUnauthorized: ARError.Code](/documentation/arkit/arerror/locationunauthorized)
- [static var highResolutionFrameCaptureFailed: ARError.Code](/documentation/arkit/arerror/highresolutionframecapturefailed)
- [static var highResolutionFrameCaptureInProgress: ARError.Code](/documentation/arkit/arerror/highresolutionframecaptureinprogress)

#### Type Properties

- [static var networkConnectionFailure: ARError.Code](/documentation/arkit/arerror/networkconnectionfailure)
- [ARError.Code](/documentation/arkit/arerror/code)

#### Errors

- [case requestFailed](/documentation/arkit/arerror/code/requestfailed)
- [case cameraUnauthorized](/documentation/arkit/arerror/code/cameraunauthorized)
- [case fileIOFailed](/documentation/arkit/arerror/code/fileiofailed)
- [case insufficientFeatures](/documentation/arkit/arerror/code/insufficientfeatures)
- [case invalidCollaborationData](/documentation/arkit/arerror/code/invalidcollaborationdata)
- [case invalidConfiguration](/documentation/arkit/arerror/code/invalidconfiguration)
- [case invalidReferenceImage](/documentation/arkit/arerror/code/invalidreferenceimage)
- [case invalidReferenceObject](/documentation/arkit/arerror/code/invalidreferenceobject)
- [case invalidWorldMap](/documentation/arkit/arerror/code/invalidworldmap)
- [case microphoneUnauthorized](/documentation/arkit/arerror/code/microphoneunauthorized)
- [case objectMergeFailed](/documentation/arkit/arerror/code/objectmergefailed)
- [case sensorFailed](/documentation/arkit/arerror/code/sensorfailed)
- [case sensorUnavailable](/documentation/arkit/arerror/code/sensorunavailable)
- [case unsupportedConfiguration](/documentation/arkit/arerror/code/unsupportedconfiguration)
- [case worldTrackingFailed](/documentation/arkit/arerror/code/worldtrackingfailed)
- [case geoTrackingFailed](/documentation/arkit/arerror/code/geotrackingfailed)
- [case geoTrackingNotAvailableAtLocation](/documentation/arkit/arerror/code/geotrackingnotavailableatlocation)
- [case locationUnauthorized](/documentation/arkit/arerror/code/locationunauthorized)
- [case highResolutionFrameCaptureFailed](/documentation/arkit/arerror/code/highresolutionframecapturefailed)
- [case highResolutionFrameCaptureInProgress](/documentation/arkit/arerror/code/highresolutionframecaptureinprogress)

#### Enumeration Cases

- [case networkConnectionFailure](/documentation/arkit/arerror/code/networkconnectionfailure)

#### Initializers

- [init?(rawValue: Int)](/documentation/arkit/arerror/code/init(rawvalue:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
