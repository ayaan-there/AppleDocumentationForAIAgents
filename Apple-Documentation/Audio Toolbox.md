# Audio Toolbox Documentation

Source: https://sosumi.ai/documentation/audiotoolbox

---
title: Audio Toolbox
source: https://developer.apple.com/documentation/audiotoolbox
timestamp: 2026-02-13T18:53:58.247Z
---

## Essentials

- [Porting your audio code to Apple silicon](/documentation/apple-silicon/porting-your-audio-code-to-apple-silicon)

## Audio Units

- [Generating spatial audio from a multichannel audio stream](/documentation/audiotoolbox/generating-spatial-audio-from-a-multichannel-audio-stream)
- [Audio Unit v3 Plug-Ins](/documentation/audiotoolbox/audio-unit-v3-plug-ins)

### Host App

- [Migrating Your Audio Unit Host to the AUv3 API](/documentation/audiotoolbox/migrating-your-audio-unit-host-to-the-auv3-api)
- [Hosting Audio Unit Extensions Using the AUv2 API](/documentation/audiotoolbox/hosting-audio-unit-extensions-using-the-auv2-api)

### Audio Units

- [Creating an audio unit extension](/documentation/avfaudio/creating-an-audio-unit-extension)
- [Creating custom audio effects](/documentation/avfaudio/creating-custom-audio-effects)
- [Incorporating Audio Effects and Instruments](/documentation/audiotoolbox/incorporating-audio-effects-and-instruments)
- [Debugging Out-of-Process Audio Units on Apple Silicon](/documentation/audiotoolbox/debugging-out-of-process-audio-units-on-apple-silicon)
- [AUAudioUnit](/documentation/audiotoolbox/auaudiounit)

#### Creating an Audio Unit

- [convenience init(componentDescription: AudioComponentDescription) throws](/documentation/audiotoolbox/auaudiounit/init(componentdescription:))
- [init(componentDescription: AudioComponentDescription, options: AudioComponentInstantiationOptions) throws](/documentation/audiotoolbox/auaudiounit/init(componentdescription:options:))
- [class func instantiate(with: AudioComponentDescription, options: AudioComponentInstantiationOptions, completionHandler: (AUAudioUnit?, (any Error)?) -> Void)](/documentation/audiotoolbox/auaudiounit/instantiate(with:options:completionhandler:))

#### Returning the Audio Busses

- [var inputBusses: AUAudioUnitBusArray](/documentation/audiotoolbox/auaudiounit/inputbusses)
- [var outputBusses: AUAudioUnitBusArray](/documentation/audiotoolbox/auaudiounit/outputbusses)

#### Customizing the Audio Unit Behavior

- [class func registerSubclass(AnyClass, as: AudioComponentDescription, name: String, version: UInt32)](/documentation/audiotoolbox/auaudiounit/registersubclass(_:as:name:version:))
- [func shouldChange(to: AVAudioFormat, for: AUAudioUnitBus) -> Bool](/documentation/audiotoolbox/auaudiounit/shouldchange(to:for:))
- [func setRenderResourcesAllocated(Bool)](/documentation/audiotoolbox/auaudiounit/setrenderresourcesallocated(_:))
- [var internalRenderBlock: AUInternalRenderBlock](/documentation/audiotoolbox/auaudiounit/internalrenderblock)
- [var midiOutputBufferSizeHint: Int](/documentation/audiotoolbox/auaudiounit/midioutputbuffersizehint)
- [AUInternalRenderBlock](/documentation/audiotoolbox/auinternalrenderblock)

#### Querying Parameters

- [var parameterTree: AUParameterTree?](/documentation/audiotoolbox/auaudiounit/parametertree)
- [var allParameterValues: Bool](/documentation/audiotoolbox/auaudiounit/allparametervalues)
- [func parametersForOverview(withCount: Int) -> [NSNumber]](/documentation/audiotoolbox/auaudiounit/parametersforoverview(withcount:))

#### Providing Data to the Host

- [var musicalContextBlock: AUHostMusicalContextBlock?](/documentation/audiotoolbox/auaudiounit/musicalcontextblock)
- [var transportStateBlock: AUHostTransportStateBlock?](/documentation/audiotoolbox/auaudiounit/transportstateblock)
- [var contextName: String?](/documentation/audiotoolbox/auaudiounit/contextname)
- [var supportsMPE: Bool](/documentation/audiotoolbox/auaudiounit/supportsmpe)
- [AUHostMusicalContextBlock](/documentation/audiotoolbox/auhostmusicalcontextblock)
- [AUHostTransportStateBlock](/documentation/audiotoolbox/auhosttransportstateblock)

#### Managing MIDI Events

- [var isMusicDeviceOrEffect: Bool](/documentation/audiotoolbox/auaudiounit/ismusicdeviceoreffect)
- [var virtualMIDICableCount: Int](/documentation/audiotoolbox/auaudiounit/virtualmidicablecount)
- [var scheduleMIDIEventBlock: AUScheduleMIDIEventBlock?](/documentation/audiotoolbox/auaudiounit/schedulemidieventblock)
- [var midiOutputEventBlock: AUMIDIOutputEventBlock?](/documentation/audiotoolbox/auaudiounit/midioutputeventblock)
- [var midiOutputNames: [String]](/documentation/audiotoolbox/auaudiounit/midioutputnames)
- [AUScheduleMIDIEventBlock](/documentation/audiotoolbox/auschedulemidieventblock)
- [AUMIDIOutputEventBlock](/documentation/audiotoolbox/aumidioutputeventblock)

#### Managing Presets

- [var fullState: [String : Any]?](/documentation/audiotoolbox/auaudiounit/fullstate)
- [var fullStateForDocument: [String : Any]?](/documentation/audiotoolbox/auaudiounit/fullstatefordocument)
- [var factoryPresets: [AUAudioUnitPreset]?](/documentation/audiotoolbox/auaudiounit/factorypresets)
- [var currentPreset: AUAudioUnitPreset?](/documentation/audiotoolbox/auaudiounit/currentpreset)
- [var supportsUserPresets: Bool](/documentation/audiotoolbox/auaudiounit/supportsuserpresets)
- [var userPresets: [AUAudioUnitPreset]](/documentation/audiotoolbox/auaudiounit/userpresets)
- [func saveUserPreset(AUAudioUnitPreset) throws](/documentation/audiotoolbox/auaudiounit/saveuserpreset(_:))
- [func deleteUserPreset(AUAudioUnitPreset) throws](/documentation/audiotoolbox/auaudiounit/deleteuserpreset(_:))
- [func presetState(for: AUAudioUnitPreset) throws -> [String : Any]](/documentation/audiotoolbox/auaudiounit/presetstate(for:))

#### Managing the Render Cycle

- [func allocateRenderResources() throws](/documentation/audiotoolbox/auaudiounit/allocaterenderresources())
- [func deallocateRenderResources()](/documentation/audiotoolbox/auaudiounit/deallocaterenderresources())
- [func reset()](/documentation/audiotoolbox/auaudiounit/reset())
- [var renderResourcesAllocated: Bool](/documentation/audiotoolbox/auaudiounit/renderresourcesallocated)
- [var renderBlock: AURenderBlock](/documentation/audiotoolbox/auaudiounit/renderblock)
- [var scheduleParameterBlock: AUScheduleParameterBlock](/documentation/audiotoolbox/auaudiounit/scheduleparameterblock)
- [var maximumFramesToRender: AUAudioFrameCount](/documentation/audiotoolbox/auaudiounit/maximumframestorender)
- [func token(byAddingRenderObserver: AURenderObserver) -> Int](/documentation/audiotoolbox/auaudiounit/token(byaddingrenderobserver:))
- [func removeRenderObserver(Int)](/documentation/audiotoolbox/auaudiounit/removerenderobserver(_:))
- [AURenderObserver](/documentation/audiotoolbox/aurenderobserver)

#### Messaging Channels

- [func messageChannel(for: String) -> any AUMessageChannel](/documentation/audiotoolbox/auaudiounit/messagechannel(for:))
- [AUMessageChannel](/documentation/audiotoolbox/aumessagechannel)

##### Sending a Message to an Audio Unit

- [func callAudioUnit([AnyHashable : Any]) -> [AnyHashable : Any]](/documentation/audiotoolbox/aumessagechannel/callaudiounit(_:))

##### Sending a Message to a Host

- [var callHostBlock: CallHostBlock?](/documentation/audiotoolbox/aumessagechannel/callhostblock)

#### Optimizing Performance

- [var latency: TimeInterval](/documentation/audiotoolbox/auaudiounit/latency)
- [var tailTime: TimeInterval](/documentation/audiotoolbox/auaudiounit/tailtime)
- [var renderQuality: Int](/documentation/audiotoolbox/auaudiounit/renderquality)
- [var shouldBypassEffect: Bool](/documentation/audiotoolbox/auaudiounit/shouldbypasseffect)
- [var canProcessInPlace: Bool](/documentation/audiotoolbox/auaudiounit/canprocessinplace)
- [var isRenderingOffline: Bool](/documentation/audiotoolbox/auaudiounit/isrenderingoffline)

#### Describing the Audio Unit

- [var componentDescription: AudioComponentDescription](/documentation/audiotoolbox/auaudiounit/componentdescription)
- [var component: AudioComponent](/documentation/audiotoolbox/auaudiounit/component)
- [var componentName: String?](/documentation/audiotoolbox/auaudiounit/componentname)
- [var componentVersion: UInt32](/documentation/audiotoolbox/auaudiounit/componentversion)
- [var audioUnitName: String?](/documentation/audiotoolbox/auaudiounit/audiounitname)
- [var audioUnitShortName: String?](/documentation/audiotoolbox/auaudiounit/audiounitshortname)
- [var manufacturerName: String?](/documentation/audiotoolbox/auaudiounit/manufacturername)

#### Configuring the Channel Capabilities

- [var channelCapabilities: [NSNumber]?](/documentation/audiotoolbox/auaudiounit/channelcapabilities)
- [var channelMap: [NSNumber]?](/documentation/audiotoolbox/auaudiounit/channelmap)
- [func profileState(forCable: UInt8, channel: MIDIChannelNumber) -> MIDICIProfileState](/documentation/audiotoolbox/auaudiounit/profilestate(forcable:channel:))
- [func enable(MIDICIProfile, cable: UInt8, onChannel: MIDIChannelNumber) throws](/documentation/audiotoolbox/auaudiounit/enable(_:cable:onchannel:))
- [func disableProfile(MIDICIProfile, cable: UInt8, onChannel: MIDIChannelNumber) throws](/documentation/audiotoolbox/auaudiounit/disableprofile(_:cable:onchannel:))
- [var profileChangedBlock: AUMIDICIProfileChangedBlock?](/documentation/audiotoolbox/auaudiounit/profilechangedblock)

#### Configuring the Device

- [var deviceID: AUAudioObjectID](/documentation/audiotoolbox/auaudiounit/deviceid)
- [func setDeviceID(AUAudioObjectID) throws](/documentation/audiotoolbox/auaudiounit/setdeviceid(_:))
- [var canPerformInput: Bool](/documentation/audiotoolbox/auaudiounit/canperforminput)
- [var canPerformOutput: Bool](/documentation/audiotoolbox/auaudiounit/canperformoutput)
- [var isInputEnabled: Bool](/documentation/audiotoolbox/auaudiounit/isinputenabled)
- [var isOutputEnabled: Bool](/documentation/audiotoolbox/auaudiounit/isoutputenabled)
- [var inputHandler: AUInputHandler?](/documentation/audiotoolbox/auaudiounit/inputhandler)
- [var outputProvider: AURenderPullInputBlock?](/documentation/audiotoolbox/auaudiounit/outputprovider)
- [var deviceInputLatency: TimeInterval](/documentation/audiotoolbox/auaudiounit/deviceinputlatency)
- [var deviceOutputLatency: TimeInterval](/documentation/audiotoolbox/auaudiounit/deviceoutputlatency)
- [func startHardware() throws](/documentation/audiotoolbox/auaudiounit/starthardware())
- [func stopHardware()](/documentation/audiotoolbox/auaudiounit/stophardware())
- [AURenderPullInputBlock](/documentation/audiotoolbox/aurenderpullinputblock)

#### Configuring the User Interface

- [var providesUserInterface: Bool](/documentation/audiotoolbox/auaudiounit/providesuserinterface)
- [func supportedViewConfigurations([AUAudioUnitViewConfiguration]) -> IndexSet](/documentation/audiotoolbox/auaudiounit/supportedviewconfigurations(_:))
- [func select(AUAudioUnitViewConfiguration)](/documentation/audiotoolbox/auaudiounit/select(_:))

#### Getting the Runtime Behavior

- [var isRunning: Bool](/documentation/audiotoolbox/auaudiounit/isrunning)
- [var isLoadedInProcess: Bool](/documentation/audiotoolbox/auaudiounit/isloadedinprocess)

#### Constants

- [AUEventSampleTime](/documentation/audiotoolbox/1387633-aueventsampletime)

##### Constants

- [var AUEventSampleTimeImmediate: AUEventSampleTime](/documentation/audiotoolbox/aueventsampletimeimmediate)
- [AUAudioUnitBusType](/documentation/audiotoolbox/auaudiounitbustype)

##### Constants

- [case input](/documentation/audiotoolbox/auaudiounitbustype/input)
- [case output](/documentation/audiotoolbox/auaudiounitbustype/output)

##### Initializers

- [init?(rawValue: Int)](/documentation/audiotoolbox/auaudiounitbustype/init(rawvalue:))
- [AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags)

##### Constants

- [static var changed: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/changed)
- [static var cycling: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/cycling)
- [static var moving: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/moving)
- [static var recording: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/recording)

##### Initializers

- [init(rawValue: UInt)](/documentation/audiotoolbox/auhosttransportstateflags/init(rawvalue:))
- [AURenderEventType](/documentation/audiotoolbox/aurendereventtype)

##### Constants

- [case MIDI](/documentation/audiotoolbox/aurendereventtype/midi)
- [case midiSysEx](/documentation/audiotoolbox/aurendereventtype/midisysex)
- [case parameter](/documentation/audiotoolbox/aurendereventtype/parameter)
- [case parameterRamp](/documentation/audiotoolbox/aurendereventtype/parameterramp)

##### Enumeration Cases

- [case midiEventList](/documentation/audiotoolbox/aurendereventtype/midieventlist)

##### Initializers

- [init?(rawValue: UInt8)](/documentation/audiotoolbox/aurendereventtype/init(rawvalue:))
- [AURenderBlock](/documentation/audiotoolbox/aurenderblock)
- [AUInputHandler](/documentation/audiotoolbox/auinputhandler)

#### Getting the Audio Unit Presets

- [var kAUPresetNumberKey: String](/documentation/audiotoolbox/kaupresetnumberkey)
- [var kAUPresetCPULoadKey: String](/documentation/audiotoolbox/kaupresetcpuloadkey)
- [var kAUPresetDataKey: String](/documentation/audiotoolbox/kaupresetdatakey)
- [var kAUPresetElementNameKey: String](/documentation/audiotoolbox/kaupresetelementnamekey)
- [var kAUPresetExternalFileRefs: String](/documentation/audiotoolbox/kaupresetexternalfilerefs)
- [var kAUPresetMASDataKey: String](/documentation/audiotoolbox/kaupresetmasdatakey)
- [var kAUPresetManufacturerKey: String](/documentation/audiotoolbox/kaupresetmanufacturerkey)
- [var kAUPresetNameKey: String](/documentation/audiotoolbox/kaupresetnamekey)
- [var kAUPresetPartKey: String](/documentation/audiotoolbox/kaupresetpartkey)
- [var kAUPresetRenderQualityKey: String](/documentation/audiotoolbox/kaupresetrenderqualitykey)
- [var kAUPresetSubtypeKey: String](/documentation/audiotoolbox/kaupresetsubtypekey)
- [var kAUPresetTypeKey: String](/documentation/audiotoolbox/kaupresettypekey)
- [var kAUPresetVSTDataKey: String](/documentation/audiotoolbox/kaupresetvstdatakey)
- [var kAUPresetVSTPresetKey: String](/documentation/audiotoolbox/kaupresetvstpresetkey)
- [var kAUPresetVersionKey: String](/documentation/audiotoolbox/kaupresetversionkey)

#### Instance properties

- [var audioUnitMIDIProtocol: MIDIProtocolID](/documentation/audiotoolbox/auaudiounit/audiounitmidiprotocol)
- [var hostMIDIProtocol: MIDIProtocolID](/documentation/audiotoolbox/auaudiounit/hostmidiprotocol)
- [var midiOutputEventListBlock: AUMIDIEventListBlock?](/documentation/audiotoolbox/auaudiounit/midioutputeventlistblock)
- [var migrateFromPlugin: [Any]](/documentation/audiotoolbox/auaudiounit/migratefromplugin)
- [var scheduleMIDIEventListBlock: AUMIDIEventListBlock?](/documentation/audiotoolbox/auaudiounit/schedulemidieventlistblock)

#### Instance Methods

- [func requestViewController(completionHandler: (UIViewController?) -> Void)](/documentation/audiotoolbox/auaudiounit/requestviewcontroller(completionhandler:))

#### Instance Properties

- [var intendedSpatialExperience: any SpatialAudioExperience](/documentation/audiotoolbox/auaudiounit/intendedspatialexperience-7uqrm)
- [AUAudioUnitBus](/documentation/audiotoolbox/auaudiounitbus)

#### Bus Methods and Properties

- [func setFormat(AVAudioFormat) throws](/documentation/audiotoolbox/auaudiounitbus/setformat(_:))
- [var format: AVAudioFormat](/documentation/audiotoolbox/auaudiounitbus/format)
- [var isEnabled: Bool](/documentation/audiotoolbox/auaudiounitbus/isenabled)
- [var name: String?](/documentation/audiotoolbox/auaudiounitbus/name)
- [var index: Int](/documentation/audiotoolbox/auaudiounitbus/index)
- [var busType: AUAudioUnitBusType](/documentation/audiotoolbox/auaudiounitbus/bustype)
- [var ownerAudioUnit: AUAudioUnit](/documentation/audiotoolbox/auaudiounitbus/owneraudiounit)
- [var supportedChannelLayoutTags: [NSNumber]?](/documentation/audiotoolbox/auaudiounitbus/supportedchannellayouttags)
- [var contextPresentationLatency: TimeInterval](/documentation/audiotoolbox/auaudiounitbus/contextpresentationlatency)
- [var shouldAllocateBuffer: Bool](/documentation/audiotoolbox/auaudiounitbus/shouldallocatebuffer)

#### Audio Unit Implementations

- [init(format: AVAudioFormat) throws](/documentation/audiotoolbox/auaudiounitbus/init(format:))
- [var supportedChannelCounts: [NSNumber]?](/documentation/audiotoolbox/auaudiounitbus/supportedchannelcounts)
- [var maximumChannelCount: AUAudioChannelCount](/documentation/audiotoolbox/auaudiounitbus/maximumchannelcount)
- [AUAudioUnitBusArray](/documentation/audiotoolbox/auaudiounitbusarray)

#### Initialization

- [convenience init(audioUnit: AUAudioUnit, busType: AUAudioUnitBusType)](/documentation/audiotoolbox/auaudiounitbusarray/init(audiounit:bustype:))
- [init(audioUnit: AUAudioUnit, busType: AUAudioUnitBusType, busses: [AUAudioUnitBus])](/documentation/audiotoolbox/auaudiounitbusarray/init(audiounit:bustype:busses:))

#### Bus Array Methods and Properties

- [var count: Int](/documentation/audiotoolbox/auaudiounitbusarray/count)
- [var isCountChangeable: Bool](/documentation/audiotoolbox/auaudiounitbusarray/iscountchangeable)
- [var ownerAudioUnit: AUAudioUnit](/documentation/audiotoolbox/auaudiounitbusarray/owneraudiounit)
- [var busType: AUAudioUnitBusType](/documentation/audiotoolbox/auaudiounitbusarray/bustype)
- [subscript(Int) -> AUAudioUnitBus](/documentation/audiotoolbox/auaudiounitbusarray/subscript(_:))
- [func setBusCount(Int) throws](/documentation/audiotoolbox/auaudiounitbusarray/setbuscount(_:))
- [func addObserver(toAllBusses: NSObject, forKeyPath: String, options: NSKeyValueObservingOptions, context: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/auaudiounitbusarray/addobserver(toallbusses:forkeypath:options:context:))
- [func removeObserver(fromAllBusses: NSObject, forKeyPath: String, context: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/auaudiounitbusarray/removeobserver(fromallbusses:forkeypath:context:))

#### Audio Unit Implementations

- [func replaceBusses([AUAudioUnitBus])](/documentation/audiotoolbox/auaudiounitbusarray/replacebusses(_:))
- [AUAudioUnitPreset](/documentation/audiotoolbox/auaudiounitpreset)

#### Preset Properties

- [var name: String](/documentation/audiotoolbox/auaudiounitpreset/name)
- [var number: Int](/documentation/audiotoolbox/auaudiounitpreset/number)
- [AUAudioUnitV2Bridge](/documentation/audiotoolbox/auaudiounitv2bridge)

#### Instance Properties

- [var audioUnit: AudioUnit](/documentation/audiotoolbox/auaudiounitv2bridge/audiounit)
- [func AudioUnitExtensionCopyComponentList(CFString) -> Unmanaged<CFArray>?](/documentation/audiotoolbox/audiounitextensioncopycomponentlist(_:))
- [func AudioUnitExtensionSetComponentList(CFString, CFArray?) -> OSStatus](/documentation/audiotoolbox/audiounitextensionsetcomponentlist(_:_:))
- [AUAudioUnitFactory](/documentation/audiotoolbox/auaudiounitfactory)

#### Required Methods

- [func createAudioUnit(with: AudioComponentDescription) throws -> AUAudioUnit](/documentation/audiotoolbox/auaudiounitfactory/createaudiounit(with:))

### Parameters

- [AUParameter](/documentation/audiotoolbox/auparameter)

#### Querying Parameter Properties

- [var minValue: AUValue](/documentation/audiotoolbox/auparameter/minvalue)
- [var maxValue: AUValue](/documentation/audiotoolbox/auparameter/maxvalue)
- [var unit: AudioUnitParameterUnit](/documentation/audiotoolbox/auparameter/unit)
- [var unitName: String?](/documentation/audiotoolbox/auparameter/unitname)
- [var flags: AudioUnitParameterOptions](/documentation/audiotoolbox/auparameter/flags)
- [var address: AUParameterAddress](/documentation/audiotoolbox/auparameter/address)
- [var valueStrings: [String]?](/documentation/audiotoolbox/auparameter/valuestrings)
- [var dependentParameters: [NSNumber]?](/documentation/audiotoolbox/auparameter/dependentparameters)

#### Managing Parameter Values

- [var value: AUValue](/documentation/audiotoolbox/auparameter/value)
- [func setValue(AUValue, originator: AUParameterObserverToken?)](/documentation/audiotoolbox/auparameter/setvalue(_:originator:))
- [func setValue(AUValue, originator: AUParameterObserverToken?, atHostTime: UInt64)](/documentation/audiotoolbox/auparameter/setvalue(_:originator:athosttime:))
- [func setValue(AUValue, originator: AUParameterObserverToken?, atHostTime: UInt64, eventType: AUParameterAutomationEventType)](/documentation/audiotoolbox/auparameter/setvalue(_:originator:athosttime:eventtype:))
- [func string(fromValue: UnsafePointer<AUValue>?) -> String](/documentation/audiotoolbox/auparameter/string(fromvalue:))
- [func value(from: String) -> AUValue](/documentation/audiotoolbox/auparameter/value(from:))
- [AUParameterGroup](/documentation/audiotoolbox/auparametergroup)

#### Obtaining Group Parameters

- [var allParameters: [AUParameter]](/documentation/audiotoolbox/auparametergroup/allparameters)
- [var children: [AUParameterNode]](/documentation/audiotoolbox/auparametergroup/children)
- [AUParameterNode](/documentation/audiotoolbox/auparameternode)

#### Identifiers

- [var identifier: String](/documentation/audiotoolbox/auparameternode/identifier)
- [var keyPath: String](/documentation/audiotoolbox/auparameternode/keypath)
- [var displayName: String](/documentation/audiotoolbox/auparameternode/displayname)
- [func displayName(withLength: Int) -> String](/documentation/audiotoolbox/auparameternode/displayname(withlength:))

#### Observers

- [func token(byAddingParameterObserver: AUParameterObserver) -> AUParameterObserverToken](/documentation/audiotoolbox/auparameternode/token(byaddingparameterobserver:))
- [func token(byAddingParameterRecordingObserver: AUParameterRecordingObserver) -> AUParameterObserverToken](/documentation/audiotoolbox/auparameternode/token(byaddingparameterrecordingobserver:))
- [func token(byAddingParameterAutomationObserver: AUParameterAutomationObserver) -> AUParameterObserverToken](/documentation/audiotoolbox/auparameternode/token(byaddingparameterautomationobserver:))
- [func removeParameterObserver(AUParameterObserverToken)](/documentation/audiotoolbox/auparameternode/removeparameterobserver(_:))

#### Audio Unit Implementations

- [var implementorValueObserver: AUImplementorValueObserver](/documentation/audiotoolbox/auparameternode/implementorvalueobserver)
- [var implementorValueProvider: AUImplementorValueProvider](/documentation/audiotoolbox/auparameternode/implementorvalueprovider)
- [var implementorStringFromValueCallback: AUImplementorStringFromValueCallback](/documentation/audiotoolbox/auparameternode/implementorstringfromvaluecallback)
- [var implementorValueFromStringCallback: AUImplementorValueFromStringCallback](/documentation/audiotoolbox/auparameternode/implementorvaluefromstringcallback)
- [var implementorDisplayNameWithLengthCallback: AUImplementorDisplayNameWithLengthCallback](/documentation/audiotoolbox/auparameternode/implementordisplaynamewithlengthcallback)

#### Constants

- [AUParameterObserver](/documentation/audiotoolbox/auparameterobserver)
- [AUParameterRecordingObserver](/documentation/audiotoolbox/auparameterrecordingobserver)
- [AUImplementorValueObserver](/documentation/audiotoolbox/auimplementorvalueobserver)
- [AUImplementorValueProvider](/documentation/audiotoolbox/auimplementorvalueprovider)
- [AUImplementorStringFromValueCallback](/documentation/audiotoolbox/auimplementorstringfromvaluecallback)
- [AUImplementorValueFromStringCallback](/documentation/audiotoolbox/auimplementorvaluefromstringcallback)
- [AUImplementorDisplayNameWithLengthCallback](/documentation/audiotoolbox/auimplementordisplaynamewithlengthcallback)
- [AUParameterTree](/documentation/audiotoolbox/auparametertree)

#### Obtaining Tree Parameters

- [func parameter(withAddress: AUParameterAddress) -> AUParameter?](/documentation/audiotoolbox/auparametertree/parameter(withaddress:))
- [func parameter(withID: AudioUnitParameterID, scope: AudioUnitScope, element: AudioUnitElement) -> AUParameter?](/documentation/audiotoolbox/auparametertree/parameter(withid:scope:element:))

#### Audio Unit Implementations

- [class func createParameter(withIdentifier: String, name: String, address: AUParameterAddress, min: AUValue, max: AUValue, unit: AudioUnitParameterUnit, unitName: String?, flags: AudioUnitParameterOptions, valueStrings: [String]?, dependentParameters: [NSNumber]?) -> AUParameter](/documentation/audiotoolbox/auparametertree/createparameter(withidentifier:name:address:min:max:unit:unitname:flags:valuestrings:dependentparameters:))
- [class func createGroup(withIdentifier: String, name: String, children: [AUParameterNode]) -> AUParameterGroup](/documentation/audiotoolbox/auparametertree/creategroup(withidentifier:name:children:))
- [class func createGroupTemplate([AUParameterNode]) -> AUParameterGroup](/documentation/audiotoolbox/auparametertree/creategrouptemplate(_:))
- [class func createGroup(fromTemplate: AUParameterGroup, identifier: String, name: String, addressOffset: AUParameterAddress) -> AUParameterGroup](/documentation/audiotoolbox/auparametertree/creategroup(fromtemplate:identifier:name:addressoffset:))
- [class func createTree(withChildren: [AUParameterNode]) -> AUParameterTree](/documentation/audiotoolbox/auparametertree/createtree(withchildren:))
- [Audio Components](/documentation/audiotoolbox/audio-components)

### Creating an Audio Component Instance

- [func AudioComponentInstanceNew(AudioComponent, UnsafeMutablePointer<AudioComponentInstance?>) -> OSStatus](/documentation/audiotoolbox/audiocomponentinstancenew(_:_:))
- [func AudioComponentInstantiate(AudioComponent, AudioComponentInstantiationOptions, (AudioComponentInstance?, OSStatus) -> Void)](/documentation/audiotoolbox/audiocomponentinstantiate(_:_:_:))
- [func AudioComponentInstanceDispose(AudioComponentInstance) -> OSStatus](/documentation/audiotoolbox/audiocomponentinstancedispose(_:))
- [AudioComponent](/documentation/audiotoolbox/audiocomponent)
- [AudioComponentInstantiationOptions](/documentation/audiotoolbox/audiocomponentinstantiationoptions)

#### Constants

- [static var loadInProcess: AudioComponentInstantiationOptions](/documentation/audiotoolbox/audiocomponentinstantiationoptions/loadinprocess)
- [static var loadOutOfProcess: AudioComponentInstantiationOptions](/documentation/audiotoolbox/audiocomponentinstantiationoptions/loadoutofprocess)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiocomponentinstantiationoptions/init(rawvalue:))

#### Type Properties

- [static var loadedRemotely: AudioComponentInstantiationOptions](/documentation/audiotoolbox/audiocomponentinstantiationoptions/loadedremotely)
- [Audio Component Errors](/documentation/audiotoolbox/1619490-audio-component-errors)

#### Constants

- [var kAudioComponentErr_DuplicateDescription: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_duplicatedescription)
- [var kAudioComponentErr_InitializationTimedOut: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_initializationtimedout)
- [var kAudioComponentErr_InvalidFormat: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_invalidformat)
- [var kAudioComponentErr_NotPermitted: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_notpermitted)
- [var kAudioComponentErr_TooManyInstances: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_toomanyinstances)
- [var kAudioComponentErr_UnsupportedType: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_unsupportedtype)

### Creating an Audio Component Dynamically

- [func AudioComponentRegister(UnsafePointer<AudioComponentDescription>, CFString, UInt32, AudioComponentFactoryFunction) -> AudioComponent](/documentation/audiotoolbox/audiocomponentregister(_:_:_:_:))
- [func AudioComponentCount(UnsafePointer<AudioComponentDescription>) -> UInt32](/documentation/audiotoolbox/audiocomponentcount(_:))
- [func AudioComponentFindNext(AudioComponent?, UnsafePointer<AudioComponentDescription>) -> AudioComponent?](/documentation/audiotoolbox/audiocomponentfindnext(_:_:))
- [func AudioComponentInstanceGetComponent(AudioComponentInstance) -> AudioComponent](/documentation/audiotoolbox/audiocomponentinstancegetcomponent(_:))
- [AudioComponentDescription](/documentation/audiotoolbox/audiocomponentdescription)

#### Properties

- [var componentType: OSType](/documentation/audiotoolbox/audiocomponentdescription/componenttype)
- [var componentSubType: OSType](/documentation/audiotoolbox/audiocomponentdescription/componentsubtype)
- [var componentManufacturer: OSType](/documentation/audiotoolbox/audiocomponentdescription/componentmanufacturer)
- [var componentFlags: UInt32](/documentation/audiotoolbox/audiocomponentdescription/componentflags)
- [var componentFlagsMask: UInt32](/documentation/audiotoolbox/audiocomponentdescription/componentflagsmask)

#### Initializers

- [init()](/documentation/audiotoolbox/audiocomponentdescription/init())
- [init(componentType: OSType, componentSubType: OSType, componentManufacturer: OSType, componentFlags: UInt32, componentFlagsMask: UInt32)](/documentation/audiotoolbox/audiocomponentdescription/init(componenttype:componentsubtype:componentmanufacturer:componentflags:componentflagsmask:))
- [AudioComponentInstance](/documentation/audiotoolbox/audiocomponentinstance)
- [AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags)

#### Flags

- [static var unsearchable: AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags/unsearchable)
- [static var sandboxSafe: AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags/sandboxsafe)
- [static var isV3AudioUnit: AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags/isv3audiounit)
- [static var requiresAsyncInstantiation: AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags/requiresasyncinstantiation)
- [static var canLoadInProcess: AudioComponentFlags](/documentation/audiotoolbox/audiocomponentflags/canloadinprocess)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiocomponentflags/init(rawvalue:))
- [AudioComponentFactoryFunction](/documentation/audiotoolbox/audiocomponentfactoryfunction)

### Getting Information About a Component

- [func AudioComponentInstanceCanDo(AudioComponentInstance, Int16) -> Bool](/documentation/audiotoolbox/audiocomponentinstancecando(_:_:))
- [func AudioComponentGetDescription(AudioComponent, UnsafeMutablePointer<AudioComponentDescription>) -> OSStatus](/documentation/audiotoolbox/audiocomponentgetdescription(_:_:))
- [func AudioComponentCopyName(AudioComponent, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/audiotoolbox/audiocomponentcopyname(_:_:))
- [func AudioComponentGetVersion(AudioComponent, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiocomponentgetversion(_:_:))
- [func AudioComponentCopyIcon(AudioComponent) -> UIImage?](/documentation/audiotoolbox/audiocomponentcopyicon(_:))
- [func AudioComponentCopyConfigurationInfo(AudioComponent, UnsafeMutablePointer<Unmanaged<CFDictionary>?>) -> OSStatus](/documentation/audiotoolbox/audiocomponentcopyconfigurationinfo(_:_:))
- [AudioComponentPlugInInterface](/documentation/audiotoolbox/audiocomponentplugininterface)

#### Initializers

- [init(Open: (UnsafeMutableRawPointer, AudioComponentInstance) -> OSStatus, Close: (UnsafeMutableRawPointer) -> OSStatus, Lookup: (Int16) -> AudioComponentMethod?, reserved: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/audiocomponentplugininterface/init(open:close:lookup:reserved:)-1bmzd)
- [init(Open: (UnsafeMutableRawPointer, AudioComponentInstance) -> OSStatus, Close: (UnsafeMutableRawPointer) -> OSStatus, Lookup: (Int16) -> AudioComponentMethod?, reserved: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/audiocomponentplugininterface/init(open:close:lookup:reserved:)-1hqa3)

#### Instance Properties

- [var Close: (UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiocomponentplugininterface/close)
- [var Lookup: (Int16) -> AudioComponentMethod?](/documentation/audiotoolbox/audiocomponentplugininterface/lookup)
- [var Open: (UnsafeMutableRawPointer, AudioComponentInstance) -> OSStatus](/documentation/audiotoolbox/audiocomponentplugininterface/open)
- [var reserved: UnsafeMutableRawPointer?](/documentation/audiotoolbox/audiocomponentplugininterface/reserved)
- [AudioComponentMethod](/documentation/audiotoolbox/audiocomponentmethod)

### Validating an Audio Component

- [func AudioComponentValidate(AudioComponent, CFDictionary?, UnsafeMutablePointer<AudioComponentValidationResult>) -> OSStatus](/documentation/audiotoolbox/audiocomponentvalidate(_:_:_:))
- [var kAudioComponentValidationParameter_LoadOutOfProcess: String](/documentation/audiotoolbox/kaudiocomponentvalidationparameter_loadoutofprocess)
- [AudioComponentValidationResult](/documentation/audiotoolbox/audiocomponentvalidationresult)

#### Constants

- [case failed](/documentation/audiotoolbox/audiocomponentvalidationresult/failed)
- [case passed](/documentation/audiotoolbox/audiocomponentvalidationresult/passed)
- [case timedOut](/documentation/audiotoolbox/audiocomponentvalidationresult/timedout)
- [case unauthorizedError_Init](/documentation/audiotoolbox/audiocomponentvalidationresult/unauthorizederror_init)
- [case unauthorizedError_Open](/documentation/audiotoolbox/audiocomponentvalidationresult/unauthorizederror_open)
- [case unknown](/documentation/audiotoolbox/audiocomponentvalidationresult/unknown)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiocomponentvalidationresult/init(rawvalue:))

### Constants

- [var kAudioComponentConfigurationInfo_ValidationResult: String](/documentation/audiotoolbox/kaudiocomponentconfigurationinfo_validationresult)
- [let kAudioComponentInstanceInvalidationNotification: CFString](/documentation/audiotoolbox/kaudiocomponentinstanceinvalidationnotification)
- [let kAudioComponentRegistrationsChangedNotification: CFString](/documentation/audiotoolbox/kaudiocomponentregistrationschangednotification)
- [var kAudioComponentValidationParameter_ForceValidation: String](/documentation/audiotoolbox/kaudiocomponentvalidationparameter_forcevalidation)
- [var kAudioComponentValidationParameter_TimeOut: String](/documentation/audiotoolbox/kaudiocomponentvalidationparameter_timeout)
- [Audio Unit v2 (C) API](/documentation/audiotoolbox/audio-unit-v2-c-api)

### Initializing the Audio Unit

- [func AudioUnitInitialize(AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiounitinitialize(_:))
- [func AudioUnitUninitialize(AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiounituninitialize(_:))
- [func AudioUnitProcess(AudioUnit, UnsafeMutablePointer<AudioUnitRenderActionFlags>?, UnsafePointer<AudioTimeStamp>, UInt32, UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/audiounitprocess(_:_:_:_:_:))
- [func AudioUnitProcessMultiple(AudioUnit, UnsafeMutablePointer<AudioUnitRenderActionFlags>?, UnsafePointer<AudioTimeStamp>, UInt32, UInt32, UnsafeMutablePointer<UnsafePointer<AudioBufferList>>, UInt32, UnsafeMutablePointer<UnsafeMutablePointer<AudioBufferList>>) -> OSStatus](/documentation/audiotoolbox/audiounitprocessmultiple(_:_:_:_:_:_:_:_:))
- [func AudioUnitReset(AudioUnit, AudioUnitScope, AudioUnitElement) -> OSStatus](/documentation/audiotoolbox/audiounitreset(_:_:_:))
- [AudioUnit](/documentation/audiotoolbox/audiounit)

### Starting and Stopping Output

- [func AudioOutputUnitStart(AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiooutputunitstart(_:))
- [func AudioOutputUnitStop(AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiooutputunitstop(_:))
- [AudioOutputUnitStartProc](/documentation/audiotoolbox/audiooutputunitstartproc)
- [AudioOutputUnitStopProc](/documentation/audiotoolbox/audiooutputunitstopproc)

### Rendering the Audio

- [func AudioUnitRender(AudioUnit, UnsafeMutablePointer<AudioUnitRenderActionFlags>?, UnsafePointer<AudioTimeStamp>, UInt32, UInt32, UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/audiounitrender(_:_:_:_:_:_:))
- [func AudioUnitAddRenderNotify(AudioUnit, AURenderCallback, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiounitaddrendernotify(_:_:_:))
- [func AudioUnitRemoveRenderNotify(AudioUnit, AURenderCallback, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiounitremoverendernotify(_:_:_:))
- [AURenderCallback](/documentation/audiotoolbox/aurendercallback)
- [AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags)

#### Constants

- [static var unitRenderAction_PreRender: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_prerender)
- [static var unitRenderAction_PostRender: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_postrender)
- [static var unitRenderAction_OutputIsSilence: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_outputissilence)
- [static var offlineUnitRenderAction_Preflight: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_preflight)
- [static var offlineUnitRenderAction_Render: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_render)
- [static var offlineUnitRenderAction_Complete: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_complete)
- [static var unitRenderAction_PostRenderError: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_postrendererror)
- [static var unitRenderAction_DoNotCheckRenderArgs: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_donotcheckrenderargs)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiounitrenderactionflags/init(rawvalue:))

### Configuring Audio Unit Properties

- [func AudioUnitGetProperty(AudioUnit, AudioUnitPropertyID, AudioUnitScope, AudioUnitElement, UnsafeMutableRawPointer, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiounitgetproperty(_:_:_:_:_:_:))
- [func AudioUnitSetProperty(AudioUnit, AudioUnitPropertyID, AudioUnitScope, AudioUnitElement, UnsafeRawPointer?, UInt32) -> OSStatus](/documentation/audiotoolbox/audiounitsetproperty(_:_:_:_:_:_:))
- [func AudioUnitGetPropertyInfo(AudioUnit, AudioUnitPropertyID, AudioUnitScope, AudioUnitElement, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audiounitgetpropertyinfo(_:_:_:_:_:_:))
- [func AudioUnitAddPropertyListener(AudioUnit, AudioUnitPropertyID, AudioUnitPropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiounitaddpropertylistener(_:_:_:_:))
- [func AudioUnitRemovePropertyListenerWithUserData(AudioUnit, AudioUnitPropertyID, AudioUnitPropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiounitremovepropertylistenerwithuserdata(_:_:_:_:))

### Responding to Events

- [func AUEventListenerCreateWithDispatchQueue(UnsafeMutablePointer<AUEventListenerRef?>, Float32, Float32, dispatch_queue_t, AUEventListenerBlock) -> OSStatus](/documentation/audiotoolbox/aueventlistenercreatewithdispatchqueue(_:_:_:_:_:))
- [func AUEventListenerCreate(AUEventListenerProc, UnsafeMutableRawPointer?, CFRunLoop?, CFString?, Float32, Float32, UnsafeMutablePointer<AUEventListenerRef?>) -> OSStatus](/documentation/audiotoolbox/aueventlistenercreate(_:_:_:_:_:_:_:))
- [func AUListenerDispose(AUParameterListenerRef) -> OSStatus](/documentation/audiotoolbox/aulistenerdispose(_:))
- [func AUEventListenerNotify(AUEventListenerRef?, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitEvent>) -> OSStatus](/documentation/audiotoolbox/aueventlistenernotify(_:_:_:))
- [func AUEventListenerAddEventType(AUEventListenerRef, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitEvent>) -> OSStatus](/documentation/audiotoolbox/aueventlisteneraddeventtype(_:_:_:))
- [func AUEventListenerRemoveEventType(AUEventListenerRef, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitEvent>) -> OSStatus](/documentation/audiotoolbox/aueventlistenerremoveeventtype(_:_:_:))
- [func AUListenerAddParameter(AUParameterListenerRef, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitParameter>) -> OSStatus](/documentation/audiotoolbox/aulisteneraddparameter(_:_:_:))
- [func AUListenerRemoveParameter(AUParameterListenerRef, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitParameter>) -> OSStatus](/documentation/audiotoolbox/aulistenerremoveparameter(_:_:_:))
- [AUEventListenerBlock](/documentation/audiotoolbox/aueventlistenerblock)

### Getting and Setting Parameters

- [func AudioUnitGetParameter(AudioUnit, AudioUnitParameterID, AudioUnitScope, AudioUnitElement, UnsafeMutablePointer<AudioUnitParameterValue>) -> OSStatus](/documentation/audiotoolbox/audiounitgetparameter(_:_:_:_:_:))
- [func AudioUnitScheduleParameters(AudioUnit, UnsafePointer<AudioUnitParameterEvent>, UInt32) -> OSStatus](/documentation/audiotoolbox/audiounitscheduleparameters(_:_:_:))
- [func AudioUnitSetParameter(AudioUnit, AudioUnitParameterID, AudioUnitScope, AudioUnitElement, AudioUnitParameterValue, UInt32) -> OSStatus](/documentation/audiotoolbox/audiounitsetparameter(_:_:_:_:_:_:))

### Monitoring Parameter Changes

- [func AUListenerCreateWithDispatchQueue(UnsafeMutablePointer<AUParameterListenerRef?>, Float32, dispatch_queue_t, AUParameterListenerBlock) -> OSStatus](/documentation/audiotoolbox/aulistenercreatewithdispatchqueue(_:_:_:_:))
- [func AUListenerCreate(AUParameterListenerProc, UnsafeMutableRawPointer, CFRunLoop?, CFString?, Float32, UnsafeMutablePointer<AUParameterListenerRef?>) -> OSStatus](/documentation/audiotoolbox/aulistenercreate(_:_:_:_:_:_:))
- [func AUParameterListenerNotify(AUParameterListenerRef?, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitParameter>) -> OSStatus](/documentation/audiotoolbox/auparameterlistenernotify(_:_:_:))
- [func AUParameterFormatValue(Float64, UnsafePointer<AudioUnitParameter>, UnsafeMutablePointer<CChar>, UInt32) -> UnsafeMutablePointer<CChar>](/documentation/audiotoolbox/auparameterformatvalue(_:_:_:_:))
- [func AUParameterSet(AUParameterListenerRef?, UnsafeMutableRawPointer?, UnsafePointer<AudioUnitParameter>, AudioUnitParameterValue, UInt32) -> OSStatus](/documentation/audiotoolbox/auparameterset(_:_:_:_:_:))
- [func AUParameterValueFromLinear(Float32, UnsafePointer<AudioUnitParameter>) -> AudioUnitParameterValue](/documentation/audiotoolbox/auparametervaluefromlinear(_:_:))
- [func AUParameterValueToLinear(AudioUnitParameterValue, UnsafePointer<AudioUnitParameter>) -> Float32](/documentation/audiotoolbox/auparametervaluetolinear(_:_:))
- [AUParameterListenerBlock](/documentation/audiotoolbox/auparameterlistenerblock)
- [AUParameterListenerProc](/documentation/audiotoolbox/auparameterlistenerproc)
- [AUParameterListenerRef](/documentation/audiotoolbox/auparameterlistenerref)
- [AUImplementorDisplayNameWithLengthCallback](/documentation/audiotoolbox/auimplementordisplaynamewithlengthcallback)
- [AUImplementorStringFromValueCallback](/documentation/audiotoolbox/auimplementorstringfromvaluecallback)
- [AUImplementorValueFromStringCallback](/documentation/audiotoolbox/auimplementorvaluefromstringcallback)

### Getting Information from the Host

- [HostCallback_GetBeatAndTempo](/documentation/audiotoolbox/hostcallback_getbeatandtempo)
- [HostCallback_GetMusicalTimeLocation](/documentation/audiotoolbox/hostcallback_getmusicaltimelocation)
- [HostCallback_GetTransportState](/documentation/audiotoolbox/hostcallback_gettransportstate)
- [HostCallback_GetTransportState2](/documentation/audiotoolbox/hostcallback_gettransportstate2)
- [AUInputSamplesInOutputCallback](/documentation/audiotoolbox/auinputsamplesinoutputcallback)
- [AUMIDIOutputCallback](/documentation/audiotoolbox/aumidioutputcallback)

### Getting the Configuration Information

- [var kAudioUnitConfigurationInfo_BusCountWritable: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_buscountwritable)
- [var kAudioUnitConfigurationInfo_ChannelConfigurations: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_channelconfigurations)
- [var kAudioUnitConfigurationInfo_HasCustomView: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_hascustomview)
- [var kAudioUnitConfigurationInfo_IconURL: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_iconurl)
- [var kAudioUnitConfigurationInfo_InitialInputs: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_initialinputs)
- [var kAudioUnitConfigurationInfo_InitialOutputs: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_initialoutputs)
- [var kAudioUnitConfigurationInfo_SupportedChannelLayoutTags: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_supportedchannellayouttags)

### Configuring the Audio Unit UI

- [AudioUnitCocoaViewInfo](/documentation/audiotoolbox/audiounitcocoaviewinfo)

#### Initializers

- [init(mCocoaAUViewBundleLocation: Unmanaged<CFURL>, mCocoaAUViewClass: Unmanaged<CFString>)](/documentation/audiotoolbox/audiounitcocoaviewinfo/init(mcocoaauviewbundlelocation:mcocoaauviewclass:))

#### Instance Properties

- [var mCocoaAUViewBundleLocation: Unmanaged<CFURL>](/documentation/audiotoolbox/audiounitcocoaviewinfo/mcocoaauviewbundlelocation)
- [var mCocoaAUViewClass: Unmanaged<CFString>](/documentation/audiotoolbox/audiounitcocoaviewinfo/mcocoaauviewclass)
- [func GetAudioUnitParameterDisplayType(AudioUnitParameterOptions) -> AudioUnitParameterOptions](/documentation/audiotoolbox/getaudiounitparameterdisplaytype(_:))
- [func SetAudioUnitParameterDisplayType(AudioUnitParameterOptions, AudioUnitParameterOptions) -> AudioUnitParameterOptions](/documentation/audiotoolbox/setaudiounitparameterdisplaytype(_:_:))

### Audio Unit Types

- [ScheduledAudioFileRegion](/documentation/audiotoolbox/scheduledaudiofileregion)

#### Initializers

- [init(mTimeStamp: AudioTimeStamp, mCompletionProc: ScheduledAudioFileRegionCompletionProc?, mCompletionProcUserData: UnsafeMutableRawPointer?, mAudioFile: OpaquePointer, mLoopCount: UInt32, mStartFrame: Int64, mFramesToPlay: UInt32)](/documentation/audiotoolbox/scheduledaudiofileregion/init(mtimestamp:mcompletionproc:mcompletionprocuserdata:maudiofile:mloopcount:mstartframe:mframestoplay:))

#### Instance Properties

- [var mAudioFile: OpaquePointer](/documentation/audiotoolbox/scheduledaudiofileregion/maudiofile)
- [var mCompletionProc: ScheduledAudioFileRegionCompletionProc?](/documentation/audiotoolbox/scheduledaudiofileregion/mcompletionproc)
- [var mCompletionProcUserData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/scheduledaudiofileregion/mcompletionprocuserdata)
- [var mFramesToPlay: UInt32](/documentation/audiotoolbox/scheduledaudiofileregion/mframestoplay)
- [var mLoopCount: UInt32](/documentation/audiotoolbox/scheduledaudiofileregion/mloopcount)
- [var mStartFrame: Int64](/documentation/audiotoolbox/scheduledaudiofileregion/mstartframe)
- [var mTimeStamp: AudioTimeStamp](/documentation/audiotoolbox/scheduledaudiofileregion/mtimestamp)
- [ScheduledAudioSlice](/documentation/audiotoolbox/scheduledaudioslice)

#### Initializers

- [init(mTimeStamp: AudioTimeStamp, mCompletionProc: ScheduledAudioSliceCompletionProc?, mCompletionProcUserData: UnsafeMutableRawPointer, mFlags: AUScheduledAudioSliceFlags, mReserved: UInt32, mReserved2: UnsafeMutableRawPointer?, mNumberFrames: UInt32, mBufferList: UnsafeMutablePointer<AudioBufferList>)](/documentation/audiotoolbox/scheduledaudioslice/init(mtimestamp:mcompletionproc:mcompletionprocuserdata:mflags:mreserved:mreserved2:mnumberframes:mbufferlist:))

#### Instance Properties

- [var mBufferList: UnsafeMutablePointer<AudioBufferList>](/documentation/audiotoolbox/scheduledaudioslice/mbufferlist)
- [var mCompletionProc: ScheduledAudioSliceCompletionProc?](/documentation/audiotoolbox/scheduledaudioslice/mcompletionproc)
- [var mCompletionProcUserData: UnsafeMutableRawPointer](/documentation/audiotoolbox/scheduledaudioslice/mcompletionprocuserdata)
- [var mFlags: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/scheduledaudioslice/mflags)
- [var mNumberFrames: UInt32](/documentation/audiotoolbox/scheduledaudioslice/mnumberframes)
- [var mReserved: UInt32](/documentation/audiotoolbox/scheduledaudioslice/mreserved)
- [var mReserved2: UnsafeMutableRawPointer?](/documentation/audiotoolbox/scheduledaudioslice/mreserved2)
- [var mTimeStamp: AudioTimeStamp](/documentation/audiotoolbox/scheduledaudioslice/mtimestamp)
- [ScheduledAudioFileRegionCompletionProc](/documentation/audiotoolbox/scheduledaudiofileregioncompletionproc)
- [ScheduledAudioSliceCompletionProc](/documentation/audiotoolbox/scheduledaudioslicecompletionproc)
- [MIDIChannelNumber](/documentation/audiotoolbox/midichannelnumber)
- [AUAudioObjectID](/documentation/audiotoolbox/auaudioobjectid)
- [AUMIDICIProfileChangedBlock](/documentation/audiotoolbox/aumidiciprofilechangedblock)
- [AUAudioChannelCount](/documentation/audiotoolbox/auaudiochannelcount)
- [AUAudioFrameCount](/documentation/audiotoolbox/auaudioframecount)
- [AUAudioUnitStatus](/documentation/audiotoolbox/auaudiounitstatus)
- [AUEventListenerProc](/documentation/audiotoolbox/aueventlistenerproc)
- [AUEventListenerRef](/documentation/audiotoolbox/aueventlistenerref)
- [AUEventSampleTime](/documentation/audiotoolbox/aueventsampletime)
- [AUImplementorValueObserver](/documentation/audiotoolbox/auimplementorvalueobserver)
- [AUImplementorValueProvider](/documentation/audiotoolbox/auimplementorvalueprovider)
- [AUInputHandler](/documentation/audiotoolbox/auinputhandler)
- [AUNodeConnection](/documentation/audiotoolbox/aunodeconnection)
- [AUParameterAddress](/documentation/audiotoolbox/auparameteraddress)
- [AUParameterAutomationObserver](/documentation/audiotoolbox/auparameterautomationobserver)
- [AUParameterObserver](/documentation/audiotoolbox/auparameterobserver)
- [AUParameterObserverToken](/documentation/audiotoolbox/auparameterobservertoken)
- [AUParameterRecordingObserver](/documentation/audiotoolbox/auparameterrecordingobserver)
- [AURenderBlock](/documentation/audiotoolbox/aurenderblock)
- [AURenderObserver](/documentation/audiotoolbox/aurenderobserver)
- [AURenderPullInputBlock](/documentation/audiotoolbox/aurenderpullinputblock)
- [AUScheduleParameterBlock](/documentation/audiotoolbox/auscheduleparameterblock)
- [AUValue](/documentation/audiotoolbox/auvalue)
- [AudioUnitAddPropertyListenerProc](/documentation/audiotoolbox/audiounitaddpropertylistenerproc)
- [AudioUnitAddRenderNotifyProc](/documentation/audiotoolbox/audiounitaddrendernotifyproc)
- [AudioUnitComplexRenderProc](/documentation/audiotoolbox/audiounitcomplexrenderproc)
- [AudioUnitElement](/documentation/audiotoolbox/audiounitelement)
- [AudioUnitGetParameterProc](/documentation/audiotoolbox/audiounitgetparameterproc)
- [AudioUnitGetPropertyInfoProc](/documentation/audiotoolbox/audiounitgetpropertyinfoproc)
- [AudioUnitGetPropertyProc](/documentation/audiotoolbox/audiounitgetpropertyproc)
- [AudioUnitInitializeProc](/documentation/audiotoolbox/audiounitinitializeproc)
- [AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameterid)
- [AudioUnitParameterNameInfo](/documentation/audiotoolbox/audiounitparameternameinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparameternameinfo/init())
- [init(inID: AudioUnitParameterID, inDesiredLength: Int32, outName: Unmanaged<CFString>?)](/documentation/audiotoolbox/audiounitparameternameinfo/init(inid:indesiredlength:outname:))

#### Instance Properties

- [var inDesiredLength: Int32](/documentation/audiotoolbox/audiounitparameternameinfo/indesiredlength)
- [var inID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameternameinfo/inid)
- [var outName: Unmanaged<CFString>?](/documentation/audiotoolbox/audiounitparameternameinfo/outname)
- [AudioUnitParameterIDName](/documentation/audiotoolbox/audiounitparameteridname)
- [AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparametervalue)
- [AudioUnitProcessMultipleProc](/documentation/audiotoolbox/audiounitprocessmultipleproc)
- [AudioUnitProcessProc](/documentation/audiotoolbox/audiounitprocessproc)
- [AudioUnitPropertyID](/documentation/audiotoolbox/audiounitpropertyid)
- [AudioUnitPropertyListenerProc](/documentation/audiotoolbox/audiounitpropertylistenerproc)
- [AudioUnitRemoteControlEventListener](/documentation/audiotoolbox/audiounitremotecontroleventlistener)
- [AudioUnitRemovePropertyListenerProc](/documentation/audiotoolbox/audiounitremovepropertylistenerproc)
- [AudioUnitRemovePropertyListenerWithUserDataProc](/documentation/audiotoolbox/audiounitremovepropertylistenerwithuserdataproc)
- [AudioUnitRemoveRenderNotifyProc](/documentation/audiotoolbox/audiounitremoverendernotifyproc)
- [AudioUnitRenderProc](/documentation/audiotoolbox/audiounitrenderproc)
- [AudioUnitResetProc](/documentation/audiotoolbox/audiounitresetproc)
- [AudioUnitScheduleParametersProc](/documentation/audiotoolbox/audiounitscheduleparametersproc)
- [AudioUnitScope](/documentation/audiotoolbox/audiounitscope)
- [AudioUnitSetParameterProc](/documentation/audiotoolbox/audiounitsetparameterproc)
- [AudioUnitSetPropertyProc](/documentation/audiotoolbox/audiounitsetpropertyproc)
- [AudioUnitUninitializeProc](/documentation/audiotoolbox/audiounituninitializeproc)

### Enumerations

- [Audio Unit Types](/documentation/audiotoolbox/1584142-audio_unit_types)

#### Types

- [var kAudioUnitType_Output: UInt32](/documentation/audiotoolbox/kaudiounittype_output)
- [var kAudioUnitType_MusicDevice: UInt32](/documentation/audiotoolbox/kaudiounittype_musicdevice)
- [var kAudioUnitType_MusicEffect: UInt32](/documentation/audiotoolbox/kaudiounittype_musiceffect)
- [var kAudioUnitType_FormatConverter: UInt32](/documentation/audiotoolbox/kaudiounittype_formatconverter)
- [var kAudioUnitType_Effect: UInt32](/documentation/audiotoolbox/kaudiounittype_effect)
- [var kAudioUnitType_Mixer: UInt32](/documentation/audiotoolbox/kaudiounittype_mixer)
- [var kAudioUnitType_Panner: UInt32](/documentation/audiotoolbox/kaudiounittype_panner)
- [var kAudioUnitType_OfflineEffect: UInt32](/documentation/audiotoolbox/kaudiounittype_offlineeffect)
- [var kAudioUnitType_Generator: UInt32](/documentation/audiotoolbox/kaudiounittype_generator)
- [var kAudioUnitType_MIDIProcessor: UInt32](/documentation/audiotoolbox/kaudiounittype_midiprocessor)
- [var kAudioUnitType_SpeechSynthesizer: UInt32](/documentation/audiotoolbox/kaudiounittype_speechsynthesizer)
- [Inter-App Audio Unit Types](/documentation/audiotoolbox/1619501-inter-app-audio-unit-types)

#### Constants

- [var kAudioUnitType_RemoteEffect: UInt32](/documentation/audiotoolbox/kaudiounittype_remoteeffect)
- [var kAudioUnitType_RemoteGenerator: UInt32](/documentation/audiotoolbox/kaudiounittype_remotegenerator)
- [var kAudioUnitType_RemoteInstrument: UInt32](/documentation/audiotoolbox/kaudiounittype_remoteinstrument)
- [var kAudioUnitType_RemoteMusicEffect: UInt32](/documentation/audiotoolbox/kaudiounittype_remotemusiceffect)
- [Audio Unit Manufacturer Identifier](/documentation/audiotoolbox/1584143-audio_unit_manufacturer_identifi)

#### Constants

- [var kAudioUnitManufacturer_Apple: UInt32](/documentation/audiotoolbox/kaudiounitmanufacturer_apple)
- [Audio Unit Output Subtypes](/documentation/audiotoolbox/1584148-audio-unit-output-subtypes)

#### Constants

- [var kAudioUnitSubType_DefaultOutput: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_defaultoutput)
- [var kAudioUnitSubType_HALOutput: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_haloutput)
- [var kAudioUnitSubType_SystemOutput: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_systemoutput)
- [I/O Audio Unit Subtypes](/documentation/audiotoolbox/1619485-i-o-audio-unit-subtypes)

#### Constants

- [var kAudioUnitSubType_RemoteIO: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_remoteio)
- [Converter Audio Unit Subtypes](/documentation/audiotoolbox/1584145-converter_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_AUConverter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auconverter)
- [var kAudioUnitSubType_AUiPodTimeOther: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auipodtimeother)
- [var kAudioUnitSubType_DeferredRenderer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_deferredrenderer)
- [var kAudioUnitSubType_Merger: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_merger)
- [var kAudioUnitSubType_MultiSplitter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_multisplitter)
- [var kAudioUnitSubType_NewTimePitch: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_newtimepitch)
- [var kAudioUnitSubType_RoundTripAAC: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_roundtripaac)
- [var kAudioUnitSubType_Splitter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_splitter)
- [var kAudioUnitSubType_Varispeed: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_varispeed)
- [Reserved Audio Unit Clump Identifier](/documentation/audiotoolbox/1533986-reserved_audio_unit_clump_identi)

#### Constants

- [var kAudioUnitClumpID_System: Int](/documentation/audiotoolbox/kaudiounitclumpid_system)
- [Offline Audio Unit Properties](/documentation/audiotoolbox/1534054-offline_audio_unit_properties)

#### Constants

- [var kAudioUnitOfflineProperty_InputSize: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitofflineproperty_inputsize)
- [var kAudioUnitOfflineProperty_OutputSize: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitofflineproperty_outputsize)
- [var kAudioUnitOfflineProperty_PreflightName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitofflineproperty_preflightname)
- [var kAudioUnitOfflineProperty_PreflightRequirements: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitofflineproperty_preflightrequirements)
- [var kAudioUnitOfflineProperty_StartOffset: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitofflineproperty_startoffset)
- [MIDI Audio Unit Parameters](/documentation/audiotoolbox/1389613-midi_audio_unit_parameters)

#### Constants

- [var kAUGroupParameterID_AllNotesOff: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_allnotesoff)
- [var kAUGroupParameterID_AllSoundOff: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_allsoundoff)
- [var kAUGroupParameterID_ChannelPressure: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_channelpressure)
- [var kAUGroupParameterID_DataEntry: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_dataentry)
- [var kAUGroupParameterID_DataEntry_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_dataentry_lsb)
- [var kAUGroupParameterID_Expression: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_expression)
- [var kAUGroupParameterID_Expression_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_expression_lsb)
- [var kAUGroupParameterID_Foot: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_foot)
- [var kAUGroupParameterID_Foot_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_foot_lsb)
- [var kAUGroupParameterID_KeyPressure: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_keypressure)
- [var kAUGroupParameterID_KeyPressure_FirstKey: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_keypressure_firstkey)
- [var kAUGroupParameterID_KeyPressure_LastKey: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_keypressure_lastkey)
- [var kAUGroupParameterID_ModWheel: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_modwheel)
- [var kAUGroupParameterID_ModWheel_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_modwheel_lsb)
- [var kAUGroupParameterID_Pan: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_pan)
- [var kAUGroupParameterID_Pan_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_pan_lsb)
- [var kAUGroupParameterID_PitchBend: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_pitchbend)
- [var kAUGroupParameterID_ResetAllControllers: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_resetallcontrollers)
- [var kAUGroupParameterID_Sostenuto: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_sostenuto)
- [var kAUGroupParameterID_Sustain: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_sustain)
- [var kAUGroupParameterID_Volume: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_volume)
- [var kAUGroupParameterID_Volume_LSB: AudioUnitParameterID](/documentation/audiotoolbox/kaugroupparameterid_volume_lsb)
- [General Audio Unit Function Selectors](/documentation/audiotoolbox/1584140-general_audio_unit_function_sele)

#### Constants

- [var kAudioUnitAddPropertyListenerSelect: Int](/documentation/audiotoolbox/kaudiounitaddpropertylistenerselect)
- [var kAudioUnitAddRenderNotifySelect: Int](/documentation/audiotoolbox/kaudiounitaddrendernotifyselect)
- [var kAudioUnitComplexRenderSelect: Int](/documentation/audiotoolbox/kaudiounitcomplexrenderselect)
- [var kAudioUnitGetParameterSelect: Int](/documentation/audiotoolbox/kaudiounitgetparameterselect)
- [var kAudioUnitGetPropertyInfoSelect: Int](/documentation/audiotoolbox/kaudiounitgetpropertyinfoselect)
- [var kAudioUnitGetPropertySelect: Int](/documentation/audiotoolbox/kaudiounitgetpropertyselect)
- [var kAudioUnitInitializeSelect: Int](/documentation/audiotoolbox/kaudiounitinitializeselect)
- [var kAudioUnitProcessMultipleSelect: Int](/documentation/audiotoolbox/kaudiounitprocessmultipleselect)
- [var kAudioUnitProcessSelect: Int](/documentation/audiotoolbox/kaudiounitprocessselect)
- [var kAudioUnitRange: Int](/documentation/audiotoolbox/kaudiounitrange)
- [var kAudioUnitRemovePropertyListenerSelect: Int](/documentation/audiotoolbox/kaudiounitremovepropertylistenerselect)
- [var kAudioUnitRemovePropertyListenerWithUserDataSelect: Int](/documentation/audiotoolbox/kaudiounitremovepropertylistenerwithuserdataselect)
- [var kAudioUnitRemoveRenderNotifySelect: Int](/documentation/audiotoolbox/kaudiounitremoverendernotifyselect)
- [var kAudioUnitRenderSelect: Int](/documentation/audiotoolbox/kaudiounitrenderselect)
- [var kAudioUnitResetSelect: Int](/documentation/audiotoolbox/kaudiounitresetselect)
- [var kAudioUnitScheduleParametersSelect: Int](/documentation/audiotoolbox/kaudiounitscheduleparametersselect)
- [var kAudioUnitSetParameterSelect: Int](/documentation/audiotoolbox/kaudiounitsetparameterselect)
- [var kAudioUnitSetPropertySelect: Int](/documentation/audiotoolbox/kaudiounitsetpropertyselect)
- [var kAudioUnitUninitializeSelect: Int](/documentation/audiotoolbox/kaudiounituninitializeselect)
- [Generator Audio Unit Subtypes](/documentation/audiotoolbox/1619493-generator_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_AudioFilePlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_audiofileplayer-6zi0a)
- [var kAudioUnitSubType_ScheduledSoundPlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_scheduledsoundplayer-55u1s)
- [Input/Output Audio Unit Subtypes](/documentation/audiotoolbox/1584139-input_output_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_GenericOutput: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_genericoutput)
- [var kAudioUnitSubType_VoiceProcessingIO: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_voiceprocessingio)
- [Audio Unit Panner Subtypes](/documentation/audiotoolbox/1584151-audio-unit-panner-subtypes)

#### Constants

- [var kAudioUnitSubType_HRTFPanner: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_hrtfpanner)
- [var kAudioUnitSubType_SoundFieldPanner: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_soundfieldpanner)
- [var kAudioUnitSubType_SphericalHeadPanner: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_sphericalheadpanner)
- [var kAudioUnitSubType_VectorPanner: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_vectorpanner)
- [Audio Unit Player Subtypes](/documentation/audiotoolbox/1584155-audio-unit-player-subtypes)

#### Constants

- [var kAudioUnitSubType_AudioFilePlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_audiofileplayer-2ewv0)
- [var kAudioUnitSubType_AudioFilePlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_audiofileplayer-6zi0a)
- [var kAudioUnitSubType_NetReceive: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_netreceive)
- [var kAudioUnitSubType_ScheduledSoundPlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_scheduledsoundplayer-55u1s)
- [var kAudioUnitSubType_ScheduledSoundPlayer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_scheduledsoundplayer-7oybj)
- [Audio Unit Pitch Subtypes](/documentation/audiotoolbox/1584152-audio-unit-pitch-subtypes)

#### Constants

- [var kAudioUnitSubType_TimePitch: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_timepitch)
- [AudioUnitEventType](/documentation/audiotoolbox/audiouniteventtype)

#### Constants

- [case beginParameterChangeGesture](/documentation/audiotoolbox/audiouniteventtype/beginparameterchangegesture)
- [case endParameterChangeGesture](/documentation/audiotoolbox/audiouniteventtype/endparameterchangegesture)
- [case parameterValueChange](/documentation/audiotoolbox/audiouniteventtype/parametervaluechange)
- [case propertyChange](/documentation/audiotoolbox/audiouniteventtype/propertychange)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiouniteventtype/init(rawvalue:))
- [AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions)

#### Constants

- [static var flag_CFNameRelease: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_cfnamerelease)
- [static var flag_CanRamp: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_canramp)
- [static var flag_DisplayCubeRoot: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaycuberoot)
- [static var flag_DisplayCubed: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaycubed)
- [static var flag_DisplayExponential: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displayexponential)
- [static var flag_DisplayLogarithmic: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaylogarithmic)
- [static var flag_DisplayMask: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaymask)
- [static var flag_DisplaySquareRoot: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaysquareroot)
- [static var flag_DisplaySquared: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaysquared)
- [static var flag_ExpertMode: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_expertmode)
- [static var flag_HasCFNameString: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_hascfnamestring)
- [static var flag_HasClump: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_hasclump)
- [static var flag_IsElementMeta: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_iselementmeta)
- [static var flag_IsGlobalMeta: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_isglobalmeta)
- [static var flag_IsHighResolution: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_ishighresolution)
- [static var flag_IsReadable: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_isreadable)
- [static var flag_IsWritable: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_iswritable)
- [static var flag_MeterReadOnly: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_meterreadonly)
- [static var flag_NonRealTime: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_nonrealtime)
- [static var flag_OmitFromPresets: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_omitfrompresets)
- [static var flag_PlotHistory: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_plothistory)
- [static var flag_ValuesHaveStrings: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_valueshavestrings)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiounitparameteroptions/init(rawvalue:))
- [AudioUnitParameterUnit](/documentation/audiotoolbox/audiounitparameterunit)

#### Enumeration Cases

- [case absoluteCents](/documentation/audiotoolbox/audiounitparameterunit/absolutecents)
- [case BPM](/documentation/audiotoolbox/audiounitparameterunit/bpm)
- [case beats](/documentation/audiotoolbox/audiounitparameterunit/beats)
- [case boolean](/documentation/audiotoolbox/audiounitparameterunit/boolean)
- [case cents](/documentation/audiotoolbox/audiounitparameterunit/cents)
- [case customUnit](/documentation/audiotoolbox/audiounitparameterunit/customunit)
- [case decibels](/documentation/audiotoolbox/audiounitparameterunit/decibels)
- [case degrees](/documentation/audiotoolbox/audiounitparameterunit/degrees)
- [case equalPowerCrossfade](/documentation/audiotoolbox/audiounitparameterunit/equalpowercrossfade)
- [case generic](/documentation/audiotoolbox/audiounitparameterunit/generic)
- [case hertz](/documentation/audiotoolbox/audiounitparameterunit/hertz)
- [case indexed](/documentation/audiotoolbox/audiounitparameterunit/indexed)
- [case linearGain](/documentation/audiotoolbox/audiounitparameterunit/lineargain)
- [case midiController](/documentation/audiotoolbox/audiounitparameterunit/midicontroller)
- [case midiNoteNumber](/documentation/audiotoolbox/audiounitparameterunit/midinotenumber)
- [case meters](/documentation/audiotoolbox/audiounitparameterunit/meters)
- [case milliseconds](/documentation/audiotoolbox/audiounitparameterunit/milliseconds)
- [case mixerFaderCurve1](/documentation/audiotoolbox/audiounitparameterunit/mixerfadercurve1)
- [case octaves](/documentation/audiotoolbox/audiounitparameterunit/octaves)
- [case pan](/documentation/audiotoolbox/audiounitparameterunit/pan)
- [case percent](/documentation/audiotoolbox/audiounitparameterunit/percent)
- [case phase](/documentation/audiotoolbox/audiounitparameterunit/phase)
- [case rate](/documentation/audiotoolbox/audiounitparameterunit/rate)
- [case ratio](/documentation/audiotoolbox/audiounitparameterunit/ratio)
- [case relativeSemiTones](/documentation/audiotoolbox/audiounitparameterunit/relativesemitones)
- [case sampleFrames](/documentation/audiotoolbox/audiounitparameterunit/sampleframes)
- [case seconds](/documentation/audiotoolbox/audiounitparameterunit/seconds)
- [case midi2Controller](/documentation/audiotoolbox/audiounitparameterunit/midi2controller)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiounitparameterunit/init(rawvalue:))
- [AudioUnitRemoteControlEvent](/documentation/audiotoolbox/audiounitremotecontrolevent)

#### Constants

- [case rewind](/documentation/audiotoolbox/audiounitremotecontrolevent/rewind)
- [case togglePlayPause](/documentation/audiotoolbox/audiounitremotecontrolevent/toggleplaypause)
- [case toggleRecord](/documentation/audiotoolbox/audiounitremotecontrolevent/togglerecord)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiounitremotecontrolevent/init(rawvalue:))
- [Audio Unit Sample Rate Converter Complexity](/documentation/audiotoolbox/1534173-audio_unit_sample_rate_converter)

#### Constants

- [var kAudioUnitSampleRateConverterComplexity_Linear: UInt32](/documentation/audiotoolbox/kaudiounitsamplerateconvertercomplexity_linear)
- [var kAudioUnitSampleRateConverterComplexity_Mastering: UInt32](/documentation/audiotoolbox/kaudiounitsamplerateconvertercomplexity_mastering)
- [var kAudioUnitSampleRateConverterComplexity_Normal: UInt32](/documentation/audiotoolbox/kaudiounitsamplerateconvertercomplexity_normal)
- [Audio Unit Scopes](/documentation/audiotoolbox/1534214-audio_unit_scopes)

#### Constants

- [var kAudioUnitScope_Global: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_global)
- [var kAudioUnitScope_Group: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_group)
- [var kAudioUnitScope_Input: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_input)
- [var kAudioUnitScope_Layer: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_layer)
- [var kAudioUnitScope_LayerItem: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_layeritem)
- [var kAudioUnitScope_Note: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_note)
- [var kAudioUnitScope_Output: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_output)
- [var kAudioUnitScope_Part: AudioUnitScope](/documentation/audiotoolbox/kaudiounitscope_part)
- [Audio Unit SRC Algorithms](/documentation/audiotoolbox/1533994-audio-unit-src-algorithms)

#### Constants

- [var kAudioUnitSRCAlgorithm_MediumQuality: UInt32](/documentation/audiotoolbox/kaudiounitsrcalgorithm_mediumquality)
- [var kAudioUnitSRCAlgorithm_Polyphase: UInt32](/documentation/audiotoolbox/kaudiounitsrcalgorithm_polyphase)
- [Audio Unit Full Name Parameter](/documentation/audiotoolbox/1534055-audio-unit-full-name-parameter)

#### Constants

- [var kAudioUnitParameterName_Full: Int](/documentation/audiotoolbox/kaudiounitparametername_full)
- [Audio Unit Parameter Flags](/documentation/audiotoolbox/1534035-audio-unit-parameter-flags)

#### Constants

- [var kAudioUnitParameterFlag_Global: Int](/documentation/audiotoolbox/kaudiounitparameterflag_global)
- [var kAudioUnitParameterFlag_Group: Int](/documentation/audiotoolbox/kaudiounitparameterflag_group)
- [var kAudioUnitParameterFlag_Input: Int](/documentation/audiotoolbox/kaudiounitparameterflag_input)
- [var kAudioUnitParameterFlag_Output: Int](/documentation/audiotoolbox/kaudiounitparameterflag_output)
- [Audio Unit Filter Parameters](/documentation/audiotoolbox/1390052-audio-unit-filter-parameters)

#### Constants

- [var kMultibandFilter_Bandwidth1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_bandwidth1)
- [var kMultibandFilter_Bandwidth2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_bandwidth2)
- [var kMultibandFilter_Bandwidth3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_bandwidth3)
- [var kMultibandFilter_CenterFreq1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centerfreq1)
- [var kMultibandFilter_CenterFreq2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centerfreq2)
- [var kMultibandFilter_CenterFreq3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centerfreq3)
- [var kMultibandFilter_CenterGain1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centergain1)
- [var kMultibandFilter_CenterGain2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centergain2)
- [var kMultibandFilter_CenterGain3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_centergain3)
- [var kMultibandFilter_HighFilterType: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_highfiltertype)
- [var kMultibandFilter_HighFrequency: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_highfrequency)
- [var kMultibandFilter_HighGain: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_highgain)
- [var kMultibandFilter_LowFilterType: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_lowfiltertype)
- [var kMultibandFilter_LowFrequency: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_lowfrequency)
- [var kMultibandFilter_LowGain: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandfilter_lowgain)
- [Audio Unit Generic Properties](/documentation/audiotoolbox/1533969-audio-unit-generic-properties)

#### Constants

- [var kAudioOfflineUnitProperty_InputSize: AudioUnitPropertyID](/documentation/audiotoolbox/kaudioofflineunitproperty_inputsize)
- [var kAudioOfflineUnitProperty_OutputSize: AudioUnitPropertyID](/documentation/audiotoolbox/kaudioofflineunitproperty_outputsize)
- [var kAudioUnitProperty_BusCount: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_buscount)
- [var kAudioUnitProperty_CurrentPreset: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_currentpreset)
- [var kAudioUnitProperty_MIDIControlMapping: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_midicontrolmapping)
- [var kAudioUnitProperty_ParameterValueName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parametervaluename)
- [var kAudioUnitProperty_SRCAlgorithm: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_srcalgorithm)
- [Audio Unit Parameter Flags](/documentation/audiotoolbox/1534166-audio-unit-parameter-flags)

#### Constants

- [var kAudioUnitParameterFlag_HasName: Int](/documentation/audiotoolbox/kaudiounitparameterflag_hasname)
- [Audio Unit Scheduled Sound Player Properties](/documentation/audiotoolbox/1534024-audio-unit-scheduled-sound-playe)

#### Constants

- [var kAudioUnitProperty_CurrentPlayTime: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_currentplaytime)
- [var kAudioUnitProperty_ScheduleAudioSlice: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduleaudioslice)
- [var kAudioUnitProperty_ScheduleStartTimeStamp: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_schedulestarttimestamp)
- [Audio Unit Offline Preflight Flags](/documentation/audiotoolbox/1534010-audio-unit-offline-preflight-fla)

#### Constants

- [var kOfflinePreflight_NotRequired: Int](/documentation/audiotoolbox/kofflinepreflight_notrequired)
- [var kOfflinePreflight_Optional: Int](/documentation/audiotoolbox/kofflinepreflight_optional)
- [var kOfflinePreflight_Required: Int](/documentation/audiotoolbox/kofflinepreflight_required)
- [Audio Unit Migration Properties](/documentation/audiotoolbox/1534149-audio-unit-migration-properties)

#### Constants

- [var kAudioUnitMigrateProperty_FromPlugin: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitmigrateproperty_fromplugin)
- [var kAudioUnitMigrateProperty_OldAutomation: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitmigrateproperty_oldautomation)
- [Audio Unit File Player Properties](/documentation/audiotoolbox/1534079-audio-unit-file-player-propertie)

#### Constants

- [var kAudioUnitProperty_ScheduledFileBufferSizeFrames: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduledfilebuffersizeframes)
- [var kAudioUnitProperty_ScheduledFileIDs: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduledfileids)
- [var kAudioUnitProperty_ScheduledFileNumberBuffers: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduledfilenumberbuffers)
- [var kAudioUnitProperty_ScheduledFilePrime: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduledfileprime)
- [var kAudioUnitProperty_ScheduledFileRegion: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_scheduledfileregion)
- [Audio Unit Parameter Listener](/documentation/audiotoolbox/1509425-audio-unit-parameter-listener)

#### Constants

- [var kAUParameterListener_AnyParameter: AudioUnitParameterID](/documentation/audiotoolbox/kauparameterlistener_anyparameter)
- [Audio Unit Errors](/documentation/audiotoolbox/1584138-audio-unit-errors)

#### Errors

- [var kAudioComponentErr_InstanceInvalidated: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_instanceinvalidated)
- [var kAudioUnitErr_CannotDoInCurrentContext: OSStatus](/documentation/audiotoolbox/kaudiouniterr_cannotdoincurrentcontext)
- [var kAudioUnitErr_FailedInitialization: OSStatus](/documentation/audiotoolbox/kaudiouniterr_failedinitialization)
- [var kAudioUnitErr_FileNotSpecified: OSStatus](/documentation/audiotoolbox/kaudiouniterr_filenotspecified)
- [var kAudioUnitErr_FormatNotSupported: OSStatus](/documentation/audiotoolbox/kaudiouniterr_formatnotsupported)
- [var kAudioUnitErr_Initialized: OSStatus](/documentation/audiotoolbox/kaudiouniterr_initialized)
- [var kAudioUnitErr_InvalidElement: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidelement)
- [var kAudioUnitErr_InvalidFile: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidfile)
- [var kAudioUnitErr_InvalidOfflineRender: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidofflinerender)
- [var kAudioUnitErr_InvalidParameter: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidparameter)
- [var kAudioUnitErr_InvalidProperty: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidproperty)
- [var kAudioUnitErr_InvalidPropertyValue: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidpropertyvalue)
- [var kAudioUnitErr_InvalidScope: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidscope)
- [var kAudioUnitErr_NoConnection: OSStatus](/documentation/audiotoolbox/kaudiouniterr_noconnection)
- [var kAudioUnitErr_PropertyNotInUse: OSStatus](/documentation/audiotoolbox/kaudiouniterr_propertynotinuse)
- [var kAudioUnitErr_PropertyNotWritable: OSStatus](/documentation/audiotoolbox/kaudiouniterr_propertynotwritable)
- [var kAudioUnitErr_TooManyFramesToProcess: OSStatus](/documentation/audiotoolbox/kaudiouniterr_toomanyframestoprocess)
- [var kAudioUnitErr_Unauthorized: OSStatus](/documentation/audiotoolbox/kaudiouniterr_unauthorized)
- [var kAudioUnitErr_Uninitialized: OSStatus](/documentation/audiotoolbox/kaudiouniterr_uninitialized)
- [var kAudioUnitErr_UnknownFileType: OSStatus](/documentation/audiotoolbox/kaudiouniterr_unknownfiletype)
- [var kAudioUnitErr_RenderTimeout: OSStatus](/documentation/audiotoolbox/kaudiouniterr_rendertimeout)
- [var kAudioComponentErr_InstanceTimedOut: OSStatus](/documentation/audiotoolbox/kaudiocomponenterr_instancetimedout)
- [var kAudioUnitErr_ExtensionNotFound: OSStatus](/documentation/audiotoolbox/kaudiouniterr_extensionnotfound)
- [var kAudioUnitErr_InvalidFilePath: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidfilepath)
- [var kAudioUnitErr_InvalidParameterValue: OSStatus](/documentation/audiotoolbox/kaudiouniterr_invalidparametervalue)
- [var kAudioUnitErr_MIDIOutputBufferFull: OSStatus](/documentation/audiotoolbox/kaudiouniterr_midioutputbufferfull)
- [var kAudioUnitErr_MissingKey: OSStatus](/documentation/audiotoolbox/kaudiouniterr_missingkey)
- [var kAudioUnitErr_ComponentManagerNotSupported: OSStatus](/documentation/audiotoolbox/kaudiouniterr_componentmanagernotsupported)
- [AUAudioUnitBusType](/documentation/audiotoolbox/auaudiounitbustype)

#### Constants

- [case input](/documentation/audiotoolbox/auaudiounitbustype/input)
- [case output](/documentation/audiotoolbox/auaudiounitbustype/output)

#### Initializers

- [init?(rawValue: Int)](/documentation/audiotoolbox/auaudiounitbustype/init(rawvalue:))
- [AUEventSampleTime](/documentation/audiotoolbox/1387633-aueventsampletime)

#### Constants

- [var AUEventSampleTimeImmediate: AUEventSampleTime](/documentation/audiotoolbox/aueventsampletimeimmediate)
- [AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags)

#### Constants

- [static var changed: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/changed)
- [static var cycling: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/cycling)
- [static var moving: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/moving)
- [static var recording: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/recording)

#### Initializers

- [init(rawValue: UInt)](/documentation/audiotoolbox/auhosttransportstateflags/init(rawvalue:))
- [AUParameterAutomationEventType](/documentation/audiotoolbox/auparameterautomationeventtype)

#### Constants

- [case release](/documentation/audiotoolbox/auparameterautomationeventtype/release)
- [case touch](/documentation/audiotoolbox/auparameterautomationeventtype/touch)
- [case value](/documentation/audiotoolbox/auparameterautomationeventtype/value)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auparameterautomationeventtype/init(rawvalue:))
- [AUParameterEventType](/documentation/audiotoolbox/auparametereventtype)

#### Constants

- [case parameterEvent_Immediate](/documentation/audiotoolbox/auparametereventtype/parameterevent_immediate)
- [case parameterEvent_Ramped](/documentation/audiotoolbox/auparametereventtype/parameterevent_ramped)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auparametereventtype/init(rawvalue:))
- [AURenderEventType](/documentation/audiotoolbox/aurendereventtype)

#### Constants

- [case MIDI](/documentation/audiotoolbox/aurendereventtype/midi)
- [case midiSysEx](/documentation/audiotoolbox/aurendereventtype/midisysex)
- [case parameter](/documentation/audiotoolbox/aurendereventtype/parameter)
- [case parameterRamp](/documentation/audiotoolbox/aurendereventtype/parameterramp)

#### Enumeration Cases

- [case midiEventList](/documentation/audiotoolbox/aurendereventtype/midieventlist)

#### Initializers

- [init?(rawValue: UInt8)](/documentation/audiotoolbox/aurendereventtype/init(rawvalue:))
- [AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags)

#### Constants

- [static var scheduledAudioSliceFlag_BeganToRender: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_begantorender)
- [static var scheduledAudioSliceFlag_BeganToRenderLate: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_begantorenderlate)
- [static var scheduledAudioSliceFlag_Complete: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_complete)
- [static var scheduledAudioSliceFlag_Interrupt: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_interrupt)
- [static var scheduledAudioSliceFlag_InterruptAtLoop: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_interruptatloop)
- [static var scheduledAudioSliceFlag_Loop: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_loop)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auscheduledaudiosliceflags/init(rawvalue:))
- [AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags)

#### Constants

- [static var anyChannelFlag: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/anychannelflag)
- [static var anyNoteFlag: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/anynoteflag)
- [static var bipolar: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/bipolar)
- [static var bipolar_On: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/bipolar_on)
- [static var subRange: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/subrange)
- [static var toggle: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/toggle)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auparametermidimappingflags/init(rawvalue:))
- [Audio Unit Properties](/documentation/audiotoolbox/audio-unit-properties)

### General

- [Other Plug-In Formats](/documentation/audiotoolbox/1534082-other-plug-in-formats)

#### Constants

- [var kOtherPluginFormat_AU: UInt32](/documentation/audiotoolbox/kotherpluginformat_au)
- [var kOtherPluginFormat_Undefined: UInt32](/documentation/audiotoolbox/kotherpluginformat_undefined)
- [var kOtherPluginFormat_kMAS: UInt32](/documentation/audiotoolbox/kotherpluginformat_kmas)
- [var kOtherPluginFormat_kVST: UInt32](/documentation/audiotoolbox/kotherpluginformat_kvst)
- [RenderQuality](/documentation/audiotoolbox/1534177-renderquality)

#### Constants

- [var kRenderQuality_High: Int](/documentation/audiotoolbox/krenderquality_high)
- [var kRenderQuality_Low: Int](/documentation/audiotoolbox/krenderquality_low)
- [var kRenderQuality_Max: Int](/documentation/audiotoolbox/krenderquality_max)
- [var kRenderQuality_Medium: Int](/documentation/audiotoolbox/krenderquality_medium)
- [var kRenderQuality_Min: Int](/documentation/audiotoolbox/krenderquality_min)
- [General Audio Unit Properties](/documentation/audiotoolbox/general-audio-unit-properties)

#### Properties

- [var kAudioUnitProperty_ElementCount: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_elementcount)
- [var kAudioUnitProperty_SupportedNumChannels: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_supportednumchannels)
- [var kAudioUnitProperty_AudioChannelLayout: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_audiochannellayout)
- [var kAudioUnitProperty_AudioUnitMIDIProtocol: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_audiounitmidiprotocol)
- [var kAudioUnitProperty_AUHostIdentifier: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_auhostidentifier)
- [var kAudioUnitProperty_BypassEffect: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_bypasseffect)
- [var kAudioUnitProperty_ClassInfo: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_classinfo)
- [var kAudioUnitProperty_ClassInfoFromDocument: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_classinfofromdocument)
- [var kAudioUnitProperty_CocoaUI: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_cocoaui)
- [var kAudioUnitProperty_ContextName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_contextname)
- [var kAudioUnitProperty_CPULoad: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_cpuload)
- [var kAudioUnitProperty_DependentParameters: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_dependentparameters)
- [var kAudioUnitProperty_ElementName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_elementname)
- [var kAudioUnitProperty_FactoryPresets: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_factorypresets)
- [var kAudioUnitProperty_FastDispatch: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_fastdispatch)
- [var kAudioUnitProperty_FrequencyResponse: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_frequencyresponse)
- [var kAudioUnitProperty_GetUIComponentList: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_getuicomponentlist)
- [var kAudioUnitProperty_HostCallbacks: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_hostcallbacks)
- [var kAudioUnitProperty_HostMIDIProtocol: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_hostmidiprotocol)
- [var kAudioUnitProperty_IconLocation: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_iconlocation)
- [var kAudioUnitProperty_InPlaceProcessing: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_inplaceprocessing)
- [var kAudioUnitProperty_InputSamplesInOutput: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_inputsamplesinoutput)
- [var kAudioUnitProperty_LastRenderError: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_lastrendererror)
- [var kAudioUnitProperty_LastRenderSampleTime: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_lastrendersampletime)
- [var kAudioUnitProperty_Latency: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_latency)
- [var kAudioUnitProperty_LoadedOutOfProcess: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_loadedoutofprocess)
- [var kAudioUnitProperty_MakeConnection: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_makeconnection)
- [var kAudioUnitProperty_MIDIOutputBufferSizeHint: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_midioutputbuffersizehint)
- [var kAudioUnitProperty_MIDIOutputCallback: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_midioutputcallback)
- [var kAudioUnitProperty_MIDIOutputCallbackInfo: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_midioutputcallbackinfo)
- [var kAudioUnitProperty_MIDIOutputEventListCallback: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_midioutputeventlistcallback)
- [var kAudioUnitProperty_MaximumFramesPerSlice: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_maximumframesperslice)
- [var kAudioUnitProperty_NickName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_nickname)
- [var kAudioUnitProperty_OfflineRender: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_offlinerender)
- [var kAudioUnitProperty_ParameterClumpName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameterclumpname)
- [var kAudioUnitProperty_ParameterHistoryInfo: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameterhistoryinfo)
- [var kAudioUnitProperty_ParameterIDName: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameteridname)
- [var kAudioUnitProperty_ParameterInfo: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameterinfo)
- [var kAudioUnitProperty_ParameterList: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameterlist)
- [var kAudioUnitProperty_ParameterStringFromValue: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parameterstringfromvalue)
- [var kAudioUnitProperty_ParameterValueFromString: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parametervaluefromstring)
- [var kAudioUnitProperty_ParameterValueStrings: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parametervaluestrings)
- [var kAudioUnitProperty_ParametersForOverview: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_parametersforoverview)
- [var kAudioUnitProperty_PresentPreset: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_presentpreset)
- [var kAudioUnitProperty_PresentationLatency: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_presentationlatency)
- [var kAudioUnitProperty_RenderQuality: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_renderquality)
- [var kAudioUnitProperty_RequestViewController: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_requestviewcontroller)
- [var kAudioUnitProperty_SampleRate: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_samplerate)
- [var kAudioUnitProperty_SetExternalBuffer: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_setexternalbuffer)
- [var kAudioUnitProperty_SetRenderCallback: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_setrendercallback)
- [var kAudioUnitProperty_StreamFormat: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_streamformat)
- [var kAudioUnitProperty_ShouldAllocateBuffer: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_shouldallocatebuffer)
- [var kAudioUnitProperty_SupportedChannelLayoutTags: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_supportedchannellayouttags)
- [var kAudioUnitProperty_SupportsMPE: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_supportsmpe)
- [var kAudioUnitProperty_TailTime: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_tailtime)
- [HostCallbackInfo](/documentation/audiotoolbox/hostcallbackinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/hostcallbackinfo/init())
- [init(hostUserData: UnsafeMutableRawPointer?, beatAndTempoProc: HostCallback_GetBeatAndTempo?, musicalTimeLocationProc: HostCallback_GetMusicalTimeLocation?, transportStateProc: HostCallback_GetTransportState?, transportStateProc2: HostCallback_GetTransportState2?)](/documentation/audiotoolbox/hostcallbackinfo/init(hostuserdata:beatandtempoproc:musicaltimelocationproc:transportstateproc:transportstateproc2:))

#### Instance Properties

- [var beatAndTempoProc: HostCallback_GetBeatAndTempo?](/documentation/audiotoolbox/hostcallbackinfo/beatandtempoproc)
- [var hostUserData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/hostcallbackinfo/hostuserdata)
- [var musicalTimeLocationProc: HostCallback_GetMusicalTimeLocation?](/documentation/audiotoolbox/hostcallbackinfo/musicaltimelocationproc)
- [var transportStateProc: HostCallback_GetTransportState?](/documentation/audiotoolbox/hostcallbackinfo/transportstateproc)
- [var transportStateProc2: HostCallback_GetTransportState2?](/documentation/audiotoolbox/hostcallbackinfo/transportstateproc2)

### Mixers

- [Audio Unit Mixer Subtypes](/documentation/audiotoolbox/1584146-audio-unit-mixer-subtypes)

#### Constants

- [var kAudioUnitSubType_3DMixer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_3dmixer)
- [var kAudioUnitSubType_StereoMixer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_stereomixer)
- [AUSpatialMixerAttenuationCurve](/documentation/audiotoolbox/auspatialmixerattenuationcurve)

#### Constants

- [case spatialMixerAttenuationCurve_Exponential](/documentation/audiotoolbox/auspatialmixerattenuationcurve/spatialmixerattenuationcurve_exponential)
- [case spatialMixerAttenuationCurve_Inverse](/documentation/audiotoolbox/auspatialmixerattenuationcurve/spatialmixerattenuationcurve_inverse)
- [case spatialMixerAttenuationCurve_Linear](/documentation/audiotoolbox/auspatialmixerattenuationcurve/spatialmixerattenuationcurve_linear)
- [case spatialMixerAttenuationCurve_Power](/documentation/audiotoolbox/auspatialmixerattenuationcurve/spatialmixerattenuationcurve_power)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixerattenuationcurve/init(rawvalue:))
- [AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags)

#### Constants

- [static var spatialMixerRenderingFlags_DistanceAttenuation: AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags/spatialmixerrenderingflags_distanceattenuation)
- [static var spatialMixerRenderingFlags_InterAuralDelay: AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags/spatialmixerrenderingflags_interauraldelay)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixerrenderingflags/init(rawvalue:))
- [AUSpatialMixer Parameters](/documentation/audiotoolbox/1390073-auspatialmixer-parameters)

#### Constants

- [var kSpatialMixerParam_Azimuth: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_azimuth)
- [var kSpatialMixerParam_Distance: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_distance)
- [var kSpatialMixerParam_Elevation: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_elevation)
- [var kSpatialMixerParam_Enable: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_enable)
- [var kSpatialMixerParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_gain)
- [var kSpatialMixerParam_GlobalReverbGain: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_globalreverbgain)
- [var kSpatialMixerParam_MaxGain: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_maxgain)
- [var kSpatialMixerParam_MinGain: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_mingain)
- [var kSpatialMixerParam_ObstructionAttenuation: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_obstructionattenuation)
- [var kSpatialMixerParam_OcclusionAttenuation: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_occlusionattenuation)
- [var kSpatialMixerParam_PlaybackRate: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_playbackrate)
- [var kSpatialMixerParam_ReverbBlend: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_reverbblend)
- [var kSpatialMixerParam_HeadPitch: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_headpitch)
- [var kSpatialMixerParam_HeadRoll: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_headroll)
- [var kSpatialMixerParam_HeadYaw: AudioUnitParameterID](/documentation/audiotoolbox/kspatialmixerparam_headyaw)
- [Panner Audio Unit Parameters](/documentation/audiotoolbox/1389991-panner-audio-unit-parameters)

#### Constants

- [var kPannerParam_Azimuth: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_azimuth)
- [var kPannerParam_CoordScale: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_coordscale)
- [var kPannerParam_Distance: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_distance)
- [var kPannerParam_Elevation: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_elevation)
- [var kPannerParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_gain)
- [var kPannerParam_RefDistance: AudioUnitParameterID](/documentation/audiotoolbox/kpannerparam_refdistance)
- [AUMatrixMixer Parameters](/documentation/audiotoolbox/1390003-aumatrixmixer-parameters)

#### Constants

- [var kMatrixMixerParam_Enable: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_enable)
- [var kMatrixMixerParam_PostAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_postaveragepower)
- [var kMatrixMixerParam_PostAveragePowerLinear: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_postaveragepowerlinear)
- [var kMatrixMixerParam_PostPeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_postpeakholdlevel)
- [var kMatrixMixerParam_PostPeakHoldLevelLinear: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_postpeakholdlevellinear)
- [var kMatrixMixerParam_PreAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_preaveragepower)
- [var kMatrixMixerParam_PreAveragePowerLinear: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_preaveragepowerlinear)
- [var kMatrixMixerParam_PrePeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_prepeakholdlevel)
- [var kMatrixMixerParam_PrePeakHoldLevelLinear: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_prepeakholdlevellinear)
- [var kMatrixMixerParam_Volume: AudioUnitParameterID](/documentation/audiotoolbox/kmatrixmixerparam_volume)
- [AUMultiChannelMixer Parameters](/documentation/audiotoolbox/1389739-aumultichannelmixer_parameters)

#### Constants

- [var kMultiChannelMixerParam_Enable: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_enable)
- [var kMultiChannelMixerParam_Pan: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_pan)
- [var kMultiChannelMixerParam_PostAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_postaveragepower)
- [var kMultiChannelMixerParam_PostPeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_postpeakholdlevel)
- [var kMultiChannelMixerParam_PreAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_preaveragepower)
- [var kMultiChannelMixerParam_PrePeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_prepeakholdlevel)
- [var kMultiChannelMixerParam_Volume: AudioUnitParameterID](/documentation/audiotoolbox/kmultichannelmixerparam_volume)
- [Spatial Mixer Property IDs](/documentation/audiotoolbox/1534150-spatial-mixer-property-ids)

#### Constants

- [var kAudioUnitProperty_ReverbRoomType: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_reverbroomtype)
- [var kAudioUnitProperty_SpatialMixerAttenuationCurve: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerattenuationcurve)
- [var kAudioUnitProperty_SpatialMixerDistanceParams: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerdistanceparams)
- [var kAudioUnitProperty_SpatialMixerRenderingFlags: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerrenderingflags)
- [var kAudioUnitProperty_SpatializationAlgorithm: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatializationalgorithm)
- [var kAudioUnitProperty_UsesInternalReverb: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_usesinternalreverb)
- [var kAudioUnitProperty_SpatialMixerOutputType: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixeroutputtype)
- [var kAudioUnitProperty_SpatialMixerPointSourceInHeadMode: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerpointsourceinheadmode)
- [var kAudioUnitProperty_SpatialMixerSourceMode: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixersourcemode)
- [var kAudioUnitProperty_SpatialMixerAnyInputIsUsingPersonalizedHRTF: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixeranyinputisusingpersonalizedhrtf)
- [var kAudioUnitProperty_SpatialMixerEnableHeadTracking: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerenableheadtracking)
- [var kAudioUnitProperty_SpatialMixerPersonalizedHRTFMode: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_spatialmixerpersonalizedhrtfmode)
- [Stereo Mixer Unit Parameters](/documentation/audiotoolbox/1389928-stereo-mixer-unit-parameters)

#### Constants

- [var kStereoMixerParam_Pan: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_pan)
- [var kStereoMixerParam_PostAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_postaveragepower)
- [var kStereoMixerParam_PostPeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_postpeakholdlevel)
- [var kStereoMixerParam_PreAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_preaveragepower)
- [var kStereoMixerParam_PrePeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_prepeakholdlevel)
- [var kStereoMixerParam_Volume: AudioUnitParameterID](/documentation/audiotoolbox/kstereomixerparam_volume)
- [Mixer Audio Unit Properties](/documentation/audiotoolbox/1534041-mixer_audio_unit_properties)

#### Constants

- [var kAudioUnitProperty_InputAnchorTimeStamp: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_inputanchortimestamp)
- [var kAudioUnitProperty_MatrixDimensions: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_matrixdimensions)
- [var kAudioUnitProperty_MatrixLevels: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_matrixlevels)
- [var kAudioUnitProperty_MeterClipping: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_meterclipping)
- [var kAudioUnitProperty_MeteringMode: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_meteringmode)
- [Mixer Audio Unit Subtypes](/documentation/audiotoolbox/1584150-mixer_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_MatrixMixer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_matrixmixer)
- [var kAudioUnitSubType_MultiChannelMixer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_multichannelmixer)
- [var kAudioUnitSubType_SpatialMixer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_spatialmixer)
- [AUSpatialMixerOutputType](/documentation/audiotoolbox/auspatialmixeroutputtype)

#### Output Types

- [case spatialMixerOutputType_BuiltInSpeakers](/documentation/audiotoolbox/auspatialmixeroutputtype/spatialmixeroutputtype_builtinspeakers)
- [case spatialMixerOutputType_ExternalSpeakers](/documentation/audiotoolbox/auspatialmixeroutputtype/spatialmixeroutputtype_externalspeakers)
- [case spatialMixerOutputType_Headphones](/documentation/audiotoolbox/auspatialmixeroutputtype/spatialmixeroutputtype_headphones)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixeroutputtype/init(rawvalue:))
- [AUSpatialMixerPointSourceInHeadMode](/documentation/audiotoolbox/auspatialmixerpointsourceinheadmode)

#### Modes

- [case spatialMixerPointSourceInHeadMode_Bypass](/documentation/audiotoolbox/auspatialmixerpointsourceinheadmode/spatialmixerpointsourceinheadmode_bypass)
- [case spatialMixerPointSourceInHeadMode_Mono](/documentation/audiotoolbox/auspatialmixerpointsourceinheadmode/spatialmixerpointsourceinheadmode_mono)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixerpointsourceinheadmode/init(rawvalue:))
- [AUSpatialMixerSourceMode](/documentation/audiotoolbox/auspatialmixersourcemode)

#### Modes

- [case spatialMixerSourceMode_AmbienceBed](/documentation/audiotoolbox/auspatialmixersourcemode/spatialmixersourcemode_ambiencebed)
- [case spatialMixerSourceMode_Bypass](/documentation/audiotoolbox/auspatialmixersourcemode/spatialmixersourcemode_bypass)
- [case spatialMixerSourceMode_PointSource](/documentation/audiotoolbox/auspatialmixersourcemode/spatialmixersourcemode_pointsource)
- [case spatialMixerSourceMode_SpatializeIfMono](/documentation/audiotoolbox/auspatialmixersourcemode/spatialmixersourcemode_spatializeifmono)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixersourcemode/init(rawvalue:))
- [3D Mixer Unit Parameters](/documentation/audiotoolbox/1389763-3d_mixer_unit_parameters)

#### Constants

- [var k3DMixerParam_Azimuth: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_azimuth)
- [var k3DMixerParam_Distance: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_distance)
- [var k3DMixerParam_Elevation: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_elevation)
- [var k3DMixerParam_Enable: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_enable)
- [var k3DMixerParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_gain)
- [var k3DMixerParam_GlobalReverbGain: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_globalreverbgain)
- [var k3DMixerParam_MaxGain: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_maxgain)
- [var k3DMixerParam_MinGain: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_mingain)
- [var k3DMixerParam_ObstructionAttenuation: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_obstructionattenuation)
- [var k3DMixerParam_OcclusionAttenuation: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_occlusionattenuation)
- [var k3DMixerParam_PlaybackRate: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_playbackrate)
- [var k3DMixerParam_PostAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_postaveragepower)
- [var k3DMixerParam_PostPeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_postpeakholdlevel)
- [var k3DMixerParam_PreAveragePower: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_preaveragepower)
- [var k3DMixerParam_PrePeakHoldLevel: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_prepeakholdlevel)
- [var k3DMixerParam_ReverbBlend: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_reverbblend)
- [var k3DMixerParam_BusEnable: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_busenable)
- [var k3DMixerParam_DryWetReverbBlend: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_drywetreverbblend)
- [var k3DMixerParam_GlobalReverbGainInDecibels: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_globalreverbgainindecibels)
- [var k3DMixerParam_MaxGainInDecibels: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_maxgainindecibels)
- [var k3DMixerParam_MinGainInDecibels: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_mingainindecibels)
- [var k3DMixerParam_ObstructionAttenuationInDecibels: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_obstructionattenuationindecibels)
- [var k3DMixerParam_OcclusionAttenuationInDecibels: AudioUnitParameterID](/documentation/audiotoolbox/k3dmixerparam_occlusionattenuationindecibels)
- [AU3DMixerAttenuationCurve](/documentation/audiotoolbox/au3dmixerattenuationcurve)

#### Constants

- [case k3DMixerAttenuationCurve_Exponential](/documentation/audiotoolbox/au3dmixerattenuationcurve/k3dmixerattenuationcurve_exponential)
- [case k3DMixerAttenuationCurve_Inverse](/documentation/audiotoolbox/au3dmixerattenuationcurve/k3dmixerattenuationcurve_inverse)
- [case k3DMixerAttenuationCurve_Linear](/documentation/audiotoolbox/au3dmixerattenuationcurve/k3dmixerattenuationcurve_linear)
- [case k3DMixerAttenuationCurve_Power](/documentation/audiotoolbox/au3dmixerattenuationcurve/k3dmixerattenuationcurve_power)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/au3dmixerattenuationcurve/init(rawvalue:))
- [AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags)

#### Constants

- [static var k3DMixerRenderingFlags_ConstantReverbBlend: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_constantreverbblend)
- [static var k3DMixerRenderingFlags_DistanceAttenuation: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distanceattenuation)
- [static var k3DMixerRenderingFlags_DistanceDiffusion: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distancediffusion)
- [static var k3DMixerRenderingFlags_DistanceFilter: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distancefilter)
- [static var k3DMixerRenderingFlags_DopplerShift: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_dopplershift)
- [static var k3DMixerRenderingFlags_InterAuralDelay: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_interauraldelay)
- [static var k3DMixerRenderingFlags_LinearDistanceAttenuation: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_lineardistanceattenuation)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/au3dmixerrenderingflags/init(rawvalue:))
- [MixerDistanceParams](/documentation/audiotoolbox/mixerdistanceparams)

#### Initializers

- [init()](/documentation/audiotoolbox/mixerdistanceparams/init())
- [init(mReferenceDistance: Float32, mMaxDistance: Float32, mMaxAttenuation: Float32)](/documentation/audiotoolbox/mixerdistanceparams/init(mreferencedistance:mmaxdistance:mmaxattenuation:))

#### Instance Properties

- [var mMaxAttenuation: Float32](/documentation/audiotoolbox/mixerdistanceparams/mmaxattenuation)
- [var mMaxDistance: Float32](/documentation/audiotoolbox/mixerdistanceparams/mmaxdistance)
- [var mReferenceDistance: Float32](/documentation/audiotoolbox/mixerdistanceparams/mreferencedistance)

### Equalizers

- [Parametric EQ Unit Parameters](/documentation/audiotoolbox/1389950-parametric_eq_unit_parameters)

#### Constants

- [var kParametricEQParam_CenterFreq: AudioUnitParameterID](/documentation/audiotoolbox/kparametriceqparam_centerfreq)
- [var kParametricEQParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kparametriceqparam_gain)
- [var kParametricEQParam_Q: AudioUnitParameterID](/documentation/audiotoolbox/kparametriceqparam_q)
- [Audio Unit Graphic EQ Parameter ID](/documentation/audiotoolbox/1389932-audio-unit-graphic-eq-parameter)

#### Constants

- [var kGraphicEQParam_NumberOfBands: AudioUnitParameterID](/documentation/audiotoolbox/kgraphiceqparam_numberofbands)
- [Peak Limiter Unit Parameters](/documentation/audiotoolbox/1389597-peak_limiter_unit_parameters)

#### Constants

- [var kLimiterParam_AttackTime: AudioUnitParameterID](/documentation/audiotoolbox/klimiterparam_attacktime)
- [var kLimiterParam_DecayTime: AudioUnitParameterID](/documentation/audiotoolbox/klimiterparam_decaytime)
- [var kLimiterParam_PreGain: AudioUnitParameterID](/documentation/audiotoolbox/klimiterparam_pregain)
- [Dynamics Processor Unit Parameters](/documentation/audiotoolbox/1389787-dynamics_processor_unit_paramete)

#### Constants

- [var kDynamicsProcessorParam_AttackTime: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_attacktime)
- [var kDynamicsProcessorParam_CompressionAmount: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_compressionamount)
- [var kDynamicsProcessorParam_ExpansionRatio: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_expansionratio)
- [var kDynamicsProcessorParam_ExpansionThreshold: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_expansionthreshold)
- [var kDynamicsProcessorParam_HeadRoom: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_headroom)
- [var kDynamicsProcessorParam_InputAmplitude: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_inputamplitude)
- [var kDynamicsProcessorParam_MasterGain: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_mastergain)
- [var kDynamicsProcessorParam_OutputAmplitude: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_outputamplitude)
- [var kDynamicsProcessorParam_ReleaseTime: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_releasetime)
- [var kDynamicsProcessorParam_Threshold: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_threshold)
- [var kDynamicsProcessorParam_OverallGain: AudioUnitParameterID](/documentation/audiotoolbox/kdynamicsprocessorparam_overallgain)
- [Frequency Response Constants](/documentation/audiotoolbox/1534092-frequency_response_constants)

#### Constants

- [var kNumberOfResponseFrequencies: Int](/documentation/audiotoolbox/knumberofresponsefrequencies)
- [AUSpatializationAlgorithm](/documentation/audiotoolbox/auspatializationalgorithm)

#### Constants

- [case spatializationAlgorithm_EqualPowerPanning](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_equalpowerpanning)
- [case spatializationAlgorithm_HRTF](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_hrtf)
- [case spatializationAlgorithm_SoundField](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_soundfield)
- [case spatializationAlgorithm_SphericalHead](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_sphericalhead)
- [case spatializationAlgorithm_StereoPassThrough](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_stereopassthrough)
- [case spatializationAlgorithm_VectorBasedPanning](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_vectorbasedpanning)

#### Enumeration Cases

- [case spatializationAlgorithm_HRTFHQ](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_hrtfhq)
- [case spatializationAlgorithm_UseOutputType](/documentation/audiotoolbox/auspatializationalgorithm/spatializationalgorithm_useoutputtype)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatializationalgorithm/init(rawvalue:))

### Filters

- [Audio Unit Filter Subtypes](/documentation/audiotoolbox/1584153-audio-unit-filter-subtypes)

#### Constants

- [var kAudioUnitSubType_AUFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_aufilter)
- [var kAudioUnitSubType_GraphicEQ: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_graphiceq)
- [var kAudioUnitSubType_MatrixReverb: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_matrixreverb)
- [var kAudioUnitSubType_MultiBandCompressor: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_multibandcompressor)
- [var kAudioUnitSubType_NetSend: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_netsend)
- [var kAudioUnitSubType_Pitch: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_pitch)
- [var kAudioUnitSubType_RogerBeep: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_rogerbeep)
- [Bandpass Unit Parameters](/documentation/audiotoolbox/1390144-bandpass_unit_parameters)

#### Constants

- [var kBandpassParam_Bandwidth: AudioUnitParameterID](/documentation/audiotoolbox/kbandpassparam_bandwidth)
- [var kBandpassParam_CenterFrequency: AudioUnitParameterID](/documentation/audiotoolbox/kbandpassparam_centerfrequency)
- [AUHipass Parameters](/documentation/audiotoolbox/1389948-auhipass_parameters)

#### Constants

- [var kHipassParam_CutoffFrequency: AudioUnitParameterID](/documentation/audiotoolbox/khipassparam_cutofffrequency)
- [var kHipassParam_Resonance: AudioUnitParameterID](/documentation/audiotoolbox/khipassparam_resonance)
- [AULowpass Parameters](/documentation/audiotoolbox/1389999-aulowpass_parameters)

#### Constants

- [var kLowPassParam_CutoffFrequency: AudioUnitParameterID](/documentation/audiotoolbox/klowpassparam_cutofffrequency)
- [var kLowPassParam_Resonance: AudioUnitParameterID](/documentation/audiotoolbox/klowpassparam_resonance)
- [AULowShelf Parameters](/documentation/audiotoolbox/1389995-aulowshelf_parameters)

#### Constants

- [var kAULowShelfParam_CutoffFrequency: AudioUnitParameterID](/documentation/audiotoolbox/kaulowshelfparam_cutofffrequency)
- [var kAULowShelfParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kaulowshelfparam_gain)
- [AUHighShelfFilter Parameters](/documentation/audiotoolbox/1389967-auhighshelffilter_parameters)

#### Constants

- [var kHighShelfParam_CutOffFrequency: AudioUnitParameterID](/documentation/audiotoolbox/khighshelfparam_cutofffrequency)
- [var kHighShelfParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/khighshelfparam_gain)
- [AUNBandEQ Filter Types](/documentation/audiotoolbox/1389965-aunbandeq_filter_types)

#### Constants

- [var kAUNBandEQFilterType_2ndOrderButterworthHighPass: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_2ndorderbutterworthhighpass)
- [var kAUNBandEQFilterType_2ndOrderButterworthLowPass: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_2ndorderbutterworthlowpass)
- [var kAUNBandEQFilterType_BandPass: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_bandpass)
- [var kAUNBandEQFilterType_BandStop: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_bandstop)
- [var kAUNBandEQFilterType_HighShelf: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_highshelf)
- [var kAUNBandEQFilterType_LowShelf: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_lowshelf)
- [var kAUNBandEQFilterType_Parametric: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_parametric)
- [var kAUNBandEQFilterType_ResonantHighPass: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_resonanthighpass)
- [var kAUNBandEQFilterType_ResonantHighShelf: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_resonanthighshelf)
- [var kAUNBandEQFilterType_ResonantLowPass: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_resonantlowpass)
- [var kAUNBandEQFilterType_ResonantLowShelf: Int](/documentation/audiotoolbox/kaunbandeqfiltertype_resonantlowshelf)
- [var kNumAUNBandEQFilterTypes: Int](/documentation/audiotoolbox/knumaunbandeqfiltertypes)
- [AUNBandEQ Property IDs](/documentation/audiotoolbox/1534022-aunbandeq-property-ids)

#### Constants

- [var kAUNBandEQProperty_BiquadCoefficients: AudioUnitPropertyID](/documentation/audiotoolbox/kaunbandeqproperty_biquadcoefficients)
- [var kAUNBandEQProperty_MaxNumberOfBands: AudioUnitPropertyID](/documentation/audiotoolbox/kaunbandeqproperty_maxnumberofbands)
- [var kAUNBandEQProperty_NumberOfBands: AudioUnitPropertyID](/documentation/audiotoolbox/kaunbandeqproperty_numberofbands)
- [AUNBandEQ Parameters](/documentation/audiotoolbox/1389745-aunbandeq-parameters)

#### Constants

- [var kAUNBandEQParam_Bandwidth: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_bandwidth)
- [var kAUNBandEQParam_BypassBand: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_bypassband)
- [var kAUNBandEQParam_FilterType: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_filtertype)
- [var kAUNBandEQParam_Frequency: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_frequency)
- [var kAUNBandEQParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_gain)
- [var kAUNBandEQParam_GlobalGain: AudioUnitParameterID](/documentation/audiotoolbox/kaunbandeqparam_globalgain)

### Effects

- [Effect Audio Unit Subtypes](/documentation/audiotoolbox/1584154-effect_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_AUiPodEQ: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auipodeq)
- [var kAudioUnitSubType_BandPassFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_bandpassfilter)
- [var kAudioUnitSubType_Delay: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_delay)
- [var kAudioUnitSubType_Distortion: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_distortion)
- [var kAudioUnitSubType_DynamicsProcessor: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_dynamicsprocessor)
- [var kAudioUnitSubType_HighPassFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_highpassfilter)
- [var kAudioUnitSubType_HighShelfFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_highshelffilter)
- [var kAudioUnitSubType_LowPassFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_lowpassfilter)
- [var kAudioUnitSubType_LowShelfFilter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_lowshelffilter)
- [var kAudioUnitSubType_NBandEQ: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_nbandeq)
- [var kAudioUnitSubType_ParametricEQ: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_parametriceq)
- [var kAudioUnitSubType_PeakLimiter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_peaklimiter)
- [var kAudioUnitSubType_SampleDelay: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_sampledelay)
- [var kAudioUnitSubType_AUSoundIsolation: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_ausoundisolation)
- [var kAudioUnitSubType_Reverb2: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_reverb2)
- [AUMatrixReverb Parameters](/documentation/audiotoolbox/1389801-aumatrixreverb-parameters)

#### Constants

- [var kReverbParam_DryWetMix: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_drywetmix)
- [var kReverbParam_LargeBrightness: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_largebrightness)
- [var kReverbParam_LargeDelay: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_largedelay)
- [var kReverbParam_LargeDelayRange: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_largedelayrange)
- [var kReverbParam_LargeDensity: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_largedensity)
- [var kReverbParam_LargeSize: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_largesize)
- [var kReverbParam_ModulationDepth: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_modulationdepth)
- [var kReverbParam_ModulationRate: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_modulationrate)
- [var kReverbParam_PreDelay: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_predelay)
- [var kReverbParam_SmallBrightness: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_smallbrightness)
- [var kReverbParam_SmallDelayRange: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_smalldelayrange)
- [var kReverbParam_SmallDensity: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_smalldensity)
- [var kReverbParam_SmallLargeMix: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_smalllargemix)
- [var kReverbParam_SmallSize: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_smallsize)
- [AUDistortion Parameters](/documentation/audiotoolbox/1390086-audistortion-parameters)

#### Constants

- [var kDistortionParam_CubicTerm: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_cubicterm)
- [var kDistortionParam_Decay: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_decay)
- [var kDistortionParam_Decimation: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_decimation)
- [var kDistortionParam_DecimationMix: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_decimationmix)
- [var kDistortionParam_Delay: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_delay)
- [var kDistortionParam_DelayMix: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_delaymix)
- [var kDistortionParam_FinalMix: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_finalmix)
- [var kDistortionParam_LinearTerm: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_linearterm)
- [var kDistortionParam_PolynomialMix: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_polynomialmix)
- [var kDistortionParam_RingModBalance: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_ringmodbalance)
- [var kDistortionParam_RingModFreq1: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_ringmodfreq1)
- [var kDistortionParam_RingModFreq2: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_ringmodfreq2)
- [var kDistortionParam_RingModMix: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_ringmodmix)
- [var kDistortionParam_Rounding: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_rounding)
- [var kDistortionParam_SoftClipGain: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_softclipgain)
- [var kDistortionParam_SquaredTerm: AudioUnitParameterID](/documentation/audiotoolbox/kdistortionparam_squaredterm)
- [Reverb Parameters](/documentation/audiotoolbox/1390119-reverb_parameters)

#### Constants

- [var kReverbParam_FilterBandwidth: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_filterbandwidth)
- [var kReverbParam_FilterEnable: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_filterenable)
- [var kReverbParam_FilterFrequency: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_filterfrequency)
- [var kReverbParam_FilterGain: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_filtergain)
- [var kReverbParam_FilterType: AudioUnitParameterID](/documentation/audiotoolbox/kreverbparam_filtertype)
- [Reverb Unit Parameters](/documentation/audiotoolbox/1615024-reverb_unit_parameters)

#### Constants

- [var kReverb2Param_DecayTimeAt0Hz: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_decaytimeat0hz)
- [var kReverb2Param_DecayTimeAtNyquist: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_decaytimeatnyquist)
- [var kReverb2Param_DryWetMix: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_drywetmix)
- [var kReverb2Param_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_gain)
- [var kReverb2Param_MaxDelayTime: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_maxdelaytime)
- [var kReverb2Param_MinDelayTime: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_mindelaytime)
- [var kReverb2Param_RandomizeReflections: AudioUnitParameterID](/documentation/audiotoolbox/kreverb2param_randomizereflections)
- [AUReverbRoomType](/documentation/audiotoolbox/aureverbroomtype)

#### Constants

- [case reverbRoomType_Cathedral](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_cathedral)
- [case reverbRoomType_LargeChamber](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_largechamber)
- [case reverbRoomType_LargeHall](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_largehall)
- [case reverbRoomType_LargeHall2](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_largehall2)
- [case reverbRoomType_LargeRoom](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_largeroom)
- [case reverbRoomType_LargeRoom2](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_largeroom2)
- [case reverbRoomType_MediumChamber](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_mediumchamber)
- [case reverbRoomType_MediumHall](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_mediumhall)
- [case reverbRoomType_MediumHall2](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_mediumhall2)
- [case reverbRoomType_MediumHall3](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_mediumhall3)
- [case reverbRoomType_MediumRoom](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_mediumroom)
- [case reverbRoomType_Plate](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_plate)
- [case reverbRoomType_SmallRoom](/documentation/audiotoolbox/aureverbroomtype/reverbroomtype_smallroom)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/aureverbroomtype/init(rawvalue:))
- [Varispeed Unit Parameters](/documentation/audiotoolbox/1390014-varispeed_unit_parameters)

#### Constants

- [var kVarispeedParam_PlaybackCents: AudioUnitParameterID](/documentation/audiotoolbox/kvarispeedparam_playbackcents)
- [var kVarispeedParam_PlaybackRate: AudioUnitParameterID](/documentation/audiotoolbox/kvarispeedparam_playbackrate)
- [AUDelay Parameters](/documentation/audiotoolbox/1390010-audelay-parameters)

#### Constants

- [var kDelayParam_DelayTime: AudioUnitParameterID](/documentation/audiotoolbox/kdelayparam_delaytime)
- [var kDelayParam_Feedback: AudioUnitParameterID](/documentation/audiotoolbox/kdelayparam_feedback)
- [var kDelayParam_LopassCutoff: AudioUnitParameterID](/documentation/audiotoolbox/kdelayparam_lopasscutoff)
- [var kDelayParam_WetDryMix: AudioUnitParameterID](/documentation/audiotoolbox/kdelayparam_wetdrymix)
- [AUMultibandCompressor Parameters](/documentation/audiotoolbox/1389781-aumultibandcompressor-parameters)

#### Constants

- [var kMultibandCompressorParam_AttackTime: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_attacktime)
- [var kMultibandCompressorParam_CompressionAmount1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_compressionamount1)
- [var kMultibandCompressorParam_CompressionAmount2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_compressionamount2)
- [var kMultibandCompressorParam_CompressionAmount3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_compressionamount3)
- [var kMultibandCompressorParam_CompressionAmount4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_compressionamount4)
- [var kMultibandCompressorParam_Crossover1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_crossover1)
- [var kMultibandCompressorParam_Crossover2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_crossover2)
- [var kMultibandCompressorParam_Crossover3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_crossover3)
- [var kMultibandCompressorParam_EQ1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_eq1)
- [var kMultibandCompressorParam_EQ2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_eq2)
- [var kMultibandCompressorParam_EQ3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_eq3)
- [var kMultibandCompressorParam_EQ4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_eq4)
- [var kMultibandCompressorParam_Headroom1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_headroom1)
- [var kMultibandCompressorParam_Headroom2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_headroom2)
- [var kMultibandCompressorParam_Headroom3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_headroom3)
- [var kMultibandCompressorParam_Headroom4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_headroom4)
- [var kMultibandCompressorParam_InputAmplitude1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_inputamplitude1)
- [var kMultibandCompressorParam_InputAmplitude2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_inputamplitude2)
- [var kMultibandCompressorParam_InputAmplitude3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_inputamplitude3)
- [var kMultibandCompressorParam_InputAmplitude4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_inputamplitude4)
- [var kMultibandCompressorParam_OutputAmplitude1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_outputamplitude1)
- [var kMultibandCompressorParam_OutputAmplitude2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_outputamplitude2)
- [var kMultibandCompressorParam_OutputAmplitude3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_outputamplitude3)
- [var kMultibandCompressorParam_OutputAmplitude4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_outputamplitude4)
- [var kMultibandCompressorParam_Postgain: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_postgain)
- [var kMultibandCompressorParam_Pregain: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_pregain)
- [var kMultibandCompressorParam_ReleaseTime: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_releasetime)
- [var kMultibandCompressorParam_Threshold1: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_threshold1)
- [var kMultibandCompressorParam_Threshold2: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_threshold2)
- [var kMultibandCompressorParam_Threshold3: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_threshold3)
- [var kMultibandCompressorParam_Threshold4: AudioUnitParameterID](/documentation/audiotoolbox/kmultibandcompressorparam_threshold4)
- [AUDeferredRenderer Properties](/documentation/audiotoolbox/1534061-audeferredrenderer-properties)

#### Constants

- [var kAudioUnitProperty_DeferredRendererExtraLatency: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_deferredrendererextralatency)
- [var kAudioUnitProperty_DeferredRendererPullSize: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_deferredrendererpullsize)
- [var kAudioUnitProperty_DeferredRendererWaitFrames: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_deferredrendererwaitframes)
- [AUSampleDelay Parameters](/documentation/audiotoolbox/3547050-ausampledelay-parameters)

#### Constants

- [var kSampleDelayParam_DelayFrames: AudioUnitParameterID](/documentation/audiotoolbox/ksampledelayparam_delayframes)
- [AUNewTimePitch Parameters](/documentation/audiotoolbox/1389643-aunewtimepitch-parameters)

#### Constants

- [var kNewTimePitchParam_EnablePeakLocking: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_enablepeaklocking)
- [var kNewTimePitchParam_Overlap: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_overlap)
- [var kNewTimePitchParam_Pitch: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_pitch)
- [var kNewTimePitchParam_Rate: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_rate)
- [var kNewTimePitchParam_EnableSpectralCoherence: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_enablespectralcoherence)
- [var kNewTimePitchParam_EnableTransientPreservation: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_enabletransientpreservation)
- [var kNewTimePitchParam_Smoothness: AudioUnitParameterID](/documentation/audiotoolbox/knewtimepitchparam_smoothness)
- [AUTimePitch, AUTimePitch (offline), and AUPitch Unit Parameters](/documentation/audiotoolbox/1389946-autimepitch_autimepitch_offline)

#### Constants

- [var kTimePitchParam_EffectBlend: AudioUnitParameterID](/documentation/audiotoolbox/ktimepitchparam_effectblend)
- [var kTimePitchParam_Pitch: AudioUnitParameterID](/documentation/audiotoolbox/ktimepitchparam_pitch)
- [var kTimePitchParam_Rate: AudioUnitParameterID](/documentation/audiotoolbox/ktimepitchparam_rate)

### Input/Output

- [I/O Audio Unit Properties](/documentation/audiotoolbox/1534116-i_o_audio_unit_properties)

#### Properties

- [var kAudioOutputUnitProperty_ChannelMap: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_channelmap)
- [var kAudioOutputUnitProperty_CurrentDevice: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_currentdevice)
- [var kAudioOutputUnitProperty_EnableIO: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_enableio)
- [var kAudioOutputUnitProperty_HasIO: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_hasio)
- [var kAudioOutputUnitProperty_SetInputCallback: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_setinputcallback)
- [var kAudioOutputUnitProperty_StartTime: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_starttime)
- [var kAudioOutputUnitProperty_StartTimestampsAtZero: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_starttimestampsatzero)
- [var kAudioOutputUnitProperty_IsRunning: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_isrunning)
- [Inter-App Output Unit Property IDs](/documentation/audiotoolbox/1621039-inter-app-output-unit-property-ids)

#### Constants

- [var kAudioOutputUnitProperty_MIDICallbacks: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_midicallbacks)
- [var kAudioOutputUnitProperty_HostReceivesRemoteControlEvents: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_hostreceivesremotecontrolevents)
- [var kAudioOutputUnitProperty_RemoteControlToHost: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_remotecontroltohost)
- [var kAudioOutputUnitProperty_HostTransportState: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_hosttransportstate)
- [var kAudioOutputUnitProperty_NodeComponentDescription: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiooutputunitproperty_nodecomponentdescription)
- [Inter-App Audio Unit Property IDs](/documentation/audiotoolbox/1621038-inter-app-audio-unit-property-ids)

#### Constants

- [var kAudioUnitProperty_IsInterAppConnected: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_isinterappconnected)
- [var kAudioUnitProperty_PeerURL: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_peerurl)
- [var kAudioUnitProperty_RemoteControlEventListener: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_remotecontroleventlistener)
- [Output Unit Parameters](/documentation/audiotoolbox/1389916-output_unit_parameters)

#### Constants

- [var kHALOutputParam_Volume: AudioUnitParameterID](/documentation/audiotoolbox/khaloutputparam_volume)
- [AUNetReceive Properties](/documentation/audiotoolbox/1534109-aunetreceive-properties)

#### Constants

- [var kAUNetReceiveProperty_Hostname: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetreceiveproperty_hostname)
- [var kAUNetReceiveProperty_Password: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetreceiveproperty_password)
- [AUNetSend Properties](/documentation/audiotoolbox/1534207-aunetsend-properties)

#### Constants

- [var kAUNetSendProperty_Disconnect: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_disconnect)
- [var kAUNetSendProperty_Password: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_password)
- [var kAUNetSendProperty_PortNum: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_portnum)
- [var kAUNetSendProperty_ServiceName: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_servicename)
- [var kAUNetSendProperty_TransmissionFormat: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_transmissionformat)
- [var kAUNetSendProperty_TransmissionFormatIndex: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendproperty_transmissionformatindex)
- [AUNetSend Parameters](/documentation/audiotoolbox/1389633-aunetsend-parameters)

#### Constants

- [var kAUNetSendParam_NumParameters: AudioUnitParameterID](/documentation/audiotoolbox/kaunetsendparam_numparameters)
- [var kAUNetSendParam_Status: AudioUnitParameterID](/documentation/audiotoolbox/kaunetsendparam_status)
- [AUNetReceive Parameters](/documentation/audiotoolbox/1389920-aunetreceive-parameters)

#### Constants

- [var kAUNetReceiveParam_NumParameters: AudioUnitParameterID](/documentation/audiotoolbox/kaunetreceiveparam_numparameters)
- [var kAUNetReceiveParam_Status: AudioUnitParameterID](/documentation/audiotoolbox/kaunetreceiveparam_status)
- [AUNetSendPresetFormat Properties](/documentation/audiotoolbox/1534212-aunetsendpresetformat-properties)

#### Constants

- [var kAUNetSendNumPresetFormats: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendnumpresetformats)
- [var kAUNetSendPresetFormat_AAC_128kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_128kbpspc)
- [var kAUNetSendPresetFormat_AAC_32kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_32kbpspc)
- [var kAUNetSendPresetFormat_AAC_40kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_40kbpspc)
- [var kAUNetSendPresetFormat_AAC_48kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_48kbpspc)
- [var kAUNetSendPresetFormat_AAC_64kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_64kbpspc)
- [var kAUNetSendPresetFormat_AAC_80kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_80kbpspc)
- [var kAUNetSendPresetFormat_AAC_96kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_96kbpspc)
- [var kAUNetSendPresetFormat_AAC_LD_32kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_ld_32kbpspc)
- [var kAUNetSendPresetFormat_AAC_LD_40kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_ld_40kbpspc)
- [var kAUNetSendPresetFormat_AAC_LD_48kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_ld_48kbpspc)
- [var kAUNetSendPresetFormat_AAC_LD_64kbpspc: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_aac_ld_64kbpspc)
- [var kAUNetSendPresetFormat_IMA4: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_ima4)
- [var kAUNetSendPresetFormat_Lossless16: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_lossless16)
- [var kAUNetSendPresetFormat_Lossless24: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_lossless24)
- [var kAUNetSendPresetFormat_PCMFloat32: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_pcmfloat32)
- [var kAUNetSendPresetFormat_PCMInt16: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_pcmint16)
- [var kAUNetSendPresetFormat_PCMInt24: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_pcmint24)
- [var kAUNetSendPresetFormat_ULaw: AudioUnitPropertyID](/documentation/audiotoolbox/kaunetsendpresetformat_ulaw)
- [Net Status Audio Unit Parameters](/documentation/audiotoolbox/1389891-net-status-audio-unit-parameters)

#### Constants

- [var kAUNetStatus_Connected: Int](/documentation/audiotoolbox/kaunetstatus_connected)
- [var kAUNetStatus_Connecting: Int](/documentation/audiotoolbox/kaunetstatus_connecting)
- [var kAUNetStatus_Listening: Int](/documentation/audiotoolbox/kaunetstatus_listening)
- [var kAUNetStatus_NotConnected: Int](/documentation/audiotoolbox/kaunetstatus_notconnected)
- [var kAUNetStatus_Overflow: Int](/documentation/audiotoolbox/kaunetstatus_overflow)
- [var kAUNetStatus_Underflow: Int](/documentation/audiotoolbox/kaunetstatus_underflow)
- [I/O Audio Unit Function Selectors](/documentation/audiotoolbox/1585807-i_o_audio_unit_function_selector)

#### Constants

- [var kAudioOutputUnitRange: Int](/documentation/audiotoolbox/kaudiooutputunitrange)
- [var kAudioOutputUnitStartSelect: Int](/documentation/audiotoolbox/kaudiooutputunitstartselect)
- [var kAudioOutputUnitStopSelect: Int](/documentation/audiotoolbox/kaudiooutputunitstopselect)
- [AudioOutputUnitMIDICallbacks](/documentation/audiotoolbox/audiooutputunitmidicallbacks)

#### Initializers

- [init(userData: UnsafeMutableRawPointer?, MIDIEventProc: (UnsafeMutableRawPointer?, UInt32, UInt32, UInt32, UInt32) -> Void, MIDISysExProc: (UnsafeMutableRawPointer?, UnsafePointer<UInt8>, UInt32) -> Void)](/documentation/audiotoolbox/audiooutputunitmidicallbacks/init(userdata:midieventproc:midisysexproc:))

#### Instance Properties

- [var MIDIEventProc: (UnsafeMutableRawPointer?, UInt32, UInt32, UInt32, UInt32) -> Void](/documentation/audiotoolbox/audiooutputunitmidicallbacks/midieventproc)
- [var MIDISysExProc: (UnsafeMutableRawPointer?, UnsafePointer<UInt8>, UInt32) -> Void](/documentation/audiotoolbox/audiooutputunitmidicallbacks/midisysexproc)
- [var userData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/audiooutputunitmidicallbacks/userdata)
- [AudioOutputUnitStartAtTimeParams](/documentation/audiotoolbox/audiooutputunitstartattimeparams)

#### Initializers

- [init()](/documentation/audiotoolbox/audiooutputunitstartattimeparams/init())
- [init(mTimestamp: AudioTimeStamp, mFlags: UInt32)](/documentation/audiotoolbox/audiooutputunitstartattimeparams/init(mtimestamp:mflags:))

#### Instance Properties

- [var mFlags: UInt32](/documentation/audiotoolbox/audiooutputunitstartattimeparams/mflags)
- [var mTimestamp: AudioTimeStamp](/documentation/audiotoolbox/audiooutputunitstartattimeparams/mtimestamp)

### Generators

- [AURandom Parameters](/documentation/audiotoolbox/1389639-aurandom-parameters)

#### Constants

- [var kRandomParam_BoundA: AudioUnitParameterID](/documentation/audiotoolbox/krandomparam_bounda)
- [var kRandomParam_BoundB: AudioUnitParameterID](/documentation/audiotoolbox/krandomparam_boundb)
- [var kRandomParam_Curve: AudioUnitParameterID](/documentation/audiotoolbox/krandomparam_curve)
- [AUSampler Parameters](/documentation/audiotoolbox/1389769-ausampler-parameters)

#### Constants

- [var kAUSamplerParam_CoarseTuning: AudioUnitParameterID](/documentation/audiotoolbox/kausamplerparam_coarsetuning)
- [var kAUSamplerParam_FineTuning: AudioUnitParameterID](/documentation/audiotoolbox/kausamplerparam_finetuning)
- [var kAUSamplerParam_Gain: AudioUnitParameterID](/documentation/audiotoolbox/kausamplerparam_gain)
- [var kAUSamplerParam_Pan: AudioUnitParameterID](/documentation/audiotoolbox/kausamplerparam_pan)
- [AUSampler Property IDs](/documentation/audiotoolbox/1534086-ausampler-property-ids)

#### Constants

- [var kAUSampler_DefaultBankLSB: Int](/documentation/audiotoolbox/kausampler_defaultbanklsb)
- [var kAUSampler_DefaultMelodicBankMSB: Int](/documentation/audiotoolbox/kausampler_defaultmelodicbankmsb)
- [var kAUSampler_DefaultPercussionBankMSB: Int](/documentation/audiotoolbox/kausampler_defaultpercussionbankmsb)
- [AUSampler Properties](/documentation/audiotoolbox/1533959-ausampler-properties)

#### Constants

- [var kAUSamplerProperty_LoadAudioFiles: AudioUnitPropertyID](/documentation/audiotoolbox/kausamplerproperty_loadaudiofiles)
- [var kAUSamplerProperty_LoadInstrument: AudioUnitPropertyID](/documentation/audiotoolbox/kausamplerproperty_loadinstrument)
- [AURogerBeep Parameters](/documentation/audiotoolbox/1389727-aurogerbeep-parameters)

#### Constants

- [var kRogerBeepParam_InGateThreshold: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_ingatethreshold)
- [var kRogerBeepParam_InGateThresholdTime: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_ingatethresholdtime)
- [var kRogerBeepParam_OutGateThreshold: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_outgatethreshold)
- [var kRogerBeepParam_OutGateThresholdTime: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_outgatethresholdtime)
- [var kRogerBeepParam_RogerGain: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_rogergain)
- [var kRogerBeepParam_RogerType: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_rogertype)
- [var kRogerBeepParam_Sensitivity: AudioUnitParameterID](/documentation/audiotoolbox/krogerbeepparam_sensitivity)
- [AUMIDISynth Properties](/documentation/audiotoolbox/1534190-aumidisynth-properties)

#### Constants

- [var kAUMIDISynthProperty_EnablePreload: AudioUnitPropertyID](/documentation/audiotoolbox/kaumidisynthproperty_enablepreload)
- [AURoundTripAACParam Parameters](/documentation/audiotoolbox/1389808-auroundtripaacparam-parameters)

#### Constants

- [var kRoundTripAACParam_BitRate: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_bitrate)
- [var kRoundTripAACParam_CompressedFormatSampleRate: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_compressedformatsamplerate)
- [var kRoundTripAACParam_EncodingStrategy: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_encodingstrategy)
- [var kRoundTripAACParam_Format: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_format)
- [var kRoundTripAACParam_Quality: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_quality)
- [var kRoundTripAACParam_RateOrQuality: AudioUnitParameterID](/documentation/audiotoolbox/kroundtripaacparam_rateorquality)
- [Audio Unit Voice I/O](/documentation/audiotoolbox/audio-unit-voice-i-o)

### Observing muted speech

- [var kAUVoiceIOProperty_MutedSpeechActivityEventListener: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_mutedspeechactivityeventlistener)
- [AUVoiceIOMutedSpeechActivityEventListener](/documentation/audiotoolbox/auvoiceiomutedspeechactivityeventlistener)
- [AUVoiceIOSpeechActivityEvent](/documentation/audiotoolbox/auvoiceiospeechactivityevent)

#### Determining when muted speech starts and stops

- [case hasStarted](/documentation/audiotoolbox/auvoiceiospeechactivityevent/hasstarted)
- [case hasEnded](/documentation/audiotoolbox/auvoiceiospeechactivityevent/hasended)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auvoiceiospeechactivityevent/init(rawvalue:))

### Configuring voice processing

- [var kAUVoiceIOProperty_BypassVoiceProcessing: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_bypassvoiceprocessing)
- [var kAUVoiceIOProperty_VoiceProcessingEnableAGC: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_voiceprocessingenableagc)
- [var kAUVoiceIOProperty_MuteOutput: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_muteoutput)

### Configuring ducking of other audio

- [AUVoiceIOOtherAudioDuckingConfiguration](/documentation/audiotoolbox/auvoiceiootheraudioduckingconfiguration)

#### Creating an audio ducking configuration

- [AUVoiceIOOtherAudioDuckingLevel](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel)

##### Identifying the audio ducking levels

- [case `default`](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel/default)
- [case min](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel/min)
- [case mid](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel/mid)
- [case max](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel/max)

##### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auvoiceiootheraudioduckinglevel/init(rawvalue:))

#### Inspecting a configuration

- [var mEnableAdvancedDucking: DarwinBoolean](/documentation/audiotoolbox/auvoiceiootheraudioduckingconfiguration/menableadvancedducking)
- [var mDuckingLevel: AUVoiceIOOtherAudioDuckingLevel](/documentation/audiotoolbox/auvoiceiootheraudioduckingconfiguration/mduckinglevel)

#### Initializers

- [init()](/documentation/audiotoolbox/auvoiceiootheraudioduckingconfiguration/init())
- [init(mEnableAdvancedDucking: DarwinBoolean, mDuckingLevel: AUVoiceIOOtherAudioDuckingLevel)](/documentation/audiotoolbox/auvoiceiootheraudioduckingconfiguration/init(menableadvancedducking:mduckinglevel:))

### Inspecting errors

- [var kAUVoiceIOErr_UnexpectedNumberOfInputChannels: OSStatus](/documentation/audiotoolbox/kauvoiceioerr_unexpectednumberofinputchannels)

## Playback and Recording

- [Audio Queue Services](/documentation/audiotoolbox/audio-queue-services)

### Creating and Disposing of Audio Queues

- [func AudioQueueNewOutputWithDispatchQueue(UnsafeMutablePointer<AudioQueueRef?>, UnsafePointer<AudioStreamBasicDescription>, UInt32, dispatch_queue_t, AudioQueueOutputCallbackBlock) -> OSStatus](/documentation/audiotoolbox/audioqueuenewoutputwithdispatchqueue(_:_:_:_:_:))
- [func AudioQueueNewInputWithDispatchQueue(UnsafeMutablePointer<AudioQueueRef?>, UnsafePointer<AudioStreamBasicDescription>, UInt32, dispatch_queue_t, AudioQueueInputCallbackBlock) -> OSStatus](/documentation/audiotoolbox/audioqueuenewinputwithdispatchqueue(_:_:_:_:_:))
- [func AudioQueueNewOutput(UnsafePointer<AudioStreamBasicDescription>, AudioQueueOutputCallback, UnsafeMutableRawPointer?, CFRunLoop?, CFString?, UInt32, UnsafeMutablePointer<AudioQueueRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueuenewoutput(_:_:_:_:_:_:_:))
- [func AudioQueueNewInput(UnsafePointer<AudioStreamBasicDescription>, AudioQueueInputCallback, UnsafeMutableRawPointer?, CFRunLoop?, CFString?, UInt32, UnsafeMutablePointer<AudioQueueRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueuenewinput(_:_:_:_:_:_:_:))
- [func AudioQueueDispose(AudioQueueRef, Bool) -> OSStatus](/documentation/audiotoolbox/audioqueuedispose(_:_:))
- [AudioQueueRef](/documentation/audiotoolbox/audioqueueref)
- [AudioQueueInputCallbackBlock](/documentation/audiotoolbox/audioqueueinputcallbackblock)
- [AudioQueueOutputCallbackBlock](/documentation/audiotoolbox/audioqueueoutputcallbackblock)

### Controlling Audio Queues

- [func AudioQueueStart(AudioQueueRef, UnsafePointer<AudioTimeStamp>?) -> OSStatus](/documentation/audiotoolbox/audioqueuestart(_:_:))
- [func AudioQueuePrime(AudioQueueRef, UInt32, UnsafeMutablePointer<UInt32>?) -> OSStatus](/documentation/audiotoolbox/audioqueueprime(_:_:_:))
- [func AudioQueueFlush(AudioQueueRef) -> OSStatus](/documentation/audiotoolbox/audioqueueflush(_:))
- [func AudioQueueStop(AudioQueueRef, Bool) -> OSStatus](/documentation/audiotoolbox/audioqueuestop(_:_:))
- [func AudioQueuePause(AudioQueueRef) -> OSStatus](/documentation/audiotoolbox/audioqueuepause(_:))
- [func AudioQueueReset(AudioQueueRef) -> OSStatus](/documentation/audiotoolbox/audioqueuereset(_:))

### Handling Audio Queue Buffers

- [func AudioQueueAllocateBuffer(AudioQueueRef, UInt32, UnsafeMutablePointer<AudioQueueBufferRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueueallocatebuffer(_:_:_:))
- [func AudioQueueAllocateBufferWithPacketDescriptions(AudioQueueRef, UInt32, UInt32, UnsafeMutablePointer<AudioQueueBufferRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueueallocatebufferwithpacketdescriptions(_:_:_:_:))
- [func AudioQueueFreeBuffer(AudioQueueRef, AudioQueueBufferRef) -> OSStatus](/documentation/audiotoolbox/audioqueuefreebuffer(_:_:))
- [func AudioQueueEnqueueBuffer(AudioQueueRef, AudioQueueBufferRef, UInt32, UnsafePointer<AudioStreamPacketDescription>?) -> OSStatus](/documentation/audiotoolbox/audioqueueenqueuebuffer(_:_:_:_:))
- [func AudioQueueEnqueueBufferWithParameters(AudioQueueRef, AudioQueueBufferRef, UInt32, UnsafePointer<AudioStreamPacketDescription>?, UInt32, UInt32, UInt32, UnsafePointer<AudioQueueParameterEvent>?, UnsafePointer<AudioTimeStamp>?, UnsafeMutablePointer<AudioTimeStamp>?) -> OSStatus](/documentation/audiotoolbox/audioqueueenqueuebufferwithparameters(_:_:_:_:_:_:_:_:_:_:))

### Tapping the Queue’s Audio

- [func AudioQueueProcessingTapNew(AudioQueueRef, AudioQueueProcessingTapCallback, UnsafeMutableRawPointer?, AudioQueueProcessingTapFlags, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamBasicDescription>, UnsafeMutablePointer<AudioQueueProcessingTapRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueueprocessingtapnew(_:_:_:_:_:_:_:))
- [func AudioQueueProcessingTapGetQueueTime(AudioQueueProcessingTapRef, UnsafeMutablePointer<Float64>, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audioqueueprocessingtapgetqueuetime(_:_:_:))
- [func AudioQueueProcessingTapGetSourceAudio(AudioQueueProcessingTapRef, UInt32, UnsafeMutablePointer<AudioTimeStamp>, UnsafeMutablePointer<AudioQueueProcessingTapFlags>, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/audioqueueprocessingtapgetsourceaudio(_:_:_:_:_:_:))
- [func AudioQueueProcessingTapDispose(AudioQueueProcessingTapRef) -> OSStatus](/documentation/audiotoolbox/audioqueueprocessingtapdispose(_:))

### Manipulating Audio Queue Parameters

- [func AudioQueueGetParameter(AudioQueueRef, AudioQueueParameterID, UnsafeMutablePointer<AudioQueueParameterValue>) -> OSStatus](/documentation/audiotoolbox/audioqueuegetparameter(_:_:_:))
- [func AudioQueueSetParameter(AudioQueueRef, AudioQueueParameterID, AudioQueueParameterValue) -> OSStatus](/documentation/audiotoolbox/audioqueuesetparameter(_:_:_:))

### Manipulating Audio Queue Properties

- [func AudioQueueGetProperty(AudioQueueRef, AudioQueuePropertyID, UnsafeMutableRawPointer, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audioqueuegetproperty(_:_:_:_:))
- [func AudioQueueSetProperty(AudioQueueRef, AudioQueuePropertyID, UnsafeRawPointer, UInt32) -> OSStatus](/documentation/audiotoolbox/audioqueuesetproperty(_:_:_:_:))
- [func AudioQueueGetPropertySize(AudioQueueRef, AudioQueuePropertyID, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audioqueuegetpropertysize(_:_:_:))
- [func AudioQueueAddPropertyListener(AudioQueueRef, AudioQueuePropertyID, AudioQueuePropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audioqueueaddpropertylistener(_:_:_:_:))
- [func AudioQueueRemovePropertyListener(AudioQueueRef, AudioQueuePropertyID, AudioQueuePropertyListenerProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audioqueueremovepropertylistener(_:_:_:_:))

### Managing the Timeline

- [func AudioQueueCreateTimeline(AudioQueueRef, UnsafeMutablePointer<AudioQueueTimelineRef?>) -> OSStatus](/documentation/audiotoolbox/audioqueuecreatetimeline(_:_:))
- [func AudioQueueDisposeTimeline(AudioQueueRef, AudioQueueTimelineRef) -> OSStatus](/documentation/audiotoolbox/audioqueuedisposetimeline(_:_:))
- [func AudioQueueDeviceGetCurrentTime(AudioQueueRef, UnsafeMutablePointer<AudioTimeStamp>) -> OSStatus](/documentation/audiotoolbox/audioqueuedevicegetcurrenttime(_:_:))
- [func AudioQueueDeviceGetNearestStartTime(AudioQueueRef, UnsafeMutablePointer<AudioTimeStamp>, UInt32) -> OSStatus](/documentation/audiotoolbox/audioqueuedevicegetneareststarttime(_:_:_:))
- [func AudioQueueDeviceTranslateTime(AudioQueueRef, UnsafePointer<AudioTimeStamp>, UnsafeMutablePointer<AudioTimeStamp>) -> OSStatus](/documentation/audiotoolbox/audioqueuedevicetranslatetime(_:_:_:))
- [func AudioQueueGetCurrentTime(AudioQueueRef, AudioQueueTimelineRef?, UnsafeMutablePointer<AudioTimeStamp>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audioqueuegetcurrenttime(_:_:_:_:))
- [AudioQueueTimelineRef](/documentation/audiotoolbox/audioqueuetimelineref)

### Performing Offline Rendering

- [func AudioQueueSetOfflineRenderFormat(AudioQueueRef, UnsafePointer<AudioStreamBasicDescription>?, UnsafePointer<AudioChannelLayout>?) -> OSStatus](/documentation/audiotoolbox/audioqueuesetofflinerenderformat(_:_:_:))
- [func AudioQueueOfflineRender(AudioQueueRef, UnsafePointer<AudioTimeStamp>, AudioQueueBufferRef, UInt32) -> OSStatus](/documentation/audiotoolbox/audioqueueofflinerender(_:_:_:_:))

### Callbacks

- [AudioQueueInputCallback](/documentation/audiotoolbox/audioqueueinputcallback)
- [AudioQueueOutputCallback](/documentation/audiotoolbox/audioqueueoutputcallback)
- [AudioQueuePropertyListenerProc](/documentation/audiotoolbox/audioqueuepropertylistenerproc)

### Data Types

- [AudioQueueChannelAssignment](/documentation/audiotoolbox/audioqueuechannelassignment)

#### Initializers

- [init(mDeviceUID: Unmanaged<CFString>, mChannelNumber: UInt32)](/documentation/audiotoolbox/audioqueuechannelassignment/init(mdeviceuid:mchannelnumber:))

#### Instance Properties

- [var mChannelNumber: UInt32](/documentation/audiotoolbox/audioqueuechannelassignment/mchannelnumber)
- [var mDeviceUID: Unmanaged<CFString>](/documentation/audiotoolbox/audioqueuechannelassignment/mdeviceuid)
- [AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags)

#### Constants

- [static var endOfStream: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/endofstream)
- [static var postEffects: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/posteffects)
- [static var preEffects: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/preeffects)
- [static var siphon: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/siphon)
- [static var startOfStream: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/startofstream)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audioqueueprocessingtapflags/init(rawvalue:))
- [AudioQueueBuffer](/documentation/audiotoolbox/audioqueuebuffer)

#### Initializers

- [init(mAudioDataBytesCapacity: UInt32, mAudioData: UnsafeMutableRawPointer, mAudioDataByteSize: UInt32, mUserData: UnsafeMutableRawPointer?, mPacketDescriptionCapacity: UInt32, mPacketDescriptions: UnsafeMutablePointer<AudioStreamPacketDescription>?, mPacketDescriptionCount: UInt32)](/documentation/audiotoolbox/audioqueuebuffer/init(maudiodatabytescapacity:maudiodata:maudiodatabytesize:muserdata:mpacketdescriptioncapacity:mpacketdescriptions:mpacketdescriptioncount:))

#### Instance Properties

- [var mAudioData: UnsafeMutableRawPointer](/documentation/audiotoolbox/audioqueuebuffer/maudiodata)
- [var mAudioDataByteSize: UInt32](/documentation/audiotoolbox/audioqueuebuffer/maudiodatabytesize)
- [var mAudioDataBytesCapacity: UInt32](/documentation/audiotoolbox/audioqueuebuffer/maudiodatabytescapacity)
- [var mPacketDescriptionCapacity: UInt32](/documentation/audiotoolbox/audioqueuebuffer/mpacketdescriptioncapacity)
- [var mPacketDescriptionCount: UInt32](/documentation/audiotoolbox/audioqueuebuffer/mpacketdescriptioncount)
- [var mPacketDescriptions: UnsafeMutablePointer<AudioStreamPacketDescription>?](/documentation/audiotoolbox/audioqueuebuffer/mpacketdescriptions)
- [var mUserData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/audioqueuebuffer/muserdata)
- [AudioQueueBufferRef](/documentation/audiotoolbox/audioqueuebufferref)
- [AudioQueueLevelMeterState](/documentation/audiotoolbox/audioqueuelevelmeterstate)

#### Initializers

- [init()](/documentation/audiotoolbox/audioqueuelevelmeterstate/init())
- [init(mAveragePower: Float32, mPeakPower: Float32)](/documentation/audiotoolbox/audioqueuelevelmeterstate/init(maveragepower:mpeakpower:))

#### Instance Properties

- [var mAveragePower: Float32](/documentation/audiotoolbox/audioqueuelevelmeterstate/maveragepower)
- [var mPeakPower: Float32](/documentation/audiotoolbox/audioqueuelevelmeterstate/mpeakpower)
- [AudioQueueParameterEvent](/documentation/audiotoolbox/audioqueueparameterevent)

#### Initializers

- [init()](/documentation/audiotoolbox/audioqueueparameterevent/init())
- [init(mID: AudioQueueParameterID, mValue: AudioQueueParameterValue)](/documentation/audiotoolbox/audioqueueparameterevent/init(mid:mvalue:))

#### Instance Properties

- [var mID: AudioQueueParameterID](/documentation/audiotoolbox/audioqueueparameterevent/mid)
- [var mValue: AudioQueueParameterValue](/documentation/audiotoolbox/audioqueueparameterevent/mvalue)
- [AudioQueueParameterID](/documentation/audiotoolbox/audioqueueparameterid)
- [AudioQueueParameterValue](/documentation/audiotoolbox/audioqueueparametervalue)
- [AudioQueueProcessingTapCallback](/documentation/audiotoolbox/audioqueueprocessingtapcallback)
- [AudioQueueProcessingTapRef](/documentation/audiotoolbox/audioqueueprocessingtapref)

### Structures

- [AudioUnitConnection](/documentation/audiotoolbox/audiounitconnection)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitconnection/init())
- [init(sourceAudioUnit: AudioUnit?, sourceOutputNumber: UInt32, destInputNumber: UInt32)](/documentation/audiotoolbox/audiounitconnection/init(sourceaudiounit:sourceoutputnumber:destinputnumber:)-63vjd)
- [init(sourceAudioUnit: AudioUnit?, sourceOutputNumber: UInt32, destInputNumber: UInt32)](/documentation/audiotoolbox/audiounitconnection/init(sourceaudiounit:sourceoutputnumber:destinputnumber:)-6kg20)

#### Instance Properties

- [var destInputNumber: UInt32](/documentation/audiotoolbox/audiounitconnection/destinputnumber)
- [var sourceAudioUnit: AudioUnit?](/documentation/audiotoolbox/audiounitconnection/sourceaudiounit)
- [var sourceOutputNumber: UInt32](/documentation/audiotoolbox/audiounitconnection/sourceoutputnumber)
- [AudioUnitEvent](/documentation/audiotoolbox/audiounitevent)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitevent/init())
- [init(mEventType: AudioUnitEventType, mArgument: AudioUnitEvent.__Unnamed_union_mArgument)](/documentation/audiotoolbox/audiounitevent/init(meventtype:margument:))

#### Instance Properties

- [var mArgument: AudioUnitEvent.__Unnamed_union_mArgument](/documentation/audiotoolbox/audiounitevent/margument)
- [var mEventType: AudioUnitEventType](/documentation/audiotoolbox/audiounitevent/meventtype)
- [AudioUnitExternalBuffer](/documentation/audiotoolbox/audiounitexternalbuffer)

#### Initializers

- [init(buffer: UnsafeMutablePointer<UInt8>, size: UInt32)](/documentation/audiotoolbox/audiounitexternalbuffer/init(buffer:size:))

#### Instance Properties

- [var buffer: UnsafeMutablePointer<UInt8>](/documentation/audiotoolbox/audiounitexternalbuffer/buffer)
- [var size: UInt32](/documentation/audiotoolbox/audiounitexternalbuffer/size)
- [AudioUnitFrequencyResponseBin](/documentation/audiotoolbox/audiounitfrequencyresponsebin)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitfrequencyresponsebin/init())
- [init(mFrequency: Float64, mMagnitude: Float64)](/documentation/audiotoolbox/audiounitfrequencyresponsebin/init(mfrequency:mmagnitude:))

#### Instance Properties

- [var mFrequency: Float64](/documentation/audiotoolbox/audiounitfrequencyresponsebin/mfrequency)
- [var mMagnitude: Float64](/documentation/audiotoolbox/audiounitfrequencyresponsebin/mmagnitude)
- [AudioUnitMeterClipping](/documentation/audiotoolbox/audiounitmeterclipping)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitmeterclipping/init())
- [init(peakValueSinceLastCall: Float32, sawInfinity: DarwinBoolean, sawNotANumber: DarwinBoolean)](/documentation/audiotoolbox/audiounitmeterclipping/init(peakvaluesincelastcall:sawinfinity:sawnotanumber:))

#### Instance Properties

- [var peakValueSinceLastCall: Float32](/documentation/audiotoolbox/audiounitmeterclipping/peakvaluesincelastcall)
- [var sawInfinity: DarwinBoolean](/documentation/audiotoolbox/audiounitmeterclipping/sawinfinity)
- [var sawNotANumber: DarwinBoolean](/documentation/audiotoolbox/audiounitmeterclipping/sawnotanumber)
- [AudioUnitMIDIControlMapping](/documentation/audiotoolbox/audiounitmidicontrolmapping)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitmidicontrolmapping/init())
- [init(midiNRPN: UInt16, midiControl: UInt8, scope: UInt8, element: AudioUnitElement, parameter: AudioUnitParameterID)](/documentation/audiotoolbox/audiounitmidicontrolmapping/init(midinrpn:midicontrol:scope:element:parameter:))

#### Instance Properties

- [var element: AudioUnitElement](/documentation/audiotoolbox/audiounitmidicontrolmapping/element)
- [var midiControl: UInt8](/documentation/audiotoolbox/audiounitmidicontrolmapping/midicontrol)
- [var midiNRPN: UInt16](/documentation/audiotoolbox/audiounitmidicontrolmapping/midinrpn)
- [var parameter: AudioUnitParameterID](/documentation/audiotoolbox/audiounitmidicontrolmapping/parameter)
- [var scope: UInt8](/documentation/audiotoolbox/audiounitmidicontrolmapping/scope)
- [AudioUnitOtherPluginDesc](/documentation/audiotoolbox/audiounitotherplugindesc)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitotherplugindesc/init())
- [init(format: UInt32, plugin: AudioClassDescription)](/documentation/audiotoolbox/audiounitotherplugindesc/init(format:plugin:))

#### Instance Properties

- [var format: UInt32](/documentation/audiotoolbox/audiounitotherplugindesc/format)
- [var plugin: AudioClassDescription](/documentation/audiotoolbox/audiounitotherplugindesc/plugin)
- [AudioUnitParameter](/documentation/audiotoolbox/audiounitparameter)

#### Initializers

- [init(mAudioUnit: AudioUnit, mParameterID: AudioUnitParameterID, mScope: AudioUnitScope, mElement: AudioUnitElement)](/documentation/audiotoolbox/audiounitparameter/init(maudiounit:mparameterid:mscope:melement:)-2hcn6)
- [init(mAudioUnit: AudioUnit, mParameterID: AudioUnitParameterID, mScope: AudioUnitScope, mElement: AudioUnitElement)](/documentation/audiotoolbox/audiounitparameter/init(maudiounit:mparameterid:mscope:melement:)-55k5j)

#### Instance Properties

- [var mAudioUnit: AudioUnit](/documentation/audiotoolbox/audiounitparameter/maudiounit)
- [var mElement: AudioUnitElement](/documentation/audiotoolbox/audiounitparameter/melement)
- [var mParameterID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameter/mparameterid)
- [var mScope: AudioUnitScope](/documentation/audiotoolbox/audiounitparameter/mscope)
- [AudioUnitParameterEvent](/documentation/audiotoolbox/audiounitparameterevent)

#### Fields

- [var scope: AudioUnitScope](/documentation/audiotoolbox/audiounitparameterevent/scope)
- [var element: AudioUnitElement](/documentation/audiotoolbox/audiounitparameterevent/element)
- [var parameter: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameterevent/parameter)
- [var eventType: AUParameterEventType](/documentation/audiotoolbox/audiounitparameterevent/eventtype)
- [var eventValues: AudioUnitParameterEvent.__Unnamed_union_eventValues](/documentation/audiotoolbox/audiounitparameterevent/eventvalues)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparameterevent/init())
- [init(scope: AudioUnitScope, element: AudioUnitElement, parameter: AudioUnitParameterID, eventType: AUParameterEventType, eventValues: AudioUnitParameterEvent.__Unnamed_union_eventValues)](/documentation/audiotoolbox/audiounitparameterevent/init(scope:element:parameter:eventtype:eventvalues:))
- [AudioUnitParameterHistoryInfo](/documentation/audiotoolbox/audiounitparameterhistoryinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparameterhistoryinfo/init())
- [init(updatesPerSecond: Float32, historyDurationInSeconds: Float32)](/documentation/audiotoolbox/audiounitparameterhistoryinfo/init(updatespersecond:historydurationinseconds:))

#### Instance Properties

- [var historyDurationInSeconds: Float32](/documentation/audiotoolbox/audiounitparameterhistoryinfo/historydurationinseconds)
- [var updatesPerSecond: Float32](/documentation/audiotoolbox/audiounitparameterhistoryinfo/updatespersecond)
- [AudioUnitParameterNameInfo](/documentation/audiotoolbox/audiounitparameternameinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparameternameinfo/init())
- [init(inID: AudioUnitParameterID, inDesiredLength: Int32, outName: Unmanaged<CFString>?)](/documentation/audiotoolbox/audiounitparameternameinfo/init(inid:indesiredlength:outname:))

#### Instance Properties

- [var inDesiredLength: Int32](/documentation/audiotoolbox/audiounitparameternameinfo/indesiredlength)
- [var inID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameternameinfo/inid)
- [var outName: Unmanaged<CFString>?](/documentation/audiotoolbox/audiounitparameternameinfo/outname)
- [AudioUnitParameterIDName](/documentation/audiotoolbox/audiounitparameteridname)
- [AudioUnitParameterInfo](/documentation/audiotoolbox/audiounitparameterinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparameterinfo/init())
- [init(name: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar), unitName: Unmanaged<CFString>?, clumpID: UInt32, cfNameString: Unmanaged<CFString>?, unit: AudioUnitParameterUnit, minValue: AudioUnitParameterValue, maxValue: AudioUnitParameterValue, defaultValue: AudioUnitParameterValue, flags: AudioUnitParameterOptions)](/documentation/audiotoolbox/audiounitparameterinfo/init(name:unitname:clumpid:cfnamestring:unit:minvalue:maxvalue:defaultvalue:flags:))

#### Instance Properties

- [var cfNameString: Unmanaged<CFString>?](/documentation/audiotoolbox/audiounitparameterinfo/cfnamestring)
- [var clumpID: UInt32](/documentation/audiotoolbox/audiounitparameterinfo/clumpid)
- [var defaultValue: AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparameterinfo/defaultvalue)
- [var flags: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameterinfo/flags)
- [var maxValue: AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparameterinfo/maxvalue)
- [var minValue: AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparameterinfo/minvalue)
- [var name: (CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar, CChar)](/documentation/audiotoolbox/audiounitparameterinfo/name)
- [var unit: AudioUnitParameterUnit](/documentation/audiotoolbox/audiounitparameterinfo/unit)
- [var unitName: Unmanaged<CFString>?](/documentation/audiotoolbox/audiounitparameterinfo/unitname)
- [AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions)

#### Constants

- [static var flag_CFNameRelease: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_cfnamerelease)
- [static var flag_CanRamp: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_canramp)
- [static var flag_DisplayCubeRoot: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaycuberoot)
- [static var flag_DisplayCubed: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaycubed)
- [static var flag_DisplayExponential: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displayexponential)
- [static var flag_DisplayLogarithmic: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaylogarithmic)
- [static var flag_DisplayMask: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaymask)
- [static var flag_DisplaySquareRoot: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaysquareroot)
- [static var flag_DisplaySquared: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_displaysquared)
- [static var flag_ExpertMode: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_expertmode)
- [static var flag_HasCFNameString: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_hascfnamestring)
- [static var flag_HasClump: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_hasclump)
- [static var flag_IsElementMeta: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_iselementmeta)
- [static var flag_IsGlobalMeta: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_isglobalmeta)
- [static var flag_IsHighResolution: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_ishighresolution)
- [static var flag_IsReadable: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_isreadable)
- [static var flag_IsWritable: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_iswritable)
- [static var flag_MeterReadOnly: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_meterreadonly)
- [static var flag_NonRealTime: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_nonrealtime)
- [static var flag_OmitFromPresets: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_omitfrompresets)
- [static var flag_PlotHistory: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_plothistory)
- [static var flag_ValuesHaveStrings: AudioUnitParameterOptions](/documentation/audiotoolbox/audiounitparameteroptions/flag_valueshavestrings)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiounitparameteroptions/init(rawvalue:))
- [AudioUnitParameterStringFromValue](/documentation/audiotoolbox/audiounitparameterstringfromvalue)

#### Initializers

- [init(inParamID: AudioUnitParameterID, inValue: UnsafePointer<AudioUnitParameterValue>, outString: Unmanaged<CFString>?)](/documentation/audiotoolbox/audiounitparameterstringfromvalue/init(inparamid:invalue:outstring:))

#### Instance Properties

- [var inParamID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparameterstringfromvalue/inparamid)
- [var inValue: UnsafePointer<AudioUnitParameterValue>](/documentation/audiotoolbox/audiounitparameterstringfromvalue/invalue)
- [var outString: Unmanaged<CFString>?](/documentation/audiotoolbox/audiounitparameterstringfromvalue/outstring)
- [AudioUnitParameterValueFromString](/documentation/audiotoolbox/audiounitparametervaluefromstring)

#### Initializers

- [init(inParamID: AudioUnitParameterID, inString: Unmanaged<CFString>, outValue: AudioUnitParameterValue)](/documentation/audiotoolbox/audiounitparametervaluefromstring/init(inparamid:instring:outvalue:))

#### Instance Properties

- [var inParamID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparametervaluefromstring/inparamid)
- [var inString: Unmanaged<CFString>](/documentation/audiotoolbox/audiounitparametervaluefromstring/instring)
- [var outValue: AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparametervaluefromstring/outvalue)
- [AudioUnitParameterValueName](/documentation/audiotoolbox/audiounitparametervaluename)

#### Initializers

- [init(inParamID: AudioUnitParameterID, inValue: UnsafePointer<Float32>, outName: Unmanaged<CFString>)](/documentation/audiotoolbox/audiounitparametervaluename/init(inparamid:invalue:outname:))

#### Instance Properties

- [var inParamID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparametervaluename/inparamid)
- [var inValue: UnsafePointer<Float32>](/documentation/audiotoolbox/audiounitparametervaluename/invalue)
- [var outName: Unmanaged<CFString>](/documentation/audiotoolbox/audiounitparametervaluename/outname)
- [AudioUnitParameterValueTranslation](/documentation/audiotoolbox/audiounitparametervaluetranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitparametervaluetranslation/init())
- [init(otherDesc: AudioUnitOtherPluginDesc, otherParamID: UInt32, otherValue: Float32, auParamID: AudioUnitParameterID, auValue: AudioUnitParameterValue)](/documentation/audiotoolbox/audiounitparametervaluetranslation/init(otherdesc:otherparamid:othervalue:auparamid:auvalue:))

#### Instance Properties

- [var auParamID: AudioUnitParameterID](/documentation/audiotoolbox/audiounitparametervaluetranslation/auparamid)
- [var auValue: AudioUnitParameterValue](/documentation/audiotoolbox/audiounitparametervaluetranslation/auvalue)
- [var otherDesc: AudioUnitOtherPluginDesc](/documentation/audiotoolbox/audiounitparametervaluetranslation/otherdesc)
- [var otherParamID: UInt32](/documentation/audiotoolbox/audiounitparametervaluetranslation/otherparamid)
- [var otherValue: Float32](/documentation/audiotoolbox/audiounitparametervaluetranslation/othervalue)
- [AudioUnitPresetMAS_SettingData](/documentation/audiotoolbox/audiounitpresetmas_settingdata)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitpresetmas_settingdata/init())
- [init(isStockSetting: UInt32, settingID: UInt32, dataLen: UInt32, data: UInt8)](/documentation/audiotoolbox/audiounitpresetmas_settingdata/init(isstocksetting:settingid:datalen:data:))

#### Instance Properties

- [var data: UInt8](/documentation/audiotoolbox/audiounitpresetmas_settingdata/data)
- [var dataLen: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settingdata/datalen)
- [var isStockSetting: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settingdata/isstocksetting)
- [var settingID: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settingdata/settingid)
- [AudioUnitPresetMAS_Settings](/documentation/audiotoolbox/audiounitpresetmas_settings)

#### Initializers

- [init()](/documentation/audiotoolbox/audiounitpresetmas_settings/init())
- [init(manufacturerID: UInt32, effectID: UInt32, variantID: UInt32, settingsVersion: UInt32, numberOfSettings: UInt32, settings: AudioUnitPresetMAS_SettingData)](/documentation/audiotoolbox/audiounitpresetmas_settings/init(manufacturerid:effectid:variantid:settingsversion:numberofsettings:settings:))

#### Instance Properties

- [var effectID: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settings/effectid)
- [var manufacturerID: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settings/manufacturerid)
- [var numberOfSettings: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settings/numberofsettings)
- [var settings: AudioUnitPresetMAS_SettingData](/documentation/audiotoolbox/audiounitpresetmas_settings/settings)
- [var settingsVersion: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settings/settingsversion)
- [var variantID: UInt32](/documentation/audiotoolbox/audiounitpresetmas_settings/variantid)
- [AudioUnitProperty](/documentation/audiotoolbox/audiounitproperty)

#### Initializers

- [init(mAudioUnit: AudioUnit, mPropertyID: AudioUnitPropertyID, mScope: AudioUnitScope, mElement: AudioUnitElement)](/documentation/audiotoolbox/audiounitproperty/init(maudiounit:mpropertyid:mscope:melement:)-1z6rt)
- [init(mAudioUnit: AudioUnit, mPropertyID: AudioUnitPropertyID, mScope: AudioUnitScope, mElement: AudioUnitElement)](/documentation/audiotoolbox/audiounitproperty/init(maudiounit:mpropertyid:mscope:melement:)-2ay1o)

#### Instance Properties

- [var mAudioUnit: AudioUnit](/documentation/audiotoolbox/audiounitproperty/maudiounit)
- [var mElement: AudioUnitElement](/documentation/audiotoolbox/audiounitproperty/melement)
- [var mPropertyID: AudioUnitPropertyID](/documentation/audiotoolbox/audiounitproperty/mpropertyid)
- [var mScope: AudioUnitScope](/documentation/audiotoolbox/audiounitproperty/mscope)
- [AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags)

#### Constants

- [static var unitRenderAction_PreRender: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_prerender)
- [static var unitRenderAction_PostRender: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_postrender)
- [static var unitRenderAction_OutputIsSilence: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_outputissilence)
- [static var offlineUnitRenderAction_Preflight: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_preflight)
- [static var offlineUnitRenderAction_Render: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_render)
- [static var offlineUnitRenderAction_Complete: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/offlineunitrenderaction_complete)
- [static var unitRenderAction_PostRenderError: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_postrendererror)
- [static var unitRenderAction_DoNotCheckRenderArgs: AudioUnitRenderActionFlags](/documentation/audiotoolbox/audiounitrenderactionflags/unitrenderaction_donotcheckrenderargs)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiounitrenderactionflags/init(rawvalue:))
- [AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags)

#### Constants

- [static var k3DMixerRenderingFlags_ConstantReverbBlend: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_constantreverbblend)
- [static var k3DMixerRenderingFlags_DistanceAttenuation: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distanceattenuation)
- [static var k3DMixerRenderingFlags_DistanceDiffusion: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distancediffusion)
- [static var k3DMixerRenderingFlags_DistanceFilter: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_distancefilter)
- [static var k3DMixerRenderingFlags_DopplerShift: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_dopplershift)
- [static var k3DMixerRenderingFlags_InterAuralDelay: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_interauraldelay)
- [static var k3DMixerRenderingFlags_LinearDistanceAttenuation: AU3DMixerRenderingFlags](/documentation/audiotoolbox/au3dmixerrenderingflags/k3dmixerrenderingflags_lineardistanceattenuation)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/au3dmixerrenderingflags/init(rawvalue:))
- [AUChannelInfo](/documentation/audiotoolbox/auchannelinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/auchannelinfo/init())
- [init(inChannels: Int16, outChannels: Int16)](/documentation/audiotoolbox/auchannelinfo/init(inchannels:outchannels:))

#### Instance Properties

- [var inChannels: Int16](/documentation/audiotoolbox/auchannelinfo/inchannels)
- [var outChannels: Int16](/documentation/audiotoolbox/auchannelinfo/outchannels)
- [AUDependentParameter](/documentation/audiotoolbox/audependentparameter)

#### Initializers

- [init()](/documentation/audiotoolbox/audependentparameter/init())
- [init(mScope: AudioUnitScope, mParameterID: AudioUnitParameterID)](/documentation/audiotoolbox/audependentparameter/init(mscope:mparameterid:))

#### Instance Properties

- [var mParameterID: AudioUnitParameterID](/documentation/audiotoolbox/audependentparameter/mparameterid)
- [var mScope: AudioUnitScope](/documentation/audiotoolbox/audependentparameter/mscope)
- [AUDistanceAttenuationData](/documentation/audiotoolbox/audistanceattenuationdata)

#### Initializers

- [init()](/documentation/audiotoolbox/audistanceattenuationdata/init())

#### Instance Properties

- [var inNumberOfPairs: UInt32](/documentation/audiotoolbox/audistanceattenuationdata/innumberofpairs)
- [AUHostIdentifier](/documentation/audiotoolbox/auhostidentifier)

#### Initializers

- [init(hostName: Unmanaged<CFString>, hostVersion: AUNumVersion)](/documentation/audiotoolbox/auhostidentifier/init(hostname:hostversion:))

#### Instance Properties

- [var hostName: Unmanaged<CFString>](/documentation/audiotoolbox/auhostidentifier/hostname)
- [var hostVersion: AUNumVersion](/documentation/audiotoolbox/auhostidentifier/hostversion)
- [AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags)

#### Constants

- [static var changed: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/changed)
- [static var cycling: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/cycling)
- [static var moving: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/moving)
- [static var recording: AUHostTransportStateFlags](/documentation/audiotoolbox/auhosttransportstateflags/recording)

#### Initializers

- [init(rawValue: UInt)](/documentation/audiotoolbox/auhosttransportstateflags/init(rawvalue:))
- [AUHostVersionIdentifier](/documentation/audiotoolbox/auhostversionidentifier)

#### Initializers

- [init(hostName: Unmanaged<CFString>, hostVersion: UInt32)](/documentation/audiotoolbox/auhostversionidentifier/init(hostname:hostversion:))

#### Instance Properties

- [var hostName: Unmanaged<CFString>](/documentation/audiotoolbox/auhostversionidentifier/hostname)
- [var hostVersion: UInt32](/documentation/audiotoolbox/auhostversionidentifier/hostversion)
- [AUInputSamplesInOutputCallbackStruct](/documentation/audiotoolbox/auinputsamplesinoutputcallbackstruct)

#### Initializers

- [init(inputToOutputCallback: AUInputSamplesInOutputCallback, userData: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/auinputsamplesinoutputcallbackstruct/init(inputtooutputcallback:userdata:))

#### Instance Properties

- [var inputToOutputCallback: AUInputSamplesInOutputCallback](/documentation/audiotoolbox/auinputsamplesinoutputcallbackstruct/inputtooutputcallback)
- [var userData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/auinputsamplesinoutputcallbackstruct/userdata)
- [AUMIDIEvent](/documentation/audiotoolbox/aumidievent)

#### Initializers

- [init()](/documentation/audiotoolbox/aumidievent/init())
- [init(next: UnsafeMutablePointer<AURenderEvent>?, eventSampleTime: AUEventSampleTime, eventType: AURenderEventType, reserved: UInt8, length: UInt16, cable: UInt8, data: (UInt8, UInt8, UInt8))](/documentation/audiotoolbox/aumidievent/init(next:eventsampletime:eventtype:reserved:length:cable:data:))

#### Instance Properties

- [var cable: UInt8](/documentation/audiotoolbox/aumidievent/cable)
- [var data: (UInt8, UInt8, UInt8)](/documentation/audiotoolbox/aumidievent/data)
- [var eventSampleTime: AUEventSampleTime](/documentation/audiotoolbox/aumidievent/eventsampletime)
- [var eventType: AURenderEventType](/documentation/audiotoolbox/aumidievent/eventtype)
- [var length: UInt16](/documentation/audiotoolbox/aumidievent/length)
- [var next: UnsafeMutablePointer<AURenderEvent>?](/documentation/audiotoolbox/aumidievent/next)
- [var reserved: UInt8](/documentation/audiotoolbox/aumidievent/reserved)
- [AUMIDIOutputCallbackStruct](/documentation/audiotoolbox/aumidioutputcallbackstruct)

#### Initializers

- [init(midiOutputCallback: AUMIDIOutputCallback, userData: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/aumidioutputcallbackstruct/init(midioutputcallback:userdata:))

#### Instance Properties

- [var midiOutputCallback: AUMIDIOutputCallback](/documentation/audiotoolbox/aumidioutputcallbackstruct/midioutputcallback)
- [var userData: UnsafeMutableRawPointer?](/documentation/audiotoolbox/aumidioutputcallbackstruct/userdata)
- [AUNumVersion](/documentation/audiotoolbox/aunumversion)

#### Initializers

- [init()](/documentation/audiotoolbox/aunumversion/init())
- [init(nonRelRev: UInt8, stage: UInt8, minorAndBugRev: UInt8, majorRev: UInt8)](/documentation/audiotoolbox/aunumversion/init(nonrelrev:stage:minorandbugrev:majorrev:))

#### Instance Properties

- [var majorRev: UInt8](/documentation/audiotoolbox/aunumversion/majorrev)
- [var minorAndBugRev: UInt8](/documentation/audiotoolbox/aunumversion/minorandbugrev)
- [var nonRelRev: UInt8](/documentation/audiotoolbox/aunumversion/nonrelrev)
- [var stage: UInt8](/documentation/audiotoolbox/aunumversion/stage)
- [AUParameterAutomationEvent](/documentation/audiotoolbox/auparameterautomationevent)

#### Initializers

- [init()](/documentation/audiotoolbox/auparameterautomationevent/init())
- [init(hostTime: UInt64, address: AUParameterAddress, value: AUValue, eventType: AUParameterAutomationEventType, reserved: UInt64)](/documentation/audiotoolbox/auparameterautomationevent/init(hosttime:address:value:eventtype:reserved:))

#### Instance Properties

- [var address: AUParameterAddress](/documentation/audiotoolbox/auparameterautomationevent/address)
- [var eventType: AUParameterAutomationEventType](/documentation/audiotoolbox/auparameterautomationevent/eventtype)
- [var hostTime: UInt64](/documentation/audiotoolbox/auparameterautomationevent/hosttime)
- [var reserved: UInt64](/documentation/audiotoolbox/auparameterautomationevent/reserved)
- [var value: AUValue](/documentation/audiotoolbox/auparameterautomationevent/value)
- [AUParameterEvent](/documentation/audiotoolbox/auparameterevent)

#### Initializers

- [init()](/documentation/audiotoolbox/auparameterevent/init())
- [init(next: UnsafeMutablePointer<AURenderEvent>?, eventSampleTime: AUEventSampleTime, eventType: AURenderEventType, reserved: (UInt8, UInt8, UInt8), rampDurationSampleFrames: AUAudioFrameCount, parameterAddress: AUParameterAddress, value: AUValue)](/documentation/audiotoolbox/auparameterevent/init(next:eventsampletime:eventtype:reserved:rampdurationsampleframes:parameteraddress:value:))

#### Instance Properties

- [var eventSampleTime: AUEventSampleTime](/documentation/audiotoolbox/auparameterevent/eventsampletime)
- [var eventType: AURenderEventType](/documentation/audiotoolbox/auparameterevent/eventtype)
- [var next: UnsafeMutablePointer<AURenderEvent>?](/documentation/audiotoolbox/auparameterevent/next)
- [var parameterAddress: AUParameterAddress](/documentation/audiotoolbox/auparameterevent/parameteraddress)
- [var rampDurationSampleFrames: AUAudioFrameCount](/documentation/audiotoolbox/auparameterevent/rampdurationsampleframes)
- [var reserved: (UInt8, UInt8, UInt8)](/documentation/audiotoolbox/auparameterevent/reserved)
- [var value: AUValue](/documentation/audiotoolbox/auparameterevent/value)
- [AUParameterMIDIMapping](/documentation/audiotoolbox/auparametermidimapping)

#### Initializers

- [init()](/documentation/audiotoolbox/auparametermidimapping/init())
- [init(mScope: AudioUnitScope, mElement: AudioUnitElement, mParameterID: AudioUnitParameterID, mFlags: AUParameterMIDIMappingFlags, mSubRangeMin: AudioUnitParameterValue, mSubRangeMax: AudioUnitParameterValue, mStatus: UInt8, mData1: UInt8, reserved1: UInt8, reserved2: UInt8, reserved3: UInt32)](/documentation/audiotoolbox/auparametermidimapping/init(mscope:melement:mparameterid:mflags:msubrangemin:msubrangemax:mstatus:mdata1:reserved1:reserved2:reserved3:))

#### Instance Properties

- [var mData1: UInt8](/documentation/audiotoolbox/auparametermidimapping/mdata1)
- [var mElement: AudioUnitElement](/documentation/audiotoolbox/auparametermidimapping/melement)
- [var mFlags: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimapping/mflags)
- [var mParameterID: AudioUnitParameterID](/documentation/audiotoolbox/auparametermidimapping/mparameterid)
- [var mScope: AudioUnitScope](/documentation/audiotoolbox/auparametermidimapping/mscope)
- [var mStatus: UInt8](/documentation/audiotoolbox/auparametermidimapping/mstatus)
- [var mSubRangeMax: AudioUnitParameterValue](/documentation/audiotoolbox/auparametermidimapping/msubrangemax)
- [var mSubRangeMin: AudioUnitParameterValue](/documentation/audiotoolbox/auparametermidimapping/msubrangemin)
- [var reserved1: UInt8](/documentation/audiotoolbox/auparametermidimapping/reserved1)
- [var reserved2: UInt8](/documentation/audiotoolbox/auparametermidimapping/reserved2)
- [var reserved3: UInt32](/documentation/audiotoolbox/auparametermidimapping/reserved3)
- [AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags)

#### Constants

- [static var anyChannelFlag: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/anychannelflag)
- [static var anyNoteFlag: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/anynoteflag)
- [static var bipolar: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/bipolar)
- [static var bipolar_On: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/bipolar_on)
- [static var subRange: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/subrange)
- [static var toggle: AUParameterMIDIMappingFlags](/documentation/audiotoolbox/auparametermidimappingflags/toggle)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auparametermidimappingflags/init(rawvalue:))
- [AUPreset](/documentation/audiotoolbox/aupreset)

#### Initializers

- [init()](/documentation/audiotoolbox/aupreset/init())
- [init(presetNumber: Int32, presetName: Unmanaged<CFString>?)](/documentation/audiotoolbox/aupreset/init(presetnumber:presetname:))

#### Instance Properties

- [var presetName: Unmanaged<CFString>?](/documentation/audiotoolbox/aupreset/presetname)
- [var presetNumber: Int32](/documentation/audiotoolbox/aupreset/presetnumber)
- [AUPresetEvent](/documentation/audiotoolbox/aupresetevent)

#### Initializers

- [init(scope: AudioUnitScope, element: AudioUnitElement, preset: Unmanaged<CFPropertyList>)](/documentation/audiotoolbox/aupresetevent/init(scope:element:preset:))

#### Instance Properties

- [var element: AudioUnitElement](/documentation/audiotoolbox/aupresetevent/element)
- [var preset: Unmanaged<CFPropertyList>](/documentation/audiotoolbox/aupresetevent/preset)
- [var scope: AudioUnitScope](/documentation/audiotoolbox/aupresetevent/scope)
- [AURecordedParameterEvent](/documentation/audiotoolbox/aurecordedparameterevent)

#### Initializers

- [init()](/documentation/audiotoolbox/aurecordedparameterevent/init())
- [init(hostTime: UInt64, address: AUParameterAddress, value: AUValue)](/documentation/audiotoolbox/aurecordedparameterevent/init(hosttime:address:value:))

#### Instance Properties

- [var address: AUParameterAddress](/documentation/audiotoolbox/aurecordedparameterevent/address)
- [var hostTime: UInt64](/documentation/audiotoolbox/aurecordedparameterevent/hosttime)
- [var value: AUValue](/documentation/audiotoolbox/aurecordedparameterevent/value)
- [AURenderCallbackStruct](/documentation/audiotoolbox/aurendercallbackstruct)

#### Initializers

- [init()](/documentation/audiotoolbox/aurendercallbackstruct/init())
- [init(inputProc: AURenderCallback?, inputProcRefCon: UnsafeMutableRawPointer?)](/documentation/audiotoolbox/aurendercallbackstruct/init(inputproc:inputprocrefcon:))

#### Instance Properties

- [var inputProc: AURenderCallback?](/documentation/audiotoolbox/aurendercallbackstruct/inputproc)
- [var inputProcRefCon: UnsafeMutableRawPointer?](/documentation/audiotoolbox/aurendercallbackstruct/inputprocrefcon)
- [AURenderEvent](/documentation/audiotoolbox/aurenderevent)

#### Instance Properties

- [var MIDI: AUMIDIEvent](/documentation/audiotoolbox/aurenderevent/midi)
- [var head: AURenderEventHeader](/documentation/audiotoolbox/aurenderevent/head)
- [var parameter: AUParameterEvent](/documentation/audiotoolbox/aurenderevent/parameter)
- [var MIDIEventsList: AUMIDIEventList](/documentation/audiotoolbox/aurenderevent/midieventslist)

#### Initializers

- [init()](/documentation/audiotoolbox/aurenderevent/init())
- [init(MIDI: AUMIDIEvent)](/documentation/audiotoolbox/aurenderevent/init(midi:))
- [init(MIDIEventsList: AUMIDIEventList)](/documentation/audiotoolbox/aurenderevent/init(midieventslist:))
- [init(head: AURenderEventHeader)](/documentation/audiotoolbox/aurenderevent/init(head:))
- [init(parameter: AUParameterEvent)](/documentation/audiotoolbox/aurenderevent/init(parameter:))
- [AURenderEventHeader](/documentation/audiotoolbox/aurendereventheader)

#### Initializers

- [init()](/documentation/audiotoolbox/aurendereventheader/init())
- [init(next: UnsafeMutablePointer<AURenderEvent>?, eventSampleTime: AUEventSampleTime, eventType: AURenderEventType, reserved: UInt8)](/documentation/audiotoolbox/aurendereventheader/init(next:eventsampletime:eventtype:reserved:))

#### Instance Properties

- [var eventSampleTime: AUEventSampleTime](/documentation/audiotoolbox/aurendereventheader/eventsampletime)
- [var eventType: AURenderEventType](/documentation/audiotoolbox/aurendereventheader/eventtype)
- [var next: UnsafeMutablePointer<AURenderEvent>?](/documentation/audiotoolbox/aurendereventheader/next)
- [var reserved: UInt8](/documentation/audiotoolbox/aurendereventheader/reserved)
- [AUSamplerBankPresetData](/documentation/audiotoolbox/ausamplerbankpresetdata)

#### Initializers

- [init(bankURL: Unmanaged<CFURL>, bankMSB: UInt8, bankLSB: UInt8, presetID: UInt8, reserved: UInt8)](/documentation/audiotoolbox/ausamplerbankpresetdata/init(bankurl:bankmsb:banklsb:presetid:reserved:))

#### Instance Properties

- [var bankLSB: UInt8](/documentation/audiotoolbox/ausamplerbankpresetdata/banklsb)
- [var bankMSB: UInt8](/documentation/audiotoolbox/ausamplerbankpresetdata/bankmsb)
- [var bankURL: Unmanaged<CFURL>](/documentation/audiotoolbox/ausamplerbankpresetdata/bankurl)
- [var presetID: UInt8](/documentation/audiotoolbox/ausamplerbankpresetdata/presetid)
- [var reserved: UInt8](/documentation/audiotoolbox/ausamplerbankpresetdata/reserved)
- [AUSamplerInstrumentData](/documentation/audiotoolbox/ausamplerinstrumentdata)

#### Initializers

- [init(fileURL: Unmanaged<CFURL>, instrumentType: UInt8, bankMSB: UInt8, bankLSB: UInt8, presetID: UInt8)](/documentation/audiotoolbox/ausamplerinstrumentdata/init(fileurl:instrumenttype:bankmsb:banklsb:presetid:))

#### Instance Properties

- [var bankLSB: UInt8](/documentation/audiotoolbox/ausamplerinstrumentdata/banklsb)
- [var bankMSB: UInt8](/documentation/audiotoolbox/ausamplerinstrumentdata/bankmsb)
- [var fileURL: Unmanaged<CFURL>](/documentation/audiotoolbox/ausamplerinstrumentdata/fileurl)
- [var instrumentType: UInt8](/documentation/audiotoolbox/ausamplerinstrumentdata/instrumenttype)
- [var presetID: UInt8](/documentation/audiotoolbox/ausamplerinstrumentdata/presetid)
- [AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags)

#### Constants

- [static var scheduledAudioSliceFlag_BeganToRender: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_begantorender)
- [static var scheduledAudioSliceFlag_BeganToRenderLate: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_begantorenderlate)
- [static var scheduledAudioSliceFlag_Complete: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_complete)
- [static var scheduledAudioSliceFlag_Interrupt: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_interrupt)
- [static var scheduledAudioSliceFlag_InterruptAtLoop: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_interruptatloop)
- [static var scheduledAudioSliceFlag_Loop: AUScheduledAudioSliceFlags](/documentation/audiotoolbox/auscheduledaudiosliceflags/scheduledaudiosliceflag_loop)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auscheduledaudiosliceflags/init(rawvalue:))
- [AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags)

#### Constants

- [static var spatialMixerRenderingFlags_DistanceAttenuation: AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags/spatialmixerrenderingflags_distanceattenuation)
- [static var spatialMixerRenderingFlags_InterAuralDelay: AUSpatialMixerRenderingFlags](/documentation/audiotoolbox/auspatialmixerrenderingflags/spatialmixerrenderingflags_interauraldelay)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixerrenderingflags/init(rawvalue:))

### Enumerations

- [AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags)

#### Constants

- [static var endOfStream: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/endofstream)
- [static var postEffects: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/posteffects)
- [static var preEffects: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/preeffects)
- [static var siphon: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/siphon)
- [static var startOfStream: AudioQueueProcessingTapFlags](/documentation/audiotoolbox/audioqueueprocessingtapflags/startofstream)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audioqueueprocessingtapflags/init(rawvalue:))
- [Anonymous](/documentation/audiotoolbox/1552627-anonymous)

#### Constants

- [var kAudioQueueErr_BufferEmpty: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_bufferempty)
- [var kAudioQueueErr_BufferEnqueuedTwice: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_bufferenqueuedtwice)
- [var kAudioQueueErr_BufferInQueue: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_bufferinqueue)
- [var kAudioQueueErr_CannotStart: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_cannotstart)
- [var kAudioQueueErr_CodecNotFound: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_codecnotfound)
- [var kAudioQueueErr_DisposalPending: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_disposalpending)
- [var kAudioQueueErr_EnqueueDuringReset: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_enqueueduringreset)
- [var kAudioQueueErr_InvalidBuffer: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidbuffer)
- [var kAudioQueueErr_InvalidCodecAccess: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidcodecaccess)
- [var kAudioQueueErr_InvalidDevice: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invaliddevice)
- [var kAudioQueueErr_InvalidOfflineMode: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidofflinemode)
- [var kAudioQueueErr_InvalidParameter: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidparameter)
- [var kAudioQueueErr_InvalidProperty: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidproperty)
- [var kAudioQueueErr_InvalidPropertySize: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidpropertysize)
- [var kAudioQueueErr_InvalidPropertyValue: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidpropertyvalue)
- [var kAudioQueueErr_InvalidQueueType: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidqueuetype)
- [var kAudioQueueErr_InvalidRunState: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidrunstate)
- [var kAudioQueueErr_InvalidTapContext: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidtapcontext)
- [var kAudioQueueErr_InvalidTapType: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidtaptype)
- [var kAudioQueueErr_Permissions: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_permissions)
- [var kAudioQueueErr_PrimeTimedOut: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_primetimedout)
- [var kAudioQueueErr_QueueInvalidated: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_queueinvalidated)
- [var kAudioQueueErr_RecordUnderrun: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_recordunderrun)
- [var kAudioQueueErr_TooManyTaps: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_toomanytaps)
- [var kAudioQueueErr_CannotStartYet: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_cannotstartyet)
- [Audio Queue Time Pitch Algorithms](/documentation/audiotoolbox/1552630-audio-queue-time-pitch-algorithm)

#### Constants

- [var kAudioQueueTimePitchAlgorithm_Spectral: UInt32](/documentation/audiotoolbox/kaudioqueuetimepitchalgorithm_spectral)
- [var kAudioQueueTimePitchAlgorithm_TimeDomain: UInt32](/documentation/audiotoolbox/kaudioqueuetimepitchalgorithm_timedomain)
- [var kAudioQueueTimePitchAlgorithm_Varispeed: UInt32](/documentation/audiotoolbox/kaudioqueuetimepitchalgorithm_varispeed)
- [Audio Queue Property IDs](/documentation/audiotoolbox/1552629-audio-queue-property-ids)

#### Constants

- [var kAudioQueueDeviceProperty_NumberChannels: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueuedeviceproperty_numberchannels)
- [var kAudioQueueDeviceProperty_SampleRate: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueuedeviceproperty_samplerate)
- [var kAudioQueueProperty_ChannelLayout: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_channellayout)
- [var kAudioQueueProperty_ConverterError: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_convertererror)
- [var kAudioQueueProperty_CurrentDevice: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentdevice)
- [var kAudioQueueProperty_CurrentLevelMeter: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentlevelmeter)
- [var kAudioQueueProperty_CurrentLevelMeterDB: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentlevelmeterdb)
- [var kAudioQueueProperty_DecodeBufferSizeFrames: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_decodebuffersizeframes)
- [var kAudioQueueProperty_EnableLevelMetering: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_enablelevelmetering)
- [var kAudioQueueProperty_EnableTimePitch: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_enabletimepitch)
- [var kAudioQueueProperty_IsRunning: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_isrunning)
- [var kAudioQueueProperty_MagicCookie: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_magiccookie)
- [var kAudioQueueProperty_MaximumOutputPacketSize: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_maximumoutputpacketsize)
- [var kAudioQueueProperty_StreamDescription: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_streamdescription)
- [var kAudioQueueProperty_TimePitchAlgorithm: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_timepitchalgorithm)
- [var kAudioQueueProperty_TimePitchBypass: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_timepitchbypass)
- [Audio Queue Property IDs](/documentation/audiotoolbox/1618733-audio-queue-property-ids)

#### Constants

- [var kAudioQueueProperty_ChannelAssignments: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_channelassignments)
- [Audio Queue Hardware Codec Policy](/documentation/audiotoolbox/1618727-audio-queue-hardware-codec-polic)

#### Constants

- [var kAudioQueueHardwareCodecPolicy_Default: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_default)
- [var kAudioQueueHardwareCodecPolicy_PreferHardware: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_preferhardware)
- [var kAudioQueueHardwareCodecPolicy_PreferSoftware: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_prefersoftware)
- [var kAudioQueueHardwareCodecPolicy_UseHardwareOnly: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_usehardwareonly)
- [var kAudioQueueHardwareCodecPolicy_UseSoftwareOnly: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_usesoftwareonly)

### Constants

- [AudioQueuePropertyID](/documentation/audiotoolbox/audioqueuepropertyid)

#### Constants

- [var kAudioQueueProperty_IsRunning: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_isrunning)
- [var kAudioQueueDeviceProperty_SampleRate: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueuedeviceproperty_samplerate)
- [var kAudioQueueDeviceProperty_NumberChannels: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueuedeviceproperty_numberchannels)
- [var kAudioQueueProperty_CurrentDevice: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentdevice)
- [var kAudioQueueProperty_MagicCookie: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_magiccookie)
- [var kAudioQueueProperty_MaximumOutputPacketSize: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_maximumoutputpacketsize)
- [var kAudioQueueProperty_StreamDescription: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_streamdescription)
- [var kAudioQueueProperty_ChannelLayout: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_channellayout)
- [var kAudioQueueProperty_EnableLevelMetering: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_enablelevelmetering)
- [var kAudioQueueProperty_CurrentLevelMeter: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentlevelmeter)
- [var kAudioQueueProperty_CurrentLevelMeterDB: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_currentlevelmeterdb)
- [var kAudioQueueProperty_DecodeBufferSizeFrames: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_decodebuffersizeframes)
- [var kAudioQueueProperty_ConverterError: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_convertererror)
- [Audio Queue Parameters](/documentation/audiotoolbox/1552626-audio-queue-parameters)

#### Constants

- [var kAudioQueueParam_Volume: AudioQueueParameterID](/documentation/audiotoolbox/kaudioqueueparam_volume)
- [var kAudioQueueParam_PlayRate: AudioQueueParameterID](/documentation/audiotoolbox/kaudioqueueparam_playrate)
- [var kAudioQueueParam_Pitch: AudioQueueParameterID](/documentation/audiotoolbox/kaudioqueueparam_pitch)
- [var kAudioQueueParam_VolumeRampTime: AudioQueueParameterID](/documentation/audiotoolbox/kaudioqueueparam_volumeramptime)
- [var kAudioQueueParam_Pan: AudioQueueParameterID](/documentation/audiotoolbox/kaudioqueueparam_pan)
- [Hardware Codec Policy Keys](/documentation/audiotoolbox/1618724-hardware-codec-policy-keys)

#### Constants

- [var kAudioQueueProperty_HardwareCodecPolicy: AudioQueuePropertyID](/documentation/audiotoolbox/kaudioqueueproperty_hardwarecodecpolicy)
- [var kAudioQueueHardwareCodecPolicy_Default: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_default)
- [var kAudioQueueHardwareCodecPolicy_UseSoftwareOnly: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_usesoftwareonly)
- [var kAudioQueueHardwareCodecPolicy_UseHardwareOnly: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_usehardwareonly)
- [var kAudioQueueHardwareCodecPolicy_PreferSoftware: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_prefersoftware)
- [var kAudioQueueHardwareCodecPolicy_PreferHardware: UInt32](/documentation/audiotoolbox/kaudioqueuehardwarecodecpolicy_preferhardware)

### Result Codes

- [var kAudioQueueErr_InvalidBuffer: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidbuffer)
- [var kAudioQueueErr_BufferEmpty: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_bufferempty)
- [var kAudioQueueErr_DisposalPending: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_disposalpending)
- [var kAudioQueueErr_InvalidProperty: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidproperty)
- [var kAudioQueueErr_InvalidPropertySize: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidpropertysize)
- [var kAudioQueueErr_InvalidParameter: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidparameter)
- [var kAudioQueueErr_CannotStart: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_cannotstart)
- [var kAudioQueueErr_InvalidDevice: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invaliddevice)
- [var kAudioQueueErr_BufferInQueue: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_bufferinqueue)
- [var kAudioQueueErr_InvalidRunState: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidrunstate)
- [var kAudioQueueErr_InvalidQueueType: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidqueuetype)
- [var kAudioQueueErr_Permissions: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_permissions)
- [var kAudioQueueErr_InvalidPropertyValue: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidpropertyvalue)
- [var kAudioQueueErr_PrimeTimedOut: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_primetimedout)
- [var kAudioQueueErr_CodecNotFound: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_codecnotfound)
- [var kAudioQueueErr_InvalidCodecAccess: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidcodecaccess)
- [var kAudioQueueErr_QueueInvalidated: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_queueinvalidated)
- [var kAudioQueueErr_RecordUnderrun: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_recordunderrun)
- [var kAudioQueueErr_EnqueueDuringReset: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_enqueueduringreset)
- [var kAudioQueueErr_InvalidOfflineMode: OSStatus](/documentation/audiotoolbox/kaudioqueueerr_invalidofflinemode)
- [var kAudioFormatUnsupportedDataFormatError: OSStatus](/documentation/audiotoolbox/kaudioformatunsupporteddataformaterror)
- [Audio Services](/documentation/audiotoolbox/audio-services)

### Creating and Disposing of System Sound Objects

- [func AudioServicesCreateSystemSoundID(CFURL, UnsafeMutablePointer<SystemSoundID>) -> OSStatus](/documentation/audiotoolbox/audioservicescreatesystemsoundid(_:_:))
- [func AudioServicesDisposeSystemSoundID(SystemSoundID) -> OSStatus](/documentation/audiotoolbox/audioservicesdisposesystemsoundid(_:))
- [SystemSoundID](/documentation/audiotoolbox/systemsoundid)
- [System Sounds](/documentation/audiotoolbox/1405222-system-sounds)

#### Constants

- [var kSystemSoundID_FlashScreen: SystemSoundID](/documentation/audiotoolbox/ksystemsoundid_flashscreen)
- [var kSystemSoundID_UserPreferredAlert: SystemSoundID](/documentation/audiotoolbox/ksystemsoundid_userpreferredalert)
- [var kUserPreferredAlert: SystemSoundID](/documentation/audiotoolbox/kuserpreferredalert)
- [Alert Sound Identifiers](/documentation/audiotoolbox/1618202-alert-sound-identifiers)

#### Constants

- [var kSystemSoundID_Vibrate: SystemSoundID](/documentation/audiotoolbox/ksystemsoundid_vibrate)
- [var kSystemSoundID_UserPreferredAlert: SystemSoundID](/documentation/audiotoolbox/ksystemsoundid_userpreferredalert)
- [var kSystemSoundID_FlashScreen: SystemSoundID](/documentation/audiotoolbox/ksystemsoundid_flashscreen)
- [var kUserPreferredAlert: SystemSoundID](/documentation/audiotoolbox/kuserpreferredalert)

### Playing Sounds

- [func AudioServicesPlayAlertSoundWithCompletion(SystemSoundID, (() -> Void)?)](/documentation/audiotoolbox/audioservicesplayalertsoundwithcompletion(_:_:))
- [func AudioServicesPlaySystemSoundWithCompletion(SystemSoundID, (() -> Void)?)](/documentation/audiotoolbox/audioservicesplaysystemsoundwithcompletion(_:_:))
- [func AudioServicesPlayAlertSound(SystemSoundID)](/documentation/audiotoolbox/audioservicesplayalertsound(_:))
- [func AudioServicesPlaySystemSound(SystemSoundID)](/documentation/audiotoolbox/audioservicesplaysystemsound(_:))

### Adding and Removing System Sound Callbacks

- [func AudioServicesAddSystemSoundCompletion(SystemSoundID, CFRunLoop?, CFString?, AudioServicesSystemSoundCompletionProc, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audioservicesaddsystemsoundcompletion(_:_:_:_:_:))
- [func AudioServicesRemoveSystemSoundCompletion(SystemSoundID)](/documentation/audiotoolbox/audioservicesremovesystemsoundcompletion(_:))
- [AudioServicesSystemSoundCompletionProc](/documentation/audiotoolbox/audioservicessystemsoundcompletionproc)

### Managing System Sound Services Properties

- [func AudioServicesGetPropertyInfo(AudioServicesPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audioservicesgetpropertyinfo(_:_:_:_:_:))
- [func AudioServicesGetProperty(AudioServicesPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audioservicesgetproperty(_:_:_:_:_:))
- [func AudioServicesSetProperty(AudioServicesPropertyID, UInt32, UnsafeRawPointer?, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audioservicessetproperty(_:_:_:_:_:))
- [AudioServicesPropertyID](/documentation/audiotoolbox/audioservicespropertyid)
- [System Sound Services Property Identifiers](/documentation/audiotoolbox/1405268-system-sound-services-property-i)

#### Constants

- [var kAudioServicesPropertyIsUISound: AudioServicesPropertyID](/documentation/audiotoolbox/kaudioservicespropertyisuisound)
- [var kAudioServicesPropertyCompletePlaybackIfAppDies: AudioServicesPropertyID](/documentation/audiotoolbox/kaudioservicespropertycompleteplaybackifappdies)
- [Audio Hardware Services Properties](/documentation/audiotoolbox/1405208-audio-hardware-services-properti)

#### Constants

- [var kAudioHardwareServiceProperty_ServiceRestarted: AudioObjectPropertySelector](/documentation/audiotoolbox/kaudiohardwareserviceproperty_servicerestarted)
- [var kAudioHardwareServiceDeviceProperty_VirtualMainBalance: AudioObjectPropertySelector](/documentation/audiotoolbox/kaudiohardwareservicedeviceproperty_virtualmainbalance)
- [var kAudioHardwareServiceDeviceProperty_VirtualMainVolume: AudioObjectPropertySelector](/documentation/audiotoolbox/kaudiohardwareservicedeviceproperty_virtualmainvolume)

### Getting Error Codes

- [Audio Services Errors](/documentation/audiotoolbox/1405232-audio-services-errors)

#### Constants

- [var kAudioServicesBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioservicesbadpropertysizeerror)
- [var kAudioServicesBadSpecifierSizeError: OSStatus](/documentation/audiotoolbox/kaudioservicesbadspecifiersizeerror)
- [var kAudioServicesNoError: OSStatus](/documentation/audiotoolbox/kaudioservicesnoerror)
- [var kAudioServicesSystemSoundClientTimedOutError: OSStatus](/documentation/audiotoolbox/kaudioservicessystemsoundclienttimedouterror)
- [var kAudioServicesSystemSoundUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioservicessystemsoundunspecifiederror)
- [var kAudioServicesUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudioservicesunsupportedpropertyerror)
- [var kAudioServicesSystemSoundExceededMaximumDurationError: OSStatus](/documentation/audiotoolbox/kaudioservicessystemsoundexceededmaximumdurationerror)
- [var kAudioServicesNoError: OSStatus](/documentation/audiotoolbox/kaudioservicesnoerror)
- [var kAudioServicesUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudioservicesunsupportedpropertyerror)
- [var kAudioServicesBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioservicesbadpropertysizeerror)
- [var kAudioServicesBadSpecifierSizeError: OSStatus](/documentation/audiotoolbox/kaudioservicesbadspecifiersizeerror)
- [var kAudioServicesSystemSoundUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioservicessystemsoundunspecifiederror)
- [var kAudioServicesSystemSoundClientTimedOutError: OSStatus](/documentation/audiotoolbox/kaudioservicessystemsoundclienttimedouterror)
- [Music Player](/documentation/audiotoolbox/music-player)

### Managing a Music Player

- [func NewMusicPlayer(UnsafeMutablePointer<MusicPlayer?>) -> OSStatus](/documentation/audiotoolbox/newmusicplayer(_:))
- [func DisposeMusicPlayer(MusicPlayer) -> OSStatus](/documentation/audiotoolbox/disposemusicplayer(_:))
- [func MusicPlayerGetBeatsForHostTime(MusicPlayer, UInt64, UnsafeMutablePointer<MusicTimeStamp>) -> OSStatus](/documentation/audiotoolbox/musicplayergetbeatsforhosttime(_:_:_:))
- [func MusicPlayerGetHostTimeForBeats(MusicPlayer, MusicTimeStamp, UnsafeMutablePointer<UInt64>) -> OSStatus](/documentation/audiotoolbox/musicplayergethosttimeforbeats(_:_:_:))
- [func MusicPlayerGetPlayRateScalar(MusicPlayer, UnsafeMutablePointer<Float64>) -> OSStatus](/documentation/audiotoolbox/musicplayergetplayratescalar(_:_:))
- [func MusicPlayerGetSequence(MusicPlayer, UnsafeMutablePointer<MusicSequence?>) -> OSStatus](/documentation/audiotoolbox/musicplayergetsequence(_:_:))
- [func MusicPlayerGetTime(MusicPlayer, UnsafeMutablePointer<MusicTimeStamp>) -> OSStatus](/documentation/audiotoolbox/musicplayergettime(_:_:))
- [func MusicPlayerIsPlaying(MusicPlayer, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/musicplayerisplaying(_:_:))
- [func MusicPlayerPreroll(MusicPlayer) -> OSStatus](/documentation/audiotoolbox/musicplayerpreroll(_:))
- [func MusicPlayerSetPlayRateScalar(MusicPlayer, Float64) -> OSStatus](/documentation/audiotoolbox/musicplayersetplayratescalar(_:_:))
- [func MusicPlayerSetSequence(MusicPlayer, MusicSequence?) -> OSStatus](/documentation/audiotoolbox/musicplayersetsequence(_:_:))
- [func MusicPlayerSetTime(MusicPlayer, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musicplayersettime(_:_:))
- [func MusicPlayerStart(MusicPlayer) -> OSStatus](/documentation/audiotoolbox/musicplayerstart(_:))
- [func MusicPlayerStop(MusicPlayer) -> OSStatus](/documentation/audiotoolbox/musicplayerstop(_:))
- [MusicPlayer](/documentation/audiotoolbox/musicplayer)
- [MusicTimeStamp](/documentation/audiotoolbox/musictimestamp)
- [var kMusicTimeStamp_EndOfTrack: Double](/documentation/audiotoolbox/kmusictimestamp_endoftrack)

### Iterating Over Music Events

- [func NewMusicEventIterator(MusicTrack, UnsafeMutablePointer<MusicEventIterator?>) -> OSStatus](/documentation/audiotoolbox/newmusiceventiterator(_:_:))
- [func DisposeMusicEventIterator(MusicEventIterator) -> OSStatus](/documentation/audiotoolbox/disposemusiceventiterator(_:))
- [func MusicEventIteratorNextEvent(MusicEventIterator) -> OSStatus](/documentation/audiotoolbox/musiceventiteratornextevent(_:))
- [func MusicEventIteratorSeek(MusicEventIterator, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorseek(_:_:))
- [func MusicEventIteratorDeleteEvent(MusicEventIterator) -> OSStatus](/documentation/audiotoolbox/musiceventiteratordeleteevent(_:))
- [func MusicEventIteratorGetEventInfo(MusicEventIterator, UnsafeMutablePointer<MusicTimeStamp>, UnsafeMutablePointer<MusicEventType>, UnsafeMutablePointer<UnsafeRawPointer?>, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorgeteventinfo(_:_:_:_:_:))
- [func MusicEventIteratorHasCurrentEvent(MusicEventIterator, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorhascurrentevent(_:_:))
- [func MusicEventIteratorHasNextEvent(MusicEventIterator, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorhasnextevent(_:_:))
- [func MusicEventIteratorHasPreviousEvent(MusicEventIterator, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorhaspreviousevent(_:_:))
- [func MusicEventIteratorPreviousEvent(MusicEventIterator) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorpreviousevent(_:))
- [func MusicEventIteratorSetEventInfo(MusicEventIterator, MusicEventType, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorseteventinfo(_:_:_:))
- [func MusicEventIteratorSetEventTime(MusicEventIterator, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musiceventiteratorseteventtime(_:_:))
- [MusicEventIterator](/documentation/audiotoolbox/musiceventiterator)
- [MusicEventType](/documentation/audiotoolbox/musiceventtype)

#### Constants

- [var kMusicEventType_NULL: UInt32](/documentation/audiotoolbox/kmusiceventtype_null)
- [var kMusicEventType_ExtendedNote: UInt32](/documentation/audiotoolbox/kmusiceventtype_extendednote)
- [var kMusicEventType_ExtendedTempo: UInt32](/documentation/audiotoolbox/kmusiceventtype_extendedtempo)
- [var kMusicEventType_User: UInt32](/documentation/audiotoolbox/kmusiceventtype_user)
- [var kMusicEventType_Meta: UInt32](/documentation/audiotoolbox/kmusiceventtype_meta)
- [var kMusicEventType_MIDINoteMessage: UInt32](/documentation/audiotoolbox/kmusiceventtype_midinotemessage)
- [var kMusicEventType_MIDIChannelMessage: UInt32](/documentation/audiotoolbox/kmusiceventtype_midichannelmessage)
- [var kMusicEventType_MIDIRawData: UInt32](/documentation/audiotoolbox/kmusiceventtype_midirawdata)
- [var kMusicEventType_Parameter: UInt32](/documentation/audiotoolbox/kmusiceventtype_parameter)
- [var kMusicEventType_AUPreset: UInt32](/documentation/audiotoolbox/kmusiceventtype_aupreset)
- [ExtendedNoteOnEvent](/documentation/audiotoolbox/extendednoteonevent)

#### Initializers

- [init()](/documentation/audiotoolbox/extendednoteonevent/init())
- [init(instrumentID: MusicDeviceInstrumentID, groupID: MusicDeviceGroupID, duration: Float32, extendedParams: MusicDeviceNoteParams)](/documentation/audiotoolbox/extendednoteonevent/init(instrumentid:groupid:duration:extendedparams:))

#### Instance Properties

- [var duration: Float32](/documentation/audiotoolbox/extendednoteonevent/duration)
- [var extendedParams: MusicDeviceNoteParams](/documentation/audiotoolbox/extendednoteonevent/extendedparams)
- [var groupID: MusicDeviceGroupID](/documentation/audiotoolbox/extendednoteonevent/groupid)
- [var instrumentID: MusicDeviceInstrumentID](/documentation/audiotoolbox/extendednoteonevent/instrumentid)
- [ExtendedTempoEvent](/documentation/audiotoolbox/extendedtempoevent)

#### Initializers

- [init()](/documentation/audiotoolbox/extendedtempoevent/init())
- [init(bpm: Float64)](/documentation/audiotoolbox/extendedtempoevent/init(bpm:))

#### Instance Properties

- [var bpm: Float64](/documentation/audiotoolbox/extendedtempoevent/bpm)
- [MusicEventUserData](/documentation/audiotoolbox/musiceventuserdata)

#### Initializers

- [init()](/documentation/audiotoolbox/musiceventuserdata/init())
- [init(length: UInt32, data: UInt8)](/documentation/audiotoolbox/musiceventuserdata/init(length:data:))

#### Instance Properties

- [var data: UInt8](/documentation/audiotoolbox/musiceventuserdata/data)
- [var length: UInt32](/documentation/audiotoolbox/musiceventuserdata/length)
- [ParameterEvent](/documentation/audiotoolbox/parameterevent)

#### Properties

- [var element: AudioUnitElement](/documentation/audiotoolbox/parameterevent/element)
- [var parameterID: AudioUnitParameterID](/documentation/audiotoolbox/parameterevent/parameterid)
- [var scope: AudioUnitScope](/documentation/audiotoolbox/parameterevent/scope)
- [var value: AudioUnitParameterValue](/documentation/audiotoolbox/parameterevent/value)

#### Initializers

- [init()](/documentation/audiotoolbox/parameterevent/init())
- [init(parameterID: AudioUnitParameterID, scope: AudioUnitScope, element: AudioUnitElement, value: AudioUnitParameterValue)](/documentation/audiotoolbox/parameterevent/init(parameterid:scope:element:value:))
- [MusicDeviceNoteParams](/documentation/audiotoolbox/musicdevicenoteparams)

#### Initializers

- [init()](/documentation/audiotoolbox/musicdevicenoteparams/init())
- [init(argCount: UInt32, mPitch: Float32, mVelocity: Float32, mControls: NoteParamsControlValue)](/documentation/audiotoolbox/musicdevicenoteparams/init(argcount:mpitch:mvelocity:mcontrols:))

#### Instance Properties

- [var argCount: UInt32](/documentation/audiotoolbox/musicdevicenoteparams/argcount)
- [var mControls: NoteParamsControlValue](/documentation/audiotoolbox/musicdevicenoteparams/mcontrols)
- [var mPitch: Float32](/documentation/audiotoolbox/musicdevicenoteparams/mpitch)
- [var mVelocity: Float32](/documentation/audiotoolbox/musicdevicenoteparams/mvelocity)
- [MusicDeviceStdNoteParams](/documentation/audiotoolbox/musicdevicestdnoteparams)

#### Initializers

- [init()](/documentation/audiotoolbox/musicdevicestdnoteparams/init())
- [init(argCount: UInt32, mPitch: Float32, mVelocity: Float32)](/documentation/audiotoolbox/musicdevicestdnoteparams/init(argcount:mpitch:mvelocity:))

#### Instance Properties

- [var argCount: UInt32](/documentation/audiotoolbox/musicdevicestdnoteparams/argcount)
- [var mPitch: Float32](/documentation/audiotoolbox/musicdevicestdnoteparams/mpitch)
- [var mVelocity: Float32](/documentation/audiotoolbox/musicdevicestdnoteparams/mvelocity)
- [NoteParamsControlValue](/documentation/audiotoolbox/noteparamscontrolvalue)

#### Initializers

- [init()](/documentation/audiotoolbox/noteparamscontrolvalue/init())
- [init(mID: AudioUnitParameterID, mValue: AudioUnitParameterValue)](/documentation/audiotoolbox/noteparamscontrolvalue/init(mid:mvalue:))

#### Instance Properties

- [var mID: AudioUnitParameterID](/documentation/audiotoolbox/noteparamscontrolvalue/mid)
- [var mValue: AudioUnitParameterValue](/documentation/audiotoolbox/noteparamscontrolvalue/mvalue)

### Managing Music Sequences

- [func NewMusicSequence(UnsafeMutablePointer<MusicSequence?>) -> OSStatus](/documentation/audiotoolbox/newmusicsequence(_:))
- [func DisposeMusicSequence(MusicSequence) -> OSStatus](/documentation/audiotoolbox/disposemusicsequence(_:))
- [func MusicSequenceBarBeatTimeToBeats(MusicSequence, UnsafePointer<CABarBeatTime>, UnsafeMutablePointer<MusicTimeStamp>) -> OSStatus](/documentation/audiotoolbox/musicsequencebarbeattimetobeats(_:_:_:))
- [func MusicSequenceBeatsToBarBeatTime(MusicSequence, MusicTimeStamp, UInt32, UnsafeMutablePointer<CABarBeatTime>) -> OSStatus](/documentation/audiotoolbox/musicsequencebeatstobarbeattime(_:_:_:_:))
- [func MusicSequenceDisposeTrack(MusicSequence, MusicTrack) -> OSStatus](/documentation/audiotoolbox/musicsequencedisposetrack(_:_:))
- [func MusicSequenceFileCreate(MusicSequence, CFURL, MusicSequenceFileTypeID, MusicSequenceFileFlags, Int16) -> OSStatus](/documentation/audiotoolbox/musicsequencefilecreate(_:_:_:_:_:))
- [func MusicSequenceFileCreateData(MusicSequence, MusicSequenceFileTypeID, MusicSequenceFileFlags, Int16, UnsafeMutablePointer<Unmanaged<CFData>?>) -> OSStatus](/documentation/audiotoolbox/musicsequencefilecreatedata(_:_:_:_:_:))
- [func MusicSequenceFileLoad(MusicSequence, CFURL, MusicSequenceFileTypeID, MusicSequenceLoadFlags) -> OSStatus](/documentation/audiotoolbox/musicsequencefileload(_:_:_:_:))
- [func MusicSequenceFileLoadData(MusicSequence, CFData, MusicSequenceFileTypeID, MusicSequenceLoadFlags) -> OSStatus](/documentation/audiotoolbox/musicsequencefileloaddata(_:_:_:_:))
- [func MusicSequenceGetAUGraph(MusicSequence, UnsafeMutablePointer<AUGraph?>) -> OSStatus](/documentation/audiotoolbox/musicsequencegetaugraph(_:_:))
- [func MusicSequenceGetBeatsForSeconds(MusicSequence, Float64, UnsafeMutablePointer<MusicTimeStamp>) -> OSStatus](/documentation/audiotoolbox/musicsequencegetbeatsforseconds(_:_:_:))
- [func MusicSequenceGetIndTrack(MusicSequence, UInt32, UnsafeMutablePointer<MusicTrack?>) -> OSStatus](/documentation/audiotoolbox/musicsequencegetindtrack(_:_:_:))
- [func MusicSequenceGetInfoDictionary(MusicSequence) -> CFDictionary](/documentation/audiotoolbox/musicsequencegetinfodictionary(_:))
- [func MusicSequenceGetSMPTEResolution(Int16, UnsafeMutablePointer<Int8>, UnsafeMutablePointer<UInt8>)](/documentation/audiotoolbox/musicsequencegetsmpteresolution(_:_:_:))
- [func MusicSequenceGetSecondsForBeats(MusicSequence, MusicTimeStamp, UnsafeMutablePointer<Float64>) -> OSStatus](/documentation/audiotoolbox/musicsequencegetsecondsforbeats(_:_:_:))
- [func MusicSequenceGetSequenceType(MusicSequence, UnsafeMutablePointer<MusicSequenceType>) -> OSStatus](/documentation/audiotoolbox/musicsequencegetsequencetype(_:_:))
- [func MusicSequenceGetTempoTrack(MusicSequence, UnsafeMutablePointer<MusicTrack?>) -> OSStatus](/documentation/audiotoolbox/musicsequencegettempotrack(_:_:))
- [func MusicSequenceGetTrackCount(MusicSequence, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/musicsequencegettrackcount(_:_:))
- [func MusicSequenceGetTrackIndex(MusicSequence, MusicTrack, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/musicsequencegettrackindex(_:_:_:))
- [func MusicSequenceNewTrack(MusicSequence, UnsafeMutablePointer<MusicTrack?>) -> OSStatus](/documentation/audiotoolbox/musicsequencenewtrack(_:_:))
- [func MusicSequenceReverse(MusicSequence) -> OSStatus](/documentation/audiotoolbox/musicsequencereverse(_:))
- [func MusicSequenceSetAUGraph(MusicSequence, AUGraph?) -> OSStatus](/documentation/audiotoolbox/musicsequencesetaugraph(_:_:))
- [func MusicSequenceSetMIDIEndpoint(MusicSequence, MIDIEndpointRef) -> OSStatus](/documentation/audiotoolbox/musicsequencesetmidiendpoint(_:_:))
- [func MusicSequenceSetSMPTEResolution(Int8, UInt8) -> Int16](/documentation/audiotoolbox/musicsequencesetsmpteresolution(_:_:))
- [func MusicSequenceSetSequenceType(MusicSequence, MusicSequenceType) -> OSStatus](/documentation/audiotoolbox/musicsequencesetsequencetype(_:_:))
- [func MusicSequenceSetUserCallback(MusicSequence, MusicSequenceUserCallback?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/musicsequencesetusercallback(_:_:_:))
- [MusicSequence](/documentation/audiotoolbox/musicsequence)
- [MusicSequenceUserCallback](/documentation/audiotoolbox/musicsequenceusercallback)
- [MusicSequenceFileFlags](/documentation/audiotoolbox/musicsequencefileflags)

#### Constants

- [static var eraseFile: MusicSequenceFileFlags](/documentation/audiotoolbox/musicsequencefileflags/erasefile)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/musicsequencefileflags/init(rawvalue:))
- [MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags)

#### Constants

- [static var smf_ChannelsToTracks: MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags/smf_channelstotracks)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/musicsequenceloadflags/init(rawvalue:))

#### Type Properties

- [static var smf_PreserveTracks: MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags/smf_preservetracks)

### Managing Music Tracks

- [func MusicTrackClear(MusicTrack, MusicTimeStamp, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musictrackclear(_:_:_:))
- [func MusicTrackCopyInsert(MusicTrack, MusicTimeStamp, MusicTimeStamp, MusicTrack, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musictrackcopyinsert(_:_:_:_:_:))
- [func MusicTrackCut(MusicTrack, MusicTimeStamp, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musictrackcut(_:_:_:))
- [func MusicTrackGetDestMIDIEndpoint(MusicTrack, UnsafeMutablePointer<MIDIEndpointRef>) -> OSStatus](/documentation/audiotoolbox/musictrackgetdestmidiendpoint(_:_:))
- [func MusicTrackGetDestNode(MusicTrack, UnsafeMutablePointer<AUNode>) -> OSStatus](/documentation/audiotoolbox/musictrackgetdestnode(_:_:))
- [func MusicTrackGetProperty(MusicTrack, UInt32, UnsafeMutableRawPointer, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/musictrackgetproperty(_:_:_:_:))
- [func MusicTrackGetSequence(MusicTrack, UnsafeMutablePointer<MusicSequence?>) -> OSStatus](/documentation/audiotoolbox/musictrackgetsequence(_:_:))
- [func MusicTrackMerge(MusicTrack, MusicTimeStamp, MusicTimeStamp, MusicTrack, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musictrackmerge(_:_:_:_:_:))
- [func MusicTrackMoveEvents(MusicTrack, MusicTimeStamp, MusicTimeStamp, MusicTimeStamp) -> OSStatus](/documentation/audiotoolbox/musictrackmoveevents(_:_:_:_:))
- [func MusicTrackNewAUPresetEvent(MusicTrack, MusicTimeStamp, UnsafePointer<AUPresetEvent>) -> OSStatus](/documentation/audiotoolbox/musictracknewaupresetevent(_:_:_:))
- [func MusicTrackNewExtendedNoteEvent(MusicTrack, MusicTimeStamp, UnsafePointer<ExtendedNoteOnEvent>) -> OSStatus](/documentation/audiotoolbox/musictracknewextendednoteevent(_:_:_:))
- [func MusicTrackNewExtendedTempoEvent(MusicTrack, MusicTimeStamp, Float64) -> OSStatus](/documentation/audiotoolbox/musictracknewextendedtempoevent(_:_:_:))
- [func MusicTrackNewMIDIChannelEvent(MusicTrack, MusicTimeStamp, UnsafePointer<MIDIChannelMessage>) -> OSStatus](/documentation/audiotoolbox/musictracknewmidichannelevent(_:_:_:))
- [func MusicTrackNewMIDINoteEvent(MusicTrack, MusicTimeStamp, UnsafePointer<MIDINoteMessage>) -> OSStatus](/documentation/audiotoolbox/musictracknewmidinoteevent(_:_:_:))
- [func MusicTrackNewMIDIRawDataEvent(MusicTrack, MusicTimeStamp, UnsafePointer<MIDIRawData>) -> OSStatus](/documentation/audiotoolbox/musictracknewmidirawdataevent(_:_:_:))
- [func MusicTrackNewMetaEvent(MusicTrack, MusicTimeStamp, UnsafePointer<MIDIMetaEvent>) -> OSStatus](/documentation/audiotoolbox/musictracknewmetaevent(_:_:_:))
- [func MusicTrackNewParameterEvent(MusicTrack, MusicTimeStamp, UnsafePointer<ParameterEvent>) -> OSStatus](/documentation/audiotoolbox/musictracknewparameterevent(_:_:_:))
- [func MusicTrackNewUserEvent(MusicTrack, MusicTimeStamp, UnsafePointer<MusicEventUserData>) -> OSStatus](/documentation/audiotoolbox/musictracknewuserevent(_:_:_:))
- [func MusicTrackSetDestMIDIEndpoint(MusicTrack, MIDIEndpointRef) -> OSStatus](/documentation/audiotoolbox/musictracksetdestmidiendpoint(_:_:))
- [func MusicTrackSetDestNode(MusicTrack, AUNode) -> OSStatus](/documentation/audiotoolbox/musictracksetdestnode(_:_:))
- [func MusicTrackSetProperty(MusicTrack, UInt32, UnsafeMutableRawPointer, UInt32) -> OSStatus](/documentation/audiotoolbox/musictracksetproperty(_:_:_:_:))
- [MusicTrack](/documentation/audiotoolbox/musictrack)
- [MusicTrackLoopInfo](/documentation/audiotoolbox/musictrackloopinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/musictrackloopinfo/init())
- [init(loopDuration: MusicTimeStamp, numberOfLoops: Int32)](/documentation/audiotoolbox/musictrackloopinfo/init(loopduration:numberofloops:))

#### Instance Properties

- [var loopDuration: MusicTimeStamp](/documentation/audiotoolbox/musictrackloopinfo/loopduration)
- [var numberOfLoops: Int32](/documentation/audiotoolbox/musictrackloopinfo/numberofloops)
- [MIDIChannelMessage](/documentation/audiotoolbox/midichannelmessage)

#### Initializers

- [init()](/documentation/audiotoolbox/midichannelmessage/init())
- [init(status: UInt8, data1: UInt8, data2: UInt8, reserved: UInt8)](/documentation/audiotoolbox/midichannelmessage/init(status:data1:data2:reserved:))

#### Instance Properties

- [var data1: UInt8](/documentation/audiotoolbox/midichannelmessage/data1)
- [var data2: UInt8](/documentation/audiotoolbox/midichannelmessage/data2)
- [var reserved: UInt8](/documentation/audiotoolbox/midichannelmessage/reserved)
- [var status: UInt8](/documentation/audiotoolbox/midichannelmessage/status)
- [MIDIMetaEvent](/documentation/audiotoolbox/midimetaevent)

#### Initializers

- [init()](/documentation/audiotoolbox/midimetaevent/init())
- [init(metaEventType: UInt8, unused1: UInt8, unused2: UInt8, unused3: UInt8, dataLength: UInt32, data: UInt8)](/documentation/audiotoolbox/midimetaevent/init(metaeventtype:unused1:unused2:unused3:datalength:data:))

#### Instance Properties

- [var data: UInt8](/documentation/audiotoolbox/midimetaevent/data)
- [var dataLength: UInt32](/documentation/audiotoolbox/midimetaevent/datalength)
- [var metaEventType: UInt8](/documentation/audiotoolbox/midimetaevent/metaeventtype)
- [var unused1: UInt8](/documentation/audiotoolbox/midimetaevent/unused1)
- [var unused2: UInt8](/documentation/audiotoolbox/midimetaevent/unused2)
- [var unused3: UInt8](/documentation/audiotoolbox/midimetaevent/unused3)
- [MIDINoteMessage](/documentation/audiotoolbox/midinotemessage)

#### Initializers

- [init()](/documentation/audiotoolbox/midinotemessage/init())
- [init(channel: UInt8, note: UInt8, velocity: UInt8, releaseVelocity: UInt8, duration: Float32)](/documentation/audiotoolbox/midinotemessage/init(channel:note:velocity:releasevelocity:duration:))

#### Instance Properties

- [var channel: UInt8](/documentation/audiotoolbox/midinotemessage/channel)
- [var duration: Float32](/documentation/audiotoolbox/midinotemessage/duration)
- [var note: UInt8](/documentation/audiotoolbox/midinotemessage/note)
- [var releaseVelocity: UInt8](/documentation/audiotoolbox/midinotemessage/releasevelocity)
- [var velocity: UInt8](/documentation/audiotoolbox/midinotemessage/velocity)
- [MIDIRawData](/documentation/audiotoolbox/midirawdata)

#### Initializers

- [init()](/documentation/audiotoolbox/midirawdata/init())
- [init(length: UInt32, data: UInt8)](/documentation/audiotoolbox/midirawdata/init(length:data:))

#### Instance Properties

- [var data: UInt8](/documentation/audiotoolbox/midirawdata/data)
- [var length: UInt32](/documentation/audiotoolbox/midirawdata/length)

### Interacting with Music Devices

- [func MusicDeviceMIDIEvent(MusicDeviceComponent, UInt32, UInt32, UInt32, UInt32) -> OSStatus](/documentation/audiotoolbox/musicdevicemidievent(_:_:_:_:_:))
- [func MusicDeviceMIDIEventList(MusicDeviceComponent, UInt32, UnsafePointer<MIDIEventList>) -> OSStatus](/documentation/audiotoolbox/musicdevicemidieventlist(_:_:_:))
- [func MusicDeviceStartNote(MusicDeviceComponent, MusicDeviceInstrumentID, MusicDeviceGroupID, UnsafeMutablePointer<NoteInstanceID>, UInt32, UnsafePointer<MusicDeviceNoteParams>) -> OSStatus](/documentation/audiotoolbox/musicdevicestartnote(_:_:_:_:_:_:))
- [func MusicDeviceStopNote(MusicDeviceComponent, MusicDeviceGroupID, NoteInstanceID, UInt32) -> OSStatus](/documentation/audiotoolbox/musicdevicestopnote(_:_:_:_:))
- [func MusicDeviceSysEx(MusicDeviceComponent, UnsafePointer<UInt8>, UInt32) -> OSStatus](/documentation/audiotoolbox/musicdevicesysex(_:_:_:))
- [MusicDeviceComponent](/documentation/audiotoolbox/musicdevicecomponent)
- [MusicDeviceGroupID](/documentation/audiotoolbox/musicdevicegroupid)
- [MusicDeviceInstrumentID](/documentation/audiotoolbox/musicdeviceinstrumentid)
- [MusicDeviceMIDIEventProc](/documentation/audiotoolbox/musicdevicemidieventproc)
- [MusicDeviceStartNoteProc](/documentation/audiotoolbox/musicdevicestartnoteproc)
- [MusicDeviceStopNoteProc](/documentation/audiotoolbox/musicdevicestopnoteproc)
- [MusicDeviceSysExProc](/documentation/audiotoolbox/musicdevicesysexproc)

### Enumerations

- [Music Instrument Audio Unit Subtypes](/documentation/audiotoolbox/1619498-music-instrument-audio-unit-subt)

#### Constants

- [var kAudioUnitSubType_DLSSynth: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_dlssynth)
- [var kAudioUnitSubType_MIDISynth: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_midisynth-3su2x)
- [var kAudioUnitSubType_MIDISynth: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_midisynth-7sqwb)
- [var kAudioUnitSubType_Sampler: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_sampler-9nhfl)
- [var kAudioUnitSubType_Sampler: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_sampler-1sys8)
- [Music Track Properties](/documentation/audiotoolbox/1515456-music-track-properties)

#### Constants

- [var kSequenceTrackProperty_LoopInfo: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_loopinfo)
- [var kSequenceTrackProperty_OffsetTime: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_offsettime)
- [var kSequenceTrackProperty_MuteStatus: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_mutestatus)
- [var kSequenceTrackProperty_SoloStatus: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_solostatus)
- [var kSequenceTrackProperty_AutomatedParameters: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_automatedparameters)
- [var kSequenceTrackProperty_TrackLength: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_tracklength)
- [var kSequenceTrackProperty_TimeResolution: UInt32](/documentation/audiotoolbox/ksequencetrackproperty_timeresolution)
- [MusicSequenceFileFlags](/documentation/audiotoolbox/musicsequencefileflags)

#### Constants

- [static var eraseFile: MusicSequenceFileFlags](/documentation/audiotoolbox/musicsequencefileflags/erasefile)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/musicsequencefileflags/init(rawvalue:))
- [MusicSequenceFileTypeID](/documentation/audiotoolbox/musicsequencefiletypeid)

#### Constants

- [case midiType](/documentation/audiotoolbox/musicsequencefiletypeid/miditype)
- [case iMelodyType](/documentation/audiotoolbox/musicsequencefiletypeid/imelodytype)

#### Enumeration Cases

- [case anyType](/documentation/audiotoolbox/musicsequencefiletypeid/anytype)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/musicsequencefiletypeid/init(rawvalue:))
- [MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags)

#### Constants

- [static var smf_ChannelsToTracks: MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags/smf_channelstotracks)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/musicsequenceloadflags/init(rawvalue:))

#### Type Properties

- [static var smf_PreserveTracks: MusicSequenceLoadFlags](/documentation/audiotoolbox/musicsequenceloadflags/smf_preservetracks)
- [MusicSequenceType](/documentation/audiotoolbox/musicsequencetype)

#### Constants

- [case beats](/documentation/audiotoolbox/musicsequencetype/beats)
- [case seconds](/documentation/audiotoolbox/musicsequencetype/seconds)
- [case samples](/documentation/audiotoolbox/musicsequencetype/samples)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/musicsequencetype/init(rawvalue:))
- [Music Extended Control Event Type](/documentation/audiotoolbox/1515446-music-extended-control-event-typ)

#### Constants

- [var kMusicEventType_ExtendedControl: Int](/documentation/audiotoolbox/kmusiceventtype_extendedcontrol)
- [Music Player Errors](/documentation/audiotoolbox/1515472-music-player-errors)

#### Constants

- [var kAudioToolboxErr_CannotDoInCurrentContext: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_cannotdoincurrentcontext)
- [var kAudioToolboxErr_EndOfTrack: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_endoftrack)
- [var kAudioToolboxErr_IllegalTrackDestination: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_illegaltrackdestination)
- [var kAudioToolboxErr_InvalidEventType: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_invalideventtype)
- [var kAudioToolboxErr_InvalidPlayerState: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_invalidplayerstate)
- [var kAudioToolboxErr_InvalidSequenceType: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_invalidsequencetype)
- [var kAudioToolboxErr_NoSequence: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_nosequence)
- [var kAudioToolboxErr_StartOfTrack: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_startoftrack)
- [var kAudioToolboxErr_TrackIndexError: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_trackindexerror)
- [var kAudioToolboxErr_TrackNotFound: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerr_tracknotfound)
- [var kAudioToolboxError_NoTrackDestination: OSStatus](/documentation/audiotoolbox/kaudiotoolboxerror_notrackdestination)
- [Music Event Types](/documentation/audiotoolbox/1515479-music-event-types)

#### Constants

- [var kMusicEventType_AUPreset: UInt32](/documentation/audiotoolbox/kmusiceventtype_aupreset)
- [var kMusicEventType_ExtendedNote: UInt32](/documentation/audiotoolbox/kmusiceventtype_extendednote)
- [var kMusicEventType_ExtendedTempo: UInt32](/documentation/audiotoolbox/kmusiceventtype_extendedtempo)
- [var kMusicEventType_MIDIChannelMessage: UInt32](/documentation/audiotoolbox/kmusiceventtype_midichannelmessage)
- [var kMusicEventType_MIDINoteMessage: UInt32](/documentation/audiotoolbox/kmusiceventtype_midinotemessage)
- [var kMusicEventType_MIDIRawData: UInt32](/documentation/audiotoolbox/kmusiceventtype_midirawdata)
- [var kMusicEventType_Meta: UInt32](/documentation/audiotoolbox/kmusiceventtype_meta)
- [var kMusicEventType_NULL: UInt32](/documentation/audiotoolbox/kmusiceventtype_null)
- [var kMusicEventType_Parameter: UInt32](/documentation/audiotoolbox/kmusiceventtype_parameter)
- [var kMusicEventType_User: UInt32](/documentation/audiotoolbox/kmusiceventtype_user)
- [Music Note Events](/documentation/audiotoolbox/1473494-music-note-events)

#### Constants

- [var kMusicNoteEvent_Unused: UInt32](/documentation/audiotoolbox/kmusicnoteevent_unused)
- [var kMusicNoteEvent_UseGroupInstrument: UInt32](/documentation/audiotoolbox/kmusicnoteevent_usegroupinstrument)
- [Music Device Selectors](/documentation/audiotoolbox/1473469-music-device-selectors)

#### Constants

- [var kMusicDeviceMIDIEventSelect: Int](/documentation/audiotoolbox/kmusicdevicemidieventselect)
- [var kMusicDevicePrepareInstrumentSelect: Int](/documentation/audiotoolbox/kmusicdeviceprepareinstrumentselect)
- [var kMusicDeviceRange: Int](/documentation/audiotoolbox/kmusicdevicerange)
- [var kMusicDeviceReleaseInstrumentSelect: Int](/documentation/audiotoolbox/kmusicdevicereleaseinstrumentselect)
- [var kMusicDeviceStartNoteSelect: Int](/documentation/audiotoolbox/kmusicdevicestartnoteselect)
- [var kMusicDeviceStopNoteSelect: Int](/documentation/audiotoolbox/kmusicdevicestopnoteselect)
- [var kMusicDeviceSysExSelect: Int](/documentation/audiotoolbox/kmusicdevicesysexselect)
- [var kMusicDeviceMIDIEventListSelect: Int](/documentation/audiotoolbox/kmusicdevicemidieventlistselect)
- [Music Device Properties](/documentation/audiotoolbox/1533931-music-device-properties)

#### Constants

- [var kMusicDeviceProperty_InstrumentName: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_instrumentname)
- [var kMusicDeviceProperty_InstrumentNumber: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_instrumentnumber)
- [Music Device Sample Frame Mask](/documentation/audiotoolbox/1533978-music-device-sample-frame-mask)

#### Constants

- [var kMusicDeviceSampleFrameMask_IsScheduled: Int](/documentation/audiotoolbox/kmusicdevicesampleframemask_isscheduled)
- [var kMusicDeviceSampleFrameMask_SampleOffset: Int](/documentation/audiotoolbox/kmusicdevicesampleframemask_sampleoffset)
- [Music Device Unit Properties](/documentation/audiotoolbox/1533963-music-device-unit-properties)

#### Constants

- [var kMusicDeviceProperty_DualSchedulingMode: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_dualschedulingmode)
- [var kMusicDeviceProperty_MIDIXMLNames: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_midixmlnames)
- [var kMusicDeviceProperty_PartGroup: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_partgroup)
- [var kMusicDeviceProperty_SupportsStartStopNote: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_supportsstartstopnote)
- [Instrument Types](/documentation/audiotoolbox/1534202-instrument-types)

#### Constants

- [var kInstrumentType_AUPreset: Int](/documentation/audiotoolbox/kinstrumenttype_aupreset)
- [var kInstrumentType_Audiofile: Int](/documentation/audiotoolbox/kinstrumenttype_audiofile)
- [var kInstrumentType_DLSPreset: Int](/documentation/audiotoolbox/kinstrumenttype_dlspreset)
- [var kInstrumentType_EXS24: Int](/documentation/audiotoolbox/kinstrumenttype_exs24)
- [var kInstrumentType_SF2Preset: Int](/documentation/audiotoolbox/kinstrumenttype_sf2preset)
- [Music Device Generic Properties](/documentation/audiotoolbox/1533930-music-device-generic-properties)

#### Constants

- [var kMusicDeviceProperty_BankName: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_bankname)
- [var kMusicDeviceProperty_InstrumentCount: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_instrumentcount)
- [var kMusicDeviceProperty_SoundBankURL: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_soundbankurl)
- [Music Effect and Instrument Unit Properties](/documentation/audiotoolbox/1533941-music-effect-and-instrument-unit)

#### Constants

- [var kAudioUnitProperty_AddParameterMIDIMapping: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_addparametermidimapping)
- [var kAudioUnitProperty_AllParameterMIDIMappings: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_allparametermidimappings)
- [var kAudioUnitProperty_HotMapParameterMIDIMapping: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_hotmapparametermidimapping)
- [var kAudioUnitProperty_RemoveParameterMIDIMapping: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_removeparametermidimapping)
- [DLS Music Device Properties](/documentation/audiotoolbox/1534153-dls-music-device-properties)

#### Constants

- [var kMusicDeviceProperty_SoundBankData: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_soundbankdata)
- [var kMusicDeviceProperty_SoundBankFSRef: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_soundbankfsref)
- [var kMusicDeviceProperty_StreamFromDisk: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_streamfromdisk)
- [var kMusicDeviceProperty_UsesInternalReverb: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_usesinternalreverb)
- [DLS Music Device Parameters](/documentation/audiotoolbox/1389667-dls-music-device-parameters)

#### Constants

- [var kMusicDeviceParam_ReverbVolume: AudioUnitParameterID](/documentation/audiotoolbox/kmusicdeviceparam_reverbvolume)
- [var kMusicDeviceParam_Tuning: AudioUnitParameterID](/documentation/audiotoolbox/kmusicdeviceparam_tuning)
- [var kMusicDeviceParam_Volume: AudioUnitParameterID](/documentation/audiotoolbox/kmusicdeviceparam_volume)
- [Anchoring sound to a window or volume](/documentation/audiotoolbox/spatializing-sound-from-a-uiscene)

## Audio Files and Formats

- [Audio Format Services](/documentation/audiotoolbox/audio-format-services)

### Audio Format Services Functions

- [func AudioFormatGetProperty(AudioFormatPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>?, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audioformatgetproperty(_:_:_:_:_:))
- [func AudioFormatGetPropertyInfo(AudioFormatPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audioformatgetpropertyinfo(_:_:_:_:))

### Data Types

- [AudioBalanceFade](/documentation/audiotoolbox/audiobalancefade)

#### Initializers

- [init(mLeftRightBalance: Float32, mBackFrontFade: Float32, mType: AudioBalanceFadeType, mChannelLayout: UnsafePointer<AudioChannelLayout>)](/documentation/audiotoolbox/audiobalancefade/init(mleftrightbalance:mbackfrontfade:mtype:mchannellayout:))

#### Instance Properties

- [var mBackFrontFade: Float32](/documentation/audiotoolbox/audiobalancefade/mbackfrontfade)
- [var mChannelLayout: UnsafePointer<AudioChannelLayout>](/documentation/audiotoolbox/audiobalancefade/mchannellayout)
- [var mLeftRightBalance: Float32](/documentation/audiotoolbox/audiobalancefade/mleftrightbalance)
- [var mType: AudioBalanceFadeType](/documentation/audiotoolbox/audiobalancefade/mtype)
- [AudioFormatInfo](/documentation/audiotoolbox/audioformatinfo)

#### Initializers

- [init(mASBD: AudioStreamBasicDescription, mMagicCookie: UnsafeRawPointer, mMagicCookieSize: UInt32)](/documentation/audiotoolbox/audioformatinfo/init(masbd:mmagiccookie:mmagiccookiesize:))

#### Instance Properties

- [var mASBD: AudioStreamBasicDescription](/documentation/audiotoolbox/audioformatinfo/masbd)
- [var mMagicCookie: UnsafeRawPointer](/documentation/audiotoolbox/audioformatinfo/mmagiccookie)
- [var mMagicCookieSize: UInt32](/documentation/audiotoolbox/audioformatinfo/mmagiccookiesize)
- [AudioFormatListItem](/documentation/coreaudiotypes/audioformatlistitem)
- [AudioPanningInfo](/documentation/audiotoolbox/audiopanninginfo)

#### Initializers

- [init(mPanningMode: AudioPanningMode, mCoordinateFlags: UInt32, mCoordinates: (Float32, Float32, Float32), mGainScale: Float32, mOutputChannelMap: UnsafePointer<AudioChannelLayout>)](/documentation/audiotoolbox/audiopanninginfo/init(mpanningmode:mcoordinateflags:mcoordinates:mgainscale:moutputchannelmap:))

#### Instance Properties

- [var mCoordinateFlags: UInt32](/documentation/audiotoolbox/audiopanninginfo/mcoordinateflags)
- [var mCoordinates: (Float32, Float32, Float32)](/documentation/audiotoolbox/audiopanninginfo/mcoordinates)
- [var mGainScale: Float32](/documentation/audiotoolbox/audiopanninginfo/mgainscale)
- [var mOutputChannelMap: UnsafePointer<AudioChannelLayout>](/documentation/audiotoolbox/audiopanninginfo/moutputchannelmap)
- [var mPanningMode: AudioPanningMode](/documentation/audiotoolbox/audiopanninginfo/mpanningmode)
- [ExtendedAudioFormatInfo](/documentation/audiotoolbox/extendedaudioformatinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/extendedaudioformatinfo/init())
- [init(mASBD: AudioStreamBasicDescription, mMagicCookie: UnsafeRawPointer?, mMagicCookieSize: UInt32, mClassDescription: AudioClassDescription)](/documentation/audiotoolbox/extendedaudioformatinfo/init(masbd:mmagiccookie:mmagiccookiesize:mclassdescription:))

#### Instance Properties

- [var mASBD: AudioStreamBasicDescription](/documentation/audiotoolbox/extendedaudioformatinfo/masbd)
- [var mClassDescription: AudioClassDescription](/documentation/audiotoolbox/extendedaudioformatinfo/mclassdescription)
- [var mMagicCookie: UnsafeRawPointer?](/documentation/audiotoolbox/extendedaudioformatinfo/mmagiccookie)
- [var mMagicCookieSize: UInt32](/documentation/audiotoolbox/extendedaudioformatinfo/mmagiccookiesize)
- [AudioFormatPropertyID](/documentation/audiotoolbox/audioformatpropertyid)

### Constants

- [AudioBalanceFadeType](/documentation/audiotoolbox/audiobalancefadetype)

#### Types

- [case equalPower](/documentation/audiotoolbox/audiobalancefadetype/equalpower)
- [case maxUnityGain](/documentation/audiotoolbox/audiobalancefadetype/maxunitygain)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiobalancefadetype/init(rawvalue:))
- [Audio Format Property Identifiers](/documentation/audiotoolbox/1577853-audio-format-property-identifier)

#### Constants

- [var kAudioFormatProperty_FormatInfo: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatinfo)
- [var kAudioFormatProperty_FormatName: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatname)
- [var kAudioFormatProperty_EncodeFormatIDs: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_encodeformatids)
- [var kAudioFormatProperty_DecodeFormatIDs: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_decodeformatids)
- [var kAudioFormatProperty_FormatList: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatlist)
- [var kAudioFormatProperty_ASBDFromESDS: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_asbdfromesds)
- [var kAudioFormatProperty_ChannelLayoutFromESDS: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayoutfromesds)
- [var kAudioFormatProperty_OutputFormatList: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_outputformatlist)
- [var kAudioFormatProperty_FirstPlayableFormatFromList: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_firstplayableformatfromlist)
- [var kAudioFormatProperty_Encoders: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_encoders)
- [var kAudioFormatProperty_Decoders: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_decoders)
- [var kAudioFormatProperty_FormatIsVBR: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatisvbr)
- [var kAudioFormatProperty_FormatIsExternallyFramed: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatisexternallyframed)
- [var kAudioFormatProperty_AvailableEncodeBitRates: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_availableencodebitrates)
- [var kAudioFormatProperty_AvailableEncodeSampleRates: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_availableencodesamplerates)
- [var kAudioFormatProperty_AvailableEncodeChannelLayoutTags: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_availableencodechannellayouttags)
- [var kAudioFormatProperty_AvailableEncodeNumberChannels: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_availableencodenumberchannels)
- [var kAudioFormatProperty_ASBDFromMPEGPacket: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_asbdfrommpegpacket)
- [var kAudioFormatProperty_BitmapForLayoutTag: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_bitmapforlayouttag)
- [var kAudioFormatProperty_MatrixMixMap: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_matrixmixmap)
- [var kAudioFormatProperty_ChannelMap: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channelmap)
- [var kAudioFormatProperty_NumberOfChannelsForLayout: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_numberofchannelsforlayout)
- [var kAudioFormatProperty_ValidateChannelLayout: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_validatechannellayout)
- [var kAudioFormatProperty_ChannelLayoutForTag: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayoutfortag)
- [var kAudioFormatProperty_TagForChannelLayout: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_tagforchannellayout)
- [var kAudioFormatProperty_ChannelLayoutName: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayoutname)
- [var kAudioFormatProperty_ChannelLayoutSimpleName: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayoutsimplename)
- [var kAudioFormatProperty_ChannelLayoutForBitmap: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayoutforbitmap)
- [var kAudioFormatProperty_ChannelName: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channelname)
- [var kAudioFormatProperty_ChannelShortName: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channelshortname)
- [var kAudioFormatProperty_TagsForNumberOfChannels: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_tagsfornumberofchannels)
- [var kAudioFormatProperty_PanningMatrix: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_panningmatrix)
- [var kAudioFormatProperty_BalanceFade: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_balancefade)
- [var kAudioFormatProperty_ID3TagSize: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_id3tagsize)
- [var kAudioFormatProperty_ID3TagToDictionary: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_id3tagtodictionary)
- [var kAudioFormatProperty_AreChannelLayoutsEquivalent: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_arechannellayoutsequivalent)
- [var kAudioFormatProperty_ChannelLayoutHash: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_channellayouthash)
- [var kAudioFormatProperty_FormatIsEncrypted: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatisencrypted)
- [var kAudioFormatProperty_AvailableDecodeNumberChannels: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_availabledecodenumberchannels)
- [var kAudioFormatProperty_FormatEmploysDependentPackets: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_formatemploysdependentpackets)
- [Audio Codec Component Constants](/documentation/audiotoolbox/1494086-audio-codec-component-constants)

#### Constants

- [var kAudioDecoderComponentType: UInt32](/documentation/audiotoolbox/kaudiodecodercomponenttype)
- [var kAudioEncoderComponentType: UInt32](/documentation/audiotoolbox/kaudioencodercomponenttype)
- [var kAudioUnityCodecComponentType: UInt32](/documentation/audiotoolbox/kaudiounitycodeccomponenttype)
- [Audio Codec Manufacturer and Implementation Types](/documentation/audiotoolbox/1620448-audio-codec-manufacturer-and-imp)

#### Constants

- [var kAppleSoftwareAudioCodecManufacturer: UInt32](/documentation/audiotoolbox/kapplesoftwareaudiocodecmanufacturer)
- [var kAppleHardwareAudioCodecManufacturer: UInt32](/documentation/audiotoolbox/kapplehardwareaudiocodecmanufacturer)
- [AudioPanningMode](/documentation/audiotoolbox/audiopanningmode)

#### Modes

- [case panningMode_SoundField](/documentation/audiotoolbox/audiopanningmode/panningmode_soundfield)
- [case panningMode_VectorBasedPanning](/documentation/audiotoolbox/audiopanningmode/panningmode_vectorbasedpanning)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/audiopanningmode/init(rawvalue:))

### Result Codes

- [Audio Format Error Codes](/documentation/audiotoolbox/1577851-audio-format-error-codes)

#### Constants

- [var kAudioFormatBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioformatbadpropertysizeerror)
- [var kAudioFormatBadSpecifierSizeError: OSStatus](/documentation/audiotoolbox/kaudioformatbadspecifiersizeerror)
- [var kAudioFormatUnknownFormatError: OSStatus](/documentation/audiotoolbox/kaudioformatunknownformaterror)
- [var kAudioFormatUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioformatunspecifiederror)
- [var kAudioFormatUnsupportedDataFormatError: OSStatus](/documentation/audiotoolbox/kaudioformatunsupporteddataformaterror)
- [var kAudioFormatUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudioformatunsupportedpropertyerror)
- [var kAudioFormatUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioformatunspecifiederror)
- [var kAudioFormatUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudioformatunsupportedpropertyerror)
- [var kAudioFormatBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioformatbadpropertysizeerror)
- [var kAudioFormatBadSpecifierSizeError: OSStatus](/documentation/audiotoolbox/kaudioformatbadspecifiersizeerror)
- [var kAudioFormatUnsupportedDataFormatError: OSStatus](/documentation/audiotoolbox/kaudioformatunsupporteddataformaterror)
- [var kAudioFormatUnknownFormatError: OSStatus](/documentation/audiotoolbox/kaudioformatunknownformaterror)
- [Audio File Services](/documentation/audiotoolbox/audio-file-services)

### Creating and Initializing Audio Files

- [func AudioFileCreateWithURL(CFURL, AudioFileTypeID, UnsafePointer<AudioStreamBasicDescription>, AudioFileFlags, UnsafeMutablePointer<AudioFileID?>) -> OSStatus](/documentation/audiotoolbox/audiofilecreatewithurl(_:_:_:_:_:))
- [func AudioFileInitializeWithCallbacks(UnsafeMutableRawPointer, AudioFile_ReadProc, AudioFile_WriteProc, AudioFile_GetSizeProc, AudioFile_SetSizeProc, AudioFileTypeID, UnsafePointer<AudioStreamBasicDescription>, AudioFileFlags, UnsafeMutablePointer<AudioFileID?>) -> OSStatus](/documentation/audiotoolbox/audiofileinitializewithcallbacks(_:_:_:_:_:_:_:_:_:))

### Opening and Closing Audio Files

- [func AudioFileOpenURL(CFURL, AudioFilePermissions, AudioFileTypeID, UnsafeMutablePointer<AudioFileID?>) -> OSStatus](/documentation/audiotoolbox/audiofileopenurl(_:_:_:_:))
- [func AudioFileOpenWithCallbacks(UnsafeMutableRawPointer, AudioFile_ReadProc, AudioFile_WriteProc?, AudioFile_GetSizeProc, AudioFile_SetSizeProc?, AudioFileTypeID, UnsafeMutablePointer<AudioFileID?>) -> OSStatus](/documentation/audiotoolbox/audiofileopenwithcallbacks(_:_:_:_:_:_:_:))
- [func AudioFileClose(AudioFileID) -> OSStatus](/documentation/audiotoolbox/audiofileclose(_:))

### Reading and Writing Audio Files

- [func AudioFileReadBytes(AudioFileID, Bool, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilereadbytes(_:_:_:_:_:))
- [func AudioFileWriteBytes(AudioFileID, Bool, Int64, UnsafeMutablePointer<UInt32>, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilewritebytes(_:_:_:_:_:))
- [func AudioFileReadPacketData(AudioFileID, Bool, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiofilereadpacketdata(_:_:_:_:_:_:_:))
- [func AudioFileWritePackets(AudioFileID, Bool, UInt32, UnsafePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilewritepackets(_:_:_:_:_:_:_:))

### Getting and Setting Audio File Properties

- [func AudioFileGetProperty(AudioFileID, AudioFilePropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilegetproperty(_:_:_:_:))
- [func AudioFileGetPropertyInfo(AudioFileID, AudioFilePropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UInt32>?) -> OSStatus](/documentation/audiotoolbox/audiofilegetpropertyinfo(_:_:_:_:))
- [func AudioFileSetProperty(AudioFileID, AudioFilePropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilesetproperty(_:_:_:_:))

### Working with User Data

- [func AudioFileCountUserData(AudioFileID, UInt32, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecountuserdata(_:_:_:))
- [func AudioFileGetUserDataSize(AudioFileID, UInt32, UInt32, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilegetuserdatasize(_:_:_:_:))
- [func AudioFileGetUserDataSize64(AudioFileID, UInt32, UInt32, UnsafeMutablePointer<UInt64>) -> OSStatus](/documentation/audiotoolbox/audiofilegetuserdatasize64(_:_:_:_:))
- [func AudioFileGetUserData(AudioFileID, UInt32, UInt32, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilegetuserdata(_:_:_:_:_:))
- [func AudioFileGetUserDataAtOffset(AudioFileID, UInt32, UInt32, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilegetuserdataatoffset(_:_:_:_:_:_:))
- [func AudioFileSetUserData(AudioFileID, UInt32, UInt32, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilesetuserdata(_:_:_:_:_:))
- [func AudioFileRemoveUserData(AudioFileID, UInt32, UInt32) -> OSStatus](/documentation/audiotoolbox/audiofileremoveuserdata(_:_:_:))

### Working with Global Information

- [func AudioFileGetGlobalInfoSize(AudioFilePropertyID, UInt32, UnsafeMutableRawPointer?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilegetglobalinfosize(_:_:_:_:))
- [func AudioFileGetGlobalInfo(AudioFilePropertyID, UInt32, UnsafeMutableRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilegetglobalinfo(_:_:_:_:_:))

### Optimizing Audio Files

- [func AudioFileOptimize(AudioFileID) -> OSStatus](/documentation/audiotoolbox/audiofileoptimize(_:))

### Parsing Audio File Content

- [func NextAudioFileRegion(UnsafePointer<AudioFileRegion>) -> UnsafeMutablePointer<AudioFileRegion>](/documentation/audiotoolbox/nextaudiofileregion(_:))
- [func NumAudioFileMarkersToNumBytes(Int) -> Int](/documentation/audiotoolbox/numaudiofilemarkerstonumbytes(_:))
- [func NumBytesToNumAudioFileMarkers(Int) -> Int](/documentation/audiotoolbox/numbytestonumaudiofilemarkers(_:))

### Callbacks

- [AudioFile_ReadProc](/documentation/audiotoolbox/audiofile_readproc)
- [AudioFile_WriteProc](/documentation/audiotoolbox/audiofile_writeproc)
- [AudioFile_GetSizeProc](/documentation/audiotoolbox/audiofile_getsizeproc)
- [AudioFile_SetSizeProc](/documentation/audiotoolbox/audiofile_setsizeproc)

### Data Types

- [AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslationflags)

#### Flags

- [static var bytePacketTranslationFlag_IsEstimate: AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslationflags/bytepackettranslationflag_isestimate)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiobytepackettranslationflags/init(rawvalue:))
- [AudioFileFlags](/documentation/audiotoolbox/audiofileflags)

#### Flags

- [static var dontPageAlignAudioData: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/dontpagealignaudiodata)
- [static var eraseFile: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/erasefile)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofileflags/init(rawvalue:))
- [AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags)

#### Constants

- [static var loopEnable: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/loopenable)
- [static var playBackward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playbackward)
- [static var playForward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playforward)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofileregionflags/init(rawvalue:))
- [AudioFileStreamParseFlags](/documentation/audiotoolbox/audiofilestreamparseflags)

#### Constants

- [static var discontinuity: AudioFileStreamParseFlags](/documentation/audiotoolbox/audiofilestreamparseflags/discontinuity)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreamparseflags/init(rawvalue:))
- [AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags)

#### Constants

- [static var cacheProperty: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/cacheproperty)
- [static var propertyIsCached: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/propertyiscached)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreampropertyflags/init(rawvalue:))
- [AudioFileStreamSeekFlags](/documentation/audiotoolbox/audiofilestreamseekflags)

#### Constants

- [static var offsetIsEstimated: AudioFileStreamSeekFlags](/documentation/audiotoolbox/audiofilestreamseekflags/offsetisestimated)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreamseekflags/init(rawvalue:))
- [AudioFileID](/documentation/audiotoolbox/audiofileid)
- [AudioFilePropertyID](/documentation/audiotoolbox/audiofilepropertyid)
- [AudioFile_SMPTE_Time](/documentation/audiotoolbox/audiofile_smpte_time)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofile_smpte_time/init())
- [init(mHours: Int8, mMinutes: UInt8, mSeconds: UInt8, mFrames: UInt8, mSubFrameSampleOffset: UInt32)](/documentation/audiotoolbox/audiofile_smpte_time/init(mhours:mminutes:mseconds:mframes:msubframesampleoffset:))

#### Instance Properties

- [var mFrames: UInt8](/documentation/audiotoolbox/audiofile_smpte_time/mframes)
- [var mHours: Int8](/documentation/audiotoolbox/audiofile_smpte_time/mhours)
- [var mMinutes: UInt8](/documentation/audiotoolbox/audiofile_smpte_time/mminutes)
- [var mSeconds: UInt8](/documentation/audiotoolbox/audiofile_smpte_time/mseconds)
- [var mSubFrameSampleOffset: UInt32](/documentation/audiotoolbox/audiofile_smpte_time/msubframesampleoffset)
- [AudioFileMarker](/documentation/audiotoolbox/audiofilemarker)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofilemarker/init())
- [init(mFramePosition: Float64, mName: Unmanaged<CFString>?, mMarkerID: Int32, mSMPTETime: AudioFile_SMPTE_Time, mType: UInt32, mReserved: UInt16, mChannel: UInt16)](/documentation/audiotoolbox/audiofilemarker/init(mframeposition:mname:mmarkerid:msmptetime:mtype:mreserved:mchannel:))

#### Instance Properties

- [var mChannel: UInt16](/documentation/audiotoolbox/audiofilemarker/mchannel)
- [var mFramePosition: Float64](/documentation/audiotoolbox/audiofilemarker/mframeposition)
- [var mMarkerID: Int32](/documentation/audiotoolbox/audiofilemarker/mmarkerid)
- [var mName: Unmanaged<CFString>?](/documentation/audiotoolbox/audiofilemarker/mname)
- [var mReserved: UInt16](/documentation/audiotoolbox/audiofilemarker/mreserved)
- [var mSMPTETime: AudioFile_SMPTE_Time](/documentation/audiotoolbox/audiofilemarker/msmptetime)
- [var mType: UInt32](/documentation/audiotoolbox/audiofilemarker/mtype)
- [AudioFileMarkerList](/documentation/audiotoolbox/audiofilemarkerlist)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofilemarkerlist/init())
- [init(mSMPTE_TimeType: UInt32, mNumberMarkers: UInt32, mMarkers: AudioFileMarker)](/documentation/audiotoolbox/audiofilemarkerlist/init(msmpte_timetype:mnumbermarkers:mmarkers:))

#### Instance Properties

- [var mMarkers: AudioFileMarker](/documentation/audiotoolbox/audiofilemarkerlist/mmarkers)
- [var mNumberMarkers: UInt32](/documentation/audiotoolbox/audiofilemarkerlist/mnumbermarkers)
- [var mSMPTE_TimeType: UInt32](/documentation/audiotoolbox/audiofilemarkerlist/msmpte_timetype)
- [AudioFileRegion](/documentation/audiotoolbox/audiofileregion)

#### Initializers

- [init(mRegionID: UInt32, mName: Unmanaged<CFString>, mFlags: AudioFileRegionFlags, mNumberMarkers: UInt32, mMarkers: AudioFileMarker)](/documentation/audiotoolbox/audiofileregion/init(mregionid:mname:mflags:mnumbermarkers:mmarkers:))

#### Instance Properties

- [var mFlags: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregion/mflags)
- [var mMarkers: AudioFileMarker](/documentation/audiotoolbox/audiofileregion/mmarkers)
- [var mName: Unmanaged<CFString>](/documentation/audiotoolbox/audiofileregion/mname)
- [var mNumberMarkers: UInt32](/documentation/audiotoolbox/audiofileregion/mnumbermarkers)
- [var mRegionID: UInt32](/documentation/audiotoolbox/audiofileregion/mregionid)
- [AudioFileRegionList](/documentation/audiotoolbox/audiofileregionlist)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofileregionlist/init())
- [init(mSMPTE_TimeType: UInt32, mNumberRegions: UInt32, mRegions: AudioFileRegion)](/documentation/audiotoolbox/audiofileregionlist/init(msmpte_timetype:mnumberregions:mregions:))

#### Instance Properties

- [var mNumberRegions: UInt32](/documentation/audiotoolbox/audiofileregionlist/mnumberregions)
- [var mRegions: AudioFileRegion](/documentation/audiotoolbox/audiofileregionlist/mregions)
- [var mSMPTE_TimeType: UInt32](/documentation/audiotoolbox/audiofileregionlist/msmpte_timetype)
- [AudioFramePacketTranslation](/documentation/audiotoolbox/audioframepackettranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audioframepackettranslation/init())
- [init(mFrame: Int64, mPacket: Int64, mFrameOffsetInPacket: UInt32)](/documentation/audiotoolbox/audioframepackettranslation/init(mframe:mpacket:mframeoffsetinpacket:))

#### Instance Properties

- [var mFrame: Int64](/documentation/audiotoolbox/audioframepackettranslation/mframe)
- [var mFrameOffsetInPacket: UInt32](/documentation/audiotoolbox/audioframepackettranslation/mframeoffsetinpacket)
- [var mPacket: Int64](/documentation/audiotoolbox/audioframepackettranslation/mpacket)
- [AudioBytePacketTranslation](/documentation/audiotoolbox/audiobytepackettranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audiobytepackettranslation/init())
- [init(mByte: Int64, mPacket: Int64, mByteOffsetInPacket: UInt32, mFlags: AudioBytePacketTranslationFlags)](/documentation/audiotoolbox/audiobytepackettranslation/init(mbyte:mpacket:mbyteoffsetinpacket:mflags:))

#### Instance Properties

- [var mByte: Int64](/documentation/audiotoolbox/audiobytepackettranslation/mbyte)
- [var mByteOffsetInPacket: UInt32](/documentation/audiotoolbox/audiobytepackettranslation/mbyteoffsetinpacket)
- [var mFlags: AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslation/mflags)
- [var mPacket: Int64](/documentation/audiotoolbox/audiobytepackettranslation/mpacket)
- [AudioFilePacketTableInfo](/documentation/audiotoolbox/audiofilepackettableinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofilepackettableinfo/init())
- [init(mNumberValidFrames: Int64, mPrimingFrames: Int32, mRemainderFrames: Int32)](/documentation/audiotoolbox/audiofilepackettableinfo/init(mnumbervalidframes:mprimingframes:mremainderframes:))

#### Instance Properties

- [var mNumberValidFrames: Int64](/documentation/audiotoolbox/audiofilepackettableinfo/mnumbervalidframes)
- [var mPrimingFrames: Int32](/documentation/audiotoolbox/audiofilepackettableinfo/mprimingframes)
- [var mRemainderFrames: Int32](/documentation/audiotoolbox/audiofilepackettableinfo/mremainderframes)
- [AudioFileTypeAndFormatID](/documentation/audiotoolbox/audiofiletypeandformatid)

#### Initializers

- [init()](/documentation/audiotoolbox/audiofiletypeandformatid/init())
- [init(mFileType: AudioFileTypeID, mFormatID: UInt32)](/documentation/audiotoolbox/audiofiletypeandformatid/init(mfiletype:mformatid:))

#### Instance Properties

- [var mFileType: AudioFileTypeID](/documentation/audiotoolbox/audiofiletypeandformatid/mfiletype)
- [var mFormatID: UInt32](/documentation/audiotoolbox/audiofiletypeandformatid/mformatid)
- [AudioIndependentPacketTranslation](/documentation/audiotoolbox/audioindependentpackettranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audioindependentpackettranslation/init())
- [init(mPacket: Int64, mIndependentlyDecodablePacket: Int64)](/documentation/audiotoolbox/audioindependentpackettranslation/init(mpacket:mindependentlydecodablepacket:))

#### Instance Properties

- [var mIndependentlyDecodablePacket: Int64](/documentation/audiotoolbox/audioindependentpackettranslation/mindependentlydecodablepacket)
- [var mPacket: Int64](/documentation/audiotoolbox/audioindependentpackettranslation/mpacket)
- [AudioPacketDependencyInfoTranslation](/documentation/audiotoolbox/audiopacketdependencyinfotranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audiopacketdependencyinfotranslation/init())
- [init(mPacket: Int64, mIsIndependentlyDecodable: UInt32, mNumberPrerollPackets: UInt32)](/documentation/audiotoolbox/audiopacketdependencyinfotranslation/init(mpacket:misindependentlydecodable:mnumberprerollpackets:))

#### Instance Properties

- [var mIsIndependentlyDecodable: UInt32](/documentation/audiotoolbox/audiopacketdependencyinfotranslation/misindependentlydecodable)
- [var mNumberPrerollPackets: UInt32](/documentation/audiotoolbox/audiopacketdependencyinfotranslation/mnumberprerollpackets)
- [var mPacket: Int64](/documentation/audiotoolbox/audiopacketdependencyinfotranslation/mpacket)
- [AudioPacketRangeByteCountTranslation](/documentation/audiotoolbox/audiopacketrangebytecounttranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audiopacketrangebytecounttranslation/init())
- [init(mPacket: Int64, mPacketCount: Int64, mByteCountUpperBound: Int64)](/documentation/audiotoolbox/audiopacketrangebytecounttranslation/init(mpacket:mpacketcount:mbytecountupperbound:))

#### Instance Properties

- [var mByteCountUpperBound: Int64](/documentation/audiotoolbox/audiopacketrangebytecounttranslation/mbytecountupperbound)
- [var mPacket: Int64](/documentation/audiotoolbox/audiopacketrangebytecounttranslation/mpacket)
- [var mPacketCount: Int64](/documentation/audiotoolbox/audiopacketrangebytecounttranslation/mpacketcount)
- [AudioPacketRollDistanceTranslation](/documentation/audiotoolbox/audiopacketrolldistancetranslation)

#### Initializers

- [init()](/documentation/audiotoolbox/audiopacketrolldistancetranslation/init())
- [init(mPacket: Int64, mRollDistance: Int64)](/documentation/audiotoolbox/audiopacketrolldistancetranslation/init(mpacket:mrolldistance:))

#### Instance Properties

- [var mPacket: Int64](/documentation/audiotoolbox/audiopacketrolldistancetranslation/mpacket)
- [var mRollDistance: Int64](/documentation/audiotoolbox/audiopacketrolldistancetranslation/mrolldistance)

### Enumerations

- [AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslationflags)

#### Flags

- [static var bytePacketTranslationFlag_IsEstimate: AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslationflags/bytepackettranslationflag_isestimate)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiobytepackettranslationflags/init(rawvalue:))
- [AudioFileFlags](/documentation/audiotoolbox/audiofileflags)

#### Flags

- [static var dontPageAlignAudioData: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/dontpagealignaudiodata)
- [static var eraseFile: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/erasefile)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofileflags/init(rawvalue:))
- [AudioFilePermissions](/documentation/audiotoolbox/audiofilepermissions)

#### Constants

- [case readPermission](/documentation/audiotoolbox/audiofilepermissions/readpermission)
- [case readWritePermission](/documentation/audiotoolbox/audiofilepermissions/readwritepermission)
- [case writePermission](/documentation/audiotoolbox/audiofilepermissions/writepermission)

#### Initializers

- [init?(rawValue: Int8)](/documentation/audiotoolbox/audiofilepermissions/init(rawvalue:))
- [AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags)

#### Constants

- [static var loopEnable: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/loopenable)
- [static var playBackward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playbackward)
- [static var playForward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playforward)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofileregionflags/init(rawvalue:))
- [AudioFileStreamParseFlags](/documentation/audiotoolbox/audiofilestreamparseflags)

#### Constants

- [static var discontinuity: AudioFileStreamParseFlags](/documentation/audiotoolbox/audiofilestreamparseflags/discontinuity)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreamparseflags/init(rawvalue:))
- [AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags)

#### Constants

- [static var cacheProperty: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/cacheproperty)
- [static var propertyIsCached: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/propertyiscached)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreampropertyflags/init(rawvalue:))
- [AudioFileStreamSeekFlags](/documentation/audiotoolbox/audiofilestreamseekflags)

#### Constants

- [static var offsetIsEstimated: AudioFileStreamSeekFlags](/documentation/audiotoolbox/audiofilestreamseekflags/offsetisestimated)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofilestreamseekflags/init(rawvalue:))

### Constants

- [AudioFileTypeID](/documentation/audiotoolbox/audiofiletypeid)

#### Constants

- [var kAudioFileAIFFType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaifftype)
- [var kAudioFileAIFCType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaifctype)
- [var kAudioFileWAVEType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilewavetype)
- [var kAudioFileSoundDesigner2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilesounddesigner2type)
- [var kAudioFileNextType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilenexttype)
- [var kAudioFileMP3Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp3type)
- [var kAudioFileMP2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp2type)
- [var kAudioFileMP1Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp1type)
- [var kAudioFileAC3Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileac3type)
- [var kAudioFileAAC_ADTSType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaac_adtstype)
- [var kAudioFileMPEG4Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilempeg4type)
- [var kAudioFileM4AType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilem4atype)
- [var kAudioFileCAFType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilecaftype)
- [var kAudioFile3GPType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofile3gptype)
- [var kAudioFile3GP2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofile3gp2type)
- [var kAudioFileAMRType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileamrtype)
- [Audio File Creation Flags](/documentation/audiotoolbox/audio_file_creation_flags)

#### Constants

- [static var eraseFile: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/erasefile)
- [static var dontPageAlignAudioData: AudioFileFlags](/documentation/audiotoolbox/audiofileflags/dontpagealignaudiodata)
- [AudioFilePermissions](/documentation/audiotoolbox/audiofilepermissions)

#### Constants

- [case readPermission](/documentation/audiotoolbox/audiofilepermissions/readpermission)
- [case readWritePermission](/documentation/audiotoolbox/audiofilepermissions/readwritepermission)
- [case writePermission](/documentation/audiotoolbox/audiofilepermissions/writepermission)

#### Initializers

- [init?(rawValue: Int8)](/documentation/audiotoolbox/audiofilepermissions/init(rawvalue:))
- [Audio File Loop Direction Constants](/documentation/audiotoolbox/1576494-audio-file-loop-direction-consta)

#### Constants

- [var kAudioFileLoopDirection_NoLooping: UInt32](/documentation/audiotoolbox/kaudiofileloopdirection_nolooping)
- [var kAudioFileLoopDirection_Forward: UInt32](/documentation/audiotoolbox/kaudiofileloopdirection_forward)
- [var kAudioFileLoopDirection_Backward: UInt32](/documentation/audiotoolbox/kaudiofileloopdirection_backward)
- [var kAudioFileLoopDirection_ForwardAndBackward: UInt32](/documentation/audiotoolbox/kaudiofileloopdirection_forwardandbackward)
- [Audio File Marker Types](/documentation/audiotoolbox/1576492-audio-file-marker-types)

#### Constants

- [var kAudioFileMarkerType_Generic: UInt32](/documentation/audiotoolbox/kaudiofilemarkertype_generic)
- [AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags)

#### Constants

- [static var loopEnable: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/loopenable)
- [static var playBackward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playbackward)
- [static var playForward: AudioFileRegionFlags](/documentation/audiotoolbox/audiofileregionflags/playforward)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiofileregionflags/init(rawvalue:))
- [Audio File Packet Translation Flags](/documentation/audiotoolbox/audio_file_packet_translation_flags)

#### Constants

- [static var bytePacketTranslationFlag_IsEstimate: AudioBytePacketTranslationFlags](/documentation/audiotoolbox/audiobytepackettranslationflags/bytepackettranslationflag_isestimate)
- [Info String Keys](/documentation/audiotoolbox/info-string-keys)

#### Constants

- [var kAFInfoDictionary_Artist: String](/documentation/audiotoolbox/kafinfodictionary_artist)
- [var kAFInfoDictionary_Album: String](/documentation/audiotoolbox/kafinfodictionary_album)
- [var kAFInfoDictionary_Tempo: String](/documentation/audiotoolbox/kafinfodictionary_tempo)
- [var kAFInfoDictionary_KeySignature: String](/documentation/audiotoolbox/kafinfodictionary_keysignature)
- [var kAFInfoDictionary_TimeSignature: String](/documentation/audiotoolbox/kafinfodictionary_timesignature)
- [var kAFInfoDictionary_TrackNumber: String](/documentation/audiotoolbox/kafinfodictionary_tracknumber)
- [var kAFInfoDictionary_Year: String](/documentation/audiotoolbox/kafinfodictionary_year)
- [var kAFInfoDictionary_Composer: String](/documentation/audiotoolbox/kafinfodictionary_composer)
- [var kAFInfoDictionary_Lyricist: String](/documentation/audiotoolbox/kafinfodictionary_lyricist)
- [var kAFInfoDictionary_Genre: String](/documentation/audiotoolbox/kafinfodictionary_genre)
- [var kAFInfoDictionary_Title: String](/documentation/audiotoolbox/kafinfodictionary_title)
- [var kAFInfoDictionary_RecordedDate: String](/documentation/audiotoolbox/kafinfodictionary_recordeddate)
- [var kAFInfoDictionary_Comments: String](/documentation/audiotoolbox/kafinfodictionary_comments)
- [var kAFInfoDictionary_Copyright: String](/documentation/audiotoolbox/kafinfodictionary_copyright)
- [var kAFInfoDictionary_SourceEncoder: String](/documentation/audiotoolbox/kafinfodictionary_sourceencoder)
- [var kAFInfoDictionary_EncodingApplication: String](/documentation/audiotoolbox/kafinfodictionary_encodingapplication)
- [var kAFInfoDictionary_NominalBitRate: String](/documentation/audiotoolbox/kafinfodictionary_nominalbitrate)
- [var kAFInfoDictionary_ChannelLayout: String](/documentation/audiotoolbox/kafinfodictionary_channellayout)
- [var kAFInfoDictionary_ApproximateDurationInSeconds: String](/documentation/audiotoolbox/kafinfodictionary_approximatedurationinseconds)
- [var kAFInfoDictionary_SourceBitDepth: String](/documentation/audiotoolbox/kafinfodictionary_sourcebitdepth)
- [var kAFInfoDictionary_ISRC: String](/documentation/audiotoolbox/kafinfodictionary_isrc)
- [var kAFInfoDictionary_SubTitle: String](/documentation/audiotoolbox/kafinfodictionary_subtitle)
- [Audio File Properties](/documentation/audiotoolbox/1576499-audio-file-properties)

#### Constants

- [var kAudioFilePropertyFileFormat: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyfileformat)
- [var kAudioFilePropertyDataFormat: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertydataformat)
- [var kAudioFilePropertyFormatList: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyformatlist)
- [var kAudioFilePropertyIsOptimized: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyisoptimized)
- [var kAudioFilePropertyMagicCookieData: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertymagiccookiedata)
- [var kAudioFilePropertyAudioDataByteCount: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyaudiodatabytecount)
- [var kAudioFilePropertyAudioDataPacketCount: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyaudiodatapacketcount)
- [var kAudioFilePropertyMaximumPacketSize: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertymaximumpacketsize)
- [var kAudioFilePropertyDataOffset: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertydataoffset)
- [var kAudioFilePropertyChannelLayout: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertychannellayout)
- [var kAudioFilePropertyDeferSizeUpdates: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertydefersizeupdates)
- [var kAudioFilePropertyDataFormatName: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertydataformatname)
- [var kAudioFilePropertyMarkerList: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertymarkerlist)
- [var kAudioFilePropertyRegionList: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyregionlist)
- [var kAudioFilePropertyPacketToFrame: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypackettoframe)
- [var kAudioFilePropertyFrameToPacket: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyframetopacket)
- [var kAudioFilePropertyPacketToByte: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypackettobyte)
- [var kAudioFilePropertyByteToPacket: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertybytetopacket)
- [var kAudioFilePropertyChunkIDs: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertychunkids)
- [var kAudioFilePropertyInfoDictionary: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyinfodictionary)
- [var kAudioFilePropertyPacketTableInfo: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypackettableinfo)
- [var kAudioFilePropertyPacketSizeUpperBound: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypacketsizeupperbound)
- [var kAudioFilePropertyReserveDuration: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyreserveduration)
- [var kAudioFilePropertyEstimatedDuration: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyestimatedduration)
- [var kAudioFilePropertyBitRate: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertybitrate)
- [var kAudioFilePropertyID3Tag: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyid3tag)
- [var kAudioFilePropertySourceBitDepth: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertysourcebitdepth)
- [var kAudioFilePropertyAlbumArtwork: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyalbumartwork)
- [var kAudioFilePropertyAudioTrackCount: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyaudiotrackcount)
- [var kAudioFilePropertyUseAudioTrack: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyuseaudiotrack)
- [var kAudioFilePropertyID3TagOffset: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyid3tagoffset)
- [var kAudioFilePropertyNextIndependentPacket: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertynextindependentpacket)
- [var kAudioFilePropertyPacketRangeByteCountUpperBound: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypacketrangebytecountupperbound)
- [var kAudioFilePropertyPacketToDependencyInfo: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypackettodependencyinfo)
- [var kAudioFilePropertyPacketToRollDistance: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypackettorolldistance)
- [var kAudioFilePropertyPreviousIndependentPacket: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertypreviousindependentpacket)
- [var kAudioFilePropertyRestrictsRandomAccess: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilepropertyrestrictsrandomaccess)
- [Audio File Global Info Properties](/documentation/audiotoolbox/1576495-audio-file-global-info-propertie)

#### Constants

- [var kAudioFileGlobalInfo_ReadableTypes: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_readabletypes)
- [var kAudioFileGlobalInfo_WritableTypes: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_writabletypes)
- [var kAudioFileGlobalInfo_FileTypeName: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_filetypename)
- [var kAudioFileGlobalInfo_AvailableFormatIDs: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_availableformatids)
- [var kAudioFileGlobalInfo_AvailableStreamDescriptionsForFormat: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_availablestreamdescriptionsforformat)
- [var kAudioFileGlobalInfo_AllExtensions: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_allextensions)
- [var kAudioFileGlobalInfo_AllHFSTypeCodes: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_allhfstypecodes)
- [var kAudioFileGlobalInfo_AllUTIs: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_allutis)
- [var kAudioFileGlobalInfo_AllMIMETypes: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_allmimetypes)
- [var kAudioFileGlobalInfo_ExtensionsForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_extensionsfortype)
- [var kAudioFileGlobalInfo_HFSTypeCodesForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_hfstypecodesfortype)
- [var kAudioFileGlobalInfo_UTIsForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_utisfortype)
- [var kAudioFileGlobalInfo_MIMETypesForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_mimetypesfortype)
- [var kAudioFileGlobalInfo_TypesForExtension: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_typesforextension)
- [var kAudioFileGlobalInfo_TypesForHFSTypeCode: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_typesforhfstypecode)
- [var kAudioFileGlobalInfo_TypesForUTI: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_typesforuti)
- [var kAudioFileGlobalInfo_TypesForMIMEType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofileglobalinfo_typesformimetype)

### Result Codes

- [var kAudioFileUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudiofileunspecifiederror)
- [var kAudioFileUnsupportedFileTypeError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupportedfiletypeerror)
- [var kAudioFileUnsupportedDataFormatError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupporteddataformaterror)
- [var kAudioFileUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupportedpropertyerror)
- [var kAudioFileBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudiofilebadpropertysizeerror)
- [var kAudioFilePermissionsError: OSStatus](/documentation/audiotoolbox/kaudiofilepermissionserror)
- [var kAudioFileNotOptimizedError: OSStatus](/documentation/audiotoolbox/kaudiofilenotoptimizederror)
- [var kAudioFileInvalidChunkError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidchunkerror)
- [var kAudioFileDoesNotAllow64BitDataSizeError: OSStatus](/documentation/audiotoolbox/kaudiofiledoesnotallow64bitdatasizeerror)
- [var kAudioFileInvalidPacketOffsetError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidpacketoffseterror)
- [var kAudioFileInvalidFileError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidfileerror)
- [var kAudioFileOperationNotSupportedError: OSStatus](/documentation/audiotoolbox/kaudiofileoperationnotsupportederror)
- [var kAudioFileNotOpenError: OSStatus](/documentation/audiotoolbox/kaudiofilenotopenerror)
- [var kAudioFileEndOfFileError: OSStatus](/documentation/audiotoolbox/kaudiofileendoffileerror)
- [var kAudioFilePositionError: OSStatus](/documentation/audiotoolbox/kaudiofilepositionerror)
- [var kAudioFileFileNotFoundError: OSStatus](/documentation/audiotoolbox/kaudiofilefilenotfounderror)
- [Extended Audio File Services](/documentation/audiotoolbox/extended-audio-file-services)

### Managing Extended Audio File Objects

- [func ExtAudioFileCreateWithURL(CFURL, AudioFileTypeID, UnsafePointer<AudioStreamBasicDescription>, UnsafePointer<AudioChannelLayout>?, UInt32, UnsafeMutablePointer<ExtAudioFileRef?>) -> OSStatus](/documentation/audiotoolbox/extaudiofilecreatewithurl(_:_:_:_:_:_:))
- [func ExtAudioFileDispose(ExtAudioFileRef) -> OSStatus](/documentation/audiotoolbox/extaudiofiledispose(_:))
- [func ExtAudioFileOpenURL(CFURL, UnsafeMutablePointer<ExtAudioFileRef?>) -> OSStatus](/documentation/audiotoolbox/extaudiofileopenurl(_:_:))
- [func ExtAudioFileWrapAudioFileID(AudioFileID, Bool, UnsafeMutablePointer<ExtAudioFileRef?>) -> OSStatus](/documentation/audiotoolbox/extaudiofilewrapaudiofileid(_:_:_:))

### Configuring Properties for Extended Audio File Objects

- [func ExtAudioFileGetProperty(ExtAudioFileRef, ExtAudioFilePropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/extaudiofilegetproperty(_:_:_:_:))
- [func ExtAudioFileGetPropertyInfo(ExtAudioFileRef, ExtAudioFilePropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/extaudiofilegetpropertyinfo(_:_:_:_:))
- [func ExtAudioFileSetProperty(ExtAudioFileRef, ExtAudioFilePropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/extaudiofilesetproperty(_:_:_:_:))

### Reading and Writing Audio Data

- [func ExtAudioFileRead(ExtAudioFileRef, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/extaudiofileread(_:_:_:))
- [func ExtAudioFileSeek(ExtAudioFileRef, Int64) -> OSStatus](/documentation/audiotoolbox/extaudiofileseek(_:_:))
- [func ExtAudioFileTell(ExtAudioFileRef, UnsafeMutablePointer<Int64>) -> OSStatus](/documentation/audiotoolbox/extaudiofiletell(_:_:))
- [func ExtAudioFileWrite(ExtAudioFileRef, UInt32, UnsafePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/extaudiofilewrite(_:_:_:))
- [func ExtAudioFileWriteAsync(ExtAudioFileRef, UInt32, UnsafePointer<AudioBufferList>?) -> OSStatus](/documentation/audiotoolbox/extaudiofilewriteasync(_:_:_:))

### Data Types

- [ExtAudioFilePacketTableInfoOverride](/documentation/audiotoolbox/extaudiofilepackettableinfooverride)
- [ExtAudioFileRef](/documentation/audiotoolbox/extaudiofileref)
- [ExtAudioFilePropertyID](/documentation/audiotoolbox/extaudiofilepropertyid)

### Constants

- [Extended Audio FIle Errors](/documentation/audiotoolbox/1486883-extended-audio-file-errors)

#### Constants

- [var kExtAudioFileError_AsyncWriteBufferOverflow: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_asyncwritebufferoverflow)
- [var kExtAudioFileError_AsyncWriteTooLarge: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_asyncwritetoolarge)
- [var kExtAudioFileError_InvalidChannelMap: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidchannelmap)
- [var kExtAudioFileError_InvalidDataFormat: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invaliddataformat)
- [var kExtAudioFileError_InvalidOperationOrder: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidoperationorder)
- [var kExtAudioFileError_InvalidProperty: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidproperty)
- [var kExtAudioFileError_InvalidPropertySize: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidpropertysize)
- [var kExtAudioFileError_InvalidSeek: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidseek)
- [var kExtAudioFileError_MaxPacketSizeUnknown: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_maxpacketsizeunknown)
- [var kExtAudioFileError_NonPCMClientFormat: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_nonpcmclientformat)
- [Codec Unavailable Errors](/documentation/audiotoolbox/1623673-codec-unavailable-errors)

#### Constants

- [var kExtAudioFileError_CodecUnavailableInputConsumed: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_codecunavailableinputconsumed)
- [var kExtAudioFileError_CodecUnavailableInputNotConsumed: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_codecunavailableinputnotconsumed)
- [Property Identifiers for Extended Audio File Objects](/documentation/audiotoolbox/1486859-property-identifiers-for-extende)

#### Constants

- [var kExtAudioFileProperty_FileDataFormat: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_filedataformat)
- [var kExtAudioFileProperty_FileChannelLayout: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_filechannellayout)
- [var kExtAudioFileProperty_ClientDataFormat: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_clientdataformat)
- [var kExtAudioFileProperty_ClientChannelLayout: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_clientchannellayout)
- [var kExtAudioFileProperty_CodecManufacturer: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_codecmanufacturer)
- [var kExtAudioFileProperty_AudioConverter: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_audioconverter)
- [var kExtAudioFileProperty_AudioFile: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_audiofile)
- [var kExtAudioFileProperty_FileMaxPacketSize: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_filemaxpacketsize)
- [var kExtAudioFileProperty_ClientMaxPacketSize: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_clientmaxpacketsize)
- [var kExtAudioFileProperty_FileLengthFrames: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_filelengthframes)
- [var kExtAudioFileProperty_ConverterConfig: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_converterconfig)
- [var kExtAudioFileProperty_IOBufferSizeBytes: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_iobuffersizebytes)
- [var kExtAudioFileProperty_IOBuffer: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_iobuffer)
- [var kExtAudioFileProperty_PacketTable: ExtAudioFilePropertyID](/documentation/audiotoolbox/kextaudiofileproperty_packettable)
- [Extended Audio File Packet Overrides](/documentation/audiotoolbox/3547074-extended-audio-file-packet-overr)

#### Constants

- [var kExtAudioFilePacketTableInfoOverride_UseFileValue: ExtAudioFilePacketTableInfoOverride](/documentation/audiotoolbox/kextaudiofilepackettableinfooverride_usefilevalue)
- [var kExtAudioFilePacketTableInfoOverride_UseFileValueIfValid: ExtAudioFilePacketTableInfoOverride](/documentation/audiotoolbox/kextaudiofilepackettableinfooverride_usefilevalueifvalid)

### Result Codes

- [var kExtAudioFileError_CodecUnavailableInputConsumed: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_codecunavailableinputconsumed)
- [var kExtAudioFileError_CodecUnavailableInputNotConsumed: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_codecunavailableinputnotconsumed)
- [var kExtAudioFileError_InvalidProperty: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidproperty)
- [var kExtAudioFileError_InvalidPropertySize: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidpropertysize)
- [var kExtAudioFileError_NonPCMClientFormat: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_nonpcmclientformat)
- [var kExtAudioFileError_InvalidChannelMap: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidchannelmap)
- [var kExtAudioFileError_InvalidOperationOrder: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidoperationorder)
- [var kExtAudioFileError_InvalidDataFormat: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invaliddataformat)
- [var kExtAudioFileError_MaxPacketSizeUnknown: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_maxpacketsizeunknown)
- [var kExtAudioFileError_InvalidSeek: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_invalidseek)
- [var kExtAudioFileError_AsyncWriteTooLarge: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_asyncwritetoolarge)
- [var kExtAudioFileError_AsyncWriteBufferOverflow: OSStatus](/documentation/audiotoolbox/kextaudiofileerror_asyncwritebufferoverflow)
- [Audio File Stream Services](/documentation/audiotoolbox/audio-file-stream-services)

### Opening Audio File Streams

- [func AudioFileStreamOpen(UnsafeMutableRawPointer?, AudioFileStream_PropertyListenerProc, AudioFileStream_PacketsProc, AudioFileTypeID, UnsafeMutablePointer<AudioFileStreamID?>) -> OSStatus](/documentation/audiotoolbox/audiofilestreamopen(_:_:_:_:_:))

### Supplying Data to the Parser

- [func AudioFileStreamParseBytes(AudioFileStreamID, UInt32, UnsafeRawPointer?, AudioFileStreamParseFlags) -> OSStatus](/documentation/audiotoolbox/audiofilestreamparsebytes(_:_:_:_:))

### Seeking Packets in the Data Stream

- [func AudioFileStreamSeek(AudioFileStreamID, Int64, UnsafeMutablePointer<Int64>, UnsafeMutablePointer<AudioFileStreamSeekFlags>) -> OSStatus](/documentation/audiotoolbox/audiofilestreamseek(_:_:_:_:))

### Working with Data Stream Property Information

- [func AudioFileStreamGetPropertyInfo(AudioFileStreamID, AudioFileStreamPropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audiofilestreamgetpropertyinfo(_:_:_:_:))
- [func AudioFileStreamGetProperty(AudioFileStreamID, AudioFileStreamPropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilestreamgetproperty(_:_:_:_:))
- [func AudioFileStreamSetProperty(AudioFileStreamID, AudioFileStreamPropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilestreamsetproperty(_:_:_:_:))

### Closing an Audio File Stream

- [func AudioFileStreamClose(AudioFileStreamID) -> OSStatus](/documentation/audiotoolbox/audiofilestreamclose(_:))

### Callbacks

- [AudioFileStream_PropertyListenerProc](/documentation/audiotoolbox/audiofilestream_propertylistenerproc)
- [AudioFileStream_PacketsProc](/documentation/audiotoolbox/audiofilestream_packetsproc)

### Data Types

- [AudioFileStreamPropertyID](/documentation/audiotoolbox/audiofilestreampropertyid)
- [AudioFileStreamID](/documentation/audiotoolbox/audiofilestreamid)

### Enumerations

- [Audio File Stream Errors](/documentation/audiotoolbox/1391572-audio-file-stream-errors)

#### Constants

- [var kAudioFileStreamError_BadPropertySize: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_badpropertysize)
- [var kAudioFileStreamError_DataUnavailable: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_dataunavailable)
- [var kAudioFileStreamError_DiscontinuityCantRecover: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_discontinuitycantrecover)
- [var kAudioFileStreamError_IllegalOperation: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_illegaloperation)
- [var kAudioFileStreamError_InvalidFile: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_invalidfile)
- [var kAudioFileStreamError_InvalidPacketOffset: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_invalidpacketoffset)
- [var kAudioFileStreamError_NotOptimized: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_notoptimized)
- [var kAudioFileStreamError_UnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unspecifiederror)
- [var kAudioFileStreamError_UnsupportedDataFormat: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupporteddataformat)
- [var kAudioFileStreamError_UnsupportedFileType: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupportedfiletype)
- [var kAudioFileStreamError_UnsupportedProperty: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupportedproperty)
- [var kAudioFileStreamError_ValueUnknown: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_valueunknown)
- [Audio File Types](/documentation/audiotoolbox/1576497-audio-file-types)

#### Constants

- [var kAudioFile3GP2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofile3gp2type)
- [var kAudioFile3GPType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofile3gptype)
- [var kAudioFileAAC_ADTSType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaac_adtstype)
- [var kAudioFileAC3Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileac3type)
- [var kAudioFileAIFCType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaifctype)
- [var kAudioFileAIFFType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileaifftype)
- [var kAudioFileAMRType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileamrtype)
- [var kAudioFileCAFType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilecaftype)
- [var kAudioFileM4AType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilem4atype)
- [var kAudioFileM4BType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilem4btype)
- [var kAudioFileMP1Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp1type)
- [var kAudioFileMP2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp2type)
- [var kAudioFileMP3Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilemp3type)
- [var kAudioFileMPEG4Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilempeg4type)
- [var kAudioFileNextType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilenexttype)
- [var kAudioFileSoundDesigner2Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilesounddesigner2type)
- [var kAudioFileWAVEType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilewavetype)
- [var kAudioFileBW64Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilebw64type)
- [var kAudioFileFLACType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofileflactype)
- [var kAudioFileLATMInLOASType: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilelatminloastype)
- [var kAudioFileRF64Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilerf64type)
- [var kAudioFileWave64Type: AudioFileTypeID](/documentation/audiotoolbox/kaudiofilewave64type)

### Constants

- [Audio File Stream Flags](/documentation/audiotoolbox/audio-file-stream-flags)

#### Constants

- [static var propertyIsCached: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/propertyiscached)
- [static var cacheProperty: AudioFileStreamPropertyFlags](/documentation/audiotoolbox/audiofilestreampropertyflags/cacheproperty)
- [static var discontinuity: AudioFileStreamParseFlags](/documentation/audiotoolbox/audiofilestreamparseflags/discontinuity)
- [static var offsetIsEstimated: AudioFileStreamSeekFlags](/documentation/audiotoolbox/audiofilestreamseekflags/offsetisestimated)
- [Audio File Stream Properties](/documentation/audiotoolbox/1391506-audio-file-stream-properties)

#### Constants

- [var kAudioFileStreamProperty_ReadyToProducePackets: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_readytoproducepackets)
- [var kAudioFileStreamProperty_FileFormat: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_fileformat)
- [var kAudioFileStreamProperty_DataFormat: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_dataformat)
- [var kAudioFileStreamProperty_FormatList: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_formatlist)
- [var kAudioFileStreamProperty_MagicCookieData: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_magiccookiedata)
- [var kAudioFileStreamProperty_AudioDataByteCount: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_audiodatabytecount)
- [var kAudioFileStreamProperty_AudioDataPacketCount: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_audiodatapacketcount)
- [var kAudioFileStreamProperty_MaximumPacketSize: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_maximumpacketsize)
- [var kAudioFileStreamProperty_DataOffset: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_dataoffset)
- [var kAudioFileStreamProperty_ChannelLayout: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_channellayout)
- [var kAudioFileStreamProperty_PacketToFrame: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packettoframe)
- [var kAudioFileStreamProperty_FrameToPacket: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_frametopacket)
- [var kAudioFileStreamProperty_PacketToByte: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packettobyte)
- [var kAudioFileStreamProperty_ByteToPacket: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_bytetopacket)
- [var kAudioFileStreamProperty_PacketTableInfo: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packettableinfo)
- [var kAudioFileStreamProperty_PacketSizeUpperBound: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packetsizeupperbound)
- [var kAudioFileStreamProperty_AverageBytesPerPacket: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_averagebytesperpacket)
- [var kAudioFileStreamProperty_BitRate: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_bitrate)
- [var kAudioFileStreamProperty_InfoDictionary: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_infodictionary)
- [var kAudioFileStreamProperty_NextIndependentPacket: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_nextindependentpacket)
- [var kAudioFileStreamProperty_PacketToDependencyInfo: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packettodependencyinfo)
- [var kAudioFileStreamProperty_PacketToRollDistance: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_packettorolldistance)
- [var kAudioFileStreamProperty_PreviousIndependentPacket: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_previousindependentpacket)
- [var kAudioFileStreamProperty_RestrictsRandomAccess: AudioFileStreamPropertyID](/documentation/audiotoolbox/kaudiofilestreamproperty_restrictsrandomaccess)

### Result Codes

- [Audio File Errors](/documentation/audiotoolbox/1576500-audio-file-errors)

#### Constants

- [var kAudioFileBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudiofilebadpropertysizeerror)
- [var kAudioFileDoesNotAllow64BitDataSizeError: OSStatus](/documentation/audiotoolbox/kaudiofiledoesnotallow64bitdatasizeerror)
- [var kAudioFileEndOfFileError: OSStatus](/documentation/audiotoolbox/kaudiofileendoffileerror)
- [var kAudioFileFileNotFoundError: OSStatus](/documentation/audiotoolbox/kaudiofilefilenotfounderror)
- [var kAudioFileInvalidChunkError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidchunkerror)
- [var kAudioFileInvalidFileError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidfileerror)
- [var kAudioFileInvalidPacketOffsetError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidpacketoffseterror)
- [var kAudioFileNotOpenError: OSStatus](/documentation/audiotoolbox/kaudiofilenotopenerror)
- [var kAudioFileNotOptimizedError: OSStatus](/documentation/audiotoolbox/kaudiofilenotoptimizederror)
- [var kAudioFileOperationNotSupportedError: OSStatus](/documentation/audiotoolbox/kaudiofileoperationnotsupportederror)
- [var kAudioFilePermissionsError: OSStatus](/documentation/audiotoolbox/kaudiofilepermissionserror)
- [var kAudioFilePositionError: OSStatus](/documentation/audiotoolbox/kaudiofilepositionerror)
- [var kAudioFileUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudiofileunspecifiederror)
- [var kAudioFileUnsupportedDataFormatError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupporteddataformaterror)
- [var kAudioFileUnsupportedFileTypeError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupportedfiletypeerror)
- [var kAudioFileUnsupportedPropertyError: OSStatus](/documentation/audiotoolbox/kaudiofileunsupportedpropertyerror)
- [var kAudioFileInvalidPacketDependencyError: OSStatus](/documentation/audiotoolbox/kaudiofileinvalidpacketdependencyerror)
- [var kAudioFileStreamError_UnsupportedFileType: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupportedfiletype)
- [var kAudioFileStreamError_UnsupportedDataFormat: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupporteddataformat)
- [var kAudioFileStreamError_UnsupportedProperty: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unsupportedproperty)
- [var kAudioFileStreamError_BadPropertySize: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_badpropertysize)
- [var kAudioFileStreamError_NotOptimized: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_notoptimized)
- [var kAudioFileStreamError_InvalidPacketOffset: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_invalidpacketoffset)
- [var kAudioFileStreamError_InvalidFile: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_invalidfile)
- [var kAudioFileStreamError_ValueUnknown: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_valueunknown)
- [var kAudioFileStreamError_DataUnavailable: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_dataunavailable)
- [var kAudioFileStreamError_IllegalOperation: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_illegaloperation)
- [var kAudioFileStreamError_UnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_unspecifiederror)
- [var kAudioFileStreamError_DiscontinuityCantRecover: OSStatus](/documentation/audiotoolbox/kaudiofilestreamerror_discontinuitycantrecover)
- [Audio File Components](/documentation/audiotoolbox/audio-file-components)

### Opening and Closing Audio Files

- [func AudioFileComponentCreateURL(AudioFileComponent, CFURL, UnsafePointer<AudioStreamBasicDescription>, UInt32) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentcreateurl(_:_:_:_:))
- [func AudioFileComponentOpenURL(AudioFileComponent, CFURL, Int8, Int32) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentopenurl(_:_:_:_:))
- [func AudioFileComponentOpenWithCallbacks(AudioFileComponent, UnsafeMutableRawPointer, AudioFile_ReadProc, AudioFile_WriteProc, AudioFile_GetSizeProc, AudioFile_SetSizeProc) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentopenwithcallbacks(_:_:_:_:_:_:))
- [func AudioFileComponentCloseFile(AudioFileComponent) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentclosefile(_:))
- [func AudioFileComponentOptimize(AudioFileComponent) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentoptimize(_:))
- [AudioFileComponent](/documentation/audiotoolbox/audiofilecomponent)
- [AudioFileComponentPropertyID](/documentation/audiotoolbox/audiofilecomponentpropertyid)
- [AudioFileComponentCreateURLProc](/documentation/audiotoolbox/audiofilecomponentcreateurlproc)
- [AudioFileComponentOpenWithCallbacksProc](/documentation/audiotoolbox/audiofilecomponentopenwithcallbacksproc)
- [AudioFileComponentOpenURLProc](/documentation/audiotoolbox/audiofilecomponentopenurlproc)
- [AudioFileComponentCloseProc](/documentation/audiotoolbox/audiofilecomponentcloseproc)
- [AudioFileComponentOptimizeProc](/documentation/audiotoolbox/audiofilecomponentoptimizeproc)

### Configuring the Callbacks

- [func AudioFileComponentInitializeWithCallbacks(AudioFileComponent, UnsafeMutableRawPointer, AudioFile_ReadProc, AudioFile_WriteProc, AudioFile_GetSizeProc, AudioFile_SetSizeProc, UInt32, UnsafePointer<AudioStreamBasicDescription>, UInt32) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentinitializewithcallbacks(_:_:_:_:_:_:_:_:_:))
- [Audio File Component Selectors](/documentation/audiotoolbox/1404047-audio-file-component-selectors)

#### Selectors

- [var kAudioFileCloseSelect: Int](/documentation/audiotoolbox/kaudiofilecloseselect)
- [var kAudioFileCountUserDataSelect: Int](/documentation/audiotoolbox/kaudiofilecountuserdataselect)
- [var kAudioFileCreateSelect: Int](/documentation/audiotoolbox/kaudiofilecreateselect)
- [var kAudioFileCreateURLSelect: Int](/documentation/audiotoolbox/kaudiofilecreateurlselect)
- [var kAudioFileDataIsThisFormatSelect: Int](/documentation/audiotoolbox/kaudiofiledataisthisformatselect)
- [var kAudioFileExtensionIsThisFormatSelect: Int](/documentation/audiotoolbox/kaudiofileextensionisthisformatselect)
- [var kAudioFileFileDataIsThisFormatSelect: Int](/documentation/audiotoolbox/kaudiofilefiledataisthisformatselect)
- [var kAudioFileFileIsThisFormatSelect: Int](/documentation/audiotoolbox/kaudiofilefileisthisformatselect)
- [var kAudioFileGetGlobalInfoSelect: Int](/documentation/audiotoolbox/kaudiofilegetglobalinfoselect)
- [var kAudioFileGetGlobalInfoSizeSelect: Int](/documentation/audiotoolbox/kaudiofilegetglobalinfosizeselect)
- [var kAudioFileGetPropertyInfoSelect: Int](/documentation/audiotoolbox/kaudiofilegetpropertyinfoselect)
- [var kAudioFileGetUserDataAtOffsetSelect: Int](/documentation/audiotoolbox/kaudiofilegetuserdataatoffsetselect)
- [var kAudioFileGetUserDataSize64Select: Int](/documentation/audiotoolbox/kaudiofilegetuserdatasize64select)
- [var kAudioFileGetPropertySelect: Int](/documentation/audiotoolbox/kaudiofilegetpropertyselect)
- [var kAudioFileGetUserDataSelect: Int](/documentation/audiotoolbox/kaudiofilegetuserdataselect)
- [var kAudioFileGetUserDataSizeSelect: Int](/documentation/audiotoolbox/kaudiofilegetuserdatasizeselect)
- [var kAudioFileInitializeSelect: Int](/documentation/audiotoolbox/kaudiofileinitializeselect)
- [var kAudioFileInitializeWithCallbacksSelect: Int](/documentation/audiotoolbox/kaudiofileinitializewithcallbacksselect)
- [var kAudioFileOpenSelect: Int](/documentation/audiotoolbox/kaudiofileopenselect)
- [var kAudioFileOpenURLSelect: Int](/documentation/audiotoolbox/kaudiofileopenurlselect)
- [var kAudioFileOpenWithCallbacksSelect: Int](/documentation/audiotoolbox/kaudiofileopenwithcallbacksselect)
- [var kAudioFileOptimizeSelect: Int](/documentation/audiotoolbox/kaudiofileoptimizeselect)
- [var kAudioFileReadBytesSelect: Int](/documentation/audiotoolbox/kaudiofilereadbytesselect)
- [var kAudioFileReadPacketDataSelect: Int](/documentation/audiotoolbox/kaudiofilereadpacketdataselect)
- [var kAudioFileReadPacketsSelect: Int](/documentation/audiotoolbox/kaudiofilereadpacketsselect)
- [var kAudioFileRemoveUserDataSelect: Int](/documentation/audiotoolbox/kaudiofileremoveuserdataselect)
- [var kAudioFileSetPropertySelect: Int](/documentation/audiotoolbox/kaudiofilesetpropertyselect)
- [var kAudioFileSetUserDataSelect: Int](/documentation/audiotoolbox/kaudiofilesetuserdataselect)
- [var kAudioFileWriteBytesSelect: Int](/documentation/audiotoolbox/kaudiofilewritebytesselect)
- [var kAudioFileWritePacketsSelect: Int](/documentation/audiotoolbox/kaudiofilewritepacketsselect)
- [AudioFileComponentInitializeWithCallbacksProc](/documentation/audiotoolbox/audiofilecomponentinitializewithcallbacksproc)

### Getting the Global Information

- [func AudioFileComponentGetGlobalInfo(AudioFileComponent, AudioFileComponentPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetglobalinfo(_:_:_:_:_:_:))
- [func AudioFileComponentGetGlobalInfoSize(AudioFileComponent, AudioFileComponentPropertyID, UInt32, UnsafeRawPointer?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetglobalinfosize(_:_:_:_:_:))
- [AudioFileComponentGetGlobalInfoProc](/documentation/audiotoolbox/audiofilecomponentgetglobalinfoproc)
- [AudioFileComponentGetGlobalInfoSizeProc](/documentation/audiotoolbox/audiofilecomponentgetglobalinfosizeproc)

### Accessing the User Data

- [func AudioFileComponentGetUserData(AudioFileComponent, UInt32, UInt32, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetuserdata(_:_:_:_:_:))
- [func AudioFileComponentSetUserData(AudioFileComponent, UInt32, UInt32, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentsetuserdata(_:_:_:_:_:))
- [func AudioFileComponentCountUserData(AudioFileComponent, UInt32, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentcountuserdata(_:_:_:))
- [func AudioFileComponentGetUserDataSize(AudioFileComponent, UInt32, UInt32, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetuserdatasize(_:_:_:_:))
- [func AudioFileComponentRemoveUserData(AudioFileComponent, UInt32, UInt32) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentremoveuserdata(_:_:_:))
- [AudioFileComponentCountUserDataProc](/documentation/audiotoolbox/audiofilecomponentcountuserdataproc)
- [AudioFileComponentGetUserDataProc](/documentation/audiotoolbox/audiofilecomponentgetuserdataproc)
- [AudioFileComponentGetUserDataSizeProc](/documentation/audiotoolbox/audiofilecomponentgetuserdatasizeproc)
- [AudioFileComponentRemoveUserDataProc](/documentation/audiotoolbox/audiofilecomponentremoveuserdataproc)
- [AudioFileComponentSetUserDataProc](/documentation/audiotoolbox/audiofilecomponentsetuserdataproc)
- [CountUserDataFDF](/documentation/audiotoolbox/countuserdatafdf)
- [GetUserDataFDF](/documentation/audiotoolbox/getuserdatafdf)
- [GetUserDataSizeFDF](/documentation/audiotoolbox/getuserdatasizefdf)

### Accessing Properties

- [func AudioFileComponentGetProperty(AudioFileComponent, AudioFileComponentPropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetproperty(_:_:_:_:))
- [func AudioFileComponentGetPropertyInfo(AudioFileComponent, AudioFileComponentPropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<UInt32>?) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetpropertyinfo(_:_:_:_:))
- [func AudioFileComponentSetProperty(AudioFileComponent, AudioFileComponentPropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentsetproperty(_:_:_:_:))
- [AudioFileComponentGetPropertyInfoProc](/documentation/audiotoolbox/audiofilecomponentgetpropertyinfoproc)
- [AudioFileComponentGetPropertyProc](/documentation/audiotoolbox/audiofilecomponentgetpropertyproc)
- [AudioFileComponentSetPropertyProc](/documentation/audiotoolbox/audiofilecomponentsetpropertyproc)
- [Audio File Component Specific Properties](/documentation/audiotoolbox/1404186-audio-file-component-specific-pr)

#### Constants

- [var kAudioFileComponent_AvailableFormatIDs: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_availableformatids)
- [var kAudioFileComponent_AvailableStreamDescriptionsForFormat: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_availablestreamdescriptionsforformat)
- [var kAudioFileComponent_CanRead: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_canread)
- [var kAudioFileComponent_CanWrite: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_canwrite)
- [var kAudioFileComponent_ExtensionsForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_extensionsfortype)
- [var kAudioFileComponent_FastDispatchTable: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_fastdispatchtable)
- [var kAudioFileComponent_FileTypeName: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_filetypename)
- [var kAudioFileComponent_HFSTypeCodesForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_hfstypecodesfortype)
- [var kAudioFileComponent_MIMETypesForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_mimetypesfortype)
- [var kAudioFileComponent_UTIsForType: AudioFilePropertyID](/documentation/audiotoolbox/kaudiofilecomponent_utisfortype)

### Reading and Writing Data

- [func AudioFileComponentReadBytes(AudioFileComponent, Bool, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentreadbytes(_:_:_:_:_:))
- [func AudioFileComponentReadPacketData(AudioFileComponent, Bool, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentreadpacketdata(_:_:_:_:_:_:_:))
- [func AudioFileComponentReadPackets(AudioFileComponent, Bool, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentreadpackets(_:_:_:_:_:_:_:))
- [func AudioFileComponentWriteBytes(AudioFileComponent, Bool, Int64, UnsafeMutablePointer<UInt32>, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentwritebytes(_:_:_:_:_:))
- [func AudioFileComponentWritePackets(AudioFileComponent, Bool, UInt32, UnsafePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentwritepackets(_:_:_:_:_:_:_:))
- [AudioFileComponentReadBytesProc](/documentation/audiotoolbox/audiofilecomponentreadbytesproc)
- [AudioFileComponentReadPacketDataProc](/documentation/audiotoolbox/audiofilecomponentreadpacketdataproc)
- [AudioFileComponentReadPacketsProc](/documentation/audiotoolbox/audiofilecomponentreadpacketsproc)
- [AudioFileComponentWriteBytesProc](/documentation/audiotoolbox/audiofilecomponentwritebytesproc)
- [AudioFileComponentWritePacketsProc](/documentation/audiotoolbox/audiofilecomponentwritepacketsproc)

### Checking the File Format

- [func AudioFileComponentFileDataIsThisFormat(AudioFileComponent, UInt32, UnsafeRawPointer, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentfiledataisthisformat(_:_:_:_:))
- [func AudioFileComponentExtensionIsThisFormat(AudioFileComponent, CFString, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentextensionisthisformat(_:_:_:))
- [AudioFileComponentExtensionIsThisFormatProc](/documentation/audiotoolbox/audiofilecomponentextensionisthisformatproc)
- [AudioFileComponentFileDataIsThisFormatProc](/documentation/audiotoolbox/audiofilecomponentfiledataisthisformatproc)
- [GetPropertyFDF](/documentation/audiotoolbox/getpropertyfdf)
- [GetPropertyInfoFDF](/documentation/audiotoolbox/getpropertyinfofdf)
- [Core Audio File Format](/documentation/audiotoolbox/core-audio-file-format)

### File Structure

- [CAFAudioDescription](/documentation/audiotoolbox/cafaudiodescription)

#### Initializers

- [init()](/documentation/audiotoolbox/cafaudiodescription/init())
- [init(mSampleRate: Float64, mFormatID: UInt32, mFormatFlags: CAFFormatFlags, mBytesPerPacket: UInt32, mFramesPerPacket: UInt32, mChannelsPerFrame: UInt32, mBitsPerChannel: UInt32)](/documentation/audiotoolbox/cafaudiodescription/init(msamplerate:mformatid:mformatflags:mbytesperpacket:mframesperpacket:mchannelsperframe:mbitsperchannel:))

#### Instance Properties

- [var mBitsPerChannel: UInt32](/documentation/audiotoolbox/cafaudiodescription/mbitsperchannel)
- [var mBytesPerPacket: UInt32](/documentation/audiotoolbox/cafaudiodescription/mbytesperpacket)
- [var mChannelsPerFrame: UInt32](/documentation/audiotoolbox/cafaudiodescription/mchannelsperframe)
- [var mFormatFlags: CAFFormatFlags](/documentation/audiotoolbox/cafaudiodescription/mformatflags)
- [var mFormatID: UInt32](/documentation/audiotoolbox/cafaudiodescription/mformatid)
- [var mFramesPerPacket: UInt32](/documentation/audiotoolbox/cafaudiodescription/mframesperpacket)
- [var mSampleRate: Float64](/documentation/audiotoolbox/cafaudiodescription/msamplerate)
- [CAFAudioFormatListItem](/documentation/audiotoolbox/cafaudioformatlistitem)

#### Instance Properties

- [var mChannelLayoutTag: UInt32](/documentation/audiotoolbox/cafaudioformatlistitem/mchannellayouttag)
- [var mFormat: CAFAudioDescription](/documentation/audiotoolbox/cafaudioformatlistitem/mformat)

#### Initializers

- [init()](/documentation/audiotoolbox/cafaudioformatlistitem/init())
- [init(mFormat: CAFAudioDescription, mChannelLayoutTag: UInt32)](/documentation/audiotoolbox/cafaudioformatlistitem/init(mformat:mchannellayouttag:))
- [CAFChunkHeader](/documentation/audiotoolbox/cafchunkheader)

#### Initializers

- [init()](/documentation/audiotoolbox/cafchunkheader/init())
- [init(mChunkType: UInt32, mChunkSize: Int64)](/documentation/audiotoolbox/cafchunkheader/init(mchunktype:mchunksize:))

#### Instance Properties

- [var mChunkSize: Int64](/documentation/audiotoolbox/cafchunkheader/mchunksize)
- [var mChunkType: UInt32](/documentation/audiotoolbox/cafchunkheader/mchunktype)
- [CAFDataChunk](/documentation/audiotoolbox/cafdatachunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafdatachunk/init())
- [init(mEditCount: UInt32, mData: UInt8)](/documentation/audiotoolbox/cafdatachunk/init(meditcount:mdata:))

#### Instance Properties

- [var mData: UInt8](/documentation/audiotoolbox/cafdatachunk/mdata)
- [var mEditCount: UInt32](/documentation/audiotoolbox/cafdatachunk/meditcount)
- [CAFFileHeader](/documentation/audiotoolbox/caffileheader)

#### Initializers

- [init()](/documentation/audiotoolbox/caffileheader/init())
- [init(mFileType: UInt32, mFileVersion: UInt16, mFileFlags: UInt16)](/documentation/audiotoolbox/caffileheader/init(mfiletype:mfileversion:mfileflags:))

#### Instance Properties

- [var mFileFlags: UInt16](/documentation/audiotoolbox/caffileheader/mfileflags)
- [var mFileType: UInt32](/documentation/audiotoolbox/caffileheader/mfiletype)
- [var mFileVersion: UInt16](/documentation/audiotoolbox/caffileheader/mfileversion)
- [CAFFormatFlags](/documentation/audiotoolbox/cafformatflags)

#### Constants

- [static var linearPCMFormatFlagIsFloat: CAFFormatFlags](/documentation/audiotoolbox/cafformatflags/linearpcmformatflagisfloat)
- [static var linearPCMFormatFlagIsLittleEndian: CAFFormatFlags](/documentation/audiotoolbox/cafformatflags/linearpcmformatflagislittleendian)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/cafformatflags/init(rawvalue:))
- [CAFInfoStrings](/documentation/audiotoolbox/cafinfostrings)

#### Initializers

- [init()](/documentation/audiotoolbox/cafinfostrings/init())
- [init(mNumEntries: UInt32)](/documentation/audiotoolbox/cafinfostrings/init(mnumentries:))

#### Instance Properties

- [var mNumEntries: UInt32](/documentation/audiotoolbox/cafinfostrings/mnumentries)
- [CAFInstrumentChunk](/documentation/audiotoolbox/cafinstrumentchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafinstrumentchunk/init())
- [init(mBaseNote: Float32, mMIDILowNote: UInt8, mMIDIHighNote: UInt8, mMIDILowVelocity: UInt8, mMIDIHighVelocity: UInt8, mdBGain: Float32, mStartRegionID: UInt32, mSustainRegionID: UInt32, mReleaseRegionID: UInt32, mInstrumentID: UInt32)](/documentation/audiotoolbox/cafinstrumentchunk/init(mbasenote:mmidilownote:mmidihighnote:mmidilowvelocity:mmidihighvelocity:mdbgain:mstartregionid:msustainregionid:mreleaseregionid:minstrumentid:))

#### Instance Properties

- [var mBaseNote: Float32](/documentation/audiotoolbox/cafinstrumentchunk/mbasenote)
- [var mInstrumentID: UInt32](/documentation/audiotoolbox/cafinstrumentchunk/minstrumentid)
- [var mMIDIHighNote: UInt8](/documentation/audiotoolbox/cafinstrumentchunk/mmidihighnote)
- [var mMIDIHighVelocity: UInt8](/documentation/audiotoolbox/cafinstrumentchunk/mmidihighvelocity)
- [var mMIDILowNote: UInt8](/documentation/audiotoolbox/cafinstrumentchunk/mmidilownote)
- [var mMIDILowVelocity: UInt8](/documentation/audiotoolbox/cafinstrumentchunk/mmidilowvelocity)
- [var mReleaseRegionID: UInt32](/documentation/audiotoolbox/cafinstrumentchunk/mreleaseregionid)
- [var mStartRegionID: UInt32](/documentation/audiotoolbox/cafinstrumentchunk/mstartregionid)
- [var mSustainRegionID: UInt32](/documentation/audiotoolbox/cafinstrumentchunk/msustainregionid)
- [var mdBGain: Float32](/documentation/audiotoolbox/cafinstrumentchunk/mdbgain)
- [CAFMarker](/documentation/audiotoolbox/cafmarker)

#### Initializers

- [init()](/documentation/audiotoolbox/cafmarker/init())
- [init(mType: UInt32, mFramePosition: Float64, mMarkerID: UInt32, mSMPTETime: CAF_SMPTE_Time, mChannel: UInt32)](/documentation/audiotoolbox/cafmarker/init(mtype:mframeposition:mmarkerid:msmptetime:mchannel:))

#### Instance Properties

- [var mChannel: UInt32](/documentation/audiotoolbox/cafmarker/mchannel)
- [var mFramePosition: Float64](/documentation/audiotoolbox/cafmarker/mframeposition)
- [var mMarkerID: UInt32](/documentation/audiotoolbox/cafmarker/mmarkerid)
- [var mSMPTETime: CAF_SMPTE_Time](/documentation/audiotoolbox/cafmarker/msmptetime)
- [var mType: UInt32](/documentation/audiotoolbox/cafmarker/mtype)
- [CAFMarkerChunk](/documentation/audiotoolbox/cafmarkerchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafmarkerchunk/init())
- [init(mSMPTE_TimeType: UInt32, mNumberMarkers: UInt32, mMarkers: CAFMarker)](/documentation/audiotoolbox/cafmarkerchunk/init(msmpte_timetype:mnumbermarkers:mmarkers:))

#### Instance Properties

- [var mMarkers: CAFMarker](/documentation/audiotoolbox/cafmarkerchunk/mmarkers)
- [var mNumberMarkers: UInt32](/documentation/audiotoolbox/cafmarkerchunk/mnumbermarkers)
- [var mSMPTE_TimeType: UInt32](/documentation/audiotoolbox/cafmarkerchunk/msmpte_timetype)
- [CAFOverviewChunk](/documentation/audiotoolbox/cafoverviewchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafoverviewchunk/init())
- [init(mEditCount: UInt32, mNumFramesPerOVWSample: UInt32, mData: CAFOverviewSample)](/documentation/audiotoolbox/cafoverviewchunk/init(meditcount:mnumframesperovwsample:mdata:))

#### Instance Properties

- [var mData: CAFOverviewSample](/documentation/audiotoolbox/cafoverviewchunk/mdata)
- [var mEditCount: UInt32](/documentation/audiotoolbox/cafoverviewchunk/meditcount)
- [var mNumFramesPerOVWSample: UInt32](/documentation/audiotoolbox/cafoverviewchunk/mnumframesperovwsample)
- [CAFOverviewSample](/documentation/audiotoolbox/cafoverviewsample)

#### Initializers

- [init()](/documentation/audiotoolbox/cafoverviewsample/init())
- [init(mMinValue: Int16, mMaxValue: Int16)](/documentation/audiotoolbox/cafoverviewsample/init(mminvalue:mmaxvalue:))

#### Instance Properties

- [var mMaxValue: Int16](/documentation/audiotoolbox/cafoverviewsample/mmaxvalue)
- [var mMinValue: Int16](/documentation/audiotoolbox/cafoverviewsample/mminvalue)
- [CAFPacketTableHeader](/documentation/audiotoolbox/cafpackettableheader)

#### Initializers

- [init()](/documentation/audiotoolbox/cafpackettableheader/init())
- [init(mNumberPackets: Int64, mNumberValidFrames: Int64, mPrimingFrames: Int32, mRemainderFrames: Int32, mPacketDescriptions: UInt8)](/documentation/audiotoolbox/cafpackettableheader/init(mnumberpackets:mnumbervalidframes:mprimingframes:mremainderframes:mpacketdescriptions:))

#### Instance Properties

- [var mNumberPackets: Int64](/documentation/audiotoolbox/cafpackettableheader/mnumberpackets)
- [var mNumberValidFrames: Int64](/documentation/audiotoolbox/cafpackettableheader/mnumbervalidframes)
- [var mPacketDescriptions: UInt8](/documentation/audiotoolbox/cafpackettableheader/mpacketdescriptions)
- [var mPrimingFrames: Int32](/documentation/audiotoolbox/cafpackettableheader/mprimingframes)
- [var mRemainderFrames: Int32](/documentation/audiotoolbox/cafpackettableheader/mremainderframes)
- [CAFPeakChunk](/documentation/audiotoolbox/cafpeakchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafpeakchunk/init())
- [init(mEditCount: UInt32, mPeaks: CAFPositionPeak)](/documentation/audiotoolbox/cafpeakchunk/init(meditcount:mpeaks:))

#### Instance Properties

- [var mEditCount: UInt32](/documentation/audiotoolbox/cafpeakchunk/meditcount)
- [var mPeaks: CAFPositionPeak](/documentation/audiotoolbox/cafpeakchunk/mpeaks)
- [CAFPositionPeak](/documentation/audiotoolbox/cafpositionpeak)

#### Initializers

- [init()](/documentation/audiotoolbox/cafpositionpeak/init())
- [init(mValue: Float32, mFrameNumber: UInt64)](/documentation/audiotoolbox/cafpositionpeak/init(mvalue:mframenumber:))

#### Instance Properties

- [var mFrameNumber: UInt64](/documentation/audiotoolbox/cafpositionpeak/mframenumber)
- [var mValue: Float32](/documentation/audiotoolbox/cafpositionpeak/mvalue)
- [CAFRegion](/documentation/audiotoolbox/cafregion)

#### Initializers

- [init()](/documentation/audiotoolbox/cafregion/init())
- [init(mRegionID: UInt32, mFlags: CAFRegionFlags, mNumberMarkers: UInt32, mMarkers: CAFMarker)](/documentation/audiotoolbox/cafregion/init(mregionid:mflags:mnumbermarkers:mmarkers:))

#### Instance Properties

- [var mFlags: CAFRegionFlags](/documentation/audiotoolbox/cafregion/mflags)
- [var mMarkers: CAFMarker](/documentation/audiotoolbox/cafregion/mmarkers)
- [var mNumberMarkers: UInt32](/documentation/audiotoolbox/cafregion/mnumbermarkers)
- [var mRegionID: UInt32](/documentation/audiotoolbox/cafregion/mregionid)
- [CAFRegionChunk](/documentation/audiotoolbox/cafregionchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafregionchunk/init())
- [init(mSMPTE_TimeType: UInt32, mNumberRegions: UInt32, mRegions: CAFRegion)](/documentation/audiotoolbox/cafregionchunk/init(msmpte_timetype:mnumberregions:mregions:))

#### Instance Properties

- [var mNumberRegions: UInt32](/documentation/audiotoolbox/cafregionchunk/mnumberregions)
- [var mRegions: CAFRegion](/documentation/audiotoolbox/cafregionchunk/mregions)
- [var mSMPTE_TimeType: UInt32](/documentation/audiotoolbox/cafregionchunk/msmpte_timetype)
- [CAFRegionFlags](/documentation/audiotoolbox/cafregionflags)

#### Constants

- [static var loopEnable: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/loopenable)
- [static var playBackward: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/playbackward)
- [static var playForward: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/playforward)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/cafregionflags/init(rawvalue:))
- [CAFStringID](/documentation/audiotoolbox/cafstringid)

#### Initializers

- [init()](/documentation/audiotoolbox/cafstringid/init())
- [init(mStringID: UInt32, mStringStartByteOffset: Int64)](/documentation/audiotoolbox/cafstringid/init(mstringid:mstringstartbyteoffset:))

#### Instance Properties

- [var mStringID: UInt32](/documentation/audiotoolbox/cafstringid/mstringid)
- [var mStringStartByteOffset: Int64](/documentation/audiotoolbox/cafstringid/mstringstartbyteoffset)
- [CAFStrings](/documentation/audiotoolbox/cafstrings)

#### Initializers

- [init()](/documentation/audiotoolbox/cafstrings/init())
- [init(mNumEntries: UInt32, mStringsIDs: CAFStringID)](/documentation/audiotoolbox/cafstrings/init(mnumentries:mstringsids:))

#### Instance Properties

- [var mNumEntries: UInt32](/documentation/audiotoolbox/cafstrings/mnumentries)
- [var mStringsIDs: CAFStringID](/documentation/audiotoolbox/cafstrings/mstringsids)
- [CAFUMIDChunk](/documentation/audiotoolbox/cafumidchunk)

#### Initializers

- [init()](/documentation/audiotoolbox/cafumidchunk/init())
- [init(mBytes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/audiotoolbox/cafumidchunk/init(mbytes:))

#### Instance Properties

- [var mBytes: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/audiotoolbox/cafumidchunk/mbytes)
- [CAF_SMPTE_Time](/documentation/audiotoolbox/caf_smpte_time)

#### Initializers

- [init()](/documentation/audiotoolbox/caf_smpte_time/init())
- [init(mHours: Int8, mMinutes: Int8, mSeconds: Int8, mFrames: Int8, mSubFrameSampleOffset: UInt32)](/documentation/audiotoolbox/caf_smpte_time/init(mhours:mminutes:mseconds:mframes:msubframesampleoffset:))

#### Instance Properties

- [var mFrames: Int8](/documentation/audiotoolbox/caf_smpte_time/mframes)
- [var mHours: Int8](/documentation/audiotoolbox/caf_smpte_time/mhours)
- [var mMinutes: Int8](/documentation/audiotoolbox/caf_smpte_time/mminutes)
- [var mSeconds: Int8](/documentation/audiotoolbox/caf_smpte_time/mseconds)
- [var mSubFrameSampleOffset: UInt32](/documentation/audiotoolbox/caf_smpte_time/msubframesampleoffset)
- [CAF_UUID_ChunkHeader](/documentation/audiotoolbox/caf_uuid_chunkheader)

#### Initializers

- [init()](/documentation/audiotoolbox/caf_uuid_chunkheader/init())
- [init(mHeader: CAFChunkHeader, mUUID: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8))](/documentation/audiotoolbox/caf_uuid_chunkheader/init(mheader:muuid:))

#### Instance Properties

- [var mHeader: CAFChunkHeader](/documentation/audiotoolbox/caf_uuid_chunkheader/mheader)
- [var mUUID: (UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8, UInt8)](/documentation/audiotoolbox/caf_uuid_chunkheader/muuid)

### Types

- [CAFFormatFlags](/documentation/audiotoolbox/cafformatflags)

#### Constants

- [static var linearPCMFormatFlagIsFloat: CAFFormatFlags](/documentation/audiotoolbox/cafformatflags/linearpcmformatflagisfloat)
- [static var linearPCMFormatFlagIsLittleEndian: CAFFormatFlags](/documentation/audiotoolbox/cafformatflags/linearpcmformatflagislittleendian)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/cafformatflags/init(rawvalue:))
- [CAFRegionFlags](/documentation/audiotoolbox/cafregionflags)

#### Constants

- [static var loopEnable: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/loopenable)
- [static var playBackward: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/playbackward)
- [static var playForward: CAFRegionFlags](/documentation/audiotoolbox/cafregionflags/playforward)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/cafregionflags/init(rawvalue:))
- [CAF File Chunk Types](/documentation/audiotoolbox/1547266-caf-file-chunk-types)

#### Constants

- [var kCAF_AudioDataChunkID: UInt32](/documentation/audiotoolbox/kcaf_audiodatachunkid)
- [var kCAF_ChannelLayoutChunkID: UInt32](/documentation/audiotoolbox/kcaf_channellayoutchunkid)
- [var kCAF_EditCommentsChunkID: UInt32](/documentation/audiotoolbox/kcaf_editcommentschunkid)
- [var kCAF_FillerChunkID: UInt32](/documentation/audiotoolbox/kcaf_fillerchunkid)
- [var kCAF_FormatListID: UInt32](/documentation/audiotoolbox/kcaf_formatlistid)
- [var kCAF_InfoStringsChunkID: UInt32](/documentation/audiotoolbox/kcaf_infostringschunkid)
- [var kCAF_InstrumentChunkID: UInt32](/documentation/audiotoolbox/kcaf_instrumentchunkid)
- [var kCAF_MIDIChunkID: UInt32](/documentation/audiotoolbox/kcaf_midichunkid)
- [var kCAF_MagicCookieID: UInt32](/documentation/audiotoolbox/kcaf_magiccookieid)
- [var kCAF_MarkerChunkID: UInt32](/documentation/audiotoolbox/kcaf_markerchunkid)
- [var kCAF_OverviewChunkID: UInt32](/documentation/audiotoolbox/kcaf_overviewchunkid)
- [var kCAF_PacketTableChunkID: UInt32](/documentation/audiotoolbox/kcaf_packettablechunkid)
- [var kCAF_PeakChunkID: UInt32](/documentation/audiotoolbox/kcaf_peakchunkid)
- [var kCAF_RegionChunkID: UInt32](/documentation/audiotoolbox/kcaf_regionchunkid)
- [var kCAF_StreamDescriptionChunkID: UInt32](/documentation/audiotoolbox/kcaf_streamdescriptionchunkid)
- [var kCAF_StringsChunkID: UInt32](/documentation/audiotoolbox/kcaf_stringschunkid)
- [var kCAF_UMIDChunkID: UInt32](/documentation/audiotoolbox/kcaf_umidchunkid)
- [var kCAF_UUIDChunkID: UInt32](/documentation/audiotoolbox/kcaf_uuidchunkid)
- [var kCAF_iXMLChunkID: UInt32](/documentation/audiotoolbox/kcaf_ixmlchunkid)
- [CAF File Marker Types](/documentation/audiotoolbox/1547272-caf-file-marker-types)

#### Constants

- [var kCAFMarkerType_EditDestinationBegin: UInt32](/documentation/audiotoolbox/kcafmarkertype_editdestinationbegin)
- [var kCAFMarkerType_EditDestinationEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_editdestinationend)
- [var kCAFMarkerType_EditSourceBegin: UInt32](/documentation/audiotoolbox/kcafmarkertype_editsourcebegin)
- [var kCAFMarkerType_EditSourceEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_editsourceend)
- [var kCAFMarkerType_Generic: UInt32](/documentation/audiotoolbox/kcafmarkertype_generic)
- [var kCAFMarkerType_Index: UInt32](/documentation/audiotoolbox/kcafmarkertype_index)
- [var kCAFMarkerType_KeySignature: UInt32](/documentation/audiotoolbox/kcafmarkertype_keysignature)
- [var kCAFMarkerType_ProgramEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_programend)
- [var kCAFMarkerType_ProgramStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_programstart)
- [var kCAFMarkerType_RegionEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_regionend)
- [var kCAFMarkerType_RegionStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_regionstart)
- [var kCAFMarkerType_RegionSyncPoint: UInt32](/documentation/audiotoolbox/kcafmarkertype_regionsyncpoint)
- [var kCAFMarkerType_ReleaseLoopEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_releaseloopend)
- [var kCAFMarkerType_ReleaseLoopStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_releaseloopstart)
- [var kCAFMarkerType_SavedPlayPosition: UInt32](/documentation/audiotoolbox/kcafmarkertype_savedplayposition)
- [var kCAFMarkerType_SelectionEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_selectionend)
- [var kCAFMarkerType_SelectionStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_selectionstart)
- [var kCAFMarkerType_SustainLoopEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_sustainloopend)
- [var kCAFMarkerType_SustainLoopStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_sustainloopstart)
- [var kCAFMarkerType_Tempo: UInt32](/documentation/audiotoolbox/kcafmarkertype_tempo)
- [var kCAFMarkerType_TimeSignature: UInt32](/documentation/audiotoolbox/kcafmarkertype_timesignature)
- [var kCAFMarkerType_TrackEnd: UInt32](/documentation/audiotoolbox/kcafmarkertype_trackend)
- [var kCAFMarkerType_TrackStart: UInt32](/documentation/audiotoolbox/kcafmarkertype_trackstart)
- [CAF File SMPTE Time Types](/documentation/audiotoolbox/1547262-caf-file-smpte-time-types)

#### Constants

- [var kCAF_SMPTE_TimeType2398: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype2398)
- [var kCAF_SMPTE_TimeType24: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype24)
- [var kCAF_SMPTE_TimeType25: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype25)
- [var kCAF_SMPTE_TimeType2997: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype2997)
- [var kCAF_SMPTE_TimeType2997Drop: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype2997drop)
- [var kCAF_SMPTE_TimeType30: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype30)
- [var kCAF_SMPTE_TimeType30Drop: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype30drop)
- [var kCAF_SMPTE_TimeType50: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype50)
- [var kCAF_SMPTE_TimeType5994: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype5994)
- [var kCAF_SMPTE_TimeType5994Drop: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype5994drop)
- [var kCAF_SMPTE_TimeType60: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype60)
- [var kCAF_SMPTE_TimeType60Drop: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetype60drop)
- [var kCAF_SMPTE_TimeTypeNone: UInt32](/documentation/audiotoolbox/kcaf_smpte_timetypenone)
- [CAF File Header](/documentation/audiotoolbox/1547255-caf-file-header)

#### Constants

- [var kCAF_FileType: UInt32](/documentation/audiotoolbox/kcaf_filetype)
- [var kCAF_FileVersion_Initial: UInt32](/documentation/audiotoolbox/kcaf_fileversion_initial)

## Utilities

- [Analyzing audio performance with Instruments](/documentation/audiotoolbox/analyzing-audio-performance-with-instruments)
- [Audio Converter Services](/documentation/audiotoolbox/audio-converter-services)

### Managing Audio Converter Objects

- [func AudioConverterNew(UnsafePointer<AudioStreamBasicDescription>, UnsafePointer<AudioStreamBasicDescription>, UnsafeMutablePointer<AudioConverterRef?>) -> OSStatus](/documentation/audiotoolbox/audioconverternew(_:_:_:))
- [func AudioConverterNewSpecific(UnsafePointer<AudioStreamBasicDescription>, UnsafePointer<AudioStreamBasicDescription>, UInt32, UnsafePointer<AudioClassDescription>, UnsafeMutablePointer<AudioConverterRef?>) -> OSStatus](/documentation/audiotoolbox/audioconverternewspecific(_:_:_:_:_:))
- [func AudioConverterReset(AudioConverterRef) -> OSStatus](/documentation/audiotoolbox/audioconverterreset(_:))
- [func AudioConverterDispose(AudioConverterRef) -> OSStatus](/documentation/audiotoolbox/audioconverterdispose(_:))

### Configuring Audio Converter Properties

- [func AudioConverterGetProperty(AudioConverterRef, AudioConverterPropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audioconvertergetproperty(_:_:_:_:))
- [func AudioConverterGetPropertyInfo(AudioConverterRef, AudioConverterPropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audioconvertergetpropertyinfo(_:_:_:_:))
- [func AudioConverterSetProperty(AudioConverterRef, AudioConverterPropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audioconvertersetproperty(_:_:_:_:))

### Performing Conversions

- [Encoding and decoding audio](/documentation/audiotoolbox/encoding-and-decoding-audio)
- [func AudioConverterConvertBuffer(AudioConverterRef, UInt32, UnsafeRawPointer, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audioconverterconvertbuffer(_:_:_:_:_:))
- [func AudioConverterFillComplexBuffer(AudioConverterRef, AudioConverterComplexInputDataProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioBufferList>, UnsafeMutablePointer<AudioStreamPacketDescription>?) -> OSStatus](/documentation/audiotoolbox/audioconverterfillcomplexbuffer(_:_:_:_:_:_:))
- [func AudioConverterConvertComplexBuffer(AudioConverterRef, UInt32, UnsafePointer<AudioBufferList>, UnsafeMutablePointer<AudioBufferList>) -> OSStatus](/documentation/audiotoolbox/audioconverterconvertcomplexbuffer(_:_:_:_:))

### Callbacks

- [AudioConverterComplexInputDataProc](/documentation/audiotoolbox/audioconvertercomplexinputdataproc)
- [AudioConverterInputDataProc](/documentation/audiotoolbox/audioconverterinputdataproc)

### Data Types

- [AudioConverterPrimeInfo](/documentation/audiotoolbox/audioconverterprimeinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audioconverterprimeinfo/init())
- [init(leadingFrames: UInt32, trailingFrames: UInt32)](/documentation/audiotoolbox/audioconverterprimeinfo/init(leadingframes:trailingframes:))

#### Instance Properties

- [var leadingFrames: UInt32](/documentation/audiotoolbox/audioconverterprimeinfo/leadingframes)
- [var trailingFrames: UInt32](/documentation/audiotoolbox/audioconverterprimeinfo/trailingframes)
- [AudioConverterRef](/documentation/audiotoolbox/audioconverterref)
- [AudioConverterPropertyID](/documentation/audiotoolbox/audioconverterpropertyid)

### Constants

- [Audio Converter Properties](/documentation/audiotoolbox/1559928-audio-converter-properties)

#### Constants

- [var kAudioConverterPropertyMinimumInputBufferSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyminimuminputbuffersize)
- [var kAudioConverterPropertyMinimumOutputBufferSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyminimumoutputbuffersize)
- [var kAudioConverterPropertyMaximumInputBufferSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertymaximuminputbuffersize)
- [var kAudioConverterPropertyMaximumInputPacketSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertymaximuminputpacketsize)
- [var kAudioConverterPropertyMaximumOutputPacketSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertymaximumoutputpacketsize)
- [var kAudioConverterPropertyCalculateInputBufferSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertycalculateinputbuffersize)
- [var kAudioConverterPropertyCalculateOutputBufferSize: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertycalculateoutputbuffersize)
- [var kAudioConverterPropertyInputCodecParameters: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyinputcodecparameters)
- [var kAudioConverterPropertyOutputCodecParameters: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyoutputcodecparameters)
- [var kAudioConverterSampleRateConverterAlgorithm: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertersamplerateconverteralgorithm)
- [var kAudioConverterSampleRateConverterComplexity: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertersamplerateconvertercomplexity)
- [var kAudioConverterSampleRateConverterQuality: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertersamplerateconverterquality)
- [var kAudioConverterSampleRateConverterInitialPhase: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertersamplerateconverterinitialphase)
- [var kAudioConverterCodecQuality: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertercodecquality)
- [var kAudioConverterPrimeMethod: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterprimemethod)
- [var kAudioConverterPrimeInfo: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterprimeinfo)
- [var kAudioConverterChannelMap: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterchannelmap)
- [var kAudioConverterDecompressionMagicCookie: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterdecompressionmagiccookie)
- [var kAudioConverterCompressionMagicCookie: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertercompressionmagiccookie)
- [var kAudioConverterEncodeBitRate: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterencodebitrate)
- [var kAudioConverterEncodeAdjustableSampleRate: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterencodeadjustablesamplerate)
- [var kAudioConverterInputChannelLayout: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterinputchannellayout)
- [var kAudioConverterOutputChannelLayout: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverteroutputchannellayout)
- [var kAudioConverterApplicableEncodeBitRates: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterapplicableencodebitrates)
- [var kAudioConverterAvailableEncodeBitRates: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverteravailableencodebitrates)
- [var kAudioConverterApplicableEncodeSampleRates: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterapplicableencodesamplerates)
- [var kAudioConverterAvailableEncodeSampleRates: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverteravailableencodesamplerates)
- [var kAudioConverterAvailableEncodeChannelLayoutTags: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverteravailableencodechannellayouttags)
- [var kAudioConverterCurrentOutputStreamDescription: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertercurrentoutputstreamdescription)
- [var kAudioConverterCurrentInputStreamDescription: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconvertercurrentinputstreamdescription)
- [var kAudioConverterPropertySettings: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertysettings)
- [var kAudioConverterPropertyBitDepthHint: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertybitdepthhint)
- [var kAudioConverterPropertyFormatList: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyformatlist)
- [var kAudioConverterPropertyCanResumeFromInterruption: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertycanresumefrominterruption)
- [Converter Priming Constants](/documentation/audiotoolbox/1559927-converter-priming-constants)

#### Constants

- [var kConverterPrimeMethod_Pre: UInt32](/documentation/audiotoolbox/kconverterprimemethod_pre)
- [var kConverterPrimeMethod_Normal: UInt32](/documentation/audiotoolbox/kconverterprimemethod_normal)
- [var kConverterPrimeMethod_None: UInt32](/documentation/audiotoolbox/kconverterprimemethod_none)
- [Sample Rate Conversion Quality Identifiers](/documentation/audiotoolbox/1559924-sample-rate-conversion-quality-i)

#### Constants

- [var kAudioConverterQuality_Max: UInt32](/documentation/audiotoolbox/kaudioconverterquality_max)
- [var kAudioConverterQuality_High: UInt32](/documentation/audiotoolbox/kaudioconverterquality_high)
- [var kAudioConverterQuality_Medium: UInt32](/documentation/audiotoolbox/kaudioconverterquality_medium)
- [var kAudioConverterQuality_Low: UInt32](/documentation/audiotoolbox/kaudioconverterquality_low)
- [var kAudioConverterQuality_Min: UInt32](/documentation/audiotoolbox/kaudioconverterquality_min)
- [Sample Rate Conversion Complexity Identifiers](/documentation/audiotoolbox/1559923-sample-rate-conversion-complexit)

#### Constants

- [var kAudioConverterSampleRateConverterComplexity_Linear: UInt32](/documentation/audiotoolbox/kaudioconvertersamplerateconvertercomplexity_linear)
- [var kAudioConverterSampleRateConverterComplexity_Normal: UInt32](/documentation/audiotoolbox/kaudioconvertersamplerateconvertercomplexity_normal)
- [var kAudioConverterSampleRateConverterComplexity_Mastering: UInt32](/documentation/audiotoolbox/kaudioconvertersamplerateconvertercomplexity_mastering)
- [var kAudioConverterSampleRateConverterComplexity_MinimumPhase: UInt32](/documentation/audiotoolbox/kaudioconvertersamplerateconvertercomplexity_minimumphase)

### Enumerations

- [Converter Audio Unit Properties](/documentation/audiotoolbox/1533972-converter_audio_unit_properties)

#### Constants

- [var kAudioUnitProperty_SampleRateConverterComplexity: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_samplerateconvertercomplexity)
- [Converter Audio Unit Subtypes](/documentation/audiotoolbox/1584145-converter_audio_unit_subtypes)

#### Constants

- [var kAudioUnitSubType_AUConverter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auconverter)
- [var kAudioUnitSubType_AUiPodTimeOther: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auipodtimeother)
- [var kAudioUnitSubType_DeferredRenderer: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_deferredrenderer)
- [var kAudioUnitSubType_Merger: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_merger)
- [var kAudioUnitSubType_MultiSplitter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_multisplitter)
- [var kAudioUnitSubType_NewTimePitch: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_newtimepitch)
- [var kAudioUnitSubType_RoundTripAAC: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_roundtripaac)
- [var kAudioUnitSubType_Splitter: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_splitter)
- [var kAudioUnitSubType_Varispeed: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_varispeed)
- [Audio Converter Dithering Algorithms](/documentation/audiotoolbox/1559931-audio-converter-dithering-algori)

#### Constants

- [var kDitherAlgorithm_NoiseShaping: UInt32](/documentation/audiotoolbox/kditheralgorithm_noiseshaping)
- [var kDitherAlgorithm_TPDF: UInt32](/documentation/audiotoolbox/kditheralgorithm_tpdf)
- [Audio Converter Properties (macOS)](/documentation/audiotoolbox/1559925-audio-converter-properties-macos)

#### Constants

- [var kAudioConverterPropertyDitherBitDepth: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyditherbitdepth)
- [var kAudioConverterPropertyDithering: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertydithering)
- [Audio Converter Errors](/documentation/audiotoolbox/1559930-audio-converter-errors)

#### Constants

- [var kAudioConverterErr_BadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_badpropertysizeerror)
- [var kAudioConverterErr_FormatNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_formatnotsupported)
- [var kAudioConverterErr_HardwareInUse: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_hardwareinuse)
- [var kAudioConverterErr_InputSampleRateOutOfRange: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_inputsamplerateoutofrange)
- [var kAudioConverterErr_InvalidInputSize: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_invalidinputsize)
- [var kAudioConverterErr_InvalidOutputSize: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_invalidoutputsize)
- [var kAudioConverterErr_NoHardwarePermission: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_nohardwarepermission)
- [var kAudioConverterErr_OperationNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_operationnotsupported)
- [var kAudioConverterErr_OutputSampleRateOutOfRange: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_outputsamplerateoutofrange)
- [var kAudioConverterErr_PropertyNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_propertynotsupported)
- [var kAudioConverterErr_RequiresPacketDescriptionsError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_requirespacketdescriptionserror)
- [var kAudioConverterErr_UnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_unspecifiederror)

### Result Codes

- [var kAudioConverterErr_FormatNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_formatnotsupported)
- [var kAudioConverterErr_OperationNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_operationnotsupported)
- [var kAudioConverterErr_PropertyNotSupported: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_propertynotsupported)
- [var kAudioConverterErr_InvalidInputSize: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_invalidinputsize)
- [var kAudioConverterErr_InvalidOutputSize: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_invalidoutputsize)
- [var kAudioConverterErr_UnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_unspecifiederror)
- [var kAudioConverterErr_BadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_badpropertysizeerror)
- [var kAudioConverterErr_RequiresPacketDescriptionsError: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_requirespacketdescriptionserror)
- [var kAudioConverterErr_InputSampleRateOutOfRange: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_inputsamplerateoutofrange)
- [var kAudioConverterErr_OutputSampleRateOutOfRange: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_outputsamplerateoutofrange)
- [var kAudioConverterErr_HardwareInUse: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_hardwareinuse)
- [var kAudioConverterErr_NoHardwarePermission: OSStatus](/documentation/audiotoolbox/kaudioconvertererr_nohardwarepermission)
- [Audio Session Support](/documentation/audiotoolbox/audio-session-support)

### Audio Session Support

- [Audio Session Property Identifiers](/documentation/audiotoolbox/1618455-audio-session-property-identifie)

#### Constants

- [var kAudioSessionProperty_PreferredHardwareSampleRate: Int](/documentation/audiotoolbox/kaudiosessionproperty_preferredhardwaresamplerate)
- [var kAudioSessionProperty_PreferredHardwareIOBufferDuration: Int](/documentation/audiotoolbox/kaudiosessionproperty_preferredhardwareiobufferduration)
- [var kAudioSessionProperty_AudioCategory: Int](/documentation/audiotoolbox/kaudiosessionproperty_audiocategory)
- [var kAudioSessionProperty_AudioRouteChange: Int](/documentation/audiotoolbox/kaudiosessionproperty_audioroutechange)
- [var kAudioSessionProperty_CurrentHardwareSampleRate: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwaresamplerate)
- [var kAudioSessionProperty_CurrentHardwareInputNumberChannels: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareinputnumberchannels)
- [var kAudioSessionProperty_CurrentHardwareOutputNumberChannels: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareoutputnumberchannels)
- [var kAudioSessionProperty_CurrentHardwareOutputVolume: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareoutputvolume)
- [var kAudioSessionProperty_CurrentHardwareInputLatency: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareinputlatency)
- [var kAudioSessionProperty_CurrentHardwareOutputLatency: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareoutputlatency)
- [var kAudioSessionProperty_CurrentHardwareIOBufferDuration: Int](/documentation/audiotoolbox/kaudiosessionproperty_currenthardwareiobufferduration)
- [var kAudioSessionProperty_OtherAudioIsPlaying: Int](/documentation/audiotoolbox/kaudiosessionproperty_otheraudioisplaying)
- [var kAudioSessionProperty_OverrideAudioRoute: Int](/documentation/audiotoolbox/kaudiosessionproperty_overrideaudioroute)
- [var kAudioSessionProperty_AudioInputAvailable: Int](/documentation/audiotoolbox/kaudiosessionproperty_audioinputavailable)
- [var kAudioSessionProperty_ServerDied: Int](/documentation/audiotoolbox/kaudiosessionproperty_serverdied)
- [var kAudioSessionProperty_OtherMixableAudioShouldDuck: Int](/documentation/audiotoolbox/kaudiosessionproperty_othermixableaudioshouldduck)
- [var kAudioSessionProperty_OverrideCategoryMixWithOthers: Int](/documentation/audiotoolbox/kaudiosessionproperty_overridecategorymixwithothers)
- [var kAudioSessionProperty_OverrideCategoryDefaultToSpeaker: Int](/documentation/audiotoolbox/kaudiosessionproperty_overridecategorydefaulttospeaker)
- [var kAudioSessionProperty_OverrideCategoryEnableBluetoothInput: Int](/documentation/audiotoolbox/kaudiosessionproperty_overridecategoryenablebluetoothinput)
- [var kAudioSessionProperty_InterruptionType: Int](/documentation/audiotoolbox/kaudiosessionproperty_interruptiontype)
- [var kAudioSessionProperty_Mode: Int](/documentation/audiotoolbox/kaudiosessionproperty_mode)
- [var kAudioSessionProperty_InputSources: Int](/documentation/audiotoolbox/kaudiosessionproperty_inputsources)
- [var kAudioSessionProperty_OutputDestinations: Int](/documentation/audiotoolbox/kaudiosessionproperty_outputdestinations)
- [var kAudioSessionProperty_InputSource: Int](/documentation/audiotoolbox/kaudiosessionproperty_inputsource)
- [var kAudioSessionProperty_OutputDestination: Int](/documentation/audiotoolbox/kaudiosessionproperty_outputdestination)
- [var kAudioSessionProperty_InputGainAvailable: Int](/documentation/audiotoolbox/kaudiosessionproperty_inputgainavailable)
- [var kAudioSessionProperty_InputGainScalar: Int](/documentation/audiotoolbox/kaudiosessionproperty_inputgainscalar)
- [var kAudioSessionProperty_AudioRouteDescription: Int](/documentation/audiotoolbox/kaudiosessionproperty_audioroutedescription)
- [Audio Session Categories](/documentation/audiotoolbox/1618427-audio-session-categories)

#### Constants

- [var kAudioSessionCategory_AmbientSound: Int](/documentation/audiotoolbox/kaudiosessioncategory_ambientsound)
- [var kAudioSessionCategory_SoloAmbientSound: Int](/documentation/audiotoolbox/kaudiosessioncategory_soloambientsound)
- [var kAudioSessionCategory_MediaPlayback: Int](/documentation/audiotoolbox/kaudiosessioncategory_mediaplayback)
- [var kAudioSessionCategory_RecordAudio: Int](/documentation/audiotoolbox/kaudiosessioncategory_recordaudio)
- [var kAudioSessionCategory_PlayAndRecord: Int](/documentation/audiotoolbox/kaudiosessioncategory_playandrecord)
- [var kAudioSessionCategory_AudioProcessing: Int](/documentation/audiotoolbox/kaudiosessioncategory_audioprocessing)
- [Audio Session Modes](/documentation/audiotoolbox/1618405-audio-session-modes)

#### Constants

- [var kAudioSessionMode_Default: Int](/documentation/audiotoolbox/kaudiosessionmode_default)
- [var kAudioSessionMode_VoiceChat: Int](/documentation/audiotoolbox/kaudiosessionmode_voicechat)
- [var kAudioSessionMode_VideoRecording: Int](/documentation/audiotoolbox/kaudiosessionmode_videorecording)
- [var kAudioSessionMode_Measurement: Int](/documentation/audiotoolbox/kaudiosessionmode_measurement)
- [var kAudioSessionMode_GameChat: Int](/documentation/audiotoolbox/kaudiosessionmode_gamechat)
- [Audio Session Category Route Overrides](/documentation/audiotoolbox/1618372-audio-session-category-route-ove)

#### Constants

- [var kAudioSessionOverrideAudioRoute_None: Int](/documentation/audiotoolbox/kaudiosessionoverrideaudioroute_none)
- [var kAudioSessionOverrideAudioRoute_Speaker: Int](/documentation/audiotoolbox/kaudiosessionoverrideaudioroute_speaker)
- [Audio Session Activation Flags](/documentation/audiotoolbox/1618357-audio-session-activation-flags)

#### Constants

- [var kAudioSessionSetActiveFlag_NotifyOthersOnDeactivation: Int](/documentation/audiotoolbox/kaudiosessionsetactiveflag_notifyothersondeactivation)
- [Audio Session Interruption States](/documentation/audiotoolbox/1618425-audio-session-interruption-state)

#### Constants

- [var kAudioSessionBeginInterruption: Int](/documentation/audiotoolbox/kaudiosessionbegininterruption)
- [var kAudioSessionEndInterruption: Int](/documentation/audiotoolbox/kaudiosessionendinterruption)
- [AudioSessionInterruptionType](/documentation/audiotoolbox/audiosessioninterruptiontype)

#### Constants

- [var kAudioSessionInterruptionType_ShouldResume: Int](/documentation/audiotoolbox/kaudiosessioninterruptiontype_shouldresume)
- [var kAudioSessionInterruptionType_ShouldNotResume: Int](/documentation/audiotoolbox/kaudiosessioninterruptiontype_shouldnotresume)

### Audio Routes

- [Audio Route Change Reasons](/documentation/audiotoolbox/1618380-audio-route-change-reasons)

#### Constants

- [var kAudioSessionRouteChangeReason_Unknown: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_unknown)
- [var kAudioSessionRouteChangeReason_NewDeviceAvailable: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_newdeviceavailable)
- [var kAudioSessionRouteChangeReason_OldDeviceUnavailable: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_olddeviceunavailable)
- [var kAudioSessionRouteChangeReason_CategoryChange: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_categorychange)
- [var kAudioSessionRouteChangeReason_Override: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_override)
- [var kAudioSessionRouteChangeReason_WakeFromSleep: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_wakefromsleep)
- [var kAudioSessionRouteChangeReason_NoSuitableRouteForCategory: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_nosuitablerouteforcategory)
- [var kAudioSessionRouteChangeReason_RouteConfigurationChange: Int](/documentation/audiotoolbox/kaudiosessionroutechangereason_routeconfigurationchange)
- [Audio Route Description Dictionary Keys](/documentation/audiotoolbox/audio-route-description-dictionary-keys)

#### Constants

- [let kAudioSession_AudioRouteKey_Inputs: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_inputs)
- [let kAudioSession_AudioRouteKey_Outputs: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_outputs)
- [Audio Route Type Key](/documentation/audiotoolbox/audio-route-type-key)

#### Constants

- [let kAudioSession_AudioRouteKey_Type: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_type)
- [Audio Input Routes](/documentation/audiotoolbox/audio-input-routes)

#### Constants

- [let kAudioSessionInputRoute_LineIn: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_linein)
- [let kAudioSessionInputRoute_BuiltInMic: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_builtinmic)
- [let kAudioSessionInputRoute_HeadsetMic: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_headsetmic)
- [let kAudioSessionInputRoute_BluetoothHFP: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_bluetoothhfp)
- [let kAudioSessionInputRoute_USBAudio: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_usbaudio)
- [Audio Output Routes](/documentation/audiotoolbox/audio-output-routes)

#### Constants

- [let kAudioSessionOutputRoute_LineOut: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_lineout)
- [let kAudioSessionOutputRoute_Headphones: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_headphones)
- [let kAudioSessionOutputRoute_BluetoothHFP: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_bluetoothhfp)
- [let kAudioSessionOutputRoute_BluetoothA2DP: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_bluetootha2dp)
- [let kAudioSessionOutputRoute_BuiltInReceiver: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_builtinreceiver)
- [let kAudioSessionOutputRoute_BuiltInSpeaker: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_builtinspeaker)
- [let kAudioSessionOutputRoute_USBAudio: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_usbaudio)
- [let kAudioSessionOutputRoute_HDMI: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_hdmi)
- [let kAudioSessionOutputRoute_AirPlay: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_airplay)
- [Audio Route Change Dictionary Keys](/documentation/audiotoolbox/audio-route-change-dictionary-keys)

#### Constants

- [let kAudioSession_RouteChangeKey_Reason: CFString!](/documentation/audiotoolbox/kaudiosession_routechangekey_reason)
- [let kAudioSession_AudioRouteChangeKey_PreviousRouteDescription: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_previousroutedescription)
- [let kAudioSession_AudioRouteChangeKey_CurrentRouteDescription: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_currentroutedescription)
- [Alternative Audio Route Change Reason Dictionary Key](/documentation/audiotoolbox/alternative-audio-route-change-reason-dictionary-key)

#### Constants

- [var kAudioSession_AudioRouteChangeKey_Reason: String](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_reason)

### USB Accessories

- [USB Accessory Audio Source Dictionary Keys](/documentation/audiotoolbox/usb-accessory-audio-source-dictionary-keys)

#### Constants

- [let kAudioSession_InputSourceKey_ID: CFString!](/documentation/audiotoolbox/kaudiosession_inputsourcekey_id)
- [let kAudioSession_InputSourceKey_Description: CFString!](/documentation/audiotoolbox/kaudiosession_inputsourcekey_description)
- [USB Accessory Audio Destination Dictionary Keys](/documentation/audiotoolbox/usb-accessory-audio-destination-dictionary-keys)

#### Constants

- [let kAudioSession_OutputDestinationKey_ID: CFString!](/documentation/audiotoolbox/kaudiosession_outputdestinationkey_id)
- [let kAudioSession_OutputDestinationKey_Description: CFString!](/documentation/audiotoolbox/kaudiosession_outputdestinationkey_description)

### Constants

- [let kAudioSessionInputRoute_BluetoothHFP: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_bluetoothhfp)
- [let kAudioSessionInputRoute_BuiltInMic: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_builtinmic)
- [let kAudioSessionInputRoute_HeadsetMic: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_headsetmic)
- [let kAudioSessionInputRoute_LineIn: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_linein)
- [let kAudioSessionInputRoute_USBAudio: CFString!](/documentation/audiotoolbox/kaudiosessioninputroute_usbaudio)
- [let kAudioSessionOutputRoute_AirPlay: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_airplay)
- [let kAudioSessionOutputRoute_BluetoothA2DP: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_bluetootha2dp)
- [let kAudioSessionOutputRoute_BluetoothHFP: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_bluetoothhfp)
- [let kAudioSessionOutputRoute_BuiltInReceiver: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_builtinreceiver)
- [let kAudioSessionOutputRoute_BuiltInSpeaker: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_builtinspeaker)
- [let kAudioSessionOutputRoute_HDMI: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_hdmi)
- [let kAudioSessionOutputRoute_Headphones: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_headphones)
- [let kAudioSessionOutputRoute_LineOut: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_lineout)
- [let kAudioSessionOutputRoute_USBAudio: CFString!](/documentation/audiotoolbox/kaudiosessionoutputroute_usbaudio)
- [let kAudioSession_AudioRouteChangeKey_CurrentRouteDescription: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_currentroutedescription)
- [let kAudioSession_AudioRouteChangeKey_PreviousRouteDescription: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_previousroutedescription)
- [let kAudioSession_AudioRouteKey_Inputs: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_inputs)
- [let kAudioSession_AudioRouteKey_Outputs: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_outputs)
- [let kAudioSession_AudioRouteKey_Type: CFString!](/documentation/audiotoolbox/kaudiosession_audioroutekey_type)
- [let kAudioSession_InputSourceKey_Description: CFString!](/documentation/audiotoolbox/kaudiosession_inputsourcekey_description)
- [let kAudioSession_InputSourceKey_ID: CFString!](/documentation/audiotoolbox/kaudiosession_inputsourcekey_id)
- [let kAudioSession_OutputDestinationKey_Description: CFString!](/documentation/audiotoolbox/kaudiosession_outputdestinationkey_description)
- [let kAudioSession_OutputDestinationKey_ID: CFString!](/documentation/audiotoolbox/kaudiosession_outputdestinationkey_id)
- [let kAudioSession_RouteChangeKey_Reason: CFString!](/documentation/audiotoolbox/kaudiosession_routechangekey_reason)

### Enumerations

- [Audio Session Interruption Types](/documentation/audiotoolbox/1618387-audio-session-interruption-types)

#### Constants

- [var kAudioSessionInterruptionType_ShouldNotResume: Int](/documentation/audiotoolbox/kaudiosessioninterruptiontype_shouldnotresume)
- [var kAudioSessionInterruptionType_ShouldResume: Int](/documentation/audiotoolbox/kaudiosessioninterruptiontype_shouldresume)

### Result Codes

- [Audio Session Errors](/documentation/audiotoolbox/1618373-audio-session-errors)

#### Constants

- [var kAudioSessionNoError: Int](/documentation/audiotoolbox/kaudiosessionnoerror)
- [var kAudioSessionNotInitialized: Int](/documentation/audiotoolbox/kaudiosessionnotinitialized)
- [var kAudioSessionAlreadyInitialized: Int](/documentation/audiotoolbox/kaudiosessionalreadyinitialized)
- [var kAudioSessionInitializationError: Int](/documentation/audiotoolbox/kaudiosessioninitializationerror)
- [var kAudioSessionUnsupportedPropertyError: Int](/documentation/audiotoolbox/kaudiosessionunsupportedpropertyerror)
- [var kAudioSessionBadPropertySizeError: Int](/documentation/audiotoolbox/kaudiosessionbadpropertysizeerror)
- [var kAudioSessionNotActiveError: Int](/documentation/audiotoolbox/kaudiosessionnotactiveerror)
- [var kAudioServicesNoHardwareError: Int](/documentation/audiotoolbox/kaudioservicesnohardwareerror)
- [var kAudioSessionNoCategorySet: Int](/documentation/audiotoolbox/kaudiosessionnocategoryset)
- [var kAudioSessionIncompatibleCategory: Int](/documentation/audiotoolbox/kaudiosessionincompatiblecategory)
- [var kAudioSessionUnspecifiedError: Int](/documentation/audiotoolbox/kaudiosessionunspecifiederror)
- [Audio Toolbox Debugging](/documentation/audiotoolbox/audio-toolbox-debugging)

### Audio Toolbox Debugging Functions

- [func CAShow(UnsafeMutableRawPointer)](/documentation/audiotoolbox/cashow(_:))
- [func CAShowFile(UnsafeMutableRawPointer, UnsafeMutablePointer<FILE>)](/documentation/audiotoolbox/cashowfile(_:_:))

### Instrument Functions

- [func CopyNameFromSoundBank(CFURL, UnsafeMutablePointer<Unmanaged<CFString>?>) -> OSStatus](/documentation/audiotoolbox/copynamefromsoundbank(_:_:))
- [func CopyInstrumentInfoFromSoundBank(CFURL, UnsafeMutablePointer<Unmanaged<CFArray>?>) -> OSStatus](/documentation/audiotoolbox/copyinstrumentinfofromsoundbank(_:_:))
- [var kInstrumentInfoKey_LSB: String](/documentation/audiotoolbox/kinstrumentinfokey_lsb)
- [var kInstrumentInfoKey_MSB: String](/documentation/audiotoolbox/kinstrumentinfokey_msb)
- [var kInstrumentInfoKey_Name: String](/documentation/audiotoolbox/kinstrumentinfokey_name)
- [var kInstrumentInfoKey_Program: String](/documentation/audiotoolbox/kinstrumentinfokey_program)

### Constants

- [var AUDIO_TOOLBOX_VERSION: Int32](/documentation/audiotoolbox/audio_toolbox_version)
- [Workgroup Management](/documentation/audiotoolbox/workgroup-management)

### Essentials

- [Understanding Audio Workgroups](/documentation/audiotoolbox/understanding-audio-workgroups)
- [Adding Parallel Real-Time Threads to Audio Workgroups](/documentation/audiotoolbox/adding-parallel-real-time-threads-to-audio-workgroups)
- [Adding Asynchronous Real-Time Threads to Audio Workgroups](/documentation/audiotoolbox/adding-asynchronous-real-time-threads-to-audio-workgroups)
- [Adding Audio Unit Auxiliary Real-Time Threads to Audio Workgroups](/documentation/audiotoolbox/adding-audio-unit-auxiliary-real-time-threads-to-audio-workgroups)

### Device Workgroup

- [var kAudioDevicePropertyIOThreadOSWorkgroup: AudioObjectPropertySelector](/documentation/coreaudio/kaudiodevicepropertyiothreadosworkgroup)
- [Audio Codec](/documentation/audiotoolbox/audio-codec)

### Initializing an Audio Codec

- [func AudioCodecInitialize(AudioCodec, UnsafePointer<AudioStreamBasicDescription>?, UnsafePointer<AudioStreamBasicDescription>?, UnsafeRawPointer?, UInt32) -> OSStatus](/documentation/audiotoolbox/audiocodecinitialize(_:_:_:_:_:))
- [func AudioCodecReset(AudioCodec) -> OSStatus](/documentation/audiotoolbox/audiocodecreset(_:))
- [func AudioCodecUninitialize(AudioCodec) -> OSStatus](/documentation/audiotoolbox/audiocodecuninitialize(_:))

### Configuring Buffers

- [func AudioCodecAppendInputBufferList(AudioCodec, UnsafePointer<AudioBufferList>, UnsafeMutablePointer<UInt32>, UnsafePointer<AudioStreamPacketDescription>?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiocodecappendinputbufferlist(_:_:_:_:_:))
- [func AudioCodecProduceOutputBufferList(AudioCodec, UnsafeMutablePointer<AudioBufferList>, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiocodecproduceoutputbufferlist(_:_:_:_:_:))

### Accessing the Data

- [func AudioCodecAppendInputData(AudioCodec, UnsafeRawPointer, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<UInt32>, UnsafePointer<AudioStreamPacketDescription>?) -> OSStatus](/documentation/audiotoolbox/audiocodecappendinputdata(_:_:_:_:_:))
- [func AudioCodecProduceOutputPackets(AudioCodec, UnsafeMutableRawPointer, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/audiocodecproduceoutputpackets(_:_:_:_:_:_:))

### Accessing Codec Properties

- [func AudioCodecGetProperty(AudioCodec, AudioCodecPropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiocodecgetproperty(_:_:_:_:))
- [func AudioCodecGetPropertyInfo(AudioCodec, AudioCodecPropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/audiocodecgetpropertyinfo(_:_:_:_:))
- [func AudioCodecSetProperty(AudioCodec, AudioCodecPropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiocodecsetproperty(_:_:_:_:))

### Codec Types

- [AudioCodecMagicCookieInfo](/documentation/audiotoolbox/audiocodecmagiccookieinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiocodecmagiccookieinfo/init())
- [init(mMagicCookieSize: UInt32, mMagicCookie: UnsafeRawPointer?)](/documentation/audiotoolbox/audiocodecmagiccookieinfo/init(mmagiccookiesize:mmagiccookie:))

#### Instance Properties

- [var mMagicCookie: UnsafeRawPointer?](/documentation/audiotoolbox/audiocodecmagiccookieinfo/mmagiccookie)
- [var mMagicCookieSize: UInt32](/documentation/audiotoolbox/audiocodecmagiccookieinfo/mmagiccookiesize)
- [AudioCodecPrimeInfo](/documentation/audiotoolbox/audiocodecprimeinfo)

#### Initializers

- [init()](/documentation/audiotoolbox/audiocodecprimeinfo/init())
- [init(leadingFrames: UInt32, trailingFrames: UInt32)](/documentation/audiotoolbox/audiocodecprimeinfo/init(leadingframes:trailingframes:))

#### Instance Properties

- [var leadingFrames: UInt32](/documentation/audiotoolbox/audiocodecprimeinfo/leadingframes)
- [var trailingFrames: UInt32](/documentation/audiotoolbox/audiocodecprimeinfo/trailingframes)
- [AudioCodec](/documentation/audiotoolbox/audiocodec)
- [AudioCodecAppendInputBufferListProc](/documentation/audiotoolbox/audiocodecappendinputbufferlistproc)
- [AudioCodecAppendInputDataProc](/documentation/audiotoolbox/audiocodecappendinputdataproc)
- [AudioCodecGetPropertyInfoProc](/documentation/audiotoolbox/audiocodecgetpropertyinfoproc)
- [AudioCodecGetPropertyProc](/documentation/audiotoolbox/audiocodecgetpropertyproc)
- [AudioCodecInitializeProc](/documentation/audiotoolbox/audiocodecinitializeproc)
- [AudioCodecProduceOutputBufferListProc](/documentation/audiotoolbox/audiocodecproduceoutputbufferlistproc)
- [AudioCodecProduceOutputPacketsProc](/documentation/audiotoolbox/audiocodecproduceoutputpacketsproc)
- [AudioCodecPropertyID](/documentation/audiotoolbox/audiocodecpropertyid)
- [AudioCodecResetProc](/documentation/audiotoolbox/audiocodecresetproc)
- [AudioCodecSetPropertyProc](/documentation/audiotoolbox/audiocodecsetpropertyproc)
- [AudioCodecUninitializeProc](/documentation/audiotoolbox/audiocodecuninitializeproc)

### Audio Settings

- [AudioSettingsFlags](/documentation/audiotoolbox/audiosettingsflags)

#### Constants

- [static var expertParameter: AudioSettingsFlags](/documentation/audiotoolbox/audiosettingsflags/expertparameter)
- [static var invisibleParameter: AudioSettingsFlags](/documentation/audiotoolbox/audiosettingsflags/invisibleparameter)
- [static var metaParameter: AudioSettingsFlags](/documentation/audiotoolbox/audiosettingsflags/metaparameter)
- [static var userInterfaceParameter: AudioSettingsFlags](/documentation/audiotoolbox/audiosettingsflags/userinterfaceparameter)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audiosettingsflags/init(rawvalue:))
- [var kAudioSettings_AvailableValues: String](/documentation/audiotoolbox/kaudiosettings_availablevalues)
- [var kAudioSettings_CurrentValue: String](/documentation/audiotoolbox/kaudiosettings_currentvalue)
- [var kAudioSettings_Hint: String](/documentation/audiotoolbox/kaudiosettings_hint)
- [var kAudioSettings_LimitedValues: String](/documentation/audiotoolbox/kaudiosettings_limitedvalues)
- [var kAudioSettings_Parameters: String](/documentation/audiotoolbox/kaudiosettings_parameters)
- [var kAudioSettings_SettingKey: String](/documentation/audiotoolbox/kaudiosettings_settingkey)
- [var kAudioSettings_SettingName: String](/documentation/audiotoolbox/kaudiosettings_settingname)
- [var kAudioSettings_Summary: String](/documentation/audiotoolbox/kaudiosettings_summary)
- [var kAudioSettings_TopLevelKey: String](/documentation/audiotoolbox/kaudiosettings_toplevelkey)
- [var kAudioSettings_Unit: String](/documentation/audiotoolbox/kaudiosettings_unit)
- [var kAudioSettings_ValueType: String](/documentation/audiotoolbox/kaudiosettings_valuetype)
- [var kAudioSettings_Version: String](/documentation/audiotoolbox/kaudiosettings_version)

### Enumerations

- [Output Status Constants](/documentation/audiotoolbox/1494122-output-status-constants)

#### Constants

- [var kAudioCodecProduceOutputPacketAtEOF: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketateof)
- [var kAudioCodecProduceOutputPacketFailure: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketfailure)
- [var kAudioCodecProduceOutputPacketNeedsMoreInputData: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketneedsmoreinputdata)
- [var kAudioCodecProduceOutputPacketSuccess: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketsuccess)
- [var kAudioCodecProduceOutputPacketSuccessHasMore: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketsuccesshasmore)
- [var kAudioCodecProduceOutputPacketSuccessConcealed: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputpacketsuccessconcealed)
- [Program Target Levels](/documentation/audiotoolbox/1494116-program-target-levels)

#### Constants

- [var kProgramTargetLevel_Minus20dB: UInt32](/documentation/audiotoolbox/kprogramtargetlevel_minus20db)
- [var kProgramTargetLevel_Minus23dB: UInt32](/documentation/audiotoolbox/kprogramtargetlevel_minus23db)
- [var kProgramTargetLevel_Minus31dB: UInt32](/documentation/audiotoolbox/kprogramtargetlevel_minus31db)
- [var kProgramTargetLevel_None: UInt32](/documentation/audiotoolbox/kprogramtargetlevel_none)
- [Dynamic Range Control Modes](/documentation/audiotoolbox/1494094-dynamic-range-control-modes)

#### Constants

- [var kDynamicRangeControlMode_Heavy: UInt32](/documentation/audiotoolbox/kdynamicrangecontrolmode_heavy)
- [var kDynamicRangeControlMode_Light: UInt32](/documentation/audiotoolbox/kdynamicrangecontrolmode_light)
- [var kDynamicRangeControlMode_None: UInt32](/documentation/audiotoolbox/kdynamicrangecontrolmode_none)
- [Bit Rate Control Mode Constants](/documentation/audiotoolbox/1494144-bit-rate-control-mode-constants)

#### Constants

- [var kAudioCodecBitRateControlMode_Constant: UInt32](/documentation/audiotoolbox/kaudiocodecbitratecontrolmode_constant)
- [var kAudioCodecBitRateControlMode_LongTermAverage: UInt32](/documentation/audiotoolbox/kaudiocodecbitratecontrolmode_longtermaverage)
- [var kAudioCodecBitRateControlMode_Variable: UInt32](/documentation/audiotoolbox/kaudiocodecbitratecontrolmode_variable)
- [var kAudioCodecBitRateControlMode_VariableConstrained: UInt32](/documentation/audiotoolbox/kaudiocodecbitratecontrolmode_variableconstrained)
- [Global Codec Properties](/documentation/audiotoolbox/1494121-global-codec-properties)

#### Constants

- [var kAudioCodecPropertyFormatCFString: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyformatcfstring)
- [var kAudioCodecPropertyManufacturerCFString: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertymanufacturercfstring)
- [var kAudioCodecPropertyNameCFString: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertynamecfstring)
- [Instance Codec Properties](/documentation/audiotoolbox/1494111-instance-codec-properties)

#### Constants

- [var kAudioCodecPropertyAdjustLocalQuality: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyadjustlocalquality)
- [var kAudioCodecPropertyApplicableBitRateRange: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyapplicablebitraterange)
- [var kAudioCodecPropertyApplicableInputSampleRates: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyapplicableinputsamplerates)
- [var kAudioCodecPropertyApplicableOutputSampleRates: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyapplicableoutputsamplerates)
- [var kAudioCodecPropertyBitRateControlMode: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertybitratecontrolmode)
- [var kAudioCodecPropertyCurrentInputChannelLayout: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentinputchannellayout)
- [var kAudioCodecPropertyCurrentInputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentinputformat)
- [var kAudioCodecPropertyCurrentInputSampleRate: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentinputsamplerate)
- [var kAudioCodecPropertyCurrentOutputChannelLayout: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentoutputchannellayout)
- [var kAudioCodecPropertyCurrentOutputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentoutputformat)
- [var kAudioCodecPropertyCurrentOutputSampleRate: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrentoutputsamplerate)
- [var kAudioCodecPropertyCurrentTargetBitRate: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycurrenttargetbitrate)
- [var kAudioCodecPropertyDelayMode: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertydelaymode)
- [var kAudioCodecPropertyDynamicRangeControlMode: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertydynamicrangecontrolmode)
- [var kAudioCodecPropertyFormatList: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyformatlist)
- [var kAudioCodecPropertyHasVariablePacketByteSizes: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyhasvariablepacketbytesizes)
- [var kAudioCodecPropertyInputBufferSize: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyinputbuffersize)
- [var kAudioCodecPropertyIsInitialized: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyisinitialized)
- [var kAudioCodecPropertyMagicCookie: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertymagiccookie)
- [var kAudioCodecPropertyMaximumPacketByteSize: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertymaximumpacketbytesize)
- [var kAudioCodecPropertyPacketFrameSize: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertypacketframesize)
- [var kAudioCodecPropertyPacketSizeLimitForVBR: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertypacketsizelimitforvbr)
- [var kAudioCodecPropertyPaddedZeros: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertypaddedzeros)
- [var kAudioCodecPropertyPrimeInfo: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyprimeinfo)
- [var kAudioCodecPropertyPrimeMethod: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyprimemethod)
- [var kAudioCodecPropertyProgramTargetLevel: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyprogramtargetlevel)
- [var kAudioCodecPropertyProgramTargetLevelConstant: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyprogramtargetlevelconstant)
- [var kAudioCodecPropertyQualitySetting: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyqualitysetting)
- [var kAudioCodecPropertyRecommendedBitRateRange: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyrecommendedbitraterange)
- [var kAudioCodecPropertySettings: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertysettings)
- [var kAudioCodecPropertySoundQualityForVBR: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertysoundqualityforvbr)
- [var kAudioCodecPropertyUsedInputBufferSize: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyusedinputbuffersize)
- [var kAudioCodecPropertyAdjustCompressionProfile: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyadjustcompressionprofile)
- [var kAudioCodecPropertyAdjustTargetLevel: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyadjusttargetlevel)
- [var kAudioCodecPropertyAdjustTargetLevelConstant: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyadjusttargetlevelconstant)
- [var kAudioCodecPropertyBitRateForVBR: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertybitrateforvbr)
- [var kAudioCodecPropertyEmploysDependentPackets: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyemploysdependentpackets)
- [Audio Codec Priming Method Constants](/documentation/audiotoolbox/1494154-audio-codec-priming-method-const)

#### Constants

- [var kAudioCodecPrimeMethod_None: UInt32](/documentation/audiotoolbox/kaudiocodecprimemethod_none)
- [var kAudioCodecPrimeMethod_Normal: UInt32](/documentation/audiotoolbox/kaudiocodecprimemethod_normal)
- [var kAudioCodecPrimeMethod_Pre: UInt32](/documentation/audiotoolbox/kaudiocodecprimemethod_pre)
- [Audio Codec Quality Constants](/documentation/audiotoolbox/1494130-audio-codec-quality-constants)

#### Constants

- [var kAudioCodecQuality_High: UInt32](/documentation/audiotoolbox/kaudiocodecquality_high)
- [var kAudioCodecQuality_Low: UInt32](/documentation/audiotoolbox/kaudiocodecquality_low)
- [var kAudioCodecQuality_Max: UInt32](/documentation/audiotoolbox/kaudiocodecquality_max)
- [var kAudioCodecQuality_Medium: UInt32](/documentation/audiotoolbox/kaudiocodecquality_medium)
- [var kAudioCodecQuality_Min: UInt32](/documentation/audiotoolbox/kaudiocodecquality_min)
- [Audio Codec Routine Selectors](/documentation/audiotoolbox/1494074-audio-codec-routine-selectors)

#### Constants

- [var kAudioCodecAppendInputBufferListSelect: UInt32](/documentation/audiotoolbox/kaudiocodecappendinputbufferlistselect)
- [var kAudioCodecAppendInputDataSelect: UInt32](/documentation/audiotoolbox/kaudiocodecappendinputdataselect)
- [var kAudioCodecGetPropertyInfoSelect: UInt32](/documentation/audiotoolbox/kaudiocodecgetpropertyinfoselect)
- [var kAudioCodecGetPropertySelect: UInt32](/documentation/audiotoolbox/kaudiocodecgetpropertyselect)
- [var kAudioCodecInitializeSelect: UInt32](/documentation/audiotoolbox/kaudiocodecinitializeselect)
- [var kAudioCodecProduceOutputBufferListSelect: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputbufferlistselect)
- [var kAudioCodecProduceOutputDataSelect: UInt32](/documentation/audiotoolbox/kaudiocodecproduceoutputdataselect)
- [var kAudioCodecResetSelect: UInt32](/documentation/audiotoolbox/kaudiocodecresetselect)
- [var kAudioCodecSetPropertySelect: UInt32](/documentation/audiotoolbox/kaudiocodecsetpropertyselect)
- [var kAudioCodecUninitializeSelect: UInt32](/documentation/audiotoolbox/kaudiocodecuninitializeselect)
- [Audio Codec Delays](/documentation/audiotoolbox/1494127-audio-codec-delays)

#### Constants

- [var kAudioCodecPropertyMinimumDelayMode: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyminimumdelaymode)
- [Audio Codec Delay Modes](/documentation/audiotoolbox/1494050-audio-codec-delay-modes)

#### Constants

- [var kAudioCodecDelayMode_Compatibility: UInt32](/documentation/audiotoolbox/kaudiocodecdelaymode_compatibility)
- [var kAudioCodecDelayMode_Minimum: UInt32](/documentation/audiotoolbox/kaudiocodecdelaymode_minimum)
- [var kAudioCodecDelayMode_Optimal: UInt32](/documentation/audiotoolbox/kaudiocodecdelaymode_optimal)
- [Audio Codec Properties](/documentation/audiotoolbox/1494068-audio-codec-properties)

#### Constants

- [var kAudioCodecPropertyAvailableBitRateRange: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailablebitraterange)
- [var kAudioCodecPropertyAvailableInputChannelLayoutTags: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableinputchannellayouttags)
- [var kAudioCodecPropertyAvailableInputSampleRates: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableinputsamplerates)
- [var kAudioCodecPropertyAvailableNumberChannels: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailablenumberchannels)
- [var kAudioCodecPropertyAvailableOutputChannelLayoutTags: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableoutputchannellayouttags)
- [var kAudioCodecPropertyAvailableOutputSampleRates: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableoutputsamplerates)
- [var kAudioCodecPropertyDoesSampleRateConversion: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertydoessamplerateconversion)
- [var kAudioCodecPropertyFormatInfo: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyformatinfo)
- [var kAudioCodecPropertyInputFormatsForOutputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyinputformatsforoutputformat)
- [var kAudioCodecPropertyMinimumNumberInputPackets: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyminimumnumberinputpackets)
- [var kAudioCodecPropertyMinimumNumberOutputPackets: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyminimumnumberoutputpackets)
- [var kAudioCodecPropertyOutputFormatsForInputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyoutputformatsforinputformat)
- [var kAudioCodecPropertySupportedInputFormats: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertysupportedinputformats)
- [var kAudioCodecPropertySupportedOutputFormats: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertysupportedoutputformats)
- [Audio Codec Errors](/documentation/audiotoolbox/1494076-audio-codec-errors)

#### Constants

- [var kAudioCodecBadPropertySizeError: OSStatus](/documentation/audiotoolbox/kaudiocodecbadpropertysizeerror)
- [var kAudioCodecIllegalOperationError: OSStatus](/documentation/audiotoolbox/kaudiocodecillegaloperationerror)
- [var kAudioCodecNoError: OSStatus](/documentation/audiotoolbox/kaudiocodecnoerror)
- [var kAudioCodecNotEnoughBufferSpaceError: OSStatus](/documentation/audiotoolbox/kaudiocodecnotenoughbufferspaceerror)
- [var kAudioCodecStateError: OSStatus](/documentation/audiotoolbox/kaudiocodecstateerror)
- [var kAudioCodecUnknownPropertyError: OSStatus](/documentation/audiotoolbox/kaudiocodecunknownpropertyerror)
- [var kAudioCodecUnspecifiedError: OSStatus](/documentation/audiotoolbox/kaudiocodecunspecifiederror)
- [var kAudioCodecUnsupportedFormatError: OSStatus](/documentation/audiotoolbox/kaudiocodecunsupportedformaterror)
- [var kAudioCodecBadDataError: OSStatus](/documentation/audiotoolbox/kaudiocodecbaddataerror)
- [Clock Utilities](/documentation/audiotoolbox/clock-utilities)

### Creating a Clock

- [func CAClockNew(UInt32, UnsafeMutablePointer<CAClockRef?>) -> OSStatus](/documentation/audiotoolbox/caclocknew(_:_:))
- [func CAClockDispose(CAClockRef) -> OSStatus](/documentation/audiotoolbox/caclockdispose(_:))
- [CAClockRef](/documentation/audiotoolbox/caclockref)

### Starting and Stopping the Clock

- [func CAClockStart(CAClockRef) -> OSStatus](/documentation/audiotoolbox/caclockstart(_:))
- [func CAClockStop(CAClockRef) -> OSStatus](/documentation/audiotoolbox/caclockstop(_:))
- [func CAClockArm(CAClockRef) -> OSStatus](/documentation/audiotoolbox/caclockarm(_:))
- [func CAClockDisarm(CAClockRef) -> OSStatus](/documentation/audiotoolbox/caclockdisarm(_:))

### Adding and Removing Listeners

- [func CAClockAddListener(CAClockRef, CAClockListenerProc, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/caclockaddlistener(_:_:_:))
- [func CAClockRemoveListener(CAClockRef, CAClockListenerProc, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/caclockremovelistener(_:_:_:))
- [CAClockListenerProc](/documentation/audiotoolbox/caclocklistenerproc)
- [CAClockMessage](/documentation/audiotoolbox/caclockmessage)

#### Constants

- [case armed](/documentation/audiotoolbox/caclockmessage/armed)
- [case disarmed](/documentation/audiotoolbox/caclockmessage/disarmed)
- [case propertyChanged](/documentation/audiotoolbox/caclockmessage/propertychanged)
- [case startTimeSet](/documentation/audiotoolbox/caclockmessage/starttimeset)
- [case started](/documentation/audiotoolbox/caclockmessage/started)
- [case stopped](/documentation/audiotoolbox/caclockmessage/stopped)
- [case wrongSMPTEFormat](/documentation/audiotoolbox/caclockmessage/wrongsmpteformat)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/caclockmessage/init(rawvalue:))

### Accessing the Current Time

- [func CAClockGetCurrentTime(CAClockRef, CAClockTimeFormat, UnsafeMutablePointer<CAClockTime>) -> OSStatus](/documentation/audiotoolbox/caclockgetcurrenttime(_:_:_:))
- [func CAClockSetCurrentTime(CAClockRef, UnsafePointer<CAClockTime>) -> OSStatus](/documentation/audiotoolbox/caclocksetcurrenttime(_:_:))
- [func CAClockGetStartTime(CAClockRef, CAClockTimeFormat, UnsafeMutablePointer<CAClockTime>) -> OSStatus](/documentation/audiotoolbox/caclockgetstarttime(_:_:_:))
- [CAClockTime](/documentation/audiotoolbox/caclocktime)

#### Initializers

- [init()](/documentation/audiotoolbox/caclocktime/init())
- [init(format: CAClockTimeFormat, reserved: UInt32, time: CAClockTime.__Unnamed_union_time)](/documentation/audiotoolbox/caclocktime/init(format:reserved:time:))

#### Instance Properties

- [var format: CAClockTimeFormat](/documentation/audiotoolbox/caclocktime/format)
- [var reserved: UInt32](/documentation/audiotoolbox/caclocktime/reserved)
- [var time: CAClockTime.__Unnamed_union_time](/documentation/audiotoolbox/caclocktime/time)
- [CAClockTimeFormat](/documentation/audiotoolbox/caclocktimeformat)

#### Constants

- [case absoluteSeconds](/documentation/audiotoolbox/caclocktimeformat/absoluteseconds)
- [case beats](/documentation/audiotoolbox/caclocktimeformat/beats)
- [case hostTime](/documentation/audiotoolbox/caclocktimeformat/hosttime)
- [case smpteSeconds](/documentation/audiotoolbox/caclocktimeformat/smpteseconds)
- [case smpteTime](/documentation/audiotoolbox/caclocktimeformat/smptetime)
- [case samples](/documentation/audiotoolbox/caclocktimeformat/samples)
- [case seconds](/documentation/audiotoolbox/caclocktimeformat/seconds)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/caclocktimeformat/init(rawvalue:))
- [CAClockSamples](/documentation/audiotoolbox/caclocksamples)

### Accessing Tempo Information

- [func CAClockGetCurrentTempo(CAClockRef, UnsafeMutablePointer<CAClockTempo>, UnsafeMutablePointer<CAClockTime>?) -> OSStatus](/documentation/audiotoolbox/caclockgetcurrenttempo(_:_:_:))
- [func CAClockSetCurrentTempo(CAClockRef, CAClockTempo, UnsafePointer<CAClockTime>?) -> OSStatus](/documentation/audiotoolbox/caclocksetcurrenttempo(_:_:_:))
- [func CAClockGetPlayRate(CAClockRef, UnsafeMutablePointer<Float64>) -> OSStatus](/documentation/audiotoolbox/caclockgetplayrate(_:_:))
- [func CAClockSetPlayRate(CAClockRef, Float64) -> OSStatus](/documentation/audiotoolbox/caclocksetplayrate(_:_:))
- [CAClockTempo](/documentation/audiotoolbox/caclocktempo)
- [CATempoMapEntry](/documentation/audiotoolbox/catempomapentry)

#### Initializers

- [init()](/documentation/audiotoolbox/catempomapentry/init())
- [init(beats: CAClockBeats, tempoBPM: CAClockTempo)](/documentation/audiotoolbox/catempomapentry/init(beats:tempobpm:))

#### Instance Properties

- [var beats: CAClockBeats](/documentation/audiotoolbox/catempomapentry/beats)
- [var tempoBPM: CAClockTempo](/documentation/audiotoolbox/catempomapentry/tempobpm)

### Accessing Clock Properties

- [func CAClockGetProperty(CAClockRef, CAClockPropertyID, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/caclockgetproperty(_:_:_:_:))
- [func CAClockGetPropertyInfo(CAClockRef, CAClockPropertyID, UnsafeMutablePointer<UInt32>?, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/caclockgetpropertyinfo(_:_:_:_:))
- [func CAClockSetProperty(CAClockRef, CAClockPropertyID, UInt32, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/caclocksetproperty(_:_:_:_:))
- [CAClockPropertyID](/documentation/audiotoolbox/caclockpropertyid)

#### Constants

- [case internalTimebase](/documentation/audiotoolbox/caclockpropertyid/internaltimebase)
- [case midiClockDestinations](/documentation/audiotoolbox/caclockpropertyid/midiclockdestinations)
- [case mtcDestinations](/documentation/audiotoolbox/caclockpropertyid/mtcdestinations)
- [case mtcFreewheelTime](/documentation/audiotoolbox/caclockpropertyid/mtcfreewheeltime)
- [case meterTrack](/documentation/audiotoolbox/caclockpropertyid/metertrack)
- [case name](/documentation/audiotoolbox/caclockpropertyid/name)
- [case smpteFormat](/documentation/audiotoolbox/caclockpropertyid/smpteformat)
- [case smpteOffset](/documentation/audiotoolbox/caclockpropertyid/smpteoffset)
- [case sendMIDISPP](/documentation/audiotoolbox/caclockpropertyid/sendmidispp)
- [case syncMode](/documentation/audiotoolbox/caclockpropertyid/syncmode)
- [case syncSource](/documentation/audiotoolbox/caclockpropertyid/syncsource)
- [case tempoMap](/documentation/audiotoolbox/caclockpropertyid/tempomap)
- [case timebaseSource](/documentation/audiotoolbox/caclockpropertyid/timebasesource)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/caclockpropertyid/init(rawvalue:))
- [CAClockSyncMode](/documentation/audiotoolbox/caclocksyncmode)

#### Constants

- [case `internal`](/documentation/audiotoolbox/caclocksyncmode/internal)
- [case midiClockTransport](/documentation/audiotoolbox/caclocksyncmode/midiclocktransport)
- [case mtcTransport](/documentation/audiotoolbox/caclocksyncmode/mtctransport)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/caclocksyncmode/init(rawvalue:))

### Parsing MIDI Data

- [func CAClockParseMIDI(CAClockRef, UnsafePointer<MIDIPacketList>) -> OSStatus](/documentation/audiotoolbox/caclockparsemidi(_:_:))

### Converting Time Values

- [func CAClockBarBeatTimeToBeats(CAClockRef, UnsafePointer<CABarBeatTime>, UnsafeMutablePointer<CAClockBeats>) -> OSStatus](/documentation/audiotoolbox/caclockbarbeattimetobeats(_:_:_:))
- [func CAClockBeatsToBarBeatTime(CAClockRef, CAClockBeats, UInt16, UnsafeMutablePointer<CABarBeatTime>) -> OSStatus](/documentation/audiotoolbox/caclockbeatstobarbeattime(_:_:_:_:))
- [func CAClockSMPTETimeToSeconds(CAClockRef, UnsafePointer<SMPTETime>, UnsafeMutablePointer<CAClockSeconds>) -> OSStatus](/documentation/audiotoolbox/caclocksmptetimetoseconds(_:_:_:))
- [func CAClockSecondsToSMPTETime(CAClockRef, CAClockSeconds, UInt16, UnsafeMutablePointer<SMPTETime>) -> OSStatus](/documentation/audiotoolbox/caclocksecondstosmptetime(_:_:_:_:))
- [func CAClockTranslateTime(CAClockRef, UnsafePointer<CAClockTime>, CAClockTimeFormat, UnsafeMutablePointer<CAClockTime>) -> OSStatus](/documentation/audiotoolbox/caclocktranslatetime(_:_:_:_:))
- [CAClockTimebase](/documentation/audiotoolbox/caclocktimebase)

#### Constants

- [case audioDevice](/documentation/audiotoolbox/caclocktimebase/audiodevice)
- [case audioOutputUnit](/documentation/audiotoolbox/caclocktimebase/audiooutputunit)
- [case hostTime](/documentation/audiotoolbox/caclocktimebase/hosttime)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/caclocktimebase/init(rawvalue:))
- [CAClockSeconds](/documentation/audiotoolbox/caclockseconds)
- [CAClockBeats](/documentation/audiotoolbox/caclockbeats)
- [CAClockSMPTEFormat](/documentation/audiotoolbox/caclocksmpteformat)
- [CABarBeatTime](/documentation/audiotoolbox/cabarbeattime)

#### Initializers

- [init()](/documentation/audiotoolbox/cabarbeattime/init())
- [init(bar: Int32, beat: UInt16, subbeat: UInt16, subbeatDivisor: UInt16, reserved: UInt16)](/documentation/audiotoolbox/cabarbeattime/init(bar:beat:subbeat:subbeatdivisor:reserved:))

#### Instance Properties

- [var bar: Int32](/documentation/audiotoolbox/cabarbeattime/bar)
- [var beat: UInt16](/documentation/audiotoolbox/cabarbeattime/beat)
- [var reserved: UInt16](/documentation/audiotoolbox/cabarbeattime/reserved)
- [var subbeat: UInt16](/documentation/audiotoolbox/cabarbeattime/subbeat)
- [var subbeatDivisor: UInt16](/documentation/audiotoolbox/cabarbeattime/subbeatdivisor)
- [CAMeterTrackEntry](/documentation/audiotoolbox/cametertrackentry)

#### Initializers

- [init()](/documentation/audiotoolbox/cametertrackentry/init())
- [init(beats: CAClockBeats, meterNumer: UInt16, meterDenom: UInt16)](/documentation/audiotoolbox/cametertrackentry/init(beats:meternumer:meterdenom:))

#### Instance Properties

- [var beats: CAClockBeats](/documentation/audiotoolbox/cametertrackentry/beats)
- [var meterDenom: UInt16](/documentation/audiotoolbox/cametertrackentry/meterdenom)
- [var meterNumer: UInt16](/documentation/audiotoolbox/cametertrackentry/meternumer)

### Getting Clock-Related Errors

- [Clock Errors](/documentation/audiotoolbox/1513526-clock-errors)

#### Constants

- [var kCAClock_CannotSetTimeError: OSStatus](/documentation/audiotoolbox/kcaclock_cannotsettimeerror)
- [var kCAClock_InvalidPlayRateError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidplayrateerror)
- [var kCAClock_InvalidPropertySizeError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidpropertysizeerror)
- [var kCAClock_InvalidSMPTEFormatError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidsmpteformaterror)
- [var kCAClock_InvalidSMPTEOffsetError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidsmpteoffseterror)
- [var kCAClock_InvalidSyncModeError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidsyncmodeerror)
- [var kCAClock_InvalidSyncSourceError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidsyncsourceerror)
- [var kCAClock_InvalidTimeFormatError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidtimeformaterror)
- [var kCAClock_InvalidTimebaseError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidtimebaseerror)
- [var kCAClock_InvalidTimebaseSourceError: OSStatus](/documentation/audiotoolbox/kcaclock_invalidtimebasesourceerror)
- [var kCAClock_InvalidUnitError: OSStatus](/documentation/audiotoolbox/kcaclock_invaliduniterror)
- [var kCAClock_UnknownPropertyError: OSStatus](/documentation/audiotoolbox/kcaclock_unknownpropertyerror)

## Deprecated

- [Deprecated Symbols](/documentation/audiotoolbox/deprecated-symbols)

### Inter-App Audio

- [func AudioOutputUnitPublish(UnsafePointer<AudioComponentDescription>, CFString, UInt32, AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiooutputunitpublish(_:_:_:_:))
- [func AudioOutputUnitGetHostIcon(AudioUnit, Float) -> UIImage?](/documentation/audiotoolbox/audiooutputunitgethosticon(_:_:))
- [func AudioComponentGetIcon(AudioComponent, Float) -> UIImage?](/documentation/audiotoolbox/audiocomponentgeticon(_:_:))
- [func AudioComponentGetLastActiveTime(AudioComponent) -> CFAbsoluteTime](/documentation/audiotoolbox/audiocomponentgetlastactivetime(_:))

### Functions

- [func AudioFileReadPackets(AudioFileID, Bool, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioStreamPacketDescription>?, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/audiofilereadpackets(_:_:_:_:_:_:_:))
- [func AudioComponentGetIcon(AudioComponent, Float) -> UIImage?](/documentation/audiotoolbox/audiocomponentgeticon(_:_:))
- [func AudioComponentGetLastActiveTime(AudioComponent) -> CFAbsoluteTime](/documentation/audiotoolbox/audiocomponentgetlastactivetime(_:))
- [func AudioHardwareServiceAddPropertyListener(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, AudioObjectPropertyListenerProc!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiohardwareserviceaddpropertylistener(_:_:_:_:))
- [func AudioHardwareServiceGetPropertyData(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UnsafeMutablePointer<UInt32>!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiohardwareservicegetpropertydata(_:_:_:_:_:_:))
- [func AudioHardwareServiceGetPropertyDataSize(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UnsafeMutablePointer<UInt32>!) -> OSStatus](/documentation/audiotoolbox/audiohardwareservicegetpropertydatasize(_:_:_:_:_:))
- [func AudioHardwareServiceHasProperty(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!) -> Bool](/documentation/audiotoolbox/audiohardwareservicehasproperty(_:_:))
- [func AudioHardwareServiceIsPropertySettable(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, UnsafeMutablePointer<DarwinBoolean>!) -> OSStatus](/documentation/audiotoolbox/audiohardwareserviceispropertysettable(_:_:_:))
- [func AudioHardwareServiceRemovePropertyListener(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, AudioObjectPropertyListenerProc!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiohardwareserviceremovepropertylistener(_:_:_:_:))
- [func AudioHardwareServiceSetPropertyData(AudioObjectID, UnsafePointer<AudioObjectPropertyAddress>!, UInt32, UnsafeRawPointer!, UInt32, UnsafeRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiohardwareservicesetpropertydata(_:_:_:_:_:_:))
- [func AudioOutputUnitGetHostIcon(AudioUnit, Float) -> UIImage?](/documentation/audiotoolbox/audiooutputunitgethosticon(_:_:))
- [func AudioOutputUnitPublish(UnsafePointer<AudioComponentDescription>, CFString, UInt32, AudioUnit) -> OSStatus](/documentation/audiotoolbox/audiooutputunitpublish(_:_:_:_:))
- [func AudioSessionAddPropertyListener(AudioSessionPropertyID, AudioSessionPropertyListener!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiosessionaddpropertylistener(_:_:_:))
- [func AudioSessionGetProperty(AudioSessionPropertyID, UnsafeMutablePointer<UInt32>!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiosessiongetproperty(_:_:_:))
- [func AudioSessionGetPropertySize(AudioSessionPropertyID, UnsafeMutablePointer<UInt32>!) -> OSStatus](/documentation/audiotoolbox/audiosessiongetpropertysize(_:_:))
- [func AudioSessionInitialize(CFRunLoop!, CFString!, AudioSessionInterruptionListener!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiosessioninitialize(_:_:_:_:))
- [func AudioSessionRemovePropertyListener(AudioSessionPropertyID) -> OSStatus](/documentation/audiotoolbox/audiosessionremovepropertylistener(_:))
- [func AudioSessionRemovePropertyListenerWithUserData(AudioSessionPropertyID, AudioSessionPropertyListener!, UnsafeMutableRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiosessionremovepropertylistenerwithuserdata(_:_:_:))
- [func AudioSessionSetActive(Bool) -> OSStatus](/documentation/audiotoolbox/audiosessionsetactive(_:))
- [func AudioSessionSetActiveWithFlags(Bool, UInt32) -> OSStatus](/documentation/audiotoolbox/audiosessionsetactivewithflags(_:_:))
- [func AudioSessionSetProperty(AudioSessionPropertyID, UInt32, UnsafeRawPointer!) -> OSStatus](/documentation/audiotoolbox/audiosessionsetproperty(_:_:_:))

### Callbacks

- [AudioSessionInterruptionListener](/documentation/audiotoolbox/audiosessioninterruptionlistener)
- [AudioSessionPropertyListener](/documentation/audiotoolbox/audiosessionpropertylistener)

### Data Types

- [ExtendedControlEvent](/documentation/audiotoolbox/extendedcontrolevent)

#### Initializers

- [init()](/documentation/audiotoolbox/extendedcontrolevent/init())
- [init(groupID: MusicDeviceGroupID, controlID: AudioUnitParameterID, value: AudioUnitParameterValue)](/documentation/audiotoolbox/extendedcontrolevent/init(groupid:controlid:value:))

#### Instance Properties

- [var controlID: AudioUnitParameterID](/documentation/audiotoolbox/extendedcontrolevent/controlid)
- [var groupID: MusicDeviceGroupID](/documentation/audiotoolbox/extendedcontrolevent/groupid)
- [var value: AudioUnitParameterValue](/documentation/audiotoolbox/extendedcontrolevent/value)
- [MIDIEndpointRef](/documentation/coremidi/midiendpointref)
- [MagicCookieInfo](/documentation/audiotoolbox/magiccookieinfo)
- [NoteInstanceID](/documentation/audiotoolbox/noteinstanceid)
- [ReadBytesFDF](/documentation/audiotoolbox/readbytesfdf)
- [ReadPacketDataFDF](/documentation/audiotoolbox/readpacketdatafdf)
- [ReadPacketsFDF](/documentation/audiotoolbox/readpacketsfdf)
- [SetPropertyFDF](/documentation/audiotoolbox/setpropertyfdf)
- [SetUserDataFDF](/documentation/audiotoolbox/setuserdatafdf)
- [WriteBytesFDF](/documentation/audiotoolbox/writebytesfdf)
- [WritePacketsFDF](/documentation/audiotoolbox/writepacketsfdf)
- [AudioSessionPropertyID](/documentation/audiotoolbox/audiosessionpropertyid)

### Constants

- [Audio Unit Attenuation Properties](/documentation/audiotoolbox/1534112-audio-unit-attenuation-propertie)

#### Constants

- [var kAudioUnitProperty_DistanceAttenuationData: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_distanceattenuationdata)
- [Audio Unit Instrument Errors](/documentation/audiotoolbox/1584141-audio-unit-instrument-errors)

#### Constants

- [var kAudioUnitErr_IllegalInstrument: OSStatus](/documentation/audiotoolbox/kaudiouniterr_illegalinstrument)
- [var kAudioUnitErr_InstrumentTypeNotFound: OSStatus](/documentation/audiotoolbox/kaudiouniterr_instrumenttypenotfound)
- [Anonymous](/documentation/audiotoolbox/1534019-anonymous)

#### Constants

- [var kAUSamplerProperty_BankAndPreset: AudioUnitPropertyID](/documentation/audiotoolbox/kausamplerproperty_bankandpreset)
- [var kAUSamplerProperty_LoadPresetFromBank: AudioUnitPropertyID](/documentation/audiotoolbox/kausamplerproperty_loadpresetfrombank)
- [Anonymous](/documentation/audiotoolbox/1534074-anonymous)

#### Constants

- [var kAUVoiceIOProperty_VoiceProcessingQuality: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_voiceprocessingquality)
- [Audio Graph Errors](/documentation/audiotoolbox/1537630-audio-graph-errors)

#### Constants

- [var kAUGraphErr_CannotDoInCurrentContext: OSStatus](/documentation/audiotoolbox/kaugrapherr_cannotdoincurrentcontext)
- [var kAUGraphErr_InvalidAudioUnit: OSStatus](/documentation/audiotoolbox/kaugrapherr_invalidaudiounit)
- [var kAUGraphErr_InvalidConnection: OSStatus](/documentation/audiotoolbox/kaugrapherr_invalidconnection)
- [var kAUGraphErr_NodeNotFound: OSStatus](/documentation/audiotoolbox/kaugrapherr_nodenotfound)
- [var kAUGraphErr_OutputNodeErr: OSStatus](/documentation/audiotoolbox/kaugrapherr_outputnodeerr)
- [Audio Converter Property ID](/documentation/audiotoolbox/1624333-audio-converter-property-id)

#### Constants

- [var kAudioConverterPropertyCanResumeFromInterruption: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertycanresumefrominterruption)
- [Anonymous](/documentation/audiotoolbox/1621044-anonymous)

#### Constants

- [var kAUVoiceIOProperty_DuckNonVoiceAudio: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_ducknonvoiceaudio)
- [Anonymous](/documentation/audiotoolbox/1618426-anonymous)

#### Constants

- [var kAudioSessionProperty_AudioRoute: Int](/documentation/audiotoolbox/kaudiosessionproperty_audioroute)
- [Anonymous](/documentation/audiotoolbox/1618742-anonymous)

#### Constants

- [var kAudioQueueTimePitchAlgorithm_LowQualityZeroLatency: UInt32](/documentation/audiotoolbox/kaudioqueuetimepitchalgorithm_lowqualityzerolatency)
- [Anonymous](/documentation/audiotoolbox/1619479-anonymous)

#### Constants

- [var kAudioUnitSubType_AU3DMixerEmbedded: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_au3dmixerembedded)
- [Anonymous](/documentation/audiotoolbox/1619504-anonymous)

#### Constants

- [var kAudioUnitSubType_AUiPodTime: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auipodtime)
- [Anonymous](/documentation/audiotoolbox/1533960-anonymous)

#### Constants

- [var kSpeakerConfiguration_5_0: Int](/documentation/audiotoolbox/kspeakerconfiguration_5_0)
- [var kSpeakerConfiguration_5_1: Int](/documentation/audiotoolbox/kspeakerconfiguration_5_1)
- [var kSpeakerConfiguration_HeadPhones: Int](/documentation/audiotoolbox/kspeakerconfiguration_headphones)
- [var kSpeakerConfiguration_Quad: Int](/documentation/audiotoolbox/kspeakerconfiguration_quad)
- [var kSpeakerConfiguration_Stereo: Int](/documentation/audiotoolbox/kspeakerconfiguration_stereo)
- [Anonymous](/documentation/audiotoolbox/1534225-anonymous)

#### Constants

- [var kAudioUnitProperty_SpeakerConfiguration: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_speakerconfiguration)
- [Music Device Properties](/documentation/audiotoolbox/1534089-music-device-properties)

#### Constants

- [var kAudioUnitProperty_PannerMode: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_pannermode)
- [var kMusicDeviceProperty_GroupOutputBus: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_groupoutputbus)
- [var kMusicDeviceProperty_SoundBankFSSpec: AudioUnitPropertyID](/documentation/audiotoolbox/kmusicdeviceproperty_soundbankfsspec)
- [3D Mixer Audio Unit Properties](/documentation/audiotoolbox/1534063-3d_mixer_audio_unit_properties)

#### Constants

- [var kAudioUnitProperty_3DMixerAttenuationCurve: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_3dmixerattenuationcurve)
- [var kAudioUnitProperty_3DMixerDistanceAtten: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_3dmixerdistanceatten)
- [var kAudioUnitProperty_3DMixerDistanceParams: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_3dmixerdistanceparams)
- [var kAudioUnitProperty_3DMixerRenderingFlags: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_3dmixerrenderingflags)
- [var kAudioUnitProperty_DopplerShift: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_dopplershift)
- [var kAudioUnitProperty_ReverbPreset: AudioUnitPropertyID](/documentation/audiotoolbox/kaudiounitproperty_reverbpreset)
- [var kAudioSession_AudioRouteChangeKey_OldRoute: String](/documentation/audiotoolbox/kaudiosession_audioroutechangekey_oldroute)
- [var AU_SUPPORT_INTERAPP_AUDIO: Int32](/documentation/audiotoolbox/au_support_interapp_audio)
- [Hardware Codec Capabilities](/documentation/audiotoolbox/1620452-hardware-codec-capabilities)

#### Constants

- [var kAudioFormatProperty_HardwareCodecCapabilities: AudioFormatPropertyID](/documentation/audiotoolbox/kaudioformatproperty_hardwarecodeccapabilities)
- [Deprecated Audio Codec Properties](/documentation/audiotoolbox/1494107-deprecated-audio-codec-propertie)

#### Constants

- [var kAudioCodecBitRateFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecbitrateformat)
- [var kAudioCodecDoesSampleRateConversion: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecdoessamplerateconversion)
- [var kAudioCodecExtendFrequencies: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecextendfrequencies)
- [var kAudioCodecInputFormatsForOutputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecinputformatsforoutputformat)
- [var kAudioCodecOutputFormatsForInputFormat: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecoutputformatsforinputformat)
- [var kAudioCodecOutputPrecedence: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecoutputprecedence)
- [var kAudioCodecPropertyAvailableBitRates: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailablebitrates)
- [var kAudioCodecPropertyAvailableInputChannelLayouts: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableinputchannellayouts)
- [var kAudioCodecPropertyAvailableOutputChannelLayouts: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyavailableoutputchannellayouts)
- [var kAudioCodecPropertyInputChannelLayout: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyinputchannellayout)
- [var kAudioCodecPropertyOutputChannelLayout: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyoutputchannellayout)
- [var kAudioCodecPropertyRequiresPacketDescription: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyrequirespacketdescription)
- [var kAudioCodecPropertyZeroFramesPadded: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyzeroframespadded)
- [var kAudioCodecUseRecommendedSampleRate: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecuserecommendedsamplerate)
- [Deprecated Constants Used With kAudioCodecBitRateFormat](/documentation/audiotoolbox/1494081-deprecated-constants-used-with-k)

#### Constants

- [var kAudioCodecBitRateFormat_ABR: UInt32](/documentation/audiotoolbox/kaudiocodecbitrateformat_abr)
- [var kAudioCodecBitRateFormat_CBR: UInt32](/documentation/audiotoolbox/kaudiocodecbitrateformat_cbr)
- [var kAudioCodecBitRateFormat_VBR: UInt32](/documentation/audiotoolbox/kaudiocodecbitrateformat_vbr)
- [Deprecated Constants Used With kAudioCodecOutputPrecedence](/documentation/audiotoolbox/1494070-deprecated-constants-used-with-k)

#### Constants

- [var kAudioCodecOutputPrecedenceBitRate: UInt32](/documentation/audiotoolbox/kaudiocodecoutputprecedencebitrate)
- [var kAudioCodecOutputPrecedenceNone: UInt32](/documentation/audiotoolbox/kaudiocodecoutputprecedencenone)
- [var kAudioCodecOutputPrecedenceSampleRate: UInt32](/documentation/audiotoolbox/kaudiocodecoutputprecedencesamplerate)
- [Deprecated Constants Used With kAudioSettings_Hint](/documentation/audiotoolbox/1494142-deprecated-constants-used-with-k)

#### Constants

- [var kHintAdvanced: UInt32](/documentation/audiotoolbox/khintadvanced)
- [var kHintBasic: UInt32](/documentation/audiotoolbox/khintbasic)
- [var kHintHidden: UInt32](/documentation/audiotoolbox/khinthidden)
- [Deprecated Audio Session Categories](/documentation/audiotoolbox/1618459-deprecated-audio-session-categor)

#### Constants

- [var kAudioSessionCategory_UserInterfaceSoundEffects: Int](/documentation/audiotoolbox/kaudiosessioncategory_userinterfacesoundeffects)
- [var kAudioSessionCategory_LiveAudio: Int](/documentation/audiotoolbox/kaudiosessioncategory_liveaudio)

### Audio Graphs

- [Audio Unit Processing Graph Services](/documentation/audiotoolbox/audio-unit-processing-graph-services)

#### Audio Unit Processing Graph Services Functions

- [func AUGraphAddNode(AUGraph, UnsafePointer<AudioComponentDescription>, UnsafeMutablePointer<AUNode>) -> OSStatus](/documentation/audiotoolbox/augraphaddnode(_:_:_:))
- [func AUGraphAddRenderNotify(AUGraph, AURenderCallback, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/augraphaddrendernotify(_:_:_:))
- [func AUGraphClearConnections(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphclearconnections(_:))
- [func AUGraphClose(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphclose(_:))
- [func AUGraphConnectNodeInput(AUGraph, AUNode, UInt32, AUNode, UInt32) -> OSStatus](/documentation/audiotoolbox/augraphconnectnodeinput(_:_:_:_:_:))
- [func AUGraphCountNodeInteractions(AUGraph, AUNode, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/augraphcountnodeinteractions(_:_:_:))
- [func AUGraphDisconnectNodeInput(AUGraph, AUNode, UInt32) -> OSStatus](/documentation/audiotoolbox/augraphdisconnectnodeinput(_:_:_:))
- [func AUGraphGetCPULoad(AUGraph, UnsafeMutablePointer<Float32>) -> OSStatus](/documentation/audiotoolbox/augraphgetcpuload(_:_:))
- [func AUGraphGetIndNode(AUGraph, UInt32, UnsafeMutablePointer<AUNode>) -> OSStatus](/documentation/audiotoolbox/augraphgetindnode(_:_:_:))
- [func AUGraphGetInteractionInfo(AUGraph, UInt32, UnsafeMutablePointer<AUNodeInteraction>) -> OSStatus](/documentation/audiotoolbox/augraphgetinteractioninfo(_:_:_:))
- [func AUGraphGetMaxCPULoad(AUGraph, UnsafeMutablePointer<Float32>) -> OSStatus](/documentation/audiotoolbox/augraphgetmaxcpuload(_:_:))
- [func AUGraphGetNodeCount(AUGraph, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/augraphgetnodecount(_:_:))
- [func AUGraphGetNodeInfoSubGraph(AUGraph, AUNode, UnsafeMutablePointer<AUGraph?>) -> OSStatus](/documentation/audiotoolbox/augraphgetnodeinfosubgraph(_:_:_:))
- [func AUGraphGetNodeInteractions(AUGraph, AUNode, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AUNodeInteraction>) -> OSStatus](/documentation/audiotoolbox/augraphgetnodeinteractions(_:_:_:_:))
- [func AUGraphGetNumberOfInteractions(AUGraph, UnsafeMutablePointer<UInt32>) -> OSStatus](/documentation/audiotoolbox/augraphgetnumberofinteractions(_:_:))
- [func AUGraphInitialize(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphinitialize(_:))
- [func AUGraphIsInitialized(AUGraph, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/augraphisinitialized(_:_:))
- [func AUGraphIsNodeSubGraph(AUGraph, AUNode, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/augraphisnodesubgraph(_:_:_:))
- [func AUGraphIsOpen(AUGraph, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/augraphisopen(_:_:))
- [func AUGraphIsRunning(AUGraph, UnsafeMutablePointer<DarwinBoolean>) -> OSStatus](/documentation/audiotoolbox/augraphisrunning(_:_:))
- [func AUGraphNewNodeSubGraph(AUGraph, UnsafeMutablePointer<AUNode>) -> OSStatus](/documentation/audiotoolbox/augraphnewnodesubgraph(_:_:))
- [func AUGraphNodeInfo(AUGraph, AUNode, UnsafeMutablePointer<AudioComponentDescription>?, UnsafeMutablePointer<AudioUnit?>?) -> OSStatus](/documentation/audiotoolbox/augraphnodeinfo(_:_:_:_:))
- [func AUGraphOpen(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphopen(_:))
- [func AUGraphRemoveNode(AUGraph, AUNode) -> OSStatus](/documentation/audiotoolbox/augraphremovenode(_:_:))
- [func AUGraphRemoveRenderNotify(AUGraph, AURenderCallback, UnsafeMutableRawPointer?) -> OSStatus](/documentation/audiotoolbox/augraphremoverendernotify(_:_:_:))
- [func AUGraphSetNodeInputCallback(AUGraph, AUNode, UInt32, UnsafePointer<AURenderCallbackStruct>) -> OSStatus](/documentation/audiotoolbox/augraphsetnodeinputcallback(_:_:_:_:))
- [func AUGraphStart(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphstart(_:))
- [func AUGraphStop(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphstop(_:))
- [func AUGraphUninitialize(AUGraph) -> OSStatus](/documentation/audiotoolbox/augraphuninitialize(_:))
- [func AUGraphUpdate(AUGraph, UnsafeMutablePointer<DarwinBoolean>?) -> OSStatus](/documentation/audiotoolbox/augraphupdate(_:_:))
- [func DisposeAUGraph(AUGraph) -> OSStatus](/documentation/audiotoolbox/disposeaugraph(_:))
- [func NewAUGraph(UnsafeMutablePointer<AUGraph?>) -> OSStatus](/documentation/audiotoolbox/newaugraph(_:))

#### Data Types

- [AudioUnitNodeConnection](/documentation/audiotoolbox/audiounitnodeconnection)

##### Initializers

- [init()](/documentation/audiotoolbox/audiounitnodeconnection/init())
- [init(sourceNode: AUNode, sourceOutputNumber: UInt32, destNode: AUNode, destInputNumber: UInt32)](/documentation/audiotoolbox/audiounitnodeconnection/init(sourcenode:sourceoutputnumber:destnode:destinputnumber:))

##### Instance Properties

- [var destInputNumber: UInt32](/documentation/audiotoolbox/audiounitnodeconnection/destinputnumber)
- [var destNode: AUNode](/documentation/audiotoolbox/audiounitnodeconnection/destnode)
- [var sourceNode: AUNode](/documentation/audiotoolbox/audiounitnodeconnection/sourcenode)
- [var sourceOutputNumber: UInt32](/documentation/audiotoolbox/audiounitnodeconnection/sourceoutputnumber)
- [AUGraph](/documentation/audiotoolbox/augraph)
- [AUNode](/documentation/audiotoolbox/aunode)
- [AUNodeInteraction](/documentation/audiotoolbox/aunodeinteraction)

##### Initializers

- [init()](/documentation/audiotoolbox/aunodeinteraction/init())
- [init(nodeInteractionType: UInt32, nodeInteraction: AUNodeInteraction.__Unnamed_union_nodeInteraction)](/documentation/audiotoolbox/aunodeinteraction/init(nodeinteractiontype:nodeinteraction:))

##### Instance Properties

- [var nodeInteraction: AUNodeInteraction.__Unnamed_union_nodeInteraction](/documentation/audiotoolbox/aunodeinteraction/nodeinteraction)
- [var nodeInteractionType: UInt32](/documentation/audiotoolbox/aunodeinteraction/nodeinteractiontype)
- [AUNodeRenderCallback](/documentation/audiotoolbox/aunoderendercallback)

##### Initializers

- [init()](/documentation/audiotoolbox/aunoderendercallback/init())
- [init(destNode: AUNode, destInputNumber: AudioUnitElement, cback: AURenderCallbackStruct)](/documentation/audiotoolbox/aunoderendercallback/init(destnode:destinputnumber:cback:))

##### Instance Properties

- [var cback: AURenderCallbackStruct](/documentation/audiotoolbox/aunoderendercallback/cback)
- [var destInputNumber: AudioUnitElement](/documentation/audiotoolbox/aunoderendercallback/destinputnumber)
- [var destNode: AUNode](/documentation/audiotoolbox/aunoderendercallback/destnode)

#### Constants

- [kAUNodeInteraction_Connection](/documentation/audiotoolbox/1537633-kaunodeinteraction-connection)

##### Constants

- [var kAUNodeInteraction_Connection: UInt32](/documentation/audiotoolbox/kaunodeinteraction_connection)
- [var kAUNodeInteraction_InputCallback: UInt32](/documentation/audiotoolbox/kaunodeinteraction_inputcallback)

#### Result Codes

- [var kAUGraphErr_NodeNotFound: OSStatus](/documentation/audiotoolbox/kaugrapherr_nodenotfound)
- [var kAUGraphErr_InvalidConnection: OSStatus](/documentation/audiotoolbox/kaugrapherr_invalidconnection)
- [var kAUGraphErr_OutputNodeErr: OSStatus](/documentation/audiotoolbox/kaugrapherr_outputnodeerr)
- [var kAUGraphErr_CannotDoInCurrentContext: OSStatus](/documentation/audiotoolbox/kaugrapherr_cannotdoincurrentcontext)
- [var kAUGraphErr_InvalidAudioUnit: OSStatus](/documentation/audiotoolbox/kaugrapherr_invalidaudiounit)

## Reference

- [AudioToolbox Structures](/documentation/audiotoolbox/audiotoolbox-structures)

### Structures

- [AUMIDIEventList](/documentation/audiotoolbox/aumidieventlist)

#### Initializers

- [init()](/documentation/audiotoolbox/aumidieventlist/init())
- [init(next: UnsafeMutablePointer<AURenderEvent>?, eventSampleTime: AUEventSampleTime, eventType: AURenderEventType, reserved: UInt8, cable: UInt8, eventList: MIDIEventList)](/documentation/audiotoolbox/aumidieventlist/init(next:eventsampletime:eventtype:reserved:cable:eventlist:))

#### Instance Properties

- [var cable: UInt8](/documentation/audiotoolbox/aumidieventlist/cable)
- [var eventList: MIDIEventList](/documentation/audiotoolbox/aumidieventlist/eventlist)
- [var eventSampleTime: AUEventSampleTime](/documentation/audiotoolbox/aumidieventlist/eventsampletime)
- [var eventType: AURenderEventType](/documentation/audiotoolbox/aumidieventlist/eventtype)
- [var next: UnsafeMutablePointer<AURenderEvent>?](/documentation/audiotoolbox/aumidieventlist/next)
- [var reserved: UInt8](/documentation/audiotoolbox/aumidieventlist/reserved)
- [AudioConverterOptions](/documentation/audiotoolbox/audioconverteroptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audioconverteroptions/init(rawvalue:))

#### Type Properties

- [static var unbuffered: AudioConverterOptions](/documentation/audiotoolbox/audioconverteroptions/unbuffered)
- [AudioToolbox Enumerations](/documentation/audiotoolbox/audiotoolbox-enumerations)

### Enumerations

- [Apple Voice Processing Audio Unit Errors](/documentation/audiotoolbox/1534085-apple-voice-processing-audio-uni)

#### Constants

- [var kAUVoiceIOErr_UnexpectedNumberOfInputChannels: OSStatus](/documentation/audiotoolbox/kauvoiceioerr_unexpectednumberofinputchannels)
- [Anonymous](/documentation/audiotoolbox/3751765-anonymous)

#### Constants

- [var kAUVoiceIOProperty_MutedSpeechActivityEventListener: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_mutedspeechactivityeventlistener)
- [Anonymous](/documentation/audiotoolbox/3950917-anonymous)

#### Constants

- [var kAUSoundIsolationParam_SoundToIsolate: AudioUnitParameterID](/documentation/audiotoolbox/kausoundisolationparam_soundtoisolate)
- [var kAUSoundIsolationParam_WetDryMixPercent: AudioUnitParameterID](/documentation/audiotoolbox/kausoundisolationparam_wetdrymixpercent)
- [Anonymous](/documentation/audiotoolbox/4103713-anonymous)

#### Constants

- [var kAUVoiceIOProperty_OtherAudioDuckingConfiguration: AudioUnitPropertyID](/documentation/audiotoolbox/kauvoiceioproperty_otheraudioduckingconfiguration)
- [Anonymous](/documentation/audiotoolbox/4304947-anonymous)

#### Constants

- [var kDynamicRangeCompressionProfile_GeneralCompression: UInt32](/documentation/audiotoolbox/kdynamicrangecompressionprofile_generalcompression)
- [var kDynamicRangeCompressionProfile_LateNight: UInt32](/documentation/audiotoolbox/kdynamicrangecompressionprofile_latenight)
- [var kDynamicRangeCompressionProfile_LimitedPlaybackRange: UInt32](/documentation/audiotoolbox/kdynamicrangecompressionprofile_limitedplaybackrange)
- [var kDynamicRangeCompressionProfile_NoisyEnvironment: UInt32](/documentation/audiotoolbox/kdynamicrangecompressionprofile_noisyenvironment)
- [var kDynamicRangeCompressionProfile_None: UInt32](/documentation/audiotoolbox/kdynamicrangecompressionprofile_none)
- [Anonymous](/documentation/audiotoolbox/4354006-anonymous)

#### Constants

- [var kAUSoundIsolationSoundType_HighQualityVoice: Int](/documentation/audiotoolbox/kausoundisolationsoundtype_highqualityvoice)
- [var kAUSoundIsolationSoundType_Voice: Int](/documentation/audiotoolbox/kausoundisolationsoundtype_voice)
- [AUSpatialMixerPersonalizedHRTFMode](/documentation/audiotoolbox/auspatialmixerpersonalizedhrtfmode)

#### Enumeration Cases

- [case auto](/documentation/audiotoolbox/auspatialmixerpersonalizedhrtfmode/auto)
- [case off](/documentation/audiotoolbox/auspatialmixerpersonalizedhrtfmode/off)
- [case on](/documentation/audiotoolbox/auspatialmixerpersonalizedhrtfmode/on)

#### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auspatialmixerpersonalizedhrtfmode/init(rawvalue:))
- [AudioConverterOptions](/documentation/audiotoolbox/audioconverteroptions)

#### Initializers

- [init(rawValue: UInt32)](/documentation/audiotoolbox/audioconverteroptions/init(rawvalue:))

#### Type Properties

- [static var unbuffered: AudioConverterOptions](/documentation/audiotoolbox/audioconverteroptions/unbuffered)
- [AudioToolbox Constants](/documentation/audiotoolbox/audiotoolbox-constants)

### Constants

- [var kAudioUnitConfigurationInfo_AvailableArchitectures: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_availablearchitectures)
- [var kAudioUnitConfigurationInfo_MIDIProtocol: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_midiprotocol)
- [var kAudioUnitConfigurationInfo_MigrateFromPlugin: String](/documentation/audiotoolbox/kaudiounitconfigurationinfo_migratefromplugin)
- [AudioToolbox Functions](/documentation/audiotoolbox/audiotoolbox-functions)

### Functions

- [func AudioComponentValidateWithResults(AudioComponent, CFDictionary?, (AudioComponentValidationResult, CFDictionary) -> Void) -> OSStatus](/documentation/audiotoolbox/audiocomponentvalidatewithresults(_:_:_:))
- [func AudioConverterNewWithOptions(UnsafePointer<AudioStreamBasicDescription>, UnsafePointer<AudioStreamBasicDescription>, AudioConverterOptions, UnsafeMutablePointer<AudioConverterRef?>) -> OSStatus](/documentation/audiotoolbox/audioconverternewwithoptions(_:_:_:_:))
- [func AudioConverterPrepare(UInt32, UnsafeMutableRawPointer?, ((OSStatus) -> Void)?)](/documentation/audiotoolbox/audioconverterprepare(_:_:_:))
- [func AudioFileComponentGetUserDataAtOffset(AudioFileComponent, UInt32, UInt32, Int64, UnsafeMutablePointer<UInt32>, UnsafeMutableRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetuserdataatoffset(_:_:_:_:_:_:))
- [func AudioFileComponentGetUserDataSize64(AudioFileComponent, UInt32, UInt32, UnsafeMutablePointer<UInt64>) -> OSStatus](/documentation/audiotoolbox/audiofilecomponentgetuserdatasize64(_:_:_:_:))
- [AudioToolbox Data Types](/documentation/audiotoolbox/audiotoolbox-data-types)

### Data Types

- [AUMIDIEventListBlock](/documentation/audiotoolbox/aumidieventlistblock)
- [AudioFileComponentGetUserDataAtOffsetProc](/documentation/audiotoolbox/audiofilecomponentgetuserdataatoffsetproc)
- [AudioFileComponentGetUserDataSize64Proc](/documentation/audiotoolbox/audiofilecomponentgetuserdatasize64proc)
- [CallHostBlock](/documentation/audiotoolbox/callhostblock)

## Macros

- [Macros](/documentation/audiotoolbox/audiotoolbox-macros)

### Macros

- [var AUDIO_UNIT_VERSION: Int32](/documentation/audiotoolbox/audio_unit_version)

## Protocols

- [SpatialAudioExperience](/documentation/audiotoolbox/spatialaudioexperience)

### Type Properties

- [static var automatic: AutomaticSpatialAudio](/documentation/audiotoolbox/spatialaudioexperience/automatic)
- [static var bypassed: BypassedSpatialAudio](/documentation/audiotoolbox/spatialaudioexperience/bypassed)
- [static var fixed: FixedSpatialAudio](/documentation/audiotoolbox/spatialaudioexperience/fixed)
- [static var headTracked: HeadTrackedSpatialAudio](/documentation/audiotoolbox/spatialaudioexperience/headtracked)

### Type Methods

- [static func fixed(soundStageSize: SpatialAudioExperiences.SoundStageSize) -> Self](/documentation/audiotoolbox/spatialaudioexperience/fixed(soundstagesize:))
- [static func headTracked(SpatialAudioExperiences.AnchoringStrategy, soundStageSize: SpatialAudioExperiences.SoundStageSize) -> Self](/documentation/audiotoolbox/spatialaudioexperience/headtracked(_:soundstagesize:))

## Structures

- [AutomaticSpatialAudio](/documentation/audiotoolbox/automaticspatialaudio)
- [BypassedSpatialAudio](/documentation/audiotoolbox/bypassedspatialaudio)
- [FixedSpatialAudio](/documentation/audiotoolbox/fixedspatialaudio)

### Instance Properties

- [var soundStageSize: SpatialAudioExperiences.SoundStageSize](/documentation/audiotoolbox/fixedspatialaudio/soundstagesize)
- [HeadTrackedSpatialAudio](/documentation/audiotoolbox/headtrackedspatialaudio)

### Instance Properties

- [var anchoringStrategy: SpatialAudioExperiences.AnchoringStrategy](/documentation/audiotoolbox/headtrackedspatialaudio/anchoringstrategy)
- [var soundStageSize: SpatialAudioExperiences.SoundStageSize](/documentation/audiotoolbox/headtrackedspatialaudio/soundstagesize)

## Variables

- [var kAUAudioMixParameter_RemixAmount: AudioUnitParameterID](/documentation/audiotoolbox/kauaudiomixparameter_remixamount)
- [var kAUAudioMixParameter_Style: AudioUnitParameterID](/documentation/audiotoolbox/kauaudiomixparameter_style)
- [var kAUAudioMixProperty_EnableSpatialization: AudioUnitPropertyID](/documentation/audiotoolbox/kauaudiomixproperty_enablespatialization)
- [var kAUAudioMixProperty_SpatialAudioMixMetadata: AudioUnitPropertyID](/documentation/audiotoolbox/kauaudiomixproperty_spatialaudiomixmetadata)
- [var kAudioCodecContentSource_AV_Spatial_Live: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_av_spatial_live)
- [var kAudioCodecContentSource_AV_Spatial_Offline: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_av_spatial_offline)
- [var kAudioCodecContentSource_AV_Traditional_Live: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_av_traditional_live)
- [var kAudioCodecContentSource_AV_Traditional_Offline: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_av_traditional_offline)
- [var kAudioCodecContentSource_AppleAV_Spatial_Live: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_appleav_spatial_live)
- [var kAudioCodecContentSource_AppleAV_Spatial_Offline: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_appleav_spatial_offline)
- [var kAudioCodecContentSource_AppleAV_Traditional_Live: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_appleav_traditional_live)
- [var kAudioCodecContentSource_AppleAV_Traditional_Offline: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_appleav_traditional_offline)
- [var kAudioCodecContentSource_AppleCapture_Spatial: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applecapture_spatial)
- [var kAudioCodecContentSource_AppleCapture_Spatial_Enhanced: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applecapture_spatial_enhanced)
- [var kAudioCodecContentSource_AppleCapture_Traditional: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applecapture_traditional)
- [var kAudioCodecContentSource_AppleMusic_Spatial: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applemusic_spatial)
- [var kAudioCodecContentSource_AppleMusic_Traditional: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applemusic_traditional)
- [var kAudioCodecContentSource_ApplePassthrough: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_applepassthrough)
- [var kAudioCodecContentSource_Capture_Spatial: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_capture_spatial)
- [var kAudioCodecContentSource_Capture_Spatial_Enhanced: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_capture_spatial_enhanced)
- [var kAudioCodecContentSource_Capture_Traditional: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_capture_traditional)
- [var kAudioCodecContentSource_Music_Spatial: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_music_spatial)
- [var kAudioCodecContentSource_Music_Traditional: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_music_traditional)
- [var kAudioCodecContentSource_Passthrough: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_passthrough)
- [var kAudioCodecContentSource_Reserved: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_reserved)
- [var kAudioCodecContentSource_Unspecified: Int32](/documentation/audiotoolbox/kaudiocodeccontentsource_unspecified)
- [var kAudioCodecDynamicRangeControlConfiguration_Capture: UInt32](/documentation/audiotoolbox/kaudiocodecdynamicrangecontrolconfiguration_capture)
- [var kAudioCodecDynamicRangeControlConfiguration_Movie: UInt32](/documentation/audiotoolbox/kaudiocodecdynamicrangecontrolconfiguration_movie)
- [var kAudioCodecDynamicRangeControlConfiguration_Music: UInt32](/documentation/audiotoolbox/kaudiocodecdynamicrangecontrolconfiguration_music)
- [var kAudioCodecDynamicRangeControlConfiguration_None: UInt32](/documentation/audiotoolbox/kaudiocodecdynamicrangecontrolconfiguration_none)
- [var kAudioCodecDynamicRangeControlConfiguration_Speech: UInt32](/documentation/audiotoolbox/kaudiocodecdynamicrangecontrolconfiguration_speech)
- [var kAudioCodecPropertyASPFrequency: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertyaspfrequency)
- [var kAudioCodecPropertyContentSource: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertycontentsource)
- [var kAudioCodecPropertyDynamicRangeControlConfiguration: AudioCodecPropertyID](/documentation/audiotoolbox/kaudiocodecpropertydynamicrangecontrolconfiguration)
- [var kAudioConverterPropertyChannelMixMap: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertychannelmixmap)
- [var kAudioConverterPropertyPerformDownmix: AudioConverterPropertyID](/documentation/audiotoolbox/kaudioconverterpropertyperformdownmix)
- [var kAudioUnitErr_MultipleVoiceProcessors: OSStatus](/documentation/audiotoolbox/kaudiouniterr_multiplevoiceprocessors)
- [var kAudioUnitSubType_AUAudioMix: UInt32](/documentation/audiotoolbox/kaudiounitsubtype_auaudiomix)

## Functions

- [func AudioConverterFillComplexBufferRealtimeSafe(AudioConverterRef, AudioConverterComplexInputDataProcRealtimeSafe, UnsafeMutableRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioBufferList>, UnsafeMutablePointer<AudioStreamPacketDescription>?) -> OSStatus](/documentation/audiotoolbox/audioconverterfillcomplexbufferrealtimesafe(_:_:_:_:_:_:))
- [func AudioConverterFillComplexBufferWithPacketDependencies(AudioConverterRef, AudioConverterComplexInputDataProc, UnsafeMutableRawPointer?, UnsafeMutablePointer<UInt32>, UnsafeMutablePointer<AudioBufferList>, UnsafeMutablePointer<AudioStreamPacketDescription>?, UnsafeMutablePointer<AudioStreamPacketDependencyDescription>) -> OSStatus](/documentation/audiotoolbox/audioconverterfillcomplexbufferwithpacketdependencies(_:_:_:_:_:_:_:))
- [func AudioFileWritePacketsWithDependencies(AudioFileID, Bool, UInt32, UnsafePointer<AudioStreamPacketDescription>?, UnsafePointer<AudioStreamPacketDependencyDescription>, Int64, UnsafeMutablePointer<UInt32>, UnsafeRawPointer) -> OSStatus](/documentation/audiotoolbox/audiofilewritepacketswithdependencies(_:_:_:_:_:_:_:_:))
- [func AudioServicesPlayAlertSound(SystemSoundID, spatialExperience: any SpatialAudioExperience) async](/documentation/audiotoolbox/audioservicesplayalertsound(_:spatialexperience:))
- [func AudioServicesPlaySystemSound(SystemSoundID, spatialExperience: any SpatialAudioExperience) async](/documentation/audiotoolbox/audioservicesplaysystemsound(_:spatialexperience:))

## Type Aliases

- [AudioConverterComplexInputDataProcRealtimeSafe](/documentation/audiotoolbox/audioconvertercomplexinputdataprocrealtimesafe)

## Enumerations

- [AUAudioMixRenderingStyle](/documentation/audiotoolbox/auaudiomixrenderingstyle)

### Enumeration Cases

- [case audioMixRenderingStyle_Cinematic](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_cinematic)
- [case audioMixRenderingStyle_CinematicBackgroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_cinematicbackgroundstem)
- [case audioMixRenderingStyle_CinematicForegroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_cinematicforegroundstem)
- [case audioMixRenderingStyle_InFrame](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_inframe)
- [case audioMixRenderingStyle_InFrameBackgroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_inframebackgroundstem)
- [case audioMixRenderingStyle_InFrameForegroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_inframeforegroundstem)
- [case audioMixRenderingStyle_Standard](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_standard)
- [case audioMixRenderingStyle_Studio](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_studio)
- [case audioMixRenderingStyle_StudioBackgroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_studiobackgroundstem)
- [case audioMixRenderingStyle_StudioForegroundStem](/documentation/audiotoolbox/auaudiomixrenderingstyle/audiomixrenderingstyle_studioforegroundstem)

### Initializers

- [init?(rawValue: UInt32)](/documentation/audiotoolbox/auaudiomixrenderingstyle/init(rawvalue:))
- [SpatialAudioExperiences](/documentation/audiotoolbox/spatialaudioexperiences)

### Enumerations

- [SpatialAudioExperiences.AnchoringStrategy](/documentation/audiotoolbox/spatialaudioexperiences/anchoringstrategy)

#### Enumeration Cases

- [case automatic](/documentation/audiotoolbox/spatialaudioexperiences/anchoringstrategy/automatic)
- [case front](/documentation/audiotoolbox/spatialaudioexperiences/anchoringstrategy/front)
- [case scene(identifier: String)](/documentation/audiotoolbox/spatialaudioexperiences/anchoringstrategy/scene(identifier:))
- [SpatialAudioExperiences.SoundStageSize](/documentation/audiotoolbox/spatialaudioexperiences/soundstagesize)

#### Enumeration Cases

- [case automatic](/documentation/audiotoolbox/spatialaudioexperiences/soundstagesize/automatic)
- [case large](/documentation/audiotoolbox/spatialaudioexperiences/soundstagesize/large)
- [case medium](/documentation/audiotoolbox/spatialaudioexperiences/soundstagesize/medium)
- [case small](/documentation/audiotoolbox/spatialaudioexperiences/soundstagesize/small)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
