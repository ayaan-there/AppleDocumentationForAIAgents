# AVFAudio Documentation

Source: https://sosumi.ai/documentation/avfaudio

---
title: AVFAudio
source: https://developer.apple.com/documentation/avfaudio
timestamp: 2026-02-13T18:54:16.033Z
---

## Essentials

- [AVFAudio updates](/documentation/updates/avfaudio)

## System audio

- [Handling audio interruptions](/documentation/avfaudio/handling-audio-interruptions)
- [Responding to audio route changes](/documentation/avfaudio/responding-to-audio-route-changes)
- [Routing audio to specific devices in multidevice sessions](/documentation/avfaudio/routing-audio-to-specific-devices-in-multidevice-sessions)
- [Adding synthesized speech to calls](/documentation/avfaudio/adding-synthesized-speech-to-calls)
- [Capturing stereo audio from built-In microphones](/documentation/avfaudio/capturing-stereo-audio-from-built-in-microphones)
- [AVAudioSession](/documentation/avfaudio/avaudiosession)

### Accessing the shared audio session

- [class func sharedInstance() -> AVAudioSession](/documentation/avfaudio/avaudiosession/sharedinstance())

### Configuring standard audio behaviors

- [func setCategory(AVAudioSession.Category, mode: AVAudioSession.Mode, policy: AVAudioSession.RouteSharingPolicy, options: AVAudioSession.CategoryOptions) throws](/documentation/avfaudio/avaudiosession/setcategory(_:mode:policy:options:))
- [func setCategory(AVAudioSession.Category, mode: AVAudioSession.Mode, options: AVAudioSession.CategoryOptions) throws](/documentation/avfaudio/avaudiosession/setcategory(_:mode:options:))
- [func setCategory(AVAudioSession.Category, options: AVAudioSession.CategoryOptions) throws](/documentation/avfaudio/avaudiosession/setcategory(_:options:))
- [func setCategory(AVAudioSession.Category) throws](/documentation/avfaudio/avaudiosession/setcategory(_:))
- [func setMode(AVAudioSession.Mode) throws](/documentation/avfaudio/avaudiosession/setmode(_:))

### Configuring the spatial experience in visionOS

- [var intendedSpatialExperience: any AVAudioSessionSpatialExperience](/documentation/avfaudio/avaudiosession/intendedspatialexperience-1bpnq)
- [func setIntendedSpatialExperience(any AVAudioSessionSpatialExperience) throws](/documentation/avfaudio/avaudiosession/setintendedspatialexperience(_:))
- [AVAudioSessionSpatialExperience](/documentation/avfaudio/avaudiosessionspatialexperience-swift.protocol)

#### Experiences

- [static func fixed(soundStageSize: AVAudioSession.SoundStageSize) -> Self](/documentation/avfaudio/avaudiosessionspatialexperience-swift.protocol/fixed(soundstagesize:))
- [static func headTracked(soundStageSize: AVAudioSession.SoundStageSize, anchoringStrategy: AVAudioSession.AnchoringStrategy) -> Self](/documentation/avfaudio/avaudiosessionspatialexperience-swift.protocol/headtracked(soundstagesize:anchoringstrategy:))
- [static var bypassed: AVAudioSession.BypassedSpatialExperience](/documentation/avfaudio/avaudiosessionspatialexperience-swift.protocol/bypassed)
- [AVAudioSession.SoundStageSize](/documentation/avfaudio/avaudiosession/soundstagesize)

##### Sound stage sizes

- [case automatic](/documentation/avfaudio/avaudiosession/soundstagesize/automatic)
- [case small](/documentation/avfaudio/avaudiosession/soundstagesize/small)
- [case medium](/documentation/avfaudio/avaudiosession/soundstagesize/medium)
- [case large](/documentation/avfaudio/avaudiosession/soundstagesize/large)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiosession/soundstagesize/init(rawvalue:))
- [AVAudioSession.AnchoringStrategy](/documentation/avfaudio/avaudiosession/anchoringstrategy)

##### Anchoring strategies

- [case automatic](/documentation/avfaudio/avaudiosession/anchoringstrategy/automatic)
- [case front](/documentation/avfaudio/avaudiosession/anchoringstrategy/front)
- [case scene(identifier: String)](/documentation/avfaudio/avaudiosession/anchoringstrategy/scene(identifier:))
- [var isNowPlayingCandidate: Bool](/documentation/avfaudio/avaudiosession/isnowplayingcandidate)
- [func setIsNowPlayingCandidate(Bool) throws](/documentation/avfaudio/avaudiosession/setisnowplayingcandidate(_:))

### Activating the audio configuration

- [func setActive(Bool, options: AVAudioSession.SetActiveOptions) throws](/documentation/avfaudio/avaudiosession/setactive(_:options:))

#### Data Types

- [AVAudioSession.SetActiveOptions](/documentation/avfaudio/avaudiosession/setactiveoptions)

##### Creating an Activation Option

- [init(rawValue: UInt)](/documentation/avfaudio/avaudiosession/setactiveoptions/init(rawvalue:))

##### Getting Standard  Options

- [static var notifyOthersOnDeactivation: AVAudioSession.SetActiveOptions](/documentation/avfaudio/avaudiosession/setactiveoptions/notifyothersondeactivation)
- [var AVAudioSessionSetActiveFlags_NotifyOthersOnDeactivation: Int](/documentation/avfaudio/avaudiosessionsetactiveflags_notifyothersondeactivation)
- [func activate(options: AVAudioSessionActivationOptions, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/avfaudio/avaudiosession/activate(options:completionhandler:))
- [AVAudioSessionActivationOptions](/documentation/avfaudio/avaudiosessionactivationoptions)

#### Getting Standard Activation Options

- [init(rawValue: UInt)](/documentation/avfaudio/avaudiosessionactivationoptions/init(rawvalue:))

### Inspecting the category configuration

- [var category: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.property)
- [var availableCategories: [AVAudioSession.Category]](/documentation/avfaudio/avaudiosession/availablecategories)
- [AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct)

#### Creating a Category

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/category-swift.struct/init(rawvalue:))

#### Getting Standard Categories

- [static let ambient: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/ambient)
- [static let multiRoute: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/multiroute)
- [static let playAndRecord: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/playandrecord)
- [static let playback: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/playback)
- [static let record: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/record)
- [static let soloAmbient: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/soloambient)
- [static let audioProcessing: AVAudioSession.Category](/documentation/avfaudio/avaudiosession/category-swift.struct/audioprocessing)
- [var categoryOptions: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.property)
- [AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct)

#### Category options

- [static var allowAirPlay: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/allowairplay)
- [static var allowBluetooth: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/allowbluetooth)
- [static var allowBluetoothA2DP: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/allowbluetootha2dp)
- [static var allowBluetoothHFP: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/allowbluetoothhfp)
- [static var bluetoothHighQualityRecording: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/bluetoothhighqualityrecording)
- [static var defaultToSpeaker: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/defaulttospeaker)
- [static var duckOthers: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/duckothers)
- [static var farFieldInput: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/farfieldinput)
- [static var interruptSpokenAudioAndMixWithOthers: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/interruptspokenaudioandmixwithothers)
- [static var mixWithOthers: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/mixwithothers)
- [static var overrideMutedMicrophoneInterruption: AVAudioSession.CategoryOptions](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/overridemutedmicrophoneinterruption)

#### Initializers

- [init(rawValue: UInt)](/documentation/avfaudio/avaudiosession/categoryoptions-swift.struct/init(rawvalue:))

### Inspecting mode configuration

- [var mode: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.property)
- [var availableModes: [AVAudioSession.Mode]](/documentation/avfaudio/avaudiosession/availablemodes)
- [AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct)

#### Creating a Mode

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/mode-swift.struct/init(rawvalue:))

#### Getting Standard Session Modes

- [static let `default`: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/default)
- [static let dualRoute: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/dualroute)
- [static let gameChat: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/gamechat)
- [static let measurement: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/measurement)
- [static let moviePlayback: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/movieplayback)
- [static let shortFormVideo: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/shortformvideo)
- [static let spokenAudio: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/spokenaudio)
- [static let videoChat: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/videochat)
- [static let videoRecording: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/videorecording)
- [static let voiceChat: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/voicechat)
- [static let voicePrompt: AVAudioSession.Mode](/documentation/avfaudio/avaudiosession/mode-swift.struct/voiceprompt)

### Inspecting rendering mode and capabilities

- [var renderingMode: AVAudioSession.RenderingMode](/documentation/avfaudio/avaudiosession/renderingmode-swift.property)
- [AVAudioSession.RenderingMode](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum)

#### Getting the rendering modes

- [case monoStereo](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/monostereo)
- [case surround](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/surround)
- [case spatialAudio](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/spatialaudio)
- [case dolbyAudio](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/dolbyaudio)
- [case dolbyAtmos](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/dolbyatmos)
- [case notApplicable](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/notapplicable)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiosession/renderingmode-swift.enum/init(rawvalue:))
- [class let renderingModeChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/renderingmodechangenotification)

#### User information keys

- [let AVAudioSessionRenderingModeNewRenderingModeKey: String](/documentation/avfaudio/avaudiosessionrenderingmodenewrenderingmodekey)
- [var supportedOutputChannelLayouts: [AVAudioChannelLayout]](/documentation/avfaudio/avaudiosession/supportedoutputchannellayouts)
- [class let renderingCapabilitiesChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/renderingcapabilitieschangenotification)

### Inspecting the route sharing policy

- [var routeSharingPolicy: AVAudioSession.RouteSharingPolicy](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.property)
- [AVAudioSession.RouteSharingPolicy](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum)

#### Route-sharing policies

- [case `default`](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/default)
- [case longFormAudio](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/longformaudio)
- [case longFormVideo](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/longformvideo)
- [case independent](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/independent)
- [static var longForm: AVAudioSession.RouteSharingPolicy](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/longform)

#### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/routesharingpolicy-swift.enum/init(rawvalue:))

### Mixing with other audio

- [var isOtherAudioPlaying: Bool](/documentation/avfaudio/avaudiosession/isotheraudioplaying)
- [var secondaryAudioShouldBeSilencedHint: Bool](/documentation/avfaudio/avaudiosession/secondaryaudioshouldbesilencedhint)
- [class let silenceSecondaryAudioHintNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/silencesecondaryaudiohintnotification)

#### User Info Keys

- [let AVAudioSessionSilenceSecondaryAudioHintTypeKey: String](/documentation/avfaudio/avaudiosessionsilencesecondaryaudiohinttypekey)

#### User Info Values

- [AVAudioSession.SilenceSecondaryAudioHintType](/documentation/avfaudio/avaudiosession/silencesecondaryaudiohinttype)

##### Constants

- [case begin](/documentation/avfaudio/avaudiosession/silencesecondaryaudiohinttype/begin)
- [case end](/documentation/avfaudio/avaudiosession/silencesecondaryaudiohinttype/end)

##### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/silencesecondaryaudiohinttype/init(rawvalue:))
- [var allowHapticsAndSystemSoundsDuringRecording: Bool](/documentation/avfaudio/avaudiosession/allowhapticsandsystemsoundsduringrecording)
- [func setAllowHapticsAndSystemSoundsDuringRecording(Bool) throws](/documentation/avfaudio/avaudiosession/setallowhapticsandsystemsoundsduringrecording(_:))

### Managing audio routing

- [Audio routing](/documentation/avfaudio/audio-routing)

#### Inspecting the current route

- [var currentRoute: AVAudioSessionRouteDescription](/documentation/avfaudio/avaudiosession/currentroute)
- [AVAudioSessionRouteDescription](/documentation/avfaudio/avaudiosessionroutedescription)

##### Getting the Input and Output Ports

- [var inputs: [AVAudioSessionPortDescription]](/documentation/avfaudio/avaudiosessionroutedescription/inputs)
- [var outputs: [AVAudioSessionPortDescription]](/documentation/avfaudio/avaudiosessionroutedescription/outputs)
- [AVAudioSessionPortDescription](/documentation/avfaudio/avaudiosessionportdescription)

##### Getting the Port Attributes

- [var portName: String](/documentation/avfaudio/avaudiosessionportdescription/portname)
- [var portType: AVAudioSession.Port](/documentation/avfaudio/avaudiosessionportdescription/porttype)
- [AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port)

###### Getting Input Ports

- [static let builtInMic: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/builtinmic)
- [static let continuityMicrophone: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/continuitymicrophone)
- [static let headsetMic: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/headsetmic)
- [static let lineIn: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/linein)

###### Getting Output Ports

- [static let airPlay: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/airplay)
- [static let bluetoothA2DP: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/bluetootha2dp)
- [static let bluetoothLE: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/bluetoothle)
- [static let builtInReceiver: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/builtinreceiver)
- [static let builtInSpeaker: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/builtinspeaker)
- [static let HDMI: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/hdmi)
- [static let headphones: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/headphones)
- [static let lineOut: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/lineout)

###### Getting I/O Ports

- [static let AVB: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/avb)
- [static let PCI: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/pci)
- [static let bluetoothHFP: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/bluetoothhfp)
- [static let carAudio: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/caraudio)
- [static let displayPort: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/displayport)
- [static let fireWire: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/firewire)
- [static let thunderbolt: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/thunderbolt)
- [static let usbAudio: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/usbaudio)
- [static let virtual: AVAudioSession.Port](/documentation/avfaudio/avaudiosession/port/virtual)

###### Initializers

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/port/init(rawvalue:))
- [var channels: [AVAudioSessionChannelDescription]?](/documentation/avfaudio/avaudiosessionportdescription/channels)
- [AVAudioSessionChannelDescription](/documentation/avfaudio/avaudiosessionchanneldescription)

###### Getting the Channel Information

- [var channelName: String](/documentation/avfaudio/avaudiosessionchanneldescription/channelname)
- [var channelNumber: Int](/documentation/avfaudio/avaudiosessionchanneldescription/channelnumber)
- [var owningPortUID: String](/documentation/avfaudio/avaudiosessionchanneldescription/owningportuid)
- [var channelLabel: AudioChannelLabel](/documentation/avfaudio/avaudiosessionchanneldescription/channellabel)
- [var uid: String](/documentation/avfaudio/avaudiosessionportdescription/uid)
- [var hasHardwareVoiceCallProcessing: Bool](/documentation/avfaudio/avaudiosessionportdescription/hashardwarevoicecallprocessing)
- [var isSpatialAudioEnabled: Bool](/documentation/avfaudio/avaudiosessionportdescription/isspatialaudioenabled)

##### Managing a Port’s Data Sources

- [var dataSources: [AVAudioSessionDataSourceDescription]?](/documentation/avfaudio/avaudiosessionportdescription/datasources)
- [var selectedDataSource: AVAudioSessionDataSourceDescription?](/documentation/avfaudio/avaudiosessionportdescription/selecteddatasource)
- [var preferredDataSource: AVAudioSessionDataSourceDescription?](/documentation/avfaudio/avaudiosessionportdescription/preferreddatasource)
- [func setPreferredDataSource(AVAudioSessionDataSourceDescription?) throws](/documentation/avfaudio/avaudiosessionportdescription/setpreferreddatasource(_:))

##### Accessing the port extension

- [var bluetoothMicrophoneExtension: AVAudioSessionPortExtensionBluetoothMicrophone?](/documentation/avfaudio/avaudiosessionportdescription/bluetoothmicrophoneextension)
- [AVAudioSessionPortExtensionBluetoothMicrophone](/documentation/avfaudio/avaudiosessionportextensionbluetoothmicrophone)

###### Inspecting the port extension

- [var farFieldCapture: AVAudioSessionCapability](/documentation/avfaudio/avaudiosessionportextensionbluetoothmicrophone/farfieldcapture)
- [var highQualityRecording: AVAudioSessionCapability](/documentation/avfaudio/avaudiosessionportextensionbluetoothmicrophone/highqualityrecording)
- [AVAudioSessionCapability](/documentation/avfaudio/avaudiosessioncapability)

###### Inspecting a capability

- [var isEnabled: Bool](/documentation/avfaudio/avaudiosessioncapability/isenabled)
- [var isSupported: Bool](/documentation/avfaudio/avaudiosessioncapability/issupported)
- [class let routeChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/routechangenotification)

##### User Info Keys

- [let AVAudioSessionRouteChangeReasonKey: String](/documentation/avfaudio/avaudiosessionroutechangereasonkey)
- [let AVAudioSessionRouteChangePreviousRouteKey: String](/documentation/avfaudio/avaudiosessionroutechangepreviousroutekey)

##### User Info Values

- [AVAudioSession.RouteChangeReason](/documentation/avfaudio/avaudiosession/routechangereason)

###### Route Change Reasons

- [case unknown](/documentation/avfaudio/avaudiosession/routechangereason/unknown)
- [case newDeviceAvailable](/documentation/avfaudio/avaudiosession/routechangereason/newdeviceavailable)
- [case oldDeviceUnavailable](/documentation/avfaudio/avaudiosession/routechangereason/olddeviceunavailable)
- [case categoryChange](/documentation/avfaudio/avaudiosession/routechangereason/categorychange)
- [case override](/documentation/avfaudio/avaudiosession/routechangereason/override)
- [case wakeFromSleep](/documentation/avfaudio/avaudiosession/routechangereason/wakefromsleep)
- [case noSuitableRouteForCategory](/documentation/avfaudio/avaudiosession/routechangereason/nosuitablerouteforcategory)
- [case routeConfigurationChange](/documentation/avfaudio/avaudiosession/routechangereason/routeconfigurationchange)

###### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/routechangereason/init(rawvalue:))

#### Configuring inputs

- [var isInputAvailable: Bool](/documentation/avfaudio/avaudiosession/isinputavailable)
- [var availableInputs: [AVAudioSessionPortDescription]?](/documentation/avfaudio/avaudiosession/availableinputs)
- [var preferredInput: AVAudioSessionPortDescription?](/documentation/avfaudio/avaudiosession/preferredinput)
- [func setPreferredInput(AVAudioSessionPortDescription?) throws](/documentation/avfaudio/avaudiosession/setpreferredinput(_:))
- [var inputDataSource: AVAudioSessionDataSourceDescription?](/documentation/avfaudio/avaudiosession/inputdatasource)
- [var inputDataSources: [AVAudioSessionDataSourceDescription]?](/documentation/avfaudio/avaudiosession/inputdatasources)
- [func setInputDataSource(AVAudioSessionDataSourceDescription?) throws](/documentation/avfaudio/avaudiosession/setinputdatasource(_:))
- [class let availableInputsChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/availableinputschangenotification)

#### Configuring outputs

- [var outputDataSources: [AVAudioSessionDataSourceDescription]?](/documentation/avfaudio/avaudiosession/outputdatasources)
- [var outputDataSource: AVAudioSessionDataSourceDescription?](/documentation/avfaudio/avaudiosession/outputdatasource)
- [func setOutputDataSource(AVAudioSessionDataSourceDescription?) throws](/documentation/avfaudio/avaudiosession/setoutputdatasource(_:))
- [AVAudioSessionDataSourceDescription](/documentation/avfaudio/avaudiosessiondatasourcedescription)

##### Identifying a Data Source

- [var dataSourceID: NSNumber](/documentation/avfaudio/avaudiosessiondatasourcedescription/datasourceid)
- [var dataSourceName: String](/documentation/avfaudio/avaudiosessiondatasourcedescription/datasourcename)

##### Retrieving the Data Source Location

- [var location: AVAudioSession.Location?](/documentation/avfaudio/avaudiosessiondatasourcedescription/location)
- [AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location)

###### Creating a Location

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/location/init(rawvalue:))

###### Getting Standard Locations

- [static let lower: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/lower)
- [static let upper: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/upper)

###### Deprecated

- [Deprecated Symbols](/documentation/avfaudio/location-deprecated-symbols)

###### Locations

- [static var orientationFront: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationfront)
- [static var orientationBack: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationback)
- [static var orientationBottom: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationbottom)
- [static var orientationTop: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationtop)
- [static var orientationLeft: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationleft)
- [static var orientationRight: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationright)
- [static var polarPatternCardioid: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatterncardioid)
- [static var polarPatternOmnidirectional: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatternomnidirectional)
- [static var polarPatternSubcardioid: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatternsubcardioid)

###### Type Properties

- [static var orientationBack: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationback)
- [static var orientationBottom: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationbottom)
- [static var orientationFront: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationfront)
- [static var orientationLeft: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationleft)
- [static var orientationRight: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationright)
- [static var orientationTop: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/orientationtop)
- [static var polarPatternCardioid: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatterncardioid)
- [static var polarPatternOmnidirectional: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatternomnidirectional)
- [static var polarPatternSubcardioid: AVAudioSession.Location](/documentation/avfaudio/avaudiosession/location/polarpatternsubcardioid)

##### Retrieving the Data Source Orientation

- [var orientation: AVAudioSession.Orientation?](/documentation/avfaudio/avaudiosessiondatasourcedescription/orientation)
- [AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation)

###### Creating an Orientation

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/orientation/init(rawvalue:))

###### Getting Standard Orientations

- [static let top: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/top)
- [static let bottom: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/bottom)
- [static let front: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/front)
- [static let back: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/back)
- [static let left: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/left)
- [static let right: AVAudioSession.Orientation](/documentation/avfaudio/avaudiosession/orientation/right)

##### Configuring Microphone Directivity

- [var selectedPolarPattern: AVAudioSession.PolarPattern?](/documentation/avfaudio/avaudiosessiondatasourcedescription/selectedpolarpattern)
- [var supportedPolarPatterns: [AVAudioSession.PolarPattern]?](/documentation/avfaudio/avaudiosessiondatasourcedescription/supportedpolarpatterns)
- [var preferredPolarPattern: AVAudioSession.PolarPattern?](/documentation/avfaudio/avaudiosessiondatasourcedescription/preferredpolarpattern)
- [func setPreferredPolarPattern(AVAudioSession.PolarPattern?) throws](/documentation/avfaudio/avaudiosessiondatasourcedescription/setpreferredpolarpattern(_:))
- [AVAudioSession.PolarPattern](/documentation/avfaudio/avaudiosession/polarpattern)

###### Creating a Polar Pattern

- [init(rawValue: String)](/documentation/avfaudio/avaudiosession/polarpattern/init(rawvalue:))

###### Getting Standard Polar Patterns

- [static let stereo: AVAudioSession.PolarPattern](/documentation/avfaudio/avaudiosession/polarpattern/stereo)
- [static let cardioid: AVAudioSession.PolarPattern](/documentation/avfaudio/avaudiosession/polarpattern/cardioid)
- [static let subcardioid: AVAudioSession.PolarPattern](/documentation/avfaudio/avaudiosession/polarpattern/subcardioid)
- [static let omnidirectional: AVAudioSession.PolarPattern](/documentation/avfaudio/avaudiosession/polarpattern/omnidirectional)
- [func overrideOutputAudioPort(AVAudioSession.PortOverride) throws](/documentation/avfaudio/avaudiosession/overrideoutputaudioport(_:))

##### Data Types

- [AVAudioSession.PortOverride](/documentation/avfaudio/avaudiosession/portoverride)

###### Port Override Types

- [case none](/documentation/avfaudio/avaudiosession/portoverride/none)
- [case speaker](/documentation/avfaudio/avaudiosession/portoverride/speaker)

###### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/portoverride/init(rawvalue:))

### Preparing for long-form video playback

- [func prepareRouteSelectionForPlayback(completionHandler: (Bool, AVAudioSession.RouteSelection) -> Void)](/documentation/avfaudio/avaudiosession/preparerouteselectionforplayback(completionhandler:))
- [AVAudioSession.RouteSelection](/documentation/avfaudio/avaudiosession/routeselection)

#### Constants

- [case none](/documentation/avfaudio/avaudiosession/routeselection/none)
- [case local](/documentation/avfaudio/avaudiosession/routeselection/local)
- [case external](/documentation/avfaudio/avaudiosession/routeselection/external)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiosession/routeselection/init(rawvalue:))

### Handling interruptions

- [var prefersNoInterruptionsFromSystemAlerts: Bool](/documentation/avfaudio/avaudiosession/prefersnointerruptionsfromsystemalerts)
- [func setPrefersNoInterruptionsFromSystemAlerts(Bool) throws](/documentation/avfaudio/avaudiosession/setprefersnointerruptionsfromsystemalerts(_:))
- [var prefersInterruptionOnRouteDisconnect: Bool](/documentation/avfaudio/avaudiosession/prefersinterruptiononroutedisconnect)
- [func setPrefersInterruptionOnRouteDisconnect(Bool) throws](/documentation/avfaudio/avaudiosession/setprefersinterruptiononroutedisconnect(_:))
- [class let interruptionNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/interruptionnotification)

#### User Info Keys

- [let AVAudioSessionInterruptionTypeKey: String](/documentation/avfaudio/avaudiosessioninterruptiontypekey)
- [let AVAudioSessionInterruptionOptionKey: String](/documentation/avfaudio/avaudiosessioninterruptionoptionkey)
- [let AVAudioSessionInterruptionReasonKey: String](/documentation/avfaudio/avaudiosessioninterruptionreasonkey)
- [let AVAudioSessionInterruptionWasSuspendedKey: String](/documentation/avfaudio/avaudiosessioninterruptionwassuspendedkey)

#### User Info Values

- [AVAudioSession.InterruptionType](/documentation/avfaudio/avaudiosession/interruptiontype)

##### Interruption Types

- [case began](/documentation/avfaudio/avaudiosession/interruptiontype/began)
- [case ended](/documentation/avfaudio/avaudiosession/interruptiontype/ended)

##### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/interruptiontype/init(rawvalue:))
- [AVAudioSession.InterruptionOptions](/documentation/avfaudio/avaudiosession/interruptionoptions)

##### Creating an Interruption Option

- [init(rawValue: UInt)](/documentation/avfaudio/avaudiosession/interruptionoptions/init(rawvalue:))

##### Getting Standard Interruption Options

- [static var shouldResume: AVAudioSession.InterruptionOptions](/documentation/avfaudio/avaudiosession/interruptionoptions/shouldresume)
- [AVAudioSession.InterruptionReason](/documentation/avfaudio/avaudiosession/interruptionreason)

##### Interruption Reasons

- [case `default`](/documentation/avfaudio/avaudiosession/interruptionreason/default)
- [case builtInMicMuted](/documentation/avfaudio/avaudiosession/interruptionreason/builtinmicmuted)
- [case routeDisconnected](/documentation/avfaudio/avaudiosession/interruptionreason/routedisconnected)
- [case sceneWasBackgrounded](/documentation/avfaudio/avaudiosession/interruptionreason/scenewasbackgrounded)
- [case appWasSuspended](/documentation/avfaudio/avaudiosession/interruptionreason/appwassuspended)

##### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/interruptionreason/init(rawvalue:))

### Monitoring spatial capabilities

- [class let spatialPlaybackCapabilitiesChangedNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/spatialplaybackcapabilitieschangednotification)

#### User Info Keys

- [let AVAudioSessionSpatialAudioEnabledKey: String](/documentation/avfaudio/avaudiosessionspatialaudioenabledkey)

### Inspecting the audio prompt style

- [var promptStyle: AVAudioSession.PromptStyle](/documentation/avfaudio/avaudiosession/promptstyle-swift.property)
- [AVAudioSession.PromptStyle](/documentation/avfaudio/avaudiosession/promptstyle-swift.enum)

#### Prompt Styles

- [case none](/documentation/avfaudio/avaudiosession/promptstyle-swift.enum/none)
- [case short](/documentation/avfaudio/avaudiosession/promptstyle-swift.enum/short)
- [case normal](/documentation/avfaudio/avaudiosession/promptstyle-swift.enum/normal)

#### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/promptstyle-swift.enum/init(rawvalue:))

### Enabling stereo recording

- [var inputOrientation: AVAudioSession.StereoOrientation](/documentation/avfaudio/avaudiosession/inputorientation)
- [var preferredInputOrientation: AVAudioSession.StereoOrientation](/documentation/avfaudio/avaudiosession/preferredinputorientation)
- [func setPreferredInputOrientation(AVAudioSession.StereoOrientation) throws](/documentation/avfaudio/avaudiosession/setpreferredinputorientation(_:))
- [AVAudioSession.StereoOrientation](/documentation/avfaudio/avaudiosession/stereoorientation)

#### Stereo Orientations

- [case none](/documentation/avfaudio/avaudiosession/stereoorientation/none)
- [case portrait](/documentation/avfaudio/avaudiosession/stereoorientation/portrait)
- [case portraitUpsideDown](/documentation/avfaudio/avaudiosession/stereoorientation/portraitupsidedown)
- [case landscapeRight](/documentation/avfaudio/avaudiosession/stereoorientation/landscaperight)
- [case landscapeLeft](/documentation/avfaudio/avaudiosession/stereoorientation/landscapeleft)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiosession/stereoorientation/init(rawvalue:))

### Enabling adding audio to calls

- [var isMicrophoneInjectionAvailable: Bool](/documentation/avfaudio/avaudiosession/ismicrophoneinjectionavailable)
- [var preferredMicrophoneInjectionMode: AVAudioSession.MicrophoneInjectionMode](/documentation/avfaudio/avaudiosession/preferredmicrophoneinjectionmode)
- [func setPreferredMicrophoneInjectionMode(AVAudioSession.MicrophoneInjectionMode) throws](/documentation/avfaudio/avaudiosession/setpreferredmicrophoneinjectionmode(_:))
- [AVAudioSession.MicrophoneInjectionMode](/documentation/avfaudio/avaudiosession/microphoneinjectionmode)

#### Microphone injection modes

- [case none](/documentation/avfaudio/avaudiosession/microphoneinjectionmode/none)
- [case spokenAudio](/documentation/avfaudio/avaudiosession/microphoneinjectionmode/spokenaudio)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiosession/microphoneinjectionmode/init(rawvalue:))
- [class let microphoneInjectionCapabilitiesChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/microphoneinjectioncapabilitieschangenotification)

#### User-information keys

- [let AVAudioSessionMicrophoneInjectionIsAvailableKey: String](/documentation/avfaudio/avaudiosessionmicrophoneinjectionisavailablekey)

### Configuring echo cancellation

- [var isEchoCancelledInputAvailable: Bool](/documentation/avfaudio/avaudiosession/isechocancelledinputavailable)
- [var isEchoCancelledInputEnabled: Bool](/documentation/avfaudio/avaudiosession/isechocancelledinputenabled)
- [func setPrefersEchoCancelledInput(Bool) throws](/documentation/avfaudio/avaudiosession/setprefersechocancelledinput(_:))
- [var prefersEchoCancelledInput: Bool](/documentation/avfaudio/avaudiosession/prefersechocancelledinput)

### Configuring audio muting

- [var isOutputMuted: Bool](/documentation/avfaudio/avaudiosession/isoutputmuted)
- [func setOutputMuted(Bool) throws](/documentation/avfaudio/avaudiosession/setoutputmuted(_:))
- [class let outputMuteStateChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/outputmutestatechangenotification)
- [class let muteStateKey: String](/documentation/avfaudio/avaudiosession/mutestatekey)
- [class let userIntentToUnmuteOutputNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/userintenttounmuteoutputnotification)
- [class let userIntentToUnmuteOutputNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/userintenttounmuteoutputnotification)
- [class let muteStateKey: String](/documentation/avfaudio/avaudiosession/mutestatekey)

### Configuring device settings

- [Audio hardware](/documentation/avfaudio/audio-hardware)

#### Configuring sample rate

- [var sampleRate: Double](/documentation/avfaudio/avaudiosession/samplerate)
- [var preferredSampleRate: Double](/documentation/avfaudio/avaudiosession/preferredsamplerate)
- [func setPreferredSampleRate(Double) throws](/documentation/avfaudio/avaudiosession/setpreferredsamplerate(_:))

#### Setting input gain

- [var inputGain: Float](/documentation/avfaudio/avaudiosession/inputgain)
- [var isInputGainSettable: Bool](/documentation/avfaudio/avaudiosession/isinputgainsettable)
- [func setInputGain(Float) throws](/documentation/avfaudio/avaudiosession/setinputgain(_:))

#### Configuring I/O buffer duration

- [var ioBufferDuration: TimeInterval](/documentation/avfaudio/avaudiosession/iobufferduration)
- [var preferredIOBufferDuration: TimeInterval](/documentation/avfaudio/avaudiosession/preferrediobufferduration)
- [func setPreferredIOBufferDuration(TimeInterval) throws](/documentation/avfaudio/avaudiosession/setpreferrediobufferduration(_:))

#### Inspecting latency

- [var inputLatency: TimeInterval](/documentation/avfaudio/avaudiosession/inputlatency)
- [var outputLatency: TimeInterval](/documentation/avfaudio/avaudiosession/outputlatency)

#### Inspecting output volume

- [var outputVolume: Float](/documentation/avfaudio/avaudiosession/outputvolume)

#### Setting the number of input channels

- [var preferredInputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/preferredinputnumberofchannels)
- [func setPreferredInputNumberOfChannels(Int) throws](/documentation/avfaudio/avaudiosession/setpreferredinputnumberofchannels(_:))
- [var inputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/inputnumberofchannels)
- [var maximumInputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/maximuminputnumberofchannels)

#### Setting the number of output channels

- [var preferredOutputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/preferredoutputnumberofchannels)
- [func setPreferredOutputNumberOfChannels(Int) throws](/documentation/avfaudio/avaudiosession/setpreferredoutputnumberofchannels(_:))
- [var outputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/outputnumberofchannels)
- [var maximumOutputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/maximumoutputnumberofchannels)

#### Configuring multichannel support

- [var supportsMultichannelContent: Bool](/documentation/avfaudio/avaudiosession/supportsmultichannelcontent)
- [func setSupportsMultichannelContent(Bool) throws](/documentation/avfaudio/avaudiosession/setsupportsmultichannelcontent(_:))

### Setting the aggregated I/O preference

- [func setAggregatedIOPreference(AVAudioSession.IOType) throws](/documentation/avfaudio/avaudiosession/setaggregatediopreference(_:))
- [AVAudioSession.IOType](/documentation/avfaudio/avaudiosession/iotype)

#### I/O Types

- [case notSpecified](/documentation/avfaudio/avaudiosession/iotype/notspecified)
- [case aggregated](/documentation/avfaudio/avaudiosession/iotype/aggregated)

#### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/iotype/init(rawvalue:))

### Handling a change of media services

- [class let mediaServicesWereResetNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/mediaserviceswereresetnotification)
- [class let mediaServicesWereLostNotification: NSNotification.Name](/documentation/avfaudio/avaudiosession/mediaserviceswerelostnotification)

### Errors

- [AVAudioSession.ErrorCode](/documentation/coreaudiotypes/avaudiosession/errorcode)

### Deprecated

- [Deprecated Symbols](/documentation/avfaudio/deprecated-symbols)

#### Activating an audio session

- [func setActive(Bool, withFlags: Int) throws](/documentation/avfaudio/avaudiosession/setactive(_:withflags:))

#### Requesting permission to record

- [var recordPermission: AVAudioSession.RecordPermission](/documentation/avfaudio/avaudiosession/recordpermission-swift.property)

##### Data Types

- [AVAudioSession.RecordPermission](/documentation/avfaudio/avaudiosession/recordpermission-swift.enum)

###### Record Permissions

- [case undetermined](/documentation/avfaudio/avaudiosession/recordpermission-swift.enum/undetermined)
- [case denied](/documentation/avfaudio/avaudiosession/recordpermission-swift.enum/denied)
- [case granted](/documentation/avfaudio/avaudiosession/recordpermission-swift.enum/granted)

###### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiosession/recordpermission-swift.enum/init(rawvalue:))
- [func requestRecordPermission((Bool) -> Void)](/documentation/avfaudio/avaudiosession/requestrecordpermission(_:))

#### Inspecting audio hardware

- [var currentHardwareInputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/currenthardwareinputnumberofchannels)
- [var currentHardwareOutputNumberOfChannels: Int](/documentation/avfaudio/avaudiosession/currenthardwareoutputnumberofchannels)
- [var currentHardwareSampleRate: Double](/documentation/avfaudio/avaudiosession/currenthardwaresamplerate)
- [var inputIsAvailable: Bool](/documentation/avfaudio/avaudiosession/inputisavailable)
- [var preferredHardwareSampleRate: Double](/documentation/avfaudio/avaudiosession/preferredhardwaresamplerate)
- [func setPreferredHardwareSampleRate(Double) throws](/documentation/avfaudio/avaudiosession/setpreferredhardwaresamplerate(_:))

#### Responding to audio session changes

- [var delegate: (any AVAudioSessionDelegate)?](/documentation/avfaudio/avaudiosession/delegate)
- [AVAudioSessionDelegate](/documentation/avfaudio/avaudiosessiondelegate)

##### Delegate Methods

- [func beginInterruption()](/documentation/avfaudio/avaudiosessiondelegate/begininterruption())
- [func endInterruption()](/documentation/avfaudio/avaudiosessiondelegate/endinterruption())
- [func endInterruption(withFlags: Int)](/documentation/avfaudio/avaudiosessiondelegate/endinterruption(withflags:))
- [func inputIsAvailableChanged(Bool)](/documentation/avfaudio/avaudiosessiondelegate/inputisavailablechanged(_:))

#### Handling audio session interruptions

- [var AVAudioSessionInterruptionFlags_ShouldResume: Int](/documentation/avfaudio/avaudiosessioninterruptionflags_shouldresume)

### Structures

- [AVAudioSession.BypassedSpatialExperience](/documentation/avfaudio/avaudiosession/bypassedspatialexperience)
- [AVAudioSession.FixedSpatialExperience](/documentation/avfaudio/avaudiosession/fixedspatialexperience)

#### Inspecting the experience

- [var soundStageSize: AVAudioSession.SoundStageSize](/documentation/avfaudio/avaudiosession/fixedspatialexperience/soundstagesize)
- [AVAudioSession.HeadTrackedSpatialExperience](/documentation/avfaudio/avaudiosession/headtrackedspatialexperience)

#### Inspecting the experience

- [var anchoringStrategy: AVAudioSession.AnchoringStrategy](/documentation/avfaudio/avaudiosession/headtrackedspatialexperience/anchoringstrategy)
- [var soundStageSize: AVAudioSession.SoundStageSize](/documentation/avfaudio/avaudiosession/headtrackedspatialexperience/soundstagesize)

### Enumerations

- [AVAudioSession.AnchoringStrategy](/documentation/avfaudio/avaudiosession/anchoringstrategy)

#### Anchoring strategies

- [case automatic](/documentation/avfaudio/avaudiosession/anchoringstrategy/automatic)
- [case front](/documentation/avfaudio/avaudiosession/anchoringstrategy/front)
- [case scene(identifier: String)](/documentation/avfaudio/avaudiosession/anchoringstrategy/scene(identifier:))
- [AVAudioApplication](/documentation/avfaudio/avaudioapplication)

### Accessing the shared instance

- [class var shared: AVAudioApplication](/documentation/avfaudio/avaudioapplication/shared)

### Requesting audio recording permission

- [class func requestRecordPermission(completionHandler: (Bool) -> Void)](/documentation/avfaudio/avaudioapplication/requestrecordpermission(completionhandler:))
- [var recordPermission: AVAudioApplication.recordPermission](/documentation/avfaudio/avaudioapplication/recordpermission-swift.property)
- [AVAudioApplication.recordPermission](/documentation/avfaudio/avaudioapplication/recordpermission-swift.enum)

#### Permissions

- [case undetermined](/documentation/avfaudio/avaudioapplication/recordpermission-swift.enum/undetermined)
- [case granted](/documentation/avfaudio/avaudioapplication/recordpermission-swift.enum/granted)
- [case denied](/documentation/avfaudio/avaudioapplication/recordpermission-swift.enum/denied)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioapplication/recordpermission-swift.enum/init(rawvalue:))

### Requesting microphone injection permission

- [class func requestMicrophoneInjectionPermission(completionHandler: (AVAudioApplication.MicrophoneInjectionPermission) -> Void)](/documentation/avfaudio/avaudioapplication/requestmicrophoneinjectionpermission(completionhandler:))
- [var microphoneInjectionPermission: AVAudioApplication.MicrophoneInjectionPermission](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.property)
- [AVAudioApplication.MicrophoneInjectionPermission](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum)

#### Permissions

- [case serviceDisabled](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum/servicedisabled)
- [case undetermined](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum/undetermined)
- [case granted](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum/granted)
- [case denied](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum/denied)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioapplication/microphoneinjectionpermission-swift.enum/init(rawvalue:))

### Managing audio input mute state

- [var isInputMuted: Bool](/documentation/avfaudio/avaudioapplication/isinputmuted)
- [func setInputMuted(Bool) throws](/documentation/avfaudio/avaudioapplication/setinputmuted(_:))
- [class let inputMuteStateChangeNotification: NSNotification.Name](/documentation/avfaudio/avaudioapplication/inputmutestatechangenotification)

#### User information keys

- [class let muteStateKey: String](/documentation/avfaudio/avaudioapplication/mutestatekey)
- [func setInputMuteStateChangeHandler(((Bool) -> Bool)?) throws](/documentation/avfaudio/avaudioapplication/setinputmutestatechangehandler(_:))
- [AVAudioRoutingArbiter](/documentation/avfaudio/avaudioroutingarbiter)

### Creating a Routing Arbiter

- [class var shared: AVAudioRoutingArbiter](/documentation/avfaudio/avaudioroutingarbiter/shared)

### Participating in AirPods Automatic Switching

- [func begin(category: AVAudioRoutingArbiter.Category, completionHandler: (Bool, (any Error)?) -> Void)](/documentation/avfaudio/avaudioroutingarbiter/begin(category:completionhandler:))
- [AVAudioRoutingArbiter.Category](/documentation/avfaudio/avaudioroutingarbiter/category)

#### Categories

- [case playback](/documentation/avfaudio/avaudioroutingarbiter/category/playback)
- [case playAndRecord](/documentation/avfaudio/avaudioroutingarbiter/category/playandrecord)
- [case playAndRecordVoice](/documentation/avfaudio/avaudioroutingarbiter/category/playandrecordvoice)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioroutingarbiter/category/init(rawvalue:))
- [func leave()](/documentation/avfaudio/avaudioroutingarbiter/leave())

## Basic playback and recording

- [AVAudioPlayer](/documentation/avfaudio/avaudioplayer)

### Creating an audio player

- [init(contentsOf: URL) throws](/documentation/avfaudio/avaudioplayer/init(contentsof:))
- [init(contentsOf: URL, fileTypeHint: String?) throws](/documentation/avfaudio/avaudioplayer/init(contentsof:filetypehint:))
- [init(data: Data) throws](/documentation/avfaudio/avaudioplayer/init(data:))
- [init(data: Data, fileTypeHint: String?) throws](/documentation/avfaudio/avaudioplayer/init(data:filetypehint:))

### Controlling playback

- [func prepareToPlay() -> Bool](/documentation/avfaudio/avaudioplayer/preparetoplay())
- [func play() -> Bool](/documentation/avfaudio/avaudioplayer/play())
- [func play(atTime: TimeInterval) -> Bool](/documentation/avfaudio/avaudioplayer/play(attime:))
- [func pause()](/documentation/avfaudio/avaudioplayer/pause())
- [func stop()](/documentation/avfaudio/avaudioplayer/stop())
- [var isPlaying: Bool](/documentation/avfaudio/avaudioplayer/isplaying)

### Configuring playback settings

- [var volume: Float](/documentation/avfaudio/avaudioplayer/volume)
- [func setVolume(Float, fadeDuration: TimeInterval)](/documentation/avfaudio/avaudioplayer/setvolume(_:fadeduration:))
- [var pan: Float](/documentation/avfaudio/avaudioplayer/pan)
- [var enableRate: Bool](/documentation/avfaudio/avaudioplayer/enablerate)
- [var rate: Float](/documentation/avfaudio/avaudioplayer/rate)
- [var numberOfLoops: Int](/documentation/avfaudio/avaudioplayer/numberofloops)

### Accessing player timing

- [var currentTime: TimeInterval](/documentation/avfaudio/avaudioplayer/currenttime)
- [var duration: TimeInterval](/documentation/avfaudio/avaudioplayer/duration)

### Configuring the Spatial Audio experience

- [var intendedSpatialExperience: any SpatialAudioExperience](/documentation/avfaudio/avaudioplayer/intendedspatialexperience-27klj)

### Managing audio channels

- [var numberOfChannels: Int](/documentation/avfaudio/avaudioplayer/numberofchannels)
- [var channelAssignments: [AVAudioSessionChannelDescription]?](/documentation/avfaudio/avaudioplayer/channelassignments)

### Managing audio-level metering

- [var isMeteringEnabled: Bool](/documentation/avfaudio/avaudioplayer/ismeteringenabled)
- [func updateMeters()](/documentation/avfaudio/avaudioplayer/updatemeters())
- [func averagePower(forChannel: Int) -> Float](/documentation/avfaudio/avaudioplayer/averagepower(forchannel:))
- [func peakPower(forChannel: Int) -> Float](/documentation/avfaudio/avaudioplayer/peakpower(forchannel:))

### Responding to player events

- [var delegate: (any AVAudioPlayerDelegate)?](/documentation/avfaudio/avaudioplayer/delegate)
- [AVAudioPlayerDelegate](/documentation/avfaudio/avaudioplayerdelegate)

#### Responding to Playback Completion

- [func audioPlayerDidFinishPlaying(AVAudioPlayer, successfully: Bool)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerdidfinishplaying(_:successfully:))

#### Responding to Audio Decoding Errors

- [func audioPlayerDecodeErrorDidOccur(AVAudioPlayer, error: (any Error)?)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerdecodeerrordidoccur(_:error:))

#### Responding to Audio Interruptions

- [func audioPlayerBeginInterruption(AVAudioPlayer)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerbegininterruption(_:))
- [func audioPlayerEndInterruption(AVAudioPlayer)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerendinterruption(_:))
- [func audioPlayerEndInterruption(AVAudioPlayer, withOptions: Int)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerendinterruption(_:withoptions:))
- [func audioPlayerEndInterruption(AVAudioPlayer, withFlags: Int)](/documentation/avfaudio/avaudioplayerdelegate/audioplayerendinterruption(_:withflags:))

### Inspecting the audio data

- [var url: URL?](/documentation/avfaudio/avaudioplayer/url)
- [var data: Data?](/documentation/avfaudio/avaudioplayer/data)
- [var format: AVAudioFormat](/documentation/avfaudio/avaudioplayer/format)
- [var settings: [String : Any]](/documentation/avfaudio/avaudioplayer/settings)

### Accessing device information

- [var currentDevice: String?](/documentation/avfaudio/avaudioplayer/currentdevice)
- [var deviceCurrentTime: TimeInterval](/documentation/avfaudio/avaudioplayer/devicecurrenttime)
- [AVAudioRecorder](/documentation/avfaudio/avaudiorecorder)

### Creating an audio recorder

- [init(url: URL, settings: [String : Any]) throws](/documentation/avfaudio/avaudiorecorder/init(url:settings:))
- [init(url: URL, format: AVAudioFormat) throws](/documentation/avfaudio/avaudiorecorder/init(url:format:))

### Controlling recording

- [func prepareToRecord() -> Bool](/documentation/avfaudio/avaudiorecorder/preparetorecord())
- [func record() -> Bool](/documentation/avfaudio/avaudiorecorder/record())
- [func record(atTime: TimeInterval) -> Bool](/documentation/avfaudio/avaudiorecorder/record(attime:))
- [func record(forDuration: TimeInterval) -> Bool](/documentation/avfaudio/avaudiorecorder/record(forduration:))
- [func record(atTime: TimeInterval, forDuration: TimeInterval) -> Bool](/documentation/avfaudio/avaudiorecorder/record(attime:forduration:))
- [func pause()](/documentation/avfaudio/avaudiorecorder/pause())
- [func stop()](/documentation/avfaudio/avaudiorecorder/stop())
- [var isRecording: Bool](/documentation/avfaudio/avaudiorecorder/isrecording)
- [func deleteRecording() -> Bool](/documentation/avfaudio/avaudiorecorder/deleterecording())

### Accessing recorder timing

- [var currentTime: TimeInterval](/documentation/avfaudio/avaudiorecorder/currenttime)
- [var deviceCurrentTime: TimeInterval](/documentation/avfaudio/avaudiorecorder/devicecurrenttime)

### Managing audio channels

- [var channelAssignments: [AVAudioSessionChannelDescription]?](/documentation/avfaudio/avaudiorecorder/channelassignments)

### Managing audio-level metering

- [var isMeteringEnabled: Bool](/documentation/avfaudio/avaudiorecorder/ismeteringenabled)
- [func updateMeters()](/documentation/avfaudio/avaudiorecorder/updatemeters())
- [func averagePower(forChannel: Int) -> Float](/documentation/avfaudio/avaudiorecorder/averagepower(forchannel:))
- [func peakPower(forChannel: Int) -> Float](/documentation/avfaudio/avaudiorecorder/peakpower(forchannel:))

### Responding to recorder events

- [var delegate: (any AVAudioRecorderDelegate)?](/documentation/avfaudio/avaudiorecorder/delegate)
- [AVAudioRecorderDelegate](/documentation/avfaudio/avaudiorecorderdelegate)

#### Responding to Recording Completion

- [func audioRecorderDidFinishRecording(AVAudioRecorder, successfully: Bool)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderdidfinishrecording(_:successfully:))

#### Responding to Audio Encoding Errors

- [func audioRecorderEncodeErrorDidOccur(AVAudioRecorder, error: (any Error)?)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderencodeerrordidoccur(_:error:))

#### Responding to Audio Interruptions

- [func audioRecorderBeginInterruption(AVAudioRecorder)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderbegininterruption(_:))
- [func audioRecorderEndInterruption(AVAudioRecorder)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderendinterruption(_:))
- [func audioRecorderEndInterruption(AVAudioRecorder, withOptions: Int)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderendinterruption(_:withoptions:))
- [func audioRecorderEndInterruption(AVAudioRecorder, withFlags: Int)](/documentation/avfaudio/avaudiorecorderdelegate/audiorecorderendinterruption(_:withflags:))

### Inspecting the audio data

- [var url: URL](/documentation/avfaudio/avaudiorecorder/url)
- [var format: AVAudioFormat](/documentation/avfaudio/avaudiorecorder/format)
- [var settings: [String : Any]](/documentation/avfaudio/avaudiorecorder/settings)
- [AVMIDIPlayer](/documentation/avfaudio/avmidiplayer)

### Creating a MIDI player

- [init(contentsOf: URL, soundBankURL: URL?) throws](/documentation/avfaudio/avmidiplayer/init(contentsof:soundbankurl:))
- [init(data: Data, soundBankURL: URL?) throws](/documentation/avfaudio/avmidiplayer/init(data:soundbankurl:))

### Controlling playback

- [func prepareToPlay()](/documentation/avfaudio/avmidiplayer/preparetoplay())
- [func play((() -> Void)?)](/documentation/avfaudio/avmidiplayer/play(_:))

#### Closures

- [AVMIDIPlayerCompletionHandler](/documentation/avfaudio/avmidiplayercompletionhandler)
- [AVMIDIPlayerCompletionHandler](/documentation/avfaudio/avmidiplayercompletionhandler)
- [func stop()](/documentation/avfaudio/avmidiplayer/stop())
- [var isPlaying: Bool](/documentation/avfaudio/avmidiplayer/isplaying)

### Configuring playback settings

- [var rate: Float](/documentation/avfaudio/avmidiplayer/rate)

### Accessing player timing

- [var currentPosition: TimeInterval](/documentation/avfaudio/avmidiplayer/currentposition)
- [var duration: TimeInterval](/documentation/avfaudio/avmidiplayer/duration)

## Advanced audio processing

- [Audio Engine](/documentation/avfaudio/audio-engine)

### Essentials

- [AVAudioEngine](/documentation/avfaudio/avaudioengine)

#### Creating an Audio Engine

- [init()](/documentation/avfaudio/avaudioengine/init())

#### Attaching and Detaching Audio Nodes

- [func attach(AVAudioNode)](/documentation/avfaudio/avaudioengine/attach(_:))
- [func detach(AVAudioNode)](/documentation/avfaudio/avaudioengine/detach(_:))
- [var attachedNodes: Set<AVAudioNode>](/documentation/avfaudio/avaudioengine/attachednodes)

#### Getting the Input, Output, and Main Mixer Nodes

- [var inputNode: AVAudioInputNode](/documentation/avfaudio/avaudioengine/inputnode)
- [var outputNode: AVAudioOutputNode](/documentation/avfaudio/avaudioengine/outputnode)
- [var mainMixerNode: AVAudioMixerNode](/documentation/avfaudio/avaudioengine/mainmixernode)

#### Connecting and Disconnecting Audio Nodes

- [func connect(AVAudioNode, to: AVAudioNode, format: AVAudioFormat?)](/documentation/avfaudio/avaudioengine/connect(_:to:format:))
- [func connect(AVAudioNode, to: AVAudioNode, fromBus: AVAudioNodeBus, toBus: AVAudioNodeBus, format: AVAudioFormat?)](/documentation/avfaudio/avaudioengine/connect(_:to:frombus:tobus:format:))
- [func disconnectNodeInput(AVAudioNode)](/documentation/avfaudio/avaudioengine/disconnectnodeinput(_:))
- [func disconnectNodeInput(AVAudioNode, bus: AVAudioNodeBus)](/documentation/avfaudio/avaudioengine/disconnectnodeinput(_:bus:))
- [func disconnectNodeOutput(AVAudioNode)](/documentation/avfaudio/avaudioengine/disconnectnodeoutput(_:))
- [func disconnectNodeOutput(AVAudioNode, bus: AVAudioNodeBus)](/documentation/avfaudio/avaudioengine/disconnectnodeoutput(_:bus:))

#### Managing MIDI Nodes

- [func connectMIDI(AVAudioNode, to: AVAudioNode, format: AVAudioFormat?, eventListBlock: AUMIDIEventListBlock?)](/documentation/avfaudio/avaudioengine/connectmidi(_:to:format:eventlistblock:)-73cd1)
- [func connectMIDI(AVAudioNode, to: [AVAudioNode], format: AVAudioFormat?, eventListBlock: AUMIDIEventListBlock?)](/documentation/avfaudio/avaudioengine/connectmidi(_:to:format:eventlistblock:)-7qtd5)
- [func disconnectMIDI(AVAudioNode, from: AVAudioNode)](/documentation/avfaudio/avaudioengine/disconnectmidi(_:from:)-1kssy)
- [func disconnectMIDI(AVAudioNode, from: [AVAudioNode])](/documentation/avfaudio/avaudioengine/disconnectmidi(_:from:)-7oaab)
- [func disconnectMIDIInput(AVAudioNode)](/documentation/avfaudio/avaudioengine/disconnectmidiinput(_:))
- [func disconnectMIDIOutput(AVAudioNode)](/documentation/avfaudio/avaudioengine/disconnectmidioutput(_:))
- [func connectMIDI(AVAudioNode, to: AVAudioNode, format: AVAudioFormat?, block: AUMIDIOutputEventBlock?)](/documentation/avfaudio/avaudioengine/connectmidi(_:to:format:block:)-3bc13)
- [func connectMIDI(AVAudioNode, to: [AVAudioNode], format: AVAudioFormat?, block: AUMIDIOutputEventBlock?)](/documentation/avfaudio/avaudioengine/connectmidi(_:to:format:block:)-666bc)

#### Playing Audio

- [func prepare()](/documentation/avfaudio/avaudioengine/prepare())
- [func start() throws](/documentation/avfaudio/avaudioengine/start())
- [var isRunning: Bool](/documentation/avfaudio/avaudioengine/isrunning)
- [func pause()](/documentation/avfaudio/avaudioengine/pause())
- [func stop()](/documentation/avfaudio/avaudioengine/stop())
- [func reset()](/documentation/avfaudio/avaudioengine/reset())
- [var musicSequence: MusicSequence?](/documentation/avfaudio/avaudioengine/musicsequence)

#### Manually Rendering an Audio Engine

- [func enableManualRenderingMode(AVAudioEngineManualRenderingMode, format: AVAudioFormat, maximumFrameCount: AVAudioFrameCount) throws](/documentation/avfaudio/avaudioengine/enablemanualrenderingmode(_:format:maximumframecount:))
- [func disableManualRenderingMode()](/documentation/avfaudio/avaudioengine/disablemanualrenderingmode())
- [func renderOffline(AVAudioFrameCount, to: AVAudioPCMBuffer) throws -> AVAudioEngineManualRenderingStatus](/documentation/avfaudio/avaudioengine/renderoffline(_:to:))

#### Getting Manual Rendering Properties

- [AVAudioEngineManualRenderingBlock](/documentation/avfaudio/avaudioenginemanualrenderingblock)
- [var manualRenderingBlock: AVAudioEngineManualRenderingBlock](/documentation/avfaudio/avaudioengine/manualrenderingblock)
- [var manualRenderingFormat: AVAudioFormat](/documentation/avfaudio/avaudioengine/manualrenderingformat)
- [var manualRenderingMaximumFrameCount: AVAudioFrameCount](/documentation/avfaudio/avaudioengine/manualrenderingmaximumframecount)
- [var manualRenderingMode: AVAudioEngineManualRenderingMode](/documentation/avfaudio/avaudioengine/manualrenderingmode)
- [var manualRenderingSampleTime: AVAudioFramePosition](/documentation/avfaudio/avaudioengine/manualrenderingsampletime)
- [var isAutoShutdownEnabled: Bool](/documentation/avfaudio/avaudioengine/isautoshutdownenabled)
- [var isInManualRenderingMode: Bool](/documentation/avfaudio/avaudioengine/isinmanualrenderingmode)

#### Using Connection Points

- [AVAudioConnectionPoint](/documentation/avfaudio/avaudioconnectionpoint)

##### Creating a Connection Point

- [init(node: AVAudioNode, bus: AVAudioNodeBus)](/documentation/avfaudio/avaudioconnectionpoint/init(node:bus:))

##### Getting Connection Point Properties

- [func inputConnectionPoint(for: AVAudioNode, inputBus: AVAudioNodeBus) -> AVAudioConnectionPoint?](/documentation/avfaudio/avaudioengine/inputconnectionpoint(for:inputbus:))
- [func outputConnectionPoints(for: AVAudioNode, outputBus: AVAudioNodeBus) -> [AVAudioConnectionPoint]](/documentation/avfaudio/avaudioengine/outputconnectionpoints(for:outputbus:))
- [var bus: AVAudioNodeBus](/documentation/avfaudio/avaudioconnectionpoint/bus)
- [var node: AVAudioNode?](/documentation/avfaudio/avaudioconnectionpoint/node)
- [func connect(AVAudioNode, to: [AVAudioConnectionPoint], fromBus: AVAudioNodeBus, format: AVAudioFormat?)](/documentation/avfaudio/avaudioengine/connect(_:to:frombus:format:))
- [func inputConnectionPoint(for: AVAudioNode, inputBus: AVAudioNodeBus) -> AVAudioConnectionPoint?](/documentation/avfaudio/avaudioengine/inputconnectionpoint(for:inputbus:))
- [func outputConnectionPoints(for: AVAudioNode, outputBus: AVAudioNodeBus) -> [AVAudioConnectionPoint]](/documentation/avfaudio/avaudioengine/outputconnectionpoints(for:outputbus:))

#### Constants

- [AVAudioEngineManualRenderingError](/documentation/avfaudio/avaudioenginemanualrenderingerror)

##### Manual Rendering Errors

- [case initialized](/documentation/avfaudio/avaudioenginemanualrenderingerror/initialized)
- [case invalidMode](/documentation/avfaudio/avaudioenginemanualrenderingerror/invalidmode)
- [case notRunning](/documentation/avfaudio/avaudioenginemanualrenderingerror/notrunning)

##### Initializers

- [init?(rawValue: OSStatus)](/documentation/avfaudio/avaudioenginemanualrenderingerror/init(rawvalue:))
- [AVAudioEngineManualRenderingMode](/documentation/avfaudio/avaudioenginemanualrenderingmode)

##### Constants

- [case offline](/documentation/avfaudio/avaudioenginemanualrenderingmode/offline)
- [case realtime](/documentation/avfaudio/avaudioenginemanualrenderingmode/realtime)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioenginemanualrenderingmode/init(rawvalue:))
- [AVAudioEngineManualRenderingStatus](/documentation/avfaudio/avaudioenginemanualrenderingstatus)

##### Constants

- [case error](/documentation/avfaudio/avaudioenginemanualrenderingstatus/error)
- [case success](/documentation/avfaudio/avaudioenginemanualrenderingstatus/success)
- [case insufficientDataFromInputNode](/documentation/avfaudio/avaudioenginemanualrenderingstatus/insufficientdatafrominputnode)
- [case cannotDoInCurrentContext](/documentation/avfaudio/avaudioenginemanualrenderingstatus/cannotdoincurrentcontext)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioenginemanualrenderingstatus/init(rawvalue:))

### Nodes

- [AVAudioNode](/documentation/avfaudio/avaudionode)

#### Configuring an Input Format Bus

- [AVAudioNodeBus](/documentation/avfaudio/avaudionodebus)
- [func inputFormat(forBus: AVAudioNodeBus) -> AVAudioFormat](/documentation/avfaudio/avaudionode/inputformat(forbus:))
- [func name(forInputBus: AVAudioNodeBus) -> String?](/documentation/avfaudio/avaudionode/name(forinputbus:))
- [var numberOfInputs: Int](/documentation/avfaudio/avaudionode/numberofinputs)

#### Creating an Output Format Bus

- [func outputFormat(forBus: AVAudioNodeBus) -> AVAudioFormat](/documentation/avfaudio/avaudionode/outputformat(forbus:))
- [func name(forOutputBus: AVAudioNodeBus) -> String?](/documentation/avfaudio/avaudionode/name(foroutputbus:))
- [var numberOfOutputs: Int](/documentation/avfaudio/avaudionode/numberofoutputs)

#### Installing and Removing an Audio Tap

- [func installTap(onBus: AVAudioNodeBus, bufferSize: AVAudioFrameCount, format: AVAudioFormat?, block: AVAudioNodeTapBlock)](/documentation/avfaudio/avaudionode/installtap(onbus:buffersize:format:block:))
- [func removeTap(onBus: AVAudioNodeBus)](/documentation/avfaudio/avaudionode/removetap(onbus:))
- [AVAudioNodeTapBlock](/documentation/avfaudio/avaudionodetapblock)

#### Getting the Audio Engine for the Node

- [var engine: AVAudioEngine?](/documentation/avfaudio/avaudionode/engine)

#### Getting the Latest Node Render Time

- [var lastRenderTime: AVAudioTime?](/documentation/avfaudio/avaudionode/lastrendertime)

#### Getting Audio Node Properties

- [var auAudioUnit: AUAudioUnit](/documentation/avfaudio/avaudionode/auaudiounit)
- [var latency: TimeInterval](/documentation/avfaudio/avaudionode/latency)
- [var outputPresentationLatency: TimeInterval](/documentation/avfaudio/avaudionode/outputpresentationlatency)

#### Resetting the Audio Node

- [func reset()](/documentation/avfaudio/avaudionode/reset())

#### Constants

- [AVAudioNodeCompletionHandler](/documentation/avfaudio/avaudionodecompletionhandler)
- [AVAudioInputNode](/documentation/avfaudio/avaudioinputnode)

#### Manually Giving Data to an Audio Engine

- [func setManualRenderingInputPCMFormat(AVAudioFormat, inputBlock: AVAudioIONodeInputBlock) -> Bool](/documentation/avfaudio/avaudioinputnode/setmanualrenderinginputpcmformat(_:inputblock:))
- [AVAudioIONodeInputBlock](/documentation/avfaudio/avaudioionodeinputblock)

#### Getting and Setting Voice Processing Properties

- [var isVoiceProcessingInputMuted: Bool](/documentation/avfaudio/avaudioinputnode/isvoiceprocessinginputmuted)
- [var isVoiceProcessingBypassed: Bool](/documentation/avfaudio/avaudioinputnode/isvoiceprocessingbypassed)
- [var isVoiceProcessingAGCEnabled: Bool](/documentation/avfaudio/avaudioinputnode/isvoiceprocessingagcenabled)
- [var voiceProcessingOtherAudioDuckingConfiguration: AVAudioVoiceProcessingOtherAudioDuckingConfiguration](/documentation/avfaudio/avaudioinputnode/voiceprocessingotheraudioduckingconfiguration)
- [AVAudioVoiceProcessingOtherAudioDuckingConfiguration](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration)

##### Configuring ducking

- [var enableAdvancedDucking: ObjCBool](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/enableadvancedducking)
- [var duckingLevel: AVAudioVoiceProcessingOtherAudioDuckingConfiguration.Level](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/duckinglevel)
- [AVAudioVoiceProcessingOtherAudioDuckingConfiguration.Level](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level)

###### Ducking levels

- [case `default`](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level/default)
- [case max](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level/max)
- [case mid](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level/mid)
- [case min](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level/min)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/level/init(rawvalue:))

##### Initializers

- [init()](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/init())
- [init(enableAdvancedDucking: ObjCBool, duckingLevel: AVAudioVoiceProcessingOtherAudioDuckingConfiguration.Level)](/documentation/avfaudio/avaudiovoiceprocessingotheraudioduckingconfiguration/init(enableadvancedducking:duckinglevel:))

#### Handling Muted Speech Events

- [func setMutedSpeechActivityEventListener(((AVAudioVoiceProcessingSpeechActivityEvent) -> Void)?) -> Bool](/documentation/avfaudio/avaudioinputnode/setmutedspeechactivityeventlistener(_:))
- [AVAudioVoiceProcessingSpeechActivityEvent](/documentation/avfaudio/avaudiovoiceprocessingspeechactivityevent)

##### Events

- [case started](/documentation/avfaudio/avaudiovoiceprocessingspeechactivityevent/started)
- [case ended](/documentation/avfaudio/avaudiovoiceprocessingspeechactivityevent/ended)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiovoiceprocessingspeechactivityevent/init(rawvalue:))
- [AVAudioOutputNode](/documentation/avfaudio/avaudiooutputnode)

#### Configuring the Spatial Audio experience

- [var intendedSpatialExperience: any SpatialAudioExperience](/documentation/avfaudio/avaudiooutputnode/intendedspatialexperience-3ts59)
- [AVAudioIONode](/documentation/avfaudio/avaudioionode)

#### Getting the Audio Unit

- [var audioUnit: AudioUnit?](/documentation/avfaudio/avaudioionode/audiounit)

#### Getting the I/O Latency

- [var presentationLatency: TimeInterval](/documentation/avfaudio/avaudioionode/presentationlatency)

#### Getting and Setting the Voice Processing State

- [func setVoiceProcessingEnabled(Bool) throws](/documentation/avfaudio/avaudioionode/setvoiceprocessingenabled(_:))
- [var isVoiceProcessingEnabled: Bool](/documentation/avfaudio/avaudioionode/isvoiceprocessingenabled)

### Playback

- [Playing custom audio with your own player](/documentation/avfaudio/playing-custom-audio-with-your-own-player)
- [Using voice processing](/documentation/avfaudio/using-voice-processing)
- [AVAudioPlayerNode](/documentation/avfaudio/avaudioplayernode)

#### Creating a Player Node

- [init()](/documentation/avfaudio/avaudioplayernode/init())

#### Scheduling Playback

- [func scheduleFile(AVAudioFile, at: AVAudioTime?, completionHandler: (() -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulefile(_:at:completionhandler:))
- [func scheduleFile(AVAudioFile, at: AVAudioTime?, completionCallbackType: AVAudioPlayerNodeCompletionCallbackType, completionHandler: ((AVAudioPlayerNodeCompletionCallbackType) -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulefile(_:at:completioncallbacktype:completionhandler:))
- [func scheduleSegment(AVAudioFile, startingFrame: AVAudioFramePosition, frameCount: AVAudioFrameCount, at: AVAudioTime?, completionHandler: (() -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulesegment(_:startingframe:framecount:at:completionhandler:))
- [func scheduleSegment(AVAudioFile, startingFrame: AVAudioFramePosition, frameCount: AVAudioFrameCount, at: AVAudioTime?, completionCallbackType: AVAudioPlayerNodeCompletionCallbackType, completionHandler: ((AVAudioPlayerNodeCompletionCallbackType) -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulesegment(_:startingframe:framecount:at:completioncallbacktype:completionhandler:))
- [func scheduleBuffer(AVAudioPCMBuffer, at: AVAudioTime?, options: AVAudioPlayerNodeBufferOptions, completionHandler: (() -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulebuffer(_:at:options:completionhandler:))
- [func scheduleBuffer(AVAudioPCMBuffer, completionHandler: (() -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulebuffer(_:completionhandler:))
- [func scheduleBuffer(AVAudioPCMBuffer, at: AVAudioTime?, options: AVAudioPlayerNodeBufferOptions, completionCallbackType: AVAudioPlayerNodeCompletionCallbackType, completionHandler: ((AVAudioPlayerNodeCompletionCallbackType) -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulebuffer(_:at:options:completioncallbacktype:completionhandler:))
- [func scheduleBuffer(AVAudioPCMBuffer, completionCallbackType: AVAudioPlayerNodeCompletionCallbackType, completionHandler: ((AVAudioPlayerNodeCompletionCallbackType) -> Void)?)](/documentation/avfaudio/avaudioplayernode/schedulebuffer(_:completioncallbacktype:completionhandler:))
- [AVAudioPlayerNodeBufferOptions](/documentation/avfaudio/avaudioplayernodebufferoptions)

##### Creating a Buffer Option

- [init(rawValue: UInt)](/documentation/avfaudio/avaudioplayernodebufferoptions/init(rawvalue:))

##### Getting Standard Buffer Options

- [static var loops: AVAudioPlayerNodeBufferOptions](/documentation/avfaudio/avaudioplayernodebufferoptions/loops)
- [static var interrupts: AVAudioPlayerNodeBufferOptions](/documentation/avfaudio/avaudioplayernodebufferoptions/interrupts)
- [static var interruptsAtLoop: AVAudioPlayerNodeBufferOptions](/documentation/avfaudio/avaudioplayernodebufferoptions/interruptsatloop)
- [AVAudioPlayerNodeCompletionCallbackType](/documentation/avfaudio/avaudioplayernodecompletioncallbacktype)

##### Completion Handler Cases

- [case dataConsumed](/documentation/avfaudio/avaudioplayernodecompletioncallbacktype/dataconsumed)
- [case dataRendered](/documentation/avfaudio/avaudioplayernodecompletioncallbacktype/datarendered)
- [case dataPlayedBack](/documentation/avfaudio/avaudioplayernodecompletioncallbacktype/dataplayedback)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioplayernodecompletioncallbacktype/init(rawvalue:))
- [AVAudioPlayerNodeCompletionHandler](/documentation/avfaudio/avaudioplayernodecompletionhandler)

#### Converting Node and Player Times

- [func nodeTime(forPlayerTime: AVAudioTime) -> AVAudioTime?](/documentation/avfaudio/avaudioplayernode/nodetime(forplayertime:))
- [func playerTime(forNodeTime: AVAudioTime) -> AVAudioTime?](/documentation/avfaudio/avaudioplayernode/playertime(fornodetime:))

#### Controlling Playback

- [func prepare(withFrameCount: AVAudioFrameCount)](/documentation/avfaudio/avaudioplayernode/prepare(withframecount:))
- [func play()](/documentation/avfaudio/avaudioplayernode/play())
- [func play(at: AVAudioTime?)](/documentation/avfaudio/avaudioplayernode/play(at:))
- [var isPlaying: Bool](/documentation/avfaudio/avaudioplayernode/isplaying)
- [func pause()](/documentation/avfaudio/avaudioplayernode/pause())
- [func stop()](/documentation/avfaudio/avaudioplayernode/stop())

### MIDI

- [AVAudioSequencer](/documentation/avfaudio/avaudiosequencer)

#### Creating an Audio Sequencer

- [init()](/documentation/avfaudio/avaudiosequencer/init())
- [init(audioEngine: AVAudioEngine)](/documentation/avfaudio/avaudiosequencer/init(audioengine:))

#### Writing to a MIDI File

- [func write(to: URL, smpteResolution: Int, replaceExisting: Bool) throws](/documentation/avfaudio/avaudiosequencer/write(to:smpteresolution:replaceexisting:))

#### Handling Music Tracks

- [AVMusicTrack](/documentation/avfaudio/avmusictrack)

##### Configuring Music Track Properties

- [var isMuted: Bool](/documentation/avfaudio/avmusictrack/ismuted)
- [var isSoloed: Bool](/documentation/avfaudio/avmusictrack/issoloed)
- [var offsetTime: AVMusicTimeStamp](/documentation/avfaudio/avmusictrack/offsettime)
- [var timeResolution: Int](/documentation/avfaudio/avmusictrack/timeresolution)
- [var usesAutomatedParameters: Bool](/documentation/avfaudio/avmusictrack/usesautomatedparameters)

##### Configuring the Track Duration

- [var lengthInBeats: AVMusicTimeStamp](/documentation/avfaudio/avmusictrack/lengthinbeats)
- [var lengthInSeconds: TimeInterval](/documentation/avfaudio/avmusictrack/lengthinseconds)

##### Configuring the Track Destinations

- [var destinationAudioUnit: AVAudioUnit?](/documentation/avfaudio/avmusictrack/destinationaudiounit)
- [var destinationMIDIEndpoint: MIDIEndpointRef](/documentation/avfaudio/avmusictrack/destinationmidiendpoint)

##### Configuring the Looping State

- [var isLoopingEnabled: Bool](/documentation/avfaudio/avmusictrack/isloopingenabled)
- [var loopRange: AVBeatRange](/documentation/avfaudio/avmusictrack/looprange)
- [var numberOfLoops: Int](/documentation/avfaudio/avmusictrack/numberofloops)

##### Adding and Clearing Events

- [func addEvent(AVMusicEvent, at: AVMusicTimeStamp)](/documentation/avfaudio/avmusictrack/addevent(_:at:))
- [func moveEvents(in: AVBeatRange, by: AVMusicTimeStamp)](/documentation/avfaudio/avmusictrack/moveevents(in:by:))
- [func clearEvents(in: AVBeatRange)](/documentation/avfaudio/avmusictrack/clearevents(in:))

##### Cutting and Copying Events

- [func cutEvents(in: AVBeatRange)](/documentation/avfaudio/avmusictrack/cutevents(in:))
- [func copyEvents(in: AVBeatRange, from: AVMusicTrack, insertAt: AVMusicTimeStamp)](/documentation/avfaudio/avmusictrack/copyevents(in:from:insertat:))
- [func copyAndMergeEvents(in: AVBeatRange, from: AVMusicTrack, mergeAt: AVMusicTimeStamp)](/documentation/avfaudio/avmusictrack/copyandmergeevents(in:from:mergeat:))

##### Iterating Over Events

- [func enumerateEvents(in: AVBeatRange, using: (AVMusicEvent, UnsafeMutablePointer<AVMusicTimeStamp>, UnsafeMutablePointer<ObjCBool>) -> Void)](/documentation/avfaudio/avmusictrack/enumerateevents(in:using:))
- [AVMusicEventEnumerationBlock](/documentation/avfaudio/avmusiceventenumerationblock)

##### Getting the End of Track Timestamp

- [var AVMusicTimeStampEndOfTrack: Double](/documentation/avfaudio/avmusictimestampendoftrack)
- [func createAndAppendTrack() -> AVMusicTrack](/documentation/avfaudio/avaudiosequencer/createandappendtrack())
- [func reverseEvents()](/documentation/avfaudio/avaudiosequencer/reverseevents())
- [func removeTrack(AVMusicTrack) -> Bool](/documentation/avfaudio/avaudiosequencer/removetrack(_:))
- [AVMusicTrackLoopCount](/documentation/avfaudio/avmusictrackloopcount)

##### Elements

- [case forever](/documentation/avfaudio/avmusictrackloopcount/forever)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avmusictrackloopcount/init(rawvalue:))

#### Handling Music Events

- [AVMusicEvent](/documentation/avfaudio/avmusicevent)
- [AVMusicUserEvent](/documentation/avfaudio/avmusicuserevent)

##### Creating a User Event

- [init(data: Data)](/documentation/avfaudio/avmusicuserevent/init(data:))

##### Inspecting a User Event

- [var sizeInBytes: UInt32](/documentation/avfaudio/avmusicuserevent/sizeinbytes)
- [AVParameterEvent](/documentation/avfaudio/avparameterevent)

##### Creating a Parameter Event

- [init(parameterID: UInt32, scope: UInt32, element: UInt32, value: Float)](/documentation/avfaudio/avparameterevent/init(parameterid:scope:element:value:))

##### Configuring a Parameter Event

- [var parameterID: UInt32](/documentation/avfaudio/avparameterevent/parameterid)
- [var scope: UInt32](/documentation/avfaudio/avparameterevent/scope)
- [var element: UInt32](/documentation/avfaudio/avparameterevent/element)
- [var value: Float](/documentation/avfaudio/avparameterevent/value)
- [AVAUPresetEvent](/documentation/avfaudio/avaupresetevent)

##### Creating a Preset Event

- [init(scope: UInt32, element: UInt32, dictionary: [AnyHashable : Any])](/documentation/avfaudio/avaupresetevent/init(scope:element:dictionary:))

##### Configuring a Preset Event

- [var scope: UInt32](/documentation/avfaudio/avaupresetevent/scope)
- [var element: UInt32](/documentation/avfaudio/avaupresetevent/element)
- [var presetDictionary: [AnyHashable : Any]](/documentation/avfaudio/avaupresetevent/presetdictionary)
- [AVExtendedTempoEvent](/documentation/avfaudio/avextendedtempoevent)

##### Creating a Tempo Event

- [init(tempo: Double)](/documentation/avfaudio/avextendedtempoevent/init(tempo:))

##### Configuring a Tempo Event

- [var tempo: Double](/documentation/avfaudio/avextendedtempoevent/tempo)
- [AVExtendedNoteOnEvent](/documentation/avfaudio/avextendednoteonevent)

##### Creating a Note On Event

- [init(midiNote: Float, velocity: Float, groupID: UInt32, duration: AVMusicTimeStamp)](/documentation/avfaudio/avextendednoteonevent/init(midinote:velocity:groupid:duration:))
- [init(midiNote: Float, velocity: Float, instrumentID: UInt32, groupID: UInt32, duration: AVMusicTimeStamp)](/documentation/avfaudio/avextendednoteonevent/init(midinote:velocity:instrumentid:groupid:duration:))

##### Configuring a Note On Event

- [var midiNote: Float](/documentation/avfaudio/avextendednoteonevent/midinote)
- [var velocity: Float](/documentation/avfaudio/avextendednoteonevent/velocity)
- [var instrumentID: UInt32](/documentation/avfaudio/avextendednoteonevent/instrumentid)
- [var groupID: UInt32](/documentation/avfaudio/avextendednoteonevent/groupid)
- [var duration: AVMusicTimeStamp](/documentation/avfaudio/avextendednoteonevent/duration)

##### Getting the Default Instrument

- [class let defaultInstrument: UInt32](/documentation/avfaudio/avextendednoteonevent/defaultinstrument)

#### Handling MIDI Events

- [AVMIDINoteEvent](/documentation/avfaudio/avmidinoteevent)

##### Creating a MIDI Note Event

- [init(channel: UInt32, key: UInt32, velocity: UInt32, duration: AVMusicTimeStamp)](/documentation/avfaudio/avmidinoteevent/init(channel:key:velocity:duration:))

##### Configuring a MIDI Note Event

- [var channel: UInt32](/documentation/avfaudio/avmidinoteevent/channel)
- [var key: UInt32](/documentation/avfaudio/avmidinoteevent/key)
- [var velocity: UInt32](/documentation/avfaudio/avmidinoteevent/velocity)
- [var duration: AVMusicTimeStamp](/documentation/avfaudio/avmidinoteevent/duration)
- [AVMIDIMetaEvent](/documentation/avfaudio/avmidimetaevent)

##### Creating a Meta Event

- [init(type: AVMIDIMetaEvent.EventType, data: Data)](/documentation/avfaudio/avmidimetaevent/init(type:data:))

##### Getting the Meta Event Type

- [var type: AVMIDIMetaEvent.EventType](/documentation/avfaudio/avmidimetaevent/type)
- [AVMIDIMetaEvent.EventType](/documentation/avfaudio/avmidimetaevent/eventtype)

###### Event Types

- [case copyright](/documentation/avfaudio/avmidimetaevent/eventtype/copyright)
- [case cuePoint](/documentation/avfaudio/avmidimetaevent/eventtype/cuepoint)
- [case endOfTrack](/documentation/avfaudio/avmidimetaevent/eventtype/endoftrack)
- [case instrument](/documentation/avfaudio/avmidimetaevent/eventtype/instrument)
- [case keySignature](/documentation/avfaudio/avmidimetaevent/eventtype/keysignature)
- [case lyric](/documentation/avfaudio/avmidimetaevent/eventtype/lyric)
- [case marker](/documentation/avfaudio/avmidimetaevent/eventtype/marker)
- [case midiChannel](/documentation/avfaudio/avmidimetaevent/eventtype/midichannel)
- [case midiPort](/documentation/avfaudio/avmidimetaevent/eventtype/midiport)
- [case proprietaryEvent](/documentation/avfaudio/avmidimetaevent/eventtype/proprietaryevent)
- [case sequenceNumber](/documentation/avfaudio/avmidimetaevent/eventtype/sequencenumber)
- [case smpteOffset](/documentation/avfaudio/avmidimetaevent/eventtype/smpteoffset)
- [case tempo](/documentation/avfaudio/avmidimetaevent/eventtype/tempo)
- [case text](/documentation/avfaudio/avmidimetaevent/eventtype/text)
- [case timeSignature](/documentation/avfaudio/avmidimetaevent/eventtype/timesignature)
- [case trackName](/documentation/avfaudio/avmidimetaevent/eventtype/trackname)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avmidimetaevent/eventtype/init(rawvalue:))
- [AVMIDISysexEvent](/documentation/avfaudio/avmidisysexevent)

##### Creates a System Event

- [init(data: Data)](/documentation/avfaudio/avmidisysexevent/init(data:))

##### Getting the Size of the Event

- [var sizeInBytes: UInt32](/documentation/avfaudio/avmidisysexevent/sizeinbytes)

#### Handling MIDI Channel Events

- [AVMIDIChannelEvent](/documentation/avfaudio/avmidichannelevent)

##### Configuring a Channel Event

- [var channel: UInt32](/documentation/avfaudio/avmidichannelevent/channel)
- [AVMIDIChannelPressureEvent](/documentation/avfaudio/avmidichannelpressureevent)

##### Creating a Pressure Event

- [init(channel: UInt32, pressure: UInt32)](/documentation/avfaudio/avmidichannelpressureevent/init(channel:pressure:))

##### Configuring a Pressure Event

- [var pressure: UInt32](/documentation/avfaudio/avmidichannelpressureevent/pressure)
- [AVMIDIProgramChangeEvent](/documentation/avfaudio/avmidiprogramchangeevent)

##### Creating a Program Change Event

- [init(channel: UInt32, programNumber: UInt32)](/documentation/avfaudio/avmidiprogramchangeevent/init(channel:programnumber:))

##### Configuring a Program Change Event

- [var programNumber: UInt32](/documentation/avfaudio/avmidiprogramchangeevent/programnumber)
- [AVMIDIPolyPressureEvent](/documentation/avfaudio/avmidipolypressureevent)

##### Creating a Poly Pressure Event

- [init(channel: UInt32, key: UInt32, pressure: UInt32)](/documentation/avfaudio/avmidipolypressureevent/init(channel:key:pressure:))

##### Configuring a Poly Pressure Event

- [var key: UInt32](/documentation/avfaudio/avmidipolypressureevent/key)
- [var pressure: UInt32](/documentation/avfaudio/avmidipolypressureevent/pressure)
- [AVMIDIPitchBendEvent](/documentation/avfaudio/avmidipitchbendevent)

##### Creating a Pitch Bend Event

- [init(channel: UInt32, value: UInt32)](/documentation/avfaudio/avmidipitchbendevent/init(channel:value:))

##### Configuring a Pitch Bend Event

- [var value: UInt32](/documentation/avfaudio/avmidipitchbendevent/value)
- [AVMIDIControlChangeEvent](/documentation/avfaudio/avmidicontrolchangeevent)

##### Creating a Control Change Event

- [init(channel: UInt32, messageType: AVMIDIControlChangeEvent.MessageType, value: UInt32)](/documentation/avfaudio/avmidicontrolchangeevent/init(channel:messagetype:value:))

##### Inspecting a Control Change Event

- [var value: UInt32](/documentation/avfaudio/avmidicontrolchangeevent/value)
- [var messageType: AVMIDIControlChangeEvent.MessageType](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.property)
- [AVMIDIControlChangeEvent.MessageType](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum)

###### Event Types

- [case bankSelect](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/bankselect)
- [case modWheel](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/modwheel)
- [case breath](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/breath)
- [case foot](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/foot)
- [case portamentoTime](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/portamentotime)
- [case dataEntry](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/dataentry)
- [case volume](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/volume)
- [case balance](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/balance)
- [case pan](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/pan)
- [case expression](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/expression)
- [case sustain](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/sustain)
- [case portamento](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/portamento)
- [case sostenuto](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/sostenuto)
- [case soft](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/soft)
- [case legatoPedal](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/legatopedal)
- [case hold2Pedal](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/hold2pedal)
- [case filterResonance](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/filterresonance)
- [case releaseTime](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/releasetime)
- [case attackTime](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/attacktime)
- [case brightness](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/brightness)
- [case decayTime](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/decaytime)
- [case vibratoRate](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/vibratorate)
- [case vibratoDepth](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/vibratodepth)
- [case vibratoDelay](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/vibratodelay)
- [case reverbLevel](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/reverblevel)
- [case chorusLevel](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/choruslevel)
- [case RPN_LSB](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/rpn_lsb)
- [case RPN_MSB](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/rpn_msb)
- [case allSoundOff](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/allsoundoff)
- [case resetAllControllers](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/resetallcontrollers)
- [case allNotesOff](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/allnotesoff)
- [case omniModeOff](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/omnimodeoff)
- [case omniModeOn](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/omnimodeon)
- [case monoModeOn](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/monomodeon)
- [case monoModeOff](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/monomodeoff)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avmidicontrolchangeevent/messagetype-swift.enum/init(rawvalue:))

#### Managing Sequence Load Options

- [func load(from: Data, options: AVMusicSequenceLoadOptions) throws](/documentation/avfaudio/avaudiosequencer/load(from:options:)-8o58w)
- [func load(from: URL, options: AVMusicSequenceLoadOptions) throws](/documentation/avfaudio/avaudiosequencer/load(from:options:)-9kb6m)
- [AVMusicSequenceLoadOptions](/documentation/avfaudio/avmusicsequenceloadoptions)

##### Getting Standard Load Options

- [static var smf_ChannelsToTracks: AVMusicSequenceLoadOptions](/documentation/avfaudio/avmusicsequenceloadoptions/smf_channelstotracks)

##### Creating a Load Option

- [init(rawValue: UInt)](/documentation/avfaudio/avmusicsequenceloadoptions/init(rawvalue:))

#### Operating an Audio Sequencer

- [func prepareToPlay()](/documentation/avfaudio/avaudiosequencer/preparetoplay())
- [func start() throws](/documentation/avfaudio/avaudiosequencer/start())
- [func stop()](/documentation/avfaudio/avaudiosequencer/stop())

#### Managing Time Stamps

- [AVMusicTimeStamp](/documentation/avfaudio/avmusictimestamp)
- [func hostTime(forBeats: AVMusicTimeStamp, error: NSErrorPointer) -> UInt64](/documentation/avfaudio/avaudiosequencer/hosttime(forbeats:error:))
- [func seconds(forBeats: AVMusicTimeStamp) -> TimeInterval](/documentation/avfaudio/avaudiosequencer/seconds(forbeats:))

#### Handling Beat Range

- [func beats(forHostTime: UInt64, error: NSErrorPointer) -> AVMusicTimeStamp](/documentation/avfaudio/avaudiosequencer/beats(forhosttime:error:))
- [func beats(forSeconds: TimeInterval) -> AVMusicTimeStamp](/documentation/avfaudio/avaudiosequencer/beats(forseconds:))
- [var AVMusicTimeStampEndOfTrack: Double](/documentation/avfaudio/avmusictimestampendoftrack)
- [AVBeatRange](/documentation/avfaudio/avbeatrange-swift.typealias)

#### Setting the User Callback

- [func setUserCallback(AVAudioSequencerUserCallback?)](/documentation/avfaudio/avaudiosequencer/setusercallback(_:))
- [AVAudioSequencerUserCallback](/documentation/avfaudio/avaudiosequencerusercallback)

#### Getting Sequence Properties

- [var isPlaying: Bool](/documentation/avfaudio/avaudiosequencer/isplaying)
- [var rate: Float](/documentation/avfaudio/avaudiosequencer/rate)
- [var tracks: [AVMusicTrack]](/documentation/avfaudio/avaudiosequencer/tracks)
- [var currentPositionInBeats: TimeInterval](/documentation/avfaudio/avaudiosequencer/currentpositioninbeats)
- [var currentPositionInSeconds: TimeInterval](/documentation/avfaudio/avaudiosequencer/currentpositioninseconds)
- [var tempoTrack: AVMusicTrack](/documentation/avfaudio/avaudiosequencer/tempotrack)
- [var userInfo: [String : Any]](/documentation/avfaudio/avaudiosequencer/userinfo)
- [AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey)

##### Getting Album Details

- [static let album: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/album)
- [static let artist: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/artist)
- [static let comments: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/comments)
- [static let composer: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/composer)
- [static let copyright: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/copyright)
- [static let genre: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/genre)
- [static let lyricist: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/lyricist)
- [static let title: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/title)
- [static let trackNumber: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/tracknumber)
- [static let subTitle: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/subtitle)
- [static let year: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/year)

##### Getting the Duration and Time

- [static let approximateDurationInSeconds: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/approximatedurationinseconds)
- [static let timeSignature: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/timesignature)
- [static let tempo: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/tempo)

##### Getting the Recording Date

- [static let recordedDate: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/recordeddate)

##### Getting Encoding Information

- [static let encodingApplication: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/encodingapplication)
- [static let sourceEncoder: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/sourceencoder)
- [static let nominalBitRate: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/nominalbitrate)
- [static let sourceBitDepth: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/sourcebitdepth)
- [static let keySignature: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/keysignature)

##### Getting the Channel Layout

- [static let channelLayout: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/channellayout)

##### Getting the Recording Code

- [static let ISRC: AVAudioSequencer.InfoDictionaryKey](/documentation/avfaudio/avaudiosequencer/infodictionarykey/isrc)

##### Creating a Dictionary Key

- [init(rawValue: String)](/documentation/avfaudio/avaudiosequencer/infodictionarykey/init(rawvalue:))
- [func data(withSMPTEResolution: Int, error: NSErrorPointer) -> Data](/documentation/avfaudio/avaudiosequencer/data(withsmpteresolution:error:))
- [var AVMusicTimeStampEndOfTrack: Double](/documentation/avfaudio/avmusictimestampendoftrack)
- [AVAudioUnitSampler](/documentation/avfaudio/avaudiounitsampler)

#### Configuring the Sampler Audio Unit

- [func loadInstrument(at: URL) throws](/documentation/avfaudio/avaudiounitsampler/loadinstrument(at:))
- [func loadAudioFiles(at: [URL]) throws](/documentation/avfaudio/avaudiounitsampler/loadaudiofiles(at:))
- [func loadSoundBankInstrument(at: URL, program: UInt8, bankMSB: UInt8, bankLSB: UInt8) throws](/documentation/avfaudio/avaudiounitsampler/loadsoundbankinstrument(at:program:bankmsb:banklsb:))

#### Getting and Setting Sampler Values

- [var globalTuning: Float](/documentation/avfaudio/avaudiounitsampler/globaltuning)
- [var overallGain: Float](/documentation/avfaudio/avaudiounitsampler/overallgain)
- [var stereoPan: Float](/documentation/avfaudio/avaudiounitsampler/stereopan)
- [var masterGain: Float](/documentation/avfaudio/avaudiounitsampler/mastergain)

### Mixing

- [AVAudioMixerNode](/documentation/avfaudio/avaudiomixernode)

#### Creating a Mixer Node

- [init()](/documentation/avfaudio/avaudiomixernode/init())

#### Getting and Setting the Mixer Volume

- [var outputVolume: Float](/documentation/avfaudio/avaudiomixernode/outputvolume)

#### Getting an Input Bus

- [var nextAvailableInputBus: AVAudioNodeBus](/documentation/avfaudio/avaudiomixernode/nextavailableinputbus)
- [AVAudioMixing](/documentation/avfaudio/avaudiomixing)

#### Defining Mixing Properties

- [AVAudioStereoMixing](/documentation/avfaudio/avaudiostereomixing)

##### Getting and Setting the Stereo Panning

- [var pan: Float](/documentation/avfaudio/avaudiostereomixing/pan)
- [AVAudio3DMixing](/documentation/avfaudio/avaudio3dmixing)

##### Getting the 3D Mixing Parameters

- [var obstruction: Float](/documentation/avfaudio/avaudio3dmixing/obstruction)
- [var occlusion: Float](/documentation/avfaudio/avaudio3dmixing/occlusion)
- [var position: AVAudio3DPoint](/documentation/avfaudio/avaudio3dmixing/position)
- [var rate: Float](/documentation/avfaudio/avaudio3dmixing/rate)
- [var pointSourceInHeadMode: AVAudio3DMixingPointSourceInHeadMode](/documentation/avfaudio/avaudio3dmixing/pointsourceinheadmode)
- [var reverbBlend: Float](/documentation/avfaudio/avaudio3dmixing/reverbblend)
- [var sourceMode: AVAudio3DMixingSourceMode](/documentation/avfaudio/avaudio3dmixing/sourcemode)

##### Getting and Setting the Rendering Algorithm

- [var renderingAlgorithm: AVAudio3DMixingRenderingAlgorithm](/documentation/avfaudio/avaudio3dmixing/renderingalgorithm)
- [AVAudio3DMixingRenderingAlgorithm](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm)

###### Rendering Algorithms

- [case auto](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/auto)
- [case equalPowerPanning](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/equalpowerpanning)
- [case HRTF](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtf)
- [case HRTFHQ](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtfhq)
- [case soundField](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/soundfield)
- [case sphericalHead](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/sphericalhead)
- [case stereoPassThrough](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/stereopassthrough)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/init(rawvalue:))

#### Getting and Setting the Destination

- [AVAudioMixingDestination](/documentation/avfaudio/avaudiomixingdestination)

##### Getting Mixing Destination Properties

- [var connectionPoint: AVAudioConnectionPoint](/documentation/avfaudio/avaudiomixingdestination/connectionpoint)
- [func destination(forMixer: AVAudioNode, bus: AVAudioNodeBus) -> AVAudioMixingDestination?](/documentation/avfaudio/avaudiomixing/destination(formixer:bus:))

#### Getting and Setting the Bus Volume

- [var volume: Float](/documentation/avfaudio/avaudiomixing/volume)

### Effects

- [Creating custom audio effects](/documentation/avfaudio/creating-custom-audio-effects)
- [Audio Units](/documentation/avfaudio/audio-units)

#### Essentials

- [Creating an audio unit extension](/documentation/avfaudio/creating-an-audio-unit-extension)
- [Using voice processing](/documentation/avfaudio/using-voice-processing)
- [AVAudioUnit](/documentation/avfaudio/avaudiounit)

##### Getting the Core Audio audio unit

- [var audioUnit: AudioUnit](/documentation/avfaudio/avaudiounit/audiounit)

##### Loading an audio preset file

- [func loadPreset(at: URL) throws](/documentation/avfaudio/avaudiounit/loadpreset(at:))

##### Creating an audio unit component

- [class func instantiate(with: AudioComponentDescription, options: AudioComponentInstantiationOptions, completionHandler: (AVAudioUnit?, (any Error)?) -> Void)](/documentation/avfaudio/avaudiounit/instantiate(with:options:completionhandler:))

##### Getting audio unit values

- [var audioComponentDescription: AudioComponentDescription](/documentation/avfaudio/avaudiounit/audiocomponentdescription)
- [var manufacturerName: String](/documentation/avfaudio/avaudiounit/manufacturername)
- [var name: String](/documentation/avfaudio/avaudiounit/name)
- [var version: Int](/documentation/avfaudio/avaudiounit/version)
- [var auAudioUnit: AUAudioUnit](/documentation/avfaudio/avaudiounit/auaudiounit)

#### Component management

- [AVAudioUnitComponent](/documentation/avfaudio/avaudiounitcomponent)

##### Getting the audio unit component’s audio unit

- [var audioComponent: AudioComponent](/documentation/avfaudio/avaudiounitcomponent/audiocomponent)

##### Getting audio unit component information

- [var audioComponentDescription: AudioComponentDescription](/documentation/avfaudio/avaudiounitcomponent/audiocomponentdescription)
- [var availableArchitectures: [NSNumber]](/documentation/avfaudio/avaudiounitcomponent/availablearchitectures)
- [var configurationDictionary: [String : Any]](/documentation/avfaudio/avaudiounitcomponent/configurationdictionary)
- [var hasCustomView: Bool](/documentation/avfaudio/avaudiounitcomponent/hascustomview)
- [var hasMIDIInput: Bool](/documentation/avfaudio/avaudiounitcomponent/hasmidiinput)
- [var hasMIDIOutput: Bool](/documentation/avfaudio/avaudiounitcomponent/hasmidioutput)
- [var manufacturerName: String](/documentation/avfaudio/avaudiounitcomponent/manufacturername)
- [var name: String](/documentation/avfaudio/avaudiounitcomponent/name)
- [var passesAUVal: Bool](/documentation/avfaudio/avaudiounitcomponent/passesauval)
- [var isSandboxSafe: Bool](/documentation/avfaudio/avaudiounitcomponent/issandboxsafe)
- [func supportsNumberInputChannels(Int, outputChannels: Int) -> Bool](/documentation/avfaudio/avaudiounitcomponent/supportsnumberinputchannels(_:outputchannels:))
- [var typeName: String](/documentation/avfaudio/avaudiounitcomponent/typename)
- [var version: Int](/documentation/avfaudio/avaudiounitcomponent/version)
- [var versionString: String](/documentation/avfaudio/avaudiounitcomponent/versionstring)
- [var componentURL: URL?](/documentation/avfaudio/avaudiounitcomponent/componenturl)

##### Getting audio unit component tags

- [var iconURL: URL?](/documentation/avfaudio/avaudiounitcomponent/iconurl)
- [var icon: UIImage?](/documentation/avfaudio/avaudiounitcomponent/icon)
- [var localizedTypeName: String](/documentation/avfaudio/avaudiounitcomponent/localizedtypename)
- [var allTagNames: [String]](/documentation/avfaudio/avaudiounitcomponent/alltagnames)
- [var userTagNames: [String]](/documentation/avfaudio/avaudiounitcomponent/usertagnames)

##### Audio unit manufacturer names

- [let AVAudioUnitManufacturerNameApple: String](/documentation/avfaudio/avaudiounitmanufacturernameapple)

##### Audio unit types

- [let AVAudioUnitTypeOutput: String](/documentation/avfaudio/avaudiounittypeoutput)
- [let AVAudioUnitTypeMusicDevice: String](/documentation/avfaudio/avaudiounittypemusicdevice)
- [let AVAudioUnitTypeMusicEffect: String](/documentation/avfaudio/avaudiounittypemusiceffect)
- [let AVAudioUnitTypeFormatConverter: String](/documentation/avfaudio/avaudiounittypeformatconverter)
- [let AVAudioUnitTypeEffect: String](/documentation/avfaudio/avaudiounittypeeffect)
- [let AVAudioUnitTypeMixer: String](/documentation/avfaudio/avaudiounittypemixer)
- [let AVAudioUnitTypePanner: String](/documentation/avfaudio/avaudiounittypepanner)
- [let AVAudioUnitTypeGenerator: String](/documentation/avfaudio/avaudiounittypegenerator)
- [let AVAudioUnitTypeOfflineEffect: String](/documentation/avfaudio/avaudiounittypeofflineeffect)
- [let AVAudioUnitTypeMIDIProcessor: String](/documentation/avfaudio/avaudiounittypemidiprocessor)
- [AVAudioUnitComponentManager](/documentation/avfaudio/avaudiounitcomponentmanager)

##### Getting the unit audio component manager

- [class func shared() -> Self](/documentation/avfaudio/avaudiounitcomponentmanager/shared())

##### Getting matching audio components

- [func components(matching: AudioComponentDescription) -> [AVAudioUnitComponent]](/documentation/avfaudio/avaudiounitcomponentmanager/components(matching:)-9qt94)
- [func components(matching: NSPredicate) -> [AVAudioUnitComponent]](/documentation/avfaudio/avaudiounitcomponentmanager/components(matching:)-96l2c)
- [func components(passingTest: (AVAudioUnitComponent, UnsafeMutablePointer<ObjCBool>) -> Bool) -> [AVAudioUnitComponent]](/documentation/avfaudio/avaudiounitcomponentmanager/components(passingtest:))

##### Getting audio unit tags

- [var standardLocalizedTagNames: [String]](/documentation/avfaudio/avaudiounitcomponentmanager/standardlocalizedtagnames)
- [var tagNames: [String]](/documentation/avfaudio/avaudiounitcomponentmanager/tagnames)

##### Observing registration changes

- [class let registrationsChangedNotification: NSNotification.Name](/documentation/avfaudio/avaudiounitcomponentmanager/registrationschangednotification)

#### Audio effects

- [AVAudioUnitEffect](/documentation/avfaudio/avaudiouniteffect)

##### Creating an audio effect

- [init(audioComponentDescription: AudioComponentDescription)](/documentation/avfaudio/avaudiouniteffect/init(audiocomponentdescription:))

##### Getting the bypass state

- [var bypass: Bool](/documentation/avfaudio/avaudiouniteffect/bypass)
- [AVAudioUnitEQ](/documentation/avfaudio/avaudiouniteq)

##### Creating an equalizer

- [init(numberOfBands: Int)](/documentation/avfaudio/avaudiouniteq/init(numberofbands:))

##### Getting and setting the equalizer values

- [AVAudioUnitEQFilterParameters](/documentation/avfaudio/avaudiouniteqfilterparameters)

###### Getting and Setting Equalizer Filter Parameters

- [var bandwidth: Float](/documentation/avfaudio/avaudiouniteqfilterparameters/bandwidth)
- [var bypass: Bool](/documentation/avfaudio/avaudiouniteqfilterparameters/bypass)
- [var filterType: AVAudioUnitEQFilterType](/documentation/avfaudio/avaudiouniteqfilterparameters/filtertype)
- [var frequency: Float](/documentation/avfaudio/avaudiouniteqfilterparameters/frequency)
- [var gain: Float](/documentation/avfaudio/avaudiouniteqfilterparameters/gain)

###### Constants

- [AVAudioUnitEQFilterType](/documentation/avfaudio/avaudiouniteqfiltertype)

###### Filter Types

- [case parametric](/documentation/avfaudio/avaudiouniteqfiltertype/parametric)
- [case lowPass](/documentation/avfaudio/avaudiouniteqfiltertype/lowpass)
- [case highPass](/documentation/avfaudio/avaudiouniteqfiltertype/highpass)
- [case resonantLowPass](/documentation/avfaudio/avaudiouniteqfiltertype/resonantlowpass)
- [case resonantHighPass](/documentation/avfaudio/avaudiouniteqfiltertype/resonanthighpass)
- [case bandPass](/documentation/avfaudio/avaudiouniteqfiltertype/bandpass)
- [case bandStop](/documentation/avfaudio/avaudiouniteqfiltertype/bandstop)
- [case lowShelf](/documentation/avfaudio/avaudiouniteqfiltertype/lowshelf)
- [case highShelf](/documentation/avfaudio/avaudiouniteqfiltertype/highshelf)
- [case resonantLowShelf](/documentation/avfaudio/avaudiouniteqfiltertype/resonantlowshelf)
- [case resonantHighShelf](/documentation/avfaudio/avaudiouniteqfiltertype/resonanthighshelf)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiouniteqfiltertype/init(rawvalue:))
- [var bands: [AVAudioUnitEQFilterParameters]](/documentation/avfaudio/avaudiouniteq/bands)
- [var globalGain: Float](/documentation/avfaudio/avaudiouniteq/globalgain)
- [AVAudioUnitDistortion](/documentation/avfaudio/avaudiounitdistortion)

##### Configuring the distortion

- [func loadFactoryPreset(AVAudioUnitDistortionPreset)](/documentation/avfaudio/avaudiounitdistortion/loadfactorypreset(_:))
- [AVAudioUnitDistortionPreset](/documentation/avfaudio/avaudiounitdistortionpreset)

###### Presets

- [case drumsBitBrush](/documentation/avfaudio/avaudiounitdistortionpreset/drumsbitbrush)
- [case drumsBufferBeats](/documentation/avfaudio/avaudiounitdistortionpreset/drumsbufferbeats)
- [case drumsLoFi](/documentation/avfaudio/avaudiounitdistortionpreset/drumslofi)
- [case multiBrokenSpeaker](/documentation/avfaudio/avaudiounitdistortionpreset/multibrokenspeaker)
- [case multiCellphoneConcert](/documentation/avfaudio/avaudiounitdistortionpreset/multicellphoneconcert)
- [case multiDecimated1](/documentation/avfaudio/avaudiounitdistortionpreset/multidecimated1)
- [case multiDecimated2](/documentation/avfaudio/avaudiounitdistortionpreset/multidecimated2)
- [case multiDecimated3](/documentation/avfaudio/avaudiounitdistortionpreset/multidecimated3)
- [case multiDecimated4](/documentation/avfaudio/avaudiounitdistortionpreset/multidecimated4)
- [case multiDistortedFunk](/documentation/avfaudio/avaudiounitdistortionpreset/multidistortedfunk)
- [case multiDistortedCubed](/documentation/avfaudio/avaudiounitdistortionpreset/multidistortedcubed)
- [case multiDistortedSquared](/documentation/avfaudio/avaudiounitdistortionpreset/multidistortedsquared)
- [case multiEcho1](/documentation/avfaudio/avaudiounitdistortionpreset/multiecho1)
- [case multiEcho2](/documentation/avfaudio/avaudiounitdistortionpreset/multiecho2)
- [case multiEchoTight1](/documentation/avfaudio/avaudiounitdistortionpreset/multiechotight1)
- [case multiEchoTight2](/documentation/avfaudio/avaudiounitdistortionpreset/multiechotight2)
- [case multiEverythingIsBroken](/documentation/avfaudio/avaudiounitdistortionpreset/multieverythingisbroken)
- [case speechAlienChatter](/documentation/avfaudio/avaudiounitdistortionpreset/speechalienchatter)
- [case speechCosmicInterference](/documentation/avfaudio/avaudiounitdistortionpreset/speechcosmicinterference)
- [case speechGoldenPi](/documentation/avfaudio/avaudiounitdistortionpreset/speechgoldenpi)
- [case speechRadioTower](/documentation/avfaudio/avaudiounitdistortionpreset/speechradiotower)
- [case speechWaves](/documentation/avfaudio/avaudiounitdistortionpreset/speechwaves)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiounitdistortionpreset/init(rawvalue:))

##### Getting and setting the distortion values

- [var preGain: Float](/documentation/avfaudio/avaudiounitdistortion/pregain)
- [var wetDryMix: Float](/documentation/avfaudio/avaudiounitdistortion/wetdrymix)
- [AVAudioUnitDelay](/documentation/avfaudio/avaudiounitdelay)

##### Getting and setting the delay values

- [var delayTime: TimeInterval](/documentation/avfaudio/avaudiounitdelay/delaytime)
- [var feedback: Float](/documentation/avfaudio/avaudiounitdelay/feedback)
- [var lowPassCutoff: Float](/documentation/avfaudio/avaudiounitdelay/lowpasscutoff)
- [var wetDryMix: Float](/documentation/avfaudio/avaudiounitdelay/wetdrymix)
- [AVAudioUnitReverb](/documentation/avfaudio/avaudiounitreverb)

##### Configure the reverb

- [func loadFactoryPreset(AVAudioUnitReverbPreset)](/documentation/avfaudio/avaudiounitreverb/loadfactorypreset(_:))
- [AVAudioUnitReverbPreset](/documentation/avfaudio/avaudiounitreverbpreset)

###### Presets

- [case smallRoom](/documentation/avfaudio/avaudiounitreverbpreset/smallroom)
- [case mediumRoom](/documentation/avfaudio/avaudiounitreverbpreset/mediumroom)
- [case largeRoom](/documentation/avfaudio/avaudiounitreverbpreset/largeroom)
- [case mediumHall](/documentation/avfaudio/avaudiounitreverbpreset/mediumhall)
- [case largeHall](/documentation/avfaudio/avaudiounitreverbpreset/largehall)
- [case plate](/documentation/avfaudio/avaudiounitreverbpreset/plate)
- [case mediumChamber](/documentation/avfaudio/avaudiounitreverbpreset/mediumchamber)
- [case largeChamber](/documentation/avfaudio/avaudiounitreverbpreset/largechamber)
- [case cathedral](/documentation/avfaudio/avaudiounitreverbpreset/cathedral)
- [case largeRoom2](/documentation/avfaudio/avaudiounitreverbpreset/largeroom2)
- [case mediumHall2](/documentation/avfaudio/avaudiounitreverbpreset/mediumhall2)
- [case mediumHall3](/documentation/avfaudio/avaudiounitreverbpreset/mediumhall3)
- [case largeHall2](/documentation/avfaudio/avaudiounitreverbpreset/largehall2)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiounitreverbpreset/init(rawvalue:))

##### Getting and setting the reverb values

- [var wetDryMix: Float](/documentation/avfaudio/avaudiounitreverb/wetdrymix)

#### Time effects

- [AVAudioUnitTimeEffect](/documentation/avfaudio/avaudiounittimeeffect)

##### Creating a time effect

- [init(audioComponentDescription: AudioComponentDescription)](/documentation/avfaudio/avaudiounittimeeffect/init(audiocomponentdescription:))

##### Getting and setting the time effect

- [var bypass: Bool](/documentation/avfaudio/avaudiounittimeeffect/bypass)
- [AVAudioUnitTimePitch](/documentation/avfaudio/avaudiounittimepitch)

##### Getting and setting time pitch values

- [var overlap: Float](/documentation/avfaudio/avaudiounittimepitch/overlap)
- [var pitch: Float](/documentation/avfaudio/avaudiounittimepitch/pitch)
- [var rate: Float](/documentation/avfaudio/avaudiounittimepitch/rate)
- [AVAudioUnitVarispeed](/documentation/avfaudio/avaudiounitvarispeed)

##### Getting and setting the playback rate

- [var rate: Float](/documentation/avfaudio/avaudiounitvarispeed/rate)

#### Audio generation

- [AVAudioUnitGenerator](/documentation/avfaudio/avaudiounitgenerator)

##### Creating an audio unit generator

- [init(audioComponentDescription: AudioComponentDescription)](/documentation/avfaudio/avaudiounitgenerator/init(audiocomponentdescription:))

##### Getting and setting the bypass status

- [var bypass: Bool](/documentation/avfaudio/avaudiounitgenerator/bypass)

#### Speech synthesis

- [Creating a custom speech synthesizer](/documentation/avfaudio/creating-a-custom-speech-synthesizer)
- [AVSpeechSynthesisProviderAudioUnit](/documentation/avfaudio/avspeechsynthesisprovideraudiounit)

##### Rendering speech

- [func synthesizeSpeechRequest(AVSpeechSynthesisProviderRequest)](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/synthesizespeechrequest(_:))
- [AVSpeechSynthesisProviderRequest](/documentation/avfaudio/avspeechsynthesisproviderrequest)

###### Creating a request

- [init(ssmlRepresentation: String, voice: AVSpeechSynthesisProviderVoice)](/documentation/avfaudio/avspeechsynthesisproviderrequest/init(ssmlrepresentation:voice:))

###### Inspecting a request

- [var ssmlRepresentation: String](/documentation/avfaudio/avspeechsynthesisproviderrequest/ssmlrepresentation)
- [var voice: AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisproviderrequest/voice)
- [AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisprovidervoice)

###### Creating a voice

- [init(name: String, identifier: String, primaryLanguages: [String], supportedLanguages: [String])](/documentation/avfaudio/avspeechsynthesisprovidervoice/init(name:identifier:primarylanguages:supportedlanguages:))

###### Inspecting a voice

- [var age: Int](/documentation/avfaudio/avspeechsynthesisprovidervoice/age)
- [var gender: AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisprovidervoice/gender)
- [AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoicegender)

###### Voice genders

- [case unspecified](/documentation/avfaudio/avspeechsynthesisvoicegender/unspecified)
- [case male](/documentation/avfaudio/avspeechsynthesisvoicegender/male)
- [case female](/documentation/avfaudio/avspeechsynthesisvoicegender/female)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicegender/init(rawvalue:))
- [var identifier: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/identifier)
- [var name: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/name)
- [var primaryLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/primarylanguages)
- [var supportedLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/supportedlanguages)
- [var version: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/version)
- [var voiceSize: Int64](/documentation/avfaudio/avspeechsynthesisprovidervoice/voicesize)

###### Updating a voice

- [class func updateSpeechVoices()](/documentation/avfaudio/avspeechsynthesisprovidervoice/updatespeechvoices())

##### Supplying metadata

- [AVSpeechSynthesisProviderOutputBlock](/documentation/avfaudio/avspeechsynthesisprovideroutputblock)
- [var speechSynthesisOutputMetadataBlock: AVSpeechSynthesisProviderOutputBlock?](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/speechsynthesisoutputmetadatablock)
- [AVSpeechSynthesisMarker](/documentation/avfaudio/avspeechsynthesismarker)

###### Creating a marker

- [init(markerType: AVSpeechSynthesisMarker.Mark, forTextRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(markertype:fortextrange:atbytesampleoffset:))
- [init(wordRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(wordrange:atbytesampleoffset:))
- [init(sentenceRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(sentencerange:atbytesampleoffset:))
- [init(paragraphRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(paragraphrange:atbytesampleoffset:))
- [init(phonemeString: String, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(phonemestring:atbytesampleoffset:))
- [init(bookmarkName: String, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(bookmarkname:atbytesampleoffset:))

###### Inspecting a marker

- [var mark: AVSpeechSynthesisMarker.Mark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.property)
- [var bookmarkName: String](/documentation/avfaudio/avspeechsynthesismarker/bookmarkname)
- [var phoneme: String](/documentation/avfaudio/avspeechsynthesismarker/phoneme)
- [var textRange: NSRange](/documentation/avfaudio/avspeechsynthesismarker/textrange)
- [var byteSampleOffset: Int](/documentation/avfaudio/avspeechsynthesismarker/bytesampleoffset)
- [AVSpeechSynthesisMarker.Mark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum)

###### Marks

- [case word](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/word)
- [case sentence](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/sentence)
- [case paragraph](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/paragraph)
- [case phoneme](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/phoneme)
- [case bookmark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/bookmark)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/init(rawvalue:))

##### Getting and setting voices

- [var speechVoices: [AVSpeechSynthesisProviderVoice]](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/speechvoices)
- [AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisprovidervoice)

###### Creating a voice

- [init(name: String, identifier: String, primaryLanguages: [String], supportedLanguages: [String])](/documentation/avfaudio/avspeechsynthesisprovidervoice/init(name:identifier:primarylanguages:supportedlanguages:))

###### Inspecting a voice

- [var age: Int](/documentation/avfaudio/avspeechsynthesisprovidervoice/age)
- [var gender: AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisprovidervoice/gender)
- [AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoicegender)

###### Voice genders

- [case unspecified](/documentation/avfaudio/avspeechsynthesisvoicegender/unspecified)
- [case male](/documentation/avfaudio/avspeechsynthesisvoicegender/male)
- [case female](/documentation/avfaudio/avspeechsynthesisvoicegender/female)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicegender/init(rawvalue:))
- [var identifier: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/identifier)
- [var name: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/name)
- [var primaryLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/primarylanguages)
- [var supportedLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/supportedlanguages)
- [var version: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/version)
- [var voiceSize: Int64](/documentation/avfaudio/avspeechsynthesisprovidervoice/voicesize)

###### Updating a voice

- [class func updateSpeechVoices()](/documentation/avfaudio/avspeechsynthesisprovidervoice/updatespeechvoices())

##### Cancelling a request

- [func cancelSpeechRequest()](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/cancelspeechrequest())

#### MIDI

- [AVAudioUnitMIDIInstrument](/documentation/avfaudio/avaudiounitmidiinstrument)

##### Creating a MIDI instrument

- [init(audioComponentDescription: AudioComponentDescription)](/documentation/avfaudio/avaudiounitmidiinstrument/init(audiocomponentdescription:))

##### Sending information to the MIDI instrument

- [func sendController(UInt8, withValue: UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendcontroller(_:withvalue:onchannel:))
- [func sendMIDIEvent(UInt8, data1: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendmidievent(_:data1:))
- [func sendMIDIEvent(UInt8, data1: UInt8, data2: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendmidievent(_:data1:data2:))
- [func sendMIDISysExEvent(Data)](/documentation/avfaudio/avaudiounitmidiinstrument/sendmidisysexevent(_:))
- [func sendPitchBend(UInt16, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendpitchbend(_:onchannel:))
- [func sendPressure(UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendpressure(_:onchannel:))
- [func sendPressure(forKey: UInt8, withValue: UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendpressure(forkey:withvalue:onchannel:))
- [func sendProgramChange(UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendprogramchange(_:onchannel:))
- [func sendProgramChange(UInt8, bankMSB: UInt8, bankLSB: UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/sendprogramchange(_:bankmsb:banklsb:onchannel:))
- [func send(UnsafePointer<MIDIEventList>)](/documentation/avfaudio/avaudiounitmidiinstrument/send(_:))

##### Starting and stopping play

- [func startNote(UInt8, withVelocity: UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/startnote(_:withvelocity:onchannel:))
- [func stopNote(UInt8, onChannel: UInt8)](/documentation/avfaudio/avaudiounitmidiinstrument/stopnote(_:onchannel:))

### Rendering

- [Building a signal generator](/documentation/avfaudio/building-a-signal-generator)
- [Performing offline audio processing](/documentation/avfaudio/performing-offline-audio-processing)
- [AVAudioSourceNode](/documentation/avfaudio/avaudiosourcenode)

#### Creating an Audio Source Node

- [AVAudioSourceNodeRenderBlock](/documentation/avfaudio/avaudiosourcenoderenderblock)
- [init(renderBlock: AVAudioSourceNodeRenderBlock)](/documentation/avfaudio/avaudiosourcenode/init(renderblock:))
- [init(format: AVAudioFormat, renderBlock: AVAudioSourceNodeRenderBlock)](/documentation/avfaudio/avaudiosourcenode/init(format:renderblock:))
- [AVAudioSinkNode](/documentation/avfaudio/avaudiosinknode)

#### Creating an Audio Sink Node

- [AVAudioSinkNodeReceiverBlock](/documentation/avfaudio/avaudiosinknodereceiverblock)
- [init(receiverBlock: AVAudioSinkNodeReceiverBlock)](/documentation/avfaudio/avaudiosinknode/init(receiverblock:))

### Conversion

- [AVAudioConverter](/documentation/avfaudio/avaudioconverter)

#### Creating an Audio Converter

- [init?(from: AVAudioFormat, to: AVAudioFormat)](/documentation/avfaudio/avaudioconverter/init(from:to:))

#### Converting Audio Formats

- [func convert(to: AVAudioBuffer, error: NSErrorPointer, withInputFrom: AVAudioConverterInputBlock) -> AVAudioConverterOutputStatus](/documentation/avfaudio/avaudioconverter/convert(to:error:withinputfrom:))

##### Callbacks

- [AVAudioConverterInputBlock](/documentation/avfaudio/avaudioconverterinputblock)
- [AVAudioConverterInputBlock](/documentation/avfaudio/avaudioconverterinputblock)
- [func convert(to: AVAudioPCMBuffer, from: AVAudioPCMBuffer) throws](/documentation/avfaudio/avaudioconverter/convert(to:from:))
- [AVAudioConverterInputStatus](/documentation/avfaudio/avaudioconverterinputstatus)

##### Status Options

- [case endOfStream](/documentation/avfaudio/avaudioconverterinputstatus/endofstream)
- [case haveData](/documentation/avfaudio/avaudioconverterinputstatus/havedata)
- [case noDataNow](/documentation/avfaudio/avaudioconverterinputstatus/nodatanow)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioconverterinputstatus/init(rawvalue:))
- [AVAudioConverterOutputStatus](/documentation/avfaudio/avaudioconverteroutputstatus)

##### Status Options

- [case haveData](/documentation/avfaudio/avaudioconverteroutputstatus/havedata)
- [case inputRanDry](/documentation/avfaudio/avaudioconverteroutputstatus/inputrandry)
- [case endOfStream](/documentation/avfaudio/avaudioconverteroutputstatus/endofstream)
- [case error](/documentation/avfaudio/avaudioconverteroutputstatus/error)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioconverteroutputstatus/init(rawvalue:))

#### Resetting an Audio Converter

- [func reset()](/documentation/avfaudio/avaudioconverter/reset())

#### Getting Audio Converter Properties

- [var channelMap: [NSNumber]](/documentation/avfaudio/avaudioconverter/channelmap)
- [var dither: Bool](/documentation/avfaudio/avaudioconverter/dither)
- [var downmix: Bool](/documentation/avfaudio/avaudioconverter/downmix)
- [var inputFormat: AVAudioFormat](/documentation/avfaudio/avaudioconverter/inputformat)
- [var outputFormat: AVAudioFormat](/documentation/avfaudio/avaudioconverter/outputformat)
- [var magicCookie: Data?](/documentation/avfaudio/avaudioconverter/magiccookie)
- [var maximumOutputPacketSize: Int](/documentation/avfaudio/avaudioconverter/maximumoutputpacketsize)

#### Getting Bit Rate Properties

- [var applicableEncodeBitRates: [NSNumber]?](/documentation/avfaudio/avaudioconverter/applicableencodebitrates)
- [var availableEncodeBitRates: [NSNumber]?](/documentation/avfaudio/avaudioconverter/availableencodebitrates)
- [var availableEncodeChannelLayoutTags: [NSNumber]?](/documentation/avfaudio/avaudioconverter/availableencodechannellayouttags)
- [var bitRate: Int](/documentation/avfaudio/avaudioconverter/bitrate)
- [var bitRateStrategy: String?](/documentation/avfaudio/avaudioconverter/bitratestrategy)

#### Getting Sample Rate Properties

- [var sampleRateConverterQuality: Int](/documentation/avfaudio/avaudioconverter/samplerateconverterquality)
- [var sampleRateConverterAlgorithm: String?](/documentation/avfaudio/avaudioconverter/samplerateconverteralgorithm)

##### Algorithms

- [let AVSampleRateConverterAlgorithm_Normal: String](/documentation/avfaudio/avsamplerateconverteralgorithm_normal)
- [let AVSampleRateConverterAlgorithm_MinimumPhase: String](/documentation/avfaudio/avsamplerateconverteralgorithm_minimumphase)
- [let AVSampleRateConverterAlgorithm_Mastering: String](/documentation/avfaudio/avsamplerateconverteralgorithm_mastering)
- [var applicableEncodeSampleRates: [NSNumber]?](/documentation/avfaudio/avaudioconverter/applicableencodesamplerates)
- [var availableEncodeSampleRates: [NSNumber]?](/documentation/avfaudio/avaudioconverter/availableencodesamplerates)

#### Getting Priming Information

- [var primeInfo: AVAudioConverterPrimeInfo](/documentation/avfaudio/avaudioconverter/primeinfo)
- [var primeMethod: AVAudioConverterPrimeMethod](/documentation/avfaudio/avaudioconverter/primemethod)
- [AVAudioConverterPrimeInfo](/documentation/avfaudio/avaudioconverterprimeinfo)

##### Creating Priming Information

- [init()](/documentation/avfaudio/avaudioconverterprimeinfo/init())
- [init(leadingFrames: AVAudioFrameCount, trailingFrames: AVAudioFrameCount)](/documentation/avfaudio/avaudioconverterprimeinfo/init(leadingframes:trailingframes:))

##### Getting Frame Properties

- [var leadingFrames: AVAudioFrameCount](/documentation/avfaudio/avaudioconverterprimeinfo/leadingframes)
- [var trailingFrames: AVAudioFrameCount](/documentation/avfaudio/avaudioconverterprimeinfo/trailingframes)
- [AVAudioConverterPrimeMethod](/documentation/avfaudio/avaudioconverterprimemethod)

##### Options

- [case pre](/documentation/avfaudio/avaudioconverterprimemethod/pre)
- [case normal](/documentation/avfaudio/avaudioconverterprimemethod/normal)
- [case none](/documentation/avfaudio/avaudioconverterprimemethod/none)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioconverterprimemethod/init(rawvalue:))

#### Managing packet dependencies

- [var audioSyncPacketFrequency: Int](/documentation/avfaudio/avaudioconverter/audiosyncpacketfrequency)
- [var contentSource: AVAudioContentSource](/documentation/avfaudio/avaudioconverter/contentsource)
- [AVAudioContentSource](/documentation/avfaudio/avaudiocontentsource)

##### Content sources

- [case appleAV_Spatial_Live](/documentation/avfaudio/avaudiocontentsource/appleav_spatial_live)
- [case appleAV_Spatial_Offline](/documentation/avfaudio/avaudiocontentsource/appleav_spatial_offline)
- [case appleAV_Traditional_Live](/documentation/avfaudio/avaudiocontentsource/appleav_traditional_live)
- [case appleAV_Traditional_Offline](/documentation/avfaudio/avaudiocontentsource/appleav_traditional_offline)
- [case appleCapture_Spatial_Enhanced](/documentation/avfaudio/avaudiocontentsource/applecapture_spatial_enhanced)
- [case appleCapture_Spatial](/documentation/avfaudio/avaudiocontentsource/applecapture_spatial)
- [case appleCapture_Traditional](/documentation/avfaudio/avaudiocontentsource/applecapture_traditional)
- [case appleMusic_Spatial](/documentation/avfaudio/avaudiocontentsource/applemusic_spatial)
- [case appleMusic_Traditional](/documentation/avfaudio/avaudiocontentsource/applemusic_traditional)
- [case applePassthrough](/documentation/avfaudio/avaudiocontentsource/applepassthrough)
- [case av_Spatial_Live](/documentation/avfaudio/avaudiocontentsource/av_spatial_live)
- [case av_Spatial_Offline](/documentation/avfaudio/avaudiocontentsource/av_spatial_offline)
- [case av_Traditional_Live](/documentation/avfaudio/avaudiocontentsource/av_traditional_live)
- [case av_Traditional_Offline](/documentation/avfaudio/avaudiocontentsource/av_traditional_offline)
- [case capture_Spatial_Enhanced](/documentation/avfaudio/avaudiocontentsource/capture_spatial_enhanced)
- [case capture_Spatial](/documentation/avfaudio/avaudiocontentsource/capture_spatial)
- [case capture_Traditional](/documentation/avfaudio/avaudiocontentsource/capture_traditional)
- [case music_Spatial](/documentation/avfaudio/avaudiocontentsource/music_spatial)
- [case music_Traditional](/documentation/avfaudio/avaudiocontentsource/music_traditional)
- [case passthrough](/documentation/avfaudio/avaudiocontentsource/passthrough)
- [case reserved](/documentation/avfaudio/avaudiocontentsource/reserved)
- [case unspecified](/documentation/avfaudio/avaudiocontentsource/unspecified)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiocontentsource/init(rawvalue:))
- [var dynamicRangeControlConfiguration: AVAudioDynamicRangeControlConfiguration](/documentation/avfaudio/avaudioconverter/dynamicrangecontrolconfiguration)
- [AVAudioDynamicRangeControlConfiguration](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration)

##### Configurations

- [case capture](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/capture)
- [case movie](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/movie)
- [case music](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/music)
- [case none](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/none)
- [case speech](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/speech)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudiodynamicrangecontrolconfiguration/init(rawvalue:))

### Spatial audio

- [AVAudioEnvironmentNode](/documentation/avfaudio/avaudioenvironmentnode)

#### Creating an Environment Node

- [init()](/documentation/avfaudio/avaudioenvironmentnode/init())

#### Getting and Setting Positional Properties

- [var listenerPosition: AVAudio3DPoint](/documentation/avfaudio/avaudioenvironmentnode/listenerposition)
- [var listenerAngularOrientation: AVAudio3DAngularOrientation](/documentation/avfaudio/avaudioenvironmentnode/listenerangularorientation)
- [var listenerVectorOrientation: AVAudio3DVectorOrientation](/documentation/avfaudio/avaudioenvironmentnode/listenervectororientation)

#### Getting Attenuation and Reverb Properties

- [var distanceAttenuationParameters: AVAudioEnvironmentDistanceAttenuationParameters](/documentation/avfaudio/avaudioenvironmentnode/distanceattenuationparameters)
- [var reverbParameters: AVAudioEnvironmentReverbParameters](/documentation/avfaudio/avaudioenvironmentnode/reverbparameters)

#### Getting and Setting Environment Properties

- [var outputVolume: Float](/documentation/avfaudio/avaudioenvironmentnode/outputvolume)
- [var outputType: AVAudioEnvironmentOutputType](/documentation/avfaudio/avaudioenvironmentnode/outputtype)

#### Getting the Available Rendering Algorithms

- [var applicableRenderingAlgorithms: [NSNumber]](/documentation/avfaudio/avaudioenvironmentnode/applicablerenderingalgorithms)

#### Getting the Head Tracking Status

- [var isListenerHeadTrackingEnabled: Bool](/documentation/avfaudio/avaudioenvironmentnode/islistenerheadtrackingenabled)

#### Getting the Input Bus

- [var nextAvailableInputBus: AVAudioNodeBus](/documentation/avfaudio/avaudioenvironmentnode/nextavailableinputbus)
- [AVAudioEnvironmentDistanceAttenuationParameters](/documentation/avfaudio/avaudioenvironmentdistanceattenuationparameters)

#### Getting and Setting the Attenuation Model

- [var distanceAttenuationModel: AVAudioEnvironmentDistanceAttenuationModel](/documentation/avfaudio/avaudioenvironmentdistanceattenuationparameters/distanceattenuationmodel)
- [AVAudioEnvironmentDistanceAttenuationModel](/documentation/avfaudio/avaudioenvironmentdistanceattenuationmodel)

##### Attenuation Models

- [case exponential](/documentation/avfaudio/avaudioenvironmentdistanceattenuationmodel/exponential)
- [case inverse](/documentation/avfaudio/avaudioenvironmentdistanceattenuationmodel/inverse)
- [case linear](/documentation/avfaudio/avaudioenvironmentdistanceattenuationmodel/linear)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioenvironmentdistanceattenuationmodel/init(rawvalue:))

#### Getting and Setting the Attenuation Values

- [var maximumDistance: Float](/documentation/avfaudio/avaudioenvironmentdistanceattenuationparameters/maximumdistance)
- [var referenceDistance: Float](/documentation/avfaudio/avaudioenvironmentdistanceattenuationparameters/referencedistance)
- [var rolloffFactor: Float](/documentation/avfaudio/avaudioenvironmentdistanceattenuationparameters/rollofffactor)
- [AVAudioEnvironmentReverbParameters](/documentation/avfaudio/avaudioenvironmentreverbparameters)

#### Enabling and Disabling Reverb

- [var enable: Bool](/documentation/avfaudio/avaudioenvironmentreverbparameters/enable)

#### Getting and Setting Reverb Values

- [var level: Float](/documentation/avfaudio/avaudioenvironmentreverbparameters/level)
- [var filterParameters: AVAudioUnitEQFilterParameters](/documentation/avfaudio/avaudioenvironmentreverbparameters/filterparameters)
- [func loadFactoryReverbPreset(AVAudioUnitReverbPreset)](/documentation/avfaudio/avaudioenvironmentreverbparameters/loadfactoryreverbpreset(_:))
- [AVAudio3DMixing](/documentation/avfaudio/avaudio3dmixing)

#### Getting the 3D Mixing Parameters

- [var obstruction: Float](/documentation/avfaudio/avaudio3dmixing/obstruction)
- [var occlusion: Float](/documentation/avfaudio/avaudio3dmixing/occlusion)
- [var position: AVAudio3DPoint](/documentation/avfaudio/avaudio3dmixing/position)
- [var rate: Float](/documentation/avfaudio/avaudio3dmixing/rate)
- [var pointSourceInHeadMode: AVAudio3DMixingPointSourceInHeadMode](/documentation/avfaudio/avaudio3dmixing/pointsourceinheadmode)
- [var reverbBlend: Float](/documentation/avfaudio/avaudio3dmixing/reverbblend)
- [var sourceMode: AVAudio3DMixingSourceMode](/documentation/avfaudio/avaudio3dmixing/sourcemode)

#### Getting and Setting the Rendering Algorithm

- [var renderingAlgorithm: AVAudio3DMixingRenderingAlgorithm](/documentation/avfaudio/avaudio3dmixing/renderingalgorithm)
- [AVAudio3DMixingRenderingAlgorithm](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm)

##### Rendering Algorithms

- [case auto](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/auto)
- [case equalPowerPanning](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/equalpowerpanning)
- [case HRTF](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtf)
- [case HRTFHQ](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtfhq)
- [case soundField](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/soundfield)
- [case sphericalHead](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/sphericalhead)
- [case stereoPassThrough](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/stereopassthrough)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/init(rawvalue:))
- [AVAudio3DPoint](/documentation/avfaudio/avaudio3dpoint)

#### Creating a Point

- [init()](/documentation/avfaudio/avaudio3dpoint/init())
- [init(x: Float, y: Float, z: Float)](/documentation/avfaudio/avaudio3dpoint/init(x:y:z:))
- [func AVAudioMake3DPoint(Float, Float, Float) -> AVAudio3DPoint](/documentation/avfaudio/avaudiomake3dpoint(_:_:_:))

#### Getting Point Properties

- [var x: Float](/documentation/avfaudio/avaudio3dpoint/x)
- [var y: Float](/documentation/avfaudio/avaudio3dpoint/y)
- [var z: Float](/documentation/avfaudio/avaudio3dpoint/z)
- [AVAudio3DVectorOrientation](/documentation/avfaudio/avaudio3dvectororientation)

#### Creating a Vector Orientation

- [init()](/documentation/avfaudio/avaudio3dvectororientation/init())
- [init(forward: AVAudio3DVector, up: AVAudio3DVector)](/documentation/avfaudio/avaudio3dvectororientation/init(forward:up:))
- [func AVAudioMake3DVectorOrientation(AVAudio3DVector, AVAudio3DVector) -> AVAudio3DVectorOrientation](/documentation/avfaudio/avaudiomake3dvectororientation(_:_:))

#### Getting Vector Orientation Properties

- [var forward: AVAudio3DVector](/documentation/avfaudio/avaudio3dvectororientation/forward)
- [var up: AVAudio3DVector](/documentation/avfaudio/avaudio3dvectororientation/up)
- [AVAudio3DAngularOrientation](/documentation/avfaudio/avaudio3dangularorientation)

#### Creating an Angular Orientation

- [init()](/documentation/avfaudio/avaudio3dangularorientation/init())
- [init(yaw: Float, pitch: Float, roll: Float)](/documentation/avfaudio/avaudio3dangularorientation/init(yaw:pitch:roll:))
- [func AVAudioMake3DAngularOrientation(Float, Float, Float) -> AVAudio3DAngularOrientation](/documentation/avfaudio/avaudiomake3dangularorientation(_:_:_:))

#### Getting Angular Orientation Properties

- [var yaw: Float](/documentation/avfaudio/avaudio3dangularorientation/yaw)
- [var pitch: Float](/documentation/avfaudio/avaudio3dangularorientation/pitch)
- [var roll: Float](/documentation/avfaudio/avaudio3dangularorientation/roll)
- [AVAudio3DMixingSourceMode](/documentation/avfaudio/avaudio3dmixingsourcemode)

#### Source Modes

- [case spatializeIfMono](/documentation/avfaudio/avaudio3dmixingsourcemode/spatializeifmono)
- [case bypass](/documentation/avfaudio/avaudio3dmixingsourcemode/bypass)
- [case pointSource](/documentation/avfaudio/avaudio3dmixingsourcemode/pointsource)
- [case ambienceBed](/documentation/avfaudio/avaudio3dmixingsourcemode/ambiencebed)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudio3dmixingsourcemode/init(rawvalue:))
- [AVAudio3DMixingRenderingAlgorithm](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm)

#### Rendering Algorithms

- [case auto](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/auto)
- [case equalPowerPanning](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/equalpowerpanning)
- [case HRTF](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtf)
- [case HRTFHQ](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/hrtfhq)
- [case soundField](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/soundfield)
- [case sphericalHead](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/sphericalhead)
- [case stereoPassThrough](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/stereopassthrough)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudio3dmixingrenderingalgorithm/init(rawvalue:))
- [AVAudioEnvironmentOutputType](/documentation/avfaudio/avaudioenvironmentoutputtype)

#### Output Types

- [case auto](/documentation/avfaudio/avaudioenvironmentoutputtype/auto)
- [case headphones](/documentation/avfaudio/avaudioenvironmentoutputtype/headphones)
- [case builtInSpeakers](/documentation/avfaudio/avaudioenvironmentoutputtype/builtinspeakers)
- [case externalSpeakers](/documentation/avfaudio/avaudioenvironmentoutputtype/externalspeakers)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioenvironmentoutputtype/init(rawvalue:))
- [AVAudio3DMixingPointSourceInHeadMode](/documentation/avfaudio/avaudio3dmixingpointsourceinheadmode)

#### In-Head Modes

- [case mono](/documentation/avfaudio/avaudio3dmixingpointsourceinheadmode/mono)
- [case bypass](/documentation/avfaudio/avaudio3dmixingpointsourceinheadmode/bypass)

#### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudio3dmixingpointsourceinheadmode/init(rawvalue:))
- [AVAudio3DVector](/documentation/avfaudio/avaudio3dvector)

#### Functions

- [func AVAudioMake3DVector(Float, Float, Float) -> AVAudio3DVector](/documentation/avfaudio/avaudiomake3dvector(_:_:_:))

### Supporting data types

- [AVAudioBuffer](/documentation/avfaudio/avaudiobuffer)

#### Getting the Buffer Format

- [var format: AVAudioFormat](/documentation/avfaudio/avaudiobuffer/format)

#### Getting the Audio Buffers

- [var audioBufferList: UnsafePointer<AudioBufferList>](/documentation/avfaudio/avaudiobuffer/audiobufferlist)
- [var mutableAudioBufferList: UnsafeMutablePointer<AudioBufferList>](/documentation/avfaudio/avaudiobuffer/mutableaudiobufferlist)

#### Specialized Audio Buffers

- [AVAudioCompressedBuffer](/documentation/avfaudio/avaudiocompressedbuffer)

##### Creating an Audio Buffer

- [init(format: AVAudioFormat, packetCapacity: AVAudioPacketCount)](/documentation/avfaudio/avaudiocompressedbuffer/init(format:packetcapacity:))
- [init(format: AVAudioFormat, packetCapacity: AVAudioPacketCount, maximumPacketSize: Int)](/documentation/avfaudio/avaudiocompressedbuffer/init(format:packetcapacity:maximumpacketsize:))

##### Getting Audio Buffer Properties

- [var byteCapacity: UInt32](/documentation/avfaudio/avaudiocompressedbuffer/bytecapacity)
- [var byteLength: UInt32](/documentation/avfaudio/avaudiocompressedbuffer/bytelength)
- [var data: UnsafeMutableRawPointer](/documentation/avfaudio/avaudiocompressedbuffer/data)
- [var maximumPacketSize: Int](/documentation/avfaudio/avaudiocompressedbuffer/maximumpacketsize)
- [var packetCapacity: AVAudioPacketCount](/documentation/avfaudio/avaudiocompressedbuffer/packetcapacity)
- [var packetCount: AVAudioPacketCount](/documentation/avfaudio/avaudiocompressedbuffer/packetcount)
- [AVAudioPacketCount](/documentation/avfaudio/avaudiopacketcount)
- [var packetDescriptions: UnsafeMutablePointer<AudioStreamPacketDescription>?](/documentation/avfaudio/avaudiocompressedbuffer/packetdescriptions)
- [var packetDependencies: [AudioStreamPacketDependencyDescription]?](/documentation/avfaudio/avaudiocompressedbuffer/packetdependencies-3a6ln)
- [AVAudioPCMBuffer](/documentation/avfaudio/avaudiopcmbuffer)

##### Creating a PCM Audio Buffer

- [init?(pcmFormat: AVAudioFormat, frameCapacity: AVAudioFrameCount)](/documentation/avfaudio/avaudiopcmbuffer/init(pcmformat:framecapacity:))
- [init?(pcmFormat: AVAudioFormat, bufferListNoCopy: UnsafePointer<AudioBufferList>, deallocator: ((UnsafePointer<AudioBufferList>) -> Void)?)](/documentation/avfaudio/avaudiopcmbuffer/init(pcmformat:bufferlistnocopy:deallocator:))

##### Getting and Setting the Frame Length

- [var frameLength: AVAudioFrameCount](/documentation/avfaudio/avaudiopcmbuffer/framelength)

##### Accessing PCM Buffer Data

- [var floatChannelData: UnsafePointer<UnsafeMutablePointer<Float>>?](/documentation/avfaudio/avaudiopcmbuffer/floatchanneldata)
- [var frameCapacity: AVAudioFrameCount](/documentation/avfaudio/avaudiopcmbuffer/framecapacity)
- [var int16ChannelData: UnsafePointer<UnsafeMutablePointer<Int16>>?](/documentation/avfaudio/avaudiopcmbuffer/int16channeldata)
- [var int32ChannelData: UnsafePointer<UnsafeMutablePointer<Int32>>?](/documentation/avfaudio/avaudiopcmbuffer/int32channeldata)
- [var stride: Int](/documentation/avfaudio/avaudiopcmbuffer/stride)
- [AVAudioFile](/documentation/avfaudio/avaudiofile)

#### Creating an Audio File

- [init(forReading: URL) throws](/documentation/avfaudio/avaudiofile/init(forreading:))
- [init(forReading: URL, commonFormat: AVAudioCommonFormat, interleaved: Bool) throws](/documentation/avfaudio/avaudiofile/init(forreading:commonformat:interleaved:))
- [init(forWriting: URL, settings: [String : Any]) throws](/documentation/avfaudio/avaudiofile/init(forwriting:settings:))
- [init(forWriting: URL, settings: [String : Any], commonFormat: AVAudioCommonFormat, interleaved: Bool) throws](/documentation/avfaudio/avaudiofile/init(forwriting:settings:commonformat:interleaved:))

#### Reading and Writing the Audio Buffer

- [func read(into: AVAudioPCMBuffer) throws](/documentation/avfaudio/avaudiofile/read(into:))
- [func read(into: AVAudioPCMBuffer, frameCount: AVAudioFrameCount) throws](/documentation/avfaudio/avaudiofile/read(into:framecount:))
- [func write(from: AVAudioPCMBuffer) throws](/documentation/avfaudio/avaudiofile/write(from:))
- [func close()](/documentation/avfaudio/avaudiofile/close())

#### Getting Audio File Properties

- [var url: URL](/documentation/avfaudio/avaudiofile/url)
- [var fileFormat: AVAudioFormat](/documentation/avfaudio/avaudiofile/fileformat)
- [var processingFormat: AVAudioFormat](/documentation/avfaudio/avaudiofile/processingformat)
- [var length: AVAudioFramePosition](/documentation/avfaudio/avaudiofile/length)
- [AVAudioFramePosition](/documentation/avfaudio/avaudioframeposition)
- [var framePosition: AVAudioFramePosition](/documentation/avfaudio/avaudiofile/frameposition)
- [AVAudioFrameCount](/documentation/avfaudio/avaudioframecount)
- [let AVAudioFileTypeKey: String](/documentation/avfaudio/avaudiofiletypekey)
- [var isOpen: Bool](/documentation/avfaudio/avaudiofile/isopen)

#### Initializers

- [init()](/documentation/avfaudio/avaudiofile/init())
- [AVAudioTime](/documentation/avfaudio/avaudiotime)

#### Creating an Audio Time Instance

- [init(audioTimeStamp: UnsafePointer<AudioTimeStamp>, sampleRate: Double)](/documentation/avfaudio/avaudiotime/init(audiotimestamp:samplerate:))
- [init(hostTime: UInt64)](/documentation/avfaudio/avaudiotime/init(hosttime:))
- [init(hostTime: UInt64, sampleTime: AVAudioFramePosition, atRate: Double)](/documentation/avfaudio/avaudiotime/init(hosttime:sampletime:atrate:))
- [init(sampleTime: AVAudioFramePosition, atRate: Double)](/documentation/avfaudio/avaudiotime/init(sampletime:atrate:))
- [func extrapolateTime(fromAnchor: AVAudioTime) -> AVAudioTime?](/documentation/avfaudio/avaudiotime/extrapolatetime(fromanchor:))

#### Manipulating Host Time

- [var hostTime: UInt64](/documentation/avfaudio/avaudiotime/hosttime)
- [var isHostTimeValid: Bool](/documentation/avfaudio/avaudiotime/ishosttimevalid)
- [class func hostTime(forSeconds: TimeInterval) -> UInt64](/documentation/avfaudio/avaudiotime/hosttime(forseconds:))
- [class func seconds(forHostTime: UInt64) -> TimeInterval](/documentation/avfaudio/avaudiotime/seconds(forhosttime:))

#### Getting Sample Rate Information

- [var sampleRate: Double](/documentation/avfaudio/avaudiotime/samplerate)
- [var sampleTime: AVAudioFramePosition](/documentation/avfaudio/avaudiotime/sampletime)
- [var isSampleTimeValid: Bool](/documentation/avfaudio/avaudiotime/issampletimevalid)

#### Getting the Core Audio Time Stamp

- [var audioTimeStamp: AudioTimeStamp](/documentation/avfaudio/avaudiotime/audiotimestamp)
- [Audio settings](/documentation/avfaudio/audio-settings)

#### Formats

- [AVAudioFormat](/documentation/avfaudio/avaudioformat)

##### Creating a New Audio Format Representation

- [init(standardFormatWithSampleRate: Double, channelLayout: AVAudioChannelLayout)](/documentation/avfaudio/avaudioformat/init(standardformatwithsamplerate:channellayout:))
- [init?(standardFormatWithSampleRate: Double, channels: AVAudioChannelCount)](/documentation/avfaudio/avaudioformat/init(standardformatwithsamplerate:channels:))
- [init?(commonFormat: AVAudioCommonFormat, sampleRate: Double, channels: AVAudioChannelCount, interleaved: Bool)](/documentation/avfaudio/avaudioformat/init(commonformat:samplerate:channels:interleaved:))
- [init(commonFormat: AVAudioCommonFormat, sampleRate: Double, interleaved: Bool, channelLayout: AVAudioChannelLayout)](/documentation/avfaudio/avaudioformat/init(commonformat:samplerate:interleaved:channellayout:))
- [init?(settings: [String : Any])](/documentation/avfaudio/avaudioformat/init(settings:))
- [init?(streamDescription: UnsafePointer<AudioStreamBasicDescription>)](/documentation/avfaudio/avaudioformat/init(streamdescription:))
- [init?(streamDescription: UnsafePointer<AudioStreamBasicDescription>, channelLayout: AVAudioChannelLayout?)](/documentation/avfaudio/avaudioformat/init(streamdescription:channellayout:))
- [init(cmAudioFormatDescription: CMAudioFormatDescription)](/documentation/avfaudio/avaudioformat/init(cmaudioformatdescription:))

##### Getting the Audio Stream Description

- [var streamDescription: UnsafePointer<AudioStreamBasicDescription>](/documentation/avfaudio/avaudioformat/streamdescription)

##### Comparing Instances

- [func isEqual(Any) -> Bool](/documentation/avfaudio/avaudioformat/isequal(_:))

##### Getting Audio Format Values

- [var sampleRate: Double](/documentation/avfaudio/avaudioformat/samplerate)
- [var channelCount: AVAudioChannelCount](/documentation/avfaudio/avaudioformat/channelcount)
- [var channelLayout: AVAudioChannelLayout?](/documentation/avfaudio/avaudioformat/channellayout)
- [var formatDescription: CMAudioFormatDescription](/documentation/avfaudio/avaudioformat/formatdescription)

##### Determining the Audio Format

- [var isInterleaved: Bool](/documentation/avfaudio/avaudioformat/isinterleaved)
- [var isStandard: Bool](/documentation/avfaudio/avaudioformat/isstandard)
- [var commonFormat: AVAudioCommonFormat](/documentation/avfaudio/avaudioformat/commonformat)
- [var settings: [String : Any]](/documentation/avfaudio/avaudioformat/settings)
- [var magicCookie: Data?](/documentation/avfaudio/avaudioformat/magiccookie)

##### Constants

- [AVAudioCommonFormat](/documentation/avfaudio/avaudiocommonformat)

###### Formats

- [case otherFormat](/documentation/avfaudio/avaudiocommonformat/otherformat)
- [case pcmFormatFloat32](/documentation/avfaudio/avaudiocommonformat/pcmformatfloat32)
- [case pcmFormatFloat64](/documentation/avfaudio/avaudiocommonformat/pcmformatfloat64)
- [case pcmFormatInt16](/documentation/avfaudio/avaudiocommonformat/pcmformatint16)
- [case pcmFormatInt32](/documentation/avfaudio/avaudiocommonformat/pcmformatint32)

###### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avaudiocommonformat/init(rawvalue:))
- [AVAudioChannelLayout](/documentation/avfaudio/avaudiochannellayout)

##### Creating an Audio Channel Layout

- [init(layout: UnsafePointer<AudioChannelLayout>)](/documentation/avfaudio/avaudiochannellayout/init(layout:))
- [convenience init?(layoutTag: AudioChannelLayoutTag)](/documentation/avfaudio/avaudiochannellayout/init(layouttag:))

##### Getting Audio Channel Layout Properties

- [AVAudioChannelCount](/documentation/avfaudio/avaudiochannelcount)
- [var channelCount: AVAudioChannelCount](/documentation/avfaudio/avaudiochannellayout/channelcount)
- [var layout: UnsafePointer<AudioChannelLayout>](/documentation/avfaudio/avaudiochannellayout/layout)
- [var layoutTag: AudioChannelLayoutTag](/documentation/avfaudio/avaudiochannellayout/layouttag)
- [func isEqual(Any) -> Bool](/documentation/avfaudio/avaudiochannellayout/isequal(_:))
- [let AVChannelLayoutKey: String](/documentation/avfaudio/avchannellayoutkey)
- [Linear PCM Format Settings](/documentation/avfaudio/linear-pcm-format-settings)

##### Settings

- [let AVLinearPCMBitDepthKey: String](/documentation/avfaudio/avlinearpcmbitdepthkey)
- [let AVLinearPCMIsBigEndianKey: String](/documentation/avfaudio/avlinearpcmisbigendiankey)
- [let AVLinearPCMIsFloatKey: String](/documentation/avfaudio/avlinearpcmisfloatkey)
- [let AVLinearPCMIsNonInterleaved: String](/documentation/avfaudio/avlinearpcmisnoninterleaved)
- [Format Settings](/documentation/avfaudio/format-settings)

##### Settings

- [let AVFormatIDKey: String](/documentation/avfaudio/avformatidkey)
- [let AVSampleRateKey: String](/documentation/avfaudio/avsampleratekey)
- [let AVNumberOfChannelsKey: String](/documentation/avfaudio/avnumberofchannelskey)

#### Settings

- [Sample Rate Conversion Settings](/documentation/avfaudio/sample-rate-conversion-settings)

##### Constants

- [let AVSampleRateConverterAudioQualityKey: String](/documentation/avfaudio/avsamplerateconverteraudioqualitykey)
- [let AVEncoderAudioQualityForVBRKey: String](/documentation/avfaudio/avencoderaudioqualityforvbrkey)
- [let AVSampleRateConverterAlgorithmKey: String](/documentation/avfaudio/avsamplerateconverteralgorithmkey)

###### Supported algorithms

- [let AVSampleRateConverterAlgorithm_Normal: String](/documentation/avfaudio/avsamplerateconverteralgorithm_normal)
- [let AVSampleRateConverterAlgorithm_MinimumPhase: String](/documentation/avfaudio/avsamplerateconverteralgorithm_minimumphase)
- [let AVSampleRateConverterAlgorithm_Mastering: String](/documentation/avfaudio/avsamplerateconverteralgorithm_mastering)
- [AVAudioQuality](/documentation/avfaudio/avaudioquality)

##### Constants

- [case min](/documentation/avfaudio/avaudioquality/min)
- [case low](/documentation/avfaudio/avaudioquality/low)
- [case medium](/documentation/avfaudio/avaudioquality/medium)
- [case high](/documentation/avfaudio/avaudioquality/high)
- [case max](/documentation/avfaudio/avaudioquality/max)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avaudioquality/init(rawvalue:))
- [let AVEncoderAudioQualityKey: String](/documentation/avfaudio/avencoderaudioqualitykey)
- [Encoder Settings](/documentation/avfaudio/encoder-settings)

##### Settings

- [let AVEncoderASPFrequencyKey: String](/documentation/avfaudio/avencoderaspfrequencykey)
- [let AVEncoderAudioQualityKey: String](/documentation/avfaudio/avencoderaudioqualitykey)
- [let AVEncoderBitDepthHintKey: String](/documentation/avfaudio/avencoderbitdepthhintkey)
- [let AVEncoderBitRateKey: String](/documentation/avfaudio/avencoderbitratekey)
- [let AVEncoderBitRatePerChannelKey: String](/documentation/avfaudio/avencoderbitrateperchannelkey)
- [let AVEncoderBitRateStrategyKey: String](/documentation/avfaudio/avencoderbitratestrategykey)

###### Bit Rate Strategies

- [let AVAudioBitRateStrategy_Constant: String](/documentation/avfaudio/avaudiobitratestrategy_constant)
- [let AVAudioBitRateStrategy_LongTermAverage: String](/documentation/avfaudio/avaudiobitratestrategy_longtermaverage)
- [let AVAudioBitRateStrategy_VariableConstrained: String](/documentation/avfaudio/avaudiobitratestrategy_variableconstrained)
- [let AVAudioBitRateStrategy_Variable: String](/documentation/avfaudio/avaudiobitratestrategy_variable)
- [let AVEncoderContentSourceKey: String](/documentation/avfaudio/avencodercontentsourcekey)
- [let AVEncoderDynamicRangeControlConfigurationKey: String](/documentation/avfaudio/avencoderdynamicrangecontrolconfigurationkey)
- [Time pitch algorithm settings](/documentation/avfoundation/time-pitch-algorithm-settings)

#### Constants

- [Encoder Bit Rate Strategy Values](/documentation/avfaudio/encoder-bit-rate-strategy-values)

##### Strategies

- [let AVAudioBitRateStrategy_Constant: String](/documentation/avfaudio/avaudiobitratestrategy_constant)
- [let AVAudioBitRateStrategy_LongTermAverage: String](/documentation/avfaudio/avaudiobitratestrategy_longtermaverage)
- [let AVAudioBitRateStrategy_VariableConstrained: String](/documentation/avfaudio/avaudiobitratestrategy_variableconstrained)
- [let AVAudioBitRateStrategy_Variable: String](/documentation/avfaudio/avaudiobitratestrategy_variable)
- [var AVAUDIOENGINE_HAVE_AUAUDIOUNIT: Int32](/documentation/avfaudio/avaudioengine_have_auaudiounit)

## Speech synthesis

- [Speech synthesis](/documentation/avfaudio/speech-synthesis)

### Spoken text attributes

- [AVSpeechUtterance](/documentation/avfaudio/avspeechutterance)

#### Creating an utterance

- [init(string: String)](/documentation/avfaudio/avspeechutterance/init(string:))
- [init(attributedString: NSAttributedString)](/documentation/avfaudio/avspeechutterance/init(attributedstring:))
- [let AVSpeechSynthesisIPANotationAttribute: String](/documentation/avfaudio/avspeechsynthesisipanotationattribute)
- [init?(ssmlRepresentation: String)](/documentation/avfaudio/avspeechutterance/init(ssmlrepresentation:))

#### Configuring an utterance

- [var voice: AVSpeechSynthesisVoice?](/documentation/avfaudio/avspeechutterance/voice)
- [var pitchMultiplier: Float](/documentation/avfaudio/avspeechutterance/pitchmultiplier)
- [var volume: Float](/documentation/avfaudio/avspeechutterance/volume)
- [var prefersAssistiveTechnologySettings: Bool](/documentation/avfaudio/avspeechutterance/prefersassistivetechnologysettings)

#### Configuring utterance timing

- [var rate: Float](/documentation/avfaudio/avspeechutterance/rate)
- [let AVSpeechUtteranceMinimumSpeechRate: Float](/documentation/avfaudio/avspeechutteranceminimumspeechrate)
- [let AVSpeechUtteranceMaximumSpeechRate: Float](/documentation/avfaudio/avspeechutterancemaximumspeechrate)
- [let AVSpeechUtteranceDefaultSpeechRate: Float](/documentation/avfaudio/avspeechutterancedefaultspeechrate)
- [var preUtteranceDelay: TimeInterval](/documentation/avfaudio/avspeechutterance/preutterancedelay)
- [var postUtteranceDelay: TimeInterval](/documentation/avfaudio/avspeechutterance/postutterancedelay)

#### Inspecting utterance text

- [var speechString: String](/documentation/avfaudio/avspeechutterance/speechstring)
- [var attributedSpeechString: NSAttributedString](/documentation/avfaudio/avspeechutterance/attributedspeechstring)
- [AVSpeechSynthesisVoice](/documentation/avfaudio/avspeechsynthesisvoice)

#### Obtaining voices

- [init?(identifier: String)](/documentation/avfaudio/avspeechsynthesisvoice/init(identifier:))
- [init?(language: String?)](/documentation/avfaudio/avspeechsynthesisvoice/init(language:))
- [class func speechVoices() -> [AVSpeechSynthesisVoice]](/documentation/avfaudio/avspeechsynthesisvoice/speechvoices())
- [let AVSpeechSynthesisVoiceIdentifierAlex: String](/documentation/avfaudio/avspeechsynthesisvoiceidentifieralex)

#### Inspecting voices

- [var identifier: String](/documentation/avfaudio/avspeechsynthesisvoice/identifier)
- [var name: String](/documentation/avfaudio/avspeechsynthesisvoice/name)
- [var quality: AVSpeechSynthesisVoiceQuality](/documentation/avfaudio/avspeechsynthesisvoice/quality)
- [var gender: AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoice/gender)
- [var voiceTraits: AVSpeechSynthesisVoice.Traits](/documentation/avfaudio/avspeechsynthesisvoice/voicetraits)
- [var audioFileSettings: [String : Any]](/documentation/avfaudio/avspeechsynthesisvoice/audiofilesettings)
- [AVSpeechSynthesisVoiceQuality](/documentation/avfaudio/avspeechsynthesisvoicequality)

##### Voice qualities

- [case `default`](/documentation/avfaudio/avspeechsynthesisvoicequality/default)
- [case enhanced](/documentation/avfaudio/avspeechsynthesisvoicequality/enhanced)
- [case premium](/documentation/avfaudio/avspeechsynthesisvoicequality/premium)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicequality/init(rawvalue:))
- [AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoicegender)

##### Voice genders

- [case unspecified](/documentation/avfaudio/avspeechsynthesisvoicegender/unspecified)
- [case male](/documentation/avfaudio/avspeechsynthesisvoicegender/male)
- [case female](/documentation/avfaudio/avspeechsynthesisvoicegender/female)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicegender/init(rawvalue:))
- [AVSpeechSynthesisVoice.Traits](/documentation/avfaudio/avspeechsynthesisvoice/traits)

##### Creating a voice trait

- [init(rawValue: UInt)](/documentation/avfaudio/avspeechsynthesisvoice/traits/init(rawvalue:))

##### Inspecting a voice trait

- [static var isNoveltyVoice: AVSpeechSynthesisVoice.Traits](/documentation/avfaudio/avspeechsynthesisvoice/traits/isnoveltyvoice)
- [static var isPersonalVoice: AVSpeechSynthesisVoice.Traits](/documentation/avfaudio/avspeechsynthesisvoice/traits/ispersonalvoice)

#### Working with language codes

- [class func currentLanguageCode() -> String](/documentation/avfaudio/avspeechsynthesisvoice/currentlanguagecode())
- [var language: String](/documentation/avfaudio/avspeechsynthesisvoice/language)

### Speech synthesis controls

- [AVSpeechSynthesizer](/documentation/avfaudio/avspeechsynthesizer)

#### Controlling speech

- [func speak(AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizer/speak(_:))
- [func continueSpeaking() -> Bool](/documentation/avfaudio/avspeechsynthesizer/continuespeaking())
- [func pauseSpeaking(at: AVSpeechBoundary) -> Bool](/documentation/avfaudio/avspeechsynthesizer/pausespeaking(at:))
- [func stopSpeaking(at: AVSpeechBoundary) -> Bool](/documentation/avfaudio/avspeechsynthesizer/stopspeaking(at:))
- [AVSpeechBoundary](/documentation/avfaudio/avspeechboundary)

##### Speech boundaries

- [case immediate](/documentation/avfaudio/avspeechboundary/immediate)
- [case word](/documentation/avfaudio/avspeechboundary/word)

##### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechboundary/init(rawvalue:))

#### Inspecting a speech synthesizer

- [var isSpeaking: Bool](/documentation/avfaudio/avspeechsynthesizer/isspeaking)
- [var isPaused: Bool](/documentation/avfaudio/avspeechsynthesizer/ispaused)

#### Managing the delegate

- [var delegate: (any AVSpeechSynthesizerDelegate)?](/documentation/avfaudio/avspeechsynthesizer/delegate)
- [AVSpeechSynthesizerDelegate](/documentation/avfaudio/avspeechsynthesizerdelegate)

##### Responding to speech synthesis events

- [func speechSynthesizer(AVSpeechSynthesizer, didStart: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:didstart:))
- [func speechSynthesizer(AVSpeechSynthesizer, willSpeakRangeOfSpeechString: NSRange, utterance: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:willspeakrangeofspeechstring:utterance:))
- [func speechSynthesizer(AVSpeechSynthesizer, willSpeak: AVSpeechSynthesisMarker, utterance: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:willspeak:utterance:))
- [func speechSynthesizer(AVSpeechSynthesizer, didPause: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:didpause:))
- [func speechSynthesizer(AVSpeechSynthesizer, didContinue: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:didcontinue:))
- [func speechSynthesizer(AVSpeechSynthesizer, didFinish: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:didfinish:))
- [func speechSynthesizer(AVSpeechSynthesizer, didCancel: AVSpeechUtterance)](/documentation/avfaudio/avspeechsynthesizerdelegate/speechsynthesizer(_:didcancel:))

#### Directing speech output

- [var usesApplicationAudioSession: Bool](/documentation/avfaudio/avspeechsynthesizer/usesapplicationaudiosession)
- [var mixToTelephonyUplink: Bool](/documentation/avfaudio/avspeechsynthesizer/mixtotelephonyuplink)
- [var outputChannels: [AVAudioSessionChannelDescription]?](/documentation/avfaudio/avspeechsynthesizer/outputchannels)
- [func write(AVSpeechUtterance, toBufferCallback: AVSpeechSynthesizer.BufferCallback)](/documentation/avfaudio/avspeechsynthesizer/write(_:tobuffercallback:))
- [AVSpeechSynthesizer.BufferCallback](/documentation/avfaudio/avspeechsynthesizer/buffercallback)
- [func write(AVSpeechUtterance, toBufferCallback: AVSpeechSynthesizer.BufferCallback, toMarkerCallback: AVSpeechSynthesizer.MarkerCallback)](/documentation/avfaudio/avspeechsynthesizer/write(_:tobuffercallback:tomarkercallback:))
- [AVSpeechSynthesizer.MarkerCallback](/documentation/avfaudio/avspeechsynthesizer/markercallback)

#### Enabling personal voices

- [class var personalVoiceAuthorizationStatus: AVSpeechSynthesizer.PersonalVoiceAuthorizationStatus](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.type.property)
- [class let availableVoicesDidChangeNotification: NSNotification.Name](/documentation/avfaudio/avspeechsynthesizer/availablevoicesdidchangenotification)
- [class func requestPersonalVoiceAuthorization(completionHandler: (AVSpeechSynthesizer.PersonalVoiceAuthorizationStatus) -> Void)](/documentation/avfaudio/avspeechsynthesizer/requestpersonalvoiceauthorization(completionhandler:))
- [AVSpeechSynthesizer.PersonalVoiceAuthorizationStatus](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum)

##### Authorization statuses

- [case authorized](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum/authorized)
- [case denied](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum/denied)
- [case notDetermined](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum/notdetermined)
- [case unsupported](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum/unsupported)

##### Initializers

- [init?(rawValue: UInt)](/documentation/avfaudio/avspeechsynthesizer/personalvoiceauthorizationstatus-swift.enum/init(rawvalue:))

### Speech synthesis audio unit

- [AVSpeechSynthesisProviderAudioUnit](/documentation/avfaudio/avspeechsynthesisprovideraudiounit)

#### Rendering speech

- [func synthesizeSpeechRequest(AVSpeechSynthesisProviderRequest)](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/synthesizespeechrequest(_:))
- [AVSpeechSynthesisProviderRequest](/documentation/avfaudio/avspeechsynthesisproviderrequest)

##### Creating a request

- [init(ssmlRepresentation: String, voice: AVSpeechSynthesisProviderVoice)](/documentation/avfaudio/avspeechsynthesisproviderrequest/init(ssmlrepresentation:voice:))

##### Inspecting a request

- [var ssmlRepresentation: String](/documentation/avfaudio/avspeechsynthesisproviderrequest/ssmlrepresentation)
- [var voice: AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisproviderrequest/voice)
- [AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisprovidervoice)

###### Creating a voice

- [init(name: String, identifier: String, primaryLanguages: [String], supportedLanguages: [String])](/documentation/avfaudio/avspeechsynthesisprovidervoice/init(name:identifier:primarylanguages:supportedlanguages:))

###### Inspecting a voice

- [var age: Int](/documentation/avfaudio/avspeechsynthesisprovidervoice/age)
- [var gender: AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisprovidervoice/gender)
- [AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoicegender)

###### Voice genders

- [case unspecified](/documentation/avfaudio/avspeechsynthesisvoicegender/unspecified)
- [case male](/documentation/avfaudio/avspeechsynthesisvoicegender/male)
- [case female](/documentation/avfaudio/avspeechsynthesisvoicegender/female)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicegender/init(rawvalue:))
- [var identifier: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/identifier)
- [var name: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/name)
- [var primaryLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/primarylanguages)
- [var supportedLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/supportedlanguages)
- [var version: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/version)
- [var voiceSize: Int64](/documentation/avfaudio/avspeechsynthesisprovidervoice/voicesize)

###### Updating a voice

- [class func updateSpeechVoices()](/documentation/avfaudio/avspeechsynthesisprovidervoice/updatespeechvoices())

#### Supplying metadata

- [AVSpeechSynthesisProviderOutputBlock](/documentation/avfaudio/avspeechsynthesisprovideroutputblock)
- [var speechSynthesisOutputMetadataBlock: AVSpeechSynthesisProviderOutputBlock?](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/speechsynthesisoutputmetadatablock)
- [AVSpeechSynthesisMarker](/documentation/avfaudio/avspeechsynthesismarker)

##### Creating a marker

- [init(markerType: AVSpeechSynthesisMarker.Mark, forTextRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(markertype:fortextrange:atbytesampleoffset:))
- [init(wordRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(wordrange:atbytesampleoffset:))
- [init(sentenceRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(sentencerange:atbytesampleoffset:))
- [init(paragraphRange: NSRange, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(paragraphrange:atbytesampleoffset:))
- [init(phonemeString: String, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(phonemestring:atbytesampleoffset:))
- [init(bookmarkName: String, atByteSampleOffset: Int)](/documentation/avfaudio/avspeechsynthesismarker/init(bookmarkname:atbytesampleoffset:))

##### Inspecting a marker

- [var mark: AVSpeechSynthesisMarker.Mark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.property)
- [var bookmarkName: String](/documentation/avfaudio/avspeechsynthesismarker/bookmarkname)
- [var phoneme: String](/documentation/avfaudio/avspeechsynthesismarker/phoneme)
- [var textRange: NSRange](/documentation/avfaudio/avspeechsynthesismarker/textrange)
- [var byteSampleOffset: Int](/documentation/avfaudio/avspeechsynthesismarker/bytesampleoffset)
- [AVSpeechSynthesisMarker.Mark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum)

###### Marks

- [case word](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/word)
- [case sentence](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/sentence)
- [case paragraph](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/paragraph)
- [case phoneme](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/phoneme)
- [case bookmark](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/bookmark)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesismarker/mark-swift.enum/init(rawvalue:))

#### Getting and setting voices

- [var speechVoices: [AVSpeechSynthesisProviderVoice]](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/speechvoices)
- [AVSpeechSynthesisProviderVoice](/documentation/avfaudio/avspeechsynthesisprovidervoice)

##### Creating a voice

- [init(name: String, identifier: String, primaryLanguages: [String], supportedLanguages: [String])](/documentation/avfaudio/avspeechsynthesisprovidervoice/init(name:identifier:primarylanguages:supportedlanguages:))

##### Inspecting a voice

- [var age: Int](/documentation/avfaudio/avspeechsynthesisprovidervoice/age)
- [var gender: AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisprovidervoice/gender)
- [AVSpeechSynthesisVoiceGender](/documentation/avfaudio/avspeechsynthesisvoicegender)

###### Voice genders

- [case unspecified](/documentation/avfaudio/avspeechsynthesisvoicegender/unspecified)
- [case male](/documentation/avfaudio/avspeechsynthesisvoicegender/male)
- [case female](/documentation/avfaudio/avspeechsynthesisvoicegender/female)

###### Initializers

- [init?(rawValue: Int)](/documentation/avfaudio/avspeechsynthesisvoicegender/init(rawvalue:))
- [var identifier: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/identifier)
- [var name: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/name)
- [var primaryLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/primarylanguages)
- [var supportedLanguages: [String]](/documentation/avfaudio/avspeechsynthesisprovidervoice/supportedlanguages)
- [var version: String](/documentation/avfaudio/avspeechsynthesisprovidervoice/version)
- [var voiceSize: Int64](/documentation/avfaudio/avspeechsynthesisprovidervoice/voicesize)

##### Updating a voice

- [class func updateSpeechVoices()](/documentation/avfaudio/avspeechsynthesisprovidervoice/updatespeechvoices())

#### Cancelling a request

- [func cancelSpeechRequest()](/documentation/avfaudio/avspeechsynthesisprovideraudiounit/cancelspeechrequest())

## Macros

- [Macros](/documentation/avfaudio/macros)

### Macros

- [var AVAUDIOENGINE_HAVE_AUAUDIOUNIT: Int32](/documentation/avfaudio/avaudioengine_have_auaudiounit)
- [var AVAUDIOENGINE_HAVE_MUSICPLAYER: Int32](/documentation/avfaudio/avaudioengine_have_musicplayer)
- [var AVAUDIOFORMAT_HAVE_CMFORMATDESCRIPTION: Int32](/documentation/avfaudio/avaudioformat_have_cmformatdescription)
- [var AVAUDIOIONODE_HAVE_AUDIOUNIT: Int32](/documentation/avfaudio/avaudioionode_have_audiounit)
- [var AVAUDIONODE_HAVE_AUAUDIOUNIT: Int32](/documentation/avfaudio/avaudionode_have_auaudiounit)
- [var AVAUDIOUNITCOMPONENT_HAVE_AUDIOCOMPONENT: Int32](/documentation/avfaudio/avaudiounitcomponent_have_audiocomponent)
- [var AVAUDIOUNIT_HAVE_AUDIOUNIT: Int32](/documentation/avfaudio/avaudiounit_have_audiounit)

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
