# RoomPlan Documentation

Source: https://sosumi.ai/documentation/roomplan

---
title: RoomPlan
source: https://developer.apple.com/documentation/roomplan
timestamp: 2026-02-13T19:01:20.949Z
---

## Essentials

- [Create a 3D model of an interior room by guiding the user through an AR experience](/documentation/roomplan/create-a-3d-model-of-an-interior-room-by-guiding-the-user-through-an-ar-experience)

## User Interface

- [RoomCaptureView](/documentation/roomplan/roomcaptureview)

### Creating a room-capture view

- [init(frame: CGRect, arSession: ARSession)](/documentation/roomplan/roomcaptureview/init(frame:arsession:))
- [init(frame: CGRect)](/documentation/roomplan/roomcaptureview/init(frame:))
- [init?(coder: NSCoder)](/documentation/roomplan/roomcaptureview/init(coder:))

### Reacting to scan events

- [var captureSession: RoomCaptureSession!](/documentation/roomplan/roomcaptureview/capturesession)
- [var delegate: (any RoomCaptureViewDelegate)?](/documentation/roomplan/roomcaptureview/delegate)

### Displaying scan progress

- [var isModelEnabled: Bool](/documentation/roomplan/roomcaptureview/ismodelenabled)

### Accessing view features

- [var subviews: [UIView]](/documentation/roomplan/roomcaptureview/subviews)
- [func layoutSubviews()](/documentation/roomplan/roomcaptureview/layoutsubviews())
- [func encode(with: NSCoder)](/documentation/roomplan/roomcaptureview/encode(with:))
- [func traitCollectionDidChange(UITraitCollection?)](/documentation/roomplan/roomcaptureview/traitcollectiondidchange(_:))
- [RoomCaptureViewDelegate](/documentation/roomplan/roomcaptureviewdelegate)

### Post-processing scan results

- [func captureView(shouldPresent: CapturedRoomData, error: (any Error)?) -> Bool](/documentation/roomplan/roomcaptureviewdelegate/captureview(shouldpresent:error:))
- [func captureView(didPresent: CapturedRoom, error: (any Error)?)](/documentation/roomplan/roomcaptureviewdelegate/captureview(didpresent:error:))

### Default implementations

- [func captureView(shouldPresent: CapturedRoomData, error: (any Error)?) -> Bool](/documentation/roomplan/roomcaptureviewdelegate/captureview(shouldpresent:error:)-5l74q)
- [func captureView(didPresent: CapturedRoom, error: (any Error)?)](/documentation/roomplan/roomcaptureviewdelegate/captureview(didpresent:error:)-6em1r)

## Scanning Protocol

- [RoomCaptureSession](/documentation/roomplan/roomcapturesession)

### Creating a session

- [init(arSession: ARSession?)](/documentation/roomplan/roomcapturesession/init(arsession:))

### Ensuring device support

- [static var isSupported: Bool](/documentation/roomplan/roomcapturesession/issupported)

### Controlling a session

- [func run(configuration: RoomCaptureSession.Configuration)](/documentation/roomplan/roomcapturesession/run(configuration:))
- [RoomCaptureSession.Configuration](/documentation/roomplan/roomcapturesession/configuration)

#### Creating a configuration

- [init()](/documentation/roomplan/roomcapturesession/configuration/init())

#### Configuring a session

- [var isCoachingEnabled: Bool](/documentation/roomplan/roomcapturesession/configuration/iscoachingenabled)
- [func stop()](/documentation/roomplan/roomcapturesession/stop())
- [func stop(pauseARSession: Bool)](/documentation/roomplan/roomcapturesession/stop(pausearsession:))

### Responding to events

- [var delegate: (any RoomCaptureSessionDelegate)?](/documentation/roomplan/roomcapturesession/delegate)
- [RoomCaptureSession.CaptureError](/documentation/roomplan/roomcapturesession/captureerror)

#### Identifying the error cause

- [case deviceNotSupported](/documentation/roomplan/roomcapturesession/captureerror/devicenotsupported)
- [case deviceTooHot](/documentation/roomplan/roomcapturesession/captureerror/devicetoohot)
- [case exceedSceneSizeLimit](/documentation/roomplan/roomcapturesession/captureerror/exceedscenesizelimit)
- [case invalidARConfiguration](/documentation/roomplan/roomcapturesession/captureerror/invalidarconfiguration)
- [case worldTrackingFailure](/documentation/roomplan/roomcapturesession/captureerror/worldtrackingfailure)
- [case internalError](/documentation/roomplan/roomcapturesession/captureerror/internalerror)

#### Inspecting error information

- [var errorDescription: String?](/documentation/roomplan/roomcapturesession/captureerror/errordescription)

### Accessing the AR session

- [var arSession: ARSession](/documentation/roomplan/roomcapturesession/arsession)

### Displaying user instructions

- [RoomCaptureSession.Instruction](/documentation/roomplan/roomcapturesession/instruction)

#### Determining a coaching recommendation

- [case normal](/documentation/roomplan/roomcapturesession/instruction/normal)
- [case moveCloseToWall](/documentation/roomplan/roomcapturesession/instruction/moveclosetowall)
- [case moveAwayFromWall](/documentation/roomplan/roomcapturesession/instruction/moveawayfromwall)
- [case turnOnLight](/documentation/roomplan/roomcapturesession/instruction/turnonlight)
- [case slowDown](/documentation/roomplan/roomcapturesession/instruction/slowdown)
- [case lowTexture](/documentation/roomplan/roomcapturesession/instruction/lowtexture)

### Initializers

- [init()](/documentation/roomplan/roomcapturesession/init())
- [RoomCaptureSessionDelegate](/documentation/roomplan/roomcapturesessiondelegate)

### Beginning a session

- [func captureSession(RoomCaptureSession, didStartWith: RoomCaptureSession.Configuration)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didstartwith:))

### Updating a session

- [func captureSession(RoomCaptureSession, didAdd: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didadd:))
- [func captureSession(RoomCaptureSession, didRemove: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didremove:))
- [func captureSession(RoomCaptureSession, didChange: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didchange:))
- [func captureSession(RoomCaptureSession, didUpdate: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didupdate:))

### Coaching the user

- [func captureSession(RoomCaptureSession, didProvide: RoomCaptureSession.Instruction)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didprovide:))

### Completing a session

- [func captureSession(RoomCaptureSession, didEndWith: CapturedRoomData, error: (any Error)?)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didendwith:error:))

### Default implementations

- [func captureSession(RoomCaptureSession, didStartWith: RoomCaptureSession.Configuration)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didstartwith:)-3c74n)
- [func captureSession(RoomCaptureSession, didUpdate: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didupdate:)-77zyg)
- [func captureSession(RoomCaptureSession, didRemove: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didremove:)-9gs76)
- [func captureSession(RoomCaptureSession, didChange: CapturedRoom)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didchange:)-gv3t)
- [func captureSession(RoomCaptureSession, didProvide: RoomCaptureSession.Instruction)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didprovide:)-5hvhl)
- [func captureSession(RoomCaptureSession, didEndWith: CapturedRoomData, error: (any Error)?)](/documentation/roomplan/roomcapturesessiondelegate/capturesession(_:didendwith:error:)-5f0mc)

## Captured Data

- [Merging multiple scans into a single structure](/documentation/roomplan/merging-multiple-scans-into-a-single-structure)
- [Scanning the rooms of a single structure](/documentation/roomplan/scanning-the-rooms-of-a-single-structure)
- [CapturedRoom](/documentation/roomplan/capturedroom)

### Creating a captured room

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroom/init(from:))

### Inspecting room details

- [var identifier: UUID](/documentation/roomplan/capturedroom/identifier)
- [var story: Int](/documentation/roomplan/capturedroom/story)
- [var floors: [CapturedRoom.Surface]](/documentation/roomplan/capturedroom/floors)
- [CapturedRoom.Surface](/documentation/roomplan/capturedroom/surface)

#### Creating a surface

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroom/surface/init(from:))

#### Identifying a surface

- [var identifier: UUID](/documentation/roomplan/capturedroom/surface/identifier)
- [var parentIdentifier: UUID?](/documentation/roomplan/capturedroom/surface/parentidentifier)
- [var category: CapturedRoom.Surface.Category](/documentation/roomplan/capturedroom/surface/category-swift.property)
- [CapturedRoom.Surface.Category](/documentation/roomplan/capturedroom/surface/category-swift.enum)

##### Determining the surface category

- [case floor](/documentation/roomplan/capturedroom/surface/category-swift.enum/floor)
- [case door(isOpen: Bool)](/documentation/roomplan/capturedroom/surface/category-swift.enum/door(isopen:))
- [case opening](/documentation/roomplan/capturedroom/surface/category-swift.enum/opening)
- [case wall](/documentation/roomplan/capturedroom/surface/category-swift.enum/wall)
- [case window](/documentation/roomplan/capturedroom/surface/category-swift.enum/window)
- [var confidence: CapturedRoom.Confidence](/documentation/roomplan/capturedroom/surface/confidence)

#### Positioning and sizing a surface

- [var transform: simd_float4x4](/documentation/roomplan/capturedroom/surface/transform)
- [var dimensions: simd_float3](/documentation/roomplan/capturedroom/surface/dimensions)
- [var story: Int](/documentation/roomplan/capturedroom/surface/story)

#### Shaping a surface

- [var completedEdges: Set<CapturedRoom.Surface.Edge>](/documentation/roomplan/capturedroom/surface/completededges)
- [CapturedRoom.Surface.Edge](/documentation/roomplan/capturedroom/surface/edge)

##### Accessing edge types

- [case top](/documentation/roomplan/capturedroom/surface/edge/top)
- [case bottom](/documentation/roomplan/capturedroom/surface/edge/bottom)
- [case left](/documentation/roomplan/capturedroom/surface/edge/left)
- [case right](/documentation/roomplan/capturedroom/surface/edge/right)
- [var curve: CapturedRoom.Surface.Curve?](/documentation/roomplan/capturedroom/surface/curve-swift.property)
- [CapturedRoom.Surface.Curve](/documentation/roomplan/capturedroom/surface/curve-swift.struct)

##### Measuring a curve

- [var startAngle: Measurement<UnitAngle>](/documentation/roomplan/capturedroom/surface/curve-swift.struct/startangle)
- [var endAngle: Measurement<UnitAngle>](/documentation/roomplan/capturedroom/surface/curve-swift.struct/endangle)
- [var radius: Float](/documentation/roomplan/capturedroom/surface/curve-swift.struct/radius)

##### Instance Properties

- [var center: simd_float2](/documentation/roomplan/capturedroom/surface/curve-swift.struct/center)
- [var polygonCorners: [simd_float3]](/documentation/roomplan/capturedroom/surface/polygoncorners)

#### Serializing a surface

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedroom/surface/encode(to:))
- [var doors: [CapturedRoom.Surface]](/documentation/roomplan/capturedroom/doors)
- [var objects: [CapturedRoom.Object]](/documentation/roomplan/capturedroom/objects)
- [CapturedRoom.Object](/documentation/roomplan/capturedroom/object)

#### Creating an object

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroom/object/init(from:))

#### Identifying an object

- [var identifier: UUID](/documentation/roomplan/capturedroom/object/identifier)
- [var parentIdentifier: UUID?](/documentation/roomplan/capturedroom/object/parentidentifier)
- [var category: CapturedRoom.Object.Category](/documentation/roomplan/capturedroom/object/category-swift.property)
- [CapturedRoom.Object.Category](/documentation/roomplan/capturedroom/object/category-swift.enum)

##### Determining the object category

- [case bathtub](/documentation/roomplan/capturedroom/object/category-swift.enum/bathtub)
- [case bed](/documentation/roomplan/capturedroom/object/category-swift.enum/bed)
- [case chair](/documentation/roomplan/capturedroom/object/category-swift.enum/chair)
- [case dishwasher](/documentation/roomplan/capturedroom/object/category-swift.enum/dishwasher)
- [case fireplace](/documentation/roomplan/capturedroom/object/category-swift.enum/fireplace)
- [case oven](/documentation/roomplan/capturedroom/object/category-swift.enum/oven)
- [case refrigerator](/documentation/roomplan/capturedroom/object/category-swift.enum/refrigerator)
- [case sink](/documentation/roomplan/capturedroom/object/category-swift.enum/sink)
- [case sofa](/documentation/roomplan/capturedroom/object/category-swift.enum/sofa)
- [case stairs](/documentation/roomplan/capturedroom/object/category-swift.enum/stairs)
- [case storage](/documentation/roomplan/capturedroom/object/category-swift.enum/storage)
- [case stove](/documentation/roomplan/capturedroom/object/category-swift.enum/stove)
- [case table](/documentation/roomplan/capturedroom/object/category-swift.enum/table)
- [case television](/documentation/roomplan/capturedroom/object/category-swift.enum/television)
- [case toilet](/documentation/roomplan/capturedroom/object/category-swift.enum/toilet)
- [case washerDryer](/documentation/roomplan/capturedroom/object/category-swift.enum/washerdryer)

##### Determining supported attributes

- [var supportedAttributeTypes: [any CapturedRoomAttribute.Type]](/documentation/roomplan/capturedroom/object/category-swift.enum/supportedattributetypes)
- [var supportedCombinations: [[any CapturedRoomAttribute]]](/documentation/roomplan/capturedroom/object/category-swift.enum/supportedcombinations)
- [func supportsCombination([any CapturedRoomAttribute]) -> Bool](/documentation/roomplan/capturedroom/object/category-swift.enum/supportscombination(_:))
- [var confidence: CapturedRoom.Confidence](/documentation/roomplan/capturedroom/object/confidence)

#### Positioning and sizing an object

- [var transform: simd_float4x4](/documentation/roomplan/capturedroom/object/transform)
- [var dimensions: simd_float3](/documentation/roomplan/capturedroom/object/dimensions)
- [var story: Int](/documentation/roomplan/capturedroom/object/story)

#### Describing an object

- [var attributes: [any CapturedRoomAttribute]](/documentation/roomplan/capturedroom/object/attributes)
- [func attribute<T>(of: T.Type) -> T?](/documentation/roomplan/capturedroom/object/attribute(of:))

#### Serializing an object

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedroom/object/encode(to:))
- [var openings: [CapturedRoom.Surface]](/documentation/roomplan/capturedroom/openings)
- [var walls: [CapturedRoom.Surface]](/documentation/roomplan/capturedroom/walls)
- [var windows: [CapturedRoom.Surface]](/documentation/roomplan/capturedroom/windows)
- [var sections: [CapturedRoom.Section]](/documentation/roomplan/capturedroom/sections)
- [CapturedRoom.Section](/documentation/roomplan/capturedroom/section)

#### Creating a section

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroom/section/init(from:))

#### Describing a section

- [var label: CapturedRoom.Section.Label](/documentation/roomplan/capturedroom/section/label-swift.property)
- [CapturedRoom.Section.Label](/documentation/roomplan/capturedroom/section/label-swift.enum)

##### Assigning a section a label

- [case livingRoom](/documentation/roomplan/capturedroom/section/label-swift.enum/livingroom)
- [case kitchen](/documentation/roomplan/capturedroom/section/label-swift.enum/kitchen)
- [case diningRoom](/documentation/roomplan/capturedroom/section/label-swift.enum/diningroom)
- [case bedroom](/documentation/roomplan/capturedroom/section/label-swift.enum/bedroom)
- [case bathroom](/documentation/roomplan/capturedroom/section/label-swift.enum/bathroom)
- [case unidentified](/documentation/roomplan/capturedroom/section/label-swift.enum/unidentified)

#### Locating a section

- [var story: Int](/documentation/roomplan/capturedroom/section/story)
- [var center: simd_float3](/documentation/roomplan/capturedroom/section/center)

#### Serializing a section

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedroom/section/encode(to:))
- [CapturedRoom.Confidence](/documentation/roomplan/capturedroom/confidence)

#### Assessing a confidence value

- [case high](/documentation/roomplan/capturedroom/confidence/high)
- [case medium](/documentation/roomplan/capturedroom/confidence/medium)
- [case low](/documentation/roomplan/capturedroom/confidence/low)
- [var version: Int](/documentation/roomplan/capturedroom/version)

### Serializing a captured room

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedroom/encode(to:))
- [CapturedRoom.AttributesCodableRepresentation](/documentation/roomplan/capturedroom/attributescodablerepresentation)

#### Creating an attributes codable representation

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroom/attributescodablerepresentation/init(from:))
- [init(attributes: [any CapturedRoomAttribute])](/documentation/roomplan/capturedroom/attributescodablerepresentation/init(attributes:))

#### Accessing room attributes

- [let attributes: [any CapturedRoomAttribute]](/documentation/roomplan/capturedroom/attributescodablerepresentation/attributes)

### Generating a USDZ file

- [func export(to: URL, exportOptions: CapturedRoom.USDExportOptions) throws](/documentation/roomplan/capturedroom/export(to:exportoptions:))
- [func export(to: URL, metadataURL: URL?, modelProvider: CapturedRoom.ModelProvider?, exportOptions: CapturedRoom.USDExportOptions) throws](/documentation/roomplan/capturedroom/export(to:metadataurl:modelprovider:exportoptions:))
- [CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions)

#### Choosing an export option

- [static let parametric: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/parametric)
- [static let mesh: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/mesh)
- [static let model: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/model)

#### Creating an export option

- [init(rawValue: Int32)](/documentation/roomplan/capturedroom/usdexportoptions/init(rawvalue:))
- [let rawValue: Int32](/documentation/roomplan/capturedroom/usdexportoptions/rawvalue)
- [CapturedRoom.ModelProvider](/documentation/roomplan/capturedroom/modelprovider)

#### Creating a model provider

- [init()](/documentation/roomplan/capturedroom/modelprovider/init())

#### Managing models

- [var modelFileURLs: [URL]](/documentation/roomplan/capturedroom/modelprovider/modelfileurls)
- [func modelFileURL(for: CapturedRoom.Object.Category) throws -> URL?](/documentation/roomplan/capturedroom/modelprovider/modelfileurl(for:)-9irqx)
- [func modelFileURL(for: CapturedRoom.Object) throws -> URL?](/documentation/roomplan/capturedroom/modelprovider/modelfileurl(for:)-96rvb)
- [func modelFileURL(for: [any CapturedRoomAttribute]) throws -> URL?](/documentation/roomplan/capturedroom/modelprovider/modelfileurl(for:)-58ykp)
- [func setModelFileURL(URL?, for: [any CapturedRoomAttribute]) throws](/documentation/roomplan/capturedroom/modelprovider/setmodelfileurl(_:for:)-8xio)
- [func setModelFileURL(URL?, for: CapturedRoom.Object.Category) throws](/documentation/roomplan/capturedroom/modelprovider/setmodelfileurl(_:for:)-4law9)

#### Handling errors

- [CapturedRoom.ModelProvider.Error](/documentation/roomplan/capturedroom/modelprovider/error)

##### Interpreting the error

- [case attributeCombinationNotSupported](/documentation/roomplan/capturedroom/modelprovider/error/attributecombinationnotsupported)
- [case nonExistingFile(url: URL)](/documentation/roomplan/capturedroom/modelprovider/error/nonexistingfile(url:))

##### Inspecting error information

- [var errorDescription: String?](/documentation/roomplan/capturedroom/modelprovider/error/errordescription)

### Handling errors

- [CapturedRoom.Error](/documentation/roomplan/capturedroom/error)

#### Interpreting the error

- [case deviceNotSupported](/documentation/roomplan/capturedroom/error/devicenotsupported)
- [case urlInvalidFileExtension](/documentation/roomplan/capturedroom/error/urlinvalidfileextension)
- [case urlInvalidFilePath](/documentation/roomplan/capturedroom/error/urlinvalidfilepath)
- [case urlInvalidScheme](/documentation/roomplan/capturedroom/error/urlinvalidscheme)
- [case urlMissingFileExtension](/documentation/roomplan/capturedroom/error/urlmissingfileextension)

#### Inspecting error information

- [var errorDescription: String?](/documentation/roomplan/capturedroom/error/errordescription)
- [CapturedStructure](/documentation/roomplan/capturedstructure)

### Creating a captured room

- [init(from: any Decoder) throws](/documentation/roomplan/capturedstructure/init(from:))

### Inspecting structure details

- [var identifier: UUID](/documentation/roomplan/capturedstructure/identifier)
- [var rooms: [CapturedRoom]](/documentation/roomplan/capturedstructure/rooms)
- [var floors: [CapturedStructure.Surface]](/documentation/roomplan/capturedstructure/floors)
- [CapturedStructure.Surface](/documentation/roomplan/capturedstructure/surface)
- [var doors: [CapturedStructure.Surface]](/documentation/roomplan/capturedstructure/doors)
- [var objects: [CapturedStructure.Object]](/documentation/roomplan/capturedstructure/objects)
- [CapturedStructure.Object](/documentation/roomplan/capturedstructure/object)
- [var openings: [CapturedStructure.Surface]](/documentation/roomplan/capturedstructure/openings)
- [var walls: [CapturedStructure.Surface]](/documentation/roomplan/capturedstructure/walls)
- [var windows: [CapturedStructure.Surface]](/documentation/roomplan/capturedstructure/windows)
- [var sections: [CapturedStructure.Section]](/documentation/roomplan/capturedstructure/sections)
- [CapturedStructure.Section](/documentation/roomplan/capturedstructure/section)
- [var version: Int](/documentation/roomplan/capturedstructure/version)

### Serializing a captured structure

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedstructure/encode(to:))

### Generating a USDZ file

- [func export(to: URL, metadataURL: URL?, modelProvider: CapturedStructure.ModelProvider?, exportOptions: CapturedStructure.USDExportOptions) throws](/documentation/roomplan/capturedstructure/export(to:metadataurl:modelprovider:exportoptions:))
- [CapturedStructure.USDExportOptions](/documentation/roomplan/capturedstructure/usdexportoptions)
- [CapturedStructure.ModelProvider](/documentation/roomplan/capturedstructure/modelprovider)

### Handling errors

- [CapturedStructure.Error](/documentation/roomplan/capturedstructure/error)
- [CapturedRoomData](/documentation/roomplan/capturedroomdata)

### Deserializing a prior scan

- [init(from: any Decoder) throws](/documentation/roomplan/capturedroomdata/init(from:))

### Serializing a prior scan

- [func encode(to: any Encoder) throws](/documentation/roomplan/capturedroomdata/encode(to:))
- [Captured Object Attributes](/documentation/roomplan/captured-object-attributes)

### Accessing object details

- [CapturedRoomAttribute](/documentation/roomplan/capturedroomattribute)

#### Identifying an attribute

- [var shortIdentifier: String](/documentation/roomplan/capturedroomattribute/shortidentifier)

#### Determining an attribute’s category

- [static var parentCategory: CapturedElementCategory?](/documentation/roomplan/capturedroomattribute/parentcategory)
- [CapturedElementCategory](/documentation/roomplan/capturedelementcategory)

#### Determining the category type

- [case object(CapturedRoom.Object.Category)](/documentation/roomplan/capturedelementcategory/object(_:))
- [case surface(CapturedRoom.Surface.Category)](/documentation/roomplan/capturedelementcategory/surface(_:))

### Describing chairs

- [ChairType](/documentation/roomplan/chairtype)

#### Choosing a chair type

- [case dining](/documentation/roomplan/chairtype/dining)
- [case stool](/documentation/roomplan/chairtype/stool)
- [case swivel](/documentation/roomplan/chairtype/swivel)
- [case unidentified](/documentation/roomplan/chairtype/unidentified)
- [ChairArmType](/documentation/roomplan/chairarmtype)

#### Choosing a chair arm type

- [case existing](/documentation/roomplan/chairarmtype/existing)
- [case missing](/documentation/roomplan/chairarmtype/missing)
- [ChairLegType](/documentation/roomplan/chairlegtype)

#### Choosing a chair leg type

- [case four](/documentation/roomplan/chairlegtype/four)
- [case star](/documentation/roomplan/chairlegtype/star)
- [case unidentified](/documentation/roomplan/chairlegtype/unidentified)
- [ChairBackType](/documentation/roomplan/chairbacktype)

#### Choosing a chair back type

- [case existing](/documentation/roomplan/chairbacktype/existing)
- [case missing](/documentation/roomplan/chairbacktype/missing)

### Describing sofas

- [SofaType](/documentation/roomplan/sofatype)

#### Choosing a sofa type

- [case rectangular](/documentation/roomplan/sofatype/rectangular)
- [case singleSeat](/documentation/roomplan/sofatype/singleseat)
- [case lShaped](/documentation/roomplan/sofatype/lshaped)
- [case lShapedExtension](/documentation/roomplan/sofatype/lshapedextension)
- [case unidentified](/documentation/roomplan/sofatype/unidentified)

### Describing closets

- [StorageType](/documentation/roomplan/storagetype)

#### Choosing a storage area type

- [case cabinet](/documentation/roomplan/storagetype/cabinet)
- [case shelf](/documentation/roomplan/storagetype/shelf)

### Describing tables

- [TableType](/documentation/roomplan/tabletype)

#### Choosing a chair type

- [case dining](/documentation/roomplan/tabletype/dining)
- [case coffee](/documentation/roomplan/tabletype/coffee)
- [case unidentified](/documentation/roomplan/tabletype/unidentified)
- [TableShapeType](/documentation/roomplan/tableshapetype)

#### Choosing a chair type

- [case rectangular](/documentation/roomplan/tableshapetype/rectangular)
- [case circularElliptic](/documentation/roomplan/tableshapetype/circularelliptic)
- [case lShaped](/documentation/roomplan/tableshapetype/lshaped)
- [case unidentified](/documentation/roomplan/tableshapetype/unidentified)

## 3D Asset Output

- [Providing custom models for captured rooms and structure exports](/documentation/roomplan/providing-custom-models-for-captured-rooms-and-structure-exports)
- [RoomBuilder](/documentation/roomplan/roombuilder)

### Creating a room builder

- [init(options: RoomBuilder.ConfigurationOptions)](/documentation/roomplan/roombuilder/init(options:))
- [RoomBuilder.ConfigurationOptions](/documentation/roomplan/roombuilder/configurationoptions)

#### Creating a configuration option

- [init(rawValue: Int)](/documentation/roomplan/roombuilder/configurationoptions/init(rawvalue:))
- [let rawValue: Int](/documentation/roomplan/roombuilder/configurationoptions/rawvalue)

#### Choosing a configuration option

- [static let beautifyObjects: RoomBuilder.ConfigurationOptions](/documentation/roomplan/roombuilder/configurationoptions/beautifyobjects)

### Processing a prior scan

- [func capturedRoom(from: CapturedRoomData) async throws -> CapturedRoom](/documentation/roomplan/roombuilder/capturedroom(from:))

### Handling errors

- [RoomBuilder.BuildError](/documentation/roomplan/roombuilder/builderror)

#### Interpreting the error cause

- [case insufficientInput](/documentation/roomplan/roombuilder/builderror/insufficientinput)
- [case invalidInput](/documentation/roomplan/roombuilder/builderror/invalidinput)
- [case exceedSceneSizeLimit](/documentation/roomplan/roombuilder/builderror/exceedscenesizelimit)
- [case internalError](/documentation/roomplan/roombuilder/builderror/internalerror)
- [case deviceNotSupported](/documentation/roomplan/roombuilder/builderror/devicenotsupported)

#### Inspecting error information

- [var errorDescription: String?](/documentation/roomplan/roombuilder/builderror/errordescription)
- [StructureBuilder](/documentation/roomplan/structurebuilder)

### Creating a structure builder

- [init(options: StructureBuilder.ConfigurationOptions)](/documentation/roomplan/structurebuilder/init(options:))
- [StructureBuilder.ConfigurationOptions](/documentation/roomplan/structurebuilder/configurationoptions)

### Building a captured structure

- [func capturedStructure(from: [CapturedRoom]) async throws -> CapturedStructure](/documentation/roomplan/structurebuilder/capturedstructure(from:))

### Interpreting build errors

- [StructureBuilder.BuildError](/documentation/roomplan/structurebuilder/builderror)

#### Enumeration Cases

- [case deviceNotSupported](/documentation/roomplan/structurebuilder/builderror/devicenotsupported)
- [case exceedSceneSizeLimit](/documentation/roomplan/structurebuilder/builderror/exceedscenesizelimit)
- [case insufficientInput](/documentation/roomplan/structurebuilder/builderror/insufficientinput)
- [case internalError](/documentation/roomplan/structurebuilder/builderror/internalerror)
- [case invalidInput](/documentation/roomplan/structurebuilder/builderror/invalidinput)
- [case invalidRoomLocation](/documentation/roomplan/structurebuilder/builderror/invalidroomlocation)

#### Instance Properties

- [var errorDescription: String?](/documentation/roomplan/structurebuilder/builderror/errordescription)
- [CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions)

### Choosing an export option

- [static let parametric: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/parametric)
- [static let mesh: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/mesh)
- [static let model: CapturedRoom.USDExportOptions](/documentation/roomplan/capturedroom/usdexportoptions/model)

### Creating an export option

- [init(rawValue: Int32)](/documentation/roomplan/capturedroom/usdexportoptions/init(rawvalue:))
- [let rawValue: Int32](/documentation/roomplan/capturedroom/usdexportoptions/rawvalue)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
