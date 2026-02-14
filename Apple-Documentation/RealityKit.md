# RealityKit Documentation

Source: https://sosumi.ai/documentation/realitykit

---
title: RealityKit
source: https://developer.apple.com/documentation/realitykit
timestamp: 2026-02-13T19:01:08.419Z
---

## Essentials

- [Understanding the modular architecture of RealityKit](/documentation/visionos/understanding-the-realitykit-modular-architecture)
- [Building an immersive experience with RealityKit](/documentation/realitykit/building-an-immersive-experience-with-realitykit)
- [Entity](/documentation/realitykit/entity)

### Creating an entity

- [init()](/documentation/realitykit/entity/init())
- [convenience init(components: [any Component])](/documentation/realitykit/entity/init(components:)-1lmhe)
- [convenience init(components: [any Component])](/documentation/realitykit/entity/init(components:)-1lmhe)
- [func clone(recursive: Bool) -> Self](/documentation/realitykit/entity/clone(recursive:))
- [func didClone(from: Entity)](/documentation/realitykit/entity/didclone(from:))

### Loading an entity from a file

- [Resource](/documentation/realitykit/resource)
- [Loading entities from a file](/documentation/realitykit/loading-entities-from-a-file)
- [Stored entities](/documentation/realitykit/stored-entities)

#### Essentials

- [Loading entities from a file](/documentation/realitykit/loading-entities-from-a-file)
- [LoadRequest](/documentation/realitykit/loadrequest)

##### Getting the result

- [var result: Result<Output, any Error>?](/documentation/realitykit/loadrequest/result)

##### Instance Methods

- [func subscribe<S>(S)](/documentation/realitykit/loadrequest/subscribe(_:))

#### Loading an entity hierarchy

- [static func load(named: String, in: Bundle?) throws -> Entity](/documentation/realitykit/entity/load(named:in:))
- [static func load(contentsOf: URL, withName: String?) throws -> Entity](/documentation/realitykit/entity/load(contentsof:withname:))
- [static func loadAsync(named: String, in: Bundle?) -> LoadRequest<Entity>](/documentation/realitykit/entity/loadasync(named:in:))
- [static func loadAsync(contentsOf: URL, withName: String?) -> LoadRequest<Entity>](/documentation/realitykit/entity/loadasync(contentsof:withname:))

#### Loading an anchor entity

- [static func loadAnchor(named: String, in: Bundle?) throws -> AnchorEntity](/documentation/realitykit/entity/loadanchor(named:in:))
- [static func loadAnchor(contentsOf: URL, withName: String?) throws -> AnchorEntity](/documentation/realitykit/entity/loadanchor(contentsof:withname:))
- [static func loadAnchorAsync(named: String, in: Bundle?) -> LoadRequest<AnchorEntity>](/documentation/realitykit/entity/loadanchorasync(named:in:))
- [static func loadAnchorAsync(contentsOf: URL, withName: String?) -> LoadRequest<AnchorEntity>](/documentation/realitykit/entity/loadanchorasync(contentsof:withname:))

#### Loading a flattened model entity

- [static func loadModel(named: String, in: Bundle?) throws -> ModelEntity](/documentation/realitykit/entity/loadmodel(named:in:))
- [static func loadModel(contentsOf: URL, withName: String?) throws -> ModelEntity](/documentation/realitykit/entity/loadmodel(contentsof:withname:))
- [static func loadModelAsync(named: String, in: Bundle?) -> LoadRequest<ModelEntity>](/documentation/realitykit/entity/loadmodelasync(named:in:))
- [static func loadModelAsync(contentsOf: URL, withName: String?) -> LoadRequest<ModelEntity>](/documentation/realitykit/entity/loadmodelasync(contentsof:withname:))

#### Loading a flattened body-tracked entity

- [static func loadBodyTracked(named: String, in: Bundle?) throws -> BodyTrackedEntity](/documentation/realitykit/entity/loadbodytracked(named:in:))
- [static func loadBodyTracked(contentsOf: URL, withName: String?) throws -> BodyTrackedEntity](/documentation/realitykit/entity/loadbodytracked(contentsof:withname:))
- [static func loadBodyTrackedAsync(contentsOf: URL, withName: String?) -> LoadRequest<BodyTrackedEntity>](/documentation/realitykit/entity/loadbodytrackedasync(contentsof:withname:))
- [static func loadBodyTrackedAsync(named: String, in: Bundle?) -> LoadRequest<BodyTrackedEntity>](/documentation/realitykit/entity/loadbodytrackedasync(named:in:))
- [Creating USD files for Apple devices](/documentation/usd/creating-usd-files-for-apple-devices)
- [convenience init(contentsOf: URL, withName: String?) async throws](/documentation/realitykit/entity/init(contentsof:withname:))
- [convenience init(named: String, in: Bundle?) async throws](/documentation/realitykit/entity/init(named:in:))
- [ReferenceComponent](/documentation/realitykit/referencecomponent)

#### Initializers

- [init(named: String, at: String, loadingPolicy: ReferenceComponent.LoadingPolicy)](/documentation/realitykit/referencecomponent/init(named:at:loadingpolicy:))
- [init(named: String, in: Bundle, loadingPolicy: ReferenceComponent.LoadingPolicy)](/documentation/realitykit/referencecomponent/init(named:in:loadingpolicy:))
- [init(named: String, loadingPolicy: ReferenceComponent.LoadingPolicy)](/documentation/realitykit/referencecomponent/init(named:loadingpolicy:))

#### Instance Properties

- [var loadingPolicy: ReferenceComponent.LoadingPolicy](/documentation/realitykit/referencecomponent/loadingpolicy-swift.property)
- [var reference: Entity?](/documentation/realitykit/referencecomponent/reference)
- [var state: ReferenceComponent.ReferenceState](/documentation/realitykit/referencecomponent/state)

#### Type Methods

- [static loadReference(at:)](/documentation/realitykit/referencecomponent/loadreference(at:))
- [static func releaseReference(at: Entity) throws](/documentation/realitykit/referencecomponent/releasereference(at:))

#### Enumerations

- [ReferenceComponent.LoadingPolicy](/documentation/realitykit/referencecomponent/loadingpolicy-swift.enum)

##### Enumeration Cases

- [case immediate](/documentation/realitykit/referencecomponent/loadingpolicy-swift.enum/immediate)
- [case onDemand](/documentation/realitykit/referencecomponent/loadingpolicy-swift.enum/ondemand)
- [ReferenceComponent.ReferenceState](/documentation/realitykit/referencecomponent/referencestate)

##### Enumeration Cases

- [case loaded](/documentation/realitykit/referencecomponent/referencestate/loaded)
- [case loading](/documentation/realitykit/referencecomponent/referencestate/loading)
- [case notLoaded](/documentation/realitykit/referencecomponent/referencestate/notloaded)

### Loading an entity from a configuration catalog

- [convenience init(from: Entity.ConfigurationCatalog, configurations: [String : String]?) async throws](/documentation/realitykit/entity/init(from:configurations:))
- [Entity.ConfigurationCatalog](/documentation/realitykit/entity/configurationcatalog)

#### Opening a catalog from a file

- [init(from: URL) async throws](/documentation/realitykit/entity/configurationcatalog/init(from:))

#### Defining configuration choices

- [Entity.ConfigurationCatalog.Configuration](/documentation/realitykit/entity/configurationcatalog/configuration)

##### Creating a configuration

- [init(id: String)](/documentation/realitykit/entity/configurationcatalog/configuration/init(id:))

##### Accessing a configuration’s name

- [var id: String](/documentation/realitykit/entity/configurationcatalog/configuration/id)
- [Entity.ConfigurationCatalog.ConfigurationSet](/documentation/realitykit/entity/configurationcatalog/configurationset)

##### Creating a configuration set

- [init(id: String, configurations: [Entity.ConfigurationCatalog.Configuration], defaultConfigurationId: String?) throws](/documentation/realitykit/entity/configurationcatalog/configurationset/init(id:configurations:defaultconfigurationid:)-5erwz)
- [init(id: String, configurations: [Entity.ConfigurationCatalog.Configuration], defaultConfigurationId: String?) throws](/documentation/realitykit/entity/configurationcatalog/configurationset/init(id:configurations:defaultconfigurationid:)-5erwz)

##### Accessing a configuration set’s name

- [var id: String](/documentation/realitykit/entity/configurationcatalog/configurationset/id)

##### Accessing configurations in a configuration set

- [var configurations: [String : Entity.ConfigurationCatalog.Configuration]](/documentation/realitykit/entity/configurationcatalog/configurationset/configurations)
- [var defaultConfiguration: Entity.ConfigurationCatalog.Configuration](/documentation/realitykit/entity/configurationcatalog/configurationset/defaultconfiguration)

##### Initializers

- [init(id:configurations:defaultConfigurationId:)](/documentation/realitykit/entity/configurationcatalog/configurationset/init(id:configurations:defaultconfigurationid:))
- [Entity.ConfigurationCatalog.ConfigurationCombination](/documentation/realitykit/entity/configurationcatalog/configurationcombination)

##### Creating a configuration combination

- [init(entity: Entity, configurationSpecifications: [String : String])](/documentation/realitykit/entity/configurationcatalog/configurationcombination/init(entity:configurationspecifications:))

##### Accessing values

- [let entity: Entity](/documentation/realitykit/entity/configurationcatalog/configurationcombination/entity)
- [let configurationSpecifications: [String : String]](/documentation/realitykit/entity/configurationcatalog/configurationcombination/configurationspecifications)

#### Querying available configuration choices

- [var configurationSets: [String : Entity.ConfigurationCatalog.ConfigurationSet]](/documentation/realitykit/entity/configurationcatalog/configurationsets)

#### Creating a configuration catalog from entities

- [init(configurationSets: [Entity.ConfigurationCatalog.ConfigurationSet], combinations: [Entity.ConfigurationCatalog.ConfigurationCombination]) throws](/documentation/realitykit/entity/configurationcatalog/init(configurationsets:combinations:)-1difa)
- [init(configurationSets: [Entity.ConfigurationCatalog.ConfigurationSet], combinations: [Entity.ConfigurationCatalog.ConfigurationCombination]) throws](/documentation/realitykit/entity/configurationcatalog/init(configurationsets:combinations:)-1difa)

#### Saving a configuration catalog to a file

- [func write(to: URL) async throws](/documentation/realitykit/entity/configurationcatalog/write(to:))

#### Initializers

- [init(configurationSets:combinations:)](/documentation/realitykit/entity/configurationcatalog/init(configurationsets:combinations:))

### Positioning entities in space

- [HasTransform](/documentation/realitykit/hastransform)

#### Accessing the component

- [var transform: Transform](/documentation/realitykit/hastransform/transform)

#### Scaling an entity

- [var scale: SIMD3<Float>](/documentation/realitykit/hastransform/scale)
- [func scale(relativeTo: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/scale(relativeto:))
- [func setScale(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hastransform/setscale(_:relativeto:))

#### Rotating an entity

- [var orientation: simd_quatf](/documentation/realitykit/hastransform/orientation)
- [func orientation(relativeTo: Entity?) -> simd_quatf](/documentation/realitykit/hastransform/orientation(relativeto:))
- [func setOrientation(simd_quatf, relativeTo: Entity?)](/documentation/realitykit/hastransform/setorientation(_:relativeto:))

#### Positioning an entity

- [var position: SIMD3<Float>](/documentation/realitykit/hastransform/position)
- [func position(relativeTo: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/position(relativeto:))
- [func setPosition(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hastransform/setposition(_:relativeto:))

#### Using a matrix

- [Transforming entities between RealityKit coordinate spaces](/documentation/realitykit/transforming-entities-between-realitykit-coordinate-spaces)
- [func transformMatrix(relativeTo: Entity?) -> float4x4](/documentation/realitykit/hastransform/transformmatrix(relativeto:))

#### Moving an entity

- [func move(to: Transform, relativeTo: Entity?)](/documentation/realitykit/hastransform/move(to:relativeto:)-6lohd)
- [func move(to: float4x4, relativeTo: Entity?)](/documentation/realitykit/hastransform/move(to:relativeto:)-6jul8)
- [func look(at: SIMD3<Float>, from: SIMD3<Float>, upVector: SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hastransform/look(at:from:upvector:relativeto:))
- [func look(at: SIMD3<Float>, from: SIMD3<Float>, upVector: SIMD3<Float>, relativeTo: Entity?, forward: Entity.ForwardDirection)](/documentation/realitykit/hastransform/look(at:from:upvector:relativeto:forward:))
- [func align(GeometricPin, to: GeometricPin) -> float4x4?](/documentation/realitykit/hastransform/align(_:to:))

#### Animating an entity

- [func move(to: Transform, relativeTo: Entity?, duration: TimeInterval, timingFunction: AnimationTimingFunction) -> AnimationPlaybackController](/documentation/realitykit/hastransform/move(to:relativeto:duration:timingfunction:)-35qp2)
- [func move(to: float4x4, relativeTo: Entity?, duration: TimeInterval, timingFunction: AnimationTimingFunction) -> AnimationPlaybackController](/documentation/realitykit/hastransform/move(to:relativeto:duration:timingfunction:)-6la93)

#### Converting values between coordinate spaces

- [func convert(position: SIMD3<Float>, from: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(position:from:))
- [func convert(position: SIMD3<Float>, to: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(position:to:))
- [func convert(direction: SIMD3<Float>, from: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(direction:from:))
- [func convert(direction: SIMD3<Float>, to: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(direction:to:))
- [func convert(normal: SIMD3<Float>, from: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(normal:from:))
- [func convert(normal: SIMD3<Float>, to: Entity?) -> SIMD3<Float>](/documentation/realitykit/hastransform/convert(normal:to:))
- [func convert(transform: Transform, from: Entity?) -> Transform](/documentation/realitykit/hastransform/convert(transform:from:))
- [func convert(transform: Transform, to: Entity?) -> Transform](/documentation/realitykit/hastransform/convert(transform:to:))

#### Getting a bounding box

- [func visualBounds(recursive: Bool, relativeTo: Entity?, excludeInactive: Bool) -> BoundingBox](/documentation/realitykit/hastransform/visualbounds(recursive:relativeto:excludeinactive:))

#### Instance Methods

- [func move(to:relativeTo:)](/documentation/realitykit/hastransform/move(to:relativeto:))
- [func move(to:relativeTo:duration:timingFunction:)](/documentation/realitykit/hastransform/move(to:relativeto:duration:timingfunction:))
- [func setTransformMatrix(float4x4, relativeTo: Entity?)](/documentation/realitykit/hastransform/settransformmatrix(_:relativeto:))
- [Transform](/documentation/realitykit/transform)

#### Creating a transform

- [init()](/documentation/realitykit/transform/init())
- [init(scale: SIMD3<Float>, rotation: simd_quatf, translation: SIMD3<Float>)](/documentation/realitykit/transform/init(scale:rotation:translation:))
- [init(pitch: Float, yaw: Float, roll: Float)](/documentation/realitykit/transform/init(pitch:yaw:roll:))
- [init(matrix: float4x4)](/documentation/realitykit/transform/init(matrix:))

#### Setting transform properties

- [var scale: SIMD3<Float>](/documentation/realitykit/transform/scale)
- [var rotation: simd_quatf](/documentation/realitykit/transform/rotation)
- [var translation: SIMD3<Float>](/documentation/realitykit/transform/translation)
- [var matrix: float4x4](/documentation/realitykit/transform/matrix)

#### Getting the identity transform

- [static let identity: Transform](/documentation/realitykit/transform/identity)

#### Initializers

- [init(AffineTransform3D)](/documentation/realitykit/transform/init(_:))
- [init(projectiveTransform:)](/documentation/realitykit/transform/init(projectivetransform:))

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/transform/hash(into:))

#### Default Implementations

- [ProjectiveTransformable3DFloat Implementations](/documentation/realitykit/transform/projectivetransformable3dfloat-implementations)

##### Instance Methods

- [func applying(ProjectiveTransform3DFloat) -> Transform](/documentation/realitykit/transform/applying(_:))
- [func transformMatrix(relativeTo: Entity.CoordinateSpaceReference) -> float4x4?](/documentation/realitykit/entity/transformmatrix(relativeto:))
- [Entity.CoordinateSpaceReference](/documentation/realitykit/entity/coordinatespacereference)

#### Enumeration Cases

- [case immersiveSpace](/documentation/realitykit/entity/coordinatespacereference/immersivespace)
- [case scene](/documentation/realitykit/entity/coordinatespacereference/scene)
- [Entity.ForwardDirection](/documentation/realitykit/entity/forwarddirection)

#### Enumeration Cases

- [case negativeZ](/documentation/realitykit/entity/forwarddirection/negativez)
- [case positiveZ](/documentation/realitykit/entity/forwarddirection/positivez)

### Relating entities

- [var parameters: Entity.ParameterSet](/documentation/realitykit/entity/parameters)
- [Entity.ChildCollection](/documentation/realitykit/entity/childcollection)

#### Accessing collection members

- [subscript(Int) -> Entity](/documentation/realitykit/entity/childcollection/subscript(_:))

#### Adding entities

- [func append<S>(contentsOf: S, preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/append(contentsof:preservingworldtransforms:)-7g61)
- [func append(Entity, preservingWorldTransform: Bool)](/documentation/realitykit/entity/childcollection/append(_:preservingworldtransform:))
- [func append(contentsOf: [Entity], preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/append(contentsof:preservingworldtransforms:)-7p4hd)

#### Removing entities

- [func remove(Entity, preservingWorldTransform: Bool)](/documentation/realitykit/entity/childcollection/remove(_:preservingworldtransform:))
- [func remove(at: Int, preservingWorldTransform: Bool)](/documentation/realitykit/entity/childcollection/remove(at:preservingworldtransform:))
- [func removeAll(preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/removeall(preservingworldtransforms:))
- [func removeAll(keepCapacity: Bool, preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/removeall(keepcapacity:preservingworldtransforms:))

#### Replacing entities

- [func replaceAll([Entity], preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/replaceall(_:preservingworldtransforms:)-4mgff)
- [func replaceAll<S>(S, preservingWorldTransforms: Bool)](/documentation/realitykit/entity/childcollection/replaceall(_:preservingworldtransforms:)-1vwk4)

#### Iterating over collection of entities

- [Entity.ChildCollection.IndexingIterator](/documentation/realitykit/entity/childcollection/indexingiterator)

##### Splitting and joining entities

- [Entity.ChildCollection.IndexingIterator.SubSequence](/documentation/realitykit/entity/childcollection/indexingiterator/subsequence)

#### Describing a collection

- [var description: String](/documentation/realitykit/entity/childcollection/description)

#### Manipulating indices

- [var startIndex: Int](/documentation/realitykit/entity/childcollection/startindex)
- [var endIndex: Int](/documentation/realitykit/entity/childcollection/endindex)
- [func index(after: Int) -> Int](/documentation/realitykit/entity/childcollection/index(after:))

#### Instance Methods

- [func append(contentsOf:preservingWorldTransforms:)](/documentation/realitykit/entity/childcollection/append(contentsof:preservingworldtransforms:))
- [func replaceAll(_:preservingWorldTransforms:)](/documentation/realitykit/entity/childcollection/replaceall(_:preservingworldtransforms:))

#### Default Implementations

- [CustomStringConvertible Implementations](/documentation/realitykit/entity/childcollection/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/realitykit/entity/childcollection/description)
- [EntityCollection Implementations](/documentation/realitykit/entity/childcollection/entitycollection-implementations)

##### Instance Methods

- [func append<S>(contentsOf: S)](/documentation/realitykit/entity/childcollection/append(contentsof:))
- [func remove(Entity)](/documentation/realitykit/entity/childcollection/remove(_:))
- [func remove(at: Int)](/documentation/realitykit/entity/childcollection/remove(at:))
- [func removeAll()](/documentation/realitykit/entity/childcollection/removeall())
- [func replaceAll<S>(S)](/documentation/realitykit/entity/childcollection/replaceall(_:))
- [HasHierarchy](/documentation/realitykit/hashierarchy)

#### Managing the parent

- [var parent: Entity?](/documentation/realitykit/hashierarchy/parent)
- [func setParent(Entity?, preservingWorldTransform: Bool)](/documentation/realitykit/hashierarchy/setparent(_:preservingworldtransform:))
- [func removeFromParent(preservingWorldTransform: Bool)](/documentation/realitykit/hashierarchy/removefromparent(preservingworldtransform:))

#### Managing children

- [var children: Entity.ChildCollection](/documentation/realitykit/hashierarchy/children)
- [func addChild(Entity, preservingWorldTransform: Bool)](/documentation/realitykit/hashierarchy/addchild(_:preservingworldtransform:))
- [func removeChild(Entity, preservingWorldTransform: Bool)](/documentation/realitykit/hashierarchy/removechild(_:preservingworldtransform:))

### Managing components

- [var components: Entity.ComponentSet](/documentation/realitykit/entity/components)
- [Entity.ComponentSet](/documentation/realitykit/entity/componentset)

#### Updating the set

- [func set<T>(T)](/documentation/realitykit/entity/componentset/set(_:)-8sii2)
- [func set([any Component])](/documentation/realitykit/entity/componentset/set(_:)-2qzsc)
- [func remove(any Component.Type)](/documentation/realitykit/entity/componentset/remove(_:))
- [func removeAll()](/documentation/realitykit/entity/componentset/removeall())

#### Accessing members

- [subscript<T>(T.Type) -> T?](/documentation/realitykit/entity/componentset/subscript(_:)-5wdsf)
- [subscript(any Component.Type) -> (any Component)?](/documentation/realitykit/entity/componentset/subscript(_:)-47rhg)

#### Checking for membership

- [func has(any Component.Type) -> Bool](/documentation/realitykit/entity/componentset/has(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/entity/componentset/count)

#### Instance Methods

- [func set(_:)](/documentation/realitykit/entity/componentset/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/entity/componentset/subscript(_:))

### Inspecting an entity

- [var scene: Scene?](/documentation/realitykit/entity/scene)
- [var name: String](/documentation/realitykit/entity/name)
- [func findEntity(named: String) -> Entity?](/documentation/realitykit/entity/findentity(named:))
- [var debugDescription: String](/documentation/realitykit/entity/debugdescription)

### Managing the entity’s state

- [var isEnabled: Bool](/documentation/realitykit/entity/isenabled)
- [var isEnabledInHierarchy: Bool](/documentation/realitykit/entity/isenabledinhierarchy)
- [var isActive: Bool](/documentation/realitykit/entity/isactive)
- [var isAnchored: Bool](/documentation/realitykit/entity/isanchored)

### Synchronizing entities with other devices

- [SynchronizationComponent](/documentation/realitykit/synchronizationcomponent)

#### Creating a synchronization component

- [init()](/documentation/realitykit/synchronizationcomponent/init())

#### Identifying a synchronization component

- [var identifier: UInt64](/documentation/realitykit/synchronizationcomponent/identifier)

#### Managing ownership

- [var isOwner: Bool](/documentation/realitykit/synchronizationcomponent/isowner)
- [var ownershipTransferMode: SynchronizationComponent.OwnershipTransferMode](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.property)

#### Operators

- [static func == (SynchronizationComponent, SynchronizationComponent) -> Bool](/documentation/realitykit/synchronizationcomponent/==(_:_:))

#### Enumerations

- [SynchronizationComponent.OwnershipTransferCompletionResult](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult)

##### Ownership transfer completion results

- [case granted](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/granted)
- [case timedOut](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/timedout)
- [SynchronizationComponent.OwnershipTransferMode](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum)

##### Ownership transfer modes

- [case autoAccept](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/autoaccept)
- [case manual](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/manual)

### Finding the nearest anchor

- [var anchor: (any HasAnchoring)?](/documentation/realitykit/entity/anchor)

### Creating a collision shape

- [func generateCollisionShapes(recursive: Bool)](/documentation/realitykit/entity/generatecollisionshapes(recursive:))
- [func generateCollisionShapes(recursive: Bool, static: Bool)](/documentation/realitykit/entity/generatecollisionshapes(recursive:static:))

### Animating an entity

- [var availableAnimations: [AnimationResource]](/documentation/realitykit/entity/availableanimations)
- [func playAnimation(AnimationResource, transitionDuration: TimeInterval, blendLayerOffset: Int, separateAnimatedValue: Bool, startsPaused: Bool, clock: CMClockOrTimebase?) -> AnimationPlaybackController](/documentation/realitykit/entity/playanimation(_:transitionduration:blendlayeroffset:separateanimatedvalue:startspaused:clock:))
- [func playAnimation(AnimationResource, transitionDuration: TimeInterval, blendLayerOffset: Int, separateAnimatedValue: Bool, startsPaused: Bool, clock: CMClockOrTimebase?, handoffType: AnimationHandoffType) -> AnimationPlaybackController](/documentation/realitykit/entity/playanimation(_:transitionduration:blendlayeroffset:separateanimatedvalue:startspaused:clock:handofftype:))
- [func playAnimation(AnimationResource, transitionDuration: TimeInterval, startsPaused: Bool) -> AnimationPlaybackController](/documentation/realitykit/entity/playanimation(_:transitionduration:startspaused:))
- [func stopAllAnimations(recursive: Bool)](/documentation/realitykit/entity/stopallanimations(recursive:))
- [var defaultAnimationClock: CMClockOrTimebase](/documentation/realitykit/entity/defaultanimationclock)
- [var parameters: Entity.ParameterSet](/documentation/realitykit/entity/parameters)
- [Entity.ParameterSet](/documentation/realitykit/entity/parameterset)

#### Subscripts

- [subscript<T>(String, T.Type) -> BindableValue<T>?](/documentation/realitykit/entity/parameterset/subscript(_:_:))
- [func playAnimation(named: String, transitionDuration: TimeInterval, startsPaused: Bool, recursive: Bool) -> AnimationPlaybackController](/documentation/realitykit/entity/playanimation(named:transitionduration:startspaused:recursive:))
- [var bindableValues: BindableValuesReference](/documentation/realitykit/entity/bindablevalues)
- [subscript(BindTarget.EntityPath) -> Entity?](/documentation/realitykit/entity/subscript(_:))

### Animating and controlling characters

- [var characterController: CharacterControllerComponent?](/documentation/realitykit/entity/charactercontroller)
- [var characterControllerState: CharacterControllerStateComponent?](/documentation/realitykit/entity/charactercontrollerstate)
- [func moveCharacter(by: SIMD3<Float>, deltaTime: Float, relativeTo: Entity?, collisionHandler: ((CharacterControllerComponent.Collision) -> Void)?) -> CharacterControllerComponent.CollisionFlags](/documentation/realitykit/entity/movecharacter(by:deltatime:relativeto:collisionhandler:))
- [func teleportCharacter(to: SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/entity/teleportcharacter(to:relativeto:))

### Playing audio

- [func playAudio(AudioResource) -> AudioPlaybackController](/documentation/realitykit/entity/playaudio(_:))
- [func playAudio(configuration: AudioGeneratorConfiguration, Audio.GeneratorRenderHandler) throws -> AudioGeneratorController](/documentation/realitykit/entity/playaudio(configuration:_:))
- [func prepareAudio(configuration: AudioGeneratorConfiguration, Audio.GeneratorRenderHandler) throws -> AudioGeneratorController](/documentation/realitykit/entity/prepareaudio(configuration:_:))
- [func prepareAudio(AudioResource) -> AudioPlaybackController](/documentation/realitykit/entity/prepareaudio(_:))
- [func stopAllAudio()](/documentation/realitykit/entity/stopallaudio())
- [var spatialAudio: SpatialAudioComponent?](/documentation/realitykit/entity/spatialaudio)
- [var ambientAudio: AmbientAudioComponent?](/documentation/realitykit/entity/ambientaudio)
- [var channelAudio: ChannelAudioComponent?](/documentation/realitykit/entity/channelaudio)

### Saving an entity and its descendants

- [func write(to: URL) async throws](/documentation/realitykit/entity/write(to:))

### Configuring accessibility features

- [Improving the Accessibility of RealityKit Apps](/documentation/realitykit/improving-the-accessibility-of-realitykit-apps)
- [var isAccessibilityElement: Bool](/documentation/realitykit/entity/isaccessibilityelement)
- [var accessibilityLabelKey: LocalizedStringResource?](/documentation/realitykit/entity/accessibilitylabelkey)
- [var accessibilityCustomActions: [LocalizedStringResource]](/documentation/realitykit/entity/accessibilitycustomactions)
- [var accessibilityCustomContent: [AccessibilityComponent.CustomContent]](/documentation/realitykit/entity/accessibilitycustomcontent)
- [var accessibilityCustomRotors: [AccessibilityComponent.RotorType]](/documentation/realitykit/entity/accessibilitycustomrotors)
- [var accessibilityLabelKey: LocalizedStringResource?](/documentation/realitykit/entity/accessibilitylabelkey)
- [var accessibilitySystemActions: AccessibilityComponent.SupportedActions](/documentation/realitykit/entity/accessibilitysystemactions)
- [var accessibilityTraits: UIAccessibilityTraits](/documentation/realitykit/entity/accessibilitytraits)
- [var accessibilityValue: LocalizedStringResource?](/documentation/realitykit/entity/accessibilityvalue)
- [var accessibilityDescription: String?](/documentation/realitykit/entity/accessibilitydescription)
- [var accessibilityLabel: String?](/documentation/realitykit/entity/accessibilitylabel)
- [var accessibilityDescription: String?](/documentation/realitykit/entity/accessibilitydescription)

### Structures

- [Entity.Observable](/documentation/realitykit/entity/observable-swift.struct)

#### Structures

- [Entity.Observable.Components](/documentation/realitykit/entity/observable-swift.struct/components-swift.struct)

##### Subscripts

- [subscript(_:)](/documentation/realitykit/entity/observable-swift.struct/components-swift.struct/subscript(_:))

#### Instance Properties

- [var children: Entity.ChildCollection](/documentation/realitykit/entity/observable-swift.struct/children)
- [var components: Entity.Observable.Components](/documentation/realitykit/entity/observable-swift.struct/components-swift.property)
- [var isEnabled: Bool](/documentation/realitykit/entity/observable-swift.struct/isenabled)
- [var name: String](/documentation/realitykit/entity/observable-swift.struct/name)
- [var orientation: simd_quatf](/documentation/realitykit/entity/observable-swift.struct/orientation)
- [var position: SIMD3<Float>](/documentation/realitykit/entity/observable-swift.struct/position)
- [var scale: SIMD3<Float>](/documentation/realitykit/entity/observable-swift.struct/scale)
- [var transform: Transform](/documentation/realitykit/entity/observable-swift.struct/transform)

### Initializers

- [convenience(components:)](/documentation/realitykit/entity/init(components:))
- [convenience init(from: Data, named: String?) async throws](/documentation/realitykit/entity/init(from:named:))

### Instance Properties

- [var observable: Entity.Observable](/documentation/realitykit/entity/observable-swift.property)
- [var pins: EntityGeometricPins](/documentation/realitykit/entity/pins)

### Instance Methods

- [func applyTapForBehaviors() -> Bool](/documentation/realitykit/entity/applytapforbehaviors())
- [func attach(GeometricPin?, to: GeometricPin)](/documentation/realitykit/entity/attach(_:to:))

### Type Methods

- [static func animate(Animation, body: () -> Void, completion: (() -> Void)?)](/documentation/realitykit/entity/animate(_:body:completion:))

### Default Implementations

- [CustomDebugStringConvertible Implementations](/documentation/realitykit/entity/customdebugstringconvertible-implementations)

#### Instance Properties

- [var debugDescription: String](/documentation/realitykit/entity/debugdescription)
- [Equatable Implementations](/documentation/realitykit/entity/equatable-implementations)

#### Operators

- [static func == (Entity, Entity) -> Bool](/documentation/realitykit/entity/==(_:_:))
- [Hashable Implementations](/documentation/realitykit/entity/hashable-implementations)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/entity/hash(into:))
- [Component](/documentation/realitykit/component)

### Registering a component type

- [static func registerComponent()](/documentation/realitykit/component/registercomponent())

## Presentation

- [Views and attachments](/documentation/realitykit/presentation-views-and-attachments)

### SwiftUI scene presentation

- [RealityView](/documentation/realitykit/realityview)

#### Creating a reality view for visionOS

- [init(make: (inout RealityViewContent) async -> Void, update: ((inout RealityViewContent) -> Void)?)](/documentation/realitykit/realityview/init(make:update:)-666xr)
- [init<P>(make: (inout RealityViewContent) async -> Void, update: ((inout RealityViewContent) -> Void)?, placeholder: () -> P)](/documentation/realitykit/realityview/init(make:update:placeholder:)-4c8yv)
- [init<A>(make: (inout RealityViewContent, RealityViewAttachments) async -> Void, update: ((inout RealityViewContent, RealityViewAttachments) -> Void)?, attachments: () -> A)](/documentation/realitykit/realityview/init(make:update:attachments:))
- [init<A, P>(make: (inout RealityViewContent, RealityViewAttachments) async -> Void, update: ((inout RealityViewContent, RealityViewAttachments) -> Void)?, placeholder: () -> P, attachments: () -> A)](/documentation/realitykit/realityview/init(make:update:placeholder:attachments:))

#### Creating a reality view for iOS and macOS

- [init(make: (inout RealityViewCameraContent) async -> Void, update: ((inout RealityViewCameraContent) -> Void)?)](/documentation/realitykit/realityview/init(make:update:)-234sv)
- [init<P>(make: (inout RealityViewCameraContent) async -> Void, update: ((inout RealityViewCameraContent) -> Void)?, placeholder: () -> P)](/documentation/realitykit/realityview/init(make:update:placeholder:)-4x7ds)

#### Inspecting the content within a reality view

- [RealityView.DefaultPlaceholder](/documentation/realitykit/realityview/defaultplaceholder)

#### Initializers

- [init(make:update:)](/documentation/realitykit/realityview/init(make:update:))
- [init(make:update:placeholder:)](/documentation/realitykit/realityview/init(make:update:placeholder:))
- [RealityViewContent](/documentation/realitykit/realityviewcontent)

#### Structures

- [RealityViewContent.Body](/documentation/realitykit/realityviewcontent/body)

#### Instance Methods

- [func animate(body: () -> Void, completion: (() -> Void)?)](/documentation/realitykit/realityviewcontent/animate(body:completion:))
- [func subscribe<E>(to: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityviewcontent/subscribe(to:on:componenttype:_:))
- [RealityViewCameraContent](/documentation/realitykit/realityviewcameracontent)

#### Structures

- [RealityViewCameraContent.Body](/documentation/realitykit/realityviewcameracontent/body)

#### Instance Properties

- [var audioListener: Entity?](/documentation/realitykit/realityviewcameracontent/audiolistener)
- [var camera: RealityViewCamera](/documentation/realitykit/realityviewcameracontent/camera)
- [var cameraTarget: Entity?](/documentation/realitykit/realityviewcameracontent/cameratarget)
- [var entities: RealityViewEntityCollection](/documentation/realitykit/realityviewcameracontent/entities)
- [var environment: RealityViewEnvironment](/documentation/realitykit/realityviewcameracontent/environment)
- [var renderingEffects: RealityViewRenderingEffects](/documentation/realitykit/realityviewcameracontent/renderingeffects)

#### Instance Methods

- [func animate(body: () -> Void, completion: (() -> Void)?)](/documentation/realitykit/realityviewcameracontent/animate(body:completion:))
- [func subscribe<E>(to: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityviewcameracontent/subscribe(to:on:componenttype:_:))
- [RealityViewContentProtocol](/documentation/realitykit/realityviewcontentprotocol)

#### Managing view content

- [func add(Entity)](/documentation/realitykit/realityviewcontentprotocol/add(_:))
- [func remove(Entity)](/documentation/realitykit/realityviewcontentprotocol/remove(_:))
- [Entities](/documentation/realitykit/realityviewcontentprotocol/entities-swift.associatedtype)
- [var entities: Self.Entities](/documentation/realitykit/realityviewcontentprotocol/entities-swift.property)

#### Handling subscriptions

- [func subscribe<E>(to: E.Type, on: (any EventSource)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityviewcontentprotocol/subscribe(to:on:_:))
- [func subscribe<E>(to: E.Type, componentType: (any Component.Type)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityviewcontentprotocol/subscribe(to:componenttype:_:))
- [func subscribe<E>(to: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityviewcontentprotocol/subscribe(to:on:componenttype:_:))
- [RealityViewDefaultPlaceholder](/documentation/realitykit/realityviewdefaultplaceholder)
- [RealityViewEntityCollection](/documentation/realitykit/realityviewentitycollection)
- [RealityViewLayoutOption](/documentation/realitykit/realityviewlayoutoption)

#### Type Properties

- [static let centered: RealityViewLayoutOption](/documentation/realitykit/realityviewlayoutoption/centered)
- [static let fixedSize: RealityViewLayoutOption](/documentation/realitykit/realityviewlayoutoption/fixedsize)
- [static let flexible: RealityViewLayoutOption](/documentation/realitykit/realityviewlayoutoption/flexible)
- [EntityCollection](/documentation/realitykit/entitycollection)

#### Instance Methods

- [func append(Entity)](/documentation/realitykit/entitycollection/append(_:))
- [func append<S>(contentsOf: S)](/documentation/realitykit/entitycollection/append(contentsof:))
- [func insert(Entity, beforeIndex: Int)](/documentation/realitykit/entitycollection/insert(_:beforeindex:))
- [func insert<S>(contentsOf: S, beforeIndex: Int)](/documentation/realitykit/entitycollection/insert(contentsof:beforeindex:))
- [func remove(Entity)](/documentation/realitykit/entitycollection/remove(_:))
- [func remove(at: Int)](/documentation/realitykit/entitycollection/remove(at:))
- [func removeAll()](/documentation/realitykit/entitycollection/removeall())
- [func removeAll(where: (Entity) throws -> Bool) rethrows](/documentation/realitykit/entitycollection/removeall(where:))
- [func replaceAll<S>(S)](/documentation/realitykit/entitycollection/replaceall(_:))

### SwiftUI 3D model presentation

- [Model3D](/documentation/realitykit/model3d)

#### Creating a Model3D

- [init(named: String, bundle: Bundle?)](/documentation/realitykit/model3d/init(named:bundle:))
- [init<Model, Placeholder>(named: String, bundle: Bundle?, content: (ResolvedModel3D) -> Model, placeholder: () -> Placeholder)](/documentation/realitykit/model3d/init(named:bundle:content:placeholder:))
- [init(named: String, bundle: Bundle?, transaction: Transaction, content: (Model3DPhase) -> Content)](/documentation/realitykit/model3d/init(named:bundle:transaction:content:))
- [init(url: URL)](/documentation/realitykit/model3d/init(url:))
- [init<Model, Placeholder>(url: URL, content: (ResolvedModel3D) -> Model, placeholder: () -> Placeholder)](/documentation/realitykit/model3d/init(url:content:placeholder:))
- [init(url: URL, transaction: Transaction, content: (Model3DPhase) -> Content)](/documentation/realitykit/model3d/init(url:transaction:content:))

#### Accessing content

- [init<Model, Placeholder>(named: String, bundle: Bundle?, content: (ResolvedModel3D) -> Model, placeholder: () -> Placeholder)](/documentation/realitykit/model3d/init(named:bundle:content:placeholder:))
- [init<Model, Placeholder>(url: URL, content: (ResolvedModel3D) -> Model, placeholder: () -> Placeholder)](/documentation/realitykit/model3d/init(url:content:placeholder:))

#### Initializers

- [init(asset: Model3DAsset)](/documentation/realitykit/model3d/init(asset:))
- [init<Model>(asset: Model3DAsset, content: (ResolvedModel3D) -> Model)](/documentation/realitykit/model3d/init(asset:content:))
- [init(from: Entity.ConfigurationCatalog, configurations: [String : String]?)](/documentation/realitykit/model3d/init(from:configurations:))
- [init<Model, Placeholder>(from: Entity.ConfigurationCatalog, configurations: [String : String]?, content: (ResolvedModel3D) -> Model, placeholder: () -> Placeholder)](/documentation/realitykit/model3d/init(from:configurations:content:placeholder:))
- [init(from: Entity.ConfigurationCatalog, configurations: [String : String]?, transaction: Transaction, content: (Model3DPhase) -> Content)](/documentation/realitykit/model3d/init(from:configurations:transaction:content:))
- [Model3DPhase](/documentation/realitykit/model3dphase)

#### Accessing the model

- [var model: ResolvedModel3D?](/documentation/realitykit/model3dphase/model)
- [var error: (any Error)?](/documentation/realitykit/model3dphase/error)

#### Obtaining the result

- [case empty](/documentation/realitykit/model3dphase/empty)
- [case success(ResolvedModel3D)](/documentation/realitykit/model3dphase/success(_:))
- [case failure(any Error)](/documentation/realitykit/model3dphase/failure(_:))
- [ResolvedModel3D](/documentation/realitykit/resolvedmodel3d)

#### Instance Methods

- [func resizable(Bool) -> ResolvedModel3D](/documentation/realitykit/resolvedmodel3d/resizable(_:))
- [Model3DPlaceholderContent](/documentation/realitykit/model3dplaceholdercontent)
- [Model3DAsset](/documentation/realitykit/model3dasset)

#### Structures

- [Model3DAsset.EntityAnimation](/documentation/realitykit/model3dasset/entityanimation)

##### Instance Properties

- [var path: String](/documentation/realitykit/model3dasset/entityanimation/path)

#### Initializers

- [init(named: String, in: Bundle?) async throws](/documentation/realitykit/model3dasset/init(named:in:))
- [init(url: URL) async throws](/documentation/realitykit/model3dasset/init(url:))

#### Instance Properties

- [var animationPlaybackController: AnimationPlaybackController?](/documentation/realitykit/model3dasset/animationplaybackcontroller)
- [var availableAnimations: [Model3DAsset.EntityAnimation]](/documentation/realitykit/model3dasset/availableanimations)
- [var selectedAnimation: Model3DAsset.EntityAnimation?](/documentation/realitykit/model3dasset/selectedanimation)

### Metal workflow rendering

- [RealityRenderer](/documentation/realitykit/realityrenderer)

#### Structures

- [RealityRenderer.CameraOutput](/documentation/realitykit/realityrenderer/cameraoutput)

##### Structures

- [RealityRenderer.CameraOutput.Descriptor](/documentation/realitykit/realityrenderer/cameraoutput/descriptor)

###### Instance Properties

- [var colorTextures: [any MTLTexture]](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/colortextures)
- [var viewports: [RealityRenderer.CameraOutput.RelativeViewport]](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/viewports)

###### Type Methods

- [static func singleProjection(colorTexture: any MTLTexture) -> RealityRenderer.CameraOutput.Descriptor](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/singleprojection(colortexture:))
- [RealityRenderer.CameraOutput.RelativeViewport](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport)

###### Initializers

- [init(originX: Double, originY: Double, width: Double, height: Double)](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/init(originx:originy:width:height:))

###### Instance Properties

- [var height: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/height)
- [var originX: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/originx)
- [var originY: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/originy)
- [var width: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/width)

##### Initializers

- [init(RealityRenderer.CameraOutput.Descriptor) throws](/documentation/realitykit/realityrenderer/cameraoutput/init(_:))

##### Instance Properties

- [var colorTextures: [any MTLTexture]](/documentation/realitykit/realityrenderer/cameraoutput/colortextures)
- [var viewports: [RealityRenderer.CameraOutput.RelativeViewport]](/documentation/realitykit/realityrenderer/cameraoutput/viewports)
- [RealityRenderer.CameraSettings](/documentation/realitykit/realityrenderer/camerasettings-swift.struct)

##### Structures

- [RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct)

###### Type Methods

- [static func color(CGColor) -> RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct/color(_:))
- [static func outputTexture() -> RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct/outputtexture())

##### Instance Properties

- [var antialiasing: AntialiasingMode](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/antialiasing)
- [var colorBackground: RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.property)
- [var isToneMappingEnabled: Bool](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/istonemappingenabled)
- [RealityRenderer.EntityCollection](/documentation/realitykit/realityrenderer/entitycollection)
- [RealityRenderer.ImageBasedLight](/documentation/realitykit/realityrenderer/imagebasedlight)

##### Instance Properties

- [var intensityExponent: Float](/documentation/realitykit/realityrenderer/imagebasedlight/intensityexponent)
- [var resource: EnvironmentResource?](/documentation/realitykit/realityrenderer/imagebasedlight/resource)
- [RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction)

##### Instance Properties

- [let event: any MTLEvent](/documentation/realitykit/realityrenderer/metaleventaction/event)
- [let value: UInt64](/documentation/realitykit/realityrenderer/metaleventaction/value)

##### Type Methods

- [static func signal(any MTLEvent, value: UInt64) -> RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction/signal(_:value:))
- [static func wait(for: any MTLEvent, value: UInt64) -> RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction/wait(for:value:))

#### Initializers

- [init() throws](/documentation/realitykit/realityrenderer/init())

#### Instance Properties

- [var activeCamera: Entity?](/documentation/realitykit/realityrenderer/activecamera)
- [var cameraSettings: RealityRenderer.CameraSettings](/documentation/realitykit/realityrenderer/camerasettings-swift.property)
- [var entities: RealityRenderer.EntityCollection](/documentation/realitykit/realityrenderer/entities)
- [var extendedDynamicRangeHeadroom: Float](/documentation/realitykit/realityrenderer/extendeddynamicrangeheadroom)
- [var extendedDynamicRangeOutput: Bool](/documentation/realitykit/realityrenderer/extendeddynamicrangeoutput)
- [var lighting: RealityRenderer.ImageBasedLight](/documentation/realitykit/realityrenderer/lighting)

#### Instance Methods

- [func subscribe<E>(to: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?, (E) -> Void) -> EventSubscription](/documentation/realitykit/realityrenderer/subscribe(to:on:componenttype:_:))
- [func update(TimeInterval) throws](/documentation/realitykit/realityrenderer/update(_:))
- [func updateAndRender(deltaTime: TimeInterval, cameraOutput: RealityRenderer.CameraOutput, whenScheduled: ((RealityRenderer) -> Void)?, onComplete: ((RealityRenderer) -> Void)?, actionsBeforeRender: [RealityRenderer.MetalEventAction], actionsAfterRender: [RealityRenderer.MetalEventAction]) throws](/documentation/realitykit/realityrenderer/updateandrender(deltatime:cameraoutput:whenscheduled:oncomplete:actionsbeforerender:actionsafterrender:))
- [RealityRenderer.CameraSettings](/documentation/realitykit/realityrenderer/camerasettings-swift.struct)

#### Structures

- [RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct)

##### Type Methods

- [static func color(CGColor) -> RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct/color(_:))
- [static func outputTexture() -> RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.struct/outputtexture())

#### Instance Properties

- [var antialiasing: AntialiasingMode](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/antialiasing)
- [var colorBackground: RealityRenderer.CameraSettings.ColorBackground](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/colorbackground-swift.property)
- [var isToneMappingEnabled: Bool](/documentation/realitykit/realityrenderer/camerasettings-swift.struct/istonemappingenabled)
- [RealityRenderer.CameraOutput](/documentation/realitykit/realityrenderer/cameraoutput)

#### Structures

- [RealityRenderer.CameraOutput.Descriptor](/documentation/realitykit/realityrenderer/cameraoutput/descriptor)

##### Instance Properties

- [var colorTextures: [any MTLTexture]](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/colortextures)
- [var viewports: [RealityRenderer.CameraOutput.RelativeViewport]](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/viewports)

##### Type Methods

- [static func singleProjection(colorTexture: any MTLTexture) -> RealityRenderer.CameraOutput.Descriptor](/documentation/realitykit/realityrenderer/cameraoutput/descriptor/singleprojection(colortexture:))
- [RealityRenderer.CameraOutput.RelativeViewport](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport)

##### Initializers

- [init(originX: Double, originY: Double, width: Double, height: Double)](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/init(originx:originy:width:height:))

##### Instance Properties

- [var height: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/height)
- [var originX: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/originx)
- [var originY: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/originy)
- [var width: Double](/documentation/realitykit/realityrenderer/cameraoutput/relativeviewport/width)

#### Initializers

- [init(RealityRenderer.CameraOutput.Descriptor) throws](/documentation/realitykit/realityrenderer/cameraoutput/init(_:))

#### Instance Properties

- [var colorTextures: [any MTLTexture]](/documentation/realitykit/realityrenderer/cameraoutput/colortextures)
- [var viewports: [RealityRenderer.CameraOutput.RelativeViewport]](/documentation/realitykit/realityrenderer/cameraoutput/viewports)
- [RealityRenderer.ImageBasedLight](/documentation/realitykit/realityrenderer/imagebasedlight)

#### Instance Properties

- [var intensityExponent: Float](/documentation/realitykit/realityrenderer/imagebasedlight/intensityexponent)
- [var resource: EnvironmentResource?](/documentation/realitykit/realityrenderer/imagebasedlight/resource)
- [RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction)

#### Instance Properties

- [let event: any MTLEvent](/documentation/realitykit/realityrenderer/metaleventaction/event)
- [let value: UInt64](/documentation/realitykit/realityrenderer/metaleventaction/value)

#### Type Methods

- [static func signal(any MTLEvent, value: UInt64) -> RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction/signal(_:value:))
- [static func wait(for: any MTLEvent, value: UInt64) -> RealityRenderer.MetalEventAction](/documentation/realitykit/realityrenderer/metaleventaction/wait(for:value:))
- [RealityRenderer.EntityCollection](/documentation/realitykit/realityrenderer/entitycollection)

### SwiftUI view attachments

- [RealityViewAttachmentBuilderContent](/documentation/realitykit/realityviewattachmentbuildercontent)
- [Attachment](/documentation/realitykit/attachment)

#### Initializers

- [init(id: AnyHashable, () -> Content)](/documentation/realitykit/attachment/init(id:_:))

#### Instance Properties

- [var content: Content](/documentation/realitykit/attachment/content)
- [var id: AnyHashable](/documentation/realitykit/attachment/id)
- [RealityViewAttachments](/documentation/realitykit/realityviewattachments)

#### Instance Methods

- [func entity(for: some Hashable) -> ViewAttachmentEntity?](/documentation/realitykit/realityviewattachments/entity(for:))
- [ViewAttachmentEntity](/documentation/realitykit/viewattachmententity)

#### Instance Properties

- [var attachment: ViewAttachmentComponent](/documentation/realitykit/viewattachmententity/attachment)
- [ViewAttachmentComponent](/documentation/realitykit/viewattachmentcomponent)

#### Initializers

- [init<Content>(rootView: Content)](/documentation/realitykit/viewattachmentcomponent/init(rootview:))

#### Instance Properties

- [var bounds: BoundingBox](/documentation/realitykit/viewattachmentcomponent/bounds)
- [var id: AnyHashable](/documentation/realitykit/viewattachmentcomponent/id)
- [PresentationComponent](/documentation/realitykit/presentationcomponent)

#### Structures

- [PresentationComponent.Configuration](/documentation/realitykit/presentationcomponent/configuration)

##### Type Methods

- [static func popover(arrowEdge: Edge?) -> PresentationComponent.Configuration](/documentation/realitykit/presentationcomponent/configuration/popover(arrowedge:))

#### Initializers

- [init<Content>(configuration: PresentationComponent.Configuration, content: Content)](/documentation/realitykit/presentationcomponent/init(configuration:content:))
- [init<Content>(isPresented: Binding<Bool>, configuration: PresentationComponent.Configuration, content: Content)](/documentation/realitykit/presentationcomponent/init(ispresented:configuration:content:))

#### Instance Properties

- [var isPresented: Bool](/documentation/realitykit/presentationcomponent/ispresented)
- [TextComponent](/documentation/realitykit/textcomponent)

#### Initializers

- [init()](/documentation/realitykit/textcomponent/init())

#### Instance Properties

- [var backgroundColor: CGColor?](/documentation/realitykit/textcomponent/backgroundcolor)
- [var cornerRadius: Float](/documentation/realitykit/textcomponent/cornerradius)
- [var edgeInsets: TextComponent.EdgeInsets](/documentation/realitykit/textcomponent/edgeinsets-3n3rn)
- [var edgeInsets: TextComponent.EdgeInsets](/documentation/realitykit/textcomponent/edgeinsets-49dib)
- [var size: CGSize](/documentation/realitykit/textcomponent/size)
- [var text: AttributedString?](/documentation/realitykit/textcomponent/text)

#### Type Aliases

- [TextComponent.EdgeInsets](/documentation/realitykit/textcomponent/edgeinsets-swift.typealias)

### Visual environment adjustments

- [RealityViewEnvironment](/documentation/realitykit/realityviewenvironment)

#### Setting the environment background

- [static var `default`: RealityViewEnvironment](/documentation/realitykit/realityviewenvironment/default)
- [static func skybox(EnvironmentResource) -> RealityViewEnvironment](/documentation/realitykit/realityviewenvironment/skybox(_:))
- [RealityViewRenderingEffects](/documentation/realitykit/realityviewrenderingeffects)

#### Instance Properties

- [var antialiasing: AntialiasingMode](/documentation/realitykit/realityviewrenderingeffects/antialiasing)
- [var cameraGrain: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffects/cameragrain)
- [var customPostProcessing: RealityViewPostProcessEffect](/documentation/realitykit/realityviewrenderingeffects/custompostprocessing)
- [var depthOfField: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffects/depthoffield)
- [var dynamicRange: RealityViewDynamicRange](/documentation/realitykit/realityviewrenderingeffects/dynamicrange)
- [var motionBlur: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffects/motionblur)
- [RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffectmode)

#### Setting the rendering effect mode

- [static var `default`: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffectmode/default)
- [static var enabled: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffectmode/enabled)
- [static var disabled: RealityViewRenderingEffectMode](/documentation/realitykit/realityviewrenderingeffectmode/disabled)
- [RealityViewDynamicRange](/documentation/realitykit/realityviewdynamicrange)

#### Setting the dynamic range

- [static var `default`: RealityViewDynamicRange](/documentation/realitykit/realityviewdynamicrange/default)
- [static var standard: RealityViewDynamicRange](/documentation/realitykit/realityviewdynamicrange/standard)
- [AntialiasingMode](/documentation/realitykit/antialiasingmode)

#### Setting the antialiasing mode

- [case multisample4X](/documentation/realitykit/antialiasingmode/multisample4x)
- [case none](/documentation/realitykit/antialiasingmode/none)
- [RealityViewPostProcessEffect](/documentation/realitykit/realityviewpostprocesseffect)

#### Type Properties

- [static var none: RealityViewPostProcessEffect](/documentation/realitykit/realityviewpostprocesseffect/none)

#### Type Methods

- [static func effect(some PostProcessEffect) -> RealityViewPostProcessEffect](/documentation/realitykit/realityviewpostprocesseffect/effect(_:))
- [PostProcessEffectContext](/documentation/realitykit/postprocesseffectcontext)

#### Instance Properties

- [var commandBuffer: CommandBuffer](/documentation/realitykit/postprocesseffectcontext/commandbuffer)
- [var device: any MTLDevice](/documentation/realitykit/postprocesseffectcontext/device)
- [var projection: float4x4](/documentation/realitykit/postprocesseffectcontext/projection)
- [var sourceColorTexture: any MTLTexture](/documentation/realitykit/postprocesseffectcontext/sourcecolortexture)
- [var sourceDepthTexture: any MTLTexture](/documentation/realitykit/postprocesseffectcontext/sourcedepthtexture)
- [var targetColorTexture: any MTLTexture](/documentation/realitykit/postprocesseffectcontext/targetcolortexture)
- [var time: TimeInterval](/documentation/realitykit/postprocesseffectcontext/time)
- [ARView.Environment](/documentation/realitykit/arview/environment-swift.struct)

#### Creating an environment

- [init(background: ARView.Environment.Background, lighting: ARView.Environment.ImageBasedLight, reverb: ARView.Environment.Reverb)](/documentation/realitykit/arview/environment-swift.struct/init(background:lighting:reverb:))

#### Setting a background

- [var background: ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.property)
- [ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct)

##### Backgrounds

- [static func cameraFeed(exposureCompensation: Float) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/camerafeed(exposurecompensation:))
- [static func color(ARView.Environment.Color) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:)-97jik)
- [static func color(ARView.Environment.Color) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:)-5hh3f)
- [static func skybox(EnvironmentResource) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/skybox(_:))

##### Type Methods

- [static color(_:)](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:))

#### Lighting the environment

- [var lighting: ARView.Environment.ImageBasedLight](/documentation/realitykit/arview/environment-swift.struct/lighting)
- [ARView.Environment.ImageBasedLight](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight)

##### Resources

- [var resource: EnvironmentResource?](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight/resource)

##### Modulating intensity

- [var intensityExponent: Float](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight/intensityexponent)

#### Defining acoustic properties

- [var reverb: ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.property)
- [ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum)

##### Available reverb settings

- [case noReverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/noreverb)
- [case preset(ARView.Environment.Reverb.Preset)](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset(_:))

##### Reverb presets

- [static var automatic: ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/automatic)
- [ARView.Environment.Reverb.Preset](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset)

###### Reverb presets

- [case cathedral](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/cathedral)
- [case largeHall](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/largehall)
- [case largeRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/largeroom)
- [case mediumHall](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/mediumhall)
- [case mediumRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/mediumroom)
- [case smallRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/smallroom)

#### Structures

- [ARView.Environment.SceneUnderstanding](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct)

##### Structures

- [ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct)

###### Type Properties

- [static let collision: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/collision)
- [static let `default`: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/default)
- [static let occlusion: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/occlusion)
- [static let physics: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/physics)
- [static let receivesLighting: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/receiveslighting)

##### Instance Properties

- [var options: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.property)

#### Instance Properties

- [var sceneUnderstanding: ARView.Environment.SceneUnderstanding](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.property)

#### Type Aliases

- [ARView.Environment.Color](/documentation/realitykit/arview/environment-swift.struct/color)
- [ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct)

#### Disabling rendering effects

- [static let disableCameraGrain: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablecameragrain)
- [static let disableHDR: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablehdr)
- [static let disableGroundingShadows: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablegroundingshadows)
- [static let disableMotionBlur: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablemotionblur)
- [static let disableDepthOfField: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disabledepthoffield)
- [static let disableFaceMesh: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablefacemesh)
- [static let disablePersonOcclusion: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablepersonocclusion)
- [static let disableAREnvironmentLighting: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablearenvironmentlighting)
- [static let disableFaceOcclusions: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablefaceocclusions)
- [static let disableAutomaticLighting: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disableautomaticlighting)

### Postprocessing

- [Postprocessing effects](/documentation/realitykit/postprocessing-effects)

#### Core Image effects

- [Applying core image filters as a postprocess effect](/documentation/realitykit/applying-core-image-filters-as-a-postprocess-effect)

#### Metal effects

- [Using Metal performance shaders to create custom postprocess effects](/documentation/realitykit/using-metal-performance-shaders-to-create-custom-postprocess-effects)
- [Implementing special rendering effects with RealityKit postprocessing](/documentation/realitykit/implementing-special-rendering-effects-with-realitykit-postprocessing)
- [Checking the pixel format of a postprocess effect’s output texture](/documentation/realitykit/checking-the-pixel-format-of-a-postprocess-effect-s-output-texture)
- [Passing Structured Data to a Metal Compute Function](/documentation/realitykit/passing-structured-data-to-a-metal-compute-function)
- [Implementing postprocess effects using Metal compute functions](/documentation/realitykit/implementing-postprocess-effects-using-metal-compute-functions)
- [ARView.PostProcessContext](/documentation/realitykit/arview/postprocesscontext)

#### Initializers

- [init(any MTLDevice, any MTLCommandBuffer, any MTLTexture, any MTLTexture, any MTLTexture, float4x4, TimeInterval)](/documentation/realitykit/arview/postprocesscontext/init(_:_:_:_:_:_:_:))

#### Instance Properties

- [var commandBuffer: any MTLCommandBuffer](/documentation/realitykit/arview/postprocesscontext/commandbuffer)
- [var device: any MTLDevice](/documentation/realitykit/arview/postprocesscontext/device)
- [var projection: float4x4](/documentation/realitykit/arview/postprocesscontext/projection)
- [var sourceColorTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/sourcecolortexture)
- [var sourceDepthTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/sourcedepthtexture)
- [var targetColorTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/targetcolortexture)
- [var time: TimeInterval](/documentation/realitykit/arview/postprocesscontext/time)
- [ARView.RenderCallbacks](/documentation/realitykit/arview/rendercallbacks-swift.struct)

#### Creating a callback object

- [init()](/documentation/realitykit/arview/rendercallbacks-swift.struct/init())

#### Register callback closures

- [var prepareWithDevice: ((any MTLDevice) -> Void)?](/documentation/realitykit/arview/rendercallbacks-swift.struct/preparewithdevice)
- [var postProcess: ((ARView.PostProcessContext) -> Void)?](/documentation/realitykit/arview/rendercallbacks-swift.struct/postprocess)
- [PostProcessEffect](/documentation/realitykit/postprocesseffect)

#### Instance Methods

- [func postProcess(context: borrowing PostProcessEffectContext<any MTLCommandBuffer>)](/documentation/realitykit/postprocesseffect/postprocess(context:))
- [func prepare(for: any MTLDevice)](/documentation/realitykit/postprocesseffect/prepare(for:))

### Coordinate space conversions

- [RealityCoordinateSpaceConverting](/documentation/realitykit/realitycoordinatespaceconverting)

#### Instance Methods

- [func convert(_:from:to:)](/documentation/realitykit/realitycoordinatespaceconverting/convert(_:from:to:))
- [func convert(boundingBox: BoundingBox, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> Rect3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(boundingbox:from:to:))
- [func convert(point: SIMD3<Float>, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> Point3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(point:from:to:))
- [func convert(rotation: simd_quatf, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> Rotation3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(rotation:from:to:))
- [func convert(size: SIMD3<Float>, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> Size3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(size:from:to:))
- [func convert(transform: Transform, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> AffineTransform3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(transform:from:to:))
- [func convert(vector: SIMD3<Float>, from: some RealityCoordinateSpace, to: some CoordinateSpaceProtocol) -> Vector3D](/documentation/realitykit/realitycoordinatespaceconverting/convert(vector:from:to:))
- [func transform(from:to:)](/documentation/realitykit/realitycoordinatespaceconverting/transform(from:to:))
- [SceneRealityCoordinateSpace](/documentation/realitykit/scenerealitycoordinatespace)

#### Initializers

- [init()](/documentation/realitykit/scenerealitycoordinatespace/init())
- [CameraRealityCoordinateSpace](/documentation/realitykit/camerarealitycoordinatespace)

#### Initializers

- [init()](/documentation/realitykit/camerarealitycoordinatespace/init())
- [RealityCoordinateSpace](/documentation/realitykit/realitycoordinatespace)

#### Type Properties

- [static var camera: CameraRealityCoordinateSpace](/documentation/realitykit/realitycoordinatespace/camera)
- [static var scene: SceneRealityCoordinateSpace](/documentation/realitykit/realitycoordinatespace/scene)
- [RealityCoordinateSpaceProjecting](/documentation/realitykit/realitycoordinatespaceprojecting)

#### Instance Methods

- [func entities(at: CGPoint, in: some CoordinateSpaceProtocol) -> [Entity]](/documentation/realitykit/realitycoordinatespaceprojecting/entities(at:in:))
- [func entity(at: CGPoint, in: some CoordinateSpaceProtocol) -> Entity?](/documentation/realitykit/realitycoordinatespaceprojecting/entity(at:in:))
- [func hitTest(point: CGPoint, in: some CoordinateSpaceProtocol, query: CollisionCastQueryType, mask: CollisionGroup) -> [CollisionCastHit]](/documentation/realitykit/realitycoordinatespaceprojecting/hittest(point:in:query:mask:))
- [func project(point: SIMD3<Float>, to: some CoordinateSpaceProtocol) -> CGPoint?](/documentation/realitykit/realitycoordinatespaceprojecting/project(point:to:))
- [func ray(through: CGPoint, in: some CoordinateSpaceProtocol, to: some RealityCoordinateSpace) -> (origin: SIMD3<Float>, direction: SIMD3<Float>)?](/documentation/realitykit/realitycoordinatespaceprojecting/ray(through:in:to:))
- [func unproject(CGPoint, from: some CoordinateSpaceProtocol, to: some RealityCoordinateSpace, ontoPlane: float4x4) -> SIMD3<Float>?](/documentation/realitykit/realitycoordinatespaceprojecting/unproject(_:from:to:ontoplane:))

### Camera mode settings

- [RealityViewCamera](/documentation/realitykit/realityviewcamera)

#### Type Properties

- [static var spatialTracking: RealityViewCamera](/documentation/realitykit/realityviewcamera/spatialtracking)
- [static var virtual: RealityViewCamera](/documentation/realitykit/realityviewcamera/virtual)
- [CameraControls](/documentation/realitykit/cameracontrols)

#### Type Properties

- [static var dolly: CameraControls](/documentation/realitykit/cameracontrols/dolly)
- [static var none: CameraControls](/documentation/realitykit/cameracontrols/none)
- [static var orbit: CameraControls](/documentation/realitykit/cameracontrols/orbit)
- [static var pan: CameraControls](/documentation/realitykit/cameracontrols/pan)
- [static var tilt: CameraControls](/documentation/realitykit/cameracontrols/tilt)
- [ARView.CameraMode](/documentation/realitykit/arview/cameramode-swift.enum)

#### Setting the camera mode

- [case ar](/documentation/realitykit/arview/cameramode-swift.enum/ar)
- [case nonAR](/documentation/realitykit/arview/cameramode-swift.enum/nonar)

### Attachment types

- [AttachmentContentBuilder](/documentation/realitykit/attachmentcontentbuilder)

#### Type Methods

- [static func buildBlock() -> EmptyAttachmentContent](/documentation/realitykit/attachmentcontentbuilder/buildblock())
- [static buildBlock(_:)](/documentation/realitykit/attachmentcontentbuilder/buildblock(_:))
- [static func buildEither<TrueContent, FalseContent>(first: TrueContent) -> ConditionalAttachmentContent<TrueContent, FalseContent>](/documentation/realitykit/attachmentcontentbuilder/buildeither(first:))
- [static func buildEither<TrueContent, FalseContent>(second: FalseContent) -> ConditionalAttachmentContent<TrueContent, FalseContent>](/documentation/realitykit/attachmentcontentbuilder/buildeither(second:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/realitykit/attachmentcontentbuilder/buildexpression(_:))
- [static func buildIf<Content>(Content?) -> Content?](/documentation/realitykit/attachmentcontentbuilder/buildif(_:))
- [static func buildLimitedAvailability(any AttachmentContent) -> some AttachmentContent](/documentation/realitykit/attachmentcontentbuilder/buildlimitedavailability(_:))
- [AttachmentContent](/documentation/realitykit/attachmentcontent)

#### Associated Types

- [Body](/documentation/realitykit/attachmentcontent/body-swift.associatedtype)

#### Instance Properties

- [var body: Self.Body](/documentation/realitykit/attachmentcontent/body-swift.property)
- [TuplePackAttachmentContent](/documentation/realitykit/tuplepackattachmentcontent)
- [ConditionalAttachmentContent](/documentation/realitykit/conditionalattachmentcontent)
- [EmptyAttachmentContent](/documentation/realitykit/emptyattachmentcontent)

#### Initializers

- [init()](/documentation/realitykit/emptyattachmentcontent/init())
- [TupleAttachmentContent](/documentation/realitykit/tupleattachmentcontent)
- [AnyAttachmentContent](/documentation/realitykit/anyattachmentcontent)

#### Initializers

- [init<Content>(Content)](/documentation/realitykit/anyattachmentcontent/init(_:))

### UIKit and AppKit presentation

- [ARView](/documentation/realitykit/arview)

#### Creating a view

- [init(frame: CGRect)](/documentation/realitykit/arview/init(frame:))
- [init(frame: CGRect, cameraMode: ARView.CameraMode, automaticallyConfigureSession: Bool)](/documentation/realitykit/arview/init(frame:cameramode:automaticallyconfiguresession:))
- [init?(coder: NSCoder)](/documentation/realitykit/arview/init(coder:))
- [convenience init(frame: CGRect, cameraMode: ARView.CameraMode)](/documentation/realitykit/arview/init(frame:cameramode:))

#### Working with the scene

- [var scene: Scene](/documentation/realitykit/arview/scene)

#### Configuring the AR session

- [var session: ARSession](/documentation/realitykit/arview/session)
- [var automaticallyConfigureSession: Bool](/documentation/realitykit/arview/automaticallyconfiguresession)
- [var renderOptions: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.property)
- [var renderCallbacks: ARView.RenderCallbacks](/documentation/realitykit/arview/rendercallbacks-swift.property)

#### Providing environmental context

- [var environment: ARView.Environment](/documentation/realitykit/arview/environment-swift.property)
- [var physicsOrigin: Entity?](/documentation/realitykit/arview/physicsorigin)
- [var audioListener: Entity?](/documentation/realitykit/arview/audiolistener)

#### Managing the camera

- [var cameraMode: ARView.CameraMode](/documentation/realitykit/arview/cameramode-swift.property)
- [var cameraTransform: Transform](/documentation/realitykit/arview/cameratransform)

#### Finding entities at a point in the view

- [func entity(at: CGPoint) -> Entity?](/documentation/realitykit/arview/entity(at:))
- [func entities(at: CGPoint) -> [Entity]](/documentation/realitykit/arview/entities(at:))
- [func hitTest(CGPoint, query: CollisionCastQueryType, mask: CollisionGroup) -> [CollisionCastHit]](/documentation/realitykit/arview/hittest(_:query:mask:))
- [func hitTest(CGPoint, types: ARHitTestResult.ResultType) -> [ARHitTestResult]](/documentation/realitykit/arview/hittest(_:types:))
- [func makeRaycastQuery(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> ARRaycastQuery?](/documentation/realitykit/arview/makeraycastquery(from:allowing:alignment:))
- [func raycast(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment) -> [ARRaycastResult]](/documentation/realitykit/arview/raycast(from:allowing:alignment:))
- [func trackedRaycast(from: CGPoint, allowing: ARRaycastQuery.Target, alignment: ARRaycastQuery.TargetAlignment, updateHandler: ([ARRaycastResult]) -> Void) -> ARTrackedRaycast?](/documentation/realitykit/arview/trackedraycast(from:allowing:alignment:updatehandler:))

#### Adding gesture recognizers to entities

- [func installGestures(ARView.EntityGestures, for: any HasCollision) -> [any EntityGestureRecognizer]](/documentation/realitykit/arview/installgestures(_:for:))
- [func gestureRecognizer(UIGestureRecognizer, shouldRecognizeSimultaneouslyWith: UIGestureRecognizer) -> Bool](/documentation/realitykit/arview/gesturerecognizer(_:shouldrecognizesimultaneouslywith:))

#### Mapping between coordinate spaces

- [func project(SIMD3<Float>) -> CGPoint?](/documentation/realitykit/arview/project(_:))
- [func unproject(CGPoint, ontoPlane: float4x4, relativeToCamera: Bool) -> SIMD3<Float>?](/documentation/realitykit/arview/unproject(_:ontoplane:relativetocamera:))
- [func unproject(CGPoint, ontoPlane: float4x4) -> SIMD3<Float>?](/documentation/realitykit/arview/unproject(_:ontoplane:))
- [func unproject(CGPoint, viewport: CGRect) -> SIMD3<Float>?](/documentation/realitykit/arview/unproject(_:viewport:))
- [func ray(through: CGPoint) -> (origin: SIMD3<Float>, direction: SIMD3<Float>)?](/documentation/realitykit/arview/ray(through:))

#### Handling touch input

- [func touchesBegan(Set<UITouch>, with: UIEvent?)](/documentation/realitykit/arview/touchesbegan(_:with:))
- [func touchesMoved(Set<UITouch>, with: UIEvent?)](/documentation/realitykit/arview/touchesmoved(_:with:))
- [func touchesEnded(Set<UITouch>, with: UIEvent?)](/documentation/realitykit/arview/touchesended(_:with:))
- [func touchesCancelled(Set<UITouch>, with: UIEvent?)](/documentation/realitykit/arview/touchescancelled(_:with:))

#### Handling keyboard input

- [var acceptsFirstResponder: Bool](/documentation/realitykit/arview/acceptsfirstresponder)
- [func keyDown(with: NSEvent)](/documentation/realitykit/arview/keydown(with:))
- [func keyUp(with: NSEvent)](/documentation/realitykit/arview/keyup(with:))

#### Handling mouse input

- [func mouseDown(with: NSEvent)](/documentation/realitykit/arview/mousedown(with:))
- [func mouseDragged(with: NSEvent)](/documentation/realitykit/arview/mousedragged(with:))
- [func mouseUp(with: NSEvent)](/documentation/realitykit/arview/mouseup(with:))
- [func mouseMoved(with: NSEvent)](/documentation/realitykit/arview/mousemoved(with:))
- [func rightMouseDown(with: NSEvent)](/documentation/realitykit/arview/rightmousedown(with:))
- [func rightMouseDragged(with: NSEvent)](/documentation/realitykit/arview/rightmousedragged(with:))
- [func rightMouseUp(with: NSEvent)](/documentation/realitykit/arview/rightmouseup(with:))
- [func otherMouseDown(with: NSEvent)](/documentation/realitykit/arview/othermousedown(with:))
- [func otherMouseDragged(with: NSEvent)](/documentation/realitykit/arview/othermousedragged(with:))
- [func otherMouseUp(with: NSEvent)](/documentation/realitykit/arview/othermouseup(with:))
- [func scrollWheel(with: NSEvent)](/documentation/realitykit/arview/scrollwheel(with:))

#### Managing the view

- [var frame: NSRect](/documentation/realitykit/arview/frame)
- [var contentScaleFactor: CGFloat](/documentation/realitykit/arview/contentscalefactor)
- [func didMoveToSuperview()](/documentation/realitykit/arview/didmovetosuperview())
- [func didMoveToWindow()](/documentation/realitykit/arview/didmovetowindow())
- [func layoutSubviews()](/documentation/realitykit/arview/layoutsubviews())
- [func layout()](/documentation/realitykit/arview/layout())
- [class var layerClass: AnyClass](/documentation/realitykit/arview/layerclass)
- [func makeBackingLayer() -> CALayer](/documentation/realitykit/arview/makebackinglayer())
- [func viewDidChangeBackingProperties()](/documentation/realitykit/arview/viewdidchangebackingproperties())
- [func viewDidMoveToSuperview()](/documentation/realitykit/arview/viewdidmovetosuperview())

#### Taking a snapshot

- [func snapshot(saveToHDR: Bool, completion: (ARView.Image?) -> Void)](/documentation/realitykit/arview/snapshot(savetohdr:completion:)-66jzu)
- [func snapshot(saveToHDR: Bool, completion: (ARView.Image?) -> Void)](/documentation/realitykit/arview/snapshot(savetohdr:completion:)-91ifk)
- [ARView.Image](/documentation/realitykit/arview/image)

#### Debugging the session

- [Improving the Performance of a RealityKit App](/documentation/realitykit/improving-the-performance-of-a-realitykit-app)

##### Optimization targets

- [Reducing CPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-cpu-utilization-in-your-realitykit-app)
- [Reducing GPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-gpu-utilization-in-your-realitykit-app)
- [var debugOptions: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.property)

#### Structures

- [ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct)

##### Configuring debug options

- [static let none: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/none)
- [static let showPhysics: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showphysics)
- [static let showStatistics: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showstatistics)
- [static let showAnchorOrigins: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showanchororigins)
- [static let showAnchorGeometry: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showanchorgeometry)
- [static let showWorldOrigin: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showworldorigin)
- [static let showFeaturePoints: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showfeaturepoints)
- [static let showSceneUnderstanding: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showsceneunderstanding)

##### Creating a debug option set

- [init(rawValue: Int)](/documentation/realitykit/arview/debugoptions-swift.struct/init(rawvalue:))
- [let rawValue: Int](/documentation/realitykit/arview/debugoptions-swift.struct/rawvalue)
- [ARView.EntityGestures](/documentation/realitykit/arview/entitygestures)

##### Recognizing gesture types

- [static let all: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/all)
- [static let rotation: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/rotation)
- [static let scale: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/scale)
- [static let translation: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/translation)

##### Using entity gestures

- [EntityGestureRecognizer](/documentation/realitykit/entitygesturerecognizer)

###### Using the gesture recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitygesturerecognizer/entity)
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitygesturerecognizer/location(in:))
- [EntityRotationGestureRecognizer](/documentation/realitykit/entityrotationgesturerecognizer)

###### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityrotationgesturerecognizer/init(target:action:))

###### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityrotationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityrotationgesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityrotationgesturerecognizer/touchesbegan(_:with:))
- [EntityScaleGestureRecognizer](/documentation/realitykit/entityscalegesturerecognizer)

###### Creating the recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityscalegesturerecognizer/init(target:action:))

###### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityscalegesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityscalegesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityscalegesturerecognizer/touchesbegan(_:with:))
- [EntityTranslationGestureRecognizer](/documentation/realitykit/entitytranslationgesturerecognizer)

###### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entitytranslationgesturerecognizer/init(target:action:))

###### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitytranslationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entitytranslationgesturerecognizer/canprevent(_:))
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/location(in:))
- [func reset()](/documentation/realitykit/entitytranslationgesturerecognizer/reset())
- [func setTranslation(SIMD3<Float>, in: Entity?)](/documentation/realitykit/entitytranslationgesturerecognizer/settranslation(_:in:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesbegan(_:with:))
- [func touchesCancelled(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchescancelled(_:with:))
- [func touchesEnded(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesended(_:with:))
- [func touchesMoved(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesmoved(_:with:))
- [func translation(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/translation(in:))
- [func velocity(in: Entity?) -> SIMD3<Float>](/documentation/realitykit/entitytranslationgesturerecognizer/velocity(in:))
- [ARView.Environment](/documentation/realitykit/arview/environment-swift.struct)

##### Creating an environment

- [init(background: ARView.Environment.Background, lighting: ARView.Environment.ImageBasedLight, reverb: ARView.Environment.Reverb)](/documentation/realitykit/arview/environment-swift.struct/init(background:lighting:reverb:))

##### Setting a background

- [var background: ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.property)
- [ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct)

###### Backgrounds

- [static func cameraFeed(exposureCompensation: Float) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/camerafeed(exposurecompensation:))
- [static func color(ARView.Environment.Color) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:)-97jik)
- [static func color(ARView.Environment.Color) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:)-5hh3f)
- [static func skybox(EnvironmentResource) -> ARView.Environment.Background](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/skybox(_:))

###### Type Methods

- [static color(_:)](/documentation/realitykit/arview/environment-swift.struct/background-swift.struct/color(_:))

##### Lighting the environment

- [var lighting: ARView.Environment.ImageBasedLight](/documentation/realitykit/arview/environment-swift.struct/lighting)
- [ARView.Environment.ImageBasedLight](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight)

###### Resources

- [var resource: EnvironmentResource?](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight/resource)

###### Modulating intensity

- [var intensityExponent: Float](/documentation/realitykit/arview/environment-swift.struct/imagebasedlight/intensityexponent)

##### Defining acoustic properties

- [var reverb: ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.property)
- [ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum)

###### Available reverb settings

- [case noReverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/noreverb)
- [case preset(ARView.Environment.Reverb.Preset)](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset(_:))

###### Reverb presets

- [static var automatic: ARView.Environment.Reverb](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/automatic)
- [ARView.Environment.Reverb.Preset](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset)

###### Reverb presets

- [case cathedral](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/cathedral)
- [case largeHall](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/largehall)
- [case largeRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/largeroom)
- [case mediumHall](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/mediumhall)
- [case mediumRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/mediumroom)
- [case smallRoom](/documentation/realitykit/arview/environment-swift.struct/reverb-swift.enum/preset/smallroom)

##### Structures

- [ARView.Environment.SceneUnderstanding](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct)

###### Structures

- [ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct)

###### Type Properties

- [static let collision: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/collision)
- [static let `default`: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/default)
- [static let occlusion: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/occlusion)
- [static let physics: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/physics)
- [static let receivesLighting: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/receiveslighting)

###### Instance Properties

- [var options: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.property)

##### Instance Properties

- [var sceneUnderstanding: ARView.Environment.SceneUnderstanding](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.property)

##### Type Aliases

- [ARView.Environment.Color](/documentation/realitykit/arview/environment-swift.struct/color)
- [ARView.PostProcessContext](/documentation/realitykit/arview/postprocesscontext)

##### Initializers

- [init(any MTLDevice, any MTLCommandBuffer, any MTLTexture, any MTLTexture, any MTLTexture, float4x4, TimeInterval)](/documentation/realitykit/arview/postprocesscontext/init(_:_:_:_:_:_:_:))

##### Instance Properties

- [var commandBuffer: any MTLCommandBuffer](/documentation/realitykit/arview/postprocesscontext/commandbuffer)
- [var device: any MTLDevice](/documentation/realitykit/arview/postprocesscontext/device)
- [var projection: float4x4](/documentation/realitykit/arview/postprocesscontext/projection)
- [var sourceColorTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/sourcecolortexture)
- [var sourceDepthTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/sourcedepthtexture)
- [var targetColorTexture: any MTLTexture](/documentation/realitykit/arview/postprocesscontext/targetcolortexture)
- [var time: TimeInterval](/documentation/realitykit/arview/postprocesscontext/time)
- [ARView.RenderCallbacks](/documentation/realitykit/arview/rendercallbacks-swift.struct)

##### Creating a callback object

- [init()](/documentation/realitykit/arview/rendercallbacks-swift.struct/init())

##### Register callback closures

- [var prepareWithDevice: ((any MTLDevice) -> Void)?](/documentation/realitykit/arview/rendercallbacks-swift.struct/preparewithdevice)
- [var postProcess: ((ARView.PostProcessContext) -> Void)?](/documentation/realitykit/arview/rendercallbacks-swift.struct/postprocess)
- [ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct)

##### Disabling rendering effects

- [static let disableCameraGrain: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablecameragrain)
- [static let disableHDR: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablehdr)
- [static let disableGroundingShadows: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablegroundingshadows)
- [static let disableMotionBlur: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablemotionblur)
- [static let disableDepthOfField: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disabledepthoffield)
- [static let disableFaceMesh: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablefacemesh)
- [static let disablePersonOcclusion: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablepersonocclusion)
- [static let disableAREnvironmentLighting: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablearenvironmentlighting)
- [static let disableFaceOcclusions: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disablefaceocclusions)
- [static let disableAutomaticLighting: ARView.RenderOptions](/documentation/realitykit/arview/renderoptions-swift.struct/disableautomaticlighting)

#### Instance Methods

- [func gestureRecognizer(UIGestureRecognizer, shouldReceive: UITouch) -> Bool](/documentation/realitykit/arview/gesturerecognizer(_:shouldreceive:))
- [func snapshot(saveToHDR:completion:)](/documentation/realitykit/arview/snapshot(savetohdr:completion:))

#### Enumerations

- [ARView.CameraMode](/documentation/realitykit/arview/cameramode-swift.enum)

##### Setting the camera mode

- [case ar](/documentation/realitykit/arview/cameramode-swift.enum/ar)
- [case nonAR](/documentation/realitykit/arview/cameramode-swift.enum/nonar)

#### Default Implementations

- [ARSessionProviding Implementations](/documentation/realitykit/arview/arsessionproviding-implementations)

##### Instance Properties

- [var session: ARSession](/documentation/realitykit/arview/session)
- [ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct)

#### Configuring debug options

- [static let none: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/none)
- [static let showPhysics: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showphysics)
- [static let showStatistics: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showstatistics)
- [static let showAnchorOrigins: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showanchororigins)
- [static let showAnchorGeometry: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showanchorgeometry)
- [static let showWorldOrigin: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showworldorigin)
- [static let showFeaturePoints: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showfeaturepoints)
- [static let showSceneUnderstanding: ARView.DebugOptions](/documentation/realitykit/arview/debugoptions-swift.struct/showsceneunderstanding)

#### Creating a debug option set

- [init(rawValue: Int)](/documentation/realitykit/arview/debugoptions-swift.struct/init(rawvalue:))
- [let rawValue: Int](/documentation/realitykit/arview/debugoptions-swift.struct/rawvalue)
- [ARViewBase](/documentation/realitykit/arviewbase)
- [Presentation UI](/documentation/realitykit/presentation-user-interface)

### Direct and indirect gestures

- [Transforming RealityKit entities using gestures](/documentation/realitykit/transforming-realitykit-entities-with-gestures)
- [InputTargetComponent](/documentation/realitykit/inputtargetcomponent)

#### Structures

- [InputTargetComponent.InputType](/documentation/realitykit/inputtargetcomponent/inputtype)

##### Type Properties

- [static let all: InputTargetComponent.InputType](/documentation/realitykit/inputtargetcomponent/inputtype/all)
- [static let direct: InputTargetComponent.InputType](/documentation/realitykit/inputtargetcomponent/inputtype/direct)
- [static let indirect: InputTargetComponent.InputType](/documentation/realitykit/inputtargetcomponent/inputtype/indirect)

#### Initializers

- [init(allowedInputTypes: InputTargetComponent.InputType)](/documentation/realitykit/inputtargetcomponent/init(allowedinputtypes:))

#### Instance Properties

- [var allowedInputTypes: InputTargetComponent.InputType](/documentation/realitykit/inputtargetcomponent/allowedinputtypes)
- [var isEnabled: Bool](/documentation/realitykit/inputtargetcomponent/isenabled)
- [ManipulationComponent](/documentation/realitykit/manipulationcomponent)

#### Creating a manipulation component

- [init()](/documentation/realitykit/manipulationcomponent/init())

#### Configuring the manipulation

- [static func configureEntity(Entity, hoverEffect: HoverEffectComponent.HoverEffect?, allowedInputTypes: InputTargetComponent.InputType?, collisionShapes: [ShapeResource]?)](/documentation/realitykit/manipulationcomponent/configureentity(_:hovereffect:allowedinputtypes:collisionshapes:))
- [var audioConfiguration: ManipulationComponent.AudioConfiguration](/documentation/realitykit/manipulationcomponent/audioconfiguration-swift.property)
- [var dynamics: ManipulationComponent.Dynamics](/documentation/realitykit/manipulationcomponent/dynamics-swift.property)
- [var releaseBehavior: ManipulationComponent.ReleaseBehavior](/documentation/realitykit/manipulationcomponent/releasebehavior-swift.property)

#### Structures

- [ManipulationComponent.AudioConfiguration](/documentation/realitykit/manipulationcomponent/audioconfiguration-swift.struct)

##### Type Properties

- [static var `default`: ManipulationComponent.AudioConfiguration](/documentation/realitykit/manipulationcomponent/audioconfiguration-swift.struct/default)
- [static var none: ManipulationComponent.AudioConfiguration](/documentation/realitykit/manipulationcomponent/audioconfiguration-swift.struct/none)
- [ManipulationComponent.Dynamics](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct)

##### Structures

- [ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.struct)

###### Type Properties

- [static var high: ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.struct/high)
- [static var low: ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.struct/low)
- [static var medium: ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.struct/medium)
- [static var zero: ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.struct/zero)
- [ManipulationComponent.Dynamics.RotationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/rotationbehavior)

###### Type Properties

- [static var none: ManipulationComponent.Dynamics.RotationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/rotationbehavior/none)
- [static var unconstrained: ManipulationComponent.Dynamics.RotationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/rotationbehavior/unconstrained)
- [ManipulationComponent.Dynamics.ScalingBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/scalingbehavior-swift.struct)

###### Type Properties

- [static var none: ManipulationComponent.Dynamics.ScalingBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/scalingbehavior-swift.struct/none)
- [static var unconstrained: ManipulationComponent.Dynamics.ScalingBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/scalingbehavior-swift.struct/unconstrained)
- [ManipulationComponent.Dynamics.TranslationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/translationbehavior-swift.struct)

###### Type Properties

- [static var none: ManipulationComponent.Dynamics.TranslationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/translationbehavior-swift.struct/none)
- [static var unconstrained: ManipulationComponent.Dynamics.TranslationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/translationbehavior-swift.struct/unconstrained)

##### Initializers

- [init()](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/init())

##### Instance Properties

- [var inertia: ManipulationComponent.Dynamics.Inertia](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/inertia-swift.property)
- [var primaryRotationBehavior: ManipulationComponent.Dynamics.RotationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/primaryrotationbehavior)
- [var scalingBehavior: ManipulationComponent.Dynamics.ScalingBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/scalingbehavior-swift.property)
- [var secondaryRotationBehavior: ManipulationComponent.Dynamics.RotationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/secondaryrotationbehavior)
- [var translationBehavior: ManipulationComponent.Dynamics.TranslationBehavior](/documentation/realitykit/manipulationcomponent/dynamics-swift.struct/translationbehavior-swift.property)
- [ManipulationComponent.HitTarget](/documentation/realitykit/manipulationcomponent/hittarget)

##### Initializers

- [init(redirectedEntity: Entity?)](/documentation/realitykit/manipulationcomponent/hittarget/init(redirectedentity:))

##### Instance Properties

- [var redirectedEntity: Entity?](/documentation/realitykit/manipulationcomponent/hittarget/redirectedentity)
- [ManipulationComponent.InputDevice](/documentation/realitykit/manipulationcomponent/inputdevice)

##### Instance Properties

- [var chirality: ManipulationComponent.InputDevice.Chirality?](/documentation/realitykit/manipulationcomponent/inputdevice/chirality-swift.property)
- [var kind: ManipulationComponent.InputDevice.Kind](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.property)
- [var pose: Pose3DFloat?](/documentation/realitykit/manipulationcomponent/inputdevice/pose)

##### Enumerations

- [ManipulationComponent.InputDevice.Chirality](/documentation/realitykit/manipulationcomponent/inputdevice/chirality-swift.enum)

###### Enumeration Cases

- [case left](/documentation/realitykit/manipulationcomponent/inputdevice/chirality-swift.enum/left)
- [case right](/documentation/realitykit/manipulationcomponent/inputdevice/chirality-swift.enum/right)
- [ManipulationComponent.InputDevice.Kind](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum)

###### Structures

- [ManipulationComponent.InputDevice.Kind.Set](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set)

###### Initializers

- [init(ManipulationComponent.InputDevice.Kind)](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set/init(_:))

###### Type Properties

- [static var all: ManipulationComponent.InputDevice.Kind.Set](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set/all)
- [static var directPinch: ManipulationComponent.InputDevice.Kind.Set](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set/directpinch)
- [static var indirectPinch: ManipulationComponent.InputDevice.Kind.Set](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set/indirectpinch)
- [static var pointer: ManipulationComponent.InputDevice.Kind.Set](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/set/pointer)

###### Enumeration Cases

- [case directPinch](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/directpinch)
- [case indirectPinch](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/indirectpinch)
- [case pointer](/documentation/realitykit/manipulationcomponent/inputdevice/kind-swift.enum/pointer)
- [ManipulationComponent.ReleaseBehavior](/documentation/realitykit/manipulationcomponent/releasebehavior-swift.struct)

##### Type Properties

- [static var reset: ManipulationComponent.ReleaseBehavior](/documentation/realitykit/manipulationcomponent/releasebehavior-swift.struct/reset)
- [static var stay: ManipulationComponent.ReleaseBehavior](/documentation/realitykit/manipulationcomponent/releasebehavior-swift.struct/stay)
- [GestureComponent](/documentation/realitykit/gesturecomponent)

#### Initializers

- [init(some Gesture)](/documentation/realitykit/gesturecomponent/init(_:))
- [EntityTargetValue](/documentation/realitykit/entitytargetvalue)

#### Accessing gesture info

- [var entity: Entity](/documentation/realitykit/entitytargetvalue/entity)
- [var gestureValue: Value](/documentation/realitykit/entitytargetvalue/gesturevalue)
- [subscript<T>(dynamicMember _: KeyPath<Value, T>) -> T](/documentation/realitykit/entitytargetvalue/subscript(dynamicmember:))

#### Instance Methods

- [func unproject(CGPoint, from: some CoordinateSpaceProtocol, to: some RealityCoordinateSpace) -> SIMD3<Float>?](/documentation/realitykit/entitytargetvalue/unproject(_:from:to:))
- [func unproject(KeyPath<Value, CGPoint>, to: some RealityCoordinateSpace) -> SIMD3<Float>?](/documentation/realitykit/entitytargetvalue/unproject(_:to:))

### Accessibility

- [Improving the Accessibility of RealityKit Apps](/documentation/realitykit/improving-the-accessibility-of-realitykit-apps)
- [AccessibilityComponent](/documentation/realitykit/accessibilitycomponent)

#### Creating an accessibility component

- [init()](/documentation/realitykit/accessibilitycomponent/init())

#### Providing accessibility information

- [var isAccessibilityElement: Bool](/documentation/realitykit/accessibilitycomponent/isaccessibilityelement)
- [var label: LocalizedStringResource?](/documentation/realitykit/accessibilitycomponent/label)
- [var value: LocalizedStringResource?](/documentation/realitykit/accessibilitycomponent/value)

#### Defining traits

- [var traits: UIAccessibilityTraits](/documentation/realitykit/accessibilitycomponent/traits)

#### Defining actions

- [var systemActions: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/systemactions)

#### Specifying custom data

- [var customActions: [LocalizedStringResource]](/documentation/realitykit/accessibilitycomponent/customactions)
- [var customContent: [AccessibilityComponent.CustomContent]](/documentation/realitykit/accessibilitycomponent/customcontent-swift.property)

#### Identifying the next element

- [var customRotors: [AccessibilityComponent.RotorType]](/documentation/realitykit/accessibilitycomponent/customrotors)

#### Structures

- [AccessibilityComponent.CustomContent](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct)

##### Initializers

- [init(label: LocalizedStringResource, value: LocalizedStringResource, importance: AXCustomContent.Importance)](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/init(label:value:importance:))

##### Instance Properties

- [var importance: AXCustomContent.Importance](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/importance)
- [var label: LocalizedStringResource](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/label)
- [var value: LocalizedStringResource](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/value)
- [AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions)

##### Type Properties

- [static let activate: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/activate)
- [static let decrement: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/decrement)
- [static let increment: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/increment)

#### Enumerations

- [AccessibilityComponent.RotorType](/documentation/realitykit/accessibilitycomponent/rotortype)

##### Enumeration Cases

- [case custom(LocalizedStringResource)](/documentation/realitykit/accessibilitycomponent/rotortype/custom(_:))
- [case system(UIAccessibilityCustomRotor.SystemRotorType)](/documentation/realitykit/accessibilitycomponent/rotortype/system(_:))
- [AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions)

#### Type Properties

- [static let activate: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/activate)
- [static let decrement: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/decrement)
- [static let increment: AccessibilityComponent.SupportedActions](/documentation/realitykit/accessibilitycomponent/supportedactions/increment)
- [AccessibilityComponent.CustomContent](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct)

#### Initializers

- [init(label: LocalizedStringResource, value: LocalizedStringResource, importance: AXCustomContent.Importance)](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/init(label:value:importance:))

#### Instance Properties

- [var importance: AXCustomContent.Importance](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/importance)
- [var label: LocalizedStringResource](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/label)
- [var value: LocalizedStringResource](/documentation/realitykit/accessibilitycomponent/customcontent-swift.struct/value)
- [AccessibilityComponent.RotorType](/documentation/realitykit/accessibilitycomponent/rotortype)

#### Enumeration Cases

- [case custom(LocalizedStringResource)](/documentation/realitykit/accessibilitycomponent/rotortype/custom(_:))
- [case system(UIAccessibilityCustomRotor.SystemRotorType)](/documentation/realitykit/accessibilitycomponent/rotortype/system(_:))
- [AccessibilityEvents](/documentation/realitykit/accessibilityevents)

#### Structures

- [AccessibilityEvents.Activate](/documentation/realitykit/accessibilityevents/activate)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/activate/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/activate/entity)
- [AccessibilityEvents.CustomAction](/documentation/realitykit/accessibilityevents/customaction)

##### Initializers

- [init(key: LocalizedStringResource, entity: Entity)](/documentation/realitykit/accessibilityevents/customaction/init(key:entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/customaction/entity)
- [var key: LocalizedStringResource](/documentation/realitykit/accessibilityevents/customaction/key)
- [AccessibilityEvents.Decrement](/documentation/realitykit/accessibilityevents/decrement)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/decrement/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/decrement/entity)
- [AccessibilityEvents.Increment](/documentation/realitykit/accessibilityevents/increment)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/increment/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/increment/entity)
- [AccessibilityEvents.RotorNavigation](/documentation/realitykit/accessibilityevents/rotornavigation)

##### Initializers

- [init(rotorType: AccessibilityComponent.RotorType, hostEntity: Entity, currentItem: Any?, searchDirection: UIAccessibilityCustomRotor.Direction, resultHandler: (Any) -> Void)](/documentation/realitykit/accessibilityevents/rotornavigation/init(rotortype:hostentity:currentitem:searchdirection:resulthandler:))

##### Instance Properties

- [let currentItem: Any?](/documentation/realitykit/accessibilityevents/rotornavigation/currentitem)
- [let hostEntity: Entity](/documentation/realitykit/accessibilityevents/rotornavigation/hostentity)
- [let resultHandler: (Any) -> Void](/documentation/realitykit/accessibilityevents/rotornavigation/resulthandler)
- [let rotorType: AccessibilityComponent.RotorType](/documentation/realitykit/accessibilityevents/rotornavigation/rotortype)
- [let searchDirection: UIAccessibilityCustomRotor.Direction](/documentation/realitykit/accessibilityevents/rotornavigation/searchdirection)

### Visual adjustments

- [HoverEffectComponent](/documentation/realitykit/hovereffectcomponent)

#### Structures

- [HoverEffectComponent.GroupID](/documentation/realitykit/hovereffectcomponent/groupid)

##### Initializers

- [init()](/documentation/realitykit/hovereffectcomponent/groupid/init())
- [HoverEffectComponent.HighlightHoverEffectStyle](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle)

##### Initializers

- [init(color:strength:)](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/init(color:strength:))
- [init(color:strength:opacityFunction:)](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/init(color:strength:opacityfunction:))

##### Instance Properties

- [var color: NSColor](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/color-369cd)
- [var color: UIColor](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/color-9v0tl)
- [var opacityFunction: HoverEffectComponent.OpacityFunction](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/opacityfunction)
- [var strength: Float](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/strength)

##### Type Properties

- [static let `default`: HoverEffectComponent.HighlightHoverEffectStyle](/documentation/realitykit/hovereffectcomponent/highlighthovereffectstyle/default)
- [HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct)

##### Instance Properties

- [var groupID: HoverEffectComponent.GroupID?](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/groupid)

##### Type Methods

- [static func highlight(HoverEffectComponent.HighlightHoverEffectStyle) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/highlight(_:))
- [static func highlight(HoverEffectComponent.HighlightHoverEffectStyle, groupID: HoverEffectComponent.GroupID) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/highlight(_:groupid:))
- [static func shader(HoverEffectComponent.ShaderHoverEffectInputs) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/shader(_:))
- [static func shader(HoverEffectComponent.ShaderHoverEffectInputs, groupID: HoverEffectComponent.GroupID) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/shader(_:groupid:))
- [static func spotlight(HoverEffectComponent.SpotlightHoverEffectStyle) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/spotlight(_:))
- [static func spotlight(HoverEffectComponent.SpotlightHoverEffectStyle, groupID: HoverEffectComponent.GroupID) -> HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.struct/spotlight(_:groupid:))
- [HoverEffectComponent.ShaderHoverEffectInputs](/documentation/realitykit/hovereffectcomponent/shaderhovereffectinputs)

##### Initializers

- [init(fadeInDuration: TimeInterval, fadeOutDuration: TimeInterval)](/documentation/realitykit/hovereffectcomponent/shaderhovereffectinputs/init(fadeinduration:fadeoutduration:))

##### Instance Properties

- [var fadeInDuration: TimeInterval](/documentation/realitykit/hovereffectcomponent/shaderhovereffectinputs/fadeinduration)
- [var fadeOutDuration: TimeInterval](/documentation/realitykit/hovereffectcomponent/shaderhovereffectinputs/fadeoutduration)

##### Type Properties

- [static let `default`: HoverEffectComponent.ShaderHoverEffectInputs](/documentation/realitykit/hovereffectcomponent/shaderhovereffectinputs/default)
- [HoverEffectComponent.SpotlightHoverEffectStyle](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle)

##### Initializers

- [init(color:strength:)](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/init(color:strength:))
- [init(color:strength:opacityFunction:)](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/init(color:strength:opacityfunction:))

##### Instance Properties

- [var color: NSColor](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/color-4n481)
- [var color: UIColor](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/color-tdv8)
- [var opacityFunction: HoverEffectComponent.OpacityFunction](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/opacityfunction)
- [var strength: Float](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/strength)

##### Type Properties

- [static let `default`: HoverEffectComponent.SpotlightHoverEffectStyle](/documentation/realitykit/hovereffectcomponent/spotlighthovereffectstyle/default)

#### Initializers

- [init()](/documentation/realitykit/hovereffectcomponent/init())
- [init(HoverEffectComponent.HoverEffect)](/documentation/realitykit/hovereffectcomponent/init(_:))

#### Instance Properties

- [var hoverEffect: HoverEffectComponent.HoverEffect](/documentation/realitykit/hovereffectcomponent/hovereffect-swift.property)

#### Enumerations

- [HoverEffectComponent.OpacityFunction](/documentation/realitykit/hovereffectcomponent/opacityfunction)

##### Enumeration Cases

- [case blend](/documentation/realitykit/hovereffectcomponent/opacityfunction/blend)
- [case full](/documentation/realitykit/hovereffectcomponent/opacityfunction/full)
- [case mask](/documentation/realitykit/hovereffectcomponent/opacityfunction/mask)
- [BillboardComponent](/documentation/realitykit/billboardcomponent)

#### Initializers

- [init()](/documentation/realitykit/billboardcomponent/init())

#### Instance Properties

- [var blendFactor: Float](/documentation/realitykit/billboardcomponent/blendfactor)
- [EnvironmentBlendingComponent](/documentation/realitykit/environmentblendingcomponent)

#### Structures

- [EnvironmentBlendingComponent.BlendingMode](/documentation/realitykit/environmentblendingcomponent/blendingmode)

##### Type Properties

- [static var `default`: EnvironmentBlendingComponent.BlendingMode](/documentation/realitykit/environmentblendingcomponent/blendingmode/default)

##### Type Methods

- [static func occluded(by: EnvironmentBlendingComponent.EnvironmentType) -> EnvironmentBlendingComponent.BlendingMode](/documentation/realitykit/environmentblendingcomponent/blendingmode/occluded(by:))

#### Initializers

- [init()](/documentation/realitykit/environmentblendingcomponent/init())
- [init(preferredBlendingMode: EnvironmentBlendingComponent.BlendingMode)](/documentation/realitykit/environmentblendingcomponent/init(preferredblendingmode:))

#### Instance Properties

- [var preferredBlendingMode: EnvironmentBlendingComponent.BlendingMode](/documentation/realitykit/environmentblendingcomponent/preferredblendingmode)

#### Enumerations

- [EnvironmentBlendingComponent.EnvironmentType](/documentation/realitykit/environmentblendingcomponent/environmenttype)

##### Enumeration Cases

- [case surroundings](/documentation/realitykit/environmentblendingcomponent/environmenttype/surroundings)
- [LensDistortionData](/documentation/realitykit/lensdistortiondata)

#### Initializers

- [init(center: SIMD2<Float>, radialLookupTable: [Float])](/documentation/realitykit/lensdistortiondata/init(center:radiallookuptable:))

#### Instance Properties

- [let center: SIMD2<Float>](/documentation/realitykit/lensdistortiondata/center)
- [let radialLookupTable: [Float]](/documentation/realitykit/lensdistortiondata/radiallookuptable)
- [ImagePresentationComponent](/documentation/realitykit/imagepresentationcomponent)

#### Creating a component from a 2D image or spatial photo

- [init(contentsOf: URL) async throws](/documentation/realitykit/imagepresentationcomponent/init(contentsof:))
- [init(imageSource: CGImageSource) async throws](/documentation/realitykit/imagepresentationcomponent/init(imagesource:))

#### Creating a component from a spatial scene

- [ImagePresentationComponent.Spatial3DImage](/documentation/realitykit/imagepresentationcomponent/spatial3dimage)

##### Creating a spatial scene from a 2D image or spatial photo

- [convenience init(contentsOf: URL) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(contentsof:))
- [init(imageSource: CGImageSource) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(imagesource:))

##### Generating a spatial scene

- [func generate() async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/generate())
- [init(spatial3DImage: ImagePresentationComponent.Spatial3DImage)](/documentation/realitykit/imagepresentationcomponent/init(spatial3dimage:))

#### Setting and discovering viewing modes

- [ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct)

##### Monoscopic presentation

- [static let mono: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/mono)

##### Stereoscopic presentation of spatial photos

- [static let spatialStereo: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereo)
- [static let spatialStereoImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereoimmersive)

##### 3D presentation of generated spatial scenes

- [static let spatial3D: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3d)
- [static let spatial3DImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3dimmersive)
- [var viewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.property)
- [var desiredViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/desiredviewingmode)
- [var availableViewingModes: Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/availableviewingmodes)
- [static func supportedViewingModes(for: CGImageSource) -> Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:)-7za1y)
- [static func supportedViewingModes(for: CGImageSource) -> Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:)-7za1y)

#### Retrieving the current image size

- [var screenImageDimension: SIMD2<Float>](/documentation/realitykit/imagepresentationcomponent/screenimagedimension)

#### Retrieving the current screen mesh size

- [var screenHeight: Float](/documentation/realitykit/imagepresentationcomponent/screenheight)
- [var presentationScreenSize: SIMD2<Float>](/documentation/realitykit/imagepresentationcomponent/presentationscreensize)

#### Instance Methods

- [func aspectRatio(for: ImagePresentationComponent.ViewingMode) -> Float?](/documentation/realitykit/imagepresentationcomponent/aspectratio(for:))

#### Type Methods

- [static supportedViewingModes(for:)](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:))

### UIKit and AppKit gestures

- [ARView.EntityGestures](/documentation/realitykit/arview/entitygestures)

#### Recognizing gesture types

- [static let all: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/all)
- [static let rotation: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/rotation)
- [static let scale: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/scale)
- [static let translation: ARView.EntityGestures](/documentation/realitykit/arview/entitygestures/translation)

#### Using entity gestures

- [EntityGestureRecognizer](/documentation/realitykit/entitygesturerecognizer)

##### Using the gesture recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitygesturerecognizer/entity)
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitygesturerecognizer/location(in:))
- [EntityRotationGestureRecognizer](/documentation/realitykit/entityrotationgesturerecognizer)

##### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityrotationgesturerecognizer/init(target:action:))

##### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityrotationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityrotationgesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityrotationgesturerecognizer/touchesbegan(_:with:))
- [EntityScaleGestureRecognizer](/documentation/realitykit/entityscalegesturerecognizer)

##### Creating the recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityscalegesturerecognizer/init(target:action:))

##### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityscalegesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityscalegesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityscalegesturerecognizer/touchesbegan(_:with:))
- [EntityTranslationGestureRecognizer](/documentation/realitykit/entitytranslationgesturerecognizer)

##### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entitytranslationgesturerecognizer/init(target:action:))

##### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitytranslationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entitytranslationgesturerecognizer/canprevent(_:))
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/location(in:))
- [func reset()](/documentation/realitykit/entitytranslationgesturerecognizer/reset())
- [func setTranslation(SIMD3<Float>, in: Entity?)](/documentation/realitykit/entitytranslationgesturerecognizer/settranslation(_:in:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesbegan(_:with:))
- [func touchesCancelled(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchescancelled(_:with:))
- [func touchesEnded(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesended(_:with:))
- [func touchesMoved(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesmoved(_:with:))
- [func translation(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/translation(in:))
- [func velocity(in: Entity?) -> SIMD3<Float>](/documentation/realitykit/entitytranslationgesturerecognizer/velocity(in:))
- [EntityRotationGestureRecognizer](/documentation/realitykit/entityrotationgesturerecognizer)

#### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityrotationgesturerecognizer/init(target:action:))

#### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityrotationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityrotationgesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityrotationgesturerecognizer/touchesbegan(_:with:))
- [EntityScaleGestureRecognizer](/documentation/realitykit/entityscalegesturerecognizer)

#### Creating the recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entityscalegesturerecognizer/init(target:action:))

#### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entityscalegesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entityscalegesturerecognizer/canprevent(_:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entityscalegesturerecognizer/touchesbegan(_:with:))
- [EntityTranslationGestureRecognizer](/documentation/realitykit/entitytranslationgesturerecognizer)

#### Creating a recognizer

- [init(target: Any?, action: Selector?)](/documentation/realitykit/entitytranslationgesturerecognizer/init(target:action:))

#### Using the recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitytranslationgesturerecognizer/entity)
- [func canPrevent(UIGestureRecognizer) -> Bool](/documentation/realitykit/entitytranslationgesturerecognizer/canprevent(_:))
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/location(in:))
- [func reset()](/documentation/realitykit/entitytranslationgesturerecognizer/reset())
- [func setTranslation(SIMD3<Float>, in: Entity?)](/documentation/realitykit/entitytranslationgesturerecognizer/settranslation(_:in:))
- [func touchesBegan(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesbegan(_:with:))
- [func touchesCancelled(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchescancelled(_:with:))
- [func touchesEnded(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesended(_:with:))
- [func touchesMoved(Set<UITouch>, with: UIEvent)](/documentation/realitykit/entitytranslationgesturerecognizer/touchesmoved(_:with:))
- [func translation(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitytranslationgesturerecognizer/translation(in:))
- [func velocity(in: Entity?) -> SIMD3<Float>](/documentation/realitykit/entitytranslationgesturerecognizer/velocity(in:))
- [EntityGestureRecognizer](/documentation/realitykit/entitygesturerecognizer)

#### Using the gesture recognizer

- [var entity: (any HasCollision)?](/documentation/realitykit/entitygesturerecognizer/entity)
- [func location(in: Entity?) -> SIMD3<Float>?](/documentation/realitykit/entitygesturerecognizer/location(in:))

## Scene management and logic

- [Scenes](/documentation/realitykit/ecs-scenes)

### Scene management

- [Scene](/documentation/realitykit/scene)

#### Identifying the scene

- [var name: String](/documentation/realitykit/scene/name)

#### Adding and removing anchors

- [var anchors: Scene.AnchorCollection](/documentation/realitykit/scene/anchors)
- [func addAnchor(any HasAnchoring)](/documentation/realitykit/scene/addanchor(_:))
- [func removeAnchor(any HasAnchoring)](/documentation/realitykit/scene/removeanchor(_:))

#### Finding entities

- [func findEntity(named: String) -> Entity?](/documentation/realitykit/scene/findentity(named:))
- [func performQuery(EntityQuery) -> QueryResult<Entity>](/documentation/realitykit/scene/performquery(_:))
- [func findEntity(id: Entity.ID) -> Entity?](/documentation/realitykit/scene/findentity(id:))

#### Detecting intersections

- [func raycast(origin: SIMD3<Float>, direction: SIMD3<Float>, length: Float, query: CollisionCastQueryType, mask: CollisionGroup, relativeTo: Entity?) -> [CollisionCastHit]](/documentation/realitykit/scene/raycast(origin:direction:length:query:mask:relativeto:))
- [func raycast(from: SIMD3<Float>, to: SIMD3<Float>, query: CollisionCastQueryType, mask: CollisionGroup, relativeTo: Entity?) -> [CollisionCastHit]](/documentation/realitykit/scene/raycast(from:to:query:mask:relativeto:))
- [func convexCast(convexShape: ShapeResource, fromPosition: SIMD3<Float>, fromOrientation: simd_quatf, toPosition: SIMD3<Float>, toOrientation: simd_quatf, query: CollisionCastQueryType, mask: CollisionGroup, relativeTo: Entity?) -> [CollisionCastHit]](/documentation/realitykit/scene/convexcast(convexshape:fromposition:fromorientation:toposition:toorientation:query:mask:relativeto:))
- [func pixelCast(from: SIMD3<Float>, to: SIMD3<Float>) async throws -> PixelCastHit?](/documentation/realitykit/scene/pixelcast(from:to:))
- [func pixelCast(origin: SIMD3<Float>, direction: SIMD3<Float>, length: Float) async throws -> PixelCastHit?](/documentation/realitykit/scene/pixelcast(origin:direction:length:))

#### Synchronizing entities with other devices

- [var synchronizationService: (any SynchronizationService)?](/documentation/realitykit/scene/synchronizationservice)

#### Publishing and subscribing to events

- [func publisher<E>(for: E.Type, on: (any EventSource)?) -> Scene.Publisher<E>](/documentation/realitykit/scene/publisher(for:on:))
- [func subscribe<E>(to: E.Type, on: (any EventSource)?, (E) -> Void) -> any Cancellable](/documentation/realitykit/scene/subscribe(to:on:_:))
- [func publisher<E>(for: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?) -> Scene.Publisher<E>](/documentation/realitykit/scene/publisher(for:on:componenttype:))
- [func subscribe<E>(to: E.Type, on: (any EventSource)?, componentType: (any Component.Type)?, (E) -> Void) -> any Cancellable](/documentation/realitykit/scene/subscribe(to:on:componenttype:_:))

#### Structures

- [Scene.AnchorCollection](/documentation/realitykit/scene/anchorcollection)

##### Iterating over the collection

- [func makeIterator() -> Scene.AnchorCollection.Iterator](/documentation/realitykit/scene/anchorcollection/makeiterator())
- [Scene.AnchorCollection.Iterator](/documentation/realitykit/scene/anchorcollection/iterator)
- [Scene.AnchorCollection.Element](/documentation/realitykit/scene/anchorcollection/element)

##### Accessing anchors

- [subscript(Int) -> any HasAnchoring](/documentation/realitykit/scene/anchorcollection/subscript(_:))
- [Scene.AnchorCollection.SubSequence](/documentation/realitykit/scene/anchorcollection/subsequence)

##### Adding anchors

- [func append(any HasAnchoring)](/documentation/realitykit/scene/anchorcollection/append(_:))
- [func append(contentsOf: [any HasAnchoring])](/documentation/realitykit/scene/anchorcollection/append(contentsof:)-3bjib)
- [func append<S>(contentsOf: S)](/documentation/realitykit/scene/anchorcollection/append(contentsof:)-4sf55)

##### Removing anchors

- [func remove(any HasAnchoring)](/documentation/realitykit/scene/anchorcollection/remove(_:))
- [func remove(at: Int)](/documentation/realitykit/scene/anchorcollection/remove(at:))
- [func removeAll()](/documentation/realitykit/scene/anchorcollection/removeall())
- [func removeAll(keepCapacity: Bool)](/documentation/realitykit/scene/anchorcollection/removeall(keepcapacity:))

##### Replacing anchors

- [func replaceAll([any HasAnchoring])](/documentation/realitykit/scene/anchorcollection/replaceall(_:)-tris)
- [func replaceAll<S>(S)](/documentation/realitykit/scene/anchorcollection/replaceall(_:)-5t195)

##### Manipulating indices

- [Scene.AnchorCollection.Index](/documentation/realitykit/scene/anchorcollection/index)
- [var startIndex: Int](/documentation/realitykit/scene/anchorcollection/startindex)
- [var endIndex: Int](/documentation/realitykit/scene/anchorcollection/endindex)
- [func index(after: Int) -> Int](/documentation/realitykit/scene/anchorcollection/index(after:))

##### Describing the collection

- [var description: String](/documentation/realitykit/scene/anchorcollection/description)

##### Instance Methods

- [func append(contentsOf:)](/documentation/realitykit/scene/anchorcollection/append(contentsof:))
- [func replaceAll(_:)](/documentation/realitykit/scene/anchorcollection/replaceall(_:))

##### Type Aliases

- [Scene.AnchorCollection.Indices](/documentation/realitykit/scene/anchorcollection/indices)

##### Default Implementations

- [CustomStringConvertible Implementations](/documentation/realitykit/scene/anchorcollection/customstringconvertible-implementations)

###### Instance Properties

- [var description: String](/documentation/realitykit/scene/anchorcollection/description)
- [Scene.Publisher](/documentation/realitykit/scene/publisher)

#### Instance Properties

- [var timebase: CMTimebase](/documentation/realitykit/scene/timebase)

#### Default Implementations

- [Equatable Implementations](/documentation/realitykit/scene/equatable-implementations)

##### Operators

- [static func == (Scene, Scene) -> Bool](/documentation/realitykit/scene/==(_:_:))
- [Hashable Implementations](/documentation/realitykit/scene/hashable-implementations)

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/scene/hash(into:))
- [Scene.AnchorCollection](/documentation/realitykit/scene/anchorcollection)

#### Iterating over the collection

- [func makeIterator() -> Scene.AnchorCollection.Iterator](/documentation/realitykit/scene/anchorcollection/makeiterator())
- [Scene.AnchorCollection.Iterator](/documentation/realitykit/scene/anchorcollection/iterator)
- [Scene.AnchorCollection.Element](/documentation/realitykit/scene/anchorcollection/element)

#### Accessing anchors

- [subscript(Int) -> any HasAnchoring](/documentation/realitykit/scene/anchorcollection/subscript(_:))
- [Scene.AnchorCollection.SubSequence](/documentation/realitykit/scene/anchorcollection/subsequence)

#### Adding anchors

- [func append(any HasAnchoring)](/documentation/realitykit/scene/anchorcollection/append(_:))
- [func append(contentsOf: [any HasAnchoring])](/documentation/realitykit/scene/anchorcollection/append(contentsof:)-3bjib)
- [func append<S>(contentsOf: S)](/documentation/realitykit/scene/anchorcollection/append(contentsof:)-4sf55)

#### Removing anchors

- [func remove(any HasAnchoring)](/documentation/realitykit/scene/anchorcollection/remove(_:))
- [func remove(at: Int)](/documentation/realitykit/scene/anchorcollection/remove(at:))
- [func removeAll()](/documentation/realitykit/scene/anchorcollection/removeall())
- [func removeAll(keepCapacity: Bool)](/documentation/realitykit/scene/anchorcollection/removeall(keepcapacity:))

#### Replacing anchors

- [func replaceAll([any HasAnchoring])](/documentation/realitykit/scene/anchorcollection/replaceall(_:)-tris)
- [func replaceAll<S>(S)](/documentation/realitykit/scene/anchorcollection/replaceall(_:)-5t195)

#### Manipulating indices

- [Scene.AnchorCollection.Index](/documentation/realitykit/scene/anchorcollection/index)
- [var startIndex: Int](/documentation/realitykit/scene/anchorcollection/startindex)
- [var endIndex: Int](/documentation/realitykit/scene/anchorcollection/endindex)
- [func index(after: Int) -> Int](/documentation/realitykit/scene/anchorcollection/index(after:))

#### Describing the collection

- [var description: String](/documentation/realitykit/scene/anchorcollection/description)

#### Instance Methods

- [func append(contentsOf:)](/documentation/realitykit/scene/anchorcollection/append(contentsof:))
- [func replaceAll(_:)](/documentation/realitykit/scene/anchorcollection/replaceall(_:))

#### Type Aliases

- [Scene.AnchorCollection.Indices](/documentation/realitykit/scene/anchorcollection/indices)

#### Default Implementations

- [CustomStringConvertible Implementations](/documentation/realitykit/scene/anchorcollection/customstringconvertible-implementations)

##### Instance Properties

- [var description: String](/documentation/realitykit/scene/anchorcollection/description)

### Entity searches

- [QueryPredicate](/documentation/realitykit/querypredicate)

#### Creating predicates

- [static func has<T>(T.Type) -> QueryPredicate<Entity>](/documentation/realitykit/querypredicate/has(_:))

#### Comparing predicates

- [func ! <Value>(QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/!(_:))
- [func && <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/&&(_:_:))
- [func || <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/__(_:_:))
- [PixelCastHit](/documentation/realitykit/pixelcasthit)

#### Instance Properties

- [var barycentric: SIMD3<Float>?](/documentation/realitykit/pixelcasthit/barycentric)
- [var entity: Entity](/documentation/realitykit/pixelcasthit/entity)
- [var instance: UInt32](/documentation/realitykit/pixelcasthit/instance)
- [var meshPart: UInt64](/documentation/realitykit/pixelcasthit/meshpart)
- [var normal: SIMD3<Float>](/documentation/realitykit/pixelcasthit/normal)
- [var position: SIMD3<Float>](/documentation/realitykit/pixelcasthit/position)
- [var primitive: UInt32](/documentation/realitykit/pixelcasthit/primitive)

### Event publishers and subscription

- [SceneEvents](/documentation/realitykit/sceneevents)

#### Detecting scene-level updates

- [SceneEvents.Update](/documentation/realitykit/sceneevents/update)

##### Characterizing an update

- [let scene: Scene](/documentation/realitykit/sceneevents/update/scene)
- [let deltaTime: TimeInterval](/documentation/realitykit/sceneevents/update/deltatime)
- [SceneEvents.AnchoredStateChanged](/documentation/realitykit/sceneevents/anchoredstatechanged)

##### Characterizing an update

- [let anchor: any HasAnchoring](/documentation/realitykit/sceneevents/anchoredstatechanged/anchor)
- [let isAnchored: Bool](/documentation/realitykit/sceneevents/anchoredstatechanged/isanchored)

#### Detecting scene hierarchy changes

- [SceneEvents.DidAddEntity](/documentation/realitykit/sceneevents/didaddentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/didaddentity/entity)
- [SceneEvents.DidReparentEntity](/documentation/realitykit/sceneevents/didreparententity)

##### Instance Properties

- [let child: Entity](/documentation/realitykit/sceneevents/didreparententity/child)
- [let previousParent: Entity?](/documentation/realitykit/sceneevents/didreparententity/previousparent)
- [SceneEvents.WillRemoveEntity](/documentation/realitykit/sceneevents/willremoveentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/willremoveentity/entity)
- [SceneEvents.DidActivateEntity](/documentation/realitykit/sceneevents/didactivateentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/didactivateentity/entity)
- [SceneEvents.WillDeactivateEntity](/documentation/realitykit/sceneevents/willdeactivateentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/willdeactivateentity/entity)

#### Structures

- [SceneEvents.TrackingStateUpdate](/documentation/realitykit/sceneevents/trackingstateupdate)

##### Instance Properties

- [let current: SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/current)
- [let previous: SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/previous)

##### Enumerations

- [SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/state)

###### Enumeration Cases

- [case orientationTracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/orientationtracked)
- [case tracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/tracked)
- [case untracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/untracked)
- [Scene.Publisher](/documentation/realitykit/scene/publisher)

### Scene reconstructions and analysis

- [Creating a game with scene understanding](/documentation/realitykit/creating-a-game-with-scene-understanding)
- [Implementing scene understanding and reconstruction in your RealityKit app](/documentation/realitykit/realitykit-scene-understanding)
- [Visualizing and interacting with a reconstructed scene](/documentation/arkit/visualizing-and-interacting-with-a-reconstructed-scene)
- [var sceneReconstruction: ARConfiguration.SceneReconstruction](/documentation/arkit/arworldtrackingconfiguration/scenereconstruction)
- [class func supportsSceneReconstruction(ARConfiguration.SceneReconstruction) -> Bool](/documentation/arkit/arworldtrackingconfiguration/supportsscenereconstruction(_:))
- [SceneUnderstandingComponent](/documentation/realitykit/sceneunderstandingcomponent)

#### Initializing a scene-understanding component

- [init()](/documentation/realitykit/sceneunderstandingcomponent/init())
- [init(entityType: SceneUnderstandingComponent.EntityType?)](/documentation/realitykit/sceneunderstandingcomponent/init(entitytype:))

#### Managing the component

- [var entityType: SceneUnderstandingComponent.EntityType?](/documentation/realitykit/sceneunderstandingcomponent/entitytype-swift.property)
- [SceneUnderstandingComponent.EntityType](/documentation/realitykit/sceneunderstandingcomponent/entitytype-swift.enum)

##### Choosing the entity type

- [case face](/documentation/realitykit/sceneunderstandingcomponent/entitytype-swift.enum/face)
- [case meshChunk](/documentation/realitykit/sceneunderstandingcomponent/entitytype-swift.enum/meshchunk)

#### Instance Properties

- [var origin: SceneUnderstandingComponent.Origin](/documentation/realitykit/sceneunderstandingcomponent/origin-swift.property)

#### Enumerations

- [SceneUnderstandingComponent.Origin](/documentation/realitykit/sceneunderstandingcomponent/origin-swift.enum)

##### Enumeration Cases

- [case system](/documentation/realitykit/sceneunderstandingcomponent/origin-swift.enum/system)
- [case user](/documentation/realitykit/sceneunderstandingcomponent/origin-swift.enum/user)
- [ARView.Environment.SceneUnderstanding](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct)

#### Structures

- [ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct)

##### Type Properties

- [static let collision: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/collision)
- [static let `default`: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/default)
- [static let occlusion: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/occlusion)
- [static let physics: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/physics)
- [static let receivesLighting: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/receiveslighting)

#### Instance Properties

- [var options: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.property)
- [ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct)

#### Type Properties

- [static let collision: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/collision)
- [static let `default`: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/default)
- [static let occlusion: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/occlusion)
- [static let physics: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/physics)
- [static let receivesLighting: ARView.Environment.SceneUnderstanding.Options](/documentation/realitykit/arview/environment-swift.struct/sceneunderstanding-swift.struct/options-swift.struct/receiveslighting)
- [HasSceneUnderstanding](/documentation/realitykit/hassceneunderstanding)

#### Understanding the scene

- [var sceneUnderstanding: SceneUnderstandingComponent](/documentation/realitykit/hassceneunderstanding/sceneunderstanding)
- [SceneReconstructionProvider](/documentation/arkit/scenereconstructionprovider)
- [ARSession](/documentation/arkit/arsession)
- [Systems](/documentation/realitykit/ecs-systems)

### System configuration

- [Implementing systems for entities in a scene](/documentation/realitykit/implementing-systems-for-entities-in-a-scene)
- [Animating entity rotation with a system](/documentation/realitykit/animated-rotation-with-a-system)
- [System](/documentation/realitykit/system)

#### Registering a system

- [static func registerSystem()](/documentation/realitykit/system/registersystem())

#### Specifying dependencies

- [static var dependencies: [SystemDependency]](/documentation/realitykit/system/dependencies)
- [SystemDependency](/documentation/realitykit/systemdependency)

##### Update order

- [case before(any System.Type)](/documentation/realitykit/systemdependency/before(_:))
- [case after(any System.Type)](/documentation/realitykit/systemdependency/after(_:))

##### Operators

- [static func == (SystemDependency, SystemDependency) -> Bool](/documentation/realitykit/systemdependency/==(_:_:))

#### Creating a system

- [init(scene: Scene)](/documentation/realitykit/system/init(scene:))

#### Implementing system logic

- [func update(context: SceneUpdateContext)](/documentation/realitykit/system/update(context:))
- [SceneUpdateContext](/documentation/realitykit/sceneupdatecontext)

##### Updating a scene

- [var scene: Scene](/documentation/realitykit/sceneupdatecontext/scene)
- [var deltaTime: TimeInterval](/documentation/realitykit/sceneupdatecontext/deltatime)

##### Instance Methods

- [func entities(matching: EntityQuery, updatingSystemWhen: SystemUpdateCondition) -> QueryResult<Entity>](/documentation/realitykit/sceneupdatecontext/entities(matching:updatingsystemwhen:))
- [EntityQuery](/documentation/realitykit/entityquery)

##### Creating an entity query

- [init()](/documentation/realitykit/entityquery/init())
- [init(where: QueryPredicate<Entity>)](/documentation/realitykit/entityquery/init(where:))
- [QueryPredicate](/documentation/realitykit/querypredicate)

##### Creating predicates

- [static func has<T>(T.Type) -> QueryPredicate<Entity>](/documentation/realitykit/querypredicate/has(_:))

##### Comparing predicates

- [func ! <Value>(QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/!(_:))
- [func && <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/&&(_:_:))
- [func || <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/__(_:_:))
- [QueryResult](/documentation/realitykit/queryresult)

##### Creating an iterator

- [QueryResult.Iterator](/documentation/realitykit/queryresult/iterator)

###### Advancing the iterator

- [func next() -> Element?](/documentation/realitykit/queryresult/iterator/next())
- [func makeIterator() -> QueryResult<Element>.Iterator](/documentation/realitykit/queryresult/makeiterator())

##### Default Implementations

- [Sequence Implementations](/documentation/realitykit/queryresult/sequence-implementations)

###### Structures

- [QueryResult.Iterator](/documentation/realitykit/queryresult/iterator)

###### Advancing the iterator

- [func next() -> Element?](/documentation/realitykit/queryresult/iterator/next())

###### Instance Methods

- [func makeIterator() -> QueryResult<Element>.Iterator](/documentation/realitykit/queryresult/makeiterator())
- [SystemUpdateCondition](/documentation/realitykit/systemupdatecondition)

#### Type Properties

- [static var rendering: SystemUpdateCondition](/documentation/realitykit/systemupdatecondition/rendering)
- [SceneUpdateContext](/documentation/realitykit/sceneupdatecontext)

#### Updating a scene

- [var scene: Scene](/documentation/realitykit/sceneupdatecontext/scene)
- [var deltaTime: TimeInterval](/documentation/realitykit/sceneupdatecontext/deltatime)

#### Instance Methods

- [func entities(matching: EntityQuery, updatingSystemWhen: SystemUpdateCondition) -> QueryResult<Entity>](/documentation/realitykit/sceneupdatecontext/entities(matching:updatingsystemwhen:))

### Entity queries

- [EntityQuery](/documentation/realitykit/entityquery)

#### Creating an entity query

- [init()](/documentation/realitykit/entityquery/init())
- [init(where: QueryPredicate<Entity>)](/documentation/realitykit/entityquery/init(where:))
- [QueryPredicate](/documentation/realitykit/querypredicate)

#### Creating predicates

- [static func has<T>(T.Type) -> QueryPredicate<Entity>](/documentation/realitykit/querypredicate/has(_:))

#### Comparing predicates

- [func ! <Value>(QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/!(_:))
- [func && <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/&&(_:_:))
- [func || <Value>(QueryPredicate<Value>, QueryPredicate<Value>) -> QueryPredicate<Value>](/documentation/realitykit/__(_:_:))
- [QueryResult](/documentation/realitykit/queryresult)

#### Creating an iterator

- [QueryResult.Iterator](/documentation/realitykit/queryresult/iterator)

##### Advancing the iterator

- [func next() -> Element?](/documentation/realitykit/queryresult/iterator/next())
- [func makeIterator() -> QueryResult<Element>.Iterator](/documentation/realitykit/queryresult/makeiterator())

#### Default Implementations

- [Sequence Implementations](/documentation/realitykit/queryresult/sequence-implementations)

##### Structures

- [QueryResult.Iterator](/documentation/realitykit/queryresult/iterator)

###### Advancing the iterator

- [func next() -> Element?](/documentation/realitykit/queryresult/iterator/next())

##### Instance Methods

- [func makeIterator() -> QueryResult<Element>.Iterator](/documentation/realitykit/queryresult/makeiterator())
- [Events](/documentation/realitykit/ecs-events)

### Core event types

- [Event](/documentation/realitykit/event)
- [EventSource](/documentation/realitykit/eventsource)
- [EventSubscription](/documentation/realitykit/eventsubscription)

#### Instance Methods

- [func cancel()](/documentation/realitykit/eventsubscription/cancel())
- [func subscribe(to: Scene)](/documentation/realitykit/eventsubscription/subscribe(to:))

### Scene and entity lifecycle events

- [SceneEvents](/documentation/realitykit/sceneevents)

#### Detecting scene-level updates

- [SceneEvents.Update](/documentation/realitykit/sceneevents/update)

##### Characterizing an update

- [let scene: Scene](/documentation/realitykit/sceneevents/update/scene)
- [let deltaTime: TimeInterval](/documentation/realitykit/sceneevents/update/deltatime)
- [SceneEvents.AnchoredStateChanged](/documentation/realitykit/sceneevents/anchoredstatechanged)

##### Characterizing an update

- [let anchor: any HasAnchoring](/documentation/realitykit/sceneevents/anchoredstatechanged/anchor)
- [let isAnchored: Bool](/documentation/realitykit/sceneevents/anchoredstatechanged/isanchored)

#### Detecting scene hierarchy changes

- [SceneEvents.DidAddEntity](/documentation/realitykit/sceneevents/didaddentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/didaddentity/entity)
- [SceneEvents.DidReparentEntity](/documentation/realitykit/sceneevents/didreparententity)

##### Instance Properties

- [let child: Entity](/documentation/realitykit/sceneevents/didreparententity/child)
- [let previousParent: Entity?](/documentation/realitykit/sceneevents/didreparententity/previousparent)
- [SceneEvents.WillRemoveEntity](/documentation/realitykit/sceneevents/willremoveentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/willremoveentity/entity)
- [SceneEvents.DidActivateEntity](/documentation/realitykit/sceneevents/didactivateentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/didactivateentity/entity)
- [SceneEvents.WillDeactivateEntity](/documentation/realitykit/sceneevents/willdeactivateentity)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/sceneevents/willdeactivateentity/entity)

#### Structures

- [SceneEvents.TrackingStateUpdate](/documentation/realitykit/sceneevents/trackingstateupdate)

##### Instance Properties

- [let current: SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/current)
- [let previous: SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/previous)

##### Enumerations

- [SceneEvents.TrackingStateUpdate.State](/documentation/realitykit/sceneevents/trackingstateupdate/state)

###### Enumeration Cases

- [case orientationTracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/orientationtracked)
- [case tracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/tracked)
- [case untracked](/documentation/realitykit/sceneevents/trackingstateupdate/state/untracked)
- [AnchorStateEvents](/documentation/realitykit/anchorstateevents)

#### Structures

- [AnchorStateEvents.DidAnchor](/documentation/realitykit/anchorstateevents/didanchor)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/anchorstateevents/didanchor/entity)
- [let reason: AnchorStateEvents.DidAnchor.Reason](/documentation/realitykit/anchorstateevents/didanchor/reason-swift.property)

##### Enumerations

- [AnchorStateEvents.DidAnchor.Reason](/documentation/realitykit/anchorstateevents/didanchor/reason-swift.enum)

###### Enumeration Cases

- [case newAnchor](/documentation/realitykit/anchorstateevents/didanchor/reason-swift.enum/newanchor)
- [case reanchor](/documentation/realitykit/anchorstateevents/didanchor/reason-swift.enum/reanchor)
- [AnchorStateEvents.DidFailToAnchor](/documentation/realitykit/anchorstateevents/didfailtoanchor)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/anchorstateevents/didfailtoanchor/entity)
- [let reason: AnchorStateEvents.DidFailToAnchor.Reason](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.property)

##### Enumerations

- [AnchorStateEvents.DidFailToAnchor.Reason](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.enum)

###### Enumeration Cases

- [case addAnchorFailed](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.enum/addanchorfailed)
- [case anchorNotSupported](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.enum/anchornotsupported)
- [case maximumLimitReached](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.enum/maximumlimitreached)
- [case unspecified](/documentation/realitykit/anchorstateevents/didfailtoanchor/reason-swift.enum/unspecified)
- [AnchorStateEvents.WillUnanchor](/documentation/realitykit/anchorstateevents/willunanchor)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/anchorstateevents/willunanchor/entity)
- [let reason: AnchorStateEvents.WillUnanchor.Reason](/documentation/realitykit/anchorstateevents/willunanchor/reason-swift.property)

##### Enumerations

- [AnchorStateEvents.WillUnanchor.Reason](/documentation/realitykit/anchorstateevents/willunanchor/reason-swift.enum)

###### Enumeration Cases

- [case anchorDisqualified](/documentation/realitykit/anchorstateevents/willunanchor/reason-swift.enum/anchordisqualified)
- [case authorizationFailed](/documentation/realitykit/anchorstateevents/willunanchor/reason-swift.enum/authorizationfailed)
- [ComponentEvents](/documentation/realitykit/componentevents)

#### Detecting component changes

- [ComponentEvents.DidAdd](/documentation/realitykit/componentevents/didadd)

##### Instance Properties

- [let componentType: any Component.Type](/documentation/realitykit/componentevents/didadd/componenttype)
- [let entity: Entity](/documentation/realitykit/componentevents/didadd/entity)
- [ComponentEvents.DidChange](/documentation/realitykit/componentevents/didchange)

##### Instance Properties

- [let componentType: any Component.Type](/documentation/realitykit/componentevents/didchange/componenttype)
- [let entity: Entity](/documentation/realitykit/componentevents/didchange/entity)
- [ComponentEvents.WillRemove](/documentation/realitykit/componentevents/willremove)

##### Instance Properties

- [let componentType: any Component.Type](/documentation/realitykit/componentevents/willremove/componenttype)
- [let entity: Entity](/documentation/realitykit/componentevents/willremove/entity)

#### Detecting component activations

- [ComponentEvents.DidActivate](/documentation/realitykit/componentevents/didactivate)

##### Instance Properties

- [let componentType: any Component.Type](/documentation/realitykit/componentevents/didactivate/componenttype)
- [let entity: Entity](/documentation/realitykit/componentevents/didactivate/entity)
- [ComponentEvents.WillDeactivate](/documentation/realitykit/componentevents/willdeactivate)

##### Instance Properties

- [let componentType: any Component.Type](/documentation/realitykit/componentevents/willdeactivate/componenttype)
- [let entity: Entity](/documentation/realitykit/componentevents/willdeactivate/entity)

### Input and interaction events

- [AccessibilityEvents](/documentation/realitykit/accessibilityevents)

#### Structures

- [AccessibilityEvents.Activate](/documentation/realitykit/accessibilityevents/activate)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/activate/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/activate/entity)
- [AccessibilityEvents.CustomAction](/documentation/realitykit/accessibilityevents/customaction)

##### Initializers

- [init(key: LocalizedStringResource, entity: Entity)](/documentation/realitykit/accessibilityevents/customaction/init(key:entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/customaction/entity)
- [var key: LocalizedStringResource](/documentation/realitykit/accessibilityevents/customaction/key)
- [AccessibilityEvents.Decrement](/documentation/realitykit/accessibilityevents/decrement)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/decrement/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/decrement/entity)
- [AccessibilityEvents.Increment](/documentation/realitykit/accessibilityevents/increment)

##### Initializers

- [init(entity: Entity)](/documentation/realitykit/accessibilityevents/increment/init(entity:))

##### Instance Properties

- [var entity: Entity](/documentation/realitykit/accessibilityevents/increment/entity)
- [AccessibilityEvents.RotorNavigation](/documentation/realitykit/accessibilityevents/rotornavigation)

##### Initializers

- [init(rotorType: AccessibilityComponent.RotorType, hostEntity: Entity, currentItem: Any?, searchDirection: UIAccessibilityCustomRotor.Direction, resultHandler: (Any) -> Void)](/documentation/realitykit/accessibilityevents/rotornavigation/init(rotortype:hostentity:currentitem:searchdirection:resulthandler:))

##### Instance Properties

- [let currentItem: Any?](/documentation/realitykit/accessibilityevents/rotornavigation/currentitem)
- [let hostEntity: Entity](/documentation/realitykit/accessibilityevents/rotornavigation/hostentity)
- [let resultHandler: (Any) -> Void](/documentation/realitykit/accessibilityevents/rotornavigation/resulthandler)
- [let rotorType: AccessibilityComponent.RotorType](/documentation/realitykit/accessibilityevents/rotornavigation/rotortype)
- [let searchDirection: UIAccessibilityCustomRotor.Direction](/documentation/realitykit/accessibilityevents/rotornavigation/searchdirection)
- [ManipulationEvents](/documentation/realitykit/manipulationevents)

#### Detecting manipulation gesture events

- [ManipulationEvents.WillBegin](/documentation/realitykit/manipulationevents/willbegin)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/manipulationevents/willbegin/entity)
- [let inputDeviceSet: ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/willbegin/inputdeviceset)
- [let pivotPoint: Point3DFloat](/documentation/realitykit/manipulationevents/willbegin/pivotpoint)
- [ManipulationEvents.DidUpdateTransform](/documentation/realitykit/manipulationevents/didupdatetransform)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/manipulationevents/didupdatetransform/entity)
- [let inputDeviceSet: ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/didupdatetransform/inputdeviceset)
- [let pivotPoint: Point3DFloat](/documentation/realitykit/manipulationevents/didupdatetransform/pivotpoint)
- [ManipulationEvents.DidHandOff](/documentation/realitykit/manipulationevents/didhandoff)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/manipulationevents/didhandoff/entity)
- [let newInputDeviceSet: ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/didhandoff/newinputdeviceset)
- [let oldInputDeviceSet: ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/didhandoff/oldinputdeviceset)
- [ManipulationEvents.WillRelease](/documentation/realitykit/manipulationevents/willrelease)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/manipulationevents/willrelease/entity)
- [let inputDeviceSet: ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/willrelease/inputdeviceset)
- [let wasCancelled: Bool](/documentation/realitykit/manipulationevents/willrelease/wascancelled)
- [ManipulationEvents.WillEnd](/documentation/realitykit/manipulationevents/willend)

##### Instance Properties

- [let entity: Entity](/documentation/realitykit/manipulationevents/willend/entity)

#### Type Aliases

- [ManipulationEvents.InputDeviceSet](/documentation/realitykit/manipulationevents/inputdeviceset)

### Physics and motion events

- [AnimationEvents](/documentation/realitykit/animationevents)

#### Recognizing animation events

- [AnimationEvents.PlaybackStarted](/documentation/realitykit/animationevents/playbackstarted)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackstarted/playbackcontroller)
- [AnimationEvents.PlaybackCompleted](/documentation/realitykit/animationevents/playbackcompleted)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackcompleted/playbackcontroller)
- [AnimationEvents.PlaybackLooped](/documentation/realitykit/animationevents/playbacklooped)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbacklooped/playbackcontroller)
- [AnimationEvents.PlaybackTerminated](/documentation/realitykit/animationevents/playbackterminated)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackterminated/playbackcontroller)

#### Recognizing skeletal events

- [AnimationEvents.SkeletalPoseUpdateComplete](/documentation/realitykit/animationevents/skeletalposeupdatecomplete)

##### Instance Properties

- [let deltaTime: Float](/documentation/realitykit/animationevents/skeletalposeupdatecomplete/deltatime)
- [CollisionEvents](/documentation/realitykit/collisionevents)

#### Detecting collisions

- [CollisionEvents.Began](/documentation/realitykit/collisionevents/began)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/began/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/began/entityb)

##### Characterizing the collision

- [let impulse: Float](/documentation/realitykit/collisionevents/began/impulse)
- [let position: SIMD3<Float>](/documentation/realitykit/collisionevents/began/position)

##### Instance Properties

- [var contacts: [Contact]](/documentation/realitykit/collisionevents/began/contacts)
- [var impulseDirection: SIMD3<Float>](/documentation/realitykit/collisionevents/began/impulsedirection)
- [var penetrationDistance: Float](/documentation/realitykit/collisionevents/began/penetrationdistance)
- [CollisionEvents.Updated](/documentation/realitykit/collisionevents/updated)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/updated/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/updated/entityb)

##### Characterizing the collision

- [let impulse: Float](/documentation/realitykit/collisionevents/updated/impulse)
- [let position: SIMD3<Float>](/documentation/realitykit/collisionevents/updated/position)

##### Instance Properties

- [var contacts: [Contact]](/documentation/realitykit/collisionevents/updated/contacts)
- [var impulseDirection: SIMD3<Float>](/documentation/realitykit/collisionevents/updated/impulsedirection)
- [var penetrationDistance: Float](/documentation/realitykit/collisionevents/updated/penetrationdistance)
- [CollisionEvents.Ended](/documentation/realitykit/collisionevents/ended)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/ended/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/ended/entityb)
- [PhysicsSimulationEvents](/documentation/realitykit/physicssimulationevents)

#### Structures

- [PhysicsSimulationEvents.DidSimulate](/documentation/realitykit/physicssimulationevents/didsimulate)

##### Instance Properties

- [let deltaTime: TimeInterval](/documentation/realitykit/physicssimulationevents/didsimulate/deltatime)
- [let simulationEntity: Entity](/documentation/realitykit/physicssimulationevents/didsimulate/simulationentity)
- [let simulationRootEntity: Entity?](/documentation/realitykit/physicssimulationevents/didsimulate/simulationrootentity)
- [PhysicsSimulationEvents.WillSimulate](/documentation/realitykit/physicssimulationevents/willsimulate)

##### Instance Properties

- [let deltaTime: TimeInterval](/documentation/realitykit/physicssimulationevents/willsimulate/deltatime)
- [let simulationEntity: Entity](/documentation/realitykit/physicssimulationevents/willsimulate/simulationentity)
- [let simulationRootEntity: Entity?](/documentation/realitykit/physicssimulationevents/willsimulate/simulationrootentity)

### Media events

- [AudioEvents](/documentation/realitykit/audioevents)

#### Recognizing playback completion

- [AudioEvents.PlaybackCompleted](/documentation/realitykit/audioevents/playbackcompleted)

##### Instance Properties

- [var playbackController: AudioPlaybackController](/documentation/realitykit/audioevents/playbackcompleted/playbackcontroller)
- [VideoPlayerEvents](/documentation/realitykit/videoplayerevents)

#### Structures

- [VideoPlayerEvents.ContentTypeDidChange](/documentation/realitykit/videoplayerevents/contenttypedidchange)

##### Instance Properties

- [let contentType: VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.property)
- [let previousType: VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/previoustype)

##### Enumerations

- [VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum)

###### Enumeration Cases

- [case equirectangular](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/equirectangular)
- [case halfEquirectangular](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/halfequirectangular)
- [case immersive](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/immersive)
- [case invalid](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/invalid)
- [case mono](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/mono)
- [case parametricImmersive](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/parametricimmersive)
- [case stereo](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/stereo)
- [VideoPlayerEvents.ImmersiveViewingModeDidChange](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange/previousmode)
- [VideoPlayerEvents.ImmersiveViewingModeDidTransition](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition/previousmode)
- [VideoPlayerEvents.ImmersiveViewingModeWillTransition](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition/previousmode)
- [VideoPlayerEvents.RenderingStatusDidChange](/documentation/realitykit/videoplayerevents/renderingstatusdidchange)

##### Instance Properties

- [let currentStatus: VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayerevents/renderingstatusdidchange/currentstatus)
- [let previousStatus: VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayerevents/renderingstatusdidchange/previousstatus)
- [VideoPlayerEvents.SpatialVideoModeDidChange](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange/currentmode)
- [let previousMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange/previousmode)
- [VideoPlayerEvents.VideoComfortMitigationDidOccur](/documentation/realitykit/videoplayerevents/videocomfortmitigationdidoccur)

##### Instance Properties

- [let comfortMitigation: VideoPlayerComponent.VideoComfortMitigation](/documentation/realitykit/videoplayerevents/videocomfortmitigationdidoccur/comfortmitigation)
- [VideoPlayerEvents.VideoSizeDidChange](/documentation/realitykit/videoplayerevents/videosizedidchange)

##### Instance Properties

- [let screenMeshSize: SIMD2<Float>](/documentation/realitykit/videoplayerevents/videosizedidchange/screenmeshsize)
- [let videoDimension: SIMD2<Float>](/documentation/realitykit/videoplayerevents/videosizedidchange/videodimension)
- [VideoPlayerEvents.ViewingModeDidChange](/documentation/realitykit/videoplayerevents/viewingmodedidchange)

##### Instance Properties

- [let currentViewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplayerevents/viewingmodedidchange/currentviewingmode)
- [let previousViewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplayerevents/viewingmodedidchange/previousviewingmode)
- [ImagePresentationEvents](/documentation/realitykit/imagepresentationevents)

#### Viewing mode transitions

- [ImagePresentationEvents.TransitionStarted](/documentation/realitykit/imagepresentationevents/transitionstarted)

##### Instance Properties

- [let currentViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitionstarted/currentviewingmode)
- [let targetViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitionstarted/targetviewingmode)
- [ImagePresentationEvents.TransitionCompleted](/documentation/realitykit/imagepresentationevents/transitioncompleted)

##### Instance Properties

- [let currentViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitioncompleted/currentviewingmode)
- [let previousViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitioncompleted/previousviewingmode)

### Network synchronization events

- [SynchronizationEvents](/documentation/realitykit/synchronizationevents)

#### Detecting ownership updates

- [SynchronizationEvents.OwnershipChanged](/documentation/realitykit/synchronizationevents/ownershipchanged)

##### Getting the involved parties

- [let entity: Entity](/documentation/realitykit/synchronizationevents/ownershipchanged/entity)
- [let newOwner: (any SynchronizationPeerID)?](/documentation/realitykit/synchronizationevents/ownershipchanged/newowner)
- [SynchronizationEvents.OwnershipRequest](/documentation/realitykit/synchronizationevents/ownershiprequest)

##### Getting the involved parties

- [let entity: Entity](/documentation/realitykit/synchronizationevents/ownershiprequest/entity)
- [let requester: any SynchronizationPeerID](/documentation/realitykit/synchronizationevents/ownershiprequest/requester)

##### Accepting the request

- [let accept: () -> Void](/documentation/realitykit/synchronizationevents/ownershiprequest/accept)
- [Entity actions](/documentation/realitykit/ecs-entity-actions)

### Action management

- [EntityAction](/documentation/realitykit/entityaction)

#### Associated Types

- [EventParameterType](/documentation/realitykit/entityaction/eventparametertype)

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/entityaction/animatedvaluetype)
- [var isAdditive: Bool](/documentation/realitykit/entityaction/isadditive)
- [var isReversible: Bool](/documentation/realitykit/entityaction/isreversible)

#### Type Methods

- [static registerAction()](/documentation/realitykit/entityaction/registeraction())
- [static subscribe(to:_:)](/documentation/realitykit/entityaction/subscribe(to:_:))
- [static func unsubscribe(from: ActionEventType)](/documentation/realitykit/entityaction/unsubscribe(from:))
- [static func unsubscribeAll()](/documentation/realitykit/entityaction/unsubscribeall())
- [ActionAnimation](/documentation/realitykit/actionanimation)

#### Initializers

- [init(for: ActionType, events: [ActionAnimation<ActionType>.EventDefinitionType], name: String, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/actionanimation/init(for:events:name:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Instance Properties

- [var action: ActionType?](/documentation/realitykit/actionanimation/action)
- [var bindTarget: BindTarget](/documentation/realitykit/actionanimation/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/actionanimation/blendlayer)
- [var delay: TimeInterval](/documentation/realitykit/actionanimation/delay)
- [var duration: TimeInterval](/documentation/realitykit/actionanimation/duration)
- [var eventDefinitions: [ActionEventDefinition<ActionType>]](/documentation/realitykit/actionanimation/eventdefinitions)
- [var fillMode: AnimationFillMode](/documentation/realitykit/actionanimation/fillmode)
- [var name: String](/documentation/realitykit/actionanimation/name)
- [var offset: TimeInterval](/documentation/realitykit/actionanimation/offset)
- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/actionanimation/repeatmode)
- [var speed: Float](/documentation/realitykit/actionanimation/speed)
- [var trimDuration: TimeInterval?](/documentation/realitykit/actionanimation/trimduration)
- [var trimEnd: TimeInterval?](/documentation/realitykit/actionanimation/trimend)
- [var trimStart: TimeInterval?](/documentation/realitykit/actionanimation/trimstart)

#### Type Aliases

- [ActionAnimation.EventDefinitionType](/documentation/realitykit/actionanimation/eventdefinitiontype)
- [ActionAnimation.EventParameterType](/documentation/realitykit/actionanimation/eventparametertype)
- [ActionEntityResolution](/documentation/realitykit/actionentityresolution)

#### Operators

- [static func == (ActionEntityResolution, ActionEntityResolution) -> Bool](/documentation/realitykit/actionentityresolution/==(_:_:))

#### Enumeration Cases

- [case entityNamed(String)](/documentation/realitykit/actionentityresolution/entitynamed(_:))
- [case entityPath(BindTarget.EntityPath)](/documentation/realitykit/actionentityresolution/entitypath(_:))

#### Initializers

- [init(from: any Decoder) throws](/documentation/realitykit/actionentityresolution/init(from:))

#### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/realitykit/actionentityresolution/encode(to:))

#### Type Properties

- [static var sourceEntity: ActionEntityResolution](/documentation/realitykit/actionentityresolution/sourceentity)
- [ActionHandlerProtocol](/documentation/realitykit/actionhandlerprotocol)

#### Associated Types

- [ActionType](/documentation/realitykit/actionhandlerprotocol/actiontype)

#### Instance Methods

- [func actionEnded(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionended(event:))
- [func actionPaused(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionpaused(event:))
- [func actionResumed(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionresumed(event:))
- [func actionSkipped(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionskipped(event:))
- [func actionStarted(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionstarted(event:))
- [func actionTerminated(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionterminated(event:))
- [func actionUpdated(event: Self.EventType)](/documentation/realitykit/actionhandlerprotocol/actionupdated(event:))

#### Type Aliases

- [ActionHandlerProtocol.EventType](/documentation/realitykit/actionhandlerprotocol/eventtype)

#### Type Methods

- [static func register((Self.EventType) -> (any ActionHandlerProtocol)?)](/documentation/realitykit/actionhandlerprotocol/register(_:))

### Action events

- [ActionEvent](/documentation/realitykit/actionevent)

#### Instance Properties

- [let action: ActionType](/documentation/realitykit/actionevent/action)
- [var animationState: (any AnimationStateProtocol)?](/documentation/realitykit/actionevent/animationstate)
- [let duration: TimeInterval](/documentation/realitykit/actionevent/duration)
- [let parameter: ActionType.EventParameterType?](/documentation/realitykit/actionevent/parameter)
- [let playbackController: AnimationPlaybackController](/documentation/realitykit/actionevent/playbackcontroller)
- [let reversed: Bool](/documentation/realitykit/actionevent/reversed)
- [let startTime: TimeInterval](/documentation/realitykit/actionevent/starttime)
- [let targetEntity: Entity?](/documentation/realitykit/actionevent/targetentity)
- [AnimationState](/documentation/realitykit/animationstate)

#### Instance Properties

- [var defaultSource: Value?](/documentation/realitykit/animationstate/defaultsource-3pn6r)
- [var defaultSource: JointTransforms?](/documentation/realitykit/animationstate/defaultsource-5ddek)
- [var defaultTarget: JointTransforms?](/documentation/realitykit/animationstate/defaulttarget-9kxlt)
- [var defaultTarget: Value?](/documentation/realitykit/animationstate/defaulttarget-gdi6)
- [let deltaTime: TimeInterval](/documentation/realitykit/animationstate/deltatime)
- [let evaluationTime: TimeInterval](/documentation/realitykit/animationstate/evaluationtime)
- [let normalizedTime: TimeInterval](/documentation/realitykit/animationstate/normalizedtime)

#### Instance Methods

- [func defaultSourceJoints(index: Int, count: Int, transforms: inout [Transform]) -> Bool](/documentation/realitykit/animationstate/defaultsourcejoints(index:count:transforms:))
- [func defaultTargetJoints(index: Int, count: Int, transforms: inout [Transform]) -> Bool](/documentation/realitykit/animationstate/defaulttargetjoints(index:count:transforms:))
- [func storeAnimatedJoints(transforms: [Transform], jointIndex: Int) -> Bool](/documentation/realitykit/animationstate/storeanimatedjoints(transforms:jointindex:))
- [func storeAnimatedValue<ValueType>(ValueType) -> Bool](/documentation/realitykit/animationstate/storeanimatedvalue(_:))
- [ActionEventType](/documentation/realitykit/actioneventtype)

#### Event types

- [static var started: ActionEventType](/documentation/realitykit/actioneventtype/started)
- [static var ended: ActionEventType](/documentation/realitykit/actioneventtype/ended)
- [static var paused: ActionEventType](/documentation/realitykit/actioneventtype/paused)
- [static var resumed: ActionEventType](/documentation/realitykit/actioneventtype/resumed)
- [static var updated: ActionEventType](/documentation/realitykit/actioneventtype/updated)
- [static var skipped: ActionEventType](/documentation/realitykit/actioneventtype/skipped)
- [static var terminated: ActionEventType](/documentation/realitykit/actioneventtype/terminated)

#### Protocol support

- [init(rawValue: UInt)](/documentation/realitykit/actioneventtype/init(rawvalue:))
- [let rawValue: UInt](/documentation/realitykit/actioneventtype/rawvalue)
- [ActionEventDefinition](/documentation/realitykit/actioneventdefinition)

#### Initializers

- [init(startTime: TimeInterval, duration: TimeInterval, parameter: ActionEventDefinition<ActionType>.EventParameterType?)](/documentation/realitykit/actioneventdefinition/init(starttime:duration:parameter:))

#### Instance Properties

- [var duration: TimeInterval](/documentation/realitykit/actioneventdefinition/duration)
- [var parameter: ActionEventDefinition<ActionType>.EventParameterType?](/documentation/realitykit/actioneventdefinition/parameter)
- [var startTime: TimeInterval](/documentation/realitykit/actioneventdefinition/starttime)

#### Type Aliases

- [ActionEventDefinition.EventParameterType](/documentation/realitykit/actioneventdefinition/eventparametertype)
- [AnimationStateProtocol](/documentation/realitykit/animationstateprotocol)

#### Associated Types

- [ValueType](/documentation/realitykit/animationstateprotocol/valuetype)

#### Instance Properties

- [var defaultSource: Self.ValueType?](/documentation/realitykit/animationstateprotocol/defaultsource)
- [var defaultTarget: Self.ValueType?](/documentation/realitykit/animationstateprotocol/defaulttarget)
- [var deltaTime: TimeInterval](/documentation/realitykit/animationstateprotocol/deltatime)
- [var evaluationTime: TimeInterval](/documentation/realitykit/animationstateprotocol/evaluationtime)
- [var normalizedTime: TimeInterval](/documentation/realitykit/animationstateprotocol/normalizedtime)

#### Instance Methods

- [func storeAnimatedValue<ValueType>(ValueType) -> Bool](/documentation/realitykit/animationstateprotocol/storeanimatedvalue(_:))

### Built-in actions

- [BillboardAction](/documentation/realitykit/billboardaction)

#### Structures

- [BillboardAction.Transition](/documentation/realitykit/billboardaction/transition)

##### Initializers

- [init(duration: TimeInterval, timingFunction: AnimationTimingFunction)](/documentation/realitykit/billboardaction/transition/init(duration:timingfunction:))

##### Instance Properties

- [var duration: TimeInterval](/documentation/realitykit/billboardaction/transition/duration)
- [var timingFunction: AnimationTimingFunction](/documentation/realitykit/billboardaction/transition/timingfunction)

#### Initializers

- [init(transitionIn: BillboardAction.Transition, transitionOut: BillboardAction.Transition)](/documentation/realitykit/billboardaction/init(transitionin:transitionout:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/billboardaction/animatedvaluetype)
- [var transitionIn: BillboardAction.Transition](/documentation/realitykit/billboardaction/transitionin)
- [var transitionOut: BillboardAction.Transition](/documentation/realitykit/billboardaction/transitionout)
- [EmphasizeAction](/documentation/realitykit/emphasizeaction)

#### Initializers

- [init(motionType: EmphasizeAction.EmphasisMotionType, style: EmphasizeAction.EmphasisAnimationStyle, isAdditive: Bool)](/documentation/realitykit/emphasizeaction/init(motiontype:style:isadditive:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/emphasizeaction/animatedvaluetype)
- [var isAdditive: Bool](/documentation/realitykit/emphasizeaction/isadditive)
- [var motionType: EmphasizeAction.EmphasisMotionType](/documentation/realitykit/emphasizeaction/motiontype)
- [var style: EmphasizeAction.EmphasisAnimationStyle](/documentation/realitykit/emphasizeaction/style)

#### Enumerations

- [EmphasizeAction.EmphasisAnimationStyle](/documentation/realitykit/emphasizeaction/emphasisanimationstyle)

##### Enumeration Cases

- [case basic](/documentation/realitykit/emphasizeaction/emphasisanimationstyle/basic)
- [case playful](/documentation/realitykit/emphasizeaction/emphasisanimationstyle/playful)
- [case wild](/documentation/realitykit/emphasizeaction/emphasisanimationstyle/wild)
- [EmphasizeAction.EmphasisMotionType](/documentation/realitykit/emphasizeaction/emphasismotiontype)

##### Enumeration Cases

- [case blink](/documentation/realitykit/emphasizeaction/emphasismotiontype/blink)
- [case bounce](/documentation/realitykit/emphasizeaction/emphasismotiontype/bounce)
- [case flip](/documentation/realitykit/emphasizeaction/emphasismotiontype/flip)
- [case float](/documentation/realitykit/emphasizeaction/emphasismotiontype/float)
- [case jiggle](/documentation/realitykit/emphasizeaction/emphasismotiontype/jiggle)
- [case pop](/documentation/realitykit/emphasizeaction/emphasismotiontype/pop)
- [case pulse](/documentation/realitykit/emphasizeaction/emphasismotiontype/pulse)
- [case spin](/documentation/realitykit/emphasizeaction/emphasismotiontype/spin)
- [FromToByAction](/documentation/realitykit/fromtobyaction)

#### Initializers

- [init(by: Value, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(by:timing:isadditive:))
- [init(from: Value, by: Value?, mode: FromToByAction<Value>.TransformMode, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(from:by:mode:timing:isadditive:))
- [init(from: Value?, by: Value, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(from:by:timing:isadditive:))
- [init(from: Value, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(from:timing:isadditive:))
- [init(from: Value?, to: Value, mode: FromToByAction<Value>.TransformMode, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(from:to:mode:timing:isadditive:))
- [init(from: Value?, to: Value, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(from:to:timing:isadditive:))
- [init(to: Value, by: Value, mode: FromToByAction<Value>.TransformMode, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(to:by:mode:timing:isadditive:))
- [init(to: Value, by: Value, timing: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/fromtobyaction/init(to:by:timing:isadditive:))

#### Instance Properties

- [let animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/fromtobyaction/animatedvaluetype)
- [let by: Value?](/documentation/realitykit/fromtobyaction/by)
- [let from: Value?](/documentation/realitykit/fromtobyaction/from)
- [var isAdditive: Bool](/documentation/realitykit/fromtobyaction/isadditive)
- [let isReversible: Bool](/documentation/realitykit/fromtobyaction/isreversible)
- [var mode: FromToByAction<Transform>.TransformMode?](/documentation/realitykit/fromtobyaction/mode)
- [var timingFunction: AnimationTimingFunction](/documentation/realitykit/fromtobyaction/timingfunction)
- [let to: Value?](/documentation/realitykit/fromtobyaction/to)

#### Enumerations

- [FromToByAction.DecodingErrors](/documentation/realitykit/fromtobyaction/decodingerrors)

##### Enumeration Cases

- [case unsupportedValueType](/documentation/realitykit/fromtobyaction/decodingerrors/unsupportedvaluetype)
- [FromToByAction.TransformMode](/documentation/realitykit/fromtobyaction/transformmode)

##### Enumeration Cases

- [case local](/documentation/realitykit/fromtobyaction/transformmode/local)
- [case parent](/documentation/realitykit/fromtobyaction/transformmode/parent)
- [case relative(to: ActionEntityResolution)](/documentation/realitykit/fromtobyaction/transformmode/relative(to:))
- [case scene](/documentation/realitykit/fromtobyaction/transformmode/scene)

##### Type Properties

- [static var `default`: FromToByAction<Value>.TransformMode](/documentation/realitykit/fromtobyaction/transformmode/default)

#### Default Implementations

- [Decodable Implementations](/documentation/realitykit/fromtobyaction/decodable-implementations)

##### Initializers

- [init(from: any Decoder) throws](/documentation/realitykit/fromtobyaction/init(from:))
- [Encodable Implementations](/documentation/realitykit/fromtobyaction/encodable-implementations)

##### Instance Methods

- [func encode(to: any Encoder) throws](/documentation/realitykit/fromtobyaction/encode(to:))
- [ImpulseAction](/documentation/realitykit/impulseaction)

#### Initializers

- [init(targetEntity: ActionEntityResolution, linearImpulse: SIMD3<Float>)](/documentation/realitykit/impulseaction/init(targetentity:linearimpulse:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/impulseaction/animatedvaluetype)
- [var linearImpulse: SIMD3<Float>](/documentation/realitykit/impulseaction/linearimpulse)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/impulseaction/targetentity)
- [OrbitEntityAction](/documentation/realitykit/orbitentityaction)

#### Initializers

- [init(pivotEntity: ActionEntityResolution, revolutions: Float, orbitalAxis: SIMD3<Float>, isOrientedToPath: Bool, isAdditive: Bool)](/documentation/realitykit/orbitentityaction/init(pivotentity:revolutions:orbitalaxis:isorientedtopath:isadditive:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/orbitentityaction/animatedvaluetype)
- [var isAdditive: Bool](/documentation/realitykit/orbitentityaction/isadditive)
- [var isOrientedToPath: Bool](/documentation/realitykit/orbitentityaction/isorientedtopath)
- [var orbitalAxis: SIMD3<Float>](/documentation/realitykit/orbitentityaction/orbitalaxis)
- [var pivotEntity: ActionEntityResolution](/documentation/realitykit/orbitentityaction/pivotentity)
- [var revolutions: Float](/documentation/realitykit/orbitentityaction/revolutions)
- [PlayAnimationAction](/documentation/realitykit/playanimationaction)

#### Initializers

- [init(animationName: String, targetEntity: ActionEntityResolution, transitionDuration: TimeInterval, blendLayer: Int, separateAnimatedValue: Bool, useParentedControllers: Bool, handoffType: AnimationHandoffType)](/documentation/realitykit/playanimationaction/init(animationname:targetentity:transitionduration:blendlayer:separateanimatedvalue:useparentedcontrollers:handofftype:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/playanimationaction/animatedvaluetype)
- [var animationName: String](/documentation/realitykit/playanimationaction/animationname)
- [var blendLayer: Int](/documentation/realitykit/playanimationaction/blendlayer)
- [var handoffType: AnimationHandoffType](/documentation/realitykit/playanimationaction/handofftype)
- [var separateAnimatedValue: Bool](/documentation/realitykit/playanimationaction/separateanimatedvalue)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/playanimationaction/targetentity)
- [var transitionDuration: TimeInterval](/documentation/realitykit/playanimationaction/transitionduration)
- [var useParentedControllers: Bool](/documentation/realitykit/playanimationaction/useparentedcontrollers)
- [PlayAudioAction](/documentation/realitykit/playaudioaction)

#### Initializers

- [init(targetEntity: ActionEntityResolution, audioResourceName: String, gain: Audio.Decibel, useControlledPlayback: Bool)](/documentation/realitykit/playaudioaction/init(targetentity:audioresourcename:gain:usecontrolledplayback:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/playaudioaction/animatedvaluetype)
- [var audioResourceName: String](/documentation/realitykit/playaudioaction/audioresourcename)
- [var gain: Audio.Decibel](/documentation/realitykit/playaudioaction/gain)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/playaudioaction/targetentity)
- [var useControlledPlayback: Bool](/documentation/realitykit/playaudioaction/usecontrolledplayback)
- [SetEntityEnabledAction](/documentation/realitykit/setentityenabledaction)

#### Initializers

- [init(targetEntity: ActionEntityResolution, isEnabled: Bool)](/documentation/realitykit/setentityenabledaction/init(targetentity:isenabled:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/setentityenabledaction/animatedvaluetype)
- [var isEnabled: Bool](/documentation/realitykit/setentityenabledaction/isenabled)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/setentityenabledaction/targetentity)
- [SpinAction](/documentation/realitykit/spinaction)

#### Initializers

- [init(revolutions: Float, localAxis: SIMD3<Float>, timingFunction: AnimationTimingFunction, isAdditive: Bool)](/documentation/realitykit/spinaction/init(revolutions:localaxis:timingfunction:isadditive:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/spinaction/animatedvaluetype)
- [var isAdditive: Bool](/documentation/realitykit/spinaction/isadditive)
- [var localAxis: SIMD3<Float>](/documentation/realitykit/spinaction/localaxis)
- [var revolutions: Float](/documentation/realitykit/spinaction/revolutions)
- [var timingFunction: AnimationTimingFunction](/documentation/realitykit/spinaction/timingfunction)

## Asset creation

- [Reality Composer Pro](/documentation/realitycomposerpro)
- [Swift Splash](/documentation/visionos/swift-splash)
- [Diorama](/documentation/visionos/diorama)
- [Presenting an artist’s scene](/documentation/realitykit/presenting-an-artists-scene)
- [Object capture](/documentation/realitykit/realitykit-object-capture)

### Model creation

- [Capturing photographs for RealityKit Object Capture](/documentation/realitykit/capturing-photographs-for-realitykit-object-capture)
- [Creating 3D objects from photographs](/documentation/realitykit/creating-3d-objects-from-photographs)
- [Scanning objects using Object Capture](/documentation/realitykit/scanning-objects-using-object-capture)
- [Building an object reconstruction app](/documentation/realitykit/building-an-object-reconstruction-app)
- [Creating a photogrammetry command-line app](/documentation/realitykit/creating-a-photogrammetry-command-line-app)
- [Using object capture assets in RealityKit](/documentation/realitykit/using-object-capture-assets-in-realitykit)
- [PhotogrammetrySession](/documentation/realitykit/photogrammetrysession)

#### Creating the session

- [convenience init(input: URL, configuration: PhotogrammetrySession.Configuration) throws](/documentation/realitykit/photogrammetrysession/init(input:configuration:)-wo4e)
- [convenience init<S>(input: S, configuration: PhotogrammetrySession.Configuration) throws](/documentation/realitykit/photogrammetrysession/init(input:configuration:)-7glmh)
- [static var isSupported: Bool](/documentation/realitykit/photogrammetrysession/issupported)

#### Configuring the session

- [var configuration: PhotogrammetrySession.Configuration](/documentation/realitykit/photogrammetrysession/configuration-swift.property)
- [PhotogrammetrySession.Configuration](/documentation/realitykit/photogrammetrysession/configuration-swift.struct)

##### Creating a configuration

- [init()](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/init())

##### Configuring object masking

- [var isObjectMaskingEnabled: Bool](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/isobjectmaskingenabled)

##### Configuring sample ordering

- [var sampleOrdering: PhotogrammetrySession.Configuration.SampleOrdering](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/sampleordering-swift.property)
- [PhotogrammetrySession.Configuration.SampleOrdering](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/sampleordering-swift.enum)

###### Specifying sample ordering

- [case unordered](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/sampleordering-swift.enum/unordered)
- [case sequential](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/sampleordering-swift.enum/sequential)

##### Configuring feature sensitivity

- [var featureSensitivity: PhotogrammetrySession.Configuration.FeatureSensitivity](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/featuresensitivity-swift.property)
- [PhotogrammetrySession.Configuration.FeatureSensitivity](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/featuresensitivity-swift.enum)

###### Specifying feature sensitivity

- [case normal](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/featuresensitivity-swift.enum/normal)
- [case high](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/featuresensitivity-swift.enum/high)

##### Structures

- [PhotogrammetrySession.Configuration.CustomDetailSpecification](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct)

###### Structures

- [PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs)

###### Type Properties

- [static let all: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/all)
- [static let ambientOcclusion: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/ambientocclusion)
- [static let diffuseColor: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/diffusecolor)
- [static let displacement: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/displacement)
- [static let normal: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/normal)
- [static let roughness: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturemapoutputs/roughness)

###### Initializers

- [init()](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/init())

###### Instance Properties

- [var maximumPolygonCount: UInt](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/maximumpolygoncount)
- [var maximumTextureDimension: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureDimension](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/maximumtexturedimension)
- [var outputTextureMaps: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureMapOutputs](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/outputtexturemaps)
- [var textureFormat: PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureFormat](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/textureformat-swift.property)

###### Enumerations

- [PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureDimension](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension)

###### Enumeration Cases

- [case eightK](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension/eightk)
- [case fourK](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension/fourk)
- [case oneK](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension/onek)
- [case sixteenK](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension/sixteenk)
- [case twoK](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/texturedimension/twok)
- [PhotogrammetrySession.Configuration.CustomDetailSpecification.TextureFormat](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/textureformat-swift.enum)

###### Enumeration Cases

- [case jpeg(compressionQuality: Float)](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/textureformat-swift.enum/jpeg(compressionquality:))
- [case png](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.struct/textureformat-swift.enum/png)

##### Initializers

- [init(checkpointDirectory: URL)](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/init(checkpointdirectory:))

##### Instance Properties

- [var checkpointDirectory: URL?](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/checkpointdirectory)
- [var customDetailSpecification: PhotogrammetrySession.Configuration.CustomDetailSpecification](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/customdetailspecification-swift.property)
- [var ignoreBoundingBox: Bool](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/ignoreboundingbox)
- [var meshPrimitive: PhotogrammetrySession.Configuration.MeshPrimitive](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/meshprimitive-swift.property)

##### Enumerations

- [PhotogrammetrySession.Configuration.MeshPrimitive](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/meshprimitive-swift.enum)

###### Enumeration Cases

- [case quad](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/meshprimitive-swift.enum/quad)
- [case triangle](/documentation/realitykit/photogrammetrysession/configuration-swift.struct/meshprimitive-swift.enum/triangle)

#### Monitoring the session

- [var activeRequests: [PhotogrammetrySession.Request]](/documentation/realitykit/photogrammetrysession/activerequests)
- [var isProcessing: Bool](/documentation/realitykit/photogrammetrysession/isprocessing)
- [var outputs: PhotogrammetrySession.Outputs](/documentation/realitykit/photogrammetrysession/outputs-swift.property)
- [PhotogrammetrySession.Output](/documentation/realitykit/photogrammetrysession/output)

##### Monitoring session status

- [case inputComplete](/documentation/realitykit/photogrammetrysession/output/inputcomplete)
- [case processingComplete](/documentation/realitykit/photogrammetrysession/output/processingcomplete)
- [case processingCancelled](/documentation/realitykit/photogrammetrysession/output/processingcancelled)

##### Monitoring request status

- [case requestProgress(PhotogrammetrySession.Request, fractionComplete: Double)](/documentation/realitykit/photogrammetrysession/output/requestprogress(_:fractioncomplete:))
- [case requestComplete(PhotogrammetrySession.Request, PhotogrammetrySession.Result)](/documentation/realitykit/photogrammetrysession/output/requestcomplete(_:_:))
- [case requestError(PhotogrammetrySession.Request, any Error)](/documentation/realitykit/photogrammetrysession/output/requesterror(_:_:))

##### Monitoring data ingestion

- [case invalidSample(id: Int, reason: String)](/documentation/realitykit/photogrammetrysession/output/invalidsample(id:reason:))
- [case automaticDownsampling](/documentation/realitykit/photogrammetrysession/output/automaticdownsampling)
- [case skippedSample(id: Int)](/documentation/realitykit/photogrammetrysession/output/skippedsample(id:))

##### Describing updates

- [var localizedDescription: String](/documentation/realitykit/photogrammetrysession/output/localizeddescription)

##### Iterating outputs

- [PhotogrammetrySession.Outputs](/documentation/realitykit/photogrammetrysession/outputs-swift.struct)

###### Iterating the collection

- [func makeAsyncIterator() -> PhotogrammetrySession.Outputs.Iterator](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/makeasynciterator())

###### Structures

- [PhotogrammetrySession.Outputs.Iterator](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/iterator)

###### Type Aliases

- [PhotogrammetrySession.Outputs.Element](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/element)

##### Structures

- [PhotogrammetrySession.Output.ProgressInfo](/documentation/realitykit/photogrammetrysession/output/progressinfo)

###### Instance Properties

- [let estimatedRemainingTime: TimeInterval?](/documentation/realitykit/photogrammetrysession/output/progressinfo/estimatedremainingtime)
- [let processingStage: PhotogrammetrySession.Output.ProcessingStage?](/documentation/realitykit/photogrammetrysession/output/progressinfo/processingstage)

##### Enumeration Cases

- [case requestProgressInfo(PhotogrammetrySession.Request, PhotogrammetrySession.Output.ProgressInfo)](/documentation/realitykit/photogrammetrysession/output/requestprogressinfo(_:_:))
- [case stitchingIncomplete](/documentation/realitykit/photogrammetrysession/output/stitchingincomplete)

##### Enumerations

- [PhotogrammetrySession.Output.ProcessingStage](/documentation/realitykit/photogrammetrysession/output/processingstage)

###### Enumeration Cases

- [case imageAlignment](/documentation/realitykit/photogrammetrysession/output/processingstage/imagealignment)
- [case meshGeneration](/documentation/realitykit/photogrammetrysession/output/processingstage/meshgeneration)
- [case optimization](/documentation/realitykit/photogrammetrysession/output/processingstage/optimization)
- [case pointCloudGeneration](/documentation/realitykit/photogrammetrysession/output/processingstage/pointcloudgeneration)
- [case preProcessing](/documentation/realitykit/photogrammetrysession/output/processingstage/preprocessing)
- [case textureMapping](/documentation/realitykit/photogrammetrysession/output/processingstage/texturemapping)

#### Controlling object creation

- [func process(requests: [PhotogrammetrySession.Request]) throws](/documentation/realitykit/photogrammetrysession/process(requests:))
- [func cancel()](/documentation/realitykit/photogrammetrysession/cancel())

#### Creating requests

- [PhotogrammetrySession.Request](/documentation/realitykit/photogrammetrysession/request)

##### Creating the request

- [init(modelFile: URL)](/documentation/realitykit/photogrammetrysession/request/init(modelfile:))

##### Specifying the output

- [case modelFile(url: URL, detail: PhotogrammetrySession.Request.Detail, geometry: PhotogrammetrySession.Request.Geometry?)](/documentation/realitykit/photogrammetrysession/request/modelfile(url:detail:geometry:))
- [case modelEntity(detail: PhotogrammetrySession.Request.Detail, geometry: PhotogrammetrySession.Request.Geometry?)](/documentation/realitykit/photogrammetrysession/request/modelentity(detail:geometry:))
- [case bounds](/documentation/realitykit/photogrammetrysession/request/bounds)
- [PhotogrammetrySession.Request.Detail](/documentation/realitykit/photogrammetrysession/request/detail)

###### Specifying a level of detail

- [case preview](/documentation/realitykit/photogrammetrysession/request/detail/preview)
- [case reduced](/documentation/realitykit/photogrammetrysession/request/detail/reduced)
- [case medium](/documentation/realitykit/photogrammetrysession/request/detail/medium)
- [case full](/documentation/realitykit/photogrammetrysession/request/detail/full)
- [case raw](/documentation/realitykit/photogrammetrysession/request/detail/raw)

###### Enumeration Cases

- [case custom](/documentation/realitykit/photogrammetrysession/request/detail/custom)

##### Transforming the created model

- [PhotogrammetrySession.Request.Geometry](/documentation/realitykit/photogrammetrysession/request/geometry)

###### Creating a geometry instance

- [init(bounds: BoundingBox, transform: Transform)](/documentation/realitykit/photogrammetrysession/request/geometry/init(bounds:transform:))

###### Accessing geometry data

- [var bounds: BoundingBox](/documentation/realitykit/photogrammetrysession/request/geometry/bounds)
- [var transform: Transform](/documentation/realitykit/photogrammetrysession/request/geometry/transform)

###### Initializers

- [init(orientedBounds: OrientedBoundingBox, transform: Transform)](/documentation/realitykit/photogrammetrysession/request/geometry/init(orientedbounds:transform:))

###### Instance Properties

- [var orientedBounds: OrientedBoundingBox](/documentation/realitykit/photogrammetrysession/request/geometry/orientedbounds)

##### Enumeration Cases

- [case pointCloud](/documentation/realitykit/photogrammetrysession/request/pointcloud)
- [case poses](/documentation/realitykit/photogrammetrysession/request/poses)

#### Obtaining results

- [PhotogrammetrySession.Result](/documentation/realitykit/photogrammetrysession/result)

##### Types of output

- [case modelFile(URL)](/documentation/realitykit/photogrammetrysession/result/modelfile(_:))
- [case modelEntity(ModelEntity)](/documentation/realitykit/photogrammetrysession/result/modelentity(_:))
- [case bounds(BoundingBox)](/documentation/realitykit/photogrammetrysession/result/bounds(_:))

##### Enumeration Cases

- [case pointCloud(PhotogrammetrySession.PointCloud)](/documentation/realitykit/photogrammetrysession/result/pointcloud(_:))
- [case poses(PhotogrammetrySession.Poses)](/documentation/realitykit/photogrammetrysession/result/poses(_:))
- [PhotogrammetrySession.PointCloud](/documentation/realitykit/photogrammetrysession/pointcloud)

##### Structures

- [PhotogrammetrySession.PointCloud.Point](/documentation/realitykit/photogrammetrysession/pointcloud/point)

###### Instance Properties

- [let color: SIMD4<UInt8>](/documentation/realitykit/photogrammetrysession/pointcloud/point/color)
- [let position: SIMD3<Float>](/documentation/realitykit/photogrammetrysession/pointcloud/point/position)

##### Instance Properties

- [let points: [PhotogrammetrySession.PointCloud.Point]](/documentation/realitykit/photogrammetrysession/pointcloud/points)
- [PhotogrammetrySession.Error](/documentation/realitykit/photogrammetrysession/error)

##### Enumeration Cases

- [case insufficientStorage(requiredBytes: Int64)](/documentation/realitykit/photogrammetrysession/error/insufficientstorage(requiredbytes:))
- [case invalidImages(URL)](/documentation/realitykit/photogrammetrysession/error/invalidimages(_:))
- [case invalidOutput(URL)](/documentation/realitykit/photogrammetrysession/error/invalidoutput(_:))

##### Instance Properties

- [var localizedDescription: String](/documentation/realitykit/photogrammetrysession/error/localizeddescription)
- [PhotogrammetrySession.Pose](/documentation/realitykit/photogrammetrysession/pose)

##### Instance Properties

- [var intrinsics: simd_float3x3?](/documentation/realitykit/photogrammetrysession/pose/intrinsics)
- [var lensDistortionData: LensDistortionData?](/documentation/realitykit/photogrammetrysession/pose/lensdistortiondata)
- [let rotation: simd_quatf](/documentation/realitykit/photogrammetrysession/pose/rotation)
- [var transform: Transform](/documentation/realitykit/photogrammetrysession/pose/transform)
- [let translation: SIMD3<Float>](/documentation/realitykit/photogrammetrysession/pose/translation)
- [PhotogrammetrySession.Poses](/documentation/realitykit/photogrammetrysession/poses)

##### Instance Properties

- [let posesBySample: [Int : PhotogrammetrySession.Pose]](/documentation/realitykit/photogrammetrysession/poses/posesbysample)
- [var urlsBySample: [Int : URL]](/documentation/realitykit/photogrammetrysession/poses/urlsbysample)

#### Structures

- [PhotogrammetrySession.Limits](/documentation/realitykit/photogrammetrysession/limits-swift.struct)

##### Instance Properties

- [var maximumInputImageDimension: Int](/documentation/realitykit/photogrammetrysession/limits-swift.struct/maximuminputimagedimension)
- [var maximumNumberOfInputImages: Int](/documentation/realitykit/photogrammetrysession/limits-swift.struct/maximumnumberofinputimages)
- [PhotogrammetrySession.Outputs](/documentation/realitykit/photogrammetrysession/outputs-swift.struct)

##### Iterating the collection

- [func makeAsyncIterator() -> PhotogrammetrySession.Outputs.Iterator](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/makeasynciterator())

##### Structures

- [PhotogrammetrySession.Outputs.Iterator](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/iterator)

##### Type Aliases

- [PhotogrammetrySession.Outputs.Element](/documentation/realitykit/photogrammetrysession/outputs-swift.struct/element)

#### Initializers

- [convenience(input:configuration:)](/documentation/realitykit/photogrammetrysession/init(input:configuration:))

#### Type Properties

- [static let limits: PhotogrammetrySession.Limits](/documentation/realitykit/photogrammetrysession/limits-swift.type.property)
- [PhotogrammetrySample](/documentation/realitykit/photogrammetrysample)

#### Creating a sample

- [init(id: Int, image: CVPixelBuffer)](/documentation/realitykit/photogrammetrysample/init(id:image:))

#### Describing the sample

- [let image: CVPixelBuffer](/documentation/realitykit/photogrammetrysample/image)
- [var metadata: [String : Any]](/documentation/realitykit/photogrammetrysample/metadata)
- [var depthDataMap: CVPixelBuffer?](/documentation/realitykit/photogrammetrysample/depthdatamap)
- [var gravity: CMAcceleration?](/documentation/realitykit/photogrammetrysample/gravity)
- [var objectMask: CVPixelBuffer?](/documentation/realitykit/photogrammetrysample/objectmask)

#### Structures

- [PhotogrammetrySample.Camera](/documentation/realitykit/photogrammetrysample/camera-swift.struct)

##### Instance Properties

- [var calibrationData: AVCameraCalibrationData?](/documentation/realitykit/photogrammetrysample/camera-swift.struct/calibrationdata)
- [var id: UInt32](/documentation/realitykit/photogrammetrysample/camera-swift.struct/id)
- [var intrinsics: simd_float3x3](/documentation/realitykit/photogrammetrysample/camera-swift.struct/intrinsics)
- [var transform: simd_float4x4](/documentation/realitykit/photogrammetrysample/camera-swift.struct/transform)

#### Initializers

- [init(contentsOf:)](/documentation/realitykit/photogrammetrysample/init(contentsof:))

#### Instance Properties

- [var boundingBox: simd_float4x4?](/documentation/realitykit/photogrammetrysample/boundingbox)
- [var camera: PhotogrammetrySample.Camera?](/documentation/realitykit/photogrammetrysample/camera-swift.property)
- [var captureTime: Date?](/documentation/realitykit/photogrammetrysample/capturetime)
- [var depthConfidenceMap: CVPixelBuffer?](/documentation/realitykit/photogrammetrysample/depthconfidencemap)
- [let id: Int](/documentation/realitykit/photogrammetrysample/id)
- [var orientation: CGImagePropertyOrientation](/documentation/realitykit/photogrammetrysample/orientation)
- [var scanPassID: Int?](/documentation/realitykit/photogrammetrysample/scanpassid)
- [var sessionID: UUID?](/documentation/realitykit/photogrammetrysample/sessionid)
- [ObjectCaptureView](/documentation/realitykit/objectcaptureview)

#### Initializers

- [init(session: ObjectCaptureSession)](/documentation/realitykit/objectcaptureview/init(session:))
- [init(session: ObjectCaptureSession, cameraFeedOverlay: () -> Overlay)](/documentation/realitykit/objectcaptureview/init(session:camerafeedoverlay:))

#### Instance Methods

- [func hideObjectReticle(Bool) -> ObjectCaptureView<Overlay>](/documentation/realitykit/objectcaptureview/hideobjectreticle(_:))
- [ObjectCaptureSession](/documentation/realitykit/objectcapturesession)

#### Creating a session

- [init()](/documentation/realitykit/objectcapturesession/init())

#### Checking availability

- [static var isSupported: Bool](/documentation/realitykit/objectcapturesession/issupported)

#### Configuring a session

- [var feedback: Set<ObjectCaptureSession.Feedback>](/documentation/realitykit/objectcapturesession/feedback-swift.property)
- [ObjectCaptureSession.Feedback](/documentation/realitykit/objectcapturesession/feedback-swift.enum)

##### Enumeration Cases

- [case environmentLowLight](/documentation/realitykit/objectcapturesession/feedback-swift.enum/environmentlowlight)
- [case environmentTooDark](/documentation/realitykit/objectcapturesession/feedback-swift.enum/environmenttoodark)
- [case movingTooFast](/documentation/realitykit/objectcapturesession/feedback-swift.enum/movingtoofast)
- [case objectNotDetected](/documentation/realitykit/objectcapturesession/feedback-swift.enum/objectnotdetected)
- [case objectNotFlippable](/documentation/realitykit/objectcapturesession/feedback-swift.enum/objectnotflippable)
- [case objectTooClose](/documentation/realitykit/objectcapturesession/feedback-swift.enum/objecttooclose)
- [case objectTooFar](/documentation/realitykit/objectcapturesession/feedback-swift.enum/objecttoofar)
- [case outOfFieldOfView](/documentation/realitykit/objectcapturesession/feedback-swift.enum/outoffieldofview)
- [case overCapturing](/documentation/realitykit/objectcapturesession/feedback-swift.enum/overcapturing)
- [var isPaused: Bool](/documentation/realitykit/objectcapturesession/ispaused)
- [var state: ObjectCaptureSession.CaptureState](/documentation/realitykit/objectcapturesession/state)
- [var cameraTracking: ObjectCaptureSession.Tracking](/documentation/realitykit/objectcapturesession/cameratracking)
- [ObjectCaptureSession.Tracking](/documentation/realitykit/objectcapturesession/tracking)

##### Enumeration Cases

- [case limited(reason: ObjectCaptureSession.Tracking.Reason)](/documentation/realitykit/objectcapturesession/tracking/limited(reason:))
- [case normal](/documentation/realitykit/objectcapturesession/tracking/normal)
- [case notAvailable](/documentation/realitykit/objectcapturesession/tracking/notavailable)

##### Enumerations

- [ObjectCaptureSession.Tracking.Reason](/documentation/realitykit/objectcapturesession/tracking/reason)

###### Enumeration Cases

- [case excessiveMotion](/documentation/realitykit/objectcapturesession/tracking/reason/excessivemotion)
- [case initializing](/documentation/realitykit/objectcapturesession/tracking/reason/initializing)
- [case insufficientFeatures](/documentation/realitykit/objectcapturesession/tracking/reason/insufficientfeatures)
- [case relocalizing](/documentation/realitykit/objectcapturesession/tracking/reason/relocalizing)

#### Monitoring the session

- [ObjectCaptureSession.CaptureState](/documentation/realitykit/objectcapturesession/capturestate)

##### Operators

- [static func == (ObjectCaptureSession.CaptureState, ObjectCaptureSession.CaptureState) -> Bool](/documentation/realitykit/objectcapturesession/capturestate/==(_:_:))

##### Enumeration Cases

- [case capturing](/documentation/realitykit/objectcapturesession/capturestate/capturing)
- [case completed](/documentation/realitykit/objectcapturesession/capturestate/completed)
- [case detecting](/documentation/realitykit/objectcapturesession/capturestate/detecting)
- [case failed(any Error)](/documentation/realitykit/objectcapturesession/capturestate/failed(_:))
- [case finishing](/documentation/realitykit/objectcapturesession/capturestate/finishing)
- [case initializing](/documentation/realitykit/objectcapturesession/capturestate/initializing)
- [case ready](/documentation/realitykit/objectcapturesession/capturestate/ready)
- [ObjectCaptureSession.Error](/documentation/realitykit/objectcapturesession/error)

##### Enumeration Cases

- [case cancelled](/documentation/realitykit/objectcapturesession/error/cancelled)
- [case directoryNotEmpty(URL)](/documentation/realitykit/objectcapturesession/error/directorynotempty(_:))
- [case insufficientStorage(requiredBytes: Int64)](/documentation/realitykit/objectcapturesession/error/insufficientstorage(requiredbytes:))
- [case sensorFailed](/documentation/realitykit/objectcapturesession/error/sensorfailed)
- [case trackingFailed](/documentation/realitykit/objectcapturesession/error/trackingfailed)

##### Instance Properties

- [var localizedDescription: String](/documentation/realitykit/objectcapturesession/error/localizeddescription)

#### Controlling the session

- [func cancel()](/documentation/realitykit/objectcapturesession/cancel())
- [func finish()](/documentation/realitykit/objectcapturesession/finish())
- [func pause()](/documentation/realitykit/objectcapturesession/pause())
- [func requestImageCapture()](/documentation/realitykit/objectcapturesession/requestimagecapture())
- [func resume()](/documentation/realitykit/objectcapturesession/resume())
- [func startCapturing()](/documentation/realitykit/objectcapturesession/startcapturing())

#### Structures

- [ObjectCaptureSession.Configuration](/documentation/realitykit/objectcapturesession/configuration-swift.struct)

##### Initializers

- [init()](/documentation/realitykit/objectcapturesession/configuration-swift.struct/init())

##### Instance Properties

- [var checkpointDirectory: URL?](/documentation/realitykit/objectcapturesession/configuration-swift.struct/checkpointdirectory)
- [var isOverCaptureEnabled: Bool](/documentation/realitykit/objectcapturesession/configuration-swift.struct/isovercaptureenabled)
- [ObjectCaptureSession.Updates](/documentation/realitykit/objectcapturesession/updates)

##### Structures

- [ObjectCaptureSession.Updates.Iterator](/documentation/realitykit/objectcapturesession/updates/iterator)

#### Instance Properties

- [var cameraTrackingUpdates: ObjectCaptureSession.Updates<ObjectCaptureSession.Tracking>](/documentation/realitykit/objectcapturesession/cameratrackingupdates)
- [var canRequestImageCapture: Bool](/documentation/realitykit/objectcapturesession/canrequestimagecapture)
- [var canRequestImageCaptureUpdates: ObjectCaptureSession.Updates<Bool>](/documentation/realitykit/objectcapturesession/canrequestimagecaptureupdates)
- [var configuration: ObjectCaptureSession.Configuration](/documentation/realitykit/objectcapturesession/configuration-swift.property)
- [var feedbackUpdates: ObjectCaptureSession.Updates<Set<ObjectCaptureSession.Feedback>>](/documentation/realitykit/objectcapturesession/feedbackupdates)
- [var isAutoCaptureEnabled: Bool](/documentation/realitykit/objectcapturesession/isautocaptureenabled)
- [var isPausedUpdates: ObjectCaptureSession.Updates<Bool>](/documentation/realitykit/objectcapturesession/ispausedupdates)
- [var maximumNumberOfInputImages: Int](/documentation/realitykit/objectcapturesession/maximumnumberofinputimages)
- [var numberOfShotsTaken: Int](/documentation/realitykit/objectcapturesession/numberofshotstaken)
- [var numberOfShotsTakenUpdates: ObjectCaptureSession.Updates<Int>](/documentation/realitykit/objectcapturesession/numberofshotstakenupdates)
- [var shouldPlayHaptics: Bool](/documentation/realitykit/objectcapturesession/shouldplayhaptics)
- [var stateUpdates: ObjectCaptureSession.Updates<ObjectCaptureSession.CaptureState>](/documentation/realitykit/objectcapturesession/stateupdates)
- [var userCompletedScanPass: Bool](/documentation/realitykit/objectcapturesession/usercompletedscanpass)
- [var userCompletedScanPassUpdates: ObjectCaptureSession.Updates<Bool>](/documentation/realitykit/objectcapturesession/usercompletedscanpassupdates)

#### Instance Methods

- [func beginNewScanPass()](/documentation/realitykit/objectcapturesession/beginnewscanpass())
- [func beginNewScanPassAfterFlip()](/documentation/realitykit/objectcapturesession/beginnewscanpassafterflip())
- [func resetDetection() -> Bool](/documentation/realitykit/objectcapturesession/resetdetection())
- [func start(imagesDirectory: URL, configuration: ObjectCaptureSession.Configuration)](/documentation/realitykit/objectcapturesession/start(imagesdirectory:configuration:))
- [func startDetecting() -> Bool](/documentation/realitykit/objectcapturesession/startdetecting())
- [ObjectCapturePointCloudView](/documentation/realitykit/objectcapturepointcloudview)

#### Initializers

- [init(session: ObjectCaptureSession)](/documentation/realitykit/objectcapturepointcloudview/init(session:))

#### Instance Methods

- [func showShotLocations(Bool) -> ObjectCapturePointCloudView](/documentation/realitykit/objectcapturepointcloudview/showshotlocations(_:))
- [USD](/documentation/usd)
- [Composing interactive 3D content with RealityKit and Reality Composer Pro](/documentation/realitykit/composing-interactive-3d-content-with-realitykit-and-reality-composer-pro)

## Scene content

- [Hello World](/documentation/visionos/world)
- [Enabling video reflections in an immersive environment](/documentation/visionos/enabling-video-reflections-in-an-immersive-environment)
- [Creating a spatial drawing app with RealityKit](/documentation/realitykit/creating-a-spatial-drawing-app-with-realitykit)
- [Generating interactive geometry with RealityKit](/documentation/realitykit/generating-interactive-geometry-with-realitykit)
- [Combining 2D and 3D views in an immersive app](/documentation/realitykit/combining-2d-and-3d-views-in-an-immersive-app)
- [Transforming RealityKit entities using gestures](/documentation/realitykit/transforming-realitykit-entities-with-gestures)
- [Responding to gestures on an entity](/documentation/realitykit/responding-to-gestures-on-an-entity)
- [Models and meshes](/documentation/realitykit/scene-content-models-and-meshes)

### Model display

- [ModelComponent](/documentation/realitykit/modelcomponent)

#### Creating a model component

- [init(mesh: MeshResource, materials: [any Material])](/documentation/realitykit/modelcomponent/init(mesh:materials:))

#### Configuring a mesh

- [var mesh: MeshResource](/documentation/realitykit/modelcomponent/mesh)

#### Configuring the materials

- [var materials: [any Material]](/documentation/realitykit/modelcomponent/materials)

#### Modifying the bounding box for rendering

- [var boundsMargin: Float](/documentation/realitykit/modelcomponent/boundsmargin)
- [MeshResource](/documentation/realitykit/meshresource)

#### Creating a mesh resource

- [static func generate(from: MeshResource.Contents) throws -> MeshResource](/documentation/realitykit/meshresource/generate(from:)-4aahn)
- [static func generate(from: MeshResource.Contents) throws -> MeshResource](/documentation/realitykit/meshresource/generate(from:)-4aahn)
- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)
- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)
- [convenience init(shape: ShapeResource)](/documentation/realitykit/meshresource/init(shape:)-3rtda)
- [convenience init(shape: ShapeResource)](/documentation/realitykit/meshresource/init(shape:)-3rtda)
- [static func generateAsync(from: MeshResource.Contents) -> LoadRequest<MeshResource>](/documentation/realitykit/meshresource/generateasync(from:)-1n2vv)
- [static func generateAsync(from: MeshResource.Contents) -> LoadRequest<MeshResource>](/documentation/realitykit/meshresource/generateasync(from:)-1n2vv)

#### Creating a low level resource

- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)
- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)
- [var lowLevelMesh: LowLevelMesh?](/documentation/realitykit/meshresource/lowlevelmesh)

#### Configuring the resource

- [var expectedMaterialCount: Int](/documentation/realitykit/meshresource/expectedmaterialcount)
- [func replace(with: MeshResource.Contents) throws](/documentation/realitykit/meshresource/replace(with:)-g0kn)
- [func replace(with: MeshResource.Contents) throws](/documentation/realitykit/meshresource/replace(with:)-g0kn)
- [func replaceAsync(with: MeshResource.Contents) -> LoadRequest<MeshResource>](/documentation/realitykit/meshresource/replaceasync(with:))

#### Accessing resource data

- [var contents: MeshResource.Contents](/documentation/realitykit/meshresource/contents-swift.property)

#### Getting a bounding box

- [var bounds: BoundingBox](/documentation/realitykit/meshresource/bounds)

#### Creating a box

- [static func generateBox(size: Float, cornerRadius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatebox(size:cornerradius:)-8em0v)
- [static func generateBox(size: SIMD3<Float>, cornerRadius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatebox(size:cornerradius:)-2ovma)
- [static func generateBox(width: Float, height: Float, depth: Float, cornerRadius: Float, splitFaces: Bool) -> MeshResource](/documentation/realitykit/meshresource/generatebox(width:height:depth:cornerradius:splitfaces:))
- [static func generateBox(size: SIMD3<Float>, majorCornerRadius: Float, minorCornerRadius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatebox(size:majorcornerradius:minorcornerradius:))

#### Creating a plane

- [static func generatePlane(width: Float, height: Float, cornerRadius: Float) -> MeshResource](/documentation/realitykit/meshresource/generateplane(width:height:cornerradius:))
- [static func generatePlane(width: Float, depth: Float, cornerRadius: Float) -> MeshResource](/documentation/realitykit/meshresource/generateplane(width:depth:cornerradius:))

#### Creating a primitive shape

- [static func generateSphere(radius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatesphere(radius:))
- [static func generateCone(height: Float, radius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatecone(height:radius:))
- [static func generateCylinder(height: Float, radius: Float) -> MeshResource](/documentation/realitykit/meshresource/generatecylinder(height:radius:))

#### Creating a text mesh resource

- [static func generateText(String, extrusionDepth: Float, font: MeshResource.Font, containerFrame: CGRect, alignment: CTTextAlignment, lineBreakMode: CTLineBreakMode) -> MeshResource](/documentation/realitykit/meshresource/generatetext(_:extrusiondepth:font:containerframe:alignment:linebreakmode:)-3py6y)
- [static func generateText(String, extrusionDepth: Float, font: MeshResource.Font, containerFrame: CGRect, alignment: CTTextAlignment, lineBreakMode: CTLineBreakMode) -> MeshResource](/documentation/realitykit/meshresource/generatetext(_:extrusiondepth:font:containerframe:alignment:linebreakmode:)-3py6y)
- [convenience init(extruding: AttributedString, textOptions: MeshResource.GenerateTextOptions, extrusionOptions: MeshResource.ShapeExtrusionOptions) throws](/documentation/realitykit/meshresource/init(extruding:textoptions:extrusionoptions:)-7xk2s)
- [convenience init(extruding: AttributedString, textOptions: MeshResource.GenerateTextOptions, extrusionOptions: MeshResource.ShapeExtrusionOptions) throws](/documentation/realitykit/meshresource/init(extruding:textoptions:extrusionoptions:)-7xk2s)

#### Creating a 3D mesh by extruding a 2D path

- [convenience init(extruding: Path, extrusionOptions: MeshResource.ShapeExtrusionOptions) throws](/documentation/realitykit/meshresource/init(extruding:extrusionoptions:)-6640v)
- [convenience init(extruding: Path, extrusionOptions: MeshResource.ShapeExtrusionOptions) throws](/documentation/realitykit/meshresource/init(extruding:extrusionoptions:)-6640v)

#### Creating a mesh from an anchor

- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)
- [convenience init(from: LowLevelMesh) async throws](/documentation/realitykit/meshresource/init(from:)-1i7c9)

#### Structures

- [MeshResource.Contents](/documentation/realitykit/meshresource/contents-swift.struct)

##### Initializers

- [init()](/documentation/realitykit/meshresource/contents-swift.struct/init())

##### Instance Properties

- [var instances: MeshInstanceCollection](/documentation/realitykit/meshresource/contents-swift.struct/instances)
- [var models: MeshModelCollection](/documentation/realitykit/meshresource/contents-swift.struct/models)
- [var skeletons: MeshSkeletonCollection](/documentation/realitykit/meshresource/contents-swift.struct/skeletons)
- [MeshResource.GenerateTextOptions](/documentation/realitykit/meshresource/generatetextoptions)

##### Initializers

- [init()](/documentation/realitykit/meshresource/generatetextoptions/init())

##### Instance Properties

- [var containerFrame: CGRect?](/documentation/realitykit/meshresource/generatetextoptions/containerframe)
- [MeshResource.Instance](/documentation/realitykit/meshresource/instance)

##### Initializers

- [init(id: String, model: String, at: simd_float4x4?)](/documentation/realitykit/meshresource/instance/init(id:model:at:))

##### Instance Properties

- [var model: String](/documentation/realitykit/meshresource/instance/model)
- [var transform: simd_float4x4](/documentation/realitykit/meshresource/instance/transform)
- [MeshResource.JointInfluences](/documentation/realitykit/meshresource/jointinfluences)

##### Initializers

- [init(influences: MeshBuffers.JointInfluences, influencesPerVertex: Int)](/documentation/realitykit/meshresource/jointinfluences/init(influences:influencespervertex:))

##### Instance Properties

- [var influences: MeshBuffers.JointInfluences](/documentation/realitykit/meshresource/jointinfluences/influences)
- [MeshResource.Model](/documentation/realitykit/meshresource/model)

##### Initializers

- [init(id: String, descriptors: [MeshDescriptor]) throws](/documentation/realitykit/meshresource/model/init(id:descriptors:))
- [init(id: String, parts: [MeshResource.Part])](/documentation/realitykit/meshresource/model/init(id:parts:))

##### Instance Properties

- [var parts: MeshPartCollection](/documentation/realitykit/meshresource/model/parts)
- [MeshResource.Part](/documentation/realitykit/meshresource/part)

##### Initializers

- [init(id: String, materialIndex: Int)](/documentation/realitykit/meshresource/part/init(id:materialindex:))

##### Instance Properties

- [var jointInfluences: MeshResource.JointInfluences?](/documentation/realitykit/meshresource/part/jointinfluences)
- [var materialIndex: Int](/documentation/realitykit/meshresource/part/materialindex)
- [var skeletonID: String?](/documentation/realitykit/meshresource/part/skeletonid)
- [var triangleIndices: MeshBuffers.TriangleIndices?](/documentation/realitykit/meshresource/part/triangleindices)
- [MeshResource.ShapeExtrusionOptions](/documentation/realitykit/meshresource/shapeextrusionoptions)

##### Structures

- [MeshResource.ShapeExtrusionOptions.MaterialAssignment](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct)

###### Initializers

- [init(assignAll: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(assignall:))
- [init(front: UInt32, back: UInt32, extrusion: UInt32, frontChamfer: UInt32, backChamfer: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(front:back:extrusion:frontchamfer:backchamfer:))

##### Initializers

- [init()](/documentation/realitykit/meshresource/shapeextrusionoptions/init())

##### Instance Properties

- [var boundaryResolution: MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/boundaryresolution)
- [var chamferMode: MeshResource.ShapeExtrusionOptions.ChamferMode](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.property)
- [var chamferProfile: Path?](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferprofile)
- [var chamferRadius: Float](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferradius)
- [var chamferResolution: MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferresolution)
- [var extrusionMethod: MeshResource.ShapeExtrusionOptions.ExtrusionMethod](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.property)
- [var materialAssignment: MeshResource.ShapeExtrusionOptions.MaterialAssignment](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.property)

##### Enumerations

- [MeshResource.ShapeExtrusionOptions.ChamferMode](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum)

###### Enumeration Cases

- [case back](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/back)
- [case both](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/both)
- [case front](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/front)
- [MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution)

###### Enumeration Cases

- [case uniformSegmentsPerSpan(segmentCount: Int)](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution/uniformsegmentsperspan(segmentcount:))
- [MeshResource.ShapeExtrusionOptions.ExtrusionMethod](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum)

###### Enumeration Cases

- [case linear(depth: Float)](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/linear(depth:))
- [case tracePositions([SIMD3<Float>])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracepositions(_:))
- [case traceTransforms([simd_float4x4])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracetransforms(_:))
- [MeshResource.Skeleton](/documentation/realitykit/meshresource/skeleton)

##### Structures

- [MeshResource.Skeleton.Joint](/documentation/realitykit/meshresource/skeleton/joint)

###### Initializers

- [init(name: String, parentIndex: Int?, inverseBindPoseMatrix: simd_float4x4, restPoseTransform: Transform)](/documentation/realitykit/meshresource/skeleton/joint/init(name:parentindex:inversebindposematrix:restposetransform:))

###### Instance Properties

- [var inverseBindPoseMatrix: simd_float4x4](/documentation/realitykit/meshresource/skeleton/joint/inversebindposematrix)
- [var name: String](/documentation/realitykit/meshresource/skeleton/joint/name)
- [var parentIndex: Int?](/documentation/realitykit/meshresource/skeleton/joint/parentindex)
- [var restPoseTransform: Transform](/documentation/realitykit/meshresource/skeleton/joint/restposetransform)

##### Initializers

- [init?(id: String, jointNames: [String], inverseBindPoseMatrices: [simd_float4x4], restPoseTransforms: [Transform]?, parentIndices: [Int?]?)](/documentation/realitykit/meshresource/skeleton/init(id:jointnames:inversebindposematrices:restposetransforms:parentindices:))
- [init(id: String, joints: [MeshResource.Skeleton.Joint])](/documentation/realitykit/meshresource/skeleton/init(id:joints:))

##### Instance Properties

- [var id: String](/documentation/realitykit/meshresource/skeleton/id)
- [var joints: [MeshResource.Skeleton.Joint]](/documentation/realitykit/meshresource/skeleton/joints)

#### Initializers

- [convenience(extruding:extrusionOptions:)](/documentation/realitykit/meshresource/init(extruding:extrusionoptions:))
- [convenience(extruding:textOptions:extrusionOptions:)](/documentation/realitykit/meshresource/init(extruding:textoptions:extrusionoptions:))
- [convenience(from:)](/documentation/realitykit/meshresource/init(from:))
- [convenience(shape:)](/documentation/realitykit/meshresource/init(shape:))

#### Instance Methods

- [func meshPartIndex(modelID: String, partID: String) -> Int?](/documentation/realitykit/meshresource/meshpartindex(modelid:partid:))
- [func replace(with:)](/documentation/realitykit/meshresource/replace(with:))

#### Type Aliases

- [MeshResource.Font](/documentation/realitykit/meshresource/font)

#### Type Methods

- [static generate(from:)](/documentation/realitykit/meshresource/generate(from:))
- [static generateAsync(from:)](/documentation/realitykit/meshresource/generateasync(from:))
- [static generateBox(size:cornerRadius:)](/documentation/realitykit/meshresource/generatebox(size:cornerradius:))
- [static generateText(_:extrusionDepth:font:containerFrame:alignment:lineBreakMode:)](/documentation/realitykit/meshresource/generatetext(_:extrusiondepth:font:containerframe:alignment:linebreakmode:))
- [ModelEntity](/documentation/realitykit/modelentity)

#### Creating a model

- [init()](/documentation/realitykit/modelentity/init())
- [init(mesh: MeshResource, materials: [any Material])](/documentation/realitykit/modelentity/init(mesh:materials:))
- [init(mesh: MeshResource, materials: [any Material], collisionShape: ShapeResource, mass: Float)](/documentation/realitykit/modelentity/init(mesh:materials:collisionshape:mass:))
- [init(mesh: MeshResource, materials: [any Material], collisionShapes: [ShapeResource], mass: Float)](/documentation/realitykit/modelentity/init(mesh:materials:collisionshapes:mass:))

### Render configuration

- [ModelSortGroupComponent](/documentation/realitykit/modelsortgroupcomponent)

#### Initializers

- [init(group: ModelSortGroup, order: Int32)](/documentation/realitykit/modelsortgroupcomponent/init(group:order:))

#### Instance Properties

- [var group: ModelSortGroup](/documentation/realitykit/modelsortgroupcomponent/group)
- [var order: Int32](/documentation/realitykit/modelsortgroupcomponent/order)
- [ModelSortGroup](/documentation/realitykit/modelsortgroup)

#### Operators

- [static func != (ModelSortGroup, ModelSortGroup) -> Bool](/documentation/realitykit/modelsortgroup/!=(_:_:))
- [static func == (ModelSortGroup, ModelSortGroup) -> Bool](/documentation/realitykit/modelsortgroup/==(_:_:))

#### Initializers

- [init(depthPass: ModelSortGroup.DepthPass?)](/documentation/realitykit/modelsortgroup/init(depthpass:))

#### Instance Properties

- [var depthPass: ModelSortGroup.DepthPass?](/documentation/realitykit/modelsortgroup/depthpass-swift.property)
- [var planarUIPlacement: ModelSortGroup.PlanarUIPlacement?](/documentation/realitykit/modelsortgroup/planaruiplacement-swift.property)

#### Type Properties

- [static let planarUIAlwaysBehind: ModelSortGroup](/documentation/realitykit/modelsortgroup/planaruialwaysbehind)
- [static let planarUIAlwaysInFront: ModelSortGroup](/documentation/realitykit/modelsortgroup/planaruialwaysinfront)
- [static let planarUIInline: ModelSortGroup](/documentation/realitykit/modelsortgroup/planaruiinline)

#### Enumerations

- [ModelSortGroup.DepthPass](/documentation/realitykit/modelsortgroup/depthpass-swift.enum)

##### Enumeration Cases

- [case postPass](/documentation/realitykit/modelsortgroup/depthpass-swift.enum/postpass)
- [case prePass](/documentation/realitykit/modelsortgroup/depthpass-swift.enum/prepass)
- [ModelSortGroup.PlanarUIPlacement](/documentation/realitykit/modelsortgroup/planaruiplacement-swift.enum)

##### Enumeration Cases

- [case alwaysBehind](/documentation/realitykit/modelsortgroup/planaruiplacement-swift.enum/alwaysbehind)
- [case alwaysInFront](/documentation/realitykit/modelsortgroup/planaruiplacement-swift.enum/alwaysinfront)
- [case inlineUI](/documentation/realitykit/modelsortgroup/planaruiplacement-swift.enum/inlineui)
- [OpacityComponent](/documentation/realitykit/opacitycomponent)

#### Operators

- [static func == (OpacityComponent, OpacityComponent) -> Bool](/documentation/realitykit/opacitycomponent/==(_:_:))

#### Initializers

- [init(opacity: Float)](/documentation/realitykit/opacitycomponent/init(opacity:))

#### Instance Properties

- [var opacity: Float](/documentation/realitykit/opacitycomponent/opacity)
- [AdaptiveResolutionComponent](/documentation/realitykit/adaptiveresolutioncomponent)

#### Initializers

- [init()](/documentation/realitykit/adaptiveresolutioncomponent/init())

#### Instance Properties

- [var pixelsPerMeter: Float](/documentation/realitykit/adaptiveresolutioncomponent/pixelspermeter)
- [ModelDebugOptionsComponent](/documentation/realitykit/modeldebugoptionscomponent)

#### Creating model debug options components

- [init(visualizationMode: ModelDebugOptionsComponent.VisualizationMode)](/documentation/realitykit/modeldebugoptionscomponent/init(visualizationmode:))

#### Setting the visualization mode

- [var visualizationMode: ModelDebugOptionsComponent.VisualizationMode](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.property)
- [ModelDebugOptionsComponent.VisualizationMode](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum)

##### Visualization modes

- [case none](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/none)
- [case normal](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/normal)
- [case tangent](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/tangent)
- [case bitangent](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/bitangent)
- [case baseColor](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/basecolor)
- [case textureCoordinates](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/texturecoordinates)
- [case finalColor](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/finalcolor)
- [case finalAlpha](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/finalalpha)
- [case roughness](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/roughness)
- [case metallic](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/metallic)
- [case ambientOcclusion](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/ambientocclusion)
- [case specular](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/specular)
- [case emissive](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/emissive)
- [case clearcoat](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/clearcoat)
- [case clearcoatRoughness](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/clearcoatroughness)
- [case lightingDiffuse](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/lightingdiffuse)
- [case lightingSpecular](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/lightingspecular)

##### Raw values


##### Enumeration Cases

- [case clearcoatNormal](/documentation/realitykit/modeldebugoptionscomponent/visualizationmode-swift.enum/clearcoatnormal)
- [MeshInstancesComponent](/documentation/realitykit/meshinstancescomponent)

#### Structures

- [MeshInstancesComponent.Part](/documentation/realitykit/meshinstancescomponent/part)

##### Initializers

- [init(data: LowLevelInstanceData, bounds: BoundingBox?)](/documentation/realitykit/meshinstancescomponent/part/init(data:bounds:))

##### Instance Properties

- [var bounds: BoundingBox?](/documentation/realitykit/meshinstancescomponent/part/bounds)
- [var data: LowLevelInstanceData](/documentation/realitykit/meshinstancescomponent/part/data)

#### Initializers

- [init()](/documentation/realitykit/meshinstancescomponent/init())
- [init(mesh: MeshResource, modelID: String?, instances: LowLevelInstanceData, bounds: BoundingBox?) throws](/documentation/realitykit/meshinstancescomponent/init(mesh:modelid:instances:bounds:))

#### Subscripts

- [subscript(partIndex _: Int) -> MeshInstancesComponent.Part?](/documentation/realitykit/meshinstancescomponent/subscript(partindex:))

### Static meshes

- [MeshDescriptor](/documentation/realitykit/meshdescriptor)

#### Initializers

- [init(name: String)](/documentation/realitykit/meshdescriptor/init(name:))

#### Instance Properties

- [var materials: MeshDescriptor.Materials](/documentation/realitykit/meshdescriptor/materials-swift.property)
- [var name: String](/documentation/realitykit/meshdescriptor/name)
- [var primitives: MeshDescriptor.Primitives?](/documentation/realitykit/meshdescriptor/primitives-swift.property)

#### Enumerations

- [MeshDescriptor.Materials](/documentation/realitykit/meshdescriptor/materials-swift.enum)

##### Enumeration Cases

- [case allFaces(UInt32)](/documentation/realitykit/meshdescriptor/materials-swift.enum/allfaces(_:))
- [case perFace([UInt32])](/documentation/realitykit/meshdescriptor/materials-swift.enum/perface(_:))
- [MeshDescriptor.Primitives](/documentation/realitykit/meshdescriptor/primitives-swift.enum)

##### Enumeration Cases

- [case polygons([UInt8], [UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/polygons(_:_:))
- [case triangles([UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/triangles(_:))
- [case trianglesAndQuads(triangles: [UInt32], quads: [UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/trianglesandquads(triangles:quads:))
- [MeshDescriptor.Primitives](/documentation/realitykit/meshdescriptor/primitives-swift.enum)

#### Enumeration Cases

- [case polygons([UInt8], [UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/polygons(_:_:))
- [case triangles([UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/triangles(_:))
- [case trianglesAndQuads(triangles: [UInt32], quads: [UInt32])](/documentation/realitykit/meshdescriptor/primitives-swift.enum/trianglesandquads(triangles:quads:))
- [MeshDescriptor.Materials](/documentation/realitykit/meshdescriptor/materials-swift.enum)

#### Enumeration Cases

- [case allFaces(UInt32)](/documentation/realitykit/meshdescriptor/materials-swift.enum/allfaces(_:))
- [case perFace([UInt32])](/documentation/realitykit/meshdescriptor/materials-swift.enum/perface(_:))

### Updatable meshes

- [Integrating virtual objects with your environment](/documentation/realitykit/integrating-virtual-objects-with-your-environment)
- [Creating a spatial drawing app with RealityKit](/documentation/realitykit/creating-a-spatial-drawing-app-with-realitykit)
- [Creating a plane with low-level mesh](/documentation/realitykit/creating-a-plane-with-low-level-mesh)
- [LowLevelMesh](/documentation/realitykit/lowlevelmesh)

#### Creating a low-level mesh

- [init(descriptor: LowLevelMesh.Descriptor) throws](/documentation/realitykit/lowlevelmesh/init(descriptor:))

#### Describing a low-level mesh

- [let descriptor: LowLevelMesh.Descriptor](/documentation/realitykit/lowlevelmesh/descriptor-swift.property)
- [var parts: LowLevelMesh.PartsCollection](/documentation/realitykit/lowlevelmesh/parts)
- [var indexCapacity: Int](/documentation/realitykit/lowlevelmesh/indexcapacity)
- [var vertexCapacity: Int](/documentation/realitykit/lowlevelmesh/vertexcapacity)

#### Accessing mesh data on the CPU with Swift

- [func withUnsafeBytes(bufferIndex: Int, (UnsafeRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/withunsafebytes(bufferindex:_:))
- [func withUnsafeMutableBytes(bufferIndex: Int, (UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/withunsafemutablebytes(bufferindex:_:))
- [func withUnsafeIndices((UnsafeRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/withunsafeindices(_:))
- [func withUnsafeMutableIndices((UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/withunsafemutableindices(_:))
- [func replaceUnsafeMutableBytes(bufferIndex: Int, (UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/replaceunsafemutablebytes(bufferindex:_:))
- [func replaceUnsafeMutableIndices((UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelmesh/replaceunsafemutableindices(_:))

#### Accessing mesh data on the GPU with Metal

- [func read(bufferIndex: Int, using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelmesh/read(bufferindex:using:))
- [func readIndices(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelmesh/readindices(using:))
- [func replace(bufferIndex: Int, using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelmesh/replace(bufferindex:using:))
- [func replaceIndices(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelmesh/replaceindices(using:))

#### Structures

- [LowLevelMesh.Attribute](/documentation/realitykit/lowlevelmesh/attribute)

##### Creating a vertex attribute

- [init(semantic: LowLevelMesh.VertexSemantic, format: MTLVertexFormat, layoutIndex: Int, offset: Int)](/documentation/realitykit/lowlevelmesh/attribute/init(semantic:format:layoutindex:offset:))

##### Describing an attribute

- [var format: MTLVertexFormat](/documentation/realitykit/lowlevelmesh/attribute/format)
- [var offset: Int](/documentation/realitykit/lowlevelmesh/attribute/offset)
- [var layoutIndex: Int](/documentation/realitykit/lowlevelmesh/attribute/layoutindex)
- [var semantic: LowLevelMesh.VertexSemantic](/documentation/realitykit/lowlevelmesh/attribute/semantic)
- [LowLevelMesh.Descriptor](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct)

##### Creating a low-level mesh descriptor

- [init(vertexCapacity: Int, vertexAttributes: [LowLevelMesh.Attribute], vertexLayouts: [LowLevelMesh.Layout], indexCapacity: Int, indexType: MTLIndexType)](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/init(vertexcapacity:vertexattributes:vertexlayouts:indexcapacity:indextype:))

##### Defining the descriptor’s contents

- [var indexType: MTLIndexType](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/indextype)
- [var vertexAttributes: [LowLevelMesh.Attribute]](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexattributes)
- [var vertexLayouts: [LowLevelMesh.Layout]](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexlayouts)
- [var vertexBufferCount: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexbuffercount)

##### Defining the descriptor’s limits

- [var vertexCapacity: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexcapacity)
- [var indexCapacity: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/indexcapacity)
- [static let maxVertexBufferCount: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/maxvertexbuffercount)
- [LowLevelMesh.Layout](/documentation/realitykit/lowlevelmesh/layout)

##### Creating a low-level mesh layout

- [init(bufferIndex: Int, bufferOffset: Int, bufferStride: Int)](/documentation/realitykit/lowlevelmesh/layout/init(bufferindex:bufferoffset:bufferstride:))

##### Describing a low-level mesh layout

- [var bufferIndex: Int](/documentation/realitykit/lowlevelmesh/layout/bufferindex)
- [var bufferOffset: Int](/documentation/realitykit/lowlevelmesh/layout/bufferoffset)
- [var bufferStride: Int](/documentation/realitykit/lowlevelmesh/layout/bufferstride)
- [LowLevelMesh.Part](/documentation/realitykit/lowlevelmesh/part)

##### Creating a low-level mesh part

- [init(indexOffset: Int, indexCount: Int, topology: MTLPrimitiveType, materialIndex: Int, bounds: BoundingBox)](/documentation/realitykit/lowlevelmesh/part/init(indexoffset:indexcount:topology:materialindex:bounds:))

##### Describing a low-level mesh part

- [var indexOffset: Int](/documentation/realitykit/lowlevelmesh/part/indexoffset)
- [var indexCount: Int](/documentation/realitykit/lowlevelmesh/part/indexcount)
- [var topology: MTLPrimitiveType](/documentation/realitykit/lowlevelmesh/part/topology)
- [var materialIndex: Int](/documentation/realitykit/lowlevelmesh/part/materialindex)
- [var bounds: BoundingBox](/documentation/realitykit/lowlevelmesh/part/bounds)
- [LowLevelMesh.PartsCollection](/documentation/realitykit/lowlevelmesh/partscollection)

##### Updating collection contents

- [func append(LowLevelMesh.PartsCollection.Element)](/documentation/realitykit/lowlevelmesh/partscollection/append(_:))
- [func append<S>(contentsOf: S)](/documentation/realitykit/lowlevelmesh/partscollection/append(contentsof:))
- [func replaceAll<S>(S)](/documentation/realitykit/lowlevelmesh/partscollection/replaceall(_:))
- [func removeAll()](/documentation/realitykit/lowlevelmesh/partscollection/removeall())

#### Enumerations

- [LowLevelMesh.VertexSemantic](/documentation/realitykit/lowlevelmesh/vertexsemantic)

##### Specifying intended use

- [case bitangent](/documentation/realitykit/lowlevelmesh/vertexsemantic/bitangent)
- [case color](/documentation/realitykit/lowlevelmesh/vertexsemantic/color)
- [case normal](/documentation/realitykit/lowlevelmesh/vertexsemantic/normal)
- [case position](/documentation/realitykit/lowlevelmesh/vertexsemantic/position)
- [case tangent](/documentation/realitykit/lowlevelmesh/vertexsemantic/tangent)
- [case unspecified](/documentation/realitykit/lowlevelmesh/vertexsemantic/unspecified)
- [case uv0](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv0)
- [case uv1](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv1)
- [case uv2](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv2)
- [case uv3](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv3)
- [case uv4](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv4)
- [case uv5](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv5)
- [case uv6](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv6)
- [case uv7](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv7)
- [LowLevelMesh.Descriptor](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct)

#### Creating a low-level mesh descriptor

- [init(vertexCapacity: Int, vertexAttributes: [LowLevelMesh.Attribute], vertexLayouts: [LowLevelMesh.Layout], indexCapacity: Int, indexType: MTLIndexType)](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/init(vertexcapacity:vertexattributes:vertexlayouts:indexcapacity:indextype:))

#### Defining the descriptor’s contents

- [var indexType: MTLIndexType](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/indextype)
- [var vertexAttributes: [LowLevelMesh.Attribute]](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexattributes)
- [var vertexLayouts: [LowLevelMesh.Layout]](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexlayouts)
- [var vertexBufferCount: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexbuffercount)

#### Defining the descriptor’s limits

- [var vertexCapacity: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/vertexcapacity)
- [var indexCapacity: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/indexcapacity)
- [static let maxVertexBufferCount: Int](/documentation/realitykit/lowlevelmesh/descriptor-swift.struct/maxvertexbuffercount)
- [LowLevelMesh.Part](/documentation/realitykit/lowlevelmesh/part)

#### Creating a low-level mesh part

- [init(indexOffset: Int, indexCount: Int, topology: MTLPrimitiveType, materialIndex: Int, bounds: BoundingBox)](/documentation/realitykit/lowlevelmesh/part/init(indexoffset:indexcount:topology:materialindex:bounds:))

#### Describing a low-level mesh part

- [var indexOffset: Int](/documentation/realitykit/lowlevelmesh/part/indexoffset)
- [var indexCount: Int](/documentation/realitykit/lowlevelmesh/part/indexcount)
- [var topology: MTLPrimitiveType](/documentation/realitykit/lowlevelmesh/part/topology)
- [var materialIndex: Int](/documentation/realitykit/lowlevelmesh/part/materialindex)
- [var bounds: BoundingBox](/documentation/realitykit/lowlevelmesh/part/bounds)
- [LowLevelMesh.Layout](/documentation/realitykit/lowlevelmesh/layout)

#### Creating a low-level mesh layout

- [init(bufferIndex: Int, bufferOffset: Int, bufferStride: Int)](/documentation/realitykit/lowlevelmesh/layout/init(bufferindex:bufferoffset:bufferstride:))

#### Describing a low-level mesh layout

- [var bufferIndex: Int](/documentation/realitykit/lowlevelmesh/layout/bufferindex)
- [var bufferOffset: Int](/documentation/realitykit/lowlevelmesh/layout/bufferoffset)
- [var bufferStride: Int](/documentation/realitykit/lowlevelmesh/layout/bufferstride)
- [LowLevelMesh.Attribute](/documentation/realitykit/lowlevelmesh/attribute)

#### Creating a vertex attribute

- [init(semantic: LowLevelMesh.VertexSemantic, format: MTLVertexFormat, layoutIndex: Int, offset: Int)](/documentation/realitykit/lowlevelmesh/attribute/init(semantic:format:layoutindex:offset:))

#### Describing an attribute

- [var format: MTLVertexFormat](/documentation/realitykit/lowlevelmesh/attribute/format)
- [var offset: Int](/documentation/realitykit/lowlevelmesh/attribute/offset)
- [var layoutIndex: Int](/documentation/realitykit/lowlevelmesh/attribute/layoutindex)
- [var semantic: LowLevelMesh.VertexSemantic](/documentation/realitykit/lowlevelmesh/attribute/semantic)
- [LowLevelMesh.VertexSemantic](/documentation/realitykit/lowlevelmesh/vertexsemantic)

#### Specifying intended use

- [case bitangent](/documentation/realitykit/lowlevelmesh/vertexsemantic/bitangent)
- [case color](/documentation/realitykit/lowlevelmesh/vertexsemantic/color)
- [case normal](/documentation/realitykit/lowlevelmesh/vertexsemantic/normal)
- [case position](/documentation/realitykit/lowlevelmesh/vertexsemantic/position)
- [case tangent](/documentation/realitykit/lowlevelmesh/vertexsemantic/tangent)
- [case unspecified](/documentation/realitykit/lowlevelmesh/vertexsemantic/unspecified)
- [case uv0](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv0)
- [case uv1](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv1)
- [case uv2](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv2)
- [case uv3](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv3)
- [case uv4](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv4)
- [case uv5](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv5)
- [case uv6](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv6)
- [case uv7](/documentation/realitykit/lowlevelmesh/vertexsemantic/uv7)
- [LowLevelMesh.PartsCollection](/documentation/realitykit/lowlevelmesh/partscollection)

#### Updating collection contents

- [func append(LowLevelMesh.PartsCollection.Element)](/documentation/realitykit/lowlevelmesh/partscollection/append(_:))
- [func append<S>(contentsOf: S)](/documentation/realitykit/lowlevelmesh/partscollection/append(contentsof:))
- [func replaceAll<S>(S)](/documentation/realitykit/lowlevelmesh/partscollection/replaceall(_:))
- [func removeAll()](/documentation/realitykit/lowlevelmesh/partscollection/removeall())
- [LowLevelBuffer](/documentation/realitykit/lowlevelbuffer)

#### Structures

- [LowLevelBuffer.Descriptor](/documentation/realitykit/lowlevelbuffer/descriptor-swift.struct)

##### Initializers

- [init(capacity: Int, sizeMultiple: Int)](/documentation/realitykit/lowlevelbuffer/descriptor-swift.struct/init(capacity:sizemultiple:))

##### Instance Properties

- [var capacity: Int](/documentation/realitykit/lowlevelbuffer/descriptor-swift.struct/capacity)
- [var sizeMultiple: Int](/documentation/realitykit/lowlevelbuffer/descriptor-swift.struct/sizemultiple)

#### Initializers

- [init(descriptor: LowLevelBuffer.Descriptor) throws](/documentation/realitykit/lowlevelbuffer/init(descriptor:))

#### Instance Properties

- [var bytesUsed: Int](/documentation/realitykit/lowlevelbuffer/bytesused)
- [let descriptor: LowLevelBuffer.Descriptor](/documentation/realitykit/lowlevelbuffer/descriptor-swift.property)

#### Instance Methods

- [func read(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelbuffer/read(using:))
- [func replace(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelbuffer/replace(using:))
- [func replaceUnsafeMutableBytes((UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelbuffer/replaceunsafemutablebytes(_:))
- [func withUnsafeBytes((UnsafeRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelbuffer/withunsafebytes(_:))
- [func withUnsafeMutableBytes((UnsafeMutableRawBufferPointer) -> Void)](/documentation/realitykit/lowlevelbuffer/withunsafemutablebytes(_:))
- [LowLevelInstanceData](/documentation/realitykit/lowlevelinstancedata)

#### Initializers

- [convenience init(instanceCount: Int) throws](/documentation/realitykit/lowlevelinstancedata/init(instancecount:))
- [init(instanceCount: Int, instanceCapacity: Int) throws](/documentation/realitykit/lowlevelinstancedata/init(instancecount:instancecapacity:))

#### Instance Properties

- [var instanceCapacity: Int](/documentation/realitykit/lowlevelinstancedata/instancecapacity)
- [var instanceCount: Int](/documentation/realitykit/lowlevelinstancedata/instancecount)

#### Instance Methods

- [func read(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelinstancedata/read(using:))
- [func replace(using: any MTLCommandBuffer) -> any MTLBuffer](/documentation/realitykit/lowlevelinstancedata/replace(using:))
- [func replaceMutableTransforms((UnsafeMutableBufferPointer<float4x4>) -> Void)](/documentation/realitykit/lowlevelinstancedata/replacemutabletransforms(_:))
- [func withMutableTransforms((UnsafeMutableBufferPointer<float4x4>) -> Void)](/documentation/realitykit/lowlevelinstancedata/withmutabletransforms(_:))
- [func withTransforms((UnsafeBufferPointer<float4x4>) -> Void)](/documentation/realitykit/lowlevelinstancedata/withtransforms(_:))

### Bounding box retrieval

- [BoundingBox](/documentation/realitykit/boundingbox)

#### Creating a bounding box

- [init()](/documentation/realitykit/boundingbox/init())
- [init(min: SIMD3<Float>, max: SIMD3<Float>)](/documentation/realitykit/boundingbox/init(min:max:))

#### Getting an empty box

- [static let empty: BoundingBox](/documentation/realitykit/boundingbox/empty)

#### Getting the box characteristics

- [var max: SIMD3<Float>](/documentation/realitykit/boundingbox/max)
- [var min: SIMD3<Float>](/documentation/realitykit/boundingbox/min)
- [var center: SIMD3<Float>](/documentation/realitykit/boundingbox/center)
- [var extents: SIMD3<Float>](/documentation/realitykit/boundingbox/extents)
- [var boundingRadius: Float](/documentation/realitykit/boundingbox/boundingradius)

#### Expanding boxes

- [func union(BoundingBox) -> BoundingBox](/documentation/realitykit/boundingbox/union(_:)-1y8hw)
- [func formUnion(BoundingBox)](/documentation/realitykit/boundingbox/formunion(_:)-5iy03)
- [func union(SIMD3<Float>) -> BoundingBox](/documentation/realitykit/boundingbox/union(_:)-g4th)
- [func formUnion(SIMD3<Float>)](/documentation/realitykit/boundingbox/formunion(_:)-6itj9)

#### Checking for overlap

- [func contains(BoundingBox) -> Bool](/documentation/realitykit/boundingbox/contains(_:)-5ux4h)
- [func contains(SIMD3<Float>) -> Bool](/documentation/realitykit/boundingbox/contains(_:)-92ap6)
- [func intersects(BoundingBox) -> Bool](/documentation/realitykit/boundingbox/intersects(_:))

#### Checking for separation

- [func distanceSquared(toPoint: SIMD3<Float>) -> Float](/documentation/realitykit/boundingbox/distancesquared(topoint:))

#### Transforming a bounding box

- [func transform(by: float4x4)](/documentation/realitykit/boundingbox/transform(by:))
- [func transformed(by: float4x4) -> BoundingBox](/documentation/realitykit/boundingbox/transformed(by:))

#### Operators

- [static func == (BoundingBox, BoundingBox) -> Bool](/documentation/realitykit/boundingbox/==(_:_:))

#### Initializers

- [init(Rect3D)](/documentation/realitykit/boundingbox/init(_:))

#### Instance Properties

- [var isEmpty: Bool](/documentation/realitykit/boundingbox/isempty)

#### Instance Methods

- [func contains(_:)](/documentation/realitykit/boundingbox/contains(_:))
- [func formUnion(_:)](/documentation/realitykit/boundingbox/formunion(_:))
- [func hash(into: inout Hasher)](/documentation/realitykit/boundingbox/hash(into:))
- [func union(_:)](/documentation/realitykit/boundingbox/union(_:))
- [OrientedBoundingBox](/documentation/realitykit/orientedboundingbox)

#### Initializers

- [init(orientation: simd_quatf, boundingBox: BoundingBox)](/documentation/realitykit/orientedboundingbox/init(orientation:boundingbox:))

#### Instance Properties

- [var boundingBox: BoundingBox](/documentation/realitykit/orientedboundingbox/boundingbox)
- [var orientation: simd_quatf](/documentation/realitykit/orientedboundingbox/orientation)

### Text generation options

- [MeshResource.GenerateTextOptions](/documentation/realitykit/meshresource/generatetextoptions)

#### Initializers

- [init()](/documentation/realitykit/meshresource/generatetextoptions/init())

#### Instance Properties

- [var containerFrame: CGRect?](/documentation/realitykit/meshresource/generatetextoptions/containerframe)
- [MeshResource.Font](/documentation/realitykit/meshresource/font)

### 2D path extrusion for 3D mesh creation

- [MeshResource.ShapeExtrusionOptions](/documentation/realitykit/meshresource/shapeextrusionoptions)

#### Structures

- [MeshResource.ShapeExtrusionOptions.MaterialAssignment](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct)

##### Initializers

- [init(assignAll: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(assignall:))
- [init(front: UInt32, back: UInt32, extrusion: UInt32, frontChamfer: UInt32, backChamfer: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(front:back:extrusion:frontchamfer:backchamfer:))

#### Initializers

- [init()](/documentation/realitykit/meshresource/shapeextrusionoptions/init())

#### Instance Properties

- [var boundaryResolution: MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/boundaryresolution)
- [var chamferMode: MeshResource.ShapeExtrusionOptions.ChamferMode](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.property)
- [var chamferProfile: Path?](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferprofile)
- [var chamferRadius: Float](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferradius)
- [var chamferResolution: MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/chamferresolution)
- [var extrusionMethod: MeshResource.ShapeExtrusionOptions.ExtrusionMethod](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.property)
- [var materialAssignment: MeshResource.ShapeExtrusionOptions.MaterialAssignment](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.property)

#### Enumerations

- [MeshResource.ShapeExtrusionOptions.ChamferMode](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum)

##### Enumeration Cases

- [case back](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/back)
- [case both](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/both)
- [case front](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/front)
- [MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution)

##### Enumeration Cases

- [case uniformSegmentsPerSpan(segmentCount: Int)](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution/uniformsegmentsperspan(segmentcount:))
- [MeshResource.ShapeExtrusionOptions.ExtrusionMethod](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum)

##### Enumeration Cases

- [case linear(depth: Float)](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/linear(depth:))
- [case tracePositions([SIMD3<Float>])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracepositions(_:))
- [case traceTransforms([simd_float4x4])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracetransforms(_:))
- [MeshResource.ShapeExtrusionOptions.MaterialAssignment](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct)

#### Initializers

- [init(assignAll: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(assignall:))
- [init(front: UInt32, back: UInt32, extrusion: UInt32, frontChamfer: UInt32, backChamfer: UInt32)](/documentation/realitykit/meshresource/shapeextrusionoptions/materialassignment-swift.struct/init(front:back:extrusion:frontchamfer:backchamfer:))
- [MeshResource.ShapeExtrusionOptions.ChamferMode](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum)

#### Enumeration Cases

- [case back](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/back)
- [case both](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/both)
- [case front](/documentation/realitykit/meshresource/shapeextrusionoptions/chamfermode-swift.enum/front)
- [MeshResource.ShapeExtrusionOptions.CurveStrokeResolution](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution)

#### Enumeration Cases

- [case uniformSegmentsPerSpan(segmentCount: Int)](/documentation/realitykit/meshresource/shapeextrusionoptions/curvestrokeresolution/uniformsegmentsperspan(segmentcount:))
- [MeshResource.ShapeExtrusionOptions.ExtrusionMethod](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum)

#### Enumeration Cases

- [case linear(depth: Float)](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/linear(depth:))
- [case tracePositions([SIMD3<Float>])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracepositions(_:))
- [case traceTransforms([simd_float4x4])](/documentation/realitykit/meshresource/shapeextrusionoptions/extrusionmethod-swift.enum/tracetransforms(_:))

### Mesh description

- [MeshBuffer](/documentation/realitykit/meshbuffer)

#### Creating a mesh buffer

- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-13uzl)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-1f0ai)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-1hyiz)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-2okpc)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-3bqai)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-3pbx9)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-4ahf1)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-5a11h)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-5sh0b)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-650mf)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-6hldv)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-77mou)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-7d6t8)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-8m4zg)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-8p5ux)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-8yhn7)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-94e5y)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-991gl)
- [init<S>(S)](/documentation/realitykit/meshbuffer/init(_:)-9eppl)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-9o6sp)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-9tja8)
- [init([Element])](/documentation/realitykit/meshbuffer/init(_:)-11fcy)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-2f47d)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-2nr7l)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-2wcfg)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-3m3mo)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-4kg29)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-4yxh4)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-5mhon)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-76tes)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-7gw7i)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-8dbzg)
- [init(elements: [Element], indices: [UInt32])](/documentation/realitykit/meshbuffer/init(elements:indices:)-97yff)

#### Inspecting a mesh

- [var elements: [Element]](/documentation/realitykit/meshbuffer/elements)
- [var rate: MeshBuffers.Rate](/documentation/realitykit/meshbuffer/rate)

#### Iterating the elements of a buffer

- [func forEach((Element, Element) throws -> Void) rethrows](/documentation/realitykit/meshbuffer/foreach(_:)-53vhs)
- [func forEach((Element, Element, Element) throws -> Void) rethrows](/documentation/realitykit/meshbuffer/foreach(_:)-7o3tb)
- [func forEach((Element, Element, Element, Element) throws -> Void) rethrows](/documentation/realitykit/meshbuffer/foreach(_:)-xhri)
- [func usingRate(MeshBuffers.Rate) -> MeshBuffer<Element>](/documentation/realitykit/meshbuffer/usingrate(_:))

#### Initializers

- [init(_:)](/documentation/realitykit/meshbuffer/init(_:))
- [init(elements:indices:)](/documentation/realitykit/meshbuffer/init(elements:indices:))

#### Instance Properties

- [let count: Int](/documentation/realitykit/meshbuffer/count)

#### Instance Methods

- [func forEach(_:)](/documentation/realitykit/meshbuffer/foreach(_:))
- [MeshBufferContainer](/documentation/realitykit/meshbuffercontainer)

#### Instance Properties

- [var bitangents: MeshBuffers.Tangents?](/documentation/realitykit/meshbuffercontainer/bitangents)
- [var blendShapeNames: [String]](/documentation/realitykit/meshbuffercontainer/blendshapenames)
- [var buffers: [MeshBuffers.Identifier : AnyMeshBuffer]](/documentation/realitykit/meshbuffercontainer/buffers)
- [var normals: MeshBuffers.Normals?](/documentation/realitykit/meshbuffercontainer/normals)
- [var positions: MeshBuffers.Positions](/documentation/realitykit/meshbuffercontainer/positions)
- [var tangents: MeshBuffers.Tangents?](/documentation/realitykit/meshbuffercontainer/tangents)
- [var textureCoordinates: MeshBuffers.TextureCoordinates?](/documentation/realitykit/meshbuffercontainer/texturecoordinates)

#### Instance Methods

- [func blendShapeOffsets(named: String) -> MeshBuffers.BlendShapeOffsets?](/documentation/realitykit/meshbuffercontainer/blendshapeoffsets(named:))
- [func setBlendShapeOffsets(named: String, buffer: MeshBuffers.BlendShapeOffsets?)](/documentation/realitykit/meshbuffercontainer/setblendshapeoffsets(named:buffer:))

#### Subscripts

- [subscript<S>(S) -> MeshBuffer<S.Element>?](/documentation/realitykit/meshbuffercontainer/subscript(_:))
- [MeshBufferSemantic](/documentation/realitykit/meshbuffersemantic)

#### Associated Types

- [Element](/documentation/realitykit/meshbuffersemantic/element)

#### Instance Properties

- [var id: MeshBuffers.Identifier](/documentation/realitykit/meshbuffersemantic/id)
- [MeshBuffers](/documentation/realitykit/meshbuffers)

#### Structures

- [MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier)

##### Instance Properties

- [let isBlendShape: Bool](/documentation/realitykit/meshbuffers/identifier/isblendshape)
- [let isCustom: Bool](/documentation/realitykit/meshbuffers/identifier/iscustom)
- [let name: String](/documentation/realitykit/meshbuffers/identifier/name)

##### Type Properties

- [static let bitangents: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/bitangents)
- [static let jointInfluences: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/jointinfluences)
- [static let normals: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/normals)
- [static let positions: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/positions)
- [static let tangents: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/tangents)
- [static let textureCoordinates: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/texturecoordinates)
- [static let triangleIndices: MeshBuffers.Identifier](/documentation/realitykit/meshbuffers/identifier/triangleindices)
- [MeshBuffers.Semantic](/documentation/realitykit/meshbuffers/semantic)

#### Type Aliases

- [MeshBuffers.BlendShapeOffsets](/documentation/realitykit/meshbuffers/blendshapeoffsets)
- [MeshBuffers.JointInfluences](/documentation/realitykit/meshbuffers/jointinfluences-swift.typealias)
- [MeshBuffers.Normals](/documentation/realitykit/meshbuffers/normals-swift.typealias)
- [MeshBuffers.Positions](/documentation/realitykit/meshbuffers/positions-swift.typealias)
- [MeshBuffers.Tangents](/documentation/realitykit/meshbuffers/tangents-swift.typealias)
- [MeshBuffers.TextureCoordinates](/documentation/realitykit/meshbuffers/texturecoordinates-swift.typealias)
- [MeshBuffers.TriangleIndices](/documentation/realitykit/meshbuffers/triangleindices-swift.typealias)

#### Type Properties

- [static let bitangents: MeshBuffers.Semantic<SIMD3<Float>>](/documentation/realitykit/meshbuffers/bitangents)
- [static let jointInfluences: MeshBuffers.Semantic<MeshJointInfluence>](/documentation/realitykit/meshbuffers/jointinfluences-swift.type.property)
- [static let normals: MeshBuffers.Semantic<SIMD3<Float>>](/documentation/realitykit/meshbuffers/normals-swift.type.property)
- [static let positions: MeshBuffers.Semantic<SIMD3<Float>>](/documentation/realitykit/meshbuffers/positions-swift.type.property)
- [static let tangents: MeshBuffers.Semantic<SIMD3<Float>>](/documentation/realitykit/meshbuffers/tangents-swift.type.property)
- [static let textureCoordinates: MeshBuffers.Semantic<SIMD2<Float>>](/documentation/realitykit/meshbuffers/texturecoordinates-swift.type.property)
- [static let triangleIndices: MeshBuffers.Semantic<UInt32>](/documentation/realitykit/meshbuffers/triangleindices-swift.type.property)

#### Type Methods

- [static func blendShapeOffsets(named: String) -> MeshBuffers.Semantic<SIMD3<Float>>](/documentation/realitykit/meshbuffers/blendshapeoffsets(named:))
- [static func custom<Value>(String, type: Value.Type) -> MeshBuffers.Semantic<Value>](/documentation/realitykit/meshbuffers/custom(_:type:))

#### Enumerations

- [MeshBuffers.ElementType](/documentation/realitykit/meshbuffers/elementtype)

##### Enumeration Cases

- [case double](/documentation/realitykit/meshbuffers/elementtype/double)
- [case float](/documentation/realitykit/meshbuffers/elementtype/float)
- [case int16](/documentation/realitykit/meshbuffers/elementtype/int16)
- [case int32](/documentation/realitykit/meshbuffers/elementtype/int32)
- [case int8](/documentation/realitykit/meshbuffers/elementtype/int8)
- [case jointInfluence](/documentation/realitykit/meshbuffers/elementtype/jointinfluence)
- [case simd2Float](/documentation/realitykit/meshbuffers/elementtype/simd2float)
- [case simd3Float](/documentation/realitykit/meshbuffers/elementtype/simd3float)
- [case simd4Float](/documentation/realitykit/meshbuffers/elementtype/simd4float)
- [case uInt16](/documentation/realitykit/meshbuffers/elementtype/uint16)
- [case uInt32](/documentation/realitykit/meshbuffers/elementtype/uint32)
- [case uInt8](/documentation/realitykit/meshbuffers/elementtype/uint8)
- [MeshBuffers.Rate](/documentation/realitykit/meshbuffers/rate)

##### Enumeration Cases

- [case face](/documentation/realitykit/meshbuffers/rate/face)
- [case faceVarying](/documentation/realitykit/meshbuffers/rate/facevarying)
- [case vertex](/documentation/realitykit/meshbuffers/rate/vertex)
- [AnyMeshBuffer](/documentation/realitykit/anymeshbuffer)

#### Inspecting a mesh buffer

- [var elementType: MeshBuffers.ElementType](/documentation/realitykit/anymeshbuffer/elementtype)
- [var id: MeshBuffers.Identifier](/documentation/realitykit/anymeshbuffer/id)
- [var rate: MeshBuffers.Rate](/documentation/realitykit/anymeshbuffer/rate)
- [func get<Value>(Value.Type) -> MeshBuffer<Value>?](/documentation/realitykit/anymeshbuffer/get(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/anymeshbuffer/count)
- [MeshInstanceCollection](/documentation/realitykit/meshinstancecollection)

#### Creating a collection

- [init()](/documentation/realitykit/meshinstancecollection/init())
- [init([MeshResource.Instance])](/documentation/realitykit/meshinstancecollection/init(_:))

#### Using the collection

- [func insert(MeshResource.Instance) -> Bool](/documentation/realitykit/meshinstancecollection/insert(_:))
- [func remove(id: String) -> MeshResource.Instance?](/documentation/realitykit/meshinstancecollection/remove(id:))
- [func removeAll()](/documentation/realitykit/meshinstancecollection/removeall())
- [func update(MeshResource.Instance) -> MeshResource.Instance?](/documentation/realitykit/meshinstancecollection/update(_:))
- [subscript(String) -> MeshResource.Instance?](/documentation/realitykit/meshinstancecollection/subscript(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/meshinstancecollection/count)
- [var isEmpty: Bool](/documentation/realitykit/meshinstancecollection/isempty)
- [MeshModelCollection](/documentation/realitykit/meshmodelcollection)

#### Creating a collection

- [init()](/documentation/realitykit/meshmodelcollection/init())
- [init([MeshResource.Model])](/documentation/realitykit/meshmodelcollection/init(_:))

#### Using the collection

- [func insert(MeshResource.Model) -> Bool](/documentation/realitykit/meshmodelcollection/insert(_:))
- [func remove(id: String) -> MeshResource.Model?](/documentation/realitykit/meshmodelcollection/remove(id:))
- [func removeAll()](/documentation/realitykit/meshmodelcollection/removeall())
- [func update(MeshResource.Model) -> MeshResource.Model?](/documentation/realitykit/meshmodelcollection/update(_:))
- [subscript(String) -> MeshResource.Model?](/documentation/realitykit/meshmodelcollection/subscript(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/meshmodelcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/meshmodelcollection/isempty)
- [MeshPartCollection](/documentation/realitykit/meshpartcollection)

#### Creating a collection

- [init()](/documentation/realitykit/meshpartcollection/init())
- [init([MeshResource.Part])](/documentation/realitykit/meshpartcollection/init(_:))

#### Using the collection

- [func insert(MeshResource.Part) -> Bool](/documentation/realitykit/meshpartcollection/insert(_:))
- [func remove(id: String) -> MeshResource.Part?](/documentation/realitykit/meshpartcollection/remove(id:))
- [func removeAll()](/documentation/realitykit/meshpartcollection/removeall())
- [func update(MeshResource.Part) -> MeshResource.Part?](/documentation/realitykit/meshpartcollection/update(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/meshpartcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/meshpartcollection/isempty)

#### Subscripts

- [subscript(String) -> MeshResource.Part?](/documentation/realitykit/meshpartcollection/subscript(_:))

### Mesh skeletons

- [MeshResource.Skeleton](/documentation/realitykit/meshresource/skeleton)

#### Structures

- [MeshResource.Skeleton.Joint](/documentation/realitykit/meshresource/skeleton/joint)

##### Initializers

- [init(name: String, parentIndex: Int?, inverseBindPoseMatrix: simd_float4x4, restPoseTransform: Transform)](/documentation/realitykit/meshresource/skeleton/joint/init(name:parentindex:inversebindposematrix:restposetransform:))

##### Instance Properties

- [var inverseBindPoseMatrix: simd_float4x4](/documentation/realitykit/meshresource/skeleton/joint/inversebindposematrix)
- [var name: String](/documentation/realitykit/meshresource/skeleton/joint/name)
- [var parentIndex: Int?](/documentation/realitykit/meshresource/skeleton/joint/parentindex)
- [var restPoseTransform: Transform](/documentation/realitykit/meshresource/skeleton/joint/restposetransform)

#### Initializers

- [init?(id: String, jointNames: [String], inverseBindPoseMatrices: [simd_float4x4], restPoseTransforms: [Transform]?, parentIndices: [Int?]?)](/documentation/realitykit/meshresource/skeleton/init(id:jointnames:inversebindposematrices:restposetransforms:parentindices:))
- [init(id: String, joints: [MeshResource.Skeleton.Joint])](/documentation/realitykit/meshresource/skeleton/init(id:joints:))

#### Instance Properties

- [var id: String](/documentation/realitykit/meshresource/skeleton/id)
- [var joints: [MeshResource.Skeleton.Joint]](/documentation/realitykit/meshresource/skeleton/joints)
- [MeshResource.Skeleton.Joint](/documentation/realitykit/meshresource/skeleton/joint)

#### Initializers

- [init(name: String, parentIndex: Int?, inverseBindPoseMatrix: simd_float4x4, restPoseTransform: Transform)](/documentation/realitykit/meshresource/skeleton/joint/init(name:parentindex:inversebindposematrix:restposetransform:))

#### Instance Properties

- [var inverseBindPoseMatrix: simd_float4x4](/documentation/realitykit/meshresource/skeleton/joint/inversebindposematrix)
- [var name: String](/documentation/realitykit/meshresource/skeleton/joint/name)
- [var parentIndex: Int?](/documentation/realitykit/meshresource/skeleton/joint/parentindex)
- [var restPoseTransform: Transform](/documentation/realitykit/meshresource/skeleton/joint/restposetransform)
- [MeshSkeletonCollection](/documentation/realitykit/meshskeletoncollection)

#### Initializers

- [init()](/documentation/realitykit/meshskeletoncollection/init())
- [init([MeshResource.Skeleton])](/documentation/realitykit/meshskeletoncollection/init(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/meshskeletoncollection/count)
- [var isEmpty: Bool](/documentation/realitykit/meshskeletoncollection/isempty)

#### Instance Methods

- [func insert(MeshResource.Skeleton) -> Bool](/documentation/realitykit/meshskeletoncollection/insert(_:))
- [func remove(id: String) -> MeshResource.Skeleton?](/documentation/realitykit/meshskeletoncollection/remove(id:))
- [func removeAll()](/documentation/realitykit/meshskeletoncollection/removeall())
- [func update(MeshResource.Skeleton) -> MeshResource.Skeleton?](/documentation/realitykit/meshskeletoncollection/update(_:))

#### Subscripts

- [subscript(String) -> MeshResource.Skeleton?](/documentation/realitykit/meshskeletoncollection/subscript(_:))
- [MeshJointInfluence](/documentation/realitykit/meshjointinfluence)

#### Initializers

- [init()](/documentation/realitykit/meshjointinfluence/init())
- [init(jointIndex: Int, weight: Float)](/documentation/realitykit/meshjointinfluence/init(jointindex:weight:))

#### Instance Properties

- [var jointIndex: Int](/documentation/realitykit/meshjointinfluence/jointindex)
- [var weight: Float](/documentation/realitykit/meshjointinfluence/weight)
- [MeshResource.JointInfluences](/documentation/realitykit/meshresource/jointinfluences)

#### Initializers

- [init(influences: MeshBuffers.JointInfluences, influencesPerVertex: Int)](/documentation/realitykit/meshresource/jointinfluences/init(influences:influencespervertex:))

#### Instance Properties

- [var influences: MeshBuffers.JointInfluences](/documentation/realitykit/meshresource/jointinfluences/influences)

### Mesh resource data

- [MeshResource.Contents](/documentation/realitykit/meshresource/contents-swift.struct)

#### Initializers

- [init()](/documentation/realitykit/meshresource/contents-swift.struct/init())

#### Instance Properties

- [var instances: MeshInstanceCollection](/documentation/realitykit/meshresource/contents-swift.struct/instances)
- [var models: MeshModelCollection](/documentation/realitykit/meshresource/contents-swift.struct/models)
- [var skeletons: MeshSkeletonCollection](/documentation/realitykit/meshresource/contents-swift.struct/skeletons)
- [MeshResource.Instance](/documentation/realitykit/meshresource/instance)

#### Initializers

- [init(id: String, model: String, at: simd_float4x4?)](/documentation/realitykit/meshresource/instance/init(id:model:at:))

#### Instance Properties

- [var model: String](/documentation/realitykit/meshresource/instance/model)
- [var transform: simd_float4x4](/documentation/realitykit/meshresource/instance/transform)
- [MeshResource.Model](/documentation/realitykit/meshresource/model)

#### Initializers

- [init(id: String, descriptors: [MeshDescriptor]) throws](/documentation/realitykit/meshresource/model/init(id:descriptors:))
- [init(id: String, parts: [MeshResource.Part])](/documentation/realitykit/meshresource/model/init(id:parts:))

#### Instance Properties

- [var parts: MeshPartCollection](/documentation/realitykit/meshresource/model/parts)
- [MeshResource.Part](/documentation/realitykit/meshresource/part)

#### Initializers

- [init(id: String, materialIndex: Int)](/documentation/realitykit/meshresource/part/init(id:materialindex:))

#### Instance Properties

- [var jointInfluences: MeshResource.JointInfluences?](/documentation/realitykit/meshresource/part/jointinfluences)
- [var materialIndex: Int](/documentation/realitykit/meshresource/part/materialindex)
- [var skeletonID: String?](/documentation/realitykit/meshresource/part/skeletonid)
- [var triangleIndices: MeshBuffers.TriangleIndices?](/documentation/realitykit/meshresource/part/triangleindices)

### Blend shape management

- [BlendShapeWeightsComponent](/documentation/realitykit/blendshapeweightscomponent)

#### Initializers

- [init(weightsMapping: BlendShapeWeightsMapping)](/documentation/realitykit/blendshapeweightscomponent/init(weightsmapping:))

#### Instance Properties

- [var weightSet: BlendShapeWeightsSet](/documentation/realitykit/blendshapeweightscomponent/weightset)
- [BlendShapeWeightsMapping](/documentation/realitykit/blendshapeweightsmapping)

#### Initializers

- [init(blendShapeName: String, weightNames: [String])](/documentation/realitykit/blendshapeweightsmapping/init(blendshapename:weightnames:))
- [init(meshResource: MeshResource)](/documentation/realitykit/blendshapeweightsmapping/init(meshresource:))
- [BlendShapeWeights](/documentation/realitykit/blendshapeweights)

#### Operators

- [static func == (BlendShapeWeights, BlendShapeWeights) -> Bool](/documentation/realitykit/blendshapeweights/==(_:_:))

#### Initializers

- [init()](/documentation/realitykit/blendshapeweights/init())
- [init<S>(S)](/documentation/realitykit/blendshapeweights/init(_:))
- [init(arrayLiteral: Float...)](/documentation/realitykit/blendshapeweights/init(arrayliteral:))

#### Instance Properties

- [var endIndex: BlendShapeWeights.Index](/documentation/realitykit/blendshapeweights/endindex)
- [var startIndex: BlendShapeWeights.Index](/documentation/realitykit/blendshapeweights/startindex)

#### Instance Methods

- [func index(after: BlendShapeWeights.Index) -> BlendShapeWeights.Index](/documentation/realitykit/blendshapeweights/index(after:))
- [func index(before: BlendShapeWeights.Index) -> BlendShapeWeights.Index](/documentation/realitykit/blendshapeweights/index(before:))

#### Subscripts

- [subscript(BlendShapeWeights.Index) -> Float](/documentation/realitykit/blendshapeweights/subscript(_:))

#### Type Aliases

- [BlendShapeWeights.ArrayLiteralElement](/documentation/realitykit/blendshapeweights/arrayliteralelement)
- [BlendShapeWeights.Element](/documentation/realitykit/blendshapeweights/element)
- [BlendShapeWeights.Index](/documentation/realitykit/blendshapeweights/index)
- [BlendShapeWeightsData](/documentation/realitykit/blendshapeweightsdata)

#### Initializers

- [init(id: BlendShapeWeightsData.ID, weights: [(String, BlendShapeWeights.Element)])](/documentation/realitykit/blendshapeweightsdata/init(id:weights:))

#### Instance Properties

- [var id: BlendShapeWeightsData.ID](/documentation/realitykit/blendshapeweightsdata/id)
- [var weightNames: [String]](/documentation/realitykit/blendshapeweightsdata/weightnames)
- [var weights: BlendShapeWeights](/documentation/realitykit/blendshapeweightsdata/weights)
- [BlendShapeWeightsSet](/documentation/realitykit/blendshapeweightsset)

#### Initializers

- [init()](/documentation/realitykit/blendshapeweightsset/init())

#### Instance Properties

- [var count: Int](/documentation/realitykit/blendshapeweightsset/count)
- [var `default`: BlendShapeWeightsSet.Element?](/documentation/realitykit/blendshapeweightsset/default)
- [var isEmpty: Bool](/documentation/realitykit/blendshapeweightsset/isempty)

#### Instance Methods

- [func contains(String) -> Bool](/documentation/realitykit/blendshapeweightsset/contains(_:))
- [func index(of: String) -> BlendShapeWeightsSet.Index?](/documentation/realitykit/blendshapeweightsset/index(of:))
- [func set(BlendShapeWeightsSet.Element) -> BlendShapeWeightsSet.Element?](/documentation/realitykit/blendshapeweightsset/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/blendshapeweightsset/subscript(_:))

#### Default Implementations

- [Collection Implementations](/documentation/realitykit/blendshapeweightsset/collection-implementations)

##### Instance Properties

- [var endIndex: BlendShapeWeightsSet.Index](/documentation/realitykit/blendshapeweightsset/endindex)
- [var startIndex: BlendShapeWeightsSet.Index](/documentation/realitykit/blendshapeweightsset/startindex)

##### Instance Methods

- [func index(after: BlendShapeWeightsSet.Index) -> BlendShapeWeightsSet.Index](/documentation/realitykit/blendshapeweightsset/index(after:))

##### Subscripts

- [subscript(BlendShapeWeightsSet.Index) -> BlendShapeWeightsSet.Element](/documentation/realitykit/blendshapeweightsset/subscript(_:)-9wfe8)

### Entity compliance

- [HasModel](/documentation/realitykit/hasmodel)

#### Retrieving a model

- [var model: ModelComponent?](/documentation/realitykit/hasmodel/model)

#### Managing joints

- [var jointNames: [String]](/documentation/realitykit/hasmodel/jointnames)
- [var jointTransforms: [Transform]](/documentation/realitykit/hasmodel/jointtransforms)

#### Instance Properties

- [var blendWeightNames: [[String]]](/documentation/realitykit/hasmodel/blendweightnames)
- [var blendWeights: [[Float]]](/documentation/realitykit/hasmodel/blendweights)
- [var modelDebugOptions: ModelDebugOptionsComponent?](/documentation/realitykit/hasmodel/modeldebugoptions)
- [Materials, textures, and shaders](/documentation/realitykit/scene-content-materials-and-shaders)

### Simple materials

- [SimpleMaterial](/documentation/realitykit/simplematerial)

#### Creating a simple material

- [init()](/documentation/realitykit/simplematerial/init())
- [init(color: SimpleMaterial.Color, roughness: MaterialScalarParameter, isMetallic: Bool)](/documentation/realitykit/simplematerial/init(color:roughness:ismetallic:)-1ebae)

#### Characterizing a material

- [var color: SimpleMaterial.BaseColor](/documentation/realitykit/simplematerial/color)
- [var baseColor: MaterialColorParameter](/documentation/realitykit/simplematerial/basecolor-swift.property)
- [SimpleMaterial.BaseColor](/documentation/realitykit/simplematerial/basecolor-swift.typealias)
- [var tintColor: NSColor](/documentation/realitykit/simplematerial/tintcolor-6v03h)
- [SimpleMaterial.Texture](/documentation/realitykit/simplematerial/texture)
- [var metallic: MaterialScalarParameter](/documentation/realitykit/simplematerial/metallic)
- [var roughness: MaterialScalarParameter](/documentation/realitykit/simplematerial/roughness)

#### Initializers

- [init(color:roughness:isMetallic:)](/documentation/realitykit/simplematerial/init(color:roughness:ismetallic:))

#### Instance Properties

- [var faceCulling: SimpleMaterial.FaceCulling](/documentation/realitykit/simplematerial/faceculling-swift.property)
- [var readsDepth: Bool](/documentation/realitykit/simplematerial/readsdepth)
- [var tintColor: UIColor](/documentation/realitykit/simplematerial/tintcolor-74a0x)
- [var triangleFillMode: SimpleMaterial.TriangleFillMode](/documentation/realitykit/simplematerial/trianglefillmode-swift.property)
- [var writesDepth: Bool](/documentation/realitykit/simplematerial/writesdepth)

#### Type Aliases

- [SimpleMaterial.FaceCulling](/documentation/realitykit/simplematerial/faceculling-swift.typealias)
- [SimpleMaterial.TriangleFillMode](/documentation/realitykit/simplematerial/trianglefillmode-swift.typealias)
- [SimpleMaterial.BaseColor](/documentation/realitykit/simplematerial/basecolor-swift.typealias)
- [SimpleMaterial.Texture](/documentation/realitykit/simplematerial/texture)
- [SimpleMaterial.FaceCulling](/documentation/realitykit/simplematerial/faceculling-swift.typealias)
- [SimpleMaterial.TriangleFillMode](/documentation/realitykit/simplematerial/trianglefillmode-swift.typealias)

### Unlit materials

- [UnlitMaterial](/documentation/realitykit/unlitmaterial)

#### Creating an unlit material

- [init()](/documentation/realitykit/unlitmaterial/init())
- [init(color: NSColor)](/documentation/realitykit/unlitmaterial/init(color:)-8xgq2)
- [init(applyPostProcessToneMap: Bool)](/documentation/realitykit/unlitmaterial/init(applypostprocesstonemap:))
- [init(color: NSColor, applyPostProcessToneMap: Bool)](/documentation/realitykit/unlitmaterial/init(color:applypostprocesstonemap:)-899er)
- [init(program: UnlitMaterial.Program)](/documentation/realitykit/unlitmaterial/init(program:))
- [init(texture: TextureResource)](/documentation/realitykit/unlitmaterial/init(texture:))

#### Configuring base color

- [var color: UnlitMaterial.BaseColor](/documentation/realitykit/unlitmaterial/color)
- [var baseColor: MaterialColorParameter](/documentation/realitykit/unlitmaterial/basecolor-swift.property)

#### Tinting an unlit material

- [var tintColor: NSColor](/documentation/realitykit/unlitmaterial/tintcolor-9v1sw)

#### Controlling opacity

- [var opacityThreshold: Float?](/documentation/realitykit/unlitmaterial/opacitythreshold)
- [var blending: UnlitMaterial.Blending](/documentation/realitykit/unlitmaterial/blending-swift.property)

#### Classes

- [UnlitMaterial.Program](/documentation/realitykit/unlitmaterial/program-swift.class)

##### Structures

- [UnlitMaterial.Program.Descriptor](/documentation/realitykit/unlitmaterial/program-swift.class/descriptor-swift.struct)

###### Initializers

- [init()](/documentation/realitykit/unlitmaterial/program-swift.class/descriptor-swift.struct/init())

###### Instance Properties

- [var applyPostProcessToneMap: Bool](/documentation/realitykit/unlitmaterial/program-swift.class/descriptor-swift.struct/applypostprocesstonemap)
- [var blendMode: MaterialParameterTypes.BlendMode?](/documentation/realitykit/unlitmaterial/program-swift.class/descriptor-swift.struct/blendmode)

##### Initializers

- [init(descriptor: UnlitMaterial.Program.Descriptor) async](/documentation/realitykit/unlitmaterial/program-swift.class/init(descriptor:))

##### Instance Properties

- [let descriptor: UnlitMaterial.Program.Descriptor](/documentation/realitykit/unlitmaterial/program-swift.class/descriptor-swift.property)

#### Initializers

- [init(color:)](/documentation/realitykit/unlitmaterial/init(color:))
- [init(color:applyPostProcessToneMap:)](/documentation/realitykit/unlitmaterial/init(color:applypostprocesstonemap:))

#### Instance Properties

- [var faceCulling: UnlitMaterial.FaceCulling](/documentation/realitykit/unlitmaterial/faceculling-swift.property)
- [var program: UnlitMaterial.Program](/documentation/realitykit/unlitmaterial/program-swift.property)
- [var readsDepth: Bool](/documentation/realitykit/unlitmaterial/readsdepth)
- [var secondaryTextureCoordinateTransform: UnlitMaterial.TextureCoordinateTransform](/documentation/realitykit/unlitmaterial/secondarytexturecoordinatetransform)
- [var textureCoordinateTransform: UnlitMaterial.TextureCoordinateTransform](/documentation/realitykit/unlitmaterial/texturecoordinatetransform-swift.property)
- [var tintColor: UIColor](/documentation/realitykit/unlitmaterial/tintcolor-k1do)
- [var triangleFillMode: UnlitMaterial.TriangleFillMode](/documentation/realitykit/unlitmaterial/trianglefillmode-swift.property)
- [var writesDepth: Bool](/documentation/realitykit/unlitmaterial/writesdepth)

#### Type Aliases

- [UnlitMaterial.BaseColor](/documentation/realitykit/unlitmaterial/basecolor-swift.typealias)
- [UnlitMaterial.Blending](/documentation/realitykit/unlitmaterial/blending-swift.typealias)
- [UnlitMaterial.FaceCulling](/documentation/realitykit/unlitmaterial/faceculling-swift.typealias)
- [UnlitMaterial.Texture](/documentation/realitykit/unlitmaterial/texture)
- [UnlitMaterial.TextureCoordinateTransform](/documentation/realitykit/unlitmaterial/texturecoordinatetransform-swift.typealias)
- [UnlitMaterial.TriangleFillMode](/documentation/realitykit/unlitmaterial/trianglefillmode-swift.typealias)
- [UnlitMaterial.BaseColor](/documentation/realitykit/unlitmaterial/basecolor-swift.typealias)
- [UnlitMaterial.Blending](/documentation/realitykit/unlitmaterial/blending-swift.typealias)
- [UnlitMaterial.Texture](/documentation/realitykit/unlitmaterial/texture)
- [UnlitMaterial.FaceCulling](/documentation/realitykit/unlitmaterial/faceculling-swift.typealias)
- [UnlitMaterial.TextureCoordinateTransform](/documentation/realitykit/unlitmaterial/texturecoordinatetransform-swift.typealias)
- [UnlitMaterial.TriangleFillMode](/documentation/realitykit/unlitmaterial/trianglefillmode-swift.typealias)

### Realistic materials

- [Applying realistic material and lighting effects to entities](/documentation/realitykit/applying-realistic-material-and-lighting-effects-to-entities)
- [PhysicallyBasedMaterial](/documentation/realitykit/physicallybasedmaterial)

#### Creating a physically based material

- [init()](/documentation/realitykit/physicallybasedmaterial/init())
- [init(program: PhysicallyBasedMaterial.Program)](/documentation/realitykit/physicallybasedmaterial/init(program:))

#### Setting the core properties

- [var baseColor: PhysicallyBasedMaterial.BaseColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.property)
- [var roughness: PhysicallyBasedMaterial.Roughness](/documentation/realitykit/physicallybasedmaterial/roughness-swift.property)
- [var metallic: PhysicallyBasedMaterial.Metallic](/documentation/realitykit/physicallybasedmaterial/metallic-swift.property)
- [var normal: PhysicallyBasedMaterial.Normal](/documentation/realitykit/physicallybasedmaterial/normal-swift.property)
- [var ambientOcclusion: PhysicallyBasedMaterial.AmbientOcclusion](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.property)
- [var specular: PhysicallyBasedMaterial.Specular](/documentation/realitykit/physicallybasedmaterial/specular-swift.property)
- [var clearcoat: PhysicallyBasedMaterial.Clearcoat](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.property)
- [var clearcoatRoughness: PhysicallyBasedMaterial.ClearcoatRoughness](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.property)
- [var clearcoatNormal: PhysicallyBasedMaterial.ClearcoatNormal](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.property)

#### Configuring transparency and highlights

- [var blending: PhysicallyBasedMaterial.Blending](/documentation/realitykit/physicallybasedmaterial/blending-swift.property)
- [var sheen: PhysicallyBasedMaterial.SheenColor?](/documentation/realitykit/physicallybasedmaterial/sheen)

#### Adding anisotropy

- [var anisotropyLevel: PhysicallyBasedMaterial.AnisotropyLevel](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.property)
- [var anisotropyAngle: PhysicallyBasedMaterial.AnisotropyAngle](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.property)

#### Adding light emission

- [var emissiveIntensity: Float](/documentation/realitykit/physicallybasedmaterial/emissiveintensity)
- [var emissiveColor: PhysicallyBasedMaterial.EmissiveColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.property)

#### Modifying texture coordinates

- [var textureCoordinateTransform: PhysicallyBasedMaterial.TextureCoordinateTransform](/documentation/realitykit/physicallybasedmaterial/texturecoordinatetransform-swift.property)
- [var secondaryTextureCoordinateTransform: PhysicallyBasedMaterial.TextureCoordinateTransform](/documentation/realitykit/physicallybasedmaterial/secondarytexturecoordinatetransform)

#### Culling unnecessary polygons

- [var faceCulling: PhysicallyBasedMaterial.FaceCulling](/documentation/realitykit/physicallybasedmaterial/faceculling-swift.property)

#### Setting depth testing properties

- [var readsDepth: Bool](/documentation/realitykit/physicallybasedmaterial/readsdepth)
- [var writesDepth: Bool](/documentation/realitykit/physicallybasedmaterial/writesdepth)

#### Setting shader properties

- [var program: PhysicallyBasedMaterial.Program](/documentation/realitykit/physicallybasedmaterial/program-swift.property)

#### Classes

- [PhysicallyBasedMaterial.Program](/documentation/realitykit/physicallybasedmaterial/program-swift.class)

##### Structures

- [PhysicallyBasedMaterial.Program.Descriptor](/documentation/realitykit/physicallybasedmaterial/program-swift.class/descriptor-swift.struct)

###### Initializers

- [init()](/documentation/realitykit/physicallybasedmaterial/program-swift.class/descriptor-swift.struct/init())

###### Instance Properties

- [var blendMode: MaterialParameterTypes.BlendMode?](/documentation/realitykit/physicallybasedmaterial/program-swift.class/descriptor-swift.struct/blendmode)

##### Initializers

- [init(descriptor: PhysicallyBasedMaterial.Program.Descriptor) async](/documentation/realitykit/physicallybasedmaterial/program-swift.class/init(descriptor:))

##### Instance Properties

- [let descriptor: PhysicallyBasedMaterial.Program.Descriptor](/documentation/realitykit/physicallybasedmaterial/program-swift.class/descriptor-swift.property)

#### Structures

- [PhysicallyBasedMaterial.AmbientOcclusion](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct)

##### Creating an ambient occlusion object

- [init(texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/init(texture:))
- [init(CustomMaterial.AmbientOcclusion)](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/init(_:))

##### Accessing ambient occlusion values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/texturesemantic)
- [PhysicallyBasedMaterial.AnisotropyAngle](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct)

##### Creating an anisotropy angle object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/init(scale:texture:))

##### Accessing anisotropy angle values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/scale)
- [PhysicallyBasedMaterial.AnisotropyLevel](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct)

##### Creating an anisotropy level object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/init(scale:texture:))

##### Accessing anisotropy level values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/scale)
- [PhysicallyBasedMaterial.BaseColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct)

##### Creating a base color object

- [init(tint: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:)-2wriz)
- [init(tint: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:)-5jeqr)
- [init(CustomMaterial.BaseColor)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(_:))

##### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/texturesemantic)

##### Initializers

- [init(tint:texture:)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:))

##### Instance Properties

- [var tint: UIColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/tint-2znu0)
- [var tint: NSColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/tint-6heih)
- [PhysicallyBasedMaterial.Clearcoat](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct)

##### Creating a clearcoat object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Clearcoat)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(_:))

##### Accessing clearcoat values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/scale)
- [PhysicallyBasedMaterial.ClearcoatNormal](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.struct)

##### Initializers

- [init(CustomMaterial.ClearcoatNormal)](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.struct/init(_:))
- [init(texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.struct/init(texture:))

##### Instance Properties

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.struct/texture)

##### Type Properties

- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/clearcoatnormal-swift.struct/texturesemantic)
- [PhysicallyBasedMaterial.ClearcoatRoughness](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct)

##### Creating a clearcoat roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(scale:texture:))
- [init(CustomMaterial.ClearcoatRoughness)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(_:))

##### Accessing clearcoat roughness values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/scale)
- [PhysicallyBasedMaterial.EmissiveColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct)

##### Creating an emissive color object

- [init(color: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:)-3dtam)
- [init(color: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:)-5hl9i)
- [init(CustomMaterial.EmissiveColor)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(_:))

##### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/texturesemantic)

##### Initializers

- [init(color:texture:)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:))

##### Instance Properties

- [var color: UIColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/color-6l8ly)
- [var color: NSColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/color-9ktf)
- [PhysicallyBasedMaterial.Metallic](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct)

##### Creating a metallic object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Metallic)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(_:))

##### Accessing metallic data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/scale)
- [PhysicallyBasedMaterial.Normal](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct)

##### Creating a normal object

- [init(texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/init(texture:))
- [init(CustomMaterial.Normal)](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/init(_:))

##### Accessing the normal map

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/texturesemantic)
- [PhysicallyBasedMaterial.Opacity](/documentation/realitykit/physicallybasedmaterial/opacity)

##### Creating an opacity object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/opacity/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/opacity/init(scale:texture:))
- [init(CustomMaterial.Opacity)](/documentation/realitykit/physicallybasedmaterial/opacity/init(_:))

##### Accessing opacity values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/opacity/texture)
- [static var textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/opacity/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/opacity/scale)
- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [PhysicallyBasedMaterial.Roughness](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct)

##### Creating a roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Roughness)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(_:))

##### Accessing roughness data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/scale)
- [PhysicallyBasedMaterial.SheenColor](/documentation/realitykit/physicallybasedmaterial/sheencolor)

##### Creating a sheen color

- [init(tint: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:)-6kcl7)
- [init(tint: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:)-12ev9)

##### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/sheencolor/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/sheencolor/texturesemantic)

##### Initializers

- [init(tint:texture:)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:))

##### Instance Properties

- [var tint: UIColor](/documentation/realitykit/physicallybasedmaterial/sheencolor/tint-20njd)
- [var tint: NSColor](/documentation/realitykit/physicallybasedmaterial/sheencolor/tint-8az9f)
- [PhysicallyBasedMaterial.Specular](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct)

##### Creating a specular object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Specular)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(_:))

##### Accessing specular values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/scale)

#### Instance Properties

- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [var triangleFillMode: PhysicallyBasedMaterial.TriangleFillMode](/documentation/realitykit/physicallybasedmaterial/trianglefillmode-swift.property)

#### Type Aliases

- [PhysicallyBasedMaterial.FaceCulling](/documentation/realitykit/physicallybasedmaterial/faceculling-swift.typealias)
- [PhysicallyBasedMaterial.Texture](/documentation/realitykit/physicallybasedmaterial/texture)
- [PhysicallyBasedMaterial.TextureCoordinateTransform](/documentation/realitykit/physicallybasedmaterial/texturecoordinatetransform-swift.typealias)
- [PhysicallyBasedMaterial.TriangleFillMode](/documentation/realitykit/physicallybasedmaterial/trianglefillmode-swift.typealias)

#### Enumerations

- [PhysicallyBasedMaterial.Blending](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum)

##### Creating transparency objects

- [init(blending: CustomMaterial.Blending)](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/init(blending:))

##### Specifying opacity

- [case opaque](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/opaque)
- [case transparent(opacity: PhysicallyBasedMaterial.Opacity)](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/transparent(opacity:))
- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [PhysicallyBasedMaterial.Opacity](/documentation/realitykit/physicallybasedmaterial/opacity)

###### Creating an opacity object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/opacity/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/opacity/init(scale:texture:))
- [init(CustomMaterial.Opacity)](/documentation/realitykit/physicallybasedmaterial/opacity/init(_:))

###### Accessing opacity values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/opacity/texture)
- [static var textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/opacity/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/opacity/scale)
- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [PhysicallyBasedMaterial.BaseColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct)

#### Creating a base color object

- [init(tint: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:)-2wriz)
- [init(tint: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:)-5jeqr)
- [init(CustomMaterial.BaseColor)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(_:))

#### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/texturesemantic)

#### Initializers

- [init(tint:texture:)](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/init(tint:texture:))

#### Instance Properties

- [var tint: UIColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/tint-2znu0)
- [var tint: NSColor](/documentation/realitykit/physicallybasedmaterial/basecolor-swift.struct/tint-6heih)
- [PhysicallyBasedMaterial.Roughness](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct)

#### Creating a roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Roughness)](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/init(_:))

#### Accessing roughness data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/roughness-swift.struct/scale)
- [PhysicallyBasedMaterial.Metallic](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct)

#### Creating a metallic object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Metallic)](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/init(_:))

#### Accessing metallic data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/metallic-swift.struct/scale)
- [PhysicallyBasedMaterial.Normal](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct)

#### Creating a normal object

- [init(texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/init(texture:))
- [init(CustomMaterial.Normal)](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/init(_:))

#### Accessing the normal map

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/normal-swift.struct/texturesemantic)
- [PhysicallyBasedMaterial.Blending](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum)

#### Creating transparency objects

- [init(blending: CustomMaterial.Blending)](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/init(blending:))

#### Specifying opacity

- [case opaque](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/opaque)
- [case transparent(opacity: PhysicallyBasedMaterial.Opacity)](/documentation/realitykit/physicallybasedmaterial/blending-swift.enum/transparent(opacity:))
- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [PhysicallyBasedMaterial.Opacity](/documentation/realitykit/physicallybasedmaterial/opacity)

##### Creating an opacity object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/opacity/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/opacity/init(scale:texture:))
- [init(CustomMaterial.Opacity)](/documentation/realitykit/physicallybasedmaterial/opacity/init(_:))

##### Accessing opacity values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/opacity/texture)
- [static var textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/opacity/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/opacity/scale)
- [var opacityThreshold: Float?](/documentation/realitykit/physicallybasedmaterial/opacitythreshold)
- [PhysicallyBasedMaterial.AmbientOcclusion](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct)

#### Creating an ambient occlusion object

- [init(texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/init(texture:))
- [init(CustomMaterial.AmbientOcclusion)](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/init(_:))

#### Accessing ambient occlusion values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/ambientocclusion-swift.struct/texturesemantic)
- [PhysicallyBasedMaterial.Specular](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct)

#### Creating a specular object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Specular)](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/init(_:))

#### Accessing specular values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/specular-swift.struct/scale)
- [PhysicallyBasedMaterial.SheenColor](/documentation/realitykit/physicallybasedmaterial/sheencolor)

#### Creating a sheen color

- [init(tint: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:)-6kcl7)
- [init(tint: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:)-12ev9)

#### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/sheencolor/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/sheencolor/texturesemantic)

#### Initializers

- [init(tint:texture:)](/documentation/realitykit/physicallybasedmaterial/sheencolor/init(tint:texture:))

#### Instance Properties

- [var tint: UIColor](/documentation/realitykit/physicallybasedmaterial/sheencolor/tint-20njd)
- [var tint: NSColor](/documentation/realitykit/physicallybasedmaterial/sheencolor/tint-8az9f)
- [PhysicallyBasedMaterial.Clearcoat](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct)

#### Creating a clearcoat object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(scale:texture:))
- [init(CustomMaterial.Clearcoat)](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/init(_:))

#### Accessing clearcoat values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/clearcoat-swift.struct/scale)
- [PhysicallyBasedMaterial.ClearcoatRoughness](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct)

#### Creating a clearcoat roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(scale:texture:))
- [init(CustomMaterial.ClearcoatRoughness)](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/init(_:))

#### Accessing clearcoat roughness values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/clearcoatroughness-swift.struct/scale)
- [PhysicallyBasedMaterial.AnisotropyLevel](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct)

#### Creating an anisotropy level object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/init(scale:texture:))

#### Accessing anisotropy level values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/anisotropylevel-swift.struct/scale)
- [PhysicallyBasedMaterial.AnisotropyAngle](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct)

#### Creating an anisotropy angle object

- [init(floatLiteral: Float)](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: PhysicallyBasedMaterial.Texture?)](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/init(scale:texture:))

#### Accessing anisotropy angle values

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/texturesemantic)
- [var scale: Float](/documentation/realitykit/physicallybasedmaterial/anisotropyangle-swift.struct/scale)
- [PhysicallyBasedMaterial.EmissiveColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct)

#### Creating an emissive color object

- [init(color: UIColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:)-3dtam)
- [init(color: NSColor, texture: MaterialParameters.Texture?)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:)-5hl9i)
- [init(CustomMaterial.EmissiveColor)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(_:))

#### Accessing texture data

- [var texture: PhysicallyBasedMaterial.Texture?](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/texture)
- [static let textureSemantic: TextureResource.Semantic](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/texturesemantic)

#### Initializers

- [init(color:texture:)](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/init(color:texture:))

#### Instance Properties

- [var color: UIColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/color-6l8ly)
- [var color: NSColor](/documentation/realitykit/physicallybasedmaterial/emissivecolor-swift.struct/color-9ktf)
- [PhysicallyBasedMaterial.TextureCoordinateTransform](/documentation/realitykit/physicallybasedmaterial/texturecoordinatetransform-swift.typealias)
- [PhysicallyBasedMaterial.FaceCulling](/documentation/realitykit/physicallybasedmaterial/faceculling-swift.typealias)
- [PhysicallyBasedMaterial.Texture](/documentation/realitykit/physicallybasedmaterial/texture)

### Portals

- [PortalMaterial](/documentation/realitykit/portalmaterial)

#### Initializers

- [init()](/documentation/realitykit/portalmaterial/init())

#### Instance Properties

- [var faceCulling: PortalMaterial.FaceCulling](/documentation/realitykit/portalmaterial/faceculling-swift.property)
- [var triangleFillMode: PortalMaterial.TriangleFillMode](/documentation/realitykit/portalmaterial/trianglefillmode-swift.property)

#### Type Aliases

- [PortalMaterial.FaceCulling](/documentation/realitykit/portalmaterial/faceculling-swift.typealias)
- [PortalMaterial.TriangleFillMode](/documentation/realitykit/portalmaterial/trianglefillmode-swift.typealias)
- [PortalMaterial.FaceCulling](/documentation/realitykit/portalmaterial/faceculling-swift.typealias)
- [PortalMaterial.TriangleFillMode](/documentation/realitykit/portalmaterial/trianglefillmode-swift.typealias)
- [PortalComponent](/documentation/realitykit/portalcomponent)

#### Structures

- [PortalComponent.ClippingPlane](/documentation/realitykit/portalcomponent/clippingplane-swift.struct)

##### Initializers

- [init(position: SIMD3<Float>, normal: SIMD3<Float>)](/documentation/realitykit/portalcomponent/clippingplane-swift.struct/init(position:normal:))

##### Instance Properties

- [var normal: SIMD3<Float>](/documentation/realitykit/portalcomponent/clippingplane-swift.struct/normal)
- [var position: SIMD3<Float>](/documentation/realitykit/portalcomponent/clippingplane-swift.struct/position)
- [PortalComponent.Options](/documentation/realitykit/portalcomponent/options)

##### Type Properties

- [static let allowCrossing: PortalComponent.Options](/documentation/realitykit/portalcomponent/options/allowcrossing)
- [static let clipContents: PortalComponent.Options](/documentation/realitykit/portalcomponent/options/clipcontents)
- [PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane)

##### Initializers

- [init(position: SIMD3<Float>, normal: SIMD3<Float>)](/documentation/realitykit/portalcomponent/plane/init(position:normal:))

##### Instance Properties

- [var normal: SIMD3<Float>](/documentation/realitykit/portalcomponent/plane/normal)
- [var position: SIMD3<Float>](/documentation/realitykit/portalcomponent/plane/position)

##### Type Properties

- [static let negativeX: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/negativex)
- [static let negativeY: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/negativey)
- [static let negativeZ: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/negativez)
- [static let positiveX: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/positivex)
- [static let positiveY: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/positivey)
- [static let positiveZ: PortalComponent.Plane](/documentation/realitykit/portalcomponent/plane/positivez)

#### Initializers

- [init(target: Entity, clippingMode: PortalComponent.ClippingMode, crossingMode: PortalComponent.CrossingMode)](/documentation/realitykit/portalcomponent/init(target:clippingmode:crossingmode:))
- [init(target: Entity, clippingPlane: PortalComponent.ClippingPlane?)](/documentation/realitykit/portalcomponent/init(target:clippingplane:))
- [init(target: Entity, plane: PortalComponent.Plane, options: PortalComponent.Options)](/documentation/realitykit/portalcomponent/init(target:plane:options:))

#### Instance Properties

- [var clippingMode: PortalComponent.ClippingMode](/documentation/realitykit/portalcomponent/clippingmode-swift.property)
- [var clippingPlane: PortalComponent.ClippingPlane?](/documentation/realitykit/portalcomponent/clippingplane-swift.property)
- [var crossingMode: PortalComponent.CrossingMode](/documentation/realitykit/portalcomponent/crossingmode-swift.property)
- [var targetEntity: Entity?](/documentation/realitykit/portalcomponent/targetentity)

#### Enumerations

- [PortalComponent.ClippingMode](/documentation/realitykit/portalcomponent/clippingmode-swift.enum)

##### Enumeration Cases

- [case disabled](/documentation/realitykit/portalcomponent/clippingmode-swift.enum/disabled)
- [case plane(PortalComponent.Plane)](/documentation/realitykit/portalcomponent/clippingmode-swift.enum/plane(_:))
- [PortalComponent.CrossingMode](/documentation/realitykit/portalcomponent/crossingmode-swift.enum)

##### Enumeration Cases

- [case disabled](/documentation/realitykit/portalcomponent/crossingmode-swift.enum/disabled)
- [case plane(PortalComponent.Plane)](/documentation/realitykit/portalcomponent/crossingmode-swift.enum/plane(_:))
- [WorldComponent](/documentation/realitykit/worldcomponent)

#### Initializers

- [init()](/documentation/realitykit/worldcomponent/init())
- [PortalCrossingComponent](/documentation/realitykit/portalcrossingcomponent)

#### Initializers

- [init()](/documentation/realitykit/portalcrossingcomponent/init())

### Texture resources

- [TextureResource](/documentation/realitykit/textureresource)

#### Creating a texture resource

- [TextureResource.Contents](/documentation/realitykit/textureresource/contents)

##### Creating the content

- [init(mipmapLevels: [TextureResource.Contents.MipmapLevel])](/documentation/realitykit/textureresource/contents/init(mipmaplevels:))

##### Defining the content

- [TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel)

###### Creating a texture mipmap level

- [static func mip(data: Data, bytesPerRow: Int) -> TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel/mip(data:bytesperrow:))
- [static func mip(data: Data, bytesPerRow: Int, bytesPerImage: Int) -> TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel/mip(data:bytesperrow:bytesperimage:))
- [static func mip(slices: [TextureResource.Contents.Slice]) -> TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel/mip(slices:))
- [static func mip(unsafeBuffer: any MTLBuffer, offset: Int, size: Int, bytesPerRow: Int) -> TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel/mip(unsafebuffer:offset:size:bytesperrow:))
- [static func mip(unsafeBuffer: any MTLBuffer, offset: Int, size: Int, bytesPerRow: Int, bytesPerImage: Int) -> TextureResource.Contents.MipmapLevel](/documentation/realitykit/textureresource/contents/mipmaplevel/mip(unsafebuffer:offset:size:bytesperrow:bytesperimage:))
- [TextureResource.Contents.Slice](/documentation/realitykit/textureresource/contents/slice)

###### Creating a texture slice

- [static func slice(data: Data, bytesPerRow: Int) -> TextureResource.Contents.Slice](/documentation/realitykit/textureresource/contents/slice/slice(data:bytesperrow:))
- [static func slice(unsafeBuffer: any MTLBuffer, offset: Int, size: Int, bytesPerRow: Int) -> TextureResource.Contents.Slice](/documentation/realitykit/textureresource/contents/slice/slice(unsafebuffer:offset:size:bytesperrow:))
- [TextureResource.Format](/documentation/realitykit/textureresource/format)

##### Creating the format

- [static func color(TextureResource.Format.ColorSpace, pixelFormat: MTLPixelFormat) -> TextureResource.Format](/documentation/realitykit/textureresource/format/color(_:pixelformat:))
- [static func normal(TextureResource.Format.NormalEncoding, pixelFormat: MTLPixelFormat) -> TextureResource.Format](/documentation/realitykit/textureresource/format/normal(_:pixelformat:))
- [static func raw(pixelFormat: MTLPixelFormat) -> TextureResource.Format](/documentation/realitykit/textureresource/format/raw(pixelformat:))

##### Defining the format profile

- [TextureResource.Format.ColorSpace](/documentation/realitykit/textureresource/format/colorspace)

###### Format color spaces

- [case displayP3](/documentation/realitykit/textureresource/format/colorspace/displayp3)
- [TextureResource.Format.NormalEncoding](/documentation/realitykit/textureresource/format/normalencoding)

###### Normal profiles

- [case wy](/documentation/realitykit/textureresource/format/normalencoding/wy)
- [case xy](/documentation/realitykit/textureresource/format/normalencoding/xy)
- [TextureResource.Compression](/documentation/realitykit/textureresource/compression)

##### Specifying the compression settings

- [static var `default`: TextureResource.Compression](/documentation/realitykit/textureresource/compression/default)
- [static var none: TextureResource.Compression](/documentation/realitykit/textureresource/compression/none)
- [static func astc(blockSize: TextureResource.Compression.ASTCBlockSize, quality: TextureResource.Compression.ASTCQuality) -> TextureResource.Compression](/documentation/realitykit/textureresource/compression/astc(blocksize:quality:))
- [TextureResource.Compression.ASTCBlockSize](/documentation/realitykit/textureresource/compression/astcblocksize)

###### Compression block sizes

- [case block4x4](/documentation/realitykit/textureresource/compression/astcblocksize/block4x4)
- [case block5x4](/documentation/realitykit/textureresource/compression/astcblocksize/block5x4)
- [case block5x5](/documentation/realitykit/textureresource/compression/astcblocksize/block5x5)
- [case block6x5](/documentation/realitykit/textureresource/compression/astcblocksize/block6x5)
- [case block6x6](/documentation/realitykit/textureresource/compression/astcblocksize/block6x6)
- [case block8x5](/documentation/realitykit/textureresource/compression/astcblocksize/block8x5)
- [case block8x6](/documentation/realitykit/textureresource/compression/astcblocksize/block8x6)
- [case block8x8](/documentation/realitykit/textureresource/compression/astcblocksize/block8x8)
- [case block10x10](/documentation/realitykit/textureresource/compression/astcblocksize/block10x10)
- [case block10x5](/documentation/realitykit/textureresource/compression/astcblocksize/block10x5)
- [case block10x6](/documentation/realitykit/textureresource/compression/astcblocksize/block10x6)
- [case block10x8](/documentation/realitykit/textureresource/compression/astcblocksize/block10x8)
- [case block12x10](/documentation/realitykit/textureresource/compression/astcblocksize/block12x10)
- [case block12x12](/documentation/realitykit/textureresource/compression/astcblocksize/block12x12)
- [TextureResource.Compression.ASTCQuality](/documentation/realitykit/textureresource/compression/astcquality)

###### Compression qualities

- [case exhaustive](/documentation/realitykit/textureresource/compression/astcquality/exhaustive)
- [case fast](/documentation/realitykit/textureresource/compression/astcquality/fast)
- [case high](/documentation/realitykit/textureresource/compression/astcquality/high)
- [case normal](/documentation/realitykit/textureresource/compression/astcquality/normal)

#### Creating a 2D texture resource

- [TextureResource.Dimensions2D](/documentation/realitykit/textureresource/dimensions2d)

##### Creating the 2D dimensions

- [static func dimensions(width: Int, height: Int) -> TextureResource.Dimensions2D](/documentation/realitykit/textureresource/dimensions2d/dimensions(width:height:))

#### Creating a cube texture resource

- [TextureResource.DimensionsCube](/documentation/realitykit/textureresource/dimensionscube)

##### Creating the cube dimensions

- [static func dimensions(faceSize: Int) -> TextureResource.DimensionsCube](/documentation/realitykit/textureresource/dimensionscube/dimensions(facesize:))

#### Creating a 2D array texture resource

- [TextureResource.Dimensions2DArray](/documentation/realitykit/textureresource/dimensions2darray)

##### Creating the 2D array dimensions

- [static func dimensions(width: Int, height: Int, length: Int) -> TextureResource.Dimensions2DArray](/documentation/realitykit/textureresource/dimensions2darray/dimensions(width:height:length:))

#### Creating a 3D texture resource

- [TextureResource.Dimensions3D](/documentation/realitykit/textureresource/dimensions3d)

##### Creating the 3D dimensions

- [static func dimensions(width: Int, height: Int, depth: Int) -> TextureResource.Dimensions3D](/documentation/realitykit/textureresource/dimensions3d/dimensions(width:height:depth:))

#### Loading a texture

- [convenience init(named: String, in: Bundle?) async throws](/documentation/realitykit/textureresource/init(named:in:))
- [convenience init(named: String, in: Bundle?, options: TextureResource.CreateOptions) async throws](/documentation/realitykit/textureresource/init(named:in:options:))
- [convenience init(contentsOf: URL, withName: String?, options: TextureResource.CreateOptions) async throws](/documentation/realitykit/textureresource/init(contentsof:withname:options:))
- [convenience init(contentsOf: URL, withName: String?) async throws](/documentation/realitykit/textureresource/init(contentsof:withname:))
- [static func load(named: String, in: Bundle?) throws -> TextureResource](/documentation/realitykit/textureresource/load(named:in:))
- [static func load(named: String, in: Bundle?, options: TextureResource.CreateOptions) throws -> TextureResource](/documentation/realitykit/textureresource/load(named:in:options:))
- [static func load(contentsOf: URL, withName: String?, options: TextureResource.CreateOptions) throws -> TextureResource](/documentation/realitykit/textureresource/load(contentsof:withname:options:))
- [static func load(contentsOf: URL, withName: String?) throws -> TextureResource](/documentation/realitykit/textureresource/load(contentsof:withname:))
- [static func loadAsync(named: String, in: Bundle?) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/loadasync(named:in:))
- [static func loadAsync(named: String, in: Bundle?, options: TextureResource.CreateOptions) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/loadasync(named:in:options:))
- [static func loadAsync(contentsOf: URL, withName: String?) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/loadasync(contentsof:withname:))

#### Describing the texture

- [var textureType: MTLTextureType](/documentation/realitykit/textureresource/texturetype)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/pixelformat)
- [var height: Int](/documentation/realitykit/textureresource/height)
- [var width: Int](/documentation/realitykit/textureresource/width)
- [var depth: Int](/documentation/realitykit/textureresource/depth)
- [var arrayLength: Int](/documentation/realitykit/textureresource/arraylength)
- [var mipmapLevelCount: Int](/documentation/realitykit/textureresource/mipmaplevelcount)
- [var semantic: TextureResource.Semantic?](/documentation/realitykit/textureresource/semantic-swift.property)

#### Drawing the texture

- [var drawableQueue: TextureResource.DrawableQueue?](/documentation/realitykit/textureresource/drawablequeue-swift.property)

#### Copying the texture

- [func copy(to: any MTLTexture) throws](/documentation/realitykit/textureresource/copy(to:)-jfbi)
- [func copyAsync(to: any MTLTexture, completionHandler: ((any Error)?) -> Void)](/documentation/realitykit/textureresource/copyasync(to:completionhandler:))

#### Modifying the texture

- [func replace(withDrawables: TextureResource.DrawableQueue)](/documentation/realitykit/textureresource/replace(withdrawables:))
- [func replace(withImage: CGImage, options: TextureResource.CreateOptions) throws](/documentation/realitykit/textureresource/replace(withimage:options:))
- [func replace(using: CGImage, options: TextureResource.CreateOptions) async throws](/documentation/realitykit/textureresource/replace(using:options:))
- [func replace(with: LowLevelTexture)](/documentation/realitykit/textureresource/replace(with:))

#### Deprecated

- [static func generate(from: CGImage, withName: String?, options: TextureResource.CreateOptions) throws -> TextureResource](/documentation/realitykit/textureresource/generate(from:withname:options:))
- [static func generateAsync(from: CGImage, withName: String?, options: TextureResource.CreateOptions) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/generateasync(from:withname:options:))
- [func replaceAsync(withImage: CGImage, options: TextureResource.CreateOptions) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/replaceasync(withimage:options:))
- [static func generate(from: CGImage, named: String?, options: TextureResource.CreateOptions) async throws -> TextureResource](/documentation/realitykit/textureresource/generate(from:named:options:))
- [static func loadAsync(contentsOf: URL, withName: String?, options: TextureResource.CreateOptions) -> LoadRequest<TextureResource>](/documentation/realitykit/textureresource/loadasync(contentsof:withname:options:))

#### Classes

- [TextureResource.Drawable](/documentation/realitykit/textureresource/drawable)

##### Working with a drawable

- [var drawableQueue: TextureResource.DrawableQueue](/documentation/realitykit/textureresource/drawable/drawablequeue)
- [var texture: any MTLTexture](/documentation/realitykit/textureresource/drawable/texture)
- [func present()](/documentation/realitykit/textureresource/drawable/present())

##### Instance Methods

- [func presentOnSceneUpdate()](/documentation/realitykit/textureresource/drawable/presentonsceneupdate())
- [TextureResource.DrawableQueue](/documentation/realitykit/textureresource/drawablequeue-swift.class)

##### Creating a queue

- [init(TextureResource.DrawableQueue.Descriptor) throws](/documentation/realitykit/textureresource/drawablequeue-swift.class/init(_:))

##### Working with queues

- [var allowsNextDrawableTimeout: Bool](/documentation/realitykit/textureresource/drawablequeue-swift.class/allowsnextdrawabletimeout)
- [var height: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/height)
- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/drawablequeue-swift.class/mipmapsmode)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/drawablequeue-swift.class/pixelformat)
- [var usage: MTLTextureUsage](/documentation/realitykit/textureresource/drawablequeue-swift.class/usage)
- [var width: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/width)
- [func nextDrawable() throws -> TextureResource.Drawable](/documentation/realitykit/textureresource/drawablequeue-swift.class/nextdrawable())

##### Structures

- [TextureResource.DrawableQueue.Descriptor](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor)

###### Initializers

- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:))
- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode, timeout: Duration)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:timeout:))

###### Instance Properties

- [var height: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/height)
- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/mipmapsmode)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/pixelformat)
- [var timeout: Duration](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/timeout)
- [var usage: MTLTextureUsage](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/usage)
- [var width: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/width)

#### Structures

- [TextureResource.CreateOptions](/documentation/realitykit/textureresource/createoptions)

##### Texture resource initializers

- [init(semantic: TextureResource.Semantic?, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/createoptions/init(semantic:mipmapsmode:))

##### Texture resource creation options

- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/createoptions/mipmapsmode)
- [var semantic: TextureResource.Semantic?](/documentation/realitykit/textureresource/createoptions/semantic)

##### Initializers

- [init(semantic: TextureResource.Semantic?, compression: TextureResource.Compression, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/createoptions/init(semantic:compression:mipmapsmode:))

##### Instance Properties

- [var compression: TextureResource.Compression](/documentation/realitykit/textureresource/createoptions/compression)

#### Initializers

- [convenience(cubeFromEquirectangular:named:quality:faceSize:options:)](/documentation/realitykit/textureresource/init(cubefromequirectangular:named:quality:facesize:options:))
- [convenience(cubeFromImage:named:options:)](/documentation/realitykit/textureresource/init(cubefromimage:named:options:))
- [convenience(dimensions:format:contents:)](/documentation/realitykit/textureresource/init(dimensions:format:contents:))
- [convenience(from:)](/documentation/realitykit/textureresource/init(from:))
- [convenience(image:withName:options:)](/documentation/realitykit/textureresource/init(image:withname:options:))

#### Instance Methods

- [func copy(to:)](/documentation/realitykit/textureresource/copy(to:))

#### Type Aliases

- [TextureResource.SamplingQuality](/documentation/realitykit/textureresource/samplingquality)

#### Type Methods

- [static cube(slices:named:options:)](/documentation/realitykit/textureresource/cube(slices:named:options:))
- [static texture2DArray(slices:named:options:)](/documentation/realitykit/textureresource/texture2darray(slices:named:options:))
- [static texture3D(slices:named:options:)](/documentation/realitykit/textureresource/texture3d(slices:named:options:))

#### Enumerations

- [TextureResource.MipmapsMode](/documentation/realitykit/textureresource/mipmapsmode)

##### Specifying allocation and generation

- [case none](/documentation/realitykit/textureresource/mipmapsmode/none)
- [case allocateAll](/documentation/realitykit/textureresource/mipmapsmode/allocateall)
- [case allocateAndGenerateAll](/documentation/realitykit/textureresource/mipmapsmode/allocateandgenerateall)
- [TextureResource.Semantic](/documentation/realitykit/textureresource/semantic-swift.enum)

##### Specifying intended use

- [case raw](/documentation/realitykit/textureresource/semantic-swift.enum/raw)
- [case color](/documentation/realitykit/textureresource/semantic-swift.enum/color)
- [case hdrColor](/documentation/realitykit/textureresource/semantic-swift.enum/hdrcolor)
- [case normal](/documentation/realitykit/textureresource/semantic-swift.enum/normal)
- [case scalar](/documentation/realitykit/textureresource/semantic-swift.enum/scalar)

#### Default Implementations

- [Equatable Implementations](/documentation/realitykit/textureresource/equatable-implementations)

##### Operators

- [static func == (TextureResource, TextureResource) -> Bool](/documentation/realitykit/textureresource/==(_:_:))
- [TextureResource.CreateOptions](/documentation/realitykit/textureresource/createoptions)

#### Texture resource initializers

- [init(semantic: TextureResource.Semantic?, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/createoptions/init(semantic:mipmapsmode:))

#### Texture resource creation options

- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/createoptions/mipmapsmode)
- [var semantic: TextureResource.Semantic?](/documentation/realitykit/textureresource/createoptions/semantic)

#### Initializers

- [init(semantic: TextureResource.Semantic?, compression: TextureResource.Compression, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/createoptions/init(semantic:compression:mipmapsmode:))

#### Instance Properties

- [var compression: TextureResource.Compression](/documentation/realitykit/textureresource/createoptions/compression)
- [TextureResource.SamplingQuality](/documentation/realitykit/textureresource/samplingquality)
- [TextureResource.MipmapsMode](/documentation/realitykit/textureresource/mipmapsmode)

#### Specifying allocation and generation

- [case none](/documentation/realitykit/textureresource/mipmapsmode/none)
- [case allocateAll](/documentation/realitykit/textureresource/mipmapsmode/allocateall)
- [case allocateAndGenerateAll](/documentation/realitykit/textureresource/mipmapsmode/allocateandgenerateall)
- [TextureResource.Semantic](/documentation/realitykit/textureresource/semantic-swift.enum)

#### Specifying intended use

- [case raw](/documentation/realitykit/textureresource/semantic-swift.enum/raw)
- [case color](/documentation/realitykit/textureresource/semantic-swift.enum/color)
- [case hdrColor](/documentation/realitykit/textureresource/semantic-swift.enum/hdrcolor)
- [case normal](/documentation/realitykit/textureresource/semantic-swift.enum/normal)
- [case scalar](/documentation/realitykit/textureresource/semantic-swift.enum/scalar)

### Texture drawing

- [Rendering a windowed game in stereo](/documentation/realitykit/rendering-a-windowed-game-in-stereo)
- [Creating a dynamic height and normal map with low-level texture](/documentation/realitykit/creating-a-dynamic-height-map-with-low-level-texture)
- [LowLevelTexture](/documentation/realitykit/lowleveltexture)

#### Structures

- [LowLevelTexture.Descriptor](/documentation/realitykit/lowleveltexture/descriptor-swift.struct)

##### Initializers

- [init(textureType: MTLTextureType, pixelFormat: MTLPixelFormat, width: Int, height: Int, depth: Int, mipmapLevelCount: Int, arrayLength: Int, textureUsage: MTLTextureUsage, swizzle: MTLTextureSwizzleChannels)](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/init(texturetype:pixelformat:width:height:depth:mipmaplevelcount:arraylength:textureusage:swizzle:))

##### Instance Properties

- [var arrayLength: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/arraylength)
- [var depth: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/depth)
- [var height: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/height)
- [var mipmapLevelCount: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/mipmaplevelcount)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/pixelformat)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/swizzle)
- [var textureType: MTLTextureType](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/texturetype)
- [var textureUsage: MTLTextureUsage](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/textureusage)
- [var width: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/width)

#### Initializers

- [init(descriptor: LowLevelTexture.Descriptor) throws](/documentation/realitykit/lowleveltexture/init(descriptor:))

#### Instance Properties

- [let descriptor: LowLevelTexture.Descriptor](/documentation/realitykit/lowleveltexture/descriptor-swift.property)

#### Instance Methods

- [func read() -> any MTLTexture](/documentation/realitykit/lowleveltexture/read())
- [func replace(using: any MTLCommandBuffer) -> any MTLTexture](/documentation/realitykit/lowleveltexture/replace(using:))
- [LowLevelTexture.Descriptor](/documentation/realitykit/lowleveltexture/descriptor-swift.struct)

#### Initializers

- [init(textureType: MTLTextureType, pixelFormat: MTLPixelFormat, width: Int, height: Int, depth: Int, mipmapLevelCount: Int, arrayLength: Int, textureUsage: MTLTextureUsage, swizzle: MTLTextureSwizzleChannels)](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/init(texturetype:pixelformat:width:height:depth:mipmaplevelcount:arraylength:textureusage:swizzle:))

#### Instance Properties

- [var arrayLength: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/arraylength)
- [var depth: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/depth)
- [var height: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/height)
- [var mipmapLevelCount: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/mipmaplevelcount)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/pixelformat)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/swizzle)
- [var textureType: MTLTextureType](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/texturetype)
- [var textureUsage: MTLTextureUsage](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/textureusage)
- [var width: Int](/documentation/realitykit/lowleveltexture/descriptor-swift.struct/width)
- [TextureResource.Drawable](/documentation/realitykit/textureresource/drawable)

#### Working with a drawable

- [var drawableQueue: TextureResource.DrawableQueue](/documentation/realitykit/textureresource/drawable/drawablequeue)
- [var texture: any MTLTexture](/documentation/realitykit/textureresource/drawable/texture)
- [func present()](/documentation/realitykit/textureresource/drawable/present())

#### Instance Methods

- [func presentOnSceneUpdate()](/documentation/realitykit/textureresource/drawable/presentonsceneupdate())
- [TextureResource.DrawableQueue](/documentation/realitykit/textureresource/drawablequeue-swift.class)

#### Creating a queue

- [init(TextureResource.DrawableQueue.Descriptor) throws](/documentation/realitykit/textureresource/drawablequeue-swift.class/init(_:))

#### Working with queues

- [var allowsNextDrawableTimeout: Bool](/documentation/realitykit/textureresource/drawablequeue-swift.class/allowsnextdrawabletimeout)
- [var height: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/height)
- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/drawablequeue-swift.class/mipmapsmode)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/drawablequeue-swift.class/pixelformat)
- [var usage: MTLTextureUsage](/documentation/realitykit/textureresource/drawablequeue-swift.class/usage)
- [var width: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/width)
- [func nextDrawable() throws -> TextureResource.Drawable](/documentation/realitykit/textureresource/drawablequeue-swift.class/nextdrawable())

#### Structures

- [TextureResource.DrawableQueue.Descriptor](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor)

##### Initializers

- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:))
- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode, timeout: Duration)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:timeout:))

##### Instance Properties

- [var height: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/height)
- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/mipmapsmode)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/pixelformat)
- [var timeout: Duration](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/timeout)
- [var usage: MTLTextureUsage](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/usage)
- [var width: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/width)
- [TextureResource.DrawableQueue.Descriptor](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor)

#### Initializers

- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:))
- [init(pixelFormat: MTLPixelFormat, width: Int, height: Int, usage: MTLTextureUsage, mipmapsMode: TextureResource.MipmapsMode, timeout: Duration)](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/init(pixelformat:width:height:usage:mipmapsmode:timeout:))

#### Instance Properties

- [var height: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/height)
- [var mipmapsMode: TextureResource.MipmapsMode](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/mipmapsmode)
- [var pixelFormat: MTLPixelFormat](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/pixelformat)
- [var timeout: Duration](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/timeout)
- [var usage: MTLTextureUsage](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/usage)
- [var width: Int](/documentation/realitykit/textureresource/drawablequeue-swift.class/descriptor/width)

### Shaders

- [ShaderGraphMaterial](/documentation/realitykit/shadergraphmaterial)

#### Shader Graph fundamentals

- [Reality Composer Pro](/documentation/realitycomposerpro)
- [Material](/documentation/realitykit/material)

##### Identifying a material

- [var name: String?](/documentation/realitykit/material/name)

##### Type Aliases

- [Material.Color](/documentation/realitykit/material/color)
- [Material.Parameters](/documentation/realitykit/material/parameters)
- [MaterialParameterTypes](/documentation/realitykit/materialparametertypes)

##### Structures

- [MaterialParameterTypes.TextureCoordinateTransform](/documentation/realitykit/materialparametertypes/texturecoordinatetransform)

###### Creating a texture coordinate transform

- [init(offset: SIMD2<Float>, scale: SIMD2<Float>, rotation: Float)](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/init(offset:scale:rotation:))

###### Accessing the transform values

- [var offset: SIMD2<Float>](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/offset)
- [var scale: SIMD2<Float>](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/scale)
- [var rotation: Float](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/rotation)

##### Enumerations

- [MaterialParameterTypes.BlendMode](/documentation/realitykit/materialparametertypes/blendmode)

###### Enumeration Cases

- [case add](/documentation/realitykit/materialparametertypes/blendmode/add)
- [case alpha](/documentation/realitykit/materialparametertypes/blendmode/alpha)
- [MaterialParameterTypes.FaceCulling](/documentation/realitykit/materialparametertypes/faceculling)

###### Face culling

- [case front](/documentation/realitykit/materialparametertypes/faceculling/front)
- [case back](/documentation/realitykit/materialparametertypes/faceculling/back)
- [case none](/documentation/realitykit/materialparametertypes/faceculling/none)
- [MaterialParameterTypes.TriangleFillMode](/documentation/realitykit/materialparametertypes/trianglefillmode)

###### Enumeration Cases

- [case fill](/documentation/realitykit/materialparametertypes/trianglefillmode/fill)
- [case lines](/documentation/realitykit/materialparametertypes/trianglefillmode/lines)

#### Initializers

- [init(materialXLabel: String, data: Data) async throws](/documentation/realitykit/shadergraphmaterial/init(materialxlabel:data:))
- [init(named:from:)](/documentation/realitykit/shadergraphmaterial/init(named:from:))
- [init(named: String, from: String, in: Bundle?) async throws](/documentation/realitykit/shadergraphmaterial/init(named:from:in:))

#### Instance Properties

- [var faceCulling: ShaderGraphMaterial.FaceCulling](/documentation/realitykit/shadergraphmaterial/faceculling-swift.property)
- [var parameterNames: [String]](/documentation/realitykit/shadergraphmaterial/parameternames)
- [var readsDepth: Bool](/documentation/realitykit/shadergraphmaterial/readsdepth)
- [var triangleFillMode: ShaderGraphMaterial.TriangleFillMode](/documentation/realitykit/shadergraphmaterial/trianglefillmode-swift.property)
- [var writesDepth: Bool](/documentation/realitykit/shadergraphmaterial/writesdepth)

#### Instance Methods

- [func getParameter(handle: MaterialParameters.Handle) -> MaterialParameters.Value?](/documentation/realitykit/shadergraphmaterial/getparameter(handle:))
- [func getParameter(name: String) -> MaterialParameters.Value?](/documentation/realitykit/shadergraphmaterial/getparameter(name:))
- [func setParameter(handle: MaterialParameters.Handle, value: MaterialParameters.Value) throws](/documentation/realitykit/shadergraphmaterial/setparameter(handle:value:))
- [func setParameter(name: String, value: MaterialParameters.Value) throws](/documentation/realitykit/shadergraphmaterial/setparameter(name:value:))

#### Type Aliases

- [ShaderGraphMaterial.FaceCulling](/documentation/realitykit/shadergraphmaterial/faceculling-swift.typealias)
- [ShaderGraphMaterial.TriangleFillMode](/documentation/realitykit/shadergraphmaterial/trianglefillmode-swift.typealias)

#### Type Methods

- [static func parameterHandle(name: String) -> MaterialParameters.Handle](/documentation/realitykit/shadergraphmaterial/parameterhandle(name:))

#### Enumerations

- [ShaderGraphMaterial.Error](/documentation/realitykit/shadergraphmaterial/error)

##### Enumeration Cases

- [case incorrectTypeForParameterName](/documentation/realitykit/shadergraphmaterial/error/incorrecttypeforparametername)
- [case parameterNameNotFound](/documentation/realitykit/shadergraphmaterial/error/parameternamenotfound)
- [ShaderGraphMaterial.LoadError](/documentation/realitykit/shadergraphmaterial/loaderror)

##### Enumeration Cases

- [case invalidTypeFound](/documentation/realitykit/shadergraphmaterial/loaderror/invalidtypefound)
- [case invalidURL](/documentation/realitykit/shadergraphmaterial/loaderror/invalidurl)
- [case materialNameNotFound](/documentation/realitykit/shadergraphmaterial/loaderror/materialnamenotfound)
- [case resourceShareFailed](/documentation/realitykit/shadergraphmaterial/loaderror/resourcesharefailed)
- [ShaderGraphMaterial.FaceCulling](/documentation/realitykit/shadergraphmaterial/faceculling-swift.typealias)
- [ShaderGraphMaterial.TriangleFillMode](/documentation/realitykit/shadergraphmaterial/trianglefillmode-swift.typealias)
- [Modifying RealityKit rendering using custom materials](/documentation/realitykit/modifying-realitykit-rendering-using-custom-materials)
- [CustomMaterial](/documentation/realitykit/custommaterial)

#### Creating custom materials

- [init(from: any Material, geometryModifier: CustomMaterial.GeometryModifier) throws](/documentation/realitykit/custommaterial/init(from:geometrymodifier:))
- [init(from: any Material, surfaceShader: CustomMaterial.SurfaceShader, geometryModifier: CustomMaterial.GeometryModifier?) throws](/documentation/realitykit/custommaterial/init(from:surfaceshader:geometrymodifier:))
- [init(surfaceShader: CustomMaterial.SurfaceShader, geometryModifier: CustomMaterial.GeometryModifier?, lightingModel: CustomMaterial.LightingModel) throws](/documentation/realitykit/custommaterial/init(surfaceshader:geometrymodifier:lightingmodel:))
- [init(program: CustomMaterial.Program)](/documentation/realitykit/custommaterial/init(program:))

#### Setting the core properties

- [var baseColor: CustomMaterial.BaseColor](/documentation/realitykit/custommaterial/basecolor-swift.property)
- [var roughness: CustomMaterial.Roughness](/documentation/realitykit/custommaterial/roughness-swift.property)
- [var metallic: CustomMaterial.Metallic](/documentation/realitykit/custommaterial/metallic-swift.property)
- [var normal: CustomMaterial.Normal](/documentation/realitykit/custommaterial/normal-swift.property)
- [var emissiveColor: CustomMaterial.EmissiveColor](/documentation/realitykit/custommaterial/emissivecolor-swift.property)
- [var ambientOcclusion: CustomMaterial.AmbientOcclusion](/documentation/realitykit/custommaterial/ambientocclusion-swift.property)
- [var specular: CustomMaterial.Specular](/documentation/realitykit/custommaterial/specular-swift.property)
- [var clearcoat: CustomMaterial.Clearcoat](/documentation/realitykit/custommaterial/clearcoat-swift.property)
- [var clearcoatRoughness: CustomMaterial.ClearcoatRoughness](/documentation/realitykit/custommaterial/clearcoatroughness-swift.property)
- [var clearcoatNormal: CustomMaterial.ClearcoatNormal](/documentation/realitykit/custommaterial/clearcoatnormal-swift.property)

#### Controlling opacity

- [var opacityThreshold: Float?](/documentation/realitykit/custommaterial/opacitythreshold)
- [var blending: CustomMaterial.Blending](/documentation/realitykit/custommaterial/blending-swift.property)

#### Setting shader properties

- [var program: CustomMaterial.Program](/documentation/realitykit/custommaterial/program-swift.property)
- [var custom: CustomMaterial.Custom](/documentation/realitykit/custommaterial/custom-swift.property)
- [var lightingModel: CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/lightingmodel-swift.property)
- [func withMutableUniforms<UniformsType>(ofType: UniformsType.Type, (inout UniformsType, inout CustomMaterial.ResourceStorage<UniformsType>) -> Void)](/documentation/realitykit/custommaterial/withmutableuniforms(oftype:_:))
- [func withMutableUniforms<UniformsType>(ofType: UniformsType.Type, stage: CustomShaderStage, (inout UniformsType, inout CustomMaterial.ResourceStorage<UniformsType>) -> Void)](/documentation/realitykit/custommaterial/withmutableuniforms(oftype:stage:_:))

#### Modifying texture coordinates

- [var textureCoordinateTransform: CustomMaterial.TextureCoordinateTransform](/documentation/realitykit/custommaterial/texturecoordinatetransform-swift.property)
- [var secondaryTextureCoordinateTransform: CustomMaterial.TextureCoordinateTransform](/documentation/realitykit/custommaterial/secondarytexturecoordinatetransform)

#### Culling unnecessary polygons

- [var faceCulling: CustomMaterial.FaceCulling](/documentation/realitykit/custommaterial/faceculling-swift.property)

#### Setting depth testing properties

- [var readsDepth: Bool](/documentation/realitykit/custommaterial/readsdepth)
- [var writesDepth: Bool](/documentation/realitykit/custommaterial/writesdepth)

#### Classes

- [CustomMaterial.Program](/documentation/realitykit/custommaterial/program-swift.class)

##### Structures

- [CustomMaterial.Program.Descriptor](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct)

###### Initializers

- [init()](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/init())

###### Instance Properties

- [var blendMode: MaterialParameterTypes.BlendMode?](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/blendmode)
- [var lightingModel: CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/lightingmodel)

##### Initializers

- [init(surfaceShader: CustomMaterial.SurfaceShader, geometryModifier: CustomMaterial.GeometryModifier?, descriptor: CustomMaterial.Program.Descriptor) async throws](/documentation/realitykit/custommaterial/program-swift.class/init(surfaceshader:geometrymodifier:descriptor:))

##### Instance Properties

- [let descriptor: CustomMaterial.Program.Descriptor](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.property)
- [let geometryModifier: CustomMaterial.GeometryModifier?](/documentation/realitykit/custommaterial/program-swift.class/geometrymodifier)
- [let surfaceShader: CustomMaterial.SurfaceShader](/documentation/realitykit/custommaterial/program-swift.class/surfaceshader)

#### Structures

- [CustomMaterial.AmbientOcclusion](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct)

##### Creating an ambient occlusion object

- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/init(texture:))
- [init(PhysicallyBasedMaterial.AmbientOcclusion)](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/init(_:))

##### Accessing ambient occlusion values

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/texture)
- [CustomMaterial.BaseColor](/documentation/realitykit/custommaterial/basecolor-swift.struct)

##### Creating a base color object

- [init(tint: UIColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:)-5c2fr)
- [init(tint: NSColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:)-71h0i)
- [init(PhysicallyBasedMaterial.BaseColor)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(_:))

##### Accessing base color data

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/basecolor-swift.struct/texture)
- [var tint: UIColor](/documentation/realitykit/custommaterial/basecolor-swift.struct/tint-4xg2a)
- [var tint: NSColor](/documentation/realitykit/custommaterial/basecolor-swift.struct/tint-99g)

##### Initializers

- [init(tint:texture:)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:))
- [CustomMaterial.Clearcoat](/documentation/realitykit/custommaterial/clearcoat-swift.struct)

##### Creating a clearcoat object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Clearcoat)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(_:))

##### Accessing clearcoat values

- [var scale: Float](/documentation/realitykit/custommaterial/clearcoat-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/clearcoat-swift.struct/texture)
- [CustomMaterial.ClearcoatNormal](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct)

##### Initializers

- [init(PhysicallyBasedMaterial.ClearcoatNormal)](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/init(_:))
- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/init(texture:))

##### Instance Properties

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/texture)
- [CustomMaterial.ClearcoatRoughness](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct)

##### Creating a clearcoat roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.ClearcoatRoughness)](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct/init(_:))

##### Accessing clearcoat roughness values

- [var scale: Float](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/clearcoatroughness-swift.struct/texture)
- [CustomMaterial.Custom](/documentation/realitykit/custommaterial/custom-swift.struct)

##### Creating a custom object

- [init(value: SIMD4<Float>, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/custom-swift.struct/init(value:texture:))

##### Accessing custom values

- [var value: SIMD4<Float>](/documentation/realitykit/custommaterial/custom-swift.struct/value)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/custom-swift.struct/texture)
- [CustomMaterial.CustomMaterialTexture](/documentation/realitykit/custommaterial/custommaterialtexture)

##### Creating a custom texture

- [init(TextureResource)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:)-1i8wq)
- [init(MaterialParameters.Texture)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:)-71hfh)

##### Accessing texture resources

- [var resource: TextureResource](/documentation/realitykit/custommaterial/custommaterialtexture/resource)

##### Initializers

- [init(_:)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:))
- [init(TextureResource, MTLTextureSwizzleChannels)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:_:))

##### Instance Properties

- [var swizzle: MTLTextureSwizzleChannels](/documentation/realitykit/custommaterial/custommaterialtexture/swizzle)
- [CustomMaterial.EmissiveColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct)

##### Creating an emissive color object

- [init(PhysicallyBasedMaterial.EmissiveColor)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(_:))
- [init(color: NSColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:)-xkh3)
- [init(color: UIColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:)-81kgh)

##### Accessing emissive color data

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/texture)
- [var color: UIColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/color-5hrho)
- [var color: NSColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/color-9scic)

##### Initializers

- [init(color:texture:)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:))
- [CustomMaterial.GeometryModifier](/documentation/realitykit/custommaterial/geometrymodifier)

##### Creating geometry modifier objects

- [init(named: String, in: any MTLLibrary)](/documentation/realitykit/custommaterial/geometrymodifier/init(named:in:))

##### Accessing geometry modifier properties

- [var name: String](/documentation/realitykit/custommaterial/geometrymodifier/name)
- [var library: any MTLLibrary](/documentation/realitykit/custommaterial/geometrymodifier/library)

##### Initializers

- [init(named: String, in: any MTLLibrary, constantValues: MTLFunctionConstantValues)](/documentation/realitykit/custommaterial/geometrymodifier/init(named:in:constantvalues:))
- [CustomMaterial.Metallic](/documentation/realitykit/custommaterial/metallic-swift.struct)

##### Creating a metallic object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Metallic)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(_:))

##### Accessing metallic data

- [var scale: Float](/documentation/realitykit/custommaterial/metallic-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/metallic-swift.struct/texture)
- [CustomMaterial.Normal](/documentation/realitykit/custommaterial/normal-swift.struct)

##### Creating a normal object

- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/normal-swift.struct/init(texture:))
- [init(PhysicallyBasedMaterial.Normal)](/documentation/realitykit/custommaterial/normal-swift.struct/init(_:))

##### Accessing the normal map

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/normal-swift.struct/texture)
- [CustomMaterial.Opacity](/documentation/realitykit/custommaterial/opacity)

##### Creating an opacity object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/opacity/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/opacity/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Opacity)](/documentation/realitykit/custommaterial/opacity/init(_:))

##### Accessing opacity data

- [var scale: Float](/documentation/realitykit/custommaterial/opacity/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/opacity/texture)
- [CustomMaterial.ResourceStorage](/documentation/realitykit/custommaterial/resourcestorage)

##### Subscripts

- [subscript<BufferType>(buffer _: KeyPath<UniformsType, UnsafeMutablePointer<BufferType>?>) -> LowLevelBuffer?](/documentation/realitykit/custommaterial/resourcestorage/subscript(buffer:))
- [subscript(textureResource _: KeyPath<UniformsType, UInt64>) -> TextureResource](/documentation/realitykit/custommaterial/resourcestorage/subscript(textureresource:))
- [CustomMaterial.Roughness](/documentation/realitykit/custommaterial/roughness-swift.struct)

##### Creating a roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Roughness)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(_:))

##### Accessing roughness values

- [var scale: Float](/documentation/realitykit/custommaterial/roughness-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/roughness-swift.struct/texture)
- [CustomMaterial.Specular](/documentation/realitykit/custommaterial/specular-swift.struct)

##### Creating a specular object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/specular-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/specular-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Specular)](/documentation/realitykit/custommaterial/specular-swift.struct/init(_:))

##### Accessing specular values

- [var scale: Float](/documentation/realitykit/custommaterial/specular-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/specular-swift.struct/texture)
- [CustomMaterial.SurfaceShader](/documentation/realitykit/custommaterial/surfaceshader)

##### Creating surface shader objects

- [init(named: String, in: any MTLLibrary)](/documentation/realitykit/custommaterial/surfaceshader/init(named:in:))

##### Accessing surface shader properties

- [var name: String](/documentation/realitykit/custommaterial/surfaceshader/name)
- [var library: any MTLLibrary](/documentation/realitykit/custommaterial/surfaceshader/library)

##### Initializers

- [init(named: String, in: any MTLLibrary, constantValues: MTLFunctionConstantValues)](/documentation/realitykit/custommaterial/surfaceshader/init(named:in:constantvalues:))

#### Instance Properties

- [var triangleFillMode: CustomMaterial.TriangleFillMode](/documentation/realitykit/custommaterial/trianglefillmode-swift.property)

#### Type Aliases

- [CustomMaterial.FaceCulling](/documentation/realitykit/custommaterial/faceculling-swift.typealias)
- [CustomMaterial.Texture](/documentation/realitykit/custommaterial/texture)
- [CustomMaterial.TextureCoordinateTransform](/documentation/realitykit/custommaterial/texturecoordinatetransform-swift.typealias)
- [CustomMaterial.TriangleFillMode](/documentation/realitykit/custommaterial/trianglefillmode-swift.typealias)

#### Type Properties

- [static var supportsMutableUniformsResources: Bool](/documentation/realitykit/custommaterial/supportsmutableuniformsresources)

#### Enumerations

- [CustomMaterial.Blending](/documentation/realitykit/custommaterial/blending-swift.enum)

##### Creating a blending object

- [init(blending: PhysicallyBasedMaterial.Blending)](/documentation/realitykit/custommaterial/blending-swift.enum/init(blending:))

##### Specifying transparency

- [case opaque](/documentation/realitykit/custommaterial/blending-swift.enum/opaque)
- [case transparent(opacity: CustomMaterial.Opacity)](/documentation/realitykit/custommaterial/blending-swift.enum/transparent(opacity:))
- [CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/lightingmodel-swift.enum)

##### Specifying the lighting model

- [case lit](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/lit)
- [case clearcoat](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/clearcoat)
- [case unlit](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/unlit)
- [CustomMaterial.SurfaceShader](/documentation/realitykit/custommaterial/surfaceshader)

#### Creating surface shader objects

- [init(named: String, in: any MTLLibrary)](/documentation/realitykit/custommaterial/surfaceshader/init(named:in:))

#### Accessing surface shader properties

- [var name: String](/documentation/realitykit/custommaterial/surfaceshader/name)
- [var library: any MTLLibrary](/documentation/realitykit/custommaterial/surfaceshader/library)

#### Initializers

- [init(named: String, in: any MTLLibrary, constantValues: MTLFunctionConstantValues)](/documentation/realitykit/custommaterial/surfaceshader/init(named:in:constantvalues:))
- [CustomMaterial.GeometryModifier](/documentation/realitykit/custommaterial/geometrymodifier)

#### Creating geometry modifier objects

- [init(named: String, in: any MTLLibrary)](/documentation/realitykit/custommaterial/geometrymodifier/init(named:in:))

#### Accessing geometry modifier properties

- [var name: String](/documentation/realitykit/custommaterial/geometrymodifier/name)
- [var library: any MTLLibrary](/documentation/realitykit/custommaterial/geometrymodifier/library)

#### Initializers

- [init(named: String, in: any MTLLibrary, constantValues: MTLFunctionConstantValues)](/documentation/realitykit/custommaterial/geometrymodifier/init(named:in:constantvalues:))
- [MaterialFunction](/documentation/realitykit/materialfunction)

#### Instance Properties

- [var constantValues: MTLFunctionConstantValues](/documentation/realitykit/materialfunction/constantvalues)
- [var library: any MTLLibrary](/documentation/realitykit/materialfunction/library)
- [var name: String](/documentation/realitykit/materialfunction/name)
- [CustomMaterial.Program](/documentation/realitykit/custommaterial/program-swift.class)

#### Structures

- [CustomMaterial.Program.Descriptor](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct)

##### Initializers

- [init()](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/init())

##### Instance Properties

- [var blendMode: MaterialParameterTypes.BlendMode?](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/blendmode)
- [var lightingModel: CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/lightingmodel)

#### Initializers

- [init(surfaceShader: CustomMaterial.SurfaceShader, geometryModifier: CustomMaterial.GeometryModifier?, descriptor: CustomMaterial.Program.Descriptor) async throws](/documentation/realitykit/custommaterial/program-swift.class/init(surfaceshader:geometrymodifier:descriptor:))

#### Instance Properties

- [let descriptor: CustomMaterial.Program.Descriptor](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.property)
- [let geometryModifier: CustomMaterial.GeometryModifier?](/documentation/realitykit/custommaterial/program-swift.class/geometrymodifier)
- [let surfaceShader: CustomMaterial.SurfaceShader](/documentation/realitykit/custommaterial/program-swift.class/surfaceshader)
- [CustomMaterial.Program.Descriptor](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct)

#### Initializers

- [init()](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/init())

#### Instance Properties

- [var blendMode: MaterialParameterTypes.BlendMode?](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/blendmode)
- [var lightingModel: CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/program-swift.class/descriptor-swift.struct/lightingmodel)
- [CustomShaderStage](/documentation/realitykit/customshaderstage)

#### Enumeration Cases

- [case geometryModifier](/documentation/realitykit/customshaderstage/geometrymodifier)
- [case surfaceShader](/documentation/realitykit/customshaderstage/surfaceshader)

### Object occlusion

- [OcclusionMaterial](/documentation/realitykit/occlusionmaterial)

#### Creating an occlusion material

- [init(receivesDynamicLighting: Bool)](/documentation/realitykit/occlusionmaterial/init(receivesdynamiclighting:))
- [init()](/documentation/realitykit/occlusionmaterial/init())

#### Receiving dynamic lighting

- [let receivesDynamicLighting: Bool](/documentation/realitykit/occlusionmaterial/receivesdynamiclighting)

#### Setting depth testing properties

- [var readsDepth: Bool](/documentation/realitykit/occlusionmaterial/readsdepth)

#### Instance Properties

- [var faceCulling: OcclusionMaterial.FaceCulling](/documentation/realitykit/occlusionmaterial/faceculling-swift.property)

#### Type Aliases

- [OcclusionMaterial.FaceCulling](/documentation/realitykit/occlusionmaterial/faceculling-swift.typealias)
- [OcclusionMaterial.FaceCulling](/documentation/realitykit/occlusionmaterial/faceculling-swift.typealias)

### Video materials

- [VideoMaterial](/documentation/realitykit/videomaterial)

#### Creating a video material

- [init(avPlayer: AVPlayer)](/documentation/realitykit/videomaterial/init(avplayer:))

#### Controlling playback

- [var avPlayer: AVPlayer?](/documentation/realitykit/videomaterial/avplayer)
- [var controller: VideoPlaybackController](/documentation/realitykit/videomaterial/controller)

#### Initializers

- [init(videoRenderer: AVSampleBufferVideoRenderer)](/documentation/realitykit/videomaterial/init(videorenderer:))

#### Instance Properties

- [var faceCulling: VideoMaterial.FaceCulling](/documentation/realitykit/videomaterial/faceculling-swift.property)
- [var readsDepth: Bool](/documentation/realitykit/videomaterial/readsdepth)
- [var triangleFillMode: VideoMaterial.TriangleFillMode](/documentation/realitykit/videomaterial/trianglefillmode-swift.property)
- [var videoRenderer: AVSampleBufferVideoRenderer?](/documentation/realitykit/videomaterial/videorenderer)
- [var writesDepth: Bool](/documentation/realitykit/videomaterial/writesdepth)

#### Type Aliases

- [VideoMaterial.FaceCulling](/documentation/realitykit/videomaterial/faceculling-swift.typealias)
- [VideoMaterial.TriangleFillMode](/documentation/realitykit/videomaterial/trianglefillmode-swift.typealias)
- [VideoMaterial.FaceCulling](/documentation/realitykit/videomaterial/faceculling-swift.typealias)
- [VideoMaterial.TriangleFillMode](/documentation/realitykit/videomaterial/trianglefillmode-swift.typealias)

### Custom material types

- [CustomMaterial.Custom](/documentation/realitykit/custommaterial/custom-swift.struct)

#### Creating a custom object

- [init(value: SIMD4<Float>, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/custom-swift.struct/init(value:texture:))

#### Accessing custom values

- [var value: SIMD4<Float>](/documentation/realitykit/custommaterial/custom-swift.struct/value)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/custom-swift.struct/texture)
- [CustomMaterial.CustomMaterialTexture](/documentation/realitykit/custommaterial/custommaterialtexture)

#### Creating a custom texture

- [init(TextureResource)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:)-1i8wq)
- [init(MaterialParameters.Texture)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:)-71hfh)

#### Accessing texture resources

- [var resource: TextureResource](/documentation/realitykit/custommaterial/custommaterialtexture/resource)

#### Initializers

- [init(_:)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:))
- [init(TextureResource, MTLTextureSwizzleChannels)](/documentation/realitykit/custommaterial/custommaterialtexture/init(_:_:))

#### Instance Properties

- [var swizzle: MTLTextureSwizzleChannels](/documentation/realitykit/custommaterial/custommaterialtexture/swizzle)
- [CustomMaterial.LightingModel](/documentation/realitykit/custommaterial/lightingmodel-swift.enum)

#### Specifying the lighting model

- [case lit](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/lit)
- [case clearcoat](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/clearcoat)
- [case unlit](/documentation/realitykit/custommaterial/lightingmodel-swift.enum/unlit)
- [CustomMaterial.BaseColor](/documentation/realitykit/custommaterial/basecolor-swift.struct)

#### Creating a base color object

- [init(tint: UIColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:)-5c2fr)
- [init(tint: NSColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:)-71h0i)
- [init(PhysicallyBasedMaterial.BaseColor)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(_:))

#### Accessing base color data

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/basecolor-swift.struct/texture)
- [var tint: UIColor](/documentation/realitykit/custommaterial/basecolor-swift.struct/tint-4xg2a)
- [var tint: NSColor](/documentation/realitykit/custommaterial/basecolor-swift.struct/tint-99g)

#### Initializers

- [init(tint:texture:)](/documentation/realitykit/custommaterial/basecolor-swift.struct/init(tint:texture:))
- [CustomMaterial.Roughness](/documentation/realitykit/custommaterial/roughness-swift.struct)

#### Creating a roughness object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Roughness)](/documentation/realitykit/custommaterial/roughness-swift.struct/init(_:))

#### Accessing roughness values

- [var scale: Float](/documentation/realitykit/custommaterial/roughness-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/roughness-swift.struct/texture)
- [CustomMaterial.Metallic](/documentation/realitykit/custommaterial/metallic-swift.struct)

#### Creating a metallic object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Metallic)](/documentation/realitykit/custommaterial/metallic-swift.struct/init(_:))

#### Accessing metallic data

- [var scale: Float](/documentation/realitykit/custommaterial/metallic-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/metallic-swift.struct/texture)
- [CustomMaterial.Normal](/documentation/realitykit/custommaterial/normal-swift.struct)

#### Creating a normal object

- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/normal-swift.struct/init(texture:))
- [init(PhysicallyBasedMaterial.Normal)](/documentation/realitykit/custommaterial/normal-swift.struct/init(_:))

#### Accessing the normal map

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/normal-swift.struct/texture)
- [CustomMaterial.EmissiveColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct)

#### Creating an emissive color object

- [init(PhysicallyBasedMaterial.EmissiveColor)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(_:))
- [init(color: NSColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:)-xkh3)
- [init(color: UIColor, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:)-81kgh)

#### Accessing emissive color data

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/texture)
- [var color: UIColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/color-5hrho)
- [var color: NSColor](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/color-9scic)

#### Initializers

- [init(color:texture:)](/documentation/realitykit/custommaterial/emissivecolor-swift.struct/init(color:texture:))
- [CustomMaterial.Blending](/documentation/realitykit/custommaterial/blending-swift.enum)

#### Creating a blending object

- [init(blending: PhysicallyBasedMaterial.Blending)](/documentation/realitykit/custommaterial/blending-swift.enum/init(blending:))

#### Specifying transparency

- [case opaque](/documentation/realitykit/custommaterial/blending-swift.enum/opaque)
- [case transparent(opacity: CustomMaterial.Opacity)](/documentation/realitykit/custommaterial/blending-swift.enum/transparent(opacity:))
- [CustomMaterial.Opacity](/documentation/realitykit/custommaterial/opacity)

#### Creating an opacity object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/opacity/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/opacity/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Opacity)](/documentation/realitykit/custommaterial/opacity/init(_:))

#### Accessing opacity data

- [var scale: Float](/documentation/realitykit/custommaterial/opacity/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/opacity/texture)
- [CustomMaterial.AmbientOcclusion](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct)

#### Creating an ambient occlusion object

- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/init(texture:))
- [init(PhysicallyBasedMaterial.AmbientOcclusion)](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/init(_:))

#### Accessing ambient occlusion values

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/ambientocclusion-swift.struct/texture)
- [CustomMaterial.Specular](/documentation/realitykit/custommaterial/specular-swift.struct)

#### Creating a specular object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/specular-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/specular-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Specular)](/documentation/realitykit/custommaterial/specular-swift.struct/init(_:))

#### Accessing specular values

- [var scale: Float](/documentation/realitykit/custommaterial/specular-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/specular-swift.struct/texture)
- [CustomMaterial.Clearcoat](/documentation/realitykit/custommaterial/clearcoat-swift.struct)

#### Creating a clearcoat object

- [init(floatLiteral: Float)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(floatliteral:))
- [init(scale: Float, texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(scale:texture:))
- [init(PhysicallyBasedMaterial.Clearcoat)](/documentation/realitykit/custommaterial/clearcoat-swift.struct/init(_:))

#### Accessing clearcoat values

- [var scale: Float](/documentation/realitykit/custommaterial/clearcoat-swift.struct/scale)
- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/clearcoat-swift.struct/texture)
- [CustomMaterial.ClearcoatNormal](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct)

#### Initializers

- [init(PhysicallyBasedMaterial.ClearcoatNormal)](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/init(_:))
- [init(texture: CustomMaterial.Texture?)](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/init(texture:))

#### Instance Properties

- [var texture: CustomMaterial.Texture?](/documentation/realitykit/custommaterial/clearcoatnormal-swift.struct/texture)
- [CustomMaterial.ResourceStorage](/documentation/realitykit/custommaterial/resourcestorage)

#### Subscripts

- [subscript<BufferType>(buffer _: KeyPath<UniformsType, UnsafeMutablePointer<BufferType>?>) -> LowLevelBuffer?](/documentation/realitykit/custommaterial/resourcestorage/subscript(buffer:))
- [subscript(textureResource _: KeyPath<UniformsType, UInt64>) -> TextureResource](/documentation/realitykit/custommaterial/resourcestorage/subscript(textureresource:))
- [CustomMaterial.TextureCoordinateTransform](/documentation/realitykit/custommaterial/texturecoordinatetransform-swift.typealias)
- [CustomMaterial.FaceCulling](/documentation/realitykit/custommaterial/faceculling-swift.typealias)
- [CustomMaterial.Texture](/documentation/realitykit/custommaterial/texture)

### Error types

- [CustomMaterialError](/documentation/realitykit/custommaterialerror)

#### Enumeration Cases

- [case defaultSurfaceShaderForMaterialNotFound](/documentation/realitykit/custommaterialerror/defaultsurfaceshaderformaterialnotfound)
- [case geometryModifierFunctionNotFound](/documentation/realitykit/custommaterialerror/geometrymodifierfunctionnotfound)
- [case surfaceShaderFunctionNotFound](/documentation/realitykit/custommaterialerror/surfaceshaderfunctionnotfound)

### Material types

- [Material](/documentation/realitykit/material)

#### Identifying a material

- [var name: String?](/documentation/realitykit/material/name)

#### Type Aliases

- [Material.Color](/documentation/realitykit/material/color)
- [Material.Parameters](/documentation/realitykit/material/parameters)
- [Material.Color](/documentation/realitykit/material/color)
- [Material.Parameters](/documentation/realitykit/material/parameters)
- [MaterialParameterTypes](/documentation/realitykit/materialparametertypes)

#### Structures

- [MaterialParameterTypes.TextureCoordinateTransform](/documentation/realitykit/materialparametertypes/texturecoordinatetransform)

##### Creating a texture coordinate transform

- [init(offset: SIMD2<Float>, scale: SIMD2<Float>, rotation: Float)](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/init(offset:scale:rotation:))

##### Accessing the transform values

- [var offset: SIMD2<Float>](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/offset)
- [var scale: SIMD2<Float>](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/scale)
- [var rotation: Float](/documentation/realitykit/materialparametertypes/texturecoordinatetransform/rotation)

#### Enumerations

- [MaterialParameterTypes.BlendMode](/documentation/realitykit/materialparametertypes/blendmode)

##### Enumeration Cases

- [case add](/documentation/realitykit/materialparametertypes/blendmode/add)
- [case alpha](/documentation/realitykit/materialparametertypes/blendmode/alpha)
- [MaterialParameterTypes.FaceCulling](/documentation/realitykit/materialparametertypes/faceculling)

##### Face culling

- [case front](/documentation/realitykit/materialparametertypes/faceculling/front)
- [case back](/documentation/realitykit/materialparametertypes/faceculling/back)
- [case none](/documentation/realitykit/materialparametertypes/faceculling/none)
- [MaterialParameterTypes.TriangleFillMode](/documentation/realitykit/materialparametertypes/trianglefillmode)

##### Enumeration Cases

- [case fill](/documentation/realitykit/materialparametertypes/trianglefillmode/fill)
- [case lines](/documentation/realitykit/materialparametertypes/trianglefillmode/lines)
- [MaterialParameters](/documentation/realitykit/materialparameters)

#### Structures

- [MaterialParameters.Handle](/documentation/realitykit/materialparameters/handle)
- [MaterialParameters.Texture](/documentation/realitykit/materialparameters/texture)

##### Structures

- [MaterialParameters.Texture.Sampler](/documentation/realitykit/materialparameters/texture/sampler-swift.struct)

###### Initializers

- [init()](/documentation/realitykit/materialparameters/texture/sampler-swift.struct/init())
- [init(MTLSamplerDescriptor)](/documentation/realitykit/materialparameters/texture/sampler-swift.struct/init(_:))

###### Instance Methods

- [func access<R>((MTLSamplerDescriptor) throws -> R) rethrows -> R](/documentation/realitykit/materialparameters/texture/sampler-swift.struct/access(_:))
- [func modify<R>((MTLSamplerDescriptor) throws -> R) rethrows -> R](/documentation/realitykit/materialparameters/texture/sampler-swift.struct/modify(_:))

##### Initializers

- [init(TextureResource)](/documentation/realitykit/materialparameters/texture/init(_:))
- [init(TextureResource, sampler: MaterialParameters.Texture.Sampler)](/documentation/realitykit/materialparameters/texture/init(_:sampler:))

##### Instance Properties

- [var resource: TextureResource](/documentation/realitykit/materialparameters/texture/resource)
- [var sampler: MaterialParameters.Texture.Sampler](/documentation/realitykit/materialparameters/texture/sampler-swift.property)
- [var swizzle: MTLTextureSwizzleChannels](/documentation/realitykit/materialparameters/texture/swizzle)
- [var uvIndex: Int](/documentation/realitykit/materialparameters/texture/uvindex)

#### Enumerations

- [MaterialParameters.Value](/documentation/realitykit/materialparameters/value)

##### Enumeration Cases

- [case bool(Bool)](/documentation/realitykit/materialparameters/value/bool(_:))
- [case color(CGColor)](/documentation/realitykit/materialparameters/value/color(_:)-swift.enum.case)
- [case float(Float)](/documentation/realitykit/materialparameters/value/float(_:))
- [case float2x2(float2x2)](/documentation/realitykit/materialparameters/value/float2x2(_:))
- [case float3x3(float3x3)](/documentation/realitykit/materialparameters/value/float3x3(_:))
- [case float4x4(float4x4)](/documentation/realitykit/materialparameters/value/float4x4(_:))
- [case int(Int32)](/documentation/realitykit/materialparameters/value/int(_:))
- [case simd2Float(SIMD2<Float>)](/documentation/realitykit/materialparameters/value/simd2float(_:))
- [case simd3Float(SIMD3<Float>)](/documentation/realitykit/materialparameters/value/simd3float(_:))
- [case simd4Float(SIMD4<Float>)](/documentation/realitykit/materialparameters/value/simd4float(_:))
- [case texture(MaterialParameters.Texture)](/documentation/realitykit/materialparameters/value/texture(_:))
- [case textureResource(TextureResource)](/documentation/realitykit/materialparameters/value/textureresource(_:))

##### Instance Properties

- [var colorValue: NSColor?](/documentation/realitykit/materialparameters/value/colorvalue-12h12)
- [var colorValue: UIColor?](/documentation/realitykit/materialparameters/value/colorvalue-1j7y0)

##### Type Methods

- [static color(_:)](/documentation/realitykit/materialparameters/value/color(_:)-6bk3t)
- [MaterialColorParameter](/documentation/realitykit/materialcolorparameter)

#### Selecting color parameters

- [case color(NSColor)](/documentation/realitykit/materialcolorparameter/color(_:)-7gx04)
- [case texture(TextureResource)](/documentation/realitykit/materialcolorparameter/texture(_:))

#### Operators

- [static func == (MaterialColorParameter, MaterialColorParameter) -> Bool](/documentation/realitykit/materialcolorparameter/==(_:_:))

#### Enumeration Cases

- [case color(UIColor)](/documentation/realitykit/materialcolorparameter/color(_:)-49aw0)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/materialcolorparameter/hash(into:))
- [MaterialScalarParameter](/documentation/realitykit/materialscalarparameter)

#### Getting scalar parameters

- [case float(Float)](/documentation/realitykit/materialscalarparameter/float(_:))
- [case texture(TextureResource)](/documentation/realitykit/materialscalarparameter/texture(_:))

#### Creating a scalar parameter

- [init(floatLiteral: Float)](/documentation/realitykit/materialscalarparameter/init(floatliteral:))
- [init(integerLiteral: Int)](/documentation/realitykit/materialscalarparameter/init(integerliteral:))

#### Operators

- [static func == (MaterialScalarParameter, MaterialScalarParameter) -> Bool](/documentation/realitykit/materialscalarparameter/==(_:_:))

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/materialscalarparameter/hash(into:))
- [Anchors](/documentation/realitykit/scene-content-anchors)

### Anchoring components

- [AnchoringComponent](/documentation/realitykit/anchoringcomponent)

#### Creating an anchoring component

- [init(_:)](/documentation/realitykit/anchoringcomponent/init(_:))
- [init(AnchoringComponent.Target, trackingMode: AnchoringComponent.TrackingMode)](/documentation/realitykit/anchoringcomponent/init(_:trackingmode:))
- [init(AnchoringComponent.Target, trackingMode: AnchoringComponent.TrackingMode, physicsSimulation: AnchoringComponent.PhysicsSimulation)](/documentation/realitykit/anchoringcomponent/init(_:trackingmode:physicssimulation:))

#### Configuring the anchor

- [let target: AnchoringComponent.Target](/documentation/realitykit/anchoringcomponent/target-swift.property)
- [var trackingMode: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.property)
- [var physicsSimulation: AnchoringComponent.PhysicsSimulation](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.property)

#### Anchor targets

- [AnchoringComponent.Target](/documentation/realitykit/anchoringcomponent/target-swift.enum)

##### Basic anchor targets

- [case world(transform: float4x4)](/documentation/realitykit/anchoringcomponent/target-swift.enum/world(transform:))
- [case plane(AnchoringComponent.Target.Alignment, classification: AnchoringComponent.Target.Classification, minimumBounds: SIMD2<Float>)](/documentation/realitykit/anchoringcomponent/target-swift.enum/plane(_:classification:minimumbounds:))
- [case camera](/documentation/realitykit/anchoringcomponent/target-swift.enum/camera)
- [case anchor(identifier: UUID)](/documentation/realitykit/anchoringcomponent/target-swift.enum/anchor(identifier:))

##### Human anchor targets

- [case face](/documentation/realitykit/anchoringcomponent/target-swift.enum/face)
- [case body](/documentation/realitykit/anchoringcomponent/target-swift.enum/body)
- [case hand(AnchoringComponent.Target.Chirality, location: AnchoringComponent.Target.HandLocation)](/documentation/realitykit/anchoringcomponent/target-swift.enum/hand(_:location:))
- [case head](/documentation/realitykit/anchoringcomponent/target-swift.enum/head)

##### Image and object anchor targets

- [case image(group: String, name: String)](/documentation/realitykit/anchoringcomponent/target-swift.enum/image(group:name:))
- [case referenceImage(from: AnchoringComponent.ImageAnchoringSource)](/documentation/realitykit/anchoringcomponent/target-swift.enum/referenceimage(from:))
- [case object(group: String, name: String)](/documentation/realitykit/anchoringcomponent/target-swift.enum/object(group:name:))
- [case referenceObject(from: AnchoringComponent.ObjectAnchoringSource)](/documentation/realitykit/anchoringcomponent/target-swift.enum/referenceobject(from:))

##### Structures

- [AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment)

###### Choosing an alignment

- [static let horizontal: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/horizontal)
- [static let vertical: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/vertical)
- [static let any: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/any)
- [AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification)

###### Classifying a target

- [static let wall: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/wall)
- [static let floor: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/floor)
- [static let ceiling: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/ceiling)
- [static let table: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/table)
- [static let seat: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/seat)
- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)

###### Creating a target classification instance

- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)
- [AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation)

###### Structures

- [AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint)

###### Type Properties

- [static let forearmArm: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmarm)
- [static let forearmWrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmwrist)
- [static let indexFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatebase)
- [static let indexFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatetip)
- [static let indexFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerknuckle)
- [static let indexFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingermetacarpal)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingertip)
- [static let littleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatebase)
- [static let littleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatetip)
- [static let littleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerknuckle)
- [static let littleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingermetacarpal)
- [static let littleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingertip)
- [static let middleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatebase)
- [static let middleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatetip)
- [static let middleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerknuckle)
- [static let middleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingermetacarpal)
- [static let middleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingertip)
- [static let ringFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatebase)
- [static let ringFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatetip)
- [static let ringFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerknuckle)
- [static let ringFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingermetacarpal)
- [static let ringFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingertip)
- [static let thumbIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatebase)
- [static let thumbIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatetip)
- [static let thumbKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbknuckle)
- [static let thumbTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/wrist)

###### Type Properties

- [static let aboveHand: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/abovehand)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/indexfingertip)
- [static let palm: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/palm)
- [static let thumbTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/wrist)

###### Type Methods

- [static func joint(for: AnchoringComponent.Target.HandLocation.HandJoint) -> AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/joint(for:))

##### Operators

- [static func == (AnchoringComponent.Target, AnchoringComponent.Target) -> Bool](/documentation/realitykit/anchoringcomponent/target-swift.enum/==(_:_:))

##### Enumeration Cases

- [case accessory(from: AnchoringComponent.AccessoryAnchoringSource, location: AnchoringComponent.AccessoryLocation)](/documentation/realitykit/anchoringcomponent/target-swift.enum/accessory(from:location:))

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/anchoringcomponent/target-swift.enum/hash(into:))

##### Enumerations

- [AnchoringComponent.Target.Chirality](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality)

###### Enumeration Cases

- [case either](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/either)
- [case left](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/left)
- [case right](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/right)
- [AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct)

##### Type Properties

- [static let continuous: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/continuous)
- [static let once: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/once)
- [static let predicted: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/predicted)
- [AnchoringComponent.PhysicsSimulation](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum)

##### Enumeration Cases

- [case isolated](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum/isolated)
- [case none](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum/none)

#### Structures

- [AnchoringComponent.AccessoryAnchoringSource](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource)

##### Initializers

- [init(accessory: Accessory) throws](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource/init(accessory:))
- [init(device: any GCDevice) async throws](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource/init(device:))

##### Instance Properties

- [var accessoryLocations: [AnchoringComponent.AccessoryLocation]](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource/accessorylocations)
- [var underlyingAccessory: Accessory?](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource/underlyingaccessory)

##### Instance Methods

- [func locationName(named: String) -> AnchoringComponent.AccessoryLocation?](/documentation/realitykit/anchoringcomponent/accessoryanchoringsource/locationname(named:))
- [AnchoringComponent.AccessoryLocation](/documentation/realitykit/anchoringcomponent/accessorylocation)

##### Instance Properties

- [var name: String?](/documentation/realitykit/anchoringcomponent/accessorylocation/name)

##### Type Properties

- [static let origin: AnchoringComponent.AccessoryLocation](/documentation/realitykit/anchoringcomponent/accessorylocation/origin)
- [AnchoringComponent.ImageAnchoringSource](/documentation/realitykit/anchoringcomponent/imageanchoringsource)

##### Initializers

- [init(URL, physicalSize: SIMD2<Float>)](/documentation/realitykit/anchoringcomponent/imageanchoringsource/init(_:physicalsize:))
- [init(group: String, name: String)](/documentation/realitykit/anchoringcomponent/imageanchoringsource/init(group:name:))
- [AnchoringComponent.ObjectAnchoringSource](/documentation/realitykit/anchoringcomponent/objectanchoringsource)

##### Initializers

- [init(URL)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(_:))
- [init(group: String, name: String)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(group:name:))
- [init(name: String, in: Bundle)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(name:in:))
- [AnchoringComponent.Target](/documentation/realitykit/anchoringcomponent/target-swift.enum)

#### Basic anchor targets

- [case world(transform: float4x4)](/documentation/realitykit/anchoringcomponent/target-swift.enum/world(transform:))
- [case plane(AnchoringComponent.Target.Alignment, classification: AnchoringComponent.Target.Classification, minimumBounds: SIMD2<Float>)](/documentation/realitykit/anchoringcomponent/target-swift.enum/plane(_:classification:minimumbounds:))
- [case camera](/documentation/realitykit/anchoringcomponent/target-swift.enum/camera)
- [case anchor(identifier: UUID)](/documentation/realitykit/anchoringcomponent/target-swift.enum/anchor(identifier:))

#### Human anchor targets

- [case face](/documentation/realitykit/anchoringcomponent/target-swift.enum/face)
- [case body](/documentation/realitykit/anchoringcomponent/target-swift.enum/body)
- [case hand(AnchoringComponent.Target.Chirality, location: AnchoringComponent.Target.HandLocation)](/documentation/realitykit/anchoringcomponent/target-swift.enum/hand(_:location:))
- [case head](/documentation/realitykit/anchoringcomponent/target-swift.enum/head)

#### Image and object anchor targets

- [case image(group: String, name: String)](/documentation/realitykit/anchoringcomponent/target-swift.enum/image(group:name:))
- [case referenceImage(from: AnchoringComponent.ImageAnchoringSource)](/documentation/realitykit/anchoringcomponent/target-swift.enum/referenceimage(from:))
- [case object(group: String, name: String)](/documentation/realitykit/anchoringcomponent/target-swift.enum/object(group:name:))
- [case referenceObject(from: AnchoringComponent.ObjectAnchoringSource)](/documentation/realitykit/anchoringcomponent/target-swift.enum/referenceobject(from:))

#### Structures

- [AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment)

##### Choosing an alignment

- [static let horizontal: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/horizontal)
- [static let vertical: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/vertical)
- [static let any: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/any)
- [AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification)

##### Classifying a target

- [static let wall: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/wall)
- [static let floor: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/floor)
- [static let ceiling: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/ceiling)
- [static let table: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/table)
- [static let seat: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/seat)
- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)

##### Creating a target classification instance

- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)
- [AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation)

##### Structures

- [AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint)

###### Type Properties

- [static let forearmArm: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmarm)
- [static let forearmWrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmwrist)
- [static let indexFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatebase)
- [static let indexFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatetip)
- [static let indexFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerknuckle)
- [static let indexFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingermetacarpal)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingertip)
- [static let littleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatebase)
- [static let littleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatetip)
- [static let littleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerknuckle)
- [static let littleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingermetacarpal)
- [static let littleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingertip)
- [static let middleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatebase)
- [static let middleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatetip)
- [static let middleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerknuckle)
- [static let middleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingermetacarpal)
- [static let middleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingertip)
- [static let ringFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatebase)
- [static let ringFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatetip)
- [static let ringFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerknuckle)
- [static let ringFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingermetacarpal)
- [static let ringFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingertip)
- [static let thumbIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatebase)
- [static let thumbIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatetip)
- [static let thumbKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbknuckle)
- [static let thumbTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/wrist)

##### Type Properties

- [static let aboveHand: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/abovehand)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/indexfingertip)
- [static let palm: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/palm)
- [static let thumbTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/wrist)

##### Type Methods

- [static func joint(for: AnchoringComponent.Target.HandLocation.HandJoint) -> AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/joint(for:))

#### Operators

- [static func == (AnchoringComponent.Target, AnchoringComponent.Target) -> Bool](/documentation/realitykit/anchoringcomponent/target-swift.enum/==(_:_:))

#### Enumeration Cases

- [case accessory(from: AnchoringComponent.AccessoryAnchoringSource, location: AnchoringComponent.AccessoryLocation)](/documentation/realitykit/anchoringcomponent/target-swift.enum/accessory(from:location:))

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/anchoringcomponent/target-swift.enum/hash(into:))

#### Enumerations

- [AnchoringComponent.Target.Chirality](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality)

##### Enumeration Cases

- [case either](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/either)
- [case left](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/left)
- [case right](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/right)
- [AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct)

#### Type Properties

- [static let continuous: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/continuous)
- [static let once: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/once)
- [static let predicted: AnchoringComponent.TrackingMode](/documentation/realitykit/anchoringcomponent/trackingmode-swift.struct/predicted)
- [ARKitAnchorComponent](/documentation/realitykit/arkitanchorcomponent)

#### Instance Properties

- [var anchor: any Anchor](/documentation/realitykit/arkitanchorcomponent/anchor)
- [var arAnchor: ARAnchor](/documentation/realitykit/arkitanchorcomponent/aranchor)
- [AnchorEntity](/documentation/realitykit/anchorentity)

#### Creating an anchor

- [init()](/documentation/realitykit/anchorentity/init())
- [convenience init(any Anchor)](/documentation/realitykit/anchorentity/init(_:)-9vipc)
- [init(AnchoringComponent.Target)](/documentation/realitykit/anchorentity/init(_:)-9rdwu)
- [convenience init(AnchoringComponent.Target, trackingMode: AnchoringComponent.TrackingMode)](/documentation/realitykit/anchorentity/init(_:trackingmode:))
- [convenience init(AnchoringComponent.Target, trackingMode: AnchoringComponent.TrackingMode, physicsSimulation: AnchoringComponent.PhysicsSimulation)](/documentation/realitykit/anchorentity/init(_:trackingmode:physicssimulation:))
- [convenience init(anchor: ARAnchor)](/documentation/realitykit/anchorentity/init(anchor:))
- [convenience init(plane: AnchoringComponent.Target.Alignment, classification: AnchoringComponent.Target.Classification, minimumBounds: SIMD2<Float>)](/documentation/realitykit/anchorentity/init(plane:classification:minimumbounds:))
- [convenience init(raycastResult: ARRaycastResult)](/documentation/realitykit/anchorentity/init(raycastresult:))
- [convenience init(world: float4x4)](/documentation/realitykit/anchorentity/init(world:)-4snw2)
- [convenience init(world: SIMD3<Float>)](/documentation/realitykit/anchorentity/init(world:)-u9qv)

#### Initializers

- [convenience(_:)](/documentation/realitykit/anchorentity/init(_:))
- [convenience(world:)](/documentation/realitykit/anchorentity/init(world:))
- [HasAnchoring](/documentation/realitykit/hasanchoring)

#### Getting the component

- [var anchoring: AnchoringComponent](/documentation/realitykit/hasanchoring/anchoring)

#### Identifying the AR anchor

- [var anchorIdentifier: UUID?](/documentation/realitykit/hasanchoring/anchoridentifier)

#### Moving the anchor

- [func reanchor(AnchoringComponent.Target, preservingWorldTransform: Bool)](/documentation/realitykit/hasanchoring/reanchor(_:preservingworldtransform:))

### Surface anchor characterization

- [AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment)

#### Choosing an alignment

- [static let horizontal: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/horizontal)
- [static let vertical: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/vertical)
- [static let any: AnchoringComponent.Target.Alignment](/documentation/realitykit/anchoringcomponent/target-swift.enum/alignment/any)
- [AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification)

#### Classifying a target

- [static let wall: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/wall)
- [static let floor: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/floor)
- [static let ceiling: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/ceiling)
- [static let table: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/table)
- [static let seat: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/seat)
- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)

#### Creating a target classification instance

- [static let any: AnchoringComponent.Target.Classification](/documentation/realitykit/anchoringcomponent/target-swift.enum/classification/any)

### Image and object tracking

- [AnchoringComponent.ImageAnchoringSource](/documentation/realitykit/anchoringcomponent/imageanchoringsource)

#### Initializers

- [init(URL, physicalSize: SIMD2<Float>)](/documentation/realitykit/anchoringcomponent/imageanchoringsource/init(_:physicalsize:))
- [init(group: String, name: String)](/documentation/realitykit/anchoringcomponent/imageanchoringsource/init(group:name:))
- [AnchoringComponent.ObjectAnchoringSource](/documentation/realitykit/anchoringcomponent/objectanchoringsource)

#### Initializers

- [init(URL)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(_:))
- [init(group: String, name: String)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(group:name:))
- [init(name: String, in: Bundle)](/documentation/realitykit/anchoringcomponent/objectanchoringsource/init(name:in:))

### Hand tracking

- [Happy Beam](/documentation/visionos/happybeam)
- [AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation)

#### Structures

- [AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint)

##### Type Properties

- [static let forearmArm: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmarm)
- [static let forearmWrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/forearmwrist)
- [static let indexFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatebase)
- [static let indexFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerintermediatetip)
- [static let indexFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingerknuckle)
- [static let indexFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingermetacarpal)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/indexfingertip)
- [static let littleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatebase)
- [static let littleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerintermediatetip)
- [static let littleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingerknuckle)
- [static let littleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingermetacarpal)
- [static let littleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/littlefingertip)
- [static let middleFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatebase)
- [static let middleFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerintermediatetip)
- [static let middleFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingerknuckle)
- [static let middleFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingermetacarpal)
- [static let middleFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/middlefingertip)
- [static let ringFingerIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatebase)
- [static let ringFingerIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerintermediatetip)
- [static let ringFingerKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingerknuckle)
- [static let ringFingerMetacarpal: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingermetacarpal)
- [static let ringFingerTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/ringfingertip)
- [static let thumbIntermediateBase: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatebase)
- [static let thumbIntermediateTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbintermediatetip)
- [static let thumbKnuckle: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbknuckle)
- [static let thumbTip: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation.HandJoint](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/handjoint/wrist)

#### Type Properties

- [static let aboveHand: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/abovehand)
- [static let indexFingerTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/indexfingertip)
- [static let palm: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/palm)
- [static let thumbTip: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/thumbtip)
- [static let wrist: AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/wrist)

#### Type Methods

- [static func joint(for: AnchoringComponent.Target.HandLocation.HandJoint) -> AnchoringComponent.Target.HandLocation](/documentation/realitykit/anchoringcomponent/target-swift.enum/handlocation/joint(for:))
- [AnchoringComponent.Target.Chirality](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality)

#### Enumeration Cases

- [case either](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/either)
- [case left](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/left)
- [case right](/documentation/realitykit/anchoringcomponent/target-swift.enum/chirality/right)

### Spatial tracking

- [SpatialTrackingSession](/documentation/realitykit/spatialtrackingsession)

#### Structures

- [SpatialTrackingSession.Configuration](/documentation/realitykit/spatialtrackingsession/configuration)

##### Structures

- [SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability)

###### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/debugdescription)

###### Type Properties

- [static let accessory: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/accessory)
- [static let body: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/body)
- [static let camera: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/camera)
- [static let face: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/face)
- [static let hand: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/hand)
- [static let image: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/image)
- [static let object: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/object)
- [static let plane: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/plane)
- [static let world: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/world)
- [SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability)

###### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/debugdescription)

###### Type Properties

- [static let collision: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/collision)
- [static let occlusion: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/occlusion)
- [static let physics: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/physics)
- [static let shadow: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/shadow)

##### Initializers

- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:))
- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>, sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:sceneunderstanding:))
- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>, sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>, camera: SpatialTrackingSession.Configuration.Camera)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:sceneunderstanding:camera:))

##### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/debugdescription)

##### Instance Methods

- [func arConfiguration() -> ARConfiguration?](/documentation/realitykit/spatialtrackingsession/configuration/arconfiguration())
- [func supportedConfiguration() -> SpatialTrackingSession.Configuration](/documentation/realitykit/spatialtrackingsession/configuration/supportedconfiguration())

##### Enumerations

- [SpatialTrackingSession.Configuration.Camera](/documentation/realitykit/spatialtrackingsession/configuration/camera)

###### Enumeration Cases

- [case back](/documentation/realitykit/spatialtrackingsession/configuration/camera/back)
- [case front](/documentation/realitykit/spatialtrackingsession/configuration/camera/front)
- [SpatialTrackingSession.UnavailableCapabilities](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities)

##### Initializers

- [init()](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/init())

##### Instance Properties

- [var anchor: Set<SpatialTrackingSession.Configuration.AnchorCapability>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/anchor)
- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/debugdescription)
- [var missingAuthorizations: Set<ARKitSession.AuthorizationType>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/missingauthorizations)
- [var missingCameraAuthorization: Bool?](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/missingcameraauthorization)
- [var sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/sceneunderstanding)

#### Initializers

- [init()](/documentation/realitykit/spatialtrackingsession/init())

#### Instance Methods

- [func run(SpatialTrackingSession.Configuration) async -> SpatialTrackingSession.UnavailableCapabilities?](/documentation/realitykit/spatialtrackingsession/run(_:))
- [func run(SpatialTrackingSession.Configuration, session: ARSession, arConfiguration: ARConfiguration) async -> SpatialTrackingSession.UnavailableCapabilities?](/documentation/realitykit/spatialtrackingsession/run(_:session:arconfiguration:))
- [func stop() async](/documentation/realitykit/spatialtrackingsession/stop())
- [SpatialTrackingSession.Configuration](/documentation/realitykit/spatialtrackingsession/configuration)

#### Structures

- [SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability)

##### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/debugdescription)

##### Type Properties

- [static let accessory: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/accessory)
- [static let body: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/body)
- [static let camera: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/camera)
- [static let face: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/face)
- [static let hand: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/hand)
- [static let image: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/image)
- [static let object: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/object)
- [static let plane: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/plane)
- [static let world: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/world)
- [SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability)

##### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/debugdescription)

##### Type Properties

- [static let collision: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/collision)
- [static let occlusion: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/occlusion)
- [static let physics: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/physics)
- [static let shadow: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/shadow)

#### Initializers

- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:))
- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>, sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:sceneunderstanding:))
- [init(tracking: Set<SpatialTrackingSession.Configuration.AnchorCapability>, sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>, camera: SpatialTrackingSession.Configuration.Camera)](/documentation/realitykit/spatialtrackingsession/configuration/init(tracking:sceneunderstanding:camera:))

#### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/debugdescription)

#### Instance Methods

- [func arConfiguration() -> ARConfiguration?](/documentation/realitykit/spatialtrackingsession/configuration/arconfiguration())
- [func supportedConfiguration() -> SpatialTrackingSession.Configuration](/documentation/realitykit/spatialtrackingsession/configuration/supportedconfiguration())

#### Enumerations

- [SpatialTrackingSession.Configuration.Camera](/documentation/realitykit/spatialtrackingsession/configuration/camera)

##### Enumeration Cases

- [case back](/documentation/realitykit/spatialtrackingsession/configuration/camera/back)
- [case front](/documentation/realitykit/spatialtrackingsession/configuration/camera/front)
- [SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability)

#### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/debugdescription)

#### Type Properties

- [static let accessory: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/accessory)
- [static let body: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/body)
- [static let camera: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/camera)
- [static let face: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/face)
- [static let hand: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/hand)
- [static let image: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/image)
- [static let object: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/object)
- [static let plane: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/plane)
- [static let world: SpatialTrackingSession.Configuration.AnchorCapability](/documentation/realitykit/spatialtrackingsession/configuration/anchorcapability/world)
- [SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability)

#### Instance Properties

- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/debugdescription)

#### Type Properties

- [static let collision: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/collision)
- [static let occlusion: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/occlusion)
- [static let physics: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/physics)
- [static let shadow: SpatialTrackingSession.Configuration.SceneUnderstandingCapability](/documentation/realitykit/spatialtrackingsession/configuration/sceneunderstandingcapability/shadow)
- [SpatialTrackingSession.Configuration.Camera](/documentation/realitykit/spatialtrackingsession/configuration/camera)

#### Enumeration Cases

- [case back](/documentation/realitykit/spatialtrackingsession/configuration/camera/back)
- [case front](/documentation/realitykit/spatialtrackingsession/configuration/camera/front)
- [SpatialTrackingSession.UnavailableCapabilities](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities)

#### Initializers

- [init()](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/init())

#### Instance Properties

- [var anchor: Set<SpatialTrackingSession.Configuration.AnchorCapability>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/anchor)
- [var debugDescription: String](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/debugdescription)
- [var missingAuthorizations: Set<ARKitSession.AuthorizationType>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/missingauthorizations)
- [var missingCameraAuthorization: Bool?](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/missingcameraauthorization)
- [var sceneUnderstanding: Set<SpatialTrackingSession.Configuration.SceneUnderstandingCapability>](/documentation/realitykit/spatialtrackingsession/unavailablecapabilities/sceneunderstanding)

### Body and face tracking

- [Creating an App for Face-Painting in AR](/documentation/realitykit/creating-an-app-for-face-painting-in-ar)
- [Occluding virtual content with people](/documentation/arkit/occluding-virtual-content-with-people)
- [BodyTrackingComponent](/documentation/realitykit/bodytrackingcomponent)

#### Creating a body tracking component

- [init()](/documentation/realitykit/bodytrackingcomponent/init())
- [init(BodyTrackingComponent.Target)](/documentation/realitykit/bodytrackingcomponent/init(_:))

#### Pausing body tracking

- [var isPaused: Bool](/documentation/realitykit/bodytrackingcomponent/ispaused)

#### Selecting a body to track

- [var target: BodyTrackingComponent.Target](/documentation/realitykit/bodytrackingcomponent/target-swift.property)
- [BodyTrackingComponent.Target](/documentation/realitykit/bodytrackingcomponent/target-swift.enum)

##### Body tracking target types

- [case any](/documentation/realitykit/bodytrackingcomponent/target-swift.enum/any)
- [case body(identifier: UUID)](/documentation/realitykit/bodytrackingcomponent/target-swift.enum/body(identifier:))

##### Operators

- [static func == (BodyTrackingComponent.Target, BodyTrackingComponent.Target) -> Bool](/documentation/realitykit/bodytrackingcomponent/target-swift.enum/==(_:_:))

##### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/bodytrackingcomponent/target-swift.enum/hash(into:))
- [BodyTrackedEntity](/documentation/realitykit/bodytrackedentity)

#### Configuring body tracking

- [HasBodyTracking](/documentation/realitykit/hasbodytracking)

#### Accessing the component

- [var bodyTracking: BodyTrackingComponent](/documentation/realitykit/hasbodytracking/bodytracking)

### Accessory tracking

- [Tracking a handheld accessory as a virtual sculpting tool](/documentation/realitykit/tracking-a-handheld-accessory-as-a-virtual-sculpting-tool)

### Physics simulation space

- [AnchoringComponent.PhysicsSimulation](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum)

#### Enumeration Cases

- [case isolated](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum/isolated)
- [case none](/documentation/realitykit/anchoringcomponent/physicssimulation-swift.enum/none)
- [Lights and cameras](/documentation/realitykit/scene-content-lights-and-cameras)

### Cameras

- [PerspectiveCameraComponent](/documentation/realitykit/perspectivecameracomponent)

#### Creating a camera component

- [init(near: Float, far: Float, fieldOfViewInDegrees: Float)](/documentation/realitykit/perspectivecameracomponent/init(near:far:fieldofviewindegrees:))
- [init(near: Float, far: Float, fieldOfViewInDegrees: Float, fieldOfViewOrientation: CameraFieldOfViewOrientation)](/documentation/realitykit/perspectivecameracomponent/init(near:far:fieldofviewindegrees:fieldofvieworientation:))

#### Setting focal points

- [var far: Float](/documentation/realitykit/perspectivecameracomponent/far)
- [var near: Float](/documentation/realitykit/perspectivecameracomponent/near)

#### Setting the field of view

- [var fieldOfViewInDegrees: Float](/documentation/realitykit/perspectivecameracomponent/fieldofviewindegrees)
- [var fieldOfViewOrientation: CameraFieldOfViewOrientation](/documentation/realitykit/perspectivecameracomponent/fieldofvieworientation)
- [OrthographicCameraComponent](/documentation/realitykit/orthographiccameracomponent)

#### Creating a camera component

- [init()](/documentation/realitykit/orthographiccameracomponent/init())

#### Setting focal points

- [var far: Float](/documentation/realitykit/orthographiccameracomponent/far)
- [var near: Float](/documentation/realitykit/orthographiccameracomponent/near)

#### Setting the camera scale

- [var scale: Float](/documentation/realitykit/orthographiccameracomponent/scale)
- [var scaleDirection: CameraFieldOfViewOrientation](/documentation/realitykit/orthographiccameracomponent/scaledirection)
- [CameraFieldOfViewOrientation](/documentation/realitykit/camerafieldofvieworientation)

#### Enumeration Cases

- [case horizontal](/documentation/realitykit/camerafieldofvieworientation/horizontal)
- [case vertical](/documentation/realitykit/camerafieldofvieworientation/vertical)
- [ProjectiveTransformCameraComponent](/documentation/realitykit/projectivetransformcameracomponent)

#### Initializers

- [init(projectionMatrix: float4x4)](/documentation/realitykit/projectivetransformcameracomponent/init(projectionmatrix:))

#### Instance Properties

- [var transform: float4x4](/documentation/realitykit/projectivetransformcameracomponent/transform)
- [PerspectiveCamera](/documentation/realitykit/perspectivecamera)

#### Creating a camera

- [init()](/documentation/realitykit/perspectivecamera/init())

### Point lights

- [PointLightComponent](/documentation/realitykit/pointlightcomponent)

#### Creating a point light component

- [init(cgColor: CGColor, intensity: Float, attenuationRadius: Float)](/documentation/realitykit/pointlightcomponent/init(cgcolor:intensity:attenuationradius:))

#### Configuring the light

- [var attenuationRadius: Float](/documentation/realitykit/pointlightcomponent/attenuationradius)
- [var intensity: Float](/documentation/realitykit/pointlightcomponent/intensity)
- [var attenuationFalloffExponent: Float](/documentation/realitykit/pointlightcomponent/attenuationfalloffexponent)

#### Supporting types

- [PointLightComponent.Color](/documentation/realitykit/pointlightcomponent/color-swift.typealias)

#### Initializers

- [init(color:intensity:attenuationRadius:)](/documentation/realitykit/pointlightcomponent/init(color:intensity:attenuationradius:))
- [init(color:intensity:attenuationRadius:attenuationFalloffExponent:)](/documentation/realitykit/pointlightcomponent/init(color:intensity:attenuationradius:attenuationfalloffexponent:))

#### Instance Properties

- [var color: PointLightComponent.Color](/documentation/realitykit/pointlightcomponent/color-4ksx7)
- [var color: PointLightComponent.Color](/documentation/realitykit/pointlightcomponent/color-8gecu)

### Directional lights and their shadows

- [DirectionalLightComponent](/documentation/realitykit/directionallightcomponent)

#### Creating a directional light

- [init(color: DirectionalLightComponent.Color, intensity: Float)](/documentation/realitykit/directionallightcomponent/init(color:intensity:))
- [init(color: DirectionalLightComponent.Color, intensity: Float, isRealWorldProxy: Bool)](/documentation/realitykit/directionallightcomponent/init(color:intensity:isrealworldproxy:)-42x82)
- [init(color: DirectionalLightComponent.Color, intensity: Float, isRealWorldProxy: Bool)](/documentation/realitykit/directionallightcomponent/init(color:intensity:isrealworldproxy:)-42x82)

#### Setting the color

- [var color: DirectionalLightComponent.Color](/documentation/realitykit/directionallightcomponent/color-5ebuh)
- [var color: DirectionalLightComponent.Color](/documentation/realitykit/directionallightcomponent/color-5ebuh)

#### Setting intensity and shadows

- [var intensity: Float](/documentation/realitykit/directionallightcomponent/intensity)
- [var isRealWorldProxy: Bool](/documentation/realitykit/directionallightcomponent/isrealworldproxy)

#### Supporting types

- [DirectionalLightComponent.Color](/documentation/realitykit/directionallightcomponent/color-swift.typealias)

#### Structures

- [DirectionalLightComponent.Shadow](/documentation/realitykit/directionallightcomponent/shadow)

##### Creating the shadow

- [init()](/documentation/realitykit/directionallightcomponent/shadow/init())
- [init(shadowProjection: DirectionalLightComponent.Shadow.ShadowProjectionType, depthBias: Float, cullMode: DirectionalLightComponent.Shadow.ShadowMapCullMode?)](/documentation/realitykit/directionallightcomponent/shadow/init(shadowprojection:depthbias:cullmode:))
- [init(maximumDistance: Float, depthBias: Float)](/documentation/realitykit/directionallightcomponent/shadow/init(maximumdistance:depthbias:))

##### Configuring the shadow

- [var depthBias: Float](/documentation/realitykit/directionallightcomponent/shadow/depthbias)
- [var cullModeOverride: DirectionalLightComponent.Shadow.ShadowMapCullMode?](/documentation/realitykit/directionallightcomponent/shadow/cullmodeoverride)
- [var shadowProjection: DirectionalLightComponent.Shadow.ShadowProjectionType](/documentation/realitykit/directionallightcomponent/shadow/shadowprojection)
- [var maximumDistance: Float](/documentation/realitykit/directionallightcomponent/shadow/maximumdistance)

##### Registering a component type


##### Type Aliases

- [DirectionalLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/directionallightcomponent/shadow/shadowmapcullmode)

##### Enumerations

- [DirectionalLightComponent.Shadow.ShadowProjectionType](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype)

###### Shadow projection types

- [case automatic(maximumDistance: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/automatic(maximumdistance:))
- [case fixed(zNear: Float, zFar: Float, orthographicScale: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/fixed(znear:zfar:orthographicscale:))

#### Initializers

- [init(color:intensity:isRealWorldProxy:)](/documentation/realitykit/directionallightcomponent/init(color:intensity:isrealworldproxy:))

#### Instance Properties

- [var color: DirectionalLightComponent.Color](/documentation/realitykit/directionallightcomponent/color-7hs4n)
- [DirectionalLightComponent.Shadow](/documentation/realitykit/directionallightcomponent/shadow)

#### Creating the shadow

- [init()](/documentation/realitykit/directionallightcomponent/shadow/init())
- [init(shadowProjection: DirectionalLightComponent.Shadow.ShadowProjectionType, depthBias: Float, cullMode: DirectionalLightComponent.Shadow.ShadowMapCullMode?)](/documentation/realitykit/directionallightcomponent/shadow/init(shadowprojection:depthbias:cullmode:))
- [init(maximumDistance: Float, depthBias: Float)](/documentation/realitykit/directionallightcomponent/shadow/init(maximumdistance:depthbias:))

#### Configuring the shadow

- [var depthBias: Float](/documentation/realitykit/directionallightcomponent/shadow/depthbias)
- [var cullModeOverride: DirectionalLightComponent.Shadow.ShadowMapCullMode?](/documentation/realitykit/directionallightcomponent/shadow/cullmodeoverride)
- [var shadowProjection: DirectionalLightComponent.Shadow.ShadowProjectionType](/documentation/realitykit/directionallightcomponent/shadow/shadowprojection)
- [var maximumDistance: Float](/documentation/realitykit/directionallightcomponent/shadow/maximumdistance)

#### Registering a component type


#### Type Aliases

- [DirectionalLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/directionallightcomponent/shadow/shadowmapcullmode)

#### Enumerations

- [DirectionalLightComponent.Shadow.ShadowProjectionType](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype)

##### Shadow projection types

- [case automatic(maximumDistance: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/automatic(maximumdistance:))
- [case fixed(zNear: Float, zFar: Float, orthographicScale: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/fixed(znear:zfar:orthographicscale:))
- [DirectionalLightComponent.Shadow.ShadowProjectionType](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype)

#### Shadow projection types

- [case automatic(maximumDistance: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/automatic(maximumdistance:))
- [case fixed(zNear: Float, zFar: Float, orthographicScale: Float)](/documentation/realitykit/directionallightcomponent/shadow/shadowprojectiontype/fixed(znear:zfar:orthographicscale:))
- [DirectionalLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/directionallightcomponent/shadow/shadowmapcullmode)

### Spotlights and their shadows

- [SpotLightComponent](/documentation/realitykit/spotlightcomponent)

#### Configuring the spotlight

- [var intensity: Float](/documentation/realitykit/spotlightcomponent/intensity)
- [var innerAngleInDegrees: Float](/documentation/realitykit/spotlightcomponent/innerangleindegrees)
- [var outerAngleInDegrees: Float](/documentation/realitykit/spotlightcomponent/outerangleindegrees)
- [var attenuationRadius: Float](/documentation/realitykit/spotlightcomponent/attenuationradius)
- [var attenuationFalloffExponent: Float](/documentation/realitykit/spotlightcomponent/attenuationfalloffexponent)

#### Supporting types

- [SpotLightComponent.Color](/documentation/realitykit/spotlightcomponent/color-swift.typealias)

#### Structures

- [SpotLightComponent.Shadow](/documentation/realitykit/spotlightcomponent/shadow)

##### Creating a shadow

- [init()](/documentation/realitykit/spotlightcomponent/shadow/init())

##### Configuring the shadow

- [var depthBias: Float](/documentation/realitykit/spotlightcomponent/shadow/depthbias)
- [var zNear: SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/znear)
- [var zFar: SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/zfar)
- [var cullModeOverride: SpotLightComponent.Shadow.ShadowMapCullMode?](/documentation/realitykit/spotlightcomponent/shadow/cullmodeoverride)

##### Type Aliases

- [SpotLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/spotlightcomponent/shadow/shadowmapcullmode)

##### Enumerations

- [SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane)

###### Clipping plane options

- [case automatic](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/automatic)
- [case fixed(Float)](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/fixed(_:))

#### Initializers

- [init(color:intensity:innerAngleInDegrees:outerAngleInDegrees:attenuationRadius:)](/documentation/realitykit/spotlightcomponent/init(color:intensity:innerangleindegrees:outerangleindegrees:attenuationradius:))
- [init(color:intensity:innerAngleInDegrees:outerAngleInDegrees:attenuationRadius:attenuationFalloffExponent:)](/documentation/realitykit/spotlightcomponent/init(color:intensity:innerangleindegrees:outerangleindegrees:attenuationradius:attenuationfalloffexponent:))

#### Instance Properties

- [var color: SpotLightComponent.Color](/documentation/realitykit/spotlightcomponent/color-2o8ve)
- [var color: SpotLightComponent.Color](/documentation/realitykit/spotlightcomponent/color-6enoj)
- [SpotLightComponent.Shadow](/documentation/realitykit/spotlightcomponent/shadow)

#### Creating a shadow

- [init()](/documentation/realitykit/spotlightcomponent/shadow/init())

#### Configuring the shadow

- [var depthBias: Float](/documentation/realitykit/spotlightcomponent/shadow/depthbias)
- [var zNear: SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/znear)
- [var zFar: SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/zfar)
- [var cullModeOverride: SpotLightComponent.Shadow.ShadowMapCullMode?](/documentation/realitykit/spotlightcomponent/shadow/cullmodeoverride)

#### Type Aliases

- [SpotLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/spotlightcomponent/shadow/shadowmapcullmode)

#### Enumerations

- [SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane)

##### Clipping plane options

- [case automatic](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/automatic)
- [case fixed(Float)](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/fixed(_:))
- [SpotLightComponent.Shadow.ShadowClippingPlane](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane)

#### Clipping plane options

- [case automatic](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/automatic)
- [case fixed(Float)](/documentation/realitykit/spotlightcomponent/shadow/shadowclippingplane/fixed(_:))
- [SpotLightComponent.Shadow.ShadowMapCullMode](/documentation/realitykit/spotlightcomponent/shadow/shadowmapcullmode)

### Image-based lights

- [ImageBasedLightComponent](/documentation/realitykit/imagebasedlightcomponent)

#### Initializers

- [init(source: ImageBasedLightComponent.Source, intensityExponent: Float)](/documentation/realitykit/imagebasedlightcomponent/init(source:intensityexponent:))

#### Instance Properties

- [var inheritsRotation: Bool](/documentation/realitykit/imagebasedlightcomponent/inheritsrotation)
- [var intensityExponent: Float](/documentation/realitykit/imagebasedlightcomponent/intensityexponent)
- [var source: ImageBasedLightComponent.Source](/documentation/realitykit/imagebasedlightcomponent/source-swift.property)

#### Enumerations

- [ImageBasedLightComponent.Source](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum)

##### Enumeration Cases

- [case blend(EnvironmentResource, EnvironmentResource, Float)](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/blend(_:_:_:))
- [case none](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/none)
- [case single(EnvironmentResource)](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/single(_:))
- [ImageBasedLightComponent.Source](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum)

#### Enumeration Cases

- [case blend(EnvironmentResource, EnvironmentResource, Float)](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/blend(_:_:_:))
- [case none](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/none)
- [case single(EnvironmentResource)](/documentation/realitykit/imagebasedlightcomponent/source-swift.enum/single(_:))
- [ImageBasedLightReceiverComponent](/documentation/realitykit/imagebasedlightreceivercomponent)

#### Initializers

- [init(imageBasedLight: Entity)](/documentation/realitykit/imagebasedlightreceivercomponent/init(imagebasedlight:))

#### Instance Properties

- [var imageBasedLight: Entity](/documentation/realitykit/imagebasedlightreceivercomponent/imagebasedlight)

### General shadows

- [GroundingShadowComponent](/documentation/realitykit/groundingshadowcomponent)

#### Initializers

- [init(castsShadow: Bool)](/documentation/realitykit/groundingshadowcomponent/init(castsshadow:))
- [init(castsShadow: Bool, receivesShadow: Bool)](/documentation/realitykit/groundingshadowcomponent/init(castsshadow:receivesshadow:))
- [init(castsShadow: Bool, receivesShadow: Bool, fadeBehaviorNearPhysicalObjects: GroundingShadowComponent.FadeBehaviorNearPhysicalObjects)](/documentation/realitykit/groundingshadowcomponent/init(castsshadow:receivesshadow:fadebehaviornearphysicalobjects:))

#### Instance Properties

- [var castsShadow: Bool](/documentation/realitykit/groundingshadowcomponent/castsshadow)
- [var fadeBehaviorNearPhysicalObjects: GroundingShadowComponent.FadeBehaviorNearPhysicalObjects](/documentation/realitykit/groundingshadowcomponent/fadebehaviornearphysicalobjects-swift.property)
- [var receivesShadow: Bool](/documentation/realitykit/groundingshadowcomponent/receivesshadow)

#### Enumerations

- [GroundingShadowComponent.FadeBehaviorNearPhysicalObjects](/documentation/realitykit/groundingshadowcomponent/fadebehaviornearphysicalobjects-swift.enum)

##### Enumeration Cases

- [case constant](/documentation/realitykit/groundingshadowcomponent/fadebehaviornearphysicalobjects-swift.enum/constant)
- [case `default`](/documentation/realitykit/groundingshadowcomponent/fadebehaviornearphysicalobjects-swift.enum/default)
- [case fade](/documentation/realitykit/groundingshadowcomponent/fadebehaviornearphysicalobjects-swift.enum/fade)
- [DynamicLightShadowComponent](/documentation/realitykit/dynamiclightshadowcomponent)

#### Initializers

- [init(castsShadow: Bool)](/documentation/realitykit/dynamiclightshadowcomponent/init(castsshadow:))

#### Instance Properties

- [var castsShadow: Bool](/documentation/realitykit/dynamiclightshadowcomponent/castsshadow)

### Environment

- [EnvironmentResource](/documentation/realitykit/environmentresource)

#### Loading the resource

- [convenience init(named: String, in: Bundle?) async throws](/documentation/realitykit/environmentresource/init(named:in:))
- [convenience init(equirectangular: CGImage, withName: String?) async throws](/documentation/realitykit/environmentresource/init(equirectangular:withname:)-8o2v7)
- [convenience init(equirectangular: CGImage, withName: String?) async throws](/documentation/realitykit/environmentresource/init(equirectangular:withname:)-8o2v7)
- [convenience init(cube: TextureResource, options: EnvironmentResource.CreateOptions) async throws](/documentation/realitykit/environmentresource/init(cube:options:)-9j9rn)
- [convenience init(cube: TextureResource, options: EnvironmentResource.CreateOptions) async throws](/documentation/realitykit/environmentresource/init(cube:options:)-9j9rn)
- [static func load(named: String, in: Bundle?) throws -> EnvironmentResource](/documentation/realitykit/environmentresource/load(named:in:))

#### Configuring the resource creation

- [EnvironmentResource.CreateOptions](/documentation/realitykit/environmentresource/createoptions)

##### Creating the options

- [init(samplingQuality: EnvironmentResource.CreateOptions.SamplingQuality, specularCubeDimension: Int?, compression: EnvironmentResource.Compression)](/documentation/realitykit/environmentresource/createoptions/init(samplingquality:specularcubedimension:compression:))

##### Specifying the quality

- [EnvironmentResource.CreateOptions.SamplingQuality](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.enum)

###### Sampling qualities

- [case fast](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.enum/fast)
- [case normal](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.enum/normal)
- [case high](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.enum/high)
- [case veryHigh](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.enum/veryhigh)

##### Accessing the option properties

- [var compression: EnvironmentResource.Compression](/documentation/realitykit/environmentresource/createoptions/compression)
- [var samplingQuality: EnvironmentResource.CreateOptions.SamplingQuality](/documentation/realitykit/environmentresource/createoptions/samplingquality-swift.property)
- [var specularCubeDimension: Int?](/documentation/realitykit/environmentresource/createoptions/specularcubedimension)
- [EnvironmentResource.Compression](/documentation/realitykit/environmentresource/compression)

#### Accessing resource data

- [var skybox: TextureResource](/documentation/realitykit/environmentresource/skybox)

#### Deprecated

- [static func generate(fromEquirectangular: CGImage, withName: String?) throws -> EnvironmentResource](/documentation/realitykit/environmentresource/generate(fromequirectangular:withname:)-3wtpe)
- [static func generate(fromEquirectangular: CGImage, withName: String?) async throws -> EnvironmentResource](/documentation/realitykit/environmentresource/generate(fromequirectangular:withname:)-6mxsi)
- [static func loadAsync(named: String, in: Bundle?) -> LoadRequest<EnvironmentResource>](/documentation/realitykit/environmentresource/loadasync(named:in:))

#### Initializers

- [convenience(cube:options:)](/documentation/realitykit/environmentresource/init(cube:options:))
- [convenience(equirectangular:withName:)](/documentation/realitykit/environmentresource/init(equirectangular:withname:))

#### Type Methods

- [static generate(fromEquirectangular:withName:)](/documentation/realitykit/environmentresource/generate(fromequirectangular:withname:))
- [EnvironmentLightingConfigurationComponent](/documentation/realitykit/environmentlightingconfigurationcomponent)

#### Creating an environment-lighting configuration component

- [init(environmentLightingWeight: Float)](/documentation/realitykit/environmentlightingconfigurationcomponent/init(environmentlightingweight:))

#### Scaling the environment-lighting contribution

- [var environmentLightingWeight: Float](/documentation/realitykit/environmentlightingconfigurationcomponent/environmentlightingweight)

#### Operators

- [static func == (EnvironmentLightingConfigurationComponent, EnvironmentLightingConfigurationComponent) -> Bool](/documentation/realitykit/environmentlightingconfigurationcomponent/==(_:_:))
- [VirtualEnvironmentProbeComponent](/documentation/realitykit/virtualenvironmentprobecomponent)

#### Structures

- [VirtualEnvironmentProbeComponent.Probe](/documentation/realitykit/virtualenvironmentprobecomponent/probe)

##### Initializers

- [init(environment: EnvironmentResource, intensityExponent: Float)](/documentation/realitykit/virtualenvironmentprobecomponent/probe/init(environment:intensityexponent:))

##### Instance Properties

- [var environment: EnvironmentResource](/documentation/realitykit/virtualenvironmentprobecomponent/probe/environment)
- [var intensityExponent: Float](/documentation/realitykit/virtualenvironmentprobecomponent/probe/intensityexponent)

#### Initializers

- [init(source: VirtualEnvironmentProbeComponent.Source)](/documentation/realitykit/virtualenvironmentprobecomponent/init(source:))

#### Instance Properties

- [var source: VirtualEnvironmentProbeComponent.Source](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.property)

#### Enumerations

- [VirtualEnvironmentProbeComponent.Source](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum)

##### Enumeration Cases

- [case blend(from: VirtualEnvironmentProbeComponent.Probe, to: VirtualEnvironmentProbeComponent.Probe, t: Float)](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/blend(from:to:t:))
- [case none](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/none)
- [case single(VirtualEnvironmentProbeComponent.Probe)](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/single(_:))
- [VirtualEnvironmentProbeComponent.Probe](/documentation/realitykit/virtualenvironmentprobecomponent/probe)

#### Initializers

- [init(environment: EnvironmentResource, intensityExponent: Float)](/documentation/realitykit/virtualenvironmentprobecomponent/probe/init(environment:intensityexponent:))

#### Instance Properties

- [var environment: EnvironmentResource](/documentation/realitykit/virtualenvironmentprobecomponent/probe/environment)
- [var intensityExponent: Float](/documentation/realitykit/virtualenvironmentprobecomponent/probe/intensityexponent)
- [VirtualEnvironmentProbeComponent.Source](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum)

#### Enumeration Cases

- [case blend(from: VirtualEnvironmentProbeComponent.Probe, to: VirtualEnvironmentProbeComponent.Probe, t: Float)](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/blend(from:to:t:))
- [case none](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/none)
- [case single(VirtualEnvironmentProbeComponent.Probe)](/documentation/realitykit/virtualenvironmentprobecomponent/source-swift.enum/single(_:))

### Entity compliance

- [HasPerspectiveCamera](/documentation/realitykit/hasperspectivecamera)

#### Getting the camera

- [var camera: PerspectiveCameraComponent](/documentation/realitykit/hasperspectivecamera/camera)
- [PointLight](/documentation/realitykit/pointlight)

#### Creating a point light

- [init()](/documentation/realitykit/pointlight/init())
- [HasPointLight](/documentation/realitykit/haspointlight)

#### Getting the point light component

- [var light: PointLightComponent](/documentation/realitykit/haspointlight/light)
- [SpotLight](/documentation/realitykit/spotlight)

#### Creating a spotlight

- [init()](/documentation/realitykit/spotlight/init())
- [HasSpotLight](/documentation/realitykit/hasspotlight)

#### Getting the spot light

- [var light: SpotLightComponent](/documentation/realitykit/hasspotlight/light)

#### Specifying the shadow

- [var shadow: SpotLightComponent.Shadow?](/documentation/realitykit/hasspotlight/shadow)
- [DirectionalLight](/documentation/realitykit/directionallight)

#### Creating a directional light

- [init()](/documentation/realitykit/directionallight/init())
- [HasDirectionalLight](/documentation/realitykit/hasdirectionallight)

#### Getting the directional light

- [var light: DirectionalLightComponent](/documentation/realitykit/hasdirectionallight/light)

#### Specifying the shadow

- [var shadow: DirectionalLightComponent.Shadow?](/documentation/realitykit/hasdirectionallight/shadow)
- [Content synchronization](/documentation/realitykit/scene-content-content-synchronization)

### Entity ownership synchronization

- [SynchronizationService](/documentation/realitykit/synchronizationservice)

#### Managing ownership

- [func owner(of: Entity) -> (any SynchronizationPeerID)?](/documentation/realitykit/synchronizationservice/owner(of:))
- [func giveOwnership(of: Entity, toPeer: any SynchronizationPeerID) -> Bool](/documentation/realitykit/synchronizationservice/giveownership(of:topeer:))

#### Finding an entity

- [func entity(for: Self.Identifier) -> Entity?](/documentation/realitykit/synchronizationservice/entity(for:))

#### Type Aliases

- [SynchronizationService.Identifier](/documentation/realitykit/synchronizationservice/identifier)
- [SynchronizationService.Identifier](/documentation/realitykit/synchronizationservice/identifier)
- [SynchronizationPeerID](/documentation/realitykit/synchronizationpeerid)
- [SynchronizationComponent](/documentation/realitykit/synchronizationcomponent)

#### Creating a synchronization component

- [init()](/documentation/realitykit/synchronizationcomponent/init())

#### Identifying a synchronization component

- [var identifier: UInt64](/documentation/realitykit/synchronizationcomponent/identifier)

#### Managing ownership

- [var isOwner: Bool](/documentation/realitykit/synchronizationcomponent/isowner)
- [var ownershipTransferMode: SynchronizationComponent.OwnershipTransferMode](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.property)

#### Operators

- [static func == (SynchronizationComponent, SynchronizationComponent) -> Bool](/documentation/realitykit/synchronizationcomponent/==(_:_:))

#### Enumerations

- [SynchronizationComponent.OwnershipTransferCompletionResult](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult)

##### Ownership transfer completion results

- [case granted](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/granted)
- [case timedOut](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/timedout)
- [SynchronizationComponent.OwnershipTransferMode](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum)

##### Ownership transfer modes

- [case autoAccept](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/autoaccept)
- [case manual](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/manual)
- [SynchronizationComponent.OwnershipTransferMode](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum)

#### Ownership transfer modes

- [case autoAccept](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/autoaccept)
- [case manual](/documentation/realitykit/synchronizationcomponent/ownershiptransfermode-swift.enum/manual)
- [SynchronizationComponent.OwnershipTransferCompletionResult](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult)

#### Ownership transfer completion results

- [case granted](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/granted)
- [case timedOut](/documentation/realitykit/synchronizationcomponent/ownershiptransfercompletionresult/timedout)
- [SynchronizationEvents](/documentation/realitykit/synchronizationevents)

#### Detecting ownership updates

- [SynchronizationEvents.OwnershipChanged](/documentation/realitykit/synchronizationevents/ownershipchanged)

##### Getting the involved parties

- [let entity: Entity](/documentation/realitykit/synchronizationevents/ownershipchanged/entity)
- [let newOwner: (any SynchronizationPeerID)?](/documentation/realitykit/synchronizationevents/ownershipchanged/newowner)
- [SynchronizationEvents.OwnershipRequest](/documentation/realitykit/synchronizationevents/ownershiprequest)

##### Getting the involved parties

- [let entity: Entity](/documentation/realitykit/synchronizationevents/ownershiprequest/entity)
- [let requester: any SynchronizationPeerID](/documentation/realitykit/synchronizationevents/ownershiprequest/requester)

##### Accepting the request

- [let accept: () -> Void](/documentation/realitykit/synchronizationevents/ownershiprequest/accept)
- [HasSynchronization](/documentation/realitykit/hassynchronization)

#### Accessing the component

- [var synchronization: SynchronizationComponent?](/documentation/realitykit/hassynchronization/synchronization)

#### Managing ownership

- [var isOwner: Bool](/documentation/realitykit/hassynchronization/isowner)
- [func requestOwnership(timeout: TimeInterval, (SynchronizationComponent.OwnershipTransferCompletionResult) -> Void)](/documentation/realitykit/hassynchronization/requestownership(timeout:_:))

#### Making local changes

- [func withUnsynchronized(() -> Void)](/documentation/realitykit/hassynchronization/withunsynchronized(_:))

### Multipeer synchronization

- [Loading remote assets in multiplayer apps](/documentation/realitykit/loading-remote-assets)
- [MultipeerConnectivityService](/documentation/realitykit/multipeerconnectivityservice)

#### Creating a connectivity service

- [init(session: MCSession) throws](/documentation/realitykit/multipeerconnectivityservice/init(session:))

#### Getting the session

- [let session: MCSession](/documentation/realitykit/multipeerconnectivityservice/session)

#### Managing ownership

- [func owner(of: Entity) -> (any SynchronizationPeerID)?](/documentation/realitykit/multipeerconnectivityservice/owner(of:))
- [func giveOwnership(of: Entity, toPeer: any SynchronizationPeerID) -> Bool](/documentation/realitykit/multipeerconnectivityservice/giveownership(of:topeer:))

#### Finding an entity

- [func entity(for: MultipeerConnectivityService.Identifier) -> Entity?](/documentation/realitykit/multipeerconnectivityservice/entity(for:))

#### Pausing and resuming

- [func stopSync()](/documentation/realitykit/multipeerconnectivityservice/stopsync())
- [func startSync()](/documentation/realitykit/multipeerconnectivityservice/startsync())

#### Configuring the session

- [func setHandshake(count: UInt32, timeoutMs: UInt32)](/documentation/realitykit/multipeerconnectivityservice/sethandshake(count:timeoutms:))
- [NetworkCompatibilityToken](/documentation/realitykit/networkcompatibilitytoken)

#### Retrieving tokens

- [static let local: NetworkCompatibilityToken](/documentation/realitykit/networkcompatibilitytoken/local)

#### Checking compatibility

- [func compatibilityWith(NetworkCompatibilityToken) -> NetworkCompatibilityToken.Compatibility](/documentation/realitykit/networkcompatibilitytoken/compatibilitywith(_:))

#### Serializing tokens

- [init(from: any Decoder) throws](/documentation/realitykit/networkcompatibilitytoken/init(from:))
- [func encode(to: any Encoder) throws](/documentation/realitykit/networkcompatibilitytoken/encode(to:))

#### Enumerations

- [NetworkCompatibilityToken.Compatibility](/documentation/realitykit/networkcompatibilitytoken/compatibility)

##### Compatibility indicators

- [case compatible](/documentation/realitykit/networkcompatibilitytoken/compatibility/compatible)
- [case sessionProtocolVersionMismatch](/documentation/realitykit/networkcompatibilitytoken/compatibility/sessionprotocolversionmismatch)
- [NetworkCompatibilityToken.Compatibility](/documentation/realitykit/networkcompatibilitytoken/compatibility)

#### Compatibility indicators

- [case compatible](/documentation/realitykit/networkcompatibilitytoken/compatibility/compatible)
- [case sessionProtocolVersionMismatch](/documentation/realitykit/networkcompatibilitytoken/compatibility/sessionprotocolversionmismatch)
- [TransientComponent](/documentation/realitykit/transientcomponent)
- [Audio](/documentation/realitykit/scene-content-audio)

### Audio source components

- [Creating a Spaceship game](/documentation/realitykit/creating-a-spaceship-game)
- [SpatialAudioComponent](/documentation/realitykit/spatialaudiocomponent)

#### Initializers

- [init(gain: Audio.Decibel, directLevel: Audio.Decibel, reverbLevel: Audio.Decibel, directivity: Audio.Directivity)](/documentation/realitykit/spatialaudiocomponent/init(gain:directlevel:reverblevel:directivity:))
- [init(gain: Audio.Decibel, directLevel: Audio.Decibel, reverbLevel: Audio.Decibel, directivity: Audio.Directivity, distanceAttenuation: Audio.DistanceAttenuation)](/documentation/realitykit/spatialaudiocomponent/init(gain:directlevel:reverblevel:directivity:distanceattenuation:))

#### Instance Properties

- [var directLevel: Audio.Decibel](/documentation/realitykit/spatialaudiocomponent/directlevel)
- [var directivity: Audio.Directivity](/documentation/realitykit/spatialaudiocomponent/directivity)
- [var distanceAttenuation: Audio.DistanceAttenuation](/documentation/realitykit/spatialaudiocomponent/distanceattenuation)
- [var gain: Audio.Decibel](/documentation/realitykit/spatialaudiocomponent/gain)
- [var reverbLevel: Audio.Decibel](/documentation/realitykit/spatialaudiocomponent/reverblevel)
- [AmbientAudioComponent](/documentation/realitykit/ambientaudiocomponent)

#### Initializers

- [init(gain: Audio.Decibel)](/documentation/realitykit/ambientaudiocomponent/init(gain:))

#### Instance Properties

- [var gain: Audio.Decibel](/documentation/realitykit/ambientaudiocomponent/gain)
- [ChannelAudioComponent](/documentation/realitykit/channelaudiocomponent)

#### Initializers

- [init(gain: Audio.Decibel)](/documentation/realitykit/channelaudiocomponent/init(gain:))

#### Instance Properties

- [var gain: Audio.Decibel](/documentation/realitykit/channelaudiocomponent/gain)

### Playback controllers

- [AudioPlaybackController](/documentation/realitykit/audioplaybackcontroller)

#### Managing the resource

- [let resource: AudioResource](/documentation/realitykit/audioplaybackcontroller/resource)

#### Setting the volume

- [var gain: AudioPlaybackController.Decibel](/documentation/realitykit/audioplaybackcontroller/gain)
- [func fade(to: AudioPlaybackController.Decibel, duration: TimeInterval)](/documentation/realitykit/audioplaybackcontroller/fade(to:duration:))

#### Setting the speed

- [var speed: Double](/documentation/realitykit/audioplaybackcontroller/speed)

#### Setting the reverb

- [var reverbSendLevel: AudioPlaybackController.Decibel](/documentation/realitykit/audioplaybackcontroller/reverbsendlevel)

#### Starting and stopping audio playback

- [func play()](/documentation/realitykit/audioplaybackcontroller/play())
- [func pause()](/documentation/realitykit/audioplaybackcontroller/pause())
- [func stop()](/documentation/realitykit/audioplaybackcontroller/stop())
- [var isPlaying: Bool](/documentation/realitykit/audioplaybackcontroller/isplaying)

#### Handling completion

- [var completionHandler: (() -> Void)?](/documentation/realitykit/audioplaybackcontroller/completionhandler)

#### Finding the associated entity

- [var entity: Entity?](/documentation/realitykit/audioplaybackcontroller/entity)

#### Instance Methods

- [func seek(to: Duration)](/documentation/realitykit/audioplaybackcontroller/seek(to:))

#### Type Aliases

- [AudioPlaybackController.Decibel](/documentation/realitykit/audioplaybackcontroller/decibel)
- [AudioGeneratorController](/documentation/realitykit/audiogeneratorcontroller)

#### Instance Properties

- [let configuration: AudioGeneratorConfiguration](/documentation/realitykit/audiogeneratorcontroller/configuration)
- [var entity: Entity?](/documentation/realitykit/audiogeneratorcontroller/entity)
- [var gain: Audio.Decibel](/documentation/realitykit/audiogeneratorcontroller/gain)
- [var isPlaying: Bool](/documentation/realitykit/audiogeneratorcontroller/isplaying)

#### Instance Methods

- [func play()](/documentation/realitykit/audiogeneratorcontroller/play())
- [func stop()](/documentation/realitykit/audiogeneratorcontroller/stop())
- [AudioGeneratorConfiguration](/documentation/realitykit/audiogeneratorconfiguration)

#### Initializers

- [init(layoutTag: AudioChannelLayoutTag, mixGroupName: String?)](/documentation/realitykit/audiogeneratorconfiguration/init(layouttag:mixgroupname:))

#### Instance Properties

- [var layoutTag: AudioChannelLayoutTag](/documentation/realitykit/audiogeneratorconfiguration/layouttag)
- [var mixGroupName: String?](/documentation/realitykit/audiogeneratorconfiguration/mixgroupname)
- [AudioEvents](/documentation/realitykit/audioevents)

#### Recognizing playback completion

- [AudioEvents.PlaybackCompleted](/documentation/realitykit/audioevents/playbackcompleted)

##### Instance Properties

- [var playbackController: AudioPlaybackController](/documentation/realitykit/audioevents/playbackcompleted/playbackcontroller)
- [PlayAudioAction](/documentation/realitykit/playaudioaction)

#### Initializers

- [init(targetEntity: ActionEntityResolution, audioResourceName: String, gain: Audio.Decibel, useControlledPlayback: Bool)](/documentation/realitykit/playaudioaction/init(targetentity:audioresourcename:gain:usecontrolledplayback:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/playaudioaction/animatedvaluetype)
- [var audioResourceName: String](/documentation/realitykit/playaudioaction/audioresourcename)
- [var gain: Audio.Decibel](/documentation/realitykit/playaudioaction/gain)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/playaudioaction/targetentity)
- [var useControlledPlayback: Bool](/documentation/realitykit/playaudioaction/usecontrolledplayback)

### Audio resources

- [AudioFileResource](/documentation/realitykit/audiofileresource)

#### Loading audio from a bundle

- [convenience init(named: String, from: String, in: Bundle?) async throws](/documentation/realitykit/audiofileresource/init(named:from:in:))
- [convenience init(named: String, in: Bundle?, configuration: AudioFileResource.Configuration) async throws](/documentation/realitykit/audiofileresource/init(named:in:configuration:))

#### Loading audio from a URL

- [convenience init(contentsOf: URL, withName: String?, configuration: AudioFileResource.Configuration) async throws](/documentation/realitykit/audiofileresource/init(contentsof:withname:configuration:))

#### Describing the resource

- [let configuration: AudioFileResource.Configuration](/documentation/realitykit/audiofileresource/configuration-swift.property)
- [var duration: Duration](/documentation/realitykit/audiofileresource/duration)
- [let name: String](/documentation/realitykit/audiofileresource/name)

#### Supporting types

- [AudioFileResource.Configuration](/documentation/realitykit/audiofileresource/configuration-swift.struct)

##### Creating a configuration for an audio file resource

- [init(loadingStrategy: AudioFileResource.LoadingStrategy, shouldLoop: Bool, shouldRandomizeStartTime: Bool, normalization: AudioResource.Normalization?, calibration: AudioResource.Calibration?, mixGroupName: String?)](/documentation/realitykit/audiofileresource/configuration-swift.struct/init(loadingstrategy:shouldloop:shouldrandomizestarttime:normalization:calibration:mixgroupname:))

##### Configuring the loading optimization strategy

- [var loadingStrategy: AudioFileResource.LoadingStrategy](/documentation/realitykit/audiofileresource/configuration-swift.struct/loadingstrategy)

##### Controlling the volume

- [var normalization: AudioResource.Normalization?](/documentation/realitykit/audiofileresource/configuration-swift.struct/normalization)
- [var calibration: AudioResource.Calibration?](/documentation/realitykit/audiofileresource/configuration-swift.struct/calibration)

##### Customizing the playback

- [var shouldRandomizeStartTime: Bool](/documentation/realitykit/audiofileresource/configuration-swift.struct/shouldrandomizestarttime)
- [var shouldLoop: Bool](/documentation/realitykit/audiofileresource/configuration-swift.struct/shouldloop)

##### Assigning an audio resource to a mix group

- [var mixGroupName: String?](/documentation/realitykit/audiofileresource/configuration-swift.struct/mixgroupname)
- [AudioFileResource.LoadingStrategy](/documentation/realitykit/audiofileresource/loadingstrategy-swift.enum)

##### Specifying a loading strategy

- [case preload](/documentation/realitykit/audiofileresource/loadingstrategy-swift.enum/preload)
- [case stream](/documentation/realitykit/audiofileresource/loadingstrategy-swift.enum/stream)

#### Deprecated

- [static func load(named: String, in: Bundle?, inputMode: AudioResource.InputMode, loadingStrategy: AudioFileResource.LoadingStrategy, shouldLoop: Bool) throws -> AudioFileResource](/documentation/realitykit/audiofileresource/load(named:in:inputmode:loadingstrategy:shouldloop:))
- [static func loadAsync(named: String, in: Bundle?, inputMode: AudioResource.InputMode, loadingStrategy: AudioFileResource.LoadingStrategy, shouldLoop: Bool) -> LoadRequest<AudioFileResource>](/documentation/realitykit/audiofileresource/loadasync(named:in:inputmode:loadingstrategy:shouldloop:))
- [static func load(contentsOf: URL, withName: String?, inputMode: AudioResource.InputMode, loadingStrategy: AudioFileResource.LoadingStrategy, shouldLoop: Bool) throws -> AudioFileResource](/documentation/realitykit/audiofileresource/load(contentsof:withname:inputmode:loadingstrategy:shouldloop:))
- [static func loadAsync(contentsOf: URL, withName: String?, inputMode: AudioResource.InputMode, loadingStrategy: AudioFileResource.LoadingStrategy, shouldLoop: Bool) -> LoadRequest<AudioFileResource>](/documentation/realitykit/audiofileresource/loadasync(contentsof:withname:inputmode:loadingstrategy:shouldloop:))
- [var loadingStrategy: AudioFileResource.LoadingStrategy](/documentation/realitykit/audiofileresource/loadingstrategy-swift.property)
- [var shouldLoop: Bool](/documentation/realitykit/audiofileresource/shouldloop)

#### Operators

- [static func == (AudioFileResource, AudioFileResource) -> Bool](/documentation/realitykit/audiofileresource/==(_:_:))

#### Type Methods

- [static func load(contentsOf: URL, withName: String?, configuration: AudioFileResource.Configuration) throws -> AudioFileResource](/documentation/realitykit/audiofileresource/load(contentsof:withname:configuration:))
- [static func load(named: String, from: String, in: Bundle?) throws -> AudioFileResource](/documentation/realitykit/audiofileresource/load(named:from:in:))
- [static func load(named: String, in: Bundle?, configuration: AudioFileResource.Configuration) throws -> AudioFileResource](/documentation/realitykit/audiofileresource/load(named:in:configuration:))
- [AudioFileGroupResource](/documentation/realitykit/audiofilegroupresource)

#### Creating a resource

- [init([AudioFileResource]) throws](/documentation/realitykit/audiofilegroupresource/init(_:))
- [convenience init(named: String, from: String, in: Bundle) async throws](/documentation/realitykit/audiofilegroupresource/init(named:from:in:))
- [static func load(named: String, from: String, in: Bundle?) throws -> AudioFileGroupResource](/documentation/realitykit/audiofilegroupresource/load(named:from:in:))

#### Working with the resource contents

- [let resources: [AudioFileResource]](/documentation/realitykit/audiofilegroupresource/resources)

#### Operators

- [static func == (AudioFileGroupResource, AudioFileGroupResource) -> Bool](/documentation/realitykit/audiofilegroupresource/==(_:_:))
- [AudioBufferResource](/documentation/realitykit/audiobufferresource)

#### Creating an audio buffer resource

- [init(buffer: AVAudioBuffer, configuration: AudioBufferResource.Configuration) throws](/documentation/realitykit/audiobufferresource/init(buffer:configuration:))

#### Describing the resource

- [let configuration: AudioBufferResource.Configuration](/documentation/realitykit/audiobufferresource/configuration-swift.property)
- [var duration: Duration](/documentation/realitykit/audiobufferresource/duration)

#### Supporting types

- [AudioBufferResource.Configuration](/documentation/realitykit/audiobufferresource/configuration-swift.struct)

##### Initializers

- [init(shouldLoop: Bool, shouldRandomizeStartTime: Bool, normalization: AudioResource.Normalization?, calibration: AudioResource.Calibration?, mixGroupName: String?)](/documentation/realitykit/audiobufferresource/configuration-swift.struct/init(shouldloop:shouldrandomizestarttime:normalization:calibration:mixgroupname:))

##### Instance Properties

- [var calibration: AudioResource.Calibration?](/documentation/realitykit/audiobufferresource/configuration-swift.struct/calibration)
- [var mixGroupName: String?](/documentation/realitykit/audiobufferresource/configuration-swift.struct/mixgroupname)
- [var normalization: AudioResource.Normalization?](/documentation/realitykit/audiobufferresource/configuration-swift.struct/normalization)
- [var shouldLoop: Bool](/documentation/realitykit/audiobufferresource/configuration-swift.struct/shouldloop)
- [var shouldRandomizeStartTime: Bool](/documentation/realitykit/audiobufferresource/configuration-swift.struct/shouldrandomizestarttime)

#### Deprecated

- [init(buffer: AVAudioBuffer, inputMode: AudioResource.InputMode, shouldLoop: Bool) throws](/documentation/realitykit/audiobufferresource/init(buffer:inputmode:shouldloop:))
- [var shouldLoop: Bool](/documentation/realitykit/audiobufferresource/shouldloop)
- [AudioLibraryComponent](/documentation/realitykit/audiolibrarycomponent)

#### Creating an audio library component

- [init(resources: [String : AudioResource])](/documentation/realitykit/audiolibrarycomponent/init(resources:))

#### Accessing audio resources

- [var resources: [String : AudioResource]](/documentation/realitykit/audiolibrarycomponent/resources)
- [AudioResource](/documentation/realitykit/audioresource)

#### Deprecated

- [var inputMode: AudioResource.InputMode](/documentation/realitykit/audioresource/inputmode-swift.property)
- [AudioResource.InputMode](/documentation/realitykit/audioresource/inputmode-swift.enum)

##### Input modes

- [case nonSpatial](/documentation/realitykit/audioresource/inputmode-swift.enum/nonspatial)
- [case spatial](/documentation/realitykit/audioresource/inputmode-swift.enum/spatial)
- [case ambient](/documentation/realitykit/audioresource/inputmode-swift.enum/ambient)

#### Structures

- [AudioResource.Calibration](/documentation/realitykit/audioresource/calibration)

##### Type Methods

- [static func absolute(dBSPL: Audio.Decibel) -> AudioResource.Calibration](/documentation/realitykit/audioresource/calibration/absolute(dbspl:))
- [static func relative(dBSPL: Audio.Decibel) -> AudioResource.Calibration](/documentation/realitykit/audioresource/calibration/relative(dbspl:))
- [AudioResource.Normalization](/documentation/realitykit/audioresource/normalization)

##### Type Properties

- [static let dynamic: AudioResource.Normalization](/documentation/realitykit/audioresource/normalization/dynamic)
- [AudioResource.Calibration](/documentation/realitykit/audioresource/calibration)

#### Type Methods

- [static func absolute(dBSPL: Audio.Decibel) -> AudioResource.Calibration](/documentation/realitykit/audioresource/calibration/absolute(dbspl:))
- [static func relative(dBSPL: Audio.Decibel) -> AudioResource.Calibration](/documentation/realitykit/audioresource/calibration/relative(dbspl:))
- [AudioResource.Normalization](/documentation/realitykit/audioresource/normalization)

#### Type Properties

- [static let dynamic: AudioResource.Normalization](/documentation/realitykit/audioresource/normalization/dynamic)

### Reverb

- [Reverb](/documentation/realitykit/reverb)

#### Structures

- [Reverb.Preset](/documentation/realitykit/reverb/preset)

##### Type Properties

- [static let concertHall: Reverb.Preset](/documentation/realitykit/reverb/preset/concerthall)
- [static let largeRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/largeroom)
- [static let largeRoomTreated: Reverb.Preset](/documentation/realitykit/reverb/preset/largeroomtreated)
- [static let mediumRoomDry: Reverb.Preset](/documentation/realitykit/reverb/preset/mediumroomdry)
- [static let mediumRoomTreated: Reverb.Preset](/documentation/realitykit/reverb/preset/mediumroomtreated)
- [static let outside: Reverb.Preset](/documentation/realitykit/reverb/preset/outside)
- [static let smallRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/smallroom)
- [static let smallRoomBright: Reverb.Preset](/documentation/realitykit/reverb/preset/smallroombright)
- [static let veryLargeRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/verylargeroom)
- [static let verySmallRoomBright: Reverb.Preset](/documentation/realitykit/reverb/preset/verysmallroombright)

#### Type Properties

- [static let anechoic: Reverb](/documentation/realitykit/reverb/anechoic)

#### Type Methods

- [static func preset(Reverb.Preset) -> Reverb](/documentation/realitykit/reverb/preset(_:))
- [Reverb.Preset](/documentation/realitykit/reverb/preset)

#### Type Properties

- [static let concertHall: Reverb.Preset](/documentation/realitykit/reverb/preset/concerthall)
- [static let largeRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/largeroom)
- [static let largeRoomTreated: Reverb.Preset](/documentation/realitykit/reverb/preset/largeroomtreated)
- [static let mediumRoomDry: Reverb.Preset](/documentation/realitykit/reverb/preset/mediumroomdry)
- [static let mediumRoomTreated: Reverb.Preset](/documentation/realitykit/reverb/preset/mediumroomtreated)
- [static let outside: Reverb.Preset](/documentation/realitykit/reverb/preset/outside)
- [static let smallRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/smallroom)
- [static let smallRoomBright: Reverb.Preset](/documentation/realitykit/reverb/preset/smallroombright)
- [static let veryLargeRoom: Reverb.Preset](/documentation/realitykit/reverb/preset/verylargeroom)
- [static let verySmallRoomBright: Reverb.Preset](/documentation/realitykit/reverb/preset/verysmallroombright)
- [ReverbComponent](/documentation/realitykit/reverbcomponent)

#### Initializers

- [init(reverb: Reverb)](/documentation/realitykit/reverbcomponent/init(reverb:))

#### Instance Properties

- [var reverb: Reverb](/documentation/realitykit/reverbcomponent/reverb)

### Audio mixing

- [AudioMixGroup](/documentation/realitykit/audiomixgroup)

#### Initializers

- [init(name: String)](/documentation/realitykit/audiomixgroup/init(name:))

#### Instance Properties

- [var gain: Audio.Decibel](/documentation/realitykit/audiomixgroup/gain)
- [var isMuted: Bool](/documentation/realitykit/audiomixgroup/ismuted)
- [let name: String](/documentation/realitykit/audiomixgroup/name)
- [var speed: Double](/documentation/realitykit/audiomixgroup/speed)

#### Instance Methods

- [func fade(to: Audio.Decibel, duration: TimeInterval)](/documentation/realitykit/audiomixgroup/fade(to:duration:))
- [AudioMixGroupsComponent](/documentation/realitykit/audiomixgroupscomponent)

#### Initializers

- [init(mixGroups: [AudioMixGroup])](/documentation/realitykit/audiomixgroupscomponent/init(mixgroups:))

#### Instance Methods

- [func mixGroup(named: String) -> AudioMixGroup?](/documentation/realitykit/audiomixgroupscomponent/mixgroup(named:))
- [func remove(named: String)](/documentation/realitykit/audiomixgroupscomponent/remove(named:))
- [func set(AudioMixGroup)](/documentation/realitykit/audiomixgroupscomponent/set(_:))

### Audio types

- [Audio](/documentation/realitykit/audio)

#### Type Aliases

- [Audio.Decibel](/documentation/realitykit/audio/decibel)
- [Audio.GeneratorRenderHandler](/documentation/realitykit/audio/generatorrenderhandler)

#### Enumerations

- [Audio.Directivity](/documentation/realitykit/audio/directivity)

##### Enumeration Cases

- [case beam(focus: Double)](/documentation/realitykit/audio/directivity/beam(focus:))
- [Audio.DistanceAttenuation](/documentation/realitykit/audio/distanceattenuation)

##### Enumeration Cases

- [case rolloff(factor: Double)](/documentation/realitykit/audio/distanceattenuation/rolloff(factor:))

##### Type Properties

- [static let `default`: Audio.DistanceAttenuation](/documentation/realitykit/audio/distanceattenuation/default)
- [Audio.Decibel](/documentation/realitykit/audio/decibel)
- [Audio.Directivity](/documentation/realitykit/audio/directivity)

#### Enumeration Cases

- [case beam(focus: Double)](/documentation/realitykit/audio/directivity/beam(focus:))
- [Audio.DistanceAttenuation](/documentation/realitykit/audio/distanceattenuation)

#### Enumeration Cases

- [case rolloff(factor: Double)](/documentation/realitykit/audio/distanceattenuation/rolloff(factor:))

#### Type Properties

- [static let `default`: Audio.DistanceAttenuation](/documentation/realitykit/audio/distanceattenuation/default)
- [Videos](/documentation/realitykit/scene-content-videos)

### Video player configurations

- [VideoPlayerComponent](/documentation/realitykit/videoplayercomponent)

#### Creating a video player component

- [init(avPlayer: AVPlayer)](/documentation/realitykit/videoplayercomponent/init(avplayer:))
- [init(videoRenderer: AVSampleBufferVideoRenderer)](/documentation/realitykit/videoplayercomponent/init(videorenderer:))

#### Configuring the video player

- [var isPassthroughTintingEnabled: Bool](/documentation/realitykit/videoplayercomponent/ispassthroughtintingenabled)
- [var desiredViewingMode: VideoPlaybackController.ViewingMode](/documentation/realitykit/videoplayercomponent/desiredviewingmode)

#### Accessing video player properties

- [var avPlayer: AVPlayer?](/documentation/realitykit/videoplayercomponent/avplayer)
- [var playerScreenSize: SIMD2<Float>](/documentation/realitykit/videoplayercomponent/playerscreensize)
- [var screenVideoDimension: SIMD2<Float>](/documentation/realitykit/videoplayercomponent/screenvideodimension)
- [var videoRenderer: AVSampleBufferVideoRenderer?](/documentation/realitykit/videoplayercomponent/videorenderer)
- [var viewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplayercomponent/viewingmode)

#### Playing immersive media

- [var desiredImmersiveViewingMode: VideoPlayerComponent.ImmersiveViewingMode](/documentation/realitykit/videoplayercomponent/desiredimmersiveviewingmode)
- [var immersiveViewingMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.property)

#### Instance Properties

- [var currentRenderingStatus: VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayercomponent/currentrenderingstatus)
- [var desiredSpatialVideoMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayercomponent/desiredspatialvideomode)
- [var spatialVideoMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayercomponent/spatialvideomode-swift.property)

#### Enumerations

- [VideoPlayerComponent.ImmersiveViewingMode](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum)

##### Enumeration Cases

- [case full](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/full)
- [case portal](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/portal)
- [case progressive](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/progressive)
- [VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayercomponent/renderingstatus)

##### Enumeration Cases

- [case loading](/documentation/realitykit/videoplayercomponent/renderingstatus/loading)
- [case ready](/documentation/realitykit/videoplayercomponent/renderingstatus/ready)
- [VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayercomponent/spatialvideomode-swift.enum)

##### Enumeration Cases

- [case screen](/documentation/realitykit/videoplayercomponent/spatialvideomode-swift.enum/screen)
- [case spatial](/documentation/realitykit/videoplayercomponent/spatialvideomode-swift.enum/spatial)
- [VideoPlayerComponent.VideoComfortMitigation](/documentation/realitykit/videoplayercomponent/videocomfortmitigation)

##### Enumeration Cases

- [case pause](/documentation/realitykit/videoplayercomponent/videocomfortmitigation/pause)
- [case play](/documentation/realitykit/videoplayercomponent/videocomfortmitigation/play)
- [case reduceImmersion](/documentation/realitykit/videoplayercomponent/videocomfortmitigation/reduceimmersion)
- [VideoPlayerComponent.ImmersiveViewingMode](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum)

#### Enumeration Cases

- [case full](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/full)
- [case portal](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/portal)
- [case progressive](/documentation/realitykit/videoplayercomponent/immersiveviewingmode-swift.enum/progressive)
- [VideoMaterial](/documentation/realitykit/videomaterial)

#### Creating a video material

- [init(avPlayer: AVPlayer)](/documentation/realitykit/videomaterial/init(avplayer:))

#### Controlling playback

- [var avPlayer: AVPlayer?](/documentation/realitykit/videomaterial/avplayer)
- [var controller: VideoPlaybackController](/documentation/realitykit/videomaterial/controller)

#### Initializers

- [init(videoRenderer: AVSampleBufferVideoRenderer)](/documentation/realitykit/videomaterial/init(videorenderer:))

#### Instance Properties

- [var faceCulling: VideoMaterial.FaceCulling](/documentation/realitykit/videomaterial/faceculling-swift.property)
- [var readsDepth: Bool](/documentation/realitykit/videomaterial/readsdepth)
- [var triangleFillMode: VideoMaterial.TriangleFillMode](/documentation/realitykit/videomaterial/trianglefillmode-swift.property)
- [var videoRenderer: AVSampleBufferVideoRenderer?](/documentation/realitykit/videomaterial/videorenderer)
- [var writesDepth: Bool](/documentation/realitykit/videomaterial/writesdepth)

#### Type Aliases

- [VideoMaterial.FaceCulling](/documentation/realitykit/videomaterial/faceculling-swift.typealias)
- [VideoMaterial.TriangleFillMode](/documentation/realitykit/videomaterial/trianglefillmode-swift.typealias)
- [VideoPlaybackController](/documentation/realitykit/videoplaybackcontroller)

#### Instance Properties

- [var audioInputMode: AudioResource.InputMode](/documentation/realitykit/videoplaybackcontroller/audioinputmode)
- [var currentImageSize: CGSize?](/documentation/realitykit/videoplaybackcontroller/currentimagesize)
- [var currentViewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplaybackcontroller/currentviewingmode)
- [var preferredViewingMode: VideoPlaybackController.ViewingMode](/documentation/realitykit/videoplaybackcontroller/preferredviewingmode)
- [var reverbSendLevel: AudioPlaybackController.Decibel](/documentation/realitykit/videoplaybackcontroller/reverbsendlevel)

#### Enumerations

- [VideoPlaybackController.ViewingMode](/documentation/realitykit/videoplaybackcontroller/viewingmode)

##### Enumeration Cases

- [case mono](/documentation/realitykit/videoplaybackcontroller/viewingmode/mono)
- [case stereo](/documentation/realitykit/videoplaybackcontroller/viewingmode/stereo)
- [VideoPlaybackController.ViewingMode](/documentation/realitykit/videoplaybackcontroller/viewingmode)

#### Enumeration Cases

- [case mono](/documentation/realitykit/videoplaybackcontroller/viewingmode/mono)
- [case stereo](/documentation/realitykit/videoplaybackcontroller/viewingmode/stereo)

### Content placement

- [DockingRegionComponent](/documentation/realitykit/dockingregioncomponent)

#### Creating a docking region component

- [init()](/documentation/realitykit/dockingregioncomponent/init())

#### Sizing a docking region

- [var width: Float](/documentation/realitykit/dockingregioncomponent/width)

### Playback notifications

- [VideoPlayerEvents](/documentation/realitykit/videoplayerevents)

#### Structures

- [VideoPlayerEvents.ContentTypeDidChange](/documentation/realitykit/videoplayerevents/contenttypedidchange)

##### Instance Properties

- [let contentType: VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.property)
- [let previousType: VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/previoustype)

##### Enumerations

- [VideoPlayerEvents.ContentTypeDidChange.ContentType](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum)

###### Enumeration Cases

- [case equirectangular](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/equirectangular)
- [case halfEquirectangular](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/halfequirectangular)
- [case immersive](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/immersive)
- [case invalid](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/invalid)
- [case mono](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/mono)
- [case parametricImmersive](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/parametricimmersive)
- [case stereo](/documentation/realitykit/videoplayerevents/contenttypedidchange/contenttype-swift.enum/stereo)
- [VideoPlayerEvents.ImmersiveViewingModeDidChange](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidchange/previousmode)
- [VideoPlayerEvents.ImmersiveViewingModeDidTransition](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodedidtransition/previousmode)
- [VideoPlayerEvents.ImmersiveViewingModeWillTransition](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition/currentmode)
- [let previousMode: VideoPlayerComponent.ImmersiveViewingMode?](/documentation/realitykit/videoplayerevents/immersiveviewingmodewilltransition/previousmode)
- [VideoPlayerEvents.RenderingStatusDidChange](/documentation/realitykit/videoplayerevents/renderingstatusdidchange)

##### Instance Properties

- [let currentStatus: VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayerevents/renderingstatusdidchange/currentstatus)
- [let previousStatus: VideoPlayerComponent.RenderingStatus](/documentation/realitykit/videoplayerevents/renderingstatusdidchange/previousstatus)
- [VideoPlayerEvents.SpatialVideoModeDidChange](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange)

##### Instance Properties

- [let currentMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange/currentmode)
- [let previousMode: VideoPlayerComponent.SpatialVideoMode](/documentation/realitykit/videoplayerevents/spatialvideomodedidchange/previousmode)
- [VideoPlayerEvents.VideoComfortMitigationDidOccur](/documentation/realitykit/videoplayerevents/videocomfortmitigationdidoccur)

##### Instance Properties

- [let comfortMitigation: VideoPlayerComponent.VideoComfortMitigation](/documentation/realitykit/videoplayerevents/videocomfortmitigationdidoccur/comfortmitigation)
- [VideoPlayerEvents.VideoSizeDidChange](/documentation/realitykit/videoplayerevents/videosizedidchange)

##### Instance Properties

- [let screenMeshSize: SIMD2<Float>](/documentation/realitykit/videoplayerevents/videosizedidchange/screenmeshsize)
- [let videoDimension: SIMD2<Float>](/documentation/realitykit/videoplayerevents/videosizedidchange/videodimension)
- [VideoPlayerEvents.ViewingModeDidChange](/documentation/realitykit/videoplayerevents/viewingmodedidchange)

##### Instance Properties

- [let currentViewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplayerevents/viewingmodedidchange/currentviewingmode)
- [let previousViewingMode: VideoPlaybackController.ViewingMode?](/documentation/realitykit/videoplayerevents/viewingmodedidchange/previousviewingmode)

### SwiftUI video content

- [Destination Video](/documentation/visionos/destination-video)
- [Docking a video player in an immersive scene](/documentation/realitykit/docking-a-video-player-in-an-immersive-scene)
- [Images](/documentation/realitykit/scene-content-images)

### Images and spatial scenes

- [ImagePresentationComponent](/documentation/realitykit/imagepresentationcomponent)

#### Creating a component from a 2D image or spatial photo

- [init(contentsOf: URL) async throws](/documentation/realitykit/imagepresentationcomponent/init(contentsof:))
- [init(imageSource: CGImageSource) async throws](/documentation/realitykit/imagepresentationcomponent/init(imagesource:))

#### Creating a component from a spatial scene

- [ImagePresentationComponent.Spatial3DImage](/documentation/realitykit/imagepresentationcomponent/spatial3dimage)

##### Creating a spatial scene from a 2D image or spatial photo

- [convenience init(contentsOf: URL) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(contentsof:))
- [init(imageSource: CGImageSource) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(imagesource:))

##### Generating a spatial scene

- [func generate() async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/generate())
- [init(spatial3DImage: ImagePresentationComponent.Spatial3DImage)](/documentation/realitykit/imagepresentationcomponent/init(spatial3dimage:))

#### Setting and discovering viewing modes

- [ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct)

##### Monoscopic presentation

- [static let mono: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/mono)

##### Stereoscopic presentation of spatial photos

- [static let spatialStereo: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereo)
- [static let spatialStereoImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereoimmersive)

##### 3D presentation of generated spatial scenes

- [static let spatial3D: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3d)
- [static let spatial3DImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3dimmersive)
- [var viewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.property)
- [var desiredViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/desiredviewingmode)
- [var availableViewingModes: Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/availableviewingmodes)
- [static func supportedViewingModes(for: CGImageSource) -> Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:)-7za1y)
- [static func supportedViewingModes(for: CGImageSource) -> Set<ImagePresentationComponent.ViewingMode>](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:)-7za1y)

#### Retrieving the current image size

- [var screenImageDimension: SIMD2<Float>](/documentation/realitykit/imagepresentationcomponent/screenimagedimension)

#### Retrieving the current screen mesh size

- [var screenHeight: Float](/documentation/realitykit/imagepresentationcomponent/screenheight)
- [var presentationScreenSize: SIMD2<Float>](/documentation/realitykit/imagepresentationcomponent/presentationscreensize)

#### Instance Methods

- [func aspectRatio(for: ImagePresentationComponent.ViewingMode) -> Float?](/documentation/realitykit/imagepresentationcomponent/aspectratio(for:))

#### Type Methods

- [static supportedViewingModes(for:)](/documentation/realitykit/imagepresentationcomponent/supportedviewingmodes(for:))
- [ImagePresentationComponent.Spatial3DImage](/documentation/realitykit/imagepresentationcomponent/spatial3dimage)

#### Creating a spatial scene from a 2D image or spatial photo

- [convenience init(contentsOf: URL) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(contentsof:))
- [init(imageSource: CGImageSource) async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/init(imagesource:))

#### Generating a spatial scene

- [func generate() async throws](/documentation/realitykit/imagepresentationcomponent/spatial3dimage/generate())

### Image presentation viewing modes

- [ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct)

#### Monoscopic presentation

- [static let mono: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/mono)

#### Stereoscopic presentation of spatial photos

- [static let spatialStereo: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereo)
- [static let spatialStereoImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatialstereoimmersive)

#### 3D presentation of generated spatial scenes

- [static let spatial3D: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3d)
- [static let spatial3DImmersive: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationcomponent/viewingmode-swift.struct/spatial3dimmersive)

### Image presentation events

- [ImagePresentationEvents](/documentation/realitykit/imagepresentationevents)

#### Viewing mode transitions

- [ImagePresentationEvents.TransitionStarted](/documentation/realitykit/imagepresentationevents/transitionstarted)

##### Instance Properties

- [let currentViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitionstarted/currentviewingmode)
- [let targetViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitionstarted/targetviewingmode)
- [ImagePresentationEvents.TransitionCompleted](/documentation/realitykit/imagepresentationevents/transitioncompleted)

##### Instance Properties

- [let currentViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitioncompleted/currentviewingmode)
- [let previousViewingMode: ImagePresentationComponent.ViewingMode](/documentation/realitykit/imagepresentationevents/transitioncompleted/previousviewingmode)

### SwiftUI image presentation

- [Presenting images in RealityKit](/documentation/realitykit/presenting-images-in-realitykit)

## Game development

- [Gaming sample code projects](/documentation/realitykit/game-development-sample-code)

### Sample code links

- [Bringing your SceneKit projects to RealityKit](/documentation/realitykit/bringing-your-scenekit-projects-to-realitykit)
- [Creating a Spaceship game](/documentation/realitykit/creating-a-spaceship-game)
- [BOT-anist](/documentation/visionos/bot-anist)
- [Rendering a windowed game in stereo](/documentation/realitykit/rendering-a-windowed-game-in-stereo)
- [Happy Beam](/documentation/visionos/happybeam)
- [Swift Splash](/documentation/visionos/swift-splash)
- [Destination Video](/documentation/visionos/destination-video)
- [Creating a game with scene understanding](/documentation/realitykit/creating-a-game-with-scene-understanding)
- [Entity animations](/documentation/realitykit/game-development-entity-animations)

### Animation playback

- [AnimationResource](/documentation/realitykit/animationresource)

#### Creating an animation resource

- [static func generate(with: any AnimationDefinition) throws -> AnimationResource](/documentation/realitykit/animationresource/generate(with:))
- [static func sequence(with: [AnimationResource]) throws -> AnimationResource](/documentation/realitykit/animationresource/sequence(with:))
- [static func group(with: [AnimationResource]) throws -> AnimationResource](/documentation/realitykit/animationresource/group(with:))
- [func `repeat`(count: Int) -> AnimationResource](/documentation/realitykit/animationresource/repeat(count:))
- [func `repeat`(duration: TimeInterval) -> AnimationResource](/documentation/realitykit/animationresource/repeat(duration:))

#### Inspecting animation information

- [let name: String?](/documentation/realitykit/animationresource/name)
- [var definition: any AnimationDefinition](/documentation/realitykit/animationresource/definition)
- [AnimationFillMode](/documentation/realitykit/animationfillmode)

##### Choosing a fill mode

- [static let none: AnimationFillMode](/documentation/realitykit/animationfillmode/none)
- [static let forwards: AnimationFillMode](/documentation/realitykit/animationfillmode/forwards)
- [static let backwards: AnimationFillMode](/documentation/realitykit/animationfillmode/backwards)
- [static let both: AnimationFillMode](/documentation/realitykit/animationfillmode/both)
- [init(rawValue: Int8)](/documentation/realitykit/animationfillmode/init(rawvalue:))

#### Associating an animation with an entity

- [func store(in: Entity)](/documentation/realitykit/animationresource/store(in:))

#### Type Methods

- [static func makeActionAnimation<T>(for: T, duration: TimeInterval, name: String, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float) throws -> AnimationResource](/documentation/realitykit/animationresource/makeactionanimation(for:duration:name:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))
- [AnimationLibraryComponent](/documentation/realitykit/animationlibrarycomponent)

#### Creating an animation library component

- [init()](/documentation/realitykit/animationlibrarycomponent/init())
- [init(animations: [String : AnimationResource])](/documentation/realitykit/animationlibrarycomponent/init(animations:))
- [init(dictionaryLiteral: (String, AnimationResource)...)](/documentation/realitykit/animationlibrarycomponent/init(dictionaryliteral:))

#### Accessing animations

- [var animations: AnimationLibraryComponent.AnimationCollection](/documentation/realitykit/animationlibrarycomponent/animations)
- [var unkeyedResources: [AnimationResource]?](/documentation/realitykit/animationlibrarycomponent/unkeyedresources)
- [var defaultAnimation: AnimationResource?](/documentation/realitykit/animationlibrarycomponent/defaultanimation)
- [var defaultKey: String?](/documentation/realitykit/animationlibrarycomponent/defaultkey)

#### Managing references to animations

- [func removeAll(resource: AnimationResource)](/documentation/realitykit/animationlibrarycomponent/removeall(resource:))

#### Structures

- [AnimationLibraryComponent.AnimationCollection](/documentation/realitykit/animationlibrarycomponent/animationcollection)

##### Creating an animation collection

- [init(dictionaryLiteral: (String, AnimationResource)...)](/documentation/realitykit/animationlibrarycomponent/animationcollection/init(dictionaryliteral:))

##### Accessing animations

- [subscript(String) -> AnimationResource?](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-4sfyo)
- [subscript(Range<AnimationLibraryComponent.AnimationCollection.Index>) -> AnimationLibraryComponent.AnimationCollection.SubSequence](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-2n5pw)
- [subscript(AnimationLibraryComponent.AnimationCollection.Index) -> AnimationLibraryComponent.AnimationCollection.Element](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-45p83)
- [AnimationLibraryComponent.AnimationCollection.SubSequence](/documentation/realitykit/animationlibrarycomponent/animationcollection/subsequence)
- [AnimationLibraryComponent.AnimationCollection.Element](/documentation/realitykit/animationlibrarycomponent/animationcollection/element)

##### Manipulating indices

- [var startIndex: AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/startindex)
- [var endIndex: AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/endindex)
- [func index(after: AnimationLibraryComponent.AnimationCollection.Index) -> AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/index(after:))
- [func formIndex(after: inout AnimationLibraryComponent.AnimationCollection.Index)](/documentation/realitykit/animationlibrarycomponent/animationcollection/formindex(after:))
- [AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/index)

###### Operators

- [static func < (AnimationLibraryComponent.AnimationCollection.Index, AnimationLibraryComponent.AnimationCollection.Index) -> Bool](/documentation/realitykit/animationlibrarycomponent/animationcollection/index/_(_:_:))

##### Iterating over animations

- [func makeIterator() -> AnimationLibraryComponent.AnimationCollection.Iterator](/documentation/realitykit/animationlibrarycomponent/animationcollection/makeiterator())
- [AnimationLibraryComponent.AnimationCollection.Iterator](/documentation/realitykit/animationlibrarycomponent/animationcollection/iterator)

##### Instance Properties

- [var count: Int](/documentation/realitykit/animationlibrarycomponent/animationcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/animationlibrarycomponent/animationcollection/isempty)

##### Subscripts

- [subscript(_:)](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:))
- [AnimationLibraryComponent.AnimationCollection](/documentation/realitykit/animationlibrarycomponent/animationcollection)

#### Creating an animation collection

- [init(dictionaryLiteral: (String, AnimationResource)...)](/documentation/realitykit/animationlibrarycomponent/animationcollection/init(dictionaryliteral:))

#### Accessing animations

- [subscript(String) -> AnimationResource?](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-4sfyo)
- [subscript(Range<AnimationLibraryComponent.AnimationCollection.Index>) -> AnimationLibraryComponent.AnimationCollection.SubSequence](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-2n5pw)
- [subscript(AnimationLibraryComponent.AnimationCollection.Index) -> AnimationLibraryComponent.AnimationCollection.Element](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:)-45p83)
- [AnimationLibraryComponent.AnimationCollection.SubSequence](/documentation/realitykit/animationlibrarycomponent/animationcollection/subsequence)
- [AnimationLibraryComponent.AnimationCollection.Element](/documentation/realitykit/animationlibrarycomponent/animationcollection/element)

#### Manipulating indices

- [var startIndex: AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/startindex)
- [var endIndex: AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/endindex)
- [func index(after: AnimationLibraryComponent.AnimationCollection.Index) -> AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/index(after:))
- [func formIndex(after: inout AnimationLibraryComponent.AnimationCollection.Index)](/documentation/realitykit/animationlibrarycomponent/animationcollection/formindex(after:))
- [AnimationLibraryComponent.AnimationCollection.Index](/documentation/realitykit/animationlibrarycomponent/animationcollection/index)

##### Operators

- [static func < (AnimationLibraryComponent.AnimationCollection.Index, AnimationLibraryComponent.AnimationCollection.Index) -> Bool](/documentation/realitykit/animationlibrarycomponent/animationcollection/index/_(_:_:))

#### Iterating over animations

- [func makeIterator() -> AnimationLibraryComponent.AnimationCollection.Iterator](/documentation/realitykit/animationlibrarycomponent/animationcollection/makeiterator())
- [AnimationLibraryComponent.AnimationCollection.Iterator](/documentation/realitykit/animationlibrarycomponent/animationcollection/iterator)

#### Instance Properties

- [var count: Int](/documentation/realitykit/animationlibrarycomponent/animationcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/animationlibrarycomponent/animationcollection/isempty)

#### Subscripts

- [subscript(_:)](/documentation/realitykit/animationlibrarycomponent/animationcollection/subscript(_:))
- [AnimationEvents](/documentation/realitykit/animationevents)

#### Recognizing animation events

- [AnimationEvents.PlaybackStarted](/documentation/realitykit/animationevents/playbackstarted)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackstarted/playbackcontroller)
- [AnimationEvents.PlaybackCompleted](/documentation/realitykit/animationevents/playbackcompleted)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackcompleted/playbackcontroller)
- [AnimationEvents.PlaybackLooped](/documentation/realitykit/animationevents/playbacklooped)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbacklooped/playbackcontroller)
- [AnimationEvents.PlaybackTerminated](/documentation/realitykit/animationevents/playbackterminated)

##### Instance Properties

- [let playbackController: AnimationPlaybackController](/documentation/realitykit/animationevents/playbackterminated/playbackcontroller)

#### Recognizing skeletal events

- [AnimationEvents.SkeletalPoseUpdateComplete](/documentation/realitykit/animationevents/skeletalposeupdatecomplete)

##### Instance Properties

- [let deltaTime: Float](/documentation/realitykit/animationevents/skeletalposeupdatecomplete/deltatime)
- [AnimationPlaybackController](/documentation/realitykit/animationplaybackcontroller)

#### Inspecting and controlling playback

- [func pause()](/documentation/realitykit/animationplaybackcontroller/pause())
- [func resume()](/documentation/realitykit/animationplaybackcontroller/resume())
- [func stop()](/documentation/realitykit/animationplaybackcontroller/stop())
- [var isPlaying: Bool](/documentation/realitykit/animationplaybackcontroller/isplaying)
- [var isStopped: Bool](/documentation/realitykit/animationplaybackcontroller/isstopped)
- [var isValid: Bool](/documentation/realitykit/animationplaybackcontroller/isvalid)
- [var blendFactor: Float](/documentation/realitykit/animationplaybackcontroller/blendfactor)

#### Managing completion

- [var isComplete: Bool](/documentation/realitykit/animationplaybackcontroller/iscomplete)
- [var isPaused: Bool](/documentation/realitykit/animationplaybackcontroller/ispaused)

#### Accessing the associated entity

- [var entity: Entity?](/documentation/realitykit/animationplaybackcontroller/entity)

#### Timing animation playback

- [var duration: TimeInterval](/documentation/realitykit/animationplaybackcontroller/duration)
- [var speed: Float](/documentation/realitykit/animationplaybackcontroller/speed)
- [var clock: CMClockOrTimebase](/documentation/realitykit/animationplaybackcontroller/clock)
- [var time: TimeInterval](/documentation/realitykit/animationplaybackcontroller/time)

#### Operators

- [static func == (AnimationPlaybackController, AnimationPlaybackController) -> Bool](/documentation/realitykit/animationplaybackcontroller/==(_:_:))

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/animationplaybackcontroller/hash(into:))
- [func stop(blendOutDuration: TimeInterval)](/documentation/realitykit/animationplaybackcontroller/stop(blendoutduration:))
- [AnimationRepeatMode](/documentation/realitykit/animationrepeatmode)

#### Choosing a repeat mode

- [case `repeat`](/documentation/realitykit/animationrepeatmode/repeat)
- [case cumulative](/documentation/realitykit/animationrepeatmode/cumulative)
- [case autoReverse](/documentation/realitykit/animationrepeatmode/autoreverse)
- [case none](/documentation/realitykit/animationrepeatmode/none)

### Animation definitions

- [SampledAnimation](/documentation/realitykit/sampledanimation)

#### Creating an animation

- [init(frames: [Value], name: String, tweenMode: TweenMode, frameInterval: Float, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/sampledanimation/init(frames:name:tweenmode:frameinterval:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))
- [init(jointNames: [String], frames: [Value], name: String, tweenMode: TweenMode, frameInterval: Float, isAdditive: Bool, isScaleAnimated: Bool, isRotationAnimated: Bool, isTranslationAnimated: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/sampledanimation/init(jointnames:frames:name:tweenmode:frameinterval:isadditive:isscaleanimated:isrotationanimated:istranslationanimated:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the animation

- [var name: String](/documentation/realitykit/sampledanimation/name)
- [var bindTarget: BindTarget](/documentation/realitykit/sampledanimation/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/sampledanimation/blendlayer)
- [var jointNames: [String]](/documentation/realitykit/sampledanimation/jointnames)
- [var isRotationAnimated: Bool](/documentation/realitykit/sampledanimation/isrotationanimated)
- [var isScaleAnimated: Bool](/documentation/realitykit/sampledanimation/isscaleanimated)
- [var isTranslationAnimated: Bool](/documentation/realitykit/sampledanimation/istranslationanimated)
- [var additive: Bool](/documentation/realitykit/sampledanimation/additive)
- [var tweenMode: TweenMode](/documentation/realitykit/sampledanimation/tweenmode)

#### Defining frames data

- [var frames: [JointTransforms]](/documentation/realitykit/sampledanimation/frames-4eeex)
- [var frames: [Transform]](/documentation/realitykit/sampledanimation/frames-4qotl)
- [var frames: [Double]](/documentation/realitykit/sampledanimation/frames-2hobp)
- [var frames: [Float]](/documentation/realitykit/sampledanimation/frames-2j4nj)
- [var frames: [simd_quatf]](/documentation/realitykit/sampledanimation/frames-2h6tu)
- [var frames: [SIMD2<Float>]](/documentation/realitykit/sampledanimation/frames-9luwf)
- [var frames: [SIMD3<Float>]](/documentation/realitykit/sampledanimation/frames-1zxo)
- [var frames: [SIMD4<Float>]](/documentation/realitykit/sampledanimation/frames-2ywfx)

#### Timing the animation

- [var frameInterval: Float](/documentation/realitykit/sampledanimation/frameinterval)
- [var start: TimeInterval](/documentation/realitykit/sampledanimation/start)
- [var end: TimeInterval](/documentation/realitykit/sampledanimation/end)
- [var speed: Float](/documentation/realitykit/sampledanimation/speed)
- [var delay: TimeInterval](/documentation/realitykit/sampledanimation/delay)
- [var duration: TimeInterval](/documentation/realitykit/sampledanimation/duration)
- [var offset: TimeInterval](/documentation/realitykit/sampledanimation/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/sampledanimation/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/sampledanimation/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/sampledanimation/trimend)

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/sampledanimation/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/sampledanimation/fillmode)

#### Initializers

- [init(weightNames: [String], frames: [Value], name: String, tweenMode: TweenMode, frameInterval: Float, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/sampledanimation/init(weightnames:frames:name:tweenmode:frameinterval:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Instance Properties

- [var frames: [BlendShapeWeights]](/documentation/realitykit/sampledanimation/frames-9jtu9)
- [var weightNames: [String]](/documentation/realitykit/sampledanimation/weightnames)
- [TweenMode](/documentation/realitykit/tweenmode)

#### Choosing a mode between frames

- [case hold](/documentation/realitykit/tweenmode/hold)
- [case linear](/documentation/realitykit/tweenmode/linear)
- [FromToByAnimation](/documentation/realitykit/fromtobyanimation)

#### Creating an animation

- [init(name: String, from: Value?, to: Value?, by: Value?, duration: TimeInterval, timing: AnimationTimingFunction, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/fromtobyanimation/init(name:from:to:by:duration:timing:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))
- [init(jointNames: [String], name: String, isScaleAnimated: Bool, isRotationAnimated: Bool, isTranslationAnimated: Bool, from: Value?, to: Value?, by: Value?, duration: TimeInterval, timing: AnimationTimingFunction, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/fromtobyanimation/init(jointnames:name:isscaleanimated:isrotationanimated:istranslationanimated:from:to:by:duration:timing:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the animation

- [var name: String](/documentation/realitykit/fromtobyanimation/name)
- [var bindTarget: BindTarget](/documentation/realitykit/fromtobyanimation/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/fromtobyanimation/blendlayer)
- [var jointNames: [String]](/documentation/realitykit/fromtobyanimation/jointnames)
- [var isScaleAnimated: Bool](/documentation/realitykit/fromtobyanimation/isscaleanimated)
- [var isRotationAnimated: Bool](/documentation/realitykit/fromtobyanimation/isrotationanimated)
- [var isTranslationAnimated: Bool](/documentation/realitykit/fromtobyanimation/istranslationanimated)
- [var isAdditive: Bool](/documentation/realitykit/fromtobyanimation/isadditive)

#### Defining a start value

- [var fromValue: JointTransforms?](/documentation/realitykit/fromtobyanimation/fromvalue-2h2wq)
- [var fromValue: Transform?](/documentation/realitykit/fromtobyanimation/fromvalue-8dr21)
- [var fromValue: Double?](/documentation/realitykit/fromtobyanimation/fromvalue-4tv25)
- [var fromValue: Float?](/documentation/realitykit/fromtobyanimation/fromvalue-umpp)
- [var fromValue: simd_quatf?](/documentation/realitykit/fromtobyanimation/fromvalue-12wzs)
- [var fromValue: SIMD2<Float>?](/documentation/realitykit/fromtobyanimation/fromvalue-5kx2b)
- [var fromValue: SIMD3<Float>?](/documentation/realitykit/fromtobyanimation/fromvalue-6msd)
- [var fromValue: SIMD4<Float>?](/documentation/realitykit/fromtobyanimation/fromvalue-5ckq7)

#### Defining an incremental value

- [var byValue: JointTransforms?](/documentation/realitykit/fromtobyanimation/byvalue-9zcwv)
- [var byValue: Transform?](/documentation/realitykit/fromtobyanimation/byvalue-5fewc)
- [var byValue: Double?](/documentation/realitykit/fromtobyanimation/byvalue-3soon)
- [var byValue: Float?](/documentation/realitykit/fromtobyanimation/byvalue-8na9o)
- [var byValue: simd_quatf?](/documentation/realitykit/fromtobyanimation/byvalue-460jf)
- [var byValue: SIMD2<Float>?](/documentation/realitykit/fromtobyanimation/byvalue-1pq4)
- [var byValue: SIMD3<Float>?](/documentation/realitykit/fromtobyanimation/byvalue-3bp3q)
- [var byValue: SIMD4<Float>?](/documentation/realitykit/fromtobyanimation/byvalue-7zwq3)

#### Defining an end value

- [var toValue: JointTransforms?](/documentation/realitykit/fromtobyanimation/tovalue-50qb4)
- [var toValue: Transform?](/documentation/realitykit/fromtobyanimation/tovalue-8jzdy)
- [var toValue: Double?](/documentation/realitykit/fromtobyanimation/tovalue-4nrhr)
- [var toValue: Float?](/documentation/realitykit/fromtobyanimation/tovalue-4m4pm)
- [var toValue: simd_quatf?](/documentation/realitykit/fromtobyanimation/tovalue-4wi6r)
- [var toValue: SIMD2<Float>?](/documentation/realitykit/fromtobyanimation/tovalue-6a1uy)
- [var toValue: SIMD3<Float>?](/documentation/realitykit/fromtobyanimation/tovalue-813jk)
- [var toValue: SIMD4<Float>?](/documentation/realitykit/fromtobyanimation/tovalue-5ki8u)

#### Timing the animation

- [var speed: Float](/documentation/realitykit/fromtobyanimation/speed)
- [var delay: TimeInterval](/documentation/realitykit/fromtobyanimation/delay)
- [var duration: TimeInterval](/documentation/realitykit/fromtobyanimation/duration)
- [var offset: TimeInterval](/documentation/realitykit/fromtobyanimation/offset)
- [var timing: AnimationTimingFunction](/documentation/realitykit/fromtobyanimation/timing)
- [var trimDuration: TimeInterval?](/documentation/realitykit/fromtobyanimation/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/fromtobyanimation/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/fromtobyanimation/trimend)

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/fromtobyanimation/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/fromtobyanimation/fillmode)

#### Initializers

- [init(weightNames: [String], name: String, from: Value?, to: Value?, by: Value?, duration: TimeInterval, timing: AnimationTimingFunction, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/fromtobyanimation/init(weightnames:name:from:to:by:duration:timing:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Instance Properties

- [var byValue: BlendShapeWeights?](/documentation/realitykit/fromtobyanimation/byvalue-2m18u)
- [var fromValue: BlendShapeWeights?](/documentation/realitykit/fromtobyanimation/fromvalue-66cs6)
- [var toValue: BlendShapeWeights?](/documentation/realitykit/fromtobyanimation/tovalue-5zgql)
- [var weightNames: [String]](/documentation/realitykit/fromtobyanimation/weightnames)
- [AnimationTimingFunction](/documentation/realitykit/animationtimingfunction)

#### Creating timing functions

- [static var `default`: AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/default)
- [static var easeIn: AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/easein)
- [static var easeInOut: AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/easeinout)
- [static var easeOut: AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/easeout)
- [static var linear: AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/linear)
- [static func cubicBezier(controlPoint1: SIMD2<Float>, controlPoint2: SIMD2<Float>) -> AnimationTimingFunction](/documentation/realitykit/animationtimingfunction/cubicbezier(controlpoint1:controlpoint2:))
- [AnimationView](/documentation/realitykit/animationview)

#### Creating an animation view

- [init(source: any AnimationDefinition, name: String, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/animationview/init(source:name:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the animation view

- [var source: (any AnimationDefinition)?](/documentation/realitykit/animationview/source)
- [var name: String](/documentation/realitykit/animationview/name)
- [var bindTarget: BindTarget](/documentation/realitykit/animationview/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/animationview/blendlayer)

#### Timing the animation

- [var speed: Float](/documentation/realitykit/animationview/speed)
- [var delay: TimeInterval](/documentation/realitykit/animationview/delay)
- [var duration: TimeInterval](/documentation/realitykit/animationview/duration)
- [var offset: TimeInterval](/documentation/realitykit/animationview/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/animationview/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/animationview/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/animationview/trimend)

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/animationview/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/animationview/fillmode)
- [OrbitAnimation](/documentation/realitykit/orbitanimation)

#### Creating an animation

- [init(name: String, duration: TimeInterval, axis: SIMD3<Float>, startTransform: Transform, spinClockwise: Bool, orientToPath: Bool, rotationCount: Float, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, isAdditive: Bool, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/orbitanimation/init(name:duration:axis:starttransform:spinclockwise:orienttopath:rotationcount:bindtarget:blendlayer:repeatmode:fillmode:isadditive:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the animation

- [var startTransform: Transform](/documentation/realitykit/orbitanimation/starttransform)
- [var axis: SIMD3<Float>](/documentation/realitykit/orbitanimation/axis)
- [var name: String](/documentation/realitykit/orbitanimation/name)
- [var bindTarget: BindTarget](/documentation/realitykit/orbitanimation/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/orbitanimation/blendlayer)
- [var rotationCount: Float](/documentation/realitykit/orbitanimation/rotationcount)
- [var spinClockwise: Bool](/documentation/realitykit/orbitanimation/spinclockwise)
- [var orientToPath: Bool](/documentation/realitykit/orbitanimation/orienttopath)
- [var additive: Bool](/documentation/realitykit/orbitanimation/additive)

#### Timing the animation

- [var speed: Float](/documentation/realitykit/orbitanimation/speed)
- [var delay: TimeInterval](/documentation/realitykit/orbitanimation/delay)
- [var duration: TimeInterval](/documentation/realitykit/orbitanimation/duration)
- [var offset: TimeInterval](/documentation/realitykit/orbitanimation/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/orbitanimation/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/orbitanimation/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/orbitanimation/trimend)

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/orbitanimation/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/orbitanimation/fillmode)
- [AnimationDefinition](/documentation/realitykit/animationdefinition)

#### Configuring the animation

- [var name: String](/documentation/realitykit/animationdefinition/name)
- [var bindTarget: BindTarget](/documentation/realitykit/animationdefinition/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/animationdefinition/blendlayer)

#### Timing the animation

- [var speed: Float](/documentation/realitykit/animationdefinition/speed)
- [var delay: TimeInterval](/documentation/realitykit/animationdefinition/delay)
- [var duration: TimeInterval](/documentation/realitykit/animationdefinition/duration)
- [var offset: TimeInterval](/documentation/realitykit/animationdefinition/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/animationdefinition/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/animationdefinition/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/animationdefinition/trimend)
- [func trimmed(start: TimeInterval?, end: TimeInterval?, duration: TimeInterval?) -> Self](/documentation/realitykit/animationdefinition/trimmed(start:end:duration:))

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/animationdefinition/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/animationdefinition/fillmode)
- [func repeated(count: TimeInterval) -> Self](/documentation/realitykit/animationdefinition/repeated(count:)-937w)
- [func repeated(count: Int) -> Self](/documentation/realitykit/animationdefinition/repeated(count:)-941x8)
- [func repeatingForever() -> Self](/documentation/realitykit/animationdefinition/repeatingforever())

#### Instance Methods

- [func repeated(count:)](/documentation/realitykit/animationdefinition/repeated(count:))
- [AnimationFillMode](/documentation/realitykit/animationfillmode)

#### Choosing a fill mode

- [static let none: AnimationFillMode](/documentation/realitykit/animationfillmode/none)
- [static let forwards: AnimationFillMode](/documentation/realitykit/animationfillmode/forwards)
- [static let backwards: AnimationFillMode](/documentation/realitykit/animationfillmode/backwards)
- [static let both: AnimationFillMode](/documentation/realitykit/animationfillmode/both)
- [init(rawValue: Int8)](/documentation/realitykit/animationfillmode/init(rawvalue:))
- [AnimationGroup](/documentation/realitykit/animationgroup)

#### Creating an animation group

- [init(group: [any AnimationDefinition], name: String, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/animationgroup/init(group:name:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the group

- [var group: [any AnimationDefinition]](/documentation/realitykit/animationgroup/group)
- [var name: String](/documentation/realitykit/animationgroup/name)
- [var bindTarget: BindTarget](/documentation/realitykit/animationgroup/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/animationgroup/blendlayer)
- [var additive: Bool](/documentation/realitykit/animationgroup/additive)
- [var group: [any AnimationDefinition]](/documentation/realitykit/animationgroup/group)

#### Timing the group

- [var speed: Float](/documentation/realitykit/animationgroup/speed)
- [var delay: TimeInterval](/documentation/realitykit/animationgroup/delay)
- [var duration: TimeInterval](/documentation/realitykit/animationgroup/duration)
- [var offset: TimeInterval](/documentation/realitykit/animationgroup/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/animationgroup/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/animationgroup/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/animationgroup/trimend)

#### Repeating group playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/animationgroup/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/animationgroup/fillmode)
- [AnimationHandoffType](/documentation/realitykit/animationhandofftype)

#### Type Properties

- [static var compose: AnimationHandoffType](/documentation/realitykit/animationhandofftype/compose)
- [static var `default`: AnimationHandoffType](/documentation/realitykit/animationhandofftype/default)
- [static var stop: AnimationHandoffType](/documentation/realitykit/animationhandofftype/stop)

#### Type Methods

- [static func replace(applyToAllLayers: Bool) -> AnimationHandoffType](/documentation/realitykit/animationhandofftype/replace(applytoalllayers:))
- [static func snapshotAndReplace(applyToAllLayers: Bool) -> AnimationHandoffType](/documentation/realitykit/animationhandofftype/snapshotandreplace(applytoalllayers:))

### Bindable animation targets

- [BindPath](/documentation/realitykit/bindpath)

#### Composing a property identifier

- [var parts: [BindPath.Part]](/documentation/realitykit/bindpath/parts)
- [BindPath.Part](/documentation/realitykit/bindpath/part)

##### Choosing the path component

- [case anchorEntity(String)](/documentation/realitykit/bindpath/part/anchorentity(_:))
- [case entity(String)](/documentation/realitykit/bindpath/part/entity(_:))
- [case jointTransforms](/documentation/realitykit/bindpath/part/jointtransforms)
- [case parameter(String)](/documentation/realitykit/bindpath/part/parameter(_:))
- [case scene(String)](/documentation/realitykit/bindpath/part/scene(_:))
- [case transform](/documentation/realitykit/bindpath/part/transform)

##### Operators

- [static func == (BindPath.Part, BindPath.Part) -> Bool](/documentation/realitykit/bindpath/part/==(_:_:))

##### Enumeration Cases

- [case billboardBlendFactor](/documentation/realitykit/bindpath/part/billboardblendfactor)
- [case blendShapeWeights](/documentation/realitykit/bindpath/part/blendshapeweights)
- [case blendShapeWeightsAtIndex(Int)](/documentation/realitykit/bindpath/part/blendshapeweightsatindex(_:))
- [case blendShapeWeightsWithID(BlendShapeWeightsData.ID)](/documentation/realitykit/bindpath/part/blendshapeweightswithid(_:))
- [case ikConstraintLookAtTarget(IKComponent.Constraint.ID)](/documentation/realitykit/bindpath/part/ikconstraintlookattarget(_:))
- [case ikConstraintTarget(IKComponent.Constraint.ID)](/documentation/realitykit/bindpath/part/ikconstrainttarget(_:))
- [case ikSolver(IKComponent.Solver.ID?)](/documentation/realitykit/bindpath/part/iksolver(_:))
- [case material(Int)](/documentation/realitykit/bindpath/part/material(_:))
- [case materialParameter(String)](/documentation/realitykit/bindpath/part/materialparameter(_:))
- [case opacity](/documentation/realitykit/bindpath/part/opacity)
- [case skeletalPose(SkeletalPose.ID)](/documentation/realitykit/bindpath/part/skeletalpose(_:))
- [BindTarget](/documentation/realitykit/bindtarget)

#### Choosing a bind target

- [case `internal`(InternalBindPath)](/documentation/realitykit/bindtarget/internal(_:))
- [case jointTransforms](/documentation/realitykit/bindtarget/jointtransforms)
- [case parameter(String)](/documentation/realitykit/bindtarget/parameter(_:))
- [case path(BindPath)](/documentation/realitykit/bindtarget/path(_:))
- [case transform](/documentation/realitykit/bindtarget/transform)

#### Targeting entities and scenes

- [static func scene(String) -> BindTarget.ScenePath](/documentation/realitykit/bindtarget/scene(_:))
- [BindTarget.ScenePath](/documentation/realitykit/bindtarget/scenepath)

##### Accessing the anchor entity

- [func anchorEntity(String) -> BindTarget.EntityPath](/documentation/realitykit/bindtarget/scenepath/anchorentity(_:))

##### Accessing the bind target

- [var `self`: BindTarget](/documentation/realitykit/bindtarget/scenepath/self)
- [static func anchorEntity(String) -> BindTarget.EntityPath](/documentation/realitykit/bindtarget/anchorentity(_:))
- [static func entity(String) -> BindTarget.EntityPath](/documentation/realitykit/bindtarget/entity(_:))
- [BindTarget.EntityPath](/documentation/realitykit/bindtarget/entitypath)

##### Accessing a bind target

- [var jointTransforms: BindTarget](/documentation/realitykit/bindtarget/entitypath/jointtransforms)
- [var transform: BindTarget](/documentation/realitykit/bindtarget/entitypath/transform)
- [var `self`: BindTarget](/documentation/realitykit/bindtarget/entitypath/self)
- [func parameter(String) -> BindTarget](/documentation/realitykit/bindtarget/entitypath/parameter(_:))

##### Accessing child-entity paths

- [func entity(String) -> BindTarget.EntityPath](/documentation/realitykit/bindtarget/entitypath/entity(_:))

##### Instance Properties

- [var billboardBlendFactor: BindTarget](/documentation/realitykit/bindtarget/entitypath/billboardblendfactor)
- [var opacity: BindTarget](/documentation/realitykit/bindtarget/entitypath/opacity)

##### Instance Methods

- [func blendShapeWeights() -> BindTarget](/documentation/realitykit/bindtarget/entitypath/blendshapeweights())
- [func blendShapeWeightsAtIndex(Int) -> BindTarget](/documentation/realitykit/bindtarget/entitypath/blendshapeweightsatindex(_:))
- [func blendShapeWeightsWithID(BlendShapeWeightsData.ID) -> BindTarget](/documentation/realitykit/bindtarget/entitypath/blendshapeweightswithid(_:))
- [func ikSolver(IKComponent.Solver.ID?) -> BindTarget.IkSolverPath](/documentation/realitykit/bindtarget/entitypath/iksolver(_:))
- [func material(Int) -> BindTarget.MaterialPath](/documentation/realitykit/bindtarget/entitypath/material(_:))
- [func skeletalPose(SkeletalPose.ID) -> BindTarget](/documentation/realitykit/bindtarget/entitypath/skeletalpose(_:))

#### Animatable properties

- [case opacity](/documentation/realitykit/bindtarget/opacity)
- [case billboardBlendFactor](/documentation/realitykit/bindtarget/billboardblendfactor)
- [case blendShapeWeights](/documentation/realitykit/bindtarget/blendshapeweights)
- [case skeletalPose(String)](/documentation/realitykit/bindtarget/skeletalpose(_:))
- [case blendShapeWeightsAtIndex(Int)](/documentation/realitykit/bindtarget/blendshapeweightsatindex(_:))
- [case blendShapeWeightsWithID(BlendShapeWeightsData.ID)](/documentation/realitykit/bindtarget/blendshapeweightswithid(_:))
- [static func material(Int) -> BindTarget.MaterialPath](/documentation/realitykit/bindtarget/material(_:))
- [BindTarget.MaterialPath](/documentation/realitykit/bindtarget/materialpath)

##### Instance Properties

- [var anisotropyAngleScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/anisotropyanglescale)
- [var anisotropyLevelScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/anisotropylevelscale)
- [var baseColorTint: BindTarget](/documentation/realitykit/bindtarget/materialpath/basecolortint)
- [var clearcoatRoughnessScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/clearcoatroughnessscale)
- [var clearcoatScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/clearcoatscale)
- [var customValue: BindTarget](/documentation/realitykit/bindtarget/materialpath/customvalue)
- [var emissiveColor: BindTarget](/documentation/realitykit/bindtarget/materialpath/emissivecolor)
- [var emissiveIntensity: BindTarget](/documentation/realitykit/bindtarget/materialpath/emissiveintensity)
- [var metallicScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/metallicscale)
- [var opacityThreshold: BindTarget](/documentation/realitykit/bindtarget/materialpath/opacitythreshold)
- [var roughnessScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/roughnessscale)
- [var secondaryTextureCoordinate: BindTarget.TextureCoordinateTransformPath](/documentation/realitykit/bindtarget/materialpath/secondarytexturecoordinate)
- [var sheenTint: BindTarget](/documentation/realitykit/bindtarget/materialpath/sheentint)
- [var specularScale: BindTarget](/documentation/realitykit/bindtarget/materialpath/specularscale)
- [var textureCoordinate: BindTarget.TextureCoordinateTransformPath](/documentation/realitykit/bindtarget/materialpath/texturecoordinate)
- [BindTarget.TextureCoordinateTransformPath](/documentation/realitykit/bindtarget/texturecoordinatetransformpath)

##### Instance Properties

- [var offset: BindTarget](/documentation/realitykit/bindtarget/texturecoordinatetransformpath/offset)
- [BindTarget.IkSolverPath](/documentation/realitykit/bindtarget/iksolverpath)

##### Instance Methods

- [func constraintLookAtTarget(String) -> BindTarget](/documentation/realitykit/bindtarget/iksolverpath/constraintlookattarget(_:))
- [func constraintTarget(String) -> BindTarget](/documentation/realitykit/bindtarget/iksolverpath/constrainttarget(_:))

#### Operators

- [static func == (BindTarget, BindTarget) -> Bool](/documentation/realitykit/bindtarget/==(_:_:))
- [BindableValue](/documentation/realitykit/bindablevalue)

#### Creating a value

- [init(T, animatedValue: T?)](/documentation/realitykit/bindablevalue/init(_:animatedvalue:))

#### Accessing the value

- [var value: T](/documentation/realitykit/bindablevalue/value)
- [var baseValue: T](/documentation/realitykit/bindablevalue/basevalue)
- [var animatedValue: T?](/documentation/realitykit/bindablevalue/animatedvalue)
- [BindableValuesReference](/documentation/realitykit/bindablevaluesreference)

#### Accessing values

- [subscript<T>(BindTarget, T.Type) -> BindableValue<T>?](/documentation/realitykit/bindablevaluesreference/subscript(_:_:))
- [ParameterSet](/documentation/realitykit/parameterset)

#### Accessing a parameter by name

- [subscript<T>(String, T.Type) -> BindableValue<T>?](/documentation/realitykit/parameterset/subscript(_:_:))
- [InternalBindPath](/documentation/realitykit/internalbindpath)

### Compliance-related protocols

- [AnimatableData](/documentation/realitykit/animatabledata)
- [BindableData](/documentation/realitykit/bindabledata)

### Blend trees

- [BlendTreeAnimation](/documentation/realitykit/blendtreeanimation)

#### Creating an animation

- [init(any BlendTreeNode, name: String, isAdditive: Bool, bindTarget: BindTarget?, blendLayer: Int32, repeatMode: AnimationRepeatMode, fillMode: AnimationFillMode, trimStart: TimeInterval?, trimEnd: TimeInterval?, trimDuration: TimeInterval?, offset: TimeInterval, delay: TimeInterval, speed: Float)](/documentation/realitykit/blendtreeanimation/init(_:name:isadditive:bindtarget:blendlayer:repeatmode:fillmode:trimstart:trimend:trimduration:offset:delay:speed:))

#### Configuring the animation

- [var root: any BlendTreeNode](/documentation/realitykit/blendtreeanimation/root)
- [var name: String](/documentation/realitykit/blendtreeanimation/name)
- [var bindTarget: BindTarget](/documentation/realitykit/blendtreeanimation/bindtarget)
- [var blendLayer: Int32](/documentation/realitykit/blendtreeanimation/blendlayer)
- [var isAdditive: Bool](/documentation/realitykit/blendtreeanimation/isadditive)

#### Timing the animation

- [var speed: Float](/documentation/realitykit/blendtreeanimation/speed)
- [var delay: TimeInterval](/documentation/realitykit/blendtreeanimation/delay)
- [var duration: TimeInterval](/documentation/realitykit/blendtreeanimation/duration)
- [var offset: TimeInterval](/documentation/realitykit/blendtreeanimation/offset)
- [var trimDuration: TimeInterval?](/documentation/realitykit/blendtreeanimation/trimduration)
- [var trimStart: TimeInterval?](/documentation/realitykit/blendtreeanimation/trimstart)
- [var trimEnd: TimeInterval?](/documentation/realitykit/blendtreeanimation/trimend)

#### Repeating animation playback

- [var repeatMode: AnimationRepeatMode](/documentation/realitykit/blendtreeanimation/repeatmode)
- [var fillMode: AnimationFillMode](/documentation/realitykit/blendtreeanimation/fillmode)
- [BlendTreeNode](/documentation/realitykit/blendtreenode)

#### Configuring the blend tree node

- [var name: String](/documentation/realitykit/blendtreenode/name)
- [var weight: BlendWeight](/documentation/realitykit/blendtreenode/weight)

#### Blending animations

- [func blend(sources: [any BlendTreeNode], name: String, isAdditive: Bool) -> any BlendTreeNode](/documentation/realitykit/blend(sources:name:isadditive:))
- [func blend(any BlendTreeNode, any BlendTreeNode, name: String, isAdditive: Bool) -> any BlendTreeNode](/documentation/realitykit/blend(_:_:name:isadditive:))
- [BlendTreeBlendNode](/documentation/realitykit/blendtreeblendnode)

#### Creating a blend-tree blend node

- [init(sources: [any BlendTreeNode], name: String, weight: BlendWeight, isAdditive: Bool)](/documentation/realitykit/blendtreeblendnode/init(sources:name:weight:isadditive:))

#### Configuring the node

- [var name: String](/documentation/realitykit/blendtreeblendnode/name)
- [var weight: BlendWeight](/documentation/realitykit/blendtreeblendnode/weight)
- [var isAdditive: Bool](/documentation/realitykit/blendtreeblendnode/isadditive)

#### Configuring child nodes

- [var sources: [any BlendTreeNode]](/documentation/realitykit/blendtreeblendnode/sources)
- [BlendTreeSourceNode](/documentation/realitykit/blendtreesourcenode)

#### Creating a blend tree animation node

- [init(source: any AnimationDefinition, name: String, weight: BlendWeight)](/documentation/realitykit/blendtreesourcenode/init(source:name:weight:))

#### Configuring a blend tree animation node

- [var name: String](/documentation/realitykit/blendtreesourcenode/name)
- [var source: (any AnimationDefinition)?](/documentation/realitykit/blendtreesourcenode/source)
- [var weight: BlendWeight](/documentation/realitykit/blendtreesourcenode/weight)
- [BlendTreeInvalidNode](/documentation/realitykit/blendtreeinvalidnode)

#### Configuring the blend tree invalid node

- [var name: String](/documentation/realitykit/blendtreeinvalidnode/name)
- [var weight: BlendWeight](/documentation/realitykit/blendtreeinvalidnode/weight)
- [BlendWeight](/documentation/realitykit/blendweight)

#### Choosing the blend weight

- [case bindTarget(BindTarget, defaultWeight: Float)](/documentation/realitykit/blendweight/bindtarget(_:defaultweight:))
- [case parameter(String, defaultWeight: Float)](/documentation/realitykit/blendweight/parameter(_:defaultweight:))
- [case value(Float)](/documentation/realitykit/blendweight/value(_:))

#### Operators

- [static func == (BlendWeight, BlendWeight) -> Bool](/documentation/realitykit/blendweight/==(_:_:))
- [Character control, skeletons, and inverse kinematics](/documentation/realitykit/game-development-character-skeletons)

### Character control

- [CharacterControllerComponent](/documentation/realitykit/charactercontrollercomponent)

#### Creating a character controller component

- [init()](/documentation/realitykit/charactercontrollercomponent/init())
- [init(radius: Float, height: Float, skinWidth: Float, slopeLimit: Float, stepLimit: Float, upVector: SIMD3<Float>, collisionFilter: CollisionFilter)](/documentation/realitykit/charactercontrollercomponent/init(radius:height:skinwidth:slopelimit:steplimit:upvector:collisionfilter:))

#### Configuring a character

- [var height: Float](/documentation/realitykit/charactercontrollercomponent/height)
- [var radius: Float](/documentation/realitykit/charactercontrollercomponent/radius)
- [var skinWidth: Float](/documentation/realitykit/charactercontrollercomponent/skinwidth)
- [var slopeLimit: Float](/documentation/realitykit/charactercontrollercomponent/slopelimit)
- [var stepLimit: Float](/documentation/realitykit/charactercontrollercomponent/steplimit)
- [var upVector: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/upvector)

#### Managing character collisions

- [var collisionFilter: CollisionFilter](/documentation/realitykit/charactercontrollercomponent/collisionfilter)

#### Reading default values

- [static let defaultHeight: Float](/documentation/realitykit/charactercontrollercomponent/defaultheight)
- [static let defaultRadius: Float](/documentation/realitykit/charactercontrollercomponent/defaultradius)
- [static let defaultSkinWidth: Float](/documentation/realitykit/charactercontrollercomponent/defaultskinwidth)
- [static let defaultSlopeLimit: Float](/documentation/realitykit/charactercontrollercomponent/defaultslopelimit)
- [static let defaultStepLimit: Float](/documentation/realitykit/charactercontrollercomponent/defaultsteplimit)
- [static let defaultUpVector: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/defaultupvector)

#### Animating a character

- [JointTransforms](/documentation/realitykit/jointtransforms)

##### Creating joint transforms

- [init()](/documentation/realitykit/jointtransforms/init())
- [init<S>(S)](/documentation/realitykit/jointtransforms/init(_:))
- [init(arrayLiteral: Transform...)](/documentation/realitykit/jointtransforms/init(arrayliteral:))

##### Identifying joint transforms

- [JointTransforms.Index](/documentation/realitykit/jointtransforms/index)

##### Inspecting joint transform details

- [var startIndex: JointTransforms.Index](/documentation/realitykit/jointtransforms/startindex)
- [var endIndex: JointTransforms.Index](/documentation/realitykit/jointtransforms/endindex)

##### Accessing joint transforms

- [subscript(JointTransforms.Index) -> Transform](/documentation/realitykit/jointtransforms/subscript(_:))
- [func index(after: JointTransforms.Index) -> JointTransforms.Index](/documentation/realitykit/jointtransforms/index(after:))
- [func index(before: JointTransforms.Index) -> JointTransforms.Index](/documentation/realitykit/jointtransforms/index(before:))

##### Operators

- [static func == (JointTransforms, JointTransforms) -> Bool](/documentation/realitykit/jointtransforms/==(_:_:))

##### Type Aliases

- [JointTransforms.ArrayLiteralElement](/documentation/realitykit/jointtransforms/arrayliteralelement)
- [JointTransforms.Element](/documentation/realitykit/jointtransforms/element)

#### Handling collisions

- [CharacterControllerComponent.Collision](/documentation/realitykit/charactercontrollercomponent/collision)

##### Initializers

- [init(characterEntity: Entity, hitEntity: Entity, hitPosition: SIMD3<Float>, hitNormal: SIMD3<Float>, moveDirection: SIMD3<Float>, moveDistance: Float)](/documentation/realitykit/charactercontrollercomponent/collision/init(characterentity:hitentity:hitposition:hitnormal:movedirection:movedistance:))

##### Instance Properties

- [var characterEntity: Entity](/documentation/realitykit/charactercontrollercomponent/collision/characterentity)
- [var hitEntity: Entity](/documentation/realitykit/charactercontrollercomponent/collision/hitentity)
- [var hitNormal: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/hitnormal)
- [var hitPosition: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/hitposition)
- [var moveDirection: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/movedirection)
- [var moveDistance: Float](/documentation/realitykit/charactercontrollercomponent/collision/movedistance)
- [CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags)

##### Initializers

- [init(rawValue: UInt8)](/documentation/realitykit/charactercontrollercomponent/collisionflags/init(rawvalue:))

##### Instance Properties

- [let rawValue: UInt8](/documentation/realitykit/charactercontrollercomponent/collisionflags/rawvalue)

##### Type Properties

- [static let bottom: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/bottom)
- [static let none: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/none)
- [static let side: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/side)
- [static let top: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/top)
- [CharacterControllerComponent.Collision](/documentation/realitykit/charactercontrollercomponent/collision)

#### Initializers

- [init(characterEntity: Entity, hitEntity: Entity, hitPosition: SIMD3<Float>, hitNormal: SIMD3<Float>, moveDirection: SIMD3<Float>, moveDistance: Float)](/documentation/realitykit/charactercontrollercomponent/collision/init(characterentity:hitentity:hitposition:hitnormal:movedirection:movedistance:))

#### Instance Properties

- [var characterEntity: Entity](/documentation/realitykit/charactercontrollercomponent/collision/characterentity)
- [var hitEntity: Entity](/documentation/realitykit/charactercontrollercomponent/collision/hitentity)
- [var hitNormal: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/hitnormal)
- [var hitPosition: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/hitposition)
- [var moveDirection: SIMD3<Float>](/documentation/realitykit/charactercontrollercomponent/collision/movedirection)
- [var moveDistance: Float](/documentation/realitykit/charactercontrollercomponent/collision/movedistance)
- [CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags)

#### Initializers

- [init(rawValue: UInt8)](/documentation/realitykit/charactercontrollercomponent/collisionflags/init(rawvalue:))

#### Instance Properties

- [let rawValue: UInt8](/documentation/realitykit/charactercontrollercomponent/collisionflags/rawvalue)

#### Type Properties

- [static let bottom: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/bottom)
- [static let none: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/none)
- [static let side: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/side)
- [static let top: CharacterControllerComponent.CollisionFlags](/documentation/realitykit/charactercontrollercomponent/collisionflags/top)
- [CharacterControllerStateComponent](/documentation/realitykit/charactercontrollerstatecomponent)

#### Creating a state component

- [init()](/documentation/realitykit/charactercontrollerstatecomponent/init())

#### Accessing character controller state

- [let isOnGround: Bool](/documentation/realitykit/charactercontrollerstatecomponent/isonground)
- [let velocity: SIMD3<Float>](/documentation/realitykit/charactercontrollerstatecomponent/velocity)

### Skeletons

- [SkeletalPosesComponent](/documentation/realitykit/skeletalposescomponent)

#### Initializers

- [init(poses: [SkeletalPose])](/documentation/realitykit/skeletalposescomponent/init(poses:))

#### Instance Properties

- [var poses: SkeletalPoseSet](/documentation/realitykit/skeletalposescomponent/poses)
- [SkeletalPose](/documentation/realitykit/skeletalpose)

#### Initializers

- [init(id: SkeletalPose.ID, from: MeshResource.Skeleton)](/documentation/realitykit/skeletalpose/init(id:from:))
- [init(id: SkeletalPose.ID, joints: [(String, JointTransforms.Element)])](/documentation/realitykit/skeletalpose/init(id:joints:))

#### Instance Properties

- [var id: SkeletalPose.ID](/documentation/realitykit/skeletalpose/id)
- [var jointNames: [String]](/documentation/realitykit/skeletalpose/jointnames)
- [var jointTransforms: JointTransforms](/documentation/realitykit/skeletalpose/jointtransforms)

#### Subscripts

- [subscript(String) -> Transform?](/documentation/realitykit/skeletalpose/subscript(_:))
- [SkeletalPoseSet](/documentation/realitykit/skeletalposeset)

#### Initializers

- [init()](/documentation/realitykit/skeletalposeset/init())

#### Instance Properties

- [var count: Int](/documentation/realitykit/skeletalposeset/count)
- [var `default`: SkeletalPoseSet.Element?](/documentation/realitykit/skeletalposeset/default)
- [var isEmpty: Bool](/documentation/realitykit/skeletalposeset/isempty)

#### Instance Methods

- [func contains(SkeletalPose.ID) -> Bool](/documentation/realitykit/skeletalposeset/contains(_:))
- [func index(of: SkeletalPose.ID) -> SkeletalPoseSet.Index?](/documentation/realitykit/skeletalposeset/index(of:))
- [func set(SkeletalPoseSet.Element) -> SkeletalPoseSet.Element?](/documentation/realitykit/skeletalposeset/set(_:))

#### Default Implementations

- [Collection Implementations](/documentation/realitykit/skeletalposeset/collection-implementations)

##### Instance Properties

- [var endIndex: SkeletalPoseSet.Index](/documentation/realitykit/skeletalposeset/endindex)
- [var startIndex: SkeletalPoseSet.Index](/documentation/realitykit/skeletalposeset/startindex)

##### Instance Methods

- [func index(after: SkeletalPoseSet.Index) -> SkeletalPoseSet.Index](/documentation/realitykit/skeletalposeset/index(after:))

##### Subscripts

- [subscript(_:)](/documentation/realitykit/skeletalposeset/subscript(_:))
- [subscript(SkeletalPoseSet.Index) -> SkeletalPoseSet.Element](/documentation/realitykit/skeletalposeset/subscript(_:)-8fm7n)

### Inverse kinematics components

- [IKComponent](/documentation/realitykit/ikcomponent)

#### Classes

- [IKComponent.Constraint](/documentation/realitykit/ikcomponent/constraint)

##### Structures

- [IKComponent.Constraint.DemandOptions](/documentation/realitykit/ikcomponent/constraint/demandoptions)

##### Instance Properties

- [var animationOverrideWeight: (position: Float, rotation: Float)](/documentation/realitykit/ikcomponent/constraint/animationoverrideweight)
- [var demands: IKComponent.Constraint.DemandOptions](/documentation/realitykit/ikcomponent/constraint/demands)
- [let id: IKComponent.Constraint.ID](/documentation/realitykit/ikcomponent/constraint/id)
- [var jointID: IKComponent.Joint.ID](/documentation/realitykit/ikcomponent/constraint/jointid)
- [var lookAtTargetPosition: SIMD3<Float>](/documentation/realitykit/ikcomponent/constraint/lookattargetposition)
- [var name: String](/documentation/realitykit/ikcomponent/constraint/name)
- [var offset: Transform](/documentation/realitykit/ikcomponent/constraint/offset)
- [var target: Transform](/documentation/realitykit/ikcomponent/constraint/target)
- [IKComponent.Joint](/documentation/realitykit/ikcomponent/joint)

##### Instance Properties

- [var fkWeightPerAxis: SIMD3<Float>](/documentation/realitykit/ikcomponent/joint/fkweightperaxis)
- [let id: IKComponent.Joint.ID](/documentation/realitykit/ikcomponent/joint/id)
- [var name: String](/documentation/realitykit/ikcomponent/joint/name)
- [var rotationStiffness: SIMD3<Float>](/documentation/realitykit/ikcomponent/joint/rotationstiffness)
- [IKComponent.Solver](/documentation/realitykit/ikcomponent/solver)

##### Structures

- [IKComponent.Solver.ID](/documentation/realitykit/ikcomponent/solver/id-swift.struct)

##### Instance Properties

- [var constraints: IKComponent.ConstraintCollection](/documentation/realitykit/ikcomponent/solver/constraints)
- [var globalFkWeight: Float](/documentation/realitykit/ikcomponent/solver/globalfkweight)
- [var id: IKComponent.Solver.ID](/documentation/realitykit/ikcomponent/solver/id-swift.property)
- [var joints: IKComponent.JointCollection](/documentation/realitykit/ikcomponent/solver/joints)
- [var maxIterations: Int](/documentation/realitykit/ikcomponent/solver/maxiterations)

##### Instance Methods

- [func reset()](/documentation/realitykit/ikcomponent/solver/reset())

#### Structures

- [IKComponent.ConstraintCollection](/documentation/realitykit/ikcomponent/constraintcollection)

##### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/constraintcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/constraintcollection/isempty)

##### Instance Methods

- [func contains(IKComponent.ConstraintCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/constraintcollection/contains(_:))
- [func set(IKComponent.ConstraintCollection.Element) -> IKComponent.ConstraintCollection.Element?](/documentation/realitykit/ikcomponent/constraintcollection/set(_:))

##### Subscripts

- [subscript(_:)](/documentation/realitykit/ikcomponent/constraintcollection/subscript(_:))
- [IKComponent.JointCollection](/documentation/realitykit/ikcomponent/jointcollection)

##### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/jointcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/jointcollection/isempty)

##### Instance Methods

- [func contains(IKComponent.JointCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/jointcollection/contains(_:))
- [func set(IKComponent.JointCollection.Element) -> IKComponent.JointCollection.Element?](/documentation/realitykit/ikcomponent/jointcollection/set(_:))

##### Subscripts

- [subscript(_:)](/documentation/realitykit/ikcomponent/jointcollection/subscript(_:))
- [IKComponent.SolverCollection](/documentation/realitykit/ikcomponent/solvercollection)

##### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/solvercollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/solvercollection/isempty)

##### Instance Methods

- [func contains(IKComponent.SolverCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/solvercollection/contains(_:))
- [func set(IKComponent.SolverCollection.Element) -> IKComponent.SolverCollection.Element?](/documentation/realitykit/ikcomponent/solvercollection/set(_:))

##### Subscripts

- [subscript(IKComponent.SolverCollection.Element.ID) -> IKComponent.SolverCollection.Element?](/documentation/realitykit/ikcomponent/solvercollection/subscript(_:))

#### Initializers

- [init(resource: IKResource?)](/documentation/realitykit/ikcomponent/init(resource:))

#### Instance Properties

- [var resource: IKResource?](/documentation/realitykit/ikcomponent/resource)
- [var solvers: IKComponent.SolverCollection](/documentation/realitykit/ikcomponent/solvers)
- [IKComponent.Joint](/documentation/realitykit/ikcomponent/joint)

#### Instance Properties

- [var fkWeightPerAxis: SIMD3<Float>](/documentation/realitykit/ikcomponent/joint/fkweightperaxis)
- [let id: IKComponent.Joint.ID](/documentation/realitykit/ikcomponent/joint/id)
- [var name: String](/documentation/realitykit/ikcomponent/joint/name)
- [var rotationStiffness: SIMD3<Float>](/documentation/realitykit/ikcomponent/joint/rotationstiffness)
- [IKComponent.JointCollection](/documentation/realitykit/ikcomponent/jointcollection)

#### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/jointcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/jointcollection/isempty)

#### Instance Methods

- [func contains(IKComponent.JointCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/jointcollection/contains(_:))
- [func set(IKComponent.JointCollection.Element) -> IKComponent.JointCollection.Element?](/documentation/realitykit/ikcomponent/jointcollection/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/ikcomponent/jointcollection/subscript(_:))
- [IKComponent.Solver](/documentation/realitykit/ikcomponent/solver)

#### Structures

- [IKComponent.Solver.ID](/documentation/realitykit/ikcomponent/solver/id-swift.struct)

#### Instance Properties

- [var constraints: IKComponent.ConstraintCollection](/documentation/realitykit/ikcomponent/solver/constraints)
- [var globalFkWeight: Float](/documentation/realitykit/ikcomponent/solver/globalfkweight)
- [var id: IKComponent.Solver.ID](/documentation/realitykit/ikcomponent/solver/id-swift.property)
- [var joints: IKComponent.JointCollection](/documentation/realitykit/ikcomponent/solver/joints)
- [var maxIterations: Int](/documentation/realitykit/ikcomponent/solver/maxiterations)

#### Instance Methods

- [func reset()](/documentation/realitykit/ikcomponent/solver/reset())
- [IKComponent.SolverCollection](/documentation/realitykit/ikcomponent/solvercollection)

#### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/solvercollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/solvercollection/isempty)

#### Instance Methods

- [func contains(IKComponent.SolverCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/solvercollection/contains(_:))
- [func set(IKComponent.SolverCollection.Element) -> IKComponent.SolverCollection.Element?](/documentation/realitykit/ikcomponent/solvercollection/set(_:))

#### Subscripts

- [subscript(IKComponent.SolverCollection.Element.ID) -> IKComponent.SolverCollection.Element?](/documentation/realitykit/ikcomponent/solvercollection/subscript(_:))
- [IKComponent.Constraint](/documentation/realitykit/ikcomponent/constraint)

#### Structures

- [IKComponent.Constraint.DemandOptions](/documentation/realitykit/ikcomponent/constraint/demandoptions)

#### Instance Properties

- [var animationOverrideWeight: (position: Float, rotation: Float)](/documentation/realitykit/ikcomponent/constraint/animationoverrideweight)
- [var demands: IKComponent.Constraint.DemandOptions](/documentation/realitykit/ikcomponent/constraint/demands)
- [let id: IKComponent.Constraint.ID](/documentation/realitykit/ikcomponent/constraint/id)
- [var jointID: IKComponent.Joint.ID](/documentation/realitykit/ikcomponent/constraint/jointid)
- [var lookAtTargetPosition: SIMD3<Float>](/documentation/realitykit/ikcomponent/constraint/lookattargetposition)
- [var name: String](/documentation/realitykit/ikcomponent/constraint/name)
- [var offset: Transform](/documentation/realitykit/ikcomponent/constraint/offset)
- [var target: Transform](/documentation/realitykit/ikcomponent/constraint/target)
- [IKComponent.ConstraintCollection](/documentation/realitykit/ikcomponent/constraintcollection)

#### Instance Properties

- [var count: Int](/documentation/realitykit/ikcomponent/constraintcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikcomponent/constraintcollection/isempty)

#### Instance Methods

- [func contains(IKComponent.ConstraintCollection.Element.ID) -> Bool](/documentation/realitykit/ikcomponent/constraintcollection/contains(_:))
- [func set(IKComponent.ConstraintCollection.Element) -> IKComponent.ConstraintCollection.Element?](/documentation/realitykit/ikcomponent/constraintcollection/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/ikcomponent/constraintcollection/subscript(_:))
- [IKResource](/documentation/realitykit/ikresource)

#### Initializers

- [convenience init(rig: IKRig) throws](/documentation/realitykit/ikresource/init(rig:))

#### Instance Properties

- [var solverDefinitions: [IKSolverDefinition]](/documentation/realitykit/ikresource/solverdefinitions)
- [IKSolverDefinition](/documentation/realitykit/iksolverdefinition)

#### Initializers

- [init(id: IKSolverDefinition.ID, rig: IKRig)](/documentation/realitykit/iksolverdefinition/init(id:rig:))

#### Instance Properties

- [let id: IKSolverDefinition.ID](/documentation/realitykit/iksolverdefinition/id)
- [var rigDefinition: IKRig](/documentation/realitykit/iksolverdefinition/rigdefinition)

### Inverse kinematics rigs

- [IKRig](/documentation/realitykit/ikrig)

#### Structures

- [IKRig.Constraint](/documentation/realitykit/ikrig/constraint)

##### Structures

- [IKRig.Constraint.ID](/documentation/realitykit/ikrig/constraint/id-swift.struct)
- [IKRig.Constraint.IKOrientationDemand](/documentation/realitykit/ikrig/constraint/ikorientationdemand)

###### Initializers

- [init()](/documentation/realitykit/ikrig/constraint/ikorientationdemand/init())

###### Instance Properties

- [var influenceDepthMaxJointCount: Int](/documentation/realitykit/ikrig/constraint/ikorientationdemand/influencedepthmaxjointcount)
- [var mode: IKRig.Constraint.IKOrientationDemand.Mode](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.property)
- [var weight: SIMD3<Float>](/documentation/realitykit/ikrig/constraint/ikorientationdemand/weight)

###### Enumerations

- [IKRig.Constraint.IKOrientationDemand.Mode](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum)

###### Enumeration Cases

- [case absoluteLookAt(targetAxis: SIMD3<Float>)](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/absolutelookat(targetaxis:))
- [case additiveLookAt(targetAxis: SIMD3<Float>)](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/additivelookat(targetaxis:))
- [case orientation](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/orientation)
- [IKRig.Constraint.IKPositionDemand](/documentation/realitykit/ikrig/constraint/ikpositiondemand)

###### Initializers

- [init()](/documentation/realitykit/ikrig/constraint/ikpositiondemand/init())

###### Instance Properties

- [var influenceDepthMaxJointCount: Int](/documentation/realitykit/ikrig/constraint/ikpositiondemand/influencedepthmaxjointcount)
- [var mode: IKRig.Constraint.IKPositionDemand.Mode](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.property)
- [var weight: SIMD3<Float>](/documentation/realitykit/ikrig/constraint/ikpositiondemand/weight)

###### Enumerations

- [IKRig.Constraint.IKPositionDemand.Mode](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum)

###### Enumeration Cases

- [case poleVector](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum/polevector)
- [case reach](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum/reach)

##### Instance Properties

- [var id: IKRig.Constraint.ID](/documentation/realitykit/ikrig/constraint/id-swift.property)
- [var jointName: String](/documentation/realitykit/ikrig/constraint/jointname)
- [var name: String](/documentation/realitykit/ikrig/constraint/name)
- [var offset: Transform](/documentation/realitykit/ikrig/constraint/offset)
- [var orientationDemand: IKRig.Constraint.IKOrientationDemand?](/documentation/realitykit/ikrig/constraint/orientationdemand)
- [var positionDemand: IKRig.Constraint.IKPositionDemand?](/documentation/realitykit/ikrig/constraint/positiondemand)

##### Type Methods

- [static func lookAtAbsolute(named: String, on: String, lookingAlong: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/lookatabsolute(named:on:lookingalong:orientationweight:))
- [static func lookAtAdditive(named: String, on: String, lookingAlong: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/lookatadditive(named:on:lookingalong:orientationweight:))
- [static func orient(named: String, on: String, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/orient(named:on:orientationweight:))
- [static func parent(named: String, on: String, positionWeight: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/parent(named:on:positionweight:orientationweight:))
- [static func point(named: String, on: String, positionWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/point(named:on:positionweight:))
- [IKRig.ConstraintsCollection](/documentation/realitykit/ikrig/constraintscollection)

##### Initializers

- [init([IKRig.ConstraintsCollection.Element])](/documentation/realitykit/ikrig/constraintscollection/init(_:))

##### Instance Properties

- [var count: Int](/documentation/realitykit/ikrig/constraintscollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikrig/constraintscollection/isempty)

##### Instance Methods

- [func contains(IKRig.ConstraintsCollection.Element.ID) -> Bool](/documentation/realitykit/ikrig/constraintscollection/contains(_:))
- [func set(IKRig.ConstraintsCollection.Element) -> IKRig.ConstraintsCollection.Element?](/documentation/realitykit/ikrig/constraintscollection/set(_:))

##### Subscripts

- [subscript(_:)](/documentation/realitykit/ikrig/constraintscollection/subscript(_:))
- [IKRig.Joint](/documentation/realitykit/ikrig/joint)

##### Structures

- [IKRig.Joint.ID](/documentation/realitykit/ikrig/joint/id-swift.struct)
- [IKRig.Joint.LimitsDefinition](/documentation/realitykit/ikrig/joint/limitsdefinition)

###### Initializers

- [init(weight: Float, boneAxis: IKRig.Joint.LimitsDefinition.Axis, minimumAngles: SIMD3<Float>, maximumAngles: SIMD3<Float>)](/documentation/realitykit/ikrig/joint/limitsdefinition/init(weight:boneaxis:minimumangles:maximumangles:))

###### Instance Properties

- [var boneAxis: IKRig.Joint.LimitsDefinition.Axis](/documentation/realitykit/ikrig/joint/limitsdefinition/boneaxis)
- [var maximumAngles: SIMD3<Float>](/documentation/realitykit/ikrig/joint/limitsdefinition/maximumangles)
- [var minimumAngles: SIMD3<Float>](/documentation/realitykit/ikrig/joint/limitsdefinition/minimumangles)
- [var weight: Float](/documentation/realitykit/ikrig/joint/limitsdefinition/weight)

###### Enumerations

- [IKRig.Joint.LimitsDefinition.Axis](/documentation/realitykit/ikrig/joint/limitsdefinition/axis)

###### Enumeration Cases

- [case x](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/x)
- [case y](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/y)
- [case z](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/z)

##### Initializers

- [init(name: String, parentID: IKRig.Joint.ID?, restTransform: Transform)](/documentation/realitykit/ikrig/joint/init(name:parentid:resttransform:))

##### Instance Properties

- [var active: Bool](/documentation/realitykit/ikrig/joint/active)
- [var fkWeightPerAxis: SIMD3<Float>](/documentation/realitykit/ikrig/joint/fkweightperaxis)
- [var id: IKRig.Joint.ID](/documentation/realitykit/ikrig/joint/id-swift.property)
- [var limits: IKRig.Joint.LimitsDefinition?](/documentation/realitykit/ikrig/joint/limits)
- [let name: String](/documentation/realitykit/ikrig/joint/name)
- [var parentID: IKRig.Joint.ID?](/documentation/realitykit/ikrig/joint/parentid)
- [var restTransform: Transform](/documentation/realitykit/ikrig/joint/resttransform)
- [var rotationStiffness: SIMD3<Float>](/documentation/realitykit/ikrig/joint/rotationstiffness)
- [IKRig.JointCollection](/documentation/realitykit/ikrig/jointcollection)

##### Instance Properties

- [var count: Int](/documentation/realitykit/ikrig/jointcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikrig/jointcollection/isempty)

##### Instance Methods

- [func contains(IKRig.JointCollection.Element.ID) -> Bool](/documentation/realitykit/ikrig/jointcollection/contains(_:))
- [func forEach(descendantOf: String, inclusive: Bool, update: (inout IKRig.JointCollection.Element) -> Void)](/documentation/realitykit/ikrig/jointcollection/foreach(descendantof:inclusive:update:))
- [func set(IKRig.JointCollection.Element) -> IKRig.JointCollection.Element?](/documentation/realitykit/ikrig/jointcollection/set(_:))

##### Subscripts

- [subscript(_:)](/documentation/realitykit/ikrig/jointcollection/subscript(_:))

#### Initializers

- [init(for: MeshResource.Skeleton) throws](/documentation/realitykit/ikrig/init(for:))

#### Instance Properties

- [var constraints: IKRig.ConstraintsCollection](/documentation/realitykit/ikrig/constraints)
- [var globalFkWeight: Float](/documentation/realitykit/ikrig/globalfkweight)
- [var globalLimitsWeight: Float](/documentation/realitykit/ikrig/globallimitsweight)
- [var joints: IKRig.JointCollection](/documentation/realitykit/ikrig/joints)
- [var maxIterations: Int](/documentation/realitykit/ikrig/maxiterations)
- [IKRig.Joint](/documentation/realitykit/ikrig/joint)

#### Structures

- [IKRig.Joint.ID](/documentation/realitykit/ikrig/joint/id-swift.struct)
- [IKRig.Joint.LimitsDefinition](/documentation/realitykit/ikrig/joint/limitsdefinition)

##### Initializers

- [init(weight: Float, boneAxis: IKRig.Joint.LimitsDefinition.Axis, minimumAngles: SIMD3<Float>, maximumAngles: SIMD3<Float>)](/documentation/realitykit/ikrig/joint/limitsdefinition/init(weight:boneaxis:minimumangles:maximumangles:))

##### Instance Properties

- [var boneAxis: IKRig.Joint.LimitsDefinition.Axis](/documentation/realitykit/ikrig/joint/limitsdefinition/boneaxis)
- [var maximumAngles: SIMD3<Float>](/documentation/realitykit/ikrig/joint/limitsdefinition/maximumangles)
- [var minimumAngles: SIMD3<Float>](/documentation/realitykit/ikrig/joint/limitsdefinition/minimumangles)
- [var weight: Float](/documentation/realitykit/ikrig/joint/limitsdefinition/weight)

##### Enumerations

- [IKRig.Joint.LimitsDefinition.Axis](/documentation/realitykit/ikrig/joint/limitsdefinition/axis)

###### Enumeration Cases

- [case x](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/x)
- [case y](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/y)
- [case z](/documentation/realitykit/ikrig/joint/limitsdefinition/axis/z)

#### Initializers

- [init(name: String, parentID: IKRig.Joint.ID?, restTransform: Transform)](/documentation/realitykit/ikrig/joint/init(name:parentid:resttransform:))

#### Instance Properties

- [var active: Bool](/documentation/realitykit/ikrig/joint/active)
- [var fkWeightPerAxis: SIMD3<Float>](/documentation/realitykit/ikrig/joint/fkweightperaxis)
- [var id: IKRig.Joint.ID](/documentation/realitykit/ikrig/joint/id-swift.property)
- [var limits: IKRig.Joint.LimitsDefinition?](/documentation/realitykit/ikrig/joint/limits)
- [let name: String](/documentation/realitykit/ikrig/joint/name)
- [var parentID: IKRig.Joint.ID?](/documentation/realitykit/ikrig/joint/parentid)
- [var restTransform: Transform](/documentation/realitykit/ikrig/joint/resttransform)
- [var rotationStiffness: SIMD3<Float>](/documentation/realitykit/ikrig/joint/rotationstiffness)
- [IKRig.JointCollection](/documentation/realitykit/ikrig/jointcollection)

#### Instance Properties

- [var count: Int](/documentation/realitykit/ikrig/jointcollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikrig/jointcollection/isempty)

#### Instance Methods

- [func contains(IKRig.JointCollection.Element.ID) -> Bool](/documentation/realitykit/ikrig/jointcollection/contains(_:))
- [func forEach(descendantOf: String, inclusive: Bool, update: (inout IKRig.JointCollection.Element) -> Void)](/documentation/realitykit/ikrig/jointcollection/foreach(descendantof:inclusive:update:))
- [func set(IKRig.JointCollection.Element) -> IKRig.JointCollection.Element?](/documentation/realitykit/ikrig/jointcollection/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/ikrig/jointcollection/subscript(_:))
- [IKRig.Constraint](/documentation/realitykit/ikrig/constraint)

#### Structures

- [IKRig.Constraint.ID](/documentation/realitykit/ikrig/constraint/id-swift.struct)
- [IKRig.Constraint.IKOrientationDemand](/documentation/realitykit/ikrig/constraint/ikorientationdemand)

##### Initializers

- [init()](/documentation/realitykit/ikrig/constraint/ikorientationdemand/init())

##### Instance Properties

- [var influenceDepthMaxJointCount: Int](/documentation/realitykit/ikrig/constraint/ikorientationdemand/influencedepthmaxjointcount)
- [var mode: IKRig.Constraint.IKOrientationDemand.Mode](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.property)
- [var weight: SIMD3<Float>](/documentation/realitykit/ikrig/constraint/ikorientationdemand/weight)

##### Enumerations

- [IKRig.Constraint.IKOrientationDemand.Mode](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum)

###### Enumeration Cases

- [case absoluteLookAt(targetAxis: SIMD3<Float>)](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/absolutelookat(targetaxis:))
- [case additiveLookAt(targetAxis: SIMD3<Float>)](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/additivelookat(targetaxis:))
- [case orientation](/documentation/realitykit/ikrig/constraint/ikorientationdemand/mode-swift.enum/orientation)
- [IKRig.Constraint.IKPositionDemand](/documentation/realitykit/ikrig/constraint/ikpositiondemand)

##### Initializers

- [init()](/documentation/realitykit/ikrig/constraint/ikpositiondemand/init())

##### Instance Properties

- [var influenceDepthMaxJointCount: Int](/documentation/realitykit/ikrig/constraint/ikpositiondemand/influencedepthmaxjointcount)
- [var mode: IKRig.Constraint.IKPositionDemand.Mode](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.property)
- [var weight: SIMD3<Float>](/documentation/realitykit/ikrig/constraint/ikpositiondemand/weight)

##### Enumerations

- [IKRig.Constraint.IKPositionDemand.Mode](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum)

###### Enumeration Cases

- [case poleVector](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum/polevector)
- [case reach](/documentation/realitykit/ikrig/constraint/ikpositiondemand/mode-swift.enum/reach)

#### Instance Properties

- [var id: IKRig.Constraint.ID](/documentation/realitykit/ikrig/constraint/id-swift.property)
- [var jointName: String](/documentation/realitykit/ikrig/constraint/jointname)
- [var name: String](/documentation/realitykit/ikrig/constraint/name)
- [var offset: Transform](/documentation/realitykit/ikrig/constraint/offset)
- [var orientationDemand: IKRig.Constraint.IKOrientationDemand?](/documentation/realitykit/ikrig/constraint/orientationdemand)
- [var positionDemand: IKRig.Constraint.IKPositionDemand?](/documentation/realitykit/ikrig/constraint/positiondemand)

#### Type Methods

- [static func lookAtAbsolute(named: String, on: String, lookingAlong: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/lookatabsolute(named:on:lookingalong:orientationweight:))
- [static func lookAtAdditive(named: String, on: String, lookingAlong: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/lookatadditive(named:on:lookingalong:orientationweight:))
- [static func orient(named: String, on: String, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/orient(named:on:orientationweight:))
- [static func parent(named: String, on: String, positionWeight: SIMD3<Float>, orientationWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/parent(named:on:positionweight:orientationweight:))
- [static func point(named: String, on: String, positionWeight: SIMD3<Float>) -> IKRig.Constraint](/documentation/realitykit/ikrig/constraint/point(named:on:positionweight:))
- [IKRig.ConstraintsCollection](/documentation/realitykit/ikrig/constraintscollection)

#### Initializers

- [init([IKRig.ConstraintsCollection.Element])](/documentation/realitykit/ikrig/constraintscollection/init(_:))

#### Instance Properties

- [var count: Int](/documentation/realitykit/ikrig/constraintscollection/count)
- [var isEmpty: Bool](/documentation/realitykit/ikrig/constraintscollection/isempty)

#### Instance Methods

- [func contains(IKRig.ConstraintsCollection.Element.ID) -> Bool](/documentation/realitykit/ikrig/constraintscollection/contains(_:))
- [func set(IKRig.ConstraintsCollection.Element) -> IKRig.ConstraintsCollection.Element?](/documentation/realitykit/ikrig/constraintscollection/set(_:))

#### Subscripts

- [subscript(_:)](/documentation/realitykit/ikrig/constraintscollection/subscript(_:))

## Physics simulation

- [Collision detection](/documentation/realitykit/physics-collision-detection)

### Collision shapes and groups

- [Simulating physics with collisions in your visionOS app](/documentation/realitykit/simulating-physics-with-collisions-in-your-visionos-app)
- [Configuring Collision in RealityKit](/documentation/realitykit/configuring-collision-in-realitykit)
- [CollisionComponent](/documentation/realitykit/collisioncomponent)

#### Creating the collision component

- [init(shapes: [ShapeResource], mode: CollisionComponent.Mode, filter: CollisionFilter)](/documentation/realitykit/collisioncomponent/init(shapes:mode:filter:))

#### Setting the collision mode

- [var mode: CollisionComponent.Mode](/documentation/realitykit/collisioncomponent/mode-swift.property)

#### Filtering collisions

- [var filter: CollisionFilter](/documentation/realitykit/collisioncomponent/filter)

#### Setting collision shapes

- [var shapes: [ShapeResource]](/documentation/realitykit/collisioncomponent/shapes)

#### Structures

- [CollisionComponent.CollisionOptions](/documentation/realitykit/collisioncomponent/collisionoptions-swift.struct)

##### Type Properties

- [static let fullContactInformation: CollisionComponent.CollisionOptions](/documentation/realitykit/collisioncomponent/collisionoptions-swift.struct/fullcontactinformation)
- [static let none: CollisionComponent.CollisionOptions](/documentation/realitykit/collisioncomponent/collisionoptions-swift.struct/none)
- [static let `static`: CollisionComponent.CollisionOptions](/documentation/realitykit/collisioncomponent/collisionoptions-swift.struct/static)

#### Initializers

- [init(shapes: [ShapeResource], isStatic: Bool, filter: CollisionFilter)](/documentation/realitykit/collisioncomponent/init(shapes:isstatic:filter:))
- [init(shapes: [ShapeResource], mode: CollisionComponent.Mode, collisionOptions: CollisionComponent.CollisionOptions, filter: CollisionFilter)](/documentation/realitykit/collisioncomponent/init(shapes:mode:collisionoptions:filter:))

#### Instance Properties

- [var collisionOptions: CollisionComponent.CollisionOptions](/documentation/realitykit/collisioncomponent/collisionoptions-swift.property)
- [var isStatic: Bool](/documentation/realitykit/collisioncomponent/isstatic)

#### Enumerations

- [CollisionComponent.Mode](/documentation/realitykit/collisioncomponent/mode-swift.enum)

##### Collision modes

- [case `default`](/documentation/realitykit/collisioncomponent/mode-swift.enum/default)
- [case trigger](/documentation/realitykit/collisioncomponent/mode-swift.enum/trigger)

##### Enumeration Cases

- [case colliding](/documentation/realitykit/collisioncomponent/mode-swift.enum/colliding)
- [CollisionComponent.Mode](/documentation/realitykit/collisioncomponent/mode-swift.enum)

#### Collision modes

- [case `default`](/documentation/realitykit/collisioncomponent/mode-swift.enum/default)
- [case trigger](/documentation/realitykit/collisioncomponent/mode-swift.enum/trigger)

#### Enumeration Cases

- [case colliding](/documentation/realitykit/collisioncomponent/mode-swift.enum/colliding)
- [ShapeResource](/documentation/realitykit/shaperesource)

#### Transforming a shape

- [func offsetBy(rotation: simd_quatf) -> ShapeResource](/documentation/realitykit/shaperesource/offsetby(rotation:))
- [func offsetBy(translation: SIMD3<Float>) -> ShapeResource](/documentation/realitykit/shaperesource/offsetby(translation:))
- [func offsetBy(rotation: simd_quatf, translation: SIMD3<Float>) -> ShapeResource](/documentation/realitykit/shaperesource/offsetby(rotation:translation:))

#### Generating boxes

- [static func generateBox(size: SIMD3<Float>) -> ShapeResource](/documentation/realitykit/shaperesource/generatebox(size:))
- [static func generateBox(width: Float, height: Float, depth: Float) -> ShapeResource](/documentation/realitykit/shaperesource/generatebox(width:height:depth:))

#### Generating spheres

- [static func generateSphere(radius: Float) -> ShapeResource](/documentation/realitykit/shaperesource/generatesphere(radius:))

#### Generating capsules

- [static func generateCapsule(height: Float, radius: Float) -> ShapeResource](/documentation/realitykit/shaperesource/generatecapsule(height:radius:))

#### Generating convex shapes

- [static func generateConvex(from: [SIMD3<Float>]) -> ShapeResource](/documentation/realitykit/shaperesource/generateconvex(from:)-6q0wj)
- [static func generateConvex(from: MeshResource) -> ShapeResource](/documentation/realitykit/shaperesource/generateconvex(from:)-53jm9)

#### Operators

- [static func == (ShapeResource, ShapeResource) -> Bool](/documentation/realitykit/shaperesource/==(_:_:))

#### Instance Properties

- [var bounds: BoundingBox](/documentation/realitykit/shaperesource/bounds)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/shaperesource/hash(into:))

#### Type Methods

- [static generateConvex(from:)](/documentation/realitykit/shaperesource/generateconvex(from:))
- [static generateStaticMesh(from:)](/documentation/realitykit/shaperesource/generatestaticmesh(from:))
- [static func generateStaticMesh(positions: [SIMD3<Float>], faceIndices: [UInt16]) async throws -> ShapeResource](/documentation/realitykit/shaperesource/generatestaticmesh(positions:faceindices:))
- [ShapeResourceError](/documentation/realitykit/shaperesourceerror)

#### Enumeration Cases

- [case convexPolyhedronGenerationFailed](/documentation/realitykit/shaperesourceerror/convexpolyhedrongenerationfailed)
- [case staticMeshGenerationFailed](/documentation/realitykit/shaperesourceerror/staticmeshgenerationfailed)
- [CollisionGroup](/documentation/realitykit/collisiongroup)

#### Standard collision groups

- [static let `default`: CollisionGroup](/documentation/realitykit/collisiongroup/default)
- [static let all: CollisionGroup](/documentation/realitykit/collisiongroup/all)
- [static let sceneUnderstanding: CollisionGroup](/documentation/realitykit/collisiongroup/sceneunderstanding)

#### Creating a collision group

- [init(rawValue: UInt32)](/documentation/realitykit/collisiongroup/init(rawvalue:))
- [CollisionFilter](/documentation/realitykit/collisionfilter)

#### Creating a collision filter

- [init(group: CollisionGroup, mask: CollisionGroup)](/documentation/realitykit/collisionfilter/init(group:mask:))
- [static let `default`: CollisionFilter](/documentation/realitykit/collisionfilter/default)
- [static let sensor: CollisionFilter](/documentation/realitykit/collisionfilter/sensor)

#### Customizing groups

- [var group: CollisionGroup](/documentation/realitykit/collisionfilter/group)
- [var mask: CollisionGroup](/documentation/realitykit/collisionfilter/mask)
- [TriggerVolume](/documentation/realitykit/triggervolume)

#### Creating a trigger volume

- [init()](/documentation/realitykit/triggervolume/init())
- [convenience init(shape: ShapeResource, filter: CollisionFilter)](/documentation/realitykit/triggervolume/init(shape:filter:))
- [init(shapes: [ShapeResource], filter: CollisionFilter)](/documentation/realitykit/triggervolume/init(shapes:filter:))

#### Detecting collisions


### Collision-related notifications

- [CollisionEvents](/documentation/realitykit/collisionevents)

#### Detecting collisions

- [CollisionEvents.Began](/documentation/realitykit/collisionevents/began)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/began/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/began/entityb)

##### Characterizing the collision

- [let impulse: Float](/documentation/realitykit/collisionevents/began/impulse)
- [let position: SIMD3<Float>](/documentation/realitykit/collisionevents/began/position)

##### Instance Properties

- [var contacts: [Contact]](/documentation/realitykit/collisionevents/began/contacts)
- [var impulseDirection: SIMD3<Float>](/documentation/realitykit/collisionevents/began/impulsedirection)
- [var penetrationDistance: Float](/documentation/realitykit/collisionevents/began/penetrationdistance)
- [CollisionEvents.Updated](/documentation/realitykit/collisionevents/updated)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/updated/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/updated/entityb)

##### Characterizing the collision

- [let impulse: Float](/documentation/realitykit/collisionevents/updated/impulse)
- [let position: SIMD3<Float>](/documentation/realitykit/collisionevents/updated/position)

##### Instance Properties

- [var contacts: [Contact]](/documentation/realitykit/collisionevents/updated/contacts)
- [var impulseDirection: SIMD3<Float>](/documentation/realitykit/collisionevents/updated/impulsedirection)
- [var penetrationDistance: Float](/documentation/realitykit/collisionevents/updated/penetrationdistance)
- [CollisionEvents.Ended](/documentation/realitykit/collisionevents/ended)

##### Getting the involved entities

- [let entityA: Entity](/documentation/realitykit/collisionevents/ended/entitya)
- [let entityB: Entity](/documentation/realitykit/collisionevents/ended/entityb)
- [Contact](/documentation/realitykit/contact)

#### Instance Properties

- [let impulse: Float](/documentation/realitykit/contact/impulse)
- [let impulseDirection: SIMD3<Float>](/documentation/realitykit/contact/impulsedirection)
- [let normal: SIMD3<Float>](/documentation/realitykit/contact/normal)
- [let penetrationDistance: Float](/documentation/realitykit/contact/penetrationdistance)
- [let point: SIMD3<Float>](/documentation/realitykit/contact/point)

### Ray casting

- [CollisionCastHit](/documentation/realitykit/collisioncasthit)

#### Getting the entity

- [var entity: Entity](/documentation/realitykit/collisioncasthit/entity)

#### Characterizing the collision cast hit

- [var position: SIMD3<Float>](/documentation/realitykit/collisioncasthit/position)
- [var normal: SIMD3<Float>](/documentation/realitykit/collisioncasthit/normal)
- [var distance: Float](/documentation/realitykit/collisioncasthit/distance)

#### Structures

- [CollisionCastHit.TriangleHit](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct)

##### Instance Properties

- [var faceIndex: Int](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct/faceindex)
- [var uv: SIMD2<Float>](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct/uv)

#### Instance Properties

- [var shapeIndex: Int](/documentation/realitykit/collisioncasthit/shapeindex)
- [var triangleHit: CollisionCastHit.TriangleHit?](/documentation/realitykit/collisioncasthit/trianglehit-swift.property)
- [CollisionCastHit.TriangleHit](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct)

#### Instance Properties

- [var faceIndex: Int](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct/faceindex)
- [var uv: SIMD2<Float>](/documentation/realitykit/collisioncasthit/trianglehit-swift.struct/uv)
- [CollisionCastQueryType](/documentation/realitykit/collisioncastquerytype)

#### Collision cast queries

- [case nearest](/documentation/realitykit/collisioncastquerytype/nearest)
- [case all](/documentation/realitykit/collisioncastquerytype/all)
- [case any](/documentation/realitykit/collisioncastquerytype/any)
- [PixelCastHit](/documentation/realitykit/pixelcasthit)

#### Instance Properties

- [var barycentric: SIMD3<Float>?](/documentation/realitykit/pixelcasthit/barycentric)
- [var entity: Entity](/documentation/realitykit/pixelcasthit/entity)
- [var instance: UInt32](/documentation/realitykit/pixelcasthit/instance)
- [var meshPart: UInt64](/documentation/realitykit/pixelcasthit/meshpart)
- [var normal: SIMD3<Float>](/documentation/realitykit/pixelcasthit/normal)
- [var position: SIMD3<Float>](/documentation/realitykit/pixelcasthit/position)
- [var primitive: UInt32](/documentation/realitykit/pixelcasthit/primitive)

### Entity compliance

- [HasCollision](/documentation/realitykit/hascollision)

#### Getting the component

- [var collision: CollisionComponent?](/documentation/realitykit/hascollision/collision)
- [Simulations and motion](/documentation/realitykit/physics-simulations-and-motion)

### Simulation setup

- [Designing scene hierarchies for efficient physics simulation](/documentation/realitykit/designing-scene-hierarchies-for-efficient-physics-simulation)
- [Handling different-sized objects in physics simulations](/documentation/realitykit/handling-different-sized-objects-in-physics-simulations)
- [PhysicsSimulationComponent](/documentation/realitykit/physicssimulationcomponent)

#### Structures

- [PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.struct)

##### Type Properties

- [static let all: PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.struct/all)
- [static let none: PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.struct/none)
- [static let reportKinematicVsKinematic: PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.struct/reportkinematicvskinematic)
- [static let reportKinematicVsStatic: PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.struct/reportkinematicvsstatic)
- [PhysicsSimulationComponent.SolverIterations](/documentation/realitykit/physicssimulationcomponent/solveriterations-swift.struct)

##### Initializers

- [init(positionIterations: Int, velocityIterations: Int)](/documentation/realitykit/physicssimulationcomponent/solveriterations-swift.struct/init(positioniterations:velocityiterations:))

##### Instance Properties

- [var positionIterations: Int](/documentation/realitykit/physicssimulationcomponent/solveriterations-swift.struct/positioniterations)
- [var velocityIterations: Int](/documentation/realitykit/physicssimulationcomponent/solveriterations-swift.struct/velocityiterations)

#### Initializers

- [init()](/documentation/realitykit/physicssimulationcomponent/init())

#### Instance Properties

- [var clock: CMClockOrTimebase](/documentation/realitykit/physicssimulationcomponent/clock)
- [var collisionOptions: PhysicsSimulationComponent.CollisionOptions](/documentation/realitykit/physicssimulationcomponent/collisionoptions-swift.property)
- [var gravity: SIMD3<Float>](/documentation/realitykit/physicssimulationcomponent/gravity)
- [var solverIterations: PhysicsSimulationComponent.SolverIterations](/documentation/realitykit/physicssimulationcomponent/solveriterations-swift.property)

#### Type Methods

- [static func nearestSimulationEntity(for: Entity) -> Entity?](/documentation/realitykit/physicssimulationcomponent/nearestsimulationentity(for:))

### Simulation-related notifications

- [PhysicsSimulationEvents](/documentation/realitykit/physicssimulationevents)

#### Structures

- [PhysicsSimulationEvents.DidSimulate](/documentation/realitykit/physicssimulationevents/didsimulate)

##### Instance Properties

- [let deltaTime: TimeInterval](/documentation/realitykit/physicssimulationevents/didsimulate/deltatime)
- [let simulationEntity: Entity](/documentation/realitykit/physicssimulationevents/didsimulate/simulationentity)
- [let simulationRootEntity: Entity?](/documentation/realitykit/physicssimulationevents/didsimulate/simulationrootentity)
- [PhysicsSimulationEvents.WillSimulate](/documentation/realitykit/physicssimulationevents/willsimulate)

##### Instance Properties

- [let deltaTime: TimeInterval](/documentation/realitykit/physicssimulationevents/willsimulate/deltatime)
- [let simulationEntity: Entity](/documentation/realitykit/physicssimulationevents/willsimulate/simulationentity)
- [let simulationRootEntity: Entity?](/documentation/realitykit/physicssimulationevents/willsimulate/simulationrootentity)

### Physical properties

- [PhysicsBodyComponent](/documentation/realitykit/physicsbodycomponent)

#### Creating a physics body component

- [init()](/documentation/realitykit/physicsbodycomponent/init())
- [init(massProperties: PhysicsMassProperties, material: PhysicsMaterialResource?, mode: PhysicsBodyMode)](/documentation/realitykit/physicsbodycomponent/init(massproperties:material:mode:))
- [init(shapes: [ShapeResource], density: Float, material: PhysicsMaterialResource?, mode: PhysicsBodyMode)](/documentation/realitykit/physicsbodycomponent/init(shapes:density:material:mode:))
- [init(shapes: [ShapeResource], mass: Float, material: PhysicsMaterialResource?, mode: PhysicsBodyMode)](/documentation/realitykit/physicsbodycomponent/init(shapes:mass:material:mode:))

#### Detecting collisions

- [var isContinuousCollisionDetectionEnabled: Bool](/documentation/realitykit/physicsbodycomponent/iscontinuouscollisiondetectionenabled)

#### Locking movement

- [var isRotationLocked: (x: Bool, y: Bool, z: Bool)](/documentation/realitykit/physicsbodycomponent/isrotationlocked)
- [var isTranslationLocked: (x: Bool, y: Bool, z: Bool)](/documentation/realitykit/physicsbodycomponent/istranslationlocked)

#### Setting the mode

- [var mode: PhysicsBodyMode](/documentation/realitykit/physicsbodycomponent/mode)

#### Setting material properties

- [var material: PhysicsMaterialResource](/documentation/realitykit/physicsbodycomponent/material)

#### Setting mass properties

- [var massProperties: PhysicsMassProperties](/documentation/realitykit/physicsbodycomponent/massproperties)

#### Operators

- [static func == (PhysicsBodyComponent, PhysicsBodyComponent) -> Bool](/documentation/realitykit/physicsbodycomponent/==(_:_:))

#### Instance Properties

- [var angularDamping: Float](/documentation/realitykit/physicsbodycomponent/angulardamping)
- [var isAffectedByGravity: Bool](/documentation/realitykit/physicsbodycomponent/isaffectedbygravity)
- [var linearDamping: Float](/documentation/realitykit/physicsbodycomponent/lineardamping)
- [PhysicsMaterialResource](/documentation/realitykit/physicsmaterialresource)

#### Using the default material resource

- [static let `default`: PhysicsMaterialResource](/documentation/realitykit/physicsmaterialresource/default)

#### Creating a custom material resource

- [static func generate(friction: Float, restitution: Float) -> PhysicsMaterialResource](/documentation/realitykit/physicsmaterialresource/generate(friction:restitution:))
- [static func generate(staticFriction: Float, dynamicFriction: Float, restitution: Float) -> PhysicsMaterialResource](/documentation/realitykit/physicsmaterialresource/generate(staticfriction:dynamicfriction:restitution:))
- [PhysicsBodyMode](/documentation/realitykit/physicsbodymode)

#### Setting the physics body mode

- [case `static`](/documentation/realitykit/physicsbodymode/static)
- [case kinematic](/documentation/realitykit/physicsbodymode/kinematic)
- [case dynamic](/documentation/realitykit/physicsbodymode/dynamic)
- [PhysicsMassProperties](/documentation/realitykit/physicsmassproperties)

#### Using default mass properties

- [static let `default`: PhysicsMassProperties](/documentation/realitykit/physicsmassproperties/default)

#### Creating custom mass properties

- [init()](/documentation/realitykit/physicsmassproperties/init())
- [init(mass: Float, inertia: SIMD3<Float>, centerOfMass: (position: SIMD3<Float>, orientation: simd_quatf))](/documentation/realitykit/physicsmassproperties/init(mass:inertia:centerofmass:))
- [init(shape: ShapeResource, density: Float)](/documentation/realitykit/physicsmassproperties/init(shape:density:))
- [init(shape: ShapeResource, mass: Float)](/documentation/realitykit/physicsmassproperties/init(shape:mass:))

#### Getting mass properties

- [var mass: Float](/documentation/realitykit/physicsmassproperties/mass)
- [var inertia: SIMD3<Float>](/documentation/realitykit/physicsmassproperties/inertia)
- [var centerOfMass: (position: SIMD3<Float>, orientation: simd_quatf)](/documentation/realitykit/physicsmassproperties/centerofmass)

#### Operators

- [static func == (PhysicsMassProperties, PhysicsMassProperties) -> Bool](/documentation/realitykit/physicsmassproperties/==(_:_:))

### Physics motion

- [PhysicsMotionComponent](/documentation/realitykit/physicsmotioncomponent)

#### Creating the motion component

- [init()](/documentation/realitykit/physicsmotioncomponent/init())
- [init(linearVelocity: SIMD3<Float>, angularVelocity: SIMD3<Float>)](/documentation/realitykit/physicsmotioncomponent/init(linearvelocity:angularvelocity:))

#### Setting velocity

- [var angularVelocity: SIMD3<Float>](/documentation/realitykit/physicsmotioncomponent/angularvelocity)
- [var linearVelocity: SIMD3<Float>](/documentation/realitykit/physicsmotioncomponent/linearvelocity)
- [ImpulseAction](/documentation/realitykit/impulseaction)

#### Initializers

- [init(targetEntity: ActionEntityResolution, linearImpulse: SIMD3<Float>)](/documentation/realitykit/impulseaction/init(targetentity:linearimpulse:))

#### Instance Properties

- [var animatedValueType: (any AnimatableData.Type)?](/documentation/realitykit/impulseaction/animatedvaluetype)
- [var linearImpulse: SIMD3<Float>](/documentation/realitykit/impulseaction/linearimpulse)
- [var targetEntity: ActionEntityResolution](/documentation/realitykit/impulseaction/targetentity)

### Particle simulation

- [Simulating particles in your visionOS app](/documentation/realitykit/simulating-particles-in-your-visionos-app)
- [ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent)

#### Structures

- [ParticleEmitterComponent.ParticleEmitter](/documentation/realitykit/particleemittercomponent/particleemitter)

##### Structures

- [ParticleEmitterComponent.ParticleEmitter.ImageSequence](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct)

###### Initializers

- [init()](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/init())

###### Instance Properties

- [var animationMode: ParticleEmitterComponent.ParticleEmitter.ImageSequence.AnimationRepeatMode](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationmode)
- [var columnCount: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/columncount)
- [var frameRate: Float](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/framerate)
- [var frameRateVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/frameratevariation)
- [var initialFrame: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/initialframe)
- [var initialFrameVariation: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/initialframevariation)
- [var rowCount: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/rowcount)

###### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.ImageSequence.AnimationRepeatMode](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode)

###### Enumeration Cases

- [case autoReverse](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/autoreverse)
- [case looping](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/looping)
- [case playOnce](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/playonce)

##### Initializers

- [init()](/documentation/realitykit/particleemittercomponent/particleemitter/init())

##### Instance Properties

- [var acceleration: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/acceleration)
- [var angle: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angle)
- [var angleVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/anglevariation)
- [var angularSpeed: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angularspeed)
- [var angularSpeedVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angularspeedvariation)
- [var attractionCenter: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/attractioncenter)
- [var attractionStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/attractionstrength)
- [var billboardMode: ParticleEmitterComponent.ParticleEmitter.BillboardMode](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.property)
- [var birthRate: Float](/documentation/realitykit/particleemittercomponent/particleemitter/birthrate)
- [var birthRateVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/birthratevariation)
- [var blendMode: ParticleEmitterComponent.ParticleEmitter.BlendMode](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.property)
- [var color: ParticleEmitterComponent.ParticleEmitter.ParticleColor](/documentation/realitykit/particleemittercomponent/particleemitter/color-swift.property)
- [var colorEvolutionPower: Float](/documentation/realitykit/particleemittercomponent/particleemitter/colorevolutionpower)
- [var dampingFactor: Float](/documentation/realitykit/particleemittercomponent/particleemitter/dampingfactor)
- [var image: TextureResource?](/documentation/realitykit/particleemittercomponent/particleemitter/image)
- [var imageSequence: ParticleEmitterComponent.ParticleEmitter.ImageSequence?](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.property)
- [var isLightingEnabled: Bool](/documentation/realitykit/particleemittercomponent/particleemitter/islightingenabled)
- [var lifeSpan: Double](/documentation/realitykit/particleemittercomponent/particleemitter/lifespan)
- [var lifeSpanVariation: Double](/documentation/realitykit/particleemittercomponent/particleemitter/lifespanvariation)
- [var mass: Float](/documentation/realitykit/particleemittercomponent/particleemitter/mass)
- [var massVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/massvariation)
- [var noiseAnimationSpeed: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noiseanimationspeed)
- [var noiseScale: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noisescale)
- [var noiseStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noisestrength)
- [var opacityCurve: ParticleEmitterComponent.ParticleEmitter.OpacityCurve](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.property)
- [var size: Float](/documentation/realitykit/particleemittercomponent/particleemitter/size)
- [var sizeMultiplierAtEndOfLifespan: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizemultiplieratendoflifespan)
- [var sizeMultiplierAtEndOfLifespanPower: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizemultiplieratendoflifespanpower)
- [var sizeVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizevariation)
- [var sortOrder: ParticleEmitterComponent.ParticleEmitter.SortOrder](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.property)
- [var spreadingAngle: Float](/documentation/realitykit/particleemittercomponent/particleemitter/spreadingangle)
- [var stretchFactor: Float](/documentation/realitykit/particleemittercomponent/particleemitter/stretchfactor)
- [var vortexDirection: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/vortexdirection)
- [var vortexStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/vortexstrength)

##### Type Aliases

- [ParticleEmitterComponent.ParticleEmitter.Color](/documentation/realitykit/particleemittercomponent/particleemitter/color-swift.typealias)

##### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.BillboardMode](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum)

###### Enumeration Cases

- [case billboard](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/billboard)
- [case billboardYAligned](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/billboardyaligned)
- [case free(axis: SIMD3<Float>, variation: Float)](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/free(axis:variation:))
- [ParticleEmitterComponent.ParticleEmitter.BlendMode](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum)

###### Enumeration Cases

- [case additive](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/additive)
- [case alpha](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/alpha)
- [case opaque](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/opaque)
- [ParticleEmitterComponent.ParticleEmitter.OpacityCurve](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum)

###### Enumeration Cases

- [case constant](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/constant)
- [case easeFadeIn](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/easefadein)
- [case easeFadeOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/easefadeout)
- [case gradualFadeInOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/gradualfadeinout)
- [case linearFadeIn](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/linearfadein)
- [case linearFadeOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/linearfadeout)
- [case quickFadeInOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/quickfadeinout)
- [ParticleEmitterComponent.ParticleEmitter.ParticleColor](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor)

###### Enumeration Cases

- [case constant(ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/constant(_:))
- [case evolving(start: ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue, end: ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/evolving(start:end:))

###### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue)

###### Enumeration Cases

- [case random(a: ParticleEmitterComponent.ParticleEmitter.Color, b: ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/random(a:b:)-1muv6)
- [case random(a: ParticleEmitterComponent.ParticleEmitter.Color, b: ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/random(a:b:)-6g22v)
- [case single(ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/single(_:)-58m53)
- [case single(ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/single(_:)-65g3i)
- [ParticleEmitterComponent.ParticleEmitter.SortOrder](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum)

###### Enumeration Cases

- [case decreasingAge](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingage)
- [case decreasingDepth](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingdepth)
- [case decreasingID](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingid)
- [case increasingAge](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingage)
- [case increasingDepth](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingdepth)
- [case increasingID](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingid)
- [case unsorted](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/unsorted)
- [ParticleEmitterComponent.Presets](/documentation/realitykit/particleemittercomponent/presets)

##### Type Properties

- [static var fireworks: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/fireworks)
- [static var impact: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/impact)
- [static var magic: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/magic)
- [static var rain: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/rain)
- [static var snow: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/snow)
- [static var sparks: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/sparks)

#### Initializers

- [init()](/documentation/realitykit/particleemittercomponent/init())

#### Instance Properties

- [var birthDirection: ParticleEmitterComponent.BirthDirection](/documentation/realitykit/particleemittercomponent/birthdirection-swift.property)
- [var birthLocation: ParticleEmitterComponent.BirthLocation](/documentation/realitykit/particleemittercomponent/birthlocation-swift.property)
- [var burstCount: Int](/documentation/realitykit/particleemittercomponent/burstcount)
- [var burstCountVariation: Int](/documentation/realitykit/particleemittercomponent/burstcountvariation)
- [var emissionDirection: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/emissiondirection)
- [var emitterShape: ParticleEmitterComponent.EmitterShape](/documentation/realitykit/particleemittercomponent/emittershape-swift.property)
- [var emitterShapeSize: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/emittershapesize)
- [var fieldSimulationSpace: ParticleEmitterComponent.SimulationSpace](/documentation/realitykit/particleemittercomponent/fieldsimulationspace)
- [var isEmitting: Bool](/documentation/realitykit/particleemittercomponent/isemitting)
- [var mainEmitter: ParticleEmitterComponent.ParticleEmitter](/documentation/realitykit/particleemittercomponent/mainemitter)
- [var particlesInheritTransform: Bool](/documentation/realitykit/particleemittercomponent/particlesinherittransform)
- [var radialAmount: Float](/documentation/realitykit/particleemittercomponent/radialamount)
- [var simulationState: ParticleEmitterComponent.SimulationState](/documentation/realitykit/particleemittercomponent/simulationstate-swift.property)
- [var spawnInheritsParentColor: Bool](/documentation/realitykit/particleemittercomponent/spawninheritsparentcolor)
- [var spawnOccasion: ParticleEmitterComponent.SpawnOccasion](/documentation/realitykit/particleemittercomponent/spawnoccasion-swift.property)
- [var spawnSpreadFactor: Float](/documentation/realitykit/particleemittercomponent/spawnspreadfactor)
- [var spawnSpreadFactorVariation: Float](/documentation/realitykit/particleemittercomponent/spawnspreadfactorvariation)
- [var spawnVelocityFactor: Float](/documentation/realitykit/particleemittercomponent/spawnvelocityfactor)
- [var spawnedEmitter: ParticleEmitterComponent.ParticleEmitter?](/documentation/realitykit/particleemittercomponent/spawnedemitter)
- [var speed: Float](/documentation/realitykit/particleemittercomponent/speed)
- [var speedVariation: Float](/documentation/realitykit/particleemittercomponent/speedvariation)
- [var timing: ParticleEmitterComponent.Timing](/documentation/realitykit/particleemittercomponent/timing-swift.property)
- [var torusInnerRadius: Float](/documentation/realitykit/particleemittercomponent/torusinnerradius)

#### Instance Methods

- [func burst()](/documentation/realitykit/particleemittercomponent/burst())
- [func restart()](/documentation/realitykit/particleemittercomponent/restart())

#### Enumerations

- [ParticleEmitterComponent.BirthDirection](/documentation/realitykit/particleemittercomponent/birthdirection-swift.enum)

##### Enumeration Cases

- [case local](/documentation/realitykit/particleemittercomponent/birthdirection-swift.enum/local)
- [case normal](/documentation/realitykit/particleemittercomponent/birthdirection-swift.enum/normal)
- [case world](/documentation/realitykit/particleemittercomponent/birthdirection-swift.enum/world)
- [ParticleEmitterComponent.BirthLocation](/documentation/realitykit/particleemittercomponent/birthlocation-swift.enum)

##### Enumeration Cases

- [case surface](/documentation/realitykit/particleemittercomponent/birthlocation-swift.enum/surface)
- [case vertices(count: SIMD3<UInt>)](/documentation/realitykit/particleemittercomponent/birthlocation-swift.enum/vertices(count:))
- [case volume](/documentation/realitykit/particleemittercomponent/birthlocation-swift.enum/volume)
- [ParticleEmitterComponent.EmitterShape](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum)

##### Enumeration Cases

- [case box](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/box)
- [case cone](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/cone)
- [case cylinder](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/cylinder)
- [case plane](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/plane)
- [case point](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/point)
- [case sphere](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/sphere)
- [case torus](/documentation/realitykit/particleemittercomponent/emittershape-swift.enum/torus)
- [ParticleEmitterComponent.SimulationSpace](/documentation/realitykit/particleemittercomponent/simulationspace)

##### Enumeration Cases

- [case global](/documentation/realitykit/particleemittercomponent/simulationspace/global)
- [case local](/documentation/realitykit/particleemittercomponent/simulationspace/local)
- [ParticleEmitterComponent.SimulationState](/documentation/realitykit/particleemittercomponent/simulationstate-swift.enum)

##### Enumeration Cases

- [case pause](/documentation/realitykit/particleemittercomponent/simulationstate-swift.enum/pause)
- [case play](/documentation/realitykit/particleemittercomponent/simulationstate-swift.enum/play)
- [case stop](/documentation/realitykit/particleemittercomponent/simulationstate-swift.enum/stop)
- [ParticleEmitterComponent.SpawnOccasion](/documentation/realitykit/particleemittercomponent/spawnoccasion-swift.enum)

##### Enumeration Cases

- [case onBirth](/documentation/realitykit/particleemittercomponent/spawnoccasion-swift.enum/onbirth)
- [case onDeath](/documentation/realitykit/particleemittercomponent/spawnoccasion-swift.enum/ondeath)
- [case onUpdate](/documentation/realitykit/particleemittercomponent/spawnoccasion-swift.enum/onupdate)
- [ParticleEmitterComponent.Timing](/documentation/realitykit/particleemittercomponent/timing-swift.enum)

##### Structures

- [ParticleEmitterComponent.Timing.VariableDuration](/documentation/realitykit/particleemittercomponent/timing-swift.enum/variableduration)

###### Initializers

- [init(duration: TimeInterval, variation: TimeInterval?)](/documentation/realitykit/particleemittercomponent/timing-swift.enum/variableduration/init(duration:variation:))

###### Instance Properties

- [let duration: TimeInterval](/documentation/realitykit/particleemittercomponent/timing-swift.enum/variableduration/duration)
- [let variation: TimeInterval?](/documentation/realitykit/particleemittercomponent/timing-swift.enum/variableduration/variation)

##### Enumeration Cases

- [case once(warmUp: TimeInterval?, emit: ParticleEmitterComponent.Timing.VariableDuration)](/documentation/realitykit/particleemittercomponent/timing-swift.enum/once(warmup:emit:))
- [case repeating(warmUp: TimeInterval?, emit: ParticleEmitterComponent.Timing.VariableDuration, idle: ParticleEmitterComponent.Timing.VariableDuration?)](/documentation/realitykit/particleemittercomponent/timing-swift.enum/repeating(warmup:emit:idle:))
- [ParticleEmitterComponent.ParticleEmitter](/documentation/realitykit/particleemittercomponent/particleemitter)

#### Structures

- [ParticleEmitterComponent.ParticleEmitter.ImageSequence](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct)

##### Initializers

- [init()](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/init())

##### Instance Properties

- [var animationMode: ParticleEmitterComponent.ParticleEmitter.ImageSequence.AnimationRepeatMode](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationmode)
- [var columnCount: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/columncount)
- [var frameRate: Float](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/framerate)
- [var frameRateVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/frameratevariation)
- [var initialFrame: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/initialframe)
- [var initialFrameVariation: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/initialframevariation)
- [var rowCount: Int](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/rowcount)

##### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.ImageSequence.AnimationRepeatMode](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode)

###### Enumeration Cases

- [case autoReverse](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/autoreverse)
- [case looping](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/looping)
- [case playOnce](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.struct/animationrepeatmode/playonce)

#### Initializers

- [init()](/documentation/realitykit/particleemittercomponent/particleemitter/init())

#### Instance Properties

- [var acceleration: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/acceleration)
- [var angle: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angle)
- [var angleVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/anglevariation)
- [var angularSpeed: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angularspeed)
- [var angularSpeedVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/angularspeedvariation)
- [var attractionCenter: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/attractioncenter)
- [var attractionStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/attractionstrength)
- [var billboardMode: ParticleEmitterComponent.ParticleEmitter.BillboardMode](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.property)
- [var birthRate: Float](/documentation/realitykit/particleemittercomponent/particleemitter/birthrate)
- [var birthRateVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/birthratevariation)
- [var blendMode: ParticleEmitterComponent.ParticleEmitter.BlendMode](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.property)
- [var color: ParticleEmitterComponent.ParticleEmitter.ParticleColor](/documentation/realitykit/particleemittercomponent/particleemitter/color-swift.property)
- [var colorEvolutionPower: Float](/documentation/realitykit/particleemittercomponent/particleemitter/colorevolutionpower)
- [var dampingFactor: Float](/documentation/realitykit/particleemittercomponent/particleemitter/dampingfactor)
- [var image: TextureResource?](/documentation/realitykit/particleemittercomponent/particleemitter/image)
- [var imageSequence: ParticleEmitterComponent.ParticleEmitter.ImageSequence?](/documentation/realitykit/particleemittercomponent/particleemitter/imagesequence-swift.property)
- [var isLightingEnabled: Bool](/documentation/realitykit/particleemittercomponent/particleemitter/islightingenabled)
- [var lifeSpan: Double](/documentation/realitykit/particleemittercomponent/particleemitter/lifespan)
- [var lifeSpanVariation: Double](/documentation/realitykit/particleemittercomponent/particleemitter/lifespanvariation)
- [var mass: Float](/documentation/realitykit/particleemittercomponent/particleemitter/mass)
- [var massVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/massvariation)
- [var noiseAnimationSpeed: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noiseanimationspeed)
- [var noiseScale: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noisescale)
- [var noiseStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/noisestrength)
- [var opacityCurve: ParticleEmitterComponent.ParticleEmitter.OpacityCurve](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.property)
- [var size: Float](/documentation/realitykit/particleemittercomponent/particleemitter/size)
- [var sizeMultiplierAtEndOfLifespan: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizemultiplieratendoflifespan)
- [var sizeMultiplierAtEndOfLifespanPower: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizemultiplieratendoflifespanpower)
- [var sizeVariation: Float](/documentation/realitykit/particleemittercomponent/particleemitter/sizevariation)
- [var sortOrder: ParticleEmitterComponent.ParticleEmitter.SortOrder](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.property)
- [var spreadingAngle: Float](/documentation/realitykit/particleemittercomponent/particleemitter/spreadingangle)
- [var stretchFactor: Float](/documentation/realitykit/particleemittercomponent/particleemitter/stretchfactor)
- [var vortexDirection: SIMD3<Float>](/documentation/realitykit/particleemittercomponent/particleemitter/vortexdirection)
- [var vortexStrength: Float](/documentation/realitykit/particleemittercomponent/particleemitter/vortexstrength)

#### Type Aliases

- [ParticleEmitterComponent.ParticleEmitter.Color](/documentation/realitykit/particleemittercomponent/particleemitter/color-swift.typealias)

#### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.BillboardMode](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum)

##### Enumeration Cases

- [case billboard](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/billboard)
- [case billboardYAligned](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/billboardyaligned)
- [case free(axis: SIMD3<Float>, variation: Float)](/documentation/realitykit/particleemittercomponent/particleemitter/billboardmode-swift.enum/free(axis:variation:))
- [ParticleEmitterComponent.ParticleEmitter.BlendMode](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum)

##### Enumeration Cases

- [case additive](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/additive)
- [case alpha](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/alpha)
- [case opaque](/documentation/realitykit/particleemittercomponent/particleemitter/blendmode-swift.enum/opaque)
- [ParticleEmitterComponent.ParticleEmitter.OpacityCurve](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum)

##### Enumeration Cases

- [case constant](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/constant)
- [case easeFadeIn](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/easefadein)
- [case easeFadeOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/easefadeout)
- [case gradualFadeInOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/gradualfadeinout)
- [case linearFadeIn](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/linearfadein)
- [case linearFadeOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/linearfadeout)
- [case quickFadeInOut](/documentation/realitykit/particleemittercomponent/particleemitter/opacitycurve-swift.enum/quickfadeinout)
- [ParticleEmitterComponent.ParticleEmitter.ParticleColor](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor)

##### Enumeration Cases

- [case constant(ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/constant(_:))
- [case evolving(start: ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue, end: ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/evolving(start:end:))

##### Enumerations

- [ParticleEmitterComponent.ParticleEmitter.ParticleColor.ColorValue](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue)

###### Enumeration Cases

- [case random(a: ParticleEmitterComponent.ParticleEmitter.Color, b: ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/random(a:b:)-1muv6)
- [case random(a: ParticleEmitterComponent.ParticleEmitter.Color, b: ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/random(a:b:)-6g22v)
- [case single(ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/single(_:)-58m53)
- [case single(ParticleEmitterComponent.ParticleEmitter.Color)](/documentation/realitykit/particleemittercomponent/particleemitter/particlecolor/colorvalue/single(_:)-65g3i)
- [ParticleEmitterComponent.ParticleEmitter.SortOrder](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum)

##### Enumeration Cases

- [case decreasingAge](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingage)
- [case decreasingDepth](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingdepth)
- [case decreasingID](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/decreasingid)
- [case increasingAge](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingage)
- [case increasingDepth](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingdepth)
- [case increasingID](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/increasingid)
- [case unsorted](/documentation/realitykit/particleemittercomponent/particleemitter/sortorder-swift.enum/unsorted)
- [ParticleEmitterComponent.Presets](/documentation/realitykit/particleemittercomponent/presets)

#### Type Properties

- [static var fireworks: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/fireworks)
- [static var impact: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/impact)
- [static var magic: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/magic)
- [static var rain: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/rain)
- [static var snow: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/snow)
- [static var sparks: ParticleEmitterComponent](/documentation/realitykit/particleemittercomponent/presets/sparks)

### Entity compliance

- [HasPhysicsBody](/documentation/realitykit/hasphysicsbody)

#### Getting the component

- [var physicsBody: PhysicsBodyComponent?](/documentation/realitykit/hasphysicsbody/physicsbody)

#### Adding and clearing forces

- [func addForce(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/addforce(_:relativeto:))
- [func addForce(SIMD3<Float>, at: SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/addforce(_:at:relativeto:))
- [func addTorque(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/addtorque(_:relativeto:))
- [func clearForcesAndTorques()](/documentation/realitykit/hasphysicsbody/clearforcesandtorques())

#### Applying impulses

- [func applyLinearImpulse(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/applylinearimpulse(_:relativeto:))
- [func applyAngularImpulse(SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/applyangularimpulse(_:relativeto:))
- [func applyImpulse(SIMD3<Float>, at: SIMD3<Float>, relativeTo: Entity?)](/documentation/realitykit/hasphysicsbody/applyimpulse(_:at:relativeto:))

#### Resetting physics simulations

- [func resetPhysicsTransform(recursive: Bool)](/documentation/realitykit/hasphysicsbody/resetphysicstransform(recursive:))
- [func resetPhysicsTransform(Transform, recursive: Bool)](/documentation/realitykit/hasphysicsbody/resetphysicstransform(_:recursive:))
- [HasPhysicsMotion](/documentation/realitykit/hasphysicsmotion)

#### Setting the motion component

- [var physicsMotion: PhysicsMotionComponent?](/documentation/realitykit/hasphysicsmotion/physicsmotion)
- [HasPhysics](/documentation/realitykit/hasphysics)
- [Force effects](/documentation/realitykit/physics-force-effects)

### Force effect components

- [ForceEffectComponent](/documentation/realitykit/forceeffectcomponent)

#### Initializers

- [init(effect: any ForceEffectBase)](/documentation/realitykit/forceeffectcomponent/init(effect:))
- [init(effects: [any ForceEffectBase], simulationState: ForceEffectComponent.SimulationState)](/documentation/realitykit/forceeffectcomponent/init(effects:simulationstate:))

#### Instance Properties

- [var effects: [any ForceEffectBase]](/documentation/realitykit/forceeffectcomponent/effects)
- [var simulationState: ForceEffectComponent.SimulationState?](/documentation/realitykit/forceeffectcomponent/simulationstate-swift.property)

#### Enumerations

- [ForceEffectComponent.SimulationState](/documentation/realitykit/forceeffectcomponent/simulationstate-swift.enum)

##### Enumeration Cases

- [case pause](/documentation/realitykit/forceeffectcomponent/simulationstate-swift.enum/pause)
- [case resume](/documentation/realitykit/forceeffectcomponent/simulationstate-swift.enum/resume)
- [case start](/documentation/realitykit/forceeffectcomponent/simulationstate-swift.enum/start)
- [ForceEffect](/documentation/realitykit/forceeffect)

#### Initializers

- [init(effect: ForceEffectType, strengthScale: Double, spatialFalloff: SpatialForceFalloff?, timedFalloff: TimedForceFalloff?, position: SIMD3<Float>, orientation: simd_quatf, mask: CollisionGroup)](/documentation/realitykit/forceeffect/init(effect:strengthscale:spatialfalloff:timedfalloff:position:orientation:mask:))

#### Instance Properties

- [var effect: ForceEffectType](/documentation/realitykit/forceeffect/effect)
- [var mask: CollisionGroup](/documentation/realitykit/forceeffect/mask)
- [var orientation: simd_quatf](/documentation/realitykit/forceeffect/orientation)
- [var position: SIMD3<Float>](/documentation/realitykit/forceeffect/position)
- [var spatialFalloff: SpatialForceFalloff?](/documentation/realitykit/forceeffect/spatialfalloff)
- [var strengthScale: Float](/documentation/realitykit/forceeffect/strengthscale)
- [var timedFalloff: TimedForceFalloff?](/documentation/realitykit/forceeffect/timedfalloff)

### Built-in force effect types

- [ConstantForceEffect](/documentation/realitykit/constantforceeffect)

#### Initializers

- [init(strength: Double, direction: SIMD3<Float>)](/documentation/realitykit/constantforceeffect/init(strength:direction:))

#### Instance Properties

- [let direction: SIMD3<Float>](/documentation/realitykit/constantforceeffect/direction)
- [var forceMode: ForceMode](/documentation/realitykit/constantforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/constantforceeffect/parametertypes)
- [let strength: Float](/documentation/realitykit/constantforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/constantforceeffect/update(parameters:))
- [ConstantRadialForceEffect](/documentation/realitykit/constantradialforceeffect)

#### Initializers

- [init(strength: Double)](/documentation/realitykit/constantradialforceeffect/init(strength:))

#### Instance Properties

- [var forceMode: ForceMode](/documentation/realitykit/constantradialforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/constantradialforceeffect/parametertypes)
- [let strength: Float](/documentation/realitykit/constantradialforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/constantradialforceeffect/update(parameters:))
- [DragForceEffect](/documentation/realitykit/dragforceeffect)

#### Initializers

- [init(strength: Double)](/documentation/realitykit/dragforceeffect/init(strength:))

#### Instance Properties

- [var forceMode: ForceMode](/documentation/realitykit/dragforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/dragforceeffect/parametertypes)
- [let strength: Float](/documentation/realitykit/dragforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/dragforceeffect/update(parameters:))
- [RadialForceEffect](/documentation/realitykit/radialforceeffect)

#### Initializers

- [init(strength: Double, restDistance: Double)](/documentation/realitykit/radialforceeffect/init(strength:restdistance:))

#### Instance Properties

- [var forceMode: ForceMode](/documentation/realitykit/radialforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/radialforceeffect/parametertypes)
- [let restDistance: Float](/documentation/realitykit/radialforceeffect/restdistance)
- [let strength: Float](/documentation/realitykit/radialforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/radialforceeffect/update(parameters:))
- [TurbulenceForceEffect](/documentation/realitykit/turbulenceforceeffect)

#### Initializers

- [init(strength: Double, smoothness: Double, speed: Double)](/documentation/realitykit/turbulenceforceeffect/init(strength:smoothness:speed:))

#### Instance Properties

- [var forceMode: ForceMode](/documentation/realitykit/turbulenceforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/turbulenceforceeffect/parametertypes)
- [let smoothness: Float](/documentation/realitykit/turbulenceforceeffect/smoothness)
- [let speed: Float](/documentation/realitykit/turbulenceforceeffect/speed)
- [let strength: Float](/documentation/realitykit/turbulenceforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/turbulenceforceeffect/update(parameters:))
- [VortexForceEffect](/documentation/realitykit/vortexforceeffect)

#### Initializers

- [init(strength: Double, axis: SIMD3<Float>)](/documentation/realitykit/vortexforceeffect/init(strength:axis:))

#### Instance Properties

- [let axis: SIMD3<Float>](/documentation/realitykit/vortexforceeffect/axis)
- [var forceMode: ForceMode](/documentation/realitykit/vortexforceeffect/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/vortexforceeffect/parametertypes)
- [let strength: Float](/documentation/realitykit/vortexforceeffect/strength)

#### Instance Methods

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/vortexforceeffect/update(parameters:))

### Force effect constraints

- [ForceEffectBounds](/documentation/realitykit/forceeffectbounds)

#### Enumeration Cases

- [case sphere(radius: Double)](/documentation/realitykit/forceeffectbounds/sphere(radius:))
- [SpatialForceFalloff](/documentation/realitykit/spatialforcefalloff)

#### Initializers

- [init(bounds: ForceEffectBounds, rate: Double, distanceOffset: Double)](/documentation/realitykit/spatialforcefalloff/init(bounds:rate:distanceoffset:))

#### Instance Properties

- [var bounds: ForceEffectBounds](/documentation/realitykit/spatialforcefalloff/bounds)
- [var distanceOffset: Double](/documentation/realitykit/spatialforcefalloff/distanceoffset)
- [var rate: Double](/documentation/realitykit/spatialforcefalloff/rate)
- [TimedForceFalloff](/documentation/realitykit/timedforcefalloff)

#### Initializers

- [init(duration: TimeInterval, rate: Double)](/documentation/realitykit/timedforcefalloff/init(duration:rate:))

#### Instance Properties

- [var duration: TimeInterval](/documentation/realitykit/timedforcefalloff/duration)
- [var rate: Double](/documentation/realitykit/timedforcefalloff/rate)

### Custom forces

- [ForceEffectProtocol](/documentation/realitykit/forceeffectprotocol)

#### Updating effects

- [func update(parameters: inout ForceEffectParameters)](/documentation/realitykit/forceeffectprotocol/update(parameters:))
- [static func register(((inout ForceEffectEvent<Self>) -> Void)?)](/documentation/realitykit/forceeffectprotocol/register(_:)-1zt9t)
- [PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes)

##### Initializers

- [init(rawValue: UInt32)](/documentation/realitykit/physicsbodyparametertypes/init(rawvalue:))

##### Instance Properties

- [let rawValue: UInt32](/documentation/realitykit/physicsbodyparametertypes/rawvalue)

##### Type Properties

- [static let angularVelocity: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/angularvelocity)
- [static let distance: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/distance)
- [static let inertiaTensor: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/inertiatensor)
- [static let mass: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/mass)
- [static let orientation: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/orientation)
- [static let position: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/position)
- [static let velocity: PhysicsBodyParameterTypes](/documentation/realitykit/physicsbodyparametertypes/velocity)
- [ForceEffectParameters](/documentation/realitykit/forceeffectparameters)

##### Instance Properties

- [let angularVelocities: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/angularvelocities)
- [let distances: UnsafeForceEffectBuffer<Float>?](/documentation/realitykit/forceeffectparameters/distances)
- [let elapsedTime: TimeInterval](/documentation/realitykit/forceeffectparameters/elapsedtime)
- [let entity: Entity](/documentation/realitykit/forceeffectparameters/entity)
- [let fixedDeltaTime: TimeInterval](/documentation/realitykit/forceeffectparameters/fixeddeltatime)
- [let inertiaTensors: UnsafeForceEffectBuffer<simd_float3x3>?](/documentation/realitykit/forceeffectparameters/inertiatensors)
- [let masses: UnsafeForceEffectBuffer<Float>?](/documentation/realitykit/forceeffectparameters/masses)
- [let orientations: UnsafeForceEffectBuffer<simd_quatf>?](/documentation/realitykit/forceeffectparameters/orientations)
- [let physicsBodyCount: Int](/documentation/realitykit/forceeffectparameters/physicsbodycount)
- [let positions: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/positions)
- [let velocities: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/velocities)

##### Instance Methods

- [func setForce(SIMD3<Float>, index: Int)](/documentation/realitykit/forceeffectparameters/setforce(_:index:))
- [func setTorque(SIMD3<Float>, index: Int)](/documentation/realitykit/forceeffectparameters/settorque(_:index:))
- [ForceEffectEvent](/documentation/realitykit/forceeffectevent)

##### Instance Properties

- [var effect: ForceEffectType](/documentation/realitykit/forceeffectevent/effect)
- [var parameters: ForceEffectParameters](/documentation/realitykit/forceeffectevent/parameters)
- [UnsafeForceEffectBuffer](/documentation/realitykit/unsafeforceeffectbuffer)

##### Structures

- [UnsafeForceEffectBuffer.Iterator](/documentation/realitykit/unsafeforceeffectbuffer/iterator)

##### Instance Properties

- [var count: Int](/documentation/realitykit/unsafeforceeffectbuffer/count)

##### Instance Methods

- [func makeIterator() -> UnsafeForceEffectBuffer<T>.Iterator](/documentation/realitykit/unsafeforceeffectbuffer/makeiterator())

##### Subscripts

- [subscript(Int) -> T](/documentation/realitykit/unsafeforceeffectbuffer/subscript(_:))

#### Instance Properties

- [var forceMode: ForceMode](/documentation/realitykit/forceeffectprotocol/forcemode)
- [var parameterTypes: PhysicsBodyParameterTypes](/documentation/realitykit/forceeffectprotocol/parametertypes)

#### Type Methods

- [static register(_:)](/documentation/realitykit/forceeffectprotocol/register(_:))
- [ForceMode](/documentation/realitykit/forcemode)

#### Enumeration Cases

- [case acceleration](/documentation/realitykit/forcemode/acceleration)
- [case force](/documentation/realitykit/forcemode/force)
- [case impulse](/documentation/realitykit/forcemode/impulse)
- [case velocity](/documentation/realitykit/forcemode/velocity)
- [ForceEffectParameters](/documentation/realitykit/forceeffectparameters)

#### Instance Properties

- [let angularVelocities: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/angularvelocities)
- [let distances: UnsafeForceEffectBuffer<Float>?](/documentation/realitykit/forceeffectparameters/distances)
- [let elapsedTime: TimeInterval](/documentation/realitykit/forceeffectparameters/elapsedtime)
- [let entity: Entity](/documentation/realitykit/forceeffectparameters/entity)
- [let fixedDeltaTime: TimeInterval](/documentation/realitykit/forceeffectparameters/fixeddeltatime)
- [let inertiaTensors: UnsafeForceEffectBuffer<simd_float3x3>?](/documentation/realitykit/forceeffectparameters/inertiatensors)
- [let masses: UnsafeForceEffectBuffer<Float>?](/documentation/realitykit/forceeffectparameters/masses)
- [let orientations: UnsafeForceEffectBuffer<simd_quatf>?](/documentation/realitykit/forceeffectparameters/orientations)
- [let physicsBodyCount: Int](/documentation/realitykit/forceeffectparameters/physicsbodycount)
- [let positions: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/positions)
- [let velocities: UnsafeForceEffectBuffer<SIMD3<Float>>?](/documentation/realitykit/forceeffectparameters/velocities)

#### Instance Methods

- [func setForce(SIMD3<Float>, index: Int)](/documentation/realitykit/forceeffectparameters/setforce(_:index:))
- [func setTorque(SIMD3<Float>, index: Int)](/documentation/realitykit/forceeffectparameters/settorque(_:index:))
- [ForceEffectBase](/documentation/realitykit/forceeffectbase)

#### Associated Types

- [ForceEffectType](/documentation/realitykit/forceeffectbase/forceeffecttype)

#### Instance Properties

- [var effect: Self.ForceEffectType](/documentation/realitykit/forceeffectbase/effect)
- [var mask: CollisionGroup](/documentation/realitykit/forceeffectbase/mask)
- [var orientation: simd_quatf](/documentation/realitykit/forceeffectbase/orientation)
- [var position: SIMD3<Float>](/documentation/realitykit/forceeffectbase/position)
- [var spatialFalloff: SpatialForceFalloff?](/documentation/realitykit/forceeffectbase/spatialfalloff)
- [var strengthScale: Float](/documentation/realitykit/forceeffectbase/strengthscale)
- [var timedFalloff: TimedForceFalloff?](/documentation/realitykit/forceeffectbase/timedfalloff)
- [Physics joints and pins](/documentation/realitykit/physics-joints-and-pins)

### Pin and joint components

- [Simulating physics joints in your RealityKit app](/documentation/realitykit/simulating-physics-joints-in-your-realitykit-app)
- [GeometricPin](/documentation/realitykit/geometricpin)

#### Operators

- [static func == (GeometricPin, GeometricPin) -> Bool](/documentation/realitykit/geometricpin/==(_:_:))

#### Initializers

- [init(named: String, offsetPosition: SIMD3<Float>, offsetOrientation: simd_quatf)](/documentation/realitykit/geometricpin/init(named:offsetposition:offsetorientation:))
- [init(named: String, skeletalJointName: String, offsetPosition: SIMD3<Float>, offsetOrientation: simd_quatf)](/documentation/realitykit/geometricpin/init(named:skeletaljointname:offsetposition:offsetorientation:))

#### Instance Properties

- [var entity: Entity?](/documentation/realitykit/geometricpin/entity)
- [var name: String](/documentation/realitykit/geometricpin/name)
- [var offsetOrientation: simd_quatf](/documentation/realitykit/geometricpin/offsetorientation)
- [var offsetPosition: SIMD3<Float>](/documentation/realitykit/geometricpin/offsetposition)
- [var orientation: simd_quatf?](/documentation/realitykit/geometricpin/orientation)
- [var position: SIMD3<Float>?](/documentation/realitykit/geometricpin/position)

#### Instance Methods

- [func hash(into: inout Hasher)](/documentation/realitykit/geometricpin/hash(into:))
- [func orientation(relativeTo: Entity?) -> simd_quatf?](/documentation/realitykit/geometricpin/orientation(relativeto:))
- [func position(relativeTo: Entity?) -> SIMD3<Float>?](/documentation/realitykit/geometricpin/position(relativeto:))
- [GeometricPinsComponent](/documentation/realitykit/geometricpinscomponent)

#### Initializers

- [init()](/documentation/realitykit/geometricpinscomponent/init())

#### Instance Properties

- [var pins: Set<GeometricPin>](/documentation/realitykit/geometricpinscomponent/pins)

#### Instance Methods

- [func removePin(named: String) -> GeometricPin?](/documentation/realitykit/geometricpinscomponent/removepin(named:))
- [func set(pin: GeometricPin)](/documentation/realitykit/geometricpinscomponent/set(pin:))

#### Subscripts

- [subscript(String) -> GeometricPin?](/documentation/realitykit/geometricpinscomponent/subscript(_:))
- [PhysicsJoint](/documentation/realitykit/physicsjoint)

#### Instance Properties

- [var checksForInternalCollisions: Bool](/documentation/realitykit/physicsjoint/checksforinternalcollisions)
- [var isActive: Bool](/documentation/realitykit/physicsjoint/isactive)
- [var pin0: GeometricPin](/documentation/realitykit/physicsjoint/pin0)
- [var pin1: GeometricPin](/documentation/realitykit/physicsjoint/pin1)

#### Instance Methods

- [func addToSimulation() throws -> Entity](/documentation/realitykit/physicsjoint/addtosimulation())
- [PhysicsJointsComponent](/documentation/realitykit/physicsjointscomponent)

#### Initializers

- [init()](/documentation/realitykit/physicsjointscomponent/init())

#### Instance Properties

- [var joints: PhysicsJoints](/documentation/realitykit/physicsjointscomponent/joints)
- [EntityGeometricPins](/documentation/realitykit/entitygeometricpins)

#### Structures

- [EntityGeometricPins.Iterator](/documentation/realitykit/entitygeometricpins/iterator)

##### Type Aliases

- [EntityGeometricPins.Iterator.Element](/documentation/realitykit/entitygeometricpins/iterator/element)

#### Instance Properties

- [var count: Int](/documentation/realitykit/entitygeometricpins/count)
- [let entity: Entity](/documentation/realitykit/entitygeometricpins/entity)
- [var isEmpty: Bool](/documentation/realitykit/entitygeometricpins/isempty)

#### Instance Methods

- [func makeIterator() -> EntityGeometricPins.Iterator](/documentation/realitykit/entitygeometricpins/makeiterator())
- [func remove(named: String)](/documentation/realitykit/entitygeometricpins/remove(named:))
- [func set(named: String, position: SIMD3<Float>, orientation: simd_quatf) -> GeometricPin](/documentation/realitykit/entitygeometricpins/set(named:position:orientation:))
- [func set(named: String, position: SIMD3<Float>, orientation: simd_quatf, relativeTo: Entity?) -> GeometricPin](/documentation/realitykit/entitygeometricpins/set(named:position:orientation:relativeto:))
- [func set(named: String, skeletalJointName: String, position: SIMD3<Float>, orientation: simd_quatf) -> GeometricPin](/documentation/realitykit/entitygeometricpins/set(named:skeletaljointname:position:orientation:))

#### Subscripts

- [subscript(String) -> GeometricPin?](/documentation/realitykit/entitygeometricpins/subscript(_:))

#### Type Aliases

- [EntityGeometricPins.Element](/documentation/realitykit/entitygeometricpins/element)
- [AttachedTransformComponent](/documentation/realitykit/attachedtransformcomponent)

#### Initializers

- [init(source: GeometricPin?, target: GeometricPin)](/documentation/realitykit/attachedtransformcomponent/init(source:target:))

#### Instance Properties

- [var source: GeometricPin?](/documentation/realitykit/attachedtransformcomponent/source)
- [var target: GeometricPin](/documentation/realitykit/attachedtransformcomponent/target)

### Built-in joint types

- [PhysicsRevoluteJoint](/documentation/realitykit/physicsrevolutejoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin, angularLimit: ClosedRange<Float>?, checksForInternalCollisions: Bool)](/documentation/realitykit/physicsrevolutejoint/init(pin0:pin1:angularlimit:checksforinternalcollisions:))

#### Instance Properties

- [var angularLimit: ClosedRange<Float>?](/documentation/realitykit/physicsrevolutejoint/angularlimit)
- [PhysicsPrismaticJoint](/documentation/realitykit/physicsprismaticjoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin, linearLimit: ClosedRange<Float>?, checksForInternalCollisions: Bool)](/documentation/realitykit/physicsprismaticjoint/init(pin0:pin1:linearlimit:checksforinternalcollisions:))

#### Instance Properties

- [var linearLimit: ClosedRange<Float>?](/documentation/realitykit/physicsprismaticjoint/linearlimit)
- [PhysicsSphericalJoint](/documentation/realitykit/physicssphericaljoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin, angularLimitInYZ: (Float, Float)?, checksForInternalCollisions: Bool)](/documentation/realitykit/physicssphericaljoint/init(pin0:pin1:angularlimitinyz:checksforinternalcollisions:))

#### Instance Properties

- [var angularLimitInYZ: (Float, Float)?](/documentation/realitykit/physicssphericaljoint/angularlimitinyz)
- [PhysicsCustomJoint](/documentation/realitykit/physicscustomjoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin, linearMotionAlongX: PhysicsCustomJoint.MotionLimit, linearMotionAlongY: PhysicsCustomJoint.MotionLimit, linearMotionAlongZ: PhysicsCustomJoint.MotionLimit, angularMotionAroundX: PhysicsCustomJoint.MotionLimit, angularMotionAroundY: PhysicsCustomJoint.MotionLimit, angularMotionAroundZ: PhysicsCustomJoint.MotionLimit, checksForInternalCollisions: Bool)](/documentation/realitykit/physicscustomjoint/init(pin0:pin1:linearmotionalongx:linearmotionalongy:linearmotionalongz:angularmotionaroundx:angularmotionaroundy:angularmotionaroundz:checksforinternalcollisions:))

#### Instance Properties

- [var angularMotionAroundX: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/angularmotionaroundx)
- [var angularMotionAroundY: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/angularmotionaroundy)
- [var angularMotionAroundZ: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/angularmotionaroundz)
- [var linearMotionAlongX: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/linearmotionalongx)
- [var linearMotionAlongY: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/linearmotionalongy)
- [var linearMotionAlongZ: PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/linearmotionalongz)

#### Enumerations

- [PhysicsCustomJoint.MotionLimit](/documentation/realitykit/physicscustomjoint/motionlimit)

##### Enumeration Cases

- [case fixed](/documentation/realitykit/physicscustomjoint/motionlimit/fixed)
- [case range(ClosedRange<Float>)](/documentation/realitykit/physicscustomjoint/motionlimit/range(_:))
- [case unlimited](/documentation/realitykit/physicscustomjoint/motionlimit/unlimited)
- [PhysicsDistanceJoint](/documentation/realitykit/physicsdistancejoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin, distanceLimit: ClosedRange<Float>, checksForInternalCollisions: Bool)](/documentation/realitykit/physicsdistancejoint/init(pin0:pin1:distancelimit:checksforinternalcollisions:))

#### Instance Properties

- [var distanceLimit: ClosedRange<Float>](/documentation/realitykit/physicsdistancejoint/distancelimit)
- [var tolerance: Float](/documentation/realitykit/physicsdistancejoint/tolerance)
- [PhysicsFixedJoint](/documentation/realitykit/physicsfixedjoint)

#### Initializers

- [init(pin0: GeometricPin, pin1: GeometricPin)](/documentation/realitykit/physicsfixedjoint/init(pin0:pin1:))

#### Instance Properties

- [let checksForInternalCollisions: Bool](/documentation/realitykit/physicsfixedjoint/checksforinternalcollisions)
- [PhysicsJoints](/documentation/realitykit/physicsjoints)

#### Initializers

- [init(any Sequence<any PhysicsJoint>)](/documentation/realitykit/physicsjoints/init(_:))

## Performance improvements

- [Improving the Performance of a RealityKit App](/documentation/realitykit/improving-the-performance-of-a-realitykit-app)

### Optimization targets

- [Reducing CPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-cpu-utilization-in-your-realitykit-app)
- [Reducing GPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-gpu-utilization-in-your-realitykit-app)
- [Reducing GPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-gpu-utilization-in-your-realitykit-app)
- [Reducing CPU Utilization in Your RealityKit App](/documentation/realitykit/reducing-cpu-utilization-in-your-realitykit-app)
- [Construct an immersive environment for visionOS](/documentation/realitykit/construct-an-immersive-environment-for-visionos)
- [Passing Metal command objects around your application](/documentation/realitykit/passing-metal-command-objects-around-your-application)

## Articles

- [Rendering stereoscopic video with RealityKit](/documentation/realitykit/rendering-stereoscopic-video-with-realitykit)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
