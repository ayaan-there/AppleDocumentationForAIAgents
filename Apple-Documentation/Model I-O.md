# ModelIO Documentation

Source: https://sosumi.ai/documentation/modelio

---
title: Model I/O
source: https://developer.apple.com/documentation/modelio
timestamp: 2026-02-13T19:57:58.286Z
---

## 3D Asset Basics

- [MDLAsset](/documentation/modelio/mdlasset)

### Creating an Asset

- [class func canImportFileExtension(String) -> Bool](/documentation/modelio/mdlasset/canimportfileextension(_:))
- [init(url: URL)](/documentation/modelio/mdlasset/init(url:))
- [init(bufferAllocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlasset/init(bufferallocator:))
- [init(url: URL?, vertexDescriptor: MDLVertexDescriptor?, bufferAllocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlasset/init(url:vertexdescriptor:bufferallocator:))
- [init(url: URL, vertexDescriptor: MDLVertexDescriptor?, bufferAllocator: (any MDLMeshBufferAllocator)?, preserveTopology: Bool, error: NSErrorPointer)](/documentation/modelio/mdlasset/init(url:vertexdescriptor:bufferallocator:preservetopology:error:))

### Exporting an Asset

- [class func canExportFileExtension(String) -> Bool](/documentation/modelio/mdlasset/canexportfileextension(_:))
- [func export(to: URL) throws](/documentation/modelio/mdlasset/export(to:))

### Working with Asset Content

- [func object(at: Int) -> MDLObject](/documentation/modelio/mdlasset/object(at:))
- [subscript(Int) -> MDLObject?](/documentation/modelio/mdlasset/subscript(_:))
- [var count: Int](/documentation/modelio/mdlasset/count)
- [func childObjects(of: AnyClass) -> [MDLObject]](/documentation/modelio/mdlasset/childobjects(of:))
- [func add(MDLObject)](/documentation/modelio/mdlasset/add(_:))
- [func remove(MDLObject)](/documentation/modelio/mdlasset/remove(_:))
- [var boundingBox: MDLAxisAlignedBoundingBox](/documentation/modelio/mdlasset/boundingbox)
- [func boundingBox(atTime: TimeInterval) -> MDLAxisAlignedBoundingBox](/documentation/modelio/mdlasset/boundingbox(attime:))
- [var url: URL?](/documentation/modelio/mdlasset/url)
- [var bufferAllocator: any MDLMeshBufferAllocator](/documentation/modelio/mdlasset/bufferallocator)
- [var vertexDescriptor: MDLVertexDescriptor?](/documentation/modelio/mdlasset/vertexdescriptor)
- [var masters: any MDLObjectContainerComponent](/documentation/modelio/mdlasset/masters)

### Working with Timed Information

- [var frameInterval: TimeInterval](/documentation/modelio/mdlasset/frameinterval)
- [var startTime: TimeInterval](/documentation/modelio/mdlasset/starttime)
- [var endTime: TimeInterval](/documentation/modelio/mdlasset/endtime)

### Working with Lights

- [class func placeLightProbes(withDensity: Float, heuristic: MDLProbePlacement, using: any MDLLightProbeIrradianceDataSource) -> [MDLLightProbe]](/documentation/modelio/mdlasset/placelightprobes(withdensity:heuristic:using:))
- [MDLProbePlacement](/documentation/modelio/mdlprobeplacement)

#### Constants

- [case irradianceDistribution](/documentation/modelio/mdlprobeplacement/irradiancedistribution)
- [case uniformGrid](/documentation/modelio/mdlprobeplacement/uniformgrid)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdlprobeplacement/init(rawvalue:))

### Constants

- [Asset File Types](/documentation/modelio/asset-file-types)

#### Constants

- [let kUTTypeAlembic: String](/documentation/modelio/kuttypealembic)
- [let kUTType3dObject: String](/documentation/modelio/kuttype3dobject)
- [let kUTTypePolygon: String](/documentation/modelio/kuttypepolygon)
- [let kUTTypeStereolithography: String](/documentation/modelio/kuttypestereolithography)
- [let kUTTypeUniversalSceneDescription: String](/documentation/modelio/kuttypeuniversalscenedescription)

### Instance Properties

- [var animations: any MDLObjectContainerComponent](/documentation/modelio/mdlasset/animations)
- [var originals: any MDLObjectContainerComponent](/documentation/modelio/mdlasset/originals)
- [var resolver: (any MDLAssetResolver)?](/documentation/modelio/mdlasset/resolver)
- [var upAxis: vector_float3](/documentation/modelio/mdlasset/upaxis)

### Instance Methods

- [func loadTextures()](/documentation/modelio/mdlasset/loadtextures())
- [func object(atPath: String) -> MDLObject](/documentation/modelio/mdlasset/object(atpath:))
- [MDLObject](/documentation/modelio/mdlobject)

### Customizing Objects with Components

- [func componentConforming(to: Protocol) -> (any MDLComponent)?](/documentation/modelio/mdlobject/componentconforming(to:))
- [func setComponent(any MDLComponent, for: Protocol)](/documentation/modelio/mdlobject/setcomponent(_:for:))

### Working with Object Hierarchies

- [var parent: MDLObject?](/documentation/modelio/mdlobject/parent)
- [var children: any MDLObjectContainerComponent](/documentation/modelio/mdlobject/children)
- [func addChild(MDLObject)](/documentation/modelio/mdlobject/addchild(_:))
- [func enumerateChildObjects(of: AnyClass, root: MDLObject, using: (MDLObject, UnsafeMutablePointer<ObjCBool>) -> Void, stopPointer: UnsafeMutablePointer<ObjCBool>)](/documentation/modelio/mdlobject/enumeratechildobjects(of:root:using:stoppointer:))
- [var path: String](/documentation/modelio/mdlobject/path)
- [func atPath(String) -> MDLObject](/documentation/modelio/mdlobject/atpath(_:))

### Working with Objects in Space

- [func boundingBox(atTime: TimeInterval) -> MDLAxisAlignedBoundingBox](/documentation/modelio/mdlobject/boundingbox(attime:))
- [var transform: (any MDLTransformComponent)?](/documentation/modelio/mdlobject/transform)

### Managing Rendering Intent

- [var hidden: Bool](/documentation/modelio/mdlobject/hidden)
- [var instance: MDLObject?](/documentation/modelio/mdlobject/instance)
- [var path: String](/documentation/modelio/mdlobject/path)
- [var components: [any MDLComponent]](/documentation/modelio/mdlobject/components)

### Object Instancing

- [func atPath(String) -> MDLObject](/documentation/modelio/mdlobject/atpath(_:))
- [func enumerateChildObjects(of: AnyClass, root: MDLObject, using: (MDLObject, UnsafeMutablePointer<ObjCBool>) -> Void, stopPointer: UnsafeMutablePointer<ObjCBool>)](/documentation/modelio/mdlobject/enumeratechildobjects(of:root:using:stoppointer:))
- [subscript(Protocol) -> (any MDLComponent)?](/documentation/modelio/mdlobject/subscript(_:))

### Constants

- [MDLAxisAlignedBoundingBox](/documentation/modelio/mdlaxisalignedboundingbox)

#### Initializers

- [init()](/documentation/modelio/mdlaxisalignedboundingbox/init())
- [init(maxBounds: vector_float3, minBounds: vector_float3)](/documentation/modelio/mdlaxisalignedboundingbox/init(maxbounds:minbounds:))

#### Instance Properties

- [var maxBounds: vector_float3](/documentation/modelio/mdlaxisalignedboundingbox/maxbounds)
- [var minBounds: vector_float3](/documentation/modelio/mdlaxisalignedboundingbox/minbounds)
- [MDLTransform](/documentation/modelio/mdltransform)

### Creating a Transform Object

- [convenience init(identity: ())](/documentation/modelio/mdltransform/init(identity:))
- [convenience init(matrix: matrix_float4x4)](/documentation/modelio/mdltransform/init(matrix:))
- [convenience init(transformComponent: any MDLTransformComponent)](/documentation/modelio/mdltransform/init(transformcomponent:))
- [convenience init(matrix: matrix_float4x4, resetsTransform: Bool)](/documentation/modelio/mdltransform/init(matrix:resetstransform:))
- [convenience init(transformComponent: any MDLTransformComponent, resetsTransform: Bool)](/documentation/modelio/mdltransform/init(transformcomponent:resetstransform:))

### Using Factors of a Static Transform

- [var translation: vector_float3](/documentation/modelio/mdltransform/translation)
- [var rotation: vector_float3](/documentation/modelio/mdltransform/rotation)
- [var scale: vector_float3](/documentation/modelio/mdltransform/scale)
- [var shear: vector_float3](/documentation/modelio/mdltransform/shear)
- [func setIdentity()](/documentation/modelio/mdltransform/setidentity())

### Using Factors of an Animated Transform

- [func translation(atTime: TimeInterval) -> vector_float3](/documentation/modelio/mdltransform/translation(attime:))
- [func setTranslation(vector_float3, forTime: TimeInterval)](/documentation/modelio/mdltransform/settranslation(_:fortime:))
- [func rotation(atTime: TimeInterval) -> vector_float3](/documentation/modelio/mdltransform/rotation(attime:))
- [func rotationMatrix(atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdltransform/rotationmatrix(attime:))
- [func setRotation(vector_float3, forTime: TimeInterval)](/documentation/modelio/mdltransform/setrotation(_:fortime:))
- [func scale(atTime: TimeInterval) -> vector_float3](/documentation/modelio/mdltransform/scale(attime:))
- [func setScale(vector_float3, forTime: TimeInterval)](/documentation/modelio/mdltransform/setscale(_:fortime:))
- [func shear(atTime: TimeInterval) -> vector_float3](/documentation/modelio/mdltransform/shear(attime:))
- [func setShear(vector_float3, forTime: TimeInterval)](/documentation/modelio/mdltransform/setshear(_:fortime:))
- [func setMatrix(matrix_float4x4, forTime: TimeInterval)](/documentation/modelio/mdltransform/setmatrix(_:fortime:))

### Initializers

- [init()](/documentation/modelio/mdltransform/init())
- [MDLMesh](/documentation/modelio/mdlmesh)

### Creating a Custom Mesh

- [init(vertexBuffer: any MDLMeshBuffer, vertexCount: Int, descriptor: MDLVertexDescriptor, submeshes: [MDLSubmesh])](/documentation/modelio/mdlmesh/init(vertexbuffer:vertexcount:descriptor:submeshes:))
- [init(vertexBuffers: [any MDLMeshBuffer], vertexCount: Int, descriptor: MDLVertexDescriptor, submeshes: [MDLSubmesh])](/documentation/modelio/mdlmesh/init(vertexbuffers:vertexcount:descriptor:submeshes:))
- [init(bufferAllocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(bufferallocator:))
- [class func newSubdividedMesh(MDLMesh, submeshIndex: Int, subdivisionLevels: Int) -> Self?](/documentation/modelio/mdlmesh/newsubdividedmesh(_:submeshindex:subdivisionlevels:))
- [init(meshBySubdividingMesh: MDLMesh, submeshIndex: Int32, subdivisionLevels: UInt32, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(meshbysubdividingmesh:submeshindex:subdivisionlevels:allocator:))

### Working with Vertex Data

- [var boundingBox: MDLAxisAlignedBoundingBox](/documentation/modelio/mdlmesh/boundingbox)
- [var submeshes: NSMutableArray?](/documentation/modelio/mdlmesh/submeshes)
- [var vertexBuffers: [any MDLMeshBuffer]](/documentation/modelio/mdlmesh/vertexbuffers)
- [var vertexCount: Int](/documentation/modelio/mdlmesh/vertexcount)
- [var vertexDescriptor: MDLVertexDescriptor](/documentation/modelio/mdlmesh/vertexdescriptor)
- [var allocator: any MDLMeshBufferAllocator](/documentation/modelio/mdlmesh/allocator)
- [func addAttribute(withName: String, format: MDLVertexFormat)](/documentation/modelio/mdlmesh/addattribute(withname:format:))
- [func addAttribute(withName: String, format: MDLVertexFormat, type: String, data: Data, stride: Int)](/documentation/modelio/mdlmesh/addattribute(withname:format:type:data:stride:))
- [func addAttribute(withName: String, format: MDLVertexFormat, type: String, data: Data, stride: Int, time: TimeInterval)](/documentation/modelio/mdlmesh/addattribute(withname:format:type:data:stride:time:))
- [func removeAttributeNamed(String)](/documentation/modelio/mdlmesh/removeattributenamed(_:))
- [func replaceAttributeNamed(String, with: MDLVertexAttributeData)](/documentation/modelio/mdlmesh/replaceattributenamed(_:with:))
- [func updateAttributeNamed(String, with: MDLVertexAttributeData)](/documentation/modelio/mdlmesh/updateattributenamed(_:with:))
- [func addUnwrappedTextureCoordinates(forAttributeNamed: String)](/documentation/modelio/mdlmesh/addunwrappedtexturecoordinates(forattributenamed:))
- [func vertexAttributeData(forAttributeNamed: String) -> MDLVertexAttributeData?](/documentation/modelio/mdlmesh/vertexattributedata(forattributenamed:))
- [func vertexAttributeData(forAttributeNamed: String, as: MDLVertexFormat) -> MDLVertexAttributeData?](/documentation/modelio/mdlmesh/vertexattributedata(forattributenamed:as:))

### Generating Geometry Data

- [func addNormals(withAttributeNamed: String?, creaseThreshold: Float)](/documentation/modelio/mdlmesh/addnormals(withattributenamed:creasethreshold:))
- [func addTangentBasis(forTextureCoordinateAttributeNamed: String, tangentAttributeNamed: String, bitangentAttributeNamed: String?)](/documentation/modelio/mdlmesh/addtangentbasis(fortexturecoordinateattributenamed:tangentattributenamed:bitangentattributenamed:))
- [func addTangentBasis(forTextureCoordinateAttributeNamed: String, normalAttributeNamed: String, tangentAttributeNamed: String)](/documentation/modelio/mdlmesh/addtangentbasis(fortexturecoordinateattributenamed:normalattributenamed:tangentattributenamed:))
- [func makeVerticesUnique()](/documentation/modelio/mdlmesh/makeverticesunique())

### Generating Ambient Occlusion Data

- [func generateAmbientOcclusionTexture(withQuality: Float, attenuationFactor: Float, objectsToConsider: [MDLObject], vertexAttributeNamed: String, materialPropertyNamed: String) -> Bool](/documentation/modelio/mdlmesh/generateambientocclusiontexture(withquality:attenuationfactor:objectstoconsider:vertexattributenamed:materialpropertynamed:))
- [func generateAmbientOcclusionTexture(withSize: vector_int2, raysPerSample: Int, attenuationFactor: Float, objectsToConsider: [MDLObject], vertexAttributeNamed: String, materialPropertyNamed: String) -> Bool](/documentation/modelio/mdlmesh/generateambientocclusiontexture(withsize:rayspersample:attenuationfactor:objectstoconsider:vertexattributenamed:materialpropertynamed:))
- [func generateAmbientOcclusionVertexColors(withQuality: Float, attenuationFactor: Float, objectsToConsider: [MDLObject], vertexAttributeNamed: String) -> Bool](/documentation/modelio/mdlmesh/generateambientocclusionvertexcolors(withquality:attenuationfactor:objectstoconsider:vertexattributenamed:))
- [func generateAmbientOcclusionVertexColors(withRaysPerSample: Int, attenuationFactor: Float, objectsToConsider: [MDLObject], vertexAttributeNamed: String) -> Bool](/documentation/modelio/mdlmesh/generateambientocclusionvertexcolors(withrayspersample:attenuationfactor:objectstoconsider:vertexattributenamed:))

### Generating Light Map Data

- [func generateLightMapTexture(withQuality: Float, lightsToConsider: [MDLLight], objectsToConsider: [MDLObject], vertexAttributeNamed: String, materialPropertyNamed: String) -> Bool](/documentation/modelio/mdlmesh/generatelightmaptexture(withquality:lightstoconsider:objectstoconsider:vertexattributenamed:materialpropertynamed:))
- [func generateLightMapTexture(withTextureSize: vector_int2, lightsToConsider: [MDLLight], objectsToConsider: [MDLObject], vertexAttributeNamed: String, materialPropertyNamed: String) -> Bool](/documentation/modelio/mdlmesh/generatelightmaptexture(withtexturesize:lightstoconsider:objectstoconsider:vertexattributenamed:materialpropertynamed:))
- [func generateLightMapVertexColorsWithLights(toConsider: [MDLLight], objectsToConsider: [MDLObject], vertexAttributeNamed: String) -> Bool](/documentation/modelio/mdlmesh/generatelightmapvertexcolorswithlights(toconsider:objectstoconsider:vertexattributenamed:))

### Creating Parametric Meshes

- [class func newBox(withDimensions: vector_float3, segments: vector_uint3, geometryType: MDLGeometryType, inwardNormals: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newbox(withdimensions:segments:geometrytype:inwardnormals:allocator:))
- [class func newEllipsoid(withRadii: vector_float3, radialSegments: Int, verticalSegments: Int, geometryType: MDLGeometryType, inwardNormals: Bool, hemisphere: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newellipsoid(withradii:radialsegments:verticalsegments:geometrytype:inwardnormals:hemisphere:allocator:))
- [class func newCylinder(withHeight: Float, radii: vector_float2, radialSegments: Int, verticalSegments: Int, geometryType: MDLGeometryType, inwardNormals: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newcylinder(withheight:radii:radialsegments:verticalsegments:geometrytype:inwardnormals:allocator:))
- [class func newEllipticalCone(withHeight: Float, radii: vector_float2, radialSegments: Int, verticalSegments: Int, geometryType: MDLGeometryType, inwardNormals: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newellipticalcone(withheight:radii:radialsegments:verticalsegments:geometrytype:inwardnormals:allocator:))
- [class func newPlane(withDimensions: vector_float2, segments: vector_uint2, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newplane(withdimensions:segments:geometrytype:allocator:))
- [class func newCapsule(withHeight: Float, radii: vector_float2, radialSegments: Int, verticalSegments: Int, hemisphereSegments: Int, geometryType: MDLGeometryType, inwardNormals: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newcapsule(withheight:radii:radialsegments:verticalsegments:hemispheresegments:geometrytype:inwardnormals:allocator:))
- [class func newIcosahedron(withRadius: Float, inwardNormals: Bool, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newicosahedron(withradius:inwardnormals:allocator:))
- [class func newIcosahedron(withRadius: Float, inwardNormals: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?) -> Self](/documentation/modelio/mdlmesh/newicosahedron(withradius:inwardnormals:geometrytype:allocator:))
- [init(boxWithExtent: vector_float3, segments: vector_uint3, inwardNormals: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(boxwithextent:segments:inwardnormals:geometrytype:allocator:))
- [init(sphereWithExtent: vector_float3, segments: vector_uint2, inwardNormals: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(spherewithextent:segments:inwardnormals:geometrytype:allocator:))
- [init(cylinderWithExtent: vector_float3, segments: vector_uint2, inwardNormals: Bool, topCap: Bool, bottomCap: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(cylinderwithextent:segments:inwardnormals:topcap:bottomcap:geometrytype:allocator:))
- [init(coneWithExtent: vector_float3, segments: vector_uint2, inwardNormals: Bool, cap: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(conewithextent:segments:inwardnormals:cap:geometrytype:allocator:))
- [init(planeWithExtent: vector_float3, segments: vector_uint2, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(planewithextent:segments:geometrytype:allocator:))
- [init(icosahedronWithExtent: vector_float3, inwardNormals: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(icosahedronwithextent:inwardnormals:geometrytype:allocator:))
- [init(capsuleWithExtent: vector_float3, cylinderSegments: vector_uint2, hemisphereSegments: Int32, inwardNormals: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(capsulewithextent:cylindersegments:hemispheresegments:inwardnormals:geometrytype:allocator:))
- [init(hemisphereWithExtent: vector_float3, segments: vector_uint2, inwardNormals: Bool, cap: Bool, geometryType: MDLGeometryType, allocator: (any MDLMeshBufferAllocator)?)](/documentation/modelio/mdlmesh/init(hemispherewithextent:segments:inwardnormals:cap:geometrytype:allocator:))

### Instance Methods

- [func addOrthTanBasis(forTextureCoordinateAttributeNamed: String, normalAttributeNamed: String, tangentAttributeNamed: String)](/documentation/modelio/mdlmesh/addorthtanbasis(fortexturecoordinateattributenamed:normalattributenamed:tangentattributenamed:))
- [func flipTextureCoordinates(inAttributeNamed: String)](/documentation/modelio/mdlmesh/fliptexturecoordinates(inattributenamed:))
- [func makeVerticesUniqueAndReturnError() throws](/documentation/modelio/mdlmesh/makeverticesuniqueandreturnerror())
- [MDLSubmesh](/documentation/modelio/mdlsubmesh)

### Creating a Submesh

- [init(indexBuffer: any MDLMeshBuffer, indexCount: Int, indexType: MDLIndexBitDepth, geometryType: MDLGeometryType, material: MDLMaterial?)](/documentation/modelio/mdlsubmesh/init(indexbuffer:indexcount:indextype:geometrytype:material:))
- [init(name: String, indexBuffer: any MDLMeshBuffer, indexCount: Int, indexType: MDLIndexBitDepth, geometryType: MDLGeometryType, material: MDLMaterial?)](/documentation/modelio/mdlsubmesh/init(name:indexbuffer:indexcount:indextype:geometrytype:material:))
- [init(name: String, indexBuffer: any MDLMeshBuffer, indexCount: Int, indexType: MDLIndexBitDepth, geometryType: MDLGeometryType, material: MDLMaterial?, topology: MDLSubmeshTopology?)](/documentation/modelio/mdlsubmesh/init(name:indexbuffer:indexcount:indextype:geometrytype:material:topology:))
- [init?(mdlSubmesh: MDLSubmesh, indexType: MDLIndexBitDepth, geometryType: MDLGeometryType)](/documentation/modelio/mdlsubmesh/init(mdlsubmesh:indextype:geometrytype:))

### Working with a Submesh’s Index Buffer

- [var indexBuffer: any MDLMeshBuffer](/documentation/modelio/mdlsubmesh/indexbuffer)
- [var indexCount: Int](/documentation/modelio/mdlsubmesh/indexcount)
- [var indexType: MDLIndexBitDepth](/documentation/modelio/mdlsubmesh/indextype)
- [var geometryType: MDLGeometryType](/documentation/modelio/mdlsubmesh/geometrytype)
- [var topology: MDLSubmeshTopology?](/documentation/modelio/mdlsubmesh/topology)
- [func indexBuffer(asIndexType: MDLIndexBitDepth) -> any MDLMeshBuffer](/documentation/modelio/mdlsubmesh/indexbuffer(asindextype:))

### Associating Materials with a Submesh

- [var material: MDLMaterial?](/documentation/modelio/mdlsubmesh/material)

### Identifying a Submesh

- [var name: String](/documentation/modelio/mdlsubmesh/name)

### Constants

- [MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth)

#### Constants

- [case invalid](/documentation/modelio/mdlindexbitdepth/invalid)
- [case uInt8](/documentation/modelio/mdlindexbitdepth/uint8-swift.enum.case)
- [case uInt16](/documentation/modelio/mdlindexbitdepth/uint16-swift.enum.case)
- [case uInt32](/documentation/modelio/mdlindexbitdepth/uint32-swift.enum.case)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlindexbitdepth/init(rawvalue:))

#### Type Properties

- [static var uint16: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint16-swift.type.property)
- [static var uint32: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint32-swift.type.property)
- [static var uint8: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint8-swift.type.property)
- [MDLGeometryType](/documentation/modelio/mdlgeometrytype)

#### Constants

- [case points](/documentation/modelio/mdlgeometrytype/points)
- [case lines](/documentation/modelio/mdlgeometrytype/lines)
- [case triangles](/documentation/modelio/mdlgeometrytype/triangles)
- [case triangleStrips](/documentation/modelio/mdlgeometrytype/trianglestrips)
- [case quads](/documentation/modelio/mdlgeometrytype/quads)
- [case variableTopology](/documentation/modelio/mdlgeometrytype/variabletopology)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdlgeometrytype/init(rawvalue:))
- [MDLSubmeshTopology](/documentation/modelio/mdlsubmeshtopology)

### Identifying Faces

- [var faceTopology: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/facetopology)
- [var faceCount: Int](/documentation/modelio/mdlsubmeshtopology/facecount)

### Identifying Creases

- [var edgeCreaseIndices: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/edgecreaseindices)
- [var edgeCreases: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/edgecreases)
- [var edgeCreaseCount: Int](/documentation/modelio/mdlsubmeshtopology/edgecreasecount)
- [var vertexCreaseIndices: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/vertexcreaseindices)
- [var vertexCreases: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/vertexcreases)
- [var vertexCreaseCount: Int](/documentation/modelio/mdlsubmeshtopology/vertexcreasecount)

### Identifying Holes

- [var holes: (any MDLMeshBuffer)?](/documentation/modelio/mdlsubmeshtopology/holes)
- [var holeCount: Int](/documentation/modelio/mdlsubmeshtopology/holecount)

### Initializers

- [init(submesh: MDLSubmesh)](/documentation/modelio/mdlsubmeshtopology/init(submesh:))
- [MDLNamed](/documentation/modelio/mdlnamed)

### Naming an Object

- [var name: String](/documentation/modelio/mdlnamed/name)

## Managing Mesh Data

- [MDLMeshBuffer](/documentation/modelio/mdlmeshbuffer)

### Working with Data in a Buffer

- [func fill(Data, offset: Int)](/documentation/modelio/mdlmeshbuffer/fill(_:offset:))
- [func map() -> MDLMeshBufferMap](/documentation/modelio/mdlmeshbuffer/map())
- [var length: Int](/documentation/modelio/mdlmeshbuffer/length)

### Inspecting a Buffer

- [var allocator: any MDLMeshBufferAllocator](/documentation/modelio/mdlmeshbuffer/allocator)
- [var zone: any MDLMeshBufferZone](/documentation/modelio/mdlmeshbuffer/zone)
- [var type: MDLMeshBufferType](/documentation/modelio/mdlmeshbuffer/type)

### Constants

- [MDLMeshBufferType](/documentation/modelio/mdlmeshbuffertype)

#### Constants

- [case vertex](/documentation/modelio/mdlmeshbuffertype/vertex)
- [case index](/documentation/modelio/mdlmeshbuffertype/index)

#### Enumeration Cases

- [case custom](/documentation/modelio/mdlmeshbuffertype/custom)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmeshbuffertype/init(rawvalue:))
- [MDLMeshBufferAllocator](/documentation/modelio/mdlmeshbufferallocator)

### Allocating Mesh Buffers

- [func newZone(Int) -> any MDLMeshBufferZone](/documentation/modelio/mdlmeshbufferallocator/newzone(_:))
- [func newZoneForBuffers(withSize: [NSNumber], andType: [NSNumber]) -> any MDLMeshBufferZone](/documentation/modelio/mdlmeshbufferallocator/newzoneforbuffers(withsize:andtype:))
- [func newBuffer(Int, type: MDLMeshBufferType) -> any MDLMeshBuffer](/documentation/modelio/mdlmeshbufferallocator/newbuffer(_:type:))
- [func newBuffer(from: (any MDLMeshBufferZone)?, length: Int, type: MDLMeshBufferType) -> (any MDLMeshBuffer)?](/documentation/modelio/mdlmeshbufferallocator/newbuffer(from:length:type:))
- [func newBuffer(with: Data, type: MDLMeshBufferType) -> any MDLMeshBuffer](/documentation/modelio/mdlmeshbufferallocator/newbuffer(with:type:))
- [func newBuffer(from: (any MDLMeshBufferZone)?, data: Data, type: MDLMeshBufferType) -> (any MDLMeshBuffer)?](/documentation/modelio/mdlmeshbufferallocator/newbuffer(from:data:type:))
- [MDLMeshBufferData](/documentation/modelio/mdlmeshbufferdata)

### Creating a Buffer

- [init(type: MDLMeshBufferType, data: Data?)](/documentation/modelio/mdlmeshbufferdata/init(type:data:))
- [init(type: MDLMeshBufferType, length: Int)](/documentation/modelio/mdlmeshbufferdata/init(type:length:))

### Accessing a Buffer’s Data

- [var data: Data](/documentation/modelio/mdlmeshbufferdata/data)
- [MDLMeshBufferDataAllocator](/documentation/modelio/mdlmeshbufferdataallocator)
- [MDLMeshBufferMap](/documentation/modelio/mdlmeshbuffermap)

### Creating a Buffer Map

- [init(bytes: UnsafeMutableRawPointer, deallocator: (() -> Void)?)](/documentation/modelio/mdlmeshbuffermap/init(bytes:deallocator:))

### Accessing Buffer Data

- [var bytes: UnsafeMutableRawPointer](/documentation/modelio/mdlmeshbuffermap/bytes)
- [MDLMeshBufferZone](/documentation/modelio/mdlmeshbufferzone)

### Inspecting a Zone

- [var allocator: any MDLMeshBufferAllocator](/documentation/modelio/mdlmeshbufferzone/allocator)
- [var capacity: Int](/documentation/modelio/mdlmeshbufferzone/capacity)
- [MDLMeshBufferZoneDefault](/documentation/modelio/mdlmeshbufferzonedefault)

### Instance Properties

- [var allocator: any MDLMeshBufferAllocator](/documentation/modelio/mdlmeshbufferzonedefault/allocator)
- [var capacity: Int](/documentation/modelio/mdlmeshbufferzonedefault/capacity)
- [MDLVertexAttribute](/documentation/modelio/mdlvertexattribute)

### Creating a Vertex Attribute

- [init(name: String, format: MDLVertexFormat, offset: Int, bufferIndex: Int)](/documentation/modelio/mdlvertexattribute/init(name:format:offset:bufferindex:))

### Inspecting a Vertex Attribute

- [var name: String](/documentation/modelio/mdlvertexattribute/name)
- [var format: MDLVertexFormat](/documentation/modelio/mdlvertexattribute/format)
- [var offset: Int](/documentation/modelio/mdlvertexattribute/offset)
- [var bufferIndex: Int](/documentation/modelio/mdlvertexattribute/bufferindex)
- [var initializationValue: vector_float4](/documentation/modelio/mdlvertexattribute/initializationvalue)

### Constants

- [Vertex Attributes](/documentation/modelio/vertex-attributes)

#### Constants

- [let MDLVertexAttributeAnisotropy: String](/documentation/modelio/mdlvertexattributeanisotropy)
- [let MDLVertexAttributeBinormal: String](/documentation/modelio/mdlvertexattributebinormal)
- [let MDLVertexAttributeBitangent: String](/documentation/modelio/mdlvertexattributebitangent)
- [let MDLVertexAttributeColor: String](/documentation/modelio/mdlvertexattributecolor)
- [let MDLVertexAttributeEdgeCrease: String](/documentation/modelio/mdlvertexattributeedgecrease)
- [let MDLVertexAttributeJointIndices: String](/documentation/modelio/mdlvertexattributejointindices)
- [let MDLVertexAttributeJointWeights: String](/documentation/modelio/mdlvertexattributejointweights)
- [let MDLVertexAttributeNormal: String](/documentation/modelio/mdlvertexattributenormal)
- [let MDLVertexAttributeOcclusionValue: String](/documentation/modelio/mdlvertexattributeocclusionvalue)
- [let MDLVertexAttributePosition: String](/documentation/modelio/mdlvertexattributeposition)
- [let MDLVertexAttributeShadingBasisU: String](/documentation/modelio/mdlvertexattributeshadingbasisu)
- [let MDLVertexAttributeShadingBasisV: String](/documentation/modelio/mdlvertexattributeshadingbasisv)
- [let MDLVertexAttributeSubdivisionStencil: String](/documentation/modelio/mdlvertexattributesubdivisionstencil)
- [let MDLVertexAttributeTangent: String](/documentation/modelio/mdlvertexattributetangent)
- [let MDLVertexAttributeTextureCoordinate: String](/documentation/modelio/mdlvertexattributetexturecoordinate)
- [MDLVertexFormat](/documentation/modelio/mdlvertexformat)

#### Constants

- [case invalid](/documentation/modelio/mdlvertexformat/invalid)
- [case packedBit](/documentation/modelio/mdlvertexformat/packedbit)
- [case uCharBits](/documentation/modelio/mdlvertexformat/ucharbits)
- [case charBits](/documentation/modelio/mdlvertexformat/charbits)
- [case uCharNormalizedBits](/documentation/modelio/mdlvertexformat/ucharnormalizedbits)
- [case charNormalizedBits](/documentation/modelio/mdlvertexformat/charnormalizedbits)
- [case uShortBits](/documentation/modelio/mdlvertexformat/ushortbits)
- [case shortBits](/documentation/modelio/mdlvertexformat/shortbits)
- [case uShortNormalizedBits](/documentation/modelio/mdlvertexformat/ushortnormalizedbits)
- [case shortNormalizedBits](/documentation/modelio/mdlvertexformat/shortnormalizedbits)
- [case uIntBits](/documentation/modelio/mdlvertexformat/uintbits)
- [case intBits](/documentation/modelio/mdlvertexformat/intbits)
- [case halfBits](/documentation/modelio/mdlvertexformat/halfbits)
- [case floatBits](/documentation/modelio/mdlvertexformat/floatbits)
- [case uChar](/documentation/modelio/mdlvertexformat/uchar)
- [case uChar2](/documentation/modelio/mdlvertexformat/uchar2)
- [case uChar3](/documentation/modelio/mdlvertexformat/uchar3)
- [case uChar4](/documentation/modelio/mdlvertexformat/uchar4)
- [case char](/documentation/modelio/mdlvertexformat/char)
- [case char2](/documentation/modelio/mdlvertexformat/char2)
- [case char3](/documentation/modelio/mdlvertexformat/char3)
- [case char4](/documentation/modelio/mdlvertexformat/char4)
- [case uCharNormalized](/documentation/modelio/mdlvertexformat/ucharnormalized)
- [case uChar2Normalized](/documentation/modelio/mdlvertexformat/uchar2normalized)
- [case uChar3Normalized](/documentation/modelio/mdlvertexformat/uchar3normalized)
- [case uChar4Normalized](/documentation/modelio/mdlvertexformat/uchar4normalized)
- [case charNormalized](/documentation/modelio/mdlvertexformat/charnormalized)
- [case char2Normalized](/documentation/modelio/mdlvertexformat/char2normalized)
- [case char3Normalized](/documentation/modelio/mdlvertexformat/char3normalized)
- [case char4Normalized](/documentation/modelio/mdlvertexformat/char4normalized)
- [case uShort](/documentation/modelio/mdlvertexformat/ushort)
- [case uShort2](/documentation/modelio/mdlvertexformat/ushort2)
- [case uShort3](/documentation/modelio/mdlvertexformat/ushort3)
- [case uShort4](/documentation/modelio/mdlvertexformat/ushort4)
- [case short](/documentation/modelio/mdlvertexformat/short)
- [case short2](/documentation/modelio/mdlvertexformat/short2)
- [case short3](/documentation/modelio/mdlvertexformat/short3)
- [case short4](/documentation/modelio/mdlvertexformat/short4)
- [case uShortNormalized](/documentation/modelio/mdlvertexformat/ushortnormalized)
- [case uShort2Normalized](/documentation/modelio/mdlvertexformat/ushort2normalized)
- [case uShort3Normalized](/documentation/modelio/mdlvertexformat/ushort3normalized)
- [case uShort4Normalized](/documentation/modelio/mdlvertexformat/ushort4normalized)
- [case shortNormalized](/documentation/modelio/mdlvertexformat/shortnormalized)
- [case short2Normalized](/documentation/modelio/mdlvertexformat/short2normalized)
- [case short3Normalized](/documentation/modelio/mdlvertexformat/short3normalized)
- [case short4Normalized](/documentation/modelio/mdlvertexformat/short4normalized)
- [case uInt](/documentation/modelio/mdlvertexformat/uint)
- [case uInt2](/documentation/modelio/mdlvertexformat/uint2)
- [case uInt3](/documentation/modelio/mdlvertexformat/uint3)
- [case uInt4](/documentation/modelio/mdlvertexformat/uint4)
- [case int](/documentation/modelio/mdlvertexformat/int)
- [case int2](/documentation/modelio/mdlvertexformat/int2)
- [case int3](/documentation/modelio/mdlvertexformat/int3)
- [case int4](/documentation/modelio/mdlvertexformat/int4)
- [case half](/documentation/modelio/mdlvertexformat/half)
- [case half2](/documentation/modelio/mdlvertexformat/half2)
- [case half3](/documentation/modelio/mdlvertexformat/half3)
- [case half4](/documentation/modelio/mdlvertexformat/half4)
- [case float](/documentation/modelio/mdlvertexformat/float)
- [case float2](/documentation/modelio/mdlvertexformat/float2)
- [case float3](/documentation/modelio/mdlvertexformat/float3)
- [case float4](/documentation/modelio/mdlvertexformat/float4)
- [case int1010102Normalized](/documentation/modelio/mdlvertexformat/int1010102normalized)
- [case uInt1010102Normalized](/documentation/modelio/mdlvertexformat/uint1010102normalized)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlvertexformat/init(rawvalue:))

### Instance Properties

- [var time: TimeInterval](/documentation/modelio/mdlvertexattribute/time)
- [MDLVertexAttributeData](/documentation/modelio/mdlvertexattributedata)

### Accessing Data for a Vertex Attribute

- [var dataStart: UnsafeMutableRawPointer](/documentation/modelio/mdlvertexattributedata/datastart)
- [var stride: Int](/documentation/modelio/mdlvertexattributedata/stride)
- [var format: MDLVertexFormat](/documentation/modelio/mdlvertexattributedata/format)

### Instance Properties

- [var bufferSize: Int](/documentation/modelio/mdlvertexattributedata/buffersize)
- [var map: MDLMeshBufferMap](/documentation/modelio/mdlvertexattributedata/map)
- [MDLVertexBufferLayout](/documentation/modelio/mdlvertexbufferlayout)

### Working with Layout Information

- [var stride: Int](/documentation/modelio/mdlvertexbufferlayout/stride)

### Initializers

- [init(stride: Int)](/documentation/modelio/mdlvertexbufferlayout/init(stride:))
- [MDLVertexDescriptor](/documentation/modelio/mdlvertexdescriptor)

### Working with Vertex Attributes

- [var attributes: NSMutableArray](/documentation/modelio/mdlvertexdescriptor/attributes)
- [func attributeNamed(String) -> MDLVertexAttribute?](/documentation/modelio/mdlvertexdescriptor/attributenamed(_:))
- [func addOrReplaceAttribute(MDLVertexAttribute)](/documentation/modelio/mdlvertexdescriptor/addorreplaceattribute(_:))
- [func setPackedOffsets()](/documentation/modelio/mdlvertexdescriptor/setpackedoffsets())

### Working with Vertex Buffer Layouts

- [var layouts: NSMutableArray](/documentation/modelio/mdlvertexdescriptor/layouts)
- [func setPackedStrides()](/documentation/modelio/mdlvertexdescriptor/setpackedstrides())

### Resetting a Vertex Descriptor

- [func reset()](/documentation/modelio/mdlvertexdescriptor/reset())

### Copying a Vertex Descriptor

- [init(vertexDescriptor: MDLVertexDescriptor)](/documentation/modelio/mdlvertexdescriptor/init(vertexdescriptor:))

### Instance Methods

- [func removeAttributeNamed(String)](/documentation/modelio/mdlvertexdescriptor/removeattributenamed(_:))

## Materials

- [MDLMaterial](/documentation/modelio/mdlmaterial)

### Creating a material

- [init(name: String, scatteringFunction: MDLScatteringFunction)](/documentation/modelio/mdlmaterial/init(name:scatteringfunction:))

### Using a material

- [var materialFace: MDLMaterialFace](/documentation/modelio/mdlmaterial/materialface)
- [var name: String](/documentation/modelio/mdlmaterial/name)

### Determining a material’s response to lighting

- [var scatteringFunction: MDLScatteringFunction](/documentation/modelio/mdlmaterial/scatteringfunction)

### Working with individual material properties

- [func propertyNamed(String) -> MDLMaterialProperty?](/documentation/modelio/mdlmaterial/propertynamed(_:))
- [func property(with: MDLMaterialSemantic) -> MDLMaterialProperty?](/documentation/modelio/mdlmaterial/property(with:))
- [func properties(with: MDLMaterialSemantic) -> [MDLMaterialProperty]](/documentation/modelio/mdlmaterial/properties(with:))
- [func setProperty(MDLMaterialProperty)](/documentation/modelio/mdlmaterial/setproperty(_:))
- [func remove(MDLMaterialProperty)](/documentation/modelio/mdlmaterial/remove(_:))
- [func removeAllProperties()](/documentation/modelio/mdlmaterial/removeallproperties())

### Sharing material properties

- [var base: MDLMaterial?](/documentation/modelio/mdlmaterial/base)

### Accessing material properties with subscript syntax

- [subscript(String) -> MDLMaterialProperty?](/documentation/modelio/mdlmaterial/subscript(_:)-323j3)
- [subscript(Int) -> MDLMaterialProperty?](/documentation/modelio/mdlmaterial/subscript(_:)-19j2)
- [var count: Int](/documentation/modelio/mdlmaterial/count)

### Working with textures using resolvers

- [func loadTextures(using: any MDLAssetResolver)](/documentation/modelio/mdlmaterial/loadtextures(using:))
- [func resolveTextures(with: any MDLAssetResolver)](/documentation/modelio/mdlmaterial/resolvetextures(with:))
- [MDLMaterialProperty](/documentation/modelio/mdlmaterialproperty)

### Creating a Material Property

- [init(name: String, semantic: MDLMaterialSemantic)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, string: String?)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:string:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, url: URL?)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:url:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, textureSampler: MDLTextureSampler?)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:texturesampler:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, color: CGColor)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:color:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, float: Float)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:float:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, float2: vector_float2)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:float2:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, float3: vector_float3)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:float3:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, float4: vector_float4)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:float4:))
- [convenience init(name: String, semantic: MDLMaterialSemantic, matrix4x4: matrix_float4x4)](/documentation/modelio/mdlmaterialproperty/init(name:semantic:matrix4x4:))

### Using a Material Property

- [var name: String](/documentation/modelio/mdlmaterialproperty/name)
- [var semantic: MDLMaterialSemantic](/documentation/modelio/mdlmaterialproperty/semantic)
- [var type: MDLMaterialPropertyType](/documentation/modelio/mdlmaterialproperty/type)

### Working with a Material Property’s Value

- [var stringValue: String?](/documentation/modelio/mdlmaterialproperty/stringvalue)
- [var urlValue: URL?](/documentation/modelio/mdlmaterialproperty/urlvalue)
- [var textureSamplerValue: MDLTextureSampler?](/documentation/modelio/mdlmaterialproperty/texturesamplervalue)
- [var color: CGColor?](/documentation/modelio/mdlmaterialproperty/color)
- [var floatValue: Float](/documentation/modelio/mdlmaterialproperty/floatvalue)
- [var float2Value: vector_float2](/documentation/modelio/mdlmaterialproperty/float2value)
- [var float3Value: vector_float3](/documentation/modelio/mdlmaterialproperty/float3value)
- [var float4Value: vector_float4](/documentation/modelio/mdlmaterialproperty/float4value)
- [var matrix4x4: matrix_float4x4](/documentation/modelio/mdlmaterialproperty/matrix4x4)

### Copying a Material Property

- [func setProperties(MDLMaterialProperty)](/documentation/modelio/mdlmaterialproperty/setproperties(_:))

### Constants

- [MDLMaterialSemantic](/documentation/modelio/mdlmaterialsemantic)

#### Constants

- [case baseColor](/documentation/modelio/mdlmaterialsemantic/basecolor)
- [case subsurface](/documentation/modelio/mdlmaterialsemantic/subsurface)
- [case metallic](/documentation/modelio/mdlmaterialsemantic/metallic)
- [case specular](/documentation/modelio/mdlmaterialsemantic/specular)
- [case specularExponent](/documentation/modelio/mdlmaterialsemantic/specularexponent)
- [case specularTint](/documentation/modelio/mdlmaterialsemantic/speculartint)
- [case roughness](/documentation/modelio/mdlmaterialsemantic/roughness)
- [case anisotropic](/documentation/modelio/mdlmaterialsemantic/anisotropic)
- [case anisotropicRotation](/documentation/modelio/mdlmaterialsemantic/anisotropicrotation)
- [case sheen](/documentation/modelio/mdlmaterialsemantic/sheen)
- [case sheenTint](/documentation/modelio/mdlmaterialsemantic/sheentint)
- [case clearcoat](/documentation/modelio/mdlmaterialsemantic/clearcoat)
- [case clearcoatGloss](/documentation/modelio/mdlmaterialsemantic/clearcoatgloss)
- [case emission](/documentation/modelio/mdlmaterialsemantic/emission)
- [case bump](/documentation/modelio/mdlmaterialsemantic/bump)
- [case opacity](/documentation/modelio/mdlmaterialsemantic/opacity)
- [case interfaceIndexOfRefraction](/documentation/modelio/mdlmaterialsemantic/interfaceindexofrefraction)
- [case materialIndexOfRefraction](/documentation/modelio/mdlmaterialsemantic/materialindexofrefraction)
- [case objectSpaceNormal](/documentation/modelio/mdlmaterialsemantic/objectspacenormal)
- [case tangentSpaceNormal](/documentation/modelio/mdlmaterialsemantic/tangentspacenormal)
- [case displacement](/documentation/modelio/mdlmaterialsemantic/displacement)
- [case displacementScale](/documentation/modelio/mdlmaterialsemantic/displacementscale)
- [case ambientOcclusion](/documentation/modelio/mdlmaterialsemantic/ambientocclusion)
- [case ambientOcclusionScale](/documentation/modelio/mdlmaterialsemantic/ambientocclusionscale)
- [case none](/documentation/modelio/mdlmaterialsemantic/none)
- [case userDefined](/documentation/modelio/mdlmaterialsemantic/userdefined)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialsemantic/init(rawvalue:))
- [MDLMaterialPropertyType](/documentation/modelio/mdlmaterialpropertytype)

#### Constants

- [case none](/documentation/modelio/mdlmaterialpropertytype/none)
- [case string](/documentation/modelio/mdlmaterialpropertytype/string)
- [case URL](/documentation/modelio/mdlmaterialpropertytype/url)
- [case texture](/documentation/modelio/mdlmaterialpropertytype/texture)
- [case color](/documentation/modelio/mdlmaterialpropertytype/color)
- [case float](/documentation/modelio/mdlmaterialpropertytype/float)
- [case float2](/documentation/modelio/mdlmaterialpropertytype/float2)
- [case float3](/documentation/modelio/mdlmaterialpropertytype/float3)
- [case float4](/documentation/modelio/mdlmaterialpropertytype/float4)
- [case matrix44](/documentation/modelio/mdlmaterialpropertytype/matrix44)

#### Enumeration Cases

- [case buffer](/documentation/modelio/mdlmaterialpropertytype/buffer)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialpropertytype/init(rawvalue:))

### Instance Properties

- [var luminance: Float](/documentation/modelio/mdlmaterialproperty/luminance)
- [MDLMaterialPropertyConnection](/documentation/modelio/mdlmaterialpropertyconnection)

### Initializers

- [init(output: MDLMaterialProperty, input: MDLMaterialProperty)](/documentation/modelio/mdlmaterialpropertyconnection/init(output:input:))

### Instance Properties

- [var input: MDLMaterialProperty?](/documentation/modelio/mdlmaterialpropertyconnection/input)
- [var output: MDLMaterialProperty?](/documentation/modelio/mdlmaterialpropertyconnection/output)
- [MDLMaterialPropertyGraph](/documentation/modelio/mdlmaterialpropertygraph)

### Initializers

- [init(nodes: [MDLMaterialPropertyNode], connections: [MDLMaterialPropertyConnection])](/documentation/modelio/mdlmaterialpropertygraph/init(nodes:connections:))

### Instance Properties

- [var connections: [MDLMaterialPropertyConnection]](/documentation/modelio/mdlmaterialpropertygraph/connections)
- [var nodes: [MDLMaterialPropertyNode]](/documentation/modelio/mdlmaterialpropertygraph/nodes)

### Instance Methods

- [func evaluate()](/documentation/modelio/mdlmaterialpropertygraph/evaluate())
- [MDLMaterialPropertyNode](/documentation/modelio/mdlmaterialpropertynode)

### Initializers

- [init(inputs: [MDLMaterialProperty], outputs: [MDLMaterialProperty], evaluationFunction: (MDLMaterialPropertyNode) -> Void)](/documentation/modelio/mdlmaterialpropertynode/init(inputs:outputs:evaluationfunction:))

### Instance Properties

- [var evaluationFunction: (MDLMaterialPropertyNode) -> Void](/documentation/modelio/mdlmaterialpropertynode/evaluationfunction)
- [var inputs: [MDLMaterialProperty]](/documentation/modelio/mdlmaterialpropertynode/inputs)
- [var outputs: [MDLMaterialProperty]](/documentation/modelio/mdlmaterialpropertynode/outputs)
- [MDLScatteringFunction](/documentation/modelio/mdlscatteringfunction)

### Naming a Scattering Function

- [var name: String](/documentation/modelio/mdlscatteringfunction/name)

### Working with Shading Properties

- [var baseColor: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/basecolor)
- [var emission: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/emission)
- [var specular: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/specular)
- [var materialIndexOfRefraction: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/materialindexofrefraction)
- [var interfaceIndexOfRefraction: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/interfaceindexofrefraction)
- [var normal: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/normal)
- [var ambientOcclusion: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/ambientocclusion)
- [var ambientOcclusionScale: MDLMaterialProperty](/documentation/modelio/mdlscatteringfunction/ambientocclusionscale)
- [MDLPhysicallyPlausibleScatteringFunction](/documentation/modelio/mdlphysicallyplausiblescatteringfunction)

### Working with Shading Properties

- [var subsurface: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/subsurface)
- [var metallic: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/metallic)
- [var specularAmount: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/specularamount)
- [var specularTint: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/speculartint)
- [var roughness: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/roughness)
- [var anisotropic: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/anisotropic)
- [var anisotropicRotation: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/anisotropicrotation)
- [var sheen: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/sheen)
- [var sheenTint: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/sheentint)
- [var clearcoat: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/clearcoat)
- [var clearcoatGloss: MDLMaterialProperty](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/clearcoatgloss)

### Instance Properties

- [var version: Int](/documentation/modelio/mdlphysicallyplausiblescatteringfunction/version)

## Textures

- [MDLTexture](/documentation/modelio/mdltexture)

### Loading Textures from a Bundle

- [convenience init?(named: String)](/documentation/modelio/mdltexture/init(named:))
- [convenience init?(named: String, bundle: Bundle?)](/documentation/modelio/mdltexture/init(named:bundle:))
- [convenience init?(cubeWithImagesNamed: [String])](/documentation/modelio/mdltexture/init(cubewithimagesnamed:))
- [convenience init?(cubeWithImagesNamed: [String], bundle: Bundle?)](/documentation/modelio/mdltexture/init(cubewithimagesnamed:bundle:))

### Creating Textures

- [init(data: Data?, topLeftOrigin: Bool, name: String?, dimensions: vector_int2, rowStride: Int, channelCount: Int, channelEncoding: MDLTextureChannelEncoding, isCube: Bool)](/documentation/modelio/mdltexture/init(data:topleftorigin:name:dimensions:rowstride:channelcount:channelencoding:iscube:))

### Exporting Textures

- [func write(to: URL) -> Bool](/documentation/modelio/mdltexture/write(to:))
- [func write(to: URL, type: CFString) -> Bool](/documentation/modelio/mdltexture/write(to:type:))
- [func imageFromTexture() -> Unmanaged<CGImage>?](/documentation/modelio/mdltexture/imagefromtexture())

### Accessing Texture Data

- [func texelDataWithTopLeftOrigin() -> Data?](/documentation/modelio/mdltexture/texeldatawithtopleftorigin())
- [func texelDataWithBottomLeftOrigin() -> Data?](/documentation/modelio/mdltexture/texeldatawithbottomleftorigin())
- [func texelDataWithTopLeftOrigin(atMipLevel: Int, create: Bool) -> Data?](/documentation/modelio/mdltexture/texeldatawithtopleftorigin(atmiplevel:create:))
- [func texelDataWithBottomLeftOrigin(atMipLevel: Int, create: Bool) -> Data?](/documentation/modelio/mdltexture/texeldatawithbottomleftorigin(atmiplevel:create:))

### Examining Texture Attributes

- [var dimensions: vector_int2](/documentation/modelio/mdltexture/dimensions)
- [var rowStride: Int](/documentation/modelio/mdltexture/rowstride)
- [var channelCount: Int](/documentation/modelio/mdltexture/channelcount)
- [var channelEncoding: MDLTextureChannelEncoding](/documentation/modelio/mdltexture/channelencoding)
- [var isCube: Bool](/documentation/modelio/mdltexture/iscube)
- [var mipLevelCount: Int](/documentation/modelio/mdltexture/miplevelcount)

### Creating Irradiance Textures

- [class func irradianceTextureCube(with: MDLTexture, name: String?, dimensions: vector_int2) -> Self](/documentation/modelio/mdltexture/irradiancetexturecube(with:name:dimensions:))
- [class func irradianceTextureCube(with: MDLTexture, name: String?, dimensions: vector_int2, roughness: Float) -> Self](/documentation/modelio/mdltexture/irradiancetexturecube(with:name:dimensions:roughness:))

### Constants

- [MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding)

#### Constants

- [case uInt8](/documentation/modelio/mdltexturechannelencoding/uint8-swift.enum.case)
- [case uInt16](/documentation/modelio/mdltexturechannelencoding/uint16-swift.enum.case)
- [case uInt24](/documentation/modelio/mdltexturechannelencoding/uint24-swift.enum.case)
- [case uInt32](/documentation/modelio/mdltexturechannelencoding/uint32-swift.enum.case)
- [case float16](/documentation/modelio/mdltexturechannelencoding/float16)
- [case float32](/documentation/modelio/mdltexturechannelencoding/float32)

#### Enumeration Cases

- [case float16SR](/documentation/modelio/mdltexturechannelencoding/float16sr)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdltexturechannelencoding/init(rawvalue:))

#### Type Properties

- [static var uint16: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint16-swift.type.property)
- [static var uint24: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint24-swift.type.property)
- [static var uint32: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint32-swift.type.property)
- [static var uint8: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint8-swift.type.property)

### Initializers

- [init()](/documentation/modelio/mdltexture/init())
- [convenience init?(named: String, assetResolver: any MDLAssetResolver)](/documentation/modelio/mdltexture/init(named:assetresolver:))

### Instance Properties

- [var hasAlphaValues: Bool](/documentation/modelio/mdltexture/hasalphavalues)

### Instance Methods

- [func imageFromTexture(atLevel: Int) -> Unmanaged<CGImage>?](/documentation/modelio/mdltexture/imagefromtexture(atlevel:))
- [func write(to: URL, level: Int) -> Bool](/documentation/modelio/mdltexture/write(to:level:))
- [func write(to: URL, type: CFString, level: Int) -> Bool](/documentation/modelio/mdltexture/write(to:type:level:))
- [MDLCheckerboardTexture](/documentation/modelio/mdlcheckerboardtexture)

### Creating a Checkerboard Texture

- [init(divisions: Float, name: String?, dimensions: vector_int2, channelCount: Int32, channelEncoding: MDLTextureChannelEncoding, color1: CGColor, color2: CGColor)](/documentation/modelio/mdlcheckerboardtexture/init(divisions:name:dimensions:channelcount:channelencoding:color1:color2:))

### Configuring the Checkerboard Pattern

- [var color1: CGColor?](/documentation/modelio/mdlcheckerboardtexture/color1)
- [var color2: CGColor?](/documentation/modelio/mdlcheckerboardtexture/color2)
- [var divisions: Float](/documentation/modelio/mdlcheckerboardtexture/divisions)
- [MDLColorSwatchTexture](/documentation/modelio/mdlcolorswatchtexture)

### Creating a Color Swatch Texture

- [init(colorGradientFrom: CGColor, to: CGColor, name: String?, textureDimensions: vector_int2)](/documentation/modelio/mdlcolorswatchtexture/init(colorgradientfrom:to:name:texturedimensions:))
- [init(colorTemperatureGradientFrom: Float, toColorTemperature: Float, name: String?, textureDimensions: vector_int2)](/documentation/modelio/mdlcolorswatchtexture/init(colortemperaturegradientfrom:tocolortemperature:name:texturedimensions:))
- [MDLNoiseTexture](/documentation/modelio/mdlnoisetexture)

### Creating a Noise Texture

- [init(scalarNoiseWithSmoothness: Float, name: String?, textureDimensions: vector_int2, channelCount: Int32, channelEncoding: MDLTextureChannelEncoding, grayscale: Bool)](/documentation/modelio/mdlnoisetexture/init(scalarnoisewithsmoothness:name:texturedimensions:channelcount:channelencoding:grayscale:))
- [init(vectorNoiseWithSmoothness: Float, name: String?, textureDimensions: vector_int2, channelEncoding: MDLTextureChannelEncoding)](/documentation/modelio/mdlnoisetexture/init(vectornoisewithsmoothness:name:texturedimensions:channelencoding:))

### Initializers

- [init(cellularNoiseWithFrequency: Float, name: String?, textureDimensions: vector_int2, channelEncoding: MDLTextureChannelEncoding)](/documentation/modelio/mdlnoisetexture/init(cellularnoisewithfrequency:name:texturedimensions:channelencoding:))
- [MDLNormalMapTexture](/documentation/modelio/mdlnormalmaptexture)

### Creating a Normal Map Texture

- [init(byGeneratingNormalMapWith: MDLTexture, name: String?, smoothness: Float, contrast: Float)](/documentation/modelio/mdlnormalmaptexture/init(bygeneratingnormalmapwith:name:smoothness:contrast:))
- [MDLSkyCubeTexture](/documentation/modelio/mdlskycubetexture)

### Creating a Sky Cube Texture

- [init(name: String?, channelEncoding: MDLTextureChannelEncoding, textureDimensions: vector_int2, turbidity: Float, sunElevation: Float, upperAtmosphereScattering: Float, groundAlbedo: Float)](/documentation/modelio/mdlskycubetexture/init(name:channelencoding:texturedimensions:turbidity:sunelevation:upperatmospherescattering:groundalbedo:))

### Working with Sky Simulation Parameters

- [var turbidity: Float](/documentation/modelio/mdlskycubetexture/turbidity)
- [var sunElevation: Float](/documentation/modelio/mdlskycubetexture/sunelevation)
- [var upperAtmosphereScattering: Float](/documentation/modelio/mdlskycubetexture/upperatmospherescattering)
- [var groundAlbedo: Float](/documentation/modelio/mdlskycubetexture/groundalbedo)
- [var groundColor: CGColor?](/documentation/modelio/mdlskycubetexture/groundcolor)
- [var horizonElevation: Float](/documentation/modelio/mdlskycubetexture/horizonelevation)

### Working with Tone Mapping Parameters

- [var gamma: Float](/documentation/modelio/mdlskycubetexture/gamma)
- [var exposure: Float](/documentation/modelio/mdlskycubetexture/exposure)
- [var brightness: Float](/documentation/modelio/mdlskycubetexture/brightness)
- [var contrast: Float](/documentation/modelio/mdlskycubetexture/contrast)
- [var saturation: Float](/documentation/modelio/mdlskycubetexture/saturation)
- [var highDynamicRangeCompression: vector_float2](/documentation/modelio/mdlskycubetexture/highdynamicrangecompression)

### Updating Texture Data

- [func update()](/documentation/modelio/mdlskycubetexture/update())

### Initializers

- [init(name: String?, channelEncoding: MDLTextureChannelEncoding, textureDimensions: vector_int2, turbidity: Float, sunElevation: Float, sunAzimuth: Float, upperAtmosphereScattering: Float, groundAlbedo: Float)](/documentation/modelio/mdlskycubetexture/init(name:channelencoding:texturedimensions:turbidity:sunelevation:sunazimuth:upperatmospherescattering:groundalbedo:))

### Instance Properties

- [var sunAzimuth: Float](/documentation/modelio/mdlskycubetexture/sunazimuth)
- [MDLURLTexture](/documentation/modelio/mdlurltexture)

### Creating a URL Texture

- [init(url: URL, name: String?)](/documentation/modelio/mdlurltexture/init(url:name:))

### Inspecting the Texture URL

- [var url: URL](/documentation/modelio/mdlurltexture/url)
- [MDLTextureFilter](/documentation/modelio/mdltexturefilter)

### Managing Texture Coordinate Wrap Modes

- [var sWrapMode: MDLMaterialTextureWrapMode](/documentation/modelio/mdltexturefilter/swrapmode)
- [var tWrapMode: MDLMaterialTextureWrapMode](/documentation/modelio/mdltexturefilter/twrapmode)
- [var rWrapMode: MDLMaterialTextureWrapMode](/documentation/modelio/mdltexturefilter/rwrapmode)

### Managing Texture Filter Modes

- [var minFilter: MDLMaterialTextureFilterMode](/documentation/modelio/mdltexturefilter/minfilter)
- [var magFilter: MDLMaterialTextureFilterMode](/documentation/modelio/mdltexturefilter/magfilter)
- [var mipFilter: MDLMaterialMipMapFilterMode](/documentation/modelio/mdltexturefilter/mipfilter)

### Constants

- [MDLMaterialTextureWrapMode](/documentation/modelio/mdlmaterialtexturewrapmode)

#### Constants

- [case clamp](/documentation/modelio/mdlmaterialtexturewrapmode/clamp)
- [case `repeat`](/documentation/modelio/mdlmaterialtexturewrapmode/repeat)
- [case mirror](/documentation/modelio/mdlmaterialtexturewrapmode/mirror)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialtexturewrapmode/init(rawvalue:))
- [MDLMaterialTextureFilterMode](/documentation/modelio/mdlmaterialtexturefiltermode)

#### Constants

- [case nearest](/documentation/modelio/mdlmaterialtexturefiltermode/nearest)
- [case linear](/documentation/modelio/mdlmaterialtexturefiltermode/linear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialtexturefiltermode/init(rawvalue:))
- [MDLMaterialMipMapFilterMode](/documentation/modelio/mdlmaterialmipmapfiltermode)

#### Constants

- [case nearest](/documentation/modelio/mdlmaterialmipmapfiltermode/nearest)
- [case linear](/documentation/modelio/mdlmaterialmipmapfiltermode/linear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialmipmapfiltermode/init(rawvalue:))
- [MDLTextureSampler](/documentation/modelio/mdltexturesampler)

### Working with Texture Parameters

- [var texture: MDLTexture?](/documentation/modelio/mdltexturesampler/texture)
- [var hardwareFilter: MDLTextureFilter?](/documentation/modelio/mdltexturesampler/hardwarefilter)
- [var transform: MDLTransform?](/documentation/modelio/mdltexturesampler/transform)

## Lights

- [MDLLight](/documentation/modelio/mdllight)

### Working with Lights

- [func irradiance(atPoint: vector_float3) -> Unmanaged<CGColor>](/documentation/modelio/mdllight/irradiance(atpoint:))
- [func irradiance(atPoint: vector_float3, colorSpace: CGColorSpace) -> Unmanaged<CGColor>](/documentation/modelio/mdllight/irradiance(atpoint:colorspace:))
- [var lightType: MDLLightType](/documentation/modelio/mdllight/lighttype)
- [var colorSpace: String](/documentation/modelio/mdllight/colorspace)

### Constants

- [MDLLightType](/documentation/modelio/mdllighttype)

#### Constants

- [case unknown](/documentation/modelio/mdllighttype/unknown)
- [case ambient](/documentation/modelio/mdllighttype/ambient)
- [case directional](/documentation/modelio/mdllighttype/directional)
- [case spot](/documentation/modelio/mdllighttype/spot)
- [case point](/documentation/modelio/mdllighttype/point)
- [case linear](/documentation/modelio/mdllighttype/linear)
- [case discArea](/documentation/modelio/mdllighttype/discarea)
- [case rectangularArea](/documentation/modelio/mdllighttype/rectangulararea)
- [case superElliptical](/documentation/modelio/mdllighttype/superelliptical)
- [case photometric](/documentation/modelio/mdllighttype/photometric)
- [case probe](/documentation/modelio/mdllighttype/probe)
- [case environment](/documentation/modelio/mdllighttype/environment)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdllighttype/init(rawvalue:))
- [MDLAreaLight](/documentation/modelio/mdlarealight)

### Managing a Light’s Shape

- [var areaRadius: Float](/documentation/modelio/mdlarealight/arearadius)
- [var aspect: Float](/documentation/modelio/mdlarealight/aspect)
- [var superEllipticPower: vector_float2](/documentation/modelio/mdlarealight/superellipticpower)
- [MDLLightProbe](/documentation/modelio/mdllightprobe)

### Creating a Light Probe

- [init(reflectiveTexture: MDLTexture?, irradianceTexture: MDLTexture?)](/documentation/modelio/mdllightprobe/init(reflectivetexture:irradiancetexture:))

### Working with Textures

- [var reflectiveTexture: MDLTexture?](/documentation/modelio/mdllightprobe/reflectivetexture)
- [var irradianceTexture: MDLTexture?](/documentation/modelio/mdllightprobe/irradiancetexture)

### Working with Spherical Harmonics

- [func generateSphericalHarmonics(fromIrradiance: Int)](/documentation/modelio/mdllightprobe/generatesphericalharmonics(fromirradiance:))
- [var sphericalHarmonicsCoefficients: Data?](/documentation/modelio/mdllightprobe/sphericalharmonicscoefficients)
- [var sphericalHarmonicsLevel: Int](/documentation/modelio/mdllightprobe/sphericalharmonicslevel)

### Generating Light Probes from Scene Contents

- [init?(textureSize: Int, forLocation: MDLTransform, lightsToConsider: [MDLLight], objectsToConsider: [MDLObject], reflectiveCubemap: MDLTexture?, irradianceCubemap: MDLTexture?)](/documentation/modelio/mdllightprobe/init(texturesize:forlocation:lightstoconsider:objectstoconsider:reflectivecubemap:irradiancecubemap:))
- [MDLLightProbeIrradianceDataSource](/documentation/modelio/mdllightprobeirradiancedatasource)

### Providing Light Probe Information

- [var boundingBox: MDLAxisAlignedBoundingBox](/documentation/modelio/mdllightprobeirradiancedatasource/boundingbox)
- [var sphericalHarmonicsLevel: Int](/documentation/modelio/mdllightprobeirradiancedatasource/sphericalharmonicslevel)
- [func sphericalHarmonicsCoefficients(atPosition: vector_float3) -> Data](/documentation/modelio/mdllightprobeirradiancedatasource/sphericalharmonicscoefficients(atposition:))
- [MDLPhotometricLight](/documentation/modelio/mdlphotometriclight)

### Creating a Photometric Light

- [init?(iesProfile: URL)](/documentation/modelio/mdlphotometriclight/init(iesprofile:))

### Interpreting the Light Web as a Cube Texture

- [func generateCubemap(fromLight: Int)](/documentation/modelio/mdlphotometriclight/generatecubemap(fromlight:))
- [var lightCubeMap: MDLTexture?](/documentation/modelio/mdlphotometriclight/lightcubemap)

### Interpreting the Light Web as Spherical Harmonics

- [func generateSphericalHarmonics(fromLight: Int)](/documentation/modelio/mdlphotometriclight/generatesphericalharmonics(fromlight:))
- [var sphericalHarmonicsCoefficients: Data?](/documentation/modelio/mdlphotometriclight/sphericalharmonicscoefficients)
- [var sphericalHarmonicsLevel: Int](/documentation/modelio/mdlphotometriclight/sphericalharmonicslevel)

### Instance Methods

- [func generateTexture(Int) -> MDLTexture](/documentation/modelio/mdlphotometriclight/generatetexture(_:))
- [MDLPhysicallyPlausibleLight](/documentation/modelio/mdlphysicallyplausiblelight)

### Managing Light Color and Intensity

- [var color: CGColor?](/documentation/modelio/mdlphysicallyplausiblelight/color)
- [var lumens: Float](/documentation/modelio/mdlphysicallyplausiblelight/lumens)
- [func setColorByTemperature(Float)](/documentation/modelio/mdlphysicallyplausiblelight/setcolorbytemperature(_:))

### Managing Light Geometry

- [var innerConeAngle: Float](/documentation/modelio/mdlphysicallyplausiblelight/innerconeangle)
- [var outerConeAngle: Float](/documentation/modelio/mdlphysicallyplausiblelight/outerconeangle)

### Managing Attenuation

- [var attenuationStartDistance: Float](/documentation/modelio/mdlphysicallyplausiblelight/attenuationstartdistance)
- [var attenuationEndDistance: Float](/documentation/modelio/mdlphysicallyplausiblelight/attenuationenddistance)

## Cameras

- [MDLCamera](/documentation/modelio/mdlcamera)

### Managing Camera Position and Orientation

- [func frameBoundingBox(MDLAxisAlignedBoundingBox, setNearAndFar: Bool)](/documentation/modelio/mdlcamera/frameboundingbox(_:setnearandfar:))
- [func look(at: vector_float3)](/documentation/modelio/mdlcamera/look(at:))
- [func look(at: vector_float3, from: vector_float3)](/documentation/modelio/mdlcamera/look(at:from:))

### Managing Camera Perspective

- [var projectionMatrix: matrix_float4x4](/documentation/modelio/mdlcamera/projectionmatrix)
- [var projection: MDLCameraProjection](/documentation/modelio/mdlcamera/projection)
- [MDLCameraProjection](/documentation/modelio/mdlcameraprojection)

#### Constants

- [case orthographic](/documentation/modelio/mdlcameraprojection/orthographic)
- [case perspective](/documentation/modelio/mdlcameraprojection/perspective)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlcameraprojection/init(rawvalue:))
- [var nearVisibilityDistance: Float](/documentation/modelio/mdlcamera/nearvisibilitydistance)
- [var farVisibilityDistance: Float](/documentation/modelio/mdlcamera/farvisibilitydistance)
- [var fieldOfView: Float](/documentation/modelio/mdlcamera/fieldofview)
- [func ray(to: vector_int2, forViewPort: vector_int2) -> vector_float3](/documentation/modelio/mdlcamera/ray(to:forviewport:))
- [var worldToMetersConversionScale: Float](/documentation/modelio/mdlcamera/worldtometersconversionscale)

### Modeling a Physical Lens

- [var barrelDistortion: Float](/documentation/modelio/mdlcamera/barreldistortion)
- [var fisheyeDistortion: Float](/documentation/modelio/mdlcamera/fisheyedistortion)
- [var opticalVignetting: Float](/documentation/modelio/mdlcamera/opticalvignetting)
- [var chromaticAberration: Float](/documentation/modelio/mdlcamera/chromaticaberration)
- [var focalLength: Float](/documentation/modelio/mdlcamera/focallength)
- [var fStop: Float](/documentation/modelio/mdlcamera/fstop)
- [var apertureBladeCount: Int](/documentation/modelio/mdlcamera/aperturebladecount)
- [func bokehKernel(withSize: vector_int2) -> MDLTexture](/documentation/modelio/mdlcamera/bokehkernel(withsize:))
- [var maximumCircleOfConfusion: Float](/documentation/modelio/mdlcamera/maximumcircleofconfusion)
- [var focusDistance: Float](/documentation/modelio/mdlcamera/focusdistance)
- [var shutterOpenInterval: TimeInterval](/documentation/modelio/mdlcamera/shutteropeninterval)

### Modeling a Physical Imaging Surface

- [var sensorVerticalAperture: Float](/documentation/modelio/mdlcamera/sensorverticalaperture)
- [var sensorAspect: Float](/documentation/modelio/mdlcamera/sensoraspect)
- [var sensorEnlargement: vector_float2](/documentation/modelio/mdlcamera/sensorenlargement)
- [var sensorShift: vector_float2](/documentation/modelio/mdlcamera/sensorshift)
- [var flash: vector_float3](/documentation/modelio/mdlcamera/flash)
- [var exposure: vector_float3](/documentation/modelio/mdlcamera/exposure)
- [var exposureCompression: vector_float2](/documentation/modelio/mdlcamera/exposurecompression)
- [MDLStereoscopicCamera](/documentation/modelio/mdlstereoscopiccamera)

### Modeling Stereoscopic Imaging

- [var interPupillaryDistance: Float](/documentation/modelio/mdlstereoscopiccamera/interpupillarydistance)
- [var overlap: Float](/documentation/modelio/mdlstereoscopiccamera/overlap)
- [var leftVergence: Float](/documentation/modelio/mdlstereoscopiccamera/leftvergence)
- [var rightVergence: Float](/documentation/modelio/mdlstereoscopiccamera/rightvergence)

### Generating View and Projection Matrices

- [var leftViewMatrix: matrix_float4x4](/documentation/modelio/mdlstereoscopiccamera/leftviewmatrix)
- [var leftProjectionMatrix: matrix_float4x4](/documentation/modelio/mdlstereoscopiccamera/leftprojectionmatrix)
- [var rightViewMatrix: matrix_float4x4](/documentation/modelio/mdlstereoscopiccamera/rightviewmatrix)
- [var rightProjectionMatrix: matrix_float4x4](/documentation/modelio/mdlstereoscopiccamera/rightprojectionmatrix)

## Extensible Asset Format Support

- [MDLComponent](/documentation/modelio/mdlcomponent)
- [MDLObjectContainer](/documentation/modelio/mdlobjectcontainer)
- [MDLObjectContainerComponent](/documentation/modelio/mdlobjectcontainercomponent)

### Working with Child Objects

- [var objects: [MDLObject]](/documentation/modelio/mdlobjectcontainercomponent/objects)
- [func add(MDLObject)](/documentation/modelio/mdlobjectcontainercomponent/add(_:))
- [func remove(MDLObject)](/documentation/modelio/mdlobjectcontainercomponent/remove(_:))

### Instance Properties

- [var count: Int](/documentation/modelio/mdlobjectcontainercomponent/count)

### Subscripts

- [subscript(Int) -> MDLObject](/documentation/modelio/mdlobjectcontainercomponent/subscript(_:))
- [MDLTransformComponent](/documentation/modelio/mdltransformcomponent)

### Working with Static Transforms

- [var matrix: matrix_float4x4](/documentation/modelio/mdltransformcomponent/matrix)
- [func setLocalTransform(matrix_float4x4)](/documentation/modelio/mdltransformcomponent/setlocaltransform(_:))

### Working with Animated Transforms

- [var minimumTime: TimeInterval](/documentation/modelio/mdltransformcomponent/minimumtime)
- [var maximumTime: TimeInterval](/documentation/modelio/mdltransformcomponent/maximumtime)
- [func localTransform(atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdltransformcomponent/localtransform(attime:))
- [func setLocalTransform(matrix_float4x4, forTime: TimeInterval)](/documentation/modelio/mdltransformcomponent/setlocaltransform(_:fortime:))

### Deriving a Global Transformation

- [static func globalTransform(with: MDLObject, atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdltransformcomponent/globaltransform(with:attime:))

### Instance Properties

- [var keyTimes: [NSNumber]](/documentation/modelio/mdltransformcomponent/keytimes)
- [var resetsTransform: Bool](/documentation/modelio/mdltransformcomponent/resetstransform)

## Volumetric Representations

- [MDLVoxelArray](/documentation/modelio/mdlvoxelarray)

### Creating a Voxel Array

- [init(asset: MDLAsset, divisions: Int32, interiorShells: Int32, exteriorShells: Int32, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/init(asset:divisions:interiorshells:exteriorshells:patchradius:))
- [init(asset: MDLAsset, divisions: Int32, interiorNBWidth: Float, exteriorNBWidth: Float, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/init(asset:divisions:interiornbwidth:exteriornbwidth:patchradius:))
- [init(data: Data, boundingBox: MDLAxisAlignedBoundingBox, voxelExtent: Float)](/documentation/modelio/mdlvoxelarray/init(data:boundingbox:voxelextent:))

### Examining Voxels

- [var count: Int](/documentation/modelio/mdlvoxelarray/count)
- [var voxelIndexExtent: MDLVoxelIndexExtent](/documentation/modelio/mdlvoxelarray/voxelindexextent)
- [func voxelExists(atIndex: MDLVoxelIndex, allowAnyX: Bool, allowAnyY: Bool, allowAnyZ: Bool, allowAnyShell: Bool) -> Bool](/documentation/modelio/mdlvoxelarray/voxelexists(atindex:allowanyx:allowanyy:allowanyz:allowanyshell:))
- [func voxels(within: MDLVoxelIndexExtent) -> Data?](/documentation/modelio/mdlvoxelarray/voxels(within:))
- [func voxelIndices() -> Data?](/documentation/modelio/mdlvoxelarray/voxelindices())

### Modifying Voxels

- [func setVoxelAtIndex(MDLVoxelIndex)](/documentation/modelio/mdlvoxelarray/setvoxelatindex(_:))
- [func setVoxelsFor(MDLMesh, divisions: Int32, interiorNBWidth: Float, exteriorNBWidth: Float, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/setvoxelsfor(_:divisions:interiornbwidth:exteriornbwidth:patchradius:))
- [func setVoxelsFor(MDLMesh, divisions: Int32, interiorShells: Int32, exteriorShells: Int32, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/setvoxelsfor(_:divisions:interiorshells:exteriorshells:patchradius:))

### Performing Constructive Solid Geometry Operations

- [func union(with: MDLVoxelArray)](/documentation/modelio/mdlvoxelarray/union(with:))
- [func intersect(with: MDLVoxelArray)](/documentation/modelio/mdlvoxelarray/intersect(with:))
- [func difference(with: MDLVoxelArray)](/documentation/modelio/mdlvoxelarray/difference(with:))

### Relating Voxels to Scene Space

- [var boundingBox: MDLAxisAlignedBoundingBox](/documentation/modelio/mdlvoxelarray/boundingbox)
- [func index(ofSpatialLocation: vector_float3) -> MDLVoxelIndex](/documentation/modelio/mdlvoxelarray/index(ofspatiallocation:))
- [func spatialLocation(ofIndex: MDLVoxelIndex) -> vector_float3](/documentation/modelio/mdlvoxelarray/spatiallocation(ofindex:))
- [func voxelBoundingBox(atIndex: MDLVoxelIndex) -> MDLAxisAlignedBoundingBox](/documentation/modelio/mdlvoxelarray/voxelboundingbox(atindex:))

### Creating a Mesh from Voxels

- [func mesh(using: (any MDLMeshBufferAllocator)?) -> MDLMesh?](/documentation/modelio/mdlvoxelarray/mesh(using:))

### Constants

- [MDLVoxelIndex](/documentation/modelio/mdlvoxelindex)
- [MDLVoxelIndexExtent](/documentation/modelio/mdlvoxelindexextent)

#### Initializers

- [init()](/documentation/modelio/mdlvoxelindexextent/init())
- [init(minimumExtent: MDLVoxelIndex, maximumExtent: MDLVoxelIndex)](/documentation/modelio/mdlvoxelindexextent/init(minimumextent:maximumextent:))

#### Instance Properties

- [var maximumExtent: MDLVoxelIndex](/documentation/modelio/mdlvoxelindexextent/maximumextent)
- [var minimumExtent: MDLVoxelIndex](/documentation/modelio/mdlvoxelindexextent/minimumextent)

### Initializers

- [init(asset: MDLAsset, divisions: Int32, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/init(asset:divisions:patchradius:))

### Instance Properties

- [var isValidSignedShellField: Bool](/documentation/modelio/mdlvoxelarray/isvalidsignedshellfield)
- [var shellFieldExteriorThickness: Float](/documentation/modelio/mdlvoxelarray/shellfieldexteriorthickness)
- [var shellFieldInteriorThickness: Float](/documentation/modelio/mdlvoxelarray/shellfieldinteriorthickness)

### Instance Methods

- [func coarseMesh() -> MDLMesh?](/documentation/modelio/mdlvoxelarray/coarsemesh())
- [func coarseMesh(using: (any MDLMeshBufferAllocator)?) -> MDLMesh?](/documentation/modelio/mdlvoxelarray/coarsemesh(using:))
- [func convertToSignedShellField()](/documentation/modelio/mdlvoxelarray/converttosignedshellfield())
- [func setVoxelsFor(MDLMesh, divisions: Int32, patchRadius: Float)](/documentation/modelio/mdlvoxelarray/setvoxelsfor(_:divisions:patchradius:))

## Reference

- [Model I/O Data Types](/documentation/modelio/model-i-o-data-types)

### Data Types

- [MDLAxisAlignedBoundingBox](/documentation/modelio/mdlaxisalignedboundingbox)

#### Initializers

- [init()](/documentation/modelio/mdlaxisalignedboundingbox/init())
- [init(maxBounds: vector_float3, minBounds: vector_float3)](/documentation/modelio/mdlaxisalignedboundingbox/init(maxbounds:minbounds:))

#### Instance Properties

- [var maxBounds: vector_float3](/documentation/modelio/mdlaxisalignedboundingbox/maxbounds)
- [var minBounds: vector_float3](/documentation/modelio/mdlaxisalignedboundingbox/minbounds)
- [MDLVoxelIndex](/documentation/modelio/mdlvoxelindex)
- [Model I/O Structures](/documentation/modelio/model-i-o-structures)

### Structures

- [MDLVoxelIndexExtent](/documentation/modelio/mdlvoxelindexextent)

#### Initializers

- [init()](/documentation/modelio/mdlvoxelindexextent/init())
- [init(minimumExtent: MDLVoxelIndex, maximumExtent: MDLVoxelIndex)](/documentation/modelio/mdlvoxelindexextent/init(minimumextent:maximumextent:))

#### Instance Properties

- [var maximumExtent: MDLVoxelIndex](/documentation/modelio/mdlvoxelindexextent/maximumextent)
- [var minimumExtent: MDLVoxelIndex](/documentation/modelio/mdlvoxelindexextent/minimumextent)
- [Model I/O Enumerations](/documentation/modelio/model-i-o-enumerations)

### Enumerations

- [MDLCameraProjection](/documentation/modelio/mdlcameraprojection)

#### Constants

- [case orthographic](/documentation/modelio/mdlcameraprojection/orthographic)
- [case perspective](/documentation/modelio/mdlcameraprojection/perspective)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlcameraprojection/init(rawvalue:))
- [MDLGeometryType](/documentation/modelio/mdlgeometrytype)

#### Constants

- [case points](/documentation/modelio/mdlgeometrytype/points)
- [case lines](/documentation/modelio/mdlgeometrytype/lines)
- [case triangles](/documentation/modelio/mdlgeometrytype/triangles)
- [case triangleStrips](/documentation/modelio/mdlgeometrytype/trianglestrips)
- [case quads](/documentation/modelio/mdlgeometrytype/quads)
- [case variableTopology](/documentation/modelio/mdlgeometrytype/variabletopology)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdlgeometrytype/init(rawvalue:))
- [MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth)

#### Constants

- [case invalid](/documentation/modelio/mdlindexbitdepth/invalid)
- [case uInt8](/documentation/modelio/mdlindexbitdepth/uint8-swift.enum.case)
- [case uInt16](/documentation/modelio/mdlindexbitdepth/uint16-swift.enum.case)
- [case uInt32](/documentation/modelio/mdlindexbitdepth/uint32-swift.enum.case)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlindexbitdepth/init(rawvalue:))

#### Type Properties

- [static var uint16: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint16-swift.type.property)
- [static var uint32: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint32-swift.type.property)
- [static var uint8: MDLIndexBitDepth](/documentation/modelio/mdlindexbitdepth/uint8-swift.type.property)
- [MDLLightType](/documentation/modelio/mdllighttype)

#### Constants

- [case unknown](/documentation/modelio/mdllighttype/unknown)
- [case ambient](/documentation/modelio/mdllighttype/ambient)
- [case directional](/documentation/modelio/mdllighttype/directional)
- [case spot](/documentation/modelio/mdllighttype/spot)
- [case point](/documentation/modelio/mdllighttype/point)
- [case linear](/documentation/modelio/mdllighttype/linear)
- [case discArea](/documentation/modelio/mdllighttype/discarea)
- [case rectangularArea](/documentation/modelio/mdllighttype/rectangulararea)
- [case superElliptical](/documentation/modelio/mdllighttype/superelliptical)
- [case photometric](/documentation/modelio/mdllighttype/photometric)
- [case probe](/documentation/modelio/mdllighttype/probe)
- [case environment](/documentation/modelio/mdllighttype/environment)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdllighttype/init(rawvalue:))
- [MDLMaterialFace](/documentation/modelio/mdlmaterialface)

#### Constants

- [case back](/documentation/modelio/mdlmaterialface/back)
- [case doubleSided](/documentation/modelio/mdlmaterialface/doublesided)
- [case front](/documentation/modelio/mdlmaterialface/front)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialface/init(rawvalue:))
- [MDLMaterialMipMapFilterMode](/documentation/modelio/mdlmaterialmipmapfiltermode)

#### Constants

- [case nearest](/documentation/modelio/mdlmaterialmipmapfiltermode/nearest)
- [case linear](/documentation/modelio/mdlmaterialmipmapfiltermode/linear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialmipmapfiltermode/init(rawvalue:))
- [MDLMaterialPropertyType](/documentation/modelio/mdlmaterialpropertytype)

#### Constants

- [case none](/documentation/modelio/mdlmaterialpropertytype/none)
- [case string](/documentation/modelio/mdlmaterialpropertytype/string)
- [case URL](/documentation/modelio/mdlmaterialpropertytype/url)
- [case texture](/documentation/modelio/mdlmaterialpropertytype/texture)
- [case color](/documentation/modelio/mdlmaterialpropertytype/color)
- [case float](/documentation/modelio/mdlmaterialpropertytype/float)
- [case float2](/documentation/modelio/mdlmaterialpropertytype/float2)
- [case float3](/documentation/modelio/mdlmaterialpropertytype/float3)
- [case float4](/documentation/modelio/mdlmaterialpropertytype/float4)
- [case matrix44](/documentation/modelio/mdlmaterialpropertytype/matrix44)

#### Enumeration Cases

- [case buffer](/documentation/modelio/mdlmaterialpropertytype/buffer)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialpropertytype/init(rawvalue:))
- [MDLMaterialSemantic](/documentation/modelio/mdlmaterialsemantic)

#### Constants

- [case baseColor](/documentation/modelio/mdlmaterialsemantic/basecolor)
- [case subsurface](/documentation/modelio/mdlmaterialsemantic/subsurface)
- [case metallic](/documentation/modelio/mdlmaterialsemantic/metallic)
- [case specular](/documentation/modelio/mdlmaterialsemantic/specular)
- [case specularExponent](/documentation/modelio/mdlmaterialsemantic/specularexponent)
- [case specularTint](/documentation/modelio/mdlmaterialsemantic/speculartint)
- [case roughness](/documentation/modelio/mdlmaterialsemantic/roughness)
- [case anisotropic](/documentation/modelio/mdlmaterialsemantic/anisotropic)
- [case anisotropicRotation](/documentation/modelio/mdlmaterialsemantic/anisotropicrotation)
- [case sheen](/documentation/modelio/mdlmaterialsemantic/sheen)
- [case sheenTint](/documentation/modelio/mdlmaterialsemantic/sheentint)
- [case clearcoat](/documentation/modelio/mdlmaterialsemantic/clearcoat)
- [case clearcoatGloss](/documentation/modelio/mdlmaterialsemantic/clearcoatgloss)
- [case emission](/documentation/modelio/mdlmaterialsemantic/emission)
- [case bump](/documentation/modelio/mdlmaterialsemantic/bump)
- [case opacity](/documentation/modelio/mdlmaterialsemantic/opacity)
- [case interfaceIndexOfRefraction](/documentation/modelio/mdlmaterialsemantic/interfaceindexofrefraction)
- [case materialIndexOfRefraction](/documentation/modelio/mdlmaterialsemantic/materialindexofrefraction)
- [case objectSpaceNormal](/documentation/modelio/mdlmaterialsemantic/objectspacenormal)
- [case tangentSpaceNormal](/documentation/modelio/mdlmaterialsemantic/tangentspacenormal)
- [case displacement](/documentation/modelio/mdlmaterialsemantic/displacement)
- [case displacementScale](/documentation/modelio/mdlmaterialsemantic/displacementscale)
- [case ambientOcclusion](/documentation/modelio/mdlmaterialsemantic/ambientocclusion)
- [case ambientOcclusionScale](/documentation/modelio/mdlmaterialsemantic/ambientocclusionscale)
- [case none](/documentation/modelio/mdlmaterialsemantic/none)
- [case userDefined](/documentation/modelio/mdlmaterialsemantic/userdefined)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialsemantic/init(rawvalue:))
- [MDLMaterialTextureFilterMode](/documentation/modelio/mdlmaterialtexturefiltermode)

#### Constants

- [case nearest](/documentation/modelio/mdlmaterialtexturefiltermode/nearest)
- [case linear](/documentation/modelio/mdlmaterialtexturefiltermode/linear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialtexturefiltermode/init(rawvalue:))
- [MDLMaterialTextureWrapMode](/documentation/modelio/mdlmaterialtexturewrapmode)

#### Constants

- [case clamp](/documentation/modelio/mdlmaterialtexturewrapmode/clamp)
- [case `repeat`](/documentation/modelio/mdlmaterialtexturewrapmode/repeat)
- [case mirror](/documentation/modelio/mdlmaterialtexturewrapmode/mirror)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmaterialtexturewrapmode/init(rawvalue:))
- [MDLMeshBufferType](/documentation/modelio/mdlmeshbuffertype)

#### Constants

- [case vertex](/documentation/modelio/mdlmeshbuffertype/vertex)
- [case index](/documentation/modelio/mdlmeshbuffertype/index)

#### Enumeration Cases

- [case custom](/documentation/modelio/mdlmeshbuffertype/custom)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlmeshbuffertype/init(rawvalue:))
- [MDLProbePlacement](/documentation/modelio/mdlprobeplacement)

#### Constants

- [case irradianceDistribution](/documentation/modelio/mdlprobeplacement/irradiancedistribution)
- [case uniformGrid](/documentation/modelio/mdlprobeplacement/uniformgrid)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdlprobeplacement/init(rawvalue:))
- [MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding)

#### Constants

- [case uInt8](/documentation/modelio/mdltexturechannelencoding/uint8-swift.enum.case)
- [case uInt16](/documentation/modelio/mdltexturechannelencoding/uint16-swift.enum.case)
- [case uInt24](/documentation/modelio/mdltexturechannelencoding/uint24-swift.enum.case)
- [case uInt32](/documentation/modelio/mdltexturechannelencoding/uint32-swift.enum.case)
- [case float16](/documentation/modelio/mdltexturechannelencoding/float16)
- [case float32](/documentation/modelio/mdltexturechannelencoding/float32)

#### Enumeration Cases

- [case float16SR](/documentation/modelio/mdltexturechannelencoding/float16sr)

#### Initializers

- [init?(rawValue: Int)](/documentation/modelio/mdltexturechannelencoding/init(rawvalue:))

#### Type Properties

- [static var uint16: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint16-swift.type.property)
- [static var uint24: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint24-swift.type.property)
- [static var uint32: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint32-swift.type.property)
- [static var uint8: MDLTextureChannelEncoding](/documentation/modelio/mdltexturechannelencoding/uint8-swift.type.property)
- [MDLVertexFormat](/documentation/modelio/mdlvertexformat)

#### Constants

- [case invalid](/documentation/modelio/mdlvertexformat/invalid)
- [case packedBit](/documentation/modelio/mdlvertexformat/packedbit)
- [case uCharBits](/documentation/modelio/mdlvertexformat/ucharbits)
- [case charBits](/documentation/modelio/mdlvertexformat/charbits)
- [case uCharNormalizedBits](/documentation/modelio/mdlvertexformat/ucharnormalizedbits)
- [case charNormalizedBits](/documentation/modelio/mdlvertexformat/charnormalizedbits)
- [case uShortBits](/documentation/modelio/mdlvertexformat/ushortbits)
- [case shortBits](/documentation/modelio/mdlvertexformat/shortbits)
- [case uShortNormalizedBits](/documentation/modelio/mdlvertexformat/ushortnormalizedbits)
- [case shortNormalizedBits](/documentation/modelio/mdlvertexformat/shortnormalizedbits)
- [case uIntBits](/documentation/modelio/mdlvertexformat/uintbits)
- [case intBits](/documentation/modelio/mdlvertexformat/intbits)
- [case halfBits](/documentation/modelio/mdlvertexformat/halfbits)
- [case floatBits](/documentation/modelio/mdlvertexformat/floatbits)
- [case uChar](/documentation/modelio/mdlvertexformat/uchar)
- [case uChar2](/documentation/modelio/mdlvertexformat/uchar2)
- [case uChar3](/documentation/modelio/mdlvertexformat/uchar3)
- [case uChar4](/documentation/modelio/mdlvertexformat/uchar4)
- [case char](/documentation/modelio/mdlvertexformat/char)
- [case char2](/documentation/modelio/mdlvertexformat/char2)
- [case char3](/documentation/modelio/mdlvertexformat/char3)
- [case char4](/documentation/modelio/mdlvertexformat/char4)
- [case uCharNormalized](/documentation/modelio/mdlvertexformat/ucharnormalized)
- [case uChar2Normalized](/documentation/modelio/mdlvertexformat/uchar2normalized)
- [case uChar3Normalized](/documentation/modelio/mdlvertexformat/uchar3normalized)
- [case uChar4Normalized](/documentation/modelio/mdlvertexformat/uchar4normalized)
- [case charNormalized](/documentation/modelio/mdlvertexformat/charnormalized)
- [case char2Normalized](/documentation/modelio/mdlvertexformat/char2normalized)
- [case char3Normalized](/documentation/modelio/mdlvertexformat/char3normalized)
- [case char4Normalized](/documentation/modelio/mdlvertexformat/char4normalized)
- [case uShort](/documentation/modelio/mdlvertexformat/ushort)
- [case uShort2](/documentation/modelio/mdlvertexformat/ushort2)
- [case uShort3](/documentation/modelio/mdlvertexformat/ushort3)
- [case uShort4](/documentation/modelio/mdlvertexformat/ushort4)
- [case short](/documentation/modelio/mdlvertexformat/short)
- [case short2](/documentation/modelio/mdlvertexformat/short2)
- [case short3](/documentation/modelio/mdlvertexformat/short3)
- [case short4](/documentation/modelio/mdlvertexformat/short4)
- [case uShortNormalized](/documentation/modelio/mdlvertexformat/ushortnormalized)
- [case uShort2Normalized](/documentation/modelio/mdlvertexformat/ushort2normalized)
- [case uShort3Normalized](/documentation/modelio/mdlvertexformat/ushort3normalized)
- [case uShort4Normalized](/documentation/modelio/mdlvertexformat/ushort4normalized)
- [case shortNormalized](/documentation/modelio/mdlvertexformat/shortnormalized)
- [case short2Normalized](/documentation/modelio/mdlvertexformat/short2normalized)
- [case short3Normalized](/documentation/modelio/mdlvertexformat/short3normalized)
- [case short4Normalized](/documentation/modelio/mdlvertexformat/short4normalized)
- [case uInt](/documentation/modelio/mdlvertexformat/uint)
- [case uInt2](/documentation/modelio/mdlvertexformat/uint2)
- [case uInt3](/documentation/modelio/mdlvertexformat/uint3)
- [case uInt4](/documentation/modelio/mdlvertexformat/uint4)
- [case int](/documentation/modelio/mdlvertexformat/int)
- [case int2](/documentation/modelio/mdlvertexformat/int2)
- [case int3](/documentation/modelio/mdlvertexformat/int3)
- [case int4](/documentation/modelio/mdlvertexformat/int4)
- [case half](/documentation/modelio/mdlvertexformat/half)
- [case half2](/documentation/modelio/mdlvertexformat/half2)
- [case half3](/documentation/modelio/mdlvertexformat/half3)
- [case half4](/documentation/modelio/mdlvertexformat/half4)
- [case float](/documentation/modelio/mdlvertexformat/float)
- [case float2](/documentation/modelio/mdlvertexformat/float2)
- [case float3](/documentation/modelio/mdlvertexformat/float3)
- [case float4](/documentation/modelio/mdlvertexformat/float4)
- [case int1010102Normalized](/documentation/modelio/mdlvertexformat/int1010102normalized)
- [case uInt1010102Normalized](/documentation/modelio/mdlvertexformat/uint1010102normalized)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlvertexformat/init(rawvalue:))
- [MDLAnimatedValueInterpolation](/documentation/modelio/mdlanimatedvalueinterpolation)

#### Enumeration Cases

- [case constant](/documentation/modelio/mdlanimatedvalueinterpolation/constant)
- [case linear](/documentation/modelio/mdlanimatedvalueinterpolation/linear)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdlanimatedvalueinterpolation/init(rawvalue:))
- [MDLDataPrecision](/documentation/modelio/mdldataprecision)

#### Enumeration Cases

- [case double](/documentation/modelio/mdldataprecision/double)
- [case float](/documentation/modelio/mdldataprecision/float)
- [case undefined](/documentation/modelio/mdldataprecision/undefined)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdldataprecision/init(rawvalue:))
- [MDLTransformOpRotationOrder](/documentation/modelio/mdltransformoprotationorder)

#### Enumeration Cases

- [case XYZ](/documentation/modelio/mdltransformoprotationorder/xyz)
- [case XZY](/documentation/modelio/mdltransformoprotationorder/xzy)
- [case YXZ](/documentation/modelio/mdltransformoprotationorder/yxz)
- [case YZX](/documentation/modelio/mdltransformoprotationorder/yzx)
- [case ZXY](/documentation/modelio/mdltransformoprotationorder/zxy)
- [case ZYX](/documentation/modelio/mdltransformoprotationorder/zyx)

#### Initializers

- [init?(rawValue: UInt)](/documentation/modelio/mdltransformoprotationorder/init(rawvalue:))
- [Model I/O Constants](/documentation/modelio/model-i-o-constants)

### Constants

- [let MDLVertexAttributeAnisotropy: String](/documentation/modelio/mdlvertexattributeanisotropy)
- [let MDLVertexAttributeBinormal: String](/documentation/modelio/mdlvertexattributebinormal)
- [let MDLVertexAttributeBitangent: String](/documentation/modelio/mdlvertexattributebitangent)
- [let MDLVertexAttributeColor: String](/documentation/modelio/mdlvertexattributecolor)
- [let MDLVertexAttributeEdgeCrease: String](/documentation/modelio/mdlvertexattributeedgecrease)
- [let MDLVertexAttributeJointIndices: String](/documentation/modelio/mdlvertexattributejointindices)
- [let MDLVertexAttributeJointWeights: String](/documentation/modelio/mdlvertexattributejointweights)
- [let MDLVertexAttributeNormal: String](/documentation/modelio/mdlvertexattributenormal)
- [let MDLVertexAttributeOcclusionValue: String](/documentation/modelio/mdlvertexattributeocclusionvalue)
- [let MDLVertexAttributePosition: String](/documentation/modelio/mdlvertexattributeposition)
- [let MDLVertexAttributeShadingBasisU: String](/documentation/modelio/mdlvertexattributeshadingbasisu)
- [let MDLVertexAttributeShadingBasisV: String](/documentation/modelio/mdlvertexattributeshadingbasisv)
- [let MDLVertexAttributeSubdivisionStencil: String](/documentation/modelio/mdlvertexattributesubdivisionstencil)
- [let MDLVertexAttributeTangent: String](/documentation/modelio/mdlvertexattributetangent)
- [let MDLVertexAttributeTextureCoordinate: String](/documentation/modelio/mdlvertexattributetexturecoordinate)
- [let kUTType3dObject: String](/documentation/modelio/kuttype3dobject)
- [let kUTTypeAlembic: String](/documentation/modelio/kuttypealembic)
- [let kUTTypePolygon: String](/documentation/modelio/kuttypepolygon)
- [let kUTTypeStereolithography: String](/documentation/modelio/kuttypestereolithography)
- [let kUTTypeUniversalSceneDescription: String](/documentation/modelio/kuttypeuniversalscenedescription)
- [let kUTTypeUniversalSceneDescriptionMobile: String](/documentation/modelio/kuttypeuniversalscenedescriptionmobile)

## Classes

- [MDLAnimatedMatrix4x4](/documentation/modelio/mdlanimatedmatrix4x4)

### Instance Properties

- [var double4x4Array: [double4x4]](/documentation/modelio/mdlanimatedmatrix4x4/double4x4array)
- [var float4x4Array: [float4x4]](/documentation/modelio/mdlanimatedmatrix4x4/float4x4array)

### Instance Methods

- [func double4x4Value(atTime: TimeInterval) -> matrix_double4x4](/documentation/modelio/mdlanimatedmatrix4x4/double4x4value(attime:))
- [func float4x4Value(atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdlanimatedmatrix4x4/float4x4value(attime:))
- [func reset(double4Array: [double4x4], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedmatrix4x4/reset(double4array:attimes:))
- [func reset(float4x4Array: [float4x4], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedmatrix4x4/reset(float4x4array:attimes:))
- [func setDouble4x4(matrix_double4x4, atTime: TimeInterval)](/documentation/modelio/mdlanimatedmatrix4x4/setdouble4x4(_:attime:))
- [func setFloat4x4(matrix_float4x4, atTime: TimeInterval)](/documentation/modelio/mdlanimatedmatrix4x4/setfloat4x4(_:attime:))
- [MDLAnimatedQuaternion](/documentation/modelio/mdlanimatedquaternion)

### Instance Properties

- [var doubleQuaternionArray: [simd_quatd]](/documentation/modelio/mdlanimatedquaternion/doublequaternionarray)
- [var floatQuaternionArray: [simd_quatf]](/documentation/modelio/mdlanimatedquaternion/floatquaternionarray)

### Instance Methods

- [func doubleQuaternionValue(atTime: TimeInterval) -> simd_quatd](/documentation/modelio/mdlanimatedquaternion/doublequaternionvalue(attime:))
- [func floatQuaternionValue(atTime: TimeInterval) -> simd_quatf](/documentation/modelio/mdlanimatedquaternion/floatquaternionvalue(attime:))
- [func reset(doubleQuaternionArray: [simd_quatd], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedquaternion/reset(doublequaternionarray:attimes:))
- [func reset(floatQuaternionArray: [simd_quatf], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedquaternion/reset(floatquaternionarray:attimes:))
- [func setDoubleQuaternion(simd_quatd, atTime: TimeInterval)](/documentation/modelio/mdlanimatedquaternion/setdoublequaternion(_:attime:))
- [func setFloatQuaternion(simd_quatf, atTime: TimeInterval)](/documentation/modelio/mdlanimatedquaternion/setfloatquaternion(_:attime:))
- [MDLAnimatedQuaternionArray](/documentation/modelio/mdlanimatedquaternionarray)

### Initializers

- [init(elementCount: Int)](/documentation/modelio/mdlanimatedquaternionarray/init(elementcount:))

### Instance Properties

- [var doubleQuaternionArray: [simd_quatd]](/documentation/modelio/mdlanimatedquaternionarray/doublequaternionarray)
- [var elementCount: Int](/documentation/modelio/mdlanimatedquaternionarray/elementcount)
- [var floatQuaternionArray: [simd_quatf]](/documentation/modelio/mdlanimatedquaternionarray/floatquaternionarray)

### Instance Methods

- [func doubleQuaternionArray(atTime: TimeInterval) -> [simd_quatd]](/documentation/modelio/mdlanimatedquaternionarray/doublequaternionarray(attime:))
- [func floatQuaternionArray(atTime: TimeInterval) -> [simd_quatf]](/documentation/modelio/mdlanimatedquaternionarray/floatquaternionarray(attime:))
- [func reset(doubleQuaternionArray: [simd_quatd], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedquaternionarray/reset(doublequaternionarray:attimes:))
- [func reset(floatQuaternionArray: [simd_quatf], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedquaternionarray/reset(floatquaternionarray:attimes:))
- [func set(doubleQuaternionArray: [simd_quatd], atTime: TimeInterval)](/documentation/modelio/mdlanimatedquaternionarray/set(doublequaternionarray:attime:))
- [func set(floatQuaternionArray: [simd_quatf], atTime: TimeInterval)](/documentation/modelio/mdlanimatedquaternionarray/set(floatquaternionarray:attime:))
- [MDLAnimatedScalar](/documentation/modelio/mdlanimatedscalar)

### Instance Properties

- [var doubleArray: [Double]](/documentation/modelio/mdlanimatedscalar/doublearray)
- [var floatArray: [Float]](/documentation/modelio/mdlanimatedscalar/floatarray)

### Instance Methods

- [func doubleValue(atTime: TimeInterval) -> Double](/documentation/modelio/mdlanimatedscalar/doublevalue(attime:))
- [func floatValue(atTime: TimeInterval) -> Float](/documentation/modelio/mdlanimatedscalar/floatvalue(attime:))
- [func reset(doubleArray: [Double], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedscalar/reset(doublearray:attimes:))
- [func reset(floatArray: [Float], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedscalar/reset(floatarray:attimes:))
- [func setDouble(Double, atTime: TimeInterval)](/documentation/modelio/mdlanimatedscalar/setdouble(_:attime:))
- [func setFloat(Float, atTime: TimeInterval)](/documentation/modelio/mdlanimatedscalar/setfloat(_:attime:))
- [MDLAnimatedScalarArray](/documentation/modelio/mdlanimatedscalararray)

### Initializers

- [init(elementCount: Int)](/documentation/modelio/mdlanimatedscalararray/init(elementcount:))

### Instance Properties

- [var doubleArray: [Double]](/documentation/modelio/mdlanimatedscalararray/doublearray)
- [var elementCount: Int](/documentation/modelio/mdlanimatedscalararray/elementcount)
- [var floatArray: [Float]](/documentation/modelio/mdlanimatedscalararray/floatarray)

### Instance Methods

- [func doubleArray(atTime: TimeInterval) -> [Double]](/documentation/modelio/mdlanimatedscalararray/doublearray(attime:))
- [func floatArray(atTime: TimeInterval) -> [Float]](/documentation/modelio/mdlanimatedscalararray/floatarray(attime:))
- [func reset(doubleArray: [Double], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedscalararray/reset(doublearray:attimes:))
- [func reset(floatArray: [Float], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedscalararray/reset(floatarray:attimes:))
- [func set(doubleArray: [Double], atTime: TimeInterval)](/documentation/modelio/mdlanimatedscalararray/set(doublearray:attime:))
- [func set(floatArray: [Float], atTime: TimeInterval)](/documentation/modelio/mdlanimatedscalararray/set(floatarray:attime:))
- [MDLAnimatedValue](/documentation/modelio/mdlanimatedvalue)

### Instance Properties

- [var interpolation: MDLAnimatedValueInterpolation](/documentation/modelio/mdlanimatedvalue/interpolation)
- [var keyTimes: [NSNumber]](/documentation/modelio/mdlanimatedvalue/keytimes)
- [var maximumTime: TimeInterval](/documentation/modelio/mdlanimatedvalue/maximumtime)
- [var minimumTime: TimeInterval](/documentation/modelio/mdlanimatedvalue/minimumtime)
- [var precision: MDLDataPrecision](/documentation/modelio/mdlanimatedvalue/precision)
- [var timeSampleCount: Int](/documentation/modelio/mdlanimatedvalue/timesamplecount)
- [var times: [TimeInterval]](/documentation/modelio/mdlanimatedvalue/times)

### Instance Methods

- [func clear()](/documentation/modelio/mdlanimatedvalue/clear())
- [func isAnimated() -> Bool](/documentation/modelio/mdlanimatedvalue/isanimated())
- [MDLAnimatedVector2](/documentation/modelio/mdlanimatedvector2)

### Instance Properties

- [var double2Array: [SIMD2<Double>]](/documentation/modelio/mdlanimatedvector2/double2array)
- [var float2Array: [SIMD2<Float>]](/documentation/modelio/mdlanimatedvector2/float2array)

### Instance Methods

- [func double2Value(atTime: TimeInterval) -> vector_double2](/documentation/modelio/mdlanimatedvector2/double2value(attime:))
- [func float2Value(atTime: TimeInterval) -> vector_float2](/documentation/modelio/mdlanimatedvector2/float2value(attime:))
- [func reset(double2Array: [SIMD2<Double>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector2/reset(double2array:attimes:))
- [func reset(float2Array: [SIMD2<Float>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector2/reset(float2array:attimes:))
- [func setDouble2(vector_double2, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector2/setdouble2(_:attime:))
- [func setFloat2(vector_float2, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector2/setfloat2(_:attime:))
- [MDLAnimatedVector3](/documentation/modelio/mdlanimatedvector3)

### Instance Properties

- [var double3Array: [SIMD3<Double>]](/documentation/modelio/mdlanimatedvector3/double3array)
- [var float3Array: [SIMD3<Float>]](/documentation/modelio/mdlanimatedvector3/float3array)

### Instance Methods

- [func double3Value(atTime: TimeInterval) -> vector_double3](/documentation/modelio/mdlanimatedvector3/double3value(attime:))
- [func float3Value(atTime: TimeInterval) -> vector_float3](/documentation/modelio/mdlanimatedvector3/float3value(attime:))
- [func reset(double3Array: [SIMD3<Double>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector3/reset(double3array:attimes:))
- [func reset(float3Array: [SIMD3<Float>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector3/reset(float3array:attimes:))
- [func setDouble3(vector_double3, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector3/setdouble3(_:attime:))
- [func setFloat3(vector_float3, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector3/setfloat3(_:attime:))
- [MDLAnimatedVector3Array](/documentation/modelio/mdlanimatedvector3array)

### Initializers

- [init(elementCount: Int)](/documentation/modelio/mdlanimatedvector3array/init(elementcount:))

### Instance Properties

- [var double3Array: [SIMD3<Double>]](/documentation/modelio/mdlanimatedvector3array/double3array)
- [var elementCount: Int](/documentation/modelio/mdlanimatedvector3array/elementcount)
- [var float3Array: [SIMD3<Float>]](/documentation/modelio/mdlanimatedvector3array/float3array)

### Instance Methods

- [func double3Array(atTime: TimeInterval) -> [SIMD3<Double>]](/documentation/modelio/mdlanimatedvector3array/double3array(attime:))
- [func float3Array(atTime: TimeInterval) -> [SIMD3<Float>]](/documentation/modelio/mdlanimatedvector3array/float3array(attime:))
- [func reset(double3Array: [SIMD3<Double>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector3array/reset(double3array:attimes:))
- [func reset(float3Array: [SIMD3<Float>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector3array/reset(float3array:attimes:))
- [func set(double3Array: [SIMD3<Double>], atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector3array/set(double3array:attime:))
- [func set(float3Array: [SIMD3<Float>], atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector3array/set(float3array:attime:))
- [MDLAnimatedVector4](/documentation/modelio/mdlanimatedvector4)

### Instance Properties

- [var double4Array: [SIMD4<Double>]](/documentation/modelio/mdlanimatedvector4/double4array)
- [var float4Array: [SIMD4<Float>]](/documentation/modelio/mdlanimatedvector4/float4array)

### Instance Methods

- [func double4Value(atTime: TimeInterval) -> vector_double4](/documentation/modelio/mdlanimatedvector4/double4value(attime:))
- [func float4Value(atTime: TimeInterval) -> vector_float4](/documentation/modelio/mdlanimatedvector4/float4value(attime:))
- [func reset(double4Array: [SIMD4<Double>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector4/reset(double4array:attimes:))
- [func reset(float4Array: [SIMD4<Float>], atTimes: [TimeInterval])](/documentation/modelio/mdlanimatedvector4/reset(float4array:attimes:))
- [func setDouble4(vector_double4, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector4/setdouble4(_:attime:))
- [func setFloat4(vector_float4, atTime: TimeInterval)](/documentation/modelio/mdlanimatedvector4/setfloat4(_:attime:))
- [MDLAnimationBindComponent](/documentation/modelio/mdlanimationbindcomponent)

### Instance Properties

- [var geometryBindTransform: matrix_double4x4](/documentation/modelio/mdlanimationbindcomponent/geometrybindtransform)
- [var jointAnimation: (any MDLJointAnimation)?](/documentation/modelio/mdlanimationbindcomponent/jointanimation)
- [var jointPaths: [String]?](/documentation/modelio/mdlanimationbindcomponent/jointpaths)
- [var skeleton: MDLSkeleton?](/documentation/modelio/mdlanimationbindcomponent/skeleton)
- [MDLBundleAssetResolver](/documentation/modelio/mdlbundleassetresolver)

### Initializers

- [init(bundle: String)](/documentation/modelio/mdlbundleassetresolver/init(bundle:))

### Instance Properties

- [var path: String](/documentation/modelio/mdlbundleassetresolver/path)
- [MDLMatrix4x4Array](/documentation/modelio/mdlmatrix4x4array)

### Initializers

- [init(elementCount: Int)](/documentation/modelio/mdlmatrix4x4array/init(elementcount:))

### Instance Properties

- [var double4x4Array: [double4x4]](/documentation/modelio/mdlmatrix4x4array/double4x4array)
- [var elementCount: Int](/documentation/modelio/mdlmatrix4x4array/elementcount)
- [var float4x4Array: [float4x4]](/documentation/modelio/mdlmatrix4x4array/float4x4array)
- [var precision: MDLDataPrecision](/documentation/modelio/mdlmatrix4x4array/precision)

### Instance Methods

- [func clear()](/documentation/modelio/mdlmatrix4x4array/clear())
- [MDLPackedJointAnimation](/documentation/modelio/mdlpackedjointanimation)

### Initializers

- [init(name: String, jointPaths: [String])](/documentation/modelio/mdlpackedjointanimation/init(name:jointpaths:))

### Instance Properties

- [var jointPaths: [String]](/documentation/modelio/mdlpackedjointanimation/jointpaths)
- [var rotations: MDLAnimatedQuaternionArray](/documentation/modelio/mdlpackedjointanimation/rotations)
- [var scales: MDLAnimatedVector3Array](/documentation/modelio/mdlpackedjointanimation/scales)
- [var translations: MDLAnimatedVector3Array](/documentation/modelio/mdlpackedjointanimation/translations)
- [MDLPathAssetResolver](/documentation/modelio/mdlpathassetresolver)

### Initializers

- [init(path: String)](/documentation/modelio/mdlpathassetresolver/init(path:))

### Instance Properties

- [var path: String](/documentation/modelio/mdlpathassetresolver/path)
- [MDLRelativeAssetResolver](/documentation/modelio/mdlrelativeassetresolver)

### Initializers

- [init(asset: MDLAsset)](/documentation/modelio/mdlrelativeassetresolver/init(asset:))

### Instance Properties

- [var asset: MDLAsset?](/documentation/modelio/mdlrelativeassetresolver/asset)
- [MDLSkeleton](/documentation/modelio/mdlskeleton)

### Initializers

- [init(name: String, jointPaths: [String])](/documentation/modelio/mdlskeleton/init(name:jointpaths:))

### Instance Properties

- [var jointBindTransforms: MDLMatrix4x4Array](/documentation/modelio/mdlskeleton/jointbindtransforms)
- [var jointPaths: [String]](/documentation/modelio/mdlskeleton/jointpaths)
- [var jointRestTransforms: MDLMatrix4x4Array](/documentation/modelio/mdlskeleton/jointresttransforms)
- [MDLTransformMatrixOp](/documentation/modelio/mdltransformmatrixop)

### Instance Properties

- [var animatedValue: MDLAnimatedMatrix4x4](/documentation/modelio/mdltransformmatrixop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformmatrixop/name)
- [MDLTransformOrientOp](/documentation/modelio/mdltransformorientop)

### Instance Properties

- [var animatedValue: MDLAnimatedQuaternion](/documentation/modelio/mdltransformorientop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformorientop/name)
- [MDLTransformRotateOp](/documentation/modelio/mdltransformrotateop)

### Instance Properties

- [var animatedValue: MDLAnimatedVector3](/documentation/modelio/mdltransformrotateop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformrotateop/name)
- [MDLTransformRotateXOp](/documentation/modelio/mdltransformrotatexop)

### Instance Properties

- [var animatedValue: MDLAnimatedScalar](/documentation/modelio/mdltransformrotatexop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformrotatexop/name)
- [MDLTransformRotateYOp](/documentation/modelio/mdltransformrotateyop)

### Instance Properties

- [var animatedValue: MDLAnimatedScalar](/documentation/modelio/mdltransformrotateyop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformrotateyop/name)
- [MDLTransformRotateZOp](/documentation/modelio/mdltransformrotatezop)

### Instance Properties

- [var animatedValue: MDLAnimatedScalar](/documentation/modelio/mdltransformrotatezop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformrotatezop/name)
- [MDLTransformScaleOp](/documentation/modelio/mdltransformscaleop)

### Instance Properties

- [var animatedValue: MDLAnimatedVector3](/documentation/modelio/mdltransformscaleop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformscaleop/name)
- [MDLTransformStack](/documentation/modelio/mdltransformstack)

### Initializers

- [init()](/documentation/modelio/mdltransformstack/init())

### Instance Properties

- [var keyTimes: [NSNumber]](/documentation/modelio/mdltransformstack/keytimes)
- [var transformOps: [any MDLTransformOp]](/documentation/modelio/mdltransformstack/transformops)

### Instance Methods

- [func addMatrixOp(String, inverse: Bool) -> MDLTransformMatrixOp](/documentation/modelio/mdltransformstack/addmatrixop(_:inverse:))
- [func addOrientOp(String, inverse: Bool) -> MDLTransformOrientOp](/documentation/modelio/mdltransformstack/addorientop(_:inverse:))
- [func addRotateOp(String, order: MDLTransformOpRotationOrder, inverse: Bool) -> MDLTransformRotateOp](/documentation/modelio/mdltransformstack/addrotateop(_:order:inverse:))
- [func addRotateXOp(String, inverse: Bool) -> MDLTransformRotateXOp](/documentation/modelio/mdltransformstack/addrotatexop(_:inverse:))
- [func addRotateYOp(String, inverse: Bool) -> MDLTransformRotateYOp](/documentation/modelio/mdltransformstack/addrotateyop(_:inverse:))
- [func addRotateZOp(String, inverse: Bool) -> MDLTransformRotateZOp](/documentation/modelio/mdltransformstack/addrotatezop(_:inverse:))
- [func addScaleOp(String, inverse: Bool) -> MDLTransformScaleOp](/documentation/modelio/mdltransformstack/addscaleop(_:inverse:))
- [func addTranslateOp(String, inverse: Bool) -> MDLTransformTranslateOp](/documentation/modelio/mdltransformstack/addtranslateop(_:inverse:))
- [func animatedValue(withName: String) -> MDLAnimatedValue](/documentation/modelio/mdltransformstack/animatedvalue(withname:))
- [func count() -> Int](/documentation/modelio/mdltransformstack/count())
- [func double4x4(atTime: TimeInterval) -> matrix_double4x4](/documentation/modelio/mdltransformstack/double4x4(attime:))
- [func float4x4(atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdltransformstack/float4x4(attime:))
- [MDLTransformTranslateOp](/documentation/modelio/mdltransformtranslateop)

### Instance Properties

- [var animatedValue: MDLAnimatedVector3](/documentation/modelio/mdltransformtranslateop/animatedvalue)
- [var name: String](/documentation/modelio/mdltransformtranslateop/name)
- [MDLUtility](/documentation/modelio/mdlutility)

### Type Methods

- [class func convert(toUSDZ: URL, writeTo: URL)](/documentation/modelio/mdlutility/convert(tousdz:writeto:))

## Protocols

- [MDLAssetResolver](/documentation/modelio/mdlassetresolver)

### Instance Methods

- [func canResolveAssetNamed(String) -> Bool](/documentation/modelio/mdlassetresolver/canresolveassetnamed(_:))
- [func resolveAssetNamed(String) -> URL](/documentation/modelio/mdlassetresolver/resolveassetnamed(_:))
- [MDLJointAnimation](/documentation/modelio/mdljointanimation)
- [MDLTransformOp](/documentation/modelio/mdltransformop)

### Instance Properties

- [var name: String](/documentation/modelio/mdltransformop/name)

### Instance Methods

- [func double4x4(atTime: TimeInterval) -> matrix_double4x4](/documentation/modelio/mdltransformop/double4x4(attime:))
- [func float4x4(atTime: TimeInterval) -> matrix_float4x4](/documentation/modelio/mdltransformop/float4x4(attime:))
- [func isInverseOp() -> Bool](/documentation/modelio/mdltransformop/isinverseop())

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
