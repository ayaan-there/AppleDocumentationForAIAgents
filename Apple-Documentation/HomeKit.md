# HomeKit Documentation

Source: https://sosumi.ai/documentation/homekit

---
title: HomeKit
source: https://developer.apple.com/documentation/homekit
timestamp: 2026-02-13T18:57:48.750Z
---

## Essentials

- [Enabling HomeKit in your app](/documentation/homekit/enabling-homekit-in-your-app)
- [HomeKit Entitlement](/documentation/bundleresources/entitlements/com.apple.developer.homekit)
- [NSHomeKitUsageDescription](/documentation/bundleresources/information-property-list/nshomekitusagedescription)

## Home Manager

- [Configuring a home automation device](/documentation/homekit/configuring-a-home-automation-device)
- [Testing your app with the HomeKit Accessory Simulator](/documentation/homekit/testing-your-app-with-the-homekit-accessory-simulator)
- [HMHomeManager](/documentation/homekit/hmhomemanager)

### Inspecting authorization status

- [var authorizationStatus: HMHomeManagerAuthorizationStatus](/documentation/homekit/hmhomemanager/authorizationstatus)
- [HMHomeManagerAuthorizationStatus](/documentation/homekit/hmhomemanagerauthorizationstatus)

#### Recognizing Status Values

- [static var determined: HMHomeManagerAuthorizationStatus](/documentation/homekit/hmhomemanagerauthorizationstatus/determined)
- [static var authorized: HMHomeManagerAuthorizationStatus](/documentation/homekit/hmhomemanagerauthorizationstatus/authorized)
- [static var restricted: HMHomeManagerAuthorizationStatus](/documentation/homekit/hmhomemanagerauthorizationstatus/restricted)

#### Creating an Authorization Status

- [init(rawValue: UInt)](/documentation/homekit/hmhomemanagerauthorizationstatus/init(rawvalue:))

### Working with the home layout

- [var homes: [HMHome]](/documentation/homekit/hmhomemanager/homes)
- [HMHome](/documentation/homekit/hmhome)

#### Keeping track of home configuration changes

- [var delegate: (any HMHomeDelegate)?](/documentation/homekit/hmhome/delegate)
- [HMHomeDelegate](/documentation/homekit/hmhomedelegate)

##### Observing Home Configuration

- [func homeDidUpdateName(HMHome)](/documentation/homekit/hmhomedelegate/homedidupdatename(_:))
- [func home(HMHome, didAdd: HMAccessory)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-6jcl7)
- [func home(HMHome, didUpdate: HMRoom, for: HMAccessory)](/documentation/homekit/hmhomedelegate/home(_:didupdate:for:))
- [func home(HMHome, didRemove: HMAccessory)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-6plye)
- [func home(HMHome, didAdd: HMRoom)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-42aqd)
- [func home(HMHome, didUpdateNameFor: HMRoom)](/documentation/homekit/hmhomedelegate/home(_:didupdatenamefor:)-1a110)
- [func home(HMHome, didAdd: HMRoom, to: HMZone)](/documentation/homekit/hmhomedelegate/home(_:didadd:to:)-4hiew)
- [func home(HMHome, didRemove: HMRoom, from: HMZone)](/documentation/homekit/hmhomedelegate/home(_:didremove:from:)-8oz67)
- [func home(HMHome, didRemove: HMRoom)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-3if6s)
- [func home(HMHome, didAdd: HMZone)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-7vyoe)
- [func home(HMHome, didUpdateNameFor: HMZone)](/documentation/homekit/hmhomedelegate/home(_:didupdatenamefor:)-1k32g)
- [func home(HMHome, didRemove: HMZone)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-3o8ta)
- [func home(HMHome, didAdd: HMUser)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-8q7jm)
- [func home(HMHome, didRemove: HMUser)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-3fm38)
- [func homeDidUpdateAccessControl(forCurrentUser: HMHome)](/documentation/homekit/hmhomedelegate/homedidupdateaccesscontrol(forcurrentuser:))
- [func home(HMHome, didUpdate: HMHomeHubState)](/documentation/homekit/hmhomedelegate/home(_:didupdate:)-5fntk)
- [func homeDidUpdateSupportedFeatures(HMHome)](/documentation/homekit/hmhomedelegate/homedidupdatesupportedfeatures(_:))
- [HMHomeHubState](/documentation/homekit/hmhomehubstate)

###### Specifying the State

- [case connected](/documentation/homekit/hmhomehubstate/connected)
- [case disconnected](/documentation/homekit/hmhomehubstate/disconnected)
- [case notAvailable](/documentation/homekit/hmhomehubstate/notavailable)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmhomehubstate/init(rawvalue:))

##### Observing Service Configuration

- [func home(HMHome, didAdd: HMServiceGroup)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-3dymz)
- [func home(HMHome, didUpdateNameFor: HMServiceGroup)](/documentation/homekit/hmhomedelegate/home(_:didupdatenamefor:)-4tam1)
- [func home(HMHome, didAdd: HMService, to: HMServiceGroup)](/documentation/homekit/hmhomedelegate/home(_:didadd:to:)-6xdgy)
- [func home(HMHome, didRemove: HMService, from: HMServiceGroup)](/documentation/homekit/hmhomedelegate/home(_:didremove:from:)-9yzp0)
- [func home(HMHome, didRemove: HMServiceGroup)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-6kqxo)

##### Observing Action and Trigger Configuration

- [func home(HMHome, didAdd: HMActionSet)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-9dcki)
- [func home(HMHome, didUpdateNameFor: HMActionSet)](/documentation/homekit/hmhomedelegate/home(_:didupdatenamefor:)-7fxvl)
- [func home(HMHome, didUpdateActionsFor: HMActionSet)](/documentation/homekit/hmhomedelegate/home(_:didupdateactionsfor:))
- [func home(HMHome, didRemove: HMActionSet)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-80ewx)
- [func home(HMHome, didAdd: HMTrigger)](/documentation/homekit/hmhomedelegate/home(_:didadd:)-64yxx)
- [func home(HMHome, didUpdateNameFor: HMTrigger)](/documentation/homekit/hmhomedelegate/home(_:didupdatenamefor:)-8vn79)
- [func home(HMHome, didUpdate: HMTrigger)](/documentation/homekit/hmhomedelegate/home(_:didupdate:)-3l4r1)
- [func home(HMHome, didRemove: HMTrigger)](/documentation/homekit/hmhomedelegate/home(_:didremove:)-4ujfa)

##### Observing Accessories

- [func home(HMHome, didEncounterError: any Error, for: HMAccessory)](/documentation/homekit/hmhomedelegate/home(_:didencountererror:for:))
- [func home(HMHome, didUnblockAccessory: HMAccessory)](/documentation/homekit/hmhomedelegate/home(_:didunblockaccessory:))

#### Identifying a home

- [var name: String](/documentation/homekit/hmhome/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmhome/uniqueidentifier)
- [var isPrimary: Bool](/documentation/homekit/hmhome/isprimary)

#### Dividing a house into rooms

- [var rooms: [HMRoom]](/documentation/homekit/hmhome/rooms)
- [func roomForEntireHome() -> HMRoom](/documentation/homekit/hmhome/roomforentirehome())
- [func addRoom(withName: String, completionHandler: (HMRoom?, (any Error)?) -> Void)](/documentation/homekit/hmhome/addroom(withname:completionhandler:))
- [func removeRoom(HMRoom, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removeroom(_:completionhandler:))
- [HMRoom](/documentation/homekit/hmroom)

##### Identifying a room

- [var name: String](/documentation/homekit/hmroom/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmroom/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmroom/uniqueidentifier)

##### Finding accessories

- [var accessories: [HMAccessory]](/documentation/homekit/hmroom/accessories)

#### Grouping rooms into zones

- [var zones: [HMZone]](/documentation/homekit/hmhome/zones)
- [func addZone(withName: String, completionHandler: (HMZone?, (any Error)?) -> Void)](/documentation/homekit/hmhome/addzone(withname:completionhandler:))
- [func removeZone(HMZone, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removezone(_:completionhandler:))
- [HMZone](/documentation/homekit/hmzone)

##### Identifying a Zone

- [var name: String](/documentation/homekit/hmzone/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmzone/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmzone/uniqueidentifier)

##### Assigning Rooms to a Zone

- [var rooms: [HMRoom]](/documentation/homekit/hmzone/rooms)
- [func addRoom(HMRoom, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmzone/addroom(_:completionhandler:))
- [func removeRoom(HMRoom, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmzone/removeroom(_:completionhandler:))

#### Managing accessories

- [var accessories: [HMAccessory]](/documentation/homekit/hmhome/accessories)
- [func addAndSetupAccessories(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/addandsetupaccessories(completionhandler:))
- [func addAndSetupAccessories(with: HMAccessorySetupPayload, completionHandler: ([HMAccessory]?, (any Error)?) -> Void)](/documentation/homekit/hmhome/addandsetupaccessories(with:completionhandler:))

##### Defining the Setup Payload

- [HMAccessorySetupPayload](/documentation/homekit/hmaccessorysetuppayload)

###### Creating a Payload

- [init?(url: URL?)](/documentation/homekit/hmaccessorysetuppayload/init(url:))
- [init?(url: URL, ownershipToken: HMAccessoryOwnershipToken?)](/documentation/homekit/hmaccessorysetuppayload/init(url:ownershiptoken:))
- [HMAccessoryOwnershipToken](/documentation/homekit/hmaccessoryownershiptoken)

###### Creating a Token

- [init?(data: Data)](/documentation/homekit/hmaccessoryownershiptoken/init(data:))
- [func addAccessory(HMAccessory, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/addaccessory(_:completionhandler:))
- [func assignAccessory(HMAccessory, to: HMRoom, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/assignaccessory(_:to:completionhandler:))
- [func removeAccessory(HMAccessory, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removeaccessory(_:completionhandler:))
- [var supportsAddingNetworkRouter: Bool](/documentation/homekit/hmhome/supportsaddingnetworkrouter)
- [func unblockAccessory(HMAccessory, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/unblockaccessory(_:completionhandler:))
- [HMAccessory](/documentation/homekit/hmaccessory)

##### Tracking changes to an accessory

- [var delegate: (any HMAccessoryDelegate)?](/documentation/homekit/hmaccessory/delegate)
- [HMAccessoryDelegate](/documentation/homekit/hmaccessorydelegate)

###### Observing accessories

- [func accessoryDidUpdateName(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdatename(_:))
- [func accessoryDidUpdateReachability(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdatereachability(_:))
- [func accessoryDidUpdateServices(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdateservices(_:))
- [func accessory(HMAccessory, didUpdateNameFor: HMService)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdatenamefor:))
- [func accessory(HMAccessory, service: HMService, didUpdateValueFor: HMCharacteristic)](/documentation/homekit/hmaccessorydelegate/accessory(_:service:didupdatevaluefor:))
- [func accessory(HMAccessory, didUpdateAssociatedServiceTypeFor: HMService)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdateassociatedservicetypefor:))
- [func accessory(HMAccessory, didAdd: HMAccessoryProfile)](/documentation/homekit/hmaccessorydelegate/accessory(_:didadd:))
- [func accessory(HMAccessory, didRemove: HMAccessoryProfile)](/documentation/homekit/hmaccessorydelegate/accessory(_:didremove:))
- [func accessory(HMAccessory, didUpdateFirmwareVersion: String)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdatefirmwareversion:))

##### Identifying an Accessory

- [var name: String](/documentation/homekit/hmaccessory/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmaccessory/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmaccessory/uniqueidentifier)
- [var identifier: UUID](/documentation/homekit/hmaccessory/identifier)

##### Categorizing an accessory

- [var category: HMAccessoryCategory](/documentation/homekit/hmaccessory/category)
- [HMAccessoryCategory](/documentation/homekit/hmaccessorycategory)

###### Reading the category type

- [var categoryType: String](/documentation/homekit/hmaccessorycategory/categorytype)
- [Accessory Category Types](/documentation/homekit/accessory-category-types)

###### Light

- [let HMAccessoryCategoryTypeLightbulb: String](/documentation/homekit/hmaccessorycategorytypelightbulb)

###### Power and switches

- [let HMAccessoryCategoryTypeOutlet: String](/documentation/homekit/hmaccessorycategorytypeoutlet)
- [let HMAccessoryCategoryTypeProgrammableSwitch: String](/documentation/homekit/hmaccessorycategorytypeprogrammableswitch)
- [let HMAccessoryCategoryTypeSwitch: String](/documentation/homekit/hmaccessorycategorytypeswitch)

###### Air quality and smoke detection

- [let HMAccessoryCategoryTypeFan: String](/documentation/homekit/hmaccessorycategorytypefan)
- [let HMAccessoryCategoryTypeAirPurifier: String](/documentation/homekit/hmaccessorycategorytypeairpurifier)

###### Temperature and humidity

- [let HMAccessoryCategoryTypeThermostat: String](/documentation/homekit/hmaccessorycategorytypethermostat)
- [let HMAccessoryCategoryTypeAirConditioner: String](/documentation/homekit/hmaccessorycategorytypeairconditioner)
- [let HMAccessoryCategoryTypeAirDehumidifier: String](/documentation/homekit/hmaccessorycategorytypeairdehumidifier)
- [let HMAccessoryCategoryTypeAirHeater: String](/documentation/homekit/hmaccessorycategorytypeairheater)
- [let HMAccessoryCategoryTypeAirHumidifier: String](/documentation/homekit/hmaccessorycategorytypeairhumidifier)

###### Windows

- [let HMAccessoryCategoryTypeWindow: String](/documentation/homekit/hmaccessorycategorytypewindow)
- [let HMAccessoryCategoryTypeWindowCovering: String](/documentation/homekit/hmaccessorycategorytypewindowcovering)

###### Locks and openers

- [let HMAccessoryCategoryTypeDoor: String](/documentation/homekit/hmaccessorycategorytypedoor)
- [let HMAccessoryCategoryTypeDoorLock: String](/documentation/homekit/hmaccessorycategorytypedoorlock)
- [let HMAccessoryCategoryTypeGarageDoorOpener: String](/documentation/homekit/hmaccessorycategorytypegaragedooropener)
- [let HMAccessoryCategoryTypeVideoDoorbell: String](/documentation/homekit/hmaccessorycategorytypevideodoorbell)

###### Safety and security

- [let HMAccessoryCategoryTypeSensor: String](/documentation/homekit/hmaccessorycategorytypesensor)
- [let HMAccessoryCategoryTypeSecuritySystem: String](/documentation/homekit/hmaccessorycategorytypesecuritysystem)

###### Cameras

- [let HMAccessoryCategoryTypeIPCamera: String](/documentation/homekit/hmaccessorycategorytypeipcamera)

###### Water

- [let HMAccessoryCategoryTypeSprinkler: String](/documentation/homekit/hmaccessorycategorytypesprinkler)
- [let HMAccessoryCategoryTypeFaucet: String](/documentation/homekit/hmaccessorycategorytypefaucet)
- [let HMAccessoryCategoryTypeShowerHead: String](/documentation/homekit/hmaccessorycategorytypeshowerhead)

###### Network

- [let HMAccessoryCategoryTypeBridge: String](/documentation/homekit/hmaccessorycategorytypebridge)
- [let HMAccessoryCategoryTypeRangeExtender: String](/documentation/homekit/hmaccessorycategorytyperangeextender)
- [let HMAccessoryCategoryTypeAirPort: String](/documentation/homekit/hmaccessorycategorytypeairport)
- [let HMAccessoryCategoryTypeWiFiRouter: String](/documentation/homekit/hmaccessorycategorytypewifirouter)

###### Audio and sound

- [let HMAccessoryCategoryTypeAudioReceiver: String](/documentation/homekit/hmaccessorycategorytypeaudioreceiver)
- [let HMAccessoryCategoryTypeSpeaker: String](/documentation/homekit/hmaccessorycategorytypespeaker)

###### Television

- [let HMAccessoryCategoryTypeTelevision: String](/documentation/homekit/hmaccessorycategorytypetelevision)
- [let HMAccessoryCategoryTypeTelevisionSetTopBox: String](/documentation/homekit/hmaccessorycategorytypetelevisionsettopbox)
- [let HMAccessoryCategoryTypeTelevisionStreamingStick: String](/documentation/homekit/hmaccessorycategorytypetelevisionstreamingstick)

###### Uncategorized

- [let HMAccessoryCategoryTypeOther: String](/documentation/homekit/hmaccessorycategorytypeother)

###### Describing the category

- [var localizedDescription: String](/documentation/homekit/hmaccessorycategory/localizeddescription)

##### Locating an accessory

- [var room: HMRoom?](/documentation/homekit/hmaccessory/room)
- [HMRoom](/documentation/homekit/hmroom)

###### Identifying a room

- [var name: String](/documentation/homekit/hmroom/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmroom/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmroom/uniqueidentifier)

###### Finding accessories

- [var accessories: [HMAccessory]](/documentation/homekit/hmroom/accessories)

##### Managing accessory profiles

- [var profiles: [HMAccessoryProfile]](/documentation/homekit/hmaccessory/profiles)
- [HMAccessoryProfile](/documentation/homekit/hmaccessoryprofile)

###### Getting information about a profile

- [var accessory: HMAccessory?](/documentation/homekit/hmaccessoryprofile/accessory)
- [var services: [HMService]](/documentation/homekit/hmaccessoryprofile/services)
- [var uniqueIdentifier: UUID](/documentation/homekit/hmaccessoryprofile/uniqueidentifier)
- [HMNetworkConfigurationProfile](/documentation/homekit/hmnetworkconfigurationprofile)

###### Restricting network access

- [var isNetworkAccessRestricted: Bool](/documentation/homekit/hmnetworkconfigurationprofile/isnetworkaccessrestricted)

###### Listening for access changes

- [var delegate: (any HMNetworkConfigurationProfileDelegate)?](/documentation/homekit/hmnetworkconfigurationprofile/delegate)
- [HMNetworkConfigurationProfileDelegate](/documentation/homekit/hmnetworkconfigurationprofiledelegate)

###### Observing network access changes

- [func profileDidUpdateNetworkAccessMode(HMNetworkConfigurationProfile)](/documentation/homekit/hmnetworkconfigurationprofiledelegate/profiledidupdatenetworkaccessmode(_:))
- [HMCameraProfile](/documentation/homekit/hmcameraprofile)

###### Controlling camera settings

- [var settingsControl: HMCameraSettingsControl?](/documentation/homekit/hmcameraprofile/settingscontrol)
- [HMCameraSettingsControl](/documentation/homekit/hmcamerasettingscontrol)

###### Controlling camera characteristics

- [var currentHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currenthorizontaltilt)
- [var targetHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targethorizontaltilt)
- [var currentVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currentverticaltilt)
- [var targetVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targetverticaltilt)
- [var opticalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/opticalzoom)
- [var digitalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/digitalzoom)
- [var imageMirroring: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagemirroring)
- [var imageRotation: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagerotation)
- [var nightVision: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/nightvision)
- [HMCameraControl](/documentation/homekit/hmcameracontrol)

###### Initializers

- [init()](/documentation/homekit/hmcameracontrol/init())

###### Playing audio

- [var microphoneControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/microphonecontrol)
- [var speakerControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/speakercontrol)
- [HMCameraAudioControl](/documentation/homekit/hmcameraaudiocontrol)

###### Controlling audio characteristics

- [var mute: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/mute)
- [var volume: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/volume)

###### Streaming

- [var streamControl: HMCameraStreamControl?](/documentation/homekit/hmcameraprofile/streamcontrol)
- [HMCameraStreamControl](/documentation/homekit/hmcamerastreamcontrol)

###### Controlling the stream

- [func startStream()](/documentation/homekit/hmcamerastreamcontrol/startstream())
- [func stopStream()](/documentation/homekit/hmcamerastreamcontrol/stopstream())
- [var cameraStream: HMCameraStream?](/documentation/homekit/hmcamerastreamcontrol/camerastream)
- [HMCameraStream](/documentation/homekit/hmcamerastream)

###### Configuring the audio stream

- [var audioStreamSetting: HMCameraAudioStreamSetting](/documentation/homekit/hmcamerastream/audiostreamsetting)
- [func updateAudioStreamSetting(HMCameraAudioStreamSetting, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcamerastream/updateaudiostreamsetting(_:completionhandler:))
- [func setAudioStreamSetting(HMCameraAudioStreamSetting)](/documentation/homekit/hmcamerastream/setaudiostreamsetting(_:))
- [HMCameraAudioStreamSetting](/documentation/homekit/hmcameraaudiostreamsetting)

###### Configuring the Audio Stream

- [case muted](/documentation/homekit/hmcameraaudiostreamsetting/muted)
- [case incomingAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/incomingaudioallowed)
- [case bidirectionalAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/bidirectionalaudioallowed)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcameraaudiostreamsetting/init(rawvalue:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastream/init())
- [var streamState: HMCameraStreamState](/documentation/homekit/hmcamerastreamcontrol/streamstate)
- [HMCameraStreamState](/documentation/homekit/hmcamerastreamstate)

###### Observing the streaming state

- [case notStreaming](/documentation/homekit/hmcamerastreamstate/notstreaming)
- [case starting](/documentation/homekit/hmcamerastreamstate/starting)
- [case stopping](/documentation/homekit/hmcamerastreamstate/stopping)
- [case streaming](/documentation/homekit/hmcamerastreamstate/streaming)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcamerastreamstate/init(rawvalue:))

###### Observing stream activity

- [var delegate: (any HMCameraStreamControlDelegate)?](/documentation/homekit/hmcamerastreamcontrol/delegate)
- [HMCameraStreamControlDelegate](/documentation/homekit/hmcamerastreamcontroldelegate)

###### Observing stream activity

- [func cameraStreamControlDidStartStream(HMCameraStreamControl)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontroldidstartstream(_:))
- [func cameraStreamControl(HMCameraStreamControl, didStopStreamWithError: (any Error)?)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontrol(_:didstopstreamwitherror:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastreamcontrol/init())

###### Capturing snapshots

- [var snapshotControl: HMCameraSnapshotControl?](/documentation/homekit/hmcameraprofile/snapshotcontrol)
- [HMCameraSnapshotControl](/documentation/homekit/hmcamerasnapshotcontrol)

###### Taking snapshots

- [func takeSnapshot()](/documentation/homekit/hmcamerasnapshotcontrol/takesnapshot())
- [var mostRecentSnapshot: HMCameraSnapshot?](/documentation/homekit/hmcamerasnapshotcontrol/mostrecentsnapshot)
- [HMCameraSnapshot](/documentation/homekit/hmcamerasnapshot)

###### Accessing snapshot properties

- [var captureDate: Date](/documentation/homekit/hmcamerasnapshot/capturedate)

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshot/init())

###### Observing snapshot activity

- [var delegate: (any HMCameraSnapshotControlDelegate)?](/documentation/homekit/hmcamerasnapshotcontrol/delegate)
- [HMCameraSnapshotControlDelegate](/documentation/homekit/hmcamerasnapshotcontroldelegate)

###### Observing snapshot activity

- [func cameraSnapshotControl(HMCameraSnapshotControl, didTake: HMCameraSnapshot?, error: (any Error)?)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontrol(_:didtake:error:))
- [func cameraSnapshotControlDidUpdateMostRecentSnapshot(HMCameraSnapshotControl)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontroldidupdatemostrecentsnapshot(_:))

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshotcontrol/init())

##### Managing camera profiles

- [CameraView](/documentation/homekit/cameraview)

###### Creating a camera view

- [init(source: HMCameraSource)](/documentation/homekit/cameraview/init(source:))
- [HMCameraSource](/documentation/homekit/hmcamerasource)

###### Getting the properties

- [var aspectRatio: Double](/documentation/homekit/hmcamerasource/aspectratio)

###### Initializers

- [init()](/documentation/homekit/hmcamerasource/init())
- [var cameraProfiles: [HMCameraProfile]?](/documentation/homekit/hmaccessory/cameraprofiles)
- [HMCameraProfile](/documentation/homekit/hmcameraprofile)

###### Controlling camera settings

- [var settingsControl: HMCameraSettingsControl?](/documentation/homekit/hmcameraprofile/settingscontrol)
- [HMCameraSettingsControl](/documentation/homekit/hmcamerasettingscontrol)

###### Controlling camera characteristics

- [var currentHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currenthorizontaltilt)
- [var targetHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targethorizontaltilt)
- [var currentVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currentverticaltilt)
- [var targetVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targetverticaltilt)
- [var opticalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/opticalzoom)
- [var digitalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/digitalzoom)
- [var imageMirroring: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagemirroring)
- [var imageRotation: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagerotation)
- [var nightVision: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/nightvision)
- [HMCameraControl](/documentation/homekit/hmcameracontrol)

###### Initializers

- [init()](/documentation/homekit/hmcameracontrol/init())

###### Playing audio

- [var microphoneControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/microphonecontrol)
- [var speakerControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/speakercontrol)
- [HMCameraAudioControl](/documentation/homekit/hmcameraaudiocontrol)

###### Controlling audio characteristics

- [var mute: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/mute)
- [var volume: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/volume)

###### Streaming

- [var streamControl: HMCameraStreamControl?](/documentation/homekit/hmcameraprofile/streamcontrol)
- [HMCameraStreamControl](/documentation/homekit/hmcamerastreamcontrol)

###### Controlling the stream

- [func startStream()](/documentation/homekit/hmcamerastreamcontrol/startstream())
- [func stopStream()](/documentation/homekit/hmcamerastreamcontrol/stopstream())
- [var cameraStream: HMCameraStream?](/documentation/homekit/hmcamerastreamcontrol/camerastream)
- [HMCameraStream](/documentation/homekit/hmcamerastream)

###### Configuring the audio stream

- [var audioStreamSetting: HMCameraAudioStreamSetting](/documentation/homekit/hmcamerastream/audiostreamsetting)
- [func updateAudioStreamSetting(HMCameraAudioStreamSetting, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcamerastream/updateaudiostreamsetting(_:completionhandler:))
- [func setAudioStreamSetting(HMCameraAudioStreamSetting)](/documentation/homekit/hmcamerastream/setaudiostreamsetting(_:))
- [HMCameraAudioStreamSetting](/documentation/homekit/hmcameraaudiostreamsetting)

###### Configuring the Audio Stream

- [case muted](/documentation/homekit/hmcameraaudiostreamsetting/muted)
- [case incomingAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/incomingaudioallowed)
- [case bidirectionalAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/bidirectionalaudioallowed)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcameraaudiostreamsetting/init(rawvalue:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastream/init())
- [var streamState: HMCameraStreamState](/documentation/homekit/hmcamerastreamcontrol/streamstate)
- [HMCameraStreamState](/documentation/homekit/hmcamerastreamstate)

###### Observing the streaming state

- [case notStreaming](/documentation/homekit/hmcamerastreamstate/notstreaming)
- [case starting](/documentation/homekit/hmcamerastreamstate/starting)
- [case stopping](/documentation/homekit/hmcamerastreamstate/stopping)
- [case streaming](/documentation/homekit/hmcamerastreamstate/streaming)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcamerastreamstate/init(rawvalue:))

###### Observing stream activity

- [var delegate: (any HMCameraStreamControlDelegate)?](/documentation/homekit/hmcamerastreamcontrol/delegate)
- [HMCameraStreamControlDelegate](/documentation/homekit/hmcamerastreamcontroldelegate)

###### Observing stream activity

- [func cameraStreamControlDidStartStream(HMCameraStreamControl)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontroldidstartstream(_:))
- [func cameraStreamControl(HMCameraStreamControl, didStopStreamWithError: (any Error)?)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontrol(_:didstopstreamwitherror:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastreamcontrol/init())

###### Capturing snapshots

- [var snapshotControl: HMCameraSnapshotControl?](/documentation/homekit/hmcameraprofile/snapshotcontrol)
- [HMCameraSnapshotControl](/documentation/homekit/hmcamerasnapshotcontrol)

###### Taking snapshots

- [func takeSnapshot()](/documentation/homekit/hmcamerasnapshotcontrol/takesnapshot())
- [var mostRecentSnapshot: HMCameraSnapshot?](/documentation/homekit/hmcamerasnapshotcontrol/mostrecentsnapshot)
- [HMCameraSnapshot](/documentation/homekit/hmcamerasnapshot)

###### Accessing snapshot properties

- [var captureDate: Date](/documentation/homekit/hmcamerasnapshot/capturedate)

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshot/init())

###### Observing snapshot activity

- [var delegate: (any HMCameraSnapshotControlDelegate)?](/documentation/homekit/hmcamerasnapshotcontrol/delegate)
- [HMCameraSnapshotControlDelegate](/documentation/homekit/hmcamerasnapshotcontroldelegate)

###### Observing snapshot activity

- [func cameraSnapshotControl(HMCameraSnapshotControl, didTake: HMCameraSnapshot?, error: (any Error)?)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontrol(_:didtake:error:))
- [func cameraSnapshotControlDidUpdateMostRecentSnapshot(HMCameraSnapshotControl)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontroldidupdatemostrecentsnapshot(_:))

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshotcontrol/init())
- [HMCameraView](/documentation/homekit/hmcameraview)

###### Getting the Camera Source

- [var cameraSource: HMCameraSource?](/documentation/homekit/hmcameraview/camerasource)
- [HMCameraSource](/documentation/homekit/hmcamerasource)

###### Getting the properties

- [var aspectRatio: Double](/documentation/homekit/hmcamerasource/aspectratio)

###### Initializers

- [init()](/documentation/homekit/hmcamerasource/init())

###### Initializers

- [init()](/documentation/homekit/hmcameraview/init())

##### Getting accessory state

- [var isReachable: Bool](/documentation/homekit/hmaccessory/isreachable)
- [var isBlocked: Bool](/documentation/homekit/hmaccessory/isblocked)

##### Asking an accessory to identify itself

- [var supportsIdentify: Bool](/documentation/homekit/hmaccessory/supportsidentify)
- [func identify(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmaccessory/identify(completionhandler:))

##### Controlling accessory features

- [var services: [HMService]](/documentation/homekit/hmaccessory/services)
- [HMService](/documentation/homekit/hmservice)

###### Getting service characteristics

- [var characteristics: [HMCharacteristic]](/documentation/homekit/hmservice/characteristics)
- [HMCharacteristic](/documentation/homekit/hmcharacteristic)

###### Identifying a characteristic

- [var uniqueIdentifier: UUID](/documentation/homekit/hmcharacteristic/uniqueidentifier)
- [var localizedDescription: String](/documentation/homekit/hmcharacteristic/localizeddescription)

###### Reading characteristic properties

- [var properties: [String]](/documentation/homekit/hmcharacteristic/properties)
- [Characteristic Properties](/documentation/homekit/characteristic-properties)

###### Properties of Characteristics

- [let HMCharacteristicPropertyReadable: String](/documentation/homekit/hmcharacteristicpropertyreadable)
- [let HMCharacteristicPropertyWritable: String](/documentation/homekit/hmcharacteristicpropertywritable)
- [let HMCharacteristicPropertyHidden: String](/documentation/homekit/hmcharacteristicpropertyhidden)

###### Determining what a characteristic controls

- [var characteristicType: String](/documentation/homekit/hmcharacteristic/characteristictype)
- [Characteristic types](/documentation/homekit/characteristic-types)

###### Light

- [let HMCharacteristicTypeCurrentLightLevel: String](/documentation/homekit/hmcharacteristictypecurrentlightlevel)
- [let HMCharacteristicTypeHue: String](/documentation/homekit/hmcharacteristictypehue)
- [let HMCharacteristicTypeBrightness: String](/documentation/homekit/hmcharacteristictypebrightness)
- [let HMCharacteristicTypeSaturation: String](/documentation/homekit/hmcharacteristictypesaturation)
- [let HMCharacteristicTypeColorTemperature: String](/documentation/homekit/hmcharacteristictypecolortemperature)

###### Power and switches

- [let HMCharacteristicTypeBatteryLevel: String](/documentation/homekit/hmcharacteristictypebatterylevel)
- [let HMCharacteristicTypeChargingState: String](/documentation/homekit/hmcharacteristictypechargingstate)

###### Values

- [HMCharacteristicValueChargingState](/documentation/homekit/hmcharacteristicvaluechargingstate)

###### Charging States

- [case none](/documentation/homekit/hmcharacteristicvaluechargingstate/none)
- [case inProgress](/documentation/homekit/hmcharacteristicvaluechargingstate/inprogress)
- [case notChargeable](/documentation/homekit/hmcharacteristicvaluechargingstate/notchargeable)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluechargingstate/init(rawvalue:))
- [let HMCharacteristicTypeContactState: String](/documentation/homekit/hmcharacteristictypecontactstate)

###### Values

- [HMCharacteristicValueContactState](/documentation/homekit/hmcharacteristicvaluecontactstate)

###### Contact Sensor State

- [case detected](/documentation/homekit/hmcharacteristicvaluecontactstate/detected)
- [case none](/documentation/homekit/hmcharacteristicvaluecontactstate/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecontactstate/init(rawvalue:))
- [let HMCharacteristicTypeOutletInUse: String](/documentation/homekit/hmcharacteristictypeoutletinuse)
- [let HMCharacteristicTypePowerState: String](/documentation/homekit/hmcharacteristictypepowerstate)
- [let HMCharacteristicTypeStatusLowBattery: String](/documentation/homekit/hmcharacteristictypestatuslowbattery)

###### Values

- [HMCharacteristicValueBatteryStatus](/documentation/homekit/hmcharacteristicvaluebatterystatus)

###### Battery Status

- [case normal](/documentation/homekit/hmcharacteristicvaluebatterystatus/normal)
- [case low](/documentation/homekit/hmcharacteristicvaluebatterystatus/low)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluebatterystatus/init(rawvalue:))
- [let HMCharacteristicTypeOutputState: String](/documentation/homekit/hmcharacteristictypeoutputstate)
- [let HMCharacteristicTypeInputEvent: String](/documentation/homekit/hmcharacteristictypeinputevent)

###### Values

- [HMCharacteristicValueInputEvent](/documentation/homekit/hmcharacteristicvalueinputevent)

###### Input Events

- [case singlePress](/documentation/homekit/hmcharacteristicvalueinputevent/singlepress)
- [case doublePress](/documentation/homekit/hmcharacteristicvalueinputevent/doublepress)
- [case longPress](/documentation/homekit/hmcharacteristicvalueinputevent/longpress)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputevent/init(rawvalue:))
- [let HMCharacteristicTypePowerModeSelection: String](/documentation/homekit/hmcharacteristictypepowermodeselection)

###### Values

- [HMCharacteristicValuePowerModeSelection](/documentation/homekit/hmcharacteristicvaluepowermodeselection)

###### Power mode status

- [case hide](/documentation/homekit/hmcharacteristicvaluepowermodeselection/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluepowermodeselection/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepowermodeselection/init(rawvalue:))

###### Temperature

- [let HMCharacteristicTypeCurrentTemperature: String](/documentation/homekit/hmcharacteristictypecurrenttemperature)
- [let HMCharacteristicTypeTargetTemperature: String](/documentation/homekit/hmcharacteristictypetargettemperature)
- [let HMCharacteristicTypeTemperatureUnits: String](/documentation/homekit/hmcharacteristictypetemperatureunits)

###### Values

- [HMCharacteristicValueTemperatureUnit](/documentation/homekit/hmcharacteristicvaluetemperatureunit)

###### Temperature Units

- [case celsius](/documentation/homekit/hmcharacteristicvaluetemperatureunit/celsius)
- [case fahrenheit](/documentation/homekit/hmcharacteristicvaluetemperatureunit/fahrenheit)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetemperatureunit/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeatingCooling: String](/documentation/homekit/hmcharacteristictypetargetheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeatingCooling: String](/documentation/homekit/hmcharacteristictypecurrentheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [HMCharacteristicValueCurrentHeatingCooling](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling)

###### Temperature States

- [case cool](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/cool)
- [case heat](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/heat)
- [case off](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/off)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypetargetheatercoolerstate)

###### Values

- [HMCharacteristicValueTargetHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate)

###### Target State

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/automatic)
- [case heat](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/heat)
- [case cool](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/cool)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypecurrentheatercoolerstate)

###### Values

- [HMCharacteristicValueCurrentHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate)

###### Current State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/idle)
- [case heating](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/heating)
- [case cooling](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/cooling)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCoolingThreshold: String](/documentation/homekit/hmcharacteristictypecoolingthreshold)
- [let HMCharacteristicTypeHeatingThreshold: String](/documentation/homekit/hmcharacteristictypeheatingthreshold)

###### Humidity

- [let HMCharacteristicTypeCurrentRelativeHumidity: String](/documentation/homekit/hmcharacteristictypecurrentrelativehumidity)
- [let HMCharacteristicTypeTargetRelativeHumidity: String](/documentation/homekit/hmcharacteristictypetargetrelativehumidity)
- [let HMCharacteristicTypeCurrentHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypecurrenthumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueCurrentHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate)

###### Current States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/idle)
- [case humidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/humidifying)
- [case dehumidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/dehumidifying)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypetargethumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueTargetHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate)

###### Target States

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/automatic)
- [case humidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/humidify)
- [case dehumidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/dehumidify)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeHumidifierThreshold: String](/documentation/homekit/hmcharacteristictypehumidifierthreshold)
- [let HMCharacteristicTypeDehumidifierThreshold: String](/documentation/homekit/hmcharacteristictypedehumidifierthreshold)

###### Air quality and smoke detection

- [let HMCharacteristicTypeAirQuality: String](/documentation/homekit/hmcharacteristictypeairquality)

###### Values

- [HMCharacteristicValueAirQuality](/documentation/homekit/hmcharacteristicvalueairquality)

###### Air Quality

- [case unknown](/documentation/homekit/hmcharacteristicvalueairquality/unknown)
- [case excellent](/documentation/homekit/hmcharacteristicvalueairquality/excellent)
- [case good](/documentation/homekit/hmcharacteristicvalueairquality/good)
- [case fair](/documentation/homekit/hmcharacteristicvalueairquality/fair)
- [case inferior](/documentation/homekit/hmcharacteristicvalueairquality/inferior)
- [case poor](/documentation/homekit/hmcharacteristicvalueairquality/poor)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairquality/init(rawvalue:))
- [let HMCharacteristicTypeAirParticulateDensity: String](/documentation/homekit/hmcharacteristictypeairparticulatedensity)
- [let HMCharacteristicTypeAirParticulateSize: String](/documentation/homekit/hmcharacteristictypeairparticulatesize)

###### Values

- [HMCharacteristicValueAirParticulateSize](/documentation/homekit/hmcharacteristicvalueairparticulatesize)

###### Air Particulate Sizes

- [case size2_5](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size2_5)
- [case size10](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size10)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairparticulatesize/init(rawvalue:))
- [let HMCharacteristicTypeSmokeDetected: String](/documentation/homekit/hmcharacteristictypesmokedetected)

###### Values

- [HMCharacteristicValueSmokeDetectionStatus](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus)

###### Smoke Detection Status

- [case none](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideDetected: String](/documentation/homekit/hmcharacteristictypecarbondioxidedetected)

###### Values

- [HMCharacteristicValueCarbonDioxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus)

###### Carbon Dioxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidelevel)
- [let HMCharacteristicTypeCarbonDioxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidepeaklevel)
- [let HMCharacteristicTypeCarbonMonoxideDetected: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidedetected)

###### Values

- [HMCharacteristicValueCarbonMonoxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus)

###### Carbon Monoxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonMonoxideLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidelevel)
- [let HMCharacteristicTypeCarbonMonoxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidepeaklevel)
- [let HMCharacteristicTypeNitrogenDioxideDensity: String](/documentation/homekit/hmcharacteristictypenitrogendioxidedensity)
- [let HMCharacteristicTypeOzoneDensity: String](/documentation/homekit/hmcharacteristictypeozonedensity)
- [let HMCharacteristicTypePM10Density: String](/documentation/homekit/hmcharacteristictypepm10density)
- [let HMCharacteristicTypePM2_5Density: String](/documentation/homekit/hmcharacteristictypepm2_5density)
- [let HMCharacteristicTypeSulphurDioxideDensity: String](/documentation/homekit/hmcharacteristictypesulphurdioxidedensity)
- [let HMCharacteristicTypeVolatileOrganicCompoundDensity: String](/documentation/homekit/hmcharacteristictypevolatileorganiccompounddensity)

###### Fans

- [let HMCharacteristicTypeCurrentFanState: String](/documentation/homekit/hmcharacteristictypecurrentfanstate)

###### Values

- [HMCharacteristicValueCurrentFanState](/documentation/homekit/hmcharacteristicvaluecurrentfanstate)

###### Fan State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetFanState: String](/documentation/homekit/hmcharacteristictypetargetfanstate)

###### Values

- [HMCharacteristicValueTargetFanState](/documentation/homekit/hmcharacteristicvaluetargetfanstate)

###### Fan State

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetfanstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetfanstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetfanstate/init(rawvalue:))
- [let HMCharacteristicTypeRotationDirection: String](/documentation/homekit/hmcharacteristictyperotationdirection)

###### Values

- [HMCharacteristicValueRotationDirection](/documentation/homekit/hmcharacteristicvaluerotationdirection)

###### Rotation

- [case clockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/clockwise)
- [case counterClockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/counterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerotationdirection/init(rawvalue:))
- [let HMCharacteristicTypeRotationSpeed: String](/documentation/homekit/hmcharacteristictyperotationspeed)
- [let HMCharacteristicTypeSwingMode: String](/documentation/homekit/hmcharacteristictypeswingmode)

###### Values

- [HMCharacteristicValueSwingMode](/documentation/homekit/hmcharacteristicvalueswingmode)

###### Movement Mode

- [case disabled](/documentation/homekit/hmcharacteristicvalueswingmode/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueswingmode/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueswingmode/init(rawvalue:))

###### Purifiers and filters

- [let HMCharacteristicTypeCurrentAirPurifierState: String](/documentation/homekit/hmcharacteristictypecurrentairpurifierstate)

###### Values

- [HMCharacteristicValueCurrentAirPurifierState](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate)

###### Air Purifier States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetAirPurifierState: String](/documentation/homekit/hmcharacteristictypetargetairpurifierstate)

###### Values

- [HMCharacteristicValueTargetAirPurifierState](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate)

###### Air Purifier States

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeFilterLifeLevel: String](/documentation/homekit/hmcharacteristictypefilterlifelevel)
- [let HMCharacteristicTypeFilterChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterchangeindication)

###### Values

- [HMCharacteristicValueFilterChange](/documentation/homekit/hmcharacteristicvaluefilterchange)

###### Filter Change Indicator

- [case notNeeded](/documentation/homekit/hmcharacteristicvaluefilterchange/notneeded)
- [case needed](/documentation/homekit/hmcharacteristicvaluefilterchange/needed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluefilterchange/init(rawvalue:))
- [let HMCharacteristicTypeFilterResetChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterresetchangeindication)

###### Water

- [let HMCharacteristicTypeWaterLevel: String](/documentation/homekit/hmcharacteristictypewaterlevel)
- [let HMCharacteristicTypeValveType: String](/documentation/homekit/hmcharacteristictypevalvetype)

###### Values

- [HMCharacteristicValueValveType](/documentation/homekit/hmcharacteristicvaluevalvetype)

###### Valve Types

- [case genericValve](/documentation/homekit/hmcharacteristicvaluevalvetype/genericvalve)
- [case irrigation](/documentation/homekit/hmcharacteristicvaluevalvetype/irrigation)
- [case showerHead](/documentation/homekit/hmcharacteristicvaluevalvetype/showerhead)
- [case waterFaucet](/documentation/homekit/hmcharacteristicvaluevalvetype/waterfaucet)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevalvetype/init(rawvalue:))
- [let HMCharacteristicTypeLeakDetected: String](/documentation/homekit/hmcharacteristictypeleakdetected)

###### Values

- [HMCharacteristicValueLeakStatus](/documentation/homekit/hmcharacteristicvalueleakstatus)

###### Leak Status

- [case none](/documentation/homekit/hmcharacteristicvalueleakstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvalueleakstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueleakstatus/init(rawvalue:))

###### Doors and windows

- [let HMCharacteristicTypeCurrentDoorState: String](/documentation/homekit/hmcharacteristictypecurrentdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetDoorState: String](/documentation/homekit/hmcharacteristictypetargetdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [HMCharacteristicValueTargetDoorState](/documentation/homekit/hmcharacteristicvaluetargetdoorstate)

###### Door States

- [case closed](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/closed)
- [case open](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/open)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentPosition: String](/documentation/homekit/hmcharacteristictypecurrentposition)
- [let HMCharacteristicTypeTargetPosition: String](/documentation/homekit/hmcharacteristictypetargetposition)
- [let HMCharacteristicTypePositionState: String](/documentation/homekit/hmcharacteristictypepositionstate)

###### Values

- [HMCharacteristicValuePositionState](/documentation/homekit/hmcharacteristicvaluepositionstate)

###### Position States

- [case closing](/documentation/homekit/hmcharacteristicvaluepositionstate/closing)
- [case opening](/documentation/homekit/hmcharacteristicvaluepositionstate/opening)
- [case stopped](/documentation/homekit/hmcharacteristicvaluepositionstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepositionstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusJammed: String](/documentation/homekit/hmcharacteristictypestatusjammed)

###### Values

- [HMCharacteristicValueJammedStatus](/documentation/homekit/hmcharacteristicvaluejammedstatus)

###### Jammed Status

- [case none](/documentation/homekit/hmcharacteristicvaluejammedstatus/none)
- [case jammed](/documentation/homekit/hmcharacteristicvaluejammedstatus/jammed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluejammedstatus/init(rawvalue:))
- [let HMCharacteristicTypeHoldPosition: String](/documentation/homekit/hmcharacteristictypeholdposition)
- [let HMCharacteristicTypeSlatType: String](/documentation/homekit/hmcharacteristictypeslattype)

###### Values

- [HMCharacteristicValueSlatType](/documentation/homekit/hmcharacteristicvalueslattype)

###### Slat Types

- [case horizontal](/documentation/homekit/hmcharacteristicvalueslattype/horizontal)
- [case vertical](/documentation/homekit/hmcharacteristicvalueslattype/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueslattype/init(rawvalue:))
- [let HMCharacteristicTypeCurrentSlatState: String](/documentation/homekit/hmcharacteristictypecurrentslatstate)

###### Values

- [HMCharacteristicValueCurrentSlatState](/documentation/homekit/hmcharacteristicvaluecurrentslatstate)

###### Slat States

- [case stationary](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/stationary)
- [case jammed](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/jammed)
- [case oscillating](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/oscillating)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/init(rawvalue:))

###### Tilting mechanisms

- [let HMCharacteristicTypeCurrentHorizontalTilt: String](/documentation/homekit/hmcharacteristictypecurrenthorizontaltilt)
- [let HMCharacteristicTypeTargetHorizontalTilt: String](/documentation/homekit/hmcharacteristictypetargethorizontaltilt)
- [let HMCharacteristicTypeCurrentVerticalTilt: String](/documentation/homekit/hmcharacteristictypecurrentverticaltilt)
- [let HMCharacteristicTypeTargetVerticalTilt: String](/documentation/homekit/hmcharacteristictypetargetverticaltilt)
- [let HMCharacteristicTypeCurrentTilt: String](/documentation/homekit/hmcharacteristictypecurrenttilt)
- [let HMCharacteristicTypeTargetTilt: String](/documentation/homekit/hmcharacteristictypetargettilt)

###### Locks and openers

- [let HMCharacteristicTypeLockManagementAutoSecureTimeout: String](/documentation/homekit/hmcharacteristictypelockmanagementautosecuretimeout)
- [let HMCharacteristicTypeLockManagementControlPoint: String](/documentation/homekit/hmcharacteristictypelockmanagementcontrolpoint)
- [let HMCharacteristicTypeLockMechanismLastKnownAction: String](/documentation/homekit/hmcharacteristictypelockmechanismlastknownaction)

###### Values

- [HMCharacteristicValueLockMechanismLastKnownAction](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction)

###### Lock Mechanism Actions

- [case securedRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedremotely)
- [case securedUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovement)
- [case securedUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementexterior)
- [case securedUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementinterior)
- [case securedWithAutomaticSecureTimeout](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithautomaticsecuretimeout)
- [case securedWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithkeypad)
- [case unsecuredRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredremotely)
- [case unsecuredUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovement)
- [case unsecuredUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementexterior)
- [case unsecuredUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementinterior)
- [case unsecuredWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredwithkeypad)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/init(rawvalue:))
- [let HMCharacteristicTypeLockPhysicalControls: String](/documentation/homekit/hmcharacteristictypelockphysicalcontrols)

###### Values

- [HMCharacteristicValueLockPhysicalControlsState](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate)

###### Lock Physical Control State

- [case notLocked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/notlocked)
- [case locked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/locked)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/init(rawvalue:))
- [let HMCharacteristicTypeMotionDetected: String](/documentation/homekit/hmcharacteristictypemotiondetected)
- [let HMCharacteristicTypeCurrentLockMechanismState: String](/documentation/homekit/hmcharacteristictypecurrentlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetLockMechanismState: String](/documentation/homekit/hmcharacteristictypetargetlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [HMCharacteristicValueTargetLockMechanismState](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate)

###### Lock Mechanism States

- [case secured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/secured)
- [case unsecured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/unsecured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeRemoteKey: String](/documentation/homekit/hmcharacteristictyperemotekey)

###### Values

- [HMCharacteristicValueRemoteKey](/documentation/homekit/hmcharacteristicvalueremotekey)

###### Remote states

- [case arrowDown](/documentation/homekit/hmcharacteristicvalueremotekey/arrowdown)
- [case arrowLeft](/documentation/homekit/hmcharacteristicvalueremotekey/arrowleft)
- [case arrowRight](/documentation/homekit/hmcharacteristicvalueremotekey/arrowright)
- [case arrowUp](/documentation/homekit/hmcharacteristicvalueremotekey/arrowup)
- [case back](/documentation/homekit/hmcharacteristicvalueremotekey/back)
- [case exit](/documentation/homekit/hmcharacteristicvalueremotekey/exit)
- [case fastForward](/documentation/homekit/hmcharacteristicvalueremotekey/fastforward)
- [case home](/documentation/homekit/hmcharacteristicvalueremotekey/home)
- [case info](/documentation/homekit/hmcharacteristicvalueremotekey/info)
- [case menu](/documentation/homekit/hmcharacteristicvalueremotekey/menu)
- [case nextTrack](/documentation/homekit/hmcharacteristicvalueremotekey/nexttrack)
- [case pause](/documentation/homekit/hmcharacteristicvalueremotekey/pause)
- [case play](/documentation/homekit/hmcharacteristicvalueremotekey/play)
- [case playPause](/documentation/homekit/hmcharacteristicvalueremotekey/playpause)
- [case previousTrack](/documentation/homekit/hmcharacteristicvalueremotekey/previoustrack)
- [case rewind](/documentation/homekit/hmcharacteristicvalueremotekey/rewind)
- [case select](/documentation/homekit/hmcharacteristicvalueremotekey/select)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueremotekey/init(rawvalue:))

###### Safety and security

- [let HMCharacteristicTypeCurrentSecuritySystemState: String](/documentation/homekit/hmcharacteristictypecurrentsecuritysystemstate)

###### Values

- [HMCharacteristicValueCurrentSecuritySystemState](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/nightarm)
- [case disarmed](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/disarmed)
- [case triggered](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/triggered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetSecuritySystemState: String](/documentation/homekit/hmcharacteristictypetargetsecuritysystemstate)

###### Values

- [HMCharacteristicValueTargetSecuritySystemState](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/nightarm)
- [case disarm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/disarm)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeObstructionDetected: String](/documentation/homekit/hmcharacteristictypeobstructiondetected)
- [let HMCharacteristicTypeOccupancyDetected: String](/documentation/homekit/hmcharacteristictypeoccupancydetected)

###### Values

- [HMCharacteristicValueOccupancyStatus](/documentation/homekit/hmcharacteristicvalueoccupancystatus)

###### Occupancy Status

- [case notOccupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/notoccupied)
- [case occupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/occupied)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueoccupancystatus/init(rawvalue:))
- [let HMCharacteristicTypeSecuritySystemAlarmType: String](/documentation/homekit/hmcharacteristictypesecuritysystemalarmtype)

###### Values

- [HMCharacteristicValueSecuritySystemAlarmType](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype)

###### Alarm Types

- [case noAlarm](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/noalarm)
- [case unknown](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/init(rawvalue:))
- [let HMCharacteristicPropertyRequiresAuthorizationData: String](/documentation/homekit/hmcharacteristicpropertyrequiresauthorizationdata)

###### Audio and video

- [let HMCharacteristicTypeSupportedRTPConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedrtpconfiguration)
- [let HMCharacteristicTypeDigitalZoom: String](/documentation/homekit/hmcharacteristictypedigitalzoom)
- [let HMCharacteristicTypeOpticalZoom: String](/documentation/homekit/hmcharacteristictypeopticalzoom)
- [let HMCharacteristicTypeImageMirroring: String](/documentation/homekit/hmcharacteristictypeimagemirroring)
- [let HMCharacteristicTypeImageRotation: String](/documentation/homekit/hmcharacteristictypeimagerotation)
- [let HMCharacteristicTypeNightVision: String](/documentation/homekit/hmcharacteristictypenightvision)
- [let HMCharacteristicTypeStreamingStatus: String](/documentation/homekit/hmcharacteristictypestreamingstatus)
- [let HMCharacteristicTypeSupportedVideoStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedvideostreamconfiguration)
- [let HMCharacteristicTypeSupportedAudioStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedaudiostreamconfiguration)
- [let HMCharacteristicTypeSelectedStreamConfiguration: String](/documentation/homekit/hmcharacteristictypeselectedstreamconfiguration)
- [let HMCharacteristicTypeSetupStreamEndpoint: String](/documentation/homekit/hmcharacteristictypesetupstreamendpoint)
- [let HMCharacteristicTypeAudioFeedback: String](/documentation/homekit/hmcharacteristictypeaudiofeedback)
- [let HMCharacteristicTypeVolume: String](/documentation/homekit/hmcharacteristictypevolume)
- [let HMCharacteristicTypeMute: String](/documentation/homekit/hmcharacteristictypemute)
- [let HMCharacteristicTypeVolumeSelector: String](/documentation/homekit/hmcharacteristictypevolumeselector)

###### Values

- [HMCharacteristicValueVolumeSelector](/documentation/homekit/hmcharacteristicvaluevolumeselector)

###### Volume cases

- [case volumeDecrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumedecrement)
- [case volumeIncrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumeincrement)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumeselector/init(rawvalue:))
- [let HMCharacteristicTypeVolumeControlType: String](/documentation/homekit/hmcharacteristictypevolumecontroltype)

###### Values

- [HMCharacteristicValueVolumeControlType](/documentation/homekit/hmcharacteristicvaluevolumecontroltype)

###### Volume types

- [case absolute](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/absolute)
- [case none](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/none)
- [case relative](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relative)
- [case relativeWithCurrent](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relativewithcurrent)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/init(rawvalue:))
- [let HMCharacteristicTypeClosedCaptions: String](/documentation/homekit/hmcharacteristictypeclosedcaptions)

###### Values

- [HMCharacteristicValueClosedCaptions](/documentation/homekit/hmcharacteristicvalueclosedcaptions)

###### Closed caption states

- [case disabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueclosedcaptions/init(rawvalue:))
- [let HMCharacteristicTypePictureMode: String](/documentation/homekit/hmcharacteristictypepicturemode)

###### Values

- [HMCharacteristicValuePictureMode](/documentation/homekit/hmcharacteristicvaluepicturemode)

###### Television states

- [case bright](/documentation/homekit/hmcharacteristicvaluepicturemode/bright)
- [case calibrated](/documentation/homekit/hmcharacteristicvaluepicturemode/calibrated)
- [case computer](/documentation/homekit/hmcharacteristicvaluepicturemode/computer)
- [case custom1](/documentation/homekit/hmcharacteristicvaluepicturemode/custom1)
- [case custom2](/documentation/homekit/hmcharacteristicvaluepicturemode/custom2)
- [case custom3](/documentation/homekit/hmcharacteristicvaluepicturemode/custom3)
- [case dark](/documentation/homekit/hmcharacteristicvaluepicturemode/dark)
- [case game](/documentation/homekit/hmcharacteristicvaluepicturemode/game)
- [case movie](/documentation/homekit/hmcharacteristicvaluepicturemode/movie)
- [case night](/documentation/homekit/hmcharacteristicvaluepicturemode/night)
- [case photo](/documentation/homekit/hmcharacteristicvaluepicturemode/photo)
- [case sport](/documentation/homekit/hmcharacteristicvaluepicturemode/sport)
- [case standard](/documentation/homekit/hmcharacteristicvaluepicturemode/standard)
- [case vivid](/documentation/homekit/hmcharacteristicvaluepicturemode/vivid)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepicturemode/init(rawvalue:))

###### General state

- [let HMCharacteristicTypeActive: String](/documentation/homekit/hmcharacteristictypeactive)

###### Values

- [HMCharacteristicValueActivationState](/documentation/homekit/hmcharacteristicvalueactivationstate)

###### Activation States

- [case inactive](/documentation/homekit/hmcharacteristicvalueactivationstate/inactive)
- [case active](/documentation/homekit/hmcharacteristicvalueactivationstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueactivationstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusTampered: String](/documentation/homekit/hmcharacteristictypestatustampered)

###### Values

- [HMCharacteristicValueTamperedStatus](/documentation/homekit/hmcharacteristicvaluetamperedstatus)

###### Tampered Status

- [case none](/documentation/homekit/hmcharacteristicvaluetamperedstatus/none)
- [case tampered](/documentation/homekit/hmcharacteristicvaluetamperedstatus/tampered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetamperedstatus/init(rawvalue:))
- [let HMCharacteristicTypeStatusFault: String](/documentation/homekit/hmcharacteristictypestatusfault)

###### Values

- [HMCharacteristicValueStatusFault](/documentation/homekit/hmcharacteristicvaluestatusfault)

###### Fault Status

- [case noFault](/documentation/homekit/hmcharacteristicvaluestatusfault/nofault)
- [case generalFault](/documentation/homekit/hmcharacteristicvaluestatusfault/generalfault)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluestatusfault/init(rawvalue:))
- [let HMCharacteristicTypeStatusActive: String](/documentation/homekit/hmcharacteristictypestatusactive)
- [let HMCharacteristicTypeInUse: String](/documentation/homekit/hmcharacteristictypeinuse)

###### Values

- [HMCharacteristicValueUsageState](/documentation/homekit/hmcharacteristicvalueusagestate)

###### Usage States

- [case notInUse](/documentation/homekit/hmcharacteristicvalueusagestate/notinuse)
- [case inUse](/documentation/homekit/hmcharacteristicvalueusagestate/inuse)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueusagestate/init(rawvalue:))
- [let HMCharacteristicTypeIsConfigured: String](/documentation/homekit/hmcharacteristictypeisconfigured)

###### Values

- [HMCharacteristicValueConfigurationState](/documentation/homekit/hmcharacteristicvalueconfigurationstate)

###### Configuration States

- [case notConfigured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/notconfigured)
- [case configured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/configured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueconfigurationstate/init(rawvalue:))
- [let HMCharacteristicTypeRemainingDuration: String](/documentation/homekit/hmcharacteristictyperemainingduration)
- [let HMCharacteristicTypeSetDuration: String](/documentation/homekit/hmcharacteristictypesetduration)
- [let HMCharacteristicTypeProgramMode: String](/documentation/homekit/hmcharacteristictypeprogrammode)

###### Values

- [HMCharacteristicValueProgramMode](/documentation/homekit/hmcharacteristicvalueprogrammode)

###### Constants

- [case notScheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/notscheduled)
- [case scheduleOverriddenToManual](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduleoverriddentomanual)
- [case scheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueprogrammode/init(rawvalue:))
- [let HMCharacteristicTypeWiFiSatelliteStatus: String](/documentation/homekit/hmcharacteristictypewifisatellitestatus)

###### Values

- [HMCharacteristicValueWiFiSatelliteStatus](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus)

###### Network states

- [case connected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/connected)
- [case notConnected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/notconnected)
- [case unknown](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/init(rawvalue:))
- [let HMCharacteristicTypeWANStatusList: String](/documentation/homekit/hmcharacteristictypewanstatuslist)
- [let HMCharacteristicTypeTargetMediaState: String](/documentation/homekit/hmcharacteristictypetargetmediastate)

###### Values

- [HMCharacteristicValueTargetMediaState](/documentation/homekit/hmcharacteristicvaluetargetmediastate)

###### Media states

- [case pause](/documentation/homekit/hmcharacteristicvaluetargetmediastate/pause)
- [case play](/documentation/homekit/hmcharacteristicvaluetargetmediastate/play)
- [case stop](/documentation/homekit/hmcharacteristicvaluetargetmediastate/stop)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetmediastate/init(rawvalue:))
- [let HMCharacteristicTypeRouterStatus: String](/documentation/homekit/hmcharacteristictyperouterstatus)

###### Values

- [HMCharacteristicValueRouterStatus](/documentation/homekit/hmcharacteristicvaluerouterstatus)

###### Router states

- [case notReady](/documentation/homekit/hmcharacteristicvaluerouterstatus/notready)
- [case ready](/documentation/homekit/hmcharacteristicvaluerouterstatus/ready)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerouterstatus/init(rawvalue:))
- [let HMCharacteristicTypeCurrentMediaState: String](/documentation/homekit/hmcharacteristictypecurrentmediastate)

###### Values

- [HMCharacteristicValueCurrentMediaState](/documentation/homekit/hmcharacteristicvaluecurrentmediastate)

###### Current media states

- [case interrupted](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/interrupted)
- [case loading](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/loading)
- [case paused](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/paused)
- [case playing](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/playing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/stopped)
- [case unknown](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentVisibilityState: String](/documentation/homekit/hmcharacteristictypecurrentvisibilitystate)

###### Values

- [HMCharacteristicValueCurrentVisibilityState](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate)

###### Visibility states

- [case alwaysShown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/alwaysshown)
- [case connected](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/connected)
- [case hidden](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/hidden)
- [case shown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/shown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/init(rawvalue:))
- [let HMCharacteristicTypeTargetVisibilityState: String](/documentation/homekit/hmcharacteristictypetargetvisibilitystate)

###### Values

- [HMCharacteristicValueTargetVisibilityState](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate)

###### Visibility states

- [case hide](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/init(rawvalue:))
- [let HMCharacteristicPropertySupportsEventNotification: String](/documentation/homekit/hmcharacteristicpropertysupportseventnotification-2f0ml)

###### Accessory identification

- [let HMCharacteristicTypeName: String](/documentation/homekit/hmcharacteristictypename)
- [let HMCharacteristicTypeIdentify: String](/documentation/homekit/hmcharacteristictypeidentify)
- [let HMCharacteristicTypeVersion: String](/documentation/homekit/hmcharacteristictypeversion)
- [let HMCharacteristicTypeLogs: String](/documentation/homekit/hmcharacteristictypelogs)
- [let HMCharacteristicTypeAdminOnlyAccess: String](/documentation/homekit/hmcharacteristictypeadminonlyaccess)
- [let HMCharacteristicTypeHardwareVersion: String](/documentation/homekit/hmcharacteristictypehardwareversion)
- [let HMCharacteristicTypeSoftwareVersion: String](/documentation/homekit/hmcharacteristictypesoftwareversion)
- [let HMCharacteristicTypeLabelIndex: String](/documentation/homekit/hmcharacteristictypelabelindex)
- [let HMCharacteristicTypeLabelNamespace: String](/documentation/homekit/hmcharacteristictypelabelnamespace)

###### Values

- [HMCharacteristicValueLabelNamespace](/documentation/homekit/hmcharacteristicvaluelabelnamespace)

###### Namespaces

- [case dot](/documentation/homekit/hmcharacteristicvaluelabelnamespace/dot)
- [case numeral](/documentation/homekit/hmcharacteristicvaluelabelnamespace/numeral)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelabelnamespace/init(rawvalue:))
- [let HMCharacteristicTypeActiveIdentifier: String](/documentation/homekit/hmcharacteristictypeactiveidentifier)
- [let HMCharacteristicTypeIdentifier: String](/documentation/homekit/hmcharacteristictypeidentifier)
- [let HMCharacteristicTypeInputDeviceType: String](/documentation/homekit/hmcharacteristictypeinputdevicetype)

###### Values

- [HMCharacteristicValueInputDeviceType](/documentation/homekit/hmcharacteristicvalueinputdevicetype)

###### Input devices

- [case audioSystem](/documentation/homekit/hmcharacteristicvalueinputdevicetype/audiosystem)
- [case none](/documentation/homekit/hmcharacteristicvalueinputdevicetype/none)
- [case other](/documentation/homekit/hmcharacteristicvalueinputdevicetype/other)
- [case playback](/documentation/homekit/hmcharacteristicvalueinputdevicetype/playback)
- [case recording](/documentation/homekit/hmcharacteristicvalueinputdevicetype/recording)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tuner)
- [case tv](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tv)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputdevicetype/init(rawvalue:))
- [let HMCharacteristicTypeInputSourceType: String](/documentation/homekit/hmcharacteristictypeinputsourcetype)

###### Values

- [HMCharacteristicValueInputSourceType](/documentation/homekit/hmcharacteristicvalueinputsourcetype)

###### Accessory source types

- [case airPlay](/documentation/homekit/hmcharacteristicvalueinputsourcetype/airplay)
- [case application](/documentation/homekit/hmcharacteristicvalueinputsourcetype/application)
- [case componentVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/componentvideo)
- [case compositeVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/compositevideo)
- [case dvi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/dvi)
- [case hdmi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/hdmi)
- [case homeScreen](/documentation/homekit/hmcharacteristicvalueinputsourcetype/homescreen)
- [case other](/documentation/homekit/hmcharacteristicvalueinputsourcetype/other)
- [case sVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/svideo)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputsourcetype/tuner)
- [case usb](/documentation/homekit/hmcharacteristicvalueinputsourcetype/usb)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputsourcetype/init(rawvalue:))
- [let HMCharacteristicTypeConfiguredName: String](/documentation/homekit/hmcharacteristictypeconfiguredname)

###### Deprecated characteristic types

- [let HMCharacteristicTypeManufacturer: String](/documentation/homekit/hmcharacteristictypemanufacturer)
- [let HMCharacteristicTypeModel: String](/documentation/homekit/hmcharacteristictypemodel)
- [let HMCharacteristicTypeFirmwareVersion: String](/documentation/homekit/hmcharacteristictypefirmwareversion)
- [let HMCharacteristicTypeSerialNumber: String](/documentation/homekit/hmcharacteristictypeserialnumber)

###### Controlling a characteristic

- [var value: Any?](/documentation/homekit/hmcharacteristic/value)
- [func readValue(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/readvalue(completionhandler:))
- [func writeValue(Any?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/writevalue(_:completionhandler:))
- [func updateAuthorizationData(Data?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/updateauthorizationdata(_:completionhandler:))

###### Managing characteristic presentation

- [var metadata: HMCharacteristicMetadata?](/documentation/homekit/hmcharacteristic/metadata)
- [HMCharacteristicMetadata](/documentation/homekit/hmcharacteristicmetadata)

###### Describing a characteristic

- [var manufacturerDescription: String?](/documentation/homekit/hmcharacteristicmetadata/manufacturerdescription)

###### Bounding the value

- [var validValues: [NSNumber]?](/documentation/homekit/hmcharacteristicmetadata/validvalues)
- [var minimumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/minimumvalue)
- [var maximumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maximumvalue)
- [var stepValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/stepvalue)
- [var maxLength: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maxlength)

###### Formatting the value

- [var format: String?](/documentation/homekit/hmcharacteristicmetadata/format)
- [Characteristic Data Formats](/documentation/homekit/characteristic-data-formats)

###### Booleans

- [let HMCharacteristicMetadataFormatBool: String](/documentation/homekit/hmcharacteristicmetadataformatbool)

###### Strings

- [let HMCharacteristicMetadataFormatString: String](/documentation/homekit/hmcharacteristicmetadataformatstring)

###### Signed Values

- [let HMCharacteristicMetadataFormatInt: String](/documentation/homekit/hmcharacteristicmetadataformatint)
- [let HMCharacteristicMetadataFormatFloat: String](/documentation/homekit/hmcharacteristicmetadataformatfloat)

###### Unsigned Integers

- [let HMCharacteristicMetadataFormatUInt8: String](/documentation/homekit/hmcharacteristicmetadataformatuint8)
- [let HMCharacteristicMetadataFormatUInt16: String](/documentation/homekit/hmcharacteristicmetadataformatuint16)
- [let HMCharacteristicMetadataFormatUInt32: String](/documentation/homekit/hmcharacteristicmetadataformatuint32)
- [let HMCharacteristicMetadataFormatUInt64: String](/documentation/homekit/hmcharacteristicmetadataformatuint64)

###### Data

- [let HMCharacteristicMetadataFormatData: String](/documentation/homekit/hmcharacteristicmetadataformatdata)
- [let HMCharacteristicMetadataFormatTLV8: String](/documentation/homekit/hmcharacteristicmetadataformattlv8)

###### Collections

- [let HMCharacteristicMetadataFormatArray: String](/documentation/homekit/hmcharacteristicmetadataformatarray)
- [let HMCharacteristicMetadataFormatDictionary: String](/documentation/homekit/hmcharacteristicmetadataformatdictionary)

###### Specifying units

- [var units: String?](/documentation/homekit/hmcharacteristicmetadata/units)
- [Characteristic Units](/documentation/homekit/characteristic-units)

###### Parts Per Total

- [let HMCharacteristicMetadataUnitsPercentage: String](/documentation/homekit/hmcharacteristicmetadataunitspercentage)
- [let HMCharacteristicMetadataUnitsPartsPerMillion: String](/documentation/homekit/hmcharacteristicmetadataunitspartspermillion)

###### Temperature

- [let HMCharacteristicMetadataUnitsCelsius: String](/documentation/homekit/hmcharacteristicmetadataunitscelsius)
- [let HMCharacteristicMetadataUnitsFahrenheit: String](/documentation/homekit/hmcharacteristicmetadataunitsfahrenheit)

###### Time

- [let HMCharacteristicMetadataUnitsSeconds: String](/documentation/homekit/hmcharacteristicmetadataunitsseconds)

###### Light

- [let HMCharacteristicMetadataUnitsLux: String](/documentation/homekit/hmcharacteristicmetadataunitslux)

###### Mass

- [let HMCharacteristicMetadataUnitsMicrogramsPerCubicMeter: String](/documentation/homekit/hmcharacteristicmetadataunitsmicrogramspercubicmeter)

###### Rotation

- [let HMCharacteristicMetadataUnitsArcDegree: String](/documentation/homekit/hmcharacteristicmetadataunitsarcdegree)

###### Initializers

- [init()](/documentation/homekit/hmcharacteristicmetadata/init())

###### Receiving change notifications

- [func enableNotification(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/enablenotification(_:completionhandler:))
- [var isNotificationEnabled: Bool](/documentation/homekit/hmcharacteristic/isnotificationenabled)

###### Getting the characterized service

- [var service: HMService?](/documentation/homekit/hmcharacteristic/service)

###### Initializers

- [init()](/documentation/homekit/hmcharacteristic/init())

###### Identifying the service

- [var name: String](/documentation/homekit/hmservice/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmservice/uniqueidentifier)

###### Getting the service type

- [var serviceType: String](/documentation/homekit/hmservice/servicetype)
- [Accessory Service Types](/documentation/homekit/accessory-service-types)

###### Light

- [let HMServiceTypeLightbulb: String](/documentation/homekit/hmservicetypelightbulb)
- [let HMServiceTypeLightSensor: String](/documentation/homekit/hmservicetypelightsensor)

###### Power and Switches

- [let HMServiceTypeSwitch: String](/documentation/homekit/hmservicetypeswitch)
- [let HMServiceTypeBattery: String](/documentation/homekit/hmservicetypebattery)
- [let HMServiceTypeOutlet: String](/documentation/homekit/hmservicetypeoutlet)
- [let HMServiceTypeStatefulProgrammableSwitch: String](/documentation/homekit/hmservicetypestatefulprogrammableswitch)
- [let HMServiceTypeStatelessProgrammableSwitch: String](/documentation/homekit/hmservicetypestatelessprogrammableswitch)

###### Air Quality and Smoke Detection

- [let HMServiceTypeAirPurifier: String](/documentation/homekit/hmservicetypeairpurifier)
- [let HMServiceTypeAirQualitySensor: String](/documentation/homekit/hmservicetypeairqualitysensor)
- [let HMServiceTypeCarbonDioxideSensor: String](/documentation/homekit/hmservicetypecarbondioxidesensor)
- [let HMServiceTypeCarbonMonoxideSensor: String](/documentation/homekit/hmservicetypecarbonmonoxidesensor)
- [let HMServiceTypeSmokeSensor: String](/documentation/homekit/hmservicetypesmokesensor)

###### Temperature and Humidity

- [let HMServiceTypeHeaterCooler: String](/documentation/homekit/hmservicetypeheatercooler)
- [let HMServiceTypeTemperatureSensor: String](/documentation/homekit/hmservicetypetemperaturesensor)
- [let HMServiceTypeThermostat: String](/documentation/homekit/hmservicetypethermostat)
- [let HMServiceTypeFan: String](/documentation/homekit/hmservicetypefan)
- [let HMServiceTypeFilterMaintenance: String](/documentation/homekit/hmservicetypefiltermaintenance)
- [let HMServiceTypeHumidifierDehumidifier: String](/documentation/homekit/hmservicetypehumidifierdehumidifier)
- [let HMServiceTypeHumiditySensor: String](/documentation/homekit/hmservicetypehumiditysensor)
- [let HMServiceTypeVentilationFan: String](/documentation/homekit/hmservicetypeventilationfan)

###### Windows

- [let HMServiceTypeWindow: String](/documentation/homekit/hmservicetypewindow)
- [let HMServiceTypeWindowCovering: String](/documentation/homekit/hmservicetypewindowcovering)
- [let HMServiceTypeSlats: String](/documentation/homekit/hmservicetypeslats)

###### Water

- [let HMServiceTypeFaucet: String](/documentation/homekit/hmservicetypefaucet)
- [let HMServiceTypeValve: String](/documentation/homekit/hmservicetypevalve)
- [let HMServiceTypeIrrigationSystem: String](/documentation/homekit/hmservicetypeirrigationsystem)
- [let HMServiceTypeLeakSensor: String](/documentation/homekit/hmservicetypeleaksensor)

###### Locks and Openers

- [let HMServiceTypeDoor: String](/documentation/homekit/hmservicetypedoor)
- [let HMServiceTypeDoorbell: String](/documentation/homekit/hmservicetypedoorbell)
- [let HMServiceTypeGarageDoorOpener: String](/documentation/homekit/hmservicetypegaragedooropener)
- [let HMServiceTypeLockManagement: String](/documentation/homekit/hmservicetypelockmanagement)
- [let HMServiceTypeLockMechanism: String](/documentation/homekit/hmservicetypelockmechanism)

###### Safety and Security

- [let HMServiceTypeMotionSensor: String](/documentation/homekit/hmservicetypemotionsensor)
- [let HMServiceTypeOccupancySensor: String](/documentation/homekit/hmservicetypeoccupancysensor)
- [let HMServiceTypeSecuritySystem: String](/documentation/homekit/hmservicetypesecuritysystem)
- [let HMServiceTypeContactSensor: String](/documentation/homekit/hmservicetypecontactsensor)

###### Video and Audio

- [let HMServiceTypeCameraControl: String](/documentation/homekit/hmservicetypecameracontrol)
- [let HMServiceTypeCameraRTPStreamManagement: String](/documentation/homekit/hmservicetypecamerartpstreammanagement)
- [let HMServiceTypeMicrophone: String](/documentation/homekit/hmservicetypemicrophone)
- [let HMServiceTypeSpeaker: String](/documentation/homekit/hmservicetypespeaker)
- [let HMServiceTypeInputSource: String](/documentation/homekit/hmservicetypeinputsource)
- [let HMServiceTypeTelevision: String](/documentation/homekit/hmservicetypetelevision)

###### Network

- [let HMServiceTypeWiFiRouter: String](/documentation/homekit/hmservicetypewifirouter)
- [let HMServiceTypeWiFiSatellite: String](/documentation/homekit/hmservicetypewifisatellite)

###### Information

- [let HMServiceTypeLabel: String](/documentation/homekit/hmservicetypelabel)
- [let HMServiceTypeAccessoryInformation: String](/documentation/homekit/hmservicetypeaccessoryinformation)
- [var localizedDescription: String](/documentation/homekit/hmservice/localizeddescription)

###### Reading service properties

- [var isPrimaryService: Bool](/documentation/homekit/hmservice/isprimaryservice)
- [var isUserInteractive: Bool](/documentation/homekit/hmservice/isuserinteractive)

###### Associating a secondary service

- [var associatedServiceType: String?](/documentation/homekit/hmservice/associatedservicetype)
- [func updateAssociatedServiceType(String?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updateassociatedservicetype(_:completionhandler:))

###### Finding the linked services

- [var linkedServices: [HMService]?](/documentation/homekit/hmservice/linkedservices)

###### Getting the service’s provider

- [var accessory: HMAccessory?](/documentation/homekit/hmservice/accessory)

###### Initializers

- [init()](/documentation/homekit/hmservice/init())

###### Instance Properties

- [var matterEndpointID: UInt16?](/documentation/homekit/hmservice/matterendpointid-62vu6)

##### Managing bridged accessories

- [var isBridged: Bool](/documentation/homekit/hmaccessory/isbridged)
- [var uniqueIdentifiersForBridgedAccessories: [UUID]?](/documentation/homekit/hmaccessory/uniqueidentifiersforbridgedaccessories)
- [var identifiersForBridgedAccessories: [UUID]?](/documentation/homekit/hmaccessory/identifiersforbridgedaccessories)

##### Getting manufacturer information

- [var firmwareVersion: String?](/documentation/homekit/hmaccessory/firmwareversion)
- [var manufacturer: String?](/documentation/homekit/hmaccessory/manufacturer)
- [var model: String?](/documentation/homekit/hmaccessory/model)

##### Browsing for accessories

- [HMAccessoryBrowser](/documentation/homekit/hmaccessorybrowser)

###### Discovering accessories

- [var discoveredAccessories: [HMAccessory]](/documentation/homekit/hmaccessorybrowser/discoveredaccessories)
- [func startSearchingForNewAccessories()](/documentation/homekit/hmaccessorybrowser/startsearchingfornewaccessories())
- [func stopSearchingForNewAccessories()](/documentation/homekit/hmaccessorybrowser/stopsearchingfornewaccessories())

###### Tracking the addition or removal of accessories

- [var delegate: (any HMAccessoryBrowserDelegate)?](/documentation/homekit/hmaccessorybrowser/delegate)
- [HMAccessoryBrowserDelegate](/documentation/homekit/hmaccessorybrowserdelegate)

###### Tracking new accessories

- [func accessoryBrowser(HMAccessoryBrowser, didFindNewAccessory: HMAccessory)](/documentation/homekit/hmaccessorybrowserdelegate/accessorybrowser(_:didfindnewaccessory:))
- [func accessoryBrowser(HMAccessoryBrowser, didRemoveNewAccessory: HMAccessory)](/documentation/homekit/hmaccessorybrowserdelegate/accessorybrowser(_:didremovenewaccessory:))

###### Initializers

- [init()](/documentation/homekit/hmaccessorybrowser/init())

##### Instance Properties

- [var matterNodeID: UInt64?](/documentation/homekit/hmaccessory/matternodeid-67v1j)
- [var bridgedAccessories: [HMAccessory]](/documentation/homekit/hmaccessory/bridgedaccessories)
- [var hapInstanceID: UInt64?](/documentation/homekit/hmaccessory/hapinstanceid-3cusx)
- [var home: HMHome?](/documentation/homekit/hmaccessory/home)
- [var isVendorAccessory: Bool](/documentation/homekit/hmaccessory/isvendoraccessory)

##### Initializers

- [init()](/documentation/homekit/hmaccessory/init())

#### Grouping services

- [func servicesWithTypes([String]) -> [HMService]?](/documentation/homekit/hmhome/serviceswithtypes(_:))
- [var serviceGroups: [HMServiceGroup]](/documentation/homekit/hmhome/servicegroups)
- [func addServiceGroup(withName: String, completionHandler: (HMServiceGroup?, (any Error)?) -> Void)](/documentation/homekit/hmhome/addservicegroup(withname:completionhandler:))
- [func removeServiceGroup(HMServiceGroup, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removeservicegroup(_:completionhandler:))
- [HMServiceGroup](/documentation/homekit/hmservicegroup)

##### Managing Service Groups

- [var name: String](/documentation/homekit/hmservicegroup/name)
- [var uniqueIdentifier: UUID](/documentation/homekit/hmservicegroup/uniqueidentifier)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservicegroup/updatename(_:completionhandler:))
- [var services: [HMService]](/documentation/homekit/hmservicegroup/services)
- [func addService(HMService, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservicegroup/addservice(_:completionhandler:))
- [func removeService(HMService, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservicegroup/removeservice(_:completionhandler:))

#### Querying the state of a home hub

- [var homeHubState: HMHomeHubState](/documentation/homekit/hmhome/homehubstate)
- [HMHomeHubState](/documentation/homekit/hmhomehubstate)

##### Specifying the State

- [case connected](/documentation/homekit/hmhomehubstate/connected)
- [case disconnected](/documentation/homekit/hmhomehubstate/disconnected)
- [case notAvailable](/documentation/homekit/hmhomehubstate/notavailable)

##### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmhomehubstate/init(rawvalue:))

#### Creating action sets

- [var actionSets: [HMActionSet]](/documentation/homekit/hmhome/actionsets)
- [func addActionSet(withName: String, completionHandler: (HMActionSet?, (any Error)?) -> Void)](/documentation/homekit/hmhome/addactionset(withname:completionhandler:))
- [func removeActionSet(HMActionSet, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removeactionset(_:completionhandler:))
- [func executeActionSet(HMActionSet, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/executeactionset(_:completionhandler:))
- [func builtinActionSet(ofType: String) -> HMActionSet?](/documentation/homekit/hmhome/builtinactionset(oftype:))
- [HMActionSet](/documentation/homekit/hmactionset)

##### Identifiying an action set

- [var uniqueIdentifier: UUID](/documentation/homekit/hmactionset/uniqueidentifier)
- [var name: String](/documentation/homekit/hmactionset/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/updatename(_:completionhandler:))

##### Specifying a type

- [var actionSetType: String](/documentation/homekit/hmactionset/actionsettype)
- [Action Set Types](/documentation/homekit/action-set-types)

###### Built-in Types

- [let HMActionSetTypeHomeArrival: String](/documentation/homekit/hmactionsettypehomearrival)
- [let HMActionSetTypeHomeDeparture: String](/documentation/homekit/hmactionsettypehomedeparture)
- [let HMActionSetTypeSleep: String](/documentation/homekit/hmactionsettypesleep)
- [let HMActionSetTypeWakeUp: String](/documentation/homekit/hmactionsettypewakeup)

###### User Defined Types

- [let HMActionSetTypeUserDefined: String](/documentation/homekit/hmactionsettypeuserdefined)

###### Trigger Owned Types

- [let HMActionSetTypeTriggerOwned: String](/documentation/homekit/hmactionsettypetriggerowned)

##### Defining the associated actions

- [var actions: Set<HMAction>](/documentation/homekit/hmactionset/actions)
- [func addAction(HMAction, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/addaction(_:completionhandler:))
- [func removeAction(HMAction, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/removeaction(_:completionhandler:))
- [HMCharacteristicWriteAction](/documentation/homekit/hmcharacteristicwriteaction)

###### New Methods

- [init(characteristic: HMCharacteristic, targetValue: TargetValueType)](/documentation/homekit/hmcharacteristicwriteaction/init(characteristic:targetvalue:))
- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicwriteaction/characteristic)
- [var targetValue: TargetValueType](/documentation/homekit/hmcharacteristicwriteaction/targetvalue)
- [func updateTargetValue(TargetValueType, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristicwriteaction/updatetargetvalue(_:completionhandler:))
- [HMAction](/documentation/homekit/hmaction)

###### Identifying an action

- [var uniqueIdentifier: UUID](/documentation/homekit/hmaction/uniqueidentifier)

###### Initializers

- [init()](/documentation/homekit/hmaction/init())

###### Type Methods

- [class func new() -> Self](/documentation/homekit/hmaction/new())

##### Keeping track of execution

- [var isExecuting: Bool](/documentation/homekit/hmactionset/isexecuting)
- [var lastExecutionDate: Date?](/documentation/homekit/hmactionset/lastexecutiondate)

#### Triggering an action set

- [var triggers: [HMTrigger]](/documentation/homekit/hmhome/triggers)
- [func addTrigger(HMTrigger, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/addtrigger(_:completionhandler:))
- [func removeTrigger(HMTrigger, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removetrigger(_:completionhandler:))
- [HMTimerTrigger](/documentation/homekit/hmtimertrigger)

##### Creating a timer trigger

- [init(name: String, fireDate: Date, recurrence: DateComponents?)](/documentation/homekit/hmtimertrigger/init(name:firedate:recurrence:))

##### Choosing the fire date

- [var fireDate: Date](/documentation/homekit/hmtimertrigger/firedate)
- [func updateFireDate(Date, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updatefiredate(_:completionhandler:))

##### Using recurrence

- [var recurrence: DateComponents?](/documentation/homekit/hmtimertrigger/recurrence)
- [func updateRecurrence(DateComponents?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updaterecurrence(_:completionhandler:))

##### Deprecated symbols

- [init(name: String, fireDate: Date, timeZone: TimeZone?, recurrence: DateComponents?, recurrenceCalendar: Calendar?)](/documentation/homekit/hmtimertrigger/init(name:firedate:timezone:recurrence:recurrencecalendar:))
- [var timeZone: TimeZone?](/documentation/homekit/hmtimertrigger/timezone)
- [func updateTimeZone(TimeZone?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updatetimezone(_:completionhandler:))
- [var recurrenceCalendar: Calendar?](/documentation/homekit/hmtimertrigger/recurrencecalendar)
- [HMEventTrigger](/documentation/homekit/hmeventtrigger)

##### Creating an event trigger

- [init(name: String, events: [HMEvent], predicate: NSPredicate?)](/documentation/homekit/hmeventtrigger/init(name:events:predicate:))
- [init(name: String, events: [HMEvent], end: [HMEvent]?, recurrences: [DateComponents]?, predicate: NSPredicate?)](/documentation/homekit/hmeventtrigger/init(name:events:end:recurrences:predicate:))

##### Querying trigger activation state

- [var triggerActivationState: HMEventTriggerActivationState](/documentation/homekit/hmeventtrigger/triggeractivationstate)
- [HMEventTriggerActivationState](/documentation/homekit/hmeventtriggeractivationstate)

###### Inspecting activation state

- [case disabled](/documentation/homekit/hmeventtriggeractivationstate/disabled)
- [case disabledNoCompatibleHomeHub](/documentation/homekit/hmeventtriggeractivationstate/disablednocompatiblehomehub)
- [case disabledNoHomeHub](/documentation/homekit/hmeventtriggeractivationstate/disablednohomehub)
- [case disabledNoLocationServicesAuthorization](/documentation/homekit/hmeventtriggeractivationstate/disablednolocationservicesauthorization)
- [case enabled](/documentation/homekit/hmeventtriggeractivationstate/enabled)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmeventtriggeractivationstate/init(rawvalue:))

##### Setting trigger events

- [var events: [HMEvent]](/documentation/homekit/hmeventtrigger/events)
- [func updateEvents([HMEvent], completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateevents(_:completionhandler:))
- [Location events](/documentation/homekit/location-events)

###### Locations

- [HMLocationEvent](/documentation/homekit/hmlocationevent)

###### Creating a Location Event

- [init(region: CLRegion)](/documentation/homekit/hmlocationevent/init(region:))

###### Inspecting the Region

- [var region: CLRegion?](/documentation/homekit/hmlocationevent/region)

###### Configuring the Region

- [func updateRegion(CLRegion, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmlocationevent/updateregion(_:completionhandler:))
- [HMMutableLocationEvent](/documentation/homekit/hmmutablelocationevent)

###### Controlling the Region

- [var region: CLRegion?](/documentation/homekit/hmmutablelocationevent/region)
- [Time events](/documentation/homekit/time-events)

###### Dates and times

- [HMCalendarEvent](/documentation/homekit/hmcalendarevent)

###### Creating a calendar event

- [init(fire: DateComponents)](/documentation/homekit/hmcalendarevent/init(fire:))

###### Inspecting the calendar event

- [var fireDateComponents: DateComponents](/documentation/homekit/hmcalendarevent/firedatecomponents)
- [HMMutableCalendarEvent](/documentation/homekit/hmmutablecalendarevent)

###### Configuring the calendar event

- [var fireDateComponents: DateComponents](/documentation/homekit/hmmutablecalendarevent/firedatecomponents)
- [HMTimeEvent](/documentation/homekit/hmtimeevent)

###### Significant events

- [HMSignificantEvent](/documentation/homekit/hmsignificantevent)

###### Significant event properties

- [static let sunrise: HMSignificantEvent](/documentation/homekit/hmsignificantevent/sunrise)
- [static let sunset: HMSignificantEvent](/documentation/homekit/hmsignificantevent/sunset)

###### Creating a significant event

- [init(String)](/documentation/homekit/hmsignificantevent/init(_:))
- [init(rawValue: String)](/documentation/homekit/hmsignificantevent/init(rawvalue:))
- [HMSignificantTimeEvent](/documentation/homekit/hmsignificanttimeevent)

###### Creating a significant time event

- [init(significantEvent: HMSignificantEvent, offset: DateComponents?)](/documentation/homekit/hmsignificanttimeevent/init(significantevent:offset:))

###### Inspecting a significant time event

- [var significantEvent: HMSignificantEvent](/documentation/homekit/hmsignificanttimeevent/significantevent)
- [var offset: DateComponents?](/documentation/homekit/hmsignificanttimeevent/offset)
- [HMMutableSignificantTimeEvent](/documentation/homekit/hmmutablesignificanttimeevent)

###### Configuring a significant time event

- [var significantEvent: HMSignificantEvent](/documentation/homekit/hmmutablesignificanttimeevent/significantevent)
- [var offset: DateComponents](/documentation/homekit/hmmutablesignificanttimeevent/offset)

###### Durations

- [HMDurationEvent](/documentation/homekit/hmdurationevent)

###### Creating a duration event

- [init(duration: TimeInterval)](/documentation/homekit/hmdurationevent/init(duration:))

###### Inspecting a duration event

- [var duration: TimeInterval](/documentation/homekit/hmdurationevent/duration)
- [HMMutableDurationEvent](/documentation/homekit/hmmutabledurationevent)

###### Configuring a duration event

- [var duration: TimeInterval](/documentation/homekit/hmmutabledurationevent/duration)
- [Characteristic events](/documentation/homekit/characteristic-events)

###### Characteristics

- [HMCharacteristicEvent](/documentation/homekit/hmcharacteristicevent)

###### Creating a characteristic event

- [init(characteristic: HMCharacteristic, triggerValue: TriggerValueType?)](/documentation/homekit/hmcharacteristicevent/init(characteristic:triggervalue:))

###### Inspecting the event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicevent/characteristic)
- [var triggerValue: TriggerValueType?](/documentation/homekit/hmcharacteristicevent/triggervalue)

###### Configuring the event

- [func updateTriggerValue(TriggerValueType?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristicevent/updatetriggervalue(_:completionhandler:))
- [HMMutableCharacteristicEvent](/documentation/homekit/hmmutablecharacteristicevent)

###### Configuring the event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmmutablecharacteristicevent/characteristic)
- [var triggerValue: TriggerValueType?](/documentation/homekit/hmmutablecharacteristicevent/triggervalue)

###### Characteristic ranges

- [HMNumberRange](/documentation/homekit/hmnumberrange)

###### Creating a number range

- [convenience init(minValue: NSNumber, maxValue: NSNumber)](/documentation/homekit/hmnumberrange/init(minvalue:maxvalue:))
- [convenience init(minValue: NSNumber)](/documentation/homekit/hmnumberrange/init(minvalue:))
- [convenience init(maxValue: NSNumber)](/documentation/homekit/hmnumberrange/init(maxvalue:))

###### Inspecting a number range

- [var minValue: NSNumber?](/documentation/homekit/hmnumberrange/minvalue)
- [var maxValue: NSNumber?](/documentation/homekit/hmnumberrange/maxvalue)
- [HMCharacteristicThresholdRangeEvent](/documentation/homekit/hmcharacteristicthresholdrangeevent)

###### Creating a characteristic threshold range event

- [init(characteristic: HMCharacteristic, thresholdRange: HMNumberRange)](/documentation/homekit/hmcharacteristicthresholdrangeevent/init(characteristic:thresholdrange:))

###### Inspecting a characteristic threshold event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicthresholdrangeevent/characteristic)
- [var thresholdRange: HMNumberRange](/documentation/homekit/hmcharacteristicthresholdrangeevent/thresholdrange)
- [HMMutableCharacteristicThresholdRangeEvent](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent)

###### Configuring a characteristic threshold event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent/characteristic)
- [var thresholdRange: HMNumberRange](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent/thresholdrange)
- [Presence events](/documentation/homekit/presence-events)

###### User presence

- [HMPresenceEvent](/documentation/homekit/hmpresenceevent)

###### Creating a presence event

- [init(presenceEventType: HMPresenceEventType, presenceUserType: HMPresenceEventUserType)](/documentation/homekit/hmpresenceevent/init(presenceeventtype:presenceusertype:))

###### Inspecting a presence event

- [var presenceEventType: HMPresenceEventType](/documentation/homekit/hmpresenceevent/presenceeventtype)
- [var presenceUserType: HMPresenceEventUserType](/documentation/homekit/hmpresenceevent/presenceusertype)
- [HMMutablePresenceEvent](/documentation/homekit/hmmutablepresenceevent)

###### Configuring a presence event

- [var presenceEventType: HMPresenceEventType](/documentation/homekit/hmmutablepresenceevent/presenceeventtype)
- [var presenceUserType: HMPresenceEventUserType](/documentation/homekit/hmmutablepresenceevent/presenceusertype)
- [HMPresenceEventType](/documentation/homekit/hmpresenceeventtype)

###### Specifying presence type

- [case everyEntry](/documentation/homekit/hmpresenceeventtype/everyentry)
- [case everyExit](/documentation/homekit/hmpresenceeventtype/everyexit)
- [case firstEntry](/documentation/homekit/hmpresenceeventtype/firstentry)
- [case lastExit](/documentation/homekit/hmpresenceeventtype/lastexit)

###### Using presence as a predicate

- [static var atHome: HMPresenceEventType](/documentation/homekit/hmpresenceeventtype/athome)
- [static var notAtHome: HMPresenceEventType](/documentation/homekit/hmpresenceeventtype/notathome)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmpresenceeventtype/init(rawvalue:))
- [HMPresenceEventUserType](/documentation/homekit/hmpresenceeventusertype)

###### Selecting users

- [case currentUser](/documentation/homekit/hmpresenceeventusertype/currentuser)
- [case homeUsers](/documentation/homekit/hmpresenceeventusertype/homeusers)
- [case customUsers](/documentation/homekit/hmpresenceeventusertype/customusers)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmpresenceeventusertype/init(rawvalue:))
- [HMEvent](/documentation/homekit/hmevent)

###### Getting information about the event

- [var uniqueIdentifier: UUID](/documentation/homekit/hmevent/uniqueidentifier)
- [class func isSupported(for: HMHome) -> Bool](/documentation/homekit/hmevent/issupported(for:))

###### Initializers

- [init()](/documentation/homekit/hmevent/init())

###### Type Methods

- [class func new() -> Self](/documentation/homekit/hmevent/new())

##### Restoring the previous scene after an event

- [var endEvents: [HMEvent]](/documentation/homekit/hmeventtrigger/endevents)
- [func updateEndEvents([HMEvent], completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateendevents(_:completionhandler:))

##### Controlling recurrence

- [var recurrences: [DateComponents]?](/documentation/homekit/hmeventtrigger/recurrences)
- [func updateRecurrences([DateComponents]?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updaterecurrences(_:completionhandler:))
- [var executeOnce: Bool](/documentation/homekit/hmeventtrigger/executeonce)
- [func updateExecuteOnce(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateexecuteonce(_:completionhandler:))

##### Adding a trigger condition

- [var predicate: NSPredicate?](/documentation/homekit/hmeventtrigger/predicate)
- [func updatePredicate(NSPredicate?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updatepredicate(_:completionhandler:))

##### Creating predicates

- [class func predicateForEvaluatingTriggerOccurring(beforeSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurring(beforesignificantevent:))
- [class func predicateForEvaluatingTriggerOccurring(afterSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurring(aftersignificantevent:))
- [class func predicate(forEvaluatingTriggerOccurringBetweenSignificantEvent: HMSignificantTimeEvent, secondSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicate(forevaluatingtriggeroccurringbetweensignificantevent:secondsignificantevent:))
- [class func predicateForEvaluatingTrigger(occurringBefore: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringbefore:))
- [class func predicateForEvaluatingTrigger(occurringOn: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringon:))
- [class func predicateForEvaluatingTrigger(occurringAfter: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringafter:))
- [class func predicateForEvaluatingTriggerOccurringBetweenDate(with: DateComponents, secondDateWith: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurringbetweendate(with:seconddatewith:))
- [class func predicateForEvaluatingTrigger(HMCharacteristic, relatedBy: NSComparisonPredicate.Operator, toValue: Any) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(_:relatedby:tovalue:))
- [class func predicateForEvaluatingTrigger(withPresence: HMPresenceEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(withpresence:))
- [let HMCharacteristicKeyPath: String](/documentation/homekit/hmcharacteristickeypath)
- [let HMCharacteristicValueKeyPath: String](/documentation/homekit/hmcharacteristicvaluekeypath)
- [let HMPresenceKeyPath: String](/documentation/homekit/hmpresencekeypath)

##### Deprecated symbols

- [func addEvent(HMEvent, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/addevent(_:completionhandler:))
- [func removeEvent(HMEvent, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/removeevent(_:completionhandler:))
- [class func predicateForEvaluatingTrigger(occurringBefore: String, applyingOffset: DateComponents?) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringbefore:applyingoffset:))
- [class func predicateForEvaluatingTrigger(occurringAfter: String, applyingOffset: DateComponents?) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringafter:applyingoffset:))
- [HMTrigger](/documentation/homekit/hmtrigger)

##### Managing Triggers

- [var name: String](/documentation/homekit/hmtrigger/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtrigger/updatename(_:completionhandler:))
- [var isEnabled: Bool](/documentation/homekit/hmtrigger/isenabled)
- [func enable(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtrigger/enable(_:completionhandler:))
- [var lastFireDate: Date?](/documentation/homekit/hmtrigger/lastfiredate)
- [var uniqueIdentifier: UUID](/documentation/homekit/hmtrigger/uniqueidentifier)

##### Managing Action Sets

- [var actionSets: [HMActionSet]](/documentation/homekit/hmtrigger/actionsets)
- [func addActionSet(HMActionSet, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtrigger/addactionset(_:completionhandler:))
- [func removeActionSet(HMActionSet, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtrigger/removeactionset(_:completionhandler:))

#### Managing users

- [func manageUsers(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/manageusers(completionhandler:))
- [var currentUser: HMUser](/documentation/homekit/hmhome/currentuser)
- [HMUser](/documentation/homekit/hmuser)

##### Getting Information About the User

- [var name: String](/documentation/homekit/hmuser/name)
- [var uniqueIdentifier: UUID](/documentation/homekit/hmuser/uniqueidentifier)

#### Controlling user access

- [func homeAccessControl(for: HMUser) -> HMHomeAccessControl](/documentation/homekit/hmhome/homeaccesscontrol(for:))
- [HMHomeAccessControl](/documentation/homekit/hmhomeaccesscontrol)

##### Getting the Privileges of a User

- [var isAdministrator: Bool](/documentation/homekit/hmhomeaccesscontrol/isadministrator)
- [HMAccessControl](/documentation/homekit/hmaccesscontrol)
- [let HMUserFailedAccessoriesKey: String](/documentation/homekit/hmuserfailedaccessorieskey)

#### Deprecated symbols

- [var users: [HMUser]](/documentation/homekit/hmhome/users)
- [func addUser(completionHandler: (HMUser?, (any Error)?) -> Void)](/documentation/homekit/hmhome/adduser(completionhandler:))
- [func removeUser(HMUser, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhome/removeuser(_:completionhandler:))

#### Instance Properties

- [var matterControllerID: String](/documentation/homekit/hmhome/mattercontrollerid)
- [var matterControllerXPCConnectBlock: () -> NSXPCConnection](/documentation/homekit/hmhome/mattercontrollerxpcconnectblock)
- [var matterStartupParametersXPCConnectBlock: () -> NSXPCConnection](/documentation/homekit/hmhome/matterstartupparametersxpcconnectblock)

### Keeping track of connected homes

- [var delegate: (any HMHomeManagerDelegate)?](/documentation/homekit/hmhomemanager/delegate)
- [HMHomeManagerDelegate](/documentation/homekit/hmhomemanagerdelegate)

#### Adding and removing homes

- [func homeManagerDidUpdateHomes(HMHomeManager)](/documentation/homekit/hmhomemanagerdelegate/homemanagerdidupdatehomes(_:))
- [func homeManager(HMHomeManager, didAdd: HMHome)](/documentation/homekit/hmhomemanagerdelegate/homemanager(_:didadd:))
- [func homeManager(HMHomeManager, didRemove: HMHome)](/documentation/homekit/hmhomemanagerdelegate/homemanager(_:didremove:))
- [func homeManagerDidUpdatePrimaryHome(HMHomeManager)](/documentation/homekit/hmhomemanagerdelegate/homemanagerdidupdateprimaryhome(_:))

#### Adding accessories

- [func homeManager(HMHomeManager, didReceiveAddAccessoryRequest: HMAddAccessoryRequest)](/documentation/homekit/hmhomemanagerdelegate/homemanager(_:didreceiveaddaccessoryrequest:))
- [HMAddAccessoryRequest](/documentation/homekit/hmaddaccessoryrequest)

##### Characterizing the Request

- [var home: HMHome](/documentation/homekit/hmaddaccessoryrequest/home)
- [var accessoryCategory: HMAccessoryCategory](/documentation/homekit/hmaddaccessoryrequest/accessorycategory)
- [var accessoryName: String](/documentation/homekit/hmaddaccessoryrequest/accessoryname)
- [var requiresOwnershipToken: Bool](/documentation/homekit/hmaddaccessoryrequest/requiresownershiptoken)
- [var requiresSetupPayloadURL: Bool](/documentation/homekit/hmaddaccessoryrequest/requiressetuppayloadurl)

##### Creating a Payload

- [func makePayload(ownershipToken: HMAccessoryOwnershipToken) -> HMAccessorySetupPayload?](/documentation/homekit/hmaddaccessoryrequest/makepayload(ownershiptoken:))
- [func makePayload(url: URL, ownershipToken: HMAccessoryOwnershipToken) -> HMAccessorySetupPayload?](/documentation/homekit/hmaddaccessoryrequest/makepayload(url:ownershiptoken:))

##### Initializers

- [init()](/documentation/homekit/hmaddaccessoryrequest/init())

#### Monitoring authorization status

- [func homeManager(HMHomeManager, didUpdate: HMHomeManagerAuthorizationStatus)](/documentation/homekit/hmhomemanagerdelegate/homemanager(_:didupdate:))

### Adding and removing homes

- [func addHome(withName: String, completionHandler: (HMHome?, (any Error)?) -> Void)](/documentation/homekit/hmhomemanager/addhome(withname:completionhandler:))
- [func removeHome(HMHome, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhomemanager/removehome(_:completionhandler:))

### Managing the primary home

- [var primaryHome: HMHome?](/documentation/homekit/hmhomemanager/primaryhome)
- [func updatePrimaryHome(HMHome, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmhomemanager/updateprimaryhome(_:completionhandler:))

### Initializers

- [init()](/documentation/homekit/hmhomemanager/init())

### Instance Methods

- [func findVendorAccessory(hapPublicKey: Data, completionHandler: (HMAccessory?, (any Error)?) -> Void)](/documentation/homekit/hmhomemanager/findvendoraccessory(happublickey:completionhandler:))

## Accessories

- [HMAccessorySetupManager](/documentation/homekit/hmaccessorysetupmanager)

### Adding accessories

- [func performAccessorySetup(using: HMAccessorySetupRequest, completionHandler: (HMAccessorySetupResult?, (any Error)?) -> Void)](/documentation/homekit/hmaccessorysetupmanager/performaccessorysetup(using:completionhandler:))

### Initializers

- [init()](/documentation/homekit/hmaccessorysetupmanager/init())
- [HMAccessorySetupResult](/documentation/homekit/hmaccessorysetupresult)

### Getting results

- [var accessoryUniqueIdentifiers: [UUID]](/documentation/homekit/hmaccessorysetupresult/accessoryuniqueidentifiers)
- [var homeUniqueIdentifier: UUID](/documentation/homekit/hmaccessorysetupresult/homeuniqueidentifier)
- [HMAccessorySetupRequest](/documentation/homekit/hmaccessorysetuprequest)

### Setting up accessorices

- [var homeUniqueIdentifier: UUID?](/documentation/homekit/hmaccessorysetuprequest/homeuniqueidentifier)
- [var payload: HMAccessorySetupPayload?](/documentation/homekit/hmaccessorysetuprequest/payload)
- [var suggestedAccessoryName: String?](/documentation/homekit/hmaccessorysetuprequest/suggestedaccessoryname)
- [var suggestedRoomUniqueIdentifier: UUID?](/documentation/homekit/hmaccessorysetuprequest/suggestedroomuniqueidentifier)

### Instance Properties

- [var matterPayload: MTRSetupPayload?](/documentation/homekit/hmaccessorysetuprequest/matterpayload)

### Initializers

- [init()](/documentation/homekit/hmaccessorysetuprequest/init())
- [Interacting with a home automation network](/documentation/homekit/interacting-with-a-home-automation-network)
- [HMAccessory](/documentation/homekit/hmaccessory)

### Tracking changes to an accessory

- [var delegate: (any HMAccessoryDelegate)?](/documentation/homekit/hmaccessory/delegate)
- [HMAccessoryDelegate](/documentation/homekit/hmaccessorydelegate)

#### Observing accessories

- [func accessoryDidUpdateName(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdatename(_:))
- [func accessoryDidUpdateReachability(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdatereachability(_:))
- [func accessoryDidUpdateServices(HMAccessory)](/documentation/homekit/hmaccessorydelegate/accessorydidupdateservices(_:))
- [func accessory(HMAccessory, didUpdateNameFor: HMService)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdatenamefor:))
- [func accessory(HMAccessory, service: HMService, didUpdateValueFor: HMCharacteristic)](/documentation/homekit/hmaccessorydelegate/accessory(_:service:didupdatevaluefor:))
- [func accessory(HMAccessory, didUpdateAssociatedServiceTypeFor: HMService)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdateassociatedservicetypefor:))
- [func accessory(HMAccessory, didAdd: HMAccessoryProfile)](/documentation/homekit/hmaccessorydelegate/accessory(_:didadd:))
- [func accessory(HMAccessory, didRemove: HMAccessoryProfile)](/documentation/homekit/hmaccessorydelegate/accessory(_:didremove:))
- [func accessory(HMAccessory, didUpdateFirmwareVersion: String)](/documentation/homekit/hmaccessorydelegate/accessory(_:didupdatefirmwareversion:))

### Identifying an Accessory

- [var name: String](/documentation/homekit/hmaccessory/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmaccessory/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmaccessory/uniqueidentifier)
- [var identifier: UUID](/documentation/homekit/hmaccessory/identifier)

### Categorizing an accessory

- [var category: HMAccessoryCategory](/documentation/homekit/hmaccessory/category)
- [HMAccessoryCategory](/documentation/homekit/hmaccessorycategory)

#### Reading the category type

- [var categoryType: String](/documentation/homekit/hmaccessorycategory/categorytype)
- [Accessory Category Types](/documentation/homekit/accessory-category-types)

##### Light

- [let HMAccessoryCategoryTypeLightbulb: String](/documentation/homekit/hmaccessorycategorytypelightbulb)

##### Power and switches

- [let HMAccessoryCategoryTypeOutlet: String](/documentation/homekit/hmaccessorycategorytypeoutlet)
- [let HMAccessoryCategoryTypeProgrammableSwitch: String](/documentation/homekit/hmaccessorycategorytypeprogrammableswitch)
- [let HMAccessoryCategoryTypeSwitch: String](/documentation/homekit/hmaccessorycategorytypeswitch)

##### Air quality and smoke detection

- [let HMAccessoryCategoryTypeFan: String](/documentation/homekit/hmaccessorycategorytypefan)
- [let HMAccessoryCategoryTypeAirPurifier: String](/documentation/homekit/hmaccessorycategorytypeairpurifier)

##### Temperature and humidity

- [let HMAccessoryCategoryTypeThermostat: String](/documentation/homekit/hmaccessorycategorytypethermostat)
- [let HMAccessoryCategoryTypeAirConditioner: String](/documentation/homekit/hmaccessorycategorytypeairconditioner)
- [let HMAccessoryCategoryTypeAirDehumidifier: String](/documentation/homekit/hmaccessorycategorytypeairdehumidifier)
- [let HMAccessoryCategoryTypeAirHeater: String](/documentation/homekit/hmaccessorycategorytypeairheater)
- [let HMAccessoryCategoryTypeAirHumidifier: String](/documentation/homekit/hmaccessorycategorytypeairhumidifier)

##### Windows

- [let HMAccessoryCategoryTypeWindow: String](/documentation/homekit/hmaccessorycategorytypewindow)
- [let HMAccessoryCategoryTypeWindowCovering: String](/documentation/homekit/hmaccessorycategorytypewindowcovering)

##### Locks and openers

- [let HMAccessoryCategoryTypeDoor: String](/documentation/homekit/hmaccessorycategorytypedoor)
- [let HMAccessoryCategoryTypeDoorLock: String](/documentation/homekit/hmaccessorycategorytypedoorlock)
- [let HMAccessoryCategoryTypeGarageDoorOpener: String](/documentation/homekit/hmaccessorycategorytypegaragedooropener)
- [let HMAccessoryCategoryTypeVideoDoorbell: String](/documentation/homekit/hmaccessorycategorytypevideodoorbell)

##### Safety and security

- [let HMAccessoryCategoryTypeSensor: String](/documentation/homekit/hmaccessorycategorytypesensor)
- [let HMAccessoryCategoryTypeSecuritySystem: String](/documentation/homekit/hmaccessorycategorytypesecuritysystem)

##### Cameras

- [let HMAccessoryCategoryTypeIPCamera: String](/documentation/homekit/hmaccessorycategorytypeipcamera)

##### Water

- [let HMAccessoryCategoryTypeSprinkler: String](/documentation/homekit/hmaccessorycategorytypesprinkler)
- [let HMAccessoryCategoryTypeFaucet: String](/documentation/homekit/hmaccessorycategorytypefaucet)
- [let HMAccessoryCategoryTypeShowerHead: String](/documentation/homekit/hmaccessorycategorytypeshowerhead)

##### Network

- [let HMAccessoryCategoryTypeBridge: String](/documentation/homekit/hmaccessorycategorytypebridge)
- [let HMAccessoryCategoryTypeRangeExtender: String](/documentation/homekit/hmaccessorycategorytyperangeextender)
- [let HMAccessoryCategoryTypeAirPort: String](/documentation/homekit/hmaccessorycategorytypeairport)
- [let HMAccessoryCategoryTypeWiFiRouter: String](/documentation/homekit/hmaccessorycategorytypewifirouter)

##### Audio and sound

- [let HMAccessoryCategoryTypeAudioReceiver: String](/documentation/homekit/hmaccessorycategorytypeaudioreceiver)
- [let HMAccessoryCategoryTypeSpeaker: String](/documentation/homekit/hmaccessorycategorytypespeaker)

##### Television

- [let HMAccessoryCategoryTypeTelevision: String](/documentation/homekit/hmaccessorycategorytypetelevision)
- [let HMAccessoryCategoryTypeTelevisionSetTopBox: String](/documentation/homekit/hmaccessorycategorytypetelevisionsettopbox)
- [let HMAccessoryCategoryTypeTelevisionStreamingStick: String](/documentation/homekit/hmaccessorycategorytypetelevisionstreamingstick)

##### Uncategorized

- [let HMAccessoryCategoryTypeOther: String](/documentation/homekit/hmaccessorycategorytypeother)

#### Describing the category

- [var localizedDescription: String](/documentation/homekit/hmaccessorycategory/localizeddescription)

### Locating an accessory

- [var room: HMRoom?](/documentation/homekit/hmaccessory/room)
- [HMRoom](/documentation/homekit/hmroom)

#### Identifying a room

- [var name: String](/documentation/homekit/hmroom/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmroom/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmroom/uniqueidentifier)

#### Finding accessories

- [var accessories: [HMAccessory]](/documentation/homekit/hmroom/accessories)

### Managing accessory profiles

- [var profiles: [HMAccessoryProfile]](/documentation/homekit/hmaccessory/profiles)
- [HMAccessoryProfile](/documentation/homekit/hmaccessoryprofile)

#### Getting information about a profile

- [var accessory: HMAccessory?](/documentation/homekit/hmaccessoryprofile/accessory)
- [var services: [HMService]](/documentation/homekit/hmaccessoryprofile/services)
- [var uniqueIdentifier: UUID](/documentation/homekit/hmaccessoryprofile/uniqueidentifier)
- [HMNetworkConfigurationProfile](/documentation/homekit/hmnetworkconfigurationprofile)

#### Restricting network access

- [var isNetworkAccessRestricted: Bool](/documentation/homekit/hmnetworkconfigurationprofile/isnetworkaccessrestricted)

#### Listening for access changes

- [var delegate: (any HMNetworkConfigurationProfileDelegate)?](/documentation/homekit/hmnetworkconfigurationprofile/delegate)
- [HMNetworkConfigurationProfileDelegate](/documentation/homekit/hmnetworkconfigurationprofiledelegate)

##### Observing network access changes

- [func profileDidUpdateNetworkAccessMode(HMNetworkConfigurationProfile)](/documentation/homekit/hmnetworkconfigurationprofiledelegate/profiledidupdatenetworkaccessmode(_:))
- [HMCameraProfile](/documentation/homekit/hmcameraprofile)

#### Controlling camera settings

- [var settingsControl: HMCameraSettingsControl?](/documentation/homekit/hmcameraprofile/settingscontrol)
- [HMCameraSettingsControl](/documentation/homekit/hmcamerasettingscontrol)

##### Controlling camera characteristics

- [var currentHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currenthorizontaltilt)
- [var targetHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targethorizontaltilt)
- [var currentVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currentverticaltilt)
- [var targetVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targetverticaltilt)
- [var opticalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/opticalzoom)
- [var digitalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/digitalzoom)
- [var imageMirroring: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagemirroring)
- [var imageRotation: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagerotation)
- [var nightVision: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/nightvision)
- [HMCameraControl](/documentation/homekit/hmcameracontrol)

##### Initializers

- [init()](/documentation/homekit/hmcameracontrol/init())

#### Playing audio

- [var microphoneControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/microphonecontrol)
- [var speakerControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/speakercontrol)
- [HMCameraAudioControl](/documentation/homekit/hmcameraaudiocontrol)

##### Controlling audio characteristics

- [var mute: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/mute)
- [var volume: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/volume)

#### Streaming

- [var streamControl: HMCameraStreamControl?](/documentation/homekit/hmcameraprofile/streamcontrol)
- [HMCameraStreamControl](/documentation/homekit/hmcamerastreamcontrol)

##### Controlling the stream

- [func startStream()](/documentation/homekit/hmcamerastreamcontrol/startstream())
- [func stopStream()](/documentation/homekit/hmcamerastreamcontrol/stopstream())
- [var cameraStream: HMCameraStream?](/documentation/homekit/hmcamerastreamcontrol/camerastream)
- [HMCameraStream](/documentation/homekit/hmcamerastream)

###### Configuring the audio stream

- [var audioStreamSetting: HMCameraAudioStreamSetting](/documentation/homekit/hmcamerastream/audiostreamsetting)
- [func updateAudioStreamSetting(HMCameraAudioStreamSetting, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcamerastream/updateaudiostreamsetting(_:completionhandler:))
- [func setAudioStreamSetting(HMCameraAudioStreamSetting)](/documentation/homekit/hmcamerastream/setaudiostreamsetting(_:))
- [HMCameraAudioStreamSetting](/documentation/homekit/hmcameraaudiostreamsetting)

###### Configuring the Audio Stream

- [case muted](/documentation/homekit/hmcameraaudiostreamsetting/muted)
- [case incomingAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/incomingaudioallowed)
- [case bidirectionalAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/bidirectionalaudioallowed)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcameraaudiostreamsetting/init(rawvalue:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastream/init())
- [var streamState: HMCameraStreamState](/documentation/homekit/hmcamerastreamcontrol/streamstate)
- [HMCameraStreamState](/documentation/homekit/hmcamerastreamstate)

###### Observing the streaming state

- [case notStreaming](/documentation/homekit/hmcamerastreamstate/notstreaming)
- [case starting](/documentation/homekit/hmcamerastreamstate/starting)
- [case stopping](/documentation/homekit/hmcamerastreamstate/stopping)
- [case streaming](/documentation/homekit/hmcamerastreamstate/streaming)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcamerastreamstate/init(rawvalue:))

##### Observing stream activity

- [var delegate: (any HMCameraStreamControlDelegate)?](/documentation/homekit/hmcamerastreamcontrol/delegate)
- [HMCameraStreamControlDelegate](/documentation/homekit/hmcamerastreamcontroldelegate)

###### Observing stream activity

- [func cameraStreamControlDidStartStream(HMCameraStreamControl)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontroldidstartstream(_:))
- [func cameraStreamControl(HMCameraStreamControl, didStopStreamWithError: (any Error)?)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontrol(_:didstopstreamwitherror:))

##### Initializers

- [init()](/documentation/homekit/hmcamerastreamcontrol/init())

#### Capturing snapshots

- [var snapshotControl: HMCameraSnapshotControl?](/documentation/homekit/hmcameraprofile/snapshotcontrol)
- [HMCameraSnapshotControl](/documentation/homekit/hmcamerasnapshotcontrol)

##### Taking snapshots

- [func takeSnapshot()](/documentation/homekit/hmcamerasnapshotcontrol/takesnapshot())
- [var mostRecentSnapshot: HMCameraSnapshot?](/documentation/homekit/hmcamerasnapshotcontrol/mostrecentsnapshot)
- [HMCameraSnapshot](/documentation/homekit/hmcamerasnapshot)

###### Accessing snapshot properties

- [var captureDate: Date](/documentation/homekit/hmcamerasnapshot/capturedate)

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshot/init())

##### Observing snapshot activity

- [var delegate: (any HMCameraSnapshotControlDelegate)?](/documentation/homekit/hmcamerasnapshotcontrol/delegate)
- [HMCameraSnapshotControlDelegate](/documentation/homekit/hmcamerasnapshotcontroldelegate)

###### Observing snapshot activity

- [func cameraSnapshotControl(HMCameraSnapshotControl, didTake: HMCameraSnapshot?, error: (any Error)?)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontrol(_:didtake:error:))
- [func cameraSnapshotControlDidUpdateMostRecentSnapshot(HMCameraSnapshotControl)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontroldidupdatemostrecentsnapshot(_:))

##### Initializers

- [init()](/documentation/homekit/hmcamerasnapshotcontrol/init())

### Managing camera profiles

- [CameraView](/documentation/homekit/cameraview)

#### Creating a camera view

- [init(source: HMCameraSource)](/documentation/homekit/cameraview/init(source:))
- [HMCameraSource](/documentation/homekit/hmcamerasource)

##### Getting the properties

- [var aspectRatio: Double](/documentation/homekit/hmcamerasource/aspectratio)

##### Initializers

- [init()](/documentation/homekit/hmcamerasource/init())
- [var cameraProfiles: [HMCameraProfile]?](/documentation/homekit/hmaccessory/cameraprofiles)
- [HMCameraProfile](/documentation/homekit/hmcameraprofile)

#### Controlling camera settings

- [var settingsControl: HMCameraSettingsControl?](/documentation/homekit/hmcameraprofile/settingscontrol)
- [HMCameraSettingsControl](/documentation/homekit/hmcamerasettingscontrol)

##### Controlling camera characteristics

- [var currentHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currenthorizontaltilt)
- [var targetHorizontalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targethorizontaltilt)
- [var currentVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/currentverticaltilt)
- [var targetVerticalTilt: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/targetverticaltilt)
- [var opticalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/opticalzoom)
- [var digitalZoom: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/digitalzoom)
- [var imageMirroring: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagemirroring)
- [var imageRotation: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/imagerotation)
- [var nightVision: HMCharacteristic?](/documentation/homekit/hmcamerasettingscontrol/nightvision)
- [HMCameraControl](/documentation/homekit/hmcameracontrol)

##### Initializers

- [init()](/documentation/homekit/hmcameracontrol/init())

#### Playing audio

- [var microphoneControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/microphonecontrol)
- [var speakerControl: HMCameraAudioControl?](/documentation/homekit/hmcameraprofile/speakercontrol)
- [HMCameraAudioControl](/documentation/homekit/hmcameraaudiocontrol)

##### Controlling audio characteristics

- [var mute: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/mute)
- [var volume: HMCharacteristic?](/documentation/homekit/hmcameraaudiocontrol/volume)

#### Streaming

- [var streamControl: HMCameraStreamControl?](/documentation/homekit/hmcameraprofile/streamcontrol)
- [HMCameraStreamControl](/documentation/homekit/hmcamerastreamcontrol)

##### Controlling the stream

- [func startStream()](/documentation/homekit/hmcamerastreamcontrol/startstream())
- [func stopStream()](/documentation/homekit/hmcamerastreamcontrol/stopstream())
- [var cameraStream: HMCameraStream?](/documentation/homekit/hmcamerastreamcontrol/camerastream)
- [HMCameraStream](/documentation/homekit/hmcamerastream)

###### Configuring the audio stream

- [var audioStreamSetting: HMCameraAudioStreamSetting](/documentation/homekit/hmcamerastream/audiostreamsetting)
- [func updateAudioStreamSetting(HMCameraAudioStreamSetting, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcamerastream/updateaudiostreamsetting(_:completionhandler:))
- [func setAudioStreamSetting(HMCameraAudioStreamSetting)](/documentation/homekit/hmcamerastream/setaudiostreamsetting(_:))
- [HMCameraAudioStreamSetting](/documentation/homekit/hmcameraaudiostreamsetting)

###### Configuring the Audio Stream

- [case muted](/documentation/homekit/hmcameraaudiostreamsetting/muted)
- [case incomingAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/incomingaudioallowed)
- [case bidirectionalAudioAllowed](/documentation/homekit/hmcameraaudiostreamsetting/bidirectionalaudioallowed)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcameraaudiostreamsetting/init(rawvalue:))

###### Initializers

- [init()](/documentation/homekit/hmcamerastream/init())
- [var streamState: HMCameraStreamState](/documentation/homekit/hmcamerastreamcontrol/streamstate)
- [HMCameraStreamState](/documentation/homekit/hmcamerastreamstate)

###### Observing the streaming state

- [case notStreaming](/documentation/homekit/hmcamerastreamstate/notstreaming)
- [case starting](/documentation/homekit/hmcamerastreamstate/starting)
- [case stopping](/documentation/homekit/hmcamerastreamstate/stopping)
- [case streaming](/documentation/homekit/hmcamerastreamstate/streaming)

###### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmcamerastreamstate/init(rawvalue:))

##### Observing stream activity

- [var delegate: (any HMCameraStreamControlDelegate)?](/documentation/homekit/hmcamerastreamcontrol/delegate)
- [HMCameraStreamControlDelegate](/documentation/homekit/hmcamerastreamcontroldelegate)

###### Observing stream activity

- [func cameraStreamControlDidStartStream(HMCameraStreamControl)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontroldidstartstream(_:))
- [func cameraStreamControl(HMCameraStreamControl, didStopStreamWithError: (any Error)?)](/documentation/homekit/hmcamerastreamcontroldelegate/camerastreamcontrol(_:didstopstreamwitherror:))

##### Initializers

- [init()](/documentation/homekit/hmcamerastreamcontrol/init())

#### Capturing snapshots

- [var snapshotControl: HMCameraSnapshotControl?](/documentation/homekit/hmcameraprofile/snapshotcontrol)
- [HMCameraSnapshotControl](/documentation/homekit/hmcamerasnapshotcontrol)

##### Taking snapshots

- [func takeSnapshot()](/documentation/homekit/hmcamerasnapshotcontrol/takesnapshot())
- [var mostRecentSnapshot: HMCameraSnapshot?](/documentation/homekit/hmcamerasnapshotcontrol/mostrecentsnapshot)
- [HMCameraSnapshot](/documentation/homekit/hmcamerasnapshot)

###### Accessing snapshot properties

- [var captureDate: Date](/documentation/homekit/hmcamerasnapshot/capturedate)

###### Initializers

- [init()](/documentation/homekit/hmcamerasnapshot/init())

##### Observing snapshot activity

- [var delegate: (any HMCameraSnapshotControlDelegate)?](/documentation/homekit/hmcamerasnapshotcontrol/delegate)
- [HMCameraSnapshotControlDelegate](/documentation/homekit/hmcamerasnapshotcontroldelegate)

###### Observing snapshot activity

- [func cameraSnapshotControl(HMCameraSnapshotControl, didTake: HMCameraSnapshot?, error: (any Error)?)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontrol(_:didtake:error:))
- [func cameraSnapshotControlDidUpdateMostRecentSnapshot(HMCameraSnapshotControl)](/documentation/homekit/hmcamerasnapshotcontroldelegate/camerasnapshotcontroldidupdatemostrecentsnapshot(_:))

##### Initializers

- [init()](/documentation/homekit/hmcamerasnapshotcontrol/init())
- [HMCameraView](/documentation/homekit/hmcameraview)

#### Getting the Camera Source

- [var cameraSource: HMCameraSource?](/documentation/homekit/hmcameraview/camerasource)
- [HMCameraSource](/documentation/homekit/hmcamerasource)

##### Getting the properties

- [var aspectRatio: Double](/documentation/homekit/hmcamerasource/aspectratio)

##### Initializers

- [init()](/documentation/homekit/hmcamerasource/init())

#### Initializers

- [init()](/documentation/homekit/hmcameraview/init())

### Getting accessory state

- [var isReachable: Bool](/documentation/homekit/hmaccessory/isreachable)
- [var isBlocked: Bool](/documentation/homekit/hmaccessory/isblocked)

### Asking an accessory to identify itself

- [var supportsIdentify: Bool](/documentation/homekit/hmaccessory/supportsidentify)
- [func identify(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmaccessory/identify(completionhandler:))

### Controlling accessory features

- [var services: [HMService]](/documentation/homekit/hmaccessory/services)
- [HMService](/documentation/homekit/hmservice)

#### Getting service characteristics

- [var characteristics: [HMCharacteristic]](/documentation/homekit/hmservice/characteristics)
- [HMCharacteristic](/documentation/homekit/hmcharacteristic)

##### Identifying a characteristic

- [var uniqueIdentifier: UUID](/documentation/homekit/hmcharacteristic/uniqueidentifier)
- [var localizedDescription: String](/documentation/homekit/hmcharacteristic/localizeddescription)

##### Reading characteristic properties

- [var properties: [String]](/documentation/homekit/hmcharacteristic/properties)
- [Characteristic Properties](/documentation/homekit/characteristic-properties)

###### Properties of Characteristics

- [let HMCharacteristicPropertyReadable: String](/documentation/homekit/hmcharacteristicpropertyreadable)
- [let HMCharacteristicPropertyWritable: String](/documentation/homekit/hmcharacteristicpropertywritable)
- [let HMCharacteristicPropertyHidden: String](/documentation/homekit/hmcharacteristicpropertyhidden)

##### Determining what a characteristic controls

- [var characteristicType: String](/documentation/homekit/hmcharacteristic/characteristictype)
- [Characteristic types](/documentation/homekit/characteristic-types)

###### Light

- [let HMCharacteristicTypeCurrentLightLevel: String](/documentation/homekit/hmcharacteristictypecurrentlightlevel)
- [let HMCharacteristicTypeHue: String](/documentation/homekit/hmcharacteristictypehue)
- [let HMCharacteristicTypeBrightness: String](/documentation/homekit/hmcharacteristictypebrightness)
- [let HMCharacteristicTypeSaturation: String](/documentation/homekit/hmcharacteristictypesaturation)
- [let HMCharacteristicTypeColorTemperature: String](/documentation/homekit/hmcharacteristictypecolortemperature)

###### Power and switches

- [let HMCharacteristicTypeBatteryLevel: String](/documentation/homekit/hmcharacteristictypebatterylevel)
- [let HMCharacteristicTypeChargingState: String](/documentation/homekit/hmcharacteristictypechargingstate)

###### Values

- [HMCharacteristicValueChargingState](/documentation/homekit/hmcharacteristicvaluechargingstate)

###### Charging States

- [case none](/documentation/homekit/hmcharacteristicvaluechargingstate/none)
- [case inProgress](/documentation/homekit/hmcharacteristicvaluechargingstate/inprogress)
- [case notChargeable](/documentation/homekit/hmcharacteristicvaluechargingstate/notchargeable)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluechargingstate/init(rawvalue:))
- [let HMCharacteristicTypeContactState: String](/documentation/homekit/hmcharacteristictypecontactstate)

###### Values

- [HMCharacteristicValueContactState](/documentation/homekit/hmcharacteristicvaluecontactstate)

###### Contact Sensor State

- [case detected](/documentation/homekit/hmcharacteristicvaluecontactstate/detected)
- [case none](/documentation/homekit/hmcharacteristicvaluecontactstate/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecontactstate/init(rawvalue:))
- [let HMCharacteristicTypeOutletInUse: String](/documentation/homekit/hmcharacteristictypeoutletinuse)
- [let HMCharacteristicTypePowerState: String](/documentation/homekit/hmcharacteristictypepowerstate)
- [let HMCharacteristicTypeStatusLowBattery: String](/documentation/homekit/hmcharacteristictypestatuslowbattery)

###### Values

- [HMCharacteristicValueBatteryStatus](/documentation/homekit/hmcharacteristicvaluebatterystatus)

###### Battery Status

- [case normal](/documentation/homekit/hmcharacteristicvaluebatterystatus/normal)
- [case low](/documentation/homekit/hmcharacteristicvaluebatterystatus/low)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluebatterystatus/init(rawvalue:))
- [let HMCharacteristicTypeOutputState: String](/documentation/homekit/hmcharacteristictypeoutputstate)
- [let HMCharacteristicTypeInputEvent: String](/documentation/homekit/hmcharacteristictypeinputevent)

###### Values

- [HMCharacteristicValueInputEvent](/documentation/homekit/hmcharacteristicvalueinputevent)

###### Input Events

- [case singlePress](/documentation/homekit/hmcharacteristicvalueinputevent/singlepress)
- [case doublePress](/documentation/homekit/hmcharacteristicvalueinputevent/doublepress)
- [case longPress](/documentation/homekit/hmcharacteristicvalueinputevent/longpress)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputevent/init(rawvalue:))
- [let HMCharacteristicTypePowerModeSelection: String](/documentation/homekit/hmcharacteristictypepowermodeselection)

###### Values

- [HMCharacteristicValuePowerModeSelection](/documentation/homekit/hmcharacteristicvaluepowermodeselection)

###### Power mode status

- [case hide](/documentation/homekit/hmcharacteristicvaluepowermodeselection/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluepowermodeselection/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepowermodeselection/init(rawvalue:))

###### Temperature

- [let HMCharacteristicTypeCurrentTemperature: String](/documentation/homekit/hmcharacteristictypecurrenttemperature)
- [let HMCharacteristicTypeTargetTemperature: String](/documentation/homekit/hmcharacteristictypetargettemperature)
- [let HMCharacteristicTypeTemperatureUnits: String](/documentation/homekit/hmcharacteristictypetemperatureunits)

###### Values

- [HMCharacteristicValueTemperatureUnit](/documentation/homekit/hmcharacteristicvaluetemperatureunit)

###### Temperature Units

- [case celsius](/documentation/homekit/hmcharacteristicvaluetemperatureunit/celsius)
- [case fahrenheit](/documentation/homekit/hmcharacteristicvaluetemperatureunit/fahrenheit)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetemperatureunit/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeatingCooling: String](/documentation/homekit/hmcharacteristictypetargetheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeatingCooling: String](/documentation/homekit/hmcharacteristictypecurrentheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [HMCharacteristicValueCurrentHeatingCooling](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling)

###### Temperature States

- [case cool](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/cool)
- [case heat](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/heat)
- [case off](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/off)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypetargetheatercoolerstate)

###### Values

- [HMCharacteristicValueTargetHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate)

###### Target State

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/automatic)
- [case heat](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/heat)
- [case cool](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/cool)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypecurrentheatercoolerstate)

###### Values

- [HMCharacteristicValueCurrentHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate)

###### Current State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/idle)
- [case heating](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/heating)
- [case cooling](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/cooling)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCoolingThreshold: String](/documentation/homekit/hmcharacteristictypecoolingthreshold)
- [let HMCharacteristicTypeHeatingThreshold: String](/documentation/homekit/hmcharacteristictypeheatingthreshold)

###### Humidity

- [let HMCharacteristicTypeCurrentRelativeHumidity: String](/documentation/homekit/hmcharacteristictypecurrentrelativehumidity)
- [let HMCharacteristicTypeTargetRelativeHumidity: String](/documentation/homekit/hmcharacteristictypetargetrelativehumidity)
- [let HMCharacteristicTypeCurrentHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypecurrenthumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueCurrentHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate)

###### Current States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/idle)
- [case humidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/humidifying)
- [case dehumidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/dehumidifying)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypetargethumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueTargetHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate)

###### Target States

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/automatic)
- [case humidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/humidify)
- [case dehumidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/dehumidify)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeHumidifierThreshold: String](/documentation/homekit/hmcharacteristictypehumidifierthreshold)
- [let HMCharacteristicTypeDehumidifierThreshold: String](/documentation/homekit/hmcharacteristictypedehumidifierthreshold)

###### Air quality and smoke detection

- [let HMCharacteristicTypeAirQuality: String](/documentation/homekit/hmcharacteristictypeairquality)

###### Values

- [HMCharacteristicValueAirQuality](/documentation/homekit/hmcharacteristicvalueairquality)

###### Air Quality

- [case unknown](/documentation/homekit/hmcharacteristicvalueairquality/unknown)
- [case excellent](/documentation/homekit/hmcharacteristicvalueairquality/excellent)
- [case good](/documentation/homekit/hmcharacteristicvalueairquality/good)
- [case fair](/documentation/homekit/hmcharacteristicvalueairquality/fair)
- [case inferior](/documentation/homekit/hmcharacteristicvalueairquality/inferior)
- [case poor](/documentation/homekit/hmcharacteristicvalueairquality/poor)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairquality/init(rawvalue:))
- [let HMCharacteristicTypeAirParticulateDensity: String](/documentation/homekit/hmcharacteristictypeairparticulatedensity)
- [let HMCharacteristicTypeAirParticulateSize: String](/documentation/homekit/hmcharacteristictypeairparticulatesize)

###### Values

- [HMCharacteristicValueAirParticulateSize](/documentation/homekit/hmcharacteristicvalueairparticulatesize)

###### Air Particulate Sizes

- [case size2_5](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size2_5)
- [case size10](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size10)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairparticulatesize/init(rawvalue:))
- [let HMCharacteristicTypeSmokeDetected: String](/documentation/homekit/hmcharacteristictypesmokedetected)

###### Values

- [HMCharacteristicValueSmokeDetectionStatus](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus)

###### Smoke Detection Status

- [case none](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideDetected: String](/documentation/homekit/hmcharacteristictypecarbondioxidedetected)

###### Values

- [HMCharacteristicValueCarbonDioxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus)

###### Carbon Dioxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidelevel)
- [let HMCharacteristicTypeCarbonDioxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidepeaklevel)
- [let HMCharacteristicTypeCarbonMonoxideDetected: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidedetected)

###### Values

- [HMCharacteristicValueCarbonMonoxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus)

###### Carbon Monoxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonMonoxideLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidelevel)
- [let HMCharacteristicTypeCarbonMonoxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidepeaklevel)
- [let HMCharacteristicTypeNitrogenDioxideDensity: String](/documentation/homekit/hmcharacteristictypenitrogendioxidedensity)
- [let HMCharacteristicTypeOzoneDensity: String](/documentation/homekit/hmcharacteristictypeozonedensity)
- [let HMCharacteristicTypePM10Density: String](/documentation/homekit/hmcharacteristictypepm10density)
- [let HMCharacteristicTypePM2_5Density: String](/documentation/homekit/hmcharacteristictypepm2_5density)
- [let HMCharacteristicTypeSulphurDioxideDensity: String](/documentation/homekit/hmcharacteristictypesulphurdioxidedensity)
- [let HMCharacteristicTypeVolatileOrganicCompoundDensity: String](/documentation/homekit/hmcharacteristictypevolatileorganiccompounddensity)

###### Fans

- [let HMCharacteristicTypeCurrentFanState: String](/documentation/homekit/hmcharacteristictypecurrentfanstate)

###### Values

- [HMCharacteristicValueCurrentFanState](/documentation/homekit/hmcharacteristicvaluecurrentfanstate)

###### Fan State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetFanState: String](/documentation/homekit/hmcharacteristictypetargetfanstate)

###### Values

- [HMCharacteristicValueTargetFanState](/documentation/homekit/hmcharacteristicvaluetargetfanstate)

###### Fan State

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetfanstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetfanstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetfanstate/init(rawvalue:))
- [let HMCharacteristicTypeRotationDirection: String](/documentation/homekit/hmcharacteristictyperotationdirection)

###### Values

- [HMCharacteristicValueRotationDirection](/documentation/homekit/hmcharacteristicvaluerotationdirection)

###### Rotation

- [case clockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/clockwise)
- [case counterClockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/counterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerotationdirection/init(rawvalue:))
- [let HMCharacteristicTypeRotationSpeed: String](/documentation/homekit/hmcharacteristictyperotationspeed)
- [let HMCharacteristicTypeSwingMode: String](/documentation/homekit/hmcharacteristictypeswingmode)

###### Values

- [HMCharacteristicValueSwingMode](/documentation/homekit/hmcharacteristicvalueswingmode)

###### Movement Mode

- [case disabled](/documentation/homekit/hmcharacteristicvalueswingmode/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueswingmode/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueswingmode/init(rawvalue:))

###### Purifiers and filters

- [let HMCharacteristicTypeCurrentAirPurifierState: String](/documentation/homekit/hmcharacteristictypecurrentairpurifierstate)

###### Values

- [HMCharacteristicValueCurrentAirPurifierState](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate)

###### Air Purifier States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetAirPurifierState: String](/documentation/homekit/hmcharacteristictypetargetairpurifierstate)

###### Values

- [HMCharacteristicValueTargetAirPurifierState](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate)

###### Air Purifier States

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeFilterLifeLevel: String](/documentation/homekit/hmcharacteristictypefilterlifelevel)
- [let HMCharacteristicTypeFilterChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterchangeindication)

###### Values

- [HMCharacteristicValueFilterChange](/documentation/homekit/hmcharacteristicvaluefilterchange)

###### Filter Change Indicator

- [case notNeeded](/documentation/homekit/hmcharacteristicvaluefilterchange/notneeded)
- [case needed](/documentation/homekit/hmcharacteristicvaluefilterchange/needed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluefilterchange/init(rawvalue:))
- [let HMCharacteristicTypeFilterResetChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterresetchangeindication)

###### Water

- [let HMCharacteristicTypeWaterLevel: String](/documentation/homekit/hmcharacteristictypewaterlevel)
- [let HMCharacteristicTypeValveType: String](/documentation/homekit/hmcharacteristictypevalvetype)

###### Values

- [HMCharacteristicValueValveType](/documentation/homekit/hmcharacteristicvaluevalvetype)

###### Valve Types

- [case genericValve](/documentation/homekit/hmcharacteristicvaluevalvetype/genericvalve)
- [case irrigation](/documentation/homekit/hmcharacteristicvaluevalvetype/irrigation)
- [case showerHead](/documentation/homekit/hmcharacteristicvaluevalvetype/showerhead)
- [case waterFaucet](/documentation/homekit/hmcharacteristicvaluevalvetype/waterfaucet)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevalvetype/init(rawvalue:))
- [let HMCharacteristicTypeLeakDetected: String](/documentation/homekit/hmcharacteristictypeleakdetected)

###### Values

- [HMCharacteristicValueLeakStatus](/documentation/homekit/hmcharacteristicvalueleakstatus)

###### Leak Status

- [case none](/documentation/homekit/hmcharacteristicvalueleakstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvalueleakstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueleakstatus/init(rawvalue:))

###### Doors and windows

- [let HMCharacteristicTypeCurrentDoorState: String](/documentation/homekit/hmcharacteristictypecurrentdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetDoorState: String](/documentation/homekit/hmcharacteristictypetargetdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [HMCharacteristicValueTargetDoorState](/documentation/homekit/hmcharacteristicvaluetargetdoorstate)

###### Door States

- [case closed](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/closed)
- [case open](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/open)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentPosition: String](/documentation/homekit/hmcharacteristictypecurrentposition)
- [let HMCharacteristicTypeTargetPosition: String](/documentation/homekit/hmcharacteristictypetargetposition)
- [let HMCharacteristicTypePositionState: String](/documentation/homekit/hmcharacteristictypepositionstate)

###### Values

- [HMCharacteristicValuePositionState](/documentation/homekit/hmcharacteristicvaluepositionstate)

###### Position States

- [case closing](/documentation/homekit/hmcharacteristicvaluepositionstate/closing)
- [case opening](/documentation/homekit/hmcharacteristicvaluepositionstate/opening)
- [case stopped](/documentation/homekit/hmcharacteristicvaluepositionstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepositionstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusJammed: String](/documentation/homekit/hmcharacteristictypestatusjammed)

###### Values

- [HMCharacteristicValueJammedStatus](/documentation/homekit/hmcharacteristicvaluejammedstatus)

###### Jammed Status

- [case none](/documentation/homekit/hmcharacteristicvaluejammedstatus/none)
- [case jammed](/documentation/homekit/hmcharacteristicvaluejammedstatus/jammed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluejammedstatus/init(rawvalue:))
- [let HMCharacteristicTypeHoldPosition: String](/documentation/homekit/hmcharacteristictypeholdposition)
- [let HMCharacteristicTypeSlatType: String](/documentation/homekit/hmcharacteristictypeslattype)

###### Values

- [HMCharacteristicValueSlatType](/documentation/homekit/hmcharacteristicvalueslattype)

###### Slat Types

- [case horizontal](/documentation/homekit/hmcharacteristicvalueslattype/horizontal)
- [case vertical](/documentation/homekit/hmcharacteristicvalueslattype/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueslattype/init(rawvalue:))
- [let HMCharacteristicTypeCurrentSlatState: String](/documentation/homekit/hmcharacteristictypecurrentslatstate)

###### Values

- [HMCharacteristicValueCurrentSlatState](/documentation/homekit/hmcharacteristicvaluecurrentslatstate)

###### Slat States

- [case stationary](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/stationary)
- [case jammed](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/jammed)
- [case oscillating](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/oscillating)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/init(rawvalue:))

###### Tilting mechanisms

- [let HMCharacteristicTypeCurrentHorizontalTilt: String](/documentation/homekit/hmcharacteristictypecurrenthorizontaltilt)
- [let HMCharacteristicTypeTargetHorizontalTilt: String](/documentation/homekit/hmcharacteristictypetargethorizontaltilt)
- [let HMCharacteristicTypeCurrentVerticalTilt: String](/documentation/homekit/hmcharacteristictypecurrentverticaltilt)
- [let HMCharacteristicTypeTargetVerticalTilt: String](/documentation/homekit/hmcharacteristictypetargetverticaltilt)
- [let HMCharacteristicTypeCurrentTilt: String](/documentation/homekit/hmcharacteristictypecurrenttilt)
- [let HMCharacteristicTypeTargetTilt: String](/documentation/homekit/hmcharacteristictypetargettilt)

###### Locks and openers

- [let HMCharacteristicTypeLockManagementAutoSecureTimeout: String](/documentation/homekit/hmcharacteristictypelockmanagementautosecuretimeout)
- [let HMCharacteristicTypeLockManagementControlPoint: String](/documentation/homekit/hmcharacteristictypelockmanagementcontrolpoint)
- [let HMCharacteristicTypeLockMechanismLastKnownAction: String](/documentation/homekit/hmcharacteristictypelockmechanismlastknownaction)

###### Values

- [HMCharacteristicValueLockMechanismLastKnownAction](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction)

###### Lock Mechanism Actions

- [case securedRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedremotely)
- [case securedUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovement)
- [case securedUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementexterior)
- [case securedUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementinterior)
- [case securedWithAutomaticSecureTimeout](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithautomaticsecuretimeout)
- [case securedWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithkeypad)
- [case unsecuredRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredremotely)
- [case unsecuredUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovement)
- [case unsecuredUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementexterior)
- [case unsecuredUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementinterior)
- [case unsecuredWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredwithkeypad)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/init(rawvalue:))
- [let HMCharacteristicTypeLockPhysicalControls: String](/documentation/homekit/hmcharacteristictypelockphysicalcontrols)

###### Values

- [HMCharacteristicValueLockPhysicalControlsState](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate)

###### Lock Physical Control State

- [case notLocked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/notlocked)
- [case locked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/locked)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/init(rawvalue:))
- [let HMCharacteristicTypeMotionDetected: String](/documentation/homekit/hmcharacteristictypemotiondetected)
- [let HMCharacteristicTypeCurrentLockMechanismState: String](/documentation/homekit/hmcharacteristictypecurrentlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetLockMechanismState: String](/documentation/homekit/hmcharacteristictypetargetlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [HMCharacteristicValueTargetLockMechanismState](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate)

###### Lock Mechanism States

- [case secured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/secured)
- [case unsecured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/unsecured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeRemoteKey: String](/documentation/homekit/hmcharacteristictyperemotekey)

###### Values

- [HMCharacteristicValueRemoteKey](/documentation/homekit/hmcharacteristicvalueremotekey)

###### Remote states

- [case arrowDown](/documentation/homekit/hmcharacteristicvalueremotekey/arrowdown)
- [case arrowLeft](/documentation/homekit/hmcharacteristicvalueremotekey/arrowleft)
- [case arrowRight](/documentation/homekit/hmcharacteristicvalueremotekey/arrowright)
- [case arrowUp](/documentation/homekit/hmcharacteristicvalueremotekey/arrowup)
- [case back](/documentation/homekit/hmcharacteristicvalueremotekey/back)
- [case exit](/documentation/homekit/hmcharacteristicvalueremotekey/exit)
- [case fastForward](/documentation/homekit/hmcharacteristicvalueremotekey/fastforward)
- [case home](/documentation/homekit/hmcharacteristicvalueremotekey/home)
- [case info](/documentation/homekit/hmcharacteristicvalueremotekey/info)
- [case menu](/documentation/homekit/hmcharacteristicvalueremotekey/menu)
- [case nextTrack](/documentation/homekit/hmcharacteristicvalueremotekey/nexttrack)
- [case pause](/documentation/homekit/hmcharacteristicvalueremotekey/pause)
- [case play](/documentation/homekit/hmcharacteristicvalueremotekey/play)
- [case playPause](/documentation/homekit/hmcharacteristicvalueremotekey/playpause)
- [case previousTrack](/documentation/homekit/hmcharacteristicvalueremotekey/previoustrack)
- [case rewind](/documentation/homekit/hmcharacteristicvalueremotekey/rewind)
- [case select](/documentation/homekit/hmcharacteristicvalueremotekey/select)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueremotekey/init(rawvalue:))

###### Safety and security

- [let HMCharacteristicTypeCurrentSecuritySystemState: String](/documentation/homekit/hmcharacteristictypecurrentsecuritysystemstate)

###### Values

- [HMCharacteristicValueCurrentSecuritySystemState](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/nightarm)
- [case disarmed](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/disarmed)
- [case triggered](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/triggered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetSecuritySystemState: String](/documentation/homekit/hmcharacteristictypetargetsecuritysystemstate)

###### Values

- [HMCharacteristicValueTargetSecuritySystemState](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/nightarm)
- [case disarm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/disarm)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeObstructionDetected: String](/documentation/homekit/hmcharacteristictypeobstructiondetected)
- [let HMCharacteristicTypeOccupancyDetected: String](/documentation/homekit/hmcharacteristictypeoccupancydetected)

###### Values

- [HMCharacteristicValueOccupancyStatus](/documentation/homekit/hmcharacteristicvalueoccupancystatus)

###### Occupancy Status

- [case notOccupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/notoccupied)
- [case occupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/occupied)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueoccupancystatus/init(rawvalue:))
- [let HMCharacteristicTypeSecuritySystemAlarmType: String](/documentation/homekit/hmcharacteristictypesecuritysystemalarmtype)

###### Values

- [HMCharacteristicValueSecuritySystemAlarmType](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype)

###### Alarm Types

- [case noAlarm](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/noalarm)
- [case unknown](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/init(rawvalue:))
- [let HMCharacteristicPropertyRequiresAuthorizationData: String](/documentation/homekit/hmcharacteristicpropertyrequiresauthorizationdata)

###### Audio and video

- [let HMCharacteristicTypeSupportedRTPConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedrtpconfiguration)
- [let HMCharacteristicTypeDigitalZoom: String](/documentation/homekit/hmcharacteristictypedigitalzoom)
- [let HMCharacteristicTypeOpticalZoom: String](/documentation/homekit/hmcharacteristictypeopticalzoom)
- [let HMCharacteristicTypeImageMirroring: String](/documentation/homekit/hmcharacteristictypeimagemirroring)
- [let HMCharacteristicTypeImageRotation: String](/documentation/homekit/hmcharacteristictypeimagerotation)
- [let HMCharacteristicTypeNightVision: String](/documentation/homekit/hmcharacteristictypenightvision)
- [let HMCharacteristicTypeStreamingStatus: String](/documentation/homekit/hmcharacteristictypestreamingstatus)
- [let HMCharacteristicTypeSupportedVideoStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedvideostreamconfiguration)
- [let HMCharacteristicTypeSupportedAudioStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedaudiostreamconfiguration)
- [let HMCharacteristicTypeSelectedStreamConfiguration: String](/documentation/homekit/hmcharacteristictypeselectedstreamconfiguration)
- [let HMCharacteristicTypeSetupStreamEndpoint: String](/documentation/homekit/hmcharacteristictypesetupstreamendpoint)
- [let HMCharacteristicTypeAudioFeedback: String](/documentation/homekit/hmcharacteristictypeaudiofeedback)
- [let HMCharacteristicTypeVolume: String](/documentation/homekit/hmcharacteristictypevolume)
- [let HMCharacteristicTypeMute: String](/documentation/homekit/hmcharacteristictypemute)
- [let HMCharacteristicTypeVolumeSelector: String](/documentation/homekit/hmcharacteristictypevolumeselector)

###### Values

- [HMCharacteristicValueVolumeSelector](/documentation/homekit/hmcharacteristicvaluevolumeselector)

###### Volume cases

- [case volumeDecrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumedecrement)
- [case volumeIncrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumeincrement)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumeselector/init(rawvalue:))
- [let HMCharacteristicTypeVolumeControlType: String](/documentation/homekit/hmcharacteristictypevolumecontroltype)

###### Values

- [HMCharacteristicValueVolumeControlType](/documentation/homekit/hmcharacteristicvaluevolumecontroltype)

###### Volume types

- [case absolute](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/absolute)
- [case none](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/none)
- [case relative](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relative)
- [case relativeWithCurrent](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relativewithcurrent)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/init(rawvalue:))
- [let HMCharacteristicTypeClosedCaptions: String](/documentation/homekit/hmcharacteristictypeclosedcaptions)

###### Values

- [HMCharacteristicValueClosedCaptions](/documentation/homekit/hmcharacteristicvalueclosedcaptions)

###### Closed caption states

- [case disabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueclosedcaptions/init(rawvalue:))
- [let HMCharacteristicTypePictureMode: String](/documentation/homekit/hmcharacteristictypepicturemode)

###### Values

- [HMCharacteristicValuePictureMode](/documentation/homekit/hmcharacteristicvaluepicturemode)

###### Television states

- [case bright](/documentation/homekit/hmcharacteristicvaluepicturemode/bright)
- [case calibrated](/documentation/homekit/hmcharacteristicvaluepicturemode/calibrated)
- [case computer](/documentation/homekit/hmcharacteristicvaluepicturemode/computer)
- [case custom1](/documentation/homekit/hmcharacteristicvaluepicturemode/custom1)
- [case custom2](/documentation/homekit/hmcharacteristicvaluepicturemode/custom2)
- [case custom3](/documentation/homekit/hmcharacteristicvaluepicturemode/custom3)
- [case dark](/documentation/homekit/hmcharacteristicvaluepicturemode/dark)
- [case game](/documentation/homekit/hmcharacteristicvaluepicturemode/game)
- [case movie](/documentation/homekit/hmcharacteristicvaluepicturemode/movie)
- [case night](/documentation/homekit/hmcharacteristicvaluepicturemode/night)
- [case photo](/documentation/homekit/hmcharacteristicvaluepicturemode/photo)
- [case sport](/documentation/homekit/hmcharacteristicvaluepicturemode/sport)
- [case standard](/documentation/homekit/hmcharacteristicvaluepicturemode/standard)
- [case vivid](/documentation/homekit/hmcharacteristicvaluepicturemode/vivid)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepicturemode/init(rawvalue:))

###### General state

- [let HMCharacteristicTypeActive: String](/documentation/homekit/hmcharacteristictypeactive)

###### Values

- [HMCharacteristicValueActivationState](/documentation/homekit/hmcharacteristicvalueactivationstate)

###### Activation States

- [case inactive](/documentation/homekit/hmcharacteristicvalueactivationstate/inactive)
- [case active](/documentation/homekit/hmcharacteristicvalueactivationstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueactivationstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusTampered: String](/documentation/homekit/hmcharacteristictypestatustampered)

###### Values

- [HMCharacteristicValueTamperedStatus](/documentation/homekit/hmcharacteristicvaluetamperedstatus)

###### Tampered Status

- [case none](/documentation/homekit/hmcharacteristicvaluetamperedstatus/none)
- [case tampered](/documentation/homekit/hmcharacteristicvaluetamperedstatus/tampered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetamperedstatus/init(rawvalue:))
- [let HMCharacteristicTypeStatusFault: String](/documentation/homekit/hmcharacteristictypestatusfault)

###### Values

- [HMCharacteristicValueStatusFault](/documentation/homekit/hmcharacteristicvaluestatusfault)

###### Fault Status

- [case noFault](/documentation/homekit/hmcharacteristicvaluestatusfault/nofault)
- [case generalFault](/documentation/homekit/hmcharacteristicvaluestatusfault/generalfault)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluestatusfault/init(rawvalue:))
- [let HMCharacteristicTypeStatusActive: String](/documentation/homekit/hmcharacteristictypestatusactive)
- [let HMCharacteristicTypeInUse: String](/documentation/homekit/hmcharacteristictypeinuse)

###### Values

- [HMCharacteristicValueUsageState](/documentation/homekit/hmcharacteristicvalueusagestate)

###### Usage States

- [case notInUse](/documentation/homekit/hmcharacteristicvalueusagestate/notinuse)
- [case inUse](/documentation/homekit/hmcharacteristicvalueusagestate/inuse)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueusagestate/init(rawvalue:))
- [let HMCharacteristicTypeIsConfigured: String](/documentation/homekit/hmcharacteristictypeisconfigured)

###### Values

- [HMCharacteristicValueConfigurationState](/documentation/homekit/hmcharacteristicvalueconfigurationstate)

###### Configuration States

- [case notConfigured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/notconfigured)
- [case configured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/configured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueconfigurationstate/init(rawvalue:))
- [let HMCharacteristicTypeRemainingDuration: String](/documentation/homekit/hmcharacteristictyperemainingduration)
- [let HMCharacteristicTypeSetDuration: String](/documentation/homekit/hmcharacteristictypesetduration)
- [let HMCharacteristicTypeProgramMode: String](/documentation/homekit/hmcharacteristictypeprogrammode)

###### Values

- [HMCharacteristicValueProgramMode](/documentation/homekit/hmcharacteristicvalueprogrammode)

###### Constants

- [case notScheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/notscheduled)
- [case scheduleOverriddenToManual](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduleoverriddentomanual)
- [case scheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueprogrammode/init(rawvalue:))
- [let HMCharacteristicTypeWiFiSatelliteStatus: String](/documentation/homekit/hmcharacteristictypewifisatellitestatus)

###### Values

- [HMCharacteristicValueWiFiSatelliteStatus](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus)

###### Network states

- [case connected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/connected)
- [case notConnected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/notconnected)
- [case unknown](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/init(rawvalue:))
- [let HMCharacteristicTypeWANStatusList: String](/documentation/homekit/hmcharacteristictypewanstatuslist)
- [let HMCharacteristicTypeTargetMediaState: String](/documentation/homekit/hmcharacteristictypetargetmediastate)

###### Values

- [HMCharacteristicValueTargetMediaState](/documentation/homekit/hmcharacteristicvaluetargetmediastate)

###### Media states

- [case pause](/documentation/homekit/hmcharacteristicvaluetargetmediastate/pause)
- [case play](/documentation/homekit/hmcharacteristicvaluetargetmediastate/play)
- [case stop](/documentation/homekit/hmcharacteristicvaluetargetmediastate/stop)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetmediastate/init(rawvalue:))
- [let HMCharacteristicTypeRouterStatus: String](/documentation/homekit/hmcharacteristictyperouterstatus)

###### Values

- [HMCharacteristicValueRouterStatus](/documentation/homekit/hmcharacteristicvaluerouterstatus)

###### Router states

- [case notReady](/documentation/homekit/hmcharacteristicvaluerouterstatus/notready)
- [case ready](/documentation/homekit/hmcharacteristicvaluerouterstatus/ready)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerouterstatus/init(rawvalue:))
- [let HMCharacteristicTypeCurrentMediaState: String](/documentation/homekit/hmcharacteristictypecurrentmediastate)

###### Values

- [HMCharacteristicValueCurrentMediaState](/documentation/homekit/hmcharacteristicvaluecurrentmediastate)

###### Current media states

- [case interrupted](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/interrupted)
- [case loading](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/loading)
- [case paused](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/paused)
- [case playing](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/playing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/stopped)
- [case unknown](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentVisibilityState: String](/documentation/homekit/hmcharacteristictypecurrentvisibilitystate)

###### Values

- [HMCharacteristicValueCurrentVisibilityState](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate)

###### Visibility states

- [case alwaysShown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/alwaysshown)
- [case connected](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/connected)
- [case hidden](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/hidden)
- [case shown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/shown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/init(rawvalue:))
- [let HMCharacteristicTypeTargetVisibilityState: String](/documentation/homekit/hmcharacteristictypetargetvisibilitystate)

###### Values

- [HMCharacteristicValueTargetVisibilityState](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate)

###### Visibility states

- [case hide](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/init(rawvalue:))
- [let HMCharacteristicPropertySupportsEventNotification: String](/documentation/homekit/hmcharacteristicpropertysupportseventnotification-2f0ml)

###### Accessory identification

- [let HMCharacteristicTypeName: String](/documentation/homekit/hmcharacteristictypename)
- [let HMCharacteristicTypeIdentify: String](/documentation/homekit/hmcharacteristictypeidentify)
- [let HMCharacteristicTypeVersion: String](/documentation/homekit/hmcharacteristictypeversion)
- [let HMCharacteristicTypeLogs: String](/documentation/homekit/hmcharacteristictypelogs)
- [let HMCharacteristicTypeAdminOnlyAccess: String](/documentation/homekit/hmcharacteristictypeadminonlyaccess)
- [let HMCharacteristicTypeHardwareVersion: String](/documentation/homekit/hmcharacteristictypehardwareversion)
- [let HMCharacteristicTypeSoftwareVersion: String](/documentation/homekit/hmcharacteristictypesoftwareversion)
- [let HMCharacteristicTypeLabelIndex: String](/documentation/homekit/hmcharacteristictypelabelindex)
- [let HMCharacteristicTypeLabelNamespace: String](/documentation/homekit/hmcharacteristictypelabelnamespace)

###### Values

- [HMCharacteristicValueLabelNamespace](/documentation/homekit/hmcharacteristicvaluelabelnamespace)

###### Namespaces

- [case dot](/documentation/homekit/hmcharacteristicvaluelabelnamespace/dot)
- [case numeral](/documentation/homekit/hmcharacteristicvaluelabelnamespace/numeral)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelabelnamespace/init(rawvalue:))
- [let HMCharacteristicTypeActiveIdentifier: String](/documentation/homekit/hmcharacteristictypeactiveidentifier)
- [let HMCharacteristicTypeIdentifier: String](/documentation/homekit/hmcharacteristictypeidentifier)
- [let HMCharacteristicTypeInputDeviceType: String](/documentation/homekit/hmcharacteristictypeinputdevicetype)

###### Values

- [HMCharacteristicValueInputDeviceType](/documentation/homekit/hmcharacteristicvalueinputdevicetype)

###### Input devices

- [case audioSystem](/documentation/homekit/hmcharacteristicvalueinputdevicetype/audiosystem)
- [case none](/documentation/homekit/hmcharacteristicvalueinputdevicetype/none)
- [case other](/documentation/homekit/hmcharacteristicvalueinputdevicetype/other)
- [case playback](/documentation/homekit/hmcharacteristicvalueinputdevicetype/playback)
- [case recording](/documentation/homekit/hmcharacteristicvalueinputdevicetype/recording)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tuner)
- [case tv](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tv)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputdevicetype/init(rawvalue:))
- [let HMCharacteristicTypeInputSourceType: String](/documentation/homekit/hmcharacteristictypeinputsourcetype)

###### Values

- [HMCharacteristicValueInputSourceType](/documentation/homekit/hmcharacteristicvalueinputsourcetype)

###### Accessory source types

- [case airPlay](/documentation/homekit/hmcharacteristicvalueinputsourcetype/airplay)
- [case application](/documentation/homekit/hmcharacteristicvalueinputsourcetype/application)
- [case componentVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/componentvideo)
- [case compositeVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/compositevideo)
- [case dvi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/dvi)
- [case hdmi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/hdmi)
- [case homeScreen](/documentation/homekit/hmcharacteristicvalueinputsourcetype/homescreen)
- [case other](/documentation/homekit/hmcharacteristicvalueinputsourcetype/other)
- [case sVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/svideo)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputsourcetype/tuner)
- [case usb](/documentation/homekit/hmcharacteristicvalueinputsourcetype/usb)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputsourcetype/init(rawvalue:))
- [let HMCharacteristicTypeConfiguredName: String](/documentation/homekit/hmcharacteristictypeconfiguredname)

###### Deprecated characteristic types

- [let HMCharacteristicTypeManufacturer: String](/documentation/homekit/hmcharacteristictypemanufacturer)
- [let HMCharacteristicTypeModel: String](/documentation/homekit/hmcharacteristictypemodel)
- [let HMCharacteristicTypeFirmwareVersion: String](/documentation/homekit/hmcharacteristictypefirmwareversion)
- [let HMCharacteristicTypeSerialNumber: String](/documentation/homekit/hmcharacteristictypeserialnumber)

##### Controlling a characteristic

- [var value: Any?](/documentation/homekit/hmcharacteristic/value)
- [func readValue(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/readvalue(completionhandler:))
- [func writeValue(Any?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/writevalue(_:completionhandler:))
- [func updateAuthorizationData(Data?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/updateauthorizationdata(_:completionhandler:))

##### Managing characteristic presentation

- [var metadata: HMCharacteristicMetadata?](/documentation/homekit/hmcharacteristic/metadata)
- [HMCharacteristicMetadata](/documentation/homekit/hmcharacteristicmetadata)

###### Describing a characteristic

- [var manufacturerDescription: String?](/documentation/homekit/hmcharacteristicmetadata/manufacturerdescription)

###### Bounding the value

- [var validValues: [NSNumber]?](/documentation/homekit/hmcharacteristicmetadata/validvalues)
- [var minimumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/minimumvalue)
- [var maximumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maximumvalue)
- [var stepValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/stepvalue)
- [var maxLength: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maxlength)

###### Formatting the value

- [var format: String?](/documentation/homekit/hmcharacteristicmetadata/format)
- [Characteristic Data Formats](/documentation/homekit/characteristic-data-formats)

###### Booleans

- [let HMCharacteristicMetadataFormatBool: String](/documentation/homekit/hmcharacteristicmetadataformatbool)

###### Strings

- [let HMCharacteristicMetadataFormatString: String](/documentation/homekit/hmcharacteristicmetadataformatstring)

###### Signed Values

- [let HMCharacteristicMetadataFormatInt: String](/documentation/homekit/hmcharacteristicmetadataformatint)
- [let HMCharacteristicMetadataFormatFloat: String](/documentation/homekit/hmcharacteristicmetadataformatfloat)

###### Unsigned Integers

- [let HMCharacteristicMetadataFormatUInt8: String](/documentation/homekit/hmcharacteristicmetadataformatuint8)
- [let HMCharacteristicMetadataFormatUInt16: String](/documentation/homekit/hmcharacteristicmetadataformatuint16)
- [let HMCharacteristicMetadataFormatUInt32: String](/documentation/homekit/hmcharacteristicmetadataformatuint32)
- [let HMCharacteristicMetadataFormatUInt64: String](/documentation/homekit/hmcharacteristicmetadataformatuint64)

###### Data

- [let HMCharacteristicMetadataFormatData: String](/documentation/homekit/hmcharacteristicmetadataformatdata)
- [let HMCharacteristicMetadataFormatTLV8: String](/documentation/homekit/hmcharacteristicmetadataformattlv8)

###### Collections

- [let HMCharacteristicMetadataFormatArray: String](/documentation/homekit/hmcharacteristicmetadataformatarray)
- [let HMCharacteristicMetadataFormatDictionary: String](/documentation/homekit/hmcharacteristicmetadataformatdictionary)

###### Specifying units

- [var units: String?](/documentation/homekit/hmcharacteristicmetadata/units)
- [Characteristic Units](/documentation/homekit/characteristic-units)

###### Parts Per Total

- [let HMCharacteristicMetadataUnitsPercentage: String](/documentation/homekit/hmcharacteristicmetadataunitspercentage)
- [let HMCharacteristicMetadataUnitsPartsPerMillion: String](/documentation/homekit/hmcharacteristicmetadataunitspartspermillion)

###### Temperature

- [let HMCharacteristicMetadataUnitsCelsius: String](/documentation/homekit/hmcharacteristicmetadataunitscelsius)
- [let HMCharacteristicMetadataUnitsFahrenheit: String](/documentation/homekit/hmcharacteristicmetadataunitsfahrenheit)

###### Time

- [let HMCharacteristicMetadataUnitsSeconds: String](/documentation/homekit/hmcharacteristicmetadataunitsseconds)

###### Light

- [let HMCharacteristicMetadataUnitsLux: String](/documentation/homekit/hmcharacteristicmetadataunitslux)

###### Mass

- [let HMCharacteristicMetadataUnitsMicrogramsPerCubicMeter: String](/documentation/homekit/hmcharacteristicmetadataunitsmicrogramspercubicmeter)

###### Rotation

- [let HMCharacteristicMetadataUnitsArcDegree: String](/documentation/homekit/hmcharacteristicmetadataunitsarcdegree)

###### Initializers

- [init()](/documentation/homekit/hmcharacteristicmetadata/init())

##### Receiving change notifications

- [func enableNotification(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/enablenotification(_:completionhandler:))
- [var isNotificationEnabled: Bool](/documentation/homekit/hmcharacteristic/isnotificationenabled)

##### Getting the characterized service

- [var service: HMService?](/documentation/homekit/hmcharacteristic/service)

##### Initializers

- [init()](/documentation/homekit/hmcharacteristic/init())

#### Identifying the service

- [var name: String](/documentation/homekit/hmservice/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmservice/uniqueidentifier)

#### Getting the service type

- [var serviceType: String](/documentation/homekit/hmservice/servicetype)
- [Accessory Service Types](/documentation/homekit/accessory-service-types)

##### Light

- [let HMServiceTypeLightbulb: String](/documentation/homekit/hmservicetypelightbulb)
- [let HMServiceTypeLightSensor: String](/documentation/homekit/hmservicetypelightsensor)

##### Power and Switches

- [let HMServiceTypeSwitch: String](/documentation/homekit/hmservicetypeswitch)
- [let HMServiceTypeBattery: String](/documentation/homekit/hmservicetypebattery)
- [let HMServiceTypeOutlet: String](/documentation/homekit/hmservicetypeoutlet)
- [let HMServiceTypeStatefulProgrammableSwitch: String](/documentation/homekit/hmservicetypestatefulprogrammableswitch)
- [let HMServiceTypeStatelessProgrammableSwitch: String](/documentation/homekit/hmservicetypestatelessprogrammableswitch)

##### Air Quality and Smoke Detection

- [let HMServiceTypeAirPurifier: String](/documentation/homekit/hmservicetypeairpurifier)
- [let HMServiceTypeAirQualitySensor: String](/documentation/homekit/hmservicetypeairqualitysensor)
- [let HMServiceTypeCarbonDioxideSensor: String](/documentation/homekit/hmservicetypecarbondioxidesensor)
- [let HMServiceTypeCarbonMonoxideSensor: String](/documentation/homekit/hmservicetypecarbonmonoxidesensor)
- [let HMServiceTypeSmokeSensor: String](/documentation/homekit/hmservicetypesmokesensor)

##### Temperature and Humidity

- [let HMServiceTypeHeaterCooler: String](/documentation/homekit/hmservicetypeheatercooler)
- [let HMServiceTypeTemperatureSensor: String](/documentation/homekit/hmservicetypetemperaturesensor)
- [let HMServiceTypeThermostat: String](/documentation/homekit/hmservicetypethermostat)
- [let HMServiceTypeFan: String](/documentation/homekit/hmservicetypefan)
- [let HMServiceTypeFilterMaintenance: String](/documentation/homekit/hmservicetypefiltermaintenance)
- [let HMServiceTypeHumidifierDehumidifier: String](/documentation/homekit/hmservicetypehumidifierdehumidifier)
- [let HMServiceTypeHumiditySensor: String](/documentation/homekit/hmservicetypehumiditysensor)
- [let HMServiceTypeVentilationFan: String](/documentation/homekit/hmservicetypeventilationfan)

##### Windows

- [let HMServiceTypeWindow: String](/documentation/homekit/hmservicetypewindow)
- [let HMServiceTypeWindowCovering: String](/documentation/homekit/hmservicetypewindowcovering)
- [let HMServiceTypeSlats: String](/documentation/homekit/hmservicetypeslats)

##### Water

- [let HMServiceTypeFaucet: String](/documentation/homekit/hmservicetypefaucet)
- [let HMServiceTypeValve: String](/documentation/homekit/hmservicetypevalve)
- [let HMServiceTypeIrrigationSystem: String](/documentation/homekit/hmservicetypeirrigationsystem)
- [let HMServiceTypeLeakSensor: String](/documentation/homekit/hmservicetypeleaksensor)

##### Locks and Openers

- [let HMServiceTypeDoor: String](/documentation/homekit/hmservicetypedoor)
- [let HMServiceTypeDoorbell: String](/documentation/homekit/hmservicetypedoorbell)
- [let HMServiceTypeGarageDoorOpener: String](/documentation/homekit/hmservicetypegaragedooropener)
- [let HMServiceTypeLockManagement: String](/documentation/homekit/hmservicetypelockmanagement)
- [let HMServiceTypeLockMechanism: String](/documentation/homekit/hmservicetypelockmechanism)

##### Safety and Security

- [let HMServiceTypeMotionSensor: String](/documentation/homekit/hmservicetypemotionsensor)
- [let HMServiceTypeOccupancySensor: String](/documentation/homekit/hmservicetypeoccupancysensor)
- [let HMServiceTypeSecuritySystem: String](/documentation/homekit/hmservicetypesecuritysystem)
- [let HMServiceTypeContactSensor: String](/documentation/homekit/hmservicetypecontactsensor)

##### Video and Audio

- [let HMServiceTypeCameraControl: String](/documentation/homekit/hmservicetypecameracontrol)
- [let HMServiceTypeCameraRTPStreamManagement: String](/documentation/homekit/hmservicetypecamerartpstreammanagement)
- [let HMServiceTypeMicrophone: String](/documentation/homekit/hmservicetypemicrophone)
- [let HMServiceTypeSpeaker: String](/documentation/homekit/hmservicetypespeaker)
- [let HMServiceTypeInputSource: String](/documentation/homekit/hmservicetypeinputsource)
- [let HMServiceTypeTelevision: String](/documentation/homekit/hmservicetypetelevision)

##### Network

- [let HMServiceTypeWiFiRouter: String](/documentation/homekit/hmservicetypewifirouter)
- [let HMServiceTypeWiFiSatellite: String](/documentation/homekit/hmservicetypewifisatellite)

##### Information

- [let HMServiceTypeLabel: String](/documentation/homekit/hmservicetypelabel)
- [let HMServiceTypeAccessoryInformation: String](/documentation/homekit/hmservicetypeaccessoryinformation)
- [var localizedDescription: String](/documentation/homekit/hmservice/localizeddescription)

#### Reading service properties

- [var isPrimaryService: Bool](/documentation/homekit/hmservice/isprimaryservice)
- [var isUserInteractive: Bool](/documentation/homekit/hmservice/isuserinteractive)

#### Associating a secondary service

- [var associatedServiceType: String?](/documentation/homekit/hmservice/associatedservicetype)
- [func updateAssociatedServiceType(String?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updateassociatedservicetype(_:completionhandler:))

#### Finding the linked services

- [var linkedServices: [HMService]?](/documentation/homekit/hmservice/linkedservices)

#### Getting the service’s provider

- [var accessory: HMAccessory?](/documentation/homekit/hmservice/accessory)

#### Initializers

- [init()](/documentation/homekit/hmservice/init())

#### Instance Properties

- [var matterEndpointID: UInt16?](/documentation/homekit/hmservice/matterendpointid-62vu6)

### Managing bridged accessories

- [var isBridged: Bool](/documentation/homekit/hmaccessory/isbridged)
- [var uniqueIdentifiersForBridgedAccessories: [UUID]?](/documentation/homekit/hmaccessory/uniqueidentifiersforbridgedaccessories)
- [var identifiersForBridgedAccessories: [UUID]?](/documentation/homekit/hmaccessory/identifiersforbridgedaccessories)

### Getting manufacturer information

- [var firmwareVersion: String?](/documentation/homekit/hmaccessory/firmwareversion)
- [var manufacturer: String?](/documentation/homekit/hmaccessory/manufacturer)
- [var model: String?](/documentation/homekit/hmaccessory/model)

### Browsing for accessories

- [HMAccessoryBrowser](/documentation/homekit/hmaccessorybrowser)

#### Discovering accessories

- [var discoveredAccessories: [HMAccessory]](/documentation/homekit/hmaccessorybrowser/discoveredaccessories)
- [func startSearchingForNewAccessories()](/documentation/homekit/hmaccessorybrowser/startsearchingfornewaccessories())
- [func stopSearchingForNewAccessories()](/documentation/homekit/hmaccessorybrowser/stopsearchingfornewaccessories())

#### Tracking the addition or removal of accessories

- [var delegate: (any HMAccessoryBrowserDelegate)?](/documentation/homekit/hmaccessorybrowser/delegate)
- [HMAccessoryBrowserDelegate](/documentation/homekit/hmaccessorybrowserdelegate)

##### Tracking new accessories

- [func accessoryBrowser(HMAccessoryBrowser, didFindNewAccessory: HMAccessory)](/documentation/homekit/hmaccessorybrowserdelegate/accessorybrowser(_:didfindnewaccessory:))
- [func accessoryBrowser(HMAccessoryBrowser, didRemoveNewAccessory: HMAccessory)](/documentation/homekit/hmaccessorybrowserdelegate/accessorybrowser(_:didremovenewaccessory:))

#### Initializers

- [init()](/documentation/homekit/hmaccessorybrowser/init())

### Instance Properties

- [var matterNodeID: UInt64?](/documentation/homekit/hmaccessory/matternodeid-67v1j)
- [var bridgedAccessories: [HMAccessory]](/documentation/homekit/hmaccessory/bridgedaccessories)
- [var hapInstanceID: UInt64?](/documentation/homekit/hmaccessory/hapinstanceid-3cusx)
- [var home: HMHome?](/documentation/homekit/hmaccessory/home)
- [var isVendorAccessory: Bool](/documentation/homekit/hmaccessory/isvendoraccessory)

### Initializers

- [init()](/documentation/homekit/hmaccessory/init())
- [HMService](/documentation/homekit/hmservice)

### Getting service characteristics

- [var characteristics: [HMCharacteristic]](/documentation/homekit/hmservice/characteristics)
- [HMCharacteristic](/documentation/homekit/hmcharacteristic)

#### Identifying a characteristic

- [var uniqueIdentifier: UUID](/documentation/homekit/hmcharacteristic/uniqueidentifier)
- [var localizedDescription: String](/documentation/homekit/hmcharacteristic/localizeddescription)

#### Reading characteristic properties

- [var properties: [String]](/documentation/homekit/hmcharacteristic/properties)
- [Characteristic Properties](/documentation/homekit/characteristic-properties)

##### Properties of Characteristics

- [let HMCharacteristicPropertyReadable: String](/documentation/homekit/hmcharacteristicpropertyreadable)
- [let HMCharacteristicPropertyWritable: String](/documentation/homekit/hmcharacteristicpropertywritable)
- [let HMCharacteristicPropertyHidden: String](/documentation/homekit/hmcharacteristicpropertyhidden)

#### Determining what a characteristic controls

- [var characteristicType: String](/documentation/homekit/hmcharacteristic/characteristictype)
- [Characteristic types](/documentation/homekit/characteristic-types)

##### Light

- [let HMCharacteristicTypeCurrentLightLevel: String](/documentation/homekit/hmcharacteristictypecurrentlightlevel)
- [let HMCharacteristicTypeHue: String](/documentation/homekit/hmcharacteristictypehue)
- [let HMCharacteristicTypeBrightness: String](/documentation/homekit/hmcharacteristictypebrightness)
- [let HMCharacteristicTypeSaturation: String](/documentation/homekit/hmcharacteristictypesaturation)
- [let HMCharacteristicTypeColorTemperature: String](/documentation/homekit/hmcharacteristictypecolortemperature)

##### Power and switches

- [let HMCharacteristicTypeBatteryLevel: String](/documentation/homekit/hmcharacteristictypebatterylevel)
- [let HMCharacteristicTypeChargingState: String](/documentation/homekit/hmcharacteristictypechargingstate)

###### Values

- [HMCharacteristicValueChargingState](/documentation/homekit/hmcharacteristicvaluechargingstate)

###### Charging States

- [case none](/documentation/homekit/hmcharacteristicvaluechargingstate/none)
- [case inProgress](/documentation/homekit/hmcharacteristicvaluechargingstate/inprogress)
- [case notChargeable](/documentation/homekit/hmcharacteristicvaluechargingstate/notchargeable)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluechargingstate/init(rawvalue:))
- [let HMCharacteristicTypeContactState: String](/documentation/homekit/hmcharacteristictypecontactstate)

###### Values

- [HMCharacteristicValueContactState](/documentation/homekit/hmcharacteristicvaluecontactstate)

###### Contact Sensor State

- [case detected](/documentation/homekit/hmcharacteristicvaluecontactstate/detected)
- [case none](/documentation/homekit/hmcharacteristicvaluecontactstate/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecontactstate/init(rawvalue:))
- [let HMCharacteristicTypeOutletInUse: String](/documentation/homekit/hmcharacteristictypeoutletinuse)
- [let HMCharacteristicTypePowerState: String](/documentation/homekit/hmcharacteristictypepowerstate)
- [let HMCharacteristicTypeStatusLowBattery: String](/documentation/homekit/hmcharacteristictypestatuslowbattery)

###### Values

- [HMCharacteristicValueBatteryStatus](/documentation/homekit/hmcharacteristicvaluebatterystatus)

###### Battery Status

- [case normal](/documentation/homekit/hmcharacteristicvaluebatterystatus/normal)
- [case low](/documentation/homekit/hmcharacteristicvaluebatterystatus/low)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluebatterystatus/init(rawvalue:))
- [let HMCharacteristicTypeOutputState: String](/documentation/homekit/hmcharacteristictypeoutputstate)
- [let HMCharacteristicTypeInputEvent: String](/documentation/homekit/hmcharacteristictypeinputevent)

###### Values

- [HMCharacteristicValueInputEvent](/documentation/homekit/hmcharacteristicvalueinputevent)

###### Input Events

- [case singlePress](/documentation/homekit/hmcharacteristicvalueinputevent/singlepress)
- [case doublePress](/documentation/homekit/hmcharacteristicvalueinputevent/doublepress)
- [case longPress](/documentation/homekit/hmcharacteristicvalueinputevent/longpress)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputevent/init(rawvalue:))
- [let HMCharacteristicTypePowerModeSelection: String](/documentation/homekit/hmcharacteristictypepowermodeselection)

###### Values

- [HMCharacteristicValuePowerModeSelection](/documentation/homekit/hmcharacteristicvaluepowermodeselection)

###### Power mode status

- [case hide](/documentation/homekit/hmcharacteristicvaluepowermodeselection/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluepowermodeselection/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepowermodeselection/init(rawvalue:))

##### Temperature

- [let HMCharacteristicTypeCurrentTemperature: String](/documentation/homekit/hmcharacteristictypecurrenttemperature)
- [let HMCharacteristicTypeTargetTemperature: String](/documentation/homekit/hmcharacteristictypetargettemperature)
- [let HMCharacteristicTypeTemperatureUnits: String](/documentation/homekit/hmcharacteristictypetemperatureunits)

###### Values

- [HMCharacteristicValueTemperatureUnit](/documentation/homekit/hmcharacteristicvaluetemperatureunit)

###### Temperature Units

- [case celsius](/documentation/homekit/hmcharacteristicvaluetemperatureunit/celsius)
- [case fahrenheit](/documentation/homekit/hmcharacteristicvaluetemperatureunit/fahrenheit)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetemperatureunit/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeatingCooling: String](/documentation/homekit/hmcharacteristictypetargetheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeatingCooling: String](/documentation/homekit/hmcharacteristictypecurrentheatingcooling)

###### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [HMCharacteristicValueCurrentHeatingCooling](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling)

###### Temperature States

- [case cool](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/cool)
- [case heat](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/heat)
- [case off](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/off)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypetargetheatercoolerstate)

###### Values

- [HMCharacteristicValueTargetHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate)

###### Target State

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/automatic)
- [case heat](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/heat)
- [case cool](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/cool)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypecurrentheatercoolerstate)

###### Values

- [HMCharacteristicValueCurrentHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate)

###### Current State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/idle)
- [case heating](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/heating)
- [case cooling](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/cooling)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCoolingThreshold: String](/documentation/homekit/hmcharacteristictypecoolingthreshold)
- [let HMCharacteristicTypeHeatingThreshold: String](/documentation/homekit/hmcharacteristictypeheatingthreshold)

##### Humidity

- [let HMCharacteristicTypeCurrentRelativeHumidity: String](/documentation/homekit/hmcharacteristictypecurrentrelativehumidity)
- [let HMCharacteristicTypeTargetRelativeHumidity: String](/documentation/homekit/hmcharacteristictypetargetrelativehumidity)
- [let HMCharacteristicTypeCurrentHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypecurrenthumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueCurrentHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate)

###### Current States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/idle)
- [case humidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/humidifying)
- [case dehumidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/dehumidifying)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypetargethumidifierdehumidifierstate)

###### Values

- [HMCharacteristicValueTargetHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate)

###### Target States

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/automatic)
- [case humidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/humidify)
- [case dehumidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/dehumidify)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeHumidifierThreshold: String](/documentation/homekit/hmcharacteristictypehumidifierthreshold)
- [let HMCharacteristicTypeDehumidifierThreshold: String](/documentation/homekit/hmcharacteristictypedehumidifierthreshold)

##### Air quality and smoke detection

- [let HMCharacteristicTypeAirQuality: String](/documentation/homekit/hmcharacteristictypeairquality)

###### Values

- [HMCharacteristicValueAirQuality](/documentation/homekit/hmcharacteristicvalueairquality)

###### Air Quality

- [case unknown](/documentation/homekit/hmcharacteristicvalueairquality/unknown)
- [case excellent](/documentation/homekit/hmcharacteristicvalueairquality/excellent)
- [case good](/documentation/homekit/hmcharacteristicvalueairquality/good)
- [case fair](/documentation/homekit/hmcharacteristicvalueairquality/fair)
- [case inferior](/documentation/homekit/hmcharacteristicvalueairquality/inferior)
- [case poor](/documentation/homekit/hmcharacteristicvalueairquality/poor)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairquality/init(rawvalue:))
- [let HMCharacteristicTypeAirParticulateDensity: String](/documentation/homekit/hmcharacteristictypeairparticulatedensity)
- [let HMCharacteristicTypeAirParticulateSize: String](/documentation/homekit/hmcharacteristictypeairparticulatesize)

###### Values

- [HMCharacteristicValueAirParticulateSize](/documentation/homekit/hmcharacteristicvalueairparticulatesize)

###### Air Particulate Sizes

- [case size2_5](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size2_5)
- [case size10](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size10)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairparticulatesize/init(rawvalue:))
- [let HMCharacteristicTypeSmokeDetected: String](/documentation/homekit/hmcharacteristictypesmokedetected)

###### Values

- [HMCharacteristicValueSmokeDetectionStatus](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus)

###### Smoke Detection Status

- [case none](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideDetected: String](/documentation/homekit/hmcharacteristictypecarbondioxidedetected)

###### Values

- [HMCharacteristicValueCarbonDioxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus)

###### Carbon Dioxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidelevel)
- [let HMCharacteristicTypeCarbonDioxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidepeaklevel)
- [let HMCharacteristicTypeCarbonMonoxideDetected: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidedetected)

###### Values

- [HMCharacteristicValueCarbonMonoxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus)

###### Carbon Monoxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonMonoxideLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidelevel)
- [let HMCharacteristicTypeCarbonMonoxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidepeaklevel)
- [let HMCharacteristicTypeNitrogenDioxideDensity: String](/documentation/homekit/hmcharacteristictypenitrogendioxidedensity)
- [let HMCharacteristicTypeOzoneDensity: String](/documentation/homekit/hmcharacteristictypeozonedensity)
- [let HMCharacteristicTypePM10Density: String](/documentation/homekit/hmcharacteristictypepm10density)
- [let HMCharacteristicTypePM2_5Density: String](/documentation/homekit/hmcharacteristictypepm2_5density)
- [let HMCharacteristicTypeSulphurDioxideDensity: String](/documentation/homekit/hmcharacteristictypesulphurdioxidedensity)
- [let HMCharacteristicTypeVolatileOrganicCompoundDensity: String](/documentation/homekit/hmcharacteristictypevolatileorganiccompounddensity)

##### Fans

- [let HMCharacteristicTypeCurrentFanState: String](/documentation/homekit/hmcharacteristictypecurrentfanstate)

###### Values

- [HMCharacteristicValueCurrentFanState](/documentation/homekit/hmcharacteristicvaluecurrentfanstate)

###### Fan State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetFanState: String](/documentation/homekit/hmcharacteristictypetargetfanstate)

###### Values

- [HMCharacteristicValueTargetFanState](/documentation/homekit/hmcharacteristicvaluetargetfanstate)

###### Fan State

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetfanstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetfanstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetfanstate/init(rawvalue:))
- [let HMCharacteristicTypeRotationDirection: String](/documentation/homekit/hmcharacteristictyperotationdirection)

###### Values

- [HMCharacteristicValueRotationDirection](/documentation/homekit/hmcharacteristicvaluerotationdirection)

###### Rotation

- [case clockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/clockwise)
- [case counterClockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/counterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerotationdirection/init(rawvalue:))
- [let HMCharacteristicTypeRotationSpeed: String](/documentation/homekit/hmcharacteristictyperotationspeed)
- [let HMCharacteristicTypeSwingMode: String](/documentation/homekit/hmcharacteristictypeswingmode)

###### Values

- [HMCharacteristicValueSwingMode](/documentation/homekit/hmcharacteristicvalueswingmode)

###### Movement Mode

- [case disabled](/documentation/homekit/hmcharacteristicvalueswingmode/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueswingmode/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueswingmode/init(rawvalue:))

##### Purifiers and filters

- [let HMCharacteristicTypeCurrentAirPurifierState: String](/documentation/homekit/hmcharacteristictypecurrentairpurifierstate)

###### Values

- [HMCharacteristicValueCurrentAirPurifierState](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate)

###### Air Purifier States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetAirPurifierState: String](/documentation/homekit/hmcharacteristictypetargetairpurifierstate)

###### Values

- [HMCharacteristicValueTargetAirPurifierState](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate)

###### Air Purifier States

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeFilterLifeLevel: String](/documentation/homekit/hmcharacteristictypefilterlifelevel)
- [let HMCharacteristicTypeFilterChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterchangeindication)

###### Values

- [HMCharacteristicValueFilterChange](/documentation/homekit/hmcharacteristicvaluefilterchange)

###### Filter Change Indicator

- [case notNeeded](/documentation/homekit/hmcharacteristicvaluefilterchange/notneeded)
- [case needed](/documentation/homekit/hmcharacteristicvaluefilterchange/needed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluefilterchange/init(rawvalue:))
- [let HMCharacteristicTypeFilterResetChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterresetchangeindication)

##### Water

- [let HMCharacteristicTypeWaterLevel: String](/documentation/homekit/hmcharacteristictypewaterlevel)
- [let HMCharacteristicTypeValveType: String](/documentation/homekit/hmcharacteristictypevalvetype)

###### Values

- [HMCharacteristicValueValveType](/documentation/homekit/hmcharacteristicvaluevalvetype)

###### Valve Types

- [case genericValve](/documentation/homekit/hmcharacteristicvaluevalvetype/genericvalve)
- [case irrigation](/documentation/homekit/hmcharacteristicvaluevalvetype/irrigation)
- [case showerHead](/documentation/homekit/hmcharacteristicvaluevalvetype/showerhead)
- [case waterFaucet](/documentation/homekit/hmcharacteristicvaluevalvetype/waterfaucet)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevalvetype/init(rawvalue:))
- [let HMCharacteristicTypeLeakDetected: String](/documentation/homekit/hmcharacteristictypeleakdetected)

###### Values

- [HMCharacteristicValueLeakStatus](/documentation/homekit/hmcharacteristicvalueleakstatus)

###### Leak Status

- [case none](/documentation/homekit/hmcharacteristicvalueleakstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvalueleakstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueleakstatus/init(rawvalue:))

##### Doors and windows

- [let HMCharacteristicTypeCurrentDoorState: String](/documentation/homekit/hmcharacteristictypecurrentdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetDoorState: String](/documentation/homekit/hmcharacteristictypetargetdoorstate)

###### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [HMCharacteristicValueTargetDoorState](/documentation/homekit/hmcharacteristicvaluetargetdoorstate)

###### Door States

- [case closed](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/closed)
- [case open](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/open)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentPosition: String](/documentation/homekit/hmcharacteristictypecurrentposition)
- [let HMCharacteristicTypeTargetPosition: String](/documentation/homekit/hmcharacteristictypetargetposition)
- [let HMCharacteristicTypePositionState: String](/documentation/homekit/hmcharacteristictypepositionstate)

###### Values

- [HMCharacteristicValuePositionState](/documentation/homekit/hmcharacteristicvaluepositionstate)

###### Position States

- [case closing](/documentation/homekit/hmcharacteristicvaluepositionstate/closing)
- [case opening](/documentation/homekit/hmcharacteristicvaluepositionstate/opening)
- [case stopped](/documentation/homekit/hmcharacteristicvaluepositionstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepositionstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusJammed: String](/documentation/homekit/hmcharacteristictypestatusjammed)

###### Values

- [HMCharacteristicValueJammedStatus](/documentation/homekit/hmcharacteristicvaluejammedstatus)

###### Jammed Status

- [case none](/documentation/homekit/hmcharacteristicvaluejammedstatus/none)
- [case jammed](/documentation/homekit/hmcharacteristicvaluejammedstatus/jammed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluejammedstatus/init(rawvalue:))
- [let HMCharacteristicTypeHoldPosition: String](/documentation/homekit/hmcharacteristictypeholdposition)
- [let HMCharacteristicTypeSlatType: String](/documentation/homekit/hmcharacteristictypeslattype)

###### Values

- [HMCharacteristicValueSlatType](/documentation/homekit/hmcharacteristicvalueslattype)

###### Slat Types

- [case horizontal](/documentation/homekit/hmcharacteristicvalueslattype/horizontal)
- [case vertical](/documentation/homekit/hmcharacteristicvalueslattype/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueslattype/init(rawvalue:))
- [let HMCharacteristicTypeCurrentSlatState: String](/documentation/homekit/hmcharacteristictypecurrentslatstate)

###### Values

- [HMCharacteristicValueCurrentSlatState](/documentation/homekit/hmcharacteristicvaluecurrentslatstate)

###### Slat States

- [case stationary](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/stationary)
- [case jammed](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/jammed)
- [case oscillating](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/oscillating)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/init(rawvalue:))

##### Tilting mechanisms

- [let HMCharacteristicTypeCurrentHorizontalTilt: String](/documentation/homekit/hmcharacteristictypecurrenthorizontaltilt)
- [let HMCharacteristicTypeTargetHorizontalTilt: String](/documentation/homekit/hmcharacteristictypetargethorizontaltilt)
- [let HMCharacteristicTypeCurrentVerticalTilt: String](/documentation/homekit/hmcharacteristictypecurrentverticaltilt)
- [let HMCharacteristicTypeTargetVerticalTilt: String](/documentation/homekit/hmcharacteristictypetargetverticaltilt)
- [let HMCharacteristicTypeCurrentTilt: String](/documentation/homekit/hmcharacteristictypecurrenttilt)
- [let HMCharacteristicTypeTargetTilt: String](/documentation/homekit/hmcharacteristictypetargettilt)

##### Locks and openers

- [let HMCharacteristicTypeLockManagementAutoSecureTimeout: String](/documentation/homekit/hmcharacteristictypelockmanagementautosecuretimeout)
- [let HMCharacteristicTypeLockManagementControlPoint: String](/documentation/homekit/hmcharacteristictypelockmanagementcontrolpoint)
- [let HMCharacteristicTypeLockMechanismLastKnownAction: String](/documentation/homekit/hmcharacteristictypelockmechanismlastknownaction)

###### Values

- [HMCharacteristicValueLockMechanismLastKnownAction](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction)

###### Lock Mechanism Actions

- [case securedRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedremotely)
- [case securedUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovement)
- [case securedUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementexterior)
- [case securedUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementinterior)
- [case securedWithAutomaticSecureTimeout](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithautomaticsecuretimeout)
- [case securedWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithkeypad)
- [case unsecuredRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredremotely)
- [case unsecuredUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovement)
- [case unsecuredUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementexterior)
- [case unsecuredUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementinterior)
- [case unsecuredWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredwithkeypad)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/init(rawvalue:))
- [let HMCharacteristicTypeLockPhysicalControls: String](/documentation/homekit/hmcharacteristictypelockphysicalcontrols)

###### Values

- [HMCharacteristicValueLockPhysicalControlsState](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate)

###### Lock Physical Control State

- [case notLocked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/notlocked)
- [case locked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/locked)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/init(rawvalue:))
- [let HMCharacteristicTypeMotionDetected: String](/documentation/homekit/hmcharacteristictypemotiondetected)
- [let HMCharacteristicTypeCurrentLockMechanismState: String](/documentation/homekit/hmcharacteristictypecurrentlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetLockMechanismState: String](/documentation/homekit/hmcharacteristictypetargetlockmechanismstate)

###### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [HMCharacteristicValueTargetLockMechanismState](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate)

###### Lock Mechanism States

- [case secured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/secured)
- [case unsecured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/unsecured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeRemoteKey: String](/documentation/homekit/hmcharacteristictyperemotekey)

###### Values

- [HMCharacteristicValueRemoteKey](/documentation/homekit/hmcharacteristicvalueremotekey)

###### Remote states

- [case arrowDown](/documentation/homekit/hmcharacteristicvalueremotekey/arrowdown)
- [case arrowLeft](/documentation/homekit/hmcharacteristicvalueremotekey/arrowleft)
- [case arrowRight](/documentation/homekit/hmcharacteristicvalueremotekey/arrowright)
- [case arrowUp](/documentation/homekit/hmcharacteristicvalueremotekey/arrowup)
- [case back](/documentation/homekit/hmcharacteristicvalueremotekey/back)
- [case exit](/documentation/homekit/hmcharacteristicvalueremotekey/exit)
- [case fastForward](/documentation/homekit/hmcharacteristicvalueremotekey/fastforward)
- [case home](/documentation/homekit/hmcharacteristicvalueremotekey/home)
- [case info](/documentation/homekit/hmcharacteristicvalueremotekey/info)
- [case menu](/documentation/homekit/hmcharacteristicvalueremotekey/menu)
- [case nextTrack](/documentation/homekit/hmcharacteristicvalueremotekey/nexttrack)
- [case pause](/documentation/homekit/hmcharacteristicvalueremotekey/pause)
- [case play](/documentation/homekit/hmcharacteristicvalueremotekey/play)
- [case playPause](/documentation/homekit/hmcharacteristicvalueremotekey/playpause)
- [case previousTrack](/documentation/homekit/hmcharacteristicvalueremotekey/previoustrack)
- [case rewind](/documentation/homekit/hmcharacteristicvalueremotekey/rewind)
- [case select](/documentation/homekit/hmcharacteristicvalueremotekey/select)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueremotekey/init(rawvalue:))

##### Safety and security

- [let HMCharacteristicTypeCurrentSecuritySystemState: String](/documentation/homekit/hmcharacteristictypecurrentsecuritysystemstate)

###### Values

- [HMCharacteristicValueCurrentSecuritySystemState](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/nightarm)
- [case disarmed](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/disarmed)
- [case triggered](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/triggered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetSecuritySystemState: String](/documentation/homekit/hmcharacteristictypetargetsecuritysystemstate)

###### Values

- [HMCharacteristicValueTargetSecuritySystemState](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/nightarm)
- [case disarm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/disarm)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeObstructionDetected: String](/documentation/homekit/hmcharacteristictypeobstructiondetected)
- [let HMCharacteristicTypeOccupancyDetected: String](/documentation/homekit/hmcharacteristictypeoccupancydetected)

###### Values

- [HMCharacteristicValueOccupancyStatus](/documentation/homekit/hmcharacteristicvalueoccupancystatus)

###### Occupancy Status

- [case notOccupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/notoccupied)
- [case occupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/occupied)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueoccupancystatus/init(rawvalue:))
- [let HMCharacteristicTypeSecuritySystemAlarmType: String](/documentation/homekit/hmcharacteristictypesecuritysystemalarmtype)

###### Values

- [HMCharacteristicValueSecuritySystemAlarmType](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype)

###### Alarm Types

- [case noAlarm](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/noalarm)
- [case unknown](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/init(rawvalue:))
- [let HMCharacteristicPropertyRequiresAuthorizationData: String](/documentation/homekit/hmcharacteristicpropertyrequiresauthorizationdata)

##### Audio and video

- [let HMCharacteristicTypeSupportedRTPConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedrtpconfiguration)
- [let HMCharacteristicTypeDigitalZoom: String](/documentation/homekit/hmcharacteristictypedigitalzoom)
- [let HMCharacteristicTypeOpticalZoom: String](/documentation/homekit/hmcharacteristictypeopticalzoom)
- [let HMCharacteristicTypeImageMirroring: String](/documentation/homekit/hmcharacteristictypeimagemirroring)
- [let HMCharacteristicTypeImageRotation: String](/documentation/homekit/hmcharacteristictypeimagerotation)
- [let HMCharacteristicTypeNightVision: String](/documentation/homekit/hmcharacteristictypenightvision)
- [let HMCharacteristicTypeStreamingStatus: String](/documentation/homekit/hmcharacteristictypestreamingstatus)
- [let HMCharacteristicTypeSupportedVideoStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedvideostreamconfiguration)
- [let HMCharacteristicTypeSupportedAudioStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedaudiostreamconfiguration)
- [let HMCharacteristicTypeSelectedStreamConfiguration: String](/documentation/homekit/hmcharacteristictypeselectedstreamconfiguration)
- [let HMCharacteristicTypeSetupStreamEndpoint: String](/documentation/homekit/hmcharacteristictypesetupstreamendpoint)
- [let HMCharacteristicTypeAudioFeedback: String](/documentation/homekit/hmcharacteristictypeaudiofeedback)
- [let HMCharacteristicTypeVolume: String](/documentation/homekit/hmcharacteristictypevolume)
- [let HMCharacteristicTypeMute: String](/documentation/homekit/hmcharacteristictypemute)
- [let HMCharacteristicTypeVolumeSelector: String](/documentation/homekit/hmcharacteristictypevolumeselector)

###### Values

- [HMCharacteristicValueVolumeSelector](/documentation/homekit/hmcharacteristicvaluevolumeselector)

###### Volume cases

- [case volumeDecrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumedecrement)
- [case volumeIncrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumeincrement)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumeselector/init(rawvalue:))
- [let HMCharacteristicTypeVolumeControlType: String](/documentation/homekit/hmcharacteristictypevolumecontroltype)

###### Values

- [HMCharacteristicValueVolumeControlType](/documentation/homekit/hmcharacteristicvaluevolumecontroltype)

###### Volume types

- [case absolute](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/absolute)
- [case none](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/none)
- [case relative](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relative)
- [case relativeWithCurrent](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relativewithcurrent)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/init(rawvalue:))
- [let HMCharacteristicTypeClosedCaptions: String](/documentation/homekit/hmcharacteristictypeclosedcaptions)

###### Values

- [HMCharacteristicValueClosedCaptions](/documentation/homekit/hmcharacteristicvalueclosedcaptions)

###### Closed caption states

- [case disabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueclosedcaptions/init(rawvalue:))
- [let HMCharacteristicTypePictureMode: String](/documentation/homekit/hmcharacteristictypepicturemode)

###### Values

- [HMCharacteristicValuePictureMode](/documentation/homekit/hmcharacteristicvaluepicturemode)

###### Television states

- [case bright](/documentation/homekit/hmcharacteristicvaluepicturemode/bright)
- [case calibrated](/documentation/homekit/hmcharacteristicvaluepicturemode/calibrated)
- [case computer](/documentation/homekit/hmcharacteristicvaluepicturemode/computer)
- [case custom1](/documentation/homekit/hmcharacteristicvaluepicturemode/custom1)
- [case custom2](/documentation/homekit/hmcharacteristicvaluepicturemode/custom2)
- [case custom3](/documentation/homekit/hmcharacteristicvaluepicturemode/custom3)
- [case dark](/documentation/homekit/hmcharacteristicvaluepicturemode/dark)
- [case game](/documentation/homekit/hmcharacteristicvaluepicturemode/game)
- [case movie](/documentation/homekit/hmcharacteristicvaluepicturemode/movie)
- [case night](/documentation/homekit/hmcharacteristicvaluepicturemode/night)
- [case photo](/documentation/homekit/hmcharacteristicvaluepicturemode/photo)
- [case sport](/documentation/homekit/hmcharacteristicvaluepicturemode/sport)
- [case standard](/documentation/homekit/hmcharacteristicvaluepicturemode/standard)
- [case vivid](/documentation/homekit/hmcharacteristicvaluepicturemode/vivid)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepicturemode/init(rawvalue:))

##### General state

- [let HMCharacteristicTypeActive: String](/documentation/homekit/hmcharacteristictypeactive)

###### Values

- [HMCharacteristicValueActivationState](/documentation/homekit/hmcharacteristicvalueactivationstate)

###### Activation States

- [case inactive](/documentation/homekit/hmcharacteristicvalueactivationstate/inactive)
- [case active](/documentation/homekit/hmcharacteristicvalueactivationstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueactivationstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusTampered: String](/documentation/homekit/hmcharacteristictypestatustampered)

###### Values

- [HMCharacteristicValueTamperedStatus](/documentation/homekit/hmcharacteristicvaluetamperedstatus)

###### Tampered Status

- [case none](/documentation/homekit/hmcharacteristicvaluetamperedstatus/none)
- [case tampered](/documentation/homekit/hmcharacteristicvaluetamperedstatus/tampered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetamperedstatus/init(rawvalue:))
- [let HMCharacteristicTypeStatusFault: String](/documentation/homekit/hmcharacteristictypestatusfault)

###### Values

- [HMCharacteristicValueStatusFault](/documentation/homekit/hmcharacteristicvaluestatusfault)

###### Fault Status

- [case noFault](/documentation/homekit/hmcharacteristicvaluestatusfault/nofault)
- [case generalFault](/documentation/homekit/hmcharacteristicvaluestatusfault/generalfault)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluestatusfault/init(rawvalue:))
- [let HMCharacteristicTypeStatusActive: String](/documentation/homekit/hmcharacteristictypestatusactive)
- [let HMCharacteristicTypeInUse: String](/documentation/homekit/hmcharacteristictypeinuse)

###### Values

- [HMCharacteristicValueUsageState](/documentation/homekit/hmcharacteristicvalueusagestate)

###### Usage States

- [case notInUse](/documentation/homekit/hmcharacteristicvalueusagestate/notinuse)
- [case inUse](/documentation/homekit/hmcharacteristicvalueusagestate/inuse)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueusagestate/init(rawvalue:))
- [let HMCharacteristicTypeIsConfigured: String](/documentation/homekit/hmcharacteristictypeisconfigured)

###### Values

- [HMCharacteristicValueConfigurationState](/documentation/homekit/hmcharacteristicvalueconfigurationstate)

###### Configuration States

- [case notConfigured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/notconfigured)
- [case configured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/configured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueconfigurationstate/init(rawvalue:))
- [let HMCharacteristicTypeRemainingDuration: String](/documentation/homekit/hmcharacteristictyperemainingduration)
- [let HMCharacteristicTypeSetDuration: String](/documentation/homekit/hmcharacteristictypesetduration)
- [let HMCharacteristicTypeProgramMode: String](/documentation/homekit/hmcharacteristictypeprogrammode)

###### Values

- [HMCharacteristicValueProgramMode](/documentation/homekit/hmcharacteristicvalueprogrammode)

###### Constants

- [case notScheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/notscheduled)
- [case scheduleOverriddenToManual](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduleoverriddentomanual)
- [case scheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueprogrammode/init(rawvalue:))
- [let HMCharacteristicTypeWiFiSatelliteStatus: String](/documentation/homekit/hmcharacteristictypewifisatellitestatus)

###### Values

- [HMCharacteristicValueWiFiSatelliteStatus](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus)

###### Network states

- [case connected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/connected)
- [case notConnected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/notconnected)
- [case unknown](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/init(rawvalue:))
- [let HMCharacteristicTypeWANStatusList: String](/documentation/homekit/hmcharacteristictypewanstatuslist)
- [let HMCharacteristicTypeTargetMediaState: String](/documentation/homekit/hmcharacteristictypetargetmediastate)

###### Values

- [HMCharacteristicValueTargetMediaState](/documentation/homekit/hmcharacteristicvaluetargetmediastate)

###### Media states

- [case pause](/documentation/homekit/hmcharacteristicvaluetargetmediastate/pause)
- [case play](/documentation/homekit/hmcharacteristicvaluetargetmediastate/play)
- [case stop](/documentation/homekit/hmcharacteristicvaluetargetmediastate/stop)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetmediastate/init(rawvalue:))
- [let HMCharacteristicTypeRouterStatus: String](/documentation/homekit/hmcharacteristictyperouterstatus)

###### Values

- [HMCharacteristicValueRouterStatus](/documentation/homekit/hmcharacteristicvaluerouterstatus)

###### Router states

- [case notReady](/documentation/homekit/hmcharacteristicvaluerouterstatus/notready)
- [case ready](/documentation/homekit/hmcharacteristicvaluerouterstatus/ready)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerouterstatus/init(rawvalue:))
- [let HMCharacteristicTypeCurrentMediaState: String](/documentation/homekit/hmcharacteristictypecurrentmediastate)

###### Values

- [HMCharacteristicValueCurrentMediaState](/documentation/homekit/hmcharacteristicvaluecurrentmediastate)

###### Current media states

- [case interrupted](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/interrupted)
- [case loading](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/loading)
- [case paused](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/paused)
- [case playing](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/playing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/stopped)
- [case unknown](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentVisibilityState: String](/documentation/homekit/hmcharacteristictypecurrentvisibilitystate)

###### Values

- [HMCharacteristicValueCurrentVisibilityState](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate)

###### Visibility states

- [case alwaysShown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/alwaysshown)
- [case connected](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/connected)
- [case hidden](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/hidden)
- [case shown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/shown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/init(rawvalue:))
- [let HMCharacteristicTypeTargetVisibilityState: String](/documentation/homekit/hmcharacteristictypetargetvisibilitystate)

###### Values

- [HMCharacteristicValueTargetVisibilityState](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate)

###### Visibility states

- [case hide](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/init(rawvalue:))
- [let HMCharacteristicPropertySupportsEventNotification: String](/documentation/homekit/hmcharacteristicpropertysupportseventnotification-2f0ml)

##### Accessory identification

- [let HMCharacteristicTypeName: String](/documentation/homekit/hmcharacteristictypename)
- [let HMCharacteristicTypeIdentify: String](/documentation/homekit/hmcharacteristictypeidentify)
- [let HMCharacteristicTypeVersion: String](/documentation/homekit/hmcharacteristictypeversion)
- [let HMCharacteristicTypeLogs: String](/documentation/homekit/hmcharacteristictypelogs)
- [let HMCharacteristicTypeAdminOnlyAccess: String](/documentation/homekit/hmcharacteristictypeadminonlyaccess)
- [let HMCharacteristicTypeHardwareVersion: String](/documentation/homekit/hmcharacteristictypehardwareversion)
- [let HMCharacteristicTypeSoftwareVersion: String](/documentation/homekit/hmcharacteristictypesoftwareversion)
- [let HMCharacteristicTypeLabelIndex: String](/documentation/homekit/hmcharacteristictypelabelindex)
- [let HMCharacteristicTypeLabelNamespace: String](/documentation/homekit/hmcharacteristictypelabelnamespace)

###### Values

- [HMCharacteristicValueLabelNamespace](/documentation/homekit/hmcharacteristicvaluelabelnamespace)

###### Namespaces

- [case dot](/documentation/homekit/hmcharacteristicvaluelabelnamespace/dot)
- [case numeral](/documentation/homekit/hmcharacteristicvaluelabelnamespace/numeral)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelabelnamespace/init(rawvalue:))
- [let HMCharacteristicTypeActiveIdentifier: String](/documentation/homekit/hmcharacteristictypeactiveidentifier)
- [let HMCharacteristicTypeIdentifier: String](/documentation/homekit/hmcharacteristictypeidentifier)
- [let HMCharacteristicTypeInputDeviceType: String](/documentation/homekit/hmcharacteristictypeinputdevicetype)

###### Values

- [HMCharacteristicValueInputDeviceType](/documentation/homekit/hmcharacteristicvalueinputdevicetype)

###### Input devices

- [case audioSystem](/documentation/homekit/hmcharacteristicvalueinputdevicetype/audiosystem)
- [case none](/documentation/homekit/hmcharacteristicvalueinputdevicetype/none)
- [case other](/documentation/homekit/hmcharacteristicvalueinputdevicetype/other)
- [case playback](/documentation/homekit/hmcharacteristicvalueinputdevicetype/playback)
- [case recording](/documentation/homekit/hmcharacteristicvalueinputdevicetype/recording)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tuner)
- [case tv](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tv)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputdevicetype/init(rawvalue:))
- [let HMCharacteristicTypeInputSourceType: String](/documentation/homekit/hmcharacteristictypeinputsourcetype)

###### Values

- [HMCharacteristicValueInputSourceType](/documentation/homekit/hmcharacteristicvalueinputsourcetype)

###### Accessory source types

- [case airPlay](/documentation/homekit/hmcharacteristicvalueinputsourcetype/airplay)
- [case application](/documentation/homekit/hmcharacteristicvalueinputsourcetype/application)
- [case componentVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/componentvideo)
- [case compositeVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/compositevideo)
- [case dvi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/dvi)
- [case hdmi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/hdmi)
- [case homeScreen](/documentation/homekit/hmcharacteristicvalueinputsourcetype/homescreen)
- [case other](/documentation/homekit/hmcharacteristicvalueinputsourcetype/other)
- [case sVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/svideo)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputsourcetype/tuner)
- [case usb](/documentation/homekit/hmcharacteristicvalueinputsourcetype/usb)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputsourcetype/init(rawvalue:))
- [let HMCharacteristicTypeConfiguredName: String](/documentation/homekit/hmcharacteristictypeconfiguredname)

##### Deprecated characteristic types

- [let HMCharacteristicTypeManufacturer: String](/documentation/homekit/hmcharacteristictypemanufacturer)
- [let HMCharacteristicTypeModel: String](/documentation/homekit/hmcharacteristictypemodel)
- [let HMCharacteristicTypeFirmwareVersion: String](/documentation/homekit/hmcharacteristictypefirmwareversion)
- [let HMCharacteristicTypeSerialNumber: String](/documentation/homekit/hmcharacteristictypeserialnumber)

#### Controlling a characteristic

- [var value: Any?](/documentation/homekit/hmcharacteristic/value)
- [func readValue(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/readvalue(completionhandler:))
- [func writeValue(Any?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/writevalue(_:completionhandler:))
- [func updateAuthorizationData(Data?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/updateauthorizationdata(_:completionhandler:))

#### Managing characteristic presentation

- [var metadata: HMCharacteristicMetadata?](/documentation/homekit/hmcharacteristic/metadata)
- [HMCharacteristicMetadata](/documentation/homekit/hmcharacteristicmetadata)

##### Describing a characteristic

- [var manufacturerDescription: String?](/documentation/homekit/hmcharacteristicmetadata/manufacturerdescription)

##### Bounding the value

- [var validValues: [NSNumber]?](/documentation/homekit/hmcharacteristicmetadata/validvalues)
- [var minimumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/minimumvalue)
- [var maximumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maximumvalue)
- [var stepValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/stepvalue)
- [var maxLength: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maxlength)

##### Formatting the value

- [var format: String?](/documentation/homekit/hmcharacteristicmetadata/format)
- [Characteristic Data Formats](/documentation/homekit/characteristic-data-formats)

###### Booleans

- [let HMCharacteristicMetadataFormatBool: String](/documentation/homekit/hmcharacteristicmetadataformatbool)

###### Strings

- [let HMCharacteristicMetadataFormatString: String](/documentation/homekit/hmcharacteristicmetadataformatstring)

###### Signed Values

- [let HMCharacteristicMetadataFormatInt: String](/documentation/homekit/hmcharacteristicmetadataformatint)
- [let HMCharacteristicMetadataFormatFloat: String](/documentation/homekit/hmcharacteristicmetadataformatfloat)

###### Unsigned Integers

- [let HMCharacteristicMetadataFormatUInt8: String](/documentation/homekit/hmcharacteristicmetadataformatuint8)
- [let HMCharacteristicMetadataFormatUInt16: String](/documentation/homekit/hmcharacteristicmetadataformatuint16)
- [let HMCharacteristicMetadataFormatUInt32: String](/documentation/homekit/hmcharacteristicmetadataformatuint32)
- [let HMCharacteristicMetadataFormatUInt64: String](/documentation/homekit/hmcharacteristicmetadataformatuint64)

###### Data

- [let HMCharacteristicMetadataFormatData: String](/documentation/homekit/hmcharacteristicmetadataformatdata)
- [let HMCharacteristicMetadataFormatTLV8: String](/documentation/homekit/hmcharacteristicmetadataformattlv8)

###### Collections

- [let HMCharacteristicMetadataFormatArray: String](/documentation/homekit/hmcharacteristicmetadataformatarray)
- [let HMCharacteristicMetadataFormatDictionary: String](/documentation/homekit/hmcharacteristicmetadataformatdictionary)

##### Specifying units

- [var units: String?](/documentation/homekit/hmcharacteristicmetadata/units)
- [Characteristic Units](/documentation/homekit/characteristic-units)

###### Parts Per Total

- [let HMCharacteristicMetadataUnitsPercentage: String](/documentation/homekit/hmcharacteristicmetadataunitspercentage)
- [let HMCharacteristicMetadataUnitsPartsPerMillion: String](/documentation/homekit/hmcharacteristicmetadataunitspartspermillion)

###### Temperature

- [let HMCharacteristicMetadataUnitsCelsius: String](/documentation/homekit/hmcharacteristicmetadataunitscelsius)
- [let HMCharacteristicMetadataUnitsFahrenheit: String](/documentation/homekit/hmcharacteristicmetadataunitsfahrenheit)

###### Time

- [let HMCharacteristicMetadataUnitsSeconds: String](/documentation/homekit/hmcharacteristicmetadataunitsseconds)

###### Light

- [let HMCharacteristicMetadataUnitsLux: String](/documentation/homekit/hmcharacteristicmetadataunitslux)

###### Mass

- [let HMCharacteristicMetadataUnitsMicrogramsPerCubicMeter: String](/documentation/homekit/hmcharacteristicmetadataunitsmicrogramspercubicmeter)

###### Rotation

- [let HMCharacteristicMetadataUnitsArcDegree: String](/documentation/homekit/hmcharacteristicmetadataunitsarcdegree)

##### Initializers

- [init()](/documentation/homekit/hmcharacteristicmetadata/init())

#### Receiving change notifications

- [func enableNotification(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/enablenotification(_:completionhandler:))
- [var isNotificationEnabled: Bool](/documentation/homekit/hmcharacteristic/isnotificationenabled)

#### Getting the characterized service

- [var service: HMService?](/documentation/homekit/hmcharacteristic/service)

#### Initializers

- [init()](/documentation/homekit/hmcharacteristic/init())

### Identifying the service

- [var name: String](/documentation/homekit/hmservice/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updatename(_:completionhandler:))
- [var uniqueIdentifier: UUID](/documentation/homekit/hmservice/uniqueidentifier)

### Getting the service type

- [var serviceType: String](/documentation/homekit/hmservice/servicetype)
- [Accessory Service Types](/documentation/homekit/accessory-service-types)

#### Light

- [let HMServiceTypeLightbulb: String](/documentation/homekit/hmservicetypelightbulb)
- [let HMServiceTypeLightSensor: String](/documentation/homekit/hmservicetypelightsensor)

#### Power and Switches

- [let HMServiceTypeSwitch: String](/documentation/homekit/hmservicetypeswitch)
- [let HMServiceTypeBattery: String](/documentation/homekit/hmservicetypebattery)
- [let HMServiceTypeOutlet: String](/documentation/homekit/hmservicetypeoutlet)
- [let HMServiceTypeStatefulProgrammableSwitch: String](/documentation/homekit/hmservicetypestatefulprogrammableswitch)
- [let HMServiceTypeStatelessProgrammableSwitch: String](/documentation/homekit/hmservicetypestatelessprogrammableswitch)

#### Air Quality and Smoke Detection

- [let HMServiceTypeAirPurifier: String](/documentation/homekit/hmservicetypeairpurifier)
- [let HMServiceTypeAirQualitySensor: String](/documentation/homekit/hmservicetypeairqualitysensor)
- [let HMServiceTypeCarbonDioxideSensor: String](/documentation/homekit/hmservicetypecarbondioxidesensor)
- [let HMServiceTypeCarbonMonoxideSensor: String](/documentation/homekit/hmservicetypecarbonmonoxidesensor)
- [let HMServiceTypeSmokeSensor: String](/documentation/homekit/hmservicetypesmokesensor)

#### Temperature and Humidity

- [let HMServiceTypeHeaterCooler: String](/documentation/homekit/hmservicetypeheatercooler)
- [let HMServiceTypeTemperatureSensor: String](/documentation/homekit/hmservicetypetemperaturesensor)
- [let HMServiceTypeThermostat: String](/documentation/homekit/hmservicetypethermostat)
- [let HMServiceTypeFan: String](/documentation/homekit/hmservicetypefan)
- [let HMServiceTypeFilterMaintenance: String](/documentation/homekit/hmservicetypefiltermaintenance)
- [let HMServiceTypeHumidifierDehumidifier: String](/documentation/homekit/hmservicetypehumidifierdehumidifier)
- [let HMServiceTypeHumiditySensor: String](/documentation/homekit/hmservicetypehumiditysensor)
- [let HMServiceTypeVentilationFan: String](/documentation/homekit/hmservicetypeventilationfan)

#### Windows

- [let HMServiceTypeWindow: String](/documentation/homekit/hmservicetypewindow)
- [let HMServiceTypeWindowCovering: String](/documentation/homekit/hmservicetypewindowcovering)
- [let HMServiceTypeSlats: String](/documentation/homekit/hmservicetypeslats)

#### Water

- [let HMServiceTypeFaucet: String](/documentation/homekit/hmservicetypefaucet)
- [let HMServiceTypeValve: String](/documentation/homekit/hmservicetypevalve)
- [let HMServiceTypeIrrigationSystem: String](/documentation/homekit/hmservicetypeirrigationsystem)
- [let HMServiceTypeLeakSensor: String](/documentation/homekit/hmservicetypeleaksensor)

#### Locks and Openers

- [let HMServiceTypeDoor: String](/documentation/homekit/hmservicetypedoor)
- [let HMServiceTypeDoorbell: String](/documentation/homekit/hmservicetypedoorbell)
- [let HMServiceTypeGarageDoorOpener: String](/documentation/homekit/hmservicetypegaragedooropener)
- [let HMServiceTypeLockManagement: String](/documentation/homekit/hmservicetypelockmanagement)
- [let HMServiceTypeLockMechanism: String](/documentation/homekit/hmservicetypelockmechanism)

#### Safety and Security

- [let HMServiceTypeMotionSensor: String](/documentation/homekit/hmservicetypemotionsensor)
- [let HMServiceTypeOccupancySensor: String](/documentation/homekit/hmservicetypeoccupancysensor)
- [let HMServiceTypeSecuritySystem: String](/documentation/homekit/hmservicetypesecuritysystem)
- [let HMServiceTypeContactSensor: String](/documentation/homekit/hmservicetypecontactsensor)

#### Video and Audio

- [let HMServiceTypeCameraControl: String](/documentation/homekit/hmservicetypecameracontrol)
- [let HMServiceTypeCameraRTPStreamManagement: String](/documentation/homekit/hmservicetypecamerartpstreammanagement)
- [let HMServiceTypeMicrophone: String](/documentation/homekit/hmservicetypemicrophone)
- [let HMServiceTypeSpeaker: String](/documentation/homekit/hmservicetypespeaker)
- [let HMServiceTypeInputSource: String](/documentation/homekit/hmservicetypeinputsource)
- [let HMServiceTypeTelevision: String](/documentation/homekit/hmservicetypetelevision)

#### Network

- [let HMServiceTypeWiFiRouter: String](/documentation/homekit/hmservicetypewifirouter)
- [let HMServiceTypeWiFiSatellite: String](/documentation/homekit/hmservicetypewifisatellite)

#### Information

- [let HMServiceTypeLabel: String](/documentation/homekit/hmservicetypelabel)
- [let HMServiceTypeAccessoryInformation: String](/documentation/homekit/hmservicetypeaccessoryinformation)
- [var localizedDescription: String](/documentation/homekit/hmservice/localizeddescription)

### Reading service properties

- [var isPrimaryService: Bool](/documentation/homekit/hmservice/isprimaryservice)
- [var isUserInteractive: Bool](/documentation/homekit/hmservice/isuserinteractive)

### Associating a secondary service

- [var associatedServiceType: String?](/documentation/homekit/hmservice/associatedservicetype)
- [func updateAssociatedServiceType(String?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmservice/updateassociatedservicetype(_:completionhandler:))

### Finding the linked services

- [var linkedServices: [HMService]?](/documentation/homekit/hmservice/linkedservices)

### Getting the service’s provider

- [var accessory: HMAccessory?](/documentation/homekit/hmservice/accessory)

### Initializers

- [init()](/documentation/homekit/hmservice/init())

### Instance Properties

- [var matterEndpointID: UInt16?](/documentation/homekit/hmservice/matterendpointid-62vu6)
- [HMCharacteristic](/documentation/homekit/hmcharacteristic)

### Identifying a characteristic

- [var uniqueIdentifier: UUID](/documentation/homekit/hmcharacteristic/uniqueidentifier)
- [var localizedDescription: String](/documentation/homekit/hmcharacteristic/localizeddescription)

### Reading characteristic properties

- [var properties: [String]](/documentation/homekit/hmcharacteristic/properties)
- [Characteristic Properties](/documentation/homekit/characteristic-properties)

#### Properties of Characteristics

- [let HMCharacteristicPropertyReadable: String](/documentation/homekit/hmcharacteristicpropertyreadable)
- [let HMCharacteristicPropertyWritable: String](/documentation/homekit/hmcharacteristicpropertywritable)
- [let HMCharacteristicPropertyHidden: String](/documentation/homekit/hmcharacteristicpropertyhidden)

### Determining what a characteristic controls

- [var characteristicType: String](/documentation/homekit/hmcharacteristic/characteristictype)
- [Characteristic types](/documentation/homekit/characteristic-types)

#### Light

- [let HMCharacteristicTypeCurrentLightLevel: String](/documentation/homekit/hmcharacteristictypecurrentlightlevel)
- [let HMCharacteristicTypeHue: String](/documentation/homekit/hmcharacteristictypehue)
- [let HMCharacteristicTypeBrightness: String](/documentation/homekit/hmcharacteristictypebrightness)
- [let HMCharacteristicTypeSaturation: String](/documentation/homekit/hmcharacteristictypesaturation)
- [let HMCharacteristicTypeColorTemperature: String](/documentation/homekit/hmcharacteristictypecolortemperature)

#### Power and switches

- [let HMCharacteristicTypeBatteryLevel: String](/documentation/homekit/hmcharacteristictypebatterylevel)
- [let HMCharacteristicTypeChargingState: String](/documentation/homekit/hmcharacteristictypechargingstate)

##### Values

- [HMCharacteristicValueChargingState](/documentation/homekit/hmcharacteristicvaluechargingstate)

###### Charging States

- [case none](/documentation/homekit/hmcharacteristicvaluechargingstate/none)
- [case inProgress](/documentation/homekit/hmcharacteristicvaluechargingstate/inprogress)
- [case notChargeable](/documentation/homekit/hmcharacteristicvaluechargingstate/notchargeable)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluechargingstate/init(rawvalue:))
- [let HMCharacteristicTypeContactState: String](/documentation/homekit/hmcharacteristictypecontactstate)

##### Values

- [HMCharacteristicValueContactState](/documentation/homekit/hmcharacteristicvaluecontactstate)

###### Contact Sensor State

- [case detected](/documentation/homekit/hmcharacteristicvaluecontactstate/detected)
- [case none](/documentation/homekit/hmcharacteristicvaluecontactstate/none)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecontactstate/init(rawvalue:))
- [let HMCharacteristicTypeOutletInUse: String](/documentation/homekit/hmcharacteristictypeoutletinuse)
- [let HMCharacteristicTypePowerState: String](/documentation/homekit/hmcharacteristictypepowerstate)
- [let HMCharacteristicTypeStatusLowBattery: String](/documentation/homekit/hmcharacteristictypestatuslowbattery)

##### Values

- [HMCharacteristicValueBatteryStatus](/documentation/homekit/hmcharacteristicvaluebatterystatus)

###### Battery Status

- [case normal](/documentation/homekit/hmcharacteristicvaluebatterystatus/normal)
- [case low](/documentation/homekit/hmcharacteristicvaluebatterystatus/low)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluebatterystatus/init(rawvalue:))
- [let HMCharacteristicTypeOutputState: String](/documentation/homekit/hmcharacteristictypeoutputstate)
- [let HMCharacteristicTypeInputEvent: String](/documentation/homekit/hmcharacteristictypeinputevent)

##### Values

- [HMCharacteristicValueInputEvent](/documentation/homekit/hmcharacteristicvalueinputevent)

###### Input Events

- [case singlePress](/documentation/homekit/hmcharacteristicvalueinputevent/singlepress)
- [case doublePress](/documentation/homekit/hmcharacteristicvalueinputevent/doublepress)
- [case longPress](/documentation/homekit/hmcharacteristicvalueinputevent/longpress)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputevent/init(rawvalue:))
- [let HMCharacteristicTypePowerModeSelection: String](/documentation/homekit/hmcharacteristictypepowermodeselection)

##### Values

- [HMCharacteristicValuePowerModeSelection](/documentation/homekit/hmcharacteristicvaluepowermodeselection)

###### Power mode status

- [case hide](/documentation/homekit/hmcharacteristicvaluepowermodeselection/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluepowermodeselection/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepowermodeselection/init(rawvalue:))

#### Temperature

- [let HMCharacteristicTypeCurrentTemperature: String](/documentation/homekit/hmcharacteristictypecurrenttemperature)
- [let HMCharacteristicTypeTargetTemperature: String](/documentation/homekit/hmcharacteristictypetargettemperature)
- [let HMCharacteristicTypeTemperatureUnits: String](/documentation/homekit/hmcharacteristictypetemperatureunits)

##### Values

- [HMCharacteristicValueTemperatureUnit](/documentation/homekit/hmcharacteristicvaluetemperatureunit)

###### Temperature Units

- [case celsius](/documentation/homekit/hmcharacteristicvaluetemperatureunit/celsius)
- [case fahrenheit](/documentation/homekit/hmcharacteristicvaluetemperatureunit/fahrenheit)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetemperatureunit/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeatingCooling: String](/documentation/homekit/hmcharacteristictypetargetheatingcooling)

##### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeatingCooling: String](/documentation/homekit/hmcharacteristictypecurrentheatingcooling)

##### Values

- [HMCharacteristicValueHeatingCooling](/documentation/homekit/hmcharacteristicvalueheatingcooling)

###### Accesory State

- [case off](/documentation/homekit/hmcharacteristicvalueheatingcooling/off)
- [case heat](/documentation/homekit/hmcharacteristicvalueheatingcooling/heat)
- [case cool](/documentation/homekit/hmcharacteristicvalueheatingcooling/cool)
- [case auto](/documentation/homekit/hmcharacteristicvalueheatingcooling/auto)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueheatingcooling/init(rawvalue:))
- [HMCharacteristicValueCurrentHeatingCooling](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling)

###### Temperature States

- [case cool](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/cool)
- [case heat](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/heat)
- [case off](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/off)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatingcooling/init(rawvalue:))
- [let HMCharacteristicTypeTargetHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypetargetheatercoolerstate)

##### Values

- [HMCharacteristicValueTargetHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate)

###### Target State

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/automatic)
- [case heat](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/heat)
- [case cool](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/cool)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentHeaterCoolerState: String](/documentation/homekit/hmcharacteristictypecurrentheatercoolerstate)

##### Values

- [HMCharacteristicValueCurrentHeaterCoolerState](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate)

###### Current State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/idle)
- [case heating](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/heating)
- [case cooling](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/cooling)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentheatercoolerstate/init(rawvalue:))
- [let HMCharacteristicTypeCoolingThreshold: String](/documentation/homekit/hmcharacteristictypecoolingthreshold)
- [let HMCharacteristicTypeHeatingThreshold: String](/documentation/homekit/hmcharacteristictypeheatingthreshold)

#### Humidity

- [let HMCharacteristicTypeCurrentRelativeHumidity: String](/documentation/homekit/hmcharacteristictypecurrentrelativehumidity)
- [let HMCharacteristicTypeTargetRelativeHumidity: String](/documentation/homekit/hmcharacteristictypetargetrelativehumidity)
- [let HMCharacteristicTypeCurrentHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypecurrenthumidifierdehumidifierstate)

##### Values

- [HMCharacteristicValueCurrentHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate)

###### Current States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/idle)
- [case humidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/humidifying)
- [case dehumidifying](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/dehumidifying)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrenthumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetHumidifierDehumidifierState: String](/documentation/homekit/hmcharacteristictypetargethumidifierdehumidifierstate)

##### Values

- [HMCharacteristicValueTargetHumidifierDehumidifierState](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate)

###### Target States

- [case automatic](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/automatic)
- [case humidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/humidify)
- [case dehumidify](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/dehumidify)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargethumidifierdehumidifierstate/init(rawvalue:))
- [let HMCharacteristicTypeHumidifierThreshold: String](/documentation/homekit/hmcharacteristictypehumidifierthreshold)
- [let HMCharacteristicTypeDehumidifierThreshold: String](/documentation/homekit/hmcharacteristictypedehumidifierthreshold)

#### Air quality and smoke detection

- [let HMCharacteristicTypeAirQuality: String](/documentation/homekit/hmcharacteristictypeairquality)

##### Values

- [HMCharacteristicValueAirQuality](/documentation/homekit/hmcharacteristicvalueairquality)

###### Air Quality

- [case unknown](/documentation/homekit/hmcharacteristicvalueairquality/unknown)
- [case excellent](/documentation/homekit/hmcharacteristicvalueairquality/excellent)
- [case good](/documentation/homekit/hmcharacteristicvalueairquality/good)
- [case fair](/documentation/homekit/hmcharacteristicvalueairquality/fair)
- [case inferior](/documentation/homekit/hmcharacteristicvalueairquality/inferior)
- [case poor](/documentation/homekit/hmcharacteristicvalueairquality/poor)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairquality/init(rawvalue:))
- [let HMCharacteristicTypeAirParticulateDensity: String](/documentation/homekit/hmcharacteristictypeairparticulatedensity)
- [let HMCharacteristicTypeAirParticulateSize: String](/documentation/homekit/hmcharacteristictypeairparticulatesize)

##### Values

- [HMCharacteristicValueAirParticulateSize](/documentation/homekit/hmcharacteristicvalueairparticulatesize)

###### Air Particulate Sizes

- [case size2_5](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size2_5)
- [case size10](/documentation/homekit/hmcharacteristicvalueairparticulatesize/size10)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueairparticulatesize/init(rawvalue:))
- [let HMCharacteristicTypeSmokeDetected: String](/documentation/homekit/hmcharacteristictypesmokedetected)

##### Values

- [HMCharacteristicValueSmokeDetectionStatus](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus)

###### Smoke Detection Status

- [case none](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesmokedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideDetected: String](/documentation/homekit/hmcharacteristictypecarbondioxidedetected)

##### Values

- [HMCharacteristicValueCarbonDioxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus)

###### Carbon Dioxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbondioxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonDioxideLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidelevel)
- [let HMCharacteristicTypeCarbonDioxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbondioxidepeaklevel)
- [let HMCharacteristicTypeCarbonMonoxideDetected: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidedetected)

##### Values

- [HMCharacteristicValueCarbonMonoxideDetectionStatus](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus)

###### Carbon Monoxide Levels

- [case notDetected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/notdetected)
- [case detected](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecarbonmonoxidedetectionstatus/init(rawvalue:))
- [let HMCharacteristicTypeCarbonMonoxideLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidelevel)
- [let HMCharacteristicTypeCarbonMonoxidePeakLevel: String](/documentation/homekit/hmcharacteristictypecarbonmonoxidepeaklevel)
- [let HMCharacteristicTypeNitrogenDioxideDensity: String](/documentation/homekit/hmcharacteristictypenitrogendioxidedensity)
- [let HMCharacteristicTypeOzoneDensity: String](/documentation/homekit/hmcharacteristictypeozonedensity)
- [let HMCharacteristicTypePM10Density: String](/documentation/homekit/hmcharacteristictypepm10density)
- [let HMCharacteristicTypePM2_5Density: String](/documentation/homekit/hmcharacteristictypepm2_5density)
- [let HMCharacteristicTypeSulphurDioxideDensity: String](/documentation/homekit/hmcharacteristictypesulphurdioxidedensity)
- [let HMCharacteristicTypeVolatileOrganicCompoundDensity: String](/documentation/homekit/hmcharacteristictypevolatileorganiccompounddensity)

#### Fans

- [let HMCharacteristicTypeCurrentFanState: String](/documentation/homekit/hmcharacteristictypecurrentfanstate)

##### Values

- [HMCharacteristicValueCurrentFanState](/documentation/homekit/hmcharacteristicvaluecurrentfanstate)

###### Fan State

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentfanstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetFanState: String](/documentation/homekit/hmcharacteristictypetargetfanstate)

##### Values

- [HMCharacteristicValueTargetFanState](/documentation/homekit/hmcharacteristicvaluetargetfanstate)

###### Fan State

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetfanstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetfanstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetfanstate/init(rawvalue:))
- [let HMCharacteristicTypeRotationDirection: String](/documentation/homekit/hmcharacteristictyperotationdirection)

##### Values

- [HMCharacteristicValueRotationDirection](/documentation/homekit/hmcharacteristicvaluerotationdirection)

###### Rotation

- [case clockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/clockwise)
- [case counterClockwise](/documentation/homekit/hmcharacteristicvaluerotationdirection/counterclockwise)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerotationdirection/init(rawvalue:))
- [let HMCharacteristicTypeRotationSpeed: String](/documentation/homekit/hmcharacteristictyperotationspeed)
- [let HMCharacteristicTypeSwingMode: String](/documentation/homekit/hmcharacteristictypeswingmode)

##### Values

- [HMCharacteristicValueSwingMode](/documentation/homekit/hmcharacteristicvalueswingmode)

###### Movement Mode

- [case disabled](/documentation/homekit/hmcharacteristicvalueswingmode/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueswingmode/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueswingmode/init(rawvalue:))

#### Purifiers and filters

- [let HMCharacteristicTypeCurrentAirPurifierState: String](/documentation/homekit/hmcharacteristictypecurrentairpurifierstate)

##### Values

- [HMCharacteristicValueCurrentAirPurifierState](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate)

###### Air Purifier States

- [case inactive](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/inactive)
- [case idle](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/idle)
- [case active](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetAirPurifierState: String](/documentation/homekit/hmcharacteristictypetargetairpurifierstate)

##### Values

- [HMCharacteristicValueTargetAirPurifierState](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate)

###### Air Purifier States

- [case manual](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/manual)
- [case automatic](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/automatic)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetairpurifierstate/init(rawvalue:))
- [let HMCharacteristicTypeFilterLifeLevel: String](/documentation/homekit/hmcharacteristictypefilterlifelevel)
- [let HMCharacteristicTypeFilterChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterchangeindication)

##### Values

- [HMCharacteristicValueFilterChange](/documentation/homekit/hmcharacteristicvaluefilterchange)

###### Filter Change Indicator

- [case notNeeded](/documentation/homekit/hmcharacteristicvaluefilterchange/notneeded)
- [case needed](/documentation/homekit/hmcharacteristicvaluefilterchange/needed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluefilterchange/init(rawvalue:))
- [let HMCharacteristicTypeFilterResetChangeIndication: String](/documentation/homekit/hmcharacteristictypefilterresetchangeindication)

#### Water

- [let HMCharacteristicTypeWaterLevel: String](/documentation/homekit/hmcharacteristictypewaterlevel)
- [let HMCharacteristicTypeValveType: String](/documentation/homekit/hmcharacteristictypevalvetype)

##### Values

- [HMCharacteristicValueValveType](/documentation/homekit/hmcharacteristicvaluevalvetype)

###### Valve Types

- [case genericValve](/documentation/homekit/hmcharacteristicvaluevalvetype/genericvalve)
- [case irrigation](/documentation/homekit/hmcharacteristicvaluevalvetype/irrigation)
- [case showerHead](/documentation/homekit/hmcharacteristicvaluevalvetype/showerhead)
- [case waterFaucet](/documentation/homekit/hmcharacteristicvaluevalvetype/waterfaucet)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevalvetype/init(rawvalue:))
- [let HMCharacteristicTypeLeakDetected: String](/documentation/homekit/hmcharacteristictypeleakdetected)

##### Values

- [HMCharacteristicValueLeakStatus](/documentation/homekit/hmcharacteristicvalueleakstatus)

###### Leak Status

- [case none](/documentation/homekit/hmcharacteristicvalueleakstatus/none)
- [case detected](/documentation/homekit/hmcharacteristicvalueleakstatus/detected)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueleakstatus/init(rawvalue:))

#### Doors and windows

- [let HMCharacteristicTypeCurrentDoorState: String](/documentation/homekit/hmcharacteristictypecurrentdoorstate)

##### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetDoorState: String](/documentation/homekit/hmcharacteristictypetargetdoorstate)

##### Values

- [HMCharacteristicValueDoorState](/documentation/homekit/hmcharacteristicvaluedoorstate)

###### Door States

- [case open](/documentation/homekit/hmcharacteristicvaluedoorstate/open)
- [case closed](/documentation/homekit/hmcharacteristicvaluedoorstate/closed)
- [case opening](/documentation/homekit/hmcharacteristicvaluedoorstate/opening)
- [case closing](/documentation/homekit/hmcharacteristicvaluedoorstate/closing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluedoorstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluedoorstate/init(rawvalue:))
- [HMCharacteristicValueTargetDoorState](/documentation/homekit/hmcharacteristicvaluetargetdoorstate)

###### Door States

- [case closed](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/closed)
- [case open](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/open)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetdoorstate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentPosition: String](/documentation/homekit/hmcharacteristictypecurrentposition)
- [let HMCharacteristicTypeTargetPosition: String](/documentation/homekit/hmcharacteristictypetargetposition)
- [let HMCharacteristicTypePositionState: String](/documentation/homekit/hmcharacteristictypepositionstate)

##### Values

- [HMCharacteristicValuePositionState](/documentation/homekit/hmcharacteristicvaluepositionstate)

###### Position States

- [case closing](/documentation/homekit/hmcharacteristicvaluepositionstate/closing)
- [case opening](/documentation/homekit/hmcharacteristicvaluepositionstate/opening)
- [case stopped](/documentation/homekit/hmcharacteristicvaluepositionstate/stopped)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepositionstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusJammed: String](/documentation/homekit/hmcharacteristictypestatusjammed)

##### Values

- [HMCharacteristicValueJammedStatus](/documentation/homekit/hmcharacteristicvaluejammedstatus)

###### Jammed Status

- [case none](/documentation/homekit/hmcharacteristicvaluejammedstatus/none)
- [case jammed](/documentation/homekit/hmcharacteristicvaluejammedstatus/jammed)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluejammedstatus/init(rawvalue:))
- [let HMCharacteristicTypeHoldPosition: String](/documentation/homekit/hmcharacteristictypeholdposition)
- [let HMCharacteristicTypeSlatType: String](/documentation/homekit/hmcharacteristictypeslattype)

##### Values

- [HMCharacteristicValueSlatType](/documentation/homekit/hmcharacteristicvalueslattype)

###### Slat Types

- [case horizontal](/documentation/homekit/hmcharacteristicvalueslattype/horizontal)
- [case vertical](/documentation/homekit/hmcharacteristicvalueslattype/vertical)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueslattype/init(rawvalue:))
- [let HMCharacteristicTypeCurrentSlatState: String](/documentation/homekit/hmcharacteristictypecurrentslatstate)

##### Values

- [HMCharacteristicValueCurrentSlatState](/documentation/homekit/hmcharacteristicvaluecurrentslatstate)

###### Slat States

- [case stationary](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/stationary)
- [case jammed](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/jammed)
- [case oscillating](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/oscillating)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentslatstate/init(rawvalue:))

#### Tilting mechanisms

- [let HMCharacteristicTypeCurrentHorizontalTilt: String](/documentation/homekit/hmcharacteristictypecurrenthorizontaltilt)
- [let HMCharacteristicTypeTargetHorizontalTilt: String](/documentation/homekit/hmcharacteristictypetargethorizontaltilt)
- [let HMCharacteristicTypeCurrentVerticalTilt: String](/documentation/homekit/hmcharacteristictypecurrentverticaltilt)
- [let HMCharacteristicTypeTargetVerticalTilt: String](/documentation/homekit/hmcharacteristictypetargetverticaltilt)
- [let HMCharacteristicTypeCurrentTilt: String](/documentation/homekit/hmcharacteristictypecurrenttilt)
- [let HMCharacteristicTypeTargetTilt: String](/documentation/homekit/hmcharacteristictypetargettilt)

#### Locks and openers

- [let HMCharacteristicTypeLockManagementAutoSecureTimeout: String](/documentation/homekit/hmcharacteristictypelockmanagementautosecuretimeout)
- [let HMCharacteristicTypeLockManagementControlPoint: String](/documentation/homekit/hmcharacteristictypelockmanagementcontrolpoint)
- [let HMCharacteristicTypeLockMechanismLastKnownAction: String](/documentation/homekit/hmcharacteristictypelockmechanismlastknownaction)

##### Values

- [HMCharacteristicValueLockMechanismLastKnownAction](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction)

###### Lock Mechanism Actions

- [case securedRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedremotely)
- [case securedUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovement)
- [case securedUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementexterior)
- [case securedUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedusingphysicalmovementinterior)
- [case securedWithAutomaticSecureTimeout](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithautomaticsecuretimeout)
- [case securedWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/securedwithkeypad)
- [case unsecuredRemotely](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredremotely)
- [case unsecuredUsingPhysicalMovement](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovement)
- [case unsecuredUsingPhysicalMovementExterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementexterior)
- [case unsecuredUsingPhysicalMovementInterior](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredusingphysicalmovementinterior)
- [case unsecuredWithKeypad](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/unsecuredwithkeypad)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismlastknownaction/init(rawvalue:))
- [let HMCharacteristicTypeLockPhysicalControls: String](/documentation/homekit/hmcharacteristictypelockphysicalcontrols)

##### Values

- [HMCharacteristicValueLockPhysicalControlsState](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate)

###### Lock Physical Control State

- [case notLocked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/notlocked)
- [case locked](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/locked)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockphysicalcontrolsstate/init(rawvalue:))
- [let HMCharacteristicTypeMotionDetected: String](/documentation/homekit/hmcharacteristictypemotiondetected)
- [let HMCharacteristicTypeCurrentLockMechanismState: String](/documentation/homekit/hmcharacteristictypecurrentlockmechanismstate)

##### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetLockMechanismState: String](/documentation/homekit/hmcharacteristictypetargetlockmechanismstate)

##### Values

- [HMCharacteristicValueLockMechanismState](/documentation/homekit/hmcharacteristicvaluelockmechanismstate)

###### Lock Mechanism State

- [case unsecured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unsecured)
- [case secured](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/secured)
- [case jammed](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/jammed)
- [case unknown](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelockmechanismstate/init(rawvalue:))
- [HMCharacteristicValueTargetLockMechanismState](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate)

###### Lock Mechanism States

- [case secured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/secured)
- [case unsecured](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/unsecured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetlockmechanismstate/init(rawvalue:))
- [let HMCharacteristicTypeRemoteKey: String](/documentation/homekit/hmcharacteristictyperemotekey)

##### Values

- [HMCharacteristicValueRemoteKey](/documentation/homekit/hmcharacteristicvalueremotekey)

###### Remote states

- [case arrowDown](/documentation/homekit/hmcharacteristicvalueremotekey/arrowdown)
- [case arrowLeft](/documentation/homekit/hmcharacteristicvalueremotekey/arrowleft)
- [case arrowRight](/documentation/homekit/hmcharacteristicvalueremotekey/arrowright)
- [case arrowUp](/documentation/homekit/hmcharacteristicvalueremotekey/arrowup)
- [case back](/documentation/homekit/hmcharacteristicvalueremotekey/back)
- [case exit](/documentation/homekit/hmcharacteristicvalueremotekey/exit)
- [case fastForward](/documentation/homekit/hmcharacteristicvalueremotekey/fastforward)
- [case home](/documentation/homekit/hmcharacteristicvalueremotekey/home)
- [case info](/documentation/homekit/hmcharacteristicvalueremotekey/info)
- [case menu](/documentation/homekit/hmcharacteristicvalueremotekey/menu)
- [case nextTrack](/documentation/homekit/hmcharacteristicvalueremotekey/nexttrack)
- [case pause](/documentation/homekit/hmcharacteristicvalueremotekey/pause)
- [case play](/documentation/homekit/hmcharacteristicvalueremotekey/play)
- [case playPause](/documentation/homekit/hmcharacteristicvalueremotekey/playpause)
- [case previousTrack](/documentation/homekit/hmcharacteristicvalueremotekey/previoustrack)
- [case rewind](/documentation/homekit/hmcharacteristicvalueremotekey/rewind)
- [case select](/documentation/homekit/hmcharacteristicvalueremotekey/select)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueremotekey/init(rawvalue:))

#### Safety and security

- [let HMCharacteristicTypeCurrentSecuritySystemState: String](/documentation/homekit/hmcharacteristictypecurrentsecuritysystemstate)

##### Values

- [HMCharacteristicValueCurrentSecuritySystemState](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/nightarm)
- [case disarmed](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/disarmed)
- [case triggered](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/triggered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeTargetSecuritySystemState: String](/documentation/homekit/hmcharacteristictypetargetsecuritysystemstate)

##### Values

- [HMCharacteristicValueTargetSecuritySystemState](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate)

###### Security System States

- [case stayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/stayarm)
- [case awayArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/awayarm)
- [case nightArm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/nightarm)
- [case disarm](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/disarm)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetsecuritysystemstate/init(rawvalue:))
- [let HMCharacteristicTypeObstructionDetected: String](/documentation/homekit/hmcharacteristictypeobstructiondetected)
- [let HMCharacteristicTypeOccupancyDetected: String](/documentation/homekit/hmcharacteristictypeoccupancydetected)

##### Values

- [HMCharacteristicValueOccupancyStatus](/documentation/homekit/hmcharacteristicvalueoccupancystatus)

###### Occupancy Status

- [case notOccupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/notoccupied)
- [case occupied](/documentation/homekit/hmcharacteristicvalueoccupancystatus/occupied)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueoccupancystatus/init(rawvalue:))
- [let HMCharacteristicTypeSecuritySystemAlarmType: String](/documentation/homekit/hmcharacteristictypesecuritysystemalarmtype)

##### Values

- [HMCharacteristicValueSecuritySystemAlarmType](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype)

###### Alarm Types

- [case noAlarm](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/noalarm)
- [case unknown](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluesecuritysystemalarmtype/init(rawvalue:))
- [let HMCharacteristicPropertyRequiresAuthorizationData: String](/documentation/homekit/hmcharacteristicpropertyrequiresauthorizationdata)

#### Audio and video

- [let HMCharacteristicTypeSupportedRTPConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedrtpconfiguration)
- [let HMCharacteristicTypeDigitalZoom: String](/documentation/homekit/hmcharacteristictypedigitalzoom)
- [let HMCharacteristicTypeOpticalZoom: String](/documentation/homekit/hmcharacteristictypeopticalzoom)
- [let HMCharacteristicTypeImageMirroring: String](/documentation/homekit/hmcharacteristictypeimagemirroring)
- [let HMCharacteristicTypeImageRotation: String](/documentation/homekit/hmcharacteristictypeimagerotation)
- [let HMCharacteristicTypeNightVision: String](/documentation/homekit/hmcharacteristictypenightvision)
- [let HMCharacteristicTypeStreamingStatus: String](/documentation/homekit/hmcharacteristictypestreamingstatus)
- [let HMCharacteristicTypeSupportedVideoStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedvideostreamconfiguration)
- [let HMCharacteristicTypeSupportedAudioStreamConfiguration: String](/documentation/homekit/hmcharacteristictypesupportedaudiostreamconfiguration)
- [let HMCharacteristicTypeSelectedStreamConfiguration: String](/documentation/homekit/hmcharacteristictypeselectedstreamconfiguration)
- [let HMCharacteristicTypeSetupStreamEndpoint: String](/documentation/homekit/hmcharacteristictypesetupstreamendpoint)
- [let HMCharacteristicTypeAudioFeedback: String](/documentation/homekit/hmcharacteristictypeaudiofeedback)
- [let HMCharacteristicTypeVolume: String](/documentation/homekit/hmcharacteristictypevolume)
- [let HMCharacteristicTypeMute: String](/documentation/homekit/hmcharacteristictypemute)
- [let HMCharacteristicTypeVolumeSelector: String](/documentation/homekit/hmcharacteristictypevolumeselector)

##### Values

- [HMCharacteristicValueVolumeSelector](/documentation/homekit/hmcharacteristicvaluevolumeselector)

###### Volume cases

- [case volumeDecrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumedecrement)
- [case volumeIncrement](/documentation/homekit/hmcharacteristicvaluevolumeselector/volumeincrement)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumeselector/init(rawvalue:))
- [let HMCharacteristicTypeVolumeControlType: String](/documentation/homekit/hmcharacteristictypevolumecontroltype)

##### Values

- [HMCharacteristicValueVolumeControlType](/documentation/homekit/hmcharacteristicvaluevolumecontroltype)

###### Volume types

- [case absolute](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/absolute)
- [case none](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/none)
- [case relative](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relative)
- [case relativeWithCurrent](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/relativewithcurrent)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluevolumecontroltype/init(rawvalue:))
- [let HMCharacteristicTypeClosedCaptions: String](/documentation/homekit/hmcharacteristictypeclosedcaptions)

##### Values

- [HMCharacteristicValueClosedCaptions](/documentation/homekit/hmcharacteristicvalueclosedcaptions)

###### Closed caption states

- [case disabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/disabled)
- [case enabled](/documentation/homekit/hmcharacteristicvalueclosedcaptions/enabled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueclosedcaptions/init(rawvalue:))
- [let HMCharacteristicTypePictureMode: String](/documentation/homekit/hmcharacteristictypepicturemode)

##### Values

- [HMCharacteristicValuePictureMode](/documentation/homekit/hmcharacteristicvaluepicturemode)

###### Television states

- [case bright](/documentation/homekit/hmcharacteristicvaluepicturemode/bright)
- [case calibrated](/documentation/homekit/hmcharacteristicvaluepicturemode/calibrated)
- [case computer](/documentation/homekit/hmcharacteristicvaluepicturemode/computer)
- [case custom1](/documentation/homekit/hmcharacteristicvaluepicturemode/custom1)
- [case custom2](/documentation/homekit/hmcharacteristicvaluepicturemode/custom2)
- [case custom3](/documentation/homekit/hmcharacteristicvaluepicturemode/custom3)
- [case dark](/documentation/homekit/hmcharacteristicvaluepicturemode/dark)
- [case game](/documentation/homekit/hmcharacteristicvaluepicturemode/game)
- [case movie](/documentation/homekit/hmcharacteristicvaluepicturemode/movie)
- [case night](/documentation/homekit/hmcharacteristicvaluepicturemode/night)
- [case photo](/documentation/homekit/hmcharacteristicvaluepicturemode/photo)
- [case sport](/documentation/homekit/hmcharacteristicvaluepicturemode/sport)
- [case standard](/documentation/homekit/hmcharacteristicvaluepicturemode/standard)
- [case vivid](/documentation/homekit/hmcharacteristicvaluepicturemode/vivid)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluepicturemode/init(rawvalue:))

#### General state

- [let HMCharacteristicTypeActive: String](/documentation/homekit/hmcharacteristictypeactive)

##### Values

- [HMCharacteristicValueActivationState](/documentation/homekit/hmcharacteristicvalueactivationstate)

###### Activation States

- [case inactive](/documentation/homekit/hmcharacteristicvalueactivationstate/inactive)
- [case active](/documentation/homekit/hmcharacteristicvalueactivationstate/active)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueactivationstate/init(rawvalue:))
- [let HMCharacteristicTypeStatusTampered: String](/documentation/homekit/hmcharacteristictypestatustampered)

##### Values

- [HMCharacteristicValueTamperedStatus](/documentation/homekit/hmcharacteristicvaluetamperedstatus)

###### Tampered Status

- [case none](/documentation/homekit/hmcharacteristicvaluetamperedstatus/none)
- [case tampered](/documentation/homekit/hmcharacteristicvaluetamperedstatus/tampered)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetamperedstatus/init(rawvalue:))
- [let HMCharacteristicTypeStatusFault: String](/documentation/homekit/hmcharacteristictypestatusfault)

##### Values

- [HMCharacteristicValueStatusFault](/documentation/homekit/hmcharacteristicvaluestatusfault)

###### Fault Status

- [case noFault](/documentation/homekit/hmcharacteristicvaluestatusfault/nofault)
- [case generalFault](/documentation/homekit/hmcharacteristicvaluestatusfault/generalfault)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluestatusfault/init(rawvalue:))
- [let HMCharacteristicTypeStatusActive: String](/documentation/homekit/hmcharacteristictypestatusactive)
- [let HMCharacteristicTypeInUse: String](/documentation/homekit/hmcharacteristictypeinuse)

##### Values

- [HMCharacteristicValueUsageState](/documentation/homekit/hmcharacteristicvalueusagestate)

###### Usage States

- [case notInUse](/documentation/homekit/hmcharacteristicvalueusagestate/notinuse)
- [case inUse](/documentation/homekit/hmcharacteristicvalueusagestate/inuse)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueusagestate/init(rawvalue:))
- [let HMCharacteristicTypeIsConfigured: String](/documentation/homekit/hmcharacteristictypeisconfigured)

##### Values

- [HMCharacteristicValueConfigurationState](/documentation/homekit/hmcharacteristicvalueconfigurationstate)

###### Configuration States

- [case notConfigured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/notconfigured)
- [case configured](/documentation/homekit/hmcharacteristicvalueconfigurationstate/configured)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueconfigurationstate/init(rawvalue:))
- [let HMCharacteristicTypeRemainingDuration: String](/documentation/homekit/hmcharacteristictyperemainingduration)
- [let HMCharacteristicTypeSetDuration: String](/documentation/homekit/hmcharacteristictypesetduration)
- [let HMCharacteristicTypeProgramMode: String](/documentation/homekit/hmcharacteristictypeprogrammode)

##### Values

- [HMCharacteristicValueProgramMode](/documentation/homekit/hmcharacteristicvalueprogrammode)

###### Constants

- [case notScheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/notscheduled)
- [case scheduleOverriddenToManual](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduleoverriddentomanual)
- [case scheduled](/documentation/homekit/hmcharacteristicvalueprogrammode/scheduled)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueprogrammode/init(rawvalue:))
- [let HMCharacteristicTypeWiFiSatelliteStatus: String](/documentation/homekit/hmcharacteristictypewifisatellitestatus)

##### Values

- [HMCharacteristicValueWiFiSatelliteStatus](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus)

###### Network states

- [case connected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/connected)
- [case notConnected](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/notconnected)
- [case unknown](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluewifisatellitestatus/init(rawvalue:))
- [let HMCharacteristicTypeWANStatusList: String](/documentation/homekit/hmcharacteristictypewanstatuslist)
- [let HMCharacteristicTypeTargetMediaState: String](/documentation/homekit/hmcharacteristictypetargetmediastate)

##### Values

- [HMCharacteristicValueTargetMediaState](/documentation/homekit/hmcharacteristicvaluetargetmediastate)

###### Media states

- [case pause](/documentation/homekit/hmcharacteristicvaluetargetmediastate/pause)
- [case play](/documentation/homekit/hmcharacteristicvaluetargetmediastate/play)
- [case stop](/documentation/homekit/hmcharacteristicvaluetargetmediastate/stop)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetmediastate/init(rawvalue:))
- [let HMCharacteristicTypeRouterStatus: String](/documentation/homekit/hmcharacteristictyperouterstatus)

##### Values

- [HMCharacteristicValueRouterStatus](/documentation/homekit/hmcharacteristicvaluerouterstatus)

###### Router states

- [case notReady](/documentation/homekit/hmcharacteristicvaluerouterstatus/notready)
- [case ready](/documentation/homekit/hmcharacteristicvaluerouterstatus/ready)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluerouterstatus/init(rawvalue:))
- [let HMCharacteristicTypeCurrentMediaState: String](/documentation/homekit/hmcharacteristictypecurrentmediastate)

##### Values

- [HMCharacteristicValueCurrentMediaState](/documentation/homekit/hmcharacteristicvaluecurrentmediastate)

###### Current media states

- [case interrupted](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/interrupted)
- [case loading](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/loading)
- [case paused](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/paused)
- [case playing](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/playing)
- [case stopped](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/stopped)
- [case unknown](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/unknown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentmediastate/init(rawvalue:))
- [let HMCharacteristicTypeCurrentVisibilityState: String](/documentation/homekit/hmcharacteristictypecurrentvisibilitystate)

##### Values

- [HMCharacteristicValueCurrentVisibilityState](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate)

###### Visibility states

- [case alwaysShown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/alwaysshown)
- [case connected](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/connected)
- [case hidden](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/hidden)
- [case shown](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/shown)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluecurrentvisibilitystate/init(rawvalue:))
- [let HMCharacteristicTypeTargetVisibilityState: String](/documentation/homekit/hmcharacteristictypetargetvisibilitystate)

##### Values

- [HMCharacteristicValueTargetVisibilityState](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate)

###### Visibility states

- [case hide](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/hide)
- [case show](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/show)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluetargetvisibilitystate/init(rawvalue:))
- [let HMCharacteristicPropertySupportsEventNotification: String](/documentation/homekit/hmcharacteristicpropertysupportseventnotification-2f0ml)

#### Accessory identification

- [let HMCharacteristicTypeName: String](/documentation/homekit/hmcharacteristictypename)
- [let HMCharacteristicTypeIdentify: String](/documentation/homekit/hmcharacteristictypeidentify)
- [let HMCharacteristicTypeVersion: String](/documentation/homekit/hmcharacteristictypeversion)
- [let HMCharacteristicTypeLogs: String](/documentation/homekit/hmcharacteristictypelogs)
- [let HMCharacteristicTypeAdminOnlyAccess: String](/documentation/homekit/hmcharacteristictypeadminonlyaccess)
- [let HMCharacteristicTypeHardwareVersion: String](/documentation/homekit/hmcharacteristictypehardwareversion)
- [let HMCharacteristicTypeSoftwareVersion: String](/documentation/homekit/hmcharacteristictypesoftwareversion)
- [let HMCharacteristicTypeLabelIndex: String](/documentation/homekit/hmcharacteristictypelabelindex)
- [let HMCharacteristicTypeLabelNamespace: String](/documentation/homekit/hmcharacteristictypelabelnamespace)

##### Values

- [HMCharacteristicValueLabelNamespace](/documentation/homekit/hmcharacteristicvaluelabelnamespace)

###### Namespaces

- [case dot](/documentation/homekit/hmcharacteristicvaluelabelnamespace/dot)
- [case numeral](/documentation/homekit/hmcharacteristicvaluelabelnamespace/numeral)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvaluelabelnamespace/init(rawvalue:))
- [let HMCharacteristicTypeActiveIdentifier: String](/documentation/homekit/hmcharacteristictypeactiveidentifier)
- [let HMCharacteristicTypeIdentifier: String](/documentation/homekit/hmcharacteristictypeidentifier)
- [let HMCharacteristicTypeInputDeviceType: String](/documentation/homekit/hmcharacteristictypeinputdevicetype)

##### Values

- [HMCharacteristicValueInputDeviceType](/documentation/homekit/hmcharacteristicvalueinputdevicetype)

###### Input devices

- [case audioSystem](/documentation/homekit/hmcharacteristicvalueinputdevicetype/audiosystem)
- [case none](/documentation/homekit/hmcharacteristicvalueinputdevicetype/none)
- [case other](/documentation/homekit/hmcharacteristicvalueinputdevicetype/other)
- [case playback](/documentation/homekit/hmcharacteristicvalueinputdevicetype/playback)
- [case recording](/documentation/homekit/hmcharacteristicvalueinputdevicetype/recording)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tuner)
- [case tv](/documentation/homekit/hmcharacteristicvalueinputdevicetype/tv)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputdevicetype/init(rawvalue:))
- [let HMCharacteristicTypeInputSourceType: String](/documentation/homekit/hmcharacteristictypeinputsourcetype)

##### Values

- [HMCharacteristicValueInputSourceType](/documentation/homekit/hmcharacteristicvalueinputsourcetype)

###### Accessory source types

- [case airPlay](/documentation/homekit/hmcharacteristicvalueinputsourcetype/airplay)
- [case application](/documentation/homekit/hmcharacteristicvalueinputsourcetype/application)
- [case componentVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/componentvideo)
- [case compositeVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/compositevideo)
- [case dvi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/dvi)
- [case hdmi](/documentation/homekit/hmcharacteristicvalueinputsourcetype/hdmi)
- [case homeScreen](/documentation/homekit/hmcharacteristicvalueinputsourcetype/homescreen)
- [case other](/documentation/homekit/hmcharacteristicvalueinputsourcetype/other)
- [case sVideo](/documentation/homekit/hmcharacteristicvalueinputsourcetype/svideo)
- [case tuner](/documentation/homekit/hmcharacteristicvalueinputsourcetype/tuner)
- [case usb](/documentation/homekit/hmcharacteristicvalueinputsourcetype/usb)

###### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmcharacteristicvalueinputsourcetype/init(rawvalue:))
- [let HMCharacteristicTypeConfiguredName: String](/documentation/homekit/hmcharacteristictypeconfiguredname)

#### Deprecated characteristic types

- [let HMCharacteristicTypeManufacturer: String](/documentation/homekit/hmcharacteristictypemanufacturer)
- [let HMCharacteristicTypeModel: String](/documentation/homekit/hmcharacteristictypemodel)
- [let HMCharacteristicTypeFirmwareVersion: String](/documentation/homekit/hmcharacteristictypefirmwareversion)
- [let HMCharacteristicTypeSerialNumber: String](/documentation/homekit/hmcharacteristictypeserialnumber)

### Controlling a characteristic

- [var value: Any?](/documentation/homekit/hmcharacteristic/value)
- [func readValue(completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/readvalue(completionhandler:))
- [func writeValue(Any?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/writevalue(_:completionhandler:))
- [func updateAuthorizationData(Data?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/updateauthorizationdata(_:completionhandler:))

### Managing characteristic presentation

- [var metadata: HMCharacteristicMetadata?](/documentation/homekit/hmcharacteristic/metadata)
- [HMCharacteristicMetadata](/documentation/homekit/hmcharacteristicmetadata)

#### Describing a characteristic

- [var manufacturerDescription: String?](/documentation/homekit/hmcharacteristicmetadata/manufacturerdescription)

#### Bounding the value

- [var validValues: [NSNumber]?](/documentation/homekit/hmcharacteristicmetadata/validvalues)
- [var minimumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/minimumvalue)
- [var maximumValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maximumvalue)
- [var stepValue: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/stepvalue)
- [var maxLength: NSNumber?](/documentation/homekit/hmcharacteristicmetadata/maxlength)

#### Formatting the value

- [var format: String?](/documentation/homekit/hmcharacteristicmetadata/format)
- [Characteristic Data Formats](/documentation/homekit/characteristic-data-formats)

##### Booleans

- [let HMCharacteristicMetadataFormatBool: String](/documentation/homekit/hmcharacteristicmetadataformatbool)

##### Strings

- [let HMCharacteristicMetadataFormatString: String](/documentation/homekit/hmcharacteristicmetadataformatstring)

##### Signed Values

- [let HMCharacteristicMetadataFormatInt: String](/documentation/homekit/hmcharacteristicmetadataformatint)
- [let HMCharacteristicMetadataFormatFloat: String](/documentation/homekit/hmcharacteristicmetadataformatfloat)

##### Unsigned Integers

- [let HMCharacteristicMetadataFormatUInt8: String](/documentation/homekit/hmcharacteristicmetadataformatuint8)
- [let HMCharacteristicMetadataFormatUInt16: String](/documentation/homekit/hmcharacteristicmetadataformatuint16)
- [let HMCharacteristicMetadataFormatUInt32: String](/documentation/homekit/hmcharacteristicmetadataformatuint32)
- [let HMCharacteristicMetadataFormatUInt64: String](/documentation/homekit/hmcharacteristicmetadataformatuint64)

##### Data

- [let HMCharacteristicMetadataFormatData: String](/documentation/homekit/hmcharacteristicmetadataformatdata)
- [let HMCharacteristicMetadataFormatTLV8: String](/documentation/homekit/hmcharacteristicmetadataformattlv8)

##### Collections

- [let HMCharacteristicMetadataFormatArray: String](/documentation/homekit/hmcharacteristicmetadataformatarray)
- [let HMCharacteristicMetadataFormatDictionary: String](/documentation/homekit/hmcharacteristicmetadataformatdictionary)

#### Specifying units

- [var units: String?](/documentation/homekit/hmcharacteristicmetadata/units)
- [Characteristic Units](/documentation/homekit/characteristic-units)

##### Parts Per Total

- [let HMCharacteristicMetadataUnitsPercentage: String](/documentation/homekit/hmcharacteristicmetadataunitspercentage)
- [let HMCharacteristicMetadataUnitsPartsPerMillion: String](/documentation/homekit/hmcharacteristicmetadataunitspartspermillion)

##### Temperature

- [let HMCharacteristicMetadataUnitsCelsius: String](/documentation/homekit/hmcharacteristicmetadataunitscelsius)
- [let HMCharacteristicMetadataUnitsFahrenheit: String](/documentation/homekit/hmcharacteristicmetadataunitsfahrenheit)

##### Time

- [let HMCharacteristicMetadataUnitsSeconds: String](/documentation/homekit/hmcharacteristicmetadataunitsseconds)

##### Light

- [let HMCharacteristicMetadataUnitsLux: String](/documentation/homekit/hmcharacteristicmetadataunitslux)

##### Mass

- [let HMCharacteristicMetadataUnitsMicrogramsPerCubicMeter: String](/documentation/homekit/hmcharacteristicmetadataunitsmicrogramspercubicmeter)

##### Rotation

- [let HMCharacteristicMetadataUnitsArcDegree: String](/documentation/homekit/hmcharacteristicmetadataunitsarcdegree)

#### Initializers

- [init()](/documentation/homekit/hmcharacteristicmetadata/init())

### Receiving change notifications

- [func enableNotification(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristic/enablenotification(_:completionhandler:))
- [var isNotificationEnabled: Bool](/documentation/homekit/hmcharacteristic/isnotificationenabled)

### Getting the characterized service

- [var service: HMService?](/documentation/homekit/hmcharacteristic/service)

### Initializers

- [init()](/documentation/homekit/hmcharacteristic/init())
- [HMMediaSourceDisplayOrderProfile](/documentation/homekit/hmmediasourcedisplayorderprofile)

### Managing input source order

- [func writeOrder([Int]) async throws](/documentation/homekit/hmmediasourcedisplayorderprofile/writeorder(_:))
- [var delegate: (any HMMediaSourceDisplayOrderProfile.Delegate)?](/documentation/homekit/hmmediasourcedisplayorderprofile/delegate-swift.property)
- [var order: [Int]](/documentation/homekit/hmmediasourcedisplayorderprofile/order)
- [let canModifyOrder: Bool](/documentation/homekit/hmmediasourcedisplayorderprofile/canmodifyorder)
- [HMMediaSourceDisplayOrderProfile.Delegate](/documentation/homekit/hmmediasourcedisplayorderprofile/delegate-swift.protocol)

#### Instance Methods

- [func mediaSourceDisplayOrderProfileDidUpdateOrder(HMMediaSourceDisplayOrderProfile)](/documentation/homekit/hmmediasourcedisplayorderprofile/delegate-swift.protocol/mediasourcedisplayorderprofiledidupdateorder(_:))

## Action Sets

- [HMActionSet](/documentation/homekit/hmactionset)

### Identifiying an action set

- [var uniqueIdentifier: UUID](/documentation/homekit/hmactionset/uniqueidentifier)
- [var name: String](/documentation/homekit/hmactionset/name)
- [func updateName(String, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/updatename(_:completionhandler:))

### Specifying a type

- [var actionSetType: String](/documentation/homekit/hmactionset/actionsettype)
- [Action Set Types](/documentation/homekit/action-set-types)

#### Built-in Types

- [let HMActionSetTypeHomeArrival: String](/documentation/homekit/hmactionsettypehomearrival)
- [let HMActionSetTypeHomeDeparture: String](/documentation/homekit/hmactionsettypehomedeparture)
- [let HMActionSetTypeSleep: String](/documentation/homekit/hmactionsettypesleep)
- [let HMActionSetTypeWakeUp: String](/documentation/homekit/hmactionsettypewakeup)

#### User Defined Types

- [let HMActionSetTypeUserDefined: String](/documentation/homekit/hmactionsettypeuserdefined)

#### Trigger Owned Types

- [let HMActionSetTypeTriggerOwned: String](/documentation/homekit/hmactionsettypetriggerowned)

### Defining the associated actions

- [var actions: Set<HMAction>](/documentation/homekit/hmactionset/actions)
- [func addAction(HMAction, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/addaction(_:completionhandler:))
- [func removeAction(HMAction, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmactionset/removeaction(_:completionhandler:))
- [HMCharacteristicWriteAction](/documentation/homekit/hmcharacteristicwriteaction)

#### New Methods

- [init(characteristic: HMCharacteristic, targetValue: TargetValueType)](/documentation/homekit/hmcharacteristicwriteaction/init(characteristic:targetvalue:))
- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicwriteaction/characteristic)
- [var targetValue: TargetValueType](/documentation/homekit/hmcharacteristicwriteaction/targetvalue)
- [func updateTargetValue(TargetValueType, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristicwriteaction/updatetargetvalue(_:completionhandler:))
- [HMAction](/documentation/homekit/hmaction)

#### Identifying an action

- [var uniqueIdentifier: UUID](/documentation/homekit/hmaction/uniqueidentifier)

#### Initializers

- [init()](/documentation/homekit/hmaction/init())

#### Type Methods

- [class func new() -> Self](/documentation/homekit/hmaction/new())

### Keeping track of execution

- [var isExecuting: Bool](/documentation/homekit/hmactionset/isexecuting)
- [var lastExecutionDate: Date?](/documentation/homekit/hmactionset/lastexecutiondate)
- [HMTimerTrigger](/documentation/homekit/hmtimertrigger)

### Creating a timer trigger

- [init(name: String, fireDate: Date, recurrence: DateComponents?)](/documentation/homekit/hmtimertrigger/init(name:firedate:recurrence:))

### Choosing the fire date

- [var fireDate: Date](/documentation/homekit/hmtimertrigger/firedate)
- [func updateFireDate(Date, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updatefiredate(_:completionhandler:))

### Using recurrence

- [var recurrence: DateComponents?](/documentation/homekit/hmtimertrigger/recurrence)
- [func updateRecurrence(DateComponents?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updaterecurrence(_:completionhandler:))

### Deprecated symbols

- [init(name: String, fireDate: Date, timeZone: TimeZone?, recurrence: DateComponents?, recurrenceCalendar: Calendar?)](/documentation/homekit/hmtimertrigger/init(name:firedate:timezone:recurrence:recurrencecalendar:))
- [var timeZone: TimeZone?](/documentation/homekit/hmtimertrigger/timezone)
- [func updateTimeZone(TimeZone?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmtimertrigger/updatetimezone(_:completionhandler:))
- [var recurrenceCalendar: Calendar?](/documentation/homekit/hmtimertrigger/recurrencecalendar)
- [HMEventTrigger](/documentation/homekit/hmeventtrigger)

### Creating an event trigger

- [init(name: String, events: [HMEvent], predicate: NSPredicate?)](/documentation/homekit/hmeventtrigger/init(name:events:predicate:))
- [init(name: String, events: [HMEvent], end: [HMEvent]?, recurrences: [DateComponents]?, predicate: NSPredicate?)](/documentation/homekit/hmeventtrigger/init(name:events:end:recurrences:predicate:))

### Querying trigger activation state

- [var triggerActivationState: HMEventTriggerActivationState](/documentation/homekit/hmeventtrigger/triggeractivationstate)
- [HMEventTriggerActivationState](/documentation/homekit/hmeventtriggeractivationstate)

#### Inspecting activation state

- [case disabled](/documentation/homekit/hmeventtriggeractivationstate/disabled)
- [case disabledNoCompatibleHomeHub](/documentation/homekit/hmeventtriggeractivationstate/disablednocompatiblehomehub)
- [case disabledNoHomeHub](/documentation/homekit/hmeventtriggeractivationstate/disablednohomehub)
- [case disabledNoLocationServicesAuthorization](/documentation/homekit/hmeventtriggeractivationstate/disablednolocationservicesauthorization)
- [case enabled](/documentation/homekit/hmeventtriggeractivationstate/enabled)

#### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmeventtriggeractivationstate/init(rawvalue:))

### Setting trigger events

- [var events: [HMEvent]](/documentation/homekit/hmeventtrigger/events)
- [func updateEvents([HMEvent], completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateevents(_:completionhandler:))
- [Location events](/documentation/homekit/location-events)

#### Locations

- [HMLocationEvent](/documentation/homekit/hmlocationevent)

##### Creating a Location Event

- [init(region: CLRegion)](/documentation/homekit/hmlocationevent/init(region:))

##### Inspecting the Region

- [var region: CLRegion?](/documentation/homekit/hmlocationevent/region)

##### Configuring the Region

- [func updateRegion(CLRegion, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmlocationevent/updateregion(_:completionhandler:))
- [HMMutableLocationEvent](/documentation/homekit/hmmutablelocationevent)

##### Controlling the Region

- [var region: CLRegion?](/documentation/homekit/hmmutablelocationevent/region)
- [Time events](/documentation/homekit/time-events)

#### Dates and times

- [HMCalendarEvent](/documentation/homekit/hmcalendarevent)

##### Creating a calendar event

- [init(fire: DateComponents)](/documentation/homekit/hmcalendarevent/init(fire:))

##### Inspecting the calendar event

- [var fireDateComponents: DateComponents](/documentation/homekit/hmcalendarevent/firedatecomponents)
- [HMMutableCalendarEvent](/documentation/homekit/hmmutablecalendarevent)

##### Configuring the calendar event

- [var fireDateComponents: DateComponents](/documentation/homekit/hmmutablecalendarevent/firedatecomponents)
- [HMTimeEvent](/documentation/homekit/hmtimeevent)

#### Significant events

- [HMSignificantEvent](/documentation/homekit/hmsignificantevent)

##### Significant event properties

- [static let sunrise: HMSignificantEvent](/documentation/homekit/hmsignificantevent/sunrise)
- [static let sunset: HMSignificantEvent](/documentation/homekit/hmsignificantevent/sunset)

##### Creating a significant event

- [init(String)](/documentation/homekit/hmsignificantevent/init(_:))
- [init(rawValue: String)](/documentation/homekit/hmsignificantevent/init(rawvalue:))
- [HMSignificantTimeEvent](/documentation/homekit/hmsignificanttimeevent)

##### Creating a significant time event

- [init(significantEvent: HMSignificantEvent, offset: DateComponents?)](/documentation/homekit/hmsignificanttimeevent/init(significantevent:offset:))

##### Inspecting a significant time event

- [var significantEvent: HMSignificantEvent](/documentation/homekit/hmsignificanttimeevent/significantevent)
- [var offset: DateComponents?](/documentation/homekit/hmsignificanttimeevent/offset)
- [HMMutableSignificantTimeEvent](/documentation/homekit/hmmutablesignificanttimeevent)

##### Configuring a significant time event

- [var significantEvent: HMSignificantEvent](/documentation/homekit/hmmutablesignificanttimeevent/significantevent)
- [var offset: DateComponents](/documentation/homekit/hmmutablesignificanttimeevent/offset)

#### Durations

- [HMDurationEvent](/documentation/homekit/hmdurationevent)

##### Creating a duration event

- [init(duration: TimeInterval)](/documentation/homekit/hmdurationevent/init(duration:))

##### Inspecting a duration event

- [var duration: TimeInterval](/documentation/homekit/hmdurationevent/duration)
- [HMMutableDurationEvent](/documentation/homekit/hmmutabledurationevent)

##### Configuring a duration event

- [var duration: TimeInterval](/documentation/homekit/hmmutabledurationevent/duration)
- [Characteristic events](/documentation/homekit/characteristic-events)

#### Characteristics

- [HMCharacteristicEvent](/documentation/homekit/hmcharacteristicevent)

##### Creating a characteristic event

- [init(characteristic: HMCharacteristic, triggerValue: TriggerValueType?)](/documentation/homekit/hmcharacteristicevent/init(characteristic:triggervalue:))

##### Inspecting the event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicevent/characteristic)
- [var triggerValue: TriggerValueType?](/documentation/homekit/hmcharacteristicevent/triggervalue)

##### Configuring the event

- [func updateTriggerValue(TriggerValueType?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmcharacteristicevent/updatetriggervalue(_:completionhandler:))
- [HMMutableCharacteristicEvent](/documentation/homekit/hmmutablecharacteristicevent)

##### Configuring the event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmmutablecharacteristicevent/characteristic)
- [var triggerValue: TriggerValueType?](/documentation/homekit/hmmutablecharacteristicevent/triggervalue)

#### Characteristic ranges

- [HMNumberRange](/documentation/homekit/hmnumberrange)

##### Creating a number range

- [convenience init(minValue: NSNumber, maxValue: NSNumber)](/documentation/homekit/hmnumberrange/init(minvalue:maxvalue:))
- [convenience init(minValue: NSNumber)](/documentation/homekit/hmnumberrange/init(minvalue:))
- [convenience init(maxValue: NSNumber)](/documentation/homekit/hmnumberrange/init(maxvalue:))

##### Inspecting a number range

- [var minValue: NSNumber?](/documentation/homekit/hmnumberrange/minvalue)
- [var maxValue: NSNumber?](/documentation/homekit/hmnumberrange/maxvalue)
- [HMCharacteristicThresholdRangeEvent](/documentation/homekit/hmcharacteristicthresholdrangeevent)

##### Creating a characteristic threshold range event

- [init(characteristic: HMCharacteristic, thresholdRange: HMNumberRange)](/documentation/homekit/hmcharacteristicthresholdrangeevent/init(characteristic:thresholdrange:))

##### Inspecting a characteristic threshold event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmcharacteristicthresholdrangeevent/characteristic)
- [var thresholdRange: HMNumberRange](/documentation/homekit/hmcharacteristicthresholdrangeevent/thresholdrange)
- [HMMutableCharacteristicThresholdRangeEvent](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent)

##### Configuring a characteristic threshold event

- [var characteristic: HMCharacteristic](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent/characteristic)
- [var thresholdRange: HMNumberRange](/documentation/homekit/hmmutablecharacteristicthresholdrangeevent/thresholdrange)
- [Presence events](/documentation/homekit/presence-events)

#### User presence

- [HMPresenceEvent](/documentation/homekit/hmpresenceevent)

##### Creating a presence event

- [init(presenceEventType: HMPresenceEventType, presenceUserType: HMPresenceEventUserType)](/documentation/homekit/hmpresenceevent/init(presenceeventtype:presenceusertype:))

##### Inspecting a presence event

- [var presenceEventType: HMPresenceEventType](/documentation/homekit/hmpresenceevent/presenceeventtype)
- [var presenceUserType: HMPresenceEventUserType](/documentation/homekit/hmpresenceevent/presenceusertype)
- [HMMutablePresenceEvent](/documentation/homekit/hmmutablepresenceevent)

##### Configuring a presence event

- [var presenceEventType: HMPresenceEventType](/documentation/homekit/hmmutablepresenceevent/presenceeventtype)
- [var presenceUserType: HMPresenceEventUserType](/documentation/homekit/hmmutablepresenceevent/presenceusertype)
- [HMPresenceEventType](/documentation/homekit/hmpresenceeventtype)

##### Specifying presence type

- [case everyEntry](/documentation/homekit/hmpresenceeventtype/everyentry)
- [case everyExit](/documentation/homekit/hmpresenceeventtype/everyexit)
- [case firstEntry](/documentation/homekit/hmpresenceeventtype/firstentry)
- [case lastExit](/documentation/homekit/hmpresenceeventtype/lastexit)

##### Using presence as a predicate

- [static var atHome: HMPresenceEventType](/documentation/homekit/hmpresenceeventtype/athome)
- [static var notAtHome: HMPresenceEventType](/documentation/homekit/hmpresenceeventtype/notathome)

##### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmpresenceeventtype/init(rawvalue:))
- [HMPresenceEventUserType](/documentation/homekit/hmpresenceeventusertype)

##### Selecting users

- [case currentUser](/documentation/homekit/hmpresenceeventusertype/currentuser)
- [case homeUsers](/documentation/homekit/hmpresenceeventusertype/homeusers)
- [case customUsers](/documentation/homekit/hmpresenceeventusertype/customusers)

##### Initializers

- [init?(rawValue: UInt)](/documentation/homekit/hmpresenceeventusertype/init(rawvalue:))
- [HMEvent](/documentation/homekit/hmevent)

#### Getting information about the event

- [var uniqueIdentifier: UUID](/documentation/homekit/hmevent/uniqueidentifier)
- [class func isSupported(for: HMHome) -> Bool](/documentation/homekit/hmevent/issupported(for:))

#### Initializers

- [init()](/documentation/homekit/hmevent/init())

#### Type Methods

- [class func new() -> Self](/documentation/homekit/hmevent/new())

### Restoring the previous scene after an event

- [var endEvents: [HMEvent]](/documentation/homekit/hmeventtrigger/endevents)
- [func updateEndEvents([HMEvent], completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateendevents(_:completionhandler:))

### Controlling recurrence

- [var recurrences: [DateComponents]?](/documentation/homekit/hmeventtrigger/recurrences)
- [func updateRecurrences([DateComponents]?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updaterecurrences(_:completionhandler:))
- [var executeOnce: Bool](/documentation/homekit/hmeventtrigger/executeonce)
- [func updateExecuteOnce(Bool, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updateexecuteonce(_:completionhandler:))

### Adding a trigger condition

- [var predicate: NSPredicate?](/documentation/homekit/hmeventtrigger/predicate)
- [func updatePredicate(NSPredicate?, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/updatepredicate(_:completionhandler:))

### Creating predicates

- [class func predicateForEvaluatingTriggerOccurring(beforeSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurring(beforesignificantevent:))
- [class func predicateForEvaluatingTriggerOccurring(afterSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurring(aftersignificantevent:))
- [class func predicate(forEvaluatingTriggerOccurringBetweenSignificantEvent: HMSignificantTimeEvent, secondSignificantEvent: HMSignificantTimeEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicate(forevaluatingtriggeroccurringbetweensignificantevent:secondsignificantevent:))
- [class func predicateForEvaluatingTrigger(occurringBefore: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringbefore:))
- [class func predicateForEvaluatingTrigger(occurringOn: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringon:))
- [class func predicateForEvaluatingTrigger(occurringAfter: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringafter:))
- [class func predicateForEvaluatingTriggerOccurringBetweenDate(with: DateComponents, secondDateWith: DateComponents) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtriggeroccurringbetweendate(with:seconddatewith:))
- [class func predicateForEvaluatingTrigger(HMCharacteristic, relatedBy: NSComparisonPredicate.Operator, toValue: Any) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(_:relatedby:tovalue:))
- [class func predicateForEvaluatingTrigger(withPresence: HMPresenceEvent) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(withpresence:))
- [let HMCharacteristicKeyPath: String](/documentation/homekit/hmcharacteristickeypath)
- [let HMCharacteristicValueKeyPath: String](/documentation/homekit/hmcharacteristicvaluekeypath)
- [let HMPresenceKeyPath: String](/documentation/homekit/hmpresencekeypath)

### Deprecated symbols

- [func addEvent(HMEvent, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/addevent(_:completionhandler:))
- [func removeEvent(HMEvent, completionHandler: ((any Error)?) -> Void)](/documentation/homekit/hmeventtrigger/removeevent(_:completionhandler:))
- [class func predicateForEvaluatingTrigger(occurringBefore: String, applyingOffset: DateComponents?) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringbefore:applyingoffset:))
- [class func predicateForEvaluatingTrigger(occurringAfter: String, applyingOffset: DateComponents?) -> NSPredicate](/documentation/homekit/hmeventtrigger/predicateforevaluatingtrigger(occurringafter:applyingoffset:))

## Errors

- [HMError](/documentation/homekit/hmerror)

### Obtaining error information

- [let HMErrorDomain: String](/documentation/homekit/hmerrordomain)

### Detecting accessory errors

- [static var accessoryIsBlocked: HMError.Code](/documentation/homekit/hmerror/accessoryisblocked)
- [static var accessoryIsBusy: HMError.Code](/documentation/homekit/hmerror/accessoryisbusy)
- [static var accessoryIsSuspended: HMError.Code](/documentation/homekit/hmerror/accessoryissuspended)
- [static var accessoryNotReachable: HMError.Code](/documentation/homekit/hmerror/accessorynotreachable)
- [static var accessoryOutOfCompliance: HMError.Code](/documentation/homekit/hmerror/accessoryoutofcompliance)
- [static var accessoryOutOfResources: HMError.Code](/documentation/homekit/hmerror/accessoryoutofresources)
- [static var accessoryPoweredOff: HMError.Code](/documentation/homekit/hmerror/accessorypoweredoff)
- [static var accessoryResponseError: HMError.Code](/documentation/homekit/hmerror/accessoryresponseerror)
- [static var addAccessoryFailed: HMError.Code](/documentation/homekit/hmerror/addaccessoryfailed)
- [static var incompatibleAccessory: HMError.Code](/documentation/homekit/hmerror/incompatibleaccessory)

### Detecting action set errors

- [static var actionInAnotherActionSet: HMError.Code](/documentation/homekit/hmerror/actioninanotheractionset)
- [static var actionSetExecutionFailed: HMError.Code](/documentation/homekit/hmerror/actionsetexecutionfailed)
- [static var actionSetExecutionInProgress: HMError.Code](/documentation/homekit/hmerror/actionsetexecutioninprogress)
- [static var actionSetExecutionPartialSuccess: HMError.Code](/documentation/homekit/hmerror/actionsetexecutionpartialsuccess)
- [static var cannotRemoveBuiltinActionSet: HMError.Code](/documentation/homekit/hmerror/cannotremovebuiltinactionset)
- [static var noActionsInActionSet: HMError.Code](/documentation/homekit/hmerror/noactionsinactionset)
- [static var noRegisteredActionSets: HMError.Code](/documentation/homekit/hmerror/noregisteredactionsets)

### Detecting association errors

- [static var invalidAssociatedServiceType: HMError.Code](/documentation/homekit/hmerror/invalidassociatedservicetype)
- [static var objectAlreadyAssociatedToHome: HMError.Code](/documentation/homekit/hmerror/objectalreadyassociatedtohome)
- [static var objectAssociatedToAnotherHome: HMError.Code](/documentation/homekit/hmerror/objectassociatedtoanotherhome)
- [static var objectNotAssociatedToAnyHome: HMError.Code](/documentation/homekit/hmerror/objectnotassociatedtoanyhome)

### Detecting authorization errors

- [static var invalidOrMissingAuthorizationData: HMError.Code](/documentation/homekit/hmerror/invalidormissingauthorizationdata)
- [static var locationForHomeDisabled: HMError.Code](/documentation/homekit/hmerror/locationforhomedisabled)
- [static var homeAccessNotAuthorized: HMError.Code](/documentation/homekit/hmerror/homeaccessnotauthorized)
- [static var insufficientPrivileges: HMError.Code](/documentation/homekit/hmerror/insufficientprivileges)
- [static var messageAuthenticationFailed: HMError.Code](/documentation/homekit/hmerror/messageauthenticationfailed)
- [static var notAuthorizedForLocationServices: HMError.Code](/documentation/homekit/hmerror/notauthorizedforlocationservices)
- [static var notAuthorizedForMicrophoneAccess: HMError.Code](/documentation/homekit/hmerror/notauthorizedformicrophoneaccess)
- [static var notSignedIntoiCloud: HMError.Code](/documentation/homekit/hmerror/notsignedintoicloud)
- [static var ownershipFailure: HMError.Code](/documentation/homekit/hmerror/ownershipfailure)
- [static var securityFailure: HMError.Code](/documentation/homekit/hmerror/securityfailure)

### Detecting bridge errors

- [static var bridgedAccessoryNotReachable: HMError.Code](/documentation/homekit/hmerror/bridgedaccessorynotreachable)
- [static var cannotRemoveNonBridgeAccessory: HMError.Code](/documentation/homekit/hmerror/cannotremovenonbridgeaccessory)
- [static var cannotUnblockNonBridgeAccessory: HMError.Code](/documentation/homekit/hmerror/cannotunblocknonbridgeaccessory)

### Detecting characteristic errors

- [static var readOnlyCharacteristic: HMError.Code](/documentation/homekit/hmerror/readonlycharacteristic)
- [static var writeOnlyCharacteristic: HMError.Code](/documentation/homekit/hmerror/writeonlycharacteristic)

### Detecting collision errors

- [static var homeWithSimilarNameExists: HMError.Code](/documentation/homekit/hmerror/homewithsimilarnameexists)
- [static var objectWithSimilarNameExists: HMError.Code](/documentation/homekit/hmerror/objectwithsimilarnameexists)
- [static var objectWithSimilarNameExistsInHome: HMError.Code](/documentation/homekit/hmerror/objectwithsimilarnameexistsinhome)
- [static var renameWithSimilarName: HMError.Code](/documentation/homekit/hmerror/renamewithsimilarname)

### Detecting communication errors

- [static var accessDenied: HMError.Code](/documentation/homekit/hmerror/accessdenied)
- [static var accessoryCommunicationFailure: HMError.Code](/documentation/homekit/hmerror/accessorycommunicationfailure)
- [static var accessoryPairingFailed: HMError.Code](/documentation/homekit/hmerror/accessorypairingfailed)
- [static var accessorySentInvalidResponse: HMError.Code](/documentation/homekit/hmerror/accessorysentinvalidresponse)
- [static var clientRequestError: HMError.Code](/documentation/homekit/hmerror/clientrequesterror)
- [static var communicationFailure: HMError.Code](/documentation/homekit/hmerror/communicationfailure)
- [static var dataResetFailure: HMError.Code](/documentation/homekit/hmerror/dataresetfailure)
- [static var timedOutWaitingForAccessory: HMError.Code](/documentation/homekit/hmerror/timedoutwaitingforaccessory)
- [static var partialCommunicationFailure: HMError.Code](/documentation/homekit/hmerror/partialcommunicationfailure)

### Detecting device and discovery errors

- [static var deviceLocked: HMError.Code](/documentation/homekit/hmerror/devicelocked)
- [static var accessoryDiscoveryFailed: HMError.Code](/documentation/homekit/hmerror/accessorydiscoveryfailed)

### Detecting general errors

- [static var alreadyExists: HMError.Code](/documentation/homekit/hmerror/alreadyexists)
- [static var genericError: HMError.Code](/documentation/homekit/hmerror/genericerror)
- [static var incompatibleHomeHub: HMError.Code](/documentation/homekit/hmerror/incompatiblehomehub)
- [static var invalidClass: HMError.Code](/documentation/homekit/hmerror/invalidclass)
- [static var notFound: HMError.Code](/documentation/homekit/hmerror/notfound)
- [static var notificationAlreadyEnabled: HMError.Code](/documentation/homekit/hmerror/notificationalreadyenabled)
- [static var notificationNotSupported: HMError.Code](/documentation/homekit/hmerror/notificationnotsupported)
- [static var operationNotSupported: HMError.Code](/documentation/homekit/hmerror/operationnotsupported)
- [static var unexpectedError: HMError.Code](/documentation/homekit/hmerror/unexpectederror)
- [static var missingEntitlement: HMError.Code](/documentation/homekit/hmerror/missingentitlement)
- [static var referToUserManual: HMError.Code](/documentation/homekit/hmerror/refertousermanual)

### Detecting home and room errors

- [static var maximumAccessoriesOfTypeInHome: HMError.Code](/documentation/homekit/hmerror/maximumaccessoriesoftypeinhome)
- [static var roomForHomeCannotBeInZone: HMError.Code](/documentation/homekit/hmerror/roomforhomecannotbeinzone)
- [static var roomForHomeCannotBeUpdated: HMError.Code](/documentation/homekit/hmerror/roomforhomecannotbeupdated)

### Detecting hub errors

- [static var noHomeHub: HMError.Code](/documentation/homekit/hmerror/nohomehub)
- [static var noCompatibleHomeHub: HMError.Code](/documentation/homekit/hmerror/nocompatiblehomehub)
- [static var incompatibleHomeHub: HMError.Code](/documentation/homekit/hmerror/code/incompatiblehomehub)

### Detecting limit errors

- [static var cannotActivateTriggerTooFarInFuture: HMError.Code](/documentation/homekit/hmerror/cannotactivatetriggertoofarinfuture)
- [static var dateMustBeOnSpecifiedBoundaries: HMError.Code](/documentation/homekit/hmerror/datemustbeonspecifiedboundaries)
- [static var fireDateInPast: HMError.Code](/documentation/homekit/hmerror/firedateinpast)
- [static var invalidMessageSize: HMError.Code](/documentation/homekit/hmerror/invalidmessagesize)
- [static var maximumObjectLimitReached: HMError.Code](/documentation/homekit/hmerror/maximumobjectlimitreached)
- [static var recurrenceTooLarge: HMError.Code](/documentation/homekit/hmerror/recurrencetoolarge)
- [static var recurrenceTooSmall: HMError.Code](/documentation/homekit/hmerror/recurrencetoosmall)
- [static var recurrenceMustBeOnSpecifiedBoundaries: HMError.Code](/documentation/homekit/hmerror/recurrencemustbeonspecifiedboundaries)

### Detecting network errors

- [static var enterpriseNetworkNotSupported: HMError.Code](/documentation/homekit/hmerror/enterprisenetworknotsupported)
- [static var failedToJoinNetwork: HMError.Code](/documentation/homekit/hmerror/failedtojoinnetwork)
- [static var incompatibleNetwork: HMError.Code](/documentation/homekit/hmerror/incompatiblenetwork)
- [static var networkUnavailable: HMError.Code](/documentation/homekit/hmerror/networkunavailable)
- [static var wiFiCredentialGenerationFailed: HMError.Code](/documentation/homekit/hmerror/wificredentialgenerationfailed)

### Detecting operation errors

- [static var operationCancelled: HMError.Code](/documentation/homekit/hmerror/operationcancelled)
- [static var operationInProgress: HMError.Code](/documentation/homekit/hmerror/operationinprogress)
- [static var operationTimedOut: HMError.Code](/documentation/homekit/hmerror/operationtimedout)

### Detecting parameter errors

- [static var invalidParameter: HMError.Code](/documentation/homekit/hmerror/invalidparameter)
- [static var missingParameter: HMError.Code](/documentation/homekit/hmerror/missingparameter)
- [static var nilParameter: HMError.Code](/documentation/homekit/hmerror/nilparameter)
- [static var unconfiguredParameter: HMError.Code](/documentation/homekit/hmerror/unconfiguredparameter)

### Detecting read and write errors

- [static var readWriteFailure: HMError.Code](/documentation/homekit/hmerror/readwritefailure)
- [static var readWritePartialSuccess: HMError.Code](/documentation/homekit/hmerror/readwritepartialsuccess)

### Detecting synchronization errors

- [static var cloudDataSyncInProgress: HMError.Code](/documentation/homekit/hmerror/clouddatasyncinprogress)
- [static var keychainSyncNotEnabled: HMError.Code](/documentation/homekit/hmerror/keychainsyncnotenabled)

### Detecting user errors

- [static var userDeclinedAddingUser: HMError.Code](/documentation/homekit/hmerror/userdeclinedaddinguser)
- [static var userDeclinedRemovingUser: HMError.Code](/documentation/homekit/hmerror/userdeclinedremovinguser)
- [static var userDeclinedInvite: HMError.Code](/documentation/homekit/hmerror/userdeclinedinvite)
- [static var userIDNotEmailAddress: HMError.Code](/documentation/homekit/hmerror/useridnotemailaddress)
- [static var userManagementFailed: HMError.Code](/documentation/homekit/hmerror/usermanagementfailed)

### Detecting value errors

- [static var invalidDataFormatSpecified: HMError.Code](/documentation/homekit/hmerror/invaliddataformatspecified)
- [static var invalidValueType: HMError.Code](/documentation/homekit/hmerror/invalidvaluetype)
- [static var nameContainsProhibitedCharacters: HMError.Code](/documentation/homekit/hmerror/namecontainsprohibitedcharacters)
- [static var nameDoesNotEndWithValidCharacters: HMError.Code](/documentation/homekit/hmerror/namedoesnotendwithvalidcharacters)
- [static var nameDoesNotStartWithValidCharacters: HMError.Code](/documentation/homekit/hmerror/namedoesnotstartwithvalidcharacters)
- [static var stringLongerThanMaximum: HMError.Code](/documentation/homekit/hmerror/stringlongerthanmaximum)
- [static var stringShorterThanMinimum: HMError.Code](/documentation/homekit/hmerror/stringshorterthanminimum)
- [static var valueHigherThanMaximum: HMError.Code](/documentation/homekit/hmerror/valuehigherthanmaximum)
- [static var valueLowerThanMinimum: HMError.Code](/documentation/homekit/hmerror/valuelowerthanminimum)

### Enumerating errors

- [HMError.Code](/documentation/homekit/hmerror/code)

#### Accessory errors

- [case accessoryIsBlocked](/documentation/homekit/hmerror/code/accessoryisblocked)
- [case accessoryIsBusy](/documentation/homekit/hmerror/code/accessoryisbusy)
- [case accessoryIsSuspended](/documentation/homekit/hmerror/code/accessoryissuspended)
- [case accessoryNotReachable](/documentation/homekit/hmerror/code/accessorynotreachable)
- [case accessoryOutOfCompliance](/documentation/homekit/hmerror/code/accessoryoutofcompliance)
- [case accessoryOutOfResources](/documentation/homekit/hmerror/code/accessoryoutofresources)
- [case accessoryPoweredOff](/documentation/homekit/hmerror/code/accessorypoweredoff)
- [case accessoryResponseError](/documentation/homekit/hmerror/code/accessoryresponseerror)
- [case addAccessoryFailed](/documentation/homekit/hmerror/code/addaccessoryfailed)
- [case incompatibleAccessory](/documentation/homekit/hmerror/code/incompatibleaccessory)

#### Action set errors

- [case actionInAnotherActionSet](/documentation/homekit/hmerror/code/actioninanotheractionset)
- [case actionSetExecutionFailed](/documentation/homekit/hmerror/code/actionsetexecutionfailed)
- [case actionSetExecutionInProgress](/documentation/homekit/hmerror/code/actionsetexecutioninprogress)
- [case actionSetExecutionPartialSuccess](/documentation/homekit/hmerror/code/actionsetexecutionpartialsuccess)
- [case cannotRemoveBuiltinActionSet](/documentation/homekit/hmerror/code/cannotremovebuiltinactionset)
- [case noActionsInActionSet](/documentation/homekit/hmerror/code/noactionsinactionset)
- [case noRegisteredActionSets](/documentation/homekit/hmerror/code/noregisteredactionsets)

#### Association errors

- [case invalidAssociatedServiceType](/documentation/homekit/hmerror/code/invalidassociatedservicetype)
- [case objectAlreadyAssociatedToHome](/documentation/homekit/hmerror/code/objectalreadyassociatedtohome)
- [case objectAssociatedToAnotherHome](/documentation/homekit/hmerror/code/objectassociatedtoanotherhome)
- [case objectNotAssociatedToAnyHome](/documentation/homekit/hmerror/code/objectnotassociatedtoanyhome)

#### Authorization errors

- [case invalidOrMissingAuthorizationData](/documentation/homekit/hmerror/code/invalidormissingauthorizationdata)
- [case locationForHomeDisabled](/documentation/homekit/hmerror/code/locationforhomedisabled)
- [case homeAccessNotAuthorized](/documentation/homekit/hmerror/code/homeaccessnotauthorized)
- [case insufficientPrivileges](/documentation/homekit/hmerror/code/insufficientprivileges)
- [case messageAuthenticationFailed](/documentation/homekit/hmerror/code/messageauthenticationfailed)
- [case notAuthorizedForLocationServices](/documentation/homekit/hmerror/code/notauthorizedforlocationservices)
- [case notAuthorizedForMicrophoneAccess](/documentation/homekit/hmerror/code/notauthorizedformicrophoneaccess)
- [case notSignedIntoiCloud](/documentation/homekit/hmerror/code/notsignedintoicloud)
- [case ownershipFailure](/documentation/homekit/hmerror/code/ownershipfailure)
- [case securityFailure](/documentation/homekit/hmerror/code/securityfailure)

#### Bridge errors

- [case bridgedAccessoryNotReachable](/documentation/homekit/hmerror/code/bridgedaccessorynotreachable)
- [case cannotRemoveNonBridgeAccessory](/documentation/homekit/hmerror/code/cannotremovenonbridgeaccessory)
- [case cannotUnblockNonBridgeAccessory](/documentation/homekit/hmerror/code/cannotunblocknonbridgeaccessory)

#### Characteristic errors

- [case readOnlyCharacteristic](/documentation/homekit/hmerror/code/readonlycharacteristic)
- [case writeOnlyCharacteristic](/documentation/homekit/hmerror/code/writeonlycharacteristic)

#### Collision errors

- [case homeWithSimilarNameExists](/documentation/homekit/hmerror/code/homewithsimilarnameexists)
- [case objectWithSimilarNameExists](/documentation/homekit/hmerror/code/objectwithsimilarnameexists)
- [case objectWithSimilarNameExistsInHome](/documentation/homekit/hmerror/code/objectwithsimilarnameexistsinhome)
- [case renameWithSimilarName](/documentation/homekit/hmerror/code/renamewithsimilarname)

#### Communication errors

- [case accessDenied](/documentation/homekit/hmerror/code/accessdenied)
- [case accessoryCommunicationFailure](/documentation/homekit/hmerror/code/accessorycommunicationfailure)
- [case accessoryPairingFailed](/documentation/homekit/hmerror/code/accessorypairingfailed)
- [case accessorySentInvalidResponse](/documentation/homekit/hmerror/code/accessorysentinvalidresponse)
- [case clientRequestError](/documentation/homekit/hmerror/code/clientrequesterror)
- [case communicationFailure](/documentation/homekit/hmerror/code/communicationfailure)
- [case dataResetFailure](/documentation/homekit/hmerror/code/dataresetfailure)
- [case timedOutWaitingForAccessory](/documentation/homekit/hmerror/code/timedoutwaitingforaccessory)

#### Device and discovery errors

- [case deviceLocked](/documentation/homekit/hmerror/code/devicelocked)
- [case accessoryDiscoveryFailed](/documentation/homekit/hmerror/code/accessorydiscoveryfailed)

#### General errors

- [case alreadyExists](/documentation/homekit/hmerror/code/alreadyexists)
- [case genericError](/documentation/homekit/hmerror/code/genericerror)
- [static var incompatibleHomeHub: HMError.Code](/documentation/homekit/hmerror/code/incompatiblehomehub)
- [case invalidClass](/documentation/homekit/hmerror/code/invalidclass)
- [case notFound](/documentation/homekit/hmerror/code/notfound)
- [case notificationAlreadyEnabled](/documentation/homekit/hmerror/code/notificationalreadyenabled)
- [case notificationNotSupported](/documentation/homekit/hmerror/code/notificationnotsupported)
- [case operationNotSupported](/documentation/homekit/hmerror/code/operationnotsupported)
- [case unexpectedError](/documentation/homekit/hmerror/code/unexpectederror)
- [case missingEntitlement](/documentation/homekit/hmerror/code/missingentitlement)
- [case referToUserManual](/documentation/homekit/hmerror/code/refertousermanual)

#### Home and room errors

- [case maximumAccessoriesOfTypeInHome](/documentation/homekit/hmerror/code/maximumaccessoriesoftypeinhome)
- [case roomForHomeCannotBeInZone](/documentation/homekit/hmerror/code/roomforhomecannotbeinzone)
- [case roomForHomeCannotBeUpdated](/documentation/homekit/hmerror/code/roomforhomecannotbeupdated)

#### Hub errors

- [case noHomeHub](/documentation/homekit/hmerror/code/nohomehub)
- [case noCompatibleHomeHub](/documentation/homekit/hmerror/code/nocompatiblehomehub)

#### Limit errors

- [case cannotActivateTriggerTooFarInFuture](/documentation/homekit/hmerror/code/cannotactivatetriggertoofarinfuture)
- [case dateMustBeOnSpecifiedBoundaries](/documentation/homekit/hmerror/code/datemustbeonspecifiedboundaries)
- [case fireDateInPast](/documentation/homekit/hmerror/code/firedateinpast)
- [case invalidMessageSize](/documentation/homekit/hmerror/code/invalidmessagesize)
- [case maximumObjectLimitReached](/documentation/homekit/hmerror/code/maximumobjectlimitreached)
- [case recurrenceTooLarge](/documentation/homekit/hmerror/code/recurrencetoolarge)
- [case recurrenceTooSmall](/documentation/homekit/hmerror/code/recurrencetoosmall)
- [case recurrenceMustBeOnSpecifiedBoundaries](/documentation/homekit/hmerror/code/recurrencemustbeonspecifiedboundaries)

#### Network errors

- [case enterpriseNetworkNotSupported](/documentation/homekit/hmerror/code/enterprisenetworknotsupported)
- [case failedToJoinNetwork](/documentation/homekit/hmerror/code/failedtojoinnetwork)
- [case incompatibleNetwork](/documentation/homekit/hmerror/code/incompatiblenetwork)
- [case networkUnavailable](/documentation/homekit/hmerror/code/networkunavailable)
- [case wiFiCredentialGenerationFailed](/documentation/homekit/hmerror/code/wificredentialgenerationfailed)

#### Operation errors

- [case operationCancelled](/documentation/homekit/hmerror/code/operationcancelled)
- [case operationInProgress](/documentation/homekit/hmerror/code/operationinprogress)
- [case operationTimedOut](/documentation/homekit/hmerror/code/operationtimedout)

#### Parameter errors

- [case invalidParameter](/documentation/homekit/hmerror/code/invalidparameter)
- [case missingParameter](/documentation/homekit/hmerror/code/missingparameter)
- [case nilParameter](/documentation/homekit/hmerror/code/nilparameter)
- [case unconfiguredParameter](/documentation/homekit/hmerror/code/unconfiguredparameter)

#### Read and write errors

- [case readWriteFailure](/documentation/homekit/hmerror/code/readwritefailure)
- [case readWritePartialSuccess](/documentation/homekit/hmerror/code/readwritepartialsuccess)

#### Synchronization errors

- [case cloudDataSyncInProgress](/documentation/homekit/hmerror/code/clouddatasyncinprogress)
- [case keychainSyncNotEnabled](/documentation/homekit/hmerror/code/keychainsyncnotenabled)

#### User errors

- [case userDeclinedAddingUser](/documentation/homekit/hmerror/code/userdeclinedaddinguser)
- [case userDeclinedRemovingUser](/documentation/homekit/hmerror/code/userdeclinedremovinguser)
- [case userDeclinedInvite](/documentation/homekit/hmerror/code/userdeclinedinvite)
- [case userIDNotEmailAddress](/documentation/homekit/hmerror/code/useridnotemailaddress)
- [case userManagementFailed](/documentation/homekit/hmerror/code/usermanagementfailed)

#### Value errors

- [case invalidDataFormatSpecified](/documentation/homekit/hmerror/code/invaliddataformatspecified)
- [case invalidValueType](/documentation/homekit/hmerror/code/invalidvaluetype)
- [case nameContainsProhibitedCharacters](/documentation/homekit/hmerror/code/namecontainsprohibitedcharacters)
- [case nameDoesNotEndWithValidCharacters](/documentation/homekit/hmerror/code/namedoesnotendwithvalidcharacters)
- [case nameDoesNotStartWithValidCharacters](/documentation/homekit/hmerror/code/namedoesnotstartwithvalidcharacters)
- [case stringLongerThanMaximum](/documentation/homekit/hmerror/code/stringlongerthanmaximum)
- [case stringShorterThanMinimum](/documentation/homekit/hmerror/code/stringshorterthanminimum)
- [case valueHigherThanMaximum](/documentation/homekit/hmerror/code/valuehigherthanmaximum)
- [case valueLowerThanMinimum](/documentation/homekit/hmerror/code/valuelowerthanminimum)

#### Enumeration Cases

- [case partialCommunicationFailure](/documentation/homekit/hmerror/code/partialcommunicationfailure)
- [case homeUpgradeRequired](/documentation/homekit/hmerror/code/homeupgraderequired)

#### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmerror/code/init(rawvalue:))

### Type Properties

- [static var errorDomain: String](/documentation/homekit/hmerror/errordomain)
- [static var homeUpgradeRequired: HMError.Code](/documentation/homekit/hmerror/homeupgraderequired)
- [let HMErrorDomain: String](/documentation/homekit/hmerrordomain)
- [HMError.Code](/documentation/homekit/hmerror/code)

### Accessory errors

- [case accessoryIsBlocked](/documentation/homekit/hmerror/code/accessoryisblocked)
- [case accessoryIsBusy](/documentation/homekit/hmerror/code/accessoryisbusy)
- [case accessoryIsSuspended](/documentation/homekit/hmerror/code/accessoryissuspended)
- [case accessoryNotReachable](/documentation/homekit/hmerror/code/accessorynotreachable)
- [case accessoryOutOfCompliance](/documentation/homekit/hmerror/code/accessoryoutofcompliance)
- [case accessoryOutOfResources](/documentation/homekit/hmerror/code/accessoryoutofresources)
- [case accessoryPoweredOff](/documentation/homekit/hmerror/code/accessorypoweredoff)
- [case accessoryResponseError](/documentation/homekit/hmerror/code/accessoryresponseerror)
- [case addAccessoryFailed](/documentation/homekit/hmerror/code/addaccessoryfailed)
- [case incompatibleAccessory](/documentation/homekit/hmerror/code/incompatibleaccessory)

### Action set errors

- [case actionInAnotherActionSet](/documentation/homekit/hmerror/code/actioninanotheractionset)
- [case actionSetExecutionFailed](/documentation/homekit/hmerror/code/actionsetexecutionfailed)
- [case actionSetExecutionInProgress](/documentation/homekit/hmerror/code/actionsetexecutioninprogress)
- [case actionSetExecutionPartialSuccess](/documentation/homekit/hmerror/code/actionsetexecutionpartialsuccess)
- [case cannotRemoveBuiltinActionSet](/documentation/homekit/hmerror/code/cannotremovebuiltinactionset)
- [case noActionsInActionSet](/documentation/homekit/hmerror/code/noactionsinactionset)
- [case noRegisteredActionSets](/documentation/homekit/hmerror/code/noregisteredactionsets)

### Association errors

- [case invalidAssociatedServiceType](/documentation/homekit/hmerror/code/invalidassociatedservicetype)
- [case objectAlreadyAssociatedToHome](/documentation/homekit/hmerror/code/objectalreadyassociatedtohome)
- [case objectAssociatedToAnotherHome](/documentation/homekit/hmerror/code/objectassociatedtoanotherhome)
- [case objectNotAssociatedToAnyHome](/documentation/homekit/hmerror/code/objectnotassociatedtoanyhome)

### Authorization errors

- [case invalidOrMissingAuthorizationData](/documentation/homekit/hmerror/code/invalidormissingauthorizationdata)
- [case locationForHomeDisabled](/documentation/homekit/hmerror/code/locationforhomedisabled)
- [case homeAccessNotAuthorized](/documentation/homekit/hmerror/code/homeaccessnotauthorized)
- [case insufficientPrivileges](/documentation/homekit/hmerror/code/insufficientprivileges)
- [case messageAuthenticationFailed](/documentation/homekit/hmerror/code/messageauthenticationfailed)
- [case notAuthorizedForLocationServices](/documentation/homekit/hmerror/code/notauthorizedforlocationservices)
- [case notAuthorizedForMicrophoneAccess](/documentation/homekit/hmerror/code/notauthorizedformicrophoneaccess)
- [case notSignedIntoiCloud](/documentation/homekit/hmerror/code/notsignedintoicloud)
- [case ownershipFailure](/documentation/homekit/hmerror/code/ownershipfailure)
- [case securityFailure](/documentation/homekit/hmerror/code/securityfailure)

### Bridge errors

- [case bridgedAccessoryNotReachable](/documentation/homekit/hmerror/code/bridgedaccessorynotreachable)
- [case cannotRemoveNonBridgeAccessory](/documentation/homekit/hmerror/code/cannotremovenonbridgeaccessory)
- [case cannotUnblockNonBridgeAccessory](/documentation/homekit/hmerror/code/cannotunblocknonbridgeaccessory)

### Characteristic errors

- [case readOnlyCharacteristic](/documentation/homekit/hmerror/code/readonlycharacteristic)
- [case writeOnlyCharacteristic](/documentation/homekit/hmerror/code/writeonlycharacteristic)

### Collision errors

- [case homeWithSimilarNameExists](/documentation/homekit/hmerror/code/homewithsimilarnameexists)
- [case objectWithSimilarNameExists](/documentation/homekit/hmerror/code/objectwithsimilarnameexists)
- [case objectWithSimilarNameExistsInHome](/documentation/homekit/hmerror/code/objectwithsimilarnameexistsinhome)
- [case renameWithSimilarName](/documentation/homekit/hmerror/code/renamewithsimilarname)

### Communication errors

- [case accessDenied](/documentation/homekit/hmerror/code/accessdenied)
- [case accessoryCommunicationFailure](/documentation/homekit/hmerror/code/accessorycommunicationfailure)
- [case accessoryPairingFailed](/documentation/homekit/hmerror/code/accessorypairingfailed)
- [case accessorySentInvalidResponse](/documentation/homekit/hmerror/code/accessorysentinvalidresponse)
- [case clientRequestError](/documentation/homekit/hmerror/code/clientrequesterror)
- [case communicationFailure](/documentation/homekit/hmerror/code/communicationfailure)
- [case dataResetFailure](/documentation/homekit/hmerror/code/dataresetfailure)
- [case timedOutWaitingForAccessory](/documentation/homekit/hmerror/code/timedoutwaitingforaccessory)

### Device and discovery errors

- [case deviceLocked](/documentation/homekit/hmerror/code/devicelocked)
- [case accessoryDiscoveryFailed](/documentation/homekit/hmerror/code/accessorydiscoveryfailed)

### General errors

- [case alreadyExists](/documentation/homekit/hmerror/code/alreadyexists)
- [case genericError](/documentation/homekit/hmerror/code/genericerror)
- [static var incompatibleHomeHub: HMError.Code](/documentation/homekit/hmerror/code/incompatiblehomehub)
- [case invalidClass](/documentation/homekit/hmerror/code/invalidclass)
- [case notFound](/documentation/homekit/hmerror/code/notfound)
- [case notificationAlreadyEnabled](/documentation/homekit/hmerror/code/notificationalreadyenabled)
- [case notificationNotSupported](/documentation/homekit/hmerror/code/notificationnotsupported)
- [case operationNotSupported](/documentation/homekit/hmerror/code/operationnotsupported)
- [case unexpectedError](/documentation/homekit/hmerror/code/unexpectederror)
- [case missingEntitlement](/documentation/homekit/hmerror/code/missingentitlement)
- [case referToUserManual](/documentation/homekit/hmerror/code/refertousermanual)

### Home and room errors

- [case maximumAccessoriesOfTypeInHome](/documentation/homekit/hmerror/code/maximumaccessoriesoftypeinhome)
- [case roomForHomeCannotBeInZone](/documentation/homekit/hmerror/code/roomforhomecannotbeinzone)
- [case roomForHomeCannotBeUpdated](/documentation/homekit/hmerror/code/roomforhomecannotbeupdated)

### Hub errors

- [case noHomeHub](/documentation/homekit/hmerror/code/nohomehub)
- [case noCompatibleHomeHub](/documentation/homekit/hmerror/code/nocompatiblehomehub)

### Limit errors

- [case cannotActivateTriggerTooFarInFuture](/documentation/homekit/hmerror/code/cannotactivatetriggertoofarinfuture)
- [case dateMustBeOnSpecifiedBoundaries](/documentation/homekit/hmerror/code/datemustbeonspecifiedboundaries)
- [case fireDateInPast](/documentation/homekit/hmerror/code/firedateinpast)
- [case invalidMessageSize](/documentation/homekit/hmerror/code/invalidmessagesize)
- [case maximumObjectLimitReached](/documentation/homekit/hmerror/code/maximumobjectlimitreached)
- [case recurrenceTooLarge](/documentation/homekit/hmerror/code/recurrencetoolarge)
- [case recurrenceTooSmall](/documentation/homekit/hmerror/code/recurrencetoosmall)
- [case recurrenceMustBeOnSpecifiedBoundaries](/documentation/homekit/hmerror/code/recurrencemustbeonspecifiedboundaries)

### Network errors

- [case enterpriseNetworkNotSupported](/documentation/homekit/hmerror/code/enterprisenetworknotsupported)
- [case failedToJoinNetwork](/documentation/homekit/hmerror/code/failedtojoinnetwork)
- [case incompatibleNetwork](/documentation/homekit/hmerror/code/incompatiblenetwork)
- [case networkUnavailable](/documentation/homekit/hmerror/code/networkunavailable)
- [case wiFiCredentialGenerationFailed](/documentation/homekit/hmerror/code/wificredentialgenerationfailed)

### Operation errors

- [case operationCancelled](/documentation/homekit/hmerror/code/operationcancelled)
- [case operationInProgress](/documentation/homekit/hmerror/code/operationinprogress)
- [case operationTimedOut](/documentation/homekit/hmerror/code/operationtimedout)

### Parameter errors

- [case invalidParameter](/documentation/homekit/hmerror/code/invalidparameter)
- [case missingParameter](/documentation/homekit/hmerror/code/missingparameter)
- [case nilParameter](/documentation/homekit/hmerror/code/nilparameter)
- [case unconfiguredParameter](/documentation/homekit/hmerror/code/unconfiguredparameter)

### Read and write errors

- [case readWriteFailure](/documentation/homekit/hmerror/code/readwritefailure)
- [case readWritePartialSuccess](/documentation/homekit/hmerror/code/readwritepartialsuccess)

### Synchronization errors

- [case cloudDataSyncInProgress](/documentation/homekit/hmerror/code/clouddatasyncinprogress)
- [case keychainSyncNotEnabled](/documentation/homekit/hmerror/code/keychainsyncnotenabled)

### User errors

- [case userDeclinedAddingUser](/documentation/homekit/hmerror/code/userdeclinedaddinguser)
- [case userDeclinedRemovingUser](/documentation/homekit/hmerror/code/userdeclinedremovinguser)
- [case userDeclinedInvite](/documentation/homekit/hmerror/code/userdeclinedinvite)
- [case userIDNotEmailAddress](/documentation/homekit/hmerror/code/useridnotemailaddress)
- [case userManagementFailed](/documentation/homekit/hmerror/code/usermanagementfailed)

### Value errors

- [case invalidDataFormatSpecified](/documentation/homekit/hmerror/code/invaliddataformatspecified)
- [case invalidValueType](/documentation/homekit/hmerror/code/invalidvaluetype)
- [case nameContainsProhibitedCharacters](/documentation/homekit/hmerror/code/namecontainsprohibitedcharacters)
- [case nameDoesNotEndWithValidCharacters](/documentation/homekit/hmerror/code/namedoesnotendwithvalidcharacters)
- [case nameDoesNotStartWithValidCharacters](/documentation/homekit/hmerror/code/namedoesnotstartwithvalidcharacters)
- [case stringLongerThanMaximum](/documentation/homekit/hmerror/code/stringlongerthanmaximum)
- [case stringShorterThanMinimum](/documentation/homekit/hmerror/code/stringshorterthanminimum)
- [case valueHigherThanMaximum](/documentation/homekit/hmerror/code/valuehigherthanmaximum)
- [case valueLowerThanMinimum](/documentation/homekit/hmerror/code/valuelowerthanminimum)

### Enumeration Cases

- [case partialCommunicationFailure](/documentation/homekit/hmerror/code/partialcommunicationfailure)
- [case homeUpgradeRequired](/documentation/homekit/hmerror/code/homeupgraderequired)

### Initializers

- [init?(rawValue: Int)](/documentation/homekit/hmerror/code/init(rawvalue:))
- [HMErrorBlock](/documentation/homekit/hmerrorblock)

## Classes

- [HMAccessorySetupPayload](/documentation/homekit/hmaccessorysetuppayload)

### Creating a Payload

- [init?(url: URL?)](/documentation/homekit/hmaccessorysetuppayload/init(url:))
- [init?(url: URL, ownershipToken: HMAccessoryOwnershipToken?)](/documentation/homekit/hmaccessorysetuppayload/init(url:ownershiptoken:))
- [HMAccessoryOwnershipToken](/documentation/homekit/hmaccessoryownershiptoken)

#### Creating a Token

- [init?(data: Data)](/documentation/homekit/hmaccessoryownershiptoken/init(data:))

---

*Extracted by [sosumi.ai](https://sosumi.ai) - Making Apple docs AI-readable.*
*This is unofficial content. All documentation belongs to Apple Inc.*
