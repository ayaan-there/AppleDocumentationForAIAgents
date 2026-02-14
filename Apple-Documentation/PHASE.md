# PHASE Documentation

Source: https://sosumi.ai/documentation/phase

---
title: PHASE
source: https://developer.apple.com/documentation/phase
timestamp: 2026-02-13T19:00:37.607Z
---

## Essentials

- [Playing sound from a location in a 3D scene](/documentation/phase/playing-sound-from-a-location-in-a-3d-scene)
- [Personalizing spatial audio in your app](/documentation/phase/personalizing-spatial-audio-in-your-app)
- [PHASE updates](/documentation/updates/phase)

## Setup

- [PHASEEngine](/documentation/phase/phaseengine)

### Creating an Engine

- [init(updateMode: PHASEEngine.UpdateMode)](/documentation/phase/phaseengine/init(updatemode:))
- [init(updateMode: PHASEEngine.UpdateMode, renderingMode: PHASEEngine.RenderingMode)](/documentation/phase/phaseengine/init(updatemode:renderingmode:))
- [PHASEEngine.UpdateMode](/documentation/phase/phaseengine/updatemode)

#### Modes

- [case automatic](/documentation/phase/phaseengine/updatemode/automatic)
- [case manual](/documentation/phase/phaseengine/updatemode/manual)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseengine/updatemode/init(rawvalue:))
- [PHASEEngine.RenderingMode](/documentation/phase/phaseengine/renderingmode)

#### Modes

- [case local](/documentation/phase/phaseengine/renderingmode/local)
- [case client](/documentation/phase/phaseengine/renderingmode/client)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseengine/renderingmode/init(rawvalue:))

### Registering Audio Resources

- [var assetRegistry: PHASEAssetRegistry](/documentation/phase/phaseengine/assetregistry)

### Accessing Scene Hierarchy

- [var rootObject: PHASEObject](/documentation/phase/phaseengine/rootobject)

### Defining Environmental Effects

- [var defaultReverbPreset: PHASEReverbPreset](/documentation/phase/phaseengine/defaultreverbpreset)
- [var defaultMedium: PHASEMedium](/documentation/phase/phaseengine/defaultmedium)
- [var outputSpatializationMode: PHASESpatializationMode](/documentation/phase/phaseengine/outputspatializationmode)

### Controlling and Inspecting Playback State

- [func pause()](/documentation/phase/phaseengine/pause())
- [func start() throws](/documentation/phase/phaseengine/start())
- [func stop()](/documentation/phase/phaseengine/stop())
- [func update()](/documentation/phase/phaseengine/update())
- [var renderingState: PHASESoundEvent.RenderingState](/documentation/phase/phaseengine/renderingstate)
- [var lastRenderTime: AVAudioTime?](/documentation/phase/phaseengine/lastrendertime)

### Managing Groups of Sounds

- [var groups: [String : PHASEGroup]](/documentation/phase/phaseengine/groups)
- [var activeGroupPreset: PHASEGroupPreset?](/documentation/phase/phaseengine/activegrouppreset)
- [var duckers: [PHASEDucker]](/documentation/phase/phaseengine/duckers)

### Accessing In-Flight Audio

- [var soundEvents: [PHASESoundEvent]](/documentation/phase/phaseengine/soundevents)

### Measuring Units

- [var unitsPerMeter: Double](/documentation/phase/phaseengine/unitspermeter)
- [var unitsPerSecond: Double](/documentation/phase/phaseengine/unitspersecond)
- [PHASEEngine.UpdateMode](/documentation/phase/phaseengine/updatemode)

### Modes

- [case automatic](/documentation/phase/phaseengine/updatemode/automatic)
- [case manual](/documentation/phase/phaseengine/updatemode/manual)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseengine/updatemode/init(rawvalue:))
- [PHASEEngine.RenderingMode](/documentation/phase/phaseengine/renderingmode)

### Modes

- [case local](/documentation/phase/phaseengine/renderingmode/local)
- [case client](/documentation/phase/phaseengine/renderingmode/client)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseengine/renderingmode/init(rawvalue:))
- [PHASEAssetRegistry](/documentation/phase/phaseassetregistry)

### Registering Sound Assets

- [func registerSoundAsset(url: URL, identifier: String?, assetType: PHASEAsset.AssetType, channelLayout: AVAudioChannelLayout?, normalizationMode: PHASENormalizationMode) throws -> PHASESoundAsset](/documentation/phase/phaseassetregistry/registersoundasset(url:identifier:assettype:channellayout:normalizationmode:))
- [func registerSoundAsset(data: Data, identifier: String?, format: AVAudioFormat, normalizationMode: PHASENormalizationMode) throws -> PHASESoundAsset](/documentation/phase/phaseassetregistry/registersoundasset(data:identifier:format:normalizationmode:))
- [func unregisterAsset(identifier: String, completion: ((Bool) -> Void)?)](/documentation/phase/phaseassetregistry/unregisterasset(identifier:completion:))

### Registering Sound Event Assets

- [func registerSoundEventAsset(rootNode: PHASESoundEventNodeDefinition, identifier: String?) throws -> PHASESoundEventNodeAsset](/documentation/phase/phaseassetregistry/registersoundeventasset(rootnode:identifier:))
- [func asset(forIdentifier: String) -> PHASEAsset?](/documentation/phase/phaseassetregistry/asset(foridentifier:))

### Registering Global Metaparameters

- [func registerGlobalMetaParameter(metaParameterDefinition: PHASEMetaParameterDefinition) throws -> PHASEGlobalMetaParameterAsset](/documentation/phase/phaseassetregistry/registerglobalmetaparameter(metaparameterdefinition:))
- [var globalMetaParameters: [String : PHASEMetaParameter]](/documentation/phase/phaseassetregistry/globalmetaparameters)
- [PHASENormalizationMode](/documentation/phase/phasenormalizationmode)

### Loudness Normalization Modes

- [case dynamic](/documentation/phase/phasenormalizationmode/dynamic)
- [case none](/documentation/phase/phasenormalizationmode/none)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasenormalizationmode/init(rawvalue:))
- [PHASESpatializationMode](/documentation/phase/phasespatializationmode)

### Modes

- [case automatic](/documentation/phase/phasespatializationmode/automatic)
- [case alwaysUseBinaural](/documentation/phase/phasespatializationmode/alwaysusebinaural)
- [case alwaysUseChannelBased](/documentation/phase/phasespatializationmode/alwaysusechannelbased)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasespatializationmode/init(rawvalue:))
- [PHASEReverbPreset](/documentation/phase/phasereverbpreset)

### Presets

- [case cathedral](/documentation/phase/phasereverbpreset/cathedral)
- [case largeChamber](/documentation/phase/phasereverbpreset/largechamber)
- [case largeHall](/documentation/phase/phasereverbpreset/largehall)
- [case largeHall2](/documentation/phase/phasereverbpreset/largehall2)
- [case largeRoom](/documentation/phase/phasereverbpreset/largeroom)
- [case largeRoom2](/documentation/phase/phasereverbpreset/largeroom2)
- [case mediumChamber](/documentation/phase/phasereverbpreset/mediumchamber)
- [case mediumHall](/documentation/phase/phasereverbpreset/mediumhall)
- [case mediumHall2](/documentation/phase/phasereverbpreset/mediumhall2)
- [case mediumHall3](/documentation/phase/phasereverbpreset/mediumhall3)
- [case mediumRoom](/documentation/phase/phasereverbpreset/mediumroom)
- [case none](/documentation/phase/phasereverbpreset/none)
- [case smallRoom](/documentation/phase/phasereverbpreset/smallroom)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasereverbpreset/init(rawvalue:))
- [PHASEMedium](/documentation/phase/phasemedium)

### Creating a Medium

- [init(engine: PHASEEngine, preset: PHASEMedium.Preset)](/documentation/phase/phasemedium/init(engine:preset:))
- [PHASEMedium.Preset](/documentation/phase/phasemedium/preset)

#### Medium Types

- [case air](/documentation/phase/phasemedium/preset/air)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasemedium/preset/init(rawvalue:))

## Soundscape Creation

- [PHASESource](/documentation/phase/phasesource)

### Creating a Source

- [init(engine: PHASEEngine)](/documentation/phase/phasesource/init(engine:))
- [init(engine: PHASEEngine, shapes: [PHASEShape])](/documentation/phase/phasesource/init(engine:shapes:))

### Controlling Sound Volume

- [var gain: Double](/documentation/phase/phasesource/gain)

### Inspecting the Shape

- [var shapes: [PHASEShape]](/documentation/phase/phasesource/shapes)
- [PHASEListener](/documentation/phase/phaselistener)

### Creating a Listener

- [init(engine: PHASEEngine)](/documentation/phase/phaselistener/init(engine:))

### Adjusting Loudness

- [var gain: Double](/documentation/phase/phaselistener/gain)

### Instance Properties

- [var automaticHeadTrackingFlags: PHASEAutomaticHeadTrackingFlags](/documentation/phase/phaselistener/automaticheadtrackingflags)
- [PHASEOccluder](/documentation/phase/phaseoccluder)

### Creating an Occluder

- [init(engine: PHASEEngine, shapes: [PHASEShape])](/documentation/phase/phaseoccluder/init(engine:shapes:))

### Inspecting the Shape

- [var shapes: [PHASEShape]](/documentation/phase/phaseoccluder/shapes)
- [PHASEObject](/documentation/phase/phaseobject)

### Creating an Object

- [init(engine: PHASEEngine)](/documentation/phase/phaseobject/init(engine:))

### Managing the Hierarchy

- [var children: [PHASEObject]](/documentation/phase/phaseobject/children)
- [var parent: PHASEObject?](/documentation/phase/phaseobject/parent)
- [func addChild(PHASEObject) throws](/documentation/phase/phaseobject/addchild(_:))
- [func removeChild(PHASEObject)](/documentation/phase/phaseobject/removechild(_:))
- [func removeChildren()](/documentation/phase/phaseobject/removechildren())

### Defining a Pose

- [var transform: simd_float4x4](/documentation/phase/phaseobject/transform)
- [var worldTransform: simd_float4x4](/documentation/phase/phaseobject/worldtransform)

### Inspecting the Orientation

- [class var forward: simd_float3](/documentation/phase/phaseobject/forward)
- [class var right: simd_float3](/documentation/phase/phaseobject/right)
- [class var up: simd_float3](/documentation/phase/phaseobject/up)
- [PHASEShape](/documentation/phase/phaseshape)

### Creating a Shape

- [init(engine: PHASEEngine, mesh: MDLMesh)](/documentation/phase/phaseshape/init(engine:mesh:))
- [convenience init(engine: PHASEEngine, mesh: MDLMesh, materials: [PHASEMaterial])](/documentation/phase/phaseshape/init(engine:mesh:materials:))

### Describing Surface Characteristics

- [var elements: [PHASEShape.Element]](/documentation/phase/phaseshape/elements)
- [PHASEShape.Element](/documentation/phase/phaseshape/element)

#### Specifying a Meterial

- [var material: PHASEMaterial?](/documentation/phase/phaseshape/element/material)
- [PHASEShape.Element](/documentation/phase/phaseshape/element)

### Specifying a Meterial

- [var material: PHASEMaterial?](/documentation/phase/phaseshape/element/material)
- [PHASEMaterial](/documentation/phase/phasematerial)

### Creating a Material

- [init(engine: PHASEEngine, preset: PHASEMaterialPreset)](/documentation/phase/phasematerial/init(engine:preset:))
- [PHASEMaterialPreset](/documentation/phase/phasematerialpreset)

### Presets

- [case brick](/documentation/phase/phasematerialpreset/brick)
- [case cardboard](/documentation/phase/phasematerialpreset/cardboard)
- [case concrete](/documentation/phase/phasematerialpreset/concrete)
- [case drywall](/documentation/phase/phasematerialpreset/drywall)
- [case glass](/documentation/phase/phasematerialpreset/glass)
- [case wood](/documentation/phase/phasematerialpreset/wood)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasematerialpreset/init(rawvalue:))
- [PHASEMixerParameters](/documentation/phase/phasemixerparameters)

### Positioning and Orienting Audio

- [func addAmbientMixerParameters(identifier: String, listener: PHASEListener)](/documentation/phase/phasemixerparameters/addambientmixerparameters(identifier:listener:))
- [func addSpatialMixerParameters(identifier: String, source: PHASESource, listener: PHASEListener)](/documentation/phase/phasemixerparameters/addspatialmixerparameters(identifier:source:listener:))

## Audio Selection and Playback

- [PHASESoundAsset](/documentation/phase/phasesoundasset)

### Accessing Sound Data

- [var data: Data?](/documentation/phase/phasesoundasset/data)
- [var url: URL?](/documentation/phase/phasesoundasset/url)

### Classifying an Asset

- [var type: PHASEAsset.AssetType](/documentation/phase/phasesoundasset/type)
- [PHASESoundEvent](/documentation/phase/phasesoundevent)

### Creating a Sound Event

- [init(engine: PHASEEngine, assetIdentifier: String) throws](/documentation/phase/phasesoundevent/init(engine:assetidentifier:))
- [init(engine: PHASEEngine, assetIdentifier: String, mixerParameters: PHASEMixerParameters) throws](/documentation/phase/phasesoundevent/init(engine:assetidentifier:mixerparameters:))

### Configuring Mixers and Metaparameters

- [var mixers: [String : PHASEMixer]](/documentation/phase/phasesoundevent/mixers)
- [var metaParameters: [String : PHASEMetaParameter]](/documentation/phase/phasesoundevent/metaparameters)

### Preparing Playback

- [func prepare(completion: ((PHASESoundEvent.PrepareHandlerReason) -> Void)?)](/documentation/phase/phasesoundevent/prepare(completion:))
- [PHASESoundEvent.PrepareHandlerReason](/documentation/phase/phasesoundevent/preparehandlerreason)

#### Reasons

- [case prepared](/documentation/phase/phasesoundevent/preparehandlerreason/prepared)
- [case terminated](/documentation/phase/phasesoundevent/preparehandlerreason/terminated)
- [case failure](/documentation/phase/phasesoundevent/preparehandlerreason/failure)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/preparehandlerreason/init(rawvalue:))
- [var prepareState: PHASESoundEvent.PrepareState](/documentation/phase/phasesoundevent/preparestate-swift.property)
- [PHASESoundEvent.PrepareState](/documentation/phase/phasesoundevent/preparestate-swift.enum)

#### States

- [case prepareInProgress](/documentation/phase/phasesoundevent/preparestate-swift.enum/prepareinprogress)
- [case prepareNotStarted](/documentation/phase/phasesoundevent/preparestate-swift.enum/preparenotstarted)
- [case prepared](/documentation/phase/phasesoundevent/preparestate-swift.enum/prepared)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/preparestate-swift.enum/init(rawvalue:))

### Checking Playback Status

- [var renderingState: PHASESoundEvent.RenderingState](/documentation/phase/phasesoundevent/renderingstate-swift.property)
- [PHASESoundEvent.RenderingState](/documentation/phase/phasesoundevent/renderingstate-swift.enum)

#### States

- [case paused](/documentation/phase/phasesoundevent/renderingstate-swift.enum/paused)
- [case started](/documentation/phase/phasesoundevent/renderingstate-swift.enum/started)
- [case stopped](/documentation/phase/phasesoundevent/renderingstate-swift.enum/stopped)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/renderingstate-swift.enum/init(rawvalue:))

### Providing Buffered Data

- [var pushStreamNodes: [String : PHASEPushStreamNode]](/documentation/phase/phasesoundevent/pushstreamnodes)

### Starting Playback

- [func start(completion: ((PHASESoundEvent.StartHandlerReason) -> Void)?)](/documentation/phase/phasesoundevent/start(completion:))
- [PHASESoundEvent.StartHandlerReason](/documentation/phase/phasesoundevent/starthandlerreason)

#### Reasons

- [case finishedPlaying](/documentation/phase/phasesoundevent/starthandlerreason/finishedplaying)
- [case terminated](/documentation/phase/phasesoundevent/starthandlerreason/terminated)
- [case failure](/documentation/phase/phasesoundevent/starthandlerreason/failure)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/starthandlerreason/init(rawvalue:))

### Seeking a Time

- [func seek(to: Double, completion: ((PHASESoundEvent.SeekHandlerReason) -> Void)?)](/documentation/phase/phasesoundevent/seek(to:completion:))
- [PHASESoundEvent.SeekHandlerReason](/documentation/phase/phasesoundevent/seekhandlerreason)

#### Reasons

- [case seekSuccessful](/documentation/phase/phasesoundevent/seekhandlerreason/seeksuccessful)
- [case failureSeekAlreadyInProgress](/documentation/phase/phasesoundevent/seekhandlerreason/failureseekalreadyinprogress)
- [case failure](/documentation/phase/phasesoundevent/seekhandlerreason/failure)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/seekhandlerreason/init(rawvalue:))

### Pausing Playback

- [func pause()](/documentation/phase/phasesoundevent/pause())
- [func resume()](/documentation/phase/phasesoundevent/resume())

### Stopping Playback

- [func stopAndInvalidate()](/documentation/phase/phasesoundevent/stopandinvalidate())
- [var isIndefinite: Bool](/documentation/phase/phasesoundevent/isindefinite)

### Instance Properties

- [var pullStreamNodes: [String : PHASEPullStreamNode]](/documentation/phase/phasesoundevent/pullstreamnodes)

### Instance Methods

- [func resume(at: AVAudioTime?)](/documentation/phase/phasesoundevent/resume(at:))
- [func seek(to: Double, resumeAt: AVAudioTime, completion: ((PHASESoundEvent.SeekHandlerReason) -> Void)?)](/documentation/phase/phasesoundevent/seek(to:resumeat:completion:))
- [func start(at: AVAudioTime?, completion: ((PHASESoundEvent.StartHandlerReason) -> Void)?)](/documentation/phase/phasesoundevent/start(at:completion:))
- [PHASESoundEvent.RenderingState](/documentation/phase/phasesoundevent/renderingstate-swift.enum)

### States

- [case paused](/documentation/phase/phasesoundevent/renderingstate-swift.enum/paused)
- [case started](/documentation/phase/phasesoundevent/renderingstate-swift.enum/started)
- [case stopped](/documentation/phase/phasesoundevent/renderingstate-swift.enum/stopped)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundevent/renderingstate-swift.enum/init(rawvalue:))
- [PHASESoundEventNodeDefinition](/documentation/phase/phasesoundeventnodedefinition)

### Accessing Child Nodes

- [var children: [PHASESoundEventNodeDefinition]](/documentation/phase/phasesoundeventnodedefinition/children)

### Identifying a Definition

- [PHASEDefinition](/documentation/phase/phasedefinition)

#### Identifying a Definition

- [var identifier: String](/documentation/phase/phasedefinition/identifier)
- [PHASESoundEventNodeAsset](/documentation/phase/phasesoundeventnodeasset)
- [PHASEAsset](/documentation/phase/phaseasset)

### Identifying an Asset

- [var identifier: String](/documentation/phase/phaseasset/identifier)

### Classifying an Asset

- [PHASEAsset.AssetType](/documentation/phase/phaseasset/assettype)

#### Types

- [case resident](/documentation/phase/phaseasset/assettype/resident)
- [case streamed](/documentation/phase/phaseasset/assettype/streamed)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseasset/assettype/init(rawvalue:))
- [Sound Event Nodes](/documentation/phase/sound-event-nodes)

### Audio-Providing Nodes

- [PHASESamplerNodeDefinition](/documentation/phase/phasesamplernodedefinition)

#### Creating a Sampler Node

- [init(soundAssetIdentifier: String, mixerDefinition: PHASEMixerDefinition)](/documentation/phase/phasesamplernodedefinition/init(soundassetidentifier:mixerdefinition:))
- [convenience init(soundAssetIdentifier: String, mixerDefinition: PHASEMixerDefinition, identifier: String)](/documentation/phase/phasesamplernodedefinition/init(soundassetidentifier:mixerdefinition:identifier:))

#### Identifying the Audio

- [var assetIdentifier: String](/documentation/phase/phasesamplernodedefinition/assetidentifier)

#### Defining Cull Behavior

- [var cullOption: PHASECullOption](/documentation/phase/phasesamplernodedefinition/culloption)
- [PHASECullOption](/documentation/phase/phaseculloption)

##### Options

- [case terminate](/documentation/phase/phaseculloption/terminate)
- [case doNotCull](/documentation/phase/phaseculloption/donotcull)
- [case sleepWakeAtRealtimeOffset](/documentation/phase/phaseculloption/sleepwakeatrealtimeoffset)
- [case sleepWakeAtZero](/documentation/phase/phaseculloption/sleepwakeatzero)
- [case sleepWakeAtRandomOffset](/documentation/phase/phaseculloption/sleepwakeatrandomoffset)

##### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseculloption/init(rawvalue:))

#### Looping the Audio

- [var playbackMode: PHASEPlaybackMode](/documentation/phase/phasesamplernodedefinition/playbackmode)
- [PHASEPlaybackMode](/documentation/phase/phaseplaybackmode)

#### Playback Modes

- [case oneShot](/documentation/phase/phaseplaybackmode/oneshot)
- [case looping](/documentation/phase/phaseplaybackmode/looping)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseplaybackmode/init(rawvalue:))
- [PHASEPushStreamNodeDefinition](/documentation/phase/phasepushstreamnodedefinition)

#### Creating a Node

- [init(mixerDefinition: PHASEMixerDefinition, format: AVAudioFormat)](/documentation/phase/phasepushstreamnodedefinition/init(mixerdefinition:format:))
- [convenience init(mixerDefinition: PHASEMixerDefinition, format: AVAudioFormat, identifier: String)](/documentation/phase/phasepushstreamnodedefinition/init(mixerdefinition:format:identifier:))

#### Observing the Format

- [var format: AVAudioFormat](/documentation/phase/phasepushstreamnodedefinition/format)

#### Shaping Loudness

- [var normalize: Bool](/documentation/phase/phasepushstreamnodedefinition/normalize)
- [PHASEPushStreamNode](/documentation/phase/phasepushstreamnode)

#### Inspecting Stream Properties

- [var mixer: PHASEMixer](/documentation/phase/phasepushstreamnode/mixer)
- [var format: AVAudioFormat](/documentation/phase/phasepushstreamnode/format)

#### Providing Audio Data

- [func scheduleBuffer(buffer: AVAudioPCMBuffer)](/documentation/phase/phasepushstreamnode/schedulebuffer(buffer:))
- [func scheduleBuffer(buffer: AVAudioPCMBuffer, time: AVAudioTime?, options: PHASEPushStreamBufferOptions)](/documentation/phase/phasepushstreamnode/schedulebuffer(buffer:time:options:))
- [func scheduleBuffer(buffer: AVAudioPCMBuffer, time: AVAudioTime?, options: PHASEPushStreamBufferOptions, completionCallbackType: PHASEPushStreamCompletionCallbackCondition, completionHandler: (PHASEPushStreamCompletionCallbackCondition) -> Void)](/documentation/phase/phasepushstreamnode/schedulebuffer(buffer:time:options:completioncallbacktype:completionhandler:))
- [func scheduleBuffer(buffer: AVAudioPCMBuffer, completionCallbackType: PHASEPushStreamCompletionCallbackCondition, completionHandler: (PHASEPushStreamCompletionCallbackCondition) -> Void)](/documentation/phase/phasepushstreamnode/schedulebuffer(buffer:completioncallbacktype:completionhandler:))
- [PHASEPushStreamCompletionCallbackCondition](/documentation/phase/phasepushstreamcompletioncallbackcondition)

##### Conditions

- [case dataRendered](/documentation/phase/phasepushstreamcompletioncallbackcondition/datarendered)

##### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasepushstreamcompletioncallbackcondition/init(rawvalue:))

#### Controlling Playback

- [var gainMetaParameter: PHASENumberMetaParameter?](/documentation/phase/phasepushstreamnode/gainmetaparameter)
- [var rateMetaParameter: PHASENumberMetaParameter?](/documentation/phase/phasepushstreamnode/ratemetaparameter)
- [PHASEPushStreamBufferOptions](/documentation/phase/phasepushstreambufferoptions)

#### Creating an Option

- [init(rawValue: UInt)](/documentation/phase/phasepushstreambufferoptions/init(rawvalue:))

#### Options

- [static var `default`: PHASEPushStreamBufferOptions](/documentation/phase/phasepushstreambufferoptions/default)
- [static var interrupts: PHASEPushStreamBufferOptions](/documentation/phase/phasepushstreambufferoptions/interrupts)
- [static var interruptsAtLoop: PHASEPushStreamBufferOptions](/documentation/phase/phasepushstreambufferoptions/interruptsatloop)
- [static var loops: PHASEPushStreamBufferOptions](/documentation/phase/phasepushstreambufferoptions/loops)
- [PHASECalibrationMode](/documentation/phase/phasecalibrationmode)

#### Modes

- [case absoluteSpl](/documentation/phase/phasecalibrationmode/absolutespl)
- [case none](/documentation/phase/phasecalibrationmode/none)
- [case relativeSpl](/documentation/phase/phasecalibrationmode/relativespl)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasecalibrationmode/init(rawvalue:))
- [PHASEGeneratorNodeDefinition](/documentation/phase/phasegeneratornodedefinition)

#### Calibrating Loudness

- [func setCalibrationMode(calibrationMode: PHASECalibrationMode, level: Double)](/documentation/phase/phasegeneratornodedefinition/setcalibrationmode(calibrationmode:level:))
- [var calibrationMode: PHASECalibrationMode](/documentation/phase/phasegeneratornodedefinition/calibrationmode)
- [var level: Double](/documentation/phase/phasegeneratornodedefinition/level)

#### Defining an Output Strategy

- [var mixerDefinition: PHASEMixerDefinition](/documentation/phase/phasegeneratornodedefinition/mixerdefinition)

#### Joining a Group

- [var group: PHASEGroup?](/documentation/phase/phasegeneratornodedefinition/group)

#### Controlling Audio Playback

- [var rate: Double](/documentation/phase/phasegeneratornodedefinition/rate)
- [var rateMetaParameterDefinition: PHASENumberMetaParameterDefinition?](/documentation/phase/phasegeneratornodedefinition/ratemetaparameterdefinition)
- [var gainMetaParameterDefinition: PHASENumberMetaParameterDefinition?](/documentation/phase/phasegeneratornodedefinition/gainmetaparameterdefinition)

### Control Nodes

- [PHASESwitchNodeDefinition](/documentation/phase/phaseswitchnodedefinition)

#### Creating a Node

- [init(switchMetaParameterDefinition: PHASEStringMetaParameterDefinition)](/documentation/phase/phaseswitchnodedefinition/init(switchmetaparameterdefinition:))
- [convenience init(switchMetaParameterDefinition: PHASEStringMetaParameterDefinition, identifier: String)](/documentation/phase/phaseswitchnodedefinition/init(switchmetaparameterdefinition:identifier:))

#### Managing Child Nodes

- [var switchMetaParameterDefinition: PHASEStringMetaParameterDefinition](/documentation/phase/phaseswitchnodedefinition/switchmetaparameterdefinition)
- [func addSubtree(PHASESoundEventNodeDefinition, switchValue: String)](/documentation/phase/phaseswitchnodedefinition/addsubtree(_:switchvalue:))
- [PHASERandomNodeDefinition](/documentation/phase/phaserandomnodedefinition)

#### Creating a Node

- [init()](/documentation/phase/phaserandomnodedefinition/init())
- [convenience init(identifier: String)](/documentation/phase/phaserandomnodedefinition/init(identifier:))

#### Adding Descendent Nodes

- [func addSubtree(PHASESoundEventNodeDefinition, weight: NSNumber)](/documentation/phase/phaserandomnodedefinition/addsubtree(_:weight:))

#### Defining Selection Queue Length

- [var uniqueSelectionQueueLength: Int](/documentation/phase/phaserandomnodedefinition/uniqueselectionqueuelength)
- [PHASEBlendNodeDefinition](/documentation/phase/phaseblendnodedefinition)

#### Creating a Blend Node

- [init(blendMetaParameterDefinition: PHASENumberMetaParameterDefinition)](/documentation/phase/phaseblendnodedefinition/init(blendmetaparameterdefinition:))
- [convenience init(blendMetaParameterDefinition: PHASENumberMetaParameterDefinition, identifier: String)](/documentation/phase/phaseblendnodedefinition/init(blendmetaparameterdefinition:identifier:))
- [init(spatialMixerDefinition: PHASESpatialMixerDefinition)](/documentation/phase/phaseblendnodedefinition/init(spatialmixerdefinition:))
- [convenience init(spatialMixerDefinition: PHASESpatialMixerDefinition, identifier: String)](/documentation/phase/phaseblendnodedefinition/init(spatialmixerdefinition:identifier:))

#### Accessing Blend Properties

- [var blendParameterDefinition: PHASENumberMetaParameterDefinition?](/documentation/phase/phaseblendnodedefinition/blendparameterdefinition)
- [var spatialMixerDefinitionForDistance: PHASESpatialMixerDefinition?](/documentation/phase/phaseblendnodedefinition/spatialmixerdefinitionfordistance)

#### Adding Child Nodes

- [func addRange(envelope: PHASEEnvelope, subtree: PHASESoundEventNodeDefinition)](/documentation/phase/phaseblendnodedefinition/addrange(envelope:subtree:))
- [func addRangeForInputValuesAbove(value: Double, fullGainAtValue: Double, fadeCurveType: PHASECurveType, subtree: PHASESoundEventNodeDefinition)](/documentation/phase/phaseblendnodedefinition/addrangeforinputvaluesabove(value:fullgainatvalue:fadecurvetype:subtree:))
- [func addRangeForInputValuesBelow(value: Double, fullGainAtValue: Double, fadeCurveType: PHASECurveType, subtree: PHASESoundEventNodeDefinition)](/documentation/phase/phaseblendnodedefinition/addrangeforinputvaluesbelow(value:fullgainatvalue:fadecurvetype:subtree:))
- [func addRangeForInputValuesBetween(lowValue: Double, highValue: Double, fullGainAtLowValue: Double, fullGainAtHighValue: Double, lowFadeCurveType: PHASECurveType, highFadeCurveType: PHASECurveType, subtree: PHASESoundEventNodeDefinition)](/documentation/phase/phaseblendnodedefinition/addrangeforinputvaluesbetween(lowvalue:highvalue:fullgainatlowvalue:fullgainathighvalue:lowfadecurvetype:highfadecurvetype:subtree:))
- [PHASEContainerNodeDefinition](/documentation/phase/phasecontainernodedefinition)

#### Creating a Node

- [init()](/documentation/phase/phasecontainernodedefinition/init())
- [init(identifier: String)](/documentation/phase/phasecontainernodedefinition/init(identifier:))
- [class func new() -> Self](/documentation/phase/phasecontainernodedefinition/new())

#### Adding Descendent Nodes

- [func addSubtree(PHASESoundEventNodeDefinition)](/documentation/phase/phasecontainernodedefinition/addsubtree(_:))

## Audio Layering and Effects

- [PHASEChannelMixerDefinition](/documentation/phase/phasechannelmixerdefinition)

### Creating a Channel Mixer

- [init(channelLayout: AVAudioChannelLayout)](/documentation/phase/phasechannelmixerdefinition/init(channellayout:))
- [convenience init(channelLayout: AVAudioChannelLayout, identifier: String)](/documentation/phase/phasechannelmixerdefinition/init(channellayout:identifier:))

### Inspecting Channel Layout

- [var inputChannelLayout: AVAudioChannelLayout](/documentation/phase/phasechannelmixerdefinition/inputchannellayout)
- [PHASEAmbientMixerDefinition](/documentation/phase/phaseambientmixerdefinition)

### Creating an Ambient Mixer

- [init(channelLayout: AVAudioChannelLayout, orientation: simd_quatf)](/documentation/phase/phaseambientmixerdefinition/init(channellayout:orientation:))
- [convenience init(channelLayout: AVAudioChannelLayout, orientation: simd_quatf, identifier: String)](/documentation/phase/phaseambientmixerdefinition/init(channellayout:orientation:identifier:))

### Inspecting the Mixer

- [var inputChannelLayout: AVAudioChannelLayout](/documentation/phase/phaseambientmixerdefinition/inputchannellayout)
- [var orientation: simd_quatf](/documentation/phase/phaseambientmixerdefinition/orientation)
- [PHASEMixerDefinition](/documentation/phase/phasemixerdefinition)

### Controlling Volume

- [var gain: Double](/documentation/phase/phasemixerdefinition/gain)
- [var gainMetaParameterDefinition: PHASENumberMetaParameterDefinition?](/documentation/phase/phasemixerdefinition/gainmetaparameterdefinition)
- [PHASEMixer](/documentation/phase/phasemixer)

### Adjusting Volume

- [var gain: Double](/documentation/phase/phasemixer/gain)
- [var gainMetaParameter: PHASEMetaParameter?](/documentation/phase/phasemixer/gainmetaparameter)

### Retrieving the Mixer Identifier

- [var identifier: String](/documentation/phase/phasemixer/identifier)
- [PHASEDefinition](/documentation/phase/phasedefinition)

### Identifying a Definition

- [var identifier: String](/documentation/phase/phasedefinition/identifier)
- [Spatial Mixing](/documentation/phase/spatial-mixing)

### Setup

- [PHASESpatialMixerDefinition](/documentation/phase/phasespatialmixerdefinition)

#### Creating a Spatial Mixer

- [init(spatialPipeline: PHASESpatialPipeline)](/documentation/phase/phasespatialmixerdefinition/init(spatialpipeline:))
- [convenience init(spatialPipeline: PHASESpatialPipeline, identifier: String)](/documentation/phase/phasespatialmixerdefinition/init(spatialpipeline:identifier:))

#### Setting a Pipeline

- [var spatialPipeline: PHASESpatialPipeline](/documentation/phase/phasespatialmixerdefinition/spatialpipeline)

#### Changing Sound Over Distance

- [var distanceModelParameters: PHASEDistanceModelParameters?](/documentation/phase/phasespatialmixerdefinition/distancemodelparameters)

#### Configuring Directivity

- [var listenerDirectivityModelParameters: PHASEDirectivityModelParameters?](/documentation/phase/phasespatialmixerdefinition/listenerdirectivitymodelparameters)
- [var sourceDirectivityModelParameters: PHASEDirectivityModelParameters?](/documentation/phase/phasespatialmixerdefinition/sourcedirectivitymodelparameters)

### Sound Reflections and Resonance

- [PHASESpatialPipeline](/documentation/phase/phasespatialpipeline)

#### Creating a Spatial Pipeline

- [init?(flags: PHASESpatialPipeline.Flags)](/documentation/phase/phasespatialpipeline/init(flags:))
- [PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct)

##### Creating a Flag

- [init(rawValue: UInt)](/documentation/phase/phasespatialpipeline/flags-swift.struct/init(rawvalue:))

##### Choosing a Flag

- [static var directPathTransmission: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/directpathtransmission)
- [static var earlyReflections: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/earlyreflections)
- [static var lateReverb: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/latereverb)

#### Inspecting Effects

- [var flags: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.property)
- [var entries: [PHASESpatialCategory : PHASESpatialPipelineEntry]](/documentation/phase/phasespatialpipeline/entries)
- [PHASESpatialPipelineEntry](/documentation/phase/phasespatialpipelineentry)

#### Setting the Send Level

- [var sendLevel: Double](/documentation/phase/phasespatialpipelineentry/sendlevel)

#### Fading the Send Level

- [var sendLevelMetaParameterDefinition: PHASENumberMetaParameterDefinition?](/documentation/phase/phasespatialpipelineentry/sendlevelmetaparameterdefinition)
- [PHASESpatialCategory](/documentation/phase/phasespatialcategory)

#### Creating a Spatial Category

- [init(rawValue: String)](/documentation/phase/phasespatialcategory/init(rawvalue:))

#### Categories

- [static let directPathTransmission: PHASESpatialCategory](/documentation/phase/phasespatialcategory/directpathtransmission)
- [static let earlyReflections: PHASESpatialCategory](/documentation/phase/phasespatialcategory/earlyreflections)
- [static let lateReverb: PHASESpatialCategory](/documentation/phase/phasespatialcategory/latereverb)
- [PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct)

#### Creating a Flag

- [init(rawValue: UInt)](/documentation/phase/phasespatialpipeline/flags-swift.struct/init(rawvalue:))

#### Choosing a Flag

- [static var directPathTransmission: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/directpathtransmission)
- [static var earlyReflections: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/earlyreflections)
- [static var lateReverb: PHASESpatialPipeline.Flags](/documentation/phase/phasespatialpipeline/flags-swift.struct/latereverb)

### Distance Modeling

- [PHASEGeometricSpreadingDistanceModelParameters](/documentation/phase/phasegeometricspreadingdistancemodelparameters)

#### Creating the Distance Model Parameters

- [init()](/documentation/phase/phasegeometricspreadingdistancemodelparameters/init())

#### Setting the Roll-Off Factor

- [var rolloffFactor: Double](/documentation/phase/phasegeometricspreadingdistancemodelparameters/rollofffactor)
- [PHASEEnvelopeDistanceModelParameters](/documentation/phase/phaseenvelopedistancemodelparameters)

#### Creating the Distance Model Parameters

- [init(envelope: PHASEEnvelope)](/documentation/phase/phaseenvelopedistancemodelparameters/init(envelope:))

#### Shaping the Volume Over a Distance

- [var envelope: PHASEEnvelope](/documentation/phase/phaseenvelopedistancemodelparameters/envelope)
- [PHASEDistanceModelFadeOutParameters](/documentation/phase/phasedistancemodelfadeoutparameters)

#### Creating the Distance Model Fade-Out Parameters

- [init(cullDistance: Double)](/documentation/phase/phasedistancemodelfadeoutparameters/init(culldistance:))

#### Inspecting the Cull Distance

- [var cullDistance: Double](/documentation/phase/phasedistancemodelfadeoutparameters/culldistance)
- [PHASEDistanceModelParameters](/documentation/phase/phasedistancemodelparameters)

#### Fading the Sound

- [var fadeOutParameters: PHASEDistanceModelFadeOutParameters?](/documentation/phase/phasedistancemodelparameters/fadeoutparameters)

### Sound Directivity

- [PHASECardioidDirectivityModelParameters](/documentation/phase/phasecardioiddirectivitymodelparameters)

#### Creating the Cardioid Directivity Model Parameters

- [init(subbandParameters: [PHASECardioidDirectivityModelSubbandParameters])](/documentation/phase/phasecardioiddirectivitymodelparameters/init(subbandparameters:))

#### Defining Subbands

- [var subbandParameters: [PHASECardioidDirectivityModelSubbandParameters]](/documentation/phase/phasecardioiddirectivitymodelparameters/subbandparameters)
- [PHASECardioidDirectivityModelSubbandParameters](/documentation/phase/phasecardioiddirectivitymodelsubbandparameters)

#### Creating Cardioid Directivity Subband Parameters

- [init()](/documentation/phase/phasecardioiddirectivitymodelsubbandparameters/init())

#### Sizing the Subband

- [var frequency: Double](/documentation/phase/phasecardioiddirectivitymodelsubbandparameters/frequency)

#### Shaping Directivity

- [var pattern: Double](/documentation/phase/phasecardioiddirectivitymodelsubbandparameters/pattern)
- [var sharpness: Double](/documentation/phase/phasecardioiddirectivitymodelsubbandparameters/sharpness)
- [PHASEConeDirectivityModelParameters](/documentation/phase/phaseconedirectivitymodelparameters)

#### Creating the Cone Directivity Model Parameters

- [init(subbandParameters: [PHASEConeDirectivityModelSubbandParameters])](/documentation/phase/phaseconedirectivitymodelparameters/init(subbandparameters:))

#### Defining Subbands

- [var subbandParameters: [PHASEConeDirectivityModelSubbandParameters]](/documentation/phase/phaseconedirectivitymodelparameters/subbandparameters)
- [PHASEConeDirectivityModelSubbandParameters](/documentation/phase/phaseconedirectivitymodelsubbandparameters)

#### Creating Cone Directivity Subband Parameters

- [init()](/documentation/phase/phaseconedirectivitymodelsubbandparameters/init())

#### Sizing the Subband

- [var frequency: Double](/documentation/phase/phaseconedirectivitymodelsubbandparameters/frequency)

#### Shaping Directivity

- [var innerAngle: Double](/documentation/phase/phaseconedirectivitymodelsubbandparameters/innerangle)
- [var outerAngle: Double](/documentation/phase/phaseconedirectivitymodelsubbandparameters/outerangle)
- [var outerGain: Double](/documentation/phase/phaseconedirectivitymodelsubbandparameters/outergain)
- [func setAngles(innerAngle: Double, outerAngle: Double)](/documentation/phase/phaseconedirectivitymodelsubbandparameters/setangles(innerangle:outerangle:))
- [PHASEDirectivityModelParameters](/documentation/phase/phasedirectivitymodelparameters)

## Dynamic Sound Control

- [PHASEEnvelope](/documentation/phase/phaseenvelope)

### Creating an Envelope

- [init?(startPoint: simd_double2, segments: [PHASEEnvelopeSegment])](/documentation/phase/phaseenvelope/init(startpoint:segments:))

### Inspecting the Envelope

- [func evaluate(x: Double) -> Double](/documentation/phase/phaseenvelope/evaluate(x:))
- [var segments: [PHASEEnvelopeSegment]](/documentation/phase/phaseenvelope/segments)
- [var startPoint: simd_double2](/documentation/phase/phaseenvelope/startpoint)

### Bounding the Input

- [var domain: PHASENumericPair](/documentation/phase/phaseenvelope/domain)
- [var range: PHASENumericPair](/documentation/phase/phaseenvelope/range)
- [PHASEEnvelopeSegment](/documentation/phase/phaseenvelopesegment)

### Creating a Segment

- [init(endPoint: simd_double2, curveType: PHASECurveType)](/documentation/phase/phaseenvelopesegment/init(endpoint:curvetype:))

### Shaping a Segment

- [var curveType: PHASECurveType](/documentation/phase/phaseenvelopesegment/curvetype)
- [var endPoint: simd_double2](/documentation/phase/phaseenvelopesegment/endpoint)
- [PHASECurveType](/documentation/phase/phasecurvetype)

### Types

- [case linear](/documentation/phase/phasecurvetype/linear)
- [case squared](/documentation/phase/phasecurvetype/squared)
- [case inverseSquared](/documentation/phase/phasecurvetype/inversesquared)
- [case cubed](/documentation/phase/phasecurvetype/cubed)
- [case inverseCubed](/documentation/phase/phasecurvetype/inversecubed)
- [case sine](/documentation/phase/phasecurvetype/sine)
- [case inverseSine](/documentation/phase/phasecurvetype/inversesine)
- [case sigmoid](/documentation/phase/phasecurvetype/sigmoid)
- [case inverseSigmoid](/documentation/phase/phasecurvetype/inversesigmoid)
- [case holdStartValue](/documentation/phase/phasecurvetype/holdstartvalue)
- [case jumpToEndValue](/documentation/phase/phasecurvetype/jumptoendvalue)

### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasecurvetype/init(rawvalue:))
- [PHASENumericPair](/documentation/phase/phasenumericpair)

### Creating a Numeric Pair

- [init(firstValue: Double, secondValue: Double)](/documentation/phase/phasenumericpair/init(firstvalue:secondvalue:))

### Defining the Values

- [var first: Double](/documentation/phase/phasenumericpair/first)
- [var second: Double](/documentation/phase/phasenumericpair/second)
- [Playback Parameterization](/documentation/phase/playback-parameterization)

### Base Metaparameters

- [PHASEMetaParameter](/documentation/phase/phasemetaparameter)

#### Accessing the Value

- [var value: Any](/documentation/phase/phasemetaparameter/value)

#### Identifying the Parameter

- [var identifier: String](/documentation/phase/phasemetaparameter/identifier)
- [PHASEMetaParameterDefinition](/documentation/phase/phasemetaparameterdefinition)

#### Setting a Metaparameter

- [var value: Any](/documentation/phase/phasemetaparameterdefinition/value)
- [PHASEGlobalMetaParameterAsset](/documentation/phase/phaseglobalmetaparameterasset)

### Linear Metaparameters

- [PHASENumberMetaParameter](/documentation/phase/phasenumbermetaparameter)

#### Inspecting Extremes

- [var minimum: Double](/documentation/phase/phasenumbermetaparameter/minimum)
- [var maximum: Double](/documentation/phase/phasenumbermetaparameter/maximum)

#### Interpolating the Value

- [func fade(value: Double, duration: TimeInterval)](/documentation/phase/phasenumbermetaparameter/fade(value:duration:))
- [PHASENumberMetaParameterDefinition](/documentation/phase/phasenumbermetaparameterdefinition)

#### Creating a Metaparameter Definition

- [convenience init(value: Double)](/documentation/phase/phasenumbermetaparameterdefinition/init(value:))
- [convenience init(value: Double, identifier: String)](/documentation/phase/phasenumbermetaparameterdefinition/init(value:identifier:))
- [init(value: Double, minimum: Double, maximum: Double)](/documentation/phase/phasenumbermetaparameterdefinition/init(value:minimum:maximum:))
- [convenience init(value: Double, minimum: Double, maximum: Double, identifier: String)](/documentation/phase/phasenumbermetaparameterdefinition/init(value:minimum:maximum:identifier:))

#### Reistricting the Value

- [var minimum: Double](/documentation/phase/phasenumbermetaparameterdefinition/minimum)
- [var maximum: Double](/documentation/phase/phasenumbermetaparameterdefinition/maximum)

### Textual Metaparameters

- [PHASEStringMetaParameter](/documentation/phase/phasestringmetaparameter)
- [PHASEStringMetaParameterDefinition](/documentation/phase/phasestringmetaparameterdefinition)

#### Creating a Parameter Definition

- [init(value: String)](/documentation/phase/phasestringmetaparameterdefinition/init(value:))
- [convenience init(value: String, identifier: String)](/documentation/phase/phasestringmetaparameterdefinition/init(value:identifier:))

### Graphed Metaparameters

- [PHASEMappedMetaParameterDefinition](/documentation/phase/phasemappedmetaparameterdefinition)

#### Creating a Mapped Metaparameter

- [init(inputMetaParameterDefinition: PHASENumberMetaParameterDefinition, envelope: PHASEEnvelope)](/documentation/phase/phasemappedmetaparameterdefinition/init(inputmetaparameterdefinition:envelope:))
- [convenience init(inputMetaParameterDefinition: PHASENumberMetaParameterDefinition, envelope: PHASEEnvelope, identifier: String)](/documentation/phase/phasemappedmetaparameterdefinition/init(inputmetaparameterdefinition:envelope:identifier:))

#### Inspecting the Input Parameter

- [var inputMetaParameterDefinition: PHASENumberMetaParameterDefinition](/documentation/phase/phasemappedmetaparameterdefinition/inputmetaparameterdefinition)

#### Inspecting the Envelope

- [var envelope: PHASEEnvelope](/documentation/phase/phasemappedmetaparameterdefinition/envelope)

## Sound Grouping and Management

- [PHASEGroup](/documentation/phase/phasegroup)

### Creating a Group

- [init(identifier: String)](/documentation/phase/phasegroup/init(identifier:))

### Identifying the Group

- [var identifier: String](/documentation/phase/phasegroup/identifier)

### Defining the Group

- [func register(engine: PHASEEngine)](/documentation/phase/phasegroup/register(engine:))
- [func unregisterFromEngine()](/documentation/phase/phasegroup/unregisterfromengine())

### Conrolling Loudness

- [var gain: Double](/documentation/phase/phasegroup/gain)
- [func fadeGain(gain: Double, duration: Double, curveType: PHASECurveType)](/documentation/phase/phasegroup/fadegain(gain:duration:curvetype:))

### Adjusting Playback Speed

- [var rate: Double](/documentation/phase/phasegroup/rate)
- [func fadeRate(rate: Double, duration: Double, curveType: PHASECurveType)](/documentation/phase/phasegroup/faderate(rate:duration:curvetype:))

### Silencing Sounds

- [func mute()](/documentation/phase/phasegroup/mute())
- [func unmute()](/documentation/phase/phasegroup/unmute())
- [var isMuted: Bool](/documentation/phase/phasegroup/ismuted)
- [func solo()](/documentation/phase/phasegroup/solo())
- [func unsolo()](/documentation/phase/phasegroup/unsolo())
- [var isSoloed: Bool](/documentation/phase/phasegroup/issoloed)
- [PHASEGroupPreset](/documentation/phase/phasegrouppreset)

### Creating a Group Preset

- [init(engine: PHASEEngine, settings: [String : PHASEGroupPresetSetting], timeToTarget: Double, timeToReset: Double)](/documentation/phase/phasegrouppreset/init(engine:settings:timetotarget:timetoreset:))

### Applying Settings

- [var settings: [String : PHASEGroupPresetSetting]](/documentation/phase/phasegrouppreset/settings)

### Fading Between Settings

- [var timeToTarget: Double](/documentation/phase/phasegrouppreset/timetotarget)
- [var timeToReset: Double](/documentation/phase/phasegrouppreset/timetoreset)

### Activating a Group Preset

- [func activate()](/documentation/phase/phasegrouppreset/activate())
- [func activate(timeToTargetOverride: Double)](/documentation/phase/phasegrouppreset/activate(timetotargetoverride:))

### Deactivating a Group Preset

- [func deactivate()](/documentation/phase/phasegrouppreset/deactivate())
- [func deactivate(timeToResetOverride: Double)](/documentation/phase/phasegrouppreset/deactivate(timetoresetoverride:))
- [PHASEGroupPresetSetting](/documentation/phase/phasegrouppresetsetting)

### Creating a Setting

- [init(gain: Double, rate: Double, gainCurveType: PHASECurveType, rateCurveType: PHASECurveType)](/documentation/phase/phasegrouppresetsetting/init(gain:rate:gaincurvetype:ratecurvetype:))

### Setting Loudness

- [var gain: Double](/documentation/phase/phasegrouppresetsetting/gain)
- [var gainCurveType: PHASECurveType](/documentation/phase/phasegrouppresetsetting/gaincurvetype)

### Setting Playback Speed

- [var rate: Double](/documentation/phase/phasegrouppresetsetting/rate)
- [var rateCurveType: PHASECurveType](/documentation/phase/phasegrouppresetsetting/ratecurvetype)
- [PHASEDucker](/documentation/phase/phaseducker)

### Creating a Ducker

- [init(engine: PHASEEngine, sourceGroups: Set<PHASEGroup>, targetGroups: Set<PHASEGroup>, gain: Double, attackTime: Double, releaseTime: Double, attackCurve: PHASECurveType, releaseCurve: PHASECurveType)](/documentation/phase/phaseducker/init(engine:sourcegroups:targetgroups:gain:attacktime:releasetime:attackcurve:releasecurve:))

### Specifying Sounds

- [var sourceGroups: Set<PHASEGroup>](/documentation/phase/phaseducker/sourcegroups)
- [var targetGroups: Set<PHASEGroup>](/documentation/phase/phaseducker/targetgroups)

### Configuring Volume Reduction

- [var gain: Double](/documentation/phase/phaseducker/gain)
- [var identifier: String](/documentation/phase/phaseducker/identifier)
- [var isActive: Bool](/documentation/phase/phaseducker/isactive)
- [var attackTime: Double](/documentation/phase/phaseducker/attacktime)
- [var attackCurve: PHASECurveType](/documentation/phase/phaseducker/attackcurve)
- [var releaseTime: Double](/documentation/phase/phaseducker/releasetime)
- [var releaseCurve: PHASECurveType](/documentation/phase/phaseducker/releasecurve)

### Altering Sound

- [func activate()](/documentation/phase/phaseducker/activate())
- [func deactivate()](/documentation/phase/phaseducker/deactivate())

## Errors

- [PHASE Errors](/documentation/phase/phase-errors)

### Framework Errors

- [PHASEError](/documentation/phase/phaseerror-swift.struct)

#### Identifying an Error Cause

- [static var initializeFailed: PHASEError.Code](/documentation/phase/phaseerror-swift.struct/initializefailed)
- [static var invalidObject: PHASEError.Code](/documentation/phase/phaseerror-swift.struct/invalidobject)

#### Creating an Error

- [PHASEError.Code](/documentation/phase/phaseerror-swift.struct/code)

##### Errors

- [case initializeFailed](/documentation/phase/phaseerror-swift.struct/code/initializefailed)
- [case invalidObject](/documentation/phase/phaseerror-swift.struct/code/invalidobject)

##### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseerror-swift.struct/code/init(rawvalue:))

#### Type Properties

- [static var errorDomain: String](/documentation/phase/phaseerror-swift.struct/errordomain)
- [PHASEError.Code](/documentation/phase/phaseerror-swift.struct/code)

#### Errors

- [case initializeFailed](/documentation/phase/phaseerror-swift.struct/code/initializefailed)
- [case invalidObject](/documentation/phase/phaseerror-swift.struct/code/invalidobject)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseerror-swift.struct/code/init(rawvalue:))
- [let PHASEErrorDomain: String](/documentation/phase/phaseerrordomain)

### Asset Errors

- [PHASEAssetError](/documentation/phase/phaseasseterror-swift.struct)

#### Creating an Error

- [PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/code)

##### Errors

- [case alreadyExists](/documentation/phase/phaseasseterror-swift.struct/code/alreadyexists)
- [case badParameters](/documentation/phase/phaseasseterror-swift.struct/code/badparameters)
- [case failedToLoad](/documentation/phase/phaseasseterror-swift.struct/code/failedtoload)
- [case generalError](/documentation/phase/phaseasseterror-swift.struct/code/generalerror)
- [case invalidEngineInstance](/documentation/phase/phaseasseterror-swift.struct/code/invalidengineinstance)
- [case memoryAllocation](/documentation/phase/phaseasseterror-swift.struct/code/memoryallocation)

##### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseasseterror-swift.struct/code/init(rawvalue:))

#### Identifying an Error Cause

- [static var alreadyExists: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/alreadyexists)
- [static var badParameters: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/badparameters)
- [static var failedToLoad: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/failedtoload)
- [static var generalError: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/generalerror)
- [static var invalidEngineInstance: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/invalidengineinstance)
- [static var memoryAllocation: PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/memoryallocation)

#### Type Properties

- [static var errorDomain: String](/documentation/phase/phaseasseterror-swift.struct/errordomain)
- [PHASEAssetError.Code](/documentation/phase/phaseasseterror-swift.struct/code)

#### Errors

- [case alreadyExists](/documentation/phase/phaseasseterror-swift.struct/code/alreadyexists)
- [case badParameters](/documentation/phase/phaseasseterror-swift.struct/code/badparameters)
- [case failedToLoad](/documentation/phase/phaseasseterror-swift.struct/code/failedtoload)
- [case generalError](/documentation/phase/phaseasseterror-swift.struct/code/generalerror)
- [case invalidEngineInstance](/documentation/phase/phaseasseterror-swift.struct/code/invalidengineinstance)
- [case memoryAllocation](/documentation/phase/phaseasseterror-swift.struct/code/memoryallocation)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phaseasseterror-swift.struct/code/init(rawvalue:))
- [let PHASEAssetErrorDomain: String](/documentation/phase/phaseasseterrordomain)

### Sound Event Errors

- [PHASESoundEventError](/documentation/phase/phasesoundeventerror-swift.struct)

#### Creating an Error

- [PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/code)

##### Errors

- [case apiMisuse](/documentation/phase/phasesoundeventerror-swift.struct/code/apimisuse)
- [case badData](/documentation/phase/phasesoundeventerror-swift.struct/code/baddata)
- [case invalidInstance](/documentation/phase/phasesoundeventerror-swift.struct/code/invalidinstance)
- [case notFound](/documentation/phase/phasesoundeventerror-swift.struct/code/notfound)
- [case outOfMemory](/documentation/phase/phasesoundeventerror-swift.struct/code/outofmemory)
- [case systemNotInitialized](/documentation/phase/phasesoundeventerror-swift.struct/code/systemnotinitialized)

##### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundeventerror-swift.struct/code/init(rawvalue:))

#### Identifying an Error Cause

- [static var apiMisuse: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/apimisuse)
- [static var badData: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/baddata)
- [static var invalidInstance: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/invalidinstance)
- [static var notFound: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/notfound)
- [static var outOfMemory: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/outofmemory)
- [static var systemNotInitialized: PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/systemnotinitialized)

#### Type Properties

- [static var errorDomain: String](/documentation/phase/phasesoundeventerror-swift.struct/errordomain)
- [PHASESoundEventError.Code](/documentation/phase/phasesoundeventerror-swift.struct/code)

#### Errors

- [case apiMisuse](/documentation/phase/phasesoundeventerror-swift.struct/code/apimisuse)
- [case badData](/documentation/phase/phasesoundeventerror-swift.struct/code/baddata)
- [case invalidInstance](/documentation/phase/phasesoundeventerror-swift.struct/code/invalidinstance)
- [case notFound](/documentation/phase/phasesoundeventerror-swift.struct/code/notfound)
- [case outOfMemory](/documentation/phase/phasesoundeventerror-swift.struct/code/outofmemory)
- [case systemNotInitialized](/documentation/phase/phasesoundeventerror-swift.struct/code/systemnotinitialized)

#### Initializers

- [init?(rawValue: Int)](/documentation/phase/phasesoundeventerror-swift.struct/code/init(rawvalue:))
- [let PHASESoundEventErrorDomain: String](/documentation/phase/phasesoundeventerrordomain)

## Classes

- [PHASEPullStreamNode](/documentation/phase/phasepullstreamnode)

### Instance Properties

- [var renderHandler: PHASEPullStreamRenderHandler](/documentation/phase/phasepullstreamnode/renderhandler)
- [PHASEPullStreamNodeDefinition](/documentation/phase/phasepullstreamnodedefinition)

### Initializers

- [init(mixerDefinition: PHASEMixerDefinition, format: AVAudioFormat)](/documentation/phase/phasepullstreamnodedefinition/init(mixerdefinition:format:))
- [convenience init(mixerDefinition: PHASEMixerDefinition, format: AVAudioFormat, identifier: String)](/documentation/phase/phasepullstreamnodedefinition/init(mixerdefinition:format:identifier:))

### Instance Properties

- [var format: AVAudioFormat](/documentation/phase/phasepullstreamnodedefinition/format)
- [var normalize: Bool](/documentation/phase/phasepullstreamnodedefinition/normalize)
- [PHASEStreamNode](/documentation/phase/phasestreamnode)

### Instance Properties

- [var format: AVAudioFormat](/documentation/phase/phasestreamnode/format)
- [var gainMetaParameter: PHASENumberMetaParameter?](/documentation/phase/phasestreamnode/gainmetaparameter)
- [var mixer: PHASEMixer](/documentation/phase/phasestreamnode/mixer)
- [var rateMetaParameter: PHASENumberMetaParameter?](/documentation/phase/phasestreamnode/ratemetaparameter)

## Structures

- [PHASEAutomaticHeadTrackingFlags](/documentation/phase/phaseautomaticheadtrackingflags)

### Initializers

- [init(rawValue: UInt)](/documentation/phase/phaseautomaticheadtrackingflags/init(rawvalue:))

### Type Properties

- [static var orientation: PHASEAutomaticHeadTrackingFlags](/documentation/phase/phaseautomaticheadtrackingflags/orientation)
- [static var position: PHASEAutomaticHeadTrackingFlags](/documentation/phase/phaseautomaticheadtrackingflags/position)

## Type Aliases

- [PHASEPullStreamRenderHandler](/documentation/phase/phasepullstreamrenderhandler)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
